---
title: Birgðaleit á sölustað
description: Þessi grein lýsir því hvernig á að nota birgðaleitaraðgerðina í Dynamics 365 Commerce sölustaður (POS) til að skoða birgðaframboð á vörum í verslunum og vöruhúsum.
author: boycezhu
ms.date: 08/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: boycez
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: Application update 5, AX 8.0
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: fc8c7dad0a7cb66ba7d6c6f527be84cfe74dee52
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288326"
---
# <a name="inventory-lookup-operation-in-pos"></a>Birgðaleit á sölustað

[!include [banner](includes/banner.md)]

Þessi grein lýsir því hvernig á að nota birgðaleitaraðgerðina í Dynamics 365 Commerce sölustaður (POS) til að skoða birgðaframboð á vörum í verslunum og vöruhúsum.

Nákvæmt yfirlit yfir í fyrirtækjum hjálpar starfsfólki verslunar að veita tímanlega og góða þjónustu við viðskiptavini. Augnablikið sem skiptir mestu máli er þegar viðskiptavinurinn er tilbúinn til að taka ákvörðun um kaup. Mikilvægt er að gjaldkeri í smásöluverslun hafi birgðaupplýsingar í rauntíma eða nálægt rauntíma innan seilingar svo þeir geti lofað með nákvæmni afhendingu afurðar.

Aðgerð birgðauppflettingar í Commerce á sölustað aðstoðar smásala að ná sem mestu úr rekstrinum og öðlast innsýn með því að tengja verslanir við Commerce Headquarters. Þessi virkni býður upp á yfirlit yfir birgðastöðu á afurðum í verslunum og vöruhúsum. Hún hjálpar einnig smásölum að keyra aukna hagkvæmni og sparnað með því að betrumbæta birgðaáætlanagerð í rauntíma.

Þegar aðgerð birgðauppflettingar er notuð í forriti sölustaðar, notar gjaldkeri sölustaðar talnaborðið til að slá inn afurðarnúmer til að spyrjast fyrir um birgðaupplýsingar hennar. Ef innslegin afurð er með afbrigði getur gjaldkerinn kosið að velja víddir eða önnur gildi til að athuga birgðaupplýsingar tiltekins afurðarafbrigðis.

## <a name="inventory-lookup-list-view-for-individual-products"></a>Listayfirlit birgðauppflettingar fyrir stakar afurðir

Fyrir einstaka afurð býður aðgerð birgðauppflettingar upp á listayfirlit birgðauppflettingar þar sem eftirfarandi afurðarupplýsingar eru sýndar fyrir lista yfir staðsetningar:

- **Birgðir** – Á við um „tiltækt efnislegt“ magn afurðar.
- **Frátekið** – Á við um „frátekið efnislegt“ magn sem sótt er úr höfuðstöðvum.
- **Pantað** - Á við um „samtals pantað“ magn sem sótt er úr höfuðstöðvum.
- **Eining** - Á við um mælieiningu birgða sem er skilgreind í höfuðstöðvum.

Listayfirlit yfir staðsetningar inniheldur allar verslanir og vöruhús sem eru skilgreind í uppfyllingarflokkunum sem núverandi verslun er tengd við eins og sýnt er í eftirfarandi myndadæmi.

![Listayfirlit yfir aðgerð birgðauppflettingar.](media/inventory-lookup-list-view.png)

> [!NOTE]
> Gakktu úr skugga um að núverandi verslun þín sé með í tilheyrandi uppfyllingarhópum.

Eftirfarandi aðgerðir eru í boði á forritastiku sölustaðar:

- **Raða** – Þessi aðgerð gerir notanda sölustaðar kleift að raða gögnum í listayfirlitinu út frá ýmsum skilyrðum. Röðun eftir staðsetningu er sjálfgefinn valkostur röðunar.

    - **Landfræðileg staðsetning** (frá næstu staðsetningu til þeirrar fjarlægustu, miðað við fjarlægð núverandi verslunar)
    - **Heiti** (í hækkandi eða lækkandi röð)
    - **Verslunarnúmer** (í hækkandi eða lækkandi röð)
    - **Birgðir** (í lækkandi röð)
    - **Frátekið** (í lækkandi röð)
    - **Pantað** (í lækkandi röð)

