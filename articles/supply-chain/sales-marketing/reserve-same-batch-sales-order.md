---
title: Taka frá í sömu runu fyrir sölupöntun
description: Í þessari grein er því lýst hvernig á að setja upp afurð til að leyfa frátekt birgða gagnvart einni runu í birgðum.
author: omulvad
manager: tfehr
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResStorageDimensionGroup, EcoResTrackingDimensionGroup, InventBatch, InventModelGroup, PdsAskSameLotForm, PdsCustSellableDays
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 28911
ms.assetid: 5823d75e-f839-46dd-beb3-e09b79fc8aa4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f1e101473c5b6958c7e0fb5c5fa80dccd3d9b467
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216023"
---
# <a name="reserve-the-same-batch-for-a-sales-order"></a>Taka frá í sömu runu fyrir sölupöntun

[!include [banner](../includes/banner.md)]

Í þessari grein er því lýst hvernig á að setja upp afurð til að leyfa frátekt birgða gagnvart einni runu í birgðum.

Frátekning í sömu runu gerir kleift að taka frá birgðir fyrir sölupöntunarlínu gagnvart einni runu birgða. Til dæmis, viðskiptavinur sem pantar veggfóður getur beðið um að öll pöntunin sé fyllt úr sömu runu eða lotu til að forðast ósamræmi milli veggfóðursrúllanna. Til að setja upp vöru sem nota á frátekningu úr sömu runu þurfa eftirfarandi°stillingar að vera virkar í vörulíkanaflokki, rakningarvíddarflokki og geymsluvíddaflokk sem er úthlutað á afurðina:

- **Vörulíkanaflokkar** – Vörulíkanaflokkurin verður að hafa **Val á sömu runu** og **Sameina kröfu** svæðin valin í **Frátekning** svæðaflokki fyrir birgðareglur.
- **Flokkar rakningarvídda** – Rakningarvíddaflokkurinn verður að hafa **Þekjuáætlun eftir vídd** svæði valið fyrir rununúmerið.
- **Flokkar geymsluvídda** – Geymsluvíddarflokkurinn verður að hafa **Þekjuáætlun eftir vídd** svæði valin fyrir **Svæði** og **Vöruhús**.

Þegar teknar eru frá birgðir fyrir vöru á sölupöntunarlínu sem er sett upp fyrir val á sömu runu, reynir kerfið að taka pantaða magnið úr einni birgðarunu. Allar sértækar runueigindakröfur eru einnig skoðaðar. Ef ekki er hægt að fylla magn úr einni runu birtist **Árekstrar í frátekningu sömu runu** síða°. Þessi síða lýsir vandamálunum og einnig aðgerðunum sem hægt er að framkvæma°til að halda áfram með frátekningu. Eftirfarandi aðstæður gætu komið í veg fyrir frátekningu runu:

- Ráðstöfunarkóði runu hefur **Hindra frátekningu** fyrir sölu merkt með flaggi sem **Hindra**.
- Runuvinnslan er útrunnin, byggt á lokadegi og öllum viðeigandi seljanlegum dögum til viðskiptavina. Varan getur enn verið hugsanleg til frátekningar ef vörulíkanaflokkur fyrir vöruna er „Fyrsti Lokadagur Fyrst Út“ (FEFO) dagsetningarstýrður og ef best-fyrir dagsetningin er valin sem skilyrði í tiltekt.
- Runuvinnslan hefur ekki nægilega langan endingartíma eftir, á grundvelli lokadagsetningar og best-fyrir dagsetningar plús seljanlega daga til viðskiptavina.

Fyrir hluti sem tengjast geymsluvíddarhóp sem hefur **Nota ferli vöruhúsastjórnunar** virkt geturðu pantað ákveðin rununúmer með því að nota pöntunarveldi með birgðafjölda rununúmersins skilgreint fyrir ofan staðsetningarvíddina. Síðan **Runufrátekt** fyrir sölu- og flutningspöntunarlínur gerir þér einnig kleift að velja og panta margar línur miðað við fyrirliggjandi rununúmer. Fyrir frekari upplýsingar um hvað á að gera ef þú notar frátekningarstigveldi sem hefur rununúmervíddina fyrir neðan staðsetningu, sjá [Sveigjanleg stefna fyrir vöruvíddarstærð fyrirvara](../warehousing/flexible-warehouse-level-dimension-reservation.md).
