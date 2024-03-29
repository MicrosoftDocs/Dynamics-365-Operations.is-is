---
title: Taka frá í sömu runu fyrir sölupöntun
description: Í þessari grein er því lýst hvernig á að setja upp afurð til að leyfa frátekt birgða gagnvart einni runu í birgðum.
author: Henrikan
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResStorageDimensionGroup, EcoResTrackingDimensionGroup, InventBatch, InventModelGroup, PdsAskSameLotForm, PdsCustSellableDays, WHSReservationHierarchy, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.custom: 28911
ms.assetid: 5823d75e-f839-46dd-beb3-e09b79fc8aa4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0d4f3ee5d99648155e663c9ad0849b0b9ae3f80e
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7576617"
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

fyirr vörur sem eru tengdar hópi geymsluvíddar sem er með **Nota ferli vöruhúsastjórnunar** virkt er h ægt að taka frá tiltekni rununúmer með því að nota frátekningarstigveldi þar sem birgðarvíddir rununúmera eru skilgreind fyrir ofan staðsetningarvíddir. Þessi gerð frátektarstigveldis er einnig þekkt sem *Runa fyrir ofan \[staðsetningu\]* frátekningarstigveldi. Síðan **Runufrátekt** fyrir sölu- og flutningspöntunarlínur gerir þér einnig kleift að velja og panta margar línur miðað við fyrirliggjandi rununúmer. Frekari upplýsingar um það hvað þarf að gera ef notað er frátekningarstigveldi með lotunúmeravídd fyrir neðan staðsetningu (*Funa fyrir neðan \[staðsetningu\]*), skal sjá [Sveigjanleg frátektarregla á vídd vöruhúsastigs](../warehousing/flexible-warehouse-level-dimension-reservation.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
