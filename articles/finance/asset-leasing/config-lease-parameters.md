---
title: Skilgreina færibreytur leigusamninga (forskoðun)
description: Þessi grein lýsir stillingum fyrir eignaleigu, svo sem öryggisupplýsingar og bókhaldsstillingar.
author: moaamer
ms.date: 01/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: twheeloc
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e878fa7634cfdcc6c0db19a91e771757c545505b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895081"
---
# <a name="configure-lease-parameters"></a>Skilgreina færibreytur leigu

[!include [banner](../includes/banner.md)]

Nokkrar skilgreiningarstillingar hafa áhrif á það hvernig Eignarleiga virkar. Þessar stillingar innihalda færslubókarnöfn, almennar færibreytur og stillingar bókunarreglu.

1. Opnið **Eignarleiga \> Uppsetning \> Færibreytur fyrir eignarleigu**.
2. Á flipanum **Leigusamningar** skal velja flipann **Almennt**.

    **Heimila Handvirk flokkun hnekking** færibreyta ákvarðar hvort hægt sé að hnekkja flokkun leigusamninga áður en greiðsluáætlun er staðfest.

    The **Krosseiningarlota** færibreytan ákvarðar hvort hægt sé að bóka á aðra lögaðila frá núverandi lögaðila. Ef kveikt er á þessari færibreytu er hægt að stofna bókarfærslu fyrir lögaðilana sem notandinn hefur aðgang að.

3. Stilltu **Leyfa eyðingu staðfestra leigusamninga** valmöguleika til **Já** að heimila að leigusamningum sem hafa staðfestar greiðsluáætlanir verði eytt. Ekki er hægt að eyða leigusamningum ef bókaðar eða óbókaðar færslur eru tengdar þeim, óháð hvernig þessi valkostur er stilltur. Ekki er hægt að endurheimta leiguskrá eftir að henni hefur verið eytt. Ef færslum fyrir eyddan leigusamning er hlaðið upp, annaðhvort handvirkt eða með gagnaeiningum, eru hlaðnar upplýsingar meðhöndlaðar sem nýjar, ekki sem uppfærslur á fyrirliggjandi leigusamningi.

    Ef þessi valkostur er stilltur á **Já**, og breytingagerð bókarinnar er **valkostur A eða B fyrir uppsafnaða endurnýjun**, stillir kerfið reitinn **vextir á nýju lánsfé** við gildi **vextir á nýju lánsfé við umbreytingu** reitinn í **bókaruppsetning** síða. Ef þessi valkostur er stilltur á **Nei** er taxtinn á höfuð leigusamningsins stilltur á gildi **vextir á nýju lánsfé** á síðunni **bókarupplýsingar**, óháð umbreytingargerð á bókinni.

4. Stilltu **Leyfa bakfærslur afskrifta á lokaðri bók** valmöguleika til **Já** til að hægt sé að bakfæra viðskipti með afskriftir. Hægt er að bakfæra kostnaðarfærslur jafnvel þegar bókaútgáfan er lokuð.

    > [!NOTE]
    > Mælt er með því að þessi valkostur sé stilltur á **Nei**. Stillingin fyrir þennan valkost er notuð sem staðfesting og stjórnun til að koma í veg fyrir að lokuð bókaútgáfa sé óvart afskrifuð. Með því að stilla valkostinn á **Nei** er hjálpað við að halda bókuðu nettóvirði og útreikningum á afskriftum í framtíðinni réttum.

5. Stilltu **Leyfa sundurliðun greiðsluupphæðar** valmöguleika til **Já** að leyfa sundurliðun á greiðsluupphæðum á **Greiðsluáætlunarlínur** Flýtiflipi á **Leiga** síðu. Greiðslusundurliðunargerðirnar eru skilgreindar undir **Uppsetning** á **Tegundir greiðsluupphæða** síðu. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
