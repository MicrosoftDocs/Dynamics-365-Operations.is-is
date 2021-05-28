---
title: Setja upp yfirvöld staðgreiðsluskatts fyrir TDS-skattgerðina
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp yfirvald skatts sem er dreginn frá upprunalegri greiðslu (TDS).
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
ms.openlocfilehash: 5375363a9b1383a83e80fc3c4b841780adab4172
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023320"
---
# <a name="set-up-withholding-tax-authorities-for-the-tds-tax-type"></a><span data-ttu-id="ff5bd-103">Setja upp yfirvöld staðgreiðsluskatts fyrir TDS-skattgerðina</span><span class="sxs-lookup"><span data-stu-id="ff5bd-103">Set up withholding tax authorities for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ff5bd-104">Í þessu efnisatriði er útskýrt hvernig á að setja upp yfirvald skatts sem er dreginn frá upprunalegri greiðslu (TDS).</span><span class="sxs-lookup"><span data-stu-id="ff5bd-104">This topic explains how to set up Tax Deducted at Source (TDS) authorities.</span></span>

1. <span data-ttu-id="ff5bd-105">Farið í **Skattur \> Óbeinir skattar \> Yfirvöld staðgreiðsluskatts**.</span><span class="sxs-lookup"><span data-stu-id="ff5bd-105">Go to **Tax \> Indirect taxes \> Withholding tax authorities**.</span></span>

    <span data-ttu-id="ff5bd-106">[![Yfirvaldssíða staðgreiðsluskatts](./media/apac-ind-TDS-12.png)](./media/apac-ind-TDS-12.png)</span><span class="sxs-lookup"><span data-stu-id="ff5bd-106">[![Withholding tax authorities page](./media/apac-ind-TDS-12.png)](./media/apac-ind-TDS-12.png)</span></span>

2. <span data-ttu-id="ff5bd-107">Í reitnum **Skattgerð** skal velja **TDS** til að setja upp skattayfirvöld fyrir skattgerð TDS.</span><span class="sxs-lookup"><span data-stu-id="ff5bd-107">In the **Tax type** field, select **TDS** to set up withholding tax authorities for the TDS tax type.</span></span>
3. <span data-ttu-id="ff5bd-108">Veldu **Nýtt** á aðgerðasvæðinu til að búa til línu.</span><span class="sxs-lookup"><span data-stu-id="ff5bd-108">On the Action Pane, select **New** to create a line.</span></span>
4. <span data-ttu-id="ff5bd-109">Í reitnum **Yfirvald staðgreiðsluskatts** skal færa inn heiti fyrir TDS-yfirvald.</span><span class="sxs-lookup"><span data-stu-id="ff5bd-109">In the **Withholding tax authority** field, enter a name for the TDS authority.</span></span>
5. <span data-ttu-id="ff5bd-110">Í reitnum **Lýsing** skal færa inn lýsingu.</span><span class="sxs-lookup"><span data-stu-id="ff5bd-110">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="ff5bd-111">Á síðunni **Viðskiptavinir** á flýtiflipanum **Lánardrottnalykill** skal velja lánardrottnalykilinn fyrir TDS-yfirvald.</span><span class="sxs-lookup"><span data-stu-id="ff5bd-111">On the **General** FastTab, in the **Vendor account** field, select the vendor account for the TDS authority.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ff5bd-112">Þú verður að skilgreina heiti bankans þar sem fjármunir sem TDS-yfirvalda eru skuldað verða lagðir inn.</span><span class="sxs-lookup"><span data-stu-id="ff5bd-112">You must define the name of the bank where funds that are owed to the TDS authority vendor will be deposited.</span></span> <span data-ttu-id="ff5bd-113">Nafn bankans er skilgreint á síðunni **Bankareikningar** (**Viðskiptaskuldir \> Allir lánardrottnar \> Lánardrottinn \> Setja upp \> Bankareikningar**).</span><span class="sxs-lookup"><span data-stu-id="ff5bd-113">The bank's name is defined on the **Bank accounts** page (**Accounts payable \> All vendors \> Vendor \> Set up \> Bank accounts**).</span></span>

7. <span data-ttu-id="ff5bd-114">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="ff5bd-114">Close the page.</span></span>
