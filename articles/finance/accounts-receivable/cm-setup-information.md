---
title: Uppsetning á lánastýringu
description: Þetta efni lýsir uppsetningunni sem krafist er fyrir lánamálastjórnun.
author: mikefalkner
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 640d81920dad391a77b58942972660b01f11b003
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830641"
---
# <a name="credit-management-setup"></a>Uppsetning á lánastýringu 

[!include [banner](../includes/banner.md)]

## <a name="credit-management-workflows"></a>Verkflæði lánastýringar

Fara til **Skuldir og innheimta \> Uppsetning \> Verkflæði lánaumsýslu** til að skilgreina verkflæði sem eru notuð til að stjórna leiðréttingum á lánamörkum.

- Þú getur búið til verkflæði sem gerir þér kleift að samþykkja runu af leiðréttingum á lánamörkum með einu samþykki.
- Þú getur bætt við verkflæði á línustigi, svo að hægt sé að samþykkja leiðréttingar á lánamörkum hver fyrir sig.
- Þú getur búið til verkflæði sem beinir biðum sjálfkrafa að verkflæðisferli.

## <a name="blocking-rules"></a>Lokunarreglur

### <a name="ranking-payment-terms"></a>Greiðsluskilmálar röðunar

Þú getur sett sölupöntun í bið ef greiðsluskilmálar pöntunarinnar passa ekki við sjálfgefna greiðsluskilmála viðskiptavinarins. Hins vegar eru greiðsluskilmálar stundum ólíkir en eru nógu líkir til að þú viljir ekki setja pöntunina í bið. Þú getur raðað greiðsluskilmálum þannig að sumir þeirra séu með sömu stöðu en aðrir hærri eða lægri.

Ef röðun greiðsluskilmála er virk og ef greiðsluskilmálar pöntunarinnar eru hærri en sjálfgefnir greiðsluskilmálar viðskiptavinarins verður sölupöntunin sett í bið.

Til að setja röðun greiðsluskilmála ferðu á **Skuldir og innheimta \> Uppsetning \> Uppsetning lánamála \>Raða greiðsluskilmálum**  

### <a name="ranking-settlement-discounts"></a>Röðun uppgjörsafsláttar

Þú getur sett sölupöntun í bið ef staðgreiðsluafsláttur pöntunarinnar passar ekki við sjálfgefinn staðgreiðsluafslátt viðskiptavinarins. Hins vegar er staðgreiðsluafsláttur stundum ólíkur en nógu líkur til að þú viljir ekki setja pöntunina í bið. Þú getur raðað staðgreiðsluafsláttum þannig að sumir þeirra séu með sömu stöðu en aðrir hærri eða lægri.

Ef röðun uppgjörsafsláttar er virk og ef staðgreiðsluafsláttur pöntunarinnar er hærri en sjálfgefnir staðgreiðsluafsláttur viðskiptavinarins verður sölupöntunin sett í bið.

Til að setja röðun greiðsluskilmála ferðu á **Skuldir og innheimta \> Uppsetning \> Uppsetning lánamála \>Flokka uppgjörsafslætti**  

## <a name="reasons"></a>Ástæður

Margvíslegar ástæður eru notaðar í lánamálum:

- Ástæður bið eru af hverju sölupöntun var sett í bið.
- Sleppingarástæðum er úthlutað til pöntunar þegar henni er sleppt úr bið.
- Stöðuástæður segja til um hvers vegna lykilstöðu var úthlutað til viðskiptavinar.

Þú getur sett upp ástæður á síðunni **Ástæður lánaumsýslu** (**Skuldir og innheimta \> Uppsetning \> Uppsetning lánastjórnunar \> Ástæður lánaumsýslu**).

1. Í reitnum **Ástæðugerð** velurðu gerð ástæðunnar: **Bið**, **Losun** eða **Staða**.
2. Í svæðið **Ástæða** er fært inn nafn fyrir ástæðuna.
3. Í reitnum **Lýsing** skal slá inn lýsingu á ástæðukóðanum.

## <a name="credit-management-groups"></a>Lánastýringarflokkar

Lánastjórnunarhópar eru notaðir til að bera kennsl á viðskiptavini eða hópa viðskiptavina sem hafa sömu lánstrausteiginleika. Til dæmis er hægt að nota lánastjórnunarhópa til að ákvarða reglur um útilokun og útilokun lána fyrir viðskiptavini.

Þú getur stofnað kreditstjórnunarhópa á síðunni **Kreditstjórnunarhópar** (**Skuldir og innheimta \> Uppsetning> Uppsetning á lánastýringu \> Lánastýringarflokkar**).

