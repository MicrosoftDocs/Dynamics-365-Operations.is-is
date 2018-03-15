---
title: "Afurðarvíddir"
description: "Það eru fjórar afurðavíddir - Litur, Skilgreining, Stærð og Stíll. Afurðavíddir eru sameinaðar í víddaflokka og víddaflokkum er úthlutað á afurðarsniðmát. Samsetning afurðavídda ræður til um það hvernig afurðarafbrigði eru skilgreind."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDimension, EcoResProductDimensionGroup, EcoResProductMasterDimension, RetailEcoResColor, RetailEcoResSize, RetailEcoResStyle
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 9cb4bded4b8d841c6d164e6b8ded2cb3fb4d0978
ms.contentlocale: is-is
ms.lasthandoff: 02/07/2018

---

# <a name="product-dimensions"></a>Afurðarvíddir

[!include[banner](../includes/banner.md)]

[!include[Retail name](../includes/retail-name.md)]


Það eru fjórar afurðavíddir - Litur, Skilgreining, Stærð og Stíll. Afurðavíddir eru sameinaðar í víddaflokka og víddaflokkum er úthlutað á afurðarsniðmát. Samsetning afurðavídda ræður til um það hvernig afurðarafbrigði eru skilgreind.

Afurðavíddir eru einkenni sem notaður er til að auðkenna afurðarafbrigði. Hægt er að nota samsetningu afurðavídda til að skilgreina afurðarafbrigði. Skilgreina verður minnst eina vídd afurðar fyrir afurðarsniðmát til að stofna afurðarafbrigði.
Afurðarafbrigði
----------------

Afurðarafbrigði eru einnig nefndar vörur. Vara er áþreifanleg afurð sem er ekki það sama og þjónusta. Einnig hægt að skilgreina afurðarsniðmát með gerðinni Þjónusta. Með því að nota þjónustugerð, er hægt að tilgreina afurðarafbrigði sem innihalda þjónustu. Til dæmis er hægt að tilgreina afurðarsniðmát fyrir ráðgjafavinnu og afurða afbrigði fyrir vinnustöð sem er framkvæmd með hjá utanaðkomandi ráðgjöfum bókara og aðalbókara hjá utanaðkomandi ráðgjöfum.

## <a name="product-dimensions"></a>Afurðarvíddir
Eftirfarandi afurðavíddir eru tiltækar: Afbrigði, Litur, Stærð og Stíll. Hægt er að mynda afurðarafbrigði fyrir á grundvelli afurðarvíddargildi.

Gildi afurðarvídda eins og Stærð, Lit og Stíl er hægt að stofna á í **Stærð**, **Litur** og **Stíll** síðum sem hægt er að komast í úr eftirfarandi staðsetningum: **Afurðarupplýsingastjórnun** &gt; **Uppsetningu** &gt; **Vídd og afbrigðaflokkar** &gt; **Stærðir/Litir/Stílar**. Afurðarvíddargildi fyrir skilgreiningarvíddir eru yfirleitt stofnaðar með afurðaafbrigðastilli eða afurðarafbrigðastillis sem byggir á víddum. Vöruvíddir er einnig hægt að stofnað og þeim viðhaldið í **afurðarvíddir** síðu, sem fæst frá eftirfarandi staðsetningum:
-   Smellið á **Upplýsingar um afurðarstjórnun** &gt; **Afurðir** &gt; **Afurðarsniðmát**. Á **Aðgerðasvæði** skal smella á **Afurðarvíddir**.
-   Smellið á **Upplýsingastjórnun afurða** &gt; **Afurðir** &gt; **Allar afurðir og afurðarsniðmát**. Veljið afurðarsniðmát. Á **Aðgerðasvæði** skal smella á **Afurðarvíddir**.
-   Smellið á **Upplýsingastjórnun afurðar** &gt; **Útgefnar afurðir**. Veljið afurðarsniðmát. Í **Aðgerðasvæði** er smellt á **Afurð**. Í reitnum **afurðarsniðmát** flokki, skal velja **afurðarvíddir**.

Númer vöruvíddasamsetningar sem hægt er að stofna fyrir vöru er takmörkuð af fjölda afurð mögulegar samsetningar.
| **Ábending**                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------|
| Þegar þú notar afurð á til dæmis pöntunarlínu velurðu afurðavíddir til að tilgreina afurðarafbrigði sem á að vinna með. |

## <a name="example"></a>Dæmi
Fyrirtæki selur denim-gallabuxur. Varan, gallabuxur, notar lit og stærð afurðarvíddirnar. Gallabuxurnar eru til í þremur mismunandi litum og sex mismunandi stærðum. Litir: Blár, Svartur, brúnn Stærðir: XS, S, M, L, XL, XXL Ekki allar stærðir eru tiltækar í öllum þremur litum. Ef allar samsetningar voru tiltæk, hún myndi stofna 18 mismunandi gerðir af gallabuxur. Í þessu dæmi eru aðeins eftirfarandi níu vara afbrigði samsetningar framleitt.

| Litur | Stærð |
|-------|------|
| Blátt  | XS   |
| Blátt  | L    |
| Blátt  | M    |
| Svart | M    |
| Svart | L    |
| Svart | XL   |
| Brúnt | L    |
| Brúnt | XL   |
| Brúnt | XXL  |






