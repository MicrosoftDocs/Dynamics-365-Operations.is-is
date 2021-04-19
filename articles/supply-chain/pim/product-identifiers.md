---
title: Afurðarkenni
description: Þetta efnisatriði veitir upplýsingar um mismunandi tegundir afurðarkenna og útskýrir hvernig hægt er að bæta við afurðarkennum í afurðargögnum þínum.
author: cvocph
ms.date: 03/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductEntityIdentifierCode, EcoResProductListPage, EcoResProductDetailsExtended, EcoResProductVariantsPerCompany
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: kamaybac
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2017-12-31
ms.openlocfilehash: c3f82834fa7fc5eec6411d92729439dfd49a1fcc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820251"
---
# <a name="product-identifiers"></a>Afurðarkenni

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

[!include [banner](../includes/banner.md)]

Þetta efnisatriði veitir upplýsingar um mismunandi tegundir afurðarkenna og útskýrir hvernig hægt er að bæta við afurðarkennum í afurðargögnum þínum.

Þegar unnið er með afurðir í vinnusal eða í vöruhúsi í Microsoft Dynamics ERP eða Microsoft Dynamics CRM þarf að hafa góða stefnu til að bera kennsl á afurðir og afurðarafbrigði.

## <a name="unique-product-numberproduct-id"></a>Einkvæm afurðarnúmer/afurðarkenni

Í Dynamics 365 Supply Chain Management er afurðarnúmerið aðalauðkenni afurðar (þ.e. einkvæma afurðarkennið). Hægt er að mynda númerið sjálfkrafa með númeraröð eða tengja handvirkt við afurð. Fyrir afurðarafbrigði er hægt að skilgreina númerin með nafnakerfissniði afurðar.

Í mörgum tilvikum er afurðarnúmerið ekki upphaflega stofnað í Dynamics 365 Supply Chain Management. Þess í stað er það tengt afurð í lífferilssstjórnunarkerfi afurðar (PLM) eða gagnastjórnunarkerfi afurðar (PDM). Í þessu tilviki eru gagnaeiningar notaðar til að flytja inn afurðir og afurðarafbrigði. Supply Chain Management notar síðan tölurnar í öllum aðgerðum.

Þegar Supply Chain Management er innleitt ætti að taka sérstakt tillit til stefnunar er varðar afurðarnúmer. Gott númerakerfi bætir flæði vörustjórnunar og hjálpar til við að koma í veg fyrir villur. Gott afurðarkenni er að hámarki 15 stafir. Helst hefur það færri en 10 stafi og inniheldur ekki meira en fimm stafaflokka. Einnig er hægt að nota leitarheiti til að virkja flýtileitir. Leitarheiti er viðbótarheiti sem táknar flokkanir afurða.

Þegar Microsoft Dataverse er notað, er afurðarnúmerið í Supply Chain Management einnig afurðarnúmerið í Microsoft Dataverse. Afurðarafbrigði eru samstillt við Dataverse sem einkvæmar afurðir.

## <a name="item-number-and-product-dimensions"></a>Vörunúmer og afurðarvíddir

Vörunúmerið er afurðarkennið sem notað er af tilteknum lögaðila. Helst ætti vörunúmerið að vera eins og afurðarnúmerið. Ef nafnakerfið er mismunandi eftir lögaðila verður erfitt að fylgjast með afurð í gegnum aðfangakeðjuna og íþyngjandi ferlar endurmerkinga og tilvísana koma þá til sögunnar. Fyrir samræmingu við eldri útgáfur (það er við Microsoft Dynamics AX 2009 og fyrr), höfum við varðveitt þetta líkan. Hins vegar mælum við með því að auðkenni sem eiga við um lögaðila verði fjarlægð hvenær sem hægt er og að í staðinn sé notað einkvæmt afurðarnúmer sem aðalauðkenni.

