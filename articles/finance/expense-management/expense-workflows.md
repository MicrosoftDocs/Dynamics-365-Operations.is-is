---
title: Setja upp verkflæði fyrir kostnaðarstýringu
description: Hægt er að setja upp verkflæði sem er notað til að skoða og samþykkja ferða- og kostnaðarskjöl.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cdd4d69cb86da12e4a265f89c021c238d00cad08
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/21/2020
ms.locfileid: "3153995"
---
# <a name="set-up-workflows-for-expense-management"></a>Setja upp verkflæði fyrir kostnaðarstýringu

[!include [banner](../includes/banner.md)]

Hægt er að setja upp verkflæði sem er notað til að skoða og samþykkja ferða- og kostnaðarskjöl. Meðal annars er hægt að skilgreina verkflæði fyrir kostnaðarskýrslur, ferðabeiðnir og beiðni um fyrirframgreiðslu.

Verkflæði endurspeglar viðskiptaferli. Það skilgreinir flæði skjals í gegnum kerfið og gefur til kynna hver verður að ljúka við verk eða samþykkja skjal. Nokkrir kostir eru við að nota verkflæðiskerfi í fyrirtækinu:

-   **Samræmt ferli** — Hægt er að skilgreina samþykktarferli fyrir einstök skjöl, eins og innkaupabeiðnir og kostnaðarskýrslur. Með því að nota verkflæðiskerfi má betur ganga úr skugga um að skjölin séu unnin og samþykkt með samræmdum og skilvirkum hætti.

-   Sýnileiki ferlis — Hægt er að rekja stöðu, sögu og afkastamælikvarða tiltekins verkflæðistilviks. Þetta auðveldar ákvörðun um hvort breyta þurfi verkflæðinu til að auka skilvirkni.

-   Miðlægur verkefnalisti — Notendur geta skoðað miðlægan verkefnalista og séð verkefni í verkflæðinu og samþykktir sem tilheyra þeim. 

**Gerðir verkflæðis sem hægt er að stofna**

Í eftirfarandi töflu er listi yfir gerðir verkflæðis sem hægt er að stofna í **Kostnaður**.


|              <strong>Gerð</strong>              |                   <strong>Notið þessa gerð til að</strong>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <strong>Kostnaðarskýrsla</strong>         |            Stofna samþykkisverkflæði fyrir kostnaðarskýrslur.             |
|  <strong>Sjálfvirk bókun á kostnaðarskýrslu</strong>   |        Búa sjálfkrafa til bókunarverkflæði fyrir kostnaðarskýrslur        |
|       <strong>Kostnaðarlínuvara</strong>        |     Búa til samþykkisverkflæði fyrir línuatriði fyrir kostnaðarskýrslur.      |
| <strong>Sjálfvirk bókun kostnaðarlínuatriða</strong> | Búa til sjálfvirk bókunarverkflæði fyrir línuatriði fyrir kostnaðarskýrslur. |
|       <strong>Ferðabeiðni</strong>       |          Stofna samþykktarverkflæði fyrir ferðabeiðnir.           |
|      <strong>Beiðni um fyrirframgreiðslu</strong>      |         Stofna samþykktarverkflæði fyrir beiðni um fyrirframgreiðslu.          |
|        <strong>Endurgreiðsla VSK</strong>        | Stofna samþykktarverkflæði fyrir endurgreiðslu virðisaukaskatts.  |

