---
title: Bæta heimilisfangi við þjónustupöntun
description: Í þessari grein er útlistað hvernig má bæta aðsetri viðskiptavinar í þjónustupöntunina.
author: sorenva
ms.date: 06/15/2020
ms.topic: article
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c485c50bab7c2e945aa0f0fc0601008dcebd3328
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015726"
---
# <a name="add-an-address-to-a-service-order"></a>Bæta heimilisfangi við þjónustupöntun

[!include [banner](../includes/banner.md)]

Í þessari grein er útlistað hvernig má bæta aðsetri viðskiptavinar í þjónustupöntunina. Þegar þjónustupöntun er stofnuð eru aðsetursupplýsingar fluttar frá verkinu sem þjónustupöntunin er tengd við. Hins vegar er hægt að velja aðra staðsetningu aðsetur sem þegar eru færðir inn í Microsoft Dynamics AX fyrir viðskiptavini, lánardrottna, setur, vöruhús, þjónustupantanir og verk.

Einnig er hægt að búa til nýtt aðsetur. Að sjálfgefnu nýja aðsetrið flutt í verkið. Hins vegar er hægt að tilgreina a‘ nýja aðsetrið er aðeins viðeigandi fyrir þetta tilvik þjónustu. Ef það er ekki gert er nýtt aðsetur er ekki flutt í verk.

## <a name="create-a-customer-address-for-a-service-order"></a>Búa til aðsetur viðskiptavinar fyrir þjónustupöntun

Fylgið eftirfarandi skrefum til að bæta við aðsetri þjónustupöntun:

1. Velji **Þjónustustjórnun** \> **Þjónustupantanir** \> **Þjónustupantanir**.

1. Opnaðu þjónustupöntun sem þú vilt að búa til netfang fyrir.

1. Opnaðu flipann **Haus**.

1. Stækkaðu flýtiflipann **Aðsetur** og veldu síðan **Bæta við aðsetri** af tækjastiku flýtiflipans.

1. Í **Nýtt heimilisfang** skjámynd, sláðu inn einkvæmt heiti fyrir heimilisfang og fylltu út í reitina sem eftir eru. 

    > [!WARNING]
    > Ef sama heiti er fært inn sem fyrirliggjandi aðsetur, upplýsingarnar sem færðar eru inn í eftirstandandi reiti mun skrifa yfir upplýsingar um fyrirliggjandi aðsetur.

1. Veldu **Í lagi** til að afrita nýja heimilisfangið á þjónustupöntunina.

## <a name="specify-an-alternative-address-on-a-service-order"></a>Aukaaðsetur tilgreint á þjónustupöntun

Til að bæta öðru aðsetri við þjónustupöntun, skal fylgja þessum skrefum:

1. Velji **Þjónustustjórnun** \> **Þjónustupantanir** \> **Þjónustupantanir**.

1. Opnaðu þjónustupöntun sem þú vilt slá inn annað aðsetur fyrir.

1. Opnaðu flipann **Haus**.

1. Stækkaðu flýtiflipann **Aðsetur** og veldu síðan **Annað aðsetur** af tækjastiku flýtiflipans.

1. Í svarglugganum **Aðsetursval** skal velja **Þjónustupantanir** úr fellilistanum fyrir ofan hnitanetið.

1. Veljið aðsetur og veljið síðan **Í lagi** að afrita það í þjónustupöntunina.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]