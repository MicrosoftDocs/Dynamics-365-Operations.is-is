---
title: Stjórna mælieiningum
description: Þetta efnisatriði lýsir því hvernig á að skilgreina mælieiningu, veita þýðingar fyrir eininguna og lýsingu hennar, og skilgreina umreikningsreglur fyrir tengdar einingar.
author: sorenva
ms.date: 04/09/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup, UnitOfMeasureCalculator, UnitOfMeasureWizard, UnitOfMeasureLookupTest
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d251f90675188426e74b8cbe672856eb4c9ecb8a391f54e735ba19b91b7e3f4a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6746940"
---
# <a name="manage-units-of-measure"></a>Stjórna mælieiningum

[!include [banner](../../includes/banner.md)]

Þetta efnisatriði lýsir því hvernig á að skilgreina mælieiningu, veita þýðingar fyrir eininguna og lýsingu hennar, og skilgreina umreikningsreglur fyrir tengdar einingar.

## <a name="open-the-units-page"></a>Opna síðuna Einingar

Til að búa til og vinna með mælieiningar sem eru í boði í kerfinu skal fara í **Fyrirtækisstjórnun \> Uppsetning \> Einingar \> Einingar**.

Eftirfarandi hlutar þessa efnis lýsa hvað hægt er að gera á síðunni **Einingar**.

## <a name="create-standard-units-and-conversions"></a>Búa til staðaleiningar og umreikninga

Ef kerfið þitt inniheldur ekki nú þegar algengustu mælieiningar metrakerfisins og/eða bandaríska einingakerfisins (USCS) getur leiðsagnarforrit einingauppsetningar auðveldað þér að hefjast strax handa með grunnskilgreiningar og umreikninga á einingum. Til að ljúka leiðsögninni skal velja **Leiðsagnarforrit við stofnun einingar** á aðgerðasvæðinu og síðan fylgja leiðbeiningunum á skjánum.

## <a name="create-or-edit-a-unit-of-measure"></a>Stofna eða breyta mælieiningu

Til að búa til eða breyta mælieiningu skal fylgja eftirfarandi skrefum.

1. Fylgið einu af eftirfarandi skrefum:

    - Til að breyta fyrirliggjandi einingu skal velja hana í listasvæðinu.
    - Til að stofna nýja einingu er valið **Ný** á aðgerðasvæðinu.

1. Í haus færslunnar skal stilla eftirfarandi reiti:

    - **Eining** – Sláið inn kennið eða tákni til að nota til að vísa í eininguna á kerfistungumálinu. Þetta auðkenni eða tákn er venjulega algeng skammstöfun fyrir eininguna, svo sem *ea* fyrir hvert stykki eða *cm* fyrir sentimetra.
    - **Lýsing** – Færið inn lýsandi nafn fyrir eininguna á kerfistungumálinu. Þetta heiti er yfirleitt fullt heiti einingarinnar, t.d. *Hvert* eða *Sentimetri*.

1. Á flýtiflipanum **Almennt** stillirðu eftirfarandi reiti:<!-- KFM: confirm this:    - **Fixed unit assignment** and **Fixed unit** – These fields have an effect only if you're using the Microsoft Retail Essentials product. If the current unit can be mapped to one of the fixed units that are used by Retail Essentials, set the **Fixed unit assignment** option to *Yes*. Then select the fixed unit in the **Fixed unit** field. -->

    - **Mælieiningarflokkur** – Veldu eignina sem einingin mælir (t.d. lengd, svæði, þyngd eða magn).
    - **Einingakerfi** – Veljið mælieiningakerfið sem einingin tilheyrir (*Einingar í metrakerfi* eða *Einingar í bandaríska einingakerfinu*).
    - **Grunneining** – Stillið þennan valkost á *Já* til að nota núverandi einingu sem grunneiningu fyrir einingarflokk hennar. Í þessu tilfelli þarf aðeins að tilgreina umreiknistuðulinn milli grunneiningarinnar og hverrar viðbótareiningar í einingaflokknum. Kerfið getur síðan breytt á milli allra eininga í þeim einingaflokki. Því er auðveldara að setja upp umreikning.

        Til dæmis, ef gallon er grunneining fyrir einingaklasann *Rúmmál* þarf aðeins að setja upp umreiknistuðul frá lítra yfir í gallon og frá hálfpotti yfir í gallon. Kerfið getur þá einnig umreiknað frá lítra yfir í hálfpott.

        Aðeins er hægt að hafa eina grunneiningu í hverjum einingarflokki.

    - **Kerfiseining** – Stillið þennan valkost á *Já* til að nota núverandi einingu sem væntanlega einingu fyrir allar óskilgreindar mælingar í mælieiningaflokki hennar. Ef til dæmis reitur sem er notaður til að færa inn magn leyfir ekki að tilgreina einingu (eða ef notandinn velur ekk einingu), notar kerfið eininguna sem er stillt sem eining kerfisins fyrir mælieiningaflokkinn *Magn*. Aðeins er hægt að hafa eina kerfiseiningu í hverjum einingarflokki.
    - **Nákvæmni aukastafa** – Tilgreinið fjölda aukastafa sem námunda á gildi sem eru tilgreind fyrir núverandi einingu eða umbreytt í hana.

