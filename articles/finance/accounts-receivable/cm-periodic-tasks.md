---
title: Regluleg verk kreditstjórnunar
description: Þetta efni lýsir reglubundnum verkefnum sem eru nauðsynlegur hluti af ferlinu við að stjórna lánamörkum fyrir viðskiptavini.
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
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 17b4b2f487fdeb9f1aa7d77bf87197885ba60e47
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4444344"
---
# <a name="periodic-credit-management-tasks"></a><span data-ttu-id="3f88d-103">Reglubundin verk lánastýringar</span><span class="sxs-lookup"><span data-stu-id="3f88d-103">Periodic credit management tasks</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3f88d-104">Þetta efni lýsir reglubundnum verkefnum sem eru nauðsynlegur hluti af ferlinu við að stjórna lánamörkum fyrir viðskiptavini.</span><span class="sxs-lookup"><span data-stu-id="3f88d-104">This topic describes the periodic tasks that are a necessary part of the process of managing credit limits for customers.</span></span>

## <a name="update-risk-scores"></a><span data-ttu-id="3f88d-105">Uppfæra áhættueinkunnir</span><span class="sxs-lookup"><span data-stu-id="3f88d-105">Update risk scores</span></span>

<span data-ttu-id="3f88d-106">Þegar fyrirtæki þróast og aðstæður breytast getur útlánaáhætta tiltekins viðskiptavinar einnig breyst.</span><span class="sxs-lookup"><span data-stu-id="3f88d-106">As businesses evolve and circumstances change, the credit risks for a given customer can also change.</span></span> <span data-ttu-id="3f88d-107">Til að hjálpa við að viðhalda viðeigandi lánamörkum fyrir viðskiptavini þína, verður þú að fara reglulega yfir viðmið fyrir hvert áhættustig og uppfæra skora fyrir hvern viðskiptavin.</span><span class="sxs-lookup"><span data-stu-id="3f88d-107">To help maintain appropriate credit limits for your customers, you must periodically review the criteria for each risk score and update the scores for each customer.</span></span> <span data-ttu-id="3f88d-108">Þú getur uppfært eftirfarandi stig með því að nota síðuna **Uppfæra áhættumat** (**Skuldir og innheimta \> Reglubundin verk \> Lánastjórnun \> Uppfæra áhættumat**).</span><span class="sxs-lookup"><span data-stu-id="3f88d-108">You can update the following scores by using the **Update risk scores** page (**Credit and collections \> Periodic tasks \> Credit management \> Update risk scores**).</span></span> <span data-ttu-id="3f88d-109">Allir notendaskilgreindir útreikningar eru einnig unnir.</span><span class="sxs-lookup"><span data-stu-id="3f88d-109">All user-defined calculations are also processed.</span></span>

- <span data-ttu-id="3f88d-110">**Meðalgreiðsludagar** - Þetta stig er meðalfjöldi daga sem viðskiptavinur tekur til að greiða reikninga.</span><span class="sxs-lookup"><span data-stu-id="3f88d-110">**Average payment days** – This score is the average number of days that a customer takes to pay invoices.</span></span>
- <span data-ttu-id="3f88d-111">**Viðskiptavinur síðan** - Þetta stig er fjöldi ára sem viðskiptavinur hefur verið viðskiptavinur fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="3f88d-111">**Customer since** – This score is the number of years that a customer has been a customer of your organization.</span></span>
- <span data-ttu-id="3f88d-112">**Í viðskiptum síðan** - Þetta stig er fjöldi ára sem viðskiptavinur hefur verið í viðskiptum.</span><span class="sxs-lookup"><span data-stu-id="3f88d-112">**In business since** – This score is the number of years that a customer has been in business.</span></span> <span data-ttu-id="3f88d-113">Það notar gildið í reitnum **Upphaf viðskipta** á síðunni **Viðskiptavinir**.</span><span class="sxs-lookup"><span data-stu-id="3f88d-113">It uses the value of the **Business start** field on the **Customers** page.</span></span>
- <span data-ttu-id="3f88d-114">**Dagasala framúrskarandi** - Þessi skora er byggð á viðskiptakröfu, sölutekjum og fjölda daga fyrir 12 mánaða tímabilið á undan.</span><span class="sxs-lookup"><span data-stu-id="3f88d-114">**Days sales outstanding** – This score is based on the accounts receivable balance, sales revenue, and number of days for the previous 12-month period.</span></span>
- <span data-ttu-id="3f88d-115">**Meðaljafnvægi** - Einkunnin er byggð á viðskiptakröfu fyrir 12 mánaða tímabil.</span><span class="sxs-lookup"><span data-stu-id="3f88d-115">**Average balance** – This score is based on the accounts receivable balance for the previous 12-month period.</span></span>
- <span data-ttu-id="3f88d-116">**Lánastjórnunarhópur**, **Staða reiknings** og **Land** - Þessar stigatölur nota upplýsingar frá viðskiptavininum.</span><span class="sxs-lookup"><span data-stu-id="3f88d-116">**Credit management group**, **Account status**, and **Country** – These scores use information from the customer.</span></span>

## <a name="update-customer-balance-statistics"></a><span data-ttu-id="3f88d-117">Uppfæra tölfræði um stöður viðskiptavina</span><span class="sxs-lookup"><span data-stu-id="3f88d-117">Update customer balance statistics</span></span>

<span data-ttu-id="3f88d-118">Þú getur keyrt ferlið **Uppfæra tölfræði um stöður viðskiptavina** til að uppfæra útreikning á tölfræði um jafnvægi sem sést á síðunni **Fyrirspurn um stöðutölur**.</span><span class="sxs-lookup"><span data-stu-id="3f88d-118">You can run the **Update customer balance statistics** process to update the calculation of balance statistics that is shown on the **Balance statistics inquiry** page.</span></span> <span data-ttu-id="3f88d-119">Þessar upplýsingar eru notaðar til að reikna út áhættustig og gildi sem sýnd eru í útlánatölfræði upplýsingareita á síðunni **Viðskiptavinur**.</span><span class="sxs-lookup"><span data-stu-id="3f88d-119">This information is used to calculate risk scores and the values that are shown in the credit statistics FactBoxes on the **Customer** page.</span></span>

<span data-ttu-id="3f88d-120">Þegar þú keyrir ferlið uppfærir það tölfræði um jafnvægi viðskiptavina fyrir einn viðskiptavin.</span><span class="sxs-lookup"><span data-stu-id="3f88d-120">When you run the process, it updates customer balance statistics for a single customer.</span></span> <span data-ttu-id="3f88d-121">Til að setja upp hópvinnu til að keyra ferlið fyrir marga viðskiptavini er hægt að nota síðuna **Reikna stöðutölur** (**Lánastjórnun \> Reglubundin verk \> Reikna stöðutölur**).</span><span class="sxs-lookup"><span data-stu-id="3f88d-121">To set up a batch job to run the process for multiple customers, you can use the **Calculate balance statistics** page (**Credit management \> Periodic tasks \> Calculate balance statistics**).</span></span>
