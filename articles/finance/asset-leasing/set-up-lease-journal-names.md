---
title: Sett upp leigubókanöfn
description: Þessi grein útskýrir hvernig á að skilgreina heiti leigubóka. Heiti leigubóka tilgreina færslubækur sem færslur sem eru með eignaleigu eru bókaðar í.
author: moaamer
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 678587e0846f6ce6d6d8113290a90b3f4d1988cc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874697"
---
# <a name="set-up-lease-journal-names"></a>Sett upp leigubókanöfn

[!include [banner](../includes/banner.md)]


Heiti leigubóka tilgreina færslubækur sem Færslur Eignarleigu eru bókaðar í. Aðeins færslubókarnöfn sem er úthlutað á færslubókargerðina **Eignarleiga** birtast í **Upphafleg skráning** og **Heiti mánaðarlegrar færslubókar** reitir á síðunni **Færibreytur eignarleigu**. Aðeins er hægt að úthluta færslubókargerðinni **skráning á reikningi lánardrottins** í reitinn **Heiti reikningabókar**.

Kerfið læsir tilteknum fjármálareitum frá því að vera breytt til að koma í veg fyrir frávik á milli færslanna og áætlana. Sumir reitir sem eru læstir eru m.a.: **Lykill**, **Upphæðir**, **Fjárhagsvíddir**, **Gjaldmiðill** og **Færslugerð**. Auk þess getur þú ekki bætt við eða eytt færslulínum færslubókar í neinum færslum eignarleigubókar því það gæti valdið frávikum á milli áætlana og færslnanna.


Til að stilla heiti leigubóka skaltu ljúka eftirfarandi skrefum.

1. Opnið **Eignarleiga \> Uppsetning \> Færibreytur fyrir eignarleigu**.
2. Á flipanum **Almennt** í reitnum **Færslubókarheiti upphaflegrar skráningar** skal velja færslubók. Allar upphaflegar færslubókarskráningar verða bókaðar á þetta færslubókarheiti.
3. Velja færslubók í svæðinu **Heiti reikningabókar**. Ef valkosturinn **Greiða lánardrottni** er stilltur á **Já** fyrir leigubókina verða reikningar leigu og kostnaðar bókaðir á þetta færslubókarheiti.
4. Velja færslubók í svæðinu **Heiti leigubókar**. Allar afskriftir, vextir og endurflokkunarfærslur fyrir skammtíma verða bókaðar á þetta færslubókarheiti. Ef valkosturinn **Greiða lánardrottni** er stilltur á **Nei** fyrir leigubókina verða leigugreiðslur og kostnaðarfærslur einnig bókaðar á þetta færslubókarheiti.
5. Í **Heiti breytingadagbókar leigusamnings** reit, veldu dagbók. Leiguleiðréttingar, uppsögn og virðisrýrnunarfærslur verða færðar á þetta færslubókarheiti. Dagbókarheitinu sem þú velur ætti ekki að vera úthlutað verkflæði eða samþykki. Ef nafn leigubókarbreytinga er ekki skilgreint verða leiðréttingar, uppsögn og virðisrýrnunarfærslur færðar í færslubókarheitið sem er valið í **Nafn leigubókar** sviði. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
