---
title: Búðu til, samþykkja og auglýsa störf í Attract
description: Þetta umræðuefni lýsir grunnatriðum starfa í Attract. Það útskýrir einnig hvernig á að búa til starf.
author: hasrivas
manager: AnnBe
ms.date: 07/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: hasrivas
ms.search.validFrom: 2018-10-24
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 351fd03f6a27073b850729e2eef5516556292225
ms.sourcegitcommit: b24c36cdd3b6f6085447bf81cb034d13d5b081fe
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/18/2019
ms.locfileid: "1773258"
---
# <a name="create-a-job"></a>Stofna starf

[!include [banner](includes/banner.md)]

Þetta umræðuefni lýsir grunnatriðum verks í Microsoft Dynamics 365 for Talent: Attract. Það útskýrir einnig hvernig á að búa til starf.

## <a name="job-creation"></a>Starf búið til

Stjórnendur, ráðningaraðilar og mannauðsstjórar geta búið til störf. Þegar þú býrð til starf er beðið um að þú veljir hlutverk þitt í því ferli: mannauðsstjóri eða ráðningaraðili. Eftir að þú hefur valið hlutverk er beðið um að þú veljir sniðmát ferlisins. Ef þú velur **Sleppa** er sjálfgefið sniðmát notað. Nánari upplýsingar um sniðmát ferla er að finna í [Búðu til sniðmát ferlis í Attract](./process-templates-attract.md).

Starf í Attract hefur upplýsingar um starfið, ráðningarteymi, ráðningarferli, atvinnuauglýsingar og greiningar.

## <a name="job-details"></a>Upplýsingar um störf

**Upplýsingar um starfið** innihalda upplýsingar um starfsábyrgð og starfseiginleika. Reitirnir fyrir starfsheiti, starfslýsingu og vinnustað eru áskildir. Önnur svið eru valfrjáls.

Sjálfgefið er að **Fjöldi lausra starfa** reiturinn sé stilltur á **1**. Þó er hægt að breyta gildinu. Þegar tilboð hefur verið undirbúið fyrir starf, er gildi **Fjöldi lausra starfa í boði** reitsins minnkað.

Ef stöðustjórnun er kveikt í stjórnendamiðstöðinni er **Uppfæra stöður** leitin tiltæk. Þessi leit les JobPosition eininguna í Common Data Service og skilar lista yfir stöður sem hægt er að velja fyrir starfið. Ef fjöldi staða sem þú velur fer yfir fjölda lausra staða berst þér viðvörun. Þér berst einnig viðvörun ef staða er notuð fyrir mörg störf.

> [!NOTE]
> Stöðustjórnun er í boði með Viðbót við alhliða ráðningar.

Háð stillingum í tilboðsvirkni ráðningarferlisins, er hægt að nota staðarnúmer tvisvar í tilboði. Nánari upplýsingar er að finna í [Ráðningarferli](./activities-attract.md).

Attract inniheldur sjálfgefið sett af **Hæfni**. Þessi hæfni birtistt sem tillögur þegar þú skrifar. Þú getur bætt við færni með því að slá inn nýja færnistexta í reitinn og styðja síðan á færslulykilinn.

Attract inniheldur sjálfgefið sett af **Starfshlutverk**. Þú getur bætt við allt að þremur starfshlutverkum til viðbótar með því að slá inn nýtt starfshlutverk í reiknum og styðja síðan á færslulykilinn.

Attract inniheldur sjálfgefið sett af **Atvinnustarfsemi fyrirtækis**. Þú getur bætt við allt að þrenns konar atvinnustarfsemi fyrirtækis til viðbótar með því að slá inn nýja atvinnustarfsemi fyrirtækisins og styðja síðan á færslulykilinn.

## <a name="hiring-team"></a>Ráðningarhópur

**Ráðningarteymi** flipann inniheldur lista yfir einstaklinga sem taka þátt í starfi. Þegar notendur eru bættir við ráðningarteymi verða þeir að fá úthlutað hlutverki í ráðningarteyminu. Hlutverkið ákvarðar þau gögn sem notendur hafa aðgang að og tilkynningunum sem þeir fá. Hlutverkin sem hægt er að velja eru **Ráðningaraðili**, **Mannauðsstjóri**, **Fulltrúi** og **Spyrill**. Nánari upplýsingar um hlutverkaréttindi er að finna í skjalinu „Hlutverkastjórnun“. Ráðningaraðilar og mannauðsstjórar geta tilnefnt einn eða fleiri fulltrúa til starfa fyrir þeirra hönd. Nánari upplýsingar um fulltrúa, sjá [Öryggi og hlutverkastjórnun í Attract](./security-attract.md).

