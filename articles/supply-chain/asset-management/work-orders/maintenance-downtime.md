---
title: Niðurtími vegna viðhalds
description: Þetta efni lýsir niðurtíma vegna viðhalds í eignastýringu.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: cc79dc1b5911679586fa560142ada5add1a881d2
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918245"
---
# <a name="maintenance-downtime"></a>Niðurtími vegna viðhalds


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Þú getur búið til skráningar á niðurtíma vegna viðhalds á eigninni sem er valin í verkbeiðni. Þetta er gagnlegt ef þú vilt skrá niðurstöðutíma viðhalds á einni eða fleiri vélum á framleiðslusvæðinu. Fyrst býrðu til ástæðukóða niðurtíma vegna viðhalds sem þú vilt nota, til dæmis sundurliðun og fyrirhugað stopp. Þetta er gert í **Ástæðukóðar niðurtíma vegna viðhalds**. Næst geturðu búið til skráningar á niðurtíma vegna viðhalds í **Niðurtími vegna viðhalds** og bæta við viðeigandi ástæðukóðum.

## <a name="create-maintenance-downtime-reason-codes"></a>Stofna ástæðukóða niðurtíma vegna viðhalds

1. Smelltu á **Eignastjórnun** > **Uppsetning** > **Verkbeiðnir** > **Ástæðukóðar niðurtíma vegna viðhaldsr**.

2. Smellt er á **Nýtt**.

3. Settu inn auðkenni í reitinn **Ástæðukóði niðurtíma vegna viðhalds**.

4. Í reitnum **Heiti** slærðu inn heiti fyrir ástæðukóðann.

5. Veldu gátreitinn **Hafa með í afkastavísi** ef ástæðukóðinn ætti að vera með í útreikningu á afkastavísi eigna. Almennt ætti ekki að taka fyrirhugaða framleiðslustöðvun með í útreikninga á afkastavísi þar sem þeir hafa ekki áhrif á vænt afköst.

6. Smellt er á **Vista**.

![Mynd 1](media/15-work-orders.png)


Þegar þú hefur búið til þá ástæðukóða niðurtíma vegna viðhalds sem þú vilt nota, getur þú búið til skráningar á niðurtími vegna viðhalds fyrir verkbeiðnir og eignir.


## <a name="create-maintenance-downtime-registrations"></a>Stofna skráningar niðurtíma vegna viðhalds

1. Smelltu á **Eignastýringu** > **Sameiginlegt** > **Verkbeiðnir** > **Allar verkbeiðnir** eða **Virkar verkbeiðnir**.

2. Veldu verkbeiðnina og smelltu á **Niðurtíma vegna viðhalds**.

3. Smellt er á **Nýtt**.

4. Settu dagsetningu og tímabil fyrir skráningu niðurtíma vegna viðhalds inn í reitina **Frá** og **Til**.

5. Þegar þú ferð úr reitnum **Til** er lengd í klukkustundum sjálfkrafa sett inn í reitnum **Tímalengd**.

6. Veldu ástæðukóða í reitnum **Ástæðukóði niðurtíma vegna viðhalds**.

7. Endurtaktu skref 3-6 ef þú vilt bæta við fleiri skráningum.

8. Smellt er á **Vista**.


![Mynd 2](media/16-work-orders.png)


Dagatalið sem notað er til að reikna út skráningu niðurtíma vegna viðhalds fer eftir vali þínu við uppsetningu eigna og færibreytur. Ef tilföng eru valin á eign í flýtiflipanum **Allar eignir** > **Fastafjármunir** > reitnum **Tilföng** er dagatalið sem sett var upp fyrir tengdan tilfangahóp notað, eins og sýnt er á myndinni hér á eftir.

![Mynd 3](media/17-work-orders.png)


Ef engin tilföng eru valin á eigninni er staðlað dagatal sem valið er í **Færibreytum eignastýringar** notað, eins og sýnt er á eftirfarandi mynd.

![Mynd 4](media/18-work-orders.png)


Smelltu á **Eignastjórnun fyrirtækja** > **Fyrirspurnir** > **Niðurtími vegna viðhalds** til að sjá yfirlit yfir allar skráningar á niðurtíma vegna viðhalds.

>[!NOTE]
>Öll dagatöl sem eru notuð í einingunni **Eignastjórnun** eru sett upp í **Fyrirtækisstjórnun** > **Uppsetning** > **Dagatöl** > **Dagatöl**.

