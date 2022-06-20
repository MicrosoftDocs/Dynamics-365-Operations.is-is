---
title: Hætta við vinnslu aðaláætlunargerðar
description: Þessi grein útskýrir hvernig á að hætta við virka áætlunarvinnu sem notar innbyggða áætlunarvirkni.
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
ms.openlocfilehash: 6a9667be9921fdde7e1ca5de68c7f51d48905ac8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860784"
---
# <a name="cancel-a-master-planning-job"></a>Hætta við aðaláætlunarverk

[!include [banner](../includes/banner.md)]

Í Microsoft Dynamics 365 Supply Chain Management eru margir möguleikar til að hætta við aðaláætlunarverk. Til dæmis gætirðu viljað hætta við aðaláætlunarverk ef það var hafið fyrir mistök eða keyrir lengur en áætlað var og þú vilt slíta því. Besta leiðin til að hætta við áætlunarvinnslu er af síðunni **Ólokin áætlunarferli**. Aðrir valkostir af síðunum **Runuvinnslur** og **Runuvinnslur auknar** ætti að nota ef afturköllun á aðaláætlunarvinnslunni af síðunni **Ólokin áætlunarferli** lauk ekki innan nokkurra mínútna.

## <a name="preferred-cancel-option"></a>Æskilegur hætta við valkost
### <a name="cancel-master-planning-job-from-unfinished-planning-processes-page"></a>Hætta við aðaláætlunarvinnslu af síðunni **Ólokin áætlunarferli**
1. Farðu í **Aðaláætlanagerð > Fyrirspurnir og skýrslur > Aðaláætlanagerð > Ólokin áætlunarferli**.
2. Veldu línuna með áætlunarferlinu sem ætlunin er að afturkalla.
3. Smelltu á **Hætta við**.

## <a name="additional-cancel-options"></a>Aukaafturköllunarvalkostir
Þetta ætti aðeins að nota ef afturköllun á aðaláætlunarvinnslunni af síðunni **Ólokin áætlunarferli** lauk ekki innan nokkurra mínútna.

### <a name="delete-master-planning-job-from-the-batch-jobs-page"></a>Eyða aðaláætlanavinnslu af síðunni **Runuvinnslur**
1. Farðu í **Kerfisstjórnun > Fyrirspurnir> Runuvinnslur**.
2. Veldu línuna með áætlunarvinnslunni sem ætlunin er að eyða.
3. Smellið á **Eyða**.

### <a name="abort-master-planning-job-task-from-the-batch-jobs-enhanced-page"></a>Hætta við aðaláætlanavinnsluverk af síðunni **Runuvinnslur auknar**
1. Farðu í **Kerfisstjórnun > Fyrirspurnir> Runuvinnslur**.
2. Ef vinnslukenni birtist ekki á listanum skaltu smella á **Skipta yfir í aukna skjámynd**, annars skalta halda áfram með næsta skref.
3. Opnaðu runuvinnsluna. Smelltu á **Vinnslukenni** fyrir runuvinnsluna með verk sem þú vilt ljúka.
4. Í **Runuverk** velurðu verkin sem á að ljúka.
5. Smellið á **Breyta stöðu** veljið **Hætta við** og á **Í lagi**.
6. Á flýtiflipanum **Runuverk** smellirðu á **Hætta við**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]