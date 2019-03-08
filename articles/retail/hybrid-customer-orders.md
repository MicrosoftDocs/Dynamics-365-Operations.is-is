---
title: Fjölpantanir viðskiptavinar
description: Fjölpöntun viðskiptavinar er stök pöntun, sem inniheldur vörur sem viðskiptavinur getur haft með sér úr verslun, sem og vörur sem verða sóttar eða sendar síðar.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 261164
ms.assetid: 9d99a5b9-4662-499a-bece-3ea1d6092934
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a00e69a589ffe744f88edb6a8b3709c4029fc1ec
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "364328"
---
# <a name="hybrid-customer-orders"></a><span data-ttu-id="c9fbd-103">Fjölpantanir viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="c9fbd-103">Hybrid customer orders</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c9fbd-104">Fjölpöntun viðskiptavinar er stök pöntun, sem inniheldur vörur sem viðskiptavinur getur haft með sér úr verslun, sem og vörur sem verða sóttar eða sendar síðar.</span><span class="sxs-lookup"><span data-stu-id="c9fbd-104">A hybrid customer order is a single order, which contains products that can be carried out of the store by the customer, as well as products that will be picked up or shipped later.</span></span>

<span data-ttu-id="c9fbd-105">Í Microsoft Dynamics 365 for Retail, geturðu annað hvort valið að fara út með allar vörur eða fara út með valdar vörur fyrir pöntun viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="c9fbd-105">In Microsoft Dynamics 365 for Retail, you can select either carry out all products or carry out selected products for a customer order.</span></span> <span data-ttu-id="c9fbd-106">Vörulínur sem eru merktar sem fara með út eru reikningsfærðar sjálfkrafa eftir að pöntun er stofnuð, það sama er gert fyrir pöntun sem á að sækja eftir að pöntun er stofnuð.</span><span class="sxs-lookup"><span data-stu-id="c9fbd-106">The product lines that are marked as carry out are automatically invoiced after the order is created, similarly this is the same for an order that is to be picked-up after the order is created.</span></span> <span data-ttu-id="c9fbd-107">Upphæð til greiðslu fyrir fjölpöntun er ákvörðuð með því að bæta prósentu innborgunar á sækja og senda vörulínum við heildarupphæð lína sem á að fara með út.</span><span class="sxs-lookup"><span data-stu-id="c9fbd-107">The amount due on hybrid orders is determined by adding the deposit percentage on pick and ship product lines with the full amount of the carry out lines.</span></span> <span data-ttu-id="c9fbd-108">Fyrir fjölpantanir skiptir kerfið á milli stillingar fyrir pöntun viðskiptavinar og stillingar fyrir staðgreitt fyrir afhendingu sem hér segir:</span><span class="sxs-lookup"><span data-stu-id="c9fbd-108">For hybrid orders, the system switches between customer order mode and cash and carry mode as follows:</span></span>

- <span data-ttu-id="c9fbd-109">Ef allar vörur í körfu eru stilltar á **Framkvæma afhending**, verður pöntun afgreidd sem Staðgreitt við afhendingu.</span><span class="sxs-lookup"><span data-stu-id="c9fbd-109">If all products in the cart are set to **Carry out delivery**, the order will be handled as a Cash and Carry transaction.</span></span>
- <span data-ttu-id="c9fbd-110">Ef allar vörur í karfa eru stilltar á annað hvort **Taka til** eða **senda afhendingu**,, verður pöntun afgreidd sem færsla á pöntun viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="c9fbd-110">If any or all lines in the cart are set to either **Pick** or **ship delivery**, the order will be handled as a Customer order transaction.</span></span>

<span data-ttu-id="c9fbd-111">Ef körfulína er valin og **Taka til er valið**, **Senda er valið**, eða **Framkvæma er valið** er valið verðu aðeins tilgreind körfulína stillt á þá afhendingaraðferð.</span><span class="sxs-lookup"><span data-stu-id="c9fbd-111">If a cart line is selected and **Pick selected**, **Ship selected**, or **Carry out selected** is selected, only the specific cart line is set with that delivery method.</span></span> <span data-ttu-id="c9fbd-112">Í því tilviki heldur niðurflæði aðgerðarinnar áfram eins og venjulega.</span><span class="sxs-lookup"><span data-stu-id="c9fbd-112">In that case, the downstream flow of the operation continues as usual.</span></span> <span data-ttu-id="c9fbd-113">Ef hins vegar **Taka til valinn**, **Afgreiða Valið: ,**, eða **Framkvæma Valið: ,** er Valið án þess að körfulína sé valin opnast ný síða með lista yfir allar körfulínur.</span><span class="sxs-lookup"><span data-stu-id="c9fbd-113">However, if **Pick selected**, **Ship selected**, or **Carry out selected** is selected without a cart line being selected, a new page opens that lists all the cart lines.</span></span> <span data-ttu-id="c9fbd-114">Á þeirri skjámynd er hægt að velja margar línur samtímis til að stilla afhendingaraðferð.</span><span class="sxs-lookup"><span data-stu-id="c9fbd-114">On that screen, you can select multiple lines at once for setting the delivery method.</span></span> <span data-ttu-id="c9fbd-115">Þegar þú notar þá aðferð fyrir línuval verða allar fyrri afhendingaraðferðir sem hefur verið úthlutað á línuna hnekkt.</span><span class="sxs-lookup"><span data-stu-id="c9fbd-115">When you use that method for selecting lines, any previous delivery method that has been assigned to the line will be overridden.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c9fbd-116">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="c9fbd-116">Additional resources</span></span>

[<span data-ttu-id="c9fbd-117">Yfirlit pantana viðskiptavina</span><span class="sxs-lookup"><span data-stu-id="c9fbd-117">Customer orders overview</span></span>](customer-orders-overview.md)
