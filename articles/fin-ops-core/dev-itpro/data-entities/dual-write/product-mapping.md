---
title: Sameinuð vöruupplifun
description: Þetta efni lýsir samþættingu afurðaupplýsinga milli forrita Finance and Operations og Dataverse.
author: t-benebo
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 3087ab8853b14308da9496eead7478822cec86b8
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750741"
---
# <a name="unified-product-experience"></a>Samræmd afurðaupplifun

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Þegar vistkerfi fyrirtækja samanstendur af Dynamics 365 forritum, svo sem Finance, Supply Chain Management og Sales, nota fyrirtæki þessi forrit oft til að fá upplýsingar um vöru. Þetta er vegna þess að þessi forrit bjóða upp á öfluga vöruinnviði ásamt háþróuðum verðlagningarhugtökum og nákvæmum birgðagögnum fyrir lagermagn. Fyrirtæki sem nota utanaðkomandi vörukerfisstjórnunarkerfi (PLM) til að afla vörugagna geta sett vörur úr forritum Finance and Operations í rásir í öðrum forritum Dynamics 365. Sameinuð vöruupplifunin færir samþætt vörugagnalíkan inn í Dataverse, þannig að allir notendur forritsins þ.m.t. notendur Power Platform geta nýtt sér þau ríku vörugögn sem koma úr forritum Finance and Operations.

Hérna er vöruupplýsingamódelið úr Sales.

![Gagnamódel fyrir vörur í CE](media/dual-write-product-4.jpg)

Hérna er vöruupplýsingamódelið úr forritum Finance and Operations.

![Gagnamódel fyrir vörur í Finance and Operations](media/dual-write-products-5.jpg)

Þessi tvö afurðalíkön hafa verið samþætt í Dataverse eins og sýnt er hér að neðan.

![Gagnamódel fyrir vörur í forritum Dynamics 365](media/dual-write-products-6.jpg)

Töflukort með tvöfaldri skráningu fyrir afurðir eru hönnuð fyrir gagnaflæði í eina átt, nærri í rauntíma frá Finance and Operations -forritum til Dataverse. Samt sem áður hafa vöruinnviðir verið opnaðir svo að hún verði tvíátta ef þess er krafist. Þó að hægt sé að sérsníða það er það á þína ábyrgð, þar sem Microsoft mælir ekki með þessari aðferð.

## <a name="templates"></a>Sniðmát

Afurðarupplýsingar innihalda allar upplýsingar sem tengjast vörunni og skilgreiningu hennar, svo sem afurðarvíddir eða mælingar og geymsluvíddir. Eins og eftirfarandi tafla sýnir er búið að stofna safn af töflukortum til að samstilla afurðir og tengdar upplýsingar.

