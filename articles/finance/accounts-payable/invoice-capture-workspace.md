---
title: Vinnusvæði Invoice capture
description: Þessi grein veitir upplýsingar um vinnusvæði Invoice capture.
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
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690987"
---
# <a name="invoice-capture-solution-workspace"></a>Vinnusvæði Invoice capture

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="side-by-side-viewer-for-the-invoice-capture-solution"></a>Samhliða yfirlit fyrir Invoice capture-lausnina

Að slá inn reikninga í kerfið hefur yfirleitt verið tímafrekt ferli sem er líklegt til að valda villum því að bókarar verða að halda utan um margar viðhengisskrár og glugga til að safna saman réttum upplýsingum. Samhliða skjalayfirlit bætir upplifunina þegar unnið er í reikningum með því að gera ferlið auðveldara, skilvirkara og nákvæmara.

Samhliða skjalayfirlit gerir notendum kleift að vera með upprunalegt skjal og reikning opið hlið við hlið í sama glugganum. Reikningssíðan er fyllt með upplýsingum sem koma úr upprunalega reikningsskjalinu. Yfirlitið býr til tengingar á milli reita reikningsíðu og upprunalegs reikningsskjals. Yfirlitið hjálpar notendum einnig að finna villur sem eru til staðar á reikningssíðunni.

### <a name="open-the-side-by-side-viewer"></a>Opna samhliða yfirlit

Í Microsoft Dynamics 365 Finance er hægt að opna samhliða yfirlit úr listanum á samantektarsíðunni eða reikningslistasíðunni. Einnig er hægt að opna það með því að tvípikka (eða tvísmella) á færslu eða með því að velja reikningsnúmerið.

### <a name="using-the-side-by-side-viewer"></a>Notkun samhliða yfirlits

#### <a name="manually-review-an-invoice"></a>Fara handvirkt yfir reikning

Reikningsskjal sem hefur verið flutt inn gæti þurft handvirka yfirferð út af villum eða viðvörunum. Í samhliða yfirlitinu mun skjalahausinn sýna stöðuna **Innflutt** og núverandi útgáfa verður **Upprunaleg útgáfa**.

Til að byrja að fara yfir reikninginn er valið **Hefja yfirferð**. Hægt verður að breyta öllum svæðum. Reiturinn **Staða** er uppfærður í **Í skoðun** og reiturinn **Núverandi útgáfa** er uppfærður í **Breytt útgáfa**.

#### <a name="view-and-work-with-messages"></a>Skoða og vinna með skilaboð

Notendur ættu að hefja endurskoðunarferlið á skilaboðasvæðinu. Villuboð eru táknuð með rauðu X, viðvörunarboð eru táknuð með þríhyrningi og upplýsingaboð eru táknuð með hring. Hægt er að flokka skilaboð sem tengjast áreiðanleikaeinkunn sem annaðhvort viðvaranir eða villur eftir því hvernig þröskuldurinn er stilltur af afbrigðisflokknum. Frekari upplýsingar eru í [Skilgreiningarhópar Invoice capture-lausnar](invoice-capture-config-group.md).

Hægt er að hunsa viðvörunar- og villuboð frá skilaboðasvæðinu, reikningshausnum eða reikningslínunum. Eftir að skilaboð eru hunsuð birtist þau ekki lengur sem villa eða viðvörun og reikningurinn fellur ekki á villuprófun.

- Til að hunsa skilaboð frá skilaboðasvæðinu velurðu **Hunsa**. Til að endurstilla skilaboð sem hafa verið hunsuð skaltu velja **Hunsa** aftur. Tegund þess er síðan breytt úr villu eða viðvörun í upplýsingar.
- Til að hunsa skilaboð frá fyrirsögn reikningsins eða reikningslínunni skal velja **Hunsa** í reitnum. Skilaboðatáknið hverfur. Hins vegar birtist það aftur ef skilaboðin eru endurstillt á skilaboðasvæðinu.

Fyrir skilaboð sem tengjast reitum reikningshauss, þegar skilaboðin eru valin á skilaboðasvæðinu, er bendillinn færður á samsvarandi reit í haushlutanum.

#### <a name="proofread-and-edit-fields"></a>Prófarkarlesturs- og breytingasvæði

Ef gildi reits er lesið úr upprunalegum reikningi gegnum stafakennsl (OCR) birtist tákn í reitnum. Ef táknið er valið eykur skjalayfirlitið aðdrátt og auðkennir staðinn þar sem reitargildið er lesið til að auðvelda staðfestingu reikningsgagna.

Til að endurstilla skjalayfirlit í upprunalega stærð skal fylgja einu af eftirfarandi skrefum:

- Veldu sama tákn og þú valdir áður.
- Velja skal hnappinn efst í hægra horninu á skjalaskjánum.

