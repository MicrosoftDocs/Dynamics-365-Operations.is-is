---
title: Uppgjörsyfirlit
description: Þetta efnisatriði veitir almennar upplýsingar um uppgjörsferlið. Hún lýsir þeim færslutegundum sem hægt er að jafna, hvenær og hvernig hægt er að jafna færslur og niðurstöðum jöfnunarferlisins.
author: kweekley
manager: AnnBe
ms.date: 05/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14551
ms.assetid: 0968fa71-5984-415b-8689-759a0136d5d1
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: e13bdcdcf6dac68a95e6c2759a66bc59013464cb
ms.sourcegitcommit: fd3db9f2052c76a5d906b9ec23cb16222452a362
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/10/2019
ms.locfileid: "1539968"
---
# <a name="settlement-overview"></a>Uppgjörsyfirlit

[!include [banner](../includes/banner.md)]

Þetta efnisatriði veitir almennar upplýsingar um uppgjörsferlið. Hún lýsir þeim færslutegundum sem hægt er að jafna, hvenær og hvernig hægt er að jafna færslur og niðurstöðum jöfnunarferlisins.

Við uppgjör, eru færslur á eitt skjal eru notuð í færslunum á annað skjal til að auka eða minnka stöðu hvers skjals. Til dæmis getur greiðsla verið beitt á reikning. Hægt að jafna ýmsar færslugerðir á mismunandi tímum og með ýmsum aðferðum. Jöfnun getur líka valdið nýjar færslur séu myndaðar.

## <a name="what-transactions-can-be-settled"></a>Hvaða færslur er hægt að jafna
Jöfnun innan viðskiptaskulda og viðskiptakrafna geta átt sér stað milli hvaða færslugerða sem hafa áhrif á stöðu lánardrottins eða stöðu viðskiptavina, svo sem reikninga, greiðslur, kreditreikningar og þóknanir. Hægt er að jafna allar færslugerðir gagnvart öllum öðrum færslugerð. Til dæmis er hægt að jafna greiðslu gegn reikning, kreditreikning við reikning, reikningur gagnvart reikningur og greiðsla gegn greiðslu. Hægt er að jafna greiðslur gagnvart færslu í sama lögaðila eða annan lögaðila. Í fyrirtækjum sem nota miðstýrðt greiðslulíkan,geta [miðstýrðar greiðslur](set-up-centralized-payments.md) hjálpað til við að straumlínulaga greiðsluferlið.

## <a name="when-to-settle-transactions"></a>Hvenær á að Jafna færslur
Hægt er að jafna færslur á tíma greiðslufærslu. Til dæmis þegar greiðsla er gerið til lánardrottins, yfirleitt velurðu reikninga til greiðslu. Með því að velja reikninga eru þeir merktir til jöfnunar gegn greiðslu. Þegar starfsmaður greiðslu fyrir viðskiptakröfur skráir viðskiptavinargreiðslu, geta þeir merkt viðeigandi reikninga fyrir jöfnun, byggt á upplýsingum sem er höfð með í greiðslu viðskiptavinar. **Jafna færslur** síða er notuð til að merkja færslur til jöfnunar. Hægt er að opna þessa síðu úr hvaða óbókaðan reikning eða greiðslu. Þegar færslan er bókuð er jöfnunin einnig bókuð Einnig er hægt að jafna færslur eftir að þær eru bókaðar. Hægt er að færa inn og bóka greiðslu viðskiptavinar án þess að það eru jafnaðar gagnvart neinum reikninga. Hins vegar gæti þurft að rannsaka fyrst, til að ganga úr skugga um að greiðslan er jöfnuð á móti rétta reikningnum. **Jafna færslur** síðan getur veri opnuð úr **Alla viðskiptavini** eða **Alla lánardrottna** síðu eða á **Færslur** síðu fyrir hvaða viðskiptavin eða lánardrottinn sem er. Er hægt að taka frá bókaðar fyrirframgreiðslur fyrir reikning með því að merkja greiðslu fyrir jöfnun gagnvart innkaupapöntun eða sölupöntun. Í þessu tilfelli hefur greiðsla enn opin staða, en hún getur ekki verið jafnaðar á móti öðrum reikningi. Greiðslan verður sjálfkrafa jöfnuð á móti reikningi sem er stofnaður úr innkaupapöntun eða sölupöntun.

