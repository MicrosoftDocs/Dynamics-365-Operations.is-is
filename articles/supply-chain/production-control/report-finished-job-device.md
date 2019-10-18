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

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a>Skrá sem lokið í númeraplötustýrða staðsetningu úr verkspjaldstækinu 

Ferlið sem kallast Tilkynnt sem lokið lýkur fullunnum vörum í framleiðslupöntun til birgða. Ef fullunnin afurð er virk fyrir háþróuð vörugeymsluferli er tilkynnt um afurðina sem lokið á stað sem kallast framleiðslu framleiðslustaðarins. Nánari upplýsingar um að setja upp framleiðslu framleiðslunnar, sjá [Staðsetning framleiðsluúttaks](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).

Þú verður að velja fyrirliggjandi númeraplötunúmer til að ljúka þessu verkefni. Ef framleiðslustað framleiðslunnar er stillt upp til að vera rakin af leyfismerki verður að fylgja með númeraplötunúmeri þegar tilkynnt er um framleiðslu framleiðslunnar sem lokið. Reiturinn **Númeraplata** er sýnilegur í kvaðningunni **Gera framvinduskýrslu** á síðunni **Verkspjaldstæki**. Reiturinn er aðeins sýnilegur í kvaðningunni **Gera framvinduskýrslu** þegar tilkynnt er um síðustu aðgerð framleiðslupöntunarinnar. Reiturinn er aðeins sýndur ef hluturinn fyrir framleiðslupöntunina er virkur fyrir vörugeymsluferlið. 
