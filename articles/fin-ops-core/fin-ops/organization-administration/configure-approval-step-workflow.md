---
title: Grunnstilla samþykktarskref í verkflæði
description: Þetta efnisatriði útskýrir hvernig skilgreina á eiginleika samþykktarskrefs.
author: ChrisGarty
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 192161
ms.assetid: 8b478e3d-d6b4-403b-aae0-f639a71ca36c
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 09f32833d914c05a1830e2bba36ebe4c66a8a52c
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/19/2020
ms.locfileid: "4797097"
---
# <a name="configure-approval-steps-in-a-workflow"></a>Grunnstilla samþykktarskref í verkflæði

[!include [banner](../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig skilgreina á eiginleika samþykktarskrefs.

Til að skilgreina samþykktarskref í verkflæðisritlinum, er hægrismellt á samþykktarskrefið og smellið síðan á **Eiginleika** til að opna í **Eiginleika** síðu. Notið síðan eftirfarandi ferli til að stilla eiginleika fyrir samþykktarskref.

## <a name="name-the-step"></a>Gefa skrefinu heiti
Fylgið þessum skrefum til að færa inn heiti á samþykktarskrefinu.

1. Í vinstri glugganum, smelltu á **grunnstillingar**.
2. Á svæðinu **Heiti** skal færa inn einkvæmt heiti fyrir samþykktarskref

## <a name="enter-a-subject-line-and-instructions"></a>Slá inn efnislínu og fyrirmæli

Veita verður þeim notendum, sem úthlutað er þessu samþykktarskref, efnislínu og fyrirmæli. Til dæmis, ef verið er að skilgreina samþykktarskref fyrir innkaupabeiðnir, mun notanda er úthlutað á skrefið sjá efnislínuna og fyrirmælin á **Innkaupabeiðnir** síðunni. Efnislínuna birtist á skilaboðaslánni á síðunni. Notandinn getur síðan smellt á teiknið á skilaboðaslánni til að sjá leiðbeiningar. Fylgið eftirfarandi skrefum til að slá inn efnislínu og fyrirmæli.

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

## <a name="assign-the-approval-step"></a>Úthluta þessu samþykktarskrefi

Farið að þessum skrefum til að tilgreina á hvern skal úthluta samþykktarskref.

1. Á vinstra svæðinu er smellt á **úthlutun**.
2. Á flipanum **úthlutunargerð** , veljið einn af valkostum í eftirfarandi töflu, og fylgið svo viðbótarskref fyrir valkostinn áður en farið er í skrefi 3.

    <table>
    <thead>
    <tr>
    <th>Valkostur</th>
    <th>Notandi sem samþykktarskref er úthlutað á.</th>
    <th>Viðbótarskref</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>Þátttakendur</td>
    <td>Notendur sem tilheyra tilteknum hópi eða hlutverki</td>
    <td>
    <ol>
    <li>Eftir að þú velur <strong>Þátttakanda</strong>á flipanum <strong>Hlutverkamiðað</strong> , á listanum <strong>Gerð þátttakanda</strong> skal velja gerð hóps eða hlutverks til að úthluta skrefinu á.</li>
    <li>Í listanum <strong>Þátttakanda</strong> skal velja hópi eða hlutverki til að úthluta skrefinu á.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Stigveldi</td>
    <td>Notendur í tilteknu stigveldi fyrirtækis</td>
    <td>
    <ol>
    <li>Eftir að þú velur <strong>stigveldi</strong>, á <strong>stigveldishluti</strong> flipanum, á listanum <strong>gerð stigveldis</strong> skal velja gerð stigveldis til að úthluta skrefinu á.</li>
    <li>Kerfið verður að sækja svið notendanafna úr stigveldinu. Þessi nöfn standa fyrir notendur sem hægt er að úthluta skrefinu á. Farðu að þessum skrefum til að tilgreina upphafspunkt og lokapunkt sviðs notendanafna sem kerfið sækir. <ol>
    <li>Þegar tilgreina á upphafspunkt skal velja aðila af listanum <strong>Byrja frá og með</strong>.</li>
    <li>Hægt er að tilgreina endapunkt með því að smella á <strong>bæta við skilyrði</strong>. Til að færa inn skilyrðu sem ákvarðar hvar í stigveldinu kerfið eigi að hætta að sækja nöfn.</li>
    </ol>
    </li>
    <li>Á <strong>stigveldisvalkostir</strong> flipanum skal tilgreina hvaða notendur á sviðinu skrefinu skal úthlutað á: <ul>
    <li><strong>Úthluta til allra sóttra notenda</strong> - þá er samþykktarskrefið úthlutað til allra notenda á sviðinu.</li>
    <li><strong>Úthluta eingöngu til síðasta sótta notanda</strong> - þá er skrefið aðeins úthlutað til síðasta notanda á sviðinu.</li>
    <li><strong>Sleppa notendum með eftirfarandi skilyrði</strong> – skrefið er ekki úthlutað á notendur innan sviðsins sem uppfylla ákveðið skilyrði. Smellið á <strong>bæta við skilyrði</strong> til að skilgreina skilyrðin.</li>
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
    <li>Listinn <strong>Tiltækir notendur</strong> inniheldur alla kerfisnotendur. Veldu Notendur til að úthluta skrefi á, og færsa íðan þessa notendur í <strong>Valdir notendur</strong> lista.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

3. Á **tímamörk** flipanum, á svæðinu **Tímalengd** , tilgreinið hve mikinn tíma notandi hefur til að bregðast við eða svara skjölum sem ná samþykktarskrefi. Veldu einn af eftirfarandi valkostum:

    - **Klukkustundir** – færið Inn fjölda klukkustunda sem notandi hefur til að bregðast við. Þá velja dagatalið sem fyrirtækið notar og færa inn upplýsingar um vinnuviku fyrirtækisins.
    - **Dagar** – færið Inn fjölda daga sem notandi hefur til að bregðast við. Þá velja dagatalið sem fyrirtækið notar og færa inn upplýsingar um vinnuviku fyrirtækisins.
    - **Vikur** – færið Inn fjölda vikna sem notandi hefur til að bregðast við.
    - **Mánuðir** — velja daginn og vikuna sem notandinn verður að vera búinn að bregðast við fyrir. Til dæmis, notandi getur óskað þess að annar notandi bregðist við á föstudegi í þriðju viku mánaðarins.
    - **Ár** — velja daginn, vikuna og mánuðinn sem notandinn verður að vera búinn að bregðast við fyrir. Til dæmis, notandi getur óskað þess að annar notandi bregðist við á föstudegi í þriðju viku desembermánaðar.

    Ef notandinn bregst ekki við skjalinu á tilgreindum tíma, er skjalið komið fram yfir á tíma. Skjal sem er komið fram yfir á tíma er stigmagnað, á grundvelli valkostanna sem þú valdir í **stigmögnun** svæðið á síðunni.

4. Ef samþykktarskrefið var úthlutað til margra notenda eða flokk af notendum, á **regla um lok** flipanum, veljið einn af eftirfarandi valkostum:

    - **Stakur samþykktaraðili** - aðgerðin fyrir skjalið ákveðin af fyrsta aðilanum sem bregst við. Til dæmis hefur Samúel sent kostnaðarskýrslu upp á $15.000. Kostnaðarskýrslu er í augnablikinu úthlutað á Brynju, Guðrúnu og Gísla. Ef Brynja er sú fyrsta sem bregst við skjalinu þá er hennar aðgerð notuð fyrir skjalið. Ef Brynja hafnar skjalinu þá er því hafnað og sent tilbaka til Samúels. Þegar Brynja samþykkir skjalið er það sent til Önnu til samþykktar.

        ![Verkflæði sem er með samþykktarferli](./media/workflow_multipleusersinstep.gif)

    - **Meirihluti samþykkjenda** - aðgerðin fyrir skjalið ákveðin þegar flestir af samþykktaraðilum bregðast við. Til dæmis hefur Samúel sent kostnaðarskýrslu upp á $15.000. Kostnaðarskýrslu er í augnablikinu úthlutað á Brynju, Guðrúnu og Gísla. Ef Brynja og Guðrún eru fyrstu tveir samþykktaraðilar sem svara, er aðgerðin sem þær grípa til beitt fyrir skjalið.

        - Ef Brynja samþykkir skjalið og Guðrún hafnar því þá er því hafnað og sent tilbaka til Samúels.
        - Ef Brynja og Guðrún samþykkja skjalið þá er skjalið sent til Önnu til samþykktar.

    - **Hlutfall samþykkjenda** - aðgerðin fyrir skjalið ákveðin þegar ákveðið hlutfall af samþykktaraðilum svara. Til dæmis hefur Samúel sent kostnaðarskýrslu upp á $15.000. Kostnaðarskýrslu er í augnablikinu úthlutað á Brynju, Guðrúnu og Gísla, og þú færðir inn **50** sem hlutfall. Ef Brynja og Guðrún eru fyrstu tveir samþykktaraðilar sem svara, er aðgerðin sem þær grípa til beitt fyrir skjalið, af því að þær uppfylla kröfurnar um 50 prósent samþykktaraðila.

        - Ef Brynja samþykkir skjalið og Guðrún hafnar því þá er því hafnað og sent tilbaka til Samúels.
        - Ef Brynja og Guðrún samþykkja skjalið þá er skjalið sent til Önnu til samþykktar.

    - **Allir samþykkjendur** – Allir samþykkjendur verða að samþykkja skjalið. Annars getur verkflæði ekki haldið áfram. Til dæmis hefur Samúel sent kostnaðarskýrslu upp á $15.000. Kostnaðarskýrslu er í augnablikinu úthlutað á Brynju, Guðrúnu og Gísla. Ef Brynja og Guðrún samþykkja skjalið og Gísli hafnar því þá er því hafnað og sent tilbaka til Samúels. Ef Brynja og Guðrún samþykkja skjalið þá er skjalið sent til Önnu til samþykktar.

## <a name="specify-when-the-approval-step-is-required"></a>Tilgreina hvenær samþykktarskrefið er nauðsynlegt

Hægt er að tilgreina hvenær samþykktarskrefið er nauðsynlegt. Samþykktarskrefið getur alltaf verið nauðsynlegt eða það getur verið nauðsynlegt aðeins ef tiltekin skilyrði eru uppfyllt.

### <a name="the-approval-step-is-always-required"></a>Þetta samþykktarskref er alltaf nauðsynlegt

Fylgið eftirfarandi skrefum ef samþykktarskrefið er alltaf nauðsynleg.

1. Á vinstra svæðinu er smellt á **Skilyrði**.
2. Veljið valkostinn **Alltaf að keyra þetta skref**.

### <a name="the-approval-step-is-required-in-specific-conditions"></a>Þetta samþykktarskref er nauðsynlegt við sérstök skilyrði.

Það getur verið að samþykktarskrefið sem verið er að skilgreina sé aðeins nauðsynlegt við sérstök skilyrði. T.d. ef verið er að skilgreina samþykktarskref fyrir verkflæði innkaupabeiðna, viltu kannski að þetta samþykktarskref komi aðeins upp ef upphæð innkaupabeiðni er meira en 10.000 USD. Fylgið eftirfarandi skrefum til að tilgreina hvenær krafist er samþykktarskrefið.

1. Á vinstra svæðinu er smellt á **Skilyrði**.
2. Veljið valkostinn **Keyra á þessu þrepi aðeins þegar eftirfarandi skilyrði eru í gildi**.
3. Færið inn skilyrði.
4. Færið inn öll önnur skilyrði sem krafist er.
5. Til að sannreyna að skilyrðin sem voru færð hafi verið sett upp rétt, skal fylgja eftirfarandi skrefum:

    1. Smellið á **Prófun**.
    2. Á síðunni **Kanna verkflæðisskilyrði** , í **Villuleita skilyrði** svæði, velja færslu.
    3. Smellið á **Prófun**. Kerfið metur færsluna og ákveður hvort hún standist skilyrði sem þú tiltókst.
    4. Smelltu á **Í lagi** eða **hætta við** til að fara aftur síðuna **forstillingar**.

## <a name="specify-what-happens-when-the-document-is-overdue"></a>Tilgreina hvað gerist þegar skjal er í vanskilum

Ef notandinn bregst ekki við skjalinu á tilgreindum tíma, er skjalið komið fram yfir á tíma. Skjal sem er komið fram yfir á tíma getur verið stigmagnað eða sjálfkrafa úthlutað til annars notanda til samþykkis. Fylgið eftirfarandi skrefum til að stigmagna skjalið ef það er komið fram yfir á tíma.

1. Á vinstra svæðinu skaltu Smellt á **Stigmagna**.
2. Velja skal **Nota stigmögnunarslóð** gátreit til að stofna stigmögnunarslóð. Kerfið mun sjálfkrafa úthluta skjalinu til notendanna sem skráðir eru í stigmögnunarslóðinni. Til dæmis, eftirfarandi töflu sýnir stigmögnunarslóð.

    | Röð | stigmögnunarslóð      |
    |----------|----------------------|
    | 1        | Úthluta til: Dísu     |
    | 2        | Úthluta til: Erlu      |
    | 3        | Endanleg aðgerð: Hafna |

    Í þessu dæmi mun kerfið sjálfkrafa úthluta skjalinu sem er komið fram yfir á tíma til Dísu. Ef Dísu ekki svarar innan tímarammans, úthlutar kerfið skjalinu til Erlu. Ef Erla ekki svarar innan tímarammans, hafnar kerfið skjalinu.

3. Til að bæta notanda við stigmögnunarslóð, smella **bæta við stigmögnun**. Á flipanum **úthlutunargerð** , veljið einn af valkostum í eftirfarandi töflu, og fylgið svo viðbótarskref fyrir valkostinn áður en farið er í skrefi 4.

    <table>
    <thead>
    <tr>
    <th>Valkostur</th>
    <th>Notendur sem skjalið er stigmagnað fyrir</th>
    <th>Viðbótarskref</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>Stigveldi</td>
    <td>Notendur í tilteknu stigveldi fyrirtækis</td>
    <td>
    <ol>
    <li>Eftir að þú velur <strong>stigveldi</strong>, á <strong>stigveldishluti</strong> flipanum, á listanum <strong>gerð stigveldis</strong> skal velja gerð stigveldis til stigmagna skjalinu fyrir.</li>
    <li>Kerfið verður að sækja svið notendanafna úr stigveldinu. Þessi nöfn standa fyrir notendur sem hægt er stigmagna skjalið fyrir. Farðu að þessum skrefum til að tilgreina upphafspunkt og lokapunkt sviðs notendanafna sem kerfið sækir. <ol>
    <li>Þegar tilgreina á upphafspunkt skal velja aðila af listanum <strong>Byrja frá og með</strong>.</li>
    <li>Hægt er að tilgreina endapunkt með því að smella á <strong>bæta við skilyrði</strong>. Til að færa inn skilyrðu sem ákvarðar hvar í stigveldinu kerfið eigi að hætta að sækja nöfn.</li>
    </ol>
    </li>
    <li>Á <strong>stigveldisvalkostir</strong> flipanum skal tilgreina hvaða notendur á sviðinu skjalið skal vera stigmagnað fyrir. <ul>
    <li><strong>Úthluta til allra sóttra notenda</strong> - þá er skjalið stigmagnað fyrir allra notenda á sviðinu.</li>
    <li><strong>Úthluta eingöngu til síðasta sótta notanda</strong> - þá er skjalið stigmagnað aðeins til síðasta notanda á sviðinu.</li>
    <li><strong>Sleppa notendum með eftirfarandi skilyrði</strong> – skjalið er ekki stigmagnað fyrir neina notendur innan sviðsins sem uppfylla ákveðið skilyrði. Smellið á <strong>bæta við skilyrði</strong> til að skilgreina skilyrðin.</li>
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
    <li>Listinn <strong>Tiltækir notendur</strong> inniheldur alla notendur. Veldu Notendur til að stigmagna skjali fyrir, og færðu síðan þessa notendur í <strong>Valdir notendur</strong> lista.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. Á **tímamörk** flipanum, á svæðinu **Tímalengd** , tilgreinið hve mikinn tíma notandi hefur til að bregðast við eða svara skjölum. Veldu einn af eftirfarandi valkostum:

    - **Klukkustundir** – færið Inn fjölda klukkustunda sem notandi hefur til að bregðast við. Þá velja dagatalið sem fyrirtækið notar og færa inn upplýsingar um vinnuviku fyrirtækisins.
    - **Dagar** – færið Inn fjölda daga sem notandi hefur til að bregðast við. Þá velja dagatalið sem fyrirtækið notar og færa inn upplýsingar um vinnuviku fyrirtækisins.
    - **Vikur** – færið Inn fjölda vikna sem notandi hefur til að bregðast við.
    - **Mánuðir** — velja daginn og vikuna sem notandinn verður að vera búinn að bregðast við fyrir. Til dæmis, notandi getur óskað þess að annar notandi bregðist við á föstudegi í þriðju viku mánaðarins.
    - **Ár** — velja daginn, vikuna og mánuðinn sem notandinn verður að vera búinn að bregðast við fyrir. Til dæmis, notandi getur óskað þess að annar notandi bregðist við á föstudegi í þriðju viku desembermánaðar.

5. Endurtakið skref 3 til 4 fyrir hvern notanda sem á að bæta við stigmögnunarslóð. Hægt er að breyta röðun notenda.
6. Ef notendunum í stigmögnunarslóðinni svara ekki innan tímarammans, grípur kerfið sjálfkrafa til aðgerða varðandi skjalið. Til að tilgreina aðgerðina sem kerfið grípur til, veldu línuna **Aðgerð** , og síðan á **Ljúka aðgerð** flipanum, veljið aðgerð.
