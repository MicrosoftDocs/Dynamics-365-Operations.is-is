---
title: "Leyst úr ósamræmi við jöfnun samtalna reiknings"
description: "Hægt er að nota jöfnun fyrir samtölur reiknings til að aðstoða við að tryggja að heildarreikningsupphæð víki ekki frá áætluðum upphæðum með meira en leyfileg frávikum."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendTotalPriceTolerance
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 63413
ms.assetid: 9ac42457-95b2-4191-ad06-c7e323704466
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 18250a735d0421daa90b923504aeb94b5003a6a7
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="resolve-discrepancies-during-invoice-totals-matching"></a>Leyst úr ósamræmi við jöfnun samtalna reiknings

[!include [banner](../includes/banner.md)]

Ein gerð villuprófunar á reikningsjöfnun er jöfnun fyrir samtölur reiknings. Til að tilgreina að kerfið eigi að framkvæma jöfnun fyrir samtölur reiknings, á **Færibreytur viðskiptaskulda** síðunni í **Reikningaprófun** flipanum skal stilla **Jafna samtölur reiknings** valkostinn á **Já**. 

Hægt er að nota jöfnun fyrir samtölur reiknings til að aðstoða við að tryggja að heildarreikningsupphæð víki ekki frá áætluðum upphæðum með meira en leyfileg frávikum. Sex samtölur eru bornar saman á síðunni **Upplýsingar um jöfnun á samtölum reiknings**. Ef ein af samtölunum víkur frá áætlaðri samsvarandi heildar innkaupapöntun er jöfnunarmisræmi merkt. 

Til að fara yfir reikning sem hefur misræmi í samtölum, í **Reikningsfærsla lánardrottins** vinnusvæðinu skal smella á **Biðreikningar** reitinn. Í Aðgerðasvæði, á **Yfirfara** flipanum, smellið á **Samsvörunarupplýsingar**. Ef misræmi hefur fundist birtist viðvörunartákn við upphæð reiknings. Hægt er að skoða frekari upplýsingar um samtölur með því að skoða upplýsingar um samsvörun reikninga. 

Eftir að kennsl hafa verið borin á misræmið, gæti verið að það þurfi að hafa samband við lánardrottinninn ef talið er að upplýsingarnar á reikningnum séu ekki réttar. Það er síðan háð samkomulagi við lánardrottinn, hver eftirfarandi verka verða framkvæmd:

-   Samþykkja verðmismun og bóka reikninginn með misræmi í samsvörun. Kerfið getur sett upp að krefjast eigi samþykkis áður en hægt er að bóka ef misræmi eru í samsvörun. Í þessu tilfelli er að samþykkja misræmi í samsvörun og einnig er hægt að færa inn athugasemd um samþykki. Síðan er hægt að velja að bóka reikninginn.
-   Endurskoða reikningsupphæð skv. þeirri upphæð sem reiknað var með og bóka reikninginn þannig..
-   Biðja um fullan kreditreikning og nýjan leiðréttan reikning frá lánardrottni.

Nánari upplýsingar er að finna í [Rannsaka eða leysa úr undantekningum](tasks/research-resolve-exceptions.md)



