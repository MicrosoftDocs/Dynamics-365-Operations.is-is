---
title: Virkja Power BI fyrir altækt birgðabókhald
description: Þetta efnisatriði lýsir hvernig á að virkja Microsoft Power BI fyrir altækt birgðabókhald.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d7979ed18b98ee6133774cd91bc866d6fca92d5f
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273173"
---
# <a name="enable-power-bi-for-global-inventory-accounting"></a><span data-ttu-id="13e41-103">Virkja Power BI fyrir altækt birgðabókhald</span><span class="sxs-lookup"><span data-stu-id="13e41-103">Enable Power BI for Global Inventory Accounting</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="13e41-104">Hægt er að festa reiti, yfirlit og skýrslur af reikningnum þínum á [PowerBI.com](https://powerbi.com/) á vinnusvæðið þitt hjá Microsoft Dynamics 365 forritum.</span><span class="sxs-lookup"><span data-stu-id="13e41-104">You can pin tiles, dashboards, and reports from your [PowerBI.com](https://powerbi.com/) account to your Microsoft Dynamics 365 application workspace.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="13e41-105">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="13e41-105">Prerequisites</span></span>

<span data-ttu-id="13e41-106">Eftirfarandi skilyrði verða að vera til staðar áður en hægt er að virkja Power BI skýrslugjöf:</span><span class="sxs-lookup"><span data-stu-id="13e41-106">The following prerequisites must be in place before you can enable Power BI reporting:</span></span>

