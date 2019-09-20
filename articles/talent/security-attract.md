---
title: Öryggi og hlutverkastjórnun í Attract
description: Þetta efnisatriði veitir upplýsingar um öryggishlutverk í Microsoft Dynamics 365 for Talent - Attract.
author: andreabichsel
manager: AnnBe
ms.date: 03/08/2019
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
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 3f804b5f79b813cf504c3deb4a95e678c6fcbf87
ms.sourcegitcommit: 7c49475402632069685df714546770d30804af7f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/11/2019
ms.locfileid: "1739841"
---
# <a name="set-user-permissions"></a>Stilla notandaheimildir

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Talent: Attract notar öryggi sem byggir á hlutverki. Með öðrum orðum er aðgangur ekki veittur einstökum notendum, heldur öryggishlutverkum sem notendur eru úthlutað. Notandi sem er úthlutað öryggishlutverki hefur aðgang að safni réttinda sem tengjast þessu hlutverki.

Attract veitir fimm grundvallar notandahlutverk:

- Stjórnandi
- Mannauðsstjóri
- Ráðningaraðili
- Spyrill
- Skrifvarinn

Stjórnandahlutverkið er eina hlutverkið sem hefur heimild til að bæta við öðrum notendum og breyta heimildum þeirra.

- **Bæta við** - Í stjórnendamiðstöðinni á **Notendaheimildum** flipanum skaltu velja **Úthluta hlutverkum**, leita að notandanum til að bæta við og þá úthluta heimildum til notandans.
- **Breyta** - Leitaðu að notandanum eða finndu notandann á listanum og veldu síðan **Breyta** til að breyta heimildum hans.
- **Eyða** - Ef þú eyðir heimildum notandans, fjarlægir þú ekki notandann úr kerfinu. Hins vegar takmarkar þú aðgang notanda og réttindi í Attract. Til dæmis hefur Hilda verið úthlutað hlutverki mannauðsstjóra og hún er bætt við starf sem mannauðsstjóra. Ef Hilda er síðar fjarlægður úr hlutverki mannauðsstjóra, er hún áfram mannauðsstjóri starfsins og hefur enn aðgang að því starfi. Hins vegar getur hún ekki búið til önnur störf.

Eftirfarandi kaflar gefa upp lýsingu á hverju hlutverki á háu stigi. Í töflunni seinna í efnisatriðinu eru nánari upplýsingar.

> [!NOTE]
> Sumir eiginleikar eru aðeins tiltækar með Viðbót við alhliða ráðningar fyrir Attract.

## <a name="administrator"></a>Stjórnandi

Notendur sem eru úthlutað stjórnandahlutverki geta nálgast og breytt öllum gögnum í Attract. Stjórnendur geta búið til, lesið, uppfært og eytt gögnum. Þeir hafa einnig aðgang að stjórnendamiðstöðinni, þar sem þeir geta stillt á Attract-forritið og sett upp notendaupplýsingar. Við mælum með að minnsta kosti einum einstaklingi sé úthlutað stjórnandahlutverki. Sjálfgefið er að stjórnandi umhverfisins í Microsoft PowerApps sé settur sem stjórnandi í Attract. Ef þú skráðir þig fyrir tilraunaútgáfu af Attract, er stjórnandahlutverkið sjálfkrafa úthlutað þér. Eins og er, til að búa til störf skulu notendur sem hafa stjórnandahlutverk einnig hafa annaðhvort hlutverk ráðningaraðila eða hlutverk mannauðsstjóra.

## <a name="hiring-manager"></a>Mannauðsstjóri

Notendur sem eru úthlutað hlutverki mannauðsstjóra geta búið til störf og uppfært störf sem þau höfðu áður búið til. Mannauðsstjórar geta aðeins framkvæmt takmarkaðan fjölda aðgerða í starfi og á forritum sem tengjast þessu starfi. Aðeins notendur sem eru úthlutað til hlutverki mannauðsstjóra má bæta við ráðningarteymi sem ráða stjórnendur.

## <a name="recruiter-role"></a>Hlutverk ráðningaraðila

Notendur sem eru úthlutað hlutverki ráðningaraðila hafa full réttindi til að lesa, búa til, uppfæra og eyða störfum sem þau hafa búið til. Þeir hafa einnig full réttindi til að búa til, lesa, uppfæra og eyða í forritunum sem tengjast störfum sem þau eiga. Aðeins notendur sem eru úthlutað í hlutverki ráðningaraðila er hægt að bæta við ráðningarteymi sem ráðningaraðilar.

## <a name="interviewer"></a>Sá sem tekur viðtal

Allir notendur sem hafa Microsoft Azure Active Directory (Azure AD) reikninginn í fyrirtækinu geta verið bætt við ráðningarhóp sem spyrlar. Notendur sem eru úthlutað hlutverki spyrils geta skoðað upplýsingar um starf gögn um umsækjendur varðandi störf sem þeir eru á ráðningarteymi fyrir. Fyrir þá störf geta spyrlar einnig gefið ráðleggingar um ráðningu og veitt endurgjöf um umsækjendur. Hins vegar geta þeir ekki uppfært upplýsingar um starf eða umsækjanda gögn.

