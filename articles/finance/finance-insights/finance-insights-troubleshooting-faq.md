---
title: Úrræðaleit fyrir vandamál varðandi uppsetningu fjármálainnsýnar
description: Í þessari grein eru talin upp vandamál sem geta komið upp þegar möguleikar Finance Insights eru notaðir. Þar er einnig útskýrt hvernig á að laga þessi vandamál.
author: panolte
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2021-08-20
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: 331c714663d212471b72f1558e6183452ef7f394
ms.sourcegitcommit: adadbc6e355e2ad68a1f6af26a1be1f89dc8eec6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/22/2022
ms.locfileid: "9573173"
---
# <a name="troubleshoot-finance-insights-setup-issues"></a>Úrræðaleit fyrir vandamál varðandi uppsetningu fjármálainnsýnar

[!include [banner](../includes/banner.md)]

Í þessari grein eru talin upp vandamál sem geta komið upp þegar möguleikar Finance Insights eru notaðir. Þar er einnig útskýrt hvernig á að laga þessi vandamál.

## <a name="symptom-why-cant-i-map-the-customer-payment-insights-data-integration-template-destination-column"></a>Einkenni: Hvers vegna get ég ekki varpað viðtökudálki fyrir sniðmát gagnasamþættingar greiðsluinnsýnar viðskiptavinar?

### <a name="resolution"></a>Upplausn

Þú gætir verið að nota sniðmát fyrir eldri útgáfu. Áður en útgáfa 10.0.17 er gefin út, hafa viðskiptavinir forskoðað og stillt sniðmát gagnasamþættingar (DI) **Niðurstöður innsýnar í greiðslur viðskiptavinar (CDS til Fin og Ops)** með því að nota eininguna **Niðurstaða greiðsluspár (forskoðun)**. Eftir uppfærslu í 10.0.17 og síðar ættir þú að nota DI-sniðmátið fyrir **Niðurstöður innsýnar í greiðslur viðskiptavinar (CDS til Fin og Ops útgáfu 10.0.17 og síðar)** til að ljúka vörpuninni. Ekki er víst að þú getir varpað viðtökudálki DI-sniðmáts fyrr en einingalisti gagnastjórnunar er uppfærður og einingin **Niðurstaða greiðsluspár** birtist þar. Til að uppfæra einingalistann og sýna niðurstöðu greiðsluspár lýkurðu við skref í bæði Microsoft Dynamics 365 Finance og Dataverse (áður þekkt sem Common Data Service \[CDS\] stjórnendagátt).

### <a name="in-finance"></a>Í Finance

Fylgdu þessum skrefum í Finance eftir uppfærslu.

1. Opnaðu **Kerfisstjórnun \> Vinnusvæði \> Gagnastjórnun**.
2. Á vinnusvæðinu **Gagnastjórnun** skal velja reitinn **Færibreytur ramma**.
3. Á síðunni **Færibreytur ramma fyrir inn- og útflutning gagna** skal velja **Einingastillingar** og síðan velja **Uppfæra einingalista**.
4. Lokaðu síðunni **Færibreytur ramma fyrir inn- og útflutning gagna**.
5. Á vinnusvæðinu **Gagnastjórnun** skal velja reitinn **Gagnaeiningar**.
6. Leitaðu að „Niðurstaða greiðsluspár“. Staðfestu að einingin **Niðurstaða greiðsluspár** sé ekki forútgáfan. Heiti forútgáfunnar endar á „(forskoðun)“. Ef þú sérð aðeins forútgáfu einingarinnar skaltu hafa samband við notendaþjónustu Microsoft.

### <a name="in-dataverse"></a>Í Dataverse

