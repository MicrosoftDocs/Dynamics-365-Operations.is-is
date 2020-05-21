---
title: Stofna spárlíkön fyrir fjárhagsáætlanir verks
description: Í þessu efnisatriði er lýst hvernig á að stofna spárlíkön og eftirstöðvar fjárhagsáætlunar.
author: RadhikaRS
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 07e540f23a668b40a54906a67d87552fe991825a
ms.sourcegitcommit: 5de75c61c33e57c813944f1ab6100aceb020d432
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/29/2020
ms.locfileid: "3321780"
---
# <a name="create-forecast-models-for-project-budgets"></a>Stofna spárlíkön fyrir fjárhagsáætlanir verks 

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er lýst hvernig á að stofna spárlíkön og eftirstöðvar fjárhagsáætlunar. Verk sem er háð fjárhagsáætlunarstýringu notar tvær gerðir áætlana: upprunaleg og eftirstöðvar. Þegar fjárhagsáætlun verks er stofnuð verður fyrst að tilgreina upprunalegu fjárhagsáætlunina og spálíkön eftirstöðva fjárhagsáætlunar sem voru stofnaðar á síðunni **Spárlíkön**. Fjárhagsáætlanir verks sem byggjast á tilteknum líkönum eru stofnaðar þegar verkáætlun er staðfest.

> [!NOTE]
> Spárlíkan sem er notað fyrir fjárhagsáætlunarstýringu getur ekki haft undirlíkan og ekki er hægt að nota það sem undirlíkan.

1. Veljið **Verkefnastjórnun og bókhald** > **Uppsetning** > **Spár**  > **Spárlíkön**.
2. Veldu **Nýtt** til að stofna nýtt spárlíkan og færðu inn kenninúmer líkans og heiti þess. 
3. Stilltu valkostinn **Stöðvað** á **Já** til að koma i veg fyrir breytingar á spárlínum fyrir spárlíkanið. 
4. Ef spálínurnar sem líkanið tengist mynda sjóðsstreymisspá í fjárhagnum skal stilla **Telja með í sjóðsstreymisspám** á **Já**. 
5. Til að nota verkdagsetningu sem reikningsdagsetningu skal stilla **Reikningsdagsetning í spá** á **Já**. 
6. Í **Gerð fjárhagsáætlunar** skal velja eina eftirfarandi líkanagerð:

   - **Upprunaleg fjárhagsáætlun**: Notið þetta fyrir upprunalegar upphæðir áætlana sem hefur verið ráðstafað þegar upphaflega fjárhagsáætlunin er stofnuð og samþykkt.
   - **Eftirstöðvar fjárhagsáætlunar**: Notið þetta fyrir upphæðir eftirstöðvar fjárhagsáætlunar á líftíma verksins. Staðan í þessu spárlíkani er lækkuð með raunverulegum færslum og aukin eða minnkuð með endurskoðun fjárhagsáætlunar.
   - **Yfirfæra**: Nota upphæð fjárhagsáætlunar frá fyrra tímabili fyrir verkið. Yfirfærsla er valfrjálst ferli sem hægt er að keyra til að flytja ónotaðar upphæðir fjárhagsáætlana frá einu fjárhagsári til annars.

7. Stillið eftirfarandi valmöguleika eins og krafist er:

   - Virkið **Reikningsdagsetning í spá** til að nota dagsetningu verksins sem dagsetningu reiknings.
   - Virkjaðu **Spá með VÍV** til að spá með verkum í vinnslu (VÍV) og velja svo VÍV-gerðina. 
   - Hægt er að halda sjálfgefinni **Gerð fjárhagsáætlunar** sem **Engin** eða slá inn nýja gerð. Ekki er hægt að breyta gerð fjárhagsáætlunar eftir að færslu er breytt.     
    > [!NOTE]
    > Ef sjálfgefinni fjárhagsáætlunargerð er breytt verða allir aðrir valmöguleikar óaðgengilegir fyrir uppfærslur og ekki er hægt að endurnýta spárlíkanið. 
   


 

