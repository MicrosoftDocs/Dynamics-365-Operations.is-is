---
title: Flytja inn ASN á innleið í gegnum V2 gagnaeininguna
description: Þetta efnisatriði útskýrir hvernig á að stýra innflutningi á ítarlegum tilkynningum á sendingum á innleið (ASN) gegnum gagnaeininguna ASN á innleið V2.
author: GalynaFedorova
ms.date: 05/31/2021
ms.topic: article
ms.search.form: WHSInboundASNV2Entity, WHSInboundASNEntity
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-04
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 470cc0c39f211a5d0f106c4c6e193867388e2b53
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249117"
---
# <a name="import-inbound-asns-through-the-v2-data-entity"></a><span data-ttu-id="aeb33-103">Flytja inn ASN á innleið í gegnum V2 gagnaeininguna</span><span class="sxs-lookup"><span data-stu-id="aeb33-103">Import inbound ASNs through the V2 data entity</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="aeb33-104">Ítarlegar sendingartilkynningar (ASN) láta þig vita um afhendingar lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="aeb33-104">Advanced shipping notices (ASNs) notify you about vendor deliveries.</span></span> <span data-ttu-id="aeb33-105">Þær hjálpa sendanda að lýsa efni sendingar og viðbótarupplýsingum um hana, svo sem vörum og umbúðum.</span><span class="sxs-lookup"><span data-stu-id="aeb33-105">They help the sender describe the contents of a shipment and additional information about it, such as the items and packaging.</span></span>

<span data-ttu-id="aeb33-106">ASNs getur hjálpað starfsmönnum vöruhúss að komast að því hvað er á leiðinni og hvenær.</span><span class="sxs-lookup"><span data-stu-id="aeb33-106">ASNs can help warehouse workers learn what is arriving when.</span></span> <span data-ttu-id="aeb33-107">Því geta þeir undirbúið sig.</span><span class="sxs-lookup"><span data-stu-id="aeb33-107">Therefore, they can prepare.</span></span> <span data-ttu-id="aeb33-108">Auk þess geta vöruhúsastarfsmenn notað ASN til að bera saman upplýsingar um sendingu við tengda innkaupapöntun sem áður var stofnuð.</span><span class="sxs-lookup"><span data-stu-id="aeb33-108">In addition, warehouse workers can use ASNs to match the details of a shipment to the related purchase order that was previously created.</span></span>

<span data-ttu-id="aeb33-109">Þetta efnisatriði kemur með ýmsar atburðarási sem sýna, með dæmum, hvernig á að vinna með ASN-skrár.</span><span class="sxs-lookup"><span data-stu-id="aeb33-109">This topic presents a collection of scenarios that show, through examples, how to work with ASN files.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="aeb33-110">Innflutningur *ASN á innleið* á aðeins við um vörur sem eru virkjaðar fyrir ítarlegt vöruhúsakerfi.</span><span class="sxs-lookup"><span data-stu-id="aeb33-110">*Inbound ASN* import applies only to items that are enabled for advanced warehouse management (WMS).</span></span> <span data-ttu-id="aeb33-111">Áður en þú móttekur ASN verður innkaupapöntun að vera skráð í kerfið gagnvart lánardrottninum sem sendir ASN.</span><span class="sxs-lookup"><span data-stu-id="aeb33-111">Before you receive an ASN, a purchase order must be registered in the system against the vendor who is sending that ASN.</span></span>

## <a name="inbound-asn-v2-entity"></a><span data-ttu-id="aeb33-112">Eining ASN á innleið V2</span><span class="sxs-lookup"><span data-stu-id="aeb33-112">Inbound ASN V2 entity</span></span>

<span data-ttu-id="aeb33-113">Þú flytur inn ASN á innleið með því að nota samsettu gagnaeininguna *ASN á innleið V2*.</span><span class="sxs-lookup"><span data-stu-id="aeb33-113">You import inbound ASNs by using the *Inbound ASN V2* composite data entity.</span></span> <span data-ttu-id="aeb33-114">*ASN á innleið V2* nýtir sér eftirfarandi einingar:</span><span class="sxs-lookup"><span data-stu-id="aeb33-114">*Inbound ASN V2* takes advantage of the following entities:</span></span>

