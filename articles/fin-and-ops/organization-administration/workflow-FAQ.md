---
title: Algengar spurningar um verkflæði
description: Þetta efnisatriði svarar algengum spurningum um verkflæðiskerfið í Microsoft Dynamics 365 for Finance and Operations.
author: ChrisGarty
manager: AnnBe
ms.date: 05/07/2019
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
ms.openlocfilehash: f6240b1b5136937aa47f455547fed6f0c7c08e2c
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/07/2019
ms.locfileid: "1509292"
---
# <a name="workflow-system"></a>Verkflæðiskerfi

[!include [banner](../includes/banner.md)]

Þetta efnisatriði svarar algengum spurningum um verkflæðiskerfið í Microsoft Dynamics 365 for Finance and Operations.

## <a name="notifications"></a>Tilkynningar

### <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a>Hvers vegna koma margar tilkynningar þegar vinnulið er hafnað?
Þegar vinnulið er hafnað er honum lokið sem höfnuðum. Annar vinnuliður er stofnaður og honum er úthlutað á upphaflegan aðila. Þetta þýðir að tilkynning er send á upphaflegan aðila vegna hafnaðs vinnuliðar og aðskilin tilkynning send á notandann sem fær úthlutaðan nýja vinnuliðinn „beiðni um breytingu“. 

Hver tilkynning er fyrir mismunandi vinnulið, en líkindin geta valdið ruglingi. Við erum að skoða leiðir til að bæta þetta í framtíðarútgáfu.

### <a name="why-are-my-workflow-exports-failing"></a>Afhverju eru útflutningar á verkflæðum að mistakast?
Sem stendur eru takmörk á eiginleikanum fyrir útflutning verkflæðis sem koma í veg fyrir að heiti verkflæða séu lengri en 48 stafir. Að nota heiti sem er lengra en 48 stafir getur leitt til villunnar „Þjónn gat ekki sannvottað beiðnina“ og/eða komið í veg fyrir að skrá verði flutt út án skráargerðar. Eftirfarandi bloggfærsla veitir frekari upplýsingar [Úrræðaleit fyrir útflutning verkflæðis](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).
