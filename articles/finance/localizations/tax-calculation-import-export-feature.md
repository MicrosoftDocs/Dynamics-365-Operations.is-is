---
title: Útreikningar á inn- og útflutningsgjaldi
description: Þessi grein veitir upplýsingar um innflutnings- og útflutningsvirkni skattútreikningsþjónustunnar.
author: Kai-Cloud
ms.date: 10/17/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-11-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 8666d4971e36279ebd2b1396de7cab37680980e6
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690234"
---
# <a name="import-and-export-tax-calculations"></a>Útreikningar á inn- og útflutningsgjaldi

Þessi grein veitir upplýsingar um innflutnings- og útflutningsvirkni skattútreikningsþjónustunnar. Þessi virkni hjálpar til við að tryggja sveigjanlega og skilvirka skilgreiningu.

## <a name="import-and-export-tax-codes"></a>Flytja skattkóða inn og út

### <a name="export-templates"></a>Flytja út sniðmát

1. Skrá inn á [Regulatory Configuration Service (RCS)](https://marketing.configure.global.dynamics.com/).
2. Á vinnusvæðinu **Altækir eiginleikar** skal velja **Eiginleikar** og síðan velja reitinn **Skattaútreikningur**.
3. Veljið fyrirliggjandi eiginleika eða [stofnið nýjan eiginleika](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs).
4. Í reitnum **Útgáfur** skaltu velja **Breyta**.
5. Á síðunni **Skattaútreikningur** skaltu stilla [útgáfa skilgreininga](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs).
6. Í flipanum **Skattkóðar** skal velja **Flytja inn**.
7. Veljið **Flytja út skattkóðasniðmát** til að sækja skrána **TaxCodesTemplate.zip**.
8. Afþjappið **TaxCodesTemplate.zip**. Skattkóðasniðmát eru þjöppuð hvert fyrir sig í samræmi við **Upprunagildi**.
9. Afþjappið **By Net Amount.zip** til að fá eftirfarandi CSV-skrár (aðskildar með kommum):

    - **TaxCode.csv** – Færið inn skattkóðana.
    - **TaxLimit.csv** – Færið inn skattmörk fyrir hvern skattkóða.
    - **TaxRate.csv** – Færið inn skatthlutföll fyrir hvern skattkóða.

> [!NOTE]
> Sjálfgefið er að færslur fyrir **Dæmi** skattkóða séu tiltækar í sniðmátunum. Ef **Dæmi** skattkóða ekki fjarlægður úr CSV-skránum verður hann fluttur inn í eiginleikann.

### <a name="import-tax-codes"></a>Flytja inn skattkóða

Fylgdu þessum skrefum til að flytja **Dæmi** skattkóðann í sniðmátinu í eiginleika skattaútreiknings.

1. Í RCS á eiginleikasíðunni **Skattaútreikningur** á flipanum **Skattkóðar** skal velja **Flytja inn**.
2. Veldu **Vafra**, finndu og veldu skrána **TaxCode.csv** og svo, í reitnum **Marktafla** veldurðu **Skattkóði**.
3. Veljið **Í lagi** til að flytja inn skattkóðann.
4. Finnið og veljið **TaxRate.csv** skrána, og síðan í reitnum **Marktafla**, veljið **Skatthlutfall**.
5. Veljið **Í lagi** til að flytja inn skatthlutfallið.
6. Finna og velja **TaxLimit.csv** skrána, og síðan, í reitnum **Marktafla**, veljið **Skattmörk**.
7. Veljið **Í lagi** til að flytja inn skattmörkin.

Einnig er hægt að flytja beint inn zip-skrá sem inniheldur allar þrjár CSV-skrárnar. Á þennan hátt er hægt að ljúka innflutningnum á fljótlegan og auðveldan hátt.

1. Í RCS á eiginleikasíðunni **Skattaútreikningur** á flipanum **Skattkóðar** skal velja **Flytja inn**.
2. Veljið **Fletta**, finnið og veljið skrána **By Net Amount.zip** og veljið síðan **Í lagi**.

### <a name="export-tax-codes"></a>Útflutningsskattkóðar

1. Í RCS á eiginleikasíðunni **Skattaútreikningur** á flipanum **Skattkóðar** skal velja **Flytja út**.

    Hnappurinn **Flytja út** er tiltækur þegar að minnsta kosti einn skattkóði er til staðar í töflunni **Skattkóðar**.

2. Veldu **Í lagi** til að flytja út alla skattkóða eiginleikans í ZIP-skrá.

> [!NOTE]
> Notaðu útfluttu skrána sem sniðmát til að flytja skattkóða inn í samsvarandi eiginleika.

## <a name="import-and-export-applicability-rules"></a>Flytja inn og út gildissviðsreglur

### <a name="export-applicability-rules"></a>Flytja út gildissviðsreglur

1. Skráðu þig inn í [RCS](https://marketing.configure.global.dynamics.com/).
2. Á vinnusvæðinu **Altækir eiginleikar** skal velja **Eiginleikar** og síðan velja reitinn **Skattaútreikningur**.
3. Veljið fyrirliggjandi eiginleika eða [stofnið nýjan eiginleika](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs).
4. Í reitnum **Útgáfur** skaltu velja **Breyta**.
5. Á síðunni **Skattaútreikningur** skaltu stilla [útgáfa skilgreininga](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs).
6. Á flipanum **Gildissvið skattflokks** er hægt að velja raðir í töflunni **Setja upp gildissvið skattflokks**.
7. Veljið hnappinn **Opna í Microsoft Office** og svo **Kvikt gildisfylki skattþjónustu**.

    [![Að flytja út gildissviðsreglur Microsoft Excel á eiginleikasíðu skattaútreiknings.](./media/tax-cal-import-export-1.png)](./media/tax-cal-import-export-1.png)

8. Veljið **Sækja** til að flytja valdar raðir á Microsoft Excel vinnublað.

### <a name="import-applicability-rules"></a>Flytja inn gildissviðsreglur

Excel-vinnublaðið sem þú sóttir inniheldur uppbyggingu töflunnar **Setja upp gildissvið skattflokks**. Hægt er að bæta við nýjum reglum beint í vinnublaðinu. Að því loknu skaltu fylgja eftirfarandi skrefum til að flytja nýju reglurnar aftur inn í töfluna **Setja upp gildissvið skattflokks**.

1. Í Excel-vinnublaðinu skal velja og afrita raðirnar sem á að flytja inn.
2. Í RCS, á eiginleikasíðunni **Skattaútreikningur** á flipanum **Gildissvið skattflokks** velurðu **Bæta við** til að setja inn tóma færslu neðst í töfluna **Setja upp gildissvið skattflokks**.
3. Veldu **Ctrl+V** til að líma afrituðu raðirnar inn í töfluna.
4. Veldu **Vista**.

## <a name="import-feature-demo-data"></a>Sýnigögn innflutningseiginleika

Fylgið þessum skrefum til að flytja inn sýnigögn eiginleika.

1. Skráðu þig inn í [RCS](https://marketing.configure.global.dynamics.com/).
2. Á vinnusvæðinu **Altækir eiginleikar** skal velja **Eiginleikar** og síðan velja reitinn **Skattaútreikningur**.
3. Veldu **Flytja inn** og svo á síðunni **Flytja inn eiginleika úr altækri geymslu** veldu **Samstilling**. 
4. Í töflunni skal velja eiginleikann **tax-calculation-feature-demo-data** og svo **Flytja inn**.
5. Veldu **Skoða** til að fara yfir skattkóða, hópa og gildissviðsreglur sem eru skilgreind í innflutta eiginleikanum.
6. Í Finance skal skipta yfir í **DEMF** lögaðilann og fara svo í **Uppsetning** \> **skatts** \> **Skattaskilgreining** \> **Færibreytur skattaútreiknings**.
7. Í flipanum **Almennt** skal velja **Virkja skattaútreikningsþjónustu**.
8. Í reitnum **Uppsetningarheiti eiginleika** velurðu **tax-calculation-feature-demo-data**.
9. Veldu **Jöfnunartímabil** og **Fjárhagsbókunarflokkur** fyrir nýja sýniskattkóða og svo **Staðfesta**.
10. Veldu **Vista**.

> [!NOTE]
> Sýnieiginleikinn **tax-calculation-feature-demo-data** byggir á eiginleikaútgáfu **40.54.234** og er hannaður fyrir **DEMF** sýnilögaðilann. Gakktu úr skugga um að Finance og RCS séu uppfærð í útgáfu 10.0.26 eða nýrri.
