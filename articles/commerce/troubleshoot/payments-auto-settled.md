---
title: Greiðslur eru sjálfkrafa jafnaðar áður en pantanir eru reikningsfærðar eða sendar
description: Þessi grein veitir leiðbeiningar um bilanaleit sem geta hjálpað þegar greiðsla er gerð upp í Adyen gáttinni strax eftir pöntun, jafnvel þó að sölupöntunin hafi ekki verið reikningsfærð eða send.
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
ms.openlocfilehash: 6fdaf48600edc22b5423e0167177616758e2dc6e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282708"
---
# <a name="payments-are-automatically-settled-before-orders-are-invoiced-or-shipped"></a>Greiðslur eru sjálfkrafa jafnaðar áður en pantanir eru reikningsfærðar eða sendar

[!include [banner](../../includes/banner.md)]

Þessi grein veitir leiðbeiningar um bilanaleit sem geta hjálpað þegar greiðsla er gerð upp í Adyen gáttinni strax eftir pöntun, jafnvel þó að sölupöntunin hafi ekki verið reikningsfærð eða send.

## <a name="description"></a>lýsing

Þegar pöntun er gerð er greiðslan strax jöfnuð í Adyen-gáttinni jafnvel þótt sölupöntunin hafi ekki verið reikningsfærð eða send.

## <a name="resolution"></a>Upplausn

### <a name="configure-manual-capture-for-e-commerce-payments-in-the-adyen-portal"></a>Skilgreina handvirka úthlutun fyrir greiðslur rafrænna viðskipta í Adyen-gáttinni

Til að skilgreina handvirka úthlutun fyrir greiðslur rafrænna viðskipta í Adyen-gáttinni skal fylgja þessum skrefum.

1. Skráðu þig inn í Adyen gáttina.
1. Efst í hægra horninu skal velja söluaðilareikninginn fyrri rás rafrænna viðskipta.
1. Á efstu yfirlitsstikunni skal velja **Reikningur** og síðan **Stillingar**.
1. Í reitnum **Seinka úthlutun** skal velja **handvirkt**.

    ![Stilling fyrir Seinka úthlutun í Adyen-gáttinni.](media/adyen-capture-delay.jpg)

## <a name="additional-resources"></a>Frekari upplýsingar

[Úthlutun Adyen-greiðslu](https://docs.adyen.com/point-of-sale/capturing-payments)

[Dynamics 365 Payment Connector fyrir Adyen](../dev-itpro/adyen-connector.md)

[Setja upp Adyen-greiðslutengil fyrir Dynamics 365](https://docs.adyen.com/plugins/microsoft-dynamics)
