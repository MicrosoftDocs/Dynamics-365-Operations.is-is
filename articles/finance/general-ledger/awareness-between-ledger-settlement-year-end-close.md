---
title: Munurinn á fjárhagsjöfnun og árslokalokun
description: Þetta efnisatriði veitir upplýsingar um endurbætur sem hafa áhrif á fjárhagsuppgjör og árslok Fjárhags.
author: kweekley
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: e18f77d73239de23000b5310d9342c6db95bc524
ms.sourcegitcommit: c0f7ee7f8837fec881e97b2a3f12e7f63cf96882
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/22/2022
ms.locfileid: "8462353"
---
# <a name="awareness-between-ledger-settlement-and-year-end-close"></a>Munurinn á fjárhagsjöfnun og árslokalokun

[!include [banner](../includes/banner.md)]


Í Microsoft Dynamics 365 Finance útgáfa 10.0.25, the **Meðvitund milli uppgjörs fjárhags og ársloka** eiginleiki er fáanlegur í **Eiginleikastjórnun** vinnurými. Þessi eiginleiki bætir við tveimur aðalaukningum sem hafa áhrif á uppgjör fjárhags og ársloka aðalbókar.

Við lok ársreiknings fjárhags munu færslur sem hafa verið jafnaðar ekki lengur vera teknar með í upphafsjöfnuði næsta reikningsárs. Þessi aukning tryggir að aðeins óuppgerðar fjárhagsfærslur séu teknar með í upphafsjöfnuði. Það er mikilvægt þegar endurmat á erlendum gjaldmiðli í aðalbók er keyrt. Endurmat gjaldeyris er aðeins keyrt fyrir fjárhagsfærslur sem hafa stöðuna **Ekki afgreitt**. Hins vegar, áður en **Meðvitund milli uppgjörs fjárhags og ársloka** eiginleiki var gefinn út, upphafsstaðan tók saman bæði viðskiptin sem hafa stöðuna **Settist** og þeir sem hafa stöðu á **Ekki afgreitt**, og staðan á samantekinni upphæð var stillt á **Ekki afgreitt**.

Önnur viðbótin gerir þér kleift að bóka ítarlegar upphafsstöðufærslur við lok ársloka aðalbókar. Ef **Haltu smáatriðum í lok árs** valkostur er stilltur á **Já**, verður aðskilin upphafsstaða stofnuð fyrir hverja fjárhagsfærslu sem ekki er gerð upp. Þessi stilling er skilgreind fyrir hvern aðalreikning í uppsetningu fjárhagsuppgjörs. Með því að geyma ítarlegar færslur fyrir upphafsstöðuna bætir þú til muna getu til að jafna óuppgerðu fjárhagsfærslurnar á næsta fjárhagsári.

Til að styðja við nýjar endurbætur voru gerðar breytingar á fjárhagsuppgjöri og árslokum.

### <a name="changes-to-ledger-settlement"></a>Breytingar á fjárhagsuppgjöri

- Fjárhagsuppgjör verður að fara fram innan reikningsárs.
- Fjárhagsuppgjör verður að fara fram fyrir færslur á einum aðalreikningi. Aðalreikningurinn er nú nauðsynleg sía á **Fjárhagsuppgjör** síðu.
- Fjárhagsjöfnun og bakfærsla á uppgjöri fjárhags er ekki hægt að gera fyrir færslur sem eru bókaðar innan lokaðs fjárhagsárs (með öðrum orðum, árslokalokun hefur verið keyrð).

### <a name="changes-to-year-end-close"></a>Breytingar til ársloka

- Ekki er hægt að snúa við árslokum ef einhver stofnjöfnuður hefur verið gerður upp á næsta reikningsári. Þessi breyting á við þegar áramót er snúið við, eða þegar áramót er endurtekið og **Eyddu núverandi árslokafærslum þegar þú lokar árinu aftur** valkostur er stilltur á **Já** í færibreytum aðalbókar.
- Ef **Haltu smáatriðum í lok árs** valkostur er stilltur á **Já** fyrir hvaða efnahagsreikning sem er í fjárhagsuppgjöri verða til ítarlegri upphafsstöðufærslur fyrir þann aðalreikning.

## <a name="before-you-enable-the-feature"></a>Áður en þú virkjar eiginleikann

