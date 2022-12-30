---
title: Kóðar fyrir innlenda flokkun farmflutnings með ökutækjum (NMFC)
description: Í þessari grein er lýst hvernig á að vinna með kóða fyrir innlenda flokkun farmflutnings með ökutækjum (NMFC) í Microsoft Dynamics 365 Supply Chain Management
author: Weijiesa
ms.date: 04/22/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 522e4d4e26b04b5ca1dd317e433c5a20ff3cb12e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893266"
---
# <a name="national-motor-freight-classification-nmfc-codes"></a>Kóðar fyrir innlenda flokkun farmflutnings með ökutækjum (NMFC)

[!include [banner](../includes/banner.md)]

Kóðar fyrir innlenda flokkun farmflutnings með ökutækjum (NMFC) auðvelda þér að flokka vörur sem hægt er að senda. NMFC-kóðinn er merking sem er notuð til að flokka vörur. Þeir gera flutningafyrirtækjum kleift að meta vörur fyrir sendingu með því að flokka vörur út frá þáttum eins og hvort passi í vörubíl, vandamál með hleðsluna, vandamál með meðhöndlun og lítið geymsluþol. Varningi er flokkað í einn af 18 farmklösum með því að nota talnasvið frá 50 til 500. Klasinn sem varningurinn er flokkaður í byggir á mati á fjórum einkennandi þáttum flutninga: þéttleika, hleðslumöguleika, meðhöndlun og ábyrgð. Saman staðfesta þessir eiginleikar flutningshæfni vörunnar.

NMFC-kóði er tengdur við allar vörur sem eru minna en fullhlaðinn trukkur. Til dæmis gæti fartölvu verið úthlutað NMFC sem er flokkað sem 2,5 en rafmagnssnúrum gætu aftur á móti verið úthlutað NMFC sem er flokkað sem 65.

Þessi eiginleiki getur hjálpað starfsmönnum að nota NMFC-kóða til að flokka LTL-sendingarhluti. Hér eru nokkur dæmi:

- Ef fyrirtækið þitt setur vörulýsingu á farmbréf (BOL) mun flutningsfyrirtækið hafa einhverja hugmynd um hver farmurinn er. Farmur er mikilvæg flokkun vegna þess að mörg flutningsfyrirtæki byggja allt viðskiptalíkan sitt á farmgerðirnar sem þau senda.
- Þessi flokkun gæti verið nauðsynleg fyrir fyrirtækið þitt þar sem hún er notuð til að ákvarða kostnað við tiltekinn farm.
- Fyrirtækið þitt getur greint arðsemi LTL-vörustjórnunar og flutningafyrirtækisins.

Í þessari grein er lýst hvernig á að vinna með NMFC-kóða í Microsoft Dynamics 365 Supply Chain Management.

## <a name="prerequisites"></a>Forkröfur

Áður en hægt er að stofna NMFC-kóða þarf að setja upp alla LTL-farmklasa sem þarf að varpa í þá. LTL-farmklasar standa fyrir flokka af vörum þar sem NMFC-kóðar tengjast tilteknum varningi í hverjum þessarar 18 farmklasa. Frekari upplýsingar um hvernig á að vinna með LTL-klasa er að finna í [Klasar sem eru minni en fullhlaðinn trukkur (LTL)](ltl-class.md).

## <a name="create-an-nmfc-code"></a>Búa til NMFC-kóða

Til að búa til NMFC-kóða skal fylgja eftirfarandi skrefum.

1. Fylgið einu af eftirfarandi skrefum:

    - Farið í **Vöruhúsakerfi \> Uppsetning \> Birgðir \> NMFC-kóðar**.
    - Farið í **Flutningsstjórnun \> Uppsetning \> Flutningsstaðlar \> NMFC-kóðar**.

1. Veljið **Nýr** til að stofna NMFC-kóða. Stillið svo eftirfarandi reiti:

    - **NMFC-kóði** – Færið inn NMFC-kóða vörutegundarinnar.
    - **Heiti** – Færið inn heiti fyrir NMFC-kóðann.
    - **LTL-flokkur** – Veljið LTL flokkinn sem tengist NMFC kóðanum.
    - **Afgreiðslueining farmbréfs** – Skilgreinið sjálfgefna gerð meðhöndlunar fyrir sendinguna.

## <a name="example-set-up-nmfc-codes"></a>Dæmi: setja upp NMFC-kóða

Eftirfarandi dæmi sýnir hvernig á að setja upp tvo mismunandi NMFC-kóða sem hægt er að nota með mismunandi vörum.

1. Farið í **Vöruhúsakerfi \> Uppsetning \> Birgðir \> NMFC-kóðar**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Stilltu eftirfarandi gildi á nýju línunni:

    - **NMFC-kóði**: *92.5*
    - **Heiti:** *Tölvur*
    - **LTL-flokkur:** *92.5*
    - **Afgreiðslueining farmbréfs:** *Eining*

1. Í aðgerðarúðunni skal velja **Vista**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Stilltu eftirfarandi gildi á nýju línunni:

    - **NMFC-kóði:** *125*
    - **Heiti:** *Símar*
    - **LTL-klasi:** *125*
    - **Afgreiðslueining farmbréfs:** *Eining*

1. Í aðgerðarúðunni skal velja **Vista**.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Klasar sem eru minni en fullhlaðinn trukkur (LTL)](ltl-class.md)
- [Stofnun farmbréfs](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
