---
title: Áætlanagerð með innkaupaverðsamningum
description: Þetta efnisatriði lýsir því hvernig fínstilling áætlanagerðar getur fundið lánardrottin og/eða afhendingartíma fyrir áætlaða pöntun samkvæmt besta verðinu eða afhendingartíma sem er að finna í innkaupasamningum.
author: ChristianRytt
ms.date: 06/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 10b4f9f45899b808bd0baa73974a173cf120aa6c3fd33e10d0d79a59614f1f70
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6757759"
---
# <a name="master-planning-with-purchase-trade-agreements"></a>Áætlanagerð með innkaupaverðsamningum

[!include [banner](../../includes/banner.md)]

Þetta efnisatriði lýsir því hvernig fínstilling áætlanagerðar getur fundið lánardrottin og/eða afhendingartíma fyrir áætlaða pöntun samkvæmt besta verðinu eða afhendingartíma sem er að finna í öllum innkaupasamningum sem hafa verið tilgreindir fyrir tiltekna afurð.

## <a name="turn-on-the-purchase-trade-agreements-for-planning-optimization-feature"></a>Kveikja á innkaupasamningum fyrir eiginleika fínstillingar áætlanagerðar

Áður en hægt er að nota þennan eiginleika þarf að kveikja á honum í kerfinu. Stjórnendur geta notað vinnusvæði [Eiginleikastjórnun](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikt á honum ef þörf krefur. Þar er eiginleikinn sýndur á eftirfarandi hátt:

- **Eining:** *Aðaláætlanagerð*
- **Heiti eiginleika:** *Innkaupasamningar fyrir fínstillingu áætlanagerðar*

## <a name="prepare-your-system-to-evaluate-purchase-trade-agreements-during-master-planning"></a>Undirbúa kerfi til að meta innkaupasamninga við aðaláætlanagerð

Fylgið þessum skrefum til að skilgreina kerfið til að nota fínstillingu áætlanagerðar sem metur innkaupasamninga.

1. Farið í **Aðaláætlanagerð \> Uppsetning \> Færibreytur aðaláætlanagerðar**. Í flipanum **Áætlaðar pantanir**, í hlutanum **Lánardrottinn**, skal stilla eftirfarandi gildi:

    - **Finna verðsamninga** - Stillið þennan valkost á **Já** til að hafa með innkaupasamninga í aðaláætlanagerð.
    - **Leitarskilyrði** – Veljið þáttinn sem á að setja í forgang fyrir hvern verðsamning: **Lágmarksafhendingartími** eða **Lægsta einingaverð**.

1. Farið í **Innkaup og aðföng \> Uppsetning \> Verð og afslættir \> Virkja verð/afslátt** og gangið úr skugga um að valkosturinn **Lánardrottinn** sé stilltur á **Já**.
1. Farið í **Afurðaupplýsingastjórnun \> Uppsetning \> Vídda- og afbrigðaflokkar \> Geymsluvíddarflokkur** og veljið geymsluvíddarflokk sem á við um afurðir sem aðaláætlanagerð á að meta innkaupasamninga fyrir. Gangið úr skugga um að hver viðeigandi geymsluvídd í þessum flokki sé með gátmerki í dálknum **Fyrir innkaupaverð**. Endurtakið þetta skref fyrir alla aðra geymsluvíddarflokka.

## <a name="prepare-a-released-product-to-evaluate-purchase-trade-agreements-during-master-planning"></a>Undirbúa útgefna afurð til að meta innkaupasamninga við aðaláætlanagerð

Eftir að kerfið er undirbúið eins og lýst er í hlutanum á undan, ætti að fylgja þessum skrefum til að ganga úr skugga um að hver afurð sem á að nota með þessum eiginleika sé rétt sett upp.

1. Opnið **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir** og opnið viðmiðunarafurð.
1. Í flýtiflipanum **Innkaup** skal ganga úr skugga um að engum lánardrottni sé úthlutað í reitnum **Lánardrottinn**.
1. Á aðgerðasvæðinu, í flipanum **Áætlun**, í flokknum **Þekja**, skal velja **Vöruþekja** til að opna síðuna **Vöruþekja** fyrir valda afurð. Staðfestið eftirfarandi stillingar:

    - Í flipanum **Almennt** er hægt að setja upp hnekkingar lánardrottins. Ef fínstilling áætlanagerðar á að nota um innkaupasamninga til að velja lánardrottin ætti að koma í veg fyrir hnekkingu lánardrottins með því að hreinsa gátreitinn **Nota tiltekna stillingu**.
    - Í flipanum **Afhendingartími** er hægt að setja upp hnekkingar afhendingartíma. Ef ætlunin er að fínstilling áætlanagerðar noti innkaupasamninga til að velja afhendingartíma ætti að koma í veg fyrir hnekkingar afhendingartíma. Hreinsið gátreitinn fyrir hverja gerð afhendingartíma sem á að velja með því að nota innkaupasamninga (**Innkaup**, **Framleiðsla** og/eða **Flutningur**).

1. Lokið síðunni **Vöruþekja** til að fara aftur á upplýsingasíðuna fyrir valda afurð.
1. Á aðgerðasvæðinu, í flipanum **Áætlun**, í flokknum **Spá**, skal velja **Birgðaspá** til að opna síðuna **Birgðaspá**. Ganga skal úr skugga um að engin lína sem sýnd er hér hafi gildi í dálknum **Lánardrottnalykill**.
1. Lokið síðunni **Birgðaspá** til að fara aftur á upplýsingasíðuna fyrir valda afurð.
1. Á aðgerðasvæðinu, í flipanum **Innkaup**, í flokknum **Viðskiptasamningar**, skal smella á **Skoða viðskiptasamninga**. Gangið úr skugga um að viðeigandi innkaupasamningar komi fram. Gangið einnig úr skugga um að valkosturinn **Hunsa afhendingartíma** sé stilltur á **Nei** fyrir hvern samning þar sem þú vilt að fínstilling áætlanagerðar noti afhendingartímann sem tilgreindur er fyrir þann samning.
1. Á aðgerðasvæðinu, í flipanum **Áætlun**, í flokknum **Pöntunarstillingar**, skal velja **Sjálfgefnar pöntunarstillingar** til að opna síðuna **Sjálfgefnar pöntunarstillingar** fyrir valda afurð. Í flýtiflipanum **Innkaupapöntun** skal skoða gildið í reitnum **Afhendingartími innkaupa**. Ef engin hnekking á afhendingartíma vöru er skilgreind mun fínstilling áætlanagerðar nota þetta gildi þegar hún velur viðskiptasamninga þar sem valkosturinn **Hunsa afhendingartíma** er stilltur á **Já**. Þess vegna ætti að leiðrétta þetta gildi eftir því sem þörf krefur.
1. Endurtakið þetta ferli fyrir hverja viðeigandi afurð.

> [!NOTE]
> Fínstilling áætlanagerðar styður innkaupasamninga með mörgum gjaldmiðlum. Þegar leitað er að viðskiptasamningi með valkostinum **Lægsta einingaverð** mun kerfið taka til greina línur innkaupasamnings með mismunandi gjaldmiðlum svo lengi sem að gengi hafi verið skilgreint á milli gjaldmiðils viðskiptasamningslínu og bókhaldsgjaldmiðils lögaðilans. Annars verður litið framhjá viðskiptasamningslínunni og villa kemur fram við aðaláætlanagerð. Því mun aðaláætlanagerð innihalda upplýsingar frá öllum viðeigandi línum innkaupasamnings þar sem hægt verður að umreikna verðin í bókhaldsgjaldmiðilinn. Mikilvægt er að athuga að rúnareglur verða ekki teknar með við viðskiptasamninginn og línuverðsbreytingar.

## <a name="examples-of-how-planning-optimization-finds-vendor-and-lead-times"></a>Dæmi um hvernig fínstilling áætlanagerðar finnur lánardrottin og afhendingartíma

Eftirfarandi tafla inniheldur dæmi sem sýna hvernig ýmsar stillingar fyrir útgefna afurð og tengda innkaupasamninga hafa áhrif á gildin sem finnast fyrir innkaupatillöguna sem verður til. **Feitletruðu** gildin dálkunum tveimur lengst til hægri eru gildin sem valin eru af fínstillingu áætlanagerðar. **_Feitleitruðu og skáletruðu_** gildin í hinum dálkunum eru stillingarnar sem leiddu til þessara gilda fyrir hverja línu.

| Útgefin afurð: Lánardrottinn | Sjálfgefnar pöntunarstillingar: Afhendingartími | Vöruþekja: Hnekking lánardrottins | Vöruþekja: Hnekking afhendingartíma | Verðsamningur: Lánardrottinn | Verðsamningur: Afhendingartími | Verðsamningur: Hunsa afhendingartíma | Lánardrottinn sem verður til | Afhendingartíma sem verður til |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| ***US001** _ | _*_1_*_ | Nei | Nei | US003 | 3 | Nei | _ *US001** | **1** |
| US001 | 1 | ***Já: US002** _ | _*_Já: 2_*_ | US003 | 3 | Nei | _ *US002** | **2** |
| *(Autt)* | 1 | Nei | Nei | ***US003** _ | _*_3_*_ | Nei | _ *US003** | **3** |
| *(Autt)* | ***1** _ | Nei | Nei | _*_US003_*_ | 3 | Já | _ *US003** | **1** |
| *(Autt)* | ***1** _ | _*_Já: US002_*_ | Nei | US003 | 3 | Nei | _ *US002** | **1** |
| *(Autt)* | ***1** _ | _*_Já: US002_*_ | Nei | US003 | 3 | Nei | _ *US002** | **1** |
| *(Autt)* | 1 | Nei | Já: 2 | ***US003** _ | _*_3_*_ | Nei | _ *US003** | **3** |
| *(Autt)* | 1 | Nei | ***Já: 2** _ | _*_US003_*_ | 3 | Já | _ *US003** | **2** |

## <a name="additional-resources"></a>Frekari upplýsingar

[Innkaupasamningar](../../procurement/purchase-agreements.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
