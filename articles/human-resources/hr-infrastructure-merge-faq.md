---
title: Algengar spurningar um sameiningu Dynamics 365 Human Resources tölvukerfis
description: Þetta efnisatriði svarar algengum spurningum um sameiningu tölvukerfis fyrir Microsoft Dynamics 365 Human Resources og Finance and Operations forrit.
author: twheeloc
ms.date: 08/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5ae2896eda98a8f9545d465e941d5b50065ae94b
ms.sourcegitcommit: 822aea26c5da259efe11ff3b3dc4cf1598425689
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/16/2021
ms.locfileid: "7386540"
---
# <a name="dynamics-365-human-resources-infrastructure-merge-faq"></a>Algengar spurningar um sameiningu Dynamics 365 Human Resources tölvukerfis

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Þetta efnisatriði svarar algengum spurningum um sameiningu tölvukerfis fyrir Microsoft Dynamics 365 Human Resources og Finance and Operations forrit.

## <a name="what-is-the-dynamics-365-human-resources-infrastructure-merge"></a>Hvað er sameining Dynamics 365 Human Resources tölvukerfis?

Dynamics 365 Human Resources er sjálfstætt forrit sem notar annað tölvukerfi en önnur Finance and Operations forrit á borð við Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce og Dynamics 365 Project Operations. Sameining tölvukerfisins mun flytja Dynamics 365 Human Resources inn í sama tölvukerfi og önnur Finance and Operations-forrit.

## <a name="value-and-benefits-of-the-infrastructure-merge"></a>Ávinningur og fríðindi vegna sameiningar tölvukerfis

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-its-hr-operations-what-benefits-will-we-see-from-these-changes"></a>Fyrirtækið mitt notar Dynamics 365 Human Resources til að stjórna mannauðsaðgerðum. Hvaða ávinning munum við sjá af þessum breytingum?

- Þessar breytingar koma í veg fyrir ruglinginn sem margir möguleikar mannauðs í Dynamics 365 valda.
- Þær bjóða bæði upp á Microsoft Power Platform stækkunarhæfni og leið til að stækka viðskiptagrunn og valkosti eiginleika.
- Þær auka stöðugleika á milli Dynamics 365 Human Resources og annarra Finance and Operations-forrita hvað varðar ALM (Application Lifecycle Management), Microsoft Dynamics Lifecycle Services (LCS), framboð eftir staðsetningu, stækkunarhæfni og fleira.
- Með þeim getur þú nýtt þér sameiginlega þjónustu og verkfæri og hjálpað til við að draga úr kostnaði.

### <a name="my-organization-uses-the-human-resources-module-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-what-benefits-will-we-see-from-these-changes"></a>Fyrirtækið mitt notar Human Resources eininguna í Dynamics 365 Finance, Supply Chain Management, Commerce eða Project Operations. Hvaða ávinning munum við sjá af þessum breytingum?

Möguleikar og fjárfestingar sem gerðar hafa verið í Dynamics 365 Human Resources munu nú standa viðskiptavinum til boða sem nota mannauðseininguna í Dynamics 365 Finance. Sumir þessara möguleika fela í sér leyfis- og fjarvistarstjórnun, fríðindastjórnun og verkstjórnun.

### <a name="will-i-lose-any-features-or-capabilities-that-i-currently-use"></a>Mun ég glata eiginleikum eða möguleikum sem ég er að nota?

