---
title: Skrá sem lokið í númeraplötustýrða staðsetningu úr verkspjaldstækinu
description: Þetta efni lýsir ferlinu til að klára fullunnar vörur í framleiðslupöntun til birgða þegar númeraplata stjórnar staðsetningu.
author: johanhoffmann
manager: AnnBe
ms.date: 01/06/2020
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
ms.openlocfilehash: 5f61c1abfb115f02e6ff314f6a3e42bb1d3b543f
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092569"
---
[!include [banner](../includes/banner.md)]

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a>Skrá sem lokið í númeraplötustýrða staðsetningu úr verkspjaldstækinu 

Ferlið sem kallast Tilkynnt sem lokið lýkur fullunnum vörum í framleiðslupöntun til birgða. Ef fullunnin afurð er virk fyrir háþróuð vörugeymsluferli er tilkynnt um afurðina sem lokið á stað sem kallast framleiðslu framleiðslustaðarins. Nánari upplýsingar um að setja upp framleiðslu framleiðslunnar, sjá [Staðsetning framleiðsluúttaks](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).

Ef framleiðslustað framleiðslunnar er stjórnað með leyfisplötum verður að gefa upp leyfisplötu þegar skýrslu er lokið. Reiturinn **Númeraplata** er sýnilegur í kvaðningunni **Gera framvinduskýrslu** á síðunni **Verkspjaldstæki**. Reiturinn er aðeins sýnilegur á kvaðningunni **Gera framvinduskýrslu** þegar tilkynnt er um síðustu aðgerð framleiðslupöntunar og hlutur framleiðslupöntunar er gerður virkur fyrir vöruhúsakerfisferli. 

Það eru tveir möguleikar til að útvega leyfisplötuna
- Notandinn er að velja fyrirliggjandi leyfisplötu í reitnum fyrir leyfisplötu.
- Leyfisplatan er sjálfkrafa búin til úr númeraröð og er sjálfgefin í reiti leyfisplötunnar.

Valkosturinn að láta leyfisplötuna myndast sjálfkrafa er stilltur með því að velja valkostinn **Mynda leyfisplötu** á síðunni **Stilla vinnslukort fyrir tæki**.
