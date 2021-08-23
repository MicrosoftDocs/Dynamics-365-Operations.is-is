---
title: Rekja þóknanir í sölustað (POS) með notkun söluflokka
description: Það er algengur háttur smásölu til að rekja sölu eftir samstarfsmanni sem vann með viðskiptavininum — veitti aðstoð, setti upp söluviðauka, krosssölu og vann færsluna.
author: jblucher
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: ca77ad5564cc93e9fcf335b5a49548f91c7c13face41fd73477ae4083f78be57
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6770910"
---
# <a name="track-commissions-in-the-point-of-sale-pos-by-using-sales-groups"></a>Rekja þóknanir í sölustað (POS) með notkun söluflokka

[!include [banner](includes/banner.md)]

Það er algengur háttur smásölu að rekja sölu eftir samstarfsmanni sem vann með viðskiptavininum við að — veita aðstoð, setja upp söluviðauka, krossselja og vinna færsluna.

Rakning sölu eftir sölufulltrúa er mæling á söluhæfni starfsmannsins, á meðan sala eftir gjaldkera mæling á hraða og skilvirkni. Sala sem er rakin eftir sölufulltrúa er einnig oft notuð til að reikna þóknanir eða aðra hvata.

## <a name="configuring-a-worker-to-be-a-sales-representative-in-pos"></a>Grunnstilling starfsmanns til að vera sölufulltrúi í POS

Þegar starfsmanni er bætt við söluflokk verður hann hæfur fyrir þóknun og hægt er að auðkenna hann sem sölufulltrúa í kerfinu. Starfsmaður sem er ekki í söluflokki er ekki hæfur fyrir þóknun og verður ekki talinn upp sem sölufulltrúi í sölustaðarforritinu (POS). Í POS er listi yfir sölufulltrúa fenginn úr öllum söluflokkum sem innihalda a.m.k. einn starfsmann sem er úthlutað á verslunina. Listinn birtist í POS sem samsetning af kenni söluflokks og nafns (Kenni: Heiti). Sjálfgefinn flokk sölu er hægt að úthluta til að styðja aðstæður þar sem smásali velur að stilla sölufulltrúa sjálfvirkt á POS-línur. Notendur geta valið úr söluflokkum þar sem starfsmaðurinn er meðlimur.

## <a name="functionality-profile-settings"></a>Stillingar virknireglna

Það eru nokkrar stillingar á virknireglum fyrir verslun sem munu ákvarða flæði og ferli í POS sem snerta sölufulltrúa.

<table>
<thead>
<tr>
<th>Regla</th>
<th>lýsing</th>
</tr>
</thead>
<tbody>
<tr>
<td>Sjálfgefið til gjaldkera þegar til staðar</td>
<td>Ef þessi valkostur er gerður virkur útfyllir POS sjálfkrafa færslulínur með sjálfgefnum söluflokki núgildandi gjaldkera. Ef gjaldkeri hefur ekki sjálfgefinn söluflokk tilgreindan verður gildi ekki stillt. Notandi gæti samt stillt söluflokka handvirkt með hnappahnitum POS-hnappa.</td>
</tr>
<tr>
<td>Kvaðning eftir sölufulltrúa</td>
<td>Þessi valkostur hefur þrjú möguleg gildi:
<ul>
<li><strong>Nei</strong> – Ef þessi valkostur er valinn verður notandi ekki beðinn um að velja söluflokk. Gildi gæti enn verið stillt með því að nota sjálfgefinn söluflokk gjaldkera eða handvirkt með því að nota hnappahnit POS-hnappa.</li>
<li><strong>Upphaf færslu</strong> – Ef þessi valkostur er valinn og annaðhvort er valkosturinn <strong>Sjálfgefið til gjaldkera</strong> ekki virkur eða gildandi gjaldkeri hefur ekki sjálfgefinn söluflokk, verður notandinn beðinn um að velja söluflokk við upphaf hverrar færslu. Val á söluflokki úr þessari kvaðningi gerir allar síðari línur sjálfgefnar í valinn flokk. Notandi gæti samt stillt söluflokka handvirkt með hnappahnitum POS-hnappa.</li>
<li><strong>Fyrir hverja línu</strong> – Ef þessi valkostur er valinn og annaðhvort er valkosturinn <strong>Sjálfgefið til gjaldkera</strong> ekki virkur eða gildandi gjaldkeri hefur ekki sjálfgefinn söluflokk, verður notandinn beðinn um að velja söluflokk þegar hverri línu er bætti við. Notandi gæti samt stillt söluflokka handvirkt með hnappahnitum POS-hnappa.</li>
</ul>
</td>
</tr>
<tr>
<td>Áskilið</td>
<td>Þessi valkostur á einungis við þegar POS er skilgreint til að biðja um sölufulltrúa. Ef hann er virkjaður þarf notandinn að velja söluflokk áður en haldið er áfram. Annars fær notandinn kvaðningu, en getur hætt við og haldið áfram án þess að velja. Eftir að línunni hefur verið bætt við getur notandi með nægilegar heimildir samt að fjarlægt söluflokka úr línunni. „Krefjast sölufulltrúa“ er ekki áskilið í þessari stöðu.</td>
</tr>
</tbody>
</table>

