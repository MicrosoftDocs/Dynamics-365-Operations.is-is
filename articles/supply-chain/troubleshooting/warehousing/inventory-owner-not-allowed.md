---
title: Birgðaeigandi er ekki leyfður þegar unnið er úr hreyfingum
description: Þú gætir fengið villuna „Birgðaeigandi %1 er ekki leyfður.“ Vöruhúsakerfisferli styðja aðeins birgðir sem eru í eigu lögaðilans.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4ee29cfc7bad990cd1ee5deaa98fca217af772ed
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476636"
---
# <a name="inventory-owner-not-allowed-when-processing-movements-in-the-warehouse-app"></a>Birgðaeigandi er ekki leyfður þegar unnið er með hreyfingar í vöruhúsaforriti

## <a name="symptoms"></a>Einkenni

Þegar unnið er úr hreyfingum í Warehouse Management-farsímaforriti gætir þú fengið eftirfarandi villuboð:

> Birgðaeigandinn „%1“ er ekki leyfður í þessu ferli.

## <a name="cause"></a>Orsök

Þetta gerist vegna þess að rakningarvíddin **Eigandi** er ekki til staðar þegar Warehouse Management-farsímaforrit er notað fyrir hreyfingar. Regluleg birgðaflutningsfærslubók úr biðlara Supply Chain Management virðist ekki virka eins og ætlað var og aðeins er hægt að bóka hana ef víddin **Eigandi** er fyllt út.

## <a name="resolution"></a>Lausn

Microsoft hefur metið þetta mál og hefur ákvarðað að þetta sé takmörkun eiginleika. Sem stendur styður vöruhúsakerfisferli aðeins birgðir sem eru í eigu lögaðilans.
