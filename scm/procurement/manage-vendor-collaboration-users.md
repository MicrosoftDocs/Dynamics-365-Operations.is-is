---
title: "Stjórna notendum fyrir samstarf lánardrottna"
description: "Þetta efnisatriði lýsir því hvernig má biðja um ráðstafanir fyrir nýja notendur samstarf lánardrottna og hvernig má bæta við nýjum tengiliðum samstarfs lánardrottna."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: smmContactPerson, VendVendorContactPerson, VendVendorPortalUser
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 220744
ms.assetid: edc19ad0-3565-4d47-98ac-dda6098f63ac
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 7e747547ed5cf4654a99382ecc8f9f6103ec5cfa
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017


---

# <a name="manage-vendor-collaboration-users"></a>Stjórna notendum fyrir samstarf lánardrottna

[!include[banner](../includes/banner.md)]


Þetta efnisatriði lýsir því hvernig má biðja um ráðstafanir fyrir nýja notendur samstarf lánardrottna og hvernig má bæta við nýjum tengiliðum samstarfs lánardrottna. 

Viðmót fyrir samstarf lánardrottna í Microsoft Dynamics 365 for Operations sýnir upplýsingar um innkaupapantanir, reikninga og vörusendingabirgðir til ytri lánardrottnum. Hægt er að stofna nýjan tengiliði fyrir samstarf lánardrottna og biðja um að nýjum notendum er úthlutað ef verið er að vinna sem ytri lánardrottni öryggishlutverk **Lánardrottinn sem er stjórnandi (ytri)** eða svipuð heimildir. Einnig er hægt að framkvæma þessi verk ef verið er að vinna sem innkaupasérfræðingur. Í þessu á hlutverkið við innkaupasérfærðing sem vinnur innan fyrirtækis sem á tilvik af Dynamics 365 for Operations. Frekari upplýsingar um hvernig á að nota samstarf lánardrottna ef þú ert ytri lánardrottni sjá [Lánardrottna með viðskiptavini](vendor-collaboration-work-customers-dynamics-365-operations.md).  

Frekari upplýsingar um hvernig á að nota samstarf lánardrottna ef þú ert innkaupasérfræðingur sjá [samstarf lánardrottna við ytri lánardrottnum](vendor-collaboration-work-external-vendors.md).

## <a name="add-new-vendor-collaboration-contacts"></a>Bætt við nýjum tengiliðum samstarf lánardrottna
Ef þú vilt að einhver hafi aðgang að samstarf lánardrottna þarf fyrst að bæta þeim við sem tengiliður samstarf lánardrottna. Einnig viltu kannski bæta við tengilið fyrir starfsmaður í þínu fyrirtæki sem mun ekki nota samstarf lánardrottna. T.d. gætu þeir verið tengiliður fyrir annars konar innkaupaupplýsingar. Nýjum tengiliðum er bætt við á **Alla tengiliði** síðu sem er opnuð í **samstarf lánardrottna** &gt; **Tengiliði** valmyndinni. Bæta við nýjum tengiliður:

