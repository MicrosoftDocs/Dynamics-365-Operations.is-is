---
title: Setja upp verktilföng.
description: Þetta efnisatriði gefur upplýsingar um uppsetningu eða beiðni verktilfanga.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c882e23794e3937f85b3e73774b36deaf28ac3ed
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760578"
---
# <a name="set-up-project-resources"></a>Setja upp verktilföng.

[!include [banner](../includes/banner.md)]

Þú þarft að setja upp dagatal og tengja það við starfsmann eða starfskraft. Dagatalið er notað til að áætla verkið og vinnutíma þeirra tilfanga sem eru frátekin fyrir verkið. Við uppsetningu dagatals geta verkefnisstjórar framkvæmt sléttun á tilföngum sem hluta af fínstillingu tilfanga. Samkvæmt áætlun dagatals geta takmarkanir verið settar á tilföng. Hægt er að setja upp dagatal sem á síðunni **Dagatöl**.

Þegar starfsmaður er settur upp sem tilföng verks er hægt að velja úr starfsmönnum sem vinna í fyrirtækinu þar sem verið er að setja upp tilföng. Einnig er hægt að velja starfskraftur úr öðrum fyrirtækjum innan fyrirtækisins þíns. Þessir starfskraftar eru þekktir sem samstæðutilföng.

Eftirfarandi ferli útskýra hvernig setja á upp starfsmanns sem tilföng verks innan fyrirtækisins og hvernig á að setja upp samstæðuverk tilfanga.

## <a name="set-up-a-worker-as-a-project-resource"></a>Setja upp starfmann sem verktilfang.

1. Á síðunni **Starfsmenn**, í listanum **Starfsfólk**, veljið starfsmann sem verið er að bæta við sem tilfang verks og opnið skrá starfsmannsins.
2. Á Aðgerðasvæðinu skal velja **Verk** &gt; **Uppsetning** &gt; **Verkuppsetning**.
3. Velja skal Dagatal og loka svo síðunni.

Einnig er hægt að tilgreina sjálfgefið verk fyrir tilföng sem gerð áætlaðs verkefnis. Hægt er að nota áætlaðar úthlutanir þegar tilfangastjórnandi eða verkstjóri veit hvaða verk tilfangið verður að vinna að fyrirfram. Einnig er hægt að byggja áætlaðar úthlutanir á beiðni kostunaraðila verks eða viðskiptavinar. Til að úthluta verki fyrirfram: Á síðunni **Úthluta verkum**, á flipanum **Verk**, á listanum **Eftirstandandi verk** skal velja viðeigandi verk.

## <a name="set-up-an-intercompany-resource"></a>Setja upp samstæðutilföng

Þegar starfsmaður er settur upp sem samstæðutilföng verður að ljúka uppsetningunni í bæði útlánafyrirtækinu og lántökufyrirtækinu.

### <a name="in-the-lending-company"></a>Í útlánafyrirtækinu:

1. Í Finance skal staðfesta að útlánafyrirtækið sé valið, og ljúka síðan ferlinu hér að framan, „Setja upp starfsmann sem tilfang verks“.
2. Á síðunni **Samstæðulyklar** skal velja **Nýtt**.
3. Í svæðinu **Kenni lögaðila** skal velja útlánafyrirtæki. Fyllið út eftirstandandi svæði eftir þörfum og velja svo **Vista**.
4. Á síðunni **Innanhússverð** skal velja **Nýtt**.
5. Í **Lögaðili sem fær lánað** reitnum skal velja viðkomandi fyrirtæki.
6. Til að lána lántökufyrirtækinu aðeins þau tilföng sem voru stofnuð í upphafi þessa hluta í svæðinu **Tilföng** skal velja nafn tilfanganna sem voru stofnuð. Til að gera öll tilföng í fyrirtækinu tiltæk lántökufyrirtæki skal skilja svæðið **Tilföng** eftir autt.
7. Á **Verkefnastjórnun og bókhaldsfæribreytur** síðunni, á flipanum **Samstæða** Skal stilla **Virkja samstæðuröðun tilfanga og tímablöð** valkostinn á **Já**.

### <a name="in-the-borrowing-company"></a>Í lántökufyrirtækinu:

- Á **Tilfangalisti** síðunni skal færa inn heiti tilfangs sem þú stofnaðir í útlánafyrirtækinu til að staðfesta að heitið sé innifalið í tilfangalistalántökufyrirtækis.

## <a name="request-project-resources"></a>Biðja um verktilföng
Virknin fyrir röðun verktilfanga styður aðeins stjórnendur tilfanga til að dreifa mönnuðum tilföngum á úttektir eða verk. Til að virkja þennan eiginleika skal ljúka eftirfarandi verkum eða að staðfesta að þeim sé lokið:

- Setja upp númeraraðir.
- Setja upp verkflæði fyrir verkefnastjórnun og bókhald
- Virkja verkflæði tilfangabeiðni.

Eftir að fyrri verkefnum hefur verið lokið er hægt að ljúka eftirfarandi verkefnum eftir þörfum:

- Stofna beiðni tilfanga úr óbundið mönnuðum tilföngum.
- Fylgjast með tilfangabeiðnum.
- Uppfylla tilfangabeiðnir.
- Biðja um mönnuð tilföng úr WBS.
- Bóka tilföng á verk án þess að þurfa að biðja um mönnuð tilföng.
