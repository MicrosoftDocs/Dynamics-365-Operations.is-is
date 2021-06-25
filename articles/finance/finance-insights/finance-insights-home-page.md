---
title: Heimasíða Fjármálainnsýnar (forskoðun)
description: Fjármálainnsýn býður upp á stillanleg og stækkanleg líkön til að spá fyrir um sjóðstreymi fyrirtækisins á nákvæman og auðveldan hátt, spá fyrir um hvenær greiðslur berast fyrir útistandandi viðskiptakröfur og leggja drög að fjárhagsáætlun sem getur hraðað fjárhagsáætlunarferlinu. Allir þessir eiginleikar byggjast á vélnámslíkönum.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 4876d2d4ad79dc09ce4b372eedf4c6ab31930957
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222511"
---
# <a name="finance-insights-home-page-preview"></a>Heimasíða Fjármálainnsýnar (forskoðun)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Fjármálainnsýn býður upp á stillanleg og stækkanleg líkön til að spá fyrir um sjóðstreymi fyrirtækisins á nákvæman og auðveldan hátt, spá fyrir um hvenær greiðslur berast fyrir útistandandi viðskiptakröfur og leggja drög að fjárhagsáætlun sem getur hraðað fjárhagsáætlunarferlinu. Allir þessir eiginleikar byggjast á vélnámslíkönum. Þegar þessir nýju eiginleikar eru sameinaðir sjálfvirkni í greiðslum lánardrottna og innheimtu, veita þeir fjölbreytt og snjallt fjármálakerfi sem styður við ákvörðunartöku og hjálpar til við að grípa til aðgerða til að bregðast við núverandi og væntanlegum viðskiptaáskorunum á skilvirkan hátt.

Forskoðun Fjármálainnsýnar er í boði til prufuuppsetningar í Bandaríkjunum, Evrópu og Bretlandi. Microsoft bætir smátt og smátt við stuðningi fyrir fleiri svæði.

