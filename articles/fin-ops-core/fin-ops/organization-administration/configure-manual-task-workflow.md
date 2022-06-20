---
title: Skilgreina handvirk verk í verkflæði
description: Þessi grein útskýrir hvernig á að stilla eiginleika fyrir handvirkt verkefni.
author: ChrisGarty
ms.date: 08/23/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 192191
ms.assetid: 27f1afde-ff26-4b6f-8c11-27ec49130bbb
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 265f127f948aa7425c5eb523abe18986a942cfb0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8889208"
---
# <a name="configure-manual-tasks-in-a-workflow"></a>Skilgreina handvirk verk í verkflæði

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Þessi grein útskýrir hvernig á að stilla eiginleika fyrir handvirkt verkefni.

Til að skilgreina handvirkt verk í verkflæðisritlinum, hægrismellt er á verkið og smellið síðan á **Eiginleika** til að opna **Eiginleika** síðu. Notið síðan eftirfarandi ferli til að stilla eiginleika fyrir handvirkt verk.

## <a name="name-the-task"></a>Gefa verkinu heiti

Fylgið þessum skrefum til að færa inn heiti á handvirku verki.

1. Í vinstri glugganum, smelltu á **grunnstillingar**.
2. Á svæðinu **Heiti** skal færa inn einkvæmt heiti fyrir verkið.

## <a name="enter-a-subject-line-and-instructions"></a>Slá inn efnislínu og fyrirmæli

Veita verður þeim notendum, sem úthlutað er þetta verk, efnislínu og fyrirmæli. Til dæmis, ef verið er að skilgreina verk fyrir innkaupabeiðnir, mun notanda sem er úthlutað á verkið sjá efnislínuna og fyrirmælin á **Innkaupabeiðnir** síðunni. Efnislínuna birtist á skilaboðaslánni á síðunni. Notandinn getur síðan smellt á teiknið á skilaboðaslánni til að sjá leiðbeiningar. Fylgið eftirfarandi skrefum til að slá inn efnislínu og fyrirmæli.

1. Í vinstri glugganum, smelltu á **grunnstillingar**.
2. Í **efni vinnuliðs** svæðinu, færið inn efnislínuna.
3. Til að sérsníða efnislínuna, er hægt að færa inn staðgengla. Staðgenglar eru settir í stað viðeigandi gagna þegar efnislínan birtist notendum. Fylgið eftirfarandi skrefum til að færa inn staðgengil:

    1. Smellið á textahólfið þar sem staðgengillinn á að birtast.
    2. Smella á **Setja inn staðgengil**
    3. Í listanum sem birtist skal velja staðgengilinn til að setja inn.
    4. Smellt er á **Setja inn**.

4. Til að bæta þýðingum við efnislínuna skal fylgja þessum skrefum:

    1. Smellt er á **Þýðingar**.
    2. Á síðunni sem birtist er smellt á **bæta við**.
    3. Í listanum sem birtist skal velja tungumálið sem verið er að færa inn í textanum.
    4. Í svæðið **þýddur texti** skal færa inn textann.
    5. Til að sérsníða textann geturðu sett inn staðgengla eins og lýst er í skrefi 3.
    6. Smellið á **Loka**.

5. Í **leiðbeiningar vinnuliðs** svæðinu, færið inn leiðbeiningar.
6. Hægt er að sérsníða leiðbeiningarnar með því að færa inn staðgengla. Staðgenglar eru settir í stað viðeigandi gagna þegar leiðbeiningar birtist notendum. Fylgið eftirfarandi skrefum til að færa inn staðgengil:

    1. Smellið á textahólfið þar sem staðgengillinn á að birtast.
    2. Smella á **Setja inn staðgengil**
    3. Í listanum sem birtist skal velja staðgengilinn til að setja inn.
    4. Smellt er á **Setja inn**.

7. Til að bæta þýðingum við leiðbeiningar skal fylgja þessum skrefum:

    1. Smellt er á **Þýðingar**.
    2. Á síðunni sem birtist er smellt á **bæta við**.
    3. Í listanum sem birtist skal velja tungumálið sem verið er að færa inn í textanum.
    4. Í svæðið **þýddur texti** skal færa inn textann.
    5. Til að sérsníða textann geturðu sett inn staðgengla eins og lýst er í skrefi 6.
    6. Smellið á **Loka**.

## <a name="assign-the-task"></a>Verkinu úthlutað

Farið að þessum skrefum til að tilgreina á hvern skal úthluta Handvirk verk.

