---
title: Bæta villu við verkbeiðni
description: Þessi grein lýsir því hvernig á að bæta villuskráningum við verkbeiðnir í eignastýringu.
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
ms.openlocfilehash: 210db3259a6c64a508119b30598a34dbda2d2dd2
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/15/2022
ms.locfileid: "9014999"
---
# <a name="add-fault-to-work-order"></a>Bæta villu við verkbeiðni

[!include [banner](../../includes/banner.md)]



Þú getur bætt bilunum sem voru settar upp í bilunarhönnuðinni við verkbeiðni. Ein eða fleiri bilanaskrár verða að vera tengdar eignagerðunum sem eru notaðar fyrir eignina sem er valin í verkbeiðninni. Nánari upplýsingar um uppsetninguna er að finna í [Villustjórnun](../setup-for-work-orders/fault-management.md).

1. Veljið **Eignastýring** > **Verkbeiðnir** > **Allar verkbeiðnir** eða **Virkar verkbeiðnir**.

2. Veldu verkbeiðnina til að skrá bilun á og síðan í aðgerðarglugganum á flipanum **Verkbeiðni**, í hópnum **Eignir**, velurðu **Bilun eignar**.

3. Á flýtiflipanum **Einkenni** velurðu **Bæta við línu**. Raðnúmer fyrir bilun er sjálfkrafa skráð í reitinn **Bilun**.

4. Í reitnum **Bilunareinkenni** velurður viðeigandi einkenni.

5. Í reitunum **Bilunarsvæði** og **Bilunartegund** velurðu viðeigandi gildi.

6. Í reitnum **Dagsetning bilunar** er núverandi dagsetning sjálfkrafa sett inn. Þú getur valið aðra dagsetningu eftir þörfum.

7. Á flýtiflipanum **Orsakir fyrir valið einkenni** bætirðu við línu til að lýsa orsökum vandans.

8. Á flýtiflipanum **Úrræði fyrir valið einkenni** bætirðu við línu til að lýsa hugsanlegri lausn við vandanum.

9. Veljið **Vista**.

Eftirfarandi skýringarmynd hér að neðan sýnir dæmi um bilanaskráningu.

![Mynd 1.](media/19-work-orders.png)


## <a name="view-asset-faults"></a>Skoða eignabilanir

Í listanum **Eignabilanir** er hægt að fá yfirlit yfir allar bilanir sem eru skráðar á eignum.

Á listasíðunni **Eignabilanir** er hægt að fá yfirlit yfir allar bilanir sem hafa verið skráðar á eignum. Til að opna síðuna velurðu **Eignastýringu** > **Fyrirspurnir** > **Bilun eignar** > **Bilanir eigna**.


## <a name="print-asset-fault-report"></a>Prenta eignabilanaskýrslur

Af listasíðunni **Allar eignir** er hægt að prenta eignabilanaskýrslu sem sýnir allar bilanaskráningar og myndrænt yfirlit yfir tölfræðilegar bilanir.

1. Veldu **Eignastýring** > **Eignir** > **Allar eignir**.

2. Veldu eignina sem á að prenta bilanaskýrslu fyrir.

3. Í Aðgerðasvæði, á flipanum **Almennt** í flokknum **Skýrslur** velurðu **Bilun eignar**.

4. Skráðu ákveðið tímabil eða veldu bilanagerð.

5. Veldu **Í lagi** til að prenta skýrsluna.

>[!NOTE]
>Til að prenta bilanaskýrslu fyrir nokkrar eignir eða eignagerðir velurðu **Eignastýringu** > **Skýrslur** > **Eignir** > **Bilun eigna**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]