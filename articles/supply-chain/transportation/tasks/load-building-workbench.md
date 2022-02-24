---
title: Hlaða sniðmáti hleðslu
description: Þetta efnisatriði útskýrir hvernig á að vinna með vinnusvæði hleðsluáætlunar.
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSLoadBuildWorkbench,TMSLoadBuildTemplateCreate,TMSLoadBuildStrategy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 429a8bac5491a342ecbc8b67c59c71715a4b0889
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646401"
---
# <a name="load-building-workbench"></a>Hlaða sniðmáti hleðslu

Vinnusvæði hleðslunnar er hægt að nota flutningshleðsluáætlanir þegar búið er að búa til hleðslu.

## <a name="create-a-load-building-strategy"></a>Stofna hleðsluáætlunarstefnu

Hleðsluáætlanir eru notaðar til að byggja hleðslur sjálfkrafa. Þessi eiginleiki getur verið gagnlegur við eftirfarandi aðstæður:

- Ef þú sendir reglulega tiltekið safn af afurðum, spara hleðsluáætlanir tíma, því að ekki þarf að búa til sömu hleðsluna í hvert skipti.
- Ef ætlunin er að forðast hálffullar hleðslur til að hámarka skilvirkni, geta hleðsluáætlanir hjálpað til við að fylla hverja hleðslu eins og mögulegt er.

Flutningshleðsluáætlun sem kallast `TMSLoadBuildingVolumeStrategy` býður upp á hleðsluáætlun sem nefnist *Hleðsluáætlun byggð á rúmmáli*. Þessi aðferð gerir kleift að nota hámarks gildi sem eru tilgreind fyrir hæð og þyngd í hleðslusniðmátinu eða hnekkja stillingum með því að færa inn ný gildi. Þessi stefna er eina stefna sem er tilbúin til notkunar. (Hins vegar er hægt að hafa einhverjar sérsniðnar aðferðir.)

Til að nota þessa tilbúnu áætlun *Hleðsluáætlun byggð á magni* skal velja hana í reitnum **Hleðsluáætlun** á síðunni **Vinnusvæði hleðsluáætlunar** (**Flutningsstjórnun &gt; Áætlanagerð &gt; Vinnusvæði hleðsluáætlunar**).

Fylgið þessum skrefum til að búa til flutningshleðsluáætlanir.

1. Farið í **-flutningsstjórnun &gt; Uppsetning &gt; Hleðsluáætlun &gt; Hleðsluáætlanir**.
1. Á aðgerðasvæðinu skal velja **Mynda klasalista** til að ganga úr skugga um þú sért með nýjustu útgáfurnar af öllum aðgengilegum klösum.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Færið inn einkvæmt heiti áætlunar, veljið klasa hleðsluáætlunar fyrir hana og færið inn lýsingu.
1. Í aðgerðarúðunni skal velja **Vista**.
1. Á aðgerðasvæðinu skal velja **Færibreytur**.
1. Á síðunni **Færibreytur fyrir hleðsluáætlun** skal velja **Rúmmálsgeta** og síðan í reitinn **Gildi** skal slá inn prósentu fyrir afkastagetu heildarrúmmáls hleðslunnar sem á að nota fyrir nýju hleðsluáætlunina.
1. Veljið **Þyngdargeta** og síðan í reitinn **Gildi** skal slá inn prósentu fyrir afkastagetu heildarþyngdar hleðslunnar sem á að nota fyrir nýju hleðsluáætlunina.
1. Lokið síðunni **Færibreytur fyrir hleðsluáætlun**.
1. Lokið síðunni **Hleðsluáætlanir**.

Nú er hægt að úthluta hleðsluáætlanir fyrir hleðslusniðmát. Einnig er hægt að nota hann beint í vinnusvæði hleðsluáætlunar.

## <a name="use-a-load-building-strategy-in-the-load-building-workbench"></a>Nota hleðsluáætlunarstefnu í vinnusvæði hleðsluáætlunar

1. Farið í **Flutningsstjórnun &gt; Áætlanagerð &gt; Hlaða sniðmáti hleðslu**.
1. Fylgið einu af eftirfarandi skrefum:

    - Velja þarf stefnu í svæðinu **Hleðsluáætlun**.
    - Ef búið er að skilgreina sniðmát hleðsluáætlunar og því verið úthlutað á hleðsluáætlunina skal á aðgerðasvæðinu í flipanum **Umsjón sniðmáta** velja **Nota sniðmát**. Síðan, í fellilistaglugganum **Nota sniðmát hleðsluáætlunar**, skal velja sniðmát í reitnum **Heiti sniðmáts hleðslu**.

1. Á flipanum **Hlaða sniðmátsröð** skal velja eitt eða fleiri [hleðslusniðmát](load-template.md). Vinnusvæðið reynir að koma hleðslunni fyrir í þessum gerðum af gámum í röðinni sem er tilgreind hér. Yfirleitt ætti að setja minnstu gámana efst í listann til að tryggja að minnsti mögulegi gámurinn sé valinn fyrst.
1. Á aðgerðasvæðinu skal velja **Fyrirhugaður farmur**.
1. Yfirfara tillögur að hleðslum og tillögur að farmlínum.
1. Á aðgerðasvæðinu skal velja **Stofna hleðslur** til að stofna hleðslur sem byggja á upprunaskjalslínum í flýtiflipanum **Fyrirhugaðar farmlínur**.
1. Lokið síðunni **Hlaða sniðmáti hleðslu**.
