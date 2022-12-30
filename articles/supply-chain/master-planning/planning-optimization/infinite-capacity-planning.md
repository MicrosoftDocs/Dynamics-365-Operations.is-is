---
title: Áætlun með ótakmarkaða getu
description: Þessi grein veitir upplýsingar um áætlanagerð ótakmarkaðrar afkastagetu. Það lýsir einnig núverandi takmörkunum á eiginleikum.
author: t-benebo
ms.date: 08/09/2022
ms.topic: article
ms.search.form: RouteInventProd
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-06-09
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 7249734e5d2644145a36276dbc818a40b5962805
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740006"
---
# <a name="scheduling-with-infinite-capacity"></a>Áætlun með ótakmarkaða getu

[!include [banner](../../includes/banner.md)]

Eiginleikinn *Ótakmörkuð afkastaáætlun fyrir fínstillingu skipulagningar* kynnir til sögunnar áætlanagerð sem byggir á upplýsingum leiðar. Hann gerir þér kleift að áætla vinnslur sem byggja á fjölbreyttum uppsetningum leiðar. Áætlanagerð nær yfir mikið notaðar stillingar leiðar, þ.m.t. röð leiðaraðgerðar eða kröfur fyrir tilföng leiðaraðgerðar.

## <a name="turn-the-infinite-capacity-scheduling-feature-on-or-off"></a>Kveikja eða slökkva á eiginleika fyrir áætlanagerð ótakmarkaðrar afkastagetu

Til að nota þennan eiginleika þarf að kveikja á honum fyrir kerfið þitt. Sem hluti af Supply Chain Management, útgáfa 10.0.29, er sjálfgefið kveikt á þessum eiginleika. Stjórnendur geta kveikt eða slökkt á þessari virkni með því að leita að eiginleikanum *Takmörkuð afkastagetuáætlun fyrir fínstillingu áætlanagerðar* á vinnusvæðinu [Eiginleikastjórnun](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Frekari upplýsingar um þennan eiginleika er að finna í [Röðun með vali á tilföngum út frá getu](capability-based-scheduling.md).

## <a name="added-functionality"></a>Virkni bætt við

Eiginleikinn *Ótakmörkuð afkastaáætlun fyrir fínstillingu skipulagningar* virkjar áætlanagerð sem byggir á upplýsingum leiðar. Því er hægt að nota uppsetningu leiðar til að áætla framleiðsluferli. Þó að þessi eiginleiki hafi einhverjar takmarkanir sem úrelt aðaláætlunarvél hefur ekki, styður hann algengustu virknina sem þarf fyrir framleiðsluaðstæður.

Eiginleikinn tekur tillit til bæði *einfaldra leiða* og *kerfi leiða*. Með því að nota reitinn **Næst** í leiðaraðgerð er hægt að setja upp flóknar leiðir sem eru með marga upphafspunkta og margar aðgerðir sem keyra samhliða. Kerfið mun taka til greina flókið skipulag leiðar af þessari gerð við áætlanagerð.

Auk þess styður eiginleikinn *samhliða aðgerðir* í leiðum. Með því að nota valkostina *Aðal* og *Auka* í reitnum **Forgangur** í leiðaraðgerðum er hægt að skilgreina skipulag leiðar þegar ein leiðaraðgerð er aðalaðgerðin og önnur er aukaaðgerðin. Í þessu tilfelli mun kerfið taka til greina skipulag leiðarinnar við áætlanagerð.

Meðan á áætlunarferlinu stendur tekur kerfið einnig tillit til *tilfangaþörf* sem er tilgreind fyrir aðgerð. Kerfið notar tilfangaþörf til að skera úr um hvaða tilföng eru nauðsynleg til að framkvæma aðgerðina. Eins og er styður eiginleikinn *Ótakmörkuð afkastaáætlun fyrir fínstillingu skipulagningar* eftirfarandi gerðir af tilfangaþörfum:

- Gerð forða
- Tilföng
- Tilfangaflokkur
- Geta (frekari upplýsingar er að finna í [Röðun með vali á tilföngum út frá getu](capability-based-scheduling.md).)

> [!NOTE]
>
> - Ef tilfangi og/eða tilfangahópurinn er stilltur á óendanlega getu mun aðalskipulag líta á þá sem óendanlega getu.
> - Kröfur sem tengjast mannauði eins og hæfniskröfur eða vottorð eru enn ekki studdar.

Eiginleikinn styður einnig rekstrareiginleikana **Uppsetningartími** og **Keyrslutími**. Þegar þú stillir þessa eiginleika á leiðaraðgerð mun áætlunarferlið búa til viðeigandi uppsetningu og vinnsluverk.

Í stuttu máli styður áætlanagerð algengustu aðstæðurnar. Þú getur búið til leiðina, bætt við aðal- og aukaaðgerðum, skilgreint næstu aðgerðir, bætt við tilfangaþörfum og bætt við uppsetningartíma og keyrslutíma. Kerfið mun síðan hafa þessar upplýsingar í huga við áætlanagerð.

## <a name="limitations"></a>Takmarkanir

Eftirfarandi takmarkanir eiga við þegar þú notar eiginleikann *Áætlanagerð ótakmarkaðrar afkastagetu fyrir fínstillingu áætlanagerðar*:

- Eiginleikinn styður aðeins ótakmarkaða getu.
- Þessi eiginleiki styður ekki virkni tilfangahleðslu.
- Eiginleikinn tekur ekki tillit til leiðarrýrnunar.
- Eiginleikinn styður einungis *Tímalengd* sem val aðaltilfangs.
