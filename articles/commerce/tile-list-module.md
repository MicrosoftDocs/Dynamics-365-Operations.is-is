---
title: Reitalistaeining
description: Þessi grein fjallar um einingar með flísum og lýsir því hvernig á að bæta þeim við vefsíður í Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 44eb9b82ef9625734c7fe5ccba85207d9f210a00
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905399"
---
# <a name="tile-list-module"></a>Reitalistaeining

[!include [banner](includes/banner.md)]

Þessi grein fjallar um einingar með flísum og lýsir því hvernig á að bæta þeim við vefsíður í Microsoft Dynamics 365 Commerce.

Reitalistaeining er safn af reitum í myndaræmu. Hún er notuð til að markaðssetja afurðarflokka eða vörumerki í gegnum myndir og texta. Til dæmis getur smásali bætt reitalistaeiningu við heimasíðu rafræns viðskiptasvæðis til að auglýsa flokka með vinsælustu vörunum.

Reitalistaeiningin er knúin áfram af gögnum frá efnisstýringarkerfinu (CMS). Hún er ekki háð öðrum einingum eða gögnum frá Commerce Headquarters. Hægt er að bæta reitalistaeiningunni við hvaða vefsíðu sem er þar sem smásali vill markaðssetja eða auglýsa eitthvað (til dæmis afurðir, flokka eða vörumerki).

Eftirfarandi mynd sýnir dæmi um reitalistaeiningu og reitaeiningar á heimasíðu Adventure Works.

![Dæmi um reitalistaeiningu og reitaeiningar á heimasíðu Adventure Works](./media/Tile_list.PNG)

> [!IMPORTANT]
> Reitalistaeiningin er í boði frá og með Dynamics 365 Commerce útgáfu 10.0.20.
> Reitalistaeiningin er sýnd í þema Adventure Works.

## <a name="tile-list-modules-and-themes"></a>Reitalistaeiningar og þema

Reitalistaeiningar geta stutt ýmis útlit og stíla út frá þema. Í þema Adventure Works geta reitir til dæmis sýnt hreyfimyndir þegar notendur vefsvæðisins fara með músarbendilinn yfir hana. Hvert þema getur innihaldið fleiri eiginleika fyrir reitalista og reitaeiningar. Þróunaraðilar þema geta einnig búið til fleiri útlit fyrir reitalista og reitaeiningar.

## <a name="tile-list-module-properties"></a>Eiginleikar reitalistaeiningar

| Nafn eiginleika | Gildi | lýsing |
|---------------|--------|-------------|
| Haus       | Texti og merki fyrirsagna | Textafyrirsögn fyrir reitalistaeininguna. |

## <a name="tile-module-properties"></a>Eiginleikar reitaeiningar

| Nafn eiginleika | Gildi | lýsing |
|---------------|--------|-------------|
| Mynd         | Myndaskrá | Hægt er að nota mynd til að sýna vöru eða flokk. Hægt er að hlaða mynd inn í miðlasafnið í vefsmið Commerce eða nota mynd sem er til staðar. |
| Haus       | Texti og merki fyrirsagnar (**H1**, **H2**, **H3**, **H4**, **H5** eða **H6**) | Sjálfgefið er að fyrirsagnarmerkið **H2** er notað fyrir fyrirsögnina, en breyta má merkinu til að uppfylla kröfur um aðgengi. |
| Efnisgrein     | Texti efnisgreinar | Einingin styður málsgreinatexta með ríku textasniði. Stuðningur er við nokkra grunntextaeiginleika, eins og tengla og feitletrun, undirstrikun og skáletrun texta. Sumum af þessum eiginleikum er hægt að hnekkja með síðuþema sem er beitt á eininguna. |
| Tengill          | Tenglatexti, vefslóð tengils, ARIA-merki (Accessible Rich Internet Applications) og **Opnaðu hlekk í nýjum flipa** | Einingar styðja einn eða fleiri „kalla til aðgerða“ tengla. Ef tengli er bætt við þarf tenglatexta, vefslóð og ARIA-merki. ARIA-merki ættu að vera lýsandi til að uppfylla kröfur um aðgengi. Hægt er að stilla tengla þannig að þeir séu opnaðir á nýjum flipa. |
| Reitartengill     | Setja tengil á texta, vefslóð, Aria-merki og valið **Opna tengil í nýjum flipa** | Þessi eiginleiki er notaður til að skilgreina „kalla til aðgerða“ tengil. Ef tengli er bætt við þarf tenglatexta, vefslóð og ARIA-merki. ARIA-merki ættu að vera lýsandi til að uppfylla kröfur um aðgengi. Hægt er að stilla tengla þannig að þeir séu opnaðir á nýjum flipa.|
| Tákn          | Mynd | Auk myndar af vöru eða flokki er hægt að bæta við tákni. Táknið mun birtast fyrir ofan myndina af vöru eða flokki. |

## <a name="add-a-tile-list-module-to-a-new-page"></a>Bæta reitalistaeiningu við nýja síðu

Fylgdu þessum skrefum til að bæta reitalistaeiningu við nýja síðu og stilla nauðsynlega eiginleika.

1. Farðu í **Sniðmát** og opnaðu markaðssetningarsniðmátið fyrir heimasíðu vefsvæðisins (eða búðu til nýtt sniðmát markaðssetningar).
1. Í **Aðal** rauf sjálfgefna síðunnar, veldu sporbaug (**...**), og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu **Flísalisti** mát og veldu síðan **Allt í lagi**.
1. Veldu **Vista**, síðan **Ljúka við breytingar** til að skila sniðmáti og veldu síðan **Birta** til að birta það.
1. Farðu í **Síður** og opnaðu heimasíðu vefsvæðisins (eða búðu til nýja heimasíðu með sniðmáti markaðssetningar).
1. Í **Aðal** rauf sjálfgefna síðunnar, veldu sporbaughnappinn (**...**), og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu **Flísalisti** mát og veldu síðan **Allt í lagi**.
1. Í eiginleikaglugga reitalistaeiningar skal bæta við fyrirsögn.
1. Í **Flísalisti** rauf, veldu sporbaughnappinn (**...**), og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu **Flísaeining** mát og veldu síðan **Allt í lagi**.
1. Í eiginleikaglugga reitaeiningar skal bæta við mynd, fyrirsögn og mynd af tákni.
1. Bættu við og stilltu fleiri reitaeiningar eins og þörf krefur.
1. Veldu **Vista** og veldu síðan **Forskoðun** til að forskoða síðuna.
1. Veldu **Ljúka við breytingar** til að athuga með sniðmátið og veldu síðan **Birta** til að birta það.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit einingasafns](starter-kit-overview.md)

[Þema Adventure Works](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
