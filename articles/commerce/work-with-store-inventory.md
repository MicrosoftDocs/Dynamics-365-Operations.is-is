---
title: Birgðastjórnun verslunar
description: Þetta efnisatriði lýsir gerðum af skjölum sem hægt er að nota til að stjórna birgðum.
author: BrianShook
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: a4a8f517ebb6fd4ce291b5d28ae22db62a832251
ms.sourcegitcommit: f4823a97c856e9a9b4ae14116a43c87f9482dd90
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/09/2021
ms.locfileid: "7779359"
---
# <a name="commerce-inventory-management"></a>Birgðastjórnun Commerce

[!include [banner](includes/banner.md)]

Þegar unnið er með birgðir í Microsoft Dynamics 365 Commerce og einhver Commerce-forrit sem eru tengd við Commerce Scale Unit eru notuð, er mikilvægt að gera sér grein fyrir að regla pöntunarúrvinnslu í CSU býður upp á takmarkaðan stuðning fyrir sumar birgðavíddir og gerðir birgðavöru. Commerce-forrit styðja ekki alla möguleika vöruafbrigða sem eru í boði í gegnum valkosti vöruafbrigðis í Dynamics 365 Supply Chain Management.

Commerce-forritin sem keyra í CSU styðja ekki eftirfarandi afurðarvíddir og vöruafbrigði:

- Afbrigði afurðavíddar og uppskriftavörur (fyrir utan afurðir smásölusetts, sem nota suma hluti uppskriftaramma)
- Vörur framleiðsluþyngdar
- Stýrð atriði útgáfu afurðavíddar

Commerce-forritin sem keyra í CSU styðja ekki eftirfarandi rakningarvíddir:
- Eigandavídd

- Forrit sölustaðar getur boðið upp á takmarkaðan stuðning fyrir eftirfarandi víddir. POS getur sjálfkrafa fært inn sumar þessara vídda í birgðafærslum, byggt á skilgreiningu vöruhúss eða uppsetningu verslunar. POS styður hins vegar ekki víddirnar að fullu eins og þær eru studdar ef sölufærsla er slegin handvirkt inn í Commerce Headquarters. 

- **Staðsetning vöruhúss** – þegar þær nota nýja [aðgerð á innleið](./pos-inbound-inventory-operation.md) og [aðgerð á útleið](./pos-outbound-inventory-operation.md) geta notendur sölustaðaaðgerða valið staðsetningu vöruhúsabirgða til að taka á móti vörum í eða sent vörur út frá. Ef þeir nota úreltu aðgerðina **tiltekt og móttaka**, er takmarkaður staðsetningarstuðningur í boði fyrir móttöku og flutning á útleið. Þessi stuðningur er aðeins tiltækur ef hægt er að nota valkostinn **Nota vöruhúsakerfisferli** fyrir vöruna og vöruhús verslunarinnar. Ekki er hægt að nota birgðastaðsetningu með aðgerðina **birgðatalning** eða **birgðauppfletting**.

- **Númeraplata** – númeraplötur gilda aðeins þegar valkosturinn **Nota vöruhúsakerfisferli** hefur verið virkjaður fyrir vöruna og vöruhús verslunar. Á sölustað, ef tekið er á móti birgðum í vöruhúsi verslunar með því að nota **aðgerð á innleið** eða **Tiltekt og móttaka** þar sem ferli vöruhúsakerfis hefur verið virkjað, og ef staðsetningu sem valin er til að taka á móti vörunni er tengd við staðsetningarforstillingu sem krefst stjórnunar á númeraplötu, bætir forrit sölustaðar kerfisbundið númeraplötu við móttökulínuna. Sölustaðarnotendur geta ekki breytt eða stjórnað þessum gögnum númeraplötu. Ef þörf er á fullri stjórnun á númeraplötum er mælt með því að verslunin noti [vöruhúsaforrit](../supply-chain/warehousing/install-configure-warehousing-app.md) eða biðlara bakvinnslu til að stjórna móttöku á þessum vörum.

- **Raðnúmer** – sölustaðarforrit býður upp á takmarkaðan stuðning við skráningu á einu raðnúmeri í sölufærslulínu fyrir pantanir sem eru stofnaðar á sölustað og taka með raðaðar vörur. Þetta raðnúmer er ekki sannprófað gagnvart skráðum raðnúmerum sem eru nú þegar í birgðum. Ef sölupöntun er stofnuð í rás símavers eða uppfyllt í gegnum ERP og mörg raðnúmer eru skráð á staka sölulínu í uppfyllingarferlinu í ERP, verður ekki hægt að nota eða sannprófa þessi raðnúmer ef unnið er úr skilum á sölustað fyrir þessa pöntun. Þegar birgðir hafa verið mótteknar með aðgerðinni **aðgerð á innleið** geta notendur [skráð inn eða staðfest raðnúmerin sem eru móttekin](./pos-serialized-items.md).

- **Runukenni** – Forrit sölustaðar býður upp á takmarkaðan stuðning í uppgjörsbókun ef runustýrð vara er seld, en notendur sölustaðar geta ekki skilgreint runukennið sem var selt eða sótt þegar forrit sölustaðar var notað.