1. Á vinstra svæðinu er smellt á **úthlutun**.
2. Á flipanum **úthlutunargerð** , veljið einn af valkostum í eftirfarandi töflu, og fylgið svo viðbótarskref fyrir valkostinn áður en farið er í skrefi 3.

    <table>
    <thead>
    <tr>
    <th>Valkostur</th>
    <th>Notandi sem verkið er úthlutað á.</th>
    <th>Viðbótarskref</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>Þátttakendur</td>
    <td>Notendur sem tilheyra tilteknum hópi eða hlutverki</td>
    <td>
    <ol>
    <li>Eftir að þú velur <strong>Þátttakanda</strong>á flipanum <strong>Hlutverkamiðað</strong> , á listanum <strong>Gerð þátttakanda</strong> skal velja gerð hóps eða hlutverks til að úthluta Verk á.</li>
    <li>Í listanum <strong>Þátttakanda</strong> skal velja hópi eða hlutverki til að úthluta Verk á.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Stigveldi</td>
    <td>Notendur í tilteknu stigveldi fyrirtækis</td>
    <td>
    <ol>
    <li>Eftir að þú velur <strong>stigveldi</strong>, á <strong>stigveldishluti</strong> flipanum, á listanum <strong>gerð stigveldis</strong> skal velja gerð stigveldis til að úthluta verk á.</li>
    <li>Kerfið verður að sækja svið notendanafna úr stigveldinu. Þessi nöfn standa fyrir notendur sem hægt er að úthluta verk á. Farðu að þessum skrefum til að tilgreina upphafspunkt og lokapunkt sviðs notendanafna sem kerfið sækir. <ol>
    <li>Þegar tilgreina á upphafspunkt skal velja aðila af listanum <strong>Byrja frá og með</strong>.</li>
    <li>Hægt er að tilgreina endapunkt með því að smella á <strong>bæta við skilyrði</strong>. Til að færa inn skilyrðu sem ákvarðar hvar í stigveldinu kerfið eigi að hætta að sækja nöfn.</li>
    </ol>
    </li>
    <li>Á <strong>stigveldisvalkostir</strong> flipanum skal tilgreina hvaða notendur á sviðinu verki skal úthlutað á: <ul>
    <li><strong>Úthluta til allra sóttra notenda</strong> - þá er verkinu úthlutað til allra notenda á sviðinu.</li>
    <li><strong>Úthluta eingöngu til síðasta sótta notanda</strong> - þá er verkinu aðeins úthlutað til síðasta notanda á sviðinu.</li>
    <li><strong>Sleppa notendum með eftirfarandi skilyrði</strong> – verkið er ekki úthlutað á notendur innan sviðsins sem uppfylla ákveðið skilyrði. Smellið á <strong>bæta við skilyrði</strong> til að skilgreina skilyrðin.</li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Verkflæðisnotandi</td>
    <td>Notendur í núverandi verkflæði</td>
    <td>
    <ul>
    <li>Eftir að þú velur <strong>verkflæðisnotandi</strong>, á <strong>verkflæðisnotandi</strong> flipanum, á <strong>verkflæðisnotandi</strong> listanum, veldu notandann sem tekur þátt í verkflæði.</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>Notandi</td>
    <td>Tilteknir notendur</td>
    <td>
    <ol>
    <li>Eftir að þú velur <strong>Notanda</strong>, skal smellið á <strong>Notanda</strong> flipa.</li>
    <li>Listinn <strong>Tiltækir notendur</strong> inniheldur alla notendur. Veldu Notendur til að úthluta verki á, og færa síðan þessa notendur í <strong>Valdir notendur</strong> lista.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Biðröð</td>
    <td>Vinnuliðalisti</td>
    <td>
    <ol>
    <li>Eftir að <strong>Biðröð</strong> er valin, smellið á <strong>byggt á Biðröð</strong> flipa.</li>
    <li>Fylgið eftirfarandi skrefum til að úthluta verki á tiltekna biðröð: <ol>
    <li>Í listanum <strong>gerð biðraðar</strong> skal velja <strong>vinnuliðalisti</strong></li>
    <li>Í <strong>heiti biðraðar</strong> listanum skal velja biðröðinni.</li>
    </ol>
    </li>
    <li>Ef tiltekin skilyrði ætti að ákvarða hvaða biðröð verki er úthlutað á, skal fylgja þessum skrefum: <ol>
    <li>Í listanum <strong>gerð biðraðar</strong> skal velja <strong>skilyrtir vinnuliðalistar</strong></li>
    <li>Í <strong>heiti biðraðar</strong> listanum skal velja <strong>skilyrt biðröð</strong>.</li>
    </ol>
    </li>
    </ol>
    <blockquote>[!NOTE] Þessi valkostur er notaður fyrir aðeins nokkur verkflæði, á borð við Málastjórnun.</blockquote>
    </td>
    </tr>
    </tbody>
    </table>

