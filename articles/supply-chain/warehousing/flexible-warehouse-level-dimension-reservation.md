---
title: Sveigjanleg frátektarregla á vídd vöruhúsastigs
description: Þetta efni lýsir stefnuskrá fyrir birgða sem láta fyrirtæki sem selja vörur sem eru rekin með runur og reka flutninga sína sem aðgerðir með WMS-virka áskilja sértækar runur fyrir sölupantanir viðskiptavina, jafnvel þó að pöntunarveldið sem er tengt vörunum banni ekki fyrirvara á tilteknum runum.
author: omulvad
manager: tfehr
ms.date: 02/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2020-01-15
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: ec80346126713cc604b00e6ca7f6e8f4c242dc6f
ms.sourcegitcommit: a7a7303004620d2e9cef0642b16d89163911dbb4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/01/2020
ms.locfileid: "3530306"
---
# <a name="flexible-warehouse-level-dimension-reservation-policy"></a><span data-ttu-id="b5452-103">Sveigjanleg frátektarregla á vídd vöruhúsastigs</span><span class="sxs-lookup"><span data-stu-id="b5452-103">Flexible warehouse-level dimension reservation policy</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b5452-104">Þegar stigveldi birgða fyrirvara á „hópnum hér að neðan\[staðsetningu\]„ gerð er tengd vörum, fyrirtækjum sem selja vöru sem er rekin með hópum og rekur flutninga sína sem aðgerðir sem eru gerðar virkar fyrir Microsoft Dynamics 365 Warehouse Management System (WMS) getur ekki pantað sértæka runu af þessum vörum fyrir sölupantanir viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="b5452-104">When an inventory reservation hierarchy of the "Batch-below\[location\]" type is associated with products, businesses that sell batch-tracked products and run their logistics as operations that are enabled for the Microsoft Dynamics 365 Warehouse Management System (WMS) can't reserve specific batches of those products for customer sales orders.</span></span> <span data-ttu-id="b5452-105">Þetta efnisatriði lýsir stefnuskráningu birgða sem gerir þessum fyrirtækjum kleift að panta sértækar runur, jafnvel þegar vörurnar eru tengdar „hópi hér að neðan\[staðsetningu\]" stigveldi fyrirvara.</span><span class="sxs-lookup"><span data-stu-id="b5452-105">This topic describes the inventory reservation policy that lets these businesses reserve specific batches, even when the products are associated with a "Batch-below\[location\]" reservation hierarchy.</span></span>

## <a name="inventory-reservation-hierarchy"></a><span data-ttu-id="b5452-106">Frátekningarstigveldi birgða</span><span class="sxs-lookup"><span data-stu-id="b5452-106">Inventory reservation hierarchy</span></span>

<span data-ttu-id="b5452-107">Þessi hluti dregur saman núverandi stigveldi birgða fyrirvara.</span><span class="sxs-lookup"><span data-stu-id="b5452-107">This section summarizes the existing inventory reservation hierarchy.</span></span> <span data-ttu-id="b5452-108">Það beinir sjónum að því hvernig meðhöndlaðir eru hlutar í hópum og raðnúmerum.</span><span class="sxs-lookup"><span data-stu-id="b5452-108">It focuses on the way that batch-tracked and serial-tracked items are handled.</span></span>

<span data-ttu-id="b5452-109">Stigveldi birgðapöntunar ræður því að hvað varðar geymsluvíddir ber eftirspurnarpöntunin nauðsynlegar víddir á staðsetningu, vörugeymslu og birgðastöðu, en rökfræði vörugeymslu er ábyrg fyrir því að tengja staðsetningu við umbeðið magn og panta staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="b5452-109">The inventory reservation hierarchy dictates that, as far as storage dimensions are concerned, the demand order carries the mandatory dimensions of site, warehouse, and inventory status, whereas the warehouse logic is responsible for assigning a location to the requested quantities and reserving the location.</span></span> <span data-ttu-id="b5452-110">Með öðrum orðum, í samskiptum milli eftirspurnarpöntunar og vörugeymslu er gert ráð fyrir að eftirspurnarpöntunin gefi til kynna hvar pöntunin verður að vera send frá (það er, hvaða staður og vörugeymsla).</span><span class="sxs-lookup"><span data-stu-id="b5452-110">In other words, in the interactions between the demand order and the warehouse operations, the demand order is expected to indicate where the order must be shipped from (that is, what site and warehouse).</span></span> <span data-ttu-id="b5452-111">Vöruhúsið treystir síðan á rökfræði þess til að finna nauðsynlegt magn í húsnæði vörugeymslu.</span><span class="sxs-lookup"><span data-stu-id="b5452-111">The warehouse then relies on its logic to find the required quantity in the warehouse premises.</span></span>

<span data-ttu-id="b5452-112">Hins vegar, til að endurspegla rekstrarlíkan fyrirtækisins, eru mælingar á stærð (runu og raðnúmer) háð meiri sveigjanleika.</span><span class="sxs-lookup"><span data-stu-id="b5452-112">However, to reflect the operational model of the business, tracking dimensions (batch and serial numbers) are subject to more flexibility.</span></span> <span data-ttu-id="b5452-113">Stigveldi birgðapöntunar rúmar atburðarás þar sem eftirfarandi skilyrði eiga við:</span><span class="sxs-lookup"><span data-stu-id="b5452-113">An inventory reservation hierarchy can accommodate scenarios where the following conditions apply:</span></span>

- <span data-ttu-id="b5452-114">Fyrirtækið treystir á vörugeymslu sína til að stjórna töku á magni sem hefur lotu eða raðnúmer eftir að magnið hefur fundist í geymsluhúsnæðinu.</span><span class="sxs-lookup"><span data-stu-id="b5452-114">The business relies on its warehouse operations to manage picking of quantities that have batch or serial numbers after the quantities have been found in the warehousing storage space.</span></span> <span data-ttu-id="b5452-115">Oft er vísað til þessa líkans *Hópur-neðan\[staðsetningu\]*.</span><span class="sxs-lookup"><span data-stu-id="b5452-115">This model is often referred to as *Batch-below\[location\]*.</span></span> <span data-ttu-id="b5452-116">Það er venjulega notað þegar framleiðslueining vöru eða raðnúmer er ekki mikilvægt fyrir viðskiptavini sem setja eftirspurnina hjá sölufyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="b5452-116">It's typically used when a product's batch or serial number identification isn't important to the customers who place the demand with the selling company.</span></span>
- <span data-ttu-id="b5452-117">Ef lotu- eða raðnúmer eru hluti af pöntunarlýsingu viðskiptavinarins og þau eru skráð í eftirspurnarpöntun, eru vörugeymsluaðgerðirnar sem finna magn í vöruhúsinu takmarkaðar af sérstökum númerum sem óskað er eftir og hafa ekki leyfi til að breyta þeim.</span><span class="sxs-lookup"><span data-stu-id="b5452-117">If batch or serial numbers are part of a customer's order specification, and they are recorded on the demand order, the warehouse operations that find the quantities in the warehouse are constrained by the specific requested numbers and aren't allowed to change them.</span></span> <span data-ttu-id="b5452-118">Vísað er til þessa líkans *Hópur-ofan\[staðsetningu\]*.</span><span class="sxs-lookup"><span data-stu-id="b5452-118">This model is referred to as *Batch-above\[location\]*.</span></span>

<span data-ttu-id="b5452-119">Í þessum atburðarásum er áskorunin sú að aðeins er hægt að úthluta einum birgða pöntunarveldi fyrir hverja vöru sem gefin er út.</span><span class="sxs-lookup"><span data-stu-id="b5452-119">In these scenarios, the challenge is that only one inventory reservation hierarchy can be assigned to each released product.</span></span> <span data-ttu-id="b5452-120">Þess vegna, fyrir WMS til að meðhöndla rakta hluti, eftir að stigveldi verkefnisins ákvarðar hvenær á að panta lotu eða raðnúmer (annað hvort þegar eftirspurnarpöntunin er tekin eða meðan á pökkunarvinnu vörugeymslu stendur), er ekki hægt að breyta þessari tímasetningu í auglýsingu -hoc grundvöllur.</span><span class="sxs-lookup"><span data-stu-id="b5452-120">Therefore, for the WMS to handle tracked items, after the hierarchy assignment determines when the batch or serial number should be reserved (either when the demand order is taken or during the warehouse picking work), this timing can't be changed on an ad-hoc basis.</span></span>

## <a name="flexible-reservation-for-batch-tracked-items"></a><span data-ttu-id="b5452-121">Sveigjanlegur fyrirvari fyrir hluti sem rekja má hóp</span><span class="sxs-lookup"><span data-stu-id="b5452-121">Flexible reservation for batch-tracked items</span></span>

### <a name="business-scenario"></a><span data-ttu-id="b5452-122">Sviðsmynd fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="b5452-122">Business scenario</span></span>

<span data-ttu-id="b5452-123">Í þessari atburðarás notar fyrirtæki birgðarstefnu þar sem fullunnum vörum er rakið eftir lotunúmerum.</span><span class="sxs-lookup"><span data-stu-id="b5452-123">In this scenario, a company uses an inventory strategy where finished goods are tracked by batch numbers.</span></span> <span data-ttu-id="b5452-124">Þetta fyrirtæki notar einnig WMS vinnuálag.</span><span class="sxs-lookup"><span data-stu-id="b5452-124">This company also uses the WMS workload.</span></span> <span data-ttu-id="b5452-125">Vegna þess að þetta vinnuálag hefur vel útbúna röksemdafærslu til að skipuleggja og keyra vörugeymslu og flutningsaðgerðir fyrir hluti sem eru búnir til í hópum eru flestir fullbúnir hlutir tengdir „hópur hér að neðan\[staðsetningu\]" stigveldi birgða fyrirvara.</span><span class="sxs-lookup"><span data-stu-id="b5452-125">Because this workload has well-equipped logic for planning and running warehouse picking and shipping operations for batch-enabled items, most of the finished items are associated with a "Batch-below\[location\]" inventory reservation hierarchy.</span></span> <span data-ttu-id="b5452-126">Kosturinn við þessa tegund rekstraruppsetningar er að ákvörðunum (sem eru í raun fyrirvara um fyrirvaralausar ákvarðanir) um hvaða runur á að velja og hvar eigi að setja þær í vörugeymslunni er frestað þangað til að vörugeymsla hefst.</span><span class="sxs-lookup"><span data-stu-id="b5452-126">The advantage of this type of operational setup is that decisions (which are effectively reservation decisions) about which batches to pick and where to put them in the warehouse are postponed until the warehouse picking operations start.</span></span> <span data-ttu-id="b5452-127">Þeir eru ekki gerðir þegar pöntun viðskiptavinarins er sett.</span><span class="sxs-lookup"><span data-stu-id="b5452-127">They aren't made when the customer's order is placed.</span></span>

<span data-ttu-id="b5452-128">Þó að „hópurinn hér að neðan\[staðsetningu\]„ Pöntunarveldi þjónar vel markmiðum fyrirtækisins, margir af rótgrónum viðskiptavinum fyrirtækisins þurfa sömu lotu og þeir keyptu áður þegar þeir panta vörur.</span><span class="sxs-lookup"><span data-stu-id="b5452-128">Although the "Batch-below\[location\]" reservation hierarchy serves the company's business goals well, many of the company's established customers require the same batch that they previously purchased when they reorder products.</span></span> <span data-ttu-id="b5452-129">Þess vegna er fyrirtækið að leita að sveigjanleika í meðhöndlun reglna um röðun pöntunar svo að eftir atvikum viðskiptavina eftir sama hlut, gerist eftirfarandi hegðun:</span><span class="sxs-lookup"><span data-stu-id="b5452-129">Therefore, the company is looking for flexibility in the way that the batch reservation rules are handled, so that, depending on the customers' demand for the same item, the following behaviors occur:</span></span>

- <span data-ttu-id="b5452-130">Hægt er að skrá lotunúmer og panta þegar pöntunin er tekin af söluaðilanum og ekki er hægt að breyta því við vörugeymslu og / eða taka af öðrum kröfum.</span><span class="sxs-lookup"><span data-stu-id="b5452-130">A batch number can be recorded and reserved when the order is taken by the sales processor, and it can't be changed during warehouse operations and/or taken by other demands.</span></span> <span data-ttu-id="b5452-131">Þessi hegðun hjálpar til við að tryggja að lotunúmerið sem var pantað er sent til viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="b5452-131">This behavior helps guarantee that the batch number that was ordered is shipped to the customer.</span></span>
- <span data-ttu-id="b5452-132">Ef lotunúmerið er ekki mikilvægt fyrir viðskiptavininn, þá geta vörugeymsluaðgerðir ákvarðað lotunúmer meðan á vinnu stendur, eftir að skráning og pöntun sölupöntunar hefur verið gert.</span><span class="sxs-lookup"><span data-stu-id="b5452-132">If the batch number isn't important to the customer, the warehouse operations can determine a batch number during picking work, after sales order registration and reservation have been done.</span></span>

### <a name="allowing-reservation-of-a-specific-batch-on-the-sales-order"></a><span data-ttu-id="b5452-133">Leyfa fyrirvara um ákveðna lotu í sölupöntuninni</span><span class="sxs-lookup"><span data-stu-id="b5452-133">Allowing reservation of a specific batch on the sales order</span></span>

<span data-ttu-id="b5452-134">Til að koma til móts við æskilegan sveigjanleika í hegðun hóps fyrirvara fyrir hluti sem eru tengdir „hópur hér að neðan\[staðsetningu\]" stigveldi birgða fyrirvara, birgðasali verður að velja **Leyfa fyrirvara á pöntunarbeiðni** gátreitinn fyrir **Hópnúmer** stig á **Stigveldi birgða fyrirvara** síðu.</span><span class="sxs-lookup"><span data-stu-id="b5452-134">To accommodate the desired flexibility in the batch reservation behavior for items that are associated with a "Batch-below\[location\]" inventory reservation hierarchy, inventory managers must select the **Allow reservation on demand order** check box for the **Batch number** level on the **Inventory reservation hierarchies** page.</span></span>

![Stigveldi fyrir birgðafrátektir gert sveigjanlegt](media/Flexible-inventory-reservation-hierarchy.png)

<span data-ttu-id="b5452-136">Þegar stigið **Rununúmer** í stigveldinu er valið, allar víddir yfir því stigi og upp í gegnum **Staðsetning** stig verður sjálfkrafa valið.</span><span class="sxs-lookup"><span data-stu-id="b5452-136">When the **Batch number** level in the hierarchy is selected, all dimensions above that level and up through the **Location** level will be automatically selected.</span></span> <span data-ttu-id="b5452-137">(Sjálfgefið að allar víddir yfir **Staðsetning** stig eru valin.) Þessi hegðun endurspeglar rökfræði þar sem allar víddir á bilinu milli lotunúmers og staðsetningar eru einnig sjálfkrafa fráteknar eftir að þú hefur pantað tiltekið lotunúmer á pöntunarlínunni.</span><span class="sxs-lookup"><span data-stu-id="b5452-137">(By default, all dimensions above the **Location** level are preselected.) This behavior reflects the logic where all dimensions in the range between the batch number and location are also automatically reserved after you reserve a specific batch number on the order line.</span></span>

