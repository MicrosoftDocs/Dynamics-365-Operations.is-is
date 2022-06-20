---
title: Kynna afbrigði og ljúka tilraun
description: Þessi grein lýsir því hvernig á að stuðla að árangursríkri afbrigði og ljúka tilraun í Dynamics 365 Commerce.
author: sushma-rao
ms.date: 06/07/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: 3e9a978551622bbb14d9213f607d9dfabe42672a
ms.sourcegitcommit: ddcb62bb5fbf26a1178c2bb1aec45a3d2362339e
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/07/2022
ms.locfileid: "8942744"
---
# <a name="promote-a-variation-and-complete-an-experiment"></a>Kynna afbrigði og ljúka tilraun

Þessi grein lýsir því hvernig á að kynna tilbrigðið sem skilaði bestum árangri í tilrauninni þinni og hvernig á að klára tilraunina. Eftirfarandi skýringarmynd sýnir öll skrefin sem taka þátt í uppsetningu og vinnslu á tilraun á vefsvæði rafrænna viðskipta í Dynamics 365 Commerce. Fjallað er um fleiri skref í aðskildum greinum.

[ ![Tilraunaferli notanda - Yfirfara og ljúka.](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)

Þegar þú hefur [keyrt tilraunina þína](experimentation-run-monitor.md) og safnað fullnægjandi gögnum til að ákveða hvaða afbrigði þú vilt nota á virka vefsvæðinu þínu, munt þú koma afbrigðinu á framfæri og ljúka við tilraunina.

## <a name="promote-a-variation"></a>Koma afbrigði á framfæri
Notið gögn og greiningar sem tengjast tilrauninni í þjónustu þriðja aðila til að ákveða hvaða afbrigði skilaði bestum árangri. Svo er hægt að kynna það með því að skipta út núverandi efni á virka vefsvæðinu fyrir afbrigðið sem stóð upp úr þannig að það sé tiltækt öllum notendum vefsvæðisins.

Til að stuðla fá bestan árangur skal fylgja þessum skrefum. 

1. Í vefsmið Commerce skal velja **Tilraunir** á vinstra yfirlitssvæðinu og síðan velja tilraunina.
1. Á skipanastikunni skal velja **Ljúka tilraun**.
1. Í svarreitnum **Ljúka tilrauninni** skal velja **Yfirfara gögn tilraunar**. Þjónusta þriðja aðila opnast þar sem hægt er að sannprófa mælingarnar og ákveða hvaða afbrigði skilaði bestum árangri.
1. Í svarglugganum **Ljúka tilrauninni** skal velja afbrigðið sem stóð upp úr og velja síðan **Næst**.
1. Opnaðu þjónustu þriðja aðila og stöðvaðu tilraunina.
1. Í vefsmiðnum skal velja **Ljúka** til að skrifa yfir upprunalegu virku síðuna og birta afbrigðið sem stóð upp úr þannig að hann sé aðgengilegt öllum notendum vefsvæðisins. 

> [!NOTE]
> Ef valið er að halda núverandi virkri síðu og birta ekki afbrigði skal velja **Endurbirta upprunalegu síðuna**.

## <a name="delete-your-experiment"></a>Eyða tilraun
Þess er ekki krafist að fullbúinni tilraun sé eytt í Commerce, en það má samt sem áður eyða henni til að spara pláss eða hreinsa vinnusvæðið. 

Fylgdu þessum skrefum til að eyða lokinni tilraun í Commerce site builder.

1. Veljið **Tilraunir** í vinstri yfirlitssvæði og veljið svo tilraunina. 
    > [!NOTE]
    > Ef tilraunin er enn virk skal stöðva hana í þjónustu þriðja aðilans áður en haldið er áfram.
1. Veljið **Taka úr birtingu** í skipanastikunni til að fjarlægja efni afbrigðisins af virka vefsvæðinu.
1. Veljið **Eyða** til að eyða tilrauninni.

## <a name="previous-step"></a>Fyrra skref
[Keyra og fylgjast með tilraun](experimentation-run-monitor.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
