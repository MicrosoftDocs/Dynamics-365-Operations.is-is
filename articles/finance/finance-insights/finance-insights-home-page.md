---
title: Heimasíða Fjármálainnsýnar
description: Fjármálainnsýn býður upp á stillanleg og stækkanleg líkön til að spá fyrir um sjóðstreymi fyrirtækisins á nákvæman og auðveldan hátt, spá fyrir um hvenær greiðslur berast fyrir útistandandi viðskiptakröfur og leggja drög að fjárhagsáætlun sem getur hraðað fjárhagsáætlunarferlinu. Allir þessir eiginleikar byggjast á vélnámslíkönum.
author: ShivamPandey-msft
ms.date: 01/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 2f04ef1a0de815596f629fede25a247c58e026f4
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/12/2022
ms.locfileid: "9643878"
---
# <a name="finance-insights-home-page"></a>Heimasíða Fjármálainnsýnar

[!include [banner](../includes/banner.md)]

Finance Insights býður upp á stillanlegar og stækkanlegar lausnir til að spá fyrir um sjóðstreymi fyrirtækisins á nákvæman og auðveldan hátt, spá fyrir um hvenær greiðslur berast fyrir útistandandi viðskiptakröfur og leggja drög að fjárhagsáætlun sem getur hraðað fjárhagsáætlunarferlinu. Þessir snjalleiginleikar nota sniðmát vélnáms til að byggja líkön með því að nota gögn sem þú veitir (þar á meðal gögn frá þriðja aðila, svo sem upplýsingar um neytendaskýrslur frá stofnun). Þessir snjalleiginleikar upplýsa ákvarðanatöku og hjálpa þér að grípa til aðgerða til að bregðast við núverandi og væntanlegum viðskiptaáskorunum á skilvirkan hátt. Þú berð ábyrgð á öllum gögnum sem notuð eru með, eða frá fjármálainnsýn.

> [!NOTE]
> Finance Insights er í boði til uppsetningar í Bandaríkjunum, Kanada, Bretlandi, Evrópu, Asíu og Kyrrahafseyjum, Japan, Ástralíu og Nýja-Sjálandi. Microsoft bætir smátt og smátt við stuðningi fyrir fleiri svæði.

## <a name="prerequisites"></a>Forkröfur

Þessi hluti fjallar um notkunarkröfur varðandi Fjármálainnsýn. Tenglar á viðbótarupplýsingar eru látnir í té þegar slíku er við komið.

### <a name="system-requirements"></a>Kerfiskröfur

Tveggja laga umhverfi (margir kassar) er áskilið við forskoðun Fjármálainnsýnar. Nánari bakgrunnsupplýsingar um umhverfi, sjá [Umhverfisskipulag](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).

### <a name="version-requirements"></a>Skilyrði samkvæmt útgáfu

Þessi grein á við um útgáfu Microsoft Dynamics 365 Finance 10.0.21 og síðar.

### <a name="license-requirements"></a>Leyfiskröfur

Finance Insights notar AI Builder inneignir til að búa til fjárhagsspár. Öll nauðsynleg leyfi til þess fylgja með leigjendaleyfinu. Hver leigjandi Dynamics 365 Finance fær 20.000 AI Builder inneign í hverjum mánuði. Ef þörf er á viðbótarinneignum vegna viðskiptaþarfa er hægt að kaupa þær beint hjá AI Builder.

### <a name="historical-data-requirements"></a>Skilyrði um eldri gögn

Að minnsta kosti eitt ár af reikningum viðskiptavina er nauðsynlegt til að þjálfa vélnámslíkanið sem er notað fyrir eiginleikann greiðsluspá viðskiptavinar. Mælt er með þriggja ára sögulegum gögnum fyrir sjóðstreymisspár. Mælt er með þremur árum af sögulegum fjárlögum og/eða raungögnum til að hámarka gæði fyrir drög að fjárhagsáætlun.

## <a name="configure-finance-insights"></a>Grunnstilla Finance insights

Þú verður að ljúka við skilgreiningarskref áður en þú getur notað Finance Insights. Frekari upplýsingar um hvernig skilgreina skal Fjármálainnsýn er að finna í [Stillingar fyrir Fjármálainnsýn](configure-for-fin-insites.md).

## <a name="create-a-data-integrator-project"></a>Stofna verk til að setja upp samþættingu gagna

Þú verður að stofna verk til að setja upp samþættingu gagna þannig að gögnin sem vélnámslíkanið býr til geti flætt yfir í Dynamics 365 Finance. Frekari upplýsingar um skrefin til að stofna verkið er að finna í [Stofna verk til að setja upp samþættingu gagna](create-data-integrate-project.md).

## <a name="enable-finance-insights-capabilities"></a>Kveikja á eiginleikum Fjármálainnsýnar

