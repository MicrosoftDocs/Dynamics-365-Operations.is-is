---
title: Fá skilavörur afhentar að hluta
description: Hlutaafhendingar eru skilgreindar í skilapöntunarlínum, ekki vöruskilasendingum.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 31db10ad820bf049192ba0446b59da16cab3c553
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010598"
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




