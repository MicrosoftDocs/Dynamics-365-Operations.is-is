---
title: Velja tækni við samþættingu gagna
description: Þessi efnisatriði gefur upplýsingar um samþættingu við gögn sem Human Resources stjórnar.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d58a42236b07bf177e09aee50a207ffdf2ed1435
ms.sourcegitcommit: 72a82e9aeabbdecf57e1aee72975c63eba75143a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/24/2021
ms.locfileid: "7414715"
---
# <a name="choose-a-data-integration-technology"></a>Velja tækni við samþættingu gagna

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Þessi efnisatriði gefur upplýsingar fyrir samþættingu við gögn sem Dynamics 365 Human Resources stjórnar. Það lýsir mismunandi samþættingartækni til að hjálpa þér að ákveða hvaða tækni hentar þínum þörfum best.

## <a name="data-integration-background"></a>Bakgrunnur gagnasamþættingar

Viðskiptagögn eru lykileign sem gerir fyrirtæki þitt einstakt. Gögn fyrirtækisins eru mjög dýrmæt. Þú getur notað venslin milli gagna sem safnað er í öllu fyrirtæki þínu til að bæta viðskiptaferla og viðskiptagreind í öllum fyrirtækjum þínum. Við leggjum okkur fram um að veita greiðan, öruggan og stöðugan aðgang að viðskiptagögnum þínum hvað sem kerfið kemur frá.

Sögulega hefur verið erfitt að samþætta gögn milli margra kerfa. Microsoft tekur skref til að auðvelda samþættingu gagna og stórt skref í átt að því markmiði er náð með [Dataverse](/powerapps/maker/common-data-service/data-platform-intro).

Human Resources er að gera Dataverse að völdu almenningsviðmóti fyrir gögn í Human Resources. Með tímanum gerum við ráð fyrir að öll mikilvægustu gögn sem stjórnað er af Human Resources verði afhjúpuð í Dataverse. Við mælum með Dataverse sem valin tækni fyrir flest samþætt forrit.

Við gerum okkur grein fyrir því Dataverse gæti ekki enn geymt öll gögnin sem umsókn þín þarfnast. Við gerum okkur einnig grein fyrir því að tímalína verkefnisins gæti þurft aðra tækni. Passaðu að láta okkur vita þegar Dataverse uppfyllir ekki samþættingarþarfir þínar.

## <a name="integration-technologies"></a>Samþættingartækni

Eftirfarandi kaflar lýsa mismunandi gagnaaðlögunartækni sem hægt er að nota með Human Resources.

### <a name="dataverse-tables"></a>Dataverse töflur

