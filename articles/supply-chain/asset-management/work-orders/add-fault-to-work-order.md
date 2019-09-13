---
title: Bættu bilun við verkbeiðnina
description: Þetta efni lýsir því hvernig bæta má bilanaskráningum við verkbeiðnir í eignastýringu.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
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
ms.openlocfilehash: 7c86973ca44d9113d14e180e27cc51343da5d2c0
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875719"
---
# <a name="add-fault-to-work-order"></a>Bættu bilun við verkbeiðnina

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Þú getur bætt bilunum sem eru settar upp í bilunarhönnuðinni við verkbeiðni. Eignin sem valin er í verkbeiðninni verður að innihalda eignagerðir sem hafa eina eða fleiri bilaskrár tengdar henni. Lestu meira um uppsetningu í kaflanum [Bilanastjórnun](../setup-for-work-orders/fault-management.md).

1. Smelltu á **Eignastýringu** > **Sameiginlegt** > **Vinnufyrirmæli** > **Allar vinnupantanir** eða **Virkar vinnupantanir**.

2. Veldu listann á verkbeiðnina sem þú vilt gera villuskráningu á og smelltu á **Bilun í eignum**.

3. Á flýtiflipanum **Einkenni** er smellt á **Bæta við línu**. Raðnúmer fyrir bilun er sjálfkrafa sett inn í reitinn **Bilun**.

4. Veldu viðeigandi einkenni í reitnum **Bilunareinkenni**.

5. Veldu **Bilunarsvæði** og **Bilunartegund**.

6. Í reitnum **Dagsetning bilunar** er núverandi dagsetning sjálfkrafa sett inn. Hægt er að velja aðra dagsetningu ef þörf krefur.

7. Á flýtiflipanum **Orsakir fyrir valið einkenni** bætirðu við línu sem lýsir orsökum vandans.

8. Á flýtiflipanum **Úrræði fyrir valið einkenni** bætirðu við línu sem lýsir hugsanlegri lausn við vandanum.

9. Smellt er á **Vista**.

![Mynd 1](media/19-work-orders.png)


## <a name="view-asset-faults"></a>Skoða eignabilanir

Í listanum **Eignabilanir** er hægt að fá yfirlit yfir allar bilanir sem eru skráðar á eignum.

Smelltu á **Eignastýringu** > **Fyrirspurnir** > **Bilun eignar** > **Bilanir eigna** til að opna listann.


## <a name="print-asset-fault-report"></a>Prenta eignabilanaskýrslur

Af listasíðunni **Allar eignir** er hægt að prenta eignabilanaskýrslu sem sýnir allar bilanaskráningar auk myndræns yfirlits yfir tölfræðilegar bilanir.

1. Smelltu á **Eignastjórnun** > **Sameiginlegt** > **Eignir** > **Allar eignir**.

2. Á listanum **Eignir** velurðu eignina sem þú vilt prenta bilanaskýrslu fyrir.

3. Á flipanum **Almennt** > **Skýrsluhluti** smellirðu á **Bilun eigna**.

4. Settu inn ákveðið tímabil eða veldu bilanagerð.

5. Smelltu á **Í lagi** til að prenta skýrsluna.

>[!NOTE]
>Þú getur líka prentað bilanaskýrslu fyrir nokkrar eignir eða eignagerðir með því að smella á **Eignastýringu** > **Skýrslur** > **Eignir** > **Bilun eigna**.

