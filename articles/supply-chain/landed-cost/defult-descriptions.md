---
title: Sjálfgefnar lýsingar fyrir fjárhag
description: Hægt er að nota sjálfgefnar lýsingar til að uppfæra lýsingarreitinn í bókun fylgiskjala í fjárhag.
author: sherry-zheng
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TransactionTexts
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 25dd72c86b22b50eccef22a5d2cbcfcf04280684
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021613"
---
# <a name="default-descriptions-for-the-general-ledger"></a>Sjálfgefnar lýsingar fyrir fjárhag

[!include [banner](../../includes/banner.md)]

Hægt er að nota sjálfgefnar lýsingar til að uppfæra reitinn **Lýsing** í bókun fylgiskjala í fjárhag. Verið er að auka þessa virkni þannig að hún virki með Heildarkostnaður.

Til að setja upp sjálfgefnar lýsingar fyrir fjárhagsbókanir skal fara í **Stjórnun fyrirtækis \> Uppsetning \> Sjálfgefnar lýsingar**.

Í eftirfarandi töflu er listi yfir ný gildi sem hefur verið bætt við reitinn **Lýsing** á síðunni **Sjálfgefnar lýsingar** til að styðja við heildarkostnað.

| Gerð lýsingar | Athugasemdir |
|---|---|
| Flytja inn kostnað – uppsafnaður kostnaður | Þegar innkaupapöntunarreikningur er bókaður er kostnaðaruppsöfnun unnin fyrir áætlun ferðakostnaðar. Hægt er að tilgreina sjálfgefnar lýsingar til að bæta ferðanúmeri við lýsinguna. Nota *%4* fyrir sendingarnúmerið. |
| Flytja inn kostnaðarútreikning – vöruflutningspöntun | Ef verið er að nota vinnslu fyrir vörur í flutningi verður innkaupapöntunarreikningurinn bókaður og vörurnar eru bókaðar á vöruflutningalykil. Hægt er að tilgreina sjálfgefnar lýsingar til að bæta pöntunarnúmeri í flutningi við lýsinguna. Nota *%4* fyrir númer pöntunar í flutningi. |
| Birgðir - lokun - Leiðrétting | Þegar reikningur viðskiptaskulda er afgreiddur fyrir kostnað ferðar er unnið úr leiðréttingu á birgðaskrá til að áætla kostnað ferðarinnar. Hægt er að tilgreina sjálfgefnar lýsingar til að bæta ferðanúmeri við lýsinguna. Nota *%4* fyrir sendingarnúmerið. |

Frekari upplýsingar um hvernig á að vinna með síðuna **Sjálfgefnar lýsingar** er að finna í [Setja upp sjálfgefnar lýsingar fyrir sjálfvirka bókun](../../finance/general-ledger/set-up-default-descriptions-for-automatic-posting.md).
