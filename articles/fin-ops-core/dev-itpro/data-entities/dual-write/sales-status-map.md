---
title: Setja upp vörpun fyrir stöðudálka sölupöntunar
description: Þetta efnisatriði útskýrir hvernig setja á upp stöðudálka sölupöntunar fyrir tvískipt skrif.
author: dasani-madipalli
manager: tonyafehr
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: damadipa
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-06-25
ms.openlocfilehash: cc70501d231390ea15104d508a36300a1b2cd44c
ms.sourcegitcommit: 7e1be696894731e1c58074d9b5e9c5b3acf7e52a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4744300"
---
# <a name="set-up-the-mapping-for-the-sales-order-status-columns"></a><span data-ttu-id="98223-103">Setja upp vörpun fyrir stöðudálka sölupöntunar</span><span class="sxs-lookup"><span data-stu-id="98223-103">Set up the mapping for the sales order status columns</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="98223-104">Dálkarnir sem gefa til kynna stöðu sölupöntunar eru með mismunandi tölusetningargildum í Microsoft Dynamics 365 Supply Chain Management og Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="98223-104">The columns that indicate sales order status have different enumeration values in Microsoft Dynamics 365 Supply Chain Management and Dynamics 365 Sales.</span></span> <span data-ttu-id="98223-105">Viðbótaruppsetning er nauðsynleg til að varpa þessum dálkum í tvískiptum skrifum.</span><span class="sxs-lookup"><span data-stu-id="98223-105">Additional setup is required to map these columns in dual-write.</span></span>

## <a name="columns-in-supply-chain-management"></a><span data-ttu-id="98223-106">dálkar í Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="98223-106">columns in Supply Chain Management</span></span>

<span data-ttu-id="98223-107">Í Supply Chain Management endurspegla tveir dálkar stöðu sölupöntunarinnar.</span><span class="sxs-lookup"><span data-stu-id="98223-107">In Supply Chain Management, two columns reflect the status of the sales order.</span></span> <span data-ttu-id="98223-108">Dálkarnir sem þarf að varpa eru **Staða** og **Staða skjals**.</span><span class="sxs-lookup"><span data-stu-id="98223-108">The columns that you must map are **Status** and **Document Status**.</span></span>

<span data-ttu-id="98223-109">Tölusetningin **Staða** tilgreinir heildarstöðu pöntunar.</span><span class="sxs-lookup"><span data-stu-id="98223-109">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="98223-110">Þessi staða er sýnd í pöntunarhausnum.</span><span class="sxs-lookup"><span data-stu-id="98223-110">This status is shown on the order header.</span></span>

<span data-ttu-id="98223-111">Tölusetningin **Staða** er með eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="98223-111">The **Status** enumeration has the following values:</span></span>

- <span data-ttu-id="98223-112">Opin pöntun</span><span class="sxs-lookup"><span data-stu-id="98223-112">Open Order</span></span>
- <span data-ttu-id="98223-113">Afhent</span><span class="sxs-lookup"><span data-stu-id="98223-113">Delivered</span></span>
- <span data-ttu-id="98223-114">Reikningsfært</span><span class="sxs-lookup"><span data-stu-id="98223-114">Invoiced</span></span>
- <span data-ttu-id="98223-115">Hætt við</span><span class="sxs-lookup"><span data-stu-id="98223-115">Cancelled</span></span>

<span data-ttu-id="98223-116">Tölusetningin **Staða skjals** tilgreinir nýlegasta skjalið sem var búið til fyrir pöntunina.</span><span class="sxs-lookup"><span data-stu-id="98223-116">The **Document Status** enumeration specifies the most recent document that was generated for the order.</span></span> <span data-ttu-id="98223-117">Til dæmis, ef pöntunin er staðfest, er þetta skjal staðfesting á sölupöntuninni.</span><span class="sxs-lookup"><span data-stu-id="98223-117">For example, if the order is confirmed, this document is a sales order confirmation.</span></span> <span data-ttu-id="98223-118">Ef sölupöntun er reikningsfærð að hluta og eftirstandandi lína er staðfest, helst staða skjalsins áfram **Reikningur** vegna þess að reikningurinn er búinn til síðar í ferlinu.</span><span class="sxs-lookup"><span data-stu-id="98223-118">If a sales order is partially invoiced, and then the remaining line is confirmed, the document status remains **Invoice**, because the invoice is generated later in the process.</span></span>

