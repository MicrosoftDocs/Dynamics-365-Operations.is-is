---
title: Vinnusvæði fyrir lausn reikningsfanga
description: Þessi grein veitir upplýsingar um vinnusvæðið fyrir lausnarupptöku reikninga.
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4f3af7abf94542437be6132344d6bb7ffaf33d07
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690987"
---
# <a name="invoice-capture-solution-workspace"></a>Vinnusvæði fyrir lausn reikningsfanga

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="side-by-side-viewer-for-the-invoice-capture-solution"></a>Hlið við hlið áhorfandi fyrir lausnina til að taka upp reikninga

Að slá inn reikninga inn í kerfið hefur venjulega verið tímafrekt ferli sem er viðkvæmt fyrir villum, vegna þess að afgreiðslufólk verður að vafra um margar viðhengisskrár og glugga til að safna réttum upplýsingum. Skjalaskoðarinn hlið við hlið mun hjálpa til við að bæta upplifun þína þegar þú vinnur með reikninga með því að gera ferlið auðveldara, skilvirkara og nákvæmara.

Skjalaskoðarinn hlið við hlið gerir notendum kleift að hafa upprunalega skjalið og reikninginn opna hlið við hlið í sama glugga. Reikningssíðan er fyllt með upplýsingum sem koma úr upprunalegu reikningsskjali. Skoðandinn byggir upp tenginguna á milli reita reikningssíðunnar og upprunalega reikningsskjalsins. Skoðandinn hjálpar einnig notendum að finna allar villur sem eru til staðar á reikningssíðunni.

### <a name="open-the-side-by-side-viewer"></a>Opnaðu hlið við hlið skoðara

Í Microsoft Dynamics 365 Finance, þú getur opnað hlið við hlið skoðara frá listanum á yfirlitssíðunni eða frá reikningalistanum. Þú getur líka opnað hana með því að tvísmella (eða tvísmella) á færslu eða með því að velja reikningsnúmer.

### <a name="using-the-side-by-side-viewer"></a>Með því að nota hlið við hlið skoðara

#### <a name="manually-review-an-invoice"></a>Farið handvirkt yfir reikning

Reikningsskjal sem hefur verið flutt inn gæti þurft handvirka yfirferð vegna villna eða viðvarana. Í hlið við hlið skoðara mun skjalhausinn sýna stöðuna **Innflutt**, og núverandi útgáfa verður **Upprunaleg útgáfa**.

Til að byrja að skoða reikninginn skaltu velja **Byrjaðu endurskoðun**. Allir reiti verða breytanlegir. The **Staða** reiturinn er uppfærður í **Í endurskoðun**, og **Núverandi útgáfa** reiturinn er uppfærður í **Breytt útgáfa**.

#### <a name="view-and-work-with-messages"></a>Skoða og vinna með skilaboð

Notendur ættu að hefja yfirferðarferlið frá skilaboðaglugganum. Villuboð eru auðkennd með rauðu X, viðvörunarskilaboð eru auðkennd með þríhyrningi og upplýsingaskilaboð eru auðkennd með hring. Skilaboð tengd öryggisstig geta verið flokkuð sem annað hvort viðvaranir eða villur, allt eftir þröskuldinum sem er stillt af stillingarhópnum. Fyrir frekari upplýsingar, sjá [Stillingarhópar fyrir lausnarupptöku reikninga](invoice-capture-config-group.md).

Viðvörunar- og villuskilaboð er hægt að hunsa í skilaboðaglugganum, reikningshausnum eða reikningslínum. Eftir að skilaboð eru hunsuð birtast þau ekki lengur sem villa eða viðvörun og reikningurinn mun ekki mistakast í staðfestingu.

- Til að hunsa skilaboð úr skilaboðaglugganum velurðu **Hunsa**. Til að endurstilla skilaboð sem hafa verið hunsuð skaltu velja **Hunsa** aftur. Gerð þess er síðan breytt úr villu eða viðvörun í upplýsingar.
- Til að hunsa skilaboð úr reikningshaus eða reikningslínu skaltu velja **Hunsa** á vellinum. Skilaboðatáknið hverfur. Hins vegar mun það birtast aftur ef skilaboðin eru endurstillt frá skilaboðaglugganum.

Fyrir skilaboð sem tengjast reikningshausreitum, þegar þú velur skilaboðin í skilaboðaglugganum, er bendillinn færður í samsvarandi reit í haushlutanum.

#### <a name="proofread-and-edit-fields"></a>Prófarkalesa og breyta reitum

Ef gildi reits er lesið af upprunalega reikningnum í gegnum optical character recognition (OCR), birtist tákn á reitnum. Ef þú velur táknið stækkar skjalaskoðarinn og auðkennir staðinn sem reiturinn er lesinn af, til að hjálpa þér að sannreyna reikningsgögn.

Til að endurstilla skjalaskoðarann á upprunalega stækkun, fylgdu einu af þessum skrefum:

- Veldu sama tákn og þú valdir áður.
- Veldu hnappinn í efra hægra horninu á skjalaskoðaranum.

