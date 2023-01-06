---
title: Munurinn á fjárhagsjöfnun og árslokalokun
description: Þessi grein veitir upplýsingar um úrbætur sem hafa áhrif á fjárhagsjafnanir og árslokalokun fjárhagsins.
author: kweekley
ms.date: 04/06/2022
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
ms.openlocfilehash: 30d3cc0bbd97cd006f12d06cda64ee63cb42252e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902517"
---
# <a name="awareness-between-ledger-settlement-and-year-end-close"></a>Munurinn á fjárhagsjöfnun og árslokalokun

[!include [banner](../includes/banner.md)]


Í Microsoft Dynamics 365 Finance, útgáfu 10.0.25, er eiginleikinn **Munurinn á fjárhagsjöfnun og árslokalokun** í boði á vinnusvæðinu **Eiginleikastjórnun**. Þessi eiginleiki bætir við tveimur úrbótum sem hafa áhrif á fjárhagsjöfnun og árslokalokun fjárhagsins.

Við árslokalokun fjárhags verða fjárhagsfærslur sem hafa verið jafnaðar ekki lengur hafðar með í opnunarstöðu næsta reikningsárs. Þessi úrbót tryggir að aðeins ójafnaðar fjárhagsfærslur eru hafðar með í opnunarstöðunni. Það er mikilvægt þegar endurmat á erlendum gjaldmiðli fjárhagsins er keyrt. Endurmat á erlendum gjaldmiðli er aðeins keyrt fyrir fjárhagsfærslur sem eru með stöðuna **Ekki jafnað**. Áður en eiginleikinn **Munurinn á fjárhagsjöfnun og árslokalokun** var gefinn út tók opnunarstaðan saman bæði færslur með stöðuna **Jafnað** og stöðuna **Ekki jafnað** og staða samantekinnar upphæðar var stillt á **Ekki jafnað**.

Seinni úrbótin gerir þér kleift að bóka ítarlegar færslur opnunarstöðu við árslokalokun fjárhagsins. Ef valkosturinn **Halda upplýsingum í árslokalokun** er stilltur á **Já** verður aðskilin opnunarstaða búin til fyrir hverja fjárhagsfærslu sem ekki er jöfnuð. Þessi stilling er skilgreind fyrir hvern aðallykil í uppsetningu fjárhagsjöfnunar. Með því að halda ítarlegum færslum fyrir opnunarstöðuna bætir þú mjög möguleika þína á að jafna ójafnaðar fjárhagsfærslur á næsta reikningsári.

Til að styðja við nýju úrbæturnar voru gerðar breytingar á fjárhagsjöfnun og árslokalokun.

### <a name="changes-to-ledger-settlement"></a>Breytingar á fjárhagsjöfnun

- Fjárhagsjöfnun verður að fara fram innan reikningsárs.
- Gera þarf fjárhagsjöfnun fyrir færslur í einum aðallykli. Aðallykillinn er nú nauðsynleg sía á síðunni **Fjárhagsjöfnun**.
- Ekki er hægt að gera fjárhagsjöfnun og bakfærslu fjárhagsjöfnunar fyrir færslur sem eru bókaðar innan lokaðs reikningsárs (m.ö.o. búið er að keyra árslokalokunina).

### <a name="changes-to-year-end-close"></a>Breytingar á lokun í árslok

- Ekki er hægt að bakfæra árslokalokun ef búið er að jafna einhverjar færslur opnunarstöðu á næsta reikningsári. Þessi breyting á við þegar árslokalokun er bakfærð eða þegar árslokalokun er endurkeyrð og valkosturinn **Eyða fyrirliggjandi árslokafærslum þegar ári er lokað aftur** er stilltur á **Já** í færibreytum fjárhags.
- Ef valkosturinn **Halda upplýsingum í árslokalokun** er stilltur á **Já** fyrir einhvern efnahagslykil í fjárhagsjöfnuninni verða ítarlegri færslur opnunarstöðu stofnaðar fyrir aðallykilinn.

## <a name="before-you-enable-the-feature"></a>Áður en eiginleikinn er virkjaður

Vegna breytinga á virkni og gagnalíkani er mikilvægt að hafa eftirfarandi atriði í huga áður en eiginleikinn er virkjaður:

