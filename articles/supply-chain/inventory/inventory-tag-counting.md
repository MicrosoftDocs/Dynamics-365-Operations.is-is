---
title: Birgðatalning
description: Þetta efnis veitir upplýsingar um birgðamerkjatalningu, sem þú notar til að bera saman rauninnihald vöruhúss við lagerbirgðir.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCountTag
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Retail
ms.custom: 11594
ms.assetid: 03772d0e-5c37-454c-ab85-82bc8b60a76d
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: efb555cdfbcf3fd0c10ec0e2abcdbe7f4a90d82d
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3212688"
---
# <a name="inventory-tag-counting"></a>Birgðatalning

[!include [banner](../includes/banner.md)]

Þetta efnis veitir upplýsingar um birgðamerkjatalningu, sem þú notar til að bera saman rauninnihald vöruhúss við lagerbirgðir.

Með því að stofna línur á **Merkjatalning** síðunni er sett merkjanúmer á hverja birgðavöru t.d. númer frá 1 upp í 500. Meðan á talningu stendur eru°færð inn vörunúmer og magn á tilheyrandi merki. Síðan er hægt að nota þetta merki sem grunn fyrir innlegg í merkjatalningarbók. Þegar merkjatalningarbók er bókuð er ný talningarbók stofnuð á síðunni **Talning**. Ný færslubók er byggt á merkjatalningu í færslubókarlínum sem voru stofnaðar. Til að framkvæma merkjatalningu á vörum eftir tiltekinni birgðavídd, skaltu velja víddina á síðunni **Birta vídd** sem birtist þegar merkjatalningarbókin er stofnuð. Til dæmis, til að telja vörur í ákveðnu vöruhúsi, veljið gátreitinn **Vöruhús**. Ef sleðinn **Læsa vörum meðan á talningu stendur** á síðunni **Færibreytur birgða- og vöruhúsakerfis** er valinn er ekki hægt að uppfæra vörur efnislega meðan á talningu stendur. Hins vegar eru vörur í merkjatalningarbókum ekki læstar meðan á talningu stendur. Birgðafærslur eru ekki stofnaðar þar til merkjatalningarlínur eru bókaðar og fluttar í talningarbók. Ef seðlar eru færðir inn af handahófi og óskað er eftir að skilgreina merki sem vantar, er smellt á dálkhausinn **Merki** til að raða línum eftir merki.

## <a name="additional-resources"></a>Frekari upplýsingar

[Regluleg talning](../warehousing/cycle-counting.md)
