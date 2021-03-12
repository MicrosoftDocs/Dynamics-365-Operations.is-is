---
title: Villuleita sölupantanir
description: Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með sölupantanir.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: c9a5b7a5e8cac7f8816233dd2d7ff1a7f84ea480
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974786"
---
# <a name="troubleshoot-sales-orders"></a>Villuleita sölupantanir

Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með sölupantanir.

## <a name="the-tax-information-isnt-updated-if-i-change-the-location-on-a-sales-order-header"></a>Skattaupplýsingarnar eru ekki uppfærðar ef ég breyti staðsetningunni í sölupöntunarhaus.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Ef svæði, vöruhúsi eða afhendingaraðsetri er breytt annaðhvort í sölupöntunarhaus eða á línustigi, uppfærast skattaupplýsingarnar ekki sjálfkrafa fyrir línurnar.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Þessi hegðun er samkvæmt hönnuninni. Vandamálið stafar af því að afhendingaraðsetri, svæði og vöruhúsi er ekki breytt sjálfkrafa á línustigi heldur. Uppfæra verður handvirkt.

## <a name="if-there-are-two-trade-agreements-for-the-same-period-or-overlapping-periods-the-same-agreement-line-is-always-selected"></a>Ef það eru tveir viðskiptasamningar fyrir sama tímabil eða tímabil sem skarast er sama samningslínan alltaf valin.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Ef tveir viðskiptasamningar eru skilgreindir fyrir sama tímabil eða tímabil sem skarast, virðist sami viðskiptasamningur vera valinn í hvert skipti sem stofnaðar eru sölupöntunarlínur sem innihalda þessar vörur.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Ef það eru fleiri en einn viðskiptasamningur fyrir tiltekna dagsetningu er viðskiptasamningurinn sem er með lægsta verðið alltaf valinn. Til að fá frekari upplýsingar skal sækja eftirfarandi hvítbók: [Viðskiptasamningar í Microsoft Dynamics AX 2012](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90).

## <a name="can-i-link-a-purchase-order-to-a-sales-order-to-fulfill-demand"></a>Get ég tengt innkaupapöntun við sölupöntunina til að uppfylla eftirspurn?

Hægt er að stofna innkaupapöntun úr sölupöntun. Frekari upplýsingar er að finna í [Stofna innkaupapöntun úr sölupöntun](tasks/create-purchase-order-sales-order.md).

## <a name="i-cant-cancel-or-delete-a-return-order-or-a-sales-order"></a>Ég get ekki hætt við eða eytt skilapöntun eða sölupöntun.

Aðeins er hægt að hætta við sölupantanir og skilapantanir sem eru með stöðuna *Stofnuð*. Frekari upplýsingar er að finna í [Hætta við skilapöntun](../service-management/cancel-return-order.md).

## <a name="when-i-try-to-cancel-a-sales-order-i-receive-a-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations-error"></a>Þegar ég reyni að hætta við sölupöntun fæ ég upp villuna „Ekki er hægt að fjarlægja frátekningar vegna þess að búið er að stofna vinnu sem byggir á frátekningunum.“

Villukóði WAX4661

Ef vinna tengist sölupöntun er ekki hægt að hætta við sölupöntunina fyrr en hætt er við vinnu og hún bakfærð. Þessi krafa gildir jafnvel þótt vinnan sem tengist sölupöntuninni sé lokuð.

Til að laga þetta vandamál skal fylgja þessum skrefum.

1. Hættið við verkið og setjið birgðir aftur á æskilega staðsetningu. Farið á viðeigandi farm sölupöntunarinnar og veljið annaðhvort **Minnka tiltektarmagn** í farmlínunni eða **Bakfæra vinnu** á aðgerðasvæðinu.

    Verkið er nú með stöðuna *Hætt við* og ný birgðahreyfingarvinna er sjálfkrafa stofnuð og unnið úr til að setja birgðir aftur í staðsetninguna sem var lýst þegar bakfærslan var gerð.

