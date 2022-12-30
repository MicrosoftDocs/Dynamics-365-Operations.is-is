---
title: Innkaup
description: Þessi grein útskýrir innkaup í Eignastýringu.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderPurchaseListPagePreviewPane, EntAssetWorkOrderPurchaseListPage, EntAssetWorkOrderPurchaseLineAmountInfoPart, EntAssetWorkOrderPurchReqListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6e41a28ec922924b0ef86858a881280fd44bfe63
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/15/2022
ms.locfileid: "9014953"
---
# <a name="procurement"></a>Innkaup

[!include [banner](../../includes/banner.md)]

Í eignastjórnun geturðu fengið yfirlit yfir innkaupabeiðnir og innkaupapantanir sem tengjast verkbeiðnum. Einnig er hægt að stofna innkaupapöntun eða innkaupabeiðni úr verkbeiðni.

Listasíðan **Innkaupabeiðni verkbeiðni** (**Eignastýring** > **Innkaup** > **Innkaupabeiðni verkbeiðni**) sýnir lista yfir innkaupabeiðnir sem tengjast verkbeiðnum. Þegar þú velur vinnslu verkbeiðni á þessari síðu geturðu notað hnappana í hópnum **Sýna** á aðgerðarúðuflipanum **Innkaupabeiðni verkbeiðni** til að framkvæma ýmsar aðgerðir:

- Til að opna tengda innkaupabeiðni skaltu velja **Innkaupabeiðni**. 
- Til að opna tengda verkbeiðni skaltu velja **Verkbeiðni**.
- Til að fá yfirlit sem sýnir hvar hluturinn á völdum línum er notaður í tengslum við eignir, vanskil tegunda viðhaldsverka, varahluti og verkbeiðnir í eignastýringu velurðu **Notkunarstaður vöru**. Fyrir frekari upplýsingar um þetta yfirlit, sjá [Notkunarstaður vöru](../controlling-and-reporting/item-where-used.md).

Skýringarmyndin hér að neðan sýnir dæmi um listasíðuna **Innkaupabeiðni verkbeiðni**.

![Mynd 1.](media/08-work-orders.png)


Listasíðan **Innkaup verkbeiðni** (**Eignastýring** > **Innkaup** > **Innkaup verkbeiðni**) sýnir lista yfir innkaupapantanir sem tengjast verkbeiðnum. Þegar þú velur vinnslu verkbeiðni á þessari síðu geturðu notað hnappana í hópnum **Sýna** á aðgerðarúðuflipanum **Innkaup verkbeiðni** til að framkvæma ýmsar aðgerðir:

- Til að opna tengda innkaupabeiðni skaltu velja **Innkaupabeiðni**. 
- Til að opna tengda verkbeiðni skaltu velja **Verkbeiðni**.
- Til að fá yfirlit sem sýnir hvar hluturinn á völdum línum er notaður í tengslum við eignir, vanskil tegunda viðhaldsverka, varahluti og verkbeiðnir í eignastýringu velurðu **Notkunarstaður vöru**. Fyrir frekari upplýsingar um þetta yfirlit, sjá [Notkunarstaður vöru](../controlling-and-reporting/item-where-used.md).

Skýringarmyndin hér að neðan sýnir dæmi um listasíðuna **Innkaup verkbeiðni**.

![Mynd 2.](media/09-work-orders.png)


Á bæði listasíðunni **Innkaup verkbeiðni** og listasíðunni **Innkaupabeiðni verkbeiðni** birtist tákn sem tengist stjórnun á afhendingardegi hægra megin við hverja línu. Ef táknið sýnir upphrópunarmerki í rauðum hring þýðir það að afhending á tengdri innkaupapöntun eða innkaupabeiðni kann að tefjast.

Fyrir innkaupapöntun er dagsetningin sem tengist innkaupapöntunarlínunni notuð til að reikna út mögulega seinkun. Til að skoða þessa dagsetningu, á síðunni **Innkaupapöntun** velurðu innkaupapöntunarlínuna. Dagsetningin er sýnd í reitnum **Staðfestur afhendingardagur** á flipanum **Uppsetning** á flýtiflipanum **Línulýsing**. Ef reiturinn **Staðfestur afhendingardagur** er ekki stilltur er dagsetningin í reitnum **Afhendingardagur** á flýtiflipanum **Innkaupapöntunarhaus** er notuð við útreikninginn. Ein af þessum dagsetningum er borin saman við tiltæka dagsetningu í verkbeiðni eða verkbeiðnivinnslu í eftirfarandi röð:

1. Raunverulegur upphafsdagur verkbeiðni  

2. Áætlaður upphafsdagur á tengdu verkbeiðniverki 

3. Áætlaður upphafsdagur verkbeiðni 

4. Væntur upphafsdagur verkbeiðni, eða 

Fyrir innkaupabeiðni er dagsetningin í reitnum **Umbeðin dagsetning** á flýtiflipanum **Haus innkaupabeiðni** á síðunni **Innkaupabeiðnir** notuð til að reikna út hugsanlega seinkun. Dagsetningin í þeim reit er borin saman við tiltæka dagsetningu í verkbeiðni eða verkbeiðnivinnslu í sömu röð og er notuð fyrir innkaupapöntun.


## <a name="create-a-purchase-order-from-a-work-order"></a>Stofna innkaupapöntun úr verkbeiðni

Á listasíðunni **Allar verkbeiðnir** er hægt að velja verkbeiðnivinnslu og stofna síðan tengda innkaupapöntun eða tengda innkaupabeiðni. Þannig tryggirðu að samskipti verka eru til staðar á milli innkaupapöntunar eða innkaupabeiðni og verkbeiðni.

1. Veljið **Eignastýring** > **Verkbeiðnir** > **Allar verkbeiðnir** eða **Virkar verkbeiðnir**.

2. Veldu verkbeiðnina sem þú vilt búa til innkaupapöntun fyrir og veldu síðan **Breyta**.

3. Á flýtiflipanum **Viðhaldsverk verkbeiðni** velurðu vinnslu verkbeiðni til að stofna innkaupapöntun fyrir.

4. Veldu **Vöruliðir** > **Innkaupapöntun úr verkbeiðniverki**.

5. Á listasíðunni **Innkaupapantanir verks** smellirðu á **Nýtt**.

6. Stofnaðu innkaupapöntunina.

>[!NOTE]
>Fylgdu sömu skrefum til að búa til tengda innkaupabeiðni. Veldu hins vegar **Vöruliðir** > **Innkaupabeiðni úr vinnslu verkbeiðni** í 4. þrepi.


## <a name="project-relation-between-work-order-and-purchase-order-or-purchase-requisition"></a>Verkefnatengsl milli verkbeiðni og innkaupapöntunar eða innkaupabeiðni

Innkaupapöntunarlína eða innkaupabeiðnilína er tengd verkbeiðniverkum í gegnum verkbeiðniverkið og tengda verkþáttanúmerið. Þegar þú býrð til innkaupapöntun eða innkaupabeiðni úr verkbeiðniverki er tengt verkþáttanúmer skylda. Ef allar verkbeiðnivinnslur í tengdri verkbeiðni er með sömu gerð viðhaldsverks er verkþáttanúmerið sjálfkrafa sett inn í innkaupapöntun eða innkaupabeiðni. Ef allar verkbeiðnivinnslur eru með aðrar gerðir viðhaldsverka verður að setja verkþáttanúmerið handvirkt inn í innkaupapöntun eða innkaupabeiðni.

Til að skoða eða slá inn verkþáttanúmerið sem er tengt innkaupapöntunarlínu, á listasíðunni **Innkaup verkbeiðni**, skaltu velja innkaupapöntunarskrána og síðan, í dálkinum **Innkaupapöntun**, velurðu hlekkinn fyrir innkaupapöntunina. Þú getur fundið reitinn **Verkþáttarnúmer** á flipanum **Verk** á flýtiflipanum **Línulýsing**.

Myndin hér að neðan sýnir dæmi um síðuna **Innkaupapöntun** með áherslu á **Verkþáttarnúmer**.

![Mynd 3.](media/10-work-orders.png)

Á sama hátt, til að skoða eða slá inn verkþáttanúmerið sem er tengt innkaupabeiðnilínu verkbeiðni, á listasíðunni **Innkaupabeiðni verkbeiðni**, skaltu velja innkaupabeiðniskrána og síðan, í dálkinum **Innkaupabeiðni**, velurðu hlekkinn fyrir innkaupabeiðnina. Þú getur fundið reitinn **Verkþáttarnúmer** á flipanum **Verk** á flýtiflipanum **Línulýsing**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]