---
title: Ástæðukóðar fyrir birgðatalningu
description: Í þessu efnisatriði er því lýst hvernig eigi að setja upp og innleiða ástæðukóðum fyrir talningarverk.
author: Mirzaab
manager: tfehr
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCountingReasonCodePolicy, InventCountingReasonCode
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: d72b171bfe149b25f5055d5bebef85b49e952295
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5228490"
---
# <a name="reason-codes-for-inventory-counting"></a>Ástæðukóðar fyrir birgðatalningu

[!include [banner](../includes/banner.md)]

Ástæðukóðar gera þér kleift að greina niðurstöður talningarferlis og hvers kyns misræmi sem á sér stað í því ferli. Hægt er að tilgreina ástæðuna fyrir því að gera talningu, t.d. brotið bretti eða lagerleiðrétting sem byggist á sýnishornum birgða.

## <a name="recommendation"></a>Ráðleggingar

Áður en kerfið er sett upp er mælt með því að skilgreina áætlun til að vinna með ástæðukóðum. Reyndu til dæmis að svara eftirfarandi spurningum:

- Eiga ástæðukóðar að vera áskildir í vöruhúsum?
- Eiga ástæðukóðar að vera áskildir eða valfrjálsir á sumum vörum?
- Hversu marga ástæðukóða þarftu á að halda?
- Hvernig eiga notendur strikamerkjaskanna að nota ástæðukóða? Eiga ástæðukóðarnir að vera forvaldir, áskildir eða óbreytanlegir?
- Þurfa starfskraftar í vöruhúsi öðruvísi tilhögun á ástæðukóðum fyrir farsímaskanna? Ef svarið er já, er hægt að búa til fleiri valmyndaratriði og úthluta þeim á mismunandi fólk.

## <a name="where-reason-codes-apply"></a>Þar sem ástæðukóðar eiga við

Hægt er að búa til margar reglur ástæðukóða og hver regla ástæðukóða getur haft tvær reglur fyrir ástæðukóða talningar. Reglur ástæðukóða talningar er hægt að nota á stigi vöruhúss eða stigi vöru.

## <a name="set-up-reason-code-policies"></a>Setja upp reglur ástæðukóða

1. Veldu **Birgðastjórnun** \> **Uppsetning** \> **Birgðir** \> **Reglur ástæðukóða talningar** og búðu til nýja reglu ástæðukóða.
2. Í reitnum **Gerð ástæðukóða talningar** skal velja annaðhvort **Áskilið** eða **Valfrjálst** til að tilgreina hvort val á ástæðukóða eigi að vera valfrjáls eða áskilin aðgerð í einni af eftirfarandi talningarbókum:

    - Regluleg talning (fartæki)
    - Stundartalning (fartæki)
    - Þröskuldstalning (fartæki)
    - Leiðrétting inn (fartæki)
    - Leiðrétting út (fartæki)
    - Talningarbók (þungbiðlari)

Einnig er hægt að setja upp ástæðukóða fyrir einstök vöruhús og afurðir. Uppsetning ástæðukóða fyrir afurðir getur hunsað uppsetningu fyrir vöruhús.

## <a name="mandatory-reason-codes"></a>Áskildir ástæðukóðar

Ef færibreytan **Áskilið** er stillt í skilgreiningu ástæðukóða fyrir vöruhús eða vörur, er ekki hægt að ljúka og loka talningarbókinni fyrr en ástæðukóði hefur verið útvegaður.

### <a name="set-up-reason-codes-for-warehouses"></a>Setja upp ástæðukóða fyrir vöruhús

1. Veldu **Birgðastjórnun** \> **Uppsetning** \> **Birgðasundurliðun** \> **Vöruhús**.
2. Í flipanum **Vöruhús**, í reitnum **Regla ástæðukóða talningar** skal velja einn af eftirfarandi valkostum:

    - **Autt** - Færibreyta sem er sett upp fyrir vöru er notuð til að ákvarða hvort talningarbækur séu áskildar fyrir afurðina.
    - **Áskilið** - Ástæðukóða er alltaf krafist fyrir talningarbækur vöruhúss.
    - **Valfrjálst** - Ástæðukóða er ekki krafist fyrir talningarbækur vöruhúss.

### <a name="set-up-reason-codes-for-products"></a>Setja upp ástæðukóða fyrir afurðir

1. Veldu **Upplýsingastjórnun afurða** \> **Afurðir** \> **Útgefnar afurðir**.
2. Á flipanum **Afurðir** skal velja **Regla ástæðukóða talningar** og síðan velja einn af eftirfarandi valkostum:

    - **Autt** - Færibreyta sem er sett upp fyrir vöruhús er notuð til að ákvarða hvort talningarbækur séu áskildar fyrir afurðina.
    - **Áskilið** - Ástæðukóða er alltaf krafist fyrir talningarbækur afurðar. Þessi stilling hnekkir öllum stillingum ástæðukóða á stigi vöruhúss.
    - **Valfrjálst** - Ástæðukóða er ekki krafist fyrir talningarbækur afurðar. Þessi stilling hnekkir öllum stillingum ástæðukóða á stigi vöruhúss.

### <a name="use-reason-codes-in-counting-journals"></a>Nota ástæðukóða í talningarbókum