1.  Smellt er á **Nýtt**.
2.  Sláðu inn Upplýsingar um tengiliður
3.  Veldu hvaða lögaðili þeir eru fulltrúi fyrir í þínu fyrirtæki, og hvaða lögaðili þeir vinna með í fyrirtækinu sem þeir vinna með. Það er gert með því að velja **lögaðila í fyrirtækið mitt**/**lögaðila í fyrirtæki viðskiptavinar** par.
4.  Smellið á **Stofna**.

Ef óskað er að eyða tengilið er aðeins hægt að eyða þeim sem þú hefur stofnað.

## <a name="vendor-collaboration-user-requests"></a>Notendabeiðnir samstarfs lánardrottna
Hægt að setja fram notendabeiðnir samstarf lánardrottna af innkaupasérfræðingi, eða af ytri lánardrottinn sem er stjórnandi.

-   Ef þú ert ytri lánardrottinn sendirðu inn beiðnir frá síðunni **Alla tengiliði** innan einingarinnar **Samstarf lánardrottna**.
-   Ef þú ert innkaupasérfræðingur sendirðu inn beiðnir frá **Skoða tengiliði** síðuna. Til að gera þetta má, á færslu lánardrottins í **Uppsetningu** hlutanum í aðgerðarúðu, velja **Tengiliði** &gt; **Skoða tengiliðina**.

Þú getur beðið um að gerðar séu ráðstafanir fyrir notanda, að gera notanda óvirkan, eða að breyta öryggishlutverkum. Ef þú ert ytri lánardrottinn sem er stjórnandi verður þú að vera skráður sem tengiliður fyrir lánardrottnalykla sem þú vilt gera notandabeiðnir fyrir, og þú verður að hafa aðgang að viðmóti fyrir samstarf lánardrottna fyrir þá lánardrottnalykla.  

Þegar beiðni er send þeim er bætt við í **notendabeiðnum samstarfs lánardrottna** í **samstarf lánardrottna** kerfiseiningu, og á **notandabeiðni samstarfs lánardrottna** í **Innkaup og aðföng** kerfiseiningu (Innkaup og aðföng kerfiseiningu er ekki aðgengileg fyrir ytri notendur).

### <a name="provision-a-user"></a>Gera ráðstafanir fyrir notanda

Áður en þú getur beðið um að gera ráðstafanir fyrir notanda, verður sá einstaklingur að vera settur upp sem tengiliður fyrir einn eða fleiri lánardrottnalykla. Stofna beiðni fyrir nýjan notanda samstarfs lánardrottna:

1.  Á **Alla tengiliði** síðunni er smellt á **Gera ráðstöfun fyrir lánardrottinn**.
2.  Slá inn netfang fyrir notanda Þetta aðsetur verða notuð af notandanum til að skrá sig inn á Dynamics 365 for Operations. Ef tölvupóstfang tilheyrir léni sem er skráður sem leigjanda með Microsoft Azure, þá verður tölvupóstfang að vera fyrirliggjandi Azure Active Directory (ADD) lykill fyrir ráðstöfunarferlið til að takist að ljúka. Ef tölvupóstfang tilheyrir ekki lén skráð með Microsoft Azure ADD lykill verður stofnuð ADD lykill sem hluti af ráðstöfunarferlinu og nýr notandi fær boð í pósti. Netföng notenda með lénum á borð við @hotmail.com, @gmail.com, eða @comcast.net er ekki hægt að nota til að skrá notanda Dynamics 365 for Operations.
3.  Stilla valkostinn **aðgang leyfð að samstarf lánardrottna** að **Já** fyrir alla lögaðila sem notandi þarf aðgang að.
4.  Í **Úthluta notendahlutverk** hlutanum skal velja **Úthluta** gátreitinn fyrir öryggishlutverk sem nýji notandinn ætti að hafa.
5.  Smelltu á **Senda**.

Þegar notandabeiðni lánardrottins er send inn, er reiturinn **aðgangur leyfður fyrir samstarf lánardrottna** stillt á **Já** fyrir valinn lánardrottnalykil og verkflæði notandabeiðni byrjar. Sem hluti af verkflæði er nýr notandi stofnaðir í Dynamics 365 for Operations og öryggishlutverk úthlutað. Auk þess er Azure B2B þjónustu virkjuð sem byrjar samskipti við Azure-gátt og tengir nýja eða núverandi AAD reikning við Dynamics 365 for Operations notandareikningurinn.

### <a name="inactivate-a-user"></a>Gera notanda óvirkan

Það eru tvær leiðir til að fjarlægja aðgang samstarf lánardrottna fyrir notanda:

-   Á **Tengiliði** síðunni fyrir lánardrottinn, stilla **aðgang leyfð fyrir samstarf lánardrottna** valkostinn á **Nei** fyrir tengiliðinn. Þetta er gert sérstaklega fyrir hvern lögaðila sem einstaklingurinn er tengiliður fyrir. Aðeins er hægt að nota þennan valkost af innkaupasérfræðingum.
-   Gera anna notandareikningurinn óvirkan með því að senda inn beiðnina **gera notanda lánardrottins óvirkan**.

Til að biðja um að gera notanda óvirkan:

1.  Á **Alla tengiliði** síðunni er smellt á **óvirkja** **notanda lánardrottins**.
2.  Skrifa athugasemd við **réttlæting viðskipta** svæði.
3.  Smelltu á **Senda**.

### <a name="modify-security-roles"></a>Breyta öryggishlutverkum

**Viðhalda notendahlutverk lánardrottins** síðu er sú sama og í **lánardrottins ráðstöfunarnotandi** síðuna nema að ekki er hægt að breyta lista yfir öryggishlutverk.  

Til að biðja um að öryggishlutverkin er breytt fyrir notanda:

1.  Á **Alla tengiliði** síðunni er smellt á **Viðhalda** **hlutverkum notanda lánardrottins**.
2.  Skrifa athugasemd við **réttlæting viðskipta** svæði.
3.  Í Hlutinn **Viðhalda notendahlutverk** , veldu öryggishlutverk sem þú vilt úthluta, eða hreinsa þær sem þú vilt fjarlægja.
4.  Smella á **Senda**.




