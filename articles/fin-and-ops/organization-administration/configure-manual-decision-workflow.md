---
title: "Skilgreina Skilgreina handvirka ákvörðun í verkflæði"
description: "Þetta efnisatriði útskýrir hvernig skilgreina á eiginleika handvirkrar ákvörðunar."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 192101
ms.assetid: 0bccad77-1a44-4f08-967b-12c62c02afc7
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 078d7d5e822a5ffa74131838b249563201b54c7f
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="configure-a-manual-decision-in-a-workflow"></a>Skilgreina Skilgreina handvirka ákvörðun í verkflæði

[!include[banner](../includes/banner.md)]


Þetta efnisatriði útskýrir hvernig skilgreina á eiginleika handvirkrar ákvörðunar.

Til að skilgreina handvirka ákvörðun í verkflæðisritlinum, hægrismellt er á handvirk ákvörðun og smellið síðan á **Eiginleika** til að opna **Eiginleika** síðu. Notið síðan eftirfarandi ferli til að stilla eiginleika fyrir handvirk ákvörðun.

## <a name="name-the-decision"></a>Heiti ákvörðunar.
Fylgið þessum skrefum til að færa inn heiti á handvirk ákvörðun.

1.  Í vinstri glugganum, smelltu á **grunnstillingar**.
2.  Á svæðinu **Heiti** skal færa inn einkvæmt heiti fyrir handvirk ákvörðun

## <a name="enter-a-subject-line-and-instructions"></a>Slá inn efnislínu og fyrirmæli
Veita verður þeim notendum, sem úthlutað er þetta handvirk ákvörðun, efnislínu og fyrirmæli. Til dæmis, ef verið er að skilgreina ákvörðun fyrir innkaupabeiðnir, mun notanda sem er úthlutað á ákvörðun sjá efnislínuna og fyrirmælin á **Innkaupabeiðnir** síðunni. Efnislínuna birtist á skilaboðaslánni á síðunni. Notandinn getur síðan smellt á teiknið á skilaboðaslánni til að sjá leiðbeiningar. Fylgið eftirfarandi skrefum til að slá inn efnislínu og fyrirmæli.

1.  Í vinstri glugganum, smelltu á **grunnstillingar**.
2.  Í flipanum **leiðbeiningar** í reitnum **efni vinnuliðs** svæðinu, færið inn efnislínuna.
3.  Til að sérsníða efnislínuna, er hægt að færa inn staðgengla. Staðgenglar eru settir í stað viðeigandi gagna þegar efnislínan birtist notendum. Fylgið eftirfarandi skrefum til að færa inn staðgengil:
    1.  Smellið á textahólfið þar sem staðgengillinn á að birtast.
    2.  Smella á **Setja inn staðgengil**
    3.  Í listanum sem birtist skal velja staðgengilinn til að setja inn.
    4.  Smellt er á **Setja inn**.

4.  Til að bæta þýðingum við efnislínuna skal fylgja þessum skrefum:
    1.  Smellt er á **Þýðingar**.
    2.  Á síðunni sem birtist er smellt á **bæta við**.
    3.  Í listanum sem birtist skal velja tungumálið sem verið er að færa inn í textanum.
    4.  Í svæðið **þýddur texti** skal færa inn textann.
    5.  Til að sérsníða textann geturðu sett inn staðgengla eins og lýst er í skrefi 3.
    6.  Smellið á **Loka**.

5.  Í **leiðbeiningar vinnuliðs** svæðinu, færið inn leiðbeiningar.
6.  Hægt er að sérsníða leiðbeiningarnar með því að færa inn staðgengla. Staðgenglar eru settir í stað viðeigandi gagna þegar leiðbeiningar birtist notendum. Fylgið eftirfarandi skrefum til að færa inn staðgengil:
    1.  Smellið á textahólfið þar sem staðgengillinn á að birtast.
    2.  Smella á **Setja inn staðgengil**
    3.  Í listanum sem birtist skal velja staðgengilinn til að setja inn.
    4.  Smellt er á **Setja inn**.

7.  Til að bæta þýðingum við leiðbeiningar skal fylgja þessum skrefum:
    1.  Smellt er á **Þýðingar**.
    2.  Á síðunni sem birtist er smellt á **bæta við**.
    3.  Í listanum sem birtist skal velja tungumálið sem verið er að færa inn í textanum.
    4.  Í svæðið **þýddur texti** skal færa inn textann.
    5.  Til að sérsníða textann geturðu sett inn staðgengla eins og lýst er í skrefi 6.
    6.  Smellið á **Loka**.

