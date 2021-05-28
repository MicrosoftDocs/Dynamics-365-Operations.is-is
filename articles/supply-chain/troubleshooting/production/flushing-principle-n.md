---
title: Ekki er farið eftir stillingum losunarreglu í uppskriftarlínum
description: Ekki er farið eftir stillingum losunarreglu í uppskriftarlínum
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PurchTable,ProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 84a84728016119a2a02f59f6903171afbceb48e7
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026611"
---
# <a name="flushing-principle-settings-on-bom-lines-arent-respected"></a><span data-ttu-id="65106-103">Ekki er farið eftir stillingum losunarreglu í uppskriftarlínum</span><span class="sxs-lookup"><span data-stu-id="65106-103">Flushing principle settings on BOM lines aren't respected</span></span>

<span data-ttu-id="65106-104">KB númer: 4612725</span><span class="sxs-lookup"><span data-stu-id="65106-104">KB number: 4612725</span></span>

## <a name="symptoms"></a><span data-ttu-id="65106-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="65106-105">Symptoms</span></span>

<span data-ttu-id="65106-106">Þetta vandamál kemur upp þegar reiturinn **Sjálfvirk uppskriftanotkun** á flipanum **Sjálfvirk uppfærsla** á síðunni **Færibreytur framleiðslustýringar** er stilltur á *Losunarregla*.</span><span class="sxs-lookup"><span data-stu-id="65106-106">This issue occurs when the **Automatic BOM consumption** field on the **Automatic update** tab of the **Production control parameters** page is set to *Flushing principle*.</span></span> <span data-ttu-id="65106-107">Þessi stilling gefur til kynna að allar uppskriftalínur skuli sjálfkrafa notast þegar innkaupapöntun berst.</span><span class="sxs-lookup"><span data-stu-id="65106-107">This setting indicates that all bill of materials (BOM) lines should automatically be consumed when a purchase order is received.</span></span> <span data-ttu-id="65106-108">Ef reiturinn **Losunarregla** á uppskriftarlínur er sérstaklega stilltur á *Handvirkt* má búast við að uppskriftarlínurnar verði ekki notaðar sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="65106-108">If the **Flushing principle** field on BOM lines is explicitly set to *Manual*, you might expect that the BOM lines won't automatically be consumed.</span></span> <span data-ttu-id="65106-109">Þegar þetta vandamál kemur eru uppskriftarlínur þar sem reiturinn **Losunarregla** er stilltur á *Handvirkt* samt notaðar.</span><span class="sxs-lookup"><span data-stu-id="65106-109">However, when this issue occurs, BOM lines where the **Flushing principle** field is set to *Manual* are automatically consumed anyway.</span></span>

## <a name="resolution"></a><span data-ttu-id="65106-110">Upplausn</span><span class="sxs-lookup"><span data-stu-id="65106-110">Resolution</span></span>

<span data-ttu-id="65106-111">Ef vandamálið kemur upp gæti verið að breytur fyrir framleiðslustjórnun séu settar upp til að víkja frá stillingu **Losunarreglu** á uppskriftarlínur.</span><span class="sxs-lookup"><span data-stu-id="65106-111">If you're experiencing this issue, your production control parameters might be set up to override the **Flushing principle** setting on BOM lines.</span></span> <span data-ttu-id="65106-112">Á síðunni **færibreytur Framleiðslustýringar**, á flipanum **Sjálfvirk uppfærsla**, skal athuga gildið í reitnum **Sjálfvirk uppskriftarnotkun**.</span><span class="sxs-lookup"><span data-stu-id="65106-112">On the **Production control parameters** page, on the **Automatic update** tab, check the value of the **Automatic BOM consumption** field.</span></span> <span data-ttu-id="65106-113">Ef það er stillt á *Alltaf* mun kerfið líta framhjá stillingu **Losunarregla** á öllum uppskriftarlínu og mun alltaf losa línurnar.</span><span class="sxs-lookup"><span data-stu-id="65106-113">If it's set to *Always*, the system will disregard the **Flushing principle** setting on all BOM lines and will always flush the lines.</span></span> <span data-ttu-id="65106-114">Til að láta kerfið virða **Losunarregla** á uppskriftarlínum er gildinu í reitnum **Sjálfvirk uppskriftanotkun** breytt í *Losunarregla*.</span><span class="sxs-lookup"><span data-stu-id="65106-114">To make the system respect the **Flushing principle** setting on BOM lines, change the value of the **Automatic BOM consumption** field to *Flushing principle*.</span></span>
