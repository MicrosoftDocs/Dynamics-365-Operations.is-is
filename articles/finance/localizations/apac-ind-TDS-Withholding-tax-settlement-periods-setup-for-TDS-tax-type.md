---
title: Setja upp jöfnunartímabil staðgreiðsluskatts fyrir TDS-skattgerðina
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp jöfnunartímabil fyrir skatt sem dreginn er frá í uppruna (TDS).
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
ms.openlocfilehash: 9430bc1386f127d02b598d6cad1b53f66e0cf2ba
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023315"
---
# <a name="set-up-withholding-tax-settlement-periods-for-the-tds-tax-type"></a><span data-ttu-id="7bdaf-103">Setja upp jöfnunartímabil staðgreiðsluskatts fyrir TDS-skattgerðina</span><span class="sxs-lookup"><span data-stu-id="7bdaf-103">Set up withholding tax settlement periods for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7bdaf-104">Í þessu efnisatriði er útskýrt hvernig á að setja upp jöfnunartímabil fyrir skatt sem dreginn er frá í uppruna (TDS).</span><span class="sxs-lookup"><span data-stu-id="7bdaf-104">This topic explains how to set up settlement periods for Tax Deducted at Source (TDS) settlement periods.</span></span>

1. <span data-ttu-id="7bdaf-105">Farið í **Skattur \> Óbeinir skattar \> Staðgreiðsluskattur \> Jöfnunartímabil staðgreiðsluskatts**.</span><span class="sxs-lookup"><span data-stu-id="7bdaf-105">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax settlement periods**.</span></span>

    <span data-ttu-id="7bdaf-106">[![Jöfnunartímabilssíða staðgreiðsluskatts](./media/apac-ind-TDS-13.png)](./media/apac-ind-TDS-13.png)</span><span class="sxs-lookup"><span data-stu-id="7bdaf-106">[![Withholding tax settlement periods page](./media/apac-ind-TDS-13.png)](./media/apac-ind-TDS-13.png)</span></span>

2. <span data-ttu-id="7bdaf-107">Í reitnum **Skattgerð** skal velja **TDS** til að setja upp uppgjörstímabil staðgreiðsluskatts fyrir skattgerð TDS.</span><span class="sxs-lookup"><span data-stu-id="7bdaf-107">In the **Tax type** field, select **TDS** to set up withholding tax settlement periods for the TDS tax type.</span></span>
3. <span data-ttu-id="7bdaf-108">Veldu **Nýtt** til að búa til nýja línu.</span><span class="sxs-lookup"><span data-stu-id="7bdaf-108">Select **New** to create a line.</span></span>
4. <span data-ttu-id="7bdaf-109">Í reitnum **Jöfnunartímabil** er fært inn heiti fyrir TDS-jöfnunartímabilið.</span><span class="sxs-lookup"><span data-stu-id="7bdaf-109">In the **Settlement period** field, enter a name for the TDS settlement period.</span></span>
5. <span data-ttu-id="7bdaf-110">Í reitnum **Lýsing** skal færa inn lýsingu.</span><span class="sxs-lookup"><span data-stu-id="7bdaf-110">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="7bdaf-111">Á svæðinu **Staðgreiðsluskattayfirvald** er valið hvaða TDS-yfirvald eru tilgreind fyrir TDS-jöfnunartímabilið.</span><span class="sxs-lookup"><span data-stu-id="7bdaf-111">In the **Withholding tax authority** field, select the TDS authority that you're defining the TDS settlement period for.</span></span>
7. <span data-ttu-id="7bdaf-112">Á flýtiflipanum **Almennt** í reitnum **Tímabili** er valin tegund tímabils fyrir TDS jöfnunartímabilið.</span><span class="sxs-lookup"><span data-stu-id="7bdaf-112">On the **General** FastTab, in the **Period interval** field, select the type of period interval for the TDS settlement period.</span></span>
8. <span data-ttu-id="7bdaf-113">Reiturinn **Fjöldi eininga** skal tilgreina fjöldi eininga fyrir gerð tímabilsins.</span><span class="sxs-lookup"><span data-stu-id="7bdaf-113">In the **Number of units** field, specify the number of units for the period interval type.</span></span>
9. <span data-ttu-id="7bdaf-114">Í flipanum **Tímabil** í **Frá dagsetning** skal velja upphafsdagsetningu fyrir TDS-jöfnunartímabilið.</span><span class="sxs-lookup"><span data-stu-id="7bdaf-114">On the **Periods** FastTab, in the **From date** field, select the start date for the TDS settlement period.</span></span> <span data-ttu-id="7bdaf-115">Í svæðið **Til dagsetningar** skal velja lokadagsetningu.</span><span class="sxs-lookup"><span data-stu-id="7bdaf-115">In the **To date** field, select the end date.</span></span>
10. <span data-ttu-id="7bdaf-116">Til að búa til eftirfylgjandi TDS jöfnunartímabil fyrir fyrirliggjandi tímabil, byggt á tímabils- og tímabilseiningum, skal velja **Nýtt tímabil**.</span><span class="sxs-lookup"><span data-stu-id="7bdaf-116">To create a subsequent TDS settlement period for an existing period, based on the period interval and period units, select **New period**.</span></span>
11. <span data-ttu-id="7bdaf-117">Til að skoða nákvæmar upplýsingar um reglulegt TDS-uppgjör sem keyrt er fyrir tiltekið uppgjörstímabil smellirðu **á Greiðslur staðgreiðsluskatts** til að opna síðuna **Greiðsla staðgreiðsluskatts**.</span><span class="sxs-lookup"><span data-stu-id="7bdaf-117">To view the details of the periodic TDS settlement that is run for a specific settlement period, select **Withholding tax payments** to open the **Withholding tax payment** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7bdaf-118">Til að keyra reglulega TDS uppgjörsferlið skaltu fara í **Fjárhagur \> Reglubundið \> Staðgreiðsluskattur \> Greiðsla staðgreiðsluskatts**.</span><span class="sxs-lookup"><span data-stu-id="7bdaf-118">To run the periodic TDS settlement process, go to **General ledger \> Periodic \> Withholding tax \> Withholding tax payment**.</span></span>

    <span data-ttu-id="7bdaf-119">[![Greiðslusíða staðgreiðsluskatts](./media/apac-ind-TDS-15.png)](./media/apac-ind-TDS-15.png)</span><span class="sxs-lookup"><span data-stu-id="7bdaf-119">[![Withholding tax payment page](./media/apac-ind-TDS-15.png)](./media/apac-ind-TDS-15.png)</span></span>

12. <span data-ttu-id="7bdaf-120">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7bdaf-120">Close the page.</span></span>
