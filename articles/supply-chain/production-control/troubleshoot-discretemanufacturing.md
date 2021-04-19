---
title: Úrræðaleit fyrir afmarkaða framleiðslu
description: Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með afmarkaða framleiðslu.
author: SmithaNataraj
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: b9c43d59e8022a365853f4b9cbb32ac3c3074e3f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810919"
---
# <a name="troubleshoot-discrete-manufacturing"></a>Úrræðaleit fyrir afmarkaða framleiðslu

Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með afmarkaða framleiðslu.

## <a name="i-receive-the-following-error-message-warehouse-management-processes-are-currently-being-used-if-work-lines-are-not-yet-registered-you-can-cancel-the-created-work-and-any-load-or-shipment-lines-and-then-continue-with-the-picking-or-shipping-process"></a>Ég fæ eftirfarandi villuboð: „Verið er að nota ferli vöruhúsakerfa“. Ef verklínur hafa ekki enn verið skráðar er hægt að hætta við stofnaða verkið og hvaða hleðslu- eða sendingarlínur sem er og halda svo áfram með tiltektar- eða sendingarferlið.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Þetta vandamál á sér stað ef reynt er að taka frá eða losa vinnu fyrir línu, en birgðafærslan er með stöðuna *Tínd*, sem gefur til kynna að búið sé að taka hana til.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Fylgið einu af eftirfarandi skrefum til að laga þetta.

- Breytið stöðu framleiðslupöntunarinnar aftur í *Áætluð* eða *Losuð*.
- Opnar upplýsingasíða fyrir tengdu framleiðslupöntunina. Í aðgerðasvæði, á flipanum **Vöruhús**, í **Stöðva** skal velja **Stöðva og afturkalla tiltekt** til að afturkalla tiltekt allra færslna. Síðan skal velja **Fjarlægja stöðvun** til að vinna úr framleiðslupöntuninni.

Hér er útskýring á aðgerðunum *Afturkalla tiltekt* og *Stöðva*:

- **Afturkalla tiltekt** – Þessi aðgerð bakfærir stöðu birgðafærslna fyrir uppskriftalínur og formúlulínur sem hafa stöðuna úr *Tiltekið* til *Í pöntun*. Þegar vinnu við hráefnistínslu er lokið er staða línanna stillt á *Tekið til*. Þessi staða kemur í veg fyrir að framleiðslupöntunin sé endurstillt á stöðuna *Stofnað*. Í þessu tilvikum er hægt að nota aðgerðina *Afturkalla tiltekt* til að snúa færslunum aftur úr *Tekið til* stöðunni og endurstilla svo framleiðslupöntunina í stöðuna *Stofnað*.
- **Stöðva** – Þessi aðgerð setur flaggið **Stöðvað** á framleiðslupöntun til að koma í veg fyrir stöðuuppfærslu á pöntuninni. Hægt er að finna **Stöðvað** flaggið í flipanum **Vöruhús** á upplýsingasíðu framleiðslupöntunar.

> [!NOTE]
>
> - Hnapparnir eru aðeins sýnilegir þegar framleiðslupöntunin er stofnuð fyrir vörur sem eru virkar fyrir vöruhúsaferli.
> - **Stöðva** flokkurinn er aðeins sýnilegur á flipanum **Vöruhús** á aðgerðasvæði á upplýsingasíðu framleiðslupöntunar. Það er ekki sýnilegt á flipanum **Vöruhús** á listasíðunni **Framleiðslupantanir**.

## <a name="the-matching-resource-name-isnt-updated-after-i-change-a-worker-name-in-the-global-address-book"></a>Samsvarandi tilfangaheiti er ekki uppfært eftir að nafni starfskrafts er breytt í altækri aðsetursbók.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Ef nafni starfskrafts er breytt í altæku aðsetursbókinni er samsvarandi heiti ekki uppfært í aðaltilfangaflokki.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Þessar aðstæður er ekki studdar eins og er. Til að laga vandamálið þarf að uppfæra heiti tilfanga handvirkt.

