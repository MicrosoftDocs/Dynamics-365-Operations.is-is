---
title: Sameinuð vöruupplifun
description: Þetta efni lýsir samþættingu afurðargagna milli forrita Finance and Operations og Common Data Service.
author: t-benebo
manager: AnnBe
ms.date: 09/3/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 9dc26e0e50c0b77555d09e4a50b846c80b1d5760
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249329"
---
# <a name="unified-product-experience"></a>Sameinuð vöruupplifun

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Þegar vistkerfi fyrirtækja samanstendur af Dynamics 365 forritum, svo sem Finance, Supply Chain Management og Sales, er það eðlilegt að viðskiptavinir noti þessi forrit til að fá upplýsingar um vöru. Þetta er vegna þess að þessi forrit bjóða upp á öfluga vöruinnviði ásamt háþróuðum verðlagningarhugtökum og nákvæmum birgðagögnum fyrir lagermagn. Viðskiptavinir sem nota utanaðkomandi vörukerfisstjórnunarkerfi (PLM) til að afla vörugagna geta sett vörur úr forritum Finance and Operations í rásir í öðrum forritum Dynamics 365. Sameinuð vöruupplifunin færir samþætt vörugagnalíkan til Common Data Service, þannig að allir notendur forritsins þ.m.t. notendur Power Platform geta nýtt sér þau ríku vörugögn sem koma úr forritum Finance and Operations.

Hérna er vöruupplýsingamódelið úr Sales.

![Gagnamódel fyrir vörur Sales](media/dual-write-product-4.jpg)

Hérna er vöruupplýsingamódelið úr forritum Finance and Operations.

![Gagnamódel fyrir vörur í Finance and Operations](media/dual-write-products-5.jpg)

Þessi tvö afurðalíkön hafa verið samþætt í Common Data Service eins og sýnt er hér að neðan.

![Gagnamódel fyrir vörur í forritum Dynamics 365](media/dual-write-products-6.jpg)

Kortin með tvískiptum skrifum fyrir vörur hafa verið hönnuð til að streyma gögnum aðeins í eina átt og það er nánast rauntíma reynsla úr forritum Finance and Operations til Common Data Service. Samt sem áður hafa vöruinnviðir verið opnaðir svo að hún verði tvíátta ef þess er krafist. Viðskiptavinir geta sérsniðið það, á eigin ábyrgð, þar sem Microsoft mælir ekki með þessari aðferð.

## <a name="templates"></a>Sniðmát

Afurðarupplýsingar innihalda allar upplýsingar sem tengjast vörunni og skilgreiningu hennar, svo sem afurðarvíddir eða mælingar og geymsluvíddir. Eins og meðfylgjandi tafla sýnir, er safn af einingakortum búið til til að samstilla vörur og tengdar upplýsingar.

Finance and Operations | Önnur Dynamics 365 forrit
-----------------------|--------------------------------
Útgefnar afurðir V2 | msdyn\_sharedproductdetails
CDS-útgefnar einkvæmar afurðir | Afurð
Afurðarnúmer sem eru auðkennd með strikamerki | msdyn\_productbarcodes
Sjálfgefnar pöntunarstillingar | msdyn\_productdefaultordersettings
Sjálfgefnar afurðatengdar pöntunarstillingar | msdyn_productspecificdefaultordersettings
Afurðavíddaflokkar | msdyn\_productdimensiongroups
Geymsluvíddarflokkar | msdyn\_productstoragedimensiongroups
Rakningarvíddarflokkar | msdyn\_producttrackingdimensiongroups
Litir | msdyn\_productcolors
Stærðir | msdyn\_productsizes
Stílar | msdyn\_productsytles
Skilgreiningar | msdyn\_productconfigurations
Litir afurðarsniðmáts. | msdyn_sharedproductcolors
Stærðir afurðarsniðmáts | msdyn_sharedproductsizes
Stílar afurðarsniðmáts | msdyn_sharedproductstyles
Skilgreiningar afurðarsniðmáts | msdyn_sharedproductconfigurations
Allar afurðir | msdyn_globalproducts
Eining | uoms
Umreikningur eininga | msdyn_ unitofmeasureconversions
Afurðatengd umskráning mælieiningar | msdyn_productspecificunitofmeasureconversion
Svæði | msdyn\_operationalsites
Vöruhús | msdyn\_inventwarehouses

[!include [symbols](../includes/dual-write-symbols.md)]

## <a name="integration-of-products"></a>Samþætting á afurðum

Í þessu líkani er varan táknuð með samsetningu tveggja aðila í Common Data Service: **Vara** og **msdyn\_sharedproductdetails**. Fyrri einingin hefur að geyma skilgreininguna á vöru (einstaka auðkenni fyrir vöruna, vöruheitið og lýsinguna), en önnur aðilinn inniheldur reitina sem eru geymdir á afurðastigi. Samsetning þessara tveggja aðila er notuð til að skilgreina afurðina í samræmi við hugtakið lagerhaldseining (SKU). Hver afurð sem gefin er út verður að hafa upplýsingar sínar í umræddum einingum (Upplýsingar um afurð og samnýtta afurð) Til að fylgjast með öllum afurðum (gefnar út og ekki gefnar út) er einingin **Altækar afurðir** notuð. 

Þar sem varan er táknuð sem SKU er hægt að fanga hugtökin aðgreindar vörur, vörumeistarar og afbrigði afurða í Common Data Service á eftirfarandi hátt:

- **Afurðir með undirgerð afurðar** eru afurðir sem eru skilgreindar af sjálfum sér. Engar víddir þarf að skilgreina fyrir þær. Dæmi er sérstök bók. Fyrir þessar afurðir er ein skrá búin til í einingunni **Afurð**, og ein skrá er búin til í einingunni **msdyn\_sharedproductdetails**. Engin skrá afurðafjölskyldu er búin til.
- **Afurðarsniðmát** eru notuð sem almennar afurðir sem innihalda skilgreininguna og reglur sem ákvarða hegðun í viðskiptaferlum. Samkvæmt þessum skilgreiningum er hægt að búa til sérstakar afurðir sem eru þekktar sem vöruafbrigði. Sem dæmi má nefna að stuttermabolur er afurðasniðmát og hann getur haft lit og stærð sem víddir. Hægt er að losa afbrigði sem hafa mismunandi samsetningar af þessum víddum, eins og litlum bláum stuttermabol eða meðalstórum grænum stuttermabol. Í samþættingunni er ein skrá á hvert afbrigði búin til í afurðatöflunni. Þessi skrá inniheldur upplýsingar um afbrigði, eins og mismunandi víddir. Almennar upplýsingar um vöruna eru geymdar í einingunni **msdyn\_sharedproductdetails**. (Þessar almennu upplýsingar eru geymdar í afurðarsniðmáti.) Að auki er ein skrá afurðafjölskyldu búin til fyrir hvert afurðasafn. Upplýsingar um afurðarsniðmát eru samstilltar við Common Data Service um leið og útgefið afurðarsniðmát er stofnað (en áður en afbrigði eru gefin út).
- **Einkvæmar afurðir** vísa til allra undirgerðaafurða afurðanna og allra afurðaafbrigðanna. 

