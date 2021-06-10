---
title: Sveigjanleg frátektarregla á vídd vöruhúsastigs
description: Þetta efni lýsir stefnuskrá fyrir birgða sem láta fyrirtæki sem selja vörur sem eru rekin með runur og reka flutninga sína sem aðgerðir með WMS-virka áskilja sértækar runur fyrir sölupantanir viðskiptavina, jafnvel þó að pöntunarveldið sem er tengt vörunum banni ekki fyrirvara á tilteknum runum.
author: perlynne
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSReservationHierarchy, WHSWorkTrans, WHSWorkInventTrans, WHSInventTableReservationHierarchy, WHSReservationHierarchyCreate, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-01-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: ed90e773e1b8c90afc119a471cf844941ad19226
ms.sourcegitcommit: 0cc89dd42c1924ca0ec735c6566bc56b39cc5f7d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/26/2021
ms.locfileid: "6103047"
---
# <a name="flexible-warehouse-level-dimension-reservation-policy"></a><span data-ttu-id="f2e80-103">Sveigjanleg frátektarregla á vídd vöruhúsastigs</span><span class="sxs-lookup"><span data-stu-id="f2e80-103">Flexible warehouse-level dimension reservation policy</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f2e80-104">Þegar frátekningarstigveldi birgða af gerðinni *Runa fyrir neðan\[staðsetningu\]* tengist afurðum, geta fyrirtæki, sem selja runuraktar afurðir og keyra vörustjórnun sína sem aðgerðir sem eru virkjaðar fyrir Microsoft Dynamics 365 vöruhúsakerfið, ekki tekið frá tilteknar runur þeirra afurða fyrir sölupantanir viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="f2e80-104">When an inventory reservation hierarchy of the *Batch-below\[location\]* type is associated with products, businesses that sell batch-tracked products and run their logistics as operations that are enabled for the Microsoft Dynamics 365 Warehouse Management System (WMS) can't reserve specific batches of those products for customer sales orders.</span></span>

<span data-ttu-id="f2e80-105">Á svipaðan hátt er ekki hægt að taka frá sérstakar númeraplötur fyrir afurðir í sölupöntunum þegar þessar afurðir eru tengdar við sjálfgefið frátekningarstigveldi.</span><span class="sxs-lookup"><span data-stu-id="f2e80-105">In a similar way, specific license plates can't be reserved for products on sales orders when those products are associated with the default reservation hierarchy.</span></span>

<span data-ttu-id="f2e80-106">Þetta efnisatriði lýsir frátekningarreglu birgða sem gerir þessum fyrirtækjum kleift að taka frá ákveðnar runur eða númeraplötur, jafnvel þegar afurðirnar eru tengdar frátekningarstigveldi *Runa fyrir neðan\[staðsetningu\]*.</span><span class="sxs-lookup"><span data-stu-id="f2e80-106">This topic describes the inventory reservation policy that lets these businesses reserve specific batches or license plates, even when the products are associated with a *Batch-below\[location\]* reservation hierarchy.</span></span>

## <a name="inventory-reservation-hierarchy"></a><span data-ttu-id="f2e80-107">Frátekningarstigveldi birgða</span><span class="sxs-lookup"><span data-stu-id="f2e80-107">Inventory reservation hierarchy</span></span>

<span data-ttu-id="f2e80-108">Þessi hluti dregur saman núverandi stigveldi birgða fyrirvara.</span><span class="sxs-lookup"><span data-stu-id="f2e80-108">This section summarizes the existing inventory reservation hierarchy.</span></span>

<span data-ttu-id="f2e80-109">Frátekningarstigveldi birgða boðar, hvað varðar geymsluvíddir, að eftirspurnarpöntunin geymi áskildar víddir svæðis, vöruhúss og birgðastöðu.</span><span class="sxs-lookup"><span data-stu-id="f2e80-109">The inventory reservation hierarchy dictates that, as far as storage dimensions are concerned, the demand order carries the mandatory dimensions of site, warehouse, and inventory status.</span></span> <span data-ttu-id="f2e80-110">Í öðrum orðum eru áskildar víddir allar víddirnar fyrir ofan vídd staðsetningar í frátekningarstigveldinu á meðan regla vöruhúss ber ábyrgð á úthlutun staðsetningar á umbeðið magn og frátekningu staðsetningarinnar.</span><span class="sxs-lookup"><span data-stu-id="f2e80-110">In other words, the mandatory dimensions are all the dimensions above the location dimension in the reservation hierarchy, while the warehouse logic is responsible for assigning a location to the requested quantities and reserving the location.</span></span> <span data-ttu-id="f2e80-111">Í samskiptum milli eftirspurnarpöntunarinnar og vöruhúsaaðgerðanna er búist við að eftirspurnarpöntunin gefi til kynna hvaðan senda á pöntunina frá (þ.e. hvaða svæði og vöruhúsi).</span><span class="sxs-lookup"><span data-stu-id="f2e80-111">In the interactions between the demand order and the warehouse operations, the demand order is expected to indicate where the order must be shipped from (that is, what site and warehouse).</span></span> <span data-ttu-id="f2e80-112">Vöruhúsið treystir síðan á rökfræði þess til að finna nauðsynlegt magn í húsnæði vörugeymslu.</span><span class="sxs-lookup"><span data-stu-id="f2e80-112">The warehouse then relies on its logic to find the required quantity in the warehouse premises.</span></span>

<span data-ttu-id="f2e80-113">Hins vegar, til að endurspegla rekstrarlíkan fyrirtækisins, eru mælingar á stærð (runu og raðnúmer) háð meiri sveigjanleika.</span><span class="sxs-lookup"><span data-stu-id="f2e80-113">However, to reflect the operational model of the business, tracking dimensions (batch and serial numbers) are subject to more flexibility.</span></span> <span data-ttu-id="f2e80-114">Stigveldi birgðapöntunar rúmar atburðarás þar sem eftirfarandi skilyrði eiga við:</span><span class="sxs-lookup"><span data-stu-id="f2e80-114">An inventory reservation hierarchy can accommodate scenarios where the following conditions apply:</span></span>

- <span data-ttu-id="f2e80-115">Fyrirtækið reiðir sig á vöruhúsaaðgerðir sínar til að stjórna tiltekt á magni sem er með runu- eða raðnúmer *eftir* að magnið finnst í geymsluplássi vöruhúss.</span><span class="sxs-lookup"><span data-stu-id="f2e80-115">The business relies on its warehouse operations to manage picking of quantities that have batch or serial numbers *after* the quantities have been found in the warehousing storage space.</span></span> <span data-ttu-id="f2e80-116">Oft er vísað í þetta líkan sem *Runa fyrir neðan\[staðsetningu\]* eða *Raðnúmer fyrir neðan\[staðsetningu\]*.</span><span class="sxs-lookup"><span data-stu-id="f2e80-116">This model is often referred to as *Batch-below\[location\]* or *Serial-below\[location\]*.</span></span> <span data-ttu-id="f2e80-117">Það er venjulega notað þegar framleiðslueining vöru eða raðnúmer er ekki mikilvægt fyrir viðskiptavini sem setja eftirspurnina hjá sölufyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="f2e80-117">It's typically used when a product's batch or serial number identification isn't important to the customers who place the demand with the selling company.</span></span>
- <span data-ttu-id="f2e80-118">Fyrirtækið reiðir sig á vöruhúsaaðgerðir sínar til að stjórna tiltekt á magni sem er með runu- eða raðnúmer *áður en* magnið finnst í geymsluplássi vöruhúss.</span><span class="sxs-lookup"><span data-stu-id="f2e80-118">The business relies on its warehouse operations to manage picking of quantities that have batch or serial numbers *before* the quantities have been found in the warehousing storage space.</span></span> <span data-ttu-id="f2e80-119">Ef runu- eða raðnúmer er nauðsynlegt sem hluti af forskrift viðskiptavinapöntunar eru þau skráð í eftirspurnarpöntunina og vöruhúsaaðgerðirnar sem finna magnið í vöruhúsinu mega ekki breyta þeim.</span><span class="sxs-lookup"><span data-stu-id="f2e80-119">If batch or serial numbers are necessary as part of a customer's order specification, they are recorded on the demand order, and the warehouse operations that find the quantities in the warehouse aren't allowed to change them.</span></span> <span data-ttu-id="f2e80-120">Þetta líkan er kallað *Runa fyrir ofan\[staðsetningu\]* eða *Raðnúmer fyrir ofan\[staðsetningu\]*.</span><span class="sxs-lookup"><span data-stu-id="f2e80-120">This model is referred to as *Batch-above\[location\]* or *Serial-above\[location\]*.</span></span> <span data-ttu-id="f2e80-121">Þar sem víddirnar fyrir ofan staðsetningu eru tilteknu kröfurnar fyrir eftirspurnirnar sem þarf að uppfylla mun regla vöruhúss ekki úthluta þeim.</span><span class="sxs-lookup"><span data-stu-id="f2e80-121">Because the dimensions above location are the specific requirements for the demands that must be fulfilled, the warehouse logic won't allocate them.</span></span> <span data-ttu-id="f2e80-122">Þessar víddir **verða** alltaf að vera tilgreindar í eftirspurnarpöntuninni eða tengdum frátekningum.</span><span class="sxs-lookup"><span data-stu-id="f2e80-122">These dimensions **must** always be specified on the demand order or in the related reservations.</span></span>

<span data-ttu-id="f2e80-123">Í þessum atburðarásum er áskorunin sú að aðeins er hægt að úthluta einum birgða pöntunarveldi fyrir hverja vöru sem gefin er út.</span><span class="sxs-lookup"><span data-stu-id="f2e80-123">In these scenarios, the challenge is that only one inventory reservation hierarchy can be assigned to each released product.</span></span> <span data-ttu-id="f2e80-124">Þess vegna, fyrir WMS til að meðhöndla rakta hluti, eftir að stigveldi verkefnisins ákvarðar hvenær á að panta lotu eða raðnúmer (annað hvort þegar eftirspurnarpöntunin er tekin eða meðan á pökkunarvinnu vörugeymslu stendur), er ekki hægt að breyta þessari tímasetningu í auglýsingu -hoc grundvöllur.</span><span class="sxs-lookup"><span data-stu-id="f2e80-124">Therefore, for the WMS to handle tracked items, after the hierarchy assignment determines when the batch or serial number should be reserved (either when the demand order is taken or during the warehouse picking work), this timing can't be changed on an ad-hoc basis.</span></span>

## <a name="flexible-reservation-for-batch-tracked-items"></a><span data-ttu-id="f2e80-125">Sveigjanlegur fyrirvari fyrir hluti sem rekja má hóp</span><span class="sxs-lookup"><span data-stu-id="f2e80-125">Flexible reservation for batch-tracked items</span></span>

### <a name="business-scenario"></a><span data-ttu-id="f2e80-126">Sviðsmynd fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="f2e80-126">Business scenario</span></span>

<span data-ttu-id="f2e80-127">Í þessari atburðarás notar fyrirtæki birgðarstefnu þar sem fullunnum vörum er rakið eftir lotunúmerum.</span><span class="sxs-lookup"><span data-stu-id="f2e80-127">In this scenario, a company uses an inventory strategy where finished goods are tracked by batch numbers.</span></span> <span data-ttu-id="f2e80-128">Þetta fyrirtæki notar einnig WMS vinnuálag.</span><span class="sxs-lookup"><span data-stu-id="f2e80-128">This company also uses the WMS workload.</span></span> <span data-ttu-id="f2e80-129">Þar sem þetta vinnuálag er með vel útbúna reglu fyrir áætlanagerð og keyrslu tiltekta og sendingaraðgerða fyrir runuvirkar vörur, tengjast flestar tilbúnu afurðirnar frátekningarstigveldi birgða fyrir *Runa fyrir neðan\[staðsetningu\]*.</span><span class="sxs-lookup"><span data-stu-id="f2e80-129">Because this workload has well-equipped logic for planning and running warehouse picking and shipping operations for batch-enabled items, most of the finished items are associated with a *Batch-below\[location\]* inventory reservation hierarchy.</span></span> <span data-ttu-id="f2e80-130">Kosturinn við þessa tegund rekstraruppsetningar er að ákvörðunum (sem eru í raun fyrirvara um fyrirvaralausar ákvarðanir) um hvaða runur á að velja og hvar eigi að setja þær í vörugeymslunni er frestað þangað til að vörugeymsla hefst.</span><span class="sxs-lookup"><span data-stu-id="f2e80-130">The advantage of this type of operational setup is that decisions (which are effectively reservation decisions) about which batches to pick and where to put them in the warehouse are postponed until the warehouse picking operations start.</span></span> <span data-ttu-id="f2e80-131">Þeir eru ekki gerðir þegar pöntun viðskiptavinarins er sett.</span><span class="sxs-lookup"><span data-stu-id="f2e80-131">They aren't made when the customer's order is placed.</span></span>

<span data-ttu-id="f2e80-132">Þótt frátekningarstigveldið *Runa fyrir neðan\[staðsetningu\]* þjónar viðskiptamarkmiðum fyrirtækisins, þurfa margir af viðskiptavinum fyrirtækisins sömu rununa og þeir keyptu áður þegar þeir pöntuðu afurðirnar aftur.</span><span class="sxs-lookup"><span data-stu-id="f2e80-132">Although the *Batch-below\[location\]* reservation hierarchy serves the company's business goals well, many of the company's established customers require the same batch that they previously purchased when they reorder products.</span></span> <span data-ttu-id="f2e80-133">Þess vegna er fyrirtækið að leita að sveigjanleika í meðhöndlun reglna um röðun pöntunar svo að eftir atvikum viðskiptavina eftir sama hlut, gerist eftirfarandi hegðun:</span><span class="sxs-lookup"><span data-stu-id="f2e80-133">Therefore, the company is looking for flexibility in the way that the batch reservation rules are handled, so that, depending on the customers' demand for the same item, the following behaviors occur:</span></span>

- <span data-ttu-id="f2e80-134">Hægt er að skrá lotunúmer og panta þegar pöntunin er tekin af söluaðilanum og ekki er hægt að breyta því við vörugeymslu og / eða taka af öðrum kröfum.</span><span class="sxs-lookup"><span data-stu-id="f2e80-134">A batch number can be recorded and reserved when the order is taken by the sales processor, and it can't be changed during warehouse operations and/or taken by other demands.</span></span> <span data-ttu-id="f2e80-135">Þessi hegðun hjálpar til við að tryggja að lotunúmerið sem var pantað er sent til viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="f2e80-135">This behavior helps guarantee that the batch number that was ordered is shipped to the customer.</span></span>
- <span data-ttu-id="f2e80-136">Ef lotunúmerið er ekki mikilvægt fyrir viðskiptavininn, þá geta vörugeymsluaðgerðir ákvarðað lotunúmer meðan á vinnu stendur, eftir að skráning og pöntun sölupöntunar hefur verið gert.</span><span class="sxs-lookup"><span data-stu-id="f2e80-136">If the batch number isn't important to the customer, the warehouse operations can determine a batch number during picking work, after sales order registration and reservation have been done.</span></span>

### <a name="allowing-reservation-of-a-specific-batch-on-the-sales-order"></a><span data-ttu-id="f2e80-137">Leyfa fyrirvara um ákveðna lotu í sölupöntuninni</span><span class="sxs-lookup"><span data-stu-id="f2e80-137">Allowing reservation of a specific batch on the sales order</span></span>

<span data-ttu-id="f2e80-138">Til að koma til móts við æskilegan sveigjanleika í hegðun runufrátekningar fyrir vörur sem tengjast *Runu fyrir neðan\[staðsetningu\]* í frátekningarstigveldi birgða, verða birgðastjórar að velja gátreitinn **Leyfa frátekt á eftirspurnarpöntun** fyrir stigið **Rununúmer** á síðunni **Frátekningarstigveldi birgða**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-138">To accommodate the desired flexibility in the batch reservation behavior for items that are associated with a *Batch-below\[location\]* inventory reservation hierarchy, inventory managers must select the **Allow reservation on demand order** check box for the **Batch number** level on the **Inventory reservation hierarchies** page.</span></span>

![Stigveldi fyrir birgðafrátektir gert sveigjanlegt](media/Flexible-inventory-reservation-hierarchy.png)

<span data-ttu-id="f2e80-140">Þegar stigið **Rununúmer** í stigveldinu er valið, allar víddir yfir því stigi og upp í gegnum **Staðsetning** stig verður sjálfkrafa valið.</span><span class="sxs-lookup"><span data-stu-id="f2e80-140">When the **Batch number** level in the hierarchy is selected, all dimensions above that level and up through the **Location** level will be automatically selected.</span></span> <span data-ttu-id="f2e80-141">(Sjálfgefið að allar víddir yfir **Staðsetning** stig eru valin.) Þessi hegðun endurspeglar rökfræði þar sem allar víddir á bilinu milli lotunúmers og staðsetningar eru einnig sjálfkrafa fráteknar eftir að þú hefur pantað tiltekið lotunúmer á pöntunarlínunni.</span><span class="sxs-lookup"><span data-stu-id="f2e80-141">(By default, all dimensions above the **Location** level are preselected.) This behavior reflects the logic where all dimensions in the range between the batch number and location are also automatically reserved after you reserve a specific batch number on the order line.</span></span>

> [!NOTE]
> <span data-ttu-id="f2e80-142">Gátreiturinn **Leyfa fyrirvara á pöntunarbeiðni** á aðeins við um stig stigveldis sem er undir staðsetningu víddar vörugeymslu.</span><span class="sxs-lookup"><span data-stu-id="f2e80-142">The **Allow reservation on demand order** check box applies only to reservation hierarchy levels that are below the warehouse location dimension.</span></span>
>
> <span data-ttu-id="f2e80-143">**Rununúmer** og **Númeraplata** eru einu stigin í stigveldinu sem eru opin fyrir sveigjanlegu frátekningarreglunni.</span><span class="sxs-lookup"><span data-stu-id="f2e80-143">**Batch number** and **License plate** are the only levels in the hierarchy that are open for the flexible reservation policy.</span></span> <span data-ttu-id="f2e80-144">Með öðrum orðum er ekki hægt að velja gátreitinn **Leyfa frátekt á eftirspurnarpöntun** fyrir stig **Staðsetningar** eða **Raðnúmers**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-144">In other words, you can't select the **Allow reservation on demand order** check box for the **Location** or **Serial number** level.</span></span>
>
> <span data-ttu-id="f2e80-145">Ef frátekningarstigveldið inniheldur vídd rununúmersins (sem verður alltaf að vera fyrir neðan stigið **Rununúmer**) og ef kveikt hefur verið á runumiðaðri frátekt fyrir rununúmerið mun kerfið halda áfram að vinna með aðgerðir rununúmerafrátekningar og tiltektar samkvæmt reglunum sem eiga við um frátekningarregluna *Raðnúmer fyrir neðan\[staðsetningu\]*.</span><span class="sxs-lookup"><span data-stu-id="f2e80-145">If your reservation hierarchy includes the serial number dimension (which must always be below the **Batch number** level), and if you've turned on batch-specific reservation for the batch number, the system will continue to handle serial number reservation and picking operations, based on the rules that apply to the *Serial-below\[location\]* reservation policy.</span></span>

<span data-ttu-id="f2e80-146">Hægt er að leyfa runumiðaða frátekningu hvenær sem er fyrir fyrirliggjandi frátekningarstigveldið *Runa fyrir neðan\[staðsetningu\]* í uppsetningunni.</span><span class="sxs-lookup"><span data-stu-id="f2e80-146">At any point, you can allow batch-specific reservation for an existing *Batch-below\[location\]* reservation hierarchy in your deployment.</span></span> <span data-ttu-id="f2e80-147">Þessi breyting mun ekki hafa áhrif á neina fyrirvara og opna vöruhúsavinnu sem voru búin til áður en breytingin átti sér stað.</span><span class="sxs-lookup"><span data-stu-id="f2e80-147">This change won't affect any reservations and open warehouse work that were created before the change occurred.</span></span> <span data-ttu-id="f2e80-148">Hins vegar **Leyfa fyrirvara á pöntunarbeiðni** Ekki er hægt að hreinsa gátreitinn ef birgðafærslur á **Frátekið pantað**, **Frátekin líkamleg**, eða **Pantaði** útgáfutegund er til fyrir einn eða fleiri hluti sem eru tengdir því pöntunarveldi.</span><span class="sxs-lookup"><span data-stu-id="f2e80-148">However, the **Allow reservation on demand order** check box can't be cleared if inventory transactions of the **Reserved ordered**, **Reserved physical**, or **Ordered** issue type exist for one or more items that are associated with that reservation hierarchy.</span></span>