## <a name="read-only"></a>Skrifvarinn

Notendur sem eru úthlutað í hlutverkinu skrifvarið, hafa skrifvarinn aðgang að öllum gögnum í Attract umhverfi. Hins vegar geta þau ekki búið til eða breytt neinum gögnum.

## <a name="find-out-which-roles-you-have"></a>Finndu út hvaða hlutverk þú hefur

1.  Í Attract skal smellt á spurningarmerki (**?**) efst í hægra horni síðunnar.

2.  Smelltu á **Um**.

    Þú munt sjá hvaða hlutverk þú hefur í Attract í glugganum sem birtist:

    ![Skoða gerð á leyfi Attract](media/attract-license-types.png)
    
## <a name="delegated-roles"></a>Úthlutað hlutverk

Fyrir hvert starf sem þeir sinna á ráðningarteyminu, geta ráðningaraðilar og mannauðsstjórar tilnefnt einn eða fleiri fulltrúa fyrir sig. Hins vegar geta þau ekki tilnefnt fulltrúa fyrir annað fólk á ráðningarteyminu.

Fulltrúar hafa sömu réttindi og sá sem tilnefndi þau. Til dæmis, ef mannauðsstjórinn tilnefnir fulltrúa fyrir sig fyrir starf mun fulltrúinn hafa sömu réttindi og mannauðsstjóri fyrir það starf. Fulltrúar geta ekki fjarlægt aðra fulltrúa frá ráðningarteyminu. Þeir geta einnig ekki fjarlægt fólkið sem tilnefndi þau sem fulltrúa.

## <a name="job-details-and-actions"></a>Starfsupplýsingar og aðgerðir

Notendur sem gegna hlutverki ráðningaraðila eða mannauðsstjóra geta búið til störf. Eftirfarandi réttindi gilda um starfsupplýsingar og aðgerðir sem hægt er að taka við störf.

