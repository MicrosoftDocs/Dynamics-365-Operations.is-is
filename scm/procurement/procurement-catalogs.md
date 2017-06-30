---
title: "Innkaupavörulistar"
description: "Þessi grein lýsir, á hærra stigi, hvernig sérfræðingar í innkaupum geta sett upp og viðhaldið innkaupavörulistum. Innkaupavörulistar skilgreina vörur og þjónustu sem starfsmenn fyrirtækja geta pantað fyrir notkun innan fyrirtækisins."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 15767a54da25c293bb3d6d5e0a14e7e05a7d730b
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017


---

# <a name="procurement-catalogs"></a>Innkaupavörulistar

[!include[banner](../includes/banner.md)]


Þessi grein lýsir, á hærra stigi, hvernig sérfræðingar í innkaupum geta sett upp og viðhaldið innkaupavörulistum. Innkaupavörulistar skilgreina vörur og þjónustu sem starfsmenn fyrirtækja geta pantað fyrir notkun innan fyrirtækisins.

innkaupasérfræðingar geta stofna og viðhalda vörulistum fyrir vörur og þjónustu sem má kaupa inn til innri notkunar í fyrirtæki. Eftir vörulista eru settir upp, geta starfsmenn fyrirtækisins stofna innkaupabeiðnir til að panta úr þeim. Hægt er að nota vörulista til að tryggja innkaupareglur, svo starfsmenn geta pantað aðeins vörur og þjónustu sem eru leyfðar fyrir þeirra innkaupalögaðila. Þegar innkaupavörulisti er stofnaður skal huga að eftirfarandi verkum:

-   Stilltu tegundastigveldi innkaupa áður en þú stofnar vörulistann.
-   Ákvarða hvaða vörur starfsmenn eiga að geta pantað. Hægt er að sýna eða fela tiltekna afurðir í hnút vörulista, eða hægt er að sýna eða fela allar afurðir í hnút.
-   Ákvarða hversu margra innkaupavörulista er krafist. Aðgangur að innkaupavörulista ákvarðast af stefnureglu vörulista sem er skilgreind fyrir lögaðilann og rekstrareininguna sem starfsmaður er tengdur við.

Nokkra þætti ákvarða afurðir sem starfsmann geta pantað og þá innkaupaflokka sem þeir geta notað þegar þeir stofna innkaupabeiðnir:

-   Stefnuregla tegundaraðgangs í innkaupastefna ákvarðar hvaða innkaupategundir eru tiltækar í innkaupabeiðni. Ef engin regla er skilgreind eru allar innkaupategundum tiltækar.
-   Starfsmenn geta eingöngu pantað afurð ef það er er í virka innkaupavörulista fyrir fyrirtækið, og ef hann er í virkur hnútur og ekki falinn. Afurðar verður einnig að vera í tegund sem tiltekinn starfsmaður hefur aðgang að samkvæmt stefnureglu aðgangs fyrir tegundina.
-   stefnuregla vörulista tilgreinir vörulista sem er notað. Ef engin stefnureglu vörulista er skilgreind , ákvarðar stefnuregla vörulista ein þær afurðirnar sem starfsmaður getur pantað í beiðninni.

## <a name="prerequisites"></a>Skilyrði
Eftirfarandi tafla lýsir verkefnunum sem verður að vera lokið áður en innkaupa professional hægt að stofna innkaupavörulista.

| Verkefni                                                | Hlutverk               | Lýsing                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Setja upp tegundastigveldi innkaupa            | Innkaupastjóri | Innkaupategundastigveldi eru notuð til að flokka vörur eða færslur fyrir skýrslugerð og greiningar. Með því að nota tegundastigveldi innkaupa geta fyrirtæki stefnubundið stjórnað tegundir, vörur, lánardrottna og öðrum stuðlum innkaupa af miðlægri staðsetningu. Eitt tegundastigveldi innkaupa er skilgreint fyrir heilt fyrirtæki. Vörulistinn er byggð á tegundastigveldi innkaupa: tegundir í stigveldinu verða hnútar í vörulistanum. Lánardrottna og vörur eru teknar með í vörulistanum þínum. |
| Bæta lánardrottnum og afurðum við innkaupaflokka. | Innkaupastjóri | Þegar tegundastigveldi innkaupa er stofnuð fyrir fyrirtækið, hver innkaupategund hægt er að tengja við tiltekna lánardrottna, vörur og svo framvegis. Þessar tengingar eru afrituð sjálfkrafa í vörulistanum.                                                                                                                                                                                                                                                                                           |