## <a name="specify-the-possible-outcomes-of-a-decision"></a>Tilgreina mögulega niðurstöðu ákvörðunar
Yfirleitt þegar skjal er tengt þeim sem tekur ákvörðun, fær sá sem tekur ákvörðun spurningu. Svar við spurningunni er yfirleitt **Já** eða **Nei**, eða **Satt** eða **Ósatt**. Fylgið eftirfarandi skrefum til að tilgreina mögulega niðurstöðu handvirku ákvörðuninni.

1.  Í vinstri glugganum, smelltu á **grunnstillingar**.
2.  Á flipanum **Niðurstöður** , á **Niðurstaða 1** skal færa inn heiti niðurstöðu eða valkostinn.
3.  Til að bæta þýðingum við útkomuna skal fylgja þessum skrefum:
    1.  Smellt er á **Þýðingar**.
    2.  Á síðunni sem birtist er smellt á **bæta við**.
    3.  Í listanum sem birtist skal velja tungumálið sem verið er að færa inn í textanum.
    4.  Í svæðið **þýddur texti** skal færa inn textann.
    5.  Smellið á **Loka**.

4.  Á flipanum **Niðurstaða 2** skal færa inn heiti niðurstöðu eða valkostinn.
5.  Til að bæta þýðingum við útkomuna skal fylgja þessum skrefum:
    1.  Smellt er á **Þýðingar**.
    2.  Á síðunni sem birtist er smellt á **bæta við**.
    3.  Í listanum sem birtist skal velja tungumálið sem verið er að færa inn í textanum.
    4.  Í svæðið **þýddur texti** skal færa inn textann.
    5.  Smellið á **Loka**.

## <a name="specify-when-notifications-are-sent"></a>Tilgreinið hvenær tilkynningar eru sendar út
Hægt er að senda tilkynningar til fólks þegar ákvörðun hefur verið tekin, framseld eða stigmögnuð. Fylgið eftirfarandi skrefum til að tilgreina hvenær senda á út tilkynningar og til hvers tilkynningar eru sendar.

1.  Á svæðinu vinstra megin, smella á **tilkynningar**.
2.  Veldu gátreitinn sem er við hliðina á tilvikunum sem tilkynningar eiga að vera senda vegna.
    -   **\[Val 1\]** – Úthlutaður notandi hefur valið **\[Val 1\]**.
    -   **\[Val 2\]** – Úthlutaður notandi hefur valið **\[Val 2\]**.
    -   **Framselja** – úthlutaður notandi hefur úthlutað ákvörðuninni til annars notanda.
    -   **Stigmagna** – úthlutaður notandi hefur ekki tekið ákvörðun innan tímarammans.

3.  Veljið línu fyrir tilvik sem þú valdir í skrefi 2.
4.  Á **tilkynningartexti** flipanum í textareitinn, færa inn texta tilkynningarinnar.
5.  Hægt er að sérsníða tilkynningu með því að færa inn staðgengla. Staðgenglar eru settir í stað viðeigandi gagna þegar tilkynning birtist notendum. Fylgið eftirfarandi skrefum til að færa inn staðgengil:
    1.  Smellið á textahólfið þar sem staðgengillinn á að birtast.
    2.  Smella á **Setja inn staðgengil**
    3.  Í listanum sem birtist skal velja staðgengilinn til að setja inn.
    4.  Smellt er á **Setja inn**.

6.  Til að bæta þýðingum við Tilkynningar skal fylgja þessum skrefum:
    1.  Smellt er á **Þýðingar**.
    2.  Á síðunni sem birtist er smellt á **bæta við**.
    3.  Í listanum sem birtist skal velja tungumálið sem verið er að færa inn í textanum.
    4.  Í svæðið **þýddur texti** skal færa inn textann.
    5.  Til að sérsníða textann geturðu sett inn staðgengla eins og lýst er í skrefi 5.
    6.  Smellið á **Loka**.

