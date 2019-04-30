---
title: Fundið með LinkedIn Recruiter
description: Þetta efnisatriði veitir upplýsingar um að vélnám til að fá ráðleggingar um störf og umsækjendur.
author: andreabichsel
manager: AnnBe
ms.date: 12/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 4ac7a302e5bf589beb2b560b0ff5818e90c67139
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/19/2019
ms.locfileid: "859575"
---
# <a name="sourcing-with-linkedin-recruiter"></a>Fundið með LinkedIn Recruiter
[!include[banner](../includes/banner.md)]

LinkedIn er stærsti gagnagrunnur umsækjenda í heimiog oft aðalkerfið sem ráðningaraðilar nota til að finna, hafa samskipti við og finna umsækjendur fyrir þau störf sem ráðningaraðilar vilja ráða í. LinkedIn Recruiter samþætting með Dynamics 365 for Talent: Attract gerir það auðveldara fyrir notendur að ráða og að halda gögnunum í samstillingu milli kerfanna tveggja.

> [!NOTE]
> Þú þarft viðbót við alhliða ráðningar og LinkedIn Recruiter sæti til að geta notað LinkedIn Recruiter samþættingu við Attract.

## <a name="set-up-linkedin-recruiter-with-attract"></a>Setja upp LinkedIn Recruiter með Attract 

Áður en þú getur notað LinkedIn Recruiter eiginleika þarftu að stilla samningsstig eða aðgang innan fyrirtækisins fyrir tilvikið í Attract. Til að ljúka skilgreiningarferlinu verður þú að vinna með notandanum sem er stjórnandi á LinkedIn Recruiter samningnum þínum. Ljúktu eftirfarandi skrefum til að skilgreina LinkedIn Recruiter með Attract.

1.  Skráðu þig inn í Attract sem stjórnanda og farðu í **Stjórnandastillingar**.

2.  Smelltu á **LinkedIn-samþætting** flipann í vinstri glugganum.

