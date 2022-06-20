---
title: Þátta skjöl á innleið á Excel-sniði
description: Þessi grein veitir upplýsingar um hönnun rafrænnar skýrslugerðar (ER) snið til að flokka efni sem er að finna í móttöku Microsoft Excel skrár.
author: NickSelin
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 64371ffb09836d6d60ba2073c706628d2009116e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858681"
---
# <a name="parse-incoming-documents-in-excel-format"></a>Þátta skjöl á innleið á Excel-sniði

[!include[banner](../includes/banner.md)]

Hægt er að hanna snið rafrænnar skýrslugerðar til að þátta mótteknar skrár Microsoft Excel sem tákna gögn í vinnubókum Microsoft Excel (skrár á XLSX-sniði). Síðan er hægt að nota efnið úr þessum skrám til að uppfæra hugbúnaðargögn. Þetta er gagnlegt ef þú:

- Hannar nýtt líkan og snið og vilt prófa þær á keyrslutíma. Í þessu tilviki mun Excel líkja eftir raunverulegum hugbúnaðargögnum.
- Stjórnar gögnum utan hugbúnaðarins í Excel og vilt flytja þessi gögn inn til að senda inn tiltekna skýrslu.

Til að læra meira um þennan eiginleika skal spila verkefnaleiðbeiningarnar **Flytja inn gögn rafrænnar skýrslugerðar frá Microsoft Excel-skrá (hluti 1: Hönnunarsnið)** og **Flytja inn gögn rafrænnar skýrslugerðar frá Microsoft Excel-skrá (hluti 2: Flytja inn gögn)** (hlutar af viðskiptaferlinum 7.5.4.3 Acquire/Develop IT þjónustu-/lausnarþáttum (10677)). Þessar verkefnaleiðbeiningar fylgja þér í gegnum það hvernig hægt er að þátta móttekna Excel-skrá með því að nota snið rafrænnar skýrslugerðar til að flytja inn upplýsingar frá mótteknum skjölum og uppfæra hugbúnaðargögn. Hægt er að sækja verkefnaleiðbeiningarnar frá [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).

Sækja eftirfarandi skrár til að ljúka verkefnaleiðbeiningunum sem minnst er á hér að ofan.

| Lýsing á efni                         | Skrá                                                                       |
|---------------------------------------------|----------------------------------------------------------------------------|
| Móttekin skrá á .XLSX-sniði - sniðmát    | [1099import-template.xlsx](https://go.microsoft.com/fwlink/?linkid=862266) |
| Móttekin skrá á .XLSX-sniði - sýnigögn | [1099import-data.xlsx](https://go.microsoft.com/fwlink/?linkid=862266)     |

Ef þú hefur ekki enn spilað eftirfarandi verkefnaleiðbeiningar, [Stofna nauðsynlega grunnstillingu rafrænnar skýrslugerðar til að flytja inn gögn frá ytri skrá](./tasks/er-required-configurations-import-data.md) í núverandi forriti Finance and Operation, skal sækja eftirfarandi skrá.

| Lýsing á efni    | Skrá                                                            |
|------------------------|-----------------------------------------------------------------|
| Líkanaskilgreining rafrænnar skýrslugerðar | [1099model.xml](https://go.microsoft.com/fwlink/?linkid=862266) |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]