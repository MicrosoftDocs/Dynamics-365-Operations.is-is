---
title: "Virkni starfatorgs í Attract"
description: "Þessi grein veitir yfirlit um starfatorg sem snýr að umsækjendum í Microsoft Dynamics 365 for Talent - Attract. Það útskýrir einnig hvernig á að setja upp þessa virkni."
author: josaw
manager: AnnBe
ms.date: 10/18/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: 452e3e92ea32ab5f1e3720ab81ff2f7ea18b2a06
ms.contentlocale: is-is
ms.lasthandoff: 10/22/2018

---
# <a name="career-site-functionality-in-attract"></a>Virkni starfatorgs í Attract

[!include [banner](includes/banner.md)]

Þessi grein veitir yfirlit um starfatorg sem snýr að umsækjendum í Microsoft Dynamics 365 for Talent: Attract. Það útskýrir einnig hvernig á að setja upp þessa virkni.

## <a name="overview"></a>Yfirlit

Attract býður upp á eitt starfatorg fyrir hvert umhverfi í leigjanda. Til dæmis, ef fyrirtæki hefur þróunarumhverfi og prófunarumhverfi er eitt starfatorg búð til fyrir þróunarumhverfið og annað starfatorg búið til fyrir prófunarumhverfið. Hvert starfatorg er **fullkomlega einangrað** og hefur eigið sannvottunarkerfi. Störf og síðum umsækjenda er ekki deilt á milli starfatorga.

Sjálfgefið er að starfatorgið sé opinbert. Þar af leiðandi geta umsækjendur skoðað öll störf sem eru merkt sem ytri án þess að þurfa að skrá sig inn. Hins vegar kalla allar aðrar aðgerðir á að umsækjendur skrái sig inn.

## <a name="career-site-management"></a>Stjórnun ferilssíðu

Eftirfarandi atriði á starfatorginu eru stjórnað af stillingum:

- **Heiti fyrirtækisins:** Heiti fyrirtækisins birtist á yfirlitsstikunni efst á starfatorginu. Með því að velja heiti fyrirtækisins, fara umsækjendur á síðu sem sýnir alla opna störf.
- **Merki fyrirtæksins** Mynd af merki fyrirtækisins birtist efst til vinstri á starfatorginu. Með því að velja merkið fara umsækjendur á síðu sem sýnir alla opna störf.

Til að stilla gildin fyrir heiti og merki fyrirtæksins, skráðu þig inn í Attract sem stjórnandi, veldu **Stjórnendamiðstöð** á **Stillingar** valmyndinni (gírtáknið) og veldu síðan flipann **Fyrirtækisupplýsingar**.

> [!NOTE]
> Merkið sem birtist á starfatorginu hefur fastsetta hæð sem nemur 20 pixlum (px). Myndin sem þú bætir við í stjórnendastöðinni er minnkuð til að passa. Þess vegna getur breiddin breyst, allt eftir myndinni.

## <a name="career-site-url"></a>Vefslóð starfatorgsins

Þegar þú [auglýsir ytra starf](./Creating-jobs-Attract.md#postings) í fyrsta skipti getur þú afritað **Sækja um** tengilinn frá Attract-forritinu. Slóðin fyrir þennan tengil verður í eftirfarandi sniði: `https://jobs.talent.dynamics.com/jobs/<company_name>/<environment_number>/<job_number>/apply`

Vefslóð starfatorgsins er undirstrengur á **Sækja um** vefslóðinni. Það samanstendur af öllu að heiti fyrirtækisins. Þar af leiðandi fyrir fyrri **Sækja um** vefslóðina er vefslóð starfatorgsins `https://jobs.talent.dynamics.com/jobs/<company_name>/`.

## <a name="authentication-options"></a>Valkostir sannvottunar

Umsækjendur hafa eftirfarandi innskráningarmöguleika fyrir Attract-starfatorg:

- Einkareikningur:

    - LinkedIn
    - Microsoft 
    - Google
    - Facebook

- Vinnu- eða skólareikningur:

    - Microsoft Azure Active Directory (Azure AD)

Azure AD-innskráning er aðeins ætlað fyrir innri umsækjendur. Þar af leiðandi virkar það aðeins fyrir innri umsækjendur sem Azure AD-skilríki fyrirtækisins síns. Til dæmis, umsækjandi sem er nú starfsmaður Contoso Ltd vill sækja um starf í ótengdum fyrirtækjum, Alpine Ski House. Í þessu tilviki mun innskráningin ekki ná árangri ef starfsmaðurinn reynir að nota Azure AD-skilríki sín frá Contoso Ltd.

## <a name="create-and-maintain-a-profile"></a>Stofna og viðhalda síðu

Eftir að umsækjendur hafa skráð sig inn á starfatorgið, geta þeir valið **Síðan mín** á yfirlitsstikunni efst á síðunni til að stofna og viðhalda síðunni sinni. Síðan inniheldur persónulegar upplýsingar, upplýsingar um starfsreynslu, upplýsingar um menntun, skjöl, tengla og upplýsingar um sérþekkingu. Eftir að síðan er stofnuð er hægt að nota hana til að sækja um störf sem umsækjandi hefur áhuga á. Síður hjálpa einnig Attract að mæla með rétt störfum fyrir umsækjendur.

## <a name="find-the-right-job"></a>Finndu rétta starfið

Á starfassíðunni geta umsækjendur leitað að tilteknu starfi með því að slá inn leitarorð. Leitin finnur leitarorðin í starfsheiti og starfslýsingar og sýnir viðeigandi störf sem niðurstöður. Umsækjendur geta síað niðurstöðurnar hvenær sem er, byggt á staðsetningu starfs eða starfshlutverki.

Umsækjendur geta einnig skoðað safn af ráðlögðum störfum á starfatorginu. Starfið sem mælt er með fyrir umsækjanda byggist á fyrri umsóknum umsækjenda, síðu hans og ferilsskrá.

> [!NOTE]
> Tillögur að störfum eru aðeins sýnd ef að minnsta kosti 10 störf eru settar fram á starfatorginu og ef umsækjandi hefur lokið við uppsetningu síðu sinnar.

## <a name="apply-for-jobs"></a>Sækja um störf

Eftir að umsækjendur hafa fundið rétt starf, þá geta þeir sótt um með því að nota **Sækja um** hnappinn á upplýsingasíðu starfsins. Á þessum tímapunkti geta umsækjendur annaðhvort búið til splunkunýja síðu eða endurskoðað upplýsingarnar í núverandi síðu. Umsækjendur geta einnig hlaðið upp ferilskrá, eftir því sem þörf krefur, og síðan sent inn starfsumsóknina.

## <a name="check-application-status"></a>Athuga stöðu umsóknar

Eftir að umsækjendur hafa sótt um eitt eða fleiri störf, geta þeir valið **Umsóknir** á yfirlitsstikunni efst á síðunni til að skoða opnar og lokaðar umsóknir sínar. Þegar umsækjendur opna eitt af umsóknunum sínum sjá þeir núverandi stig og aðgerðaratriði sem bíða eftir að þeir ljúki þeim. Til dæmis, ef umsækjandi verður að gefa upp hugsanlegar dagsetningar fyrir viðtal í eigin persónu, sýnir síðan valkostina hans.

## <a name="internal-jobs"></a>Innri störf

Nú birtast störf sem eru merktar sem innri störf og sett fram á Attract-svæðinu ekki á starfatorginu. Þau eru aðeins aðgengileg í gegnum að **Sækja um** beint á vefslóðinni sem hægt er að afrita úr Attract-forritinu.

