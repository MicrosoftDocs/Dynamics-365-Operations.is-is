---
title: Sameinuð vöruupplifun
description: Þetta efni lýsir samþættingu afurðaupplýsinga milli forrita Finance and Operations og Common Data Service.
author: t-benebo
manager: AnnBe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 3c564d580d2743d8a80cdf5667b1f95e00736d60
ms.sourcegitcommit: afc43699c0edc4ff2be310cb37add2ab586b64c0
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/14/2020
ms.locfileid: "4000765"
---
# <a name="unified-product-experience"></a>Samræmd afurðaupplifun

[!include [banner](../../includes/banner.md)]

Þegar vistkerfi fyrirtækja samanstendur af Dynamics 365 forritum, svo sem Finance, Supply Chain Management og Sales, nota fyrirtæki þessi forrit oft til að fá upplýsingar um vöru. Þetta er vegna þess að þessi forrit bjóða upp á öfluga vöruinnviði ásamt háþróuðum verðlagningarhugtökum og nákvæmum birgðagögnum fyrir lagermagn. Fyrirtæki sem nota utanaðkomandi vörukerfisstjórnunarkerfi (PLM) til að afla vörugagna geta sett vörur úr forritum Finance and Operations í rásir í öðrum forritum Dynamics 365. Sameinuð vöruupplifunin færir samþætt vörugagnalíkan inn í Common Data Service, þannig að allir notendur forritsins þ.m.t. notendur Power Platform geta nýtt sér þau ríku vörugögn sem koma úr forritum Finance and Operations.

Hérna er vöruupplýsingamódelið úr Sales.

![Gagnamódel fyrir vörur í CE](media/dual-write-product-4.jpg)

Hérna er vöruupplýsingamódelið úr forritum Finance and Operations.

![Gagnamódel fyrir vörur í Finance and Operations](media/dual-write-products-5.jpg)

Þessi tvö afurðalíkön hafa verið samþætt í Common Data Service eins og sýnt er hér að neðan.

![Gagnamódel fyrir vörur í forritum Dynamics 365](media/dual-write-products-6.jpg)

Kortin með tvískiptum skrifum fyrir vörur hafa verið hönnuð til að streyma gögnum aðeins í eina átt, í nánast rauntíma úr forritum Finance and Operations til Common Data Service. Samt sem áður hafa vöruinnviðir verið opnaðir svo að hún verði tvíátta ef þess er krafist. Þó að hægt sé að sérsníða það er það á þína ábyrgð, þar sem Microsoft mælir ekki með þessari aðferð.

## <a name="templates"></a>Sniðmát

Afurðarupplýsingar innihalda allar upplýsingar sem tengjast vörunni og skilgreiningu hennar, svo sem afurðarvíddir eða mælingar og geymsluvíddir. Eins og meðfylgjandi tafla sýnir, er safn af einingakortum búið til til að samstilla vörur og tengdar upplýsingar.

