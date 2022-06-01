---
title: Fast kostnaðarverð
description: Þetta efni útskýrir hvernig þú getur stillt og notað föst kvittunarverð í Microsoft Dynamics 365 Supply Chain Management.
author: raprofit
ms.date: 04/25/2022
ms.topic: article
ms.search.form: InventPosting, InventItemGroup, InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2022-04-25
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: 8e26d84ddc309249d8bd6e54987ad3ae8eed68f0
ms.sourcegitcommit: 2b4ee1fe05792332904396b5f495d74f2a217250
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/18/2022
ms.locfileid: "8770338"
---
# <a name="fixed-receipt-price"></a>Fast kostnaðarverð

[!include [banner](../includes/banner.md)]

**Fast kvittunarverð** er valkostur sem þú getur valið á vörulíkanflokki þegar þú notar annað birgðalíkan en *Staðalkostnaður* eða *Vegið meðaltal á hreyfingu*. Í fyrstu útgáfum af Microsoft Dynamics AX, var þessi valkostur nefndur **Staðalkostnaður**. Það var endurnefnt **Fast kvittunarverð** þegar nýja staðalkostnaðarbirgðalíkanið var kynnt í Dynamics AX 2012. Þetta efni útskýrir hvernig þú getur stillt og notað föst kvittunarverð í Dynamics 365 Supply Chain Management.

## <a name="about-fixed-receipt-prices"></a>Um föst kvittunarverð

Þegar þú velur **Fast kvittunarverð** gátreitinn á **Vörulíkanahópur** síðu fyrir vöru notar kerfið innhreyfingarverðið sem staðalkostnað fyrir birgðakvittunina. Ef innkaupaverð og sjálfgefið kostnaðarverð vöru sem er stillt fyrir vöru eru mismunandi er mismunurinn bókaður á **Fastur kvittunarverð hagnaður** eða **Fast verðtap kvittunar** reikning og mótvægi í **Föst kvittunarverð á móti** reikning sem þú tilgreinir á **Birgðafærslusnið** síðu.

Vegna þess að **Fast kvittunarverð** valmöguleikinn er notaður í tengslum við mismunandi birgðalíkön (svo sem fyrst inn, fyrst út (FIFO); síðast inn, fyrst út (LIFO); og vegið meðaltal), *Birgðalokun og aðlögun* ferli mun samt búa til uppgjör og leiðréttingar í samræmi við birgðaregluna sem þú velur á **Vörulíkanahópur** síðu. Hins vegar eru leiðréttingar aðeins gerðar á útgáfum úr birgðum.

Til dæmis hefur þú stillt vöru með vörulíkanaflokki þar sem **Birgðalíkan** reiturinn er stilltur á *FIFO* og **Fast kvittunarverð** valkostur er valinn. Þegar þú færð birgðir í gegnum innkaupapöntun er birgðaverðmæti stillt á gildi sjálfgefið kostnaðarverðs vörunnar við móttöku vöru. Þegar innkaupapöntunin er reikningsfærð, ef reikningsverð er annað, bókar kerfið sjálfgefið kostnaðarverð á losuðu vörunni á birgðareikninginn. Það bókar mismuninn á fasta innhreyfingarverðsreikninginn. Síðar, þegar þú selur eða notar vöruna, notar kerfið hlaupandi meðaltal vörunnar á þeim tíma þegar sölupöntunarreikningurinn var bókaður (nema þú notir merkingu).

Þegar þú keyrir *Birgðalokun og aðlögun* ferli skapar kerfið uppgjör við fyrstu útgáfu gegn fyrstu kvittun. Mismunur á kvittunarverði sem notað var á kvittun og hlaupandi meðaltali sem notað var við útgáfuna er bókaður í nýju fylgiskjali.

## <a name="enable-fixed-receipt-prices"></a>Virkja föst kvittunarverð

Til að virkja fast kvittunarverð fyrir vöru skaltu fylgja þessum skrefum.