7.  Á **Viðtakanda** flipanum, tilgreinið hverjum tilkynningar eru sendar. Veljið einn af valkostum í eftirfarandi töflu, og fylgið svo viðbótarskref fyrir valkostinn áður en farið er í skrefi 8.
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Valkostur</th>
    <th>Viðtakendur tilkynninga.</th>
    <th>Viðbótarskref</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Þátttakendur</td>
    <td>Notendur sem tilheyra tilteknum hópi eða hlutverki</td>
    <td><ol>
    <li>Eftor að þú velur <strong>viðtakanda</strong>, Á flipanum <strong>Hlutverkamiðað</strong> , á listanum <strong>Gerð þátttakanda</strong> skal velja gerð hóps eða hlutverks til að senda tilkynningu á.</li>
    <li>Í listanum <strong>Þátttakanda</strong> skal velja hópi til að senda tilkynningar til.</li>
    </ol></td>
    </tr>
    <tr class="even">
    <td>Verkflæðisnotandi</td>
    <td>Notendur í núverandi verkflæði</td>
    <td><ul>
    <li>Eftir að þú velur <strong>verkflæðisnotandi</strong>, á <strong>verkflæðisnotandi</strong> flipanum, á <strong>verkflæðisnotandi</strong> listanum, veldu notandann sem tekur þátt í verkflæði.</li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td>Notandi</td>
    <td>Sértækir notendur Microsoft Dynamics 365 for Finance and Operations</td>
    <td><ol>
    <li>Eftir að þú velur <strong>Notanda</strong>, skal smellið á <strong>Notanda</strong> flipa.</li>
    <li>Listinn <strong>Tiltækir notendur</strong>: inniheldur alla notendur í Finance and Operations. Veldu Notendur til að senda tilkynningar til, og færðu síðan þessa notendur í <strong>Valdir notendur</strong> lista.</li>
    </ol></td>
    </tr>
    </tbody>
    </table>

8.  Endurtakið skref 3 til 7 hvert tilvik sem valin var í skrefi 2.

## <a name="assign-a-decision"></a>Úthluta ákvörðun
Farið að þessum skrefum til að tilgreina á hvern skal úthluta Handvirk Ákvörðun.