Fylgdu eftirfarandi skrefum í [Power Platform stjórnendamiðstöð](https://admin.powerplatform.microsoft.com/environments) til að uppfæra gagnasamþættingarverkin þín.

1. Ef þú ert að nota forútgáfu fjármálainnsýnar skaltu fjarlægja DI-verkið sem er tengt við sniðmátið **Niðurstöður innsýnar í greiðslur viðskiptavinar (CDS til Fin og Ops)**.
2. Fylgdu skrefunum í [Stofna gagnasamþættingarverk](create-data-integrate-project.md). Notaðu sniðmátið **Niðurstöður innsýnar í greiðslur viðskiptavinar (CDS til Fin og Ops 10.0.17 og síðar)**.

## <a name="symptom-when-i-try-to-open-ai-builder-by-using-the-links-on-the-customer-payment-predictions-setup-page-why-do-i-receive-the-following-error-message-sorry-theres-been-a-disconnect"></a>Einkenni: Þegar ég reyni að opna AI Builder með því að nota tenglana á uppsetningarsíðu fyrir greiðsluspá viðskiptavinar, hvers vegna fæ ég eftirfarandi villuboð: „Því miður rofnaði tengingin“?

### <a name="resolution"></a>Upplausn

Notendur Dynamics 365 Finance verða að vera með Microsoft Power Apps notandareikning fyrir umhverfið og sá notandareikningur verður að vera með hlutverk kerfisstillis. Kerfisstjóri Microsoft Power Apps getur búið til notandareikninginn og úthlutað hlutverkinu. Svo geturðu farið í <https://make.preview.powerapps.com/>, skráð þig inn með því að nota notandareikninginn og prófað tenglana aftur.

## <a name="symptom-why-doesnt-the-cash-forecast-tab-in-the-cash-flow-forecast-workspace-show-any-data"></a>Einkenni: Hvers vegna sýnir flipi reiðufjárspár á vinnusvæði sjóðsstreymisspáar ekki nein gögn?

### <a name="resolution"></a>Upplausn

Virkni sjóðsstreymisspár í reiðufjár- og bankastjórnun og eiginleika sjóðsstreymisspáar í fjármálainnsýn verður að vera sett upp og virkjuð til að sýna gögn á réttan hátt á vinnusvæðinu **Sjóðstreymisspá**.

Fyrst skal setja upp og virkja sjóðsstreymisspá og greiðslugetulykla. Frekari upplýsingar er að finna í [Sjóðstreymisspá](../cash-bank-management/cash-flow-forecasting.md). Ef þessari uppsetningu er lokið en þú sérð ekki niðurstöðurnar sem þú býst við skaltu skoða [Úrræðaleit vegna uppsetningar sjóðstreymisspár](../cash-bank-management/cash-flow-forecasting-tsg.md) til að fá frekari upplýsingar.

Næst skal staðfesta að eiginleiki sjóðsstreymisspár í fjármálainnsýn (**Reiðufjár- og bankastjórnun \> Uppsetning \> Fjármálainnsýn \> Sjóðstreymisspár**) hafi verið virkjaður og að þjálfun gervigreindarlíkansins sé lokið. Ef þjálfuninni er ekki lokið skaltu velja **Spá núna** til að hefja þjálfunarferli líkansins.

## <a name="symptom-why-isnt-the-install-a-new-add-in-button-visible-in-microsoft-dynamics-lifecycle-services"></a>Einkenni: Hvers vegna er hnappurinn „Setja upp nýja innbót“ ekki sýnilegur í Microsoft Dynamics Lifecycle Services?

### <a name="resolution"></a>Upplausn

Fyrst skal ganga úr skugga um að hlutverkið **Stjórnandi umhverfis** eða **Eigandi verks** sé úthlutað á innskráðan notanda í reitnum **Öryggishlutverk verks** í Microsoft Dynamics Lifecycle Services (LCS). Uppsetning á nýjum innbótum krefst eins af þessum öryggishlutverkum verks.

Ef þér er úthlutað réttu öryggishlutverki verks gætirðu þurft að endurhlaða vafragluggann til að sjá hnappinn **Setja upp nýja innbót**.

## <a name="symptom-the-finance-insights-add-in-doesnt-seem-to-be-installing-why-is-that"></a>Einkenni: Uppsetning á innbót Finance Insights virðist ekki fara í gang. Hvers vegna?

### <a name="resolution"></a>Upplausn

Eftirfarandi skrefum ætti að vera lokið.

- Gakktu úr skugga um að þú hafir aðgang **Kerfisstjóra** og **Kerfisstillis** í stjórnendamiðstöð Power Portal.
- Staðfestu að Dynamics 365 Finance eða sambærilegt leyfi sé notað fyrir notandann sem er að setja upp innbótina.
- Staðfestið að eftirfarandi Azure AD forrit sé skráð í Azure AD: 

    | Forrit                  | Auðkenni forrits           |
    | ---------------------------- | ---------------- |
    | Microsoft Dynamics ERP Microservices CDS | 703e2651-d3fc-48f5-942c-74274233dba8 | 
  
    Til að ganga úr skugga um að forritið sé skráð í Azure AD skal athuga listann **Öll forrit**. Frekari upplýsingar er að finna í [Skoða forrit fyrirtækis](/azure/active-directory/manage-apps/view-applications-portal).
  
    Ef forritið er ekki skráð í Azure AD skal hafa samband við notendaþjónustu.

## <a name="symptom-error-we-didnt-find-any-data-for-the-selected-filter-range-please-select-a-different-filter-range-and-try-again"></a>Einkenni: Villa: „Engin gögn fundust fyrir valið síusvið. Veldu annað síusvið og reyndu aftur.“ 

### <a name="resolution"></a>Upplausn

Athugaðu uppsetningu gagnasamþættingar til að ganga úr skugga um að hún virki sem skyldi og settu upp gögnin úr AI Builder aftur í Finance.  
Frekari upplýsingar er að finna í [Stofna verk gagnasamþættingar](../finance-insights/create-data-integrate-project.md).

## <a name="symptom-customer-payment-prediction-training-failed-and-the-ai-builder-error-states-prediction-should-have-only-2-distinct-outcome-values-to-train-the-model-map-to-two-outcomes-and-retrain-training-report-issue-isnotminrequireddistinctnonnullvalues"></a>Einkenni: Þjálfun fyrir greiðsluspá viðskiptavinar mistókst og AI Builder villan segir: „Spá á aðeins að vera með tvö aðgreind gildi útkomu til að þjálfa líkanið. Varpaðu í tvær útkomur og gerðu þjálfun aftur“, „Vandamál með þjálfunarskýrslu: IsNotMinRequiredDistinctNonNullValues“.

### <a name="resolution"></a>Upplausn

Þessi villa gefur til kynna að það eru ekki nógu margar sögulegar færslur á síðasta ári sem sýna hvern flokk sem lýst er í flokkunum **Á réttum tíma**, **Seint** og **Mjög seint**. Til að leysa þessa villu skal breyta færslutímabilinu **Mjög seint**. Ef breyting á færslutímabilinu **Mjög seint** lagar ekki villuna eru **Greiðsluspár viðskiptavinar** ekki besta lausnin til að nota því hún þarf gögn í hverjum flokki í þjálfunarskyni.

Frekari upplýsingar um hvernig á að breyta flokkunum **Á réttum tíma**, **Seint** og **Mjög seint** er að finna í [Virkja greiðsluspár viðskiptavinar](../finance-insights/enable-cust-paymnt-prediction.md).

## <a name="symptom-model-training-failed"></a>Einkenni: Líkanaþjálfun mistókst

### <a name="resolution"></a>Upplausn

Líkanaþjálfunin **Sjóðstreymisspá** þarf gögn sem innihalda 100 eða fleiri færslur sem ná yfir meira en eitt ár. Við mælum með að notuð séu að minnsta kosti tvö ár af gögnum með meira en 1.000 færslur.

Meira en 100 færslur undanfarna sex til níu mánuði eru gerðar vegna **Greiðsluspár viðskiptavinar**. Færslunar geta falið í sér textareikninga, sölupantanir og greiðslur til viðskiptavina. Þessi gögn verða að vera dreifð á stillingarnar **Á réttum tíma**, **Seint** og **Mjög seint** sem skilgreindar eru á síðunni **Skilgreining**.    

**Drög að fjárhagsáætlun** krefst að lágmarki þriggja ára fjárhagsáætlunar eða raunverulegra gagna. Þessi lausn notar þriggja til tíu ára gögn í spánum. Meira en þrjú ár veita betri niðurstöður. Gögnin sjálf virka best þegar breytileiki er í gildunum. Ef gögnin innihalda aðeins föst gögn, svo sem leigukostnað, getur verið að þjálfunin mistakist þar sem skortur á breytileika krefst þess ekki að gervigreind birti upphæðirnar.

## <a name="symptom-error-message-states-that-the-table-with-name-msdyn_paypredpredictionresultentities-does-not-exist-the-remote-server-returned-an-error-404-not-found"></a>Einkenni: Villuboð segja að „Tafla með heitinu „msdyn_paypredpredictionresultentities“ sé ekki til. Fjartengdur þjónn skilaði villu: (404) Finnst ekki...“

### <a name="resolution"></a>Upplausn

Umhverfið hefur náð hámarki fyrir töflu gagnalindarþjónustu. Frekari upplýsingar um mörkin er að finna í hlutanum **Virkja breytingar á næstum rauntímagögnum** í greininni [Yfirlit yfir „Flytja út í Azure Data Lake“](../../fin-ops-core/dev-itpro/data-entities/Azure-Data-Lake-GA-version-overview.md).
