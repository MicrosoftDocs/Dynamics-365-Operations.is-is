---
title: Stofna, reikna og bóka yfirlit fyrir smásöluverslun
description: Þetta efni lýsir handvirkum skrefum fyrir stofnun, útreikning og bókun á uppgjöri fyrir verslun.
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
ms.openlocfilehash: 58900ca4d3f6893689822a8cc5657d8c91772f65
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798538"
---
# <a name="create-calculate-and-post-statements-for-a-retail-store"></a>Stofna, reikna og bóka yfirlit fyrir smásöluverslun

[!include [banner](../includes/banner.md)]

Þetta efni lýsir handvirkum skrefum fyrir stofnun, útreikning og bókun á uppgjöri fyrir verslun. Einnig eru runuvinnslur sem hægt er að skilgreina fyrir sama verk. Skrefin til að skilgreina og keyra sem runuvinnslur er að finna í öðrum efnisatriði. Til að ljúka þessu ferli, verður að hafa færslur sem voru fylltir út á sölustað og draga þær síðan inn í Dynamics 365 Commerce. Þessi skráning notar sýnigögn fyrirtæki USRT .

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