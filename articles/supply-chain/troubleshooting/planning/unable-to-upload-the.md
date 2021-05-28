---
title: Ekki er hægt að uppfæra áætlaðan einingarkostnað þegar færslur eftirspurnarspár eru fluttar inn
description: Þegar þú notar gagnaeiningar til að flytja inn færslur eftirspurnarspár er kostnaðarverð fyrir fyrirliggjandi færslur ekki uppfært svo það samsvari innfluttum gögnum.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: c8ea8322a6c7bafe2dfcaaee3e9989f753c85e2a
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026613"
---
# <a name="you-cant-update-the-forecasted-unit-cost-when-you-import-demand-forecast-records"></a>Ekki er hægt að uppfæra áætlaðan einingarkostnað þegar færslur eftirspurnarspár eru fluttar inn

KB númer: 4614109

## <a name="symptoms"></a>Einkenni

Þegar þú notar gagnaeiningar til að flytja inn færslur eftirspurnarspár er gildi **Áætlaður einingarkostnaður** fyrir fyrirliggjandi færslur ekki uppfært svo það samsvari innfluttum gögnum.

## <a name="cause"></a>Orsök

**Áætlaður einingarkostnaður** er skrifvarinn reitur. Gildið er byggt á einingarkostnaði vörunnar og ekki er hægt að stilla það beint í gegnum innflutning.

## <a name="resolution"></a>Upplausn

Þar sem reiturinn er skrifvarinn er ekki hægt að flytja inn gildi fyrir hann. Gildið verður reiknað samkvæmt fyrirliggjandi viðskiptagrunni.
