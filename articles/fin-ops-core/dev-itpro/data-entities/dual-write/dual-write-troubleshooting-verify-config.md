---
title: Gakktu úr skugga um að tvískipt skrif sé stillt í forritum Finance and Operations og Dataverse
description: Þetta efni útskýrir hvernig þú getur ákvarðað hvort tvískipt skrif eru stillt í forritum Finance and Operations og í Dataverse.
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
ms.openlocfilehash: f389bcf133cc7e6a086167d5e26c1b8795d0fa30
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685540"
---
# <a name="verify-that-dual-write-is-configured-in-finance-and-operations-apps-and-dataverse"></a><span data-ttu-id="d3e7e-103">Gakktu úr skugga um að tvískipt skrif sé stillt í forritum Finance and Operations og Dataverse</span><span class="sxs-lookup"><span data-stu-id="d3e7e-103">Verify that dual-write is configured in Finance and Operations apps and Dataverse</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="d3e7e-104">Þetta efni veitir upplýsingar um úrræðaleit um samþættingu á tvöföldum skrifum á milli forrita Finance and Operations og Dataverse.</span><span class="sxs-lookup"><span data-stu-id="d3e7e-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="d3e7e-105">Einkum útskýrir það hvernig þú getur ákvarðað hvort tvískipt skrif eru stillt í forritum Finance and Operations og í Dataverse.</span><span class="sxs-lookup"><span data-stu-id="d3e7e-105">Specifically, it explains how you can determine whether dual-write is configured in Finance and Operations apps and in Dataverse.</span></span>

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a><span data-ttu-id="d3e7e-106">Gakktu úr skugga um að tvískipt skrif sé stillt í forriti Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d3e7e-106">Verify that dual-write is configured in a Finance and Operations app</span></span>

<span data-ttu-id="d3e7e-107">Til að ákvarða hvort villa sem birtist þegar reynt er að vista línur til að uppfæra eru úr tvöfaldri skráningu skal fyrst staðfesta að tvöföld skráning sé stillt.</span><span class="sxs-lookup"><span data-stu-id="d3e7e-107">To determine whether the errors that you see when you try to save rows for update come from dual-write, first verify that dual-write is configured.</span></span>

+ <span data-ttu-id="d3e7e-108">Ef þú hefur stjórnunarréttindi í forriti Finance and Operations, farðu til **Vinnusvæði \> Gagnastjórnun** og veldu reitinn **Tvöfalt skrif**.</span><span class="sxs-lookup"><span data-stu-id="d3e7e-108">If you have admin privileges in the Finance and Operations app, go to **Workspaces \> Data management**, and select the **Dual-write** tile.</span></span> <span data-ttu-id="d3e7e-109">Ef upplýsingar um tengt umhverfi og lista yfir töflukort sem eru í keyrslu eru birtar er tvöföld skráning stillt.</span><span class="sxs-lookup"><span data-stu-id="d3e7e-109">If the details of the linked environments and the list of table maps that are running are shown, dual-write is configured.</span></span>

    ![Staðfestir Finance and Operations forritatengingu þegar þú hefur stjórnunarréttindi](media/verify_fin_ops_1.png)

+ <span data-ttu-id="d3e7e-111">Ef þú ert ekki með stjórnandaréttindi muntu fá villuboð, *Ekki er hægt að skrifa gögn í eininguna \<entity name\>*.</span><span class="sxs-lookup"><span data-stu-id="d3e7e-111">If you don't have admin privileges, you will receive an error message, *Unable to write data to entity \<entity name\>*.</span></span> <span data-ttu-id="d3e7e-112">Í dæminu á eftirfarandi mynd er ekki hægt að stofna viðskiptamannslínu í Finance and Operations forritinu vegna þess að tvöföld skráning er grunnstillt en viðskiptavinaflokkur og tilvísunargögn greiðsluskilmála eru ekki til í Dataverse.</span><span class="sxs-lookup"><span data-stu-id="d3e7e-112">In the example in the following illustration, you can't create a customer row in the Finance and Operations app, because dual-write is configured, but the customer group and payment terms reference data don't exist in Dataverse.</span></span>

    ![Staðfestir Finance and Operations forritatengingu þegar þú hefur ekki stjórnunarréttindi](media/verify_fin_ops_2.png)

<span data-ttu-id="d3e7e-114">Fyrir upplýsingar um hvernig eigi að laga mál þegar þú býrð til gögn í forriti Finance and Operations, sjá [Úrræðaleita bein samstillingarvandamál](dual-write-troubleshooting-live-sync.md).</span><span class="sxs-lookup"><span data-stu-id="d3e7e-114">For information about how to fix issues when you create data in Finance and Operations apps, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a><span data-ttu-id="d3e7e-115">Gakktu úr skugga um að tvískipt skrif sé stillt í Dataverse</span><span class="sxs-lookup"><span data-stu-id="d3e7e-115">Verify that dual-write is configured in Dataverse</span></span>

<span data-ttu-id="d3e7e-116">Þegar þú býrð til gögn, ef þú sérð reitinn **Fyrirtæki** á síðum í Dataverse, tvískipt skrif er stillt.</span><span class="sxs-lookup"><span data-stu-id="d3e7e-116">When you create data, if you see the **Company** field on pages in Dataverse, dual-write is configured.</span></span>

![Staðfestir Dataverse tenginguna](media/verify_cds.png)

<span data-ttu-id="d3e7e-118">Fyrir upplýsingar um hvernig eigi að laga mál þegar þú býrð til gögn í Dataverse, sjá [Úrræðaleita bein samstillingarvandamál](dual-write-troubleshooting-live-sync.md).</span><span class="sxs-lookup"><span data-stu-id="d3e7e-118">For information about how to fix issues when you create data in Dataverse, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

<span data-ttu-id="d3e7e-119">Fyrir upplýsingar um hvernig á að skoða villuupplýsingar ef þú lendir í villum meðan þú býrð til gögn í Dataverse, sjáðu [Kveiktu á og skoðaðu rekja innskráningu viðbótarinnar Dataverse til að skoða villuupplýsingar](dual-write-troubleshooting.md#enable-view-trace).</span><span class="sxs-lookup"><span data-stu-id="d3e7e-119">For information about how to view error details if you encounter any errors while you create data in Dataverse, see [Enable and view the plug-in trace log in Dataverse to view error details](dual-write-troubleshooting.md#enable-view-trace).</span></span>
