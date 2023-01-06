---
title: Prentari ER-gerð áfangastaðar
description: Þessi grein útskýrir hvernig á að skilgreina viðtökuprentara tölvupósts fyrir hvern MÖPPU- eða SKRÁARHLUTA rafræns skýrslugerðarsniðs.
author: kfend
ms.date: 02/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.custom: 97423
ms.assetid: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
ms.openlocfilehash: 7e01476b85c6c35d7c36c90db4d64ab2a2930fec
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271735"
---
# <a name="printer-destination"></a><a name="PrinterDestinationType"></a>Viðtökustaður prentara

[!include [banner](../includes/banner.md)]

Þú getur sent skjal sem myndað er beint til netprentara til beinnar prentunar.

## <a name="prerequisites"></a>Forkröfur

Áður en þú byrjar verður þú að setja upp og stilla Document Routing Agent og skrá síðan netprentara. Nánari upplýsingar er að finna í [Setja upp eftirlitsbúnað skjalasendingar til að virkja nettengda prentun](./install-document-routing-agent.md).

## <a name="make-the-printer-destination-available"></a>Gerðu prentaramiðstöðina tiltækan

Til að gera **Prentari** ákvörðunarstaður í boði í núverandi tilviki Microsoft Dynamics 365 Finance, farðu á vinnusvæði **Stjórnun eiginleika** og kveiktu á eftirfarandi aðgerðum, í þessari röð:

1. Umbreyta fylgiskjölum rafrænnar skýrslugerðar á útleið úr Microsoft Office-sniði í PDF
2. Document Routing Agent sem viðtökustaður rafrænnar skýrslugerðar fyrir fylgiskjöl á útleið

[![Kveikt á ákvörðunarstað ER-prentara í eiginleikastjórnun.](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)

### <a name="applicability"></a>Gildissvið

#### <a name="pdf-printing"></a>PDF-prentun

Í eldri útgáfum Finance en 10.0.18 er aðeins hægt að skilgreina áfangastaðinn **Prentari** fyrir skráhluta sem eru notaðir til að búa til framleiðsla á prentvænu PDF-sniði (**PDF-samruna** eða **PDF-skrá** sniðseiningar) eða Microsoft Office Excel og Word-snið (sniðseining **Excel-skrá**). Þegar úttak hefur verið myndað á PDF sniði er það sent til prentara. Þegar úttak er myndað á Office-sniði með **Excel-skrá** sniðseiningu er því sjálfkrafa breytt í PDF-snið og síðan sent til prentara.

Frá og með útgáfu 10.0.18 er hins vegar hægt að skilgreina áfangastað **Prentara** fyrir sniðseininguna **Almenn skrá**. Þessi sniðseining er að mestu leyti notuð til að mynda úttak á annaðhvort TXT- XML-sniði. Hægt er að skilgreina rafrænt skýrslugerðarsnið sem inniheldur sniðseininguna **Almenn skrá** sem rótarsniðseiningu og sniðseininguna **Tvíundarinnihald** sem einu földuðu eininguna undir henni. Í þessu tilfelli mun sniðseiningin **Almenn skrá** framleiða úttak á sniðinu sem tilgreint er af bindingunni sem þú skilgreinir fyrir sniðseininguna **Tvíundarinnihald**. Til dæmis er hægt að skilgreina þessa bindingu til að [fylla út](tasks/er-document-management-files-5.md#modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format) þessa einingu með efninu í viðhengi [Skjalastjórnunar](../../fin-ops/organization-administration/configure-document-management.md) á PDF- eða Office-sniði (Excel eða Word). Hægt er að prenta út útkomuna með því að nota skilgreindan viðtökustað fyrir **Prentari**. 

> [!NOTE]
> Þegar þú velur sniðseininguna **Almenn\\Skrá** til að skilgreina áfangastað **Prentara** er ekki hægt að ábyrgjast á hönnunartíma að valin eining muni koma með úttak á PDF-sniði eða úttak sem hægt er að umbreyta í PDF-snið. Af þeim sökum ættu eftirfarandi viðvörunarboð að birtast: „Tryggið að hægt sé að umbreyta úttakinu sem valinn sniðsþáttur myndar í PDF-skjal. Annars skal afmerkja valkostinn „Umbreyta í PDF-skjal“. Gera þarf ráðstafanir til að koma í veg fyrir keyrsluvandamál þegar gefið er upp úttak fyrir prentun sem er ekki PDF eða ekki hægt að umbreyta í PDF fyrir prentun við keyrslu. Ef búist er við að taka á móti úttaki Office-sniði (Excel eða Word) verður að velja valkostinn **Umbreyta í PDF**.
>
> Í útgáfu 10.0.26 og síðar, til að nota valkostinn **Umbreyta í PDF**, þarf að velja **PDF** fyrir færibreytuna **Gerð skjalaleiðar** fyrir skilgreindan áfangastað **Prentara**.

#### <a name="zpl-printing"></a>ZPL-prentun

Í útgáfu 10.0.26 og síðar er hægt að skilgreina áfangastað **Prentara** fyrir sniðseininguna **Almenn\\Skrá** með því að velja **ZPL** fyrir færibreytuna **Gerð skjalaleiðar**. Í þessu tilviki er valkosturinn **Umbreyta í PDF** hunsaður við keyrslu og TXT- eða XML-úttakið er sent beint til valins prentara með því að nota samning Zebra-forritunarmáls (ZPL) fyrir [Document Routing Agent (DRA)](install-document-routing-agent.md). Notaðu þennan eiginleika fyrir snið rafrænnar skýrslugerðar sem stendur fyrir hönnun ZPL II merkis til að prenta ýmis merki.

[![Að stilla færibreytu fyrir gerð skjalasendingar í svargluggi fyrir stillingar áfangastaðar](./media/ER_Destinations-SetDocumentRoutingType.png)](./media/ER_Destinations-SetDocumentRoutingType.png)

Frekari upplýsingar um þennan eiginleika er að finna í [Hanna nýja rafræna skýrslugerðarlausn til að prenta ZPL-merki](er-design-zpl-labels.md).

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
