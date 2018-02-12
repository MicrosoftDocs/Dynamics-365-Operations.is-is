---
title: "Setja upp verkflæði fyrir kostnað"
description: "Hægt er að setja upp verkflæði sem er notað til að skoða og samþykkja ferða- og kostnaðarskjöl."
author: saraschi2
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 19d725f15f00afce1a2ae4b336226f1dafa94b41
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-workflows-for-expense"></a>Setja upp verkflæði fyrir kostnað

[!include[banner](../includes/banner.md)] Hægt er að setja upp verkflæði sem er notað til að skoða og samþykkja ferða- og kostnaðarskjöl. Meðal annars er hægt að skilgreina verkflæði fyrir kostnaðarskýrslur, ferðabeiðnir og beiðni um fyrirframgreiðslu.

Verkflæði endurspeglar viðskiptaferli. Það skilgreinir flæði skjals í gegnum kerfið og gefur til kynna hver verður að ljúka við verk eða samþykkja skjal. Nokkrir kostir eru við að nota verkflæðiskerfi í fyrirtækinu:

-   **Samræmt ferli** — Hægt er að skilgreina samþykktarferli fyrir einstök skjöl, eins og innkaupabeiðnir og kostnaðarskýrslur. Með því að nota verkflæðiskerfi má betur ganga úr skugga um að skjölin séu unnin og samþykkt með samræmdum og skilvirkum hætti.

-   Sýnileiki ferlis — Hægt er að rekja stöðu, sögu og afkastamælikvarða tiltekins verkflæðistilviks. Þetta auðveldar ákvörðun um hvort breyta þurfi verkflæðinu til að auka skilvirkni.

-   Miðlægur verkefnalisti — Notendur geta skoðað miðlægan verkefnalista og séð verkefni í verkflæðinu og samþykktir sem tilheyra þeim. 

**Gerðir verkflæðis sem hægt er að stofna**

Í eftirfarandi töflu er listi yfir gerðir verkflæðis sem hægt er að stofna í **Kostnaður**.

| **Gerð**                           | **Notið þessa gerð til að**                                                 |     
|------------------------------------|----------------------------------------------------------------------|
| **Kostnaðarskýrsla**                 | Stofna samþykkisverkflæði fyrir kostnaðarskýrslur.                       |      
| **Sjálfvirk bókun á kostnaðarskýrslu**    | Búa sjálfkrafa til bókunarverkflæði fyrir kostnaðarskýrslur              |     
| **Kostnaðarlínuvara**              | Búa til samþykkisverkflæði fyrir línuatriði fyrir kostnaðarskýrslur.         |     
| **Sjálfvirk bókun kostnaðarlínuatriða** | Búa til sjálfvirk bókunarverkflæði fyrir línuatriði fyrir kostnaðarskýrslur.|
| **Ferðabeiðni**             | Stofna samþykktarverkflæði fyrir ferðabeiðnir.                   |    
| **Beiðni um fyrirframgreiðslu**           | Stofna samþykktarverkflæði fyrir beiðni um fyrirframgreiðslu.                 |     
| **Endurgreiðsla VSK**               | Stofna samþykktarverkflæði fyrir endurgreiðslu virðisaukaskatts. |       

