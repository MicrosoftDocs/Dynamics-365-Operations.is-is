---
title: Breyta afhendingarmáta í POS
description: Þetta efni lýsir því hvernig á að stilla og nota breytingamáta fyrir afhendingu í POS.
author: hhainesms
manager: annbe
ms.date: 03/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhainesms
ms.search.validFrom: 2020-02-20
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: d2691ef6b08a44a845857c34fe60072211364f82
ms.sourcegitcommit: 02640a0f63daa9e509146641824ed623c4d69c7f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/16/2020
ms.locfileid: "3265481"
---
# <a name="change-mode-of-delivery-in-pos"></a>Breyta afhendingarmáta í POS

[!include [banner](includes/banner.md)]

Þetta efnisatriði lýsir því hvernig á að setja upp og nota „breyting á afhendingarstillingu“ virkni í sölustað (POS) umhverfi þínu. 

Í Dynamics 365 Commerce útgáfur 10.0.10 og nýrri, **Breyta afhendingaraðferð** aðgerð (647) er tiltæk til að bæta við POS skjáuppsetninguna þína.

Breytingarháttur afhendingaraðgerðar veitir þér möguleika á að breyta afhendingarháttum fyrir eina eða fleiri sölulínur fyrir sendingu í POS viðskiptunum. Í fyrri útgáfum af viðskiptum varstu að fara í gegnum það í heild sinni **Senda allt** eða **Senda valið** stillingar streyma ef þú vilt breyta afhendingarháttum á núverandi línu sem var stillt til sendingar. Þetta ferli var tímafrekt og gæti valdið slysni breytingum á uppruna afhendingar eða afhendingardögum fyrir línuna. Hin nýja virkni býður upp á aðra aðferð til að uppfæra skilvirkni á þessum sölulínum á skilvirkan hátt.

Nánari upplýsingar um hvernig á að bæta aðgerð við hnapp á POS hnapparitinu, sjá [Skjáuppsetning fyrir sölustað](https://docs.microsoft.com/dynamics365/commerce/pos-screen-layouts).

Eftir að þessi aðgerð er stillt í POS, þegar þú velur **Breyta afhendingaraðferð**, verður þér kynnt listasíða sem gerir þér kleift að velja línurnar í viðskiptunum sem þú vilt breyta afhendingarháttum fyrir. Þú getur valið nokkrar eða allar línurnar, eða lokað án þess að gera neinar breytingar. Sölulínurnar sem áður voru stilltar til sendingar eru einu línurnar á listanum sem þú getur breytt. Ef þú vilt breyta línu sem er ætluð til afhendingar eða flutnings í skip, verður þú að nota **Senda allt** eða **Senda valið** aðgerðir. Hins vegar, ef þú vilt breyta línu sem er tilgreind sem sending í pallbíll eða flutning, verður þú að nota **Sækja allt**, **Sækja valið**, **Framkvæma allt** eða **Framkvæma valið** aðgerðir.

Eftir að þú hefur valið línurnar sem þú vilt breyta, smelltu á **Breyta afhendingaraðferð** að vera beðinn um að velja valkosti afhendingarstillingar. Ef þú valdir margar línur til að breyta, birtir POS aðeins afhendingaraðferðir sem hafa verið stilltir sem leyfilegt fyrir allar valdar vörur. Hægt er að stilla afhendingaraðferðir til að styðja við tilteknar vörur og afhendingarföng. Ef það er til staðar afhendingarstaður sem er ásættanlegur fyrir eina vöru- og heimilisfangasamsetningu en er ekki ásættanlegur fyrir aðra valda vöru- og heimilisfangasamsetningu, er afhendingarháttur ekki tiltækur. Þú gætir þurft að velja línur einn í einu og breyta afhendingarháttum fyrir hverja línu fyrir sig ef þú vilt velja afhendingaraðferð fyrir eina vöru sem er ekki studd af annarri vöru.  

Eftir að þú hefur valið nýja afhendingarstillingu birtist viðskiptasíðan. Til að skoða nýju afhendingarstillingarnar þínar skaltu velja flipann **Afhending** á færslulistanum.   