- Vegna þess að aðeins jafnaðar færslur eru færðar áfram í opnunarstöðuna þarf að bakfæra jöfnun færslna á núverandi reikningsári sem eru jafnaðar við færslur á fyrra reikningsári. Jafna þarf færslurnar aftur á móti færslum innan núverandi reikningsárs. Þetta er hægt að gera í gegnum leiðréttingarfærslu á núverandi reikningsári. Leiðréttingin bakfærir samanteknum opnunarstöðum og jafnar við ítarlega færslu sem þarf til að jafna fjárhagsfærslurnar á núverandi ári. 

  > [!IMPORTANT]
  > Ef þetta er ekki gert færðu **skekkju** villu þegar árslokalokun er keyrð fyrir núverandi reikningsár. Ef ekki er hægt að bakfæra jöfnun og jafna aftur fjárhagsfærslurnar við sama fjárhagsárið skal ekki virkja þennan eiginleika fyrr en árslokalokun er lokið. Virkja þennan eiginleika strax eftir að árslokum er lokið og áður en nýjar fjárhagsfærslur eru jafnaðar á næsta reikningsári. 
  
- Allar færslur sem hafa verið merktar fyrir jöfnun en hafa ekki verið jafnaðar sjálfkrafa verða afmerktar þegar eiginleikinn er virkjaður. Til að koma í veg fyrir vinnutap skaltu jafna allar merktar færslur áður en eiginleikinn er virkjaður.
- Sum fyrirtæki keyra árslokalokun mörgum sinnum fyrir sama reikningsárið. Ekki virkja eiginleikann ef árslokalokun hefur þegar verið keyrð einu sinni og verður keyrð aftur fyrir sama reikningsárið. Virkja þarf eiginleikann áður en unnið er úr fyrstu árslokalokun eða eftir að unnið hefur verið úr síðustu árslokalokun fyrir reikningsárið.

  Ef virkja á eiginleikann en árslokalokunin hefur verið keyrð einu sinni þarf að bakfæra árslokalokunina áður eiginleikinn er virkjaður.

- Vegna þess að jöfnun yfir aðallykla er ekki lengur leyfð skaltu breyta bókhaldslyklum eða ferlum eins og þarf til að tryggja að hægt sé að framkvæma fjárhagsjöfnun í sama aðallyklinum.
- Ekki er hægt að virkja eiginleikann ef ferli árslokalokunar fyrir opinbera geirann er í notkun.

## <a name="set-up-ledger-settlement"></a>Setja upp fjárhagsjöfnun

Eftir að eiginleikinn er virkjaður og áður en næsta árslokalokun er keyrð þarf hvert fyrirtæki að ákveða hvort það vilji halda færsluupplýsingum í árslokalokuninni. Valið hefur engin áhrif á að bókanir á opnunarstöðum frá fyrri ferlum árslokalokunar.

Valkosturinn **Halda upplýsingum í árslokalokun** er stilltur fyrir hvern aðallykil á síðunni **Uppsetning fjárhagsjöfnunar**.

1.  Opnið **Fjárhagur** >  **Fjárhagsuppsetning**  >  **Færibreytur fyrir fjárhag**.
2.  Í flipanum **Fjárhagsjafnanir** skal velja **Lykla fjárhagsjöfnunar**.

-eða-

1.  Opnið **Fjárhagur**  >  **Reglubundin verkefni**  >  **Fjárhagsuppgjör**.
2.  Veljið **Lyklar fjárhagsuppgjörs**.

Tveimur dálkum hefur verið bætt við síðuna **Fjárhagsjafnanir**:
    
- **Aðallykilgerð** – Þessi dálkur er eingöngu til upplýsinga. Það sýnir gerðina sem er úthlutað á aðallykilinn.
- **Halda upplýsingum í árslokalokun** – Valkosturinn er sjálfgefið stilltur á **Nei**. Hægt er að stilla hann á **Já** aðeins ef gildið í dálknum **Aðallykilgerð** er **Efnahagsreikningur**, **Eign** eða **Skuld**. Þegar valkosturinn er stilltur á **Nei** verða opnunarstöður bókaðar í samantekt eins og er venjulega gert í árslokalokun. Ef hann er stilltur á **Já** verða opnunarstöður búnar til í smáatriðum fyrir hverja fjárhagsfærslu sem er ekki jöfnuð fyrir aðallykilinn.

## <a name="year-end-close"></a>Árslokalokun

