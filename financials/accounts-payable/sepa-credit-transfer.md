---
title: "Yfirlit yfir SEPA-kreditfærslur"
description: "Þessi skrá inniheldur almennar upplýsingar um 20022 kredit flutninga ISO, sem innihalda Eina Evru Greiðslur Svæði (SEPA) kredit flutningsskýrslum og öllum öðrum rafrænar greiðslur til lánardrottna. Sepa-millifærslur er greiðsla í evrum frá einu fyrirtæki eða einstaka fyrir annað fyrirtæki eða einstaka tiltekinni gerð. Efni einnig útskýrir hvernig á að setja upp og senda greiðsluskrá kredit flutning."
author: twheeloc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTransVendInvoice, LedgerJournalTransVendPaym, VendPaymMode
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 11124
ms.assetid: 36b0f870-16d4-4bbb-8da5-e747e69b970d
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 848df5e3898f37284d7746c59bff8b38d35ac883
ms.lasthandoff: 03/31/2017


---

# <a name="sepa-credit-transfer-overview"></a>Yfirlit yfir SEPA-kreditfærslur

Þessi skrá inniheldur almennar upplýsingar um 20022 kredit flutninga ISO, sem innihalda Eina Evru Greiðslur Svæði (SEPA) kredit flutningsskýrslum og öllum öðrum rafrænar greiðslur til lánardrottna. Sepa-millifærslur er greiðsla í evrum frá einu fyrirtæki eða einstaka fyrir annað fyrirtæki eða einstaka tiltekinni gerð. Efni einnig útskýrir hvernig á að setja upp og senda greiðsluskrá kredit flutning.

## <a name="what-is-a-credit-transfer-message"></a>Hvað er kredit skilaboð flutningi?
Flytja boðin kredit er beiðni sendir initiating aðila (fyrirtækisins) til að flytja fjármagn úr eigin lykils til lánardrottins. Það eru margar lands/svæðis-bundnar og tiltekin banka útfærslur kredit flutnings skilaboðum. Sumir þeirra eru notaðar innan einu landi/svæði, og sumar eru verði stöðlum. Einn vel altæka staðal er ISO 20022 og hennar upphafi skilaboð, eins og millifærslur. Eftirfarandi skýringarmynd sýnir tengsl og fyrir flutning skilaboð valins kredit. 
![Kreditfæra tansfer](./media/credit-transfer.jpg) Lánamark flytja skilaboð\[/myndatexti\] 

## <a name="what-are-iso-20022-and-sepa-payments"></a>Hvað eru ISO 20022 og sepa-greiðslna?
Sameiginlegt evrópskt greiðslusvæði (SEPA) er sett upp af Evrópsku framkvæmdastjórninni og segir fyrir um að allar rafrænar greiðslur séu taldar vera innanlands, án tillits til lands/svæðis þar sem einstaklingur, fyrirtæki eða banki er staðsettur. Það er enginn mismunur innanlandsgreiðslur greiðslna milli landa. Á SEPA inniheldur 28 aðildarríki á er Innan Evrópusambandsins (ESB), og einnig Ísland, Liechtenstein, Noregur, Sviss, Monaco og San Marino. SEPA sem hjálpar til við ákvarða einn fyrir greiðslufærslur innan á Evrópska Efnahagslegt Svæði (EEA) skjámynd. Að lokum, í SEPA er búist við að draga úr fjölda greiðslusniða sem bankar, fyrirtæki og einstaklingar þurfa að vinna með. Evrópska framkvæmdastjórnin kom á fót lagagrunni fyrir SEPA-greiðslur með í Tilskipun um greiðsluþjónustu (PSD). Evrópska greiðslumiðlunarráðið (EPC) styður SEPA með eftirfarandi aðgerðum:

-   Það setur staðla fyrir rafrænar SEPA-greiðslur með ISO 20022 Alþjóðlegur fjárhagslegar atvinnugrein vildarkerfis XML skilaboðasniðið.
-   Það kemur á reglum og leiðbeiningum um umsjón greiðslna í evrum.

EPC, sem samanstendur af evrópskum bönkum, þróar heildarsöluverðmæti og tæknilega ramma fyrir SEPA-greiðslutæki. Þrjár gerðir af SEPA-greiðslum eru notuðar:

-   Kreditmillifærslur
-   Beint debet
-   Kort

