---
title: Viðskiptagreining (Forskoðun)
description: Þetta efni lýsir uppsetningu og notkun greiningargetu í Dynamics 365 Commerce.
author: AamirAllaq
ms.date: 11/15/2021
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: 2021-11-12
ms.openlocfilehash: 7f3e51cc3f7314bd33bca9e598bd0b1c9118caef
ms.sourcegitcommit: 9f8da0ae3dcf3861e8ece2c2df4f693490563d5e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/16/2021
ms.locfileid: "7817456"
---
# <a name="commerce-analytics-preview"></a>Viðskiptagreining (Forskoðun)

[!include [banner](includes/banner.md)]

Viðskiptagreining er hagnýtur greiningargeta sem er innifalin í Dynamics 365 Commerce. Þetta efni lýsir viðskiptagreiningum í smáatriðum og útskýrir hvernig á að setja það upp. 

## <a name="system-architecture"></a>Kerfisarkitektúr
### <a name="key-components"></a>Lykilþættir
Viðskiptagreining er samsett úr eftirfarandi lykilþáttum:
- Tilbúið til notkunar gagnvirkt Power BI skýrslur
- SQL skoðanir í Azure Synapse Greining
- Eininga- og verufræðigögn í Azure Data Lake
- Hrá gögn í Azure Data Lake

![Kerfisarkitektúr viðskiptagreiningar](media/CommerceAnalytics.png)

### <a name="data-flow"></a>Gagnaflæði
#### <a name="step-1-data-generation"></a>Skref 1: Gagnagerð
Gögn eru annaðhvort upprunnin sem viðskiptagögn eða hegðunargögn frá einni af eftirfarandi heimildum:
- Félagi í símaver sem notar viðskiptavin Commerce HQ til að vinna úr sölupöntunum
- Gjaldkeri á sölustað (POS) sem vinnur sölufærslur
- Sala búin til í sérsniðnum forritum með Headless Commerce (Commerce Scale Unit)
- E-verslun kaupandi skoðar e-verslun vefsíðu þína 
- Kaupandi í rafrænum viðskiptum sem leggur inn pöntun á vefverslun þinni fyrir rafræn viðskipti
- Gögn framleidd af öðrum kerfum eins og Dynamics 365 Connected Spaces

#### <a name="step-2-ingestion-and-pre-processing"></a>Skref 2: Inntaka og forvinnsla
Viðskiptagögn fara inn í Commerce HQ annað hvort beint (pantanir teknar beint í Commerce HQ viðskiptavinur) eða frá Commerce Scale Unit (pantanir teknar á POS, rafrænum viðskiptum eða sérsniðnum viðskiptavinum með Headless Commerce). 

Viðskiptagögn eru síðan afrituð yfir í Azure Data Lake sem hrá gögn með the **Flytja út í Data Lake** eiginleiki og gögnin eru geymd í möppunni „Töflur“. Gögn um vefvirkni rafræn viðskipti eru send beint í gagnavatnið.

Gögn framleidd af öðrum kerfum, svo sem Dynamics 365 Connected Spaces, er einnig sent beint í gagnavatnið.

#### <a name="step-3-transformation-and-aggregation"></a>Skref 3: Umbreyting og samsöfnun
Þegar óunnin gögn eru komin í gagnavatnið les Commerce greiningarþjónustan gögnin, umbreytir, safnar þeim saman og skrifar þau aftur í gagnavatnið í formi rökréttra eininga í möppunni „Entities“ og samansafnaðra mælikvarða í „Ontologies“ " möppu. 

#### <a name="step-4-querying"></a>Skref 4: Fyrirspurnir
Gögnum í vatninu er spurt í gegnum T-SQL viðmót með því að nota Azure Synapse Greining. Viðmótið inniheldur SQL skoðanir sem gera kleift að leita að gögnum í vatninu, annaðhvort með því að nota beint T-SQL biðlara fyrir sértæka greiningu, eða með sjónrænu tóli eins og Power BI.

#### <a name="step-5-modeling-and-serving"></a>Skref 5: Líkangerð og framreiðslu
Gögn beðin af Azure Synapse Analytics fer síðan í Power BI merkingarfræðilegt líkan. Það fer eftir tegund gagna, þau eru annað hvort flutt inn í minnið Power BI með reglulegu millibili eða beint fyrirspurn á keyrslutíma. 

Lokastigið er að gögnin eru birt innan Power BI myndefni fyrir notendur til að skoða og hafa samskipti við. 