Vegna breytinga á virkni og gagnalíkaninu er mikilvægt að þú íhugar eftirfarandi atriði áður en þú virkjar eiginleikann:

- Allar færslur sem hafa verið merktar til uppgjörs en hafa ekki verið jafnaðar verða sjálfkrafa afmerktar þegar aðgerðin er virkjuð. Til að koma í veg fyrir vinnutap skaltu gera upp allar merktar færslur áður en þú virkjar eiginleikann.
- Sumar stofnanir halda árslokum mörgum sinnum fyrir sama fjárhagsár. Ekki virkja eiginleikann ef árslokalokun hefur þegar verið keyrð einu sinni og verður keyrð aftur fyrir sama fjárhagsár. Eiginleikinn verður að vera virkur áður en þú vinnur úr fyrstu árslokum eða eftir að þú vinnur úr síðustu áramótum fyrir fjárhagsárið.

  Ef þú vilt virkja eiginleikann, en árslokun hefur þegar verið keyrð einu sinni, verður þú að snúa við árslokun áður en þú getur virkjað eiginleikann.

- Vegna þess að uppgjör milli reikningsára er ekki lengur leyfð, mælum við með því að þú kveikir á eiginleikanum áður en þú byrjar lokaferli ársins. Síðan, til að tryggja að upphafsjöfnuður næsta reikningsárs verði ekki fyrir áhrifum af fyrri uppgjöri milli reikningsára, ætti að gera upp upphafsjöfnuðinn fyrir reikningsárið sem verið er að loka.
- Vegna þess að uppgjör milli aðalreikninga er ekki lengur leyfð skaltu breyta reikningaskránni þinni eða ferlum eftir þörfum til að tryggja að hægt sé að gera fjárhagsuppgjör á sama aðalreikningi.
- Ekki er hægt að virkja eiginleikann ef verið er að nota árslokaferli hins opinbera.

## <a name="set-up-ledger-settlement"></a>Setja upp fjárhagsuppgjör

Eftir að þú hefur virkjað eiginleikann, og áður en þú keyrir næstu áramótalokun, verður hvert fyrirtæki að ákveða hvort það muni halda færsluupplýsingunum við árslokun. Valið hefur engin áhrif á upphafsstöðufærslur frá fyrri lokaferli í árslok.

The **Haltu smáatriðum í lok árs** valkostur er stilltur fyrir hvern aðalreikning á **Uppsetning fjárhagsuppgjörs** síðu.

1.  Fara til **Aðalbók** > **Uppsetning höfuðbókar** > **Fjárhagsfæribreytur**.
2.  Á **Fjárhagsuppgjör** flipa, veldu **Fjárhagsuppgjörsreikningar**.

-eða-

1.  Fara til **Aðalbók** > **Reglubundin verkefni** > **Fjárhagsuppgjör**.
2.  Veldu **Fjárhagsuppgjörsreikningar**.

Tveimur dálkum hefur verið bætt við **Fjárhagsuppgjör** síða:
    
- **Aðalreikningstegund** – Þessi dálkur er eingöngu til upplýsinga. Það sýnir tegundina sem er úthlutað á aðalreikninginn.
- **Haltu smáatriðum í lok árs** – Sjálfgefið er valkosturinn stilltur á **Nei**. Það er hægt að stilla á **Já** aðeins ef gildið í **Aðalreikningstegund** dálkur er **Efnahagsreikningur**, **·**, eða **Ábyrgð**. Þegar valkosturinn er stilltur á **Nei**, upphafsstöður verða birtar í yfirliti, eins og dæmigert er við lok árs. Ef það er stillt á **Já**, verða upphafsstöður búnar til í smáatriðum fyrir hverja fjárhagsfærslu sem er ekki gerð upp fyrir aðalreikning.

## <a name="year-end-close"></a>Árslokalokun

Þegar þú keyrir áramót nálægt því að fara til **Aðalbók** > **Lokað tímabil** > **Lokaárslok**, ferlið stofnar upphafsstöður fyrir aðalreikninga sem eru skilgreindir fyrir fjárhagsuppgjör. Opnunarstöðurnar eru búnar til annað hvort í yfirliti eða smáatriðum, allt eftir uppsetningu fjárhagsuppgjörs. Ferlið útilokar fjárhagsfærslur sem eru jafnaðar, óháð því hvort upphafsstaða hvers aðalreiknings er bókuð í samantekt eða í smáatriðum.