![Gagnamódel fyrir afurðir](media/dual-write-product.png)

Þegar tvískipt skrifað er virkt verða forritin úr Finance and Operations samstillt í öðrum forritum Dynamics 365 í stöðunni **Drög**. Þeim er bætt við fyrstu verðskrána með sama gjaldmiðil. Með öðrum orðum, þeim er bætt við fyrstu verðskrána í forriti Dynamics 365 sem samsvarar gjaldmiðli lögaðila þíns þar sem varan er gefin út í forriti Finance and Operations. 

Til að samstilla vöruna við stöðuna **Virkt**, svo þú getir til dæmis notað hana beint í sölupöntunartilboðum þarf að velja eftirfarandi stillingu: undir **Kerfið> Stjórnun> Kerfisstjórnun> Kerfisstillingar> Sala** velurðu **Stofna vörur í virkri stöðu = já**. 

### <a name="cds-released-distinct-products-to-product"></a>CDS gaf út einkvæmar afurðir í Afurð

Einingin **Afurð** inniheldur reitina sem skilgreina afurðina. Hún felur í sér einstakar afurðir (afurðir með undirgerðaafurð) og afurðarafbrigðin. Eftirfarandi tafla sýnir vörpun.

Upprunasvæði | Gerð vörpunar | Áfangasvæði
---|---|---
PRODUCTNUMBER | >> | productnumber
PRODUCTNAME | >> | heiti
PRODUCTDESCRIPTION | >> | lýsing
ITEMNUMBER | >> | msdyn_itemnumber
CURRENCYCODE | >> | transactioncurrencyid.isocurrencycode
SALESUNITSYMBOL | >> | defaultuomid.msdyn_symbol
SALESPRICE | >> | verð
UNITCOST | >> | currentcost
PRODUCTTYPE | >> | producttypecode
SALESUNITDECIMALPRECISION | >> | quantitydecimal
ISCATCHWEIGHTPRODUCT | >> | msdyn_iscatchweight
PRODUCTCOLORID | >> | msdyn_productcolor.msdyn_productcolorname
PRODUCTCONFIGURATIONID | >> | msdyn_productconfiguration.msdyn_productconfiguration
PRODUCTSIZEID | >> | msdyn_productsize.msdyn_productsize
PRODUCTSTYLEID | >> | msdyn_productstyle.msdyn_productstyle

### <a name="released-products-v2-to-msdyn_sharedproductdetails"></a>Útgefnar afurðir V2 til msdyn\_sharedproductdetails

Einingin **msdyn\_sharedproductdetails** inniheldur reitina úr forritum Finance and Operations sem skilgreina afurðina og innihalda fjárhags- og stjórnunarupplýsingar afurðarinnar. Eftirfarandi tafla sýnir vörpun.

