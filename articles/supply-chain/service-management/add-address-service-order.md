---
title: Bæta aðsetur við þjónustupöntun
description: Í þessu efnisatriði er útlistað hvernig bæta aðsetur viðskiptavinar í þjónustupöntunina.
author: ShylaThompson
manager: AnnBe
ms.date: 05/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 58188be6f82b6587011188379e5370b81f8fd114
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1570366"
---
# <a name="add-an-address-to-a-service-order"></a>Bæta aðsetur við þjónustupöntun    

[!include [banner](../includes/banner.md)]


Í þessu efnisatriði er útlistað hvernig bæta aðsetur viðskiptavinar í þjónustupöntunina. Þegar þjónustupöntun er stofnuð eru aðsetursupplýsingar fluttar frá verkinu sem þjónustupöntunin er tengd við. Hins vegar er hægt að velja aðra staðsetningu aðsetur sem þegar eru færðir inn í Microsoft Dynamics AX fyrir viðskiptavini, lánardrottna, setur, vöruhús, þjónustupantanir og verk.

Einnig er hægt að búa til nýtt aðsetur. Að sjálfgefnu nýja aðsetrið flutt í verkið. Hins vegar er hægt að tilgreina a‘ nýja aðsetrið er aðeins viðeigandi fyrir þetta tilvik þjónustu. Ef það er ekki gert er nýtt aðsetur er ekki flutt í verk.

## <a name="create-a-customer-address-for-a-service-order"></a>Búa til aðsetur viðskiptavinar fyrir þjónustupöntun

Fylgið eftirfarandi skrefum til að bæta við aðsetri þjónustupöntun:

1.  Smelltu á **Þjónustustjórnun** \> **Almennt** \> **Þjónustupantanir** \> **Þjónustupantanir**.

2.  Opnaðu þjónustupöntun sem þú vilt að búa til netfang fyrir.

3.  Á **Aðgerðarrúða**, smelltu á **Breyta** og smelltu síðan **Haus skoðun**.

4.  Á **Heimilisfang** flýtiflipi, smelltu á **Bæta við heimilisfangi**.

5.  Í **Nýtt heimilisfang** skjámynd, sláðu inn einkvæmt heiti fyrir heimilisfang og fylltu út í reitina sem eftir eru. 
    

    > [!WARNING]
    > <P>Ef sama heiti er fært inn sem fyrirliggjandi aðsetur, upplýsingarnar sem færðar eru inn í eftirstandandi reiti mun skrifa yfir upplýsingar um fyrirliggjandi aðsetur.</P>


6.  Smellið á **í lagi** til að afrita nýja aðsetrið á þjónustupöntunina.

## <a name="specify-an-alternative-address-on-a-service-order"></a>Aukaaðsetur tilgreint á þjónustupöntun

Til að bæta öðru aðsetri við þjónustupöntun, skal fylgja þessum skrefum:

1.  Smelltu á **Þjónustustjórnun** \> **Almennt** \> **Þjónustupantanir** \> **Þjónustupantanir**.

2.  Opnaðu þjónustupöntun sem þú vilt slá inn annað aðsetur fyrir.

3.  Á **Aðgerðarrúða**, smelltu á **Breyta** og smelltu síðan **Haus skoðun**.

4.  Á **Heimilisfang** flýtiflipi, smelltu á **Annað heimilisfang**.

5.  Í **Val á heimilisfangi** skjámyndinni, í reitnum **Færslugerð**, veldu **Þjónustupantanir**.

6.  Veljið aðsetur og smellið síðan á **í lagi** að afrita í þjónustupöntunina.


  


