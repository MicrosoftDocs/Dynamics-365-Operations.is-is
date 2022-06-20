---
title: Commerce-greining (forútgáfa)
description: Þessi grein útskýrir hvernig á að setja upp og nota greiningargetu í Microsoft Dynamics 365 Commerce.
author: AamirAllaq
ms.date: 02/24/2022
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: 2021-11-12
ms.openlocfilehash: 9ffa0affa0b80af65dd2aa37ef2fe969752ae332
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887167"
---
# <a name="commerce-analytics-preview"></a>Commerce-greining (forútgáfa)

[!include [banner](includes/banner.md)]

Þessi grein útskýrir hvernig á að setja upp Commerce analytics (Preview), hagnýtu greiningargetuna sem er innifalinn í Microsoft Dynamics 365 Commerce.

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
- Gögn eru framleidd af öðrum kerfum, svo sem Dynamics 365 Connected Spaces.

#### <a name="step-2-ingestion-and-pre-processing"></a>Skref 2: Inntaka og forvinnsla

Viðskiptagögn fara til Commerce HQ annað hvort beint (þegar um er að ræða pantanir sem eru teknar beint í Commerce HQ viðskiptavininn) eða í gegnum Commerce Scale Unit (þegar um er að ræða pantanir sem eru teknar á POS, í rafrænum viðskiptum eða sérsniðnum viðskiptavinir sem nota Headless Commerce).

Eiginleikinn Flytja út í gagnavatn er síðan notaður til að afrita viðskiptagögnin í gagnavatnið þitt sem hrá gögn. Í gagnavatninu eru hrágögnin geymd í Töflur möppunni.

Gögn um vefvirkni rafræn viðskipti eru send beint í gagnavatnið. Gögn sem eru framleidd af öðrum kerfum, svo sem Dynamics 365 Connected Spaces, er sent beint í gagnavatnið af þessum kerfum.

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

- Síðubirtingar

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

Nafnlaus gestur á netverslunarsíðunni þinni er auðkenndur á grundvelli tiltekins vafra og tiltekins tækis sem notandinn notar. Commerce Analytics fylgist ekki með nafnlausum gestum í mismunandi vöfrum eða tækjum. Nafnlaus gestur sem notar sama vafrann á sama tæki er auðkenndur á mörgum notendafundum, þar til annað hvort eru skyndiminnisgögn vafrans hreinsuð eða tímabil (venjulega 12 mánuðir) líður, hvort sem kemur fyrst fram.

Ef gestir vafra um netverslunarsíðuna þína á meðan þeir eru skráðir inn getur Commerce Analytics veitt frekari upplýsingar um þau. Þessar upplýsingar eru byggðar á núverandi sambandi sem fyrirtækið þitt hefur við gesti vegna fyrri kaupa þeirra á öllum Dynamics 365 Commerce söluleiðum (þ.m.t. posa, netverslun og símaveri). Viðbótarupplýsingarnar innihalda endurstillingu, lengd tengsla, líftíma og tíðnigögn.

- Framlegð gesta
- Meðalpantanir gesta
- Meðalsala gesta
- Fjöldi gesta í netverslun

    - Eftir dagsetningu
    - Eftir staðsetningu

        Eins og er, Commerce analytics getur veitt aðeins land / svæði-láréttur flötur korn fyrir staðsetningu innsýn fyrir e-verslun gestir.

    - Með endurhæfingu

        Tíðni er reiknuð út frá fjölda daga frá síðustu viðskiptatengslum viðskiptavinar við fyrirtækið. Eins og er, tekur nýleg ekki tillit til þátttökumerkja sem ekki eru viðskipti, eins og vefskoðunarvirkni í rafrænum viðskiptum.

    - Eftir lengd vensla

        Lengd tengsla er reiknuð út frá fjölda daga frá því viðskiptamannafærsla var stofnuð í kerfinu.

    - Eftir líftíma (LTV)

        LTV er reiknað út frá heildarupphæðinni sem viðskiptavinur eyðir yfir allt Dynamics 365 Commerce sölurásir (þar á meðal POS, rafræn viðskipti og símaver).

    - Eftir tíðni

        Tíðni er reiknuð út frá viðskiptatengslum viðskiptavinar við fyrirtækið. Eins og er, tekur tíðnin ekki tillit til þátttökumerkja sem ekki eru viðskipti, eins og vefskoðunarvirkni í rafrænum viðskiptum.