1. Veldu **Nýtt** til að búa til nýja línu.
2. Færið inn kenni fyrir hópinn. Kennið getur haft allt að 10 stafi.
3. Í reitinn **Lýsing** skal færa inn heiti á hópnum. Heitið getur haft allt að 60 stafi.

Kreditstjórnunarhópurinn er úthlutaður á viðskiptavin á flýtiflipanum **Skuldir og innheimta** af síðunni **Allir viðskiptavinir** (**Viðskiptakröfur \> Viðskiptavinir \> Allir viðskiptavinir**).

## <a name="account-statuses"></a>Stöður reikninga

Þú getur búið til stöðu reikninga til að bera kennsl á lánstraust viðskiptavinarreiknings. Þú getur skilgreint stöðu og áhrif hennar á reikninga og afhendingar í biðferlum. Einnig er hægt að nota stöðu reikninga til að ákvarða útilokunarreglur fyrir viðskiptavin.

Þú getur búið til stöðu reikninga á síðunni **Lykilstöður** (**Skuldir og innheimta \> Uppsetning> Uppsetning á lánastýringu \> Lykilstöður**).

1. Bættu við stöðu reiknings og sláðu inn lýsingu sem táknar lánstraust viðskiptavinar. Notaðu til dæmis **Venjulegt** til að gefa til kynna að viðskiptavinur sé í góðu ástandi og opnar pantanir eru háðar stöðluðu vinnslu lánamála.
2. Í reitunum **Reikningsfærsla** og **Afhending í bið** velurðu þá tegund bið sem ætti að eiga sér stað fyrir viðskiptavini sem hafa þessa reikningsstöðu. Þú getur haldið allri vinnslu, haldið aðeins á reikningsvinnslu eða ekki haft neina vinnslu þegar lánamörkunarreglunum er beitt.

## <a name="scoring-groups"></a>Einkunnaflokkar

Þú getur sett upp stigahópa til að skilgreina áhættuþætti og viðmið sem eru notuð til að mæla þá. Þegar upplýsingum um viðskiptavin er beitt á stigahóp er stig reiknað fyrir hvern áhættuþátt og notaður til að setja viðskiptavininn í áhættuhóp. Hægt er að nota áhættuhópinn til að bera kennsl á lánstraust og reikna sjálfvirk lánamörk.

Þú getur búið til stigahópa á síðunni **Stigahópar** (**Skuldir og innheimta \> Uppsetning \> Uppsetning á lánastýringu \> Áhætta \> Stigahópar**).

1. Stofnaðu stigahóp og skráðu heiti fyrir hann.
2. Sláðu inn lýsingu til að lýsa stigahópnum frekar.
3. Veldu hópgerð. Það eru átta fyrirframskilgreindar gerðir. Þú getur líka valið **Notandaskilgreint** til að skilgreina hópgerð sem hentar betur fyrirtækinu þínu.
4. Veldu stigagjöf til að skilgreina hvernig stigahópurinn reiknar út áhættustigið. Eftirtaldir valkostir eru í boði:

    - **Svið** - Notaðu þennan valkost til að skilgreina svið gildi sem ætti að nota til að reikna stig.
    - **Notandaskilgreint** - Notaðu þennan valkost til að skilgreina handvirkt lista yfir gildi sem ætti að nota fyrir stigagjöfina.

5. Ef þú valdir **Svið** sem stigagjöf, bættu við línum til að skilgreina gildissviðið og samsvarandi stig.

    1. Í reitnum **Frá gildi** tilgreindu lægsta gildi á sviðinu.
    2. Í reitnum **Til gildis** tilgreindu hæsta gildi á sviðinu.
    3. Í reitinn **Stig** sláðu inn stig sem ætti að vera úthlutað þegar gildið sem er gefið er í sviðinu "frá" / "til".

    Ef þú valdir **Notendaskilgreint** sem stigagjöf, bættu við línum til að skilgreina notendaskilgreind gildi og samsvarandi stig.

    1. Í reitnum **Gildi** sláðu inn notendaskilgreint gildi sem ætti að vera veitt frá upplýsingum viðskiptavinarins.
    2. Í reitinn **Stig** sláðu inn stig sem ætti að vera úthlutað þegar gildið sem er gefið er í sviðinu "frá" / "til".

## <a name="risk-classification"></a>Áhættuflokkun