Þegar árslokalokun er keyrð með því að fara í **Fjárhagur** > **Lokun tímabils** > **Árslokalokun** býr ferlið til opnunarstöður fyrir aðallyklana sem eru skilgreindir fyrir fjárhagsjöfnun. Opnunarstöðurnar eru búnar til í annaðhvort samantekt eða smáatriðum eftir því hver uppsetningin er á fjárhagsjöfnuninni. Ferlið útilokar fjárhagsfærslur sem eru jafnaðar burtséð frá því hvort þú bókir opnunarstöðuna fyrir hvern aðallykil í samantekt eða smáatriðum.

Til dæmis eru margar færslur bókaðar á aðallykil 130100 á reikningsárinu 2021.

| Færslubókarnúmer | Fylgiskjal  | Dagsetning       | Gerð      | Fjárhagslykill | Heiti lykils        | Lýsing       | Gjaldmiðill | Upphæð í gjaldmiðli færslu | Upphæð  | Upphæð í skýrslugjaldmiðli |
|----------------|----------|------------|-----------|----------------|---------------------|-------------------|----------|--------------------------------|---------|------------------------------|
| 20853          | FTV-3000 | 3/12/2021  | Í gangi | 130100-001-    | Viðskiptakröfur | Þjónustugjald       | USD      | 10.000                            | 10.000     | 10.000                          |
| 20855          | FTV-3004 | 5/12/2021  | Í gangi | 130100-002-    | Viðskiptakröfur | Hjálparforrit         | USD      | 175                            | 175     | 175                          |
| 20854          | CMV-4000 | 16/12/2021 | Í gangi | 130100-001-    | Viðskiptakröfur | Endurgreiðsla            | USD      | -100                           | -100    | -100                         |
| 20851          | ARP-8000 | 20/12/2021 | Í gangi | 130100-002-    | Viðskiptakröfur |                   | USD      | -0,88                          | -0,88   | -0,88                        |
| 20853          | ARPM0004 | 20/12/2021 | Í gangi | 130100-002-    | Viðskiptakröfur |                   | EUR      | -127,11                        | -174,12 | -174,12                      |
| 20856          | CMV-4010 | 21/12/2021 | Í gangi | 130100-002-    | Viðskiptakröfur | Kreditáfangareikningur | USD      | -175                           | -175    | -175                         |
| 20857          | FTV-3011 | 28/12/2021 | Í gangi | 130100-001-    | Viðskiptakröfur | Hjálparforrit         | USD      | 400                            | 400     | 400                          |
| 20910          | FTV-3020 | 29/12/2021 | Í gangi | 130100-002-    | Viðskiptakröfur | Þjónusta           | USD      | 300                            | 300     | 300                          |

Af þessum færslum eru þrjár jafnaðar í fjárhagsjöfnuninni.

Reikningur fyrir 175 Bandaríkjadali (175 USD) er til staðar. Þessi reikningur var greiddur með greiðslu í evrum (EUR) og staðgreiðsluafsláttur var tekinn.

| Færslubókarnúmer | Fylgiskjal  | Dagsetning       | Gerð      | Fjárhagslykill | Heiti lykils        | Lýsing | Gjaldmiðill | Upphæð í gjaldmiðli færslu | Upphæð  | Upphæð í skýrslugjaldmiðli |
|----------------|----------|------------|-----------|----------------|---------------------|-------------|----------|--------------------------------|---------|------------------------------|
| 20855          | FTV-3004 | 5/12/2021  | Í gangi | 130100-002-    | Viðskiptakröfur | Hjálparforrit   | USD      | 175                            | 175     | 175                          |
| 20851          | ARP-8000 | 20/12/2021 | Í gangi | 130100-002-    | Viðskiptakröfur |             | USD      | -0,88                          | -0,88   | -0,88                        |
| 20853          | ARPM0004 | 20/12/2021 | Í gangi | 130100-002-    | Viðskiptakröfur |             | EUR      | -127,11                        | -174,12 | -174,12                      |

Niðurstöður fyrir aðallykil 130100 fara eftir því hvort eiginleikinn sé virkur áður en árslokalokun er keyrð. Ef eiginleikinn er virkjaður fer niðurstaðan einnig eftir stillingu á valkostinum „Halda upplýsingum í árslokalokun“.

### <a name="the-feature-isnt-enabled"></a>Eiginleikinn er ekki virkur
Árslokalokun stofnar þrjár færslur opnunarstöðu fyrir aðallykil 130100 árið 2022. Samtala færslna í bókhaldsgjaldmiðlinum er USD 525.

