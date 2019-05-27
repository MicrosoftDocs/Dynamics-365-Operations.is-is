---
title: Setja upp breytilega launaáætlun.
description: Breytileg laun snúa að óreglulegum launum starfsmanns, eins og bónusum og hlutabréfaveitingu. Þetta efnisatriði lýsir þáttum sem þarf að setja upp áður en þú getur notað breytileg laun og ráða starfsmann inn í breytilega greiðsluáætlun.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HCMCompEligibility, HcmJobFunction, HcmWorker, HRMCompPerfPlan
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 16011
ms.assetid: fc3a394e-9ac6-4f8c-9162-dc16ec22720f
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: 4097026e652a2b2cdeb9944bde45f83f49565fbb
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518273"
---
# <a name="create-variable-compensation-plans"></a>Setja upp breytilega launaáætlun.

[!include [banner](includes/banner.md)]

Breytileg laun snúa að óreglulegum launum starfsmanns, eins og bónusum og hlutabréfaveitingu. Þessari grein lýsir þáttum sem þarf að setja upp áður en þú getur notað breytileg laun og ráða starfsmann inn í breytilega greiðsluáætlun.

Útreikningur breytilegra launaupphæða fyrir starfsmennina getur byggt á nokkrum þáttum, svo°sem°frammistöðu starfsmanns, launastigi starfsmannsins og afköstum deildar.

## <a name="variable-compensation-components"></a>Efnisþættir breytilegra launa
### <a name="create-compensation-types"></a>Stofna launategundir

**Gerðir breytilegra launa**eru áskilinn þáttur. Gerðir breytilegra launa°leyfa að hægt er að lýsa gerðum breytilegra uppbóta sem fyrirtækið umbunar með. Þær gera einnig kleift að tilgreina hvort laun eru í reiðufé eða í öðru formi, svo sem í hlutabréfum.

### <a name="describe-vesting-rules"></a>Lýsing veitireglna

Fyrirtæki geta valið um að setja upp **veitireglur**. Veitireglur lýsa hvernig úthluta á breytilegri umbun yfir tíma. Til dæmis getur veitingarregla mælt fyrir um að starfsmaður fái 25 prósent af heildarlaunum hans eða hennar á hverju ári næstu fjögur árin. Veitireglur eru aðeins til upplýsingar.

## <a name="variable-compensation-plans"></a>Launafyrirkomulög breytilegra uppbóta
**Launafyrirkomulag breytilegra uppbóta** inniheldur reglur, útreikningsaðferðir og sjálfgefin gildi fyrir útreikning breytilegra uppbóta fyrir skráða starfsmenn. Þegar launafyrirkomulag breytilegra uppbóta er stofnað verður að ákvarða gerð breytilegrar uppbóta. Gerð breytilegrar uppbótar ákvarðar hvort kerfið reiknar gjaldmiðilsupphæð eða fjölda eininga sem umbun. Einnig þarf að velja útreikningsaðferð:

-   **Tímapunktur** – útreikningur á breytilegri umbun byggist á föstum launum sem starfsmaðurinn var með á tiltekinni dagsetningu. Sú dagsetning er tilgreind á vinnslutilvikinu þegar nýjar launaupphæðir eru unnar.
-   **Samsett** – upphæð umbunar er reiknuð fyrir hvern sértækan fastlaunataxta sem starfsmaðurinn var með milli upphafs- og lokadagsetningar ferlis á vinnslutilvikinu. Taxtarnir eru síðan lagðir saman til að ákvarða lokaumbunina. Til dæmis meðan á ferlinu stóð fluttist starfsmaður í aðra stöðu sem hafði annan launataxta. Í þessu tilfelli er breytilega umbunin leiðrétt fyrir lengd þess tíma sem°starfsmaður hafði hvern°launataxta.

Upphæð breytilegrar umbunar er hægt að byggja á annað hvort hlutfalli af reglulegum grunntekjum starfsmanns eða ákveðnum fjölda eininga.

