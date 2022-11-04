---
title: Algengar spurningar um flutning viðskiptavinar í Human Resources
description: Þessi grein svarar algengum spurningum um flutning Microsoft Dynamics 365 Human Resources til fjármála og rekstrar sameinaðs innviða.
author: twheeloc
ms.date: 07/06/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0e11d26ebe084762a8616c8aa0aa041a87306473
ms.sourcegitcommit: e25fe4228add88dd37f4f38ece86979e1c621f6a
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/01/2022
ms.locfileid: "9734359"
---
# <a name="human-resources-customer-migration"></a>Flutningur mannauðs viðskiptavina

## <a name="how-should-dynamics-365-human-resources-customers-plan-to-move-to-the-finance-and-operations-infrastructure"></a>Hvernig ætti Dynamics 365 Human Resources hyggjast viðskiptavinir fara yfir í fjármála- og rekstrarinnviði?

Tveir flokkar Microsoft Dynamics 365 Human Resources Viðskiptavinir verða fyrir áhrifum og verða að gera breytingar til að tryggja að þeir séu á nýjustu fjármála- og rekstrarinnviðum:

- Viðskiptavinir sem nota Dynamics 365 Human Resources og eru ekki með önnur rekstrarforrit frá Dynamics 365
- Viðskiptavinir sem nota bæði Dynamics 365 Human Resources og Dynamics 365 Finance,Dynamics 365 Supply Chain Management,Dynamics 365 Commerce, eða Dynamics 365 Project Operations

Óháð því hvaða flokki þeir tilheyra verða viðskiptavinir að færa gögn inn í nýstofnað umhverfi á fjármála- og rekstrarinnviðum og staðfesta að sameiningunni hafi verið lokið.

Framvegis, sem Dynamics 365 Human Resources app mun hafa sitt eigið fjármála- og rekstrarumhverfi sem er aðskilið frá öðrum rekstraröppum. Þannig munu viðskiptavinir geta nýtt sér stækkanleika valkosti án þess að þurfa að sameina núverandi gögn sín. Microsoft mun útvega verkfæri og sandkassaumhverfi sem viðskiptavinir geta notað til að prófa og staðfesta gagnaflutninginn áður en þeir fara í framleiðsluumhverfi. Verkfærin munu gera nánast sjálfvirkt ferli kleift og verða fáanlegt á milli ágúst og nóvember 2022.

Viðskiptavinir sem nota önnur öpp á fjármála- og rekstrarinnviðum munu hafa möguleika á að sameina mannauðsgögn sín við núverandi umhverfi. 

## <a name="when-will-customers-be-moved-to-the-finance-and-operations-infrastructure"></a>Hvenær verða viðskiptavinir fluttir yfir í fjármála- og rekstrarinnviði?

Umskiptin fyrir hvert fyrirtæki munu ráðast af núverandi uppsetningu þess fyrirtækis og reiðubúinn til að fara yfir í fjármála- og rekstrarinnviði. Við mælum með því að viðskiptavinir vinni með Microsoft samstarfsaðila sínum til að ákvarða bestu leiðina áfram.

- Samtök sem nota **Mannauður** mát í Dynamics 365 Finance mun geta virkjað nýja möguleika frá Dynamics 365 Human Resources sem hluti af venjulegu One Version uppfærsluferli. Stefnt er að því að nýir eiginleikar verði almennt fáanlegir frá og með janúar 2022.
- Samtök sem nota Dynamics 365 Human Resources munu hafa aðgang að verkfærum sem þeir geta notað til að ljúka samruna innviða. Microsoft mun vinna með viðskiptavinum við umskiptin til að koma í veg fyrir truflun á þjónustu. Viðskiptavinir munu hafa 12 mánuði til að gera umskiptin, frá þeim tíma þegar flutningstækin verða tiltæk.
- Samtök sem nota bæði Dynamics 365 Human Resources og **Mannauður** mát getur fært sjálfstæða mannauðsinnviði yfir á fjármála- og rekstrarinnviði. Annar valkostur er að nota samrunaverkfærin til að koma umhverfinu í eitt umhverfi. Það er engin krafa eða tímarammi fyrir sameiningu þessara tveggja umhverfi.

