---
title: Verkbeiðnihópar
description: Þetta efnisatriði lýsir því hvernig á að vinna með verkbeiðnisöfn í eignastjórnun.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderTablePoolPart, EntAssetWorkOrderPoolReferenceInfoPart, EntAssetWorkOrderPool, EntAssetWorkOrderPoolPreviewPart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3e95a4fdfaf4817867f3d2df7774df6a27ee6599
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430628"
---
# <a name="work-order-pools"></a>Verkbeiðnihópar

[!include [banner](../../includes/banner.md)]


Þú getur notað verkbeiðnisöfn til að flokka verkbeiðnir sem eiga eitthvað sameiginlegt. Hér eru nokkur dæmi um hluti sem þú getur búið til verkbeiðnisöfn fyrir:

- Vinnuáhafnir, til dæmis viðhaldsáhafnir A eða viðhaldsáhafnir B  

- Faglega færni, til dæmis rafvirkjar eða pípulagningarmenn  

- Efnislegar staðsetningar  

- Tímaáætlanir, til dæmis vikur eða önnur tímabil  

Hægt er að setja eina verkbeiðni í mörg verkbeiðnisöfn, eftir þörfum.


## <a name="create-a-work-order-pool"></a>Stofna verkbeiðnasafn

Á listasíðunni **Öll verkbeiðnisöfn** eða **Virk verkbeiðnisöfn** geturðu fengið yfirlit yfir verkbeiðnisöfn þín og búið til ný söfn.

1. Veldu **Eignastýringu** > **Sameiginlegt** > **Verkbeiðnsöfn** > **Öll verkbeiðnasöfn** eða **Virk verkbeiðnasöfn**.

2. Veljið **Nýtt**.

3. Í reitnum **Safn** skal færa inn kenni fyrir verkbeiðnisafnið.

4. reitinn **Heiti** skal færa inn heiti.

5. Stilltu valkostinn **Virkt** á **Já** til að gefa til kynna að verkbeiðnisafnið sé virkt.

6. Stilltu valkostinn **Eyða samskiptum við verkbeiðni** á **Já** ef verkbeiðnir skulu vera sjálfkrafa fjarlægðar úr verkbeiðnisafninu.

7. Í reitnum **Eyða líftímastöðu** velurðu líftímastöðu verkbeiðni. Til dæmis væri hægt að stilla líftímastöðu verkbeiðninnar til að klára verkbeiðni til að eyða sjálfkrafa samskiptum við verkbeiðnisöfn.

    Þú getur byrjað að bæta verkbeiðnum við verkbeiðnasafnið þitt strax.

8. Á flýtiflipanum **Verkbeiðnir** velurðu **Bæta við línu**.

9. Í reitnum **Verkbeiðni** velurðu verkbeiðni. Tengdir reitir eru sjálfkrafa uppfærðir.

10. Endurtakið skref 8 til og með 9 til að bæta við fleiri verkbeiðnum.

11. Ef verkbeiðnir sem þú bætir við ættu að vera gerðar í tiltekinni röð er hægt að slá inn í reitinn **Röð** tölurnar **1**, **2**, **3**, og svo framvegis, til að tilgreina þá röð.

12. Til að skoða lista yfir allar vinnupantanir sem eru innifaldar í vinnupöntunarlauginni, á aðgerðarglugganum, á flipanum **Verkbeiðnasafn**, í hópnum **Skoða safn yfir tengdar verkbeiðnir**, veldu **Verkbeiðnir** til að opna listasíðuna **Allar verkbeiðnir**.

13. Til að reikna og skoða getu álags fyrir viðhaldsáætlun, óskipulagðar verkbeiðnir og áætlaðar verkbeiðnir, á aðgerðarglugganum, á flipanum **Verkbeiðnasafn**, í hópnum **Skoða safn yfir tengdar verkbeiðnir**, veldu **Álag** til að opna gluggann **Reikna álag**.

14. Til að reikna og skoða spár fyrir hluti (varahluti og aðra áskilda hluti) sem tengjast viðhaldsáætlun, óskipulagðar verkbeiðnir og áætlaðar verkbeiðnir, á aðgerðarglugganum, á flipanum **Verkbeiðnasafn**, í hópnum **Skoða safn yfir tengdar verkbeiðnir**, veldu **Vöruspá** til að opna gluggann **Reikna vöruspá**.

15. Til að skoða lista yfir innkaupabeiðnir sem tengjast verkbeiðnum í verkbeiðnisafninu, á aðgerðarglugganum, á flipanum **Verkbeiðnasafn**, í hópnum **Innkaup**, veldu **Innkaupabeiðni verkbeiðni** til að opna listasíðuna **Innkaupabeiðni verkbeiðni**.

16. Til að skoða lista yfir innkaupapantanir sem tengjast verkbeiðnum í verkbeiðnisafninu, á aðgerðarglugganum, á flipanum **Verkbeiðnasafn**, í hópnum **Innkaup**, veldu **Innkaup verkbeiðni** til að opna listasíðuna **Innkaup verkbeiðni**.

>[!NOTE]
>Þegar verkbeiðnisafn er ekki lengur viðeigandi fyrir vinnuáætlun þína skaltu stilla gátreitinn **Virkt** fyrir safnið á **Nei** í listasýninni á síðunni **Verkbeiðnisafn**.

Til að eyða öllum pöntunarlínum starfsmanna stillirðu valkostinn **Eyða samskiptum við verkbeiðni** á **Já**. Þessi valkostur er gagnlegur ef þú vilt til dæmis búa til tómt safn sem þú getur notað seinna fyrir aðrar verkbeiðnir. Þegar þú ert tilbúin/n til að nota verkbeiðnasafnið til að stofna ný tengsl verkbeiðna skaltu muna að stilla valkostinn **Eyða samskiptum við verkbeiðni** á **Nei**.

Skýringarmyndin hér að neðan sýnir dæmi um listasíðuna **Verkbeiðnasafn**.

![Mynd 1](media/22-work-orders.png)


## <a name="add-a-work-order-to-a-work-order-pool"></a>Bættu verkbeiðni við verkbeiðnasafn

Eins og lýst er í kaflanum hér á undan, geturðu bætt verkbeiðnum við verkbeiðnisafn þegar þú stofnar safnið. Þú getur líka bætt verkbeiðnum við verkbeiðnasafnið á listasíðunni **Allar verkbeiðnir** eða **Virkar verkbeiðnir**.

1. Veldu verkbeiðni og síðan á aðgerðarrúðunni, á flipanum **Verkbeiðni**, í hópnum **Viðhalda**, velurðu **Verkbeiðnisafn**.

2. Veldu verkbeiðnina á listanum og smelltu á **Verkbeiðnasafn**.

3. Í glugganum **Viðhalda verkbeiðnisafni** í reitnum **Bæta við/fjarlægja**, veldu **Bæta við**.

4. Í reitnum **Safn** velurðu verkbeiðnasafnið.

5. Veljið **Í lagi**.

6. Til að setja verkbeiðnina sem þú bætir við í tiltekna röð í verkbeiðnasafnið, á listasíðunni **Öll verkbeiðnisöfn** eða **Virk verkbeiðnasöfn**, veldu safnið og veldu síðan **Breyta**. Síðan, á síðunni **Verkbeiðnasafn**, á flýtiflipanum **Verkbeiðnir**, notarðu reitinn **Röð** til að aðlaga röðun verkbeiðna sem eru innifaldar í safninu.

Til að fjarlægja valda vinnupöntun úr verkbeiðnasafni skaltu endurtaka þessi skref en velja **Fjarlægja** í þrepi 3.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]