> [!NOTE]
> <span data-ttu-id="f2e80-149">Ef núverandi fyrirvaralegveldi hlutar leyfir ekki forskrift lotur í pöntuninni, þá geturðu endurúthlutað því í pöntunarveldi sem gerir kleift að skilgreina lotu, að því tilskildu að stigskipulag stigveldisins sé það sama í báðum stigveldum.</span><span class="sxs-lookup"><span data-stu-id="f2e80-149">If an item's existing reservation hierarchy doesn't allow batch specification on the order, you can reassign it to a reservation hierarchy that does allow batch specification, provided that the hierarchy level structure is the same in both hierarchies.</span></span> <span data-ttu-id="f2e80-150">Nota **Breyta pöntunarveldi fyrir hluti** virka til að framkvæma endurúthlutun.</span><span class="sxs-lookup"><span data-stu-id="f2e80-150">Use the **Change reservation hierarchy for items** function to do the reassignment.</span></span> <span data-ttu-id="f2e80-151">Þessi breyting gæti skipt máli þegar þú vilt koma í veg fyrir sveigjanlegan pöntunarhluta fyrir hlutmengi af hlutum sem eru rekin í hópum en leyfa það fyrir restina af vöruframboði.</span><span class="sxs-lookup"><span data-stu-id="f2e80-151">This change might be relevant when you want to prevent flexible batch reservation for a subset of batch-tracked items but allow it for the rest of the product portfolio.</span></span>

<span data-ttu-id="f2e80-152">Hvort sem þú hefur valið gátreitinn **Leyfa frátekt á eftirspurnarpöntun** eða ekki, ef þú vilt ekki taka frá ákveðið rununúmer fyrir vöruna í pöntunarlínu mun sjálfgefin regla vöruhúsaaðgerðar sem gildir fyrir *Runa fyrir neðan\[staðsetningu\]* í frátekningarstigveldi samt eiga við.</span><span class="sxs-lookup"><span data-stu-id="f2e80-152">Regardless of whether you've selected the **Allow reservation on demand order** check box, if you don't want to reserve a specific batch number for the item on an order line, default warehouse operations logic that is valid for a *Batch-below\[location\]* reservation hierarchy will still apply.</span></span>

### <a name="reserve-a-specific-batch-number-for-a-customer-order"></a><span data-ttu-id="f2e80-153">Pantaðu tiltekið lotunúmer fyrir pöntun viðskiptavina</span><span class="sxs-lookup"><span data-stu-id="f2e80-153">Reserve a specific batch number for a customer order</span></span>

<span data-ttu-id="f2e80-154">Þegar *Runa fyrir neðan\[staðsetningu\]* í frátekningarstigveldi birgða fyrir runurakta vöru er sett upp til að leyfa frátekningu á ákveðnum rununúmerum í sölupöntunum, geta úrvinnsluaðilar sölupöntunar tekið viðskiptavinapantanir fyrir sömu vöruna á einn af eftirfarandi hátt, eftir því hver beiðni viðskiptavinarins er:</span><span class="sxs-lookup"><span data-stu-id="f2e80-154">After a batch-tracked item's *Batch-below\[location\]* inventory reservation hierarchy is set up to allow reservation of specific batch numbers on sales orders, sales order processors can take customer orders for the same item in one of the following ways, depending on the customer's request:</span></span>

- <span data-ttu-id="f2e80-155">**Sláðu inn pöntunarupplýsingar án þess að tilgreina lotunúmer** - Þessa nálgun ætti að nota þegar framleiðslulota vöru er ekki mikilvæg fyrir viðskiptavininn.</span><span class="sxs-lookup"><span data-stu-id="f2e80-155">**Enter order details without specifying a batch number** – This approach should be used when the product's batch specification isn't important to the customer.</span></span> <span data-ttu-id="f2e80-156">Allir núverandi ferlar sem tengjast meðhöndlun pöntunar af þessari gerð kerfisins eru óbreytt.</span><span class="sxs-lookup"><span data-stu-id="f2e80-156">All existing processes that are associated with handling an order of this type in the system remain unchanged.</span></span> <span data-ttu-id="f2e80-157">Engin viðbótarsjónarmið eru nauðsynleg af hálfu notenda.</span><span class="sxs-lookup"><span data-stu-id="f2e80-157">No additional considerations are required on the part of users.</span></span>
- <span data-ttu-id="f2e80-158">**Sláðu inn pöntunarupplýsingar og pantaðu tiltekið lotunúmer** - Þessa aðferð ætti að nota þegar viðskiptavinurinn óskar eftir ákveðinni lotu.</span><span class="sxs-lookup"><span data-stu-id="f2e80-158">**Enter order details and reserve a specific batch number** – This approach should be used when the customer requests a specific batch.</span></span> <span data-ttu-id="f2e80-159">Venjulega munu viðskiptavinir biðja um ákveðna lotu þegar þeir eru að panta vöru sem þeir keyptu áður.</span><span class="sxs-lookup"><span data-stu-id="f2e80-159">Typically, customers will request a specific batch when they are reordering a product that they previously purchased.</span></span> <span data-ttu-id="f2e80-160">Þessari tegund af sértækum pöntunum er vísað til *pöntunarbundinn fyrirvara*.</span><span class="sxs-lookup"><span data-stu-id="f2e80-160">This type of batch-specific reservation is referred to as *order-committed reservation*.</span></span>

<span data-ttu-id="f2e80-161">Eftirfarandi reglur eru í gildi þegar magn er afgreitt og lotunúmer er skuldbundið til sérstakrar pöntunar:</span><span class="sxs-lookup"><span data-stu-id="f2e80-161">The following set of rules is valid when quantities are processed, and a batch number is committed to a specific order:</span></span>

- <span data-ttu-id="f2e80-162">Til að leyfa frátekningu á ákveðnu rununúmeri fyrir vörur undir frátekningarreglunni *Runa fyrir neðan\[staðsetningu\]* verður kerfið að taka frá allar víddir upp í gegnum staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="f2e80-162">To allow reservation of a specific batch number for an item under the *Batch-below\[location\]* reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="f2e80-163">Þetta svið inniheldur venjulega stærð skírteinisins.</span><span class="sxs-lookup"><span data-stu-id="f2e80-163">This range typically includes the license plate dimension.</span></span>
- <span data-ttu-id="f2e80-164">Staðsetningartilskipanir eru ekki notaðar þegar val á vinnu er búið til fyrir sölulínu sem notar pöntunarbundna hópapöntun.</span><span class="sxs-lookup"><span data-stu-id="f2e80-164">Location directives aren't used when picking work is created for a sales line that uses order-committed batch reservation.</span></span>
- <span data-ttu-id="f2e80-165">Við vinnslu vörugeymslu á vinnu fyrir pöntunarbundna lotur er hvorki notanda né kerfinu heimilt að breyta lotunúmerinu.</span><span class="sxs-lookup"><span data-stu-id="f2e80-165">During warehouse processing of work for order-committed batches, neither the user nor the system is allowed to change the batch number.</span></span> <span data-ttu-id="f2e80-166">(Þessi vinnsla felur í sér meðhöndlun undantekninga.)</span><span class="sxs-lookup"><span data-stu-id="f2e80-166">(This processing includes exception handling.)</span></span>

<span data-ttu-id="f2e80-167">Eftirfarandi dæmi sýnir flæði frá enda til enda.</span><span class="sxs-lookup"><span data-stu-id="f2e80-167">The following example shows the end-to-end flow.</span></span>

## <a name="example-scenario-batch-number-allocation"></a><span data-ttu-id="f2e80-168">Sýniaðstæður: Úthlutun rununúmers</span><span class="sxs-lookup"><span data-stu-id="f2e80-168">Example scenario: Batch number allocation</span></span>

<span data-ttu-id="f2e80-169">Fyrir þetta dæmi verða kynningargögn að vera sett upp og þú verður að nota kynningarfyrirtækið **USMF**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-169">For this example, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="set-up-an-inventory-reservation-hierarchy-to-allow-batch-specific-reservation"></a><a name="Example-batch-allocation"></a><span data-ttu-id="f2e80-170">Setjið upp stigveldi birgða fyrirvara til að leyfa ákveðna pöntun</span><span class="sxs-lookup"><span data-stu-id="f2e80-170">Set up an inventory reservation hierarchy to allow batch-specific reservation</span></span>

1. <span data-ttu-id="f2e80-171">Fara til **Vöruhúsastjórnun** \> **Skipulag** \> **Birgðir \> Pöntunarveldi**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-171">Go to **Warehouse management** \> **Setup** \> **Inventory \> Reservation hierarchy**.</span></span>
2. <span data-ttu-id="f2e80-172">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-172">Select **New**.</span></span>
3. <span data-ttu-id="f2e80-173">Í reitnum **Heiti** skaltu slá inn nafn (til dæmis **BatchFlex**).</span><span class="sxs-lookup"><span data-stu-id="f2e80-173">In the **Name** field, enter a name (for example, **BatchFlex**).</span></span>
4. <span data-ttu-id="f2e80-174">Í reitinn **Lýsing** slærðu inn lýsingu (t.d. **Hópur fyrir neðan sveigjanlegan**).</span><span class="sxs-lookup"><span data-stu-id="f2e80-174">In the **Description** field, enter a description (for example, **Batch below flexible**).</span></span>
5. <span data-ttu-id="f2e80-175">Í reitinn **Valinn**, veldu **Raðnúmer** og **Eigandi** og veldu síðan vinstri örvarhnappinn til að færa þá í reitinn **Tiltækt**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-175">In the **Selected** field, select **Serial number** and **Owner**, and then select the left arrow button to move them to the **Available** field.</span></span>
6. <span data-ttu-id="f2e80-176">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-176">Select **OK**.</span></span>
7. <span data-ttu-id="f2e80-177">Í röðinni fyrir **Hópnúmer** víddarstig, veldu **Leyfa fyrirvara á pöntunarbeiðni** gátreitinn.</span><span class="sxs-lookup"><span data-stu-id="f2e80-177">In the row for the **Batch number** dimension level, select the **Allow reservation on demand order** check box.</span></span> <span data-ttu-id="f2e80-178">Stigin **Númeraplata** og **Staðsetning** eru sjálfkrafa valin og þú getur ekki hreinsað gátreitina fyrir þá.</span><span class="sxs-lookup"><span data-stu-id="f2e80-178">The **License plate** and **Location** levels are automatically selected, and you can't clear the check boxes for them.</span></span>
8. <span data-ttu-id="f2e80-179">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-179">Select **Save**.</span></span>

### <a name="create-a-new-released-product"></a><span data-ttu-id="f2e80-180">Stofna nýja útgefna afurð</span><span class="sxs-lookup"><span data-stu-id="f2e80-180">Create a new released product</span></span>

1. <span data-ttu-id="f2e80-181">Stilltu þrjár aðalgagnabreytur vörunnar með því að nota þessi gildi:</span><span class="sxs-lookup"><span data-stu-id="f2e80-181">Set the product's three master data parameters by using these values:</span></span>

    - <span data-ttu-id="f2e80-182">Í reitnum **Geymsluvíddarflokkur** velurðu **Ware**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-182">In the **Storage dimension group** field, select **Ware**.</span></span>
    - <span data-ttu-id="f2e80-183">Í reitnum **Rakningarvíddarflokkur** velurðu **Batch-Phy**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-183">In the **Tracking dimension group** field, select **Batch-Phy**.</span></span>
    - <span data-ttu-id="f2e80-184">Í skjámyndinni **Frátektastigveldi** velurðu **BatchFlex**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-184">In the **Reservation hierarchy** field, select **BatchFlex**.</span></span>

2. <span data-ttu-id="f2e80-185">Búðu til tvö lotunúmer, svo sem **B11** og **B22**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-185">Create two batch numbers, such as **B11** and **B22**.</span></span>
3. <span data-ttu-id="f2e80-186">Bættu magni hlutar við á lager með því að nota eftirfarandi gildi.</span><span class="sxs-lookup"><span data-stu-id="f2e80-186">Add item quantities to on-hand stock by using the following values.</span></span>

    | <span data-ttu-id="f2e80-187">Vöruhús</span><span class="sxs-lookup"><span data-stu-id="f2e80-187">Warehouse</span></span> | <span data-ttu-id="f2e80-188">Rununúmer</span><span class="sxs-lookup"><span data-stu-id="f2e80-188">Batch number</span></span> | <span data-ttu-id="f2e80-189">Staðsetning</span><span class="sxs-lookup"><span data-stu-id="f2e80-189">Location</span></span> | <span data-ttu-id="f2e80-190">Númeraplata</span><span class="sxs-lookup"><span data-stu-id="f2e80-190">License plate</span></span> | <span data-ttu-id="f2e80-191">Magn</span><span class="sxs-lookup"><span data-stu-id="f2e80-191">Quantity</span></span> |
    |-----------|--------------|----------|---------------|----------|
    | <span data-ttu-id="f2e80-192">24</span><span class="sxs-lookup"><span data-stu-id="f2e80-192">24</span></span>        | <span data-ttu-id="f2e80-193">B11</span><span class="sxs-lookup"><span data-stu-id="f2e80-193">B11</span></span>          | <span data-ttu-id="f2e80-194">BULK-001</span><span class="sxs-lookup"><span data-stu-id="f2e80-194">BULK-001</span></span> | <span data-ttu-id="f2e80-195">Enginn</span><span class="sxs-lookup"><span data-stu-id="f2e80-195">None</span></span>          | <span data-ttu-id="f2e80-196">10</span><span class="sxs-lookup"><span data-stu-id="f2e80-196">10</span></span>       |
    | <span data-ttu-id="f2e80-197">24</span><span class="sxs-lookup"><span data-stu-id="f2e80-197">24</span></span>        | <span data-ttu-id="f2e80-198">B11</span><span class="sxs-lookup"><span data-stu-id="f2e80-198">B11</span></span>          | <span data-ttu-id="f2e80-199">FL-001</span><span class="sxs-lookup"><span data-stu-id="f2e80-199">FL-001</span></span>   | <span data-ttu-id="f2e80-200">LP11</span><span class="sxs-lookup"><span data-stu-id="f2e80-200">LP11</span></span>          | <span data-ttu-id="f2e80-201">10</span><span class="sxs-lookup"><span data-stu-id="f2e80-201">10</span></span>       |
    | <span data-ttu-id="f2e80-202">24</span><span class="sxs-lookup"><span data-stu-id="f2e80-202">24</span></span>        | <span data-ttu-id="f2e80-203">B22</span><span class="sxs-lookup"><span data-stu-id="f2e80-203">B22</span></span>          | <span data-ttu-id="f2e80-204">FL-002</span><span class="sxs-lookup"><span data-stu-id="f2e80-204">FL-002</span></span>   | <span data-ttu-id="f2e80-205">LP22</span><span class="sxs-lookup"><span data-stu-id="f2e80-205">LP22</span></span>          | <span data-ttu-id="f2e80-206">10</span><span class="sxs-lookup"><span data-stu-id="f2e80-206">10</span></span>       |

### <a name="enter-sales-order-details"></a><a name="sales-order-details"></a><span data-ttu-id="f2e80-207">Slá inn upplýsingar um sölupöntun</span><span class="sxs-lookup"><span data-stu-id="f2e80-207">Enter sales order details</span></span>

1. <span data-ttu-id="f2e80-208">Farðu í **Sölu og markaðssetningu** \> **Sölupantanir** \> **Allar sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-208">Go to **Sales and marketing** \> **Sales orders** \> **All sales orders**.</span></span>
2. <span data-ttu-id="f2e80-209">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-209">Select **New**.</span></span>
3. <span data-ttu-id="f2e80-210">Í sölupöntunarhausnum, í reitnum **Viðskiptavinur reikningur** slærðu inn **US-003**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-210">On the sales order header, in the **Customer account** field, enter **US-003**.</span></span>
4. <span data-ttu-id="f2e80-211">Bættu við línu fyrir nýja vöru og sláðu inn **10** sem magnið.</span><span class="sxs-lookup"><span data-stu-id="f2e80-211">Add a line for the new item, and enter **10** as the quantity.</span></span> <span data-ttu-id="f2e80-212">Gangið úr skugga um að reiturinn **Vöruhús** er stillt á **24**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-212">Make sure that the **Warehouse** field is set to **24**.</span></span>
5. <span data-ttu-id="f2e80-213">Á flýtiflipanum **Sölupöntunarlínur**, veldu **Birgðir** og síðan, í hópnum **Viðhalda**, veldu **Hópapöntun**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-213">On the **Sales order lines** FastTab, select **Inventory**, and then, in the **Maintain** group, select **Batch reservation**.</span></span> <span data-ttu-id="f2e80-214">Síðan **Hópapöntun** sýnir lista yfir lotur sem hægt er að panta fyrir pöntunarlínuna.</span><span class="sxs-lookup"><span data-stu-id="f2e80-214">The **Batch reservation** page shows a list of batches that are available for reservation for the order line.</span></span> <span data-ttu-id="f2e80-215">Fyrir þetta dæmi sýnir það magn af **20** fyrir lotunúmer **B11** og magn af **10** fyrir lotunúmer **B22**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-215">For this example, it shows a quantity of **20** for batch number **B11** and a quantity of **10** for batch number **B22**.</span></span> <span data-ttu-id="f2e80-216">Athugaðu að síðuna **Frátekt á runu** er ekki hægt að opna úr línu ef varan í þeirri línu tengist frátekningarstigveldinu *Runa fyrir neðan\[staðsetningu\]* nema hún sé sett upp til að leyfa runumiðaða frátekningu.</span><span class="sxs-lookup"><span data-stu-id="f2e80-216">Note that the **Batch reservation** page cannot be accessed from a line if the item on that line is associated with *Batch-below\[location\]* reservation hierarchy unless it is set up to allow batch-specific reservation.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f2e80-217">Til að panta ákveðna lotu fyrir sölupöntun verður þú að nota síðuna **Hópapöntun**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-217">To reserve a specific batch for a sales order, you must use the **Batch reservation** page.</span></span>
    >
    > <span data-ttu-id="f2e80-218">Ef rununúmerið er slegið beint inn í sölupöntunarlínuna mun kerfið taka því eins og þú hafir slegið inn sérstakt runugildi fyrir vörur sem heyrir undir frátekningarregluna *Runa fyrir neðan\[staðsetningu\]*.</span><span class="sxs-lookup"><span data-stu-id="f2e80-218">If you enter the batch number directly on the sales order line, the system will behave as though you entered a specific batch value for an item that is subject to the *Batch-below\[location\]* reservation policy.</span></span> <span data-ttu-id="f2e80-219">Þegar þú vistar línuna færðu viðvörunarskilaboð.</span><span class="sxs-lookup"><span data-stu-id="f2e80-219">When you save the line, you will receive a warning message.</span></span> <span data-ttu-id="f2e80-220">Ef þú staðfestir að tilgreina skuli lotunúmerið beint á pöntunarlínunni verður línan ekki meðhöndluð samkvæmt reglulegri vörugeymslu stjórnunar.</span><span class="sxs-lookup"><span data-stu-id="f2e80-220">If you confirm that the batch number should be specified directly on the order line, the line won't be handled by the regular warehouse management logic.</span></span>
    >
    > <span data-ttu-id="f2e80-221">Ef magnið er frátekið á síðunni **Frátekning** verður engin sérstök runa tekin frá og framkvæmd vöruhúsaaðgerða fyrir línuna mun fylgja reglunum sem heyra undir frátekningarregluna *Runa fyrir neðan\[staðsetningu\]*.</span><span class="sxs-lookup"><span data-stu-id="f2e80-221">If you reserve the quantity from the **Reservation** page, no specific batch will be reserved, and the execution of warehouse operations for the line will follow the rules that are applicable under the *Batch-below\[location\]* reservation policy.</span></span>

    <span data-ttu-id="f2e80-222">Almennt séð virkar þessi síða og er notuð á sama hátt og fyrir vörur sem eru með tengt frátekningarstigveldi af gerðinni *Runa fyrir ofan\[staðsetningu\]*.</span><span class="sxs-lookup"><span data-stu-id="f2e80-222">In general, this page works and is interacted with in the same way for items that have an associated reservation hierarchy of the *Batch-above\[location\]* type.</span></span> <span data-ttu-id="f2e80-223">Eftirfarandi undantekningar eiga þó við:</span><span class="sxs-lookup"><span data-stu-id="f2e80-223">However, the following exceptions apply:</span></span>

    - <span data-ttu-id="f2e80-224">Flýtiflipinn **Hópatölur skuldbundnar til upprunalínu** sýnir lotunúmerin sem eru frátekin fyrir pöntunarlínuna.</span><span class="sxs-lookup"><span data-stu-id="f2e80-224">The **Batch numbers committed to source line** FastTab shows the batch numbers that are reserved for the order line.</span></span> <span data-ttu-id="f2e80-225">Runugildin í hnitanetinu verða sýnd í gegnum allan uppfyllingartíma pöntunarlínunnar, þar á meðal stig vöruhúsavinnslunnar.</span><span class="sxs-lookup"><span data-stu-id="f2e80-225">The batch values in the grid will be shown throughout the fulfillment cycle of the order line, including the warehouse processing stages.</span></span> <span data-ttu-id="f2e80-226">Aftur á móti, á flýtiflipanum **Yfirlit**, venjulegur pöntunarlínupöntun (það er fyrirvari sem er gerður fyrir málin fyrir ofan **Staðsetning** stig) er sýnt í töflunni upp að því marki þegar vörugeymsla er búin til.</span><span class="sxs-lookup"><span data-stu-id="f2e80-226">By contrast, on the **Overview** FastTab, regular order line reservation (that is, reservation that is done for the dimensions above the **Location** level) is shown in the grid up to the point when warehouse work is created.</span></span> <span data-ttu-id="f2e80-227">Vinnuaðilinn tekur svo við línupöntuninni og línupöntunin birtist ekki lengur á síðunni.</span><span class="sxs-lookup"><span data-stu-id="f2e80-227">The work entity then takes over the line reservation, and the line reservation no longer appears on the page.</span></span> <span data-ttu-id="f2e80-228">Flýtiflipinn **Hópatölur skuldbundnar til upprunalínu** hjálpar til við að ábyrgjast að sölupöntunaraðili getur skoðað lotunúmerin sem voru skuldbundin pöntun viðskiptavinarins hvenær sem er á líftíma hans, upp í gegnum reikninga.</span><span class="sxs-lookup"><span data-stu-id="f2e80-228">The **Batch numbers committed to source line** FastTab helps guarantee that the sales order processor can view the batch numbers that were committed to the customer's order at any point during its lifecycle, up through invoicing.</span></span>
    - <span data-ttu-id="f2e80-229">Auk þess að panta sértæka lotu getur notandi valið handvirkt sértækan stað og framleiðslueiningar plötunnar í stað þess að láta kerfið velja þá sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="f2e80-229">In addition to reserving a specific batch, a user can manually select the batch's specific location and license plate instead of letting the system automatically select them.</span></span> <span data-ttu-id="f2e80-230">Þessi hæfileiki tengist hönnun pöntunarbundins fyrirkomulags fyrir pöntun.</span><span class="sxs-lookup"><span data-stu-id="f2e80-230">This capability is related to the design of the order-committed batch reservation mechanism.</span></span> <span data-ttu-id="f2e80-231">Eins og minnst var á hér á undan, þegar rununúmer er tekið frá fyrir vöru samkvæmt frátekningarreglunni *Runa fyrir neðan\[staðsetningu\]* verður kerfið að taka frá allar víddir upp í gegnum staðsetninguna.</span><span class="sxs-lookup"><span data-stu-id="f2e80-231">As was mentioned earlier, when a batch number is reserved for an item under the *Batch-below\[location\]* reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="f2e80-232">Þess vegna mun vörugeymsla hafa sömu geymsluvíddir og notendurnir sem unnu með pantanirnar áskildu og það gæti ekki alltaf táknað geymslu hlutarins sem er þægilegt eða jafnvel mögulegt fyrir tínaaðgerðir.</span><span class="sxs-lookup"><span data-stu-id="f2e80-232">Therefore, warehouse work will carry the same storage dimensions that were reserved by the users who worked with the orders, and it might not always represent the item storage placement that is convenient, or even possible, for picking operations.</span></span> <span data-ttu-id="f2e80-233">Ef pöntunaraðilar eru meðvitaðir um takmarkanir vörugeymslu, gætu þeir viljað handvirkt velja tiltekna staði og leyfismerki þegar þeir panta hóp.</span><span class="sxs-lookup"><span data-stu-id="f2e80-233">If order processors are aware of the warehouse constraints, they might want to manually select the specific locations and license plates when they reserve a batch.</span></span> <span data-ttu-id="f2e80-234">Í þessu tilfelli verður notandinn að nota **Sýna mál** virkni á síðuhausnum og verður að bæta við staðsetningu og kennitala í ristina á flýtiflipanum **Yfirlit**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-234">In this case, the user must use the **Display dimensions** functionality on the page header, and must add the location and license plate in the grid on the **Overview** FastTab.</span></span>

