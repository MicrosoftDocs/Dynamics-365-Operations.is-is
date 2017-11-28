---
title: "Samstarf lánardrottna við viðskiptavini"
description: "Þessi efni lýsir því hvernig hægt er að nota samstarf lánardrottna í Finance and Operations til að vinna með IP og fylgjast með vörusendingabirgðum."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ConsignmentProductReceiptLines, ConsignmentVendorPortalOnHand, PurchVendorPortalConfirmedOrders, PurchVendorPortalOriginalOrder, PurchVendorPortalResponsesHistoryList, PurchVendorPortalResponsesPart
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 221234
ms.assetid: 6e69fb8b-6d3a-46ef-88cf-6d01212aa7c3
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4ad7c4f14cf60b2f59124ac98d55c4b92edabb47
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="vendor-collaboration-with-customers"></a>Samstarf lánardrottna við viðskiptavini

[!include[banner](../includes/banner.md)]


Þessi efni lýsir því hvernig hægt er að nota samstarf lánardrottna í Finance and Operations til að vinna með IP og fylgjast með vörusendingabirgðum.

Þessi efni lýsir því hvernig hægt er að nota samstarf lánardrottna við viðskiptavini í Microsoft Finance and Operations. Það felur í sér upplýsingar um hvernig á að fylgjast með og svara innkaupapantanir og hvernig á að fylgjast með vörusendingabirgðir. Einnig er hægt að nota samstarf lánardrottna til að vinna með reikninga. Nánari upplýsingar er að finna í [Vinnusvæði fyrir reikningsfærslur fyrir samstarf lánardrottna](../../financials/accounts-payable/vendor-portal-invoicing-workspace.md).

## <a name="working-with-purchase-orders"></a>Unnið með Innkaupapantanir
Í **staðfesting á Innkaupapöntun** vinnusvæði gerir mögulegt að bregðast við Innkaupapöntunina sem hafa verið send til þín til skoðunar. Það gerir einnig kleift að skoða upplýsingar um IP sem bíða eftir aðgerð frá viðskiptavininum og IP sem hafa verið staðfest en eru enn opnar. Það eru þrjár listum í **staðfesting á Innkaupapöntun** vinnusvæðis:

-   **Innkaupapantanir fyrir yfirferð** -listinn sýnir IP sem hafa verið send að og bíða svars frá þér. Eftir að þú svarar, hverfur Innkaupapöntunin af listanum. Ef viðskiptavinurinn sendir þér ný útgáfa fyrir Innkaupapöntunina áður en þú hefur getað svarað fyrri, birtist aðeins nýjustu útgáfuna.
-   **Beðið eftir aðgerð viðskiptavinar** -Þennan lista gerir þér kleift að sjá IP sem hefur verið svarað, en hefur ekki verið staðfest af viðskiptavini. Ef Innkaupapöntunin er samþykkt af þér, er hægt að fylgjast með henni í þessum lista þar til staðan breytist í **Staðfest**. Ef Innkaupapöntunin er hafnað eða það er samþykkt með breytingar er hægt fylgjast með Innkaupapöntun hér þar til viðskiptavinar sendir nýja útgáfu.
-   **Opna Staðfestar innkaupapöntunum** -listinn inniheldur allar IP fyrir þinn reikninginn sem hafa stöðuna **Staðfest**. Þegar afurðir eða þjónustur eru móttekið að fullu gagnvart Innkaupapöntunin, hverfur Innkaupapöntunin úr listanum.

Eftirfarandi listi sýnir fjórum síðum sem nota má til að vinna við innkaupapantanir, tvö sem innihalda sömu upplýsingar og listar birtir á vinnusvæði:

-   **Innkaupapantanir fyrir yfirferð** (sjá hér á undan)
-   **Staðfestingarsögu lánardrottins fyrir innkaupapantanir** -Þessi síða inniheldur allar IP og útgáfur IP sem hafa verið send til lánardrottins og öllum svörum sem hafa borist frá lánardrottni.
-   **Opna staðfestar innkaupapantanir**(sjá að ofan)
-   **Allar staðfestar innkaupapantanir** -Þessi síða inniheldur allar IP sem hafa verið staðfest, þ.m.t. þær þar sem vörur eða þjónustu hafa verið mótteknar. Hægt er að nota þennan lista til að fylgjast með hvaða IP er hægt að senda reikninga fyrir.

### <a name="responding-to-purchase-orders"></a>Innkaupapöntunum svarað

Innkaupapantanir sem viðskiptavinurinn hefur sent þér til að fara yfir eru ekki sýnilegir í **staðfesting á Innkaupapöntun** vinnusvæðis og á **Innkaupapantanir fyrir yfirferð** síðuna. Eftir Innkaupapöntun er opnuð er hægt að velja að samþykkja hana, hafna henni eða samþykkja hana með breytingum. Það gætu verið viðhengi á haus Innkaupapöntunar eða einstakra lína. Líka er hægt að hengja upplýsingar við svari þínu á einstakar línur eða haus Innkaupapöntunar. Til dæmis gætu lagt til staðgengilsvöru fyrir ein línanna. Forskoðun og prenta Innkaupapöntunina er mögulegt sem pdf-skrá með því að nota **Prenta /Forskoðun** valkostur. Hægt er að fela eða sýna eftirfarandi víddardálka með því að nota **Birta víddir** aðgerð: Svæði, Vöruhúsi, Lit, Stærð, Stíl, Afbrigði. Ef nota á **Samþykkja með breytingum** valkost er hægt að samþykkja eða hafna einstakar línur. Einnig er hægt að gera breytingar á eftirfarandi línum:

-   Breyta dagsetningum eða magn. Ef óskað er að uppfæra staðfestrar afhendingardagsetningar á öllum línum skal nota **Uppfæra afhendingardagsetningu** valkost á haus Innkaupapöntunar.
-   Skipta línum fyrir mismunandi afhendingardagsetningar eða magn.
-   Nota staðgengilsvöru. Til að gera þetta skal færa inn lýsingu á vöru og vörunúmer í **Ytri** reit í **Línuupplýsingar** hluta.

Ekki hægt að breyta verðupplýsingar eða gjöld, en hægt að gera tillögur um breytingar með því að nota athugasemdir. Ef viðskiptavinur sendir þér nýja útgáfu af IP mun hún vera með viðskeyti til að gefa til kynna að það sé breytt útgáfa af Innkaupapöntun sem var áður í gangi. Í **staðfestingarsögu innkaupapantana lánardrottins** síðu getur þú rekja sögu hverja pöntun.

## <a name="monitoring-consignment-inventory"></a>Fylgjast með vörusendingabirgðir
Ef verið er að nota vörusendingabirgðir, geta þú notað viðmót fyrir samstarf lánardrottna til að skoða upplýsingar um eftirfarandi síður:

-   **Innkaupapantanir sem notar vörusendingabirgðir** - innkaupapantanir fyrir vörusendingabirgðir eru myndaðar þegar viðskiptavinur tekur yfir eignarhald á birgðum. Þessum innkaupapantanir vörusendinga birtast aðeins á **Innkaupapantanir sem nota vörusendingabirgðir** síðuna. Eru ekki teknar með í **Allar staðfestar innkaupapantanir** síðu.
-   **Afurðir sem er tekið við úr vörusendingabirgðum** - Þessi síða inniheldur lista yfir allar færslur þar sem eignarhald afurða hefur verið flutt til fyrirtækis sem er að nota birgðirnar. Þú geta nota þessar upplýsingar til að reikningsfæra á viðskiptavininn.
-   **Vörusendingarbirgðir á lager** -Þessi síða sýnir vörusendingarbirgðir á lager í eigu fyrirtækis þíns og er á lager í vöruhúsi viðskiptavinar.


<a name="see-also"></a>Sjá einnig
--------

[Stjórna notendum fyrir samstarf lánardrottna](manage-vendor-collaboration-users.md)




