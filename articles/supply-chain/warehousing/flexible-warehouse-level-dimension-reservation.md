---
title: Sveigjanleg frátektarregla á vídd vöruhúsastigs
description: Þetta efni lýsir stefnuskrá fyrir birgða sem láta fyrirtæki sem selja vörur sem eru rekin með runur og reka flutninga sína sem aðgerðir með WMS-virka áskilja sértækar runur fyrir sölupantanir viðskiptavina, jafnvel þó að pöntunarveldið sem er tengt vörunum banni ekki fyrirvara á tilteknum runum.
author: perlynne
manager: tfehr
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReservationHierarchy, WHSWorkTrans, WHSWorkInventTrans, WHSInventTableReservationHierarchy, WHSReservationHierarchyCreate, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-01-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: b9bd4e67ed64218f9c4ac87bd143f73680af9ac4
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4430661"
---
# <a name="flexible-warehouse-level-dimension-reservation-policy"></a><span data-ttu-id="0190d-103">Sveigjanleg frátektarregla á vídd vöruhúsastigs</span><span class="sxs-lookup"><span data-stu-id="0190d-103">Flexible warehouse-level dimension reservation policy</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0190d-104">Þegar stigveldi birgða fyrirvara á „hópnum hér að neðan\[staðsetningu\]„ gerð er tengd vörum, fyrirtækjum sem selja vöru sem er rekin með hópum og rekur flutninga sína sem aðgerðir sem eru gerðar virkar fyrir Microsoft Dynamics 365 Warehouse Management System (WMS) getur ekki pantað sértæka runu af þessum vörum fyrir sölupantanir viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="0190d-104">When an inventory reservation hierarchy of the "Batch-below\[location\]" type is associated with products, businesses that sell batch-tracked products and run their logistics as operations that are enabled for the Microsoft Dynamics 365 Warehouse Management System (WMS) can't reserve specific batches of those products for customer sales orders.</span></span>

<span data-ttu-id="0190d-105">Á svipaðan hátt er ekki hægt að taka frá sérstakar númeraplötur fyrir afurðir í sölupöntunum þegar þessar afurðir eru tengdar við sjálfgefið frátekningarstigveldi.</span><span class="sxs-lookup"><span data-stu-id="0190d-105">In a similar way, specific license plates can't be reserved for products on sales orders when those products are associated with the default reservation hierarchy.</span></span>

<span data-ttu-id="0190d-106">Þetta efnisatriði lýsir frátekningarreglu birgða sem gerir þessum fyrirtækjum kleift að taka frá ákveðnar runur eða númeraplötur, jafnvel þegar afurðirnar eru tengdar frátekningarstigveldi „Runa fyrir neðan\[staðsetningu\]“.</span><span class="sxs-lookup"><span data-stu-id="0190d-106">This topic describes the inventory reservation policy that lets these businesses reserve specific batches or license plates, even when the products are associated with a "Batch-below\[location\]" reservation hierarchy.</span></span>

## <a name="inventory-reservation-hierarchy"></a><span data-ttu-id="0190d-107">Frátekningarstigveldi birgða</span><span class="sxs-lookup"><span data-stu-id="0190d-107">Inventory reservation hierarchy</span></span>

<span data-ttu-id="0190d-108">Þessi hluti dregur saman núverandi stigveldi birgða fyrirvara.</span><span class="sxs-lookup"><span data-stu-id="0190d-108">This section summarizes the existing inventory reservation hierarchy.</span></span>

<span data-ttu-id="0190d-109">Stigveldi birgðapöntunar ræður því að hvað varðar geymsluvíddir ber eftirspurnarpöntunin nauðsynlegar víddir á staðsetningu, vörugeymslu og birgðastöðu, en rökfræði vörugeymslu er ábyrg fyrir því að tengja staðsetningu við umbeðið magn og panta staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="0190d-109">The inventory reservation hierarchy dictates that, as far as storage dimensions are concerned, the demand order carries the mandatory dimensions of site, warehouse, and inventory status, whereas the warehouse logic is responsible for assigning a location to the requested quantities and reserving the location.</span></span> <span data-ttu-id="0190d-110">Með öðrum orðum, í samskiptum milli eftirspurnarpöntunar og vörugeymslu er gert ráð fyrir að eftirspurnarpöntunin gefi til kynna hvar pöntunin verður að vera send frá (það er, hvaða staður og vörugeymsla).</span><span class="sxs-lookup"><span data-stu-id="0190d-110">In other words, in the interactions between the demand order and the warehouse operations, the demand order is expected to indicate where the order must be shipped from (that is, what site and warehouse).</span></span> <span data-ttu-id="0190d-111">Vöruhúsið treystir síðan á rökfræði þess til að finna nauðsynlegt magn í húsnæði vörugeymslu.</span><span class="sxs-lookup"><span data-stu-id="0190d-111">The warehouse then relies on its logic to find the required quantity in the warehouse premises.</span></span>

<span data-ttu-id="0190d-112">Hins vegar, til að endurspegla rekstrarlíkan fyrirtækisins, eru mælingar á stærð (runu og raðnúmer) háð meiri sveigjanleika.</span><span class="sxs-lookup"><span data-stu-id="0190d-112">However, to reflect the operational model of the business, tracking dimensions (batch and serial numbers) are subject to more flexibility.</span></span> <span data-ttu-id="0190d-113">Stigveldi birgðapöntunar rúmar atburðarás þar sem eftirfarandi skilyrði eiga við:</span><span class="sxs-lookup"><span data-stu-id="0190d-113">An inventory reservation hierarchy can accommodate scenarios where the following conditions apply:</span></span>

- <span data-ttu-id="0190d-114">Fyrirtækið treystir á vörugeymslu sína til að stjórna töku á magni sem hefur lotu eða raðnúmer eftir að magnið hefur fundist í geymsluhúsnæðinu.</span><span class="sxs-lookup"><span data-stu-id="0190d-114">The business relies on its warehouse operations to manage picking of quantities that have batch or serial numbers after the quantities have been found in the warehousing storage space.</span></span> <span data-ttu-id="0190d-115">Oft er vísað til þessa líkans *Hópur-neðan\[staðsetningu\]*.</span><span class="sxs-lookup"><span data-stu-id="0190d-115">This model is often referred to as *Batch-below\[location\]*.</span></span> <span data-ttu-id="0190d-116">Það er venjulega notað þegar framleiðslueining vöru eða raðnúmer er ekki mikilvægt fyrir viðskiptavini sem setja eftirspurnina hjá sölufyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="0190d-116">It's typically used when a product's batch or serial number identification isn't important to the customers who place the demand with the selling company.</span></span>
- <span data-ttu-id="0190d-117">Ef lotu- eða raðnúmer eru hluti af pöntunarlýsingu viðskiptavinarins og þau eru skráð í eftirspurnarpöntun, eru vörugeymsluaðgerðirnar sem finna magn í vöruhúsinu takmarkaðar af sérstökum númerum sem óskað er eftir og hafa ekki leyfi til að breyta þeim.</span><span class="sxs-lookup"><span data-stu-id="0190d-117">If batch or serial numbers are part of a customer's order specification, and they are recorded on the demand order, the warehouse operations that find the quantities in the warehouse are constrained by the specific requested numbers and aren't allowed to change them.</span></span> <span data-ttu-id="0190d-118">Vísað er til þessa líkans *Hópur-ofan\[staðsetningu\]*.</span><span class="sxs-lookup"><span data-stu-id="0190d-118">This model is referred to as *Batch-above\[location\]*.</span></span>

<span data-ttu-id="0190d-119">Í þessum atburðarásum er áskorunin sú að aðeins er hægt að úthluta einum birgða pöntunarveldi fyrir hverja vöru sem gefin er út.</span><span class="sxs-lookup"><span data-stu-id="0190d-119">In these scenarios, the challenge is that only one inventory reservation hierarchy can be assigned to each released product.</span></span> <span data-ttu-id="0190d-120">Þess vegna, fyrir WMS til að meðhöndla rakta hluti, eftir að stigveldi verkefnisins ákvarðar hvenær á að panta lotu eða raðnúmer (annað hvort þegar eftirspurnarpöntunin er tekin eða meðan á pökkunarvinnu vörugeymslu stendur), er ekki hægt að breyta þessari tímasetningu í auglýsingu -hoc grundvöllur.</span><span class="sxs-lookup"><span data-stu-id="0190d-120">Therefore, for the WMS to handle tracked items, after the hierarchy assignment determines when the batch or serial number should be reserved (either when the demand order is taken or during the warehouse picking work), this timing can't be changed on an ad-hoc basis.</span></span>

## <a name="flexible-reservation-for-batch-tracked-items"></a><span data-ttu-id="0190d-121">Sveigjanlegur fyrirvari fyrir hluti sem rekja má hóp</span><span class="sxs-lookup"><span data-stu-id="0190d-121">Flexible reservation for batch-tracked items</span></span>

### <a name="business-scenario"></a><span data-ttu-id="0190d-122">Sviðsmynd fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="0190d-122">Business scenario</span></span>

<span data-ttu-id="0190d-123">Í þessari atburðarás notar fyrirtæki birgðarstefnu þar sem fullunnum vörum er rakið eftir lotunúmerum.</span><span class="sxs-lookup"><span data-stu-id="0190d-123">In this scenario, a company uses an inventory strategy where finished goods are tracked by batch numbers.</span></span> <span data-ttu-id="0190d-124">Þetta fyrirtæki notar einnig WMS vinnuálag.</span><span class="sxs-lookup"><span data-stu-id="0190d-124">This company also uses the WMS workload.</span></span> <span data-ttu-id="0190d-125">Vegna þess að þetta vinnuálag hefur vel útbúna röksemdafærslu til að skipuleggja og keyra vörugeymslu og flutningsaðgerðir fyrir hluti sem eru búnir til í hópum eru flestir fullbúnir hlutir tengdir „hópur hér að neðan\[staðsetningu\]" stigveldi birgða fyrirvara.</span><span class="sxs-lookup"><span data-stu-id="0190d-125">Because this workload has well-equipped logic for planning and running warehouse picking and shipping operations for batch-enabled items, most of the finished items are associated with a "Batch-below\[location\]" inventory reservation hierarchy.</span></span> <span data-ttu-id="0190d-126">Kosturinn við þessa tegund rekstraruppsetningar er að ákvörðunum (sem eru í raun fyrirvara um fyrirvaralausar ákvarðanir) um hvaða runur á að velja og hvar eigi að setja þær í vörugeymslunni er frestað þangað til að vörugeymsla hefst.</span><span class="sxs-lookup"><span data-stu-id="0190d-126">The advantage of this type of operational setup is that decisions (which are effectively reservation decisions) about which batches to pick and where to put them in the warehouse are postponed until the warehouse picking operations start.</span></span> <span data-ttu-id="0190d-127">Þeir eru ekki gerðir þegar pöntun viðskiptavinarins er sett.</span><span class="sxs-lookup"><span data-stu-id="0190d-127">They aren't made when the customer's order is placed.</span></span>

<span data-ttu-id="0190d-128">Þó að „hópurinn hér að neðan\[staðsetningu\]„ Pöntunarveldi þjónar vel markmiðum fyrirtækisins, margir af rótgrónum viðskiptavinum fyrirtækisins þurfa sömu lotu og þeir keyptu áður þegar þeir panta vörur.</span><span class="sxs-lookup"><span data-stu-id="0190d-128">Although the "Batch-below\[location\]" reservation hierarchy serves the company's business goals well, many of the company's established customers require the same batch that they previously purchased when they reorder products.</span></span> <span data-ttu-id="0190d-129">Þess vegna er fyrirtækið að leita að sveigjanleika í meðhöndlun reglna um röðun pöntunar svo að eftir atvikum viðskiptavina eftir sama hlut, gerist eftirfarandi hegðun:</span><span class="sxs-lookup"><span data-stu-id="0190d-129">Therefore, the company is looking for flexibility in the way that the batch reservation rules are handled, so that, depending on the customers' demand for the same item, the following behaviors occur:</span></span>

- <span data-ttu-id="0190d-130">Hægt er að skrá lotunúmer og panta þegar pöntunin er tekin af söluaðilanum og ekki er hægt að breyta því við vörugeymslu og / eða taka af öðrum kröfum.</span><span class="sxs-lookup"><span data-stu-id="0190d-130">A batch number can be recorded and reserved when the order is taken by the sales processor, and it can't be changed during warehouse operations and/or taken by other demands.</span></span> <span data-ttu-id="0190d-131">Þessi hegðun hjálpar til við að tryggja að lotunúmerið sem var pantað er sent til viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="0190d-131">This behavior helps guarantee that the batch number that was ordered is shipped to the customer.</span></span>
- <span data-ttu-id="0190d-132">Ef lotunúmerið er ekki mikilvægt fyrir viðskiptavininn, þá geta vörugeymsluaðgerðir ákvarðað lotunúmer meðan á vinnu stendur, eftir að skráning og pöntun sölupöntunar hefur verið gert.</span><span class="sxs-lookup"><span data-stu-id="0190d-132">If the batch number isn't important to the customer, the warehouse operations can determine a batch number during picking work, after sales order registration and reservation have been done.</span></span>

### <a name="allowing-reservation-of-a-specific-batch-on-the-sales-order"></a><span data-ttu-id="0190d-133">Leyfa fyrirvara um ákveðna lotu í sölupöntuninni</span><span class="sxs-lookup"><span data-stu-id="0190d-133">Allowing reservation of a specific batch on the sales order</span></span>

<span data-ttu-id="0190d-134">Til að koma til móts við æskilegan sveigjanleika í hegðun hóps fyrirvara fyrir hluti sem eru tengdir „hópur hér að neðan\[staðsetningu\]" stigveldi birgða fyrirvara, birgðasali verður að velja **Leyfa fyrirvara á pöntunarbeiðni** gátreitinn fyrir **Hópnúmer** stig á **Stigveldi birgða fyrirvara** síðu.</span><span class="sxs-lookup"><span data-stu-id="0190d-134">To accommodate the desired flexibility in the batch reservation behavior for items that are associated with a "Batch-below\[location\]" inventory reservation hierarchy, inventory managers must select the **Allow reservation on demand order** check box for the **Batch number** level on the **Inventory reservation hierarchies** page.</span></span>

![Stigveldi fyrir birgðafrátektir gert sveigjanlegt](media/Flexible-inventory-reservation-hierarchy.png)

<span data-ttu-id="0190d-136">Þegar stigið **Rununúmer** í stigveldinu er valið, allar víddir yfir því stigi og upp í gegnum **Staðsetning** stig verður sjálfkrafa valið.</span><span class="sxs-lookup"><span data-stu-id="0190d-136">When the **Batch number** level in the hierarchy is selected, all dimensions above that level and up through the **Location** level will be automatically selected.</span></span> <span data-ttu-id="0190d-137">(Sjálfgefið að allar víddir yfir **Staðsetning** stig eru valin.) Þessi hegðun endurspeglar rökfræði þar sem allar víddir á bilinu milli lotunúmers og staðsetningar eru einnig sjálfkrafa fráteknar eftir að þú hefur pantað tiltekið lotunúmer á pöntunarlínunni.</span><span class="sxs-lookup"><span data-stu-id="0190d-137">(By default, all dimensions above the **Location** level are preselected.) This behavior reflects the logic where all dimensions in the range between the batch number and location are also automatically reserved after you reserve a specific batch number on the order line.</span></span>

> [!NOTE]
> <span data-ttu-id="0190d-138">Gátreiturinn **Leyfa fyrirvara á pöntunarbeiðni** á aðeins við um stig stigveldis sem er undir staðsetningu víddar vörugeymslu.</span><span class="sxs-lookup"><span data-stu-id="0190d-138">The **Allow reservation on demand order** check box applies only to reservation hierarchy levels that are below the warehouse location dimension.</span></span>
>
> <span data-ttu-id="0190d-139">**Rununúmer** og **Númeraplata** eru einu stigin í stigveldinu sem eru opin fyrir sveigjanlegu frátekningarreglunni.</span><span class="sxs-lookup"><span data-stu-id="0190d-139">**Batch number** and **License plate** are the only levels in the hierarchy that are open for the flexible reservation policy.</span></span> <span data-ttu-id="0190d-140">Með öðrum orðum er ekki hægt að velja gátreitinn **Leyfa frátekt á eftirspurnarpöntun** fyrir stig **Staðsetningar** eða **Raðnúmers**.</span><span class="sxs-lookup"><span data-stu-id="0190d-140">In other words, you can't select the **Allow reservation on demand order** check box for the **Location** or **Serial number** level.</span></span>
>
> <span data-ttu-id="0190d-141">Ef pöntunarveldið þitt inniheldur röð raðnúmera (sem verður alltaf að vera undir **Rununúmer** stig), og ef þú hefur kveikt á lotusértækum fyrirvara fyrir lotunúmerið mun kerfið halda áfram að sjá um röðun og tína aðgerðir á raðnúmerum, byggt á reglunum sem eiga við um „Rað-neðan\[staðsetningu\]" fyrirvara stefnu.</span><span class="sxs-lookup"><span data-stu-id="0190d-141">If your reservation hierarchy includes the serial number dimension (which must always be below the **Batch number** level), and if you've turned on batch-specific reservation for the batch number, the system will continue to handle serial number reservation and picking operations, based on the rules that apply to the "Serial-below\[location\]" reservation policy.</span></span>

<span data-ttu-id="0190d-142">Hvenær sem er geturðu leyft lotusértæka pöntun fyrir núverandi „runu hér að neðan\[staðsetningu\]" pöntunarveldi í uppsetningu þinni.</span><span class="sxs-lookup"><span data-stu-id="0190d-142">At any point, you can allow batch-specific reservation for an existing "Batch-below\[location\]" reservation hierarchy in your deployment.</span></span> <span data-ttu-id="0190d-143">Þessi breyting mun ekki hafa áhrif á neina fyrirvara og opna vöruhúsavinnu sem voru búin til áður en breytingin átti sér stað.</span><span class="sxs-lookup"><span data-stu-id="0190d-143">This change won't affect any reservations and open warehouse work that were created before the change occurred.</span></span> <span data-ttu-id="0190d-144">Hins vegar **Leyfa fyrirvara á pöntunarbeiðni** Ekki er hægt að hreinsa gátreitinn ef birgðafærslur á **Frátekið pantað**, **Frátekin líkamleg**, eða **Pantaði** útgáfutegund er til fyrir einn eða fleiri hluti sem eru tengdir því pöntunarveldi.</span><span class="sxs-lookup"><span data-stu-id="0190d-144">However, the **Allow reservation on demand order** check box can't be cleared if inventory transactions of the **Reserved ordered**, **Reserved physical**, or **Ordered** issue type exist for one or more items that are associated with that reservation hierarchy.</span></span>

> [!NOTE]
> <span data-ttu-id="0190d-145">Ef núverandi fyrirvaralegveldi hlutar leyfir ekki forskrift lotur í pöntuninni, þá geturðu endurúthlutað því í pöntunarveldi sem gerir kleift að skilgreina lotu, að því tilskildu að stigskipulag stigveldisins sé það sama í báðum stigveldum.</span><span class="sxs-lookup"><span data-stu-id="0190d-145">If an item's existing reservation hierarchy doesn't allow batch specification on the order, you can reassign it to a reservation hierarchy that does allow batch specification, provided that the hierarchy level structure is the same in both hierarchies.</span></span> <span data-ttu-id="0190d-146">Nota **Breyta pöntunarveldi fyrir hluti** virka til að framkvæma endurúthlutun.</span><span class="sxs-lookup"><span data-stu-id="0190d-146">Use the **Change reservation hierarchy for items** function to do the reassignment.</span></span> <span data-ttu-id="0190d-147">Þessi breyting gæti skipt máli þegar þú vilt koma í veg fyrir sveigjanlegan pöntunarhluta fyrir hlutmengi af hlutum sem eru rekin í hópum en leyfa það fyrir restina af vöruframboði.</span><span class="sxs-lookup"><span data-stu-id="0190d-147">This change might be relevant when you want to prevent flexible batch reservation for a subset of batch-tracked items but allow it for the rest of the product portfolio.</span></span>

