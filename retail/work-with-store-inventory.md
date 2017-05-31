---
title: "Stjórna Birgðir verslunar"
description: "Þessi grein lýsir gerðum skjala sem hægt er að nota til að stýra birgðum."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 5e5043d5951015fc14d29989ef4cab20a8b24f3b
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017


---

# <a name="manage-store-inventory"></a>Stjórna Birgðir verslunar

[!include[banner](includes/banner.md)]


Þessi grein lýsir gerðum skjala sem hægt er að nota til að stýra birgðum.

Hægt er að nota eftirfarandi gerðir af skjölum til að stjórna birgðum fyrirtækisins.

## <a name="purchase-orders"></a>Innkaupapantanir
Innkaupapantanir eru stofnaðar á aðalskrifstofu. Ef vöruhús smásölu er innifalið í haus innkaupapöntunar er hægt að taka við pöntuninni í verslun með því að nota Modern POS (MPOS) eða Cloud POS í Microsoft Dynamics 365 for Operations - Retail. Eftir að umbeðið magn hefur verið móttekið í versluninni er hægt að vista það staðbundið fyrir frekari breytingar. Einnig er hægt að ráðstafa magninu og senda það á aðalskrifstofu. Á aðalskrifstofunni birtist magn sem var móttekið í verslun í Dynamics 365 for Operations í reitnum **Móttaka núna** á innkaupapöntuninni.

## <a name="transfer-orders"></a>Flutningspantanir
Flutningspöntun getur tilgreint að ákveðin verslun sé staðsetning sem hægt er að senda vörurnar úr. Í þessu tilfelli birtist flutningspöntun í verslun sem beiðni um tiltekt í MPOS eða Cloud POS. Eftir að umbeðið magn hefur verið tekið til er því ráðstafað og sent til aðalskrifstofu. Á aðalskrifstofunni birtist magn sem var móttekið í verslun í Dynamics 365 for Operations í reitnum **Senda núna** á flutningspöntuninni. Flutningspöntun getur tilgreint að ákveðin verslun sé staðsetning sem hægt er að senda vörurnar til. Í þessu tilfelli birtist flutningspöntun í verslun sem beiðni um móttöku í MPOS eða Cloud POS. Eftir að umbeðið magn hefur verið móttekið í versluninni er hægt að vista það staðbundið fyrir frekari breytingar. Einnig er hægt að ráðstafa magninu og senda það á aðalskrifstofu. Á aðalskrifstofunni birtist magn sem var móttekið í verslun í Dynamics 365 for Operations í reitnum **Móttaka núna** á flutningspöntuninni.

## <a name="stock-counts"></a>Birgðatalning
Birgðatalningar geta verið annaðhvort áætlaðar eða óskipulagðar. Áætluð birgðatalning – Þessar birgðatalningar eru gerðar að frumkvæði aðalskrifstofunnar og það er hún sem ákveður hvaða vörur á að telja. Aðalskrifstofa útbýr talningarskjal og sendir versluninni það og þar eru upplýsingar um birgðastöðu færðar inn í MPOS eða Cloud POS. Óundirbúin birgðatalning er hafin í verslun og magn raunbirgða á lager er uppfært í annaðhvort MPOS eða Cloud POS. Ólíkt áætlaðri birgðatalningu hafa óundirbúnar birgðatalningar ekki fyrirfram skilgreindan lista yfir vörur. Þegar birgðatalningu af annarri hvorri gerð er lokið er henni ráðstafað og send til aðalskrifstofu. Á aðalskrifstofu er talningin villuleituð og bókuð.






