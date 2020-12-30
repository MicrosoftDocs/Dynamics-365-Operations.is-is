---
title: Valkostir tilkynninga
description: Þessi grein útskýrir hvernig á að leysa vandamál þar sem viðskiptamaður vill sérsníða skýrslur eða stofna nýjar skýrslur Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 51d84df5c3c29510e2742148b8c260a2cf402639
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527718"
---
# <a name="reporting-options"></a><span data-ttu-id="848b5-103">Valkostir tilkynninga</span><span class="sxs-lookup"><span data-stu-id="848b5-103">Reporting options</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="848b5-104">**Umhverfisupplýsingar**</span><span class="sxs-lookup"><span data-stu-id="848b5-104">**Environment details**</span></span>

<span data-ttu-id="848b5-105">Þetta vandamál á við um öll umhverfi.</span><span class="sxs-lookup"><span data-stu-id="848b5-105">This issue applies to all environments.</span></span>

<span data-ttu-id="848b5-106">**Einkenni**</span><span class="sxs-lookup"><span data-stu-id="848b5-106">**Symptom**</span></span>

<span data-ttu-id="848b5-107">Viðskiptamaður vill sérsníða skýrslur eða stofna nýjar Microsoft Dynamics 365 Human Resources skýrslur.</span><span class="sxs-lookup"><span data-stu-id="848b5-107">The customer wants to customize Microsoft Dynamics 365 Human Resources reports or create new reports.</span></span>

<span data-ttu-id="848b5-108">**Úthreyfing**</span><span class="sxs-lookup"><span data-stu-id="848b5-108">**Issue**</span></span>

<span data-ttu-id="848b5-109">Notandi getur ekki sérsniðið innfelldar skýrslur Microsoft Power BI.</span><span class="sxs-lookup"><span data-stu-id="848b5-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="848b5-110">**Lausn**</span><span class="sxs-lookup"><span data-stu-id="848b5-110">**Solution**</span></span>

- <span data-ttu-id="848b5-111">Hægt er að gefa skýrslu um gögn Human Resources sem flæða til Common Data Service í gegnum Power Apps Common Data Service-tengingu við Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="848b5-111">The Human Resources data that flows to Common Data Service can be reported on via the Power Apps Common Data Service connector to Power BI Desktop.</span></span> <span data-ttu-id="848b5-112">Athugið að Common Data Service inniheldur undirsafn af Human Resources-gögnum.</span><span class="sxs-lookup"><span data-stu-id="848b5-112">Note that Common Data Service contains a subset of Human Resources data.</span></span> <span data-ttu-id="848b5-113">Frekari upplýsingar um Power BI og yfirlit eru í [Stofna Power BI-skýrslur og yfirlit með Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span><span class="sxs-lookup"><span data-stu-id="848b5-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="848b5-114">Rafræn skýrslugerð (ER) er í boði fyrir sumar skýrslur í Human Resources.</span><span class="sxs-lookup"><span data-stu-id="848b5-114">Electronic reporting (ER) is available for some reports in Human Resources.</span></span> <span data-ttu-id="848b5-115">Hægt er að gera sérstillingar, knúnar af viðskiptamönnum, með stillingarmöguleikum rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="848b5-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="848b5-116">Hægt er að flytja út gögn í Microsoft Excel eða Microsoft Word með ýmsum gagnaeiningum sem Human Resources útvegar í gegnum samþættingu Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="848b5-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Human Resources provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="848b5-117">**Langtímalausn**</span><span class="sxs-lookup"><span data-stu-id="848b5-117">**Long-term solution**</span></span>

<span data-ttu-id="848b5-118">Frekari Power BI-valkostir verða tiltækir og fleiri gögn og einingar verða hluti af Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="848b5-118">Additional Power BI options will be available, and more data and entities will be part of Common Data Service.</span></span>
