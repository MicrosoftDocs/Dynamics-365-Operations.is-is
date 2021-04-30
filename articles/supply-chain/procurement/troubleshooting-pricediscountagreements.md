---
title: Villuleita verð, afslætti, samninga og eftirágreiddan afslátt
description: Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með verð, afslætti, samninga og eftirágreidda afslætti.
author: SmithaNataraj
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 2ccc1d52b83f9319af1c6336c1876c795c70028a
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908520"
---
# <a name="troubleshoot-prices-discounts-agreements-and-rebates"></a>Villuleita verð, afslætti, samninga og eftirágreiddan afslátt

Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með verð, afslætti, samninga og eftirágreidda afslætti.

## <a name="i-cant-link-a-purchase-agreement-to-a-purchase-order-line-after-the-purchase-order-is-created"></a>Ekki er hægt að tengja innkaupasamning við innkaupapöntunarlínu eftir að innkaupapöntunin er stofnuð.

Innkaupasamningur verður að vera tengdur við innkaupapöntun þegar innkaupapöntunin er stofnuð. Annars er ekki hægt að tengja innkaupapöntunarlínur við innkaupasamningslínur.

## <a name="what-check-triggers-the-update-prices-and-discounts-entered-manually-or-external-document-message"></a>Hvaða athugun ræsir skilaboðin „Uppfæra verð og afslætti sem færð voru inn handvirkt eða með ytra skjali“?

Þegar sendingardagsetningu er breytt gætu borist skilaboð þar sem stendur „Uppfæra verð og afslætti sem færð voru inn handvirkt eða með ytra skjali.“ Þessi skilaboð berast vegna þess að ef sendingardagsetningunni hefur verið breytt gæti annar verð- eða sölusamningur verið ræstur og valdið breytingu á verði. Breyting á sendingardagsetningunni getur einnig haft áhrif á vöruhúsaáætlanir og aðrar tengdar upplýsingar.

Skilaboðin eru ræst þegar einhverjum dagsetninganna eða færibreytanna er breytt. Tilgangur skilaboðanna er að ganga úr skugga um að þú gerir þér grein fyrir verðbreytingum sem geta átt sér stað vegna þessara breytinga.

Skilaboðin eru kvaðning um mat á verðsamningi. Ítarlegri lýsingu má finna í [Reglur um mat á verðsamningi](/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper).

## <a name="a-purchase-order-receipt-doesnt-include-all-charges"></a>Kvittun innkaupapöntunar inniheldur ekki öll gjöld.

### <a name="reproduce-the-issue"></a>Framkallaðu vandamálið

Eftirfarandi ferli sýnir eina leið til að endurtaka málið.

1. Á síðunni **Færibreytur innkaupa og aðfanga**, í flipanum **Afhending**, skal ganga úr skugga um valkosturinn **Mynda gjöld á innhreyfingarskjali afurða** sé stilltur á *Já*.
1. Stofna innkaupapöntun sem inniheldur gjöld.
1. Staðfesta innkaupapöntun.
1. Takið á móti innkaupapöntuninni.
1. Skoðið samtölu kvittunarinnar og berið hana saman við samtöluna sem búist var við.
1. Takið eftir að ekki öll gjöld eru tekin með í kvittun innkaupapöntunar.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Úrlausnin fer eftir því hvernig þessi ýmsu gjöld hafa verið sett upp. Upplýsingar um hvernig á að setja upp ýmis gjöld til að uppfylla kröfur, er að finna í eftirfarandi bloggfærslu: [Bóka gjöld við móttöku afurðar](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).

## <a name="trade-agreement-prices-and-discounts-arent-applied-on-sales-or-purchase-order-lines-that-are-imported-through-data-management"></a>Verð og afslættir verðsamninga eru ekki notuð á sölu-eða innkaupapöntunarlínum sem eru fluttar inn í gegnum gagnastjórnun.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Verðsamningar sem eiga við um sölu- og innkaupapöntunarlínur eru ekki notaðir í línum sem eru fluttar inn í gegnum gagnastjórnun. Hins vegar eru notaðir sömu verðsamningar á sölu- eða innkaupapöntunarlínum sem eru búnar til handvirkt.

### <a name="reason-for-the-issue"></a>Ástæða fyrir vandamálinu

Ef innkaupapöntunarlínur sem eru fluttar inn gegnum gagnastjórnun innihalda þegar verðupplýsingar, verður verðsamningurinn ekki endurmetinn fyrir þessar línur. Til dæmis, ef **Prósenta línuafsláttar** eða eitthvert gildi fyrir verð eða afslátt er sett inn í línu, þá verða verðsamningar ekki skoðaðir fyrir þessa línu.

### <a name="issue-workaround"></a>Lausn á vandanum

Búist er við þessari hegðun og hún er svipuð bæði fyrir sölupantanir og innkaupapantanir.

Leið framhjá þessu er að flytja inn innkaupapöntunarlínurnar án þess að setja inn neinar verðupplýsingar. Verðsamningarnir verða þá notaðir og innkaupapöntunarlínurnar verða uppfærðar á grundvelli skilgreindra verðsamninga.