Til að fá uppfærðar upplýsingar skaltu skoða reglulega [Gefa út áætlanir](/dynamics365/release-plans/).

## <a name="will-customers-still-need-custom-integrations-between-dynamics-365-human-resources-and-the-human-resources-module"></a>Munu viðskiptavinir enn þurfa sérsniðnar samþættingar á milli Dynamics 365 Human Resources og mannauðseiningunni?

- Viðskiptavinir sem eiga bæði Dynamics 365 Human Resources og önnur innviðaumhverfi fjármála og rekstrar sem nú eru samþætt verða að halda áfram að samþætta þessi tvö umhverfi eftir sameininguna.
- Viðskiptavinir sem kjósa að halda sínu Dynamics 365 Human Resources umhverfi sem er aðskilið frá núverandi fjármála- og rekstrarumhverfi þeirra verður að halda áfram að samþætta umhverfið til að gera gögnin aðgengileg í báðum umhverfi.
- Viðskiptavinir geta haldið áfram að nota Data Integrator til að afrita gögn á milli þessara tveggja umhverfi. Viðskiptavinir sem sameina gögn í eitt umhverfi eftir flutning þurfa ekki lengur að samþætta gögnin, því öll gögn verða í einum gagnagrunni.

## <a name="will-customer-isv-solutions-automatically-be-migrated"></a>Verða ISV lausnir viðskiptavina sjálfkrafa fluttar?

Upplifun flutnings fyrir hverja lausn óháðs hugbúnaðarsala verður breytileg eftir því hver samþættingaraðferð lausnarinnar er. Microsoft mun vinna náið með ISV til að hjálpa til við að veita slétt umskipti yfir í fjármála- og rekstrarinnviði. Margar ISV lausnir eru byggðar á Dataverse með því að nota möguleika á Microsoft Power Platform. Þessar lausnir eru háðar Dataverse sameining milli Dynamics 365 Human Resources umhverfi og Dataverse umhverfi. The Dataverse samþætting er aflögð sem hluti af samruna innviða. Í fjármála- og rekstrarinnviðum er gert ráð fyrir nýjum tvískrifakortum sem koma í stað virkni Dataverse samþættingu.

## <a name="how-will-the-data-integrator-that-moves-data-between-dynamics-365-human-resources-and-other-dynamics-365-apps-be-affected"></a>Hvernig mun Data Integrator sem flytur gögn á milli Dynamics 365 Human Resources og önnur Dynamics 365 forrit verða fyrir áhrifum?

Eftir að viðskiptavinir fara yfir í fjármála- og rekstrarinnviðina verða þeir að halda áfram að samþætta gögn á milli þessara tveggja umhverfi. Viðskiptavinir geta haldið áfram að nota Data Integrator til að framkvæma þessi gagnaflutningsverkefni. Viðskiptavinir sem ætla að halda sínum Dynamics 365 Human Resources umhverfi sem er aðskilið frá núverandi fjármála- og rekstrarumhverfi þeirra mun þurfa að halda áfram að samþætta gögnin á milli umhverfianna tveggja. Fyrir viðskiptavini sem sameina umhverfið tvö í eitt umhverfi verður ekki lengur þörf á samþættingu milli þessara tveggja umhverfi.

## <a name="how-will-data-be-moved-between-dynamics-365-human-resources-on-the-finance-and-operations-infrastructure-and-dataverse-after-the-migration"></a>Hvernig verða gögn flutt á milli Dynamics 365 Human Resources um fjármála- og rekstrarinnviði og Dataverse eftir fólksflutninga?

