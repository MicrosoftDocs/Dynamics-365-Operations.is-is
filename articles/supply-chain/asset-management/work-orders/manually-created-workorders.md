---
title: Handvirkt stofnaðar verkbeiðnir
description: Þetta efni útskýrir hvernig á að stofna verkbeiðnir handvirkt í eignastýringu.
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
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
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8a8494bdefcf11dc331be18bfe02e0df1e39d602
ms.sourcegitcommit: deb87e518a151d8bb084891851a39758938a96e4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/15/2019
ms.locfileid: "2626248"
---
# <a name="manually-created-work-orders"></a>Handvirkt stofnaðar verkbeiðnir

[!include [banner](../../includes/banner.md)]


Hægt er að stofna verkbeiðnir handvirkt á tvo vegu:

- Á síðunni **Allar verkbeiðnir** eða **Virkar verkbeiðnir** 
- Á síðunni **Allar viðhaldsbeiðnir** eða **Virkar viðhaldsbeiðnir** eða **Mínar viðhaldsbeiðnir á virkri staðsetningu**. 

## <a name="create-work-order"></a>Stofna verkbeiðni

1. Veldu **Eignastýringu** > **Sameiginlegt** > **Verkbeiðnir** > **Allar verkbeiðnir** eða **Virkar verkbeiðnir**.

2. Veljið **Nýtt**.

3. Í glugganum **Stofna verkbeiðni** velurðu gerð verkbeiðni í reitnum **Gerð verkbeiðni**.

4. Ef þess er krafist skal velja **Lýsingu**.

5. Í reitnum **Eign** velurðu eignina.

>[!NOTE]
>Þegar þú velur eign gætu þrír flipar verið tiltækir í fellivalmyndinni **Eignir**: 

- **Virkar eignir** - Þessi flipi inniheldur lista yfir allar eignir sem hafa eignalíftímastöðuna „Virkt“. 
- **Eignayfirlit** - Þessi flipi sýnir trjáyfirlit yfir virkar staðseningar og eignirnar sem eru settar upp á þeim.
- **Mínar eignir** - Þessi flipi inniheldur eignir sem tengjast virkum staðsetningum sem þú (starfsmaðurinn sem er skráður inn í kerfið) getur verið úthlutað á. (Sjá upplýsingar um uppsetninguna í [Viðhaldsstarfsmenn og starfsmannahópar](../setup-for-objects/workers-and-worker-groups.md).) Ef engar virkar staðsetningar eru settar upp á starfskrafti í [Viðhaldsstarfsmenn og starfsmannahópar](../setup-for-objects/workers-and-worker-groups.md) er flipinn **Mínar eignir** ekki tiltækur. 

6. Í reitnum **Tegund viðhaldsverka** velurðu gerð viðhaldsverka fyrir verkbeiðnina.

7. Ef þörf krefur skaltu velja **Afbrigði af gerð viðhaldsstarfa** og **Viðskipti**.

8. Ef þess er krafist geturðu breytt þjónustustigi verkbeiðni í reitnum **Þjónustustig**.

9. Veldu dagsetningarnar **Væntanlegt upphaf** og **Væntanleg lok** í tengdum reitum.

10. Smelltu á **Í lagi** til að stofna verkbeiðnina.

11. Á listasíðunni **Allar verkbeiðnir** er hægt að breyta verkbeiðninni eftir þörfum.

Athugið eftirfarandi stig:

- Á listasíðunni **Allar verkbeiðnir** er hægt að bæta nokkrum eignum við verkbeiðni í smáatriðum með því að bæta við línum á flýtiflipanum **Viðhaldsverk verkbeiðna**. Á eign er aðeins hægt að velja gerðir viðhaldsverka sem eru skilgreindar á eignategundinni sem er valin á eigninni.  

- Ef þú breytir þjónustustigi eigna eða mikilvægi eigna eftir að þú hefur notað eignina í verkbeiðni, er þjónustustigið eða mikilvægi á verkbeiðninnar ekki uppfært til samræmis. Fyrir frekari upplýsingar um þjónustustig og mikilvægi, sjá [Þjónustustig eigna](../setup-for-objects/object-priorities.md) og [Mikilvægi eigna](../setup-for-objects/object-criticalities.md).

- Mikilvægi á verkbeiðni er endurútreiknað í hvert skipti sem vinnslu verkbeiðni er bætt við eða henni eytt úr verkbeiðninni.

