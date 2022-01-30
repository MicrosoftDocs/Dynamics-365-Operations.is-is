---
title: Heimasíða Fjármálainnsýnar
description: Fjármálainnsýn býður upp á stillanleg og stækkanleg líkön til að spá fyrir um sjóðstreymi fyrirtækisins á nákvæman og auðveldan hátt, spá fyrir um hvenær greiðslur berast fyrir útistandandi viðskiptakröfur og leggja drög að fjárhagsáætlun sem getur hraðað fjárhagsáætlunarferlinu. Allir þessir eiginleikar byggjast á vélnámslíkönum.
author: ShivamPandey-msft
ms.date: 11/15/2021
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
ms.openlocfilehash: 8cc7b2d733cdcf1adef2885b7900ea312a10d98c
ms.sourcegitcommit: 133aa728b8a795eaeaef22544f76478da2bd1df9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/13/2022
ms.locfileid: "7968811"
---
# <a name="finance-insights-home-page"></a>Heimasíða Fjármálainnsýnar

[!include [banner](../includes/banner.md)]

Fjármálainnsýn veitir stillanlegar og stækkanlegar lausnir til að hjálpa þér að spá fyrir um sjóðstreymi fyrirtækis þíns á skynsamlegan hátt, spá fyrir um hvenær þú gætir fengið greiðslu fyrir útistandandi kröfur og búa til fjárhagsáætlunartillögu sem getur hjálpað þér að flýta fyrir fjárhagsáætlunargerð. Þessir eiginleikar nota snjöll vélnámssniðmát til að búa til líkön með því að nota gögn sem þú gefur upp (þar á meðal gögn frá þriðja aðila eins og neytendaskýrsluupplýsingar frá skrifstofu). Þessi greindur hæfileiki upplýsir ákvarðanatöku og hjálpar þér að grípa til aðgerða til að bregðast skilvirkt við núverandi og væntanlegum viðskiptaáskorunum. Þú berð ábyrgð á hvers kyns gögnum sem notuð eru með, eða framleiðsla úr, innsýn í fjármálum.

> [!NOTE]
> Fjármálainnsýn er í boði fyrir dreifingu í Bandaríkjunum, Kanada, Bretlandi, Evrópu, Kyrrahafsasíu, Japan, Ástralíu og Nýja Sjálandi. Microsoft bætir smátt og smátt við stuðningi fyrir fleiri svæði.

## <a name="prerequisites"></a>Forkröfur

Þessi hluti fjallar um notkunarkröfur varðandi Fjármálainnsýn. Tenglar á viðbótarupplýsingar eru látnir í té þegar slíku er við komið.

### <a name="legal-requirements"></a>Lagaskilyrði

Fylltu út [samninginn um forskoðun Dynamics 365 Finance Fjármálainnsýnar](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUM1c0Uzc1RFpaU1RVTEwxVTNWUERPRThUSy4u) til að sækja um forskoðunaráætlunina.

### <a name="system-requirements"></a>Kerfiskröfur

Tveggja laga umhverfi (margir kassar) er áskilið við forskoðun Fjármálainnsýnar. Nánari bakgrunnsupplýsingar um umhverfi, sjá [Umhverfisskipulag](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).

### <a name="version-requirements"></a>Skilyrði samkvæmt útgáfu

Þetta efni á við um Microsoft Dynamics 365 Finance útgáfu 10.0.21 og síðar.

### <a name="historical-data-requirements"></a>Skilyrði um eldri gögn

Að minnsta kosti eitt ár af reikningum viðskiptavina er nauðsynlegt til að þjálfa vélnámslíkanið sem er notað fyrir eiginleikann greiðsluspá viðskiptavinar. Mælt er með þriggja ára sögulegum gögnum fyrir sjóðstreymisspár. Mælt er með þriggja ára sögulegri fjárhagsáætlun og/eða raungildi fyrir greindar fjárlagatillögur.

## <a name="configure-finance-insights"></a>Grunnstilla Finance insights

Þú verður að ljúka stillingarskrefum áður en þú getur notað Finance Insights. Frekari upplýsingar um hvernig skilgreina skal Fjármálainnsýn er að finna í [Stillingar fyrir Fjármálainnsýn](configure-for-fin-insites.md).

## <a name="create-a-data-integrator-project"></a>Stofna verk til að setja upp samþættingu gagna

Þú verður að stofna verk til að setja upp samþættingu gagna þannig að gögnin sem vélnámslíkanið býr til geti flætt yfir í Dynamics 365 Finance. Frekari upplýsingar um skrefin til að stofna verkið er að finna í [Stofna verk til að setja upp samþættingu gagna](create-data-integrate-project.md).

## <a name="enable-finance-insights-capabilities"></a>Kveikja á eiginleikum Fjármálainnsýnar

Þegar skilgreiningarskrefunum er lokið og uppsetningu sýnigagna er lokið verður að kveikja á og setja upp alla eiginleika sem ætlunin er að nota: greiðsluspár viðskiptavinar, sjóðsstreymisspá og drög að fjárhagsáætlunum.