Til dæmis eru margar færslur færðar inn á aðalreikning 130100 á reikningsárinu 2021.

| Færslubókarnúmer | Fylgiskjal  | Dagsetning       | Gerð      | Fjárhagslykill | Heiti lykils        | Lýsing       | Gjaldmiðill | Upphæð í gjaldmiðli færslu | Upphæð  | Upphæð í skýrslugjaldmiðli |
|----------------|----------|------------|-----------|----------------|---------------------|-------------------|----------|--------------------------------|---------|------------------------------|
| 20853          | FTV-3000 | 3.12.2021  | Í gangi | 130100-001-    | Viðskiptakröfur | Þjónustugjald       | USD      | 10.000                            | 10.000     | 10.000                          |
| 20855          | FTV-3004 | 5.12.2021  | Í gangi | 130100-002-    | Viðskiptakröfur | Veitur         | USD      | 175                            | 175     | 175                          |
| 20854          | CMV-4000 | 16.12.2021 | Í gangi | 130100-001-    | Viðskiptakröfur | Endurgreiðsla            | USD      | -100                           | -100    | -100                         |
| 20851          | ARP-8000 | 20.12.2021 | Í gangi | 130100-002-    | Viðskiptakröfur |                   | USD      | -0,88                          | -0,88   | -0,88                        |
| 20853          | ARPM0004 | 20.12.2021 | Í gangi | 130100-002-    | Viðskiptakröfur |                   | EUR      | -127.11                        | -174.12 | -174.12                      |
| 20856          | CMV-4010 | 21.12.2021 | Í gangi | 130100-002-    | Viðskiptakröfur | Inneign á reikningi | USD      | -175                           | -175    | -175                         |
| 20857          | FTV-3011 | 28.12.2021 | Í gangi | 130100-001-    | Viðskiptakröfur | Veitur         | USD      | 400                            | 400     | 400                          |
| 20910          | FTV-3020 | 29.12.2021 | Í gangi | 130100-002-    | Viðskiptakröfur | Þjónusta           | USD      | 300                            | 300     | 300                          |

Af þessum færslum eru þrjár jafnaðar við fjárhagsuppgjör.

Það er reikningur upp á 175 Bandaríkjadali (175 USD). Þessi reikningur var greiddur með greiðslu í evrum (EUR) og tekinn var staðgreiðsluafsláttur.

| Færslubókarnúmer | Fylgiskjal  | Dagsetning       | Gerð      | Fjárhagslykill | Heiti lykils        | Lýsing | Gjaldmiðill | Upphæð í gjaldmiðli færslu | Upphæð  | Upphæð í skýrslugjaldmiðli |
|----------------|----------|------------|-----------|----------------|---------------------|-------------|----------|--------------------------------|---------|------------------------------|
| 20855          | FTV-3004 | 5.12.2021  | Í gangi | 130100-002-    | Viðskiptakröfur | Veitur   | USD      | 175                            | 175     | 175                          |
| 20851          | ARP-8000 | 20.12.2021 | Í gangi | 130100-002-    | Viðskiptakröfur |             | USD      | -0,88                          | -0,88   | -0,88                        |
| 20853          | ARPM0004 | 20.12.2021 | Í gangi | 130100-002-    | Viðskiptakröfur |             | EUR      | -127.11                        | -174.12 | -174.12                      |

Niðurstöður fyrir aðalreikning 130100 ráðast af því hvort aðgerðin er virkjuð áður en árslokun er keyrð. Ef aðgerðin er virkjuð veltur niðurstaðan einnig á stillingunni á Hafðu smáatriði við lok ársloka.

### <a name="the-feature-isnt-enabled"></a>Eiginleikinn er ekki virkur
Árslokun skapar þrjár upphafsstöðufærslur fyrir aðalreikning 130100 árið 2022. Summa viðskiptanna í bókhaldsgjaldmiðlinum er USD 525.