## <a name="displaying-the-sales-representative-information-on-the-pos-transactions-screen"></a>Birting upplýsinga sölufulltrúa á færsluskjá POS

Útlit og efni færsluskjás POS er skilgreinanlegr með því að nota á skjá útlit hönnuðar og úthlutuðum útlit afgreiðsluskjás á verslanir, afgreiðslukassar eða starfsmenn. Hægt er að bæta við svæðinu **Sölufulltrúi** á flipanum Línur í kvittunarrúðunni.  Þetta mun birta Kenni tilgreinds söluflokks fyrir hverja línu á færsluskjánum.

## <a name="adding-sales-representative-operations-to-pos-button-grids"></a>Bæta við Sölu sölufulltrúa aðgerðir á Sölustað hnappinn hnitanet

POS gerir notendum kleift að skilgreina hnappahnit sem eru höfð með í útliti afgreiðsluskjás til að veita aðgang að aðgerðir POS. Hægt er að úthluta eftirfarandi aðgerðum POS á hnappahnitum sem snerta sölufulltrúa.

| Aðgerð                                 | lýsing |
|-------------------------------------------|-------------|
| Stilla sölufulltrúa í línu          | Þessi aðgerð POS birtir lista yfir hæfa söluflokka (Kenni: Heiti) fyrir verslunina. Val á söluflokki af listanum mun stilla gildið í núgildandi færslulínu. |
| Hreinsa sölufulltrúa í línu        | Þessi aðgerð POS fjarlægir núgildandi gildi söluflokks úr núgildandi færslulínu. |
| Stilla sölufulltrúa í færslu   | Þessi aðgerð POS birtir lista yfir hæfa söluflokka (Kenni: Heiti) fyrir verslunina. Val á söluflokki af listanum mun stilla sjálfgildið í núgildandi færslu. Öllum fyrirliggjandi línum án söluflokks verður úthlutað, ásamt öllum línum sem síðar hefur verið bætt við. |
| Hreinsa sölufulltrúa í færslu | Þessi aðgerð POS fjarlægir núgildandi sjálfgildi söluflokks úr núgildandi færslu. Það ekki áhrif á þær línur sem þegar eru til í færslunni. |

## <a name="calculating-commissions"></a>Útreikningur á þóknun

Þóknun er reiknuð fyrir starfsmenn í tilgreindum söluflokkum við bókun uppgjörs eða bókun sölupöntunar. Upphæð þóknunar er ákvörðuð samkvæmt þóknunarhluta starfsmanns, eins og skilgreint er í söluflokki og stillingum útreikninga fyrir tengda þóknun fyrir viðskiptavin og/eða afurðir í færslunni.


[!INCLUDE[footer-include](../includes/footer-banner.md)]