> [!NOTE]
> <span data-ttu-id="b5452-138">Gátreiturinn **Leyfa fyrirvara á pöntunarbeiðni** á aðeins við um stig stigveldis sem er undir staðsetningu víddar vörugeymslu.</span><span class="sxs-lookup"><span data-stu-id="b5452-138">The **Allow reservation on demand order** check box applies only to reservation hierarchy levels that are below the warehouse location dimension.</span></span>
>
> <span data-ttu-id="b5452-139">**Rununúmer** er eina stigið í stigveldinu sem er opið fyrir sveigjanlega pöntunarstefnu.</span><span class="sxs-lookup"><span data-stu-id="b5452-139">**Batch number** is the only level in the hierarchy that is open for the flexible reservation policy.</span></span> <span data-ttu-id="b5452-140">Með öðrum orðum, þú getur ekki valið gátreiturinn **Leyfa fyrirvara á pöntunarbeiðni** fyrir **Staðsetning**, **Númeraplata**, eða **Raðnúmer** stigi.</span><span class="sxs-lookup"><span data-stu-id="b5452-140">In other words, you can't select the **Allow reservation on demand order** check box for the **Location**, **License plate**, or **Serial number** level.</span></span>
>
> <span data-ttu-id="b5452-141">Ef pöntunarveldið þitt inniheldur röð raðnúmera (sem verður alltaf að vera undir **Rununúmer** stig), og ef þú hefur kveikt á lotusértækum fyrirvara fyrir lotunúmerið mun kerfið halda áfram að sjá um röðun og tína aðgerðir á raðnúmerum, byggt á reglunum sem eiga við um „Rað-neðan\[staðsetningu\]" fyrirvara stefnu.</span><span class="sxs-lookup"><span data-stu-id="b5452-141">If your reservation hierarchy includes the serial number dimension (which must always be below the **Batch number** level), and if you've turned on batch-specific reservation for the batch number, the system will continue to handle serial number reservation and picking operations, based on the rules that apply to the "Serial-below\[location\]" reservation policy.</span></span>

<span data-ttu-id="b5452-142">Hvenær sem er geturðu leyft lotusértæka pöntun fyrir núverandi „runu hér að neðan\[staðsetningu\]" pöntunarveldi í uppsetningu þinni.</span><span class="sxs-lookup"><span data-stu-id="b5452-142">At any point, you can allow batch-specific reservation for an existing "Batch-below\[location\]" reservation hierarchy in your deployment.</span></span> <span data-ttu-id="b5452-143">Þessi breyting mun ekki hafa áhrif á neina fyrirvara og opna vöruhúsavinnu sem voru búin til áður en breytingin átti sér stað.</span><span class="sxs-lookup"><span data-stu-id="b5452-143">This change won't affect any reservations and open warehouse work that were created before the change occurred.</span></span> <span data-ttu-id="b5452-144">Hins vegar **Leyfa fyrirvara á pöntunarbeiðni** Ekki er hægt að hreinsa gátreitinn ef birgðafærslur á **Frátekið pantað**, **Frátekin líkamleg**, eða **Pantaði** útgáfutegund er til fyrir einn eða fleiri hluti sem eru tengdir því pöntunarveldi.</span><span class="sxs-lookup"><span data-stu-id="b5452-144">However, the **Allow reservation on demand order** check box can't be cleared if inventory transactions of the **Reserved ordered**, **Reserved physical**, or **Ordered** issue type exist for one or more items that are associated with that reservation hierarchy.</span></span>

> [!NOTE]
> <span data-ttu-id="b5452-145">Ef núverandi fyrirvaralegveldi hlutar leyfir ekki forskrift lotur í pöntuninni, þá geturðu endurúthlutað því í pöntunarveldi sem gerir kleift að skilgreina lotu, að því tilskildu að stigskipulag stigveldisins sé það sama í báðum stigveldum.</span><span class="sxs-lookup"><span data-stu-id="b5452-145">If an item's existing reservation hierarchy doesn't allow batch specification on the order, you can reassign it to a reservation hierarchy that does allow batch specification, provided that the hierarchy level structure is the same in both hierarchies.</span></span> <span data-ttu-id="b5452-146">Nota **Breyta pöntunarveldi fyrir hluti** virka til að framkvæma endurúthlutun.</span><span class="sxs-lookup"><span data-stu-id="b5452-146">Use the **Change reservation hierarchy for items** function to do the reassignment.</span></span> <span data-ttu-id="b5452-147">Þessi breyting gæti skipt máli þegar þú vilt koma í veg fyrir sveigjanlegan pöntunarhluta fyrir hlutmengi af hlutum sem eru rekin í hópum en leyfa það fyrir restina af vöruframboði.</span><span class="sxs-lookup"><span data-stu-id="b5452-147">This change might be relevant when you want to prevent flexible batch reservation for a subset of batch-tracked items but allow it for the rest of the product portfolio.</span></span>

<span data-ttu-id="b5452-148">Óháð því hvort þú hefur valið **Leyfa fyrirvara á pöntunarbeiðni** gátreitinn, ef þú vilt ekki panta sérstakt lotunúmer fyrir hlutinn á pöntunarlínu, þá er sjálfgefin rökfræði aðgerða vörugeymsla sem gildir fyrir „Hóp hér að neðan\[staðsetningu\]" fyrirkomulag stigveldi mun enn eiga við.</span><span class="sxs-lookup"><span data-stu-id="b5452-148">Regardless of whether you've selected the **Allow reservation on demand order** check box, if you don't want to reserve a specific batch number for the item on an order line, default warehouse operations logic that is valid for a "Batch-below\[location\]" reservation hierarchy will still apply.</span></span>

### <a name="reserve-a-specific-batch-number-for-a-customer-order"></a><span data-ttu-id="b5452-149">Pantaðu tiltekið lotunúmer fyrir pöntun viðskiptavina</span><span class="sxs-lookup"><span data-stu-id="b5452-149">Reserve a specific batch number for a customer order</span></span>

<span data-ttu-id="b5452-150">Eftir hlut sem er rekja hópur er „Hópur hér að neðan\[staðsetningu\]„ Stigveldi birgðapöntunar er sett upp til að leyfa fyrirvara á tilteknum lotunúmerum á sölupöntunum, sölupöntunaraðilar geta tekið pantanir viðskiptavina fyrir sama hlut á einn af eftirfarandi leiðum, allt eftir beiðni viðskiptavinarins:</span><span class="sxs-lookup"><span data-stu-id="b5452-150">After a batch-tracked item's "Batch-below\[location\]" inventory reservation hierarchy is set up to allow reservation of specific batch numbers on sales orders, sales order processors can take customer orders for the same item in one of the following ways, depending on the customer's request:</span></span>

- <span data-ttu-id="b5452-151">**Sláðu inn pöntunarupplýsingar án þess að tilgreina lotunúmer** - Þessa nálgun ætti að nota þegar framleiðslulota vöru er ekki mikilvæg fyrir viðskiptavininn.</span><span class="sxs-lookup"><span data-stu-id="b5452-151">**Enter order details without specifying a batch number** – This approach should be used when the product's batch specification isn't important to the customer.</span></span> <span data-ttu-id="b5452-152">Allir núverandi ferlar sem tengjast meðhöndlun pöntunar af þessari gerð kerfisins eru óbreytt.</span><span class="sxs-lookup"><span data-stu-id="b5452-152">All existing processes that are associated with handling an order of this type in the system remain unchanged.</span></span> <span data-ttu-id="b5452-153">Engin viðbótarsjónarmið eru nauðsynleg af hálfu notenda.</span><span class="sxs-lookup"><span data-stu-id="b5452-153">No additional considerations are required on the part of users.</span></span>
- <span data-ttu-id="b5452-154">**Sláðu inn pöntunarupplýsingar og pantaðu tiltekið lotunúmer** - Þessa aðferð ætti að nota þegar viðskiptavinurinn óskar eftir ákveðinni lotu.</span><span class="sxs-lookup"><span data-stu-id="b5452-154">**Enter order details and reserve a specific batch number** – This approach should be used when the customer requests a specific batch.</span></span> <span data-ttu-id="b5452-155">Venjulega munu viðskiptavinir biðja um ákveðna lotu þegar þeir eru að panta vöru sem þeir keyptu áður.</span><span class="sxs-lookup"><span data-stu-id="b5452-155">Typically, customers will request a specific batch when they are reordering a product that they previously purchased.</span></span> <span data-ttu-id="b5452-156">Þessari tegund af sértækum pöntunum er vísað til *pöntunarbundinn fyrirvara*.</span><span class="sxs-lookup"><span data-stu-id="b5452-156">This type of batch-specific reservation is referred to as *order-committed reservation*.</span></span>

<span data-ttu-id="b5452-157">Eftirfarandi reglur eru í gildi þegar magn er afgreitt og lotunúmer er skuldbundið til sérstakrar pöntunar:</span><span class="sxs-lookup"><span data-stu-id="b5452-157">The following set of rules is valid when quantities are processed, and a batch number is committed to a specific order:</span></span>

- <span data-ttu-id="b5452-158">Til að leyfa fyrirvara á ákveðnu lotunúmeri fyrir hlut undir „Hópur hér að neðan\[staðsetningu\]" pöntunarstefna, kerfið verður að panta allar víddir upp í gegnum staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="b5452-158">To allow reservation of a specific batch number for an item under the "Batch-below\[location\]" reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="b5452-159">Þetta svið inniheldur venjulega stærð skírteinisins.</span><span class="sxs-lookup"><span data-stu-id="b5452-159">This range typically includes the license plate dimension.</span></span>
- <span data-ttu-id="b5452-160">Staðsetningartilskipanir eru ekki notaðar þegar val á vinnu er búið til fyrir sölulínu sem notar pöntunarbundna hópapöntun.</span><span class="sxs-lookup"><span data-stu-id="b5452-160">Location directives aren't used when picking work is created for a sales line that uses order-committed batch reservation.</span></span>
- <span data-ttu-id="b5452-161">Við vinnslu vörugeymslu á vinnu fyrir pöntunarbundna lotur er hvorki notanda né kerfinu heimilt að breyta lotunúmerinu.</span><span class="sxs-lookup"><span data-stu-id="b5452-161">During warehouse processing of work for order-committed batches, neither the user nor the system is allowed to change the batch number.</span></span> <span data-ttu-id="b5452-162">(Þessi vinnsla felur í sér meðhöndlun undantekninga.)</span><span class="sxs-lookup"><span data-stu-id="b5452-162">(This processing includes exception handling.)</span></span>

<span data-ttu-id="b5452-163">Eftirfarandi dæmi sýnir flæði frá enda til enda.</span><span class="sxs-lookup"><span data-stu-id="b5452-163">The following example shows the end-to-end flow.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="b5452-164">Dæmi</span><span class="sxs-lookup"><span data-stu-id="b5452-164">Example scenario</span></span>

<span data-ttu-id="b5452-165">Fyrir þetta dæmi verða kynningargögn að vera sett upp og þú verður að nota kynningarfyrirtækið **USMF**.</span><span class="sxs-lookup"><span data-stu-id="b5452-165">For this example, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="set-up-an-inventory-reservation-hierarchy-to-allow-batch-specific-reservation"></a><span data-ttu-id="b5452-166">Setjið upp stigveldi birgða fyrirvara til að leyfa ákveðna pöntun</span><span class="sxs-lookup"><span data-stu-id="b5452-166">Set up an inventory reservation hierarchy to allow batch-specific reservation</span></span>

1. <span data-ttu-id="b5452-167">Fara til **Vöruhúsastjórnun** \> **Skipulag** \> **Birgðir \> Pöntunarveldi**.</span><span class="sxs-lookup"><span data-stu-id="b5452-167">Go to **Warehouse management** \> **Setup** \> **Inventory \> Reservation hierarchy**.</span></span>
2. <span data-ttu-id="b5452-168">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="b5452-168">Select **New**.</span></span>
3. <span data-ttu-id="b5452-169">Í reitnum **Heiti** skaltu slá inn nafn (til dæmis **BatchFlex**).</span><span class="sxs-lookup"><span data-stu-id="b5452-169">In the **Name** field, enter a name (for example, **BatchFlex**).</span></span>
4. <span data-ttu-id="b5452-170">Í reitinn **Lýsing** slærðu inn lýsingu (t.d. **Hópur fyrir neðan sveigjanlegan**).</span><span class="sxs-lookup"><span data-stu-id="b5452-170">In the **Description** field, enter a description (for example, **Batch below flexible**).</span></span>
5. <span data-ttu-id="b5452-171">Í reitinn **Valinn**, veldu **Raðnúmer** og **Eigandi** og veldu síðan vinstri örvarhnappinn til að færa þá í reitinn **Tiltækt**.</span><span class="sxs-lookup"><span data-stu-id="b5452-171">In the **Selected** field, select **Serial number** and **Owner**, and then select the left arrow button to move them to the **Available** field.</span></span>
6. <span data-ttu-id="b5452-172">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b5452-172">Select **OK**.</span></span>
7. <span data-ttu-id="b5452-173">Í röðinni fyrir **Hópnúmer** víddarstig, veldu **Leyfa fyrirvara á pöntunarbeiðni** gátreitinn.</span><span class="sxs-lookup"><span data-stu-id="b5452-173">In the row for the **Batch number** dimension level, select the **Allow reservation on demand order** check box.</span></span> <span data-ttu-id="b5452-174">Stigin **Númeraplata** og **Staðsetning** eru sjálfkrafa valin og þú getur ekki hreinsað gátreitina fyrir þá.</span><span class="sxs-lookup"><span data-stu-id="b5452-174">The **License plate** and **Location** levels are automatically selected, and you can't clear the check boxes for them.</span></span>
8. <span data-ttu-id="b5452-175">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="b5452-175">Select **Save**.</span></span>

### <a name="create-a-new-released-product"></a><span data-ttu-id="b5452-176">Stofna nýja útgefna afurð</span><span class="sxs-lookup"><span data-stu-id="b5452-176">Create a new released product</span></span>

