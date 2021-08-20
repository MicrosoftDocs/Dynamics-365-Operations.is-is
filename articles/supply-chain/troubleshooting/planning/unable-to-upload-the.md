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
ms.openlocfilehash: de471da861785f283eeaa78f97b5d1e1a6b023d71de6fff72ae39edd6bb124cc
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6765371"
---
# <a name="you-cant-update-the-forecasted-unit-cost-when-you-import-demand-forecast-records"></a>Ekki er hægt að uppfæra áætlaðan einingarkostnað þegar færslur eftirspurnarspár eru fluttar inn

KB númer: 4614109

## <a name="symptoms"></a>Einkenni

Þegar þú notar gagnaeiningar til að flytja inn færslur eftirspurnarspár er gildi **Áætlaður einingarkostnaður** fyrir fyrirliggjandi færslur ekki uppfært svo það samsvari innfluttum gögnum.

## <a name="cause"></a>Orsök

**Áætlaður einingarkostnaður** er skrifvarinn reitur. Gildið er byggt á einingarkostnaði vörunnar og ekki er hægt að stilla það beint í gegnum innflutning.

## <a name="resolution"></a>Upplausn

Þar sem reiturinn er skrifvarinn er ekki hægt að flytja inn gildi fyrir hann. Gildið verður reiknað samkvæmt fyrirliggjandi viðskiptagrunni.
