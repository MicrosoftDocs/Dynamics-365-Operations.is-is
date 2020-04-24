---
title: Aldursskýrsla birgða
description: Þetta efni lýsir virkni sem gerir þér kleift að keyra aldursgreiningarskýrslu birgða og gera úttakið tiltækt sem form og töflu.
author: AndersGirke
manager: tfehr
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2019-01-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 790c8fe3a52bce652227f1cef97eff6496476100
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201621"
---
# <a name="inventory-aging-report"></a>Aldursskýrsla birgða


[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Í Microsoft Dynamics 365 Supply Chain Management geturðu keyrt skýrsluna **Aldursgreiningu birgða** og gera úttakið tiltækt sem form og töflu. Á forminu er dálkum og samanlögðum stöðum gagnvirkt breytt, allt eftir því skipulagi sem er stillt. Grafið gefur sjónrænt yfirlit sem styður síun og gerir þér kleift að bora niður í smáatriði. Að auki gerir gagnaeining sem heitir **Aldursskýrsla birgða** þér kleift að flytja út niðurstöður skýrslunnar **Aldursgreining birgða** sem var keyrð á snið eins og Microsoft Excel-skjal eða PDF-skjal.

Þessi aðferð til að keyra skýrsluna **Aldursgreining birgða** er gagnlegt í tilvikum þar sem úttakið inniheldur margar línur. Til dæmis mun úttakið innihalda margar línur ef þú ert með 50.000 hluti og 300 verslanir sem eru stofnaðar sem vöruhús og þú biður um aldursgreiningu birgða eftir hlut, síðu og vörugeymslu.

## <a name="run-an-inventory-aging-report"></a>Keyra aldursskýrslu birgða

1. Farðu í **Kostnaðarstjórnun \> Fyrirspurnir og skýrslur \> Geymsla aldursgreiningarskýrslu birgða**.
1. Veljið **Nýtt**.
1. Í reitinn **Kenni ferlis – Heiti** er slegið inn einkvæmt heiti fyrir skýrsluna.
1. Veldu skýrsluna **Auðkenning - kenni** og síaðu hana eftir þörfum.

    Framkvæmd skýrslu er alltaf gerð í runuvinnslu.

1. Eftir að runuvinnslunni er lokið er úttakið sýnt á síðunni **Geymsla aldursgreiningarskýrslu birgða**.
1. Til að skoða úttakið sem glugga með hefðbundið hnitaútlit skaltu velja **Skoða upplýsingar**. Til að skoða úttakið sem uppsafnaða töflu velurðu **Skoða rit**.

    > [!NOTE]
    > Formið mun ekki innihalda millisamtölur sem eru skilgreindar í skýrsluútliti.

Gagnaeiningin **Aldursskýrsla birgða** gerir þér kleift að flytja úttakið úr skýrslunni **Aldursgreining birgða** með því að beita síu fyrir reitinn **Kenni ferlis – Heiti** á hvaða snið sem gagnastjórnun styður.