-   Velja skal **Prósenta af grunni** valkost til að færa inn sjálfgefna prósentu og tilgreinið°hvort grunnurinn eigi að vera fastur launataxti starfsmannsins eða stýripunktur fyrir launastig starfsmannsins. Launastig er stillt á starf starfsmanns. Einn af tilvísunarpunktunum úr launafyrirkomulagi má stilla sem the stýripunkt á launafyrirkomulagi fastra launa. Kerfið mun nota launastig úr starfi starfsmanns og millivísa það með stýripunkti sem er skráður í launafyrirkomulag fastra launa starfsmanns til að finna stýripunkt fyrir upphæð launastigs starfsmannsins. Upphæð stýripunktsins verður svo notuð í staðinn fyrir fasta launataxta starfsmanns sem grunn fyrir umbunina.
-   Velja skal valkostinn**Fjölda eininga** til að færa inn sjálfgefinn fjölda eininga, gildi hverrar einingar og gjaldmiðil einingarvirðisins ef launafyrirkomulag er ekki-staðgreiðsluumbun (t.d. 200 einingar af birgðum sem eru metnar á 40 USD), eða einungis einingafjölda sé launafyrirkomulag staðgreiðsluumbun. Fyrir staðgreiðsluumbun fær starfsmaður tiltekinn fjölda eininga af gjaldmiðli sem notaður er fyrir launafyrirkomulag fastra launa hans (t.d. 500 einingar af 1 USD).  Beina tengslastýringu má nota til að tilgreina hvort það er bein vörpun milli gildi einingu og fjölda eininga. Þegar áætlun breytilegra uppbóta er byggð á reiðufé með því að nota fjölda eininga er þessi valkostur sjálfkrafa læstur á **Já**, og einingarvirðið er **1,0000**.

Í stillingunni **Ráðningarregla** er hægt að tilgreina hvort°allir starfsmenn eigi að fá sömu hækkun, án tillits til dagsetningarinnar sem þeir voru ráðnir (**Ráðningarregla** = **Ekkert**), eða hvort starfsmenn eigi að fá prósentu umbunar á grundvelli tímalengdar í starfi í ferlinu (**Ráðningarregla** = **Prósent**). 

**Skuldsetning** gerir kleift að leiðrétta umbun starfsmanns, á grunni afkoma í deild starfsmannsins. Afkomumælikvarðar má setja upp fyrir hverja deild á **Deildir** síða, undir **Tengt skjámynd** &gt; **Uppbót** &gt; **Afkoma**. Umbun sem starfsmenn í viðkomandi deild taka á móti fer eftir gildi svæðisins **Prósenta sem náðist af markmiði** sem tilgreinir afköst deildarinnar:

-   Ef afköst deildar eru 100 prósent, er umbun fyrir starfsmenn í þeirri deild þáttaðar eftir prósentunni sem sett er°á**Útborgun við 100%** svæðinu.
-   Ef afköst deildar eru meira en 100 prósent bætir kerfið prósentunni sem sett er á svæðinu **á 1% yfir markmiði** við prósentuna sem sett er í á svæðinu **Útborgun við 100%** þar til það gildi sem er sett í **Hæsta leyfilega útborgun** svæði hefur verið náð.
-   Ef afköst deild eru minna en 100 prósent dregur kerfið prósentuna sem sett er á svæðinu **á 1% yfir markmiði** frá prósentunni sem sett er á svæðinu **Útborgun við 100%** þar til það gildi sem er sett í á **Lægsta leyfilega útborgun** svæði hefur verið náð.

Hægt er að setja**stig vikmarka** á prósentuþröskuld, þannig að viðvörunarskilaboð birtast°ef sú skuldsetning veldur því að prósentan er utan prósentuþröskuldsins. 

Það er sjálfgefið að kerfið leitar að deildinni sem er stillt á stöðu starfsmanns. Hins vegar getur umbun fyrir suma starfsmenn verið háð afköstum margra deilda. Í þessu tilfelli er hægt að stilla mismunandi deildir og prósentu umbunar sem er úthlutað til afkasta hverrar deildar á skráningu í breytilega uppbót starfsmanns. Nánari upplýsingar, í hlutanum „Skráningu í Breytilega uppbót" hér á eftir. 

Vogun er aðeins notuð ef **Árangurstengd Laun** er valinn þegar verið er að keyra launavinnsluna. 

Flipinn **Stig hnekkingar** gerir kleift að hnekkja sjálfgefinni prósentu umbunar eða einingafjölda, byggt á launastigs starsmanns. Ef **Leyfa stig hnekkingar** er stillt á **Já** fyrir starfsmenn sem skráðir eru í launafyrirkomulagi breytilegu uppbótarinnar tekur kerfið stig úr starfi starfsmanns og leitar síðan eftir því í töflunni um stig hnekkingar til að ákvarða prósentu eða fjölda eininga fyrir það stig. Ef stig finnst ekki í töflunni um stig hnekkingar er sjálfgefin prósenta eða fjölda eininga úr **Almennt** flipanum notað. Prósentu og fjölda eininga er einnig hægt að hnekkja á innskráningu starfsmannsins í breytilegu greiðsluáætluninni.

## <a name="variable-compensation-enrollment"></a>Skráning í breytilega uppbót
### <a name="determine-who-is-eligible-for-the-plan"></a>Ákvarða hver er hæfur fyrir áætlun

