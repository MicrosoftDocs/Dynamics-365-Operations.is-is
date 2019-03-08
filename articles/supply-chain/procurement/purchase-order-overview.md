---
title: Yfirlit yfir „Innkaupapöntun“
description: Þessi grein inniheldur almennar upplýsingar um innkaupapantanir (POs) og tengir viðbótar greinum sem eru tengdar við mörg stig sem Innkaupapöntun fer í gegnum.
author: FrankDahl
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 93083
ms.assetid: e9b7bc5b-1d7e-4ec2-97be-d655274b0613
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b86e934a0ac25b1fe77a3359b74e707fb372ae6b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "338982"
---
# <a name="purchase-order-overview"></a>Yfirlit yfir „Innkaupapöntun“

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

Þessi grein inniheldur almennar upplýsingar um innkaupapantanir (POs) og tengir viðbótar greinum sem eru tengdar við mörg stig sem Innkaupapöntun fer í gegnum.

Innkaupapöntunina (PO) er skjal sem stendur fyrir samningur við lánardrottinn til að kaupa vörur eða þjónustu. Skjalið hjálpar einnig fylgjast með innhreyfingarskjöl afurða sem eru framleiddra átt pöntunina og síðar, bókhald lánardrottnareikninga sem lánardrottins reikningsfæra til pöntunar.  

**Innkaupapantanir** síða inniheldur yfirlit yfir tiltækar pantanir og gerir það mögulegt að breyta þeim pöntunum. Þegar Innkaupapöntun er opnuð, er hægt að velja á **Haus** yfirlit, sem inniheldur upplýsingar sem er tilgreint aðeins einu sinni fyrir hverja Innkaupapöntun, svo sem upplýsingar um lánardrottin. Einnig er hægt að velja **Línur** yfirlit þar sem hægt er að breyta pöntunarlínum. Yfirleitt hægt verður að skipta á milli þessara tveggja yfirlita þegar innkaupapöntunum er breytt. Gjöldum ekki eru skráð beint á **Innkaupapantanir** síðunni en er hægt að fá aðgang í valmyndir í haus pöntunar og línum.  

Það eru margar skýrslur þar sem hægt er að skoða upplýsingar um innkaupapantanir, innhreyfingarskjölum afurða og reikningum lánardrottins. Þessum skýrslum finnast í **Innkaup og aðföng** og **Viðskiptaskuldir** kerfiseiningar.  

**undirbúningi innkaupapöntunar** og **móttöku innkaupapöntunar Og eftirfylgni** vinnusvæðin gera kleift að skoða lista yfir innkaupapantanir í mismunandi stöðum sem þeir hafa verið komin til. Þær veita einnig yfirlit yfir aðgerðir sem þarf að framkvæma. **Undirbúningi innkaupapöntunar** vinnusvæði er einbeitt á stofnun Innkaupapöntunar og vinnslu pöntunar gegnum samþykkis og staðfestingar lánardrottins. **Móttöku innkaupapöntunar Og eftirfylgni** vinnusvæði er einbeitt á vinnslu móttöku af vörum eða þjónustu gegn innkaupapöntun. Það felur í sér lista sem veita innsýn í innhreyfingar sem eru í vanskilum eða sem verður brátt til afhendingu af birgi. Þessar vinnusvæðin ekki eru notað til að framkvæma aðgerðir tengdar innhreyfingar sem gerðar eru í vöruhúsinu. Þessar aðgerðir eru framkvæmdar með því að nota síðurnar í **Birgðastjórnun** og **Vöruhúsakerfi** kerfiseiningar. Vinnslu á reikningum lánardrottna ætti að gera með því að nota **skráningu reiknings Lánardrottins** vinnusvæði og greiðslur á að framkvæma með því að nota **lánardrottnagreiðslur** vinnusvæði.  

Eftirfarandi greinum veita yfirlit yfir mismunandi stigum Innkaupapöntun fer í gegnum:

-   [Stofnun innkaupapöntunar](purchase-order-creation.md)
-   [Staðfesting innkaupapöntunar og samþykki](purchase-order-approval-confirmation.md)
-   [innhreyfingarskjal afurða gagnvart innkaupapantanir](product-receipt-against-purchase-orders.md)
-   [Yfirlit yfir lánardrottnareikninga](../../financials/accounts-payable/vendor-invoices-overview.md)

## <a name="types-of-purchase-orders"></a>Gerðir innkaupapantana
Það eru þrjár gerðir innkaupapantana. Þegar innkaupapöntun er stofnuð verður að tilgreina gerð. Hægt er að setja upp sjálfgefna pöntunargerð fyrir nýjar pantanir á **færibreytur Innkaupa og aðfanga** síðu.

