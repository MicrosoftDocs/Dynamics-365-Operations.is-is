---
title: Búa til áætlun innan samstæðu
description: Þessi verklýsing sýnir hvernig á að stofna innansamstæðu áætlun.
author: ChristianRytt
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7ef1484e6925427454f819a5effdc911f762b48b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578273"
---
# <a name="create-an-intercompany-plan"></a>Búa til áætlun innan samstæðu

[!include [banner](../../includes/banner.md)]

Þessi verklýsing sýnir hvernig á að stofna innansamstæðu áætlun. Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.

## <a name="set-up-an-intercompany-planning-group"></a>Setja upp Áætlunarflokk innan samstæðu

1. Í **skoðunarrúðunni** ferðu í **Kerfiseiningar > Aðaláætlanagerð > Uppsetning > Áætlunarhópar innan samstæðu**.
2. Nota flýtiafmörkun til að finna færslur Til dæmis, sía svæðið Heiti með virði '10'.
3. Í listanum skal merkja valda línu.
4. Veljið **Eyða**. Þetta skref er nauðsynlegt til að stytta áætlunarkeyrslu innan samstæðu.   Áætlanagerð innan samstæðu mun keyra aðaláætlanagerð í öllum fyrirtækjum í áætlunarflokki, frá lægstu röðunarröðinni.  
5. Velja skal **Já**.
6. Lokið síðunni.

## <a name="create-an-intercompany-master-plan"></a>Stofna aðaláætlun innan samstæðu

1. Í **skoðunarrúðunni** ferðu í **Kerfiseiningar > Aðaláætlanagerð > Vinnusvæði > Aðaláætlanagerð**.
2. Veljið **Aðaláætlanagerð innan samstæðu**.  
3. Í reitnum **Áætlunarflokkur innan samstæðu** skal velja á fellilistahnappinn til að opna leitina.
4. Í listanum skal velja tengilinn í valinni línu. Veldu áætlunarflokk innan samstæðu 10.  
5. Í reitnum **Fjöldi áætlaðra ítrekana innan samstæðu** skal færa inn ‚2‘. Áætlunarflokkur innan samstæðu 10 er með tvo meðlimi. Til að dreifa seinkanir frá upprunafyrirtæki (USMF) til fyrirtækis viðskiptavinar (DEMF), þarf að keyra innan samstæðu í báðum fyrirtækjunum tvisvar sinnum. Fyrsta ítrekun mun dreifa eftirspurninni og auðkenna seinkanir í upprunafyrirtækinu (USMF). Önnur ítrekun mun dreifa seinkanir úr USMF til DEMF.  
6. Í reitnum **Fyrsta ítrekun** skal velja „Endurgerð“.
7. Í reitnum **Síðari ítrekanir** skal velja „Endurgerð“.
8. Í reitinn **Fjöldi þráða** skal færa inn tölu. Þetta táknar fjölda samhliða þráða sem er nota við áætlanagerð.  
9. Veljið **Í lagi**.

## <a name="view-the-result-of-the-plan"></a>Skoða niðurstaða áætlunar.

1. Í reitnum **Áætlun** velurðu fellilistahnappinn til að opna uppflettinguna.
2. Í listanum skal velja tengilinn í valinni línu. Veljið tengil StaticPlan. Þú þarft að vera í fyrirtæki USMF.  
3. Veldu **Tillögur**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]