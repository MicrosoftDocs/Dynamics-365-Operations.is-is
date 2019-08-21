---
title: Uppsetning samsvörunarreglna bankaafstemmingar
description: Þetta efnisatriði útskýrir hvernig Hægt er að setja upp jöfnunarreglur afstemmingar og jöfnunarreglusett bankaafstemmingar til að aðstoða við afstemmingarferli bankans. Samsvörunarreglur afstemmingar eru safn skilyrða sem eru notuð til að sía bankayfirlitslínur og bankaskjalslínur á meðan á afsemmingarferlinu stendur.
author: ShylaThompson
manager: AnnBe
ms.date: 10/27/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankReconciliationMatchRule, BankReconciliationMatchRuleSet
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 12971
ms.assetid: b5073f83-31dc-404f-af42-3fd84a02a7c6
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8ced5d7b00fd512d0af0fb88f9d30042213b6908
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1842234"
---
# <a name="set-up-bank-reconciliation-matching-rules"></a>Uppsetning samsvörunarreglna bankaafstemmingar

[!include [banner](../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig Hægt er að setja upp jöfnunarreglur afstemmingar og jöfnunarreglusett bankaafstemmingar til að aðstoða við afstemmingarferli bankans. Samsvörunarreglur afstemmingar eru safn skilyrða sem eru notuð til að sía bankayfirlitslínur og bankaskjalslínur á meðan á afsemmingarferlinu stendur.

Hægt er að setja upp jöfnunarreglur afstemmingar og jöfnunarreglusett bankaafstemmingar til að aðstoða við afstemmingarferli bankans. Jöfnunarregla afstemmingar er safn skilyrða sem eru notuð til að sía bankayfirlitslínur og bankaskjalslínur Microsoft Dynamics 365 for Finance and Operations á meðan á afstemmingarferlinu stendur. Nota skal síðuna **Jöfnunarreglur afstemmingarr** síðu til að setja upp reglur fyrir samsvörunarreglu afstemmingar. Hægt er að setja upp fleiri en eina jöfnunarreglu og stofna síðan jöfnunarreglusett á afstemmingar á síðunni **Jöfnunarreglusett afstemmingar**. 

> [!NOTE] 
> Jöfnunarreglur afstemmingar banka eru notaðar þegar verið er að stemma af rafrænt bankayfirlit með því að nota ítarlega bankaafstemmingu. 

Á síðunni **Jöfnunarreglur afstemmingar** er hægt að velja hvaða aðgerðir og valskilyrði eru notuð við keyrslu jöfnunarreglu. Í reitaflokknum **Aðgerðir** skal velja aðgerðina sem verður framkvæmd þegar jöfnunarreglan er keyrð meðan á afstemmingu stendur.  

> [!NOTE] 
> Kosturinn sem er valinn ákvarðar reitina sem birtast.

|                                    |                                                                                                                                                                                                                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Aðgerð**                         |                                                                                                                                                                                                                                                                                                               | **Valskilyrði tiltæk þegar aðgerð er valin.**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Jafna með bankaskjali**       | Stofna skilyrði til að tilgreina hvernig bankaskjöl og bankayfirlitslínur eru jafnaðar þegar jöfnunarregla er keyrð af síðunni **Vinnublað bankaafstemmingar**. Færslulínur eru valdar samkvæmt uppsetningu aukaskilyrða á flýtiflipunum.                                | **Skref 1: Skilgreina jöfnunarregluna** – Velja skilyrði til að tilgreina hvaða bankayfirlit ætti að jafna við bankafærslur Finance and Operations. **Skref 2 (valfrjálst): Velja uppgjörslínu til að keyra jöfnunarreglur gagnvart:**  Beita síu á hvaða uppgjörslínu skal keyra reglur gagnvart.                                                                                                                                                                                                                                                                                                               |
| **Hreinsa bakfærslulínur** | Stofna skilyrði til að tilgreina hvernig bakfærslulínur eru fjarlægðar af síðunni **Vinnublað bankaafstemmingar** þegar jöfnunarkeyrsla er keyrð. Þessi valkostur er notaður þegar bankamistök valda því að tvær bankayfirlitslínur eru skráðar í innfluttu bankayfirliti og línurnar verður að stemma af. | **Skref 1**: **Finna bakfærðar uppgjörslínur**– Bæta við valskilyrðum til að velja bakfærslulínur banka. Til dæmis til að velja aðeins ávísanir skal velja **Bankafærslukóði** í reitnum Reitur, velja plúsmerkið (+) í reitnum **Reiknimerki** og færa síðan inn **Ávísanir** í reitnum Gildi. **Skref 2: Finna upprunalegar uppgjörslínur**– Hægt er að bæta við valskilyrðum til að jafna línur í bankaskjali við bankafærslulínur. **Skref 3: Finna bankafærslur Finance and Operations** – Hægt er að bæta við valskilyrðum til að jafna Finance and Operations bankafærslur við bankafærslulínur. |
| **Merkja nýjar færslur**          | Stofna skilyrði til að tilgreina hvernig nýjar línur skulu merktar á síðunni **Vinnublað bankaafstemmingar** þegar jöfnunarkeyrsla er keyrð.                                                                                                                                                                 | **Skref 1: Finna uppgjörslínur**– Bæta við valreitum til að tilgreina hvaða bankayfirlitslínur ætti að velja af síðunni **Vinnublað bankaafstemmingar**. **Skref 2: Finna bankafærslur Finance and Operations** – Hægt er að bæta við valskilyrðum til að leita að bankaskjalslínum. Ef ekkert bankaskjal finnst verður uppgjörslína merkt sem ný færsla.                                                                                                                                                                                                                                             |