| Færslubókarnúmer | Fylgiskjal  | Dagsetning     | Gerð    | Fjárhagslykill | Heiti lykils        | Lýsing | Gjaldmiðill | Upphæð í gjaldmiðli færslu | Upphæð  | Upphæð í skýrslugjaldmiðli |
|----------------|----------|----------|---------|----------------|---------------------|-------------|----------|--------------------------------|---------|------------------------------|
| 20910          | YEC_2021 | 1/1/2022 | Opnar | 130100-002-    | Viðskiptakröfur |             | USD      | 299,12                         | 299,12  | 299,12                       |
| 20910          | YEC_2021 | 1/1/2022 | Opnar | 130100-001-    | Viðskiptakröfur |             | USD      | 400                            | 400     | 400                          |
| 20910          | YEC_2021 | 1/1/2022 | Opnar | 130100-002-    | Viðskiptakröfur |             | EUR      | -127,11                        | -174,12 | -174,12                      |

Enda þótt færsla greiðslunnar fyrir EUR - 127,11 var fjárhagsjöfnuð fer færslan samt áfram sem upphafsstaða.

### <a name="feature-is-enabled-and-keep-detail-during-year-end-close--no"></a>Eiginleiki er virkur og „Halda upplýsingum í árslokalokun“ = Nei

Árslokalokun stofnar tvær færslur opnunarstöðu fyrir aðallykil 130100 árið 2022. Samtala færslna í bókhaldsgjaldmiðlinum er USD 525, en fjárhagsjafnaðar færslur eru útilokaðar frá opnunarstöðunni. Heildarupphæð fyrir lykil 130100-002- er USD 125 í stað USD 299,12 og færslan fyrir EUR 127,11/USD 174,12 er algjörlega undanskilin.

| Færslubókarnúmer | Fylgiskjal  | Dagsetning     | Gerð    | Fjárhagslykill | Heiti lykils        | Lýsing | Gjaldmiðill | Upphæð í gjaldmiðli færslu | Upphæð | Upphæð í skýrslugjaldmiðli |
|----------------|----------|----------|---------|----------------|---------------------|-------------|----------|--------------------------------|--------|------------------------------|
| 20910          | YEC_2021 | 1/1/2022 | Opnar | 130100-002-    | Viðskiptakröfur |             | USD      | 125                            | 125    | 125                          |
| 20910          | YEC_2021 | 1/1/2022 | Opnar | 130100-001-    | Viðskiptakröfur |             | USD      | 400                            | 400    | 400                          |

### <a name="feature-is-enabled-and-keep-detail-during-year-end-close--yes"></a>Eiginleiki er virkur og „Halda upplýsingum í árslokalokun“ = Já

Árslokalokun stofnar fimm færslur opnunarstöðu fyrir aðallykil 130100 árið 2022. Aðskilin færsla opnunarstöðu er stofnuð fyrir hverja af fimm færslum sem ekki voru jafnaðar. Samtala færslna í bókhaldsgjaldmiðlinum er enn USD 525.

| Færslubókarnúmer | Fylgiskjal  | Dagsetning     | Gerð    | Fjárhagslykill | Heiti lykils        | Lýsing       | Gjaldmiðill | Upphæð í gjaldmiðli færslu | Upphæð | Upphæð í skýrslugjaldmiðli |
|----------------|----------|----------|---------|----------------|---------------------|-------------------|----------|--------------------------------|--------|------------------------------|
| 20910          | YEC_2021 | 1/1/2022 | Opnar | 130100-001-    | Viðskiptakröfur | Þjónustugjald       | USD      | 10.000                            | 10.000    | 10.000                          |
| 20910          | YEC_2021 | 1/1/2022 | Opnar | 130100-001-    | Viðskiptakröfur | Endurgreiðsla            | USD      | -100                           | -100   | -100                         |
| 20910          | YEC_2021 | 1/1/2022 | Opnar | 130100-002-    | Viðskiptakröfur | Kreditáfangareikningur | USD      | -175                           | -175   | -175                         |
| 20910          | YEC_2021 | 1/1/2022 | Opnar | 130100-001-    | Viðskiptakröfur | Hjálparforrit         | USD      | 400                            | 400    | 400                          |
| 20910          | YEC_2021 | 1/1/2022 | Opnar | 130100-002-    | Viðskiptakröfur | Þjónusta           | USD      | 300                            | 300    | 300                          |

