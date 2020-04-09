---
title: Stofna uppsöfnunarskemu
description: Í þessu efnisatriði er útskýrt hvernig á að stofna uppsöfnunarskema.
author: aprilolson
manager: AnnBe
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAccrualTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a83870c4cec4de2e51e90ff1889d4beff6c23f95
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145194"
---
# <a name="create-accrual-schemes"></a><span data-ttu-id="37d1e-103">Stofna uppsöfnunarskemu</span><span class="sxs-lookup"><span data-stu-id="37d1e-103">Create accrual schemes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="37d1e-104">Í þessu efnisatriði er útskýrt hvernig á að stofna uppsöfnunarskema.</span><span class="sxs-lookup"><span data-stu-id="37d1e-104">This topic explains how to create an accrual scheme.</span></span> <span data-ttu-id="37d1e-105">Þetta verkefni notar USMF-sýnifyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="37d1e-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="37d1e-106">Farðu í **skoðunarrúðuna > Kerfiseiningar > Fjárhagur > Færslubókaruppsetning > Uppsöfnunarskemu**.</span><span class="sxs-lookup"><span data-stu-id="37d1e-106">Go to **Navigation pane > Modules > General ledger > Journal setup > Accrual schemes**.</span></span>
2. <span data-ttu-id="37d1e-107">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="37d1e-107">Select **New**.</span></span>
3. <span data-ttu-id="37d1e-108">Í reitinn **Auðkenning uppsöfnunar** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="37d1e-108">In the **Accrual identification** field, type a value.</span></span>
4. <span data-ttu-id="37d1e-109">Í reitnum **Lýsing á uppsöfnunarskema** skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="37d1e-109">In the **Description of accrual scheme** field, type a value.</span></span>
5. <span data-ttu-id="37d1e-110">Í reitnum **Debet** skal tilgreina gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="37d1e-110">In the **Debit** field, specify the desired values.</span></span> <span data-ttu-id="37d1e-111">Skilgreindur aðallykill mun skipta út aðallykli debets í línu færslubókarfylgiskjals og hann verður einnig notaður fyrir bakfærslu á frestun sem byggir á uppsöfnunarfærslum fjárhags.</span><span class="sxs-lookup"><span data-stu-id="37d1e-111">The main account defined will replace the debit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
6. <span data-ttu-id="37d1e-112">Í reitnum **Kredit** skal tilgreina gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="37d1e-112">In the **Credit** field, specify the desired values.</span></span> <span data-ttu-id="37d1e-113">Skilgreindur aðallykill mun skipta út aðallykli kredits í línu færslubókarfylgiskjals og hann verður einnig notaður fyrir bakfærslu á frestun sem byggir á uppsöfnunarfærslum fjárhags.</span><span class="sxs-lookup"><span data-stu-id="37d1e-113">The main account defined will replace the credit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
7. <span data-ttu-id="37d1e-114">Í reitnum **Fylgiskjal** skal velja hvernig það á að ákvarða fylgiskjal þegar færslur eru bókaðar.</span><span class="sxs-lookup"><span data-stu-id="37d1e-114">In the **Voucher** field, select how you want the voucher determined when the transactions are posted.</span></span>
8. <span data-ttu-id="37d1e-115">Í reitnum **Lýsing** skal færa inn gildi til að lýsa færslunum sem verða bókaðar.</span><span class="sxs-lookup"><span data-stu-id="37d1e-115">In the **Description** field, type a value to describe the transactions that will be posted.</span></span>
9. <span data-ttu-id="37d1e-116">Í reitnum **Tímabilstíðni** skal velja hversu oft færslur eiga að eiga sér stað.</span><span class="sxs-lookup"><span data-stu-id="37d1e-116">In the **Period frequency** field, select how often the transactions should occur.</span></span>
10. <span data-ttu-id="37d1e-117">Í reitnum **Fjöldi tilvika eftir tímabilum** skal færa inn tölu.</span><span class="sxs-lookup"><span data-stu-id="37d1e-117">In the **Number of occurrences by period** field, enter a number.</span></span>
11. <span data-ttu-id="37d1e-118">Í reitnum **Bóka færslur** skal velja hvenær bóka skal færslur, eins og **Mánaðarlega**.</span><span class="sxs-lookup"><span data-stu-id="37d1e-118">In the **Post transactions** field, select when the transactions should be posted, such as **Monthly**.</span></span>

