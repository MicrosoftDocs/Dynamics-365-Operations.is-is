---
title: Framkvæma uppfærslur á reikningi vegna skila
description: Þessi virkni styður viðskiptaferla fyrirtækja sem velja að hafa skila- og sölupantanir reikningsfærðar á sama tíma og af sama einstaklingnum.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d99f067e93de57b5b13787f128f450f736660351
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006678"
---
# <a name="perform-invoice-updates-for-returns"></a>Framkvæma uppfærslur á reikningi vegna skila 

[!include [banner](../includes/banner.md)]


Skilapöntun er gerð af sölupöntun sem merkt er sem skilapöntun. Þess vegna er listasíðan **Allar sölupantanir** notuð til að búa til reikninga fyrir skilapantanir í staðinn fyrir skjámyndina **Skilapantanir**. Þessi virkni styður viðskiptaferla fyrirtækja sem velja að hafa skila- og sölupantanir reikningsfærðar á sama tíma og af sama einstaklingnum.

Vegna þess að reikningur fyrir skilavöru er fyrir neikvæðri upphæð er hann kallaður kreditnóta.

Þegar þú setur upp uppfærslu reiknings fyrir runuvinnslu verður sölupöntunin af gerðinni **Skilapöntun** að hafa stöðu skilalínu sem **Móttekið** sem gefur til kynna að fylgiseðill pöntunarinnar hafi verið uppfærður.

## <a name="post-an-invoice-for-a-return-order"></a>Bóka reikning fyrir skilapöntun

1.  Smelltu á **Viðskiptakröfur** \> **Algengt** \> **Sölupantanir** \> **Allar sölupantanir**.

2.  Veldu sölupöntun þar sem **Skilapöntun** birtist í reitnum **Gerð pöntunar**.

3.  Á aðgerðasvæðinu, á flipanum **Reikningur**, í flokknum **Búa til** skal smella á **Reikningur**.

4.  Á flipanum **Færibreytur** skal velja gátreitinn **Bókun**.

5.  Skoðaðu upplýsingar í skjámyndinni og gerðu þær breytingar sem eru nauðsynlegar.

6.  Smellið á **Í lagi**. Kreditnótan er bókuð.

## <a name="see-also"></a>Sjá einnig

[Uppfærslur á fylgiseðli fyrir skil](packing-slip-updates-returns.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]