---
title: Röðun með ótakmarkaða getu
description: Þessi grein veitir upplýsingar um óendanlega afkastagetu tímasetningu fyrir áætlanagerð fínstillingu. Það lýsir einnig núverandi takmörkunum á eiginleikum.
author: t-benebo
ms.date: 09/21/2021
ms.topic: article
ms.search.form: RouteInventProd
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-06-09
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 3646a7ca1f9a3a87a2f130783dc4961a61335f1d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873870"
---
# <a name="scheduling-with-infinite-capacity"></a>Röðun með ótakmarkaða getu

[!include [banner](../../includes/banner.md)]

Eiginleikinn *Ótakmörkuð afkastaáætlun fyrir fínstillingu skipulagningar* kynnir til sögunnar áætlanagerð sem byggir á upplýsingum leiðar. Hann gerir þér kleift að áætla vinnslur sem byggja á fjölbreyttum uppsetningum leiðar. Áætlanagerð fyrir fínstillingu skipulagningar nær yfir mikið notaðar stillingar leiðar, þ.m.t. röð leiðaraðgerðar eða kröfur fyrir tilföng leiðaraðgerðar.

## <a name="turn-on-the-infinite-capacity-scheduling-feature"></a>Kveikja á eiginleika ótakmarkaðrar afkastaáætlunar

Áður en hægt er að nota þennan eiginleika þarf að kveikja á honum í kerfinu. Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikja á honum. Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:

- **Eining:** *Aðaláætlanagerð*
- **Heiti eiginleika:** *Ótakmörkuð afkastaáætlun fyrir fínstillingu áætlanagerðar*

Frekari upplýsingar um þennan eiginleika er að finna í [Röðun með vali á tilföngum út frá getu](capability-based-scheduling.md).

## <a name="added-functionality"></a>Virkni bætt við

Eiginleikinn *Ótakmörkuð afkastaáætlun fyrir fínstillingu skipulagningar* virkjar áætlanagerð sem byggir á upplýsingum leiðar. Því er hægt að nota uppsetningu leiðar til að áætla framleiðsluferli. Þó að þessi eiginleiki hafi einhverjar takmarkanir sem innbyggð aðaláætlanagerð hefur ekki, styður hann algengustu virknina sem þarf fyrir framleiðsluaðstæður.

Eiginleikinn tekur tillit til bæði *einfaldra leiða* og *kerfi leiða*. Með því að nota reitinn **Næst** í leiðaraðgerð er hægt að setja upp flóknar leiðir sem eru með marga upphafspunkta og margar aðgerðir sem keyra samhliða. Kerfið mun taka til greina flókið skipulag leiðar af þessari gerð við áætlanagerð.

Auk þess styður eiginleikinn *samhliða aðgerðir* í leiðum. Með því að nota valkostina *Aðal* og *Auka* í reitnum **Forgangur** í leiðaraðgerðum er hægt að skilgreina skipulag leiðar þegar ein leiðaraðgerð er aðalaðgerðin og önnur er aukaaðgerðin. Í þessu tilfelli mun kerfið taka til greina skipulag leiðarinnar við áætlanagerð.

Meðan á áætlunarferlinu stendur tekur kerfið einnig tillit til *tilfangaþörf* sem er tilgreind fyrir aðgerð. Kerfið notar tilfangaþörf til að skera úr um hvaða tilföng eru nauðsynleg til að framkvæma aðgerðina. Eins og er styður eiginleikinn *Ótakmörkuð afkastaáætlun fyrir fínstillingu skipulagningar* eftirfarandi gerðir af tilfangaþörfum:

- Gerð forða
- Tilföng
- Tilfangaflokkur
- Geta (frekari upplýsingar er að finna í [Röðun með vali á tilföngum út frá getu](capability-based-scheduling.md).)

> [!NOTE]
>
> - Ef tilfangið og/eða tilfangahópurinn er stilltur á óendanlega getu, mun aðalskipulag líta á þau sem óendanlega getu.
> - Kröfur sem tengjast mannauði eins og hæfniskröfur eða vottorð eru enn ekki studdar.

Eiginleikinn styður einnig rekstrareiginleikana **Uppsetningartími** og **Keyrslutími**. Þegar þú stillir þessa eiginleika á leiðaraðgerð mun áætlunarferlið búa til viðeigandi uppsetningu og vinnsluverk.

Í stuttu máli styður fínstilling skipulagningar algengustu aðstæðurnar. Þú getur búið til leiðina, bætt við aðal- og aukaaðgerðum, skilgreint næstu aðgerðir, bætt við tilfangaþörfum og bætt við uppsetningartíma og keyrslutíma. Kerfið mun síðan hafa þessar upplýsingar í huga við áætlanagerð.

## <a name="limitations"></a>Takmarkanir

Eftirfarandi takmarkanir eiga við þegar þú notar áætlanagerð fyrir fínstillingu skipulagningar:

- Eiginleikinn styður aðeins ótakmarkaða getu.
- Þessi eiginleiki styður ekki virkni tilfangahleðslu.
- Eiginleikinn tekur ekki tillit til leiðarrýrnunar.
- Eiginleikinn styður einungis *Tímalengd* sem val aðaltilfangs.

Athugaðu að það er stöðugt verið að bæta eiginleikann *Ótakmörkuð afkastaáætlun fyrir fínstillingu skipulagningar*. Microsoft gerir ráð fyrir að innleiða stuðning við viðbótarstillingar fyrir áætlanagerð í komandi útgáfum.
