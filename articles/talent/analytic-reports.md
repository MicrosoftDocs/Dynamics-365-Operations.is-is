---
title: Notaðu greiningarskýrslur í Attract
description: Þetta efni lýsir greiningarskýrslum fyrir ráðningu á ferli í Microsoft Dynamics 365 Talent - Attract
author: fewatson
manager: AnnBe
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: fewatson
ms.search.validFrom: 2019-04-30
ms.dyn365.ops.version: Talent April 2019 update
ms.openlocfilehash: 081988e8b8cfe1e2ddb533247b678ba38a07f5f1
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092224"
---
# <a name="use-analytic-reports-in-attract"></a>Notaðu greiningarskýrslur í Attract

[!include [banner](includes/banner.md)]

Greiningarskýrslur í Microsoft Dynamics 365 Talent: Attract veita tilbúna lausn fyrir innsýn í ráðningarferlin. Tiltækar aðgerðir eru meðal annars:

- **Starfsgreiningar** Smellið á flipann **Greiningar** innan starfs fyrir mæligildi umsækjenda starfs.
- **Greiningarmiðstöð** Smellið á **Greiningar** vinstra megin á yfirlitinu fyrir samantekin mæligildi allra starfa.
- **Notandamiðað öryggi** - Aðgangur að skýrslum er stjórnað af Attract [hlutverki](security-attract.md) og hlutverki þátttakanda í starfi.
- **Krosssíun** Smellið á myndefni innan skýrslu til að skoða önnur síuð mæligildi valdra gagna.

>[!NOTE] 
>- Þessi eiginleiki er í [forútgáfu](access-preview-feature.md) sem stendur. Til að reyna hana er nauðsynlegt að vera með [**Viðbót við alhliða ráðningar**](attract-comprehensive-hiring.md).
>- Allar opinberar forskoðunarskýrslur birtast á ensku.
>- Skýrslur endurhlaðast á 3 tíma fresti. Tími síðustu endurhleðslu (í staðbundnu tímabelti) er að finna efst í skýrslunni. Endurhleðslutímar eru ekki nákvæmir og eru breytilegir út af gagnamagni og tilfangahleðslu í þínu svæði.

## <a name="job-analytics"></a>Greining starfs

Starfsgreiningaskýrslur eru skyndimynd af ráðningarferli fyrir starf.  Helstu mæligildi eru:

- Virkir umsækjendur eftir stigi
- Uppruni umsækjanda
- Gerð umsækjanda (innan eða utan fyrirtækis)

## <a name="analytics-hub"></a>Greiningarmiðstöð

Skýrslur greiningarmiðstöðvar taka saman gögn frá öllum störfum til að bera kennsl á mynstur í ráðningarferlinu. Attract inniheldur tvær tilbúnar skýrslur: Sölukeðjuyfirlit og trektargreining.

### <a name="pipeline-summary"></a>Sölukeðjuyfirlit

Skýrsla sölukeðjuyfirlits safnar saman gögnum fyrir opin störf. Helstu mæligildi eru:

- Umsækjendur í öllum störfum eftir stigi
- Uppruni umsækjanda
- Laus störf eftir starfsaldri

### <a name="funnel-analysis"></a>Trektargreining

Skýrsla trektargreiningar safnar saman gögnum fyrir störf sem hafa verið lokuð sem útfyllt. Helstu mæligildi eru:

- Tími fyrir ráðningu
- Mælikvarðar breytinga (þegar bendli er haldið yfir)
- Tíðni tilboðssamþykktar

Til athugunar: Skýrslugerð um nákvæmasta tíma til að ráða er mælt með því að þú notir [Tilboðsstjórnun](offer-setup.md), eiginleiki sem er í boði sem hluti af viðbót við alhliða ráðningar.

>[!TIP] 
>Prófaðu að halda bendli yfir myndefni fyrir frekari upplýsingar. Dæmi: Að halda bendli yfir myndefninu **Virkir umsækjendur** birtir meðalfjölda daga á stigi. Að greina þessar upplýsingar getur veitt mikilvæga innsýn í að draga úr tíma til að ráða og gert ráðningaraðilum kleift að einblína á leiðir til að draga úr tímanum sem fer í hvert stig.

## <a name="user-specific-security"></a>Öryggi sem miðast við notanda

Attract-skýrslur eru aðgengilegar fyrir stjórnanda, Lesa allt, Ráðningaraðila og Ráðningarstjóra [hlutverk](security-attract.md). Óúthlutaðir notendur hafa ekki aðgang að síðum greiningarskýrslunnar (Starfsgreiningar eða Starfsgreiningarmiðstöðvar).

Skýrslur starfsgreiningar sýna gögn fyrir valið starf. Skýrslur starfsgreiningarmiðstöðvar safna saman gögnum frá öllum störfum sem notandi getur skoðað. Notendur sem geta skoðað bæði Mín störf og Öll störf á starfasíðunni eru með sömu yfirlitin tiltæk í Starfsgreiningarmiðstöðinni.

## <a name="cross-filter"></a>Krosssíun

Einn af frábærum eiginleikum Power BI er hvernig allt myndefni á skýrslusíðu er tengt innbyrðis. Ef gagnapunktur er valinn í einu myndefnanna, breytist allt annað myndefni á síðunni sem inniheldur þessi gögn, á grunni þessa vals. Fáðu að vita meira og sjáðu dæmi í [Hvernig myndefni krosssía hvert annað í Power BI-skýrslu](https://docs.microsoft.com/power-bi/consumer/end-user-interactions).

## <a name="export-to-excel"></a>Flytja út í Excel

Til að skoða skýrslugögn í Excel er hægt að smella á valmyndina fyrir valkosti (þrír punktar) í myndefni og velja **Flytja út undirliggjandi gögn**. Útflutt gögn flytjast út sem síuð, tekur mið af heimildum notanda í Attract. Frekari upplýsingar eru í [Flytja gögn út úr myndrænum framsetningum](https://docs.microsoft.com/power-bi/visuals/power-bi-visualization-export-data).
