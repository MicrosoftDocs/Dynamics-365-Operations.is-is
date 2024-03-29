---
title: Yfirlit yfir SEPA-kreditfærslur
description: Þessi grein inniheldur almennar upplýsingar um ISO 20022 kreditflutninga, sem innihalda sameiginlegt evrópskt greiðslusvæði (SEPA) kreditfærslur og allar aðrar rafrænar greiðslur til lánardrottna.
author: mrolecki
ms.date: 06/20/2017
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendInvoice, LedgerJournalTransVendPaym, VendPaymMode
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "11124"
- intro-internal
ms.assetid: 36b0f870-16d4-4bbb-8da5-e747e69b970d
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 671594b1ac6f10fae7c95ed9210e16f168e8dea1
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/25/2022
ms.locfileid: "9716075"
---
# <a name="sepa-credit-transfer-overview"></a>Yfirlit yfir SEPA-kreditfærslur

[!include [banner](../includes/banner.md)]

Þessi grein inniheldur almennar upplýsingar um ISO 20022 kreditflutninga, sem innihalda sameiginlegt evrópskt greiðslusvæði (SEPA) kreditfærslur og allar aðrar rafrænar greiðslur til lánardrottna. SEPA-kreditfærsla er tiltekin gerð greiðslu (í evrum) frá einu fyrirtæki eða einstaklingi til annars fyrirtækis eða einstaklings. Greinin lýsir því einnig hvernig á að setja upp og senda greiðsluskrá kreditfærslna.

## <a name="what-is-a-credit-transfer-message"></a>Hvað eru kreditfærsluskilaboð?
Kreditfærsluskilaboð er beiðni sendir aðila sem hóf greiðsluna (þínu fyrirtæki) um að flytja fjármagn af eigin reikningi til lánardrottins. Það eru margar lands/svæðis-bundnar og bankaháðar útfærslur kreditflutningsskilaboða. Sumar þeirra eru notaðar innan eins lands/svæðis, og sumar eru að verða að stöðlum. Einn þekktur altækur staðall er ISO 20022 og upphafsskilaboð hans, eins og kreditfærslur. Eftirfarandi skýringarmynd sýnir tengsl og umfang valinna kreditfærsluskilaboða. 
![Kreditmillifærsla.](./media/credit-transfer.jpg) Skilaboð kreditmillifærslu 

## <a name="what-are-iso-20022-and-sepa-payments"></a>Hvað eru ISO 20022 og SPEA-greiðslur?
Sameiginlegt evrópskt greiðslusvæði (SEPA) er sett upp af Evrópsku framkvæmdastjórninni og segir fyrir um að allar rafrænar greiðslur séu taldar vera innanlands, án tillits til lands/svæðis þar sem einstaklingur, fyrirtæki eða banki er staðsettur. Það er enginn munur milli innanlandsgreiðslna og greiðslna milli landa. SEPA inniheldur 28 aðildarríki Evrópusambandsins (ESB) auk Íslands, Liechtenstein, Noregs, Sviss, Mónakó og San Marínó. SEPA sem hjálpar til við ákvarða einn fyrir greiðslufærslur innan á Evrópska Efnahagslegt Svæði (EEA) skjámynd. Að lokum, í SEPA er búist við að draga úr fjölda greiðslusniða sem bankar, fyrirtæki og einstaklingar þurfa að vinna með. Evrópska framkvæmdastjórnin kom á fót lagagrunni fyrir SEPA-greiðslur með í Tilskipun um greiðsluþjónustu (PSD). Evrópska greiðslumiðlunarráðið (EPC) styður SEPA með eftirfarandi aðgerðum:

-   Það setur staðla fyrir rafrænar SEPA-greiðslur með ISO 20022 Alþjóðlegur fjárhagslegar atvinnugrein vildarkerfis XML skilaboðasniðið.
-   Það kemur á reglum og leiðbeiningum um umsjón greiðslna í evrum.

EPC, sem samanstendur af evrópskum bönkum, þróar heildarsöluverðmæti og tæknilega ramma fyrir SEPA-greiðslutæki. Þrjár gerðir af SEPA-greiðslum eru notuðar:

-   Kreditmillifærslur
-   Beint debet
-   Kort

## <a name="what-is-a-sepa-credit-transfer"></a>Hvað er SEPA-kreditfærsla?
SEPA-kreditfærsla er greiðsla frá einu fyrirtæki eða einstaklingi í öðru fyrirtæki eða einstaklingi. Greiðslur verða að vera í evrum og verða að innihalda alþjóðleg bankareikningsnúmer (IBAN) og bankaeinkenniskóða (BIC) fyrir báða aðila. (BIC er einnig þekkt sem auðkenniskóði banka \[SWIFT\] númer). Að auki verður færslukostnaður að deilast á báða aðila. Kreditfærslur sem eiga sér stað á milli aðila eiga að nota xml-skrár sem samræmast ISO-stöðlum 20022 um greiðsluvinnslu og xml-snið, eins og tilgreint er af EPC.

## <a name="how-is-a-credit-transfer-implemented"></a>Hvernig er kreditfærsla framkvæmd?
Greiðslusnið SEPA-kreditfærslu fyrir evrópulönd er innleitt með því að nota virknina Rafræn skýrslugerð og Greiðsluhættir í Microsoft Dynamics 365 Finance. Nokkur kreditfærslusnið sem eru notuð eru á öðrum svæðum nota enn eldri greiðsluramma. Meðal margra annara sniða, eru tólf ISO 20022 kreditflutnings skrársnið tiltæk. Þessi útflutningssnið samræmast staðlinum SEPA ISO 20022 XML. Þau eru notuð til að mynda greiðsluflutninga sem eru ekki í evrum fyrir lönd/svæði þar sem þau eru notuð og evrugreiðslur eins og tilgreint er í útgáfu 8.2 í SEPA Credit Transfer Scheme Rulebook sem EPC gefur út. Áður en ekki er hægt að innleiða kreditfærslur verður að hafa samband við bankann til að fá hugbúnaðinn sem er krafist til að senda inn rafrænar bankaskrár. Þú munt nota þennan hugbúnað til að flytja xml-skrár sem innihalda greiðslupantanir til bankans.

## <a name="what-credit-transfer-formats-are-currently-supported"></a>Hvað millifærslusnið eru studd eins og stendur?
Alltaf skal fara eignasafnið Samnýtt eign í Microsoft Dynamics Lifecycle Services (LCS) og skoða nýjustu lista yfir tiltækar skrár af eignargerðinni **GER-skilgreining**. Næsti hluti „Hvað þarf að setja upp?“ veitir tengla í grein þar sem útskýrt er hvernig búa á til LCS-geymslu til að fara yfir tiltækar stillingar og flytja inn valdar stillingar.

## <a name="what-do-i-have-to-set-up"></a>Hvað þarf að setja upp?
-   Áður en hægt er að kreditfærsluskrár verður að minnsta kosti ein virk skilgreining kreditfærslu að vera flutt inn í skilgreiningar þínar í rafrænni skýrslugerð. Hægt er að skoða leiðbeiningar í [Niðurhal skilgreininga fyrir rafræna skýrslugerð af Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md)
-   Þegar þú stillir greiðsluaðferðir viðskiptaskulda velurðu gátreitinn **Almenna rafræn skýrslugerð** og viðeigandi kreditfærslusnið (t.d. **ISO 20022 kreditfærsla (AT)**) sem stillingar útflutningssniðs.
-   Einnig þarf að setja upp lögaðila einingar og bankareikningsupplýsingar.
-   Krafist er númer bankareiknings, IBANs og stundum SWIFT-kóða (BICs) eða annarra kenna til að stofna gildar kreditfærslugreiðslur. Þess vegna verður að setja þær upp fyrir bankareikning lánardrottins og bankareikningur fyrirtækisins sem óskar eftir flutningnum.
-   Viðbótarupplýsingar gætu verið nauðsynlegar, svo sem virðisaukaskattsnúmer fyrir aðila sem á að vísa í kreditfærsluskilaboðum. Setja verður þessar upplýsingar upp fyrir lánardrottna og fyrir lögaðilann þegar beðið er um það.
-   Sumir greiðsluhætti viðskiptaskulda, helst ISO-20022 byggðir greiðsluhættir, gætu krafist viðbótaruppsetningar fyrir **Greiðslusniðskóðasetts**, eins og **Þjónustugerð** = **SLEV**. Þessir kóðar eru notaðir sem viðbótarmerking fyrir greiðslufærslur við greiðsluvinnslu. Sjálfgefin gildi greiðslukóða, t.d. **Tilgangur flokks**, **Greiðandi**, **Staðbundið stjórntæki** og **Þjónustustig** er hægt að velja á tveimur stöðum. Fyrsti staðurinn er **Haus greiðslubókar viðskiptaskulda** og annar er **Greiðsluaðferðir viðskiptaskulda**. Við stofnun greiðslubókarlína, eri greiðslukóðagildi sem stillt er í greiðslubókarhaus flutt í færslubókarlínu, ef það er ekki stillt, eru gildin úr Greiðsluhættir notuð.

