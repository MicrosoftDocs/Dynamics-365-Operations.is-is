---
title: Búntvara er ekki studd í ferli innan samstæðu
description: Búntvaran er ekki í boði fyrir innkaup. Sölupöntunin kaupir aðeins hluti búntvörunnar en ekki sjálfa búntvöruna.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 21adc7d071837b762157364f6f8ed370c69c7fd3
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476662"
---
# <a name="a-bundle-item-isnt-supported-in-an-intercompany-process"></a>Búntvara er ekki studd í samstæðuferli

## <a name="symptoms"></a>Einkenni

Búntvaran er ekki tiltæk fyrir innkaupapöntunina því að ef þú skoðar sölupöntunarlínurnar fyrir búntvöruna muntu taka eftir því að magnið er *0* (núll) og staðan er *Afturkölluð*.

## <a name="resolution"></a>Lausn

Þessi hegðun er samkvæmt hönnuninni. Sölupöntunin kaupir aðeins þætti búntvörunnar. Hún kaupir ekki búntvöruna sjálfa. Ef kaupa þarf búnt, þarf að hafa í huga hvort merkja eigi það sem búntvöru, þar sem þessi virkni er hönnuð fyrir aðstæður tekjuskráningar. Frekari upplýsingar um búntvörur er að finna í [Búnt](/dynamics365/finance/accounts-receivable/revenue-recognition-setup).
