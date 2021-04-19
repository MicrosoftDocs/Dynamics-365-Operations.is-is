---
title: Endurgreiðslu skilapöntunar er hafnað
description: Þetta efnisatriði býður upp á leiðsögn úrræðaleitar sem getur reynst hjálpleg þegar endurgreiðslu skilapöntunar er hafnað vegna þess að kreditkortið sem er notað fyrir reikningsfærslu er annað en kortið sem var notað í upphaflegri greiðsluheimild.
author: Reza-Assadi
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
ms.openlocfilehash: 5961e77de1de5dc23454fc1a6e16f8c0b4e7cc6a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801556"
---
# <a name="refund-on-a-return-order-is-declined"></a>Endurgreiðslu skilapöntunar er hafnað

[!include [banner](../../includes/banner.md)]

Þetta efnisatriði býður upp á leiðsögn úrræðaleitar sem getur reynst hjálpleg þegar endurgreiðslu skilapöntunar er hafnað vegna þess að kreditkortið sem er notað fyrir reikningsfærslu er annað en kortið sem var notað í upphaflegri greiðsluheimild.

## <a name="description"></a>lýsing

Endurgreiðslu er hafnað þegar kreditkortið sem er notað til að reikningsfæra skilapöntun er annað en kortið sem var notað í upphaflegri greiðsluheimild. Eftirfarandi villuboð koma upp: „Sumar greiðslur eru ekki með rétta stöðu fyrir bókun. Sannprófa skal stöðu allra greiðslna aftur áður en þær eru reikningsfærðar.“

Upplýsingar um greiðsluheimildina mun innihalda eftirfarandi villuboð: „Adyen gateway SendRequest() mistókst með stöðuna 'InternalServerError‘.22144; Auðu svari skilað úr Adyen.(22001);“

![Villa vegna hafnaðrar endurgreiðslu skilapöntunar](media/refund-order-decline.jpg)

## <a name="resolution"></a>Upplausn

### <a name="enable-blind-returns-in-adyen"></a>Virkja blind skil í Adyen

Til að virkja blind skil skal fylgja skrefunum í [Úrræðaleita Dynamics 365-greiðslutengil fyrir vandamál varðandi Adyen](adyen-support.md) til að hafa samband við notendaþjónustu Adyen og óska eftir að blind skil verði virkjuð á söluaðilareikningnum hjá Adyen.

## <a name="additional-resources"></a>Frekari upplýsingar

[Dynamics 365-greiðslutengill fyrir Adyen](../dev-itpro/adyen-connector.md)

[Setja upp Adyen-greiðslutengil fyrir Dynamics 365](https://docs.adyen.com/plugins/microsoft-dynamics)
