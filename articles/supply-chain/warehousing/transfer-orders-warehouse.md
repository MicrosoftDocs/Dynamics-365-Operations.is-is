---
title: Setja upp vöruhús fyrir flutningspantanir
description: Þetta efnisatriði lýsir því hvernig hægt er að setja upp vöruhús fyrir flutningspantanir.
author: Mirzaab
manager: AnnBe
ms.date: 01/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 91db6e8f921bd674211f6d478b6d0f0a832c983c
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1847016"
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
