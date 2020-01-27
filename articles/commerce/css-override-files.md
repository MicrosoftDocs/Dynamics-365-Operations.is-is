---
title: Vinna með CSS-hnekkingarskrár
description: Þetta efni lýsir hvers vegna, hvenær og hvernig á að nota Cascading Style Sheets (CSS) hnekkingarskrár í Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-12-12
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b5a50fc0c9060117cdddc0875446afc2edc12a11
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915440"
---
# <a name="work-with-css-override-files"></a>Vinna með CSS-hnekkingarskrár

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Þetta efni lýsir hvers vegna, hvenær og hvernig á að nota Cascading Style Sheets (CSS) hnekkingarskrár í Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Varanlegir svæðisstílar ættu venjulega að vera meðhöndlaðir með þema svæðisins. Þemu veita grunninn að CSS og stílstillingar fyrir einingarnar á hvaða síðu sem er á svæðinu. Þemu eru búin til með því að nota Dynamics 365 Commerce hugbúnaðarþróunarbúnað (SDK) á netinu og þau eru send á vefsíður þínar í gegnum Microsoft Dynamics Lifecycle Services (LCS). Kembigeta fyrir þemu og stillingar á einingaviðmótum í SDK hjálpa vefhönnuðum við að skapa sérsníðanlega og samloðandi vefhönnunarpakka. Þegar þessir hönnunarpakkar eru settir á vefsvæði geta höfundar vefsvæðisins lagt áherslu á að búa til, breyta og birta efni í stað þess að þróa vefinn.

Í ljósi venjulegs líftíma þema getur hæði við hönnuði að gera stílbreytingar í gegnum uppsetningarleiðslu SDK og LCS verið hindrandi í sumum tilfellum. Frumgerð vefsvæða eða bráðabóta geta virst fyrirferðarmikil ef SDK er ekki stillt eða ef þú hefur ekki tíma til að bíða eftir LCS-dreifingu.

Í þessum atburðarásum geta CSS hnekkingarskrár hjálpað. Í höfundatækjum Commerce geta staðfestir notendur flutt upp CSS-skrá, forskoðað hana og virkjað síðan til að hnekkja þema vefsvæðisins. Ekki er krafist kostnaðar við uppsetningu á SDK eða LCS. Hnekkingar sem eru tilgreindar í CSS-hnekkingarskrá geta verið eins litlar og breyting á einum textastíl eða eins umfangsmiklar og algjör yfirhalning vörumerkis.

Áður en þú notar CSS-hnekkingarskrár skaltu hafa eftirfarandi takmarkanir í huga:

- Aðeins ein CSS-hnekkingarskrá í einu getur verið virk á vefsíðu. Þess vegna verða allar virkar hnekkingar að vera til staðar í einni hnekkingarskrá.
- Þrátt fyrir að þú getir forskoðað hnekkingar í höfundatækjum Commerce eru engir sérstakir kembieiginleikar til að hjálpa til við að bera kennsl á villur sem hnekkingarnar koma á. Með öðrum orðum, þegar þú notar CSS-hnekkingarskrár ertu ekki með sama verkfæri og SDK veitir fyrir staðfestingu eininga og höfundar.

Samt sem áður veita CSS-hnekkingarskrár skjóta leið til að frumgera hönnun eða útfæra bráðabót áður en full þemuuppfærsla er þróuð og dreift.

## <a name="create-a-css-override-file"></a>Stofna CSS-hnekkingarskrá

Til að búa til CSS-hnekkingarskrá er hægt að nota hvaða Integrated Development Environment (IDE), textaritil eða frumkóðaritil sem er. Dæmigerð nálgun er að nota stöðluð kembiforrit í vafranum til að bera kennsl á stílveljara, eiginleika og gildi á núverandi svæði. Flestir vafrar gera þér klefta að breyta gildum og forskoða þau í kembiforritinu. Eftir að þú hefur bent á breytingarnar sem þú vilt gera geturðu vistað þær í þína eigin CSS-skrá.

## <a name="upload-a-css-override-file"></a>Hlaða upp CSS-hnekkingarskrá

Til að hlaða upp CSS-skrá á síðuna þína í Commerce skaltu fylgja þessum skrefum.

1. Farðu á vefsvæðið í höfundatólunum.
1. Í stýriglugganum vinstra megin velurðu **Hanna**.

    > [!NOTE]
    > Það fer eftir útgáfu af höfundatækjum Commerce sem þú notar en þú gætir þurft að stækka **Stillingar** í leiðsöguglugganum áður en þú getur valið **Hönnun**.

