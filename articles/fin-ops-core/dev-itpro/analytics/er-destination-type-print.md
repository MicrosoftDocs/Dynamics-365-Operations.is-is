---
title: Prentari ER-gerð áfangastaðar
description: Þetta efni útskýrir hvernig þú getur stillt áfangastað prentara fyrir hvern FOLDER eða FILE hluti á rafrænu skýrslugerðarsniðinu (ER) sem er stillt til að búa til skjöl á útleið í annaðhvort PDF eða Microsoft Office snið (Excel\Word).
author: NickSelin
manager: AnnBe
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: b7a279dcb30e7681ae654ab17d898a5364391d57
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679607"
---
# <a name="printer-destination"></a><a name="PrinterDestinationType"></a><span data-ttu-id="f3984-103">Áfangastaður prentara</span><span class="sxs-lookup"><span data-stu-id="f3984-103">Printer destination</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f3984-104">Þú getur sent skjal sem myndað er beint til netprentara til beinnar prentunar.</span><span class="sxs-lookup"><span data-stu-id="f3984-104">You can send a generated document directly to a network printer for direct printing.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f3984-105">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="f3984-105">Prerequisites</span></span>

<span data-ttu-id="f3984-106">Áður en þú byrjar verður þú að setja upp og stilla skjalaleiðslumiðlun og skrá síðan netprentara.</span><span class="sxs-lookup"><span data-stu-id="f3984-106">Before you begin, you must install and configure the Document Routing Agent, and then register the network printers.</span></span> <span data-ttu-id="f3984-107">Nánari upplýsingar er að finna í [Setja upp eftirlitsbúnað skjalasendingar til að virkja nettengda prentun](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent).</span><span class="sxs-lookup"><span data-stu-id="f3984-107">For more information, see [Install the Document Routing Agent to enable network printing](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent).</span></span>

## <a name="make-the-printer-destination-available"></a><span data-ttu-id="f3984-108">Gerðu prentaramiðstöðina tiltækan</span><span class="sxs-lookup"><span data-stu-id="f3984-108">Make the Printer destination available</span></span>

<span data-ttu-id="f3984-109">Til að gera **Prentari** ákvörðunarstaður í boði í núverandi tilviki Microsoft Dynamics 365 Finance, farðu á vinnusvæði **Stjórnun eiginleika** og kveiktu á eftirfarandi aðgerðum, í þessari röð:</span><span class="sxs-lookup"><span data-stu-id="f3984-109">To make the **Printer** destination available in the current instance of Microsoft Dynamics 365 Finance, go to the **Feature management** workspace, and turn on the following features, in this order:</span></span>

1. <span data-ttu-id="f3984-110">Umbreyta fylgiskjölum rafrænnar skýrslugerðar á útleið úr Microsoft Office-sniði í PDF</span><span class="sxs-lookup"><span data-stu-id="f3984-110">Convert Electronic Reporting outbound documents from Microsoft Office formats to PDF</span></span>
2. <span data-ttu-id="f3984-111">Miðlari skjalasendingar sem viðtökustaður rafrænnar skýrslugerðar fyrir fylgiskjöl á útleið</span><span class="sxs-lookup"><span data-stu-id="f3984-111">Document Routing Agent as Electronic Reporting destination for outbound documents</span></span>

