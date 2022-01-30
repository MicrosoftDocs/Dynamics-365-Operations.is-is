---
title: Yfirlit afurðarupplýsinga
description: Í þessu efnisatriði er að finna upplýsingar um afurðastjórnun. Stjórnun afurðarupplýsinga nýtist með skilgreiningu á samnýttum afurðum, flokkun og auðkennum fyrir alla lögaðila og einnig tilteknar skilgreiningar afurðar þannig að þær passa vel í viðskiptaferla.
author: t-benebo
ms.date: 06/01/2017
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductListPage, EcoResProductVariantMaintainWorkspace, EcoResProductVariantPerCompanyImagePart, EcoResProductRelationType,EcoResProductAvailabilityPart,  EcoResProductReleasedSelect, EcoResProductLookup, EcoResProductVariantsPendingReleaseFormPart, EcoResProductSearchLookup, EcoResProductNumberRename, EcoResDimensionBasedConfigWorkspace, EcoResProductVariantImagePart, EcoResProductImagePart, EcoResProductVariantsPerCompanyPart, InventItemIdLookupByDefaultOrderSetting, EcoResProductReleaseSessions, EcoResProductVariantMaintainWorkspaceConfiguration, EcoResProductProcessManufacturingWorkspaceConfiguration, EcoResProductMasterVariantsPart, EcoResProductDiscreteManufacturingWorkspaceConfiguration, EcoResProductVariantAvailabilityPart, EcoResProductInformationFactBox, EcoResProductLookupTest, EcoResProductImageTest, EcoResProductReleasedRecentlyCreatedFormPart, EcoResPhysicalProductDimensions, PdsMRCRegulatedListItem, EcoResProductAvailabilityPart, PdsMRCRestrictionList, InventItemIdLookupAllocationId, EcoResProductAvailability, EcoResProductEntityAttributeTableFieldAssociation, EcoResProductImagePart, EcoResProductRelation, EcoResProductReleaseAddProduct, EcoResProductPerCompanyListPage, EcoResProductParameters, PdsMRCRestrictedItemByCountryState, EngChgCasePreview, InventTablePreview, PdsMRCItemDetails, EngChgCaseAssociate, PdsMRCCustomerHistory, PdsMRCVendorHistory, PdsMRCRestrictedCountryStateByItem, InventItemIdGroupLookup, InventLocationLookup, PdsMRCValidityIntervalbyCountry, PdsMRCValidityIntervalbyCountry, PdsMRCEventTracker, PdsMRCReportingCountry, PdsMRCDocument, PdsMRCReportingList, PdsMRCItemCAS, GraphicsTestForm, EngChgPicklist
audience: Application User
ms.reviewer: kamaybac
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bf814ec7c76ff2a8fd6bb4f7bbf8aec109465e34
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2022
ms.locfileid: "7984321"
---
# <a name="product-information-overview"></a>Yfirlit afurðarupplýsinga

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Í þessu efnisatriði er að finna upplýsingar um afurðastjórnun. Stjórnun afurðarupplýsinga nýtist með skilgreiningu á samnýttum afurðum, flokkun og auðkennum fyrir alla lögaðila og einnig tilteknar skilgreiningar afurðar þannig að þær passa vel í viðskiptaferla. 

Afurðarupplýsingar eru grundvöllur fyrir birgðakeðju og viðskiptaforrit í öllum greinum. Þær vísa til ferla og tækni þar sem lögð er áhersla á miðlæga stjórnun afurðaupplýsinga (til dæmis í birgðakeðju). Það er mikilvægt að samnýttar afurðaskilgreiningar, skjöl, eigindir og auðkenni séu notuð. Í ýmsum kerfum viðskiptalausna eru afurðaháðar upplýsingar og skilgreiningar nauðsynlegar til stýringar á viðskiptaferlum sem tengjast tilteknum afurðum, afurðafjölskyldum eða afurðaflokkum.

## <a name="product-definition"></a>Afurðarskilgreining

Afurð er fyrst og fremst skilgreind af afurðarnúmeri, heiti og lýsingu. Hins vegar þarf fleiri upplýsingar til að hægt sé að lýsa afurð eða þjónustu:

- Afurðargerð: Vara eða þjónusta
- Undirgerð afurðar: Einkvæmar afurðir eða afurðarsniðmát
- Skilgreining á afurðarafbrigðislíkani:

     - Afurðarvíddir og afurðaflokkar
     - Nafnakerfi afurðar
     - Afbrigðalíkön afurða

- Tengsl afurðarinnar við einn eða fleiri flokka
- Skilgreining á afurð og afurðategundum
- Myndir afurðar
- Viðhengi
- Mælieiningar og tengdir umreikningar
- Þýðingar fyrir öll nöfn og lýsingar

## <a name="distribution-export-and-import-of-product-data"></a>Dreifing, út- og innflutningur á afurðarupplýsingum

Afurðarskilgreiningu er hægt að stofna í Supply Chain Management. Einnig er hægt að sækja hana úr lífsferilsstjórnun afurðar, stjórnun afurðaupplýsinga eða upplýsingakerfum um afurðarstjórnun. Þegar fleiri en eitt tilvik af Supply Chain Management eru notuð er eitt tilvik yfirleitt notað sem afurðarsniðmát fyrir öll önnur tilvik. Þessi aðferð er studd af stóru safni gagnaeininga sem gera út- og innflutning mögulegan á afurðarskilgreiningargögnum úr einu tilviki í annað.

Til að styðja við dreifingu afurðargagna á mörg tilfelli, leyfir Supply Chain Management þér að nota Microsoft Dataverse. Afurðarskilgreiningu er hægt að stofna í frá tilviki í Supply Chain Management í Microsoft Dataverse. Afurðarskilgreining er þá hægt að nota til að úthluta öðrum viðskiptaferlum, t.d. Dynamics 365 Sales, með afurðargögnum.

Athugaðu að í kvikum og snörpum fyrirtækjum breytast afurðarupplýsingar daglega. Þess vegna er viðhald á réttum og áreiðanlegum afurðarupplýsingum mikilvægt viðskiptaferli eitt og sér.

## <a name="product-masters-and-product-variants"></a>Afurðarsniðmát og afurðarafbrigði

Í kvikum heimi, þar sem nauðsynlegt að er að vörur séu strax þróaðar að kröfum viðskiptavina, tilgreina afurðaskilgreiningar safn afurða í stað einkvæmra afurða. Í Supply Chain Management, eru þessar almennu afurðir þekktar sem *afurðarsniðmát*. Afurðarsniðmát hafa að geyma skilgreiningu og reglur sem tilgreina hvernig einkvæmum afurðum er lýst og hvernig þær hegða sér í viðskiptaferlum. Á grundvelli þessara skilgreininga er hægt að kalla fram einkvæmar afurðir. Þessar einkvæmu vörur kallast *afurðarafbrigði*.

Afurðarsniðmát er tengt við afurðavíddaflokk og skilgreiningartækni til að tilgreina viðskiptareglurnar. Afurðavíddir (litur, stærð, stíll og skilgreining) eru sértæk söfn eiginda sem hægt er að nota í hugbúnaðinum til að skilgreina og fylgjast með tiltekinni hegðun tengdra afurða. Þessar víddir hjálpa notendum einnig að leita að og auðkenna afurðirnar.

## <a name="configuration-technologies"></a>Skilgreiningartækni

Þú getur valið milli þrenns konar skilgreiningartækni:

- Fyrirframskilgreind afbrigði eru skilgreind af fyrirframskilgreindum afurðavíddum. Afurðarskilgreining felur í sér skilgreiningu á tiltekinni gildri víddasamsetningu, eins og lit, stíl og stærð. Hver samsetning myndar einkvæmt afurðarafbrigði.
- Víddaskilgreiningar eru vanalega notaðar við framleiðsluaðstæður og gera þér kleift að nota skilgreiningarvíddir í skilgreiningu á uppskriftum. Eftir að tiltekin skilgreining er valin notar kerfið undirsamstæðu af uppskriftarlínum sem eru gildar fyrir þá skilgreiningu til áætlunar og framleiðslu. Þetta hugtak nefnist líka *altæk uppskrift*, þar sem ein samnýtt uppskrift er notuð fyrir allar skilgreiningar afurðar.
- Skorðuskilgreining notast við afbrigðalíkan afurðar til að lýsa öllum mögulegum eiginleikum og þáttum sem þarf til að lýsa öllum mögulegum afbrigðum afurðar í einu líkani. Hægt er að lýsa skorðum samsetninga eiginda með reglulegum segðum eða töfluskorðum. Afbrigðalíkön og stillar verða sífellt mikilvægari í stjórnun afurðaupplýsinga og eru notuð í öllum greinum.