## <a name="commerce-analytics-functional-overview"></a>Hagnýtt yfirlit viðskiptagreiningar
### <a name="1-summary"></a>1. Samantekt
#### <a name="top-level-filters"></a>Síur á hæsta stigi
1.  Dagsetningarstillingar
    1. Ár
    2. Ársfjórðungur    
    3. Mánuður    
    4. Vika    
    5. Dagur
2. Rásarstillingar
    1. Lögaðili    
    2. Gerð rásar    
    3. Gerð viðskiptavinar    
    4. Sölugerð    
    5. Rás    
    6. Stigveldi fyrirtækis
3. Vörustillingar
    1. Tegundastigveldi    
    2. Tegund

#### <a name="a-product"></a>a. Afurð
1. Sala
2. Spássía
3. Vöruskil

#### <a name="b-customer"></a>b. Viðskiptavinur
1. Sala
2. Spássía
3. Vöruskil

#### <a name="c-channel"></a>c. Rás
1. Sala
2. Spássía
3. Vöruskil

### <a name="2-sales"></a>2. Sala
1. Eftir afhendingarstað
2. Eftir rás/verslun/útstöð
3. Eftir starfsmönnum
4. Eftir dagsetningu
5. Eftir klukkustund
6. Eftir vöruflokkum

### <a name="3-margin"></a>3. Framlegð
1. Eftir afhendingarstað
2. Eftir vöru
3. Eftir dagsetningu

### <a name="4-return"></a>4. Aftur
1. Skil eftir upphæð
    1. Eftir verslun    
    2. Eftir vöru    
    3. Eftir dagsetningu
2. Skil eftir viðskiptum
    1. Eftir verslun    
    2. Eftir vöru    
    3. Eftir dagsetningu

### <a name="5-discount"></a>5. Afsláttur
1. Eftir verslun
2. Eftir vöru
3. Eftir dagsetningu
4. Sundurliðun
    1. Lögaðili    
    2. Verslun    
    3. Gerð afsláttar    
    4. Heiti afsláttar    
    5. Afurð

### <a name="6-payment"></a>6. Greiðsla
1. Eftir rás/stöð
2. Eftir greiðslumáta/tegund
3. Eftir dagsetningu
4. Sundurliðun
    1. Lögaðili    
    2. Gerð rásar    
    3. Verslun    
    4. Afgreiðslustöð    
    5. Greiðslumáti

### <a name="7-customer"></a>7. Viðskiptavinur
1. Líftímagildi (LTV): Líftímagildi er reiknað út frá heildarupphæð sem viðskiptavinur eyðir á öllum sölurásum viðskipta (POS, rafræn viðskipti og símaver).
2. Tíðni: Tíðni er reiknuð út frá fjölda daga frá síðustu viðskiptatengslum viðskiptavinar við fyrirtækið. Nýlega tekur ekki tillit til þátttökumerkja sem ekki tengjast viðskiptum eins og vafravirkni í rafrænum viðskiptum.
3. Tíðni: Tíðni er reiknuð út frá viðskiptatengslum viðskiptavinar við fyrirtækið. Tíðni tekur ekki tillit til þátttökumerkja sem ekki tengjast viðskiptum eins og vafravirkni í rafrænum viðskiptum.
4. Lengd tengsla: Lengd tengsla er reiknuð út frá fjölda daga frá því viðskiptamannaskráin var stofnuð í kerfinu. 
5. Færslutalning

### <a name="8-comparison"></a>8. Samanburður
1. Vörusamanburður eftir tímabilum
    1. Sala og sölumunur
    2. Framlegð og framlegðarmunur
2. Viðskiptavinur eftir tímabili
    1. Sala og sölumunur
    2. Framlegð og framlegðarmunur

### <a name="9-web-activity"></a>9. Vefvirkni

#### <a name="top-level-filters"></a>Síur á hæsta stigi
1. Dagsetningabil
2. Gerð rásar
3. Rás
4. Tegundastigveldi

#### <a name="a-acquisition"></a>a. Kaup
1. Síðuskoðanir
    1. Eftir landi/svæði    
    2. Eftir vöru    
    3. Eftir innskráðan notanda stöðu    
    4. Eftir dagsetningu
2. Rafræn viðskipti pantanir
3. Gengi gjaldmiðla
    1. Eftir dagsetningu