<span data-ttu-id="98223-119">Tölusetningin **Staða skjals** er með eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="98223-119">The **Document Status** enumeration has the following values:</span></span>

- <span data-ttu-id="98223-120">Staðfesting</span><span class="sxs-lookup"><span data-stu-id="98223-120">Confirmation</span></span>
- <span data-ttu-id="98223-121">Tiltektarlisti</span><span class="sxs-lookup"><span data-stu-id="98223-121">Picking List</span></span>
- <span data-ttu-id="98223-122">Fylgiseðill</span><span class="sxs-lookup"><span data-stu-id="98223-122">Packing Slip</span></span>
- <span data-ttu-id="98223-123">Reikningur</span><span class="sxs-lookup"><span data-stu-id="98223-123">Invoice</span></span>

## <a name="columns-in-sales"></a><span data-ttu-id="98223-124">dálkar í Sales</span><span class="sxs-lookup"><span data-stu-id="98223-124">columns in Sales</span></span>

<span data-ttu-id="98223-125">Í Sales sýna tveir dálkar stöðu pöntunar.</span><span class="sxs-lookup"><span data-stu-id="98223-125">In Sales, two columns indicate the status of the order.</span></span> <span data-ttu-id="98223-126">Dálkarnir sem þarf að varpa eru **Staða** og **Staða úrvinnslu**.</span><span class="sxs-lookup"><span data-stu-id="98223-126">The columns that you must map are **Status** and **Processing Status**.</span></span>

<span data-ttu-id="98223-127">Tölusetningin **Staða** tilgreinir heildarstöðu pöntunar.</span><span class="sxs-lookup"><span data-stu-id="98223-127">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="98223-128">Hún eru með eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="98223-128">It has the following values:</span></span>

- <span data-ttu-id="98223-129">Í gangi</span><span class="sxs-lookup"><span data-stu-id="98223-129">Active</span></span>
- <span data-ttu-id="98223-130">Sent inn</span><span class="sxs-lookup"><span data-stu-id="98223-130">Submitted</span></span>
- <span data-ttu-id="98223-131">Uppfyllt</span><span class="sxs-lookup"><span data-stu-id="98223-131">Fulfilled</span></span>
- <span data-ttu-id="98223-132">Reikningsfært</span><span class="sxs-lookup"><span data-stu-id="98223-132">Invoiced</span></span>
- <span data-ttu-id="98223-133">Hætt við</span><span class="sxs-lookup"><span data-stu-id="98223-133">Cancelled</span></span>

<span data-ttu-id="98223-134">Tölusetningin **Staða úrvinnslu** var kynnt svo að hægt sé að varpa stöðunni með nákvæmari hætti í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="98223-134">The **Processing Status** enumeration was introduced so that the status can be mapped more accurately with Supply Chain Management.</span></span>

<span data-ttu-id="98223-135">Eftirfarandi tafla sýnir vörpun á **Stöðu úrvinnslu** í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="98223-135">The following table shows the mapping of **Processing Status** in Supply Chain Management.</span></span>

