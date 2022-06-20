---
title: Skilgreina og stjórna gagnagrunnsskráningu
description: Hægt er að rekja breytingar til taflna og reita í Dynamics 365 Human Resources með gagnagrunnsskráningu.
author: twheeloc
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8faf0be5f094f18b75f2263fa622c9b7f3983274
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899764"
---
# <a name="configure-and-manage-database-logging"></a>Skilgreina og stjórna gagnagrunnsskráningu


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Hægt er að rekja breytingar til taflna og reita í Dynamics 365 Human Resources með gagnagrunnsskráningu. Þessi grein lýsir því hvernig á að:

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
2. Veljið **Næst**. 
3. Á síðunni **Töflur og svæði** í leiðsagnarforritinu skal velja töflurnar og reitina sem á að virkja gagnagrunnsinnskráningu fyrir og velja **Áfram**.

   > [!Note]
   > Gagnagrunnsskráning er ekki tiltæk í öllum töflum í gagnagrunni mannauðs. Með því að velja **Sýna allar töflur** fyrir neðan listann stækkar listinn yfir töflur og reiti og sýnir allar gagnagrunnstöflur þar sem gagnagrunnsinnskráning er í boði, en þetta verður undirmengi á heildarlistanum yfir gagnagrunnstöflur.

4. Á **Gerðir breytinga** síðu leiðsagnarforritsins skal velja gagnaaðgerðirnar sem eigia að rekja breytingar fyrir hverja töflu og reiti og velja **Áfram**. Sjá töfluna hér fyrir neðan fyrir lýsingu á gagnavirkni sem eru í boði fyrir skráningu.
5. Á síðunni **Ljúka** skal fara yfir breytingarnar sem verða gerðar og velja **Ljúka**.

| Aðgerð | lýsing |
| -- | -- |
| Rekja nýjar færslur | Búa til kladda fyrir nýjar færslur sem eru búnar til í töflunni. |
| Update | Búa til kladda fyrir uppfærslur á töflufærslum eða uppfærslur á hvern sérvalinn reit í töflunni. Ef valið er að skrá uppfærslur fyrir töfluna er kladdafærsla búin til í hvert skipti sem verið er að uppfæra hvaða reit sem er í hvaða færslu sem er í töflunni. Ef valið er að skrá uppfærslur fyrir tiltekna reiti er kladdafærsla aðeins búin til þegar uppfærslur eru gerðar á þessum reitum í töflufærslum. |
| Eyða | Búa til kladda fyrir færslur sem er eytt úr töflunni. |
| Endurnefna lykil | Búa til annálafærslu þegar töflulykill er endurnefndur. |


## <a name="clean-up-database-logs"></a>Hreinsa upp gagnagrunnsskrár

Hægt er að eyða öllum eða hluta af gagnagrunnsklöddunum með því að nota eftirfarandi valkosti:

- Veljið alla kladda fyrir tiltekna töflu.
- Veljið tiltekna gerð af gagnagrunnskladda.
- Veljið dagsetningu og tíma sem kladdi var stofnaður á.

Til að setja upp hreinsun gagnagrunnskladda skal fylgja þessum skrefum: 

1. Farið í **Kerfisstjórnun > Tenglar > Gagnagrunnur > Gagnagrunnskladdi**. Veljið **Hreinsa kladda**.
2. Undir **Skrár til að hafa með** haus, veldu **Sía**.
3. Veldu aðferðina sem verður notuð til að velja annála til að eyða. Sláðu inn einn af eftirfarandi valkostum:

   - Töflu-ID
   - Gerð kladda
   - Tími og dagsetning stofnunar

4. Notið flipann **Hreinsun gagnagrunnskladda** til að ákveða hvenær keyra á hreinsunarverk kladdans. Gagnagrunnskladdar eru í boði í 30 daga að sjálfgefnu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
