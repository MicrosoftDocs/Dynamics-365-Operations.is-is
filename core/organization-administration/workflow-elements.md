---
title: "Verkflæðiseiningar"
description: "Þessi grein lýsir hinum ýmsu þáttum sem verkflæði samanstendur af."
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 56441
ms.assetid: de740262-6ffd-42b9-a325-540eae5cec94
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: ee20b567b402bf638a54f6394159f7f8a9f02da6
ms.lasthandoff: 03/31/2017


---

# <a name="workflow-elements"></a>Verkflæðiseiningar

[!include[banner](../includes/banner.md)]


Þessi grein lýsir hinum ýmsu þáttum sem verkflæði samanstendur af.

Verkflæði samanstendur af einingum. Eftirfarandi hlutar útskýra hverja einingu gerð einingar.

## <a name="tasks"></a>Verk
*Verkefni * er vinnueining sem þarf að vinna. Tvær gerðir af verkum má bæta við verkflæði: handvirk verk og sjálfvirk verk.

### <a name="manual-task"></a>Handvirk verk

*Handvirkt Verkefni * er vinnueining sem notandinn þarf að vinna. Til dæmis getur verkflæði kostnaðarskýrslu haft handvirkt verk sem krefjast þess af skráðum notendum að ljúka eftirfarandi aðgerðum:

-   Endurskoða innhreyfingarnar sem eru sendar með kostnaðarskýrslu.
-   Hringjá í yfirmann starfsmanns

### <a name="automated-task"></a>Sjálfvirkt verk

*Sjálfvirkt Verkefni * er vinnueining sem kerfið þarf að vinna. Engin mannleg samskipti eru nauðsynleg. Til dæmis getur verkflæði sölupöntunar haft sjálfvirkt verk sem krefjast þess af kerfinu að ljúka eftirfarandi aðgerðum:

-   Framkvæma athugun á lánamarki.
-   Stofna færsla viðskiptavinar fyrir viðskiptavininn, ef færsla er ekki þegar til.

## <a name="approval-processes"></a>samþykktarferli
*Samþykktarferli* er ferli felur í sér nokkur skref. Notandinn á hverju samþykktarskrefi getur framkvæmt eftirfarandi aðgerðir:

-   Samþykkja skjalið.
-   Hafna skjalinu.
-   Biðja um breytingu á skjalinu.
-   Úthluta skjalinu til annars notanda til samþykktar.

## <a name="lineitem-workflow-elements"></a>Verkflæðiseining línuatriðis
Hægt er að stofna verkflæði til að vinna annað hvort úr skjölum eða línuvörum á skjali. Til dæmis hefur verið stofnað samþykkisverkflæði fyrir vinnukort. (Vísað verður í þetta verkflæði sem *skjalaverkflæði*.) Hægt er að bæta við einingunni *verkflæði línuatriðis* í þetta skjalaverkflæði. Þegar eining línuatriðis er keyrt, er hvert línuatriði á skjalinu sent til vinnslu. Þú gætir viljað að öll línuatriðin séu innin með sama verkflæði línuatriðis eða þú gætir viljað láta vinna hvert línuatriði af mismunandi verkflæði línuvöru. Hugsum hafi starfsmaður hefur senda vinnukort sem svipar eftirfarandi tala. ![Verkflæði með línuatriði](./media/workflow_lineitemworkflow.gif) í þessum aðstæðum gætirðu viljað stofna eftirfarandi verkflæði línuatriðis:

-   **verkflæði línuatriðis 1** – Þetta verkflæði er notað til að vinna línuatriði þar sem verkkennið er 1111.
-   **Verkflæði línuatriðis 2** – Þetta verkflæði er notað til að vinna línuatriði þar sem verkkennið er 2222.
-   **Verkflæði línuatriðis 3** – Þetta verkflæði er notað til að vinna línuatriði þar sem verkkennið er 3333.

## <a name="flowcontrol-elements"></a>Einingar flæðistýringar
Eftirfarandi einingar gera þér kleift að hanna verkflæði sem hafa aðrar greinar eða greinar sem keyra á sama tíma.

### <a name="manual-decision"></a>Handvirk ákvörðun

*Handvirk ákvörðun * er punktur þar sem verkflæði skiptist í tvær greinar. Notandi verður að gera ákvörðun og þessi ákvörðun ákveður hvaða grein er notuð til að vinna úr skjali sem sent var inn.

### <a name="conditional-decision"></a>Skilyrt ákvörðun

*Skilyrt ákvörðun * er einnig punktur þar sem verkflæði skiptist í tvær greinar. Hinsvegar ákvarðar kerfið hvaða grein er notuð til að vinna úr skjali sem sent var inn. Til að gera þetta ákvörðun, metur kerfið skjals til að ákvarða hvort það uppfyllir tilgreind skilyrði.

### <a name="parallel-activity"></a>Hliðstæður verkþáttur

*hliðstæður verkþáttur* er verkflæðiseining sem inniheldur tvær eða fleiri verkflæðisgreinar sem eru keyrðar á sama tíma

### <a name="subworkflow"></a>Undirverkflæði

*Undirverkflæði * er verkflæði sem keirir í samhengi við annað yfirverkflæði.




