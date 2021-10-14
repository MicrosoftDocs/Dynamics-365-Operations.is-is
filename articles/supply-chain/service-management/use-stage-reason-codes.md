---
title: Nota ástæðukóða stigs
description: Notaður er ástæðukóði til þess að gefa til kynna hvers vegna hætt hefur verið við þjónustustigssamning (SLA) eða hvers vegna þjónustupöntun hefur farið hefur verið framúr tímamörkum sem voru tilgreind í SLA.
author: kamaybac
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ac825fe96ee69491953bd50c758dde42744cea85
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573154"
---
# <a name="use-stage-reason-codes"></a>Nota ástæðukóða stigs 

[!include [banner](../includes/banner.md)]


Notaður er ástæðukóði til þess að gefa til kynna hvers vegna hætt hefur verið við þjónustustigssamning (SLA) eða hvers vegna þjónustupöntun hefur farið hefur verið framúr tímamörkum sem voru tilgreind í SLA.

Einnig er hægt að tilgreina að ástæðukóða sé krafist þegar hætt er við SLA eða þegar farið er yfir tímamörkin sem eru tilgreind í SLA fyrir þjónustupöntunina.

Ef búið er að tilgreina að ástæðukóða sé krafist, verður að færa inn ástæðukóða við eftirfarandi aðstæður:

  - Þegar þjónustupöntun er flutt á stig þar sem tímaskráningu er hætt, þvert á það sem kveðið er á um í SLA fyrir þjónustupöntunina.

  - Þegar þjónustupöntunin er staðfest.

  - Þegar tímaskráning er stöðvuð handvirkt.

## <a name="set-up-reason-codes"></a>Setja upp ástæðukóða

1.  Smelltu á **Þjónustukerfi** \> **Uppsetning** \> **Þjónustupantanir** \> **Stig ástæðukóðar**.

2.  Í skjámyndinni **Stig ástæðukóða** er smellt á **Nýtt** til að stofna nýjan ástæðukóða.

3.  Í reitnum **Stig ástæðukóða** skal slá inn einkvæmt stig ástæðukóða.

4.  Í reitnum **Lýsing** skal slá inn lýsingu á stigi ástæðukóða.

5.  Skjámyndinni er lokað til að vista breytingar.

## <a name="require-reason-codes-when-a-service-level-agreement-is-canceled"></a>Krefjast ástæðukóða þegar hætt er við þjónustustigssamning

1.  Smelltu á **Þjónustustjórnun** \> **Uppsetning** \> **Færibreytur þjónustustjórnunar**.

2.  Í skjámyndinni **Færibreytur þjónustustjórnunar** skal smella á tengilinn **Almennt** og velja síðan gátreitinn **Ástæðukóði afturköllunar**.

## <a name="require-reason-codes-when-the-a-service-order-exceeds-the-time-limit-that-is-set-by-the-service-level-agreement"></a>Krefjast ástæðukóða þegar þjónustupöntun fer fram úr settum tímamörkum í þjónustustigssamningi

1.  Smelltu á **Þjónustustjórnun** \> **Uppsetning** \> **Færibreytur þjónustustjórnunar**.

2.  Í skjámyndinni **Færibreytur þjónustustjórnunar** skal smella á tengilinn **Almennt** og velja síðan gátreitinn **Ástæðukóði fyrir að fara yfir á tíma**.

## <a name="see-also"></a>Sjá einnig

[Hefja og stöðva tímaskráningu fyrir þjónustupöntun](start-and-stop-time-recording-on-a-service-order.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]