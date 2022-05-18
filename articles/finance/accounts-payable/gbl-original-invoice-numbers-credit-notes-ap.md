---
title: Tilvísun í upprunalega reikninga í kreditnótum (reikningar lánardrottins)
description: Í þessu efnisatriði er lýst hvernig á að búa til tilvísun í upprunalegan reikning þegar kreditnóta er stofnuð.
author: v-oloski
ms.date: 09/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: v-oloski
ms.search.validFrom: 2021-09-23
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 698a23a98f027014c89073203e6d9dfa5539a2f6
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689186"
---
# <a name="reference-original-invoices-in-credit-notes-vendor-invoices"></a>Tilvísun í upprunalega reikninga í kreditnótum (reikningar lánardrottins)

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er lýst hvernig á að búa til tilvísun í upprunalegan reikning þegar kreditnóta er stofnuð.

## <a name="prerequisites"></a>Forkröfur

Á vinnusvæðinu **Eiginleikastjórnun** skal virkja eiginleikann **Virkja kreditreikningsfærslu fyrir reikninga lánardrottins**. Frekari upplýsingar er að finna í [Eiginleikastjórnunaryfirlit](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Virknin sem lýst er í þessu efnisatriði gildir um eftirfarandi viðskiptaskjöl.

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
