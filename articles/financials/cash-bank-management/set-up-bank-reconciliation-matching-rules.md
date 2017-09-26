---
title: "Setja upp samsvörunarreglur afstemmingar banka"
description: "Þessi grein útskýrir hvernig Hægt er að setja upp jöfnunarreglur afstemmingar og jöfnunarreglusett bankaafstemmingar til að aðstoða við afstemmingarferli bankans. Samsvörunarreglur afstemmingar eru safn skilyrða sem eru notuð til að sía bankayfirlitslínur og bankaskjalslínur á meðan á afsemmingarferlinu stendur."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankReconciliationMatchRule, BankReconciliationMatchRuleSet
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 12971
ms.assetid: b5073f83-31dc-404f-af42-3fd84a02a7c6
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 60cd6a7f7b4d5c3acc68aa27c920f42f1d4b910e
ms.contentlocale: is-is
ms.lasthandoff: 06/13/2017


---

# <a name="set-up-bank-reconciliation-matching-rules"></a>Setja upp samsvörunarreglur afstemmingar banka

[!include[banner](../includes/banner.md)]


Þessi grein útskýrir hvernig Hægt er að setja upp jöfnunarreglur afstemmingar og jöfnunarreglusett bankaafstemmingar til að aðstoða við afstemmingarferli bankans. Samsvörunarreglur afstemmingar eru safn skilyrða sem eru notuð til að sía bankayfirlitslínur og bankaskjalslínur á meðan á afsemmingarferlinu stendur.

Hægt er að setja upp jöfnunarreglur afstemmingar og jöfnunarreglusett bankaafstemmingar til að aðstoða við afstemmingarferli bankans. Samsvörunarregla afstemmingar er safn skilyrða sem notað er til að sía bankayfirlitslínur og bankaskjalslínur á meðan á afstemmingarferli stendur í Microsoft Dynamics 365 for Finance and Operations, Enterprise edition. Nota skal síðuna **Jöfnunarreglur afstemmingarr** síðu til að setja upp reglur fyrir samsvörunarreglu afstemmingar. Hægt er að setja upp fleiri en eina jöfnunarreglu og stofna síðan jöfnunarreglusett á afstemmingar á síðunni **Jöfnunarreglusett afstemmingar**. 

> [!NOTE] 
> Jöfnunarreglur afstemmingar banka eru notaðar þegar verið er að stemma af rafrænt bankayfirlit með því að nota ítarlega bankaafstemmingu. 

Á síðunni **Jöfnunarreglur afstemmingar** er hægt að velja hvaða aðgerðir og valskilyrði eru notuð við keyrslu jöfnunarreglu. Í reitaflokknum **Aðgerðir** skal velja aðgerðina sem verður framkvæmd þegar jöfnunarreglan er keyrð meðan á afstemmingu stendur.  

> [!NOTE] 
> Kosturinn sem er valinn ákvarðar reitina sem birtast.

|                                    |                                                                                                                                                                                                                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Aðgerð**                         |                                                                                                                                                                                                                                                                                                               | **Valskilyrði tiltæk þegar aðgerð er valin.**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Jafna með bankaskjali**       | Stofna skilyrði til að tilgreina hvernig bankaskjöl og bankayfirlitslínur eru jafnaðar þegar jöfnunarregla er keyrð af síðunni **Vinnublað bankaafstemmingar**. Færslulínur eru valdar samkvæmt uppsetningu aukaskilyrða á flýtiflipunum.                                | **Skref 1: Skilgreina jöfnunarregluna** – Velja skilyrði til að tilgreina hvaða bankayfirlit ætti að jafna við bankafærslur Finance and Operations. **Skref 2 (valfrjálst): Velja uppgjörslínu til að keyra jöfnunarreglur gagnvart:** Beita síu á hvaða uppgjörslínu skal keyra reglur gagnvart.                                                                                                                                                                                                                                                                                                               |
| **Hreinsa bakfærslulínur** | Stofna skilyrði til að tilgreina hvernig bakfærslulínur eru fjarlægðar af síðunni **Vinnublað bankaafstemmingar** þegar jöfnunarkeyrsla er keyrð. Þessi valkostur er notaður þegar bankamistök valda því að tvær bankayfirlitslínur eru skráðar í innfluttu bankayfirliti og línurnar verður að stemma af. | **Skref 1**:**Finna bakfærðar uppgjörslínur**– Bæta við valskilyrðum til að velja bakfærslulínur banka. Til dæmis til að velja aðeins ávísanir skal velja **Bankafærslukóði** í reitnum Reitur, velja plúsmerkið (+) í reitnum **Reiknimerki** og færa síðan inn **Ávísanir** í reitnum Gildi. **Skref 2: Finna upprunalegar uppgjörslínur**– Hægt er að bæta við valskilyrðum til að jafna línur í bankaskjali við bankafærslulínur. **Skref 3: Finna bankafærslur Finance and Operations **– Hægt er að bæta við valskilyrðum til að jafna Finance and Operations bankafærslur við bankafærslulínur. |
| **Merkja nýjar færslur**          | Stofna skilyrði til að tilgreina hvernig nýjar línur skulu merktar á síðunni **Vinnublað bankaafstemmingar** þegar jöfnunarkeyrsla er keyrð.                                                                                                                                                                 | **Skref 1: Finna uppgjörslínur**– Bæta við valreitum til að tilgreina hvaða bankayfirlitslínur ætti að velja af síðunni **Vinnublað bankaafstemmingar**. **Skref 2: Finna bankafærslur Finance and Operations **– Hægt er að bæta við valskilyrðum til að leita að bankaskjalslínum. Ef ekkert bankaskjal finnst verður uppgjörslína merkt sem ný færsla.                                                                                                                                                                                                                                             |

 






