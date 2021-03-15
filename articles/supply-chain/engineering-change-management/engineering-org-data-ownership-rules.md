---
title: Hönnunarfyrirtæki og reglur um eignarrétt gagna
description: Þetta efnisatriði lýsir því hvernig má nota eitt eða fleiri hönnunarfyrirtæki til að ganga úr skugga um að aðalgögn fyrir afurðir séu stofnuð og unnin miðlægt. Hönnunarfyrirtæki táknar fyrirtækið sem er eigandi hönnunarafurðanna og viðeigandi hönnunartengdra gagna.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgEngineeringOrganization
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: ab5ca3bee65bb0ee8ce7f44ba97c00347fe38366
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963664"
---
# <a name="engineering-companies-and-data-ownership-rules"></a>Hönnunarfyrirtæki og reglur um eignarrétt gagna

[!include [banner](../includes/banner.md)]

## <a name="engineering-companies-and-operational-companies"></a>Hönnunarfyrirtæki og rekstrarfyrirtæki

Þú getur notað eitt eða fleiri *hönnunarfyrirtæki* til að ganga úr skugga um að aðalgögn hönnunarafurða séu stofnuð og unnin miðlægt. Hönnunarfyrirtæki er eigandi hönnunarafurða og viðeigandi hönnunartengdra gagna. Hönnunarfyrirtækið er alltaf tengt við (byggt á) fyrirliggjandi *lögaðila* sem er einnig fyrirtæki. Í gegnum þessa tengingu býr kerfið til miðlægan aðgangsstað fyrir öll viðeigandi hönnunartengd gögn fyrir hönnunarafurðir í hönnunarfyrirtækinu. Hönnunarafurðir eru stofnaðar í slíkum miðlægum aðgangsstað og unnið er með viðeigandi hönnunartengdum gögn. Þaðan verða hönnunarafurðir og hönnunartengd gögn losuð til *rekstrarfyrirtækja* sem eru aðrir lögaðilar. (Frekari upplýsingar um losunarstjórnun er að finna í [Skipulag afurðarlosunar](release-product-structure.md).) Slík rekstrarfyrirtæki nota hönnunargögnin eins og gögnin voru hönnuð af hönnunarfyrirtækinu. Hvert hönnunarfyrirtæki og hvert rekstrarfyrirtæki vinnur með öll skipulagsgögn á hverjum stað.

Opnaðu **Umsjón hönnunarbreytinga \> Uppsetning \> Hönnunarfyrirtæki** til að stofna hönnunarfyrirtæki. Smelltu á **Nýtt**, sláðu inn heiti hönnunarfyrirtækisins og veldu núverandi fyrirtæki (lögaðila) sem það byggist á.

Þegar þú samþættir líftímastjórnunarkerfi ytri afurða (PLM) verður þú að stofna viðskiptaeiningu (fyrirtækjagerð) sem verður ytra fyrirtæki.

## <a name="engineering-product-categories-and-engineering-companies"></a>Flokkar hönnunarafurða og hönnunarfyrirtæki

*Flokkar hönnunarafurða* tryggja að hönnunarafurðir séu stofnaðar í samræmi við viðskiptareglur fyrirtækisins þíns og hegði sér á áskilinn hátt. Frekari upplýsingar um flokka hönnunarafurða er að finna í [Hönnunarútgáfur og flokkar hönnunarafurðar](engineering-versions-product-category.md).

Hver flokkur hönnunarafurðar tilheyrir tilteknu hönnunarfyrirtæki og getur aðeins stofnað afurðir sem tilheyra því fyrirtæki. Á sama hátt tilheyrir einnig rétturinn til að vinna með hönnunarafurð fyrirtækinu sem tengist flokki hönnunarafurðar fyrir viðkomandi afurð.

## <a name="data-that-is-owned-by-the-engineering-company"></a>Gögn sem eru í eigu hönnunarfyrirtækisins

Vegna þess að hönnunarfyrirtækið á viðeigandi hönnunartengd gögn stjórnar fyrirtækið eftirfarandi ferlum:

