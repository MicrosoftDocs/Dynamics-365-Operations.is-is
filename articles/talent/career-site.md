---
title: Virkni starfatorgs í Attract
description: Þessi efnisatriði veitir yfirlit yfir starfatorg sem snýr að umsækjendum í Attract.
author: hasrivas
manager: AnnBe
ms.date: 03/20/2019
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
ms.author: hasrivas
ms.search.validFrom: 2019-02-12
ms.dyn365.ops.version: AX 7.1.0, Talent April 2018 update
ms.openlocfilehash: e51fb00536884d2b3815c05a0968714d8b9326f2
ms.sourcegitcommit: a6b32be10b6eb6340f8f68261bf62d0202c03dd1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/05/2019
ms.locfileid: "1729704"
---
# <a name="career-site-functionality-in-attract"></a>Virkni starfatorgs í Attract

[!include[banner](../includes/banner.md)]

Þetta efnisatriði veitir yfirlit um starfatorg sem snýr að umsækjendum í Microsoft Dynamics 365 for Talent: Attract. Það útskýrir einnig hvernig á að setja upp þessa virkni.

Attract býður upp á eitt starfatorg fyrir hvert umhverfi í leigjanda. Til dæmis, ef fyrirtæki hefur þróunarumhverfi og prófunarumhverfi er eitt starfatorg búð til fyrir þróunarumhverfið og annað starfatorg búið til fyrir prófunarumhverfið. Hvert starfatorg er fullkomlega einangrað og hefur eigið sannvottunarkerfi. Störf og síðum umsækjenda er ekki deilt á milli starfatorga.

Sjálfgefið er að starfatorgið sé opinbert. Þar af leiðandi geta umsækjendur skoðað öll störf sem eru merkt sem ytri án þess að þurfa að skrá sig inn. Hins vegar kalla allar aðrar aðgerðir á að umsækjendur skrái sig inn.

## <a name="career-site-management"></a>Stjórnun ferilssíðu

Til að stilla gildin fyrir eftirfarandi atriði, skráðu þig inn í Attract sem stjórnandi, veldu **Stjórnendamiðstöð** á **Stillingar** valmyndinni (gírtáknið) og veldu síðan flipann **Fyrirtækisupplýsingar**.

-   **Heiti fyrirtækisins** - Heiti fyrirtækisins birtist á yfirlitsstikunni efst á starfatorginu. Með því að velja heiti fyrirtækisins, fara umsækjendur á síðu sem sýnir alla opna störf.

-   **Merki fyrirtækisins** - Mynd af merki fyrirtækisins birtist efst til vinstri á starfatorginu. Með því að velja merkið fara umsækjendur á síðu sem sýnir alla opna störf.

    > [!NOTE] 
    > Merkið sem birtist á starfatorginu hefur fastsetta hæð sem nemur 20 pixlum (px). Myndin sem þú bætir við í stjórnendamiðstöðinni er minnkuð til að passa. Þess vegna getur breiddin breyst, allt eftir myndinni.
 
Til að stilla gildin fyrir eftirfarandi atriði, skráðu þig inn í Attract sem stjórnandi, veldu **Stjórnendamiðstöð** á **Stillingar** valmyndinni og veldu síðan flipann **Starfatorg umsækjanda**.

-   **Leitarvélabestun** - Ef virkt verður hægt að leita að öllum almennum störfum sem birtast í starfatorgi Attract þegar leitarvélar eins og Bing og Google eru notaðar. 

    > [!NOTE] 
    > Það gæti orðið tafir á milli þess að kveikja á þessari stillingu og leitarniðurstöður birtast, fer allt eftir leitarvélinni sem þú notar.
    
-   **Skilmálar og skilyrði** - Þegar þetta er virkt verða allir umsækjendur að samþykkja skilmála og skilyrði fyrirtækisins þegar sótt er um starf. Kerfisstjóri Attract getur skilgreint eigin samþykkistexta ásamt tengli á skilmálasíðuna. 

        
## <a name="career-site-urls"></a>Vefslóðir starfatorgs

Eftirfarandi listi inniheldur algengar vefslóðir starfatorga og hvernig skuli nálgast þau.

-   **Vefslóð á heimasíðu starfatorgs** - Til að sjá vefslóð á heimasíðu starfatorgs skaltu skrá þig inn í Attract sem stjórnandi, veldu **Stjórnendamiðstöð** á **Stillingar** valmyndinni og veldu síðan flipann **Starfatorg umsækjanda**.

