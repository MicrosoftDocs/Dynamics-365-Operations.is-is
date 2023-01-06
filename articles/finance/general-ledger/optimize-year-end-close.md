---
title: Fínstilla lokun í árslok
description: Þessi grein lýsir innbótinni fyrir fínstillingu lokunar í árslok sem er í boði fyrir lokun í árslok í fjárhag.
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
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/08/2022
ms.locfileid: "9749996"
---
# <a name="optimize-year-end-close"></a>Fínstilla lokun í árslok

Innbót fyrir fínstillingu lokunar í árslok fyrir Microsoft Dynamics 365 Finance gerir ferli fyrir lokun í árslok kleift að keyra utan Application Object Server (AOS) tilviks fyrir Dynamics 365 Finance. Notast er við örþjónustutækni. Kostirnir við fínstillingu lokunar í árslok eru m.a. bætt afkastageta og minni áhrif á SQL-gagnagrunninn við keyrslur við lokun í árslok.

Til að nota aðgerðina fínstillingu lokunar í árslok verður þú að ljúka eftirfarandi verkum:

1. Setja upp innbótina fyrir innbótina Fínstilla lokun í árslok úr verkefninu í Microsoft Dynamics Lifecycle Services.
2. Virkjun eiginleikans **Fínstilla lokun í árslok** í Eiginleikastjórnun.

> [!NOTE]
> Þú getur enn notað núverandi virkni fyrir lokun í árslok fyrir Finance tilföng með því að óvirkja **Fínstilla lokun í árslok** í Eiginleikastjórnun.

## <a name="improved-performance"></a>Bætt afköst

Eiginleikinn **Fínstilla lokun í árslok** er hannaður til að hraða vinnslu í árslok, sérstaklega fyrir viðskiptavini sem hafa mikið gagnamagn. Þegar lokun í árslok keyrir á þjónustu er gagnafrek vinnslan flutt frá Finance tilföngum til að draga úr vinnslutíma og losa tilföng sem gætu haft áhrif á daglegan rekstur annarra notenda.

Eiginleikinn **Fínstilla lokun í árslok** getur auðveldað þér að ná eftirfarandi markmiðum:

- Bæta afköst við lokun í árslok með því að draga úr keyrslutíma.
- Draga úr áhrifum á aðra ferla í lokun í árslok.
- Bættu skýrslugerð og leiðréttingar fyrir lokun í árslok, vegna þess að lokun í árslok tekur skemmri tíma.

## <a name="new-options-and-visibility"></a>Nýir valkostir og sýnileiki

Þegar eiginleikinn **Fínstilla lokun í árslok** er virkur eru tveimur nýjum dálkum **Niðurstöður** og **Staða**, bætt við á eftirfarandi stöðum:

- Á síðunni **Lokun í árslok**
- Í **Niðurstaða lokunar í árslok** svarglugganum
- Í valkostum **Flutningur fjárhagsvíddar efnahagsreiknings** á síðunni **Sniðmát fyrir lokun í árslok**

Eftirfarandi mynd sýnir dæmi um dálkana **Niðurstöður** og **Staða** á síðunni **Lokun í árslok**. Hægt er að velja tengilinn **Skoða niðurstöður** í dálkinum **Niðurstöður** til að opna niðurstöður loka ársloka. Dálkurinn **Staða** sýnir núverandi stöðu ferlisins fyrir lokun í árslok. Því veita nýju dálkarnir innsýn í framvindu ferlisins fyrir lokun í árslok.

[![Niðurstöður og stöðudálkar á síðu lokunar í árslok.](./media/Yearendclose.jpg)](./media/Yearendclose.jpg)

Að auki, þegar eiginleikinn **Fínstilla lokun í árslok** er virkjaður verður flýtiflipinn fyrir **Fjárhagsvíddir efnahagsreiknings** aðgengilegur á síðunni **Sniðmát árslokalokunar**. Hægt er að nota þennan flýtiflipa til að tilgreina fjárhagsvíddir efnahagsreiknings í smáatriðum þegar ári er lokað. Þessi möguleiki er samhliða þeim möguleika sem þegar er fyrir hendi fyrir rekstrarreikninga.

## <a name="architecture-and-data-flow"></a>Skipulag og gagnaflæði

Til að nota eiginleikann **Fínstilla lokun í árslok** og keyra lokun í árslok í örþjónustu þarf að setja upp innbót fyrir fínstillingu lokunar í árslok úr Lifecycle Services og virkja svo **Fínstilla lokun í árslok** í Eiginleikastjórnun.

Eins og eftirfarandi mynd sýnir staðfestir ferli árslokavinnslu að innbótin sé uppsett og eiginleikinn sé virkur. Sé báðum forsendum fullnægt keyrir árslokunin á örþjónustunni.

[![Gagnaflæðirit.](./media/Lifecycle-services.jpg)](./media/Lifecycle-services.jpg)

## <a name="high-level-flow-for-year-end-close-processing"></a>Mikið flæði fyrir vinnslu lokunar í árslok

1. Árslokaferlið hefst í Finance, í **Fjárhagur \> Loka tímabils \> Lokun í árslok**. Ferlið býr til lokun runuvinnslu og verkefnum fyrir lögaðilana sem verið er að loka.
2. Lokun í árslok ákvarðar hvort keyra eigi lokun í árslok á örþjónustunni eða á núverandi lokunarrökum.

    - Ef þjónustan Fínstilla lokun í árslok er sett upp í Lifecycle Services og eiginleikinn **Fínstilla lokun í árslok** er virkur í Eiginleikastjórnun mun lokun í árslok keyra á örþjónustunni.

        1. Virknin Fínstilla lokun í árslok býr til þjónustuverk fyrir lokun í árslok fyrir alla lögaðila sem verið er að loka og keyrir svo lokunarrök fyrir lokun í árslok. Örþjónustan framkvæmir lokun í árslok.
        2. Finance hlustar á lokun í árslok á örþjónustunni til að ákvarða hvenær örþjónustan er búin. Niðurstöður lokunar í árslok eru síðan uppfærðar á síðunni **Lokun í árslok** í Finance.

    - Annars mun lokun í árslok keyra á núverandi lokunarrökum.
