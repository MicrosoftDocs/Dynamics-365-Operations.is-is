---
title: "Yfirlit yfir „Innkaupapöntun“"
description: "Þessi grein inniheldur almennar upplýsingar um innkaupapantanir (POs) og tengir viðbótar greinum sem eru tengdar við mörg stig sem Innkaupapöntun fer í gegnum."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: PurchTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 93083
ms.assetid: e9b7bc5b-1d7e-4ec2-97be-d655274b0613
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: aed1a411aaefeebb96c2b922afc2e3e7f82cdbb7
ms.lasthandoff: 03/31/2017


---

# <a name="purchase-order-overview"></a>Yfirlit yfir „Innkaupapöntun“

Þessi grein inniheldur almennar upplýsingar um innkaupapantanir (POs) og tengir viðbótar greinum sem eru tengdar við mörg stig sem Innkaupapöntun fer í gegnum.

Innkaupapöntunina (PO) er skjal sem stendur fyrir samningur við lánardrottinn til að kaupa vörur eða þjónustu. Skjalið hjálpar einnig fylgjast með innhreyfingarskjöl afurða sem eru framleiddra átt pöntunina og síðar, bókhald lánardrottnareikninga sem lánardrottins reikningsfæra til pöntunar.  

**Innkaupapantanir** síða inniheldur yfirlit yfir tiltækar pantanir og gerir það mögulegt að breyta þeim pöntunum. Þegar Innkaupapöntun er opnuð, er hægt að velja á **Haus** yfirlit, sem inniheldur upplýsingar sem er tilgreint aðeins einu sinni fyrir hverja Innkaupapöntun, svo sem upplýsingar um lánardrottin. Einnig er hægt að velja **Línur** yfirlit þar sem hægt er að breyta pöntunarlínum. Vanalega verður skipt er á milli þessara tvö yfirlit sem er að breyta Sölustaðar. Gjöld sem ekki eru kostnaðarjafnaðar skráð beint á **Innkaupapantanir** síðunni en eru opnaðar með valmyndir í haus og línum.  

Það eru margar skýrslur þar sem hægt er að skoða upplýsingar um innkaupapantanir, innhreyfingarskjölum afurða og reikningum lánardrottins. Þessum skýrslum finnast í **Innkaup og aðföng** og **Viðskiptaskuldir** kerfiseiningar.  

**undirbúningi innkaupapöntunar** og **móttöku innkaupapöntunar Og eftirfylgni** vinnusvæðin gera kleift að skoða lista yfir innkaupapantanir í mismunandi stöðum sem þeir hafa verið komin til. Þær veita einnig yfirlit yfir aðgerðir sem þarf að framkvæma. **Undirbúningi innkaupapöntunar** vinnusvæði er einbeitt á stofnun Innkaupapöntunar og vinnslu pöntunar gegnum samþykkis og staðfestingar lánardrottins. Í **móttöku innkaupapöntunar Og eftirfylgni** vinnusvæði er focused á móttöku af vörum eða þjónustu gegn POs í vinnslu. Það felur í sér lista sem veita insight í innhreyfingum sem eru í vanskilum eða sem verður brátt til greiðslu fyrir afhendingu af birgi. Þessar vinnusvæðin ekki eru notað til að framkvæma aðgerðir tengdar innhreyfingar sem gerðar eru í vöruhúsinu. Þessar aðgerðir eru framkvæmdar með því að nota síðurnar í **Birgðastjórnun** og **Vöruhúsakerfi** kerfiseiningar. Vinnslu á reikningum lánardrottna ætti að gera með því að nota **skráningu reiknings Lánardrottins** vinnusvæði og greiðslur á að framkvæma með því að nota **lánardrottnagreiðslur** vinnusvæði.  

Eftirfarandi greinum veita yfirlit yfir mismunandi stigum Innkaupapöntun fer í gegnum:

-   [Stofnun innkaupapöntunar](purchase-order-creation.md)
-   [Staðfesting innkaupapöntunar og samþykki](purchase-order-approval-confirmation.md)
-   [innhreyfingarskjal afurða gagnvart innkaupapantanir](product-receipt-against-purchase-orders.md)
-   [Yfirlit reikninga lánardrottina](/dynamics365/operations/financials/accounts-payable/vendor-invoices-overview)

## <a name="types-of-purchase-orders"></a>Gerðir innkaupapantana
Það eru þrjár gerðir POs. Þegar Innkaupapöntun er stofnuð verður að tilgreina gerð. Hægt er að setja upp sjálfgefna pöntunargerð fyrir nýjar pantanir á **færibreytur Innkaupa og aðfanga** síðu.

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


<a name="see-also"></a>Sjá einnig
--------

[Purchase order creation](purchase-order-creation.md)

[Staðfesting og samþykkt innkaupapöntunar](purchase-order-approval-confirmation.md)

[innhreyfingarskjal afurða gagnvart innkaupapantanir](product-receipt-against-purchase-orders.md)

[Yfirlit reikninga lánardrottina](/dynamics365/operations/financials/accounts-payable/vendor-invoices-overview)


