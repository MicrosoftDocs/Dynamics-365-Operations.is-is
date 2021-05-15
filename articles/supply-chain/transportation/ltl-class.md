---
title: Klasar sem eru minni en fullhlaðinn trukkur (LTL)
description: Í þessu efnisatriði er gerð grein fyrir klösum sem eru minna en fullhlaðinn trukkur (LTL) og útskýrt hvernig á að setja þá upp í Microsoft Dynamics 365 Supply Chain Management.
author: Henrikan
ms.date: 04/05/2021
ms.topic: article
ms.search.form: WHSLTLClass
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-05
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 295006cac0a67cd577809a1b62566de043ea55fb
ms.sourcegitcommit: 636c1bf096a8666a551b67e898da1f48feb9a187
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/26/2021
ms.locfileid: "5941811"
---
# <a name="less-than-truckload-ltl-classes"></a>Klasar sem eru minni en fullhlaðinn trukkur (LTL)

[!include [banner](../includes/banner.md)]

Klasi sem er minna en fullhlaðinn trukkur (LTL) er klasi farmsendingar sem er notaður til að flokka vörur sem hægt er að senda. Almennt eru allar gerðir afurða eða vöru með kóða fyrir innlenda flokkun farmflutnings með ökutækjum (NMFC) sem samsvarar tilteknu númeri farmklasa fyrir LTL-sendingar. LTL-farmklasar standa fyrir flokka af vörum þar sem NMFC-kóðar tengjast tilteknum varningi í hverjum þessarar 18 farmklasa.

Þessi eiginleiki gerir þér kleift að nota kerfið til að framkvæma eftirfarandi verk:

- Skilgreinið klasa LTL-farms sem eru notaðir í fyrirtækinu.
- Úthlutið hverjum LTL-klasa NMFC-kóða á síðunni **NMFC-kóðar**. Frekari upplýsingar er að finna í [Kóðar fyrir innlenda flokkun farmflutnings með ökutækjum (NMFC)](nmfc-codes.md).
- Úthlutið NMFC-kóða (og þar af leiðandi tengdan LTL-kóða) á hverja afurð á síðunni **Afurðir**.
- Leggðu nákvæmt mat á LTL-klasa hverrar afurðar sem NMFC-kóðanum er úthlutað til.
- Takið ákvörðun um kröfur pökkunar fyrir hvern LTL-klasa með því að athuga alþjóðlega LTL-staðla. Á þennan hátt er tryggt að vörurnar séu vel varðar og sendar á öruggan hátt.
- Fáið nákvæmt mát á sendingu út frá LTL-farmklasa hverrar afurðar.

Í þessu efnisatriði er lýst hvernig á að stofna LTL-klasa í Microsoft Dynamics 365 Supply Chain Management.

## <a name="create-an-ltl-class"></a>Stofna LTL-klasa

Til að stofna LTL-flokk skal fylgja eftirfarandi skrefum.

1. Fylgið einu af eftirfarandi skrefum:

    - Farið í **Vöruhúsakerfi \> Uppsetning \> Birgðir \> LTL-klasar**.
    - Farið í **Flutningsstjórnun \> Uppsetning \> Flutningsstaðlar \> LTL-klasar**.

2. Á aðgerðasvæðinu skal velja **Nýtt** til að búa til LTL-flokk. Stillið svo eftirfarandi reiti:

    - **LTL-klasi** – Sláið inn innra LTL-klasakenni fyrirtækisins fyrir vörutegundina. Flest fyrirtæki nota alþjóðlegan staðal. Í slíku tilfelli mun gildi þessa svæðis samsvara gildi svæðisins **Flokkur**. Ef fyrirtækið notar sinn eigin staðal er hins vegar færður inn kóði sem er í samræmi við þann staðal.
    - **Heiti** – Færið inn lýsandi heiti sem hjálpar ykkur og öðrum notendum að velja réttan LTL-klasa fyrir hvern NMFC-kóða.
    - **Klasi** – Færið inn alþjóðlegan staðal LTL-klasakennis fyrir vörutegundina. Kóðinn sem færður er hér inn verður að vera í samræmi við opinberan staðal.

## <a name="example-set-up-ltl-classes"></a>Dæmi: setja upp LTL-flokka

Eftirfarandi dæmi sýnir hvernig á að setja upp tvo mismunandi LTL-flokka sem hægt er að nota með mismunandi vörutegundum.

1. Farið í **Vöruhúsakerfi \> Uppsetning \> Birgðir \> LTL-klasar**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Stilltu eftirfarandi gildi á nýju línunni:

    - **LTL-flokkur:** *92.5*
    - **Heiti:** *Tölvur, skjáir, ísskápar*
    - **Flokkur:** *92.5*

1. Í aðgerðarúðunni skal velja **Vista**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Stilltu eftirfarandi gildi á nýju línunni:

    - **LTL-klasi:** *125*
    - **Heiti:** *Lítil heimilistæki*
    - **Flokkur:** *125*

1. Í aðgerðarúðunni skal velja **Vista**.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Kóðar fyrir innlenda flokkun farmflutnings með ökutækjum (NMFC)](nmfc-codes.md)
- [Stofnun farmbréfs](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
