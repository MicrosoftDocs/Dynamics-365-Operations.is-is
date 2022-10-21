---
title: Útreikningar á inn- og útflutningsgjaldi
description: Þessi grein veitir upplýsingar um inn- og útflutningsvirkni skattreikningsþjónustunnar.
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
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690234"
---
# <a name="import-and-export-tax-calculations"></a>Útreikningar á inn- og útflutningsgjaldi

Þessi grein veitir upplýsingar um inn- og útflutningsvirkni skattreikningsþjónustunnar. Þessi virkni hjálpar til við að tryggja sveigjanlega og skilvirka uppsetningarupplifun.

## <a name="import-and-export-tax-codes"></a>Inn- og útflutningsskattanúmer

### <a name="export-templates"></a>Flytja út sniðmát

1. Skrá inn [Regulatory Configuration Service (RCS)](https://marketing.configure.global.dynamics.com/).
2. Í **Hnattvæðingareiginleikar** vinnusvæði, veldu **Eiginleikar**, og veldu síðan **Skattútreikningur** flísar.
3. Veldu núverandi eiginleika, eða [búa til nýjan eiginleika](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs).
4. Í **Útgáfur** rist, veldu **Breyta**.
5. Á **Skattútreikningur** eiginleikasíðu, stilltu [stillingarútgáfu](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs).
6. Á **Skattkóðar** flipa, veldu **Flytja inn**.
7. Veldu **Flytja út skattakóðasniðmát** til að hlaða niður **TaxCodesTemplate.zip** skrá.
8. Renndu niður **TaxCodesTemplate.zip**. Skattkóðasniðmátið er þjappað sérstaklega skv **Uppruni útreiknings** gildi.
9. Renndu niður **Eftir Netto Amount.zip** til að fá eftirfarandi með kommum aðskilin gildi (CSV) skrár:

    - **TaxCode.csv** – Sláðu inn skattanúmerin.
    - **TaxLimit.csv** – Sláðu inn skattamörk fyrir hvern skattkóða.
    - **TaxRate.csv** – Sláðu inn skatthlutföll fyrir hvern skattkóða.

> [!NOTE]
> Sjálfgefið er að færslur fyrir **Sýnishorn** skattakóði er tiltækur í sniðmátunum. Ef **Sýnishorn** skattkóði er ekki fjarlægður úr CSV skránum, hann verður fluttur inn í eiginleikann.

### <a name="import-tax-codes"></a>Innflutningsskattanúmer

Fylgdu þessum skrefum til að flytja inn **Sýnishorn** skattkóða í sniðmátinu í skattútreikningsaðgerðina þína.

1. Í RCS, á **Skattútreikningur** eiginleikasíðu, á **Skattkóðar** flipa, veldu **Flytja inn**.
2. Veldu **Skoðaðu**, finndu og veldu **TaxCode.csv** skrá, og síðan í **Markborð** reit, veldu **Skattkóði**.
3. Veldu **Allt í lagi** að flytja inn skattanúmerið.
4. Finndu og veldu **TaxRate.csv** skrá, og síðan í **Markborð** reit, veldu **Skatthlutfall**.
5. Veldu **Allt í lagi** að flytja inn skattprósentuna.
6. Finndu og veldu **TaxLimit.csv** skrá, og síðan í **Markborð** reit, veldu **Skatttakmark**.
7. Veldu **Allt í lagi** að flytja inn skattahámarkið.

Þú getur líka flutt beint inn zip skrána sem inniheldur allar þrjár CSV skrárnar. Þannig geturðu fljótt og auðveldlega klárað innflutninginn.

1. Í RCS, á **Skattútreikningur** eiginleikasíðu, á **Skattkóðar** flipa, veldu **Flytja inn**.
2. Veldu **Skoðaðu**, finndu og veldu **Eftir Netto Amount.zip** skrá og veldu síðan **Allt í lagi**.

### <a name="export-tax-codes"></a>Útflutningsskattanúmer

1. Í RCS, á **Skattútreikningur** eiginleikasíðu, á **Skattkóðar** flipa, veldu **Útflutningur**.

    The **Útflutningur** hnappur er tiltækur þegar það er að minnsta kosti einn skattkóði í **Skattkóðar** rist.

2. Veldu **Allt í lagi** til að flytja út alla skattkóða eiginleikans í zip skrá.

> [!NOTE]
> Notaðu útfluttu skrána sem sniðmát til að flytja inn skattkóða í samsvarandi eiginleika.

## <a name="import-and-export-applicability-rules"></a>Innflutnings- og útflutningsreglur

### <a name="export-applicability-rules"></a>Útflutningsgildisreglur

1. Skráðu þig inn í [RCS](https://marketing.configure.global.dynamics.com/).
2. Í **Hnattvæðingareiginleikar** vinnusvæði, veldu **Eiginleikar**, og veldu síðan **Skattútreikningur** flísar.
3. Veldu núverandi eiginleika, eða [búa til nýjan eiginleika](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs).
4. Í **Útgáfur** rist, veldu **Breyta**.
5. Á **Skattútreikningur** eiginleikasíðu, stilltu [stillingarútgáfu](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs).
6. Á **Gildistími skattaflokka** flipann, veldu línurnar í **Settu upp gildandi skattaflokka** rist.
7. Veldu **Opið inn Microsoft Office** hnappinn og veldu síðan **Kraftmikið nothæfisfylki skattaþjónustu**.

    [![Flytja út gildisreglur til Microsoft Excel á síðunni Skattútreikningur eiginleikar.](./media/tax-cal-import-export-1.png)](./media/tax-cal-import-export-1.png)

8. Veldu **Sækja** til að flytja valdar línur til a Microsoft Excel vinnublað.

### <a name="import-applicability-rules"></a>Innflutningsgildisreglur

Excel vinnublaðið sem þú hleður niður inniheldur uppbyggingu **Settu upp gildandi skattaflokka** rist. Þú getur bætt við nýjum reglum beint í vinnublaðið. Þegar þú hefur lokið við skaltu fylgja þessum skrefum til að flytja nýju reglurnar aftur inn í **Settu upp gildandi skattaflokka** rist.

1. Í Excel vinnublaðinu skaltu velja og afrita línurnar til að flytja inn.
2. Í RCS, á **Skattútreikningur** eiginleikasíðu, á **Gildistími skattaflokka** flipa, veldu **Bæta við** til að setja inn tóma skrá neðst á **Settu upp gildandi skattaflokka** rist.
3. Veldu **Ctrl+V** til að líma afrituðu línurnar inn í ristina.
4. Veldu **Vista**.

## <a name="import-feature-demo-data"></a>Flytja inn kynningargögn fyrir eiginleika

Fylgdu þessum skrefum til að flytja inn kynningargögn um eiginleika.

1. Skráðu þig inn í [RCS](https://marketing.configure.global.dynamics.com/).
2. Í **Hnattvæðingareiginleikar** vinnusvæði, veldu **Eiginleikar**, og veldu síðan **Skattútreikningur** flísar.
3. Veldu **Flytja inn**, og síðan, á **Flytja inn eiginleiki frá alþjóðlegri geymslu** síðu, veldu **Samstilla**. 
4. Í töflunni skaltu velja **skatt-útreikning-eiginleika-sýnishorn-gögn** eiginleiki og veldu síðan **Flytja inn**.
5. Veldu **Útsýni** til að skoða skattakóða, hópa og gildandi reglur sem eru skilgreindar í innfluttu eiginleikanum.
6. Í Fjármálum skaltu skipta yfir í **DEMF** lögaðila, og fara síðan til **Skattur** \> **Uppsetning** \> **Skattstilling** \> **Skattreikningsbreytur**.
7. Á **Almennt** flipa, veldu **Virkja skattreikningsþjónustu**.
8. Í **Heiti eiginleikauppsetningar** reit, veldu **skatt-útreikning-eiginleika-sýnishorn-gögn**.
9. Veldu a **Uppgjörstímabil** og a **Fjárhagsbókunarhópur** fyrir nýju kynningarskattakóðana og veldu síðan **Staðfesta**.
10. Veldu **Vista**.

> [!NOTE]
> The **skatta-útreikning-eiginleika-sýni-gögn** kynningu eiginleiki er byggður á lögun útgáfu **40.54.234** og hannað fyrir **DEMF** kynningu lögaðila. Gakktu úr skugga um að Finance og RCS séu uppfærð í útgáfu 10.0.26 eða nýrri.
