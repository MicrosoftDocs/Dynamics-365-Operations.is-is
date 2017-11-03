---
title: "Útreikningsaðferðir virðisaukaskatts í reitnum Uppruni"
description: "Þessi grein útskýrir valkosti á svæðinu Uppruni á síðunni vsk-kóðar og hvernig virðisaukaskattur er reiknaður á grundvelli þeirra valkosta sem ákveðnir eru fyrir virðisaukaskattskóða."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f5683b8b3e5457a05e5039876eed40357ae84e4b
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="sales-tax-calculation-methods-in-the-origin-field"></a>Útreikningsaðferðir virðisaukaskatts í reitnum Uppruni

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


Þessi grein útskýrir valkosti á svæðinu Uppruni á síðunni vsk-kóðar og hvernig virðisaukaskattur er reiknaður á grundvelli þeirra valkosta sem ákveðnir eru fyrir virðisaukaskattskóða.

Fyrir hvern VSK-kóða sem stofnaður er á síðunni VSK-kóðar þarf að velja útreikningsaðferð sem notuð er á upphæð VSK-stofns í reitnum Uppruni.

## <a name="percentage-of-net-amount"></a>Prósenta af nettóupphæð
Prósenta af útreikningsaðferð nettóupphæðar er sjálfgefna gildið í reitnum Uppruna. Virðisaukaskatturinn er reiknaður sem prósenta af innkaupa- eða söluupphæð, án annarra virðisaukaskatta.
### <a name="example"></a>Dæmi

Skatthlutfallið er 25%. Reikningslínan sýnir magn 10 vara sem kosta 1,00 hver og viðskiptavinurinn fær 10% línuafslátt. Nettóupphæð: (10 x 1,00) -10% = 9,00 VSK: 9,00 x 25% = Heildarupphæð 2,25: 9,00 + 2,25 = 11,25

## <a name="percentage-of-gross-amount"></a> Prósenta af brúttó upphæð
Ef valin er aðferðin Prósenta af brúttóupphæð er VSK reiknaður sem prósenta af brúttósöluupphæð. Brúttóupphæð er nettólínuupphæð plús allir skattar og gjöld línunnar, nema einn skattur með Uppruna = Prósenta af brúttóupphæð.
### <a name="example"></a>Dæmi

Skattyfirvöld hafa lagt sérstök gjöld á vöru. Upphæð gjaldanna er bætt við nettóupphæðina áður en virðisaukaskattur er reiknaður út. Eftirfarandi VSK-kóðar eru gefnir:
-   Gjald 1 = 10%, notar útreikningsaðferð fyrir prósentu af nettóupphæð
-   Gjald 2 = 20%, notar útreikningsaðferð fyrir prósentu af nettóupphæð
-   VSK = 25%, notar útreikningsaðferð fyrir prósentu af brúttóupphæð

Ef nettóupphæðin er 10,00 þá er Gjald 1 1,00 (10,00 x 10%) og Gjald 2 2,00 ( 10,00 x 20%). Upphæðirnar yrðu eftirfarandi: Brúttóupphæð: Nettóupphæð + upphæð GJALD 1 + upphæð GJALD 2 (10,00 + 1,00 + 2,00) = 13,00 VSK = 13,00 x 25% = 3,25 Samtals GJÖLD og VSK: 1,00 + 2,00 + 3,25 = 6,25 Heildarupphæð: 10,00 + 6,25 = 16,25
| **Ábending**                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Aðeins er hægt að nota einn VSK-kóða með Uppruna = Prósenta af brúttóupphæð fyrir færslu. Ef fleiri en einn slíkur skattkóði er ákvarðaður fyrir færslu birtist villa um að ekki sé hægt að reikna út virðisaukaskatt. |

 
<a name="percentage-of-sales-tax"></a>Prósenta af VSK
-----------------------

