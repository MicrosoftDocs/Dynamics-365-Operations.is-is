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
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 18395f300965df7e024f0eec2b53fa4e8ad2cc3e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566203"
---
# <a name="create-a-bank-facility-agreement-for-a-letter-of-credit"></a><span data-ttu-id="64bdc-103">Stofna bankaaðstöðusamning fyrir bankaábyrgð</span><span class="sxs-lookup"><span data-stu-id="64bdc-103">Create a bank facility agreement for a letter of credit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="64bdc-104">Þetta verk útskýrir stofnun bankaaðstöðusamning til að vinna ábyrgðarbréf.</span><span class="sxs-lookup"><span data-stu-id="64bdc-104">This task walks through the creating a Bank facility agreement to process a Letter of credit.</span></span> <span data-ttu-id="64bdc-105">Þú þarft að setja upp bankaaðstöður og bókunarreglur á undan þetta verk.</span><span class="sxs-lookup"><span data-stu-id="64bdc-105">You will want to set up bank facilities and posting profiles before this task.</span></span>  <span data-ttu-id="64bdc-106">Þetta notar verk 'USMF' sýnigögn fyrirtækið .</span><span class="sxs-lookup"><span data-stu-id="64bdc-106">This task uses the demo company 'USMF'.</span></span>  


## <a name="create-bank-facility-agreement"></a><span data-ttu-id="64bdc-107">Stofna bankaaðstöðusamningur</span><span class="sxs-lookup"><span data-stu-id="64bdc-107">Create Bank facility agreement</span></span>
1. <span data-ttu-id="64bdc-108">Fara í Reiðufé og bankastjórnun > Kreditbréf > Bankaaðstöðusamningur.</span><span class="sxs-lookup"><span data-stu-id="64bdc-108">Go to Cash and bank management > Letters of credit > Bank facility agreements.</span></span>
2. <span data-ttu-id="64bdc-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="64bdc-109">Click New.</span></span>
3. <span data-ttu-id="64bdc-110">Í svæðið samningsnúmer, færðu inn samningsnúmer samkvæmt samkomulagi við bankann.</span><span class="sxs-lookup"><span data-stu-id="64bdc-110">In the Agreement number field, enter the agreement number according to the agreement with the bank.</span></span>
4. <span data-ttu-id="64bdc-111">Í svæðinu bankareikning, færið inn lykilnúmer bankans sem gefur út.</span><span class="sxs-lookup"><span data-stu-id="64bdc-111">In the Bank account field, enter the account number at the issuing bank.</span></span>
5. <span data-ttu-id="64bdc-112">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="64bdc-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="64bdc-113">Í reitnum upphafsdagur, færa inn dagsetningu og tíma.</span><span class="sxs-lookup"><span data-stu-id="64bdc-113">In the Start date field, enter a date and time.</span></span>
7. <span data-ttu-id="64bdc-114">Í reitnum Lokadagur, færa inn dagsetningu og tíma.</span><span class="sxs-lookup"><span data-stu-id="64bdc-114">In the End date field, enter a date and time.</span></span>
8. <span data-ttu-id="64bdc-115">Útvíkka eða draga saman hlutann Almennt.</span><span class="sxs-lookup"><span data-stu-id="64bdc-115">Expand or collapse the General section.</span></span>
9. <span data-ttu-id="64bdc-116">Smella á bæta Við línu.</span><span class="sxs-lookup"><span data-stu-id="64bdc-116">Click Add line.</span></span>
10. <span data-ttu-id="64bdc-117">Í reitnum aðstöðugerð skal smella a fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="64bdc-117">In the Facility type field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="64bdc-118">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="64bdc-118">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="64bdc-119">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="64bdc-119">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="64bdc-120">Í reitinn Mörk færirðu inn upphæð aðstöðu sem samið var um við bankann.</span><span class="sxs-lookup"><span data-stu-id="64bdc-120">In the Limit field, enter the facility amount that was negotiated with the bank.</span></span>
14. <span data-ttu-id="64bdc-121">Smelltu á Vista.</span><span class="sxs-lookup"><span data-stu-id="64bdc-121">Click Save.</span></span>
15. <span data-ttu-id="64bdc-122">Smellt er á víkka út til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="64bdc-122">Click Extend to open the drop dialog.</span></span>
16. <span data-ttu-id="64bdc-123">Færa inn gildi í svæðið nýtt samningsnúmer.</span><span class="sxs-lookup"><span data-stu-id="64bdc-123">In the New agreement number field, type a value.</span></span>
17. <span data-ttu-id="64bdc-124">Í reitnum Lokadagur, færa inn dagsetningu og tíma.</span><span class="sxs-lookup"><span data-stu-id="64bdc-124">In the End date field, enter a date and time.</span></span>
18. <span data-ttu-id="64bdc-125">Smellt er á Framlengja.</span><span class="sxs-lookup"><span data-stu-id="64bdc-125">Click Extend.</span></span>
19. <span data-ttu-id="64bdc-126">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="64bdc-126">Close the page.</span></span>