1. Efst í aðalhönnunarglugganum velurðu flipann **CSS-hnekking**, ef hann hefur ekki þegar verið valinn.
1. Undir **Tiltækar CSS-hnekkingar** velurðu **Hlaða upp CSS-skrá**. Gluggi í File Explorer birtist.
1. Í File Explorer flettirðu að og velur CSS-skrá og velur síðan **Opið**. Uppflutt CSS-skrá birtist nú undir **Tiltækar CSS-hnekkingar**.

## <a name="preview-a-css-override-file"></a>Forskoðun á CSS-hnekkingarskrá

Til að forskoða CSS-hnekkingarskrá áður en þú gerir hana virka á lifandi vefsvæði skaltu fylgja þessum skrefum.

1. Í yfirlitssvæðinu til vinstri skaltu velja **Hanna** og síðan, á flipanum **CSS-hnekking**, undir **Tiltækar CSS-hnekkingar** skaltu finna CSS-skrána sem þú ætlar að forskoða.
1. Við hliðina á CSS-skráarheiti skaltu velja **Forskoða svæði**.
1. Í glugganum **Velja slóð** skaltu velja slóð vefsvæðisins sem þú vilt sjá að hnekkingu beitt á og veldu síðan **Í lagi**.
1. Ef mörg afbrigði eru fyrir valda slóði skaltu velja afbrigðið sem óskað er í glugganum **Forskoða afbrigði** sem birtist.

Nýr vafraflipi eða -gluggi opnast þar sem þú getur sannreynt stílhnekkingar gagnvart vefsvæðinu. Þú getur síðan deilt slóðinni með öðrum staðfestum notendum Commerce til skoðunar og endurgjafar.

## <a name="activate-a-css-override-file-on-your-live-site"></a>Virkja CSS-hnekkingarskrá á lifandi vefsvæði

Eftir að þú hefur forskoðað og samþykkt CSS-hnekkingarskrá geturðu virkjað hana á lifandi vefsvæði þínu.

> [!NOTE]
> Aðeins ein CSS-hnekkingarskrá í einu getur verið virk á vefsíðunni. Ef þú virkjar nýja hnekkingarskrá er fyrri hnekkingarskráin óvirk. Gakktu þess vegna úr skugga um að allar nauðsynlegar hnekkingar séu til staðar í einni CSS-hnekkingarskrá.

Til að virkja CSS-hnekkingarskrá skal fylgja þessum skrefum.

1. Í yfirlitssvæðinu til vinstri skaltu velja **Hanna** og síðan, á flipanum **CSS-hnekking**, undir **Tiltækar CSS-hnekkingar** skaltu finna CSS-skrána sem þú ætlar að virkja.
1. Undir CSS-skráarheiti velurðu **Virkja**. Hnekkingarskráin verður strax virk á lifandi vefsvæðinu.

## <a name="deactivate-a-css-override-file-on-your-live-site"></a>Afvirkja CSS-hnekkingarskrá á lifandi vefsvæði

Til að afvirkja CSS-hnekkingarskrá á vefsvæðinu skaltu fylgja þessum skrefum.

1. Í yfirlitssvæðinu til vinstri skaltu velja **Hanna** og síðan, á flipanum **CSS-hnekking**, undir **Tiltækar CSS-hnekkingar** skaltu finna CSS-skrána sem þú ætlar að afvirkja.
1. Undir CSS-skráarheiti velurðu **Afvirkja**. Hnekkingarskráin verður strax óvirk á lifandi vefsvæðinu.

> [!TIP]
> Til að fá aðgang að viðbótarmöguleikum fyrir CSS-hnekkingarskrár skaltu velja úrfellingarmerkið (**...**) við hliðina á CSS-skráarheitinu. Valkostirnir **Hlaða niður**, **Endurnefna** og **Skipta út** eru nauðsynlegir fyrir snöggar breytingar á fyrirliggjandi CSS-hnekkingarskrá.

## <a name="additional-resources"></a>Frekari upplýsingar

[Bæta við lógói](add-logo.md)

[Velja þema svæðis](select-site-theme.md)

[Bæta við táknmynd](add-favicon.md)

[Bæta við opnunarkveðju](add-welcome-message.md)

[Bæta við yfirlýsingu um höfundarrétt](add-copyright-notice.md)

[Bæta tungumálum við síðuna](add-languages-to-site.md)

[Bæta skriftarkóða við síður vefsvæðis til að aðstoða við fjarmælingar](add-telemetry.md)
