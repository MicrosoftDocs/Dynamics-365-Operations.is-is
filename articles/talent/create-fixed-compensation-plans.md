---
title: Stofna launafyrirkomulag fastra launa
description: "Föst laun vísa til reglubundinna vergra launa eða greiðslna til starfsmanns. Þessari grein lýsir þáttum sem þarf að setja upp áður en þú getur stofnað launafyrirkomulag fastra launa og ráða starfsmenn."
author: kherr75
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HRCCompGrid, HRCCompRefPointSetup, HRMCompEligibility, HRMCompEvent, HRMFixedCompPlanTable
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 15991
ms.assetid: ef8cf992-176c-4c98-9dff-6510e1eb9f1c
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f84caa64f4583df97817f8ee8dcdf7e0591b857c
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="create-fixed-compensation-plans"></a>Stofna launafyrirkomulag fastra launa

[!include[banner](includes/banner.md)]


Föst laun vísa til reglubundinna vergra launa eða greiðslna til starfsmanns. Þetta efnisatriði lýsir þáttum sem þarf að setja upp áður en þú getur stofnað launafyrirkomulag fastra launa og ráða starfsmenn.

Hægt er að reikna upphæðir fastra°launa fyrir starfsmenn, á grundvelli þátta eins og afköst, svæði og aukningu fjárhagsáætlunar. Microsoft Talent styður skref, launaþrep og greiningartímabil launa.

## <a name="fixed-compensation-components"></a>Fastir launaþættir
### <a name="compensation-levels"></a>Launastig

Hægt er að nota **launastig** til að setja inn laun fyrir mismunandi störf, til að tryggja að starfsmenn sem sinna þeim störfum fái sanngjörn laun. Á **launastig** síðu er hægt að setja upp launastig sem krafist er fyrir hvert skref, launaþrep og greiningaráætlun. Nota skal **Upp** og **Niður** hnappana til að setja stig í réttri röð,°eftir gerð þeirra. Með því að stilla launastig á°starf, hjálpar það til við tryggja að allir starfsmenn í°því starfi fái greitt á sama stigi.

### <a name="reference-points"></a>Tilvísunarpunktar

**Tilvísunarpunktar** eru dálkar í hnitanetinu sem skilgreina launasvið fyrir°hvert stig. Launastig er línan í hnitanetinu. Dæmigerðir tilvísunarpunktar fyrir áætlun um gerð launaþrepa eru lágmark, miðpunktur og hámark. Tilvísunarpunktar eru stofnaðir á síðunni **Uppsetning tilvísunarpunkta**.

### <a name="compensation-grids"></a>Launanet

Eftir að búið er að setja upp stig og tilvísunarpunkta er hægt að sameina°það til að búa til **launanet**. Á **launanet** síðunni, tilgreinið upplýsingar um hnitanetið. Til dæmis er hægt að tilgreina fyrir hvað hnitanetið er hannað, hvaða gerð áætlunar það verði notað við og hvaða tilvísunarpunkta eða dálka sé krafist í hnitanetinu. Eftir að lokið hefur verið við að færa inn þær upplýsingar skal smella á **launaskipulag** til að bæta stigum og upphæðum við hnitanetið. 

**Ábending:** Notið **Fjöldabreytingar** aðgerð á launaskipulagi til að setja upphaflegar upphæðir, og síðan°þrepaaukning eftir upphæðir eða prósentur milli stiga eða tilvísunarpunkta.

### <a name="pay-frequencies"></a>Greiðslutíðni

**Greiðslutíðni** er notuð til að skilgreina hvernig laun eða greiðslur starfsmanns hafa verið tilgreind (t.d. $10 á klukkustund°eða°$50.000 á ári), og umreikning milli tímakaups, vikukaups, mánaðarlauna (12 mánuðir) og árslauna. Til dæmis fyrirtæki sem notar 38 klukkustund vinnuviku fyrir starfsmenn á tímakaupi setur upp greiðslutíðni sem hefur tímakaupið 1, vikukaupið 38, mánaðarleg hlutfall 164,6666666667 og árlegt hlutfall 1,976. Þessi umreikningur eru notaður til að reikna út ýmsa launataxta sem birtast á fastlaunaskrá starfsmanns.