Finance and Operations-smáforrit | Önnur Dynamics 365 forrit | lýsing
-----------------------|--------------------------------|---
Útgefnar afurðir V2 | msdyn\_sharedproductdetails | Einingin **msdyn\_sharedproductdetails** inniheldur reitina úr forritum Finance and Operations sem skilgreina afurðina og innihalda fjárhags- og stjórnunarupplýsingar afurðarinnar. 
Common Data Service útgefnar einkvæmar afurðir | Afurð | Einingin **Afurð** inniheldur reitina sem skilgreina afurðina. Hún felur í sér einstakar afurðir (afurðir með undirgerðaafurð) og afurðarafbrigðin. Eftirfarandi tafla sýnir vörpun.
Afurðarnúmer sem eru auðkennd með strikamerki | msdyn\_productbarcodes | Strikamerki afurða eru notuð til að bera kennsl á afurðir á einkvæman hátt.
Sjálfgefnar pöntunarstillingar | msdyn\_productdefaultordersettings
Sjálfgefnar afurðatengdar pöntunarstillingar | msdyn_productdefaultordersettings
Afurðavíddaflokkar | msdyn\_productdimensiongroups | Afurðavíddarhópurinn skilgreindi hvaða afurðavíddir skilgreina vöruna. 
Geymsluvíddarflokkar | msdyn\_productstoragedimensiongroups | Víddarhópur afurðageymslu táknar aðferðina sem notuð er til að skilgreina staðsetningu afurðarinnar í vöruhúsinu.
Rakningarvíddarflokkar | msdyn\_producttrackingdimensiongroups | Víddarflokkur afurðarakningar táknar aðferðina sem notuð er til að rekja afurðina í birgðum.
Litir | msdyn\_productcolors
Stærðir | msdyn\_productsizes
Stílar | msdyn\_productsytles
Skilgreiningar | msdyn\_productconfigurations
Litir afurðarsniðmáts. | msdyn_sharedproductcolors | Einingin **Sameiginlegur afurðalitur** gefur til kynna liti sem sérstakt afurðarsniðmát getur haft. Þetta hugtak er flutt í Common Data Service til að halda gögnum samkvæmum.
Stærðir afurðarsniðmáts | msdyn_sharedproductsizes | Einingin **Sameiginleg afurðastærð** gefur til kynna stærðir sem sérstakt afurðarsniðmát getur haft. Þetta hugtak er flutt í Common Data Service til að halda gögnum samkvæmum.
Stílar afurðarsniðmáts | msdyn_sharedproductstyles | Einingin **Sameiginlegur afurðastíll** gefur til kynna stíla sem sérstakt afurðarsniðmát getur haft. Þetta hugtak er flutt í Common Data Service til að halda gögnum samkvæmum.
Skilgreiningar afurðarsniðmáts | msdyn_sharedproductconfigurations | Einingin **Sameiginleg skilgreining afurða** gefur til kynna skilgreiningar sem sérstakt afurðarsniðmát getur haft. Þetta hugtak er flutt í Common Data Service til að halda gögnum samkvæmum.
Allar afurðir | msdyn_globalproducts | Einingin fyrir allar afurðir inniheldur allar afurðir sem eru í boði í forritum Finance and Operations, bæði útgefnar afurðir og afurðir sem ekki eru gefnar út.
Eining | uoms
Umreikningur eininga | msdyn_ unitofmeasureconversions
Afurðatengd umskráning mælieiningar | msdyn_productspecificunitofmeasureconversion
Afurðartegundir | msdyn_productcategories | Hver vöruflokkur og upplýsingar um uppbyggingu hans og einkenni eru að finna í vöruflokkseiningunni. 
Tegundastigveldi afurðar | msdyn_productcategoryhierarhies | Stigveldi afurðar eru notuð til að flokka eða flokka afurðir. Flokkastigveldin eru fáanleg í Common Data Service með því að nota einingu tegundastigveldi afurðar. 
Hlutverk tegundastigveldis afurðar | msdyn_productcategoryhierarchies | Hægt er að nota vöruveldi fyrir mismunandi hlutverk í D365 Finance and Operations. Þau tilgreina hvaða flokkur er notaður í hverju hlutverki hlutverkaeiningar afurðaflokks er notaður. 
Úthlutanir afurðategundar | msdyn_productcategoryassignments | Til að úthluta vöru í flokk er hægt að nota eininguna fyrir vöruflokkaúthlutanir.

## <a name="integration-of-products"></a>Samþætting á afurðum

Í þessu líkani er varan táknuð með samsetningu tveggja aðila í Common Data Service: **Vara** og **msdyn\_sharedproductdetails**. Fyrri einingin hefur að geyma skilgreininguna á vöru (einstaka auðkenni fyrir vöruna, vöruheitið og lýsinguna), en önnur aðilinn inniheldur reitina sem eru geymdir á afurðastigi. Samsetning þessara tveggja aðila er notuð til að skilgreina afurðina í samræmi við hugtakið lagerhaldseining (SKU). Hver afurð sem gefin er út verður að hafa upplýsingar sínar í umræddum einingum (Upplýsingar um afurð og samnýtta afurð) Til að fylgjast með öllum afurðum (gefnar út og ekki gefnar út) er einingin **Altækar afurðir** notuð. 

Þar sem varan er táknuð sem SKU er hægt að fanga hugtökin aðgreindar vörur, vörumeistarar og afbrigði afurða í Common Data Service á eftirfarandi hátt:

