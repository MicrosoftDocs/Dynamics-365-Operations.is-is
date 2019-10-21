---
title: Virkja frestun skattaútreiknings á dagbók
description: Þetta efni útskýrir hvernig á að nota eiginleikann **Virkja frestun skattaútreiknings á dagbók** til að bæta afköst skattaútreikninga þegar magn dagbókarlína er mikið.
author: ericwang
manager: Ann Beebe
ms.date: 09/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2019-09-18
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 5a8ae30a007d3e2b8b7a9bc9eb7786f6e58246d0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178245"
---
# <a name="enable-delayed-tax-calculation-on-journal"></a>Virkja frestun skattaútreiknings á dagbók
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Þetta efni útskýrir hvernig á að nota eiginleikann **Virkja frestun skattaútreiknings á dagbók** til að bæta afköst skattaútreikninga þegar magn dagbókarlína er mikið.

Núverandi hegðun útreiknings á söluskatti á dagbók virkjast í rauntíma þegar notandi uppfærir skattskylda reiti, t.d. VSK-skattshóp/VSK-skattshóp vöru. Sérhver uppfærsla á dagbókarlínustigi reiknar skattfjárhæð á alla dagbókarlínur. Það hjálpar notendum að sjá reiknaðan skattfjárhæð í rauntíma, en það gæti einnig leitt af sér vandamál með afköst ef magn dagbókarlína er mikið.

Þessi eiginleiki veitir möguleika á að fresta útreikningi skatta til að leysa vandamál með afköst. Ef kveikt er á þessum eiginleika verður skattafjárhæð einungis reiknuð þegar notandi smellir á skipunina „Virðisaukaskatt“ eða bókar færslubókina.

Notandi getur kveikt/slökkt á færibreytunni á þremur stigum:
- Eftir lögaðila
- Eftir heiti færslubókar
- Eftir færslubókarhaus

Kerfið mun taka færibreytugildið á færslubókarhaus sem endanlegt. Færibreytugildi á færslubókarhaus er sjálfgefið frá nafni færslubókar. Færibreytugildi á færslubókarheiti verður sjálfgefið frá aðalbókarbreytunni þegar færslubókarheitið er búið til.

Reitirnir „Eiginleg virðisaukaskattsupphæð“ og „Reiknuð virðisaukaupphæð“ í færslubókinni verða faldir ef kveikt er á þessari færibreytu. Tilgangurinn er ekki að rugla notanda þar sem gildi þessara tveggja reita mun alltaf sýna 0 áður en notandi kveikir á skattútreikningi.

## <a name="enable-delayed-tax-calculation-by-legal-entity"></a>Virkja frestun skattaútreikninga af lögaðila

1. Farðu í **Fjárhagur > Fjárhagsuppsetning > Færibreytur fyrir fjárhag**
2. Smelltu á flipann **Vsk.**
3. Undir flýtiflipanum **Almennt** finnurðu færibreytuna **Frestun skattaútreikings** og kveikir/slekkur á henni

![](media/delayed-tax-calculation-gl.png)



## <a name="enable-delayed-tax-calculation-by-journal-name"></a>Virkja frestun skattaútreiknings eftir heiti færslubókar

1. Farðu í **Fjárhag > Færslubókaruppsetning > Heiti færslubókar**
2. Undir flýtiflipanum **Almennt** finnurðu færibreytuna **Frestun skattaútreikings** og kveikir/slekkur á henni

![](media/delayed-tax-calculation-journal-name.png)

## <a name="enable-delayed-tax-calculation-by-journal"></a>Virkja frestun skattaútreiknings eftir færslubók

1. Farðu í **Fjárhag > Færslubókarfærslur > Almennar færslubækur**
2. Smelltu á **Nýtt**
3. Veldu heiti færslubókar
4. Smelltu á **Uppsetningu**
5. Finndu færibreytuna **Frestun skattaútreiknings**, kveiktu/slökktu á henni

![](media/delayed-tax-calculation-journal-header.png)