4. Viðskiptatrekt
    1. Síðuskoðun eftir tegund síðu (heimasíða, flokkasíða, vöruupplýsingasíða)  
    2. Bæta í körfu    
    3. Ljúka kaupum   
    4. Innkaup

#### <a name="b-session"></a>b. Seta
Session er skilgreind sem þáttur í heimsókn notanda á netverslunarvefsíðuna þína. Tíma er talið lokið eftir 30 mínútna aðgerðaleysi eða eftir 24 klukkustunda virka notkun.
1. Eftir landi/svæði
2. Eftir uppruna (ytri tilvísun)
3. Eftir innskráðan notanda stöðu
4. Talning þings
    1. Eftir dagsetningu    
    2. Eftir inngangssíðu
5. Panta á hverja lotu
    1. Eftir dagsetningu
6. Hopphlutfall lotu: Hopp frá lotu er skilgreint sem lota þar sem notandinn fer strax eftir að hafa heimsótt netverslunarvefsíðuna þína. 
7. Smellir á hverja lotu

#### <a name="c-visitor"></a>c. Gestur
Nafnlaus gestur á netverslunarsíðunni þinni er ákvarðaður út frá einstöku auðkenni í þeim tiltekna vafra á því tiltekna tæki. Viðskiptagreining rekur ekki nafnlausa notendur í mismunandi vöfrum eða tækjum. Nafnlaus notandi sem notar sama vafra á sömu tölvu er auðkenndur á einstakan hátt á mörgum notendalotum, þar til skyndiminni vafrans er hreinsað eða venjulega fram að 12 mánaða tímabili, hvort sem kemur á undan.

Viðskiptagreining getur veitt þér frekari upplýsingar um gesti sem vafra um netverslunarsíðuna þína á meðan þeir eru skráðir inn. Upplýsingarnar eru byggðar á núverandi sambandi þínu við þessa notendur, þar á meðal kaup sem notendur hafa gert frá fyrirtækinu þínu á öllum söluleiðum viðskipta (POS, símaver og rafræn viðskipti), og innihalda nýlega, lengd sambands, lífstímagildi og tíðni.

1. Framlegð gesta
2. Meðaltal pantanir gesta
3. Meðalsala gesta
4. Fjöldi gesta í rafrænum viðskiptum
    1. Eftir dagsetningu
    2. Eftir staðsetningu: Viðskiptagreining getur aðeins veitt nákvæmni á stigi lands/svæðis fyrir staðsetningarinnsýn fyrir gesti í rafrænum viðskiptum.     
    3. Eftir nýgengi: Nýleiki er reiknaður út frá fjölda daga frá síðustu viðskiptatengslum viðskiptavinar við fyrirtækið. Nýlega tekur ekki tillit til þátttökumerkja sem ekki tengjast viðskiptum eins og vafravirkni í rafrænum viðskiptum.    
    4. Eftir tengslalengd: Lengd tengsla er reiknuð út frá fjölda daga frá því viðskiptamannaskráin var stofnuð í kerfinu.     
    5. Eftir lífstímagildi (LTV): Líftímavirði er reiknað út frá heildarupphæð sem viðskiptavinur eyddi á öllum sölurásum viðskipta (POS, rafræn viðskipti og símaver).
    6. Eftir tíðni: Tíðni er reiknuð út frá viðskiptatengslum viðskiptavinar við fyrirtækið. Tíðni tekur ekki tillit til þátttökumerkja sem ekki tengjast viðskiptum eins og vafravirkni í rafrænum viðskiptum.

#### <a name="d-impression"></a>d. Sýning
Birting er skilgreind sem hver skoðun á myndefni af vöru sem gestur í rafrænum viðskiptum skoðar. Til dæmis, ef gestur í rafrænum viðskiptum fer á heimasíðu vefsíðunnar þinnar og skoðar jógamottuvöru innan söluhæstu listaeiningarinnar, og skoðar einnig sömu jógamottuvöruna innan vals fyrir þig listaeiningu, telja þessar samskipti sem tvær vörubirtingar. Birtingar fylgjast með vörusýnum á eftirfarandi flötum:
1. Listar (til dæmis, mælt með, söluhæstu, val fyrir þig, vinsælt)
2. Körfueining
3. Ílát leitarniðurstöðu
4. Gámur fyrir leitarniðurstöður flokka
    
Vörur sem birtar eru í hringekjueiningu eða í sérsniðnum myndefni eru ekki taldar með í birtingarmælingunni.

