---
title: Úrræðaleit fyrir vandamál varðandi uppsetningu fjármálainnsýnar
description: Þessi grein listar upp vandamál sem geta komið upp þegar þú notar Finance Insights möguleika. Þar er einnig útskýrt hvernig á að laga þessi vandamál.
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
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/22/2022
ms.locfileid: "9573173"
---
# <a name="troubleshoot-finance-insights-setup-issues"></a>Úrræðaleit fyrir vandamál varðandi uppsetningu fjármálainnsýnar

[!include [banner](../includes/banner.md)]

Þessi grein listar upp vandamál sem geta komið upp þegar þú notar Finance Insights möguleika. Þar er einnig útskýrt hvernig á að laga þessi vandamál.

## <a name="symptom-why-cant-i-map-the-customer-payment-insights-data-integration-template-destination-column"></a>Einkenni: Hvers vegna get ég ekki varpað viðtökudálki fyrir sniðmát gagnasamþættingar greiðsluinnsýnar viðskiptavinar?

### <a name="resolution"></a>Upplausn

Þú gætir verið að nota sniðmát fyrir eldri útgáfu. Áður en útgáfa 10.0.17 er gefin út, hafa viðskiptavinir forskoðað og stillt sniðmát gagnasamþættingar (DI) **Niðurstöður innsýnar í greiðslur viðskiptavinar (CDS til Fin og Ops)** með því að nota eininguna **Niðurstaða greiðsluspár (forskoðun)**. Eftir uppfærslu í 10.0.17 og síðar ættir þú að nota DI-sniðmátið fyrir **Niðurstöður innsýnar í greiðslur viðskiptavinar (CDS til Fin og Ops útgáfu 10.0.17 og síðar)** til að ljúka vörpuninni. Ekki er víst að þú getir varpað viðtökudálki DI-sniðmáts fyrr en einingalisti gagnastjórnunar er uppfærður og einingin **Niðurstaða greiðsluspár** birtist þar. Til að endurnýja aðilalistann og sýna niðurstöðu greiðsluspá, muntu ljúka skrefum í báðum Microsoft Dynamics 365 Fjármál og Dataverse (áður þekkt sem Common Data Service\[ Geisladiskar\] stjórnendagátt).

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

## <a name="symptom-when-i-try-to-open-ai-builder-by-using-the-links-on-the-customer-payment-predictions-setup-page-why-do-i-receive-the-following-error-message-sorry-theres-been-a-disconnect"></a>Einkenni: Þegar ég reyni að opna AI Builder með því að nota tenglana á uppsetningarsíðunni fyrir greiðsluspá viðskiptavina, hvers vegna fæ ég eftirfarandi villuboð: "Því miður, það hefur verið sambandsleysi"?

### <a name="resolution"></a>Upplausn

Dynamics 365 Finance notendur verða að hafa a Microsoft Power Apps notandareikningur fyrir umhverfið, og sá notendareikningur verður að hafa hlutverkið System customizer. The Microsoft Power Apps kerfisstjóri getur búið til notendareikninginn og úthlutað hlutverkinu. Þú getur þá farið á<https://make.preview.powerapps.com/>, skráðu þig inn með því að nota þann notandareikning og reyndu aftur tenglana.

## <a name="symptom-why-doesnt-the-cash-forecast-tab-in-the-cash-flow-forecast-workspace-show-any-data"></a>Einkenni: Hvers vegna sýnir flipi reiðufjárspár á vinnusvæði sjóðsstreymisspáar ekki nein gögn?

### <a name="resolution"></a>Upplausn

Virkni sjóðsstreymisspár í reiðufjár- og bankastjórnun og eiginleika sjóðsstreymisspáar í fjármálainnsýn verður að vera sett upp og virkjuð til að sýna gögn á réttan hátt á vinnusvæðinu **Sjóðstreymisspá**.

Fyrst skal setja upp og virkja sjóðsstreymisspá og greiðslugetulykla. Frekari upplýsingar er að finna í [Sjóðstreymisspá](../cash-bank-management/cash-flow-forecasting.md). Ef þessari uppsetningu er lokið en þú sérð ekki niðurstöðurnar sem þú býst við skaltu skoða [Úrræðaleit vegna uppsetningar sjóðstreymisspár](../cash-bank-management/cash-flow-forecasting-tsg.md) til að fá frekari upplýsingar.

Næst skal staðfesta að eiginleiki sjóðsstreymisspár í fjármálainnsýn (**Reiðufjár- og bankastjórnun \> Uppsetning \> Fjármálainnsýn \> Sjóðstreymisspár**) hafi verið virkjaður og að þjálfun gervigreindarlíkansins sé lokið. Ef þjálfuninni er ekki lokið skaltu velja **Spá núna** til að hefja þjálfunarferli líkansins.

## <a name="symptom-why-isnt-the-install-a-new-add-in-button-visible-in-microsoft-dynamics-lifecycle-services"></a>Einkenni: Af hverju er hnappurinn Setja upp nýja viðbót ekki sýnilegur í Microsoft Dynamics Lífsferilsþjónusta?

### <a name="resolution"></a>Upplausn

Fyrst skaltu ganga úr skugga um að **Umhverfisstjóri** eða **Verkeigandi** hlutverki er úthlutað innskráðum notanda í **Öryggishlutverk verkefnisins** sviði inn Microsoft Dynamics Lífsferilsþjónusta (LCS). Uppsetning á nýju viðbótunum krefst eitt af þessum öryggishlutverkum verkefnisins.

Ef þér er úthlutað réttu öryggishlutverki verkefnisins gætirðu þurft að endurnýja vafragluggann til að sjá **Settu upp nýja viðbót** takki.

