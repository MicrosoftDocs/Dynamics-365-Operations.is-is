---
title: Eitt fylgiskjal
description: Eitt fylgiskjal fyrir fjárhagsbækur (almenna færslubók, eignabók, greiðslubók lánardrottins, o.s.frv.) gerir þér kleift að slá inn margar undirbókarfærslur í tengslum við eitt fylgiskjal.
author: kweekley
manager: AnnBe
ms.date: 11/05/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-03-16
ms.dyn365.ops.version: 8.0.2
ms.openlocfilehash: ada04948c4775091091cc30664dd7d9405b4f9da
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "308553"
---
# <a name="one-voucher"></a>Eitt fylgiskjal

[!include [banner](../includes/banner.md)]


## <a name="what-is-one-voucher"></a>Hvað er „Eitt fylgiskjal“?

Núverandi virkni fyrir fjárhagsbækur (almenna færslubók, eignabók, greiðslubók lánardrottins, o.s.frv.) gerir þér kleift að slá inn margar undirbókarfærslur í tengslum við eitt fylgiskjal (viðskiptavinur, lánardrottinn, eignir, verk og banki) í tengslum við eitt fylgiskjal. Microsoft vísar til þessa virkni sem *Eitt fylgiskjal*. Þú getur búið til eitt fylgiskjal með því að nota eina af eftirfarandi aðferðum:

- Setjið upp færslubókarheitið (**Fjárhagur** \> **Uppsetning færslubókar** \>**Færslubókarheiti**) þannig að reiturinn **Nýtt fylgiskjal** sé stilltur á **Aðeins eitt fylgiskjalsnúmer**. Sérhverri línu sem bætt er við færslubókina er nú að finna í sama fylgiskjalinu. Því er hægt að færa inn fylgiskjalið sem marglínu fylgiskjal, sem lykil/mótlykil í sömu línunni eða sem samsetningu.

    [![Stök lína](./media/same-line.png)](./media/same-line.png)

    > [!IMPORTANT]
    > Skilgreiningu á Einu fylgiskjali nær **ekki** yfir tilvik þar sem færslubókarheiti eru sett upp eins og **Eitt fylgiskjalsnúmer eingöngu**, en notandinn færir þá inn fylgiskjal sem inniheldur aðeins fjárhagslyklagerðir. Í þessu efnisatriði þýðir Eitt fylgiskjal að það sé Eitt fylgiskjal sem inniheldur fleiri en einn seljanda, viðskiptavin, banka, eign eða verk.

- Sláið inn marglínu fylgiskjal þar sem enginn mótlykill er.

    [![Marglínu fylgiskjal](./media/Multi-line.png)](./media/Multi-line.png)

- Sláið inn fylgiskjal þar sem bæði lykillinn og mótlykillinn innihalda lyklagerð undirbókar, svo sem **lánardrottinn**/**lánardrottinn**, **viðskiptavinur**/**viðskiptavinur**, **lánardrottinn**/**viðskiptavinur** eða **banki**/**banki**.

    [![Fylgiskjal undirbókar](./media/subledger.png)](./media/subledger.png)

## <a name="issues-with-one-voucher"></a>Vandamál varðandi eitt fylgiskjal

