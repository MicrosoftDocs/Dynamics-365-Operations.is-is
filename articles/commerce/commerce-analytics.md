---
title: Viðskiptagreining (Forskoðun)
description: Þetta efni útskýrir hvernig á að setja upp og nota greiningargetu í Microsoft Dynamics 365 Commerce.
author: AamirAllaq
ms.date: 11/23/2021
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: 2021-11-12
ms.openlocfilehash: 8cfe2af756315b5be3eb22d99376a96166fffc52
ms.sourcegitcommit: f9fca3d55b47e615e5ef64669dab184e057ec234
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/23/2021
ms.locfileid: "7862774"
---
# <a name="commerce-analytics-preview"></a>Viðskiptagreining (Forskoðun)

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
- SQL skoðanir í Azure Synapse Greining
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

Gögn um vefvirkni rafræn viðskipti eru send beint í gagnavatnið. Gögn sem eru framleidd af öðrum kerfum, svo sem Dynamics 365 Connected Spaces, er sent beint í gagnavatnið af þessum kerfum.

#### <a name="step-3-transformation-and-aggregation"></a>Skref 3: Umbreyting og samsöfnun

Eftir að hrá gögn eru í gagnavatninu þínu les Commerce greiningarþjónustan þau, umbreytir þeim, safnar þeim saman og skrifar þau aftur í gagnavatnið í formi rökréttra eininga (í Entities möppunni) og uppsafnaðra mælinga (í Ontologies möppunni ).

#### <a name="step-4-querying"></a>Skref 4: Fyrirspurnir

Azure Synapse Greining er notuð til að spyrjast fyrir um gögn í gagnavatninu þínu í gegnum Transact-SQL (T-SQL) viðmót. Þetta viðmót inniheldur SQL skoðanir. SQL skoðanir gera sameinaða fyrirspurnir um gögn í gagnavatninu, annað hvort beint í gegnum T-SQL biðlara (fyrir sértæka greiningu) eða í gegnum sjónrænt tól eins og Power BI.

#### <a name="step-5-modeling-and-serving"></a>Skref 5: Líkangerð og framreiðslu

Gögn sem spurt er um af Azure Synapse Greining fer til Power BI merkingarfræðilegu líkaninu. Það fer eftir tegund gagna, þau eru annað hvort reglulega flutt inn í minnið Power BI eða beint fyrirspurn á keyrslutíma.

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

####  <a name="top-level-filters"></a><a name="TopLevelFilters"></a> Síur á hæsta stigi

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
    - Tegund

####  <a name="products"></a><a name="ProductsPage"></a> Vörur

- Sala
- Spássía
- Vöruskil

####  <a name="customers"></a><a name="CustomersPage"></a> Viðskiptavinir

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

Eins og er eru vörur sem eru birtar í hringekjueiningu eða í sérsniðnu myndefni ekki taldar með í birtingartengdum mælikvörðum.

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
> Viðskiptagreining (Preview) er í forskoðun í Bandaríkjunum, Kanada, Bretlandi, Evrópu, Suðaustur-Asíu, Austur-Asíu, Ástralíu og Japan. Ef þín Finance and Operations umhverfi er á einhverju af þessum svæðum geturðu virkjað þennan eiginleika í umhverfi þínu með því að nota Microsoft Dynamics Lífsferilsþjónusta (LCS). Áður en þú getur notað þennan eiginleika skaltu skoða [Stilla útflutning í Azure Data Lake](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).

### <a name="enable-and-configure-commerce-analytics-preview"></a><a name="enableCommerceAnalytics"></a> Virkja og stilla viðskiptagreiningu (forskoðun)

Til að setja upp Commerce Analytics (Preview) verður þú að hafa heimildir til að búa til tilföng í Azure áskrift. Þú verður líka að hafa heimildir til að setja upp viðbætur í LCS. Hér er yfirlit yfir skrefin:

1. [Sendu forskoðunarinntökueyðublaðið fyrir viðskiptagreiningu (Preview)](#joinPreview).
2. [Virkjaðu og stilltu Export to Data Lake](#enableExportToDataLake).
3. [Virkjaðu og stilltu Commerce analytics (Preview) viðbótina](#enableCommerceAnalyticsAddin).
4. [Búðu til samnýtt undirskrift (SAS) tákn fyrir geymslureikninginn þinn](#getSASToken).
5. [Sækja uppsetningarforskriftir fyrir Azure Synapse skoðanir](#downloadSynapseDeploymentScripts).
6. [Settu upp og stilltu an Azure Synapse vinnurými](#configureAzureSynapse).
7. [Settu upp Power BI sniðmát app](#powerbi).

### <a name="submit-the-preview-intake-form-for-commerce-analytics-preview"></a><a name="joinPreview"></a> Sendu forskoðunarinntökueyðublaðið fyrir viðskiptagreiningu (Preview)

Sendu inn [Forskoða inntökueyðublað fyrir viðskiptagreiningu (Forskoðun)](https://forms.office.com/r/vW5VLJGXZ2). Gefðu allt að þrjá virka daga til að vinna úr eyðublaðinu. Eftir að það hefur verið unnið verður staðfestingarpóstur sendur á netfangið sem þú gafst upp í eyðublaðinu.

### <a name="enable-and-configure-export-to-data-lake"></a><a name="enableExportToDataLake"></a> Virkjaðu og stilltu Export to Data Lake

Viðskiptagreining (Preview) byggir á Flytja út í Data Lake eiginleikann til að flytja út Commerce HQ gögn til Data Lake og halda gögnunum ferskum. Áður en þú stillir viðskiptagreiningu (Forskoðun) skaltu virkja og stilla Export to Data Lake með því að fylgja skrefunum í [Stilla útflutning í Azure Data Lake](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).

Á meðan þú ert að stilla Export to Data Lake skaltu skrá eftirfarandi upplýsingar, því þú verður að slá þær inn síðar:

- <a name="keyVault"></a> Domain Name System (DNS) heiti lyklahólfsins og leyndarheitin þar sem þú geymir auðkenni forritsins og forritsleyndarmálið. Fyrir frekari upplýsingar, sjá [Bættu leyndarmálum við lyklahólfið](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#addsecrets).
- <a name="storageAccount"></a> Heiti geymslureiknings fyrir Data Lake tilvikið. Fyrir frekari upplýsingar, sjá [Búðu til Data Lake Storage (Gen2) reikning í áskriftinni þinni](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#createsubscription).

### <a name="enable-and-configure-the-commerce-analytics-preview-add-in"></a><a name="enableCommerceAnalyticsAddin"></a> Virkjaðu og stilltu Commerce analytics (Preview) viðbótina

Til að setja upp Commerce analytics (Preview) viðbótina í LCS verður þú að vera umhverfisstjóri í LCS fyrir umhverfið sem þú ætlar að nota.

Til að setja upp og stilla Commerce Analytics (Preview) viðbótina skaltu fylgja þessum skrefum.

1. Skrá inn [LCS](https://lcs.dynamics.com/), og farðu í umhverfið þitt.
2. Á **Umhverfi** síðu, á **Umhverfisviðbætur** flipa, veldu **Settu upp nýja viðbót**.
3. Veldu í glugganum **Viðskiptagreining (Forskoðun)**.

    Ef **Viðskiptagreining (Forskoðun)** er ekki á listanum skaltu ganga úr skugga um að þú hafir gengið í innherjaáætlunina.

4. Í **Setja upp viðbót** valmynd, sláðu inn eftirfarandi upplýsingar.

    | Upplýsingar | Uppruni | Dæmi um gildi |
    |---|---|---|
    | Azure AD Leigjanda auðkenni fyrir umhverfið þitt | Skráðu þig inn á [Azure gátt](https://portal.azure.com/), og opnaðu **Azure Active Directory** þjónustu. Opnaðu síðan **Eiginleikar** síðu og afritaðu gildið í **Auðkenni skráa** sviði. | 72f988bf-0000-0000-00000-2d7cd011db47 |
    | DNS nafn lykilhólfsins þíns | Sláðu inn [DNS nafn](#keyVault) af lyklageymslunni þinni. Þú hefðir átt að skrá þetta gildi í fyrri hlutanum. | `https://contosod365datafeedpoc.vault.azure.net/` |
    | Leyndarmál sem inniheldur umsóknareitið | Sláðu inn [leynilegt nafn sem geymir auðkenni forritsins](#keyVault). Þú hefðir átt að skrá þetta gildi í fyrri hlutanum. | forrit-auðkenni |
    | Leyndarmál sem inniheldur umsóknarleyndarmálið | Sláðu inn [leyndarmál nafn sem geymir leyndarmál forritsins](#keyVault). Þú hefðir átt að skrá þetta gildi í fyrri hlutanum. | forrit-leyndarmál |

5. Samþykktu skilmála tilboðsins með því að velja gátreitinn og velja síðan **Settu upp**.

    Kerfið setur upp og stillir Commerce analytics (Preview) viðbótina fyrir umhverfið. Þetta ferli gæti tekið nokkrar mínútur. Eftir að því er lokið, **Viðskiptagreining (Forskoðun)** ætti að vera skráð á **Umhverfi** síðu, og staðan ætti að vera **Uppsett**.

### <a name="generate-a-sas-token-for-your-storage-account"></a><a name="getSASToken"></a> Búðu til SAS tákn fyrir geymslureikninginn þinn

SAS tákn gerir ytri aðilum kleift að fá aðgang að geymslureikningnum þínum og hafa tiltekið sett af forréttindum í takmarkaðan tíma. Azure Synapse mun nota SAS táknið til að fá aðgang að undirliggjandi gögnum í Data Lake.

> [!NOTE]
> Vegna þekktrar takmarkana á viðskiptagreiningum (Preview), the Azure Synapse tilvik mun missa aðgang að gagnavatninu þegar SAS táknið rennur út. Þess vegna, þegar þú býrð til SAS táknið, ættir þú að stilla hámarks fyrningardagsetningu sem öryggisreglur fyrirtækisins þíns leyfa.

Til að búa til SAS tákn skaltu fylgja þessum skrefum.

1. Í Azure gáttinni, farðu í [geymslureikning](#storageAccount) sem þú bjóst til á meðan þú stilltir Export to Data Lake.
2. Í vinstri glugganum, undir geymslureikningnum, veldu **Sameiginlegur aðgangur undirskrift**.
3. Á **SAS valkostir** síðu, stilltu eftirfarandi reiti.

    | Svæði | Gildi |
    |---|---|
    | Leyfileg þjónusta | Veldu **Blobbi**. |
    | Leyfðar tegundir tilfanga | Veldu **Þjónusta**, **·**, og **Hlutur**. |
    | Leyfilegar heimildir | Veldu **Lestu**, **·**, **·**, **·**, **við**, og **Búa til**. |
    | Útgáfuheimildir Blob | Veldu **Gerir kleift að eyða útgáfum**. |
    | Upphafs- og gildistími/tími | Stilltu upphafs- og lokadagsetningu og tíma fyrir SAS táknið eftir því sem við á. |
    | Leyfðar IP tölur | Hafa reitinn auðann. |
    | Leyfðar samskiptareglur | Veldu **Aðeins HTTPS**. |
    | Æskilegt leiðarstig | Veldu **Basic (sjálfgefið)**. |
    | Undirritunarlykill | Veldu **lykill 1** eða **lykill 2**, eftir því sem við á. |

4. Veldu **Búðu til SAS og tengistreng**.
5. Afritaðu gildið í **SAS tákn** reit og límdu það inn í textaritli eins og Notepad.

### <a name="download-the-deployment-scripts-for-azure-synapse-views"></a><a name="downloadSynapseDeploymentScripts"></a> Sækja uppsetningarforskriftir fyrir Azure Synapse skoðanir

Til að búa til og birta nauðsynlegar skoðanir í an Azure Synapse vinnusvæði, þú verður að keyra sett af skriftum. Fylgdu þessum skrefum til að hlaða niður skriftunum.

1. Á GitHub, farðu í [Microsoft/Dynamics365Commerce.Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions) geymsla (repo).
2. Sæktu forskriftirnar á staðbundna tölvuna þína með því að klóna endurhverfan eða hlaða því niður sem zip skrá.

### <a name="install-and-configure-an-azure-synapse-workspace"></a><a name="configureAzureSynapse"></a> Settu upp og stilltu an Azure Synapse vinnurými

Til að setja upp og stilla Azure Synapse vinnusvæði, fylgdu þessum skrefum.

1. Settu upp an Azure Synapse vinnusvæði í Azure áskriftinni þinni. Fyrir frekari upplýsingar, sjá [Flýtiræsing: Búðu til Synapse vinnusvæði](/azure/synapse-analytics/quickstart-create-workspace).
2. Í Notepad eða öðrum textaritli skaltu opna **SetupSynapse.sql** skriftuskrá úr möppunni á tölvunni þinni sem þú klónaðir eða halaðir niður Dynamics365Commerce.Solutions endurhverfinu í í fyrri hlutanum. Handritaskráin verður undir /Pipeline/CommerceAnalyticsSynapse/ möppunni. Í handritinu, skiptu staðsetningartexta út fyrir gildi eins og sýnt er í eftirfarandi töflu.

    | Staðsetningartexti | Gildi útskiptingar |
    |---|---|
    | staðhaldari_geymslureikningur | Nafnið á [geymslureikning](#storageAccount) sem þú bjóst til á meðan þú stilltir Export to Data Lake. |
    | <a name="phContainer"></a> staðhaldari_ílát | Heiti geymsluílátsins sem var búið til í Data Lake tilvikinu þínu eftir að þú settir upp Export to Data Lake viðbótina í LCS. Til að fá gámaheitið verður þú að nota Storage Explorer í Azure gáttinni til að skoða geymslureikninginn þinn. |
    | placeholder_sastoken | The [SAS tákn](#getSASToken) sem þú bjóst til. Vertu viss um að fjarlægja spurningarmerkið (**?**) frá upphafi SAS tákngildis. |
    | <a name="phUserPwd"></a> staðgengilslykilorð | Sterkt lykilorð að eigin vali. Skráðu þetta lykilorð. Það verður stillt sem lykilorð fyrir nýja **skýrsluskrifaðeins notanda** reikningur sem handritið býr til. Gerðu **ekki** sláðu inn lykilorðið á **sqladminuser** reikning. |

3. Afritaðu uppfært innihald handritsskrárinnar.
4. Í Azure gáttinni, farðu í nýja Azure Synapse vinnurými. Á **Yfirlit** síðu, veldu **Opnaðu Synapse Studio**.
5. Í Synapse Studio, veldu **Nýtt \> SQL handrit**, og límdu innihald skriftuskrárinnar inn í SQL skriftaritilinn.
6. Gakktu úr skugga um að **Notaðu gagnagrunn** reiturinn er stilltur á **húsbóndi**.
7. Veldu **Hlaupa**, og bíddu eftir að handritinu lýkur. Árangursrík framkvæmd skriftunnar mun búa til gagnagrunn fyrir Commerce greiningar, skilríki fyrir aðgang að gagnavatninu og skrifvarinn notendareikning sem Power BI mun nota til að tengjast Azure Synapse dæmi.
8. Á tölvunni þinni, opnaðu Windows PowerShell í stjórnunarham og farðu í /Pipeline/CommerceAnalyticsSynapse/ möppuna undir möppunni sem þú klónaðir eða halaðir niður Dynamics365Commerce.Solutions endurhverfunni í.
9. Settu upp Windows PowerShell keyrslustefnuna með því að keyra eftirfarandi skipun.

    ```powershell
    Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
    ```

10. Ef SQL Server PowerShell einingin er ekki þegar uppsett skaltu setja hana upp með því að keyra eftirfarandi skipun.

    ```powershell
    Install-Module sqlserver
    ```

    > [!NOTE]
    > Við uppsetningu einingarinnar gætirðu verið beðinn um að setja upp NuGet veitanda. Í þessu tilfelli skaltu velja **Y** að setja upp NuGet veitanda. Þú gætir líka verið beðinn um að viðurkenna að þú setur upp einingar frá ótraustri geymslu. Í þessu tilfelli skaltu velja **Y** til að halda áfram með uppsetninguna. Þú getur valfrjálst keyrt **Set-PSRepository** cmdlet til að treysta **PSGallery** geymsla.

11. Gefðu út Azure Synapse skoða með því að keyra eftirfarandi skipun.

    ```powershell
    .\PublishSynapseViews.ps1 -serverName SERVER_NAME -password PASSWORD -storageAccount STORAGE_ACCOUNT -containerName CONTAINER_NAME -datarootpath DATA_ROOT_PATH
    ```

    Þegar þú keyrir þessa skipun skaltu skipta um staðgengilsgildi eins og sýnt er í eftirfarandi töflu.

    | Staðgengilsgildi | Gildi útskiptingar |
    |---|---|
    | SERVER_NAME | Nafnið á Azure Synapse Serverlaus SQL endapunktur. Þú getur fengið þetta gildi frá **Yfirlit** síðu fyrir Azure Synapse vinnusvæði í Azure gáttinni. |
    | LYKILORÐ | Lykilorðið fyrir **sqladminuser** reikning. |
    | STORAGE_ACCOUNT | Heiti geymslureikningsins fyrir Data Lake. |
    | CONTAINER_NAME | Heiti gámsins sem var búið til af eiginleikanum Export to Data Lake. Þessi gámur er sami gámur og þú tilgreindir sem [staðhaldari_ílát](#phContainer) gildi í skrefi 2. |
    | DATA_ROOT_PATH | Möppuheitið undir ílátinu sem inniheldur öll gögnin. |

    > [!NOTE]
    > Þú getur fundið geymslureikningsheitið, gámaheitið og gagnarótarslóðina með því að nota Azure Storage vafra og Data Lake geymslureikninginn þinn í Azure gáttinni.

12. Bíddu eftir að handritinu lýkur. Árangursrík framkvæmd skriftunnar mun búa til SQL skoðanir í Azure Synapse Serverlaust SQL dæmi.

### <a name="install-the-power-bi-template-app"></a><a name="powerbi"></a> Settu upp Power BI sniðmát app

Til að setja upp Power BI sniðmátsforrit fyrir viðskiptagreiningu (Preview), fylgdu þessum skrefum.

1. Skráðu þig inn á [Power BI gátt](https://powerbi.microsoft.com/) með því að nota auðkenni fyrirtækisins þíns.
2. Settu upp viðskiptagreininguna (Preview)Power BI sniðmát app með því að fara á [https://aka.ms/cdireport-installapp](https://aka.ms/cdireport-installapp). Þú gætir fengið viðvörun sem segir að appið sé ekki skráð á AppSource. Velja **Setja upp**.
3. Ef þú setur forritið upp í fyrsta skipti skaltu sleppa áfram í skref 5. Ef þú hefur sett þetta forrit upp áður birtast eftirfarandi valkostir til að uppfæra forritið:

    - **Uppfærðu vinnusvæðið og appið** - Uppfærðu núverandi sniðmátsforrit og skrifaðu yfir núverandi forritastillingar þínar, svo sem heiti appstilviks og leyfisstillingar.
    - **Uppfærðu aðeins efni á vinnusvæði án þess að uppfæra forritið** - Uppfærðu núverandi sniðmátsforrit, en haltu núverandi forritastillingum þínum. *Þessi valkostur er ráðlagður valkostur fyrir appuppfærslur.*
    - **Settu upp annað eintak af forritinu á nýtt vinnusvæði** - Búðu til nýtt vinnusvæði og búðu til afrit af núverandi sniðmátsforriti í því. Núverandi vinnusvæði verður ósnortið.

4. Veldu einn af uppfærsluvalkostunum og veldu síðan **Settu upp**.
5. Opnaðu uppsetta appið með því að velja **Forrit** í vinstri glugganum og veldu síðan appið.
6. Tengdu forritið við gagnagjafann þinn með því að velja **Tengdu**. Ef þú hefur sett upp forritið áður skaltu velja **Tengdu gögnin þín** hlekkur í gulu skilaboðastikunni.
7. Stilltu eftirfarandi reiti.

    | Svæði | Gildi |
    |---|---|
    | Þjónn | Sláðu inn nafnið á Azure Synapse Serverlaus SQL endapunktur sem þú bjóst til í fyrri hlutanum. Þú getur fengið þetta gildi frá **Yfirlit** síðu fyrir Azure Synapse vinnusvæði í Azure gáttinni. |
    | Gagnagrunnur | Koma inn **CommerceAnalytics**. |
    | Tungumál | Veldu gildi á listanum. Þessi reitur er notaður fyrir staðbundin vöru- og flokkunarheiti. Gildið er hástöfum. |
    | Dagsetningarbil | Veldu gildi á listanum. Gögn fyrir valinn fjölda mánaða verða flutt inn í Power BI gagnasafn. Gildið sem þú velur hefur áhrif á stærð gagnasafnsins og þann tíma sem þarf til samstillingar. |

8. Veljið **Næst**. Þú ert beðinn um að slá inn skilríki fyrir tengingu við Azure Synapse SQL gagnagrunnur. Stilltu reitina eins og sýnt er í eftirfarandi töflu.

    | Svæði | Gildi |
    |---|---|
    | Sannvottunaraðferð | Veldu **Basic**. |
    | Notandanafn | Koma inn **skýrsluskrifaðeins notanda**. |
    | Aðgangsorð | Sláðu inn gildið sem þú hefur skipt út fyrir [staðgengilslykilorð](#phUserPwd) staðgengill í SetupSynapse.sql forskriftinni. Þetta lykilorð er lykilorðið fyrir **skýrsluskrifaðeins notanda** reikning. |

9. Veldu **skráðu þig inn og tengdu**.
10. Bíddu þar til gagnasafnið hefur verið uppfært. Veldu síðan **Breyta app** hnappinn til að opna forritavinnusvæðið, þar sem þú getur skoðað uppfærslustöðu gagnasafnsins. Í forritavinnusvæðinu geturðu einnig valfrjálst sett upp sjálfvirkar uppfærsluáætlanir fyrir gagnasafnið þitt, stjórnað heimildum og endurnefna forritatilvikið.

### <a name="privacy"></a><a name="privacy"></a>Persónuvernd

Persónuvernd þín er okkur mikilvæg. Frekari upplýsingar má finna í [tilkynningu okkar um persónuvernd](https://go.microsoft.com/fwlink/?LinkId=521839).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
