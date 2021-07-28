---
title: Eitt fylgiskjal
description: Eitt fylgiskjal fyrir fjárhagsbækur (almenna færslubók, eignabók, greiðslubók lánardrottins, o.s.frv.) gerir þér kleift að slá inn margar undirbókarfærslur í tengslum við eitt fylgiskjal.
author: kweekley
ms.date: 11/05/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerParameters, AssetProposalDepreciation
audience: Application User
ms.reviewer: roschlom
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-03-16
ms.dyn365.ops.version: 8.0.2
ms.openlocfilehash: 105fdc1b8e8c9e30c0d305894910194591707193
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/06/2021
ms.locfileid: "6356704"
---
# <a name="one-voucher"></a>Eitt fylgiskjal

[!include [banner](../includes/banner.md)]


## <a name="what-is-one-voucher"></a>Hvað er „Eitt fylgiskjal“?

Núverandi virkni fyrir fjárhagsbækur (almenna færslubók, eignabók, greiðslubók lánardrottins, o.s.frv.) gerir þér kleift að slá inn margar undirbókarfærslur í tengslum við eitt fylgiskjal (viðskiptavinur, lánardrottinn, eignir, verk og banki) í tengslum við eitt fylgiskjal. Microsoft vísar til þessa virkni sem *Eitt fylgiskjal*. Þú getur búið til eitt fylgiskjal með því að nota eina af eftirfarandi aðferðum:

- Setjið upp færslubókarheitið (**Fjárhagur** \> **Uppsetning færslubókar** \> **Færslubókarheiti**) þannig að reiturinn **Nýtt fylgiskjal** sé stilltur á **Aðeins eitt fylgiskjalsnúmer**. Sérhverri línu sem bætt er við færslubókina er nú að finna í sama fylgiskjalinu. Því er hægt að færa inn fylgiskjalið sem marglínu fylgiskjal, sem lykil/mótlykil í sömu línunni eða sem samsetningu.

    [![Stök lína.](./media/same-line.png)](./media/same-line.png)

    > [!IMPORTANT]
    > Skilgreiningu á Einu fylgiskjali nær **ekki** yfir tilvik þar sem færslubókarheiti eru sett upp eins og **Eitt fylgiskjalsnúmer eingöngu**, en notandinn færir þá inn fylgiskjal sem inniheldur aðeins fjárhagslyklagerðir. Í þessu efnisatriði þýðir Eitt fylgiskjal að það sé Eitt fylgiskjal sem inniheldur fleiri en einn seljanda, viðskiptavin, banka, eign eða verk.

- Sláið inn marglínu fylgiskjal þar sem enginn mótlykill er.

    [![Marglínu fylgiskjal.](./media/Multi-line.png)](./media/Multi-line.png)

- Sláið inn fylgiskjal þar sem bæði lykillinn og mótlykillinn innihalda lyklagerð undirbókar, svo sem **lánardrottinn**/**lánardrottinn**, **viðskiptavinur**/**viðskiptavinur**, **lánardrottinn**/**viðskiptavinur** eða **banki**/**banki**.

    [![Fylgiskjal undirbókar.](./media/subledger.png)](./media/subledger.png)

## <a name="issues-with-one-voucher"></a>Vandamál varðandi eitt fylgiskjal

Eiginleiki eins fylgiskjals veldur vandamálum í uppgjöri, skattaútreikningum, bakfærslum, afstemmingu undirbókar við fjárhagsbók, fjárhagsskýrslugerð og fleira. (Til að fá frekari upplýsingar um vandamál sem geta komið upp við uppgjör skal t.d. sjá [Stakt fylgiskjal með mörgum færslum viðskiptavina eða lánardrottna](../accounts-payable/single-voucher-multiple-customer-vendor-records.md).) Til að vinna og skrá rétt þurfa þessi ferli og skýrslur færsluupplýsingar. Þó að sumar aðstæður gætu samt sem áður virkað rétt, en það fer eftir uppsetningu fyrirtækisins, koma oft upp vandamál þegar margar færslur eru færðar inn í eitt fylgiskjal.

Til dæmis þegar eftirfarandi marglínu fylgiskjal er bókað.

[![Dæmi um fylgiskjal með mörgum línum.](./media/example.png)](./media/example.png)

