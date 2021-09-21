---
title: Sjálfgefinn skattflokkur og staðgreiðsluafsláttur eru ekki fyllt út í reikningslyklinum
description: Sjálfgefinn skattflokkur og sjálfgefinn staðgreiðsluafsláttur eru ekki fyllt út í reikningslyklinum
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: bb984eb17209dc92e336df5ad475bb0f70c6e35c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476653"
---
# <a name="default-tax-group-and-cash-discount-arent-filled-in-from-the-invoice-account"></a>Sjálfgefinn skattflokkur og staðgreiðsluafsláttur eru ekki fyllt út í reikningslyklinum

## <a name="symptoms"></a>Einkenni

Ef reikningslykill er notaður sem er frábrugðinn lykli viðskiptavinar, er ekki fyllt út í sjálfgefinn skattflokk og sjálfgefinn staðgreiðsluafslátt í reikningslyklinum þegar innkaupapöntun er búin til.

## <a name="resolution"></a>Lausn

Þessi hegðun er samkvæmt hönnuninni. Sjálfgefin gildi fyrir skattflokkinn, staðgreiðsluafslætti og aðrar verðupplýsingar byggja á viðskiptavinalyklinum, ekki reikningslyklinum.
