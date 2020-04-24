---
title: Tilkynna framleiðslupöntun sem lokna
description: Þessi verklýsing sýnir hvernig á að skrá framleiðslupöntunina sem tilbúna.
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdParmReportFinished, ProdJournalTransProd
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: def39fa86103bc69d1c88dde8d0660945c1de82e
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210549"
---
# <a name="report-a-production-order-as-finished"></a><span data-ttu-id="25adc-103">Tilkynna framleiðslupöntun sem lokna</span><span class="sxs-lookup"><span data-stu-id="25adc-103">Report a production order as finished</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="25adc-104">Þessi verklýsing sýnir hvernig á að skrá framleiðslupöntunina sem tilbúna.</span><span class="sxs-lookup"><span data-stu-id="25adc-104">This procedure shows how to report a production order as finished.</span></span> <span data-ttu-id="25adc-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="25adc-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="25adc-106">Þetta er sjötta ferli úr sjö sem útskýrir lífsferil framleiðslupöntunar.</span><span class="sxs-lookup"><span data-stu-id="25adc-106">This is the sixth procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="report-a-production-order-as-finished"></a><span data-ttu-id="25adc-107">Tilkynna framleiðslupöntun sem lokna</span><span class="sxs-lookup"><span data-stu-id="25adc-107">Report a production order as finished</span></span>
1. <span data-ttu-id="25adc-108">Fara í Framleiðslustýringar > Framleiðslupantanir > Allar framleiðslupantanir.</span><span class="sxs-lookup"><span data-stu-id="25adc-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="25adc-109">Veljið framleiðslupöntun sem hefur stöðuna Hafið.</span><span class="sxs-lookup"><span data-stu-id="25adc-109">Select a production order that has the Started status.</span></span>  
2. <span data-ttu-id="25adc-110">Smellið á „Framleiðslupöntun“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="25adc-110">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="25adc-111">Smellið á „Bóka sem tilbúið“.</span><span class="sxs-lookup"><span data-stu-id="25adc-111">Click Report as finished.</span></span>
    * <span data-ttu-id="25adc-112">Á þessari síðu er hægt að staðfesta magn lokinnar vöru til að skrá sem tilbúna.</span><span class="sxs-lookup"><span data-stu-id="25adc-112">On this page, you can confirm the quantity of the finished product to be reported as finished.</span></span>  
4. <span data-ttu-id="25adc-113">Smellið á flipann „Almennt“.</span><span class="sxs-lookup"><span data-stu-id="25adc-113">Click the General tab.</span></span>
5. <span data-ttu-id="25adc-114">Setja Gallalaust magn á '18'.</span><span class="sxs-lookup"><span data-stu-id="25adc-114">Set Good quantity to '18'.</span></span>
6. <span data-ttu-id="25adc-115">Setja Gallað magn á "2".</span><span class="sxs-lookup"><span data-stu-id="25adc-115">Set Error quantity to '2'.</span></span>
7. <span data-ttu-id="25adc-116">Í ástæða Villu svæðinu, veljið 'Efni'.</span><span class="sxs-lookup"><span data-stu-id="25adc-116">In the Error cause field, select 'Material'.</span></span>
8. <span data-ttu-id="25adc-117">Veldu eða hreinsaðu gátreitinn Ljúka vinnslu.</span><span class="sxs-lookup"><span data-stu-id="25adc-117">Select or clear the End job check box.</span></span>
9. <span data-ttu-id="25adc-118">Veldu eða hreinsaðu gátreitinn Samþykkja Villu.</span><span class="sxs-lookup"><span data-stu-id="25adc-118">Select or clear the Accept error check box.</span></span>
10. <span data-ttu-id="25adc-119">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="25adc-119">Click OK.</span></span>

## <a name="verify-the-report-as-finished-journal"></a><span data-ttu-id="25adc-120">Staðfesta færslubók bóka sem tilbúið</span><span class="sxs-lookup"><span data-stu-id="25adc-120">Verify the Report as finished journal</span></span>
1. <span data-ttu-id="25adc-121">Smellið á „Skoða“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="25adc-121">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="25adc-122">Smellið á Bókað sem tilbúið.</span><span class="sxs-lookup"><span data-stu-id="25adc-122">Click Reported as finished.</span></span>
3. <span data-ttu-id="25adc-123">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="25adc-123">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="25adc-124">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="25adc-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="25adc-125">Bóka sem tilbúið færslubók er bókuð.</span><span class="sxs-lookup"><span data-stu-id="25adc-125">The Report as finished journal is posted.</span></span> <span data-ttu-id="25adc-126">Ef óskað er að leiðrétta færslubókina handvirkt er hægt að stofna nýja færslubók þar sem hægt er að gera breytingar.</span><span class="sxs-lookup"><span data-stu-id="25adc-126">If you want to make adjustments to the journal, you can manually create  a new journal where you can make changes.</span></span>  