Þegar er verið að skrá starfsmenn í áætlun um breytilega uppbót er fyrsta skrefið að°ákvarða hver er hæfur fyrir uppbótina sem er tilgreind í áætluninni. Ekki er hægt að úthluta áætluninni til starfsmanna nema að meta hæfni. Til að setja upp hæfni, opnið þá **Hæfnisreglur** síðuna til að stofna nýja hæfnisreglu fyrir áætlunina og skilgreinið síðan skilyrðin sem starfsmaður verður að uppfylla til að uppfylla skilyrði fyrir launafyrirkomulagið. Skilyrði geta verið takmörkuð við Deild, verkalýðsfélag, Staðsetningar (launasvæði), starf, starfshlutverk, starfstegund, og/eða launastig. Starfsmenn geta aðeins verið skráðir í launafyrirkomulag ef þeir standast **öll** skilyrðin sem eru sett á hæfnisregluna. 

**Ábending:** Hæfnisreglur ákvarða hæfni fyrir launafyrirkomulag fastra launa og°breytilegrar uppbótar. Hæfnisreglur nota°eftirfarandi svæði í vinnslu, stöðu og starfsmannafærslum til að ákvarða hvort starfsmaðurinn er hæfur fyrir launafyrirkomulag:

- Á síðunni **Starf**:
  -   **Starf** svæðið
  -   Í **Aðgerð** og **Starfstegund** svæði á flipanum **Vinnsluflokkun**
  -   Á svæðinu **Stig**í flipanum **Laun**
- Á síðunni **Stöður**: Svæðin **Deild** og **launasvæði**
- Á síðunni <strong>Starfskraftar</strong>: Upplýsingar um verkalýðsfélög sem tengjast starfskrafti undir <strong>Persónulegar upplýsingar</strong> &gt; <strong>Verkalýðsfélög</strong> í flipanum *<strong><em>Starfskraftur</em></strong>*

### <a name="enable-enrollment-for-the-variable-compensation-plan"></a>Stofna skráningu í launafyrirkomulag breytilegrar uppbótar

Á síðunni **Breytilegt launafyrirkomulag**, stilla valkostinn **Virkja innskráningu** á **Já** til að leyfa hæfum starfsmönnum að vera skráðir í áætluninni.

### <a name="enroll-the-employee"></a>Innrita starfsmanninn

Nú er hægt að skrá starfsmann inn í°breytilega greiðsluáætlun. Til að skrá starfsmann, er farið í **Starfsmenn** síðunni og velja þann starfsmann. Smellið síðan á Aðgerðasvæðinu á **Laun** &gt; **skráning í Breytilega áætlun**. 

**Ábending:** **Innskráningar** verður að stilla á **Já** í launafyrirkomulagi breytilegu uppbótarinnar. Svæðið **Áætlun** sýnir aðeins áætlanir sem starfsmaður hefur rétt á, byggt á hæfnisreglur sem eru settir upp fyrir þær áætlanir. Ef hæfnisregla er ekki stillt fyrir áætlun, verður enginn starfsmenn hæfur fyrir þá áætlun. 

Gangið úr skugga um að reiturinn **gildisdagsetning** er stillt á rétt. Ef áætlun breytilegrar uppbótar notar **Samsetta** útreikningsaðferð, þarf að hafa í huga upphafsdagsetningu innskráningar við útreikning á umbun starfsmanns. 

Hægt er að nota flipann **Hnekkja** gildum fyrir starfsmanninn. Til dæmis, ef **Ráðningarregla** er stillt á **Prósent** á áætlun, og aðra ráðningardagsetningu ætti að nota við útreikning á ráðningarprósentu starfsmannsins, er hægt að stilla ráðningardagsetningu í **dagsetning Ráðningarreglu** svæði. Einnig er hægt að hnekkja annaðhvort **Umbunarprósenta** gildi eða **Einingafjöldi** gildi tiltekins starfsmanns eftir stillingum áætlunarinnar. Þessum gildum verða áfram þættir í ráðningarreglunni, afkastastuðlum og öðrum stillingum á áætluninni. 

**Hnekkingar fyrirtækis** eru notaðar til að byggja umbun starfsmanns á afköstum einnar eða fleiri deilda. Prósenta sem er úthlutað á milli deilda ætti samanlagt að vera 100 prósent. Einnig er tekið tillit til einstaklingsframmistöðu starfsmanns. Þessar stillingar eru aðeins notaðar ef **árangurstengd Laun** er valið þegar verið er að keyra launavinnsluna.

<a name="additional-resources"></a>Frekari upplýsingar
--------

[Launafyrirkomulag](compensation-plans.md)