- **Afurðir með undirgerð afurðar** eru afurðir sem eru skilgreindar af sjálfum sér. Engar víddir þarf að skilgreina. Dæmi er sérstök bók. Fyrir þessar afurðir er ein skrá búin til í einingunni **Afurð** , og ein skrá er búin til í einingunni **msdyn\_sharedproductdetails**. Engin skrá afurðafjölskyldu er búin til.
- **Afurðarsniðmát** eru notuð sem almennar afurðir sem innihalda skilgreininguna og reglur sem ákvarða hegðun í viðskiptaferlum. Samkvæmt þessum skilgreiningum er hægt að búa til sérstakar afurðir sem eru þekktar sem vöruafbrigði. Sem dæmi má nefna að stuttermabolur er afurðasniðmát og hann getur haft lit og stærð sem víddir. Hægt er að losa afbrigði sem hafa mismunandi samsetningar af þessum víddum, eins og litlum bláum stuttermabol eða meðalstórum grænum stuttermabol. Í samþættingunni er ein skrá á hvert afbrigði búin til í afurðatöflunni. Þessi skrá inniheldur upplýsingar um afbrigði, eins og mismunandi víddir. Almennar upplýsingar um vöruna eru geymdar í einingunni **msdyn\_sharedproductdetails**. (Þessar almennu upplýsingar eru geymdar í afurðarsniðmátinu.) Upplýsingar afurðarsniðmáts eru samstilltar við Common Data Service um leið og útgefið afurðarsniðmát er búið til (en áður en afbrigði eru losuð).
- **Einkvæmar afurðir** vísa til allra undirgerðaafurða afurðanna og allra afurðaafbrigðanna. 

![Gagnamódel fyrir afurðir](media/dual-write-product.png)

Með tvíritunarvirkni virkjaða verða vörur úr Finance and Operations samstilltar í öðrum Dynamics 365 vörum í stöðunni **Drög**. Þeim er bætt við fyrstu verðskrána með sama gjaldmiðil. Með öðrum orðum, þeim er bætt við fyrstu verðskrána í forriti Dynamics 365 sem samsvarar gjaldmiðli lögaðila þíns þar sem varan er gefin út í forriti Finance and Operations. 

Sjálfgefið er að vörur úr forritum Finance and Operations eru samstilltar við önnur Dynamics 365 forrit með stöðuna **Drög**. Til að samstilla vöruna við stöðuna **Virkt** , svo að þú getir til dæmis notað hana beint í sölupöntunartilboðum þarf að velja eftirfarandi stillingu: **Kerfið> Stjórnun> Kerfisstjórnun> Kerfisstillingar> Sala** og velja **Stofna vörur í virkri stöðu = já**. 

Athugaðu að samstilling vara fer fram úr forritum Finance and Operations í Common Data Service. Þetta þýðir að hægt er að breyta reitum afurðaeiningar í Common Data Service, en þegar samstillingu er hrundið af stað (þegar afurðareit er breytt í forriti Finance and Operations) mun þetta skrifa yfir gildin í Common Data Service. 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [products](includes/EcoResReleasedDistinctProductCDSEntity-products.md)]

[!include [product details](includes/EcoResReleasedProductV2-msdyn-sharedproductdetails.md)]

[!include [global products](includes/EcoResEveryProductEntity-msdyn-globalproducts.md)]

## <a name="product-dimensions"></a>Afurðarvíddir 

Afurðavíddir eru einkenni sem auðkenna afurðarafbrigði. Fjórar vöruvíddir (Litur, Stærð, Stíll og Stilling) er einnig varpað á Common Data Service til að skilgreina afbrigði afurða. Eftirfarandi mynd sýnir gagnalíkanið fyrir afurðavíddina Litur. Sama líkani er beitt á stærðir, stíl og stillingar. 

![Gangalíkan fyrir afurðavíddir](media/dual-write-product-two.png)

[!include [product colors](includes/EcoResProductColorEntity-msdyn-productcolor.md)]

[!include [product sizes](includes/EcoResProductSizeEntity-msdyn-productsizes.md)]

[!include [product sizes](includes/EcoResProductStyleEntity-msdyn-productstyles.md)]

[!include [product sizes](includes/EcoResProductConfigurationsEntity-msdyn-productconfigurations.md)]

