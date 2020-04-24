---
title: Sjálfvirk styrking með fínstillingu skipulags
description: Þetta efni útskýrir hvernig á að nota sjálfvirka styrkingu með fínstillingu skipulagsins.
author: ChristianRytt
manager: tfehr
ms.date: 11/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-11-30
ms.dyn365.ops.version: AX 10.0.7
ms.openlocfilehash: 5bfa8a1f025c2884f31b9fcb817e008a007ac010
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209744"
---
# <a name="auto-firming-with-planning-optimization"></a>Sjálfvirk styrking með fínstillingu skipulags

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

Sjálfvirk styrking gerir þér kleift að festa (það er að losa) fyrirhugaðar pantanir sem hluta af ferli aðaláætlunargerðar. Þegar fyrirhugaðar pantanir eru styrktar er þeim breytt í raunverulegar innkaupapantanir, millifærslupantanir eða framleiðslupantanir. Þegar fínstilling skipulags er notuð eru skipulagðar pantanir styrktar meðan á aðaláætlunargerð stendur þegar pöntunardagsetningin (það er upphafsdagsetningin) er innan tímamarka.

> [!NOTE]
> Sjálfvirk staðfesting áætlaðrar innkaupapöntunar getur aðeins farið fram ef varan er tengd lánardrottni.

## <a name="turn-on-auto-firming"></a>Kveiktu á sjálfvirkri staðfestingu

Fylgdu þessum skrefum til að kveikja á sjálfvirkri staðfestingu.

1. Á vinnusvæðinu **Stjórnun eiginleika**, á flipanum **Nýtt**, velurðu **Sjálfvirk styrking með fínstillingu skipulags** á listanum. Ef eiginleikinn birtist ekki á flipanum **Nýtt** skaltu líta á flipana **Ekki gert virkt** og **Allt**.
1. Veldu **Virkja núna**. Að öðrum kosti velurðu **Áætlun** og velur síðan tímann þegar kveikt skal á aðgerðinni.

## <a name="set-up-the-firming-time-fence"></a>Setja upp tímamörk staðfestingar

Staðfestingartímamörkin eru framreiknuð frá keyrsludagsetningu aðaláætlunargerðar. Þau eru skilgreind af fjölda daga sem eru færð inn. Þú getur stjórnað tímamörkum staðfestingar á eftirfarandi hátt:

- Til að skilgreina sjálfgefinn girðingartíma girðingar fyrir umfjöllunarhóp ferðu í **Aðaláætlunargerð** \> **Uppsetning** \> **Þekja** \> **Þekjuhópar** og veldu þekjuhóp. Síðan, á flýtiflipanum **Annað**, í reitinn **Sjálfvirk tímamörk staðfestinga (dagar)**, sláðu inn fjölda daga.
- Til að skrifa yfir tímamörk staðfestingar sem eru skilgreind fyrir þekjuhópinn fyrir tiltekinn hlut ferðu í **Afurðaupplýsingastjórnun** \> **Útgefnar afurðir**, veldu síðan af aðgerðarrúðunni **Áætlun** og veldu síðan **Vöruþekja**. Síðan, á flipanum **Almennt** velurðu **Hnekkja tímamörkum** og í reitinn **Sjálfvirk tímamörk staðfestinga (dagar)** slærðu inn fjölda daga.
- Til að skrifa yfir þau tímamörk staðfestingar sem eru skilgreind fyrir þekjuhópinn og vöruþekju fyrir tiltekið aðalskipulag **Aðaláætlunargerð** \> **Uppsetning** \> **Aðaláætlanir** og velur aðalskipulag. Síðan, á flýtiflipanum **Tímamörk í dögum**, stillirðu **Frysta** á **Já** og slærð inn fjölda daga.

Ef kveikt er á sjálfvirkri staðfestingu fyrir keyrslu aðaláætlunargerðar sem notar fínstillingu skipulags er ferli sjálfvirkrar staðfestingar gert samkvæmt uppsetningu á sjálfvirkri staðfestingu. Ef ekki er kveikt á sjálfvirkri staðfestingu eða ef áætlunargerð er hafin af síðunni **Nettóþörf** er sjálfvirkt staðfestandi ferli sleppt.

## <a name="planning-optimization-vs-the-built-in-supply-chain-management-planning-engine"></a>Fínstilling skipulags vs. innbyggða áætlunarvélin Supply Chain Management

Bæði fínstillingu skipulags og skipulagsvélin sem er innbyggð í Microsoft Dynamics 365 Supply Chain Management er hægt að nota til að gera sjálfvirkt fyrirhugaðar pantanir. Þó er til staðar mikilvægur munur. Til dæmis, meðan fínstilling skipulagsins notar pöntunardaginn (þ.e.a.s. upphafsdaginn) til að ákvarða hvaða fyrirhugaðar pantanir verða festar, þá notar innbyggða skipulagsvélin fyrir Supply Chain Management dagsetninguna (þ.e.a.s. lokadagsetningin). Hér er yfirlit yfir mismuninn.

**Fínstilling áætlanagerðar**

- Sjálfvirk staðfesting byggist á pöntunardegi (upphafsdegi).
- Vegna þess að pöntunardagsetningin (upphafsdagsetningin) kallar á staðfestingu þarftu ekki að líta á afhendingartímann sem hluta af tímamörkum staðfestingar.
- Ef þú vilt staðfesta allar pantanir sem verða að byrja í þessari viku, verða tímamörk staðfestingar að vera ein vika.

**Innbyggð áætlunarvél í Supply Chain Management**

- Sjálfvirk staðfesting byggist á þarfadagsetningu (lokadegi).
- Til að hjálpa til við að tryggja að pantanir séu staðfestar á réttum tíma verða tímamörk staðfestingar að vera lengri en afhendingartíminn.
- Ef þú vilt staðfesta allar pantanir sem verða að byrja í þessari viku, verða tímamörk staðfestingar að vera afhendingartíminn plús ein vika.
