---
title: Valkostir skýrslugerðar í Talent
description: Þetta efnisatriði útskýrir hvernig á að leysa vandamál þar sem viðskiptamaður vill sérsníða skýrslur eða stofna nýjar skýrslur Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 2007e6adec7255b0b3abda7490c2103a8583393f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "304898"
---
# <a name="reporting-options-in-talent"></a><span data-ttu-id="33d1d-103">Valkostir tilkynninga í Talent</span><span class="sxs-lookup"><span data-stu-id="33d1d-103">Reporting options in Talent</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="33d1d-104">**Umhverfisupplýsingar**</span><span class="sxs-lookup"><span data-stu-id="33d1d-104">**Environment details**</span></span>

<span data-ttu-id="33d1d-105">Þetta vandamál á við um öll umhverfi.</span><span class="sxs-lookup"><span data-stu-id="33d1d-105">This issue applies to all environments.</span></span>

<span data-ttu-id="33d1d-106">**Einkenni**</span><span class="sxs-lookup"><span data-stu-id="33d1d-106">**Symptom**</span></span>

<span data-ttu-id="33d1d-107">Viðskiptamaður vill sérsníða skýrslur eða stofna nýjar Microsoft Dynamics 365 for Talent skýrslur.</span><span class="sxs-lookup"><span data-stu-id="33d1d-107">The customer wants to customize Microsoft Dynamics 365 for Talent reports or create new reports.</span></span>

<span data-ttu-id="33d1d-108">**Úthreyfing**</span><span class="sxs-lookup"><span data-stu-id="33d1d-108">**Issue**</span></span>

<span data-ttu-id="33d1d-109">Notandi getur ekki sérsniðið innfelldar skýrslur Microsoft Power BI.</span><span class="sxs-lookup"><span data-stu-id="33d1d-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="33d1d-110">**Lausn**</span><span class="sxs-lookup"><span data-stu-id="33d1d-110">**Solution**</span></span>

- <span data-ttu-id="33d1d-111">Hægt er að gefa skýrslu um gögn Core HR sem flæða til Common Data Service for Apps í gegnum PowerApps CDS-tengingu við Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="33d1d-111">The Core HR data that flows to Common Data Service for Apps can be reported on via the PowerApps CDS connector to Power BI Desktop.</span></span> <span data-ttu-id="33d1d-112">Athugið að Common Data Service for Apps inniheldur undirsafn af Core HR-gögnum.</span><span class="sxs-lookup"><span data-stu-id="33d1d-112">Note that Common Data Service for Apps contains a subset of Core HR data.</span></span> <span data-ttu-id="33d1d-113">Frekari upplýsingar um Power BI og yfirlit eru í [Stofna Power BI -skýrslur og yfirlit með PowerApps Common Data Service](https://powerapps.microsoft.com/en-us/blog/cdsconnectortopowerbi).</span><span class="sxs-lookup"><span data-stu-id="33d1d-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with PowerApps Common Data Service](https://powerapps.microsoft.com/en-us/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="33d1d-114">Rafræn skýrslugerð (ER) er í boði fyrir sumar skýrslur í Talent.</span><span class="sxs-lookup"><span data-stu-id="33d1d-114">Electronic reporting (ER) is available for some reports in Talent.</span></span> <span data-ttu-id="33d1d-115">Hægt er að gera sérstillingar, knúnar af viðskiptamönnum, með stillingarmöguleikum rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="33d1d-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="33d1d-116">Hægt er að flytja út gögn í Microsoft Excel eða Microsoft Word með ýmsum gagnaeiningum sem Talent útvegar í gegnum samþættingu Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="33d1d-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Talent provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="33d1d-117">**Langtímalausn**</span><span class="sxs-lookup"><span data-stu-id="33d1d-117">**Long-term solution**</span></span>

<span data-ttu-id="33d1d-118">Frekari valkostir Power BI verða tiltækir og fleiri gögn og einingar verða hluti af Common Data Service fyrir Apps.</span><span class="sxs-lookup"><span data-stu-id="33d1d-118">Additional Power BI options will be available, and more data and entities will be part of Common Data Service for Apps.</span></span>
