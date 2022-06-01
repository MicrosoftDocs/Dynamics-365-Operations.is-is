---
title: Gagnvirk eiginleikaeining
description: Þetta efnisatriði fjallar um gagnvirkar eiginleikaeiningar og útskýrir hvernig á að bæta þeim við síður svæða í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3ab325189812289390740e31fd673ee9892f9759
ms.sourcegitcommit: ccb39767bd3430c24f4653c26560bba2cd66553c
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/19/2022
ms.locfileid: "8780740"
---
# <a name="interactive-feature-module"></a>Gagnvirk eiginleikaeining

[!include [banner](includes/banner.md)]

Þetta efnisatriði fjallar um gagnvirkar eiginleikaeiningar og útskýrir hvernig á að bæta þeim við síður svæða í Microsoft Dynamics 365 Commerce.

Gagnvirkar einingar eiginleika eru mósaíklíkar einingar sem hægt er að nota til að markaðssetja marga vöruflokka eða vörumerki með því að nota samsetningu mynda og texta. Til dæmis getur smásali bætt gagnvirkri einingu eiginleika við heimasíðu rafræns viðskiptasvæðis til að auglýsa flokka með mest seldu vörurnar. Gagnvirk eining eiginleikans líkist reitalistaeiningunni en er með öðruvísi útlit og aðrar samskiptaaðgerðir.

Hver gagnvirk eining eiginleika er safn af einingum yfir gagnvirk eiginleikaatriði. Hver eining eiginleikaatriðis er knúin áfram af gögnum frá efnisstýringarkerfinu (CMS). Hún er ekki háð öðrum einingum eða gögnum frá Commerce Headquarters. Hægt er að bæta einingu gagnvirks eiginleika við hvaða vefsíðu sem er þar sem smásali vill markaðssetja eða auglýsa eitthvað (til dæmis afurðir, flokka eða vörumerki).

> [!IMPORTANT]
> - Eining gagnvirks eiginleika er í boði frá og með Dynamics 365 Commerce útgáfu 10.0.20.
> - Gagnvirk eiginleikaeining er sýnd í þema Adventure Works.

Eftirfarandi mynd sýnir dæmi um einingu gagnvirks eiginleika á heimasíðu Adventure Works.

![Dæmi um einingu gagnvirks eiginleika á heimasíðu Adventure Works](./media/Feature.PNG)

## <a name="interactive-feature-module-and-themes"></a>Gagnvirk eiginleikaeining og þemu

Eining gagnvirks eiginleika getur stutt ýmis útlit og stíla út frá þema. Í þema Adventure Works getur eining gagnvirks eiginleika til dæmis verið með tveggja dálka útlit sem sýnir hreyfingar þegar notandi vefsvæðis er með músarbendilinn yfir vöru. Eining gagnvirks eiginleika er stillt inn á slétta tölu af myndum sem er raðað í tveggja dálka útlit.

## <a name="interactive-feature-module-properties"></a>Eiginleikar gagnvirkrar eiginleikaeiningar

| Nafn eiginleika | Gildi | lýsing |
|---------------|--------|-------------|
| Haus       | Texti og merki fyrirsagnar (**H1**, **H2**, **H3**, **H4**, **H5** eða **H6**) | Textafyrirsögn fyrir einingu gagnvirks eiginleika. |

## <a name="interactive-feature-item-module-properties"></a>Eiginleikar einingar fyrir gagnvirkt eiginleikaatriði

| Nafn eiginleika | Gildi | lýsing |
|---------------|--------|-------------|
| Mynd         | Myndaskrá | Mynd sem sýnir afurð eða flokk. Hægt er að hlaða mynd inn í miðlasafnið í vefsmið Commerce eða nota mynd sem er til staðar. |
| Haus       | Texti og merki fyrirsagnar (**H1**, **H2**, **H3**, **H4**, **H5** eða **H6**) | Sjálfgefið er að fyrirsagnarmerkið **H2** er notað fyrir fyrirsögnina, en breyta má merkinu til að uppfylla kröfur um aðgengi. |
| Efnisgrein     | Texti efnisgreinar | Einingin styður málsgreinatexta með ríku textasniði. Stuðningur er við nokkra grunntextaeiginleika, eins og tengla og feitletrun, undirstrikun og skáletrun texta. Sumum af þessum eiginleikum er hægt að hnekkja með síðuþema sem er beitt á eininguna. |
| Tengill          | Tenglatexti, vefslóð tengils, ARIA-merki (Accessible Rich Internet Applications) og valið **Opnaðu hlekk í nýjum flipa** | Einingin styður einn eða fleiri „kalla til aðgerða“ tengla. Ef tengli er bætt við þarf tenglatexta, vefslóð og ARIA-merki. ARIA-merki ættu að vera lýsandi til að uppfylla kröfur um aðgengi. Hægt er að stilla tengla þannig að þeir séu opnaðir á nýjum flipa. |

## <a name="add-an-interactive-feature-module-to-a-new-page"></a>Bæta gagnvirkri eiginleikaeiningu við nýja síðu

Til að bæta einingu gagnvirks eiginleika við nýja síðu og stilla nauðsynlega eiginleika í vefsmið Commerce skal fylgja þessum skrefum.

1. Farðu í **Sniðmát** og opnaðu markaðssetningarsniðmátið fyrir heimasíðu vefsvæðisins (eða búðu til nýtt sniðmát markaðssetningar).
1. Í **Aðal** rauf sjálfgefna síðunnar, veldu sporbaug (**...**), og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu **Gagnvirkur eiginleiki** mát og veldu síðan **Allt í lagi**.
1. Veldu **Vista**, síðan **Ljúka við breytingar** til að skila sniðmáti og veldu síðan **Birta** til að birta það.
1. Farðu í **Síður** og opnaðu heimasíðu vefsvæðisins (eða búðu til nýja heimasíðu með sniðmáti markaðssetningar).
1. Í **Aðal** rauf sjálfgefna síðunnar, veldu sporbaug hnappinn (**...**), og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** svargluggi, undir **Veldu Modules**, veldu **Gagnvirkur eiginleiki** mát og veldu síðan **Allt í lagi**.
1. Í eiginleikaglugga einingar fyrir gagnvirkan eiginleika skal bæta við fyrirsögn.
1. Í **Gagnvirkur eiginleiki** rauf, veldu sporbaughnappinn (**...**), og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu **Gagnvirkt atriði** mát og veldu síðan **Allt í lagi**.
1. Bættu við mynd, fyrirsagnartexta, málsgreinatexta og vefslóð í eiginleikarúðu gagnvirku eiginleikahlutareiningarinnar.
1. Bættu við og skilgreindu fleiri einingar fyrir gagnvirkt eiginleikaatriði eftir þörfum.
1. Veldu **Vista** og veldu síðan **Forskoðun** til að forskoða síðuna.
1. Veldu **Ljúka við breytingar** til að athuga með sniðmátið og veldu síðan **Birta** til að birta það.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit einingasafns](starter-kit-overview.md)

[Þema Adventure Works](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