<span data-ttu-id="f3984-112">[![Kveiktu á ákvörðunarstað ER prentara í Stjórnun eiginleika](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span><span class="sxs-lookup"><span data-stu-id="f3984-112">[![Turning on the ER printer destination feature in Feature management](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span></span>

### <a name="applicability"></a><span data-ttu-id="f3984-113">Gildissvið</span><span class="sxs-lookup"><span data-stu-id="f3984-113">Applicability</span></span>

<span data-ttu-id="f3984-114">Ákvörðunarstað **Prentara** er aðeins hægt að stilla áfangastað fyrir skráhluta sem eru notaðir til að búa til framleiðsla á annaðhvort prentvænu PDF sniði (PDF samruna eða PDF skráarsniðsþátta) eða Microsoft Office Excel/Word snið (Excel skjal).</span><span class="sxs-lookup"><span data-stu-id="f3984-114">The **Printer** destination can be configured only for file components that are used to generate output in either printable PDF format (PDF Merger or PDF file format elements) or Microsoft Office Excel/Word format (Excel file).</span></span> <span data-ttu-id="f3984-115">Þegar úttak hefur verið myndað á PDF sniði er það sent til prentara.</span><span class="sxs-lookup"><span data-stu-id="f3984-115">When output is generated in PDF format, it's sent to a printer.</span></span> <span data-ttu-id="f3984-116">Þegar úttak er myndað á Microsoft Office-sniði er því sjálfkrafa breytt í PDF-snið og síðan sent til prentara.</span><span class="sxs-lookup"><span data-stu-id="f3984-116">When output is generated in Microsoft Office format, it's automatically converted to PDF format and then sent to a printer.</span></span>

### <a name="limitations"></a><span data-ttu-id="f3984-117">Takmarkanir</span><span class="sxs-lookup"><span data-stu-id="f3984-117">Limitations</span></span>

<span data-ttu-id="f3984-118">Þessi eiginleiki er forsýningaraðgerð og er háð þeim notkunarskilmálum sem lýst er í [Viðbótarskilmálar notkunar fyrir Microsoft Dynamics 365 Forskoðanir](https://go.microsoft.com/fwlink/?linkid=2105274).</span><span class="sxs-lookup"><span data-stu-id="f3984-118">This feature is a preview feature and is subject to the terms of use that are described in [Supplemental Terms of Use for Microsoft Dynamics 365 Previews](https://go.microsoft.com/fwlink/?linkid=2105274).</span></span>

<span data-ttu-id="f3984-119">Ákvörðunarstaður **Prentara** er aðeins útfærður fyrir skýjadreifingar.</span><span class="sxs-lookup"><span data-stu-id="f3984-119">The **Printer** destination is implemented only for cloud deployments.</span></span>

### <a name="use-the-printer-destination"></a><span data-ttu-id="f3984-120">Nota viðtökustað prentara</span><span class="sxs-lookup"><span data-stu-id="f3984-120">Use the Printer destination</span></span>

1. <span data-ttu-id="f3984-121">Stilltu valkostinn **Virkt** á **Já** til að senda myndað skjal til prentara.</span><span class="sxs-lookup"><span data-stu-id="f3984-121">Set the **Enabled** option to **Yes** to send a generated document to a printer.</span></span>
2. <span data-ttu-id="f3984-122">Í reitinn **Heiti prentara** velurðu nauðsynlegan netprentara.</span><span class="sxs-lookup"><span data-stu-id="f3984-122">In the **Printer name** field, select the required network printer.</span></span>
3. <span data-ttu-id="f3984-123">Stilltu valkostinn **Vista á prentskjalasafni?** á **Já** til að geyma myndaða framleiðsluna í skjalasafninu, svo að hann sé tiltækur til frekari prentunar.</span><span class="sxs-lookup"><span data-stu-id="f3984-123">Set the **Save in print archive?** option to **Yes** to store the generated output in the print archive, so that it's available for further printing.</span></span> <span data-ttu-id="f3984-124">Til að fá aðgang í geymsluframleiðslu síðar, farðu til **Fyrirtækisstjórnun** \> **Fyrirspurnir og skýrslur** \> **Skýrsluskjalasafn**.</span><span class="sxs-lookup"><span data-stu-id="f3984-124">To access archived output later, go to **Organization administration** \> **Inquiries and reports** \> **Report archive**.</span></span>

<span data-ttu-id="f3984-125">[![Notkun á viðtökustað prentara](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span><span class="sxs-lookup"><span data-stu-id="f3984-125">[![Using the Printer destination](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span></span>

> [!NOTE]
> <span data-ttu-id="f3984-126">Ekki þarf að vera kveikt á valkostinum **Umbreyta í PDF** þegar þú stillir ákvörðunarstað **Prentara**.</span><span class="sxs-lookup"><span data-stu-id="f3984-126">The **Convert to PDF** option doesn't have to be turned on when you configure the **Printer** destination.</span></span> <span data-ttu-id="f3984-127">PDF-umbreytingin í prentunarskyni mun eiga sér stað jafnvel þó að slökkt sé á valkostinum.</span><span class="sxs-lookup"><span data-stu-id="f3984-127">The PDF conversion for printing purposes will occur even if the option is turned off.</span></span>

<span data-ttu-id="f3984-128">Til að nota ákveðna [síðustefnu](electronic-reporting-destinations.md#SelectPdfPageOrientation) þegar þú prentar skjá á útleið á Excel-sniði verðurðu að kveikja á valkostinum **Umbreyta í PDF**.</span><span class="sxs-lookup"><span data-stu-id="f3984-128">To use a specific [page orientation](electronic-reporting-destinations.md#SelectPdfPageOrientation) when you print an outbound document in Excel format, you must turn on the **Convert to PDF** option.</span></span> <span data-ttu-id="f3984-129">Þegar þú stillir valkostinn **Umbreyta í PDF** á **Já** verður reiturinn **Síðustefna** tiltækur.</span><span class="sxs-lookup"><span data-stu-id="f3984-129">When you set the **Convert to PDF** option to **Yes**, the **Page orientation** field becomes available.</span></span> <span data-ttu-id="f3984-130">Í reitnum **Síðustefna** geturðu valið síðustefnu.</span><span class="sxs-lookup"><span data-stu-id="f3984-130">In the **Page orientation** field, you can select a page orientation.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f3984-131">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="f3984-131">Additional resources</span></span>

- [<span data-ttu-id="f3984-132">Yfirlit yfir rafræna skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="f3984-132">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="f3984-133">Áfangastaðir fyrir rafræna skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="f3984-133">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
