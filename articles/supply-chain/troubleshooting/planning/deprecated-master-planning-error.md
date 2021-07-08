---
title: Villa kemur upp við keyrslu á innbyggðri aðaláætlunarvél
description: Þegar úreld innbyggð aðaláætlunarvél er keyrð koma upp villuboð.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: Dialog_ReqCalcScheduleItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 9c950292a4f43319d21a7deafdfb341b7bef15d8
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294102"
---
# <a name="you-receive-an-error-when-running-the-built-in-master-planning-engine"></a><span data-ttu-id="ce250-103">Villa kemur upp við keyrslu á innbyggðri aðaláætlunarvél</span><span class="sxs-lookup"><span data-stu-id="ce250-103">You receive an error when running the built-in master planning engine</span></span>

<span data-ttu-id="ce250-104">Villukóði: ReqCalcScheduleItemTablePlanningOptimizationFitError</span><span class="sxs-lookup"><span data-stu-id="ce250-104">Error code: ReqCalcScheduleItemTablePlanningOptimizationFitError</span></span>

## <a name="symptoms"></a><span data-ttu-id="ce250-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="ce250-105">Symptoms</span></span>

<span data-ttu-id="ce250-106">Þegar aðaláætlanagerð er keyrð með úreldri innbyggðri aðaláætlunarvél koma upp eftirfarandi villuboð:</span><span class="sxs-lookup"><span data-stu-id="ce250-106">When you run master planning by using the deprecated built-in master planning engine, you receive the following error message:</span></span>

> <span data-ttu-id="ce250-107">Þú færð þessi villuskilaboð vegna þess að innbyggð aðaláætlunarvél var notuð fyrir aðstæður sem eru studdar fínstillingu skipulagningar.</span><span class="sxs-lookup"><span data-stu-id="ce250-107">You receive this error message because the built-in master planning engine was used for scenarios supported by Planning Optimization.</span></span> <span data-ttu-id="ce250-108">Þú ættir að flytja þig yfir í fínstillingu skipulagningar núna, þar sem núverandi aðaláætlanagerð verður úrelt.</span><span class="sxs-lookup"><span data-stu-id="ce250-108">You should migrate to Planning Optimization now, as the current built-in master planning will be deprecated.</span></span> <span data-ttu-id="ce250-109">Athugaðu að þessi áætlanakeyrsla var keyrð.</span><span class="sxs-lookup"><span data-stu-id="ce250-109">Note that this master planning run did complete successfully.</span></span> <span data-ttu-id="ce250-110">Ef flutningurinn þinn inniheldur sterk tengsl um eiginleika sem bíða er hægt að biðja um undantekningu á áframhaldandi notkun á vél fyrir innbyggðri aðaláætlunarvél.</span><span class="sxs-lookup"><span data-stu-id="ce250-110">In case your migration has strong dependencies on pending features, an exception to continued usage of the built-in master planning engine can be requested.</span></span> <span data-ttu-id="ce250-111">Ljúktu við eftirfarandi spurningalista til að hefjast handa og, ef svo á við, biddu um undantekningu frá yfirfærslu í fínstillingu skipulagningar.</span><span class="sxs-lookup"><span data-stu-id="ce250-111">Please complete the following questionnaire to get started and, if relevant, request an exception from migration to Planning Optimization.</span></span> [<span data-ttu-id="ce250-112">Fínstilling áætlanagerðar, yfirfærsla og spurningalisti undantekningar</span><span class="sxs-lookup"><span data-stu-id="ce250-112">Planning Optimization migration and exception questionnaire</span></span>](https://go.microsoft.com/fwlink/?linkid=2144962)

## <a name="cause"></a><span data-ttu-id="ce250-113">Orsök</span><span class="sxs-lookup"><span data-stu-id="ce250-113">Cause</span></span>

<span data-ttu-id="ce250-114">Ef aðaláætlanagerð er keyrð og eiginleikar framleiðslustýringar eru ekki notaðir ættirðu að huga að því að flytja þig yfir í fínstillingu skipulagningar.</span><span class="sxs-lookup"><span data-stu-id="ce250-114">If you run planning and don't use production control features, you should consider migrating to Planning Optimization.</span></span> <span data-ttu-id="ce250-115">Verið er að úrelda innbyggða aðaláætlunarvél.</span><span class="sxs-lookup"><span data-stu-id="ce250-115">The built-in master planning engine is being deprecated.</span></span> <span data-ttu-id="ce250-116">Ef þú vilt halda áfram að nota hana án þess að fá villuboð verður þú að sækja um undanþágu hjá Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ce250-116">Therefore, if you want to continue to use it without receiving the error message, you must apply for an exception from Microsoft.</span></span>

## <a name="resolution"></a><span data-ttu-id="ce250-117">Lausn</span><span class="sxs-lookup"><span data-stu-id="ce250-117">Resolution</span></span>

<span data-ttu-id="ce250-118">Frekari upplýsingar um hvernig á að flytja yfir í fínstillingu skipulagningar eða hvernig á að sækja um undanþágu svo þú getir í staðinn haldið áfram að nota úrelda innbyggða áætlunarvél er að finna í [Flutningur yfir í fínstillingu skipulagningar fyrir aðaláætlanagerð](/dynamics365/supply-chain/master-planning/new-master-planning-engine).</span><span class="sxs-lookup"><span data-stu-id="ce250-118">For more information about how to migrate to Planning Optimization, or how to apply for an exception so that you can continue to use the deprecated built-in planning engine instead, see [Migration to Planning Optimization for master planning](/dynamics365/supply-chain/master-planning/new-master-planning-engine).</span></span>
