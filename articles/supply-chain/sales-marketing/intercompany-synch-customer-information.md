---
title: Samstilla upplýsingar um samstæðuviðskiptavini
description: Þessi grein útskýrir samstillingu viðskiptavinaupplýsinga fyrir samstæðupantanir
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: a3a67c9bcf93f88375d2d4d78d87175200626d50
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897517"
---
# <a name="synchronize-intercompany-customer-information"></a>Samstilla upplýsingar um samstæðuviðskiptavini

[!include [banner](../../includes/banner.md)]

Upplýsingar um viðskiptavin eru samstilltar ef svæðið **Upplýsingar um viðskiptavin** er virkjað þegar sölupöntun er stofnuð eða þegar breyting er gerð á viðskiptavini, tilvísun í lánardrottin eða beiðninúmeri viðskiptavinar.

Það er alltaf hægt að breyta gildinu í þessum reitum samstillingar. Hinsvegar er einungis hægt að ákvarða hvort þetta gildi er afritað í aðrar samstæðupantanir með því að velja þessa færibreytu. Ef svæðið **Upplýsingar um viðskiptavin** hefur verið virkjað á sölupöntun samstæðu, verða breytingar á henni samstilltar með innkaupapöntun samstæðu. Ef svæðið **Upplýsingar um viðskiptavin** hefur líka verið virkjað í samstæðuinnkaupapöntuninni er hún líka samstillt aftur til upprunalegu sölupöntunarinnar.

> [!NOTE]
> Ef svæðið **Upplýsingar um viðskiptavin** var virkjað bæði á samstæðusölupöntuninni og á samstæðuinnkaupapöntuninni verður uppfærslum sem eru gerðar af starfsmanni eins fyrirtækis hnekkt með uppfærslum sem annar starfsmaður í öðru fyrirtæki gerir á sömu pöntun.

Best er að virkja reitinn **Upplýsingar um viðskiptavin** í samstæðuinnkaupapöntuninni. Þetta virkjar samstillingu á milli upprunalegu sölupöntunarinnar og samstæðuinnkaupapöntunarinnar og úr samstæðuinnkaupapöntuninni í samstæðusölupöntunina.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
