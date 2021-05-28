---
title: Endurgreiðslu skilapöntunar er hafnað
description: Þetta efnisatriði býður upp á leiðsögn úrræðaleitar sem getur reynst hjálpleg þegar endurgreiðslu skilapöntunar er hafnað vegna þess að kreditkortið sem er notað fyrir reikningsfærslu er annað en kortið sem var notað í upphaflegri greiðsluheimild.
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
ms.openlocfilehash: 99fd4b816b1a3a1fe3c2d1579be45b43fdc3d385
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020757"
---
# <a name="refund-on-a-return-order-is-declined"></a><span data-ttu-id="2957e-103">Endurgreiðslu skilapöntunar er hafnað</span><span class="sxs-lookup"><span data-stu-id="2957e-103">Refund on a return order is declined</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2957e-104">Þetta efnisatriði býður upp á leiðsögn úrræðaleitar sem getur reynst hjálpleg þegar endurgreiðslu skilapöntunar er hafnað vegna þess að kreditkortið sem er notað fyrir reikningsfærslu er annað en kortið sem var notað í upphaflegri greiðsluheimild.</span><span class="sxs-lookup"><span data-stu-id="2957e-104">This topic provides troubleshooting guidance that can help when a refund on a return order is declined because the credit card that is used for invoicing differs from the card that was used during the original payment authorization.</span></span>

## <a name="description"></a><span data-ttu-id="2957e-105">lýsing</span><span class="sxs-lookup"><span data-stu-id="2957e-105">Description</span></span>

<span data-ttu-id="2957e-106">Endurgreiðslu er hafnað þegar kreditkortið sem er notað til að reikningsfæra skilapöntun er annað en kortið sem var notað í upphaflegri greiðsluheimild.</span><span class="sxs-lookup"><span data-stu-id="2957e-106">A refund is declined when the credit card that is used to invoice a return order differs from the card that was used during the original payment authorization.</span></span> <span data-ttu-id="2957e-107">Eftirfarandi villuboð koma upp: „Sumar greiðslur eru ekki með rétta stöðu fyrir bókun.</span><span class="sxs-lookup"><span data-stu-id="2957e-107">You receive the following error message: "Some payments are not in the correct status for posting.</span></span> <span data-ttu-id="2957e-108">Sannprófa skal stöðu allra greiðslna aftur áður en þær eru reikningsfærðar.“</span><span class="sxs-lookup"><span data-stu-id="2957e-108">Please re-validate the status of all payments prior to invoicing."</span></span>

<span data-ttu-id="2957e-109">Upplýsingar um greiðsluheimildina mun innihalda eftirfarandi villuboð: „Adyen gateway SendRequest() mistókst með stöðuna 'InternalServerError‘.22144; Auðu svari skilað úr Adyen.(22001);“</span><span class="sxs-lookup"><span data-stu-id="2957e-109">The payment authorization details will include the following error message: "Adyen gateway SendRequest() failed with status 'InternalServerError'.22144; Empty response returned from Adyen.(22001);"</span></span>

![Villa vegna hafnaðrar endurgreiðslu skilapöntunar](media/refund-order-decline.jpg)

## <a name="resolution"></a><span data-ttu-id="2957e-111">Upplausn</span><span class="sxs-lookup"><span data-stu-id="2957e-111">Resolution</span></span>

### <a name="enable-blind-returns-in-adyen"></a><span data-ttu-id="2957e-112">Virkja blind skil í Adyen</span><span class="sxs-lookup"><span data-stu-id="2957e-112">Enable blind returns in Adyen</span></span>

<span data-ttu-id="2957e-113">Til að virkja blind skil skal fylgja skrefunum í [Úrræðaleita Dynamics 365-greiðslutengil fyrir vandamál varðandi Adyen](adyen-support.md) til að hafa samband við notendaþjónustu Adyen og óska eftir að blind skil verði virkjuð á söluaðilareikningnum hjá Adyen.</span><span class="sxs-lookup"><span data-stu-id="2957e-113">To enable blind returns, follow the steps in [Troubleshoot Dynamics 365 Payment Connector for Adyen issues](adyen-support.md) to contact the Adyen support team and request that blind returns be enabled on your Adyen merchant account.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2957e-114">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="2957e-114">Additional resources</span></span>

[<span data-ttu-id="2957e-115">Dynamics 365-greiðslutengill fyrir Adyen</span><span class="sxs-lookup"><span data-stu-id="2957e-115">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="2957e-116">Setja upp Adyen-greiðslutengil fyrir Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="2957e-116">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)
