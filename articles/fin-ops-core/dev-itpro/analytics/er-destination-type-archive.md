---
title: Skjalageymsla ER-gerð áfangastaðar
description: Þetta efni veitir upplýsingar um hvernig á að stilla skjalasafn áfangastaðar fyrir hvern FOLDER eða FILE hluti á rafrænu skýrslugerðarsniðinu (ER) sem er stillt til að búa til útgönguskjöl.
author: NickSelin
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 8797a68507a5116c6adbf1f2d805838fa507958c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745586"
---
# <a name="archive-destination"></a>áfangastaður skjalasafns

[!include [banner](../includes/banner.md)]

Hægt er að stilla skjalasafn áfangastaðar fyrir hvern FOLDER eða FILE hluti á rafrænu skýrslugerðarsniðinu (ER) sem er stillt til að búa til útgönguskjöl. Byggt á ákvörðunarstað, er myndað skjal geymt sem viðhengi við skrá yfir ER-vinnslulistann.

Hægt er að nota þennan valkost til að senda myndað skjal á Microsoft SharePoint-möppu eða Microsoft Microsoft Azure Geymslu. Stilla **Virkt** á **Já** til að senda frálag á áfangastað sem er skilgreind með völdu skjalagerðina. einungis gerð skjals þar sem flokksins er stillt á **Skrá** eru tiltækar til vals. Hægt er að skilgreina [gerðir skjala](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) í **Fyrirtækisstjórnun** \> **Skjalastjórnun** \> **Skjalagerðir**. Skilgreining fyrir áfangastaði rafrænnar skýrslugerðar er sú sama og skilgreiningin fyrir skjalastjórnunarkerfið.

[![Síðan Gerðir skjala](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)

Staðsetning ákvarðar hvar skráin er vistuð. Eftir að áfangastaður **skjalasafns** er virkjaður er hægt að vista niðurstöður í Vinnsluskjalasafn. Hægt er að skoða niðurstöðurnar í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Viðtökustaður rafrænnar skýrslugerðar**.

> [!NOTE]
> Veldu gerð skjals fyrir Vinnslu skjalasafns með því að fara í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð** \> **Færibreytur rafrænnar skýrslugerðar**. Frekari upplýsingar er að finna í [Stilla ramma rafrænnar skýrslugerðar (ER)](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).

## <a name="sharepoint"></a>SharePoint

Hægt er að vista skrá í möppu merktu SharePoint. Til að skilgreina sjálfgefinn þjón SharePoint ferðu á **Fyrirtækisstjórnun** \> **Skjalastjórnun** \> **Færibreytur skjalastjórnunar**. Á flipanum **SharePoint** stillirðu SharePoint-möppuna. Síðan geturðu valið það sem möppu þar sem ER framleiðsla verður vistuð. Staðsetning **SharePoint** verður að vera valin í þessari gerð skjals.

[![Val á SharePoint möppu](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)

## <a name="azure-storage"></a>Azure-geymsla

Þegar staðsetning gerðar skjals er stillt á **Azure-geymsla**, er hægt að vista skrá í Azure Geymslu.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Yfirlit yfir rafræna skýrslugerð](general-electronic-reporting.md)
- [Áfangastaðir fyrir rafræna skýrslugerð](electronic-reporting-destinations.md)
- [Stilla skjalastjórnun](../../fin-ops/organization-administration/configure-document-management.md)
