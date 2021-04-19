---
title: Úrræðaleit fyrir hleðsluáætlun og sendingar
description: Þetta efnisatriði lýsir hvernig á að leysa algeng vandamál sem kunna að koma upp þegar unnið er með hleðsluáætlun og sendingar í Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 10/19/2020
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
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: e9964376a794661058da78152879d2142dd7ec51
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828203"
---
# <a name="troubleshoot-load-building-and-shipments"></a>Úrræðaleit fyrir hleðsluáætlun og sendingar

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir hvernig á að leysa algeng vandamál sem kunna að koma upp þegar unnið er með hleðsluáætlun og sendingar í Microsoft Dynamics 365 Supply Chain Management.

## <a name="i-receive-the-following-error-message-you-cant-create-a-load-line-for-this-order-line-because-it-contains-inventory-dimensions-that-are-invalid"></a>Ég fæ eftirfarandi villuboð: „Ekki er hægt að stofna farmlínu fyrir þessa pöntunarlínu vegna þess að hún inniheldur ógildar birgðavíddir...“

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Eftirfarandi villuboð birtast þegar reynt er að losa skilapöntun í vöruhúsið:

> Ekki er hægt að stofna hleðslulínu fyrir þessa pöntunarlínu vegna þess að hún inniheldur ógildar birgðavíddir. Ekki er hægt að vísa til birgðavídda sem eru staðsettar fyrir neðan staðsetningarvíddina í frátekningarstigveldinu. Fjarlægðu ógildu víddirnar úr pöntunarlínunni.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Því miður styður afurðin ekki hleðsluvinnslu fyrir söluskilaferli. Þar af leiðandi er ekki hægt að losa sölupöntun aftur í vöruhúsið.

Í sölupöntunarfærslum er ekki hægt að vísa til birgðavídda sem eru staðsettar fyrir neðan víddina **Staðsetning** í frátekningarstigveldinu. Lausnin við slíku er að fjarlægja ógildu víddirnar úr pöntunarlínunni.

## <a name="i-receive-the-following-error-message-one-of-the-lines-is-already-on-a-load-unable-to-release-to-warehouse"></a>Ég fær eftirfarandi villuboð: „Ein línanna er þegar í farmi. Ekki er hægt að losa í vöruhús“.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Þegar farmur er búinn til handvirkt, eða þú setur upp ferlið þannig að farmur er þegar búinn til áður en færsla sölupöntunarlínunnar á sér stað, er gert ráð fyrir því að þar á eftir fari losun fram handvirkt og notast verði við leið og flokkun farmsins.

Við aðrar hugsanlega aðstæður reynir þú sjálfvirka losun í vöruhúsið en bylgjuferlinu mistókst að stofna vinnu. Þar af leiðandi er opin sending eða opinn farmur samt sem áður búin til. Slík opin sending eða opinn farmur loka síðan á tilraunir þar á eftir til að losa sjálfkrafa pöntunina þar til þú annað hvort eyðir opnu sendingunni eða opna farminum eða endurvinnur bylgjuna handvirkt.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Þú getur losað frá sölupöntunarsíðunni eða losað sjálfvirkt á sölupöntunarsíðu losunar, en einungis ef enginn farmur er fyrir hendi áður en losað er í vöruhúsið. Farmurinn verður sjálfkrafa búinn til eftir að úrvinnslu bylgjunnar er lokið.

## <a name="i-receive-the-following-error-message-the-delivery-note-correction-cant-be-processed-the-delivery-note-only-contains-items-that-are-subject-to-warehouse-management-processes-as-these-are-not-supported-by-delivery-note-correction"></a>Ég fæ eftirfarandi villuboð: „Ekki er hægt að vinna úr leiðréttingu fylgiseðilsins. Fylgiseðillinn inniheldur eingöngu atriði sem falla undir vöruhúsakerfisferli, vegna þess að slík atriði eru ekki studd af leiðréttingu fylgiseðilsins“.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Þegar lokið er við að bóka fylgiseðil er ekki hægt að hætta við hann vegna þess að hnappurinn **Hætta við** er ekki tiltækur. Ennfremur er ekki hægt að leiðrétta fylgiseðilinn. Eftirfarandi villuboð birtast ef þú reynir slíkt.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Þú verður að bóka af farminum en ekki beint af pöntuninni til að leiðrétta bókaða fylgiseðla fyrir atriði sem eru virk í ítarlegu vöruhúsakerfi (WMS).

## <a name="how-can-i-create-work-from-outbound-loads-instead-of-waves"></a>Hvernig stofna ég vinnu í farmi á útleið í stað bylgja?

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Hér er ein leið til að endurskapa þetta vandamál.

1. Búðu til farm á útleið úr sölupöntun eða flutningspöntun.
2. Losið hleðsluna í vöruhúsið.
3. Taktu eftir því að engin tiltekt hefur enn verið mynduð.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Þegar mynda skal vinnu um leið og farmur er losaður verður þú að grunnstilla bylgjusniðmátið því til samræmis. Stilltu eftirfarandi valkosti á *Já* á bylgjusniðmátinu:

- Gera stofnun bylgju sjálfvirka
- Vinna úr bylgju við losun í vörugeymslu
- Gera losun bylgju sjálfvirka

## <a name="i-cant-re-release-a-partially-shipped-load"></a>Ég get ekki losað aftur um farm sem hefur verið sendur að hluta til.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Þú getur ekki losað um farm í vöruhúsið sem hefur verið sendur að hluta til. Þegar þú losar í vöruhúsið birtast skilaboðin „Aðgerðinni er lokið“ en ekkert gerist og engin vinna er mynduð fyrir magnið sem eftir er. Þetta vandamál á sér stað þegar þú notar virkni farmflutnings og frátekning er ekki fullfrágengin.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

[KB vandamál 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) („Farmur sem hefur verið sendur að hluta til er hægt að setja í aðra bylgju og aðra úrvinnslu“) er leyst í [útgáfu 10.0.15](../get-started/whats-new-scm-10-0-15.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]