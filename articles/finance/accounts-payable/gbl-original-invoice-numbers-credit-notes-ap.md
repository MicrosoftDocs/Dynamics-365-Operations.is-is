---
title: Tilvísun í upprunalega reikninga í kreditnótum (reikningar lánardrottins)
description: Í þessari grein er lýst hvernig á að búa til tilvísun í upprunalegan reikning þegar kreditnóta er stofnuð.
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
ms.openlocfilehash: 39cf4eb7eef1a83abeb7bd44fa7b2abefee0806e
ms.sourcegitcommit: 8eb0cafe5ad20be2c4fff684e88d7d3f2249f820
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/06/2022
ms.locfileid: "9409665"
---
# <a name="reference-original-invoices-in-credit-notes-vendor-invoices"></a>Tilvísun í upprunalega reikninga í kreditnótum (reikningar lánardrottins)

[!include [banner](../includes/banner.md)]

Í sumum löndum og svæðum er lagaleg krafa um að prentaðar kreditnótur eða skýrslurútínur innihaldi tilvísanir í upprunalega reikninga. Í þessari grein er lýst hvernig á að búa til tilvísun í upprunalegan reikning þegar kreditnóta er stofnuð.

## <a name="prerequisites"></a>Forkröfur

Á vinnusvæðinu **Eiginleikastjórnun** skal virkja eiginleikann **Virkja kreditreikningsfærslu fyrir reikninga lánardrottins**. Frekari upplýsingar er að finna í [Eiginleikastjórnunaryfirlit](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Virknin sem lýst er í þessari grein gildir um eftirfarandi viðskiptaskjöl.

**Lánardrottnar:**

- Innkaupapöntun
- Reikningabók
- Skráningabók reikninga

**Fjárhagur:**

- Almenn færslubók

## <a name="define-a-reference-to-an-original-invoice"></a>Skilgreina tilvísun í upprunalegan reikning

Skilgreining tilvísunar í upprunalegan reikning felur í sér eftirfarandi skref á háu stigi:
1. Búa til og bóka reikning lánardrottins
2. Stofna kreditnótu lánardrottins.
3. Notið kreditreikningseiginleikann til að tengja reikninginn við kreditnótu.
4. Bókið kreditnótuna.

Notaðu eftirfarandi aðferðir til að skilgreina tilvísun í upprunalegan reikning í tilgreindum tegundum viðskiptaskjala.

### <a name="vendor-credit-note-purchase-order"></a>Kreditnóta lánardrottins (innkaupapöntun)

1. Farðu í **Viðskiptaskuldir** > **Innkaupapantanir** > **Allar innkaupapantanir**.
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