Upprunasvæði | Gerð vörpunar | Áfangasvæði
---|---|---
PRODUCTNUMBER | > | msdyn_globalproduct.msdyn_productnumber
INTRASTATCHARGEPERCENTAGE | > | msdyn_intrastatchargepercentage
ITEMNUMBER | >> | msdyn_itemnumber
APPROXIMATESALESTAXPERCENTAGE | > | msdyn_approximatesalestaxpercentage
BESTBEFOREPERIODDAYS | > | msdyn_bestbeforeperioddays
CARRYINGCOSTABCCODE | >> | msdyn_carryingcostabccode
CONSTANTSCRAPQUANTITY | > | msdyn_constantscrapquantity
COSTCHARGESQUANTITY | > | msdyn_costchargesquantity
DEFAULTRECEIVINGQUANTITY | > | msdyn_defaultreceivingquantity
FIXEDPURCHASEPRICECHARGES | > | msdyn_fixedpurchasepricecharges
FIXEDSALESPRICECHARGES | > | msdyn_fixedsalespricecharges
GROSSDEPTH | > | msdyn_grossdepth
GROSSPRODUCTHEIGHT | > | msdyn_grossproductheight
GROSSPRODUCTWIDTH | > | msdyn_grossproductwidth
INVENTORYUNITSYMBOL | > | msdyn_inventoryunitsymbol.msdyn_symbol
ISDISCOUNTPOSREGISTRATIONPROHIBITED | >> | msdyn_isdiscountposregistrationprohibited
ISEXEMPTFROMAUTOMATICNOTIFICATIONANDCANCELLATION | >> | msdyn_exemptautomaticnotificationcancel
ISINSTALLMENTELIGIBLE | >> | msdyn_isinstallmenteligible
ISINTERCOMPANYPURCHASEUSAGEBLOCKED | >> | msdyn_isintercompanypurchaseusageblocked
ISINTERCOMPANYSALESUSAGEBLOCKED | >> | msdyn_isintercompanysalesusageblocked
ISMANUALDISCOUNTPOSREGISTRATIONPROHIBITED | >> | msdyn_ismanualdiscposregistrationprohibited
ISPHANTOM | >> | msdyn_isphantom
ISPOSREGISTRATIONBLOCKED | >> | msdyn_isposregistrationblocked
ISPOSREGISTRATIONQUANTITYNEGATIVE | >> | msdyn_isposregistrationquantitynegative
ISPURCHASEPRICEAUTOMATICALLYUPDATED | >> | msdyn_ispurchasepriceautomaticallyupdated
ISPURCHASEPRICEINCLUDINGCHARGES | >> | msdyn_ispurchasepriceincludingcharges
ISSALESWITHHOLDINGTAXCALCULATED | >> | msdyn_issaleswithholdingtaxcalculated
ISRESTRICTEDFORCOUPONS | >> | msdyn_isrestrictedforcoupons
ISSALESPRICEADJUSTMENTALLOWED | >> | msdyn_issalespriceadjustmentallowed
ISSALESPRICEINCLUDINGCHARGES | >> | msdyn_issalespriceincludingcharges
ISSCALEPRODUCT | >> | msdyn_isscaleproduct
ISSHIPALONEENABLED | >> | msdyn_isshipaloneenabled
ISUNITCOSTPRODUCTVARIANTSPECIFIC | >> | msdyn_isunitcostproductvariantspecific
ISVARIANTSHELFLABELSPRINTINGENABLED | >> | msdyn_isvariantshelflabelsprintingenabled
ISZEROPRICEPOSREGISTRATIONALLOWED | >> | msdyn_iszeropriceposregistrationallowed
KEYINPRICEREQUIREMENTSATPOSREGISTER | >> | msdyn_keyinpricerequirementsatposregister
KEYINQUANTITYREQUIREMENTSATPOSREGISTER | >> | msdyn_keyinquantityrequirementsatposregister
MARGINABCCODE | >> | msdyn_marginabccode
MAXIMUMPICKQUANTITY | > | msdyn_maximumpickquantity
MUSTKEYINCOMMENTATPOSREGISTER | >> | msdyn_mustkeyincommentatposregister
NECESSARYPRODUCTIONWORKINGTIMESCHEDULINGPROPERTYID | > | msdyn_necessaryproductionworkingtimeschedulingp
NETPRODUCTWEIGHT | > | msdyn_netproductweight
PACKINGDUTYQUANTITY | > | msdyn_packingdutyquantity
POSREGISTRATIONACTIVATIONDATE | > | msdyn_posregistrationactivationdate
POSREGISTRATIONBLOCKEDDATE | > | msdyn_posregistrationblockeddate
POSREGISTRATIONPLANNEDBLOCKEDDATE | > | msdyn_posregistrationplannedblockeddate
POTENCYBASEATTIBUTETARGETVALUE | > | msdyn_potencybaseattibutetargetvalue
POTENCYBASEATTRIBUTEVALUEENTRYEVENT | >> | msdyn_potencybaseattributevalueentryevent
PRODUCTTYPE | >> | msdyn_producttype
PRODUCTIONCONSUMPTIONDENSITYCONVERSIONFACTOR | > | msdyn_productionconsumptiondensityconversion
PRODUCTIONCONSUMPTIONDEPTHCONVERSIONFACTOR | > | msdyn_productionconsumptiondepthconversion
PRODUCTIONCONSUMPTIONHEIGHTCONVERSIONFACTOR | > | msdyn_productionconsumptionheightconversion
PRODUCTIONCONSUMPTIONWIDTHCONVERSIONFACTOR | > | msdyn_productionconsumptionwidthconversion
PRODUCTVOLUME | > | msdyn_productvolume
PURCHASECHARGESQUANTITY | > | msdyn_purchasechargesquantity
PURCHASEOVERDELIVERYPERCENTAGE | > | msdyn_purchaseoverdeliverypercentage
PURCHASEPRICE | > | msdyn_purchaseprice
PURCHASEPRICEDATE | > | msdyn_purchasepricedate
PURCHASEPRICINGPRECISION | > | msdyn_purchasepricingprecision
PURCHASEUNDERDELIVERYPERCENTAGE | > | msdyn_purchaseunderdeliverypercentage
RAWMATERIALPICKINGPRINCIPLE | >> | msdyn_rawmaterialpickingprinciple
SALESCHARGESQUANTITY | > | msdyn_saleschargesquantity
SALESOVERDELIVERYPERCENTAGE | > | msdyn_salesoverdeliverypercentage
SALESPRICE | > | msdyn_salesprice
SALESPRICECALCULATIONCHARGESPERCENTAGE | > | msdyn_salespricecalculationchargespercentage
SALESPRICECALCULATIONCONTRIBUTIONRATIO | > | msdyn_salespricecalculationcontributionratio
SALESPRICECALCULATIONMODEL | >> | msdyn_salespricecalculationmodel
SALESPRICEDATE | > | msdyn_salespricedate
SALESPRICINGPRECISION | > | msdyn_salespricingprecision
SALESUNDERDELIVERYPERCENTAGE | > | msdyn_salesunderdeliverypercentage
SALESUNITSYMBOL | > | msdyn_salesunitsymbol.msdyn_symbol
SCALEINDICATOR | >> | msdyn_scaleindicator
SELLSTARTDATE | > | msdyn_sellstartdate
SHELFADVICEPERIODDAYS | > | msdyn_shelfadviceperioddays
SHELFLIFEPERIODDAYS | > | msdyn_shelflifeperioddays
SHIPSTARTDATE | > | msdyn_shipstartdate
TAREPRODUCTWEIGHT | > | msdyn_tareproductweight
TRANSFERORDEROVERDELIVERYPERCENTAGE | > | msdyn_transferorderoverdeliverypercentage
TRANSFERORDERUNDERDELIVERYPERCENTAGE | > | msdyn_transferorderunderdeliverypercentage
UNITCOST | > | msdyn_unitcost
UNITCOSTDATE | > | msdyn_unitcostdate
UNITCOSTQUANTITY | > | msdyn_unitcostquantity
VARIABLESCRAPPERCENTAGE | > | msdyn_variablescrappercentage
WAREHOUSEMOBILEDEVICEDESCRIPTIONLINE1 | > | msdyn_warehousemobiledevicedescriptionline1
WAREHOUSEMOBILEDEVICEDESCRIPTIONLINE2 | > | msdyn_warehousemobiledevicedescriptionline2
WILLINVENTORYISSUEAUTOMATICALLYREPORTASFINISHED | >> | msdyn_willinventoryissueautoreportasfinished
WILLINVENTORYRECEIPTIGNOREFLUSHINGPRINCIPLE | >> | msdyn_willinventoryreceiptignoreflushing
WILLPICKINGWORKBENCHAPPLYBOXINGLOGIC | >> | msdyn_willpickingworkbenchapplyboxinglogic
WILLTOTALPURCHASEDISCOUNTCALCULATIONINCLUDEPRODUCT | >> | msdyn_willtotalpurchdiscountcalcincludeproduct
WILLTOTALSALESDISCOUNTCALCULATIONINCLUDEPRODUCT | >> | msdyn_willtotalsalesdiscountcalcincludeproduct
WILLWORKCENTERPICKINGALLOWNEGATIVEINVENTORY | >> | msdyn_willworkcenterpickingallownegativeinvent
YIELDPERCENTAGE | > | msdyn_yieldpercentage
ISUNITCOSTAUTOMATICALLYUPDATED | >> | msdyn_isunitcostautomaticallyupdated
PURCHASEUNITSYMBOL | > | msdyn_purchaseunitsymbol.msdyn_symbol
PURCHASEPRICEQUANTITY | > | msdyn_purchasepricequantity
ISUNITCOSTINCLUDINGCHARGES | >> | msdyn_isunitcostincludingcharges
FIXEDCOSTCHARGES | >> | msdyn_fixedcostcharges
MINIMUMCATCHWEIGHTQUANTITY | >> | msdyn_minimumcatchweightquantity
MAXIMUMCATCHWEIGHTQUANTITY | >> | msdyn_maximumcatchweightquantity
ALTERNATIVEITEMNUMBER | >> | msdyn_alternativeitemnumber.msdyn_itemnumber
BOMUNITSYMBOL | >> | msdyn_bomunitsymbol.msdyn_symbol
CATCHWEIGHTUNITSYMBOL | >> | msdyn_catchweightunitsymbol.msdyn_symbol
COMPARISONPRICEBASEUNITSYMBOL | >> | msdyn_comparisonpricebaseunitsymbol.msdyn_symbol
PRIMARYVENDORACCOUNTNUMBER | >> | msdyn_vendorid.msdyn_vendoraccountnumber
ISCATCHWEIGHTPRODUCT | >> | msdyn_iscatchweight
PRODUCTDIMENSIONGROUPNAME | >> | msdyn_productdimensiongroupid.msdyn_groupname

