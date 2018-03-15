---
title: "Þjónustuhlutarflokkar"
description: "Hlutaflokkar gagnast til þess að flokka og sía gögnin um hluti fyrir skýrslur og talnagögn."
author: YuyuScheller
manager: AnnBe
ms.date: 02/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceObjectGroups
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 221b9dae7e83e7f4a535ac60f2a2011533d7861c
ms.openlocfilehash: fa503ac82286099a0eafc7034d169e165b538e2c
ms.contentlocale: is-is
ms.lasthandoff: 02/21/2018

---

# <a name="service-object-groups"></a><span data-ttu-id="ce328-103">Þjónustuhlutarflokkar</span><span class="sxs-lookup"><span data-stu-id="ce328-103">Service object groups</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ce328-104">Hlutaflokkar gagnast til þess að flokka og sía gögnin um hluti fyrir skýrslur og talnagögn.</span><span class="sxs-lookup"><span data-stu-id="ce328-104">Object groups are useful for sorting and filtering the data about objects for reports and statistics.</span></span> <span data-ttu-id="ce328-105">Til dæmis er hægt að flokka hluti eftir landfræðilegri staðsetningu eða gerð.</span><span class="sxs-lookup"><span data-stu-id="ce328-105">For example, you can group objects by geographical location or by type.</span></span>

## <a name="group-by-geographical-location"></a><span data-ttu-id="ce328-106">Flokkur eftir landfræðilegri staðsetningu</span><span class="sxs-lookup"><span data-stu-id="ce328-106">Group by geographical location</span></span>

<span data-ttu-id="ce328-107">Hægt er að nota þessa flokkunaraðferð til þess að sýna hvar hinir ýmsu ólíku hlutir sem fyrirtæki notanda þjónustar eru staðsettir.</span><span class="sxs-lookup"><span data-stu-id="ce328-107">You can use this grouping method to show where the various different objects that your company services are located.</span></span> <span data-ttu-id="ce328-108">Flokkun hluta eftir landfræðilegri staðsetningu getur líka verið gagnleg ef nauðsynlegt er að auðkenna hlutina sem fyrirtæki notanda veitir nú þegar þjónustu fyrir í tilteknu landi/svæði, svo dæmi sé tekið.</span><span class="sxs-lookup"><span data-stu-id="ce328-108">Grouping objects by geographical location can also be useful if, for example, you must identify the objects that your company already provides services for in a particular country/region.</span></span>

## <a name="example"></a><span data-ttu-id="ce328-109">Dæmi</span><span class="sxs-lookup"><span data-stu-id="ce328-109">Example</span></span>

<span data-ttu-id="ce328-110">Viðskiptavinur frá Belgíu hringir í þjónustumiðstöð notanda og vill stofna þjónustusamning fyrir hlut, ABC.</span><span class="sxs-lookup"><span data-stu-id="ce328-110">A customer from Belgium calls your service center and wants to create a service agreement for an object, ABC.</span></span> <span data-ttu-id="ce328-111">Notandinn hefur tengt hlutaflokk eftir landfræðilegri staðsetningu, Belgíu, við alla hluti sem eru þjónustaðir í Belgíu.</span><span class="sxs-lookup"><span data-stu-id="ce328-111">You have attached an object group for geographical location, Belgium, to all objects that are serviced in Belgium.</span></span> <span data-ttu-id="ce328-112">Með því að nota þennan flokk sem síu er hægt að leita með hraði til þess að kanna hvort ABC sé þegar til sem færsla í forriti notanda eða hvort nauðsynlegt er að setja upp nýjan hlut.</span><span class="sxs-lookup"><span data-stu-id="ce328-112">By using this group as a filter, you can quickly search to see whether you already have a record for ABC in the program, or whether you must set up a new object.</span></span> 

## <a name="group-by-type"></a><span data-ttu-id="ce328-113">Flokkur eftir gerð</span><span class="sxs-lookup"><span data-stu-id="ce328-113">Group by type</span></span>

<span data-ttu-id="ce328-114">Hægt er að nota þessa flokkunaraðferð til þess að sýna gerðir þeirra hluta sem fyrirtæki notanda þjónustar.</span><span class="sxs-lookup"><span data-stu-id="ce328-114">You can use this grouping method to show the types of objects that your company services.</span></span> <span data-ttu-id="ce328-115">Flokkun hluta eftir gerð getur líka verið gagnleg ef ætlunin er að stofna nýjan hlut byggðan á svipuðum hlutum sem þegar eru til í forritinu.</span><span class="sxs-lookup"><span data-stu-id="ce328-115">Grouping objects by type can also be useful if, for example, you want to create a new object based on similar objects that already exist in the program.</span></span>

## <a name="example"></a><span data-ttu-id="ce328-116">Dæmi</span><span class="sxs-lookup"><span data-stu-id="ce328-116">Example</span></span>

<span data-ttu-id="ce328-117">Viðskiptavinur hringir og vill setja upp þjónustusamning fyrir loftræstibúnað, HIJ.</span><span class="sxs-lookup"><span data-stu-id="ce328-117">A customer calls and wants to set up a service agreement for an air conditioning machine, HIJ.</span></span> <span data-ttu-id="ce328-118">Engin færsla er til fyrir þetta tæki.</span><span class="sxs-lookup"><span data-stu-id="ce328-118">You do not already have a record for this machine.</span></span> <span data-ttu-id="ce328-119">Hins vegar er búið að setja upp hlutaflokk með nafninu Loftræstibúnaður og tengja hann við alla loftræstibúnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="ce328-119">However, you have set up an object group titled Air Conditioners, and you have attached this group to all air conditioning objects.</span></span> <span data-ttu-id="ce328-120">Þar af leiðandi er hægt að leita fljótt að og auðkenna allan annan loftræstibúnað og nota sniðmátsupplýsingar um þessa hluti til þess að stofna þjónustusamningslínur fyrir HIJ.</span><span class="sxs-lookup"><span data-stu-id="ce328-120">Therefore, you can quickly search for and identify all other air conditioning machines and use the template information from these objects to create service agreement lines for HIJ.</span></span> <span data-ttu-id="ce328-121">Með þvi að nota flokka á þennan hátt er hægt að setja upp nýja hluti með hraði og ákvarða þjónustuverkliðina sem þarf að framkvæma á þeim.</span><span class="sxs-lookup"><span data-stu-id="ce328-121">By using object groups in this manner, you can quickly set up new objects and determine the service tasks that must be performed on them.</span></span> 




