---
title: Handvirkt stofnaðar verkbeiðnir
description: Þetta efni útskýrir hvernig á að stofna verkbeiðnir handvirkt í eignastýringu.
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
ms.openlocfilehash: 261448a134a7c1aacfbb4ea6f954ce03a63c23e2
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875713"
---
# <a name="manually-created-work-orders"></a>Handvirkt stofnaðar verkbeiðnir

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Hægt er að stofna verkbeiðnir handvirkt á tvo vegu:

- í **Öllum verkbeiðnum** eða **Virkum verkbeiðnum**  
- í **Öllum viðhaldsbeiðnum** eða **Virkum viðhaldsbeiðnum** eða **Mínum viðhaldsbeiðnum á virkri staðsetningu**.  

## <a name="create-work-order"></a>Stofna verkbeiðni

1. Smelltu á **Eignastýringu** > **Sameiginlegt** > **Verkbeiðnir** > **Allar verkbeiðnir** eða **Virkar verkbeiðnir**.

2. Smellið á hnappinn **Nýtt**.

3. Í fellivalmyndinni **Stofna verkbeiðni** velurðu gerð verkbeiðni.

4. Ef þess er krafist skal velja lýsingu.

5. Veldu eignina fyrir verkbeiðnina sem og gerð viðhaldsstarfa.

>[!NOTE]
>Þegar þú velur eign kunna þrír flipar að vera tiltækir: Flipinn **Mínar eignir** inniheldur eignir sem tengjast virkum staðsetningum sem þú (viðhaldsstarfsmaðurinn sem er skráður inn í kerfið) getur fengið úthlutað (sett upp í [Viðhaldsstarfsmenn og starfsmannahópar](../setup-for-objects/workers-and-worker-groups.md)). Ef engar virkar staðsetningar eru settar upp á viðhaldsstarfsmanni í [Viðhaldsstarfsmenn og starfsmannahópar](../setup-for-objects/workers-and-worker-groups.md) verður flipinn **Mínar eignir** ekki sýnilegur. Flipinn **Virkar eignir** hefur að geyma lista yfir allar eignir með eignalíftímastöðuna „Virkt“. Flipinn **Eignayfirlit** sýnir trjáyfirlit yfir virkar staðseningar og eignir sem eru settar upp á þessum stöðum.

6. Ef þörf krefur skaltu velja **Afbrigði af gerð viðhaldsstarfa** og **Viðskipti**.

7. Ef þess er krafist geturðu breytt þjónustustigi verkbeiðni í reitnum **Þjónustustig**.

8. Veldu áætlaðar upphafs- og lokadagsetningar í tengdum reitum.

9. Smelltu á **Í lagi** til að stofna nýja verkbeiðni.

10. Breytu verkbeiðninni í **Allar verkbeiðnir**, ef nauðsyn krefur.

- Í **Öllum verkbeiðnum** er hægt að bæta nokkrum eignum við verkbeiðni í smáatriðum með því að bæta við línum á flýtiflipanum **Viðhaldsverk verkbeiðna**. Á eign er aðeins hægt að velja gerðir viðhaldsverka sem eru skilgreindar á eignategundinni sem var valin fyrir eignina.  
- Ef þú hefur breytt þjónustustigi eigna eða mikilvægi eigna eftir að þú hefur notað þær í verkbeiðni (sjá [Þjónustustig](../setup-for-objects/object-priorities.md) og [Mikilvægi eigna](../setup-for-objects/object-criticalities.md)) er þjónustustig eða gagnrýni á vinnuskipunina ekki uppfærð til samræmis.
- Mikilvægi á verkbeiðni er endurútreiknuð í hvert skipti sem verkbeiðnilínu er bætt við eða henni eytt á verkbeiðninni.
- Í upplýsingaglugganum **Allar verkbeiðnir** > glugganum **Haus** > flýtiflipanum **Tímasetja** geturðu valið ábyrgan starfsmannahóp eða ábyrgan viðhaldsstarfsmann í reitunum **Ábyrgur hópur** eða **Ábyrgðarmaður**. Þessum stillingum er hægt að breyta eins lengi sem verkbeiðnin er virk, t.d. þegar líftímastaða verkbeiðninnar breytist. Sjálfvirka valið sem gert var við stofnun verkbeiðni er byggt á uppsetningunni í **Ábyrgir viðhaldsstarfsmenn**. Ef þú bætir við eða fjarlægir verkbeiðniverk eftir að þú hefur búið til verkbeiðni og reiturinn **Ábyrgur hópur** og reiturinn **Ábyrgðarmaður** eru auðir þegar þú uppfærir verkbeiðnina leitar Eignastjórnun að mögulegri samsvörun í uppsetningarforminu fyrir ábyrgan viðhaldsstarfsmannahóp eða ábyrgan viðhaldsstarfsmann. Ef reiturinn **Ábyrgur hópur** eða reiturinn **Ábyrgðarmaður** eru þegar fylltir út þegar þú uppfærir verkbeiðnina verða engar breytingar gerðar. 

