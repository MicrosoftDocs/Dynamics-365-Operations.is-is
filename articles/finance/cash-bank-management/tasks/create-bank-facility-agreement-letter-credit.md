---
title: Stofna bankaaðstöðusamning fyrir bankaábyrgð
description: Þetta verk útskýrir stofnun bankaaðstöðusamning til að vinna ábyrgðarbréf.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankDocumentFacilityAgreement, BankAccountTableLookUp, BankDocumentFacilityAgreementExtension, DefaultDashboard
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e63e0ffa4ddafd38595d7e9d84ffa2399a9f67b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188212"
---
# <a name="create-a-bank-facility-agreement-for-a-letter-of-credit"></a><span data-ttu-id="78148-103">Stofna bankaaðstöðusamning fyrir bankaábyrgð</span><span class="sxs-lookup"><span data-stu-id="78148-103">Create a bank facility agreement for a letter of credit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="78148-104">Þetta verk útskýrir stofnun bankaaðstöðusamning til að vinna ábyrgðarbréf.</span><span class="sxs-lookup"><span data-stu-id="78148-104">This task walks through the creating a Bank facility agreement to process a Letter of credit.</span></span> <span data-ttu-id="78148-105">Þú þarft að setja upp bankaaðstöður og bókunarreglur á undan þetta verk.</span><span class="sxs-lookup"><span data-stu-id="78148-105">You will want to set up bank facilities and posting profiles before this task.</span></span>  <span data-ttu-id="78148-106">Þetta notar verk 'USMF' sýnigögn fyrirtækið .</span><span class="sxs-lookup"><span data-stu-id="78148-106">This task uses the demo company 'USMF'.</span></span>  


## <a name="create-bank-facility-agreement"></a><span data-ttu-id="78148-107">Stofna bankaaðstöðusamningur</span><span class="sxs-lookup"><span data-stu-id="78148-107">Create Bank facility agreement</span></span>
1. <span data-ttu-id="78148-108">Fara í Reiðufé og bankastjórnun > Kreditbréf > Bankaaðstöðusamningur.</span><span class="sxs-lookup"><span data-stu-id="78148-108">Go to Cash and bank management > Letters of credit > Bank facility agreements.</span></span>
2. <span data-ttu-id="78148-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="78148-109">Click New.</span></span>
3. <span data-ttu-id="78148-110">Í svæðið samningsnúmer, færðu inn samningsnúmer samkvæmt samkomulagi við bankann.</span><span class="sxs-lookup"><span data-stu-id="78148-110">In the Agreement number field, enter the agreement number according to the agreement with the bank.</span></span>
4. <span data-ttu-id="78148-111">Í svæðinu bankareikning, færið inn lykilnúmer bankans sem gefur út.</span><span class="sxs-lookup"><span data-stu-id="78148-111">In the Bank account field, enter the account number at the issuing bank.</span></span>
5. <span data-ttu-id="78148-112">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="78148-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="78148-113">Í reitnum upphafsdagur, færa inn dagsetningu og tíma.</span><span class="sxs-lookup"><span data-stu-id="78148-113">In the Start date field, enter a date and time.</span></span>
7. <span data-ttu-id="78148-114">Í reitnum Lokadagur, færa inn dagsetningu og tíma.</span><span class="sxs-lookup"><span data-stu-id="78148-114">In the End date field, enter a date and time.</span></span>
8. <span data-ttu-id="78148-115">Útvíkka eða draga saman hlutann Almennt.</span><span class="sxs-lookup"><span data-stu-id="78148-115">Expand or collapse the General section.</span></span>
9. <span data-ttu-id="78148-116">Smella á bæta Við línu.</span><span class="sxs-lookup"><span data-stu-id="78148-116">Click Add line.</span></span>
10. <span data-ttu-id="78148-117">Í reitnum aðstöðugerð skal smella a fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="78148-117">In the Facility type field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="78148-118">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="78148-118">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="78148-119">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="78148-119">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="78148-120">Í reitinn Mörk færirðu inn upphæð aðstöðu sem samið var um við bankann.</span><span class="sxs-lookup"><span data-stu-id="78148-120">In the Limit field, enter the facility amount that was negotiated with the bank.</span></span>
14. <span data-ttu-id="78148-121">Smelltu á Vista.</span><span class="sxs-lookup"><span data-stu-id="78148-121">Click Save.</span></span>
15. <span data-ttu-id="78148-122">Smellt er á víkka út til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="78148-122">Click Extend to open the drop dialog.</span></span>
16. <span data-ttu-id="78148-123">Færa inn gildi í svæðið nýtt samningsnúmer.</span><span class="sxs-lookup"><span data-stu-id="78148-123">In the New agreement number field, type a value.</span></span>
17. <span data-ttu-id="78148-124">Í reitnum Lokadagur, færa inn dagsetningu og tíma.</span><span class="sxs-lookup"><span data-stu-id="78148-124">In the End date field, enter a date and time.</span></span>
18. <span data-ttu-id="78148-125">Smellt er á Framlengja.</span><span class="sxs-lookup"><span data-stu-id="78148-125">Click Extend.</span></span>
19. <span data-ttu-id="78148-126">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="78148-126">Close the page.</span></span>