#### <a name="impressions"></a>Birtingar

Far er ein sýn á vöru sjón af e-verslun gestur. Til dæmis fer netverslunargestur á heimasíðu e-verslun vefsíðunnar þinnar og skoðar jógamottuvöru í söluhæstu **listaeiningunni**. Gesturinn skoðar síðan sömu jógamottuvöruna í **Picks fyrir þig** listaeiningu. Í þessu tilfelli eru tvær vöru birtingar.

Eins og er eru birtingar raktar á eftirfarandi fleti:

- Listar (til dæmis **, Mælt með**, **Söluhæsta**, **Val fyrir þig** og **Stefna**)
- Körfueining
- Gámur leitarniðurstöðu
- Gámur leitarniðurstöður tegundar

Eins og er eru vörur sem eru gerðar í hringekjueiningu eða í sérsniðnu myndefni ekki taldar með í birtingartengdum mælikvörðum.

Síðan **Birtingarskýrslan** inniheldur eftirfarandi mælikvarða:

- Birtingarfjöldi

    - Eftir síðugerð og kerfiseiningu

        Síðugerð er almenn gerð síðu sem er skilgreind fyrir hverja síðu á vefverslunarvefnum þínum. Gerð einingar er sú gerð sjónræns kerfiseiningar rafrænna viðskipta sem varan er sýnd í.

        Til að skoða birtingar eftir einingum gætirðu þurft að kafa niður í síðuna og myndefni einingarinnar.

    - Eftir vöru
    - Eftir innskráðan notanda stöðu
    - Eftir dagsetningu

- Birtingarsmelltufjöldi

    Birtingarsmellur á sér stað þegar netverslunargestur velur sjónræna vöru. Venjulega er gesturinn síðan fluttur á upplýsingasíðu vörunnar fyrir vöruna.

- Smellihraði birtingar (CTR)

    CTR er reiknað sem heildarfjöldi birtingarsmella deilt með heildarfjölda birtinga.

## <a name="commerce-analytics-preview-installation"></a>Uppsetning Commerce Analytics (Preview)

> [!NOTE]
> Commerce Analytics (Preview) er í forskoðun í Bandaríkjunum, Kanada, Bretlandi, Evrópu, Suðaustur-Asíu, Austur-Asíu, Ástralíu og Japan. Ef fjármála- og rekstrarumhverfið þitt er á einhverjum þessara svæða er hægt að virkja þennan eiginleika í umhverfinu með því að nota Microsoft Dynamics Lifecycle Services (LCS). Áður en þú getur notað þessa aðgerð, sjá [Configure export to Azure Data Lake](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).

### <a name="enable-and-configure-commerce-analytics-preview"></a><a name="enableCommerceAnalytics"></a> Virkja og samskipa Commerce Analytics (Forskoðun)

Til að setja upp Commerce analytics (Preview) verður þú að hafa heimildir til að búa til tilföng í Azure áskrift. Þú verður einnig að hafa heimildir til að setja upp viðbætur í LCS.

Til að virkja og skilgreina Commerce analytics (Preview) skal fylgja þessum skrefum.

