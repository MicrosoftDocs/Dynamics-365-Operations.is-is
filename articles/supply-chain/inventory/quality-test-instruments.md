---
title: Prófunartæki gæðastjórnunar
description: Í þessu efnisatriði er lýst hvernig á að stofna prufubreytur sem hægt er að nota í prófunum gæðapantana í Microsoft Dynamics 365 Supply Chain Management.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestInstrument
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dc09021f89a9064a3140a726fca74e3eceab13da
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956700"
---
# <a name="quality-management-test-instruments"></a><span data-ttu-id="7f188-103">Prófunartæki gæðastjórnunar</span><span class="sxs-lookup"><span data-stu-id="7f188-103">Quality management test instruments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7f188-104">Í þessu efnisatriði er lýst hvernig á að stofna prufubreytur sem hægt er að nota í prófunum gæðapantana í Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="7f188-104">This topic describes how to create test instruments that can be used for tests on quality orders in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="7f188-105">Þú notar síðuna **Prófunartæki** til að skilgreina og skoða upplýsingar um tækin sem eru notuð til að framkvæma prófanir á gæðapöntunum.</span><span class="sxs-lookup"><span data-stu-id="7f188-105">You use the **Test instruments** page to define and view details about the devices that are used to perform tests on quality orders.</span></span> <span data-ttu-id="7f188-106">Prófunartæki eru valfrjáls.</span><span class="sxs-lookup"><span data-stu-id="7f188-106">Test instruments are optional.</span></span> <span data-ttu-id="7f188-107">Hins vegar geta þeir hjálpað gæðastarfsmönnum að vita hvaða tæki eða tól þeir ættu að nota til að framkvæma sérstakt próf.</span><span class="sxs-lookup"><span data-stu-id="7f188-107">However, they can help quality workers know which device or tool they should use to perform a specific test.</span></span>

## <a name="test-instrument-example"></a><span data-ttu-id="7f188-108">Dæmi um prófunartæki</span><span class="sxs-lookup"><span data-stu-id="7f188-108">Test instrument example</span></span>

<span data-ttu-id="7f188-109">Þú ert að framkvæma ýmis próf á íhlutum raftækja.</span><span class="sxs-lookup"><span data-stu-id="7f188-109">You're performing various tests on electrical components.</span></span> <span data-ttu-id="7f188-110">Sum próf eru fyrir rafspennu íhlutanna, eitt próf er fyrir hitastig þeirra og eitt próf er fyrir þyngd þeirra.</span><span class="sxs-lookup"><span data-stu-id="7f188-110">Some tests are for the voltage output of the components, one test is for their temperature, and one test is for their weight.</span></span> <span data-ttu-id="7f188-111">Mismunandi verkfæri, tæki eða búnaður er notaður til að framkvæma hvert próf.</span><span class="sxs-lookup"><span data-stu-id="7f188-111">Different tools, devices, or equipment is used to perform each test.</span></span> <span data-ttu-id="7f188-112">Til dæmis er spennumælir notaður til að mæla spennu, hitamælir notaður til að mæla hitastig og vog notuð til að mæla þyngd.</span><span class="sxs-lookup"><span data-stu-id="7f188-112">For example, a voltage meter is used to measure voltage, a thermometer is used to measure temperature, and a scale is used to measure weight.</span></span> <span data-ttu-id="7f188-113">Þú getur stillt hvert þessara tækja sem prófunarbúnað og tilgreint mælieininguna sem skal skrá niðurstöður prófunarinnar í.</span><span class="sxs-lookup"><span data-stu-id="7f188-113">You can configure each of these devices as a test instrument and indicate the unit of measure that the test results should be recorded in.</span></span> <span data-ttu-id="7f188-114">Til dæmis eru niðurstöður úr spennumælinum skráðar í voltum, niðurstöður úr hitamælinum eru skráðar í gráðum Fahrenheit eða gráðum selsíus og niðurstöður vigtarinnar eru skráðar í pundum eða kílóum.</span><span class="sxs-lookup"><span data-stu-id="7f188-114">For example, results from the voltage meter are recorded in volts, results from the thermometer are recorded in degrees Fahrenheit or degrees Celsius, and results from the scale are recorded in pounds or kilograms.</span></span>

## <a name="create-a-test-instrument"></a><span data-ttu-id="7f188-115">Stofna prófunartæki</span><span class="sxs-lookup"><span data-stu-id="7f188-115">Create a test instrument</span></span>

1. <span data-ttu-id="7f188-116">Farið í **Birgðastjórnun \> Uppsetning \> Gæðastjórnun \> Prófunartæki**.</span><span class="sxs-lookup"><span data-stu-id="7f188-116">Go to **Inventory management \> Setup \> Quality control \> Test instruments**.</span></span>
1. <span data-ttu-id="7f188-117">Á aðgerðasvæðinu skal velja **Ný** til að bæta línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="7f188-117">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="7f188-118">Stillið svo eftirfarandi reiti fyrir nýju línuna:</span><span class="sxs-lookup"><span data-stu-id="7f188-118">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="7f188-119">**Prófunartæki** – Færið inn einkvæmt kenni eða heiti fyrir prófunartækið.</span><span class="sxs-lookup"><span data-stu-id="7f188-119">**Test instrument** – Enter a unique ID or name for the test instrument.</span></span>
    - <span data-ttu-id="7f188-120">**Lýsing** – Færið inn nákvæma lýsingu á prófunartækinu.</span><span class="sxs-lookup"><span data-stu-id="7f188-120">**Description** – Enter a detailed description of the test instrument.</span></span>
    - <span data-ttu-id="7f188-121">**Eining** – Veljið eininguna sem tækið mælir niðurstöður í.</span><span class="sxs-lookup"><span data-stu-id="7f188-121">**Unit** – Select the unit that the instrument measures results in.</span></span> <span data-ttu-id="7f188-122">Reiturinn **Nákvæmni** er sjálfkrafa stilltur út frá einingunni sem þú velur.</span><span class="sxs-lookup"><span data-stu-id="7f188-122">The **Precision** field is automatically set, based on the unit that you select.</span></span>

1. <span data-ttu-id="7f188-123">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7f188-123">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7f188-124">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="7f188-124">Additional resources</span></span>

- [<span data-ttu-id="7f188-125">Prófun gæðastjórnunar</span><span class="sxs-lookup"><span data-stu-id="7f188-125">Quality management test</span></span>](quality-tests.md)
- [<span data-ttu-id="7f188-126">Prófunarflokkar gæðastjórnunar</span><span class="sxs-lookup"><span data-stu-id="7f188-126">Quality management test groups</span></span>](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
