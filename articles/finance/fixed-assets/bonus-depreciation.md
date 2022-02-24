---
title: Viðbótarafskriftir
description: Þessi grein veitir yfirlit yfir virknina viðbótarafskriftir.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBonus
audience: Application User
ms.reviewer: roschlom
ms.custom: 3621
ms.assetid: 835ec594-744e-461c-a676-1b9abc094173
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 41a59b9dfe0482c995cfefc7a70f63550794428d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969179"
---
# <a name="bonus-depreciation"></a>Viðbótarafskriftir

[!include [banner](../includes/banner.md)]

Þessi grein veitir yfirlit yfir virknina viðbótarafskriftir.

Fyrir viðbótarafskriftir er hægt að taka aukalegar afskriftarupphæðir á fyrsta ári sem eign er í þjónustu og afskrifuð . Viðbótarafskriftir verður að taka á undan öðrum afskriftaútreikningum. Þess vegna er best að nota viðbótarafskriftir með bækur þar sem Bóka á fjárhag virkni er óvirkur. Hægt er að nota **Eyða færslum sem eru ekki bókaðar í fjárhag** valkost til að eyða sögulegum færslum fyrir bókum sem ekki bóka í fjárhag. Svo er hægt að hýsa viðbótarafskriftir síðar í líftíma eignar með því að eyða afskriftarfærslum sem voru áður bókaðar. 

Hægt er að reikna út viðbótarafskriftir með því að nota tillöguferli og hægt er að stofna handvirkar færslur viðbótarafskrifta. Ekki er hægt að stofna viðbótarafsrkiftir ef afskriftarfærslur eða -breytingar eru þegar til fyrir viðkomandi eignabók.

Þegar tillöguferli er notað til að reikna viðbótarafskriftir eru allar tiltækar viðbótarfærslur hafðar með í útreikningi á grunninum. Útreikningurinn inniheldur einnig allar fyrri viðbótarafskriftir sem voru færðar inn handvirkt fyrir eignina. 

Þegar gera á fleiri en eina afskrift fyrir eign er tekið tillit til forgangs. Hver viðbót dregur úr grunni fyrir næstu viðbót. Ekki er tekið tillit til hrakvirðis í eignagrundvelli fyrir útreikning viðbótarafskriftar og afskriftarhefð á ekki við fyrir viðbótarafskriftir. 

Eins og er falla ákveðnar eignir undir eignir í Kafla 179 í Bandaríkjunum. Með því að nota frádrátt Kafla 179 er hægt að endurheimta allt eða hluta af kostnaði við tiltekna eignir, upp að mörkum. Hægt er að endurheimta kostnað með því að draga hann frá á árinu þegar þú setur eign í þjónustu.

## <a name="example"></a>Dæmi
Eftirfarandi viðbótaruppskriftir eru tengdar eignabók:

-   **Kafli 179**: $1.000,00, Forgangur 1
-   **Liberty Zone**: 30%, Forgangur 2

Stofnkostnaðurinn er 5.000,00. Þegar viðbótarafskrift er reiknaður er fyrsta upphæð viðbótaruppskriftar 1.000,00 fyrir Kafla 179 afskrift. 

Upphæð næstu viðbótarafskriftar, fyrir afskrift Liberty Zone, er reiknuð á eftirfarandi: 

Kaupverð - $1.000 (afskrift Kafla 179) x 30% = 1.200 

Ef upphæð viðbótarafskriftar er hærri en eftirstandandi kaupverð er upphæð viðbótarafskrifta annað hvort niðurstaða útreikningur viðbótarafskrifta eða eftirstandandi kaupverð, hvort heldur sem er lægri. 

Ef eftirstandandi kaupverð er 0 eða minna verða viðbótarafskriftafærslur ekki myndaðar. 

Þegar viðbótarafskrift er reiknuð með tillöguferlinu er viðbótarafskriftarfærsla stofnuð fyrir allar viðeigandi skrár viðbótarafskrifta sem tengjast eignabók. 

Hægt er að stofna ótakmarkaðan fjölda af viðbótarafskriftafærslum. Eftir að þessum færslum hefur verið úthlutað á eignaflokka eru þær notaðar í eignabók. 

Viðbótarafskriftir eru færðar inn sem prósenta eða föst upphæð. Þegar þú bókar afskriftartillögur eru bókaðar viðbótarafskriftafærslur í bókina sem aðskildar færslur úr afskriftarfærslum.



