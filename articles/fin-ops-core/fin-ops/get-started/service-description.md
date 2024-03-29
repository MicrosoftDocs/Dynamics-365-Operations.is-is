---
title: Þjónustulýsing fyrir fjármála- og reksturs-forrit
description: Þessi grein inniheldur þjónustulýsingar fyrir forrit fjármála- og reksturs.
author: tomhig
ms.date: 04/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: whigginb
ms.search.validFrom: 2021-09-03
ms.openlocfilehash: 9e5160cc3961703475ffb8dc4a4daf2ae872aaba
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/06/2022
ms.locfileid: "9124926"
---
# <a name="service-description-for-finance-and-operations-apps"></a>Þjónustulýsing fyrir fjármála- og reksturs-forrit

[!include[banner](../includes/banner.md)]

Forrit fjármála- og reksturs eru bókhalds- og áætlunargerðarhugbúnaður fyrir SaaS-þjónustum sem eru byggðar upp á og fyrir [Microsoft Azure](https://azure.microsoft.com/overview/what-is-azure/). fjármála- og reksturs-þjónustan veitir stofnunum/fyrirtækjum virkni bókhalds- og áætlunargerðarhugbúnaðar sem styður einstakar kröfur þeirra og hjálpar þeim að laga sig að síbreytilegu viðskiptaumhverfi, án þess að gera kröfu um að þeir sjái um tölvukerfi. Forrit fjármála- og reksturs geta innihaldið eitt eða fleiri af eftirfarandi lausnasvæðum:

- [Dynamics 365 Finance](/dynamics365/finance/)
- [Dynamics 365 Human Resources](/dynamics365/human-resources/)
- [Dynamics 365 Supply Chain Management](/dynamics365/supply-chain/)
- [Dynamics 365 Commerce](/dynamics365/commerce/)
- [Dynamics 365 Project Operations](/dynamics365/project-operations/)

Með [viðskiptagreind](/power-bi/fundamentals/power-bi-service-overview), [tölvukerfi](https://azure.microsoft.com/global-infrastructure/), [reikningsgetu](/azure/service-fabric/service-fabric-overview) og [gagnagrunnsþjónustum](https://devblogs.microsoft.com/azure-sql/running-1m-databases-on-azure-sql-for-a-large-saas-provider-microsoft-dynamics-365-and-power-platform/) gera þessi forrit stofnunum/fyrirtækjum kleift að keyra iðnaðar- og rekstrarferli. Viðskiptavinir, með stuðningi innleiðingaraðila, ákvarða stillingar á rökum viðskiptaforritsins sem henta best einstökum viðskiptaferlum þeirra. Hægt er að auka eða lengja virkni og viðskiptaferli með einni eða fleiri af eftirfarandi lausnum:

- Innbyggð [sérsniðna upplifun](personalize-user-experience.md)
- [Microsoft Power Platform](../../dev-itpro/power-platform/overview.md)-verkfæri
- [Sjálfvirkni byggð á Visual Studio](https://visualstudio.microsoft.com) [fjármála- og reksturs-hugbúnaðarþróunarpakka (SDK)](../../dev-itpro/dev-tools/developer-home-page.md) og [Azure DevOps-smíði](../../dev-itpro/dev-tools/developer-home-page.md#build-automation-using-azure)
- Lausnir óháðs hugbúnaðarsala frá [AppSource](https://appsource.microsoft.com/partners)

Út frá þessum kröfum velja viðskiptavinir sína lausn. Þeir vinna með innleiðingaraðila sínum til að skilgreina, þróa og prófa lausn sína með því að nota tólin og bestu starfsvenjurnar sem veittar eru í [Microsoft Dynamics Lifecycle Services (LCS)](../../dev-itpro/lifecycle-services/lcs.md). Það eru fjórar algengar aðstæður:

- Venjuleg skilgreining fjármála- og reksturs-forrita beint úr kassanum (engar viðbætur)
- Forritastilling fjármála- og reksturs sem inniheldur eina eða fleiri lausnir óháðra hugbúnaðarsala
- Grunnstilling forrit fjármála- og reksturs sem inniheldur eina eða fleiri viðbætur sem eru sértækar fyrir viðskiptavini
- Forritsstilling fjármála- og reksturs sem inniheldur samsetningu viðbóta frá viðskiptavini og einnar eða fleiri lausna óháðra hugbúnaðarsala

Stofnanir/fyrirtæki geta jafnað vöxt rekstrarins með því að bæta notendum og viðskiptaferlum auðveldlega við með einföldu, gagnsæju áskriftarlíkani. Frekari upplýsingar eru í [Leiðbeiningar fyrir Dynamics 365-leyfi](https://www.microsoft.com/licensing/docs/view/Microsoft-Dynamics-365).

## <a name="operating-model"></a>Vinnslulíkan

Rekstrarlíkan fjármála- og reksturs-forrita skilgreinir tiltekin hlutverk og ábyrgð fyrir viðskiptavininn, innleiðingaraðila og Microsoft á öllu líftíma þjónustunnar. Frekari upplýsingar er að finna í [Aðgerðir og þjónusta í skýi](../../dev-itpro/lifecycle-services/cloud-operations-servicing.md).

### <a name="customer-activities"></a>Verkþættir viðskiptavinar

Viðskiptavinir vinna með samstarfsaðila sínum og [Microsoft FastTrack](/dynamics365/fasttrack/) með því að fylgja [Leiðbeiningar fyrir innleiðingu Dynamics 365](https://community.dynamics.com/365/dynamics-365-fasttrack/p/dynamics365implementationguide), rammanum [Success by Design](/dynamics365/fasttrack/success-by-design-overview) og nota verkfæri og sniðmát fyrir bestu starfsvenjur sem veitt eru í [Lifecycle Services](../../dev-itpro/lifecycle-services/lcs.md) til að innleiða lausn sína. Almennar aðgerðir eru m.a.:

- Notandaauðkenni og öryggisstjórnun
- Skilgreina, þróa og reka viðskiptaferla
- Skilgreina, þróa, prófa og nota viðbætur
- Fylgjast með og stjórna útfærslum sem ekki tengjast framleiðslu
- Stjórna uppfærslum forrits og sannprófa viðbætur
- Hafa umsjón með lausnum óháðra hugbúnaðarsala og samþættingum þriðju aðila

### <a name="microsoft-responsibilities"></a>Skyldur Microsoft

Microsoft hefur umsjón með fjármála- og reksturs-þjónustunni með því að innleiða, hafa virkt eftirlit með og þjónusta sandkassa- og framleiðsluumhverfi viðskiptavina í Microsoft SaaS-áskriftinni. Þessi stjórnun felur í sér að úthluta nauðsynlegum tölvukerfum til að keyra þjónustuna og eiga í framvirkum samskiptum við viðskiptavini um ástand þjónustunnar. Ábyrgð nær til:

**Stjórnun tölvukerfa**
- Öryggi og einangrun
- Stýrikerfi og sýndartækni
- Þjónar, geymsla og nettenging
- Gagnamiðstöðvarafl, nettenging, kæling

**Stjórnun forritsverkvangs**
- Eftirlit og tilkynningar fyrir forrit allan sólarhringinn
- Greiningar, uppfærslur á verkvangi, bætur, uppfærslur á þjónustu
- Leiðir umsókna, álagsjöfnun, afritun svæðis
- Úthlutun og stjórnun umhverfis
- Gagnagrunnsstjórnun, mikið framboð/endurheimt eftir hamfarir, umfang, aðgerðir
- Reikna uppsetningu, stækka, minnka

## <a name="system-configuration"></a>Kerfisgrunnstilling

Stærð forrita fjármála- og reksturs eftir færslumagni og notkun. Hver innleiðing viðskiptavinar skapar einstaka lausn sem samanstendur af eftirfarandi þáttum:

- **Gagnasamsetning** – Einstakt sett af færibreytum sem stýra hegðun, skipulagi stofnunar/fyrirtækis, uppbyggingu aðalgagna (eins og fjárhags- og birgðavíddir) og rekjanleika færslna.
- **Viðbót og stilling** – Viðbótaleiðir sem nota kóðaviðbætur, ISV-lausnir og einstakar stillingar sem fela í sér vinnuflæði, samþættingar og skýrslugerðarstillingar.
- **Notkunarmynstur** – Einstök samsetning net- og lotunotkunar, ásamt möguleikanum á að samþætta við upp- og niðurstreymiskerfi fyrir sameinað gagnaflæði og getu til að aðgreina á grundvelli upplýsingasýna sem viðskiptavinir nota í viðskiptaferlum sínum.

Microsoft stillir framleiðsluumhverfi viðskiptavina sem eru stærðarflokkuð til að ráða við færslumagn og samkeyrslu notenda. Microsoft ber ábyrgð á eftirfarandi verkum:

- Rétt úthlutun tilfanga framleiðsluumhverfis, byggt á upplýsingum viðskiptavinarins í [LCS-áskriftarmatstækinu](../../dev-itpro/lifecycle-services/subscription-estimator.md)
- Stöðugt eftirlit og greining á þjónustuframboði framleiðsluumhverfa
- Vandamál við greiningu og bilanagreiningu á afköstum kerfisins með forritum fjármála- og reksturs

Til að tryggja að innleiðing sé stillt með tilliti til mikilla afkasta verða viðskiptavinir að ljúka þessum verkum:

- Gefa réttar notkunarupplýsingar um fjármála- og reksturs-innleiðingu í [LCS-áskriftarmatstækinu](../../dev-itpro/lifecycle-services/subscription-estimator.md).
- Smíða- og prufuviðbætur fyrir afköst og umfang.
- Prófa gagnastillingar rétt vegna afkasta.
- Gakktu úr skugga um skalanleika með því að gera [afkastapróf](https://community.dynamics.com/365/b/techtalks/posts/performance-testing-approach-april-30-2018) áður en keyrsla fer í gang.

## <a name="onboarding-and-implementation"></a>Innleiðing og framkvæmd

Eftirfarandi tafla sýnir dæmigerða atburði við innleiðingu og framkvæmd þeirra.

| Beiðni | Væntanleg Microsoft-aðgerð | Áætlaðar aðgerðir viðskiptavinar/samstarfsaðila í innleiðingu |
|---|---|---|
| Upphaflegt kauptilboð | LCS-verk er búið til eftir að tilboðið er keypt, byggt á tilviki sem viðskiptavinurinn setur af stað. | Farið í gegnum [viðskiptaferli](before-you-buy.md) samnings við fyrirtæki (EA) eða skýjalausnaveitu (CSP). Samstarfsaðilinn býr til leigjanda fyrir viðskiptavininn, ef við á. |
| Viðbótarkaup | Veita viðskiptavini aðgang að viðbótinni sem er valin meðan á innleiðingu stendur. | Ekki tiltækt |
| Innleiðing áætlanagerðar og greiningar | Veita viðeigandi verkfæri í LCS, svo sem [viðskiptaferlavinnslu](../../dev-itpro/lifecycle-services/bpm-overview.md) og [samvirkni við Azure DevOps](../../dev-itpro/lifecycle-services/synchronize-bpm-vsts.md). | Gera verkáætlun, setja upp Azure DevOps, ljúka innleiðingu og setja upp stjórnendareikninga. |

Frekari upplýsingar er að finna í [Innleiðing innleiðingarverks](../imp-lifecycle/onboard.md).

## <a name="globalization"></a>Staðfæring

Forrit fjármála- og reksturs eru veitt frá nokkrum Azure svæðum um allan heim. Forrit fjármála- og reksturs veita virkni til að styðja við mismunandi lönd/svæði og móðurmál. Frekari upplýsingar er að finna [Staðfærslu- og eftirlitseiginleikar](../../dev-itpro/lcs-solutions/country-region.md#localization-and-regulatory-features).

### <a name="countryregion-specific-considerations"></a>Atriði sem varða tiltekið land/svæði

- Viðskiptavinir í eftirlitsskyldum iðnaði eða viðskiptafélögum sem eiga viðskipti við aðila í Frakklandi sem gera kröfu um búsetu á staðnum ættu að fara yfir gögn [fjármála- og reksturs í Frakklandi](../../dev-itpro/deployment/france-local-deployment.md).
- Viðskiptavinir með starfsemi í Kína ættu að yfirfara [Azure China Playbook](/azure/china/) og [Fjármála- og reksturs operated by 21Vianet in China](../../dev-itpro/deployment/china-local-deployment.md).
- Viðskiptavinir sem eru með starfsemi í Rússlandi ættu að fara yfir [rússnesk lög um staðfærslu persónuupplýsinga](/business-applications-release-notes/october18/dynamics365-finance-operations/russian-regulations-on-prem#when-will-the-cloud-deployment-option-of-dynamics-365-for-finance-and-operations-be-generally-available-for-russia).

### <a name="general-data-protection-regulation-gdpr"></a>Almenna persónuverndarreglugerðin (GDPR)

Fyrir forrit fjármála- og reksturs virkar Microsoft sem vinnsluminni. Sem gagnavinnsluaðili veitir fjármála- og reksturs ferli og eiginleika sem hjálpa viðskiptavinum að uppfylla skyldur GDPR sem ábyrgðaraðili gagna. Frekari upplýsingar er að finna í [GDPR-yfirlit](../../dev-itpro/gdpr/gdpr-guide.md).

## <a name="environment-and-data-management"></a>Umhverfi og gagnastjórnun

Í þessum hluta er lýst dæmigerðu umhverfi og gagnaumsjónartilvikum sem eiga sér stað í þjónustunni.

### <a name="environment-and-data-management-events-for-production-instances"></a>Umhverfis- og gagnastjórnunarviðburðir fyrir framleiðslutilvik

LCS veitir [sjálfsafgreiðsluverkfæri](../../dev-itpro/deployment/infrastructure-stack.md) og [gagnagrunnsaðgerðir](../../dev-itpro/database/dbmovement-operations.md) sem eru notuð til að sinna verkefnum í umhverfi og gagnaumsýslu. Hér eru nokkur dæmi:

**Viðburður:** [Óskað eftir framleiðslutilviki](../imp-lifecycle/go-live-faq.md#when-can-i-configure-and-request-my-production-environment)

- Fyllið út [Yfirferð Go-live Readiness](../imp-lifecycle/prepare-go-live.md) og sendið hann til starfsfólks [Microsoft FastTrack](/dynamics365/fasttrack/).
- Fylltu út [LCS-áskriftarmatstækið](../../dev-itpro/lifecycle-services/subscription-estimator.md) áður en þú biður um framleiðslutilvik.
- Ljúka öllum innleiðingarverkefnum sem tilgreind eru í [LCS aðferðafræðinni](../../dev-itpro/lifecycle-services/create-methodology.md).

**Viðburður:** [Afritun sandkassagagnagrunns í framleiðslutilvik](../../dev-itpro/database/dbmovement-scenario-goldenconfig.md)

- Gert fyrir skipti yfir í hermikeyrslu eða raunkeyrslu.

**Tilvik:** [Viðhaldsstilling](../../dev-itpro/sysadmin/maintenance-mode.md)

1. Kveikja á viðhaldsstillingu í LCS.
2. Ljúka við áskilið viðhald.
3. Slökkva skal á viðhaldsstillingu í LCS.

### <a name="environment-and-data-management-events-for-non-production-instances"></a>Umhverfis- og gagnaumsjónarviðburðir fyrir tilvik sem ekki tengjast framleiðslu

LCS veitir [sjálfsafgreiðsluúthlutun](../../dev-itpro/deployment/infrastructure-stack.md) og [gagnagrunnsaðgerðir](../../dev-itpro/database/dbmovement-operations.md) sem eru notuð til að sinna verkefnum í umhverfi og gagnaumsýslu. Hér eru nokkur dæmi:

**Viðburður:** [Uppsetning nýs sandkassatilviks](../../dev-itpro/deployment/deployenvironment-newinfrastructure.md)

- Gangið úr skugga um að öll nauðsynleg tilvik hafi verið [skipulögð](../imp-lifecycle/environment-planning.md) og að viðeigandi viðbótatilboð hafi verið keypt.
- Keyrið uppsetningarferli í LCS.
- Kláraðu öll verkefni sem eru tilgreind í gátlistum LCS.
    
>[!NOTE]
>Þróunarumhverfi fyrir sandkassa er sýndarvél (VM) sem er [sett inn á Azure-áskrift viðskiptavinar](../../dev-itpro/dev-tools/access-instances.md) og stjórnað af viðskiptavini.

**Viðburður:** [Afritun gyllts grunnstillingagagnagrunns frá sandkassa til framleiðslu](../../dev-itpro/database/dbmovement-scenario-goldenconfig.md)

- Gert fyrir skipti yfir í hermikeyrslu eða raunkeyrslu.

**Viðburður:** [Endurheimt tímapunktsafrits framleiðslu í tilvik sem ekki tengist framleiðslu](../../dev-itpro/database/database-pitr-prod-sandbox.md)

- Keyra [Uppfæra gagnagrunn](../../dev-itpro/database/database-refresh.md) í LCS.
- Eftir afritun: Eyða eða loka á viðkvæm gögn með forskriftum, aðlaga umhverfissértækar stillingar forrita (svo sem endapunkta samþættingar) og virkja eða bæta við notendum. Athugaðu að þessar breytingar eru gerðar með því að nota [gagnapakka](../../dev-itpro/data-entities/data-entities-data-packages.md#import-a-data-package).

**Atburður:** [Endurheimt gagnagrunns tilvika sem ekki tengjast framleiðslu](../../dev-itpro/database/database-point-in-time-restore.md)

- Samþykkja að ekki sé hægt að afturkalla ferlið.
- Keyra endurheimt tímapunkts í LCS.

**Tilvik:** Afritun lags 2 sandkassa gagnagrunns í þróunarsandkassa fyrir úrræðaleit og [kembingu](../../dev-itpro/database/dbmovement-scenario-debugdiag.md)

- Keyra gagnagrunnsútflutningsaðgerðina í LCS á lag 2 sandkassaumhverfinu.
- Flytja inn og uppfæra gagnagrunninn í þróunarumhverfinu.

## <a name="data-backup-and-retention"></a>Öryggisafrit og varðveisla gagna

Gagnagrunnar fyrir umhverfi fjármála- og reksturs í SaaS-áskriftinni eru varðir með sjálfvirkum öryggisafritum. Í framleiðsluumhverfi eru sjálfvirk öryggisafrit geymd í 28 daga, nema Microsoft sé með öryggisafrit. Fyrir umhverfi sandkassa (lag 2+) eru þeir geymdir í sjö daga. Hægt er að endurheimta framleiðsluumhverfi ef bilun kemur upp við áætlaða viðhaldsuppfærslu.

Frekari upplýsingar um sjálfvirk öryggisafrit eru í [Sjálfvirk öryggisafrit - Azure SQL-gagnagrunnur & SQL-stjórnað tilvik](/azure/azure-sql/database/automated-backups-overview?tabs=single-database).

## <a name="service-activity-responsibilities"></a>Þjónustuverkþáttarábyrgð

Eftirfarandi tafla lýsir dæmigerðum aðstæðum og starfsemi þjónustunnar. Einnig kemur fram hvort Microsoft, viðskiptavinurinn, eða bæði Microsoft og viðskiptavinurinn bera ábyrgð á starfseminni.

| Aðgerð | Ábyrgð Microsoft | Ábyrgð viðskiptavinar |
|---|---|---|
| **Úthlutun fyrstu leigjenda** | | |
| Stærð áætlaðs álags í LCS með því að nota áskriftarmatstækið og óska eftir því að tiltekið umhverfi sé útvegað. | | X |
| Úthluta öllum framleiðslutilvikum og tilvikum sem tengjast ekki framleiðslu. | X | |
| Sannreyna uppsett framleiðslutilvik og tilvik sem ekki tengjast framleiðslu. | | X |
| **Þjónustuuppfærslur** | |
| Notið þjónustuuppfærslur á tilgreind tilvik sem tengjast ekki framleiðslu sem og framleiðslutilvik. | X | |
| Komdu á þjónustuuppfærslum handvirkt úr LCS í sandkassatilfelli. Skilgreindu, þróaðu og prófaðu uppfærsluna og færðu uppfærslupakka kóðans aftur í LCS. | | X |
| Óska eftir og tímasettu hvenær uppfærslur viðbóta verða notaðar í framleiðslutilvikið. | | X |
| Búa til kóða og taka öryggisafrit af gögnum fyrir framleiðslutilvikið áður en uppfærslur eru gerðar. | X | |
| Ef um bilun er að ræða skal endurheimta framleiðslutilvikið með kóðanum og öryggisafritinu. | X | |
| **Stjórnun gagna (taka öryggisafrit, endurheimta og uppfæra)** | | |
| Gerið öryggisafrit af gagnagrunninum. | X | |
| Ákveðið mikið framboð og viðbragðsáætlun vegna hamfara. | X | |
| Fylgjast með afköstum gagnagrunns framleiðslutilvika. | X | |
| Stillið gagnagrunn framleiðslutilvika fyrir afköst. | X | |
| Framkvæmdu uppfærslu á tímapunkti í gagnagrunni framleiðslutilviks í tilviki sem er ekki framleiðslutilvik. | | X |
| **Uppfærsla tölvukerfa** | | |
| Skipuleggja reglulegar uppfærslur á tölvukerfi. | X | |
| **Stækka og minnka (notendur, geymsla og tilvik)** | | |
| Kaupa viðbótarnotendur og viðbætur sem ekki tengjast framleiðslu. | | X |
| Uppfæra breytingar á notkun í LCS-áskriftarmatstækinu. | | X |
| Tilkynntu um veruleg afkastavandamál sem hafa áhrif á notkun þjónustunnar. | | X |
| Stjórnið tilföngum sem eru nauðsynleg fyrir viðeigandi þjónustu. | X | |
| Rannsaka og bilanagreina atvik. | X | |
| **Öryggi (aðgangur notanda)** | | |
| Veita notanda aðgang að þjónustunni. | | X |
| Veita LCS-verki aðgang að stjórnun og virkni tilvika sem voru sett upp í gegnum LCS. | | X |
| **Fylgjast með framleiðslutilvikum** | | |
| Fylgjast með framleiðslutilvikum allan sólarhringinn. | X | |
| Tilkynnið viðskiptavinum um atvik sem tengjast framleiðslutilvikinu. | X | |
| **Umsjón og eftirlit með tilvikum sem ekki tengjast framleiðslu** | | |
| Hafa umsjón með tilvikum sem ekki tengjast framleiðslu með því að nota LCS. | | X |
| Fylgjast með tilvikum sem ekki tengjast framleiðslu. | | X |

## <a name="service-update-strategy"></a>Þjónustuuppfærsluáætlun

Í samræmi við [reglur um stuðningstíma hugbúnaðar](../../dev-itpro/migration-upgrade/versions-update-policy.md) fylgja forrit fjármála- og reksturs [Modern-reglum Microsoft um stuðningstíma](../../dev-itpro/migration-upgrade/versions-update-policy.md#modern-lifecycle-policy), sem nær yfir vörur sem eru stöðugt þjónustaðar og studdar. 

Microsoft gefur út átta þjónustuuppfærslur á forrit fjármála- og rekstursum á hverju ári á eftirfarandi mánuðum:

- janúar
- febrúar
- apríl
- maí
- júlí
- ágúst
- október
- nóvember

>[!NOTE]
>Apríl og október eru mikilvæg útgáfutímabil. Viðskiptavinir geta gert hlé á einstökum þjónustuuppfærslum í allt að þrjár samfelldar uppfærslulotur.

Frekari upplýsingar er hægt að finna í eftirfarandi efnisatriðum:

- [Yfirlit yfir þjónustuuppfærslur fyrir One Version](../../dev-itpro/lifecycle-services/oneversion-overview.md)
- [Skilgreina þjónustuuppfærslur í gegnum LCS](../../dev-itpro/lifecycle-services/configure-service-updates.md)
- [Gera hlé á þjónustuuppfærslum í gegnum LCS](../../dev-itpro/lifecycle-services/pause-service-updates.md)
- [Fá tilkynningar um þjónustuuppfærslur í gegnum LCS](../../dev-itpro/lifecycle-services/notifications-service-updates.md)
- [Regression-prófunarverkfæri til að staðfesta þjónustuuppfærslur](../../dev-itpro/perf-test/rsat/rsat-overview.md)
- [Dynamics 365 leiðarvísir og útgáfutímabil](https://dynamics.microsoft.com/roadmap/overview/)

## <a name="security-and-administrative-access"></a>Öryggi og stjórnunaraðgangur

Stjórnunaraðgangi framleiðsluumhverfi fjármála- og reksturs er stranglega stýrt og hann skráður. Gögn um viðskiptavini eru meðhöndluð í samræmi við [skilmála Microsoft Online Services](https://www.microsoft.com/licensing/terms/productoffering). 

### <a name="customer-administrative-access"></a>Stjórnunaraðgangur viðskiptavinar

Stjórnandi leigjanda hjá viðskiptavini getur fengið aðgang að framleiðslutilvikum eða tilvikum sem ekki eru framleiðslutilvik, eins og lýst er í eftirfarandi töflu:

| Gerð umhverfis | Notkun | Aðgangsstig viðskiptavinar |
|---|---|---|
| **Ekki framleiðsla**<br>Lag 1 sandkassi | Umhverfi sem ekki tengist framleiðslu sem viðskiptavinir setja upp í þróunar-, sýningar- eða þjálfunarskyni. | Lag 1 sandkassi (einnig nefnt skýjahýst umhverfi) er sýndarvél sem viðskiptavinur stjórnar sem er sett upp á Azure-áskrift viðskiptavinarins frá LCS. Þar sem um sýndarvél á Azure-áskrift viðskiptavinarins er að ræða hefur viðskiptavinurinn fullan stjórnunaraðgang að umhverfinu í gegnum fjartengt skjáborð. |
| **Ekki framleiðsla**<br>Lag 2 (eða hærra) sandkassi | Framleiðsluumhverfi sem ekki tengist framleiðslu sem viðskiptavinir setja upp fyrir samþykkisprófun notanda, prófanir á samþættingu, þjálfun, sviðsetningu eða aðrar aðstæður fyrir framleiðslu. | Lag 2 og hærri sandkassar eru settir í fjármála- og reksturs SaaS-þjónustuáskriftina. Aðgangur að Azure SQL-gagnagrunnum sem eru tengdir umhverfi sem ekki tengist framleiðslu er veittur með [samtímaaðgangi](../../dev-itpro/database/database-just-in-time-jit-access.md). Aðgangur í gegnum fjartengt skjáborð er ekki í boði. |
| **Framleiðsla** | Framleiðsluumhverfi er tekið í notkun þegar verkið er [tilbúið fyrir fyrstu keyrslu](../imp-lifecycle/environment-planning.md#production-system-readiness). | Framleiðsluumhverfi er sett upp á SaaS-áskriftina. Allur aðgangur er í gegnum vafra, endastöðvar þjónustu eða LCS. |

### <a name="microsoft-administrative-access"></a>Microsoft-stjórnunaraðgangur

Eftirfarandi tafla sýnir mismunandi stig aðgangs fyrir mismunandi Microsoft-stjórnendur:

| Kerfisstjóri | Gögn viðskiptavinar |
|---|---|
| Operations-viðbragðsteymi<br>(Aðeins takmarkað við lykilstarfsmenn) | Aðgangur er veittur í gegnum þjónustubeiðni. Aðgangur er endurskoðaður og takmarkaður við þann tíma sem stuðningsaðgerðin varir. |
| Notendaþjónusta Microsoft (CSS) | Enginn beinn aðgangur. Viðskiptavinur getur notað skjádeilingu til að vinna með starfsfólki þjónustuvers við að leysa vandamál. |
| Hönnun | Enginn beinn aðgangur. Operations-viðbragðsteymið getur notað skjádeilingu til að vinna með þróunardeild við að leysa vandamál. |
| Aðrir í Microsoft | Enginn aðgangur. |

## <a name="monitoring"></a>Eftirlit

Microsoft hefur fjárfest í umfangsmiklu verkfærasetti til að fylgjast með og greina framleiðslutilvik viðskiptavina. Microsoft vaktar framleiðsluumhverfi viðskiptavina allan sólarhringinn, alla daga vikunnar. Frekari upplýsingar er að finna í [Stuðningur og eftirlit með framleiðslu](../imp-lifecycle/production-support-monitoring.md).

| Skyldur Microsoft | Skyldur viðskiptavina |
|---|---|
| <ul><li>Vakta framboð þjónustu.</li><li>Stöðug vöktun og viðvaranir í gegnum ástandsmælingar og vöktun mikilvæga þátta eins og AOS-þjón hugbúnaðarhluta, lotu, gagnainnflutnings-/útflutningsramma (DIXF), Commerce og Management Reporter.</li><li>Fylgjast með afkastaminnkun vegna tölvukerfaþjónustu (svo sem Azure Active Directory \[Azure AD\] og Azure SQL).</li><li>Ef Microsoft kemst að þeirri niðurstöðu að eitt ferli eða runuvinnsla valdi frávikum verður því ferli eða vinnslu hætt eftir samskipti við viðskiptavininn.</li></ul> | <ul><li>Fylgjast með breytingum á forritastillingum og viðbótum sem geta valdið vandamálum varðandi virkni og afköst.</li><li>Forritsvillur þarf að greina með því að nota eftirlitstækin. Þessi verkfæri eru notuð til að greina afkastafrávik sem notendur greina frá.</li><li>Láta Microsoft vita ef búist er við að álag verði á kerfinu umfram áætlaða hámarksnotkun.</li><li>Ef viðeigandi þjónusta er ekki tiltæk í framleiðslutilviki getur viðskiptavinur notað LCS til að tilkynna um [framleiðslustöðvun](../../dev-itpro/lifecycle-services/report-production-outage.md).</li></ul> |

Með því að senda inn þjónustubeiðnir á netinu, um LCS, gera viðskiptavinir Microsoft fyrirtækinu kleift að bjóða upp á hraða og yfirgripsmikla tæknilega sérþekkingu á sem árangursríkastan og skilvirkastan hátt. Þrátt fyrir að hægt sé að nota síma ætti aðeins að nota hann ef þjónustan er ekki tiltæk á netinu. Frekari upplýsingar er að finna í [Stuðningsvalkostir í síma](/power-platform/admin/support-overview?toc=%2Fdynamics365%2Ffin-ops-core%2Fdev-itpro%2Ftoc.json&bc=%2Fdynamics365%2Fbreadcrumb%2Ftoc.json#is-there-a-phone-number-i-can-call-to-contact-support).

## <a name="incident-management"></a>Tilvikastjórnun

Microsoft bregst við og lagar atvik miðað við alvarleikastig. Hægt er að breyta alvarleika atvika hjá Microsoft við upphaflegt mat á atvikinu og eftir því sem meiri upplýsingar eru í boði um áhrifin og umfang þeirra. Ef dregið er úr atviki helst alvarleiki þess óbreyttur.

Frekari upplýsingar varðandi alvarleikastig eru í [þessari alvarleikatöflu](/power-platform/admin/support-overview#what-is-initial-response-time-and-how-quickly-can-i-expect-to-hear-back-from-someone-after-submitting-my-support-request).

## <a name="business-continuity-through-high-availability-and-disaster-recovery"></a>Samfella í rekstri með miklu framboði og endurheimt eftir hamfarir 

Microsoft býður upp á samfellu í rekstri og endurheimt eftir hamfarir vegna framleiðslutilvika fjármála- og reksturs-forrita ef bilun verður í Azure innan svæðis. Frekari upplýsingar, þ.m.t. RTO (Recovery Time Objective) og RPO (Recovery Point Objective), er að finna í [Rekstrarsamfella og endurheimt eftir áföll](../../dev-itpro/sysadmin/business-continuity-disaster-recovery.md).

- **Mikið framboð** – Virknin „Mikið framboð“ býður upp á leiðir til að koma í veg fyrir stöðvun sem stafar af bilun í einum hnút í Azure-gagnaveri. Uppbygging skýs hvers þjónustusvæðis notar Azure-framboðs fyrir tölvulagið til að koma í veg fyrir atburði vegna afmarkaðrar bilunar. HA fyrir gagnagrunna er veitt í gegnum [Azure SQL HA eiginleika](/azure/azure-sql/database/high-availability-sla).
- **Endurheimt vegna hamfara** – [Azure-endurheimtareiginleikar vegna hamfara](/azure/best-practices-availability-paired-regions) vernda hverja þjónustu gegn bilunum sem hafa víðtæk áhrif á alla Azure-gagnamiðstöðina. Hér eru nokkrir þessara eiginleika:

    - Azure SQL active-geo afritun fyrir aðalgagnagrunn (viðskiptagagnagrunnur).
    - Landfræðileg afrit af Azure Blob Storage (sem inniheldur fylgiskjöl í viðhengi) á öðrum Azure svæðum.
    - Aukasvæði fyrir Azure SQL- og Azure Blob Storage-afritanir.

Ef endurheimt eftir hamfarir er notuð til að endurheimta framleiðslutilvik viðskiptavinarins munu Microsoft og viðskiptavinurinn uppfylla skyldur sínar varðandi [stjórnun atvika](service-description.md#incident-management).

Endurheimtuáætlanir og verklagsreglur Microsoft vegna hamfara eru skoðaðar reglulega með endurskoðun á kerfi og skipulagi (SOC). Þessar úttektir bera vott um tæknilegt og verklag við DR-endurskoðun Microsoft, þar á meðal Dynamics 365 fjármála- og rekstrarforrit. [Úttektarskýrslur](/compliance/regulatory/offering-soc-2) og allar aðrar reglufylgniskýrslur eru aðgengilegar í [Microsoft Trust Center](/compliance/regulatory/offering-home).

## <a name="finance-and-operations-support-offerings"></a>Þjónustutilboð fyrir fjármál- og rekstur

Tæknileg aðstoð er í boði á mörkuðum þar sem boðið er upp á fjármála- og reksturs-þjónustu. [Stuðningsupplifanir](../../dev-itpro/lifecycle-services/lcs-support.md) eru veittar í LCS eða forritum fjármála- og reksturs. Hér eru nokkur dæmi:

- [Vandamálaleit](../../dev-itpro/lifecycle-services/issue-search-lcs.md) í LCS
- [Samþættur tæknilegur stuðningur](../../dev-itpro/lifecycle-services/support-experience.md) í forritum fjármála- og reksturs
- [Stuðningur í skýi](../../dev-itpro/lifecycle-services/cloud-powered-support-lcs.md) í LCS

Microsoft býður fjármála- og reksturs-viðskiptavinum upp á þrjár þjónustuáætlanir: Premier, Professional Direct og þann stuðning sem er innifalinn í áskriftinni. Stuðningsstigið fer eftir áskriftum. Eftirfarandi tafla sýnir samanburð á áskriftarleiðunum þremur.

| Studdur eiginleiki | Premier-samningur | Professional Direct | Áskrift |
|---|---|---|---|
| Ótakmörkuð innsending bilana/lagfæringa | Já | Já | Já |
| Sólarhringsaðgangur í gegnum LCS | Já | Já | Já |
| Svartími tilviks | Styttri en klukkustund | Styttri en klukkustund | Næsti virki dagur |
| Afgreiðslutími ráðgjafar | Hópar eru í boði skv. samkomulagi. | Nei | Nei |
| Sérstakur reikningsstjóri hjá notendaþjónustu | Já | Nei | Nei |
| Sérstakur tæknimaður hjá notendaþjónustu | Tekið þátt samkvæmt sérstökum samningi | Nei | Nei |

Frekari upplýsingar eru í [Stuðningsyfirlit](/power-platform/admin/support-overview).

### <a name="process-to-engage-support"></a>Ferli til að nýta stuðning

Ef upp koma atvik sem fela í sér fjármála- og reksturs-forrit geta viðskiptavinir sent inn þjónustubeiðni til Microsoft í gegnum LCS. CSS meðhöndlar atvikin, byggt á þjónustuáætlun viðskiptavinarins og alvarleika atviksins eins hann er skilgreindur af CSS.

### <a name="service-level-agreement"></a>Þjónustustigssamningur

Microsoft ábyrgist notkunartíma þjónustu upp á 99,9 prósent á mánuði. Ef Microsoft nær ekki og viðheldur þjónustustiginu fyrir viðkomandi þjónustu eins og lýst er í þjónustustigssamningnum gæti viðskiptavinurinn átt rétt á inneign upp í hluta af mánaðarlegum þjónustugjöldum sínum fyrir þessa þjónustu. Frekari upplýsingar um hvernig á að nýta þjónustuinneign er að finna í hlutanum „Kröfur“ í [þjónustustigssamningnum](https://www.microsoft.com/licensing/docs/view/Service-Level-Agreements-SLA-for-Online-Services).

## <a name="important-resources"></a>Mikilvæg tilföng

- **[Öryggismiðstöð](https://www.microsoft.com/trust-center)** – Fáðu upplýsingar um hvar fjármála- og reksturs-gögnin þín eru geymd ásamt viðbótarupplýsingum um persónuvernd, reglufylgni og öryggisaðferðir.
- **[Leyfisskilmálar og fylgigögn](https://www.microsoftvolumelicensing.com/)** – Fljótur aðgangur að leyfisskilmálum, skilyrðum og viðbótarupplýsingum sem skipta máli fyrir notkun á vörum og þjónustu sem hafa leyfi samkvæmt fjöldaleyfisáætlunum Microsoft.
- **[Leyfisskilmálar](https://www.microsoft.com/licensing/product-licensing/)** – Úrræðin á þessari síðu skilgreina skilmála fyrir hugbúnað og þjónustu á netinu sem þú kaupir í gegnum Microsoft viðskiptaleyfisáætlanir.
- **[Reglur Microsoft um stuðningstíma](/lifecycle/)** – Þessi síða inniheldur samræmdar reglur sem segja fyrir um gildistíma notendaþjónustu fyrir tiltekna vöru.
- **[Leyfishandbók](https://www.microsoft.com/licensing/docs/view/Microsoft-Dynamics-365)** – Notaðu þessa handbók til að fá frekari upplýsingar um leyfi fyrir Dynamics 365.
- **[Þjónustuver](https://dynamics.microsoft.com/support/)** – Fáðu stuðning besta mögulega stuðning fyrir Dynamics 365 forritin þín.
- **[Dynamics Lifecycle Services](https://lcs.dynamics.com/)** – Stjórna líftíma forrits og velja fyrirsjáanlegar, endurteknar hágæða innleiðingar.
- **[Innleiðingarleiðbeiningar Dynamics 365](https://aka.ms/D365ImplementationGuideFlip)** - Innleiðingarleiðbeiningar Dynamics 365 skrá tímaprófaðar Success by Design reglur og innihalda leiðbeiningar um hönnun, smíði, prófun og uppsetningu á lausnum Dynamics 365.

## <a name="definitions"></a>Skilgreiningar

### <a name="azure-region"></a>[Azure-svæði](/azure/availability-zones/az-overview#regions)

Landsvæði þar sem eitt eða fleiri Azure-gagnaver eru til staðar. Dæmi taka með Bandaríkin og Evrópu.

### <a name="business-process-modeler-bpm"></a>[Viðskiptaferlavinnsla (BPM)](../../dev-itpro/lifecycle-services/bpm-overview.md)

Verkfæri í LCS sem hjálpar til við að ljúka greiningu á kröfufylgni fyrir tiltekna innleiðingu með viðskiptaferlaskilgreiningum frá APQC (American Productivity & Quality Center) sem eru studdar í forriti fjármála- og reksturs.

### <a name="cloud-solution-provider"></a>Skýjalausnarveita

Samstarfsaðili sem er hluti af skýjaþjónustu Microsoft (CSP) og sem veitir viðskiptavinum virðisaukandi skýjaþjónustu, stuðning, einn reikning og stjórnun viðskiptavina í einu.

### <a name="customer"></a>Viðskiptamaður

Viðskiptaaðili sem notar forrit fjármála- og reksturs og kemur fram sem leigjandi í Office 365.

### <a name="development-environment"></a>Þróunarumhverfi

Sandkassaumhverfi sem ekki tengist framleiðslu sem er notað til að þróa viðbætur. Viðskiptavinir geta útfært þetta umhverfi á eigin Azure-áskrift frá LCS. Þetta umhverfi er einnig hægt að nota fyrir sýningu, þjálfun eða önnur prófunarverkefni. Það kallast einnig [Lag 1 sandkassi](../imp-lifecycle/environment-planning.md#tier-1-vs-tier-2-and-higher).

### <a name="downtime"></a>Niðurtími

Öll tímabil þar sem notendur geta ekki skráð sig inn eða fengið aðgang að virkum leigjanda vegna bilunar á óútrunnum verkvangi eða þjónustukerfum, eins og Microsoft ákvarðar út frá sjálfvirkum annálum fyrir ástandseftirlit og kerfi. Niðurtími felur ekki í sér áætlaðan niðurtíma, að viðbótareiginleikar við þjónustuna séu ekki fyrir hendi, að ekki sé hægt að fá aðgang að þjónustunni vegna breytinga á þjónustunni eða tímabil þar sem farið er fram úr getu einingarinnar.

### <a name="implementation-partner"></a>Samstarfsaðili innleiðingar

Samstarfsaðilinn sem viðskiptavinurinn velur til að sérsníða, stilla, innleiða og hafa umsjón með fjármála- og reksturs-lausnum sínum.

### <a name="incident"></a>Atvik

Vandamál sem viðskiptavinir lenda í þegar þeir nota þjónustu fjármála- og reksturs og sem þeir leggja fram beiðni um í gegnum LCS.

### <a name="microsoft-customer-support-services-css"></a>Notendaþjónusta Microsoft (CSS)

Alþjóðlegt þjónustuteymi Microsoft sem sérhæfir sig í að veita gæðaþjónustu fyrir forrit fjármála- og reksturs.

### <a name="microsoft-dynamics-lifecycle-services-lcs"></a>Microsoft Dynamics Lifecycle Services (LCS)

Stjórnunargáttin fyrir stuðningstímastjórnun forrit fjármála- og rekstursa, frá prófun til innleiðingar, til stjórnunar og stuðnings eftir framleiðslu. Frekari upplýsingar er að finna í [Tilföng Lifecycle Services](../../dev-itpro/lifecycle-services/lcs.md).

### <a name="non-production-instance"></a>Frávik ótengt framleiðslu

Öll eftirfarandi tilvik þjónustu sem viðskiptavinurinn notar til að staðfesta viðbætur og sinna öðrum þróunarverkefnum:

- **Sandkassalag 1** – tilvik þróunaraðila (viðskiptavinur hýsir)
- **Sandkassalag 2** – Tilvik prófunar staðlaðrar samþykktar
- **Sandkassalög 3–5** – viðbótarsandkassar

Frekari upplýsingar um lög 2 til 5 eru í [Val á réttu lagi 2 eða nýrra umhverfi](../imp-lifecycle/environment-planning.md#selecting-the-correct-tier-2-or-higher-environment).

### <a name="production-instance"></a>Framleiðslutilvik

Umhverfi fjármála- og reksturs sem viðskiptavinurinn notar til að stjórna daglegum viðskiptum sínum og viðskiptaferlum í rauntíma.

### <a name="sandbox-environment"></a>Sandkassaumhverfi

Umhverfi sem ekki tengist framleiðslu sem viðskiptavinurinn notar til sýningar, þjálfunar, samþykkisprófana á notendum, staðfestingar á viðbótum og annarra prófunarverkefna.

### <a name="service"></a>Þjónusta

Allar grunnþjónustur sem eru innifaldar í forritum fjármála- og reksturs.

### <a name="service-level-agreement-sla-for-microsoft-online-services"></a>Þjónustustigssamningur (SLA) fyrir netþjónustu Microsoft

Þjónustustigssamningur á við um netþjónustu Microsoft. Nánari upplýsingar er að finna í [Þjónustustigssamningar](https://www.microsoft.com/licensing/docs/view/Service-Level-Agreements-SLA-for-Online-Services).

### <a name="service-update"></a>Þjónustuuppfærsla

Microsoft þjónustar umhverfi fjármála- og reksturs í gegnum þjónustuuppfærslur. Viðskiptavinir setja upp eigið þjónustuuppfærsludagatal eftir þörfum fyrirtækisins. Nánari upplýsingar má finna í [Uppfærsluþjónusta One Version](../../dev-itpro/lifecycle-services/oneversion-overview.md).

### <a name="success-by-design"></a>[Success by Design](/dynamics365/fasttrack/success-by-design-overview)

Ramminn sýnir á kerfisbundinn hátt innleiðingu í gegnum mat á mikilvægum stigum til að tryggja sem besta hönnun, öryggi, afköst og notandaupplifun fyrir Dynamics 365-lausn.

### <a name="user"></a>Notandi

Einstaklingur sem notar umhverfi fjármála- og reksturs og er tengdur leigjanda viðskiptavinar.