- <span data-ttu-id="aeb33-115">Haus farms á innleið</span><span class="sxs-lookup"><span data-stu-id="aeb33-115">Inbound load header</span></span>
- <span data-ttu-id="aeb33-116">Haus sendingar á innleið</span><span class="sxs-lookup"><span data-stu-id="aeb33-116">Inbound shipment header</span></span>
- <span data-ttu-id="aeb33-117">Pakkaskipan farms á innleið</span><span class="sxs-lookup"><span data-stu-id="aeb33-117">Inbound load packing structures</span></span>
- <span data-ttu-id="aeb33-118">Kassar pakkaskipana farms á innleið</span><span class="sxs-lookup"><span data-stu-id="aeb33-118">Inbound load packing structure cases</span></span>
- <span data-ttu-id="aeb33-119">Kassalínur pakkaskipanar farms á innleið</span><span class="sxs-lookup"><span data-stu-id="aeb33-119">Inbound load packing structure case lines</span></span>
- <span data-ttu-id="aeb33-120">Pakkaskipunarlínur farms á innleið</span><span class="sxs-lookup"><span data-stu-id="aeb33-120">Inbound load packing structure lines</span></span>

<span data-ttu-id="aeb33-121">Samsetta gagnaeiningin *ASN á innleið V2* er ætluð fyrir aðstæður ósamstilltrar samþættingar þar sem innflutningur á XML-skrá er notaður.</span><span class="sxs-lookup"><span data-stu-id="aeb33-121">The *Inbound ASN V2* composite data entity is intended for asynchronous integration scenarios where XML file–based imports are used.</span></span>

## <a name="xml-format-for-importing-asns"></a><span data-ttu-id="aeb33-122">XML-snið til að flytja inn ASN</span><span class="sxs-lookup"><span data-stu-id="aeb33-122">XML format for importing ASNs</span></span>

<span data-ttu-id="aeb33-123">Microsoft Dynamics 365 Supply Chain Management styður eftirfarandi XML-snið til að flytja inn ASN.</span><span class="sxs-lookup"><span data-stu-id="aeb33-123">Microsoft Dynamics 365 Supply Chain Management supports the following XML format for importing ASNs.</span></span> <span data-ttu-id="aeb33-124">Hver hnútur í XML-skránni táknar eigind frá stakri einingu.</span><span class="sxs-lookup"><span data-stu-id="aeb33-124">Each node in the XML file represents an attribute from an individual entity.</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity>
        <WHSInboundShipmentHeaderEntity>
            <WHSInboundLoadPackingStructureEntity>
                <WHSInboundLoadPackingStructureCaseEntity>
                    <WHSInboundPackingStructureCaseLineV2Entity>
                    </WHSInboundPackingStructureCaseLineV2Entity>
                </WHSInboundLoadPackingStructureCaseEntity>
                <WHSInboundLoadPackingStructureLineV2Entity>
                </WHSInboundLoadPackingStructureLineV2Entity>
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

## <a name="examples"></a><span data-ttu-id="aeb33-125">Dæmi</span><span class="sxs-lookup"><span data-stu-id="aeb33-125">Examples</span></span>

<span data-ttu-id="aeb33-126">Í eftirfarandi undirhlutum eru dæmi um XML-innflutningsskrár ASN fyrir sendingar lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="aeb33-126">The following subsections provide examples of ASN XML import files for vendor shipments.</span></span>

### <a name="example-1"></a><span data-ttu-id="aeb33-127">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="aeb33-127">Example 1</span></span>

<span data-ttu-id="aeb33-128">Eftirfarandi dæmi sýnir XML-skrá til að flytja inn sendingar lánardrottins fyrir eina innkaupapöntun þegar engar upplýsingar um mál eru innifaldar.</span><span class="sxs-lookup"><span data-stu-id="aeb33-128">The following example shows an XML file for importing vendor shipments for one purchase order when no case details are included.</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity TRACTORNUMBER="0000101">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_01" VENDORADDRESSCOUNTRYREGIONID = "USA" VENDORADDRESSSTREET = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000176" ITEMNUMBER="A0001" QUANTITY="1" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

### <a name="example-2"></a><span data-ttu-id="aeb33-129">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="aeb33-129">Example 2</span></span>

<span data-ttu-id="aeb33-130">Eftirfarandi dæmi sýnir XML-skrá til að flytja inn sendingar lánardrottins fyrir eina innkaupapöntun þegar upplýsingar um mál eru innifaldar.</span><span class="sxs-lookup"><span data-stu-id="aeb33-130">The following example shows an XML file for importing vendor shipments for one purchase order when case details are included.</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity ESTIMATEDARRIVALDATETIME="2021-04-25T11:00:00+00:00">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="MVR_SNN_0004">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="MVR_SNN_0004" PACKEDTOTALQUANTITY="2.00">
                <WHSInboundLoadPackingStructureCaseEntity PARENTPACKINGSTRUCTURELICENSEPLATENUMBER="MVR_SNN_0004" LICENSEPLATENUMBER="MVR_SNN_0004A" PACKEDTOTALQUANTITY="2.00" />
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000175" ITEMNUMBER="A0001" PURCHASEORDERLINENUMBER="1" QUANTITY="2.00" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

