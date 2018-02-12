---
title: "Birta pöntunartilkynningar á Sölustað"
description: "Þetta efnisatriði lýsir því hvernig hægt er að gera virkar tilkynningar á Sölustað og tilkynningarammanum, sem hægt er að víkka út til annarra aðgerða."
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailOperations, RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: retail
ms.author: ShalabhjainMSFT
ms.search.validFrom: 2017-10-30
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: ec6cb212766dd90fa9db7719a2119419ecb935c7
ms.openlocfilehash: aea36591a81f727059e37a958efa62a9ebde9d9d
ms.contentlocale: is-is
ms.lasthandoff: 12/20/2017

---

# <a name="display-notifications-in-point-of-sale"></a>Birta tilkynningar á Sölustað

Í nútíma smásalaumhverfi dagsins í dag eru verslunarstarfsmenn úthlutað ýmsum verkefnum, svo sem að aðstoða viðskiptavini, færa inn viðskipti, framkvæma birgðatalningu og taka á móti pantanir í verslun. Biðlari sölustaðarins (POS) gerir starfsmönnum kleift að gera þetta verkefni og margt fleira, allt í einu forriti. Þar sem ýmsum verkefnum þarf að framkvæma yfir daginn, gætu starfsmenn þurft að fá tilkynningu þegar eitthvað þarf að athygli þeirra. Tilkynningaramminn í POS leysir þetta vandamál með því að leyfa smásölum að stilla hlutverkatengdar tilkynningar. Með Dynamics 365 for Retail með forritsuppfærslu 5, geta þessar tilkynningar aðeins verið stilltir fyrir POS aðgerðir.

Sem stendur veitir kerfið möguleika á að birta tilkynningar fyrir pöntunaruppfyllingaraðgerð, en ramminn er hins vegar hannaður til að vera teygjanlegur, þannig að þróunaraðilar muni í framtíðinni geta skrifað tilkynningarekil fyrir hvaða aðgerð sem er og birta tilkynningarnar í POS.  

## <a name="enable-notifications-for-order-fulfillment-operations"></a>Virkja tilkynningar fyrir pöntunaruppfyllingaraðgerðir

Til að virkja tilkynningar um pöntunaruppfyllingaraðgerðir skal vísa í eftirfarandi skref:

 - Farðu á **Aðgerðir** síðuna (**Smásala** > **Uppsetning rásar** > **Uppsetning sölustaðar** > **Sölustaður** > **Aðgerðir**).
 - Leitaðu að Pöntunaruppfyllingaraðgerðinni og veldu hnappinn **Virkja tilkynningar** fyrir þessa aðgerð. Þetta bendir tilkynningarrammanum á að hlusta á rekilinn fyrir pöntunaruppfyllingaraðgerðina. Ef rekillinn er innleiddur, verður tilkynningarnar birtar á POS, annars munu tilkynningarnar ekki verða birtar fyrir þessa aðgerð.
- Farðu í POS heimildir tengdar starfsmönnum og undir flýtiflipanum **Tilkynningar**, bætið Pöntunaruppfyllingaraðgerðinni með „Birtingarröð“ sem 1. Þegar fleiri en ein tilkynning hefur verið skilgreind er birtingarröðin notuð til að raða tilkynningunni frá toppi og niður, með 1 á toppnum. Aðeins er hægt að bæta við þeim aðgerðum sem gátreiturinn **Virkja tilkynningar** hefur verið valinn fyrir. Tilkynningarnar verða einnig birtar aðeins fyrir þær aðgerðir sem hefur verið bætt við hér og aðeins birtar þeim starfsmönnum sem aðgerðunum hefur verið bætt við fyrir, fyrir samsvarandi POS heimildir. 

