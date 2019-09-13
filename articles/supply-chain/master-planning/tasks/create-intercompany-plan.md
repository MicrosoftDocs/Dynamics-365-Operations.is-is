---
title: Búa til áætlun innan samstæðu
description: Þessi verklýsing sýnir hvernig á að stofna innansamstæðu áætlun.
author: ShylaThompson
manager: AnnBe
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f7fe8d155b39190f6c0ee1ee310a5edd2400623c
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916715"
---
# <a name="create-an-intercompany-plan"></a>Búa til áætlun innan samstæðu

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þessi verklýsing sýnir hvernig á að stofna innansamstæðu áætlun. Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.


## <a name="set-up-an-intercompany-planning-group"></a>Setja upp Áætlunarflokk innan samstæðu 
1. Í **skoðunarrúðunni** ferðu í **Kerfiseiningar > Aðaláætlanagerð > Uppsetning > Áætlunarhópar innan samstæðu**. 
2. Nota flýtiafmörkun til að finna færslur Til dæmis, sía svæðið Heiti með virði '10'.
3. Í listanum skal merkja valda línu.
4. Smellið á **Eyða**. Þetta skref er nauðsynlegt til að stytta áætlunarkeyrslu innan samstæðu.   Áætlanagerð innan samstæðu mun keyra aðaláætlanagerð í öllum fyrirtækjum í áætlunarflokki, frá lægstu röðunarröðinni.  
5. Smellið á **Já**.
6. Lokið síðunni.

## <a name="create-an-intercompany-plan"></a>Búa til áætlun innan samstæðu
1. Í **skoðunarrúðunni** ferðu í **Kerfiseiningar > Aðaláætlanagerð > Vinnusvæði > Aðaláætlanagerð**.
2. Smelltu á **Aðaláætlanagerð innan samstæðu**.  
3. Í reitnum **Fjárhagsáætlunarflokkur innan samstæðu** skal smella á fellilistahnappinn til að opna leitina.
4. Í listanum skal smella á tengilinn í valinni línu. Veldu áætlunarflokk innan samstæðu 10.  
5. Í reitnum **Fjöldi áætlaðra ítrekana innan samstæðu** skal færa inn ‚2‘. Áætlunarflokkur innan samstæðu 10 er með tvo meðlimi. Til að dreifa seinkanir frá upprunafyrirtæki (USMF) til fyrirtækis viðskiptavinar (DEMF), þarf að keyra innan samstæðu í báðum fyrirtækjunum tvisvar sinnum. Fyrsta ítrekun mun dreifa eftirspurninni og auðkenna seinkanir í upprunafyrirtækinu (USMF). Önnur ítrekun mun dreifa seinkanir úr USMF til DEMF.  
6. Í reitnum **Fyrsta ítrekun** skal velja „Endurgerð“.
7. Í reitnum **Síðari ítrekanir** skal velja „Endurgerð“.
8. Í reitinn **Fjöldi þráða** skal færa inn tölu. Þetta táknar fjölda samhliða þráða sem er nota við áætlanagerð.  
9. Smellt er á **OK**.

## <a name="view-the-result-of-the-plan"></a>Skoða niðurstaða áætlunar.
1. Í reitnum **Áætlun** skal smella á fellilistahnappinn til að opna leitina.
2. Í listanum skal smella á tengilinn í valinni línu. Smelltu á tengil StaticPlan. Þú þarft að vera í fyrirtæki USMF.  
3. Smelltu á **Tillögur**.

