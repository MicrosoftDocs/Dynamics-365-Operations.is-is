---
title: Gakktu úr skugga um að tvískipt skrif sé stillt í forritum Finance and Operations og Common Data Service
description: Þetta efni útskýrir hvernig þú getur ákvarðað hvort tvískipt skrif eru stillt í forritum Finance and Operations og í Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
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
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 2ddac76871a3ac574a1edcb5446be6c64e5e4682
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997231"
---
# <a name="verify-that-dual-write-is-configured-in-finance-and-operations-apps-and-common-data-service"></a><span data-ttu-id="610b1-103">Gakktu úr skugga um að tvískipt skrif sé stillt í forritum Finance and Operations og Common Data Service</span><span class="sxs-lookup"><span data-stu-id="610b1-103">Verify that dual-write is configured in Finance and Operations apps and Common Data Service</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="610b1-104">Þetta efni veitir upplýsingar um úrræðaleit um samþættingu á tvöföldum skrifum á milli forrita Finance and Operations og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="610b1-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="610b1-105">Einkum útskýrir það hvernig þú getur ákvarðað hvort tvískipt skrif eru stillt í forritum Finance and Operations og í Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="610b1-105">Specifically, it explains how you can determine whether dual-write is configured in Finance and Operations apps and in Common Data Service.</span></span>

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a><span data-ttu-id="610b1-106">Gakktu úr skugga um að tvískipt skrif sé stillt í forriti Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="610b1-106">Verify that dual-write is configured in a Finance and Operations app</span></span>

<span data-ttu-id="610b1-107">Til að ákvarða hvort villurnar sem þú sérð þegar þú reynir að vista skrár til uppfærslu koma frá tvískiptri skrifun, staðfestu fyrst að tvískipt skrif er stillt.</span><span class="sxs-lookup"><span data-stu-id="610b1-107">To determine whether the errors that you see when you try to save records for update come from dual-write, first verify that dual-write is configured.</span></span>

+ <span data-ttu-id="610b1-108">Ef þú hefur stjórnunarréttindi í forriti Finance and Operations, farðu til **Vinnusvæði \> Gagnastjórnun** og veldu reitinn **Tvöfalt skrif**.</span><span class="sxs-lookup"><span data-stu-id="610b1-108">If you have admin privileges in the Finance and Operations app, go to **Workspaces \> Data management** , and select the **Dual-write** tile.</span></span> <span data-ttu-id="610b1-109">Ef upplýsingar um tengd umhverfi og listi yfir heildarkort sem eru í gangi birtast er tvískipt skrifað.</span><span class="sxs-lookup"><span data-stu-id="610b1-109">If the details of the linked environments and the list of entity maps that are running are shown, dual-write is configured.</span></span>

    ![Staðfestir Finance and Operations forritatengingu þegar þú hefur stjórnunarréttindi](media/verify_fin_ops_1.png)

+ <span data-ttu-id="610b1-111">Ef þú ert ekki með stjórnandaréttindi muntu fá villuboð, *Ekki er hægt að skrifa gögn í eininguna \<entity name\>*.</span><span class="sxs-lookup"><span data-stu-id="610b1-111">If you don't have admin privileges, you will receive an error message, *Unable to write data to entity \<entity name\>*.</span></span> <span data-ttu-id="610b1-112">Í dæminu á eftirfarandi mynd, þú getur ekki búið til viðskiptavinaskrá í forritinu Finance and Operations, vegna þess að tvískipt skrif er stillt, en viðmiðunargögn viðskiptavinahópsins og greiðsluskilmálar eru ekki til Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="610b1-112">In the example in the following illustration, you can't create a customer record in the Finance and Operations app, because dual-write is configured, but the customer group and payment terms reference data don't exist in Common Data Service.</span></span>

    ![Staðfestir Finance and Operations forritatengingu þegar þú hefur ekki stjórnunarréttindi](media/verify_fin_ops_2.png)

<span data-ttu-id="610b1-114">Fyrir upplýsingar um hvernig eigi að laga mál þegar þú býrð til gögn í forriti Finance and Operations, sjá [Úrræðaleita bein samstillingarvandamál](dual-write-troubleshooting-live-sync.md).</span><span class="sxs-lookup"><span data-stu-id="610b1-114">For information about how to fix issues when you create data in Finance and Operations apps, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

## <a name="verify-that-dual-write-is-configured-in-common-data-service"></a><span data-ttu-id="610b1-115">Gakktu úr skugga um að tvískipt skrif sé stillt í Common Data Service</span><span class="sxs-lookup"><span data-stu-id="610b1-115">Verify that dual-write is configured in Common Data Service</span></span>

<span data-ttu-id="610b1-116">Þegar þú býrð til gögn, ef þú sérð reitinn **Fyrirtæki** á síðum í Common Data Service, tvískipt skrif er stillt.</span><span class="sxs-lookup"><span data-stu-id="610b1-116">When you create data, if you see the **Company** field on pages in Common Data Service, dual-write is configured.</span></span>

![Staðfestir Common Data Service tenginguna](media/verify_cds.png)

<span data-ttu-id="610b1-118">Fyrir upplýsingar um hvernig eigi að laga mál þegar þú býrð til gögn í Common Data Service, sjá [Úrræðaleita bein samstillingarvandamál](dual-write-troubleshooting-live-sync.md).</span><span class="sxs-lookup"><span data-stu-id="610b1-118">For information about how to fix issues when you create data in Common Data Service, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

<span data-ttu-id="610b1-119">Fyrir upplýsingar um hvernig á að skoða villuupplýsingar ef þú lendir í villum meðan þú býrð til gögn í Common Data Service, sjáðu [Kveiktu á og skoðaðu rekja innskráningu viðbótarinnar Common Data Service til að skoða villuupplýsingar](dual-write-troubleshooting.md#enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details).</span><span class="sxs-lookup"><span data-stu-id="610b1-119">For information about how to view error details if you encounter any errors while you create data in Common Data Service, see [Enable and view the plug-in trace log in Common Data Service to view error details](dual-write-troubleshooting.md#enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details).</span></span>
