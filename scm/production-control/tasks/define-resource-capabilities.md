--- 
title: "Skilgreina möguleika tilfanga"
description: "Tilfangageta lýsa því hvað rekstrartilföng getur gert."
author: sorenva
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 4a7d342eeb16fd76f2dde58151bfc7973de76e2d
ms.contentlocale: is-is
ms.lasthandoff: 07/27/2017

---
# <a name="define-resource-capabilities"></a>Skilgreina möguleika tilfanga

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tilfangageta lýsa því hvað rekstrartilföng getur gert. Við áætlunargerð, eru allar kröfur vinnslu og jafnaðar gagnvart getu tiltæk tilfanga. Þessi leiðarvísi fyrir verk aðstoðar við að stofna getu tilfangs og úthluta á tilföngum. Sýnigögn gögn fyrirtækisins til að stofna verkið er USMF.


## <a name="create-a-resource-capability"></a>Stofna tilfangagetu.
1. Fara á Tilfangagetu
2. Smellt er á Nýtt.
3. Færið inn Kenni tilfangagetu í svæðinu Getu.
    * Fyrir tiltekna aðgerð, notarðu auðkenni getu til að tilgreina að tilfanga verður að hafa þennan getu til að framkvæma aðgerðina.  
4. Í reitinn Lýsing er færð stutt lýsing á getunni.

## <a name="assign-capability-to-a-resource"></a>Úthluta getu á tilföng
1. Smelltu á Bæta við.
2. Færið inn Kenni tilfanga í svæðinu Tilfanga.
    * Hægt er að úthluta getu tilfangs á ein eða fleiri tilföng.  
3. Í reitinn lokadagsetning, skal færa inn dagsetningu.
    * Hægt er að nota þetta svæði til að tilgreina að tilföng hefur getuna fyrir aðeins takmarkaðan tíma.  
4. Í reitinn forgangur skal slá inn númer.
    * Þegar þú áætlar vinnslur og aðgerðir, hægt er að tilgreina hvort að velja tilföng eftir forgangi. Ef valið er að gera þetta, og fleiri en einn tilföng geta framkvæmt vinnslu eða aðgerðar á umbeðna dagsetningu, er valið tilfang með minnstan forgang með tilliti til getu sem krafist er.  
5. Í reitinn Stig skal slá inn númer.
    * Þegar tilgreindur er vinnslu eða aðgerð sem krefst tiltekna getu, er einnig hægt að tilgreina lágmarksstig sem krafist er. Notaðu getistig til að aðgreina tilföng sem geta framkvæmt sömu vinnslu en með mismunandi hraða, styrkleikum, stærðir og svo framvegis.  


