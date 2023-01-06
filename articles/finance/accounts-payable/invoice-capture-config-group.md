---
title: Stillingahópar Invoice Capture-lausnar
description: Þessi grein veitir almennar upplýsingar um stillingahóp í Invoice capture lausninni.
author: sunfzam
ms.date: 09/28/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: cfe5ae35b4f87a350d944b30a49251081766ad27
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690994"
---
# <a name="invoice-capture-solution-configuration-groups"></a>Stillingahópar Invoice Capture-lausnar

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Notendur geta stjórnað listanum yfir reikningsreiti og handvirkar stillingar fyrir yfirferð fyrir lögaðila með því að nota stillingahópana. Notendur geta sett upp reikningsstillingar fyrir mismunandi lögaðila í hópum. Allir lögaðilar í sama stillingahópi nota sömu reikningsreiti og handvirkar stillingar fyrir yfirferð.

## <a name="manage-configuration-groups"></a>Vinna með skilgreiningaflokka

Til að stjórna stillingahópum með því að nota forritið skaltu fara í **Uppsetning** og velja **Kerfisuppsetning \> Skilgreina stillingahópa**.

Á síðunni **Skilgreina stillingahópa** sýnir aðalflipinn lista yfir stillingahópa sem hafa verið skilgreindir. Hann sýnir einnig sjálfgefinn stillingahóp. Fyrir hvern stillingahóp eru eftirfarandi aðgerðir í boði:

- **Afrita stillingahóp** – Þú getur búið til nýjan stillingahóp með því að afrita hóp sem fyrir er. Nýi hópurinn er með sömu gildi og upprunalegi hópurinn fyrir alla reitina nema **Heiti hóps** og **Lýsing á hópi**. Eftir að stillingahópur hefur verið afritaður skal velja **Í lagi**.
- **Eyða stillingahópum** – Til að eyða stillingahópi skal velja hann og velja **Eyða**.

    > [!NOTE]
    > Ekki er hægt að eyða sjálfgefnum stillingahópi.

- **Breyta auðkenni stillingahóps** – Til að breyta auðkenni stillingahóps, veldu reitinn fyrir **Kenni hóps** og uppfærðu gildið. Auðkenni hóps mega ekki innihalda bil eða sérstafi og þau mega ekki vera lengri en 20 stafir.

    > [!NOTE]
    > Gildi **Auðkenni hóps** er aðeins hægt að uppfæra einu sinni.

- **Breyta lýsingu stillingahóps** – Til að breyta lýsingu á stillingahópi skaltu velja reitinn **Lýsing** og uppfæra gildið.
- **Breyta stillingu handvirkrar yfirferðar** – Notendur geta ákveðið hvort reikningur verður að vera yfirfarinn handvirkt. Til að breyta stillingu handvirkrar yfirferðar skal velja **Þarf handvirka yfirferð**. Eftirtaldir valkostir eru í boði:

    - **Alltaf handvirk yfirferð** – Veljið þennan kost ef reikningar í stillingahópnum krefjast alltaf handvirkrar yfirferðar.
    - **Fyrir villur og viðvaranir** – Veljið þennan valkost ef reikningar sem innihalda villuboð eða viðvörunarskilaboð krefjast handvirkrar yfirferðar.
    - **Fyrir villur** – Veljið þennan valkost ef reikningar sem innihalda villuboð krefjast handvirkrar yfirferðar.

- **Breyta stillingu öryggisstigs** – Öryggisstigið eru lýsigögn sem Invoice capture lausnin veitir til að sýna nákvæmni auðkenndra reikningsgagna. Því hærra sem stigið er, því nákvæmari kunna auðkennd gögn að vera. Stillingarnar gera notendum kleift að skilgreina hvenær þörf er á handvirkri skoðun, á grundvelli öryggisstigsins. Notendur geta breytt viðmiðunarmörkum fyrir öryggisstig fyrir reikninga. Til að uppfæra stillinguna fyrir öryggisstig skaltu velja reitinn **Öryggisstig** og uppfæra gildið.

    Til eru tvenns konar viðvaranir fyrir áreiðanleikaeinkunn:

    - **Viðvörun** – Reikningsreitir sem eru með öryggisstig yfir viðvörunarþröskuldi eru taldir réttir. Viðvörunarþröskuldurinn verður að vera hærri en villumörkin og minni en 100.
    - **Villa** – Reikningsreitir sem eru með öryggisstig undir villumörkum eru taldir fallnir. Notandinn sér villuboð. Villuþröskuldurinn verður að vera hærri en 0 (núll) og minni en viðvörunarþröskuldurinn. Viðvörunarskilaboð verða sýnd fyrir reikningareiti sem eru með öryggisstig á milli viðvörunarþröskulds og villumarka.

- **Stjórna reikningsreitum** – Notendur geta stjórnað lista yfir reikningsreiti sem er sýndur á hliðarsvæði. Á flipanum **Stjórnun reikningsreitar** velja gíratáknið, velja reikningsreiti til að bæta við og velja svo **Vista**. Völdu reitunum verður bætt á listann. Til að fjarlægja reikningsreit af listanum skal velja **Fjarlægja** á reitnum.

### <a name="manage-file-filters-optional"></a>Stjórna skráarsíum (valfrjálst)

Stjórna skráarsíum gerir notendum kleift að skilgreina fleiri síur fyrir mótteknar reikningsskrár. Skrár sem uppfylla ekki síuskilyrðin verða mótteknar og munu birtast á listanum yfir **Mótteknar skrár**, en þær munu sýna villur við villuleit. Þessi hegðun er frábrugðið hegðun fyrir síur sem eru skilgreindar í rásinni. Fyrir þessar síur eru skrár sem uppfylla ekki skilyrðin ekki mótteknar yfir höfuð. Notendur geta farið yfir mótteknar skrár og ákveðið hvort hver skrá sé ógildur reikningur og geta þá úrelt skrána eða tekið hana handvirkt með til að auðkenna og taka með í fönguðum reikningum.

Þegar lausnin Invoice capture er uppsett er sjálfgefin skráarsía skilgreind. Þessi skráarsía er altæk. Ef þú vilt hafa aðrar síustillingar getur þú uppfært sjálfgefnu síuna. Ef reitur er áskilinn skal velja **Áskilið**. 

### <a name="accepted-file-size"></a>Samþykkt skráarstærð

Hægt er að velja samþykkta skráarstærð.

> [!NOTE]
> Skrár sem eru stærri en 20.480 kílóbæti (KB) eru ekki studdar.

### <a name="supported-file-types"></a>Studdar skráargerðir

Eftirfarandi skráargerðir eru studdar:

- PDF
- PNG
- JPG
- JPEG
- TIF
- TIFF