| Færslubókarnúmer | Fylgiskjal  | Dagsetning     | Gerð    | Fjárhagslykill | Heiti lykils        | Lýsing | Gjaldmiðill | Upphæð í gjaldmiðli færslu | Upphæð  | Upphæð í skýrslugjaldmiðli |
|----------------|----------|----------|---------|----------------|---------------------|-------------|----------|--------------------------------|---------|------------------------------|
| 20910          | YEC_2021 | 1/1/2022 | Opnunarstaða | 130100-002-    | Viðskiptakröfur |             | USD      | 299.12                         | 299.12  | 299.12                       |
| 20910          | YEC_2021 | 1/1/2022 | Opnunarstaða | 130100-001-    | Viðskiptakröfur |             | USD      | 400                            | 400     | 400                          |
| 20910          | YEC_2021 | 1/1/2022 | Opnunarstaða | 130100-002-    | Viðskiptakröfur |             | EUR      | -127.11                        | -174.12 | -174.12                      |

Jafnvel þó að færslu greiðslunnar fyrir EUR -127,11 hafi verið gerð upp, kemur færslan samt fram sem upphafsstaða.

### <a name="feature-is-enabled-and-keep-detail-during-year-end-close--no"></a>Eiginleiki er virkur og Geymdu smáatriði í lok árs = Nei

Lokun ársins skapar tvær upphafsstöðufærslur fyrir aðalreikning 130100 árið 2022. Summa færslna í bókhaldsgjaldmiðlinum er enn USD 525, en færslur sem eru uppgjörðar í fjárhagsbók eru undanskildar upphafsstöðu. Heildarupphæð reikningsins 130100-002- er USD 125 í stað USD 299.12 og viðskiptin fyrir 127,11 EUR/USD 174,12 eru algjörlega útilokuð.

| Færslubókarnúmer | Fylgiskjal  | Dagsetning     | Gerð    | Fjárhagslykill | Heiti lykils        | Lýsing | Gjaldmiðill | Upphæð í gjaldmiðli færslu | Upphæð | Upphæð í skýrslugjaldmiðli |
|----------------|----------|----------|---------|----------------|---------------------|-------------|----------|--------------------------------|--------|------------------------------|
| 20910          | YEC_2021 | 1/1/2022 | Opnunarstaða | 130100-002-    | Viðskiptakröfur |             | USD      | 125                            | 125    | 125                          |
| 20910          | YEC_2021 | 1/1/2022 | Opnunarstaða | 130100-001-    | Viðskiptakröfur |             | USD      | 400                            | 400    | 400                          |

### <a name="feature-is-enabled-and-keep-detail-during-year-end-close--yes"></a>Eiginleikinn er virkur og Geymdu smáatriði í lok árs = Já

Lokun ársins skapar fimm upphafsstöðufærslur fyrir aðalreikning 130100 árið 2022. Sérstök upphafsjöfnuður færsla er búin til fyrir hverja af fimm færslum sem ekki voru gerð upp. Summa viðskiptanna í bókhaldsgjaldmiðlinum er enn USD 525.

| Færslubókarnúmer | Fylgiskjal  | Dagsetning     | Gerð    | Fjárhagslykill | Heiti lykils        | Lýsing       | Gjaldmiðill | Upphæð í gjaldmiðli færslu | Upphæð | Upphæð í skýrslugjaldmiðli |
|----------------|----------|----------|---------|----------------|---------------------|-------------------|----------|--------------------------------|--------|------------------------------|
| 20910          | YEC_2021 | 1/1/2022 | Opnunarstaða | 130100-001-    | Viðskiptakröfur | Þjónustugjald       | USD      | 10.000                            | 10.000    | 10.000                          |
| 20910          | YEC_2021 | 1/1/2022 | Opnunarstaða | 130100-001-    | Viðskiptakröfur | Endurgreiðsla            | USD      | -100                           | -100   | -100                         |
| 20910          | YEC_2021 | 1/1/2022 | Opnunarstaða | 130100-002-    | Viðskiptakröfur | Inneign á reikningi | USD      | -175                           | -175   | -175                         |
| 20910          | YEC_2021 | 1/1/2022 | Opnunarstaða | 130100-001-    | Viðskiptakröfur | Veitur         | USD      | 400                            | 400    | 400                          |
| 20910          | YEC_2021 | 1/1/2022 | Opnunarstaða | 130100-002-    | Viðskiptakröfur | Þjónusta           | USD      | 300                            | 300    | 300                          |

