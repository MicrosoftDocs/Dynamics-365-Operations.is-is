---
title: Setja upp númeraraðir fyrir smásöluuppgjör
description: Þessi grein lýsir því hvernig á að stilla númeraraðirnar sem eru nauðsynlegar fyrir smásöluyfirlit í Microsoft Dynamics 365 Commerce.
author: analpert
ms.date: 04/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: analpert
ms.search.validFrom: 2022-04-12
ms.openlocfilehash: 5c4eb872ec2151a9f4ac5462ad43dd03a6705487
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880004"
---
# <a name="set-up-number-sequences-for-retail-statements"></a>Setja upp númeraraðir fyrir smásöluuppgjör

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Þessi grein lýsir því hvernig á að stilla númeraraðirnar sem eru nauðsynlegar fyrir smásöluyfirlit í Microsoft Dynamics 365 Commerce.

Tvær tegundir smásöluyfirlita eru notaðar í Dynamics 365 Commerce: 

- **Viðskiptayfirlýsingar** er ætlað að búa til og birta með mikilli tíðni. Þau eru notuð til að bóka allar ófjárhagslegar færslur í versluninni á Dynamics 365 Commerce höfuðstöðvar. 
- **Ársreikningur** er ætlað að búa til og birta einu sinni á virkum degi. Þær innihalda aðeins lokaðar vaktir frá smásöluverslunum sem hafa verið hlaðið upp í höfuðstöðvar Commerce í gegnum p-starfið.

## <a name="configure-a-number-sequence-for-statement-posting"></a>Stilltu númeraröð fyrir færslu yfirlits

Eftir að þú hefur lokið við uppsetningu smásöluverslunar, í höfuðstöðvum Commerce, verður þú að stilla einstaka númeraröð sem verður notuð fyrir yfirlýsingar meðan á stofnun yfirlýsingarinnar stendur.

Til að stilla númeraröð fyrir birtingu yfirlits í höfuðstöðvum Commerce skaltu fylgja þessum skrefum.

1. Farðu á **Fyrirtækisstjórnun \> Númeraröð \> Númeraröð**.
1. Veldu **Nýtt \> Númeraröð** til að búa til nýtt met.
1. Á **Auðkenning** flýtiflipann, í **Númeraraðarkóði** reit, sláðu inn númerarunarkóða.
1. Í **Nafn númeraraðar** reit, sláðu inn nafn.
1. Á **Umfangsbreytur** flýtiflipann, í **Umfang** reit, veldu **Rekstrareining**.
1. Í **Rekstrareining** reit, veldu verslunina sem númeraröðin verður notuð fyrir.
1. Á **Hluti** Flýtiflipi, skilgreindu hlutina.
1. Á **Heimildir** flýtiflipann, stilltu **Svæði** sviði til **Smásöluverslun**.
1. Stilltu **Tilvísun** sviði til **Yfirlitsnúmer**, og veldu síðan **Allt í lagi**.

    ![Auðkenning, Umfangsfæribreytur, Hlutir og Tilvísanir flýtiflipar á síðunni Númeraraðir.](media/retail-statements-num-seq-setup-01.png)

1. Á **Almennt** flýtiflipann, í **Númeraúthlutun** kafla, uppfærðu **Minnstu** og **Stærsta** reiti þannig að þeir passi við lengd **Alfatölulegt** hluti sem þú skilgreindir á **Hluti** Flýtiflipi.
1. Á **Frammistaða** flýtiflipann, við mælum með að þú stillir **Forúthlutun** valmöguleika til **Já** og **Magn af tölum** sviði til **25**.

    ![Almennar og afköst flýtiflipar á síðunni Númeraraðir.](media/retail-statements-num-seq-setup-02.png)

1. Á aðgerðarrúðunni velurðu **Vista** til að vista breytingarnar og loka síðunni.
