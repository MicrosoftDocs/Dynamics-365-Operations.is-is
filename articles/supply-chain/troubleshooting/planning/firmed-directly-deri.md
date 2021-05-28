---
title: Unnið er úr beint afleiddum staðfestum pöntunum með verkflæði endurskoðunar
description: Beint afleiddar staðfestar pantanir eru unnar með vinnuflæði sem hefur stöðuna Í endurskoðun.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: d54985707d82df2b947a7cb615fc25f90aa31702
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026617"
---
# <a name="directly-derived-firmed-orders-are-processed-by-an-in-review-workflow"></a>Unnið er úr beint afleiddum staðfestum pöntunum með verkflæði endurskoðunar

KB númer: 4612450

## <a name="symptoms"></a>Einkenni

Beint afleiddar staðfestar pantanir eru unnar með vinnuflæði sem hefur stöðuna *Í endurskoðun*.

## <a name="resolution"></a>Upplausn

Þegar kveikt er á breytingarrakningu er staðan *Í endurskoðun* úthlutuð á staðferstar afleiddar pantanir (innkaupapantanir undirverktaka). Ef innkaupapöntun er afleidd (innkaupapöntun undirverktaka) er hún því aðeins send í vinnuflæði. Ef innkaupapöntun er staðfest innkaupatillaga er hún sjálfkrafa samþykkt til að tryggja að áætlunarvélin stofni ekki nýjar áætlaðar pantanir á meðan innkaupapöntunin er enn í stöðunni *Drög*.