## <a name="when-i-create-a-new-production-order-i-dont-receive-the-following-message-insert-the-active-version-of-bill-of-material-and-route"></a>Þegar ég bý til nýja framleiðslupöntun fæ ég ekki eftirfarandi skilaboð: „Setjið inn virka útgáfuna uppskriftar og leið?“

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Þegar ný framleiðslupöntun er stofnuð þegar búið er að færa inn vörunúmerið eru reitirnir **Svæði** og **Vöruhús** sjálfkrafa stilltir á sjálfgefið svæði og vöruhús sem eru skilgreind á síðunni **Sjálfgefnar pöntunarstillingar** fyrir fullunna vöru. Þar að auki er virka uppskriftarnúmerið mitt og leiðarnúmer sjálfkrafa færð inn. Þú færð ekki eftirfarandi skilaboð sem biðja þig um þessi gildi:

> Á að setja inn virka útgáfu fyrir uppskrift og leið?

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Notandi er ekki beðinn um að setja inn uppskrift og leiðarnúmer ef afurð er valin sem svæði og vöruhús eru skilgreind fyrir á síðunni **Sjálfgefnar pöntunarstillingar**. Beiðni birtist aðeins ef gildin eru ekki skilgreind fyrir valda afurð.

## <a name="production-orders-arent-shown-on-the-marking-page"></a>Framleiðslupantanir eru ekki sýndar á síðunni Merking.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Sumar framleiðslupantanir eru ekki sýndar á síðunni **Merking**.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Ekki er hægt að merkja vörur sem hafa eftirfarandi stillingar. Þess vegna birtast þær ekki á síðunni **Merking**:

- Afurðirnar eru skilgreindar sem afurðir af gerðinni *þyngd afurðar*.
- Þær eru virkjaðar fyrir ítarleg vöruhúsaferli.
- Þeim er grunnstillt til að stjórna reglunni *Staðalkostnaður*.

## <a name="when-i-try-to-end-a-production-order-i-receive-the-following-error-message-calculating-bom-consumptioncost-value-must-be-negative-upon-issue-from-inventory"></a>Þegar ég reyni að ljúka við framleiðslupöntun fæ ég eftirfarandi villuboð: „Útreikningur á gildi consumptionCost uppskriftar verður að vera neikvæður við úthreyfingu úr birgðum.“

Þetta vandamál var lagfært í útgáfu 10.0.15.

## <a name="when-the-status-of-a-production-order-is-changed-from-reported-as-finished-to-end-i-receive-the-following-error-messages-update-conflict-the-standard-cost-does-not-match-with-the-financial-inventory-value-after-the-update-and-a-critical-error-has-occurred-in-function-inventcostmovementcheckvariance"></a>Þegar stöðu framleiðslupöntunar er breytt úr Tilkynna sem tilbúið í lokið, fæ ég eftirfarandi villuboð: „Uppfærsluárekstur“. Staðalkostnaður stemmir ekki við gildi fjárhagslegra birgða eftir uppfærsluna og Alvarleg villa varð í aðgerð InventCostMovement.checkVariance.

Þetta vandamál á sér stað vegna þess að undirliggjandi gögnum var breytt í öðru ferli. Ferlið mun reyna að uppfæra gögnin allt að fimm sinnum. Ef áreksturinn er enn til staðar eftir fimm tilraunir verða eftirfarandi villuboð send:

> Uppfæra árekstur. Staðalkostnaður stemmir ekki við gildi fjárhagslegra birgða eftir uppfærsluna.

> Alvarleg villa varð í aðgerð InventCostMovement.checkVariance.

Þessi hegðun er samkvæmt hönnuninni. Til að laga vandamálið skal halda áfram með runuvinnsluna. Það ætti að ljúka vinnslu.

Ef runuvinnslan mistekst endurtekið þegar henni er haldið áfram skal ganga úr skugga um að sléttunarnákvæmni fyrir sjálfgefinn gjaldmiðil fjárhags fylgi sléttunarreglum sem eru notaðar fyrir gildi í töflunni InventSum. Ef sléttunarnákvæmni hefur verið breytt í ósamræmanlegt gildi verður líklega að breyta henni aftur í samræmanlegt gildi. Leitið að **ModifiedDateTime**. Í þessu tilvikum sýnir gildið venjulega að sléttunarnákvæmni var breytt nýlega.