Þá er búin til skýrslan **Útgjöld lánardrottins** á vinnusvæðinu **Fjármálainnsýn**. Í þessari skýrslu eru reikningsstöður kostnaðarlykla flokkaðir af lánardrottnaflokk og síðan lánardrottni. Við gerð skýrslunnar getur kerfið ekki ákvarðað hvaða lánardrottnaflokkar/lánardrottnar stofnuðu til kostnaðarins 250,00. Færsluupplýsingar vantar og þess vegna gerir kerfið ráð fyrir að fyrsti lánardrottin sem finnst í fylgiskjalinu hafi stofnað til 250,00. Þess vegna er 250,00 kostnaður, sem er hluti af stöðu aðallykils 600120, sýndur undir þeim lánardrottnaflokki/lánardrottni. Hins vegar er mjög líklegt að fyrsti lánardrottininn í fylgiskjalinu sé ekki rétti lánardrottininn. Þess vegna er skýrslan líklega rangt.

[![Kostnaðarskýrsla eftir lánardrottni.](./media/expenses.png)](./media/expenses.png)

## <a name="the-future-of-one-voucher"></a>Framtíð eins fylgiskjals

Vegna vandamála sem geta komið upp þegar eitt fylgiskjal er notað, verður þessi virkni úreld að lokum. En hins vegar eru virknigloppur sem reiða sig á þessa virkni og úreldingin gerist því ekki öll í einu. Þess í stað verður eftirfarandi áætlun notuð:

- **Vorútgáfa 2018** - Sjálfgefið var slökkt á virkninni í gegnum færibreytuna **Leyfa margar færslur í einu fylgiskjali** færibreytunni í flipanum **Almennt** á síðunni **Færibreytur fjárhags**. Hins vegar geturðu kveikt aftur á því ef fyrirtækið hefur atburðarás sem heyrir undir viðskiptagloppur sem eru skráðar seinna í þessu efnisatriði.

    - Ef viðskiptaaðstæðurnar krefjast ekki eins fylgiskjals er mælt með því að slökkt sé á virkninni. Ef hún er notuð jafnvel þótt önnur lausn sé til staðar, mun Microsoft ekki laga „villur“ á svæðum sem ekki er minnst á í þessu efnisatriði.
    - Mælt er með því að hætta að nota eitt fylgiskjal fyrir samþættingar nema virknin sé nauðsynleg fyrir eina eða fleiri skráðar virknigloppur.

- **Síðari útgáfur** – Nokkrar viðskiptakröfur er aðeins hægt að uppfylla með því að nota eitt fylgiskjal. Microsoft verður að tryggja að enn verði hægt að uppfylla allar skilgreindar viðskiptakröfur í kerfinu eftir að virknin er gerð úreld. Þess vegna þarf líklega að bæta við nýjum eiginleikum til að fylla í virknigloppur. Microsoft getur ekki boðið upp á eina sérstaka lausn vegna þess að hver eiginleikagloppa er mismunandi og verður að meta hana út frá viðskiptakröfunum. Einhverjum virknigloppum verður líklega skipt út fyrir eiginleika sem hjálpa til við að mæta tilteknum viðskiptakröfum. Hins vegar gæti verið fyllt í aðrar gloppur með því að leyfa áfram færslu í færslubók, eins og eitt fylgiskjal er notað, en að rakning kerfisins á upplýsingum verði bætt eftir þörfum.

Þegar fyllt hefur verið í allar virknigloppur mun Microsoft láta vita að eiginleikinn verði gerður úreldur. Hins vegar tekur úreldingin ekki gildi fyrr en a.m.k. einu ári eftir samskiptin. Þrátt fyrir að Microsoft geti ekki lagt fram mat þegar virkni eins fylgiskjals verður gerð úreld, þá mun það líklega taka að minnsta kosti tvö ár áður en úreldingin mun eiga sér stað. Stefna Microsoft er að láta líða a.m.k. 12 mánuði frá tilkynningu um úreldingu á virkni og þar til sjálf úreldingin á sér stað þannig að viðskiptavinir og óháðir hugbúnaðarsalar hafi tíma til að bregðast við breytingunni. Til dæmis gæti fyrirtæki þurft að uppfæra viðskiptaferli sína, einingar og samþættingar.

Úrelding eins fylgiskjals er umtalsverð breyting sem verður tilkynnt víðsvegar. Sem hluti af þeim samskiptum mun Microsoft uppfæra þetta efnisatriði, birta bloggfærslu á bloggsvæði Microsoft Dynamics 365 Finance, uppfæra efnisatriðið „Fjarlægðir eða úreltir eiginleikar“, láta vita af breytingunni á viðeigandi ráðstefnum Microsoft o.s.frv.

