---
title: Skilyrði verðsamnings eru ekki notuð á innfluttar pöntunarlínur
description: Verð og afslættir verðsamninga eru ekki notuð á sölu-eða innkaupapöntunarlínum sem eru fluttar inn í gegnum gagnastjórnun
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: fef38819efaff2f2a927cf09fc7f469490149574
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476688"
---
# <a name="trade-agreement-conditions-arent-applied-to-imported-order-lines"></a>Skilyrði verðsamnings eru ekki notuð á innfluttar pöntunarlínur

## <a name="symptoms"></a>Einkenni

Verðsamningar sem eiga við um sölu- og innkaupapöntunarlínur eru ekki notaðir í línum sem eru fluttar inn í gegnum gagnastjórnun. Hins vegar eru notaðir sömu verðsamningar á sölu- eða innkaupapöntunarlínum sem eru búnar til handvirkt.

## <a name="cause"></a>Orsök

Ef innkaupapöntunarlínur sem eru fluttar inn gegnum gagnastjórnun innihalda þegar verðupplýsingar, verður verðsamningurinn ekki endurmetinn fyrir þessar línur. Til dæmis, ef **Prósenta línuafsláttar** eða eitthvert gildi fyrir verð eða afslátt er sett inn í línu, þá verða verðsamningar ekki skoðaðir fyrir þessa línu.

## <a name="workaround"></a>Hjáleið

Búist er við þessari hegðun og hún er svipuð bæði fyrir sölupantanir og innkaupapantanir.

Leið framhjá þessu er að flytja inn innkaupapöntunarlínurnar án þess að setja inn neinar verðupplýsingar. Verðsamningarnir verða þá notaðir og innkaupapöntunarlínurnar verða uppfærðar á grundvelli skilgreindra verðsamninga.