## <a name="all-product-to-msdyn_global-products"></a>Allar afurðir til msdyn_global products

Einingin fyrir allar afurðir inniheldur allar afurðir sem eru í boði í forritum Finance and Operations, bæði útgefnar afurðir og afurðir sem ekki eru gefnar út. Þessar afurðir eru fáanlegar í Common Data Service með eftirfarandi vörpunum:

Upprunasvæði | Gerð vörpunar | Áfangasvæði
---|---|---
PRODUCTNAME | >> | msdyn_productname
PRODUCTNUMBER | >> | msdyn_productnumber

## <a name="product-dimensions"></a>Afurðarvíddir 

Afurðavíddir eru einkenni sem auðkenna afurðarafbrigði. Fjórar vöruvíddir (Litur, Stærð, Stíll og Stilling) er einnig varpað á Common Data Service til að skilgreina afbrigði afurða. Eftirfarandi mynd sýnir gagnalíkanið fyrir afurðavíddina Litur. Sama líkani er beitt á stærðir, stíl og stillingar. 

![Gagnamódel fyrir afurðir](media/dual-write-product-2.PNG)

### <a name="colors"></a>Litir

Hugsanlegir litir í eru fáanlegir í Common Data Service í gegnum eftirfarandi varpanir.

Upprunasvæði | Gerð vörpunar | Áfangasvæði
---|---|---
COLORID | \>\> | msdyn\_productcolorname

### <a name="sizes"></a>Stærðir

Hugsanlegar stærðir í eru fáanlegar í Common Data Service í gegnum eftirfarandi varpanir.

Upprunasvæði | Gerð vörpunar | Áfangasvæði
---|---|---
SIZEID | \>\> | msdyn\_productsize

### <a name="styles"></a>Stílar

Hugsanlegir stílar í eru fáanlegir í Common Data Service í gegnum eftirfarandi varpanir.

Upprunasvæði | Gerð vörpunar | Áfangasvæði
---|---|---
STYLEID | \>\> | msdyn\_productstyle

### <a name="configurations"></a>Skilgreiningar

Hugsanlegar skilgreiningar í eru fáanlegar í Common Data Service í gegnum eftirfarandi varpanir.

Upprunasvæði | Gerð vörpunar | Áfangasvæði
---|---|---
CONFIGURATIONID | \>\> | msdyn\_name

Þegar afurð hefur mismunandi afurðavíddir (til dæmis hefur afurðarsniðmát stærð og lit sem afurðavíddir) er hver einkvæm afurð (það er hvert afurðarafbrigði) skilgreind sem samsetning þessara afurðavíddar. Til dæmis er afurðanúmer B0001 extra-lítill svartur bolur og afurðanúmer B0002 er lítill svartur bolur. Í þessu tilfelli eru núverandi samsetningar afurðavíddar skilgreindar. Bolurinn úr dæminu á undan getur til dæmis verið extra-lítill og svartur, lítill og svartur, meðalstór og svartur, eða stór og svartur, en hann getur ekki verið extra-stór og svartur. Með öðrum orðum eru afurðavíddir sem afurðarsniðmát getur notað tilgreindar og hægt er að gefa afbrigði út frá þessum gildum.

Til að halda utan um afurðavíddir sem afurðarsniðmát getur notað eru eftirfarandi einingar stofnaðar og varpað í Common Data Service fyrir hverja afurðavídd. Frekari upplýsingar eru í [Yfirlit afurðarupplýsinga](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/pim/product-information).

### <a name="shared-product-color"></a>Sameiginlegur afurðalitur

Einingin **Sameiginlegur afurðalitur** gefur til kynna liti sem sérstakt afurðarsniðmát getur haft. Þetta hugtak er flutt í Common Data Service til að halda gögnum samkvæmum. Eftirfarandi tafla sýnir vörpun.

Upprunasvæði | Gerð vörpunar | Áfangasvæði
---|---|---
PRODUCTCOLORID | \>\> | msdyn\_productcolorid.msdyn\_productcolorname
PRODUCTMASTERNUMBER | \>\> | msdyn\_sharedproductdetailid.msdyn\_itemnumber
REPLENISHMENTWEIGHT | \>\> | msdyn\_replenishmentweight
DISPLAYSEQUENCENUMBER | \>\> | msdyn\_retaildisplayorder

### <a name="shared-product-size"></a>Sameiginleg afurðastærð

Einingin **Sameiginleg afurðastærð** gefur til kynna stærðir sem sérstakt afurðarsniðmát getur haft. Þetta hugtak er flutt í Common Data Service til að halda gögnum samkvæmum. Eftirfarandi tafla sýnir vörpun.

Upprunasvæði | Gerð vörpunar | Áfangasvæði
---|---|---
PRODUCTMASTERNUMBER | \>\> | msdyn\_sharedproductdetailid.msdyn\_itemnumber
PRODUCTSIZEID | \>\> | msdyn\_productsizeid.msdyn\_productsize
REPLENISHMENTWEIGHT | \>\> | msdyn\_replenishmentweight
DISPLAYSEQUENCENUMBER | \>\> | msdyn\_displaysequencenumber

### <a name="shared-product-style"></a>Sameiginlegur afurðastíll

Einingin **Sameiginlegur afurðastíll** gefur til kynna stíla sem sérstakt afurðarsniðmát getur haft. Þetta hugtak er flutt í Common Data Service til að halda gögnum samkvæmum. Eftirfarandi tafla sýnir vörpun.

Upprunasvæði | Gerð vörpunar | Áfangasvæði
---|---|---
PRODUCTMASTERNUMBER | \>\> | msdyn\_sharedproductdetailsid.msdyn\_itemnumber
PRODUCTSTYLEID | \>\> | msdyn\_productstyleintegration
PRODUCTSTYLEID | \>\> | msdyn\_productstyleid.msdyn\_productstyle
REPLENISHMENTWEIGHT | \>\> | msdyn\_replenishmentweight
DISPLAYSEQUENCENUMBER | \>\> | msdyn\_displaysequencenumber

