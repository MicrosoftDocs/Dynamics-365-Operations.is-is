---
title: Algengar spurningar um verkflæði
description: Þetta efnisatriði svarar algengum spurningum um verkflæðiskerfið í Microsoft Dynamics 365 for Finance and Operations.
author: ChrisGarty
manager: AnnBe
ms.date: 02/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f058a450eb18e688efbc5306a42b4efef6aa91e7
ms.sourcegitcommit: 9a723737565ac78c884e40f7129d0f5aad747524
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/01/2019
ms.locfileid: "773215"
---
# <a name="workflow-system"></a>Verkflæðiskerfi

[!include [banner](../includes/banner.md)]

Þetta efnisatriði svarar algengum spurningum um verkflæðiskerfið í Microsoft Dynamics 365 for Finance and Operations.

## <a name="notifications"></a>Tilkynningar

### <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a>Hvers vegna koma margar tilkynningar þegar vinnulið er hafnað?
Þegar vinnulið er hafnað er honum lokið sem höfnuðum. Annar vinnuliður er stofnaður og honum er úthlutað á upphaflegan aðila. Þetta þýðir að tilkynning er send á upphaflegan aðila vegna hafnaðs vinnuliðar og aðskilin tilkynning send á notandann sem fær úthlutaðan nýja vinnuliðinn „beiðni um breytingu“. 

Hver tilkynning er fyrir mismunandi vinnulið, en líkindin geta valdið ruglingi. Við erum að skoða leiðir til að bæta þetta í framtíðarútgáfu.