Þegar færsluupplýsingar eru geymdar verða upprunalegar ítarlegar færslur ekki fyrir áhrifum. Þær haldast bókaðar og ójafnaðar á reikningsárinu sem verið er að loka. Afrit af þessum færslum er búið til fyrir opnunarstöðuna. Eftirfarandi gildi úr upprunalegum færslum eru afrituð í færslur opnunarstöðunnar.

- Fjárhagslykill (aðallykillinn og allar fjárhagsvíddir)
- Upphæðir í færslu-, bókhalds- og skýrslugjaldmiðlum.
- Lýsing
- Bókunarlag
- Bókunargerð

   > [!NOTE]
   > Engum öðrum færslum opnunarstöðu er úthlutað bókunargerð. Þar af leiðandi er hægt að nota bókunargerðin til að gera greinarmun á milli opnunarfærslna sem voru færðar áfram í ítarlegt.

Sumum reitum úr upprunalegum færslum þarf að breyta í ítarlegum færslum opnunarstöðunnar. Dagsetning á færslum opnunarstöðu er alltaf fyrstu dagur næsta reikningsárs. Breyta þarf færslubókarnúmerinu og fylgiskjalsnúmerið breytist í gildið sem var fært inn í svarglugga árslokalokunar.

Upplýsingar úr upprunalegum færslum má finna á síðunni **Fjárhagsjöfnun**. Hver ítarleg færsla opnunarstöðu sýnir dálkinn **Upprunaleg færsludagsetning** í hnitanetinu. Þessi dálkur getur hjálpað þér að stemma af færslur á nýja reikningsárinu. Hægt er að velja **Skoða upprunalegt fylgiskjal** til að kafa aftur ofan í allt upprunalega fylgiskjalið.

## <a name="settle-transactions"></a><a name="settle-transactions"></a>Jafna færslur
Til að jafn fjárhagsfærslur skaltu fylgja þessum skrefum.

1. Opnið **Fjárhagur**  >  **Reglubundin verkefni**  >  **Fjárhagsuppgjör**.
2.  Setjið síurnar efst á síðuna.

    1. Velja dagsetningarsvið. Einnig er hægt að velja kóða dagsetningarbils til að fylla dagsetningabil sjálfkrafa inn.

       - Dagsetningabilið getur ekki farið á milli reikningsára. Ef dagsetningabilið fer á milli reikningsára verða engar færslur sýndar þegar þú velur **Birta færslur**.
       - Ef dagsetningabilið er á opnu reikningsári er hægt að jafna færslur og hægt er að bakfæra jöfnunina. Ef dagsetningabilið er á lokuðu reikningsári eða ef árslokalokuninni er lokið eru færslur sýndar, en ekki er hægt að jafna þær eða bakfæra jöfnun. Einungis er hægt að afmerkja færslur í lokuðu reikningsári. Ef dagsetningabilið er á lokuðu reikningsári eru hnapparnir **Merkja valið**, **Jafna merktar færslur** og **Bakfæra merktar færslur** ekki í boði.

    2. Velja aðallykilinn sem sýna á færslur fyrir. Þessi reitur er áskilinn. Uppflettingin sýnir aðeins aðallyklana sem eru valdir á síðunni **Fjárhagsjöfnun** fyrir bókhaldslykil fyrirtækisins.
    3. Veljið bókunarlagið. Þú getur ekki gert upp færslur sem eru í mismunandi bókunarlögum.
    4. Til að birta aðallykil og víddir í aðskildum dálkum skal velja fjárhagsvíddarsamstæðu.

3.  Veldu **Birta færslur** til að sýna allar færslur sem passa við síurnar sem þú stillir. Ef þú breytir einhverjum síum eða víddarsamstæðum þarftu að velja **Birta færslur** aftur.
4.  Veljið línur sem á að jafna. Gildið á svæðinu **Valin upphæð** efst á síðunni eykst eða lækkar með heildarupphæðinni á línum sem þú valdir.
5.  Þegar þú hefur lokið við að velja færslur skaltu velja **Merkja sem valið**. Gátmerki birtist í **Merkt** dálknum fyrir hverja færslu sem þú valdir. Auk þess hækkar gildið á svæðinu **Valin upphæð** fyrir ofan hnitanetið eða lækkar með heildarupphæðinni á línunum sem þú merktir.
6.  Þegar gildið á svæðinu **Valin upphæð** er **0** (núll) skaltu velja **Jafna valdar færslur**.

    - Hlutajöfnun er ekki leyfð. Til dæmis er ekki hægt að jafna $100 debetfærslu á móti $90 kreditfærslu. Einnig þarf að merkja eftirstandandi $10 kreditfærslu til að hafa með í jöfnuninni.
    - Færið inn jöfnunardagsetningu. Dagsetning verður að vera á eða á eftir síðustu dagsetningu færslnanna sem eru merktar fyrir jöfnun.