### <a name="shared-product-configuration"></a>Sameiginleg skilgreining afurða

Einingin **Sameiginleg skilgreining afurða** gefur til kynna skilgreiningar sem sérstakt afurðarsniðmát getur haft. Þetta hugtak er flutt í Common Data Service til að halda gögnum samkvæmum. Eftirfarandi tafla sýnir vörpun.

Upprunasvæði | Gerð vörpunar | Áfangasvæði
---|---|---
CONTAINERUNITSYMBOL | \>\> | msdyn\_containerunitsymbol
PRODUCTCONFIGURATIONID | \>\> | msdyn\_productconfigurationid.msdyn\_productconfiguration
PRODUCTMASTERNUMBER | \>\> | msdyn\_sharedproductdetailid.msdyn\_itemnumber
REPLENISHMENTWEIGHT | \>\> | msdyn\_replenishmentweight
DISPLAYSEQUENCENUMBER | \>\> | msdyn\_displaysequencenumber

## <a name="product-number-identifier-bar-codes"></a>Afurðarnúmer sem eru auðkennd með strikamerki

Strikamerki afurða eru notuð til að bera kennsl á afurðir á einkvæman hátt. Eftirfarandi varpanir eru notaðar til að gera þessi strikamerki afurða tiltæk í Common Data Service.

Upprunasvæði | Gerð vörpunar | Áfangasvæði
---|---|---
PRODUCTNUMBER | \> | msdyn\_productnumberid.productnumber
BARCODE | \> | msdyn\_name
BARCODE | \> | msdyn\_barcode
PRODUCTQUANTITY | \> | msdyn\_productquantity
PRODUCTDESCRIPTION | \> | msdyn\_productdescription
BARCODESETUPID | \> | msdyn\_barcodesetupid
PRODUCTQUANTITYUNITSYMBOL | \> | msdyn\_unitofmeasureid.name
ISDEFAULTSCANNEDBARCODE | \>\> | msdyn\_isdefaultscannedbarcode
ISDEFAULTPRINTEDBARCODE | \>\> | msdyn\_isdefaultprintedbarcode
ISDEFAULTDISPLAYEDBARCODE | \>\> | msdyn\_isdefaultdisplayedbarcode

## <a name="default-order-settings-and-product-specific-default-order-settings"></a>Sjálfgefnar pöntunarstillingar og afurðatengdar sjálfgefnar pöntunarstillingar

Sjálfgefið pöntunarstillingar skilgreina svæði og vöruhús þar sem afurðir verða upprunnin frá eða geymdar, í lágmarks, hámarks, margar og staðlaðs magns sem verða notuð fyrir viðskipti eða birgðastjórnun, afhendingartíma, stöðvunarflagg, og aðferðina pöntun lofað. Þessar upplýsingar verða aðgengilegar í CDS með því að nota sjálfgefnu pöntunarstillingarnar og afurðatengda sjálfgefnr pöntunarstillingaeiningu. Þú getur lesið frekari upplýsingar um virkni á [Sjálfgefin pöntunarstillingar](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/production-control/default-order-settings).

### <a name="default-order-settings"></a>Sjálfgefnar pöntunarstillingar

Eftirfarandi varpanir eru notaðar til að gera sjálfgefnar pöntunarstillingar tiltækar í Common Data Service.

Upprunasvæði | Gerð vörpunar | Áfangasvæði
---|---|---
INVENTWAREHOUSEID | = | msdyn_inventorywarehouse.msdyn_warehouseidentifier
INVENTORYSITEID | = | msdyn_inventorysite.msdyn_siteid
INVENTORYATPDELAYEDDEMANDOFFSETDAYS | = | msdyn_inventoryatpdelayeddemandoffsetdays
INVENTORYATPDELAYEDSUPPLYOFFSETDAYS | = | msdyn_inventoryatpdelayedsupplyoffsetdays
ITEMNUMBER | = | msdyn_itemnumber.msdyn_itemnumber
INVENTORYATPBACKWARDDEMANDTIMEFENCEDAYS | = | msdyn_inventoryatpbackwarddemandtimefencedays
INVENTORYATPBACKWARDSUPPLYTIMEFENCEDAYS | = | msdyn_inventoryatpbackwardsupplytimefencedays
INVENTORYATPTIMEFENCEDAYS | = | msdyn_inventoryatptimefencedays
MAXIMUMINVENTORYORDERQUANTITY | = | msdyn_maximuminventoryorderquantity
MAXIMUMPROCUREMENTORDERQUANTITY | = | msdyn_maximumprocurementorderquantity
MAXIMUMSALESORDERQUANTITY | = | msdyn_maximumsalesorderquantity
MINIMUMINVENTORYORDERQUANTITY | = | msdyn_minimuminventoryorderquantity
MINIMUMPROCUREMENTORDERQUANTITY | = | msdyn_minimumprocurementorderquantity
MINIMUMSALESORDERQUANTITY | = | msdyn_minimumsalesorderquantity
STANDARDINVENTORYORDERQUANTITY | = | msdyn_standardinventoryorderquantity
STANDARDPROCUREMENTORDERQUANTITY | = | msdyn_standardprocurementorderquantity
STANDARDSALESORDERQUANTITY | = | msdyn_standardsalesorderquantity
INVENTORYLEADTIMEDAYS | = | msdyn_inventoryleadtimedays
INVENTORYQUANTITYMULTIPLES | = | msdyn_inventoryquantitymultiples
PROCUREMENTQUANTITYMULTIPLES | = | msdyn_procurementquantitymultiples
SALESQUANTITYMULTIPLES | = | msdyn_salesquantitymultiples
PROCUREMENTSITEID | = | msdyn_procurementsite.msdyn_siteid
PROCUREMENTLEADTIMEDAYS | = | msdyn_procurementleadtimedays
SALESSITEID | = | msdyn_salessite.msdyn_siteid
SALESATPDELAYEDDEMANDOFFSETDAYS | = | msdyn_salesatpdelayeddemandoffsetdays
SALESATPDELAYEDSUPPLYOFFSETDAYS | = | msdyn_salesatpdelayedsupplyoffsetdays
SALESATPBACKWARDDEMANDTIMEFENCEDAYS | = | msdyn_salesatpbackwarddemandtimefencedays
SALESATPBACKWARDSUPPLYTIMEFENCEDAYS | = | msdyn_salesatpbackwardsupplytimefencedays
SALESATPTIMEFENCEDAYS | = | msdyn_salesatptimefencedays
SALESLEADTIMEDAYS | = | msdyn_salesleadtimedays
PROCUREMENTWAREHOUSEID | = | msdyn_procurementwarehouse.msdyn_warehouseidentifier
SALESWAREHOUSEID | = | msdyn_saleswarehouse.msdyn_warehouseidentifier
AREINVENTORYORDERPROMISINGDEFAULTSOVERRIDDEN | >< | msdyn_areinventoryorderdefaultsoverridden
INVENTORYORDERPROMISINGMETHOD | >< | msdyn_inventoryorderpromisingmethod
ISINVENTORYATPINCLUDINGPLANNEDORDERS | >< | msdyn_isinventoryatpincludingplannedorders
ISINVENTORYUSINGWORKINGDAYS | >< | msdyn_isinventoryusingworkingdays
ISINVENTORYSITEMANDATORY | >< | msdyn_isinventorysitemandatory
ISINVENTORYPROCESSINGSTOPPED | >< | msdyn_isinventoryprocessingstopped
ISPROCUREMENTUSINGWORKINGDAYS | >< | msdyn_isprocurementusingworkingdays
ISPROCUREMENTSITEMANDATORY | >< | msdyn_isprocurementsitemandatory
ISPROCUREMENTPROCESSINGSTOPPED | >< | msdyn_isprocurementprocessingstopped
ARESALESORDERPROMISINGDEFAULTSOVERRIDDEN | >< | msdyn_aresalesorderdefaultsoverridden
SALESORDERPROMISINGMETHOD | >< | msdyn_salesorderpromisingmethod
ISSALESATPINCLUDINGPLANNEDORDERS | >< | msdyn_issalesatpincludingplannedorders
ISSALESSITEMANDATORY | >< | msdyn_issalessitemandatory
ISSALESLEADTIMEOVERRIDDEN | >< | msdyn_issalesleadtimeoverridden
ISSALESPROCESSINGSTOPPED | >< | msdyn_issalesprocessingstopped
ISINVENTORYWAREHOUSEMANDATORY | >< | msdyn_isinventorywarehousemandatory
ISPROCUREMENTWAREHOUSEMANDATORY | >< | msdyn_isprocurementwarehousemandatory
ISSALESWAREHOUSEMANDATORY | >< | msdyn_issaleswarehousemandatory

