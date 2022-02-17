---
title: Úrræðaleit fyrir vandamál varðandi uppsetningu fjármálainnsýnar
description: Í þessu efnisatriði eru talin upp vandamál sem geta komið upp þegar möguleikar fjármálainnsýnar eru notaðir. Þar er einnig útskýrt hvernig á að laga þessi vandamál.
author: panolte
ms.date: 01/29/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-08-20
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: f77cddfdab22bef8af7f62d49723e330c4f13261
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/31/2022
ms.locfileid: "8064867"
---
# <a name="troubleshoot-finance-insights-setup-issues"></a>Úrræðaleit fyrir vandamál varðandi uppsetningu fjármálainnsýnar

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði eru talin upp vandamál sem geta komið upp þegar möguleikar fjármálainnsýnar eru notaðir. Þar er einnig útskýrt hvernig á að laga þessi vandamál.

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

## <a name="symptom-when-i-try-to-open-ai-builder-by-using-the-links-on-the-customer-payment-predictions-setup-page-why-do-i-receive-the-following-error-message-sorry-theres-been-a-disconnect"></a>Einkenni: Þegar ég reyni að opna AI Builder af hverju fæ ég eftirfarandi villuboð með því að nota tenglana á uppsetningarsíðunni fyrir greiðsluspá viðskiptavinar: „Því miður, það hefur verið sambandsleysi“?

### <a name="resolution"></a>Upplausn

Dynamics 365 Finance notendur verða að hafa a Microsoft Power Apps notendareikningur fyrir umhverfið, og sá notendareikningur verður að hafa hlutverk sérsníðakerfis. The Microsoft Power Apps kerfisstjóri getur búið til notendareikninginn og úthlutað hlutverkinu. Þú getur þá farið á<https://make.preview.powerapps.com/>, skráðu þig inn með því að nota þann notandareikning og reyndu aftur tenglana.

## <a name="symptom-why-doesnt-the-cash-forecast-tab-in-the-cash-flow-forecast-workspace-show-any-data"></a>Einkenni: Hvers vegna sýnir flipi reiðufjárspár á vinnusvæði sjóðsstreymisspáar ekki nein gögn?

### <a name="resolution"></a>Upplausn

Virkni sjóðsstreymisspár í reiðufjár- og bankastjórnun og eiginleika sjóðsstreymisspáar í fjármálainnsýn verður að vera sett upp og virkjuð til að sýna gögn á réttan hátt á vinnusvæðinu **Sjóðstreymisspá**.

Fyrst skal setja upp og virkja sjóðsstreymisspá og greiðslugetulykla. Frekari upplýsingar er að finna í [Sjóðstreymisspá](../cash-bank-management/cash-flow-forecasting.md). Ef þessari uppsetningu er lokið en þú sérð ekki niðurstöðurnar sem þú býst við skaltu skoða [Úrræðaleit vegna uppsetningar sjóðstreymisspár](../cash-bank-management/cash-flow-forecasting-tsg.md) til að fá frekari upplýsingar.

Næst skal staðfesta að eiginleiki sjóðsstreymisspár í fjármálainnsýn (**Reiðufjár- og bankastjórnun \> Uppsetning \> Fjármálainnsýn \> Sjóðstreymisspár**) hafi verið virkjaður og að þjálfun gervigreindarlíkansins sé lokið. Ef þjálfuninni er ekki lokið skaltu velja **Spá núna** til að hefja þjálfunarferli líkansins.

## <a name="symptom-why-isnt-the-install-a-new-add-in-button-visible-in-microsoft-dynamics-lifecycle-services"></a>Einkenni: Af hverju er hnappurinn Setja upp nýja viðbót ekki sýnilegur í Microsoft Dynamics Lífsferilsþjónusta?

### <a name="resolution"></a>Upplausn

Fyrst skaltu ganga úr skugga um að **Umhverfisstjóri** eða **Verkeigandi** hlutverki er úthlutað innskráðum notanda í **Öryggishlutverk verkefnisins** sviði inn Microsoft Dynamics Lífsferilsþjónusta (LCS). Uppsetning á nýju viðbótunum krefst eitt af þessum öryggishlutverkum verkefnisins.

