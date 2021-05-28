---
title: Safnvistun útprentaðra reikninga viðskiptavina með tætigildum
description: Þetta efnisatriði útskýrir hvernig á að virkja safnvistun til þess að geyma prentaða reikninga viðskiptavina með tætigildum.
author: ilyako
ms.date: 03/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 841e6059f5b0d70dbd1fe12a1f8910bbb31ddc86
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018979"
---
# <a name="archive-printed-customer-invoices-with-hash-numbers"></a><span data-ttu-id="6a86d-103">Safnvistun útprentaðra reikninga viðskiptavina með tætigildum</span><span class="sxs-lookup"><span data-stu-id="6a86d-103">Archive printed customer invoices with hash numbers</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="6a86d-104">Í sumum löndum eru lagalegar kröfur um að geyma reiknuð tætigildi í kerfinu ásamt útprentun á sömu skjala.</span><span class="sxs-lookup"><span data-stu-id="6a86d-104">In some countries, there is a legal requirement to store calculated hash numbers in the system together with printouts of some documents.</span></span> <span data-ttu-id="6a86d-105">Tætigildi er hægt að nota til að tilkynninga yfirvöldum og við endurskoðun.</span><span class="sxs-lookup"><span data-stu-id="6a86d-105">Hash numbers can be used for reporting to authorities and during audits.</span></span>

<span data-ttu-id="6a86d-106">Þetta efnisatriði útskýrir hvernig á að skilgreina safnvistun til þess að geyma prentaða reikninga viðskiptavina með tætigildum.</span><span class="sxs-lookup"><span data-stu-id="6a86d-106">This topic explains how to configure archiving in order to store printed customer invoices with hash numbers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6a86d-107">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="6a86d-107">Prerequisites</span></span>

- <span data-ttu-id="6a86d-108">Á vinnusvæðinu **Eiginleikastjórnun** skal kveikja á eiginleikanum **Safnvistun útprentaðra reikninga viðskiptavina með tætigildum**.</span><span class="sxs-lookup"><span data-stu-id="6a86d-108">In the **Feature management** workspace, turn on the feature, **Archive printed customer invoices with hash numbers**.</span></span> <span data-ttu-id="6a86d-109">Frekari upplýsingar er að finna í [Eiginleikastjórnunaryfirlit](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6a86d-109">For more information, see [Feature management overview](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
- <span data-ttu-id="6a86d-110">Skilgreinið prentvæn snið nauðsynlegra skjala í **Prentstýringu**.</span><span class="sxs-lookup"><span data-stu-id="6a86d-110">Configure the printable formats of required documents in **Print management**.</span></span>

<span data-ttu-id="6a86d-111">Virknin gildir um eftirfarandi skjöl.</span><span class="sxs-lookup"><span data-stu-id="6a86d-111">This functionality is applicable to the following documents.</span></span>

<span data-ttu-id="6a86d-112">**Viðskiptakröfur**</span><span class="sxs-lookup"><span data-stu-id="6a86d-112">**Accounts receivable**</span></span>
- <span data-ttu-id="6a86d-113">Reikningur viðskiptavina</span><span class="sxs-lookup"><span data-stu-id="6a86d-113">Customer invoice</span></span>
- <span data-ttu-id="6a86d-114">Kreditnóta viðskiptavina</span><span class="sxs-lookup"><span data-stu-id="6a86d-114">Customer credit note</span></span>
- <span data-ttu-id="6a86d-115">Textareikningur</span><span class="sxs-lookup"><span data-stu-id="6a86d-115">Free text invoice</span></span>
- <span data-ttu-id="6a86d-116">Textakreditnóta</span><span class="sxs-lookup"><span data-stu-id="6a86d-116">Free text credit note</span></span>

<span data-ttu-id="6a86d-117">**Verkefnastjórnun og bókhald**</span><span class="sxs-lookup"><span data-stu-id="6a86d-117">**Project management and accounting**</span></span>
- <span data-ttu-id="6a86d-118">Verkreikningur</span><span class="sxs-lookup"><span data-stu-id="6a86d-118">Project invoice</span></span>
- <span data-ttu-id="6a86d-119">Kreditnóta verks</span><span class="sxs-lookup"><span data-stu-id="6a86d-119">Project credit note</span></span>

## <a name="configure-customer-master-data"></a><span data-ttu-id="6a86d-120">Skilgreina aðalgögn viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="6a86d-120">Configure customer master data</span></span>
<span data-ttu-id="6a86d-121">Ljúkið eftirfarandi skrefum til að skilgreina gögn viðskiptavinar og kveikið á sjálfvirkri vistun útprentaðra reikninga sem viðhengi.</span><span class="sxs-lookup"><span data-stu-id="6a86d-121">Complete the following steps to configure customer data and turn on the ability to automatically save printed invoices as attachments.</span></span>

1. <span data-ttu-id="6a86d-122">Farið í **Viðskiptakröfur** > **Allir viðskiptavinir**.</span><span class="sxs-lookup"><span data-stu-id="6a86d-122">Go to **Accounts receivable** > **All customers**.</span></span> 
2. <span data-ttu-id="6a86d-123">Veljið viðskiptavin og í flýtiflipanum **Reikningur og afhending**, í hlutanum **Rafrænn reikningur**, í reitnum **Rafrænn reikningur í viðhengi**, skal velja **Já**.</span><span class="sxs-lookup"><span data-stu-id="6a86d-123">Select a customer, and on the **Invoice and delivery** FastTab, in the **E-INVOCE** section, in the **eInvoice attachment** field, select **Yes**.</span></span>

## <a name="print-invoices"></a><span data-ttu-id="6a86d-124">Prenta reikninga</span><span class="sxs-lookup"><span data-stu-id="6a86d-124">Print invoices</span></span>
<span data-ttu-id="6a86d-125">Hægt er að bóka og prenta út alla frjálsa texta, viðskiptavini og verkreikninga eða kreditnótur fyrir viðskiptavininn sem er skilgreindur í ferlinu hér á undan.</span><span class="sxs-lookup"><span data-stu-id="6a86d-125">You can post and print any free text, customer, and project invoice or credit note for the customer configured in the previous procedure.</span></span>

<span data-ttu-id="6a86d-126">Opnið síðuna **Viðhengi** fyrir prentaðan reikning.</span><span class="sxs-lookup"><span data-stu-id="6a86d-126">Open the **Attachments** page for the printed invoice.</span></span> <span data-ttu-id="6a86d-127">Í flýtiflipanum **Viðhengi**, í reitahópnum **Frekari upplýsingar**, í reitnum **Tætinúmer skjals**, skal leita að geymdu tætigildi sem var reiknað út fyrir prentaðan reikning.</span><span class="sxs-lookup"><span data-stu-id="6a86d-127">On the **Attachment** FastTab, in the **Additional details** field group, in **Document hash number** field, find the stored hash number calculated for the printed invoice.</span></span>

![Tætinúmer viðhengis](media/attach-hash-num.jpg)

