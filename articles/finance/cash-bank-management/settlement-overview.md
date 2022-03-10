---
title: Uppgjörsyfirlit
description: Þetta efnisatriði veitir almennar upplýsingar um uppgjörsferlið. Í því er útskýrt hvaða færslugerðir er hægt að jafna og tímasetningin og ferlið við jöfnun þeirra. Þar eru niðurstöður jöfnunarferlisins einnig útskýrðar.
author: panolte
ms.date: 07/30/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "14551"
- intro-internal
ms.assetid: 0968fa71-5984-415b-8689-759a0136d5d1
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 57f2b209a852bb9513218fab3df118c7d7a2a1e7
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2022
ms.locfileid: "7986384"
---
# <a name="settlement-overview"></a>Uppgjörsyfirlit

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


Þetta efnisatriði veitir almennar upplýsingar um uppgjörsferlið. Í því er útskýrt hvaða færslugerðir er hægt að jafna og tímasetningin og ferlið við jöfnun þeirra. Þar eru niðurstöður jöfnunarferlisins einnig útskýrðar.

Við uppgjör, eru færslur á eitt skjal eru notuð í færslunum á annað skjal til að auka eða minnka stöðu hvers skjals. Til dæmis getur greiðsla verið beitt á reikning. Hægt er að jafna ýmsar færslugerðir, á mismunandi tímum og í með mismunandi aðferðum. Jöfnunarferlið getur einnig myndað nýjar færslur.

## <a name="what-transactions-can-be-settled"></a>Hvaða færslur er hægt að jafna

Jöfnun innan viðskiptaskulda og viðskiptakrafna geta átt sér stað milli hvaða færslugerða sem hafa áhrif á stöðu lánardrottins eða stöðu viðskiptavina. Þessar færslugerðir geta falið í sér reikninga, greiðslur, kreditreikninga og þóknanir. Hægt er að jafna allar færslugerðir gagnvart öllum öðrum færslugerð. Til dæmis er hægt að jafna greiðslu á móti reikningi, kreditreikning á móti reikningi, reikning á móti öðrum reikningi og greiðslu á móti annarri greiðslu.

Hægt er að jafna greiðslur gagnvart færslu í sama lögaðila eða annan lögaðila. Í fyrirtækjum sem nota miðstýrðt greiðslulíkan,geta [miðstýrðar greiðslur](set-up-centralized-payments.md) hjálpað til við að straumlínulaga greiðsluferlið.

## <a name="when-to-settle-transactions"></a>Hvenær á að Jafna færslur

Hægt er að jafna færslur þegar greiðslur eru færðar inn. Til dæmis þegar greiðsla er gerð til lánardrottins er oftast valið hvaða reikning á að borga. Með því að velja reikninga eru þeir merktir til jöfnunar gegn greiðslu. Þegar starfsmaður greiðslu fyrir viðskiptakröfur skráir viðskiptavinargreiðslu, geta þeir merkt viðeigandi reikninga fyrir jöfnun, byggt á upplýsingum sem er höfð með í greiðslu viðskiptavinar. Síðan **Jafna færslur** er notuð til að merkja færslur fyrir jöfnun. Hægt er að opna þessa síðu úr hvaða óbókuðum reikningi eða greiðslu. Þegar færslan er bókuð er jöfnunin einnig bókuð 

Einnig er hægt að jafna færslur eftir að þær eru bókaðar. Hægt er að færa inn og bóka greiðslu viðskiptavinar án þess að það eru jafnaðar gagnvart neinum reikninga. Hins vegar gæti þurft að ganga úr skugga um að greiðslan sé jöfnuð á móti rétta reikningnum áður en jöfnunin er bókuð. **Jafna færslur** síðan getur veri opnuð úr **Alla viðskiptavini** eða **Alla lánardrottna** síðu eða á **Færslur** síðu fyrir hvaða viðskiptavin eða lánardrottinn sem er.

Er hægt að taka frá bókaðar fyrirframgreiðslur fyrir reikning með því að merkja greiðslu fyrir jöfnun gagnvart innkaupapöntun eða sölupöntun. Í þessu tilfelli hefur greiðsla enn opin staða, en hún getur ekki verið jafnaðar á móti öðrum reikningi. Greiðslan verður sjálfkrafa jöfnuð á móti reikningi sem er stofnaður úr innkaupapöntun eða sölupöntun.

## <a name="how-to-settle-transactions"></a>Hvernig á að Jafna færslur

Hægt er að jafna færslur handvirkt, sjálfvirkt, eða sambland af aðferðunum tveimur. Val á jöfnunaraðferð fer eftir viðskiptaferlunum. Á síðunum **Færibreytur viðskiptaskulda** og **Færibreytur viðskiptakrafna** er hægt að grunnstilla jöfnunarferlið svo að það sé í samræmi við þessa viðskiptaferla.

