---
title: Vinna úr viðburðum
description: Í líftíma starfsmannsins í Microsoft Dynamics 365 Human Resources, getur hver starfsmaður lent í ýmsum breytingum á atburði í lífinu.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes, BenefitEligibilityProcessResultViewer
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 42b7e2606bca4bb5eda1c9bfc7940f9067c4b943
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112929"
---
# <a name="process-life-events"></a>Vinna úr viðburðum

Í líftíma starfsmannsins í Microsoft Dynamics 365 Human Resources, getur hver starfsmaður lent í ýmsum breytingum á atburði í lífinu. Til dæmis hjónaband, breyting á atvinnu eða breyting á skjólstæðingi/rétthafi. Til að nota atburði í lífinu verður þú að virkja lífatburði á formi hagur breytur, setja upp gerðir atburða fyrir líf og setja upp val á atburði fyrir áætlunartegundir.

Áður en þú getur afgreitt atburði í lífinu verður þú að hafa þegar rekið opna skráningu amk einu sinni á ráðningartíma. Í Bandaríkjunum er opin innritun venjulega einu sinni á ári. Utan Bandaríkjanna kann að vera opin innritun við ráðningu. Starfsmaður þarf ekki að velja bótaáætlun til að lífatburðir verði afgreiddir, en þeir þurfa að hafa verið með í opinni skráningarvinnslu. 

Notaðu vinnslu lífsviðburða þegar þú ert með starfsmenn sem eru með atburði í lífinu sem eiga sér stað á framtíðardegi. Þessi atburður vinnur alla atburði í lífinu sem ekki hafa verið afgreiddir (eins og atburðir í framtíðinni, eða lífatburðir sem hafa verið bættir við sem eru ekki sérstakir fyrir einn starfsmann - eitt dæmi er nýr ávinningur). Atburðir í rauntíma eru faldir.

Til dæmis, ef í dag er 1. febrúar, og þann 14. febrúar, áætlar starfsmaður Joe Smith að breyta lögaðilum, ef þú rekur vinnslu atburða fyrir 15. febrúar, vinnur kerfið alla atburði til 15. febrúar. 

1. Í vinnusvæðinu **Fríðindastjórnun**, undir **Í vinnslu**, veldu **Vinnsla viðburða**.

2. Í valmyndinni **Keyra viðburðaferli**, tilgreindu gildi fyrir eftirfarandi reiti:

   | Svæði | Lýsing |
   | --- | --- |
   | **Skráningartímabil** | Innritunartímabilið til að vinna úr viðburðum fyrir. |
   | **Lögaðili** | Lögaðilinn til að vinna úr viðburðum fyrir. |
   | **Dagsetning viðburðar** | Kerfið vinnur alla atburði á innritunartímabilinu sem eiga sér stað fram til þessa dags. |
   | **Starfskraftur** | Starfskrafturinn til að vinna úr viðburðum fyrir. Ef þú skilur þennan reit eftir auðan verða viðburðir allra starfsmanna afgreiddir. |

3. Ef þú vilt keyra ferlið í bakgrunni skaltu velja **Keyra í bakgrunni** og framkvæma eftirfarandi verk:

   1. Færið inn upplýsingar fyrir ferlið.

   2. Veldu til að setja upp endurtekið starf **Endurtekning**, sláðu inn upplýsingar um endurtekningu og veldu **Í lagi**.

   3. Veldu til að setja upp atvinnuviðvörun **Viðvaranir**, veldu viðvaranir sem berast og veldu síðan **Í lagi**.

   4. Veljið **Í lagi**. Ferlið keyrir með breytunum sem þú stillir.

4. Veljið **Í lagi**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]