---
title: Úrræðaleit fyrir tiltekt og pöntun
description: Þetta efnisatriði lýsir því hvernig á að laga almenn vandamál sem kunna að koma upp við tínslu og frágang í Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 01e33b63e09a035f5243bd57faf53b522737c987
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5223243"
---
# <a name="troubleshoot-picking-and-packing"></a>Úrræðaleit fyrir tiltekt og pöntun

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir því hvernig á að laga almenn vandamál sem kunna að koma upp við tínslu og frágang í Microsoft Dynamics 365 Supply Chain Management.

## <a name="i-receive-the-following-error-message-dimension-location-cant-be-left-blank-if-dimension-serial-number-is-set"></a>Ég fæ eftirfarandi villuboð: „Víddarstaðsetning má ekki vera skilin eftir auð ef raðnúmersvídd er stillt.“

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Þessi villuboð birtast ef flutningspöntun fyrir vöru með raðnúmeri er stofnuð með því að nota vöruhús sem er virkt fyrir ítarlega vöruhúsastjórnun (WMS), og svp er reynt að staðfesta sendinguna eftir að vinnu er lokið.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Reiturinn **Sjálfgefin staðsetning innhreyfinga** er auður fyrir flutningsvöruhús „úr“ vöruhúsi. Til að laga þetta vandamál þarf að tilgreina sjálfgefna staðsetningu móttöku í flutningsvöruhúsinu. Ganga skal úr skugga um að þessi staðsetning sé númeraplata – stjórnað.

## <a name="i-receive-the-following-error-message-invalid-license-plate"></a>Ég fæ eftirfarandi villuboð: „Ógild númeraplata.“

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Þessi villuboð birtast í vöruhúsaforritinu þegar kenni númeraplötu er skannað.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Ganga skal úr skugga um að númeraplötukennið sé til staðar í töflu númeraplatna og að vörurnar og magnið í númeraplötunni sé tiltækt (þ.e. að ekki sé lokað á það).

## <a name="i-receive-the-following-error-message-field-load-weight-1-can-only-contain-positive-numbers-update-has-been-canceled"></a>Ég fæ eftirfarandi villuboð: „Reitur „Hleðsluþyngd“(=-%1) getur aðeins innihaldið jákvæðar tölur. Hætt hefur verið við uppfærslu.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Þessi villuboð birtast ef verk er opið þegar unnið er úr vinnu úr pökkunarstaðsetningum í geymslustaðsetningar eða úr geymslustaðsetningum í innhlið.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Til að laga þetta vandamál skal fara í **Kerfisstjórnun \> Reglubundin verk \> Gagnagrunnur \> Samræmisathugun** og keyra ferlið fyrir **Samræmisathugun á hleðsluþyngd vöruhúss**.

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a>Ég fæ eftirfarandi villuskilaboð: „Magnið er ekki gilt fyrir einingu %1“.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Þessi villuboð birtast þegar reynt er að framkvæma *Skipta tiltekt* á mörgum runum.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Starfskraftur í vöruhúsi verður að nota ferlið *Stutt tiltekt* í vöruhúsaforritinu. Ef reynt er að taka til margar runur úr sömu staðsetningunni er einnig hægt að nota valkostinn **Full** í vöruhúsaforritinu.

## <a name="i-cant-move-inventory-to-a-location-that-is-license-platecontrolled"></a>Ég get ekki flutt birgðir á staðsetningu sem er númeraplata – stýrt.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Ekki er hægt að minnka tiltektarmagn í farmi.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Í fyrri útgáfum er ekki hægt að minnka tiltektarmagn farms. Hins vegar er nú hægt að taka tiltekt til baka á staðsetningu sem er númeraplötustýrð. Tilgreina þarf bæði gildi fyrir **Staðsetningu** og **Númeraplötu** fyrir hleðslulínuna á síðunni **Minnka tiltektarmagn**.

## <a name="can-i-print-a-delivery-note-or-packing-content-by-warehouse"></a>Get ég prentað út fylgiseðil eða efni eftir vöruhúsi?

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Þú vilt prenta afhendingarnótu eða fylgiseðil eftir vöruhúsi eða svæði á síðunni **Uppfærsla á línum í sniðmáti vinnuendurskoðunar** .

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Þegar skjal er prentað með því að nota stillingar prentstýringar skal takmarka umfangið (svæði/vöruhús) í gegnum prentstýringu í stað þess að velja **Breyta prentstillingum** á síðunni **Uppfæra línu vinnuendurskoðunarsniðmáts**.

## <a name="i-cant-cancel-a-packing-slip-after-its-posted-from-a-sales-order"></a>Ekki er hægt að hætta við fylgiseðil eftir að hann hefur verið bókaður úr sölupöntun.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Þegar tiltektar- og afhendingarferlin eru virkjuð fyrir vöruhúsakerfi er ekki hægt að hætta við fylgiseðil þegar búið er að bóka hann í sölupöntun.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Til að leiðrétta bókaða fylgiseðla fyrir vörur sem eru virkar í vöruhúsakerfi þarf bókunin að gerast í hleðslunni, ekki pöntuninni. Microsoft hefur metið þetta mál og hefur ákvarðað að þetta sé takmörkun eiginleika. Sölupöntun sem hefur verið tínd og send í gegnum vöruhúsakerfisferla er almennt hægt að uppfæra fylgiseðil fyrir í hleðslunni eða sendingunni og sjálfu sölupöntunarskjalinu. Ef fylgiseðill í sölupöntun er hinsvegar uppfærður úr sölupöntunarskjalinu, verður samt ekki hægt að afturkalla fylgiseðil úr hleðslunni eða sölupöntuninni. Þess vegna er mælt með því að bókun fylgiseðilsins sé notuð úr hleðslunni. Í þessu tilfellum er bakfærslan sem verður að vera gerð úr hleðslunni gerð virk.

## <a name="i-receive-the-following-error-message-not-enough-work-can-be-found-for-cluster"></a>Ég fæ eftirfarandi villuboð „Ekki finnst nægileg vinna fyrir klasann“.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Þegar ferlið *Kerfisstýrð klasatiltekt* er notað, ef klasaforstilling er skilgreind þar sem t.d. hægt er að tína úr 10 staðsetningum, virkar ferlið samkvæmt áætlun þegar næg vinna er til að tína í 10 staðsetningum. Ef hinsvegar aðeins átta staðsetningar eru til að tína úr, koma upp þessi villuboð vegna þess að ekki er nóg vinna fyrir einn klasa.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Til að laga þetta vandamál skal breyta klasaforstillingunni og stilla valkostinn **Virkja stöður** á *Nei*.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]