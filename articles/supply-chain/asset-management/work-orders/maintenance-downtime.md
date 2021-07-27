---
title: Niðurtími vegna viðhalds fyrir verkbeiðnir
description: Þetta efnisatriði lýsir því hvernig á að stofna niðurtímaskráningar vegna viðhalds á eigninni sem er valin í verkbeiðni.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 09c20020e5e0b957785a88ad511cedfec50a5f29
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/06/2021
ms.locfileid: "6344617"
---
# <a name="maintenance-downtime-for-work-orders"></a>Niðurtími vegna viðhalds fyrir verkbeiðnir

[!include [banner](../../includes/banner.md)]


Þú getur búið til skráningar á niðurtíma vegna viðhalds á eigninni sem er valin í verkbeiðni. Þessi afkastageta er gagnleg ef þú vilt skrá niðurstöðutíma viðhalds á einni eða fleiri vélum á framleiðslusvæðinu. Fyrst býrðu til ástæðukóða niðurtíma vegna viðhalds sem þú vilt nota, eins og **Sundurliðun** og **Fyrirhugað stopp**. Þetta skref er gert á síðunni **Ástæðukóðar niðurtíma vegna viðhalds**. Síðan geturðu búið til skráningar á niðurtíma vegna viðhalds á síðunni **Niðurtími vegna viðhalds** og bætt við viðeigandi ástæðukóðum niðurtíma vegna viðhalds.

## <a name="create-maintenance-downtime-reason-codes"></a>Stofna ástæðukóða niðurtíma vegna viðhalds

1. Veldu **Eignastjórnun** > **Uppsetning** > **Verkbeiðnir** > **Ástæðukóðar niðurtíma vegna viðhaldsr**.

2. Veljið **Nýtt**.

3. Í reitnum **Ástæðukóði niðurtíma vegna viðhalds** slærðu inn kenni fyrir ástæðukóða niðurtíma vegna viðhalds.

4. Færið inn lýsandi nafn í reitinn **Heiti**.

5. Veldu gátreitinn **Hafa með í afkastavísi** ef ástæðukóðinn ætti að vera með í útreikningum á afkastavísi (KPI) fyrir eignina. Almennt ætti ekki að taka fyrirhugaða framleiðslustöðvun með í útreikninga á afkastavísi þar sem þeir hafa ekki áhrif á vænt afköst.

6. Veljið **Vista**.

Myndin hér að neðan sýnir dæmi um síðuna **Ástæðukóðar niðurtíma vegna viðhalds**.

![Mynd 1.](media/15-work-orders.png)

Þegar þú hefur búið til þá ástæðukóða niðurtíma vegna viðhalds sem þú vilt nota, getur þú búið til skráningar á niðurtími vegna viðhalds fyrir verkbeiðnir og eignir.


## <a name="create-maintenance-downtime-registrations"></a>Stofna skráningar niðurtíma vegna viðhalds

1. Smelltu á **Eignastýringu** > **Sameiginlegt** > **Verkbeiðnir** > **Allar verkbeiðnir** eða **Virkar verkbeiðnir**.

2. Veldu verkbeiðni og síðan á flipanum **Verkbeiðni**, í hópnum **Eign**, velurðu **Niðurtími vegna viðhalds**.

3. Veljið **Nýtt**.

4. Í reitunum **Frá** og **Til** skilgreinirðu dagsetningu og tímabil fyrir skráningu á niðurtíma vegna viðhalds.

>[!NOTE]
>Þegar þú ferð úr reitnum **Til** er lengd í klukkustundum sjálfkrafa sett inn í reitnum **Tímalengd**.

5. Í reitnum **Ástæðukóði niðurtíma vegna viðhalds** velurðu ástæðukóða.

6. Endurtakið skref 3 til og með 5 til að bæta við fleiri skráningum.

7. Veljið **Vista**.

Eftirfarandi skýringarmynd hér að neðan sýnir dæmi um skráningu á niðurtíma vegna viðhalds.

![Mynd 2.](media/16-work-orders.png)

Dagatalið sem notað er til að reikna út skráningu niðurtíma vegna viðhalds fer eftir vali þínu við uppsetningu eigna og færibreytur. Ef tilföng eru valin á eign í reitnum **Tilföng** á flýtiflipanum **Föst eign** á síðunni **Allar eignir** er datalið sem sett var upp fyrir tengdan tilfangahóp notað, eins og sýnt er á myndinni hér á eftir.

![Mynd 3.](media/17-work-orders.png)

Ef engin tilföng eru valin á eigninni er staðlað dagatal sem valið er á síðunni **Færibreytum eignastýringar** notað, eins og sýnt er á eftirfarandi skýringarmynd.

![Mynd 4.](media/18-work-orders.png)

Til að sjá yfirlit yfir allar skráningar á niðurtíma vegna viðhalds smellirðu á **Eignastjórnun fyrirtækja** > **Fyrirspurnir** > **Niðurtími vegna viðhalds**.

>[!NOTE]
>Öll dagatöl sem eru notuð í einingunni **Eignastjórnun** eru sett upp í **Fyrirtækisstjórnun** > **Uppsetning** > **Dagatöl** > **Dagatöl**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]