Þegar Prósenta af virðisaukaskatti er valin í reitnum Uppruni er virðisaukaskattur reiknaður sem prósenta af virðisaukaskatti sem valinn er í reitnum VSK á VSK. Virðisaukaskattur sem er valinn í reitnum VSK á VSK er reiknaður fyrst. Seinni virðisaukaskatturinn er síðan reiknaður á grunni fyrri virðisaukaskattsins.
### <a name="example"></a>Dæmi

Eftirfarandi VSK-kóðar eru gefnir:
-   Gjald 1 = 10%, notar aðferð fyrir prósentu af nettóupphæð
-   GJALD 2 = 20%, notar aðferð prósentu af vsk, með Gjald 1 í reitnum VSK á VSK
-   VSK = 25%, notar aðferð fyrir prósentu af brúttóupphæð

Nettóupphæð: 10,00 GJALD 1: 10,00 x 10% = 1,00 GJALDI 2: 1,00 x 20% = 0.20 Brúttóupphæð: 10,00 + 1,00 + 0,20 = 11,20 VSK: 11,20 x 25% = 2.80 Samtals GJÖLD og VSK: 1,00 + 0,20 + 2,80 = 4,00 Heildarupphæð: 10,00 + 4,00 = 14,00
| **Ábending**                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Margstiga skattur í skattaútreikningum er ekki mögulegur. Ekki er hægt að reikna út skatt á grundvelli skatts sem þegar er reiknaður út frá öðrum skatti. Hægt er að reikna marga eins stigs skatta í skattkóðum í færslu. |

## <a name="amount-per-unit"></a> Upphæð á einingu
Þegar Upphæð á einingu í er valin í reitnum Uppruni er virðisaukaskattur reiknaður sem föst upphæð á einingu margfaldað með magninu sem fært er inn í línuna. Velja skal einingu í reitnum Eining. Upphæð á einingu er tilgreind á síðunni Gildi VSK-kóða.
### <a name="example"></a>Dæmi

Vsk-kóðinn er settur upp sem: 1,20 USD á hverja einingu = kassi Á sölureikningslínu 25 kassar af vöru eru seldir VSK er reiknaður sem 25 x 1,20 = 30,00
| **Ábending**                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ef færslan er færð inn í aðra einingu en einingu sem er tilgreind á VSK-kóða, umreiknast hún sjálfkrafa á grundvelli einingaumreikninga sem eru settir upp á síðunni Umreikningur eininga. |

###  <a name="amount-per-unit-additional-option"></a> Upphæð á einingu, viðbótarvalkostur

Á flipanum Útreikningur er hægt að velja hvort reiknaður skattur á upphæð á einingu er reiknaður út á undan öðrum vsk-kóða og bætt við nettóupphæðina áður en aðrir VSK-kóðar með Uppruna = Prósenta af nettóupphæð eru reiknaðir.

### <a name="examples"></a>Dæmi

Gerum ráð fyrir að við reiknum 2 skattkóða á færslu:

-   GJALD: Uppruni = Upphæð á einingu og virðisaukaskatt, gildi er stillt á 5,00 á einingu = stykki
-   VSK: Uppruni = eins og sýnt er í dæmunum hér að neðan, gildi er stillt á 25%

Við seljum 1 stykki af vöru á einingaverðinu 10,00
#### <a name="example-1"></a>Dæmi 1

VSK: Uppruni = Prósenta af brúttóupphæð aðferð Valkosturinn Reikna út á undan VSK hefur engin áhrif, þar sem VSK er reiknaður sem prósenta af brúttóupphæð. GJALD: 1 x 5,00 = 5,00 brúttóupphæð: 10,00 + 5,00 = 15,00 VSK: 15,00 x 25% = 3,75 Heildarupphæð virðisaukaskatts: 5,00 + 3,75 = 8,75 Heildarupphæð: 10,00 + 8,75 = 18,75

#### <a name="example-2"></a>Dæmi 2

