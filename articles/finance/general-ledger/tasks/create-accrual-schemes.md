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
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 457be741dfd3b44cb963db37857d6a7bceecc14e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994666"
---
# <a name="create-accrual-schemes"></a><span data-ttu-id="d4d12-103">Stofna uppsöfnunarskemu</span><span class="sxs-lookup"><span data-stu-id="d4d12-103">Create accrual schemes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d4d12-104">Í þessu efnisatriði er útskýrt hvernig á að stofna uppsöfnunarskema.</span><span class="sxs-lookup"><span data-stu-id="d4d12-104">This topic explains how to create an accrual scheme.</span></span> <span data-ttu-id="d4d12-105">Þetta verkefni notar USMF-sýnifyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="d4d12-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="d4d12-106">Farðu í **skoðunarrúðuna > Kerfiseiningar > Fjárhagur > Færslubókaruppsetning > Uppsöfnunarskemu**.</span><span class="sxs-lookup"><span data-stu-id="d4d12-106">Go to **Navigation pane > Modules > General ledger > Journal setup > Accrual schemes**.</span></span>
2. <span data-ttu-id="d4d12-107">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="d4d12-107">Select **New**.</span></span>
3. <span data-ttu-id="d4d12-108">Í reitinn **Auðkenning uppsöfnunar** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="d4d12-108">In the **Accrual identification** field, type a value.</span></span>
4. <span data-ttu-id="d4d12-109">Í reitnum **Lýsing á uppsöfnunarskema** skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="d4d12-109">In the **Description of accrual scheme** field, type a value.</span></span>
5. <span data-ttu-id="d4d12-110">Í reitnum **Debet** skal tilgreina gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="d4d12-110">In the **Debit** field, specify the desired values.</span></span> <span data-ttu-id="d4d12-111">Skilgreindur aðallykill mun skipta út aðallykli debets í línu færslubókarfylgiskjals og hann verður einnig notaður fyrir bakfærslu á frestun sem byggir á uppsöfnunarfærslum fjárhags.</span><span class="sxs-lookup"><span data-stu-id="d4d12-111">The main account defined will replace the debit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
6. <span data-ttu-id="d4d12-112">Í reitnum **Kredit** skal tilgreina gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="d4d12-112">In the **Credit** field, specify the desired values.</span></span> <span data-ttu-id="d4d12-113">Skilgreindur aðallykill mun skipta út aðallykli kredits í línu færslubókarfylgiskjals og hann verður einnig notaður fyrir bakfærslu á frestun sem byggir á uppsöfnunarfærslum fjárhags.</span><span class="sxs-lookup"><span data-stu-id="d4d12-113">The main account defined will replace the credit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
7. <span data-ttu-id="d4d12-114">Í reitnum **Fylgiskjal** skal velja hvernig það á að ákvarða fylgiskjal þegar færslur eru bókaðar.</span><span class="sxs-lookup"><span data-stu-id="d4d12-114">In the **Voucher** field, select how you want the voucher determined when the transactions are posted.</span></span>
8. <span data-ttu-id="d4d12-115">Í reitnum **Lýsing** skal færa inn gildi til að lýsa færslunum sem verða bókaðar.</span><span class="sxs-lookup"><span data-stu-id="d4d12-115">In the **Description** field, type a value to describe the transactions that will be posted.</span></span>
9. <span data-ttu-id="d4d12-116">Í reitnum **Tímabilstíðni** skal velja hversu oft færslur eiga að eiga sér stað.</span><span class="sxs-lookup"><span data-stu-id="d4d12-116">In the **Period frequency** field, select how often the transactions should occur.</span></span>
10. <span data-ttu-id="d4d12-117">Í reitnum **Fjöldi tilvika eftir tímabilum** skal færa inn tölu.</span><span class="sxs-lookup"><span data-stu-id="d4d12-117">In the **Number of occurrences by period** field, enter a number.</span></span>
11. <span data-ttu-id="d4d12-118">Í reitnum **Bóka færslur** skal velja hvenær bóka skal færslur, eins og **Mánaðarlega**.</span><span class="sxs-lookup"><span data-stu-id="d4d12-118">In the **Post transactions** field, select when the transactions should be posted, such as **Monthly**.</span></span>