Þegar afurð hefur mismunandi afurðavíddir (til dæmis hefur afurðarsniðmát stærð og lit sem afurðavíddir) er hver einkvæm afurð (það er hvert afurðarafbrigði) skilgreind sem samsetning þessara afurðavíddar. Til dæmis er afurðanúmer B0001 extra-lítill svartur bolur og afurðanúmer B0002 er lítill svartur bolur. Í þessu tilfelli eru núverandi samsetningar afurðavíddar skilgreindar. Bolurinn úr dæminu á undan getur til dæmis verið extra-lítill og svartur, lítill og svartur, meðalstór og svartur, eða stór og svartur, en hann getur ekki verið extra-stór og svartur. Með öðrum orðum eru afurðavíddir sem afurðarsniðmát getur notað tilgreindar og hægt er að gefa afbrigði út frá þessum gildum.

Til að halda utan um afurðavíddir sem afurðarsniðmát getur notað eru eftirfarandi einingar stofnaðar og varpað í Common Data Service fyrir hverja afurðavídd. Frekari upplýsingar eru í [Yfirlit afurðarupplýsinga](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/pim/product-information).

[!include [product colors](includes/EcoResProductMasterColorEntity-msdyn-sharedproductcolors.md)]

[!include [product sizes](includes/EcoResProductMasterSize-msdyn-sharedproductsizes.md)]

[!include [product styles](includes/EcoResProductMasterStyleEntity-msdyn-sharedproductstyles.md)]

[!include [product configurations](includes/EcoResProductMasterConfigurationEntity-msdyn-sharedproductconfigurations.md)]

[!include [product bar codes](includes/EcoResProductNumberIdentifiedBarcode-msdyn-productbarcodes.md)]

## <a name="default-order-settings-and-product-specific-default-order-settings"></a>Sjálfgefnar pöntunarstillingar og afurðatengdar sjálfgefnar pöntunarstillingar

Sjálfgefið pöntunarstillingar skilgreina svæði og vöruhús þar sem afurðir verða upprunnin frá eða geymdar, í lágmarks, hámarks, margar og staðlaðs magns sem verða notuð fyrir viðskipti eða birgðastjórnun, afhendingartíma, stöðvunarflagg, og aðferðina pöntun lofað. Þessar upplýsingar eru aðgengilegar í Common Data Service með því að nota sjálfgefnu pöntunarstillingarnar og afurðatengda sjálfgefnr pöntunarstillingaeiningu. Þú getur lesið frekari upplýsingar um virkni í efninu [Sjálfgefnar pöntunarstillingar](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/default-order-settings).

[!include [product sizes](includes/InventProductDefaultOrderSettingsEntity-msdyn-productdefaultordersetting.md)]

[!include [product sizes](includes/InventProductSpecificOrderSettingsV2Entity-msdyn-productspecificdefaultordersetting.md)]

## <a name="unit-of-measure-and-unit-of-measure-conversions"></a>Mælieining og umreikningur á mælieiningum viðskipta

Mælieiningarnar og umreikningur á þeim eru aðgengilegar í Common Data Service eftir gagnalíkaninu sem sýnt er á myndinni.

![Gagnalíkan fyrir mælieiningu](media/dual-write-product-three.png)

Mælieiningin er samþætt á milli forrita Finance and Operations og annarra forrita Dynamics 365. Fyrir hvern einingaflokk í forriti Finance and Operations er einingahópur búinn til í forriti Dynamics 365, sem hefur að geyma einingar sem tilheyra einingaflokknum. Sjálfgefin grunneining er einnig búin til fyrir hvern einingahóp. 

[!include [unit of measure](includes/UnitOfMeasureEntity-uom.md)]

[!include [unit of measure conversions](includes/UnitOfMeasureConversionEntity-msdyn-unitofmeasureconversions.md)]

[!include [product-specific unit of measure conversions](includes/EcoResProductSpecificUnitConversionEntity-msdyn-productspecificunitofmeasureconversions.md)]

## <a name="initial-synchronization-of-units-data-matching-between-finance-and-operations-and-common-data-service"></a>Upphafleg samstilling á samsvörun einingagagna á milli Finance and Operations og Common Data Service

### <a name="initial-synchronization-of-units"></a>Upphafleg samstilling á einingum

