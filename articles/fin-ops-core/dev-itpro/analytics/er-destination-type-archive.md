---
title: Skjalageymsla ER-gerð áfangastaðar
description: Þetta efni veitir upplýsingar um hvernig á að stilla skjalasafn áfangastaðar fyrir hvern FOLDER- eða FILE-hluta á rafrænu skýrslugerðarsniði.
author: NickSelin
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: e2566fc5115df8b47277fc6b6d7f4698cea0a00bea83bcb17e9d7a9e9b765b65
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6718334"
---
# <a name="archive-er-destination-type"></a>Skjalageymsla ER-gerð áfangastaðar

[!include [banner](../includes/banner.md)]

Hægt er að stilla skjalasafn áfangastaðar fyrir hveja **Möppu** eða **Skrá** hluta á rafrænu skýrslugerðarsniði sem er stillt til að búa til skjöl á útleið. Byggt á ákvörðunarstað, er myndað skjal geymt sem viðhengi við skrá yfir ER-vinnslulistann. Til að skoða niðurstöðurnar skal fara í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Rafræn skýrslugerðarvinnsla**.

Hægt er að nota þennan valkost til að senda myndað skjal á Microsoft SharePoint-möppu eða Microsoft Microsoft Azure Geymslu. Stilla **Virkt** á **Já** til að senda frálag á áfangastað sem er skilgreind með völdu skjalagerðina. einungis gerð skjals þar sem flokksins er stillt á **Skrá** eru tiltækar til vals. Hægt er að skilgreina [gerðir skjala](../../fin-ops/organization-administration/configure-document-management.md#configure-document-types) í **Fyrirtækisstjórnun** \> **Skjalastjórnun** \> **Skjalagerðir**. Skilgreining fyrir áfangastaði rafrænnar skýrslugerðar er sú sama og skilgreiningin fyrir skjalastjórnunarkerfið.

[![Síða skjalategunda.](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)

Staðsetning ákvarðar hvar skráin er vistuð. Eftir að áfangastaður **skjalasafns** er virkjaður er hægt að vista niðurstöður í Vinnsluskjalasafn. Hægt er að skoða niðurstöðurnar í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Viðtökustaður rafrænnar skýrslugerðar**.

> [!NOTE]
> Veldu gerð skjals fyrir Vinnslu skjalasafns með því að fara í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð** \> **Færibreytur rafrænnar skýrslugerðar**. Frekari upplýsingar er að finna í [Skilgreina ramma rafrænnar skýrslugerðar](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).

## <a name="sharepoint"></a>SharePoint

Hægt er að vista skrá í möppu merktu SharePoint. Til að skilgreina sjálfgefinn þjón SharePoint ferðu á **Fyrirtækisstjórnun** \> **Skjalastjórnun** \> **Færibreytur skjalastjórnunar**. Á flipanum **SharePoint** stillirðu SharePoint-möppuna. Síðan geturðu valið það sem möppu þar sem ER framleiðsla verður vistuð. Staðsetning **SharePoint** verður að vera valin í þessari gerð skjals.

[![Val á SharePoint möppu.](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)

## <a name="azure-storage"></a>Azure-geymsla

Þegar staðsetning gerðar skjals er stillt á **Azure-geymsla**, er hægt að vista skrá í Azure Geymslu.

> [!NOTE] 
> Rammi rafrænnar skýrslugerðar vistar skrár varanlega í Azure Blob geymslu ólíkt ramma Gagnastjórnunar sem notar sjö daga varðveislureglu fyrir skjöl sem þarf að vinna úr. Frekari upplýsingar er að finna í [API til að sækja skilaboðastöðu](../data-entities/recurring-integrations.md#api-for-getting-message-status) og [Stöðuprófun API](../data-entities/data-management-api.md#status-check-api). Ótengdar skrár verða geymdar í Azure Blob geymslu sem viðhengi töflufærslna forrits eins lengi og þörf er á. Einni skrá verður eytt úr Azure Blob geymslu ásamt hugbúnaðartöflufærslunni sem þessi skrá var hengd við.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Yfirlit yfir rafræna skýrslugerð](general-electronic-reporting.md)
- [Áfangastaðir fyrir rafræna skýrslugerð](electronic-reporting-destinations.md)
- [Stilla skjalastjórnun](../../fin-ops/organization-administration/configure-document-management.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]