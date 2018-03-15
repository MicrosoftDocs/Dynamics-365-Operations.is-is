--- 
title: " Búa til, reikna og bóka yfirlit fyrir smásöluverslun"
description: "Þetta ferli fer í gegnum handvirkar skref til að stofna, reikna út og bóka uppgjör fyrir verslun."
author: jashanno
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 33ebb28196baa9ae944dbd124274b05cb587fea4
ms.contentlocale: is-is
ms.lasthandoff: 02/07/2018

---
# <a name="create-calculate-and-post-a-statement-for-a-retail-store"></a> Búa til, reikna og bóka yfirlit fyrir smásöluverslun

[!include[task guide banner](../includes/task-guide-banner.md)]

Þetta ferli fer í gegnum handvirkar skref til að stofna, reikna út og bóka uppgjör fyrir verslun. Einnig eru runuvinnslur sem hægt er að skilgreina fyrir sama verk. Skrefin til að skilgreina og keyra sem runuvinnslur er að finna í öðrum efnisatriði. Til að ljúka þessu ferli, verður að hafa færslur sem voru fylltir út í sölustaður og síðan dregin inn í Dynamics AX. Þessi skráning notar sýnigögn fyrirtæki USRT . Þetta ferli gæti vísað til Microsoft Dynamics AX. Athugaðu að Dynamics AX er nú kallað Microsoft Dynamics 365 for Operations.

1. Fara í Öll vinnusvæði > .. > Fjárhagur smásöluverslunar
2. Smella á Nýtt uppgjör.
3. Í reitnum verslunarnúmer skal smella á fellilistahnappinn til að opna leitina.
4. Í listanum skal smella á tengilinn í valinni línu.
5. Smellið á „Í lagi“.
    * Uppsetning flokka hefur stillingarnar sem stýra hvaða færslur eru teknar með í uppgjörinu og hvernig þau eru flokkuð í uppgjörslínunum. Hægt er að opna Uppsetningu flokka og breyta þessum stillingum, eða hægt er að nota sem sjálfgildi.  
    * svæðið uppgjörsaðferð skilgreinir hvernig uppgjörslínurnar verða flokkaðar.  
    * Veljið afgreiðslukassa eða starfsmaður eigi að reikna uppgjör aðeins fyrir tiltekinn starfsmaður eða afgreiðslukassa.  
6. Í reitnum lokunaraðferð skal velja valkost.
7. Smellt er á Reikna út uppgjör.
8. Smella á Já.
    * Eftir að reikna uppgjör, ætti að vera eru stofnaðar línur með heildarupphæðir fyrir hvern greiðslumáta og uppgjörsaðferð sem var notaður.  
    * Færa inn talda upphæð í hverja línu ef það þarf að færa inn eða uppfæra. Talið svæði er fyllt út með upphæðir frá í talning skiptimyntar gert í sölustaður.  
9. Smellt er á Bóka uppgjör.
10. Smellið á „Loka“.
11. Fara í Smásala og viðskipti > Rásir > Efnahagur smásöluverslunar.
12. Smellið á flipann Bókað uppgjör.