- Í **Viðhaldsstöðu** geturðu gert útreikning til að fá yfirlit yfir vinnuálag varðandi komandi og loknar verkbeiðnir.  

- Á flýtiflipanum **Línulýsing** skaltu nota reitina **Breiddargráða** og **Lengdargráða** til að bæta við landfræðilegum hnitum fyrir þá eign sem valin var í verkbeiðnivinnslunni.  

## <a name="create-related-work-order"></a>Stofna tengda verkbeiðni

Þú getur búið til tengda verkbeiðni við núverandi verkbeiðni ef þú vilt til dæmis vinna með aðal- og annars flokks verkbeiðnir. Ný verkbeiðni er byggð á verkbeiðnivinnslu úr fyrirliggjandi verkbeiðni.

1. Smelltu á **Eignastýringu** > **Sameiginlegt** > **Verkbeiðnir** > **Allar verkbeiðnir** eða **Virkar verkbeiðnir**.

2. Veldu verkbeiðnina sem þú vilt búa til tengda verkbeiðni fyrir.

3. Smelltu á **Tengd verkbeiðni**.

4. Í felliglugganum **Stofna tengda verkbeiðni** velurðu verkbeiðnivinnsluna sem þú vilt búa til tengda verkbeiðni fyrir í reitnum **Verkbeiðnivinnsla**.

5. Veldu gerð viðhaldsverks í reitnum **Gerð viðhaldsverks** og, ef þess er krafist, tengt viðhaldsverkategundafbrigði og viðskipti í reitunum **Tegundaafbrigði viðhaldsverka** og **Viðskipti**.

6. Ef þetta er fyrsta tengda verkbeiðnin sem þú gerir skaltu smella á valhringinn **Ný verkbeiðni**.

7. Veldu **Gerð verkbeiðni** og **Lýsingu** í tengdum reitum.

8. Ef þess er krafist skaltu breyta þjónustustigi verkbeiðni í reitnum **Þjónustustig**.

9. Settu inn áætlaðar upphafs- og lokadagsetningar í tengdum reitum.

10. Smellt er á **OK**. Nýja tengda verkbeiðnin er sýnd í listanum **Allar verkbeiðnir**.

11. Ef þú býrð til tengda verkbeiðni í verkbeiðni sem er þegar með tengdar verkbeiðnir geturðu bætt verkbeiðni vinnslunni við þegar tengda verkbeiðni. Þetta er gert með því að smella á valhringinn **Bæta við tengda verkbeiðni** í 6. þrepi. Síðan velurðu tengda verkbeiðni sem þú vilt bæta nýju verkbeiðniverki við. Breyttu reitunum **Þjónustustig**, **Áætluð byrjun** og **Áætluð lok** eftir þörfum og smelltu á **Í lagi**. Verkbeiðnivinnslunni er bætt við fyrirliggjandi tengda verkbeiðni.


![Mynd 1](media/03-work-orders.png)