Ráðningarteymið er hægt að uppfæra eftir að starfið er virk.

## <a name="process"></a>Vinna

Sjálfgefin upplýsingar um ráðningarferlið byggjast á sniðmáti ferlisins sem var valið þegar starfið var búin til. Ef tiltekið sniðmát var ekki valið þá var sjálfgefið sniðmát notað. Þegar þú skilgreinir ráðningarferlið getur þú bætt við eða fjarlægt ýmis stig, nema viðfangs-, umsóknar- og tilboðsstigið. Þrátt fyrir að ekki sé hægt að fjarlægja viðfangsstigið getur það verið slökkt. Innan hvers stigs er hægt að bæta við eða fjarlægja eina eða fleiri fyrirfram skilgreinda aðgerð.

Nánari upplýsingar um aðgerð sem hægt er að bæta við ráðningarferlið er að finna í [Ráðningarferli í Attract](./activities-attract.md).

> [!NOTE]
> Ekki er hægt að uppfæra ráðningarferlið eftir að starf hefur verið virkjað.

## <a name="postings"></a>Bókanir

Eftir að starf er virkjað er hægt að auglýsa það laust. Aðeins ráðningaraðilar og stjórnendur geta auglýst laus störf. Starfið getur annaðhvort verið auglýst á Talent Careers (Microsoft Dynamics 365 for Talent starfsframasvæðinu) eða LinkedIn. Attract-teymið vinnur stöðugt í samstarfi við samantektaraðila starfatorga. Þessi listi stækkar með tímanum. Þegar starf er auglýst sem eingöngu innan fyrirtækis þurfa umsækjendur AAD-reikning til að skoða og sækja um starfið. Ef starfið er auglýst opinberlega geta umsækjendur skoðað og sótt um störf með því að nota alla valkosti sannvottunar. 

Nánari upplýsingar um auglýsingar á störfum er að finna í [Virkni starfatorga í Attract](career-site.md).

> [!NOTE]
> Auglýsing á störfum er aðeins í boði með Viðbót við alhliða ráðningar fyrir Attract.

## <a name="activate"></a>Virkja

Eftir að starf er virkjað er hægt að auglýsa það og hægt er að bæta viðföngum og umsækjendum. Möguleikinn á að bæta viðföngum við starf er stilltur í aðgerðinni fyrir viðföng í ráðningarferlinu.

> [!NOTE]
> Ekki er hægt að uppfæra ráðningarferlið eftir að starf hefur verið virkjað.

## <a name="prospects-and-applicants"></a>Horfur og umsækjendur

