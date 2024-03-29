---
title: Villan Greiðslugerð verður að vera kreditkort á sölupöntunarsíðunni
description: Þessi grein veitir leiðbeiningar um bilanaleit sem geta hjálpað þegar villuboð eru sýnd á sölupöntunarsíðunni eftir að pöntun hefur verið samstillt.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: 71c5cbaf574866c74e222f4d67132004327db8fe
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285633"
---
# <a name="payment-type-must-be-credit-card-error-on-the-sales-order-page"></a>Villan „Greiðslugerð verður að vera kreditkort“ á sölupöntunarsíðunni

[!include [banner](../../includes/banner.md)]

Þessi grein veitir leiðbeiningar um bilanaleit sem geta hjálpað þegar villuboð eru sýnd á sölupöntunarsíðunni eftir að pöntun hefur verið samstillt.

## <a name="description"></a>lýsing

Þegar sölupöntunarsíðan er opnuð eftir að pöntun er samstillt koma upp eftirfarandi villuboð: „Greiðslugerðin verður að vera kreditkort þar sem númer kreditkorts hefur verið tilgreint.“

![Villan Greiðslugerðin verður að vera kreditkorta.](media/payment-type-must-be-credit-card.jpg)

## <a name="resolution"></a>Lausn

### <a name="set-the-payment-type-in-commerce-headquarters"></a>Stilla greiðslugerð í Commerce Headquarters

1. Farið í **Viðskiptakröfur \> Greiðsluuppsetning \> Greiðsluskilmálar**.
1. Í vinstri flettingunni skal velja greiðsluskilmálana.
1. Í reitnum **Greiðslugerð** skal ganga úr skugga um **Kreditkort** sé valið.

## <a name="additional-resources"></a>Frekari upplýsingar

[Bókun á netsölu og -greiðslum](../tasks/posting-online-sales-payments.md)
