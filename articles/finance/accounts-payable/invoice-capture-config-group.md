---
title: Stillingarhópar fyrir lausnarupptöku reikninga
description: Þessi grein veitir almennar upplýsingar um stillingarhópa í reikningsfangalausninni.
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
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690994"
---
# <a name="invoice-capture-solution-configuration-groups"></a>Stillingarhópar fyrir lausnarupptöku reikninga

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Notendur geta stjórnað lista yfir reikningareitir og handvirka yfirferðarstillingu fyrir lögaðila með því að nota stillingarhópa. Notendur geta sett upp reikningsstillingar fyrir mismunandi lögaðila í hópum. Allir lögaðilar í sama stillingarhópi nota sömu reikningareitina og handvirka yfirferðarstillingu.

## <a name="manage-configuration-groups"></a>Vinna með skilgreiningaflokka

Til að stjórna stillingarhópum með því að nota appið, farðu á **Uppsetning**, og veldu síðan **Kerfisuppsetning \> Skilgreindu stillingarhópa íhlut**.

Á **Skilgreindu stillingarhópa** síðu sýnir aðalflipi lista yfir stillingarhópa sem hafa verið skilgreindir. Það sýnir einnig sjálfgefna stillingarhóp. Fyrir hvern stillingarhóp eru eftirfarandi aðgerðir tiltækar:

- **Afritaðu stillingarhóp** – Þú getur búið til nýjan stillingarhóp með því að afrita hóp sem fyrir er. Nýi hópurinn hefur sömu gildi og upphaflegi hópurinn fyrir alla reiti nema **Nafn hóps** og **Hóplýsing**. Eftir að stillingarhópurinn hefur verið afritaður skaltu velja **Allt í lagi**.
- **Eyða stillingarhópum** – Til að eyða stillingarhópi velurðu hann og velur svo **Eyða**.

    > [!NOTE]
    > Ekki er hægt að eyða sjálfgefna stillingarhópnum.

- **Breyttu auðkenni stillingarhóps** – Til að breyta auðkenni stillingahóps velurðu **Hópauðkenni** reit og uppfærðu gildið. Hópauðkennið ætti ekki að innihalda bil eða sérstafi og það ætti ekki að vera meira en 20 stafir.

    > [!NOTE]
    > Verðmæti **Hópauðkenni** reitinn er aðeins hægt að uppfæra einu sinni.

- **Breyttu lýsingu stillingarhóps** – Til að breyta lýsingu á stillingarhópi skaltu velja **Lýsing** reit og uppfærðu gildið.
- **Breyttu stillingu handvirkrar skoðunar** – Notendur geta ákveðið hvort reikningur þurfi að fara yfir handvirkt. Til að breyta handvirkri skoðunarstillingu skaltu velja **Þarf handvirka endurskoðun** valmöguleika. Eftirtaldir valkostir eru í boði:

    - **Alltaf handvirk skoðun** – Veldu þennan valkost ef reikningar í stillingarhópnum krefjast alltaf handvirkrar skoðunar.
    - **Fyrir villur og viðvaranir** – Veldu þennan valkost ef reikningar sem innihalda villuboð eða viðvörunarskilaboð krefjast handvirkrar yfirferðar.
    - **Fyrir villur** – Veldu þennan valkost ef reikningar sem innihalda villuboð krefjast handvirkrar yfirferðar.

- **Breyttu öryggisstigastillingunni** – Öryggisstigið er lýsigögn sem Invoice capture lausnin veitir til að tilkynna um nákvæmni viðurkenndra reikningsgagna. Því hærra sem stigið er, því nákvæmari gætu viðurkenndu gögnin verið. Stillingin gerir notendum kleift að skilgreina hvenær handvirkrar endurskoðunar er krafist, byggt á öryggisstiginu. Notendur geta breytt öryggismörkum fyrir reikninga. Til að uppfæra öryggisstigastillinguna skaltu velja **Sjálfstraust stig** reit og uppfærðu gildið.

    Það eru tvær viðvörunargerðir fyrir öryggisstig:

    - **Viðvörun** – Reitir reikninga sem hafa öryggisstig yfir viðvörunarmörkum teljast réttir. Viðvörunarþröskuldurinn verður að vera hærri en villuþröskuldurinn og minna en 100.
    - **Villa** – Reitir reikninga sem hafa öryggisstig undir villumörkum teljast misheppnaðir. Villuskilaboð verða sýnd notanda. Villuþröskuldurinn verður að vera meiri en 0 (núll) og lægri en viðvörunarþröskuldurinn. Viðvörunarskilaboð verða sýnd fyrir reikningareiti sem hafa öryggisstig á milli viðvörunarþröskulds og villuþröskulds.

- **Stjórna reikningsreitum** - Notendur geta stjórnað listanum yfir reikningareiti sem eru sýndir í hlið við hlið skoðara. Á **Reikningarstjórnun** flipann, veldu tannhjólstáknið, veldu reikningsreitina til að bæta við og veldu síðan **Vista**. Völdum reitum verður bætt við listann. Til að fjarlægja reikningsreit af listanum velurðu **Fjarlægja** á vellinum.

### <a name="manage-file-filters-optional"></a>Stjórna skráasíum (valfrjálst)

Stjórna skráasíur gerir notendum kleift að skilgreina viðbótarsíur fyrir reikningaskrár á innleið. Skrár sem uppfylla ekki síuskilyrðin verða móttekin og munu birtast í **Mótteknar skrár** lista, en þeir munu sýna skráarstaðfestingarvillur. Þessi hegðun er frábrugðin hegðun fyrir síur sem eru skilgreindar í rásinni. Fyrir þessar síur munu skrár sem uppfylla ekki skilyrðin alls ekki berast. Notendur geta skoðað innkomnar skrár og ákveðið hvort hver skrá sé ógildur reikningur, og þeir geta úrelt skrána eða látið hana fylgja með handvirkt til að bera kennsl á og setja inn í reikninga.

Þegar reikningsfangalausnin er sett upp er sjálfgefin skráasía skilgreind. Þessi skráasía er alþjóðleg. Ef þú vilt aðrar síustillingar geturðu uppfært sjálfgefna síuna. Ef reit er skyldubundið skaltu velja **Áskilið**. 

### <a name="accepted-file-size"></a>Samþykkt skráarstærð

Þú getur valið samþykkta skráarstærð.

> [!NOTE]
> Skrár sem eru stærri en 20.480 kílóbæti (KB) eru ekki studdar.

### <a name="supported-file-types"></a>Stuðlar skráargerðir

Eftirfarandi skráargerðir eru studdar eins og er:

- PDF
- PNG
- JPG
- JPEG
- TIF
- TIFF