1. <span data-ttu-id="b5452-177">Stilltu þrjár aðalgagnabreytur vörunnar með því að nota þessi gildi:</span><span class="sxs-lookup"><span data-stu-id="b5452-177">Set the product's three master data parameters by using these values:</span></span>

    - <span data-ttu-id="b5452-178">Í reitnum **Geymsluvíddarflokkur** velurðu **Ware**.</span><span class="sxs-lookup"><span data-stu-id="b5452-178">In the **Storage dimension group** field, select **Ware**.</span></span>
    - <span data-ttu-id="b5452-179">Í reitnum **Rakningarvíddarflokkur** velurðu **Batch-Phy**.</span><span class="sxs-lookup"><span data-stu-id="b5452-179">In the **Tracking dimension group** field, select **Batch-Phy**.</span></span>
    - <span data-ttu-id="b5452-180">Í skjámyndinni **Frátektastigveldi** velurðu **BatchFlex**.</span><span class="sxs-lookup"><span data-stu-id="b5452-180">In the **Reservation hierarchy** field, select **BatchFlex**.</span></span>

2. <span data-ttu-id="b5452-181">Búðu til tvö lotunúmer, svo sem **B11** og **B22**.</span><span class="sxs-lookup"><span data-stu-id="b5452-181">Create two batch numbers, such as **B11** and **B22**.</span></span>
3. <span data-ttu-id="b5452-182">Bættu magni hlutar við á lager með því að nota eftirfarandi gildi.</span><span class="sxs-lookup"><span data-stu-id="b5452-182">Add item quantities to on-hand stock by using the following values.</span></span>

    | <span data-ttu-id="b5452-183">Vöruhús</span><span class="sxs-lookup"><span data-stu-id="b5452-183">Warehouse</span></span> | <span data-ttu-id="b5452-184">Rununúmer</span><span class="sxs-lookup"><span data-stu-id="b5452-184">Batch number</span></span> | <span data-ttu-id="b5452-185">Staðsetning</span><span class="sxs-lookup"><span data-stu-id="b5452-185">Location</span></span> | <span data-ttu-id="b5452-186">Númeraplata</span><span class="sxs-lookup"><span data-stu-id="b5452-186">License plate</span></span> | <span data-ttu-id="b5452-187">Magn</span><span class="sxs-lookup"><span data-stu-id="b5452-187">Quantity</span></span> |
    |-----------|--------------|----------|---------------|----------|
    | <span data-ttu-id="b5452-188">24</span><span class="sxs-lookup"><span data-stu-id="b5452-188">24</span></span>        | <span data-ttu-id="b5452-189">B11</span><span class="sxs-lookup"><span data-stu-id="b5452-189">B11</span></span>          | <span data-ttu-id="b5452-190">BULK-001</span><span class="sxs-lookup"><span data-stu-id="b5452-190">BULK-001</span></span> | <span data-ttu-id="b5452-191">Enginn</span><span class="sxs-lookup"><span data-stu-id="b5452-191">None</span></span>          | <span data-ttu-id="b5452-192">10</span><span class="sxs-lookup"><span data-stu-id="b5452-192">10</span></span>       |
    | <span data-ttu-id="b5452-193">24</span><span class="sxs-lookup"><span data-stu-id="b5452-193">24</span></span>        | <span data-ttu-id="b5452-194">B11</span><span class="sxs-lookup"><span data-stu-id="b5452-194">B11</span></span>          | <span data-ttu-id="b5452-195">FL-001</span><span class="sxs-lookup"><span data-stu-id="b5452-195">FL-001</span></span>   | <span data-ttu-id="b5452-196">LP11</span><span class="sxs-lookup"><span data-stu-id="b5452-196">LP11</span></span>          | <span data-ttu-id="b5452-197">10</span><span class="sxs-lookup"><span data-stu-id="b5452-197">10</span></span>       |
    | <span data-ttu-id="b5452-198">24</span><span class="sxs-lookup"><span data-stu-id="b5452-198">24</span></span>        | <span data-ttu-id="b5452-199">B22</span><span class="sxs-lookup"><span data-stu-id="b5452-199">B22</span></span>          | <span data-ttu-id="b5452-200">FL-002</span><span class="sxs-lookup"><span data-stu-id="b5452-200">FL-002</span></span>   | <span data-ttu-id="b5452-201">LP22</span><span class="sxs-lookup"><span data-stu-id="b5452-201">LP22</span></span>          | <span data-ttu-id="b5452-202">10</span><span class="sxs-lookup"><span data-stu-id="b5452-202">10</span></span>       |

### <a name="enter-sales-order-details"></a><span data-ttu-id="b5452-203">Slá inn upplýsingar um sölupöntun</span><span class="sxs-lookup"><span data-stu-id="b5452-203">Enter sales order details</span></span>

1. <span data-ttu-id="b5452-204">Farðu í **Sölu og markaðssetningu** \> **Sölupantanir** \> **Allar sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="b5452-204">Go to **Sales and marketing** \> **Sales orders** \> **All sales orders**.</span></span>
2. <span data-ttu-id="b5452-205">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="b5452-205">Select **New**.</span></span>
3. <span data-ttu-id="b5452-206">Í sölupöntunarhausnum, í reitnum **Viðskiptavinur reikningur** slærðu inn **US-003**.</span><span class="sxs-lookup"><span data-stu-id="b5452-206">On the sales order header, in the **Customer account** field, enter **US-003**.</span></span>
4. <span data-ttu-id="b5452-207">Bættu við línu fyrir nýja vöru og sláðu inn **10** sem magnið.</span><span class="sxs-lookup"><span data-stu-id="b5452-207">Add a line for the new item, and enter **10** as the quantity.</span></span> <span data-ttu-id="b5452-208">Gangið úr skugga um að reiturinn **Vöruhús** er stillt á **24**.</span><span class="sxs-lookup"><span data-stu-id="b5452-208">Make sure that the **Warehouse** field is set to **24**.</span></span>
5. <span data-ttu-id="b5452-209">Á flýtiflipanum **Sölupöntunarlínur**, veldu **Birgðir** og síðan, í hópnum **Viðhalda**, veldu **Hópapöntun**.</span><span class="sxs-lookup"><span data-stu-id="b5452-209">On the **Sales order lines** FastTab, select **Inventory**, and then, in the **Maintain** group, select **Batch reservation**.</span></span> <span data-ttu-id="b5452-210">Síðan **Hópapöntun** sýnir lista yfir lotur sem hægt er að panta fyrir pöntunarlínuna.</span><span class="sxs-lookup"><span data-stu-id="b5452-210">The **Batch reservation** page shows a list of batches that are available for reservation for the order line.</span></span> <span data-ttu-id="b5452-211">Fyrir þetta dæmi sýnir það magn af **20** fyrir lotunúmer **B11** og magn af **10** fyrir lotunúmer **B22**.</span><span class="sxs-lookup"><span data-stu-id="b5452-211">For this example, it shows a quantity of **20** for batch number **B11** and a quantity of **10** for batch number **B22**.</span></span> <span data-ttu-id="b5452-212">Athugaðu að **Hópapöntun** síðu er ekki hægt að nálgast frá línu ef hluturinn á þeirri línu er tengdur „Hópur hér að neðan\[staðsetningu\]" pöntunarveldi nema að það sé sett upp til að leyfa ákveðna pöntun.</span><span class="sxs-lookup"><span data-stu-id="b5452-212">Note that the **Batch reservation** page cannot be accessed from a line if the item on that line is associated with "Batch-below\[location\]" reservation hierarchy unless it is set up to allow batch-specific reservation.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b5452-213">Til að panta ákveðna lotu fyrir sölupöntun verður þú að nota síðuna **Hópapöntun**.</span><span class="sxs-lookup"><span data-stu-id="b5452-213">To reserve a specific batch for a sales order, you must use the **Batch reservation** page.</span></span>
    >
    > <span data-ttu-id="b5452-214">Ef þú slærð inn lotunúmerið beint á sölupöntunarlínunni mun kerfið haga sér eins og þú hafir slegið inn sérstakt lotugildi fyrir hlut sem er háð „hópnum hér að neðan\[staðsetningu\]" fyrirvara stefnu.</span><span class="sxs-lookup"><span data-stu-id="b5452-214">If you enter the batch number directly on the sales order line, the system will behave as though you entered a specific batch value for an item that is subject to the "Batch-below\[location\]" reservation policy.</span></span> <span data-ttu-id="b5452-215">Þegar þú vistar línuna færðu viðvörunarskilaboð.</span><span class="sxs-lookup"><span data-stu-id="b5452-215">When you save the line, you will receive a warning message.</span></span> <span data-ttu-id="b5452-216">Ef þú staðfestir að tilgreina skuli lotunúmerið beint á pöntunarlínunni verður línan ekki meðhöndluð samkvæmt reglulegri vörugeymslu stjórnunar.</span><span class="sxs-lookup"><span data-stu-id="b5452-216">If you confirm that the batch number should be specified directly on the order line, the line won't be handled by the regular warehouse management logic.</span></span>
    >
    > <span data-ttu-id="b5452-217">Ef þú áskilur magnið af síðunni **Fyrirvari**, engin sérstök lota verður frátekin og framkvæmd vörugeymsluaðgerða fyrir línuna mun fylgja þeim reglum sem gilda undir „Hópur hér að neðan\[staðsetningu\]" fyrirvara stefnu.</span><span class="sxs-lookup"><span data-stu-id="b5452-217">If you reserve the quantity from the **Reservation** page, no specific batch will be reserved, and the execution of warehouse operations for the line will follow the rules that are applicable under the "Batch-below\[location\]" reservation policy.</span></span>

    <span data-ttu-id="b5452-218">Almennt virkar þessi síða og er samspiluð á sama hátt og hún virkar og er samspiluð þeim með atriðum sem hafa tilheyrandi frátektarveldi „Hópurinn hér að ofan\[staðsetningu\]" gerð.</span><span class="sxs-lookup"><span data-stu-id="b5452-218">In general, this page works and is interacted with in the same way that it works and is interacted with for items that have an associated reservation hierarchy of the "Batch-above\[location\]" type.</span></span> <span data-ttu-id="b5452-219">Eftirfarandi undantekningar eiga þó við:</span><span class="sxs-lookup"><span data-stu-id="b5452-219">However, the following exceptions apply:</span></span>

    - <span data-ttu-id="b5452-220">Flýtiflipinn **Hópatölur skuldbundnar til upprunalínu** sýnir lotunúmerin sem eru frátekin fyrir pöntunarlínuna.</span><span class="sxs-lookup"><span data-stu-id="b5452-220">The **Batch numbers committed to source line** FastTab shows the batch numbers that are reserved for the order line.</span></span> <span data-ttu-id="b5452-221">Runugildin í hnitanetinu verða sýnd í gegnum allan uppfyllingartíma pöntunarlínunnar, þar á meðal stig vöruhúsavinnslunnar.</span><span class="sxs-lookup"><span data-stu-id="b5452-221">The batch values in the grid will be shown throughout the fulfillment cycle of the order line, including the warehouse processing stages.</span></span> <span data-ttu-id="b5452-222">Aftur á móti, á flýtiflipanum **Yfirlit**, venjulegur pöntunarlínupöntun (það er fyrirvari sem er gerður fyrir málin fyrir ofan **Staðsetning** stig) er sýnt í töflunni upp að því marki þegar vörugeymsla er búin til.</span><span class="sxs-lookup"><span data-stu-id="b5452-222">By contrast, on the **Overview** FastTab, regular order line reservation (that is, reservation that is done for the dimensions above the **Location** level) is shown in the grid up to the point when warehouse work is created.</span></span> <span data-ttu-id="b5452-223">Vinnuaðilinn tekur svo við línupöntuninni og línupöntunin birtist ekki lengur á síðunni.</span><span class="sxs-lookup"><span data-stu-id="b5452-223">The work entity then takes over the line reservation, and the line reservation no longer appears on the page.</span></span> <span data-ttu-id="b5452-224">Flýtiflipinn **Hópatölur skuldbundnar til upprunalínu** hjálpar til við að ábyrgjast að sölupöntunaraðili getur skoðað lotunúmerin sem voru skuldbundin pöntun viðskiptavinarins hvenær sem er á líftíma hans, upp í gegnum reikninga.</span><span class="sxs-lookup"><span data-stu-id="b5452-224">The **Batch numbers committed to source line** FastTab helps guarantee that the sales order processor can view the batch numbers that were committed to the customer's order at any point during its lifecycle, up through invoicing.</span></span>
    - <span data-ttu-id="b5452-225">Auk þess að panta sértæka lotu getur notandi valið handvirkt sértækan stað og framleiðslueiningar plötunnar í stað þess að láta kerfið velja þá sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="b5452-225">In addition to reserving a specific batch, a user can manually select the batch's specific location and license plate instead of letting the system automatically select them.</span></span> <span data-ttu-id="b5452-226">Þessi hæfileiki tengist hönnun pöntunarbundins fyrirkomulags fyrir pöntun.</span><span class="sxs-lookup"><span data-stu-id="b5452-226">This capability is related to the design of the order-committed batch reservation mechanism.</span></span> <span data-ttu-id="b5452-227">Eins og nefnt var áður, þegar rununúmer er tekið frá fyrir vöru undir „Hópur hér að neðan\[staðsetningu\]" pöntunarstefna, kerfið verður að panta allar víddir upp í gegnum staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="b5452-227">As was mentioned earlier, when a batch number is reserved for an item under the "Batch-below\[location\]" reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="b5452-228">Þess vegna mun vörugeymsla hafa sömu geymsluvíddir og notendurnir sem unnu með pantanirnar áskildu og það gæti ekki alltaf táknað geymslu hlutarins sem er þægilegt eða jafnvel mögulegt fyrir tínaaðgerðir.</span><span class="sxs-lookup"><span data-stu-id="b5452-228">Therefore, warehouse work will carry the same storage dimensions that were reserved by the users who worked with the orders, and it might not always represent the item storage placement that is convenient, or even possible, for picking operations.</span></span> <span data-ttu-id="b5452-229">Ef pöntunaraðilar eru meðvitaðir um takmarkanir vörugeymslu, gætu þeir viljað handvirkt velja tiltekna staði og leyfismerki þegar þeir panta hóp.</span><span class="sxs-lookup"><span data-stu-id="b5452-229">If order processors are aware of the warehouse constraints, they might want to manually select the specific locations and license plates when they reserve a batch.</span></span> <span data-ttu-id="b5452-230">Í þessu tilfelli verður notandinn að nota **Sýna mál** virkni á síðuhausnum og verður að bæta við staðsetningu og kennitala í ristina á flýtiflipanum **Yfirlit**.</span><span class="sxs-lookup"><span data-stu-id="b5452-230">In this case, the user must use the **Display dimensions** functionality on the page header, and must add the location and license plate in the grid on the **Overview** FastTab.</span></span>

