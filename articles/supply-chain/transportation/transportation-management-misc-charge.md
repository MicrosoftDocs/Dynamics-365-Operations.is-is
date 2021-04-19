---
title: Ýmis gjöld flutningsstjórnunar
description: Þetta efnisatriði útskýrir hvernig gjöld sem myndast vegna flutninga verða að vera tengd við gjaldakóða.
author: Henrikan
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 53c25f204e98a911e9697f5bb950706555749a55
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828318"
---
# <a name="transportation-management-miscellaneous-charges"></a><span data-ttu-id="6c0fa-103">Ýmis gjöld flutningsstjórnunar</span><span class="sxs-lookup"><span data-stu-id="6c0fa-103">Transportation management miscellaneous charges</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6c0fa-104">Eins og á við um öll gjöld verða flutningsgjöld að vera tengd við gjaldakóða.</span><span class="sxs-lookup"><span data-stu-id="6c0fa-104">As with all miscellaneous charges, transportation-generated charges must be associated with a charge code.</span></span> <span data-ttu-id="6c0fa-105">Að öðrum kosti verður þeim ekki bætt við aftur í pöntunina sem gjald.</span><span class="sxs-lookup"><span data-stu-id="6c0fa-105">Otherwise, they won't be added back to the order as a miscellaneous charge.</span></span> <span data-ttu-id="6c0fa-106">**Gjaldakóði** ákvarðar hvernig gjöldin eru gjaldfærð í tengslum við pöntun og pöntunarlínuna þar sem honum er bætt við.</span><span class="sxs-lookup"><span data-stu-id="6c0fa-106">The **Charges code** determines how the charge is accounted for in relation to the order and order line where it is added.</span></span>

<span data-ttu-id="6c0fa-107">Opnaðu **Flutningsstjórnun > Uppsetning > Flokkun > Ýmis gjöld** til að skilgreina flokkunarskilyrðin sem ákvarða hvenær tiltekinn **Gjaldakóði** er notaður fyrir gjald.</span><span class="sxs-lookup"><span data-stu-id="6c0fa-107">Go to **Transportation management > Setup > Rating > Miscellaneous charges** to define the qualifying criteria that determine when a specific **Charges code** is applied to a charge.</span></span>

<span data-ttu-id="6c0fa-108">Þú ættir að hafa að minnsta kosti eina uppsetningu fyrir hverja viðeigandi stillingu **Gjaldaeiningar** (*Viðskiptavinur* og *Lánardrottinn*) þar sem **Gerð ýmissa gjalda** er stillt á *Engin*.</span><span class="sxs-lookup"><span data-stu-id="6c0fa-108">You should have at least one setup for each relevant **Charges module** setting (*Customer* and *Vendor*) where the **Miscellaneous charge type** is set to *None*.</span></span> <span data-ttu-id="6c0fa-109">Ef þetta vantar verður gjaldinu *ekki* bætt við pöntunina.</span><span class="sxs-lookup"><span data-stu-id="6c0fa-109">If this is missing, the miscellaneous charge will *not* be added to the order.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]