Núverandi Dataverse sameining á milli Dynamics 365 Human Resources og Dataverse er afskrifað sem hluti af fjármála- og rekstrarinnviðum. Áætlanir eru uppi um að kynna kort með tvöföldum skrifum til að kortleggja fjármála- og rekstrareiningarnar Dataverse borðum. Viðskiptavinir verða að ákveða hvaða kort með tvöföldum skrifum eru nauðsynleg fyrir innleiðingu þeirra. Við mælum með því að sýndartöflur séu notaðar fyrir samþættingu og ISV lausnir, nema það sé sérstök viðskiptaþörf fyrir að gögnin séu afrituð í Dataverse að reka viðskiptarökfræði.

## <a name="how-does-the-migration-affect-dataverse-extensions-for-dynamics-365-human-resources"></a>Hvaða áhrif hefur fólksflutningurinn Dataverse framlengingar fyrir Dynamics 365 Human Resources?

Viðskiptavinir þurfa að flytja í sandkassaumhverfi áður en þeir flytja framleiðsluumhverfi sitt. Þegar viðskiptavinir flytja sandkassaumhverfi sitt verða þeir að búa til afrit af því Dataverse umhverfi til að tengjast nýju fjármála- og rekstrarumhverfinu. Við mælum með því að viðskiptavinur afriti bæði gögnin og lausnirnar fyrir umhverfið, þannig að þær passi við núverandi framleiðsluumhverfi viðskiptavinarins.

Þegar viðskiptavinir eru tilbúnir til að flytja framleiðslu sína Dynamics 365 Human Resources umhverfi mun Microsoft sjálfkrafa flytja gagnagrunninn og Azure Blob geymsluna. Flutti gagnagrunnurinn og geymslan mun vísa nýju umhverfi fjármála- og rekstrarinnviða á sömu framleiðslu Dataverse umhverfi. Áður en hægt er að halda áfram að afrita gögnin til Dataverse, munu viðskiptavinir þurfa að virkja öll tvöfalt skrif kort sem eru nauðsynleg fyrir samþættingu þeirra, viðbætur og ISV lausnir sem eru byggðar á Dataverse.

## <a name="will-microsoft-power-platform-components-that-were-built-for-dynamics-365-human-resources-automatically-work-after-the-infrastructure-migration-is-completed"></a>Will Microsoft Power Platform íhlutir sem voru smíðaðir fyrir Dynamics 365 Human Resources vinna sjálfkrafa eftir að innviðaflutningi er lokið?

Forrit sem eru búin til í Power Apps, flæði sem verða til í Power Automate, og aðrir Microsoft Power Platform sérstillingar eru eins og Dataverse framlengingar. Við flutning á framleiðsluumhverfi viðskiptavina hafa engin áhrif á Dataverse umhverfi, þar með talið allar viðbætur. Forrit, flæði og aðrar sérstillingar á Power Microsoft Platform ættu að halda áfram að virka án þess að þurfa frekari stillingar.

## <a name="what-will-happen-to-dataverse-virtual-table-entities-for-dynamics-365-human-resources-during-the-migration"></a>Hvað verður um Dataverse sýndarborðseiningar fyrir Dynamics 365 Human Resources á meðan á fólksflutningunum stóð?

Þegar viðskiptavinir flytja sína Dynamics 365 Human Resources umhverfi við fjármála- og rekstrarinnviði, umhverfið verður áfram tengt við Dataverse umhverfi sem nú er tengt við Dynamics 365 Human Resources. The Dataverse sýndartöflur sem hafa verið búnar til í umhverfinu munu halda áfram að virka án þess að þurfa frekari stillingar. Sýndartöflurnar gætu þurft að endurnýjast í Dataverse umhverfi sem er tengt núverandi fjármála- og rekstrarumhverfi viðskiptavinar.

## <a name="how-will-an-integration-that-uses-the-applicant-tracking-system-ats-api-payroll-api-dataverse-virtual-tables-for-dynamics-365-human-resources-or-other-entities-in-the-dataverse-web-api-work-after-the-infrastructure-merge-is-completed"></a>Hvernig mun samþætting sem notar umsækjendurakningarkerfi (ATS) API, Payroll API,Dataverse sýndarborð fyrir Dynamics 365 Human Resources, eða öðrum aðilum í Dataverse Vef API vinna eftir að innviðasamruna er lokið?

