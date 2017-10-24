---
title: "Hreyfing birgða með tengdri vinnu í vöruhúsakerfi"
description: "Í þessu efnisatriði er því lýst hvernig eigi að setja upp og nota staðfestingu einingartiltektar úr fartæki."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 463e438418c4bc1b38fd1bde8251d1383cb44a13
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="movement-of-inventory-with-associated-work-in-warehouse-management"></a>Hreyfing birgða með tengdri vinnu í vöruhúsakerfi

[!include[banner](../includes/banner.md)]

Með notkun á hreyfingu birgða er hægt að skera úr um hvaða starfsmenn í vöruhúsi megi hreyfa fráteknar birgðir. Þetta gefur sveigjanleika í stýrðum vöruhúsum, þar sem þú getur ákveðið að heimila ekki starfsmanni að velja nýja tiltektarstaðsetningu fyrir tínsluvinnu sem hefur þegar verið stofnuð. Það gerir vöruhúsastjóra einnig kleift að stýra hvaða heimildir reynsluminni starfsmenn eiga að hafa.

Sveigjanleiki til að stjórna daglegri starfsemi starfsfólks í vöruhúsi getur verið gagnlegur við aðstæður sem þessar:

## <a name="scenario-1"></a>Aðstæður 1
Fyrirtæki hefur tiltölulega lítið móttökusvæði og það er yfirfullt af brettum og kössum sem bíða frágangs. Stór sending er væntanleg síðar sama dag þannig að starfsmaður í móttöku ákveður að hreinsa móttökusvæðið með því að færa sum brettin í biðgeymslu fyrir vörur á innleið.

## <a name="scenario-2"></a>Aðstæður 2
Reyndur starfsmaður í vöruhúsi sér tækifæri til að sameina vörurnar á einni staðsetningu í stað þess að dreifa þeim á þrjár nærliggjandi staðsetningar með litlu magni í hverri þeirra. Starfsmaðurinn vill sameina magnið með því að færa vörurnar úr hverri þessara staðsetninga á sömu staðsetningu og á sömu númeraplötuna.

## <a name="scenario-3"></a>Aðstæður 3
Bretti bíður sendingar í biðgeymslu, eins og BIÐ01 sem er nálægt AFGREIÐSLUHURÐ01. Hins vegar verður breyting, þar sem flutningabíllinn á að koma í AFGREIÐSLUHURÐ04. Starfsmaður sem sér um sendinguna er meðvitaður um þetta og þarf að sjá til þess að flutningabíllinn þurfi ekki að bíða þess að vera fermdur úr BIÐ01. Starfsmaðurinn ákveður að færa vörurnar í þeirri sendingu úr BIÐ01 í BIÐ04, sem er nær nýju staðsetningunni.

### <a name="current-limitations"></a>Núverandi takmarkanir

Vinnufrátektir sem þú getur fært takmarkast við Sölupöntun, Útgáfu flutningspöntunar, Innhreyfingu flutningspöntunar, Innkaupapöntun og Áfyllingarvinnu.

Hreyfing á vörum takmarkast við að skipta upp vinnulínum. Þetta þýðir að ef þú ert með vinnulínu fyrir 100 stk. af vöru A úr staðsetningu Sta1, er ekki hægt að færa bara 30 stk. af vöru A þaðan í aðra staðsetningu. Það myndi þýða skiptingu á fyrirliggjandi vinnulínu í 30 og 70, þar sem staðsetningarnar eru nú mismunandi.

Þegar um er að ræða biðgeymsluaðstæður, þar sem númeraplatan sem þú færir vörur frá eða númeraplata sem þú færir vörur á, er stillt á Marknúmeraplötu fyrir verkbeiðni, má aðeins færa alla númeraplötuna þannig að marknúmeraplata sé ekki brotin upp.
Aðeins tilfallandi hreyfing er studd eins og er. Þetta þýðir að ekki verður hægt að færa fráteknar birgðir með hreyfingu sniðmátsvalmyndaratriða úr fartæki.

### <a name="set-up-permission-to-move-reserved-inventory-for-individual-workers"></a>Setja heimild til að færa fráteknar birgðir fyrir einstaka starfsmenn

Fyrir starfsmann sem má flytja fráteknar birgðir skal velja gátreitinn **Leyfa hreyfingu birgða með tengdri vinnu** undir **Vöruhúsastjórnun** > **Uppsetning** > **Starfsmaður**.  

### <a name="backported"></a>Bakfært

Þessi eiginleiki hefur einnig verið bakfærður í Microsoft Dynamics AX 2012 R3 og verður í boði sem hluti af CU12.
Einnig er hægt að hlaða honum niður einum og sér í gegnum KB-númer 3192548. 