<span data-ttu-id="0190d-148">Óháð því hvort þú hefur valið **Leyfa fyrirvara á pöntunarbeiðni** gátreitinn, ef þú vilt ekki panta sérstakt lotunúmer fyrir hlutinn á pöntunarlínu, þá er sjálfgefin rökfræði aðgerða vörugeymsla sem gildir fyrir „Hóp hér að neðan\[staðsetningu\]" fyrirkomulag stigveldi mun enn eiga við.</span><span class="sxs-lookup"><span data-stu-id="0190d-148">Regardless of whether you've selected the **Allow reservation on demand order** check box, if you don't want to reserve a specific batch number for the item on an order line, default warehouse operations logic that is valid for a "Batch-below\[location\]" reservation hierarchy will still apply.</span></span>

### <a name="reserve-a-specific-batch-number-for-a-customer-order"></a><span data-ttu-id="0190d-149">Pantaðu tiltekið lotunúmer fyrir pöntun viðskiptavina</span><span class="sxs-lookup"><span data-stu-id="0190d-149">Reserve a specific batch number for a customer order</span></span>

<span data-ttu-id="0190d-150">Eftir hlut sem er rekja hópur er „Hópur hér að neðan\[staðsetningu\]„ Stigveldi birgðapöntunar er sett upp til að leyfa fyrirvara á tilteknum lotunúmerum á sölupöntunum, sölupöntunaraðilar geta tekið pantanir viðskiptavina fyrir sama hlut á einn af eftirfarandi leiðum, allt eftir beiðni viðskiptavinarins:</span><span class="sxs-lookup"><span data-stu-id="0190d-150">After a batch-tracked item's "Batch-below\[location\]" inventory reservation hierarchy is set up to allow reservation of specific batch numbers on sales orders, sales order processors can take customer orders for the same item in one of the following ways, depending on the customer's request:</span></span>

- <span data-ttu-id="0190d-151">**Sláðu inn pöntunarupplýsingar án þess að tilgreina lotunúmer** - Þessa nálgun ætti að nota þegar framleiðslulota vöru er ekki mikilvæg fyrir viðskiptavininn.</span><span class="sxs-lookup"><span data-stu-id="0190d-151">**Enter order details without specifying a batch number** – This approach should be used when the product's batch specification isn't important to the customer.</span></span> <span data-ttu-id="0190d-152">Allir núverandi ferlar sem tengjast meðhöndlun pöntunar af þessari gerð kerfisins eru óbreytt.</span><span class="sxs-lookup"><span data-stu-id="0190d-152">All existing processes that are associated with handling an order of this type in the system remain unchanged.</span></span> <span data-ttu-id="0190d-153">Engin viðbótarsjónarmið eru nauðsynleg af hálfu notenda.</span><span class="sxs-lookup"><span data-stu-id="0190d-153">No additional considerations are required on the part of users.</span></span>
- <span data-ttu-id="0190d-154">**Sláðu inn pöntunarupplýsingar og pantaðu tiltekið lotunúmer** - Þessa aðferð ætti að nota þegar viðskiptavinurinn óskar eftir ákveðinni lotu.</span><span class="sxs-lookup"><span data-stu-id="0190d-154">**Enter order details and reserve a specific batch number** – This approach should be used when the customer requests a specific batch.</span></span> <span data-ttu-id="0190d-155">Venjulega munu viðskiptavinir biðja um ákveðna lotu þegar þeir eru að panta vöru sem þeir keyptu áður.</span><span class="sxs-lookup"><span data-stu-id="0190d-155">Typically, customers will request a specific batch when they are reordering a product that they previously purchased.</span></span> <span data-ttu-id="0190d-156">Þessari tegund af sértækum pöntunum er vísað til *pöntunarbundinn fyrirvara*.</span><span class="sxs-lookup"><span data-stu-id="0190d-156">This type of batch-specific reservation is referred to as *order-committed reservation*.</span></span>

<span data-ttu-id="0190d-157">Eftirfarandi reglur eru í gildi þegar magn er afgreitt og lotunúmer er skuldbundið til sérstakrar pöntunar:</span><span class="sxs-lookup"><span data-stu-id="0190d-157">The following set of rules is valid when quantities are processed, and a batch number is committed to a specific order:</span></span>

- <span data-ttu-id="0190d-158">Til að leyfa fyrirvara á ákveðnu lotunúmeri fyrir hlut undir „Hópur hér að neðan\[staðsetningu\]" pöntunarstefna, kerfið verður að panta allar víddir upp í gegnum staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="0190d-158">To allow reservation of a specific batch number for an item under the "Batch-below\[location\]" reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="0190d-159">Þetta svið inniheldur venjulega stærð skírteinisins.</span><span class="sxs-lookup"><span data-stu-id="0190d-159">This range typically includes the license plate dimension.</span></span>
- <span data-ttu-id="0190d-160">Staðsetningartilskipanir eru ekki notaðar þegar val á vinnu er búið til fyrir sölulínu sem notar pöntunarbundna hópapöntun.</span><span class="sxs-lookup"><span data-stu-id="0190d-160">Location directives aren't used when picking work is created for a sales line that uses order-committed batch reservation.</span></span>
- <span data-ttu-id="0190d-161">Við vinnslu vörugeymslu á vinnu fyrir pöntunarbundna lotur er hvorki notanda né kerfinu heimilt að breyta lotunúmerinu.</span><span class="sxs-lookup"><span data-stu-id="0190d-161">During warehouse processing of work for order-committed batches, neither the user nor the system is allowed to change the batch number.</span></span> <span data-ttu-id="0190d-162">(Þessi vinnsla felur í sér meðhöndlun undantekninga.)</span><span class="sxs-lookup"><span data-stu-id="0190d-162">(This processing includes exception handling.)</span></span>

<span data-ttu-id="0190d-163">Eftirfarandi dæmi sýnir flæði frá enda til enda.</span><span class="sxs-lookup"><span data-stu-id="0190d-163">The following example shows the end-to-end flow.</span></span>

## <a name="example-scenario-batch-number-allocation"></a><span data-ttu-id="0190d-164">Sýniaðstæður: Úthlutun rununúmers</span><span class="sxs-lookup"><span data-stu-id="0190d-164">Example scenario: Batch number allocation</span></span>

<span data-ttu-id="0190d-165">Fyrir þetta dæmi verða kynningargögn að vera sett upp og þú verður að nota kynningarfyrirtækið **USMF**.</span><span class="sxs-lookup"><span data-stu-id="0190d-165">For this example, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="set-up-an-inventory-reservation-hierarchy-to-allow-batch-specific-reservation"></a><a name="Example-batch-allocation"></a><span data-ttu-id="0190d-166">Setjið upp stigveldi birgða fyrirvara til að leyfa ákveðna pöntun</span><span class="sxs-lookup"><span data-stu-id="0190d-166">Set up an inventory reservation hierarchy to allow batch-specific reservation</span></span>

1. <span data-ttu-id="0190d-167">Fara til **Vöruhúsastjórnun** \> **Skipulag** \> **Birgðir \> Pöntunarveldi**.</span><span class="sxs-lookup"><span data-stu-id="0190d-167">Go to **Warehouse management** \> **Setup** \> **Inventory \> Reservation hierarchy**.</span></span>
2. <span data-ttu-id="0190d-168">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="0190d-168">Select **New**.</span></span>
3. <span data-ttu-id="0190d-169">Í reitnum **Heiti** skaltu slá inn nafn (til dæmis **BatchFlex**).</span><span class="sxs-lookup"><span data-stu-id="0190d-169">In the **Name** field, enter a name (for example, **BatchFlex**).</span></span>
4. <span data-ttu-id="0190d-170">Í reitinn **Lýsing** slærðu inn lýsingu (t.d. **Hópur fyrir neðan sveigjanlegan**).</span><span class="sxs-lookup"><span data-stu-id="0190d-170">In the **Description** field, enter a description (for example, **Batch below flexible**).</span></span>
5. <span data-ttu-id="0190d-171">Í reitinn **Valinn**, veldu **Raðnúmer** og **Eigandi** og veldu síðan vinstri örvarhnappinn til að færa þá í reitinn **Tiltækt**.</span><span class="sxs-lookup"><span data-stu-id="0190d-171">In the **Selected** field, select **Serial number** and **Owner**, and then select the left arrow button to move them to the **Available** field.</span></span>
6. <span data-ttu-id="0190d-172">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="0190d-172">Select **OK**.</span></span>
7. <span data-ttu-id="0190d-173">Í röðinni fyrir **Hópnúmer** víddarstig, veldu **Leyfa fyrirvara á pöntunarbeiðni** gátreitinn.</span><span class="sxs-lookup"><span data-stu-id="0190d-173">In the row for the **Batch number** dimension level, select the **Allow reservation on demand order** check box.</span></span> <span data-ttu-id="0190d-174">Stigin **Númeraplata** og **Staðsetning** eru sjálfkrafa valin og þú getur ekki hreinsað gátreitina fyrir þá.</span><span class="sxs-lookup"><span data-stu-id="0190d-174">The **License plate** and **Location** levels are automatically selected, and you can't clear the check boxes for them.</span></span>
8. <span data-ttu-id="0190d-175">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="0190d-175">Select **Save**.</span></span>

### <a name="create-a-new-released-product"></a><span data-ttu-id="0190d-176">Stofna nýja útgefna afurð</span><span class="sxs-lookup"><span data-stu-id="0190d-176">Create a new released product</span></span>

1. <span data-ttu-id="0190d-177">Stilltu þrjár aðalgagnabreytur vörunnar með því að nota þessi gildi:</span><span class="sxs-lookup"><span data-stu-id="0190d-177">Set the product's three master data parameters by using these values:</span></span>

    - <span data-ttu-id="0190d-178">Í reitnum **Geymsluvíddarflokkur** velurðu **Ware**.</span><span class="sxs-lookup"><span data-stu-id="0190d-178">In the **Storage dimension group** field, select **Ware**.</span></span>
    - <span data-ttu-id="0190d-179">Í reitnum **Rakningarvíddarflokkur** velurðu **Batch-Phy**.</span><span class="sxs-lookup"><span data-stu-id="0190d-179">In the **Tracking dimension group** field, select **Batch-Phy**.</span></span>
    - <span data-ttu-id="0190d-180">Í skjámyndinni **Frátektastigveldi** velurðu **BatchFlex**.</span><span class="sxs-lookup"><span data-stu-id="0190d-180">In the **Reservation hierarchy** field, select **BatchFlex**.</span></span>

2. <span data-ttu-id="0190d-181">Búðu til tvö lotunúmer, svo sem **B11** og **B22**.</span><span class="sxs-lookup"><span data-stu-id="0190d-181">Create two batch numbers, such as **B11** and **B22**.</span></span>
3. <span data-ttu-id="0190d-182">Bættu magni hlutar við á lager með því að nota eftirfarandi gildi.</span><span class="sxs-lookup"><span data-stu-id="0190d-182">Add item quantities to on-hand stock by using the following values.</span></span>

    | <span data-ttu-id="0190d-183">Vöruhús</span><span class="sxs-lookup"><span data-stu-id="0190d-183">Warehouse</span></span> | <span data-ttu-id="0190d-184">Rununúmer</span><span class="sxs-lookup"><span data-stu-id="0190d-184">Batch number</span></span> | <span data-ttu-id="0190d-185">Staðsetning</span><span class="sxs-lookup"><span data-stu-id="0190d-185">Location</span></span> | <span data-ttu-id="0190d-186">Númeraplata</span><span class="sxs-lookup"><span data-stu-id="0190d-186">License plate</span></span> | <span data-ttu-id="0190d-187">Magn</span><span class="sxs-lookup"><span data-stu-id="0190d-187">Quantity</span></span> |
    |-----------|--------------|----------|---------------|----------|
    | <span data-ttu-id="0190d-188">24</span><span class="sxs-lookup"><span data-stu-id="0190d-188">24</span></span>        | <span data-ttu-id="0190d-189">B11</span><span class="sxs-lookup"><span data-stu-id="0190d-189">B11</span></span>          | <span data-ttu-id="0190d-190">BULK-001</span><span class="sxs-lookup"><span data-stu-id="0190d-190">BULK-001</span></span> | <span data-ttu-id="0190d-191">Enginn</span><span class="sxs-lookup"><span data-stu-id="0190d-191">None</span></span>          | <span data-ttu-id="0190d-192">10</span><span class="sxs-lookup"><span data-stu-id="0190d-192">10</span></span>       |
    | <span data-ttu-id="0190d-193">24</span><span class="sxs-lookup"><span data-stu-id="0190d-193">24</span></span>        | <span data-ttu-id="0190d-194">B11</span><span class="sxs-lookup"><span data-stu-id="0190d-194">B11</span></span>          | <span data-ttu-id="0190d-195">FL-001</span><span class="sxs-lookup"><span data-stu-id="0190d-195">FL-001</span></span>   | <span data-ttu-id="0190d-196">LP11</span><span class="sxs-lookup"><span data-stu-id="0190d-196">LP11</span></span>          | <span data-ttu-id="0190d-197">10</span><span class="sxs-lookup"><span data-stu-id="0190d-197">10</span></span>       |
    | <span data-ttu-id="0190d-198">24</span><span class="sxs-lookup"><span data-stu-id="0190d-198">24</span></span>        | <span data-ttu-id="0190d-199">B22</span><span class="sxs-lookup"><span data-stu-id="0190d-199">B22</span></span>          | <span data-ttu-id="0190d-200">FL-002</span><span class="sxs-lookup"><span data-stu-id="0190d-200">FL-002</span></span>   | <span data-ttu-id="0190d-201">LP22</span><span class="sxs-lookup"><span data-stu-id="0190d-201">LP22</span></span>          | <span data-ttu-id="0190d-202">10</span><span class="sxs-lookup"><span data-stu-id="0190d-202">10</span></span>       |

### <a name="enter-sales-order-details"></a><a name="sales-order-details"></a><span data-ttu-id="0190d-203">Slá inn upplýsingar um sölupöntun</span><span class="sxs-lookup"><span data-stu-id="0190d-203">Enter sales order details</span></span>

1. <span data-ttu-id="0190d-204">Farðu í **Sölu og markaðssetningu** \> **Sölupantanir** \> **Allar sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="0190d-204">Go to **Sales and marketing** \> **Sales orders** \> **All sales orders**.</span></span>
2. <span data-ttu-id="0190d-205">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="0190d-205">Select **New**.</span></span>
3. <span data-ttu-id="0190d-206">Í sölupöntunarhausnum, í reitnum **Viðskiptavinur reikningur** slærðu inn **US-003**.</span><span class="sxs-lookup"><span data-stu-id="0190d-206">On the sales order header, in the **Customer account** field, enter **US-003**.</span></span>
4. <span data-ttu-id="0190d-207">Bættu við línu fyrir nýja vöru og sláðu inn **10** sem magnið.</span><span class="sxs-lookup"><span data-stu-id="0190d-207">Add a line for the new item, and enter **10** as the quantity.</span></span> <span data-ttu-id="0190d-208">Gangið úr skugga um að reiturinn **Vöruhús** er stillt á **24**.</span><span class="sxs-lookup"><span data-stu-id="0190d-208">Make sure that the **Warehouse** field is set to **24**.</span></span>
5. <span data-ttu-id="0190d-209">Á flýtiflipanum **Sölupöntunarlínur**, veldu **Birgðir** og síðan, í hópnum **Viðhalda**, veldu **Hópapöntun**.</span><span class="sxs-lookup"><span data-stu-id="0190d-209">On the **Sales order lines** FastTab, select **Inventory**, and then, in the **Maintain** group, select **Batch reservation**.</span></span> <span data-ttu-id="0190d-210">Síðan **Hópapöntun** sýnir lista yfir lotur sem hægt er að panta fyrir pöntunarlínuna.</span><span class="sxs-lookup"><span data-stu-id="0190d-210">The **Batch reservation** page shows a list of batches that are available for reservation for the order line.</span></span> <span data-ttu-id="0190d-211">Fyrir þetta dæmi sýnir það magn af **20** fyrir lotunúmer **B11** og magn af **10** fyrir lotunúmer **B22**.</span><span class="sxs-lookup"><span data-stu-id="0190d-211">For this example, it shows a quantity of **20** for batch number **B11** and a quantity of **10** for batch number **B22**.</span></span> <span data-ttu-id="0190d-212">Athugaðu að **Hópapöntun** síðu er ekki hægt að nálgast frá línu ef hluturinn á þeirri línu er tengdur „Hópur hér að neðan\[staðsetningu\]" pöntunarveldi nema að það sé sett upp til að leyfa ákveðna pöntun.</span><span class="sxs-lookup"><span data-stu-id="0190d-212">Note that the **Batch reservation** page cannot be accessed from a line if the item on that line is associated with "Batch-below\[location\]" reservation hierarchy unless it is set up to allow batch-specific reservation.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0190d-213">Til að panta ákveðna lotu fyrir sölupöntun verður þú að nota síðuna **Hópapöntun**.</span><span class="sxs-lookup"><span data-stu-id="0190d-213">To reserve a specific batch for a sales order, you must use the **Batch reservation** page.</span></span>
    >
    > <span data-ttu-id="0190d-214">Ef þú slærð inn lotunúmerið beint á sölupöntunarlínunni mun kerfið haga sér eins og þú hafir slegið inn sérstakt lotugildi fyrir hlut sem er háð „hópnum hér að neðan\[staðsetningu\]" fyrirvara stefnu.</span><span class="sxs-lookup"><span data-stu-id="0190d-214">If you enter the batch number directly on the sales order line, the system will behave as though you entered a specific batch value for an item that is subject to the "Batch-below\[location\]" reservation policy.</span></span> <span data-ttu-id="0190d-215">Þegar þú vistar línuna færðu viðvörunarskilaboð.</span><span class="sxs-lookup"><span data-stu-id="0190d-215">When you save the line, you will receive a warning message.</span></span> <span data-ttu-id="0190d-216">Ef þú staðfestir að tilgreina skuli lotunúmerið beint á pöntunarlínunni verður línan ekki meðhöndluð samkvæmt reglulegri vörugeymslu stjórnunar.</span><span class="sxs-lookup"><span data-stu-id="0190d-216">If you confirm that the batch number should be specified directly on the order line, the line won't be handled by the regular warehouse management logic.</span></span>
    >
    > <span data-ttu-id="0190d-217">Ef þú áskilur magnið af síðunni **Fyrirvari**, engin sérstök lota verður frátekin og framkvæmd vörugeymsluaðgerða fyrir línuna mun fylgja þeim reglum sem gilda undir „Hópur hér að neðan\[staðsetningu\]" fyrirvara stefnu.</span><span class="sxs-lookup"><span data-stu-id="0190d-217">If you reserve the quantity from the **Reservation** page, no specific batch will be reserved, and the execution of warehouse operations for the line will follow the rules that are applicable under the "Batch-below\[location\]" reservation policy.</span></span>

    <span data-ttu-id="0190d-218">Almennt virkar þessi síða og er samspiluð á sama hátt og hún virkar og er samspiluð þeim með atriðum sem hafa tilheyrandi frátektarveldi „Hópurinn hér að ofan\[staðsetningu\]" gerð.</span><span class="sxs-lookup"><span data-stu-id="0190d-218">In general, this page works and is interacted with in the same way that it works and is interacted with for items that have an associated reservation hierarchy of the "Batch-above\[location\]" type.</span></span> <span data-ttu-id="0190d-219">Eftirfarandi undantekningar eiga þó við:</span><span class="sxs-lookup"><span data-stu-id="0190d-219">However, the following exceptions apply:</span></span>

    - <span data-ttu-id="0190d-220">Flýtiflipinn **Hópatölur skuldbundnar til upprunalínu** sýnir lotunúmerin sem eru frátekin fyrir pöntunarlínuna.</span><span class="sxs-lookup"><span data-stu-id="0190d-220">The **Batch numbers committed to source line** FastTab shows the batch numbers that are reserved for the order line.</span></span> <span data-ttu-id="0190d-221">Runugildin í hnitanetinu verða sýnd í gegnum allan uppfyllingartíma pöntunarlínunnar, þar á meðal stig vöruhúsavinnslunnar.</span><span class="sxs-lookup"><span data-stu-id="0190d-221">The batch values in the grid will be shown throughout the fulfillment cycle of the order line, including the warehouse processing stages.</span></span> <span data-ttu-id="0190d-222">Aftur á móti, á flýtiflipanum **Yfirlit**, venjulegur pöntunarlínupöntun (það er fyrirvari sem er gerður fyrir málin fyrir ofan **Staðsetning** stig) er sýnt í töflunni upp að því marki þegar vörugeymsla er búin til.</span><span class="sxs-lookup"><span data-stu-id="0190d-222">By contrast, on the **Overview** FastTab, regular order line reservation (that is, reservation that is done for the dimensions above the **Location** level) is shown in the grid up to the point when warehouse work is created.</span></span> <span data-ttu-id="0190d-223">Vinnuaðilinn tekur svo við línupöntuninni og línupöntunin birtist ekki lengur á síðunni.</span><span class="sxs-lookup"><span data-stu-id="0190d-223">The work entity then takes over the line reservation, and the line reservation no longer appears on the page.</span></span> <span data-ttu-id="0190d-224">Flýtiflipinn **Hópatölur skuldbundnar til upprunalínu** hjálpar til við að ábyrgjast að sölupöntunaraðili getur skoðað lotunúmerin sem voru skuldbundin pöntun viðskiptavinarins hvenær sem er á líftíma hans, upp í gegnum reikninga.</span><span class="sxs-lookup"><span data-stu-id="0190d-224">The **Batch numbers committed to source line** FastTab helps guarantee that the sales order processor can view the batch numbers that were committed to the customer's order at any point during its lifecycle, up through invoicing.</span></span>
    - <span data-ttu-id="0190d-225">Auk þess að panta sértæka lotu getur notandi valið handvirkt sértækan stað og framleiðslueiningar plötunnar í stað þess að láta kerfið velja þá sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="0190d-225">In addition to reserving a specific batch, a user can manually select the batch's specific location and license plate instead of letting the system automatically select them.</span></span> <span data-ttu-id="0190d-226">Þessi hæfileiki tengist hönnun pöntunarbundins fyrirkomulags fyrir pöntun.</span><span class="sxs-lookup"><span data-stu-id="0190d-226">This capability is related to the design of the order-committed batch reservation mechanism.</span></span> <span data-ttu-id="0190d-227">Eins og nefnt var áður, þegar rununúmer er tekið frá fyrir vöru undir „Hópur hér að neðan\[staðsetningu\]" pöntunarstefna, kerfið verður að panta allar víddir upp í gegnum staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="0190d-227">As was mentioned earlier, when a batch number is reserved for an item under the "Batch-below\[location\]" reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="0190d-228">Þess vegna mun vörugeymsla hafa sömu geymsluvíddir og notendurnir sem unnu með pantanirnar áskildu og það gæti ekki alltaf táknað geymslu hlutarins sem er þægilegt eða jafnvel mögulegt fyrir tínaaðgerðir.</span><span class="sxs-lookup"><span data-stu-id="0190d-228">Therefore, warehouse work will carry the same storage dimensions that were reserved by the users who worked with the orders, and it might not always represent the item storage placement that is convenient, or even possible, for picking operations.</span></span> <span data-ttu-id="0190d-229">Ef pöntunaraðilar eru meðvitaðir um takmarkanir vörugeymslu, gætu þeir viljað handvirkt velja tiltekna staði og leyfismerki þegar þeir panta hóp.</span><span class="sxs-lookup"><span data-stu-id="0190d-229">If order processors are aware of the warehouse constraints, they might want to manually select the specific locations and license plates when they reserve a batch.</span></span> <span data-ttu-id="0190d-230">Í þessu tilfelli verður notandinn að nota **Sýna mál** virkni á síðuhausnum og verður að bæta við staðsetningu og kennitala í ristina á flýtiflipanum **Yfirlit**.</span><span class="sxs-lookup"><span data-stu-id="0190d-230">In this case, the user must use the **Display dimensions** functionality on the page header, and must add the location and license plate in the grid on the **Overview** FastTab.</span></span>

