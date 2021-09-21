---
title: Röðun með ótakmarkaða getu
description: Þetta efnisatriði veitir upplýsingar um ótakmarkaða afkastaáætlun fyrir fínstillingu skipulagningar. Það lýsir einnig núverandi takmörkunum á eiginleikum.
author: crytt
ms.date: 09/02/2021
ms.topic: article
ms.search.form: RouteInventProd
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-06-09
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 2e730340cddac107b04a6b5877e51b84f4dd7b21
ms.sourcegitcommit: a21166da59675e37890786ebf7e0f198507f7c9b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/03/2021
ms.locfileid: "7471669"
---
# <a name="scheduling-with-infinite-capacity"></a>Röðun með ótakmarkaða getu

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

Eiginleikinn *Ótakmörkuð afkastaáætlun fyrir fínstillingu skipulagningar* kynnir til sögunnar áætlanagerð sem byggir á upplýsingum leiðar. Hann gerir þér kleift að áætla vinnslur sem byggja á fjölbreyttum uppsetningum leiðar. Áætlanagerð fyrir fínstillingu skipulagningar nær yfir mikið notaðar stillingar leiðar, þ.m.t. röð leiðaraðgerðar eða kröfur fyrir tilföng leiðaraðgerðar.

## <a name="turn-on-the-infinite-capacity-scheduling-feature"></a>Kveikja á eiginleika ótakmarkaðrar afkastaáætlunar

Ef kerfið inniheldur ekki eiginleikana sem lýst er í þessu efnisatriði skal fara á vinnusvæðið [Eiginleikastjórnun](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og kveikja á eiginleikanum *Ótakmörkuð afkastaáætlun fyrir fínstillingu skipulagningar*.

## <a name="added-functionality"></a>Virkni bætt við

Eiginleikinn *Ótakmörkuð afkastaáætlun fyrir fínstillingu skipulagningar* virkjar áætlanagerð sem byggir á upplýsingum leiðar. Því er hægt að nota uppsetningu leiðar til að áætla framleiðsluferli. Þó að þessi eiginleiki hafi einhverjar takmarkanir sem innbyggð aðaláætlanagerð hefur ekki, styður hann algengustu virknina sem þarf fyrir framleiðsluaðstæður.

Eiginleikinn tekur tillit til bæði *einfaldra leiða* og *kerfi leiða*. Með því að nota reitinn **Næst** í leiðaraðgerð er hægt að setja upp flóknar leiðir sem eru með marga upphafspunkta og margar aðgerðir sem keyra samhliða. Kerfið mun taka til greina flókið skipulag leiðar af þessari gerð við áætlanagerð.

Auk þess styður eiginleikinn *samhliða aðgerðir* í leiðum. Með því að nota valkostina *Aðal* og *Auka* í reitnum **Forgangur** í leiðaraðgerðum er hægt að skilgreina skipulag leiðar þegar ein leiðaraðgerð er aðalaðgerðin og önnur er aukaaðgerðin. Í þessu tilfelli mun kerfið taka til greina skipulag leiðarinnar við áætlanagerð.

Meðan á áætlunarferlinu stendur tekur kerfið einnig tillit til *tilfangaþörf* sem er tilgreind fyrir aðgerð. Kerfið notar tilfangaþörf til að skera úr um hvaða tilföng eru nauðsynleg til að framkvæma aðgerðina. Eins og er styður eiginleikinn *Ótakmörkuð afkastaáætlun fyrir fínstillingu skipulagningar* eftirfarandi gerðir af tilfangaþörfum:

- Gerð forða
- Tilföng
- Tilfangaflokkur
- Geta

> [!NOTE]
> Kröfur sem tengjast mannauði eins og hæfniskröfur eða vottorð eru enn ekki studdar.

Eiginleikinn styður einnig rekstrareiginleikana **Uppsetningartími** og **Keyrslutími**. Þegar þú stillir þessa eiginleika á leiðaraðgerð mun áætlunarferlið búa til viðeigandi uppsetningu og vinnsluverk.

Í stuttu máli styður fínstilling skipulagningar algengustu aðstæðurnar. Þú getur búið til leiðina, bætt við aðal- og aukaaðgerðum, skilgreint næstu aðgerðir, bætt við tilfangaþörfum og bætt við uppsetningartíma og keyrslutíma. Kerfið mun síðan hafa þessar upplýsingar í huga við áætlanagerð.

## <a name="limitations"></a>Takmarkanir

Eftirfarandi takmarkanir eiga við þegar þú notar áætlanagerð fyrir fínstillingu skipulagningar:

- Eiginleikinn styður aðeins vinnsluröðun. Ekki er tekið tillit til stillinga sem tengjast áætlanagerð aðgerðar við áætlanagerð burtséð frá aðferð áætlanagerðar í aðaláætlunum.
- Eiginleikinn styður aðeins ótakmarkaða getu.
- Þessi eiginleiki styður ekki virkni tilfangahleðslu.
- Eiginleikinn tekur ekki tillit til leiðarrýrnunar.
- Eiginleikinn styður einungis *Tímalengd* sem val aðaltilfangs.

Athugaðu að það er stöðugt verið að bæta eiginleikann *Ótakmörkuð afkastaáætlun fyrir fínstillingu skipulagningar*. Microsoft gerir ráð fyrir að innleiða stuðning við viðbótarstillingar fyrir áætlanagerð í komandi útgáfum.
