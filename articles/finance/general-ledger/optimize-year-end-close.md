---
title: Fínstilla lokun í árslok
description: Þessi grein lýsir Fínstilltu árslokaþjónustuviðbótinni sem er tiltæk fyrir árslokaferli aðalbókar.
author: moaamer
ms.date: 11/02/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerClosingSheet
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2022-11-28
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: 41d0c2975341cf3d612cc36be348326e24e94f1b
ms.sourcegitcommit: 707957bb7bcd98faf2600eff1c98067901a0fb73
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/08/2022
ms.locfileid: "9749996"
---
# <a name="optimize-year-end-close"></a>Fínstilla lokun í árslok

Optimize árslokaþjónustuviðbót fyrir Microsoft Dynamics 365 Finance gerir lokavinnslu í árslok kleift að keyra utan tilviks Application Object Server (AOS) fyrir Dynamics 365 Finance tilföng. Það notar örþjónustutækni. Ávinningurinn sem tengist Optimize árslokaaðgerðinni felur í sér bættan árangur og lágmarksáhrif á SQL gagnagrunninn við lokavinnslu í árslok.

Til að nota Optimize árslokaaðgerðina verður þú að klára eftirfarandi verkefni:

1. Settu upp Optimize árslokaþjónustuviðbótina úr verkefninu þínu í Microsoft Dynamics Lífsferilsþjónusta.
2. Virkjaðu **Fínstilltu árslok** eiginleiki í Eiginleikastjórnun.

> [!NOTE]
> Þú getur samt notað núverandi lokunaraðgerðir í árslok fyrir Fjármálatilföng með því að slökkva á **Fínstilltu árslok** eiginleiki í Eiginleikastjórnun.

## <a name="improved-performance"></a>Bætt afköst

The **Fínstilltu árslok** eiginleiki er hannaður til að flýta fyrir lokavinnslu í árslok, sérstaklega fyrir viðskiptavini sem hafa mikið magn af gögnum. Þegar áramótin renna út á þjónustu er þunga vinnslan losuð af Finance auðlindum til að draga úr vinnslutíma og losa um auðlindir sem gætu haft áhrif á daglegan rekstur annarra notenda.

The **Fínstilltu árslok** eiginleiki getur hjálpað þér að ná eftirfarandi markmiðum:

- Bættu afköst ársloka með því að draga úr keyrslutíma.
- Draga úr áhrifum á önnur ferli í lok árs.
- Bættu skýrslugerð og leiðréttingar fyrir árslokauppgjör vegna þess að lok ársloka tekur styttri tíma.

## <a name="new-options-and-visibility"></a>Nýir valkostir og sýnileiki

Þegar **Fínstilltu árslok** eiginleiki er virkur, tveir nýir dálkar, **Niðurstöður** og **Staða**, bætist við á eftirfarandi stöðum:

- Á **Lokaárslok** síðu
- Í **Lokatölur um áramót** valmynd
- Í **Flutningur fjárhagsvíddar efnahagsreiknings** valkostir á **Sniðmát fyrir lok ársloka** síðu

Eftirfarandi mynd sýnir dæmi um **Niðurstöður** og **Staða** dálkar á **Lokaárslok** síðu. Þú getur valið **Skoða niðurstöður** hlekkur í **Niðurstöður** dálki til að opna niðurstöður ársloka. The **Staða** dálkurinn sýnir núverandi stöðu lokaferlis í árslok. Þess vegna veita nýju dálkarnir sýnileika í framvindu árslokaferlisins.

[![Niðurstöður og Staða dálkar á lokasíðu ársloka.](./media/Yearendclose.jpg)](./media/Yearendclose.jpg)

Að auki, þegar **Fínstilltu árslok** eiginleiki er virkur, a **Fjárhagsstærðir efnahagsreiknings** flýtiflipinn verður aðgengilegur á **Sniðmát fyrir lok ársloka** síðu. Þú getur notað þennan flýtiflipann til að tilgreina fjárhagsvíddir efnahagsreiknings í smáatriðum þegar þú lokar ári. Þessi hæfileiki er samhliða þeirri hæfni sem þegar er tiltæk fyrir rekstrarreikninga.

## <a name="architecture-and-data-flow"></a>Skipulag og gagnaflæði

Að nota **Fínstilltu árslok** eiginleika og keyra áramótalokun á örþjónustu, verður þú að setja upp Optimize árslokaþjónustuviðbótina frá Lifecycle Services og virkja síðan **Fínstilltu árslok** eiginleiki í Eiginleikastjórnun.

Eins og eftirfarandi mynd sýnir, staðfestir lokavinnsla ársloka að viðbótin sé uppsett og eiginleikinn virkur. Ef báðar forsendurnar eru uppfylltar keyrir árslokun á örþjónustunni.

[![Skýringarmynd gagnaflæðis.](./media/Lifecycle-services.jpg)](./media/Lifecycle-services.jpg)

## <a name="high-level-flow-for-year-end-close-processing"></a>Hátt flæði fyrir loka vinnslu í árslok

1. Árslokaferli hefst í Fjármálum, kl **Aðalbók \> Lokað tímabil \> Lokaárslok**. Ferlið skapar lokunarlotuvinnu og verkefni fyrir þá lögaðila sem verið er að loka.
2. Árslokun ákvarðar hvort áramótalokun ætti að keyra á örþjónustunni eða á núverandi lokunarrökfræði.

    - Ef Optimize árslokaþjónustuviðbótin er sett upp í Lifecycle Services og **Fínstilltu árslok** eiginleiki er virkjaður í eiginleikastjórnun, árslokun mun keyra á örþjónustunni.

        1. Fínstilla árslokaaðgerðin býr til árslokaþjónustuvinnu fyrir hvern lögaðila sem verið er að loka, og keyrir síðan árslokunarrökfræðina. Örþjónustan framkvæmir árslok.
        2. Finance hlustar á árslok á örþjónustunni til að ákvarða hvenær örþjónustunni er lokið. Árslokauppgjör eru síðan uppfærð á **Lokaárslok** síðu í Fjármálum.

    - Annars mun árslok keyra á núverandi lokunarrökfræði.
