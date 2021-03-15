---
title: Setja upp B2B svæði fyrir rafræn viðskipti
description: Í þessu efnisatriði er lýst hvernig skal setja upp B2B tengingu (tenging á milli fyrirtækja) á milli svæði fyrir rafræn viðskipti í Microsoft Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ac6f6511f4f96c00e10369329b2111a46f23d1a2
ms.sourcegitcommit: f9df202aefef761be52c0360b0e22da88773914c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035924"
---
# <a name="set-up-a-b2b-e-commerce-site"></a>Setja upp B2B svæði fyrir rafræn viðskipti

[!include [banner](../../includes/banner.md)]

B2B-svæði fyrir rafræn viðskipti bjóða upp á lykilmöguleika sem fínstilla verkflæði fyrir B2B-notendur. Í þessu efnisatriði er lýst hvernig skal setja upp B2B tengingu á milli svæði fyrir rafræn viðskipti í Microsoft Dynamics 365 Commerce. Það fer í gegnum einingar og stillingar svæða sem þarf að skilgreina til að virkja aðstæður sem tengjast B2B.

## <a name="prerequisites"></a>Forkröfur

- Til að setja upp B2B-svæði fyrir rafræn viðskipti þarf að virkja og skilgreina tiltekna eiginleika í Commerce Headquarters eins og lýst er í þessu efnisatriði.
- Meginupplifanir, t.d. uppgötvun afurðar, upplýsingasíða afurðar, karfan og greiðsluferlið, eru keyrðar af sömu einingunum sem notaðar eru fyrir B2B-svæði fyrir rafræn viðskipti. Síðuhöfundar ættu að þekja allar einingar sem Dynamics 365 Commerce styðja. Frekari upplýsingar er að finna á [Yfirlit einingasafns](../starter-kit-overview.md).
- Þetta efnisatriði gerir ráð fyrir að síðuhöfundar skilji grunnatriði við smíði viðskiptasvæðis, sniðmát, brot og síður þannig að þeir geti virkjað B2B-eiginleika fyrir svæði rafrænna viðskipta.

## <a name="site-level-settings"></a>Stillingar á svæðisstigi

Hægt er að fá aðgang að stillingum á svæðisstigi í svæðissmiðnum á **Stillingar svæðis \> Viðbætur**. Eftirfarandi tvær stillingar á svæðisstigi eiga við um B2B-aðstæður:

- **Virkja greiðslur viðskiptavinareiknings** – Þessi eiginleiki gerir notendum kleift að greiða fyrir pantanir með viðskiptavinareikningum. Tiltæk gildi eru **Virkjað fyrir B2B-viðskiptavini**, **Virkjað fyrir B2C-viðskiptavini**, **Virkjað fyrir alla viðskiptavini** og **Gert óvirkt fyrir alla viðskiptavini**. Ef B2B-svæðið styður viðskiptavinareikninga ætti að velja **Virkjað fyrir B2C-viðskiptavini**.
- **Virkja takmörk pöntunarmagns** – Þessi eiginleiki gerir þér kleift að stilla takmörk á fjölda vara sem hægt er að panta fyrir hverja afurð eða flokk. Tiltæk gildi eru **Virkjað fyrir B2B-viðskiptavini**, **Virkjað fyrir B2C-viðskiptavini**, **Virkjað fyrir alla viðskiptavini** og **Gert óvirkt fyrir alla viðskiptavini**.

