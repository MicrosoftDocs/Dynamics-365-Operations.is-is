---
title: Hanna skilgreiningar rafrænnar skýrslugerðar til að útiloka BOM-stafi í mynduðum skrám
description: Í þessari grein er útskýrt hvernig skilgreina á snið rafrænnar skýrslugerðar til að búa til skýrslur sem útiloka BOM-stafi.
author: kfend
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: EROperationDesigner
ms.openlocfilehash: a2ea132b51f2f451fbe81a9c7869bea84bf4017a
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/23/2022
ms.locfileid: "9324020"
---
# <a name="design-er-configurations-to-suppress-bom-characters-in-generated-files"></a>Hanna skilgreiningar rafrænnar skýrslugerðar til að útiloka BOM-stafi í mynduðum skrám

[!include [banner](../includes/banner.md)]

Hægt er að hanna [Rafræna skýrslugerðar](general-electronic-reporting.md)[lausn](er-quick-start1-new-solution.md) til að mynda skjöl á útleið. Til að mynda skölin sem texta eða XML-skrá verður lausnin að fela í sér [skilgreiningu](general-electronic-reporting.md#Configuration) rafrænnar skýrslugerðar sem inniheldur sniðshlut rafrænnar skýrslugerðar. Til að tilgreina [stafakóðun](/windows/win32/intl/character-sets) sem stendur fyrir safn stafa í mynduðum skrám, verður snið rafrænnar skýrslugerðar að innihalda sniðseininguna **Algeng\\Skrá**. Til að skilgreina sniðsþátt rafrænnar skýrslugerðar skal opna útgáfu draga fyrir skilgreiningu rafrænnar skýrslugerðar í sniðshönnuði rafrænnar skýrslugerðar og bæta við einingunni **Algeng\\Skrá**. Í reitnum **Kóðun** skal tilgreina kóðun á skjölum á útleið sem eru mynduð við keyrslu með því að nota þennan þátt.

> [!NOTE]
> Ef sniðið inniheldur rangt kóðunarheiti kemur upp villa þegar breytingarnar eru vistaðar í stillingum sniðsins.

![Rótareiningu bætt við síðu sniðshönnuðar.](./media/er-suppress-bom-characters-image1.gif)

Ef **UTF-8**, **UTF-16** eða **UTF-32** er tilgreint sem kóðunin verður valkosturinn **Útiloka BOM-stafi** tiltækur. Stillið þennan valkost á **Já** til að útiloka [BOM-stafi](/globalization/encoding/byte-order-mark) í skrám á útleið sem eru myndaðar við keyrslu þegar breytanlegt snið rafrænnar skýrslugerðar er keyrt.

> [!NOTE]
> Ef reiturinn **Kóðun** er skilinn eftur auður verður sjálfgefna kóðunin **UTF-8** notuð.

![Valkostur útilokunar BOM-stafa stilltur á síðu sniðshönnuðar.](./media/er-suppress-bom-characters-image2.gif)

Til að fara yfir virkni við keyrslu skal ljúka viðeigandi ferli. Ljúkið sem dæmi við skrefin í greininni [Fresta keyrslu XML-eininga á sniði rafrænnar skýrslugerðar](er-defer-xml-element.md). Þegar búið er að ljúka við skrefin í hlutanum [Breyta sniði þannig að útreikningurinn byggist á mynduðu úttaki](er-defer-xml-element.md#modify-the-format-so-that-the-calculation-is-based-on-generated-output) í þeirri grein skal fylgja þessum viðbótarskrefum.

1. Tilgreinið UTF-kóðunina:

    1. Velja skal eininguna **Skýrsla** af gerðinni **Algeng\\Skrá**.
    2. Í reitnum **Kóðun** skal tilgreina kóðunina **UTF-8**.

2. Myndið XML-skrá sem inniheldur BOM-stafi:

    1. Stillið valkostinn **Útiloka BOM-stafi** á **Nei** til að hafa með BOM-stafi í mynduðum XML-skrám.
    2. Ljúkið skrefunum í hlutanum [Fresta keyrslu á samantekt XML-einingar þannig að reiknuð samtala sé notuð](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) í greininni [Fresta keyrslu XML-eininga á sniði rafrænnar skýrslugerðar](er-defer-xml-element.md) og vistið myndaða skrá sem **SampleXmlReport.xml**.

3. Myndið XML-skrá sem inniheldur ekki BOM-stafi:

    1. Stillið valkostinn **Útiloka BOM-stafi** á **Já** til að útiloka BOM-stafi í mynduðum XML-skrám.
    2. Ljúkið skrefunum í hlutanum [Fresta keyrslu á samantekt XML-einingar þannig að reiknuð samtala sé notuð](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) í greininni [Fresta keyrslu XML-eininga á sniði rafrænnar skýrslugerðar](er-defer-xml-element.md) og vistið myndaða skrá sem **SampleXmlReport (1).xml**.

4. Í skráarsamanburði skal bera saman myndaðar skrár.

    Fyrsti munurinn sem tekið verður eftir er skráarhausinn. Skráin SampleXmlReport.xml inniheldur BOM-staf þar sem skráin SampleXmlReport (1).xml gerir ekki.

    ![Myndaðar skrár bornar saman með forriti samanburðarskráar.](./media/er-suppress-bom-characters-image3.png)

## <a name="see-also"></a>Sjá einnig

- [Fresta keyrslu XML-eininga á sniði rafrænnar skýrslugerðar](er-defer-xml-element.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
