---
title: "Setja upp samsvörunarreglur afstemmingar banka"
description: "Þessi grein útskýrir hvernig Hægt er að setja upp jöfnunarreglur afstemmingar og jöfnunarreglusett bankaafstemmingar til að aðstoða við afstemmingarferli bankans. Samsvörunarreglur afstemmingar eru safn skilyrða sem eru notuð til að sía bankayfirlitslínur og bankaskjalslínur á meðan á afsemmingarferlinu stendur."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BankReconciliationMatchRule, BankReconciliationMatchRuleSet
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 12971
ms.assetid: b5073f83-31dc-404f-af42-3fd84a02a7c6
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 3b16ef53f9fb57a6663db0be1f7e0a57471db2fb
ms.openlocfilehash: e4c07a6afb90535c57f372d5b850919b5b34aaa4
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-bank-reconciliation-matching-rules"></a>Setja upp samsvörunarreglur afstemmingar banka

Þessi grein útskýrir hvernig Hægt er að setja upp jöfnunarreglur afstemmingar og jöfnunarreglusett bankaafstemmingar til að aðstoða við afstemmingarferli bankans. Samsvörunarreglur afstemmingar eru safn skilyrða sem eru notuð til að sía bankayfirlitslínur og bankaskjalslínur á meðan á afsemmingarferlinu stendur.

Hægt er að setja upp jöfnunarreglur afstemmingar og jöfnunarreglusett bankaafstemmingar til að aðstoða við afstemmingarferli bankans. Samsvörunarreglu afstemmingar er safn skilyrða sem eru notaðar til að sía bankayfirlitslínur og Microsoft Dynamics 365 fyrir línur Aðgerðir banka afstemmingarferlinu. Nota skal síðuna **Jöfnunarreglur afstemmingarr** síðu til að setja upp reglur fyrir samsvörunarreglu afstemmingar. Hægt er að setja upp fleiri en eina jöfnunarreglu og stofna síðan jöfnunarreglusett á afstemmingar á síðunni **Jöfnunarreglusett afstemmingar**. 

> [!NOTE] 
> Jöfnunarreglur afstemmingar eru notaðar ef um er að afstemma bankayfirlit til rafræna með því að nota fyrirframgreiðslu bankaafstemmingar. 

Á síðunni **Jöfnunarreglur afstemmingar** er hægt að velja hvaða aðgerðir og valskilyrði eru notuð við keyrslu jöfnunarreglu. Í því **Aðgerðir** svæðisflokknum, skal velja aðgerðina sem framkvæma skal þegar jöfnunarreglan er keyrð meðan á afstemmingu stendur.  

> [!NOTE] 
> Kosturinn sem er valinn ákvarðar svæðin sem birtast.

|                                    |                                                                                                                                                                                                                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Aðgerð**                         |                                                                                                                                                                                                                                                                                                               | **Valskilyrði tiltæk þegar aðgerð er valin.**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Jafna með bankaskjali **       | Stofna skilyrði til að tilgreina hvernig bankaskjöl og bankayfirlitslínur eru jafnaðar þegar jöfnunarregla er keyrð af síðunni **Vinnublað bankaafstemmingar**. Færslulínur eru valdar samkvæmt uppsetningu aukaskilyrða á flýtiflipunum.                                | **1. skref: Skilgreina skal jöfnunarreglan** – Veljið criterias til að tilgreina hvaða bankayfirlit ætti að samsvara með Dynamics 365 fyrir Aðgerðir bankafærslur. **Skref 2 (valfrjálst): Velja uppgjörslínu til að keyra jöfnunarreglur gagnvart:** Beita síu á hvaða uppgjörslínu skal keyra reglur gagnvart.                                                                                                                                                                                                                                                                                                               |
| **Hreinsa bakfærslulínur** | Stofna skilyrði til að tilgreina hvernig bakfærslulínur eru fjarlægðar af síðunni **Vinnublað bankaafstemmingar** þegar jöfnunarkeyrsla er keyrð. Þessi valkostur er notaður þegar bankamistök valda því að tvær bankayfirlitslínur eru skráðar í innfluttu bankayfirliti og línurnar verður að stemma af. | **Skref 1**:** Finna bakfærðar uppgjörslínur **– Bæta við valskilyrðum til að velja bakfærslulínur banka. Til dæmis til að velja aðeins ávísanir skal velja **Bankafærslukóði** í reitnum Reitur, velja plúsmerkið (+) í reitnum **Reiknimerki** og færa síðan inn **Ávísanir** í reitnum Gildi. **Skref 2: Finna upprunalegar uppgjörslínur **– Hægt er að bæta við valskilyrðum til að jafna línur í bankaskjali við bankafærslulínur. ** 3. skref: Finna Dynamics 365 Aðgerðir bankafærslur **-hægt er að bæta við valskilyrði til að passa við Dynamics 365 fyrir Aðgerðir bankafærslum í bankayfirlitslínur. |
| **Mark new transactions**          | Stofna skilyrði til að tilgreina hvernig nýjar línur skulu merktar á síðunni **Vinnublað bankaafstemmingar** þegar jöfnunarkeyrsla er keyrð.                                                                                                                                                                 | **Skref 1: Finna uppgjörslínur **– Bæta við valreitum til að tilgreina hvaða bankayfirlitslínur ætti að velja af síðunni **Vinnublað bankaafstemmingar**. ** 2. skref: Finna Dynamics 365 Aðgerðir bankafærslur ** – hægt er að bæta við valskilyrði til að leita bankaskjalslínur. Ef ekkert bankaskjal finnst verður uppgjörslína merkt sem ný færsla.                                                                                                                                                                                                                                             |

 