- **Sía** - Þessi aðgerð gerir notanda sölustaðar kleift að skoða síuð gögn fyrir tiltekna staðsetningu.
- **Sýna framboð verslunar** - Þessi aðgerð gerir notanda sölustaðar kleift að skoða magn sem má lofa (ATP) fyrir afurð í valdri verslun.
- **Sýna staðsetningu verslunar** - Þessi aðgerð opnar aðskilda síðu til að sýna kortayfirlit, aðsetur og opnunartíma verslunar fyrir valda verslun.
- **Sækja í verslun** - Þessi aðgerð stofnar pöntun viðskiptavinar fyrir afurðina sem verður sótt í verslun og beinir notandanum að færsluskjámyndinni.
- **Senda afurð** - Þessi aðgerð stofnar pöntun viðskiptavinar fyrir afurðina sem verður send úr valdri verslun og beinir notandanum að færsluskjámyndinni.
- **Skoða öll afbrigði** - Fyrir afurð með afbrigði skiptir þessi aðgerð úr listayfirliti yfir í fylkisyfirlit sem sýnir birgðaupplýsingar fyrir öll afbrigði afurðarinnar.
- **Bæta við færslu** - Þessi aðgerð bætir afurðinni við körfuna og vísar notandanum á færsluskjáinn.

> [!NOTE]
> Röðun eftir staðsetningu sem var kynnt í útgáfu 10.0.17 af Commerce sýnir núverandi verslun efst. Fyrir aðrar staðsetningar er fjarlægð milli staðsetningar og núverandi verslunar ákvörðuð út frá hnitum (lengdar- og breiddargráðu) sem skilgreind eru í Commerce Headquarters. Fyrir verslun eru staðsetningarupplýsingar skilgreindar í aðalaðsetri rekstrareiningarinnar sem tengist versluninni. Fyrir vöruhús án verslunar eru staðsetningarupplýsingarnar skilgreindar í aðsetri vöruhúss. Fyrir útgáfu 10.0.17 sýnir listayfirlitið alltaf núverandi verslun efst og raðar öðrum staðsetningum í stafrófsröð.
>
> Aðgerðirnar **Sýna framboð verslunar**, **Sýna staðsetningu verslunar**, **Sækja í verslun** og **Senda afurð** eru ekki í boði fyrir staðsetningar án verslunar.

## <a name="inventory-lookup-matrix-view-for-variants"></a>Fylkisyfirlit birgðauppflettingar fyrir afbrigði

Fyrir aðalafurðir með afbrigði býður aðgerð birgðauppflettingar einnig upp á fylkisyfirlit eftir víddum sem sýnir upplýsingar um birgðaframboð fyrir öll afbrigði aðalafurðar á valdri staðsetningu. Fylkisyfirlitið sýnir sjálfkrafa gögn fyrir núverandi verslun. Hægt er að nota aðgerðina **Verslun** á forritastikunni til að fletta upp birgðaupplýsingum í öðrum verslunum sem skilgreindar eru í uppfyllingarflokkunum sem núverandi verslun er tengd við.

Eftirfarandi myndadæmi sýnir fylkisyfirlit birgðauppflettingar á sölustað.

![Fylkisyfirlit aðgerðar birgðauppflettingar.](media/inventory-lookup-matrix-view.png)

Í fylkisyfirlitinu stendur hvert hólf fyrir ákveðið afbrigði og sýnir gildi lagerbirgða (efnislega tiltækar) niðri í hægra horninu auk gilda fyrir **frátekið** (efnislega frátekið) og **pantað** (samtals pantað) uppi í vinstra horninu. Eftirfarandi tafla útskýrir merkingu á hinum ýmsu lagergildum.

| Virði á lager                            | lýsing |
|------------------------------------------|-------------|
| Tölugildi sem er meira en 0 (núll) | Afbrigði hefur verið gefið út á valda staðsetningu og þú getur framkvæmt fleiri aðgerðir í hólfinu. |
| **0** (núll)                             | Afbrigði hefur verið gefið út á valda staðsetningu en varan er ekki tiltæk á valdri staðsetningu. Hægt er að framkvæma fleiri aðgerðir í hólfinu. |
| **Á ekki við** eða óvirkt hólf              | Afbrigði hefur ekki verið gefið út á valda staðsetningu og þú getur ekki framkvæmt fleiri aðgerðir í hólfinu. |

Birtingarröðin fyrir víddargildin í fylkisyfirlitinu byggir á skilgreiningu á röð víddarbirtingar í Commerce Headquarters. Hægt er að breyta skilgreiningu á birtingarröð vídda með því að velja nýja vídd til að nota. 