## <a name="symptom-the-finance-insights-add-in-doesnt-seem-to-be-installing-why-is-that"></a>Einkenni: Finance Insights viðbótin virðist ekki vera að setja upp. Afhverju er það?

### <a name="resolution"></a>Upplausn

Eftirfarandi skref ætti að hafa verið lokið.

- Staðfestu að þú hafir **Kerfisstjóri** og **Kerfisaðlögun** aðgang í Power Portal stjórnunarmiðstöðinni.
- Staðfestu að Dynamics 365 Finance eða sambærilegt leyfi sé notað fyrir notandann sem er að setja upp viðbótina.
- Staðfestu að eftirfarandi Azure AD app er skráð í Azure AD: 

    | Forrit                  | Auðkenni forrits           |
    | ---------------------------- | ---------------- |
    | Microsoft Dynamics ERP Microservices CDS | 703e2651-d3fc-48f5-942c-74274233dba8 | 
  
    Til að staðfesta að forritið sé skráð í Azure AD, athugaðu **Allar umsóknir** lista. Fyrir frekari upplýsingar, sjá [Skoða fyrirtækjaforrit](/azure/active-directory/manage-apps/view-applications-portal).
  
    Ef umsóknin er ekki skráð í Azure AD, hafðu samband við þjónustudeild.

## <a name="symptom-error-we-didnt-find-any-data-for-the-selected-filter-range-please-select-a-different-filter-range-and-try-again"></a>Einkenni: Villa, „Við fundum engin gögn fyrir valið síusvið. Vinsamlegast veldu annað síusvið og reyndu aftur." 

### <a name="resolution"></a>Upplausn

Athugaðu gagnasamþættingaruppsetninguna til að sannreyna að hún virki eins og búist var við og bætir gögnunum frá AI Builder aftur í Fjármál.  
Fyrir frekari upplýsingar, sjá [Búðu til gagnasamþættingarverkefni](../finance-insights/create-data-integrate-project.md).

## <a name="symptom-customer-payment-prediction-training-failed-and-the-ai-builder-error-states-prediction-should-have-only-2-distinct-outcome-values-to-train-the-model-map-to-two-outcomes-and-retrain-training-report-issue-isnotminrequireddistinctnonnullvalues"></a>Einkenni: Þjálfun viðskiptavina greiðsluspá mistókst og AI Builder villa segir, "Spá ætti aðeins að hafa 2 aðgreind útkomugildi til að þjálfa líkanið. Kortið að tveimur útkomum og endurmenntuð“, „Þjálfunarskýrslumál: IsNotMinRequiredDistinctNonNullValues“.

### <a name="resolution"></a>Upplausn

Þessi villa gefur til kynna að það séu ekki nægar sögulegar færslur á síðasta ári sem tákna hvern flokk sem lýst er í **Tímanlega**, **·**, og **Mjög seint** flokkum. Til að leysa þessa villu skaltu stilla **Mjög seint** viðskiptatímabil. Ef stillt er á **Mjög seint** viðskiptatímabil lagar ekki villuna, **Greiðsluspá viðskiptavina** er ekki besta lausnin til að nota þar sem það þarf gögn í hverjum flokki í þjálfunarskyni.

Fyrir frekari upplýsingar um hvernig á að stilla **Tímanlega**, **·**, og **Mjög seint** flokka, sjá [Virkjaðu greiðsluspár viðskiptavina](../finance-insights/enable-cust-paymnt-prediction.md).

## <a name="symptom-model-training-failed"></a>Einkenni: Líkanþjálfun mistókst

### <a name="resolution"></a>Upplausn

The **Sjóðstreymisspá** líkanþjálfun krefst gagna sem innihalda 100 eða fleiri færslur sem spanna meira en ár. Við mælum með að þú hafir að minnsta kosti tveggja ára gögn með meira en 1.000 færslum.

The **Greiðsluspá viðskiptavina** eiginleiki krefst meira en 100 færslur á síðustu sex til níu mánuðum. Færslurnar geta falið í sér ókeypis textareikninga, sölupantanir og greiðslur viðskiptavina. Þessum gögnum verður að dreifa yfir **Tímanlega**, **·**, og **Mjög seint** stillingar sem eru skilgreindar á **Stillingar** síðu.    

The **Fjárlagafrumvarp** eiginleiki krefst að lágmarki þriggja ára fjárhagsáætlunar eða raunverulegra gagna. Þessi lausn notar þriggja til tíu ára gögn í áætlunum. Meira en þrjú ár munu skila betri árangri. Gögnin sjálf virka best þegar breytileiki er í gildunum. Ef gögnin innihalda öll stöðug gögn, svo sem leigukostnað, gæti þjálfunin mistekist vegna þess að skortur á breytileika krefst ekki gervigreindar til að varpa fram upphæðunum.

## <a name="symptom-error-message-states-that-the-table-with-name-msdyn_paypredpredictionresultentities-does-not-exist-the-remote-server-returned-an-error-404-not-found"></a>Einkenni: Villuskilaboð segja að „tafla með nafni, 'msdyn_paypredpredictionresultenities' er ekki til. Fjarþjónninn skilaði villu: (404) Fannst ekki…"

### <a name="resolution"></a>Upplausn

Umhverfið hefur náð hámarks töflumörkum Data Lake Services. Fyrir frekari upplýsingar um mörkin, sjáðu **Virkja næstum rauntíma gagnabreytingar** kafla greinarinnar, [Flytja út í Azure Data Lake yfirlit](../../fin-ops-core/dev-itpro/data-entities/Azure-Data-Lake-GA-version-overview.md).