3. Á **tímamörk** flipanum, á svæðinu **Tímalengd** , tilgreinið hve mikinn tíma notandi hefur til að klára verkið. Veldu einn af eftirfarandi valkostum:

    - **Klukkustundir** – færið Inn fjölda klukkustunda sem notandi hefur til að klára verkið. Þá velja dagatalið sem fyrirtækið notar og færa inn upplýsingar um vinnuviku fyrirtækisins.
    - **Dagar** – færið Inn fjölda daga sem notandi hefur til að klára verkið. Þá velja dagatalið sem fyrirtækið notar og færa inn upplýsingar um vinnuviku fyrirtækisins.
    - **Vikur** – færið Inn fjölda vikna sem notandi hefur til að klára verkið.
    - **Mánuðir** — velja daginn og vikuna sem notandinn verður að vera búinn að klára verkið fyrir. Til dæmis getur notandinn átt að vera búinn að ljúka verkinu fyrir föstudaginn í þriðju viku mánaðarins.
    - **Ár** — velja daginn, vikuna og mánuðinn sem notandinn verður að vera búinn að klára verkið fyrir. Til dæmis getur notandinn átt að vera búinn að ljúka verkinu fyrir föstudaginn í þriðju viku desembermánaðar.

    Ef notandinn klárar ekki verkið innan tímarammans, er verkið komið fram yfir á tíma. Verk sem er komið fram yfir á tíma er hægt að stigmagna, á grundvelli valkostanna sem þú valdir í **stigmögnun** svæðið á síðunni.

## <a name="specify-what-happens-when-the-task-is-overdue"></a>Tilgreina hvað ætti að gerast þegar verk er komið fram yfir á tíma.

Ef notandinn klárar ekki handvirka verkið innan tímarammans, er verkið komið fram yfir á tíma. Verk sem er komið fram yfir á tíma má stigmagna, eða úthluta sjálfkrafa á annan notanda. Fylgið eftirfarandi skrefum til að stigmagna Verk ef það er komið fram yfir á tíma.

1. Á vinstra svæðinu skaltu Smellt á **Stigmagna**.
2. Velja skal **Nota stigmögnunarslóð** gátreit til að stofna stigmögnunarslóð. Kerfið mun sjálfkrafa úthluta verk til notendanna sem skráðir eru í stigmögnunarslóðinni. Til dæmis, eftirfarandi töflu sýnir stigmögnunarslóð.

    | Röð | stigmögnunarslóð      |
    |----------|----------------------|
    | 1        | Úthluta til: Dísu     |
    | 2        | Úthluta til: Erlu      |
    | 3        | Endanleg aðgerð: Hafna |

    Í þessu dæmi mun kerfið sjálfkrafa úthluta verki sem er komið fram yfir á tíma til Dísu. Ef Dísu klárar ekki verkið innan tímarammans, úthlutar kerfið verkinu til Erlu. Ef Erla ekki klárar ekki verkið innan tímarammans, hafnar kerfið skjalinu sem var sent inn til vinnslu.

