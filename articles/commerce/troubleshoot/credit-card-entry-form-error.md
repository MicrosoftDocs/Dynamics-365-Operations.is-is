---
title: Síða fyrir innslátt kreditkorts sýnir villu í greiðsluferlinu
description: Þetta efnisatriði býður upp á leiðsögn úrræðaleitar sem getur reynst hjálpleg þegar greiðslumátahlutinn hleðst ekki og hann sýnir villuboð.
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
ms.openlocfilehash: f0751fc76e6eb4320f766886b4c1efcb1042e996
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585370"
---
# <a name="credit-card-entry-page-shows-an-error-at-checkout"></a><span data-ttu-id="f9022-103">Síða fyrir innslátt kreditkorts sýnir villu í greiðsluferlinu</span><span class="sxs-lookup"><span data-stu-id="f9022-103">Credit card entry page shows an error at checkout</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f9022-104">Þetta efnisatriði býður upp á leiðsögn úrræðaleitar sem getur reynst hjálpleg þegar hlutinn **Greiðslumáti** hleðst ekki og hann sýnir villuboð.</span><span class="sxs-lookup"><span data-stu-id="f9022-104">This topic provides troubleshooting guidance that can help when the **Payment method** section isn't loaded and shows an error message.</span></span>

## <a name="description"></a><span data-ttu-id="f9022-105">lýsing</span><span class="sxs-lookup"><span data-stu-id="f9022-105">Description</span></span>

<span data-ttu-id="f9022-106">Þegar greiðsluferlissíða netverslunar er opnuð hleðst hlutinn **Greiðslumáti** ekki og eftirfarandi villuboð koma upp: „Eitthvað fór úrskeiðis.</span><span class="sxs-lookup"><span data-stu-id="f9022-106">When you open the checkout page of an online store, the **Payment method** section isn't loaded, and the following error message is shown: "Something went wrong.</span></span> <span data-ttu-id="f9022-107">Reyna skal aftur síðar.</span><span class="sxs-lookup"><span data-stu-id="f9022-107">Please try again later."</span></span>

![Villa greiðslueiningar](media/payment-module-error.jpg)

## <a name="resolution"></a><span data-ttu-id="f9022-109">Upplausn</span><span class="sxs-lookup"><span data-stu-id="f9022-109">Resolution</span></span>

### <a name="wait-for-the-commerce-scale-unit-cache-to-expire"></a><span data-ttu-id="f9022-110">Bíða eftir því að skyndiminni Commerce Scale Unit renni út</span><span class="sxs-lookup"><span data-stu-id="f9022-110">Wait for the Commerce Scale Unit cache to expire</span></span>

<span data-ttu-id="f9022-111">Stillingar greiðsluþjónustunnar á greiðsluferlissíðu netverslunar eru vistaðar í skyndiminni á Commerce Scale Unit og geta tekið allt að 15 mínútur að birtast á svæði rafrænna viðskipta.</span><span class="sxs-lookup"><span data-stu-id="f9022-111">The payment service settings on the online store's checkout page are cached on the Commerce Scale Unit and can take up to 15 minutes to appear on the e-commerce site.</span></span> <span data-ttu-id="f9022-112">Þessar stillingar greiðsluþjónustunnar fela í sér breytingar á reikningskenni söluaðila, API-lykli í skýinu og ýmsar skilgreiningarstillingar sem tengjast greiðslumátanum.</span><span class="sxs-lookup"><span data-stu-id="f9022-112">These payment service settings include changes to the merchant account ID, cloud API key, and various configuration settings that are related to the payment method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f9022-113">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="f9022-113">Additional resources</span></span>

[<span data-ttu-id="f9022-114">Setja upp netrás</span><span class="sxs-lookup"><span data-stu-id="f9022-114">Set up an online channel</span></span>](../channel-setup-online.md)