## <a name="when-i-release-to-a-warehouse-i-receive-the-following-error-message-item-rm-could-not-be-fully-reserved-ensure-that-the-full-quantity-is-available-or-reserve-the-items-manually-if-the-reservation-field-on-the-bom-line-is-set-to-manual-or-started-could-not-release-the-order-to-warehouse-because-some-materials-could-not-be-reserved-however-the-status-is-updated-to-released"></a>Þegar ég losa í vöruhús fæ ég eftirfarandi villuboð: „Ekki var hægt að taka vöru RM frá að fullu. Tryggið að fullt magn sé tiltækt eða takið vöruna frá handvirkt ef reiturinn Frátekning á uppskriftarlínunni er stilltur á Handvirkt eða Byrjað. Ekki var hægt að losa pöntunina í vöruhús því að ekki tókst að taka einhver hráefni frá. Hins vegar er staðan uppfærð í Losað.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Ef það eru ekki allar vörulínur uppskriftar efnislega til staðar þegar framleiðslupöntun er losuð og **Losa í vöruhús** er stillt á *Fullrar frátekningar er krafist* á framleiðslupöntuninni birtast eftirfarandi villuboð:

> Ekki var hægt að taka vöru RM frá að fullu. Tryggið að fullt magn sé tiltækt eða takið vöruna frá handvirkt ef reiturinn Frátekning á uppskriftarlínunni er stilltur á Handvirkt eða Byrjað. Ekki var hægt að losa pöntunina í vöruhús því að ekki tókst að taka einhver hráefni frá.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Þessi hegðun er samkvæmt hönnuninni og virkar eins og búist var við.

## <a name="when-i-try-to-end-a-production-order-and-report-as-finished-i-receive-the-following-error-message-total-good-quantity-reported-as-finished-for-the-production-will-be-1-feedback-for-the-last-operation-is-000-in-total"></a>Þegar ég reyni að ljúka framleiðslupöntun og tilkynna sem lokið, fæ ég eftirfarandi villuboð: „Samtals gallalaust magn, skráð tilbúið úr framleiðslunni verður %1“. Heildarsvörun síðustu aðgerðar er 0,00 alls.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Þegar reynt er að bóka skýrslu sem tilbúna færslubók í framleiðslupöntun birtast eftirfarandi villuboð:

> Samtals gallalaust magn, skráð tilbúið úr framleiðslunni, verður %1. Heildarsvörun síðustu aðgerðar er 0,00 alls.

### <a name="possible-cause"></a>Möguleg orsök

Þetta vandamál á sér stað ef magnið sem var bókað í síðustu aðgerðum var rangt. Ef framleiðsla er til dæmis hafin, en magninu sem þarf að hefja er ekki úthlutað, verður færslubók leiðarspjalds bókuð án nokkurra lína. Til að staðfesta ástandið skal opna framleiðslupöntunina og síðan, á aðgerðasvæðinu á flipanum **Skoða** skal velja **Leiðarspjald**.

### <a name="workaround"></a>Hjáleið

Hægt er að lagfæra þetta með því að bóka viðbótarbækur fyrir aðgerðirnar sem bækurnar voru ekki rétt bókaðar fyrir. Endurræsið framleiðslupöntunina og veljið að bóka fleiri færslubækur. Þessi aðgerð mun ekki ræsa framleiðslupöntunina, en hún bókar færslubækurnar. Leiðarspjaldið ætti síðan að sýna magnið sem var bókað og það ætti að vera hægt að ljúka framleiðslupöntunum.

## <a name="can-i-report-a-production-order-as-finished-while-i-report-the-error-quantity-but-not-while-i-report-the-time-or-material-quantity"></a>Er hægt að tilkynna framleiðslupöntun sem lokið á meðan tilkynnt er um villumagn, en ekki á meðan verið er að skrá tíma eða efnismagn?

Ekki er hægt að skrá villumagn í framleiðslupöntun nema einnig sé skráð rétt magn. Aðstæðurnar eru **ekki** studdar. Tilkynning sem lokið mistekst á endanum þegar reynt er að ljúka framleiðslupöntuninni og eftirfarandi villuboð birtast:

> Magn vantar til að tilkynna tilbúið.

## <a name="can-i-trace-the-serial-numbers-of-finished-goods-against-the-serial-numbers-of-consumed-goods"></a>Get ég rakið raðnúmer fullunninna vara á móti raðnúmerum notaðra vara?

Ekki er hægt að rekja raðnúmer fullunninna vara á móti raðnúmerum efnis sem framleiðslupöntun notar til að gera þessar fullunnu vörur. Þessar aðstæður er ekki studdar eins og er. Verið er að búa til framleiðslupantanir fyrir magnið 1.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]