1. Opnið **Birgðastjórnun \> Uppsetning \> Birgðir \> Vörulíkanaflokkar.**
2. Búðu til nýjan vörulíkanahóp eða veldu fyrirliggjandi líkanahóp.
3. Á **Kostnaðaraðferð og kostnaðarviðurkenning** flýtiflipann, veldu **Fast kvittunarverð** gátreit.

    > [!NOTE]
    > Þú getur ekki valið **Fast kvittunarverð** gátreit ef **Birgðalíkan** reiturinn er stilltur á *Staðalkostnaður* eða *Hækkandi meðaltal*.

4. Lokið síðunni.

Eftir að þú hefur virkjað **Fast kvittunarverð** valkostur, verður þú að uppfæra birgðafærslusniðið þitt með því að fylgja þessum skrefum.

1. Opnið **Birgðastjórnun \> Uppsetning \> Bókun \> Bókun**.
1. Á **Pöntun** flipa, í **Veldu** dálk, veldu **Fastur kvittunarverð hagnaður**.
1. Á aðgerðasvæðinu skal velja **Ný** til að bæta línu við hnitanetið.
1. Settu upp nýju línuna þannig að hún eigi við vörulíkanaflokkinn sem þú virkjaðir fasta innhreyfingarverðlagningu fyrir og tilgreindu aðalreikninginn sem er notaður til að skrá fasta innhreyfingarverðshagnað fyrir innkaupapantanir. Stilltu aðrar stillingar eftir þörfum.
1. Í **Veldu** dálk, veldu **Fast verðtap kvittunar**. Bættu við nýrri línu sem á við vörulíkanaflokkinn sem þú virkjaðir fasta innhreyfingarverðlagningu fyrir og tilgreindu aðalreikninginn sem er notaður til að skrá fast innhreyfingarverðtap fyrir innkaupapantanir. Stilltu aðrar stillingar eftir þörfum.
1. Í **Veldu** dálk, veldu **Föst kvittun verðjöfnun**. Bættu við nýrri línu sem á við vörulíkanaflokkinn sem þú virkjaðir fasta innhreyfingarverðlagningu fyrir og tilgreindu aðalreikninginn sem er notaður til að skrá fasta móttökuverðsjöfnun fyrir innkaupapantanir. Stilltu aðrar stillingar eftir þörfum.
1. Á **Birgðir** flipa, í **Veldu** dálk, veldu **Fastur kvittunarverð hagnaður**. Bættu við nýrri línu sem á við vörulíkanaflokkinn sem þú virkjaðir fasta innhreyfingarverðlagningu fyrir, og tilgreindu aðalreikninginn sem er notaður til að skrá fasta innhreyfingarverðshagnað fyrir birgðahald. Stilltu aðrar stillingar eftir þörfum.
1. Í **Veldu** dálk, veldu **Fast verðtap kvittunar**. Bættu við nýrri línu sem á við vörulíkanaflokkinn sem þú virkjaðir fasta innhreyfingarverðlagningu fyrir og tilgreindu aðalreikninginn sem er notaður til að skrá fast innhreyfingarverðtap fyrir birgðahald. Stilltu aðrar stillingar eftir þörfum.

> [!NOTE]
> Við mælum venjulega með því að **Fastur kvittunarverð hagnaður** og **Fast verðtap kvittunar** reitirnir nota sama aðalreikninginn fyrir bæði innkaupapantanir og birgðir.

> [!IMPORTANT]
> Þegar þú breytir gildinu í **Verð** sviði á **Stjórna kostnaði** Flýtiflipi á **Útgefnar vörur** síðu endurmetur kerfið ekki sjálfkrafa þær birgðir sem eru til staðar. Sem handvirk lausn skaltu opna **Lokun og aðlögun** síðu og veldu **Aðlögun \> Á hendi** á aðgerðasvæðinu. Veldu síðan hlutina sem eru til staðar og stilltu þá að núverandi verði. Einn skýr kostur við að nota staðlaða kostnaðarbirgðalíkanið er að það veldur því að kerfið endurmetur sjálfkrafa á lager.
