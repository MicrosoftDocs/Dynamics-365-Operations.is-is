---
title: Grunnstilla verðgildi reiðufjár fyrir sölustað (POS)
description: Tilgreint verðgildi reiðufjár fyrir seðla og myntir er hægt að skilgreina í bakvinnslunni fyrir notkun gjaldkera, sölutengiliða og stjórnenda í versluninni innan sölustaðarins.
author: jblucher
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreCashDeclarationTable
audience: Application User
ms.reviewer: josaw
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 0ff4eb5bc7c5e2c0192a5349219301b26e479ac6be978eb05063b68f348b4e55
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6743459"
---
# <a name="configure-cash-denominations-for-the-point-of-sale-pos"></a>Grunnstilla verðgildi reiðufjár fyrir sölustað (POS)

[!include [banner](includes/banner.md)]

Tilgreint verðgildi reiðufjár fyrir seðla og myntir er hægt að skilgreina í bakvinnslunni fyrir notkun gjaldkera, sölutengiliða og stjórnenda í versluninni innan sölustaðarins. Tilgreint verðgildi má nota sem aðstoð við talningu reiðufjár fyrir talningu skiptimyntar í lok dags eða fyrir greiðslumáta við sölu.

## <a name="define-denominations"></a>Skilgreina tilgreint verðgildi

Tilgreint verðgildi er sett upp í hverri verslun fyrir sig á síðunni **Uppsetning** \> **Valkostur fyrir talningu** reiðufjár frá eiginleika verslunar.

![Valkostur fyrir talningu reiðufjár.](./media/image1-denomination.png)

Að skilgreina tilgreint verðgildi:

1. Smellt er á **Nýtt**.
1. Tilgreina tegundina (mynt eða seðill).
1. Tilgreina upphæðina (gildi).

![Síða gjaldmiðla fyrir talningu reiðufjár.](./media/image2-denomination.png)

## <a name="configure-the-functionality-profile"></a>Grunnstilla virkniregluna

Þegar borgað er með reiðufé á sölustað, getur notandinn notað tilgreint verðgildi seðils til að færa inn á fljótlegan máta upphæðina sem viðskiptavinurinn reiddi af hendi. Í virknireglunni geturðu grunnstillt þá tvo valmöguleika sem sýna tilgreint verðgildi á sölustað.

- **Hærra eða jafnt upphæð til greiðslu** – Að sjálfgefnu, sölustaður mun aðeins sýna tilgreint verðgildi seðils sem er hærra en upphæð til greiðslu, sem gerir einnar snertingar greiðslumáta mögulegan. Ef upphæðin til greiðslu er t.d. $7.50, myndi sölustaður sýna eftirfarandi tilgreint verðgildi: $10, $20, $50, og $100. Snerting við allar þessar upphæðir mun sjálfvirkt setja upp greiðslumáta sölu fyrir þá upphæð. $1 og $5 seðlarnir eru ekki sýndir þar sem þessar upphæðir eru minni en upphæð til greiðslu.
- **Öll tilgreind verðgildi** – Veljið þennan valkost til að sýna alltaf öll verðgildi seðils á sölustað, óháð upphæð til greiðslu. Þetta þýðir að notandinn getur notað samsetning seðla til að ná upphæð til greiðslu. Ef upphæðin til greiðslu er t.d. $25.00, getur notandinn valið $20 og $5 til að ljúka sölunni.


[!INCLUDE[footer-include](../includes/footer-banner.md)]