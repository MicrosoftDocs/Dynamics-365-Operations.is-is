---
title: Endurgreiðslu skilapöntunar er hafnað
description: Þetta efnisatriði býður upp á leiðsögn úrræðaleitar sem getur reynst hjálpleg þegar endurgreiðslu skilapöntunar er hafnað vegna þess að kreditkortið sem er notað fyrir reikningsfærslu er annað en kortið sem var notað í upphaflegri greiðsluheimild.
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
ms.openlocfilehash: e202c6b4b9e025d5af1cd5eb6235884aab6444e6
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585381"
---
# <a name="refund-on-a-return-order-is-declined"></a><span data-ttu-id="4393f-103">Endurgreiðslu skilapöntunar er hafnað</span><span class="sxs-lookup"><span data-stu-id="4393f-103">Refund on a return order is declined</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4393f-104">Þetta efnisatriði býður upp á leiðsögn úrræðaleitar sem getur reynst hjálpleg þegar endurgreiðslu skilapöntunar er hafnað vegna þess að kreditkortið sem er notað fyrir reikningsfærslu er annað en kortið sem var notað í upphaflegri greiðsluheimild.</span><span class="sxs-lookup"><span data-stu-id="4393f-104">This topic provides troubleshooting guidance that can help when a refund on a return order is declined because the credit card that is used for invoicing differs from the card that was used during the original payment authorization.</span></span>

## <a name="description"></a><span data-ttu-id="4393f-105">lýsing</span><span class="sxs-lookup"><span data-stu-id="4393f-105">Description</span></span>

<span data-ttu-id="4393f-106">Endurgreiðslu er hafnað þegar kreditkortið sem er notað til að reikningsfæra skilapöntun er annað en kortið sem var notað í upphaflegri greiðsluheimild.</span><span class="sxs-lookup"><span data-stu-id="4393f-106">A refund is declined when the credit card that is used to invoice a return order differs from the card that was used during the original payment authorization.</span></span> <span data-ttu-id="4393f-107">Eftirfarandi villuboð koma upp: „Sumar greiðslur eru ekki með rétta stöðu fyrir bókun.</span><span class="sxs-lookup"><span data-stu-id="4393f-107">You receive the following error message: "Some payments are not in the correct status for posting.</span></span> <span data-ttu-id="4393f-108">Sannprófa skal stöðu allra greiðslna aftur áður en þær eru reikningsfærðar.“</span><span class="sxs-lookup"><span data-stu-id="4393f-108">Please re-validate the status of all payments prior to invoicing."</span></span>

<span data-ttu-id="4393f-109">Upplýsingar um greiðsluheimildina mun innihalda eftirfarandi villuboð: „Adyen gateway SendRequest() mistókst með stöðuna 'InternalServerError‘.22144; Auðu svari skilað úr Adyen.(22001);“</span><span class="sxs-lookup"><span data-stu-id="4393f-109">The payment authorization details will include the following error message: "Adyen gateway SendRequest() failed with status 'InternalServerError'.22144; Empty response returned from Adyen.(22001);"</span></span>

![Villa vegna hafnaðrar endurgreiðslu skilapöntunar](media/refund-order-decline.jpg)

## <a name="resolution"></a><span data-ttu-id="4393f-111">Upplausn</span><span class="sxs-lookup"><span data-stu-id="4393f-111">Resolution</span></span>

### <a name="enable-blind-returns-in-adyen"></a><span data-ttu-id="4393f-112">Virkja blind skil í Adyen</span><span class="sxs-lookup"><span data-stu-id="4393f-112">Enable blind returns in Adyen</span></span>

<span data-ttu-id="4393f-113">Til að virkja blind skil skal fylgja skrefunum í [Úrræðaleita Dynamics 365-greiðslutengil fyrir vandamál varðandi Adyen](adyen-support.md) til að hafa samband við notendaþjónustu Adyen og óska eftir að blind skil verði virkjuð á söluaðilareikningnum hjá Adyen.</span><span class="sxs-lookup"><span data-stu-id="4393f-113">To enable blind returns, follow the steps in [Troubleshoot Dynamics 365 Payment Connector for Adyen issues](adyen-support.md) to contact the Adyen support team and request that blind returns be enabled on your Adyen merchant account.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4393f-114">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="4393f-114">Additional resources</span></span>

[<span data-ttu-id="4393f-115">Dynamics 365-greiðslutengill fyrir Adyen</span><span class="sxs-lookup"><span data-stu-id="4393f-115">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="4393f-116">Setja upp Adyen-greiðslutengil fyrir Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="4393f-116">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)