Eiginleiki eins fylgiskjals veldur vandamálum í uppgjöri, skattaútreikningum, bakfærslum, afstemmingu undirbókar við fjárhagsbók, fjárhagsskýrslugerð og fleira. (Til að fá frekari upplýsingar um vandamál sem geta komið upp við uppgjör skal t.d. sjá [Stakt fylgiskjal með mörgum færslum viðskiptavina eða lánardrottna](https://docs.microsoft.com/en-us/dynamics365/unified-operations/financials/accounts-payable/single-voucher-multiple-customer-vendor-records).) Til að vinna og skrá rétt þurfa þessi ferli og skýrslur færsluupplýsingar. Þó að sumar aðstæður gætu samt sem áður virkað rétt, en það fer eftir uppsetningu fyrirtækisins, koma oft upp vandamál þegar margar færslur eru færðar inn í eitt fylgiskjal.

Til dæmis þegar eftirfarandi marglínu fylgiskjal er bókað.

[![Dæmi](./media/example.png)](./media/example.png)

Þá er búin til skýrslan **Útgjöld lánardrottins** á vinnusvæðinu **Fjármálainnsýn**. Í þessari skýrslu eru reikningsstöður kostnaðarlykla flokkaðir af lánardrottnaflokk og síðan lánardrottni. Við gerð skýrslunnar getur kerfið ekki ákvarðað hvaða lánardrottnaflokkar/lánardrottnar stofnuðu til kostnaðarins 250,00. Færsluupplýsingar vantar og þess vegna gerir kerfið ráð fyrir að fyrsti lánardrottin sem finnst í fylgiskjalinu hafi stofnað til 250,00. Þess vegna er 250,00 kostnaður, sem er hluti af stöðu aðallykils 600120, sýndur undir þeim lánardrottnaflokki/lánardrottni. Hins vegar er mjög líklegt að fyrsti lánardrottininn í fylgiskjalinu sé ekki rétti lánardrottininn. Þess vegna er skýrslan líklega rangt.

[![Kostnaður](./media/expenses.png)](./media/expenses.png)

## <a name="the-future-of-one-voucher"></a>Framtíð eins fylgiskjals

Vegna vandamálanna sem fyrr voru nefndar, mun Eitt fylgiskjal virkni verða úrelt. Hins vegar, vegna þess að það eru virknigloppur sem treysta á þessa virkni, mun virknin ekki vera úreld öll í einu. Þess í stað verður eftirfarandi áætlun notuð:

- **Vorútgáfa 2018** - Sjálfgefið verður slökkt á virkninni sjálfgefið á **Leyfa margar færslur í einu fylgiskjali** færibreytunni á **Almennt** flipanum á **Færibreytur fjárhagsbókar** síðu. Hins vegar geturðu kveikt á virkni ef fyrirtækið hefur atburðarás sem heyrir undir viðskiptagloppur sem eru skráðar seinna í þessu efnisatriði.

    - Ef viðskiptavinir hafa viðskiptaatburðarrás sem ekki krefst Eins fylgiskjals, ættu þeir ekki að kveikja á virkni. Microsoft mun ekki laga „villur“ á þeim svæðum sem eru auðkenndar síðar í þessu efnisatriði ef þessi virkni er notuð jafnvel þó að önnur lausn sé til staðar.
    - Hættið að nota Eitt fylgiskjal fyrir samþættingu í Microsoft Dynamics 365 for Finance and Operations, nema virknin sé nauðsynleg fyrir eina af virknigloppunum.

- **Seinni útgáfur**- Allar virknigloppur verða fylltar. **Eftir að virknigloppur eru fylltir og nýjar aðgerðir eru afhentar, verður að líða að minnsta kosti eitt ár áður en virkni Eins fylgiskjals er varanlega slökkt**, vegna þess að viðskiptavinir og óháðir hugbúnaðarsalar (ISV) verða að hafa nægan tíma til að bregðast við nýju virkninni. Til dæmis gætu þeir þurft að uppfæra viðskiptaferli sín, einingar og samþættingar.

> [!IMPORTANT]
> **Eitt fylgiskjal eingöngu** valkosturinn hefur **ekki** verið fjarlægður úr uppsetningu færslubókarheitis. Þessi valkostur er ennþá studdur þegar fylgiskjalið inniheldur aðeins fjárhagslyklagerðir. Viðskiptavinir verða að vera varkárir þegar þeir nota þessa stillingu, því fylgiskjalið verður ekki bókað ef þeir nota **Eitt fylgiskjal eingöngu** kostinn en slá síðan inn fleiri en eitt viðskiptavina, lánardrottinn, banka, eign eða verk. Þar að auki geta viðskiptavinir ennþá slegið inn lyklagerðir undirbókar, svo sem greiðslu í einu fylgiskjali sem inniheldur lyklagerðir **Lánardrottins**/**Banka**.

## <a name="why-use-one-voucher"></a>Af hverju að nota Eitt fylgiskjal?

Byggt á samtölum við viðskiptavini hefur Microsoft tekið saman eftirfarandi lista yfir aðstæður þar sem viðskiptavinir nota virknina Eitt fylgiskjal eða ástæður þess að þeir nota hana. Nokkrar af þessum viðskiptakröfum er aðeins hægt að uppfylla með því að nota Eitt fylgiskjal. Hins vegar, í mörgum tilfellum, geta aðrir valkostir uppfyllt sömu viðskiptakröfum.

### <a name="scenarios-that-require-one-voucher"></a>Tilfelli sem krefjast Eins fylgiskjals

Eftirtaldar tilfelli er aðeins hægt að ná með því að nota virknina Eitt fylgiskjal. Ef fyrirtækið hefur eitthvað af þessum atburðarrásum, þú verður að virkja margar færslur sem færa skal í fylgiskjalið með því að breyta stillingu á **Leyfa margar færslur í einu fylgiskjali** færibreytunni á **Fjárhagsfæribreytur** síðunni. Þessar virknigloppur verða fylltar með öðrum eiginleikum í síðari útgáfum.

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

### <a name="bills-of-exchange-and-promissory-notes"></a> Víxlar og eigin víxlar
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

Þessi atburðarás er venjulega að finna í smásölufyrirtækjum þar sem viðskiptavinir geta notað margar greiðsluaðferðir til að greiða fyrir innkaup. Í þessari tilfelli verður fyrirtækið að geta skráð margar óbókaðar greiðslur og jafna þær á móti reikningi viðskiptavinar.

Nýr eiginleiki sem var bætt í Microsoft Dynamics 365 for Operations útgáfa 1611 (nóvember 2016) gerir kleift að gera upp margar óbókaðar greiðslur á móti einum reikningi. Margar greiðslur viðskiptavina þurfa ekki lengur að vera færðar inn í eitt fylgiskjal.

### <a name="import-bank-statement-transactions"></a>Flytja inn bankayfirlitsfærslur

Bankar greiða oft og fá greiðslur fyrir hönd fyrirtækis og þessar færslur eru skráðar í Finance and Operations með skrá sem berst frá bankanum. Fyrirtæki vilja oft að flokka saman þessar færslur með því að nota bankayfirlitsnúmerið í skránni. Vegna þess að hver færsla er sýnd í smáatriðum á bankayfirlitinu, er ekki krafist samantektar í bankaundirbók.

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