## <a name="why-use-one-voucher"></a>Af hverju að nota Eitt fylgiskjal?

Byggt á samtölum við viðskiptavini hefur Microsoft tekið saman eftirfarandi lista yfir aðstæður þar sem viðskiptavinir nota virknina Eitt fylgiskjal eða ástæður þess að þeir nota hana. Nokkrar af þessum viðskiptakröfum er aðeins hægt að uppfylla með því að nota Eitt fylgiskjal. Hins vegar, í mörgum tilfellum, geta aðrir valkostir uppfyllt sömu viðskiptakröfum.

### <a name="scenarios-that-require-one-voucher"></a>Tilfelli sem krefjast Eins fylgiskjals

Eftirtaldar tilfelli er aðeins hægt að ná með því að nota virknina Eitt fylgiskjal. Ef fyrirtækið hefur eitthvað af þessum atburðarrásum, þú verður að virkja margar færslur sem færa skal í fylgiskjalið með því að breyta stillingu á **Leyfa margar færslur í einu fylgiskjali** færibreytunni á **Fjárhagsfæribreytur** síðunni. Þessar virknigloppur verða fylltar með öðrum eiginleikum í síðari útgáfum.

> [!Note]
> [Fyrir sérhverja eftirfarandi sviðsmynda verður reiturinn **Leyfa margar færslur á einu fylgiskjali** að vera stilltur á Já í flýtiflipanum **Almennt** á síðunni **Fjárhagsfæribreytur**.]

### <a name="post-vendor-or-customer-payments-in-summary-form-to-a-bank-account"></a>Bóka lánardrottin eða greiðslur viðskiptavinar á samantektarskjámynd bankareiknings

**Dæmi** Fyrirtæki miðlar lista yfir lánardrottna og upphæðum á bankann sinn og bankinn notar listann til að greiða lánardrottnum fyrir hönd fyrirtækisins. Bankinn bókar samtölu greiðslnanna sem staka úttekt af bankareikningnum.

Samantekt á greiðslum lánardrottins er aðeins studd af Einu fylgiskjali. Hver seljandi er færður inn sem aðskilin lína til að viðhalda upplýsingum í undirbók viðskiptaskuldar. Hins vegar er samantekna upphæðin fyrir allar greiðslur jöfnuð við eina línu fyrir bankareikninginn. Þess vegna er úttektin sýnd sem stök samantekin upphæð í undirbók bankans.

**Dæmi** Fyrirtæki greiðir innborgun viðskiptavina eða bankinn greiðir innborgun viðskiptavina fyrir hönd fyrirtækisins og innborgunin er sýnd sem eingreiðsla á bankareikningnum.

Samantekt á greiðslum viðskiptavina er yfirleitt studd með innborgunarvirkni. Hins vegar, ef þú notar „brúun" á greiðslumáta, er þessi atburðarás aðeins studd með Einu fylgiskjali. Greiðslur viðskiptavina eru færðar inn á sama hátt og lýst er fyrir samantekt á greiðslu lánardrottins.

### <a name="mechanism-to-group-transactions-from-a-business-event"></a>Kerfi til að flokka færslur frá viðskiptatilviki

**Atburðarrás** Fyrirtæki hefur stakt viðskiptatilfelli sem kveikir á mörgum færslum. Hins vegar vill bókhaldsdeildin skoða bókhaldsfærslurnar saman fyrir betri endurskoðun.

Ef fyrirtæki þarf að skoða bókhaldsfærslur viðskiptatilviks saman verður að nota Eitt fylgiskjal. 

### <a name="country-specific-features"></a>Landsbundnar aðgerðir

**Atburðarrás** Eitt stjórnsýsluskjal (SAD) fyrir Pólland krefst þess eins og er að notað sé eitt fylgiskjal. Þangað til flokkunarvalkostur er tiltækur fyrir þessa aðgerð, verður að halda áfram að nota virknina Eitt fylgiskjal. Það kunna að vera til fleiri landsbundnar aðgerðir sem krefjast virknina Eitt fylgiskjal.

### <a name="customer-prepayment-payment-journal-that-has-taxes-on-multiple-lines"></a>Greiðslubók fyrirframgreiðslu fyrir viðskiptavini sem hefur skatta á mörgum „línum"

Í þessari tilfelli eru viðskiptavinirnar í eina fylgiskjalinu sömu viðskiptavinirnir vegna þess að færslan líkir eftir línum fyrir pöntun viðskiptavinar. Fyrirframgreiðslan verður að vera færð inn í eitt fylgiskjal vegna þess að skattaútreikningur verður að vera gerður á „línum“ stöku greiðslunnar sem viðskiptavinurinn gerði.