Virk samsvörun verður milli Dynamics 365 Human Resources og mannauðseiningarinnar í Finance and Operations-forritum. Dynamics 365 Human Resources mun hafa forgang fyrir líka eiginleika. Frekari upplýsingar er að finna í [Eiginleikastjórnunaryfirlit](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="will-the-experience-change-for-my-users"></a>Breytist upplifunin fyrir notendur mína?

Nýjum möguleikum mannauðs verður stjórnað í gegnum eiginleikastjórnun. Viðskiptavinir taka ákvörðun um hvort þeir vilji taka þá upp. Í sumum tilfellum gæti möguleikum verið breytt. Í þeim tilfellum verða lögð fram fylgigögn.

### <a name="how-does-this-change-affect-me-if-i-am-an-existing-customer-and-i-use-both-the-hr-module-on-the-finance-and-operations-infrastructure-and-dynamics-365-human-resources-through-custom-integrations"></a>Hvernig hefur þessi breyting áhrif á mig ef ég er núverandi viðskiptavinur og ég nota bæði mannauðseininguna í Finance and Operations tölvukerfinu og Dynamics 365 Human Resources með sérsniðnum samþættingum?

Sérsniðnar samþættingar milli Dynamics 365 Human Resources og mannauðseiningarinnar í Dynamics 365 Finance verða ekki lengur nauðsynlegar. Öll mannauðsgögn verða geymd í sama gagnagrunni og önnur Finance and Operations-forrit.

## <a name="migration-from-dynamics-365-human-resources-to-finance-and-operations-apps"></a>Flutningur úr Dynamics 365 Human Resources í Finance and Operations-forrit

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-hr-operations-what-do-we-have-to-plan-for-to-migrate-to-the-new-experience"></a>Fyrirtækið mitt notar Dynamics 365 Human Resources til að stjórna mannauðsaðgerðum. Hvað þurfum við að undirbúa fyrir flutning yfir í nýju upplifunina?

Ef fyrirtækið notar Dynamics 365 Human Resources en notar ekki önnur Finance and Operations forrit verður mannauðsumhverfið flutt yfir í nýja tölvukerfið. Mikið af þessu flutningsferli verður sjálfvirkt. Ferlar verða til staðar til að flytja gagnagrunninn þinn og samstilla hann við nýja tölvukerfið.

Að auki verður komið upp verkfærum svo að hægt sé að prófa flutningsferlið og sannprófa gögn og upplifun áður en vinnsluumhverfið er flutt.

Ef fyrirtækið notar bæði Dynamics 365 Human Resources og önnur Finance and Operations forrit ættir þú að skipuleggja meiri tíma fyrir staðfestingu til að tryggja að gögnin þín séu flutt á réttan hátt í nýja umhverfið. Flutningurinn yfir í nýja tölvukerfið mun sameina gögn úr mannauðsumhverfinu saman við Finance and Operations umhverfið þitt. Árekstur gagna þarf á inngripi notanda að halda til að ákveða hvernig á að leysa úr árekstrinum. Notendur og stjórnendur þurfa að hafa umsjón með gagnavörpunum þar sem árekstrar koma upp og prófa flutninginn í sandkassaumhverfi áður en vinnsluumhverfi eru flutt.

### <a name="my-organization-uses-the-human-resources-module-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-what-do-we-have-to-plan-for-to-migrate-to-the-new-experience"></a>Fyrirtækið mitt notar Human Resources eininguna í Dynamics 365 Finance, Supply Chain Management, Commerce eða Project Operations. Hvað þurfum við að undirbúa fyrir flutning yfir í nýju upplifunina?

Fyrir fyrirtæki sem nota mannauðseininguna í Finance and Operations forritum verður nýi eiginleiki virkninnar úr Dynamics 365 Human Resources notaður í umhverfi þitt í gegnum hefðbundið uppfærsluferli fyrir One Version. Þú getur búist við að sjá nýju virknina í umhverfinu þínu eftir því sem hún verður tiltæk í hverri uppfærslu. Hægt er að nota eiginleikastjórnun til að kveikja á nýjum eiginleikum en þó ætti að leggja drög að því að staðfesta þessa eiginleika. Fylgdu ferlunum sem þú hefur til staðar til að staðfesta aðrar uppfærslur á umhverfi þínu. Frekari upplýsingar um hvernig uppfærslur eru notaðar í Finance and Operations forritum er að finna í [Yfirlit One Version](../fin-ops-core/dev-itpro/lifecycle-services/oneversion-overview.md).

### <a name="when-will-my-organization-be-migrated"></a>Hvenær verður fyrirtækið mitt flutt?

Flutningur hvers fyrirtækis fer eftir núverandi skilgreiningu og hvort það sé tilbúið undir flutning í nýja tölvukerfið. Þessar dagsetningar geta breyst.

- Fyrirtæki sem nota mannauðseininguna í Finance and Operations forritum fá virkni mannauðs fyrir Dynamics 365 Human Resources sem hluta af reglubundnu uppfærsluferli One Version. Áformað er að nýir eiginleikar verði almennt í boði frá og með janúar 2022.
- Fyrirtæki sem nota aðeins Dynamics 365 Human Resources munu hafa aðgang að flutningsverkfærum svo að þau geti hafið prófanir og hafið flutninginn um miðbik 2022. Dagsetningin þegar flutningur í nýja tölvukerfið verður að vera lokið hefur ekki verið ákveðin. Hins vegar verður það að minnsta kosti einu ári eftir dagsetninguna þegar flutningsverkfærin verða aðgengileg.
- Fyrirtæki sem nota bæði Dynamics 365 Human Resources og önnur Finance and Operations forrit munu hafa aðgang að flutningsverkfærum svo að þau geti hafið prófanir og hafið flutninginn seinni hluta 2022. Dagsetningin þegar flutningur í nýja tölvukerfið verður að vera lokið hefur ekki verið ákveðin. Hins vegar verður það að minnsta kosti einu ári eftir dagsetninguna þegar flutningsverkfærin verða aðgengileg.

Frekari upplýsingar um nýju eiginleikana fyrir Dynamics 365 Human Resources er að finna í [Hvað er nýtt eða breytt í Human Resources](./hr-admin-whats-new.md).

### <a name="my-organization-has-not-yet-gone-live-on-dynamics-365-human-resources-should-we-go-live-with-the-human-resources-module-in-the-finance-and-operations-apps-or-with-the-dynamics-365-human-resources-app-on-the-legacy-infrastructure"></a>Fyrirtækið mitt hefur ekki enn verið sett af stað í Dynamics 365 Human Resources. Ættum við að keyra einingu Human Resources í Finance and Operations forritum eða með Dynamics 365 Human Resources forritinu í eldra tölvukerfi?

Mikilvæg atriði sem þarf að hafa í huga eru hvaða virkni Human Resources er þörf á og hvenær sú virkni verður tiltæk í nýja tölvukerfinu. Ef fyrirtækið þarf meginvirknina fyrir starfsmannastjórnun er hún í boði í einingu Human Resources í Finance and Operations forritinu í nýja tölvukerfinu. Gert er ráð fyrir jafngildi milli einingar Human Resources fyrir Finance and Operations forritin og Dynamics 365 Human Resources forritið í útgáfu 10.0.25 sem áætlað er að verði almennt aðgengileg í mars 2022. Samþættingareiginleikar á borð við Teams-forritið og Dataverse samþættingareiningar verða tiltæk í síðari útgáfum.

Ef virkni Human Resources í fyrirtækinu þarf að vera aðgengilegt í nýja tölvukerfinu innan tímarammans sem fyrirtækið er sett á laggirnar, gæti verið auðveldara að keyra það í einingu Human Resources í Finance and Operations forritunum. Þetta leiðir til auðveldari flutnings þar sem þetta verður hefðbundin uppfærsla forrits í Dynamics 365 Human Resources forritinu og viðskiptavinurinn verður þegar í nýja tölvukerfinu. Ef fyrirtækið ákveður að fara af stað í Dynamics 365 Human Resources forritinu í eldra tölvukerfinu þá þarf að flytja umhverfi yfir í nýja tölvukerfið. Hægt er að komast hjá þessu með því að keyra í nýja tölvukerfinu.

### <a name="i-am-using-new-capabilities-that-are-available-only-in-dynamics-365-human-resources-such-as-leave-and-absence-and-benefits-management-will-these-capabilities-now-be-available-in-the-human-resources-module-on-the-finance-and-operations-infrastructure-too"></a>Ég er að nota nýja möguleika sem eru aðeins í boði í Dynamics 365 Human Resources (eins **Leyfi og fjarvistir** og **Fríðindastjórnun**). Munu þessir möguleikar nú vera aðgengilegir í einingu Human Resources í Finance and Operations tölvukerfinu líka?

Já, allar einingarnar úr Dynamics 365 Human Resources munu virka eins og þær eru í Finance and Operations forritum og það verður 100 prósent jafngildi. Sem hluti af heildaráætlun um flutning fyrir viðskiptavini sem nú nota þessa möguleika í mannauðsstjórnun verða gögn viðskiptavina flutt þannig að þau haldi áfram að vinna í Finance and Operations tölvukerfinu.

### <a name="i-use-the-new-dynamics-365-human-resources-benefits-management-capabilities-ive-built-custom-integrations-with-the-hr-module-on-the-finance-and-operations-infrastructure-so-that-i-can-take-advantage-of-the-payroll-capabilities-by-using-benefits-data-will-these-custom-integrations-be-required-going-forward"></a>Ég nota nýju Dynamics 365 Human Resources fríðindastjórnunarmöguleikana. Ég hef búið til sérsniðnar samþættingar með mannauðseiningunni í Finance and Operations tölvukerfinu svo ég geti nýtt mér mögulega launaskráar með því að nota fríðindagögn. Verða þessar sérsniðnu samþættingar nauðsynlegar í framhaldinu?

Sem hluti af samruna tölvukerfis eru mannauðsgögn færð inn í sama gagnagrunn og önnur Finance and Operations forrit. Ekki verður lengur þörf á samþættingu milli eininga í Finance and Operations forritum.

### <a name="my-organization-uses-one-or-more-isv-solutions-with-dynamics-365-human-resources-will-our-isv-solutions-be-migrated-automatically"></a>Fyrirtækið mitt notar eina eða fleiri lausnir óháðs hugbúnaðarsala með Dynamics 365 Human Resources. Munu lausnir óháðs hugbúnaðarsala verða fluttar sjálfkrafa?

Upplifun flutnings fyrir hverja lausn óháðs hugbúnaðarsala verður breytileg eftir því hver samþættingaraðferð lausnarinnar er. Microsoft mun vinna náið með óháðum hugbúnaðarsölum til að tryggja hnökralausan flutning yfir í nýja tölvukerfið.

### <a name="my-organization-uses-linkedin-talent-hub-integration-with-dynamics-365-human-resources-will-this-integration-continue-to-work-after-the-infrastructure-change-is-completed"></a>Fyrirtækið mitt notar samþættingu LinkedIn Talent Hub við Dynamics 365 Human Resources. Mun þessi samþætting halda áfram að virka eftir að breytingu tölvukerfis er lokið?

Nei, LinkedIn Talent Hub samþættingin mun ekki virka eftir flutninginn í nýja tölvukerfið. Þjónustan fyrir samþættingu LinkedIn Talent Hub verður hætt með eldra Dynamics 365 Human Resources tölvukerfinu.

### <a name="my-organization-uses-the-human-resources-app-for-teams-will-the-app-continue-to-work-after-the-infrastructure-change-is-completed"></a>Fyrirtækið mitt notar forrit Human Resources fyrir Teams. Mun forritið halda áfram að virka eftir að breytingu tölvukerfis er lokið?

Já, Human Resources-forritið fyrir Teams mun halda áfram að virka eftir flutninginn í nýja tölvukerfið.

### <a name="my-organization-has-configured-custom-security-in-dynamics-365-human-resources-will-our-custom-security-still-be-applied-after-the-infrastructure-change-is-completed"></a>Fyrirtækið mitt hefur skilgreint sérstillt öryggi í Dynamics 365 Human Resources. Verður sérstillt öryggi notað eftir að breytingu tölvukerfis er lokið?

Já, sérsniðnar öryggisstillingar verða teknar með í gagnaflutningi yfir í nýja tölvukerfið.

### <a name="we-are-using-data-integrator-to-move-data-between-dynamics-365-human-resources-and-finance-and-operations-apps-how-will-the-data-that-is-currently-being-integrated-be-affected"></a>Við erum að nota Data integrator til að færa gögn á milli Dynamics 365 Human Resources og Finance and Operations forrita. Hvaða áhrif hefur það á gögnin sem er verið að samþætta?

Mannauðsgögnin sem er nú stjórnað í Dynamics 365 Human Resources eru samstillt við Dataverse. Þá er hægt að nota Data Integrator fyrir einstefnusamstillingu við Finance and Operations forrit. Eftir flutninginn í nýja tölvukerfið verða mannauðsgögnin staðbundin í Finance and Operations forritum. Ekki verður lengur þörf á Data Integrator til að samstilla gögn milli Finance and Operations forrita og Human Resources.

Núverandi Dataverse staðbundnar gagnatöflur fyrir Human Resources munu halda áfram að samstilla gögn úr umhverfinu í nýja tölvukerfinu. Einingunum verður umbreytt til að styðja tvöfalda skráningu. Allar aðrar samþættingar gagna sem eru stilltar með Data Integrator á móti þessum töflum fyrir önnur Dynamics 365 forrit munu halda áfram að virka eins og þær eru stilltar núna.

### <a name="we-are-using-dual-write-to-move-hr-data-between-dataverse-and-other-finance-and-operations-apps-how-will-the-data-that-is-currently-being-integrated-be-affected-by-the-migration-to-the-new-infrastructure"></a>Við erum að nota tvöfalda skráningu til að flytja mannauðsgögn milli Dataverse og annarra Finance and Operations forrita. Hvernig verða gögnin sem nú er verið að samþætta fyrir áhrifum af flutningi í nýja tölvukerfið?

Mannauðsgögnin verða staðbundin Finance and Operations forritunum í umhverfum í nýja tölvukerfinu. Tvískrifuð gögn verða notuð til að færa mannauðsgögn á milli nýja umhverfisins og Dataverse umhverfisins.

### <a name="we-have-built-custom-integrations-from-dynamics-365-human-resources-to-one-or-more-external-systems-will-we-have-to-develop-new-integrations-after-the-infrastructure-change-is-completed"></a>Við höfum búið til sérsniðnar samþættingar úr Dynamics 365 Human Resources í eitt eða fleiri ytri kerfi. Þurfum við að þróa nýjar samþættingar eftir að breytingu tölvukerfis er lokið?

Það fer eftir endastöð samþættingarinnar. Nánari upplýsingar um samþættingartækni sem er í boði í Finance and Operations forritum og hvernig á að velja bestu samþættingartæknina er að finna í [Yfirlit yfir samþættingu](../fin-ops-core/dev-itpro/data-entities/integration-overview.md).

### <a name="we-have-extended-dataverse-for-dynamics-365-human-resources-will-these-extensions-be-migrated-automatically"></a>Við höfum stækkað Dataverse fyrir Dynamics 365 Human Resources. Verða þessar viðbætur fluttar sjálfkrafa?

Ef Dynamics 365 Human Resources og Finance and Operations umhverfin sem verða tengd við umhverfið í nýja tölvukerfinu eru tengd við sama Dataverse umhverfið munu forritin tvö vera áfram tengd við sama Dataverse umhverfið eftir flutninginn. Ekki þarf að flytja neitt fyrir Dataverse viðbætur.

Hins vegar ef Dynamics 365 Human Resources og Finance and Operations umhverfin eru þegar tengd við aðskilin Dataverse umhverfi þarf að sameina Dataverse umhverfin tvö þannig að þau séu tengd við eitt umhverfi í nýja tölvukerfinu. Fyrir þennan Dataverse flutning er hægt að tengja Dataverse töflurnar sem eru staðlaðar við lausnir Human Resources við og samstilla þær við nýja Dataverse umhverfið. Allar viðbætur við Dataverse umhverfið verða ekki fluttar sjálfkrafa heldur þarf að setja þær upp aftur í nýja umhverfinu. Mælt er með því að nota stýrðar lausnir til að stjórna Dataverse viðbótunum þínum. Frekari upplýsingar er að finna í [Kynning á lausnum](/powerapps/developer/data-platform/introduction-solutions).

### <a name="we-have-configured-microsoft-power-automate-flows-andor-microsoft-power-apps-to-work-with-dynamics-365-human-resources-will-these-microsoft-power-platform-components-be-migrated-and-work-automatically-after-the-infrastructure-change-is-completed"></a>Við höfum skilgreint Microsoft Power Automate flæði og/eða Microsoft Power Apps til að virka með Dynamics 365 Human Resources. Verða þessir Microsoft Power Platform þættir fluttir og virka þeir sjálfkrafa eftir að breyting á tölvukerfinu er lokið?

Power Apps, Power Automate flæði og aðrar Microsoft Power Platform sérstillingar eru svipaðar Dataverse viðbótum. Hvort þau virki sjálfkrafa eftir flutninginn yfir í nýja tölvukerfið fer eftir því hvort Human Resources-forritið og Finance and Operations forritin séu tengd við sama Power Apps umhverfið og fyrir flutninginn.

Ef forritin eru tengd við sama Power Apps umhverfið verða þau tengd áfram við það Power Apps umhverfi eftir flutninginn yfir í nýja tölvukerfið. Í þessu tilviki munu Power Apps, Power Automate flæði og aðrar Microsoft Power Platform sérstillingar halda áfram að virka án frekari skilgreiningar. Við mælum með að þú notir stýrðar lausnir til að stjórna forritsviðbóðtum í Dataverse. Frekari upplýsingar er að finna í [Kynning á lausnum](/powerapps/developer/data-platform/introduction-solutions).

Ef Human Resources-forritið og Finance and Operations forritin eru hinsvegar tengd við aðskilin Power Apps umhverfi þarf að sameina þau sem hluti af flutningnum. Þetta verk krefst þess að allar Power Apps og aðrar sérstillingar verði enduruppsettar í nýja umhverfinu.

### <a name="we-have-enabled-dataverse-virtual-tables-for-dynamics-365-human-resources-what-will-happen-to-these-tables-during-the-migration"></a>Við höfum virkjað Dataverse sýndartöflur fyrir Dynamics 365 Human Resources. Hvað verður um þessar töflur við flutninginn?

Eftir flutninginn, ef umhverfið í nýja tölvukerfinu er áfram tengt við Dataverse umhverfið sem nú er tengt við Dynamics 365 Human Resources, munu Dataverse sýndartöflurnar sem hafa verið búnar til í því umhverfi halda áfram að virka án viðbótarstillinga.

Ef hins vegar umhverfið í nýja tölvukerfinu er tengt við annað Dataverse umhverfi eftir flutninginn þarf að endurgera sýndartöflurnar í nýja Dataverse umhverfinu.

### <a name="we-have-developed-an-integration-by-using-the-applicant-tracking-system-ats-api-payroll-api-dataverse-virtual-tables-for-dynamics-365-human-resources-or-other-entities-in-the-dataverse-web-api-will-these-integrations-continue-to-work-after-the-infrastructure-change-is-completed"></a>Við höfum þróað samþættingu með því að nota ATS (Applicant Tracking System) API, API launaskráar, Dataverse sýndartöflur fyrir Dynamics 365 Human Resources eða aðrar einingar í API Dataverse á netinu. Munu þessar samþættingar halda áfram að virka að lokinni breytingu á tölvukerfinu?

Eftir flutninginn, ef umhverfið í nýja tölvukerfinu er áfram tengt við Dataverse umhverfið sem nú er tengt við Dynamics 365 Human Resources, munu allar samþættingar sem hafa verið þróaðar vegna API Dataverse á netinu halda áfram að virka að loknum flutningi.

Ef hins vegar umhverfið í nýja tölvukerfinu er tengt við annað Dataverse umhverfi eftir flutninginn þarf að endurstilla allar samþættingar sem hafa verið þróaðar vegna API Dataverse á netinu þannig að þær tengjast við nýja Dataverse umhverfið.

### <a name="is-there-an-impact-on-the-azure-region-when-my-environment-is-migrated"></a>Hefur það áhrif á Azure-svæðið þegar umhverfi mitt er flutt?

Gert er ráð fyrir að umhverfi Human Resources haldist almennt á sama Azure-svæðinu meðan á flutningnum stendur. Eina undantekningin er ef umhverfi Human Resources verður sameinað öðru Finance and Operations umhverfi sem er á öðru svæði. Í þessu tilviki verður umhverfi Human Resources flutt á Azure-svæðið í Finance and Operations umhverfinu.

### <a name="my-organization-depends-on-workflows-in-dynamics-365-human-resources-for-one-or-more-business-processes-will-the-workflows-be-migrated-automatically"></a>Fyrirtækið mitt reiðir sig á verkflæði í Dynamics 365 Human Resources fyrir einn eða fleiri viðskiptaferla. Verða verkflæðin flutt sjálfkrafa?

Já, skilgreiningar verkflæðis, verkflæðissaga og verkflæði sem eru í vinnslu verða flutt.

### <a name="what-training-and-resources-will-be-available-to-help-with-the-migration-process"></a>Hvaða þjálfun og úrræði verða í boði til að aðstoða við flutningsferlið?

Boðið verður upp á ítarleg fylgigögn til að lýsa nákvæmlega hverju skrefi flutningsferlisins. Frekari þjálfunarúrræði, svo sem myndbönd og vinnustofur, gætu einnig verið í boði ef þörf er á því.

### <a name="my-organization-has-created-saved-views-in-dynamics-365-human-resources-to-improve-the-usability-of-the-interface-will-the-saved-views-be-migrated-automatically"></a>Fyrirtækið mitt hefur búið til vistuð yfirlit í Dynamics 365 Human Resources til að bæta notagildi viðmótsins. Verða vistuð yfirlit flutt sjálfkrafa?

Já, vistuð yfirlit verða flutt í nýja tölvukerfið.

### <a name="we-are-using-ceridian-with-dynamics-365-human-resources-will-the-ceridian-integration-be-available-after-the-infrastructure-change-is-completed"></a>Við erum að nota Ceridian með Dynamics 365 Human Resources. Verður Ceridian-samþættingin tiltæk eftir að breytingu tölvukerfis er lokið? 

Samþættingin við Ceridian verður flutt í samþættingu launaskráar sem byggir á API. Samþætting skráa sem nú er til staðar í Dynamics 365 Human Resources verður ekki flutt í Finance and Operations tölvukerfið. Frekari upplýsingar er að finna í [Kynning á API-launaskrá](./hr-admin-integration-payroll-api-introduction.md).

### <a name="how-will-the-migration-affect-the-service-update-process"></a>Hvernig mun flutningurinn hafa áhrif á ferli þjónustuuppfærslunnar?

Eftir flutninginn munu viðskiptavinir hafa mun meiri sveigjanleika hvað varðar ALM og þjónustuuppfærslur. Þjónustuuppfærslur verða ekki lengur notaðar sjálfkrafa í umhverfum Human Resources. Þess í stað mun þjónustan fylgja ferlum og virkni fyrir þjónustuuppfærslur One Version. Því verða stillingarvalkostir fyrir uppfærslur í boði í gegnum LCS. Nánari upplýsingar má finna í [Yfirlit One Version](../fin-ops-core/dev-itpro/lifecycle-services/oneversion-overview.md).

### <a name="how-will-the-migration-affect-my-lcs-project-for-dynamics-365-human-resources"></a>Hvernig mun flutningurinn hafa áhrif á LCS-verkin fyrir Dynamics 365 Human Resources?

Flutningurinn yfir í nýja tölvukerfið mun færa stjórnun Dynamics 365 Human Resources umhverfisins inn í Finance and Operations samþættingarverk í LCS. Ef flutningurinn sameinar Dynamics 365 Human Resources við núverandi Finance and Operations umhverfi, verður LCS-verk Human Resources sameinað í LCS-samþættingarverk fyrir Finance and Operations forritið. Ef þú ert aðeins að nota Dynamics 365 Human Resources verður nýtt LCS-samþættingarverk stofnað og núverandi LCS-verk Human Resources verður flutt í nýja verkið.

Nýja verkið verður sama gerð af verki og Finance and Operations forritin nota. Það mun hafa sömu eiginleika og virkni fyrir umhverfisstjórnun. Frekari upplýsingar er að finna í [Tilföng Lifecycle Services](../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).

### <a name="we-have-linked-our-task-recordings-to-the-business-process-modeler-in-human-resources-how-will-the-business-process-modeler-be-migrated-and-merged-into-lcs"></a>Við höfum tengt verkskráningarnar okkar við viðskiptaferlavinnsluna í Human Resources. Hvernig verður viðskiptaferlavinnslan flutt og sameinuð í LCS?

Söfn viðskiptaferla fyrir LCS-verkið mun verða flutt í nýja LCS-verkið fyrir Human Resources.

### <a name="my-organization-currently-uses-only-dynamics-365-human-resources-what-resources-are-available-so-that-we-can-learn-more-about-the-development-capabilities-after-the-infrastructure-change-is-completed"></a>Sem stendur notar fyrirtækið mitt aðeins Dynamics 365 Human Resources. Hvaða úrræði eru í boði svo að við getum fengið frekari upplýsingar um þróunarmöguleika eftir að breytingum tölvukerfis er lokið?

Bæði Microsoft Power Platform stækkunarmöguleikar og Finance and Operations stækkunarmöguleikar verða í boði og hægt að nota í þróun. Frekari upplýsingar er að finna í [Þróa og sérstilla heimasíðu](../fin-ops-core/dev-itpro/dev-tools/developer-home-page.md).

### <a name="we-have-enabled-features-in-dynamics-365-human-resources-will-these-features-be-enabled-automatically-during-the-migration"></a>Við höfum virkjað eiginleika í Dynamics 365 Human Resources. Verða þessir eiginleikar sjálfkrafa virkjaðir við flutninginn?

Hvort eiginleiki er virkjaður sjálfkrafa í nýja tölvukerfinu verður ákvarðað sérstaklega fyrir hvern eiginleika. Þessar upplýsingar má finna í fylgigögnum eiginleikans.

### <a name="what-happens-to-my-byod-database-during-the-migration"></a>Hvað verður um BYOD-gagnagrunninn minn við flutninginn?

Inn- og útflutningsstillingar fyrir eigin gagnagrunn (BYOD) verða fluttar í nýja tölvukerfið.

### <a name="what-happens-to-my-azure-data-lake-during-the-migration"></a>Hvað verður um Azure Data Lake við flutninginn?

Allur útflutningur sem er stilltur fyrir Azure Data Lake Storage í Finance and Operations forritum mun halda sömu stillingu eftir flutninginn.

### <a name="we-are-currently-using-dynamics-ax-2012-will-the-upgrade-tools-that-are-currently-available-be-used-to-upgrade-the-hr-module-in-ax-2012-to-dynamics-365-human-resources"></a>Við erum að nota Dynamics AX 2012 eins og er. Verða uppfærsluverkfærin sem nú eru til staðar notuð til að uppfæra mannauðseininguna í AX 2012 í Dynamics 365 Human Resources?

Já. Dynamics 365 Human Resources verður með í sameinuðum kóðagrunni og tölvukerfi fyrir Finance and Operations forrit. Uppfærsla úr Dynamics AX 2012 í Dynamics 365 Human Resources mun nota sömu uppfærsluleið og -verkfæri sem eru notuð til að uppfæra í nýjustu útgáfu af Finance and Operations forritum.

### <a name="we-use-document-handling-with-dynamics-365-human-resources-what-will-happen-to-the-documents-during-the-migration"></a>Við notum skjalastjórnun með Dynamics 365 Human Resources. Hvað verður um skjölin við flutninginn?

Skjölin verða áfram í fyrirliggjandi skjalageymslu. Þeim verður endurvarpað í umhverfið í nýja tölvukerfinu.

### <a name="what-happens-to-the-batch-jobs-that-we-have-configured-in-dynamics-365-human-resources-after-the-migration"></a>Hvað verður um runuvinnslurnar sem við höfum stillt í Dynamics 365 Human Resources eftir flutninginn?

Viðeigandi runuvinnslur verða fluttar sjálfkrafa í nýja tölvukerfið.

## <a name="licensing-impact"></a>Áhrif á leyfisveitingar

Þessi fylgigögn koma ekki í staðinn fyrir lagaleg fylgigögn sem ná yfir notkunarrétt.

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-its-hr-operations-does-our-licensing-or-cost-change"></a>Fyrirtækið mitt notar Dynamics 365 Human Resources til að stjórna mannauðsaðgerðum. Breytist leyfið eða kostnaðurinn?

Þetta hefur engin áhrif á viðskiptavini sem hafa keypt Dynamics 365 Human Resources leyfi. Enginn flutningur á leyfum er til fyrir þessa viðskiptavini. Aukaleg birgðahaldseining (SKU) sandkassa sem tilheyrði Human Resources verður ekki lengur í boði. Þess í stað geta viðskiptavinir valið að kaupa Finance and Operations forrit í sandkassalagi 2 á örlítið lægra verði. Núverandi viðskiptavinir sem hafa keypt sandkassa Human Resources verða fluttir í Finance and Operations forrit í sandkassalagi 2 án aukakostnaðar.

### <a name="my-organization-uses-the-human-resources-module-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-does-my-licensing-or-cost-change"></a>Fyrirtækið mitt notar Human Resources eininguna í Dynamics 365 Finance, Supply Chain Management, Commerce eða Project Operations. Breytist leyfi mitt eða kostnaður?

Núverandi notendur Dynamics 365 forrita og notendur sjálfstæðs Dynamics 365 Finance, Supply Chain Management, Commerce og Project Operations geta fengið aðgang að Human Resources sem hluta af þessum leyfum þangað til febrúar 2025 eða þangað til núverandi leyfissamningur rennur út, hvort sem kemur á undan. Þú getur valið að fara í leyfi Human Resources fyrr ef það sparar kostnað. Frá og með febrúar 2025 verða allir núverandi viðskiptavinir CSP og EA að hætta í einingu Human Resources og kaupa leyfi Human Resources til að geta nýtt sér nýju möguleikana sem verið er að innleiða í Finance and Operations forritin.

### <a name="my-organization-is-live-with-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-will-we-be-required-to-purchase-an-additional-environment-to-support-the-infrastructure-merge"></a>Fyrirtækið mitt er í rauntíma með Dynamics 365 Finance, Supply Chain Management, Commerce eða Project Operations. Þurfum við að kaupa viðbótarumhverfi til að styðja sameiningu tölvukerfisins?

Ekki er gerð krafa um viðbótarumhverfi til að styðja við breytingar á tölvukerfi.

### <a name="where-should-i-go-if-i-have-additional-questions-about-product-licensing"></a>Hvert á ég að snúa mér ef ég er með frekari spurningar um leyfisveitingu vörunnar?

Ef þú hefur spurningar um leyfisveitingar getur þú fundið frekari upplýsingar í [Miðstöð viðskiptaforrita – D365 Verðlagning og leyfisveitingar](https://businessapplications.transform.microsoft.com/resources/pricing-and-licensing?tab=grandfathering). Opnaðu beiðni með LicenseQ ef upplýsingarnar eru ekki að hjálpa til.
