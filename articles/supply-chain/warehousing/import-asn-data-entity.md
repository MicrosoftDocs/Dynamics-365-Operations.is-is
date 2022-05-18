---
title: Flyttu inn ASN-númer á heimleið í gegnum V3 gagnaeininguna
description: Þetta efnisatriði útskýrir hvernig á að stjórna innflutningi á háþróaða sendingartilkynningum á heimleið (ASN) í gegnum ASN gagnaeininguna á heimleið.
author: GalynaFedorova
ms.date: 05/11/2022
ms.topic: article
ms.search.form: WHSInboundASNV3Entity, WHSInboundASNEntity, DMFEntity
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2021-06-04
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 44ec0230236451a413d483b3e9f3ddc58b49a0b0
ms.sourcegitcommit: 90ffd763d18f97654b9dbc9e3f71c998e6094c6b
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2022
ms.locfileid: "8740056"
---
# <a name="import-inbound-asns-through-the-v3-data-entity"></a>Flyttu inn ASN-númer á heimleið í gegnum V3 gagnaeininguna

[!include [banner](../../includes/banner.md)]

Ítarlegar sendingartilkynningar (ASN) láta þig vita um afhendingar lánardrottna. Þær hjálpa sendanda að lýsa efni sendingar og viðbótarupplýsingum um hana, svo sem vörum og umbúðum.

ASNs getur hjálpað starfsmönnum vöruhúss að komast að því hvað er á leiðinni og hvenær. Því geta þeir undirbúið sig. Auk þess geta vöruhúsastarfsmenn notað ASN til að bera saman upplýsingar um sendingu við tengda innkaupapöntun sem áður var stofnuð.

Þetta efnisatriði kemur með ýmsar atburðarási sem sýna, með dæmum, hvernig á að vinna með ASN-skrár.

> [!IMPORTANT]
> Innflutningur *ASN á innleið* á aðeins við um vörur sem eru virkjaðar fyrir ítarlegt vöruhúsakerfi. Áður en þú móttekur ASN verður innkaupapöntun að vera skráð í kerfið gagnvart lánardrottninum sem sendir ASN.

## <a name="inbound-asn-v3-entity"></a>Eining ASN á innleið V3

Þú flytur inn ASN-númer á heimleið með því að nota *Á heimleið ASN V3* samsett gagnaeining. *ASN á innleið V3* nýtir sér eftirfarandi einingar:

- Haus farms á innleið
- Haus sendingar á innleið
- Pakkaskipan farms á innleið
- Kassar pakkaskipana farms á innleið
- Kassalínur pakkaskipanar farms á innleið
- Pakkaskipunarlínur farms á innleið

Samsetta gagnaeiningin *ASN á innleið V3* er ætluð fyrir aðstæður ósamstilltrar samþættingar þar sem innflutningur á XML-skrá er notaður.

## <a name="xml-format-for-importing-asns"></a>XML-snið til að flytja inn ASN

Microsoft Dynamics 365 Supply Chain Management styður eftirfarandi XML-snið til að flytja inn ASN. Hver hnútur í XML-skránni táknar eigind frá stakri einingu.

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity>
        <WHSInboundShipmentHeaderEntity>
            <WHSInboundLoadPackingStructureEntity>
                <WHSInboundLoadPackingStructureCaseEntity>
                    <WHSInboundPackingStructureCaseLineV3Entity>
                    </WHSInboundPackingStructureCaseLineV3Entity>
                </WHSInboundLoadPackingStructureCaseEntity>
                <WHSInboundLoadPackingStructureLineV3Entity>
                </WHSInboundLoadPackingStructureLineV3Entity>
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

## <a name="examples"></a>Dæmi

Í eftirfarandi undirhlutum eru dæmi um XML-innflutningsskrár ASN fyrir sendingar lánardrottins.

### <a name="example-1"></a>Dæmi 1