6. <span data-ttu-id="b5452-231">Á **Hópapöntun** síðu, veldu línuna fyrir hópinn **B11** og veldu síðan **Varalína**.</span><span class="sxs-lookup"><span data-stu-id="b5452-231">On the **Batch reservation** page, select the line for batch **B11**, and then select **Reserve line**.</span></span> <span data-ttu-id="b5452-232">Það er engin tiltekin rökfræði til að úthluta staðsetningum og skiltum við sjálfvirka fyrirvara.</span><span class="sxs-lookup"><span data-stu-id="b5452-232">There is no designated logic for assigning locations and license plates during automatic reservation.</span></span> <span data-ttu-id="b5452-233">Þú getur slegið inn magnið handvirkt í reitinn **Frátekning**.</span><span class="sxs-lookup"><span data-stu-id="b5452-233">You can manually enter the quantity in the **Reservation** field.</span></span> <span data-ttu-id="b5452-234">Taktu eftir því að á flýtiflipanum **Hópatölur skuldbundnar til upprunalínu**, hópur **B11** er sýnt sem **Skuldbundinn**.</span><span class="sxs-lookup"><span data-stu-id="b5452-234">Notice that, on the **Batch numbers committed to source line** FastTab, batch **B11** is shown as **Committed**.</span></span>

    ![Að fremja ákveðið lotunúmer í sölupöntunarlínu á síðu síðu frátektar á runu](media/Batch-reservation-form-with-order-committed-reservation.png)

    > [!NOTE]
    > <span data-ttu-id="b5452-236">Bókun magns á sölupöntunarlínu er hægt að gera í mörgum lotum.</span><span class="sxs-lookup"><span data-stu-id="b5452-236">Reservation of the quantity on a sales order line can be done across multiple batches.</span></span> <span data-ttu-id="b5452-237">Sömuleiðis er hægt að panta sömu lotu gagnvart mörgum stöðum og skiltum (ef leyfisplötur eru virkar fyrir staðina).</span><span class="sxs-lookup"><span data-stu-id="b5452-237">Likewise, reservation of the same batch can be done against multiple locations and license plates (if license plates are enabled for the locations).</span></span>
    >
    > <span data-ttu-id="b5452-238">Pöntun á tiltekinni lotu fyrir magnið á sölupöntunarlínu getur einnig verið að hluta.</span><span class="sxs-lookup"><span data-stu-id="b5452-238">Reservation of a specific batch for the quantity on a sales order line can also be partial.</span></span> <span data-ttu-id="b5452-239">Til dæmis er hægt að panta heildarmagn 100 eininga þannig að ákveðin lota er skuldbundin til 20 eininga en 80 einingar eru fráteknar á staðnum og vörugeymslustigi fyrir alla tiltæka lotu.</span><span class="sxs-lookup"><span data-stu-id="b5452-239">For example, the total quantity of 100 units can be reserved so that a specific batch is committed to 20 units, whereas 80 units are reserved at the site and warehouse levels for any available batch.</span></span> <span data-ttu-id="b5452-240">Í þessu tilfelli mun WMS sjá um tínaaðgerðir með því að nota tvær aðskildar vinnulínur.</span><span class="sxs-lookup"><span data-stu-id="b5452-240">In this case, the WMS will handle picking operations by using two separate work lines.</span></span>

7. <span data-ttu-id="b5452-241">Farðu í **Afurðaupplýsingastjórnun** \> **Afurðir** \> **Losaðar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="b5452-241">Go to **Product information management** \> **Products** \> **Released products**.</span></span> <span data-ttu-id="b5452-242">Veldu hlutinn þinn og veldu síðan **Stjórna birgðum** \> **Skoða** \> **Færslur**.</span><span class="sxs-lookup"><span data-stu-id="b5452-242">Select your item, and then select **Manage inventory** \> **View** \> **Transactions**.</span></span>

    ![Pöntunarbundin fyrirvara sem birgðafærslugerð](media/Inventory-transactions-for-order-committed-reservation.png)

8. <span data-ttu-id="b5452-244">Skoðaðu birgðafærslur hlutarins sem tengjast pöntun sölupöntunarlínunnar.</span><span class="sxs-lookup"><span data-stu-id="b5452-244">Review the item's inventory transactions that are related to the sales order line reservation.</span></span>

    - <span data-ttu-id="b5452-245">Viðskipti þar sem **Tilvísun** reiturinn er stilltur á **Sölupöntun** og **Mál** reiturinn er stilltur á **Frátekin líkamleg** táknar pöntunarlínu fyrirvara fyrir birgðavíddir fyrir ofan **Staðsetning** stigi.</span><span class="sxs-lookup"><span data-stu-id="b5452-245">A transaction where the **Reference** field is set to **Sales order** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the inventory dimensions above the **Location** level.</span></span> <span data-ttu-id="b5452-246">Samkvæmt stigveldi birgðapöntunar hlutanna eru þessar víddir staða, vörugeymsla og birgðastaða.</span><span class="sxs-lookup"><span data-stu-id="b5452-246">According to the item's inventory reservation hierarchy, those dimensions are site, warehouse, and inventory status.</span></span>
    - <span data-ttu-id="b5452-247">Viðskipti þar sem reiturinn **Tilvísun** er stilltur á **Pöntunarbundna frátekt** og reiturinn **Úthreyfing** er stilltur á **Frátekið á lager** táknar pöntunarlínu frátektar fyrir tiltekna runu og annar birgðavíddir fyrir ofan hana.</span><span class="sxs-lookup"><span data-stu-id="b5452-247">A transaction where the **Reference** field is set to **Order-committed reservation** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the specific batch and all inventory dimensions above it.</span></span> <span data-ttu-id="b5452-248">Samkvæmt stigveldi birgðapöntunar hlutanna eru þessar víddir rununúmer og staðsetning.</span><span class="sxs-lookup"><span data-stu-id="b5452-248">According to the item's inventory reservation hierarchy, those dimensions are batch number and location.</span></span> <span data-ttu-id="b5452-249">Í þessu dæmi er staðsetningin **Magn-001**.</span><span class="sxs-lookup"><span data-stu-id="b5452-249">In this example, the location is **Bulk-001**.</span></span>

9. <span data-ttu-id="b5452-250">Veldu á sölupöntunarhaus **Vöruhús** \> **Aðgerðir** \> **Losa í vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="b5452-250">On the sales order header, select **Warehouse** \> **Actions** \> **Release to warehouse**.</span></span> <span data-ttu-id="b5452-251">Pöntunarlínan hefur verið sett í bylgju og álag og vinna búin til.</span><span class="sxs-lookup"><span data-stu-id="b5452-251">The order line is now waved, and a load and work are created.</span></span>

### <a name="review-and-process-warehouse-work-that-has-order-committed-batch-numbers"></a><span data-ttu-id="b5452-252">Farið yfir og unnið úr vöruhúsagerð sem er með pöntunarbundna lotunúmer</span><span class="sxs-lookup"><span data-stu-id="b5452-252">Review and process warehouse work that has order-committed batch numbers</span></span>