### <a name="example-3"></a><span data-ttu-id="aeb33-131">Dæmi 3</span><span class="sxs-lookup"><span data-stu-id="aeb33-131">Example 3</span></span>

<span data-ttu-id="aeb33-132">Eftirfarandi dæmi sýnir XML-skrá til að flytja inn sendingar lánardrottins fyrir margar innkaupapantanir þegar upplýsingar um mál eru innifaldar.</span><span class="sxs-lookup"><span data-stu-id="aeb33-132">The following example shows an XML file for importing vendor shipments for multiple purchase orders when case details are included.</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity TRACTORNUMBER="0000101">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_01" VENDORADDRESSCOUNTRYREGIONID = "USA" VendorAddressStreet = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000176" ITEMNUMBER="A0001" QUANTITY="100" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_02" VENDORADDRESSCOUNTRYREGIONID = "USA" VendorAddressStreet = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="A0001" QUANTITY="200" UNITSYMBOL="ea" />
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="P0004" QUANTITY="300" UNITSYMBOL="ea" ITEMBATCHNUMBER="BN0001" />
            </WHSInboundLoadPackingStructureEntity>
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_002">
                <WHSInboundLoadPackingStructureCaseEntity LICENSEPLATENUMBER="LP_ASN_002_C01">
                    <WHSInboundLoadPackingStructureCaseLineV2Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="A0001" QUANTITY="400" UNITSYMBOL="ea" />
                </WHSInboundLoadPackingStructureCaseEntity>
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

## <a name="inspect-the-results-of-importing-an-asn-file"></a><span data-ttu-id="aeb33-133">Skoða niðurstöður innflutnings ASN-skráar</span><span class="sxs-lookup"><span data-stu-id="aeb33-133">Inspect the results of importing an ASN file</span></span>

<span data-ttu-id="aeb33-134">Fylgið þessum skrefum til að skoða niðurstöður innflutnings ASN-skráar.</span><span class="sxs-lookup"><span data-stu-id="aeb33-134">Follow these steps to inspect the results of importing an ASN file.</span></span>

1. <span data-ttu-id="aeb33-135">Farðu í **Vöruhúsakerfi \> Hleðslur \> Allar hleðslur**.</span><span class="sxs-lookup"><span data-stu-id="aeb33-135">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="aeb33-136">Finnið og opnið hleðslu sem var búin til sem hluti af ASN-innflutningi.</span><span class="sxs-lookup"><span data-stu-id="aeb33-136">Find and open a load that was created as part of an ASN import.</span></span>
1. <span data-ttu-id="aeb33-137">Í flýtiflipanum **Hleðsla** ættir þú að sjá gildi sem byggjast á XML-skránni.</span><span class="sxs-lookup"><span data-stu-id="aeb33-137">On the **Load** FastTab, you should see values that are based on the XML file.</span></span>
1. <span data-ttu-id="aeb33-138">Í flýtiflipanum **Hleðslulínur** ættirðu að sjá innkaupapöntunarnúmer og upplýsingar um vöru sem byggjast á XML-skránni.</span><span class="sxs-lookup"><span data-stu-id="aeb33-138">On the **Load lines** FastTab, you should see purchase order numbers and item details that are based on the XML file.</span></span>
1. <span data-ttu-id="aeb33-139">Á aðgerðasvæðinu, í flipanum **Senda og móttaka**, í hópnum **Móttaka**, skal velja **Pökkunarskipulag** til að yfirfara pökkunarskipulag hleðslunnar.</span><span class="sxs-lookup"><span data-stu-id="aeb33-139">On the Action Pane, on the **Ship and receive** tab, in the **Receive** group, select **Packing structure** to review the packing structure of the load.</span></span>
1. <span data-ttu-id="aeb33-140">Í flýtiflipanum **Vörubretti** ættir þú að sjá númeraplötur sem byggjast á XML-skránni.</span><span class="sxs-lookup"><span data-stu-id="aeb33-140">On the **Pallets** FastTab, you should see license plates that are based on the XML file.</span></span>
1. <span data-ttu-id="aeb33-141">Í flýtiflipanum **Kassar** ættir þú að sjá kassa sem byggjast á XML-skránni.</span><span class="sxs-lookup"><span data-stu-id="aeb33-141">On the **Cases** FastTab, you should see cases that are based on the XML file.</span></span>
1. <span data-ttu-id="aeb33-142">Í flýtiflipanum **Vörur** ættir þú að sjá vörur og magn sem byggist á XML-skránni.</span><span class="sxs-lookup"><span data-stu-id="aeb33-142">On the **Items** FastTab, you should see items and quantities that are based on the XML file.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
