---
title: Prentari ER-gerð áfangastaðar
description: Þetta efnisatriði útskýrir hvernig á að skilgreina viðtökuprentara tölvupósts fyrir hvern MÖPPU- eða SKRÁARHLUTA rafræns skýrslugerðarsniðs.
author: NickSelin
ms.date: 02/14/2022
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
ms.openlocfilehash: 2513fc4f86519c71602089cd46e9757813b1a708
ms.sourcegitcommit: b80692c3521dad346c9cbec8ceeb9612e4e07d64
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/05/2022
ms.locfileid: "8388289"
---
# <a name="printer-destination"></a><a name="PrinterDestinationType"></a>Viðtökustaður prentara

[!include [banner](../includes/banner.md)]

Þú getur sent skjal sem myndað er beint til netprentara til beinnar prentunar.

## <a name="prerequisites"></a>Forkröfur

Áður en þú byrjar verður þú að setja upp og stilla skjalaleiðslumiðlun og skrá síðan netprentara. Nánari upplýsingar er að finna í [Setja upp eftirlitsbúnað skjalasendingar til að virkja nettengda prentun](./install-document-routing-agent.md).

## <a name="make-the-printer-destination-available"></a>Gerðu prentaramiðstöðina tiltækan

Til að gera **Prentari** ákvörðunarstaður í boði í núverandi tilviki Microsoft Dynamics 365 Finance, farðu á vinnusvæði **Stjórnun eiginleika** og kveiktu á eftirfarandi aðgerðum, í þessari röð:

1. Umbreyta fylgiskjölum rafrænnar skýrslugerðar á útleið úr Microsoft Office-sniði í PDF
2. Miðlari skjalasendingar sem viðtökustaður rafrænnar skýrslugerðar fyrir fylgiskjöl á útleið

