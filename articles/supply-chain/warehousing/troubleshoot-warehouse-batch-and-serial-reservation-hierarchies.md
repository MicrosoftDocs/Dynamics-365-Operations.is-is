---
title: Úrræðaleit fyrir keyrslur vöruhúss og frátekningastigveldi raða
description: Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með frátekningastigveldi sem nota runu- eða raðnúmeravíddir.
author: perlynne
ms.date: 3/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 3/12/2021
ms.openlocfilehash: 1cd4883cdd95a97f821e0103da910e2c0346a08d
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022547"
---
# <a name="troubleshoot-warehouse-batch-and-serial-reservation-hierarchies"></a>Úrræðaleit fyrir keyrslur vöruhúss og frátekningastigveldi raða

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með frátekningastigveldi sem nota runu- eða raðnúmeravíddir.

Frekari upplýsingar er að finna í [Sveigjanleg frátektarregla á vídd vöruhúsastigs](flexible-warehouse-level-dimension-reservation.md).

Frátekningastigveldi vöru segir til um kröfur geymsluvídda sem þarf að uppfylla til að úthluta staðsetningu á eftirspurnarpöntun. Hægt er að lýsa þessum víddum sem *víddum fyrir ofan staðsetningu* fyrir allar víddirnar sem þarf að uppfylla áður en staðsetningu er úthlutað og *víddir fyrir neðan staðsetningu* fyrir víddir sem hægt er að úthluta eftir að staðsetningu hefur verið úthlutað á eftirspurnarpöntunina. Þessi frátekningastigveldi eru einnig þekkt sem *runa fyrir ofan* og *runa fyrir neðan* frátekningastigveldi, eða *raðnúmer fyrir ofan* og *raðnúmer fyrir neðan* frátekningastigveldi.

Aðeins er hægt að úthluta birgðum ef engar eyður eru í víddunum fyrir ofan staðsetningu. Til dæmis má búast við að í *runa fyrir ofan* frátekningarstigveldi séu víddirnar **Svæði**, **Vöruhús** og **Rununúmer** tilgreindar í eftirspurnarpöntuninni. Ef einhverjar af þessum víddum vantar mun úthlutunarferlið mistakast. Hins vegar, í *runa fyrir neðan* eða *raðnúmer fyrir neðan* frátekningastigveldi gæti runu- eða raðnúmer verið tilgreint í eftirspurnarpöntuninni, en úthlutunarferlið krefst þess ekki.

## <a name="i-receive-the-following-error-message-to-be-assigned-to-wave-load-lines-must-specify-the-dimensions-above-the-location-to-assign-these-dimensions-reserve-and-recreate-the-load-line"></a>Ég fæ eftirfarandi villuboð: „Til að úthluta bylgju verða hleðslulínur að tilgreina víddirnar fyrir ofan staðsetninguna. Til að úthluta þessum víddum skal taka hleðslulínuna frá og endurgera hana.“

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Þegar notuð er vara með *runa fyrir ofan* frátekningastigveldi mun skipunin **Losa í vöruhús** á síðunni **Vinnusvæði hleðsluáætlunar** ekki virka ef reynt er að losa hleðslu fyrir hlutamagn. Þessi villuskilaboð berast og engin vinna er stofnuð fyrir hlutamagnið.

Hins vegar, þegar notuð er vara sem er með *runa fyrir neðan* frátekningastigveldi, er hægt að losa hleðslu fyrir hlutamagn á síðunni **Vinnusvæði hleðsluáætlunar**.

### <a name="issue-cause"></a>Ástæða vandamáls

Þegar vídd er fyrir ofan víddina **Staðsetning** er sett upp í frátekningarstigveldi verður að tilgreina hana áður en hún er losuð í vöruhúsið. Ekki er hægt að losa hlutamagn ef ein eða fleiri vídd fyrir ofan **Staðsetning** eru ekki tilgreindar.

## <a name="the-auto-reservation-prompt-for-a-batch-number-is-triggered-even-though-there-is-available-inventory"></a>Kvaðning sjálfvirkrar frátekningar fyrir rununúmer er sett í gang þó að tiltækar birgðir séu í boði.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Þegar notuð er vara sem er með *runa fyrir ofan* frátekningastigveldi í vöruhúsi sem hefur ekki virkjað vöruhúsaferla og sjálfvirk frátekning er virkjuð, birtist kvaðning sjálfvirkrar frátekningar fyrir rununúmer þótt aðeins ein runa er tiltæk fyrir tiltekt.

Hins vegar þegar sama varan er notuð í vöruhúsi þar sem vöruhúsaferli eru virkjuð, er kvaðning sjálfvirkrar frátekningar ekki sýnd.

### <a name="issue-cause"></a>Ástæða vandamáls

Ef frátekningastigveldi er skilgreint sem *runa fyrir ofan* eða *raðnúmer fyrir ofan* verður alltaf að tilgreina vídd sem vísað er í (**Rununúmer** eða **Raðnúmer**) í eftirspurnarpöntunum. Vöruhúsaferli gætu lokið upplýsingunum ef ein runa eða raðnúmer er í boði. En þar sem vöruhúsið er ekki virkjað fyrir vöruhúsaferli, verður notandinn alltaf að tilgreina allar víddir fyrir ofan **Staðsetningu**.

## <a name="slotting-templates-that-have-the-consider-on-hand-slot-criterion-dont-consider-current-on-hand-inventory-for-batch-enabled-items"></a>Hólfasniðmát sem eru með hólfaskilyrðið Íhuga magn í birgðum taka ekki til greina núverandi lagerbirgðir fyrir runuvirkar vörur.

Frekari upplýsingar er að finna í [Hólfaskipting vöruhúss](warehouse-slotting.md).

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Hólfasniðmát sem eru með hólfaskilyrðið *Íhuga magn í birgðum* taka ekki til greina núverandi lagerbirgðir fyrir *runu fyrir ofan* vörur. Þau taka þær aðeins til greina ef rununúmerið er tilgreint í sölupöntunarlínunni.

En þegar notuð er *runa fyrir ofan* vörur verða núverandi lagerbirgðir teknar til greina eins og vænta má.

### <a name="issue-cause"></a>Ástæða vandamáls

Hægt er að skilgreina haus hólfasniðmáts fyrir eftirspurnarleiðina *Pantað*, *Frátekið* eða *Losað*. Fyrir eftirspurnarleiðina *Pantað* eiga sömu kröfur um frátekningastigveldi við og gilda um frátekningu eða losun í vöruhúsaferli. Þar af leiðandi, fyrir vörur sem eru með *runa fyrir ofan* og *raðnúmer fyrir neðan* frátekningastigveldi, þarf að tilgreina runu eða raðnúmer í eftirspurnarpöntuninni (sölu eða flutning). Annars er hægt að nota eftirspurnarleiðina *Frátekið* til að velja runu eða raðnúmer áður en eftirspurn eftir hólfaskiptingu í vöruhúsi er búin til.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