## <a name="fixed-compensation-plans"></a>Launafyrirkomulög fastra launa
Hægt er að hanna launafyrirkomulag fastra launa til að sameina alla uppsetta þætti sem hafa verið skilgreindir. Til að stofna fasta launaáætlun, opnið skjámyndina **Föst launaáætlun**. Hér er hægt að gefa áætluninni heiti og lýsingu, veljið af hvaða gerð áætlunin er (skref, stigi eða braut), veljið greiðslutíðni sem verður að nota fyrir starfsmanns launataxti (upphæð á klukkustund, upphæð á ári og svo framvegis) og setja upp valkosti sem stýra því hvernig laun eru unnin. 

Í stillingunni **Vikmörk utan marka** er gert kleift að tilgreina hvernig strangur á að vera varðandi að sannreyna að upphæðir launa séu á milli lágmarks- og hámarks upphæðir. **Hörð** vikmörk krefst þess að laun séu á bilinu sem er skilgreint°fyrir tiltekið stig. **Mjúk** vikmörk gefa viðvaranir þegar launafjárhæðin er utan marka en gerir þér þó kleift að halda áfram. Ef vikmörkin eru stillt á **Ekkert**, er hægt að færa inn hvaða upphæð launa sem er fyrir starfsmann án þess að taka á móti villuskilaboðum eða viðvörunum. 

Í stillingunni **Ráðningarregla** er gert kleift að tilgreina hvort allir starfsmenn eigi að fá sömu hækkun, án tillits til dagsetningarinnar sem þeir voru ráðnir (**Ráðningarregla** = **Ekkert**), eða hvort starfsmenn eigi að fá prósentu umbunar á grundvelli þess hversu lengi þeir voru í starfi á tímabilinu (**Ráðningarregla** = **Prósent**). 

°**Nýtingarfylki sviðs** er gagnlegt ef annað hvort er óskað eftir að minnka tímann sem krafist er fyrir starfsmenn til að ná miðpunkti sviðsins eða auka tímann sem krafist er fyrir starfsmenn til að ná hámarks viðmiðunarpunkti sviðsins. Til dæmis, ef óskað er að gefa starfsmönnum sem eru í neðstu 25 prósentum síns sviðs 110 prósent°af markverðlaunum þeirra, en veita starfsmönnum sem eru í efstu 25 prósentum°síns sviðs aðeins 80 prósent af þeirra markverðlaunum til að koma í veg fyrir að þeir nái hámarki eins hratt. 

Þegar búið er að skilgreina grunnatriði fasts launafyrirkomulags, er hægt að setja upp launaskipulag fyrir fyrirkomulagið. Smellt er á **Setja upp laun**. Svargluggasleði opnast sem gefur þrjá valkosti:

-   Búa til nýtt launanet með því að velja uppsetningu tilvísunarpunkts og gefa hnitanetinu nafn.
-   Búa til nýtt launanet með því að búa til afrit af fyrirliggjandi hnitaneti sem hægt er að nota°sem upphafspunkt.
-   Nota fyrirliggjandi launanet sem þegar hefur verið skilgreint. Allt launafyrirkomulag sem notar sama hnitanet fær uppfærslur ef því hnitaneti er breytt.

Þegar valkostur er valinn, opnast°síðan **Launaskipulag** og hægt er að gera breytingar á nýju launaneti eða fyrirliggjandi launaneti.

## <a name="fixed-compensation-enrollment"></a>Skráning í föst laun
### <a name="determine-who-is-eligible-for-the-plan"></a>Ákvarða hver er hæfur fyrir áætlun

