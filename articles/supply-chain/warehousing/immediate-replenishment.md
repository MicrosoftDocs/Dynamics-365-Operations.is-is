---
title: Tafarlaus áfylling
description: Þessi grein lýsir því hvernig hægt er að nota tafarlausa áfyllingu til að fylla á birgðir þegar staðsetningarleiðbeining tekst ekki úthluta birgðum.
author: Mirzaab
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocDirTable, WHSReplenishmentTemplates
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: cf48f2f34f574503bbcae827f8013afe8532fc14
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899267"
---
# <a name="immediate-replenishment"></a>Tafarlaus áfylling

[!include [banner](../includes/banner.md)]

Tafarlaus áfylling gerir þér kleift að fylla á birgðir strax eftir að lína staðsetningarleiðbeiningar tekst ekki að úthluta birgðum. Áfyllingin byggist á einni línu í uppsetningu staðsetningarleiðbeiningarinnar. Ef birgðir eru ekki á lager í mælieiningunni sem er tilgreind af þeirri línu, á sér stað áfylling á þessari mælieiningu þegar í stað.

Tafarlaus áfylling býður upp á annan valkost við aðferðina þar sem úthlutun birgða byggist á fleiri línum í staðsetningarleiðbeiningunni og þar sem eftirspurnin er tekin saman við lok úthlutunarinnar og fyllt á í mælieiningunni sem tilgreind er af síðustu línunni í staðsetningarleiðbeiningunni.

Ávinningur þess að nota tafarlausa áfyllingu er sá að hægt er að takmarka áfyllingu með sérstökum einingum og magnið er hægt að stjórna til tiltekinna staða.

## <a name="business-scenario"></a>Sviðsmynd fyrirtækis

Til dæmis ertu með vöruhús sem hefur aðskilin tiltektarsvæði fyrir „kassann“ og „hverja“ mælieiningu. Þú vilt fínstilla tiltektarferlið með því að tína eins marga kassa og mögulegt er og síðan tína allt eftirstandandi magn sem er minna en kassi frá „hverju“ svæðinu.

Í þessu tilviki er hægt að nota tafarlausa áfyllingu. Í staðsetningarleiðbeiningunni er hægt að setja upp tafarlausa áfyllingu fyrir kassa svo eftirspurnaráfylling verði notuð um leið og skortur er á kössum sem hægt er að tína fyrir eftirspurnarmagnið. Með þessum hætti er tiltektarferlið fínstillt þannig að það tiltektin feli í sér eins marga kassa og mögulegt er. Tafarlaus áfylling mun búa til áfyllingu á kössunum og eftirspurnin verður send áfram svo að magnið sé tínt í „hverri“ mælieiningu. Með öðrum orðum verður aðeins magnið sem á að tína í „hverri“ mælieiningu (það er magn sem er minna en kassi) verður valið úr „hverju“ svæðinu. Ef skortur er á „kassa“svæðinu getur þú tínt eins marga kassa og mögulegt er af heildareftirspurninni. Eftirstandandi magn verður síðan tínt úr „hverju“ svæði.

## <a name="where-it-applies"></a>Þar sem það á við

Tafarlaus áfylling er notuð við bylgjukeyrslur ef úthlutun mistekst fyrir línu staðsetningarleiðbeiningar sem áfyllingarsniðmát er sett fyrir.

## <a name="set-up-immediate-replenishment"></a>Setja upp tafarlausa áfyllingu

- Farðu í **Vöruhúsakerfi** \> **Uppsetning** \> **Staðsetningarleiðbeiningar** og síðan í flipanum **Línur** á listanum **Sniðmát tafarlausrar áfyllingar** skal velja áfyllingarsniðmát fyrir bylgjueftirspurn.

Áfyllingarsniðmátinu er beitt ef lína staðsetningarleiðbeiningar tekst ekki að úthluta sérstökum mælieiningum.

## <a name="troubleshooting"></a>Úrræðaleit

Ef tafarlaus áfylling er valin fyrir línu staðsetningarleiðbeiningar, en engin áfyllingarvinna er búin til þegar þú notar sniðmát eftirspurnaráfyllingar fyrir þá línu staðsetningarleiðbeiningar, verður að rannsaka tvær meginorsakir:

- Gakktu úr skugga um að sniðmát eftirspurnaráfyllingar sem er notað sé sett upp til að nota rétt staðsetningarsniðmát og vinnusniðmát af gerðinni **Áfylling**.
- Gakktu úr skugga um að það sé nóg af birgðum á lager á þeirri staðsetningu sem sniðmát eftirspurnaráfyllingar leitar að birgðum á lager fyrir áfyllingu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]