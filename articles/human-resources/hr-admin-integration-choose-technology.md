---
title: Velja tækni við samþættingu gagna
description: Þessi grein veitir leiðbeiningar um ýmsa möguleika til að samþætta við gögn sem stjórnað er af Human Resources og lýsa einkennum mismunandi aðlögunartækni svo samþættingar geti tekið upplýstar ákvarðanir varðandi hvaða tækni hentar best þeirra þörfum.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f2de5dd41c00e6546b4a4feadaf5774430d572bb
ms.sourcegitcommit: 13c4a6f98ccce243d6befde90992aefcf562bdab
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029889"
---
# <a name="choose-a-data-integration-technology"></a>Velja tækni við samþættingu gagna

Dynamics 365 Human Resources heldur utan um viðskiptagögn sem eru gagnleg í ýmsum viðskiptaferlum. Þessi grein veitir leiðbeiningar um ýmsa möguleika til að samþætta við gögn sem stjórnað er af Human Resources og lýsa einkennum mismunandi aðlögunartækni svo samþættingar geti tekið upplýstar ákvarðanir varðandi hvaða tækni hentar best þeirra þörfum.

## <a name="data-integration-vision"></a>Samþættingarstefna gagna

Microsoft lítur á viðskiptagögn sem lykil eign sem gerir fyrirtæki þitt einstakt. Gögn fyrirtækisins eru mjög dýrmæt. Gögn sem safnað er og viðhaldið af einum hluta starfseminnar tengjast gögnum sem safnað er af öðrum hluta starfseminnar og þessi samskipti geta verið notuð til að bæta viðskiptaferla og viðskiptagreind í öllum fyrirtækjum þínum. Að veita greiðan, öruggan, stöðugan aðgang að viðskiptagögnum þínum, óháð því hvaða kerfi „á“ gögnin, er lykilatriðið í þeirri framtíðarsýn sem við höfum varðandi samþættingu gagna við Human Resources.

Sögulega hefur verið erfitt að samþætta gögn milli margra kerfa.
Microsoft tekur skref til að auðvelda samþættingu gagna og stórt skref í átt að því markmiði er náð með [Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).

Framundan er Human Resources að gera Common Data Service valinn almenningsviðmót fyrir gögn í Human Resources. Með tímanum gerum við ráð fyrir að öll mikilvægustu gögn sem stjórnað er af Human Resources verði afhjúpuð í Common Data Service. Við mælum með Common Data Service sem valin tækni fyrir flest samþætt forrit. Þó að við gerum okkur grein fyrir að ekki eru öll gögn sem umsókn þín þarfnast nú til Common Data Service, og að tímalínur verkefna þinna geti þurft aðra tækni, vinsamlegast láttu okkur vita hvenær Common Data Service uppfyllir ekki samþættingarþörf þína.

## <a name="integration-technologies"></a>Samþættingartækni

Eftirfarandi kaflar lýsa mismunandi gagnaaðlögunartækni sem hægt er að nota með Human Resources.

### <a name="common-data-service-entities"></a>Common Data Service einingar