Þegar tvöföld skrift er virkjuð eru eininar úr Finance and Operations samstilltar við önnur Dynamics 365 forrit. Einingahóparnir sem eru samstilltir úr forritum Finance and Operations í Common Data Service eru með fánasett sem gefur til kynna að þeir séu „utanhúss“.

### <a name="matching-units-and-unit-classesgroups-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>Samsvarandi einingar og gögn mælieiningaflokka/flokkar gögn úr Finance and Operations og öðrum Dynamics 365 forritum

Í fyrsta lagi er mikilvægt að hafa í huga að samstillingarlykillinn fyrir eininguna er msdyn_symbol. Þess vegna verður þetta gildi að vera einstakt í Common Data Service eða öðrum Dynamics 365 forritum. Þar sem að í öðrum Dynamics 365 forritum er það parið „Kenni einingahóps“ og „Heiti“ sem skilgreinir sérstöðu einingar þarft þú að huga að mismunandi aðstæðum fyrir samsvarandi einingagögn á milli forrita Finance and Operations og Common Data Service.

Fyrir samsvarandi/skarandi einingar í forritum Finance and Operations og öðrum Dynamics 365 forritum:

+ **Einingin tilheyrir einingahópi í öðrum Dynamics 365 forritum sem samsvarar tengdum einingaflokki í forritum Finance and Operations**. Í þessu tilfelli verður að fylla út svæðið msdyn_symbol í öðrum Dynamics 365 forritum með einingartákninu úr forritum Finance and Operations. Þess vegna, þegar gögnin verða jöfnuð og einingahópurinn stilltur sem „Utanaðkomandi viðhald“ í öðrum Dynamics 365 forritum.
+ **Einingin tilheyrir einingahópi í öðrum Dynamics 365 forritum sem samsvarar ekki tilheyrandi einingaflokki í forritum Finance and Operations (engin núverandi einingaflokkur í forritum Finance and Operations fyrir einingaflokkinn í öðrum Dynamics 365 forritum).** Í þessu tilfelli verður að fylla út msdyn_symbol með streng af handahófi. Athugaðu að þetta gildi verður að vera einstakt í öðrum Dynamics 365 forritum.

Fyrir einingar og einingaflokka í Finance and Operations sem eru ekki til í öðrum Dynamics 365 forritum:

Sem hluti af tvískrifun eru einingarhóparnir úr forritum Finance and Operations og samsvarandi einingar stofnaðar og samstilltar í öðrum Dynamics 365 forritum og Common Data Service og einingahópurinn verður stilltur sem „Utanaðkomandi viðhald“. Ekki er þörf á neinu auka átaki fyrir ræsingu.

Fyrir einingar í öðrum forritum Dynamics 365 sem eru ekki til í forritum Finance and Operations:

Fyllt verður út reitinn msdyn_symbol fyrir allar einingar. Alltaf er hægt að búa til einingarnar í forritum Finance and Operations í samsvarandi einingaflokki (ef þær eru til). Ef einingaflokkur er ekki til verður fyrst að búa til einingaflokkinn (athugaðu að þú getur ekki búið til einingaflokk í forritum Finance and Operations nema í gegnum viðbót ef þú ert að lengja enum) sem samsvarar hinum Dynamics 365 forritseiningahópnum. Síðan er hægt að stofna eininguna. Athugaðu að einingatáknið í Finance and Operations verður að vera msdyn_symbol sem var áður tilgreint í öðrum Dynamics 365 forritum fyrir eininguna.

## <a name="product-policies-dimension-tracking-and-storage-groups"></a>Afurðastefna: vídd, mælingar og geymsluhópar

Afurðareglurnar eru reglur sem notaðar eru til að skilgreina afurðir og eiginleika þeirra í birgðum. Hægt er að finna afurðavíddarhópinn, afurðarakningarvíddarhópinn og geymsluvíddarhópinn sem afurðareglur. 

[!include [product dimension group](includes/EcoResProductDimensionGroup-msdyn-productdimensiongroups.md)]

[!include [product tracking dimension group](includes/EcoResTrackingDimensionGroup-msdyn-producttrackingdimensiongroups.md)]

[!include [product storage dimension group](includes/EcoResStorageDimensionGroup-msdyn-productstoragedimensiongroups.md)]

## <a name="product-hierarchies"></a>Afurðarstigveldi

[!include [product category hierarchy](includes/EcoResProductCategoryHierarchyEntity-msdyn-productcategoryhierarchy.md)]