### <a name="product-specific-default-order-settings"></a>Sjálfgefnar afurðatengdar pöntunarstillingar

Eftirfarandi varpanir eru notaðar til að gera afurðatengdar sjálfgefnar pöntunarstillingar tiltækar í Common Data Service.

Upprunasvæði | Gerð vörpunar | Áfangasvæði
---|---|---
INVENTORYWAREHOUSEID | = | msdyn_inventorywarehouse.msdyn_warehouseidentifier
INVENTORYSITEID | = | msdyn_inventorysite.msdyn_siteid
INVENTORYATPDELAYEDDEMANDOFFSETDAYS | = | msdyn_inventoryatpdelayeddemandoffsetdays
INVENTORYATPDELAYEDSUPPLYOFFSETDAYS | = | msdyn_inventoryatpdelayedsupplyoffsetdays
ITEMNUMBER | = | msdyn_itemnumber.msdyn_itemnumber
INVENTORYATPBACKWARDDEMANDTIMEFENCEDAYS | = | msdyn_inventoryatpbackwarddemandtimefencedays
INVENTORYATPBACKWARDSUPPLYTIMEFENCEDAYS | = | msdyn_inventoryatpbackwardsupplytimefencedays
INVENTORYATPTIMEFENCEDAYS | = | msdyn_inventoryatptimefencedays
MAXIMUMINVENTORYORDERQUANTITY | = | msdyn_maximuminventoryorderquantity
MAXIMUMPROCUREMENTORDERQUANTITY | = | msdyn_maximumprocurementorderquantity
MAXIMUMSALESORDERQUANTITY | = | msdyn_maximumsalesorderquantity
MINIMUMINVENTORYORDERQUANTITY | = | msdyn_minimuminventoryorderquantity
MINIMUMPROCUREMENTORDERQUANTITY | = | msdyn_minimumprocurementorderquantity
MINIMUMSALESORDERQUANTITY | = | msdyn_minimumsalesorderquantity
STANDARDINVENTORYORDERQUANTITY | = | msdyn_standardinventoryorderquantity
STANDARDPROCUREMENTORDERQUANTITY | = | msdyn_standardprocurementorderquantity
STANDARDSALESORDERQUANTITY | = | msdyn_standardsalesorderquantity
INVENTORYLEADTIMEDAYS | = | msdyn_inventoryleadtimedays
INVENTORYQUANTITYMULTIPLES | = | msdyn_inventoryquantitymultiples
PROCUREMENTQUANTITYMULTIPLES | = | msdyn_procurementquantitymultiples
SALESQUANTITYMULTIPLES | = | msdyn_salesquantitymultiples
PROCUREMENTSITEID | = | msdyn_procurementsite.msdyn_siteid
PROCUREMENTLEADTIMEDAYS | = | msdyn_procurementleadtimedays
SALESSITEID | = | msdyn_salessite.msdyn_siteid
SALESATPDELAYEDDEMANDOFFSETDAYS | = | msdyn_salesatpdelayeddemandoffsetdays
SALESATPDELAYEDSUPPLYOFFSETDAYS | = | msdyn_salesatpdelayedsupplyoffsetdays
SALESATPBACKWARDDEMANDTIMEFENCEDAYS | = | msdyn_salesatpbackwarddemandtimefencedays
SALESATPBACKWARDSUPPLYTIMEFENCEDAYS | = | msdyn_salesatpbackwardsupplytimefencedays
SALESATPTIMEFENCEDAYS | = | msdyn_salesatptimefencedays
SALESLEADTIMEDAYS | = | msdyn_salesleadtimedays
PROCUREMENTWAREHOUSEID | = | msdyn_procurementwarehouse.msdyn_warehouseidentifier
SALESWAREHOUSEID | = | msdyn_saleswarehouse.msdyn_warehouseidentifier
AREINVENTORYDEFAULTORDERSETTINGSOVERRIDDEN | >< | msdyn_areinventoryorderdefaultsoverridden
INVENTORYORDERPROMISINGMETHOD | >< | msdyn_inventoryorderpromisingmethod
ISINVENTORYATPINCLUDINGPLANNEDORDERS | >< | msdyn_isinventoryatpincludingplannedorders
ISINVENTORYUSINGWORKINGDAYS | >< | msdyn_isinventoryusingworkingdays
ISINVENTORYSITEMANDATORY | >< | msdyn_isinventorysitemandatory
ISINVENTORYPROCESSINGSTOPPED | >< | msdyn_isinventoryprocessingstopped
ISPROCUREMENTUSINGWORKINGDAYS | >< | msdyn_isprocurementusingworkingdays
ISPROCUREMENTSITEMANDATORY | >< | msdyn_isprocurementsitemandatory
ISPROCUREMENTPROCESSINGSTOPPED | >< | msdyn_isprocurementprocessingstopped
ARESALESDEFAULTORDERSETTINGSOVERRIDDEN | >< | msdyn_aresalesorderdefaultsoverridden
SALESORDERPROMISINGMETHOD | >< | msdyn_salesorderpromisingmethod
ISSALESATPINCLUDINGPLANNEDORDERS | >< | msdyn_issalesatpincludingplannedorders
ISSALESSITEMANDATORY | >< | msdyn_issalessitemandatory
ISSALESLEADTIMEOVERRIDDEN | >< | msdyn_issalesleadtimeoverridden
ISSALESPROCESSINGSTOPPED | >< | msdyn_issalesprocessingstopped
ISINVENTORYWAREHOUSEMANDATORY | >< | msdyn_isinventorywarehousemandatory
ISPROCUREMENTWAREHOUSEMANDATORY | >< | msdyn_isprocurementwarehousemandatory
ISSALESWAREHOUSEMANDATORY | >< | msdyn_issaleswarehousemandatory
OPERATIONALSITEID | = | msdyn_operationalsite.msdyn_siteid
PRODUCTCOLORID | = | msdyn_productcolor.msdyn_productcolorname
PRODUCTCONFIGURATIONID | = | msdyn_productconfiguration.msdyn_productconfiguration
PRODUCTSIZEID | = | msdyn_productsize.msdyn_productsize
PRODUCTSTYLEID | = | msdyn_productstyle.msdyn_productstyle

