---
title: Framkvæma uppfærslur á reikningi vegna skila
description: Þessi virkni styður viðskiptaferla fyrirtækja sem velja að hafa skila- og sölupantanir reikningsfærðar á sama tíma og af sama einstaklingnum.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 32a108694c11a2ebd922a71d5c82691584bbb397
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/15/2022
ms.locfileid: "9014750"
---
# <a name="perform-invoice-updates-for-returns"></a>Framkvæma uppfærslur á reikningi vegna skila 

[!include [banner](../includes/banner.md)]


Skilapöntun er gerð af sölupöntun sem merkt er sem skilapöntun. Þess vegna er listasíðan **Allar sölupantanir** notuð til að búa til reikninga fyrir skilapantanir í staðinn fyrir skjámyndina **Skilapantanir**. Þessi virkni styður viðskiptaferla fyrirtækja sem velja að hafa skila- og sölupantanir reikningsfærðar á sama tíma og af sama einstaklingnum.

Vegna þess að reikningur fyrir skilavöru er fyrir neikvæðri upphæð er hann kallaður kreditnóta.

Þegar þú setur upp uppfærslu reiknings fyrir runuvinnslu verður sölupöntunin af gerðinni **Skilapöntun** að hafa stöðu skilalínu sem **Móttekið** sem gefur til kynna að fylgiseðill pöntunarinnar hafi verið uppfærður.

## <a name="post-an-invoice-for-a-return-order"></a>Bóka reikning fyrir skilapöntun

1.  Smelltu á **Viðskiptakröfur** \>  **Pantanir** \> **Allar sölupantanir**.

2.  Veldu sölupöntun þar sem **Skilapöntun** birtist í reitnum **Gerð pöntunar**.

3.  Á aðgerðasvæðinu, á flipanum **Reikningur**, í flokknum **Búa til** skal smella á **Reikningur**.

4.  Á flipanum **Færibreytur** skal velja gátreitinn **Bókun**.

5.  Skoðaðu upplýsingar í skjámyndinni og gerðu þær breytingar sem eru nauðsynlegar.

6.  Smellið á **Í lagi**. Kreditnótan er bókuð.

## <a name="see-also"></a>Sjá einnig

[Uppfærslur á fylgiseðli fyrir skil](packing-slip-updates-returns.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]