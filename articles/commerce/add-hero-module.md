---
title: Eining fyrir bálk með efni
description: Þessi grein fjallar um efnisblokkareiningar og lýsir því hvernig á að bæta þeim við vefsíður í Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 253600e48bab2ecfb1e744e15d2fe36fa1ec6765
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870611"
---
# <a name="content-block-module"></a>Eining fyrir bálk með efni

[!include [banner](includes/banner.md)]

Þessi grein fjallar um efnisblokkareiningar og lýsir því hvernig á að bæta þeim við vefsíður í Microsoft Dynamics 365 Commerce.

Innihaldsbálkseining er notuð til að markaðssetja vörur eða kynningar með blöndu af myndum og texta. Til dæmis getur smásali bætt innihaldsbálkseiningu á heimasíðu svæðis fyrir rafræn viðskipti til að kynna nýja vöru og vekja athygli viðskiptavina.

Innihaldsbálkseining er knúin áfram af gögnum frá efnisstýringarkerfinu (CMS). Þetta er sjálfstæð eining sem er ekki háð öðrum einingum á síðunni. Hægt er að setja innihaldsbálkseiningar á hvaða síðu sem er þar sem smásali vill markaðssetja eða auglýsa eitthvað (til dæmis vörur, útsölu eða eiginleika).

## <a name="examples-of-content-block-module-in-e-commerce"></a>Dæmi um innihaldsbálkseiningu í rafrænum viðskiptum

- Hægt er að nota innihaldsbálkseiningu á heimasíðu svæðis fyrir rafræn viðskipti til að varpa ljósi á kynningar og nýjar vörur.
- Hægt er að nota innihaldsbálkseiningu á upplýsingasíðu vöru til að sýna upplýsingar um vöru.
- Hægt er að setja margar innihaldsbálkseiningar í myndaræmueiningu til að varpa ljósi á margar vörur eða kynningar.

## <a name="content-block-modules-and-themes"></a>Innihaldsbálkseiningar og -þemu

Innihaldsbálkseiningar geta stutt ýmis útlit og stíla út frá þema. Til dæmis styður Fabrikam þemað þrjú skipulagstilbrigði af innihaldsbálkseiningum: hetja, eiginleiki og reitur. Hetjuuppsetningin sýnir mynd á bakgrunni með textayfirlagi. Skipulag eiginleika sýnir mynd og texta hlið við hlið. Uppsetning reitanna gerir kleift að hafa margvíslega efnisbálka á reitasniði.

Að auki getur þemað afhjúpað mismunandi eiginleika fyrir hvert skipulag. Þemahönnuður getur smíðað fleiri skipulag með fleiri stílum með því að nota innihaldsbálkaeininguna.

Eftirfarandi mynd sýnir dæmi um innihaldsbálkseiningu með hetjuuppsetningu.

![Dæmi um hetjueiningu.](./media/Hero.PNG)

Eftirfarandi mynd sýnir dæmi um innihaldsbálkseiningu með eiginleikauppsetningu.

![Dæmi um eiginleikaeiningar.](./media/Feature.PNG)

## <a name="content-block-module-properties"></a>Eiginleikar innihaldsbálks

| Nafn eiginleika  | Gildi | lýsing |
|----------------|--------|-------------|
| Mynd          | Myndaskrá | Hægt er að nota mynd til að sýna vöruna eða auglýsa. Hægt er að hlaða mynd inn í myndasafnið eða nota núverandi mynd. |
| Fyrirsögn        | Texti og merki fyrirsagnar (**H1**, **H2**, **H3**, **H4**, **H5** eða **H6**) | Sérhver hetjueining getur haft fyrirsögn. Sjálfgefið er að fyrirsagnarmerkið **H2** er notað fyrir fyrirsögnina. Hins vegar er hægt að breyta merkinu til að uppfylla kröfur um aðgengi. |
| Efnisgrein      | Texti efnisgreinar | Hetjueiningar styðja málsgreinatexta með ríku textasniði. Stuðningur er við nokkra grunntextaeiginleika, eins og feitletrun, undirstrikun og skáletrun texta og tengla. Sumum af þessum eiginleikum er hægt að hnekkja með síðuþema sem er beitt á eininguna. |
| Tengill           | Tenglatexti, vefslóð tengils, ARIA-merki (Accessible Rich Internet Applications) og **Opnaðu hlekk í nýjum flipa** | Hetjueiningar styðja einn eða fleiri „kalla til aðgerða“ tengla. Ef tengli er bætt við þarf tenglatexta, vefslóð og ARIA-merki. ARIA-merki ættu að vera lýsandi til að uppfylla kröfur um aðgengi. Hægt er að stilla tengla þannig að þeir séu opnaðir á nýjum flipa. |