- Í upplýsingaglugganum **Allar verkbeiðnir** > flipanum **Haus** > flýtiflipanum **Áætlun** í reitunum **Ábyrgur hópur** eða **Ábyrgðarmaður** geturðu valið ábyrgan starfsmanahóp eða ábyrgan viðhaldsstarfsmann. Þessum stillingum er hægt að breyta meðan verkbeiðnin er virk. Til dæmis er hægt að breyta þeim þegar ástand líftíma verkbeiðni breytist. Sjálfvirka valið sem gert var við stofnun verkbeiðni er byggt á uppsetningunni á síðunni **Ábyrgir viðhaldsstarfsmenn**. Ef þú bætir við eða fjarlægir verkbeiðniverk eftir að þú hefur búið til verkbeiðni og ef reiturinn **Ábyrgur hópur** og reiturinn **Ábyrgðarmaður** eru auðir þegar þú uppfærir verkbeiðnina reynir Eignastjórnun að finna ábyrgan viðhaldsstarfsmannahóp eða ábyrgan viðhaldsstarfsmann fyrir hugsanlega samsvörun á uppsetningarsíðunni. Ef reiturinn **Ábyrgur hópur** eða reiturinn **Ábyrgðarmaður** eru þegar stilltir þegar þú uppfærir verkbeiðnina verða engar breytingar gerðar. Nánari upplýsingar um hvernig á að setja upp starfskrafta og viðhaldsstarfsmannahóps er að finna í [Ábyrgir viðhaldsstarfskraftar](../setup-for-maintenance-requests/responsible-workers.md).)

- Af síðunni [Viðhaldsstaða](../controlling-and-reporting/maintenance-status.md) er hægt að gera útreikning til að fá yfirlit yfir vinnuálag varðandi komandi og loknar verkbeiðnir.  

- Í upplýsingayfirlitinu á síðunni **Allar verkbeiðnir**, á flýtiflipanum **Línulýsing**, er hægt að nota reitina **Breidd** og **Lengdargráða** til að bæta við landfræðilegum hnitum fyrir eignina sem er valin í vinnslu verkbeiðni.  


## <a name="create-related-work-order"></a>Stofna tengda verkbeiðni

Hægt er að stofna verkbeiðni sem tengist fyrirliggjandi verkbeiðni. Þessi afkastageta er gagnleg ef þú vilt til dæmis vinna með aðal- og annars flokks verkbeiðnir. Ný verkbeiðni er byggð á verkbeiðnivinnslu úr fyrirliggjandi verkbeiðni.

1. Veldu **Eignastýringu** > **Sameiginlegt** > **Verkbeiðnir** > **Allar verkbeiðnir** eða **Virkar verkbeiðnir**.

2. Veldu verkbeiðnina til að stofna tengda verkbeiðni fyrir.

3. Á aðgerðarrúðunni, á flipanum **Verkbeiðni**, í hópnum **Nýtt** skaltu velja **Tengd verkbeiðni**.

4. Í glugganum **Stofna tengda verkbeiðni**, í reitnum **Verkbeiðnivinnsla**, velurðu verkbeiðnivinnsluna sem þú vilt búa til tengda verkbeiðni fyrir.

5. Veldu gerð viðhaldsverka í reitnum **Tegund viðhaldsverka**.

6. Veldu tengt afbrigði og viðskipti viðhaldsverks í reitunum **Afbrigði af gerð viðhaldsverka** og **Viðskipti**, eftir þörfum.

7. Ef þessi verkbeiðni er fyrsta tengda verkbeiðnin sem hefur verið búin til fyrir valda verkbeiðni, fylgdu þessum skrefum:
    1. Veldu valkostinn **Ný verkbeiðni**.
    2. Í reitnum **Verkbeiðni** velurðu gerð verkbeiðni.
    3. Í **Lýsing** skal færa inn lýsingu.
    4. Í reitnum **Þjónustustig** skaltu breyta þjónustustigi verkbeiðna eftir þörfum.
    5. Í reitunum **Væntanlegt upphaf** og **Væntanleg lok** velurðu væntar upphafs- og lokadagsetningar.
    6. Veljið **Í lagi**. Nýja tengda verkbeiðnin er sýnd á listasíðunni **Allar verkbeiðnir**.  

8. Ef verkbeiðnin sem þú ert að stofna þessa skyldu verkbeiðni fyrir er þegar með tengdar verkbeiðnir, fylgdu þessum skrefum til að bæta nýrri vinnslu verkbeiðni við fyrirliggjandi tengda verkbeiðni:
    1. Veldu valkostinn **Bæta við tengdri verkbeiðni**.
    2. Í reitnum **Verkbeiðni** velurðu tengda verkbeiðni sem þú vilt bæta nýju verkbeiðniverki við.
    3. Í reitnum **Þjónustustig** skaltu breyta þjónustustigi verkbeiðna eftir þörfum.
    4. Í reitunum **Væntanlegt upphaf** og **Væntanleg lok** breytirðu væntum upphafs- og lokadagsetningum, eftir þörfum.
    5. Veljið **Í lagi**. Verkbeiðnivinnslunni er bætt við fyrirliggjandi tengda verkbeiðni.

Skýringarmyndin hér að neðan sýnir dæmi um gluggann **Stofna tengda verkbeiðni**.

![Mynd 1](media/03-work-orders.png)

