---
title: Skýrsla um aldursgreiningu birgða
description: Þetta efni lýsir virkni sem gerir þér kleift að keyra aldursgreiningarskýrslu birgða og gera úttakið tiltækt sem form og töflu.
author: AndersGirke
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2019-01-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2ddddb0b1e377ed525b7c17fec5a4b3305573d0eba551bc03f075109a2ed769b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6781111"
---
# <a name="inventory-aging-report-storage"></a>Skýrsla um aldursgreiningu birgða

[!include [banner](../includes/banner.md)]

Í Microsoft Dynamics 365 Supply Chain Management er hægt að keyra skýrsluna **Geymsla aldursgreiningarskýrslu birgða** og gera niðurstöðurnar tiltækar sem skjámynd og graf. Á forminu er dálkum og samanlögðum stöðum gagnvirkt breytt, allt eftir því skipulagi sem er stillt. Grafið gefur sjónrænt yfirlit sem styður síun og gerir þér kleift að bora niður í smáatriði. Að auki leyfir gagnaeining sem kölluð er **Skýrsla um aldursgreiningu birgða** að flytja út niðurstöður á keyrslu á skýrslu **Geymsla aldursgreiningarskýrslu birgða** á form eins og Microsoft Excel-skrá eða PDF-skrá.

Þessi aðferð við að keyra **Geymsla aldursgreiningarskýrslu birgða** skýrslu er gagnleg í tilfellum þegar niðurstöðurnar innihalda margar línur. Til dæmis mun úttakið innihalda margar línur ef þú ert með 50.000 hluti og 300 verslanir sem eru stofnaðar sem vöruhús og þú biður um aldursgreiningu birgða eftir hlut, síðu og vörugeymslu.

## <a name="enable-the-inventory-value-storage-report-feature"></a>Virkja eiginleika fyrir geymslu aldursgreiningarskýrslu birgða

Áður en hægt er að nota þennan eiginleika þarf að virkja hann í kerfinu. Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleika og virkja hann ef þörf krefur. Hérna er eiginleikinn skráður sem:

- **Eining** - Kostnaðarstjórnun
- **Heiti eiginleika** - Skýrsla um aldursgreiningu birgða

## <a name="run-an-inventory-aging-report-storage"></a>Keyra skýrslu um aldursgreiningu birgða

1. Farðu í **Kostnaðarstjórnun \> Fyrirspurnir og skýrslur \> Geymsla aldursgreiningarskýrslu birgða**.
1. Veljið **Nýtt**.
1. Í reitinn **Kenni ferlis – Heiti** er slegið inn einkvæmt heiti fyrir skýrsluna.
1. Veldu skýrsluna **Auðkenning - kenni** og síaðu hana eftir þörfum.

    Framkvæmd skýrslu er alltaf gerð í runuvinnslu.

1. Eftir að runuvinnslunni er lokið er úttakið sýnt á síðunni **Geymsla aldursgreiningarskýrslu birgða**.
1. Til að skoða úttakið sem glugga með hefðbundið hnitaútlit skaltu velja **Skoða upplýsingar**. Til að skoða úttakið sem uppsafnaða töflu velurðu **Skoða rit**.

    > [!NOTE]
    > Formið mun ekki innihalda millisamtölur sem eru skilgreindar í skýrsluútliti.

Gagnaeiningin **Skýrsla um aldursgreiningu birgða** gerir þér kleift að flytja niðurstöðurnar af **Geymsla aldursgreiningarskýrslu birgða** skýrslu út með því að nota síu fyrir reitinn **Kenni ferlis - Heiti** á hvaða snið sem gagnastjórnun styður.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]