## <a name="what-parameters-are-available-for-generating-credit-transfer-payments"></a>Hvaða færibreytur eru tiltækar til að mynda greiðslur með kreditfærslum?
Listi yfir sérstakar færibreytur fer eftir kreditfærslusniði. Eftirfarandi tafla sýnir þær færibreytur sem hægt er að nota þegar mynduð er greiðsluskrá ISO 20022-kreditfærslu í þýskalandi í greiðslubók lánardrottins. Með því að nota valkostina sem eru tiltækir á flipanum **Keyra í bakgrunni** flipa, er hægt að keyra myndun greiðslu í runustillingu.

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
<li><strong>Strd</strong> – Veljið þennan valkost til að nota skipulegt snið þegar ein greiðslulína er jöfnuð við reikning. Þessi valkostur er ekki &#39; tiltækur fyrir tiltekin lands-/svæðissértæk útflutningssnið fyrir Frakkland, Þýskaland eða Holland.</li>
<li><strong>Ustrd</strong> – Veljið þennan valkost til að nota óskipulegt snið þegar greiðslan er jöfnuð við marga reikninga. Reikningsnúmer fyrir jafnaða reikninga eru tengd saman og notuð sem greiðsluupplýsingar. Samkvæmt ISO 20022 leiðbeiningum takmarkast óskilpulegar greiðsluupplýsingar við 140 stafi.</li>
</ul></td>
</tr>
<tr class="even">
<td>Fjöldi reikninga</td>
<td>Færið inn þann fjölda reikninga sem <strong>Greiðslutilkynning</strong> skýrslan er prentuð úr.</td>
</tr>
<tr class="odd">
<td>Raðnúmer</td>
<td>Færa inn raðnúmer til að auðkenna skrána. Raðnúmerið er birt í skýrslunni <strong>Þátttökuathugasemd</strong>.</td>
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
Alþjóðlegt númer bankareiknings (IBAN) og bankaeinkenniskóði (BIC) eru notuð til að auðkenna alla lykla í mörgum löndum/svæðum. Þar á meðal er 34 SEPA lönd/svæði. Færið inn í BIC í **SWIFT-kóði** svæði og IBAN-númerið í **IBAN** reitinn. Bæði fyrir bankareikning lánardrottins sem og bankareikning viðskiptavinar eru þessir reitir staðsettir á flýtiflipanum **Aukakenni** á flipanum **Bankareikningur** á síðunni **Bankareikningar**. Notkun BIC fyrir SEPA-greiðslur er ekki lengur framfylgt.

## <a name="how-do-i-transmit-a-payment-file-to-the-bank"></a>Hvernig sendi ég greiðsluskrá í bankann?
Greiðsluskráin er mynduð þegar greiðslur eru myndaðar og það verður beðnir um að vista hana úr vafranum á einhverja tiltæka staðsetningu. Næsta skref er að senda xml-skrána til bankans. Þetta ferli er breytilegr frá einum banka til annars. Fylgja skal leiðbeiningunum frá bankanum til að senda inn skrár til banka fyrir vinnslu.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