VSK: Uppruni = Prósenta af nettóupphæð Valkosturinn Reikna út á undan VSK er ekki valinn fyrir útreikning á GJALDI. Nettóupphæð: 10,00 GJALD: 1 x 5,00 = 5,00 VSK: 10,00 x 25% = 2,50 Heildarupphæð virðisaukaskatts: 5,00 + 2,50 = 7,50 Heildarupphæð: 10,00 + 7,50 = 17,50

#### <a name="example-3"></a>Dæmi 3

VSK: Uppruni = Prósenta af nettóupphæð Valkosturinn Reikna út á undan VSK er ekki valinn fyrir útreikning á GJALDI. Nettóupphæð: 10,00 GJALD: 1 x 5,00 = 5,00 VSK: (10,00 + 5,00) x 25% = 3,75 Heildarupphæð virðisaukaskatts: 5,00 + 3,75 = 8,75 Heildarupphæð: 10,00 + 8,75 = 18,75

#### <a name="example-4"></a>Dæmi 4

Niðurstaðan úr dæmi 3 og dæmi 1 er sú sama, þar sem aðeins er um eitt gjald að ræða. Gefum okkur að greiða þurfi tvenns konar GJÖLD og aðeins önnur þeirra eru með í nettóupphæð fyrir útreikning vsk: GJALD 1: 5,00 með Upphæð á hverja einingu aðferð og reikna það Út áður en vsk-valkosturinn er valinn GJALDI 2: 2,50 með Upphæð á hverja einingu aðferð og reikna það Út áður en vsk-valkosturinn er ekki valinn vsk : 25%, með því að nota Prósentu af nettó upphæð nettóupphæð aðferð: 10,00 GJALD 1: 1 x 5,00 = 5,00 GJALD 2: 1 x 2,50 = 2,50 nettóupphæð skatts: 10,00 + 5,00 = 15,00 SALESTAX: 15,00 x 25% = 3.75 Samtals virðisaukaskatt, þ.m.t. gjöld: 5,00 + 2,50 + 3,75 = 11,25 heildarupphæð: 10,00 + 11,25 = 21,25 25% SALESTAX er reiknað út fyrir samtöluna af nettóupphæðinni (10,00) + GJALD 1 (5,00) = 15,00. Gjaldi 2 er bætt við skattupphæðina eftir að virðisaukaskatturinn hefur verið reiknaður út.

## <a name="calculated-percentage-of-net-amount"></a> Reiknuð prósenta af nettóupphæð
Reiknuð prósenta af nettóupphæð meðhöndlar skattaútreikninga á annan hátt allt eftir stillingu færibreytunnar Upphæðir innihalda vsk fyrir skjalið eða færslubókina.
### <a name="example-1"></a>Dæmi 1

Skjal / færslubók er stillt á Upphæðir með virðisaukaskatti = Já Færslulínuupphæð: 10,00 Skatthlutfall: 25% Virðisaukaskattur: færslulínuupphæðin x skatthlutf (10,00 x 25%) = 2,50 Grunnupphæð (upphæð uppruna): Færslulínuupphæð - Vsk (10,00-2,50) = 7,50

### <a name="example-2"></a>Dæmi 2

Skjal / færslubók er stillt á Upphæðir með virðisaukaskatti = Nei Færslulínuupphæð: 10,00 Skatthlutfall: 25% Virðisaukaskattur: (Færslulínuupphæð x Skatthlutf) / (100 - skatthlutfall) (10,00 x 25%) / (100% - 25%) = 3,33 Grunnupphæð (upphæð uppruna): færslulínuupphæð = 10,00



<a name="see-also"></a>Sjá einnig
--------

[Ákvarða skatthlutfall virðisaukaskatts á grundvelli reitanna Jaðargrunnur og Útreikningsaðferð](marginal-base-field.md)

[Útreikningsaðferð heildarupphæðar og tímabils fyrir vsk-kóða](whole-amount-interval-options-sales-tax-codes.md)




