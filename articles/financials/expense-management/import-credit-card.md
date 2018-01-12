---
title: "Flytja inn og vinna með kreditkortafærslur"
description: "Í þessu efnisatriði er útskýrt hvernig á að flytja inn og viðhalda kostnaðartengdum kreditkortafærslum. Hægt er að setja upp þessar færslur þannig að þær séu fluttar inn sjálfkrafa á endurteknum tíma, og einnig er hægt að flytja þær inn handvirkt eftir þörfum."
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: knelson
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e640c9e44add5599be4a2e381b4ffd81f212889c
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="import-and-maintain-credit-card-transactions"></a>Flytja inn og vinna með kreditkortafærslur

[!include[banner](../includes/banner.md)]

Kostnaðartengdar kreditkortafærslur er hægt að setja upp þannig að þær séu fluttar inn sjálfkrafa á endurteknum tíma. Einnig er hægt að flytja viðskiptin inn handvirkt eftir þörfum. Kreditkortafærslurnar eru fluttar inn gagnaeiningunni Kreditkortafærslur.

Frekari upplýsingar um gagnaeiningar er að finna í [Gagnaeiningar](../../dev-itpro/data-entities/data-entities.md).

## <a name="import-credit-card-transactions"></a>Flytja inn kreditkortafærslur

1. Á síðunni **Kreditkortafærslur** skal velja **Flytja inn færslur**. Ef þú opnar gagnastjórnun í fyrsta skipti verður kerfið að uppfæra lista yfir gagnaeiningar áður en hægt er að halda áfram.
2. Í reitnum **Heiti** skal slá inn einkvæma lýsingu innflutningsverksins.
3. Í **Snið upprunagagna** reitnum skal velja snið skárinnar sem inniheldur kreditkortafærslurnar til innflutnings.
4. Smellið á **Flytja inn** og veljið síðan skrána til að flytja inn.
5. Eftir að skránni hefur verið hlaðið upp skal staðfesta vörpun kreditkortafærslunnar og dálka gagnaeiningar kreditkortafærslunnar með því að velja **Skoða kort** tengilinn á reitnum. Ef um er að ræða vörpunarvillur, eða ef nauðsynlegt er að breyta vörpuninni skal gera breytingar á vörpuninni í flipanum **Vörpunarbirting** eða **Vörpunarupplýsingar**.
6. Til að gera kreditkortafærslur sjálfvirkar skal velja **Stofna endurtekna gagnavinnslu**. Svo er hægt að velja endurtekningar sem skilgreina hversu oft kreditkortafærslurskuli fluttar inn. Þegar þú hefur lokið þessu skaltu velja **Í lagi**.
7. Til að flytja inn völdu skrána strax skaltu velja **Flytja inn**.
8. Ef villur eiga sér stað við innflutning er hægt að skoða keyrsluskrána eða sviðsetningargögn til að sjá villurnar sem verður að laga til að tryggja að innflutningur heppnist.

> [!NOTE]
> Ef nauðsynlegt er að flytja inn fleiri en eitt skjalasnið þarf að búa til aðskilin innflutningsverk fyrir hverja skjalagerð.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Endurúthluta kreditkortafærslum fyrir starfsmenn sem hafa lokið störfum

Þegar samningi starfsmanns er sagt upp er AD DS (Active Directory Domain Services) reikningur hans er gerður óvirkur. Hins vegar gætu verið virkar kreditkortafærslur sem þarf samt að gjaldfæra og endurgreiða. Á síðunni **Kreditkortafærslur** er hægt að endurúthluta starfsmanni á allar kreditkortafærslur þar sem tengdum starfsmanni hefur verið sagt upp störfum.

Veldu eina eða fleiri kreditkortafærslur og svo **Endurúthluta færslu**. Þú getur síðan valið annan starfsmann til að úthluta kreditkortafærslunum á. Eftir endurúthlutun kreditkortafærsluna er hægt að velja þær fyrir kostnaðarskýrslu og greiða hana með reglulegu ferli fyrir endurgreiðslu kostnaðarskýrslu.