| <span data-ttu-id="98223-136">Vinnslustaða</span><span class="sxs-lookup"><span data-stu-id="98223-136">Processing Status</span></span>   | <span data-ttu-id="98223-137">Staða í Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="98223-137">Status in Supply Chain Management</span></span> | <span data-ttu-id="98223-138">Staða skjals í Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="98223-138">Document Status in Supply Chain Management</span></span> |
|---------------------|-----------------------------------|--------------------------------------------|
| <span data-ttu-id="98223-139">Í gangi</span><span class="sxs-lookup"><span data-stu-id="98223-139">Active</span></span>              | <span data-ttu-id="98223-140">Opin pöntun</span><span class="sxs-lookup"><span data-stu-id="98223-140">Open Order</span></span>                        | <span data-ttu-id="98223-141">Engum</span><span class="sxs-lookup"><span data-stu-id="98223-141">None</span></span>                                       |
| <span data-ttu-id="98223-142">Staðfest</span><span class="sxs-lookup"><span data-stu-id="98223-142">Confirmed</span></span>           | <span data-ttu-id="98223-143">Opin pöntun</span><span class="sxs-lookup"><span data-stu-id="98223-143">Open Order</span></span>                        | <span data-ttu-id="98223-144">Staðfesting</span><span class="sxs-lookup"><span data-stu-id="98223-144">Confirmation</span></span>                               |
| <span data-ttu-id="98223-145">Tekið til</span><span class="sxs-lookup"><span data-stu-id="98223-145">Picked</span></span>              | <span data-ttu-id="98223-146">Opin pöntun</span><span class="sxs-lookup"><span data-stu-id="98223-146">Open Order</span></span>                        | <span data-ttu-id="98223-147">Tínslulisti</span><span class="sxs-lookup"><span data-stu-id="98223-147">Picking List</span></span>                               |
| <span data-ttu-id="98223-148">Afhent að hluta</span><span class="sxs-lookup"><span data-stu-id="98223-148">Partially Delivered</span></span> | <span data-ttu-id="98223-149">Opin pöntun</span><span class="sxs-lookup"><span data-stu-id="98223-149">Open Order</span></span>                        | <span data-ttu-id="98223-150">Fylgiseðill</span><span class="sxs-lookup"><span data-stu-id="98223-150">Packing Slip</span></span>                               |
| <span data-ttu-id="98223-151">Afhent</span><span class="sxs-lookup"><span data-stu-id="98223-151">Delivered</span></span>           | <span data-ttu-id="98223-152">Afhent</span><span class="sxs-lookup"><span data-stu-id="98223-152">Delivered</span></span>                         | <span data-ttu-id="98223-153">Fylgiseðill</span><span class="sxs-lookup"><span data-stu-id="98223-153">Packing Slip</span></span>                               |
| <span data-ttu-id="98223-154">Reikningsfært að hluta</span><span class="sxs-lookup"><span data-stu-id="98223-154">Partially Invoiced</span></span>  | <span data-ttu-id="98223-155">Afhent</span><span class="sxs-lookup"><span data-stu-id="98223-155">Delivered</span></span>                         | <span data-ttu-id="98223-156">Reikningur</span><span class="sxs-lookup"><span data-stu-id="98223-156">Invoice</span></span>                                    |
| <span data-ttu-id="98223-157">Reikningsfært</span><span class="sxs-lookup"><span data-stu-id="98223-157">Invoiced</span></span>            | <span data-ttu-id="98223-158">Reikningsfært</span><span class="sxs-lookup"><span data-stu-id="98223-158">Invoiced</span></span>                          | <span data-ttu-id="98223-159">Reikningur</span><span class="sxs-lookup"><span data-stu-id="98223-159">Invoice</span></span>                                    |
| <span data-ttu-id="98223-160">Hætt við</span><span class="sxs-lookup"><span data-stu-id="98223-160">Cancelled</span></span>           | <span data-ttu-id="98223-161">Hætt við</span><span class="sxs-lookup"><span data-stu-id="98223-161">Cancelled</span></span>                         | <span data-ttu-id="98223-162">Ekki tiltækt</span><span class="sxs-lookup"><span data-stu-id="98223-162">Not applicable</span></span>                             |

<span data-ttu-id="98223-163">Eftirfarandi tafla sýnir vörpun á **Stöðu úrvinnslu** milli Sales og Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="98223-163">The following table shows the mapping of **Processing Status** between Sales and Supply Chain Management.</span></span>

