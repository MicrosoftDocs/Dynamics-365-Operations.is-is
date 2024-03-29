---
title: Skoða og flytja út svæðalýsingar
description: Þessi grein er lýst hvernig á að skoða lýsingar á svæðum og hvernig á að nota síðuna lýsingar Svæðið til að flytja út lýsingar.
author: twheeloc
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 11534
ms.assetid: e2795f51-a8a7-4c74-bdb9-b1be93bdd358
ms.search.form: FieldDescriptions
ms.openlocfilehash: d2d59796b312d50d69bf7722b605c159a933a283
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292367"
---
# <a name="view-and-export-field-descriptions"></a>Skoða og flytja út svæðalýsingar

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Þessi grein er lýst hvernig á að skoða lýsingar á svæðum og hvernig á að nota síðuna lýsingar Svæðið til að flytja út lýsingar.

Sumir af flóknari reitunum eru með lýsingar. Lýsingar á þessum birtist þegar þú músabendil yfir svæði. Í **Lýsingar svæðis** síðunni geturðu skoðað og flutt út lýsingar.

Ekki eru allar síður með lýsingum. Við viljum aðeins veita lýsingu fyrir flóknari svæði og ekki þau þar sem notkun svæðisins er augljós. Þess vegna sumar síður hafa engar lýsingum sumar síður hafa nokkrar lýsingar og sumar flóknari síðum, eins og margar síður færibreytur hafa margar lýsingar.

Ef þú hefur aðgang að þróunarumhverfinu geturðu bæta við eigin reitalýsingum og sérsniðið eldri lýsingar. Til dæmis er hægt að bæta upplýsingum bundin tilteknu fyrirtæki í lýsing svæðis. Nánari upplýsingar eru í svæðahjálpinni í [Sérstilla lýsingar á reit](../../dev-itpro/user-interface/customize-field-help.md).

## <a name="see-field-descriptions-in-the-user-interface"></a>Sjá svæðislýsingar í notendaviðmótinu

Hægt er að skoða lýsingar á svæðum með halda yfir á svæðið. Sé engin lýsing tiltæk, er hægt að sjá heiti svæðis þegar þú setur músabendil yfir svæðið.

> [!NOTE]
> Í Dynamics AX 7.0 (febrúar 2016) er aðeins hægt að skoða svæðislýsingar á síðunni **Svæðislýsingar**.

Eftirfarandi skýringarmynd sýnir lýsingu sem birtist þegar þú setur músabendil yfir **Læsa vörum á meðan á talningu stendur** svæði.

[![Dæmi um svæðislýsingu.](./media/field-description.png)](./media/field-description.png)

## <a name="use-the-field-descriptions-page-to-view-and-export-field-help"></a>Notið Svæðið lýsingar síðu til þess að skoða og flytja út svæðið hjálp

Í **Lýsingar svæðis** síðunni geturðu skoðað og flutt út reitalýsingar. Hægt er að finna lýsingar sem eru tiltækar fyrir eina síðu í einu.

### <a name="view-the-descriptions-for-a-page"></a>Skoða lýsingar á síðu

Til að skoða lýsingar fyrir síðu skaltu fylgja þessu skrefi.

- Í svæðið **velja síðu** skal færa inn heiti síðunnar. Einnig er hægt að smella á örina til að opna lista yfir allar síður, og síðan flett eða sía lista.

Hægt er að nota heiti síðunnar sem er sýnt í Notendaviðmóti, (til dæmis **Viðskiptavini**)eða kóðanafn (AOT-heiti) sem er tiltæk með því að hægrismella á síðu, (til dæmis **CustTable**).

Upplýsingar um mismunandi aðferðir til að sía lista yfir síður, sjá hlutann „Leit fyrir síðu" síðar í þessari grein.

Ef stilltur er **Hafa svæði án lýsingar** valkostur á **Já** birtast öll svæði á síðunni, óháð því hvort þeir hafa lýsing svæðis.

### <a name="export-the-descriptions-for-a-page"></a>Flytja út lýsingar á síðu

Til að flytja út lýsingar fyrir síðu skaltu fylgja þessum skrefum.

