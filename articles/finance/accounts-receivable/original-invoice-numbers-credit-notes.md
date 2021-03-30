---
title: Tilvísanir í upprunalega reikninga í kreditnótum
description: Þetta efnisatriði útskýrir hvernig á að setja upp og prenta upprunaleg reikningsnúmer í tengdum kreditnótum.
author: ilkond
manager: AnnBe
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 04a4fc96cb7de60052b17e36c33ad5d5be322be4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207352"
---
# <a name="references-to-original-invoices-in-credit-notes"></a>Tilvísanir í upprunalega reikninga í kreditnótum

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Í sumum löndum og svæðum er lagaleg krafa um að prentaðar kreditnótur innihaldi tilvísanir í upprunalega reikninga. Þetta efnisatriði útskýrir hvernig á að setja upp og prenta upprunaleg reikningsnúmer í tengdum kreditnótum.

## <a name="prerequisites"></a>Forkröfur

- Á vinnusvæðinu **Eiginleikastjórnun** skal kveikja á eiginleikanum **Útlit kreditreikningsfærslu fyrir sölu- og verkreikningsskýrslur**. Frekari upplýsingar er að finna í [Eiginleikastjórnunaryfirlit](../../fin-and-ops/get-started/feature-management/feature-management-overview.md).
- Skilgreina þarf prentsnið fyrir nauðsynleg skjöl í Prentstýring.

Virknin sem lýst er í þessu efnisatriði gildir um eftirfarandi skjöl:

**Viðskiptakröfur**

- Textakreditnóta
- Kreditnóta viðskiptavina

**Verkefnastjórnun og bókhald**

- Kreditnóta verks

## <a name="configure-accounts-receivable-parameters"></a>Skilgreina færibreytur viðskiptakrafna

Fylgið þessum skrefum til að stilla færibreytur sem stýra því hvort tilvísanir í upprunalega reikninga séu prentaðar í tengdum kreditnótum.

1. Farðu í **Viðskiptakröfur** \> **Uppsetning** \> **Færibreytur viðskiptakröfu**.
2. Í flipanum **Uppfærslur**, í flýtiflipanum **Reikningur**, skal stilla valkostinn **Nota útlit kreditreikningsfærslu í sölu- og verkreikningaskýrslum** á **Já**.

![Færibreytur viðskiptakrafna skilgreindar](media/original-invoice-number-in-credit-note.jpg)

## <a name="define-references-to-original-invoices"></a>Skilgreina tilvísanir í upprunalega reikninga

Notið eftirfarandi ferli til að skilgreina tilvísanir í upprunalega reikninga, samkvæmt gerð skjals.

### <a name="free-text-credit-note"></a>Textakreditnóta

1. Fara í **Viðskiptakröfur** \> **Reikningar** \> **Allir reikningar með frjálsum texta**.
2. Stofnið nýja kreditnótu eða veljið fyrirliggjandi kreditnótu.
3. Opnið reikninginn.
4. Á aðgerðasvæðinu, í flipanum **Reikningur**, í flokknum **Aðgerðir**, skal velja **Kreditreikningsfærsla**.
5. Færið inn tilvísunina í upprunalegan reikning og veljið ástæðu leiðréttingarinnar.

![Tilvísun fyrir reikning með frjálsum texta skilgreind](media/reference-original-invoice-FTI.jpg)

### <a name="customer-credit-note"></a>Kreditnóta viðskiptavina

1. Farið í **Viðskiptakröfur** \> **Pantanir** \> **Allar sölupantanir**.
2. Veljið og opnið reikningsfærða sölupöntun sem þarf að leiðrétta.
3. Á aðgerðasvæðinu, í flipanum **Selja**, í flokknum **Kreditnóta**, skal velja **Kreditnóta**.
4. Færið inn ástæðu leiðréttingarinnar. Tilvísun í upprunalegan reikning er komið fyrir sjálfkrafa.

![Tilvísun fyrir sölupöntun skilgreind](media/reference-original-invoice-SO.jpg)

### <a name="project-credit-note"></a>Kreditnóta verks

1. Farið í **Verkefnastjórnun og bókhald** \> **Verkreikningar** \> **Verkreikningar**.
2. Veljið og opnið verkreikning sem á að leiðrétta.
3. Á aðgerðasvæðinu, í flipanum **Verkreikningur**, í flokknum **Aðgerðir**, skal velja **Velja fyrir kreditnótu**.
4. Veljið **Kreditreikningsfærsla**.
5. Færið inn ástæðu leiðréttingarinnar. Tilvísun í upprunalegan reikning er komið fyrir sjálfkrafa.

![Tilvísun fyrir verkreikning skilgreind](media/reference-original-invoice-project.jpg)

## <a name="printing-credit-notes"></a>Kreditnótur prentaðar

Þegar kreditnótur með frjálsum texta, fyrir viðskiptavini og verk eru prentaðar munu þær innihalda tilvísunina í upprunalegan reikning og ástæðu leiðréttingar.

![Prentuð kreditnóta](media/credit-note-FTI.jpg)

> [!NOTE]
> Gangið úr skugga um að prentvæn snið skjalanna séu rétt skilgreind með það í huga að tilvísanir í upprunalega reikninga verði prentaðar.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]