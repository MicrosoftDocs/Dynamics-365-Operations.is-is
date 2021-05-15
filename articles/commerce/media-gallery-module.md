---
title: Eining efnissafns
description: Þetta efnisatriði fjallar um einingar efnissafns og útskýrir hvernig á að bæta þeim við svæðissíður í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: de0bc650393b035adea4570c5e64ecb76283117e
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937387"
---
# <a name="media-gallery-module"></a>Eining efnissafns

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Þetta efnisatriði fjallar um einingar efnissafns og útskýrir hvernig á að bæta þeim við svæðissíður í Microsoft Dynamics 365 Commerce.

Einingar efnissafns sýna eina eða fleiri myndir í yfirliti efnissafns. Einingar efnissafns styðja smámyndir, sem hægt er að raða annaðhvort lárétt (sem röð fyrir neðan myndina) eða lóðrétt (sem dálk við hliðina á myndinni). Einingar efnissafns bjóða einnig upp á möguleika sem leyfa aðdrátt á myndum (stækka þær) eða skoða þær á heilum skjá. Til að mynd sjáist í einingu efnissafns, verður mynd að vera til staðar í miðlasafni Commerce-vefssmiðsins. Sem stendur styðja einingar efnissafns eingöngu myndir.

Í sjálfgefinni stillingu notar eining efnissafns afurðarkennið sem er til staðar í síðuinnihaldi fyrir upplýsingasíðu afurðar til að myndþýða samsvarandi myndir afurða. Í höfuðstöðvum Commerce verður að skilgreina slóð miðlaskráar fyrir allar afurðir. Myndum ætti síðan að hlaða upp í miðlasafni vefsmiðsins samkvæmt skráarslóðinni sem skilgreind var fyrir afurðir í höfuðstöðvum Commerce. Þessar myndir innihalda myndir afurða og allra afurðarafbrigða. Frekari upplýsingar um hvernig á að hlaða upp myndum í miðlasafni vefssmiðs er að finna í [Hlaða upp myndum](dam-upload-images.md).

Önnur leið er að eining efnissafns getur hýst sérvalið safn af myndum á síðu myndasafns sem ekki er háð afurðarkennum eða síðuinnihaldi. Í slíku tilfelli verður að hlaða upp myndum í miðlasafn vefssmiðs og tilgreindar í vefssmið.

Hér eru nokkur dæmi um notkun á einingum efnissafns:

- Myndþýðing afurðarmynda á upplýsingasíðu afurðar
- Myndþýðing afurðarmynda á markaðssíðu afurðar
- Sýna sérvalið safn af myndum á markaðssíðu, t.d. gallerísíðu

Í dæminu á eftirfarandi skýringarmynd, kaupgluggi á upplýsingasíðu afurðar hýsir afurðarmyndir með því að nota einingu efnissafns.

![Dæmi um kaupglugga á upplýsingasíðu afurðar sem hýsir afurðarmyndir með því að nota einingu efnissafns](./media/ecommerce-pdp-buybox.PNG)

## <a name="media-gallery-properties"></a>Eiginleikar efnissafns

| Nafn eiginleika | Gildi | lýsing |
|---------------|--------|-------------|
| Uppruni myndar | **Síðuinnihald** eða **Afurðarkenni** | Sjálfgefið gildi er **Síðuinnihald**. Ef **Síðuinnihald** er notað, gerir einingin ráð fyrir því að síðan útvegi upplýsingar um afurðarkennið. Ef **Afurðarkenni** er valið, verður að útvega afurðarkennið fyrir mynd sem gildið á eiginleikanum **Afurðarkenni**. Þessi möguleiki er í boði í Commerce, útgáfu 10.0.12. |
| Afurðarauðkenni | Auðkenni afurðar | Þessi eiginleiki á aðeins við ef gildið á eiginleikanum **Uppruni myndar** er **Afurðarkenni**. |
| Myndaaðdráttur | **Innfellt** eða **Hólf** | Þessi eiginleiki gerir notanda kleift að stækka myndir í einingu efnissafns. Hægt er að stækka myndir annaðhvort innan myndar eða í aðskildu hólfi við hliðina á myndinni. Þessi möguleiki er í boði í 10.0.12. |
| Aðdráttarstuðull | Tugatala | Þessi eiginleiki tilgreinir kvarðahlutfallið fyrir aðdrátt mynda. Til dæmis ef gildið er stillt á **2,5** eru myndir stækkaðar 2,5 sinnum. |
| Allur skjárinn | **Satt** eða **Ósatt** | Þessi eiginleiki tilgreinir hvort hægt er að skoða myndir á heilum skjá. Í heilskjásstillingu er einnig hægt að stækka myndir enn frekar ef kveikt er á aðdrættinum. Þessi möguleiki er í boði í Commerce-útgáfu 10.0.13. |
| Gæði mynda með aðdrætti | Tala frá 1 til 100 sem táknar prósentuhlutfall og sem er valið með því að nota stýringu sleðastiku | Þessi eiginleiki skilgreinir myndgæði fyrir myndir í aðdrætti. Hægt er að stilla hann á 100 prósent til að tryggja að stækkuð mynd noti alltaf hæstu mögulegu upplausn. Þessi eiginleiki á ekki við um PNG-skrár vegna þess að þær nota taplaust snið. Þessi möguleiki er í boði í Commerce-útgáfu 10.0.19. |
| Myndir | Myndir sem eru valdar úr miðlasafni vefsmiðs | Auk þess að vera myndþýddar frá afurð, er hægt að velja myndir fyrir einingu efnissafns. Þessum myndum verður bætt við allar afurðarmyndir sem eru í boði. Þessi möguleiki er í boði í Commerce, útgáfu 10.0.12. |
| Stefna smámynda | **Lóðrétt** eða **Lárétt** | Þessi eiginleiki tilgreinir hvort sýna eigi smámyndir í lóðréttri ræmu eða láréttri ræmu. |
| Fela sniðmátsmyndir afurðar fyrir afbrigði | **Satt** eða **Ósatt** | Ef þessi eiginleiki er stilltur á **Satt**, þegar afbrigði er valið, eru myndir aðalsniðmátsins faldar nema afbrigði sé ekki með neinar myndir. Þessi eiginleiki hefur ekki áhrif á afurðir sem eru ekki með nein afbrigði. |

