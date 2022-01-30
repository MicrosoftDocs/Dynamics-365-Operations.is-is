---
title: Bættu við gerðum greiðsluupphæða
description: Þetta efnisatriði útskýrir hvernig á að setja upp tegundir greiðsluupphæða í eignaleigu.
author: moaamer
ms.date: 01/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseIndexRevaluation
audience: Application User
ms.reviewer: twheeloc
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 037afa458277a3a07bcb937c6ec4d961d0dd5ca9
ms.sourcegitcommit: 7adf9ad53b4e6d1c4d5d612ce0977b76c61ec173
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/13/2022
ms.locfileid: "7968415"
---
# <a name="add-payment-amount-types"></a>Bættu við gerðum greiðsluupphæða

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir því hvernig á að setja upp tegundir greiðsluupphæða í eignaleigu. Þannig er hægt að sundurliða leigugreiðsluupphæðina í stað þess að bæta eingreiðsluupphæðinni við greiðsluáætlunarlínurnar.

Til að bæta við gerðum greiðsluupphæða skaltu fylgja þessum skrefum.

1. Fara til **Eignaleiga \> Uppsetning \> Tegundir greiðsluupphæða**.
2. Veljið **Nýtt**.
3. Sláðu inn nýju greiðslutegundina og lýsingu.

> [!NOTE]
> Fyrir IFRS 16 vísitöluendurmat verður að búa til eina greiðsluupphæðartegund og merkja hana sem **Notað fyrir endurmat IRFS 16 vísitölu**. Þessi greiðsluupphæðartegund verður notuð þegar vísitöluendurmatsferlið er keyrt á móti IFRS 16 bókinni og mun taka til greina þær breytingar sem urðu vegna vísitöluendurmatsferlisins.
>
> Þegar **Greiðslu sundurliðun** valkostur í leigusamningi er stilltur á **Já**, ef vísitöluendurmat fyrir IFRS 16 er keyrt, en það er engin greiðslutegund fyrir IFRS 16, verður ferlinu ekki lokið.

Aðeins er hægt að merkja eina skrá sem **Notað fyrir endurmat IFRS 16 vísitölu**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]