[!include [product category](includes/EcoResProductCategoryEntity-msdyn-productcategory.md)]

[!include [product category assignments](includes/EcoResProductCategoryAssignmentEntity-msdyn-productcategoryassignment.md)]

[!include [product category role](includes/EcoResProductCategoryHierarchyRoleEntity-msdyn-productcategoryhierarchyrole.md)]


## <a name="integration-key-for-products"></a>Sameiningartakki fyrir vörur 

Til að auðkenna vörur á milli Dynamics 365 for Finance and Operations og vörur í Common Data Service eru samstillingarlyklarnir notaðir. Fyrir afurðir er **(productnumber)** einkvæmur lykill sem auðkennir afurð í Common Data Service. Hann er samsettur með samtengingu á: **(company, msdyn_productnumber)**. **Fyrirtækið** gefur til kynna lögaðila í Finance and Operations og **msdyn_productnumber** sýnir vörunúmer fyrir tiltekna vöru í Finance and Operations. 

Fyrir notendur Dynamics 365 forrits er afurðin auðkennd í UI með **msdyn_productnumber** (athugið að merki reitsins er **Vörunúmer** ). Á vöruforminu eru bæði fyrirtækið og msydn_productnumber sýnt. Hins vegar er reiturinn (productnumber), sem er einstakur lykill fyrir afurð, ekki sýndur. 

Ef þú byggir forrit á Common Data Service, ættir þú að passa að nota **productnumber** (einkvæmt afurðakenni) sem samþættingarlykill. Ekki nota **msdyn_productnumber** þar sem það er ekki einkvæmt. 

## <a name="initial-synchronization-of-products-and-migration-of-data-from-common-data-service-to-finance-and-operations"></a>Upphafleg samstilling vöru og flutningur gagna úr Common Data Service í Finance and Operations

### <a name="initial-synchronization-of-products"></a>Upphafleg samstilling á afurðum 

Þegar tvöföld skrift er virkjuð eru afurðir úr forritum Finance and Operations samstilltar við Common Data Service og önnur líkanadrifin forrit Dynamics 365. Afurðir stofnaðar í Common Data Service og öðrum forritum Dynamics 365 áður en tvöfaldri ritun var gefin út verða ekki uppfærðar eða jafnaðar við afurðaögn úr forritum Finance and Operations.

### <a name="matching-product-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>Samsvarandi vörugögn úr Finance and Operations og öðrum Dynamics 365 forritum

Ef sömu vörur eru geymdar (skarast/samsvara) í Finance and Operations og í Common Data Service og öðrum forritum Dynamics 365, þegar gert er ráð fyrir tvíritun samstillingar vara úr Finance and Operations, og afritaskrár munu birtast í Common Data Service fyrir sömu vöru.
Til að forðast fyrri aðstæður, ef önnur Dynamics 365 forrit hafa vörur sem skarast/samsvara við Finance and Operations, verður stjórnandi sem gerir kleift að nota tvískipt ræsingu reitina **Fyrirtæki** (dæmi: "USMF") og **msdyn_productnumber** (dæmi: "1234:Svartur:S") áður en samstilling vara fer fram. Með öðrum orðum, þessa tvo reiti í afurðinni í Common Data Service þarf að fylla út með viðkomandi fyrirtæki í Finance and Operations sem þarf að passa við vöruna og með vörunúmeri hennar. 

Þegar samstillingin er virk og fer fram verða vörur úr Finance and Operations samstilltar við samsvarandi vörur í Common Data Service og önnur Dynamics 365 forrit. Þetta á bæði við um einkvæmar afurðir og afbrigði afurða. 


### <a name="migration-of-product-data-from-other-dynamics-365-apps-to-finance-and-operations"></a>Flutningur á afurðagögnum úr öðrum Dynamics 365 forritum í Finance and Operations

Ef önnur Dynamics 365 forrit eru með vörur sem eru ekki til staðar í Finance and Operations, getur kerfisstjórinn fyrst notað **EcoResReleasedProductCreationV2Entity** til að flytja inn þessar vörur í Finance and Operations. Og í öðru lagi skal jafna afurðagögnin úr Finance and Operations og önnur Dynamics 365 forrit eins og lýst er hér að ofan. 