Þegar viðskiptavinir flytja sína Dynamics 365 Human Resources umhverfi við fjármála- og rekstrarinnviði, umhverfið verður áfram tengt við Dataverse umhverfi sem nú er tengt við Dynamics 365 Human Resources. Allar samþættingar sem voru þróaðar gegn Dataverse Web API mun halda áfram að virka eftir að flutningi er lokið.

## <a name="our-organization-has-configured-custom-security-in-dynamics-365-human-resources-will-it-still-be-applied-after-the-infrastructure-migration-is-completed"></a>Stofnunin okkar hefur stillt sérsniðið öryggi í Dynamics 365 Human Resources. Verður því enn beitt eftir að innviðaflutningi er lokið?

Já, sérsniðnar öryggisstillingar verða innifaldar í gagnaflutningnum.

## <a name="will-workflows-in-dynamics-365-human-resources-automatically-be-migrated"></a>Mun verkflæði inn Dynamics 365 Human Resources sjálfkrafa flutt?

Já, verkflæðisstillingar, verkflæðisferill og núverandi verkflæði í vinnslu verða flutt yfir í sameinaða innviðina.

## <a name="will-saved-views-in-dynamics-365-human-resources-automatically-be-migrated"></a>Vilja vistaðar skoðanir í Dynamics 365 Human Resources sjálfkrafa flutt?

Já, vistaðar skoðanir verða fluttar yfir í sameinaða innviðina.

## <a name="will-features-that-are-enabled-in-dynamics-365-human-resources-automatically-be-available-after-the-infrastructure-merge"></a>Vilja eiginleikar sem eru virkir í Dynamics 365 Human Resources verða sjálfkrafa tiltækar eftir sameiningu innviða?

- Fyrir viðskiptavini sem nota **Mannauður** mát, eiginleikar sem eru aðeins fáanlegir í Dynamics 365 Human Resources verður stjórnað í gegnum eiginleikastjórnun. Venjulega verða þessir eiginleikar ekki virkjaðir sjálfgefið. Allir eiginleikar sem verða að vera virkjaðir sjálfgefið verða skjalfestir.
- Fyrir viðskiptavini sem nota Dynamics 365 Human Resources, eiginleikar verða fáanlegir í innviðunum. Allir eiginleikar sem eru ekki tiltækir verða skjalfestir. Sérhver eiginleikastjórnunarlykill sem er virkur í núverandi Dynamics 365 Human Resources umhverfi verður gert kleift í sameinuðum innviðum. Frekari upplýsingar er að finna í [Eiginleikastjórnunaryfirlit](/fin-ops/get-started/feature-management-overview.md).

## <a name="what-happens-to-byod-databases-during-the-migration"></a>Hvað verður um BYOD gagnagrunna við flutninginn?

Innflutnings- og útflutningsstillingar fyrir koma með eigin gagnagrunn (BYOD) verða fluttar yfir í fjármála- og rekstrarinnviði.

## <a name="is-there-an-impact-on-the-azure-region-when-the-customer-environment-is-migrated"></a>Eru áhrif á Azure svæðinu þegar viðskiptaumhverfið er flutt?

The Dynamics 365 Human Resources umhverfi mun vera á sama Azure svæðinu fyrir flutninginn. Ef það er krafa um að færa umhverfi yfir á annað Azure svæði verða viðskiptavinir að fylgja stöðluðum skrefum til að flytja á nýtt svæði eftir að flutningi er lokið.

## <a name="what-happens-to-azure-data-lakes-during-the-migration"></a>Hvað verður um Azure gagnavötn við flutninginn?

Allur útflutningur sem er stilltur fyrir Azure Data Lake í fjármála- og rekstrarforritum mun halda sömu uppsetningu eftir flutninginn.

