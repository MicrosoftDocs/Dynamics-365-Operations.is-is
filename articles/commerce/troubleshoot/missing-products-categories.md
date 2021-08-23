---
title: Vantar afurðir og flokka eftir afritun umhverfis
description: Þetta efnisatriði býður upp á leiðsögn úrræðaleitar sem getur reynst hjálpleg þegar afurðir og flokka vantar eftir að svæði er afritað milli umhverfa eða innan sama umhverfis.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 813289db052323fd87cd5a65184d71a580f1a3e0df9ea7d50a752e26b3962d1c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6763621"
---
# <a name="products-and-categories-missing-after-environment-copy"></a>Afurðir og flokka vantar eftir afritun umhverfis

[!include [banner](../../includes/banner.md)]

Þetta efnisatriði býður upp á leiðsögn úrræðaleitar sem getur reynst hjálpleg þegar afurðir og flokka vantar eftir að svæði er afritað milli umhverfa eða innan sama umhverfis.

## <a name="description"></a>lýsing

Þegar svæði er afritað úr einu umhverfi í annað, eða innan sama umhverfis, vantar afurðir og flokka úr svæðinu. Afurðirnar og flokkana vantar úr netverslun rafrænna viðskipta og úr flipanum **Afurðir** í vefsmið Commerce.

## <a name="resolution"></a>Upplausn

### <a name="map-the-channel-operating-unit-number-to-a-newly-copied-site-in-commerce-site-builder"></a>Varpa rásarnúmeri rekstrareiningar í nýlega afritað svæði í vefsmið Commerce

Til að varpa rásarnúmeri rekstrareiningar í nýlega afritað svæði í vefsmið Commerce skal fylgja þessum skrefum.

1. Veljið nýlega afritað svæði.
1. Undir **Svæðisstillingar** skal velja **Rásir**.
1. Við hliðina á heiti rásarinnar skal velja úrfellingarmerkið (**...**) og síðan velja **Breyta netverslunarrás**.
1. Í svarglugganum **Breyta netverslunarrás** skal velja rásina til að varpa í nýlega afritað svæði og síðan velja **Í lagi**.
1. Veljið **Vista og birta**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Tengja svæði Dynamics 365 Commerce við netrás](../associate-site-online-store.md)