Common Data Service er ákjósanlegt almenningsgagnaviðmót Human Resources. Common Data Service er byggður á þroskuðum vettvangi og hefur vaxið úr Dynamics 365 "XRM" pallinum, sem [Dynamics 365 Customer Engagement](https://docs.microsoft.com/dynamics365/#pivot=business-apps&panel=customer-engagement) lausnir eru byggðar.

Common Data Service veitir vettvang fyrir gagnaeiningar og API til að fá aðgang að þeim einingum. Þegar starfsmannamálum er komið fyrir í fyrirtækinu þínu er mannauðsmál tengt a Common Data Service tilvik og þær einingar sem halda uppi mannauðsgögnum eru settir inn í það Common Data Service tilvik, sem gerir aðilana og gögn þeirra aðgengileg öllum forritum sem geta tengst við Common Data Service tilvik. Eftir því hvaða mannauðsforrit þú notar, framkvæmir mannauður annaðhvort gagnaaðgerðir beint gegn Common Data Service einingum (þetta á við um Attract og Onboard) eða samstilla gögn til / frá Common Data Service einingar.

Þegar gagnaeiningar sem afhjúpa gögnin sem samþættingarforritin þín þarfnast eru til staðar í Common Data Service, þú getur nýtt þér að fullu [Common Data Service og API sem það styður](https://docs.microsoft.com/powerapps/#pivot=home&panel=developer). Meðal forritaðra API er [Dynamics 365 Web API](https://docs.microsoft.com/dynamics365/customer-engagement/developer/use-microsoft-dynamics-365-web-api), sem veitir OData framkvæmd til að fá aðgang Common Data Service gögnum.

Einingar Common Data Service og tengd API eru besti kosturinn til að fá aðgang að mannauðsgögnum frá vefforritum, vefþjónustum / API, og frá öðru forriti sem tengist OData straumum.

> [!NOTE]
> Með þeirri ákvörðun að taka Common Data Service þar sem ákjósanlegt gagnaviðmót Human Resources er tiltölulega nýlegt gætir þú fundið að þeim mannauðsgagnaeiningum sem þú þarft fyrir samþættingu þína eru ekki enn tiltækar í Common Data Service<sup>1</sup>. Ef einingar Human Resources, sem krafist er fyrir samþættingu þína, eru ekki enn tiltækir, verður þú að bíða eftir að gagnaeiningarnar verða gerðar aðgengilegar eða þú verður að nota eina af hinum samþættingartæknunum sem lýst er hér að neðan.
> 
> Sjálfgefið er að slökkt sé á samþættingu Common Data Service í nýju umhverfi sem inniheldur ekki meðfylgjandi kynningargögn. Kveikt er á því í nýju umhverfi sem innihalda kynningargögn og samstilling gagna hefst þegar umhverfið er útvegað. Eftir að umhverfi þitt er tilbúið til að samstilla gögn geturðu kveikt á samþættingunni.

<sup>1</sup>Fyrir lista yfir einingar Human Resources sem fáanlegar eru í Common Data Service, sjáðu [Human Resources og Common Data Service](https://docs.microsoft.com/dynamics365/unified-operations/talent/corehrentities). Fyrir Attract og Onboard eru allar einingar fáanlegar í Common Data Service.

### <a name="dmfdixf-entities"></a>DMF/DIXF einingar

Human Resources byggður fyrst og fremst á sama vettvang og Finance and Operations forrit, veitir [Gagnastjórnunarramma (DMF)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json), stundum einnig þekkt sem Data Import Export Framework eða DIXF, og safn gagnaeininga sem hægt er að nota til að flytja / flytja út gögn til / frá Human Resources. Meðan einingar Common Data Service eru valinn viðmót gagnagrunna fyrir Human Resources, DMF einingar munu enn vera gagnlegar við sumar kringumstæður, svo sem:

- Common Data Service einingar eru ekki enn tiltækar.

- Samþættingin krefst mikillar flutnings / útflutningsgetu magns gagna.

Stofnanir DMF veita um þessar mundir fullkomnustu gagnaumfjöllun vegna gagna Human Resources.

DMF hentar ekki í rauntíma samþættingu (svo sem þegar tafarlaus viðbrögð notenda í notendaviðmóti er krafist), vegna þess að pakkaðgerðir eru áætlaðar runuvinnslur og munu oft hafa að lágmarki 1-2 mínútna leynd áður en runuþjónustan velur upp starfið til framkvæmdar, auk þess sem tími þarf til að ljúka innflutningi / útflutningi.

DMF getur verið besti kosturinn þegar mikil afköst eru nauðsynleg (svo sem daglega innflutning / útflutning á mörg þúsund plötum á nóttunni).

> [!NOTE]
> DMF er ekki fáanlegt fyrir Attract og Onboard.

### <a name="dmf-package-rest-api"></a>DMF pakki REST API

DMF veitir [REST API](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-management-api) til að vinna með gagnapakka. Þetta API er hægt að nota til að hafa forritunarsamskipti við DMF og leyfa aðgerðir eins og:

- innflutning gagnapakka.

- Útflutning gagnapakka.

- Athugað stöðu innflutnings / útflutningsaðgerðar.

DMF pakki REST API er fyllilega studdur í Human Resources: Core HR.

### <a name="azure-sql-db-byod"></a>Azure SQL DB (BYOD)

DMF býður einnig upp á öflugan eiginleika (almennt þekktur sem [Komdu með eigin gagnagrunn](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/export-entities-to-your-own-database), eða BYOD) sem gerir Human Resources kleift að flytja gögn út til þíns eigin Microsoft Azure SQL gagnagrunnur. Þetta veitir gríðarlegan sveigjanleika, vegna þess að þegar gögnin eru til staðar í eigin SQL gagnagrunni geturðu notað öll forrit eða millitæki sem geta tengst SQL gagnageymslu.

BYOD ætti almennt að teljast skrifvarin lausn. Þó að þú getir unnið og geymt hvaða gögn sem þú vilt hafa í Azure SQL gagnagrunninum (svo sem vegna gagnauppsveiflu), verða gögn sem eru geymd í Azure SQL gagnagrunninum ekki samstillt aftur til mannauðs.

BYOD er viðeigandi fyrir skýrslugerð lausna, samþættingu gagna, gagnaupptöku, sem gagnaheimild fyrir [Azure Data Factory](https://docs.microsoft.com/azure/data-factory/) leiðsla.

> [!NOTE]
> BYOD er ekki fáanlegt fyrir Attract og Onboard.

### <a name="odata-enabled-entities"></a>Aðilar sem gera OData kleift

Flestir DMF aðilar eru einnig gerðir virkir fyrir aðgang í gegnum Human Resources gagnaþjónustuna (OData). Gögnin sem veitt voru fyrir [Finance and Operations OData þjónusta](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/odata) almennt á einnig við um Human Resources, þó að skjöl um stofnun eigin OData-aðila sem verða fyrir áhrifum muni ekki eiga við.

Meðan Common Data Service og útfærslan á OData sem veitt er af Common Data Service (í gegnum [Dynamics 365 Web API](https://docs.microsoft.com/previous-versions/dynamicscrm-2016/developers-guide/mt593051(v=crm.8))) er ákjósanlegra yfir gagnaþjónustuna Human Resources, upplýsingaþjónusta Human Resources hefur nú fullkomnari umfjöllun um einingar vegna gagna Human Resources.

### <a name="excel-add-in"></a>Innbótin Excel

[Excel-innbótin](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/office-integration/use-excel-add-in?toc=/dynamics365/unified-operations/talent/toc.json) nýtir sér OData-gerðar einingar undir yfirborðinu. Það veitir notanda þægilegan hátt til að sækja og breyta gögnum um Human Resources í gegnum þekkta Excel UI.

Excel-viðbætið er viðeigandi fyrir sértækan innflutning / útflutning gagna frá sérfræðingum á viðskiptasviði. Fyrir endurtekna samþættingu gagna sem krefst forritunar sjálfvirkni mun önnur samþættingartækni vera heppilegri.

### <a name="data-integrator"></a>Gagnasamþætting

Stjórnandareynsla Common Data Service veitir [Gagnaaðlögunarþjónustu](https://docs.microsoft.com/powerapps/administrator/data-integrator) sem hægt er að nota til að samþætta gögn til / frá Common Data Service. Hægt er að nota gagnasamþættara til að skilgreina samþættingarverkefni (oft byggð á fyrirfram skilgreindum sniðmátum sem forritarar hafa sniðið að tilteknum samþættingum). Hægt er að áætla samþættingarverkefnin sjálfkrafa á endurteknum tímaáætlun eða vera keyrð handvirkt.

Gagnasamþættarverkefni henta Common Data Service runusamþættingar og gera frábært val fyrir samþættingu Dynamics 365 forritafjölskyldunnar. Sem dæmi, Microsoft býður upp á útbúið sniðmát fyrir gagnaflutning sem hægt er að nota til að samþætta gögn úr Human Resources í Dynamics 365 Finance. Nánari upplýsingar er að finna í [Samþætting úr Dynamics 365 Human Resources í Dynamics 365 Finance](hr-admin-integration-finance.md).

### <a name="power-query"></a>Power Query

Gagnaaðili styður einnig [Power Fyrirspurn](https://docs.microsoft.com/power-query/power-query-what-is-power-query) (í gegnum þess [Ítarleg fyrirspurn lögun](https://docs.microsoft.com/powerapps/administrator/data-integrator#advanced-data-transformation-and-filtering)).
Power Fyrirspurn veitir öfluga, sveigjanlega gagnasíun og umbreytingu, þar með talið auðugt M formúlutungumál, og mun líklega þekkja þá sem hafa reynslu af þróun Power BI skýrslur.

## <a name="deciding-on-an-integration-technology"></a>Ákveðið að samþættingu tækni

Með svo mörgum mismunandi aðlögunartækni sem til eru, getur það verið yfirþyrmandi að ákveða hvaða samþættingaraðferð til að nota. Með tímanum, og sérstaklega þegar umfjöllun gagna í Common Data Service þroskast, ákvörðunin verður auðveldari, með Common Data Service að vera ákjósanlegt gagnatengi í flestum tilvikum. En þangað til gætirðu fundið það Common Data Service fullnægir ekki enn þínum þörfum. Eftirfarandi tafla hjálpar til við að draga saman lykil einkenni ýmissa valkosta samþættingartækni.

| Tækni/Tool/API    | Endurteknar samþættingar                   | Samstilltur / ósamstilltur                    | Forritunaraðgangur í gegnum API        | Viðeigandi gagnamagn                                   | Gagnaþekja                       |
|------------------------|------------------------------------------|---------------------------------------------|-------------------------------------------|------------------------------------------------------------|-------------------------------------|
| Common Data Service einingar           | Já, nota Gagnasamritara eða millitæki | Samstilla ósamstilltur, hópur (í gegnum gagnaflutning) | Já, í gegnum Dynamics 365 Web API (OData) | Mismunandi eftir notkunartilfelli (styður síðuskip fyrir gagnvirka notkun) | Bætir<sup>2</sup>                       |
| DMF einingar           | Já, tímaáætlun í gegnum millitæki        | Async, runa                                | Já, í gegnum DMF Package REST API         | Hátt (hundruð þúsund skráa)                    | Mikill                                |
| DMF pakki REST API   | Já, tímaáætlun í gegnum millitæki        | Async, runa                                | Já                                       | Hátt (hundruð þúsund skráa)                    | API styður alla DMF einingar       |
| BYOD                   | Já, áætlað af stjórnanda í Human Resources        | Async, runa                                | Nr.<sup>3</sup>                                    | Hátt (hundruð þúsund skráa)                    | Styður alla DMF einingar           |
| Aðilar sem gera OData kleift | Já, nota millitæki                    | Samstilla                                        | Já, í gegnum Human Resources gagnaþjónustu (OData)  | Mismunandi eftir notkunartilfelli (styður síðuskip fyrir gagnvirka notkun) | Mikill                                |
| Innbótin Excel           | Nr                                       | Samstilla                                        | Nr                                        | Miðlungs (tugþúsundir skráa)                      | Styður alla aðila sem gera OData kleift |
| Gagnasamþætting        | Já, tímaáætlun í Gagnasamþættinum        | Async, runa                                | Nr                                        | Misjafnt hvað varðar notkun                                       | Styður alla Common Data Service einingar           |

<sup>2</sup>Microsoft fjárfestir mikið í að auka gagnaumfjöllun fyrir Common Data Service einingar, og mælir með Common Data Service sem ákjósanlegt gagnatengi þegar þekja er tiltæk. Sem stendur Common Data Service gagnaþekja er lítil miðað við DMF og OData-virkar einingar.

<sup>3</sup>Hægt er að nálgast SQL gagnagrunn með forritun.

## <a name="summary"></a>Samantekt

Fyrirtækjagögn þín eru dýrmæt eign en hægt er að draga verulega úr gildi þeirra ef það er erfitt að nota gögnin í sérstökum tilgangi þínum (svo sem skýrslugerð, gagnaöflun eða sérsniðin forrit). Dynamics 365 Human Resources býður upp á ýmsa tækni til að vinna með gögnin þín utan notendaviðmóta Human Resources-forritsins (UI), sem gerir samþættingu aðgangs að gögnunum kleift. Þetta efni hefur lýst fyrirliggjandi samþættingartækni og nokkrum lykil einkennum þeirra. Þessar upplýsingar ættu að hjálpa þér að taka betri ákvarðanir um hvaða aðferðir við skuldsetningu fyrir samþættingarverkefni þín.