Þegar er verið að skrá starfsmenn í áætlun um föst laun er fyrsta skrefið að ákvarða hver er hæfur fyrir launin sem eru tilgreind í°áætluninni. Ekki er hægt er að úthluta áætluninni á starfsmenn nema að meta hæfni. Til að setja upp hæfni skal opna síðuna **Hæfnisreglur**. Þar er hægt að stofna nýja hæfnisreglu fyrir launaáætluninni og skilgreina síðan skilyrðin sem starfsmaður verður að uppfylla til að falla undir skilyrði fyrir launafyrirkomulagið. Skilyrði geta verið Deild, verkalýðsfélag, Staðsetningar (launasvæði), starf, starfshlutverk, vinnslugerð, eða launastig. Starfsmenn geta aðeins verið skráðir í launafyrirkomulag ef þeir uppfylla öll skilyrðin sem eru sett á hæfnisregluna. 

**Ábending:** Hæfnisreglur ákvarða hæfni fyrir launafyrirkomulag fastra launa og breytilegrar uppbótar. 

Hæfnisreglur meta gildi sértækra svæða í starfinu, stöðunni og starfsmannaskrám til að ákvarða hvort starfsmaðurinn er hæfur fyrir launafyrirkomulag.

-   Á **Starf** síðunni tekur hæfnisreglan til eftirfarandi svæða:
    -   **Starf** svæðið
    -   Í flipanum **Starfsflokkun**, **Aðgerð** og **Starfstegund** svæðin
    -   Á flipanum **Laun**, °**Stig** svæðið
-   Á síðunni **Stöður** tekur hæfnisreglan tillit til svæðanna **Deild** og **Launasvæði**.

Hæfnisreglan tekur einnig tillit til verkalýðsfélaga sem tengjast starfsmanninum (á síðunni **Starfsmenn**, í flipanum **Starfskraftur**, smellið á **Persónuupplýsingar** &gt; **Verkalýðsfélög**).

### <a name="define-fixed-compensation-actions"></a>Skilgreina aðgerðir fastra launa

**Fastlaunaaðgerðir** eru notaðar þegar stillt er eða breytt uppsetningu fastra launa starfsmanns. Fastlaunaaðgerðir gefa færi á að veita lýsandi heiti fyrir tegundir aðgerða sem stjórnandi launa og fríðinda getur framkvæmt. Mismunandi tegundir aðgerða hafa sérstök rök á bak við sig,°svo þær megi nota á tilteknum tímum. 

Til dæmis þegar föst laun eru sett upp fyrir starfsmann, er aðeins hægt að nota aðgerðir sem eru með gerðina **Ráða/Endurráða**. Í þessu tilfelli, gæti verið hægt að stofna°þrjár°aðgerðir af **Ráða/Endurráða** gerð og kalla þær **Ráða**, **Endurráða**, og **Flytja**. Síðan hefurðu lýsandi útskýringu á því hvers vegna föst launin voru gefin til starfsmanns eða þeim breytt.

### <a name="enroll-the-employee"></a>Innrita starfsmanninn

Nú er hægt að tengja starfsmann við launafyrirkomulag fastra launa. Opna skal síðuna **Starfsmenn** og veljið starfsmann til að skrá í launafyrirkomulaginu. Smellið á **Bætur** &gt; **Föst áætlun** á aðgerðarúðunni. Nú er hægt að stofna nýja aðgerð fastra launa fyrir þann starfsmann. 

**Ábending:** Svæðið Launaáætlun sýnir aðeins°áætlanir sem starfsmaður er hæfur fyrir undir hæfnisreglum sem settar voru upp fyrir hverja áætlun. Ef engin hæfnisregla er sett upp fyrir áætlun verður engin starfsmaður hæfur fyrir þá áætlun. 

Kerfið°staðfestir launafjárhæðina sem tilgreind er í launafyrirkomulagi af því stigi eða braut°sem er innan lágmarks- og hámarkspunkta fyrir tiltekið launastig starfs viðkomandi starfsmanns. Ef laun eru utan leyfilegra marka,°munu viðvörun°eða villuboð birtast , eftir því vikmarkastigi sem fasta launafyrirkomulagið er stillt á.

<a name="see-also"></a>Sjá einnig
--------

[Launafyrirkomulag](compensation-plans.md)