3. Til að bæta notanda við stigmögnunarslóð, smella **bæta við stigmögnun**. Á flipanum **úthlutunargerð** , veljið einn af valkostum í eftirfarandi töflu, og fylgið svo viðbótarskref fyrir valkostinn áður en farið er í skrefi 4.

    <table>
    <thead>
    <tr>
    <th>Valkostur</th>
    <th>Notendur sem verkið er stigmagnað fyrir</th>
    <th>Viðbótarskref</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>Stigveldi</td>
    <td>Notendur í tilteknu stigveldi fyrirtækis</td>
    <td>
    <ol>
    <li>Eftir að þú velur <strong>stigveldi</strong>, á <strong>stigveldishluti</strong> flipanum, á listanum <strong>gerð stigveldis</strong> skal velja gerð stigveldis til stigmagna verk fyrir.</li>
    <li>Kerfið verður að sækja svið notendanafna úr stigveldinu. Þessi nöfn standa fyrir notendur sem hægt er stigmagna verk fyrir. Farðu að þessum skrefum til að tilgreina upphafspunkt og lokapunkt sviðs notendanafna sem kerfið sækir. <ol>
    <li>Þegar tilgreina á upphafspunkt skal velja aðila af listanum <strong>Byrja frá og með</strong>.</li>
    <li>Hægt er að tilgreina endapunkt með því að smella á <strong>bæta við skilyrði</strong>. Til að færa inn skilyrðu sem ákvarðar hvar í stigveldinu kerfið eigi að hætta að sækja nöfn.</li>
    </ol>
    </li>
    <li>Á <strong>stigveldisvalkostir</strong> flipanum skal tilgreina hvaða notendur á sviðinu verk skal vera stigmagnað fyrir. <ul>
    <li><strong>Úthluta til allra sóttra notenda</strong> - þá er verk stigmagnað fyrir allra notenda á sviðinu.</li>
    <li><strong>Úthluta eingöngu til síðasta sótta notanda</strong> - þá er verk stigmagnað aðeins til síðasta notanda á sviðinu.</li>
    <li><strong>Sleppa notendum með eftirfarandi skilyrði</strong> – verkið er ekki stigmagnað fyrir notendur innan sviðsins sem uppfylla ákveðið skilyrði. Smellið á <strong>bæta við skilyrði</strong> til að skilgreina skilyrðin.</li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Verkflæðisnotandi</td>
    <td>Notendur í núverandi verkflæði</td>
    <td>
    <ul>
    <li>Eftir að þú velur <strong>verkflæðisnotandi</strong>, á <strong>verkflæðisnotandi</strong> flipanum, á <strong>verkflæðisnotandi</strong> listanum, veldu notandann sem tekur þátt í verkflæði.</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>Notandi</td>
    <td>Tilteknir notendur</td>
    <td>
    <ol>
    <li>Eftir að þú velur <strong>Notanda</strong>, skal smellið á <strong>Notanda</strong> flipa.</li>
    <li>Listinn <strong>Tiltækir notendur</strong> inniheldur alla notendur. Veldu Notendur til að stigmagna verk fyrir, og færðu síðan þessa notendur í <strong>Valdir notendur</strong> lista.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. Á **tímamörk** flipanum, á svæðinu **Tímalengd** , tilgreinið hve mikinn tíma notandi hefur til að klára verkið. Veldu einn af eftirfarandi valkostum:

    - **Klukkustundir** – færið Inn fjölda klukkustunda sem notandi hefur til að klára verkið. Þá velja dagatalið sem fyrirtækið notar og færa inn upplýsingar um vinnuviku fyrirtækisins.
    - **Dagar** – færið Inn fjölda daga sem notandi hefur til að klára verkið. Þá velja dagatalið sem fyrirtækið notar og færa inn upplýsingar um vinnuviku fyrirtækisins.
    - **Vikur** – færið Inn fjölda vikna sem notandi hefur til að klára verkið.
    - **Mánuðir** — velja daginn og vikuna sem notandinn verður að vera búinn að klára verkið fyrir. Til dæmis getur notandinn átt að vera búinn að ljúka verkinu fyrir föstudaginn í þriðju viku mánaðarins.
    - **Ár** — velja daginn, vikuna og mánuðinn sem notandinn verður að vera búinn að klára verkið fyrir. Til dæmis getur notandinn átt að vera búinn að ljúka verkinu fyrir föstudaginn í þriðju viku desembermánaðar.

5. Endurtakið skref 3 til 4 fyrir hvern notanda sem á að bæta við stigmögnunarslóð. Hægt er að breyta röðun notenda.
6. Ef notendunum í stigmögnunarslóðinni klára ekki verkefni innan tímarammans, grípur kerfið til aðgerða varðandi verkið. Til að tilgreina aðgerðina sem kerfið grípur til, veldu línuna **Aðgerð** , og síðan á **Ljúka aðgerð** flipanum, veljið aðgerð.

## <a name="specify-when-the-system-automatically-acts-on-the-task"></a>Tilgreindu hvenær kerfið bregst sjálfkrafa við vegna verks.