### <a name="customer-reimbursement"></a>Endurgreiðsla til viðskiptavina

**Dæmi** Viðskiptavinur greiðir fyrirframgreiðslu fyrir pöntun, og línurnar í pöntuninni hafa mismunandi skatta sem verða að vera skráðir fyrir fyrirframgreiðsluna. Fyrirframgreiðsla á greiðsla viðskiptavinar er ein færsla sem hermir eftir línum pöntunar, þannig að hægt sé að skrá viðeigandi skatt fyrir upphæðina á hverri línu.

Ef reglubundna verk endurgreiðslu er keyrt úr einingu viðskiptakrafna stofnar það færslu til að færa stöðu frá viðskiptavini til lánardrottins. Í þessari atburðarás verður að nota Eitt fylgiskjal til að endurgreiða viðskiptavininum.

### <a name="fixed-asset-maintenance-catch-up-depreciation-split-asset-calculate-depreciation-on-disposal"></a>Viðhald eigna: Vinna upp afskriftir, skipta eign, reikna út afskrift á losun
Eftirfarandi eignafærslur búa einnig til margar færslur innan eins fylgiskjals:

- Viðbótarkaup eru gerð á eign og „vinna upp" afskrift er reiknuð út.
- Eign er skipt.
- Breytur til að reikna afskriftir við förgun er kveikt á og þá er eignin fargað.
- Þjónustudagsetning eignar er fyrir kaupdagsetningu. Þar af leiðandi er leiðrétting afskriftar bókuð.

> [!Note]
> Þegar þú ert að fara í færslur skaltu vera viss um að allar færslur eigi við um sömu fastafjármuni. Fylgiskjalið verður ekki bókað ef það inniheldur fleiri en eina fasta eign, jafnvel þó að reiturinn **Nýtt fylgiskjal** sé stilltur á Aðeins eitt fylgiskjal á síðunni **Færslubókaheiti** í fjárhag. Ef þú setur fleiri en eina fasta eign í fylgiskjali verða skilaboðin **Aðeins má vera ein eignarfærsla á hverju fylgiskjali** birt og þú munt ekki geta sent fylgiskjalið.  

### <a name="bills-of-exchange-and-promissory-notes"></a>Víxlar og eigin víxlar
Víxlar og eigin víxlar krefjast þess að Eitt fylgiskjal sé notaður vegna þess að færslurnar flytja stöðu viðskiptavinar eða lánardrottins frá einum viðskiptakröfum/viðskiptaskulda til annarra, miðað við stöðu greiðslunnar.

## <a name="scenarios-that-dont-require-one-voucher"></a>Tilfelli sem þurfa ekki Eitt fylgiskjal

Eftirfarandi atburðarásum er hægt að ná með öðrum hætti og ætti ekki að nota virknina fyrir Eitt fylgiskjal.

### <a name="post-customer-payments-in-summary-form-to-the-bank-account"></a>Bóka greiðslur viðskiptavinar á samantektarskjámynd bankareiknings

Fyrirtæki greiðir innborgun viðskiptavina eða bankinn greiðir innborgun viðskiptavina fyrir hönd fyrirtækisins og innborgunin er sýnd sem eingreiðsla á bankareikningnum.

Samantekt á greiðslum viðskiptavina er studd með virkni innborgunar þegar „brúun“ er ekki notuð á greiðslumátann.

### <a name="netting"></a>Greiðslujöfnun

Í greiðslujöfnun eru stöður lánardrottins og viðskiptavinar greiðslujafnaðar gagnvart hvor annarri vegna þess að lánardrottin og viðskiptavinur eru sami aðilinn. Þessi nálgun lágmarkar peningafærslur milli fyrirtækis og viðskiptavinar/lánardrottins.

Hægt er að greiðslujafna með því að færa inn aukningu og minnkun í aðskildum fylgiskjölum og bóka svo jöfnunina á jöfnunarfjárhagslykil.

### <a name="post-in-summary-to-the-general-ledger"></a>Bóka í samantekt á fjárhagsbók

Fyrirtæki vilja oft bóka í samantekt fjárhagsbókar til að lágmarka gagnamagn. Hins vegar krefjast slík fyrirtæki vanalega að færsluupplýsingunum sé samt sem áður viðhaldið. Þegar bókun er gerð á samantektarskjámynd í gegnum eitt fylgiskjal eru færsluupplýsingar ekki þekktar og því ekki hægt að viðhalda þeim.

