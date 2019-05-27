---
title: Samþætting fyrir þjónustusamninga og verk
description: Þegar unnið er með þjónustusamninga og þjónustusamningslínur eru notuð gögn sem sett eru upp í svæðunum í „Verkefnastjórnun og bókhald“.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6bd2fb1f54a3decb77f019db6b2016cebdcaddb9
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571049"
---
# <a name="integration-for-service-agreements-and-projects"></a>Samþætting fyrir þjónustusamninga og verk 

[!include [banner](../includes/banner.md)]


Þegar unnið er með þjónustusamninga og þjónustusamningslínur eru notuð gögn sem sett eru upp í eftirfarandi svæðum í **Verkefnastjórnun og bókhald**.

## <a name="project-prices"></a>Verkverð

Kostnaðar- og söluverð á færslu þjónustusamnings er fengið frá uppsetningu kostnaðarverðs sem á við um verkið sem fylgir þjónustusamningnum. Kostnaðar- og söluverð er hægt að setja upp eftir verki, starfsmanni og flokki. 

## <a name="project-validation"></a>Villuleit verks

Hægt er að takmarka val á verkum, starfsmönnum og flokkum sem eru í boði fyrir þjónustusamningslínu með villuleitaruppsetningu í **Verkefnastjórnun og bókhald**. Með villuleitaruppsetningunni er hægt að sameina starfsmenn, verk og flokka til að stjórna aðgangi. 

## <a name="project-line-properties"></a>Línueiginleikar verks

Línueiginleiki er sleginn inn sjálfvirkt fyrir þjónustusamningslínu.

Línueiginleikar eru búnir til í skjámyndinni **Línueiginleikar** í **Verkefnastjórnun og bókhald**. Línueiginleikinn sem er sleginn inn í þjónustusamning er tengdur við verkið sem valið er fyrir þjónustusamninginn sem þjónustusamningslínan erfir síðan. 

## <a name="default-offset-accounts"></a>Sjálfgefnir mótlyklar

Ef þú slærð inn kostnaðarfærslu er sjálfgefinn kostnaðarmótlykill valinn sjálfkrafa fyrir færsluna. Sjálfgefni kostnaðarlykillinn er settur upp fyrir verkið sem fylgir núverandi þjónustusamningi.

## <a name="project-categories"></a>Verktegundir

Flokkarnir sem eru tiltækir fyrir þjónustusamningslínur eru settir upp í skjámyndinni **Verktegundir** í **Verkefnastjórnun og bókhald**. 

> [!NOTE]
> <P>Hægt er að velja flokkana sem hafa gátreitinn <STRONG>Virkir í færslubókum</STRONG> valdan í flipanum <STRONG>Verk</STRONG> í skjámyndinni <STRONG>Verktegundir</STRONG>. Hins vegar er í boði að velja alla flokka ef gátreiturinn <STRONG>Óvirkir flokkar</STRONG> er valinn í flipanum <STRONG>Færslubækur</STRONG> í skjámyndinni <STRONG>Verkefnastjórnun og bókhaldsbreytur</STRONG>.</P>

## <a name="project-parameters"></a>Færibreytur verka

Ef reiturinn **Starfsfólk sem er hætt** í flipanum **Færslubækur** í skjámyndinni **Verkefnastjórnun og bókhaldsfæribreytur** er valinn er hægt að velja óvirka og virka starfsmenn í skjámyndunum **Þjónustusamningar** og **Þjónustupantanir**.

Einnig er hægt að virkja reitina **Upphafstími** og **Lokatími** í flipanum **Verk** í skjámyndinni **Þjónustupantanir** til að færa inn upphafs- og lokatíma á þjónustupöntunarlínum.

## <a name="enable-the-starting-and-ending-time-feature-for-service-orders"></a>Virkja eiginleika upphafs- og lokatíma fyrir þjónustupantanir

1.  Smelltu á **Verkefnastjórnun og bókhald** \> **Uppsetning** \> **Verkefnastjórnun og bókhaldsfæribreytur**.

2.  Smelltu á flipann **Færslubækur** og veldu síðan gátreitinn **Sýna upphafs/lokatíma**.

3.  Smelltu á **Verkefnastjórnun og bókhald** \> **Uppsetning** \> **Færslubækur** \> **Heiti færslubóka**.

4.  Veldu heiti færslubókar sem fylgir þjónustupöntuninni.

5.  Smelltu á flipann **Almennt** og veldu síðan gátreitinn **Sýna upphafs/lokatíma**.


> [!NOTE]
> <P>Veldu heiti færslubókar fyrir þjónustupöntunina í reitnum <STRONG>Klst</STRONG> í flipanum <STRONG>Færslubækur</STRONG> í skjámyndinni <STRONG>Færibreytur þjónustustjórnunar</STRONG>.</P>





