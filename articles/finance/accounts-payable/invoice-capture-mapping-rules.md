---
title: Kortlagningarreglur fyrir lausn reikningsfanga
description: Þessi grein veitir upplýsingar um uppsetningu kortlagningarreglna í reikningsfangalausninni.
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
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690998"
---
# <a name="invoice-capture-solution-mapping-rules"></a>Kortlagningarreglur fyrir lausn reikningsfanga

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Kortlagningarreglur koma með helstu aðalgögn frá Microsoft Dynamics 365 Fjármál eða Enterprise Resource Planning (ERP) kerfið. Eftir að kortlagningarreglur eru settar upp eru upplýsingarnar sem þarf til að búa til lánardrottnareikninga í Finance fengnar. Þegar kortlagningarreglur eru notaðar mun viðskiptavinur (AP) skrifstofumaður athuga stöðuna í stað þess að fylla út handvirkt öll reitagildi sem vantar.

Það eru fjórar tegundir af kortlagningarreglum:

- Lögaðili
- Lykill lánardrottins
- Atriði
- Kostnaðargerð

## <a name="manage-mapping-rules-by-using-the-app"></a>Stjórnaðu kortareglum með því að nota appið

Til að stjórna kortlagningarreglum með því að nota forritið skaltu velja **Uppsetning**. The **Uppsetning kortlagningarreglu** flipinn býður upp á fjóra valkosti:

- Lögaðili 
- Lykill lánardrottins 
- Atriðakortlagning 
- Kostnaðargerð

Til dæmis velur þú **Reglur um kortlagningu lögaðila** valmöguleika. Lögaðilakóði verður auðkenndur með því að nota fyrirtækisnafn, heimilisfang og skattskrárnúmer. Fyrir reglu sem er nefnd **LE-USPM**, ef nafn fyrirtækisins inniheldur textann „Contoso Robotics USA,“ verður lögaðilakóði **USPM**.

Síðan sýnir allar virkar kortlagningarreglur. Ef þú vilt skoða óvirku kortlagningarreglurnar skaltu velja **Reglur um virka kortlagningu lögaðila**, og veldu síðan **Óvirkar kortlagningarreglur lögaðila**.

Eftirfarandi aðgerðir eru tiltækar fyrir kortlagningarreglur.

### <a name="create-a-mapping-rule"></a>Búðu til kortlagningarreglu

Þú getur notað tvær aðferðir til að búa til kortlagningarreglu:

- Veldu **Nýtt** til að búa til nýja kortlagningarreglu. Sláðu síðan inn upplýsingarnar fyrir kortlagningarregluna. The **Regluheiti** gildi ætti að vera einstakt fyrir hverja gerð vörpunarreglu.
- Ef þú velur núverandi kortlagningarreglu, **Afrita** hnappur verður tiltækur. Veldu það og veldu síðan **Allt í lagi** í glugganum sem birtist. Vörunarregla er búin til með því að afrita valda reglu.

### <a name="edit-a-mapping-rule"></a>Breyttu kortlagningarreglu

Til að breyta vörpunarreglu skaltu velja reit og breyta gildinu.

### <a name="activatedeactivate-mapping-rules"></a>Virkja/afvirkja kortlagningarreglur

Til að gera eina eða fleiri kortlagningarreglur óvirka skaltu velja þær á **Virkar kortlagningarreglur** síðu og veldu síðan **Afvirkja**. Reglurnar eru færðar úr **Virkar kortlagningarreglur** síðu til **Óvirkar kortlagningarreglur** síðu.

Sömuleiðis, til að virkja kortlagningarreglur skaltu velja þær á **Óvirkar kortlagningarreglur** síðu og veldu síðan **Virkjaðu**.

### <a name="remove-mapping-rules"></a>Fjarlægðu kortlagningarreglur

Til að fjarlægja kortlagningarreglur velurðu þær og velur svo **Eyða**.

### <a name="check-for-conflicts"></a>Athugaðu hvort árekstrar séu

Ef tvær kortlagningarreglur hafa það sama **Lögaðili** og **Reikningur söluaðila** gildi, en öðruvísi **Nafn hlutar** gildum, árekstur verður greindur og kortlagningarreglan verður ekki búin til eða uppfærð.

## <a name="importexport-mapping-rules-from-excel"></a>Inn-/útflutningur kortlagningarreglur úr Excel

Hægt er að nota Excel viðbót til að stjórna reglum í lotu. Eftirtaldir valkostir eru í boði:

- Sækja sniðmát fyrir Excel.
- Flytja út í Excel.
- Flytja inn úr Excel.

### <a name="download-an-excel-template"></a>Sækja sniðmát fyrir Excel

Til að hlaða niður Excel sniðmáti skaltu velja **Sækja sniðmát**. Veldu síðan reiti sem á að hafa með í sniðmátinu.

### <a name="export-to-excel"></a>Flytja út í Excel

Þú getur flutt út á tvo vegu:

- Veldu **Opnaðu í Excel Online** til að opna skrána í Excel. Þú getur síðan breytt skránni á netinu. Þegar þessu er lokið skal velja **Vista**. Allar breytingar þínar verða vistaðar á **Kortlagningarregla** síðu.
- Veldu **Sækja vinnublað** að hlaða niður Excel skrá sem inniheldur kortlagningarreglur. Þú getur síðan breytt skránni. Þegar þú hefur lokið skaltu velja **Flytja inn úr Excel** til að hlaða upp uppfærðu vinnublaðinu.

### <a name="import-from-excel"></a>Flytja inn úr Excel

1. Veldu **Flytja inn úr Excel** til að flytja inn gögn úr XLSX skrá. Þú getur líka flutt inn úr kommum aðskilin gildi (CSV) eða XML skrár. Áður en þú flytur inn ættir þú að ákveða hvort afrit séu leyfð.
2. Veldu **Skoðaðu kortlagningu** til að endurskoða eiginleika kortlagningu og ákvarða hvort hún sé rétt. Þú getur breytt kortlagningarsambandinu.
3. Þegar þú hefur lokið skaltu velja **Ljúka innflutningi** til að hefja innflutning.
4. Þú getur valið **Rekja ferli** til að fylgjast með framvindu innflutningsferlisins.

    Innflutningsstaðan er uppfærð frá **Klára** til **Dálka**, þá til **Umbreytir**, og að lokum til **Lokið**.

Þegar innflutningsferlinu er lokið birtast tölfræði um árangur, bilanir að hluta, villur og heildarvinnslu.
