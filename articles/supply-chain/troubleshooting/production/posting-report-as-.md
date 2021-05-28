---
title: Villa þegar Bóka sem tilbúið færslubók er bókuð.
description: Þegar bókað er í færslubókina Tilkynna sem lokið birtast villuboð þar sem fram kemur að ekki sé hægt að minnka pantað magn.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTableListPage, ProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 55db7d0033dd66c1b973abf96671a20ab05d61d8
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026598"
---
# <a name="error-when-the-report-as-finished-journal-is-posted"></a><span data-ttu-id="90da6-103">Villa þegar Bóka sem tilbúið færslubók er bókuð.</span><span class="sxs-lookup"><span data-stu-id="90da6-103">Error when the Report as finished journal is posted</span></span>

<span data-ttu-id="90da6-104">KB númer: 4612891</span><span class="sxs-lookup"><span data-stu-id="90da6-104">KB number: 4612891</span></span>

## <a name="symptoms"></a><span data-ttu-id="90da6-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="90da6-105">Symptoms</span></span>

<span data-ttu-id="90da6-106">Villa kemur upp þegar dagbókin **Tilkynna sem lokið** er bókuð og eftirfarandi villuboð munu berast:</span><span class="sxs-lookup"><span data-stu-id="90da6-106">When you post the **Report as finished** journal, an error occurs, and you receive the following error message:</span></span>

> <span data-ttu-id="90da6-107">Ekki er hægt að minnka pantað magn því ekki eru nógu margar opnar birgðafærslur með stöðu pöntunar.</span><span class="sxs-lookup"><span data-stu-id="90da6-107">Quantity ordered cannot be reduced because there are not enough open inventory transactions with the ordered status.</span></span> <span data-ttu-id="90da6-108">Vörurnar eru keyptar, mótteknar eða skráðar.</span><span class="sxs-lookup"><span data-stu-id="90da6-108">The items are Purchased, Received or Registered.</span></span>

<span data-ttu-id="90da6-109">Þessi villa á sér aðeins stað þegar reiturinn **Gallað magn** er stilltur á fyrstu línu færslubókarinnar **Tilkynna sem lokið** og reiturinn **Gallalaust magn** er stilltur á síðustu línu.</span><span class="sxs-lookup"><span data-stu-id="90da6-109">This error occurs only when the **Error quantity** field is set on the first line of the **Report as finished** journal, and the **Good quantity** field is set on the last line.</span></span> <span data-ttu-id="90da6-110">Ef reiturinn **Gallað magn** er stilltur á síðustu línu kemur engin villa upp.</span><span class="sxs-lookup"><span data-stu-id="90da6-110">If the **Error quantity** field is set on the last line, no error occurs.</span></span>

## <a name="resolution"></a><span data-ttu-id="90da6-111">Upplausn</span><span class="sxs-lookup"><span data-stu-id="90da6-111">Resolution</span></span>

<span data-ttu-id="90da6-112">Til að koma í veg fyrir þessa villu skal opna síðuna **færibreytur Framleiðslustýringar** og síðan, á flipanum **Almennt**, stilla valkostinn **Auka eftirstandandi magn með villumagni** valkostinn á *Já*.</span><span class="sxs-lookup"><span data-stu-id="90da6-112">To prevent this error, open the **Production control parameters** page, and then, on the **General** tab, set the **Increase remain qty with error qty** option to *Yes*.</span></span>
