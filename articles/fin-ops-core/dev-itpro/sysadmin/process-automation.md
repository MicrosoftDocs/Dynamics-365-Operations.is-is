---
title: Sjálfvirkni ferlis
description: Þessi grein birtir upplýsingar um hvernig sjálfvirkni ferlis býður upp á einfalda áætlanagerð fyrir ferla sem runuþjónninn keyrir.
author: RyanCCarlson2
ms.date: 06/29/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProcessScheduleSeries
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-06-30
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: 1a1d152a01e0ebe6a20e2e6b31f12ed7b8deb024
ms.sourcegitcommit: 07ed6f04dcf92a2154777333651fefe3206a817a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2022
ms.locfileid: "9423960"
---
# <a name="process-automation"></a>Sjálfvirkni ferlis

[!include[banner](../includes/banner.md)]

Sjálfvirkni ferlis býður upp á einfalda áætlanagerð fyrir ferla sem runuþjónninn keyrir. Uppfært dagatalsyfirlit áætlaðrar vinnu gerir notendum kleift að skoða og grípa til aðgerða á áætluðum og loknum vinnum.

## <a name="administration"></a>Stjórnun

Síða stjórnunarmiðstöðvar fyrir alla sjálfvirkni ferla finnst kerfisstjórnunareiningunni undir valmyndinni **Uppsetning**. Þessi síða sýnir alla sjálfvirka ferla (raðir) sem settar eru upp í kerfinu. Hún gerir þér einnig kleift að bæta við nýrri sjálfvirkni fyrir ferla beint af síðunni. Þegar búið er að setja upp röð er hægt að stjórna hverri röð úr þessum lista. Hægt er að breyta allri röðinni, eyða henni, skoða öll tilvik í listayfirliti eða slökkva á röðinni ef gera á hlé á áætlaðri vinnu í einhvern tíma. 

Notaðu flipann **Bakgrunnsferlar** á þessari síðu til að stjórna bakgrunnsvinnslum sem eru að keyra í umhverfinu þínu. Veldu **Breyta** til að gera breytingar á áætlun fyrir hvaða bakgrunnsvinnslu sem er. Þessar breytingar geta falið í sér tímabil hvíldarstöðu sem mun valda því að vinnslan fari í „hvíldarstöðu“ eða geri hlé á keyrslu fyrir tiltekið tíma á hverjum degi. Veldu **Skoða síðustu niðurstöður** til að skoða niðurstöður keyrslu fyrir hverja bakgrunnsvinnslu.

Öll ferli sem eru óvirk í eiginleikastjórnun birtast ekki þegar eiginleikinn er óvirkur. Þar að auki mun röðunarvél fyrir sjálfvirkni ferlis ekki tímasetja nein tilvik eða bakgrunnsvinnslur fyrir óvirkan eiginleika. Með því að virkja eiginleikann aftur verða öll tímasett tilvik eða bakgrunnsvinnslur í fortíðinni keyrð strax. Sjálfvirk áætlunarvél ferlisins treystir á runuvinnslu kerfisins, **Bókunarvinnsla sjálfvirkniferlis í kerfinu**, keyri. Ekki má breyta eða eiga við verkið á neinum tímapunkti. Ef þessi runuvinnsla er ekki í gangi eða er í villustöðu skal velja **Frumstilla sjálfvirkni ferlis** til að endurstilla runuvinnsluna. Þessi endurstilling tryggir að öll ný sjálfvirkni sem gefin er út í nýlegri útgáfu af forritinu er frumstillt. 

## <a name="calendar-view"></a>Dagbókaryfirlit

Einn af helstu kostum þess að gera feril sjálfvirkan er möguleikinn á því að sjá áætlaða vinnu í einföldu dagatalsyfirliti.  Þetta yfirlit gerir þér kleift að sjá vinnu eina viku í senn. Þú munt sjá þetta yfirlit hægra megin á síðunni **Sjálfvirkni ferlis**. Fyllt verður út í hana með áætlaðri vinnu fyrir valdar raðir. 

[![Dagatal sjálfvirkni ferlis.](./media/CalendarView2.png)](./media/CalendarView2.png)

## <a name="occurrence-changes"></a>Breytingar á tilviki

Hægt er að breyta hverju tilviki fyrir sig án þess að hafa áhrif á önnur tilvik sem skilgreind er af röðinni þar sem tilvikin áttu uppruna sinn. Tilvik áætlaðrar vinnu er hægt að breyta í dagatalsyfirlitinu með því að velja hnappinn **Skoða/breyta** og velja **Tilvik**. Þessi síða veitir þér aðgang að öllum stillingum sem birtast upphaflega í leiðsagnarforriti fyrir uppsetningu raðar og býður upp á möguleikann á að gera einkvæma breytingu á völdu tilviki. Einnig er hægt að slökkva á tilviki áætlaðrar vinnu með því að velja hnappinn **Gera óvirkt** í dagatalsyfirlitinu.

## <a name="developer-documentation"></a>Fylgiskjöl forritunar

Þróunarrammi ferlisins gerir þróunaraðilum kleift að víkka sjálfvirkni ferlisins. Í fylgiskjölum [Meðhöndla sjálfvirkniramma](../process-automation/process-automation-framework.md) verður að finna upplýsingar um hvernig hægt er að búa til sérsniðin ferli sem þarf að keyra með runuþjóninum sem áætlaður er með leiðsagnarforriti fyrir sjálfvirkni ferlis og birtist sjálfkrafa í dagatalsyfirlitinu.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
