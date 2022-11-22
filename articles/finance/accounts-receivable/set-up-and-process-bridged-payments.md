---
title: Uppsetning og vinnsla greiðslna á millilykli
description: Þessi grein útskýrir hvernig á að setja upp og vinna brúaðar greiðslur viðskiptavina. Brúguð greiðsla er greiðsla sem er bókuð í aðalbók í tveimur þrepum.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPaymMode, VendPaymMode, LedgerJournalTable, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, LedgerJournalTransDaily
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bb563008f156e1bfa6e4e9a705e9170342719ce7
ms.sourcegitcommit: 9740f9b41a7dcf1821c6baccb2e05b9865ac2966
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/15/2022
ms.locfileid: "9775169"
---
# <a name="set-up-and-process-bridged-payments"></a>Uppsetning og vinnsla greiðslna á millilykli

[!include [banner](../includes/banner.md)]

Brúguð greiðsla er greiðsla sem er bókuð í aðalbók í tveimur þrepum. Venjulega er þessi aðferð notuð þegar greiðslumáti er stilltur á **Banki**, og þú verður að bóka færslur á bankareikninginn aðeins þegar færslan hefur hreinsað bankann. Hins vegar geturðu líka notað það fyrir fjárhagsreikning. Í þessu tilviki verður upphæðin færð af einum aðalreikningi yfir á annan aðalreikning þegar brúarbókunin er afgreidd.

Þú getur búið til brúaðar greiðslur úr annað hvort viðskiptaskuldum eða viðskiptakröfum. Þó að þessi grein útskýri hvernig á að stilla brúarbókun fyrir viðskiptakröfur, eru skrefin fyrir viðskiptaskuldafærslur svipuð.

## <a name="set-up-bridging-posting"></a>Settu upp brúarfærslu

Til að nota brúarfærslu verður þú að setja upp eina eða fleiri greiðslumáta þannig að þeir noti **Brúarpóstur** aðferð. Þú verður þá að velja brúarreikning.

1. Fara til **Reikningur fáanlegur&gt; Uppsetning greiðslu&gt; Greiðslumáti**.
2. Veldu núverandi greiðslumáta til að virkja brúarfærslu fyrir. Einnig er hægt að búa til nýjan greiðslumáta.
3. Veldu **Brúarpóstur** gátreit.
4. Í **Brúarreikningur** reit, veldu aðalreikninginn sem greiðslur eiga að bóka á áður en þær eru jafnaðar á bankareikninginn.
5. Lokið síðunni.

## <a name="process-and-transfer-bridging-posting"></a>Vinna og flytja brúarfærslu

Til að búa til og vinna úr brúarfærslu skaltu fylgja þessum skrefum.

1. Farið í **Viðskiptakröfur &gt; Greiðslur &gt; Greiðslubók viðskiptavinar**.
2. Veljið **Ný** til að stofna færslubók.
3. Í **Nafn** reit, veldu nafn.
4. Bættu línum við greiðslubók viðskiptavinar og veldu greiðslumáta sem er stilltur fyrir brúarbókun.
5. Bóka færslubókina. Færslurnar verða færðar á aðalreikninginn sem þú valdir í **Brúarreikningur** reit í fyrri aðferð.

Þegar færslurnar hafa hreinsað bankann og þú vilt færa greiðsluna af brúarreikningnum yfir á greiðslureikninginn sem er tilgreindur fyrir greiðslumáta skaltu fylgja þessum skrefum.

1. Farðu í **Fjárhag &gt; Færslubókarfærslur &gt; Almennar færslubækur**.
2. Veljið **Ný** til að stofna færslubók.
3. Í **Nafn** reit, veldu nafn.
4. Veldu **Línur** til að opna dagbókarupplýsingarnar.
5. Veldu **Aðgerðir&gt; Veldu brúaðar færslur**.
6. Merktu við hverja greiðslu sem hefur verið hreinsuð og veldu síðan **Taka**.
7. Bóka færslubókina.