> [!NOTE]
> Tvöfalt ritakort verða að vera virkt til að halda áfram að skrifa gögn úr mannauðsumhverfinu inn í Dataverse.

Viðskiptavinir sem vilja flytja mannauðsgögn út í gagnavatnið geta virkjað þennan eiginleika eftir að flutningi yfir í fjármála- og rekstrarinnviði er lokið. Fyrir frekari upplýsingar, sjá [Gagnavötn - Azure Architecture Center](/azure/architecture/data-guide/scenarios/data-lake).

Viðskiptavinir geta tengt mörg fjármála- og rekstrarumhverfi við sama gagnavatnið. Hins vegar mun hvert umhverfi benda á aðra möppu og ílát. Viðskiptavinir sem ætla að sameina umhverfi síðar ættu að skipuleggja nálgun sína vandlega.
 
## <a name="what-migration-will-be-required-if-a-customer-is-currently-using-the-human-resources-module"></a>Hvaða flutnings verður krafist ef viðskiptavinur er að nota mannauðseininguna?

Viðskiptavinir sem nota **Mannauður** eining mun hafa nýja eiginleika virkni frá Dynamics 365 Human Resources beitt á umhverfi sitt með stöðluðu One Version uppfærsluferlinu. Viðskiptavinir geta búist við að sjá nýju virknina í umhverfi sínu þegar þeir verða fáanlegir í hverri uppfærslu. Viðskiptavinir geta notað eiginleikastjórnun til að virkja eiginleikana. Viðskiptavinir ættu að skipuleggja að staðfesta þessa nýju eiginleika með því að nota ferlana sem þeir hafa þegar til staðar og nota til að sannreyna aðrar uppfærslur á umhverfi sínu.

## <a name="what-will-happen-to-custom-integrations-to-external-systems"></a>Hvað verður um sérsniðnar samþættingar við ytri kerfi?

Viðskiptavinir verða að flytja samþættingar sínar yfir í fjármála- og rekstrarumhverfið. Þar sem endapunktur þessa umhverfis er annar gætu viðskiptavinir þurft að uppfæra eða breyta samþættingunum þannig að þær bendi á nýja umhverfið. Þetta verkefni verður fyrst og fremst handvirkt ferli og þær breytingar sem þarf fara eftir arkitektúr samþættingarinnar. Viðskiptavinir ættu að vinna með Microsoft samstarfsaðila sínum til að ákvarða bestu aðferðina til að flytja samþættingar.

## <a name="what-will-happen-to-microsoft-power-platform-dataverse-extensions-if-customers-merge-a-dynamics-365-human-resources-environment-with-an-existing-finance-and-operations-environment"></a>Hvað verður um Microsoft Power Platform (Dataverse) viðbætur ef viðskiptavinir sameinast a Dynamics 365 Human Resources umhverfi með núverandi fjármála- og rekstrarumhverfi?

Ef viðskiptavinir ákveða að sameina a Dynamics 365 Human Resources umhverfi og núverandi fjármála- og rekstrarumhverfi í eitt Dataverse dæmi eftir fólksflutninga, þeirra Dataverse umhverfi verður að sameina sem hluta af samrunaferlinu. Þetta verkefni mun krefjast þess að öll forrit sem eru búin til með því að nota Power Apps, og allar aðrar sérstillingar, vera endurdreifðar í nýja umhverfinu.

## <a name="what-will-happen-to-documents-during-the-migration"></a>Hvað verður um skjöl við flutninginn?

Þegar viðskiptavinir flytja sína Dynamics 365 Human Resources umhverfi við fjármála- og rekstrarinnviði, verða skjölin áfram í núverandi skjalageymslu og verða sjálfkrafa kortlögð í hið nýja umhverfi í fjármála- og rekstrarinnviðum.

