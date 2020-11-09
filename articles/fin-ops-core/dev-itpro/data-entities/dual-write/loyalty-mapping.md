---
title: Vildarkort og vildarpunktar viðskiptavinar
description: Þetta efni lýsir samþættingu gagna um vildarkort viðskiptavina og verðlaunapunkta á milli forrita Finance and Operations og Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: 24ce08bb6cba9c74075151bafe0b07509fbdf73d
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "3998015"
---
# <a name="customer-loyalty-cards-and-reward-points"></a>Vildarkort og vildarpunktar viðskiptavinar

[!include [banner](../../includes/banner.md)]



Fyrirtæki flokka viðskiptavini og veita háþróaða þjónustu, byggð á innkaupum viðskiptavina og eyðslumynstri. Í Microsoft Dynamics 365 forritasvítunni hefur Dynamics 365 Commerce innviði og aðgerðir til að auðvelda og meðhöndla vildarkort viðskiptavina, verðlaunastig, verðmæti sem byggir á hollustu og umbun byggir á verslunarupplifun. Þegar gögn um vildarkort viðskiptavina og umbunarpunkta í viðskiptum eru samstillt við Common Data Service geta líkanadrifin forrit í Dynamics 365 notað þessi gögn. Til dæmis geta notendur Dynamics 365 Customer Service notað gögnin til að veita sömu háþróuðu þjónustu í gegnum þjónustuborðið.

## <a name="templates"></a>Sniðmát

| Finance and Operations-smáforrit | Líkanadrifin forrit í Dynamics 365 | lýsing |
|-----------------------------|-----------------------------------|-------------|
| Vildarkort                | msdyn\_loyaltycards               | Þetta sniðmát samstillir upplýsingar um vildarkort viðskiptavina. |
| Vildarpunktar       | msdyn\_loyaltyrewardpoints        | Þetta sniðmát samstillir upplýsingar um vildarpunkta viðskiptavina. |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]