Þú getur skilgreint krefið til að grípa til aðgerða vegna handvirka verksins þegar tilteknum skilyrðum er uppfyllt. Til dæmis krefst verk að meðlimur kostnaðarskýrsludeildarinnar endurskoði innhreyfingarnar sem eru sendar með kostnaðarskýrslu. Samkvæmt stefnu fyrirtækisins verður að framkvæma þetta verk ef heildarupphæð kostnaðarskýrslu er meiri en 100 USD. Í þessu dæmi, er hægt að skilgreina kerfið þannig að það merkir sjálfkrafa verkið sem **Lokið** þegar heildarupphæðin er lægri en 100. Fylgið eftirfarandi skrefum til að tilgreina hvenær kerfið grípur til aðgerða vegna handvirks verks.

1. Í vinstri glugganum, smelltu á **sjálfvirkar aðgerðir**.
2. Útvíkkið gátreitur **virkja sjálfvirkar aðgerðir** .
3. Smellt er á **Bæta við Skilyrði**.
4. Færið inn skilyrði.
5. Færið inn öll önnur skilyrði sem krafist er.
6. Til að sannreyna að skilyrðin sem voru færð hafi verið sett upp rétt, skal fylgja eftirfarandi skrefum:

    1. Smellið á **Prófun**.
    2. Á síðunni **Kanna verkflæðisskilyrði** , í **Villuleita skilyrði** svæði, velja færslu.
    3. Smellið á **Prófun**. Kerfið metur færsluna og ákveður hvort hún standist skilyrði sem þú tiltókst.
    4. Smelltu á **Í lagi** eða **hætta við** til að fara aftur síðuna **forstillingar**.

7. Í listanum **ljúka aðgerð sjálfvirkt** skal velja aðgerðina sem kerfið á að grípa til vegna verksins.

## <a name="specify-when-notifications-are-sent"></a>Tilgreinið hvenær tilkynningar eru sendar út

Hægt er að senda tilkynningar til fólks þegar handvirku verki hefur verið framselja, stigmagnað, lokið, eða hafnað, eða þegar beðið hefur verið um breytingu. Fylgið eftirfarandi skrefum til að tilgreina hvenær senda á út tilkynningar og til hvers tilkynningar eru sendar.

1. Á svæðinu vinstra megin, smella á **tilkynningar**.
2. Veldu gátreitinn sem er við hliðina á tilvikunum sem tilkynningar eiga að vera senda vegna.

    - **Framselja** – verki hefur verið úthlutað til annars notanda.
    - **Stigmagna** – úthlutaður notandi hefur ekki lokið verkinu innan tímarammans.
    - **Ljúka** – úthlutaður notandi hefur lokið verkinu.
    - **Hafna** – úthlutaður notandi hefur hafnað skjalinu sem var sent.
    - **Biðja um breytingu** – úthlutaður notandi hefur beðið um breytingu á skjalinu sem var sent.

3. Veljið línu fyrir tilvik sem þú valdir í skrefi 2.
4. Á **tilkynningartexti** flipanum í textareitinn, færa inn texta tilkynningarinnar.
5. Hægt er að sérsníða tilkynningu með því að færa inn staðgengla. Staðgenglar eru settir í stað viðeigandi upplýsinga þegar tilkynning birtist notanda. Fylgið eftirfarandi skrefum til að færa inn staðgengil:

    1. Smellið á textahólfið þar sem staðgengillinn á að birtast.
    2. Smella á **Setja inn staðgengil**
    3. Í listanum sem birtist skal velja staðgengilinn til að setja inn.
    4. Smellt er á **Setja inn**.

6. Til að bæta þýðingum við Tilkynningar skal fylgja þessum skrefum:

    1. Smellt er á **Þýðingar**.
    2. Á síðunni sem birtist er smellt á **bæta við**.
    3. Í listanum sem birtist skal velja tungumálið sem verið er að færa inn í textanum.
    4. Í svæðið **þýddur texti** skal færa inn textann.
    5. Til að sérsníða textann geturðu sett inn staðgengla eins og lýst er í skrefi 5.
    6. Smellið á **Loka**.

