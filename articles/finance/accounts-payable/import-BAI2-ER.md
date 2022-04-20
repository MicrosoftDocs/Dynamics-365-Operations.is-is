---
title: Settu upp háþróaðan bankaafstemmingarinnflutning með því að nota rafræna skýrslugerð
description: Þetta efnisatriði útskýrir hvernig á að nota rafræna skýrslugerð til að setja upp háþróaða innflutningsferli bankaafstemmingar fyrir BAI2 yfirlit.
author: panolte
ms.date: 03/30/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: twheeloc
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.25
ms.openlocfilehash: 39f1d8ba561ab0e36346f1dfb4f70df318c92a37
ms.sourcegitcommit: cf7d4af11bf85638ee831a28ea5ee1a1e041a675
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 04/04/2022
ms.locfileid: "8544558"
---
# <a name="set-up-advanced-bank-reconciliation-import-by-using-electronic-reporting"></a>Settu upp háþróaðan bankaafstemmingarinnflutning með því að nota rafræna skýrslugerð

[!include [banner](../includes/banner.md)]

Ítarlegri bankaafstemmingareiginleikinn gerir þér kleift að flytja inn rafræn bankayfirlit og samræma þau sjálfkrafa við bankafærslur í Microsoft Dynamics 365 Fjármál. Þetta efni útskýrir hvernig á að setja upp innflutningsvirkni fyrir BAI2 bankayfirlitin þín.

## <a name="set-up-the-electronic-reporting-configuration"></a>Settu upp rafræna skýrslugerð

1. Fara til **Vinnurými \> Rafræn skýrslugerð**.
2. Á flísum fyrir **Microsoft** stillingarveita, veldu **Geymslur**.
3. Veldu **Altækt** og síðan **Opna**.
4. Ef tenging við geymsluna þarf að koma á, velurðu bláa tengilinn í svarglugganum.
5. Í stillingarlistanum, finndu **Fyrirmynd bankayfirlits \> Bankayfirlitslíkan af BAI2**.
6. Veldu **BAI2** sniði.
7. Á **Útgáfur** Flýtiflipi, veldu nýjustu útgáfuna og veldu síðan **Flytja inn**.

## <a name="set-up-the-bank-statement-format"></a>Settu upp bankayfirlitssniðið

1. Fara til **Handbært fé og bankastjórnun \> Uppsetning \> Ítarleg uppsetning bankaafstemmingar \> Bankayfirlitssnið**.
2. Veljið **Nýtt**.
3. Stilltu **Yfirlýsingasnið** og **Nafn** sviðum.
4. Veldu **Almennt rafrænt innflutningssnið** gátreit.
5. Stilltu **Flytja inn sniðstillingar** sviði til **BAI2** sniði.

## <a name="set-up-the-bank-account"></a>Settu upp bankareikninginn

1. Farið í **Reiðufjár- og bankastjórnun \> Bankareikningar \> Bankareikningar**.
2. Opnaðu bankareikninginn.
3. Á **Sátt** flýtiflipann, stilltu **Ítarleg bankaafstemming** valmöguleika til **Já**.
4. Stilltu **Yfirlýsingasnið** sviði til **BAI2** sniði sem var búið til áður.

## <a name="import-the-bank-statement"></a>Flyttu inn bankayfirlitið

1. Fara til **Handbært fé og bankastjórnun \> Afstemming bankayfirlits \> Bankayfirlit**.
2. Efst á **Bankayfirlit** síðu, veldu **Innflutningsyfirlýsing**.
3. Stilltu **bankareikning** reitinn á bankareikninginn í yfirlitinu.
4. Stilltu **Yfirlýsingasnið** sviði til **BAI2** sniði sem var búið til áður.
5. Veldu **Skoðaðu**, og veldu **BAI** skrá.
6. Veldu **Hlaða upp**.
7. Veldu **Allt í lagi** til að flytja inn valda skrá.