1. Velja síðu á **Velja síðu** reitnum.
2. Smellið á **Opna í Microsoft Office** hnappinn í hægra efra horninu og smellið á **FieldDescriptionTmp**.

### <a name="searching-for-a-page"></a>Leita að síðu

Nokkrar leiðir eru til að leita að síðu í reitnum **Velja síðu**. Í mörgum tilvikum þarf að smella á örina í **Velja síðu** reitnum til að opna fellilistinn og velja úr síaða lista yfir síður.

- Færið inn hluta úr nafni, þá svo skal opna fellilistann til að velja úr lista yfir síaðar síður.
- Opna fellilistinn og smella á annaðhvort titilinn **Síðuheiti** efst á listanum eða **AOT-heiti síðu** titill. Þetta opnar svarglugga þar sem hægt er að nota ítarlega síunarvalkosti, eins og **Síðuheiti hefst á**.
- Sláðu inn fullt nafn síðunanr. Þegar þessi valkostur er notaður er best að opna fellilistinn og sjá hvað annað er á listanum, jafnvel þótt lýsingum eru sýndar.

    - Ef einn nákvæm samsvörun heiti er til staðar birtist lýsing fyrir þá síðu.
    - Ef fleiri en einn nákvæm samsvörun er engin lýsingar sýndar. Þú verður að Opna í fellilistanum og veljið síðan sem óskað er.
    - Ef heiti sem slegið er inn er hluta á nafni á aðra síðu sérðu lýsingu á síðunni. Hins vegar ef á fellilistann er opnuð, er að sjá aðrar síður sem innihalda nafninu.

Til dæmis eru engar lýsingar sýndar þegar fært er inn **Talning** í svæðið **Velja síðu**. Ef opnað er á fellilistanum sést að það eru tvær síður með heitið **"Talning"** auk nokkrum síða sem innihalda orðið "Talning“ í nafni. Ef valin er síða með AOT-heiti **"InventJournalCount"** birtast svæðislýsingar fyrir þá síðu. Hins vegar ef fellilistinn er opnuð aftur, sést að listinn inniheldur allar síður sem hafa "InventJournalCount" sem hluti af þeirra AOT-heiti.

## <a name="troubleshooting"></a>Úrræðaleit

Eftirfarandi kaflar veita upplýsingar við úrræðaleit vegna vandamála sem koma upp við notkun á svæðislýsingum.

### <a name="i-cant-find-a-field-description"></a>Ég finn ekki svæðislýsingu

Við höfum verið að bæta við lýsingar fyrir flóknari svæði. Ef þú þarft hjálp vegna tiltekins svæðis, skaltu láta okkur vita með því að bæta við athugasemd við þessa grein.

### <a name="the-field-description-isnt-helpful"></a>Svæðislýsingin er ekki gagnleg

Láttu okkur vita með því að bæta við athugasemd um þessa grein. Ef hægt er, lýsa viðbótarupplýsingar sem þarf.

### <a name="i-cant-find-a-field-on-the-field-descriptions-page"></a>Ég finnur ekki svæðið á síðunni Svæði lýsingar

Til að sýna alla reiti á síðu skal stilla valkostinn **Hafa með reiti án lýsingar** á **Já.** Smellið á **Velja síðu** svæði til að staðfesta er valin rétt síðu. Ef heiti sem fært er inn er hluti af annarri svæðisheiti gæti hafa verið valdar síðu sem hefur lengra heiti.

### <a name="i-cant-find-a-page-on-the-field-descriptions-page"></a>Ég finnur ekki svæðið á síðunni Svæði lýsingar

Upplýsingar um mismunandi aðferðir til að finna síður, sjá hlutann „Leit fyrir síðu" fyrr í þessari grein. Ef nákvæmt heiti síðunnar hefur verið fært inn, kunna lýsingar á svæðum ekki að vera sýndar ef er meira en eina síða er með sama heiti. Smella á örina í kassanum **Velja síðu** til að opna síaða lista yfir tiltækar síður.

## <a name="additional-resources"></a>Frekari upplýsingar

[Sérstilla lýsingar á reit](../../dev-itpro/user-interface/customize-field-help.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
