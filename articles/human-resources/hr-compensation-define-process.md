---
title: Skilgreina launavinnslu og reikna niðurstöður
description: Launavinnslu eru notaðar til að ákvarða nýja upphæðir launa og umbun fyrir starfsmenn sem eru skráðir í fyrirkomulag fastra launa og breytilegrar uppbótar.
author: twheeloc
ms.date: 08/25/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HRMCompProcess, HRMCompProcessLine, HRMCompEvent, HRMCompEventEmpl, HcmCompensationWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 196c907521bba5440f12149abcb2fc446c2aa523
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/04/2022
ms.locfileid: "8687052"
---
# <a name="define-compensation-process-and-calculate-results"></a>Skilgreina launavinnslu og reikna niðurstöður


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Launavinnslu eru notaðar til að ákvarða nýja upphæðir launa og umbun fyrir starfsmenn sem eru skráðir í fyrirkomulag fastra launa og breytilegrar uppbótar. Hægt er að keyra launavinnslu margsinnis til að framkvæma „hvað ef" greiningar til að staðfesta breytingar og stillingar séu réttar. Þetta ferli mun stofna launavinnsla, keyra vinnsluna og skoða niðurstöður. Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.


## <a name="create-a-compensation-process"></a>Stofna Launavinnsla
1. Farðu í **Launastjórnun** > **Úrvinnsla** > **Launavinnsla**.
2. Smelltu á **Ný launavinnsla**.
3. Í reitinn **Ferli** skal slá inn gildi.
4. Í reitinn **Lýsing** skal slá inn gildi.
5. Veljið valkost í svæðinu **Gerð ferlis**.
    * Ferli tilgreinir metið tímabil til að ákvarða umbun. Mat tekur til skoðunar stöður sem starfsmenn voru ráðnir í, hvaða afkastaeinkunnir til að hafa með, útreikningur prósentu af tími sem starfsmaðurinn var ráðinn á meðan á ferlinu stóð, og fleira. Dæmi um upphafsdagsetning ferlis gæti verið fyrsta degi fyrri fjárhagsársins .  
6. Í reitinn **Upphaf ferlis** skal færa inn dagsetningu.
    * Lokadagsetning ferlis er mikilvæg þar sem hún er dagsetningin sem er notuð til að ákvarða hvaða starfsmenn voru í virkri ráðningu og skráður í eitt eða fleiri launafyrirkomulag.  
7. Í reitinn **Endir ferlis** skal færa inn dagsetningu.
    * Virka dagsetningu færslu er dagsetningin sem ný launataxta ætti að taka gildi. Mörg fyrirtæki hafa nokkrar mánuðir á milli þeirra ferlisloka og tímans þegar nýja launataxta tekin í gildi. Viðbótar tími notaður til vinnslu og endurskoða nýja launa.  
8. Í svæðinu **Virka dagsetning færslu**, færið inn dagsetningu.
    * Dagsetning á tímapunkti er notað fyrir breytilegar launafyrirkomulag sem ákvarða upphæð umbunar starfsmanns á grundvelli þeirra launataxti á þessum tímapunkti.  
    * Föst laun hlutfallslega ráðningardagsetning er notuð með föstum bótaáætlunum með ráðningarreglu um **Hlutfall**. Starfsmenn sem ráðnir eru á milli upphafs ferlisins og á föst laun á metið ráðningardagsetning fær 100% af þeirra útreiknuðu launa aukningum, í stað hlutfallslegrar prósentu.  
9. Færa inn dagsetningu í reitnum **Ráðningardagsetning fyrir hlutfallsleg föst laun**.
    * Lokadagsetning endurskoðunar er dagsetningin sem allar niðurstöður ferlis ætti að endurskoða fyrir, svo þær er hægt að hlaða inn launafærslu starfsmanns fyrir virka dagsetningu færslunnar. Þetta svæði er einungis til upplýsingar.  
10. Í reitinn **Endurskoða lokadagsetningu**, skal færa inn dagsetningu.
11. Smelltu á **Vista**.

## <a name="set-up-the-compensation-plans-and-actions-for-a-compensation-process"></a>Settu upp bótaáætlanir og aðgerðir fyrir bótaferli
1. **Smellt er á Uppsetningu.**
    * **Uppsetning** síðu er notuð til að velja hvaða áætlanir sem vinna á sem hluti af þessu launavinnsla, auk hvaða aðgerðir eigi að beita gagnvart hverja áætlun.  