6. <span data-ttu-id="f2e80-235">Á **Hópapöntun** síðu, veldu línuna fyrir hópinn **B11** og veldu síðan **Varalína**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-235">On the **Batch reservation** page, select the line for batch **B11**, and then select **Reserve line**.</span></span> <span data-ttu-id="f2e80-236">Það er engin tiltekin rökfræði til að úthluta staðsetningum og skiltum við sjálfvirka fyrirvara.</span><span class="sxs-lookup"><span data-stu-id="f2e80-236">There is no designated logic for assigning locations and license plates during automatic reservation.</span></span> <span data-ttu-id="f2e80-237">Þú getur slegið inn magnið handvirkt í reitinn **Frátekning**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-237">You can manually enter the quantity in the **Reservation** field.</span></span> <span data-ttu-id="f2e80-238">Taktu eftir því að á flýtiflipanum **Hópatölur skuldbundnar til upprunalínu**, hópur **B11** er sýnt sem **Skuldbundinn**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-238">Notice that, on the **Batch numbers committed to source line** FastTab, batch **B11** is shown as **Committed**.</span></span>

    ![Að fremja ákveðið lotunúmer í sölupöntunarlínu á síðu síðu frátektar á runu](media/Batch-reservation-form-with-order-committed-reservation.png)

    > [!NOTE]
    > <span data-ttu-id="f2e80-240">Bókun magns á sölupöntunarlínu er hægt að gera í mörgum lotum.</span><span class="sxs-lookup"><span data-stu-id="f2e80-240">Reservation of the quantity on a sales order line can be done across multiple batches.</span></span> <span data-ttu-id="f2e80-241">Sömuleiðis er hægt að panta sömu lotu gagnvart mörgum stöðum og skiltum (ef leyfisplötur eru virkar fyrir staðina).</span><span class="sxs-lookup"><span data-stu-id="f2e80-241">Likewise, reservation of the same batch can be done against multiple locations and license plates (if license plates are enabled for the locations).</span></span>
    >
    > <span data-ttu-id="f2e80-242">Pöntun á tiltekinni lotu fyrir magnið á sölupöntunarlínu getur einnig verið að hluta.</span><span class="sxs-lookup"><span data-stu-id="f2e80-242">Reservation of a specific batch for the quantity on a sales order line can also be partial.</span></span> <span data-ttu-id="f2e80-243">Til dæmis er hægt að panta heildarmagn 100 eininga þannig að ákveðin lota er skuldbundin til 20 eininga en 80 einingar eru fráteknar á staðnum og vörugeymslustigi fyrir alla tiltæka lotu.</span><span class="sxs-lookup"><span data-stu-id="f2e80-243">For example, the total quantity of 100 units can be reserved so that a specific batch is committed to 20 units, whereas 80 units are reserved at the site and warehouse levels for any available batch.</span></span> <span data-ttu-id="f2e80-244">Í þessu tilfelli mun WMS sjá um tínaaðgerðir með því að nota tvær aðskildar vinnulínur.</span><span class="sxs-lookup"><span data-stu-id="f2e80-244">In this case, the WMS will handle picking operations by using two separate work lines.</span></span>

7. <span data-ttu-id="f2e80-245">Farðu í **Afurðaupplýsingastjórnun** \> **Afurðir** \> **Losaðar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-245">Go to **Product information management** \> **Products** \> **Released products**.</span></span> <span data-ttu-id="f2e80-246">Veldu hlutinn þinn og veldu síðan **Stjórna birgðum** \> **Skoða** \> **Færslur**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-246">Select your item, and then select **Manage inventory** \> **View** \> **Transactions**.</span></span>

    ![Pöntunarbundin fyrirvara sem birgðafærslugerð](media/Inventory-transactions-for-order-committed-reservation.png)

8. <span data-ttu-id="f2e80-248">Skoðaðu birgðafærslur hlutarins sem tengjast pöntun sölupöntunarlínunnar.</span><span class="sxs-lookup"><span data-stu-id="f2e80-248">Review the item's inventory transactions that are related to the sales order line reservation.</span></span>

    - <span data-ttu-id="f2e80-249">Viðskipti þar sem **Tilvísun** reiturinn er stilltur á **Sölupöntun** og **Mál** reiturinn er stilltur á **Frátekin líkamleg** táknar pöntunarlínu fyrirvara fyrir birgðavíddir fyrir ofan **Staðsetning** stigi.</span><span class="sxs-lookup"><span data-stu-id="f2e80-249">A transaction where the **Reference** field is set to **Sales order** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the inventory dimensions above the **Location** level.</span></span> <span data-ttu-id="f2e80-250">Samkvæmt stigveldi birgðapöntunar hlutanna eru þessar víddir staða, vörugeymsla og birgðastaða.</span><span class="sxs-lookup"><span data-stu-id="f2e80-250">According to the item's inventory reservation hierarchy, those dimensions are site, warehouse, and inventory status.</span></span>
    - <span data-ttu-id="f2e80-251">Viðskipti þar sem reiturinn **Tilvísun** er stilltur á **Pöntunarbundna frátekt** og reiturinn **Úthreyfing** er stilltur á **Frátekið á lager** táknar pöntunarlínu frátektar fyrir tiltekna runu og annar birgðavíddir fyrir ofan hana.</span><span class="sxs-lookup"><span data-stu-id="f2e80-251">A transaction where the **Reference** field is set to **Order-committed reservation** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the specific batch and all inventory dimensions above it.</span></span> <span data-ttu-id="f2e80-252">Samkvæmt stigveldi birgðapöntunar hlutanna eru þessar víddir rununúmer og staðsetning.</span><span class="sxs-lookup"><span data-stu-id="f2e80-252">According to the item's inventory reservation hierarchy, those dimensions are batch number and location.</span></span> <span data-ttu-id="f2e80-253">Í þessu dæmi er staðsetningin **Magn-001**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-253">In this example, the location is **Bulk-001**.</span></span>

9. <span data-ttu-id="f2e80-254">Veldu á sölupöntunarhaus **Vöruhús** \> **Aðgerðir** \> **Losa í vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-254">On the sales order header, select **Warehouse** \> **Actions** \> **Release to warehouse**.</span></span> <span data-ttu-id="f2e80-255">Pöntunarlínan hefur verið sett í bylgju og álag og vinna búin til.</span><span class="sxs-lookup"><span data-stu-id="f2e80-255">The order line is now waved, and a load and work are created.</span></span>

### <a name="review-and-process-warehouse-work-that-has-order-committed-batch-numbers"></a><span data-ttu-id="f2e80-256">Farið yfir og unnið úr vöruhúsagerð sem er með pöntunarbundna lotunúmer</span><span class="sxs-lookup"><span data-stu-id="f2e80-256">Review and process warehouse work that has order-committed batch numbers</span></span>

