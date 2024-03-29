---
title: Fá skilavörur afhentar að hluta
description: Hlutaafhendingar eru skilgreindar í skilapöntunarlínum, ekki vöruskilasendingum.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c0e27e3a5cb6be36a1d69190ce1b01ecada48a6
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/03/2022
ms.locfileid: "8677115"
---
# <a name="receive-partial-deliveries-of-returned-items"></a>Fá skilavörur afhentar að hluta    

[!include [banner](../includes/banner.md)]


Hlutaafhendingar eru skilgreindar í skilapöntunarlínum, ekki vöruskilasendingum.

Þetta þýðir að afhendingin er ekki hlutaafhending ef tekið er á móti öllu magninu sem fram kemur í einni skilapöntunarlínu en engu úr öðrum línum í skilapöntuninni. Hins vegar, ef skilapöntunarlína krefst tíu eininga af tiltekinni vöru sem á að skila, en einungis er tekið á móti fjórum, er um að ræða hlutaafhendingu.

Ef vöruskilasending inniheldur minna en allt magnið í skilapöntunarlínu, er hægt að setja sendinguna til hliðar og bíða þess að afgangurinn af skiluðu magni berist eða skrá og bóka hluta af magninu.

## <a name="register-and-post-a-partial-quantity"></a>Skrá og bóka hluta af magni

1.  Eftir að þú velur skilapöntun fyrir afhendingu í skjámyndinni **Komuyfirlit - Vöruhús: %1, dreifing: %2 Heiti færslubókar: %3** skal smella á **Upphafskoma** til að búa til komubók og smella síðan á **Færslubækur** \> **Sýna komur frá kvittunum** til að opna skjámyndina **Staðsetningarbók**.

2.  Veldu línu færslubókarinnar sem þú vilt vinna með og smelltu svo á **Línur** til að opna skjámyndina **Færslubókarlínur, staðsetningar**.

3.  Veldu línu vörunúmersins sem aðeins hluti magns hefur komið fyrir og smelltu síðan á **Aðgerðir** \> **Skipta** til að opna skjámyndina **Skipta**.

4.  Sláðu inn magnið fyrir heildarfjölda varanna sem hafa borist í reitinn **Skipta magni** og smelltu síðan á **Í lagi**.

5.  Í skjámyndinni **Færslubókarlínur, staðsetningar** skal velja línuna fyrir magnið af vörum sem hefur komið og smella síðan á **Bóka**. Þú getur bókað línuna fyrir viðbótarmagnið eftir að vörurnar hafa skilað sér.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]