1. Í aðgerðarúðunni skal velja **Vista**.

## <a name="define-unit-translations"></a>Skilgreina þýðingar eininga

Til að skilgreina þýðingar fyrir auðkenni eða tákn og lýsingu fyrir mælieiningu skal fylgja eftirfarandi skrefum.

1. Búa til eða velja eininguna sem á að búa til þýðingar fyrir.
1. Veljið **Einingatextar** á aðgerðasvæðinu.

    Síðan **Einingatextar** birtist. Þú notar þessa síðu til að skilgreina þýðingar fyrir kennin eða táknið fyrir valda einingu. Þessar þýðingar er síðan hægt að nota í ytri skjölum á tungumálum tengdum viðskiptavini eða lánardrottni.

1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Í svæðinu **Tungumál** skal velja tungumál sem þýða á einingakenni eða tákn á yfir á.
1. Í reitinn **Texti** skal færa inn þýðingu á kenni eða tákni einingarinnar á völdu tungumáli.
1. Í aðgerðarúðunni skal velja **Vista**.
1. Lokið síðunni.
1. Veljið **Aðgerðasvæðinu** skal velja **Þýddar lýsingar á einingum**.

    **Þýddar lýsingar á einingum** birtast. Þessi síða er notuð til að skilgreina tungumálasértækar lýsingar fyrir völdu eininguna.

1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Í reitnum **Tungumál** velurðu tungumálið sem á að þýða einingarlýsinguna yfir á.
1. Í reitinn **Lýsing** er færð inn þýðing á einingarlýsingunni á völdu tungumáli.
1. Í aðgerðarúðunni skal velja **Vista**.
1. Lokið síðunni.

## <a name="define-unit-conversion-rules"></a>Skilgreina umreikningsreglur eininga

Til að skilgreina reglur fyrir umbreytingar milli mælieininga skal fylgja eftirfarandi skrefum.

1. Búa til eða velja eininguna sem á að skilgreina umreikningsreglur fyrir.
1. Veljið **Umreikningur eininga** á aðgerðasvæðinu.

    Síðan **Umreikningur eininga** birtist. Þú notar þessa síðu til að skilgreina reglur til að breyta völdu einingunni í og frá öðrum einingum í einingaflokknum.

1. Veljið einn af eftirfarandi flipum eftir því hvaða gerð umreiknings á að setja upp:

    - **Staðlaðir umreikningar** – Setja upp staðlaðar umreikningsreglur fyrir allar afurðir.
    - **Umreikningar innan flokks** – Setja upp afurðabundnar umreikningsreglur fyrir einingar í sama einingaflokki.
    - **Umreikningar á milli flokka** – Setja upp afurðabundnar umreikningsreglur fyrir einingar á milli einingaflokka.

1. Fylgið einu af eftirfarandi skrefum:

    - Til að stofna nýja umbreytingu skal velja **Ný** á tækjastiku.
    - Til að breyta núverandi umbreytingu skal velja umbreytinguna í netinu og síðan **Breyta** á tækjastikunni.

1. Í svarglugganum sem birtist, skal stilla eftirfarandi reiti:

    - **Vara** – Veljið vöruna sem umreikningurin á við um. Þessi reitur er aðeins í boði fyrir umreikninga innan flokks og milli flokka.
    - **Útlit formúlu** – Skiljið þennan reit stilltan á *Einfalt* til að tilgreina einfaldan umreikning sem er með einn stuðul. Stillið hana á *Ítarlegt* til að setja upp flóknari jöfnu. Snið fyrir ítarlegar jöfnur er breytilegt eftir einingarflokknum.
    - **Frá einingu** – Í þessum reit birtist valin eining. Yfirleitt ætti ekki að breyta gildinu. (Ef gildinu er breytt verður að opna síðuna **Umreikningur eininga** fyrir valda einingu til að skoða nýju breytinguna eftir að hún hefur verið vistuð.)
    - **Til einingar** – Velja skal eininguna sem á að umreikna í.
    - **Sléttun** – Veljið hvernig á að slétta brot út frá gildinu í **Nákvæmni aukastafa** af valdri einingu (*Til næsta*, *Upp* eða *Niður*).
    - **Umbreytingarformúla** – Notið eftirstandandi reiti efst í felliglugganum til að tilgreina formúluna fyrir umreikning milli tveggja eininga. Reitirnir sem eru tiltækir eru breytilegir eftir því hvaða einingaflokkur og formúluuppsetning var valin.

1. Veljið **Í lagi**.
1. Lokið síðunni.

> [!TIP]
> Einnig er hægt að setja upp einingarumreikning fyrir hvert vöruafbrigði. Frekari upplýsingar eru í [Umreikningur mælieiningar eftir afurðarafbrigði](../uom-conversion-per-product-variant.md).

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
