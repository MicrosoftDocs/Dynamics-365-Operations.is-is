---
title: "Yfirlit afurðarupplýsinga"
description: "Í þessu efnisatriði er að finna upplýsingar um afurðastjórnun. Stjórnun afurðarupplýsinga nýtist með skilgreiningu á samnýttum afurðum, flokkun og auðkennum fyrir alla lögaðila og einnig tilteknar skilgreiningar afurðar þannig að þær passa vel í viðskiptaferla."
author: cvocph
manager: AnnBe
ms.date: 06/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductListPage, EcoResProductVariantMaintainWorkspace
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: 
ms.author: cvocph
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: db8a9666518b58b6b32bb4a14933095dd9416aa0
ms.contentlocale: is-is
ms.lasthandoff: 06/13/2017

---

# <a name="product-information-overview"></a>Yfirlit afurðarupplýsinga

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]

Í þessu efnisatriði er að finna upplýsingar um afurðastjórnun. Stjórnun afurðarupplýsinga nýtist með skilgreiningu á samnýttum afurðum, flokkun og auðkennum fyrir alla lögaðila og einnig tilteknar skilgreiningar afurðar þannig að þær passa vel í viðskiptaferla. 

Afurðarupplýsingar eru grundvöllur fyrir birgðakeðju og smásöluforrit í öllum greinum. Þær vísa til ferla og tækni þar sem lögð er áhersla á miðlæga stjórnun afurðaupplýsinga (til dæmis í birgðakeðju). Það er mikilvægt að samnýttar afurðaskilgreiningar, skjöl, eigindir og auðkenni séu notuð. Í ýmsum kerfum viðskiptalausna eru afurðaháðar upplýsingar og skilgreiningar nauðsynlegar til stýringar á viðskiptaferlum sem tengjast tilteknum afurðum, afurðafjölskyldum eða afurðaflokkum.

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

Hægt er að stofna skilgreiningu afurðar í Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition. Einnig er hægt að sækja hana úr lífsferilsstjórnun afurðar, stjórnun afurðaupplýsinga eða upplýsingakerfum um afurðarstjórnun. Þegar fleiri en eitt tilvik af Finance and Operations eru notuð er eitt tilvik yfirleitt notað sem afurðarsniðmát fyrir öll önnur tilvik. Þessi aðferð er studd af stóru safni gagnaeininga sem gera út- og innflutning mögulegan á afurðarskilgreiningargögnum úr einu tilviki í annað.

Finance and Operations leyfir þér að nota Common Data Service til að styðja við dreifingu afurðarupplýsinga í mörg tilvikum. Hægt er að flytja afurðarskilgreiningar úr einu tilviki Finance and Operations í Common Data Service. Síðan er hægt að nota afurðarskilgreiningar til að útvega öðrum viðskiptaforritum, eins og Microsoft Dynamics 365 for Sales, afurðarupplýsingar.

Athugaðu að í kvikum og snörpum fyrirtækjum breytast afurðarupplýsingar daglega. Þess vegna er viðhald á réttum og áreiðanlegum afurðarupplýsingum mikilvægt viðskiptaferli eitt og sér.

## <a name="product-masters-and-product-variants"></a>Afurðarsniðmát og afurðarafbrigði

Í kvikum heimi, þar sem nauðsynlegt að er að vörur séu strax þróaðar að kröfum viðskiptavina, tilgreina afurðaskilgreiningar safn afurða í stað einkvæmra afurða. Í Microsoft Dynamics 365 for Finance and Operations kallast þessar almennu afurðir *afurðarsniðmát*. Afurðarsniðmát hafa að geyma skilgreiningu og reglur sem tilgreina hvernig einkvæmum afurðum er lýst og hvernig þær hegða sér í viðskiptaferlum. Á grundvelli þessara skilgreininga er hægt að kalla fram einkvæmar afurðir. Þessar einkvæmu vörur kallast *afurðarafbrigði*.

Í Finance and Operations er afurðarsniðmát tengt við afurðavíddaflokk og skilgreiningartækni til að tilgreina viðskiptareglurnar. Afurðavíddir (litur, stærð, stíll og skilgreining) eru sértæk söfn eiginda sem hægt er að nota í hugbúnaðinum til að skilgreina og fylgjast með tiltekinni hegðun tengdra afurða. Þessar víddir hjálpa notendum einnig að leita að og auðkenna afurðirnar.

## <a name="configuration-technologies"></a>Skilgreiningartækni

Þú getur valið milli þrenns konar skilgreiningartækni:

- Fyrirframskilgreind afbrigði eru skilgreind af fyrirframskilgreindum afurðavíddum. Afurðarskilgreining felur í sér skilgreiningu á tiltekinni gildri víddasamsetningu, eins og lit, stíl og stærð. Hver samsetning myndar einkvæmt afurðarafbrigði.
- Víddaskilgreiningar eru vanalega notaðar við framleiðsluaðstæður og gera þér kleift að nota skilgreiningarvíddir í skilgreiningu á uppskriftum. Eftir að tiltekin skilgreining er valin notar kerfið undirsamstæðu af uppskriftarlínum sem eru gildar fyrir þá skilgreiningu til áætlunar og framleiðslu. Þetta hugtak nefnist líka *altæk uppskrift*, þar sem ein samnýtt uppskrift er notuð fyrir allar skilgreiningar afurðar.
- Skorðuskilgreining notast við afbrigðalíkan afurðar til að lýsa öllum mögulegum eiginleikum og þáttum sem þarf til að lýsa öllum mögulegum afbrigðum afurðar í einu líkani. Hægt er að lýsa skorðum samsetninga eiginda með reglulegum segðum eða töfluskorðum. Afbrigðalíkön og stillar verða sífellt mikilvægari í stjórnun afurðaupplýsinga og eru notuð í öllum greinum.

Þegar innleiðing á Finance and Operations er áætluð er mjög mikilvægt að valin sé rétt skilgreiningartækni fyrir viðskiptaferli. Ekki er hægt að umbreyta afurð úr einu líkani í annað eftir innleiðingu.

## <a name="product-variant-model-definition-workspace"></a>Vinnusvæði skilgreiningar afurðarafbrigðislíkans

Vinnusvæðið **Skilgreining afurðarafbrigðislíkans** gefur yfirlit yfir afurðarsniðmát. Það sýnir líka stöðu á útgáfu sniðmáta og tengdra afbrigða til tiltekinna lögaðila.

## <a name="released-products"></a>Útgefnar afurðir

Afurðir sem eru útgefnar á tiltekinn lögaðila kallast *útgefnar afurðir*. Hægt er að gefa út vörur í magni á einn lögaðila eða á marga lögaðila á sama tíma. Þar sem það getur þurft að bæta við ýmsum eiginleikum og eigindum afurðarinnar á hvern lögaðila, gerir vinnusvæðið **Viðhald útgefinnar afurðar** þér kleift að fylgjast með og ljúka við nýlega útgefnar afurðir fyrir hvern lögaðila, eða í undirfyrirtækjum lögaðila.

### <a name="released-product-maintenance-workspace"></a>Vinnusvæði fyrir viðhald útgefinnar afurðar

Hægt er að skilgreina vinnusvæðið **Viðhald útgefinnar afurðar** í valmyndaratriðinu **Skilgreina eigið vinnusvæði**. Veldu tegundastigveldi og flokk til að sía vinnusvæðið eftir. Til að leiðrétta viðeigandi afurðagögn í vinnusvæðinu getur þú einnig skilgreint, í dögum, tímamörk fyrir **Nýlega útgefnar afurðir** og **Stöðvaðar útgefnar afurðir**.

Vinnusvæðið samanstendur af samanteknum reitum og tveimur listum. Listinn **Opin tilvik** sýnir tilvik afurðabreytinga sem hafa afurðir í völdu stigveldi afurðarflokks sem ekki er lokið og eru opnar. Listinn **Útgefið nýlega** sýnir afurðir sem hafa verið útgefnar innan þeirra tímamarka sem eru sett í skilgreiningu vinnusvæðisins. Fyrir hverja vöru á listanum er villuleit keyrð og staða hennar sýnd. Þessi staða gæti gefið til kynna að nauðsynlegri skilgreiningu fyrir lögaðilann sé ekki lokið. Af listanum getur þú fengið beinan aðgang að síðunum **Upplýsingar um losaðar afurðir**, **Viðhald afurðareiginda**, **Viðhald afurðarflokks**, **Sjálfgefnar pöntunarstillingar**, og **Textaþýðingar** til að ljúka við nauðsynlegar skilgreiningar afurðarinnar.

### <a name="manually-creating-a-new-released-product"></a>Handvirk stofnun á nýrri útgefinni afurð

Hægt er að stofna útgefna afurð í einni keyrslu, allt eftir viðskiptaferlum fyrirtækisins og þeim reglum sem gilda um hvort þessi virkni skuli notuð. Þessi virkni stofnar nýja afurð og gefur hana sjálfkrafa út til núverandi lögaðila. Til að stofna nýja afurð skaltu smella **Útgefnar afurðir** á vinnusvæðinu **Viðhald útgefinnar afurðar** eða á listasíðunni **Útgefin afurð**.