### <a name="enable-customer-payment-predictions"></a>Virkja greiðsluspár viðskiptavinar
Ef verið er að nota sýnigögn til að prófa greiðsluspá viðskiptavinar gæti þurft að flytja inn fleiri sýnigögn til að búa til vélnámslíkanið á fullnægjandi hátt. 

Til að virkja greiðsluspá viðskiptavina, verður þú að ljúka nokkrum skrefum til að byggja upp vélrænt líkan sem notar gögn fyrirtækisins til að búa til spár um hvenær viðskiptavinir eru líklegir til að greiða útistandandi reikninga og hvenær líklegt er að tilteknir reikningar verði greiddir. Frekari upplýsingar og sértæk skref sem verður að ljúka er að finna í [Virkja greiðsluspár viðskiptavinar](enable-cust-paymnt-prediction.md). 

### <a name="enable-cash-flow-forecasting"></a>Virkja sjóðstreymisspá
Til að virkja sjóðsstreymisspá verður að ljúka við nokkur skref til að smíða vélnámslíkan sem notar gögn fyrirtækisins til að mynda sjóðsstreymisspár. Frekari upplýsingar og sértæk skref sem verður að ljúka við er að finna í [Virkja sjóðsstreymisspá](enable-cash-flow-forecasting.md).

### <a name="enable-budget-proposals"></a>Virkja drög að fjárhagsáætlun

Eiginleikinn drög að fjárhagsáætlun notar vélnámslíkan ásamt eldri gögnum fyrirtækisins til að gera drög að fjárhagsáætlun. Drögin sem eru mynduð geta hjálpað til við að hefja fjárhagsáætlunarferli sem er áhrifaríkara og skilvirkara en handvirkt ferli. Fyrir sérstök skref til að virkja þennan eiginleika, sjá [Virkja fjárlagatillögur](enable-budget-proposal.md). 

## <a name="using-finance-insights-features"></a>Notkun eiginleika Fjármálainnsýnar

### <a name="using-customer-payment-predictions"></a>Notkun greiðsluspár viðskiptavinar

- Til að læra hvernig greiðsluspár viðskiptavina geta veitt þær upplýsingar sem eru nauðsynlegar til að hefja innheimtuaðgerðir með fyrirbyggjandi hætti, sjá [Notaðu greiðsluspá viðskiptavina](use-customer-payment-predictions.md).
- Til að fá upplýsingar sem geta hjálpað til við að meta virkni spálíkansins eftir að þú hefur byrjað að nota eiginleikann er að finna í [Meta upprunalega greiðsluspá viðskiptavinar](evaluate-payment-prediction.md).
- Til að fá upplýsingar sem geta hjálpað þér að breyta gögnunum sem eru notuð til að gera spá og bæta þannig virkni hennar er að finna á [Bæta spálíkanið](improve-model.md).
- Frekari upplýsingar um niðurstöður vélnámslíkansins er að finna í [Niðurstöður vélnámslíkana](confusion-matrix.md).

### <a name="using-cash-flow-forecasts"></a>Nota sjóðstreymisspár

Eiginleiki sjóðsstreymisspár getur aðstoðað við að gera nákvæmara mat reiðufjárstöðu. Snjöll sjóðstreymisspáin er byggð ofan á núverandi virkni sjóðstreymisspár í Dynamics 365 Finance. Opnaðu [Sjóðstreymisspár](../cash-bank-management/cash-flow-forecasting.md) til að skoða núverandi getu.

- Til að fræðast um nýja möguleika í sjóðstreymisspám, sjá [Sjóðstreymisspá](cash-flow-forecast-intro.md).
- Upplýsingar um innflutning ytri gagna sem skal taka með í sjóðsstreymisspá er að finna í [Nota ytri gögn við sjóðsstreymisspár](external-data-in-cash-flow.md). 
- Upplýsingar um hvernig á að nota vélnámslíkan til að varpa sjóðsstreymi til skemmri tíma er að finna í [Reiðufjárstöðu](cash-position.md).
- Frekari upplýsingar um hvernig sjóðsstreymisstöður og sjóðsstreymisspár eru vistaðar sem skyndimyndir og bera skyndimynd saman við raunverulega stöðu er að finna í [Yfirlit yfir skyndimyndir](payment-snapshots.md).

### <a name="using-budget-proposal"></a>Notkun fjárhagsáætlunar

Frekari upplýsingar um hvernig stofnun fjárhagsáætlunar er flýtt er að finna í [Drög að fjárhagsáætlunum](budget-proposals.md). 

## <a name="feedback-and-support"></a>Ábendingar og stuðningur

Ef þú hefur áhuga á að veita endurgjöf, eða ef þú þarft aðstoð, sendu tölvupóst á [Innsýn í fjármálum](mailto:fiap@microsoft.com).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
