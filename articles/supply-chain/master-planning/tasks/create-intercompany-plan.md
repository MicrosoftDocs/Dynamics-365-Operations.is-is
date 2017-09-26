--- 
title: "Búa til áætlun innan samstæðu"
description: "Þessi verklýsing sýnir hvernig á að stofna innansamstæðu áætlun."
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 7c7f466add55fb9a24c3fb8f1f92df712a8622e3
ms.contentlocale: is-is
ms.lasthandoff: 07/27/2017

---
# <a name="create-an-intercompany-plan"></a>Búa til áætlun innan samstæðu

[!include[task guide banner](../../includes/task-guide-banner.md)]

Þessi verklýsing sýnir hvernig á að stofna innansamstæðu áætlun. Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.


## <a name="set-up-an-intercompany-planning-group"></a>Setja upp Áætlunarflokk innan samstæðu 
1. Fara í Áætlunarflokkar innan samstæðu.
    * Aðaláætlanagerð > Uppsetning > Áætlunarhópar innan samstæðu.  
2. Nota flýtiafmörkun til að finna færslur Til dæmis, sía svæðið Heiti með virði '10'.
3. Í listanum skal merkja valda línu.
4. Smellið á Eyða.
    * Þetta skref er nauðsynlegt til að stytta áætlunarkeyrslu innan samstæðu.   Áætlanagerð innan samstæðu mun keyra aðaláætlanagerð í öllum fyrirtækjum í áætlunarflokki, frá lægstu röðunarröðinni.  
5. Smella á Já.
6. Lokið síðunni.

## <a name="create-an-intercompany-plan"></a>Búa til áætlun innan samstæðu
1. Smelltu á samstæðuáætlun
    * Þetta er á vinnusvæði aðaláætlanagerðar.  
2. Í reitnum Áætlunarflokkur innan samstæðu áætlunskal smella á fellilistahnappinn til að opna leitina.
3. Í listanum skal smella á tengilinn í valinni línu.
    * Veldu áætlunarflokk innan samstæðu 10.  
4. Í reitnum Fjöldi ítrekana fyrir samstæðuáætlun skal færa inn ‚2‘.
    * Áætlunarflokkur innan samstæðu 10 er með tvo meðlimi. Til að dreifa seinkanir frá upprunafyrirtæki (USMF) til fyrirtækis viðskiptavinar (DEMF), þarf að keyra innan samstæðu í báðum fyrirtækjunum tvisvar sinnum. Fyrsta ítrekun mun dreifa eftirspurninni og auðkenna seinkanir í upprunafyrirtækinu (USMF). Önnur ítrekun mun dreifa seinkanir úr USMF til DEMF.  
5. Veljið valkost í svæðinu fyrsta ítrekun.
6. Í reitnum fyrsta ítrekun skal velja "Endurnýjun".
7. Í reitnum síðari ítrekanir skal velja "Endurnýjun".
8. Í svæðinu Fjölda þráða skal færa inn tölu.
    * Þetta táknar fjölda samhliða þráða sem er nota við áætlanagerð.  
9. Smellið á „Í lagi“.

## <a name="view-the-result-of-the-plan"></a>Skoða niðurstaða áætlunar.
1. Í reitnum Áætlun skal smella á fellilistahnappinn til að opna leitina.
2. Í listanum skal smella á tengilinn í valinni línu.
    * Smelltu á tengil StaticPlan. Þú þarft að vera í fyrirtæki USMF.  
3. Smellt er á Áætlaðar pantanir.


