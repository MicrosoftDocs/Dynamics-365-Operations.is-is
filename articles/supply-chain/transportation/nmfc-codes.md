---
title: Kóðar fyrir innlenda flokkun farmflutnings með ökutækjum (NMFC)
description: Í þessu efnisatriði er lýst hvernig á að vinna með kóða fyrir innlenda flokkun farmflutnings með ökutækjum (NMFC) í Microsoft Dynamics 365 Supply Chain Management
author: Henrikan
ms.date: 04/22/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 0307437d3868f7ac34fa16a0913907a046ac14d4
ms.sourcegitcommit: 636c1bf096a8666a551b67e898da1f48feb9a187
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/26/2021
ms.locfileid: "5941883"
---
# <a name="national-motor-freight-classification-nmfc-codes"></a>Kóðar fyrir innlenda flokkun farmflutnings með ökutækjum (NMFC)

[!include [banner](../includes/banner.md)]

Kóðar fyrir innlenda flokkun farmflutnings með ökutækjum (NMFC) auðvelda þér að flokka vörur sem hægt er að senda. NMFC-kóðinn er merking sem er notuð til að flokka vörur. Þeir gera flutningafyrirtækjum kleift að meta vörur fyrir sendingu með því að flokka vörur út frá þáttum eins og hvort passi í vörubíl, vandamál með hleðsluna, vandamál með meðhöndlun og lítið geymsluþol. Varningi er flokkað í einn af 18 farmklösum með því að nota talnasvið frá 50 til 500. Klasinn sem varningurinn er flokkaður í byggir á mati á fjórum einkennandi þáttum flutninga: þéttleika, hleðslumöguleika, meðhöndlun og ábyrgð. Saman staðfesta þessir eiginleikar flutningshæfni vörunnar.

NMFC-kóði er tengdur við allar vörur sem eru minna en fullhlaðinn trukkur. Til dæmis gæti fartölvu verið úthlutað NMFC sem er flokkað sem 2,5 en rafmagnssnúrum gætu aftur á móti verið úthlutað NMFC sem er flokkað sem 65.

Þessi eiginleiki getur hjálpað starfsmönnum að nota NMFC-kóða til að flokka LTL-sendingarhluti. Hér eru nokkur dæmi:

- Ef fyrirtækið þitt setur vörulýsingu á farmbréf (BOL) mun flutningsfyrirtækið hafa einhverja hugmynd um hver farmurinn er. Farmur er mikilvæg flokkun vegna þess að mörg flutningsfyrirtæki byggja allt viðskiptalíkan sitt á farmgerðirnar sem þau senda.
- Þessi flokkun gæti verið nauðsynleg fyrir fyrirtækið þitt þar sem hún er notuð til að ákvarða kostnað við tiltekinn farm.
- Fyrirtækið þitt getur greint arðsemi LTL-vörustjórnunar og flutningafyrirtækisins.

Í þessu efnisatriði er lýst hvernig á að vinna með NMFC-kóða í Microsoft Dynamics 365 Supply Chain Management.

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
