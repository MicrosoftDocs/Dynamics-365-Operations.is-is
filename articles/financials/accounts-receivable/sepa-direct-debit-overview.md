---
title: Yfirlit yfir SEPA beint debet
description: "Í Einni Evru Greiðslur Svæði (SEPA) er sett upp með Evrópska Þóknun og ákvarðar hverng sem teljast rafrænar greiðslur innanlands, land/svæði þar sem einstaka viðskiptum eða fyrirtækisins og bankans er staðsettur. Það er enginn mismunur innanlandsgreiðslur og landamæri greiðslur. SEPA inniheldur 28 aðildarríki Evrópusambandsins (ESB) sem og Íslands, Liechtenstein, Noregs, Sviss, Mónakó og San Marínó. SEPA sem hjálpar til við ákvarða einn fyrir greiðslufærslur innan á Evrópska Efnahagslegt Svæði (EEA) skjámynd. Að lokum, í SEPA er búist við að draga úr fjölda greiðslusniða sem bankar, fyrirtæki og einstaklingar þurfa að vinna með."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankAccountTable, CustBankAccounts, CustParameters, CustTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 11144
ms.assetid: 3277c9b6-e46e-40c9-aa76-9b0449467842
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: fb55f4b0b06019891c2e490eda837cfad882e6db
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="sepa-direct-debit-overview"></a>Yfirlit yfir SEPA beint debet

[!include [banner](../includes/banner.md)]

Í Einni Evru Greiðslur Svæði (SEPA) er sett upp með Evrópska Þóknun og ákvarðar hverng sem teljast rafrænar greiðslur innanlands, land/svæði þar sem einstaka viðskiptum eða fyrirtækisins og bankans er staðsettur. Það er enginn mismunur innanlandsgreiðslur og landamæri greiðslur. SEPA inniheldur 28 aðildarríki Evrópusambandsins (ESB) sem og Íslands, Liechtenstein, Noregs, Sviss, Mónakó og San Marínó. SEPA sem hjálpar til við ákvarða einn fyrir greiðslufærslur innan á Evrópska Efnahagslegt Svæði (EEA) skjámynd. Að lokum, í SEPA er búist við að draga úr fjölda greiðslusniða sem bankar, fyrirtæki og einstaklingar þurfa að vinna með.   

<a name="what-is-the-goal-of-sepa-direct-debits"></a>Hvert er markmiðið SEPA beint debet?
---------------------------------------

SEPA-beingreiðsla leyfir lánardrottins til að safna fjármagn frá bankareikningi viðskiptavinar, svo lengi sem undirrituð umboðið hefur verið veitt af viðskiptavini til lánardrottins. Viðskiptavinurinn skrifar umboð heimilar lánardrottins til að safna greiðslu og instructs banka viðskiptavinar til greiðslu í innheimtu. 

SEPA Beina Debet stofnar í fyrsta sinn greiðslutæki sem nota má fyrir bæði innanlandsgreiðslur og evrugreiðslur þvert á landamæri alls staðar á 32 SEPA lönd/svæði. 

Tvær skemu eru tiltækir: á SEPA Kjarnauppsetning Beint Debetkerfi og í SEPA Fyrirtæki til Fyrirtækis (B2B) Beint Debetkerfi. Bæði skemu nota sama skráarsnið.

## <a name="what-is-the-core-direct-debit-scheme"></a>Hvað er Kjarni Beint debetkerfi?
Í SEPA Kjarnauppsetning Beint Debetkerfi er grunnur vildarkerfis. Það hefur eftirfarandi eiginleika:
-   Flutningur fjármagn er í evrum (þó bankareikninga gæti bið fjármagn í öðrum gjaldmiðlum).
-   Viðskiptavinar og lánardrottins verður hver bið lykil með kreditkortafyrirtæki er staðsettur innan á SEPA.
-   Viðskiptavinur verður að veita undirrituð umboðs til lánardrottins á.
-   Umboð renna út 36 mánuðum eftir að söfnun var síðast hafin.
-   Í lánardrottins verður að geyma umboð fyrir fyrir svo lengi sem umboðið er gild og fyrir minnst 14 mánuði eftir síðasta innheimtubréf.
-   Kerfið sem má nota fyrir einn (einskiptis) eða endurtekna beint debet innheimtu.
-   Viðskiptavinir hafa "engin spurningar lagðar" rétt á endurgreiðslu alltt að átta vikum eftir debet þeirra lykils.

## <a name="what-is-the-sepa-business-to-business-b2b-direct-debit-scheme"></a>Hvað er SEPA Business til Fyrirtækis (B2B) Beint debetkerfi?
Í SEPA B2B Beint Debetkerfi við færslur fyrirtæki til fyrirtækis og byggir á SEPA Kjarnauppsetning Beint Debetkerfi. Aðal mismun eru:
-   Í SEPA B2B Beint Debetkerfi er ekki heimil þegar viðskiptavinur er einka einstaka (consumer).
-   Viðskiptavinurinn er ekki rétt til að fá endurgreiðslu heimiluð færslunnar.
-   Banka viðskiptavinar verður að tryggja að söfnun er heimilaður, með því að staðfesta innheimtubréf gagnvart umboð upplýsingar. Banka viðskiptavinar og viðskiptavinir eru nauðsynlegar til að samþykkir í staðfestingu sem þarf að framkvæma fyrir hverja beint debet.
-   Kerfi sem býður upp á styttra tímaásinn þröskuldsframboðs beint debet og minnkar skila tímabil.