Í talningarbókum er hægt að bæta við ástæðukóðum fyrir talningar af eftirfarandi gerðum:

- Regluleg talning
- Stundartalning
- Þröskuldstalning
- Leiðrétting inn
- Leiðrétting út

Ástæðukóðum er bætt við færslubókarlínur í talningarbókum af gerðinni **Talningarbók**.

1. Veldu **Birgðastjórnun** \> **Færslubókarfærslur** \> **Vörutalning** \> **Talning**.
2. Í línuupplýsingum talningarbókar, í reitnum **Ástæðukóði talningar** skal velja valkost.

### <a name="view-the-counting-history-as-its-recorded-by-reason-codes"></a>Skoðaðu talningarferilinn eins og hann er skráður af ástæðukóðum

- Veldu **Birgðastjórnun** \> **Fyrirspurnir og skýrslur** \> **Talningarferill** og síðan í reitnum **Ástæðukóði talningar** skaltu skoða talningarferilinn sem hefur verið skráður í gegnum ástæðukóða.

### <a name="use-a-reason-code-for-a-quantity-adjustment"></a>Notaðu ástæðukóða fyrir magnleiðréttingu

1. Á síðunni **Lagerbirgðir** skal velja **Leiðrétta magn**. Hægt er að opna síðuna **Lagerbirgðir** á nokkra vegu. Veldu til dæmis **Birgðastjórnun** \> **Fyrirspurnir og skýrslur** \> **Lagerbirgðir**.
2. Veldu **Leiðrétta magn** og síðan í reitnum **Ástæðukóði talningar** skal velja ástæðukóða.

### <a name="configure-reason-codes-for-mobile-device-menu-items"></a>Skilgreina ástæðukóða fyrir valmyndaratriði fartækis

Hægt er að skilgreina ástæðukóða fyrir hvaða talningargerð sem er í valmyndaratriði fartækis. Uppsetning valmyndaratriðis fartækis inniheldur eftirfarandi upplýsingar:

- Hvort ástæðukóðinn sjáist fyrir starfskraft fartækis meðan á talningu stendur.
- Sjálfgefni ástæðukóðinn sem er sýndur í valmyndaratriði fartækis.
- Hvort notandi geti breytt ástæðukóða.

### <a name="set-up-reason-codes-on-a-mobile-device"></a>Setja upp ástæðukóða á fartæki

1. Veldu **Vöruhúsakerfi** \> **Uppsetning** \> **Fartæki** \> **Valmyndaratriði fartækis**.
2. Í flipanum **Regluleg talning** skal velja **Regluleg talning**.
3. Í reitnum **Sjálfgefinn ástæðukóði talningar** skal stilla sjálfgefinn ástæðukóða sem á að skrá þegar talning er gerð með því að nota valmyndaratriði fartækis.
4. Í reitnum **Birta ástæðukóða talningar** skal velja **Lína** til að sýna ástæðukóða eftir að hvert frávik er skráð. Að öðrum kosti skal velja **Fela** ef ekki á að sýna ástæðukóða.
5. Stilltu valkostinn **Breyta ástæðukóða talningar** á annaðhvort **Já** eða **Nei**. Ef þú stillir valkostinn á **Já** getur starfskraftur breytt ástæðukóða þegar hann er sýndur á fartækinu meðan á talningu stendur.

> [!NOTE]
> Hægt er að virkja hnappinn **Regluleg talning** á valmyndaratriði hvaða fartækis sem er þar sem talning getur farið fram. Dæmi um það eru valmyndaratriðin fyrir stundartalningar, notendastýrð verk og kerfisstýrð verk.

## <a name="cycle-count-approvals"></a>Samþykki reglulegrar talningar

Áður en talning er samþykkt getur notandi breytt ástæðukóðanum sem tengist talningunni. Þegar talning er samþykkt er ástæðukóði sleginn inn í línu talningarbókar.

### <a name="modify-cycle-count-approvals"></a>Breyta samþykki reglulegrar talningar

1. Veldu **Vöruhúsakerfi** \> **Regluleg talning** \> **Verk reglulegrar talningar bíður yfirferðar**.
2. Veldu **Regluleg talning** og síðan í reitnum **Ástæðukóði** skal velja nýjan ástæðukóða.

### <a name="modify-the-mobile-device-menu-item-for-adjustment-in-and-adjustment-out"></a>Breyttu valmyndaratriði fartækis fyrir Leiðréttingu inn og Leiðréttingu út

1. Veldu **Vöruhúsakerfi** \> **Uppsetning** \> **Fartæki** \> **Valmyndaratriði fartækis** og veldu síðan **Leiðrétting inn og út**.
2. Stilltu valkostinn **Nota núverandi verk** á **Nei**.
3. Í reitnum **Ferli verkstofnunar** skal velja **Leiðrétting inn**.

Eftirfarandi reitum verður bætt við valmyndaratriði fartækis þegar **Leiðrétting inn** eða **Leiðrétting út** er valin á meðan ferli verkstofnunar stendur yfir:

- Sjálfgefinn ástæðukóði talningar
- Birta ástæðukóða talningar
- Breyta ástæðukóða talningar


[!INCLUDE[footer-include](../../includes/footer-banner.md)]