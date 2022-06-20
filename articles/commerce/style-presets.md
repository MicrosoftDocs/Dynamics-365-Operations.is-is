---
title: Vinna með forstillta stíla
description: Þessi grein lýsir því hvernig á að vinna með forstillingar vefstíls í Microsoft Dynamics 365 Commerce vefsmiður.
author: phinneyridge
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0a06052ab29502c57a2ad5a25e5bec870585ef4a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900361"
---
# <a name="work-with-style-presets"></a>Vinna með forstillta stíla

[!include [banner](includes/banner.md)]

Þessi grein lýsir því hvernig á að vinna með forstillingar vefstíls í Microsoft Dynamics 365 Commerce vefsmiður.

Forstilltur stíll er safn af öllum höfundarlegum stílgildum í þema svæðisins. Hægt er að nota hann til að breyta strax útliti svæðis úr svæðissmið. Forstilltir stílar gera höfundum Commerce-svæðissmið kleift að breyta, forskoða og virkja safn stílgilda á svæðinu þeirra, án þess að þurfa að nota stallað stílblað (CSS) eða nota þemu. Leturstílar, hnappastílar og litir á svæði eru góð dæmi um stílbreytur sem hægt er að stjórna í gegnum forstillta stíla.

Safn stílbreyta sem eru í boði á svæði ákvarðast af þema- og einingasafni sem sett er upp hjá leigjanda svæði. Hugbúnaðarþróunarpakkinn Dynamics 365 Commerce á netinu gerir þróunaraðilum kleift að innleiða eins margar (eða eins fáar) höfundarlegar stílbreytur eins og þörf krefur fyrir tiltekið þema. Með því að virkja fleiri stílbreytur getur þróunaraðili þema komið lokaákvörðunum um stílsnið í hendurnar á þeim sem búa til svæðið. Þess vegna geta þeir sem ekki eru þróunaraðilar uppfært og forskoðað stílsnið með því að nota verkfærakistuna. Möguleikinn er einnig gagnlegur fyrir allar aðstæður þar sem beinar breytingar á þema eða CSS munu valda óþarfa umstangi.

Þemu þar sem höfundarlegar stílbreytur eru virkjaðar þarfnast sjálfgefins forstillts stíls. Þau mega innihalda fleiri forstillta valkosti sem hluti af uppsettum þemapakka. Til dæmis er hægt að nota þema sem er með einn sjálfgefinn forstilltan stíl, „nýtískuleg lýsing“. Að öðrum kosti gæti það falið í sér aðra valkosti fyrir forstillt stíleinkenni heldur en sjálfgefnu forstillinguna, t.d. „nýtískulegt rökkur“, „gamaldags lýsing“ eða „gamaldags rökkur“. Þessar innbyggðu forstillingar eru búnar til af þróunaraðilum og er hægt að nota sem upphafspunkt nýrrar hönnunar á síðu.

Í svæðissmiðnum geta höfundar valið úr safni innbyggðra forstilltra þema, eða þeir geta búið til sína eigin forstilltu stíla og sérstillingar með því að nota virkjuðu stílbreyturnar. Hægt er að forskoða forstilltan stíl í svæðissmið áður en hann er virkjaður á raunverulega svæðinu. Þegar stílbreytingar höfundar hafa verið skoðaðar er hægt að stilla forstilltan stíl á „virkur“ fyrir raunverulega svæðið.

## <a name="preview-a-style-preset"></a>Forskoða forstilltan stíl

Til að forskoða forstilltan stíl á svæðinu þínu í svæðissmiðnum skal fylgja þessum skrefum.