Aðeins er hægt að kveikja á forskoðunaraðgerðum í tveggja laga sandkassaumhverfi. Uppsetningar- og gervigreindarlíkön sem eru stofnuð í sandkassaumhverfi eru ekki hægt að flytja yfir í vinnsluumhverfi. Frekari upplýsingar er að finna í [Viðbótarnotkunarskilmálum fyrir Microsoft Dynamics 365 forskoðanir](/dynamics365/legal/supp-dynamics365-preview#:~:text=Supplemental%20Terms%20of%20Use%20for%20Microsoft%20Dynamics%20365,%28governing%20your%20use%20of%20Microsoft%20Dynamics%20365%20Online%29.).

## <a name="prerequisites"></a>Forkröfur

Þessi hluti fjallar um notkunarkröfur varðandi Fjármálainnsýn. Tenglar á viðbótarupplýsingar eru látnir í té þegar slíku er við komið.

### <a name="legal-requirements"></a>Lagaskilyrði

Fylltu út [samninginn um forskoðun Dynamics 365 Finance Fjármálainnsýnar](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUM1c0Uzc1RFpaU1RVTEwxVTNWUERPRThUSy4u) til að sækja um forskoðunaráætlunina.

### <a name="system-requirements"></a>Kerfiskröfur

Tveggja laga sandkassaumhverfi (margir kassar) er áskilið við forskoðun Fjármálainnsýnar. Nánari bakgrunnsupplýsingar um umhverfi, sjá [Umhverfisskipulag](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).

### <a name="version-requirements"></a>Skilyrði samkvæmt útgáfu

Þetta skjal á við útgáfu 10.0.11 af Finance and Operations-forritum (verkvangsuppfærsla 35) og nýrri útgáfur.

### <a name="historical-data-requirements"></a>Skilyrði um eldri gögn

Að minnsta kosti eitt ár af reikningum viðskiptavina er nauðsynlegt til að þjálfa vélnámslíkanið sem er notað fyrir eiginleikann greiðsluspá viðskiptavinar.

Sýnigögn eru tiltæk fyrir sýnikerfi með Contoso-sýnigagnasafnið.

### <a name="role-and-permission-requirements"></a>Skilyrði um hlutverk og heimildir

Breytingar verða gerðar á Microsoft Dynamics 365 Finance, Microsoft Dynamics Lifecycle Services (LCS), Power Apps, og Azure. Réttar heimildir eru áskildar fyrir öll þessi umhverfi. Hér eru nokkur dæmi um breytingarnar sem verða gerðar:

- Nýtt umhverfi verður búið til í Microsoft Power Platform.
- Geymslureikningur, lyklageymsla og forrit verða stofnuð í Azure.
- Handhafastjóri Active Directory verður að heimila aðgang AI Builder-forritsins að Data Lake.
- Kveikt verður á eiginleikann í Dynamics 365.

Þekking á ferlinu við að búa til og vinna með tilföng í Azure, Microsoft Dataverse og LCS er gagnleg til að ljúka við ferlið.

## <a name="configure-finance-insights"></a>Grunnstilla fjármálainnsýn

Þú verður að ljúka við tiltekin skilgreiningarskref áður en þú getur notað Fjármálainnsýn. Frekari upplýsingar um hvernig á að skilgreina Fjármálainnsýn er að finna í:
  - Fyrir útgáfur 10.0.19 og eldri: [Skilgreining fyrir Fjármálainnsýn- útgáfur 10.0.19 og eldri](configure-for-fin-insites.md).
  - Fyrir útgáfur 10.0.20 og nýrri: [Skilgreining fyrir Fjármálainnsýn (forútgáfa) - útgáfur 10.0.20 og nýrri](configure-for-fin-insites-PubPrvw.md).

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

Snjöll sjóðsstreymisspá er byggð ofan á núverandi virkni sjóðstreymisspár í Dynamics 365 Finance. Opnaðu [Sjóðstreymisspár](../cash-bank-management/cash-flow-forecasting.md) til að skoða núverandi getu.

- Til að fá upplýsingar um hvernig greiðsluspár viðskiptavinar geta veitt upplýsingarnar sem þarf til að hægt sé að framkvæma forvirkar innheimtuaðgerðir er að finna á [Nota greiðsluspár viðskiptavinar](use-customer-payment-predictions.md).
- Til að fá upplýsingar sem geta hjálpað til við að meta virkni spálíkansins eftir að þú hefur byrjað að nota eiginleikann er að finna í [Meta upprunalega greiðsluspá viðskiptavinar](evaluate-payment-prediction.md).
- Til að fá upplýsingar sem geta hjálpað þér að breyta gögnunum sem eru notuð til að gera spá og bæta þannig virkni hennar er að finna á [Bæta spálíkanið](improve-model.md).

Frekari upplýsingar um niðurstöður vélnámslíkansins er að finna í [Niðurstöður vélnámslíkana](confusion-matrix.md).

### <a name="using-cash-flow-forecasts"></a>Nota sjóðstreymisspár

Eiginleiki sjóðsstreymisspár getur aðstoðað við að gera nákvæmara mat reiðufjárstöðu. 

- Frekari upplýsingar um nýja eiginleika sjóðsstreymisspár er að finna í [Sjóðstreymisspá](cash-flow-forecast-intro.md).
- Upplýsingar um innflutning ytri gagna sem skal taka með í sjóðsstreymisspá er að finna í [Nota ytri gögn við sjóðsstreymisspár](external-data-in-cash-flow.md). 
- Upplýsingar um hvernig á að nota vélnámslíkan til að varpa sjóðsstreymi til skemmri tíma er að finna í [Reiðufjárstöðu](cash-position.md).
- Frekari upplýsingar um hvernig sjóðsstreymisstöður og sjóðsstreymisspár eru vistaðar sem skyndimyndir og bera skyndimynd saman við raunverulega stöðu er að finna í [Yfirlit yfir skyndimyndir](payment-snapshots.md).

### <a name="using-budget-proposal"></a>Notkun fjárhagsáætlunar

Frekari upplýsingar um hvernig stofnun fjárhagsáætlunar er flýtt er að finna í [Drög að fjárhagsáætlunum](budget-proposals.md). 

## <a name="feedback-and-support"></a>Ábendingar og stuðningur

Sendið tölvupóst á [Innsýn í greiðslur viðskiptavinar (forskoðun)](mailto:fiap@microsoft.com) ef áhugi er á að senda inn ábendingar eða aðstoð vantar.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
