---
title: Afturkalla stillingar á færslubókum og línum
description: Í þessu efnisatriði er útskýrt hvers vegna bakfærsla sem færð var inn í almenna færslubók er hugsanlega ekki höfð með í bókuðu færslunni.
author: kweekley
ms.date: 04/29/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-5-05
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 74020f6fc9b0fa8e05a1e2a09fd13dcd60490dc0
ms.sourcegitcommit: 817716c2e96f24af0ef1d7d5323afdeccdc602f3
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/13/2021
ms.locfileid: "6028568"
---
# <a name="reverse-settings-on-journals-and-lines"></a><span data-ttu-id="2024d-103">Afturkalla stillingar á færslubókum og línum</span><span class="sxs-lookup"><span data-stu-id="2024d-103">Reverse settings on journals and lines</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2024d-104">Í þessu efnisatriði er útskýrt hvers vegna bakfærsla sem færð var inn í almenna færslubók er hugsanlega ekki höfð með í bókuðu færslunni.</span><span class="sxs-lookup"><span data-stu-id="2024d-104">This topic addresses why a reversing entry that was entered on a general journal might not be included on the posted transaction.</span></span>  

## <a name="symptom"></a><span data-ttu-id="2024d-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="2024d-105">Symptom</span></span>

<span data-ttu-id="2024d-106">Almenn færslubók inniheldur bakfærslu og dagsetningu hennar í færslubókinni.</span><span class="sxs-lookup"><span data-stu-id="2024d-106">A general journal includes a reversing entry and reversing date on the journal.</span></span> <span data-ttu-id="2024d-107">Þegar þú bókar dagbókina er ekkert fylgiskjal bakfært.</span><span class="sxs-lookup"><span data-stu-id="2024d-107">When you post the journal, none of the vouchers are reversed.</span></span> <span data-ttu-id="2024d-108">Af hverju gerist þetta?</span><span class="sxs-lookup"><span data-stu-id="2024d-108">Why does this happen?</span></span>

## <a name="resolution"></a><span data-ttu-id="2024d-109">Lausn</span><span class="sxs-lookup"><span data-stu-id="2024d-109">Resolution</span></span>

<span data-ttu-id="2024d-110">Þegar færslubókin er bókuð skoðar bakfærsluferlið eingöngu stillingar **Bakfærslu** og **Dags. bakfærslu** í hlutanum **Línur** í fylgiskjalinu.</span><span class="sxs-lookup"><span data-stu-id="2024d-110">When the journal is posted, the reversing process looks only at the **Revering entry** and **Reversing date** settings on the **Lines** section of the voucher.</span></span> <span data-ttu-id="2024d-111">Þessi aðferð gerir færslubók kleift að hafa með sum fylgiskjöl sem eru merkt fyrir bakfærslu og önnur ekki.</span><span class="sxs-lookup"><span data-stu-id="2024d-111">This approach allows a journal to include some vouchers that are marked for reversing, and others that are not.</span></span>

<span data-ttu-id="2024d-112">Gildin úr færslubókinni eru aðeins notuð sem sjálfgefin gildi þegar *nýjum* línum er bætt við.</span><span class="sxs-lookup"><span data-stu-id="2024d-112">The values from the journal are only used as defaults when adding *new* lines.</span></span> <span data-ttu-id="2024d-113">Breyting á gildum í færslubókinni hefur ekki áhrif á línur sem eru til staðar.</span><span class="sxs-lookup"><span data-stu-id="2024d-113">Changing the values on the journal doesn’t affect existing lines.</span></span> <span data-ttu-id="2024d-114">Í þessu dæmi voru línur afsláttarkóðans slegnar inn fyrst.</span><span class="sxs-lookup"><span data-stu-id="2024d-114">In this example, the voucher lines were entered first.</span></span> <span data-ttu-id="2024d-115">Þegar þú slærð inn línuupplýsingarnar áður en þú tilgreinir færslubókina sem bakfærslu, verður merking hennar sem bakfærslu og dagsetningu bakfærslu ekki notuð í neinum línum sem eru til staðar.</span><span class="sxs-lookup"><span data-stu-id="2024d-115">When you enter the line detail before designating the journal as reversing, the designation as a reversing entry and date won't be applied to any existing lines.</span></span>

<span data-ttu-id="2024d-116">Ef bakfærslunni eða dagsetningu bakfærslunnar er breytt í fyrirliggjandi línu mun sú breyting koma fram í öðrum línum í sama fylgiskjalinu.</span><span class="sxs-lookup"><span data-stu-id="2024d-116">Changing the reversing entry or reversing date on an existing line propagates that change to other lines in the same voucher.</span></span> <span data-ttu-id="2024d-117">Til að hámarka afköst er netið ekki uppfært eftir að breytingar hafa verið færðar yfir á aðrar línur.</span><span class="sxs-lookup"><span data-stu-id="2024d-117">To optimize performance, the grid is not refreshed after propagating changes to other Lines.</span></span> <span data-ttu-id="2024d-118">Hægt er að birta uppfærð gildi með því að endurhlaða hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="2024d-118">You can display the updated values by refreshing the grid.</span></span>