Eftirfarandi mynd sýnir dæmi um einingu efnissafns þar sem boðið er upp á heilan skjá og aðdrátt.

![Dæmi um einingu efnissafns þar sem boðið er upp á heilan skjá og aðdrátt](./media/ecommerce-media-zoom.png)

Eftirfarandi skýringarmynd sýnir dæmi um einingu efnissafns sem er með sérvaldar myndir (þ.e. tilteknar myndir eru ekki háðar afurðarkenni eða síðuinnihaldi).

![Dæmi um einingu efnissafns sem er með sérvaldar myndir](./media/ecommerce-media-curated.PNG)

## <a name="commerce-scale-unit-interaction"></a>Samskipti við Commerce Scale Unit

Þegar uppruni myndar er fenginn frá síðuinnihaldinu, er afurðarkennið af upplýsingasíðu afurðar notað til að sækja myndirnar. Eining efnissafns sækir skráarslóð myndar fyrir afurðir með því að nota viðmót Commerce Scale Unit. Myndirnar eru síðan teknar úr miðlasafninu þannig að hægt sé að sýna þær í einingunni.

## <a name="add-a-media-gallery-module-to-a-page"></a>Bæta einingu efnissafns við síðu

Til að bæta einingu efnissafns við markaðssíðu skal fylgja þessum skrefum.

1. Farðu í **Sniðmát** og veldu **Nýtt** til að búa til nýtt sniðmát.
1. Í svarglugganum **Nýtt sniðmát**, undir **Heiti sniðmáts**, skal slá inn **Markaðssniðmát** og velja síðan **Í lagi**.
1. Í hólfinu **Meginmál**, skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.
1. Í glugganum **Bæta við einingu** skal velja eininguna **Sjálfgefin síða** og síðan velja **Í lagi**.
1. Í hólfinu **Aðalsvæði** á Sjálfgefin síða skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.
1. Í glugganum **Bæta við einingu** skal velja eininguna **Hólf** og síðan velja **Í lagi**.
1. Veldu **Vista**, síðan **Ljúka við breytingar** til að skila sniðmáti og veldu síðan **Birta** til að birta það.
1. Farðu í **Síður** og veldu **Ný** til að búa til nýja síðu.
1. Í svarglugganum **Velja sniðmát** skal velja sniðmátið **Markaðssniðmát**. Undir **Síðuheiti** skal færa inn **Síða efnissafns** og síðan velja **Í lagi**.
1. Í hólfinu **Aðalsvæði** á nýju síðunni skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.
1. Í glugganum **Bæta við einingu** skal velja eininguna **Hólf** og síðan velja **Í lagi**.
1. Í hólfinu **Hólf** skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.
1. Í glugganum **Bæta við einingu** skal velja eininguna **Efnissafn** og síðan velja **Í lagi**.
1. Á eiginleikasvæðinu fyrir einingu efnissafns, undir **Uppruni myndar**, skal velja **Afurðarkenni**. Því næst, í reitinn **Afurðarkenni**, skal færa inn auðkenni afurðar.
1. Veldu **Vista** og veldu síðan **Forskoðun** til að forskoða síðuna. Nú ættu myndirnar fyrir afurðirnar að sjást í yfirliti efnissafns.
1. Til að nota aðeins sérvaldar myndir, á eiginleikasvæðinu, undir **Uppruni myndar**, skal velja **Afurðarkenni**. Því næst, undir **Myndir**, skal velja **Bæta við mynd** eins oft og nauðsynlegt er til að bæta við myndum úr miðlasafninu.
1. Stillið alla aðra eiginleika sem á að stilla, svo sem **Aðdráttur myndar**, **Kvarði aðdráttar** og **Stefna smámynda**.
1. Þegar þessu er lokið skal velja **Vista**, síðan **Ljúka við breytingar** til að skila síðunni og velja síðan **Birta** til að birta hana.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit einingasafns](starter-kit-overview.md)

[Kaupgluggaeining](add-buy-box.md)

[Hólfeining](add-container-module.md)

[Hlaða upp myndum](dam-upload-images.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
