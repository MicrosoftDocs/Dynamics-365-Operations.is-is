---
title: Stofna þjónustupantanir sjálfkrafa
description: Þú getur búið til þjónustupantanir sem eru byggðar á þjónustusamningi fyrir gildistíma þjónustusamningsins.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0b864aee332c82bc6b6845e7f9e425cfef377033
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824631"
---
# <a name="automatically-create-service-orders"></a><span data-ttu-id="fd3b6-103">Stofna þjónustupantanir sjálfkrafa</span><span class="sxs-lookup"><span data-stu-id="fd3b6-103">Automatically create service orders</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="fd3b6-104">Þú getur búið til þjónustupantanir sem eru byggðar á þjónustusamningi fyrir gildistíma þjónustusamningsins.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-104">You can generate service orders that are based on a service agreement for the valid period of the service agreement.</span></span>

<span data-ttu-id="fd3b6-105">Þjónustupantanirnar sem þú býrð til úr þjónustusamningi eru allar tengdar við þjónustusamninginn.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-105">The service orders that you generate from a service agreement are all attached to the service agreement.</span></span>

<span data-ttu-id="fd3b6-106">Þjónustupantanir eru myndaðar sjálfkrafa samkvæmt eftirfarandi stillingum:</span><span class="sxs-lookup"><span data-stu-id="fd3b6-106">Service orders are generated automatically from the following settings:</span></span>

  - <span data-ttu-id="fd3b6-107">Þjónustusamningsbilið sem er sett upp í þjónustusamningslínunum.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-107">The service agreement interval that is set up in the service agreement lines.</span></span> <span data-ttu-id="fd3b6-108">Þjónustusamningsbilið gefur til kynna hversu oft þjónustupöntunarlínur eru búnar til.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-108">The service agreement interval indicates the frequency that service-order lines are created.</span></span> <span data-ttu-id="fd3b6-109">Nánari upplýsingar er að finna í [Þjónustutímabil](service-intervals.md).</span><span class="sxs-lookup"><span data-stu-id="fd3b6-109">For more information, see [Service intervals](service-intervals.md).</span></span>

  - <span data-ttu-id="fd3b6-110">Tímabilið sem þú tilgreinir til að skilgreina þjónustutímabilið í **Frá dagsetningu** og **Til dagsetningar** reitunum í **Búa til þjónustupantanir** skjámyndinni.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-110">The period that you specify to define the service period in the **From date** and **To date** fields in the **Create service orders** form.</span></span> <span data-ttu-id="fd3b6-111">Nánari upplýsingar er að finna í [Búa til þjónustupantanir sjálfkrafa](create-service-orders-automatically.md).</span><span class="sxs-lookup"><span data-stu-id="fd3b6-111">For more information, see [Create service orders automatically](create-service-orders-automatically.md).</span></span>

  - <span data-ttu-id="fd3b6-112">The **Sameina þjónustupantanir** valkostur á þjónustusamningnum haus.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-112">The **Combine service orders** option on the service agreement header.</span></span> <span data-ttu-id="fd3b6-113">Þessi valkostur skilgreinir hvort þjónustupöntunarlínur sem búnar eru til úr þjónustusamningi, sameinar þjónustupantanir samkvæmt starfsmanni, þjónustuverklið, þjónustuhlut eða þjónustusamningi.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-113">This option defines whether service order lines generated from a service agreement, combines service orders according to employee, service task, service object, or service agreement.</span></span> <span data-ttu-id="fd3b6-114">Nánari upplýsingar er að finna í [Sameina þjónustupantanir](combine-service-orders.md).</span><span class="sxs-lookup"><span data-stu-id="fd3b6-114">For more information, see [Combine service orders](combine-service-orders.md).</span></span>

  - <span data-ttu-id="fd3b6-115">**Tímagluggi** valkosturinn á þjónustusamningslínunni.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-115">The **Time window** option on the service agreement line.</span></span> <span data-ttu-id="fd3b6-116">Tímaglugginn skilgreinir hversu langt þjónustupöntunarlínan getur færst með tilliti til reiknaðrar dagsetningar hennar.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-116">The time window defines how far a service order line can move with regard to its calculated date.</span></span> <span data-ttu-id="fd3b6-117">Nánari upplýsingar er að finna í [Tímagluggi](time-windows.md).</span><span class="sxs-lookup"><span data-stu-id="fd3b6-117">For more information, see [Time windows](time-windows.md).</span></span>


