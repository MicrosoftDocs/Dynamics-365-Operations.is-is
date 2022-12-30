---
title: Fast kostnaðarverð
description: Þessi grein útskýrir hvernig er hægt að skilgreina og nota föst innhreyfingarverð í Microsoft Dynamics 365 Supply Chain Management.
author: rachel-profitt
ms.date: 04/25/2022
ms.topic: article
ms.search.form: InventPosting, InventItemGroup, InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2022-04-25
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: d58e8dcc580bf9327cd89427530f59340e27f4aa
ms.sourcegitcommit: 78576abe5c7cbab1bb69d26c999b038e8c24873a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/13/2022
ms.locfileid: "8954693"
---
# <a name="fixed-receipt-price"></a>Fast kostnaðarverð

[!include [banner](../includes/banner.md)]

**Fast innhreyfingarverð** er valkostur sem hægt er að velja í vörulíkanaflokki þegar notað er annað birgðalíkan en *Staðlaður kostnaður* eða *Hlaupið vegið meðaltal*. Í eldri útgáfum af Microsoft Dynamics AX kallaðist þessi valkostur **Staðalkostnaður**. Hann var endurnefndur **Fast innhreyfingarverð** þegar nýja birgðalíkan staðalkostnaðar var kynnt í Dynamics AX 2012. Í þessari grein er útskýrt hvernig á að skilgreina og nota föst innhreyfingarverð í Dynamics 365 Supply Chain Management.

## <a name="about-fixed-receipt-prices"></a>Um föst innhreyfingarverð

Þegar þú velur gátreitinn **Fast verð innhreyfingar** á síðunni **Vörulíkanaflokkur** fyrir vöru notar kerfið verð innhreyfingar sem hefðbundinn kostnað fyrir innhreyfing birgða. Ef innkaupaverð og sjálfgefið kostnaðarverð vöru sem skilgreint er fyrir vöru er mismunandi er munurinn bókaður á lykilinn **Hagnaður á föstu verði innhreyfingar** eða **Tap á föstu verði innhreyfingar** og mótbókaður á lykilinn **Mótbókun fasts innhreyfingarverðs** sem tilgreint er á síðunni **Birgðabókunarregla**.

Þar sem valkosturinn **Fast innhreyfingarverð** er notaður saman með öðrum birgðalíkönum (t.d. fyrst inn, fyrst út (FIFO); síðast inn, fyrst út (LIFO) og vegið meðaltal) mun ferlið *Birgðalokun og leiðrétting* enn búa til jafnanir og leiðréttingar samkvæmt birgðareglunni sem er valin á síðunni **Vörulíkanaflokkur**. Leiðréttingar eru þó aðeins gerðar vegna vandamála úr birgðum.

Til dæmis hefurðu skilgreint vöru með vörulíkanaflokki þar sem reiturinn **Birgðalíkan** er stilltur á *FIFO* og valkosturinn **Fast innhreyfingarverð** er valinn. Þegar birgðir eru mótteknar í gegnum innkaupapöntun er birgðavirðið stillt á virðið fyrir sjálfgefið kostnaðarverð vörunnar við innhreyfingarskjal afurðar. Þegar innkaupapöntunin er reikningsfærð, ef reikningsverðið er annað, bókar kerfið sjálfgefið kostnaðarverð á útgefnu afurðina í birgðalyklinum. Hann bókar mismuninn á rekstrarreikningi fyrir fast verð. Síðar, þegar þú selur eða neytir vörunnar, notar kerfið keyrandi meðaltal fyrir hlutinn á þeim tíma sem reikningur fyrir sölupöntun var birtur (nema þú notir merkingu).

Þegar ferlið *Birgðalokun og leiðrétting* er keyrt býr kerfið til jöfnun við fyrstu úthreyfingu á móti fyrstu innhreyfingu. Mismunurinn á milli innhreyfingarverð sem var notað í innhreyfingarskjalinu og hlaupandi meðaltal sem var notað í úthreyfingunni er bókaður í nýtt fylgiskjal.

## <a name="enable-fixed-receipt-prices"></a>Virkja fast innhreyfingarverð

Til að virkja föst innhreyfingarverð fyrir vöru skal fylgja þessum skrefum.