1.  Á vinstra svæðinu er smellt á **úthlutun**.
2.  Á flipanum **úthlutunargerð** , veljið einn af valkostum í eftirfarandi töflu, og fylgið svo viðbótarskref fyrir valkostinn áður en farið er í skrefi 3.
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Valkostur</th>
    <th>Notendur sem er úthlutað er ákvörðuninni</th>
    <th>Viðbótarskref</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Þátttakendur</td>
    <td>Notendur sem tilheyra tilteknum hópi eða hlutverki</td>
    <td><ol>
    <li>Eftir að þú velur <strong>Þátttakanda</strong>á flipanum <strong>Hlutverkamiðað</strong> , á listanum <strong>Gerð þátttakanda</strong> skal velja gerð hóps eða hlutverks til að úthluta ákvörðun á.</li>
    <li>Í listanum <strong>Þátttakanda</strong> skal velja hópi eða hlutverki til að úthluta ákvörðun á.</li>
    </ol></td>
    </tr>
    <tr class="even">
    <td>Stigveldi</td>
    <td>Notendur í tilteknu stigveldi fyrirtækis</td>
    <td><ol>
    <li>Eftir að þú velur <strong>stigveldi</strong>, á <strong>stigveldishluti</strong> flipanum, á listanum <strong>gerð stigveldis</strong> skal velja gerð stigveldis til að úthluta ákvörðun á.</li>
    <li>Kerfið verður að sækja svið notendanafna úr stigveldinu. Þessi nöfn standa fyrir notendur sem hægt er að úthluta ákvörðun á. Farðu að þessum skrefum til að tilgreina upphafspunkt og lokapunkt sviðs notendanafna sem kerfið sækir. <ol>
    <li>Þegar tilgreina á upphafspunkt skal velja aðila af listanum <strong>Byrja frá og með</strong>.</li>
    <li>Hægt er að tilgreina endapunkt með því að smella á <strong>bæta við skilyrði</strong>. Til að færa inn skilyrðu sem ákvarðar hvar í stigveldinu kerfið eigi að hætta að sækja nöfn.</li>
    </ol></li>
    <li>Á <strong>stigveldisvalkostir</strong> flipanum skal tilgreina hvaða notendur á sviðinu ákvörðun skal úthlutað á: <ul>
    <li><strong>Úthluta til allra sóttra notenda</strong> - þá er Ákvörðun úthlutað til allra notenda á sviðinu.</li>
    <li><strong>Úthluta eingöngu til síðasta sótta notanda</strong> - þá er ákvörðun aðeins úthlutað til síðasta notanda á sviðinu.</li>
    <li><strong>Sleppa notendum með eftirfarandi skilyrði</strong> – Ákvörðun er ekki úthlutað á notendur innan sviðsins sem uppfylla ákveðið skilyrði. Smellið á <strong>bæta við skilyrði </strong> til að skilgreina skilyrðin.</li>
    </ul></li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td>Verkflæðisnotandi</td>
    <td>Notendur í núverandi verkflæði</td>
    <td><ul>
    <li>Eftir að þú velur <strong>verkflæðisnotandi</strong>, á <strong>verkflæðisnotandi</strong> flipanum, á <strong>verkflæðisnotandi</strong> listanum, veldu notandann sem tekur þátt í verkflæði.</li>
    </ul></td>
    </tr>
    <tr class="even">
    <td>Notandi</td>
    <td>Sértækir notendur Finance and Operations</td>
    <td><ol>
    <li>Eftir að þú velur <strong>Notanda</strong>, skal smellið á <strong>Notanda</strong> flipa.</li>
    <li>Listinn <strong>Tiltækir notendur</strong>: inniheldur alla notendur í Finance and Operations. Veldu Notendur til að úthluta Ákvörðun á, og færa síðan þessa notendur í <strong>Valdir notendur</strong> lista.</li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td>Biðröð</td>
    <td>Vinnuliðalisti</td>
    <td><ol>
    <li>Eftir að <strong>Biðröð</strong> er valin, smellið á <strong>byggt á Biðröð</strong> flipa.</li>
    <li>Fylgið eftirfarandi skrefum til að úthluta Ákvörðun á tiltekna biðröð: <ol>
    <li>Í listanum <strong>gerð biðraðar </strong> skal velja <strong>vinnuliðalisti</strong></li>
    <li>Í <strong>heiti biðraðar</strong> listanum skal velja biðröðinni.</li>
    </ol></li>
    <li>Ef tiltekin skilyrði ætti að ákvarða hvaða biðröð Ákvörðun er úthlutað á, skal fylgja þessum skrefum: <ol>
    <li>Í listanum <strong>gerð biðraðar </strong> skal velja <strong>skilyrtir vinnuliðalistar</strong></li>
    <li>Í <strong>heiti biðraðar</strong> listanum skal velja <strong>skilyrt biðröð</strong>.</li>
    </ol></li>
    </ol>
    <strong>Athugasemd:</strong> Þessi valkostur er notaður fyrir aðeins nokkrar verkflæði, s.s. málastjórnun.</td>
    </tr>
    </tbody>
    </table>

3.  Á **tímamörk** flipanum, á svæðinu **Tímalengd** , tilgreinið hve mikinn tíma notandi hefur til að taka ákvörðunina. Veldu einn af eftirfarandi valkostum:
    -   **Klukkustundir** – færið Inn fjölda klukkustunda sem notandi hefur til að taka ákvörðunina. Þá velja dagatalið sem fyrirtækið notar og færa inn upplýsingar um vinnuviku fyrirtækisins.
    -   **Dagar** – færið Inn fjölda daga sem notandi hefur til að taka ákvörðunina. Þá velja dagatalið sem fyrirtækið notar og færa inn upplýsingar um vinnuviku fyrirtækisins.
    -   **Vikur** – færið Inn fjölda vikna sem notandi hefur til að taka ákvörðunina.
    -   **Mánuðir** — velja daginn og vikuna sem notandinn verður að vera búinn að taka ákvörðunina fyrir. Til dæmis, notandi getur óskað þess að annar notandi taka ákvörðunina fyrir föstudag í þriðju viku mánaðarins.
    -   **Ár** — velja daginn, vikuna og mánuðinn sem notandinn verður að vera búinn að taka ákvörðunina fyrir. Til dæmis, notandi getur óskað þess að annar notandi taka ákvörðunina fyrir föstudag í þriðju viku desembermánaðar.

    Ef notandinn tekur ekki ákvörðunina innan tímarammans, er ákvörðunin komið fram yfir á tíma. Ákvörðun sem er komið fram yfir á tíma er stigmagnað, á grundvelli valkostanna sem þú valdir í **stigmögnun** svæðið á síðunni.

