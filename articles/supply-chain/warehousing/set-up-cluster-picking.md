---
title: Setja upp klasatiltekt
description: Í þessari grein er því lýst hvernig á að setja upp klasatiltekt og hvernig á að nota vörustaðfestingu með klasatiltekt.
author: Mirzaab
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSClusterProfile, WHSRFAutoConfirm, WHSWorkCluster
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0ec3de073def2ff63af3c04b5696cbcec4f09948
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/15/2022
ms.locfileid: "9014721"
---
# <a name="set-up-cluster-picking"></a>Setja upp klasatiltekt

[!include[banner](../includes/banner.md)]

Þessi grein lýsir því hvernig virkja má starfsmenn til að nota fartæki sín við tiltekt í klasa, þannig að þeir geti tekið vörur frá einum stað fyrir margar vinnupantanir á sama tíma. Þetta er kallað *klasatínslu*.

## <a name="about-cluster-picking"></a>Um klasatiltekt

Eftir að verkpantanir eru gefnar út á vöruhús getur starfsmaður notað farsímann til að úthluta pöntunum í klasa. Klasa verður að skipuleggja tiltektarvinnu fyrir starfsmann. Vinna pöntun er tengdur við klasa, starfsmaður verður að nota klasa tiltektarlista til að framkvæma vinnu við tiltekt pöntunarinnar. Starfsmaðurinn getur ekki notað annarri tiltektaraðferð. Ef vinnu pöntun er úthlutað á klasa mistök, verður starfsmaðurinn skipta klasanum sem og síðan búðu það aftur.

Ef þörf krefur, getur starfsmaður látið klasa ganga til annan starfsmann. Þetta breytir stöðunni í klasa Skilað. Þegar starfsmaður notar fartæki til að tilgreina að lokið er við tiltektar- og frágangsvinnu, verður að staðfesta sendinguna eða farminn í biðlara.

## <a name="enable-cluster-picking"></a>Virkja klasatiltekt

Til að virkja klasatínslu, verður að setja upp eftirfarandi:

- **Klasaforstillingar** - Tilgreindu hvort á að sjálfkrafa búa til auðkenni klasa, fjölda stöðugilda til að nota, hvenær á að brjóta upp klasa, og hvernig á að raða og staðfesta tiltekt.

- **Vinnusniðmát** - Tilgreindu hvernig á að búa til tiltekt fyrir klasatiltekt.

- **Staðsetningarleiðbeiningar** - Tilgreindu hvar á að taka til vörur og hvar á að setja þær.

- **Valmyndaratriði fartækis** - Stilla valmyndaratriði fartækis til að nota fyrirliggjandi verk sem er stjórnað af klasatiltekt. Þú verður að bæta valmyndaratriði valmynd fartækis þannig að það birtist í fartækjum.

- **Færibreytur vöruhúsakerfis** - Tilgreindu talnarunu til að nota ef þú vilt búa til auðkenni fyrir klasa.

## <a name="set-up-a-cluster-profile"></a>Setja upp klasaforstillingu

Til að setja upp forstillingu sem klasa, skal fylgja þessum skrefum:

1. Smelltu á **Vöruhúsakerfi** \> **Uppsetning** \> **Fartæki** \> **Klasaforstillingar**.

1. Smelltu á **Nýtt** til að stofna nýja forstillingu.

1. Smelltu á **Stofna klasa** og, undir **Klasaröðun**, skal smella á **Nýtt** til að setja upp röðunarforsendur fyrir klasann. Röðunarforsendur að stýra röðinni sem starfsmaðurinn mun framkvæma tiltekt vinnu. Hægt er að bæta við eins mörgum skilyrðum og þarf.

1. Í reitnum **Númeraröð** skal slá inn númer til að skilgreina röðina sem unnið er úr röðunarforsendum.

1. Í reitnum **Reitarheiti** velurðu reitinn sem mun ákvarða flokkun. Til dæmis, ef þú velur **WMSLocationId** svæðinu vinnu verður raðað eftir staðsetningu.

1. Í reitnum **Röðun** skal velja einn af eftirfarandi valkostum.

| **Valkostur**     | **Lýsing**                                                                                                                                                                                                                    |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Hækkandi**  | Tiltektarvinnu er raðað í hækkandi röð samkvæmt röðunarforsendunni. Til dæmis, ef nota á **WMSLocationId** eru svæði sem á að raða skilyrðum og Kenni skal staðsetningu 1, 2, 3 og 4, er verður að taka frá staðsetningu 4 fyrst. |
| **Í lækkandi röð** | Tiltektarvinnu er raðað í lækkandi röð samkvæmt röðunarforsendunni. Til dæmis, ef nota á **WMSLocationId** eru svæði sem á að raða skilyrðum og Kenni skal staðsetningu 1, 2, 3 og 4, er verður að taka frá staðsetningu 1 fyrst. |

## <a name="item-confirmation"></a>Vörustaðfesting

Þegar klasatiltekt er notuð, er vörustaðfesting nauðsynleg svo hægt sé að staðfesta þær vörur sem bætt er við klasa. Hægt er að staðfesta vörur í klasatiltekt á meðan klasatiltekt stendur yfir. Uppsetning byggist á strikamerkjauppsetningu vöru.

### <a name="set-up-item-verification-with-cluster-picking"></a>Setja upp vörustaðfestingu með klasatiltekt

1. Farðu í **Vöruhúsastjórnun**  >  **Uppsetning**  >  **Fartæki**  >  **Valmyndaratriði fartækis**.
1. Á listasvæðinu skaltu velja valmyndaratriðið sem þú vilt setja upp.
1. Á aðgerðasvæðinu skal velja **Uppsetning vinnustaðfestingar**.
1. Gerðu svo eitt af eftirfarandi:
    - Ef nú þegar er til lína fyrir **Vinnugerð** sem á að setja upp skal velja hana og síðan velja **Breyta** á aðgerðasvæðinu.
    - Ef viðeigandi lína er ekki til skaltu velja **Nýtt** á Aðgerðasvæði og stilla síðan **Vinnutegund** á viðeigandi tegund.
1. Merktu gátreitinn **Staðfesting afurðar** fyrir nýja eða valda línu. Þetta gerir starfsmönnum kleift að staðfesta allar birgðir með fartækinu.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]