| IP-gerð        | Lýsing                                                                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Færslubók        | Notið þessa gerð til þess að stofna uppkast af pöntun. Þessi gerð hefur ekki áhrif á lagermagn eða myndar birgðafærslur. Innkaupapöntunarbókarlínur eru ekki teknar með í  aðalröðun.                                                                                                       |
| Innkaupapöntun | Þessi gerð er notuð til að stofna innkaupapantanir þegar pantanir eru staðfestar við lánardrottinn og meðan pantanir eru unnar í gegnum innhreyfingu og reikningsfærslu áður en gengið er frá greiðslu til lánardrottins. Þessi gerð Innkaupapöntunar er algengastar.                                                                          |
| Skilapöntun | Notið þessa gerð þegar vörum er skilað aftur til lánardrottins. Þessi gerð af pöntunar krefst þess að tilgreina númer skila efni vöruskilaheimildar (RMA) sem lánardrottinn veitir. Rma-númer er tilgreint á **Almennt** flipanum á Innkaupapöntun. Pöntunarlínurnar verður hafa neikvætt magn. |

## <a name="purchase-order-statuses"></a>Staða innkaupapöntunar
Innkaupapantanir hafa stöðusvæði sem sýna framvindu pöntunarinnar. Þessi svæði eru sjáanleg í **Haus** yfirlit pöntuninni og fáir þeirra eru einnig sýnilegt í hnitanetinu yfirlit yfir allar pantanir. **Stöðu** svæðið sýna stöðu fyrir magn í pöntun. Eftirtalin gildi eru tiltæk:

-   **Opin pöntun** – pantanir hafa verið stofnaðar og magni eru í pöntun.
-   **Móttekið** – Eitthvað af því magni sem hefur verið móttekið en hefur ekki verið reikningsfærð enn.
-   **Reikningsfærðar** – fullt magn í pöntun hefur verið reikningsfærð. **Athugasemd:** Ef pöntun hefur verið *hluta* reikningsfærðar, hvorki **Móttekið** stöðu né **Reikningsfært** staða er viðeigandi. Þess vegna er pöntunin enn skráðar stöðuna **Opin pöntun**.
-   **Hætt við** – pöntunin var staðfest en hætt við síðar. Þar af leiðandi þessi staða tilgreinir að ekki lengur opið magn í pöntun.

**Skjalastaða** svæði hjálpar til við að fara yfir framvindu pöntunarinnar í skjölum sem hafa verið unnin. Hún sýnir stöðu nýjustu skjalið sem hefur verið lokið fyrir pöntunina. Eftirtalin gildi eru tiltæk:

-   **Ekkert** – Ekkert skjal hefur verið unnin fyrir pöntun enn.
-   **Innkaupafyrirspurn** – innkaup fyrirspurn hefur verið mynduð og pöntun bíður svörun frá lánardrottni.
-   **Innkaupapöntun** – Staðfesting hefur verið unnin í pöntun.
-   **Innhreyfingarskjal afurða** – Innhreyfingarskjal afurða hefur verið unnin í pöntun.
-   **Reikningur** – reikningur hefur verið kostnaðarfært við pöntunina.

**samþykktarstöðu** svæði er notað þegar Innkaupapöntun fer í gegnum endurskoðunarferli eða verkflæði. Eftirtalin gildi eru tiltæk:

-   **Drög**, **í yfirferð**, og **Hafnað** – Þessar stöður eru eingöngu notaðar þegar samþykkis verkflæðis er notaður fyrir Innkaupapöntunina.
-   **Samþykkt** – Þessi staða er úthlutað til pantana sem hafa lokið verkflæðissamþykki. Pantanirnar sem eru stofnaðar án samþykkis verkflæðis fá stöðuna **Samþykkt** strax.
-   **Í ytri yfirferð** – Þessi staða er notuð í aðstæðum þar sem fyrirspurn um innkaup er send til lánadrottna, þannig að lánardrottinn geti staðfesta greiðsluskilmála í Innkaupapöntun. Þessi staða er einnig notuð við vinnslu sem er hafin með **Staðfestingu beiðni** aðgerð. Þetta ferli, lánardrottins beðnir um að staðfesta greiðsluskilmála í Innkaupapöntun með tengingu við kerfið þitt og skrá hvort hún staðfestir eða hafnað pöntunina.
-   **Staðfesta** – Þessi staða er úthlutað eftir að pöntun hefur verið staðfest. Venjulega er þessi staða síðustu stöðu samþykkis sem úthlutað er pöntun.


<a name="additional-resources"></a>Frekari upplýsingar
--------

[Stofnun innkaupapöntunar](purchase-order-creation.md)

[Staðfesting innkaupapöntunar og samþykki](purchase-order-approval-confirmation.md)

[innhreyfingarskjal afurða gagnvart innkaupapantanir](product-receipt-against-purchase-orders.md)

[Yfirlit yfir lánardrottnareikninga](../../financials/accounts-payable/vendor-invoices-overview.md)



