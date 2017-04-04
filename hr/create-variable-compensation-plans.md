---
title: "Setja upp breytilega launaáætlun."
description: "Breytileg laun snúa að óreglulegum launum starfsmanns, eins og bónusum og hlutabréfaveitingu. Þetta efnisatriði lýsir íhluta sem þarf að setja upp áður en hægt er að nota breytilegu og innskráning starfsmanns í breytilegri greiðsluáætlun."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HCMCompEligibility, HcmJobFunction, HcmWorker, HRMCompPerfPlan
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16011
ms.assetid: fc3a394e-9ac6-4f8c-9162-dc16ec22720f
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9397e84f03ee5b340fa2aa0a64e582fc0078526e
ms.openlocfilehash: be156afa73de731e54985485b617bcbae883db3a
ms.lasthandoff: 03/31/2017


---

# <a name="create-variable-compensation-plans"></a>Setja upp breytilega launaáætlun.

Breytileg laun snúa að óreglulegum launum starfsmanns, eins og bónusum og hlutabréfaveitingu. Þessari grein lýsir þáttum sem þarf að setja upp áður en þú getur notað breytileg laun og ráða starfsmann inn í breytilega greiðsluáætlun.

Útreikningur breytilegra launaupphæða fyrir starfsmennina getur byggt á nokkrum þáttum, svo°sem°frammistöðu starfsmanns, launastigi starfsmannsins og afköstum deildar.

## <a name="variable-compensation-components"></a>Efnisþættir breytilegra launa
### <a name="create-compensation-types"></a>Stofna launategundir

**Gerðir breytilegra launa **eru áskilinn þáttur. Gerðir breytilegra launa°leyfa að hægt er að lýsa gerðum breytilegra uppbóta sem fyrirtækið umbunar með. Þær gera einnig kleift að tilgreina hvort laun eru í reiðufé eða í öðru formi, svo sem í hlutabréfum.

### <a name="describe-vesting-rules"></a>Lýsing veitireglna

Fyrirtæki geta valið um að setja upp **veitireglur**. Veitireglur lýsa hvernig breytileg umbun sé úthlutað yfir tíma. Til dæmis veitingarreglu gæti ríki sem starfsmaður fær 25 prósenta umbunar hans eða hennar samtals hvert ár fyrir fjögur næsta árs. Veitireglur eru til upplýsingar aðeins.

## <a name="variable-compensation-plans"></a>Launafyrirkomulög breytilegra uppbóta
**Launafyrirkomulag breytilegra uppbóta** inniheldur reglur, útreikningsaðferðir og sjálfgefin gildi fyrir útreikning breytilegra uppbóta fyrir skráða starfsmenn. Þegar launafyrirkomulag breytilegrar er stofnuð verður að setja breytilegrar gerðar endurgjalds. Gerð breytilegrar uppbótar ákvarðar hvort kerfið reiknar gjaldmiðilsupphæð eða fjölda eininga sem umbunar. Einnig þarf að velja útreikningsaðferð:

-   **Tímapunkt** – útreikningur á breytileg umbun byggist á fastra launa sem starfsmaðurinn á tiltekinni dagsetningu. Sú dagsetning er tilgreind á vinnslutilvikið þegar ný laun upphæðir eru unnar.
-   **Samsett** – upphæð umbunar er reiknuð fyrir hvern sértækan fastlaunataxta sem starfsmaðurinn var með milli upphafs- og lokadagsetningar ferlis á vinnslutilvikinu. Taxtarnir bætt saman til að ákvarða á lokaumbunina. Til dæmis við ferli starfsmaður flutt í aðra stöðu hafði mismunandi launataxta. Í þessu tilfelli er breytilega umbunin leiðrétt fyrir lengd þess tíma sem°starfsmaður hafði hvern°launataxta.

Upphæð breytilegrar umbunar er hægt að byggja á annað hvort hlutfalli af reglulegum grunntekjum starfsmanns eða ákveðnum fjölda eininga.

