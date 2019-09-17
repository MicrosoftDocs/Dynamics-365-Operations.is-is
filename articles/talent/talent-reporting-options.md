---
title: Valkostir skýrslugerðar í Talent
description: Þetta efnisatriði útskýrir hvernig á að leysa vandamál þar sem viðskiptamaður vill sérsníða skýrslur eða stofna nýjar skýrslur Dynamics 365 for Talent.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 8e7348a515b08523c15aa8f74d5616a3daf645b7
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/12/2019
ms.locfileid: "1741799"
---
# <a name="reporting-options-in-talent"></a><span data-ttu-id="559f8-103">Valkostir tilkynninga í Talent</span><span class="sxs-lookup"><span data-stu-id="559f8-103">Reporting options in Talent</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="559f8-104">**Umhverfisupplýsingar**</span><span class="sxs-lookup"><span data-stu-id="559f8-104">**Environment details**</span></span>

<span data-ttu-id="559f8-105">Þetta vandamál á við um öll umhverfi.</span><span class="sxs-lookup"><span data-stu-id="559f8-105">This issue applies to all environments.</span></span>

<span data-ttu-id="559f8-106">**Einkenni**</span><span class="sxs-lookup"><span data-stu-id="559f8-106">**Symptom**</span></span>

<span data-ttu-id="559f8-107">Viðskiptamaður vill sérsníða skýrslur eða stofna nýjar Microsoft Dynamics 365 for Talent skýrslur.</span><span class="sxs-lookup"><span data-stu-id="559f8-107">The customer wants to customize Microsoft Dynamics 365 for Talent reports or create new reports.</span></span>

<span data-ttu-id="559f8-108">**Úthreyfing**</span><span class="sxs-lookup"><span data-stu-id="559f8-108">**Issue**</span></span>

<span data-ttu-id="559f8-109">Notandi getur ekki sérsniðið innfelldar skýrslur Microsoft Power BI.</span><span class="sxs-lookup"><span data-stu-id="559f8-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="559f8-110">**Lausn**</span><span class="sxs-lookup"><span data-stu-id="559f8-110">**Solution**</span></span>

- <span data-ttu-id="559f8-111">Hægt er að gefa skýrslu um gögn Core HR sem flæða til Common Data Service í gegnum PowerApps Common Data Service-tengingu við Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="559f8-111">The Core HR data that flows to Common Data Service can be reported on via the PowerApps Common Data Service connector to Power BI Desktop.</span></span> <span data-ttu-id="559f8-112">Athugið að Common Data Service inniheldur undirsafn af Core HR-gögnum.</span><span class="sxs-lookup"><span data-stu-id="559f8-112">Note that Common Data Service contains a subset of Core HR data.</span></span> <span data-ttu-id="559f8-113">Frekari upplýsingar um Power BI og yfirlit eru í [Stofna Power BI -skýrslur og yfirlit með PowerApps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span><span class="sxs-lookup"><span data-stu-id="559f8-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with PowerApps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="559f8-114">Rafræn skýrslugerð (ER) er í boði fyrir sumar skýrslur í Talent.</span><span class="sxs-lookup"><span data-stu-id="559f8-114">Electronic reporting (ER) is available for some reports in Talent.</span></span> <span data-ttu-id="559f8-115">Hægt er að gera sérstillingar, knúnar af viðskiptamönnum, með stillingarmöguleikum rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="559f8-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="559f8-116">Hægt er að flytja út gögn í Microsoft Excel eða Microsoft Word með ýmsum gagnaeiningum sem Talent útvegar í gegnum samþættingu Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="559f8-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Talent provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="559f8-117">**Langtímalausn**</span><span class="sxs-lookup"><span data-stu-id="559f8-117">**Long-term solution**</span></span>

<span data-ttu-id="559f8-118">Frekari Power BI-valkostir verða tiltækir og fleiri gögn og einingar verða hluti af Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="559f8-118">Additional Power BI options will be available, and more data and entities will be part of Common Data Service.</span></span>