Hægt er að stofna greiðslur lánardrottins og greiðslur viðskiptavina með greiðslutillögu. Greiðslutillaga er notuð til að velja reikninga til greiðslu. Greiðslutillaga er sett af stað handvirkt og svo merkir kerfið valda reikninga sjálfkrafa fyrir jöfnun þegar greiðslur eru stofnaðar.

Ef greiðslur eru stofnaðar handvirkt er hægt að nota í **Jafna færslur** síðu til að velja reikninga til jöfnunar. Hægt er að velja reikningana handvirkt eða nota **Merkja eftir forgangi** valkost til að hafa reikninga sjálfkrafa merkt til jöfnunar. Í **Merkja eftir forgangi** valkostur er einungis tiltæk fyrir viðskiptakröfur. Hægt er að kveikja á þessum valkosti í flipanum **Jöfnunarforgangur** á síðunni **Færibreytur viðskiptakrafna**.

Ef gjaldkeri færir inn greiðslu, en jafnar ekki greiðsluna áður en hún er bókuð, er hægt að jafna greiðsluna sjálfkrafa. Hægt er að virkja sjálfvirka jöfnun í **Færibreytur viðskiptakrafna** og **Færibreytur viðskiptaskulda**. Sjálfvirk jöfnun jafnar færslur aðeins á sama lögaðila. Hún jafnar ekki færslur yfir marga lögaðila.

Þegar sjálfvirk jöfnun er notuð er hægt að nota forskilgreindan jöfnunarforgang eða hægt er að skilgreina eigin jöfnunarforgang á síðunni **Færibreytur viðskiptakrafna**. Þessi eiginleiki er einungis tiltæk fyrir viðskiptakröfur.

## <a name="results-of-settlement"></a>Afleiðingar jöfnunar

Þegar færslur eru jafnaðar er útistandandi staða hverrar færslu aukinn eða minnkuð eins og við á. Vanalega, þar sem reikningur og greiðsla eru jafnaðar, er stöðu og hverrar færslu er uppfærð samkvæmt eftirfarandi reglum:

- Ef greiðsluupphæðin er hærri en reikningsupphæðin er staða reiknings er minnkað í 0,00 og reikningur er lokaður. Greiðslan helst opin og staðan er mismunurinn á milli greiðsluupphæðar og reikningsupphæðar.
- Ef greiðsluupphæðin er lægri en reikningsupphæðin er staða greiðslu er minnkað í 0,00 og greiðsla er lokaður. Reikningurinn helst opinn og staðan er mismunurinn á milli reikningsupphæðar og greiðsluupphæðar.
- Ef greiðsluupphæðin er sú sama og reikningsupphæðin verður bæði greiðslunni og reikningnum lokað og staða beggja lækkuð niður í 0,00.

Ef [greiðsluupphæð er lægri en reikningsupphæðin](../accounts-payable/vendor-payments-partial-amount.md) vegna staðgreiðsluafsláttar, afskriftar eða vangreiðslu, gætu reikningar og greiðslu enn verið lokað, eftir uppsetningu á jöfnun í **færibreytum viðskiptaskulda** og **færibreytum viðskiptakrafna**.

Jöfnun getur einnig myndað færslur. Til dæmis gæti jöfnun reiknings og greiðslu framleitt staðgreiðsluafslátt, innleystan hagnaður eða tap, leiðréttingar virðisaukaskatts, afskriftir eða auramismun.

## <a name="identifying-marked-transactions-during-settlement"></a>Að bera kennsl á merktar færslur þegar jöfnun er í gangi

Þegar reynt er að jafna færslu gætir þú tekið eftir tákni sem sýnir að færslan er merkt á öðrum stað. Í slíku tilfelli er hægt að velja færsluna á síðunni **Jafna færslur** og síðan velja **Fyrirspurn \> Jöfnun úr jöfnunarglugganum**. Yfirlitið fyrir þessa fyrirspurn sýnir færslubækur, sölupantanir, reikninga, greiðslutillögur og staðsetningar viðskiptavina sem gætu staðið í vegi fyrir jöfnun færslunnar. Til að leysa úr vandanum er hægt að velja tengilinn til að fara beint úr fyrirspurninni til útilokuðu staðsetningarinnar. Síðan er hægt að uppfæra skjalið með leiðréttingunum sem eru nauðsynlegar til að jafna það. Einnig er hægt að nota vísinn **Merkt** til að bera kennsl á önnur skjöl sem eru hluti af sömu útilokunarstaðsetningunni.

## <a name="resolve-issues-with-transactions-that-cant-be-settled"></a>Leysa vandamál með færslur sem ekki er hægt að ganga frá