-   Velja skal **Prósenta af grunni** valkost til að færa inn sjálfgefna prósentu og tilgreinið°hvort grunnurinn eigi að vera fastur launataxti starfsmannsins eða stýripunktur fyrir launastig starfsmannsins. Launastig er stillt á starf starfsmanns. Hægt er að setja einn tilvísunarpunktar launafyrirkomulagið sem stýringin á fast launafyrirkomulag. Mun kerfið nota launastig úr starfi starfsmanns og millivísun hann með stýringu sem er skráður í launafyrirkomulag fastra launa starfsmanns til að finna upphæð þjónustustaðar fjárhagsáætlunarstýringar fyrir launastig starfsmannsins. Upphæð þjónustustaðar stýringu verður svo að nota en föstum launataxta starfsmanns sem grunn fyrir umbunina.
-   Velja skal valkostinn** Fjölda eininga** til að færa inn sjálfgefinn fjölda eininga, gildi hverrar einingar og gjaldmiðil einingarvirðisins ef launafyrirkomulag er ekki-staðgreiðsluumbun (t.d. 200 einingar af birgðum sem eru metnar á 40 USD), eða einungis einingafjölda sé launafyrirkomulag staðgreiðsluumbun. Staðgreiðsluverðlaun skal fyrir að starfsmaður fær tiltekinn fjölda eininga af gjaldmiðli sem notaður er fyrir sölumannsins launafyrirkomulag fastra launa (t.d. 500 eininga 1 USD). Beinu tengslin stýring má nota til að tilgreina hvort er bein beinu vörpun milli gildi einingu og fjölda eininga. Þegar breytilegra uppbóta fyrir áætlun byggða á reiðufé með fjölda eininga er þessi valkostur sjálfvirkt læst í **Já**, og einingarvirðið er **1,0000**.

Í **ráðningarreglu** uppsetning gerir kleift að tilgreina hvort allir starfsmenn eigi að fá sömu hækkun, dagsetninguna sem þeir voru ráðnir (**ráðningarreglu** = **Ekkert**), eða hvort starfsmenn eigi að fá prósenta umbunar á grundvelli lengdar hans í starfi við reglulega (**ráðningarreglu** = **Prósent**). 

**Vogun** gerir það mögulegt að leiðrétta umbun starfsmanns, byggt á afkastagetu starfsmanns í deild. Afkastamælikvarða er hægt að setja á fyrir hverja deild á **Deildir** síðuna undir **Tengdar skjámyndir**&gt;**Launa**&gt;**Afköst**. Umbun sem starfsmanna í deild sem taka á móti fer eftir því gildi sem **Prósenta sem náðist af markmiði** svæðið sem sýnir afköst í deild:

-   Ef afköst deildar eru 100 prósent, er umbun fyrir starfsmenn í þeirri deild þáttaðar eftir prósentunni sem sett er°á** Útborgun við 100%** svæðinu.
-   Ef afköst deildar eru meira en 100 prósent bætir kerfið prósentunni sem sett er á svæðinu **á 1% yfir markmiði** við prósentuna sem sett er í á svæðinu **Útborgun við 100%** þar til það gildi sem er sett í **Hæsta leyfilega útborgun** svæði hefur verið náð.
-   Ef afköst deild eru minna en 100 prósent dregur kerfið prósentuna sem sett er á svæðinu **á 1% yfir markmiði** frá prósentunni sem sett er á svæðinu **Útborgun við 100%** þar til það gildi sem er sett í á **Lægsta leyfilega útborgun** svæði hefur verið náð.

Hægt er að setja** stig vikmarka** á prósentuþröskuld, þannig að viðvörunarskilaboð birtast°ef sú skuldsetning veldur því að prósentan er utan prósentuþröskuldsins. 

Að sjálfgefnu sölutilboðslínu leitar kerfið deild sem er stillt á stöðu starfsmanns. Hins vegar umbun fyrir suma starfsmenn gætu háð afköst margar deildir. Í þessu tilfelli mismunandi deildir og prósenta umbunar sem er úthlutað til hverrar deildar afköst er að stilla á skráningu í breytilega uppbót starfsmanns. Nánari upplýsingar í hlutanum "skráningu í Breytilega uppbót" sem fylgir. 

Vogun er aðeins notuð ef **Árangurstengd Laun** er valinn þegar verið er að keyra launavinnsluna. 

Í **Stig hnekkingar** flipa er hægt að hnekkja sjálfgefna prósentu eða fjölda eininga sem grundvelli greiðslustigs starfsmanns skal umbun. Ef **Virkja hnekkir þrepa** er stillt á **Já** fyrir starfsmenn sem skráðir eru í launafyrirkomulagi breytilegu uppbótarinnar kerfið tekur stig úr starfi starfsmanns og síðan hnekkir eitthvað fyrir það stig í töflu til að ákvarða prósentu eða fjölda eininga fyrir það stig. Ef stig finnst ekki í stig hnekkir töflu, sjálfgefin prósenta eða fjölda eininga úr á **Almennt** flipinn er notaður. Prósenta og fjölda eininga getur einnig að hnekkja á skráningar starfsmannsins í breytilegu greiðsluáætluninni.

## <a name="variable-compensation-enrollment"></a>Skráning í breytilega uppbót
### <a name="determine-who-is-eligible-for-the-plan"></a>Ákvarða hver er hæfur fyrir áætlun