| <span data-ttu-id="98223-164">Vinnslustaða</span><span class="sxs-lookup"><span data-stu-id="98223-164">Processing Status</span></span>   | <span data-ttu-id="98223-165">Staða í Sales</span><span class="sxs-lookup"><span data-stu-id="98223-165">Status in Sales</span></span> | <span data-ttu-id="98223-166">Staða í Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="98223-166">Status in Supply Chain Management</span></span> |
|---------------------|-----------------|-----------------------------------|
| <span data-ttu-id="98223-167">Í gangi</span><span class="sxs-lookup"><span data-stu-id="98223-167">Active</span></span>              | <span data-ttu-id="98223-168">Í gangi</span><span class="sxs-lookup"><span data-stu-id="98223-168">Active</span></span>          | <span data-ttu-id="98223-169">Opin pöntun</span><span class="sxs-lookup"><span data-stu-id="98223-169">Open Order</span></span>                        |
| <span data-ttu-id="98223-170">Staðfest</span><span class="sxs-lookup"><span data-stu-id="98223-170">Confirmed</span></span>           | <span data-ttu-id="98223-171">Sent inn</span><span class="sxs-lookup"><span data-stu-id="98223-171">Submitted</span></span>       | <span data-ttu-id="98223-172">Opin pöntun</span><span class="sxs-lookup"><span data-stu-id="98223-172">Open Order</span></span>                        |
| <span data-ttu-id="98223-173">Tekið til</span><span class="sxs-lookup"><span data-stu-id="98223-173">Picked</span></span>              | <span data-ttu-id="98223-174">Sent inn</span><span class="sxs-lookup"><span data-stu-id="98223-174">Submitted</span></span>       | <span data-ttu-id="98223-175">Opin pöntun</span><span class="sxs-lookup"><span data-stu-id="98223-175">Open Order</span></span>                        |
| <span data-ttu-id="98223-176">Afhent að hluta</span><span class="sxs-lookup"><span data-stu-id="98223-176">Partially Delivered</span></span> | <span data-ttu-id="98223-177">Í gangi</span><span class="sxs-lookup"><span data-stu-id="98223-177">Active</span></span>          | <span data-ttu-id="98223-178">Opin pöntun</span><span class="sxs-lookup"><span data-stu-id="98223-178">Open Order</span></span>                        |
| <span data-ttu-id="98223-179">Reikningsfært að hluta</span><span class="sxs-lookup"><span data-stu-id="98223-179">Partially Invoiced</span></span>  | <span data-ttu-id="98223-180">Í gangi</span><span class="sxs-lookup"><span data-stu-id="98223-180">Active</span></span>          | <span data-ttu-id="98223-181">Opin pöntun</span><span class="sxs-lookup"><span data-stu-id="98223-181">Open Order</span></span>                        |
| <span data-ttu-id="98223-182">Reikningsfært að hluta</span><span class="sxs-lookup"><span data-stu-id="98223-182">Partially Invoiced</span></span>  | <span data-ttu-id="98223-183">Uppfyllt</span><span class="sxs-lookup"><span data-stu-id="98223-183">Fulfilled</span></span>       | <span data-ttu-id="98223-184">Afhent</span><span class="sxs-lookup"><span data-stu-id="98223-184">Delivered</span></span>                         |
| <span data-ttu-id="98223-185">Reikningsfært</span><span class="sxs-lookup"><span data-stu-id="98223-185">Invoiced</span></span>            | <span data-ttu-id="98223-186">Reikningsfært</span><span class="sxs-lookup"><span data-stu-id="98223-186">Invoiced</span></span>        | <span data-ttu-id="98223-187">Reikningsfært</span><span class="sxs-lookup"><span data-stu-id="98223-187">Invoiced</span></span>                          |
| <span data-ttu-id="98223-188">Hætt við</span><span class="sxs-lookup"><span data-stu-id="98223-188">Cancelled</span></span>           | <span data-ttu-id="98223-189">Hætt við</span><span class="sxs-lookup"><span data-stu-id="98223-189">Cancelled</span></span>       | <span data-ttu-id="98223-190">Hætt við</span><span class="sxs-lookup"><span data-stu-id="98223-190">Cancelled</span></span>                         |

## <a name="setup"></a><span data-ttu-id="98223-191">Setja upp</span><span class="sxs-lookup"><span data-stu-id="98223-191">Setup</span></span>

<span data-ttu-id="98223-192">Til að setja upp vörpun fyrir stöðudálka sölupöntunar þarf að virkja eigindirnar **IsSOPIntegrationEnabled** og **isIntegrationUser**.</span><span class="sxs-lookup"><span data-stu-id="98223-192">To set up the mapping for the sales order status columns, you must enable the **IsSOPIntegrationEnabled** and **isIntegrationUser** attributes.</span></span>

<span data-ttu-id="98223-193">Til að virkja eigindina **IsSOPIntegrationEnabled** skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="98223-193">To enable the **IsSOPIntegrationEnabled** attribute, follow these steps.</span></span>

1. <span data-ttu-id="98223-194">Í vafra skal fara á `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span><span class="sxs-lookup"><span data-stu-id="98223-194">In a browser, go to `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span></span> <span data-ttu-id="98223-195">Skiptið út **\<test-name\>** með tengli fyrirtækisins við Sales.</span><span class="sxs-lookup"><span data-stu-id="98223-195">Replace **\<test-name\>** with your company's link to Sales.</span></span>
2. <span data-ttu-id="98223-196">Á síðunni sem opnast skal finna **organizationid** og gera athugasemd um gildið.</span><span class="sxs-lookup"><span data-stu-id="98223-196">On the page that is opened, find **organizationid**, and make a note of the value.</span></span>

    ![Leit að organizationid](media/sales-map-orgid.png)

