---
title: Aðeins eitt merki er prentað fyrir marga vinnuhausa í einni innhreyfingu
description: Aðeins eitt merki er prentað fyrir marga vinnuhausa í einni innhreyfingu
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLicensePlateLabel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 8e11dc918eb3c9085018d15b43819522cc8bebe3
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026608"
---
# <a name="only-one-label-is-printed-for-multiple-work-headers-on-a-single-receipt"></a><span data-ttu-id="3fbc2-103">Aðeins eitt merki er prentað fyrir marga vinnuhausa í einni innhreyfingu</span><span class="sxs-lookup"><span data-stu-id="3fbc2-103">Only one label is printed for multiple work headers on a single receipt</span></span>

<span data-ttu-id="3fbc2-104">KB númer: 4614667</span><span class="sxs-lookup"><span data-stu-id="3fbc2-104">KB number: 4614667</span></span>

## <a name="symptoms"></a><span data-ttu-id="3fbc2-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="3fbc2-105">Symptoms</span></span>

<span data-ttu-id="3fbc2-106">Fjölmargir vinnuhausar eru stofnaðir fyrir sömu markanúmeraplötu sem hluti af einu vöruhúsaforriti sem tekur á móti viðburði.</span><span class="sxs-lookup"><span data-stu-id="3fbc2-106">Multiple work headers are created for the same target license plate as part of a single warehouse app receiving event.</span></span> <span data-ttu-id="3fbc2-107">Hins vegar er aðeins prentað eitt númeraplötumerki þegar varan berst.</span><span class="sxs-lookup"><span data-stu-id="3fbc2-107">However, only one license plate label is printed when the product is received.</span></span>

## <a name="resolution"></a><span data-ttu-id="3fbc2-108">Upplausn</span><span class="sxs-lookup"><span data-stu-id="3fbc2-108">Resolution</span></span>

<span data-ttu-id="3fbc2-109">Kerfið hagar sér eins og það er hannað.</span><span class="sxs-lookup"><span data-stu-id="3fbc2-109">The system is behaving as designed.</span></span>

<span data-ttu-id="3fbc2-110">Í núverandi hönnun er ávallt myndaður stakur merkimiði á númeraplötunni, burtséð frá fjölda vinnuhausa og vinnulínusamsetninga sem eru til staðar.</span><span class="sxs-lookup"><span data-stu-id="3fbc2-110">In the current design, a single license plate label is always generated, regardless of the number of work header and work line combinations that exist.</span></span> <span data-ttu-id="3fbc2-111">Merkið sem myndast inniheldur aðeins upplýsingar um eina samsetningu.</span><span class="sxs-lookup"><span data-stu-id="3fbc2-111">The generated label includes the information for only one combination.</span></span>

<span data-ttu-id="3fbc2-112">Til að vinna í kringum þetta vandamál þarf að ganga úr skugga um að myndun vinnuhauss sé ávallt varpað á aðeins eina marknúmeraplötu.</span><span class="sxs-lookup"><span data-stu-id="3fbc2-112">To work around this issue, make sure that work header creation is always mapped to just one target license plate.</span></span>