Finance and Operations-smáforrit | Önnur Dynamics 365 forrit | lýsing
-----------------------|--------------------------------|---
Útgefnar afurðir V2 | msdyn\_sharedproductdetails | Taflan **msdyn\_sharedproductdetails** inniheldur dálka úr forritum Finance and Operations sem skilgreina afurðina og innihalda fjárhags- og stjórnunarupplýsingar afurðarinnar. 
Dataverse útgefnar einkvæmar afurðir | Afurð | Taflan **Afurð** inniheldur dálkana sem skilgreina afurðina. Hún felur í sér einstakar afurðir (afurðir með undirgerðaafurð) og afurðarafbrigðin. Eftirfarandi tafla sýnir vörpun.
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
Litir afurðarsniðmáts. | msdyn_sharedproductcolors | Taflan **Sameiginlegur afurðalitur** gefur til kynna liti sem sérstakt afurðarsniðmát getur haft. Þetta hugtak er flutt í Dataverse til að halda gögnum samkvæmum.
Stærðir afurðarsniðmáts | msdyn_sharedproductsizes | Taflan **Sameiginleg afurðastærð** gefur til kynna stærðir sem sérstakt afurðarsniðmát getur haft. Þetta hugtak er flutt í Dataverse til að halda gögnum samkvæmum.
Stílar afurðarsniðmáts | msdyn_sharedproductstyles | Taflan **Sameiginlegur afurðastíll** gefur til kynna stíla sem sérstakt afurðarsniðmát getur haft. Þetta hugtak er flutt í Dataverse til að halda gögnum samkvæmum.
Skilgreiningar afurðarsniðmáts | msdyn_sharedproductconfigurations | Taflan **Sameiginleg skilgreining afurða** gefur til kynna skilgreiningar sem sérstakt afurðarsniðmát getur haft. Þetta hugtak er flutt í Dataverse til að halda gögnum samkvæmum.
Allar afurðir | msdyn_globalproducts | Taflan fyrir allar afurðir inniheldur allar afurðir sem eru í boði í forritum Finance and Operations, bæði útgefnar afurðir og afurðir sem ekki eru gefnar út.
Eining | uoms
Umreikningur eininga | msdyn_ unitofmeasureconversions
Afurðatengd umskráning mælieiningar | msdyn_productspecificunitofmeasureconversion
Afurðartegundir | msdyn_productcategories | Hver vöruflokkur og upplýsingar um uppbyggingu hans og einkenni eru að finna í vöruflokkstöflunni. 
Tegundastigveldi afurðar | msdyn_productcategoryhierarhies | Stigveldi afurðar eru notuð til að flokka eða flokka afurðir. Flokkastigveldin eru fáanleg í Dataverse með því að nota töflu tegundastigveldi afurðar. 
Hlutverk tegundastigveldis afurðar | msdyn_productcategoryhierarchies | Hægt er að nota vöruveldi fyrir mismunandi hlutverk í D365 Finance and Operations. Þau tilgreina hvaða flokkur er notaður í hverju hlutverki hlutverkatöflu afurðaflokks er notaður. 
Úthlutanir afurðategundar | msdyn_productcategoryassignments | Til að úthluta vöru í flokk er hægt að nota töfluna fyrir vöruflokkaúthlutanir.

## <a name="integration-of-products"></a>Samþætting á afurðum

Í þessu líkani er afurðin táknuð með samsetningu á tveimur töflum í Dataverse: **Afurð** og **msdyn\_samnýttar afurðarupplýsingar**. Fyrri taflan hefur að geyma skilgreininguna á vöru (einstaka auðkenni fyrir vöruna, vöruheitið og lýsinguna), en önnur taflan inniheldur dálkana sem eru geymdir á afurðastigi. Samsetning þessara tveggja taflna er notuð til að skilgreina afurðina í samræmi við hugtakið birgðahaldseining (BHE). Hver útgefin afurð er með upplýsingar í framangreindum töflum (afurð og samnýttar afurðaupplýsingar). Til að fylgjast með öllum afurðum (gefnar út og ekki gefnar út) er taflan **Altækar afurðir** notuð. 

Þar sem varan er táknuð sem SKU er hægt að fanga hugtökin aðgreindar vörur, vörumeistarar og afbrigði afurða í Dataverse á eftirfarandi hátt:

- **Afurðir með undirgerð afurðar** eru afurðir sem eru skilgreindar af sjálfum sér. Engar víddir þarf að skilgreina. Dæmi er sérstök bók. Fyrir þessar afurðir er ein lína búin til í töflunni **Afurð** og ein lína er búin til í töflunni **msdyn\_sharedproductdetails**. Engin lína afurðafjölskyldu er búin til.
- **Afurðarsniðmát** eru notuð sem almennar afurðir sem innihalda skilgreininguna og reglur sem ákvarða hegðun í viðskiptaferlum. Samkvæmt þessum skilgreiningum er hægt að búa til sérstakar afurðir sem eru þekktar sem vöruafbrigði. Sem dæmi má nefna að stuttermabolur er afurðasniðmát og hann getur haft lit og stærð sem víddir. Hægt er að losa afbrigði sem hafa mismunandi samsetningar af þessum víddum, eins og litlum bláum stuttermabol eða meðalstórum grænum stuttermabol. Í samþættingunni er ein lína á hvert afbrigði búin til í afurðatöflunni. Þessi lína inniheldur upplýsingar um afbrigði, eins og mismunandi víddir. Almennar upplýsingar um vöruna eru geymdar í töflunni **msdyn\_sharedproductdetails**. (Þessar almennu upplýsingar eru geymdar í afurðarsniðmátinu.) Upplýsingar afurðarsniðmáts eru samstilltar við Dataverse um leið og útgefið afurðarsniðmát er búið til (en áður en afbrigði eru losuð).
- **Einkvæmar afurðir** vísa til allra undirgerðaafurða afurðanna og allra afurðaafbrigðanna. 

