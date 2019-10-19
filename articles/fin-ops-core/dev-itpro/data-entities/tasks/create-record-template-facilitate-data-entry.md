---
title: Búa til færslusniðmát til að greiða fyrir skráningu gagna
description: Þetta efni sýnir hvernig stofna færslusniðmát til að gildi í svæði sem oft notað ekki þurfa að slá inn sérstaklega fyrir hverja ný færsla.
author: margoc
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, SysRecordInfo, SysRecordTemplatePromptOnCreate
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 08ee7d0f0ce7e92eaa85137dcd2761bfd702eb8c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2181934"
---
# <a name="create-a-record-template-to-facilitate-data-entry"></a><span data-ttu-id="16efe-103">Búa til færslusniðmát til að greiða fyrir skráningu gagna</span><span class="sxs-lookup"><span data-stu-id="16efe-103">Create a record template to facilitate data entry</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="16efe-104">Þetta efni sýnir hvernig stofna færslusniðmát til að gildi í svæði sem oft notað ekki þurfa að slá inn sérstaklega fyrir hverja ný færsla.</span><span class="sxs-lookup"><span data-stu-id="16efe-104">This topic demonstrates how to create a record template so that field values that are used often do not have to be entered explicitly for each new record.</span></span> <span data-ttu-id="16efe-105">Í þessu ferli er stofnað ný færsla fyrir nýjar fartölvur sem ætti að bæta við þínar eignir.</span><span class="sxs-lookup"><span data-stu-id="16efe-105">In this procedure, you’ll create a new record for new laptops that should be added to your fixed assets.</span></span> <span data-ttu-id="16efe-106">Þetta ferli notar USMF sýnifyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="16efe-106">This procedure uses the USMF sample company.</span></span>

1. <span data-ttu-id="16efe-107">Í skoðunarrúðnni ferðu í **Kerfseiningar > Fastafjármunir > Fastafjármunir > Fastafjármunir**.</span><span class="sxs-lookup"><span data-stu-id="16efe-107">In the navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="16efe-108">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="16efe-108">Select **New**.</span></span>
3. <span data-ttu-id="16efe-109">Í reitnum **Eignaflokkur** skal færa inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="16efe-109">In the **Fixed asset group** field, enter or select a value.</span></span>
4. <span data-ttu-id="16efe-110">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="16efe-110">In the **Name** field, type a value.</span></span> <span data-ttu-id="16efe-111">Sláðu til dæmis inn **Fartölva yfirmanns**.</span><span class="sxs-lookup"><span data-stu-id="16efe-111">For example, enter **Corporate lead laptop**.</span></span>  
5. <span data-ttu-id="16efe-112">Í svæði **Leita að nafni** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="16efe-112">In the **Search name** field, type a value.</span></span> <span data-ttu-id="16efe-113">Sláðu til dæmis inn **fartölva**.</span><span class="sxs-lookup"><span data-stu-id="16efe-113">For example, enter **laptop**.</span></span>  
6. <span data-ttu-id="16efe-114">Víkkaðu út hlutann **Tæknilegar upplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="16efe-114">Expand the **Technical information** section.</span></span>
7. <span data-ttu-id="16efe-115">Í reitunum **Gerð**, **Líkan** og **Árgerð** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="16efe-115">In the **Make**, **Model**, and **Model year** fields, type values.</span></span>
8. <span data-ttu-id="16efe-116">Í aðgerðasvæðinu velurðu **Valkostir**.</span><span class="sxs-lookup"><span data-stu-id="16efe-116">On the Action Pane, select **Options**.</span></span>
9. <span data-ttu-id="16efe-117">Veldu **Skrá upplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="16efe-117">Select **Record info**.</span></span>
10. <span data-ttu-id="16efe-118">Velja **Notandasniðmát**.</span><span class="sxs-lookup"><span data-stu-id="16efe-118">Select **User template**.</span></span>
11. <span data-ttu-id="16efe-119">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="16efe-119">In the **Name** field, type a value.</span></span>
12. <span data-ttu-id="16efe-120">Í reitinn **Lýsing** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="16efe-120">In the **Description** field, type a value.</span></span>
13. <span data-ttu-id="16efe-121">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="16efe-121">Select **OK**.</span></span>
14. <span data-ttu-id="16efe-122">Veljið **Loka**.</span><span class="sxs-lookup"><span data-stu-id="16efe-122">Select **Close**.</span></span>