- <span data-ttu-id="13e41-107">Þú verður að vera kerfisstjóri í Dynamics 365-forritinu.</span><span class="sxs-lookup"><span data-stu-id="13e41-107">You must be a system administrator in the Dynamics 365 application.</span></span>
- <span data-ttu-id="13e41-108">Nauðsynlegt er að vera með reikning hjá [PowerBI.com](https://powerbi.com/).</span><span class="sxs-lookup"><span data-stu-id="13e41-108">You must have a [PowerBI.com](https://powerbi.com/) account.</span></span>
- <span data-ttu-id="13e41-109">Nauðsynlegt er að vera með a.m.k. eitt yfirlit og eina skýrslu á Power BI-reikningnum.</span><span class="sxs-lookup"><span data-stu-id="13e41-109">You must have at least one dashboard and one report in your Power BI account.</span></span>
- <span data-ttu-id="13e41-110">Nauðsynlegt er að vera stjórnandi fyrir Azure Active Directory (Azure AD) reikninginn.</span><span class="sxs-lookup"><span data-stu-id="13e41-110">You must be an administrator for your Azure Active Directory (Azure AD) account.</span></span>
- <span data-ttu-id="13e41-111">Lénið Azure AD verður að vera sama lénið og þú notaðir fyrir [PowerBI.com](https://powerbi.com/) reikninginn.</span><span class="sxs-lookup"><span data-stu-id="13e41-111">The Azure AD domain must be the same domain that you used for your [PowerBI.com](https://powerbi.com/) account.</span></span>

## <a name="setup"></a><span data-ttu-id="13e41-112">Setja upp</span><span class="sxs-lookup"><span data-stu-id="13e41-112">Setup</span></span>

<span data-ttu-id="13e41-113">Fylgið þessum skrefum til að setja upp Power BI-samþættingu.</span><span class="sxs-lookup"><span data-stu-id="13e41-113">To set up the Power BI integration, follow these steps.</span></span>

1. <span data-ttu-id="13e41-114">Skráðu þig inn í [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).</span><span class="sxs-lookup"><span data-stu-id="13e41-114">Sign in to [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).</span></span>
1. <span data-ttu-id="13e41-115">Farið í **Samnýtt eignasafn**, veljið **Power BI skýrslulíkan** sem eignagerðina og sækið pakkann **Altækt birgðabókhald**.</span><span class="sxs-lookup"><span data-stu-id="13e41-115">Go to **Shared asset library**, select **Power BI report model** as the asset type, and download the **Global Inventory Accounting** package.</span></span> 
1. <span data-ttu-id="13e41-116">Skráið ykkur inn á [PowerBI.com](https://app.powerbi.com/) og hlaðið upp **Altæku birgðabókhaldi** Power BI skýrsluskrá með því að fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="13e41-116">Sign in to [PowerBI.com](https://app.powerbi.com/), and upload the **Global Inventory Accounting** Power BI report file by following these steps:</span></span>

    1. <span data-ttu-id="13e41-117">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="13e41-117">Select **New**.</span></span>
    1. <span data-ttu-id="13e41-118">Veljið **Hlaða upp skrá**.</span><span class="sxs-lookup"><span data-stu-id="13e41-118">Select **Upload a file**.</span></span>
    1. <span data-ttu-id="13e41-119">Veljið **Altækt birgðabókhald** Power BI skýrsluskrá.</span><span class="sxs-lookup"><span data-stu-id="13e41-119">Select the **Global Inventory Accounting** Power BI report file.</span></span>

1. <span data-ttu-id="13e41-120">Stillið **Altækt birgðabókhald** Power BI skýrslu með því að fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="13e41-120">Configure the **Global Inventory Accounting** Power BI report by following these steps:</span></span>

    1. <span data-ttu-id="13e41-121">Farið á **Vinnusvæðið mitt**, finnið gagnasafnið fyrir altækt birgðabókhald og síðan í valmyndinni **Valkostir** skal velja **Stillingar**.</span><span class="sxs-lookup"><span data-stu-id="13e41-121">Go to **My workspace**, find the dataset for Global Inventory Accounting, and then, on the **Options** menu, select **Settings**.</span></span>
    1. <span data-ttu-id="13e41-122">Í **Stillingar fyrir altækt birgðabókhald** skal víkka út **Færibreytur** og uppfæra allar færibreytur eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="13e41-122">In **Settings for Global inventory accounting**, expand **Parameters**, and update all parameters as required.</span></span>

1. <span data-ttu-id="13e41-123">Skrá forritið eins og lýst er í [Stilla PowerBI.com samþættingu](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md#registration-process).</span><span class="sxs-lookup"><span data-stu-id="13e41-123">Register the application as described in [Configure PowerBI.com integration](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md#registration-process).</span></span>
1. <span data-ttu-id="13e41-124">Samþættið **Altækt birgðabókhald** Power BI skýrsluskrá við Dynamics 365 Supply Chain Management með því að fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="13e41-124">Integrate the **Global Inventory Accounting** Power BI report file into Dynamics 365 Supply Chain Management by following these steps:</span></span>

    1. <span data-ttu-id="13e41-125">Farið í **Kerfisstjórnun \> Uppsetning \> Skilgreining PowerBI.com**.</span><span class="sxs-lookup"><span data-stu-id="13e41-125">Go to **System administration \> Setup \> PowerBI.com configuration**.</span></span>
    1. <span data-ttu-id="13e41-126">Veljið **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="13e41-126">Select **Edit**.</span></span>
    1. <span data-ttu-id="13e41-127">Veldu **Gera PowerBI.com-samþættingu virka**.</span><span class="sxs-lookup"><span data-stu-id="13e41-127">Select **Enable PowerBI.Com integration**.</span></span>
    1. <span data-ttu-id="13e41-128">Í reitinn **Kenni forrits** skal slá inn kenni forrits.</span><span class="sxs-lookup"><span data-stu-id="13e41-128">In the **Application ID** field, enter the application ID.</span></span>
    1. <span data-ttu-id="13e41-129">Í reitinn **Forritslykill** skal slá inn lykil forrits.</span><span class="sxs-lookup"><span data-stu-id="13e41-129">In the **Application key** field, enter the application key.</span></span>
    1. <span data-ttu-id="13e41-130">Veldu **Vista**.</span><span class="sxs-lookup"><span data-stu-id="13e41-130">Select **Save**.</span></span>

1. <span data-ttu-id="13e41-131">Endurhlaðið síðunni þannig að innskráningargluggi Power BI birtist.</span><span class="sxs-lookup"><span data-stu-id="13e41-131">Refresh the page so that the Power BI sign-in dialog box appears.</span></span>
1. <span data-ttu-id="13e41-132">Í flipanum **Valkostir** skal velja **Opna skýrslulista** og síðan velja **Altækt birgðabókhald** Power BI skýrsluskrá sem var hlaðin upp hér áður.</span><span class="sxs-lookup"><span data-stu-id="13e41-132">On the **Options** tab, select **Open report catalog**, and then select the **Global Inventory Accounting** Power BI report file that you uploaded earlier.</span></span>
1. <span data-ttu-id="13e41-133">Endurhlaðið síðuna.</span><span class="sxs-lookup"><span data-stu-id="13e41-133">Refresh the page.</span></span> <span data-ttu-id="13e41-134">Þú ættir að sjá að skýrslunni hefur verið bætt við.</span><span class="sxs-lookup"><span data-stu-id="13e41-134">You should see that your report has been added.</span></span>
1. <span data-ttu-id="13e41-135">Undir **Power BI skýrslur** skal velja tengilinn **Altækt birgðabókhald**.</span><span class="sxs-lookup"><span data-stu-id="13e41-135">Under **Power BI reports**, select the **Global Inventory Accounting** link.</span></span>

<span data-ttu-id="13e41-136">Frekari upplýsingar er að finna í [Skilgreina samþættingu PowerBI.com](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md).</span><span class="sxs-lookup"><span data-stu-id="13e41-136">For more information, see [Configure PowerBI.com integration](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md).</span></span>
