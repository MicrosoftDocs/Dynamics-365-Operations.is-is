---
title: Villuleita í færslum verslunar fyrir útreikning uppgjörs
description: Þetta efnisatriði lýsir virkni til að villuleita færslur verslunar í Microsoft Dynamics 365 Commerce.
author: analpert
ms.date: 12/15/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: analpert
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: 008368ae32aa92682d578b75b148e0587fcc94e0
ms.sourcegitcommit: 70ac76be31bab7ed5e93f92f4683e65031fbdf85
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/16/2021
ms.locfileid: "7924772"
---
# <a name="validate-store-transactions-for-statement-calculation"></a>Villuleita í færslum verslunar fyrir útreikning uppgjörs

[!include [banner](includes/banner.md)]

Þetta efnisatriði lýsir virkni til að villuleita færslur verslunar í Microsoft Dynamics 365 Commerce. Villuleitarferlið auðkennir og merkir færslur sem munu valda villum við bókun, áður en þær eru teknar inn í bókunarferli uppgjörsins.

Þegar reynt er að bóka uppgjör getur villuleitarferlið mistekist vegna ósamræmis í gögnum í færslutöflum viðskiptanna. Hér eru nokkur dæmi um þætti sem geta valdið þessu ósamræmi:

- Heildarfærsla í haustöflu er ekki í samræmi við heildarfærslu í línunum.
- Vörufjöldinn sem tilgreindur er í haustöflunni samsvarar ekki vörufjöldanum í færslutöflunni.
- Skattar í haustöflu eru ekki í samræmi við skattupphæð í línunum. 

Ef færslur með ósamræmi eru teknar inn í bókunarferli uppgjörsins geta sölureikningar og greiðslubækur sem búin eru til valdið því að bókun uppgjörs mistakist. Ferlið **Villuleita í færslum verslunar** kemur í veg fyrir þessi vandamál með því að tryggja að aðeins færslur sem standast villuleitarreglur færslu séu færðar yfir í útreikningsferli færsluuppgjörs.

Eftirfarandi skýringarmynd sýnir endurtekin dagferli fyrir upphleðslu færslna, villuleit færslna og útreikning og bókun færsluuppgjöra og ferli við dagslok fyrir útreikning og bókun fjárhagsskýrslna.

![Skýringarmynd sem sýnir endurtekin dagferli fyrir upphleðslu færslna, villuleit færslna og útreikning og bókun færsluuppgjöra og ferli við dagslok fyrir útreikning og bókun fjárhagsskýrslna](./media/valid-checker-statement-posting-flow.png)

## <a name="store-transaction-validation-rules"></a>Villuleitarreglur fyrir færslur verslunar

Runuvinnslan **Villuleita í færslum verslunar** athugar samræmi viðskiptafærslutaflna út frá eftirfarandi villuleitarreglum.

> [!NOTE]
> Villuleitarreglum verður áfram bætt við síðari útgáfur.

### <a name="transaction-header-validation-rules"></a>Villuleitarreglur í færsluhaus

Eftirfarandi tafla telur upp villuleitarreglur í færsluhaus sem bornar eru saman við hausa smásölufærslna áður en þessar færslur eru sendar í bókun uppgjörs.

| Titill | Lýsing |
|-------|-------------|
| Viðskiptadagur | Þessi regla staðfestir að viðskiptadagur færslu sé tengdur við opið fjárhagstímabil í fjárhagnum. |
| Sléttun gjaldmiðils | Þessi regla staðfestir að færsluupphæðirnar eru sléttaðar samkvæmt sléttunarreglu gjaldmiðils. |
| Viðskiptavinalykill | Þessi regla staðfestir að viðskiptavinurinn sem notaður er í færslunni sé til í gagnagrunninum. |
| Afsláttarupphæð | Þessi regla staðfestir að afsláttarupphæð í hausnum jafngildi samtölu afsláttarupphæða í línunum. |
| Bókunarstaða fjárhagsskjals (Brasilía) | Þessi regla staðfestir að hægt sé að bóka fjárhagsskjalið. |
| Brúttóupphæð | Þessi regla staðfestir að brúttóupphæð í færsluhaus samsvari nettóupphæð með sköttum í færslulínunum ásamt gjöldum. |
| Nettó | Þessi regla staðfestir að nettóupphæð í færsluhaus samsvari nettóupphæð án skatta í færslulínunum ásamt gjöldum. |
| Nettó + skattur | Þessi regla staðfestir að brúttóupphæð í færsluhaus samsvari nettóupphæð án skatta í færslulínunum ásamt öllum sköttum og gjöldum. |
| Vörufjöldi | Þessi regla staðfestir að vörufjöldi sem tilgreindur er í færsluhaus samsvari heildarmagni í færslulínunum. |
| Greiðsluupphæð | Þessi regla staðfestir að greiðsluupphæð í færsluhaus samsvari samtölu allra greiðslufærslna. |
| Útreikningur skattundanþágu | Þessi regla staðfestir að summa reiknaðrar upphæðar og undanþeginnar skattupphæðar gjaldalínu jafngildir upprunalegri reiknaðri upphæð. |
| Verðlagning með sköttum | Þessi regla staðfestir að flaggið **Skattur er innifalinn í verði** sé í samræmi við færsluhaus og skattfærslur. |
| Færsla ekki tóm | Þessi regla staðfestir að færslan innihaldi línur og að minnsta kosti ein lína er ekki ógild. |
| Van-/ofgreiðsla | Þessi regla staðfestir að mismunur milli brúttóupphæðar og greiðsluupphæðar fari ekki umfram skilgreiningu á hámarki fyrir vangreiðslu/ofgreiðslu. |