Þú getur skilgreint áhættumat sem hægt er að úthluta viðskiptavinum, út frá áhættustiginu. Áhættustig er reiknað með því að bera saman upplýsingar viðskiptavina við hvern stigahóp. Stigin eru dregin saman og heildarstigið er borið saman við gildin í uppstillingu áhættuhópsins til að bera kennsl á áhættuhópinn sem viðskiptavinurinn tilheyrir. Stig áhættuhópsins er síðan notað til að skilgreina útilokunar- og útilokunarreglur fyrir lánastjórnun fyrir viðskiptavininn.

Þú getur sett upp áhættuhópa á síðunni **Áhættumat** (**Skuldir og innheimta \> Uppsetning \> Uppsetning á lánastýringu \> Áhætta \> Áhættuflokkun**).

1. Sláðu inn auðkenni áhættuhóps.
2. Sláðu inn lýsingu til að útskýrir áhættuhópinn frekar.
3. Sláðu inn svið skora sem er notað til að ákvarða hvaða viðskiptavinir tilheyra áhættuhópnum.
4. Veldu áhættuhóp til að tilgreina táknið sem táknar áhættuhópinn.

## <a name="guaranteeinsurance-types"></a>Gerðir ábyrgða/trygginga

Þú getur sett upp gerðir ábyrgða/trygginga á síðunni **Gerðir ábyrgða/trygginga** (**Skuldir og innheimta \> Uppsetning \> Uppsetning á lánastýringu \> Trygging og ábyrgðir \> Gerðir tryggingar og ábyrgðar**).

1. Sláðu inn ábyrgð eða tryggingategund sem auðkennir nafn ábyrgðaraðila eða vátryggingamiðlara.
2. Sláðu inn lýsingu til að lýsa ábyrgðarmanni / vátryggingamiðlara.

## <a name="coverage-types"></a>Tegundir trygginga

Hægt er að nota umfjöllunargerðir til að flokka tryggingar frekar. Þeir geta ekki verið notaðir með ábyrgðir.

Þú getur bætt við vátryggingagerðum á síðunni **Gerðir vátrygginga** (**Skuldir og innheimta \> Uppsetning \> Uppsetning á lánastýringu \> Trygging og ábyrgðir \> Gerðir vátrygginga**).

1. Sláðu inn gerð vátryggingar til að bera kennsl á gerð vátryggingar sem ætti að bæta við sem tryggingu eða ábyrgð.
2. Færa inn lýsingu til að lýsa gerð vátryggingar.

## <a name="automatic-credit-limits"></a>Sjálfvirk lánamörk

Þú getur búið til viðmið fyrir sjálfvirk lánamörk á síðunni **Sjálfvirk lánamörk** (**Skuldir og innheimta \> Uppsetning \> Uppsetning á lánastýringu \> Áhætta \> Sjálfvirk lánamörk**).

1. Veldu áhættuhóp sem sjálfvirka lánsfjárhæðinni skal úthlutað til.
2. Veldu gjaldmiðil fyrir sjálfvirka lánamörk. Þú getur búið til mörg sjálfvirk lánamörk í mismunandi gjaldmiðlum fyrir sama áhættuhóp.
3. Sláðu inn tekjuupphæðina sem táknar hámarks tekjur fyrirtækisins sem hægt er að nota fyrir þetta sjálfvirka lánamörk. Þegar lánamörk eru búin til er tekjufjárhæðin borin saman við tekjuvirði sem er að finna á síðunni **Fjármál** (**Viðskiptakröfur \> Allir viðskiptavinir \> Veldu viðskiptavin \> Almennt \> Talnagögn \> Fjármál**). Kerfið notar nýjasta gildi í kaflanum **Yfirlit**.

Fylgdu þessum skrefum til að bæta við línum sem tákna lánamörk sem verða til miðað við valin viðmið.

1. Veldu stigahópinn sem skilgreinir viðskiptavinaupplýsingarnar sem ætti að nota til að reikna út lánamörkin.
2. Veldu samanburðarstjórann sem skilgreinir hvernig meta skal upplýsingar um stigahópinn.
3. Sláðu inn gildi sem ber að bera saman við gildi sem er tilgreint fyrir stigahópinn.
4. Sláðu inn lánsfjárhæðina sem ætti að vera úthlutað ef viðskiptavinaupplýsingin samsvarar gildinu sem er tilgreint fyrir stigahópinn. Til dæmis stofnarðu sjálfvirka lánamörk fyrir stigahópinn **Lágt**. Ef árin í viðskiptum eru einn af stigahópunum geturðu skilgreint eina línu sem úthlutar 100.000 lánamörkum ef viðskiptavinurinn hefur verið í viðskiptum í fimm ár og önnur lína sem úthlutar 200.000 kreditmörkum ef viðskiptavinurinn hefur verið í viðskiptum í 10 ár.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]