[![Yfirlit Attract stjórnanda til að hefja LinkedIn Recruiter-samþættingu](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)

3.  Smelltu á **Tengja** til að hefja uppsetninguna og fá leiðsögn fyrir LinkedIn innskráningu.

4.  Ef þú hefur sæti á mörgum LinkedIn samningum skaltu velja samninginn sem þú vilt tengja við Attract-kerfið. Ef þú hefur aðeins sæti á einum LinkedIn samningi, verður þetta skref ekki þörf.

5.  LinkedIn græjan mun nú hlaða inn í stjórnandastillingar þínar með lista yfir samþættingar sem sýndar eru. Fyrir neðan **Tengja kerfi ráðningaraðila**, smelltu á **Beiðni**.

[![Yfirlit Attract stjórnanda til að biðja um LinkedIn Recruiter-samþættingu](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)

6.  Eftir að samþættingin er beðið frá Attract mun hún sýna sem **Samstarfsaðili tilbúinn** og er hægt að kveikja á með **Stjórnandastillingum ráðningaraðila**. Ef þú sérð **Tilkynna samstarfsaðila** á þessari síðu skaltu bíða í nokkrar sekúndur, smelltu á **Tilkynna samstarfsaðila** og endurnýja síðan síðuna. Það ætti nú að sýna sem **Samstarfsaðili tilbúinn**.

[![Yfirlit Attract-sjórnanda til að gefa til kynna beiðnum Attract megin hefur verið lokið](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)

Til að ljúka næsta skrefi þarftu að hafa stjórnandaréttindi á LinkedIn Recruiter samningnum þínum.

7.  Skráðu þig inn á LinkedIn með því að nota stjórnandareikninginn og farðu í LinkedIn Recruiter efst til hægri. 

8. Í **Fleira** valmyndinni efst á skjánum smellirðu á **stjórnandastillingar**, og smelltu síðan á **ATS** flipann.

Attract-kerfið verður skráð með nokkrum valkostum sem hægt er að kveikja á.

9. Ef þú vilt aðeins virkja útflutning með einum smell fyrir **IN-ATS-vísirinn** og **In-ATS Profile græjuna** skaltu velja **Aðgangur að fyrirtækinu**. Ef þú vilt virkja alla aðgangseiginleika að fyrirtækinu auk InMail-ferils, athugasemdaferils og InMail-forstillingaraðgang, veldu **Aðgangur á samningsstigi**.

10. Kveiktu á viðkomandi aðgangsstigi frá LinkedIn Recruiter **Admin-ATS** stillingunum.

[![Kveikja á Attract-samþættingu úr LinkedIn Recruiter yfirliti stjórnanda](./media/EnableRSC.png)](./media/EnableRSC.png)

12. Farðu aftur í stjórnandastillingar Attract sem AttractAdmin og veldu **LinkedIn-samþættingu** flipann. Þú ættir nú að sjá LinkedIn græjurálagið sem sýnir **Virkt** með valið aðgangsstig kveikt.

[![LinkedIn Recruiter samþættingu lokið](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)

## <a name="using-linkedin-recruiter-capabilities"></a>Notkun á LinkedIn Recruiter möguleikum

Eftir að LinkedIn Recruiter möguleikar hafa verið virkjaðir af Attract-stjórnanda hafa ráðningarstjórar og ráðningaraðilar aðgang að þeim. Til að nota þessa eiginleika skaltu tengja LinkedIn reikninginn þinn fyrir neðan **Notandastillingar**. Nokkrir eiginleikar verða tiltækir eftir að bæði stjórnanda- og notendastillingar hafa verið tengdir.

### <a name="in-ats-profile-widget"></a>In-ATS forstillingargræjan

Þú getur skoðað LinkedIn forstillingar umsækjanda í Attract. LinkedIn-græjan mun sýna forstillingar umsækjanda þegar ATS upplýsingar passa við LinkedIn upplýsingar notenda.

Til að skoða forstillingu skaltu fara á forstillingar umsækjanda annaðhvort af starfi eða starfatorgi. Í forstillingum umsækjanda skaltu velja **LinkedIn** flipann og forstillingargræjan verður hlaðið. Þú getur einnig vistað umsækjandann í LinkedIn Recruiter verkefnum þínum frá þessari síðu.
1. Ef LinkedIn fann samsvörun sem byggist á netfangi eða LinkedIn-meðlimakenni (nákvæmri samsvörun) verða forstillingar umsækjanda sýndar. Notandi hefur enn möguleika á því að tengja/aftengja forstillingarnar.

2. Ef LinkedIn finnur ekki umsækjandann út frá netfangi eða meðlimakenni birtist listi yfir umsækjendur sem hugsanlega passa við nafn umsækjanda og notandinn getur valið einn af þeim og tengt forstillingarnar.  

3. Ef engin umsækjandi finnst út frá nafninu skilar LinkedIn því að leitin hafi ekki skilað neinum niðurstöðum.

### <a name="1-click-export"></a>Útflutningur með einum smell 

Á meðan leitað er að umsækjendum á LinkedIn getur þú flutt út með einum smelli umsækjandann í þau störf sem þú hefur nú þegar opnað. Ljúktu eftirfarandi skrefum fyrir útflutning með einum smelli. Áður en þú lýkur þessum skrefum skaltu ganga úr skugga um að þú sért úthlutað hlutverki mannauðsstjóra eða ráðningaraðila fyrir starfið og að starfið sé á **Viðfangs** stiginu.

1.  Búðu til starfið, úthlutaðu viðeigandi hlutverkum og virkjaðu starfið.

2.  Þegar verkið er virkjað skaltu fara í LinkedIn Recruiter.

3.  Finndu umsækjandann sem þú ert að leita að og opnaðu forstillingar hans.

4.  Notaðu leitarreitinn á tengiliðaspjaldinu, finndu starfið með starfstitlinum eða starfskenninu sem var virkjað í Attract. Ef þú finnur ekki starfið skaltu smella á **Breyta ATS** til að finna rétta tilvikið í Attract.

5. Eftir að starfið er valið skaltu smella á **Flytja út**. Umsækjandinn er nú sóttur af Attract.

6.  Farðu í Attract og opnaðu viðkomandi starf. Þú finnur umsækjandann sem þú hefur flutt út á **Viðfanga** stigi starfsins.

### <a name="in-ats-indicator"></a>In-ATS vísir 

Með því að nota LinkedIn recruiter getur þú fylgst með því hvort umsækjandi hafi sótt um önnur störf í fyrirtækinu þínu, skoðað hvar hann er á mismunandi stigum starfsumsókna og skoðað endurgjöf og athugasemdir úr Attract í LinkedIn Recruiter.

1.  Opnaðu LinkedIn Recruiter og finndu forstillingar umsækjandans sem þú leitar að.

2.  Flettu niður til að skoða **In-ATS** kafla á forstillingum umsækjanda.

3.  Þú getur notað þessa græju til að skoða allar upplýsingar um umsækjandann sem er til staðar í Attract í yfirliti LinkedIn Recruiter.

4.  Veldu **Störf og stöður** flipann til að sjá störf sem þeir eru hluti af, nýjasta stöðu og hvernig þau hafa verið að hreyfa sig að hverju starfi.

5.  Veldu flipann **endurgjöf viðtals** til að sjá endurgjöf sem spyrlar hafa lagt fram í Attract.

6.  Veldu **Athugasemdir** flipann til að sjá athugasemdir sem hafa verið teknar fyrir þennan umsækjanda í Attract.

> [!NOTE]
> Umsækjandi og umsóknargögn verða samstillt við LinkedIn Recruiter ef umsækjandi komst ekki yfir viðfangsstigið.

### <a name="inmail-history"></a>InMail saga

LinkedIn InMail-ferillinn er fáanlegur með aðgangi að samningi við LinkedIn Recruiter. Þegar það er virkt er hægt að skoða allan InMail-ferilinn þinn með umsækjanda. Þú getur líka séð hverjir aðrir í fyrirtækinu hafa skipst á InMail með umsækjanda, en þú getur ekki skoðað skilaboðin á milli þeirra.

Til að skoða InMail ferilinn skaltu fara í forstillingar umsækjanda, fara á **LinkedIn** flipann og fletta að neðst á síðunni til að skoða ferilinn. Hægt er að skoða InMail feril ef þú hefur átt í umræðum við umsækjandann. Skilaboðin frá InMail verða samstillt við Attract á nokkurra klukkutíma fresti.

### <a name="notes-history"></a>Athugasemdaferill 

LinkedIn athugasemdaferill er fáanlegur með aðgangi að samningi við LinkedIn Recruiter. Þegar það er virkt er hægt að skoða athugasemdir sem hafa verið teknar um umsækjanda með mismunandi ráðningaraðilum frá fyrirtækinu þínu.

Til að skoða athugasemdaferilinn skaltu fara í forstillingar umsækjanda, fara á **LinkedIn** flipann og fletta að neðst á síðunni til að skoða ferilinn. Þú getur skoðað allar athugasemdir um umsækjanda frá LinkedIn Recruiter.

### <a name="inmail-stub-profile"></a>InMail stutt forstilling

InMail Stutt forstilling er fáanleg með aðgangi að samningi við LinkedIn Recruiter. Ef umsækjendur samþykkja að deila LinkedIn forstillingum sínum með einhverjum notanda í fyrirtækinu þínu, getur þú fylgst með umsækjendum í Attract og ný umsækjendafærsla verður búin til fyrir hvern umsækjanda. Hægt er að skoða netfang umsækjanda ef hann er þegar til staðar í kerfinu með netfang eða hann hefur kosið að deila netfanginu með ráðningaraðilanum.

Til að skoða lista yfir umsækjendur farðu í **Hæfileikasöfn** til að sjá LinkedIn hæfileikasafn búið til af kerfinu. Þessi hæfileikasafn inniheldur lista yfir umsækjendur og stutta forstillingu þeirra sem var fengin frá LinkedIn, sem sýnir umsækjanda fornafn og eftirnafn. Tölvupóstkenni umsækjandans verður birt ef umsækjandi hafði valið að deila netfanginu sínu.
