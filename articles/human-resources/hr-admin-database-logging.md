---
title: Skilgreina og stjórna gagnagrunnsskráningu
description: Hægt er að rekja breytingar til taflna og reita í Dynamics 365 Human Resources með gagnagrunnsskráningu.
author: Darinkramer
manager: AnnBe
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3dc4658a0a13af95978c66f5aab882902f754a2d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419022"
---
# <a name="configure-and-manage-database-logging"></a>Skilgreina og stjórna gagnagrunnsskráningu

Hægt er að rekja breytingar til taflna og reita í Dynamics 365 Human Resources með gagnagrunnsskráningu. Þetta efnisatriði lýsir hvernig á að:

- Stjórna öryggi og afköstum fyrir skráningu gagnagrunns
- Setja upp gagnagrunnsskráningu
- Hreinsa upp gagnagrunnsskrár

## <a name="overview-of-database-logging"></a>Yfirlit gagnagrunnsskráningar

Skráning gagnagrunns rekur sérstakar breytingar til taflna og reita Microsoft Dynamics 365 Human Resources. Þessar breytingar fela í sér að setja inn, uppfæra eða eyða. Gagnagrunnsskráning geymir færslur yfir breytingar á töflum í töflu gagnagrunnsskráar.

Notkun fyrirtækis á gagnagrunnsskráningu felur í sér:

- Að búa til eftirlitsfærslu yfir breytinga á tilteknum töflum sem innihalda viðkvæmar upplýsingar.
- Rakning einstakra færslna. Gagnagrunnsskráning er ekki ætluð til þess að rekja sjálfvirkar færslur sem eru keyrðar í runuvinnslum.

## <a name="security-for-database-logging"></a>Öryggi fyrir gagnagrunnsskráningu

Gagnagrunnskladdar geta innihaldið viðkvæm gögn. Takmarkið aðgang til að hafa aðeins öryggishlutverk sem þurfa aðgang að skráningargögnum.

## <a name="database-logging-and-performance"></a>Gagnagrunnsskráning og afköst

Þótt þetta sé mikilvægt fyrir fyrirtækið, getur gagnagrunnsskráning verið dýr í notkun á tilföngum og stjórnun. Afköst vegna gagnagrunnsskráningar fela í sér:

- Tafla gagnagrunnsskráar getur vaxið hratt og leitt til stækkunar á gagnagrunninum. Vöxtur veltur á magni skráðra gagna sem þú ákveður að geyma. Sjálfgefið er að tafla gagnagrunnsskráar haldi við aðeins 30 dögum af skráningargögnum. 

- Gagnagrunnsskráning getur haft neikvæð áhrif á sjálfvirk langtímaferli, t.d. langtíma gagnainnflutning.

### <a name="best-practices"></a>Bestu venjur

Til að bæta afköst skal takmarka færslur skráar með því að velja tiltekna reiti til að skrá í stað heilla taflna. Til að stuðla að betri heildarafköstum takmarkast gagnagrunnsskráningar við 20 töflur.

> [!NOTE]
> Aðeins er hægt að skrá uppfærslur fyrir einstaka reiti.

## <a name="set-up-database-logging"></a>Setja upp gagnagrunnsskráningu

Hægt er að nota leiðsagnarforritið **Skrifa gagnagrunnsbreytingar í kladda** til að setja upp gagnagrunnsskráningu. Leiðsagnarforritið býður upp á sveigjanlega leið til að setja upp kladdaskráningu fyrir töflur og reiti.

1. Farið í **Kerfisstjórnun > Tenglar > Gagnagrunnur > Uppsetning gagnagrunnskladda**. Veljið **Nýr** til að hefja leiðsagnarforritið **Skrifa gagnagrunnsbreytingar í kladda**.
2. Leiðsagnarforritinu er síðan fylgt til loka.

## <a name="clean-up-database-logs"></a>Hreinsa upp gagnagrunnsskrár

Hægt er að eyða öllum eða hluta af gagnagrunnsklöddunum með því að nota eftirfarandi valkosti:

- Veljið alla kladda fyrir tiltekna töflu.
- Veljið tiltekna gerð af gagnagrunnskladda.
- Veljið dagsetningu og tíma sem kladdi var stofnaður á.

Til að setja upp hreinsun gagnagrunnskladda skal fylgja þessum skrefum: 

1. Farið í **Kerfisstjórnun > Tenglar > Gagnagrunnur > Gagnagrunnskladdi**. Veljið **Hreinsa kladda**.

2. Veljið aðferð við að velja kladda sem á að eyða með því að færa inn einn af eftirfarandi valmöguleikum:

   - Töflu-ID
   - Gerð kladda
   - Tími og dagsetning stofnunar

3. Notið flipann **Hreinsun gagnagrunnskladda** til að ákveða hvenær keyra á hreinsunarverk kladdans. Gagnagrunnskladdar eru í boði í 30 daga að sjálfgefnu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]