- **Birgðastaða** – Fyrir vörur sem nota ferli vöruhúsakerfis og þurfa birgðastöðu, verður ekki hægt að stilla eða breyta þessum stöðureit í gegnum forrit sölustaðar. Sjálfgefin birgðastaða eins og hún er skilgreind í skilgreiningu fyrir vöruhús verslunar verður notuð þegar vörur eru mótteknar í birgðum.

> [!NOTE]
> Öll fyrirtæki verða að prófa vöruafbrigðin í gegnum Commerce í þróunar- eða prófunarumhverfi áður en þau nota þessir vöruafbrigði í vinnsluumhverfum. Prófið vörurnar með því að nota þær til að framkvæma venjulegar sölufærslur staðgreiðslu á sölustað og stofna pantanir viðskiptavinar (ef það á við) í gegnum sölustað, símaver eða rafræn viðskipti til að ganga úr skugga um að hægt sé að styðja þær að fullu. Einnig ætti að prófa uppfyllingar sölustaðar og birgðaferli (svo sem móttaka birgða og uppfyllingaraðgerðir pöntunar) áður en ný vöruafbrigði eru sett upp, til að ganga úr skugga um að sölustaðarforrit geti stutt þau. Prófun verður að fela í sér að keyra ítarleg bókunarferli uppgjörs/pöntunar í prófunarumhverfinu og staðfesta að engin bókunarvandamál séu til staðar þegar pantanir fyrir þessar vörur eru stofnaðar og bókaðar í Commerce Headquarters.
>
> Ef vörur eru skilgreindar þannig að þær eru ekki studdar af forritum Commerce og viðeigandi prófun er ekki framkvæmd, geta komið upp gagnabilanir sem er ekki svo auðvelt að lagfæra eða jafnvel ekki hægt að laga yfirhöfuð.

## <a name="purchase-orders"></a>Innkaupapantanir

Innkaupabeiðnir eru stofnaðar í Commerce Headquarters. Ef vöruhús verslunar er tekin með í haus innkaupapöntunar eða á innkaupapöntunarlínum er hægt að taka á móti línunum í versluninni með aðgerðinni [aðgerð á innleið](./pos-inbound-inventory-operation.md) á sölustað. 

## <a name="transfer-orders"></a>Flutningspantanir

Hægt er að stofna flutningspantanir í Commerce Headquarters eða í gegnum annað hvort [aðgerð á innleið](./pos-inbound-inventory-operation.md) eða [aðgerð á útleið](./pos-outbound-inventory-operation.md) í sölustað. Notið **aðgerð á innleið** POS-aðgerð til að stofna flutningspöntunarbeiðni til að hafa birgðir sendar í verslun frá öðru vöruhúsi eða geymslustað. Notaðu **aðgerð á útleið** POS-aðgerð til að stofna flutningspöntunarbeiðni til að hafa birgðir sendar úr versluninni í annað vöruhús eða geymslustað. Eftir að flutningspöntun fyrir verslun er stofnuð getur þessi verslun stjórnað móttöku birgða fyrir flutningspöntunina í gegnum **aðgerð á innleið** á sölustað. Ef verslunin er að senda birgðir á aðra staðsetningu, er **aðgerð á útleið** á sölustaðnum notuð til að stjórna sendingu á útleið í þessari verslun.

## <a name="stock-counts"></a>Birgðatalning

Birgðatalningar geta verið annaðhvort áætlaðar eða óskipulagðar. Áætlaðar birgðatalningar eru stofnaðar í gegnum Commerce Headquarters með því að stofna talningarbókarskjal sem er tengt við vöruhúsið fyrir verslunina. Þessi færslubók tilgreinir vörurnar sem þarf að telja. Í versluninni er síðan hægt að fá aðgang að þessum fyrirframgefnu talningarbókum og vinna með þær með því að nota **birgðatalning** í sölustað. Notendur verslunar hafa frumkvæði að óundirbúinni birgðatalningu þar sem þess er krafist þegar þeir nota **birgðatalning** í sölustað. Ólíkt áætlaðri birgðatalningu hafa óundirbúnar birgðatalningar ekki fyrirfram skilgreindan lista yfir vörur. Þegar birgðatalningu af annarri hvorri gerð er lokið á sölustað er henni ráðstafað og hún send til aðalskrifstofu. Á aðalskrifstofu er talningin villuleituð og bókuð sem aukaskref í Commerce Headquarters.

## <a name="inventory-lookup"></a>Birgðauppfletting

Núverandi afurðarmagn á lager fyrir margar verslanir og vöruhús er hægt að skoða á síðunni **Uppfletting á birgðum**. Til viðbótar við núverandi magn á lager er hægt að skoða magn sem tiltækt er að lofa í framtíðinni (ATP) fyrir hverja verslun. Veldu verslunina til að skoða ATP-magn fyrir og veldu síðan **Sýna tiltækileika verslunar**. Upplýsingar um skilgreiningarvalkostina sem eru í boði er að finna í [Reikna út birgðaframboð fyrir smásölurásir](./calculated-inventory-retail-channels.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]