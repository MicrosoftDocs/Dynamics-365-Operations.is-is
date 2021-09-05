---
title: Sett upp leigubókanöfn
description: Þetta efnisatriði útskýrir hvernig á að skilgreina heiti leigubóka. Heiti leigubóka tilgreina færslubækur sem færslur sem eru með eignaleigu eru bókaðar í.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1ea35ec40ddd459e1a9e7641557147e23fe45d3e
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/13/2021
ms.locfileid: "7343215"
---
# <a name="set-up-lease-journal-names"></a>Sett upp leigubókanöfn

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


Heiti leigubóka tilgreina færslubækur sem Færslur Eignarleigu eru bókaðar í. Aðeins færslubókarnöfn sem er úthlutað á færslubókargerðina **Eignarleiga** birtast í **Upphafleg skráning** og **Heiti mánaðarlegrar færslubókar** reitir á síðunni **Færibreytur eignarleigu**. Aðeins er hægt að úthluta færslubókargerðinni **skráning á reikningi lánardrottins** í reitinn **Heiti reikningabókar**.

Kerfið læsir tilteknum fjármálareitum frá því að vera breytt til að koma í veg fyrir frávik á milli færslanna og áætlana. Sumir reitir sem eru læstir eru m.a.: **Lykill**, **Upphæðir**, **Fjárhagsvíddir**, **Gjaldmiðill** og **Færslugerð**. Auk þess getur þú ekki bætt við eða eytt færslulínum færslubókar í neinum færslum eignarleigubókar því það gæti valdið frávikum á milli áætlana og færslnanna.


Til að skilgreina heiti leigubóka skal fylgja þessum skrefum.

1. Opnið **Eignarleiga \> Uppsetning \> Færibreytur fyrir eignarleigu**.
2. Á flipanum **Almennt** í reitnum **Færslubókarheiti upphaflegrar skráningar** skal velja færslubók. Allar upphaflegar færslubókarskráningar verða bókaðar á þetta færslubókarheiti.
3. Velja færslubók í svæðinu **Heiti reikningabókar**. Ef valkosturinn **Greiða lánardrottni** er stilltur á **Já** fyrir leigubókina verða reikningar leigu og kostnaðar bókaðir á þetta færslubókarheiti.
4. Velja færslubók í svæðinu **Heiti leigubókar**. Allar afskriftir, vextir og endurflokkunarfærslur fyrir skammtíma verða bókaðar á þetta færslubókarheiti. Ef valkosturinn **Greiða lánardrottni** er stilltur á **Nei** fyrir leigubókina verða leigugreiðslur og kostnaðarfærslur einnig bókaðar á þetta færslubókarheiti.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
