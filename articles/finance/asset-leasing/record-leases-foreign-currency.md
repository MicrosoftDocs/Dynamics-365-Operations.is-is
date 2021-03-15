---
title: Skrá leigusamninga í erlendum gjaldmiðlum
description: Þetta efnisatriði útskýrir hvernig á að skrá leigusamninga í gjaldmiðlum öðrum en bókhalds- eða skýrslugjaldmiðli.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 7f70442450cc1c814ae23e41a1feb3a63f2aade8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992890"
---
# <a name="record-leases-in-foreign-currencies"></a>Skrá leigusamninga í erlendum gjaldmiðlum

[!include [banner](../includes/banner.md)]

Reikningar eignarleiga fyrir leigusamninga sem eru í gjaldmiðlum öðrum en bókhaldsgjaldmiðlinum eða skýrslugjaldmiðlinum eru stofnaðir á síðunni **Fjárhagsuppsetning**. Allir leigusamningar ættu að vera færðir inn í færslugjaldmiðil þeirra. Með öðrum orðum ætti að færa þær inn í gjaldmiðlinum sem er tilgreindur í leigusamningnum. Þetta efnisatriði útskýrir hvernig á að skrá leigusamninga í gjaldmiðlum öðrum en bókhalds- eða skýrslugjaldmiðli.

Ef verið er að færa inn leigusamning í erlendum gjaldmiðli er afnotaréttur af eign (ROU) afskrifaður bæði í bókhaldsgjaldmiðli og skýrslugjaldmiðli. Þessir gjaldmiðlar eru skilgreindir á síðunni **Fjárhagsuppsetning**. Þessi hegðun er einnig notuð í eignum. Þegar búið er að stofna leigusamning í erlendum gjaldmiðli skal velja færslugjaldmiðil í reitnum **Gjaldmiðill**.

Gengi bókhaldsgjaldmiðilsins er sjálfgefið gildi í reitnum **Bókhaldsgjaldmiðill**. Gengi skýrslugjaldmiðils er sjálfgefið gildi í reitnum **Gengi skýrslugjaldmiðils**. Þessi gengi voru virk á upphafsdegi leigunnar. Reitirnir **Gengi bókhaldsgjaldmiðils** og **Gengi skýrslugjaldmiðils** eru í flýtiflipanum **Upplýsingar um fjárhag og skýrslugjaldmiðil** á síðunni **Upplýsingar um leigu**.

1. Veljið gátreitinn **Fast gengi** til að hnekkja genginu sem var fært inn sjálfkrafa og færið síðan inn nýja gengið.
2. Í öðrum reitum skal færa inn upplýsingar sem eru nauðsynlegar fyrir leiguna og síðan skal velja **Stofna áætlanir**.
3. Á nýju síðunni **Upplýsingar um leigu** skal velja **Bækur**.
4. Á síðunni **Leigubók** á flipanum **Upplýsingar um fjárhag og skýrslugjaldmiðil** skal staðfesta gildi reitanna **Bókhaldsgjaldmiðill upphaflegs afnotaréttar af eign** og **Skýrslugjaldmiðill afnotaréttar af eign**. Hver þessara reita sýnir stöðu afnotaréttar af eign í samsvarandi gjaldmiðli. Þessir reitir eru uppfærðir þegar fjárhagsupplýsingum er breytt. Veljið **Stofna áætlanir** áður en greiðsluáætlun er staðfest.

    Upphaflega bókarfærslan skráir afnotarétt af eign sem notar gengi gjaldmiðla sem er skráð á leigusamningnum. Bókarfærslan inniheldur einnig gildi fyrir reitina **Bókhaldsgjaldmiðill upphaflegs afnotaréttar af eign** og **Skýrslugjaldmiðill upphaflegs afnotaréttar af eign**.

## <a name="subsequent-measurement-for-foreign-currency-leases"></a>Síðari mælingar fyrir leigusamninga í erlendum gjaldmiðli

Afskriftaráætlunin sýnir áætlaðar kostnaðarupphæðir afskrifta í skýrslugjaldmiðlinum, bókhaldsgjaldmiðlinum og færslugjaldmiðlinum.

Til að skoða stöðu afnotaréttar af eign og afskriftarupphæðir í annaðhvort skýrslugjaldmiðlinum eða bókhaldsgjaldmiðlinum skal opna **Afskriftaráætlun eignar** og velja gátreitinn **Sýna upphæðir bókhaldsgjaldmiðils** eða **Sýna skýrslugjaldmiðilsupphæðir**.

Þegar stofnaðar eru kostnaðarfærslur afskrifta á móti leigusamningum sem eru gerðir upp í erlendum gjaldmiðli notar færslan gengið sem er skráð á leigusamningnum. Þar eru einnig notuð gildi **bókhaldsgjaldmiðils upphaflegs afnotaréttar af eign** og **skýrslugjaldmiðils upphaflegs afnotaréttar af eign**.

Hægt er að reikna út heildarupphæð afskrifta með því að nota örlítið annað gengi, þannig að afnotaréttur af eign sé að fullu afskrifaður bæði í bókhaldsgjaldmiðlinum og skýrslugjaldmiðlinum.

Ef leigusamningurinn hefur verið endurflokkaður sem **Frestaðar leigugreiðslur** hreinsar kerfið sjálfkrafa gengi bókhalds-og skýrslugjaldmiðla, ef það hefur þegar verið skilgreint.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]