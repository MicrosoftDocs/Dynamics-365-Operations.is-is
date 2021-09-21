---
title: Einingaverð á innkaupapöntunum eru ekki reiknuð út á grundvelli umreiknings einingar
description: Einingaverð á innkaupapöntunum eru ekki reiknuð út á grundvelli umreiknings einingar
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
ms.openlocfilehash: 4695f4661c3abb8ab38e3ca74b513e8529e37d20
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476655"
---
# <a name="unit-prices-on-purchase-orders-arent-calculated-based-on-the-unit-conversion"></a>Einingaverð á innkaupapöntunum eru ekki reiknuð út á grundvelli umreiknings einingar

## <a name="symptoms"></a>Einkenni

Þegar einingu er breytt í innkaupapöntun eru verð verðsamnings ekki endurreiknuð samkvæmt skilgreiningum einingaumreiknings.

## <a name="cause"></a>Orsök

Verð eru alltaf fengin úr verðsamningum (eða öðrum verðstillingum í kerfinu, svo sem sölusamningum eða vöruverði) og þeir eru stilltir fyrir einingu.

Ef einingunni er breytt í pöntunarlínu, leitar kerfið að verði fyrir nýju eininguna og notar það verð. Ef ekkert verð finnst fyrir eininguna setur kerfið ekki verð á. Ekki er hægt að nota umreikning einingar til að endurreikna verðið í aðra einingu. Fræðilega séð er verðið fyrir einn kassa af tíu ekki endilega jafnt og tífalt verðið á einum kassa.

## <a name="workaround"></a>Hjáleið

Ein leið framhjá þessu vandamáli er að ganga úr skugga um til séu verðsamningar fyrir einingarnar sem búist er við að verði notaðar í pöntunarlínum fyrir vöruna.
