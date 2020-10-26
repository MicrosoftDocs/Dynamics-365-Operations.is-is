---
title: Kynna afbrigði og ljúka tilraun
description: Þetta efnisatriði lýsir því hvernig á að koma vel heppnuðu afbrigði á framfæri og ljúka tilraun í Dynamics 365 Commerce.
author: sushma-rao
manager: AnnBe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 2e011f10e908d6a2efe2e928fc5e0abc7659cb8b
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930216"
---
# <a name="promote-a-variation-and-complete-an-experiment"></a>Kynna afbrigði og ljúka tilraun

Þetta efnisatriði lýsir því hvernig á að koma afbrigðum á framfæri sem skiluðu bestum árangri í tilrauninni og hvernig á að ljúka við tilraunina. Eftirfarandi skýringarmynd sýnir öll skrefin sem taka þátt í uppsetningu og vinnslu á tilraun á vefsvæði rafrænna viðskipta í Dynamics 365 Commerce. Önnur skref eru afgreidd í aðskildum efnisatriðum.

[ ![Ferli tilraunanotanda - Yfirfara og ljúka](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)

Þegar þú hefur [keyrt tilraunina þína](experimentation-run-monitor.md) og safnað fullnægjandi gögnum til að ákveða hvaða afbrigði þú vilt nota á virka vefsvæðinu þínu, munt þú koma afbrigðinu á framfæri og ljúka við tilraunina.

## <a name="promote-a-variation"></a>Koma afbrigði á framfæri
Notið gögn og greiningar sem tengjast tilrauninni í þjónustu þriðja aðila til að ákveða hvaða afbrigði skilaði bestum árangri. Til að skipta út núverandi efni á virka vefsvæðinu fyrir afbrigðið sem stóð upp úr þannig að það sé tiltækt öllum notendum vefsvæðisins, skal gera eftirfarandi. 

1. Farið í flipann **Tilraunir** í vefsmiðnum og veljið tilraunina.
1. Veljið **Ljúka tilraun** á efstu stikunni.
1. Í svarglugganum **Ljúka tilrauninni** skal velja **Yfirfara gögn tilraunar**. Þjónusta þriðja aðila opnast þar sem hægt er að sannprófa mælingarnar og ákveða hvaða afbrigði skilaði bestum árangri.
1. Í svarglugganum **Ljúka tilrauninni** í vefsmiðnum, skal velja afbrigðið sem stóð upp úr og velja síðan **Næst**.
1. Opnaðu þjónustu þriðja aðila og stöðvaðu tilraunina.
1. Í vefsmiðnum skal velja **Ljúka** til að skrifa yfir upprunalegu virku síðuna og birta afbrigðið sem stóð upp úr þannig að hann sé aðgengilegt öllum notendum vefsvæðisins. 

> [!NOTE]
> Ef valið er að halda núverandi virkri síðu og birta ekki afbrigði skal velja **Endurbirta upprunalegu síðuna**.

## <a name="delete-your-experiment"></a>Eyða tilraun
Þess er ekki krafist að fullbúinni tilraun sé eytt í Commerce, en það má samt sem áður eyða henni til að spara pláss eða hreinsa vinnusvæðið. Til að eyða tilraun skaltu gera eftirfarandi.

1. Farið í flipann **Tilraunir** í vefsmiðnum og veljið tilraunina. 
    > [!NOTE]
    > Ef tilraunin er enn virk skal stöðva hana í þjónustu þriðja aðilans áður en haldið er áfram.
1. Veljið **Taka úr birtingu** í skipanastikunni til að fjarlægja efni afbrigðisins af virka vefsvæðinu.
1. Veljið **Eyða** í skipanastikunni til að eyða tilrauninni.

## <a name="previous-step"></a>Fyrra skref
[Keyra og fylgjast með tilraun](experimentation-run-monitor.md)
