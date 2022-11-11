---
title: Nota verkflæði til að haga starfsmannaupplýsingum
description: Þessi grein útskýrir hvernig þú getur notað verkflæði til að stjórna starfsmannaupplýsingum.
author: twheeloc
ms.date: 11/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: dbbbb0ee807cb65fa4f4f9a29cc4a2b6b045b08c
ms.sourcegitcommit: 2b654e60e2553a5835ab5790db4ccfa58828fae7
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/08/2022
ms.locfileid: "9750735"
---
# <a name="use-workflows-to-manage-employee-information"></a>Nota verkflæði til að haga starfsmannaupplýsingum

[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Í þessari grein er útskýrt hvernig hægt er að nota verkflæðisgetu fyrir mannauð til að stjórna upplýsingum starfsmanns. Til dæmis er hægt að tengja verkflæði við stöðu og skilgreina samþykkisverkflæði sem er ræst þegar starfsmenn breyta skráningu sinni.

Verkflæðisgeta fyrir mannauð veitir fjölda verkflæða fyrir stjórnun mannauðsaðgerða. Þar að auki eru fjölmargir valkostir tiltækir svo að hægt er að breyta tilteknum verkflæðum og tengja þau við skýrslustigveldi. Verkflæði eru tiltæk til að hjálpa til við að stjórna breytingum á nokkrum tegundum starfsmannaupplýsinga. Hægt er að tengja verkflæði við stöðu. Síðan, ef starfsmenn breyta skráningu sinni, er verkflæði hafið sem þarfnast samþykkis áður en nýju upplýsingarnar eru vistaðar. Verkflæði eru fyrirfram skilgreind fyrir eftirfarandi tegundir upplýsinga til að hjálpa þér að stjórna breytingum á skilvirkan hátt og halda gögnum starfsmanna þinna nákvæmum:

-   Auðkennisnúmer
-   Námskeið
-   Menntun
-   Mynd
-   Lánsvörur
-   Starfsreynsla
-   Verkreynsla
-   Hæfni
-   Ábyrgðarstöður
-   Mannauðsaðgerðir
-   Námskeiðsskráning

Þegar starfsmenn eru ráðnir, fluttir eða hættir getur verkflæðið innihaldið endurskoðunarferli. Þannig er hægt að endurskoða skjal eða skilgreina skilmála aðgerða sem hluta af verkflæðinu. Þegar endurskoðunarferli er lokið er skjalið eða aðgerð lokið og verkflæðið færist yfir í endanlegt samþykktarskref.

## <a name="associate-a-workflow-with-a-position-hierarchy"></a>Tengja verkflæði við stigveldi stöðu

Þú getur tengt verkflæði við hvaða stöðustigveldi sem þú stillir. Tvær stigveldisgerðir eru notaðar fyrir verkflæðisleiðingu: **Stjórnandi** og **Stillanlegt**.

- A **Stjórnandi** stigveldi táknar skýrslugerð fyrirtækisins eða stofnunarinnar. Fyrir frekari upplýsingar um þessa stigveldistegund, sjá [Skýrslur til stöðu](hr-personnel-positions.md#reports-to-position).
- A **Stillanlegt** stigveldi táknar fylki eða sérsniðið stigveldi. Fyrir frekari upplýsingar um þessa stigveldistegund, sjá [Sambönd](hr-personnel-positions.md#relationships).

### <a name="managerial-hierarchy-example"></a>Dæmi um stjórnunarstigveldi

Þú gætir stillt verkflæði þannig að þegar starfsmaður sendir inn innkaupabeiðni fyrir nýja tölvu sé beiðninni beint til yfirmanns starfsmanns og yfirmanns sleppastigs. Þegar þú stillir verkflæðisskrefið skaltu stilla **Tegund verkefnis** sviði til **Stigveldi**. The **Tegund stigveldis** flipinn verður þá aðgengilegur. Fyrir þetta dæmi skaltu velja **Stjórnandi** stigveldi.

### <a name="configurable-hierarchy-example"></a>Stillanlegt stigveldisdæmi

Ef staða er tengd við fylkisskýrslustigveldi er hægt að stilla verkflæði sem beinir útgjöldum fyrir tiltekið verkefni til verkefnastjóra í stað yfirmanns starfsmanns. Í þessu tilviki skaltu stilla **Tegund verkefnis** sviði til **Stigveldi**. Síðan, á **Tegund stigveldis** flipann, veldu **Stillanlegt** stigveldi. Eftir að verkflæðið er sett upp skaltu velja **Félagi** stigveldi á **Uppsetning vinnuflæðis** síðu til að velja stigveldið sem ætti að nota fyrir verkflæðisleiðina.

> [!IMPORTANT]
> Þegar skjal, færslu eða aðalskrá er lögð fram til samþykkis verkflæðis, verður aðalstaða sendanda notuð til að ákvarða til hvers skjalið ætti að beina næst.

### <a name="hierarchy-setting-in-workflow-parameters"></a>Stigveldisstilling í færibreytum verkflæðis

1. Á **Verkflæðisbreytur** síðu, farðu á **Stigveldisleiðsögn**.
2. Sjálfgefið er **Notaðu stöðustigveldi** valkostur er stilltur á **Nei**. Í þessu tilviki mun verkflæðið nota aðalstöðu starfsmannsins þegar það vafrar um stigveldið. Stilltu valkostinn á **Já** til að láta verkflæðið nota foreldri stöðunnar þegar það vafrar um stigveldið.

### <a name="additional-example"></a>Viðbótar dæmi 

Starfsmaður Grace Sturman hefur tvær stöður: ráðgjafi og þjálfari. Aðal staða Graces er þjálfari. Þegar hún er ekki að þjálfa nýja starfsmenn er hún tiltæk í ráðgjafarstörf. Í gegnum aðalstöðu sína heyrir Grace undir Claire, starfsmannastjóra. Claire skýrir frá Charlie. Fyrir ráðgjafastöðu sína hefur Grace mörg punktalínusambönd, allt eftir verkefninu.

Fyrirtæki Grace býr til vinnuflæðisleiðarreglur sem byggjast á a **Stillanlegt** stigveldi (fylki/verkefnabundið stigveldi). Þetta stigveldi notar ráðgjafastöðu Grace. Ef **Notaðu stöðustigveldi** valkostur er stilltur á **Nei**, þegar skjal er sent til Grace til samþykkis hennar, mun verkflæðið skoða aðalstöðu hennar (þjálfara) til að ákvarða hvert skjalið ætti að beina næst. Í þessu tilviki verður það flutt fyrst til Claire og síðan til Charlie. Ef valkosturinn er stilltur á **Já**, og verkflæðið notar a **Stillanlegt** stigveldi mun verkflæðið líta á ráðgjafastöðu Grace og skýrslutengslin til að ákvarða hvert skjalið ætti að beina næst.

### <a name="configure-a-human-resources-workflow"></a>Grunnstilla verkflæði fyrir mannauð
Til að grunnstilla grunnverkflæði sem ræsist þegar starfsmenn biðja um breytingar á persónuupplýsingum sínum, skal fylgja þessum skrefum.

1.  Á **Starfsflæði mannauðs** síðu, veldu **Nýtt**.
2.  Í listanum yfir tiltæk verkflæði velurðu **Auðkennisnúmer**.
3.  Veldu **Hlaupa** til að opna verkflæðishönnuðinn og sláðu síðan inn notandanafn og lykilorð.
4.  Færðu **Samþykkja kennitölu** þáttur af lista yfir verkflæðisþætti yfir á hönnuðarstriga.
5.  Tengja samþykktareininguna við **Ræsa** og **Ljúka**.
6.  Tvísmelltu (eða tvísmelltu) **Samþykkja þátt**, veldu og haltu inni (eða hægrismelltu) og veldu síðan **Eiginleikar**.
7.  Fylgja skal þessum skrefum til að bæta við vöruleiðbeiningum:

    1.  Veldu **Úthlutun** og veldu síðan **Stigveldi** undir úthlutunargerð.
    2.  Undir valinu **Stigveldi** skal velja **Skilgreinanleg stigveldi**.
    3.  Bæta við stöðvunarskilyrði og loka síðunni.

8.  Ljúktu við allar viðbótarleiðbeiningar.
9.  Veljið **Vista og loka**. Virkja nýja verkflæðið þegar svarglugginn opnast og velja **Gera virka**.
10. Fara í **Mannauð** &gt; **Stöður** &gt; **Stigveldisgerðir stöðu**.
11. Velja **Fylki**.
12. Bæta við verkflæðinu **Auðkennisnúmer starfsmanns** við listann.

## <a name="additional-resources"></a>Frekari upplýsingar

[Skoða og hafa umsjón með breytingum á aðsetri](hr-personnel-view-address-changes.md) 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
