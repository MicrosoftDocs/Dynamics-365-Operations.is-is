---
title: Vinna með uppskrift fyrir afbrigðalíkan afurðar
description: Keyra þetta ferli krefst fyrirliggjandi skilgreiningu afbrigðalíkan afurðar.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCBOMLineDetails, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd78b06f10d0c9b1df57dacdd824b06ebe414b3b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577289"
---
# <a name="maintain-bom-for-a-product-configuration-model"></a>Vinna með uppskrift fyrir afbrigðalíkan afurðar

[!include [banner](../../includes/banner.md)]

Keyra þetta ferli krefst fyrirliggjandi skilgreiningu afbrigðalíkan afurðar. Hágæða hátalara líkan í fyrirtækinu sýnigögn USMF er notað til að stofna þetta ferli.

## <a name="add-a-bom-line"></a>Bæta við uppskriftarlína

1. Farið í **Afurðarupplýsingastjórnun \> Afurðir \> Afbrigðalíkön afurða**.
1. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Veljið hágæða hátalara fyrir þetta ferli.  
1. Í listanum skal velja tengilinn í valinni línu.
1. Stækka hlutann **Uppskriftarlínur**.
1. Veljið **Bæta við**.
1. Í reitinn **Heiti** skal slá inn gildi.
1. Í reitinn **Lýsing** skal slá inn gildi.
1. Veljið **Vista**.

## <a name="add-bom-line-details"></a>Bæta við uppskriftarlínuupplýsingar

1. Veljið **Upplýsingar um uppskriftarlínu**.
2. Í reitinn **Vörunúmer** skal slá inn eða velja gildi.
    * Til dæmis er hægt að velja M0055 vöru.  
    * Fyrir hvern línueiginleika Uppskriftar, er hægt að velja hvort hún tekur fast gildi eða er varpað á eigind.  
3. Veljið gátreitinn **Stilla**.
4. Velja skal *Já* í reitnum **Útreikningur**.
    * Ef **Útreikningur** eiginleikinn er stilltur á *Já* er uppskriftarlínunni tekin með í útreikningi kostnaðar.  
5. Veljið flipann **Uppsetning**.
6. Veljið gátreitinn **Stilla**.
7. Í reitnum **Magn** slærðu inn tölu.
    * Magn svæðið ákvarðar hversu mikið vörunnar sem verða innifalin í Uppskriftinni. Þetta gæti verið að augljós umsækjanda fyrir eigindarvörpun.  
8. Veljið flipann **Vídd**.
    * Staðfesta ef einhver afurðarvíddum eru virk og þess vegna verður að hafa gildi eða eigind sem er úthlutað.  
9. Veljið **Í lagi**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]