## <a name="a-vendor-rebate-isnt-cumulated-based-on-invoices"></a>Eftirágreiddur afsláttur lánardrottins er ekki uppsafnaður samkvæmt reikningum.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Ef reikningar sem eru bókaðir eru með mismunandi gjalddögum, koma þessir reikningar ekki fram í eftirágreiddum afslætti lánardrottins sem er myndaður úr þeim.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Samkvæmt hönnun er gjalddagi ekki tekinn til greina þegar eftirágreiddur afsláttur lánardrottins er reiknaður. Íhugið að sérsníða kerfið þannig að gjalddaginn og tengslin við reikninginn séu augljósari með tilliti til raunverulegs eftirágreidds afsláttar lánardrottins.

## <a name="unit-prices-on-purchase-orders-arent-calculated-based-on-the-unit-conversion"></a>Einingaverð á innkaupapöntunum eru ekki reiknuð út á grundvelli umreiknings einingar.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Þegar einingu er breytt í innkaupapöntun eru verð verðsamnings ekki endurreiknuð samkvæmt skilgreiningum einingaumreiknings.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Verð eru alltaf fengin úr verðsamningum (eða öðrum verðstillingum í kerfinu, svo sem sölusamningum eða vöruverði) og þeir eru stilltir fyrir einingu.

Ef einingunni er breytt í pöntunarlínu, leitar kerfið að verði fyrir nýju eininguna og notar það verð. Ef ekkert verð finnst fyrir eininguna setur kerfið ekki verð á. Ekki er hægt að nota umreikning einingar til að endurreikna verðið í aðra einingu. Fræðilega séð er verðið fyrir einn kassa af tíu ekki endilega jafnt og tífalt verðið á einum kassa.

### <a name="issue-workaround"></a>Lausn á vandanum

Ein leið framhjá þessu vandamáli er að ganga úr skugga um til séu verðsamningar fyrir einingarnar sem búist er við að verði notaðar í pöntunarlínum fyrir vöruna.

## <a name="currency-conversion-issues-occur-with-trade-agreements"></a>Vandamál varðandi umreikning gjaldmiðils eiga sér stað með verðsamningum.

Verð verðsamninga eru ekki endurreiknuð samkvæmt gjaldmiðlinum þegar gjaldmiðillinn er annar í innkaupapöntun.

Eiginleikinn *Almennur gjaldmiðill* gerir kleift að skilgreina verð og afslætti í aðeins einum gjaldmiðli. Síðan er hægt að umbreyta í aðra gjaldmiðla eftir því sem þörf er á. Þegar búið er að framkvæma umreikninginn getur eiginleikinn sjálfkrafa notað snjallverðsléttun.

## <a name="when-i-open-the-purchase-agreement-page-in-a-line-view-mode-i-cant-personalize-the-page-by-adding-the-price-unit-field-in-the-overview-of-the-line"></a>Þegar ég opna síðu innkaupasamnings í línuskoðunarstillingu, þá get ég ekki sérstillt síðuna með því að bæta við reit verðeiningar í yfirliti línunnar.

Ekki er hægt að taka með suma samnýtta reiti í sérstillingum samningsrammans. Þessi takmörkun kemur til vegna gagnalíkansins sem er innleitt. Þess vegna er ekki hægt að sérsníða reitinn **Verðeining**.

## <a name="the-maximum-limit-from-a-purchase-agreement-isnt-effective-on-a-purchase-requisition"></a>Hámarkið í innkaupasamningi gildir ekki í innkaupabeiðni.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Þegar innkaupabeiðni er tengd við innkaupasamning er hámarkið samkvæmt innkaupasamningi ekki virkt í innkaupabeiðninni. Sjálfgefnar upplýsingar um verð eru slegnar inn á réttan hátt en hægt er að panta meira en hámarkið samkvæmt innkaupasamningi í innkaupabeiðninni.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Búist er við þessari hegðun. Vegna þess að beiðnir eru ekki alltaf samþykktar ætti magn eða upphæð ekki að vera geymt í innkaupasamningi. Þess vegna er ekki hægt að uppfylla hámarkið í innkaupasamningnum.

## <a name="trade-agreements-can-be-created-from-rejected-rfqs-therefore-the-system-doesnt-prevent-trade-agreement-journals-from-being-created-if-the-rfq-line-hasnt-been-accepted"></a>Hægt er að stofna verðsamninga úr höfnuðum tilboðsbeiðnum. Þess vegna hindrar kerfið ekki að færslubækur verðsamninga séu stofnaðar ef lína tilboðsbeiðni hefur ekki verið samþykkt.

Hægt er að stofna verðsamninga fyrir öll svör fyrir beiðni um tilboð (tilboðsbeiðni), óháð því hvort þau voru samþykkt eða þeim hafnað. Frekari upplýsingar er að finna í [Yfirlit yfir beiðni um tilboð (tilboðsbeiðni)](request-quotations.md).



[!INCLUDE[footer-include](../../includes/footer-banner.md)]