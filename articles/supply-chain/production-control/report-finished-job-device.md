---
title: Skrá sem lokið í númeraplötustýrða staðsetningu úr verkspjaldstækinu
description: Þetta efni lýsir ferlinu til að klára fullunnar vörur í framleiðslupöntun til birgða þegar númeraplata stjórnar staðsetningu.
author: johanhoffmann
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistration, ProdJournalTransJob, ProdJournalTransRoute, ProdParmReportFinished
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19351
ms.assetid: bcc9e242-b4b8-4144-b14d-c3c106fb40ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2019-09-06
ms.dyn365.ops.version: AX 10.0.6
ms.openlocfilehash: 35ad27a6b8a52bfd086fbe4fc57b1681ff88fd5b
ms.sourcegitcommit: 58db26b7edf02e7c33aaaf1c934e3263aa74b01f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/11/2019
ms.locfileid: "1995143"
---
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a><span data-ttu-id="e52d5-103">Skrá sem lokið í númeraplötustýrða staðsetningu úr verkspjaldstækinu</span><span class="sxs-lookup"><span data-stu-id="e52d5-103">Report as finished to a license plate controlled location from the Job card device</span></span> 

<span data-ttu-id="e52d5-104">Ferlið sem kallast Tilkynnt sem lokið lýkur fullunnum vörum í framleiðslupöntun til birgða.</span><span class="sxs-lookup"><span data-stu-id="e52d5-104">The process called Reporting as finished completes finished products on a production order to the inventory.</span></span> <span data-ttu-id="e52d5-105">Ef fullunnin afurð er virk fyrir háþróuð vörugeymsluferli er tilkynnt um afurðina sem lokið á stað sem kallast framleiðslu framleiðslustaðarins.</span><span class="sxs-lookup"><span data-stu-id="e52d5-105">If the finished product is enabled for the advanced warehouse processes, the product is reported as finished to a location called the production output location.</span></span> <span data-ttu-id="e52d5-106">Nánari upplýsingar um að setja upp framleiðslu framleiðslunnar, sjá [Staðsetning framleiðsluúttaks](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).</span><span class="sxs-lookup"><span data-stu-id="e52d5-106">For information about setting up the production output location, see [Production output location](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).</span></span>

<span data-ttu-id="e52d5-107">Þú verður að velja fyrirliggjandi númeraplötunúmer til að ljúka þessu verkefni.</span><span class="sxs-lookup"><span data-stu-id="e52d5-107">You must select an existing license plate number to complete this task.</span></span> <span data-ttu-id="e52d5-108">Ef framleiðslustað framleiðslunnar er stillt upp til að vera rakin af leyfismerki verður að fylgja með númeraplötunúmeri þegar tilkynnt er um framleiðslu framleiðslunnar sem lokið.</span><span class="sxs-lookup"><span data-stu-id="e52d5-108">If the production output location is set up to be tracked by license plate, then a license plate number must be included when reporting the production output location as finished.</span></span> <span data-ttu-id="e52d5-109">Reiturinn **Númeraplata** er sýnilegur í kvaðningunni **Gera framvinduskýrslu** á síðunni **Verkspjaldstæki**.</span><span class="sxs-lookup"><span data-stu-id="e52d5-109">The **License plate** field is visible on the **Report progress** prompt on the **Job card device** page.</span></span> <span data-ttu-id="e52d5-110">Reiturinn er aðeins sýnilegur í kvaðningunni **Gera framvinduskýrslu** þegar tilkynnt er um síðustu aðgerð framleiðslupöntunarinnar.</span><span class="sxs-lookup"><span data-stu-id="e52d5-110">The field is only visible on the **Report progress** prompt when reporting on the last operation of the production order.</span></span> <span data-ttu-id="e52d5-111">Reiturinn er aðeins sýndur ef hluturinn fyrir framleiðslupöntunina er virkur fyrir vörugeymsluferlið.</span><span class="sxs-lookup"><span data-stu-id="e52d5-111">The field is only shown if the item for the production order is enabled for the warehouse management processes.</span></span> 
