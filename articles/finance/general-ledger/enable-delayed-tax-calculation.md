---
title: Virkja frestun skattaútreiknings á dagbókum
description: Þetta efni útskýrir hvernig á að kveikja á eiginleikanum Frestun skattaútreiknings að bæta afköst skattaútreikninga þegar fjöldi dagbókarlína er afar mikið.
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
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-09-18
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 4ea79747e8e7c078baa6e270ecebf88c4832e079
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968805"
---
# <a name="enable-delayed-tax-calculation-on-journals"></a>Virkja frestun skattaútreiknings á dagbókum
[!include [banner](../includes/banner.md)]


Þetta efni útskýrir hvernig þú getur seinkað útreikningi á söluskatti í færslubókum. Þessi geta hjálpar til við að bæta afköst skattaútreikninga þegar margar færslubókarlínur eru til staðar.

Sjálfgefið er að fjárhæðir söluskatts í færslubókarlínum eru reiknaðar út í hvert skipti sem skattatengdir reitir eru uppfærðir. Þessir reitir innihalda reiti fyrir VSK-flokka og VSK-flokka vöru. Sérhver uppfærsla á færslubókarlínu veldur því að skattfjárhæðir eru endurreiknaðar fyrir allar dagbókarlínur. Þrátt fyrir að þessi hegðun hjálpi notendum að sjá skattaupphæðir reiknaðar í rauntíma getur það einnig haft áhrif á afköst ef fjöldi færslubókarlína er mjög mikill.

Aðgerðin fyrir útreikning á sköttum gerir kleift að fresta skattaútreikningi á færslubókum og hjálpar því til við að laga afkastavandamál. Þegar kveikt er á þessum eiginleika verða skattaupphæðir aðeins reiknaðar þegar notandi velur **Virðisaukaskatt** eða bókar færslubókina.

Þú getur tafið útreikning á VSK-skatti á þremur stigum:

- Lögaðili
- Heiti færslubókar
- Færslubókarhaus

Kerfið hefur forgang til stillingar fyrir færslubókarhaus. Sjálfgefið er að þessi stilling er tekin úr nafni færslubókarinnar. Sjálfgefið er að stillingin fyrir færslubókarheitið sé tekin úr stillingunni á síðunni **Almennar fjárhagsbreytur** þegar færslubókarheitið er búið til. Eftirfarandi kaflar útskýra hvernig á að kveikja á seinkuðum útreikningum á skatti lögaðila, færslubókarheiti og færslubókarhausum.

## <a name="turn-on-delayed-tax-calculation-at-the-legal-entity-level"></a>Kveiktu á frestun skattaútreiknings á stigi lögaðila

1. Farðu í **Fjárhag \> Fjárhagsuppsetning \> Fjárhagsfæribreytur**.
2. Á flipanum **VSK-skattur** á flýtiflipanum **Almennt** skal stilla valkostinn **Frestun skattaútreiknings** á **Já**.

![Mynd af almennum fjárhagsfæribreytum](media/delayed-tax-calculation-gl.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-name-level"></a>Kveiktu á frestun skattaútreiknings á stigi færslubókarheitis

1. Farðu í **Fjárhag \> Færslubókaruppsetning \> Færslubókarheiti**.
2. Á flýtiflipanum **Almennt**, í kaflanum **VSK-skattur**, skal stilla valkostinn **Frestun skattaútreiknings** á **Já**.

![Mynd af færslubókanöfnum](media/delayed-tax-calculation-journal-name.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-header-level"></a>Kveiktu á frestun skattaútreiknings á stigi færslubókarhauss

1. Farðu í **Fjárhag \> Færslubókarfærslur \> Almennar færslubækur**.
2. Veljið **Nýtt**.
3. Veldu heiti færslubókar.
4. Á flipanum **Uppsetning** stillirðu valkostinn **Frestun skattaútreiknings** á **Já**.

![Mynd af síðu almennrar færslubókar](media/delayed-tax-calculation-journal-header.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]