- Þar sem viðskiptaupplýsingar er ekki hægt að viðhalda, mælum við með að fyrirtæki noti **ekki** Eitt fylgiskjal til að bóka í samantekt.
- Eftir að stuðningur við Eitt fylgiskjal hefur verið tekinn af er hægt að innleiða upprunaskjals- og bókhaldsrammann í færslubókina. Þessar rammar munu síðan halda við færsluupplýsingunum og styðja samantekt inn í fjárhagsbókina.


### <a name="settle-multiple-unposted-payments-to-the-same-invoice"></a>Gera upp margar óbókaðar greiðslur á sama reikninginn

Þessi atburðarás er venjulega að finna í fyrirtækjum þar sem viðskiptavinir geta notað margar greiðsluaðferðir til að greiða fyrir innkaup. Í þessari tilfelli verður fyrirtækið að geta skráð margar óbókaðar greiðslur og jafna þær á móti reikningi viðskiptavinar.

Nýr eiginleiki sem var bætt í Microsoft Dynamics 365 for Operations útgáfa 1611 (nóvember 2016) gerir kleift að gera upp margar óbókaðar greiðslur á móti einum reikningi. Margar greiðslur viðskiptavina þurfa ekki lengur að vera færðar inn í eitt fylgiskjal.

### <a name="import-bank-statement-transactions"></a>Flytja inn bankayfirlitsfærslur

Bankar greiða oft og fá greiðslur fyrir hönd fyrirtækis og þessar færslur eru skráðar í Finance með skrá sem berst frá bankanum. Fyrirtæki vilja oft að flokka saman þessar færslur með því að nota bankayfirlitsnúmerið í skránni. Vegna þess að hver færsla er sýnd í smáatriðum á bankayfirlitinu, er ekki krafist samantektar í bankaundirbók.

Hægt er að flokka færslur með því að nota aðra reiti í færslubókinni, svo sem sjálft rununúmer færslubókarinnar eða skjalsnúmerið.


### <a name="transfer-balances"></a>Flytja stöður

Fyrirtækið gæti þurft að flytja stöðu frá einum lánardrottni til annars lánardrottins, annaðhvort út af mistökum eða vegna þess að annar lánardrottin hefur tekið yfir ábyrgðina. Millifærslur af þessu tagi eiga sér stað einnig fyrir reikningsgerðir eins og **Viðskiptavin** og **Banka**.

Stöðufærslur frá einum lykli (lánardrottni, viðskiptavini, bankai, o.s.frv.) til annars lykils er hægt að gera í gegnum aðskilin fylgiskjöl og hægt er að bóka jöfnunina á jöfnunarfjárhagslykil.

### <a name="enter-beginning-balances"></a>Færa inn upphafsstöðu

Fyrirtæki færa oft inn upphafsstöður fyrir lykla undirbóka (lánardrottin, viðskiptavin, eignir o.s.frv.) sem eina fylgiskjalsfærslu. Upphafsstöður fyrir hvern undirbókarlykil er hægt að færa inn sem aðskildin fylgiskjöl og hægt er að bóka jöfnunina á jöfnunarfjárhagslykil.

### <a name="correct-the-accounting-entry-of-a-posted-customer-or-vendor-document"></a>Leiðrétta bókhaldsfærslu á bókuðu skjali viðskiptavinar eða lánardrottins

Fyrirtæki gæti þurft að leiðrétta fjárhagslykil viðskiptakrafna eða viðskiptaskulda vegna bókhaldsfærslu á bókuðum reikningi, en reikninginn er ekki hægt að bakfæra eða leiðrétta með öðrum hætti.

Ef þarf að gera leiðréttingu á fjárhagslykli viðskiptakrafna eða viðskiptaskulda verður að gera hana beint á fjárhagslyklinum. Ekki er hægt að gera aðlögunina með því að bóka í gegnum lánardrottin eða viðskiptavin. Þessi nálgun krefst þess leiðréttingin sé gerð á „óvirkum tíma“ svo að fjárhagslykillinn geti tímabundið leyft handvirka færslu.

### <a name="the-system-allows-it"></a>„Kerfið leyfir það“

Fyrirtæki nota oft virknina Eitt fylgiskjal eingöngu vegna þess að kerfið leyfir notkun þess án þess að gerð sé grein fyrir afleiðingunum.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]