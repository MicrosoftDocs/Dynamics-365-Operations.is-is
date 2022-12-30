---
title: Stækkunarhæfni á fínstillingu áætlanagerðar
description: Þessi grein lýsir aðstæðum stækkunarhæfni sem eru studdar í fínstillingu áætlanagerðar.
author: t-benebo
ms.date: 08/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-07-07
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 7d649110959e6bcfdaeb32dd53c55dbc446ed1be
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857545"
---
# <a name="planning-optimization-extensibility"></a>Stækkunarhæfni á fínstillingu áætlanagerðar

[!include [banner](../../includes/banner.md)]

Þessi grein lýsir aðstæðum stækkunarhæfni sem eru tengjast aðaláætlanagerð og eru studdar í fínstillingu áætlanagerðar. Þessir möguleikar eru í boði frá og með Microsoft Dynamics 365 Supply Chain Management útgáfu 10.0.13.

## <a name="custom-processing-when-master-planning-is-completed"></a>Sérsniðin vinnsla þegar áætlanagerð lýkur

Í algengustu aðstæðum stækkunarhæfni í fínstillingu áætlanagerðar er sérsniðin vinnsla gerð eftir að áætlunin hefur verið uppfærð. Til dæmis gætir þú bætt dálki við töflu áætlaðra pantana (`ReqPO`) eða þú gætir viljað ná í tölfræðilegar upplýsingar úr myndaðri áætlun. Helsti punktur stækkunarhæfni sem gerir þessar aðstæður mögulegar er `jobCompletedSuccessfully` aðferðin í `MpsMasterPlanningEvents` klasanum.

```X++
public static void jobCompletedSuccessfully(MpsMasterPlanningJobCompletedSuccessfullyEventArgs _args)
```

Hér er dæmi um viðbót sem stillir sérstilltan `CstmOrderPriority` reit í áætlaðri pöntun.

```X++
[ExtensionOf(classStr(MpsMasterPlanningEvents))]
public static final class MpsMasterPlanningEvents_Cstm_Extension
{
    public static void jobCompletedSuccessfully(MpsMasterPlanningJobCompletedSuccessfullyEventArgs _args)
    {
        ttsbegin;

        var affectedPlannedOrdersQuery = _args.parmPostProcessingQueryBuilder().buildAffectedPlannedOrdersQuery();
        var affectedPlannedOrdersQueryRun = new QueryRun(affectedPlannedOrdersQuery);

        while (affectedPlannedOrdersQueryRun.next())
        {
            ReqPO reqPO = affectedPlannedOrdersQueryRun.get(tableNum(ReqPO));
            reqPO.selectForUpdate(true);
            reqPO.CstmOrderPriority = reqPO.ReqDate - systemDateGet() < 7 ? CstmPlannedOrderPriority::Urgent : CstmPlannedOrderPriority::Regular;
            reqPO.doUpdate();
        }

        ttscommit;

        next jobCompletedSuccessfully(_args);
    }

}
```

Þegar þú bætir við sérsniðnum rökum skaltu hafa eftirfarandi takmarkanir og bestu venjur í huga:

- Kallað er á aðferðina `jobCompletedSuccessfully` utan við umfang færslunnar. Þess vegna er áætlunin þegar sýnileg notandanum þegar sérsniðin rök byrja keyrslu. Ef sérstillingin þín stillir viðbótarreiti í áætluðum pöntunum er mikilvægt að þú látir notendur vita að gildi þessara reita verða að lokum stöðug (þau gætu með öðrum orðum úrelst strax eftir að vinnu aðaláætlanagerðar lýkur).
- Annað verk aðaláætlanagerðar getur hafist þegar kallað er á `jobCompletedSuccessfully` aðferðina. Nýja verkið getur haft áhrif á heildaráætlunina eða hluta hennar. Nýja verkið gæti uppfært eða eytt sömu áætluðu pöntunum eða þarfafærslum sem voru stofnaðar eða uppfærðar sem hluti af verki aðaláætlanagerðar sem var meðhöndlað í `jobCompletedSuccessfully`. Undantekningar uppfærsluárekstra þarf að meðhöndla þegar þetta tilvik er stækkað.
- Forðastu að nota umfang einnar færslu þegar þú stækkar þessa aðferð. Ein aðaláætlunarkeyrsla getur skapað milljónir þarfafærslna og hundruð þúsunda áætlaðra pantana. Ef allar þessar færslur og áætlaðar pantanir afgreiddar í umfangi einnar færslu munu margar SQL-læsingar eiga sér stað og loka á aðra ferla áætlanagerðar. Auk þess, ef færslunni er haldið í langan tíma, munu „skuggafærslur“ verða stofnaðar í SQL-gagnagrunninum. Skuggafærslur munu hafa neikvæð áhrif á alla ferla í kerfinu.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]