![Gagnamódel fyrir afurðir](media/dual-write-product.png)

Með tvíritunarvirkni virkjaða verða vörur úr Finance and Operations samstilltar í öðrum Dynamics 365 vörum í stöðunni **Drög**. Þeim er bætt við fyrsta verðlistann með sama gjaldmiðil. Með öðrum orðum, þeim er bætt við fyrstu verðskrána í forriti Dynamics 365 sem samsvarar gjaldmiðli lögatöflunnar þinnar þar sem varan er gefin út í forriti Finance and Operations. Ef engin verðlisti er til staðar fyrir tiltekinn gjaldmiðil verður verðlisti sjálfkrafa búinn til og afurðinni verður úthlutað á hann. 

Núverandi innleiðing á viðbótum tvöfaldrar skráningar sem tengir sjálfgefinn verðlista við uppflettieininguna fyrir gjaldmiðilinn sem tengist Finance and Operations-forritinu og finnur fyrsta verðlistann í forriti viðskiptavinar með því að nota stafrófsröð á heiti verðlistans. Til að stilla sjálfgefinn verðlista fyrir tiltekinn gjaldmiðil þegar margir verðlistar eru til fyrir þann gjaldmiðil þarf að uppfæra heiti verðlistans í heiti sem kemur á undan öllum öðrum verðlistum í stafrófsröð fyrir þennan sama gjaldmiðil.

Sjálfgefið er að vörur úr forritum Finance and Operations eru samstilltar við önnur Dynamics 365 forrit með stöðuna **Drög**. Til að samstilla vöruna við stöðuna **Virkt**, svo að þú getir til dæmis notað hana beint í sölupöntunartilboðum þarf að velja eftirfarandi stillingu: **Kerfið> Stjórnun> Kerfisstjórnun> Kerfisstillingar> Sala** og velja **Stofna vörur í virkri stöðu = já**. 

Þegar afurðir eru samstilltar verður að færa inn gildi fyrir reitinn **Sölueining** í Finance and Operations-forritinu vegna þess að hann er áskilinn reitur í Sales.

Stofnun afurðafjölskyldna úr Dynamics 365 Sales er ekki studd með samstillingu tvöfaldrar skráningar fyrir afurðir.

Samstilling afurða gerist frá Finance and Operations-forritinu til Dataverse. Þetta þýðir að hægt er að breyta töfludálkinum afurðaeiningar í Dataverse, en þegar samstillingu er hrundið af stað (þegar afurðardálki er breytt í forriti Finance and Operations) mun þetta skrifa yfir gildin í Dataverse. 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [products](includes/EcoResReleasedDistinctProductCDSEntity-products.md)]

[!include [product details](includes/EcoResReleasedProductV2-msdyn-sharedproductdetails.md)]

[!include [global products](includes/EcoResEveryProductEntity-msdyn-globalproducts.md)]

## <a name="product-dimensions"></a>Afurðarvíddir 

Afurðavíddir eru einkenni sem auðkenna afurðarafbrigði. Fjórar vöruvíddir (Litur, Stærð, Stíll og Stilling) er einnig varpað á Dataverse til að skilgreina afbrigði afurða. Eftirfarandi mynd sýnir gagnalíkanið fyrir afurðavíddina Litur. Sama líkani er beitt á stærðir, stíl og stillingar. 

