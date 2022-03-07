---
title: Færibreytur fyrir farsíma á heimsvísu
description: Þetta efnisatriði útskýrir hvernig á að setja upp stillingar fartækis á færibreytusíðu vöruhúsakerfis.
author: HuberIvan
ms.date: 08/13/2021
ms.topic: article
ms.search.form: WHS
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-huberivan
ms.search.validFrom: 2021-08-13
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 03c10232d55c99c73e625170797f89f6c77e812b
ms.sourcegitcommit: 99bde425ade701ef244c6bca6d411aef94a59b3c
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/20/2021
ms.locfileid: "7505576"
---
# <a name="global-mobile-device-parameters"></a>Færibreytur fyrir farsíma á heimsvísu

[!include [banner](../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig á að setja upp altækar færibreytur vöruhúsakerfis sem hafa áhrif á hvernig kerfið á í samskiptum við fartækin.

Frekari upplýsingar um hvernig á að setja upp starfsmenn vöruhúss er að finna í [Stjórna starfsmanni vöruhúss](manage-warehouse-workers.md). Frekari upplýsingar um meðhöndlun númeraplötu á fartækjum er að finna í [Móttaka númeraplötu í gegnum farsímaforrit vöruhúsakerfis](warehousing-mobile-device-app-license-plate-receiving.md). Frekari upplýsingar um ferli reglulegrar talningar er að finna í [Regluleg talning](cycle-counting.md) og [Sýnidæmi reglulegrar talningar](cycle-counting-scenarios.md).

## <a name="open-the-warehouse-management-parameters-page"></a>Opna færibreytusíðu vöruhúsakerfis

Til að opna síðuna **Færibreytur vöruhúsakerfis** skal fara í **Vöruhúsakerfi \> Uppsetning \> Færibreytur vöruhúsakerfis**. Síðan er hægt að stilla reitina sem tengjast vinnu fartækis eins og lýst er í næsta hluta þessa efnisatriðis.

## <a name="mobile-device-fasttab-on-the-general-tab"></a>Flýtiflipi fartækis í almenna flipanum

Altækar stillingar fartækis finnast í flýtiflipanum **Fartæki** í flipanum **Almennt** á síðunni **Færibreytur vöruhúsakerfis**. Eftirfarandi reitir eru tiltækir.

| Svæði | lýsing |
|---|---|
| Gerð athugasemdar fartækis | Veldu hvers konar upplýsingar á að sýna starfsmönnum við tiltekt sölupöntunar. |
| Mörk skannaðs magns | Sláðu inn hámarksmagn vöru sem starfsmaður getur skannað í hverri lotu með því að nota valmyndaratriði fartækis sem er gildið **Ferli verkstofnunar** sem *Leiðrétting inn*. Þessi reitur hefur ekki áhrif á skönnun sem er gerð með því að nota aðra gerð valmyndaratriðis. |
| Nota kladda fyrir fartæki | Stilltu þennan valkost á *Já* til að halda skrá yfir innskráningarferil starfsmanns. Til að skoða kladdann skal fara í **Lotur verknotanda \> Fyrirspurnir og skýrslur \> Kladdar fartækis \> Lotur verknotanda**. |
| Fjöldi vistaðra villna | Færðu inn hámarksfjölda af villufærslum sem kerfið hefur geymt. Til að skoða villukladdann skal fara í **Lotur verknotanda \> Fyrirspurnir og skýrslur \> Kladdar fartækis \> Lotur verknotanda**. |
| Sjálfgefin færslubók vöruhússflutninga | Veldu færslubókina sem er notuð þegar starfsmenn nota fartæki til að flytja afurðir úr einu vöruhúsi í annað. |
| Leyfa skráningu innkaupapöntunarlína í ytri yfirferð | Stilltu þennan valkost á *Já* ef starfsmenn eiga að geta notað fartæki til að skrá pöntunarlínur fyrir innkaupapantanir sem eru með gildi **Samþykktarstöðu** sem *Í ytri yfirferð*. Stilltu þennan valkost á *Nei* til að koma í veg fyrir að starfsmenn skrái línur fyrir innkaupapantanir sem eru í ytri yfirferð. |
| Virkja RSAT-stuðning | Reiturinn virkjar sannprófun á verki í fartækjaforriti vöruhúsakerfis sem skráir og sannprófar hvert skref sem forritið framkvæmir. Þar sem þetta ferli getur hægt verulega á afköstum kerfisins ættir þú aðeins að virkja sannprófarann við prófun. Þú ættir aldrei að virkja hann í vinnsluumhverfi. |
