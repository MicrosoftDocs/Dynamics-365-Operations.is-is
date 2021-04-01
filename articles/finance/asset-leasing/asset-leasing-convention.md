---
title: Viðteknar reglur eignarleigu
description: Þetta efnisatriði lýsir viðteknum reglum fyrir leigðar eignir.
author: moaamer
manager: Ann Beebe
ms.date: 1/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetLease
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2021-1-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 7072c34ccbffc6bf135f55fd594cac4d9ea5a463
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5237517"
---
# <a name="asset-leasing-conventions"></a>Viðteknar reglur eignarleigu

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Þetta efnisatriði lýsir viðteknum reglum fyrir leigðar eignir. Viðteknar reglur leigusamninga eru notaðar til að ákvarða upphafsdag leigubókar. Ef viðtekin regla leigusamnings er stillt á **Engin** er upphafsdagurinn sá sami og upphafsdagsetning leigusamningsins (þ.e. gildið í reitnum **Upphafsdagsetning leigusamnings**). Ef viðtekin regla leigusamnings er stillt á **Heill mánuður** er upphafsdagurinn fyrsti dagur mánaðarins sem upphafsdagsetning leigusamningings fellur undir.

Upphafsdagurinn ákvarðar upphafsdagsetningu tímabilsins fyrir afskriftaráætlun leiguskuldbindingar og eignar. Vaxtakostnaður og afskriftakostnaður eru bókaðir á lokadagsetningu tímabils samsvarandi áætlana. Upphafleg skráningarfærsla og færsla í leiðréttingabók eru bókaðar á upphafsdeginum.

> [!NOTE]
> Það verður að kveikja á eiginleikanum fyrir viðteknar reglur leigusamninga í gegnum eiginleikastjórnun. Á vinnusvæðinu **Eiginleikastjórnun** skal finna og velja eiginleikann sem heitir **Viðtekin regla leigusamnings fyrir eignarleigu** og velja því næst **Virkja núna**.

Viðteknum reglum leigusamninga er úthlutað á uppsetninguna fyrir leigubók leigusamnings.

Til að skoða eða úthluta viðtekinni reglu leigusamnings skal fylgja þessum skrefum.

1. Opnið **Eignarleiga \> Uppsetning \> Leigubækur**.
2. Í reitnum **Viðtekin regla leigusamnings** skal velja eitt af eftirfarandi gildum.

    | Reglur leigusamnings | lýsing |
    |--------------------|-------------|
    | Engum               | Afskiftaráætlanir leiguskuldbindingar og eignar hefjast á upphafsdagsetningu leigusamningsins vegna þess að upphafsdagurinn jafngildir upphafsdagsetningu leigusamningsins. Lokadagsetningin er einum mánuði síðar. Þessi viðtekna regla leigusamnings tryggir ekki að vextirnir verði bókaðir á síðasta degi hvers mánaðar. |
    | Heill mánuður         | Fyrir leigusamninga sem eru með upphafsdagsetningu sem kemur upp einhvern tímann í mánuðinum byrja afskriftaráætlanir leiguskuldbindingar og eignar að safna saman kostnaði á fyrsta degi þess mánaðar. Þessi viðtekna regla leigusamnings tryggir að vöxtum er safnað saman á síðasta degi hvers mánaðar fyrir allan mánuðinn. |

3. Veljið **Vista**.

Þegar leigusamningur er stofnaður er upphafsdagur hverrar bókar sjálfkrafa færður inn samkvæmt upphafsdagsetningunni sem er færð inn fyrir leigusamninginn og viðteknu reglu hans sem er tilgreind fyrir bókina.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]