Staða valinna færslna er uppfært í **Jafnað**.

> [!IMPORTANT]
> Allar færslur sem þú hefur merkt fyrir jöfnun fyrir virkan lögaðila og valinn aðallykill verður jafnað. Færslurnar þurfa ekki að birtast á síðunni. Þær verða jafnaðar þótt þær séu faldar vegna síunnar.

Sum ferli, t.d. bakfærsla, jafna fjárhagsfærslur sjálfkrafa. Til dæmis er greiðsla og reikningur jafnaðar í viðskiptakröfum og jöfnunin býr til innleystan hagnað/tap. Jöfnun greiðslunnar og reikningsins jafnar ekki fjárhagsfærslur eins og færslur fyrir fjárhagslykil viðskiptakrafna. Ef greiðslan og reikningurinn eru hins vegar ójöfnuð í viðskiptakröfum mun bakfærð bókhaldsfærsla sem var bókuð við bakfærslu á jöfnun viðskiptakrafna leiða til þess að upprunalegar og bakfærðar bókhaldsfærslur verði fjárhagsjafnaðar í fjárhagsbókinni. Þegar eiginleikinn **Munurinn á fjárhagsjöfnun og árslokalokun** er virkur mun fjárhagsjöfnun bakfærslu ekki sjálfkrafa gerast ef bakfærsludagsetningin er á öðru reikningsári.

## <a name="use-excel-for-ledger-settlement"></a>Notið Excel fyrir fjárhagsjöfnun

Hægt er að flytja færslur sem eru sýndar á síðunni **Fjárhagsjöfnun** út í Excel. Í Excel er hægt að sía færslur enn frekar til að ákvarða hvaða færslur á að merkja fyrir jöfnun.
Báðar fjárhagsjöfnunareiningar flytja út fjárhagsfærslur aðeins fyrir aðallykilinn sem er valinn á síðunni **Fjárhagsjöfnun**. Þótt enn sé hægt að merkja eða afmerkja færslur fyrir lokuð reikningsár með Excel, er ekki hægt að jafna þær. Auk þess er ekki hægt að jafna færslur fyrir það reikningsár.

## <a name="make-transactions-easier-to-find"></a>Gera það auðveldara að finna færslur

Síðan **Fjárhagsuppgjör** inniheldur aðgerðir sem auðveldar að sjá færslurnar sem þarf að jafna.

Notið síuna **Valið** til að sía færslur miðað við hvort gátreiturinn **Valið** reitinn fyrir þær sé valinn.
•   Notaðu síuna **Staða** til að sía færslur út frá stöðu þeirra.
•   Veldu **Raða eftir raunupphæð** til að raða upphæðunum eftir raungildi. Á þennan hátt er hægt að flokka debet- og kreditfærslur sem eru með sömu upphæðina.

## <a name="reverse-a-settlement"></a>Bakfæra jöfnun

Þú getur bakfært jöfnun sem var gerð fyrir mistök.

1.  Fylgdu skrefum 1 til 3 í hlutanum [Jafna færslur](#settle-transactions) til að sýna færslurnar sem þú ert að leita að.
2.  Í **Staða** síu, veldu **Jöfnuð**.
3.  Veljið línur sem á að afturkalla.
4.  Veljið **Bakfæra merktar færslur**. Staða allra færslna sem eru með sama jöfnunarkennið er uppfærð í **Ekki jafnað**.

> [!IMPORTANT]
> Allar færslur sem eru með sama jöfnunarkennið verða bakfærðar jafnvel þótt þær séu ekki merktar. Til dæmis voru fjórar línur merktar og jafnaðar. Allar fjórar línurnar eru með sama jöfnunarauðkenni. Ef þú merkir eina af þessum fjórum línum og velur síðan **Bakfæra merktar færslur** verða allar fjórar línurnar bakfærðar.






