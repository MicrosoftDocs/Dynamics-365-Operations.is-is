---
title: Setja upp gjöld í samstæðupöntunum
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp gjöld í samstæðupöntunum
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: CustTable, VendTable, EcoResProductListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 3786df5ce185fa8433d7c69bed5bef09b4983b8b
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548337"
---
# <a name="set-up-charges-on-intercompany-orders"></a>Setja upp gjöld í samstæðupöntunum

[!include [banner](../../includes/banner.md)]

Þú getur sett upp gjöld til að bæta við pöntun innan samstæðu. Þegar gjaldi er bætt við samstæðusölupöntun er hún sjálfkrafa samstillt við samstæðuinnkaupapöntunina. Virkar eins í báðar áttir — úr samstæðusölupöntun í innkaupapöntun og öfugt.

Einnig er hægt að nota gjöld til að bæta hagnaði við samstæðusölupöntun með því að skilgreina gjaldið sem samstæðuprósentu.

Þegar sett eru upp gjöld sem nota á við samstæðupantanir eru útreikningar á innri hagnaði í samstæðusölupöntun af nettó upphæð á upprunalegu sölupöntuninni gerðir virkir. Þetta gæti átt við ef samstæðulánardrottinn selur vörurnar á kostnaðarverði. Eftirfarandi aðferð lýsir því hvernig þetta er gert fyrir samstæðuviðskiptavini. Hægt er að nota sömu aðferð fyrir lánardrottna.

1. Farðu í **Viðskiptakröfur \> Uppsetning \> Gjöld \> Gjaldflokkar viðskiptavina**.
1. Stofna gjaldaflokk.
1. Farðu í **Viðskiptakröfur \> Viðskiptavinir \> Alla viðskiptavini**. Velja viðskiptavinalykilstengil. Á aðgerðasvæðinu skal velja flipann **Viðskipavinur** og síðan velja flýtiflipann **Sölupöntun**.
1. Veldu **Breyta** á aðgerðasvæðinu til að virkja breytingar á reitnum. Í reitnum **Gjaldaflokkur** skaltu velja samstæðugjaldaflokkinn sem þú settir upp í skrefi 2.
1. Farðu í **Viðskiptakröfur \> Uppsetning \> Gjöld \> Sjálfvirk gjöld**.
1. Settu upp gjöldin með því að fylla út viðeigandi reiti.
1. Í reitnum **Tengsl viðskiptavina** skaltu velja samstæðugjaldaflokkinn sem þú settir upp í skrefi 2.
1. Í flýtiflipanum **Línur**, í reitnum **Flokkur**, skal velja **Samstæðuprósenta**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