- **Stofnun hönnunarafurða:** Hvert hönnunarfyrirtæki getur einungis stofnað hönnunarafurðir byggðar á flokki hönnunarafurða sem eru í eigu fyrirtækisins. Í sumum tilvikum geta rekstrarfyrirtæki unnið við eigin staðbundin gögn sem tengjast þessum afurðum.
- **Stofnun hönnunarútgáfu:** Þegar fyrirtæki stofnar nýja hönnunarafurð, býr kerfið sjálfkrafa til upprunalega hönnunarútgáfu afurðarinnar. Eingöngu hönnunarfyrirtækið sem er eigandinn getur stofnað nýjar útgáfur af umræddri af.
- **Stofnun og viðhald hönnunareiginda:** Þegar fyrirtæki stofnar nýja hönnunarafurð bætir kerfið sjálfkrafa við hönnunareigindum hana. Eingöngu hönnunarfyrirtækið sem er eigandinn getur stofnað og unnið með gildin fyrir slíkar eigindir. Frekari upplýsingar um hönnunareigindir er að finna í [Hönnunareigindir og leit að hönnunareigind](engineering-attributes-and-search.md).
- **Stofna og vinna með uppskriftir (BOM) sem eru tengdar við hönnunarútgáfur:** Hönnunarfyrirtækið sem er eigandinn getur tengt uppskrift beint við útgáfu hönnunarafurðar. Þegar þessar uppskriftir eru losaðar yfir á aðra lögaðila eru breytingar hönnunargagna á uppskriftunum takmarkaðar á eftirfarandi hátt:

    - Rekstrarfyrirtækið getur ekki fjarlægt birtar uppskriftarlínur.
    - Hönnunarsvæðin í uppskriftarlínunum eru skrifvarin fyrir rekstrarfyrirtækið. Öll önnur svæði eru framkvæmdarsvæði flutnings sem rekstrarfyrirtækið getur breytt.
    - Rekstrarfyrirtækið getur bætt uppskriftarlínum við sömu uppskriftina. Á þennan hátt getur það bætt við staðbundnum viðbótum, svo sem umbúðaefnum eða smurvökva.
    - Rekstrarfyrirtækið getur bætt við nýrri, staðbundinni uppskrift. Þessi breyting kann að vera nauðsynleg í tilvikum þegar t.d. engin uppskrift er látin í té þegar losað er. Rekstrarfyrirtækið er eigandinn og vinnur með slíkar staðbundnar uppskriftir. Frekari upplýsingar um losunarstjórnun er að finna í [Skipulag afurðarlosunar](release-product-structure.md).
    - Allar staðbundnar uppskriftir og uppskriftarlínur eru varðveittar þegar hönnunarfyrirtækið uppfærir uppskriftir sínar.

- **Stofna og vinna með leiðir sem eru tengdar við hönnunarútgáfurnar:** Hönnunarfyrirtækið getur tengt leið beint við hverja hönnunarútgáfu. Þegar þessar leiðir eru losaðar til annarra lögaðila verða breytingar á leiðunum takmarkaðar á eftirfarandi hátt:

    - Hinir lögaðilarnir geta ekki fjarlægt hönnunargögnin á leiðunum.
    - Hinir lögaðilarnir geta bætt við aðgerðum á leiðina. Á þennan hátt er hægt að bæta við staðbundnum leiðarskrefum.
    - Rekstrarfyrirtæki geta bætt við nýjum, staðbundnum leiðum. Þessi breyting gæti verið nauðsynleg ef leiðir hafa til dæmis ekki verið teknar með við losun. Rekstrarfélögin eiga og viðhalda þessum staðbundnu leiðum. Frekari upplýsingar um losunarstjórnun er að finna í [Skipulag afurðarlosunar](release-product-structure.md).
    - Allar breytingar sem eru gerðar staðbundið eru varðveittar þegar uppfærslur frá hönnunarfyrirtækinu eru losaðar aftur til leiðanna.

- **Stofna og vinna með hönnunarskjöl:** Hönnunarfyrirtækið getur hengt hönnunarskjöl við hverja hönnunarútgáfu.

    - Þegar þessi skjöl eru losuð til annarra lögaðila eru skjölin skrifvarin og rekstrarfyrirtækið getur því ekki fjarlægt þau.
    - Aðrir lögaðilar geta bætt við alveg nýjum, staðbundnum fylgiskjölum. Rekstrarfyrirtækið er eigandinn og vinnur með slík staðbundin skjöl.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]