Breytið reitunum eftir þörfum. Breytingar eru vistaðar sjálfkrafa þegar bendillinn fer úr reit. Tákn hægra megin við reit gefur til kynna að reiturinn hafi verið uppfærður handvirkt. Þegar síðan er uppfærð verður táknið fjarlægt.

#### <a name="check-an-invoice-to-get-up-to-date-messages"></a>Skoða reikning til að fá skilaboð með nýjustu upplýsingum

Þegar reit er breytt er reitargildið uppfært en nýju villuleitarboðin eru ekki búin til. Til að fá uppfærð staðfestingarskilaboð skaltu velja **Athuga**. Skilaboðin í skilaboðasvæðinu, í reikningshausnum og á reikningslínunum eru uppfærð.

#### <a name="complete-the-review"></a>Ljúka yfirferðinni.

Til að ljúka við yfirferðina velur þú **Ljúka yfirferðinni**. Reikningarnir eru staðfestir. Ef villur finnast er staða skjalsins áfram **Í skoðun** og skilaboðsstika birtist. Öll skilaboð á skilaboðasvæðinu og í reikningshausnum og línunum eru sjálfkrafa uppfærð til að gefa upplýsingar um orsakir þess að ekki tókst að villuleita.

Eftir að allar villur hafa verið lagfærðar er hægt að ljúka við yfirferðina. Staða skjalsins er uppfærð í **Yfirfarið** og ekki er lengur hægt að breyta reitunum. Hægt er að endurræsa yfirferðina með því að velja **Hefja yfirferð** aftur.

#### <a name="generate-a-pending-vendor-invoice-in-finance"></a>Búa til reikning lánardrottins í bið í Finance

Til að senda reikningsskjalið til tengds Finance-umhverfis velur þú **Mynda**. Ef reikningsmyndun mistekst birtast villuboð á skilaboðastiku.

#### <a name="void-an-invoice"></a>Ógilda reikning

Veldu **Ógilda** til að ógilda reikning. Ekki er hægt að fara yfir ógilta reikninga og þeir eru ekki sýndir á listanum **Fara þarf handvirkt yfir reikninga**.

### <a name="validation-logic"></a>Villuleitarrök

Sumir lykilreitir í samhliða yfirlitinu eru ekki til staðar í sviðsetningargögnum reikningsins en eru nauðsynlegir til að búa til reikninga í biðstöðu í Finance. Þessir reitir koma frá samsetningu af núverandi sviðsetningargögnum reiknings og aðalgögnum úr Finance.

Reitirnir sem verða að vera afleiddir eru **Lögaðili**, **Lykill lánardrottins** og **Vörunúmer**. Af þeim verður að leiða í eftirfarandi röð. Ef ekki er hægt að leiða af svæði stöðvast ferlið.

1. **Lögaðili** – Lögaðilinn er afleiddur fyrst. Ef virk vörpunarregla finnst fyrir lögaðilann er lögaðilinn fenginn út frá heiti og aðsetri fyrirtækisins.
2. **Lánardrottnalykill** – Næst er lánardrottnalykillinn byggður á virkri vörpunarreglu og samsetningu af afleiddum lögaðila og heiti og aðsetri lánardrottins.
3. **Vörunúmer** – Að lokum er vöruheitið byggt á sviðsetningu, samkvæmt eftirfarandi þremur gerður af upplýsingum:

    - Skilgreind vörpunarregla
    - Afleiddi lögaðilinn
    - Afleiddi lánardrottnalykillinn

Til að keyra staðfestingu velur þú **Athuga** í samhliða yfirliti. Sem stendur framkvæmir staðfesting eftirfarandi athuganir:

- **Skylduathugun** – Þessi athugun staðfestir skyldusvæði fyrir yfirlit hlið við hlið. Notendur geta valið hvaða reitir verða að vera áskildir á síðunni **Skilgreiningarstilling**.
- **Áreiðanleikaeinkunn** – Notendur geta stillt viðvörunarmörk og villumörk fyrir áreiðanleikaeinkunnina. Í þessari athugun er lögð áhersla á áreiðanleikaeinkunn frá OCR sem er undir þeim mörkum. Villuboð eða viðvörunarskilaboð verða sýnd á grundvelli niðurstöðu staðfestingar.
- **Lögaðili** – Þessi athugun staðfestir að lögaðili er í Finance. Ef lögaðilinn er ekki til staðar í Finance-umhverfinu tekst staðfestingin ekki.

Þegar samhliða yfirlitið er notað í fyrsta skipti og notandi velur **Athuga** er afleiðslu- og villuleitarferlið keyrt. Ef reikningarnir eru nákvæmir er villuleitarferlið keyrt þegar notandi velur **Ljúka yfirferð**. Það er einnig keyrt þegar notandinn velur **Mynda reikning lánardrottins**.

Afleiðsluferlið á sér stað á undan villuleitarferlinu og allar viðvaranir og villur koma úr villuleitarferlinu. Viðvaranirnar og villurnar verða skráðar inn í Finance.
