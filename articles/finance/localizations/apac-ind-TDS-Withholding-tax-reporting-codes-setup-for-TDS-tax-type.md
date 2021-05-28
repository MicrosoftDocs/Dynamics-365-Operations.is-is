---
title: Setja upp skýrslugerðarkóða staðgreiðsluskatts fyrir TDS-skattgerðina
description: Skýrslukóðar fyrir staðgreiðsluskatt eru notaðir til að stofna eyðublað 26Q og eyðublað 27Q fyrir skattur sem dreginn er frá í uppruna (TDS). Í þessu efnisatriði er útskýrt hvernig staðgreiðslukóðar eru settir upp svo hægt sé að setja upp TDS skýrslukóða.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 1f9325d182f89b98e8b943ae047c55e7e1aeb02f
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023338"
---
# <a name="set-up-withholding-tax-reporting-codes-for-the-tds-tax-type"></a><span data-ttu-id="6bc2c-104">Setja upp skýrslugerðarkóða staðgreiðsluskatts fyrir TDS-skattgerðina</span><span class="sxs-lookup"><span data-stu-id="6bc2c-104">Set up withholding tax reporting codes for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6bc2c-105">Skýrslukóðar fyrir staðgreiðsluskatt eru notaðir til að stofna eyðublað 26Q og eyðublað 27Q fyrir skattur sem dreginn er frá í uppruna (TDS).</span><span class="sxs-lookup"><span data-stu-id="6bc2c-105">Withholding tax reporting codes are used to generate Form 26Q and Form 27Q statements for Tax Deducted at Source (TDS).</span></span> <span data-ttu-id="6bc2c-106">Í þessu efnisatriði er útskýrt hvernig staðgreiðslukóðar eru settir upp svo hægt sé að setja upp TDS skýrslukóða.</span><span class="sxs-lookup"><span data-stu-id="6bc2c-106">This topic explains how to set up withholding tax reporting codes steps so that you can set up TDS reporting codes.</span></span>

1. <span data-ttu-id="6bc2c-107">Farið í **Skattur \> Uppsetning \> Staðgreiðsluskattur \> Skýrslugerðarkóðar staðgreiðsluskatts**.</span><span class="sxs-lookup"><span data-stu-id="6bc2c-107">Go to **Tax \> Setup \> Withholding tax \> Withholding tax reporting codes**.</span></span>

    <span data-ttu-id="6bc2c-108">[![Síða skýrslugerðarkóða staðgreiðsluskatts](./media/apac-ind-TDS-16.png)](./media/apac-ind-TDS-16.png)</span><span class="sxs-lookup"><span data-stu-id="6bc2c-108">[![Withholding tax reporting codes page](./media/apac-ind-TDS-16.png)](./media/apac-ind-TDS-16.png)</span></span>

2. <span data-ttu-id="6bc2c-109">Í reitnum **Skattgerð** skal velja **TDS** til að skilgreina skýrslugerðarkóði staðgreiðsluskatts fyrir skattgerð TDS.</span><span class="sxs-lookup"><span data-stu-id="6bc2c-109">In the **Tax type** field, select **TDS** to define withholding tax reporting codes for the TDS tax type.</span></span>
3. <span data-ttu-id="6bc2c-110">Í reitnum **Staðgreiðsluþáttur** skal velja TDS-þáttinn sem kóði staðgreiðsluskattskýrslu er skilgreindur fyrir.</span><span class="sxs-lookup"><span data-stu-id="6bc2c-110">In the **Withholding tax component** field, select the TDS component to that you're defining the withholding tax reporting code for.</span></span> <span data-ttu-id="6bc2c-111">Reiturinn **Hópur staðgreiðsluskattshluti** sýnir TDS-hlutahópinn sem tilgreindur er fyrir TDS-hlutann sem verið er að skilgreina.</span><span class="sxs-lookup"><span data-stu-id="6bc2c-111">The **Withholding tax component group** field shows the TDS component group that was defined for the TDS component that you're defining.</span></span>

    <span data-ttu-id="6bc2c-112">Reiturinn **Kaflakóði** á flýtiflipanum **Almennt** sýnir kaflakóðann sem tengdur er TDS-hlutaflokknum.</span><span class="sxs-lookup"><span data-stu-id="6bc2c-112">The **Section code** field on the **General** FastTab shows the section code that is attached to the TDS component group.</span></span>

4. <span data-ttu-id="6bc2c-113">Á flýtiflipanum **Almennt** í reitnum **Skýrslugerðarkóði** skal velja TDS skýrslugerðarkóðann.</span><span class="sxs-lookup"><span data-stu-id="6bc2c-113">On the **General** FastTab, in the **Reporting code** field, select the TDS reporting code:</span></span>

    - <span data-ttu-id="6bc2c-114">TDS</span><span class="sxs-lookup"><span data-stu-id="6bc2c-114">TDS</span></span>
    - <span data-ttu-id="6bc2c-115">TCS</span><span class="sxs-lookup"><span data-stu-id="6bc2c-115">TCS</span></span>
    - <span data-ttu-id="6bc2c-116">Álag </span><span class="sxs-lookup"><span data-stu-id="6bc2c-116">Surcharge</span></span>
    - <span data-ttu-id="6bc2c-117">PE\_Cess</span><span class="sxs-lookup"><span data-stu-id="6bc2c-117">PE\_Cess</span></span>
    - <span data-ttu-id="6bc2c-118">SHE\_Cess</span><span class="sxs-lookup"><span data-stu-id="6bc2c-118">SHE\_Cess</span></span>

5. <span data-ttu-id="6bc2c-119">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="6bc2c-119">Close the page.</span></span>
