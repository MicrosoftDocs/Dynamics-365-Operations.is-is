---
title: Ekki var hægt að gefa út sölupöntun með vöruhúsavinnslum á útleið
description: Nokkrar ástæður geta verið fyrir villuskilaboðum um að ekki hafi verið hægt að losa sölupöntun. Á þessari síðu er útskýrt hvers vegna og hvernig draga má úr vandamálinu.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: fca5ee1bc97545ea4de56d940fdedd320a6cfe84
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476675"
---
# <a name="sales-order-could-not-be-released-with-outbound-warehouse-operations"></a>Ekki var hægt að losa sölupöntun með vöruhúsaaðgerðum á útleið

## <a name="symptoms"></a>Einkenni

Þegar unnið er með vöruhúsaaðgerðir á útleið gætir þú fengið eftirfarandi villuboð:

> Ekki var hægt að losa sölupöntun.

## <a name="cause"></a>Orsök

Þetta vandamál getur komið upp af ýmsum ástæðum. Til dæmis, pöntunin er í lánastýringarbið og ekki er hægt að stofna sendingar fyrr en gilt póstfang er fært inn fyrir allar sölulínur sem tengjast pöntun. Að öðrum kosti er pöntunarbið sem þarf að leysa áður en hægt er að losa pöntunina í vöruhúsið. Þessi bið gæti verið bundin við pöntunina eða hún kann að vera á viðskiptavinalykli.

## <a name="resolution"></a>Lausn

Bæta við eða uppfæra aðsetur á sölupöntunum og pöntunarlínunum og losa svo pöntunina í vöruhúsið. Aðeins er hægt að losa pantanir í vöruhúsið ef þær hafa gilt afhendingaraðsetur (samkvæmt uppsetningu á sniði aðseturs í einingunni **Fyrirtækisstjórnun**).

Rannsaka pöntun í bið og leysa vandamálið. Taktu síðan biðina af pöntuninni eða viðskiptavininum og losaðu pöntunina í vöruhúsið.
