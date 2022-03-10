---
title: Commerce-greining (forútgáfa)
description: Þetta efni útskýrir hvernig á að setja upp og nota greiningargetu í Microsoft Dynamics 365 Commerce.
author: AamirAllaq
ms.date: 02/24/2022
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: 2021-11-12
ms.openlocfilehash: 7e3721421e15bc3e5937691cdbaee51e4d3cdd17
ms.sourcegitcommit: d2e5d38ed1550287b12c90331fc4136ed546b14c
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/25/2022
ms.locfileid: "8349744"
---
# <a name="commerce-analytics-preview"></a>Commerce-greining (forútgáfa)

[!include [banner](includes/banner.md)]

Þetta efnisatriði útskýrir hvernig á að setja upp Commerce analytics (Preview), virkni greiningargetu sem er innifalin í Microsoft Dynamics 365 Commerce.

## <a name="commerce-analytics-preview-live-demo"></a>Commerce Analytics (Preview) lifandi kynning

Þú getur prófað a [lifandi kynningu á Commerce Analytics (Preview)](https://aka.ms/CommerceAnalyticsDemo).

![Samantekt viðskiptagreiningar (forskoðun).](media/CommerceAnalytics_Summary.png)
![Commerce Analytics (Preview) Greiðslur](media/CommerceAnalytics_Payments.png)
![Commerce Analytics (Preview) Vefvirkni](media/CommerceAnalytics_WebActivity.png)

## <a name="commerce-analytics-preview-system-architecture"></a>Viðskiptagreiningar (Preview) kerfisarkitektúr

### <a name="key-components"></a>Lykilþættir

Viðskiptagreining (Preview) samanstendur af eftirfarandi lykilþáttum:

- Gagnvirkt tilbúið til notkunar Power BI skýrslur
- SQL skoðanir í Azure Synapse Analytics
- Eininga- og verufræðigögn í Azure Data Lake
- Hrá gögn í Data Lake

![Lykilþættir viðskiptagreiningarkerfisins](media/CommerceAnalyticsArchitecture_v2.png)

### <a name="data-flow"></a>Gagnaflæði

#### <a name="step-1-data-generation"></a>Skref 1: Gagnagerð

Gögn eru annaðhvort upprunnin sem viðskiptagögn eða hegðunargögn frá einni af eftirfarandi heimildum:

- Samstarfsaðili í símaveri notar viðskiptavinur Commerce HQ til að vinna úr sölupöntunum.
- Gjaldkeri á sölustað (POS) vinnur sölufærslur.
- Sala er búin til í sérsniðnum forritum með því að nota Headless Commerce (Commerce Scale Unit).
- Netverslunarkaupandi skoðar netverslunarsíðuna þína.
- Kaupandi í rafrænum viðskiptum leggur fram pöntun á vefsíðunni þinni fyrir rafræn viðskipti.
- Gögn eru framleidd af öðrum kerfum, ss Dynamics 365 Connected Spaces.

#### <a name="step-2-ingestion-and-pre-processing"></a>Skref 2: Inntaka og forvinnsla

Viðskiptagögn fara til Commerce HQ annað hvort beint (þegar um er að ræða pantanir sem eru teknar beint í Commerce HQ viðskiptavininn) eða í gegnum Commerce Scale Unit (þegar um er að ræða pantanir sem eru teknar á POS, í rafrænum viðskiptum eða sérsniðnum viðskiptavinir sem nota Headless Commerce).

Eiginleikinn Flytja út í gagnavatn er síðan notaður til að afrita viðskiptagögnin í gagnavatnið þitt sem hrá gögn. Í gagnavatninu eru hrágögnin geymd í Töflur möppunni.

Gögn um vefvirkni rafræn viðskipti eru send beint í gagnavatnið. Gögn sem eru framleidd af öðrum kerfum, ss Dynamics 365 Connected Spaces, er sent beint í gagnavatnið af þessum kerfum.

#### <a name="step-3-transformation-and-aggregation"></a>Skref 3: Umbreyting og samsöfnun

Eftir að hrá gögn eru í gagnavatninu þínu les Commerce greiningarþjónustan þau, umbreytir þeim, safnar þeim saman og skrifar þau aftur í gagnavatnið í formi rökréttra eininga (í Entities möppunni) og uppsafnaðra mælinga (í Ontologies möppunni ).

#### <a name="step-4-querying"></a>Skref 4: Fyrirspurnir

Azure Synapse Analytics er notað til að spyrjast fyrir um gögn í gagnavatninu þínu í gegnum Transact-SQL (T-SQL) viðmót. Þetta viðmót inniheldur SQL skoðanir. SQL skoðanir gera sameinaða fyrirspurnir um gögn í gagnavatninu, annað hvort beint í gegnum T-SQL biðlara (fyrir sértæka greiningu) eða í gegnum sjónrænt tól eins og Power BI.

#### <a name="step-5-modeling-and-serving"></a>Skref 5: Líkangerð og framreiðslu

Gögn sem spurt er um af Azure Synapse Analytics fer til Power BI merkingarfræðilegu líkaninu. Það fer eftir tegund gagna, þau eru annað hvort reglulega flutt inn í minnið Power BI eða beint fyrirspurn á keyrslutíma.

Að lokum eru gögnin færð inn Power BI myndefni, svo að notendur geti skoðað og haft samskipti við það.

## <a name="commerce-analytics-preview-functional-overview"></a>Viðskiptagreiningar (Preview) hagnýtur yfirlit

### <a name="summary"></a>Samantekt

Commerce Analytics sniðmátsforrit inniheldur eftirfarandi aðalskýrslusíður:

1. [Síur á hæsta stigi](#TopLevelFilters)
2. [Afurðir](#ProductsPage)
3. [Viðskiptavinir](#CustomersPage)
4. [Rásir](#ChannelsPage)
5. [Sala](#SalesPage)
6. [Spássíur](#MarginsPage)
7. [Vöruskil](#ReturnsPage)
8. [Afslættir](#DiscountsPage)
9. [Greiðslur](#PaymentsPage)
10. [Viðskiptavinir](#CustomersPage)
11. [Samanburður](#ComparisonPage)
12. [Aðgerðir á vefnum](#WebActivityPage)
13. [Vefvirkni - Sía á efstu stigi](#WebActivityTopLevelFilters)

#### <a name="top-level-filters"></a><a name="TopLevelFilters"></a> Síur á hæsta stigi

- Dagsetningarstillingar

    - Ár
    - Ársfjórðungur
    - Mánuður
    - Vika
    - Dagur

- Rásarstillingar

    - Lögaðili
    - Gerð rásar
    - Gerð viðskiptavinar
    - Sölugerð
    - Rás
    - Stigveldi fyrirtækis

- Vörustillingar

    - Tegundastigveldi
    - Flokkur

#### <a name="products"></a><a name="ProductsPage"></a> Vörur

- Sala
- Spássía
- Vöruskil

#### <a name="customers"></a><a name="CustomersPage"></a> Viðskiptavinir

- Sala
- Spássía
- Vöruskil

#### <a name="channels"></a><a name="ChannelsPage"></a> Rásir

- Sala
- Spássía
- Vöruskil

### <a name="sales"></a>Sala<a name="SalesPage"></a>

- Eftir afhendingarstað
- Eftir rás/verslun/útstöð
- Eftir starfsmönnum
- Eftir dagsetningu
- Eftir klukkustund
- Eftir vöruflokkum

### <a name="margins"></a><a name="MarginsPage"></a> Framlegð

- Eftir afhendingarstað
- Eftir vöru
- Eftir dagsetningu

### <a name="returns"></a><a name="ReturnsPage"></a> Skilar

- Skil eftir upphæð

    - Eftir verslun
    - Eftir vöru
    - Eftir dagsetningu

- Skil eftir viðskiptum

    - Eftir verslun
    - Eftir vöru
    - Eftir dagsetningu

### <a name="discounts"></a><a name="DiscountsPage"></a> Afslættir

- Eftir verslun
- Eftir vöru
- Eftir dagsetningu
- Sundurliðun

    - Lögaðili
    - Verslun
    - Gerð afsláttar
    - Heiti afsláttar
    - Afurð

### <a name="payments"></a><a name="PaymentsPage"></a> Greiðslur

- Eftir rás/stöð
- Eftir greiðslumáta/tegund
- Eftir dagsetningu
- Sundurliðun

    - Lögaðili
    - Gerð rásar
    - Verslun
    - Afgreiðslustöð
    - Greiðslumáti

### <a name="customers"></a><a name="CustomersPage"></a> Viðskiptavinir

- Líftímagildi (LTV)

    LTV er reiknað út frá heildarupphæðinni sem viðskiptavinur eyðir yfir allt Dynamics 365 Commerce sölurásir (þar á meðal POS, rafræn viðskipti og símaver).

- Recency

    Tíðni er reiknuð út frá fjölda daga frá síðustu viðskiptatengslum viðskiptavinar við fyrirtækið. Eins og er, tekur nýleg ekki tillit til þátttökumerkja sem ekki eru viðskipti, eins og vefskoðunarvirkni í rafrænum viðskiptum.

- Tíðni

    Tíðni er reiknuð út frá viðskiptatengslum viðskiptavinar við fyrirtækið. Eins og er, tekur tíðnin ekki tillit til þátttökumerkja sem ekki eru viðskipti, eins og vefskoðunarvirkni í rafrænum viðskiptum.

- Lengd sambands

    Lengd tengsla er reiknuð út frá fjölda daga frá því viðskiptamannafærsla var stofnuð í kerfinu.

- Færslutalning

### <a name="comparison"></a><a name="ComparisonPage"></a> Samanburður

- Vörusamanburður eftir tímabilum

    - Sala og sölumunur
    - Framlegð og framlegðarmunur

- Viðskiptavinur eftir tímabili

    - Sala og sölumunur
    - Framlegð og framlegðarmunur

### <a name="web-activity"></a><a name="WebActivityPage"></a> Vefvirkni

#### <a name="top-level-filters"></a><a name="WebActivityTopLevelFilters"></a> Síur á hæsta stigi

- Dagsetningabil
- Gerð rásar
- Rás
- Tegundastigveldi

#### <a name="acquisitions"></a>Kaup

- Síðuskoðanir

    - Eftir landi eða svæði
    - Eftir vöru
    - Eftir innskráðan notanda stöðu
    - Eftir dagsetningu

- Rafræn viðskipti pantanir
- Gengi gjaldmiðla

    - Eftir dagsetningu

- Viðskiptatrekt

    - Síðuskoðun eftir tegund síðu (heimasíða, flokkasíða eða vöruupplýsingasíða)
    - Bæta í körfu
    - Ljúka kaupum
    - Innkaup

#### <a name="sessions"></a>Setur

Fundur er þáttur um heimsókn notanda á netverslunarvefsíðuna þína. Tíma er talið lokið eftir 30 mínútna óvirkni eða 24 klukkustunda virka notkun.

- Eftir landi eða svæði
- Eftir uppruna (ytri tilvísun)
- Eftir innskráðan notanda stöðu
- Talning þings

    - Eftir dagsetningu
    - Eftir inngangssíðu

- Panta á hverja lotu

    - Eftir dagsetningu

- Hopphlutfall lotu

    Setuhopp er fundur þar sem notandi fer strax eftir að hann heimsækir netverslunarvefsíðuna þína. Fyrir frekari upplýsingar, sjá [Hopphlutfall](https://en.wikipedia.org/wiki/Bounce_rate).

- Smellir á hverja lotu

#### <a name="visitors"></a>Gestir

Nafnlaus gestur á netverslunarsíðunni þinni er auðkenndur á einstakan hátt út frá tilteknum vafra og tilteknu tæki sem notandinn notar. Viðskiptagreining rekur ekki nafnlausa gesti í mismunandi vöfrum eða tækjum. Nafnlaus gestur sem notar sama vafra á sama tæki er auðkenndur á einstakan hátt í mörgum notendalotum, þar til annað hvort gögnum í skyndiminni vafrans er hreinsað eða tímabil (venjulega 12 mánuðir) líður, hvort sem kemur fyrst.

Ef gestir vafra um netviðskiptasíðuna þína á meðan þeir eru skráðir inn getur Commerce Analytics veitt frekari upplýsingar um þá. Þessar upplýsingar eru byggðar á núverandi sambandi sem fyrirtæki þitt hefur við gestina vegna fyrri kaupa þeirra á öllum Dynamics 365 Commerce sölurásir (þar á meðal POS, rafræn viðskipti og símaver). Viðbótarupplýsingarnar innihalda nýlega, lengd sambands, lífstímagildi og tíðnigögn.

- Framlegð gesta
- Meðaltal pantanir gesta
- Meðalsala gesta
- Fjöldi gesta í rafrænum viðskiptum

    - Eftir dagsetningu
    - Eftir staðsetningu

        Eins og er, Commerce greiningar geta aðeins veitt land-/svæðisstig fyrir staðsetningarinnsýn fyrir gesti í rafrænum viðskiptum.

    - Eftir nýlegri

        Tíðni er reiknuð út frá fjölda daga frá síðustu viðskiptatengslum viðskiptavinar við fyrirtækið. Eins og er, tekur nýleg ekki tillit til þátttökumerkja sem ekki eru viðskipti, eins og vefskoðunarvirkni í rafrænum viðskiptum.

    - Eftir lengd sambandsins

        Lengd tengsla er reiknuð út frá fjölda daga frá því viðskiptamannafærsla var stofnuð í kerfinu.

    - Eftir ævigildi (LTV)

        LTV er reiknað út frá heildarupphæðinni sem viðskiptavinur eyðir yfir allt Dynamics 365 Commerce sölurásir (þar á meðal POS, rafræn viðskipti og símaver).

    - Eftir tíðni

        Tíðni er reiknuð út frá viðskiptatengslum viðskiptavinar við fyrirtækið. Eins og er, tekur tíðnin ekki tillit til þátttökumerkja sem ekki eru viðskipti, eins og vefskoðunarvirkni í rafrænum viðskiptum.

#### <a name="impressions"></a>Birtingar

Birting er ein sýn á vörumynd frá gesti í rafrænum viðskiptum. Til dæmis fer rafræn viðskiptagestur á heimasíðuna á netverslunarvefsíðunni þinni og skoðar jógamottuvöru í **Mest seld** lista mát. Gesturinn skoðar síðan sömu jógamottuvöruna í a **Val fyrir þig** lista mát. Í þessu tilviki eru tvær vörubirtingar.

Eins og er eru birtingar raktar á eftirfarandi flötum:

- Listar (td.**Mælt er með**, **seld**, **fyrir þig**, og **Vinsælt**)
- Körfueining
- Ílát leitarniðurstöðu
- Gámur fyrir leitarniðurstöður flokka

Eins og er, eru vörur sem eru birtar í hringekjueiningu eða í sérsniðnum myndefni ekki taldar með í birtingartengdum mælikvörðum.

The **Birtingarskýrsla** síða inniheldur eftirfarandi mælikvarða:

- Birtingarfjöldi

    - Eftir síðugerð og einingu

        Síðugerð er almenna gerð síðu sem er skilgreind fyrir hverja síðu á netverslunarvefsíðunni þinni. Tegund eininga er tegund sjónræna einingarinnar fyrir rafræn viðskipti sem varan er sýnd í.

        Til að skoða birtingar eftir einingu gætirðu þurft að kafa niður í síðuna og myndefni.

    - Eftir vöru
    - Eftir innskráðan notanda stöðu
    - Eftir dagsetningu

- Fjöldi smella birtinga

    Birtingarsmellur á sér stað þegar gestur í rafrænum viðskiptum velur myndefni vöru. Venjulega er gesturinn síðan tekinn á vöruupplýsingasíðu vörunnar.

- Birtingarsmellihlutfall (CTR)

    Smellihlutfall er reiknað sem heildarfjölda birtingarsmella deilt með heildarfjölda birtinga.

## <a name="commerce-analytics-preview-installation"></a>Viðskiptagreiningar (Preview) uppsetning

> [!NOTE]
> Viðskiptagreining (Preview) er í forskoðun í Bandaríkjunum, Kanada, Bretlandi, Evrópu, Suðaustur-Asíu, Austur-Asíu, Ástralíu og Japan. Ef fjármála- og rekstrarumhverfi þitt er á einhverju af þessum svæðum geturðu virkjað þennan eiginleika í umhverfi þínu með því að nota Microsoft Dynamics Lífsferilsþjónusta (LCS). Áður en þú getur notað þennan eiginleika skaltu skoða [Stilla útflutning í Azure Data Lake](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).

### <a name="enable-and-configure-commerce-analytics-preview"></a><a name="enableCommerceAnalytics"></a> Virkja og stilla viðskiptagreiningu (forskoðun)

Til að setja upp Commerce Analytics (Preview) verður þú að hafa heimildir til að búa til tilföng í Azure áskrift. Þú verður líka að hafa heimildir til að setja upp viðbætur í LCS. 

Til að virkja og stilla viðskiptagreiningu (forskoðun) skaltu fylgja þessum skrefum.

1. [Virkjaðu og stilltu Export to Data Lake viðbótina](#enableExportToDataLake).
1. [Settu upp og stilltu an Azure Synapse vinnurými](#configureAzureSynapse).
1. [Bættu leyndarmálum við lyklahólfið](#addSecrets).
1. [Virkjaðu og stilltu Commerce analytics (Preview) viðbótina](#enableCommerceAnalyticsAddin).
1. [Settu upp Power BI sniðmát app](#powerbi).

### <a name="enable-and-configure-the-export-to-data-lake-add-in"></a><a name="enableExportToDataLake"></a> Virkjaðu og stilltu Export to Data Lake viðbótina

> [!IMPORTANT]
> Þegar þú stillir Export to Data Lake viðbótina skaltu hreinsa **Rauntíma gagnabreytingar** gátreitinn á Uppsetningarsíðunni Export to Data Lake viðbót til að tryggja að gagnabreytingar í rauntíma séu ekki virkar. The **Rauntíma gagnabreytingar** eiginleiki er í forskoðun og er ekki studdur af Commerce Analytics eins og er. Ef þú virkjar eiginleikann mun Commerce Analytics ekki geta unnið úr gögnunum þínum í gagnavatninu og flest Power BI skýrslur sýna engin gögn.

Viðskiptagreining (Preview) byggir á Flytja út í Data Lake eiginleikann til að flytja gögn Commerce höfuðstöðvar til Data Lake og halda gögnunum ferskum. Áður en þú stillir viðskiptagreiningu (Forskoðun) skaltu virkja og stilla Export to Data Lake með því að fylgja skrefunum í [Stilla útflutning í Azure Data Lake](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).

Á meðan þú stillir Export to Data Lake viðbótina skaltu skrifa niður eftirfarandi upplýsingar, því þú verður að slá þær inn síðar:

- <a name="keyVault"></a> Domain Name System (DNS) nafn lykilhólfsins sem þú gafst upp.
- Leyndarnöfnin sem þú gafst upp og innihalda auðkenni forritsins og leyndarmál forritsins. Fyrir frekari upplýsingar, sjá [Bættu leyndarmálum við lyklahólfið](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#addsecrets).

### <a name="install-and-configure-an-azure-synapse-workspace"></a><a name="configureAzureSynapse"></a> Settu upp og stilltu an Azure Synapse vinnurými

Commerce Analytics (Preview) krefst þess að Synapse SQL on-demand sé útvegað í þínum Azure Synapse vinnurými. Til að setja upp og stilla Azure Synapse vinnusvæði, fylgdu þessum skrefum.

1. Settu upp an Azure Synapse vinnusvæði í Azure áskriftinni þinni. Fyrir frekari upplýsingar, sjá [Flýtiræsing: Búðu til Synapse vinnusvæði](/azure/synapse-analytics/quickstart-create-workspace).
1. <a name="serverlessep"></a> Eftir að vinnusvæðið hefur verið útvegað skaltu opna yfirlitssíðu tilfanga og taka eftir **Serverlaus SQL endapunktur** gildi. Þú verður að geyma þetta gildi í lyklahólfinu í næsta hluta.
1. Á yfirlitssíðunni skaltu velja **Opnaðu Synapse Studio** hlekkur til að opna Azure Synapse Stúdíó fyrir vinnusvæðið þitt.
1. Veldu **Stjórna** á vinstri valmyndinni. Til að sjá valmyndarnöfnin gætirðu þurft að velja útvíkkunartengilinn á vinstri valmyndinni.
1. Undir **Öryggishópur**, veldu **Aðgangsstýring**. 
1. Veljið **Bæta við**.
1. Í **Bæta við hlutverkaúthlutun** glugga, stilltu valkostina eins og lýst er í eftirfarandi töflu.

    | Valkostur | Gildi |
    |--------|-------|
    | Umfang | Veldu **Vinnurými**. |
    | Hlutverk | Veldu **Synapse SQL stjórnandi**.|
    | Velja notanda | Leitaðu að nafni forritsins sem þú [búin til við uppsetningu á Export to Data Lake viðbótinni](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#createapplication). Þegar forritið birtist í leitarniðurstöðum skaltu velja það. Umsóknin mun nú birtast í **Valdir notendur, hópar eða þjónustustjórar** kafla. |

1. Veldu **Sækja um** til að klára hlutverkaúthlutunina. Forritinu eru veitt Synapse SQL stjórnandaréttindi. Þess vegna getur það búið til nauðsynlegar skoðanir við uppsetningu á Commerce Analytics (Preview) LCS viðbótinni.

### <a name="add-secrets-to-the-key-vault"></a><a name="addSecrets"></a> Bættu leyndarmálum við lyklahólfið

Í sama [lyklahólf](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#createkeyvault) sem þú notaðir á meðan þú stilltir Export to Data Lake viðbótina, verður þú að bæta við leyndarmálunum sem eru sýnd í eftirfarandi töflu. Fyrir hvert leyndarmál verður þú að gefa upp leyndarmál og tilgreint gildi.

| Tillaga um leyndarmál | Leynilykill | Dæmi um leyndarmál |
|---------|---------|---------|
| synapse-sql-þjónn | Serverlausa SQL endapunktsgildið sem þú bentir á meðan þú [stillti Azure Synapse vinnurými](#serverlessep). | `test-ondemand.sql.azuresynapse.net` |
| <a name="roUser"></a> readonly-sql-pwd | Lykilorðið sem á að setja fyrir SQL-skrifvarinn notanda. The Power BI skýrsla mun nota þetta lykilorð til að tengjast netþjónslausu SQL. Til að stilla lykilorðið skaltu fylgja lykilorðareglum fyrirtækisins þíns. | |

### <a name="enable-and-configure-the-commerce-analytics-preview-add-in"></a><a name="enableCommerceAnalyticsAddin"></a> Virkjaðu og stilltu Commerce analytics (Preview) viðbótina

Til að setja upp Commerce analytics (Preview) viðbótina í LCS verður þú að vera umhverfisstjóri í LCS fyrir umhverfið sem þú ætlar að nota.

Til að setja upp og stilla Commerce Analytics (Preview) viðbótina skaltu fylgja þessum skrefum.

1. Skrá inn [LCS](https://lcs.dynamics.com/), og farðu í umhverfið þitt.
2. Á **Umhverfi** síðu, á **Umhverfisviðbætur** flipa, veldu **Settu upp nýja viðbót**.
3. Veldu í glugganum **Viðskiptagreining (Forskoðun)**.
4. Í **Setja upp viðbót** valmynd, sláðu inn eftirfarandi upplýsingar.

    | Upplýsingar | Uppruni | Dæmi um gildi |
    |---|---|---|
    | Azure Active Directory(Azure AD) Auðkenni leigjanda | Skráðu þig inn á [Azure gátt](https://portal.azure.com/), og opnaðu **Azure Active Directory** þjónustu. Opnaðu síðan **Eiginleikar** síðu og afritaðu gildið í **Auðkenni leigjanda** sviði. | `72f988bf-0000-0000-00000-2d7cd011db47` |
    | DNS nafn Azure lykilhólfsins þíns | Sláðu inn DNS nafn lykilhólfsins þíns. Þú hefðir átt að skrá þetta gildi á meðan þú [stillti Export to Data Lake viðbótina](#keyVault). | `https://contosod365datafeedpoc.vault.azure.net/` |
    | Leyndarheiti sem inniheldur auðkenni forritsins | Sláðu inn leynda nafnið sem geymir auðkenni forritsins. Þú hefðir átt að skrá þetta gildi á meðan þú [stillti Export to Data Lake viðbótina](#keyVault). | `app-id` |
    | Leyndarheiti sem inniheldur leyndarmál forritsins | Sláðu inn leyndarmálið sem geymir leyndarmál forritsins. Þú hefðir átt að skrá þetta gildi á meðan þú [stillti Export to Data Lake viðbótina](#keyVault). | `app-secret` |
    | Leyndarheiti sem inniheldur netþjónslausa SQL endapunkt fyrir Azure Synapse | Sláðu inn leyndarmálið sem geymir netþjónslausa SQL endapunktinn. Þú hefðir átt að búa til leyndarmálið á meðan þú [bætti leyndarmálum við lykilgildið](#addSecrets). | `synapse-sql-server` |
    | Leyndarheiti sem inniheldur lykilorðið til að setja fyrir SQL-skrifvarða notendur í Azure Synapse | Sláðu inn leyndarmálið sem geymir lykilorðið til að stilla fyrir netþjónslausan SQL-skrifvarinn notanda. Þessi notandi verður búinn til fyrir þig og ætti að vera notaður í Power BI skýrslu til að tengjast serverlausa SQL netþjóninum. Þú hefðir átt að búa til leyndarmálið á meðan þú [bætti leyndarmálum við lykilgildið](#addSecrets). | `readonly-sql-pwd` |

1. Samþykktu skilmála tilboðsins með því að velja gátreitinn og velja síðan **Settu upp**.

    Kerfið setur upp og stillir Commerce analytics (Preview) viðbótina fyrir umhverfið. Þetta ferli gæti tekið nokkrar mínútur. Eftir að því er lokið, **Viðskiptagreining (Forskoðun)** ætti að vera skráð á **Umhverfi** síðu, og staðan ætti að vera **Uppsett**.

### <a name="install-the-power-bi-template-app"></a><a name="powerbi"></a> Settu upp Power BI sniðmát app

Til að setja upp Power BI sniðmátsforrit fyrir viðskiptagreiningu (Preview), fylgdu þessum skrefum.

1. Skráðu þig inn á [Power BI gátt](https://powerbi.microsoft.com/) með því að nota auðkenni fyrirtækisins þíns.
1. Settu upp viðskiptagreininguna (Preview)Power BI sniðmát app með því að fara á [https://aka.ms/cdireport-installapp](https://aka.ms/cdireport-installapp). Að öðrum kosti, heimsækja [AppSource síðu fyrir Dynamics 365 Commerce Greining](https://appsource.microsoft.com/product/power-bi/dynamics-365-commerce.dydnamics-365-commerce-analytics), og veldu **Náðu í það núna**.
1. Ef þú setur forritið upp í fyrsta skipti skaltu sleppa áfram í skref 5. Ef þú hefur sett það upp áður gilda eftirfarandi valkostir til að uppfæra forritið:

    - **Uppfærðu vinnusvæðið og appið** - Uppfærðu núverandi sniðmátsforrit og skrifaðu yfir núverandi forritastillingar þínar, svo sem heiti appstilviks og leyfisstillingar.
    - **Uppfærðu aðeins efni á vinnusvæði án þess að uppfæra forritið** - Uppfærðu núverandi sniðmátsforrit, en haltu núverandi forritastillingum þínum. *Þessi valkostur er ráðlagður valkostur fyrir appuppfærslur.*
    - **Settu upp annað eintak af forritinu á nýtt vinnusvæði** – Búðu til nýtt vinnusvæði og búðu til afrit af núverandi sniðmátsforriti í því. Núverandi vinnurými verður óbreytt.

1. Veldu einn af uppfærsluvalkostunum og veldu síðan **Settu upp**.
1. Opnaðu uppsetta appið með því að velja **Forrit** í vinstri glugganum og veldu síðan appið.
1. Tengdu forritið við gagnagjafann þinn með því að velja **Tengdu**. Ef þú hefur sett upp forritið áður skaltu velja **Tengdu gögnin þín** hlekkur í gulu skilaboðastikunni.
1. Stilltu eftirfarandi reiti.

    | Reitur | Gildi |
    |---|---|
    | Þjónn | Sláðu inn netþjónslausa SQL endapunktinn sem þú skrifaðir eftir á eftir þér [búið til Azure Synapse vinnurými](#serverlessep). |
    | Gagnagrunnur | Koma inn **CommerceAnalytics**. |
    | Tungumál | Veldu gildi á listanum. Þessi reitur er notaður fyrir staðbundin vöru- og flokkunarheiti. Gildið er hástöfum. |
    | Dagsetningarbil | Veldu gildi á listanum. Gögn fyrir valinn fjölda mánaða verða flutt inn í Power BI gagnasafn. Gildið sem þú velur hefur áhrif á stærð gagnasafnsins og þann tíma sem þarf til samstillingar. |

1. Veljið **Næst**. Þegar þú ert beðinn um að slá inn skilríki fyrir tengingu við Azure Synapse SQL gagnagrunnur, stilltu svæðisgildin eins og sýnt er í eftirfarandi töflu.

    | Reitur | Gildi |
    |---|---|
    | Sannvottunaraðferð | Veldu **Basic**. |
    | Notandanafn | Koma inn **skýrsluskrifaðeins notanda**. |
    | Aðgangsorð | Sláðu inn lykilorðið sem þú [geymt fyrir SQL-skrifvarinn notanda í lyklageymslunni](#roUser). |

1. Veldu **skráðu þig inn og tengdu**.
1. Bíddu þar til gagnasafnið hefur verið uppfært. Veldu síðan **Breyta app** til að opna App vinnusvæðið, þar sem þú getur skoðað uppfærslustöðu gagnasafnsins. Í forritavinnusvæðinu geturðu einnig valfrjálst sett upp sjálfvirkar uppfærsluáætlanir fyrir gagnasafnið þitt, stjórnað heimildum og endurnefna forritatilvikið.

### <a name="privacy"></a><a name="privacy"></a>Persónuvernd

Persónuvernd þín er okkur mikilvæg. Frekari upplýsingar má finna í [tilkynningu okkar um persónuvernd](https://go.microsoft.com/fwlink/?LinkId=521839).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
