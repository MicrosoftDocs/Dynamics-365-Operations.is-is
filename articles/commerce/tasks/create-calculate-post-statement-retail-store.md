---
title: Stofna, reikna og bóka uppgjör fyrir smásöluverslun
description: Þessi grein lýsir handvirkum skrefum til að búa til, reikna út og bóka yfirlit fyrir verslun.
author: jashanno
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailStatementTable
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 740857e6a902e21588855eef5e36cac68e560898
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873279"
---
# <a name="create-calculate-and-post-statements-for-a-retail-store"></a>Stofna, reikna og bóka uppgjör fyrir smásöluverslun

[!include [banner](../includes/banner.md)]

Þessi grein lýsir handvirkum skrefum til að búa til, reikna út og bóka yfirlit fyrir verslun. Einnig eru runuvinnslur sem hægt er að skilgreina fyrir sama verk. Skrefin til að stilla og keyra runuvinnuna má finna í öðrum greinum. Til að ljúka þessu ferli, verður að hafa færslur sem voru fylltir út á sölustað og draga þær síðan inn í Dynamics 365 Commerce. Þessi skráning notar sýnigögn fyrirtæki USRT .

1. Veldu **Fjárhagur verslunar** af heimasíðunni.
2. Veldu **Nýtt yfirlit**.
3. Í reitnum **Verslunarnúmer** reitinn velurðu valkost úr fellivalmyndinni.
4. Veljið **Í lagi**.
5. Hópurinn **Uppsetning** hefur stillingarnar sem stýra hvaða færslur eru teknar með í uppgjörinu og hvernig þau eru flokkuð í uppgjörslínunum. Hægt er að opna hópinn **Uppsetningu** og breyta þessum stillingum, eða hægt er að nota sem sjálfgildi.  
    - Reiturinn **uppgjörsaðferð** skilgreinir hvernig uppgjörslínurnar verða flokkaðar.  
    - Veljið starfsmann eða afgreiðslukassa í reitnum **Starfsmaður/afgreiðslukassi** ef þú vilt reikna uppgjör aðeins fyrir tiltekinn starfsmann eða afgreiðslukassa.  
6. Í reitnum **Lokunaraðferð** skal velja valkost.
7. Veldu **Reikna uppgjör** úr aðgerðarglugganum.
8. Velja skal **Já**.
    - Eftir að reikna uppgjör, ætti að vera eru stofnaðar línur með heildarupphæðir fyrir hvern greiðslumáta og uppgjörsaðferð sem var notaður.  
    - Færa inn talda upphæð í hverja línu ef það þarf að færa inn eða uppfæra. Talið svæði er fyllt út með upphæðir frá í talning skiptimyntar gert í sölustaður.  
9. Veldu **Bóka uppgjör** úr aðgerðarglugganum.
10. Veljið **Loka**.
11. Lokið glugganum.
12. Á heimasíðunni velurðu **Fjárhagur verslunar**.
13. Veldu flipann **Bókuð uppgjör**.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]