## <a name="unit-of-measure-and-unit-of-measure-conversions"></a>Mælieining og umreikningur á mælieiningum viðskipta

Mælieiningarnar og umreikningur á þeim verða aðgengilegar í Common Data Service eftir gagnalíkaninu sem sýnt er á myndinni.

![Gagnamódel fyrir afurðir](media/dual-write-product-3.PNG)

Mælieiningin er samþætt á milli forrita Finance and Operations og annarra forrita Dynamics 365. Fyrir hvern einingaflokk í forriti Finance and Operations er einingahópur búinn til í forriti Dynamics 365, sem hefur að geyma einingar sem tilheyra einingaflokknum. Sjálfgefin grunneining er einnig búin til fyrir hvern einingahóp. 

### <a name="unit-of-measure"></a>Mælieining

Eftirfarandi varpanir eru notaðar til að gera mælieiningar í forritum Finance and Operations tiltækar í Common Data Service.

Upprunasvæði | Gerð vörpunar | Áfangasvæði
---|---|---
UNITSYMBOL | >> | msdyn_symbol
UNITCLASS | >> | msdyn_externalunitclassname
DECIMALPRECISION | >> | msdyn_decimalprecision
ISBASEUNIT | >> | msdyn_isbaseunit
ISSYSTEMUNIT | >> | msdyn_issystemunit
SYSTEMOFUNITS | >> | msdyn_systemofunits
UNITSYMBOL | >> | heiti
UNITDESCRIPTION | >> | msdyn_description

### <a name="unit-of-measure-conversions"></a>Umreikningur mælieininga

Eftirfarandi varpanir eru notaðar til að gera umreikning á mælieiningum í forritum Finance and Operations tiltækar í Common Data Service.

Upprunasvæði | Gerð vörpunar | Áfangasvæði
---|---|---
DENOMINATOR | = | msdyn_denominator
NUMERATOR | = | msdyn_numerator
FACTOR | = | msdyn_factor
INNEROFFSET | = | msdyn_inneroffset
OUTEROFFSET | = | msdyn_outeroffset
ROUNDING | >< | msdyn_rounding
TOUNITSYMBOL | = | msdyn_tounit.msdyn_symbol
FROMUNITSYMBOL | = | msdyn_fromunit.msdyn_symbol

### <a name="product-specific-unit-of-measure-conversions"></a>Umreikningur afurðatengdra mælieininga

Eftirfarandi varpanir eru notaðar til að gera umreikning á afurðatengdum mælieiningum í forritum Finance and Operations tiltækar í Common Data Service.

Upprunasvæði | Gerð vörpunar | Áfangasvæði
---|---|---
DENOMINATOR | = | msdyn_denominator
NUMERATOR | = | msdyn_numerator
FACTOR | = | msdyn_factor
FROMUNITSYMBOL | = | msdyn_fromunit.msdyn_symbol
TOUNITSYMBOL | = | msdyn_tounit.msdyn_symbol
PRODUCTNUMBER | = | msdyn_globalproduct.msdyn_productnumber
INNEROFFSET | = | msdyn_inneroffset
OUTEROFFSET | = | msdyn_outeroffset
ROUNDING | >< | msdyn_rounding

## <a name="product-policies-dimension-tracking-and-storage-groups"></a>Afurðastefna: vídd, mælingar og geymsluhópar

Afurðareglurnar eru reglur sem notaðar eru til að skilgreina afurðir og eiginleika þeirra í birgðum. Hægt er að finna afurðavíddarhópinn, afurðarakningarvíddarhópinn og geymsluvíddarhópinn sem afurðareglur. 

### <a name="product-dimension-group"></a>Afurðavíddaflokkur

Afurðavíddarhópurinn skilgreindi hvaða afurðavíddir skilgreina vöruna. Fjórir mögulegir afurðavíddaflokkar eru: stærð, litur, stíll og skilgreining. Afurðavíddaflokkarnir eru fáanlegir í Common Data Service með eftirfarandi vörpunum. 

Upprunasvæði | Gerð vörpunar | Áfangasvæði
---|---|---
WILLSALESPRICESEARCHUSEPRODUCTSTYLE | >< | msdyn_willsalespricesearchuseproductstyle
WILLPURCHASEPRICESEARCHUSEPRODUCTSIZE | >< | msdyn_willpurchasepricesearchuseproductsize
WILLSALESPRICESEARCHUSEPRODUCTCONFIGURATION | >< | msdyn_willsalespricesearchuseprodconfig
WILLSALESPRICESEARCHUSEPRODUCTCOLOR | >< | msdyn_willsalespricesearchuseproductcolor
WILLPURCHASEPRICESEARCHUSEPRODUCTSTYLE | >< | msdyn_willpurchasepricesearchuseproductstyle
WILLPURCHASEPRICESEARCHUSEPRODUCTCONFIGURATION | >< | msdyn_willpurchpricesearchuseprodconfig
WILLPURCHASEPRICESEARCHUSEPRODUCTCOLOR | >< | msdyn_willpurchpricesearchuseproductcolor
ISPRODUCTSTYLEACTIVE | >< | msdyn_isproductstyleactive
ISPRODUCTSIZEACTIVE | >< | msdyn_isproductsizeactive
ISPRODUCTCONFIGURATIONACTIVE | >< | msdyn_isproductconfigurationactive
ISPRODUCTCOLORACTIVE | >< | msdyn_isproductcoloractive
GROUPNAME | = | msdyn_groupname
GROUPDESCRIPTION | = | msdyn_groupdescription
PRODUCTVARIANTNOMENCLATURENAME | = | msdyn_productvariantnomenclaturename
WILLSALESPRICESEARCHUSEPRODUCTSIZE | >< | msdyn_willsalespricesearchuseproductsize