## <a name="setting-up-a-catalog"></a>Setja upp vörulista
Eftir að frumskilyrði hafi verið uppfyllt, getur þú sett upp vörulista. Hægt er að stofna eina vörulista sem allt fyrirtækið notar eða margar vörulista sem mismunandi deildir fyrirtækisins nota . Ef stofna á eina vörulista fyrir allt fyrirtækið eru aðgang að vörulistinn er stjórnað af innkaupastefnureglum.  

Vörulistinn skilgreinir hvaða vörur eru tiltækar þegar innkaupabeiðnir eru stofnaðar, en þú getur notað stefnureglur tegundaraðgangs til að beita frekari takmörkunum. Þar sem hnútar í vörulista eru innkaupaflokka, er hægt að fela þær af stefnuregla tegundaraðgangs. Í þessu tilfelli eru afurðir af þeirri tegund ekki tiltækar fyrir starfsmenn til að nota á innkaupabeiðnum.  Stefnureglur tegundaraðgangs eru skilgreindar á síðunni **Innkaupareglur**. Eftirfarandi tafla lýsir verkefnunum sem þarf að ljúka til að setja upp vörulista.

| Verkefni                                                   | Hlutverk             | Lýsing                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Búa til nýtt vörulisti.                                  | Innkaupaaðili | Þegar vörulisti er stofnaðu skaltu tilgreina heiti og lýsingu fyrir vörulistann. Einnig skilgreinirðu hvort vörulistinn er uppfærður sjálfkrafa eða handvirkt og tilgreina eiganda vörulista.                                                                                                                                      |
| Stjórna hvort afurðir eru tiltækar í vörulistanum. | Innkaupaaðili | Þar sem afurðir erfast frá vinnustöðvaflokkum birtast þær allar í viðeigandi vörulistahnútum. Hægt er að stjórna hvort allar afurðir í hnút eru falin eða sýnd þegar vörulista er notuð í innkaupabeiðni. Einnig er Hægt að stjórna hvort einstakar afurðir í hnút eru falin eða sýnd. |
| Birta vörulistann                                   | Innkaupaaðili | Áður en vörulisti er tiltækur fyrir starfsmenn að nota í beiðni, verður þú að skilgreina stefnureglu vörulista, stilla stöðu vörulistans á **Virkur** og birta vörulistann. hægt er að gera vörulista sem ekki er lengur ætlunin að sé til staðar fyrir notendur.                                              |

Uppfærslur eru birt annað hvort sjálfvirkt eða handvirkt, eftir því hvað valkostur er valin fyrir vörulistann í á **Sjálfgefin uppfærslugerð** á í **Vörulista** síðu. Eftirfarandi sjálfvirkar uppfærslugerðir eru tiltækar fyrir vörulista.

-   **Gagnvirk** – Vörulistinn uppfærist sjálfkrafa hvenær sem honum er breytt.
-   **Fastur** – vörulista verður að uppfæra handvirkt.
-   **Bæði** – Ef vörulista inniheldur afurðarflokkar sem hafa sjálfgefinn uppfærslugerð sem **Fasta**, það verður að uppfæra handvirkt þegar þær eru uppfærðar. Ef vörulista inniheldur afurðarflokkar sem hafa sjálfgefinn uppfærslugerð sem **gagnvirkt**, er hann sjálfkrafa uppfærður hvenær sem honum er breytt.


<a name="see-also"></a>Sjá einnig
--------

[Setja upp tegundastigveldi innkaupa (verkefnaleiðbeiningar)](http://ax.help.dynamics.com/en/wiki/set-up-a-procurement-category-hierarchy/)