Þegar skilgreiningarskrefunum er lokið og uppsetningu sýnigagna er lokið verður að kveikja á og setja upp alla eiginleika sem ætlunin er að nota: greiðsluspár viðskiptavinar, sjóðsstreymisspá og drög að fjárhagsáætlunum.

### <a name="enable-customer-payment-predictions"></a>Virkja greiðsluspár viðskiptavinar
Ef verið er að nota sýnigögn til að prófa greiðsluspá viðskiptavinar gæti þurft að flytja inn fleiri sýnigögn til að búa til vélnámslíkanið á fullnægjandi hátt. 

Til að virkja greiðsluspár viðskiptavinar verður þú að ljúka nokkrum skrefum til að smíða vélnámslíkan sem notar gögn fyrirtækisins til að búa til spár um það hvenær viðskiptavinir eru líklegir til að greiða útistandandi reikninga, og hvenær líklegt er að tilteknir reikningar verði greiddir. Frekari upplýsingar og sértæk skref sem verður að ljúka er að finna í [Virkja greiðsluspár viðskiptavinar](enable-cust-paymnt-prediction.md). 

### <a name="enable-cash-flow-forecasting"></a>Virkja sjóðstreymisspá
Til að virkja sjóðsstreymisspá verður að ljúka við nokkur skref til að smíða vélnámslíkan sem notar gögn fyrirtækisins til að mynda sjóðsstreymisspár. Frekari upplýsingar og sértæk skref sem verður að ljúka við er að finna í [Virkja sjóðsstreymisspá](enable-cash-flow-forecasting.md).

### <a name="enable-budget-proposals"></a>Virkja drög að fjárhagsáætlun

Eiginleikinn drög að fjárhagsáætlun notar vélnámslíkan ásamt eldri gögnum fyrirtækisins til að gera drög að fjárhagsáætlun. Drögin sem eru mynduð geta hjálpað til við að hefja fjárhagsáætlunarferli sem er áhrifaríkara og skilvirkara en handvirkt ferli. Frekari upplýsingar um sértæk skref til að virkja þennan eiginleika er að finna í [Virkja drög að fjárhagsáætlun](enable-budget-proposal.md). 

## <a name="using-finance-insights-features"></a>Notkun eiginleika Fjármálainnsýnar

### <a name="using-customer-payment-predictions"></a>Notkun greiðsluspár viðskiptavinar

- Til að fá upplýsingar um hvernig greiðsluspár viðskiptavinar geta veitt upplýsingarnar sem þarf til að hægt sé að framkvæma forvirkar innheimtuaðgerðir er að finna á [Nota greiðsluspár viðskiptavinar](use-customer-payment-predictions.md).
- Til að fá upplýsingar sem geta hjálpað til við að meta virkni spálíkansins eftir að þú hefur byrjað að nota eiginleikann er að finna í [Meta upprunalega greiðsluspá viðskiptavinar](evaluate-payment-prediction.md).
- Til að fá upplýsingar sem geta hjálpað þér að breyta gögnunum sem eru notuð til að gera spá og bæta þannig virkni hennar er að finna á [Bæta spálíkanið](improve-model.md).
- Frekari upplýsingar um niðurstöður vélnámslíkansins er að finna í [Niðurstöður vélnámslíkana](confusion-matrix.md).

### <a name="using-cash-flow-forecasts"></a>Nota sjóðstreymisspár

Eiginleiki sjóðsstreymisspár getur aðstoðað við að gera nákvæmara mat reiðufjárstöðu. Snjöll sjóðsstreymisspá er byggð ofan á núverandi virkni sjóðstreymisspár í Dynamics 365 Finance. Opnaðu [Sjóðstreymisspár](../cash-bank-management/cash-flow-forecasting.md) til að skoða núverandi getu.

- Frekari upplýsingar um nýja eiginleika sjóðsstreymisspár er að finna í [Sjóðstreymisspá](cash-flow-forecast-intro.md).
- Upplýsingar um innflutning ytri gagna sem skal taka með í sjóðsstreymisspá er að finna í [Nota ytri gögn við sjóðsstreymisspár](external-data-in-cash-flow.md). 
- Upplýsingar um hvernig á að nota vélnámslíkan til að varpa sjóðsstreymi til skemmri tíma er að finna í [Reiðufjárstöðu](cash-position.md).
- Frekari upplýsingar um hvernig sjóðsstreymisstöður og sjóðsstreymisspár eru vistaðar sem skyndimyndir og bera skyndimynd saman við raunverulega stöðu er að finna í [Yfirlit yfir skyndimyndir](payment-snapshots.md).

### <a name="using-budget-proposal"></a>Notkun fjárhagsáætlunar

Frekari upplýsingar um hvernig stofnun fjárhagsáætlunar er flýtt er að finna í [Drög að fjárhagsáætlunum](budget-proposals.md). 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
