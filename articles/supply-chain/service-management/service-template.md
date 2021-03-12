---
title: Þjónustusniðmát
description: Hægt er að skilgreina þjónustusamning sem sniðmát og síðar afritað línur sniðmátsins í annan þjónustusamning eða þjónustupöntun.
author: ShylaThompson
manager: tfehr
ms.date: 02/19/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3e1353b3576270e9f0c202b85628fae4f49c882f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974286"
---
# <a name="service-templates"></a><span data-ttu-id="a855a-103">Þjónustusniðmát</span><span class="sxs-lookup"><span data-stu-id="a855a-103">Service templates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a855a-104">Hægt er að skilgreina þjónustusamning sem sniðmát og síðar afritað línur sniðmátsins í annan þjónustusamning eða þjónustupöntun.</span><span class="sxs-lookup"><span data-stu-id="a855a-104">You can define a service agreement as a template and copy the lines of the template later into another service agreement or into a service order.</span></span>

## <a name="example"></a><span data-ttu-id="a855a-105">Dæmi</span><span class="sxs-lookup"><span data-stu-id="a855a-105">Example</span></span>

<span data-ttu-id="a855a-106">Viðskiptavinur, sem fyrirtækið veitir þjónustu, er með alveg eins þjónustulyftur á fimm mismunandi stöðum.</span><span class="sxs-lookup"><span data-stu-id="a855a-106">A customer for whom you provide service has identical service elevators at five different locations.</span></span>

<span data-ttu-id="a855a-107">Ætlunin er að setja upp fimm þjónustusamninga fyrir viðskiptavininn, einn fyrir hvert svæði.</span><span class="sxs-lookup"><span data-stu-id="a855a-107">You want to set up five service agreements for the customer, one for each site.</span></span>
<span data-ttu-id="a855a-108">Til að takmarka endurtekna vinnu við uppsetningu og til að ganga úr skugga um að upplýsingarnar um uppsetninguna í þjónustusamningunum séu eins er hægt að stofna þjónustusamning og tilgreina hann sem sniðmát fyrir þjónustuvinnuna við lyfturnar.</span><span class="sxs-lookup"><span data-stu-id="a855a-108">To limit repetitive setup work, and to make sure that the setup information in the service agreements is identical, you create a service agreement and specify it as a template for the service work on the elevators.</span></span>

<span data-ttu-id="a855a-109">Núna er hægt að afrita sniðmátslínurnar í nýju þjónustusamningana fimm þannig að allir þjónustusamningarnir séu með línur úr sniðmátinu.</span><span class="sxs-lookup"><span data-stu-id="a855a-109">You can now copy the template lines into the five new service agreements, so that each service agreement is populated with the lines from the template.</span></span>

## <a name="create-a-template"></a><span data-ttu-id="a855a-110">Búa til sniðmát</span><span class="sxs-lookup"><span data-stu-id="a855a-110">Create a template</span></span>

<span data-ttu-id="a855a-111">Þegar þjónustusniðmát er stofnað er þjónustusamningur stofnaður, línurnar sem þörf er á fyrir hann stofnaðar og þjónustusamningurinn tengdur við þjónustusniðmátsflokk.</span><span class="sxs-lookup"><span data-stu-id="a855a-111">When you create a service template, you create a service agreement, create the required lines on it, and attach the service agreement to a service-template group.</span></span>

> [!NOTE]
> <span data-ttu-id="a855a-112">Aðeins er hægt að skilgreina þjónustusamning sem sniðmát ef hann er ekki með neinar þjónustupantanir tengdar við sig.</span><span class="sxs-lookup"><span data-stu-id="a855a-112">A service agreement can be defined as a template only if it has no service orders attached to it.</span></span> <span data-ttu-id="a855a-113">Einnig er ekki hægt að búa til þjónustupöntun úr þjónustusamningi sem er skilgreindur sem sniðmát.</span><span class="sxs-lookup"><span data-stu-id="a855a-113">Also, no service orders can be generated from a service agreement that is defined as a template.</span></span>

## <a name="copy-template-lines"></a><span data-ttu-id="a855a-114">Afrita sniðmátslínur</span><span class="sxs-lookup"><span data-stu-id="a855a-114">Copy template lines</span></span>

<span data-ttu-id="a855a-115">Hægt er að afrita sniðmátslínur úr þjónustusniðmáti í annan þjónustusamning eða þjónustupöntun.</span><span class="sxs-lookup"><span data-stu-id="a855a-115">You can copy template lines from a service template into another service agreement or into a service order.</span></span>

<span data-ttu-id="a855a-116">Þegar sniðmátslínur eru afritaðar í þjónustupantanirnar eða þjónustusamningana birtast sniðmátsflokkarnir í trjáyfirliti þar sem hægt er að víkka út flokkana.</span><span class="sxs-lookup"><span data-stu-id="a855a-116">When you copy template lines into your service orders or service agreements, your template groups are displayed in a tree view in which each group can be expanded.</span></span> <span data-ttu-id="a855a-117">Þessi skjár gerir þér kleift að skoða öll sniðmátin og sniðmátslínurnar.</span><span class="sxs-lookup"><span data-stu-id="a855a-117">This display lets you view each template and template line.</span></span>

<span data-ttu-id="a855a-118">Það er auðveldara að ákvarða sniðmátslínurnar sem á að afrita ef sniðmátin hafa verið flokkuð undir nöfnum sem endurspegla notkun sniðmátsins.</span><span class="sxs-lookup"><span data-stu-id="a855a-118">It is easier to determine the service-template lines that you want to copy if you have grouped the templates under names that reflect the use of the templates.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a855a-119">Tengd efnisatriði</span><span class="sxs-lookup"><span data-stu-id="a855a-119">Related topics</span></span>

[<span data-ttu-id="a855a-120">Afrita línur þjónustusniðmáta</span><span class="sxs-lookup"><span data-stu-id="a855a-120">Copy service templates lines</span></span>](copy-service-template-lines.md)
