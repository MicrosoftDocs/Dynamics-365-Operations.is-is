---
title: Algengar spurningar um sölupantanir
description: Á þessari síðu er fjallað um algengar spurningar sem vakna þegar verið er að vinna með sölupantanir í Dynamics 365 Supply Chain Management.
author: Henrikan
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 3cee75b1d740e7cb414c674157dde0146e8faa50
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571618"
---
# <a name="sales-order-faqs"></a>Algengar spurningar um sölupantanir

Á þessari síðu er fjallað um algengar spurningar sem vakna þegar verið er að vinna með sölupantanir í Dynamics 365 Supply Chain Management.

## <a name="can-i-link-a-purchase-order-to-a-sales-order-to-fulfill-demand"></a>Get ég tengt innkaupapöntun við sölupöntunina til að uppfylla eftirspurn?

Hægt er að stofna innkaupapöntun úr sölupöntun. Frekari upplýsingar er að finna í [Stofna innkaupapöntun úr sölupöntun](/dynamics365/supply-chain/sales-marketing/tasks/create-purchase-order-sales-order).

## <a name="can-i-cancel-or-delete-a-sales-order-or-return-order"></a>Er hægt að hætta við eða eyða skilapöntun eða sölupöntun?

Aðeins er hægt að hætta við sölupantanir og skilapantanir sem eru með stöðuna *Stofnuð*. Frekari upplýsingar er að finna í [Hætta við skilapöntun](/dynamics365/supply-chain/service-management/cancel-return-order).

## <a name="can-i-restore-an-invoiced-sales-order-that-was-deleted"></a>Get ég endurheimt reikningsfærða sölupöntun sem var eytt?

Ef reikningsfærðri sölupöntun var eytt fyrir mistök og þú vilt endurheimta hana eða skoða upplýsingarnar um hana.

Fara  í **Viðskiptavinalykill \> Færslur \> Upprunalegt skjal \> Skoða upplýsingar**. Finnið reikninginn sem leitað er að og veljið hann til að skoða upplýsingarnar. Þessar upplýsingar innihalda tilvísun sölupöntunarinnar. Einnig ætti að vera hægt að fá aðgang að upplýsingum um sölupöntunina á þessari síðu.

## <a name="how-do-i-delete-orphaned-sales-order-records"></a>Hvernig er sölupöntunarfærslum án tilvísana eytt?

Til að hreinsa upp sölupöntunarfærslur án tilvísana skal keyra reglubundnu vinnsluna *Eyðing sölupöntunar* með því að fara á annan hvorn staðinn:

- Sala og markaðssetning \> Reglubundnar vinnslur \> Hreinsun \> Eyða sölupöntunum
- Smásala og viðskipti \> Upplýsingatækni smásölu og viðskipta \> Hreinsun \> Eyða sölupöntunum

## <a name="is-there-a-way-to-calculate-commissions-on-invoices-that-have-already-been-posted"></a>Er leið til að reikna út þóknanir á reikningum sem hafa þegar verið bókaðir?

Supply Chain Management styður ekki útreikning á þóknunum fyrir bókaða reikninga sem stendur.