2. Eyðið farminum. Sendingunni er einnig eytt.
3. Nú ætti að vera hægt að fara í sölupöntunina og hætta við hana.

## <a name="i-cant-cancel-an-intercompany-purchase-order-that-is-linked-to-a-sales-order"></a>Ekki er hægt að hætta við samstæðuinnkaupapöntun sem er tengd við sölupöntun.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Ef reynt er að hætta við samstæðuinnkaupapöntun sem tengist sölupöntun, gætu eftirfarandi villuboð borist: „Ekki er hægt að minnka magn, þar sem eftirstöðvar uppfærðs magns breyta um formerki.“

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Þetta vandamál var lagfært í Microsoft Dynamics 365 Supply Chain Management útgáfu 10.0.13. Í þeirri útgáfu og nýrri útgáfum er nú hægt að hætta við samstæðuinnkaupapöntun sem tengist sölupöntun.

## <a name="can-i-restore-an-invoiced-sales-order-that-was-deleted"></a>Get ég endurheimt reikningsfærða sölupöntun sem var eytt?

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Reikningsfærðri sölupöntun var eytt fyrir mistök og þú vilt endurheimta hana eða skoða upplýsingarnar um hana.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Ef eydd sölupöntun hefur þegar verið reikningsfærð skal fara í **Viðskiptavinalykill \> Færslur \> Upprunalegt skjal \> Skoða upplýsingar**. Finnið reikninginn sem leitað er að og veljið hann til að skoða upplýsingarnar. Þessar upplýsingar innihalda tilvísun sölupöntunarinnar. Einnig ætti að vera hægt að fá aðgang að upplýsingum um sölupöntunina á þessari síðu.

## <a name="the-deadline-of-a-sales-order-header-cant-be-found-in-the-salesorderheaderv2entity-data-entity"></a>Ekki er hægt að finna tímamörk sölupöntunarhauss í gagnaeiningunni SalesOrderHeaderV2Entity.

Reiturinn fyrir tímamörk er ekki til í gagnaeiningunni *SalesOrderHeaderV2Entity*.

## <a name="i-must-delete-orphaned-sales-order-records"></a>Ég verð að eyða sölupöntunarfærslum án tilvísana.

Til að hreinsa upp sölupöntunarfærslur án tilvísana skal keyra reglubundnu vinnsluna *Eyðing sölupöntunar* með því að fara á annan hvorn staðinn:

- Sala og markaðssetning \> Reglubundnar vinnslur \> Hreinsun \> Eyða sölupöntunum
- Smásala og viðskipti \> Upplýsingatækni smásölu og viðskipta \> Hreinsun \> Eyða sölupöntunum

## <a name="is-there-a-way-to-calculate-commissions-on-invoices-that-have-already-been-posted"></a>Er leið til að reikna út þóknanir á reikningum sem hafa þegar verið bókaðir?

Supply Chain Management styður ekki útreikning á þóknunum fyrir bókaða reikninga sem stendur.

## <a name="a-bundle-item-isnt-supported-in-an-intercompany-process"></a>Búntvara er ekki studd í samstæðuferli.

Búntvaran er ekki tiltæk fyrir innkaupapöntunina því að ef þú skoðar sölupöntunarlínurnar fyrir búntvöruna muntu taka eftir því að magnið er *0* (núll) og staðan er *Afturkölluð*. Þessi hegðun er samkvæmt hönnuninni. Sölupöntunin kaupir aðeins þætti búntvörunnar. Hún kaupir ekki búntvöruna sjálfa.

Ef kaupa þarf búnt, þarf að hafa í huga hvort merkja eigi það sem búntvöru, þar sem þessi virkni er hönnuð fyrir aðstæður tekjuskráningar. Frekari upplýsingar um búntvörur er að finna í [Búnt](../../finance/accounts-receivable/revenue-recognition-setup.md#bundles).