![Gangalíkan fyrir afurðavíddir](media/dual-write-product-two.png)

[!include [product colors](includes/EcoResProductColorEntity-msdyn-productcolor.md)]

[!include [product sizes](includes/EcoResProductSizeEntity-msdyn-productsizes.md)]

[!include [product sizes](includes/EcoResProductStyleEntity-msdyn-productstyles.md)]

[!include [product sizes](includes/EcoResProductConfigurationsEntity-msdyn-productconfigurations.md)]

Þegar afurð hefur mismunandi afurðavíddir (til dæmis hefur afurðarsniðmát stærð og lit sem afurðavíddir) er hver einkvæm afurð (það er hvert afurðarafbrigði) skilgreind sem samsetning þessara afurðavíddar. Til dæmis er afurðanúmer B0001 extra-lítill svartur bolur og afurðanúmer B0002 er lítill svartur bolur. Í þessu tilfelli eru núverandi samsetningar afurðavíddar skilgreindar. Bolurinn úr dæminu á undan getur til dæmis verið extra-lítill og svartur, lítill og svartur, meðalstór og svartur, eða stór og svartur, en hann getur ekki verið extra-stór og svartur. Með öðrum orðum eru afurðavíddir sem afurðarsniðmát getur notað tilgreindar og hægt er að gefa afbrigði út frá þessum gildum.

Til að halda utan um afurðavíddirnar sem afurðarsniðmát getur tekið, eru eftirfarandi töflur stofnaðar og kortlagðar í Dataverse fyrir hverja afurðarvídd. Frekari upplýsingar eru í [Yfirlit afurðarupplýsinga](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/pim/product-information).

[!include [product colors](includes/EcoResProductMasterColorEntity-msdyn-sharedproductcolors.md)]

[!include [product sizes](includes/EcoResProductMasterSize-msdyn-sharedproductsizes.md)]

[!include [product styles](includes/EcoResProductMasterStyleEntity-msdyn-sharedproductstyles.md)]

[!include [product configurations](includes/EcoResProductMasterConfigurationEntity-msdyn-sharedproductconfigurations.md)]

[!include [product bar codes](includes/EcoResProductNumberIdentifiedBarcode-msdyn-productbarcodes.md)]

## <a name="default-order-settings-and-product-specific-default-order-settings"></a>Sjálfgefnar pöntunarstillingar og afurðatengdar sjálfgefnar pöntunarstillingar

Sjálfgefið pöntunarstillingar skilgreina svæði og vöruhús þar sem afurðir verða upprunnin frá eða geymdar, í lágmarks, hámarks, margar og staðlaðs magns sem verða notuð fyrir viðskipti eða birgðastjórnun, afhendingartíma, stöðvunarflagg, og aðferðina pöntun lofað. Þessar upplýsingar eru aðgengilegar í Dataverse með því að nota sjálfgefnu pöntunarstillingarnar og afurðatengda sjálfgefnr pöntunarstillingaeiningu. Þú getur lesið frekari upplýsingar um virkni í efninu [Sjálfgefnar pöntunarstillingar](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/default-order-settings).

[!include [product sizes](includes/InventProductDefaultOrderSettingsEntity-msdyn-productdefaultordersetting.md)]

[!include [product sizes](includes/InventProductSpecificOrderSettingsV2Entity-msdyn-productspecificdefaultordersetting.md)]

## <a name="unit-of-measure-and-unit-of-measure-conversions"></a>Mælieining og umreikningur á mælieiningum viðskipta

Mælieiningarnar og umreikningur á þeim eru aðgengilegar í Dataverse eftir gagnalíkaninu sem sýnt er á myndinni.

![Gagnalíkan fyrir mælieiningu](media/dual-write-product-three.png)

Mælieiningin er samþætt á milli forrita Finance and Operations og annarra forrita Dynamics 365. Fyrir hvern einingaflokk í forriti Finance and Operations er einingahópur búinn til í forriti Dynamics 365, sem hefur að geyma einingar sem tilheyra einingaflokknum. Sjálfgefin grunneining er einnig búin til fyrir hvern einingahóp. 