Eftirfarandi aðgerðir eru í boði í hólfi fylkisyfirlitsins:

- **Selja núna** - Þessi aðgerð bætir völdu afbrigði við körfuna og vísar notandanum á færsluskjáinn.
- **Sækja í verslun** - Þessi aðgerð stofnar pöntun viðskiptavinar fyrir valið afbrigði sem verður sótt í verslun og beinir notandanum að færsluskjámyndinni.
- **Senda afurð** - Þessi aðgerð stofnar pöntun viðskiptavinar fyrir valið afbrigði sem verður sent úr valdri verslun og beinir notandanum að færsluskjámyndinni.
- **Framboð** - Þessi aðgerð fer með notandann á aðskilda síðu sem sýnir ATP-magnið fyrir valið afbrigði í valdri verslun.
- **Sýna allar staðsetningar** - Þessi aðgerð skiptir yfir í listayfirlit yfir framboð á stöðluðum birgðum sem sýnir birgðaupplýsingarnar fyrir valið afbrigði.
- **Skoða afurðarupplýsingar** - Þessi aðgerð vísar notandanum á upplýsingasíðu afurðar (PDP) fyrir valið afbrigði.

## <a name="access-inventory-lookup-from-other-pages-in-pos"></a>Opna birgðauppflettingu af annarri síðu á sölustað

Notendur sölustaðar geta nálgast aðgerð birgðauppflettingar af annarri síðu á sölustað.

Eftirfarandi myndadæmi sýnir niðurstöður birgðauppflettingar af PDF á sölustað.

![Birgðauppfletting af upplýsingasíðu afurðar.](media/inventory-lookup-from-product-details-page.png)

Á PDP aðalafurðar er hægt að nota aðgerðina **Skoða öll afbrigði** á forritastikunni til að ræsa fylkisyfirlit birgðauppflettingar sem sýnir upplýsingar um birgðaframboð fyrir núverandi verslun fyrir öll afbrigði afurðar. Fyrir staka afurð sýnir PDP gildi lagerbirgða (tiltækar efnislega) fyrir þá afurð fyrir núverandi verslun. Auk þess er hægt að velja tengilinn **Birgðir annarra verslana** til að ræsa aðgerð uppflettingar til að athuga birgðaframboð afurðar í öðrum verslunum og vöruhúsum.

> [!NOTE]
> Aðgerðin **Skoða öll afbrigði** á PDP er aðeins í boði fyrir aðalafurðir sem eru með afbrigði. Hún er ekki í boði fyrir tilteknar afurðir eða sett.

Hægt er að stilla aðgerð birgðauppflettingar þannig að hún birtist sem tengill í hnappahnitinu í færsluskjámynd sölustaðar. Eftir skilgreiningu, þegar notandinn velur körfulínu og velur svo hnappinn **Birgðauppfletting** verður listayfirlit birgðauppflettingar fyrir valda afurð sýnt. Nánari upplýsingar um hvernig á að skilgreina hnappahnit með verkfæri skjáhönnunar sölustaðar er að finna í [Sjónrænar skilgreiningar fyrir notandaviðmót sölustaðar](pos-screen-layouts.md).

## <a name="inventory-lookup-with-channel-side-calculation"></a>Birgðauppfletting með útreikning rásar

Í Commerce-útgáfu 10.0.9 og eldri er gildið fyrir **tiltækar birgðir** í aðgerð birgðauppflettingar sótt úr Commerce Headquarters í gegnum þjónustukall í rauntíma. Í Commerce-útgáfu 10.0.10 og nýrri er hægt að skilgreina aðgerð birgðauppflettingar á sölustað svo hún noti útreikning rásar í netþjóni Commerce til að finna út tiltækt efnistlegt virði sem getur gefið áreiðanlegra og nákvæmara mat á lagerbirgðum með því að taka til greina færslugögn sem hafa ekki enn verið samstillt við höfuðstöðvarnar. Frekari upplýsingar um birgðaútreikning rásar og tengdar stillingar sölustaðar í höfuðstöðvum er að finna í [Reikna tiltækar birgðir fyrir smásölurásir](calculated-inventory-retail-channels.md).

## <a name="additional-resources"></a>Frekari upplýsingar

[Sjónrænar skilgreiningar fyrir notandaviðmót sölustaðar](pos-screen-layouts.md)

[Reikna tiltækar birgðir fyrir smásölurásir](calculated-inventory-retail-channels.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
