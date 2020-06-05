---
title: Skrá sem lokið í númeraplötustýrða staðsetningu úr verkspjaldstækinu
description: Þetta efni lýsir ferlinu til að klára fullunnar vörur í framleiðslupöntun til birgða þegar númeraplata stjórnar staðsetningu.
author: johanhoffmann
manager: tfehr
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistration, ProdJournalTransJob, ProdJournalTransRoute, ProdParmReportFinished
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19351
ms.assetid: bcc9e242-b4b8-4144-b14d-c3c106fb40ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2019-09-06
ms.dyn365.ops.version: AX 10.0.6
ms.openlocfilehash: 74e1e30f5afe51cd0ecec2530ffcb9a59eec5fee
ms.sourcegitcommit: 89022f39502b19c24c0997ae3a01a64b93280f42
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/12/2020
ms.locfileid: "3367246"
---
# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a><span data-ttu-id="d19dc-103">Skrá sem lokið í númeraplötustýrða staðsetningu úr verkspjaldstækinu</span><span class="sxs-lookup"><span data-stu-id="d19dc-103">Report as finished to a license plate controlled location from the Job card device</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d19dc-104">Ferlið sem kallast Tilkynnt sem lokið lýkur fullunnum vörum í framleiðslupöntun til birgða.</span><span class="sxs-lookup"><span data-stu-id="d19dc-104">The process called Reporting as finished completes finished products on a production order to the inventory.</span></span> <span data-ttu-id="d19dc-105">Ef fullunnin afurð er virk fyrir háþróuð vörugeymsluferli er tilkynnt um afurðina sem lokið á stað sem kallast framleiðslu framleiðslustaðarins.</span><span class="sxs-lookup"><span data-stu-id="d19dc-105">If the finished product is enabled for the advanced warehouse processes, the product is reported as finished to a location called the production output location.</span></span> <span data-ttu-id="d19dc-106">Nánari upplýsingar um að setja upp framleiðslu framleiðslunnar, sjá [Staðsetning framleiðsluúttaks](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).</span><span class="sxs-lookup"><span data-stu-id="d19dc-106">For information about setting up the production output location, see [Production output location](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).</span></span>

<span data-ttu-id="d19dc-107">Ef framleiðslustað framleiðslunnar er stjórnað með leyfisplötum verður að gefa upp leyfisplötu þegar skýrslu er lokið.</span><span class="sxs-lookup"><span data-stu-id="d19dc-107">If the production output location is license plate controlled, then a license plate must be provided when reporting as finished.</span></span> <span data-ttu-id="d19dc-108">Reiturinn **Númeraplata** er sýnilegur í kvaðningunni **Gera framvinduskýrslu** á síðunni **Verkspjaldstæki**.</span><span class="sxs-lookup"><span data-stu-id="d19dc-108">The **License plate** field is visible on the **Report progress** prompt on the **Job card device** page.</span></span> <span data-ttu-id="d19dc-109">Reiturinn er aðeins sýnilegur á kvaðningunni **Gera framvinduskýrslu** þegar tilkynnt er um síðustu aðgerð framleiðslupöntunar og hlutur framleiðslupöntunar er gerður virkur fyrir vöruhúsakerfisferli.</span><span class="sxs-lookup"><span data-stu-id="d19dc-109">The field is only visible on the **Report progress** prompt when reporting on the last operation of the production order and the item for the production order is enabled for the warehouse management processes.</span></span>

<span data-ttu-id="d19dc-110">Valkostirnir eru tveir til að veita númeraplötuna:</span><span class="sxs-lookup"><span data-stu-id="d19dc-110">There are two options for providing the license plate:</span></span>

- <span data-ttu-id="d19dc-111">Notandinn velur fyrirliggjandi númeraplötu í reit númeraplötu.</span><span class="sxs-lookup"><span data-stu-id="d19dc-111">The user selects an existing license plate in the license plate field.</span></span>
- <span data-ttu-id="d19dc-112">Leyfisplatan er sjálfkrafa búin til úr númeraröð og er sjálfgefin í reiti leyfisplötunnar.</span><span class="sxs-lookup"><span data-stu-id="d19dc-112">The license plate is automatically generated from a number sequence and defaulted to the license plate field.</span></span>

<span data-ttu-id="d19dc-113">Valkosturinn að láta leyfisplötuna myndast sjálfkrafa er stilltur með því að velja valkostinn **Mynda leyfisplötu** á síðunni **Stilla vinnslukort fyrir tæki**.</span><span class="sxs-lookup"><span data-stu-id="d19dc-113">The option to have the license plate generated automatically is configured by selecting the option **Generate license plate** on the **Configure job card for devices** page.</span></span>
