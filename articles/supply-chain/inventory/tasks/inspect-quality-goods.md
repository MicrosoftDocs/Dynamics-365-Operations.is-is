---
title: Kanna vörugæði
description: Þessi grein lýsir því hvernig á að vinna úr gæðapöntunum.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b881f9c6f872061864d4254ce880d981ca71c479
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/02/2022
ms.locfileid: "9219035"
---
# <a name="inspect-the-quality-of-goods"></a>Kanna vörugæði

[!include [banner](../../includes/banner.md)]

Þessi grein lýsir því hvernig á að vinna úr gæðapöntunum. Gæðaskoðanir eru vanalega gerðar af gæðastarfsmanni.

Ef stöðluð [sýnigögn](../../../fin-ops-core/fin-ops/get-started/demo-data.md) eru uppsett er hægt að nota þau til að ljúka ferlunum í þessari grein. Til að nota sýnigögnin skal velja lögaðilann *USMF* áður en hafist er handa. Þú verður síðan að staðfesta innkaupapöntun *000016* og bóka innhreyfingarskjal afurðar. Gæðapöntun myndast sjálfkrafa.

## <a name="step-1-select-a-quality-order"></a>Skref 1: Velja gæðapöntun

Fylgja skal eftirfarandi skrefum til að velja gæðapöntun.

1. Farðu í **Birgðastjórnun \> Reglubundin verk \> Gæðastjórnun \> Gæðapantanir**.
1. Veldu gæðapöntunina sem var búin til áður en þú hófst þetta ferli.

## <a name="step-2-record-test-results"></a>Skref 2: Skrá niðurstöður prófunar

Fylgja skal eftirfarandi skrefum til að skrá niðurstöður prófunar.

1. Veldu **Niðurstöður**.
1. Veljið **Breyta**.
1. Í reitnum **Niðurstöðumagn** skal slá inn tölu.
1. Í reitnum **Útkoma** skal velja æskilega skrá. Í þessu dæmi byggist niðurstaðan á fyrirframskilgreindri útkomu. Yfirleitt er skráð ítarlegri niðurstaða prófunar á borð við stærð eða aðra mælivídd.
1. Veljið **Vista**.
1. Lokið síðunni.

## <a name="step-3-validate-the-quality-order"></a>Skref 3: Staðfesta gæðapöntunina

Til að staðfesta gæðapöntunina skal fylgja eftirfarandi skrefum.

1. Veldu **Staðfesta**.
1. Í reitnum **Staðfest af** skal velja notandann sem sér um skoðunina.
1. Veljið **Velja**.
1. Veljið **Í lagi**.
1. Lokið síðunni.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