1. Vinstra megin á yfirlitssvæðinu skal opna **Stillingar svæðis \> Hönnun**.
1. Í flipanum **Forstillingar stíla**, efst í hönnunarritlinum, í listanum **Tiltækar forstillingar**, skal velja forstillingu og síðan velja **Skoða** til að fara í forstilltan ritil.

    Ef engar forstillingar eru til staðar í listanum **Tiltækar forstillingar** skal skoða [Búa til sérsniðinn forstilltan stíl](#create-a-custom-style-preset) til að fá upplýsingar um hvernig á að búa til sérsniðinn forstilltan stíl.

    > [!NOTE]
    > Forstillingar sem fylgdu með þemanu eru tilgreindar með merkinu **Innbyggt**. Þessar innbyggðu forstillingar eru skrifvarðar. Til að afrita innbyggða forstillingu sem nýja sérstillanlega forstillingu skal velja úrfellingarmerkið (**...**) fyrir forstillinguna og síðan velja **Vista sem**.

1. Á skipanastikunni skal velja **Forskoða**.
1. Veljið vefslóð af svæðinu ykkar til að nota til að forskoða forstillta stílinn og veljið síðan **Í lagi**.
1. Veljið afbrigði vefslóðar, sem miðast við rás og staðsetningu, til að forskoða með því að velja heiti afbrigðisins. Nýr forskoðunargluggi í vafranum opnast þar sem valin forstilling stíls er notuð á tiltekna síðu.

> [!NOTE]
> Forskoðunarslóðin er varanleg og sannvottuð. Þess vegna er hægt að afrita, líma og senda hana á aðra sannvottaða samstarfsmenn til skoðunar áður en hún er stillt á „virk“ á raunverulega svæðinu. Forskoðunarslóðin er einnig gagnleg til að athuga stíl á mismunandi tækjum, í mismunandi vöfrum og á mismunandi skjám.

> [!TIP]
> Þegar forstilltum stíl er breytt gæti reynst gagnlegt að skilja vafraglugga forskoðunar eftir opinn í aðskildum vafraglugga, svo fljótlegt sé að sannreyna breytingarnar. Þegar búið er að vista breytingarnar í forstillingu þarf að uppfæra opinn vafraglugga forskoðunar til að staðfesta notandaupplifunina.

## <a name="create-a-custom-style-preset"></a>Búa til sérsniðinn forstilltan stíl

Til að búa til sérsniðinn forstilltan stíl í svæðissmið skal fylgja þessum skrefum.

1. Vinstra megin á yfirlitssvæðinu skal opna **Stillingar svæðis \> Hönnun**.
1. Í flipanum **Forstillingar stíla**, efst í hönnunarritlinum, í skipanastikunni, skal velja **Ný forstilling**.
1. Færa skal inn heiti og lýsingu fyrir nýju forstillinguna og síðan velja **Vista**. Ný sérstillanleg forstilling er búin til sem notar sjálfgefin gildi þemans sem upphafspunkt.

> [!NOTE]
> Einnig er hægt að búa til nýja forstillingu sérsniðins stíls úr einhverri fyrirliggjandi forstillingu með því að velja úrfellingarmerkið (**...**) fyrir þá forstillingu og velja síðan **Vista sem**. Einnig er hægt að velja **Vista sem** á skipanastikunni í ritli forstillingar.

## <a name="modify-global-and-module-type-style-values"></a>Breyta altækri gerð og einingargerð stílgilda

Sumar stílbreytur þema eru samnýttar af mörgum einingargerðum. Þessar stílbreytur nefnast *altækar* stílbreytur. Sem dæmi má nefna liti á aðalsvæði, sjálfgefna stíla leturgerðar og hnappastílar. Ef altækar breytur eru stilltar er hugsanlega verið að breyta útliti margra mismunandi einingargerða.

Sum stílgildi geta verið einkvæm fyrir einingargerð eða þau gætu þurft að hnekkja sjálfgefnu altæku gildi. Ef þema svæðis hefur innleitt stílbreytur einingargerðar geta höfundar svæðissmiðs sérsniðið stíl einingargerðar óháð altækum stillingum. Breytur einingargerðar geta annaðhvort aukið eða hnekkt altækum stílbreytum í þema.

> [!NOTE]
> Stigveldi stílgilda á svæði fer fram með eftirfarandi hætti. Stílgildi sem birtast lengra til hægri hnekkja stílgildunum vinstra megin við þau.
>
> Sjálfgefin gildi þema \< Altæk stílgildi \< Stílgildi einingargerðar \< CSS hnekkja

Til að breyta forstilltum stílgildum af altækri gerð eða einingargerð stíls í svæðissmið skal fylgja þessum skrefum.

1. Vinstra megin á yfirlitssvæðinu skal opna **Stillingar svæðis \> Hönnun**.
1. Í flipanum **Forstillingar stíla**, efst í hönnunarritlinum, skal velja **Skoða** fyrir einhverja forstillingu stíls til að fara í ritil forstillingar.
1. Veljið **Forskoða** og fylgið síðan leiðbeiningum um val á vefslóð til að opna forskoðun í vafraglugga í fullri stærð með forstillingunni. Skiljið þennan vafraglugga forskoðunar eftir opinn.
1. Í ritli forskoðunar skal velja **Breyta** efst í hægra horninu.
1. Nota skal stjórnun stílbrigða í ritlinum til að breyta nokkrum altækum stílgildum.
1. Efst í ritlinum, í flipanum **Einingar** hægra megin við flipann **Altækt** skal velja einingargerð sem verður að stílgera.
1. Notið stílstjórnun til að breyta nokkrum gildum fyrir einingargerðina.
1. Þegar notandi er reiðubúinn að forskoða breytingarnar skal velja **Vista** á skipanastikunni.
1. Fara skal aftur í opinn vafraglugga forskoðunar og endurhlaða hann. Forskoðun í vafraglugga í fullri stærð er gagnleg til þess að athuga stílbreytingar á mismunandi rofstöðum, í mismunandi vöfrum og á mismunandi verkvangstækjum.
1. Þegar öllum breytingum er lokið og þær staðfestar skal velja **Ljúka við breytingar** efst hægra megin í ritlinum.

> [!NOTE]
> Ef þú ert að breyta forstillingu stílsins sem er virkur á svæðinu þínu sem stendur, sérðu blátt merki **Virk** í ritlinum. Þetta merki gefur til kynna að forstillingin er virk á vefsvæðinu þínu. Ef virku forstillingunni er breytt skal velja **Birta** til að flytja þessar breytingar yfir á raunverulega svæðið.

## <a name="make-a-new-style-preset-active-on-your-live-site"></a>Búa til nýja forstillingu stíls á raunverulega svæðinu

Til að stilla forstilltan stíl sem nýju virku forstillinguna á svæðinu þínu skaltu fylgja þessum skrefum.

- Veljið **Stilla sem virkt** á einum af þessum stöðum:

    - Skipanastikan í ritli forstillingar stíls
    - Úrfellingarvalmyndin (**...**) fyrir einhverja tiltæka forstillingu í aðalyfirlitinu í flipanum **Forstillingar stíla** í **Stillingar svæðis \> Hönnun**

Stílgildi forstillingar eru gerð virk á almenna vefsvæðinu.

## <a name="additional-resources"></a>Frekari upplýsingar

[Bæta við lógói](add-logo.md)

[Velja þema svæðis](select-site-theme.md)

[Unnið með CSS hnekkiskrám](css-override-files.md)

[Bæta við táknmynd](add-favicon.md)

[Bæta við yfirlýsingu um höfundarrétt](add-copyright-notice.md)

[Bæta tungumálum við síðuna](add-languages-to-site.md)

[Bæta skriftarkóða við síður vefsvæðis til að aðstoða við fjarmælingar](add-telemetry.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