>[!NOTE]
>Athugasemd: Ef þú hefur sett upp tengda verkbeiðnisíu á flipanum **Færibreytur eignastýringar** > **Verkbeiðnir** > reitnum **Tengd verkbeiðnisía** verða kenni verkbeiðna stofnuð í samræmi við uppsetningu síunnar. Ef engin tengd verkbeiðnisía er sett upp er næsta tiltæka kenni verkbeiðni notað fyrir tengdar verkbeiðnir.

## <a name="copy-a-work-order"></a>Afrita verkbeiðni

Það er mögulegt að fljótt búa til nýja verkbeiðni úr núverandi verkbeiðni. Þessi leið til að vinna með verkbeiðnir er frábrugðin stofnun verkbeiðna samkvæmt [viðhaldsáætlunum](../preventive-and-reactive-maintenance/maintenance-plans.md). Það er gagnlegt ef þú hefur til dæmis verkbeiðni sem inniheldur margar verkbeiðnavinnslur og ljúka skal ýmsum vinnslum á mismunandi eignum með reglulegu millibili.

1. Veldu **Eignastýringu** > **Sameiginlegt** > **Verkbeiðnir** > **Allar verkbeiðnir** eða **Virkar verkbeiðnir**.

2. Veldu verkbeiðnina til að afrita efni úr.

3. Á aðgerðarrúðunni > flipanum **Verkbeiðni** > hópnum **Nýtt** skaltu velja **Afrita verkbeiðni**.

4. Uppsetning verkbeiðninnar úr valinni verkbeiðni er sýnd. Hægt er að breyta nokkrum reitanna, eftir þörfum.

5. Veldu **Í lagi** til að stofna nýja verkbeiðni.

6. Á listasíðunni **Allar verkbeiðnir** er hægt að breyta verkbeiðninni eftir þörfum.

>[!NOTE]
>Þegar nýja verkbeiðnin er búin til eru sumar upplýsingar afritaðar beint úr fyrirliggjandi verkbeiðni. Upplýsingar um spár, verkfæri, viðhaldsgátlista, virka staðsetningu, heimilisföng og tímasetningar eru ekki afritaðar. Í staðinn eru þær frumstilltar úr núverandi uppsetningu í Eignastjórnun. Þess vegna, ef þeim upplýsingum var breytt á milli tímabilsins þegar fyrsta verkbeiðnin var búin til og þess tíma þegar þú bjóst til afrit af verkbeiðninni, eru breytingarnar með í nýju verkbeiðninni. Dæmi um það eru breytingar á spám og uppfærslur á viðhaldsgátlistum.

Myndin hér að neðan sýnir dæmi um gluggann **Afrita verkbeiðnir**.

![Mynd 2](media/04-work-orders.png)


## <a name="create-a-work-order-based-on-a-maintenance-request"></a>Stofna verkbeiðni sem byggist á viðhaldsbeiðni

1. Veldu **Eignastýring** > **Sameiginlegt** > **Viðhaldsbeiðnir** > **Allar viðhaldsbeiðnir** eða **Virkar viðhaldsbeiðnir**.

2. Veldu viðhaldsbeiðni til að stofna verkbeiðni fyrir og smelltu á **Breyta**.

3. Á aðgerðarrúðunni > flipanum **Viðhaldsbeiðni** > hópnum **Nýtt** skaltu velja **Verkbeiðni**.

4. Í glugganum **Verkbeiðni** skaltu stilla reitina. Ef gerð viðhaldsverks hefur verið valin í viðhaldsbeiðninni geturðu valið aðra tegund viðhaldsverka, ef þörf krefur, þegar þú stofnar verkbeiðnina, eftir þörfum.

5. Veljið **Í lagi**. Skilaboð tilkynna þér að verkbeiðni hefur verið stofnuð.

6. Til að sjá verkbeiðnirnar sem tengjast viðhaldsbeiðni skaltu velja viðhaldsbeiðnina á listasíðunni **Allar viðhaldsbeiðnir** eða **Virkar viðhaldsbeiðnir**. Síðan, á aðgerðarrúðunni, á flipanum **Viðhaldsbeiðni**, í hópnum **Skoða**, skaltu velja **Verkbeiðnir**.


Myndin hér að neðan sýnir dæmi um gluggann **Stofna verkbeiðni**.

![Mynd 3](media/05-work-orders.png)


>[!NOTE]
>Ef þú vilt að verkbeiðnir sé sjálfvirkt stofnaðar er hægt að tímastilla vinnslur viðhaldsáætlana eða hægt er að setja upp „Stofna sjálfvirkt“ [viðhaldsáætlanir](../preventive-and-reactive-maintenance/maintenance-plans.md) eða [viðhaldslotur](../preventive-and-reactive-maintenance/maintenance-rounds.md) á eign. Verkbeiðnir sem eru stofnaðar úr viðhaldsbeiðnum á listasíðunni **Öll viðhaldsskemu** eru með þær gerðir viðhaldsverka sem eru valdar í viðhaldsbeiðnum.