## <a name="content-block-module-properties-exposed-by-the-fabrikam-theme"></a>Eiginleikar innihaldsbálkseininga útsettir fyrir Fabrikam-þema 

| Nafn eiginleika  | Gildi | Lýsing |
|----------------|--------|-------------|
| Staðsetning texta | **Hægri**, **vinstri**, **miðja** | Þessi eiginleiki skilgreinir staðsetningu textans á myndinni. Hann á aðeins við um hetjuuppsetninguna. |
| Aðalefni texta     | **Ljóst** eða **Dökkt** | Hægt er að skilgreina litasamsetningu fyrir textann, byggt á bakgrunnsmyndinni. Til dæmis, ef myndin er með dökkan bakgrunn, er hægt að beita léttu þema til að gera textann sýnilegri og til að mæta andstæða litastigshlutfalla í aðgengisskyni. Hann á aðeins við um hetjuuppsetninguna.|
| Staðsetning myndar       | **Vintri**,  **hægri** | Þessi eiginleiki tilgreinir hvort myndin skuli vera til vinstri eða hægri í textanum. Hann á aðeins við um eiginleikauppsetninguna.  |

## <a name="add-a-content-block-module-to-a-new-page"></a>Bæta við innihaldsbálkseiningu á nýja síðu

Fylgdu þessum skrefum til að bæta hetjueiningu við nýja síðu og stilla nauðsynlega eiginleika.

1. Farðu í **Sniðmát** og búðu til síðusniðmát sem heitir **Sniðmát útilokunar á efni**.
1. Í hólfinu **Aðal** á sjálfgefnu síðunni bætirðu við hetjueiningu.
1. Veldu **Vista**, síðan **Ljúka við breytingar** til að skila sniðmáti og veldu síðan **Birta** til að birta það.
1. Notaðu sniðmátið fyrir aðalsíðuna sem þú varst að búa til, til að búa til síðu sem heitir **Síða útilokunar á efni**.
1. Í **Aðal** rauf sjálfgefna síðunnar, veldu sporbaughnappinn (**...**), og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu hetjueininguna og veldu síðan **Allt í lagi**.
1. Veldu innihaldsbálkseininguna í útlínutrénu til vinstri.
1. Í eiginleikaglugganum til hægri velurðu **Bæta við mynd**. Veldu þá annaðhvort núverandi mynd eða hladdu upp nýrri mynd.
1. Veldu **Fyrirsögn**.
1. Í valmyndinni **Fyrirsögn** bætirðu við fyrirsagnartexta, velur hausstig og velur síðan **Í lagi**.
1. Undir **Sniðinn texti** bætirðu við texta eftir þörfum.
1. Veldu **Bæta við tengli**.
1. Í valmyndinni **Tengill** bætirðu við texta, slóð og ARIA-merki fyrir tengilinn og velur síðan **Í lagi**.
1. Veldu skipulagið **Hetja**.
1. Veldu **Vista** og veldu síðan **Forskoðun** til að forskoða síðuna.
1. Veldu **Ljúka við breytingar** til að athuga með sniðmátið og veldu síðan **Birta** til að birta það. 

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit einingasafns](starter-kit-overview.md)

[Tilboðsborðaeining](add-alert.md)

[Myndaræmueining](add-carousel.md)

[Textabálkseining](add-content-rich-block.md)

[Myndspilaraeining](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