1. Opnið **Birgðastjórnun \> Uppsetning \> Birgðir \> Vörulíkanaflokkar.**
2. Stofnaðu nýjan vörulíkanaflokk eða veldu fyrirliggjandi líkanaflokk.
3. Í flýtiflipanum **Aðferð kostnaðarútreiknings og kostnaðargreining** skal velja gátreitinn **Fast innhreyfingarverð**.

    > [!NOTE]
    > Ekki er hægt að velja gátreitinn **Fast innhreyfingarverð** ef reiturinn **Birgðalíkan** er stilltur á *Staðalkostnaður* eða *Hlaupandi meðaltal*.

4. Lokið síðunni.

Þegar valkosturinn **Fast innhreyfingarverð** er virkjaður þarf að uppfæra birgðabókunarregluna með því að fylgja þessum skrefum.

1. Opnið **Birgðastjórnun \> Uppsetning \> Bókun \> Bókun**.
1. Í flipanum **Innkaupapöntun**, í dálknum **Velja**, skal velja **Hagnaður á föstu verði innhreyfingar**.
1. Á aðgerðasvæðinu skal velja **Ný** til að bæta línu við hnitanetið.
1. Settu upp nýju línuna þannig að hún eigi við um vörulíkanaflokkinn sem þú virkjaðir fasta innhreyfingarverðlagningu fyrir og tilgreindu aðallykilinn sem er notaður til skrá hagnað af föstu innhreyfingarverði fyrir innkaupapantanir. Stilla aðrar stillingar eins og þú þarft.
1. Í dálkinum **Velja** velur þú **Tap á föstu verði innhreyfingar**. Bætt við nýrri línu sem á við um vörulíkanaflokkinn sem þú virkjaðir fasta innhreyfingarverðlagningu fyrir og tilgreindu aðallykilinn sem er notaður til að skrá tap á föstu innhreyfingarverði fyrir innkaupapantanir. Stilla aðrar stillingar eins og þú þarft.
1. Í dálkinum **Velja** velur þú **Mótbókun fasts innhreyfingarverðs**. Bættu nýrri línu við sem á við um vörulíkanaflokkinn sem þú virkjaðir fasta innhreyfingarverðlagningu fyrir og tilgreindu aðallykilinn sem er notaður til að skrá mótbókanir á föstu innhreyfingarverði fyrir innkaupapantanir. Stilla aðrar stillingar eins og þú þarft.
1. Í flipanum **Birgðir**, í dálknum **Velja**, skal velja **Hagnaður á föstu verði innhreyfingar**. Bættu nýrri línu við sem á við um vörulíkanaflokkinn sem þú virkjaðir fasta innhreyfingarverðlagningu fyrir og tilgreindu aðallykilinn sem er notaður til að skrá hagnað á föstu innhreyfingarverði fyrir birgðir. Stilla aðrar stillingar eins og þú þarft.
1. Í dálkinum **Velja** velur þú **Tap á föstu verði innhreyfingar**. Bætt við nýrri línu sem á við um vörulíkanaflokkinn sem þú virkjaðir fasta innhreyfingarverðlagningu fyrir og tilgreindu aðallykilinn sem er notaður til að skrá tap á föstu innhreyfingarverði fyrir birgðir. Stilla aðrar stillingar eins og þú þarft.

> [!NOTE]
> Yfirleitt er mælt með að reitirnir **Hagnaður á föstu verði innhreyfingar** og **Tap á föstu verði innhreyfingar** noti sama aðallykilinn fyrir bæði innkaupapantanir og birgðir.

> [!IMPORTANT]
> Þegar gildinu er breytt í reitnum **Verð** í flýtiflipanum **Stjórna kostnaði** á síðunni **Útgefnar afurðir** endurmetur kerfið ekki birgðirnar sem eru á lager sjálfkrafa. Sem handvirka hjáleið skal opna síðuna **Lokun og leiðrétting** og velja **Leiðrétting \> Á lager** á aðgerðasvæðinu. Veldu síðan vörurnar sem eru á lager og leiðréttu þær í núverandi verð. Einn skýr kostur við að nota birgðalíkan staðalkostnaðar er að það veldur því að kerfið endurmeti birgðirnar sjálfkrafa.