## <a name="what-is-a-sepa-credit-transfer"></a>Hvað er SEPA-kreditfærsla?
SEPA-kreditfærsla er greiðsla frá einu fyrirtæki eða einstaklingi í öðru fyrirtæki eða einstaklingi. Greiðslur verða að vera í evrum og verða að innihalda alþjóðleg bankareikningsnúmer (IBAN) og bankaeinkenniskóða (BIC) fyrir báða aðila. (BIC sem er einnig þekkt sem Society for Worldwide interbank-Financial Telecommunication \[SWIFT\] kóða.) Þar að auki er tímafærslukostnað verður að vera samnýtt milli bæði aðila. Kreditfærslur sem eiga sér stað á milli aðila eiga að nota xml-skrár sem samræmast ISO-stöðlum 20022 um greiðsluvinnslu og xml-snið, eins og tilgreint er af EPC.

## <a name="how-is-a-credit-transfer-implemented"></a>Hvernig er kredit flutningur virkur?
Greiðslusnið flutning kredit fyrir evrópulönd er innleidd með því að nota Rafræna skýrslugerð (ER) og Aðferðir greiðsluvirkni í Dynamics 365 Aðgerðir. Nokkrar lánamark flutning snið sem notuð eru í öðrum svæðum enn nota ramma eldri greiðslu. Meðal margar aðrar snið, eru twelve ISO 20022 kredit flytja skrársnið sem eru tiltækar. Þessar útflutningssnið staðlaða SEPA ISO 20022 XML samræmist. Þær eru notaðar til að mynda greiðsluflutningar ekki evru fyrir lönd/svæði þar sem þær eru notaðar og evru greiðslur eins og tilgreint er í útgáfu 8.2 á SEPA Kredit Flytja Vildarkerfis Rulebook sem EPC er losuð. Áður en ekki er hægt að innleiða flutninga kredit, verður að hafa samband við bankann til að fá hugbúnaðar sem er krafist til að senda inn skrár rafrænna bankaviðskipta. Farmflutningshugbúnaðurinn er notuð til að flytja xml-skrár sem innihalda greiðslubeiðnir til bankans.

## <a name="what-credit-transfer-formats-are-currently-supported-in-dynamics-365-for-operations"></a>Hvaða snið flutning kredit eru nú studd í Dynamics 365 aðgerða?
Alltaf skal fara eignasafni Samnýttum í Microsoft Dynamics Lifecycle services (LCS) og skoða nýjustu stöðugt lista yfir tiltækar skrár sem hafa af gerðinni eign **GER skilgreiningu**. Næsta hlutanum "Hvað I þarf að setja upp?", veitir tengil í efnisatriði sem útskýrir hvernig stofna á lcs-geymsla til að skoða tiltæk afbrigði og flytja inn afbrigði valið.

## <a name="what-do-i-have-to-set-up"></a>Hvað þarf að setja upp?
-   Áður en hægt er að stofna millifærslur skrár, a.m.k. eina virka kredit flutningi skilgreiningu verður flutt í skilgreiningum þitt ER. Leiðbeiningar fást [Sækja Rafræna skilgreiningar frá Lifecycle Services reporting](https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs).
-   Þegar greiðsluhætti í viðskiptaskuldir, veljið sem **Almennan rafræna skýrslugerð** gátreitinn og velja viðeigandi kredit flutning sniði (til dæmis **ISO 20022 millifærslur (AT)**) sem sníða skilgreiningu útflutning.
-   Einnig þarf að setja upp lögaðila einingar og bankareikningur upplýsingar í Dynamics 365 aðgerða.
-   Númer bankareiknings IBANs og stundum SWIFT kóðar (BICs) eða önnur Kenni er krafist til að stofna gild millifærslur greiðslur. Þess vegna verður að setja upp þau fyrir bankareikning lánardrottins og bankareikningur fyrirtækisins sem óskar eftir flutning.
-   Viðbótarupplýsingar gæti verið nauðsynleg, svo sem númer bókargerðir virðisaukaskattsins (VSK) fyrir aðila sem vísað er til að flytja boðin kredit. Þessar upplýsingar verður að setja upp fyrir lánardrottna og fyrir lögaðilann þegar hún er beðið um.
-   Sumar Lykla lánardrottna greiðsluhætti, eru ISO-20022 – byggð greiðsluhætti, gætu krafist viðbótaruppsetning fyrir **Greiðslu snið kóða stillir**, eins og **Þjónustu gerð** = **SLEV**. Þessir kóðar eru notaðir sem viðbótar merking fyrir greiðslufærslur við greiðsluvinnslu. Sjálfgildi kóðar, like **Tegund málefni**, **Gjalda brettis**, **Staðbundna tæki** og **Þjónustu stig** hægt er að setja í tveimur tugasætum. Er fyrsta stað **Lykla lánardrottna greiðslubókarhaus** og annað skilyrðið er **Lykla lánardrottna aðferðir fyrir greiðslur**. Við stofnun greiðslu færslubókar línur, kóðagildi Greiðslan sett í greiðslubókarhaus eru fluttar í færslubókarlínu, ef það er ekki stillt, gildi úr Greiðsluhættir eru notaðir.

