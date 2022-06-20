---
title: Altækar færibreytur fartækja
description: Þessi grein útskýrir hvernig á að setja upp farsímastillingar á síðunni Vöruhússtjórnunarfæribreytur.
author: Mirzaab
ms.date: 08/13/2021
ms.topic: article
ms.search.form: WHS
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-08-13
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: e6e03414edd9243fcc4156195928455b30a7cee9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847760"
---
# <a name="global-mobile-device-parameters"></a>Altækar færibreytur fartækja

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir hvernig á að setja upp alþjóðlegar vöruhúsastjórnunarfæribreytur sem hafa áhrif á hvernig kerfið hefur samskipti við fartæki.

Frekari upplýsingar um hvernig á að setja upp starfsmenn vöruhúss er að finna í [Stjórna starfsmanni vöruhúss](manage-warehouse-workers.md). Frekari upplýsingar um meðhöndlun númeraplötu á fartækjum er að finna í [Móttaka númeraplötu í gegnum farsímaforrit vöruhúsakerfis](warehousing-mobile-device-app-license-plate-receiving.md). Frekari upplýsingar um ferli reglulegrar talningar er að finna í [Regluleg talning](cycle-counting.md) og [Sýnidæmi reglulegrar talningar](cycle-counting-scenarios.md).

## <a name="open-the-warehouse-management-parameters-page"></a>Opna færibreytusíðu vöruhúsakerfis

Til að opna síðuna **Færibreytur vöruhúsakerfis** skal fara í **Vöruhúsakerfi \> Uppsetning \> Færibreytur vöruhúsakerfis**. Þú getur síðan stillt reiti sem tengjast vinnu farsíma, eins og lýst er í næsta hluta þessarar greinar.

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