## <a name="specify-what-happens-when-a-decision-is-overdue"></a>Tilgreina hvað gerist þegar ákvörðun er komið fram yfir á tíma
Ef notandinn tekur ekki ákvörðunina innan tímarammans, er ákvörðunin komið fram yfir á tíma. Ákvörðun sem er komið fram yfir á tíma má stigmagna, eða úthluta sjálfkrafa á annan notanda. Fylgið eftirfarandi skrefum til að stigmagna Ákvörðun ef það er komið fram yfir á tíma.

1.  Á vinstra svæðinu skaltu Smellt á **Stigmagna**.
2.  Velja skal **Nota stigmögnunarslóð** gátreit til að stofna stigmögnunarslóð. Kerfið mun sjálfkrafa úthluta Ákvörðun til notendanna sem skráðir eru í stigmögnunarslóðinni. Til dæmis, eftirfarandi töflu sýnir stigmögnunarslóð.
    | Röð | stigmögnunarslóð            |
    |----------|----------------------------|
    | 1        | Úthluta til: Dísu           |
    | 2        | Úthluta til: Erlu            |
    | 3        | Endanleg aðgerð: \[Val 1\] |

    Í þessu dæmi mun kerfið sjálfkrafa úthluta Ákvörðun sem er komið fram yfir á tíma til Dísu. Ef Dísu tekur ekki ákvörðun innan tímarammans, úthlutar kerfið ákvörðuninni til Erlu. Ef Erla tekur ekki ákvörðun innan tímarammans, Velur kerfið **\[Val 1\]** sem ákvörðun.
3.  Til að bæta notanda við stigmögnunarslóð, smella **bæta við stigmögnun**. Veljið einn af valkostum í eftirfarandi töflu, og fylgið svo viðbótarskref fyrir valkostinn áður en farið er í skrefi 4.
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Valkostur</th>
    <th>Notendur sem Ákvörðun er stigmagnað fyrir</th>
    <th>Viðbótarskref</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Stigveldi</td>
    <td>Notendur í tilteknu stigveldi fyrirtækis</td>
    <td><ol>
    <li>Eftir að þú velur <strong>stigveldi</strong>, á <strong>stigveldishluti</strong> flipanum, á listanum <strong>gerð stigveldis</strong> skal velja gerð stigveldis til að stigmagna ákvörðun fyrir.</li>
    <li>Kerfið verður að sækja svið notendanafna úr stigveldinu. Þessi nöfn standa fyrir notendur sem hægt er stigmagna Ákvörðun fyrir. Farðu að þessum skrefum til að tilgreina upphafspunkt og lokapunkt sviðs notendanafna sem kerfið sækir. <ol>
    <li>Þegar tilgreina á upphafspunkt skal velja aðila af listanum <strong>Byrja frá og með</strong>.</li>
    <li>Hægt er að tilgreina endapunkt með því að smella á <strong>bæta við skilyrði</strong>. Til að færa inn skilyrðu sem ákvarðar hvar í stigveldinu kerfið eigi að hætta að sækja nöfn.</li>
    </ol></li>
    <li>Á <strong>stigveldisvalkostir</strong> flipanum skal tilgreina hvaða notendur á sviðinu ákvörðun skal stigmagnað fyrir: <ul>
    <li><strong>Úthluta til allra sóttra notenda</strong> - þá er ákvörðun stigmagnað fyrir allra notenda á sviðinu.</li>
    <li><strong>Úthluta eingöngu til síðasta sótta notanda</strong> - þá er ákvörðun stigmagnað aðeins til síðasta notanda á sviðinu.</li>
    <li><strong>Sleppa notendum með eftirfarandi skilyrði</strong> – Ákvörðun er ekki stigmagnað fyrir neina notendur innan sviðsins sem uppfylla ákveðið skilyrði. Smellið á <strong>bæta við skilyrði </strong> til að skilgreina skilyrðin.</li>
    </ul></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td>Verkflæðisnotandi</td>
    <td>Notendur í núverandi verkflæði</td>
    <td><ul>
    <li>Eftir að þú velur <strong>verkflæðisnotandi</strong>, á <strong>verkflæðisnotandi</strong> flipanum, á <strong>verkflæðisnotandi</strong> listanum, veldu notandann sem tekur þátt í verkflæði.</li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td>Notandi</td>
    <td>Sértækir notendur Finance and Operations</td>
    <td><ol>
    <li>Eftir að þú velur <strong>Notanda</strong>, skal smellið á <strong>Notanda</strong> flipa.</li>
    <li>Listinn <strong>Tiltækir notendur</strong>: inniheldur alla notendur í Finance and Operations. Veldu Notendur til að stigmagna Ákvörðun fyrir, og færðu síðan þessa notendur í <strong>Valdir notendur</strong> lista.</li>
    </ol></td>
    </tr>
    </tbody>
    </table>