## <a name="what-parameters-are-available-for-generating-credit-transfer-payments"></a>Hvaða færibreytur eru tiltækar til að mynda greiðslur flutningi kredit?
Listi yfir sérstakar færibreytur fer eftir sniði flutning kredit. Eftirfarandi tafla sýnir færibreytur sem eru tiltækar þegar ISO-20022 kredit flutning greiðsluskrá fyrir Þýskaland í greiðslubók lánardrottins. Með því að nota valkostina sem eru tiltækar í í **Keyra í bakgrunni** flipa, er hægt að keyra myndun greiðslu í runustillingu.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Svæði</th>
<th>lýsing</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Runubókun</td>
<td>Veljið þennan gátreit til að taka með bókunarmerki runu í xml-skrána.</td>
</tr>
<tr class="even">
<td>Vinnsludagsetning</td>
<td>Færið inn dagsetninguna þegar bankinn á að vinna greiðslur.</td>
</tr>
<tr class="odd">
<td>Snið</td>
<td>Veljið snið fyrir greiðsluupplýsingar eftir þörfum bankans eða landi/svæði:
<ul>
<li><strong>Strd</strong> – Veljið þennan valkost til að nota sniðið skipulagt þegar einni greiðslulínu jafnist reikningur. Þessi valkostur er ekki tiltæk fyrir tiltekin lönd/svæði útflutningssnið fyrir Frakkland, Þýskalandi eða Holland.</li>
<li><strong>Ustrd</strong> – Veljið þennan valkost til að nota óskipulegt snið þegar greiðslan er jöfnuð við marga reikninga. Reikningsnúmer fyrir jafnaða reikninga eru tengd saman og notuð sem greiðsluupplýsingar. Beinni ISO 20022 leiðbeiningar, óskipulagðar greiðsluupplýsingar takmarkast við 140 stafir.</li>
</ul></td>
</tr>
<tr class="even">
<td>Fjöldi reikninga</td>
<td>Færið inn fjölda reikninga sem á <strong>greiðslutilkynningu</strong> skýrslan er prentuð þaðan.</td>
</tr>
<tr class="odd">
<td>Raðnúmer</td>
<td>Færa inn raðnúmer til að auðkenna skrána. Raðnúmer birtist á á <strong>Þátttökuathugasemd</strong> skýrslu.</td>
</tr>
<tr class="even">
<td>Prenta þátttökuathugasemd</td>
<td>Veljið þennan gátreit til að prenta skýrsluna <strong>Þátttökuathugasemd</strong>.</td>
</tr>
<tr class="odd">
<td>Prenta eftirlitsskýrslu</td>
<td>Veljið þennan gátreit til að prenta skýrslu sem inniheldur greiðsluupplýsingar.</td>
</tr>
<tr class="even">
<td>Prenta upplýsingabréf</td>
<td>Veljið þennan gátreit til að prenta skýrsluna <strong>Greiðslutilkynningar</strong>.</td>
</tr>
</tbody>
</table>

## <a name="what-are-ibans-and-bics"></a>Hvað eru IBANs og BIC?
Alþjóðlega Númer Bankareiknings (IBAN) og Bic-Kóði (BANK) eru notaðar til að auðkenna hvaða lykill í mörgum löndum/svæðum worldwide. Þar á meðal er 34 SEPA lönd/svæði. Færa BIC í á **swift-kóði** svæði og IBAN í á **IBAN** svæði. Bæði fyrir bankareikning lánardrottins og bankareikningur viðskiptavinar, þessara svæða er staðsettur á er **aukakenni** FastTab á er **bankareikning** flipanum á **bankareikninga** síðu. Notkun BIC sepa-greiðslna er ekki lengur framfylgt.

## <a name="how-do-i-transmit-a-payment-file-to-the-bank"></a>Hvernig sendi ég greiðsluskrá í bankann?
Greiðsluskráin er mynduð þegar greiðslur, og það verið beðnir um að vista hana úr vafranum engar tiltækar staðsetningar. Næsta skref er að senda xml-skrána til bankans. Þetta ferli er breytilegr frá einum banka til annars. Fylgja skal leiðbeiningunum frá bankanum til að senda inn skrár til banka fyrir vinnslu.