6. <span data-ttu-id="0190d-231">Á **Hópapöntun** síðu, veldu línuna fyrir hópinn **B11** og veldu síðan **Varalína**.</span><span class="sxs-lookup"><span data-stu-id="0190d-231">On the **Batch reservation** page, select the line for batch **B11**, and then select **Reserve line**.</span></span> <span data-ttu-id="0190d-232">Það er engin tiltekin rökfræði til að úthluta staðsetningum og skiltum við sjálfvirka fyrirvara.</span><span class="sxs-lookup"><span data-stu-id="0190d-232">There is no designated logic for assigning locations and license plates during automatic reservation.</span></span> <span data-ttu-id="0190d-233">Þú getur slegið inn magnið handvirkt í reitinn **Frátekning**.</span><span class="sxs-lookup"><span data-stu-id="0190d-233">You can manually enter the quantity in the **Reservation** field.</span></span> <span data-ttu-id="0190d-234">Taktu eftir því að á flýtiflipanum **Hópatölur skuldbundnar til upprunalínu**, hópur **B11** er sýnt sem **Skuldbundinn**.</span><span class="sxs-lookup"><span data-stu-id="0190d-234">Notice that, on the **Batch numbers committed to source line** FastTab, batch **B11** is shown as **Committed**.</span></span>

    ![Að fremja ákveðið lotunúmer í sölupöntunarlínu á síðu síðu frátektar á runu](media/Batch-reservation-form-with-order-committed-reservation.png)

    > [!NOTE]
    > <span data-ttu-id="0190d-236">Bókun magns á sölupöntunarlínu er hægt að gera í mörgum lotum.</span><span class="sxs-lookup"><span data-stu-id="0190d-236">Reservation of the quantity on a sales order line can be done across multiple batches.</span></span> <span data-ttu-id="0190d-237">Sömuleiðis er hægt að panta sömu lotu gagnvart mörgum stöðum og skiltum (ef leyfisplötur eru virkar fyrir staðina).</span><span class="sxs-lookup"><span data-stu-id="0190d-237">Likewise, reservation of the same batch can be done against multiple locations and license plates (if license plates are enabled for the locations).</span></span>
    >
    > <span data-ttu-id="0190d-238">Pöntun á tiltekinni lotu fyrir magnið á sölupöntunarlínu getur einnig verið að hluta.</span><span class="sxs-lookup"><span data-stu-id="0190d-238">Reservation of a specific batch for the quantity on a sales order line can also be partial.</span></span> <span data-ttu-id="0190d-239">Til dæmis er hægt að panta heildarmagn 100 eininga þannig að ákveðin lota er skuldbundin til 20 eininga en 80 einingar eru fráteknar á staðnum og vörugeymslustigi fyrir alla tiltæka lotu.</span><span class="sxs-lookup"><span data-stu-id="0190d-239">For example, the total quantity of 100 units can be reserved so that a specific batch is committed to 20 units, whereas 80 units are reserved at the site and warehouse levels for any available batch.</span></span> <span data-ttu-id="0190d-240">Í þessu tilfelli mun WMS sjá um tínaaðgerðir með því að nota tvær aðskildar vinnulínur.</span><span class="sxs-lookup"><span data-stu-id="0190d-240">In this case, the WMS will handle picking operations by using two separate work lines.</span></span>

7. <span data-ttu-id="0190d-241">Farðu í **Afurðaupplýsingastjórnun** \> **Afurðir** \> **Losaðar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="0190d-241">Go to **Product information management** \> **Products** \> **Released products**.</span></span> <span data-ttu-id="0190d-242">Veldu hlutinn þinn og veldu síðan **Stjórna birgðum** \> **Skoða** \> **Færslur**.</span><span class="sxs-lookup"><span data-stu-id="0190d-242">Select your item, and then select **Manage inventory** \> **View** \> **Transactions**.</span></span>

    ![Pöntunarbundin fyrirvara sem birgðafærslugerð](media/Inventory-transactions-for-order-committed-reservation.png)

8. <span data-ttu-id="0190d-244">Skoðaðu birgðafærslur hlutarins sem tengjast pöntun sölupöntunarlínunnar.</span><span class="sxs-lookup"><span data-stu-id="0190d-244">Review the item's inventory transactions that are related to the sales order line reservation.</span></span>

    - <span data-ttu-id="0190d-245">Viðskipti þar sem **Tilvísun** reiturinn er stilltur á **Sölupöntun** og **Mál** reiturinn er stilltur á **Frátekin líkamleg** táknar pöntunarlínu fyrirvara fyrir birgðavíddir fyrir ofan **Staðsetning** stigi.</span><span class="sxs-lookup"><span data-stu-id="0190d-245">A transaction where the **Reference** field is set to **Sales order** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the inventory dimensions above the **Location** level.</span></span> <span data-ttu-id="0190d-246">Samkvæmt stigveldi birgðapöntunar hlutanna eru þessar víddir staða, vörugeymsla og birgðastaða.</span><span class="sxs-lookup"><span data-stu-id="0190d-246">According to the item's inventory reservation hierarchy, those dimensions are site, warehouse, and inventory status.</span></span>
    - <span data-ttu-id="0190d-247">Viðskipti þar sem reiturinn **Tilvísun** er stilltur á **Pöntunarbundna frátekt** og reiturinn **Úthreyfing** er stilltur á **Frátekið á lager** táknar pöntunarlínu frátektar fyrir tiltekna runu og annar birgðavíddir fyrir ofan hana.</span><span class="sxs-lookup"><span data-stu-id="0190d-247">A transaction where the **Reference** field is set to **Order-committed reservation** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the specific batch and all inventory dimensions above it.</span></span> <span data-ttu-id="0190d-248">Samkvæmt stigveldi birgðapöntunar hlutanna eru þessar víddir rununúmer og staðsetning.</span><span class="sxs-lookup"><span data-stu-id="0190d-248">According to the item's inventory reservation hierarchy, those dimensions are batch number and location.</span></span> <span data-ttu-id="0190d-249">Í þessu dæmi er staðsetningin **Magn-001**.</span><span class="sxs-lookup"><span data-stu-id="0190d-249">In this example, the location is **Bulk-001**.</span></span>

9. <span data-ttu-id="0190d-250">Veldu á sölupöntunarhaus **Vöruhús** \> **Aðgerðir** \> **Losa í vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="0190d-250">On the sales order header, select **Warehouse** \> **Actions** \> **Release to warehouse**.</span></span> <span data-ttu-id="0190d-251">Pöntunarlínan hefur verið sett í bylgju og álag og vinna búin til.</span><span class="sxs-lookup"><span data-stu-id="0190d-251">The order line is now waved, and a load and work are created.</span></span>

### <a name="review-and-process-warehouse-work-that-has-order-committed-batch-numbers"></a><span data-ttu-id="0190d-252">Farið yfir og unnið úr vöruhúsagerð sem er með pöntunarbundna lotunúmer</span><span class="sxs-lookup"><span data-stu-id="0190d-252">Review and process warehouse work that has order-committed batch numbers</span></span>

