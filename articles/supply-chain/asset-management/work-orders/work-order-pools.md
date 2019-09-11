---
title: Verkbeiðnihópar
description: Þetta efnisatriði lýsir því hvernig á að vinna með verkbeiðnisöfn í eignastjórnun.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 069fa02073808fd7bbaac9bc1603e49ce4d450eb
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875715"
---
# <a name="work-order-pools"></a>Verkbeiðnihópar


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Þú getur notað verkbeiðnisöfn til að flokka verkbeiðnir sem eiga eitthvað sameiginlegt. Til dæmis er hægt að búa til verkbeiðnisöfn fyrir

- vinnuáhafnir, til dæmis viðhaldsáhafnir A, viðhaldsáhafnir B  

- faglega færni, til dæmis rafvirkjar eða pípulagningarmenn  

- efnislegar staðsetningar  

- tímaáætlanir, til dæmis vikur eða önnur tímabil  


Ef þess er krafist er hægt að setja eina verkbeiðni í mörg verkbeiðnisöfn.


## <a name="create-work-order-pool"></a>Stofna verkbeiðnasafn

Í **Öllum verkbeiðnisöfnum** eða **Virkum verkbeiðnisöfnum** geturðu fengið yfirlit yfir verkbeiðnisöfn þín og búið til ný söfn.

1. Smelltu á **Eignastýringu** > **Sameiginlegt** > **Verkbeiðnsöfn** > **Öll verkbeiðnasöfn** eða **Virk verkbeiðnasöfn**.

2. Smellt er á **Nýtt**.

3. Settu inn kenni verkbeiðnisafns í reitinn **Safn** og heiti í reitinn **Heiti**.

4. Veldu „Já“ á skiptihnappnum **Virkur** til að gefa til kynna að verkbeiðnisafnið sé virkt.

5. Veldu „Já“ á skiptihnappnum **Eyða samskiptum við verkbeiðni** ef þú vilt að verkbeiðnir verði sjálfkrafa fjarlægðar úr verkbeiðnisafninu.

6. Í reitnum **Eyða líftímastöðu** velurðu líftímastöðu verkbeiðni. Til dæmis væri hægt að stilla líftímastöðu verkbeiðninnar til að klára verkbeiðni til að eyða sjálfkrafa samskiptum við verkbeiðnisöfn.

7. Þú getur byrjað að bæta verkbeiðnum við verkbeiðnasafnið þitt strax. Á flýtiflipanum **Verkbeiðnir** er smellt á **Bæta við línu**.

8. Veldu verkbeiðni í reitnum **Verkbeiðni**. Tengdir reitir eru sjálfkrafa uppfærðir.

9. Endurtaktu skref 7-8 ef þú vilt bæta við fleiri verkbeiðnum.

10. Í reitnum **Flokkun** geturðu gefið til kynna hvort verkbeiðnirnar ættu að fara fram í ákveðinni röð. Settu inn tölur 1, 2, 3 og svo framvegis til að gefa til kynna ákveðna röð fyrir valdar verkbeiðnir.

11. Smelltu á hnappinn **Verkbeiðnir** til að sjá lista yfir allar verkbeiðnir sem fylgja með í verkbeiðnisafninu.

12. Smelltu á hnappinn **Álag** til að opna **Álag** til að reikna og skoða álag fyrir viðhaldsskema, óáætlaðar verkbeiðnir og áætlaðar verkbeiðnir.

13. Smelltu á hnappinn **Vöruspá** til að opna **Vöruspá** til að reikna út og skoða spár fyrir vörur (varahluti og aðrar umbeðnar vörur) sem tengjast viðhaldsskema, óáætluðum verkbeiðnum og áætluðum verkbeiðnum.

14. Smelltu á hnappinn **Innkaupabeiðni um verkbeiðni** til að opna listann **Innkaupabeiðni um verkbeiðni** til að sjá lista yfir innkaupabeiðnir sem tengjast verkbeiðnum í verkbeiðnasafni.

15. Smelltu á hnappinn **Innkaupabeiðni um verkbeiðni** til að opna listann **Innkaupabeiðni um verkbeiðni** til að sjá lista yfir innkaupapandanir sem tengjast verkbeiðnum í verkbeiðnasafni.

>[!NOTE]
>Þegar verkbeiðnisafn er ekki lengur viðeigandi fyrir vinnuáætlun þína skaltu stilla gátreitinn **Virkur** fyrir safnið á „Nei“ í listasýninni **Verkbeiðnisafn**.

Veldu gátreitinn **Eyða samskiptum við verkbeiðnir** ef þú vilt eyða öllum verkbeiðnilínum, til dæmis til að stofna tómt safn sem þú getur seinna notað fyrir aðrar verkbeiðnir. Mundu að hreinsa gátreitinn **Eyða samskiptum við verkbeiðni** ef þú vilt nota verkbeiðnisafnið til að búa til ný verkbeiðnitengsl síðar.


![Mynd 1](media/22-work-orders.png)


## <a name="add-work-order-to-a-work-order-pool"></a>Bættu verkbeiðni við verkbeiðnasafn

Eins og lýst er í kaflanum hér að ofan, geturðu bætt verkbeiðnum við verkbeiðnisafn þegar þú stofnar safnið. Þú getur líka bætt við verkbeiðni í verkbeiðnasafnið úr einum af listunum **Allar verkbeiðnir**.

1. Smelltu á **Eignastýringu** > **Sameiginlegt** > **Verkbeiðnir** > **Allar verkbeiðnir** eða **Virkar verkbeiðnir**.

2. Veldu verkbeiðnina á listanum og smelltu á **Verkbeiðnasafn**.

3. Veldu „Bæta við“ í reitnum **Bæta við/fjarlægja**.

4. Veldu verkbeiðnina í reitnum **Safn**.

5. Smellt er á **OK**.

6. Eftir að þú hefur bætt verkbeiðni við verkbeiðnisafnið, ef þú vilt setja verkbeiðnina í tiltekna röð í safninu: Opnaðu eina af listasíðum verkbeiðnisafnanna, veldu safnið og smelltu á **Breyta** og aðlagaðu röðun verkbeiðnanna sem eru innifaldar í safninu í myndinni **Verkbeiðnasafn** > flýtiflipanum **Verkbeiðni** > reitnum **Flokkun**.

Ef þú vilt fjarlægja valda vinnupöntun úr verkbeiðnasafni skaltu velja „Fjarlægja“ í þrepi 3.

