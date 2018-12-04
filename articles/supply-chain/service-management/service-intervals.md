---
title: "Þjónustubil"
description: "Þjónustubil gefur til kynna þá tíðni sem þjónustupöntunarlínur eru stofnaðar fyrir þjónustusamningslínur þegar þjónustupantanir eru stofnaðar."
author: ShylaThompson
manager: AnnBe
ms.date: 02/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 4ea10e4c0fbfd21538bba16d2b01deb3e4b3a10d
ms.openlocfilehash: 4a51a3c3483e81cefdaf3d8e62a4f1f47fcd706b
ms.contentlocale: is-is
ms.lasthandoff: 02/20/2018

---

# <a name="service-intervals"></a>Þjónustubil

[!include [banner](../includes/banner.md)]

Þjónustusamningsbilið gefur til kynna þá tíðni sem þjónustupöntunarlínur eru stofnaðar fyrir þjónustusamningalínur þegar þjónustupantanir eru stofnaðar sjálfkrafa.

Þegar þjónustupantanir eru stofnaðar sjálfkrafa eru þjónustupöntunarlínur stofnaðar samkvæmt bilinu sem hefur verið tilgreint fyrir þjónustusamningslínurnar frá upphafsdagsetningu samningslínunnar.

Ef svæðið **Bil** fyrir þjónustusamningslínu á síðunni **Þjónustusamningar** er autt er línan einskiptis tilvik og hún er ekki notuð til að stofna þjónustupantanir í sífellu.

## <a name="example"></a>Dæmi

Þetta dæmi sýnir hvernig þjónustubil hefur áhrif á þjónustusamningslínur og þjónustupöntunarlínur í þjónustupöntun.

### <a name="create-a-service-agreement"></a>Stofna þjónustusamning

Fyrst er stofnaður þjónustusamningur og valmöguleikinn **Sameina þjónustupantanir** stilltur á **Eftir þjónustusamning**.

1. Smellið á **Þjónustusamningar**
2. Á **Aðgerðarrúðunni** í flipanum **Þjónustusamningur** í flokknum **Nýr** skal smella á **Þjónustusamning** til að stofna nýjan þjónustusamning.
3. Færið inn lýsingu, veljið verk í reitnum **Verkkenni** og færið inn dagsetningu í reitinn **Upphafsdagsetning**.
4. Í reitnum **Sameina þjónustupantanir**, skal velja **Eftir þjónustusamning**.

Nú er búið að stofna eftirfarandi þjónustusamninginn:

| Verkefni      | Fyrsti vinnudagur                                                                         |
|--------------|------------------------------------------------------------------------------------|
| Verkið | Dagsetningin sem var tilgreind fyrir verkið. Í þessu dæmi er núgildandi dagsetning notuð. |

### <a name="create-a-service-agreement-line"></a>Stofna þjónustusamningslínu

Næst er þjónustusamningslína stofnuð sem er með færslugerðina **Klst.**.

Til að ljúka þessum hluta dæmisins þarf að stofna þjónustubil sem nemur 10 dögum á síðunni **Þjónustubil**. 

1. Veljið þjónustusamninginn sem var nýverið stofnaður. 
2. Á flýtiflipanum **Línur** skal smella á hnappinn **Bæta við** til að stofna nýja línu í neðri rúðu síðunnar **Þjónustusamningar**.
3. Í reitnum **Færslugerð** skal velja **Klst.**.
4. Í reitnum **Starfskraftur** skal velja starfskraftinn sem mun afhenda þjónustuna.
5. Í reitnum **Þjónustubil** skal velja 10-daga bil.

Nú er búið að stofna þjónustusamningslínu með eftirfarandi upplýsingum:

| Færslugerð | Fyrsti vinnudagur                               | Þjónustubil |
|------------------|------------------------------------------|------------------|
| Vinnustund             | Núgildandi dagsetning.                        | Hverja 10 daga    |
| Starfsmaður           | Starfskrafturinn sem framkvæmir þjónustuna. |                  |

Enginn tímagluggi er tilgreindur fyrir línuna. 

### <a name="create-planned-service-orders"></a>Stofna áætlaðar þjónustupantanir

Nú er hægt að stofna áætlaðar þjónustupantanir og þjónustupöntunarlínur fyrir komandi mánuð.

1. Á síðunni **Þjónustusamningar**, í **Aðgerðarrúðunni**, í flipanum **Afhenda** skal smella á **Áætlaðar þjónustupantanir**.
2. Á síðunni **Stofna þjónustupantanir** skal færa inn núgildandi dagsetningu í reitinn **Dagsetning frá**. og dagsetningu sem er einum mánuði frá núgildandi dagsetningu í reitinn **Dagsetning til**.
3. Stillið sleðann **Klst.** á **Já**. 
4. Smellið á **Í lagi**.

Ein þjónustupöntunarlína er stofnuð fyrir hverja þjónustupöntun vegna þess að engin flokkun í þjónustupöntuninni er til (skilgreind af valkostinum **Eftir þjónustusamning** í reitnum **Sameina þjónustupantanir**).

### <a name="service-orders-created"></a>Þjónustupantanir stofnaðar

Þrjár þjónustupöntunarlínur hafa verið stofnaðar innan tímarammans sem var tilgreindur í svarglugganum **Stofna þjónustupantanir**. Hægt er að skoða þjónustupöntunarlínurnar á síðunni **Þjónustusamningar** (**Aðgerðarrúða** \> flipinn **Afhenda**\>, hnappurinn **Skoða**).

## <a name="related-topics"></a>Tengd efnisatriði

[Setja upp þjónustubil](set-up-service-intervals.md)  