2. Í reitinn **Áætlun** slærðu inn eða velur gildi.
3. Smelltu á **Vista**.
4. Smelltu á **Bæta við**.
5. Velja gerð **Eigin fé** í svæðinu **Aðgerð**.
6. Smelltu á **Bæta við**.
7. Velja **Verðleikategund** aðgerðar í svæðinu **Aðgerð**.
    * Launaaðgerðir getur verið „hlekkjuð" saman með því að nota svæðið **Nota fyrri niðurstöðu** til að gefa til kynna hvort valin aðgerð skuli nota grunnlaunum starfsmenn eða niðurstöður síðustu aðgerðar sem upphafspunkt fyrir útreikning í þessari aðgerð.  
8. Veldu **Já** í **Notaðu fyrri niðurstöðu** sviði.
9. Smelltu á **Bæta við**.
10. Velja **Almenn** gerð aðgerðarinnar í svæðinu **Aðgerð**.
    * Mismunandi launagerðir aðgerða virkja mismunandi svæðum. Fyrir almenna launagerð aðgerðar, er hægt að tilgreina hækkaða prósentu eða hækkaða upphæð.  
11. Veljið valkostinn **Velja upphæð aukningar**.
12. Í reitinn **Upphæð aukningar** skal slá inn númer.
13. Smelltu á **Bæta við**.
14. Veljið **Kynningartilboðsgerð** aðgerðar í svæðinu **Aðgerð**.
    * Kynningartilboð og Aðrar gerðir aðgerða til að breyta stigi gera notendum kleift að gera handvirkar leiðréttingar á launum starfsmanns. Hægt er að virkja leiðbeiningar fyrir þessar gerðir aðgerða, eins og aðrar gerðir aðgerða til að gera það kleift að færa inn nýtt gildi ráðlögð laun fyrir starfsmanns.  
15. Smelltu á **Bæta við**.
16. Í reitnum **Tegund** skal velja valkost.
    * Hægt er að keyra fasta og breytilega launafyrirkomulag í sama launavinnsluna.  
17. Í reitinn **Áætlun** slærðu inn eða velur gildi.
    * Nota gátreið **Virkja laun fyrir frammistöðu** til að ákvarða hvort föst og breytileg launaupphæðir ætti að leiðrétta á grundvelli afkastaeinkunn starfsmanns.  
    * Hægt er að hnekkja vogun í breytilegu launafyrirkomulagi.  
18. Smelltu á **Vista**.
19. Smelltu á **Bæta við**.
20. Lokið síðunni.

## <a name="run-the-compensation-process"></a>Keyra Launavinnsla
1. Smelltu á **Keyra vinnslu**.
    * Stýringin **Sýna niðurstöður vinnslu** gerir kleift að skoða vinnsluskilaboð fyrir lokið launavinnsla þegar vinnslu er lokið.  
2. Velja skal **Já** í svæðisins **Sýna niðurstöður vinnslu**.
3. Smellt er á **OK**.

## <a name="view-the-results"></a>Skoða niðurstöður
1. Smelltu á **Niðurstöður ferlis**.
2. Smelltu á **niðurstöður starfsmaður**.
3. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
4. Stækkaðu **Fastar bætur** kafla.
    * Útvíkka flýtiflipar til að skoða niðurstöður ferlis. Ef **Virkja ráðleggingar** var merkt fyrir aðgerð launa, munu reitirnir **Ráðlegging** vera virkjað fyrir þá aðgerð.  
5. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Hægt er að skoða niðurstöður fyrir stakan starfsmann með því að smella á hnappinn **Skoða niðurstöður**.  
    * Hægt er að skrifa yfir reiknað launaupphæð með því að stilla prósentu eða upphæð aukningar í svæðunum **Ráðleggingar**.  
6. Í reitinn **Ráðlögð prósenta** skal slá inn númer.
7. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
8. Í reitinn **Ráðlögð prósenta** skal slá inn númer.
    * Endurreikna má nota til að hunsa breytingar voru gerðar á fyrirliggjandi færsla og búa til nýja niðurstaða launa fyrir valinn starfsmann.  
    * Breyta stöðu í **Samþykkt** þegar öllum breytingum er lokið fyrir starfsmann.  
9. Smelltu á **Breyta stöðu**.
10. Smellt er á **Samþykkt**.
    * Eftir að færslan hefur verið samþykkt það hægt að hlaða það í opinber launafærslu starfsmanns. Ný laun verður virkt frá og með færsludagsetningu sem stillt var í launavinnsluna.  



[!INCLUDE[footer-include](../includes/footer-banner.md)]
