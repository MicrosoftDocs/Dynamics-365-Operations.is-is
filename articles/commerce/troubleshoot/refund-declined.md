---
title: Endurgreiðslu skilapöntunar er hafnað
description: Þessi grein veitir leiðbeiningar um bilanaleit sem geta hjálpað þegar endurgreiðslu á skilapöntun er hafnað vegna þess að kreditkortið sem er notað við reikningagerð er frábrugðið því kortinu sem var notað við upphaflega greiðsluheimildina.
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
ms.openlocfilehash: d8d1c40673d4b159a7b7bf00bf6011ba45f47edd
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268233"
---
# <a name="refund-on-a-return-order-is-declined"></a>Endurgreiðslu skilapöntunar er hafnað

[!include [banner](../../includes/banner.md)]

Þessi grein veitir leiðbeiningar um bilanaleit sem geta hjálpað þegar endurgreiðslu á skilapöntun er hafnað vegna þess að kreditkortið sem er notað við reikningagerð er frábrugðið því kortinu sem var notað við upphaflega greiðsluheimildina.

## <a name="description"></a>lýsing

Endurgreiðslu er hafnað þegar kreditkortið sem er notað til að reikningsfæra skilapöntun er annað en kortið sem var notað í upphaflegri greiðsluheimild. Eftirfarandi villuboð koma upp: „Sumar greiðslur eru ekki með rétta stöðu fyrir bókun. Sannprófa skal stöðu allra greiðslna aftur áður en þær eru reikningsfærðar.“

Upplýsingar um greiðsluheimildina mun innihalda eftirfarandi villuboð: „Adyen gateway SendRequest() mistókst með stöðuna 'InternalServerError‘.22144; Auðu svari skilað úr Adyen.(22001);“

![Villa vegna hafnaðrar endurgreiðslu skilapöntunar.](media/refund-order-decline.jpg)

## <a name="resolution"></a>Lausn

### <a name="enable-blind-returns-in-adyen"></a>Virkja blind skil í Adyen

Til að virkja blind skil skal fylgja skrefunum í [Úrræðaleita Dynamics 365-greiðslutengil fyrir vandamál varðandi Adyen](adyen-support.md) til að hafa samband við notendaþjónustu Adyen og óska eftir að blind skil verði virkjuð á söluaðilareikningnum hjá Adyen.

## <a name="additional-resources"></a>Frekari upplýsingar

[Dynamics 365-greiðslutengill fyrir Adyen](../dev-itpro/adyen-connector.md)

[Setja upp Adyen-greiðslutengil fyrir Dynamics 365](https://docs.adyen.com/plugins/microsoft-dynamics)