Ef réttu öryggishlutverki verkefnisins er úthlutað þér gætirðu þurft að endurnýja vafragluggann til að sjá **Settu upp nýja viðbót** takki.

## <a name="symptom-the-finance-insights-add-in-doesnt-seem-to-be-installing-why-is-that"></a>Einkenni: Finance Insights viðbótin virðist ekki vera að setja upp. Afhverju er það?

### <a name="resolution"></a>Upplausn

Eftirfarandi skref ætti að hafa verið lokið.

- Staðfestu að þú hafir **Kerfisstjóri** og **Kerfisaðlögun** aðgangur í Power Portal stjórnunarmiðstöðinni.
- Staðfestu að a Dynamics 365 Finance eða sambærilegt leyfi er beitt fyrir notandann sem er að setja upp viðbótina.
- Staðfestu að eftirfarandi Azure AD app er skráð í Azure AD: 

  | Forrit                  | Auðkenni forrits           |
  | ---------------------------- | ---------------- |
  | Microsoft Dynamics ERP Microservices CDS | 703e2651-d3fc-48f5-942c-74274233dba8 | 
  
## <a name="symptom-error-we-didnt-find-any-data-for-the-selected-filter-range-please-select-a-different-filter-range-and-try-again"></a>Einkenni: Villa, „Við fundum engin gögn fyrir valið síusvið. Vinsamlegast veldu annað síusvið og reyndu aftur." 

### <a name="resolution"></a>Upplausn

Athugaðu uppsetningu gagnasamþættingar til að sannreyna að hún virki eins og búist var við og bætir gögnum frá AI Builder aftur í Fjármál.  
Fyrir frekari upplýsingar, sjá [Búðu til gagnasamþættingarverkefni](../finance-insights/create-data-integrate-project.md).

## <a name="symptom-customer-payment-prediction-training-failed-and-the-ai-builder-error-states-prediction-should-have-only-2-distinct-outcome-values-to-train-the-model-map-to-two-outcomes-and-retrain-training-report-issue-isnotminrequireddistinctnonnullvalues"></a>Einkenni: Þjálfun viðskiptavina greiðsluspá mistókst og AI Builder villa segir, "Spá ætti að hafa aðeins 2 aðgreind útkomugildi til að þjálfa líkanið. Kortið að tveimur útkomum og endurmenntuð“, „Málfræði um þjálfunarskýrslu: IsNotMinRequiredDistinctNonNullValues“.

### <a name="resolution"></a>Upplausn

Þessi villa gefur til kynna að það séu ekki nægar sögulegar færslur á síðasta ári sem tákna hvern flokk sem lýst er í **Tímanlega**, **·**, og **Mjög seint** flokkum. Til að leysa þessa villu skaltu stilla **Mjög seint** viðskiptatímabil. Ef stillt er á **Mjög seint** viðskiptatímabil lagar ekki villuna, **Greiðsluspá viðskiptavina** er ekki besta lausnin til að nota þar sem það þarf gögn í hverjum flokki fyrir þjálfunartilgang.

Fyrir frekari upplýsingar um hvernig á að stilla **Tímanlega**, **·**, og **Mjög seint** flokka, sjá [Virkjaðu greiðsluspár viðskiptavina](../finance-insights/enable-cust-paymnt-prediction.md).

## <a name="symptom-model-training-failed"></a>Einkenni: Líkanþjálfun mistókst

### <a name="resolution"></a>Upplausn

The **Sjóðstreymisspá** líkanþjálfun krefst gagna sem spanna meira en eitt ár og innihalda meira en 100 færslur. Þessar færslur verða að hafa áhrif á lausafjárreikninga sem eru innifalin í uppsetningu sjóðstreymisspár.

The **Greiðsluspá viðskiptavina** þarf að minnsta kosti 100 reikninga og greiðslufærslur viðskiptavina á síðustu sex til níu mánuðum til að búa til spár.  