Eftirfarandi dæmi sýnir XML-skrá til að flytja inn sendingar lánardrottins fyrir eina innkaupapöntun þegar engar upplýsingar um mál eru innifaldar.

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity TRACTORNUMBER="0000101">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_01" VENDORADDRESSCOUNTRYREGIONID = "USA" VENDORADDRESSSTREET = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV3Entity PURCHASEORDERNUMBER="00000176" ITEMNUMBER="A0001" QUANTITY="1" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

### <a name="example-2"></a>Dæmi 2

Eftirfarandi dæmi sýnir XML-skrá til að flytja inn sendingar lánardrottins fyrir eina innkaupapöntun þegar upplýsingar um mál eru innifaldar.

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity ESTIMATEDARRIVALDATETIME="2021-04-25T11:00:00+00:00">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="MVR_SNN_0004">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="MVR_SNN_0004" PACKEDTOTALQUANTITY="2.00">
                <WHSInboundLoadPackingStructureCaseEntity PARENTPACKINGSTRUCTURELICENSEPLATENUMBER="MVR_SNN_0004" LICENSEPLATENUMBER="MVR_SNN_0004A" PACKEDTOTALQUANTITY="2.00" />
                <WHSInboundLoadPackingStructureLine3Entity PURCHASEORDERNUMBER="00000175" ITEMNUMBER="A0001" PURCHASEORDERLINENUMBER="1" QUANTITY="2.00" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

### <a name="example-3"></a>Dæmi 3

Eftirfarandi dæmi sýnir XML-skrá til að flytja inn sendingar lánardrottins fyrir margar innkaupapantanir þegar upplýsingar um mál eru innifaldar.

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity TRACTORNUMBER="0000101">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_01" VENDORADDRESSCOUNTRYREGIONID = "USA" VendorAddressStreet = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV3Entity PURCHASEORDERNUMBER="00000176" ITEMNUMBER="A0001" QUANTITY="100" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_02" VENDORADDRESSCOUNTRYREGIONID = "USA" VendorAddressStreet = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV3Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="A0001" QUANTITY="200" UNITSYMBOL="ea" />
                <WHSInboundLoadPackingStructureLineV3Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="P0004" QUANTITY="300" UNITSYMBOL="ea" ITEMBATCHNUMBER="BN0001" />
            </WHSInboundLoadPackingStructureEntity>
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_002">
                <WHSInboundLoadPackingStructureCaseEntity LICENSEPLATENUMBER="LP_ASN_002_C01">
                    <WHSInboundLoadPackingStructureCaseLineV3Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="A0001" QUANTITY="400" UNITSYMBOL="ea" />
                </WHSInboundLoadPackingStructureCaseEntity>
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

## <a name="inspect-the-results-of-importing-an-asn-file"></a>Skoða niðurstöður innflutnings ASN-skráar

Fylgið þessum skrefum til að skoða niðurstöður innflutnings ASN-skráar.

1. Farðu í **Vöruhúsakerfi \> Hleðslur \> Allar hleðslur**.
1. Finnið og opnið hleðslu sem var búin til sem hluti af ASN-innflutningi.
1. Í flýtiflipanum **Hleðsla** ættir þú að sjá gildi sem byggjast á XML-skránni.
1. Í flýtiflipanum **Hleðslulínur** ættirðu að sjá innkaupapöntunarnúmer og upplýsingar um vöru sem byggjast á XML-skránni.
1. Á aðgerðasvæðinu, í flipanum **Senda og móttaka**, í hópnum **Móttaka**, skal velja **Pökkunarskipulag** til að yfirfara pökkunarskipulag hleðslunnar.
1. Í flýtiflipanum **Vörubretti** ættir þú að sjá númeraplötur sem byggjast á XML-skránni.
1. Í flýtiflipanum **Kassar** ættir þú að sjá kassa sem byggjast á XML-skránni.
1. Í flýtiflipanum **Vörur** ættir þú að sjá vörur og magn sem byggist á XML-skránni.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
