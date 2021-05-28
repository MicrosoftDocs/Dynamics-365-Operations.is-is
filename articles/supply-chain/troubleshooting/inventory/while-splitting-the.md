---
title: Þegar framleiðsluþyngdum er skipt er lágmarksmagn notað í staðinn fyrir nafnmagn
description: Þegar framleiðsluþyngdum er skipt í lotur notar reiturinn Velja magn lágmarksmagnið sem er stillt fyrir vöruna en ekki nafnmagnið.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 185365ced5c4516d8fcdbdca88794d0078615888
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026618"
---
# <a name="when-a-catch-weight-quantity-is-split-minimum-quantity-is-used-instead-of-nominal-quantity"></a><span data-ttu-id="80154-103">Þegar framleiðsluþyngdum er skipt er lágmarksmagn notað í staðinn fyrir nafnmagn</span><span class="sxs-lookup"><span data-stu-id="80154-103">When a catch-weight quantity is split, minimum quantity is used instead of nominal quantity</span></span>

<span data-ttu-id="80154-104">KB númer: 4612073</span><span class="sxs-lookup"><span data-stu-id="80154-104">KB number: 4612073</span></span>

## <a name="symptoms"></a><span data-ttu-id="80154-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="80154-105">Symptoms</span></span>

<span data-ttu-id="80154-106">Þegar framleiðsluþyngdum er skipt í lotur notar reiturinn **Velja magn** lágmarksmagnið sem er stillt fyrir vöruna en ekki nafnmagnið.</span><span class="sxs-lookup"><span data-stu-id="80154-106">When a catch-weight quantity is being split into batches, the **Pick qty** field uses the minimum quantity that is set for the item, not the nominal quantity.</span></span>

## <a name="resolution"></a><span data-ttu-id="80154-107">Upplausn</span><span class="sxs-lookup"><span data-stu-id="80154-107">Resolution</span></span>

<span data-ttu-id="80154-108">Kerfið hagar sér eins og það er hannað.</span><span class="sxs-lookup"><span data-stu-id="80154-108">The system is behaving as designed.</span></span> <span data-ttu-id="80154-109">Kerfið notar uppsetningu lágmarksmagns hvers hlutar til að velja.</span><span class="sxs-lookup"><span data-stu-id="80154-109">The system uses each item's minimum quantity setup for picking.</span></span>
