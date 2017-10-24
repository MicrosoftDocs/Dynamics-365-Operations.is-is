---
title: "Færslusniðmát"
description: "Þessi grein kynnir hugtakið skýrslusnið og útskýrir hvernig hægt er að nota þau til að stofna skýrslur sem deila upplýsingum."
author: pvillads
manager: AnnBe
ms.date: 08/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 16101
ms.assetid: 61ada2d8-84c3-44bc-b4c5-516b1aeac3d1
ms.search.region: Global
ms.author: pvillads
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e89e4a74550597a4e497a1128fe91c07e766d697
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="record-templates"></a><span data-ttu-id="ef3ac-103">Færslusniðmát</span><span class="sxs-lookup"><span data-stu-id="ef3ac-103">Record templates</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="ef3ac-104">Þessi grein kynnir hugtakið skýrslusnið og útskýrir hvernig hægt er að nota þau til að stofna skýrslur sem deila upplýsingum.</span><span class="sxs-lookup"><span data-stu-id="ef3ac-104">This article introduces the concept of record templates and explains how they can be used to create records that share information.</span></span>

<span data-ttu-id="ef3ac-105">Færslusniðmát geta hjálpað til við að stofna færslur hraðar í Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ef3ac-105">Record templates can help you to create records more quickly in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="ef3ac-106">Aðeins er hægt að stofna færslusniðmát fyrir sumar af færslugerðunum í Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ef3ac-106">You can create record templates for only some of the record types in Microsoft Dynamics 365 for Finance and Operations.</span></span> 

<span data-ttu-id="ef3ac-107">Til dæmis hugsum okkur að verið sé að færa inn upplýsingar um leigu bílaleigufyrirtækis sem er staðsett í San Francisco.</span><span class="sxs-lookup"><span data-stu-id="ef3ac-107">For example, imagine you are entering rental information for a car rental business that is located in San Francisco.</span></span> <span data-ttu-id="ef3ac-108">Þar sem flestir viðskiptavina eru líklega frá San Francisco svæðinu, væri gott ef hægt væri að fylla sjálfkrafa út gildi°fyrir°**Fylki**, **Land**, og **Borg** svæðin á leiguskjámyndinni.</span><span class="sxs-lookup"><span data-stu-id="ef3ac-108">Since most of the customers are likely to be from the San Francisco area, it would be nice if you could automatically fill in the values for the **State**, **Country**, and **City** fields on the rental form.</span></span> 

> [!Note]
> <span data-ttu-id="ef3ac-109">Aðeins er hægt að nota sniðmát fyrir þau svæði Finance and Operations sem viðkomandi hefur aðgang að.</span><span class="sxs-lookup"><span data-stu-id="ef3ac-109">You can apply templates only for the areas of Finance and Operations that you have access to.</span></span> <span data-ttu-id="ef3ac-110">Hins vegar eru öll sniðmátsheiti sýnileg öllum notendum þegar ný færsla er stofnuð, ef verið er að stofna sniðmát sem verða svo aðgengileg fyrir alla notendur.</span><span class="sxs-lookup"><span data-stu-id="ef3ac-110">However all template titles are visible to you when you create a new record, and to other users as well, if you are creating templates that will be available for all users.</span></span> <span data-ttu-id="ef3ac-111">Gætið þess að þetta í huga þegar sniðmát eru nefnd.</span><span class="sxs-lookup"><span data-stu-id="ef3ac-111">Be sure to consider this when naming templates.</span></span> <span data-ttu-id="ef3ac-112">Til dæmis ætti að forðast að nota heiti með orðum eins og „kaupauki“ ef það er trúnaðarmál að sumir starfsmenn fá greidda kaupauka.</span><span class="sxs-lookup"><span data-stu-id="ef3ac-112">For example, avoid using names that include words, such as "commission," if is confidential that some employees in the company have commission-based salaries.</span></span> 

<span data-ttu-id="ef3ac-113">Þegar eitt eða fleiri sniðmát sem viðkomandi hefur aðgang að eru til fyrir tiltekna skjámynd og reynt er að stofna nýja færslu í skjámyndinni birtist **Velja sniðmát** síðan.</span><span class="sxs-lookup"><span data-stu-id="ef3ac-113">When one or more templates that you have access to exist for a specific form and you attempt to create a new record in the form, the **Select a template for** page is displayed.</span></span> <span data-ttu-id="ef3ac-114">Þegar sniðmát er valið úr listanum er nýja færslan stofnuð og inniheldur hún sjálfgefnar upplýsingar sem eru byggðar á sniðmátinu sem valið er.</span><span class="sxs-lookup"><span data-stu-id="ef3ac-114">When you select a template from the list, the new record is created and contains default information that is based on the template that you selected.</span></span> <span data-ttu-id="ef3ac-115">Ef ekki á að nota sniðmát þegar nýjar færslur eru stofnaðar skal velja **Ekki spyrja aftur** gátreit á síðunni **Velja sniðmát fyrir**.</span><span class="sxs-lookup"><span data-stu-id="ef3ac-115">If you do not want to use templates when you create new records, select the **Do not ask again** check box in the **Select a template for** page.</span></span> <span data-ttu-id="ef3ac-116">Til að birta svargluggann fyrir sniðmátsval aftur skal hægrismella á hvaða færslu sem er, smella svo á **Færsluupplýsingar**, og svo á **Sýna sniðmátsval**.</span><span class="sxs-lookup"><span data-stu-id="ef3ac-116">To display the template selection dialog box again, right-click any record, click **Record info**, and then click **Show template selection**.</span></span>