Þegar færsluupplýsingar eru geymdar hafa upprunalegu nákvæmu færslurnar ekki áhrif. Þeir eru áfram settir og óuppgerðir á því fjárhagsári sem verið er að loka. Afrit af þessum viðskiptum er búið til fyrir upphafsstöðuna. Eftirfarandi gildi úr upprunalegu færslunum eru afrituð í upphafsstöðufærslur.

- Fjárhagsreikningur (aðalreikningur og allar fjárhagsvíddir)
- Upphæðir í viðskipta-, bókhalds- og skýrslugjaldmiðlum
- Lýsing
- Bókunarlag
- Bókunargerð

   > [!NOTE]
   > Engum öðrum upphafsstöðufærslum er úthlutað bókunartegund. Þess vegna er hægt að nota bókunargerðina til að aðgreina upphafsfærslur sem voru færðar fram í smáatriðum.

Sumir reitir úr upprunalegu færslunum verða að breytast í ítarlegum færslum í upphafsjöfnuði. Dagsetning upphafsviðskipta er alltaf fyrsti dagur næsta reikningsárs. Færslubókarnúmerið verður að breytast og fylgiskjalsnúmerið breytist í gildið sem var slegið inn í glugganum fyrir lok ársloka.

Upplýsingar frá upphaflegum viðskiptum er að finna á **Fjárhagsuppgjör** síðu. Hver ítarleg opnunarjöfnuðsfærsla sýnir **Upprunaleg viðskiptadagsetning** dálki í ristinni. Þessi dálkur getur hjálpað þér að passa við færslur á nýju reikningsári. Þú getur valið **Skoða upprunalega skírteini** til að bora til baka að fullu upprunalegu fylgiskjali.

## <a name="settle-transactions"></a><a name="settle-transactions"></a>Jafna færslur
Til að jafn fjárhagsfærslur skaltu fylgja þessum skrefum.

1. Fara til **Aðalbók** > **Reglubundin verkefni** > **Fjárhagsuppgjör**.
2.  Stilltu síurnar efst á síðunni.

    1. Veldu tímabil. Að öðrum kosti, veldu dagsetningarbilskóða til að fylla út dagsetningarbilið sjálfkrafa.

       - Dagsetningarbilið getur ekki farið yfir reikningsár. Ef dagsetningarbilið fer yfir reikningsár munu engar færslur birtast þegar þú velur **Sýna viðskipti**.
       - Ef dagsetningarbilið er á opnu reikningsári er hægt að gera upp færslur og hægt er að bakfæra uppgjörið. Ef dagsetningarbilið er á lokuðu reikningsári, eða ef árslokun er lokið, eru færslur sýndar, en ekki er hægt að gera þær upp eða ójafnaðar. Aðeins er hægt að afmerkja færslur á lokuðu reikningsári. Ef dagsetningarbilið er á lokuðu reikningsári, er **Merktu valið**, **upp merktar færslur**, og **Bakfæra merktar færslur** hnappar eru ekki tiltækir.

    2. Veldu aðalreikninginn til að sýna færslur fyrir. Þessi reitur er áskilinn. Uppflettingin sýnir aðeins helstu reikninga sem eru valdir á **Fjárhagsuppgjör** síðu fyrir reikningsyfirlit félagsins.
    3. Veldu færslulagið. Þú getur ekki jafnað færslur sem eru í mismunandi bókunarlögum.
    4. Til að sýna aðalreikninginn og víddir í aðskildum dálkum, veljið fjárhagsvíddarsett.

3.  Veldu **Sýna viðskipti** til að sýna allar færslur sem passa við síurnar sem þú stillir. Ef þú breytir einhverjum síum eða víddarsamstæðum þarftu að velja **Birta færslur** aftur.
4.  Veldu línur til uppgjörs. Gildið í **Valin upphæð** reiturinn efst á síðunni hækkar eða lækkar til að endurspegla heildarupphæðina á völdum línum.
5.  Þegar þú hefur lokið við að velja færslur skaltu velja **Merktu valið**. Fyrir hverja valda færslu birtist gátmerki í **Merkt** dálki. Að auki, gildið í **Merkt magn** reiturinn fyrir ofan hnitanetið hækkar eða minnkar til að endurspegla heildarmagnið á merktu línunum.
6.  Þegar gildið í **Merkt magn** sviði er **0** (núll), veldu **Gerðu upp merktar færslur**.

    - Hlutauppgjör er óheimilt. Til dæmis er ekki hægt að jafna $100 debetfærslu á móti $90 kreditfærslu. Eftirstöðvar $10 inneignarfærslur verða einnig að vera merktar til að taka með í uppgjörið.
    - Sláðu inn uppgjörsdagsetningu. Dagsetningin verður að vera á eða eftir síðasta dagsetningu viðskiptanna sem eru merkt til uppgjörs.

