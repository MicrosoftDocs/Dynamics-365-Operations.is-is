---
title: Umreikningur mælieiningar eftir afurðarafbrigði
description: Þessi grein útskýrir hvernig á að setja upp umreikning mælieiningar fyrir afurðarafbrigði. Dæmi um uppsetninguna fylgir með.
author: t-benebo
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: UnitOfMeasureConversion
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: a605e510ac8faa1f92e105c9fcc30222ef78e05e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869634"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a>Umreikningur mælieiningar eftir afurðarafbrigði

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir hvernig á að setja upp umreikning mælieiningar fyrir ýmis afurðarafbrigði.

Í stað þess að búa til margar stakar afurðir sem þarf að vinna með er hægt að nota afurðarafbrigði til að búa til afbrigði af einni afurð. Til dæmis gæti afurðarafbrigðið verið stuttermabolur af tiltekinni stærð og lit.

Áður var aðeins hægt að setja umreikning eininga upp á afurðarsniðmáti. Þess vegna voru öll afurðarafbrigði með sömu umreikningsreglur einingar. Hins vegar þegar kveikt er á *Umreikningur mælieiningar fyrir afurðarafbrigði*, ef stuttermabolirnir eru seldir í kössum, og fjöldi stuttermabola sem hægt er að pakka í kassa fer eftir stærð stuttermabolanna, er hægt að setja upp umreikning eininga á milli mismunandi bolastærða og kassa sem notaðir eru sem umbúðir.

## <a name="turn-on-the-feature-in-your-system"></a>Kveikja á eiginleikanum í kerfinu

Ef þessi eiginleiki er ekki þegar til staðar í kerfinu skal fara á [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), og kveikja á *Umreikningur mælieiningar fyrir afurðarafbrigði*.

## <a name="set-up-a-product-for-unit-conversion-per-variant"></a>Setja upp afurð fyrir umreikning einingar fyrir hvert afbrigði

Aðeins er hægt að stofna afurðarafbrigði fyrir afurðir sem eru afurðarsniðmát. Nánari upplýsingar er að finna í [Stofna afurðarsniðmát](tasks/create-product-master.md). *Umreikningur mælieiningar fyrir afurðarafbrigði* er ekki tiltækur fyrir afurðir sem eru settar upp fyrir ferli fyrir þyngd afurðar.

Til að skilgreina afurðarsniðmát til að styðja umbreytingu eininga á hvert afbrigði skal fylgja þessum skrefum.

1. Opna **upplýsingar um afurðastjórnun \> Afurðir \> Afurðarsniðmát**.
1. Stofna eða opna afurðarsniðmát til að fara á **Upplýsingar um afurð**-síðuna.
1. Stilltu **Virkja umreikning mælieiningar** á *Já*.
1. Á aðgerðarúðunni á flipanum **Afurð** í flokknum **Uppsetning** skal velja **Umreikningur eininga**.
1. **Umreikningur eininga** síðan opnast. Velja einn af eftirfarandi flipum:

    - **Umreikningur innan flokks** – Veljið þennan flipa til að umbreyta á milli eininga sem tilheyra sama mælieiningaflokki.
    - **Umreikningur milli flokka** – Veljið þennan flipa til að umbreyta á milli eininga sem tilheyra mismunandi mælieiningaflokkum.

1. Ef bæta á nýrri einingu við er smellt á **Nýtt**.
1. Stillið **Búa til umreikning fyrir** reitinn á eitt af eftirfarandi gildum:

    - **Afurð** – Ef þú velur þetta gildi getur þú sett upp umreikning eininga fyrir afurðarsniðmát. Þessi umreikningur eininga verður notaður til vara fyrir öll afurðarafbrigði sem enginn umreikningur eininga er skilgreindur fyrir.
    - **Afurðarafbrigði** – ef þetta gildi er valið er hægt að setja upp umreikning eininga fyrir tilgreint afurðarafbrigði. Notaðu reitinn **Afurðarafbrigði** til að velja afbrigðið.

    ![Nýjum umreikningi eininga bætt við.](media/uom-new-conversion.png "Nýjum umreikningi eininga bætt við")

1. Notaðu önnur svæði sem eru gefin upp til að setja upp umreikning eininga.
1. Veljið **Í lagi** til að vista nýja umreikning eininga.

> [!TIP]
> Hægt er að opna **Umreikningur eininga** síðu afurðar eða afurðarafbrigðis af einhverri eftirfarandi síðna:
> 
> - Upplýsingar um afurð
> - Upplýsingar um losaðar afurðir
> - Útgefin afurðarafbrigði

## <a name="example-scenario"></a>Dæmi

Í þessu tilviki selur fyrirtæki stuttermaboli í eftirfarandi stærðum: litlir, miðlungs, stórir og mjög stórir. Stuttermabolur er skilgreindur sem afurð og mismunandi stærðir eru skilgreindar sem afbrigði af afurðinni. Bolirnir eru pakkaðir í kössum. Fyrir stærðir lítill, meðalstór og stór geta verið fimm bolir í hverjum kassa. Hins vegar, fyrir mjög stóra, er ekki til pláss nema fyrir fjóra boli í hverjum kassa.

Fyrirtækið vill rekja mismunandi afbrigði í einingunni *Stykki*, en það selur þær í einingunni *Kassar*. Fyrir stærðir lítill, miðlungs og stór er umreikningur milli birgðaeiningar og sölueiningar 1 kassi = 5 stykki. Fyrir stærð mjög stór er umreikningurinn 1 kassi = 4 stykki.

1. Á síðunni **Upplýsingar um losaðar afurðir** fyrir vöruna **Stuttermabolir** opnaðu síðuna **Umreikningur eininga**.
1. Á síðunni **Umreikningur eininga** skal setja upp eftirfarandi umreikning eininga fyrir útgefna afurðarafbrigðið **Mjög stór**.

    | Svæði                 | Stilling                 |
    |-----------------------|-------------------------|
    | Búa til umskráningu fyrir | Afurðarafbrigði         |
    | Afurðarafbrigði       | Stuttermabolur : : Mjög stór : : |
    | Frá einingu             | Kassar                   |
    | Stuðull                | 4                       |
    | Til einingar               | Stykki                  |

1. Útgefnu afurðarafbrigðin **Lítill**, **Miðlungs** og **Stór** eru með sama umreikning eininga milli eininganna *Kassi* og *Stykki*, sem þýðir að hægt er að skilgreina umreikning eininga fyrir þessi afurðarafbrigði í afurðarsniðmátinu.

    | Svæði                 | Stilling |
    |-----------------------|---------|
    | Búa til umskráningu fyrir | Afurð |
    | Afurð               | Stuttermabolur |
    | Frá einingu             | Kassar   |
    | Stuðull                | 5       |
    | Til einingar               | Stykki  |

## <a name="using-excel-to-update-the-unit-conversions"></a>Nota Excel til að uppfæra umreikning eininga

Ef afurð er með mörg afurðarafbrigði með mismunandi umreikningum eininga, er góð hugmynd að flytja út umreikninga eininga í Microsoft Excel vinnubók, uppfæra umreikningana, og síðan senda þá til baka til Dynamics 365 Supply Chain Management.

Til að flytja út umreikninga eininga í Excel, á síðunni **Umreikningur eininga**, í aðgerðasvæði, skal velja **Opna í Microsoft Office**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Stjórna mælieiningum](tasks/manage-unit-measure.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]