| Gögn eða aðgerð    | Ráðningaraðili | Mannauðsstjóri | Spyrill |
|-------------------|-----------|----------------|-------------|
| Upplýsingar um störf       | Búðu til, lesið, uppfærðu og eyða fyrir störf sem notandinn er á ráðningarteyminu fyrir | Búðu til, lesið, uppfærðu og eyða fyrir störf sem notandinn er á ráðningarteyminu fyrir | Skrifvarinn |
| Ráðningarhópur       | Búðu til, lesið, uppfærðu og eyða fyrir störf sem notandinn er á ráðningarteyminu fyrir | Búðu til, lesið, uppfærðu og eyða fyrir störf sem notandinn er á ráðningarteyminu fyrir | Skrifvarinn |
| Starfsauglýsing       | Búðu til, lesið, uppfærðu og eyða fyrir störf sem notandinn er á ráðningarteyminu fyrir | Skrifvarinn | Skrifvarinn |
| Vinna           | Búðu til, lesið, uppfærðu og eyða fyrir störf sem notandinn er á ráðningarteyminu fyrir | Búðu til, lesið, uppfærðu og eyða fyrir störf sem notandinn er á ráðningarteyminu fyrir | Skrifvarinn |
| Bæta við umsækjendum    | Bæta við umsækjendum um störf sem notandinn er í ráðningarteyminu fyrir | Bæta við umsækjendum um störf sem notandinn er í ráðningarteyminu fyrir | Ekki leyfð |
| Bæta við viðföngum     | Bæta við viðföngum fyrir störf sem notandinn er á ráðningarteyminu fyrir | Stillingarvalkostur í [uppsetningu á aðgerðum fyrir viðföng](./activities-attract.md#prospect-activity) stjórnar hvort spyrlar geti bætt við og skoðað viðföng. | Ekki leyfð |
| Virkja starf      | Virkja störf sem notandinn er á ráðningarteyminu fyrir | Virkja störf sem notandinn er á ráðningarteyminu fyrir | Ekki leyfð |
| Loka starfi         | Loka störf sem notandinn er á ráðningarteyminu fyrir | Ekki leyfð | Ekki leyfð |
| Eyða starfi        | Eyða störfum sem notandinn er á ráðningarteyminu fyrir | Aðeins ef engar umsækjendur hafa verið bættir við starfið | Ekki leyfð |
| Eyða umsækjendum | Eyða umsækjendum ef notandinn er á ráðningarteyminu | Ekki leyfð | Ekki leyfð |

## <a name="application-details-and-actions"></a>Upplýsingar um forrit og aðgerðir

Eftirfarandi réttindi gilda um vinnusértæk gögn fyrir umsækjendur og aðgerðir sem hægt er að taka á umsóknum.

| Gögn eða aðgerð          | Ráðningaraðili | Mannauðsstjóri | Spyrill |
|-------------------------|-----------|----------------|-------------|
| Umsóknarskjöl   | Búðu til, lesið, uppfærðu og eyða fyrir störf sem notandinn er á ráðningarteyminu fyrir | Búðu til, lesið, uppfærðu og eyða fyrir störf sem notandinn er á ráðningarteyminu fyrir | Skrifvarinn |
| Athugasemdir við umsókn       | Búðu til, lesið, uppfærðu og eyða fyrir störf sem notandinn er á ráðningarteyminu fyrir | Búðu til, lesið, uppfærðu og eyða fyrir störf sem notandinn er á ráðningarteyminu fyrir | Lesa eingöngu|
| Umsóknaraðgerð    | Skoða, ef notandinn er á ráðningarteyminu | Skoða, ef notandinn er á ráðningarteyminu | Skrifvarinn |
| Endurgjöf við umsókn    | Bættu við og skoðaðu alla endurgjöf ef notandinn er á ráðningarteyminu | Bættu við og skoðaðu alla endurgjöf ef notandinn er á ráðningarteyminu | Geta bætt við endurgjöf\*\* |
| Hafna umsókn      | Geti hafnað ef notandinn er á ráðningarteyminu | Ekki leyfð | Ekki leyfð |
| Ítarlegt stig           | Geti hafnað ef notandinn er á ráðningarteyminu | Geta haldið áfram ef notandinn er á ráðningarteyminu | Ekki leyfð |
| Ræsa tilboðsstjórnun | Getur byrjað tilboðsstjórnun | Það er stillingarmöguleiki á tilboðsaðgerðinni. | Ekki leyfð |


\*\* Stillingarmöguleiki í [uppsetningu á endurgjafaraðgerð](./activities-attract.md) stýrir því hvort spyrlar geta séð endurgjöf hvers annars.


## <a name="process-templates"></a>Vinna sniðmát

Eftirfarandi réttindi eiga við um sniðmát fyrir ráðningarferli. Getu teymismeðlima til að búa til og breyta sniðmát er stillt í **Stjórnun sniðmáts** í stjórnandamiðstöðinni. Ef slökkt er á stjórnun sniðmáts, geta ráðningaraðilar og mannauðsstjórar búið til og breytt eigin sniðmátum fyrir ferli. Ef stjórnun sniðmáts er slökkt, geta aðeins stjórnendur búið til og breytt sniðmátum ferlis. Í eftirfarandi töflu er gert ráð fyrir að stjórnun sniðmáts sé kveikt.

| Gögn              | Ráðningaraðili                                           | Mannauðsstjóri                                      | Spyrill |
|-------------------|-----------------------------------------------------|-----------------------------------------------------|-------------|
| Vinna sniðmát | Full réttindi fyrir sniðmát sem notandinn býr til | Full réttindi fyrir sniðmát sem notandinn býr til | Enginn aðgangur   |

## <a name="email-and-email-templates"></a>Tölvupóstur og sniðmát fyrir tölvupóst

Eftirfarandi réttindi eiga við um sniðmát fyrir tölvupóst og aðgerðir sem hægt er að taka á tölvupósti. Aðeins stjórnendur geta búið til og breytt sniðmátum fyrir tölvupóst.

| Gögn eða aðgerð     | Ráðningaraðili          | Mannauðsstjóri     | Spyrill |
|--------------------|--------------------|--------------------|-------------|
| Sniðmát fyrir tölvupóst    | Eingöngu skrifvarið   | Eingöngu skrifvarið   | Enginn aðgangur   |
| Senda tölvupóst         | Senda samkvæmt aðgerð  | Senda samkvæmt aðgerð  | Enginn aðgangur   |
| Breyta tölvupóstinnihaldi | Breyta tölvupóstinnihaldi | Breyta tölvupóstinnihaldi | Enginn aðgangur   |

## <a name="talent-pools"></a>Hæfileikasöfn

Eftirfarandi réttindi eiga við um hæfileikasöfn. Hæfileikasöfn eru aðeins sýnilegar þeim einstaklingi sem skapaði þau, nema sá einstaklingur velji að deila þeim. Umsækjendaleit má nota til að leita að umsækjenda sem ekki hafa verið bætt við nefnt hæfileikasafn.

| Gögn eða aðgerð   | Ráðningaraðili                                       | Mannauðsstjóri                                  | Spyrill |
|------------------|-------------------------------------------------|-------------------------------------------------|-------------|
| Nefnt safn       | Full réttindi fyrir söfn sem notandi skapar | Full réttindi fyrir söfn sem notandi skapar | Enginn aðgangur   |
| Deila safni       | Aðeins söfn sem notandinn býr til                | Aðeins söfn sem notandinn býr til                | Enginn aðgangur   |
| Umsækjendaleit | Full leitargeta                        | Full leitargeta                        | Enginn aðgangur   |

## <a name="candidates"></a>Umsækjendur

Umsækjendur eru fólk sem hefur verið bætt við hæfileikasafn en eru ekki tengdir starfi.

| Gögn                        | Ráðningaraðili                        | Mannauðsstjóri                   | Spyrill |
|-----------------------------|----------------------------------|----------------------------------|-------------|
| Forstillingar - upplýsingar um umsækjanda | Búðu til, lestu, uppfærðu og eyða | Búðu til, lestu, uppfærðu og eyða | Enginn aðgangur   |
| Skjöl                   | Búðu til, lestu, uppfærðu og eyða | Búðu til, lestu, uppfærðu og eyða | Enginn aðgangur   |