Stundum er ekki hægt að ganga frá færslum vegna þess að önnur aðgerð er að vinna úr skjalinu. Ef þú reynir að ganga frá færslunum kemur upp villa vegna þess að þessar færslur eru í notkun. Til að leysa úr þessu vandamáli geturðu notað síðuna **Merktar færsluupplýsingar** til að finna færslur sem eru merktar fyrir jöfnun og borið kennsl á aðra ferla sem eru með aðgang að þeim.

Færslur eru merktar fyrir jöfnun annaðhvort þegar lánardrottnareikningar eru greiddir eða þegar viðskiptavinir greiða opna reikningana sína. Stundum getur þegar verið búið að merkja þessa reikninga fyrir jöfnun. Notendur geta því ekki valið þá til greiðslu. Reikningarnir gætu verið merktir af annarri greiðslubók viðskiptavinar, sölupöntun, greiðslubók lánardrottins eða innkaupapöntun í núverandi lögaðila eða öðrum lögaðila.

Ef lokað er fyrir jöfnun færslu þegar þú færir inn greiðslu viðskiptavinar skaltu opna síðuna **Færsluupplýsingar merktar viðskiptavini** (**Viðskiptakröfur \> Reglubundin verk \> Færsluupplýsingar merktar viðskiptavini**). Til að finna á fljótlegan hátt hvar lokað er á færslu geturðu stillt einhverjar af eftirfarandi valfæribreytum: **Viðskiptavinalykill**, **Fylgiskjal**, **Dagsetning** eða **Reikningur**. Ef þú stillir engar valfæribreytur sýnir kerfið öll útilokuð skjöl úr núverandi fyrirtæki eða öðru fyrirtæki sem þú velur. Eftir að færslan sem lokað hefur verið fyrir jöfnun er fundin geturðu valið hana og síðan valið **Afmerkja valdar færslur**. Valin færsla er síðan fjarlægð úr færslubókinni sem inniheldur hana. Hins vegar er skjalið ekki fjarlægt úr hinni staðsetningunni. Aðeins upplýsingar merkingar eru fjarlægðar úr þeirri færslubók.

Ef lokað er fyrir jöfnun á færslu þegar þú færir inn greiðslu lánardrottins skaltu opna síðuna **Færsluupplýsingar merktar lánardrottni** (**Viðskiptaskuldir \> Reglubundin verk \> Færsluupplýsingar merktar lánardrottni**). Til að finna á fljótlegan hátt hvar lokað er á færslu geturðu stillt einhverjar af eftirfarandi valfæribreytum: **Lánardrottnalykill**, **Fylgiskjal**, **Dagsetning** eða **Reikningur**. Ef þú stillir engar valfæribreytur sýnir kerfið öll útilokuð skjöl úr núverandi fyrirtæki eða öðru fyrirtæki sem þú velur. Eftir að færslan er fundin geturðu valið hana og síðan valið **Afmerkja valdar færslur** til að laga vandamál varðandi útilokun. Valin færsla er síðan fjarlægð úr öðrum færslubókum þar sem hún er valin. Hins vegar er skjalið ekki fjarlægt úr hinni staðsetningunni. Aðeins upplýsingar merkingar eru fjarlægðar úr þeirri færslubók.

Til að auðkenna öll útilokuð skjöl skal opna síðuna **Allar merktar færsluupplýsingar** (**Viðskiptakröfur \> Reglubundin verk \> Allar merktar færsluupplýsingar** eða **Viðskiptaskuldir \> Reglubundin verk \> Allar merktar færsluupplýsingar**). Til að finna á fljótlegan hátt hvar lokað er á færslu geturðu stillt einhverjar af eftirfarandi valfæribreytum: **Viðskiptavinalykill**, **Lánardrottnalykill**, **Fylgiskjal**, **Dagsetning** eða **Reikningur**. Ef þú stillir engar valfæribreytur sýnir kerfið öll útilokuð skjöl úr núverandi fyrirtæki eða öðru fyrirtæki sem þú velur. Eftir að færslan er fundin geturðu valið hana og síðan valið **Afmerkja valdar færslur** til að laga vandamál varðandi útilokun. Valin færsla er síðan fjarlægð úr öðrum færslubókum þar sem hún er valin. Hins vegar er skjalið ekki fjarlægt úr hinni staðsetningunni. Aðeins upplýsingar merkingar eru fjarlægðar úr þeirri færslubók.

Áður en hægt er að nota þennan eiginleika þarf að kveikja á honum í kerfinu. Stjórnendur geta notað vinnusvæði **Eiginleikastjórnun** til að athuga stöðu eiginleikans og kveikt á honum ef þörf krefur. Þar er eiginleikinn sýndur á eftirfarandi hátt:

- **Eining:** Reiðufjár- og bankastjórnun
- **Heiti eiginleika:** Skjámynd merktra færsluupplýsinga

## <a name="additional-resources"></a>Frekari upplýsingar

- [Gera upp eftirstöðvar](settle-remainder.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