The **Birtingarskýrsla** síða inniheldur eftirfarandi mælikvarða:
1. Birtingarfjöldi
    1. Eftir síðugerð og einingu: Síðugerð er almenna síðugerðin sem er skilgreind fyrir hverja síðu á netverslunarvefsíðunni þinni. Tegund eininga skilgreinir tegund sjónrænnar einingar fyrir rafræn viðskipti þar sem varan er sýnd. Þú gætir þurft að kafara niður á síðuna og myndeininguna til að skoða birtingar eftir einingu.    
    2. Eftir vöru    
    3. Eftir innskráðan notanda stöðu    
    4. Eftir dagsetningu
2. Birtingarsmellafjöldi: Birtingarsmellur er skilgreindur sem gestur í rafrænum viðskiptum sem smellir á myndefni vöru, sem venjulega fer notendur á vöruupplýsingasíðuna fyrir þá vöru.     
3. Smellihlutfall birtinga (CTR): Smellihlutfall er skilgreint sem heildarfjölda birtingarsmella deilt með heildarfjölda birtinga.

## <a name="install-commerce-analytics"></a>Settu upp viðskiptagreiningu

> [!NOTE]
> Viðskiptagreining er í forskoðunarfasa í Bandaríkjunum, Kanada, Bretlandi, Evrópu, Suðaustur-Asíu, Austur-Asíu, Ástralíu og Japan. Ef umhverfið þitt er á einhverju af þessum svæðum geturðu virkjað viðskiptagreiningu í þínu umhverfi með Microsoft Dynamics Lífsferilsþjónusta (LCS). Áður en þú getur notað viðskiptagreiningu skaltu skoða [Stilla útflutning í Azure Data Lake](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).