[![Kveikt á ákvörðunarstað ER-prentara í eiginleikastjórnun.](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)

### <a name="applicability"></a>Gildissvið

#### <a name="pdf-printing"></a>PDF prentun

Í útgáfum af Finance fyrir útgáfu 10.0.18 er **Prentari** áfangastað er aðeins hægt að stilla fyrir skráaríhluti sem eru notaðir til að búa til úttak á prentanlegu PDF sniði (**PDF samruni** eða **PDF skjal** sniðsþættir) eða Microsoft Office Excel og Word sniði (**Excel skrá** sniðþáttur). Þegar úttakið er búið til á PDF formi er það sent í prentara. Þegar úttakið er búið til á Office sniði með því að nota **Excel skrá** Format frumefni, er því sjálfkrafa breytt í PDF snið og síðan sent í prentara.

Hins vegar, frá og með útgáfu 10.0.18, geturðu stillt **Prentari** áfangastaður fyrir **Algeng skrá** sniðþáttur. Þessi sniðþáttur er aðallega notaður til að búa til úttak á annað hvort TXT eða XML sniði. Þú getur stillt ER snið sem inniheldur **Algeng skrá** sniðsþáttur sem rótsniðsþáttur og **Tvöfaldur innihald** sniðeining sem eina hreiðra þátturinn undir því. Í þessu tilviki er **Algeng skrá** format frumefni mun framleiða úttak á því sniði sem er tilgreint af bindingunni sem þú stillir fyrir **Tvöfaldur innihald** sniðþáttur. Til dæmis geturðu stillt þessa bindingu til [fylla út](tasks/er-document-management-files-5.md#modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format) þessi þáttur með innihaldi a [Skjalastjórnun](../../fin-ops/organization-administration/configure-document-management.md) viðhengi á PDF eða Office (Excel eða Word) formi. Þú getur prentað út úttakið með því að nota stillt **Prentari** áfangastað. 

> [!NOTE]
> Þegar þú velur **Sameiginlegt\\ Skrá** sniðþáttur til að stilla **Prentari** áfangastað, er engin leið til að tryggja, á hönnunartíma, að valinn þáttur muni framleiða úttak á PDF formi eða úttak sem hægt er að breyta í PDF formi. Þess vegna færðu eftirfarandi viðvörunarskilaboð: "Vinsamlegast, vertu viss um að hægt sé að breyta úttakinu sem er búið til af völdum sniði í PDF. Annars skaltu taka hakið úr 'Breyta í PDF' valkostinn." Þú verður að gera ráðstafanir til að koma í veg fyrir vandamál með keyrslutíma þegar úttak sem ekki er PDF- eða PDF-breytanlegt er gefið til prentunar á keyrslutíma. Ef þú býst við að fá úttak á Office (Excel eða Word) sniði, **Umbreyta í PDF** valkostur verður að vera valinn.
>
> Í útgáfu 10.0.26 og síðar, til að nota **Umbreyta í PDF** valmöguleika, þú verður að velja **PDF** fyrir **Tegund skjalaleiðar** færibreytu stillingarinnar **Prentari** áfangastað.

#### <a name="zpl-printing"></a>ZPL prentun

Í útgáfu 10.0.26 og síðar geturðu stillt **Prentari** áfangastaður fyrir **Sameiginlegt\\ Skrá** snið frumefni með því að velja **ZPL** fyrir **Tegund skjalaleiðar** breytu. Í þessu tilviki er **Umbreyta í PDF** valkosturinn er hunsaður á keyrslutíma og TXT eða XML úttakið er sent beint á valinn prentara með því að nota Zebra Programming Language (ZPL) samninginn [Document routing agent (DRA)](install-document-routing-agent.md). Notaðu þennan eiginleika fyrir ER snið sem táknar ZPL II merkimiðaútlit til að prenta ýmis merki.

[![Stilling færibreytunnar Document routing type í valmyndinni Destination settings.](./media/ER_Destinations-SetDocumentRoutingType.png)](./media/ER_Destinations-SetDocumentRoutingType.png)

Fyrir frekari upplýsingar um þennan eiginleika, sjá [Hannaðu nýja ER lausn til að prenta ZPL merki](er-design-zpl-labels.md).

### <a name="limitations"></a>Takmarkanir

Ákvörðunarstaður **Prentara** er aðeins útfærður fyrir skýjadreifingar.

### <a name="use-the-printer-destination"></a>Nota viðtökustað prentara

1. Stilltu valkostinn **Virkt** á **Já** til að senda myndað skjal til prentara.
2. Í reitinn **Heiti prentara** velurðu nauðsynlegan netprentara.
3. Stilltu valkostinn **Vista á prentskjalasafni?** á **Já** til að geyma myndaða framleiðsluna í skjalasafninu, svo að hann sé tiltækur til frekari prentunar. Til að fá aðgang í geymsluframleiðslu síðar, farðu til **Fyrirtækisstjórnun** \> **Fyrirspurnir og skýrslur** \> **Skýrsluskjalasafn**.

[![Notkun á viðtökustað prentara.](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)

> [!NOTE]
> Ekki þarf að vera kveikt á valkostinum **Umbreyta í PDF** þegar þú stillir ákvörðunarstað **Prentara**. PDF-umbreytingin í prentunarskyni mun eiga sér stað jafnvel þó að slökkt sé á valkostinum.

Til að nota ákveðna [síðustefnu](electronic-reporting-destinations.md#SelectPdfPageOrientation) þegar þú prentar skjá á útleið á Excel-sniði verðurðu að kveikja á valkostinum **Umbreyta í PDF**. Þegar þú stillir valkostinn **Umbreyta í PDF** á **Já** verður reiturinn **Síðustefna** tiltækur. Í reitnum **Síðustefna** geturðu valið síðustefnu.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Yfirlit yfir rafræna skýrslugerð](general-electronic-reporting.md)
- [Áfangastaðir fyrir rafræna skýrslugerð](electronic-reporting-destinations.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
