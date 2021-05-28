---
title: Þú getur ekki notað sniðmát á útgefna vöru
description: Þú getur ekki notað sniðmát á útgefna vöru.
author: t-benebo
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1ad6efdced9bce924fbf5bc207c92fa2c3a6c79d
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026602"
---
# <a name="you-cant-apply-a-template-to-create-a-released-product"></a><span data-ttu-id="1a62b-103">Þú getur ekki notað sniðmát til að búa til útgefna vöru</span><span class="sxs-lookup"><span data-stu-id="1a62b-103">You can't apply a template to create a released product</span></span>

<span data-ttu-id="1a62b-104">KB númer: 4612097</span><span class="sxs-lookup"><span data-stu-id="1a62b-104">KB number: 4612097</span></span>

## <a name="symptoms"></a><span data-ttu-id="1a62b-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="1a62b-105">Symptoms</span></span>

<span data-ttu-id="1a62b-106">Þegar ný útgefin vara er stofnuð með því að nota gluggann **Ný útgefin afurð** er hægt að velja sniðmát.</span><span class="sxs-lookup"><span data-stu-id="1a62b-106">When you create a new released product by using the **New released product** dialog box, you can select a template.</span></span> <span data-ttu-id="1a62b-107">Sniðmátið á að gefa sjálfgefnar stillingar fyrir marga reiti í nýju útgefnu vörunni.</span><span class="sxs-lookup"><span data-stu-id="1a62b-107">The template is supposed to provide default settings for many fields of the new released product.</span></span> <span data-ttu-id="1a62b-108">Sumir eða allir reitir eru þó ekki stilltir eftir að sniðmátið er valið.</span><span class="sxs-lookup"><span data-stu-id="1a62b-108">However, some or all of the fields aren't set after you select the template.</span></span>

## <a name="cause"></a><span data-ttu-id="1a62b-109">Orsök</span><span class="sxs-lookup"><span data-stu-id="1a62b-109">Cause</span></span>

<span data-ttu-id="1a62b-110">Margar í Microsoft Dynamics 365 Supply Chain Management gera notendum kleift að stofna sniðmát sem setur upphafsstillingar fyrir færslurnar sem eru sýndar á þeim síðum.</span><span class="sxs-lookup"><span data-stu-id="1a62b-110">Many pages in Microsoft Dynamics 365 Supply Chain Management let you create a template that establishes initial settings for the records that are shown on those pages.</span></span> <span data-ttu-id="1a62b-111">Hægt er að stofna eitt af þessum sniðmátum með því að velja **Færsluupplýsingar** í flipanum **Valkostir** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="1a62b-111">You can create one of these templates by selecting **Record info** on the **Options** tab of the Action Pane.</span></span> <span data-ttu-id="1a62b-112">Hins vegar eru útgefnar vörur mun flóknari en flestar aðrar gerðir færslna.</span><span class="sxs-lookup"><span data-stu-id="1a62b-112">However, released products are much more complex than most other types of records.</span></span> <span data-ttu-id="1a62b-113">Þó að hægt sé að velja **Skráningarupplýsingar** á síðunni **Útgefinar vörur** til að stofna sniðmát, og þó hægt sé að velja það sniðmát þegar útgefin vara er stofnuð, mun sniðmátið ekki veita væntanleg reitargildi fyrir nýju útgefnu vöruna.</span><span class="sxs-lookup"><span data-stu-id="1a62b-113">Although you can select **Record info** on the **Released products** page to create a template, and although you can select that template when you create a released product, the template won't provide the expected field values for the new released product.</span></span> <span data-ttu-id="1a62b-114">Því er ekki hægt að nota sniðmát fyrir „skráningarupplýsingar“ fyrir útgefnar vörur.</span><span class="sxs-lookup"><span data-stu-id="1a62b-114">Therefore, you can't use "record info" templates for released products.</span></span> <span data-ttu-id="1a62b-115">Þess í stað verður að stofna sérstök vörusniðmát.</span><span class="sxs-lookup"><span data-stu-id="1a62b-115">Instead, you must create dedicated product templates.</span></span>

## <a name="resolution"></a><span data-ttu-id="1a62b-116">Upplausn</span><span class="sxs-lookup"><span data-stu-id="1a62b-116">Resolution</span></span>

<span data-ttu-id="1a62b-117">Til að búa til sniðmát vöru skal nota valmyndina **Sniðmát** á flipanum **Vara** á aðgerðasvæði, ekki hnappinn **Skrá upplýsingar** á flipanum **Valkostir**.</span><span class="sxs-lookup"><span data-stu-id="1a62b-117">To create a product template, use the **Template** menu on the **Product** tab of the Action Pane, not the **Record info** button on the **Options** tab.</span></span>

1. <span data-ttu-id="1a62b-118">Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="1a62b-118">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="1a62b-119">Á aðgerðasvæðinu, í flipanum **Afurð**, í flokknum **Nýtt**, skal velja **Sniðmát** og velja svo **Búa til persónulegt sniðmát** eða **Stofna samnýtt sniðmát** eftir því sem við á.</span><span class="sxs-lookup"><span data-stu-id="1a62b-119">On the Action Pane, on the **Product** tab, in the **New** group, select **Template**, and then select either **Create personal template** or **Create shared template**, as appropriate.</span></span>
