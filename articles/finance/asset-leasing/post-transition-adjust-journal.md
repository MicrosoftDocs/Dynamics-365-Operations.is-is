---
title: Bóka færslur umbreytingar leiðréttingarbókar í eignarleigu
description: Þetta efnisatriði lýsir virkninni sem gerir þér kleift að umbreyta safni leigusamninga í nýjar bókhaldsreglur um leigusamninga, efnisatriði um skráningarkerfi reikningsskilastaðla 842 (ASC 842) og alþjóðlegan reikningsskilastaðal 16 (IFRS 16).
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 51ae41e22507d77f32b8b0f4685cce797fd19cff
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969554"
---
# <a name="post-transition-adjustment-journal-entries-in-asset-leasing"></a><span data-ttu-id="8f48a-103">Bóka færslur umbreytingar leiðréttingarbókar í eignarleigu</span><span class="sxs-lookup"><span data-stu-id="8f48a-103">Post transition adjustment journal entries in Asset leasing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8f48a-104">Þetta efnisatriði lýsir virkninni sem gerir þér kleift að umbreyta safni leigusamninga í nýjar bókhaldsreglur um leigusamninga: Efnisatriði um skráningarkerfi reikningsskilastaðla 842 (ASC 842) sem er staðall fyrir almennt samþykktar reikningsskilareglur í Bandaríkjunum (US GAAP) og alþjóðlegan reikningsskilastaðal 16 (IFRS 16).</span><span class="sxs-lookup"><span data-stu-id="8f48a-104">This topic describes the functionality that lets you transition a lease portfolio to the new lease accounting standards: Accounting Standards Codification Topic 842 (ASC 842), which is the standard in Generally Accepted Accounting Principles in the US (US GAAP), and International Financial Reporting Standard 16 (IFRS 16).</span></span>

<span data-ttu-id="8f48a-105">Frekari upplýsingar um hvernig á að setja upp bók til umbreytingar í nýju staðlana að finna í [Setja upp leigubækur](set-up-lease-books.md).</span><span class="sxs-lookup"><span data-stu-id="8f48a-105">For information about how to set up a book for the transition to the new standards, see [Set up lease books](set-up-lease-books.md).</span></span>

<span data-ttu-id="8f48a-106">Þegar stofnuð er færsla umbreytingar leiðréttingabókar er bókarfærsla stofnuð.</span><span class="sxs-lookup"><span data-stu-id="8f48a-106">When you create a transition adjustment journal entry, a journal entry is generated.</span></span> <span data-ttu-id="8f48a-107">Þessi færsla endurspeglar áhrif efnahagsreiknings með því að skrá leigusamninginn samkvæmt nýjum stöðlunum á þeirri dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="8f48a-107">This entry reflects the balance sheet impact of recording the lease under the new standards on that date.</span></span> <span data-ttu-id="8f48a-108">Viðeigandi eignalykill er debetfærður fyrir bókfært virði á þeirri dagsetningu og skuldalykillinn er kreditfærður.</span><span class="sxs-lookup"><span data-stu-id="8f48a-108">The appropriate asset account is debited for the carrying amount on that date, and the liability account is credited.</span></span> <span data-ttu-id="8f48a-109">Mismunurinn er annaðhvort debetfærður eða kreditfærður í óráðstafað eigið fé.</span><span class="sxs-lookup"><span data-stu-id="8f48a-109">The difference is either debited or credited to retained earnings.</span></span>

<span data-ttu-id="8f48a-110">Til að bóka leiðréttingu umbreytingar samkvæmt nýju bókhaldsstöðlunum skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="8f48a-110">To post a transition adjustment in compliance with the new accounting standards, follow these steps.</span></span>

1. <span data-ttu-id="8f48a-111">Á síðunni **Samantekt leigu** skal velja leiguna og síðan **Bækur**.</span><span class="sxs-lookup"><span data-stu-id="8f48a-111">On the **Lease summary** page, select the lease, and then select **Books**.</span></span>
2. <span data-ttu-id="8f48a-112">Í bókinni skal velja **Greiðsluáætlun**.</span><span class="sxs-lookup"><span data-stu-id="8f48a-112">In the book, select **Payment schedule**.</span></span>
3. <span data-ttu-id="8f48a-113">Í svarglugganum **Greiðsluáætlun** skal velja **Staðfesta**.</span><span class="sxs-lookup"><span data-stu-id="8f48a-113">In the **Payment schedule** dialog box, select **Confirm**.</span></span> <span data-ttu-id="8f48a-114">Lokið svo svarglugganum.</span><span class="sxs-lookup"><span data-stu-id="8f48a-114">Then close the dialog box.</span></span>
4. <span data-ttu-id="8f48a-115">Veljið **Leiðrétting umbreytingar**.</span><span class="sxs-lookup"><span data-stu-id="8f48a-115">Select **Transition adjustment**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8f48a-116">Aðeins er hægt að stofna leiðréttingu umbreytingar fyrir leigubækur sem er úthlutað á bók þar sem svæðið **Umbreytingarbók** er tiltækt.</span><span class="sxs-lookup"><span data-stu-id="8f48a-116">A transition adjustment can be created only for lease books that are assigned to a book where the **Transition book** field is available.</span></span> <span data-ttu-id="8f48a-117">Ef gildið í svæðinu **Upphafsdagsetning leigusamnings** er síðar en umbreytingardagsetningin verður gildið í svæðinu **Leiðrétting umbreytingar** ekki uppfært.</span><span class="sxs-lookup"><span data-stu-id="8f48a-117">If the value in the **Lease commencement** field is later than the transition date, the value in the **Transition adjustment** field won't be updated.</span></span>

5. <span data-ttu-id="8f48a-118">Til að skoða bókarfærsluna skal velja **Færslubækur eignarleigu**.</span><span class="sxs-lookup"><span data-stu-id="8f48a-118">To view the journal entry, select **Asset leasing journals**.</span></span>
6. <span data-ttu-id="8f48a-119">Veldu nýja bók og veldu síðan **Bóka**.</span><span class="sxs-lookup"><span data-stu-id="8f48a-119">Select the new journal, and then select **Post**.</span></span>