Að auki er ekki hægt að auðkenna afurðarafbrigði með vörunúmeri á einkvæman hátt. Það krefst alltaf sambland af vörunúmeri og öllum afurðarvíddum sem eru skilgreindar í afurðarsniðmáti. Þessi krafa getur orðið fyrirferðarmikil og getur hægt á auðkenningarferlinu. Af þessum sökum mælum við með því að þú notir einkvæmt afurðarnúmer í staðinn fyrir vörunúmerið hvenær sem þú getur.

Margar síður hafa enn vörunúmer og afurðarvíddir sem aðalauðkenni. Hins vegar er hægt að nota afurðarnúmerin við leit. Á **Sala og markaðssetning** &gt; **Uppsetning** &gt; **Leita** &gt; **Leita að færibreytum** er hægt að breyta uppflettingu leitar þannig að hún noti afurðarnúmer í stað vörunúmera sem aðalleitarstefnu. Ef þú stillir valkostinn **Virkja uppflettingu fyrir afurðarleit** á **Já** mun uppflettingin ekki aðeins sýna afurðarsniðmát heldur líka afurðarafbrigði. Nánari upplýsingar er að finna í [Leita að afurðum og afurðarafbrigðum við pöntunarfærslu](search-products-product-variants.md).

Auk þess getur þú leitað og afmarkað afurðarnúmerið, afurðarheiti og lýsingu og kenni afurðarvíddar á afurðarafbrigði. Þegar þú velur afbrigði verður viðkomandi vörunúmer og öll kenni afurðarvídda valin. Þess vegna getur þú auðveldlega fundið og valið rétta afbrigðið. Mælt er með þessari stillingu ef notuð eru afurðarafbrigði og einkvæm afurðarnúmer sem aðalauðkenni fyrir afurðir. Eina undantekningin gæti verið tískuiðnaðurinn, þar sem viðskiptaferlarnir krefjast oft að aðalsniðmát sé valið áður en afbrigði er valið. Þú ættir að meta þennan valkost vandlega áður en þú setur inn númerakerfið.

> [!NOTE]
> Ekki er hægt að breyta vörunúmeri fyrir vöru þegar ein eða fleiri viðskipti eru fyrir hendi fyrir þá vöru.

## <a name="product-name-and-description"></a>Afurðarheiti og lýsing

Afurðarheiti og lýsing eru auðkenni afurðar sem eru læsileg mönnum og hægt er að viðhalda á mörgum tungumálum. Sjálfgefið birtir biðlari Supply Chain Management allar afurðarupplýsingar í sjálfgefnu tungumáli fyrirtækis, ekki á tungumáli notandans. Hins vegar er þýdd afurðarheiti og lýsingar notaðar í öllum samskiptum við viðskiptavini og lánardrottna. Þýðingarnar eru byggðar á tungumálakóða viðskiptavina- og lánardrottnalykla.

Fyrir afurðarafbrigði er hægt að mynda afurðarheiti með nafnakerfissniði afurðar. Þar sem engar kröfur eru um að afurðarheitin séu einkvæm, gætirðu fundið margar afurðir sem bera sama heiti.

## <a name="product-and-item-search-names"></a>Leitarheiti afurðar og vöru

Supply Chain Management býður upp á annars konar leitarheit fyrir afurðir og líka fyrir vörur (útgefnar afurðir). Þetta leitarheiti þarf ekki að vera einkvæmt og það er hægt að breyta því eftir að afurð eða afurðarafbrigði varan er stofnað. Við mælum með að þú notir leitarheitið til að leita að afurðum eftir flokkum. Leitarheitin virkja flýtileit, einkum í sölu- og innkaupferlum.

Leitarheitið getur einnig innihaldið afurðarkenni viðskiptavinar eða lánardrottins, eða einhver önnur ytri afurðarkenni, ef þetta ytra kenni er aðalleitarskilyrði fyrir afurð.

## <a name="external-product-identifiers-customer-and-vendor-identifiers"></a>Ytri afurðarkenni (Auðkenni viðskiptavinar og lánardrottins)