1. <span data-ttu-id="f2e80-257">Á flýtiflipanum **Sölupöntunarlínur**, veldu **Vöruhús** \> **Upplýsingar um vinnu**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-257">On the **Sales order lines** FastTab, select **Warehouse** \> **Work details**.</span></span>

    <span data-ttu-id="f2e80-258">Vinnan sem annast tínsluaðgerðina fyrir magn magn sem skuldbundið sig til sölupöntunarlínunnar hefur eftirfarandi einkenni:</span><span class="sxs-lookup"><span data-stu-id="f2e80-258">The work that handles the picking operation for batch quantities that are committed to the sales order line has the following characteristics:</span></span>

    - <span data-ttu-id="f2e80-259">Til að búa til vinnu notar kerfið vinnusniðmát en ekki staðsetningartilskipanir.</span><span class="sxs-lookup"><span data-stu-id="f2e80-259">To create work, the system uses work templates but not location directives.</span></span> <span data-ttu-id="f2e80-260">Öllum stöðluðum stillingum sem eru skilgreindar fyrir vinnusniðmát, svo sem hámarksfjölda vallína eða ákveðin mælieining, verður beitt til að ákvarða hvenær ný vinna ætti að búa til.</span><span class="sxs-lookup"><span data-stu-id="f2e80-260">All the standard settings that are defined for work templates, such as a maximum number of pick lines or a specific unit of measure, will be applied to determine when new work should be created.</span></span> <span data-ttu-id="f2e80-261">Hins vegar er ekki tekið tillit til reglnanna sem eru tengdar staðsetningarleiðbeiningum til að bera kennsl á valstöðum, vegna þess að pöntunin sem framin er fyrir pöntunin tilgreinir þegar allar birgðarvíddirnar.</span><span class="sxs-lookup"><span data-stu-id="f2e80-261">However, the rules that are associated with location directives for identifying pick locations aren't considered, because the order-committed reservation already specifies all the inventory dimensions.</span></span> <span data-ttu-id="f2e80-262">Þessar birgðastærðir innihalda mál á lagergeymslu stigsins.</span><span class="sxs-lookup"><span data-stu-id="f2e80-262">Those inventory dimensions include the dimensions at the warehouse storage level.</span></span> <span data-ttu-id="f2e80-263">Þess vegna erfðir verkið þessar víddir án þess að þurfa að hafa samráð um staðsetningartilskipanir.</span><span class="sxs-lookup"><span data-stu-id="f2e80-263">Therefore, the work inherits those dimensions without having to consult location directives.</span></span>
    - <span data-ttu-id="f2e80-264">Lotunúmerið er ekki sýnt í tiltektarlínunni (eins og er gert fyrir vinnulínuna sem er stofnuð fyrir vöru sem er með tengt frátekningarstigveldi *Runa fyrir ofan\[staðsetningu\]*.) Í staðinn eru „frá“ rununúmerið og allar aðrar geymsluvíddir sýndar í birgðafærsluvinnu vinnulínunnar sem vísar er í úr tengdum birgðafærslum.</span><span class="sxs-lookup"><span data-stu-id="f2e80-264">The batch number isn't shown on the pick line (as is the case for the work line that is created for an item that has an associated *Batch-above\[location\]* reservation hierarchy.) Instead, the "from" batch number and all other storage dimensions are shown on the work line's work inventory transaction that is referenced from the associated inventory transactions.</span></span>

        ![Vörugeymslufærsla vegna vinnu sem er upprunnin í pöntunarbundinni frátekt](media/Work-inventory-transactions-for-order-committed-reservation.png)

    - <span data-ttu-id="f2e80-266">Eftir að vinna er búin til, birgðir hlutarins þar sem **Tilvísun** reiturinn er stilltur á **Pöntunarbundin frátekt** er fjarlægður.</span><span class="sxs-lookup"><span data-stu-id="f2e80-266">After work is created, the item's inventory transaction where the **Reference** field is set to **Order-committed reservation** is removed.</span></span> <span data-ttu-id="f2e80-267">Birgðafærslan þar sem **Tilvísun** reiturinn er stilltur á **Vinna** geymir nú líkamlegan fyrirvara á öllum birgðastærðum magnsins.</span><span class="sxs-lookup"><span data-stu-id="f2e80-267">The inventory transaction where the **Reference** field is set to **Work** now holds the physical reservation on all the quantity's inventory dimensions.</span></span>

        <span data-ttu-id="f2e80-268">Vöruhúsaaðgerðir geta haldið áfram til að sjá um framkvæmd verksins á venjulegan hátt.</span><span class="sxs-lookup"><span data-stu-id="f2e80-268">Warehouse operations can proceed to handle execution of the work in the usual manner.</span></span> <span data-ttu-id="f2e80-269">Leiðbeiningarnar í farsímanum munu hins vegar leiðbeina starfsmanni að velja ákveðið lotunúmer.</span><span class="sxs-lookup"><span data-stu-id="f2e80-269">However, the instructions on the mobile device will instruct the worker to pick a specific batch number.</span></span> <span data-ttu-id="f2e80-270">Í vöruhúsaumhverfum þar sem staðsetningar eru númeraplötustýrðar, eftir að starfsmaður kemur á staðsetningu sem geymir rununa á mörgum númeraplötum, getur hann valið úr einhverri númeraplötu sem ekki er þegar frátekin (til dæmis með annarri frátekningu á ráðstafaðri pöntun eða vinnu sem verður til út frá frátekningu að þessari gerð.)</span><span class="sxs-lookup"><span data-stu-id="f2e80-270">In warehouse environments where locations are license plate–controlled, after a worker reaches a location that stores the same batch on multiple license plates, they can pick from any license plate that isn't already reserved (for example, by another order-committed reservation or work that originates from a reservation of that type.)</span></span>

        <span data-ttu-id="f2e80-271">Ef það reynist óframkvæmanlegt að velja frá þeim stað sem er tilgreindur á vinnulínunni geta rekstraraðilar vörugeymslu notað eina af eftirfarandi aðgerðum til að beina því að velja ákveðna lotu frá þægilegri stað:</span><span class="sxs-lookup"><span data-stu-id="f2e80-271">If it turns out to be impractical to pick from the location that is specified on the work line, the warehouse operators can use one of the following actions to redirect picking of the specific batch from a more convenient location:</span></span>

        - <span data-ttu-id="f2e80-272">Staðallinn **Hnekkja staðsetningu** aðgerð í farsíma (að því tilskildu að starfsmaður vörugeymslu **Leyfa val á staðsetningu staðsetningu** stilling er virk)</span><span class="sxs-lookup"><span data-stu-id="f2e80-272">The standard **Override location** action on a mobile device (provided that the warehouse worker's **Allow pick location override** setting is enabled)</span></span>
        - <span data-ttu-id="f2e80-273">Aðgerðin **Breyta staðsetningu** á **Upplýsingar um vinnulista** síðu.</span><span class="sxs-lookup"><span data-stu-id="f2e80-273">The **Change location** action on the **Work list details** page.</span></span> 

2. <span data-ttu-id="f2e80-274">Ljúktu við að velja og setja verkið í farsímann.</span><span class="sxs-lookup"><span data-stu-id="f2e80-274">On the mobile device, finish picking and putting the work.</span></span>

    <span data-ttu-id="f2e80-275">Magnið **10** fyrir lotunúmer **B11** er nú valinn í sölupöntunarlínuna og settur í **Afgreiðsluhurð** staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="f2e80-275">The quantity of **10** for batch number **B11** is now picked for the sales order line and put in the **Baydoor** location.</span></span> <span data-ttu-id="f2e80-276">Á þessum tímapunkti er það tilbúið að hlaða það á vörubílinn og senda á heimilisfang viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="f2e80-276">At this point, it's ready to be loaded onto the truck and dispatched to the customer's address.</span></span>

## <a name="flexible-license-plate-reservation"></a><span data-ttu-id="f2e80-277">Sveigjanleg frátekning númeraplötu</span><span class="sxs-lookup"><span data-stu-id="f2e80-277">Flexible license plate reservation</span></span>

### <a name="business-scenario"></a><span data-ttu-id="f2e80-278">Sviðsmynd fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="f2e80-278">Business scenario</span></span>

<span data-ttu-id="f2e80-279">Í þessum aðstæðum notar fyrirtæki vöruhúsakerfi og vinnuferli og sér um hleðsluáætlun á stigi einstakra bretta/gáma utan Supply Chain Management áður en vinna er stofnuð.</span><span class="sxs-lookup"><span data-stu-id="f2e80-279">In this scenario, a company uses warehouse management and work processing, and handles load planning at the level of individual pallets/containers outside Supply Chain Management before work is created.</span></span> <span data-ttu-id="f2e80-280">Þessir gámar eru táknaðir með númeraplötum í birgðavíddunum.</span><span class="sxs-lookup"><span data-stu-id="f2e80-280">These containers are represented by license plates in the inventory dimensions.</span></span> <span data-ttu-id="f2e80-281">Fyrir þessa nálgun þarf þar af leiðandi að úthluta sérstökum númeraplötum fyrirfram á sölupöntunarlínur áður en tiltekt er gerð.</span><span class="sxs-lookup"><span data-stu-id="f2e80-281">Therefore, for this approach, specific license plates must be pre-assigned to sales order lines before picking work is done.</span></span> <span data-ttu-id="f2e80-282">Fyrirtækið leitar að sveigjanleika í því hvernig reglur um frátekningu númeraplötu eru meðhöndlaðar, þannig að eftirfarandi hegðun eigi sér stað:</span><span class="sxs-lookup"><span data-stu-id="f2e80-282">The company is looking for flexibility in the way that the license plate reservation rules are handled, so that the following behaviors occur:</span></span>

- <span data-ttu-id="f2e80-283">Hægt er að skrá og taka frá númeraplötu þegar pöntunin er tekin af úrvinnsluaðila sölumála og ekki er hægt að taka hana af öðrum eftirspurnum.</span><span class="sxs-lookup"><span data-stu-id="f2e80-283">A license plate can be recorded and reserved when the order is taken by the sales processor, and it can't be taken by other demands.</span></span> <span data-ttu-id="f2e80-284">Þessi hegðun hjálpar til við að tryggja að númeraplatan sem var áætluð sé send til viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="f2e80-284">This behavior helps guarantee that the license plate that was planned is shipped to the customer.</span></span>
- <span data-ttu-id="f2e80-285">Ef númeraplötunni hefur ekki þegar verið úthlutað á sölupöntunarlínu, getur starfsmaður í vöruhúsi valið númeraplötu meðan á tiltekt stendur, þegar búið er að ljúka skráningu sölupöntunar og frátekningu.</span><span class="sxs-lookup"><span data-stu-id="f2e80-285">If the license plate isn't already assigned to a sales order line, warehouse personnel can select a license plate during picking work, after sales order registration and reservation are completed.</span></span>

### <a name="turn-on-flexible-license-plate-reservation"></a><span data-ttu-id="f2e80-286">Kveikja á sveigjanlegri frátekningu númeraplötu</span><span class="sxs-lookup"><span data-stu-id="f2e80-286">Turn on flexible license plate reservation</span></span>

<span data-ttu-id="f2e80-287">Áður en hægt er að nota sveigjanlega frátekningu númeraplötu, þarf að kveikja á tveimur eiginleikum í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="f2e80-287">Before you can use flexible license plate reservation, two features must be turned on in your system.</span></span> <span data-ttu-id="f2e80-288">Stjórnendur geta notað stillingar [eiginleikastjórnunar](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikanna og kveikja á þeim ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="f2e80-288">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the features and turn them on if they are required.</span></span> <span data-ttu-id="f2e80-289">Kveikja verður á eiginleikunum í eftirfarandi röð:</span><span class="sxs-lookup"><span data-stu-id="f2e80-289">You must turn on the features in the following order:</span></span>

1. <span data-ttu-id="f2e80-290">**Heiti eiginleika:** *Sveigjanleg frátekt á vídd vöruhúsastigs*</span><span class="sxs-lookup"><span data-stu-id="f2e80-290">**Feature name:** *Flexible warehouse-level dimension reservation*</span></span>
1. <span data-ttu-id="f2e80-291">**Heiti eiginleika:** *Sveigjanleg frátekt á númeraplötu ráðstafaðrar pöntunar*</span><span class="sxs-lookup"><span data-stu-id="f2e80-291">**Feature name:** *Flexible order-committed license plate reservation*</span></span>

### <a name="reserve-a-specific-license-plate-on-the-sales-order"></a><span data-ttu-id="f2e80-292">Taka frá tiltekna númeraplötu í sölupöntuninni</span><span class="sxs-lookup"><span data-stu-id="f2e80-292">Reserve a specific license plate on the sales order</span></span>

<span data-ttu-id="f2e80-293">Til að virkja frátekningu á númeraplötu í pöntun þarf að velja gátreitinn **Leyfa frátekt á eftirspurnarpöntun** fyrir stigið **Númeraplata** á síðunni **Frátekningarstigveldi birgða** fyrir stigveldið sem tengist viðkomandi vöru.</span><span class="sxs-lookup"><span data-stu-id="f2e80-293">To enable license plate reservation on an order, you must select the **Allow reservation on demand order** check box for the **License plate** level on the **Inventory reservation hierarchies** page for the hierarchy that is associated with the relevant item.</span></span>

![Síða frátekningarstigveldis birgða fyrir frátekningarstigveldi sveigjanlegrar númeraplötu](media/Flexible-LP-reservation-hierarchy.png)

<span data-ttu-id="f2e80-295">Hægt er að virkja frátekningu á númeraplötu í pöntuninni hvenær sem er í uppsetningunni.</span><span class="sxs-lookup"><span data-stu-id="f2e80-295">You can enable license plate reservation on the order at any point in your deployment.</span></span> <span data-ttu-id="f2e80-296">Þessi breyting hefur ekki áhrif á neinar frátekningar eða opna vöruhúsavinnu sem var stofnuð áður en breytingin var gerð.</span><span class="sxs-lookup"><span data-stu-id="f2e80-296">This change won't affect any reservations or open warehouse work that were created before the change occurred.</span></span> <span data-ttu-id="f2e80-297">Hins vegar er ekki hægt að hreinsa gátreitinn **Leyfa frátekt á eftirspurnarpöntun** ef opnar birgðafærslur á útleið sem eru með úthreyfingarstöðuna *Í pöntun*, *Frátekið pantað* eða *Frátekið efnislegt magn* eru til fyrir eina eða fleiri vörur sem tengjast þessu frátekningarstigveldi.</span><span class="sxs-lookup"><span data-stu-id="f2e80-297">However, you can't clear the **Allow reservation on demand order** check box if open outbound inventory transactions that have an issue status of *On order*, *Reserved ordered*, or *Reserved physical* exist for one or more items that are associated with that reservation hierarchy.</span></span>

<span data-ttu-id="f2e80-298">Jafnvel ef gátreiturinn **Leyfa frátekt á eftirspurnarpöntun** er valinn fyrir stigið **Númeraplata** er enn mögulegt að *ekki* taka frá tiltekna númeraplötu í pöntuninni.</span><span class="sxs-lookup"><span data-stu-id="f2e80-298">Even if the **Allow reservation on demand order** check box is selected for the **License plate** level, it's still possible *not* to reserve a specific license plate on the order.</span></span> <span data-ttu-id="f2e80-299">Í slíku tilfelli gilda sjálfgefin rök vöruhúsaaðgerða fyrir frátekningarstigveldið.</span><span class="sxs-lookup"><span data-stu-id="f2e80-299">In this case, the default warehouse operations logic that is valid for the reservation hierarchy applies.</span></span>

<span data-ttu-id="f2e80-300">Til að taka frá tiltekna númeraplötu þarf að nota [OData-ferli](../../fin-ops-core/dev-itpro/data-entities/odata.md).</span><span class="sxs-lookup"><span data-stu-id="f2e80-300">To reserve a specific license plate, you must use an [Open Data Protocol (OData)](../../fin-ops-core/dev-itpro/data-entities/odata.md) process.</span></span> <span data-ttu-id="f2e80-301">Í forritinu er hægt að gera þessa frátekningu beint úr sölupöntun með því að nota valkostinn **Frátektir á ráðstöfuðum pöntunum eftir númeraplötu** fyrir skipunina **Opna í Excel**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-301">In the application, you can do this reservation directly from a sales order by using the **Order-committed reservations per license plate** option of the **Open in Excel** command.</span></span> <span data-ttu-id="f2e80-302">Í einingagögnunum sem opnuð eru í Excel-innbótinni þarf að færa inn eftirfarandi frátektartengd gögn og síðan velja **Birta** til að senda gögnin aftur í Supply Chain Management:</span><span class="sxs-lookup"><span data-stu-id="f2e80-302">In the entity data that is opened in the Excel add-in, you must enter the following reservation-related data and then select **Publish** to send the data back to Supply Chain Management:</span></span>

- <span data-ttu-id="f2e80-303">Tilvísun (eingöngu gildið *Sölupöntun* er stutt.)</span><span class="sxs-lookup"><span data-stu-id="f2e80-303">Reference (Only the *Sales order* value is supported.)</span></span>
- <span data-ttu-id="f2e80-304">Pöntunarnúmer (gildið er hægt að fá úr lotu.)</span><span class="sxs-lookup"><span data-stu-id="f2e80-304">Order number (The value can be derived from the lot.)</span></span>
- <span data-ttu-id="f2e80-305">Lotukenni</span><span class="sxs-lookup"><span data-stu-id="f2e80-305">Lot ID</span></span>
- <span data-ttu-id="f2e80-306">Númeraplata</span><span class="sxs-lookup"><span data-stu-id="f2e80-306">License plate</span></span>
- <span data-ttu-id="f2e80-307">Magn</span><span class="sxs-lookup"><span data-stu-id="f2e80-307">Quantity</span></span>

<span data-ttu-id="f2e80-308">Ef taka þarf frá tiltekna númeraplötu fyrir runurakta vöru skal nota síðuna **Frátekt á runu**, eins og lýst er í hlutanum [Færa inn upplýsingar um sölupöntun](#sales-order-details).</span><span class="sxs-lookup"><span data-stu-id="f2e80-308">If you must reserve a specific license plate for a batch-tracked item, use the **Batch reservation** page, as described in the [Enter sales order details](#sales-order-details) section.</span></span>

<span data-ttu-id="f2e80-309">Þegar sölupöntunarlína sem notar frátekt á númeraplötu ráðstafaðrar pöntunar er unnin af vöruhúsaaðgerðum, eru staðsetningarleiðbeiningar ekki notaðar.</span><span class="sxs-lookup"><span data-stu-id="f2e80-309">When the sales order line that uses an order-committed license plate reservation is processed by warehouse operations, location directives aren't used.</span></span>

<span data-ttu-id="f2e80-310">Ef vinnuliður vöruhúss samanstendur af línum sem jafngilda heilu bretti og eru með númeraplöturáðstafað magn, er hægt að fínstilla tiltektina með því að nota valmyndaratriði fartækis þar sem valkosturinn **Meðhöndla eftir númeraplötu** er stilltur á *Já*.</span><span class="sxs-lookup"><span data-stu-id="f2e80-310">If a warehouse work item consists of lines that equal a complete pallet and have license plate–committed quantities, you can optimize the picking process by using a mobile device menu item where the **Handle by license plate** option is set to *Yes*.</span></span> <span data-ttu-id="f2e80-311">Starfsmaður í vöruhúsi getur síðan skannað númeraplötu til að ljúka tiltekt í stað þess að þurfa að skanna vörurnar úr vinnunni hver á eftir annarri.</span><span class="sxs-lookup"><span data-stu-id="f2e80-311">A warehouse worker can then scan a license plate to complete a pick instead of having to scan the items from the work one by one.</span></span>

![Valmyndaratriði fartækis þar sem valkosturinn „Meðhöndla eftir númeraplötu" er stilltur á „Já“](media/Handle-by-LP-menu-item.png)

<span data-ttu-id="f2e80-313">Vegna þess að virknin **Meðhöndla eftir númeraplötu** styður ekki vinnu sem nær yfir mörg bretti, er betra að vera með aðskilinn vinnulið fyrir mismunandi númeraplötur.</span><span class="sxs-lookup"><span data-stu-id="f2e80-313">Because the **Handle by license plate** functionality doesn't support work that covers multiple pallets, it's better to have a separate work item for different license plates.</span></span> <span data-ttu-id="f2e80-314">Til að nota þessa aðferð skal bæta reitnum **Númeraplötukenni ráðstafaðrar pöntunar** sem vinnuhausaskil á síðunni **Vinnusniðmát**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-314">To use this approach, add the **Order-committed license plate ID** field as a work header break on the **Work template** page.</span></span>

> [!NOTE]
> <span data-ttu-id="f2e80-315">Fyrir stofnferli á vinnu ráðstafaðrar pöntunar, verður gildinu „birgðavíddir ráðstafaðrar pöntunar“ úthlutað á vinnulínur tiltektar og ekki verið mögulegt að skoða gildið á númeraplötunni með beinum hætti.</span><span class="sxs-lookup"><span data-stu-id="f2e80-315">For the order-committed work creation process, an "order-committed inventory dimension" value will be assigned to the picking work lines, and it won't be possible to view the license plate value directly.</span></span> <span data-ttu-id="f2e80-316">Aðeins *Notandastýrt* ferli er stutt þegar valmyndaratriði fartækis er sett upp.</span><span class="sxs-lookup"><span data-stu-id="f2e80-316">Only the *User directed* process is supported when setting up a mobile device menu item.</span></span>

## <a name="example-scenario-set-up-and-process-an-order-committed-license-plate-reservation"></a><span data-ttu-id="f2e80-317">Dæmi: Setja upp og vinna úr frátekt á númeraplötu ráðstafaðrar pöntunar</span><span class="sxs-lookup"><span data-stu-id="f2e80-317">Example scenario: Set up and process an order-committed license plate reservation</span></span>

<span data-ttu-id="f2e80-318">Þessi atburðarás sýnir hvernig á að setja upp og vinna úr frátekt á númeraplötu ráðstafaðrar pöntunar.</span><span class="sxs-lookup"><span data-stu-id="f2e80-318">This scenario shows how to set up and process an order-committed license plate reservation.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="f2e80-319">Bjóða upp á sýnigögn</span><span class="sxs-lookup"><span data-stu-id="f2e80-319">Make demo data available</span></span>

<span data-ttu-id="f2e80-320">Þessi atburðarás vísar í gildi og færslur sem eru innifalin í stöðluðum sýnigögnum sem boðið er upp á fyrir Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f2e80-320">This scenario refers to values and records that are included in the standard demo data that is provided for Supply Chain Management.</span></span> <span data-ttu-id="f2e80-321">Ef ætlunin er að fara í gegnum atburðarásina með því að nota gildin sem hér eru gefin skal gæta þess að vinna í umhverfi þar sem sýnigögnin eru uppsett.</span><span class="sxs-lookup"><span data-stu-id="f2e80-321">If you want to work through the scenario by using the values that are provided here, be sure to work on an environment where the demo data is installed.</span></span> <span data-ttu-id="f2e80-322">Þar að auki skal stilla lögaðilann á **USMF** áður en hafist er handa.</span><span class="sxs-lookup"><span data-stu-id="f2e80-322">Additionally, set the legal entity to **USMF** before you begin.</span></span>

### <a name="create-an-inventory-reservation-hierarchy-that-allows-for-license-plate-reservation"></a><span data-ttu-id="f2e80-323">Stofna frátekningarstigveldi birgða sem leyfir frátekningu á númeraplötu</span><span class="sxs-lookup"><span data-stu-id="f2e80-323">Create an inventory reservation hierarchy that allows for license plate reservation</span></span>

1. <span data-ttu-id="f2e80-324">Fara í **Vöruhúsakerfi \> Uppsetning \> Birgðir \> Frátekningarstigveldi**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-324">Go to **Warehouse management \> Setup \> Inventory \> Reservation hierarchy**.</span></span>
1. <span data-ttu-id="f2e80-325">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-325">Select **New**.</span></span>
1. <span data-ttu-id="f2e80-326">Í reitinn **Heiti** skal slá inn gildi (til dæmis *FlexibleLP*).</span><span class="sxs-lookup"><span data-stu-id="f2e80-326">In the **Name** field, enter a value (for example, *FlexibleLP*).</span></span>
1. <span data-ttu-id="f2e80-327">Í reitinn **Lýsing** skal færa inn gildi (til dæmis *Sveigjanleg frátekning á númeraplötu*).</span><span class="sxs-lookup"><span data-stu-id="f2e80-327">In the **Description** field, enter a value (for example, *Flexible LP reservation*).</span></span>
1. <span data-ttu-id="f2e80-328">Í listanum **Valið** skal velja **Rununúmer**, **Raðnúmer** og **Eigandi**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-328">In the **Selected** list, select **Batch number**, **Serial number**, and **Owner**.</span></span>
1. <span data-ttu-id="f2e80-329">Veljið hnappinn **Fjarlægja** ![ör til baka](media/backward-button.png) til að flytja valdar færslur í listann **Tiltækt**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-329">Select the **Remove** button ![backward arrow](media/backward-button.png) to move the selected records to the **Available** list.</span></span>
1. <span data-ttu-id="f2e80-330">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-330">Select **OK**.</span></span>
1. <span data-ttu-id="f2e80-331">Í línunni fyrir víddarstigið **Númeraplata** skal velja gátreitinn **Leyfa frátekt á eftirspurnarpöntun**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-331">In the row for the **License plate** dimension level, select the **Allow reservation on demand order** check box.</span></span> <span data-ttu-id="f2e80-332">Stigið **Staðsetning** er valið sjálfkrafa og ekki er hægt að hreinsa gátreitinn fyrir það.</span><span class="sxs-lookup"><span data-stu-id="f2e80-332">The **Location** level is automatically selected, and you can't clear the check box for it.</span></span>
1. <span data-ttu-id="f2e80-333">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-333">Select **Save**.</span></span>

### <a name="create-two-released-products"></a><span data-ttu-id="f2e80-334">Stofna tvær útgefnar afurðir</span><span class="sxs-lookup"><span data-stu-id="f2e80-334">Create two released products</span></span>

1. <span data-ttu-id="f2e80-335">Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-335">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="f2e80-336">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-336">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="f2e80-337">Í svarglugganum **Ný útgefin afurð** skal stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="f2e80-337">In the **New released product** dialog box, set the following values:</span></span>

    - <span data-ttu-id="f2e80-338">**Afurðarnúmer:** *Item1*</span><span class="sxs-lookup"><span data-stu-id="f2e80-338">**Product number:** *Item1*</span></span>
    - <span data-ttu-id="f2e80-339">**Vörunúmer:** *Item1*</span><span class="sxs-lookup"><span data-stu-id="f2e80-339">**Item number:** *Item1*</span></span>
    - <span data-ttu-id="f2e80-340">**Vörulíkanaflokkur:** *FIFO*</span><span class="sxs-lookup"><span data-stu-id="f2e80-340">**Item model group:** *FIFO*</span></span>
    - <span data-ttu-id="f2e80-341">**Vöruflokkur:** *Hljóð*</span><span class="sxs-lookup"><span data-stu-id="f2e80-341">**Item group:** *Audio*</span></span>
    - <span data-ttu-id="f2e80-342">**Geymsluvíddarflokkur:** *Afurð*</span><span class="sxs-lookup"><span data-stu-id="f2e80-342">**Storage dimension group:** *Ware*</span></span>
    - <span data-ttu-id="f2e80-343">**Rakningarvíddarflokkur:** *Enginn*</span><span class="sxs-lookup"><span data-stu-id="f2e80-343">**Tracking dimension group:** *None*</span></span>
    - <span data-ttu-id="f2e80-344">**Frátekningarstigveldi:** *FlexibleLP*</span><span class="sxs-lookup"><span data-stu-id="f2e80-344">**Reservation hierarchy:** *FlexibleLP*</span></span>

1. <span data-ttu-id="f2e80-345">Veljið **Í lagi** til að stofna afurðina og loka svarglugganum.</span><span class="sxs-lookup"><span data-stu-id="f2e80-345">Select **OK** to create the product and close the dialog box.</span></span>
1. <span data-ttu-id="f2e80-346">Nýja afurðin opnast.</span><span class="sxs-lookup"><span data-stu-id="f2e80-346">The new product is opened.</span></span> <span data-ttu-id="f2e80-347">Í flýtiflipanum **Vöruhús** skal stilla reitinn **Auðkenni röðunarflokks einingar** á *ea*.</span><span class="sxs-lookup"><span data-stu-id="f2e80-347">On the **Warehouse** FastTab, set the **Unit sequence group ID** field to *ea*.</span></span>
1. <span data-ttu-id="f2e80-348">Endurtakið fyrri skref til að stofna aðra afurð sem er með sömu stillingar, en stillið reitina **Afurðarnúmer** og **Vörunúmer** á *Item2*.</span><span class="sxs-lookup"><span data-stu-id="f2e80-348">Repeat the previous steps to create a second product that has the same settings, but set the **Product number** and **Item number** fields to *Item2*.</span></span>
1. <span data-ttu-id="f2e80-349">Á aðgerðasvæðinu, í flipanum **Stjórna birgðum**, í flokknum **Skoða**, skal velja **Lagerbirgðir**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-349">On the Action Pane, on the **Manage inventory** tab, in the **View** group, select **On-hand inventory**.</span></span> <span data-ttu-id="f2e80-350">Veljið síðan **Leiðrétting á magni**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-350">Then select **Quantity adjustment**.</span></span>
1. <span data-ttu-id="f2e80-351">Leiðréttið lagerbirgðir nýju varanna eins og tilgreint er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="f2e80-351">Adjust the on-hand inventory of the new items as specified in the following table.</span></span>

    | <span data-ttu-id="f2e80-352">vara</span><span class="sxs-lookup"><span data-stu-id="f2e80-352">Item</span></span>  | <span data-ttu-id="f2e80-353">Vöruhús</span><span class="sxs-lookup"><span data-stu-id="f2e80-353">Warehouse</span></span> | <span data-ttu-id="f2e80-354">Staður</span><span class="sxs-lookup"><span data-stu-id="f2e80-354">Location</span></span> | <span data-ttu-id="f2e80-355">Númeraplata</span><span class="sxs-lookup"><span data-stu-id="f2e80-355">License plate</span></span> | <span data-ttu-id="f2e80-356">Magn</span><span class="sxs-lookup"><span data-stu-id="f2e80-356">Quantity</span></span> |
    |-------|-----------|----------|---------------|----------|
    | <span data-ttu-id="f2e80-357">VARA1</span><span class="sxs-lookup"><span data-stu-id="f2e80-357">Item1</span></span> | <span data-ttu-id="f2e80-358">24</span><span class="sxs-lookup"><span data-stu-id="f2e80-358">24</span></span>        | <span data-ttu-id="f2e80-359">FL-010</span><span class="sxs-lookup"><span data-stu-id="f2e80-359">FL-010</span></span>   | <span data-ttu-id="f2e80-360">LP01</span><span class="sxs-lookup"><span data-stu-id="f2e80-360">LP01</span></span>          | <span data-ttu-id="f2e80-361">10</span><span class="sxs-lookup"><span data-stu-id="f2e80-361">10</span></span>       |
    | <span data-ttu-id="f2e80-362">VARA1</span><span class="sxs-lookup"><span data-stu-id="f2e80-362">Item1</span></span> | <span data-ttu-id="f2e80-363">24</span><span class="sxs-lookup"><span data-stu-id="f2e80-363">24</span></span>        | <span data-ttu-id="f2e80-364">FL-011</span><span class="sxs-lookup"><span data-stu-id="f2e80-364">FL-011</span></span>   | <span data-ttu-id="f2e80-365">LP02</span><span class="sxs-lookup"><span data-stu-id="f2e80-365">LP02</span></span>          | <span data-ttu-id="f2e80-366">10</span><span class="sxs-lookup"><span data-stu-id="f2e80-366">10</span></span>       |
    | <span data-ttu-id="f2e80-367">VARA2</span><span class="sxs-lookup"><span data-stu-id="f2e80-367">Item2</span></span> | <span data-ttu-id="f2e80-368">24</span><span class="sxs-lookup"><span data-stu-id="f2e80-368">24</span></span>        | <span data-ttu-id="f2e80-369">FL-010</span><span class="sxs-lookup"><span data-stu-id="f2e80-369">FL-010</span></span>   | <span data-ttu-id="f2e80-370">LP01</span><span class="sxs-lookup"><span data-stu-id="f2e80-370">LP01</span></span>          | <span data-ttu-id="f2e80-371">5</span><span class="sxs-lookup"><span data-stu-id="f2e80-371">5</span></span>        |
    | <span data-ttu-id="f2e80-372">VARA2</span><span class="sxs-lookup"><span data-stu-id="f2e80-372">Item2</span></span> | <span data-ttu-id="f2e80-373">24</span><span class="sxs-lookup"><span data-stu-id="f2e80-373">24</span></span>        | <span data-ttu-id="f2e80-374">FL-011</span><span class="sxs-lookup"><span data-stu-id="f2e80-374">FL-011</span></span>   | <span data-ttu-id="f2e80-375">LP02</span><span class="sxs-lookup"><span data-stu-id="f2e80-375">LP02</span></span>          | <span data-ttu-id="f2e80-376">5</span><span class="sxs-lookup"><span data-stu-id="f2e80-376">5</span></span>        |

    > [!NOTE]
    > <span data-ttu-id="f2e80-377">Stofna þarf tvær númeraplötur og nota staðsetningar sem leyfa blandaðar vörur, svo sem *FL-010* og *FL-011*.</span><span class="sxs-lookup"><span data-stu-id="f2e80-377">You must create the two license plates and use locations that allow for mixed items, such as *FL-010* and *FL-011*.</span></span>

### <a name="create-a-sales-order-and-reserve-a-specific-license-plate"></a><span data-ttu-id="f2e80-378">Stofna sölupöntun og taka frá tiltekna númeraplötu</span><span class="sxs-lookup"><span data-stu-id="f2e80-378">Create a sales order and reserve a specific license plate</span></span>

1. <span data-ttu-id="f2e80-379">Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-379">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="f2e80-380">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-380">Select **New**.</span></span>
1. <span data-ttu-id="f2e80-381">Sláið inn eftirfarandi gildi í svarglugganum **Stofna sölupöntun**:</span><span class="sxs-lookup"><span data-stu-id="f2e80-381">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="f2e80-382">**Viðskiptavinalykill:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="f2e80-382">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="f2e80-383">**Vöruhús:** *24*</span><span class="sxs-lookup"><span data-stu-id="f2e80-383">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="f2e80-384">Veljið **Í lagi** til að loka svarglugganum **Stofna sölupöntun** og opnið nýju sölupöntunina.</span><span class="sxs-lookup"><span data-stu-id="f2e80-384">Select **OK** to close the **Create sales order** dialog box and open the new sales order.</span></span>
1. <span data-ttu-id="f2e80-385">Í flýtiflipanum **Sölupöntunarlínur** skal bæta við línu sem er með eftirfarandi stillingum:</span><span class="sxs-lookup"><span data-stu-id="f2e80-385">On the **Sales order lines** FastTab, add a line that has the following settings:</span></span>

    - <span data-ttu-id="f2e80-386">**Vörunúmer:** *Item1*</span><span class="sxs-lookup"><span data-stu-id="f2e80-386">**Item number:** *Item1*</span></span>
    - <span data-ttu-id="f2e80-387">**Magn:** *10*</span><span class="sxs-lookup"><span data-stu-id="f2e80-387">**Quantity:** *10*</span></span>

1. <span data-ttu-id="f2e80-388">Bæta við annarri sölupöntunarlínu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="f2e80-388">Add a second sales order line that has the following settings:</span></span>

    - <span data-ttu-id="f2e80-389">**Vörunúmer:** *Item2*</span><span class="sxs-lookup"><span data-stu-id="f2e80-389">**Item number:** *Item2*</span></span>
    - <span data-ttu-id="f2e80-390">**Magn:** *5*</span><span class="sxs-lookup"><span data-stu-id="f2e80-390">**Quantity:** *5*</span></span>

1. <span data-ttu-id="f2e80-391">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-391">Select **Save**.</span></span>
1. <span data-ttu-id="f2e80-392">Í flýtiflipanum **Upplýsingar um línu**, í flipanum **Uppsetning**, skal skrá hjá sér gildið **Lotukenni** fyrir hverja línu.</span><span class="sxs-lookup"><span data-stu-id="f2e80-392">On the **Line details** FastTab, on the **Setup** tab, make a note of the **Lot ID** value for each line.</span></span> <span data-ttu-id="f2e80-393">Þessi gildi eru nauðsynleg þegar tilteknar númeraplötur eru teknar frá.</span><span class="sxs-lookup"><span data-stu-id="f2e80-393">These values will be required during reservation of specific license plates.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f2e80-394">Til að taka frá tiltekna númeraplötu þarf að nota gagnaeininguna **Frátektir á ráðstöfuðum pöntunum eftir númeraplötu**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-394">To reserve a specific license plate, you must use the **Order-committed reservations per license plate** data entity.</span></span> <span data-ttu-id="f2e80-395">Til að taka frá runurakta vöru á tiltekinni númeraplötu er einnig hægt að nota síðuna **Frátekt á runu**, eins og lýst er í hlutanum [Færa inn upplýsingar um sölupöntun](#sales-order-details).</span><span class="sxs-lookup"><span data-stu-id="f2e80-395">To reserve a batch-tracked item on a specific license plate, you can also use the **Batch reservation** page, as described in the [Enter sales order details](#sales-order-details) section.</span></span>
    >
    > <span data-ttu-id="f2e80-396">Ef númeraplata er færð beint inn í sölupöntunarlínuna og hún síðan staðfest í kerfinu, verður vinnsla vöruhúsakerfis ekki notuð fyrir línuna.</span><span class="sxs-lookup"><span data-stu-id="f2e80-396">If you enter the license plate directly on the sales order line and confirm it to the system, warehouse management processing won't be used for the line.</span></span>

1. <span data-ttu-id="f2e80-397">Veljið **Opna í Microsoft Office**, veljið **Frátektir á ráðstöfuðum pöntunum eftir númeraplötu** og hlaðið niður skránni.</span><span class="sxs-lookup"><span data-stu-id="f2e80-397">Select **Open in Microsoft Office**, select **Order-committed reservations per license plate**, and download the file.</span></span>
1. <span data-ttu-id="f2e80-398">Opnið niðurhalaða skrá í Excel og veljið **Virkja breytingar** svo að Excel-innbótin geti keyrt.</span><span class="sxs-lookup"><span data-stu-id="f2e80-398">Open the downloaded file in Excel, and select **Enable editing** to enable the Excel add-in to run.</span></span>
1. <span data-ttu-id="f2e80-399">Ef verið er að keyra í Excel-innbót í fyrsta sinn, er valið **Treysta þessari innbót**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-399">If you're running the Excel add-in for the first time, select **Trust this Add-in**.</span></span>
1. <span data-ttu-id="f2e80-400">Ef beðið er um að skrá sig inn skal velja **Innskráningu**, og síðan skrá sig inn með því að nota sömu innskráningarupplýsingar og eru notuð til að skrá sig inn í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f2e80-400">If you're prompted to sign in, select **Sign in**, and then sign in by using the same credentials that you used to sign in to Supply Chain Management.</span></span>
1. <span data-ttu-id="f2e80-401">Til að taka frá vöru á tiltekinni númeraplötu, í Excel-innbótinni, skal velja **Ný** til að bæta við frátektarlínu og stilla síðan eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="f2e80-401">To reserve an item on a specific license plate, in the Excel add-in, select **New** to add a reservation line, and then set the following values:</span></span>

    - <span data-ttu-id="f2e80-402">**Lotukenni:** Færið inn gildið fyrir **Lotukenni** sem fannst sölupöntunarlínuna fyrir *Item1*.</span><span class="sxs-lookup"><span data-stu-id="f2e80-402">**Lot ID:** Enter the **Lot ID** value that you found for the sales order line for *Item1*.</span></span>
    - <span data-ttu-id="f2e80-403">**Númeraplata:** *LP02*</span><span class="sxs-lookup"><span data-stu-id="f2e80-403">**License plate:** *LP02*</span></span>
    - <span data-ttu-id="f2e80-404">**ReservedInventoryQuantity:** *10*</span><span class="sxs-lookup"><span data-stu-id="f2e80-404">**ReservedInventoryQuantity:** *10*</span></span>

1. <span data-ttu-id="f2e80-405">Veljið **Ný** til að bæta við annarri frátektarlínu og stillið eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="f2e80-405">Select **New** to add another reservation line, and set the following values:</span></span>

    - <span data-ttu-id="f2e80-406">**Lotukenni:** Færið inn gildið fyrir **Lotukenni** sem fannst sölupöntunarlínuna fyrir *Item2*.</span><span class="sxs-lookup"><span data-stu-id="f2e80-406">**Lot ID:** Enter the **Lot ID** value you found for the sales order line for *Item2*.</span></span>
    - <span data-ttu-id="f2e80-407">**Númeraplata:** *LP02*</span><span class="sxs-lookup"><span data-stu-id="f2e80-407">**License plate:** *LP02*</span></span>
    - <span data-ttu-id="f2e80-408">**ReservedInventoryQuantity:** *5*</span><span class="sxs-lookup"><span data-stu-id="f2e80-408">**ReservedInventoryQuantity:** *5*</span></span>

1. <span data-ttu-id="f2e80-409">Í Excel-innbótinni skal velja **Birta** til að senda gögnin aftur í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f2e80-409">In the Excel add-in, select **Publish** to send the data back to Supply Chain Management.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f2e80-410">Frátektarlínan birtist aðeins í kerfinu ef birtingu er lokið án villna.</span><span class="sxs-lookup"><span data-stu-id="f2e80-410">The reservation line will appear in the system only if publishing is completed without errors.</span></span>

1. <span data-ttu-id="f2e80-411">Farið aftur í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f2e80-411">Go back to Supply Chain Management.</span></span> 
1. <span data-ttu-id="f2e80-412">Til að yfirfara frátekningu vörunnar, í flýtiflipanum **Sölupöntunarlínur**, í valmyndinni **Birgðir**, skal velja **Vinna með \> Frátekning**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-412">To review the item's reservation, on the **Sales order lines** FastTab, on the **Inventory** menu, select **Maintain \> Reservation**.</span></span> <span data-ttu-id="f2e80-413">Athugið að fyrir sölupöntunarlínuna fyrir *Item1* eru birgðir upp á *10* teknar frá og fyrir sölupöntunarlínuna fyrir *Item2*, eru birgðir upp á *5* teknar frá.</span><span class="sxs-lookup"><span data-stu-id="f2e80-413">Notice that, for the sales order line for *Item1*, inventory of *10* is reserved, and for the sales order line for *Item2*, inventory of *5* is reserved.</span></span>
1. <span data-ttu-id="f2e80-414">Til að fara yfir birgðafærslur sem tengjast frátekningu sölupöntunarlínu, í flýtiflipanum **Sölupöntunarlínur**, í valmyndinni **Birgðir**, skal velja **Skoða \> Færslur**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-414">To review inventory transactions that are related to the sales order line reservation, on the **Sales order lines** FastTab, on the **Inventory** menu, select **View \> Transactions**.</span></span> <span data-ttu-id="f2e80-415">Athugið að tvær færslur eru tengdar frátekningunni: ein þar sem reiturinn **Tilvísun** er stilltur á *Sölupöntun* og ein þar sem reiturinn **Tilvísun** er stilltur á *Frátekning á ráðstafaðri pöntun*.</span><span class="sxs-lookup"><span data-stu-id="f2e80-415">Notice that there are two transactions that are related to the reservation: one where the **Reference** field is set to *Sales order* and one where the **Reference** field is set to *Order-committed reservation*.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f2e80-416">Færsla þar sem reiturinn **Tilvísun** er stilltur á *Sölupöntun* sýnir frátekningu pöntunarlínu fyrir birgðavíddir sem eru fyrir ofan stigið **Staðsetning** (svæði, vöruhús og birgðastaða).</span><span class="sxs-lookup"><span data-stu-id="f2e80-416">A transaction where the **Reference** field is set to *Sales order* represents the order line reservation for inventory dimensions that are above the **Location** level (site, warehouse, and inventory status).</span></span> <span data-ttu-id="f2e80-417">Færsla þar sem reiturinn **Tilvísun** er stilltur á *Frátekning á ráðstafaðri pöntun* sýnir frátekningu pöntunarlínu fyrir tiltekna númeraplötu og staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="f2e80-417">A transaction where the **Reference** field is set to *Order-committed reservation* represents the order line reservation for the specific license plate and location.</span></span>

1. <span data-ttu-id="f2e80-418">Til að losa sölupöntunina, á aðgerðasvæðinu, í flipanum **Vöruhús**, í flokknum **Aðgerðir**, skal velja **Losa í vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-418">To release the sales order, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

### <a name="review-and-process-warehouse-work-with-order-committed-license-plates-assigned"></a><span data-ttu-id="f2e80-419">Yfirfara og vinna úr vöruhúsavinnu með úthlutaðar númeraplötur ráðstafaðrar pöntunar</span><span class="sxs-lookup"><span data-stu-id="f2e80-419">Review and process warehouse work with order-committed license plates assigned</span></span>

1. <span data-ttu-id="f2e80-420">Í flýtiflipanum **Sölupöntunarlínur**, í valmyndinni **Vöruhús**, skal velja **Upplýsingar um vinnu**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-420">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Work details**.</span></span>

    <span data-ttu-id="f2e80-421">Þar sem frátekning er gerð fyrir tiltekna runu, notar kerfið ekki staðsetningarleiðbeiningar þegar það stofnar vinnu fyrir sölupöntunina sem notar frátekningu númeraplötu.</span><span class="sxs-lookup"><span data-stu-id="f2e80-421">As when reservation is done for a specific batch, the system doesn't use location directives when it creates the work for the sales order that uses license plate reservation.</span></span> <span data-ttu-id="f2e80-422">Vegna þess að frátekning ráðstafaðrar pöntunar tilgreinir allar birgðavíddir, þ.á.m. staðsetningu, þarf ekki að nota staðsetningarleiðbeiningar vegna þess að birgðavíddir eru aðeins færðar inn í vinnuna.</span><span class="sxs-lookup"><span data-stu-id="f2e80-422">Because the order-committed reservation specifies all the inventory dimensions, including the location, location directives don't have to be used, because those inventory dimensions are just entered in the work.</span></span> <span data-ttu-id="f2e80-423">Þær eru sýndar í hlutanum **Úr birgðavíddum** á síðunni **Birgðafærslur vinnu**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-423">They are shown in the **From inventory dimensions** section on the **Work inventory transactions** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f2e80-424">Þegar búið er að stofna vinnu, er birgðafærsla vörunnar þar sem reiturinn **Tilvísun** er stilltur á *Frátekning á ráðstafaðri pöntun* fjarlægð.</span><span class="sxs-lookup"><span data-stu-id="f2e80-424">After the work is created, the item's inventory transaction where the **Reference** field is set to *Order-committed reservation* is removed.</span></span> <span data-ttu-id="f2e80-425">Birgðafærslan þar sem reiturinn **Tilvísun** er stilltur á *Vinna* inniheldur nú efnislega frátekningu fyrir allar birgðavíddir magns.</span><span class="sxs-lookup"><span data-stu-id="f2e80-425">The inventory transaction where the **Reference** field is set to *Work* now holds the physical reservation for all the quantity's inventory dimensions.</span></span>

1. <span data-ttu-id="f2e80-426">Í fartækinu skal ljúka tiltekt og frágangi vinnunnar með því að nota valmyndaratriði þar sem gátreiturinn **Meðhöndla eftir númeraplötu** er valið.</span><span class="sxs-lookup"><span data-stu-id="f2e80-426">On the mobile device, finish picking and putting the work by using a menu item where the **Handle by license plate** check box is selected.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f2e80-427">Aðgerðin **Meðhöndla eftir númeraplötu** sér um að vinna úr allri númeraplötunni.</span><span class="sxs-lookup"><span data-stu-id="f2e80-427">The **Handle by license plate** functionality helps you process the whole license plate.</span></span> <span data-ttu-id="f2e80-428">Ef nauðsynlegt er að vinna úr hluta númeraplötunnar, er ekki hægt að nota þessa aðgerð.</span><span class="sxs-lookup"><span data-stu-id="f2e80-428">If you must process part of the license plate, you can't use this functionality.</span></span>
    >
    > <span data-ttu-id="f2e80-429">Mælt er með því að aðskilin vinna sé búin til fyrir hverja númeraplötu.</span><span class="sxs-lookup"><span data-stu-id="f2e80-429">We recommend that you have separate work generated for each license plate.</span></span> <span data-ttu-id="f2e80-430">Til að ná þessu fram skal nota eiginleikann **Vinnuhausaskil** á síðunni **Vinnusniðmát**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-430">To achieve this result, use the **Work header breaks** feature on the **Work template** page.</span></span>

    <span data-ttu-id="f2e80-431">Númeraplata *LP02* er nú tínd fyrir sölupöntunarlínur og komið fyrir á staðsetningunni *Útskot*.</span><span class="sxs-lookup"><span data-stu-id="f2e80-431">License plate *LP02* is now picked for sales order lines and put to the *Baydoor* location.</span></span> <span data-ttu-id="f2e80-432">Á þessu stigi má hlaða og senda hana til viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="f2e80-432">At this point, it's ready to be loaded and dispatched to the customer.</span></span>

## <a name="exception-handling-of-warehouse-work-that-has-order-committed-batch-numbers"></a><span data-ttu-id="f2e80-433">Meðhöndlun undantekninga á vöruhúsavinnu sem er með rununúmer ráðstafaðra pantana</span><span class="sxs-lookup"><span data-stu-id="f2e80-433">Exception handling of warehouse work that has order-committed batch numbers</span></span>

<span data-ttu-id="f2e80-434">Vörugeymsla til að velja pöntunarbundin lotunúmer er háð sömu stöðluðu meðhöndlun undantekninga vörugeymslu og aðgerðum og venjuleg vinna.</span><span class="sxs-lookup"><span data-stu-id="f2e80-434">Warehouse work for picking order-committed batch numbers is subject to the same standard warehouse exception handling and actions as regular work.</span></span> <span data-ttu-id="f2e80-435">Almennt er hægt að hætta við opna verkið eða vinnu línuna, það er hægt að trufla það vegna þess að notendastaður er fullur, það er hægt að velja hann stutt og það er hægt að uppfæra hann vegna hreyfingar.</span><span class="sxs-lookup"><span data-stu-id="f2e80-435">In general, the open work or work line can be canceled, it can be interrupted because a user location is full, it can be short-picked, and it can be updated because of a movement.</span></span> <span data-ttu-id="f2e80-436">Sömuleiðis er hægt að draga úr valinni vinnu sem þegar hefur verið lokið eða hægt er að snúa verkinu við.</span><span class="sxs-lookup"><span data-stu-id="f2e80-436">Likewise, the picked quantity of work that has already been completed can be reduced, or the work can be reversed.</span></span>

<span data-ttu-id="f2e80-437">Eftirfarandi lykilregla er notuð við allar þessar undantekningarmeðferðaraðgerðir: aldrei er hægt að skipta um lotunúmer sem var frátekið fyrir viðskiptavininn fyrir annað lotunúmer, en hægt er að breyta geymsluvíddum hans (staðsetningu og kennitala) með annað hvort handvirkri uppfærslu af notanda eða sjálfvirka uppfærslu af kerfinu.</span><span class="sxs-lookup"><span data-stu-id="f2e80-437">The following key rule is applied to all these exception handling actions: the batch number that was reserved for the customer can never be replaced with a different batch number, but its storage dimensions (location and license plate) can be changed through either a manual update by the user or an automatic update by the system.</span></span> <span data-ttu-id="f2e80-438">Sjálfvirka uppfærslan er byggð á sömu handahófi úthlutun geymsluvíddar og gilti þegar ákveðin lota var sjálfkrafa frátekin en engar geymsluvíddir voru tilgreindar.</span><span class="sxs-lookup"><span data-stu-id="f2e80-438">The automatic update is based on the same random assignment of storage dimensions that applied when a specific batch was automatically reserved but no storage dimensions were specified.</span></span>

### <a name="example-scenario"></a><span data-ttu-id="f2e80-439">Dæmi</span><span class="sxs-lookup"><span data-stu-id="f2e80-439">Example scenario</span></span>

<span data-ttu-id="f2e80-440">Dæmi um þessa atburðarás er ástand þar sem verið er að velja áður lokið verk með því að nota virknina **Draga úr völdu magni**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-440">An example of this scenario is a situation where previously completed work is being unpicked by using the **Reduce picked quantity** function.</span></span> <span data-ttu-id="f2e80-441">Þetta dæmi gerir ráð fyrir því að skrefunum sem lýst er í [Sýniaðstæður: Úthlutun rununúmers](#Example-batch-allocation) sé lokið.</span><span class="sxs-lookup"><span data-stu-id="f2e80-441">This example assumes that you've already completed the steps that are described in [Example scenario: Batch number allocation](#Example-batch-allocation).</span></span> <span data-ttu-id="f2e80-442">Það heldur áfram þar sem frá var horfið í því dæmi.</span><span class="sxs-lookup"><span data-stu-id="f2e80-442">It continues from that example.</span></span>

1. <span data-ttu-id="f2e80-443">Farðu í **Vöruhúsakerfi** \> **Hleðslur** \> **Virkar hleðslur**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-443">Go to **Warehouse management** \> **Loads** \> **Active loads**.</span></span>
2. <span data-ttu-id="f2e80-444">Veldu álag sem var búið til í tengslum við sendingu sölupöntunar þinnar.</span><span class="sxs-lookup"><span data-stu-id="f2e80-444">Select the load that was created in connection with the shipment of your sales order.</span></span>
3. <span data-ttu-id="f2e80-445">Af flýtiflipanum **Hlaðið pöntunarlínum**, veldu **Draga úr völdum magni**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-445">From the **Load order lines** FastTab, select **Reduce picked quantity**.</span></span>
4. <span data-ttu-id="f2e80-446">Á **Draga úr völdum magni** síðu, í **Færa á staðsetningu** reit, veldu **FL-001**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-446">On the **Reduce picked quantity** page, in the **Move to location** field, select **FL-001**.</span></span>
5. <span data-ttu-id="f2e80-447">Í reitnum **Flytja á númeraplötu** velurðu **LP33**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-447">In the **Move to license plate** field, select **LP33**.</span></span>
6. <span data-ttu-id="f2e80-448">Í hnitanetinu í reitnum **Magn birgða til að afturkalla tiltekt á** sláðu inn **10**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-448">In the grid, in the **Inventory quantity to unpick** field, enter **10**.</span></span>
7. <span data-ttu-id="f2e80-449">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-449">Select **OK**.</span></span>

<span data-ttu-id="f2e80-450">Hér eru niðurstöður úr aðgerð til að afturkalla tiltekt:</span><span class="sxs-lookup"><span data-stu-id="f2e80-450">Here are the results of the unpicking action:</span></span>

- <span data-ttu-id="f2e80-451">Staða fyrri lokaðs verks er stillt á **Hætt við**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-451">The status of the previously closed work is set to **Canceled**.</span></span>
- <span data-ttu-id="f2e80-452">Nýtt verk af gerðinni **Birgðahreyfing** er búin til fyrir óvalið magn af **10** fyrir lotunúmer **B11**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-452">New work of the **Inventory movement** type is created for the unpicked quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="f2e80-453">Þessi vinna táknar hreyfingu frá **Afgreiðsluhurð** staðsetningu til númeraplötu **LP33** á staðsetningu **FL-001**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-453">This work represents the movement from the **Baydoor** location to license plate **LP33** in location **FL-001**.</span></span> <span data-ttu-id="f2e80-454">Staðan er stillt á **Lokað**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-454">The status is set to **Closed**.</span></span>
- <span data-ttu-id="f2e80-455">Kerfið áskilur aftur lotunúmerið sem upphaflega var pantað og úthlutar auðkenni staðsetningar og korts.</span><span class="sxs-lookup"><span data-stu-id="f2e80-455">The system re-reserves the batch number that was originally ordered, and assigns the location and license plate IDs.</span></span> <span data-ttu-id="f2e80-456">(Þetta ferli jafngildir því að keyra virknina **Frátektarlína** fyrir pöntunarlínuna fyrir tiltekið lotunúmer).</span><span class="sxs-lookup"><span data-stu-id="f2e80-456">(This process is equivalent to running the **Reserve line** function for the order line for a given batch number).</span></span> <span data-ttu-id="f2e80-457">Fyrir vikið, hópur **B11** er sýnt sem framið á flýtiflipanum **Hópatölur skuldbundnar til upprunalínu** af **Runufrátekt** síðu og **Frátekt** reiturinn inniheldur magn af **10** fyrir lotunúmer **B11**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-457">As a result, batch **B11** is shown as committed on the **Batch numbers committed to source line** FastTab of the **Batch reservation** page, and the **Reservation** field contains a quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="f2e80-458">Að auki, er **Staðsetning** reiturinn stilltur á **FL-001**, og **Númeraplata** reiturinn er stilltur á **LP11**.</span><span class="sxs-lookup"><span data-stu-id="f2e80-458">Additionally, the **Location** field is set to **FL-001**, and the **License plate** field is set to **LP11**.</span></span> <span data-ttu-id="f2e80-459">(Þú getur bætt þessum reitum við töfluna ef þeir eru ekki sýnilegir.)</span><span class="sxs-lookup"><span data-stu-id="f2e80-459">(You can add these fields to the grid if they aren't visible.)</span></span>

<span data-ttu-id="f2e80-460">Eftirfarandi töflur veita yfirlit sem sýnir hvernig kerfið meðhöndlar pöntunarbundna lotu fyrirvara fyrir sérstakar vörugeymsluaðgerðir.</span><span class="sxs-lookup"><span data-stu-id="f2e80-460">The following tables provide an overview that shows how the system handles order-committed batch reservation for specific warehouse actions.</span></span> <span data-ttu-id="f2e80-461">Til að túlka innihaldið í töflunum, gerðu ráð fyrir að hver vörugeymslaaðgerð sé keyrð í samhengi við núverandi vörugeymsluverk sem er upprunnin í pöntunarbundinni lotu fyrirvara, eða að framkvæmd hverrar vörugerðaraðgerðar hefur áhrif á vinnu af þeirri gerð.</span><span class="sxs-lookup"><span data-stu-id="f2e80-461">To interpret the content in the tables, assume that each warehouse action is run in the context of existing warehouse work that originates from an order-committed batch reservation, or that execution of each warehouse action affects work of that type.</span></span>

> [!NOTE]
> <span data-ttu-id="f2e80-462">Í þessum töflum gefur dálkurinn „Hópmagn er fáanlegt“ til kynna hvort magn af framleiðslulotu er til viðbótar við það magn sem er annað hvort þegar frátekið fyrir núverandi pöntunarbundna fyrirvara eða þegar er frátekið af vörugeymsluverkinu sem kemur frá fyrirvörum af þeirri gerð.</span><span class="sxs-lookup"><span data-stu-id="f2e80-462">In these tables, the "Batch quantity is available" column indicates whether a batch quantity is available in addition to the quantity that is either already reserved for the current order-committed reservations or already reserved by the warehouse work that originates from reservations of that type.</span></span>

#### <a name="override-the-pick-location-on-the-open-work"></a><span data-ttu-id="f2e80-463">Yfirskrifa tínslustaðsetningu í opinni vinnu</span><span class="sxs-lookup"><span data-stu-id="f2e80-463">Override the pick location on the open work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="f2e80-464">Færibreyta lykiluppsetningar</span><span class="sxs-lookup"><span data-stu-id="f2e80-464">Key setup parameter</span></span></th>
<th><span data-ttu-id="f2e80-465">Runumagn er fáanlegt</span><span class="sxs-lookup"><span data-stu-id="f2e80-465">Batch quantity is available</span></span></th>
<th><span data-ttu-id="f2e80-466">Lykilþrep notenda</span><span class="sxs-lookup"><span data-stu-id="f2e80-466">Key user steps</span></span></th>
<th><span data-ttu-id="f2e80-467">Vinna vöruhúss</span><span class="sxs-lookup"><span data-stu-id="f2e80-467">Warehouse work</span></span></th>
<th><span data-ttu-id="f2e80-468">Pantanaskuldbundin hópapöntun</span><span class="sxs-lookup"><span data-stu-id="f2e80-468">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="f2e80-469">Valkosturinn <strong>Leyfa val á staðsetningu staðsetningu</strong> er virkur á starfsmanninum.</span><span class="sxs-lookup"><span data-stu-id="f2e80-469">The <strong>Allow pick location override</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="f2e80-470">Já</span><span class="sxs-lookup"><span data-stu-id="f2e80-470">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="f2e80-471">Veljið valmyndaratriðið <strong>Yfirskrifa staðsetningu</strong> í farsímaforriti vöruhúsakerfis þegar tiltektarverk er hafið.</span><span class="sxs-lookup"><span data-stu-id="f2e80-471">Select the <strong>Override location</strong> menu item on the Warehouse Management mobile app when you start picking work.</span></span></li>
<li><span data-ttu-id="f2e80-472">Veldu <strong>Stinga upp</strong>.</span><span class="sxs-lookup"><span data-stu-id="f2e80-472">Select <strong>Suggest</strong>.</span></span></li>
<li><span data-ttu-id="f2e80-473">Staðfestu nýja staðsetninguna sem lagt er til með tilliti til framboðs í fjölda magns.</span><span class="sxs-lookup"><span data-stu-id="f2e80-473">Confirm the new location that is suggested based on batch quantity availability.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="f2e80-474">Eftirfarandi aðgerðir eiga sér stað í núverandi vinnu:</span><span class="sxs-lookup"><span data-stu-id="f2e80-474">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="f2e80-475">Staðsetningin á velja línunni er uppfærð á nýjan stað.</span><span class="sxs-lookup"><span data-stu-id="f2e80-475">The location on the pick line is updated to the new location.</span></span> <span data-ttu-id="f2e80-476">(Ef staðsetningin er stjórnað með leyfismerki er úthlutað af handahófi leyfismerki fyrir vörubirgðafærsluna og starfsmaðurinn getur valið úr hvaða skilti sem er með tiltækt magn.)</span><span class="sxs-lookup"><span data-stu-id="f2e80-476">(If the location is license plate–controlled, a random license plate is assigned to the work inventory transaction, and the worker can pick from any license plate that has available quantity.)</span></span></li>
<li><span data-ttu-id="f2e80-477">Ef magnið er að finna á fleiri en einni leyfisplötu á nýjum stað, er upprunalegu vallínunni skipt í margar línur sem passa við hvern kennitala.</span><span class="sxs-lookup"><span data-stu-id="f2e80-477">If the quantity is found on more than one license plate in the new location, the original pick line is split into multiple lines to match each license plate.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="f2e80-478">Ekki tiltækt</span><span class="sxs-lookup"><span data-stu-id="f2e80-478">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f2e80-479">Ekkert</span><span class="sxs-lookup"><span data-stu-id="f2e80-479">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="f2e80-480">Veljið valmyndaratriðið <strong>Yfirskrifa staðsetningu</strong> í farsímaforriti vöruhúsakerfis þegar tiltektarverk er hafið.</span><span class="sxs-lookup"><span data-stu-id="f2e80-480">Select the <strong>Override location</strong> menu item on the Warehouse Management mobile app when you start picking work.</span></span></li>
<li><span data-ttu-id="f2e80-481">Færa handvirkt inn staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="f2e80-481">Manually enter a location.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="f2e80-482">Aðgerðin <strong>Hnekkja staðsetningu</strong> er ekki möguleg.</span><span class="sxs-lookup"><span data-stu-id="f2e80-482">The <strong>Override location</strong> action isn't possible.</span></span> <span data-ttu-id="f2e80-483">Það mistekst og villu er hent.</span><span class="sxs-lookup"><span data-stu-id="f2e80-483">It fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="f2e80-484">Á ekki við</span><span class="sxs-lookup"><span data-stu-id="f2e80-484">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="full-button--split-a-work-line-because-of-overflow-on-the-user-location"></a><span data-ttu-id="f2e80-485">Fullur hnappur - Skiptu vinnulínu vegna flæða á staðsetningu notandans</span><span class="sxs-lookup"><span data-stu-id="f2e80-485">Full button – Split a work line because of overflow on the user location</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="f2e80-486">Færibreyta lykiluppsetningar</span><span class="sxs-lookup"><span data-stu-id="f2e80-486">Key setup parameter</span></span></th>
<th><span data-ttu-id="f2e80-487">Runumagn er fáanlegt</span><span class="sxs-lookup"><span data-stu-id="f2e80-487">Batch quantity is available</span></span></th>
<th><span data-ttu-id="f2e80-488">Lykilþrep notenda</span><span class="sxs-lookup"><span data-stu-id="f2e80-488">Key user steps</span></span></th>
<th><span data-ttu-id="f2e80-489">Vinna vöruhúss</span><span class="sxs-lookup"><span data-stu-id="f2e80-489">Warehouse work</span></span></th>
<th><span data-ttu-id="f2e80-490">Pantanaskuldbundin hópapöntun</span><span class="sxs-lookup"><span data-stu-id="f2e80-490">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f2e80-491">Valkosturinn <strong>Leyfa verkaskiptingu</strong> er virkur í valmyndaratriðinu fyrir farsíma.</span><span class="sxs-lookup"><span data-stu-id="f2e80-491">The <strong>Allow splitting of work</strong> option is enabled on the mobile device menu item.</span></span></td>
<td><span data-ttu-id="f2e80-492">Ekki tiltækt</span><span class="sxs-lookup"><span data-stu-id="f2e80-492">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="f2e80-493">Veljið valmyndaratriðið <strong>Fullt</strong> í farsímaforriti vöruhúsakerfis þegar tiltektarverk er hafið.</span><span class="sxs-lookup"><span data-stu-id="f2e80-493">Select the <strong>Full</strong> menu item on the Warehouse Management mobile app when you process picking work.</span></span></li>
<li><span data-ttu-id="f2e80-494">Í <strong>Veldu fjölda</strong> reitinn, sláðu inn hluta magns af nauðsynlegu valinu til að gefa til kynna fullan afköst.</span><span class="sxs-lookup"><span data-stu-id="f2e80-494">In the <strong>Pick Qty</strong> field, enter a partial quantity of the required pick to indicate the full capacity.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="f2e80-495">Í núverandi vinnu er magnið uppfært í það magn sem eftir verður sem þarf að velja.</span><span class="sxs-lookup"><span data-stu-id="f2e80-495">On the current work, the quantity is updated to the remaining quantity that must be picked.</span></span></li>
<li><span data-ttu-id="f2e80-496">Ný verk fyrir valið magn er búið til og lokað.</span><span class="sxs-lookup"><span data-stu-id="f2e80-496">New work for the picked quantity is created and closed.</span></span></li>
</ul></td>
<td><span data-ttu-id="f2e80-497">Á ekki við</span><span class="sxs-lookup"><span data-stu-id="f2e80-497">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reduce-the-picked-quantity-of-completed-work-from-a-load"></a><span data-ttu-id="f2e80-498">Draga úr valið magn af fullunninni vinnu (úr álagi)</span><span class="sxs-lookup"><span data-stu-id="f2e80-498">Reduce the picked quantity of completed work (from a load)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="f2e80-499">Færibreyta lykiluppsetningar</span><span class="sxs-lookup"><span data-stu-id="f2e80-499">Key setup parameter</span></span></th>
<th><span data-ttu-id="f2e80-500">Runumagn er fáanlegt</span><span class="sxs-lookup"><span data-stu-id="f2e80-500">Batch quantity is available</span></span></th>
<th><span data-ttu-id="f2e80-501">Lykilþrep notenda</span><span class="sxs-lookup"><span data-stu-id="f2e80-501">Key user steps</span></span></th>
<th><span data-ttu-id="f2e80-502">Vinna vöruhúss</span><span class="sxs-lookup"><span data-stu-id="f2e80-502">Warehouse work</span></span></th>
<th><span data-ttu-id="f2e80-503">Pantanaskuldbundin hópapöntun</span><span class="sxs-lookup"><span data-stu-id="f2e80-503">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="f2e80-504">Á ekki við</span><span class="sxs-lookup"><span data-stu-id="f2e80-504">Not applicable</span></span></td>
<td><span data-ttu-id="f2e80-505">Já</span><span class="sxs-lookup"><span data-stu-id="f2e80-505">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="f2e80-506">Opnaðu <strong>Draga úr völdum magni</strong> síðu frá hleðslulínunni.</span><span class="sxs-lookup"><span data-stu-id="f2e80-506">Open the <strong>Reduce picked quantity</strong> page from the load line.</span></span></li>
<li><span data-ttu-id="f2e80-507">Færa skal inn fullt magn til að afturkalla tiltekt á.</span><span class="sxs-lookup"><span data-stu-id="f2e80-507">Enter the full quantity to unpick.</span></span></li>
<li><span data-ttu-id="f2e80-508">Veldu „færa til“ staðsetningu / kennitala.</span><span class="sxs-lookup"><span data-stu-id="f2e80-508">Select a "move to" location/license plate.</span></span></li>
</ol>
</td>
<td>
<ul> 
<li><span data-ttu-id="f2e80-509">Vinna sem er tengd hleðslulínunni fellur niður.</span><span class="sxs-lookup"><span data-stu-id="f2e80-509">Work that is associated with the load line is canceled.</span></span></li>
<li><span data-ttu-id="f2e80-510">Ný verk fyrir birgðahreyfingar er búið til og lokað.</span><span class="sxs-lookup"><span data-stu-id="f2e80-510">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="f2e80-511">Magnið er aftur frátekið fyrir sömu lotu.</span><span class="sxs-lookup"><span data-stu-id="f2e80-511">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="f2e80-512">Kerfið úthlutar af handahófi staðsetningu og kennitala (ef staðsetningin er stjórnað með skiltum) þar sem magnið er fáanlegt.</span><span class="sxs-lookup"><span data-stu-id="f2e80-512">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f2e80-513">Nr</span><span class="sxs-lookup"><span data-stu-id="f2e80-513">No</span></span></td>
<td><span data-ttu-id="f2e80-514">Sjá fyrri línuna.</span><span class="sxs-lookup"><span data-stu-id="f2e80-514">See the previous row.</span></span></td>
<td><span data-ttu-id="f2e80-515">Sjá fyrri línuna.</span><span class="sxs-lookup"><span data-stu-id="f2e80-515">See the previous row.</span></span></td>
<td><span data-ttu-id="f2e80-516">Magnið er aftur frátekið fyrir sömu framleiðslulotu og fyrir sama stað og skírteini (ef staðsetningin er stjórnað með skiltum) sem var slegið inn við upptöku.</span><span class="sxs-lookup"><span data-stu-id="f2e80-516">The quantity is re-reserved for the same batch, and for the same location and license plate (if the location is license plate–controlled) that were entered during unpicking.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="move-an-item-within-a-warehouse"></a><span data-ttu-id="f2e80-517">Færa vöru til innan vöruhúss</span><span class="sxs-lookup"><span data-stu-id="f2e80-517">Move an item within a warehouse</span></span>

> [!NOTE]
> <span data-ttu-id="f2e80-518">Þessi vörugeymsla á aðeins við um flutninga á **Vinnusköpunarferli** tegund, ekki til hreyfingar eftir sniðmáti.</span><span class="sxs-lookup"><span data-stu-id="f2e80-518">This warehouse action is applicable only to movement of the **Work creation process** type, not to movement by template.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="f2e80-519">Færibreyta lykiluppsetningar</span><span class="sxs-lookup"><span data-stu-id="f2e80-519">Key setup parameter</span></span></th>
<th><span data-ttu-id="f2e80-520">Runumagn er fáanlegt</span><span class="sxs-lookup"><span data-stu-id="f2e80-520">Batch quantity is available</span></span></th>
<th><span data-ttu-id="f2e80-521">Lykilþrep notenda</span><span class="sxs-lookup"><span data-stu-id="f2e80-521">Key user steps</span></span></th>
<th><span data-ttu-id="f2e80-522">Vinna vöruhúss</span><span class="sxs-lookup"><span data-stu-id="f2e80-522">Warehouse work</span></span></th>
<th><span data-ttu-id="f2e80-523">Pantanaskuldbundin hópapöntun</span><span class="sxs-lookup"><span data-stu-id="f2e80-523">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="f2e80-524">Valkostur <strong>Leyfa flutning birgða með tilheyrandi vinnu</strong> er virkur á starfsmanninum.</span><span class="sxs-lookup"><span data-stu-id="f2e80-524">The <strong>Allow movement of inventory with associated work</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="f2e80-525">Já</span><span class="sxs-lookup"><span data-stu-id="f2e80-525">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="f2e80-526">Hefja færslu í farsímaforriti vöruhúsakerfis.</span><span class="sxs-lookup"><span data-stu-id="f2e80-526">Start a movement on the Warehouse Management mobile app.</span></span></li>
<li><span data-ttu-id="f2e80-527">Sláið inn staðsetningar „frá” og „til”.</span><span class="sxs-lookup"><span data-stu-id="f2e80-527">Enter "from" and "to" locations.</span></span></li>
</ol></td>
<td>
<ul>
<li><span data-ttu-id="f2e80-528">Í allri núverandi vinnu sem hefur áhrif á flutninginn, er staðsetningin valin uppfærð á nýja „til“ staðinn.</span><span class="sxs-lookup"><span data-stu-id="f2e80-528">On all existing work that is affected by the move, the pick location is updated to the new "to" location.</span></span></li>
<li><span data-ttu-id="f2e80-529">Ný verk fyrir birgðahreyfingar er búið til og lokað.</span><span class="sxs-lookup"><span data-stu-id="f2e80-529">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="f2e80-530">Allir núverandi fyrirvarar sem hafa áhrif á magnhreyfingu frá tilteknum stað eru aftur áskilnir fyrir sömu lotu.</span><span class="sxs-lookup"><span data-stu-id="f2e80-530">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch.</span></span> <span data-ttu-id="f2e80-531">Kerfið úthlutar af handahófi staðsetningu og kennitala (ef staðsetningin er stjórnað með skiltum) þar sem magnið er fáanlegt.</span><span class="sxs-lookup"><span data-stu-id="f2e80-531">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f2e80-532">Nr</span><span class="sxs-lookup"><span data-stu-id="f2e80-532">No</span></span></td>
<td><span data-ttu-id="f2e80-533">Sjá fyrri línuna.</span><span class="sxs-lookup"><span data-stu-id="f2e80-533">See the previous row.</span></span></td>
<td><span data-ttu-id="f2e80-534">Sjá fyrri línuna.</span><span class="sxs-lookup"><span data-stu-id="f2e80-534">See the previous row.</span></span></td>
<td><span data-ttu-id="f2e80-535">Allur fyrirliggjandi fyrirvari sem hefur áhrif á magnhreyfingu frá tilteknum stað er aftur áskilinn fyrir sömu framleiðslulotu og fyrir nýja „til“ staðsetningar og kennitala (ef staðsetningin er stjórnað með skiltum).</span><span class="sxs-lookup"><span data-stu-id="f2e80-535">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch, and for the new "to" location and license plate (if the location is license plate–controlled).</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reverse-the-picked-quantity-of-completed-work-from-a-load-or-a-wave"></a><span data-ttu-id="f2e80-536">Bakfærðu tiltekið magn af fullunninni vinnu (úr álagi eða bylgju)</span><span class="sxs-lookup"><span data-stu-id="f2e80-536">Reverse the picked quantity of completed work (from a load or a wave)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="f2e80-537">Færibreyta lykiluppsetningar</span><span class="sxs-lookup"><span data-stu-id="f2e80-537">Key setup parameter</span></span></th>
<th><span data-ttu-id="f2e80-538">Runumagn er fáanlegt</span><span class="sxs-lookup"><span data-stu-id="f2e80-538">Batch quantity is available</span></span></th>
<th><span data-ttu-id="f2e80-539">Lykilþrep notenda</span><span class="sxs-lookup"><span data-stu-id="f2e80-539">Key user steps</span></span></th>
<th><span data-ttu-id="f2e80-540">Vinna vöruhúss</span><span class="sxs-lookup"><span data-stu-id="f2e80-540">Warehouse work</span></span></th>
<th><span data-ttu-id="f2e80-541">Pantanaskuldbundin hópapöntun</span><span class="sxs-lookup"><span data-stu-id="f2e80-541">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='6'><span data-ttu-id="f2e80-542">Á ekki við</span><span class="sxs-lookup"><span data-stu-id="f2e80-542">Not applicable</span></span></td>
<td><span data-ttu-id="f2e80-543">Já</span><span class="sxs-lookup"><span data-stu-id="f2e80-543">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="f2e80-544">Opnaðu <strong>Bakfæra vinnu</strong> síðu.</span><span class="sxs-lookup"><span data-stu-id="f2e80-544">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="f2e80-545">Veldu beiðnissíðuna <strong>Skildu hluti eftir núverandi staðsetningu</strong> kostur.</span><span class="sxs-lookup"><span data-stu-id="f2e80-545">On the request page, select the <strong>Leave items at current location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="f2e80-546">Öll vinna sem er tengd hleðslunni fellur niður.</span><span class="sxs-lookup"><span data-stu-id="f2e80-546">All work that is associated with the load is canceled.</span></span></td>
<td><span data-ttu-id="f2e80-547">Magnið er aftur frátekið fyrir sömu lotu.</span><span class="sxs-lookup"><span data-stu-id="f2e80-547">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="f2e80-548">Kerfið úthlutar af handahófi staðsetningu og kennitala (ef staðsetningin er stjórnað með skiltum) þar sem magnið er fáanlegt.</span><span class="sxs-lookup"><span data-stu-id="f2e80-548">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f2e80-549">Nr</span><span class="sxs-lookup"><span data-stu-id="f2e80-549">No</span></span></td>
<td><span data-ttu-id="f2e80-550">Sjá fyrri línuna.</span><span class="sxs-lookup"><span data-stu-id="f2e80-550">See the previous row.</span></span></td>
<td><span data-ttu-id="f2e80-551">Sjá fyrri línuna.</span><span class="sxs-lookup"><span data-stu-id="f2e80-551">See the previous row.</span></span></td>
<td><span data-ttu-id="f2e80-552">Magnið er frátekið fyrir sömu framleiðslulotu og fyrir staðsetningu og kennitala þar sem magnið var eftir við afturköllun.</span><span class="sxs-lookup"><span data-stu-id="f2e80-552">The quantity is re-reserved for the same batch, and for the location and license plate where the quantity was left upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f2e80-553">Já</span><span class="sxs-lookup"><span data-stu-id="f2e80-553">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="f2e80-554">Opnaðu <strong>Bakfæra vinnu</strong> síðu.</span><span class="sxs-lookup"><span data-stu-id="f2e80-554">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="f2e80-555">Veldu beiðnissíðuna <strong>Úthluta vörum á þessa staðsetningu</strong> kostur.</span><span class="sxs-lookup"><span data-stu-id="f2e80-555">On the request page, select the <strong>Assign items to this location</strong> option.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="f2e80-556">Núgildandi vinna er afturkölluð.</span><span class="sxs-lookup"><span data-stu-id="f2e80-556">The current work is canceled.</span></span></li>
<li><span data-ttu-id="f2e80-557">Ný verk fyrir birgðahreyfingar er búið til og lokað.</span><span class="sxs-lookup"><span data-stu-id="f2e80-557">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="f2e80-558">Magnið er aftur frátekið fyrir sömu lotu.</span><span class="sxs-lookup"><span data-stu-id="f2e80-558">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="f2e80-559">Kerfið úthlutar af handahófi staðsetningu og kennitala (ef staðsetningin er stjórnað með skiltum) þar sem magnið er fáanlegt.</span><span class="sxs-lookup"><span data-stu-id="f2e80-559">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f2e80-560">Nr</span><span class="sxs-lookup"><span data-stu-id="f2e80-560">No</span></span></td>
<td><span data-ttu-id="f2e80-561">Sjá fyrri línuna.</span><span class="sxs-lookup"><span data-stu-id="f2e80-561">See the previous row.</span></span></td>
<td><span data-ttu-id="f2e80-562">Sjá fyrri línuna.</span><span class="sxs-lookup"><span data-stu-id="f2e80-562">See the previous row.</span></span></td>
<td><span data-ttu-id="f2e80-563">Magnið er frátekið fyrir sömu framleiðslulotu og fyrir staðsetningu og kennitala þar sem magnið var úthlutað á við bakfærslu.</span><span class="sxs-lookup"><span data-stu-id="f2e80-563">The quantity is re-reserved for the same batch, and for the location and license plate that the quantity was assigned to upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f2e80-564">Já/nei</span><span class="sxs-lookup"><span data-stu-id="f2e80-564">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="f2e80-565">Opnaðu <strong>Bakfæra vinnu</strong> síðu.</span><span class="sxs-lookup"><span data-stu-id="f2e80-565">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="f2e80-566">Veldu beiðnissíðuna <strong>Færa vörur á þessa staðsetningu</strong> kostur.</span><span class="sxs-lookup"><span data-stu-id="f2e80-566">On the request page, select the <strong>Move items to this location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="f2e80-567">Bakfærsla er ekki studd.</span><span class="sxs-lookup"><span data-stu-id="f2e80-567">Reversal isn't supported.</span></span></td>
<td><span data-ttu-id="f2e80-568">Á ekki við</span><span class="sxs-lookup"><span data-stu-id="f2e80-568">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f2e80-569">Já/nei</span><span class="sxs-lookup"><span data-stu-id="f2e80-569">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="f2e80-570">Opnaðu <strong>Bakfæra vinnu</strong> síðu.</span><span class="sxs-lookup"><span data-stu-id="f2e80-570">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="f2e80-571">Veldu beiðnissíðuna <strong>Færa vörur byggt á staðsetningartilskipunum</strong> kostur.</span><span class="sxs-lookup"><span data-stu-id="f2e80-571">On the request page, select the <strong>Move items based on location directives</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="f2e80-572">Bakfærsla er ekki studd.</span><span class="sxs-lookup"><span data-stu-id="f2e80-572">Reversal isn't supported.</span></span> </td>
<td><span data-ttu-id="f2e80-573">Á ekki við</span><span class="sxs-lookup"><span data-stu-id="f2e80-573">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="short-pick-a-quantity--register-the-quantity-as-physically-not-found-at-the-locationlicense-plate-while-you-perform-picking-work"></a><span data-ttu-id="f2e80-574">Veldu stutt skammt - Skráðu magnið sem ekki finnast líkamlega á staðnum / leyfismerkinu meðan þú framkvæmir tínaverk</span><span class="sxs-lookup"><span data-stu-id="f2e80-574">Short-pick a quantity – Register the quantity as physically not found at the location/license plate while you perform picking work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="f2e80-575">Færibreyta lykiluppsetningar</span><span class="sxs-lookup"><span data-stu-id="f2e80-575">Key setup parameter</span></span></th>
<th><span data-ttu-id="f2e80-576">Runumagn er fáanlegt</span><span class="sxs-lookup"><span data-stu-id="f2e80-576">Batch quantity is available</span></span></th>
<th><span data-ttu-id="f2e80-577">Lykilþrep notenda</span><span class="sxs-lookup"><span data-stu-id="f2e80-577">Key user steps</span></span></th>
<th><span data-ttu-id="f2e80-578">Vinna vöruhúss</span><span class="sxs-lookup"><span data-stu-id="f2e80-578">Warehouse work</span></span></th>
<th><span data-ttu-id="f2e80-579">Pantanaskuldbundin hópapöntun</span><span class="sxs-lookup"><span data-stu-id="f2e80-579">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="f2e80-580">Vinna undantekning frá <strong>Stutt val</strong> gerð er sett upp, hvar <strong>Endurúthlutun hlutar</strong> = <strong>Enginn</strong>, <strong>Stilla lager</strong> = <strong>Já</strong> og <strong>Fjarlægðu fyrirvara</strong> = <strong>Nei</strong>.</span><span class="sxs-lookup"><span data-stu-id="f2e80-580">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span></td>
<td><span data-ttu-id="f2e80-581">Já</span><span class="sxs-lookup"><span data-stu-id="f2e80-581">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="f2e80-582">Veljið valmyndaratriðið <strong>Of lítil tiltekt</strong> í farsímaforriti vöruhúsakerfis þegar tiltekt er keyrð.</span><span class="sxs-lookup"><span data-stu-id="f2e80-582">Select the <strong>Shortpick</strong> menu item on the Warehouse Management mobile app when you run picking work.</span></span></li>
<li><span data-ttu-id="f2e80-583">Í <strong>Tiltekið magn</strong> reitinn er fært inn <strong>0</strong> (núll).</span><span class="sxs-lookup"><span data-stu-id="f2e80-583">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="f2e80-584">Í reitinn <strong>Ástæða</strong> slærðu inn <strong>Engin endurúthlutun</strong>.</span><span class="sxs-lookup"><span data-stu-id="f2e80-584">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="f2e80-585">Núverandi verk er lokað og valið magn er 0 (núll).</span><span class="sxs-lookup"><span data-stu-id="f2e80-585">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="f2e80-586">Birgðafærsla <strong>Telja</strong> tegund og <strong>Selt</strong> útgáfutegund er búin til til að tákna aðlögunina.</span><span class="sxs-lookup"><span data-stu-id="f2e80-586">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="f2e80-587">Magnið er aftur frátekið fyrir sömu lotu.</span><span class="sxs-lookup"><span data-stu-id="f2e80-587">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="f2e80-588">Kerfið úthlutar af handahófi staðsetningu og kennitala (ef staðsetningin er stjórnað með skiltum) þar sem magnið er fáanlegt.</span><span class="sxs-lookup"><span data-stu-id="f2e80-588">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f2e80-589">Nr</span><span class="sxs-lookup"><span data-stu-id="f2e80-589">No</span></span></td>
<td><span data-ttu-id="f2e80-590">Sjá fyrri línuna.</span><span class="sxs-lookup"><span data-stu-id="f2e80-590">See the previous row.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="f2e80-591">Of lítil tiltekt-aðgerðin mistekst og villu er hent.</span><span class="sxs-lookup"><span data-stu-id="f2e80-591">The short-picking action fails, and an error is thrown.</span></span></li>
<li><span data-ttu-id="f2e80-592">Núverandi verk er áfram opið.</span><span class="sxs-lookup"><span data-stu-id="f2e80-592">The current work remains open.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="f2e80-593">Á ekki við</span><span class="sxs-lookup"><span data-stu-id="f2e80-593">Not applicable</span></span></td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="f2e80-594">Vinna undantekning frá <strong>Stutt val</strong> gerð er sett upp, hvar <strong>Endurúthlutun hlutar</strong> = <strong>Enginn</strong>, <strong>Stilla lager</strong> = <strong>Já</strong> og <strong>Fjarlægðu fyrirvara</strong> = <strong>Já</strong>.</span><span class="sxs-lookup"><span data-stu-id="f2e80-594">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span></td>
<td><span data-ttu-id="f2e80-595">Já</span><span class="sxs-lookup"><span data-stu-id="f2e80-595">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="f2e80-596">Veljið valmyndaratriðið <strong>Of lítil tiltekt</strong> í farsímaforriti vöruhúsakerfis þegar tiltekt er keyrð.</span><span class="sxs-lookup"><span data-stu-id="f2e80-596">Select the <strong>Shortpick</strong> menu item on the Warehouse Management mobile app when you run picking work.</span></span></li>
<li><span data-ttu-id="f2e80-597">Í <strong>Tiltekið magn</strong> reitinn er fært inn <strong>0</strong> (núll).</span><span class="sxs-lookup"><span data-stu-id="f2e80-597">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="f2e80-598">Í reitinn <strong>Ástæða</strong> slærðu inn <strong>Engin endurúthlutun</strong>.</span><span class="sxs-lookup"><span data-stu-id="f2e80-598">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="f2e80-599">Núverandi verk er lokað og valið magn er 0 (núll).</span><span class="sxs-lookup"><span data-stu-id="f2e80-599">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="f2e80-600">Birgðafærsla <strong>Telja</strong> tegund og <strong>Selt</strong> útgáfutegund er búin til til að tákna aðlögunina.</span><span class="sxs-lookup"><span data-stu-id="f2e80-600">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="f2e80-601">Allar núverandi frátektir sem hafa áhrif á magnleiðréttingu á staðsetningu þar sem tiltekt er of lítil eru endurfráteknar fyrir sömu lotu.</span><span class="sxs-lookup"><span data-stu-id="f2e80-601">All existing reservations that are affected by the quantity adjustment in the short-picked location are re-reserved for the same batch.</span></span> <span data-ttu-id="f2e80-602">Kerfið úthlutar af handahófi staðsetningu og kennitala (ef staðsetningin er stjórnað með skiltum) þar sem magnið er fáanlegt.</span><span class="sxs-lookup"><span data-stu-id="f2e80-602">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f2e80-603">Nr</span><span class="sxs-lookup"><span data-stu-id="f2e80-603">No</span></span></td>
<td><span data-ttu-id="f2e80-604">Sjá fyrri línuna.</span><span class="sxs-lookup"><span data-stu-id="f2e80-604">See the previous row.</span></span></td>
<td><span data-ttu-id="f2e80-605">Sjá fyrri línuna.</span><span class="sxs-lookup"><span data-stu-id="f2e80-605">See the previous row.</span></span></td>
<td><span data-ttu-id="f2e80-606">Allar núverandi frátektir sem hafa áhrif á magnleiðréttingu á staðsetningu þar sem tiltekt er of lítil eru fjarlægðar.</span><span class="sxs-lookup"><span data-stu-id="f2e80-606">All existing reservations that are affected by the quantity adjustment in the short-picked location are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f2e80-607">Vinna undantekning frá <strong>Stutt val</strong> gerð er sett upp, hvar <strong>Endurúthlutun hlutar</strong> = <strong>Handvirkt</strong>, <strong>Stilla lager</strong> = <strong>Já</strong> og <strong>Fjarlægðu fyrirvara</strong> = <strong>Nei/Já</strong>.</span><span class="sxs-lookup"><span data-stu-id="f2e80-607">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No/Yes</strong>.</span></span> <span data-ttu-id="f2e80-608">Að auki, er <strong>Leyfa endurúthlutun handvirkra atriða</strong> valkostur virkur á starfsmanninum.</span><span class="sxs-lookup"><span data-stu-id="f2e80-608">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="f2e80-609">Já</span><span class="sxs-lookup"><span data-stu-id="f2e80-609">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="f2e80-610">Veljið valmyndaratriðið <strong>Of lítil tiltekt</strong> í farsímaforriti vöruhúsakerfis þegar tiltekt er keyrð.</span><span class="sxs-lookup"><span data-stu-id="f2e80-610">Select the <strong>Shortpick</strong> menu item on the Warehouse Management mobile app when you run picking work.</span></span></li>
<li><span data-ttu-id="f2e80-611">Í <strong>Magn með of litla tiltekt</strong> reitinn er fært inn <strong>0</strong> (núll).</span><span class="sxs-lookup"><span data-stu-id="f2e80-611">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="f2e80-612">Í <strong>Ástæða</strong> reit, veldu <strong>Stuttur velja með handvirkri úthlutun</strong>.</span><span class="sxs-lookup"><span data-stu-id="f2e80-612">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="f2e80-613">Veldu staðsetningu / kennitala á listanum.</span><span class="sxs-lookup"><span data-stu-id="f2e80-613">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="f2e80-614">Eftirfarandi aðgerðir eiga sér stað í núverandi vinnu:</span><span class="sxs-lookup"><span data-stu-id="f2e80-614">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="f2e80-615">Tínslulínan er lokuð og valið magn er 0 (núll).</span><span class="sxs-lookup"><span data-stu-id="f2e80-615">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="f2e80-616">Hætt er við að söluréttarlínuna.</span><span class="sxs-lookup"><span data-stu-id="f2e80-616">The put line is canceled.</span></span></li>
<li><span data-ttu-id="f2e80-617">Ný tiltektarlína er búin til.</span><span class="sxs-lookup"><span data-stu-id="f2e80-617">A new pick line is created.</span></span> <span data-ttu-id="f2e80-618">Það notar staðsetningu / númeraplötu sem notandinn valdi.</span><span class="sxs-lookup"><span data-stu-id="f2e80-618">It uses the location/license plate that the user selected.</span></span></li>
<li><span data-ttu-id="f2e80-619">Ný söluréttarlína er búin til.</span><span class="sxs-lookup"><span data-stu-id="f2e80-619">A new put line is created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="f2e80-620">Birgðafærsla <strong>Telja</strong> tegund og <strong>Selt</strong> útgáfutegund er búin til til að tákna aðlögunina.</span><span class="sxs-lookup"><span data-stu-id="f2e80-620">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="f2e80-621">Á ekki við</span><span class="sxs-lookup"><span data-stu-id="f2e80-621">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f2e80-622">Vinnuundantekning frá <strong>Stutt val</strong> gerð er sett upp, hvar <strong>Endurúthlutun hlutar</strong> = <strong>Handvirkt</strong>, <strong>Stilla lager</strong> = <strong>Já</strong> og <strong>Fjarlægðu fyrirvara</strong> = <strong>Nei</strong>.</span><span class="sxs-lookup"><span data-stu-id="f2e80-622">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span> <span data-ttu-id="f2e80-623">Að auki, er <strong>Leyfa endurúthlutun handvirkra atriða</strong> valkostur virkur á starfsmanninum.</span><span class="sxs-lookup"><span data-stu-id="f2e80-623">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="f2e80-624">Ekkert</span><span class="sxs-lookup"><span data-stu-id="f2e80-624">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="f2e80-625">Veljið valmyndaratriðið <strong>Of lítil tiltekt</strong> í farsímaforriti vöruhúsakerfis þegar tiltekt er keyrð.</span><span class="sxs-lookup"><span data-stu-id="f2e80-625">Select the <strong>Shortpick</strong> menu item on the Warehouse Management mobile app when you run picking work.</span></span></li>
<li><span data-ttu-id="f2e80-626">Í <strong>Magn með of litla tiltekt</strong> reitinn er fært inn <strong>0</strong> (núll).</span><span class="sxs-lookup"><span data-stu-id="f2e80-626">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="f2e80-627">Í <strong>Ástæða</strong> reit, veldu <strong>Stuttur velja með handvirkri úthlutun</strong>.</span><span class="sxs-lookup"><span data-stu-id="f2e80-627">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="f2e80-628">Of lítil tiltekt-aðgerðin mistekst og villu er hent.</span><span class="sxs-lookup"><span data-stu-id="f2e80-628">The short-picking action fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="f2e80-629">Á ekki við</span><span class="sxs-lookup"><span data-stu-id="f2e80-629">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f2e80-630">Vinnuundantekning frá <strong>Stutt val</strong> gerð er sett upp, hvar <strong>Endurúthlutun hlutar</strong> = <strong>Handvirkt</strong>, <strong>Stilla lager</strong> = <strong>Já</strong> og <strong>Fjarlægðu fyrirvara</strong> = <strong>Já</strong>.</span><span class="sxs-lookup"><span data-stu-id="f2e80-630">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span> <span data-ttu-id="f2e80-631">Að auki, er <strong>Leyfa endurúthlutun handvirkra atriða</strong> valkostur virkur á starfsmanninum.</span><span class="sxs-lookup"><span data-stu-id="f2e80-631">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="f2e80-632">Ekkert</span><span class="sxs-lookup"><span data-stu-id="f2e80-632">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="f2e80-633">Veljið valmyndaratriðið <strong>Of lítil tiltekt</strong> í farsímaforriti vöruhúsakerfis þegar tiltekt er keyrð.</span><span class="sxs-lookup"><span data-stu-id="f2e80-633">Select the <strong>Shortpick</strong> menu item on the Warehouse Management mobile app when you run picking work.</span></span></li>
<li><span data-ttu-id="f2e80-634">Í <strong>Magn með of litla tiltekt</strong> reitinn er fært inn <strong>0</strong> (núll).</span><span class="sxs-lookup"><span data-stu-id="f2e80-634">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="f2e80-635">Í <strong>Ástæða</strong> reit, veldu <strong>Stuttur velja með handvirkri úthlutun</strong>.</span><span class="sxs-lookup"><span data-stu-id="f2e80-635">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="f2e80-636">Veldu staðsetningu / kennitala á listanum.</span><span class="sxs-lookup"><span data-stu-id="f2e80-636">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="f2e80-637">Eftirfarandi aðgerðir eiga sér stað í núverandi vinnu:</span><span class="sxs-lookup"><span data-stu-id="f2e80-637">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="f2e80-638">Tínslulínan er lokuð og valið magn er 0 (núll).</span><span class="sxs-lookup"><span data-stu-id="f2e80-638">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="f2e80-639">Hætt er við að söluréttarlínuna.</span><span class="sxs-lookup"><span data-stu-id="f2e80-639">The put line is canceled.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="f2e80-640">Birgðafærsla <strong>Telja</strong> tegund og <strong>Selt</strong> útgáfutegund er búin til til að tákna aðlögunina.</span><span class="sxs-lookup"><span data-stu-id="f2e80-640">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="f2e80-641">Allar núverandi frátektir sem hafa áhrif á magnleiðréttingu á staðsetningu þar sem tiltekt er of lítil/númeraplötu eru fjarlægðar.</span><span class="sxs-lookup"><span data-stu-id="f2e80-641">All existing reservations that are affected by the quantity adjustment in the short-picked location/license plate are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f2e80-642">Vinnuundantekning frá <strong>Stutt val</strong> gerð er sett upp, hvar <strong>Endurúthlutun hlutar</strong> = <strong>Sjálfvirkt</strong>, <strong>Stilla lager</strong> = <strong>Já/Nei</strong> og <strong>Fjarlægðu fyrirvara</strong> = <strong>Já/Nei</strong>.</span><span class="sxs-lookup"><span data-stu-id="f2e80-642">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Automatic</strong>, <strong>Adjust inventory</strong> = <strong>Yes/No</strong>, and <strong>Remove reservations</strong> = <strong>Yes/No</strong>.</span></span></td>
<td><span data-ttu-id="f2e80-643">Ekki tiltækt</span><span class="sxs-lookup"><span data-stu-id="f2e80-643">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="f2e80-644">Veljið valmyndaratriðið <strong>Of lítil tiltekt</strong> í farsímaforriti vöruhúsakerfis þegar tiltekt er keyrð.</span><span class="sxs-lookup"><span data-stu-id="f2e80-644">Select the <strong>Shortpick</strong> menu item on the Warehouse Management mobile app when you run picking work.</span></span></li>
<li><span data-ttu-id="f2e80-645">Í <strong>Magn með of litla tiltekt</strong> reitinn er fært inn <strong>0</strong> (núll).</span><span class="sxs-lookup"><span data-stu-id="f2e80-645">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="f2e80-646">Í <strong>Ástæða</strong> reit, veldu <strong>Stuttur velja með sjálfvirkri endurúthlutun</strong>.</span><span class="sxs-lookup"><span data-stu-id="f2e80-646">In the <strong>Reason</strong> field, select <strong>Short Picking with automatic reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="f2e80-647">Ekki er stutt í skammval sem felur í sér sjálfvirka endurúthlutun.</span><span class="sxs-lookup"><span data-stu-id="f2e80-647">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
<td><span data-ttu-id="f2e80-648">Ekki er stutt í skammval sem felur í sér sjálfvirka endurúthlutun.</span><span class="sxs-lookup"><span data-stu-id="f2e80-648">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="change-the-inventory-status"></a><span data-ttu-id="f2e80-649">Breyta á birgðastöðunni</span><span class="sxs-lookup"><span data-stu-id="f2e80-649">Change the inventory status</span></span>

> [!NOTE]
> <span data-ttu-id="f2e80-650">Þessa vörugeymsluaðgerð er hægt að framkvæma frá mörgum inngangspunktum.</span><span class="sxs-lookup"><span data-stu-id="f2e80-650">This warehouse action can be performed from multiple entry points.</span></span> <span data-ttu-id="f2e80-651">Dæmið sem sýnt er hér notar **Breyting á birgðum** aðgerð á **Á lager eftir birgðageymslu** síðu.</span><span class="sxs-lookup"><span data-stu-id="f2e80-651">The example that is shown here uses **Inventory status change** action on the **On-hand by location** page.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="f2e80-652">Færibreyta lykiluppsetningar</span><span class="sxs-lookup"><span data-stu-id="f2e80-652">Key setup parameter</span></span></th>
<th><span data-ttu-id="f2e80-653">Runumagn er fáanlegt</span><span class="sxs-lookup"><span data-stu-id="f2e80-653">Batch quantity is available</span></span></th>
<th><span data-ttu-id="f2e80-654">Lykilþrep notenda</span><span class="sxs-lookup"><span data-stu-id="f2e80-654">Key user steps</span></span></th>
<th><span data-ttu-id="f2e80-655">Vinna vöruhúss</span><span class="sxs-lookup"><span data-stu-id="f2e80-655">Warehouse work</span></span></th>
<th><span data-ttu-id="f2e80-656">Pantanaskuldbundin hópapöntun</span><span class="sxs-lookup"><span data-stu-id="f2e80-656">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="f2e80-657">Á <strong>Vöruhús</strong> flipanum, í <strong>Vöruhús</strong> skrá, er <strong>Fjarlægja frátektir og merkingar</strong> reiturinn stilltur á <strong>Frátektir</strong> eða <strong>Merkingar og fyrirvarar</strong>.</span><span class="sxs-lookup"><span data-stu-id="f2e80-657">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>Reservations</strong> or <strong>Markings and reservations</strong>.</span></span></td>
<td><span data-ttu-id="f2e80-658">Já</span><span class="sxs-lookup"><span data-stu-id="f2e80-658">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="f2e80-659">Veldu tiltekna staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="f2e80-659">Select a specific location.</span></span></li>
<li><span data-ttu-id="f2e80-660">Veldu línu sem er með tiltekinn hlut, staðsetningu og númeraplötu (ef staðsetningin er stjórnað með skiltum).</span><span class="sxs-lookup"><span data-stu-id="f2e80-660">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="f2e80-661">Veldu <strong>Breyting á birgðastöðu</strong>.</span><span class="sxs-lookup"><span data-stu-id="f2e80-661">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="f2e80-662">Stilltu reitinn <strong>Staða birgða</strong> til <strong>Lokun</strong>.</span><span class="sxs-lookup"><span data-stu-id="f2e80-662">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="f2e80-663">Breytingar á birgðastöðu eru ekki leyfðar fyrir magn sem er frátekið fyrir vinnu.</span><span class="sxs-lookup"><span data-stu-id="f2e80-663">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="f2e80-664">Magnið er aftur frátekið fyrir sömu lotu.</span><span class="sxs-lookup"><span data-stu-id="f2e80-664">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="f2e80-665">Kerfið úthlutar af handahófi staðsetningu og kennitala (ef staðsetningin er stjórnað með skiltum) þar sem magnið er fáanlegt.</span><span class="sxs-lookup"><span data-stu-id="f2e80-665">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></li>
<li><span data-ttu-id="f2e80-666">Tvö birgðafærslur <strong>Breyting á birgðum</strong> gerð eru búin til til að tákna breytinguna á stöðu birgða.</span><span class="sxs-lookup"><span data-stu-id="f2e80-666">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="f2e80-667">Birgðafærsla af gerðinni <strong>Stöðvun birgða</strong> og gerð útreyfingar <strong>Frátekið á lager</strong> er búin til til að tákna fyrirvara á lokað magn.</span><span class="sxs-lookup"><span data-stu-id="f2e80-667">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="f2e80-668">Nr</span><span class="sxs-lookup"><span data-stu-id="f2e80-668">No</span></span></td>
<td><span data-ttu-id="f2e80-669">Sjá fyrri línuna.</span><span class="sxs-lookup"><span data-stu-id="f2e80-669">See the previous row.</span></span></td>
<td><span data-ttu-id="f2e80-670">Breytingar á birgðastöðu eru ekki leyfðar fyrir magn sem er frátekið fyrir vinnu.</span><span class="sxs-lookup"><span data-stu-id="f2e80-670">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="f2e80-671">Pöntunin er fjarlægð.</span><span class="sxs-lookup"><span data-stu-id="f2e80-671">The reservation is removed.</span></span></li>
<li><span data-ttu-id="f2e80-672">Tvö birgðafærslur <strong>Breyting á birgðum</strong> gerð eru búin til til að tákna breytinguna á stöðu birgða.</span><span class="sxs-lookup"><span data-stu-id="f2e80-672">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="f2e80-673">Birgðafærsla af gerðinni <strong>Stöðvun birgða</strong> og gerð útreyfingar <strong>Frátekið á lager</strong> er búin til til að tákna fyrirvara á lokað magn.</span><span class="sxs-lookup"><span data-stu-id="f2e80-673">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="f2e80-674">Á flipanum <strong>Vöruhús</strong>, í skránni <strong>Vöruhús</strong>, er reiturinn <strong>Fjarlægja frátektir og merkingar</strong> stilltur á <strong>Ekkert</strong>.</span><span class="sxs-lookup"><span data-stu-id="f2e80-674">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>None</strong>.</span></span></td>
<td><span data-ttu-id="f2e80-675">Já</span><span class="sxs-lookup"><span data-stu-id="f2e80-675">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="f2e80-676">Veldu tiltekna staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="f2e80-676">Select a specific location.</span></span></li>
<li><span data-ttu-id="f2e80-677">Veldu línu sem er með tiltekinn hlut, staðsetningu og númeraplötu (ef staðsetningin er stjórnað með skiltum).</span><span class="sxs-lookup"><span data-stu-id="f2e80-677">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="f2e80-678">Veldu <strong>Breyting á birgðastöðu</strong>.</span><span class="sxs-lookup"><span data-stu-id="f2e80-678">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="f2e80-679">Stilltu reitinn <strong>Staða birgða</strong> til <strong>Lokun</strong>.</span><span class="sxs-lookup"><span data-stu-id="f2e80-679">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="f2e80-680">Breytingar á birgðastöðu eru ekki leyfðar fyrir magn sem er frátekið fyrir vinnu.</span><span class="sxs-lookup"><span data-stu-id="f2e80-680">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="f2e80-681">Magnið er aftur frátekið fyrir sömu lotu.</span><span class="sxs-lookup"><span data-stu-id="f2e80-681">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="f2e80-682">Kerfið úthlutar af handahófi staðsetningu og kennitala (ef staðsetningin er stjórnað með skiltum) þar sem magnið er fáanlegt.</span><span class="sxs-lookup"><span data-stu-id="f2e80-682">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f2e80-683">Nr</span><span class="sxs-lookup"><span data-stu-id="f2e80-683">No</span></span></td>
<td><span data-ttu-id="f2e80-684">Sjá fyrri línuna.</span><span class="sxs-lookup"><span data-stu-id="f2e80-684">See the previous row.</span></span></td>
<td><span data-ttu-id="f2e80-685">Breytingar á birgðastöðu eru ekki leyfðar fyrir magn sem er frátekið fyrir vinnu.</span><span class="sxs-lookup"><span data-stu-id="f2e80-685">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="f2e80-686">Breytingar á birgðastöðu eru ekki leyfðar.</span><span class="sxs-lookup"><span data-stu-id="f2e80-686">Inventory status changes aren't allowed.</span></span></td>
</tr>
</tbody>
</table>

## <a name="limitations"></a><span data-ttu-id="f2e80-687">Takmarkanir</span><span class="sxs-lookup"><span data-stu-id="f2e80-687">Limitations</span></span>

- <span data-ttu-id="f2e80-688">Sveigjanleiki vörugeymsluvíddar pöntunaraðgerða styður ekki eftirfarandi eiginleika:</span><span class="sxs-lookup"><span data-stu-id="f2e80-688">The flexible warehouse-level dimension reservation functionality doesn't support the following features:</span></span>

    - <span data-ttu-id="f2e80-689">Stjórnun framleiðsluþyngdar</span><span class="sxs-lookup"><span data-stu-id="f2e80-689">Catch weight management</span></span>
    - <span data-ttu-id="f2e80-690">Efnislega neikvæð birgðastaða</span><span class="sxs-lookup"><span data-stu-id="f2e80-690">Physical negative inventory</span></span>
    - <span data-ttu-id="f2e80-691">Frátekt gegn pöntuðu framboði</span><span class="sxs-lookup"><span data-stu-id="f2e80-691">Reservation against ordered supply</span></span>
    - <span data-ttu-id="f2e80-692">Flytja pantanir og hráefni tína</span><span class="sxs-lookup"><span data-stu-id="f2e80-692">Transfer orders and raw material picking</span></span>

- <span data-ttu-id="f2e80-693">Reglugerð um gámasamstæðu fyrir pökkun með tilskipunareiningunni hefur takmarkanir.</span><span class="sxs-lookup"><span data-stu-id="f2e80-693">The container consolidation rule for packing by directive unit has limitations.</span></span> <span data-ttu-id="f2e80-694">Fyrir pöntunarbundna fyrirvara mælum við með að þú notir ekki sniðmát fyrir gámagerð þar sem **Pakkning eftir tilskipunareining** reiturinn er virkur.</span><span class="sxs-lookup"><span data-stu-id="f2e80-694">For order-committed reservations, we recommend that you not use container build templates where the **Pack by directive unit** field is enabled.</span></span> <span data-ttu-id="f2e80-695">Í núverandi hönnun eru staðsetningartilskipanir ekki notaðar þegar vörugeymsla er búin til.</span><span class="sxs-lookup"><span data-stu-id="f2e80-695">In the current design, location directives aren't used when warehouse work is created.</span></span> <span data-ttu-id="f2e80-696">Þess vegna er aðeins lægsta einingin í einingaröðarhópnum (birgðaeiningin) beitt á gámabylgjuskrefinu.</span><span class="sxs-lookup"><span data-stu-id="f2e80-696">Therefore, only the lowest unit in the unit sequence group (the inventory unit) is applied during the containerization wave step.</span></span>

## <a name="see-also"></a><span data-ttu-id="f2e80-697">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="f2e80-697">See also</span></span>

- [<span data-ttu-id="f2e80-698">Rununúmer í Vöruhúsakerfi</span><span class="sxs-lookup"><span data-stu-id="f2e80-698">Batch numbers in Warehouse management</span></span>](/dynamicsax-2012/appuser-itpro/batch-numbers-in-warehouse-management)
- [<span data-ttu-id="f2e80-699">Frátekning sömu runu fyrir sölupöntun</span><span class="sxs-lookup"><span data-stu-id="f2e80-699">Reserve the same batch for a sales order</span></span>](../sales-marketing/reserve-same-batch-sales-order.md)
- [<span data-ttu-id="f2e80-700">Tína elstu runu í fartæki</span><span class="sxs-lookup"><span data-stu-id="f2e80-700">Pick oldest batch on a mobile device</span></span>](pick-oldest-batch.md)
- [<span data-ttu-id="f2e80-701">Staðfesting lotu og númeraplötu</span><span class="sxs-lookup"><span data-stu-id="f2e80-701">Batch and license plate confirmation</span></span>](batch-and-license-plate-confirmation.md)
- [<span data-ttu-id="f2e80-702">Úrræðaleit fyrir frátekningar í vöruhúsakerfi</span><span class="sxs-lookup"><span data-stu-id="f2e80-702">Troubleshoot reservations in warehouse management</span></span>](troubleshoot-warehouse-reservations.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]