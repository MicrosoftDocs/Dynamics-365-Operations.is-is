---
title: Tilvísun í upprunalega reikninga í kreditnótum (reikningar lánardrottins)
description: Þessi grein lýsir því hvernig á að búa til tilvísun í upprunalegan reikning þegar þú stofnar kreditnótu.
author: AdamTrukawka
ms.date: 09/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: 2021-09-23
ms.dyn365.ops.version: 10.0.20
ms.search.form: ''
ms.openlocfilehash: ed07ae9784da3ca721fcb25a9c5a14c4f75f2e59
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277371"
---
# <a name="reference-original-invoices-in-credit-notes-vendor-invoices"></a>Tilvísun í upprunalega reikninga í kreditnótum (reikningar lánardrottins)

[!include [banner](../includes/banner.md)]

Þessi grein lýsir því hvernig á að búa til tilvísun í upprunalegan reikning þegar þú stofnar kreditnótu.

## <a name="prerequisites"></a>Forkröfur

Á vinnusvæðinu **Eiginleikastjórnun** skal virkja eiginleikann **Virkja kreditreikningsfærslu fyrir reikninga lánardrottins**. Frekari upplýsingar er að finna í [Eiginleikastjórnunaryfirlit](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Virknin sem lýst er í þessari grein á við um eftirfarandi viðskiptaskjöl.

**Lánardrottnar:**

- Innkaupapöntun
- Reikningabók
- Skráningabók reikninga

**Fjárhagur:**

- Almenn færslubók

## <a name="define-a-reference-to-an-original-invoice"></a>Skilgreina tilvísun í upprunalegan reikning

Notaðu eftirfarandi aðferðir til að skilgreina tilvísun í upprunalegan reikning í tilgreindum tegundum viðskiptaskjala.

### <a name="vendor-credit-note-purchase-order"></a>Kreditnóta lánardrottins (innkaupapöntun)

1. Farðu í **Viðskiptaskuldir** \> **Innkaupapantanir** \> **Allar innkaupapantanir**.
2. Stofnaðu nýja innkaupapöntun eða notaðu fyrirliggjandi pöntun til að stofna kreditnótu.
3. Á aðgerðasvæðinu, í flipanum **Reikningur**, í flokknum **Kynna**, skal velja **Kreditreikningsfærsla**.
4. Færðu inn ástæðu leiðréttingar og tilvísunina í upprunalegan reikning.

### <a name="vendor-credit-note-ledger-journals"></a>Kreditnóta lánardrottins (færslubækur fjárhags)

1. Fylgið einu af eftirfarandi skrefum:

    - Farðu í **Viðskiptaskuldir** \>**Reikningabækur**.
    - Farðu í **Viðskiptaskuldir** \> **Komubók**.
    - Opnið **Fjárhagur** \> **Færslubókarfærslur** \> **Almennar færslubækur**.

2. Stofnaðu nýja færslubók og færslubókarlínur.
3. Á aðgerðasvæðinu skal velja **Aðgerðir** \> **Kreditreikningsfærsla**.
4. Færðu inn ástæðu leiðréttingar og tilvísunina í upprunalegan reikning.

> [!NOTE]
> Skipunin **Kreditreikningsfærsla** er sýnileg í almennu færslubókarfylgiskjali ef reiturinn **Reikningsgerð** er stilltur á **Lánardrottinn**.
