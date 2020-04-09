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
ms.openlocfilehash: ec21415158ad611d0ad55778e76aa128f53561bd
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143385"
---
# <a name="create-a-record-template-to-facilitate-data-entry"></a><span data-ttu-id="77cd5-103">Búa til færslusniðmát til að greiða fyrir skráningu gagna</span><span class="sxs-lookup"><span data-stu-id="77cd5-103">Create a record template to facilitate data entry</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="77cd5-104">Þetta efni sýnir hvernig stofna færslusniðmát til að gildi í svæði sem oft notað ekki þurfa að slá inn sérstaklega fyrir hverja ný færsla.</span><span class="sxs-lookup"><span data-stu-id="77cd5-104">This topic demonstrates how to create a record template so that field values that are used often do not have to be entered explicitly for each new record.</span></span> <span data-ttu-id="77cd5-105">Í þessu ferli er stofnuð ný færsla fyrir nýjar fartölvur sem ætti að bæta við eignir þínar.</span><span class="sxs-lookup"><span data-stu-id="77cd5-105">In this procedure, you'll create a new record for new laptops that should be added to your fixed assets.</span></span> <span data-ttu-id="77cd5-106">Þetta ferli notar USMF sýnifyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="77cd5-106">This procedure uses the USMF sample company.</span></span>

1. <span data-ttu-id="77cd5-107">Í skoðunarrúðnni ferðu í **Kerfseiningar > Fastafjármunir > Fastafjármunir > Fastafjármunir**.</span><span class="sxs-lookup"><span data-stu-id="77cd5-107">In the navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="77cd5-108">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="77cd5-108">Select **New**.</span></span>
3. <span data-ttu-id="77cd5-109">Í reitnum **Eignaflokkur** skal færa inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="77cd5-109">In the **Fixed asset group** field, enter or select a value.</span></span>
4. <span data-ttu-id="77cd5-110">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="77cd5-110">In the **Name** field, type a value.</span></span> <span data-ttu-id="77cd5-111">Sláðu til dæmis inn **Fartölva yfirmanns**.</span><span class="sxs-lookup"><span data-stu-id="77cd5-111">For example, enter **Corporate lead laptop**.</span></span>  
5. <span data-ttu-id="77cd5-112">Í svæði **Leita að nafni** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="77cd5-112">In the **Search name** field, type a value.</span></span> <span data-ttu-id="77cd5-113">Sláðu til dæmis inn **fartölva**.</span><span class="sxs-lookup"><span data-stu-id="77cd5-113">For example, enter **laptop**.</span></span>  
6. <span data-ttu-id="77cd5-114">Víkkaðu út hlutann **Tæknilegar upplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="77cd5-114">Expand the **Technical information** section.</span></span>
7. <span data-ttu-id="77cd5-115">Í reitunum **Gerð**, **Líkan** og **Árgerð** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="77cd5-115">In the **Make**, **Model**, and **Model year** fields, type values.</span></span>
8. <span data-ttu-id="77cd5-116">Í aðgerðasvæðinu velurðu **Valkostir**.</span><span class="sxs-lookup"><span data-stu-id="77cd5-116">On the Action Pane, select **Options**.</span></span>
9. <span data-ttu-id="77cd5-117">Veldu **Skrá upplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="77cd5-117">Select **Record info**.</span></span>
10. <span data-ttu-id="77cd5-118">Velja **Notandasniðmát**.</span><span class="sxs-lookup"><span data-stu-id="77cd5-118">Select **User template**.</span></span>
11. <span data-ttu-id="77cd5-119">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="77cd5-119">In the **Name** field, type a value.</span></span>
12. <span data-ttu-id="77cd5-120">Í reitinn **Lýsing** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="77cd5-120">In the **Description** field, type a value.</span></span>
13. <span data-ttu-id="77cd5-121">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="77cd5-121">Select **OK**.</span></span>
14. <span data-ttu-id="77cd5-122">Veljið **Loka**.</span><span class="sxs-lookup"><span data-stu-id="77cd5-122">Select **Close**.</span></span>

