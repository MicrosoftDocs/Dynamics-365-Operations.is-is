---
title: Greiðslur eru sjálfkrafa jafnaðar áður en pantanir eru reikningsfærðar eða sendar
description: Þetta efnisatriði býður upp á leiðsögn úrræðaleitar sem getur reynst hjálpleg þegar greiðsla er jöfnuð í Adyen-gátt strax og pöntun er gerð, jafnvel þótt sölupöntunin hafi ekki verið reikningsfærð eða send.
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
ms.openlocfilehash: b4fd37a3c45f2559c9659f072ca0b6f02e712f53
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018261"
---
# <a name="payments-are-automatically-settled-before-orders-are-invoiced-or-shipped"></a>Greiðslur eru sjálfkrafa jafnaðar áður en pantanir eru reikningsfærðar eða sendar

[!include [banner](../../includes/banner.md)]

Þetta efnisatriði býður upp á leiðsögn úrræðaleitar sem getur reynst hjálpleg þegar greiðsla er jöfnuð í Adyen-gátt strax og pöntun er gerð, jafnvel þótt sölupöntunin hafi ekki verið reikningsfærð eða send.

## <a name="description"></a>lýsing

Þegar pöntun er gerð er greiðslan strax jöfnuð í Adyen-gáttinni jafnvel þótt sölupöntunin hafi ekki verið reikningsfærð eða send.

## <a name="resolution"></a>Upplausn

### <a name="configure-manual-capture-for-e-commerce-payments-in-the-adyen-portal"></a>Skilgreina handvirka úthlutun fyrir greiðslur rafrænna viðskipta í Adyen-gáttinni

Til að skilgreina handvirka úthlutun fyrir greiðslur rafrænna viðskipta í Adyen-gáttinni skal fylgja þessum skrefum.

1. Skráðu þig inn í Adyen gáttina.
1. Efst í hægra horninu skal velja söluaðilareikninginn fyrri rás rafrænna viðskipta.
1. Á efstu yfirlitsstikunni skal velja **Reikningur** og síðan **Stillingar**.
1. Í reitnum **Seinka úthlutun** skal velja **handvirkt**.

    ![Stilling Seinka úthlutun í Adyen-gáttinni](media/adyen-capture-delay.jpg)

## <a name="additional-resources"></a>Frekari upplýsingar

[Úthlutun Adyen-greiðslu](https://docs.adyen.com/point-of-sale/capturing-payments)

[Dynamics 365-greiðslutengill fyrir Adyen](../dev-itpro/adyen-connector.md)

[Setja upp Adyen-greiðslutengil fyrir Dynamics 365](https://docs.adyen.com/plugins/microsoft-dynamics)