Fyrir útgefnar afurðir er hægt að viðhalda vörunúmerum, vöruheitum og vörulýsingum sem viðskiptavinurinn eða lánardrottin notar. Tilvísanirnar eru sýndar á ytri skjölum, t.d. sölupöntunum, innkaupapöntunum, fylgiseðlum og reikningum. Í núverandi útgáfu af Supply Chain Management eru ytri tilvísanir ekki sýndar í síðum kjarnastarfsemi. Eina undantekningin er vörunúmer lánardrottins. Þetta númer er sýnt í svarglugganum **Afurðarupplýsingar** ef sjálfgefin lánardrottin er skilgreindur fyrir útgefna afurð.

Þú getur unnið með ytri afurðarkennum eftir útgefnum afurðum, útgefnum afurðarafbrigðum, viðskiptavini eða viðskiptavinaflokki eða lánardrottni eða lánardrottnaflokki.

Á síðunni **Útgefnar afurðir** skaltu fylgja einum af þessum skrefum.

- Fyrir viðskiptavini, á flipanum **Selja**, í flokknum **Tengdar upplýsingar** skal velja **Ytri vörulýsing**.
- Fyrir lánardrottna, á flipanum **Innkaup**, í flokknum **Tengdar upplýsingar** skal velja **Ytri vörulýsing**.

Á síðunni **Ytri vörulýsingar** geturðu tengt vörunúmer viðskiptavinar eða lánardrottins við útgefna afurð. Þessa tengingu verður að gera fyrir hvern lögaðila. Eftirfarandi upplýsingar er hægt að ná í. Því miður eru merkingarnar örlítið villandi í núverandi útgáfu af Supply Chain Management. Hins vegar gæti þessum merkingum verið breytt í framtíðarútgáfu.

| Svæði | Samsvarandi upplýsingar viðskiptavinar | Samsvarandi upplýsingar lánardrottins |
|-------|------------------------------------|----------------------------------|
| Ytra númer hlutar | Vörunúmer viðskiptavinar | Vörunúmer lánardrottins |
| lýsing | Heitið sem viðskiptavinurinn tengir við vöruna | Heitið sem lánardrottinn tengir við vöruna |
| Ytri vörutexti | Vörulýsing viðskiptavinar | Vörulýsing lánardrottins |

Ef margir viðskiptavinir eða lánardrottnar nota sömu vörunúmerin (eins og í tilfelli tengdra innkaupa eða viðskiptahóps sem dæmi), getur þú stofnað flokk viðskiptavina eða lánardrottna til að einfalda viðhald á ytri afurðarupplýsingum.

- Fyrir viðskiptavinaflokka skaltu fara í **Sala** &gt; **Uppsetning** &gt; **Vörur** &gt; **Ytri vörulýsing** til að stofna og vinna með flokkunum og tengdum vörunúmerum. Til að tengja viðskiptavini við flokk skal fara í **Viðskiptakröfur** &gt; **Viðskiptavinir** &gt; **Allir viðskiptavinir** og þá á flýtiflipanum **Sjálfgefnar stillingar sölupantana** skal tilgreina gildi í reitnum **Vara - viðskiptavinaflokkur**.
- Fyrir flokka lánardrottna skaltu fara í **Innkaup og aðföng** &gt; **Uppsetning** &gt; **Ytri vörulýsingarflokkur** til að stofna og vinna með flokkunum og tengdum vörunúmerum. Til að tengja lánardrottna við flokk skaltu fara í **Viðskiptaskuldir** &gt; **Lánardrottnar** &gt; **Allir lánardrottnar** og síðan á flýtiflipanum **Sjálfgefnar stillingar sölupantana** skal tilgreina gildi í reitnum **Vara - lánardrottnaflokkur**.
 
## <a name="bar-codes"></a>Strikamerki

Ef þú vilt nota strikamerkjaskanna til að bera kennsl á afurðir verður kenni afurðar að uppfylla kröfur strikamerkjastaðalsins sem er notaður. Þess vegna innihalda strikamerki venjulega ekki hrá afurðarnúmer, heldur númer sem er sérstaklega búið til fyrir valda strikamerkjatækni. Þú getur viðhaldið mörgum strikamerkjum eftir strikamerkjagerð. Þú getur jafnvel tengt sama strikamerkið við margar vörur og síðan valið virku tenginguna sem á við þegar þú skannar strikamerki.