## <a name="how-to-settle-transactions"></a>Hvernig á að Jafna færslur
Hægt er að jafna færslur handvirkt, sjálfvirkt, eða sambland af aðferðunum tveimur. Val á aðferð jöfnunar fer eftir viðskiptaferli, sem er síðan hægt að beita í gegnum uppsetningu jöfnunar í færibreytum viðskiptaskuldir og færibreytur viðskiptakrafna. Hægt er að stofna greiðslur lánardrottins og greiðslur viðskiptavina með beingreiðslu sem er notuð til að velja reikninga til greiðslu. Greiðslutillaga er ræst handvirkt og svo merkir Dynamics 365 for Finance and Operations valda reikninga fyrir jöfnun þegar greiðslur eru stofnaðar. Ef greiðslur eru stofnaðar handvirkt er hægt að nota í **Jafna færslur** síðu til að velja reikninga til jöfnunar. Hægt er að velja reikningana handvirkt eða nota **Merkja eftir forgangi** valkost til að hafa reikninga sjálfkrafa merkt til jöfnunar. Í **Merkja eftir forgangi** valkostur er einungis tiltæk fyrir viðskiptakröfur. Til að virkja þennan valkost, skal nota við **jöfnunarforgangur** síðu í færibreytum viðskiptakrafa. Ef starfsmaður greiðslna færir inn greiðslu, en jafnar ekki greiðsluna áður en hún er bókuð, er hægt að jafna greiðsluna sjálfkrafa. Hægt er að virkja sjálfvirka jöfnun í færibreytur viðskiptakrafna og færibreytum viðskiptaskulda. Sjálfvirk jöfnun jafnar færslur innan sama lögaðila og jafnar ekki yfir marga lögaðila. Þegar sjálfvirka jöfnun er notuð er hægt að nota forskilgreint jöfnunarröð eða hægt er að skilgreina eigin jöfnunarröð í færibreytum viðskiptakrafa. Þessi eiginleiki er einungis tiltæk fyrir viðskiptakröfur.

## <a name="results-of-settlement"></a>Afleiðingar jöfnunar
Þegar færslur eru jafnaðar er útistandandi staða hverrar færslu aukinn eða minnkaður eins og við á. Í dæmigerðum aðstæðum, þar sem reikningur og greiðsla eru jafnaðar, er stöðu og hverrar færslu er uppfærð samkvæmt eftirfarandi reglum:

-   Ef greiðsluupphæðin er hærri en reikningsupphæðin er staða reiknings er minnkað í 0,00 og reikningur er lokaður. Greiðslan helst opin, og staðan er upphæðin samsvarandi því að hve miklu leiti greiðslan er umfram reikningsupphæð
-   Ef greiðsluupphæðin er lægri en reikningsupphæðin er staða greiðslu er minnkað í 0,00 og greiðsla er lokaður. reikningur helst opin, og staðan er samsvarandi því að hve miklu leiti greiðslan vangreiddi reikningsupphæð
-   Ef greiðsluupphæðin er jafnt og upphæð reikningsins, er bæði greiðslu og reiknings lokaðar, og stöðu bæði er 0,00.

Ef [greiðslu er lægri en reikningsupphæðin](../accounts-payable/vendor-payments-partial-amount.md) vegna staðgreiðsluafsláttar, afskriftar eða vangreiðslu, gætu reiknings og greiðslu enn verið lokað, eftir uppsetningu á jöfnun í færibreytum viðskiptaskulda og færibreytur viðskiptakrafna. Jöfnun getur einnig myndað færslur. Til dæmis gæti jöfnun reiknings og greiðslu framleitt staðgreiðsluafslátt, innleystan hagnaður eða tap, leiðréttingar virðisaukaskatts, afskriftir eða auramismun.


## <a name="additional-resources"></a>Frekari upplýsingar
- [Gera upp eftirstöðvar](settle-remainder.md)