**Athugasemd:** Ef þú hefur sett upp tengda verkbeiðnisíu í tenglinum **Færibreytur eignastýringar** > **Verkbeiðnir** > reitinn **Tengd verkbeiðnisía** verða kenni verkbeiðna stofnuð í samræmi við uppsetningu síunnar. Ef engin tengd verkbeiðnisía er sett upp verður næsta tiltæka kenni verkbeiðni notað fyrir tengdar verkbeiðnir.

## <a name="copy-work-order"></a>Afrita verkbeiðni

Það er mögulegt að fljótt búa til nýja verkbeiðni úr núverandi verkbeiðni. Þessi leið til að vinna með verkbeiðnir er frábrugðin því að búa til verkbeiðnir byggðar á viðhaldsáætlunum. Það er gagnlegt ef þú hefur til dæmis verkbeiðni sem inniheldur margar verkbeiðnavinnslur með ýmsar vinnslur á mismunandi eignum sem á að ljúka með reglulegu millibili.

1. Smelltu á **Eignastýringu** > **Sameiginlegt** > **Verkbeiðnir** > **Allar verkbeiðnir** eða **Virkar verkbeiðnir**.

2. Veldu verkbeiðnina sem þú vilt afrita efni úr.

3. Smelltu á **Afrita verkbeiðni**. Uppsetning verkbeiðninnar úr valinni verkbeiðni er sýnd. Ef þess er krafist geturðu breytt nokkrum reitum.

4. Smelltu á **Í lagi** til að stofna nýja verkbeiðni.

5. Breytu verkbeiðninni í **Allar verkbeiðnir**, ef nauðsyn krefur.

>[!NOTE]
>Þegar nýja verkbeiðnin er búin til eru sumar upplýsingar afritaðar beint úr fyrirliggjandi verkbeiðni. Upplýsingar varðandi spár, verkfæri, viðhaldsgátlista, virka staðsetningu, netföng og tímasetningar eru ekki afritaðar heldur frumstilltar úr núverandi uppsetningu í Eignastjórnun. Þetta þýðir að ef breytingar voru gerðar í þessum gögnum frá stofnun fyrstu verkbeiðninnar þar til þú gerðir afrit af verkbeiðninni, þá eru þessar breytingar með í nýju verkbeiðninni sem þú bjóst til. Dæmi um það eru breytingar á spám eða uppfærðir viðhaldsgátlistar.


![Mynd 2](media/04-work-orders.png)


## <a name="create-work-order-based-on-a-maintenance-request"></a>Stofna verkbeiðni sem byggist á viðhaldsbeiðni

1. Smelltu á **Eignastýring** > **Sameiginlegt** > **Viðhaldsbeiðnir** > **Allar viðhaldsbeiðnir** eða **Virkar viðhaldsbeiðnir**.

2. Veldu viðhaldsbeiðni sem þú vilt búa til verkbeiðni fyrir og smelltu á **Breyta**.

3. Í **Öllum beiðnum** smellirðu á **Verkbeiðni**.

4. Fylltu út fellivalmyndina **Verkbeiðni**. Ef gerð viðhaldsverks hefur verið valin í viðhaldsbeiðninni geturðu valið aðra tegund viðhaldsverka, ef þörf krefur, þegar þú stofnar verkbeiðnina.

5. Smellt er á **OK**. Þú munt sjá skilaboð sem segja þér að verkbeiðnin hafi verið stofnuð.

6. Ef þú vilt sjá hvaða verkbeiðnir tengjast viðhaldsbeiðni skaltu velja viðhaldsbeiðnina í listunum **Allar viðhaldsbeiðnir** eða **Virkar viðhaldsbeiðnir** og smella á hnappinn **Verkbeiðnir**.


![Mynd 3](media/05-work-orders.png)


>[!NOTE]
>Verkbeiðnir geta einnig verið stofnaðar sjálfkrafa með því að tímasetja vinnslur viðhaldsáætlana, eða með því að setja upp „Stofna sjálfkrafa“ viðhaldsáætlanir eða viðhaldslotur á eign. Verkbeiðnir stofnaðar úr viðhaldsbeiðnum í **Viðhaldsáætlun** eru stofnaðar með þeim gerðum viðhaldsverka sem valdar eru í viðhaldsbeiðnum.

