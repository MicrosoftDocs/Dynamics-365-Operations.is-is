---
title: "Fjarvistarskráning í Tími og mæting"
description: "Í þessu efnisatriði er útskýrt hvernig á að meðhöndla fjarvistarskráningu í Tími og mæting."
author: johanhoffmann
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JMGParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 477724e6211a084638e8a0b7133f60edef07b3ad
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="absence-registration-in-time-and-attendance"></a>Fjarvistarskráning í Tími og mæting

[!include [banner](../includes/banner.md)]

Þetta efni lýsir hugtökunum um fjarveru og útskýrir hvernig á að meðhöndla fjarveru í Tíma og mætingu.

## <a name="absence-that-is-based-on-regular-work-hours"></a>Fjarvist sem er byggður á venjulegum vinnustundum

Starfsmenn eru talin fjarverandi allar klukkustundir sem þeir vinna ekki á venjulegum vinnutíma. Venjulegur vinnutími er skilgreindur í forstillingu staðalvinnutíma starfsmanns.

Til dæmis vinnur starfsmaður á forstillingu dags útfrá innstimplun klukkan 07:00 og útstimplun klukkan 15:00. Ef starfsmaður stimplar sig inn klukkan 09:00 er hann talinn fjarverandi frá 07:00 til 09:00 á þeim degi.

Í þessu tilviki eru starfsmenn beðnir um að slá inn ástæðu fyrir fjarveru þeirra. Þeir geta skilgreint ástæðu með því að velja fjarveru kóða.

## <a name="absence-codes"></a>Fjarvistarkóðar

Gerðir fjarvistarkóða leyfa skilgreina hinar ýmsu gerðir fjarvista. Fyrirtækin skilgreina kóðana.

Ýmsar reglur er hægt að setja um fjarvistarkóða. Til dæmis er hægt að stilla fjarvistarkóða til að draga frá eða veita greiðslur.

Til dæmis skilgreinir fyrirtæki **Seint** frágangskóði sem starfsmenn nota ef þeir koma seint og hafa ekki góða ástæðu. Fyrirtækið skilgreinir einnig **innri námskeið** fjarvistarkóða sem starfsmenn nota fyrir tíma sem þeir eyða að sækja innri námskeið. Þessar fjarvistarkóðar geta verið settar upp þannig að **Seint** dregur frá launum starfsmanns en **innri námskeið** dregur ekki frá launum starfsmanns.

Hægt er að setja upp sjálfvirka fjarvistarkóða. Þessar fjarverukóðar geta verið notaðir til að reikna tíma starfsmanns þegar engin fjarvist er skráð. Forstilling starfsmanns ákvarðar hvort fjarvistarkóði fyrir staðlaðan tíma eða sveigjanlegan tíma er notuð.

### <a name="set-up-standard-time-and-flex-time"></a>Setja upp staðlaðan og sveigjanlegan tíma

- Stilla færibreytur fyrir staðlaða tíma og sveigjanlegan tíma með því að nota **sjálfvirka innsetning fjarvista** og **sjálfvirk innsetningu sveigjanlegt** valmöguleikar á **tími og mæting færibreytur** síðunni.

## <a name="absence-groups"></a>Fjarvistaflokkar

Fjarvistarkóðar eru flokkaðar í fjarveruhópa. Fjarvistarflokkar eru notaðir til að flokka fjarvistarkóða sem hafa svipaða eiginleika í hóp. Dæmi um það eru fjarvistarkóðar vegna lagalegrar fjarvistar eða fjarveru vegna læknisheimsóknar, kviðdómsskyldu eða barns sem er lasið.

## <a name="planned-absence"></a>Áætlaðar fjarvistir

Ef þú veist að starfsmaður verður fjarverandi um tíma, svo sem komandi frí, getur þú notað áætlaða fjarvist. Þú setur upp áætlaðan fjarvist með því að stilla fjarvistarkóðann þannig að hann geri ráð fyrir áætlaðri fjarvist. Þegar þú setur upp áætlaða fjarvist ertu ekki beðin(n) um fjarvistarkóða meðan á fjarveru stendur þegar skráningar notandatíma eru reiknuð. Áætlaða fjarvist er hægt að skilgreina fyrir einn starfsmann, eða þú getur skilgreint runuvinnslu til þess að fjöldauppfæra áætlaðar fjarvistir fyrir starfsmenn.

### <a name="set-up-planned-absence"></a>Setja upp áætlaða fjarvist

1. Veldu **Mannauður** &gt; **Starfsfólk** &gt; **Starfsmenn** og veldu starfsmann.
2. Veldu **Tími** &gt; **Tími úthlutanir** &gt; **Tími fjarvistarskráning** og setja upp fyrirhugaða fjarvist.

