---
title: Nýir notendur stofnaðir
description: Notendur eru innri starfsmenn fyrirtækisins, eða ytri viðskiptavinir og lánardrottnar sem þurfa aðgang að kerfinu til að framkvæma vinnslum.
author: peakerbl
manager: AnnBe
ms.date: 01/12/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f30f6292ed0a4de93ba75341bc917f9205c4e39c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5571054"
---
# <a name="create-new-users"></a>Búa til nýja notendur

[!include [banner](../../includes/banner.md)]

Áður en hægt er opna Finance and Operations-forrit þarf fyrst að bæta notanda við síðuna **Notendur** (**Kerfisstjórnun \> Notendur \> Notendur**). Notendur samanstanda af innri starfsmönnum fyrirtækisins eða ytri viðskiptavinum og lánardrottnum. Hægt er að flytja notendur inn eða bæta þeim við handvirkt. Allir notendur verða að vera með tilskilinn leyfi fyrir tilhlýðilega notkun.

Upplýsingar um hvernig á að kaupa og veita leyfi fyrir Finance and Operations-forrit er að finna í [Leyfishandbók Microsoft Dynamics 365](https://go.microsoft.com/fwlink/?LinkId=866544&amp;clcid=0x409).

## <a name="assign-a-license-to-a-user"></a>Úthluta leyfi til notanda
Kerfisstjórar geta það [úthluta leyfi til notenda](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) í [stjórnunarmiðstöð Microsoft 365](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).

## <a name="add-an-external-user-in-azure-ad-and-assign-a-license"></a>Bæta ytri notanda við Azure AD og úthluta leyfi 
Ytri notendur verða að koma fram í notendaskrá biðlara (Azure Active Directory (Azure AD)) þannig að hægt sé að úthluta þeim leyfum. Þessum utanaðkomandi notendum ætti að bæta við leigjandann í Azure AD sem gestanotendum og úthluta þeim síðan viðeigandi leyfum. Krafa Finance and Operations-forrita er að fyrirtæki gestanotenda verði að nota Azure AD. Nánari upplýsingar er að finna í [Bæta Azure Active Directory B2B samvinnunotendum við í Azure-gáttinni](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).

## <a name="import-new-users-from-azure-ad"></a>Flytja inn nýja notendur úr Azure AD 
1. Farið í **Kerfisstjórnun** \> **Notandi** \> **Notendur**.
2. Á Aðgerðasvæðinu skal velja **Flytja inn notendur**.
3. Veljið notendurnar sem á að flytja inn. Listinn inniheldur Azure AD notendur sem eru ekki notendur í þessu umhverfi.
4. Veldu **Flytja inn notendur**.
5. Veljið **Loka**.

> [!NOTE]
> Gildið fyrir reitinn **Fyrirtæki** verður stillt samkvæmt núverandi lotufyrirtæki fyrir stjórnandann. Eftir innflutning þarf að úthluta hlutverkum og fyrirtækjum eins og við á. Nánari upplýsingar er að finna á [Úthluta notendum á öryggishlutverk](assign-users-security-roles.md). Einnig gæti verið nauðsynlegt að tengja notandann við **Einstakling** og uppfæra valkosti notanda, t.d. tungumál.

## <a name="manually-add-a-new-user"></a>Bæta við nýjum notanda handvirkt
1. Farið í **Kerfisstjórnun** \> **Notendur** \> **Notendur**.
2. Í aðgerðarúðunni velurðu **Nýtt**.
3. Í reitnum **Notandakenni** er fært inn einkvæmt kenni fyrir notandann.   
4. Í reitnum **Notandanafn** skal færa inn notandaheiti.  
5. Í reitnum **Veita**:
 - Fyrir innri notendur skal nota sjálfgefið gildi. Til dæmis er Azure AD-leigjandanum gefið forskeytið https://sts.windows.net/.  
 - Fyrir aðra en Azure AD-notendur, t.d. Service-2-Service-reikningar, skal færa inn einfalt textagildi. Til dæmis, NA. Þetta gildi hjálpar til við að forðast rangar sannvottunarhringingar sem gætu skilað sér í villum ef gilt gildi fyrir auðkenni veitu er notað.  
 - Fyrir ytri notendur eða gestanotendur skal bæta við heiti Azure AD-biðlarans á eftir https://sts.windows.net/.
6. Í reitinn **Tölvupóstur** skal færa inn fullt heiti netfangs notanda/aðalheiti notanda.  
7. Í reitnum **Fyrirtæki** skal velja sjálfgefið ræsingarfyrirtæki fyrir notanda. 
8. Veljið **Vista**.

Gildin fyrir kenni veitu og fjarmælingarkenni verða uppfærð samkvæmt kalli [Microsoft Graph](https://docs.microsoft.com/graph/overview) þegar skrá notanda er vistuð. Fjarmælingarkennið byggir á hlutarkenni/öryggiskenni notanda í Azure AD.

> [!NOTE]
> Eftir að notanda hefur verið bætt við þarf að úthluta hlutverkum og fyrirtækjum eftir því sem við á. Nánari upplýsingar er að finna á [Úthluta notendum á öryggishlutverk](assign-users-security-roles.md). Einnig gæti verið nauðsynlegt að tengja notandann við **Einstakling** og uppfæra **Notandavalkosti**, t.d. tungumál.

## <a name="change-a-user-id"></a>Breyta notandakenni
Til að breyta notandakenni þarf að endurnefna lykilinn í gagnagrunninum. Þegar notandakenni er breytt með því að nota þetta ferli er öllum tengdum notandastillingum breytt til að nota nýja notandakennið. Til dæmis eru notkunarupplýsingar í töflunni **SysLastValue** uppfærðar til að vísa til nýja notandakennið.

> [!NOTE]
> Notandakennið er aðallykill töflunnar fyrir notandaupplýsingar. Það getur tekið sinn tíma að endurnefna aðallykilinn fyrir núverandi notendur vegna þess að allar tilvísanir í lykilinn eru einnig uppfærðar í gagnagrunninum. 

1. Farðu í **Kerfisstjórnun \> Notendur \> Notendur**.
2. Veljið notanda úr listanum og veljið **Valmöguleikar\> Færsluupplýsingar**.
3. Velja **Endurnefna**.
4. Færa skal inn nýtt einkvæmt gildi fyrir notandakennið og síðan velja **Í lagi**. 
5. Veljið **Já** til að staðfesta.

## <a name="additional-resources"></a>Frekari upplýsingar

Frekari möguleikar til að innleiða B2B-notendur er að finna í [Flytja út B2B-notendur í Azure AD](../implement-b2b.md).

Frekari upplýsingar um forstillta kerfisreikninga er að finna í [Forstilltir kerfisreikningar](../pre-configured-system-accounts.md)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]