---
title: Vörpunarreglur Invoice Capture-lausnar
description: Þessi grein veitir upplýsingar um uppsetningu vörpunarreglan í lausninni Invoice capture.
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: cd0d06f7fd3ed946756e975d0706687c2d4acc93
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690998"
---
# <a name="invoice-capture-solution-mapping-rules"></a>Vörpunarreglur Invoice Capture-lausnar

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Vörpunar koma með grunngögn frá Office Microsoft Dynamics 365 Finance eða ERP-kerfinu. Eftir að vörpunarreglur hafa verið settar upp er aflað upplýsinga sem þarf til að búa til sölureikninga í Finance. Þegar vörpunarreglur eru notaðar munu viðskiptaskuldir athuga stöðuna í stað þess að fylla handvirkt inn öll gildi sem vantar í reitinn.

Til eru fjórar tegundir vörpunarreglna:

- Lögaðili
- Lykill lánardrottins
- Atriði
- Kostnaðargerð

## <a name="manage-mapping-rules-by-using-the-app"></a>Hafðu umsjón með vörpunarreglum með því að nota forritið

Til að stjórna vörpunarreglum með forritinu velur þú **Uppsetning**. Flipinn **Uppsetning vörpunarreglu** gefur fjóra valkosti:

- Lögaðili 
- Lykill lánardrottins 
- Vöruvörpun 
- Kostnaðargerð

Þú velur til dæmis valkostinn **Vörpunarreglur lögaðila**. Kóði lögaðila verður auðkenndur með því að nota nafn fyrirtækis, heimilisfang og skattskráningarnúmer. Fyrir reglu sem kallast **LE-USPM** ef heiti fyrirtækisins inniheldur textann „Contoso Robotics USA“ verður kóði lögaðilans **USPM**.

Síðan sýnir allar virku kortlagningarreglurnar. Ef þú vilt skoða óvirkar vörpunarreglur skaltu velja **Virkar vörpunarreglur lögaðila** og velja síðan **Óvirkar vörpunarreglur lögaðila**.

Eftirtaldar aðgerðir er hægt að stilla fyrir vörpunarreglur.

### <a name="create-a-mapping-rule"></a>Búa til vörpunarreglu

Nota má tvær aðferðir til að stofna vörpunarreglu:

- Velja skal **Nýtt** til að búa til nýja vörpunarreglu. Sláðu síðan inn upplýsingarnar fyrir vörpunarregluna. Gildið **Regluheiti** ætti að vera einstakt fyrir hverja gerð vörpunarreglu.
- Ef þú velur fyrirliggjandi vörpunarreglu verður **Afrita** hnappurinn tiltækur. Veldu það og svo í  svarglugganum sem birtist skal velja **Í lagi**. Vörpunarregla er búin til með því að afrita valda reglu.

### <a name="edit-a-mapping-rule"></a>Breyta vörpunarreglu

Til að breyta vörpunarreglu skaltu velja reit og breyta gildinu.

### <a name="activatedeactivate-mapping-rules"></a>Gera vörpunarreglur virkar/óvirkar

Til að afvirkja eina eða fleiri vörpunarreglur velur þú þær á síðunni **Virkar vörpunarreglur** og velur svo **Afvirkja**. Reglurnar eru færðar af síðunni **Virkja vörpunarreglur** kortareglur á síðuna **Óvirkar vörpunarreglur**.

Sömuleiðis til að virkja vörpunarreglur skal velja þær á síðunni **Óvirkar vörpunarreglur** og velja síðan **Virkja**.

### <a name="remove-mapping-rules"></a>Fjarlægja vörpunarreglu

Til að fjarlægja vörpunarreglu skaltu velja þær og velja svo **Eyða**.

### <a name="check-for-conflicts"></a>Leita að árekstrum

Ef tvær vörpunarreglur hafa sömu gildi fyrir **Lögaðili** og **Lykill lánardrottins**, en mismunandi gildi fyrir **Vöruheiti**, verður árekstrar vart og vörpunarreglan verður ekki búin til eða uppfærð.

## <a name="importexport-mapping-rules-from-excel"></a>Innflutningur- og útflutningur vörpunarregla úr Excel

Hægt er að nota Excel viðbót til að stjórna reglum í lotu. Eftirtaldir valkostir eru í boði:

- Sækja Excel-sniðmát.
- Flytja inn í Excel.
- Flytja inn úr Excel.

### <a name="download-an-excel-template"></a>Sækja Excel-sniðmát

Til að sækja Excel-sniðmát skal velja **Sækja sniðmát**. Veljið svæðin sem nota á í sniðmátinu.

### <a name="export-to-excel"></a>Flytja út í Excel

Hægt er að flytja út á tvo vegu:

- Veldu **Opna í Excel Online** til að opna skrána í Excel. Hægt er að breyta skránni á netinu. Þegar þessu er lokið skal velja **Vista**. Allar breytingar sem þú hefur gert verða vistaðar á **Vörpunarregla** síðunni.
- Veldu **Sækja vinnublað** til að hlaða niður Excel-skrá sem inniheldur vörpunarreglur. Síðan er hægt að breyta skránni. Að þessu loknu skaltu velja **Flytja inn úr Excel** til að hlaða upp uppfærðu vinnublaðinu.

### <a name="import-from-excel"></a>Flytja inn úr Excel

1. Veldu **Flytja inn úr Excel** til að flytja inn gögn úr XLSX-skrá. Einnig er hægt að flytja inn úr aðgreindum gildum (CSV) eða XML skrám. Áður en þú flytur inn ættir þú að ákveða hvort tvítekningar séu leyfðar.
2. Veldu **Yfirfara vörpun** til að fara yfir eiginleikana og ákvarða hvort þeir séu réttir. Hægt er að breyta vörpunarsambandinu.
3. Þegar þú hefur lokið skaltu velja **Ljúka innflutningi** til að hefja innflutninginn.
4. Hægt er að velja **Rekja ferli** til að rekja framvindu innflutningsferlisins.

    Innflutningsstaðan er uppfærð úr **Ljúka** í **Þáttun**, síðan í **Ummyndun** og loks í **Lokið**.

Þegar innflutningsferlinu er lokið er tölfræði yfir árangur, bilanir, villur og heildarúrvinnslu sýnd.