> [!NOTE]
> Tilkynningum getur verið hnekkt á notendastiginu með því að fara inn á skrá starfsmannsins og velja **POS heimildir** og síðan breyta tilkynningaáskrift þess notanda.

 - Farðu á **Virkniregla** síðuna (**Smásala** > **Uppsetning rásar** > **Uppsetning sölustaðar** > **Notandastillingar sölustaðar** > **Virknireglur**). Uppfærðu **Tilkynningamillibil** eiginleikann, til að stilla bilið í mínútum sem tilkynningarnar ættu að dragast. Við mælum með að setja þetta gildi í 10 mínútur til að koma í veg fyrir óþarfa samskipti við höfuðstöðvarnar. Ef tilkynningarmillibilið er stillt á „0“ verður slökkt á tilkynningum.  

 - Fara í **Smásala** > **Smásöluupplýsingatækni** > **dreifingaráætlun**. Veljið áætlun „1060-Starfsmenn“ til að samhæfa stillingar fyrir tilkynningaáskrift og smellið síðan á **Keyra nú**. Næst skal samhæfa heimildarmillibilið með því að velja „1070-grunnstilling rásar“ og smellið síðan á **Keyra nú**. 

## <a name="view-notifications-in-pos"></a>Skoða tilkynningar í POS

Eftir að ofangreindar skref er lokið, geta starfsmenn, sem tilkynningarnar eru settar upp fyrir, skoðað tilkynningarnar í POS. Til að skoða tilkynningarnar, skal smella á tilkynningatáknið á titilstiku POS. Við það birtist tilkynningamiðstöð með tilkynningunum fyrir pöntunaruppfyllingaraðgerðina. Tilkynningamiðstöðin ætti að birta eftirfarandi hópa innan pöntunaruppfyllingaraðgerðarinnar: 

- **Pantanir í bið** - Þessi hópur sýnir fjölda pantana sem eru í biðstöðu, svo sem pantanir sem þurfa að vera samþykkt af POS starfsmanni sem hefur nauðsynlegar heimildir til verslunaruppfyllingar. Ef smellt er á númerið í hópnum opnast **Pöntunaruppfylling** síðan, síuð til að birta aðeins pantanir í bið sem er úthlutað í verslunina til uppfyllingar. Ef pantanirnar eru sjálfkrafa samþykktar fyrir verslunina, þá er fjöldi þessa hóps núll.

- **Afhending í verslun** - Þessi hópur sýnir fjölda pantana sem hafa afhendingarstillinguna **Afhending** og afhendingin er áætlaður frá núgildandi verslun. Með því að smella á númerið í hópnum opnast **Pöntunaruppfylling** síðan, síuð til að birta virkar pantanir sem eru settar upp til afhendingar frá núgildandi verslun.

- **Senda frá verslun** - Þessi hópur sýnir fjölda pantana sem hafa afhendingarstillinguna **Senda** og sendingin er áætlað frá núgildandi verslun. Ef smellt er á númerið í hópnum opnast **Pöntunaruppfylling** síðan, síuð til að birta virkar pantanir sem eru settar upp til sendingar frá núgildandi verslun.

Þegar nýjar pantanir er úthlutað í búðina til uppfyllingar þá breytist tilkynningartáknið til að gefa til kynna nýjar tilkynningar og fjöldi samsvarandi hópa verður uppfærður. Notandinn getur einnig smellt á endurhleðslutáknið, við hliðina á heiti aðgerðarinnar, til að uppfæra fjölda hópanna strax. Fjöldinn verður einnig uppfærður á fyrirfram ákveðnu millibili. Allir hópar sem hafa nýtt atriði, sem ekki er séð af núverandi starfsmanni, munu sýna sprengitákn sem gefur til kynna að þessi hópur sé með nýtt atriði. Ef smellt er á reitina innan tilkynninga opnast sú tiltekna aðgerð sem tilkynningin er skilgreind fyrir. Í ofangreindum atriðum, með því að smella á tilkynningarnar opnarðu **Pöntunaruppfylling** síðuna og ferð í gegnum viðeigandi breytur: Pantanir í bið, afhending í verslun og sending frá verslun. 

> [!NOTE]
> Tilkynningar fyrir pantanir í bið verða virkjaðar í væntanlegri uppfærslu af Dynamics 365 for Retail. 


