---
title: Leiðrétt spá heimiluð
description: Ekki skal samþykkja öll spágögn strax. Þessi grein útskýrir hvernig hægt er að tilgreina tímabilið sem spá er heimiluð fyrir. Hún útskýrir líka hvernig á að heimila spá fyrir tiltekin fyrirtæki og spárlíkön.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanImportForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72734
ms.assetid: cb8fd809-605a-4a8b-a390-636edfec21f9
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8ab8558f25f5ffd3b7eb3e1bc5680b1a1f8d5139
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4961446"
---
# <a name="authorize-an-adjusted-forecast"></a>Leiðrétt spá heimiluð

[!include [banner](../includes/banner.md)]

Ekki skal samþykkja öll spágögn strax. Þessi grein útskýrir hvernig hægt er að tilgreina tímabilið sem spá er heimiluð fyrir. Hún útskýrir líka hvernig á að heimila spá fyrir tiltekin fyrirtæki og spárlíkön.

Ekki skal samþykkja öll spágögn strax. Hægt er að tilgreina upphafs- og dagsetningar tímabilsins sem spáin er heimiluð fyrir. Þessi aðgerð gerir það mögulegt að frysta tiltekna ramma. 

Upphafs- og lokadagsetningar sem eru tilgreindar verða að samsvara upphafs- og lokadagsetningum ramma sem spáin er mynduð í. Kerfið setur þessar takmarkanir og leiðréttir sjálfvirkt dagsetningar, ef leiðréttingar er þörf. 

Á flipanum **Upplýsingar** á síðunni **Heimild** er hægt að skoða upplýsingar um spána sem síðast var mynduð. 

Hægt er að velja þau fyrirtæki og nota spálíkön til að heimila spá fyrir. Sjálfgefið er að hnitanetið felur í sér öll þau fyrirtæki sem spáreftirspurn hefur verið stofnuð fyrir. Fyrir hvert fyrirtæki er spárlíkan sem samsvarar gildandi spáráætlun sem sett er upp í færibreytum aðalröðunar fyrirfram fyllt út fyrir hvert fyrirtæki. Hins vegar er hægt að breyta þessu spárlíkani í hvaða spálíkan sem er sem tilheyrir því fyrirtæki. Ef engin gögn um spáreftirspurn voru mynduð fyrir valið fyrirtæki mun viðvörunarboð berast á innflutningstíma. 

Mjög mikilvægt er að skilja hvernig gátreiturinn **Vista handvirkar leiðréttingar á grunnlínu eftirspurnarspár** virkar. Ef gerð hafa verið handvirkar leiðréttingar á tölfræðilegri grunnlínuspá eru leiðrétt gildi heimil til notkunar, jafnvel þó að gátreiturinn sé hreinsaður. Hins vegar er breytingunum fleygt eftir heimildina. Þess vegna, næst þegar spá er mynduð er sú spá aðeins tölfræðileg spá og ekki með neinar handvirkar hnekkingar, jafnvel þótt **Flytja handvirkar leiðréttingar á eftirspurnarspánni** sé valinn. Þess vegna er hægt að líta á gátreitinn **Vista handvirkar leiðréttingar á grunnlínu eftirspurnarspár** sem ferli sem gerir kleift að halda eða henda öllum handvirkum breytingum.

<a name="additional-resources"></a>Frekari upplýsingar
--------

[Gera handvirkar leiðréttingar á grunnlínuspánni](manual-adjustments-baseline-forecast.md)

[Eftirlit með nákvæmni spár](monitor-forecast-accuracy.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]