Þegar innleiðing á Supply Chain Management er áætluð er mjög mikilvægt að valin sé rétt skilgreiningartækni fyrir viðskiptaferli. Ekki er hægt að umbreyta afurð úr einu líkani í annað eftir innleiðingu.

## <a name="product-variant-model-definition-workspace"></a>Vinnusvæði skilgreiningar afurðarafbrigðislíkans

Vinnusvæðið **Skilgreining afurðarafbrigðislíkans** gefur yfirlit yfir afurðarsniðmát. Það sýnir líka stöðu á útgáfu sniðmáta og tengdra afbrigða til tiltekinna lögaðila.

## <a name="released-products"></a>Útgefnar afurðir

Afurðir sem eru útgefnar á tiltekinn lögaðila kallast *útgefnar afurðir*. Hægt er að gefa út vörur í magni á einn lögaðila eða á marga lögaðila á sama tíma. Þar sem það getur þurft að bæta við ýmsum eiginleikum og eigindum afurðarinnar á hvern lögaðila, gerir vinnusvæðið **Viðhald útgefinnar afurðar** þér kleift að fylgjast með og ljúka við nýlega útgefnar afurðir fyrir hvern lögaðila, eða í undirfyrirtækjum lögaðila.

### <a name="released-product-maintenance-workspace"></a>Vinnusvæði fyrir viðhald útgefinnar afurðar

Hægt er að skilgreina vinnusvæðið **Viðhald útgefinnar afurðar** í valmyndaratriðinu **Skilgreina eigið vinnusvæði**. Veldu tegundastigveldi og flokk til að sía vinnusvæðið eftir. Til að leiðrétta viðeigandi afurðagögn í vinnusvæðinu getur þú einnig skilgreint, í dögum, tímamörk fyrir **Nýlega útgefnar afurðir** og **Stöðvaðar útgefnar afurðir**.

Vinnusvæðið samanstendur af samanteknum reitum og tveimur listum. Listinn **Opin tilvik** sýnir tilvik afurðabreytinga sem hafa afurðir í völdu stigveldi afurðarflokks sem ekki er lokið og eru opnar. Listinn **Útgefið nýlega** sýnir afurðir sem hafa verið útgefnar innan þeirra tímamarka sem eru sett í skilgreiningu vinnusvæðisins. Fyrir hverja vöru á listanum er villuleit keyrð og staða hennar sýnd. Þessi staða gæti gefið til kynna að nauðsynlegri skilgreiningu fyrir lögaðilann sé ekki lokið. Af listanum getur þú fengið beinan aðgang að síðunum **Upplýsingar um losaðar afurðir**, **Viðhald afurðareiginda**, **Viðhald afurðarflokks**, **Sjálfgefnar pöntunarstillingar**, og **Textaþýðingar** til að ljúka við nauðsynlegar skilgreiningar afurðarinnar.

### <a name="manually-creating-a-new-released-product"></a>Handvirk stofnun á nýrri útgefinni afurð

Hægt er að stofna útgefna afurð í einni keyrslu, allt eftir viðskiptaferlum fyrirtækisins og þeim reglum sem gilda um hvort þessi virkni skuli notuð. Þessi virkni stofnar nýja afurð og gefur hana sjálfkrafa út til núverandi lögaðila. Til að stofna nýja afurð skaltu smella **Útgefnar afurðir** á vinnusvæðinu **Viðhald útgefinnar afurðar** eða á listasíðunni **Útgefin afurð**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]