> [!NOTE]
> <P><span data-ttu-id="fd3b6-118">Ef dagurinn sem tilgreindur er fyrir þjónustupöntun er ekki opinn í dagatalinu sem þú hefur valið í <STRONG>Færibreytur þjónustukerfis</STRONG> skjámynd, birtist skilaboð um ósamræmi í dagatali.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-118">If the day that is specified for a service order is not open in the calendar that you have selected in the <STRONG>Service management parameters</STRONG> form, a message will indicate that there is a calendar conflict.</span></span> <span data-ttu-id="fd3b6-119">Þú getur hæglega hunsað skilaboðin; þjónustupöntunin mun verða búin til, jafnvel þótt dagurinn sé lokaður á dagatalinu.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-119">You can safely ignore the message; the service order will be created, even though the day is closed on the calendar.</span></span></P>

## <a name="example-1"></a><span data-ttu-id="fd3b6-120">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="fd3b6-120">Example 1</span></span>

<span data-ttu-id="fd3b6-121">Þjónustusamningurinn stendur frá 1. janúar 2012 til 31. desember 2012.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-121">The service agreement lasts from January 1, 2012 until December 31, 2012.</span></span> <span data-ttu-id="fd3b6-122">Ef þjónustutímabilið sem þú tilgreinir í **Búa til þjónustupantanir** skjámynd er frá 1. nóvember 2012 til 1. febrúar 2013, eru þjónustupantanir búnar til frá 1. nóvember 2012 til 31. desember 2012.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-122">If the service period that you specify in the **Create service orders** form is from November 1, 2012 until February 1, 2013, service orders are created from November 1, 2012 until December 31, 2012.</span></span>

## <a name="example-2"></a><span data-ttu-id="fd3b6-123">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="fd3b6-123">Example 2</span></span>

<span data-ttu-id="fd3b6-124">Þjónustusamningurinn stendur frá 1. janúar 2012 til 31. desember 2012.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-124">The service agreement lasts from January 1, 2012 until December 31, 2012.</span></span> <span data-ttu-id="fd3b6-125">Tvær þjónustusamningslínur eru hengdar við þjónustusamninginn.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-125">Two service agreement lines are attached to the service agreement.</span></span> <span data-ttu-id="fd3b6-126">Fyrsti þjónustusamningslínan er með upphafsdagur 2. janúar 2012 og lokadagur 1. mars 2012.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-126">The first service agreement line has a starting date on January 2, 2012 and an ending date on March 1, 2012.</span></span> <span data-ttu-id="fd3b6-127">Önnur þjónustusamningslína er með upphafsdag 1. apríl 2012 og lokadagsetning 31. desember 2012.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-127">The second service agreement line has a starting date on April 1, 2012 and an ending date on December 31, 2012.</span></span> <span data-ttu-id="fd3b6-128">Þú tilgreinir tímabil í **Búa til þjónustupantanir** skjámynd sem er frá 1. október 2012 til 31. desember 2012.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-128">You specify a period in the **Create service orders** form that is from October 1, 2012 until December 31, 2012.</span></span> <span data-ttu-id="fd3b6-129">Þess vegna eru þjónustupantanir aðeins myndaðar fyrir aðra samningslínuna, vegna þess að upphafsdagur og lokadagur fyrstu samningslínunnar eru fyrir tímabilið sem þú tilgreindir fyrir þjónustupöntunina.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-129">Therefore, service orders are generated only for the second agreement line, because the starting date and ending date of the first agreement line are before the period that you specified for the service order.</span></span>

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]