7. Á **Viðtakanda** flipanum, tilgreinið hverjum tilkynningar eru sendar. Veljið einn af valkostum í eftirfarandi töflu, og fylgið svo viðbótarskref fyrir valkostinn áður en farið er í skrefi 8.

    <table>
    <thead>
    <tr>
    <th>Valkostur</th>
    <th>Viðtakendur tilkynninga.</th>
    <th>Viðbótarskref</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>Þátttakendur</td>
    <td>Notendur sem tilheyra tilteknum hópi eða hlutverki</td>
    <td>
    <ol>
    <li>Eftor að þú velur <strong>viðtakanda</strong>, Á flipanum <strong>Hlutverkamiðað</strong> , á listanum <strong>Gerð þátttakanda</strong> skal velja gerð hóps eða hlutverks til að senda tilkynningu á.</li>
    <li>Í listanum <strong>Þátttakanda</strong> skal velja hópi eða hlutverk til að senda tilkynningar til.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Verkflæðisnotandi</td>
    <td>Notendur í núverandi verkflæði</td>
    <td>
    <ul>
    <li>Eftir að þú velur <strong>verkflæðisnotandi</strong>, á <strong>verkflæðisnotandi</strong> flipanum, á <strong>verkflæðisnotandi</strong> listanum, veldu notandann sem tekur þátt í verkflæði.</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>Notandi</td>
    <td>Tilteknir notendur</td>
    <td>
    <ol>
    <li>Eftir að þú velur <strong>Notanda</strong>, skal smellið á <strong>Notanda</strong> flipa.</li>
    <li>Listinn <strong>Tiltækir notendur</strong> inniheldur alla notendur. Veldu Notendur til að senda tilkynningar til, og færðu síðan þessa notendur í <strong>Valdir notendur</strong> lista.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. Endurtakið skref 3 til 7 hvert tilvik sem valin var í skrefi 2.

## <a name="set-a-time-limit"></a>Setja upp tímamörk

Fylgið eftirfarandi skrefum ef verður að ljúka handvirku verki innan tiltekins tíma.

> [!NOTE]
> Valkostirnir sem valdir eru í þessu ferli munu hnekkja valkostunum sem valdir voru í svæðunum **Úthlutun** og **Stigmögnun** á síðunni.

1. Í vinstri glugganum, smelltu á **ítarlegar stillingar**.
2. Veldu gátreitinn **Stilla tímamörk verkflæðiseiningar**
3. Í reitnum **tímalengd** tilgreinið þegar Verk á að vera lokið. Veldu einn af eftirfarandi valkostum:

    - **Klukkustundir** – færið Inn fjölda klukkustunda sem notandi hefur til að klára verkið. Þá velja dagatalið sem fyrirtækið notar og færa inn upplýsingar um vinnuviku fyrirtækisins.
    - **Dagar** – færið Inn fjölda daga sem notandi hefur til að klára verkið. Þá velja dagatalið sem fyrirtækið notar og færa inn upplýsingar um vinnuviku fyrirtækisins.
    - **Vikur** – færið Inn fjölda vikna sem notandi hefur til að klára verkið.
    - **Mánuðir** — velja daginn og vikuna sem verður að vera búið að klára verkið fyrir. Til dæmis getur átt að vera búið að ljúka verkinu fyrir föstudaginn í þriðju viku mánaðarins.
    - **Ár** — velja daginn, vikuna og mánuðinn sem verður að vera búið að klára verkið fyrir. Til dæmis getur átt að vera búið að ljúka verkinu fyrir föstudaginn í þriðju viku desembermánaðar.

4. Ef farið er yfir tímamörkin mun kerfið grípa til aðgerða vegna verksins. Veljið aðgerðina, sem kerfið á að framkvæma, í listanum **Aðgerðir**.

## <a name="specify-which-actions-are-available-to-the-user"></a>Tilgreina hvaða aðgerðir verða tiltækar notandanum.

Þegar notandi fær handvirkt verk úthlutað verður hann að vinna að verkinu. Fylgið eftirfarandi skrefum til að tilgreina hvaða aðgerðir notandi getur gripið til vegna verksins.

> [!NOTE]
> Mismunandi aðgerðir eru í boði, fer eftir hönnun verksins.

1. Í vinstri glugganum, smelltu á **ítarlegar stillingar**.
2. Veljið gátreitinn **Lokið** ef notandinn á að geta merkt við verkið sem **lokið**.
3. Veljið gátreitinn **hafna** ef notandinn á að geta hafnað skjalinu sem var sent inn.
4. Veljið gátreitinn **Biðja um breytingu** ef notandinn á að geta beðið um breytingar á skjalinu sem sent var inn.
5. Veljið gátreitinn **framselja** ef notandinn á að geta framselt verkinu til annars notanda.
6. Veljið gátreitinn **endurúthluta** ef notandinn á að geta endurúthlutað verkinu til annars notanda í vinnuliðalistanum.
7. Veljið gátreitinn **Losa** ef notandinn á að geta endurúthlutað verkinu til vinnuliðalista. Annar notandi getur þá ljúka verkefninu.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]