---
title: Setja upp vöruhús fyrir flutningspantanir
description: Þessi grein lýsir því hvernig hægt er að setja upp vöruhús fyrir flutningspantanir.
author: Mirzaab
ms.date: 01/18/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocation,CustVendTransportPoint2Point
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 984f90343805d35833b7ddd1a175af5833c23dd5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905516"
---
# <a name="set-up-warehouses-for-transfer-orders"></a>Setja upp vöruhús fyrir flutningspantanir 

[!include [banner](../includes/banner.md)]

Nota má vöruhúsastig til að búa til þrepun sem styður pantanir á milli vöruhúsa. Miðað við þessa uppsetningu, reiknar aðalröðun vöruþörf á stöku vöruhúsaþrepi og gefur út flutningstillögur frá úthlutuðu upprunavöruhúsi til að uppfylla þær.

1.  Smella á **Birgðastjórnun > Uppsetning > Birgðasundurliðun > Vöruhús**.

2.  Velja vöruhúsið sem fylla skal á.

3.  Í flýtiflipanum **Aðaláætlanagerð** skal velja gátreitinn **Enduráfylling**.

4.  Á svæðinu **Aðalvöruhús** skal velja vöruhúsið sem á að úthluta sem vöruhús fyrir endurhleðslu. Aðalröðun reiknar út flutningsþörf fyrir valið vöruhús og býr til áætlaða flutningspöntun úr úthlutaða **Aðalvöruhúsinu**.
   
    > [!NOTE]
    > <P>Ef þú hreinsar gátreitinn <STRONG>Enduráfylling</STRONG> er völdu vöruhúsi úthlutað vöruhúsastigi í tengslum við <STRONG>Aðalvöruhús</STRONG>, en <STRONG>Aðalvöruhús</STRONG> er ekki uppsett sem vöruhús fyrir endurhleðslu.</P>

5.  Síðiunni er lokað til að nota nýju uppsetninguna.


> [!TIP]
> <P>Ef úthluta á vöruhúsi fyrir enduráfyllingu verður fyrst að setja upp vöruhúsið sem geymsluvídd á síðunni <STRONG>Geymsluvíddarflokkar</STRONG>. Á þessari síðu skal velja reitinn <STRONG>Virkt</STRONG> og reitinn <STRONG>Þekjuáætlun eftir vídd</STRONG> fyrir vöruhúsið.</P>

## <a name="set-up-transport-lead-time"></a>Setja upp afhendingartíma flutnings

Þú verður einnig að setja upp afhendingartíma flutnings milli vöruhúsanna á síðunni **Flutningsdagar**. 
1. Fara í **Birgðastjórnun > Uppsetning > Dreifing > Flutningsdagar**.
2. Í reitnum **Viðtökustaður** skal velja **vöruhús**.
3. Veljið **Sendingarvöruhús**, **Viðtökuvöruhús** og **Flutningsdagar**. 
4. (Valfrjálst) Einnig er hægt að stilla flutningstíma, fer allt eftir flutningsmáta, undir flipanum **Flutningsdagar eftir flutningsmáta**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]