1. <span data-ttu-id="b5452-253">Á flýtiflipanum **Sölupöntunarlínur**, veldu **Vöruhús** \> **Upplýsingar um vinnu**.</span><span class="sxs-lookup"><span data-stu-id="b5452-253">On the **Sales order lines** FastTab, select **Warehouse** \> **Work details**.</span></span>

    <span data-ttu-id="b5452-254">Vinnan sem annast tínsluaðgerðina fyrir magn magn sem skuldbundið sig til sölupöntunarlínunnar hefur eftirfarandi einkenni:</span><span class="sxs-lookup"><span data-stu-id="b5452-254">The work that handles the picking operation for batch quantities that are committed to the sales order line has the following characteristics:</span></span>

    - <span data-ttu-id="b5452-255">Til að búa til vinnu notar kerfið vinnusniðmát en ekki staðsetningartilskipanir.</span><span class="sxs-lookup"><span data-stu-id="b5452-255">To create work, the system uses work templates but not location directives.</span></span> <span data-ttu-id="b5452-256">Öllum stöðluðum stillingum sem eru skilgreindar fyrir vinnusniðmát, svo sem hámarksfjölda vallína eða ákveðin mælieining, verður beitt til að ákvarða hvenær ný vinna ætti að búa til.</span><span class="sxs-lookup"><span data-stu-id="b5452-256">All the standard settings that are defined for work templates, such as a maximum number of pick lines or a specific unit of measure, will be applied to determine when new work should be created.</span></span> <span data-ttu-id="b5452-257">Hins vegar er ekki tekið tillit til reglnanna sem eru tengdar staðsetningarleiðbeiningum til að bera kennsl á valstöðum, vegna þess að pöntunin sem framin er fyrir pöntunin tilgreinir þegar allar birgðarvíddirnar.</span><span class="sxs-lookup"><span data-stu-id="b5452-257">However, the rules that are associated with location directives for identifying pick locations aren't considered, because the order-committed reservation already specifies all the inventory dimensions.</span></span> <span data-ttu-id="b5452-258">Þessar birgðastærðir innihalda mál á lagergeymslu stigsins.</span><span class="sxs-lookup"><span data-stu-id="b5452-258">Those inventory dimensions include the dimensions at the warehouse storage level.</span></span> <span data-ttu-id="b5452-259">Þess vegna erfðir verkið þessar víddir án þess að þurfa að hafa samráð um staðsetningartilskipanir.</span><span class="sxs-lookup"><span data-stu-id="b5452-259">Therefore, the work inherits those dimensions without having to consult location directives.</span></span>
    - <span data-ttu-id="b5452-260">Hópnúmerið er ekki sýnt á velja línunni (eins og á við um vinnulínuna sem er búin til fyrir hlut sem er með tilheyrandi „hópur hér að ofan\[staðsetningu\]„ fyrirvara stigveldi.) Í staðinn eru„ frá “lotunúmerinu og öllum öðrum geymsluvíddum sýndar á verkbirgðir vinnu línunnar sem vísað er til úr tilheyrandi birgðafærslum.</span><span class="sxs-lookup"><span data-stu-id="b5452-260">The batch number isn't shown on the pick line (as is the case for the work line that is created for an item that has an associated "Batch-above\[location\]" reservation hierarchy.) Instead, the "from" batch number and all other storage dimensions are shown on the work line's work inventory transaction that is referenced from the associated inventory transactions.</span></span>

        ![Vörugeymslufærsla vegna vinnu sem er upprunnin í pöntunarbundinni frátekt](media/Work-inventory-transactions-for-order-committed-reservation.png)

    - <span data-ttu-id="b5452-262">Eftir að vinna er búin til, birgðir hlutarins þar sem **Tilvísun** reiturinn er stilltur á **Pöntunarbundin frátekt** er fjarlægður.</span><span class="sxs-lookup"><span data-stu-id="b5452-262">After work is created, the item's inventory transaction where the **Reference** field is set to **Order-committed reservation** is removed.</span></span> <span data-ttu-id="b5452-263">Birgðafærslan þar sem **Tilvísun** reiturinn er stilltur á **Vinna** geymir nú líkamlegan fyrirvara á öllum birgðastærðum magnsins.</span><span class="sxs-lookup"><span data-stu-id="b5452-263">The inventory transaction where the **Reference** field is set to **Work** now holds the physical reservation on all the quantity's inventory dimensions.</span></span>

        <span data-ttu-id="b5452-264">Vöruhúsaaðgerðir geta haldið áfram til að sjá um framkvæmd verksins á venjulegan hátt.</span><span class="sxs-lookup"><span data-stu-id="b5452-264">Warehouse operations can proceed to handle execution of the work in the usual manner.</span></span> <span data-ttu-id="b5452-265">Leiðbeiningarnar í farsímanum munu hins vegar leiðbeina starfsmanni að velja ákveðið lotunúmer.</span><span class="sxs-lookup"><span data-stu-id="b5452-265">However, the instructions on the mobile device will instruct the worker to pick a specific batch number.</span></span> <span data-ttu-id="b5452-266">Í vöruhúsumhverfi þar sem staðsetningar eru stjórnaðar með leyfi fyrir skiltum, eftir að starfsmaður hefur náð staðsetningu sem geymir sömu framleiðslulotu á mörgum skiltum, þá getur hann eða hún valið af hvaða skilti sem er ekki þegar frátekinn (til dæmis með annarri pöntun- skuldbundinn fyrirvara eða vinnu sem er upprunnin í fyrirvara af þeirri gerð.)</span><span class="sxs-lookup"><span data-stu-id="b5452-266">In warehouse environments where locations are license plate–controlled, after a worker reaches a location that stores the same batch on multiple license plates, he or she can pick from any license plate that isn't already reserved (for example, by another order-committed reservation or work that originates from a reservation of that type.)</span></span>

        <span data-ttu-id="b5452-267">Ef það reynist óframkvæmanlegt að velja frá þeim stað sem er tilgreindur á vinnulínunni geta rekstraraðilar vörugeymslu notað eina af eftirfarandi aðgerðum til að beina því að velja ákveðna lotu frá þægilegri stað:</span><span class="sxs-lookup"><span data-stu-id="b5452-267">If it turns out to be impractical to pick from the location that is specified on the work line, the warehouse operators can use one of the following actions to redirect picking of the specific batch from a more convenient location:</span></span>

        - <span data-ttu-id="b5452-268">Staðallinn **Hnekkja staðsetningu** aðgerð í farsíma (að því tilskildu að starfsmaður vörugeymslu **Leyfa val á staðsetningu staðsetningu** stilling er virk)</span><span class="sxs-lookup"><span data-stu-id="b5452-268">The standard **Override location** action on a mobile device (provided that the warehouse worker's **Allow pick location override** setting is enabled)</span></span>
        - <span data-ttu-id="b5452-269">Aðgerðin **Breyta staðsetningu** á **Upplýsingar um vinnulista** síðu.</span><span class="sxs-lookup"><span data-stu-id="b5452-269">The **Change location** action on the **Work list details** page.</span></span> 

2. <span data-ttu-id="b5452-270">Ljúktu við að velja og setja verkið í farsímann.</span><span class="sxs-lookup"><span data-stu-id="b5452-270">On the mobile device, finish picking and putting the work.</span></span>

    <span data-ttu-id="b5452-271">Magnið **10** fyrir lotunúmer **B11** er nú valinn í sölupöntunarlínuna og settur í **Afgreiðsluhurð** staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="b5452-271">The quantity of **10** for batch number **B11** is now picked for the sales order line and put in the **Baydoor** location.</span></span> <span data-ttu-id="b5452-272">Á þessum tímapunkti er það tilbúið að hlaða það á vörubílinn og senda á heimilisfang viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="b5452-272">At this point, it's ready to be loaded onto the truck and dispatched to the customer's address.</span></span>

## <a name="exception-handling-of-warehouse-work-that-has-order-committed-batch-numbers"></a><span data-ttu-id="b5452-273">Meðhöndlun undantekninga á vöruhúsavinnu sem er með rununúmer ráðstafaðra pantana</span><span class="sxs-lookup"><span data-stu-id="b5452-273">Exception handling of warehouse work that has order-committed batch numbers</span></span>

<span data-ttu-id="b5452-274">Vörugeymsla til að velja pöntunarbundin lotunúmer er háð sömu stöðluðu meðhöndlun undantekninga vörugeymslu og aðgerðum og venjuleg vinna.</span><span class="sxs-lookup"><span data-stu-id="b5452-274">Warehouse work for picking order-committed batch numbers is subject to the same standard warehouse exception handling and actions as regular work.</span></span> <span data-ttu-id="b5452-275">Almennt er hægt að hætta við opna verkið eða vinnu línuna, það er hægt að trufla það vegna þess að notendastaður er fullur, það er hægt að velja hann stutt og það er hægt að uppfæra hann vegna hreyfingar.</span><span class="sxs-lookup"><span data-stu-id="b5452-275">In general, the open work or work line can be canceled, it can be interrupted because a user location is full, it can be short-picked, and it can be updated because of a movement.</span></span> <span data-ttu-id="b5452-276">Sömuleiðis er hægt að draga úr valinni vinnu sem þegar hefur verið lokið eða hægt er að snúa verkinu við.</span><span class="sxs-lookup"><span data-stu-id="b5452-276">Likewise, the picked quantity of work that has already been completed can be reduced, or the work can be reversed.</span></span>

<span data-ttu-id="b5452-277">Eftirfarandi lykilregla er notuð við allar þessar undantekningarmeðferðaraðgerðir: aldrei er hægt að skipta um lotunúmer sem var frátekið fyrir viðskiptavininn fyrir annað lotunúmer, en hægt er að breyta geymsluvíddum hans (staðsetningu og kennitala) með annað hvort handvirkri uppfærslu af notanda eða sjálfvirka uppfærslu af kerfinu.</span><span class="sxs-lookup"><span data-stu-id="b5452-277">The following key rule is applied to all these exception handling actions: the batch number that was reserved for the customer can never be replaced with a different batch number, but its storage dimensions (location and license plate) can be changed through either a manual update by the user or an automatic update by the system.</span></span> <span data-ttu-id="b5452-278">Sjálfvirka uppfærslan er byggð á sömu handahófi úthlutun geymsluvíddar og gilti þegar ákveðin lota var sjálfkrafa frátekin en engar geymsluvíddir voru tilgreindar.</span><span class="sxs-lookup"><span data-stu-id="b5452-278">The automatic update is based on the same random assignment of storage dimensions that applied when a specific batch was automatically reserved but no storage dimensions were specified.</span></span>

### <a name="example-scenario"></a><span data-ttu-id="b5452-279">Dæmi</span><span class="sxs-lookup"><span data-stu-id="b5452-279">Example scenario</span></span>

<span data-ttu-id="b5452-280">Dæmi um þessa atburðarás er ástand þar sem verið er að velja áður lokið verk með því að nota virknina **Draga úr völdu magni**.</span><span class="sxs-lookup"><span data-stu-id="b5452-280">An example of this scenario is a situation where previously completed work is being unpicked by using the **Reduce picked quantity** function.</span></span> <span data-ttu-id="b5452-281">Þetta dæmi heldur áfram með fyrra dæminu í þessu efni.</span><span class="sxs-lookup"><span data-stu-id="b5452-281">This example continues the previous example in this topic.</span></span>

1. <span data-ttu-id="b5452-282">Farðu í **Vöruhúsakerfi** \> **Hleðslur** \> **Virkar hleðslur**.</span><span class="sxs-lookup"><span data-stu-id="b5452-282">Go to **Warehouse management** \> **Loads** \> **Active loads**.</span></span>
2. <span data-ttu-id="b5452-283">Veldu álag sem var búið til í tengslum við sendingu sölupöntunar þinnar.</span><span class="sxs-lookup"><span data-stu-id="b5452-283">Select the load that was created in connection with the shipment of your sales order.</span></span>
3. <span data-ttu-id="b5452-284">Af flýtiflipanum **Hlaðið pöntunarlínum**, veldu **Draga úr völdum magni**.</span><span class="sxs-lookup"><span data-stu-id="b5452-284">From the **Load order lines** FastTab, select **Reduce picked quantity**.</span></span>
4. <span data-ttu-id="b5452-285">Á **Draga úr völdum magni** síðu, í **Færa á staðsetningu** reit, veldu **FL-001**.</span><span class="sxs-lookup"><span data-stu-id="b5452-285">On the **Reduce picked quantity** page, in the **Move to location** field, select **FL-001**.</span></span>
5. <span data-ttu-id="b5452-286">Í reitnum **Flytja á númeraplötu** velurðu **LP33**.</span><span class="sxs-lookup"><span data-stu-id="b5452-286">In the **Move to license plate** field, select **LP33**.</span></span>
6. <span data-ttu-id="b5452-287">Í hnitanetinu í reitnum **Magn birgða til að afturkalla tiltekt á** sláðu inn **10**.</span><span class="sxs-lookup"><span data-stu-id="b5452-287">In the grid, in the **Inventory quantity to unpick** field, enter **10**.</span></span>
7. <span data-ttu-id="b5452-288">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b5452-288">Select **OK**.</span></span>

<span data-ttu-id="b5452-289">Hér eru niðurstöður úr aðgerð til að afturkalla tiltekt:</span><span class="sxs-lookup"><span data-stu-id="b5452-289">Here are the results of the unpicking action:</span></span>

- <span data-ttu-id="b5452-290">Staða fyrri lokaðs verks er stillt á **Hætt við**.</span><span class="sxs-lookup"><span data-stu-id="b5452-290">The status of the previously closed work is set to **Canceled**.</span></span>
- <span data-ttu-id="b5452-291">Nýtt verk af gerðinni **Birgðahreyfing** er búin til fyrir óvalið magn af **10** fyrir lotunúmer **B11**.</span><span class="sxs-lookup"><span data-stu-id="b5452-291">New work of the **Inventory movement** type is created for the unpicked quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="b5452-292">Þessi vinna táknar hreyfingu frá **Afgreiðsluhurð** staðsetningu til númeraplötu **LP33** á staðsetningu **FL-001**.</span><span class="sxs-lookup"><span data-stu-id="b5452-292">This work represents the movement from the **Baydoor** location to license plate **LP33** in location **FL-001**.</span></span> <span data-ttu-id="b5452-293">Staðan er stillt á **Lokað**.</span><span class="sxs-lookup"><span data-stu-id="b5452-293">The status is set to **Closed**.</span></span>
- <span data-ttu-id="b5452-294">Kerfið áskilur aftur lotunúmerið sem upphaflega var pantað og úthlutar auðkenni staðsetningar og korts.</span><span class="sxs-lookup"><span data-stu-id="b5452-294">The system re-reserves the batch number that was originally ordered, and assigns the location and license plate IDs.</span></span> <span data-ttu-id="b5452-295">(Þetta ferli jafngildir því að keyra virknina **Frátektarlína** fyrir pöntunarlínuna fyrir tiltekið lotunúmer).</span><span class="sxs-lookup"><span data-stu-id="b5452-295">(This process is equivalent to running the **Reserve line** function for the order line for a given batch number).</span></span> <span data-ttu-id="b5452-296">Fyrir vikið, hópur **B11** er sýnt sem framið á flýtiflipanum **Hópatölur skuldbundnar til upprunalínu** af **Runufrátekt** síðu og **Frátekt** reiturinn inniheldur magn af **10** fyrir lotunúmer **B11**.</span><span class="sxs-lookup"><span data-stu-id="b5452-296">As a result, batch **B11** is shown as committed on the **Batch numbers committed to source line** FastTab of the **Batch reservation** page, and the **Reservation** field contains a quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="b5452-297">Að auki, er **Staðsetning** reiturinn stilltur á **FL-001**, og **Númeraplata** reiturinn er stilltur á **LP11**.</span><span class="sxs-lookup"><span data-stu-id="b5452-297">Additionally, the **Location** field is set to **FL-001**, and the **License plate** field is set to **LP11**.</span></span> <span data-ttu-id="b5452-298">(Þú getur bætt þessum reitum við töfluna ef þeir eru ekki sýnilegir.)</span><span class="sxs-lookup"><span data-stu-id="b5452-298">(You can add these fields to the grid if they aren't visible.)</span></span>

<span data-ttu-id="b5452-299">Eftirfarandi töflur veita yfirlit sem sýnir hvernig kerfið meðhöndlar pöntunarbundna lotu fyrirvara fyrir sérstakar vörugeymsluaðgerðir.</span><span class="sxs-lookup"><span data-stu-id="b5452-299">The following tables provide an overview that shows how the system handles order-committed batch reservation for specific warehouse actions.</span></span> <span data-ttu-id="b5452-300">Til að túlka innihaldið í töflunum, gerðu ráð fyrir að hver vörugeymslaaðgerð sé keyrð í samhengi við núverandi vörugeymsluverk sem er upprunnin í pöntunarbundinni lotu fyrirvara, eða að framkvæmd hverrar vörugerðaraðgerðar hefur áhrif á vinnu af þeirri gerð.</span><span class="sxs-lookup"><span data-stu-id="b5452-300">To interpret the content in the tables, assume that each warehouse action is run in the context of existing warehouse work that originates from an order-committed batch reservation, or that execution of each warehouse action affects work of that type.</span></span>

> [!NOTE]
> <span data-ttu-id="b5452-301">Í þessum töflum gefur dálkurinn „Hópmagn er fáanlegt“ til kynna hvort magn af framleiðslulotu er til viðbótar við það magn sem er annað hvort þegar frátekið fyrir núverandi pöntunarbundna fyrirvara eða þegar er frátekið af vörugeymsluverkinu sem kemur frá fyrirvörum af þeirri gerð.</span><span class="sxs-lookup"><span data-stu-id="b5452-301">In these tables, the "Batch quantity is available" column indicates whether a batch quantity is available in addition to the quantity that is either already reserved for the current order-committed reservations or already reserved by the warehouse work that originates from reservations of that type.</span></span>

#### <a name="override-the-pick-location-on-the-open-work"></a><span data-ttu-id="b5452-302">Yfirskrifa tínslustaðsetningu í opinni vinnu</span><span class="sxs-lookup"><span data-stu-id="b5452-302">Override the pick location on the open work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b5452-303">Færibreyta lykiluppsetningar</span><span class="sxs-lookup"><span data-stu-id="b5452-303">Key setup parameter</span></span></th>
<th><span data-ttu-id="b5452-304">Runumagn er fáanlegt</span><span class="sxs-lookup"><span data-stu-id="b5452-304">Batch quantity is available</span></span></th>
<th><span data-ttu-id="b5452-305">Lykilþrep notenda</span><span class="sxs-lookup"><span data-stu-id="b5452-305">Key user steps</span></span></th>
<th><span data-ttu-id="b5452-306">Vinna vöruhúss</span><span class="sxs-lookup"><span data-stu-id="b5452-306">Warehouse work</span></span></th>
<th><span data-ttu-id="b5452-307">Pantanaskuldbundin hópapöntun</span><span class="sxs-lookup"><span data-stu-id="b5452-307">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="b5452-308">Valkosturinn <strong>Leyfa val á staðsetningu staðsetningu</strong> er virkur á starfsmanninum.</span><span class="sxs-lookup"><span data-stu-id="b5452-308">The <strong>Allow pick location override</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="b5452-309">Já</span><span class="sxs-lookup"><span data-stu-id="b5452-309">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="b5452-310">Veljið valmyndaratriðið <strong>Yfirskrifa staðsetningu</strong> í vöruhúsaforritinu þegar tiltektarverk er hafið.</span><span class="sxs-lookup"><span data-stu-id="b5452-310">Select the <strong>Override location</strong> menu item on the warehouse app when you start picking work.</span></span></li>
<li><span data-ttu-id="b5452-311">Veldu <strong>Stinga upp</strong>.</span><span class="sxs-lookup"><span data-stu-id="b5452-311">Select <strong>Suggest</strong>.</span></span></li>
<li><span data-ttu-id="b5452-312">Staðfestu nýja staðsetninguna sem lagt er til með tilliti til framboðs í fjölda magns.</span><span class="sxs-lookup"><span data-stu-id="b5452-312">Confirm the new location that is suggested based on batch quantity availability.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="b5452-313">Eftirfarandi aðgerðir eiga sér stað í núverandi vinnu:</span><span class="sxs-lookup"><span data-stu-id="b5452-313">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="b5452-314">Staðsetningin á velja línunni er uppfærð á nýjan stað.</span><span class="sxs-lookup"><span data-stu-id="b5452-314">The location on the pick line is updated to the new location.</span></span> <span data-ttu-id="b5452-315">(Ef staðsetningin er stjórnað með leyfismerki er úthlutað af handahófi leyfismerki fyrir vörubirgðafærsluna og starfsmaðurinn getur valið úr hvaða skilti sem er með tiltækt magn.)</span><span class="sxs-lookup"><span data-stu-id="b5452-315">(If the location is license plate–controlled, a random license plate is assigned to the work inventory transaction, and the worker can pick from any license plate that has available quantity.)</span></span></li>
<li><span data-ttu-id="b5452-316">Ef magnið er að finna á fleiri en einni leyfisplötu á nýjum stað, er upprunalegu vallínunni skipt í margar línur sem passa við hvern kennitala.</span><span class="sxs-lookup"><span data-stu-id="b5452-316">If the quantity is found on more than one license plate in the new location, the original pick line is split into multiple lines to match each license plate.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="b5452-317">Ekki tiltækt</span><span class="sxs-lookup"><span data-stu-id="b5452-317">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b5452-318">Ekkert</span><span class="sxs-lookup"><span data-stu-id="b5452-318">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="b5452-319">Veljið valmyndaratriðið <strong>Yfirskrifa staðsetningu</strong> í vöruhúsaforritinu þegar tiltektarverk er hafið.</span><span class="sxs-lookup"><span data-stu-id="b5452-319">Select the <strong>Override location</strong> menu item on the warehouse app when you start picking work.</span></span></li>
<li><span data-ttu-id="b5452-320">Færa handvirkt inn staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="b5452-320">Manually enter a location.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="b5452-321">Aðgerðin <strong>Hnekkja staðsetningu</strong> er ekki möguleg.</span><span class="sxs-lookup"><span data-stu-id="b5452-321">The <strong>Override location</strong> action isn't possible.</span></span> <span data-ttu-id="b5452-322">Það mistekst og villu er hent.</span><span class="sxs-lookup"><span data-stu-id="b5452-322">It fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="b5452-323">Á ekki við</span><span class="sxs-lookup"><span data-stu-id="b5452-323">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="full-button--split-a-work-line-because-of-overflow-on-the-user-location"></a><span data-ttu-id="b5452-324">Fullur hnappur - Skiptu vinnulínu vegna flæða á staðsetningu notandans</span><span class="sxs-lookup"><span data-stu-id="b5452-324">Full button – Split a work line because of overflow on the user location</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b5452-325">Færibreyta lykiluppsetningar</span><span class="sxs-lookup"><span data-stu-id="b5452-325">Key setup parameter</span></span></th>
<th><span data-ttu-id="b5452-326">Runumagn er fáanlegt</span><span class="sxs-lookup"><span data-stu-id="b5452-326">Batch quantity is available</span></span></th>
<th><span data-ttu-id="b5452-327">Lykilþrep notenda</span><span class="sxs-lookup"><span data-stu-id="b5452-327">Key user steps</span></span></th>
<th><span data-ttu-id="b5452-328">Vinna vöruhúss</span><span class="sxs-lookup"><span data-stu-id="b5452-328">Warehouse work</span></span></th>
<th><span data-ttu-id="b5452-329">Pantanaskuldbundin hópapöntun</span><span class="sxs-lookup"><span data-stu-id="b5452-329">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b5452-330">Valkosturinn <strong>Leyfa verkaskiptingu</strong> er virkur í valmyndaratriðinu fyrir farsíma.</span><span class="sxs-lookup"><span data-stu-id="b5452-330">The <strong>Allow splitting of work</strong> option is enabled on the mobile device menu item.</span></span></td>
<td><span data-ttu-id="b5452-331">Ekki tiltækt</span><span class="sxs-lookup"><span data-stu-id="b5452-331">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="b5452-332">Veljið valmyndaratriðið <strong>Fullt</strong> í vöruhúsaforritinu þegar tiltektarverk er hafið.</span><span class="sxs-lookup"><span data-stu-id="b5452-332">Select the <strong>Full</strong> menu item on the warehouse app when you process picking work.</span></span></li>
<li><span data-ttu-id="b5452-333">Í <strong>Veldu fjölda</strong> reitinn, sláðu inn hluta magns af nauðsynlegu valinu til að gefa til kynna fullan afköst.</span><span class="sxs-lookup"><span data-stu-id="b5452-333">In the <strong>Pick Qty</strong> field, enter a partial quantity of the required pick to indicate the full capacity.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="b5452-334">Í núverandi vinnu er magnið uppfært í það magn sem eftir verður sem þarf að velja.</span><span class="sxs-lookup"><span data-stu-id="b5452-334">On the current work, the quantity is updated to the remaining quantity that must be picked.</span></span></li>
<li><span data-ttu-id="b5452-335">Ný verk fyrir valið magn er búið til og lokað.</span><span class="sxs-lookup"><span data-stu-id="b5452-335">New work for the picked quantity is created and closed.</span></span></li>
</ul></td>
<td><span data-ttu-id="b5452-336">Á ekki við</span><span class="sxs-lookup"><span data-stu-id="b5452-336">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reduce-the-picked-quantity-of-completed-work-from-a-load"></a><span data-ttu-id="b5452-337">Draga úr valið magn af fullunninni vinnu (úr álagi)</span><span class="sxs-lookup"><span data-stu-id="b5452-337">Reduce the picked quantity of completed work (from a load)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b5452-338">Færibreyta lykiluppsetningar</span><span class="sxs-lookup"><span data-stu-id="b5452-338">Key setup parameter</span></span></th>
<th><span data-ttu-id="b5452-339">Runumagn er fáanlegt</span><span class="sxs-lookup"><span data-stu-id="b5452-339">Batch quantity is available</span></span></th>
<th><span data-ttu-id="b5452-340">Lykilþrep notenda</span><span class="sxs-lookup"><span data-stu-id="b5452-340">Key user steps</span></span></th>
<th><span data-ttu-id="b5452-341">Vinna vöruhúss</span><span class="sxs-lookup"><span data-stu-id="b5452-341">Warehouse work</span></span></th>
<th><span data-ttu-id="b5452-342">Pantanaskuldbundin hópapöntun</span><span class="sxs-lookup"><span data-stu-id="b5452-342">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="b5452-343">Á ekki við</span><span class="sxs-lookup"><span data-stu-id="b5452-343">Not applicable</span></span></td>
<td><span data-ttu-id="b5452-344">Já</span><span class="sxs-lookup"><span data-stu-id="b5452-344">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="b5452-345">Opnaðu <strong>Draga úr völdum magni</strong> síðu frá hleðslulínunni.</span><span class="sxs-lookup"><span data-stu-id="b5452-345">Open the <strong>Reduce picked quantity</strong> page from the load line.</span></span></li>
<li><span data-ttu-id="b5452-346">Færa skal inn fullt magn til að afturkalla tiltekt á.</span><span class="sxs-lookup"><span data-stu-id="b5452-346">Enter the full quantity to unpick.</span></span></li>
<li><span data-ttu-id="b5452-347">Veldu „færa til“ staðsetningu / kennitala.</span><span class="sxs-lookup"><span data-stu-id="b5452-347">Select a "move to" location/license plate.</span></span></li>
</ol>
</td>
<td>
<ul> 
<li><span data-ttu-id="b5452-348">Vinna sem er tengd hleðslulínunni fellur niður.</span><span class="sxs-lookup"><span data-stu-id="b5452-348">Work that is associated with the load line is canceled.</span></span></li>
<li><span data-ttu-id="b5452-349">Ný verk fyrir birgðahreyfingar er búið til og lokað.</span><span class="sxs-lookup"><span data-stu-id="b5452-349">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="b5452-350">Magnið er aftur frátekið fyrir sömu lotu.</span><span class="sxs-lookup"><span data-stu-id="b5452-350">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="b5452-351">Kerfið úthlutar af handahófi staðsetningu og kennitala (ef staðsetningin er stjórnað með skiltum) þar sem magnið er fáanlegt.</span><span class="sxs-lookup"><span data-stu-id="b5452-351">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b5452-352">Nr</span><span class="sxs-lookup"><span data-stu-id="b5452-352">No</span></span></td>
<td><span data-ttu-id="b5452-353">Sjá fyrri línuna.</span><span class="sxs-lookup"><span data-stu-id="b5452-353">See the previous row.</span></span></td>
<td><span data-ttu-id="b5452-354">Sjá fyrri línuna.</span><span class="sxs-lookup"><span data-stu-id="b5452-354">See the previous row.</span></span></td>
<td><span data-ttu-id="b5452-355">Magnið er aftur frátekið fyrir sömu framleiðslulotu og fyrir sama stað og skírteini (ef staðsetningin er stjórnað með skiltum) sem var slegið inn við upptöku.</span><span class="sxs-lookup"><span data-stu-id="b5452-355">The quantity is re-reserved for the same batch, and for the same location and license plate (if the location is license plate–controlled) that were entered during unpicking.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="move-an-item-within-a-warehouse"></a><span data-ttu-id="b5452-356">Færa vöru til innan vöruhúss</span><span class="sxs-lookup"><span data-stu-id="b5452-356">Move an item within a warehouse</span></span>

> [!NOTE]
> <span data-ttu-id="b5452-357">Þessi vörugeymsla á aðeins við um flutninga á **Vinnusköpunarferli** tegund, ekki til hreyfingar eftir sniðmáti.</span><span class="sxs-lookup"><span data-stu-id="b5452-357">This warehouse action is applicable only to movement of the **Work creation process** type, not to movement by template.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b5452-358">Færibreyta lykiluppsetningar</span><span class="sxs-lookup"><span data-stu-id="b5452-358">Key setup parameter</span></span></th>
<th><span data-ttu-id="b5452-359">Runumagn er fáanlegt</span><span class="sxs-lookup"><span data-stu-id="b5452-359">Batch quantity is available</span></span></th>
<th><span data-ttu-id="b5452-360">Lykilþrep notenda</span><span class="sxs-lookup"><span data-stu-id="b5452-360">Key user steps</span></span></th>
<th><span data-ttu-id="b5452-361">Vinna vöruhúss</span><span class="sxs-lookup"><span data-stu-id="b5452-361">Warehouse work</span></span></th>
<th><span data-ttu-id="b5452-362">Pantanaskuldbundin hópapöntun</span><span class="sxs-lookup"><span data-stu-id="b5452-362">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="b5452-363">Valkostur <strong>Leyfa flutning birgða með tilheyrandi vinnu</strong> er virkur á starfsmanninum.</span><span class="sxs-lookup"><span data-stu-id="b5452-363">The <strong>Allow movement of inventory with associated work</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="b5452-364">Já</span><span class="sxs-lookup"><span data-stu-id="b5452-364">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="b5452-365">Hefja færslu í vöruhúsaforritinu.</span><span class="sxs-lookup"><span data-stu-id="b5452-365">Start a movement on the warehouse app.</span></span></li>
<li><span data-ttu-id="b5452-366">Sláið inn staðsetningar „frá” og „til”.</span><span class="sxs-lookup"><span data-stu-id="b5452-366">Enter "from" and "to" locations.</span></span></li>
</ol></td>
<td>
<ul>
<li><span data-ttu-id="b5452-367">Í allri núverandi vinnu sem hefur áhrif á flutninginn, er staðsetningin valin uppfærð á nýja „til“ staðinn.</span><span class="sxs-lookup"><span data-stu-id="b5452-367">On all existing work that is affected by the move, the pick location is updated to the new "to" location.</span></span></li>
<li><span data-ttu-id="b5452-368">Ný verk fyrir birgðahreyfingar er búið til og lokað.</span><span class="sxs-lookup"><span data-stu-id="b5452-368">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="b5452-369">Allir núverandi fyrirvarar sem hafa áhrif á magnhreyfingu frá tilteknum stað eru aftur áskilnir fyrir sömu lotu.</span><span class="sxs-lookup"><span data-stu-id="b5452-369">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch.</span></span> <span data-ttu-id="b5452-370">Kerfið úthlutar af handahófi staðsetningu og kennitala (ef staðsetningin er stjórnað með skiltum) þar sem magnið er fáanlegt.</span><span class="sxs-lookup"><span data-stu-id="b5452-370">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b5452-371">Nr</span><span class="sxs-lookup"><span data-stu-id="b5452-371">No</span></span></td>
<td><span data-ttu-id="b5452-372">Sjá fyrri línuna.</span><span class="sxs-lookup"><span data-stu-id="b5452-372">See the previous row.</span></span></td>
<td><span data-ttu-id="b5452-373">Sjá fyrri línuna.</span><span class="sxs-lookup"><span data-stu-id="b5452-373">See the previous row.</span></span></td>
<td><span data-ttu-id="b5452-374">Allur fyrirliggjandi fyrirvari sem hefur áhrif á magnhreyfingu frá tilteknum stað er aftur áskilinn fyrir sömu framleiðslulotu og fyrir nýja „til“ staðsetningar og kennitala (ef staðsetningin er stjórnað með skiltum).</span><span class="sxs-lookup"><span data-stu-id="b5452-374">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch, and for the new "to" location and license plate (if the location is license plate–controlled).</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reverse-the-picked-quantity-of-completed-work-from-a-load-or-a-wave"></a><span data-ttu-id="b5452-375">Bakfærðu tiltekið magn af fullunninni vinnu (úr álagi eða bylgju)</span><span class="sxs-lookup"><span data-stu-id="b5452-375">Reverse the picked quantity of completed work (from a load or a wave)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b5452-376">Færibreyta lykiluppsetningar</span><span class="sxs-lookup"><span data-stu-id="b5452-376">Key setup parameter</span></span></th>
<th><span data-ttu-id="b5452-377">Runumagn er fáanlegt</span><span class="sxs-lookup"><span data-stu-id="b5452-377">Batch quantity is available</span></span></th>
<th><span data-ttu-id="b5452-378">Lykilþrep notenda</span><span class="sxs-lookup"><span data-stu-id="b5452-378">Key user steps</span></span></th>
<th><span data-ttu-id="b5452-379">Vinna vöruhúss</span><span class="sxs-lookup"><span data-stu-id="b5452-379">Warehouse work</span></span></th>
<th><span data-ttu-id="b5452-380">Pantanaskuldbundin hópapöntun</span><span class="sxs-lookup"><span data-stu-id="b5452-380">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='6'><span data-ttu-id="b5452-381">Á ekki við</span><span class="sxs-lookup"><span data-stu-id="b5452-381">Not applicable</span></span></td>
<td><span data-ttu-id="b5452-382">Já</span><span class="sxs-lookup"><span data-stu-id="b5452-382">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="b5452-383">Opnaðu <strong>Bakfæra vinnu</strong> síðu.</span><span class="sxs-lookup"><span data-stu-id="b5452-383">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="b5452-384">Veldu beiðnissíðuna <strong>Skildu hluti eftir núverandi staðsetningu</strong> kostur.</span><span class="sxs-lookup"><span data-stu-id="b5452-384">On the request page, select the <strong>Leave items at current location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="b5452-385">Öll vinna sem er tengd hleðslunni fellur niður.</span><span class="sxs-lookup"><span data-stu-id="b5452-385">All work that is associated with the load is canceled.</span></span></td>
<td><span data-ttu-id="b5452-386">Magnið er aftur frátekið fyrir sömu lotu.</span><span class="sxs-lookup"><span data-stu-id="b5452-386">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="b5452-387">Kerfið úthlutar af handahófi staðsetningu og kennitala (ef staðsetningin er stjórnað með skiltum) þar sem magnið er fáanlegt.</span><span class="sxs-lookup"><span data-stu-id="b5452-387">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b5452-388">Nr</span><span class="sxs-lookup"><span data-stu-id="b5452-388">No</span></span></td>
<td><span data-ttu-id="b5452-389">Sjá fyrri línuna.</span><span class="sxs-lookup"><span data-stu-id="b5452-389">See the previous row.</span></span></td>
<td><span data-ttu-id="b5452-390">Sjá fyrri línuna.</span><span class="sxs-lookup"><span data-stu-id="b5452-390">See the previous row.</span></span></td>
<td><span data-ttu-id="b5452-391">Magnið er frátekið fyrir sömu framleiðslulotu og fyrir staðsetningu og kennitala þar sem magnið var eftir við afturköllun.</span><span class="sxs-lookup"><span data-stu-id="b5452-391">The quantity is re-reserved for the same batch, and for the location and license plate where the quantity was left upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b5452-392">Já</span><span class="sxs-lookup"><span data-stu-id="b5452-392">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="b5452-393">Opnaðu <strong>Bakfæra vinnu</strong> síðu.</span><span class="sxs-lookup"><span data-stu-id="b5452-393">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="b5452-394">Veldu beiðnissíðuna <strong>Úthluta vörum á þessa staðsetningu</strong> kostur.</span><span class="sxs-lookup"><span data-stu-id="b5452-394">On the request page, select the <strong>Assign items to this location</strong> option.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="b5452-395">Núgildandi vinna er afturkölluð.</span><span class="sxs-lookup"><span data-stu-id="b5452-395">The current work is canceled.</span></span></li>
<li><span data-ttu-id="b5452-396">Ný verk fyrir birgðahreyfingar er búið til og lokað.</span><span class="sxs-lookup"><span data-stu-id="b5452-396">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="b5452-397">Magnið er aftur frátekið fyrir sömu lotu.</span><span class="sxs-lookup"><span data-stu-id="b5452-397">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="b5452-398">Kerfið úthlutar af handahófi staðsetningu og kennitala (ef staðsetningin er stjórnað með skiltum) þar sem magnið er fáanlegt.</span><span class="sxs-lookup"><span data-stu-id="b5452-398">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b5452-399">Nr</span><span class="sxs-lookup"><span data-stu-id="b5452-399">No</span></span></td>
<td><span data-ttu-id="b5452-400">Sjá fyrri línuna.</span><span class="sxs-lookup"><span data-stu-id="b5452-400">See the previous row.</span></span></td>
<td><span data-ttu-id="b5452-401">Sjá fyrri línuna.</span><span class="sxs-lookup"><span data-stu-id="b5452-401">See the previous row.</span></span></td>
<td><span data-ttu-id="b5452-402">Magnið er frátekið fyrir sömu framleiðslulotu og fyrir staðsetningu og kennitala þar sem magnið var úthlutað á við bakfærslu.</span><span class="sxs-lookup"><span data-stu-id="b5452-402">The quantity is re-reserved for the same batch, and for the location and license plate that the quantity was assigned to upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b5452-403">Já/nei</span><span class="sxs-lookup"><span data-stu-id="b5452-403">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="b5452-404">Opnaðu <strong>Bakfæra vinnu</strong> síðu.</span><span class="sxs-lookup"><span data-stu-id="b5452-404">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="b5452-405">Veldu beiðnissíðuna <strong>Færa vörur á þessa staðsetningu</strong> kostur.</span><span class="sxs-lookup"><span data-stu-id="b5452-405">On the request page, select the <strong>Move items to this location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="b5452-406">Bakfærsla er ekki studd.</span><span class="sxs-lookup"><span data-stu-id="b5452-406">Reversal isn't supported.</span></span></td>
<td><span data-ttu-id="b5452-407">Á ekki við</span><span class="sxs-lookup"><span data-stu-id="b5452-407">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b5452-408">Já/nei</span><span class="sxs-lookup"><span data-stu-id="b5452-408">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="b5452-409">Opnaðu <strong>Bakfæra vinnu</strong> síðu.</span><span class="sxs-lookup"><span data-stu-id="b5452-409">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="b5452-410">Veldu beiðnissíðuna <strong>Færa vörur byggt á staðsetningartilskipunum</strong> kostur.</span><span class="sxs-lookup"><span data-stu-id="b5452-410">On the request page, select the <strong>Move items based on location directives</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="b5452-411">Bakfærsla er ekki studd.</span><span class="sxs-lookup"><span data-stu-id="b5452-411">Reversal isn't supported.</span></span> </td>
<td><span data-ttu-id="b5452-412">Á ekki við</span><span class="sxs-lookup"><span data-stu-id="b5452-412">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="short-pick-a-quantity--register-the-quantity-as-physically-not-found-at-the-locationlicense-plate-while-you-perform-picking-work"></a><span data-ttu-id="b5452-413">Veldu stutt skammt - Skráðu magnið sem ekki finnast líkamlega á staðnum / leyfismerkinu meðan þú framkvæmir tínaverk</span><span class="sxs-lookup"><span data-stu-id="b5452-413">Short-pick a quantity – Register the quantity as physically not found at the location/license plate while you perform picking work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b5452-414">Færibreyta lykiluppsetningar</span><span class="sxs-lookup"><span data-stu-id="b5452-414">Key setup parameter</span></span></th>
<th><span data-ttu-id="b5452-415">Runumagn er fáanlegt</span><span class="sxs-lookup"><span data-stu-id="b5452-415">Batch quantity is available</span></span></th>
<th><span data-ttu-id="b5452-416">Lykilþrep notenda</span><span class="sxs-lookup"><span data-stu-id="b5452-416">Key user steps</span></span></th>
<th><span data-ttu-id="b5452-417">Vinna vöruhúss</span><span class="sxs-lookup"><span data-stu-id="b5452-417">Warehouse work</span></span></th>
<th><span data-ttu-id="b5452-418">Pantanaskuldbundin hópapöntun</span><span class="sxs-lookup"><span data-stu-id="b5452-418">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="b5452-419">Vinna undantekning frá <strong>Stutt val</strong> gerð er sett upp, hvar <strong>Endurúthlutun hlutar</strong> = <strong>Enginn</strong>, <strong>Stilla lager</strong> = <strong>Já</strong> og <strong>Fjarlægðu fyrirvara</strong> = <strong>Nei</strong>.</span><span class="sxs-lookup"><span data-stu-id="b5452-419">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span></td>
<td><span data-ttu-id="b5452-420">Já</span><span class="sxs-lookup"><span data-stu-id="b5452-420">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="b5452-421">Veljið <strong>Of lítil tiltekt</strong> -valmyndaratriðið í vöruhúsaforritinu þegar tiltektarverk er hafið.</span><span class="sxs-lookup"><span data-stu-id="b5452-421">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="b5452-422">Í <strong>Tiltekið magn</strong> reitinn er fært inn <strong>0</strong> (núll).</span><span class="sxs-lookup"><span data-stu-id="b5452-422">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="b5452-423">Í reitinn <strong>Ástæða</strong> slærðu inn <strong>Engin endurúthlutun</strong>.</span><span class="sxs-lookup"><span data-stu-id="b5452-423">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="b5452-424">Núverandi verk er lokað og valið magn er 0 (núll).</span><span class="sxs-lookup"><span data-stu-id="b5452-424">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="b5452-425">Birgðafærsla <strong>Telja</strong> tegund og <strong>Selt</strong> útgáfutegund er búin til til að tákna aðlögunina.</span><span class="sxs-lookup"><span data-stu-id="b5452-425">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="b5452-426">Magnið er aftur frátekið fyrir sömu lotu.</span><span class="sxs-lookup"><span data-stu-id="b5452-426">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="b5452-427">Kerfið úthlutar af handahófi staðsetningu og kennitala (ef staðsetningin er stjórnað með skiltum) þar sem magnið er fáanlegt.</span><span class="sxs-lookup"><span data-stu-id="b5452-427">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b5452-428">Nr</span><span class="sxs-lookup"><span data-stu-id="b5452-428">No</span></span></td>
<td><span data-ttu-id="b5452-429">Sjá fyrri línuna.</span><span class="sxs-lookup"><span data-stu-id="b5452-429">See the previous row.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="b5452-430">Of lítil tiltekt-aðgerðin mistekst og villu er hent.</span><span class="sxs-lookup"><span data-stu-id="b5452-430">The short-picking action fails, and an error is thrown.</span></span></li>
<li><span data-ttu-id="b5452-431">Núverandi verk er áfram opið.</span><span class="sxs-lookup"><span data-stu-id="b5452-431">The current work remains open.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="b5452-432">Á ekki við</span><span class="sxs-lookup"><span data-stu-id="b5452-432">Not applicable</span></span></td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="b5452-433">Vinna undantekning frá <strong>Stutt val</strong> gerð er sett upp, hvar <strong>Endurúthlutun hlutar</strong> = <strong>Enginn</strong>, <strong>Stilla lager</strong> = <strong>Já</strong> og <strong>Fjarlægðu fyrirvara</strong> = <strong>Já</strong>.</span><span class="sxs-lookup"><span data-stu-id="b5452-433">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span></td>
<td><span data-ttu-id="b5452-434">Já</span><span class="sxs-lookup"><span data-stu-id="b5452-434">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="b5452-435">Veljið <strong>Of lítil tiltekt</strong> -valmyndaratriðið í vöruhúsaforritinu þegar tiltektarverk er hafið.</span><span class="sxs-lookup"><span data-stu-id="b5452-435">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="b5452-436">Í <strong>Tiltekið magn</strong> reitinn er fært inn <strong>0</strong> (núll).</span><span class="sxs-lookup"><span data-stu-id="b5452-436">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="b5452-437">Í reitinn <strong>Ástæða</strong> slærðu inn <strong>Engin endurúthlutun</strong>.</span><span class="sxs-lookup"><span data-stu-id="b5452-437">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="b5452-438">Núverandi verk er lokað og valið magn er 0 (núll).</span><span class="sxs-lookup"><span data-stu-id="b5452-438">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="b5452-439">Birgðafærsla <strong>Telja</strong> tegund og <strong>Selt</strong> útgáfutegund er búin til til að tákna aðlögunina.</span><span class="sxs-lookup"><span data-stu-id="b5452-439">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="b5452-440">Allar núverandi frátektir sem hafa áhrif á magnleiðréttingu á staðsetningu þar sem tiltekt er of lítil eru endurfráteknar fyrir sömu lotu.</span><span class="sxs-lookup"><span data-stu-id="b5452-440">All existing reservations that are affected by the quantity adjustment in the short-picked location are re-reserved for the same batch.</span></span> <span data-ttu-id="b5452-441">Kerfið úthlutar af handahófi staðsetningu og kennitala (ef staðsetningin er stjórnað með skiltum) þar sem magnið er fáanlegt.</span><span class="sxs-lookup"><span data-stu-id="b5452-441">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b5452-442">Nr</span><span class="sxs-lookup"><span data-stu-id="b5452-442">No</span></span></td>
<td><span data-ttu-id="b5452-443">Sjá fyrri línuna.</span><span class="sxs-lookup"><span data-stu-id="b5452-443">See the previous row.</span></span></td>
<td><span data-ttu-id="b5452-444">Sjá fyrri línuna.</span><span class="sxs-lookup"><span data-stu-id="b5452-444">See the previous row.</span></span></td>
<td><span data-ttu-id="b5452-445">Allar núverandi frátektir sem hafa áhrif á magnleiðréttingu á staðsetningu þar sem tiltekt er of lítil eru fjarlægðar.</span><span class="sxs-lookup"><span data-stu-id="b5452-445">All existing reservations that are affected by the quantity adjustment in the short-picked location are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b5452-446">Vinna undantekning frá <strong>Stutt val</strong> gerð er sett upp, hvar <strong>Endurúthlutun hlutar</strong> = <strong>Handvirkt</strong>, <strong>Stilla lager</strong> = <strong>Já</strong> og <strong>Fjarlægðu fyrirvara</strong> = <strong>Nei/Já</strong>.</span><span class="sxs-lookup"><span data-stu-id="b5452-446">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No/Yes</strong>.</span></span> <span data-ttu-id="b5452-447">Að auki, er <strong>Leyfa endurúthlutun handvirkra atriða</strong> valkostur virkur á starfsmanninum.</span><span class="sxs-lookup"><span data-stu-id="b5452-447">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="b5452-448">Já</span><span class="sxs-lookup"><span data-stu-id="b5452-448">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="b5452-449">Veljið <strong>Of lítil tiltekt</strong> -valmyndaratriðið í vöruhúsaforritinu þegar tiltektarverk er hafið.</span><span class="sxs-lookup"><span data-stu-id="b5452-449">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="b5452-450">Í <strong>Magn með of litla tiltekt</strong> reitinn er fært inn <strong>0</strong> (núll).</span><span class="sxs-lookup"><span data-stu-id="b5452-450">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="b5452-451">Í <strong>Ástæða</strong> reit, veldu <strong>Stuttur velja með handvirkri úthlutun</strong>.</span><span class="sxs-lookup"><span data-stu-id="b5452-451">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="b5452-452">Veldu staðsetningu / kennitala á listanum.</span><span class="sxs-lookup"><span data-stu-id="b5452-452">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="b5452-453">Eftirfarandi aðgerðir eiga sér stað í núverandi vinnu:</span><span class="sxs-lookup"><span data-stu-id="b5452-453">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="b5452-454">Tínslulínan er lokuð og valið magn er 0 (núll).</span><span class="sxs-lookup"><span data-stu-id="b5452-454">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="b5452-455">Hætt er við að söluréttarlínuna.</span><span class="sxs-lookup"><span data-stu-id="b5452-455">The put line is canceled.</span></span></li>
<li><span data-ttu-id="b5452-456">Ný tiltektarlína er búin til.</span><span class="sxs-lookup"><span data-stu-id="b5452-456">A new pick line is created.</span></span> <span data-ttu-id="b5452-457">Það notar staðsetningu / númeraplötu sem notandinn valdi.</span><span class="sxs-lookup"><span data-stu-id="b5452-457">It uses the location/license plate that the user selected.</span></span></li>
<li><span data-ttu-id="b5452-458">Ný söluréttarlína er búin til.</span><span class="sxs-lookup"><span data-stu-id="b5452-458">A new put line is created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="b5452-459">Birgðafærsla <strong>Telja</strong> tegund og <strong>Selt</strong> útgáfutegund er búin til til að tákna aðlögunina.</span><span class="sxs-lookup"><span data-stu-id="b5452-459">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="b5452-460">Á ekki við</span><span class="sxs-lookup"><span data-stu-id="b5452-460">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b5452-461">Vinnuundantekning frá <strong>Stutt val</strong> gerð er sett upp, hvar <strong>Endurúthlutun hlutar</strong> = <strong>Handvirkt</strong>, <strong>Stilla lager</strong> = <strong>Já</strong> og <strong>Fjarlægðu fyrirvara</strong> = <strong>Nei</strong>.</span><span class="sxs-lookup"><span data-stu-id="b5452-461">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span> <span data-ttu-id="b5452-462">Að auki, er <strong>Leyfa endurúthlutun handvirkra atriða</strong> valkostur virkur á starfsmanninum.</span><span class="sxs-lookup"><span data-stu-id="b5452-462">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="b5452-463">Ekkert</span><span class="sxs-lookup"><span data-stu-id="b5452-463">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="b5452-464">Veljið <strong>Of lítil tiltekt</strong> -valmyndaratriðið í vöruhúsaforritinu þegar tiltektarverk er hafið.</span><span class="sxs-lookup"><span data-stu-id="b5452-464">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="b5452-465">Í <strong>Magn með of litla tiltekt</strong> reitinn er fært inn <strong>0</strong> (núll).</span><span class="sxs-lookup"><span data-stu-id="b5452-465">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="b5452-466">Í <strong>Ástæða</strong> reit, veldu <strong>Stuttur velja með handvirkri úthlutun</strong>.</span><span class="sxs-lookup"><span data-stu-id="b5452-466">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="b5452-467">Of lítil tiltekt-aðgerðin mistekst og villu er hent.</span><span class="sxs-lookup"><span data-stu-id="b5452-467">The short-picking action fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="b5452-468">Á ekki við</span><span class="sxs-lookup"><span data-stu-id="b5452-468">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b5452-469">Vinnuundantekning frá <strong>Stutt val</strong> gerð er sett upp, hvar <strong>Endurúthlutun hlutar</strong> = <strong>Handvirkt</strong>, <strong>Stilla lager</strong> = <strong>Já</strong> og <strong>Fjarlægðu fyrirvara</strong> = <strong>Já</strong>.</span><span class="sxs-lookup"><span data-stu-id="b5452-469">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span> <span data-ttu-id="b5452-470">Að auki, er <strong>Leyfa endurúthlutun handvirkra atriða</strong> valkostur virkur á starfsmanninum.</span><span class="sxs-lookup"><span data-stu-id="b5452-470">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="b5452-471">Ekkert</span><span class="sxs-lookup"><span data-stu-id="b5452-471">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="b5452-472">Veljið <strong>Of lítil tiltekt</strong> -valmyndaratriðið í vöruhúsaforritinu þegar tiltektarverk er hafið.</span><span class="sxs-lookup"><span data-stu-id="b5452-472">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="b5452-473">Í <strong>Magn með of litla tiltekt</strong> reitinn er fært inn <strong>0</strong> (núll).</span><span class="sxs-lookup"><span data-stu-id="b5452-473">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="b5452-474">Í <strong>Ástæða</strong> reit, veldu <strong>Stuttur velja með handvirkri úthlutun</strong>.</span><span class="sxs-lookup"><span data-stu-id="b5452-474">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="b5452-475">Veldu staðsetningu / kennitala á listanum.</span><span class="sxs-lookup"><span data-stu-id="b5452-475">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="b5452-476">Eftirfarandi aðgerðir eiga sér stað í núverandi vinnu:</span><span class="sxs-lookup"><span data-stu-id="b5452-476">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="b5452-477">Tínslulínan er lokuð og valið magn er 0 (núll).</span><span class="sxs-lookup"><span data-stu-id="b5452-477">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="b5452-478">Hætt er við að söluréttarlínuna.</span><span class="sxs-lookup"><span data-stu-id="b5452-478">The put line is canceled.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="b5452-479">Birgðafærsla <strong>Telja</strong> tegund og <strong>Selt</strong> útgáfutegund er búin til til að tákna aðlögunina.</span><span class="sxs-lookup"><span data-stu-id="b5452-479">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="b5452-480">Allar núverandi frátektir sem hafa áhrif á magnleiðréttingu á staðsetningu þar sem tiltekt er of lítil/númeraplötu eru fjarlægðar.</span><span class="sxs-lookup"><span data-stu-id="b5452-480">All existing reservations that are affected by the quantity adjustment in the short-picked location/license plate are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b5452-481">Vinnuundantekning frá <strong>Stutt val</strong> gerð er sett upp, hvar <strong>Endurúthlutun hlutar</strong> = <strong>Sjálfvirkt</strong>, <strong>Stilla lager</strong> = <strong>Já/Nei</strong> og <strong>Fjarlægðu fyrirvara</strong> = <strong>Já/Nei</strong>.</span><span class="sxs-lookup"><span data-stu-id="b5452-481">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Automatic</strong>, <strong>Adjust inventory</strong> = <strong>Yes/No</strong>, and <strong>Remove reservations</strong> = <strong>Yes/No</strong>.</span></span></td>
<td><span data-ttu-id="b5452-482">Ekki tiltækt</span><span class="sxs-lookup"><span data-stu-id="b5452-482">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="b5452-483">Veljið <strong>Of lítil tiltekt</strong> -valmyndaratriðið í vöruhúsaforritinu þegar tiltektarverk er hafið.</span><span class="sxs-lookup"><span data-stu-id="b5452-483">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="b5452-484">Í <strong>Magn með of litla tiltekt</strong> reitinn er fært inn <strong>0</strong> (núll).</span><span class="sxs-lookup"><span data-stu-id="b5452-484">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="b5452-485">Í <strong>Ástæða</strong> reit, veldu <strong>Stuttur velja með sjálfvirkri endurúthlutun</strong>.</span><span class="sxs-lookup"><span data-stu-id="b5452-485">In the <strong>Reason</strong> field, select <strong>Short Picking with automatic reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="b5452-486">Ekki er stutt í skammval sem felur í sér sjálfvirka endurúthlutun.</span><span class="sxs-lookup"><span data-stu-id="b5452-486">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
<td><span data-ttu-id="b5452-487">Ekki er stutt í skammval sem felur í sér sjálfvirka endurúthlutun.</span><span class="sxs-lookup"><span data-stu-id="b5452-487">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="change-the-inventory-status"></a><span data-ttu-id="b5452-488">Breyta á birgðastöðunni</span><span class="sxs-lookup"><span data-stu-id="b5452-488">Change the inventory status</span></span>

> [!NOTE]
> <span data-ttu-id="b5452-489">Þessa vörugeymsluaðgerð er hægt að framkvæma frá mörgum inngangspunktum.</span><span class="sxs-lookup"><span data-stu-id="b5452-489">This warehouse action can be performed from multiple entry points.</span></span> <span data-ttu-id="b5452-490">Dæmið sem sýnt er hér notar **Breyting á birgðum** aðgerð á **Á lager eftir birgðageymslu** síðu.</span><span class="sxs-lookup"><span data-stu-id="b5452-490">The example that is shown here uses **Inventory status change** action on the **On-hand by location** page.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b5452-491">Færibreyta lykiluppsetningar</span><span class="sxs-lookup"><span data-stu-id="b5452-491">Key setup parameter</span></span></th>
<th><span data-ttu-id="b5452-492">Runumagn er fáanlegt</span><span class="sxs-lookup"><span data-stu-id="b5452-492">Batch quantity is available</span></span></th>
<th><span data-ttu-id="b5452-493">Lykilþrep notenda</span><span class="sxs-lookup"><span data-stu-id="b5452-493">Key user steps</span></span></th>
<th><span data-ttu-id="b5452-494">Vinna vöruhúss</span><span class="sxs-lookup"><span data-stu-id="b5452-494">Warehouse work</span></span></th>
<th><span data-ttu-id="b5452-495">Pantanaskuldbundin hópapöntun</span><span class="sxs-lookup"><span data-stu-id="b5452-495">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="b5452-496">Á <strong>Vöruhús</strong> flipanum, í <strong>Vöruhús</strong> skrá, er <strong>Fjarlægja frátektir og merkingar</strong> reiturinn stilltur á <strong>Frátektir</strong> eða <strong>Merkingar og fyrirvarar</strong>.</span><span class="sxs-lookup"><span data-stu-id="b5452-496">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>Reservations</strong> or <strong>Markings and reservations</strong>.</span></span></td>
<td><span data-ttu-id="b5452-497">Já</span><span class="sxs-lookup"><span data-stu-id="b5452-497">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="b5452-498">Veldu tiltekna staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="b5452-498">Select a specific location.</span></span></li>
<li><span data-ttu-id="b5452-499">Veldu línu sem er með tiltekinn hlut, staðsetningu og númeraplötu (ef staðsetningin er stjórnað með skiltum).</span><span class="sxs-lookup"><span data-stu-id="b5452-499">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="b5452-500">Veldu <strong>Breyting á birgðastöðu</strong>.</span><span class="sxs-lookup"><span data-stu-id="b5452-500">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="b5452-501">Stilltu reitinn <strong>Staða birgða</strong> til <strong>Lokun</strong>.</span><span class="sxs-lookup"><span data-stu-id="b5452-501">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="b5452-502">Breytingar á birgðastöðu eru ekki leyfðar fyrir magn sem er frátekið fyrir vinnu.</span><span class="sxs-lookup"><span data-stu-id="b5452-502">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="b5452-503">Magnið er aftur frátekið fyrir sömu lotu.</span><span class="sxs-lookup"><span data-stu-id="b5452-503">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="b5452-504">Kerfið úthlutar af handahófi staðsetningu og kennitala (ef staðsetningin er stjórnað með skiltum) þar sem magnið er fáanlegt.</span><span class="sxs-lookup"><span data-stu-id="b5452-504">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></li>
<li><span data-ttu-id="b5452-505">Tvö birgðafærslur <strong>Breyting á birgðum</strong> gerð eru búin til til að tákna breytinguna á stöðu birgða.</span><span class="sxs-lookup"><span data-stu-id="b5452-505">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="b5452-506">Birgðafærsla af gerðinni <strong>Stöðvun birgða</strong> og gerð útreyfingar <strong>Frátekið á lager</strong> er búin til til að tákna fyrirvara á lokað magn.</span><span class="sxs-lookup"><span data-stu-id="b5452-506">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="b5452-507">Nr</span><span class="sxs-lookup"><span data-stu-id="b5452-507">No</span></span></td>
<td><span data-ttu-id="b5452-508">Sjá fyrri línuna.</span><span class="sxs-lookup"><span data-stu-id="b5452-508">See the previous row.</span></span></td>
<td><span data-ttu-id="b5452-509">Breytingar á birgðastöðu eru ekki leyfðar fyrir magn sem er frátekið fyrir vinnu.</span><span class="sxs-lookup"><span data-stu-id="b5452-509">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="b5452-510">Pöntunin er fjarlægð.</span><span class="sxs-lookup"><span data-stu-id="b5452-510">The reservation is removed.</span></span></li>
<li><span data-ttu-id="b5452-511">Tvö birgðafærslur <strong>Breyting á birgðum</strong> gerð eru búin til til að tákna breytinguna á stöðu birgða.</span><span class="sxs-lookup"><span data-stu-id="b5452-511">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="b5452-512">Birgðafærsla af gerðinni <strong>Stöðvun birgða</strong> og gerð útreyfingar <strong>Frátekið á lager</strong> er búin til til að tákna fyrirvara á lokað magn.</span><span class="sxs-lookup"><span data-stu-id="b5452-512">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="b5452-513">Á flipanum <strong>Vöruhús</strong>, í skránni <strong>Vöruhús</strong>, er reiturinn <strong>Fjarlægja frátektir og merkingar</strong> stilltur á <strong>Ekkert</strong>.</span><span class="sxs-lookup"><span data-stu-id="b5452-513">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>None</strong>.</span></span></td>
<td><span data-ttu-id="b5452-514">Já</span><span class="sxs-lookup"><span data-stu-id="b5452-514">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="b5452-515">Veldu tiltekna staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="b5452-515">Select a specific location.</span></span></li>
<li><span data-ttu-id="b5452-516">Veldu línu sem er með tiltekinn hlut, staðsetningu og númeraplötu (ef staðsetningin er stjórnað með skiltum).</span><span class="sxs-lookup"><span data-stu-id="b5452-516">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="b5452-517">Veldu <strong>Breyting á birgðastöðu</strong>.</span><span class="sxs-lookup"><span data-stu-id="b5452-517">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="b5452-518">Stilltu reitinn <strong>Staða birgða</strong> til <strong>Lokun</strong>.</span><span class="sxs-lookup"><span data-stu-id="b5452-518">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="b5452-519">Breytingar á birgðastöðu eru ekki leyfðar fyrir magn sem er frátekið fyrir vinnu.</span><span class="sxs-lookup"><span data-stu-id="b5452-519">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="b5452-520">Magnið er aftur frátekið fyrir sömu lotu.</span><span class="sxs-lookup"><span data-stu-id="b5452-520">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="b5452-521">Kerfið úthlutar af handahófi staðsetningu og kennitala (ef staðsetningin er stjórnað með skiltum) þar sem magnið er fáanlegt.</span><span class="sxs-lookup"><span data-stu-id="b5452-521">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b5452-522">Nr</span><span class="sxs-lookup"><span data-stu-id="b5452-522">No</span></span></td>
<td><span data-ttu-id="b5452-523">Sjá fyrri línuna.</span><span class="sxs-lookup"><span data-stu-id="b5452-523">See the previous row.</span></span></td>
<td><span data-ttu-id="b5452-524">Breytingar á birgðastöðu eru ekki leyfðar fyrir magn sem er frátekið fyrir vinnu.</span><span class="sxs-lookup"><span data-stu-id="b5452-524">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="b5452-525">Breytingar á birgðastöðu eru ekki leyfðar.</span><span class="sxs-lookup"><span data-stu-id="b5452-525">Inventory status changes aren't allowed.</span></span></td>
</tr>
</tbody>
</table>

## <a name="limitations"></a><span data-ttu-id="b5452-526">Takmarkanir</span><span class="sxs-lookup"><span data-stu-id="b5452-526">Limitations</span></span>

- <span data-ttu-id="b5452-527">Sveigjanleiki vörugeymsluvíddar pöntunaraðgerða styður ekki eftirfarandi eiginleika:</span><span class="sxs-lookup"><span data-stu-id="b5452-527">The flexible warehouse-level dimension reservation functionality doesn't support the following features:</span></span>

    - <span data-ttu-id="b5452-528">Stjórnun framleiðsluþyngdar</span><span class="sxs-lookup"><span data-stu-id="b5452-528">Catch weight management</span></span>
    - <span data-ttu-id="b5452-529">Efnislega neikvæð birgðastaða</span><span class="sxs-lookup"><span data-stu-id="b5452-529">Physical negative inventory</span></span>
    - <span data-ttu-id="b5452-530">Frátekt gegn pöntuðu framboði</span><span class="sxs-lookup"><span data-stu-id="b5452-530">Reservation against ordered supply</span></span>
    - <span data-ttu-id="b5452-531">Flytja pantanir og hráefni tína</span><span class="sxs-lookup"><span data-stu-id="b5452-531">Transfer orders and raw material picking</span></span>

- <span data-ttu-id="b5452-532">Reglugerð um gámasamstæðu fyrir pökkun með tilskipunareiningunni hefur takmarkanir.</span><span class="sxs-lookup"><span data-stu-id="b5452-532">The container consolidation rule for packing by directive unit has limitations.</span></span> <span data-ttu-id="b5452-533">Fyrir pöntunarbundna fyrirvara mælum við með að þú notir ekki sniðmát fyrir gámagerð þar sem **Pakkning eftir tilskipunareining** reiturinn er virkur.</span><span class="sxs-lookup"><span data-stu-id="b5452-533">For order-committed reservations, we recommend that you not use container build templates where the **Pack by directive unit** field is enabled.</span></span> <span data-ttu-id="b5452-534">Í núverandi hönnun eru staðsetningartilskipanir ekki notaðar þegar vörugeymsla er búin til.</span><span class="sxs-lookup"><span data-stu-id="b5452-534">In the current design, location directives aren't used when warehouse work is created.</span></span> <span data-ttu-id="b5452-535">Þess vegna er aðeins lægsta einingin í einingaröðarhópnum (birgðaeiningin) beitt á gámabylgjuskrefinu.</span><span class="sxs-lookup"><span data-stu-id="b5452-535">Therefore, only the lowest unit in the unit sequence group (the inventory unit) is applied during the containerization wave step.</span></span>