[!include [unit of measure](includes/UnitOfMeasureEntity-uom.md)]

[!include [unit of measure conversions](includes/UnitOfMeasureConversionEntity-msdyn-unitofmeasureconversions.md)]

[!include [product-specific unit of measure conversions](includes/EcoResProductSpecificUnitConversionEntity-msdyn-productspecificunitofmeasureconversions.md)]

## <a name="initial-synchronization-of-units-data-matching-between-finance-and-operations-and-dataverse"></a>Upphafleg samstilling á samsvörun einingagagna á milli Finance and Operations og Dataverse

### <a name="initial-synchronization-of-units"></a>Upphafleg samstilling á einingum

Þegar tvöföld skrift er virkjuð eru eininar úr Finance and Operations samstilltar við önnur Dynamics 365 forrit. Einingahóparnir sem eru samstilltir úr forritum Finance and Operations í Dataverse eru með fánasett sem gefur til kynna að þeir séu „utanhúss“.

### <a name="matching-units-and-unit-classesgroups-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>Samsvarandi einingar og gögn mælieiningaflokka/flokkar gögn úr Finance and Operations og öðrum Dynamics 365 forritum

Í fyrsta lagi er mikilvægt að hafa í huga að samstillingarlykillinn fyrir eininguna er msdyn_symbol. Þess vegna verður þetta gildi að vera einstakt í Dataverse eða öðrum Dynamics 365 forritum. Þar sem að í öðrum Dynamics 365 forritum er það parið „Kenni einingahóps“ og „Heiti“ sem skilgreinir sérstöðu einingar þarft þú að huga að mismunandi aðstæðum fyrir samsvarandi einingagögn á milli forrita Finance and Operations og Dataverse.

Fyrir samsvarandi/skarandi einingar í forritum Finance and Operations og öðrum Dynamics 365 forritum:

+ **Einingin tilheyrir einingahópi í öðrum Dynamics 365 forritum sem samsvarar tengdum einingaflokki í forritum Finance and Operations**. Í þessu tilfelli verður að fylla út dálkinn msdyn_symbol í öðrum Dynamics 365 forritum með einingartákninu úr forritum Finance and Operations. Þess vegna, þegar gögnin verða jöfnuð og einingahópurinn stilltur sem „Utanaðkomandi viðhald“ í öðrum Dynamics 365 forritum.
+ **Einingin tilheyrir einingahópi í öðrum Dynamics 365 forritum sem samsvarar ekki tilheyrandi einingaflokki í forritum Finance and Operations (engin núverandi einingaflokkur í forritum Finance and Operations fyrir einingaflokkinn í öðrum Dynamics 365 forritum).** Í þessu tilfelli verður að fylla út msdyn_symbol með streng af handahófi. Athugaðu að þetta gildi verður að vera einstakt í öðrum Dynamics 365 forritum.

Fyrir einingar og einingaflokka í Finance and Operations sem eru ekki til í öðrum Dynamics 365 forritum:

Sem hluti af tvískrifun eru einingarhóparnir úr forritum Finance and Operations og samsvarandi einingar stofnaðar og samstilltar í öðrum Dynamics 365 forritum og Dataverse og einingahópurinn verður stilltur sem „Utanaðkomandi viðhald“. Ekki er þörf á neinu auka átaki fyrir ræsingu.

Fyrir einingar í öðrum forritum Dynamics 365 sem eru ekki til í forritum Finance and Operations:

Fyllt verður út dálkinn msdyn_symbol fyrir allar einingar. Alltaf er hægt að búa til einingarnar í forritum Finance and Operations í samsvarandi einingaflokki (ef þær eru til). Ef einingaflokkur er ekki til verður fyrst að búa til einingaflokkinn (athugaðu að þú getur ekki búið til einingaflokk í forritum Finance and Operations nema í gegnum viðbót ef þú ert að lengja enum) sem samsvarar hinum Dynamics 365 forritseiningahópnum. Síðan er hægt að stofna eininguna. Athugaðu að einingatáknið í Finance and Operations verður að vera msdyn_symbol sem var áður tilgreint í öðrum Dynamics 365 forritum fyrir eininguna.

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