Þegar er verið að skrá starfsmenn í áætlun um breytilega uppbót er fyrsta skrefið að°ákvarða hver er hæfur fyrir uppbótina sem er tilgreind í áætluninni. Ekki er hægt að úthluta áætluninni til starfsmanna nema að meta hæfni. Til að setja upp hæfni, opnið þá **Hæfnisreglur** síðuna til að stofna nýja hæfnisreglu fyrir áætlunina og skilgreinið síðan skilyrðin sem starfsmaður verður að uppfylla til að uppfylla skilyrði fyrir launafyrirkomulagið. Skilyrði geta verið takmörkuð við Deild, verkalýðsfélag, Staðsetningar (launasvæði), starf, starfshlutverk, starfstegund, og/eða launastig. Starfsmenn geta aðeins verið skráðir í launafyrirkomulag ef þeir standast **öll** skilyrðin sem eru sett á hæfnisregluna. 

**Ábending:** Hæfnisreglur ákvarða hæfni fyrir launafyrirkomulag fastra launa og°breytilegrar uppbótar. Hæfnisreglur nota°eftirfarandi svæði í vinnslu, stöðu og starfsmannafærslum til að ákvarða hvort starfsmaðurinn er hæfur fyrir launafyrirkomulag:

-   Á síðunni **Starf**:
    -   **Starf** svæðið
    -   Í **Aðgerð** og **Starfstegund** svæði á flipanum **Vinnsluflokkun**
    -   Á svæðinu **Stig**í flipanum **Laun**
-   Á síðunni **Stöður**: Svæðin **Deild** og **launasvæði**
-   Á við **Starfsmenn** síðu: upplýsingar um verkalýðsfélög sem tengist starfsmanni undir **Persónulegar upplýsingar**&gt;**verkalýðsfélög** á í *** Starfsmanns *** flipa

### <a name="enable-enrollment-for-the-variable-compensation-plan"></a>Stofna skráningu í launafyrirkomulag breytilegrar uppbótar

Á síðunni **Breytilegt launafyrirkomulag**, stilla valkostinn **Virkja innskráningu** á **Já** til að leyfa hæfum starfsmönnum að vera skráðir í áætluninni.

### <a name="enroll-the-employee"></a>Innrita starfsmanninn

Nú er hægt að skrá starfsmann inn í°breytilega greiðsluáætlun. Til að skrá starfsmann, er farið í **Starfsmenn** síðunni og velja þann starfsmann. Smellið síðan á Aðgerðasvæðinu skal á **Launa**&gt;**skráning í Breytilega áætlun**. 

**Ábending:** **Innskráningar** verður að stilla á **Já** í launafyrirkomulagi breytilegu uppbótarinnar. Í **Áætlun** sýnir aðeins áætlanir sem starfsmaður hefur rétt fyrir byggt á hæfnisreglur sem eru settir upp fyrir þær áætlanir. Ef hæfnisreglunum er ekki stillt fyrir áætlun, verður engum starfsmenn hæfur fyrir þá áætlun. 

Gangið úr skugga um það **gildisdagsetningu** svæðis er sett upp rétt. Ef notar breytilegrar uppbótar er **Samsetta** útreikningsaðferð, upphafsdagsetningu innskráningar hugsaður við útreikning á umbun starfsmanns. 

Hægt er að nota í **Hnekkir** flipa til að hnekkja ákveðnum gildum fyrir starfsmanninn. Til dæmis, ef **ráðningarreglu** er stillt á **Prósent** í áætlun, og aðra ráðningardagsetning ætti að nota við útreikning á ráðningarprósentu starfsmannsins, er hægt að stilla dagsetningu ráðningarreglu í í **dagsetning Ráðningarreglu** svæði. Einnig er hægt að hnekkja annað hvort í **Umbunarupphæð** gildi eða **Einingafjöldi** gildi tiltekins starfsmanns eftir stillingar áætlunarinnar. Þessum gildum verða samt líkanaflokksuppsetning með ráðningarreglu afkastastuðla og aðrar stillingar á áætluninni. 

**Hnekkir** eru notaðar til að byggja umbun starfsmanns afköstum eina eða fleiri deildir. Prósenta sem er úthlutað á milli deilda ætti samanlagt 100 prósent. Einnig er tekið tillit til einstaklingsframmistöðu starfsmanns. Þessar stillingar eru aðeins notað ef **árangurstengd Laun** er valinn þegar um er að keyra launavinnsluna.

<a name="see-also"></a>Sjá einnig
--------

[Launafyrirkomulag](compensation-plans.md)