Dataverse er ákjósanlegt almenningsgagnaviðmót Human Resources. Það er afsprengi Dynamics 365 XRM verkvangsins, sem er notaður af lausnum [Dynamics 365 Customer Engagement](/dynamics365/?panel=customer-engagement#pivot=business-apps).

Dataverse býður upp á verkvang og API fyrir gagnatöflur. Þegar þú setur upp Human Resources tengist það tilviki Dataverse. Einingar fyrir gögn Human Resources eru settar upp í það tilvik Dataverse. Töflurnar og gögnin þeirra eru tiltæk öllum forritum sem hægt er að tengjast við Dataverse tilvikið. Mannauður samstillir gögn til og frá Dataverse töflunum.

> [!NOTE]
> Mannauðseiningar samsvara Dataverse töflum. Frekari upplýsingar um Dataverse (áður Common Data Service) og uppfærslur á hugtökum er að finna í [Hvað er Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)

Þegar gagnatöflurnar sem krafist er af samþættingarforritinu eru í er Dataverse hægt að nota þær að fullu [Dataverse og API sem það styður](/powerapps/?panel=developer#pivot=home). Meðal forritaðra API er [Dynamics 365 Web API](/dynamics365/customer-engagement/developer/use-microsoft-dynamics-365-web-api), sem veitir OData framkvæmd til að fá aðgang Dataverse gögnum.

Dataverse töflur og tengd API þeirra eru besti valkosturinn til að fá aðgang að mannauðsgögnum úr vefforritum, vefþjónustu/API og úr öðrum forritum sem tengjast OData-straumum.

> [!NOTE]
> Þar sem sú ákvörðun að gera Dataverse að ákjósanlegu gagnaviðmót Human Resources er tiltölulega nýleg gætir þú fundið að þær gagnaeiningar Human Resources sem þú þarft fyrir samþættingu þína eru ekki enn tiltækar í Dataverse.
> </br>
> Fyrir lista yfir einingar Human Resources sem fáanlegar eru í Dataverse, sjá [Human Resources og Dataverse](/dynamics365/unified-operations/talent/corehrentities).
> </br>
> Ef einingar Human Resources, sem krafist er fyrir samþættingu þína, eru ekki enn tiltækir, verður þú að bíða eftir að gagnaeiningarnar verða gerðar aðgengilegar eða nota eina af hinum samþættingartæknunum sem lýst er hér að neðan.
> </br>
> Sjálfgefið er að slökkt sé á samþættingu Dataverse í nýju umhverfi sem inniheldur ekki meðfylgjandi kynningargögn. Kveikt er á því í nýju umhverfi sem innihalda kynningargögn og samstilling gagna hefst þegar umhverfið er útvegað. Eftir að umhverfi þitt er tilbúið til að samstilla gögn geturðu kveikt á samþættingunni.

### <a name="dmfdixf-entities"></a>DMF/DIXF einingar

Human Resources byggist fyrst og fremst á sama verkvangi og forrit Finance and Operations og veitir [Gagnastjórnunarramma (DMF)](/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=%2ffin-and-ops%2ftoc.json). DMF er einnig þekkt sem DIXF (Data Import Export Framework). Human Resources veitir safn gagnaeininga sem þú getur notað til að flytja inn og flytja út mannauðsgögn. Meðan Dataverse töflur eru æskileg samþættingarviðmót gagna fyrir mannauð eru DMF-einingar enn gagnlegar í sumum aðstæðum, svo sem:

- Dataverse töflur eru ekki enn til staðar.

- Samþættingin krefst mikillar flutnings-/útflutningsgetu magns gagna.

> [!NOTE]
> Mannauðseiningar samsvara Dataverse töflum. Frekari upplýsingar um Dataverse (áður Common Data Service) og uppfærslur á hugtökum er að finna í [Hvað er Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)

Sem stendur bjóða DMF-einingar upp á bestu gagnaþekju fyrir gögn Human Resources.

DMF hentar ekki í rauntíma samþættingu, svo sem þegar þú þarft strax endurgjöf notenda í notendaviðmóti. Pakkaaðgerðir eru áætlaðar runuvinnslur og hafa oft að lágmarki 1-2 mínútna biðtíma áður en runuþjónustan sækir starfið til framkvæmdar, auk þess tíma þarf til að ljúka innflutningi/útflutningi.

DMF getur verið besti kosturinn þegar mikil afköst eru nauðsynleg (svo sem daglega innflutning / útflutning á mörg þúsund plötum á nóttunni).

> [!NOTE]
> DMF er ekki fáanlegt fyrir Attract og Onboard.

### <a name="dmf-package-rest-api"></a>DMF pakki REST API

DMF veitir [REST API](/dynamics365/unified-operations/dev-itpro/data-entities/data-management-api) til að vinna með gagnapakka. Þetta API er hægt að nota til að hafa forritunarsamskipti við DMF og leyfa aðgerðir eins og:

- innflutning gagnapakka.

- Útflutning gagnapakka.

- Athugað stöðu innflutnings / útflutningsaðgerðar.

Human Resources styður að fullu DMF-pakka REST API.

### <a name="azure-sql-db-byod"></a>Azure SQL DB (BYOD)

DMF býður einnig upp á öflugan eiginleika (þekktur sem [Komdu með eigin gagnagrunn](/dynamics365/unified-operations/dev-itpro/analytics/export-entities-to-your-own-database), eða BYOD) sem gerir Human Resources kleift að flytja gögn út til þíns eigin Microsoft Azure SQL gagnagrunnur. Þessi hæfileiki veitir gríðarlegan sveigjanleika. Þegar gögnin eru til staðar í eigin SQL gagnagrunni geturðu notað öll forrit eða millitæki sem geta tengst SQL gagnageymslu.

BYOD er aðallega skrifvarin lausn. Þó að þú getir unnið og geymt hvaða gögn sem þú vilt hafa í Azure SQL gagnagrunninum (svo sem vegna gagnauppsveiflu), eru gögn sem eru geymd í Azure SQL gagnagrunninum ekki samstillt við Human Resources.

BYOD er viðeigandi fyrir skýrslugerð lausna, samþættingu gagna, gagnaupptöku, sem gagnaheimild fyrir [Azure Data Factory](/azure/data-factory/) leiðsla.

> [!NOTE]
> BYOD er ekki fáanlegt fyrir Attract og Onboard.

### <a name="odata-enabled-entities"></a>Aðilar sem gera OData kleift

Flestir DMF aðilar eru einnig gerðir virkir fyrir aðgang í gegnum Human Resources gagnaþjónustuna (OData). Fylgiskjöl sem veitt voru fyrir [Finance and Operations OData þjónustu](/dynamics365/unified-operations/dev-itpro/data-entities/odata) eiga við um Human Resources, nema að búa til þínar eigin einingar sem birtast í OData.

Meðan Dataverse og útfærslan á OData sem veitt er af Dataverse (í gegnum [Dynamics 365 Web API](/previous-versions/dynamicscrm-2016/developers-guide/mt593051(v=crm.8))) er ákjósanlegra yfir gagnaþjónustuna Human Resources, upplýsingaþjónusta Human Resources hefur nú fullkomnari umfjöllun um einingar vegna gagna Human Resources.

### <a name="excel-add-in"></a>Innbótin Excel

[Excel-innbótin](/dynamics365/unified-operations/dev-itpro/office-integration/use-excel-add-in?toc=%2fdynamics365%2funified-operations%2ftalent%2ftoc.json) nýtir sér OData-gerðar einingar undir yfirborðinu. Það veitir notanda þægilegan hátt til að sækja og breyta gögnum um Human Resources í gegnum þekkta Excel UI.

Excel-viðbætið er viðeigandi fyrir sértækan innflutning / útflutning gagna frá sérfræðingum á viðskiptasviði. Fyrir endurtekna samþættingu gagna sem krefst forritunar sjálfvirkni mun önnur samþættingartækni vera heppilegri.

### <a name="data-integrator"></a>Gagnasamþætting

Þú getur notað [Gagnaaðlögunarþjónustu](/powerapps/administrator/data-integrator) til að samþætta gögn í og úr Dataverse. Gagnasamþættari gerir kleift að skilgreina samþættingarverk, oft byggð á fyrirfram skilgreindum sniðmátum sem forritarar hafa sniðið að tilteknum samþættingum. Þú getur áætlað samþættingarverk til að keyra sjálfkrafa á endurtekninni áætlun eða keyrt þau handvirkt.

Gagnasamþættingarverk henta fyrir Dataverse runusamþættingar. Þau eru frábær valkostur fyrir samþættingu Dynamics 365 forritafjölskyldunnar. Til dæmis býður Microsoft upp á sniðmát fyrir gagnaflutning til að samþætta gögn úr Human Resources í Dynamics 365 Finance. Þú getur lært meira um sniðmátið í [Samþætting úr Dynamics 365 Human Resources í Dynamics 365 Finance](hr-admin-integration-finance.md).

### <a name="power-query"></a>Power Query

Gagnasamþætting styður [Power Query](/power-query/power-query-what-is-power-query) í gegnum [eiginleikann Ítarleg fyrirspurn](/powerapps/administrator/data-integrator#advanced-data-transformation-and-filtering). Power Query veitir öfluga, sveigjanlega gagnasíun og umbreytingu, þar með talið fjölbreytt M formúlutungumálið. Power Query verður líklega kunnugleg ef þú hefur þróað Power BI skýrslur.

## <a name="deciding-on-an-integration-technology"></a>Ákveðið að samþættingu tækni

Með svo mörgum mismunandi aðlögunartækni sem til eru, getur það verið yfirþyrmandi að ákveða hvaða samþættingaraðferð til að nota. Þegar umfjöllun gagna í Dataverse þroskast verður ákvörðunin auðveldari, með Dataverse sem ákjósanlegt gagnaviðmót í flestum tilvikum. En þangað til gætirðu fundið það Dataverse fullnægir ekki enn þínum þörfum. Eftirfarandi tafla dregur saman nokkur af lykileinkennum valkosta samþættingartækni.

| Tækni/Tool/API    | Endurteknar samþættingar                   | Samstilltur / ósamstilltur                    | Forritunaraðgangur í gegnum API        | Viðeigandi gagnamagn                                   | Gagnaþekja                       |
|------------------------|------------------------------------------|---------------------------------------------|-------------------------------------------|------------------------------------------------------------|-------------------------------------|
| Dataverse töflur           | Já, nota Gagnasamritara eða millitæki | Samstilla ósamstilltur, hópur (í gegnum gagnaflutning) | Já, í gegnum Dynamics 365 Web API (OData) | Mismunandi eftir notkunartilfelli (styður síðuskip fyrir gagnvirka notkun) | Bætir<sup>2</sup>                       |
| DMF einingar           | Já, tímaáætlun í gegnum millitæki        | Async, runa                                | Já, í gegnum DMF Package REST API         | Hátt (hundruð þúsund skráa)                    | Mikill                                |
| DMF pakki REST API   | Já, tímaáætlun í gegnum millitæki        | Async, runa                                | Já                                       | Hátt (hundruð þúsund skráa)                    | API styður alla DMF einingar       |
| BYOD                   | Já, áætlað af stjórnanda í Human Resources        | Async, runa                                | Nr.<sup>3</sup>                                    | Hátt (hundruð þúsund skráa)                    | Styður alla DMF einingar           |
| Aðilar sem gera OData kleift | Já, nota millitæki                    | Samstilla                                        | Já, í gegnum Human Resources gagnaþjónustu (OData)  | Mismunandi eftir notkunartilfelli (styður síðuskip fyrir gagnvirka notkun) | Mikill                                |
| Innbótin Excel           | Nr                                       | Samstilla                                        | Nr                                        | Miðlungs (tugþúsundir skráa)                      | Styður alla aðila sem gera OData kleift |
| Gagnasamþætting        | Já, tímaáætlun í Gagnasamþættinum        | Async, runa                                | Ekkert                                        | Misjafnt hvað varðar notkun                                       | Styður allar Dataverse töflur           |

<sup>2</sup>Microsoft fjárfestir mikið í því að auka gagnaþekju fyrir Dataverse töflur. Við mælum með að nota Dataverse þegar umfjöllun er fyrir hendi. Sem stendur Dataverse gagnaþekja er lítil samanborið við DMF og OData-virkar einingar.

<sup>3</sup>Hægt er að nálgast SQL gagnagrunn með forritun.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