Möguleiki á að bæta viðföngum við starf er stilltur í [Aðgerð fyrir viðföng](./activities-attract.md#prospect-activity) í ráðningarferlinu. Þessi valkostur ætti að vera stilltur áður en þú virkjar starfið. Eftir að starf er virkjað má bæta viðföngum og umsækjendum við það.

## <a name="approvals"></a>Samþykki

Attract störf er hægt að skila inn til samþykktar. Ekki þurfa allir störf samþykki. Krafan er sett á sniðmátarstiginu. Sjálfgefið er að slökkt sé á samþykki á sniðmátinu. Til að setja upp samþykki, farðu í sniðmát ferlis og stilltu **Samþykki** reitinn í Sjálfgefið. Veldu síðan það sniðmát þegar þú býrð til starfið.

Eftir að starf er vistað getur það verið lögð fyrir samþykki. Eftirfarandi tafla sýnir stöðu skjals sem notar samþykki.

| Staða   | Ríki                                                               |
|----------|---------------------------------------------------------------------|
| Drög    | Starfið hefur verið vistað, en það hefur ekki verið sent í verkflæði. |
| Í bið  | Starfið hefur verið sent til samþykktaraðila.                            |
| Samþ. | Starfið hefur verið samþykkt, en það hefur ekki verið virkjað.            |
| Hafnað | Starfið hefur verið hafnað og það er ekki hægt að virkja það.               |
| Í gangi   | Starfið hefur verið samþykkt og virkjað.                            |

Á starfalistanum er hægt að sía stöðu á störfum.

Samþykki geta verið sendar til Microsoft Azure Active Directory (Azure AD) notandans í fyrirtækinu. Samþykkti eru send samhliða öllum þeim sem eru skráðir sem samþykktaraðilar. Allir samþykktaraðilar verða að samþykka starfið áður en það er sent áfram. Ef einn samþykktaraðili hafnar starfinu birtist staðan **Hafnað** fyrir starfið. Eftir að starf hefur verið samþykkt getur það verið virkjað.

Ef notandi breytir starfinu eftir að það er samþykkt, en ekki gert virkt, verður staða starfsins aftur að **Uppkast** og senda þarf starfið aftur inn til samþykkis. Eftir að samþykkt starf hefur verið virkjað, er hægt að breyta því.

Fólkið sem er skráð sem samþykktaraðilar mun fá tilkynningu í Attract og tölvupóst til að tilkynna þeim að þeir hafi atriði til að samþykkja.  Í tölvupóstinum geta samþykktaraðilar smellt á tengilinn til að opna starfið, yfirfarið upplýsingarnar og annaðhvort samþykkt það eða hafnað því. Eftir að staða starfsins er stillt á **Samþykkt** eða **Hafnað** fær sendandinn tilkynningu um það í Attract og hann fær sendan tölvupóst. Einnig munu samþykktaraðilar fá tölvupóstsáminningu ef þeir hafa ekki svarað samþykktarbeiðninni innan sólarhrings.

> [!NOTE]
> Hægt er að búa til sérsniðin sniðmát fyrir samþykki í tölvupósti. Frekari upplýsingar er að finna í [Búa til sniðmát fyrir tölvupóst og stýra þeim](https://docs.microsoft.com/dynamics365/unified-operations/talent/email-templates).

## <a name="create-a-job"></a>Starf stofnað

Fylgdu þessum skrefum til að búa til starf.

1. Farðu í **Störf**.
2. Veljið **Nýtt**.
3. Í **Starfsheiti** reitnum skaltu slá inn starfsheiti. Í **Hlutverk** reitnum, sláðu hlutverk þitt.
4. Í **Sniðmát** reitnum, veldu sniðmát. Einnig er hægt að velja **Sleppa**. Ef þú velur **Sleppa** er sniðmátið sem merkt er sem sjálfgefið sniðmát notað.

    Ef skjalið ætti að fara í gegnum samþykktarferli, veldu sniðmát þar sem **samþykktarferli** reiturinn er stilltur á **Sjálfgefið**.

5. Á flipanum **Upplýsingar**, sláðu inn upplýsingar um starfið. Reitirnir **Titill**, **Starfslýsing** og **Staðsetning** eru áskildir.
6. Veldu **Vista**.
7. Á **Ráðningarteymi** flipanum skaltu bæta við mannauðsstjóra, ráðningaraðila eða spyrli.
8. Veldu **Vista**.
9. Á flipanum **Ferli** skaltu bæta við eða fjarlægja stig eftir þörfum:

    - Til að bæta við stigi skaltu velja **+ Nýtt stig**.
    - Til að fjarlægja stig skaltu setja bendilinn yfir stigið til að fjarlægja og veldu síðan ruslakörfuhnappinn sem birtist.

        > [!NOTE]
        > Ekki er hægt að fjarlægja viðfangs-, umsóknar- og tilboðsstig.

10. Bæta við eða fjarlægðu aðgerð eftir þörfum:

    - Til að bæta við aðgerð skaltu draga það af listanum hægra megin á viðeigandi stig. Einnig er hægt að tvísmella á aðgerðina og velja síðan stigið til að bæta því við.
    - Til að fjarlægja aðgerð skaltu stækka aðgerðina og velja síðan ruslakörfuhnappinn á aðgerðarhausnum.

11. Veldu **Vista**.
12. Ef þú hefur valið að nota samþykktarferli skaltu fylgja þessum skrefum:

    1. Veldu **+ Bæta við samþykktaraðila** og sláðu síðan inn notanda sem hefur Azure AD reikning. Þú getur bætt við mörgum samþykktaraðilum.
    2. Veldu **Senda til samþykktaraðila**.

    **Starfsstaða** reitur starfsins er stilltur á **Í bið**. Eftir að gildi **Starfsstöðu** reitsins breytist í **Samþykkt** er hægt að virkja starfið.

13. Til að virkja starfið skaltu velja **Virkja**.
14. Til að auglýsa starf, farðu til **Starfsauglýsingar** og veldu síðan **Auglýsa núna** á síðu Talent Careers eða LinkedIn.