1. <span data-ttu-id="0190d-253">Á flýtiflipanum **Sölupöntunarlínur**, veldu **Vöruhús** \> **Upplýsingar um vinnu**.</span><span class="sxs-lookup"><span data-stu-id="0190d-253">On the **Sales order lines** FastTab, select **Warehouse** \> **Work details**.</span></span>

    <span data-ttu-id="0190d-254">Vinnan sem annast tínsluaðgerðina fyrir magn magn sem skuldbundið sig til sölupöntunarlínunnar hefur eftirfarandi einkenni:</span><span class="sxs-lookup"><span data-stu-id="0190d-254">The work that handles the picking operation for batch quantities that are committed to the sales order line has the following characteristics:</span></span>

    - <span data-ttu-id="0190d-255">Til að búa til vinnu notar kerfið vinnusniðmát en ekki staðsetningartilskipanir.</span><span class="sxs-lookup"><span data-stu-id="0190d-255">To create work, the system uses work templates but not location directives.</span></span> <span data-ttu-id="0190d-256">Öllum stöðluðum stillingum sem eru skilgreindar fyrir vinnusniðmát, svo sem hámarksfjölda vallína eða ákveðin mælieining, verður beitt til að ákvarða hvenær ný vinna ætti að búa til.</span><span class="sxs-lookup"><span data-stu-id="0190d-256">All the standard settings that are defined for work templates, such as a maximum number of pick lines or a specific unit of measure, will be applied to determine when new work should be created.</span></span> <span data-ttu-id="0190d-257">Hins vegar er ekki tekið tillit til reglnanna sem eru tengdar staðsetningarleiðbeiningum til að bera kennsl á valstöðum, vegna þess að pöntunin sem framin er fyrir pöntunin tilgreinir þegar allar birgðarvíddirnar.</span><span class="sxs-lookup"><span data-stu-id="0190d-257">However, the rules that are associated with location directives for identifying pick locations aren't considered, because the order-committed reservation already specifies all the inventory dimensions.</span></span> <span data-ttu-id="0190d-258">Þessar birgðastærðir innihalda mál á lagergeymslu stigsins.</span><span class="sxs-lookup"><span data-stu-id="0190d-258">Those inventory dimensions include the dimensions at the warehouse storage level.</span></span> <span data-ttu-id="0190d-259">Þess vegna erfðir verkið þessar víddir án þess að þurfa að hafa samráð um staðsetningartilskipanir.</span><span class="sxs-lookup"><span data-stu-id="0190d-259">Therefore, the work inherits those dimensions without having to consult location directives.</span></span>
    - <span data-ttu-id="0190d-260">Hópnúmerið er ekki sýnt á velja línunni (eins og á við um vinnulínuna sem er búin til fyrir hlut sem er með tilheyrandi „hópur hér að ofan\[staðsetningu\]„ fyrirvara stigveldi.) Í staðinn eru„ frá “lotunúmerinu og öllum öðrum geymsluvíddum sýndar á verkbirgðir vinnu línunnar sem vísað er til úr tilheyrandi birgðafærslum.</span><span class="sxs-lookup"><span data-stu-id="0190d-260">The batch number isn't shown on the pick line (as is the case for the work line that is created for an item that has an associated "Batch-above\[location\]" reservation hierarchy.) Instead, the "from" batch number and all other storage dimensions are shown on the work line's work inventory transaction that is referenced from the associated inventory transactions.</span></span>

        ![Vörugeymslufærsla vegna vinnu sem er upprunnin í pöntunarbundinni frátekt](media/Work-inventory-transactions-for-order-committed-reservation.png)

    - <span data-ttu-id="0190d-262">Eftir að vinna er búin til, birgðir hlutarins þar sem **Tilvísun** reiturinn er stilltur á **Pöntunarbundin frátekt** er fjarlægður.</span><span class="sxs-lookup"><span data-stu-id="0190d-262">After work is created, the item's inventory transaction where the **Reference** field is set to **Order-committed reservation** is removed.</span></span> <span data-ttu-id="0190d-263">Birgðafærslan þar sem **Tilvísun** reiturinn er stilltur á **Vinna** geymir nú líkamlegan fyrirvara á öllum birgðastærðum magnsins.</span><span class="sxs-lookup"><span data-stu-id="0190d-263">The inventory transaction where the **Reference** field is set to **Work** now holds the physical reservation on all the quantity's inventory dimensions.</span></span>

        <span data-ttu-id="0190d-264">Vöruhúsaaðgerðir geta haldið áfram til að sjá um framkvæmd verksins á venjulegan hátt.</span><span class="sxs-lookup"><span data-stu-id="0190d-264">Warehouse operations can proceed to handle execution of the work in the usual manner.</span></span> <span data-ttu-id="0190d-265">Leiðbeiningarnar í farsímanum munu hins vegar leiðbeina starfsmanni að velja ákveðið lotunúmer.</span><span class="sxs-lookup"><span data-stu-id="0190d-265">However, the instructions on the mobile device will instruct the worker to pick a specific batch number.</span></span> <span data-ttu-id="0190d-266">Í vöruhúsumhverfi þar sem staðsetningar eru stjórnaðar með leyfi fyrir skiltum, eftir að starfsmaður hefur náð staðsetningu sem geymir sömu framleiðslulotu á mörgum skiltum, þá getur hann eða hún valið af hvaða skilti sem er ekki þegar frátekinn (til dæmis með annarri pöntun- skuldbundinn fyrirvara eða vinnu sem er upprunnin í fyrirvara af þeirri gerð.)</span><span class="sxs-lookup"><span data-stu-id="0190d-266">In warehouse environments where locations are license plate–controlled, after a worker reaches a location that stores the same batch on multiple license plates, he or she can pick from any license plate that isn't already reserved (for example, by another order-committed reservation or work that originates from a reservation of that type.)</span></span>

        <span data-ttu-id="0190d-267">Ef það reynist óframkvæmanlegt að velja frá þeim stað sem er tilgreindur á vinnulínunni geta rekstraraðilar vörugeymslu notað eina af eftirfarandi aðgerðum til að beina því að velja ákveðna lotu frá þægilegri stað:</span><span class="sxs-lookup"><span data-stu-id="0190d-267">If it turns out to be impractical to pick from the location that is specified on the work line, the warehouse operators can use one of the following actions to redirect picking of the specific batch from a more convenient location:</span></span>

        - <span data-ttu-id="0190d-268">Staðallinn **Hnekkja staðsetningu** aðgerð í farsíma (að því tilskildu að starfsmaður vörugeymslu **Leyfa val á staðsetningu staðsetningu** stilling er virk)</span><span class="sxs-lookup"><span data-stu-id="0190d-268">The standard **Override location** action on a mobile device (provided that the warehouse worker's **Allow pick location override** setting is enabled)</span></span>
        - <span data-ttu-id="0190d-269">Aðgerðin **Breyta staðsetningu** á **Upplýsingar um vinnulista** síðu.</span><span class="sxs-lookup"><span data-stu-id="0190d-269">The **Change location** action on the **Work list details** page.</span></span> 

2. <span data-ttu-id="0190d-270">Ljúktu við að velja og setja verkið í farsímann.</span><span class="sxs-lookup"><span data-stu-id="0190d-270">On the mobile device, finish picking and putting the work.</span></span>

    <span data-ttu-id="0190d-271">Magnið **10** fyrir lotunúmer **B11** er nú valinn í sölupöntunarlínuna og settur í **Afgreiðsluhurð** staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="0190d-271">The quantity of **10** for batch number **B11** is now picked for the sales order line and put in the **Baydoor** location.</span></span> <span data-ttu-id="0190d-272">Á þessum tímapunkti er það tilbúið að hlaða það á vörubílinn og senda á heimilisfang viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="0190d-272">At this point, it's ready to be loaded onto the truck and dispatched to the customer's address.</span></span>

## <a name="flexible-license-plate-reservation"></a><span data-ttu-id="0190d-273">Sveigjanleg frátekning númeraplötu</span><span class="sxs-lookup"><span data-stu-id="0190d-273">Flexible license plate reservation</span></span>

### <a name="business-scenario"></a><span data-ttu-id="0190d-274">Sviðsmynd fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="0190d-274">Business scenario</span></span>

<span data-ttu-id="0190d-275">Í þessum aðstæðum notar fyrirtæki vöruhúsakerfi og vinnuferli og sér um hleðsluáætlun á stigi einstakra bretta/gáma utan Supply Chain Management áður en vinna er stofnuð.</span><span class="sxs-lookup"><span data-stu-id="0190d-275">In this scenario, a company uses warehouse management and work processing, and handles load planning at the level of individual pallets/containers outside Supply Chain Management before work is created.</span></span> <span data-ttu-id="0190d-276">Þessir gámar eru táknaðir með númeraplötum í birgðavíddunum.</span><span class="sxs-lookup"><span data-stu-id="0190d-276">These containers are represented by license plates in the inventory dimensions.</span></span> <span data-ttu-id="0190d-277">Fyrir þessa nálgun þarf þar af leiðandi að úthluta sérstökum númeraplötum fyrirfram á sölupöntunarlínur áður en tiltekt er gerð.</span><span class="sxs-lookup"><span data-stu-id="0190d-277">Therefore, for this approach, specific license plates must be pre-assigned to sales order lines before picking work is done.</span></span> <span data-ttu-id="0190d-278">Fyrirtækið leitar að sveigjanleika í því hvernig reglur um frátekningu númeraplötu eru meðhöndlaðar, þannig að eftirfarandi hegðun eigi sér stað:</span><span class="sxs-lookup"><span data-stu-id="0190d-278">The company is looking for flexibility in the way that the license plate reservation rules are handled, so that the following behaviors occur:</span></span>

- <span data-ttu-id="0190d-279">Hægt er að skrá og taka frá númeraplötu þegar pöntunin er tekin af úrvinnsluaðila sölumála og ekki er hægt að taka hana af öðrum eftirspurnum.</span><span class="sxs-lookup"><span data-stu-id="0190d-279">A license plate can be recorded and reserved when the order is taken by the sales processor, and it can't be taken by other demands.</span></span> <span data-ttu-id="0190d-280">Þessi hegðun hjálpar til við að tryggja að númeraplatan sem var áætluð sé send til viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="0190d-280">This behavior helps guarantee that the license plate that was planned is shipped to the customer.</span></span>
- <span data-ttu-id="0190d-281">Ef númeraplötunni hefur ekki þegar verið úthlutað á sölupöntunarlínu, getur starfsmaður í vöruhúsi valið númeraplötu meðan á tiltekt stendur, þegar búið er að ljúka skráningu sölupöntunar og frátekningu.</span><span class="sxs-lookup"><span data-stu-id="0190d-281">If the license plate isn't already assigned to a sales order line, warehouse personnel can select a license plate during picking work, after sales order registration and reservation are completed.</span></span>

### <a name="turn-on-flexible-license-plate-reservation"></a><span data-ttu-id="0190d-282">Kveikja á sveigjanlegri frátekningu númeraplötu</span><span class="sxs-lookup"><span data-stu-id="0190d-282">Turn on flexible license plate reservation</span></span>

<span data-ttu-id="0190d-283">Áður en hægt er að nota sveigjanlega frátekningu númeraplötu, þarf að kveikja á tveimur eiginleikum í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="0190d-283">Before you can use flexible license plate reservation, two features must be turned on in your system.</span></span> <span data-ttu-id="0190d-284">Stjórnendur geta notað stillingar [eiginleikastjórnunar](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikanna og kveikja á þeim ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="0190d-284">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the features and turn them on if they are required.</span></span> <span data-ttu-id="0190d-285">Kveikja verður á eiginleikunum í eftirfarandi röð:</span><span class="sxs-lookup"><span data-stu-id="0190d-285">You must turn on the features in the following order:</span></span>

1. <span data-ttu-id="0190d-286">**Heiti eiginleika:** *Sveigjanleg frátekt á vídd vöruhúsastigs*</span><span class="sxs-lookup"><span data-stu-id="0190d-286">**Feature name:** *Flexible warehouse-level dimension reservation*</span></span>
1. <span data-ttu-id="0190d-287">**Heiti eiginleika:** *Sveigjanleg frátekt á númeraplötu ráðstafaðrar pöntunar*</span><span class="sxs-lookup"><span data-stu-id="0190d-287">**Feature name:** *Flexible order-committed license plate reservation*</span></span>

### <a name="reserve-a-specific-license-plate-on-the-sales-order"></a><span data-ttu-id="0190d-288">Taka frá tiltekna númeraplötu í sölupöntuninni</span><span class="sxs-lookup"><span data-stu-id="0190d-288">Reserve a specific license plate on the sales order</span></span>

<span data-ttu-id="0190d-289">Til að virkja frátekningu á númeraplötu í pöntun þarf að velja gátreitinn **Leyfa frátekt á eftirspurnarpöntun** fyrir stigið **Númeraplata** á síðunni **Frátekningarstigveldi birgða** fyrir stigveldið sem tengist viðkomandi vöru.</span><span class="sxs-lookup"><span data-stu-id="0190d-289">To enable license plate reservation on an order, you must select the **Allow reservation on demand order** check box for the **License plate** level on the **Inventory reservation hierarchies** page for the hierarchy that is associated with the relevant item.</span></span>

![Síða frátekningarstigveldis birgða fyrir frátekningarstigveldi sveigjanlegrar númeraplötu](media/Flexible-LP-reservation-hierarchy.png)

<span data-ttu-id="0190d-291">Hægt er að virkja frátekningu á númeraplötu í pöntuninni hvenær sem er í uppsetningunni.</span><span class="sxs-lookup"><span data-stu-id="0190d-291">You can enable license plate reservation on the order at any point in your deployment.</span></span> <span data-ttu-id="0190d-292">Þessi breyting hefur ekki áhrif á neinar frátekningar eða opna vöruhúsavinnu sem var stofnuð áður en breytingin var gerð.</span><span class="sxs-lookup"><span data-stu-id="0190d-292">This change won't affect any reservations or open warehouse work that were created before the change occurred.</span></span> <span data-ttu-id="0190d-293">Hins vegar er ekki hægt að hreinsa gátreitinn **Leyfa frátekt á eftirspurnarpöntun** ef opnar birgðafærslur á útleið sem eru með úthreyfingarstöðuna *Í pöntun*, *Frátekið pantað* eða *Frátekið efnislegt magn* eru til fyrir eina eða fleiri vörur sem tengjast þessu frátekningarstigveldi.</span><span class="sxs-lookup"><span data-stu-id="0190d-293">However, you can't clear the **Allow reservation on demand order** check box if open outbound inventory transactions that have an issue status of *On order*, *Reserved ordered*, or *Reserved physical* exist for one or more items that are associated with that reservation hierarchy.</span></span>

<span data-ttu-id="0190d-294">Jafnvel ef gátreiturinn **Leyfa frátekt á eftirspurnarpöntun** er valinn fyrir stigið **Númeraplata** er enn mögulegt að *ekki* taka frá tiltekna númeraplötu í pöntuninni.</span><span class="sxs-lookup"><span data-stu-id="0190d-294">Even if the **Allow reservation on demand order** check box is selected for the **License plate** level, it's still possible *not* to reserve a specific license plate on the order.</span></span> <span data-ttu-id="0190d-295">Í slíku tilfelli gilda sjálfgefin rök vöruhúsaaðgerða fyrir frátekningarstigveldið.</span><span class="sxs-lookup"><span data-stu-id="0190d-295">In this case, the default warehouse operations logic that is valid for the reservation hierarchy applies.</span></span>

<span data-ttu-id="0190d-296">Til að taka frá tiltekna númeraplötu verður að nota ferlið [Samskiptaregla opinna gagna (OData)](../../fin-ops-core/dev-itpro/data-entities/odata.md). Í forritinu er hægt að gera þessa frátekningu beint úr sölupöntun með því að nota valkostinn **Frátektir á ráðstöfuðum pöntunum eftir númeraplötu** fyrir skipunina **Opna í Excel**.</span><span class="sxs-lookup"><span data-stu-id="0190d-296">To reserve a specific license plate, you must use an [Open Data Protocol (OData)](../../fin-ops-core/dev-itpro/data-entities/odata.md) process.In the application, you can do this reservation directly from a sales order by using the **Order-committed reservations per license plate** option of the **Open in Excel** command.</span></span> <span data-ttu-id="0190d-297">Í einingagögnunum sem opnuð eru í Excel-innbótinni þarf að færa inn eftirfarandi frátektartengd gögn og síðan velja **Birta** til að senda gögnin aftur í Supply Chain Management:</span><span class="sxs-lookup"><span data-stu-id="0190d-297">In the entity data that is opened in the Excel add-in, you must enter the following reservation-related data and then select **Publish** to send the data back to Supply Chain Management:</span></span>

- <span data-ttu-id="0190d-298">Tilvísun (eingöngu gildið *Sölupöntun* er stutt.)</span><span class="sxs-lookup"><span data-stu-id="0190d-298">Reference (Only the *Sales order* value is supported.)</span></span>
- <span data-ttu-id="0190d-299">Pöntunarnúmer (gildið er hægt að fá úr lotu.)</span><span class="sxs-lookup"><span data-stu-id="0190d-299">Order number (The value can be derived from the lot.)</span></span>
- <span data-ttu-id="0190d-300">Lotukenni</span><span class="sxs-lookup"><span data-stu-id="0190d-300">Lot ID</span></span>
- <span data-ttu-id="0190d-301">Númeraplata</span><span class="sxs-lookup"><span data-stu-id="0190d-301">License plate</span></span>
- <span data-ttu-id="0190d-302">Magn</span><span class="sxs-lookup"><span data-stu-id="0190d-302">Quantity</span></span>

<span data-ttu-id="0190d-303">Ef taka þarf frá tiltekna númeraplötu fyrir runurakta vöru skal nota síðuna **Frátekt á runu**, eins og lýst er í hlutanum [Færa inn upplýsingar um sölupöntun](#sales-order-details).</span><span class="sxs-lookup"><span data-stu-id="0190d-303">If you must reserve a specific license plate for a batch-tracked item, use the **Batch reservation** page, as described in the [Enter sales order details](#sales-order-details) section.</span></span>

<span data-ttu-id="0190d-304">Þegar sölupöntunarlína sem notar frátekt á númeraplötu ráðstafaðrar pöntunar er unnin af vöruhúsaaðgerðum, eru staðsetningarleiðbeiningar ekki notaðar.</span><span class="sxs-lookup"><span data-stu-id="0190d-304">When the sales order line that uses an order-committed license plate reservation is processed by warehouse operations, location directives aren't used.</span></span>

<span data-ttu-id="0190d-305">Ef vinnuliður vöruhúss samanstendur af línum sem jafngilda heilu bretti og eru með númeraplöturáðstafað magn, er hægt að fínstilla tiltektina með því að nota valmyndaratriði fartækis þar sem valkosturinn **Meðhöndla eftir númeraplötu** er stilltur á *Já*.</span><span class="sxs-lookup"><span data-stu-id="0190d-305">If a warehouse work item consists of lines that equal a complete pallet and have license plate–committed quantities, you can optimize the picking process by using a mobile device menu item where the **Handle by license plate** option is set to *Yes*.</span></span> <span data-ttu-id="0190d-306">Starfsmaður í vöruhúsi getur síðan skannað númeraplötu til að ljúka tiltekt í stað þess að þurfa að skanna vörurnar úr vinnunni hver á eftir annarri.</span><span class="sxs-lookup"><span data-stu-id="0190d-306">A warehouse worker can then scan a license plate to complete a pick instead of having to scan the items from the work one by one.</span></span>

![Valmyndaratriði fartækis þar sem valkosturinn „Meðhöndla eftir númeraplötu" er stilltur á „Já“](media/Handle-by-LP-menu-item.png)

<span data-ttu-id="0190d-308">Vegna þess að virknin **Meðhöndla eftir númeraplötu** styður ekki vinnu sem nær yfir mörg bretti, er betra að vera með aðskilinn vinnulið fyrir mismunandi númeraplötur.</span><span class="sxs-lookup"><span data-stu-id="0190d-308">Because the **Handle by license plate** functionality doesn't support work that covers multiple pallets, it's better to have a separate work item for different license plates.</span></span> <span data-ttu-id="0190d-309">Til að nota þessa aðferð skal bæta reitnum **Númeraplötukenni ráðstafaðrar pöntunar** sem vinnuhausaskil á síðunni **Vinnusniðmát**.</span><span class="sxs-lookup"><span data-stu-id="0190d-309">To use this approach, add the **Order-committed license plate ID** field as a work header break on the **Work template** page.</span></span>

> [!NOTE]
> <span data-ttu-id="0190d-310">Fyrir stofnferli á vinnu ráðstafaðrar pöntunar, verður gildinu „birgðavíddir ráðstafaðrar pöntunar“ úthlutað á vinnulínur tiltektar og ekki verið mögulegt að skoða gildið á númeraplötunni með beinum hætti.</span><span class="sxs-lookup"><span data-stu-id="0190d-310">For the order-committed work creation process, an "order-committed inventory dimension" value will be assigned to the picking work lines, and it won't be possible to view the license plate value directly.</span></span> <span data-ttu-id="0190d-311">Aðeins *Notandastýrt* ferli er stutt þegar valmyndaratriði fartækis er sett upp.</span><span class="sxs-lookup"><span data-stu-id="0190d-311">Only the *User directed* process is supported when setting up a mobile device menu item.</span></span>

## <a name="example-scenario-set-up-and-process-an-order-committed-license-plate-reservation"></a><span data-ttu-id="0190d-312">Dæmi: Setja upp og vinna úr frátekt á númeraplötu ráðstafaðrar pöntunar</span><span class="sxs-lookup"><span data-stu-id="0190d-312">Example scenario: Set up and process an order-committed license plate reservation</span></span>

<span data-ttu-id="0190d-313">Þessi atburðarás sýnir hvernig á að setja upp og vinna úr frátekt á númeraplötu ráðstafaðrar pöntunar.</span><span class="sxs-lookup"><span data-stu-id="0190d-313">This scenario shows how to set up and process an order-committed license plate reservation.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="0190d-314">Bjóða upp á sýnigögn</span><span class="sxs-lookup"><span data-stu-id="0190d-314">Make demo data available</span></span>

<span data-ttu-id="0190d-315">Þessi atburðarás vísar í gildi og færslur sem eru innifalin í stöðluðum sýnigögnum sem boðið er upp á fyrir Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="0190d-315">This scenario refers to values and records that are included in the standard demo data that is provided for Supply Chain Management.</span></span> <span data-ttu-id="0190d-316">Ef ætlunin er að fara í gegnum atburðarásina með því að nota gildin sem hér eru gefin skal gæta þess að vinna í umhverfi þar sem sýnigögnin eru uppsett.</span><span class="sxs-lookup"><span data-stu-id="0190d-316">If you want to work through the scenario by using the values that are provided here, be sure to work on an environment where the demo data is installed.</span></span> <span data-ttu-id="0190d-317">Þar að auki skal stilla lögaðilann á **USMF** áður en hafist er handa.</span><span class="sxs-lookup"><span data-stu-id="0190d-317">Additionally, set the legal entity to **USMF** before you begin.</span></span>

### <a name="create-an-inventory-reservation-hierarchy-that-allows-for-license-plate-reservation"></a><span data-ttu-id="0190d-318">Stofna frátekningarstigveldi birgða sem leyfir frátekningu á númeraplötu</span><span class="sxs-lookup"><span data-stu-id="0190d-318">Create an inventory reservation hierarchy that allows for license plate reservation</span></span>

1. <span data-ttu-id="0190d-319">Fara í **Vöruhúsakerfi \> Uppsetning \> Birgðir \> Frátekningarstigveldi**.</span><span class="sxs-lookup"><span data-stu-id="0190d-319">Go to **Warehouse management \> Setup \> Inventory \> Reservation hierarchy**.</span></span>
1. <span data-ttu-id="0190d-320">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="0190d-320">Select **New**.</span></span>
1. <span data-ttu-id="0190d-321">Í reitinn **Heiti** skal slá inn gildi (til dæmis *FlexibleLP*).</span><span class="sxs-lookup"><span data-stu-id="0190d-321">In the **Name** field, enter a value (for example, *FlexibleLP*).</span></span>
1. <span data-ttu-id="0190d-322">Í reitinn **Lýsing** skal færa inn gildi (til dæmis *Sveigjanleg frátekning á númeraplötu*).</span><span class="sxs-lookup"><span data-stu-id="0190d-322">In the **Description** field, enter a value (for example, *Flexible LP reservation*).</span></span>
1. <span data-ttu-id="0190d-323">Í listanum **Valið** skal velja **Rununúmer**, **Raðnúmer** og **Eigandi**.</span><span class="sxs-lookup"><span data-stu-id="0190d-323">In the **Selected** list, select **Batch number**, **Serial number**, and **Owner**.</span></span>
1. <span data-ttu-id="0190d-324">Veljið hnappinn **Fjarlægja** ![ör til baka](media/backward-button.png) til að flytja valdar færslur í listann **Tiltækt**.</span><span class="sxs-lookup"><span data-stu-id="0190d-324">Select the **Remove** button ![backward arrow](media/backward-button.png) to move the selected records to the **Available** list.</span></span>
1. <span data-ttu-id="0190d-325">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="0190d-325">Select **OK**.</span></span>
1. <span data-ttu-id="0190d-326">Í línunni fyrir víddarstigið **Númeraplata** skal velja gátreitinn **Leyfa frátekt á eftirspurnarpöntun**.</span><span class="sxs-lookup"><span data-stu-id="0190d-326">In the row for the **License plate** dimension level, select the **Allow reservation on demand order** check box.</span></span> <span data-ttu-id="0190d-327">Stigið **Staðsetning** er valið sjálfkrafa og ekki er hægt að hreinsa gátreitinn fyrir það.</span><span class="sxs-lookup"><span data-stu-id="0190d-327">The **Location** level is automatically selected, and you can't clear the check box for it.</span></span>
1. <span data-ttu-id="0190d-328">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="0190d-328">Select **Save**.</span></span>

### <a name="create-two-released-products"></a><span data-ttu-id="0190d-329">Stofna tvær útgefnar afurðir</span><span class="sxs-lookup"><span data-stu-id="0190d-329">Create two released products</span></span>

1. <span data-ttu-id="0190d-330">Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="0190d-330">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="0190d-331">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="0190d-331">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="0190d-332">Í svarglugganum **Ný útgefin afurð** skal stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="0190d-332">In the **New released product** dialog box, set the following values:</span></span>

    - <span data-ttu-id="0190d-333">**Afurðarnúmer:** *Item1*</span><span class="sxs-lookup"><span data-stu-id="0190d-333">**Product number:** *Item1*</span></span>
    - <span data-ttu-id="0190d-334">**Vörunúmer:** *Item1*</span><span class="sxs-lookup"><span data-stu-id="0190d-334">**Item number:** *Item1*</span></span>
    - <span data-ttu-id="0190d-335">**Vörulíkanaflokkur:** *FIFO*</span><span class="sxs-lookup"><span data-stu-id="0190d-335">**Item model group:** *FIFO*</span></span>
    - <span data-ttu-id="0190d-336">**Vöruflokkur:** *Hljóð*</span><span class="sxs-lookup"><span data-stu-id="0190d-336">**Item group:** *Audio*</span></span>
    - <span data-ttu-id="0190d-337">**Geymsluvíddarflokkur:** *Afurð*</span><span class="sxs-lookup"><span data-stu-id="0190d-337">**Storage dimension group:** *Ware*</span></span>
    - <span data-ttu-id="0190d-338">**Rakningarvíddarflokkur:** *Enginn*</span><span class="sxs-lookup"><span data-stu-id="0190d-338">**Tracking dimension group:** *None*</span></span>
    - <span data-ttu-id="0190d-339">**Frátekningarstigveldi:** *FlexibleLP*</span><span class="sxs-lookup"><span data-stu-id="0190d-339">**Reservation hierarchy:** *FlexibleLP*</span></span>

1. <span data-ttu-id="0190d-340">Veljið **Í lagi** til að stofna afurðina og loka svarglugganum.</span><span class="sxs-lookup"><span data-stu-id="0190d-340">Select **OK** to create the product and close the dialog box.</span></span>
1. <span data-ttu-id="0190d-341">Nýja afurðin opnast.</span><span class="sxs-lookup"><span data-stu-id="0190d-341">The new product is opened.</span></span> <span data-ttu-id="0190d-342">Í flýtiflipanum **Vöruhús** skal stilla reitinn **Auðkenni röðunarflokks einingar** á *ea*.</span><span class="sxs-lookup"><span data-stu-id="0190d-342">On the **Warehouse** FastTab, set the **Unit sequence group ID** field to *ea*.</span></span>
1. <span data-ttu-id="0190d-343">Endurtakið fyrri skref til að stofna aðra afurð sem er með sömu stillingar, en stillið reitina **Afurðarnúmer** og **Vörunúmer** á *Item2*.</span><span class="sxs-lookup"><span data-stu-id="0190d-343">Repeat the previous steps to create a second product that has the same settings, but set the **Product number** and **Item number** fields to *Item2*.</span></span>
1. <span data-ttu-id="0190d-344">Á aðgerðasvæðinu, í flipanum **Stjórna birgðum**, í flokknum **Skoða**, skal velja **Lagerbirgðir**.</span><span class="sxs-lookup"><span data-stu-id="0190d-344">On the Action Pane, on the **Manage inventory** tab, in the **View** group, select **On-hand inventory**.</span></span> <span data-ttu-id="0190d-345">Veljið síðan **Leiðrétting á magni**.</span><span class="sxs-lookup"><span data-stu-id="0190d-345">Then select **Quantity adjustment**.</span></span>
1. <span data-ttu-id="0190d-346">Leiðréttið lagerbirgðir nýju varanna eins og tilgreint er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="0190d-346">Adjust the on-hand inventory of the new items as specified in the following table.</span></span>

    | <span data-ttu-id="0190d-347">vara</span><span class="sxs-lookup"><span data-stu-id="0190d-347">Item</span></span>  | <span data-ttu-id="0190d-348">Vöruhús</span><span class="sxs-lookup"><span data-stu-id="0190d-348">Warehouse</span></span> | <span data-ttu-id="0190d-349">Staður</span><span class="sxs-lookup"><span data-stu-id="0190d-349">Location</span></span> | <span data-ttu-id="0190d-350">Númeraplata</span><span class="sxs-lookup"><span data-stu-id="0190d-350">License plate</span></span> | <span data-ttu-id="0190d-351">Magn</span><span class="sxs-lookup"><span data-stu-id="0190d-351">Quantity</span></span> |
    |-------|-----------|----------|---------------|----------|
    | <span data-ttu-id="0190d-352">VARA1</span><span class="sxs-lookup"><span data-stu-id="0190d-352">Item1</span></span> | <span data-ttu-id="0190d-353">24</span><span class="sxs-lookup"><span data-stu-id="0190d-353">24</span></span>        | <span data-ttu-id="0190d-354">FL-010</span><span class="sxs-lookup"><span data-stu-id="0190d-354">FL-010</span></span>   | <span data-ttu-id="0190d-355">LP01</span><span class="sxs-lookup"><span data-stu-id="0190d-355">LP01</span></span>          | <span data-ttu-id="0190d-356">10</span><span class="sxs-lookup"><span data-stu-id="0190d-356">10</span></span>       |
    | <span data-ttu-id="0190d-357">VARA1</span><span class="sxs-lookup"><span data-stu-id="0190d-357">Item1</span></span> | <span data-ttu-id="0190d-358">24</span><span class="sxs-lookup"><span data-stu-id="0190d-358">24</span></span>        | <span data-ttu-id="0190d-359">FL-011</span><span class="sxs-lookup"><span data-stu-id="0190d-359">FL-011</span></span>   | <span data-ttu-id="0190d-360">LP02</span><span class="sxs-lookup"><span data-stu-id="0190d-360">LP02</span></span>          | <span data-ttu-id="0190d-361">10</span><span class="sxs-lookup"><span data-stu-id="0190d-361">10</span></span>       |
    | <span data-ttu-id="0190d-362">VARA2</span><span class="sxs-lookup"><span data-stu-id="0190d-362">Item2</span></span> | <span data-ttu-id="0190d-363">24</span><span class="sxs-lookup"><span data-stu-id="0190d-363">24</span></span>        | <span data-ttu-id="0190d-364">FL-010</span><span class="sxs-lookup"><span data-stu-id="0190d-364">FL-010</span></span>   | <span data-ttu-id="0190d-365">LP01</span><span class="sxs-lookup"><span data-stu-id="0190d-365">LP01</span></span>          | <span data-ttu-id="0190d-366">5</span><span class="sxs-lookup"><span data-stu-id="0190d-366">5</span></span>        |
    | <span data-ttu-id="0190d-367">VARA2</span><span class="sxs-lookup"><span data-stu-id="0190d-367">Item2</span></span> | <span data-ttu-id="0190d-368">24</span><span class="sxs-lookup"><span data-stu-id="0190d-368">24</span></span>        | <span data-ttu-id="0190d-369">FL-011</span><span class="sxs-lookup"><span data-stu-id="0190d-369">FL-011</span></span>   | <span data-ttu-id="0190d-370">LP02</span><span class="sxs-lookup"><span data-stu-id="0190d-370">LP02</span></span>          | <span data-ttu-id="0190d-371">5</span><span class="sxs-lookup"><span data-stu-id="0190d-371">5</span></span>        |

    > [!NOTE]
    > <span data-ttu-id="0190d-372">Stofna þarf tvær númeraplötur og nota staðsetningar sem leyfa blandaðar vörur, svo sem *FL-010* og *FL-011*.</span><span class="sxs-lookup"><span data-stu-id="0190d-372">You must create the two license plates and use locations that allow for mixed items, such as *FL-010* and *FL-011*.</span></span>

### <a name="create-a-sales-order-and-reserve-a-specific-license-plate"></a><span data-ttu-id="0190d-373">Stofna sölupöntun og taka frá tiltekna númeraplötu</span><span class="sxs-lookup"><span data-stu-id="0190d-373">Create a sales order and reserve a specific license plate</span></span>

1. <span data-ttu-id="0190d-374">Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="0190d-374">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="0190d-375">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="0190d-375">Select **New**.</span></span>
1. <span data-ttu-id="0190d-376">Sláið inn eftirfarandi gildi í svarglugganum **Stofna sölupöntun**:</span><span class="sxs-lookup"><span data-stu-id="0190d-376">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="0190d-377">**Viðskiptavinalykill:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="0190d-377">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="0190d-378">**Vöruhús:** *24*</span><span class="sxs-lookup"><span data-stu-id="0190d-378">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="0190d-379">Veljið **Í lagi** til að loka svarglugganum **Stofna sölupöntun** og opnið nýju sölupöntunina.</span><span class="sxs-lookup"><span data-stu-id="0190d-379">Select **OK** to close the **Create sales order** dialog box and open the new sales order.</span></span>
1. <span data-ttu-id="0190d-380">Í flýtiflipanum **Sölupöntunarlínur** skal bæta við línu sem er með eftirfarandi stillingum:</span><span class="sxs-lookup"><span data-stu-id="0190d-380">On the **Sales order lines** FastTab, add a line that has the following settings:</span></span>

    - <span data-ttu-id="0190d-381">**Vörunúmer:** *Item1*</span><span class="sxs-lookup"><span data-stu-id="0190d-381">**Item number:** *Item1*</span></span>
    - <span data-ttu-id="0190d-382">**Magn:** *10*</span><span class="sxs-lookup"><span data-stu-id="0190d-382">**Quantity:** *10*</span></span>

1. <span data-ttu-id="0190d-383">Bæta við annarri sölupöntunarlínu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="0190d-383">Add a second sales order line that has the following settings:</span></span>

    - <span data-ttu-id="0190d-384">**Vörunúmer:** *Item2*</span><span class="sxs-lookup"><span data-stu-id="0190d-384">**Item number:** *Item2*</span></span>
    - <span data-ttu-id="0190d-385">**Magn:** *5*</span><span class="sxs-lookup"><span data-stu-id="0190d-385">**Quantity:** *5*</span></span>

1. <span data-ttu-id="0190d-386">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="0190d-386">Select **Save**.</span></span>
1. <span data-ttu-id="0190d-387">Í flýtiflipanum **Upplýsingar um línu**, í flipanum **Uppsetning**, skal skrá hjá sér gildið **Lotukenni** fyrir hverja línu.</span><span class="sxs-lookup"><span data-stu-id="0190d-387">On the **Line details** FastTab, on the **Setup** tab, make a note of the **Lot ID** value for each line.</span></span> <span data-ttu-id="0190d-388">Þessi gildi eru nauðsynleg þegar tilteknar númeraplötur eru teknar frá.</span><span class="sxs-lookup"><span data-stu-id="0190d-388">These values will be required during reservation of specific license plates.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0190d-389">Til að taka frá tiltekna númeraplötu þarf að nota gagnaeininguna **Frátektir á ráðstöfuðum pöntunum eftir númeraplötu**.</span><span class="sxs-lookup"><span data-stu-id="0190d-389">To reserve a specific license plate, you must use the **Order-committed reservations per license plate** data entity.</span></span> <span data-ttu-id="0190d-390">Til að taka frá runurakta vöru á tiltekinni númeraplötu er einnig hægt að nota síðuna **Frátekt á runu**, eins og lýst er í hlutanum [Færa inn upplýsingar um sölupöntun](#sales-order-details).</span><span class="sxs-lookup"><span data-stu-id="0190d-390">To reserve a batch-tracked item on a specific license plate, you can also use the **Batch reservation** page, as described in the [Enter sales order details](#sales-order-details) section.</span></span>
    >
    > <span data-ttu-id="0190d-391">Ef númeraplata er færð beint inn í sölupöntunarlínuna og hún síðan staðfest í kerfinu, verður vinnsla vöruhúsakerfis ekki notuð fyrir línuna.</span><span class="sxs-lookup"><span data-stu-id="0190d-391">If you enter the license plate directly on the sales order line and confirm it to the system, warehouse management processing won't be used for the line.</span></span>

1. <span data-ttu-id="0190d-392">Veljið **Opna í Microsoft Office**, veljið **Frátektir á ráðstöfuðum pöntunum eftir númeraplötu** og hlaðið niður skránni.</span><span class="sxs-lookup"><span data-stu-id="0190d-392">Select **Open in Microsoft Office**, select **Order-committed reservations per license plate**, and download the file.</span></span>
1. <span data-ttu-id="0190d-393">Opnið niðurhalaða skrá í Excel og veljið **Virkja breytingar** svo að Excel-innbótin geti keyrt.</span><span class="sxs-lookup"><span data-stu-id="0190d-393">Open the downloaded file in Excel, and select **Enable editing** to enable the Excel add-in to run.</span></span>
1. <span data-ttu-id="0190d-394">Ef verið er að keyra í Excel-innbót í fyrsta sinn, er valið **Treysta þessari innbót**.</span><span class="sxs-lookup"><span data-stu-id="0190d-394">If you're running the Excel add-in for the first time, select **Trust this Add-in**.</span></span>
1. <span data-ttu-id="0190d-395">Ef beðið er um að skrá sig inn skal velja **Innskráningu**, og síðan skrá sig inn með því að nota sömu innskráningarupplýsingar og eru notuð til að skrá sig inn í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="0190d-395">If you're prompted to sign in, select **Sign in**, and then sign in by using the same credentials that you used to sign in to Supply Chain Management.</span></span>
1. <span data-ttu-id="0190d-396">Til að taka frá vöru á tiltekinni númeraplötu, í Excel-innbótinni, skal velja **Ný** til að bæta við frátektarlínu og stilla síðan eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="0190d-396">To reserve an item on a specific license plate, in the Excel add-in, select **New** to add a reservation line, and then set the following values:</span></span>

    - <span data-ttu-id="0190d-397">**Lotukenni:** Færið inn gildið fyrir **Lotukenni** sem fannst sölupöntunarlínuna fyrir *Item1*.</span><span class="sxs-lookup"><span data-stu-id="0190d-397">**Lot ID:** Enter the **Lot ID** value that you found for the sales order line for *Item1*.</span></span>
    - <span data-ttu-id="0190d-398">**Númeraplata:** *LP02*</span><span class="sxs-lookup"><span data-stu-id="0190d-398">**License plate:** *LP02*</span></span>
    - <span data-ttu-id="0190d-399">**ReservedInventoryQuantity:** *10*</span><span class="sxs-lookup"><span data-stu-id="0190d-399">**ReservedInventoryQuantity:** *10*</span></span>

1. <span data-ttu-id="0190d-400">Veljið **Ný** til að bæta við annarri frátektarlínu og stillið eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="0190d-400">Select **New** to add another reservation line, and set the following values:</span></span>

    - <span data-ttu-id="0190d-401">**Lotukenni:** Færið inn gildið fyrir **Lotukenni** sem fannst sölupöntunarlínuna fyrir *Item2*.</span><span class="sxs-lookup"><span data-stu-id="0190d-401">**Lot ID:** Enter the **Lot ID** value you found for the sales order line for *Item2*.</span></span>
    - <span data-ttu-id="0190d-402">**Númeraplata:** *LP02*</span><span class="sxs-lookup"><span data-stu-id="0190d-402">**License plate:** *LP02*</span></span>
    - <span data-ttu-id="0190d-403">**ReservedInventoryQuantity:** *5*</span><span class="sxs-lookup"><span data-stu-id="0190d-403">**ReservedInventoryQuantity:** *5*</span></span>

1. <span data-ttu-id="0190d-404">Í Excel-innbótinni skal velja **Birta** til að senda gögnin aftur í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="0190d-404">In the Excel add-in, select **Publish** to send the data back to Supply Chain Management.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0190d-405">Frátektarlínan birtist aðeins í kerfinu ef birtingu er lokið án villna.</span><span class="sxs-lookup"><span data-stu-id="0190d-405">The reservation line will appear in the system only if publishing is completed without errors.</span></span>

1. <span data-ttu-id="0190d-406">Farið aftur í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="0190d-406">Go back to Supply Chain Management.</span></span> 
1. <span data-ttu-id="0190d-407">Til að yfirfara frátekningu vörunnar, í flýtiflipanum **Sölupöntunarlínur**, í valmyndinni **Birgðir**, skal velja **Vinna með \> Frátekning**.</span><span class="sxs-lookup"><span data-stu-id="0190d-407">To review the item's reservation, on the **Sales order lines** FastTab, on the **Inventory** menu, select **Maintain \> Reservation**.</span></span> <span data-ttu-id="0190d-408">Athugið að fyrir sölupöntunarlínuna fyrir *Item1* eru birgðir upp á *10* teknar frá og fyrir sölupöntunarlínuna fyrir *Item2*, eru birgðir upp á *5* teknar frá.</span><span class="sxs-lookup"><span data-stu-id="0190d-408">Notice that, for the sales order line for *Item1*, inventory of *10* is reserved, and for the sales order line for *Item2*, inventory of *5* is reserved.</span></span>
1. <span data-ttu-id="0190d-409">Til að fara yfir birgðafærslur sem tengjast frátekningu sölupöntunarlínu, í flýtiflipanum **Sölupöntunarlínur**, í valmyndinni **Birgðir**, skal velja **Skoða \> Færslur**.</span><span class="sxs-lookup"><span data-stu-id="0190d-409">To review inventory transactions that are related to the sales order line reservation, on the **Sales order lines** FastTab, on the **Inventory** menu, select **View \> Transactions**.</span></span> <span data-ttu-id="0190d-410">Athugið að tvær færslur eru tengdar frátekningunni: ein þar sem reiturinn **Tilvísun** er stilltur á *Sölupöntun* og ein þar sem reiturinn **Tilvísun** er stilltur á *Frátekning á ráðstafaðri pöntun*.</span><span class="sxs-lookup"><span data-stu-id="0190d-410">Notice that there are two transactions that are related to the reservation: one where the **Reference** field is set to *Sales order* and one where the **Reference** field is set to *Order-committed reservation*.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0190d-411">Færsla þar sem reiturinn **Tilvísun** er stilltur á *Sölupöntun* sýnir frátekningu pöntunarlínu fyrir birgðavíddir sem eru fyrir ofan stigið **Staðsetning** (svæði, vöruhús og birgðastaða).</span><span class="sxs-lookup"><span data-stu-id="0190d-411">A transaction where the **Reference** field is set to *Sales order* represents the order line reservation for inventory dimensions that are above the **Location** level (site, warehouse, and inventory status).</span></span> <span data-ttu-id="0190d-412">Færsla þar sem reiturinn **Tilvísun** er stilltur á *Frátekning á ráðstafaðri pöntun* sýnir frátekningu pöntunarlínu fyrir tiltekna númeraplötu og staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="0190d-412">A transaction where the **Reference** field is set to *Order-committed reservation* represents the order line reservation for the specific license plate and location.</span></span>

1. <span data-ttu-id="0190d-413">Til að losa sölupöntunina, á aðgerðasvæðinu, í flipanum **Vöruhús**, í flokknum **Aðgerðir**, skal velja **Losa í vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="0190d-413">To release the sales order, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

### <a name="review-and-process-warehouse-work-with-order-committed-license-plates-assigned"></a><span data-ttu-id="0190d-414">Yfirfara og vinna úr vöruhúsavinnu með úthlutaðar númeraplötur ráðstafaðrar pöntunar</span><span class="sxs-lookup"><span data-stu-id="0190d-414">Review and process warehouse work with order-committed license plates assigned</span></span>

1. <span data-ttu-id="0190d-415">Í flýtiflipanum **Sölupöntunarlínur**, í valmyndinni **Vöruhús**, skal velja **Upplýsingar um vinnu**.</span><span class="sxs-lookup"><span data-stu-id="0190d-415">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Work details**.</span></span>

    <span data-ttu-id="0190d-416">Þar sem frátekning er gerð fyrir tiltekna runu, notar kerfið ekki staðsetningarleiðbeiningar þegar það stofnar vinnu fyrir sölupöntunina sem notar frátekningu númeraplötu.</span><span class="sxs-lookup"><span data-stu-id="0190d-416">As when reservation is done for a specific batch, the system doesn't use location directives when it creates the work for the sales order that uses license plate reservation.</span></span> <span data-ttu-id="0190d-417">Vegna þess að frátekning ráðstafaðrar pöntunar tilgreinir allar birgðavíddir, þ.á.m. staðsetningu, þarf ekki að nota staðsetningarleiðbeiningar vegna þess að birgðavíddir eru aðeins færðar inn í vinnuna.</span><span class="sxs-lookup"><span data-stu-id="0190d-417">Because the order-committed reservation specifies all the inventory dimensions, including the location, location directives don't have to be used, because those inventory dimensions are just entered in the work.</span></span> <span data-ttu-id="0190d-418">Þær eru sýndar í hlutanum **Úr birgðavíddum** á síðunni **Birgðafærslur vinnu**.</span><span class="sxs-lookup"><span data-stu-id="0190d-418">They are shown in the **From inventory dimensions** section on the **Work inventory transactions** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0190d-419">Þegar búið er að stofna vinnu, er birgðafærsla vörunnar þar sem reiturinn **Tilvísun** er stilltur á *Frátekning á ráðstafaðri pöntun* fjarlægð.</span><span class="sxs-lookup"><span data-stu-id="0190d-419">After the work is created, the item's inventory transaction where the **Reference** field is set to *Order-committed reservation* is removed.</span></span> <span data-ttu-id="0190d-420">Birgðafærslan þar sem reiturinn **Tilvísun** er stilltur á *Vinna* inniheldur nú efnislega frátekningu fyrir allar birgðavíddir magns.</span><span class="sxs-lookup"><span data-stu-id="0190d-420">The inventory transaction where the **Reference** field is set to *Work* now holds the physical reservation for all the quantity's inventory dimensions.</span></span>

1. <span data-ttu-id="0190d-421">Í fartækinu skal ljúka tiltekt og frágangi vinnunnar með því að nota valmyndaratriði þar sem gátreiturinn **Meðhöndla eftir númeraplötu** er valið.</span><span class="sxs-lookup"><span data-stu-id="0190d-421">On the mobile device, finish picking and putting the work by using a menu item where the **Handle by license plate** check box is selected.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0190d-422">Aðgerðin **Meðhöndla eftir númeraplötu** sér um að vinna úr allri númeraplötunni.</span><span class="sxs-lookup"><span data-stu-id="0190d-422">The **Handle by license plate** functionality helps you process the whole license plate.</span></span> <span data-ttu-id="0190d-423">Ef nauðsynlegt er að vinna úr hluta númeraplötunnar, er ekki hægt að nota þessa aðgerð.</span><span class="sxs-lookup"><span data-stu-id="0190d-423">If you must process part of the license plate, you can't use this functionality.</span></span>
    >
    > <span data-ttu-id="0190d-424">Mælt er með því að aðskilin vinna sé búin til fyrir hverja númeraplötu.</span><span class="sxs-lookup"><span data-stu-id="0190d-424">We recommend that you have separate work generated for each license plate.</span></span> <span data-ttu-id="0190d-425">Til að ná þessu fram skal nota eiginleikann **Vinnuhausaskil** á síðunni **Vinnusniðmát**.</span><span class="sxs-lookup"><span data-stu-id="0190d-425">To achieve this result, use the **Work header breaks** feature on the **Work template** page.</span></span>

    <span data-ttu-id="0190d-426">Númeraplata *LP02* er nú tínd fyrir sölupöntunarlínur og komið fyrir á staðsetningunni *Útskot*.</span><span class="sxs-lookup"><span data-stu-id="0190d-426">License plate *LP02* is now picked for sales order lines and put to the *Baydoor* location.</span></span> <span data-ttu-id="0190d-427">Á þessu stigi má hlaða og senda hana til viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="0190d-427">At this point, it's ready to be loaded and dispatched to the customer.</span></span>

## <a name="exception-handling-of-warehouse-work-that-has-order-committed-batch-numbers"></a><span data-ttu-id="0190d-428">Meðhöndlun undantekninga á vöruhúsavinnu sem er með rununúmer ráðstafaðra pantana</span><span class="sxs-lookup"><span data-stu-id="0190d-428">Exception handling of warehouse work that has order-committed batch numbers</span></span>

<span data-ttu-id="0190d-429">Vörugeymsla til að velja pöntunarbundin lotunúmer er háð sömu stöðluðu meðhöndlun undantekninga vörugeymslu og aðgerðum og venjuleg vinna.</span><span class="sxs-lookup"><span data-stu-id="0190d-429">Warehouse work for picking order-committed batch numbers is subject to the same standard warehouse exception handling and actions as regular work.</span></span> <span data-ttu-id="0190d-430">Almennt er hægt að hætta við opna verkið eða vinnu línuna, það er hægt að trufla það vegna þess að notendastaður er fullur, það er hægt að velja hann stutt og það er hægt að uppfæra hann vegna hreyfingar.</span><span class="sxs-lookup"><span data-stu-id="0190d-430">In general, the open work or work line can be canceled, it can be interrupted because a user location is full, it can be short-picked, and it can be updated because of a movement.</span></span> <span data-ttu-id="0190d-431">Sömuleiðis er hægt að draga úr valinni vinnu sem þegar hefur verið lokið eða hægt er að snúa verkinu við.</span><span class="sxs-lookup"><span data-stu-id="0190d-431">Likewise, the picked quantity of work that has already been completed can be reduced, or the work can be reversed.</span></span>

<span data-ttu-id="0190d-432">Eftirfarandi lykilregla er notuð við allar þessar undantekningarmeðferðaraðgerðir: aldrei er hægt að skipta um lotunúmer sem var frátekið fyrir viðskiptavininn fyrir annað lotunúmer, en hægt er að breyta geymsluvíddum hans (staðsetningu og kennitala) með annað hvort handvirkri uppfærslu af notanda eða sjálfvirka uppfærslu af kerfinu.</span><span class="sxs-lookup"><span data-stu-id="0190d-432">The following key rule is applied to all these exception handling actions: the batch number that was reserved for the customer can never be replaced with a different batch number, but its storage dimensions (location and license plate) can be changed through either a manual update by the user or an automatic update by the system.</span></span> <span data-ttu-id="0190d-433">Sjálfvirka uppfærslan er byggð á sömu handahófi úthlutun geymsluvíddar og gilti þegar ákveðin lota var sjálfkrafa frátekin en engar geymsluvíddir voru tilgreindar.</span><span class="sxs-lookup"><span data-stu-id="0190d-433">The automatic update is based on the same random assignment of storage dimensions that applied when a specific batch was automatically reserved but no storage dimensions were specified.</span></span>

### <a name="example-scenario"></a><span data-ttu-id="0190d-434">Dæmi</span><span class="sxs-lookup"><span data-stu-id="0190d-434">Example scenario</span></span>

<span data-ttu-id="0190d-435">Dæmi um þessa atburðarás er ástand þar sem verið er að velja áður lokið verk með því að nota virknina **Draga úr völdu magni**.</span><span class="sxs-lookup"><span data-stu-id="0190d-435">An example of this scenario is a situation where previously completed work is being unpicked by using the **Reduce picked quantity** function.</span></span> <span data-ttu-id="0190d-436">Þetta dæmi gerir ráð fyrir því að skrefunum sem lýst er í [Sýniaðstæður: Úthlutun rununúmers](#Example-batch-allocation) sé lokið.</span><span class="sxs-lookup"><span data-stu-id="0190d-436">This example assumes that you've already completed the steps that are described in [Example scenario: Batch number allocation](#Example-batch-allocation).</span></span> <span data-ttu-id="0190d-437">Það heldur áfram þar sem frá var horfið í því dæmi.</span><span class="sxs-lookup"><span data-stu-id="0190d-437">It continues from that example.</span></span>

1. <span data-ttu-id="0190d-438">Farðu í **Vöruhúsakerfi** \> **Hleðslur** \> **Virkar hleðslur**.</span><span class="sxs-lookup"><span data-stu-id="0190d-438">Go to **Warehouse management** \> **Loads** \> **Active loads**.</span></span>
2. <span data-ttu-id="0190d-439">Veldu álag sem var búið til í tengslum við sendingu sölupöntunar þinnar.</span><span class="sxs-lookup"><span data-stu-id="0190d-439">Select the load that was created in connection with the shipment of your sales order.</span></span>
3. <span data-ttu-id="0190d-440">Af flýtiflipanum **Hlaðið pöntunarlínum**, veldu **Draga úr völdum magni**.</span><span class="sxs-lookup"><span data-stu-id="0190d-440">From the **Load order lines** FastTab, select **Reduce picked quantity**.</span></span>
4. <span data-ttu-id="0190d-441">Á **Draga úr völdum magni** síðu, í **Færa á staðsetningu** reit, veldu **FL-001**.</span><span class="sxs-lookup"><span data-stu-id="0190d-441">On the **Reduce picked quantity** page, in the **Move to location** field, select **FL-001**.</span></span>
5. <span data-ttu-id="0190d-442">Í reitnum **Flytja á númeraplötu** velurðu **LP33**.</span><span class="sxs-lookup"><span data-stu-id="0190d-442">In the **Move to license plate** field, select **LP33**.</span></span>
6. <span data-ttu-id="0190d-443">Í hnitanetinu í reitnum **Magn birgða til að afturkalla tiltekt á** sláðu inn **10**.</span><span class="sxs-lookup"><span data-stu-id="0190d-443">In the grid, in the **Inventory quantity to unpick** field, enter **10**.</span></span>
7. <span data-ttu-id="0190d-444">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="0190d-444">Select **OK**.</span></span>

<span data-ttu-id="0190d-445">Hér eru niðurstöður úr aðgerð til að afturkalla tiltekt:</span><span class="sxs-lookup"><span data-stu-id="0190d-445">Here are the results of the unpicking action:</span></span>

- <span data-ttu-id="0190d-446">Staða fyrri lokaðs verks er stillt á **Hætt við**.</span><span class="sxs-lookup"><span data-stu-id="0190d-446">The status of the previously closed work is set to **Canceled**.</span></span>
- <span data-ttu-id="0190d-447">Nýtt verk af gerðinni **Birgðahreyfing** er búin til fyrir óvalið magn af **10** fyrir lotunúmer **B11**.</span><span class="sxs-lookup"><span data-stu-id="0190d-447">New work of the **Inventory movement** type is created for the unpicked quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="0190d-448">Þessi vinna táknar hreyfingu frá **Afgreiðsluhurð** staðsetningu til númeraplötu **LP33** á staðsetningu **FL-001**.</span><span class="sxs-lookup"><span data-stu-id="0190d-448">This work represents the movement from the **Baydoor** location to license plate **LP33** in location **FL-001**.</span></span> <span data-ttu-id="0190d-449">Staðan er stillt á **Lokað**.</span><span class="sxs-lookup"><span data-stu-id="0190d-449">The status is set to **Closed**.</span></span>
- <span data-ttu-id="0190d-450">Kerfið áskilur aftur lotunúmerið sem upphaflega var pantað og úthlutar auðkenni staðsetningar og korts.</span><span class="sxs-lookup"><span data-stu-id="0190d-450">The system re-reserves the batch number that was originally ordered, and assigns the location and license plate IDs.</span></span> <span data-ttu-id="0190d-451">(Þetta ferli jafngildir því að keyra virknina **Frátektarlína** fyrir pöntunarlínuna fyrir tiltekið lotunúmer).</span><span class="sxs-lookup"><span data-stu-id="0190d-451">(This process is equivalent to running the **Reserve line** function for the order line for a given batch number).</span></span> <span data-ttu-id="0190d-452">Fyrir vikið, hópur **B11** er sýnt sem framið á flýtiflipanum **Hópatölur skuldbundnar til upprunalínu** af **Runufrátekt** síðu og **Frátekt** reiturinn inniheldur magn af **10** fyrir lotunúmer **B11**.</span><span class="sxs-lookup"><span data-stu-id="0190d-452">As a result, batch **B11** is shown as committed on the **Batch numbers committed to source line** FastTab of the **Batch reservation** page, and the **Reservation** field contains a quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="0190d-453">Að auki, er **Staðsetning** reiturinn stilltur á **FL-001**, og **Númeraplata** reiturinn er stilltur á **LP11**.</span><span class="sxs-lookup"><span data-stu-id="0190d-453">Additionally, the **Location** field is set to **FL-001**, and the **License plate** field is set to **LP11**.</span></span> <span data-ttu-id="0190d-454">(Þú getur bætt þessum reitum við töfluna ef þeir eru ekki sýnilegir.)</span><span class="sxs-lookup"><span data-stu-id="0190d-454">(You can add these fields to the grid if they aren't visible.)</span></span>

<span data-ttu-id="0190d-455">Eftirfarandi töflur veita yfirlit sem sýnir hvernig kerfið meðhöndlar pöntunarbundna lotu fyrirvara fyrir sérstakar vörugeymsluaðgerðir.</span><span class="sxs-lookup"><span data-stu-id="0190d-455">The following tables provide an overview that shows how the system handles order-committed batch reservation for specific warehouse actions.</span></span> <span data-ttu-id="0190d-456">Til að túlka innihaldið í töflunum, gerðu ráð fyrir að hver vörugeymslaaðgerð sé keyrð í samhengi við núverandi vörugeymsluverk sem er upprunnin í pöntunarbundinni lotu fyrirvara, eða að framkvæmd hverrar vörugerðaraðgerðar hefur áhrif á vinnu af þeirri gerð.</span><span class="sxs-lookup"><span data-stu-id="0190d-456">To interpret the content in the tables, assume that each warehouse action is run in the context of existing warehouse work that originates from an order-committed batch reservation, or that execution of each warehouse action affects work of that type.</span></span>

> [!NOTE]
> <span data-ttu-id="0190d-457">Í þessum töflum gefur dálkurinn „Hópmagn er fáanlegt“ til kynna hvort magn af framleiðslulotu er til viðbótar við það magn sem er annað hvort þegar frátekið fyrir núverandi pöntunarbundna fyrirvara eða þegar er frátekið af vörugeymsluverkinu sem kemur frá fyrirvörum af þeirri gerð.</span><span class="sxs-lookup"><span data-stu-id="0190d-457">In these tables, the "Batch quantity is available" column indicates whether a batch quantity is available in addition to the quantity that is either already reserved for the current order-committed reservations or already reserved by the warehouse work that originates from reservations of that type.</span></span>

#### <a name="override-the-pick-location-on-the-open-work"></a><span data-ttu-id="0190d-458">Yfirskrifa tínslustaðsetningu í opinni vinnu</span><span class="sxs-lookup"><span data-stu-id="0190d-458">Override the pick location on the open work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="0190d-459">Færibreyta lykiluppsetningar</span><span class="sxs-lookup"><span data-stu-id="0190d-459">Key setup parameter</span></span></th>
<th><span data-ttu-id="0190d-460">Runumagn er fáanlegt</span><span class="sxs-lookup"><span data-stu-id="0190d-460">Batch quantity is available</span></span></th>
<th><span data-ttu-id="0190d-461">Lykilþrep notenda</span><span class="sxs-lookup"><span data-stu-id="0190d-461">Key user steps</span></span></th>
<th><span data-ttu-id="0190d-462">Vinna vöruhúss</span><span class="sxs-lookup"><span data-stu-id="0190d-462">Warehouse work</span></span></th>
<th><span data-ttu-id="0190d-463">Pantanaskuldbundin hópapöntun</span><span class="sxs-lookup"><span data-stu-id="0190d-463">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="0190d-464">Valkosturinn <strong>Leyfa val á staðsetningu staðsetningu</strong> er virkur á starfsmanninum.</span><span class="sxs-lookup"><span data-stu-id="0190d-464">The <strong>Allow pick location override</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="0190d-465">Já</span><span class="sxs-lookup"><span data-stu-id="0190d-465">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="0190d-466">Veljið valmyndaratriðið <strong>Yfirskrifa staðsetningu</strong> í vöruhúsaforritinu þegar tiltektarverk er hafið.</span><span class="sxs-lookup"><span data-stu-id="0190d-466">Select the <strong>Override location</strong> menu item on the warehouse app when you start picking work.</span></span></li>
<li><span data-ttu-id="0190d-467">Veldu <strong>Stinga upp</strong>.</span><span class="sxs-lookup"><span data-stu-id="0190d-467">Select <strong>Suggest</strong>.</span></span></li>
<li><span data-ttu-id="0190d-468">Staðfestu nýja staðsetninguna sem lagt er til með tilliti til framboðs í fjölda magns.</span><span class="sxs-lookup"><span data-stu-id="0190d-468">Confirm the new location that is suggested based on batch quantity availability.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="0190d-469">Eftirfarandi aðgerðir eiga sér stað í núverandi vinnu:</span><span class="sxs-lookup"><span data-stu-id="0190d-469">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="0190d-470">Staðsetningin á velja línunni er uppfærð á nýjan stað.</span><span class="sxs-lookup"><span data-stu-id="0190d-470">The location on the pick line is updated to the new location.</span></span> <span data-ttu-id="0190d-471">(Ef staðsetningin er stjórnað með leyfismerki er úthlutað af handahófi leyfismerki fyrir vörubirgðafærsluna og starfsmaðurinn getur valið úr hvaða skilti sem er með tiltækt magn.)</span><span class="sxs-lookup"><span data-stu-id="0190d-471">(If the location is license plate–controlled, a random license plate is assigned to the work inventory transaction, and the worker can pick from any license plate that has available quantity.)</span></span></li>
<li><span data-ttu-id="0190d-472">Ef magnið er að finna á fleiri en einni leyfisplötu á nýjum stað, er upprunalegu vallínunni skipt í margar línur sem passa við hvern kennitala.</span><span class="sxs-lookup"><span data-stu-id="0190d-472">If the quantity is found on more than one license plate in the new location, the original pick line is split into multiple lines to match each license plate.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="0190d-473">Ekki tiltækt</span><span class="sxs-lookup"><span data-stu-id="0190d-473">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0190d-474">Ekkert</span><span class="sxs-lookup"><span data-stu-id="0190d-474">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="0190d-475">Veljið valmyndaratriðið <strong>Yfirskrifa staðsetningu</strong> í vöruhúsaforritinu þegar tiltektarverk er hafið.</span><span class="sxs-lookup"><span data-stu-id="0190d-475">Select the <strong>Override location</strong> menu item on the warehouse app when you start picking work.</span></span></li>
<li><span data-ttu-id="0190d-476">Færa handvirkt inn staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="0190d-476">Manually enter a location.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="0190d-477">Aðgerðin <strong>Hnekkja staðsetningu</strong> er ekki möguleg.</span><span class="sxs-lookup"><span data-stu-id="0190d-477">The <strong>Override location</strong> action isn't possible.</span></span> <span data-ttu-id="0190d-478">Það mistekst og villu er hent.</span><span class="sxs-lookup"><span data-stu-id="0190d-478">It fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="0190d-479">Á ekki við</span><span class="sxs-lookup"><span data-stu-id="0190d-479">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="full-button--split-a-work-line-because-of-overflow-on-the-user-location"></a><span data-ttu-id="0190d-480">Fullur hnappur - Skiptu vinnulínu vegna flæða á staðsetningu notandans</span><span class="sxs-lookup"><span data-stu-id="0190d-480">Full button – Split a work line because of overflow on the user location</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="0190d-481">Færibreyta lykiluppsetningar</span><span class="sxs-lookup"><span data-stu-id="0190d-481">Key setup parameter</span></span></th>
<th><span data-ttu-id="0190d-482">Runumagn er fáanlegt</span><span class="sxs-lookup"><span data-stu-id="0190d-482">Batch quantity is available</span></span></th>
<th><span data-ttu-id="0190d-483">Lykilþrep notenda</span><span class="sxs-lookup"><span data-stu-id="0190d-483">Key user steps</span></span></th>
<th><span data-ttu-id="0190d-484">Vinna vöruhúss</span><span class="sxs-lookup"><span data-stu-id="0190d-484">Warehouse work</span></span></th>
<th><span data-ttu-id="0190d-485">Pantanaskuldbundin hópapöntun</span><span class="sxs-lookup"><span data-stu-id="0190d-485">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0190d-486">Valkosturinn <strong>Leyfa verkaskiptingu</strong> er virkur í valmyndaratriðinu fyrir farsíma.</span><span class="sxs-lookup"><span data-stu-id="0190d-486">The <strong>Allow splitting of work</strong> option is enabled on the mobile device menu item.</span></span></td>
<td><span data-ttu-id="0190d-487">Ekki tiltækt</span><span class="sxs-lookup"><span data-stu-id="0190d-487">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="0190d-488">Veljið valmyndaratriðið <strong>Fullt</strong> í vöruhúsaforritinu þegar tiltektarverk er hafið.</span><span class="sxs-lookup"><span data-stu-id="0190d-488">Select the <strong>Full</strong> menu item on the warehouse app when you process picking work.</span></span></li>
<li><span data-ttu-id="0190d-489">Í <strong>Veldu fjölda</strong> reitinn, sláðu inn hluta magns af nauðsynlegu valinu til að gefa til kynna fullan afköst.</span><span class="sxs-lookup"><span data-stu-id="0190d-489">In the <strong>Pick Qty</strong> field, enter a partial quantity of the required pick to indicate the full capacity.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="0190d-490">Í núverandi vinnu er magnið uppfært í það magn sem eftir verður sem þarf að velja.</span><span class="sxs-lookup"><span data-stu-id="0190d-490">On the current work, the quantity is updated to the remaining quantity that must be picked.</span></span></li>
<li><span data-ttu-id="0190d-491">Ný verk fyrir valið magn er búið til og lokað.</span><span class="sxs-lookup"><span data-stu-id="0190d-491">New work for the picked quantity is created and closed.</span></span></li>
</ul></td>
<td><span data-ttu-id="0190d-492">Á ekki við</span><span class="sxs-lookup"><span data-stu-id="0190d-492">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reduce-the-picked-quantity-of-completed-work-from-a-load"></a><span data-ttu-id="0190d-493">Draga úr valið magn af fullunninni vinnu (úr álagi)</span><span class="sxs-lookup"><span data-stu-id="0190d-493">Reduce the picked quantity of completed work (from a load)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="0190d-494">Færibreyta lykiluppsetningar</span><span class="sxs-lookup"><span data-stu-id="0190d-494">Key setup parameter</span></span></th>
<th><span data-ttu-id="0190d-495">Runumagn er fáanlegt</span><span class="sxs-lookup"><span data-stu-id="0190d-495">Batch quantity is available</span></span></th>
<th><span data-ttu-id="0190d-496">Lykilþrep notenda</span><span class="sxs-lookup"><span data-stu-id="0190d-496">Key user steps</span></span></th>
<th><span data-ttu-id="0190d-497">Vinna vöruhúss</span><span class="sxs-lookup"><span data-stu-id="0190d-497">Warehouse work</span></span></th>
<th><span data-ttu-id="0190d-498">Pantanaskuldbundin hópapöntun</span><span class="sxs-lookup"><span data-stu-id="0190d-498">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="0190d-499">Á ekki við</span><span class="sxs-lookup"><span data-stu-id="0190d-499">Not applicable</span></span></td>
<td><span data-ttu-id="0190d-500">Já</span><span class="sxs-lookup"><span data-stu-id="0190d-500">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="0190d-501">Opnaðu <strong>Draga úr völdum magni</strong> síðu frá hleðslulínunni.</span><span class="sxs-lookup"><span data-stu-id="0190d-501">Open the <strong>Reduce picked quantity</strong> page from the load line.</span></span></li>
<li><span data-ttu-id="0190d-502">Færa skal inn fullt magn til að afturkalla tiltekt á.</span><span class="sxs-lookup"><span data-stu-id="0190d-502">Enter the full quantity to unpick.</span></span></li>
<li><span data-ttu-id="0190d-503">Veldu „færa til“ staðsetningu / kennitala.</span><span class="sxs-lookup"><span data-stu-id="0190d-503">Select a "move to" location/license plate.</span></span></li>
</ol>
</td>
<td>
<ul> 
<li><span data-ttu-id="0190d-504">Vinna sem er tengd hleðslulínunni fellur niður.</span><span class="sxs-lookup"><span data-stu-id="0190d-504">Work that is associated with the load line is canceled.</span></span></li>
<li><span data-ttu-id="0190d-505">Ný verk fyrir birgðahreyfingar er búið til og lokað.</span><span class="sxs-lookup"><span data-stu-id="0190d-505">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="0190d-506">Magnið er aftur frátekið fyrir sömu lotu.</span><span class="sxs-lookup"><span data-stu-id="0190d-506">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="0190d-507">Kerfið úthlutar af handahófi staðsetningu og kennitala (ef staðsetningin er stjórnað með skiltum) þar sem magnið er fáanlegt.</span><span class="sxs-lookup"><span data-stu-id="0190d-507">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0190d-508">Nr</span><span class="sxs-lookup"><span data-stu-id="0190d-508">No</span></span></td>
<td><span data-ttu-id="0190d-509">Sjá fyrri línuna.</span><span class="sxs-lookup"><span data-stu-id="0190d-509">See the previous row.</span></span></td>
<td><span data-ttu-id="0190d-510">Sjá fyrri línuna.</span><span class="sxs-lookup"><span data-stu-id="0190d-510">See the previous row.</span></span></td>
<td><span data-ttu-id="0190d-511">Magnið er aftur frátekið fyrir sömu framleiðslulotu og fyrir sama stað og skírteini (ef staðsetningin er stjórnað með skiltum) sem var slegið inn við upptöku.</span><span class="sxs-lookup"><span data-stu-id="0190d-511">The quantity is re-reserved for the same batch, and for the same location and license plate (if the location is license plate–controlled) that were entered during unpicking.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="move-an-item-within-a-warehouse"></a><span data-ttu-id="0190d-512">Færa vöru til innan vöruhúss</span><span class="sxs-lookup"><span data-stu-id="0190d-512">Move an item within a warehouse</span></span>

> [!NOTE]
> <span data-ttu-id="0190d-513">Þessi vörugeymsla á aðeins við um flutninga á **Vinnusköpunarferli** tegund, ekki til hreyfingar eftir sniðmáti.</span><span class="sxs-lookup"><span data-stu-id="0190d-513">This warehouse action is applicable only to movement of the **Work creation process** type, not to movement by template.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="0190d-514">Færibreyta lykiluppsetningar</span><span class="sxs-lookup"><span data-stu-id="0190d-514">Key setup parameter</span></span></th>
<th><span data-ttu-id="0190d-515">Runumagn er fáanlegt</span><span class="sxs-lookup"><span data-stu-id="0190d-515">Batch quantity is available</span></span></th>
<th><span data-ttu-id="0190d-516">Lykilþrep notenda</span><span class="sxs-lookup"><span data-stu-id="0190d-516">Key user steps</span></span></th>
<th><span data-ttu-id="0190d-517">Vinna vöruhúss</span><span class="sxs-lookup"><span data-stu-id="0190d-517">Warehouse work</span></span></th>
<th><span data-ttu-id="0190d-518">Pantanaskuldbundin hópapöntun</span><span class="sxs-lookup"><span data-stu-id="0190d-518">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="0190d-519">Valkostur <strong>Leyfa flutning birgða með tilheyrandi vinnu</strong> er virkur á starfsmanninum.</span><span class="sxs-lookup"><span data-stu-id="0190d-519">The <strong>Allow movement of inventory with associated work</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="0190d-520">Já</span><span class="sxs-lookup"><span data-stu-id="0190d-520">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="0190d-521">Hefja færslu í vöruhúsaforritinu.</span><span class="sxs-lookup"><span data-stu-id="0190d-521">Start a movement on the warehouse app.</span></span></li>
<li><span data-ttu-id="0190d-522">Sláið inn staðsetningar „frá” og „til”.</span><span class="sxs-lookup"><span data-stu-id="0190d-522">Enter "from" and "to" locations.</span></span></li>
</ol></td>
<td>
<ul>
<li><span data-ttu-id="0190d-523">Í allri núverandi vinnu sem hefur áhrif á flutninginn, er staðsetningin valin uppfærð á nýja „til“ staðinn.</span><span class="sxs-lookup"><span data-stu-id="0190d-523">On all existing work that is affected by the move, the pick location is updated to the new "to" location.</span></span></li>
<li><span data-ttu-id="0190d-524">Ný verk fyrir birgðahreyfingar er búið til og lokað.</span><span class="sxs-lookup"><span data-stu-id="0190d-524">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="0190d-525">Allir núverandi fyrirvarar sem hafa áhrif á magnhreyfingu frá tilteknum stað eru aftur áskilnir fyrir sömu lotu.</span><span class="sxs-lookup"><span data-stu-id="0190d-525">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch.</span></span> <span data-ttu-id="0190d-526">Kerfið úthlutar af handahófi staðsetningu og kennitala (ef staðsetningin er stjórnað með skiltum) þar sem magnið er fáanlegt.</span><span class="sxs-lookup"><span data-stu-id="0190d-526">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0190d-527">Nr</span><span class="sxs-lookup"><span data-stu-id="0190d-527">No</span></span></td>
<td><span data-ttu-id="0190d-528">Sjá fyrri línuna.</span><span class="sxs-lookup"><span data-stu-id="0190d-528">See the previous row.</span></span></td>
<td><span data-ttu-id="0190d-529">Sjá fyrri línuna.</span><span class="sxs-lookup"><span data-stu-id="0190d-529">See the previous row.</span></span></td>
<td><span data-ttu-id="0190d-530">Allur fyrirliggjandi fyrirvari sem hefur áhrif á magnhreyfingu frá tilteknum stað er aftur áskilinn fyrir sömu framleiðslulotu og fyrir nýja „til“ staðsetningar og kennitala (ef staðsetningin er stjórnað með skiltum).</span><span class="sxs-lookup"><span data-stu-id="0190d-530">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch, and for the new "to" location and license plate (if the location is license plate–controlled).</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reverse-the-picked-quantity-of-completed-work-from-a-load-or-a-wave"></a><span data-ttu-id="0190d-531">Bakfærðu tiltekið magn af fullunninni vinnu (úr álagi eða bylgju)</span><span class="sxs-lookup"><span data-stu-id="0190d-531">Reverse the picked quantity of completed work (from a load or a wave)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="0190d-532">Færibreyta lykiluppsetningar</span><span class="sxs-lookup"><span data-stu-id="0190d-532">Key setup parameter</span></span></th>
<th><span data-ttu-id="0190d-533">Runumagn er fáanlegt</span><span class="sxs-lookup"><span data-stu-id="0190d-533">Batch quantity is available</span></span></th>
<th><span data-ttu-id="0190d-534">Lykilþrep notenda</span><span class="sxs-lookup"><span data-stu-id="0190d-534">Key user steps</span></span></th>
<th><span data-ttu-id="0190d-535">Vinna vöruhúss</span><span class="sxs-lookup"><span data-stu-id="0190d-535">Warehouse work</span></span></th>
<th><span data-ttu-id="0190d-536">Pantanaskuldbundin hópapöntun</span><span class="sxs-lookup"><span data-stu-id="0190d-536">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='6'><span data-ttu-id="0190d-537">Á ekki við</span><span class="sxs-lookup"><span data-stu-id="0190d-537">Not applicable</span></span></td>
<td><span data-ttu-id="0190d-538">Já</span><span class="sxs-lookup"><span data-stu-id="0190d-538">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="0190d-539">Opnaðu <strong>Bakfæra vinnu</strong> síðu.</span><span class="sxs-lookup"><span data-stu-id="0190d-539">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="0190d-540">Veldu beiðnissíðuna <strong>Skildu hluti eftir núverandi staðsetningu</strong> kostur.</span><span class="sxs-lookup"><span data-stu-id="0190d-540">On the request page, select the <strong>Leave items at current location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="0190d-541">Öll vinna sem er tengd hleðslunni fellur niður.</span><span class="sxs-lookup"><span data-stu-id="0190d-541">All work that is associated with the load is canceled.</span></span></td>
<td><span data-ttu-id="0190d-542">Magnið er aftur frátekið fyrir sömu lotu.</span><span class="sxs-lookup"><span data-stu-id="0190d-542">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="0190d-543">Kerfið úthlutar af handahófi staðsetningu og kennitala (ef staðsetningin er stjórnað með skiltum) þar sem magnið er fáanlegt.</span><span class="sxs-lookup"><span data-stu-id="0190d-543">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0190d-544">Nr</span><span class="sxs-lookup"><span data-stu-id="0190d-544">No</span></span></td>
<td><span data-ttu-id="0190d-545">Sjá fyrri línuna.</span><span class="sxs-lookup"><span data-stu-id="0190d-545">See the previous row.</span></span></td>
<td><span data-ttu-id="0190d-546">Sjá fyrri línuna.</span><span class="sxs-lookup"><span data-stu-id="0190d-546">See the previous row.</span></span></td>
<td><span data-ttu-id="0190d-547">Magnið er frátekið fyrir sömu framleiðslulotu og fyrir staðsetningu og kennitala þar sem magnið var eftir við afturköllun.</span><span class="sxs-lookup"><span data-stu-id="0190d-547">The quantity is re-reserved for the same batch, and for the location and license plate where the quantity was left upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0190d-548">Já</span><span class="sxs-lookup"><span data-stu-id="0190d-548">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="0190d-549">Opnaðu <strong>Bakfæra vinnu</strong> síðu.</span><span class="sxs-lookup"><span data-stu-id="0190d-549">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="0190d-550">Veldu beiðnissíðuna <strong>Úthluta vörum á þessa staðsetningu</strong> kostur.</span><span class="sxs-lookup"><span data-stu-id="0190d-550">On the request page, select the <strong>Assign items to this location</strong> option.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="0190d-551">Núgildandi vinna er afturkölluð.</span><span class="sxs-lookup"><span data-stu-id="0190d-551">The current work is canceled.</span></span></li>
<li><span data-ttu-id="0190d-552">Ný verk fyrir birgðahreyfingar er búið til og lokað.</span><span class="sxs-lookup"><span data-stu-id="0190d-552">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="0190d-553">Magnið er aftur frátekið fyrir sömu lotu.</span><span class="sxs-lookup"><span data-stu-id="0190d-553">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="0190d-554">Kerfið úthlutar af handahófi staðsetningu og kennitala (ef staðsetningin er stjórnað með skiltum) þar sem magnið er fáanlegt.</span><span class="sxs-lookup"><span data-stu-id="0190d-554">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0190d-555">Nr</span><span class="sxs-lookup"><span data-stu-id="0190d-555">No</span></span></td>
<td><span data-ttu-id="0190d-556">Sjá fyrri línuna.</span><span class="sxs-lookup"><span data-stu-id="0190d-556">See the previous row.</span></span></td>
<td><span data-ttu-id="0190d-557">Sjá fyrri línuna.</span><span class="sxs-lookup"><span data-stu-id="0190d-557">See the previous row.</span></span></td>
<td><span data-ttu-id="0190d-558">Magnið er frátekið fyrir sömu framleiðslulotu og fyrir staðsetningu og kennitala þar sem magnið var úthlutað á við bakfærslu.</span><span class="sxs-lookup"><span data-stu-id="0190d-558">The quantity is re-reserved for the same batch, and for the location and license plate that the quantity was assigned to upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0190d-559">Já/nei</span><span class="sxs-lookup"><span data-stu-id="0190d-559">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="0190d-560">Opnaðu <strong>Bakfæra vinnu</strong> síðu.</span><span class="sxs-lookup"><span data-stu-id="0190d-560">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="0190d-561">Veldu beiðnissíðuna <strong>Færa vörur á þessa staðsetningu</strong> kostur.</span><span class="sxs-lookup"><span data-stu-id="0190d-561">On the request page, select the <strong>Move items to this location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="0190d-562">Bakfærsla er ekki studd.</span><span class="sxs-lookup"><span data-stu-id="0190d-562">Reversal isn't supported.</span></span></td>
<td><span data-ttu-id="0190d-563">Á ekki við</span><span class="sxs-lookup"><span data-stu-id="0190d-563">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0190d-564">Já/nei</span><span class="sxs-lookup"><span data-stu-id="0190d-564">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="0190d-565">Opnaðu <strong>Bakfæra vinnu</strong> síðu.</span><span class="sxs-lookup"><span data-stu-id="0190d-565">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="0190d-566">Veldu beiðnissíðuna <strong>Færa vörur byggt á staðsetningartilskipunum</strong> kostur.</span><span class="sxs-lookup"><span data-stu-id="0190d-566">On the request page, select the <strong>Move items based on location directives</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="0190d-567">Bakfærsla er ekki studd.</span><span class="sxs-lookup"><span data-stu-id="0190d-567">Reversal isn't supported.</span></span> </td>
<td><span data-ttu-id="0190d-568">Á ekki við</span><span class="sxs-lookup"><span data-stu-id="0190d-568">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="short-pick-a-quantity--register-the-quantity-as-physically-not-found-at-the-locationlicense-plate-while-you-perform-picking-work"></a><span data-ttu-id="0190d-569">Veldu stutt skammt - Skráðu magnið sem ekki finnast líkamlega á staðnum / leyfismerkinu meðan þú framkvæmir tínaverk</span><span class="sxs-lookup"><span data-stu-id="0190d-569">Short-pick a quantity – Register the quantity as physically not found at the location/license plate while you perform picking work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="0190d-570">Færibreyta lykiluppsetningar</span><span class="sxs-lookup"><span data-stu-id="0190d-570">Key setup parameter</span></span></th>
<th><span data-ttu-id="0190d-571">Runumagn er fáanlegt</span><span class="sxs-lookup"><span data-stu-id="0190d-571">Batch quantity is available</span></span></th>
<th><span data-ttu-id="0190d-572">Lykilþrep notenda</span><span class="sxs-lookup"><span data-stu-id="0190d-572">Key user steps</span></span></th>
<th><span data-ttu-id="0190d-573">Vinna vöruhúss</span><span class="sxs-lookup"><span data-stu-id="0190d-573">Warehouse work</span></span></th>
<th><span data-ttu-id="0190d-574">Pantanaskuldbundin hópapöntun</span><span class="sxs-lookup"><span data-stu-id="0190d-574">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="0190d-575">Vinna undantekning frá <strong>Stutt val</strong> gerð er sett upp, hvar <strong>Endurúthlutun hlutar</strong> = <strong>Enginn</strong>, <strong>Stilla lager</strong> = <strong>Já</strong> og <strong>Fjarlægðu fyrirvara</strong> = <strong>Nei</strong>.</span><span class="sxs-lookup"><span data-stu-id="0190d-575">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span></td>
<td><span data-ttu-id="0190d-576">Já</span><span class="sxs-lookup"><span data-stu-id="0190d-576">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="0190d-577">Veljið <strong>Of lítil tiltekt</strong> -valmyndaratriðið í vöruhúsaforritinu þegar tiltektarverk er hafið.</span><span class="sxs-lookup"><span data-stu-id="0190d-577">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="0190d-578">Í <strong>Tiltekið magn</strong> reitinn er fært inn <strong>0</strong> (núll).</span><span class="sxs-lookup"><span data-stu-id="0190d-578">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="0190d-579">Í reitinn <strong>Ástæða</strong> slærðu inn <strong>Engin endurúthlutun</strong>.</span><span class="sxs-lookup"><span data-stu-id="0190d-579">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="0190d-580">Núverandi verk er lokað og valið magn er 0 (núll).</span><span class="sxs-lookup"><span data-stu-id="0190d-580">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="0190d-581">Birgðafærsla <strong>Telja</strong> tegund og <strong>Selt</strong> útgáfutegund er búin til til að tákna aðlögunina.</span><span class="sxs-lookup"><span data-stu-id="0190d-581">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="0190d-582">Magnið er aftur frátekið fyrir sömu lotu.</span><span class="sxs-lookup"><span data-stu-id="0190d-582">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="0190d-583">Kerfið úthlutar af handahófi staðsetningu og kennitala (ef staðsetningin er stjórnað með skiltum) þar sem magnið er fáanlegt.</span><span class="sxs-lookup"><span data-stu-id="0190d-583">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0190d-584">Nr</span><span class="sxs-lookup"><span data-stu-id="0190d-584">No</span></span></td>
<td><span data-ttu-id="0190d-585">Sjá fyrri línuna.</span><span class="sxs-lookup"><span data-stu-id="0190d-585">See the previous row.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="0190d-586">Of lítil tiltekt-aðgerðin mistekst og villu er hent.</span><span class="sxs-lookup"><span data-stu-id="0190d-586">The short-picking action fails, and an error is thrown.</span></span></li>
<li><span data-ttu-id="0190d-587">Núverandi verk er áfram opið.</span><span class="sxs-lookup"><span data-stu-id="0190d-587">The current work remains open.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="0190d-588">Á ekki við</span><span class="sxs-lookup"><span data-stu-id="0190d-588">Not applicable</span></span></td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="0190d-589">Vinna undantekning frá <strong>Stutt val</strong> gerð er sett upp, hvar <strong>Endurúthlutun hlutar</strong> = <strong>Enginn</strong>, <strong>Stilla lager</strong> = <strong>Já</strong> og <strong>Fjarlægðu fyrirvara</strong> = <strong>Já</strong>.</span><span class="sxs-lookup"><span data-stu-id="0190d-589">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span></td>
<td><span data-ttu-id="0190d-590">Já</span><span class="sxs-lookup"><span data-stu-id="0190d-590">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="0190d-591">Veljið <strong>Of lítil tiltekt</strong> -valmyndaratriðið í vöruhúsaforritinu þegar tiltektarverk er hafið.</span><span class="sxs-lookup"><span data-stu-id="0190d-591">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="0190d-592">Í <strong>Tiltekið magn</strong> reitinn er fært inn <strong>0</strong> (núll).</span><span class="sxs-lookup"><span data-stu-id="0190d-592">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="0190d-593">Í reitinn <strong>Ástæða</strong> slærðu inn <strong>Engin endurúthlutun</strong>.</span><span class="sxs-lookup"><span data-stu-id="0190d-593">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="0190d-594">Núverandi verk er lokað og valið magn er 0 (núll).</span><span class="sxs-lookup"><span data-stu-id="0190d-594">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="0190d-595">Birgðafærsla <strong>Telja</strong> tegund og <strong>Selt</strong> útgáfutegund er búin til til að tákna aðlögunina.</span><span class="sxs-lookup"><span data-stu-id="0190d-595">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="0190d-596">Allar núverandi frátektir sem hafa áhrif á magnleiðréttingu á staðsetningu þar sem tiltekt er of lítil eru endurfráteknar fyrir sömu lotu.</span><span class="sxs-lookup"><span data-stu-id="0190d-596">All existing reservations that are affected by the quantity adjustment in the short-picked location are re-reserved for the same batch.</span></span> <span data-ttu-id="0190d-597">Kerfið úthlutar af handahófi staðsetningu og kennitala (ef staðsetningin er stjórnað með skiltum) þar sem magnið er fáanlegt.</span><span class="sxs-lookup"><span data-stu-id="0190d-597">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0190d-598">Nr</span><span class="sxs-lookup"><span data-stu-id="0190d-598">No</span></span></td>
<td><span data-ttu-id="0190d-599">Sjá fyrri línuna.</span><span class="sxs-lookup"><span data-stu-id="0190d-599">See the previous row.</span></span></td>
<td><span data-ttu-id="0190d-600">Sjá fyrri línuna.</span><span class="sxs-lookup"><span data-stu-id="0190d-600">See the previous row.</span></span></td>
<td><span data-ttu-id="0190d-601">Allar núverandi frátektir sem hafa áhrif á magnleiðréttingu á staðsetningu þar sem tiltekt er of lítil eru fjarlægðar.</span><span class="sxs-lookup"><span data-stu-id="0190d-601">All existing reservations that are affected by the quantity adjustment in the short-picked location are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0190d-602">Vinna undantekning frá <strong>Stutt val</strong> gerð er sett upp, hvar <strong>Endurúthlutun hlutar</strong> = <strong>Handvirkt</strong>, <strong>Stilla lager</strong> = <strong>Já</strong> og <strong>Fjarlægðu fyrirvara</strong> = <strong>Nei/Já</strong>.</span><span class="sxs-lookup"><span data-stu-id="0190d-602">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No/Yes</strong>.</span></span> <span data-ttu-id="0190d-603">Að auki, er <strong>Leyfa endurúthlutun handvirkra atriða</strong> valkostur virkur á starfsmanninum.</span><span class="sxs-lookup"><span data-stu-id="0190d-603">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="0190d-604">Já</span><span class="sxs-lookup"><span data-stu-id="0190d-604">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="0190d-605">Veljið <strong>Of lítil tiltekt</strong> -valmyndaratriðið í vöruhúsaforritinu þegar tiltektarverk er hafið.</span><span class="sxs-lookup"><span data-stu-id="0190d-605">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="0190d-606">Í <strong>Magn með of litla tiltekt</strong> reitinn er fært inn <strong>0</strong> (núll).</span><span class="sxs-lookup"><span data-stu-id="0190d-606">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="0190d-607">Í <strong>Ástæða</strong> reit, veldu <strong>Stuttur velja með handvirkri úthlutun</strong>.</span><span class="sxs-lookup"><span data-stu-id="0190d-607">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="0190d-608">Veldu staðsetningu / kennitala á listanum.</span><span class="sxs-lookup"><span data-stu-id="0190d-608">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="0190d-609">Eftirfarandi aðgerðir eiga sér stað í núverandi vinnu:</span><span class="sxs-lookup"><span data-stu-id="0190d-609">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="0190d-610">Tínslulínan er lokuð og valið magn er 0 (núll).</span><span class="sxs-lookup"><span data-stu-id="0190d-610">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="0190d-611">Hætt er við að söluréttarlínuna.</span><span class="sxs-lookup"><span data-stu-id="0190d-611">The put line is canceled.</span></span></li>
<li><span data-ttu-id="0190d-612">Ný tiltektarlína er búin til.</span><span class="sxs-lookup"><span data-stu-id="0190d-612">A new pick line is created.</span></span> <span data-ttu-id="0190d-613">Það notar staðsetningu / númeraplötu sem notandinn valdi.</span><span class="sxs-lookup"><span data-stu-id="0190d-613">It uses the location/license plate that the user selected.</span></span></li>
<li><span data-ttu-id="0190d-614">Ný söluréttarlína er búin til.</span><span class="sxs-lookup"><span data-stu-id="0190d-614">A new put line is created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="0190d-615">Birgðafærsla <strong>Telja</strong> tegund og <strong>Selt</strong> útgáfutegund er búin til til að tákna aðlögunina.</span><span class="sxs-lookup"><span data-stu-id="0190d-615">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="0190d-616">Á ekki við</span><span class="sxs-lookup"><span data-stu-id="0190d-616">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0190d-617">Vinnuundantekning frá <strong>Stutt val</strong> gerð er sett upp, hvar <strong>Endurúthlutun hlutar</strong> = <strong>Handvirkt</strong>, <strong>Stilla lager</strong> = <strong>Já</strong> og <strong>Fjarlægðu fyrirvara</strong> = <strong>Nei</strong>.</span><span class="sxs-lookup"><span data-stu-id="0190d-617">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span> <span data-ttu-id="0190d-618">Að auki, er <strong>Leyfa endurúthlutun handvirkra atriða</strong> valkostur virkur á starfsmanninum.</span><span class="sxs-lookup"><span data-stu-id="0190d-618">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="0190d-619">Ekkert</span><span class="sxs-lookup"><span data-stu-id="0190d-619">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="0190d-620">Veljið <strong>Of lítil tiltekt</strong> -valmyndaratriðið í vöruhúsaforritinu þegar tiltektarverk er hafið.</span><span class="sxs-lookup"><span data-stu-id="0190d-620">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="0190d-621">Í <strong>Magn með of litla tiltekt</strong> reitinn er fært inn <strong>0</strong> (núll).</span><span class="sxs-lookup"><span data-stu-id="0190d-621">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="0190d-622">Í <strong>Ástæða</strong> reit, veldu <strong>Stuttur velja með handvirkri úthlutun</strong>.</span><span class="sxs-lookup"><span data-stu-id="0190d-622">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="0190d-623">Of lítil tiltekt-aðgerðin mistekst og villu er hent.</span><span class="sxs-lookup"><span data-stu-id="0190d-623">The short-picking action fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="0190d-624">Á ekki við</span><span class="sxs-lookup"><span data-stu-id="0190d-624">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0190d-625">Vinnuundantekning frá <strong>Stutt val</strong> gerð er sett upp, hvar <strong>Endurúthlutun hlutar</strong> = <strong>Handvirkt</strong>, <strong>Stilla lager</strong> = <strong>Já</strong> og <strong>Fjarlægðu fyrirvara</strong> = <strong>Já</strong>.</span><span class="sxs-lookup"><span data-stu-id="0190d-625">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span> <span data-ttu-id="0190d-626">Að auki, er <strong>Leyfa endurúthlutun handvirkra atriða</strong> valkostur virkur á starfsmanninum.</span><span class="sxs-lookup"><span data-stu-id="0190d-626">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="0190d-627">Ekkert</span><span class="sxs-lookup"><span data-stu-id="0190d-627">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="0190d-628">Veljið <strong>Of lítil tiltekt</strong> -valmyndaratriðið í vöruhúsaforritinu þegar tiltektarverk er hafið.</span><span class="sxs-lookup"><span data-stu-id="0190d-628">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="0190d-629">Í <strong>Magn með of litla tiltekt</strong> reitinn er fært inn <strong>0</strong> (núll).</span><span class="sxs-lookup"><span data-stu-id="0190d-629">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="0190d-630">Í <strong>Ástæða</strong> reit, veldu <strong>Stuttur velja með handvirkri úthlutun</strong>.</span><span class="sxs-lookup"><span data-stu-id="0190d-630">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="0190d-631">Veldu staðsetningu / kennitala á listanum.</span><span class="sxs-lookup"><span data-stu-id="0190d-631">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="0190d-632">Eftirfarandi aðgerðir eiga sér stað í núverandi vinnu:</span><span class="sxs-lookup"><span data-stu-id="0190d-632">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="0190d-633">Tínslulínan er lokuð og valið magn er 0 (núll).</span><span class="sxs-lookup"><span data-stu-id="0190d-633">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="0190d-634">Hætt er við að söluréttarlínuna.</span><span class="sxs-lookup"><span data-stu-id="0190d-634">The put line is canceled.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="0190d-635">Birgðafærsla <strong>Telja</strong> tegund og <strong>Selt</strong> útgáfutegund er búin til til að tákna aðlögunina.</span><span class="sxs-lookup"><span data-stu-id="0190d-635">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="0190d-636">Allar núverandi frátektir sem hafa áhrif á magnleiðréttingu á staðsetningu þar sem tiltekt er of lítil/númeraplötu eru fjarlægðar.</span><span class="sxs-lookup"><span data-stu-id="0190d-636">All existing reservations that are affected by the quantity adjustment in the short-picked location/license plate are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0190d-637">Vinnuundantekning frá <strong>Stutt val</strong> gerð er sett upp, hvar <strong>Endurúthlutun hlutar</strong> = <strong>Sjálfvirkt</strong>, <strong>Stilla lager</strong> = <strong>Já/Nei</strong> og <strong>Fjarlægðu fyrirvara</strong> = <strong>Já/Nei</strong>.</span><span class="sxs-lookup"><span data-stu-id="0190d-637">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Automatic</strong>, <strong>Adjust inventory</strong> = <strong>Yes/No</strong>, and <strong>Remove reservations</strong> = <strong>Yes/No</strong>.</span></span></td>
<td><span data-ttu-id="0190d-638">Ekki tiltækt</span><span class="sxs-lookup"><span data-stu-id="0190d-638">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="0190d-639">Veljið <strong>Of lítil tiltekt</strong> -valmyndaratriðið í vöruhúsaforritinu þegar tiltektarverk er hafið.</span><span class="sxs-lookup"><span data-stu-id="0190d-639">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="0190d-640">Í <strong>Magn með of litla tiltekt</strong> reitinn er fært inn <strong>0</strong> (núll).</span><span class="sxs-lookup"><span data-stu-id="0190d-640">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="0190d-641">Í <strong>Ástæða</strong> reit, veldu <strong>Stuttur velja með sjálfvirkri endurúthlutun</strong>.</span><span class="sxs-lookup"><span data-stu-id="0190d-641">In the <strong>Reason</strong> field, select <strong>Short Picking with automatic reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="0190d-642">Ekki er stutt í skammval sem felur í sér sjálfvirka endurúthlutun.</span><span class="sxs-lookup"><span data-stu-id="0190d-642">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
<td><span data-ttu-id="0190d-643">Ekki er stutt í skammval sem felur í sér sjálfvirka endurúthlutun.</span><span class="sxs-lookup"><span data-stu-id="0190d-643">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="change-the-inventory-status"></a><span data-ttu-id="0190d-644">Breyta á birgðastöðunni</span><span class="sxs-lookup"><span data-stu-id="0190d-644">Change the inventory status</span></span>

> [!NOTE]
> <span data-ttu-id="0190d-645">Þessa vörugeymsluaðgerð er hægt að framkvæma frá mörgum inngangspunktum.</span><span class="sxs-lookup"><span data-stu-id="0190d-645">This warehouse action can be performed from multiple entry points.</span></span> <span data-ttu-id="0190d-646">Dæmið sem sýnt er hér notar **Breyting á birgðum** aðgerð á **Á lager eftir birgðageymslu** síðu.</span><span class="sxs-lookup"><span data-stu-id="0190d-646">The example that is shown here uses **Inventory status change** action on the **On-hand by location** page.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="0190d-647">Færibreyta lykiluppsetningar</span><span class="sxs-lookup"><span data-stu-id="0190d-647">Key setup parameter</span></span></th>
<th><span data-ttu-id="0190d-648">Runumagn er fáanlegt</span><span class="sxs-lookup"><span data-stu-id="0190d-648">Batch quantity is available</span></span></th>
<th><span data-ttu-id="0190d-649">Lykilþrep notenda</span><span class="sxs-lookup"><span data-stu-id="0190d-649">Key user steps</span></span></th>
<th><span data-ttu-id="0190d-650">Vinna vöruhúss</span><span class="sxs-lookup"><span data-stu-id="0190d-650">Warehouse work</span></span></th>
<th><span data-ttu-id="0190d-651">Pantanaskuldbundin hópapöntun</span><span class="sxs-lookup"><span data-stu-id="0190d-651">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="0190d-652">Á <strong>Vöruhús</strong> flipanum, í <strong>Vöruhús</strong> skrá, er <strong>Fjarlægja frátektir og merkingar</strong> reiturinn stilltur á <strong>Frátektir</strong> eða <strong>Merkingar og fyrirvarar</strong>.</span><span class="sxs-lookup"><span data-stu-id="0190d-652">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>Reservations</strong> or <strong>Markings and reservations</strong>.</span></span></td>
<td><span data-ttu-id="0190d-653">Já</span><span class="sxs-lookup"><span data-stu-id="0190d-653">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="0190d-654">Veldu tiltekna staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="0190d-654">Select a specific location.</span></span></li>
<li><span data-ttu-id="0190d-655">Veldu línu sem er með tiltekinn hlut, staðsetningu og númeraplötu (ef staðsetningin er stjórnað með skiltum).</span><span class="sxs-lookup"><span data-stu-id="0190d-655">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="0190d-656">Veldu <strong>Breyting á birgðastöðu</strong>.</span><span class="sxs-lookup"><span data-stu-id="0190d-656">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="0190d-657">Stilltu reitinn <strong>Staða birgða</strong> til <strong>Lokun</strong>.</span><span class="sxs-lookup"><span data-stu-id="0190d-657">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="0190d-658">Breytingar á birgðastöðu eru ekki leyfðar fyrir magn sem er frátekið fyrir vinnu.</span><span class="sxs-lookup"><span data-stu-id="0190d-658">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="0190d-659">Magnið er aftur frátekið fyrir sömu lotu.</span><span class="sxs-lookup"><span data-stu-id="0190d-659">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="0190d-660">Kerfið úthlutar af handahófi staðsetningu og kennitala (ef staðsetningin er stjórnað með skiltum) þar sem magnið er fáanlegt.</span><span class="sxs-lookup"><span data-stu-id="0190d-660">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></li>
<li><span data-ttu-id="0190d-661">Tvö birgðafærslur <strong>Breyting á birgðum</strong> gerð eru búin til til að tákna breytinguna á stöðu birgða.</span><span class="sxs-lookup"><span data-stu-id="0190d-661">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="0190d-662">Birgðafærsla af gerðinni <strong>Stöðvun birgða</strong> og gerð útreyfingar <strong>Frátekið á lager</strong> er búin til til að tákna fyrirvara á lokað magn.</span><span class="sxs-lookup"><span data-stu-id="0190d-662">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="0190d-663">Nr</span><span class="sxs-lookup"><span data-stu-id="0190d-663">No</span></span></td>
<td><span data-ttu-id="0190d-664">Sjá fyrri línuna.</span><span class="sxs-lookup"><span data-stu-id="0190d-664">See the previous row.</span></span></td>
<td><span data-ttu-id="0190d-665">Breytingar á birgðastöðu eru ekki leyfðar fyrir magn sem er frátekið fyrir vinnu.</span><span class="sxs-lookup"><span data-stu-id="0190d-665">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="0190d-666">Pöntunin er fjarlægð.</span><span class="sxs-lookup"><span data-stu-id="0190d-666">The reservation is removed.</span></span></li>
<li><span data-ttu-id="0190d-667">Tvö birgðafærslur <strong>Breyting á birgðum</strong> gerð eru búin til til að tákna breytinguna á stöðu birgða.</span><span class="sxs-lookup"><span data-stu-id="0190d-667">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="0190d-668">Birgðafærsla af gerðinni <strong>Stöðvun birgða</strong> og gerð útreyfingar <strong>Frátekið á lager</strong> er búin til til að tákna fyrirvara á lokað magn.</span><span class="sxs-lookup"><span data-stu-id="0190d-668">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="0190d-669">Á flipanum <strong>Vöruhús</strong>, í skránni <strong>Vöruhús</strong>, er reiturinn <strong>Fjarlægja frátektir og merkingar</strong> stilltur á <strong>Ekkert</strong>.</span><span class="sxs-lookup"><span data-stu-id="0190d-669">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>None</strong>.</span></span></td>
<td><span data-ttu-id="0190d-670">Já</span><span class="sxs-lookup"><span data-stu-id="0190d-670">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="0190d-671">Veldu tiltekna staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="0190d-671">Select a specific location.</span></span></li>
<li><span data-ttu-id="0190d-672">Veldu línu sem er með tiltekinn hlut, staðsetningu og númeraplötu (ef staðsetningin er stjórnað með skiltum).</span><span class="sxs-lookup"><span data-stu-id="0190d-672">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="0190d-673">Veldu <strong>Breyting á birgðastöðu</strong>.</span><span class="sxs-lookup"><span data-stu-id="0190d-673">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="0190d-674">Stilltu reitinn <strong>Staða birgða</strong> til <strong>Lokun</strong>.</span><span class="sxs-lookup"><span data-stu-id="0190d-674">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="0190d-675">Breytingar á birgðastöðu eru ekki leyfðar fyrir magn sem er frátekið fyrir vinnu.</span><span class="sxs-lookup"><span data-stu-id="0190d-675">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="0190d-676">Magnið er aftur frátekið fyrir sömu lotu.</span><span class="sxs-lookup"><span data-stu-id="0190d-676">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="0190d-677">Kerfið úthlutar af handahófi staðsetningu og kennitala (ef staðsetningin er stjórnað með skiltum) þar sem magnið er fáanlegt.</span><span class="sxs-lookup"><span data-stu-id="0190d-677">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0190d-678">Nr</span><span class="sxs-lookup"><span data-stu-id="0190d-678">No</span></span></td>
<td><span data-ttu-id="0190d-679">Sjá fyrri línuna.</span><span class="sxs-lookup"><span data-stu-id="0190d-679">See the previous row.</span></span></td>
<td><span data-ttu-id="0190d-680">Breytingar á birgðastöðu eru ekki leyfðar fyrir magn sem er frátekið fyrir vinnu.</span><span class="sxs-lookup"><span data-stu-id="0190d-680">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="0190d-681">Breytingar á birgðastöðu eru ekki leyfðar.</span><span class="sxs-lookup"><span data-stu-id="0190d-681">Inventory status changes aren't allowed.</span></span></td>
</tr>
</tbody>
</table>

## <a name="limitations"></a><span data-ttu-id="0190d-682">Takmarkanir</span><span class="sxs-lookup"><span data-stu-id="0190d-682">Limitations</span></span>

- <span data-ttu-id="0190d-683">Sveigjanleiki vörugeymsluvíddar pöntunaraðgerða styður ekki eftirfarandi eiginleika:</span><span class="sxs-lookup"><span data-stu-id="0190d-683">The flexible warehouse-level dimension reservation functionality doesn't support the following features:</span></span>

    - <span data-ttu-id="0190d-684">Stjórnun framleiðsluþyngdar</span><span class="sxs-lookup"><span data-stu-id="0190d-684">Catch weight management</span></span>
    - <span data-ttu-id="0190d-685">Efnislega neikvæð birgðastaða</span><span class="sxs-lookup"><span data-stu-id="0190d-685">Physical negative inventory</span></span>
    - <span data-ttu-id="0190d-686">Frátekt gegn pöntuðu framboði</span><span class="sxs-lookup"><span data-stu-id="0190d-686">Reservation against ordered supply</span></span>
    - <span data-ttu-id="0190d-687">Flytja pantanir og hráefni tína</span><span class="sxs-lookup"><span data-stu-id="0190d-687">Transfer orders and raw material picking</span></span>

- <span data-ttu-id="0190d-688">Reglugerð um gámasamstæðu fyrir pökkun með tilskipunareiningunni hefur takmarkanir.</span><span class="sxs-lookup"><span data-stu-id="0190d-688">The container consolidation rule for packing by directive unit has limitations.</span></span> <span data-ttu-id="0190d-689">Fyrir pöntunarbundna fyrirvara mælum við með að þú notir ekki sniðmát fyrir gámagerð þar sem **Pakkning eftir tilskipunareining** reiturinn er virkur.</span><span class="sxs-lookup"><span data-stu-id="0190d-689">For order-committed reservations, we recommend that you not use container build templates where the **Pack by directive unit** field is enabled.</span></span> <span data-ttu-id="0190d-690">Í núverandi hönnun eru staðsetningartilskipanir ekki notaðar þegar vörugeymsla er búin til.</span><span class="sxs-lookup"><span data-stu-id="0190d-690">In the current design, location directives aren't used when warehouse work is created.</span></span> <span data-ttu-id="0190d-691">Þess vegna er aðeins lægsta einingin í einingaröðarhópnum (birgðaeiningin) beitt á gámabylgjuskrefinu.</span><span class="sxs-lookup"><span data-stu-id="0190d-691">Therefore, only the lowest unit in the unit sequence group (the inventory unit) is applied during the containerization wave step.</span></span>