> [!NOTE]
> Þegar uppfært er í nýjustu útgáfu einingasafnsins verður að fylgja viðbótarskrefum til að tryggja að áður lýstar svæðisstillingar séu í boði í umhverfinu. Frekari upplýsingar eru í [Uppfæra app.settings.json skrá](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="create-business-partner-sign-up-pages"></a>Búa til nýskráningarsíður samstarfsaðila

Til að gerast samstarfsaðili verða notendur fyrst að leggja inn beiðni sem samstarfsaðili. Tengill á beiðnisíðu samstarfsaðilans verður aðgengilegur á B2B-heimasíðunni þannig að notendur geta hafið ferlið. Þegar notendur hafa sent inn beiðni samstarfsaðila fá þeir staðfestingu um að beiðnin hafi verið send inn. 

### <a name="create-a-business-partner-request-page"></a>Búa til beiðnisíðu samstarfsaðila

Einingin **Nýskráning samstarfsaðila** á beiðnisíðu samstarfsaðila er notuð til að hefja beiðnir notenda um að gerast samstarfsaðilar. Þessi eining gerir þér kleift að safna notandaupplýsingum sem þarf fyrir nýskráningarferlið. Þar að auki er einingin **Aðsetur viðskiptavinareiknings** notuð til að sækja aðsetur notandans.

Til að setja upp og skilgreina beiðnisíðu samstarfsaðila í svæðissmiði skal fylgja þessum skrefum.

1. Búið til sniðmát sem heitir **Nýskráning**. Þetta sniðmát ætti að innihalda eftirfarandi einingar:

    - Skráning samstarfsaðila
    - Brauðmolalína
    - Haus
    - Síðufótur
    - Útilokun á efni
    - Textabálkur
    - Vörusafn

1. Nota skal sniðmátið **Nýskráning** til að stofna síðu sem heitir **Beiðni samstarfsaðila**.
1. Í bilinu **Haus** skal bæta við hausbroti sem er fyrirframskilgreint í hausasvæðinu.
1. Í bilinu **Neðanmál** skal bæta við neðanmálsbroti sem er fyrirframskilgreint í neðanmálssvæðinu.
1. Í bilinu **Aðal** skal bæta við einingunni **Hólf**. Á eiginleikasvæði einingarinnar skal stilla gildið **Breidd** á **Fylla hólf**.
1. Í bilinu **Hólf** skal bæta við einingunni **Brauðmylsna**. Í eiginleikasvæði einingarinnar, undir **Tenglar**, skal skilgreina tengil á heimasíðuna og slá inn **Heim** sem texta tengilsins.
1. Í bilinu **Hólf** skal bæta við einingunni **Nýskráning samstarfsaðila** fyrir neðan eininguna **Brauðmylsna**. Í eiginleikasvæði einingarinnar, undir **Fyrirsögn**, skal færa inn **Gerstu samstarfsaðili**.
1. Í bilinu **Nýskráning samstarfsaðila** skal bæta við einingunni **Aðsetur viðskiptavinareiknings**.
1. Í bilinu **Hólf** skal bæta við einingunni **Textabálkur** fyrir neðan eininguna **Nýskráning samstarfsaðila**. Hér er hægt að skilgreina suma skilmála og skilyrði fyrir skráningarferlið.
1. Veldu **Vista** og veldu síðan **Forskoðun** til að forskoða síðuna.
1. Veldu **Vista**, síðan **Ljúka við breytingar** til að skila síðunni og veldu síðan **Birta** til að birta hana.
1. Birtið vefslóð fyrir síðuna.

### <a name="create-a-business-partner-request-confirmation-page"></a>Búa til staðfestingarsíðu fyrir beiðni samstarfsaðila

Þegar beiðni samstarfsaðila er send inn, ætti staðfestingarsíða að birtast notandanum sem staðfestir innsendinguna. 

Til að setja upp og skilgreina staðfestingarsíðu beiðni í svæðissmið skal fylgja þessum skrefum.

1. Nota skal sniðmátið **Nýskráning** sem búið var til hér áður til að búa til síðu sem heitir **Staðfesting á beiðni samstarfsaðila**.
1. Í bilinu **Haus** skal bæta við hausbroti sem er fyrirframskilgreint í hausasvæðinu.
1. Í bilinu **Neðanmál** skal bæta við neðanmálsbroti sem er fyrirframskilgreint í neðanmálssvæðinu.
1. Í bilinu **Aðal** skal bæta við einingunni **Hólf**. Á eiginleikasvæði einingarinnar skal stilla gildið **Breidd** á **Fylla hólf**.
1. Í bilinu **Hólf** skal bæta við einingunni **Efnisbálkur**. Í eiginleikasvæði einingarinnar, undir **Fyrirsögn**, skal færa inn **Beiðni send inn**. Í reitinn **RTF-snið** skal slá inn **Beiðni þín var send**. Undir **Tenglar** skal skilgreina tengil á heimasíðuna og slá inn **Aftur í verslun** sem texta tengilsins.
1. Bætið við annarri **Hólfeiningu** og bætið **Vörusafnseiningu** við hana.
1. Skilgreinið eininguna **Vörusafn** með listanum yfir tillögur eða flokka sem á að sýna á síðunni.
1. Veldu **Vista** og veldu síðan **Forskoðun** til að forskoða síðuna.
1. Veldu **Vista**, síðan **Ljúka við breytingar** til að skila síðunni og veldu síðan **Birta** til að birta hana.
1. Birtið vefslóð fyrir síðuna.

Til að bæta tengli við staðfestingarsíðu beiðni í svæðissmið skal fylgja þessum skrefum.

1. Farið á síðuna **Beiðni samstarfsaðila** sem var búin til hér áður og veljið **Breyta**. 
1. Velja bileininguna **Nýskráning samstarfsaðila**. Á eiginleikasvæðinu, undir **Tengja við staðfestingarsíðu nýskráningar**, skilgreinið tengilinn á beiðnisíðu samstarfsaðila sem var búin til hér áður. 
1. Veldu **Vista**, síðan **Ljúka við breytingar** til að skila síðunni og veldu síðan **Birta** til að birta hana.

### <a name="add-a-business-partner-request-link-to-the-home-page"></a>Bæta tengli fyrir beiðni samstarfsaðila við heimasíðuna

Þegar beiðnisíða nýskráningar og staðfestingarsíða samstarfsaðila hafa verið búnar til þarf að gera nýskráningarsíðuna aðgengilega í gegnum tengil á heimasíðunni. Hægt er að ljúka þessu verki með því að bæta tenglinum við einhverja einingu **Efnisbálks** á heimasíðunni.

Til að bæta tengli á beiðni samstarfsaðila við heimasíðuna í svæðissmið skal fylgja þessum skrefum.

1. Farið á heimasíðu svæðisins og veljið **Breyta**.
1. Veljið bileininguna **Efnisbálkur**. Á eiginleikasvæði einingarinnar, undir **Tenglar**, skal skilgreina tengil á beiðnisíðu samstarfsaðila sem var búin til hér áður og slá inn **Skrá sig til að gerast samstarfsaðili** eða svipaðan texta sem texta tengilsins. Bætið við mynd ef það á við.
1. Veldu **Vista**, síðan **Ljúka við breytingar** til að skila síðunni og veldu síðan **Birta** til að birta hana.

## <a name="account-management-landing-page"></a>Lendingasíða fyrir stjórnun reikninga

Lendingarsíða reikningsstjórnunar inniheldur allar upplýsingar um stjórnun reiknings sem eru nauðsynlegar fyrir bæði B2B- og B2C-svæði rafrænna viðskipta. Aðeins innskráðir notendur geta skoðað þessa síðu.

Til að búa til og skilgreina B2B-lendingarsíðu reikningsstjórnunar í svæðissmið skal fylgja þessum skrefum.

1. Búið til sniðmát sem heitir **Stjórnun reikninga**. Þetta sniðmát ætti að innihalda eftirfarandi einingar:

    - Haus
    - Síðufótur
    - Brauðmolalína
    - Upphafsreitur reiknings
    - Almennur reitur reiknings
    - Reitur fyrir aðsetur reiknings
    - Reitur fyrir óskalista reiknings
    - Reitur fyrir aðsetur reiknings
    - Reitur fyrir vildarreikning
    - Reitur fyrir reikningsstöðu viðskiptavinar
    - Reitur pöntunarsniðmáts reiknings
    - Notendur í fyrirtæki
    - Fyrirtækjalisti
    - Staða reiknings viðskiptavinar
    - Pöntunarsniðmátslínur
    - Pöntunarsniðmátslisti
    - Reitur fyrir reikning
    - Reikningalisti
    - Upplýsingar um reikning

1. Nota skal sniðmátið **Reikningsstjórnun** til að búa til síðu sem heitir **Reikningurinn minn**.
1. Í bilinu **Haus** skal bæta við hausbroti sem er fyrirframskilgreint í hausasvæðinu.
1. Í bilinu **Neðanmál** skal bæta við neðanmálsbroti sem er fyrirframskilgreint í neðanmálssvæðinu.
1. Í bilinu **Aðal** skal bæta við einingunni **Hólf**. Á eiginleikasvæði einingarinnar skal stilla gildið **Breidd** á **Fylla hólf**. 
1. Í bilinu **Hólf** skal bæta við einingunni **Brauðmylsna**. Í eiginleikasvæði einingarinnar, undir **Tenglar**, skal skilgreina tengil á heimasíðuna og slá inn **Heim** sem texta tengilsins.
1. Í bilinu **Hólf** skal bæta við einingunni **Upphafsreitur**. Í eiginleikasvæði einingarinnar, undir **Fyrirsögn**, skal færa inn **Velkomin(n)**.
1. Í bilinu **Aðal** skal bæta við annarri **Hólfeiningu** (**Hólf 2**). Á eiginleikasvæði einingarinnar skal stilla gildið **Breidd** á **Fylla hólf**. Stillið gildið **Undireining sýnd** á **Tvo**. 
1. Í bilinu **Hólf 2** skal bæta við einingunni **Almennur reitur reiknings**. Í eiginleikasvæði einingarinnar, undir **Fyrirsögn**, skal færa inn **Notandaupplýsingar mínar**. Undir **Tenglar** skal skilgreina tengil á síðunni **Notandaupplýsingar mínar**. 
1. Í bilinu **Hólf 2** skal bæta við annarri einingu fyrir **Almennan reit reiknings**. Í eiginleikasvæði einingarinnar, undir **Fyrirsögn**, skal færa inn **Pantanaferill**. Undir **Tenglar** skal skilgreina tengil á síðu pantanaferils.
1. Í bilinu **Aðal** skal bæta við annarri **Hólfeiningu** (**Hólf 3**). Á eiginleikasvæði einingarinnar skal stilla gildið **Breidd** á **Fylla hólf**. Stillið gildið **Undireining sýnd** á **Tvo**. 
1. Í bilinu **Hólf 3** skal bæta við einingunni **Reitur fyrir aðsetur reiknings**. Í eiginleikasvæði einingarinnar, undir **Fyrirsögn**, skal færa inn **Aðsetur mitt**. Undir **Tenglar** skal skilgreina tengil á síðunni **Aðsetur mitt**. 
1. Í bilinu **Hólf 3** skal bæta við einingunni **Reitur fyrir óskalista reiknings**. Í eiginleikasvæði einingarinnar, undir **Fyrirsögn**, skal færa inn **Óskalistinn minn**. Undir **Tenglar** skal skilgreina tengil á síðunni **Óskalistinn minn**.
1. Í bilinu **Aðal** skal bæta við annarri **Hólfeiningu** (**Hólf 4**). Á eiginleikasvæði einingarinnar skal stilla gildið **Breidd** á **Fylla hólf**. Stillið gildið **Undireining sýnd** á **Tvo**. 
1. Í bilinu **Hólf 4** skal bæta við einingunni **Notendur í fyrirtæki**. Í eiginleikasvæði einingarinnar, undir **Fyrirsögn**, skal færa inn **Notendur í fyrirtæki**. 
1. Í bilinu **Hólf 4** skal bæta við einingunni **Reitur fyrir reikningsstöðu viðskiptavinar**. Í eiginleikasvæði einingarinnar, undir **Fyrirsögn**, skal færa inn **Inneign reiknings**. 
1. Í bilinu **Aðal** skal bæta við annarri **Hólfeiningu** (**Hólf 5**). Á eiginleikasvæði einingarinnar skal stilla gildið **Breidd** á **Fylla hólf**. Stillið gildið **Undireining sýnd** á **Tvo**. 
1. Í eininguna **Hólf 5** skal bæta við einingunni **Reitur pöntunarsniðmáts reiknings**. Í eiginleikasvæði einingarinnar, undir **Fyrirsögn**, skal færa inn **Pöntunarsniðmát**. 
1. Veldu **Vista**, síðan **Ljúka við breytingar** til að skila síðunni og veldu síðan **Birta** til að birta hana.

> [!NOTE] 
> Sumir hlutarnir sem bætt var við í skrefum 13 til 18 birtast ekki á vinnusvæðinu „það sem þú sérð er það sem þú færð“ í svæðissmið vegna þess að þeir þurfa innskráðan B2B-reikning.

## <a name="create-and-configure-customer-balance-pages-and-modules"></a>Búa til og skilgreina síður einingar fyrir stöðu viðskiptavinar 

Hægt er að nota reikninga viðskiptavina til að greiða fyrir pantanir. Hægt er að skoða tiltæka stöðu á viðskiptavinareikningi á reikningsstjórnunarsíðu notanda.

### <a name="create-a-customer-balance-page"></a>Búa til síðu yfir stöðu viðskiptavinar 

Áður en innskráðir B2B-notendur geta skoðað viðskiptavinastöðuna sína þarf að búa til síðu yfir stöðu viðskiptavinar. 

Til að búa til sérsniðna síðu yfir stöðu í svæðissmið skal fylgja þessum skrefum.

1. Nota skal sniðmátið **Reikningsstjórnun** sem búið var til hér áður til að búa til síðu sem heitir **Staða viðskiptavinar**.
1. Í bilinu **Haus** skal bæta við hausbroti sem er fyrirframskilgreint í hausasvæðinu.
1. Í bilinu **Neðanmál** skal bæta við neðanmálsbroti sem er fyrirframskilgreint í neðanmálssvæðinu.
1. Í bilinu **Aðal** skal bæta við annarri **Hólfeiningu** (**Hólf 3**). Á eiginleikasvæði einingarinnar skal stilla gildið **Breidd** á **Fylla hólf**. Stillið gildið **Undireining sýnd** á **Tvo**.
1. Í bilinu **Hólf** skal bæta við einingunni **Brauðmylsna**. Í eiginleikasvæði einingarinnar, undir **Tenglar** skal skilgreina tengil á lendingarsíðu reikningsstjórnunar og færa inn **Reikningurinn minn** sem texta tengilsins.
1. Í bilið **Hólf** skal bæta við einingunni **Reikningsstaða viðskiptavinar**. Í eiginleikasvæði einingarinnar, undir **Fyrirsögn**, skal færa inn **Reikningsstaða**.
1. Veldu **Vista**, síðan **Ljúka við breytingar** til að skila síðunni og veldu síðan **Birta** til að birta hana.
1. Birtið vefslóð fyrir síðuna.
1. Farið á lendingarsíðu reikningsstjórnunar (**Reikningurinn minn**) sem var búin til hér áður.
1. Í eiginleikasvæðinu fyrir eininguna **Reitur fyrir reikningsstöðu viðskiptavinar** skal bæta tengli við síðu yfir stöðu viðskiptavinar. 
1. Vista og birta síðuna.

Síða yfir stöðu viðskiptavinar hefur nú verið búin til og notendur geta opnað hana á lendingarsíðu reikningsstjórnunar.

### <a name="configure-a-checkout-page-so-that-the-customer-balance-can-be-used-as-a-form-of-payment"></a>Skilgreina greiðslusíðu þannig að hægt sé að nota stöðu viðskiptavinar sem greiðsluleið

Þörf er á einingunni **Greiðsla með viðskiptavinareikningi** til að virkja stöðu viðskiptavinar svo hægt sé að nota hana sem greiðsluleið. Þessari einingu ætti að bæta við greiðslusíðuna sem greiðsluleið. Upplýsingar um hvernig skilgreina á greiðslusíðu og einingarnar sem þarf fyrir greiðsluferlið, þ.m.t. allar greiðsluupplýsingar, er að finna í [Greiðsluferliseining](../add-checkout-module.md).

Þegar búið er að skilgreina greiðslusíðu, þarf að bæta einingunni **Greiðsla með viðskiptavinareikningi** við greiðsluhlutann og síðan vista og birta síðuna. B2B-notendur geta þá skráð sig inn á svæði fyrir rafræn viðskipti og notað tiltæka viðskiptavinastöðu í pantanir í greiðsluferlinu.

Þar að auki, í **Svæðissmið \> Viðbætur**, þarf að ganga úr skugga um að eiginleikinn **Virkja greiðslur viðskiptavinareiknings** sé stilltur á **Virkjað fyrir B2B-viðskiptavini**.

## <a name="create-order-template-pages"></a>Búa til síður pöntunarsniðmáts

Hægt er að setja upp tvær síður pöntunarsniðmáts fyrir B2B-svæði rafrænna viðskipta: listasíðu pöntunarsniðmáta og síðu pöntunarsniðmátslína.

Listasíða pöntunarsniðmáta sýnir lista yfir öll pöntunarsniðmát sem eru í boði. Hún er sett upp með því að nota eininguna **Listi pöntunarsniðmáta**. Listasíða pöntunarsniðmáta gerir þér kleift að búa til og eyða sniðmáti og bæta vörum í sniðmáti við körfuna.

Síða pöntunarsniðmátslína sýnir upplýsingar um pöntunarsniðmátið sem er valið á listasíðu pöntunarsniðmáta. Hún er sett upp með því að velja eininguna **Pöntunarsniðmátslínur**. Þegar notandi velur heiti sniðmáts á listasíðu pöntunarsniðmáta, birtist síða pöntunarsniðmátslína og sýnir upplýsingar um sniðmátið. Notandinn getur þá skoðað og breytt vörunum í sniðmátinu.

### <a name="create-an-order-templates-list-page"></a>Búa til listasíðu pöntunarsniðmáta

Til að búa til listasíðu pöntunarsniðmáta í svæðissmið skal fylgja þessum skrefum.

1. Nota skal sniðmátið **Reikningsstjórnun** sem búið var til hér áður til að búa til síðu sem heitir **Pöntunarsniðmát**.
1. Í bilinu **Haus** skal bæta við hausbroti sem er fyrirframskilgreint í hausasvæðinu.
1. Í bilinu **Neðanmál** skal bæta við neðanmálsbroti sem er fyrirframskilgreint í neðanmálssvæðinu.
1. Í bilinu **Aðal** skal bæta við einingunni **Hólf**. Á eiginleikasvæði einingarinnar skal stilla gildið **Breidd** á **Fylla hólf**.
1. Í bilinu **Hólf** skal bæta við einingunni **Brauðmylsna**. Í eiginleikasvæði einingarinnar, undir **Tenglar** skal skilgreina tengil á lendingarsíðu reikningsstjórnunar og færa inn **Reikningurinn minn** sem texta tengilsins.
1. Í bilinu **Hólf** skal bæta við einingunni **Listi pöntunarsniðmáta**.
1. Veldu **Vista**, síðan **Ljúka við breytingar** til að skila síðunni og veldu síðan **Birta** til að birta hana.
1. Birtið vefslóð fyrir síðuna.
1. Farið á lendingarsíðu reikningsstjórnunar (**Reikningurinn minn**) sem var búin til hér áður.
1. Í eiginleikasvæðinu fyrir eininguna **Reitur pöntunarsniðmáts reiknings**, undir **Tenglar**, skal skilgreina tengil á listasíðu pöntunarsniðmáta sem var verið að búa til.
1. Vista og birta síðuna.

Listasíða pöntunarsniðmáta hefur nú verið búin til og notendur geta opnað hana á lendingarsíðu reikningsstjórnunar.

### <a name="create-an-order-template-lines-page"></a>Búa til síðu pöntunarsniðmátslína

Til að búa til síðu pöntunarsniðmátslína í svæðissmið skal fylgja þessum skrefum.

1. Nota skal sniðmátið **Reikningsstjórnun** sem búið var til hér áður til að búa til síðu sem heitir **Pöntunarsniðmátslínur**.
1. Í bilinu **Haus** skal bæta við hausbroti sem er fyrirframskilgreint í hausasvæðinu.
1. Í bilinu **Neðanmál** skal bæta við neðanmálsbroti sem er fyrirframskilgreint í neðanmálssvæðinu.
1. Í bilinu **Aðal** skal bæta við einingunni **Hólf**. Á eiginleikasvæði einingarinnar skal stilla gildið **Breidd** á **Fylla hólf**.
1. Í bilinu **Hólf** skal bæta við einingunni **Brauðmylsna**. Í eiginleikasvæði einingarinnar, undir **Tenglar** skal skilgreina tengil á lendingarsíðu reikningsstjórnunar og færa inn **Reikningurinn minn** sem texta tengilsins.
1. Í bilinu **Hólf** skal bæta við einingunni **Pöntunarsniðmátslínur**.
1. Veldu **Vista**, síðan **Ljúka við breytingar** til að skila síðunni og veldu síðan **Birta** til að birta hana.
1. Birtið vefslóð fyrir síðuna.

## <a name="onboard-business-partner-users"></a>Taka inn notendur samstarfsaðila

Síða fyrirtækisnotenda gerir stjórnanda samstarfsaðilafyrirtækis kleift að taka fleiri notendur úr því fyrirtæki inn á B2B-svæði rafrænna viðskipta. Hún er sett upp með því að nota eininguna **Fyrirtækjalisti**. Á síðu fyrirtækisnotenda getur stjórnandi bætt við eða fjarlægt notendur, skilgreint reikningsstöður og beðið um yfirlit fyrir notanda.

Til að búa til síðu fyrirtækisnotenda í svæðissmið skal fylgja þessum skrefum.

1. Nota skal sniðmátið **Reikningsstjórnun** sem búið var til hér áður til að búa til síðu sem heitir **Notendur í fyrirtæki**.
1. Í bilinu **Haus** skal bæta við hausbroti sem er fyrirframskilgreint í hausasvæðinu.
1. Í bilinu **Neðanmál** skal bæta við neðanmálsbroti sem er fyrirframskilgreint í neðanmálssvæðinu.
1. Í bilinu **Aðal** skal bæta við einingunni **Hólf**. Á eiginleikasvæði einingarinnar skal stilla gildið **Breidd** á **Fylla hólf**.
1. Í bilinu **Hólf** skal bæta við einingunni **Brauðmylsna**. Í eiginleikasvæði einingarinnar, undir **Tenglar** skal skilgreina tengil á lendingarsíðu reikningsstjórnunar og færa inn **Reikningurinn minn** sem texta tengilsins.
1. Í bilinu **Hólf** skal bæta við einingunni **Fyrirtækjalisti**. Í eiginleikasvæði einingarinnar, undir **Fyrirsögn**, skal færa inn **Notendur í fyrirtæki**.
1. Í eiginleikasvæði einingarinnar **Fyrirtækjalisti** skal virkja eiginleikana **Töfluröðun** og **Síðuskiptingu töflu**. Stillið síðuskiptingu töflunnar á **5**.
1. Veldu **Vista**, síðan **Ljúka við breytingar** til að skila síðunni og veldu síðan **Birta** til að birta hana.
1. Birtið vefslóð fyrir síðuna.
1. Farið á lendingarsíðu reikningsstjórnunar (**Reikningurinn minn**) sem var búin til hér áður.
1. Í eiginleikasvæðinu fyrir eininguna **Reitur fyrirtækisnotenda**, undir **Tenglar**, skal skilgreina tengil á síðu fyrirtækisnotenda sem var verið að búa til. 
1. Veldu **Vista**, síðan **Ljúka við breytingar** til að skila síðunni og veldu síðan **Birta** til að birta hana.

## <a name="create-invoice-pages"></a>Stofna reikningsíður

Listasíða reikninga sýnir lista yfir alla tiltæka reikninga. Hún er sett upp með því að nota eininguna **InvoicesList**. Á listasíðu reikninga geta notendur greitt eða óskað eftir reikningum. 

Upplýsingasíða reiknings sýnir upplýsingar um reikninginn sem valinn er á listasíðu reikninga. Hún er sett upp með því að nota eininguna **Upplýsingar um reikning**. Þegar notandi velur reikningskenni á listasíðu reikninga, þá birtist upplýsingasíða reikningsins og sýnir upplýsingar um reikninginn.

### <a name="create-an-invoices-list-page"></a>Stofna reikningslistsíðu

Til að búa til listasíðu reikninga í svæðissmið skal fylgja þessum skrefum.

1. Nota skal sniðmátið **Reikningsstjórnun** sem búið var til hér áður til að búa til síðu sem heitir **Reikningalisti**.
1. Í bilinu **Haus** skal bæta við hausbroti sem er fyrirframskilgreint í hausasvæðinu.
1. Í bilinu **Neðanmál** skal bæta við neðanmálsbroti sem er fyrirframskilgreint í neðanmálssvæðinu.
1. Í bilinu **Aðal** skal bæta við einingunni **Hólf**. Á eiginleikasvæði einingarinnar skal stilla gildið **Breidd** á **Fylla hólf**.
1. Í bilinu **Hólf** skal bæta við einingunni **Brauðmylsna**. Í eiginleikasvæði einingarinnar, undir **Tenglar** skal skilgreina tengil á lendingarsíðu reikningsstjórnunar og færa inn **Reikningurinn minn** sem texta tengilsins.
1. Í bilinu **Hólf** skal bæta við einingunni **InvoicesList**. Í eiginleikasvæði einingarinnar, undir **Fyrirsögn**, skal færa inn **Reikningar**.
1. Veldu **Vista**, síðan **Ljúka við breytingar** til að skila síðunni og veldu síðan **Birta** til að birta hana.
1. Birtið vefslóð fyrir síðuna.
1. Farið á lendingarsíðu reikningsstjórnunar (**Reikningurinn minn**) sem var búin til hér áður.
1. Í eiginleikasvæðinu fyrir eininguna **Reitur reikninga**, undir **Tenglar**, skal skilgreina tengil á listasíðu reikninga sem var verið að búa til. 
1. Veldu **Vista**, síðan **Ljúka við breytingar** til að skila síðunni og veldu síðan **Birta** til að birta hana.

### <a name="create-an-invoice-details-page"></a>Stofna reikningsupplýsingasíðu

Til að búa til upplýsingasíðu reiknings í svæðissmið skal fylgja þessum skrefum.

1. Nota skal sniðmátið **Reikningsstjórnun** sem búið var til hér áður til að búa til síðu sem heitir **Upplýsingar um reikning**.
1. Í bilinu **Haus** skal bæta við hausbroti sem er fyrirframskilgreint í hausasvæðinu.
1. Í bilinu **Neðanmál** skal bæta við neðanmálsbroti sem er fyrirframskilgreint í neðanmálssvæðinu.
1. Í bilinu **Aðal** skal bæta við einingunni **Hólf**. Á eiginleikasvæði einingarinnar skal stilla gildið **Breidd** á **Fylla hólf**.
1. Í bilinu **Hólf** skal bæta við einingunni **Brauðmylsna**. Í eiginleikasvæði einingarinnar, undir **Tenglar** skal skilgreina tengil á lendingarsíðu reikningsstjórnunar og færa inn **Reikningurinn minn** sem texta tengilsins. Síðan skal skilgreina tengil á listasíðu reikninga og færa inn **Listar yfir reikninga** sem texta tengilsins.
1. Í bilinu **Hólf** skal bæta við einingunni **Upplýsingar um reikning**.
1. Veldu **Vista**, síðan **Ljúka við breytingar** til að skila síðunni og veldu síðan **Birta** til að birta hana.
1. Birtið vefslóð fyrir síðuna.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit einingasafns](../starter-kit-overview.md)

[Síðuyfirlit höfunda](../authoring-home-overview.md)

[Yfirlit yfir sniðmát og útlit](../templates-layouts-overview.md)

[Vinna með brot](../work-with-fragments.md)

[Bæta við nýrri síðu á svæði](../add-new-page.md)

[Greiðsluferliseining](../add-checkout-module.md)

[Eining fyrir bálk með efni](../add-hero-module.md)

[Vörusafn](../product-collection-module-overview.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]