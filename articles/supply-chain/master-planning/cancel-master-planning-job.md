---
title: Hætta við verk sem var stofnað með úreltri aðaláætlunarvél
description: Þessi grein útskýrir hvernig á að hætta við virkt áætlunarverk sem notar úrelta aðalskipulagsvél.
author: t-benebo
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace, ReqProcessList
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-12-16
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7b71a43f407050dccb7550db7c4b6a98a596d589
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740878"
---
# <a name="cancel-a-job-that-was-created-using-the-deprecated-master-planning-engine"></a>Hætta við verk sem var stofnað með úreltri aðaláætlunarvél

[!include [banner](../includes/banner.md)]

Það eru margir valkostir til að hætta við verk sem var stofnað með úreltri aðaláætlunarvél. Til dæmis gætirðu viljað hætta við aðaláætlunarverk ef það var hafið fyrir mistök eða keyrir lengur en áætlað var og þú vilt slíta því.

Besta leiðin til að hætta við áætlunarvinnslu er af síðunni **Ólokin áætlunarferli**. Aðrir valkostir af síðunum **Runuvinnslur** og **Runuvinnslur auknar** ætti að nota ef afturköllun á aðaláætlunarvinnslunni af síðunni **Ólokin áætlunarferli** lauk ekki innan nokkurra mínútna.

## <a name="preferred-cancel-option"></a>Æskilegur hætta við valkost

### <a name="cancel-master-planning-job-from-the-unfinished-planning-processes-page"></a>Hætta við aðalskipulagsvinnu af síðunni Ólokin áætlunarferli

1. Farðu í **Aðaláætlanagerð > Fyrirspurnir og skýrslur > Aðaláætlanagerð > Ólokin áætlunarferli**.
2. Veldu línuna með áætlunarferlinu sem ætlunin er að afturkalla.
3. Veldu **Hætta við**.

## <a name="additional-cancel-options"></a>Aukaafturköllunarvalkostir

Þetta ætti aðeins að nota ef afturköllun á aðaláætlunarvinnslunni af síðunni **Ólokin áætlunarferli** lauk ekki innan nokkurra mínútna.

### <a name="delete-master-planning-job-from-the-batch-jobs-page"></a>Eyða aðaláætlanavinnslu af síðunni **Runuvinnslur**

1. Farðu í **Kerfisstjórnun > Fyrirspurnir> Runuvinnslur**.
2. Veldu línuna með áætlunarvinnslunni sem ætlunin er að eyða.
3. Veljið **Eyða**.

### <a name="abort-master-planning-job-task-from-the-batch-jobs-enhanced-page"></a>Hætta við aðaláætlanavinnsluverk af síðunni **Runuvinnslur auknar**

1. Farðu í **Kerfisstjórnun > Fyrirspurnir> Runuvinnslur**.
2. Ef vinnslukenni birtist ekki á listanum skaltu smella á **Skipta yfir í aukna skjámynd**, annars skalta halda áfram með næsta skref.
3. Opnaðu runuvinnsluna. Veldu **Vinnslukenni** fyrir runuvinnsluna með verkum sem þú vilt ljúka.
4. Í **Runuverk** velurðu verkin sem á að ljúka.
5. Veljið **Breyta stöðu** veljið **Hætta við** og á **Í lagi**.
6. Á flýtiflipanum **Runuverk** smellirðu á **Hætta við**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]