### <a name="product-tracking-dimension-group"></a>Víddaflokkur afurðarakningar

Víddarflokkur afurðarakningar táknar aðferðina sem notuð er til að rekja afurðina í birgðum. Þessar eru fáanlegar í Common Data Service með eftirfarandi vörpunum. 

Upprunasvæði | Gerð vörpunar | Áfangasvæði
---|---|---
SERIALNUMBERCAPTURINGOPERATION | >< | msdyn_serialnumbercapturingoperation
GROUPNAME | = | msdyn_groupname
GROUPDESCRIPTION | = | msdyn_groupdescription
ISSERIALNUMBERENABLEDFORPRODUCTIONCONSUMPTIONPROCESS | >< | msdyn_issnenabledforpcprocess
ISSERIALNUMBERCONTROLENABLED | >< | msdyn_isserialnumbercontrolenabled
ISSERIALNUMBERENABLEDFORSALESPROCESS | >< | msdyn_isserialnumberenabledforsalesprocess
ISSERIALNUMBERACTIVE | >< | msdyn_isserialnumberactive
ISSALESPRICEBYSERIALNUMBER | >< | msdyn_issalespricebyserialnumber
ISSALESPRICEBYBATCHNUMBER | >< | msdyn_issalespricebybatchnumber
ISPURCHASEPRICEBYSERIALNUMBER | >< | msdyn_ispurchasepricebyserialnumber
ISPURCHASEPRICEBYBATCHNUMBER | >< | msdyn_ispurchasepricebybatchnumber
ISPRIMARYSTOCKINGENABLEDFORSERIALNUMBER | >< | msdyn_isprimarystockingenabledforsn
ISPRIMARYSTOCKINGENABLEDFORBATCHNUMBER | >< | msdyn_isprimarystockingenabledforbn
ISPHYSICALINVENTORYENABLEDFORSERIALNUMBER | >< | msdyn_isphysicalinventoryenabledforsn
ISPHYSICALINVENTORYENABLEDFORBATCHNUMBER | >< | msdyn_isphysicalinventoryenabledforbn
ISFINANCIALINVENTORYENABLEDFORSERIALNUMBER | >< | msdyn_isfinancialinventoryenabledforsn
ISFINANCIALINVENTORYENABLEDFORBATCHNUMBER | >< | msdyn_isfinancialinventoryenabledforbn
ISCOVERAGEPLANENABLEDFORSERIALNUMBER | >< | msdyn_iscoverageplanenabledforserialnumber
ISCOVERAGEPLANENABLEDFORBATCHNUMBER | >< | msdyn_iscoverageplanenabledforbatchnumber
ISBLANKRECEIPTALLOWEDFORSERIALNUMBER | >< | msdyn_isblankreceiptallowedforserialnumber
ISBLANKRECEIPTALLOWEDFORBATCHNUMBER | >< | msdyn_isblankreceiptallowedforbatchnumber
ISBLANKISSUEALLOWEDFORSERIALNUMBER | >< | msdyn_isblankissueallowedforserialnumber
ISBLANKISSUEALLOWEDFORBATCHNUMBER | >< | msdyn_isblankissueallowedforbatchnumber
ISBATCHNUMBERACTIVE | >< | msdyn_isbatchnumberactive
ISINVENTORYOWNERACTIVE | >< | msdyn_isinventoryowneractive

### <a name="product-storage-dimension-group"></a>Víddarflokkur afurðageymslu

Víddarhópur afurðageymslu táknar aðferðina sem notuð er til að skilgreina staðsetningu afurðarinnar í vöruhúsinu. Þessar eru fáanlegar í Common Data Service með eftirfarandi vörpunum. 

Upprunasvæði | Gerð vörpunar | Áfangasvæði
---|---|---
WILLSALESPRICESEARCHUSEWAREHOUSE | >< | msdyn_willsalespricesearchusewarehouse
WILLSALESPRICESEARCHUSESITE | >< | msdyn_willsalespricesearchusesite
WILLSALESPRICESEARCHUSEINVENTORYSTATUS | >< | msdyn_willsalespricesearchuseinventorystatus
WILLPURCHASEPRICESEARCHUSEWAREHOUSE | >< | msdyn_willpurchasepricesearchusewarehouse
WILLPURCHASEPRICESEARCHUSESITE | >< | msdyn_willpurchasepricesearchusesite
WILLPURCHASEPRICESEARCHUSEINVENTORYSTATUS | >< | msdyn_willpurchpricesearchuseinventstatus
WILLCOVERAGEPLANNINGUSEWAREHOUSE | >< | msdyn_willcoverageplanusewarehouse
WILLCOVERAGEPLANNINGUSELOCATION | >< | msdyn_iscoverageplanenabledforlocation
WILLCOVERAGEPLANNINGUSEINVENTORYSTATUS | >< | msdyn_willcoverageplanuseinventorystatus
AREADVANCEDWAREHOUSEMANAGEMENTPROCESSESENABLED | >< | msdyn_areadvancedwmprocessesenabled
ISWAREHOUSEPRIMARYSTORAGEDIMENSION | >< | msdyn_iswarehouseprimarystoragedimension
ISWAREHOUSEMANDATORY | >< | msdyn_iswarehousemandatory
ISPHYSICALINVENTORYENABLEDFORWAREHOUSE | >< | msdyn_isphysicalinventoryenabledforwarehouse
ISPHYSICALINVENTORYENABLEDFORLOCATION | >< | msdyn_isphysicalinventoryenabledforlocation
ISLOCATIONACTIVE | >< | msdyn_islocationactive
ISFINANCIALINVENTORYENABLEDFORWAREHOUSE | >< | msdyn_isfinancialinventoryenabledforwarehouse
GROUPNAME | = | msdyn_groupname
GROUPDESCRIPTION | = | msdyn_groupdescription
ISBLANKRECEIPTALLOWEDFORLOCATION | >< | msdyn_isblankreceiptallowedforlocation
ISBLANKISSUEALLOWEDFORLOCATION | >< | msdyn_isblankissueallowedforlocation