## <a name="interrupted-planned-absence"></a>Rof á ætlaðri fjarvist

Ef þú notar **Rof** valkostinn þegar þú setur upp áætlaða fjarvist verður áætlaða fjarvistin rofin ef starfsmaðurinn skráir sig á áætlaðan fjarvistartíma. Áætluð fjarvist verður merkt sem **Rofin** og mun ekki hafa nein áhrif á framtíðarútreikninga.

### <a name="set-up-a-planned-absence-for-interruption"></a>Setja upp áætlaða fjarvist fyrir rof

1. Opnaðu **Skráningar tíma fjarvista** síðuna eins og lýst er í ferlinu til að setja upp áætlaða fjarvist.
2. Velja **Rof**.

**Rof** valkosturinn á við þegar tími er skráður í gegnum vinnusal afgreiðslustöðvar eða tæki vinnusals. Valkosturinn gildir ekki ef skráningar eru færðar inn á útreikninga- og samþykktarsíðunum, eða á **rafrænt tímaspjald** síðunni.

## <a name="examples-of-the-use-of-absence-in-a-flex-profile"></a>Dæmi um notkun á fjarvist í sveigjanlegri forstillingu

Eftirfarandi þrjú dæmi sýna hvernig fjarvistir eru reiknaður út í forstillingu sem hefur sveigjanlegan tíma.

Í dæmunum er notuð eftirfarandi forstilling.

| Innstimplun | Staðaltími    | Hlé             | Staðaltími | Sveigjanlegt-        | Útstimplun | Sveigjanlegt+        |
|----------|------------------|-------------------|---------------|--------------|-----------|--------------|
| 08:00     | 09:30 til 11:30 | 11:30 til 12:00 | 12:00 til 15:00 | 15:00 til 16:00 | 16:00      | 16: 00 til 18: 00 |

### <a name="example-1-signing-out-during-a-flex--period"></a>Dæmi 1: Útskráning á sveigjanlegum tíma

Starfsmaðurinn stimplar sig inn klukkan 08:00 og út klukkan 15:30. Í þessu tilfelli, vegna þess að starfsmaður stimplar sig út á sveigjanlegum tíma, er engin fjarvera reiknuð og hálftíma er dreginn frá stöðu sveigjanlegs tíma starfsmannsins.

### <a name="example-2-signing-out-in-during-standard-time-period"></a>Dæmi 2: Innskráning á stöðluðum tíma

Starfsmaðurinn stimplar sig inn klukkan 08:00 og út klukkan 14:30. Í þessu tilviki, vegna þess að starfsmaður klukkur út á stöðluðum tíma, er fjarvera reiknuð frá kl. 14:30 til 16:00 og 1,5 klst. fjarvist er skráð. Krafist er fjarvistarkóða fyrir það tímabil.

### <a name="example-3-signing-out-during-a-flex-period"></a>Dæmi 3: Útskráning á sveigjanlegum+ tíma

Starfsmaðurinn stimplar sig inn klukkan 08:00 og út klukkan 16:30. Í þessu tilfelli, vegna þess að starfsmaður stimplar sig út á sveigjanlegum+ tíma, er engin fjarvera reiknuð og hálftíma er bætt við stöðu sveigjanlegs tíma starfsmannsins.

## <a name="absence-in-the-calculation-and-approval-process"></a>Fjarvistir í útreiknings- og samþykktarferlinu

Skráningar vinnutíma starfsmanns þarf að reikna og samþykkja áður en hægt er að flytja þær í launakerfi sem greiðslur.

Samþykkjandi getur breytt tímaskráningum starfsmanns. Samþykkjandinn getur jafnvel breytt öllum fjarvistarkóðum sem starfsmaðurinn hefur skráð. Ef samþykkjandinn fer inn í tímabil sem hefur fjarvistarkóða, er fjarvistarkóða þess tímabils ekki hnekkt af sjálfgefnum fjarvistarkóða frá færibreytum Tíma og mætinga.

Starfsmaður stimplar sig t.d. inn klukkan 10:00 og velur fjarvistarkóða sem gefur til kynna að hann sé seinn. Seinna upplýsir starfsmaður yfirmann sinn um það að hann hafi þurft til læknis frá kl. 8:00 til 10:00. Læknisheimsókn skal ekki leiða til frádráttar af launum starfsmanns. Þar af leiðandi getur umsjónarmaðurinn í þessu tilviki leiðrétt tvær klukkustundir frá kl. 8:00 til 10:00 með því að slá handvirkt inn fjarvistarkóða sem gefur til kynna veikindi fyrir þessar tvær klukkustundir.

### <a name="calculate-and-approve-absence"></a>Reikna út og samþykkja fjarvistir

- Veldu **Tími mæting** &gt; **Skoða og samþykkja** &gt; **Samþykkja eða Reikna**.

