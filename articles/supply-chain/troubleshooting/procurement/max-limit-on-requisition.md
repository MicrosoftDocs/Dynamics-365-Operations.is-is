---
title: Hámarkið í innkaupasamningi gildir ekki í innkaupabeiðni
description: Hámarkið í innkaupasamningi gildir ekki í innkaupabeiðni
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
ms.openlocfilehash: c19d40dce65acbe80d4572bfc4e925aa87ea4f02
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476638"
---
# <a name="the-purchase-agreement-maximum-limit-isnt-effective-on-a-purchase-requisition"></a>Hámarkið í innkaupasamningi gildir ekki í innkaupabeiðni

## <a name="symptoms"></a>Einkenni

Þegar innkaupabeiðni er tengd við innkaupasamning er hámarkið samkvæmt innkaupasamningi ekki virkt í innkaupabeiðninni. Sjálfgefnar upplýsingar um verð eru slegnar inn á réttan hátt en hægt er að panta meira en hámarkið samkvæmt innkaupasamningi í innkaupabeiðninni.

## <a name="resolution"></a>Lausn

Búist er við þessari hegðun. Vegna þess að beiðnir eru ekki alltaf samþykktar ætti magn eða upphæð ekki að vera geymt í innkaupasamningi. Þess vegna er ekki hægt að uppfylla hámarkið í innkaupasamningnum.