Breyttu reitunum eftir þörfum. Breytingar eru sjálfkrafa vistaðar þegar bendillinn yfirgefur reit. Tákn hægra megin við reit gefur til kynna að reiturinn hafi verið uppfærður handvirkt. Þegar síðan er endurnýjuð verður táknið fjarlægt.

#### <a name="check-an-invoice-to-get-up-to-date-messages"></a>Athugaðu reikning til að fá uppfærð skilaboð

Þegar þú breytir reit er reitgildið uppfært, en ný staðfestingarskilaboð eru ekki búin til. Til að fá uppfærð staðfestingarskilaboð skaltu velja **Athugaðu**. Skilaboðin í skilaboðaglugganum, á reikningshausnum og á reikningslínunum eru uppfærð.

#### <a name="complete-the-review"></a>Ljúktu við endurskoðunina

Til að ljúka yfirferð velurðu **Heill endurskoðun**. Reikningarnir eru staðfestir. Ef einhverjar villur finnast heldur staða skjalsins áfram **Í endurskoðun**, og skilaboðaslá birtist. Öll skilaboð í skilaboðaglugganum og á reikningshaus og línum eru sjálfkrafa uppfærð til að veita upplýsingar um orsakir misheppnaðrar staðfestingar.

Eftir að allar blokkunarvillur hafa verið lagaðar er hægt að ljúka endurskoðuninni. Staða skjalsins er uppfærð í **Farið yfir**, og ekki er lengur hægt að breyta reitunum. Þú getur endurræst endurskoðunina með því að velja **Byrjaðu endurskoðun** aftur.

#### <a name="generate-a-pending-vendor-invoice-in-finance"></a>Búðu til reikning lánardrottins í bið í Finance

Til að senda reikningsskjalið í tengda fjármálaumhverfið velurðu **Mynda**. Ef reikningsgerð mistekst birtast villuboð á skilaboðastiku.

#### <a name="void-an-invoice"></a>Ógilda reikning

Til að ógilda reikning skaltu velja **Ógilt**. Ekki er hægt að fara yfir ógilda reikninga og þeir eru ekki sýndir í **Reikningar þurfa handvirka yfirferð** lista.

### <a name="validation-logic"></a>Löggildingarrökfræði

Sumir lykilreitir í hlið-við-hlið skoðara eru ekki til í reikningsskilagögnum en eru nauðsynlegir til að búa til biðreikninga í Finance. Þessir reitir eru fengnir úr samsetningu núverandi reikningssviðsetningargagna og aðalgagna frá Finance.

Reitirnir sem þarf að leiða eru **Lögaðili**, **söluaðila**, og **Vörunúmer**. Þeir verða að vera fengnir í eftirfarandi röð. Ef útleiðsla á reit mistekst stöðvast ferlið.

1. **Lögaðili** – Lögaðilinn er fyrst afleiddur. Ef virk kortlagningarregla finnst fyrir lögaðilann er lögaðilinn fenginn út frá nafni fyrirtækis og heimilisfangi fyrirtækis.
2. **Reikningur söluaðila** – Því næst er lánardrottinsreikningurinn fenginn út frá virkri kortlagningarreglu og samsetningu af afleidda lögaðilanum og nafni lánardrottins og heimilisfangi lánardrottins.
3. **Vörunúmer** – Að lokum er vöruheitið dregið af sviðsetningu, byggt á eftirfarandi þremur tegundum upplýsinga:

    - Stillt kortlagningarregla
    - Hinn afleiddi lögaðili
    - Afleiddur lánardrottinn reikningur

Til að keyra staðfestingu skaltu velja **Athugaðu** í hlið við hlið áhorfanda. Eins og er framkvæmir staðfestingin eftirfarandi athuganir:

- **Skylduskoðun** – Þessi athugun staðfestir lögboðna reiti fyrir hlið við hlið áhorfanda. Notendur geta valið hvaða reitir verða að vera lögboðnir á **Stillingarstillingar** síðu.
- **Sjálfstraust stig** - Notendur geta stillt viðvörunarþröskuld og villuþröskuld fyrir öryggisstigið. Þessi athugun beinist að öryggisstiginu frá OCR sem er undir þessum viðmiðunarmörkum. Villu- eða viðvörunarskilaboð verða sýnd á grundvelli staðfestingarniðurstöðunnar.
- **Lögaðili** – Þessi ávísun staðfestir að lögaðili sé í Fjármálum. Ef lögaðilinn er ekki til í fjármálaumhverfinu mistekst fullgildingin.

Þegar hlið við hlið áhorfandi er notaður í fyrsta skipti og notandinn velur **Athugaðu**, eru afleiðslu- og staðfestingarferlar keyrðir. Ef reikningarnir eru nákvæmir er staðfestingarferlið keyrt þegar notandinn velur **Heill endurskoðun**. Það er líka keyrt þegar notandinn velur **Búðu til reikning lánardrottins**.

Afleiðingarferlið á sér stað fyrir staðfestingarferlið og allar viðvaranir eða villur koma frá staðfestingarferlinu. Viðvaranirnar og villurnar verða skráðar í Finance.