4.  Á **tímamörk** flipanum, á svæðinu **Tímalengd** , tilgreinið hve mikinn tíma notandi hefur til að taka ákvörðunina. Veldu einn af eftirfarandi valkostum:
    -   **Klukkustundir** – færið Inn fjölda klukkustunda sem notandi hefur til að taka ákvörðunina. Þá velja dagatalið sem fyrirtækið notar og færa inn upplýsingar um vinnuviku fyrirtækisins.
    -   **Dagar** – færið Inn fjölda daga sem notandi hefur til að taka ákvörðunina. Þá velja dagatalið sem fyrirtækið notar og færa inn upplýsingar um vinnuviku fyrirtækisins.
    -   **Vikur** – færið Inn fjölda vikna sem notandi hefur til að taka ákvörðunina.
    -   **Mánuðir** — velja daginn og vikuna sem notandinn verður að vera búinn að taka ákvörðunina fyrir. Til dæmis, notandi getur óskað þess að annar notandi taka ákvörðunina fyrir föstudag í þriðju viku mánaðarins.
    -   **Ár** — velja daginn, vikuna og mánuðinn sem notandinn verður að vera búinn að taka ákvörðunina fyrir. Til dæmis, notandi getur óskað þess að annar notandi taka ákvörðunina fyrir föstudag í þriðju viku desembermánaðar.

5.  Endurtakið skref 3 til 4 fyrir hvern notanda sem á að bæta við stigmögnunarslóð. Hægt er að breyta röðun notenda.
6.  Ef notendunum í hækkunarslóðinni taka ekki ákvörðun innan tímarammans, tekur kerfið ákvörðunina. Til að tilgreina valkostinn sem kerfið velur , veldu línuna **Aðgerð** , og síðan á **Ljúka aðgerð** flipanum, veljið valkost.

## <a name="set-a-time-limit"></a>Setja upp tímamörk
Fylgið eftirfarandi skrefum ef verður að taka ákvörðunina innan tiltekins tíma. **Athugasemd:** Valkostirnir sem valdir eru í þessu ferli munu hnekkja valkostunum sem valdir voru í svæðunum **úthlutun** og **stigmögnun** á síðunni.

1.  Í vinstri glugganum, smelltu á **ítarlegar stillingar**.
2.  Veldu gátreitinn **Stilla tímamörk verkflæðiseiningar**
3.  Í reitnum **tímalengd** tilgreinið þegar Ákvörðun á að vera tekin. Veldu einn af eftirfarandi valkostum:
    -   **Klukkustundir** - Færa þarf inn fjölda klukkustunda. Þá velja dagatalið sem fyrirtækið notar og færa inn upplýsingar um vinnuviku fyrirtækisins.
    -   **Dagar** - Færið inn fjölda daga. Þá velja dagatalið sem fyrirtækið notar og færa inn upplýsingar um vinnuviku fyrirtækisins.
    -   **Vikur** - Færið inn fjölda vikna.
    -   **Mánuðir** — velja daginn og vikuna sem verður að vera búið að taka ákvörðunina fyrir. Til dæmis getur átt að vera búið að taka ákvörðunina fyrir föstudaginn í þriðju viku mánaðarins.
    -   **Ár** — velja daginn, vikuna og mánuðinn sem verður að vera búið að taka ákvörðunina fyrir. Til dæmis getur átt að vera búið að taka ákvörðunina fyrir föstudaginn í þriðju viku desembermánaðar.

4.  Ef farið er yfir tímamörkin mun kerfið taka ákvörðunina vegna verksins. Veljið Valkost, sem kerfið á að velja, í listanum **Aðgerðir**.





