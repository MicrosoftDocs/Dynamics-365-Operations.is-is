---
title: Virk myndeining
description: Þetta efnisatriði fjallar um virkar myndeiningar og útskýrir hvernig á að bæta þeim við síður svæða í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 6cc2f9bafcdd17ac33d5591b8c21f3354d95d92e
ms.sourcegitcommit: 7e976059118938b0089e40bef948029a8c088b38
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/09/2021
ms.locfileid: "6479476"
---
# <a name="active-image-module"></a>Virk myndeining

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Þetta efnisatriði fjallar um virkar myndeiningar og útskýrir hvernig á að bæta þeim við síður svæða í Microsoft Dynamics 365 Commerce.

Hægt er að nota virka myndeiningu til að fella vörumerki inn í mynd. Notendur rafrænna viðskiptasvæða geta síðan haldið músarbendlinum yfir merkin til að forskoða vörur sem sýndar eru á myndinni. Forskoðanirnar eru sýndar í sprettigluggum. Með því að velja sprettiglugga forskoðunar geta notendur farið beint á upplýsingasíðu vörunnar (PDP) fyrir samsvarandi vöru.

Merkin eru skilgreind með því að nota X og Y hnit á myndinni. Sérhver merktur punktur ætti að vera stilltur með vörukenni vörunnar sem er sýnd á myndinni.

Eftirfarandi mynd sýnir dæmi um sprettiglugga forskoðunar á hetjumynd á heimasíðu Adventure Works.

![Dæmi um sprettiglugga forskoðunar í virkri myndeiningu](./media/Active_image.PNG)

> [!IMPORTANT]
> - Virka myndeiningin er í boði frá og með Dynamics 365 Commerce útgáfu 10.0.20.
> - Virka myndeiningin er sýnd í þema Adventure Works.

## <a name="active-image-module-properties"></a>Eiginleikar virkrar myndeiningar

| Nafn eiginleika      | Gildi | lýsing |
|--------------------|--------|-------------|
| Mynd              | Myndaskrá | Nota má mynd til að sýna eina eða fleiri vörur. Hægt er að hlaða mynd inn í miðlasafnið í vefsmið Commerce eða nota mynd sem er til staðar. |
| Breidd              | Fjöldi pixla | Þessi eiginleiki skilgreinir breidd myndar. Virku hnitin eru reiknuð út samkvæmt breidd myndar.|
| Virk hnit | X og Y hnit og vörunúmer | Sérhvert myndafylki samanstendur af X og Y hnitum og vörunúmeri.|
| Haus            | Texti og merki fyrirsagnar (**H1**, **H2**, **H3**, **H4**, **H5** eða **H6**) | Sjálfgefið er að fyrirsagnarmerkið **H2** er notað fyrir fyrirsögnina, en breyta má merkinu til að uppfylla kröfur um aðgengi. |
| Efnisgrein          | Texti efnisgreinar | Einingin styður málsgreinatexta með ríku textasniði. Stuðningur er við nokkra grunntextaeiginleika, eins og tengla og feitletrun, undirstrikun og skáletrun texta. Sumum af þessum eiginleikum er hægt að hnekkja með síðuþema sem er beitt á eininguna. |
| Tengill               | Tenglatexti, vefslóð tengils, ARIA-merki (Accessible Rich Internet Applications) og valið **Opnaðu hlekk í nýjum flipa** | Einingin styður einn eða fleiri „kalla til aðgerða“ tengla. Ef tengli er bætt við þarf tenglatexta, vefslóð og ARIA-merki. ARIA-merki ættu að vera lýsandi til að uppfylla kröfur um aðgengi. Hægt er að stilla tengla þannig að þeir séu opnaðir á nýjum flipa. |
| Texti efnis           | Fyrirsögn, texti og tenglar | Hægt er að bæta við öðru samhengi fyrir myndina, svo sem nafni höfundar eða hönnuðar eða tenglum á persónuleg blogg.|
| Aðalefni texta         | **Ljóst** eða **Dökkt** | Þessi eiginleiki gerir notanda kleift að stilla textann á ljósan eða dökkan út frá bakgrunnsmyndinni. Hann er í boði sem þemaviðbót við þema Adventure Works. |

## <a name="add-an-active-image-module-to-a-new-page"></a>Bæta virkri myndeiningu við nýja síðu

Til að bæta virkri myndeiningu við nýja síðu og stilla nauðsynlega eiginleika skal fylgja þessum skrefum.

1. Farðu í **Sniðmát** og opnaðu markaðssetningarsniðmátið fyrir heimasíðu vefsvæðisins (eða búðu til nýtt sniðmát markaðssetningar).
1. Í hólfinu **Aðalsvæði** á Sjálfgefin síða skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.
1. Í glugganum **Bæta við einingu** skal velja eininguna **Virk mynd** og síðan velja **Í lagi**.
1. Veldu **Vista**, síðan **Ljúka við breytingar** til að skila sniðmáti og veldu síðan **Birta** til að birta það.
1. Farðu í **Síður** og opnaðu heimasíðu vefsvæðisins (eða búðu til nýja heimasíðu með sniðmáti markaðssetningar).
1. Í hólfinu **Aðal** á sjálfgefnu síðunni velurðu úrfellingarhnappinn (**...**) og velur síðan **Bæta við einingu**.
1. Í glugganum **Bæta við einingu** skal velja eininguna **Virk mynd** og síðan velja **Í lagi**.
1. Í eiginleikaglugga virkrar myndeiningar skal bæta við mynd og stilla breidd myndarammans á stærð myndarinnar.
1. Stilltu X og Y hnitin og bættu við viðeigandi vörunúmeri.
1. Bættu við og stilltu fleiri virkar myndeiningar eins og þörf krefur.
1. Veldu **Vista** og veldu síðan **Forskoðun** til að forskoða síðuna.
1. Veldu **Ljúka við breytingar** til að athuga með sniðmátið og veldu síðan **Birta** til að birta það.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit einingasafns](starter-kit-overview.md)

[Þema Adventure Works](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
