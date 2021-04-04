---
title: Villan Greiðslugerð verður að vera kreditkort á sölupöntunarsíðunni
description: Þetta efnisatriði býður upp á leiðsögn úrræðaleitar sem getur reynst hjálpleg þegar villuboð koma upp í sölupöntunarsíðunni þegar búið er að samstilla pöntun.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: 20f18507dee330fd1affedeee092b3dfa7cc10bc
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585376"
---
# <a name="payment-type-must-be-credit-card-error-on-the-sales-order-page"></a>Villan „Greiðslugerð verður að vera kreditkort“ á sölupöntunarsíðunni

[!include [banner](../../includes/banner.md)]

Þetta efnisatriði býður upp á leiðsögn úrræðaleitar sem getur reynst hjálpleg þegar villuboð koma upp í sölupöntunarsíðunni þegar búið er að samstilla pöntun.

## <a name="description"></a>lýsing

Þegar sölupöntunarsíðan er opnuð eftir að pöntun er samstillt koma upp eftirfarandi villuboð: „Greiðslugerðin verður að vera kreditkort þar sem númer kreditkorts hefur verið tilgreint.“

![Villan Greiðslugerð verður að vera kreditkort](media/payment-type-must-be-credit-card.jpg)

## <a name="resolution"></a>Upplausn

### <a name="set-the-payment-type-in-commerce-headquarters"></a>Stilla greiðslugerð í Commerce Headquarters

1. Farið í **Viðskiptakröfur \> Greiðsluuppsetning \> Greiðsluskilmálar**.
1. Í vinstri flettingunni skal velja greiðsluskilmálana.
1. Í reitnum **Greiðslugerð** skal ganga úr skugga um **Kreditkort** sé valið.

## <a name="additional-resources"></a>Frekari upplýsingar

[Bókun á netsölu og -greiðslum](../tasks/posting-online-sales-payments.md)
