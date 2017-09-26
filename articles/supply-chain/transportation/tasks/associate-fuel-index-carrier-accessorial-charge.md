--- 
title: "Tengja eldsneytisvísi flutningsaðila sem aukagjald"
description: "Þessar leiðbeiningar sýnir hvernig stofna á aukaúthlutunina, aukalegt gjald flutningsaðila, aukalega sniðmát fyrir eldsneytisálag og tengja eldsneytisvísi flutningsaðila við flutningsaðila."
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: d3ab4ee1a8ab74226b784496b56f26d26ed04ed8
ms.contentlocale: is-is
ms.lasthandoff: 07/27/2017

---
# <a name="associate-a-fuel-index-with-a-carrier-as-an-accessorial-charge"></a>Tengja eldsneytisvísi flutningsaðila sem aukagjald

[!include[task guide banner](../../includes/task-guide-banner.md)]

Þessar leiðbeiningar sýnir hvernig stofna á aukaúthlutunina, aukalegt gjald flutningsaðila, aukalega sniðmát fyrir eldsneytisálag og tengja eldsneytisvísi flutningsaðila við flutningsaðila. Það Þarf að vera uppsettur eldsneytisvísi flutningsaðila áður en þessari leiðbeiningar er keyrð. Hægt er að nota "Setja upp eldsneytisvísi flutningsaðila" leiðbeiningar til að gera þetta. Þessi uppsetningarverk eru yfirleitt gert með stjórnanda í Vörustjórnun. Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.


## <a name="create-an-accessorial-master"></a>Stofna aukalegt sniðmát
1. Fara í flutningsstjórnun > Uppsetning > Einkunn > Aukalegt sniðmát.
2. Smellið á „Nýtt“.
3. Í reitinn Aukalegt sniðmát skal færa inn gildi.
4. Í reitinn Heiti skal slá inn gildi.
5. Smellið á „Vista“.

## <a name="create-a-carrier-accessorial-charge"></a>Stofna aukagjöld flutningsaðila
1. Fara í flutningsstjórnun > Uppsetning >Einkunn > Aukagjöld flutningsaðila.
2. Smellið á „Nýtt“.
3. Færa inn gildi í reitnum aukalegt kenni flutningsaðila.
4. Í reitnum Farmflytjandi skal smella á fellilistahnappinn til að opna leitina.
5. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Í þessu dæmi skal velja Flutningsaðila með vörubíla.  
6. Í listanum skal smella á tengilinn í valinni línu.
7. Í reitnum Flutningsþjónusta skal smella á fellilistahnappinn til að opna leitina.
8. Í listanum skal smella á tengilinn í valinni línu.
9. Í reitnum Aukalegt sniðmát skal smella á fellilistahnappinn til að opna leitina.
10. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Í þessu dæmi skal velja nýstofnuð aukalega sniðmátið.  
11. Smellið á „Vista“.

## <a name="create-an-accessorial-assignment"></a>Stofna aukalega úthlutun
1. Smellt er á úthlutanir aukaþjónustu.
2. Smellið á „Nýtt“.
3. Í reitinn Heiti skal slá inn gildi.
4. Víxla útvíkkun á liðnum skilyrði.
    * Í skilyrðunum er Hægt er að velja að nota alltaf eldsneytisálag eða í þessu dæmi velja að það á einungis við innan ákveðið svæði.  
5. Í reitinn Póstnúmer frá skal slá inn gildi.
6. Í reitinn Póstnúmer til skal slá inn gildi.
7. Víxla útvíkkun á liðnum útreikningur.
    * Í hlutanum útreikning er hægt að tilgreina hvernig á að reikna út eldsneytisálag. Þessi útreikningur fer eftir aukalegu einunguna sem þú valdir sem grunn fyrir útreikninga.  
8. Veljið í svæðinu aukagjalds skal velja 'Eldsneytisálag'.
9. Veljið 'Vegalengd' í svæðinu aukaleg eining.
10. Í reitnum Svæði skal smella á fellilistahnappinn til að opna leitina.
11. Í listanum skal smella á tengilinn í valinni línu.
12. Smellið á „Vista“.

## <a name="update-the-carrier-rating-profile"></a>Uppfæra taxtaforstillingu flutningsaðila
1. Farið í flutningsstjórnun > Uppsetning > Flutningsaðilar > Farmflytjendur.
2. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
3. Víxla útvíkkun á liðnum taxtaforstillingar.
4. Smella á Breyta.
5. Í reitnum Eldsneytisvísir flutningsaðila skal smella á fellilistahnappinn til að opna leitina.
6. Í listanum skal smella á tengilinn í valinni línu.
7. Smellið á „Vista“.

