---
title: Forkröfur fyrir umreikning staðalkostnaðar
description: Þessi grein lýsir verkum til að framkvæma áður en staðlaður kostnaðarumreikningur er keyrður.
author: JennySong-SH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventStdCostConv
audience: Application User
ms.reviewer: kamaybac
ms.custom: 50891
ms.assetid: 73af66cf-c924-45be-837a-a648dbd05a31
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9295269c9979fb693d6f2976d4960a799d88f5ca
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887546"
---
# <a name="prerequisites-for-a-standard-cost-conversion"></a>Forkröfur fyrir umreikning staðalkostnaðar

[!include [banner](../includes/banner.md)]

Þessi grein lýsir verkum til að framkvæma áður en staðlaður kostnaðarumreikningur er keyrður. 

Áður en staðlaður kostnaðarumreikningur er keyrður, skal fylgja þessum skrefum:

1.  Skilgreina **birgðalíkanaflokk** fyrir staðalkostnað. Notið síðunni vörulíkanaflokkur til að stofna vörulíkanaflokk sem notar birgðalíkan staðalkostnaðar. Þegar umreikningur staðalkostnaðar er settur upp er þessi birgðalíkanaflokkur tengdur vörunum sem verið er að umbreyta.
2.  Úthluta hverri vöru **kostnaðarflokk**.
    -   Kostnaðarflokkur sem er úthlutaður keyptri vöru getur virkað sem grunnur fyrir úthlutun fjárhagslykla sem tengjast stöðluðum kostnaði. Þetta getur falið í sér úthlutun fjárhagslykla fyrir frávik innkaupaverða. Í framleiðsluumhverfi veitir kostnaðarflokkurinn sem er tengdur keyptum íhlutum einnig sundurliðun á útreiknuðum kostnaði framleiddrar vöru.
    -   Kostnaðarflokkur sem er tengdur framleiddri vöru getur virkað sem grunnur fyrir úthlutun fjárhagslykla sem tengjast staðalkostnaði, til dæmis úthlutun fjárhagslykla fyrir framleiðslufrávik.

3.  Úthluta framleiddri vöru **staðlað pöntunarmagn** þegar hún hefur fastan kostnað. Staðlað pöntunarmagn fyrir framleidda vöru þjónar sem lotustærð bókhalds fyrir afborganir af eða hlutfallsdreifingu, fasts kostnaðar. Þetta getur falið í sér uppsetningartíma í leiðaraðgerðum eða fast magn íhlutar í uppskrift (BOM).
4.  Úthluta **fjárhagslyklum** sem eru tengdir staðalkostnaði, sérstaklega endurmatsfráviki. Nota skal **Bókun** síðu (**Birgðastjórnun** &gt; **Uppsetning**) til að úthluta fjárhagslyklum sem eru tengdir við staðalkostnað. Í útreikningi staðalkostnaðar þarf að tengja lykil endurmatsfráviks fyrir allar vörur og kostnaðarflokka. Nota síðuna **bókhaldslykill** til að skilgreina fjárhagslykla sem þarf fyrir staðalkostnað. Notið síðuna **færslusamsetningar** til að virkja kostnaðartengsl (fyrir töflur, flokka og allt) áður en bókunarreglur eru skilgreindar.
5.  Skilgreina þær birgðafæribreytur tengjast staðalkostnaði. Nota skal **Númeraraðir** flipanum á í **færibreytur Birgða- og vöruhúsastjórnunar** síðu til að úthluta númeraröð á fylgiskjöl endurmats. Fylgiskjal endurmats er myndað þegar umreikningur staðalkostnaðar veldur breytingu á birgðavirði vöru. Notið skjámyndina **færibreytur birgða- og vöruhúsastjórnunar** til að skilgreina færibreytur kostnaðarstýringar (á flipanum **birgðabókhald**) til að skilgreina tvær færibreytur sem eru tengdar við staðalkostnað.
    -   Nota skal **sundurliðun Kostnaðar** svæðið til að velja Nei eða Undir fjárhagur. Valið á undir fjárhag kallast virk sundurliðun kostnaðar. Virk sundurliðun kostnaðar er mikilvæg við útreikning, viðhald og yfirlit yfir sundurliðun kostnaðarflokka í margstiga uppbyggingu vöru fyrir staðalkostnaðarvörur. Þegar sundurliðun kostnaðar er virk er hægt að skrá og greina eftirfarandi í einu stigi, mörgum stigum eða heildarsniði:
        1.  Birgðir
        2.  Verk í vinnslu (VÍV)
        3.  Kostnaður seldra vara (cogs) á kostnaðarflokk.

        Virk sundurliðun kostnaðar þýðir að ef þú virkjar kostnaðar framleiddrar vöru leiðir það til þess að sundurliðun kostnaðarflokks er geymd í kostnaðarfærslu vörunnar. Ef ekkert er valið fyrir svæðið **sundurliðun kostnaðar** þýðir það að sundurliðun kostnaðarflokka verði ekki viðhaldið fyrir staðlaðar kostnaðarvörur. Það er að segja að staðalkostnaður framleiddrar vöru verði reiknaður og honum viðhaldið sem einni upphæð innan sundurliðunar kostnaðarflokka og kostnaðarframlegð framleiddra íhluta verði steypt saman í þessa einu upphæð.
    -   Notið svæðið **frávik frá staðal** til að velja samanlagt eða fyrir hvern kostnaðarflokk. Valið Á hvern kostnaðarflokk gerir þér kleift að tilgreina frávik frá innkaupaverði og framleiðsluafbrigði eftir kostnaðarflokki. Þetta einnig þér einnig kleift að tilgreina fjórar gerðir framleiðslufrávika (lotukenni stærð, magn, verð og staðgöngufrávikin). Ef valið er samanlagt þýðir það að ekki verður hægt að tilgreina frávik eftir kostnaðarflokki og ekki verður hægt að tilgreina fjórar gerðir framleiðslufrávika. Aðeins verður hægt að skoða samantekið framleiðslufrávik. Reglan um frávik frá staðli virkar óháð reglunni um sundurliðun kostnaðar. Því er hægt að sleppa því að velja reglu fyrir sundurliðun kostnaðar og velja frávik fyrir hvern kostnaðarflokk til að framleiðslufrávik greinist áfram eftir kostnaðarflokki.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]