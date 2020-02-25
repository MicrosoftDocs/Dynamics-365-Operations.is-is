---
title: Lánaflokkar viðskiptavina
description: Í þessu efnisatriði er að finna upplýsingar um kredithópa viðskiptavinar.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: f7121b78f3318bae9f82b2f0f951bc7bfe6c4358
ms.sourcegitcommit: 6a70f9ac296158edd065d52a12703b3ce85ce5ee
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/03/2020
ms.locfileid: "3015266"
---
# <a name="customer-credit-groups"></a><span data-ttu-id="fef35-103">Lánaflokkar viðskiptavina</span><span class="sxs-lookup"><span data-stu-id="fef35-103">Customer credit groups</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="fef35-104">Þú getur skilgreint hópa viðskiptavina sem hafa sama lánsheimild.</span><span class="sxs-lookup"><span data-stu-id="fef35-104">You can define groups of customers who have the same credit limit.</span></span> <span data-ttu-id="fef35-105">Einnig er tekið tillit til einstakra lánamarka sem eru skilgreind á reikningslykli viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="fef35-105">The individual credit limit that is defined on the customer invoice account is also considered.</span></span>

<span data-ttu-id="fef35-106">Hægt er að velja meðlimi í kredithóp viðskiptavina úr mismunandi lögaðilum.</span><span class="sxs-lookup"><span data-stu-id="fef35-106">Members of a customer credit group can be selected from different legal entities.</span></span> <span data-ttu-id="fef35-107">Þegar þú bætir viðskiptavin við lista yfir viðskiptavini í viðskiptavinahópnum, er lokadegi lánamarka fyrir hvern viðskiptavin breytt í lokadag sem úthlutað er til hópsins.</span><span class="sxs-lookup"><span data-stu-id="fef35-107">When you add a customer to the list of customers in the customer credit group, the expiration date of the credit limit for each customer is changed to the expiration date that is assigned to the group.</span></span>

<span data-ttu-id="fef35-108">Þú getur sett upp lánshópa viðskiptavina á síðunni **Lánshópar viðskiptavina** (**Lánastjórnun \> Lánshópar viðskiptavina \> Lánshópar viðskiptavina**).</span><span class="sxs-lookup"><span data-stu-id="fef35-108">You can set up customer credit groups on the **Customer credit groups** page (**Credit management \> Customer credit groups \> Customer credit groups**).</span></span>

1. <span data-ttu-id="fef35-109">Í reitinn **Hópnúmer** og **Lýsing** slærðu inn kennimerki og lýsingu fyrir hópinn.</span><span class="sxs-lookup"><span data-stu-id="fef35-109">In the **Group number** and **Description** fields, enter an identifier and description for the group.</span></span>
2. <span data-ttu-id="fef35-110">Í reitunum **Lánamörk** og **Gjaldmiðill** slærðu inn lánamörk og gjaldmiðil sem ætti að nota þegar kerfið skoðar lánamörk fyrir einhvern meðlim í flokknum.</span><span class="sxs-lookup"><span data-stu-id="fef35-110">In the **Credit limit** and **Currency** fields, enter the credit limit and currency that should be used when the system checks the credit limit for any member of the group.</span></span>
3. <span data-ttu-id="fef35-111">Í reitinn **Lánamörk hingað til** slærðu inn dagsetningu þegar lánsfjárhámarkið rennur út.</span><span class="sxs-lookup"><span data-stu-id="fef35-111">In the **Credit limit to date** field, enter the date when the credit limit expires.</span></span> <span data-ttu-id="fef35-112">Lánshópar viðskiptavina verða að hafa lokadag.</span><span class="sxs-lookup"><span data-stu-id="fef35-112">Customer credit groups must have an expiration date.</span></span>

<span data-ttu-id="fef35-113">Eftir að þú hefur lokið við að setja upp viðskiptahóp fyrir lánsfé geturðu bætt viðskiptavinum við hann með því að tilgreina lögaðila þeirra og auðkenni viðskiptavinarreiknings.</span><span class="sxs-lookup"><span data-stu-id="fef35-113">After you've finished setting up a customer credit group, you can add customers to it by specifying their legal entity and customer account ID.</span></span> <span data-ttu-id="fef35-114">Þegar þú bætir nýjum viðskiptavini við viðskiptavinahóp, leitar kerfið að sama viðskiptavinareikningi yfir alla lögaðila og biður þig um að bæta honum við viðskiptahópinn.</span><span class="sxs-lookup"><span data-stu-id="fef35-114">When you add a new customer to a customer credit group, the system searches for the same customer account across all legal entities and prompts you to add it to the customer credit group.</span></span>

<span data-ttu-id="fef35-115">Notaðu valmyndina **Aldursgreindar stöður** til að skoða upplýsingar um aldursgreinda stöðu fyrir alla reikningviðskiptavini í kredithóp viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="fef35-115">Use the **Aged balances** menu to view the details of the aging balance for all invoice customers in a customer credit group.</span></span> <span data-ttu-id="fef35-116">Síðan **Aldursgreind staða** sýnir yfirlit yfir aldursgreiningar fyrir reikninga viðskiptavinarreikninga.</span><span class="sxs-lookup"><span data-stu-id="fef35-116">The **Aging balance** page shows a summary of the aged balances for the invoice customer accounts.</span></span>