### <a name="enable-and-configure-commerce-analytics"></a>Virkjaðu og stilltu viðskiptagreiningu
Til að setja upp Commerce Analytics þarftu heimildir til að búa til tilföng í Azure áskrift og heimildir til að setja upp viðbætur í LCS. Ljúktu við skrefin sem lýst er hér að neðan til að virkja og stilla viðskiptagreiningu.
1. [Sendu forskoðunarinntökueyðublaðið fyrir viðskiptagreiningu (Preview)](#submit-the-preview-intake-form-for-commerce-analytics).
2. [Virkjaðu og stilltu Export to Data Lake](#enable-and-configure-export-to-data-lake).
3. [Virkjaðu og stilltu Commerce Analytics (Preview) viðbótina](#enable-and-configure-commerce-analytics-add-in).
4. [Búðu til SAS tákn fyrir geymslureikning](#generate-storage-account-sas-token).
5. [Sækja uppsetningarforskriftir fyrir Azure Synapse skoðanir](#download-deployment-scripts-for-azure-synapse-views).
6. [Settu upp og stilltu Azure Synapse vinnurými](#install-and-configure-azure-synapse-workspace).
7. [Settu upp Power BI sniðmát app](#install-power-bi-template-app). 

### <a name="submit-the-preview-intake-form-for-commerce-analytics"></a>Sendu inn forskoðunarinntökueyðublaðið fyrir viðskiptagreiningu
Fylltu út og sendu inn [Inntökueyðublað fyrir viðskiptagreiningar (Preview).](https://forms.office.com/r/vW5VLJGXZ2). Vinsamlegast leyfðu allt að þremur virkum dögum þar til beiðnin er afgreidd. Þegar búið er að vinna úr eyðublaðinu verður staðfestingarpóstur sendur á netfangið sem gefið er upp í eyðublaðinu.

### <a name="enable-and-configure-export-to-data-lake"></a>Virkjaðu og stilltu Export to Data Lake
Viðskiptagreining treystir á **Flytja út í Data Lake** eiginleika til að flytja Commerce HQ gögn til Azure Data Lake og halda gögnunum ferskum. Áður en þú stillir viðskiptagreiningu skaltu virkja og stilla **Flytja út í Data Lake** með því að fylgja skrefunum sem lýst er í [Stilla útflutning í Azure Data Lake](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md). Þegar þú stillir **Flytja út í Data Lake** eiginleika, athugaðu eftirfarandi upplýsingar. Þú þarft að slá inn þessar upplýsingar í síðari skrefum.
1. DNS-nafn lyklageymslunnar og leyndarheitin þar sem þú geymir auðkenni forritsins og forritsleyndarmálið. Fyrir frekari upplýsingar, sjá [Bættu leyndarmálum við lyklahólfið](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#addsecrets).
2. Geymslureikningsheitið fyrir Azure Data Lake tilvikið. Fyrir frekari upplýsingar, sjá [Búðu til Data Lake Storage (Gen2) reikning í áskriftinni þinni](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#createsubscription).

### <a name="enable-and-configure-commerce-analytics-add-in"></a>Virkjaðu og stilltu viðskiptagreiningarviðbót
Til að setja upp Commerce analytics viðbótina í LCS verður þú að vera umhverfisstjóri í LCS fyrir umhverfið sem þú ætlar að nota.

Þú þarft eftirfarandi upplýsingar til að stilla Commerce analytics viðbótina. 

|Svæði | Upplýsingaheimild| Dæmi|
|----|----|----|
|Azure AD Leigjanda auðkenni fyrir umhverfið þitt| Þinn Azure AD leigjanda auðkenni í Azure gáttinni. Skráðu þig inn á **Azure gátt** og opnaðu **Azure Active Directory** þjónustu. Opnaðu **Eiginleikar** síðu og afritaðu gildið í **Auðkenni skráa** sviði.| 72f988bf-0000-0000-00000-2d7cd011db47|
|DNS nafn lykilhólfsins þíns|Sláðu inn [DNS nafn](#enable-and-configure-export-to-data-lake) af lyklageymslunni þinni.| `https://contosod365datafeedpoc.vault.azure.net/`|
|Leyndarmál sem inniheldur umsóknareitið| Sláðu inn [leyndarmál nafn](#enable-and-configure-export-to-data-lake) sem geymir auðkenni forritsins. Þetta er sama gildi og þú notaðir þegar þú settir upp **Flytja út í Data Lake** Bæta við.|forrit-auðkenni|
|Leyndarmál sem inniheldur umsóknarleyndarmálið| Sláðu inn [leyndarmál nafn](#enable-and-configure-export-to-data-lake) sem geymir forritið leyndarmál. Þetta er sama gildi og þú notaðir þegar þú settir upp **Flytja út í Data Lake** Bæta við.| forrit-leyndarmál|

1. Skrá inn [Lífsferilsþjónusta](https://lcs.dynamics.com/) og farðu í umhverfi þitt.
2. Á **Umhverfi** síðu, veldu **Umhverfisviðbætur** flipa.
3. Veldu **Settu upp nýja viðbót**, og veldu í glugganum **Viðskiptagreining (Forskoðun)**. Ef **Viðskiptagreining (Forskoðun)** er ekki á listanum, vertu viss um að þú hafir gengið í innherjaáætlunina.
4. Í **Setja upp viðbót** valmynd, sláðu inn nauðsynlegar upplýsingar eins og lýst er í töflunni hér að ofan.
5. Samþykkja skilmála tilboðsins með því að velja gátreitinn og velja síðan **Settu upp**.

Kerfið setur upp og stillir Commerce analytics (Preview) fyrir umhverfið. Aðgerðin gæti tekið nokkrar mínútur. Eftir að uppsetningu og stillingum er lokið, **Viðskiptagreining (Forskoðun)** er skráð á **Umhverfi** síðu og staðan er **Uppsett**.

### <a name="generate-storage-account-sas-token"></a>Búðu til SAS tákn fyrir geymslureikning
> [!NOTE]
> Þekkt takmörkun viðskiptagreiningar (Preview) er að Azure Synapse tilvik mun missa aðgang að gagnavatninu þegar SAS táknið rennur út. Þú ættir að stilla hámarks fyrningardagsetningu sem leyfilegt er af öryggisreglum fyrirtækisins þíns þegar þú býrð til Shared Access Signature (SAS) táknið.

SAS-tákn gerir ytri aðilum kleift að fá aðgang að geymslureikningnum þínum, með tilteknu setti réttinda í takmarkaðan tíma. Azure Synapse mun nota SAS táknið til að fá aðgang að undirliggjandi gögnum í Azure Data Lake. Ljúktu við skrefin hér að neðan til að búa til SAS tákn.
1. Farðu á geymslureikninginn í Azure gáttinni sem þú bjóst til við uppsetningu **Flytja út í Data Lake**, eins og lýst er í [Búðu til Data Lake Storage (Gen2) reikning í áskriftinni þinni](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#createsubscription).
2. Í **Valmöguleikar** gluggann til vinstri, undir geymslureikningnum, veldu **Sameiginlegur aðgangur undirskrift**.
3. Veldu eftirfarandi valkosti á SAS-valkostasíðunni:

    | Heiti valkosts | Valkostur gildi |
    |-------------|--------------|
    | Leyfileg þjónusta | Veldu **Blobbi**. |
    | Leyfðar tegundir tilfanga | Veldu **Þjónusta**, **·** og **Hlutur**.|
    | Leyfilegar heimildir | Veldu **Lestu**, **·**, **·**, **·**, **við**, og **Búa til**. |
    | Útgáfuheimildir Blob | Veldu **Gerir kleift að eyða útgáfum**. |
    | Upphafs- og fyrningardagsetning/tími | Stilltu lokadagsetningu og tíma fyrir SAS táknið eftir því sem við á. |
    | Leyfðar IP tölur | Skildu eftir autt. |
    | Leyfðar samskiptareglur | Veldu **Aðeins HTTPS**. |
    | Æskilegt leiðarstig | Veldu **Basic (sjálfgefið)**. |
    | Undirritunarlykill | Veldu **lykill 1** eða **lykill 2** eftir því sem við á. |

4. Veldu **Búðu til SAS og tengistreng**.
5. Afritaðu gildið úr **SAS tákn** textareit í textaritil eins og Notepad.

### <a name="download-deployment-scripts-for-azure-synapse-views"></a>Sækja uppsetningarforskriftir fyrir Azure Synapse skoðanir
Til að búa til og birta nauðsynlegar skoðanir í Azure Synapse vinnusvæði, þú verður að hlaða niður og framkvæma sett af forskriftum. Ljúktu við skrefin hér að neðan til að hlaða niður skriftunum.
1. Farðu í [Microsoft/Dynamics365Commerce.Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions) GitHub endurhverf. Handritin eru fáanleg í endurvörslunni.
2. Til að hlaða niður forskriftunum á staðbundna vélina þína geturðu annað hvort klónað endurhverfan eða hlaðið niður endurhverfunni sem zip skrá.

### <a name="install-and-configure-azure-synapse-workspace"></a>Settu upp og stilltu Azure Synapse vinnurými
Til að setja upp og stilla Azure Synapse vinnusvæði, kláraðu skrefin hér að neðan.
1. Settu upp Azure Synapse vinnusvæði í Azure áskriftinni þinni með því að fylgja skrefunum sem lýst er í [Flýtiræsing: Búðu til Synapse vinnusvæði](/azure/synapse-analytics/quickstart-create-workspace).
2. Opnaðu SetupSynapse.sql skriftuskrána í Notepad frá staðbundinni vélamöppu þar sem þú klónaðir eða hleður niður Dynamics365Commerce.Solutions endurhverfinu. Fyrir frekari upplýsingar, sjá [Sækja uppsetningarforskriftir fyrir Azure Synapse skoðanir](#download-deployment-scripts-for-azure-synapse-views). Handritaskráin verður undir "/Pipeline/CommerceAnalyticsSynapse/" möppunni. Breyttu forskriftinni til að skipta staðsetningartextanum út fyrir gildin fyrir neðan.

   | Staðsetningartexti | Gildi útskiptingar |
   |------------------|-------------------|
   | staðhaldari_geymslureikningur | Skiptu út fyrir nafnið fyrir geymslureikninginn sem þú bjóst til við uppsetningu **Flytja út í Data Lake**, eins og lýst er í [Búðu til Data Lake Storage (Gen2) reikning í áskriftinni þinni](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#createsubscription). |
   | <a name="phContainer"></a> staðhaldari_ílát | Skiptu út fyrir nafn geymsluílátsins sem var búið til í Azure Data Lake tilvikinu þínu eftir að þú settir upp **Flytja út í Data Lake** viðbót í LCS. Til að fá nafn gámans þarftu að nota Storage Explorer í Azure gáttinni til að skoða geymslureikninginn þinn. |
   | placeholder_sastoken | Skiptu út fyrir SAS táknið sem þú afritaðir í [Fáðu SAS tákn fyrir geymslureikning](#generate-storage-account-sas-token). Vertu viss um að fjarlægja **'?'** í upphafi SAS tákngildis. |
   | <a name="phUserPwd"></a> staðgengilslykilorð | Skiptu út fyrir sterkt lykilorð að eigin vali. Skráðu lykilorðið. Lykilorðið verður stillt sem lykilorð fyrir nýja 'reportreadonlyuser' reikninginn sem verður búinn til með handritinu. **EKKI GERA** sláðu inn lykilorðið fyrir 'sqladminuser' reikninginn hér.  |

3. Farðu í nýja Azure Synapse vinnusvæði í Azure portal. Veldu **Opnaðu Synapse Studio** valmöguleika á **Yfirlit** síðu.
4. Afritaðu innihald`SetupSynapse.sql` sem þú uppfærðir í skrefi 2 hér að ofan. Í Synapse Studio á Azure gáttinni, veldu **Nýtt > SQL forskrift**. Límdu innihaldið inn í SQL handritaritilinn í Synapse Studio.
5. Staðfestu það **Notaðu gagnagrunn** er stillt á **Meistari**. Veldu **Hlaupa** til að framkvæma handritið.
6. Bíddu eftir að handritinu lýkur. Handritið mun búa til gagnagrunn fyrir Commerce greiningar, skilríki fyrir aðgang að Azure Data Lake og skrifvarinn notendareikning sem verður notaður af Power BI til að tengjast Azure Synapse dæmi.
7. Opnaðu PowerShell í stjórnunarham á staðnum þinni. Farðu í "/Pipeline/CommerceAnalyticsSynapse/" möppuna undir möppunni þar sem þú klónaðir eða halaðir niður Dynamics365Commerce.Solutions endurhverfinu, eins og lýst er í [Sækja uppsetningarforskriftir fyrir Azure Synapse skoðanir](#download-deployment-scripts-for-azure-synapse-views).
8. Settu upp PowerShell keyrslustefnuna með því að keyra eftirfarandi skipun í PowerShell glugganum:

   ```powershell
   Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
   ```
   
9. Settu upp SQL Server PowerShell eininguna með því að keyra eftirfarandi skipun í PowerShell glugganum:

   ```powershell
   Install-Module sqlserver
   ```
   
   > [!NOTE]
   > Ef þú ert nú þegar með SQL Server eininguna uppsetta geturðu sleppt þessu skrefi. Við uppsetningu á þessari einingu gætir þú verið beðinn um að setja upp NuGet veitanda. Ýttu á **Y** að halda áfram með uppsetningu á NuGet veitanda. Þú gætir líka fengið skilaboð um að þú sért að setja upp einingar frá ótraustri geymslu. Ýttu á **Y** til að halda áfram með uppsetninguna. Valfrjálst geturðu keyrt`Set-PSRepository` cmdlet til að treysta`PSGallery` geymsla.
   
10. Gefðu út Azure Synapse skoða með því að keyra eftirfarandi skipun í PowerShell glugganum:

    ```powershell
    .\PublishSynapseViews.ps1 -serverName SERVER_NAME -password PASSWORD -storageAccount STORAGE_ACCOUNT -containerName CONTAINER_NAME -datarootpath DATA_ROOT_PATH
    ```
    
    Skiptu um staðgengilsgildin í skipuninni sem hér segir:
    
    | Staðgengilsgildi | Gildi útskiptingar |
    |-------------------|-------------------|
    | SERVER_NAME | Skiptu út fyrir nafnið á Azure Synapse Serverlaus SQL endapunktur. Þú getur fengið þetta gildi frá Azure Synapse vinnurými **Yfirlit** síðu í Azure portal. |
    | LYKILORÐ | Skiptu út fyrir lykilorðið fyrir sqladminuser. |
    | STORAGE_ACCOUNT | Skiptu út fyrir nafn geymslureiknings fyrir Azure Data Lake. |
    | CONTAINER_NAME | Skiptu út fyrir heiti ílátsins sem var búið til af **Flytja út í Data Lake**. Nafnið er fyrir sama ílát og þú tilgreindir í [staðhaldari_ílát](#install-and-configure-azure-synapse-workspace) gildi fyrir ofan. |
    | DATA_ROOT_PATH | Skiptu út fyrir möppuheitið undir ílátinu sem inniheldur öll gögnin. |

    > [!NOTE]
    > Þú getur fundið geymslureikningsheitið, gámaheitið og gagnarótarslóðina frá Azure gáttinni með því að nota Azure Storage vafra með Azure Data Lake geymslureikningnum þínum.

11. Bíddu eftir að handritinu lýkur. Handritið mun búa til SQL skoðanir í Azure Synapse netþjónalaust SQL dæmi.

### <a name="install-power-bi-template-app"></a>Settu upp Power BI sniðmát app
Til að setja upp Power BI sniðmátsforrit fyrir viðskiptagreiningu, kláraðu skrefin hér að neðan.
1. Skrá inn [Power BI gátt](https://powerbi.microsoft.com/) með auðkenni fyrirtækisins þíns.
2. Settu upp viðskiptagreininguna Power BI sniðmát app með því að fara á [https://aka.ms/cdireport-installapp](https://aka.ms/cdireport-installapp). Þú gætir fengið viðvörun um að appið sé ekki skráð á AppSource. Velja **Setja upp**.
3. Ef þetta er í fyrsta skipti sem þú setur upp forritið skaltu sleppa því í skref 5. Ef þú hefur þegar sett upp þetta forrit muntu sjá eftirfarandi valkosti til að uppfæra forritið.
   1. Uppfærðu vinnusvæðið og forritið: Þessi valkostur uppfærir núverandi sniðmátsforrit og skrifar yfir forritastillingar eins og nafn appstilviks og leyfisstillingar.
   2. Uppfærðu innihald vinnusvæðis án þess að uppfæra forritið: Þessi valkostur uppfærir núverandi sniðmátsforrit og varðveitir forritastillingarnar þínar. Þetta er **mælt með** valkostur fyrir app uppfærslu.
   3. Settu upp annað eintak af forritinu á nýtt vinnusvæði: Þessi valkostur býr til nýtt afrit af forritinu í nýtt vinnusvæði sem verður búið til fyrir þig. Núverandi vinnusvæði er skilið eftir ósnortið.      
4. Veldu einn af ofangreindum valkostum og veldu síðan **Settu upp**.
5. Opnaðu uppsetta appið með því að velja **Forrit** valmyndaratriði á vinstri glugganum og veldu síðan appið.
6. Tengdu forritið við gagnagjafann þinn með því að velja **Tengdu**. Ef þetta er ekki í fyrsta skipti sem appið er sett upp skaltu velja **Tengdu gögnin þín** í gulu upplýsingastikunni.
7. Sláðu inn eftirfarandi færibreytugildi:

   | Heiti færibreytu | Gildi |
   |----------------|-------|
   | Þjónn       | Sláðu inn nafnið á Azure Synapse serverlaus SQL endapunktur sem þú bjóst til í [Settu upp og stilltu Azure Synapse vinnurými](#install-and-configure-azure-synapse-workspace) kafla. Þú getur fundið þetta gildi á Azure Synapse vinnurými **Yfirlit** síðu í Azure portal. |
   | Gagnagrunnur | Sláðu inn gildið "CommerceAnalytics".
   | Tungumál | Veldu gildi af fellilistanum. Stillingin er notuð fyrir staðbundin vöru- og flokkaheiti. Gildið er hástöfum. |
   | Dagsetningarbil | Veldu gildi af fellilistanum. Gögn fyrir valinn fjölda mánaða verða flutt inn á Power BI gagnasafn. Stærð gagnasafnsins og tíminn sem þarf til að samstilla fer eftir gildinu sem þú velur. |

8. Veljið **Næst**. Þú verður beðinn um að slá inn skilríki fyrir tengingu við Azure Synapse SQL gagnagrunnur. Sláðu inn eftirfarandi gildi:

   | Heiti færibreytu | Gildi |
   |----------------|-------|
   |Sannvottunaraðferð|Veldu **Basic**.|
   |Notandanafn| Sláðu inn "reportreadonlyuser".|
   |Aðgangsorð|Sláðu inn gildið sem þú notaðir til að skipta um [staðgengilslykilorð](#install-and-configure-azure-synapse-workspace) innan SetupSynapse.sql forskriftarinnar. Þetta er lykilorðið fyrir reportreadonlyuser reikninginn.| 

9. Veldu **skráðu þig inn og tengdu**.
10. Bíddu þar til gagnasafnið hefur verið endurnýjað. Farðu síðan á vinnusvæði appsins með því að velja **Breyta app** táknmynd. Þú getur athugað endurnýjunarstöðu gagnasafnsins á vinnusvæðinu. Þú getur líka sett upp sjálfvirka endurnýjunaráætlanir fyrir gagnasafnið þitt, stjórnað heimildum og endurnefna forritatilvikið.

### <a name="privacy"></a>Persónuvernd
Persónuvernd þín er okkur mikilvæg. Til að læra meira um friðhelgi einkalífsins, lestu okkar [Persónuverndaryfirlýsing](https://go.microsoft.com/fwlink/?LinkId=521839).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
