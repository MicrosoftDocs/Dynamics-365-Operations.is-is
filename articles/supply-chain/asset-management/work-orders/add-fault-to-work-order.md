---
title: Bættu bilun við verkbeiðnina
description: Þetta efni lýsir því hvernig bæta má bilanaskráningum við verkbeiðnir í eignastýringu.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e82026f1d73e7368d93109bc0b895b7368ac84d4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430362"
---
# <a name="add-fault-to-work-order"></a>Bæta villu við verkbeiðni

[!include [banner](../../includes/banner.md)]



Þú getur bætt bilunum sem voru settar upp í bilunarhönnuðinni við verkbeiðni. Ein eða fleiri bilanaskrár verða að vera tengdar eignagerðunum sem eru notaðar fyrir eignina sem er valin í verkbeiðninni. Nánari upplýsingar um uppsetninguna er að finna í [Villustjórnun](../setup-for-work-orders/fault-management.md).

1. Veldu **Eignastýringu** > **Sameiginlegt** > **Verkbeiðnir** > **Allar verkbeiðnir** eða **Virkar verkbeiðnir**.

2. Veldu verkbeiðnina til að skrá bilun á og síðan í aðgerðarglugganum á flipanum **Verkbeiðni**, í hópnum **Eignir**, velurðu **Bilun eignar**.

3. Á flýtiflipanum **Einkenni** velurðu **Bæta við línu**. Raðnúmer fyrir bilun er sjálfkrafa skráð í reitinn **Bilun**.

4. Í reitnum **Bilunareinkenni** velurður viðeigandi einkenni.

5. Í reitunum **Bilunarsvæði** og **Bilunartegund** velurðu viðeigandi gildi.

6. Í reitnum **Dagsetning bilunar** er núverandi dagsetning sjálfkrafa sett inn. Þú getur valið aðra dagsetningu eftir þörfum.

7. Á flýtiflipanum **Orsakir fyrir valið einkenni** bætirðu við línu til að lýsa orsökum vandans.

8. Á flýtiflipanum **Úrræði fyrir valið einkenni** bætirðu við línu til að lýsa hugsanlegri lausn við vandanum.

9. Veljið **Vista**.

Eftirfarandi skýringarmynd hér að neðan sýnir dæmi um bilanaskráningu.

![Mynd 1](media/19-work-orders.png)


## <a name="view-asset-faults"></a>Skoða eignabilanir

Í listanum **Eignabilanir** er hægt að fá yfirlit yfir allar bilanir sem eru skráðar á eignum.

Á listasíðunni **Eignabilanir** er hægt að fá yfirlit yfir allar bilanir sem hafa verið skráðar á eignum. Til að opna síðuna velurðu **Eignastýringu** > **Fyrirspurnir** > **Bilun eignar** > **Bilanir eigna**.


## <a name="print-asset-fault-report"></a>Prenta eignabilanaskýrslur

Af listasíðunni **Allar eignir** er hægt að prenta eignabilanaskýrslu sem sýnir allar bilanaskráningar og myndrænt yfirlit yfir tölfræðilegar bilanir.

1. Veldu **Eignastýring** > **Sameiginlegt** > **Eignir** > **Allar eignir**.

2. Veldu eignina sem á að prenta bilanaskýrslu fyrir.

3. Í Aðgerðasvæði, á flipanum **Almennt** í flokknum **Skýrslur** velurðu **Bilun eignar**.

4. Skráðu ákveðið tímabil eða veldu bilanagerð.

5. Veldu **Í lagi** til að prenta skýrsluna.

>[!NOTE]
>Til að prenta bilanaskýrslu fyrir nokkrar eignir eða eignagerðir velurðu **Eignastýringu** > **Skýrslur** > **Eignir** > **Bilun eigna**.