## <a name="can-i-use-the-cor1-scheme-for-direct-debit-mandates"></a>Get ég nota COR1-kerfi í umboð fyrir beint debet?
Já. Hægt er að nota COR1-kerfi fyrir umboð SEPA-beingreiðslukerfis í Austurríki, Belgíu, Þýskalandi, Frakklandi, Ítalíu, Spáni og í Hollandi. Kerfið sem veitir styttra tímabili fortilkynningu fyrir beint debet safnið fyrir á lánardrottins.

## <a name="what-are-international-bank-account-numbers-iban-and-bank-identifier-codes-bic"></a>Hvað eru Alþjóðlega Númer Bankareiknings (IBAN) og Banka Kóða Bic (BANK)?
Alþjóðlega Númer Bankareiknings (IBAN) og Bic-Kóði (BANK) eru notaðar til að auðkenna hvaða lykill í 32 SEPA löndum/svæðum. Færið inn í BIC í SWIFT-kóði svæðið og IBAN í svæðið IBAN. Báðir reitirnir eru staðsettir á flýtiflipanum Aukakenni á flipanum Bankareikningur á síðunni Bankareikningar. Þetta gildir bæði fyrir bankareikning lánardrottins sem og bankareikningur viðskiptavinar.

## <a name="where-do-i-enter-creditor-identifiers-direct-debit-ids"></a>Hvar færi ég inn auðkenni lánardrottins (kenni fyrir beingreiðslur)?
Í SEPA er hver lánveitandi auðkenndur með einkvæmu kenni lánveitanda. Þetta auðkenni er viðskiptavinar og banka viðskiptavinar sía hverja beingreiðsla og vinnur eða hafna beingreiðsla samkvæmt leiðbeiningar viðskiptavinar. Lánardrottnar verða að biðja um þessa kenni gegnum þeirra banka. Færðu þetta kennimerki inn í reitinn kenni beingreiðslu fyrir bankareikninginn fyrir lögaðilann.

## <a name="what-are-mandates"></a>Hvað eru umboð?
Viðskiptavinurinn skrifar umboð heimilar lánardrottins til að safna greiðslu og instructs banka viðskiptavinar til greiðslu í innheimtu. Viðskiptavinurinn út umboðið í skjámynd pappír eða rafrænt. Að sjálfgefnu umboðið rennur út 36 mánuðir eftir síðustu ræst beint debet.

## <a name="where-do-i-specify-the-sepa-direct-debit-file-format-iso-20022"></a>Hvar tilgreini ég SEPA-beingreiðsluskráarsnið (ISO 20022)?
SEPA gögn sniðin byggja á stöðlum ISO-20022 skilaboð. Þú munt velja gátreitinn Almenna rafræna skýrslugerð og sniðmátið SEPA-beingreiðslusnið sem útflutningssnið þegar greiðsluhættir í viðskiptakröfum eru skilgreindir. Hægt er að nota þann greiðsluhátt þegar greiðsluskrá er mynduð í greiðslubók viðskiptavinar.

## <a name="in-what-file-formats-can-i-generate-sepa-direct-debit-payment-files"></a>Í hvaða skráarsniðmátum get ég búið til SEPA-beingreiðslurskrár?
Hægt er að mynda rafrænar greiðsluskrár fyrir SPEA beingreiðslu á eftirfarandi sniði:
-   SEPA-beingreiðsluskrár á skráarsniðinu PAIN.008.001.02 XML fyrir Belgíu, Þýskaland, Spán, Frakkland, Ítalíu og Holland.
-   SEPA-beingreiðsluskrár eru á skráarsniðinu PAIN.008.001.02 XML fyrir Austurríki, og á skráarsniðinu PAIN.008.003.02 XML fyrir Þýskaland.

## <a name="how-do-refunds-and-returns-work-with-sepa-direct-debits"></a>Hvernig virka endurgreiðslur og skil með beina debetfærslu SEPA?
Undir báðum skemum SEPA-beingreiðslna, hafa viðskiptavinir ákveðin réttindi á endurgreiðslum. Viðskiptavini er heimilt að afturkalla heimild færslur með átta vikna tímabili eftir gjalddaga, án þess að þurfa að gefa ástæðu. Í tilviki óheimilaðra færslna er tímabilið framlengt til 13 mánuðum eftir gjalddaga. Bakfærslur sem hafa verið gerðar er í náð handvirkt með því að nota hnappinn Hætta við greiðslu á síðunni Færslur viðskiptavinar.