### <a name="transaction-line-validation-rules"></a>Villuleitarreglur færslulínu

Eftirfarandi tafla telur upp villuleitarreglur færslulínu sem bornar eru saman við línuupplýsingar smásölufærslna áður en þessar færslur eru sendar í bókun uppgjörs.

| Titill | Lýsing |
|-------|-------------|
| Strikamerki | Þessi regla staðfestir að öll strikamerki fyrir vörur sem notuð eru í færslulínunum séu til í gagnagrunninum. |
| Gjaldalínur | Þessi regla staðfestir að summa reiknaðrar upphæðar og undanþeginnar skattupphæðar gjaldalínu jafngildir upprunalegri reiknaðri upphæð. |
| Skil á gjafakortum | Þessi regla staðfestir að engin skil á gjafakortum séu í færslunni. |
| Vöruafbrigði | Þessi regla staðfestir að allar vörur og öll afbrigði sem notuð eru í færslulínunum séu til í gagnagrunninum. |
| Línuafsláttur | Þessi regla staðfestir að upphæð línuafsláttar samsvari samtölu afsláttarfærslna. |
| Línuskattur | Þessi regla staðfestir að skattupphæð línu samsvari samtölu skattafærslna. |
| Neikvætt verð | Þessi regla staðfestir að engin neikvæð verð séu notuð í færslulínum. |
| Stýrt af raðnúmeri | Þessi regla staðfestir að raðnúmer sé til staðar í færslulínunni fyrir vörur sem stýrt er af raðnúmeri. |
| Raðnúmeravídd | Þessi regla staðfestir að ekkert raðnúmer er gefið upp ef raðnúmeravídd vörunnar er óvirk. |
| Mótsögn merkis | Þessi regla staðfestir að merki fyrir magn og merki fyrir nettóupphæð sé það sama í öllum færslulínunum. |
| Skattaundanþága | Þessi regla staðfestir að samtala línuvöru og upphæðar undanþegins skatts er jöfn upprunalegu verði. |
| Skattflokksúthlutun | Þessi regla staðfestir að samsetning VSK-flokks og skattflokks vöru leiði til gilds skattasniðmengis. |
| Umreikningur mælieininga | Þessi regla staðfestir að mælieiningar í öllum línum séu með gilda umreikninga yfir í mælieiningu birgða. |

## <a name="enable-the-store-transaction-validation-process"></a>Virkja villuleitarferli fyrir færslur verslunar

Skilgreina skal runuvinnsluna **Villuleita í færslum verslunar** fyrir reglulega keyrslu í Commerce Headquarters (**Retail og Commerce \> Upplýsingatækni Retail og Commerce \> Sölustaðarbókun**). Runuvinnslan er tímasett út frá stigveldi verslunarinnar. Við mælum með því að þessi runuvinnsla sé skilgreind á að vera keyrð eins oft og **P-vinnslan** og runuvinnslur af gerðinni **Útreikningur færsluuppgjörs**.

## <a name="results-of-the-validation-process"></a>Niðurstöður villuleitarferlis

Hægt er að skoða niðurstöður runuvinnslunnar **Villuleita í færslum verslunar** í færslu hverrar smásöluverslunar. Svæðið **Staða villuleitar** í viðkomandi færslu er stillt á **Lokið**, **Villa** eða **Ekkert**. Svæðið **Tími síðustu villuleitar** sýnir dagsetningu síðustu villuleitar.

Eftirfarandi tafla lýsir hverri stöðu villuleitar.

| Staða prófunar | Lýsing |
|-------------------|-------------|
| Tókst | Allar virkar villuleitarreglur stóðust skoðun. |
| Villa | Virk villuleitarregla fann villu. Hægt er að sjá frekari upplýsingar um villuna með því að velja **Villur við villuleit** á aðgerðasvæðinu. |
| Ekkert | Færslugerðin gerir ekki kröfu um að villuleitarreglur séu notaðar. |

![Síðan fyrir færslur verslunar sýnir svæðið fyrir stöðu villuleitar og hnappinn fyrir villur við villuleit.](./media/valid-checker-validation-status-errors.png)

Aðeins færslur með villuleitarstöðuna **Lokið** verða teknar með í færsluuppgjörunum. Til að skoða færslur sem hafa stöðuna **Villa** skal yfirfara reitinn **Villuleitarbilun við staðgreiðslu** á vinnusvæðinu **Fjármál verslunar**.

![Reitir á vinnusvæðinu „Fjármál verslunar“.](./media/valid-checker-cash-carry-validation-failures.png)

Frekari upplýsingar um hvernig hægt er að lagfæra villuleitarbilanir við staðgreiðslu er að finna í [Breyta og endurskoða færslur staðgreiðslu við afhendingu og stjórnun reiðufjár](edit-cash-trans.md).

## <a name="additional-resources"></a>Frekari upplýsingar

[Breyta og endurskoða færslur staðgreiðslu við afhendingu og stjórnun reiðufjár](edit-cash-trans.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
