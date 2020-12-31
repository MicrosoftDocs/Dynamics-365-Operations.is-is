---
title: Yfirlit sniðmátsskráningar
description: Þessi grein kynnir hugtakið skýrslusnið og útskýrir hvernig hægt er að nota þau til að stofna skýrslur sem deila upplýsingum.
author: pvillads
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 16101
ms.assetid: 61ada2d8-84c3-44bc-b4c5-516b1aeac3d1
ms.search.region: Global
ms.author: pvillads
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c0b55046e6c523398b4a30e674dc9f77bb6fedf3
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693209"
---
# <a name="record-templates-overview"></a><span data-ttu-id="94790-103">Yfirlit sniðmátsskráningar</span><span class="sxs-lookup"><span data-stu-id="94790-103">Record templates overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="94790-104">Þessi grein kynnir hugtakið skýrslusnið og útskýrir hvernig hægt er að nota þau til að stofna skýrslur sem deila upplýsingum.</span><span class="sxs-lookup"><span data-stu-id="94790-104">This article introduces the concept of record templates and explains how they can be used to create records that share information.</span></span>

<span data-ttu-id="94790-105">Skráasniðmát geta hjálpað þér að búa til færslur hraðar, en þú getur aðeins búið til skráasniðmát fyrir nokkrar skráagerðir.</span><span class="sxs-lookup"><span data-stu-id="94790-105">Record templates can help you to create records more quickly, however you can only create record templates for some record types.</span></span>

<span data-ttu-id="94790-106">Til dæmis hugsum okkur að verið sé að færa inn upplýsingar um leigu bílaleigufyrirtækis sem er staðsett í San Francisco.</span><span class="sxs-lookup"><span data-stu-id="94790-106">For example, imagine you are entering rental information for a car rental business that is located in San Francisco.</span></span> <span data-ttu-id="94790-107">Þar sem flestir viðskiptavina eru líklega frá San Francisco svæðinu, væri gott ef hægt væri að fylla sjálfkrafa út gildi fyrir **Fylki**, **Land**, og **Borg** svæðin á leiguskjámyndinni.</span><span class="sxs-lookup"><span data-stu-id="94790-107">Since most of the customers are likely to be from the San Francisco area, it would be nice if you could automatically fill in the values for the **State**, **Country**, and **City** fields on the rental form.</span></span>

> [!NOTE]
> <span data-ttu-id="94790-108">Aðeins er hægt að nota sniðmát á þeim svæðum sem viðkomandi hefur aðgang að.</span><span class="sxs-lookup"><span data-stu-id="94790-108">You can apply templates only in areas that you have access to.</span></span> <span data-ttu-id="94790-109">Hins vegar eru öll sniðmátsheiti sýnileg öllum notendum þegar ný færsla er stofnuð, ef verið er að stofna sniðmát sem verða svo aðgengileg fyrir alla notendur.</span><span class="sxs-lookup"><span data-stu-id="94790-109">However all template titles are visible to you when you create a new record, and to other users as well, if you are creating templates that will be available for all users.</span></span> <span data-ttu-id="94790-110">Gætið þess að þetta í huga þegar sniðmát eru nefnd.</span><span class="sxs-lookup"><span data-stu-id="94790-110">Be sure to consider this when naming templates.</span></span> <span data-ttu-id="94790-111">Til dæmis ætti að forðast að nota heiti með orðum eins og „kaupauki“ ef það er trúnaðarmál að sumir starfsmenn fá greidda kaupauka.</span><span class="sxs-lookup"><span data-stu-id="94790-111">For example, avoid using names that include words, such as "commission," if is confidential that some employees in the company have commission-based salaries.</span></span>

<span data-ttu-id="94790-112">Þegar eitt eða fleiri sniðmát sem viðkomandi hefur aðgang að eru til fyrir tiltekna skjámynd og reynt er að stofna nýja færslu í skjámyndinni birtist **Velja sniðmát** síðan.</span><span class="sxs-lookup"><span data-stu-id="94790-112">When one or more templates that you have access to exist for a specific form and you attempt to create a new record in the form, the **Select a template for** page is displayed.</span></span> <span data-ttu-id="94790-113">Þegar sniðmát er valið úr listanum er nýja færslan stofnuð og inniheldur hún sjálfgefnar upplýsingar sem eru byggðar á sniðmátinu sem valið er.</span><span class="sxs-lookup"><span data-stu-id="94790-113">When you select a template from the list, the new record is created and contains default information that is based on the template that you selected.</span></span> <span data-ttu-id="94790-114">Ef ekki á að nota sniðmát þegar nýjar færslur eru stofnaðar skal velja **Ekki spyrja aftur** gátreit á síðunni **Velja sniðmát fyrir**.</span><span class="sxs-lookup"><span data-stu-id="94790-114">If you do not want to use templates when you create new records, select the **Do not ask again** check box in the **Select a template for** page.</span></span> <span data-ttu-id="94790-115">Til að birta svargluggann fyrir sniðmátsval aftur skal hægrismella á hvaða færslu sem er, smella svo á **Færsluupplýsingar**, og svo á **Sýna sniðmátsval**.</span><span class="sxs-lookup"><span data-stu-id="94790-115">To display the template selection dialog box again, right-click any record, click **Record info**, and then click **Show template selection**.</span></span>