Í framtíðarútgáfu verða nýjar gagnaeiningar veittar. Eftir að sú breyting er gerð munu viðskiptavinir sem kjósa að sameina sitt Dynamics 365 Human Resources umhverfi með núverandi fjármála- og rekstrarumhverfi mun þá geta flutt út skjöl og flutt þau inn í núverandi umhverfi.

## <a name="after-the-migration-what-happens-to-the-batch-jobs-that-were-configured-in-dynamics-365-human-resources"></a>Eftir flutninginn, hvað verður um runuvinnslurnar sem voru stilltar í Dynamics 365 Human Resources?

Hópvinnu verður að endurstilla í fjármála- og rekstrarumhverfi. Viðskiptavinir verða að meta hvert lotuverk og bera það saman við núverandi lista yfir lotustörf í fjármála- og rekstrarumhverfi. Viðskiptavinir ættu einnig að greina heildar runuáætlunina þegar þeir sameina tvö sett af runuverkum, til að ákvarða hvort breytingar eigi að gera á runuáætluninni, forgangsröðun eða runuhópum.

## <a name="how-will-the-migration-affect-the-lcs-project-for-dynamics-365-human-resources"></a>Hvaða áhrif mun flutningurinn hafa á LCS verkefnið fyrir Dynamics 365 Human Resources?

Viðskiptavinir verða krafðir um að búa til nýtt Microsoft Dynamics Lifecycle Service (LCS) verkefni, og þeir verða að velja fjármála- og rekstrarforrit sem vöru og **Framkvæmd** sem verkefnistegund. Að auki er nýr reitur fyrir gerð undirverkefna tiltækur þegar LCS verkefni er búið til. Viðskiptavinir verða að velja valkostinn fyrir Dynamics 365 Human Resources flutningur til að flytja núverandi LCS verkefni á sviði starfsmannamála yfir í fjármála- og rekstrarinnviði.

Eiginleikar LCS-verkefna í fjármálum og rekstri eru frábrugðnir eiginleikum LCS-verkefna mannauðs.

Til að fara í loftið þurfa nýir viðskiptavinir að klára eftirfarandi verkefni:

- Ljúktu við inngöngu í verkefni.
- Ljúktu við aðferðafræðina.
- Fylltu út áskriftarmat.
- Ljúktu viðbúningsferlinu til að hefja rekstur.

## <a name="how-will-the-business-process-modeler-be-migrated"></a>Hvernig verður viðskiptaferlislíkanið flutt?

Viðskiptavinir verða krafðir um að flytja út viðskiptaferlislíkanasafn sitt úr Human Resources LCS verkefninu og flytja það inn í fjármála- og rekstrar LCS verkefnið. Að auki verða viðskiptavinir að uppfæra hjálparstillingarnar í forritinu þannig að þeir bendi á nýja LCS verkefnið.

## <a name="how-will-the-service-update-process-be-affected-by-the-migration"></a>Hvernig mun flutningurinn hafa áhrif á þjónustuuppfærsluferlið?

Eftir flutninginn munu viðskiptavinir hafa mun meiri sveigjanleika fyrir umsóknarlífsferilsstjórnun (ALM) og þjónustuuppfærslur. Þjónustuuppfærslur verða ekki lengur sjálfkrafa beittar í mannauðsumhverfi. Þess í stað mun þjónustan fylgja One Version þjónustuuppfærsluferlum og virkni, og stillingarvalkostir fyrir uppfærslur í gegnum LCS verða virkjaðir.

## <a name="will-customers-be-eligible-for-fasttrack-assistance-with-the-infrastructure-merge"></a>Verða viðskiptavinir gjaldgengir fyrir FastTrack aðstoð við samruna innviða?

Microsoft er enn að skilgreina hvaða verkfæri og úrræði verða tiltæk frá FastTrack til að hjálpa við sameininguna.

## <a name="licensing-impact"></a>Áhrif á leyfisveitingar

Fyrir frekari upplýsingar um hvernig leyfisveiting hefur áhrif, sjá [Dynamics 365 Human Resources sameining innviða](hr-infrastructure-merge.md#licensing).