-   **Vefslóð til að sækja um auglýst starf** - Þegar þú [auglýsir ytra starf](Creating-jobs-Attract.md#postings) í fyrsta skipti getur þú afritað **Sækja um** tengilinn frá Attract-forritinu. Slóðin fyrir þennan tengil verður í eftirfarandi sniði: [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>/apply](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e/apply)

-   **Vefslóð fyrir auglýst starf** - Vefslóð auglýsts starfs er undirstrengur á Sækja um vefslóðinni. Hún samanstendur af öllu sem tengist númeri starfs. Þar af leiðandi fyrir fyrri Sækja um vefslóðina er vefslóð auglýsta starfsins [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e)

## <a name="authentication-options"></a>Valkostir sannvottunar

Umsækjendur hafa eftirfarandi innskráningarmöguleika fyrir Attract-starfatorg:

-   Einkareikningur:

    -   LinkedIn

    -   Microsoft 

    -   Google

    -   Facebook

-   Vinnu- eða skólareikningur:

    -   Microsoft Azure Active Directory (Azure AD)

Azure AD innskráning er aðeins ætluð fyrir innri umsækjendur. Þar af leiðandi virkar það aðeins fyrir innri umsækjendur sem nota Azure AD skilríki fyrirtækisins. Til dæmis, umsækjandi sem er nú starfsmaður Contoso Ltd vill sækja um starf í ótengdum fyrirtækjum, Alpine Ski House. Í þessu tilviki mun innskráningin ekki ná árangri ef starfsmaðurinn reynir að nota Azure AD skilríki frá Contoso Ltd. 

Umsækjendur verða að skrá sig inn með því að nota Azure AD ef starfið sem þeir eru að skoða eða sækja um er flokkað sem eingöngu innan fyrirtækis.

## <a name="create-and-maintain-a-profile"></a>Stofna og viðhalda síðu

Eftir að umsækjendur hafa skráð sig inn á starfatorgið, geta þeir valið **Síðan mín** á yfirlitsstikunni efst á síðunni til að stofna og viðhalda síðunni sinni.
Síðan inniheldur persónulegar upplýsingar, upplýsingar um starfsreynslu, upplýsingar um menntun, skjöl, tengla og upplýsingar um sérþekkingu. Eftir að síðan er stofnuð er hægt að nota hana til að sækja um störf sem umsækjandi hefur áhuga á. Síður hjálpa einnig Attract að mæla með rétt störfum fyrir umsækjendur.

> [!NOTE]
> Ef umsækjandi notar tölvupóstsauðkenni til að skrá þig inn með því að nota eina af sannvottunarþjónustunum sem taldir eru upp hér að ofan, mun þetta tölvupóstsauðkenni verða sjálfgefið að tölvupóstsauðkenni tengiliðar sem tengist prófílnum. Hins vegar er hægt að breyta seinni tölvupóstinum hvenær sem er og er algjörlega óháð fyrri tölvupóstinum. Attract mun alltaf nota kenni tengiliðanetfangsins til að tengja við prófílinn þinn fyrir öll tölvupóstsamskipti.

## <a name="find-the-right-job"></a>Finndu rétta starfið

Á starfassíðunni geta umsækjendur leitað að tilteknu starfi með því að slá inn leitarorð. Leitin finnur leitarorðin í starfsheiti og starfslýsingar og sýnir viðeigandi störf sem niðurstöður. Umsækjendur geta síað niðurstöðurnar hvenær sem er, byggt á staðsetningu starfs eða starfshlutverki.

Umsækjendur geta einnig skoðað safn af ráðlögðum störfum á starfatorginu. Starfið sem mælt er með fyrir umsækjanda byggist á fyrri umsóknum umsækjenda, síðu hans og ferilsskrá.

> [!NOTE] 
> Tillögur að störfum eru aðeins sýnd ef að minnsta kosti 10 störf eru birt á starfatorginu og ef umsækjandi hefur lokið við notandasíðu.

Umsækjendur innan fyrirtækis geta einnig séð hver mannauðsstjórinn og/eða ráðningaraðilinn er fyrir starfið, ef þeir skyldu vilja hafa samband við þessa aðila í ráðningarhópnum. Umsækjendur utan fyrirtækis sjá hins vegar ekki hverjir aðilar ráðningarhópsins eru fyrir hvaða starf sem er.

## <a name="contact-the-hiring-team"></a>Hafa samband við ráðningarhópinn
Einungis umsækjendur innan fyrirtækisins geta haft samband við ráðningarhópinn. Þessi takmörkun á við um öll störf, óháð því hvort þau eru eingöngu innan fyrirtækis eða birt opinberlega.

Hugsanlega vilja umsækjendur hafa samband við ráðningarhópinn til að láta vita af áhuga um starf sem var auglýst eða viljað fá frekari upplýsingar. Þeir geta haft samband við einhvern úr ráðningarhópnum sem eru skráðir (ráðningarstjóri eða ráðningaraðilar). Þeir geta einnig valið að hengja ferilskrá við skilaboðin, eða þeir geta valið ferilskrá sem er til staðar, sem var hlaðið upp sem hluta af prófíl þeirra.

Eftir að umsækjandi innan fyrirtækisins velur aðila ráðningarhópsins til að hafa samband við, sendir Attract tölvupóst til þeirra fyrir hönd umsækjanda. Á sama tíma er prófíl umsækjanda bætt við stigið **Viðfang** ef stigið er tiltækt fyrir starfið. Undir stiginu **Viðfang** geta ráðningaraðilar eða ráðningarstjórar skoðað umsækjendur sem hafa haft samband við þá. Þeir geta einnig yfirfarið notendasíður umsækjenda og boðið mögulegum umsækjendum að sækja um.

Umsækjendur geta sótt um starf sem þeir hafa þegar haft samband við meðlimi ráðningarhóps út af. Eftir að þeir hafa sótt um, geta umsækjendur ekki lengur haft samband við ráðningarhópinn í gegnum starfsferilssíðu.

## <a name="apply-for-jobs"></a>Sækja um störf

Eftir að umsækjendur hafa fundið rétt starf, þá geta þeir sótt um með því að nota  **Sækja um** hnappinn á síðunni  **Starfsupplýsingar**. Á þessum tímapunkti geta umsækjendur annaðhvort búið til nýja síðu eða endurskoðað upplýsingarnar á núverandi síðu.
Umsækjendur geta einnig hlaðið upp ferilskrá, eftir því sem þörf krefur, og síðan sent inn starfsumsóknina.

### <a name="enable-applying-for-jobs-with-linkedin-profiles"></a>Gera kleift að sækja um störf með notendasíðum LinkedIn

Hægt er að auðvelda umsækjendum að sækja um stöður þínar með því að stilla Attract þannig að þeir geti sótt um í gegnum LinkedIn.

> [!NOTE] 
> Nauðsynlegt er að hafa eitt eða fleiri ráðningarleyfi frá LinkedIn áður en hægt er að leyfa umsækjendum að sækja um með LinkedIn.

1. Skráðu þig inn í Attract sem stjórnandi.
2. Veldu hnappinn **Stillingar** (gírtáknið) efst í hægra horni síðunnar og veldu síðan **Stjórnandamiðstöð**.
3. Velja skal flipann **LinkedIn-samþætting** og tengjast við LinkedIn Recruiter reikning.
4. Í hlutanum **LinkedIn Recruiter System Connect Samþætting** skal velja **Gera virkt** fyrir stillinguna **Sækja um með LinkedIn**.

Eftir að þú hefur virkjað stillinguna, geta umsækjendur sótt um með því að nota núverandi prófílgögn á LinkedIn. Þegar umsækjendur sækja um með því að velja hnappinn **Sækja um með LinkedIn** eru þeir beðnir um að sannvotta með LinkedIn ef þeir hafa ekki þegar skráð sig inn. Eftir að þeir hafa sannvottað, kemur LinkedIn-notandasíða þeirra í stað núverandi prófílgagna sem birtast á umsóknarsíðunni. Umsækjendur geta breytt upplýsingunum eftir þörfum og síðan sent inn umsóknina. Ef umsækjandi fer af síðunni án þess að sækja um starfið verða prófílgögn hans ekki uppfærð í Attract.

## <a name="check-application-status"></a>Athuga stöðu umsóknar

Eftir að umsækjendur hafa sótt um eitt eða fleiri störf, geta þeir valið **Umsóknir** á yfirlitsstikunni efst á síðunni til að skoða opnar og lokaðar umsóknir sínar. Þegar umsækjendur opna eitt af umsóknunum sínum sjá þeir núverandi stig og aðgerðaratriði sem bíða eftir að þeir ljúki þeim. Til dæmis, ef umsækjandi verður að gefa upp hugsanlegar dagsetningar fyrir viðtal í eigin persónu, sýnir síðan tiltæka valkosti.

## <a name="internal-jobs"></a>Innri störf

Nú birtast störf sem eru merktar sem innri störf og sett fram á Attract-svæðinu ekki á starfatorginu. Þau eru aðeins aðgengileg með því að nota vefslóðina **Sækja um** beint sem hægt er að afrita úr Attract-forritinu.
