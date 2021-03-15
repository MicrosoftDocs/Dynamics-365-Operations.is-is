---
title: Skilgreina færibreytur leigusamninga (forskoðun)
description: Þetta efnisatriði lýsir skilgreiningarstillingum fyrir Eignaleigu, svo sem öryggisupplýsingum og bókhaldsstillingum.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ff0aa5fd0b78814dfa5bb00d6d5ef2984c566d14
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971404"
---
# <a name="configure-lease-parameters"></a>Skilgreina færibreytur leigu

[!include [banner](../includes/banner.md)]

Nokkrar skilgreiningarstillingar hafa áhrif á það hvernig Eignarleiga virkar. Þessar stillingar innihalda færslubókarnöfn, almennar færibreytur og stillingar bókunarreglu.

1. Opnið **Eignarleiga \> Uppsetning \> Færibreytur fyrir eignarleigu**.
2. Á flipanum **Leigusamningar** skal velja flipann **Almennt**.

    **Heimila Handvirk flokkun hnekking** færibreyta ákvarðar hvort hægt sé að hnekkja flokkun leigusamninga áður en greiðsluáætlun er staðfest.

    **Runueining yfir allt** færibreytan ákvarðar hvort hægt er að bóka á aðra lögaðila frá núverandi lögaðila. Ef kveikt er á þessari færibreytu er hægt að stofna bókarfærslu fyrir lögaðilana sem notandinn hefur aðgang að.

3. Stilla **leyfa eyðingu á staðfestum leigusamningum** valkostur á **Já** til að heimila leigusamninga sem eru með staðfestar greiðsluáætlanir sem á að eyða. Ekki er hægt að eyða leigusamningum ef bókaðar eða óbókaðar færslur eru tengdar þeim, óháð hvernig þessi valkostur er stilltur. Ekki er hægt að endurheimta leiguskrá eftir að henni hefur verið eytt. Ef færslum fyrir eyddan leigusamning er hlaðið upp, annaðhvort handvirkt eða með gagnaeiningum, eru hlaðnar upplýsingar meðhöndlaðar sem nýjar, ekki sem uppfærslur á fyrirliggjandi leigusamningi.

    Ef þessi valkostur er stilltur á **Já**, og breytingagerð bókarinnar er **valkostur A eða B fyrir uppsafnaða endurnýjun**, stillir kerfið reitinn **vextir á nýju lánsfé** við gildi **vextir á nýju lánsfé við umbreytingu** reitinn í **bókaruppsetning** síða. Ef þessi valkostur er stilltur á **Nei** er taxtinn á höfuð leigusamningsins stilltur á gildi **vextir á nýju lánsfé** á síðunni **bókarupplýsingar**, óháð umbreytingargerð á bókinni.

4. Stilla valkostinn **útgáfu Leyfa bakfærslur afskrifta í lokaðri bók** á **Já** til að leyfa að hægt sé að bakfæra afskriftarkostnaðarfærslur. Hægt er að bakfæra kostnaðarfærslur jafnvel þegar bókaútgáfan er lokuð.

    > [!NOTE]
    > Mælt er með því að þessi valkostur sé stilltur á **Nei**. Stillingin fyrir þennan valkost er notuð sem staðfesting og stjórnun til að koma í veg fyrir að lokuð bókaútgáfa sé óvart afskrifuð. Með því að stilla valkostinn á **Nei** er hjálpað við að halda bókuðu nettóvirði og útreikningum á afskriftum í framtíðinni réttum.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]