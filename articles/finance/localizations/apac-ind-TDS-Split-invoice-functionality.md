---
title: Aðgerð skiptingar á reikningi
description: Í þessu efnisatriði er útskýrð uppsetning og virkni fyrir skiptingu reikninga eftir afhendingaraðsetri og skattlykilnúmeri (TAN).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 8906461f151f80c22d41fa91a46d761d2a5cf2fff50560cc0d388d279c5bdc7d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742178"
---
# <a name="split-invoice-functionality"></a>Aðgerð skiptingar á reikningi

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er útskýrð uppsetning og virkni fyrir skiptingu reikninga eftir afhendingaraðsetri og skattlykilnúmeri (TAN).

Á síðunni **Færibreytur viðskiptaskulda**, í flipanum **Almennt**, skal velja gátreitinn **Innhreyfingarskjal afurðar** eða **Reikningur** til að bóka og skipta innhreyfingarskjali afurðar eða reikningi sem er með annað afhendingaraðsetur og TAN á síðunni **Innkaupapöntun**. Bókuðum reikningi verður þá skipt eftir afhendingaraðsetri og TAN.

Í flipanum **Samantektaruppfærsla**, í flýtiflipanum **Skipting byggð á**, í línunni **Afhendingarupplýsingar**, skal stilla valkostinn **Staðfesting**, **Tiltektarlisti**, **Fylgiseðill** eða **Reikningur** á **Já** til að bóka og skipta staðfestingu, tiltektarlista, fylgiseðli eða reikningi þar sem önnur afhendingaraðsetur og TAN eru skilgreind fyrir mismunandi reikningslínur á síðunni **Sölupöntun**. Reikningnum verður fyrst skipt eftir afhendingaraðsetri og síðan eftir TAN.

> [!IMPORTANT]
> - Ef engir valkostir fyrir **Afhendingarupplýsingar** eru stilltir á **Já** verður reikningurinn bókaður sem einn reikningur. Engin skipting á reikningi mun eiga sér stað.
> - Til að skipta og bóka fylgiseðil þar sem reikningslínurnar eru með mismunandi afhendingaraðsetur og TAN þarf að stilla valkostinn **Fylgiseðill** fyrir **Afhendingarupplýsingar** á **Já**.
> - Til að skipta og bóka reikning þar sem reikningslínurnar eru með mismunandi afhendingaraðsetur og TAN þarf að stilla valkostinn **Reikningur** fyrir **Afhendingarupplýsingar** á **Já**.
> - Til að bóka reikning þar sem reikningslínurnar eru með mismunandi afhendingaraðsetur en sama TAN skal stilla valkostinn **Reikningur** fyrir **Afhendingarupplýsingar** á **Nei**. Reikningnum verður skipt eftir afhendingaraðsetri.

## <a name="example"></a>Dæmi

Í þessu dæmi er valkosturinn **Reikningur** fyrir **Afhendingarupplýsingar** stilltur á **Já** í flipanum **Samantektaruppfærsla** á síðunni **Færibreytur viðskiptaskulda**. Innkaupareikningur er bókaður sem er með eftirfarandi uppsetningu fyrir afhendingaraðsetur og TAN í línunum:

- **Vörulína 1:** Afhendingaraðsetur 1, TAN-ABCD12345A
- **Vörulína 2:** Afhendingaraðsetur 1, TAN-ABCD12345A
- **Vörulína 3:** Afhendingaraðsetur 2, TAN-ABCD12345A
- **Vörulína 4:** Afhendingaraðsetur 3, TAN-ABCD12345A

Í þessu tilfelli er upphaflegum reikningi skipt í tvo reikninga og hann bókaður á eftirfarandi hátt:

- Reikningur 1 er bókaður fyrir vörulínu 1 og vörulínu 2 vegna þess að báðar línurnar eru með sama afhendingaraðsetur og TAN.
- Reikningur 2 er bókaður fyrir vörulínu 3.
- Reikningur 3 er bókaður fyrir vörulínu 4.