Staða valinna færslna er uppfært í **Jafnað**.

> [!IMPORTANT]
> Allar færslur sem þú hefur merkt til uppgjörs fyrir virka lögaðilann og valda aðalreikninginn verða jafnaðar. Viðskiptin þurfa ekki að birtast á síðunni. Þeir verða settir jafnvel þótt þeir séu falir vegna síu.

Sum ferli, eins og bakfærsla á færslu, jafna sjálfkrafa fjárhagsfærslur. Til dæmis er greiðsla og reikningur gerður upp í viðskiptakröfum og uppgjörið skapar innleyst hagnað/tap. Uppgjör greiðslu og reiknings jafnar ekki neinar fjárhagsfærslur, svo sem færslur fyrir viðskiptareikninga. Hins vegar, ef greiðsla og reikningur er óuppgerður í viðskiptakröfum, mun bakfærsla bókhaldsfærslunnar sem var bókuð við bakfærslu á viðskiptakröfuuppgjöri valda því að upprunalegu og bakfærðu bókhaldsfærslurnar verða jafnaðar í fjárhag. Þegar **Meðvitund milli uppgjörs fjárhags og ársloka** eiginleiki er virkjaður, fjárhagsuppgjör bakfærslu á sér ekki sjálfkrafa sér stað ef bakfærsludagsetningin er á öðru fjárhagsári.

## <a name="use-excel-for-ledger-settlement"></a>Notaðu Excel fyrir fjárhagsuppgjör

Viðskipti sem eru sýnd á **Fjárhagsuppgjör** síðu er hægt að flytja út í Excel. Í Excel er hægt að sía færslur frekar til að ákvarða hvaða færslur á að merkja fyrir uppgjör.
Báðar fjárhagsjöfnunareiningar flytja út bókhaldsfærslur eingöngu fyrir aðalreikninginn sem er valinn á **Fjárhagsuppgjör** síðu. Þó að enn sé hægt að merkja eða afmerkja færslur fyrir lokuð reikningsár með því að nota Excel, þá er ekki hægt að jafna þær. Að auki er ekki hægt að bakfæra uppgjörnar færslur fyrir það reikningsár.

## <a name="make-transactions-easier-to-find"></a>Gera það auðveldara að finna færslur

The **Fjárhagsuppgjör** síðu inniheldur möguleika sem gera það auðveldara að skoða færslurnar sem þú þarfnast fyrir uppgjör.

• Nota **Merkt** sía til að sía viðskipti út frá því hvort **Merkt** gátreiturinn fyrir þá er valinn.
• Nota **Staða** sía til að sía viðskipti út frá stöðu þeirra.
• Veldu **Raða eftir algeru magni** að flokka upphæðirnar eftir algildi. Þannig er hægt að flokka skuldir og inneignir sem hafa sömu upphæð.

## <a name="reverse-a-settlement"></a>Bakfæra jöfnun

Þú getur bakfært jöfnun sem var gerð fyrir mistök.

1.  Fylgdu skrefum 1 til 3 í [Gera upp viðskipti](#settle-transactions) kafla til að sýna færslurnar sem þú hefur áhuga á.
2.  Í **Staða** síu, veldu **Jöfnuð**.
3.  Veldu línur til að snúa við.
4.  Veldu **Bakfæra merktar færslur**. Staða allra færslna sem hafa sama uppgjörsauðkenni er uppfærð í **Ekki afgreitt**.

> [!IMPORTANT]
> Allar færslur sem hafa sama uppgjörsauðkenni verða bakfærðar, jafnvel þótt þær séu ekki merktar. Til dæmis voru fjórar línur merktar og afgreiddar. Allar fjórar línurnar eru með sama uppgjörsauðkenni. Ef þú merkir við eina af þessum fjórum línum og velur síðan **Bakfæra merktar færslur**, allar fjórar línurnar verða snúnar við.