1. [Senda inn skjámyndina Forskoðun inntaka fyrir Commerce Analytics (Preview)](#joinPreview)
2. [Virkja og stilla innbótina Flytja út í](#enableExportToDataLake) gagnavatn.
3. [Setja upp og skilgreina Azure Synapse vinnusvæði](#configureAzureSynapse).
4. [Bættu leyndarmálum við lykilhvelfinguna](#addSecrets).
5. [Virkja og skilgreina innbótina](#enableCommerceAnalyticsAddin) Commerce Analytics (Preview).
6. [Settu upp sniðmátsforritið Power BI](#powerbi).

### <a name="submit-the-preview-intake-form-for-commerce-analytics-preview"></a><a name="joinPreview"></a> Senda inn skjámyndina Forskoðun inntaka fyrir Commerce Analytics (Preview)

Senda inn skjámyndina [Forskoðun inntaka fyrir Commerce Analytics (Preview)](https://forms.office.com/r/vW5VLJGXZ2). Eftir að beiðni þín hefur verið afgreidd verður staðfestingartölvupóstur sendur á netfangið sem þú gafst upp í eyðublaðinu.

### <a name="enable-and-configure-the-export-to-data-lake-add-in"></a><a name="enableExportToDataLake"></a> Virkja og stilla innbótina Flytja út í gagnavatn

> [!IMPORTANT]
> Þegar þú samskipar Innbótinni Flytja út í gagnavatn skal hreinsa **gátreitinn Rauntímagögn breyta** gátreitnum á síðunni Flytja út í gagnavatnsinnbót til að tryggja að rauntímagagnabreytingar séu ekki virkar. Eiginleikinn **Rauntímagagnabreytingar** er í forskoðun og er ekki studdur af Commerce Analytics eins og er. Ef þú virkjar aðgerðina mun Commerce Analytics ekki geta unnið úr gögnunum þínum í gagnavatninu og flestar skýrslur þínar Power BI munu ekki sýna nein gögn.

Commerce Analytics (Preview) byggir á aðgerðinni Export to Data Lake til að flytja út gögn um höfuðstöðvar Commerce í Data Lake og halda gögnunum ferskum. Áður en Commerce analytics (Preview) er samskipað skal virkja og stilla Flytja út í Gagnavatn með því að fylgja skrefunum í Configure export to [Azure Data Lake](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).

Þó að þú stillir innfluttingu Flytja út í gagnavatn skaltu gera athugasemd við eftirfarandi upplýsingar, því þú verður að slá það inn síðar:

- <a name="keyVault"></a> Heiti lénsheitiskerfisins (DNS) lykilhvelfingarinnar sem þú gafst upp.
- Leynilegheitin sem þú gafst upp og innihalda umsóknarkennið og umsóknarleyndarmálið. Frekari upplýsingar er að finna í [Bæta leyndarmálum við lyklahvelfinguna](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#addsecrets).

### <a name="install-and-configure-an-azure-synapse-workspace"></a><a name="configureAzureSynapse"></a> Setja upp og skilgreina Azure Synapse vinnusvæði

Commerce Analytics (Preview) krefst þess að Synapse SQL eftir þörfum sé veitt á vinnusvæðinu þínu Azure Synapse. Til að setja upp og skilgreina Azure Synapse vinnusvæði skal fylgja þessum skrefum.

1. Azure Synapse Settu upp vinnusvæði í Azure áskriftinni þinni. Sjá Quickstart: Create a Synapse workspace fyrir frekari [upplýsingar](/azure/synapse-analytics/quickstart-create-workspace).
1. <a name="serverlessep"></a> Eftir að vinnusvæðið hefur verið gefið út skal opna yfirlitssíðuna tilfangayfirlit og gera athugasemd við **gildið Serverless SQL endpoint**. Þú verður að geyma þetta gildi í lykilhvelfingunni í næsta kafla.
1. Á yfirlitssíðunni skal velja tengilinn **Opna Synapse Studio** til að opna Azure Synapse Stúdíó fyrir vinnusvæðið þitt.
1. Veldu **Stjórna** á vinstri valmyndinni. Til að sjá heiti valmyndarinnar gætirðu þurft að velja stækka tengilinn í vinstri valmyndinni.
1. Undir **Öryggisflokkur** skal velja **Aðgangsstýring**. 
1. Veljið **Bæta við**.
1. Í rúðunni **Bæta við úthlutun** hlutverka skal stilla valkostina eins og lýst er í eftirfarandi töflu.

    | Valkostur | Gildi |
    |--------|-------|
    | Umfang | Veljið **vinnusvæði**. |
    | Hlutverk | Veljið **Synapse SQL-kerfisstjóra**.|
    | Velja notanda | Leitaðu að heiti forritsins sem þú [bjóst til við uppsetningu á innbótinni Flytja út í](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#createapplication) Gagnavatn. Þegar forritið birtist í leitarniðurstöðunum skal velja það. Forritið mun nú birtast í hlutanum **Valdir notendur, hópar eða þjónustustjórar**. |

1. Veljið **Nota** til að ljúka hlutverkaúthlutuninni. Umsóknin er veitt Synapse SQL Administrator réttindi. Þess vegna getur það búið til nauðsynleg yfirlit við skilgreiningu á LCS-innbót Commerce Analytics (Preview).

### <a name="add-secrets-to-the-key-vault"></a><a name="addSecrets"></a> Bæta leyndarmálum við lykilhvelfinguna

Í sömu [lykilhvelfingu](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#createkeyvault) og þú notaðir þegar þú samskipaðir innbótinni Flytja út í gagnavatn verður að bæta við leyndarmálunum sem sýndar eru í eftirfarandi töflu. Fyrir hvert leyndarmál verður þú að gefa upp leynilegt nafn og tilgreint gildi.

| Tillaga að leyninafni | Leynilykill | Dæmi um leyndargildi |
|---------|---------|---------|
| synapse-sql-server | Þjónslausa SQL endastöð gildið sem kom fram þegar [vinnusvæðið Azure Synapse var](#serverlessep) skilgreint. | `test-ondemand.sql.azuresynapse.net` |
| <a name="roUser"></a> readonly-sql-pwd | Aðgangsorðið sem á að stilla fyrir SQL skrifvarinn notanda. Skýrslan Power BI notar þetta aðgangsorð til að tengjast þjónslausum SQL. Til að stilla aðgangsorðið skal fylgja aðgangsorðareglum fyrirtækisins. | |

### <a name="enable-and-configure-the-commerce-analytics-preview-add-in"></a><a name="enableCommerceAnalyticsAddin"></a> Virkja og skilgreina Commerce analytics (Preview) viðbótina

Til að setja upp Commerce analytics (Preview) viðbótina í LCS verður þú að vera umhverfisstjóri í LCS fyrir umhverfið sem þú ætlar að nota.

Til að setja upp og skilgreina Commerce analytics (Preview) viðbótina skal fylgja þessum skrefum.

1. Skráðu þig inn á LCS [og farðu í](https://lcs.dynamics.com/) umhverfið þitt.
2. **Á síðunni Umhverfi** á flipanum **Viðbætur í** umhverfi skal velja **Setja upp nýja viðbót**.
3. Í svarglugganum skal velja **Commerce analytics (Preview)**.
4. **Í svarglugganum Innbót** uppsetningar eru eftirfarandi upplýsingar færðar inn.

    | Upplýsingar | Uppruni | Dæmi um gildi |
    |---|---|---|
    | Azure Active Directory(Azure AD) Kenni leigjanda | Skráðu þig inn á [Azure vefgáttina](https://portal.azure.com/) og opnaðu þjónustuna **Azure Active Directory**. Síðan er síðan **síðunni Eiginleikar** opnað og gildið afritað í reitnum **Kenni** leigjanda. | `72f988bf-0000-0000-00000-2d7cd011db47` |
    | DNS nafn Azure lyklahvelfingarinnar þinnar | Sláðu inn DNS-heiti lykilhvelfingarinnar. Þú ættir að hafa gert athugasemd við þetta gildi á meðan þú [samskipaðir Flytja út í](#keyVault) gagnavatnsinnbótina. | `https://contosod365datafeedpoc.vault.azure.net/` |
    | Leyniheiti sem inniheldur umsóknarkennið | Færið inn leyniheitið sem geymir kenni forritsins. Þú ættir að hafa gert athugasemd við þetta gildi á meðan þú [samskipaðir Flytja út í](#keyVault) gagnavatnsinnbótina. | `app-id` |
    | Leyniheiti sem inniheldur forritsleyndarmálið | Sláðu inn leyninafnið sem geymir leyndarmál forritsins. Þú ættir að hafa gert athugasemd við þetta gildi á meðan þú [samskipaðir Flytja út í](#keyVault) gagnavatnsinnbótina. | `app-secret` |
    | Leyniheiti sem inniheldur þjónslausa SQL endastöð fyrir Azure Synapse | Færið inn leyniheitið sem geymir þjónslausa SQL endastöðina. Þú ættir að hafa búið til leyndarmálið á meðan þú [bættir leyndarmálum við lykilgildið](#addSecrets). | `synapse-sql-server` |
    | Leyniheiti sem inniheldur aðgangsorðið sem á að stilla fyrir SQL-skrifvarna notendur í Azure Synapse | Færið inn leyniheitið sem geymir aðgangsorðið sem á að stilla fyrir þjónlausa SQL skrifvarna notandann. Þessi notandi verður búinn til fyrir þig og ætti að vera notaður í Power BI skýrslu til að tengjast serverlausa SQL netþjóninum. Þú hefðir átt að búa til leyndarmálið á meðan þú [bætti leyndarmálum við lykilgildið](#addSecrets). | `readonly-sql-pwd` |

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
