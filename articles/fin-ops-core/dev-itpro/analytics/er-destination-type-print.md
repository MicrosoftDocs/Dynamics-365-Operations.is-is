---
title: Prentari ER-gerð áfangastaðar
description: Þetta efnisatriði útskýrir hvernig á að skilgreina viðtökuprentara tölvupósts fyrir hvern MÖPPU- eða SKRÁARHLUTA rafræns skýrslugerðarsniðs.
author: NickSelin
ms.date: 02/24/2021
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
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 83081f8c17a903cd447a34596df2e61ebda0cafc
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753433"
---
# <a name="printer-destination"></a><a name="PrinterDestinationType"></a>Viðtökustaður prentara

[!include [banner](../includes/banner.md)]

Þú getur sent skjal sem myndað er beint til netprentara til beinnar prentunar.

## <a name="prerequisites"></a>Forkröfur

Áður en þú byrjar verður þú að setja upp og stilla skjalaleiðslumiðlun og skrá síðan netprentara. Nánari upplýsingar er að finna í [Setja upp eftirlitsbúnað skjalasendingar til að virkja nettengda prentun](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent).

## <a name="make-the-printer-destination-available"></a>Gerðu prentaramiðstöðina tiltækan

Til að gera **Prentari** ákvörðunarstaður í boði í núverandi tilviki Microsoft Dynamics 365 Finance, farðu á vinnusvæði **Stjórnun eiginleika** og kveiktu á eftirfarandi aðgerðum, í þessari röð:

1. Umbreyta fylgiskjölum rafrænnar skýrslugerðar á útleið úr Microsoft Office-sniði í PDF
2. Miðlari skjalasendingar sem viðtökustaður rafrænnar skýrslugerðar fyrir fylgiskjöl á útleið

[![Kveiktu á ákvörðunarstað ER prentara í Stjórnun eiginleika](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)

### <a name="applicability"></a>Gildissvið

Ákvörðunarstað **Prentara** er aðeins hægt að stilla áfangastað fyrir skráhluta sem eru notaðir til að búa til framleiðsla á annaðhvort prentvænu PDF sniði (PDF samruna eða PDF skráarsniðsþátta) eða Microsoft Office Excel/Word snið (Excel skjal). Þegar úttak hefur verið myndað á PDF sniði er það sent til prentara. Þegar úttak er myndað á Microsoft Office-sniði er því sjálfkrafa breytt í PDF-snið og síðan sent til prentara.

### <a name="limitations"></a>Takmarkanir

Ákvörðunarstaður **Prentara** er aðeins útfærður fyrir skýjadreifingar.

### <a name="use-the-printer-destination"></a>Nota viðtökustað prentara

1. Stilltu valkostinn **Virkt** á **Já** til að senda myndað skjal til prentara.
2. Í reitinn **Heiti prentara** velurðu nauðsynlegan netprentara.
3. Stilltu valkostinn **Vista á prentskjalasafni?** á **Já** til að geyma myndaða framleiðsluna í skjalasafninu, svo að hann sé tiltækur til frekari prentunar. Til að fá aðgang í geymsluframleiðslu síðar, farðu til **Fyrirtækisstjórnun** \> **Fyrirspurnir og skýrslur** \> **Skýrsluskjalasafn**.

[![Notkun á viðtökustað prentara](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)

> [!NOTE]
> Ekki þarf að vera kveikt á valkostinum **Umbreyta í PDF** þegar þú stillir ákvörðunarstað **Prentara**. PDF-umbreytingin í prentunarskyni mun eiga sér stað jafnvel þó að slökkt sé á valkostinum.

Til að nota ákveðna [síðustefnu](electronic-reporting-destinations.md#SelectPdfPageOrientation) þegar þú prentar skjá á útleið á Excel-sniði verðurðu að kveikja á valkostinum **Umbreyta í PDF**. Þegar þú stillir valkostinn **Umbreyta í PDF** á **Já** verður reiturinn **Síðustefna** tiltækur. Í reitnum **Síðustefna** geturðu valið síðustefnu.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Yfirlit yfir rafræna skýrslugerð](general-electronic-reporting.md)
- [Áfangastaðir fyrir rafræna skýrslugerð](electronic-reporting-destinations.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
