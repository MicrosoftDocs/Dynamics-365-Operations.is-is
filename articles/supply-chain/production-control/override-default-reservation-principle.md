---
title: Hnekkja sjálfgefinni frátekningarreglu fyrir efni í framleiðslu
description: Þetta efnisatriði lýsir því hvernig á að setja upp sjálfgefna frátekningarreglu fyrir hvern vörulíkanaflokk, svo hægt sé að nota mismunandi frátekningarreglur sjálfkrafa fyrir hverja vöru sem er hluti af formúlu framleiðsluuppskriftar eða runupöntunar.
author: johanhoffmann
ms.date: 12/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-10
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 959b8b85fe55ed5e0a93b5b614c3f6166bbd2bb6ef07e9d0f0f4c2b1ea3c4659
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6721320"
---
# <a name="override-the-default-reservation-principle-for-materials-in-production"></a>Hnekkja sjálfgefinni frátekningarreglu fyrir efni í framleiðslu

[!include [banner](../includes/banner.md)]

Eiginleikinn *Hnekkja sjálfgefinni frátekningu framleiðslu* gerir kleift að stilla sjálfgefna frátekningarreglu fyrir hvern vörulíkanaflokk. Mismunandi frátekningarreglur er þar af leiðandi hægt að nota sjálfkrafa fyrir hverja vöru sem er hluti af formúlu framleiðsluuppskriftar eða runupöntunar. Hægt er að velja hvort hver vörulíkanaflokkur eigi að hnekkja sjálfgefinni frátekningarreglu sem er stillt fyrir pöntun, og hvaða frátekningarreglu eigi að nota í staðinn (*handvirkt*, *mat*, *áætlanagerð*, *losun* eða *upphaf*).

Þegar ný framleiðslupöntun eða runupöntun er stofnuð er beðið um að velja frátekningarregluna sem á að nota á þá pöntun og allar uppskriftar- og formúlulínur hennar. Þegar eiginleikinn *Hnekkja sjálfgefinni frátekningu framleiðslu* er notaður geta sumar eða allar uppskriftar- eða formúlulínur hnekkt þeirri frátekningarreglu og notað í staðinn frátekningarreglu sem er stillt fyrir tilheyrandi vörulíkanaflokk.

Til dæmis, ef um er að ræða hráefni eða innihaldsefni sem krefjast tiltektar, krefjast uppskriftar- eða formúlulínur sem stofnaðar eru fyrir þessar afurðir efnislega frátekningu vegna þess að efnisleg frátekning er skilyrði fyrir myndun vöruhúsavinnu. Yfirleitt, ef frátekningin á að gerast sjálfkrafa, skal velja eina af eftirfarandi frátekningarreglum: *mat*, *áætlanagerð*, *losun* eða *upphaf*. Hins vegar, ef til staðar er efni eða innihald sem krefst ekki tiltektar vegna þess að það er notað beint frá staðsetningunni, er yfirleitt valin frátekningarreglan *handvirkt* sem gerir engar efnislegar frátekningar eða býr til tiltekt.

## <a name="turn-on-the-feature"></a>Kveikja á eiginleikanum

Áður en hægt er að nota eiginleikann verður að vera kveikt á honum í kerfinu. Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikja á honum. Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:

- **Eining:** *Framleiðslustýring*
- **Heiti eiginleika:** *Hnekkja sjálfgefinni framleiðslufrátekningu*

## <a name="assign-a-production-reservation-policy-to-an-item-model-group"></a>Úthluta reglu framleiðslufrátekningar á vörulíkanaflokk

1. Farið í **Kostnaðarstjórnun \> Uppsetning á reglum birgðabókhalds \> Vörulíkanaflokkar**.
1. Stofnið eða veljið vörulíkanaflokk.
1. Í flýtiflipanum **Birgðareglur** skal velja gátreitinn **Hnekkja frátekningu vöruframleiðslu**.
1. Í reitnum **Frátekning** skal velja frátekningarregluna fyrir vörur sem tilheyra völdum líkanaflokki. (Þessar vörur innihalda vörur sem eru í uppskriftar- eða formúlulínu.)

    - **Handvirkt** – Vörur í líkanaflokknum verða ekki teknar efnislega frá sjálfkrafa fyrir framleiðslu. Hins vegar er hægt að taka þær frá handvirkt eftir þörfum.
    - **Mat** – Vörur í líkanaflokknum verða efnislega teknar frá við mat á framleiðslupöntuninni.
    - **Áætlanagerð** – Vörur í líkanaflokknum verða efnislega teknar frá við áætlanagerð framleiðslupöntunarinnar.
    - **Losa** – Vörur í líkanaflokknum verða efnislega teknar frá þegar framleiðslupöntunin er losuð.
    - **Upphaf** – Vörur í líkanaflokknum verða efnislega teknar frá við upphaf framleiðslupöntunarinnar.

## <a name="example-using-reservation-principles-in-a-bulkpack-scenario"></a>Dæmi: Frátekningarreglur notaðar í aðstæðum magnvöru/pakkavöru

Smurolía í magnvöru er framleidd í 1000 lítra blandara. Þegar magnvaran er tilbúin er henni dælt inn á nokkrar áfyllingarstöðvar þar sem flöskur í mismunandi stærðum eru fylltar. Að áfyllingu lokinni er flöskunum pakkað í kassa. Þessum kössum er síðan raðað á vörubretti.

Í þessum aðstæðum er stofnuð runupöntun til að gera 1000 lítra magnvöru. (Þessi pöntun er magnpöntunin) Þegar þessari runupöntun er lokið er tilkynnt um lok hennar hjá inntaksstað efnisins á áfyllingarstöðvunum. Runupöntun til að fylla og pakka hverri flöskustærð er því næst stofnuð. (Þessar pantanir eru pakkapantanir.) Pakkapantanir eru með formúlu sem samanstendur af magnvöru, tómri flösku, merkimiða og öðru umbúðaefni. Vegna þess að magnvaran rennur beint frá blöndunartankinum til áfyllingarstöðvanna er ekki þörf á neinni vöruhúsavinnu til að taka til þetta efni og magnvaran er notuð beint frá inntaksstaðnum. Þess vegna er frátekningarreglan stillt á *handvirkt*. Öðrum efnum er komið til áfyllingarstöðvarinnar í gegnum tiltekt. Þess vegna er frátekningarreglan fyrir þessar línur stillt á *losa* sem dæmi, þannig að frátekningin gerist sjálfkrafa þegar pakkapöntunin er losuð.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]