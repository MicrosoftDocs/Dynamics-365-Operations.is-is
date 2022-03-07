---
title: Staðsetningarforstilling leyfir ekki neikvæða birgðaskráningu en neikvæð birgðastaða er leyfð
description: Valkosturinn Leyfa neikvæða birgðir fyrir staðsetningarforstillinguna er stilltur á Nei, en kerfið leyfir samt neikvæðar birgðir.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: shawan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 2a7345281301ee70a512dfadcd553cb4eb33003904d0dddf6967659b693f60d7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742609"
---
# <a name="location-profile-disallows-negative-inventory-but-negative-on-hand-inventory-is-permitted"></a>Staðsetningarforstilling leyfir ekki neikvæða birgðaskráningu en neikvæð birgðastaða er leyfð

KB númer: 4613622

## <a name="symptoms"></a>Einkenni

Valkosturinn **Leyfa neikvæða birgðir** fyrir staðsetningarforstillinguna er stilltur á *Nei*, en kerfið leyfir samt neikvæðar birgðir.

## <a name="example-scenario"></a>Dæmi

Við færslur við opinbera aðila þarf kerfið að geta skráð neikvæðar birgðir til að bókfæra tap. Þú vilt að hlutur geti sýnt neikvæða birgðir, en aðeins á tilgreindum stöðum, svo sem geymum. Ef vörulíkanahópurinn leyfir hins vegar neikvæðar birgðir kemur í ljós að það skiptir ekki máli hvort staðsetningin er stillt til að leyfa neikvæðar birgðir. Ef varan er sett upp þannig að neikvæð birgðastaða er ekki leyfð skiptir ekki máli hvernig staðsetningarlýsingin er sett upp.

## <a name="resolution"></a>Upplausn

**Leyfa neikvæða birgðir** frá staðsetningarforstillingunni á aðeins við um vöruhúsferli, svo sem tínslu. Vörulíkanaflokkar sem eru hins vegar stilltir til að leyfa neikvæðar birgðir hafa hins vegar áhrif á öll ferli úr einingum birgðastjórnunar og lagerstjórnunar og staðsetningarforstillingin mun ekki víkja frá stillingunni.

Þú getur stýrt því hvort vöruhús megi hafa neikvæðar birgðir. Stillið vörulíkanaflokkana á að leyfa ekki neikvæðar efnislegar birgðir og stillið aðeins viðkomandi vöruhús á að leyfa neikvæðar birgðir.