3. <span data-ttu-id="98223-198">Í Sales skal opna stjórnborð vafrans og keyra eftirfarandi forskrift.</span><span class="sxs-lookup"><span data-stu-id="98223-198">In Sales, open the browser console, and run following script.</span></span> <span data-ttu-id="98223-199">Notið gildið **organizationid** úr skrefi 2.</span><span class="sxs-lookup"><span data-stu-id="98223-199">Use the **organizationid** value from step 2.</span></span>

    ```javascript
    Xrm.WebApi.updateRecord("organization",
    "d9a7c5f7-acbf-4aa9-86e8-a891c43f748c", {"issopintegrationenabled" :
    true}).then(
        function success(result) {
            console.log("Account updated");
            // perform operations on row update
        },
        function (error) {
            console.log(error.message);
            // handle error conditions
        }
    );
    ```

    ![JavaScript-kóði í stjórnborði vafrans](media/sales-map-script.png)

4. <span data-ttu-id="98223-201">Gangið úr skugga um að **IsSOPIntegrationEnabled** sé stillt á **satt**.</span><span class="sxs-lookup"><span data-stu-id="98223-201">Verify that **IsSOPIntegrationEnabled** is set to **true**.</span></span> <span data-ttu-id="98223-202">Notið vefslóðina úr skrefi 1 til að athuga gildið.</span><span class="sxs-lookup"><span data-stu-id="98223-202">Use the URL from step 1 to check the value.</span></span>

    ![IsSOPIntegrationEnabled stillt á satt](media/sales-map-integration-enabled.png)

<span data-ttu-id="98223-204">Til að virkja eigindina **erIntegrationUser** skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="98223-204">To enable the **isIntegrationUser** attribute, follow these steps.</span></span>

1. <span data-ttu-id="98223-205">Í Sales skal farið á **Stilling \> Sérstillingar \> Sérstilla kerfið**, velja **Notandatafla** og opna svo **Skjámynd \> Notandi**.</span><span class="sxs-lookup"><span data-stu-id="98223-205">In Sales, go to **Setting \> Customization \> Customize the System**, select **User table**, and then open **Form \> User**.</span></span>

    ![Skjámynd notanda opnuð](media/sales-map-user.png)

2. <span data-ttu-id="98223-207">Í Field Explorer skal finna **Stilling samþættingarnotanda** og tvísmella á það til að bæta því við skjámyndina.</span><span class="sxs-lookup"><span data-stu-id="98223-207">In Field Explorer, find **Integration user mode**, and double-click it to add it to the form.</span></span> <span data-ttu-id="98223-208">Vistið breytingarnar.</span><span class="sxs-lookup"><span data-stu-id="98223-208">Save your change.</span></span>

    ![Stillingadálki samþættingarnotanda bætt við skjámyndina](media/sales-map-field-explorer.png)

3. <span data-ttu-id="98223-210">Í Sales skal farið í **Stilling \> Öryggi \> Notendur** og breyta yfirlitinu úr **Virkjaðir notendur** í **Notendur forrits**.</span><span class="sxs-lookup"><span data-stu-id="98223-210">In Sales, go to **Setting \> Security \> Users**, and change the view from **Enabled Users** to **Application Users**.</span></span>

    ![Yfirlitinu breytt úr Virkjaðir notendur í Notendur forrits](media/sales-map-enabled-users.png)

4. <span data-ttu-id="98223-212">Veljið færslurnar tvær fyrir **Samþættingarnotandi tvöfaldra skrifa**.</span><span class="sxs-lookup"><span data-stu-id="98223-212">Select the two entries for **DualWrite IntegrationUser**.</span></span>

    ![Listi yfir notendur forrits](media/sales-map-user-mode.png)

5. <span data-ttu-id="98223-214">Breytið gildinu á dálkinum **Stilling samþættingarnotanda** í **Já**.</span><span class="sxs-lookup"><span data-stu-id="98223-214">Change the value of the **Integration user mode** column to **Yes**.</span></span>

    ![Gildinu breytt á stillingadálki samþættingarnotanda](media/sales-map-user-mode-yes.png)

<span data-ttu-id="98223-216">Sölupöntunum hefur verið varpað.</span><span class="sxs-lookup"><span data-stu-id="98223-216">Your sales orders are now mapped.</span></span>