Áður en þú skilgreinir strikamerki getur þú skilgreint eina eða fleiri uppsetningar á strikamerki. Uppsetningar strikamerkis geta hjálpað til við að sannprófa að strikamerki fylgi nauðsynlegum viðmiðum og að það sé því hægt að prenta og skanna þau. Þú getur einnig viðhaldið sérstökum strikamerkjum fyrir tiltekið afurðarmagn.

Við mælum með að þú notir uppsetningu strikamerkja til að viðhalda GTIN númeri (Global Trade Item Number) eða EAN-kóðum (International Article Number).

Til að vinna með strikamerki, á síðunni **Útgefnar afurðir**, á flipanum **Stjórna birgðum**, í flokknum **Vöruhús** skal velja **Strikamerki**.

## <a name="gtin-codes"></a>GTIN-kóðar

Í rafrænum viðskiptum er lykilatriði að allir aðilar tali sameiginlegt tungumál og vísi í afurðir með því að nota sameiginlegt sett af auðkennum. Þ.a.l. eru nokkrar atvinnugreinar sem treysta á [GTIN](https://www.gs1.org/id-keys/gtin), sem er alþjóðlegt vörunúmerakerfi sem er einfaldað með GS1.

Við mælum með að viðhalda GTIN sem strikamerki. Hins vegar getur þú einnig unnið með það á síðunni **Vara - GTIN**. Til að opna þessa síðu, skaltu á síðunni **Útgefnar afurðir**, á flipanum **Stjórna birgðum**, í flokknum **Vöruhús** velja **GTIN-kóðar**. GTIN er ekki viðhaldið sem alþjóðlegt númer. Þess í stað er því viðhaldið af lögaðila.

Í Supply Chain Management skilgreinir þú umbúðarafbrigði í vöruhúsaaðgerðum með því að skilgreina tilteknar mælieiningar. Til dæmis er hægt að geyma vöru í stykkjum, í búntum af sex, í bökkum af 18 eða á heilum brettum. Tiltekin mælieining verður skilgreind fyrir hver þessara umbúðarafbrigða. Vegna þess að GTIN er venjulega tengt umbúðaeiningu afurðar, leyfir síðan **Vara - GTIN** að viðhalda mörgum GTIN-kóðum á hverja vöru og mælieiningu. Hins vegar getur þú ekki notað sama GTIN-kóðan oftar en einu sinni fyrir mismunandi vörur eða afurðarafbrigði lögaðila.

Til að viðhalda **GTIN-kóðar** skal á síðunni **Útgefnar afurðir**, á flipanum **Stjórna birgðum** í flokknum **Vöruhús** velja **GTIN**.

## <a name="external-codes"></a>Ytri kóðar

Hægt er að skilgreina ytri kóða fyrir marga aðila. Til dæmis getur þú skilgreint ytri kóða til að bera kennsl á afurðir og útgefnar afurðir. Þessir ytri kóðar geta verið notaðir til að tengja tölfræðilega kóða eða skattkóða við útgefna afurð og útgefið afurðarafbrigði. Ytri kóðar eru skilgreindir af lögaðila og gerð kóða. Þeir verða að vera einkvæmir af lögaðilum, gerð kóða og töflutilvísun.

Því miður er engin staðalvirkni sem gerir þér kleift að leita að afurðum út frá ytri kóða.

## <a name="data-entities-that-are-used-to-import-and-export-product-identifiers"></a>Gagnaeiningar sem eru notaðir til að flytja inn og flytja út afurðarkenni

| Einingarheiti | Flytja inn kenni | Flytja út kenni | Athugasemdir |
|-------------|--------------------|--------------------|----------|
| Afurðir V2 | Afurðarnúmer, leitarheiti afurðar, afurðarheiti, afurðarlýsing | Afurðarnúmer, leitarheiti afurðar, afurðarheiti, afurðarlýsing | Það fer eftir stillingum á einingu og númeraröð afurðarnúmers hvort hægt sé að stofna sjálfkrafa afurðarnúmer við innflutning. |
| Afurðarafbrigði | Afurðarnúmer, leitarheiti afurðar, afurðarheiti, afurðarlýsing | Afurðarnúmer, leitarheiti afurðar, afurðarheiti, afurðarlýsing | Það fer eftir nafnakerfissniði afurðar hvort hægt sé að stofna sjálfkrafa afurðarnúmerið við innflutning. Þó er hægt að flytja inn einkvæmt afurðarnúmer og það afurðarnúmer þarf ekki að fylgja skipulaginu á nafnakerfissniði afurðar. |
| Þýðingar afurðar | Afurðarheiti, afurðarlýsing | Afurðarheiti, afurðarlýsing | Þessi eining skrifar yfir hvaða tungumál sem er. Þegar skrifað er yfir heitið eða lýsinguna á aðaltungumáli lögaðila, breytist heitið og lýsingin á sjálfri vörunni. |
| Útgefin stofnun afurðar V2 | Vörunúmer, afurðarnúmer, leitarheiti vöru| Vörunúmer, afurðarnúmer, leitarheiti vöru, leitarheiti afurðar, afurðarheiti | Þessi eining getur verið áskorun þegar númeraraðir eru notaðar við stofnun á nýjum útgefnum afurðum. Báðar númeraraðirnar **Vörunúmer** og **Afurðarnúmer** hafa áhrif. Hins vegar er númeraröðin **Vörunúmer** fyrir hvern lögaðila, en númeraröðin **Afurðarnúmer** er alþjóðleg. Því mælum við með því að þú notir númeraröðina **Vörunúmer** þegar þú setur upp nýjar útgefnar afurðir. Augljóslega, þegar einingin er notuð til að gefa út fyrirliggjandi afurð verður afurðarnúmerið að vera gefið í einingunni. Nánari upplýsingar er að finna í kaflanum „Afurðar- og vörunúmeraraðir" í þessu efnisatriði. |
| Útgefin afurðarafbrigði | Vörunúmer, afurðarvíddir, afurðarnúmer | Afurðarnúmer, leitarheiti afurðar, afurðarheiti, afurðarlýsing, afurðarvíddir | Eins og einingin **Afurðarafbrigði**, er hægt að nota þessa einingu til að stofna nýjar afurðir sem annaðhvort fylgja nafnakerfissniði afurðar eða nota sín eigin afurðarnúmer fyrir afbrigðið. |
| Ytri vörulýsing fyrir viðskiptavini | Vörunúmer viðskiptavinar, vöruheiti viðskiptavinar, lýsing viðskiptavinar, viðskiptavinalykill | Vörunúmer viðskiptavinar, vöruheiti viðskiptavinar, lýsing viðskiptavinar, viðskiptavinalykill | Hóp af viðskiptavinum (t.d. samtök kaupenda) er hægt að sameina í einn flokk með því að nota eininguna **Viðskiptavinaflokkar ytri vörulýsinga**. |
| Ytri vörulýsing fyrir lánardrottna | Vörunúmer lánardrottins, vöruheiti lánardrottins, lýsing lánardrottins, lánardrottnalykill | Vörunúmer lánardrottins, vöruheiti lánardrottins, lýsing lánardrottins, lánardrottnalykill | Hóp af lánardrottnum (t.d. samtök lánardrottna eða iðnaðarsamtök) er hægt að safna saman í einn flokk með því að nota eininguna **Lánardrottnaflokkar ytri vörulýsinga**. |
| Strikamerki vöru | Strikamerki | Strikamerki | Við innflutning verður að vísa til uppsetningu strikamerkis sem er skilgreind í markkerfinu. Innfluttar tilvísanir strikamerkja eru villuleitaðar gagnvart uppsetningu strikamerkis og þeim er hafnað ef strikamerkin standast ekki kröfurnar sem eru skilgreindar í þeirri uppsetningu. |
| Ytri kóðar fyrir útgefnar afurðir | Ytri kóði | Ytri kóði, ytri kóðaklasar, vörunúmer | Ytri kóðar eru eftir lögaðila. Fyrir innflutning verður þú að vísa í skilgreindan kóðaklasa. Flyttu inn kóðaklasana með því að nota eininguna **Ytri kóðaklasar fyrir útgefnar afurðir**. |
| Ytri kóðar fyrir útgefin afurðarafbrigði | Ytri kóði | Ytri kóði, ytri kóðaklasar, vörunúmer, afurðarvíddir | Ytri kóðar eru eftir lögaðila. Fyrir innflutning verður þú að vísa í skilgreindan kóðaklasa. Flyttu inn kóðaklasana með því að nota eininguna **Ytri kóðaklasar fyrir útgefnar afurðir**. Þessi eining vísar til afurðarafbrigða eftir vörunúmeri og afurðarvíddum. |
| Ytri kóðar fyrir útgefin afurðarafbrigði eftir kenni afurðarnúmers | Ytri kóði | Ytri kóði, ytri kóðaklasar, afurðarnúmer | Ytri kóðar eru eftir lögaðila. Fyrir innflutning verður þú að vísa í skilgreindan kóðaklasa. Flyttu inn kóðaklasana með því að nota eininguna **Ytri kóðaklasar fyrir útgefnar afurðir**. Þessi eining vísar til afurðarafbrigða eftir afurðarnúmeri afbrigðisins. (Frá næstu stóru útgáfu) |
| GTIN | Ekki tiltækt | Ekki tiltækt | Eins og er, er engin sérstök eining sem er notuð til að flytja inn og flytja út GTIN-kóða. Við mælum með að þú notir eininguna **Strikamerki vöru** í staðinn. |
| Afurðareining auðkenniseiningar Common data service | Ekki tiltækt | Vöruheiti, leitarheiti vöru, leitarheiti afurðar, vörunúmer lánardrottins, vörunúmer viðskiptavinar, ytri kóðar, GTIN-kóðar, strikamerki | Þessi eining sameinar öll auðkenni í eitt gagnalíkan, þannig að hægt sé að nota eitt viðmót til að auðveldlega flytja út öll auðkenni og tengdar gerðir þeirra. Notaðu eininguna **Auðkenniskóði afurðareiningar** til að flytja út auðkenniskóða og lýsingar. Notaðu eininguna **Umfang auðkennis afurðareiningar** til að flytja út viðbótarupplýsingar umfangs til auðkennis, svo sem aðilans, lögaðilans, magns eða einingar. |

### <a name="product-and-item-number-sequences"></a>Númeraraðir afurðar og vöru

Þú getur skilgreint tvær mismunandi númeraraðir:

- Númeraröðin **Afurðarnúmer** fyrir alþjóðlega afurðarnúmerið
- Númeraröðin **Vörunúmer** fyrir vörunúmer á lögaðila

> [!NOTE]
> Þú ættir aðeins að nota vörunúmerið sem aðskilið auðkenni þegar þú flytur mismunandi lögaðila frá mismunandi upprunastöðum sem höfðu mismunandi númerakerfi. Þú ættir alltaf að reyna að nota vörukenni sem er einkvæmt þvert yfir alla lögaðila. Þess vegna ættir þú að stilla valkostinn **Handvirkt** á **Já** fyrir númeraröðina **Vörunúmer**. Þannig mun vörunúmerið fylgja afurðarnúmerinu við stofnunina. Ef Supply Chain Management er ekki leiðandi kerfið fyrir ný afurðarnúmer, þá ættir þú að stilla valkostinn **Handvirkt** á **Já** fyrir báðar númeraraðirnar **Vörunúmer** og **Afurðarnúmer**.

Þegar þú notar eininguna **Útgefin afurðarstofnun V2** til að stofna afurðir, geta margar stillingar haft áhrif á hvernig númeraraðirnar eru notaðar til að stofna afurðarnúmer og vörunúmer:

- Stillingar á númeraröðinni **Afurðarnúmer**
- Stillingar á númeraröðinni **Vörunúmer**
- Vörpun vörunúmersins 
- Vörpun afurðarnúmers

Eftirfarandi tafla veitir yfirlit yfir niðurstöður innflutnings og handvirkrar stofnunar með tilteknum samsetningum númeraraðar og reitavörpunarstillinga.

| Númeraröð afurðarnúmers | Númeraröð vörurnúmers | Vörpun vörunúmers | Vörpun afurðarnúmersins | Niðurstaða innflutnings eininga | Niðurstaða handvirkrar stofnunar | Niðurstaða |
|--------------------------------|-----------------------------|----------------------------|-------------------------------|-------------------------|----------------------------|-----------|
| Handvirkt = Nei | Handvirkt = Nei | Engin vörpun | Engin vörpun | Afurðarnúmer nota númeraröðina **Afurðarnúmer**. Vörunúmer nota númeraröðina **Vörunúmer**. | Afurðarnúmer nota númeraröðina **Afurðarnúmer**. Vörunúmer nota númeraröðina **Vörunúmer**. | Með þessari stillingu munu vörunúmer fylgja vörunúmeraröðinni og vörunúmer fylgja röð númeraraðar. Samt sem áður mun þessi stilling ekki virka ef það er meira en einn hlutur (röð) til að flytja inn. |
| Handvirkt = Nei | Handvirkt = Já | Mynda sjálfkrafa | Engin vörpun | Bæði afurðarnúmer og vörunúmer nota númeraröðina **Vörunúmer**. | Bæði afurðarnúmer og vörunúmer nota númeraröðina **Afurðarnúmer**. | Bæði afurðarnúmer og vörunúmer munu fylgja númeraröð afurðarnúmers. Þetta er mælt með aðferð til að flytja inn magnafurðir með V2 gagnaeiningunni fyrir afurðaútgáfu.<br><br>Aðeins er hægt að nota þessa nálgun þegar vörur eru fluttar inn í magni (nokkrar línur) og þegar ekki er verið að búa til vörur í gegnum notandaviðmótið. Ef þarf bæði að flytja inn í magni og búa til afurðir í gegnum notandaviðmótið skal í staðinn nota ferlið í næstu línu þessarar töflu. Til að fara úr því að nota aðferð magninnflutnings í að nota notandaviðmótið til að flytja inn og búa til afurðir handvirkt þarf að breyta **Næsta númer** handvirkt í númerröð vörunúmersins til að það passi við **Næsta númer** í númeraröð afurðarnúmersins. Síðan er hægt að skipta yfir í næstu línu töflunnar. |
| Handvirkt = Nei | Handvirkt = Já | Engin vörpun | Engin vörpun | Bæði afurðarnúmer og vörunúmer nota númeraröðina **Afurðarnúmer**. | Bæði afurðarnúmer og vörunúmer nota númeraröðina **Afurðarnúmer**. | Bæði afurðarnúmer og vörunúmer munu nota númeraröð afurðarnúmers. Samt sem áður mun þessi stilling ekki virka ef það er meira en einn hlutur (röð) til að flytja inn.<br><br>Nota verður þessa aðferð ef bæði þarf að flytja inn afurðir með því að nota einingarnar (aðeins er hægt að flytja inn eina línu í einu) og stofna afurðir í gegnum notandaviðmótið. |
| Handvirkt = Já | Ekki tiltækt | Ekki tiltækt | Mynda sjálfkrafa | Þú færð eftirfarandi villuboð: "Númeraröð er ekki hægt að greina." | Samkvæmt númeraröðinni **Vörunúmer** | Þessi stilling er ekki studd fyrir innflutning. |

## <a name="product-entity-identifier-export-all-product-identifiers"></a>Kenni afurðareiningar (Flytja út öll afurðarkenni)

Kennilíkan afurðareiningar var stofnað til að gera útgáfu 1.0 af Dataverse kleift að vera úthlutað með öllum auðkennum sem eru notuð til að vísa í afurð. Til að einfalda þetta verk er öllum auðkennum safnað saman í eina altæka auðkennistöflu, svo að hægt sé að flytja þau út sem eitt líkan. Athugaðu að þessi útgáfa af Dataverse notar ekki kennilíkan afurðar. Þess vegna hefur einingin **Afurðareining auðkenniseiningar Common data service** og þetta ferli takmarkaða hagnýta notkun og mun líklega verða fyrir breytingum í framtíðinni.

Auðkennistafla afurðar er altæk tafla sem er útfyllt af öllum tilvísanatöflum helstu lögaðila með endurtekinni runuvinnslu. Þú verður að velja lögaðila og tegundastigveldi afurðar sem skilgreiningu á umfangi alþjóðlegs afurðarsniðmáts. Myndun á altækri auðkennistöflu afurðar takmarkast við afurðir sem eru gefnar út til valinna lögaðila og afurða sem tilheyra afurðastigveldinu sem er valið fyrir hlutverkið **Common data service** í tegundastigveldi afurðar.

Í þessu ferli er gert ráð fyrir að gögn afurðarsniðmáts séu fyrst og fremst viðhaldið í einum miðlægum lögaðila. (Hins vegar getur þessi lögaðili verið sýndarlögaðili sem er aðeins notaður til að viðhalda alþjóðlegum aðalgögnum.)

Fylgdu þessum skrefum til að grunnstilla umhverfið.

1. Veldu tegundastigveldi fyrir Dataverse. Á síðunni **Tengsl hlutverka í tegundastigveldi**, ef engin stigveldi eru tengd við **Common data service**, verður þú að stofna nýja tengingu. Veldu hlutverkið **Common Data Service** og tengdu síðan tegundastigveldi afurðar sem sýnir afurðasafnið sem ætti að samstilla við Dataverse.
2. Veldu lögaðilann fyrir alþjóðleg gögn afurðarsniðmáts. Á síðunni **Færibreytur afurðarupplýsingastjórnunar**, á flipanum **Afurðareigindir** skal velja aðalfyrirtækið þar sem kennum afurðar og vöru er fyrst og fremst viðhaldið.
3. Skilgreindu gerðir auðkenniskóða og kóða sem á að flytja út. Farðu í **Afurðaupplýsingastjórnun** &gt; **Uppsetning** &gt; **Auðkenniskóðar afurðar**. Til að búa til gerðir auðkenniskóða skaltu velja **Búa til kóða**. Færsla kóðagerðar er búin til fyrir hverja gerð fyrir auðkenni sem er að finna í völdum lögaðilum.

    Fyrir strikamerki er gerð kóða búin til fyrir hverja uppsetningu á strikamerki. Fyrir ytri kóða er gerð kóða búin til fyrir hvern ytri kóðaklasa.

    Þú getur nú unnið með lista yfir kóðagerðir. Þú getur breytt kóða, heiti og lýsingu. Þú getur einnig eytt kóðagerðum. Kóðagerðir sem þú eyðir verða ekki notaðar til að fylla út í altækar auðkennistöflur afurðareiningar.

4. Þegar þú hefur lokið við að skilgreina kóðagerðir afurðarkenna, getur þú stofnað auðkennin í altæku töflunni með því að hefja vinnsluna **Stofna auðkenni afurðareiningar** á síðunni **Auðkenniskóðar afurðareiningar**. Þú ættir að keyra vinnsluna í runu. Vinnslan ætti að vera sett upp sem reglubundin runuvinnsla svo að fyllt sé í töfluna samkvæmt nýjum færslum.

Þú getur nú notað gagnaeiningarnar **Afurðareining auðkenniseiningar Common data service**, **Auðkenniskóðar afurðareiningar** og **Umfang auðkennis afurðareiningar** til að flytja út auðkennin fyrir hvaða markkerfi sem er.

## <a name="related-topic"></a>Tengt efni

[Leita að afurðum og afurðarafbrigðum við pöntunarfærslu](search-products-product-variants.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
