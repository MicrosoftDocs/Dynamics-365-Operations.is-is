---
title: Samstilla upplýsingar um samstæðuviðskiptavini
description: Þetta efnisatriði útskýrir samstillingu viðskiptavinaupplýsinga fyrir samstæðupantanir
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: c82216c8391f6c447bec74f25cd16b9db18d468d
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548336"
---
# <a name="synchronize-intercompany-customer-information"></a>Samstilla upplýsingar um samstæðuviðskiptavini

[!include [banner](../../includes/banner.md)]

Upplýsingar um viðskiptavin eru samstilltar ef svæðið **Upplýsingar um viðskiptavin** er virkjað þegar sölupöntun er stofnuð eða þegar breyting er gerð á viðskiptavini, tilvísun í lánardrottin eða beiðninúmeri viðskiptavinar.

Það er alltaf hægt að breyta gildinu í þessum reitum samstillingar. Hinsvegar er einungis hægt að ákvarða hvort þetta gildi er afritað í aðrar samstæðupantanir með því að velja þessa færibreytu. Ef svæðið **Upplýsingar um viðskiptavin** hefur verið virkjað á sölupöntun samstæðu, verða breytingar á henni samstilltar með innkaupapöntun samstæðu. Ef svæðið **Upplýsingar um viðskiptavin** hefur líka verið virkjað í samstæðuinnkaupapöntuninni er hún líka samstillt aftur til upprunalegu sölupöntunarinnar.

> [!NOTE]
> Ef svæðið **Upplýsingar um viðskiptavin** var virkjað bæði á samstæðusölupöntuninni og á samstæðuinnkaupapöntuninni verður uppfærslum sem eru gerðar af starfsmanni eins fyrirtækis hnekkt með uppfærslum sem annar starfsmaður í öðru fyrirtæki gerir á sömu pöntun.

Best er að virkja reitinn **Upplýsingar um viðskiptavin** í samstæðuinnkaupapöntuninni. Þetta virkjar samstillingu á milli upprunalegu sölupöntunarinnar og samstæðuinnkaupapöntunarinnar og úr samstæðuinnkaupapöntuninni í samstæðusölupöntunina.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
