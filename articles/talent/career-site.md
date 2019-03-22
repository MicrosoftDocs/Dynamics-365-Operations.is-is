---
title: Virkni starfatorgs í Attract
description: Þessi efnisatriði veitir yfirlit yfir starfatorg sem snýr að umsækjendum í Attract.
author: josaw1
manager: AnnBe
ms.date: 02/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-02-12
ms.dyn365.ops.version: AX 7.1.0, Talent April 2018 update
ms.openlocfilehash: 087ab4034a1e601e7f3514c77d56ef54b0c5c52d
ms.sourcegitcommit: 1ee613a88edddab036d145f27f19d071a4b8ad24
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/13/2019
ms.locfileid: "389968"
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

    >   [!NOTE] 
    >   Merkið sem birtist á starfatorginu hefur fastsetta hæð sem nemur 20 pixlum (px). Myndin sem þú bætir við í stjórnendastöðinni er minnkuð til að passa. Þess vegna getur breiddin breyst, allt eftir myndinni.
 
Til að stilla gildin fyrir eftirfarandi atriði, skráðu þig inn í Attract sem stjórnandi, veldu **Stjórnendamiðstöð** á **Stillingar** valmyndinni og veldu síðan flipann **Starfatorg umsækjanda**.

-   **Leitarvélabestun** - Ef virkt verður hægt að leita að öllum almennum störfum sem birtast í starfatorgi Attract þegar leitarvélar eins og Bing og Google eru notaðar.

    >   [!NOTE] 
    >   Það gæti orðið tafir á milli þess að kveikja á þessari stillingu og leitarniðurstöður birtast, fer allt eftir leitarvélinni sem þú notar.
         
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

## <a name="create-and-maintain-a-profile"></a>Stofna og viðhalda síðu

Eftir að umsækjendur hafa skráð sig inn á starfatorgið, geta þeir valið **Síðan mín** á yfirlitsstikunni efst á síðunni til að stofna og viðhalda síðunni sinni.
Síðan inniheldur persónulegar upplýsingar, upplýsingar um starfsreynslu, upplýsingar um menntun, skjöl, tengla og upplýsingar um sérþekkingu. Eftir að síðan er stofnuð er hægt að nota hana til að sækja um störf sem umsækjandi hefur áhuga á. Síður hjálpa einnig Attract að mæla með rétt störfum fyrir umsækjendur.

>   [!NOTE]
>   Ef umsækjandi notar tölvupóstsauðkenni til að skrá þig inn með því að nota eina af sannvottunarþjónustunum sem taldir eru upp hér að ofan, mun þetta tölvupóstsauðkenni verða sjálfgefið að tölvupóstsauðkenni tengiliðar sem tengist prófílnum. Hins vegar er hægt að breyta seinni tölvupóstinum hvenær sem er og er algjörlega óháð fyrri tölvupóstinum. Attract mun alltaf nota kenni tengiliðanetfangsins til að tengja við prófílinn þinn fyrir öll tölvupóstsamskipti.

## <a name="find-the-right-job"></a>Finndu rétta starfið

Á starfassíðunni geta umsækjendur leitað að tilteknu starfi með því að slá inn leitarorð. Leitin finnur leitarorðin í starfsheiti og starfslýsingar og sýnir viðeigandi störf sem niðurstöður. Umsækjendur geta síað niðurstöðurnar hvenær sem er, byggt á staðsetningu starfs eða starfshlutverki.

Umsækjendur geta einnig skoðað safn af ráðlögðum störfum á starfatorginu. Starfið sem mælt er með fyrir umsækjanda byggist á fyrri umsóknum umsækjenda, síðu hans og ferilsskrá.

>   [!NOTE] 
>   Tillögur að störfum eru aðeins sýnd ef að minnsta kosti 10 störf eru birt á starfatorginu og ef umsækjandi hefur lokið við notandasíðu.

## <a name="apply-for-jobs"></a>Sækja um störf

Eftir að umsækjendur hafa fundið rétt starf, þá geta þeir sótt um með því að nota **Sækja um** hnappinn á síðunni **Starfsupplýsingar**. Á þessum tímapunkti geta umsækjendur annaðhvort búið til nýja síðu eða endurskoðað upplýsingarnar á núverandi síðu.
Umsækjendur geta einnig hlaðið upp ferilskrá, eftir því sem þörf krefur, og síðan sent inn starfsumsóknina.

## <a name="check-application-status"></a>Athuga stöðu umsóknar

Eftir að umsækjendur hafa sótt um eitt eða fleiri störf, geta þeir valið **Umsóknir** á yfirlitsstikunni efst á síðunni til að skoða opnar og lokaðar umsóknir sínar. Þegar umsækjendur opna eitt af umsóknunum sínum sjá þeir núverandi stig og aðgerðaratriði sem bíða eftir að þeir ljúki þeim. Til dæmis, ef umsækjandi verður að gefa upp hugsanlegar dagsetningar fyrir viðtal í eigin persónu, sýnir síðan tiltæka valkosti.

## <a name="internal-jobs"></a>Innri störf

Nú birtast störf sem eru merktar sem innri störf og sett fram á Attract-svæðinu ekki á starfatorginu. Þau eru aðeins aðgengileg með því að nota vefslóðina **Sækja um** beint sem hægt er að afrita úr Attract-forritinu.