Til að auðkenna vörur á milli Dynamics 365 for Finance and Operations og vörur í Dataverse eru samstillingarlyklarnir notaðir. Fyrir afurðir er **(productnumber)** einkvæmur lykill sem auðkennir afurð í Dataverse. Hann er samsettur með samtengingu á: **(company, msdyn_productnumber)**. **Fyrirtækið** gefur til kynna lögaðila í Finance and Operations og **msdyn_productnumber** sýnir vörunúmer fyrir tiltekna vöru í Finance and Operations. 

Fyrir notendur Dynamics 365 forrits er afurðin auðkennd í UI með **msdyn_productnumber** (athugið að merki dálksins er **Vörunúmer**). Á vöruforminu eru bæði fyrirtækið og msydn_productnumber sýnt. Hins vegar er dálkurinn (productnumber), sem er einstakur lykill fyrir afurð, ekki sýndur. 

Ef þú byggir forrit á Dataverse, ættir þú að passa að nota **productnumber** (einkvæmt afurðakenni) sem samþættingarlykill. Ekki nota **msdyn_productnumber** þar sem það er ekki einkvæmt. 

## <a name="initial-synchronization-of-products-and-migration-of-data-from-dataverse-to-finance-and-operations"></a>Upphafleg samstilling vöru og flutningur gagna úr Dataverse í Finance and Operations

### <a name="initial-synchronization-of-products"></a>Upphafleg samstilling á afurðum 

Þegar tvöföld skráning er virkjuð eru afurðir úr forritum Finance and Operations samstilltar við Dataverse og forrit viðskiptavina. Afurðir stofnaðar í Dataverse og öðrum forritum Dynamics 365 áður en tvöfaldri ritun var gefin út verða ekki uppfærðar eða jafnaðar við afurðaögn úr forritum Finance and Operations.

### <a name="matching-product-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>Samsvarandi vörugögn úr Finance and Operations og öðrum Dynamics 365 forritum

Ef sömu vörur eru geymdar (skarast/samsvara) í Finance and Operations og í Dataverse og öðrum forritum Dynamics 365, þegar gert er ráð fyrir tvíritun samstillingar vara úr Finance and Operations, og tvöfaldar raðir munu birtast í Dataverse fyrir sömu vöru.
Til að forðast fyrri aðstæður, ef önnur Dynamics 365 forrit hafa vörur sem skarast/samsvara við Finance and Operations, verður stjórnandi sem gerir kleift að nota tvískipt ræsingu dálkama **Fyrirtæki** (dæmi: "USMF") og **msdyn_productnumber** (dæmi: "1234:Svartur:S") áður en samstilling vara fer fram. Með öðrum orðum, þessa tvo dálka í afurðinni í Dataverse þarf að fylla út með viðkomandi fyrirtæki í Finance and Operations sem þarf að passa við vöruna og með vörunúmeri hennar. 

Þegar samstillingin er virk og fer fram verða vörur úr Finance and Operations samstilltar við samsvarandi vörur í Dataverse og önnur Dynamics 365 forrit. Þetta á bæði við um einkvæmar afurðir og afbrigði afurða. 


### <a name="migration-of-product-data-from-other-dynamics-365-apps-to-finance-and-operations"></a>Flutningur á afurðagögnum úr öðrum Dynamics 365 forritum í Finance and Operations

Ef önnur Dynamics 365 forrit eru með vörur sem eru ekki til staðar í Finance and Operations, getur kerfisstjórinn fyrst notað **EcoResReleasedProductCreationV2Entity** til að flytja inn þessar vörur í Finance and Operations. Og í öðru lagi skal jafna afurðagögnin úr Finance and Operations og önnur Dynamics 365 forrit eins og lýst er hér að ofan. 


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
