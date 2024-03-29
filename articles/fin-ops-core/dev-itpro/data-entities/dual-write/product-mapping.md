---
title: Samræmd afurðaupplifun
description: Þessi grein lýsir samþættingu afurðaupplýsinga milli forrita fjármála- og reksturs og Dataverse.
author: t-benebo
ms.date: 06/23/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 89ef56510ec971ef97fc9eb5c80768527abf5f88
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288923"
---
# <a name="unified-product-experience"></a>Samræmd afurðaupplifun

[!include [banner](../../includes/banner.md)]



Þegar vistkerfi fyrirtækja samanstendur af Dynamics 365 forritum, svo sem Finance, Supply Chain Management og Sales, nota fyrirtæki þessi forrit oft til að fá upplýsingar um vöru. Þetta er vegna þess að þessi forrit bjóða upp á öfluga vöruinnviði ásamt háþróuðum verðlagningarhugtökum og nákvæmum birgðagögnum fyrir lagermagn. Fyrirtæki sem nota utanaðkomandi vörukerfisstjórnunarkerfi (PLM) til að afla vörugagna geta sett vörur úr forritum fjármála- og reksturs í rásir í öðrum forritum Dynamics 365. Sameinuð vöruupplifunin færir samþætt vörugagnalíkan inn í Dataverse, þannig að allir notendur forritsins þ.m.t. notendur Power Platform geta nýtt sér þau ríku vörugögn sem koma úr forritum fjármála- og reksturs.

Hérna er vöruupplýsingamódelið úr Sales.

![Gagnamódel fyrir vörur í CE.](media/dual-write-product-4.jpg)

Hérna er afurðargagnalíkanið úr forritum fjármála- og reksturs.

![Gagnamódel fyrir afurðir í fjármála- og reksturs.](media/dual-write-products-5.jpg)

Þessi tvö afurðalíkön hafa verið samþætt í Dataverse eins og sýnt er hér að neðan.

![Gagnamódel fyrir vörur í forritum Dynamics 365.](media/dual-write-products-6.jpg)

Töflukort með tvöfaldri skráningu fyrir afurðir eru hönnuð fyrir gagnaflæði í eina átt, nærri í rauntíma frá forritum fjármála- og reksturs til Dataverse. Samt sem áður hafa vöruinnviðir verið opnaðir svo að hún verði tvíátta ef þess er krafist. Þó að hægt sé að sérsníða það er það á þína ábyrgð, þar sem Microsoft mælir ekki með þessari aðferð.

## <a name="templates"></a>Sniðmát

Afurðarupplýsingar innihalda allar upplýsingar sem tengjast vörunni og skilgreiningu hennar, svo sem afurðarvíddir eða mælingar og geymsluvíddir. Eins og eftirfarandi tafla sýnir er búið að stofna safn af töflukortum til að samstilla afurðir og tengdar upplýsingar.

Forrit fyrir fjármál- og rekstur | Önnur Dynamics 365 forrit | Lýsing
-----------------------|--------------------------------|---
[Allar afurðir](mapping-reference.md#138) | msdyn_globalproducts | Taflan fyrir allar afurðir inniheldur allar afurðir sem eru í boði í forritum fjármála- og reksturs, bæði útgefnar afurðir og afurðir sem ekki eru gefnar út.
[CDS-útgefnar einkvæmar afurðir](mapping-reference.md#213) | Afurð | Taflan **Afurð** inniheldur dálkana sem skilgreina afurðina. Hún felur í sér einstakar afurðir (afurðir með undirgerðaafurð) og afurðarafbrigðin. Eftirfarandi tafla sýnir vörpun.
[Litir](mapping-reference.md#170) | msdyn\_productcolors
[Afbrigði](mapping-reference.md#171) | msdyn\_productconfigurations
[Sjálfgefnar pöntunarstillingar](mapping-reference.md#172) | msdyn_productdefaultordersettings |
[Afurðartegundir](mapping-reference.md#166) | msdyn_productcategories | Hver vöruflokkur og upplýsingar um uppbyggingu hans og einkenni eru að finna í vöruflokkstöflunni.
[Úthlutanir afurðategundar](mapping-reference.md#167) | msdyn_productcategoryassignments | Til að úthluta vöru í flokk er hægt að nota töfluna fyrir vöruflokkaúthlutanir.
[Tegundastigveldi afurðar](mapping-reference.md#168) | msdyn_productcategoryhierarchies | Stigveldi afurðar eru notuð til að flokka eða flokka afurðir. Flokkastigveldin eru fáanleg í Dataverse með því að nota töflu tegundastigveldi afurðar.
[Hlutverk tegundastigveldis afurðar](mapping-reference.md#169) | msdyn_productcategoryhierarchyroles | Hægt er að nota vöruveldi fyrir mismunandi hlutverk í D365 fjármála- og reksturs. Þau tilgreina hvaða flokkur er notaður í hverju hlutverki hlutverkatöflu afurðaflokks er notaður.
[Sjálfgefnar vörupöntunarstillingar V2](mapping-reference.md#175) | msdyn_productspecificdefaultordersettings |
[Afurðavíddaflokkar](mapping-reference.md#173) | msdyn\_productdimensiongroups | Afurðavíddarhópurinn skilgreindi hvaða afurðavíddir skilgreina vöruna.
[Litir afurðarsniðmáts.](mapping-reference.md#187) | msdyn_sharedproductcolors | Taflan **Sameiginlegur afurðalitur** gefur til kynna liti sem sérstakt afurðarsniðmát getur haft. Þetta hugtak er flutt í Dataverse til að halda gögnum samkvæmum.
[Skilgreiningar afurðarsniðmáts](mapping-reference.md#188) | msdyn_sharedproductconfigurations | Taflan **Sameiginleg skilgreining afurða** gefur til kynna skilgreiningar sem sérstakt afurðarsniðmát getur haft. Þetta hugtak er flutt í Dataverse til að halda gögnum samkvæmum.
[Stærðir afurðarsniðmáts](mapping-reference.md#190) | msdyn_sharedproductsizes | Taflan **Sameiginleg afurðastærð** gefur til kynna stærðir sem sérstakt afurðarsniðmát getur haft. Þetta hugtak er flutt í Dataverse til að halda gögnum samkvæmum.
[Stílar afurðarsniðmáts](mapping-reference.md#191) | msdyn_sharedproductstyles | Taflan **Sameiginlegur afurðastíll** gefur til kynna stíla sem sérstakt afurðarsniðmát getur haft. Þetta hugtak er flutt í Dataverse til að halda gögnum samkvæmum.
[Afurðarnúmer sem eru auðkennd með strikamerki](mapping-reference.md#164) | msdyn\_productbarcodes | Strikamerki afurða eru notuð til að bera kennsl á afurðir á einkvæman hátt.
[Afurðartengdur umreikningur eininga](mapping-reference.md#176) | msdyn_productspecificunitofmeasureconversions |
[Útgefnar afurðir V2](mapping-reference.md#189) | msdyn\_sharedproductdetails | Taflan **msdyn\_sharedproductdetails** inniheldur dálka úr forritum fjármála- og reksturs sem skilgreina afurðina og innihalda fjárhags- og stjórnunarupplýsingar afurðarinnar.
[Stærðir](mapping-reference.md#174) | msdyn\_productsizes
[Geymsluvíddarflokkar](mapping-reference.md#177) | msdyn_productstoragedimensiongroups | Víddarhópur afurðageymslu táknar aðferðina sem notuð er til að skilgreina staðsetningu afurðarinnar í vöruhúsinu.
[Stílar](mapping-reference.md#178) | msdyn\_productstyles
[Rakningarvíddarflokkar](mapping-reference.md#179) | msdyn_producttrackingdimensiongroups | Víddarflokkur afurðarakningar táknar aðferðina sem notuð er til að rekja afurðina í birgðum.
[Einingar](mapping-reference.md#219) | uoms
[Umreikningur eininga](mapping-reference.md#199) | msdyn_ unitofmeasureconversions

## <a name="integration-of-products"></a>Samþætting á afurðum

Í þessu líkani er afurðin táknuð með samsetningu á tveimur töflum í Dataverse: **Afurð** og **msdyn\_samnýttar afurðarupplýsingar**. Fyrri taflan hefur að geyma skilgreininguna á vöru (einstaka auðkenni fyrir vöruna, vöruheitið og lýsinguna), en önnur taflan inniheldur dálkana sem eru geymdir á afurðastigi. Samsetning þessara tveggja taflna er notuð til að skilgreina afurðina í samræmi við hugtakið birgðahaldseining (BHE). Hver útgefin afurð er með upplýsingar í framangreindum töflum (afurð og samnýttar afurðaupplýsingar). Til að fylgjast með öllum afurðum (gefnar út og ekki gefnar út) er taflan **Altækar afurðir** notuð.

Þar sem varan er táknuð sem SKU er hægt að fanga hugtökin aðgreindar vörur, vörumeistarar og afbrigði afurða í Dataverse á eftirfarandi hátt:

- **Afurðir með undirgerð afurðar** eru afurðir sem eru skilgreindar af sjálfum sér. Engar víddir þarf að skilgreina. Dæmi er sérstök bók. Fyrir þessar afurðir er ein lína búin til í töflunni **Afurð** og ein lína er búin til í töflunni **msdyn\_sharedproductdetails**. Engin lína afurðafjölskyldu er búin til.
- **Afurðarsniðmát** eru notuð sem almennar afurðir sem innihalda skilgreininguna og reglur sem ákvarða hegðun í viðskiptaferlum. Samkvæmt þessum skilgreiningum er hægt að búa til sérstakar afurðir sem eru þekktar sem vöruafbrigði. Sem dæmi má nefna að stuttermabolur er afurðasniðmát og hann getur haft lit og stærð sem víddir. Hægt er að losa afbrigði sem hafa mismunandi samsetningar af þessum víddum, eins og litlum bláum stuttermabol eða meðalstórum grænum stuttermabol. Í samþættingunni er ein lína á hvert afbrigði búin til í afurðatöflunni. Þessi lína inniheldur upplýsingar um afbrigði, eins og mismunandi víddir. Almennar upplýsingar um vöruna eru geymdar í töflunni **msdyn\_sharedproductdetails**. (Þessar almennu upplýsingar eru geymdar í afurðarsniðmátinu.) Upplýsingar afurðarsniðmáts eru samstilltar við Dataverse um leið og útgefið afurðarsniðmát er búið til (en áður en afbrigði eru losuð).
- **Einkvæmar afurðir** vísa til allra undirgerðaafurða afurðanna og allra afurðaafbrigðanna.

![Gagnamódel fyrir afurðir.](media/dual-write-product.png)

Með tvíritunarvirkni virkjaða verða vörur úr fjármála- og reksturs samstilltar í öðrum Dynamics 365 vörum í stöðunni **Drög**. Þeim er bætt við fyrsta verðlistann með sama gjaldmiðil og er notaður í forriti viðskiptavinar og raðar heiti verðlista eftir stafrófsröð. Með öðrum orðum, þeim er bætt við fyrstu verðskrána í forriti Dynamics 365 sem samsvarar gjaldmiðli lögtöflunnar þinnar þar sem varan er gefin út í forriti fjármála- og reksturs. Ef engin verðlisti er til staðar fyrir tiltekinn gjaldmiðil verður verðlisti sjálfkrafa búinn til og afurðinni verður úthlutað á hann.

Núverandi innleiðing á viðbótum tvöfaldrar skráningar sem tengir sjálfgefinn verðlista við uppflettieininguna fyrir gjaldmiðilinn sem tengist forriti fjármála- og reksturs og finnur fyrsta verðlistann í forriti viðskiptavinar með því að nota stafrófsröð á heiti verðlistans. Til að stilla sjálfgefinn verðlista fyrir tiltekinn gjaldmiðil þegar margir verðlistar eru til fyrir þann gjaldmiðil þarf að uppfæra heiti verðlistans í heiti sem kemur á undan öllum öðrum verðlistum í stafrófsröð fyrir þennan sama gjaldmiðil. Ef hún er ekki með neinn verðlista fyrir tiltekinn gjaldmiðil er nýr búinn til.

Sjálfgefið er að vörur úr forritum fjármála- og reksturs eru samstilltar við önnur Dynamics 365 forrit með stöðuna **Drög**. Til að samstilla vöruna við stöðuna **Virkt**, svo að þú getir til dæmis notað hana beint í sölupöntunartilboðum þarf að velja eftirfarandi stillingu: **Kerfið> Stjórnun> Kerfisstjórnun> Kerfisstillingar> Sala** og velja **Stofna vörur í virkri stöðu = já**.

Þegar afurðir eru samstilltar verður að færa inn gildi fyrir reitinn **Sölueining** í forriti fjármála- og reksturs vegna þess að hann er áskilinn reitur í Sales.

Stofnun afurðafjölskyldna úr Dynamics 365 Sales er ekki studd með samstillingu tvöfaldrar skráningar fyrir afurðir.

Samstilling afurða gerist frá forriti fjármála- og reksturs til Dataverse. Þetta þýðir að hægt er að breyta töfludálkinum afurðaeiningar í Dataverse, en þegar samstillingu er hrundið af stað (þegar afurðardálki er breytt í forriti fjármála- og reksturs) mun þetta skrifa yfir gildin í Dataverse.

Forrit fyrir fjármál- og rekstur | Forrit viðskiptavinatengsla |
---|---
[CDS-útgefnar einkvæmar afurðir](mapping-reference.md#213) | Afurð |
[Útgefnar afurðir V2](mapping-reference.md#189) | msdyn_sharedproductdetails |
[Allar afurðir](mapping-reference.md#138) | msdyn_globalproducts |

## <a name="product-dimensions"></a>Afurðarvíddir

Afurðavíddir eru einkenni sem auðkenna afurðarafbrigði. Fjórar vöruvíddir (Litur, Stærð, Stíll og Stilling) er einnig varpað á Dataverse til að skilgreina afbrigði afurða. Eftirfarandi mynd sýnir gagnalíkanið fyrir afurðavíddina Litur. Sama líkani er beitt á stærðir, stíl og stillingar.

![Gangalíkan fyrir afurðavíddir.](media/dual-write-product-two.png)

Forrit fyrir Finance and Operations | Forrit viðskiptavinatengsla |
---|---
[Litir](mapping-reference.md#170) | msdyn\_productcolors
[Stærðir](mapping-reference.md#174) | msdyn\_productsizes
[Stílar](mapping-reference.md#178) | msdyn\_productstyles
[Afbrigði](mapping-reference.md#171) | msdyn\_productconfigurations

Þegar afurð hefur mismunandi afurðavíddir (til dæmis hefur afurðarsniðmát stærð og lit sem afurðavíddir) er hver einkvæm afurð (það er hvert afurðarafbrigði) skilgreind sem samsetning þessara afurðavíddar. Til dæmis er afurðanúmer B0001 extra-lítill svartur bolur og afurðanúmer B0002 er lítill svartur bolur. Í þessu tilfelli eru núverandi samsetningar afurðavíddar skilgreindar. Bolurinn úr dæminu á undan getur til dæmis verið extra-lítill og svartur, lítill og svartur, meðalstór og svartur, eða stór og svartur, en hann getur ekki verið extra-stór og svartur. Með öðrum orðum eru afurðavíddir sem afurðarsniðmát getur notað tilgreindar og hægt er að gefa afbrigði út frá þessum gildum.

Til að halda utan um afurðavíddirnar sem afurðarsniðmát getur tekið, eru eftirfarandi töflur stofnaðar og kortlagðar í Dataverse fyrir hverja afurðarvídd. Frekari upplýsingar eru í [Yfirlit afurðarupplýsinga](../../../../supply-chain/pim/product-information.md).

Forrit fyrir Finance and Operations | Forrit viðskiptavinatengsla |
---|---
[Litir afurðarsniðmáts.](mapping-reference.md#187) | msdyn_sharedproductcolors |
[Skilgreiningar afurðarsniðmáts](mapping-reference.md#188) | msdyn_sharedproductconfigurations |
[Stærðir afurðarsniðmáts](mapping-reference.md#190) | msdyn_sharedproductsizes |
[Stílar afurðarsniðmáts](mapping-reference.md#191) | msdyn_sharedproductstyles |
[Afurðarnúmer sem eru auðkennd með strikamerki](mapping-reference.md#164) | msdyn\_productbarcodes |

## <a name="default-order-settings-and-product-specific-default-order-settings"></a>Sjálfgefnar pöntunarstillingar og afurðatengdar sjálfgefnar pöntunarstillingar

Sjálfgefið pöntunarstillingar skilgreina svæði og vöruhús þar sem afurðir verða upprunnin frá eða geymdar, í lágmarks, hámarks, margar og staðlaðs magns sem verða notuð fyrir viðskipti eða birgðastjórnun, afhendingartíma, stöðvunarflagg, og aðferðina pöntun lofað. Þessar upplýsingar eru aðgengilegar í Dataverse með því að nota sjálfgefnu pöntunarstillingarnar og afurðatengda sjálfgefnr pöntunarstillingaeiningu. Þú getur lesið frekari upplýsingar um virkni í greininni [Sjálfgefnar pöntunarstillingar](../../../../supply-chain/production-control/default-order-settings.md).

Forrit fyrir fjármál- og rekstur | Forrit viðskiptavinatengsla |
---|---
[Sjálfgefnar pöntunarstillingar](mapping-reference.md#172) | msdyn_productdefaultordersettings |
[Sjálfgefnar vörupöntunarstillingar V2](mapping-reference.md#175) | msdyn_productspecificdefaultordersettings |

## <a name="unit-of-measure-and-unit-of-measure-conversions"></a>Mælieining og umreikningur á mælieiningum viðskipta

Mælieiningarnar og umreikningur á þeim eru aðgengilegar í Dataverse eftir gagnalíkaninu sem sýnt er á myndinni.

![Gagnalíkan fyrir mælieiningu.](media/dual-write-product-three.png)

Mælieiningin er samþætt á milli forrita fjármála- og reksturs og annarra forrita Dynamics 365. Fyrir hvern einingaflokk í forriti fjármála- og reksturs er einingahópur búinn til í forriti Dynamics 365, sem hefur að geyma einingar sem tilheyra einingaflokknum. Sjálfgefin grunneining er einnig búin til fyrir hvern einingahóp.

Forrit fyrir Finance and Operations | Forrit viðskiptavinatengsla |
---|---
[Afurðartengdur umreikningur eininga](mapping-reference.md#176) | msdyn_productspecificunitofmeasureconversions |
[Einingar](mapping-reference.md#219) | uoms
[Umreikningur eininga](mapping-reference.md#199) | msdyn_ unitofmeasureconversions

## <a name="initial-synchronization-of-units-data-matching-between-finance-and-operations-and-dataverse"></a>Upphafleg samstilling á samsvörun einingagagna á milli fjármála- og reksturs og Dataverse

### <a name="initial-synchronization-of-units"></a>Upphafleg samstilling á einingum

Þegar tvöföld skrift er virkjuð eru einingar úr fjármála- og reksturs samstilltar við önnur Dynamics 365 forrit. Einingahóparnir sem eru samstilltir úr forritum fjármála- og reksturs í Dataverse eru með fánasett sem gefur til kynna að þeir séu „utanhúss“.

### <a name="matching-units-and-unit-classesgroups-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>Samsvarandi einingar og gögn mælieiningaflokka/flokkar gögn úr fjármála- og reksturs og öðrum Dynamics 365 forritum

Í fyrsta lagi er mikilvægt að hafa í huga að samstillingarlykillinn fyrir eininguna er msdyn_symbol. Þess vegna verður þetta gildi að vera einstakt í Dataverse eða öðrum Dynamics 365 forritum. Þar sem að í öðrum Dynamics 365 forritum er það parið „Kenni einingahóps“ og „Heiti“ sem skilgreinir sérstöðu einingar þarft þú að huga að mismunandi aðstæðum fyrir samsvarandi einingagögn á milli forrita fjármála- og reksturs og Dataverse.

Fyrir samsvarandi/skarandi einingar í forritum fjármála- og reksturs og öðrum Dynamics 365-forritum:

+ **Einingin tilheyrir einingahópi í öðrum Dynamics 365 forritum sem samsvarar tengdum einingaflokki í forrit fjármála- og rekstursum**. Í þessu tilfelli verður að fylla út dálkinn msdyn_symbol í öðrum Dynamics 365 forritum með einingartákninu úr forritum fjármála- og reksturs. Þess vegna, þegar gögnin verða jöfnuð og einingahópurinn stilltur sem „Utanaðkomandi viðhald“ í öðrum Dynamics 365 forritum.
+ **Einingin tilheyrir einingahópi í öðrum Dynamics 365 forritum sem samsvarar ekki tilheyrandi einingaflokki í forritum fjármála- og reksturs (engin núverandi einingaflokkur í forritum fjármála- og reksturs fyrir einingaflokkinn í öðrum Dynamics 365 forritum).** Í þessu tilfelli verður að fylla út msdyn_symbol með streng af handahófi. Athugaðu að þetta gildi verður að vera einstakt í öðrum Dynamics 365 forritum.

Fyrir einingar og einingaflokka í fjármála- og reksturs sem eru ekki til í öðrum Dynamics 365 forritum:

Sem hluti af tvískrifun eru einingarhóparnir úr forritum fjármála- og reksturs og samsvarandi einingar stofnaðar og samstilltar í öðrum Dynamics 365 forritum og Dataverse og einingahópurinn verður stilltur sem „Utanaðkomandi viðhald“. Ekki er þörf á neinu auka átaki fyrir ræsingu.

Fyrir einingar í öðrum forritum Dynamics 365 sem eru ekki til í forritum fjármála- og reksturs:

Fyllt verður út dálkinn msdyn_symbol fyrir allar einingar. Alltaf er hægt að búa til einingarnar í forritum fjármála- og reksturs í samsvarandi einingaflokki (ef þær eru til). Ef einingaflokkur er ekki til verður fyrst að búa til einingaflokkinn (athugaðu að þú getur ekki búið til einingaflokk í forrit fjármála- og rekstursum nema í gegnum viðbót ef þú ert að lengja enum) sem samsvarar hinum Dynamics 365 forritseiningahópnum. Síðan er hægt að stofna eininguna. Athugaðu að einingatáknið í fjármála- og reksturs verður að vera msdyn_symbol sem var áður tilgreint í öðrum Dynamics 365 forritum fyrir eininguna.

## <a name="product-policies-dimension-tracking-and-storage-groups"></a>Afurðastefna: vídd, mælingar og geymsluhópar

Afurðareglurnar eru reglur sem notaðar eru til að skilgreina afurðir og eiginleika þeirra í birgðum. Hægt er að finna afurðavíddarhópinn, afurðarakningarvíddarhópinn og geymsluvíddarhópinn sem afurðareglur.

Forrit fyrir Finance and Operations | Forrit viðskiptavinatengsla |
---|---
[Afurðavíddaflokkar](mapping-reference.md#173) | msdyn\_productdimensiongroups |
[Geymsluvíddarflokkar](mapping-reference.md#177) | msdyn_productstoragedimensiongroups |
[Rakningarvíddarflokkar](mapping-reference.md#179) | msdyn_producttrackingdimensiongroups |

## <a name="product-hierarchies"></a>Afurðarstigveldi

Forrit fyrir Finance and Operations | Forrit viðskiptavinatengsla |
---|---
[Úthlutanir afurðategundar](mapping-reference.md#167) | msdyn_productcategoryassignments |
[Tegundastigveldi afurðar](mapping-reference.md#168) | msdyn_productcategoryhierarchies |
[Hlutverk tegundastigveldis afurðar](mapping-reference.md#169) | msdyn_productcategoryhierarchyroles |

## <a name="integration-key-for-products"></a>Sameiningartakki fyrir vörur

Til að auðkenna vörur á milli Dynamics 365 Finance og vörur í Dataverse eru samstillingarlyklarnir notaðir.
Fyrir afurðir er **(productnumber)** einkvæmur lykill sem auðkennir afurð í Dataverse. Hann er samsettur með samtengingu á: **(company, msdyn_productnumber)**. **Fyrirtækið** gefur til kynna lögaðila í fjármála- og reksturs og **msdyn_productnumber** sýnir vörunúmer fyrir tiltekna vöru í .

Fyrir notendur Dynamics 365 forrits er afurðin auðkennd í UI með **msdyn_productnumber** (athugið að merki dálksins er **Vörunúmer**). Á vöruforminu eru bæði fyrirtækið og msydn_productnumber sýnt. Hins vegar er dálkurinn (productnumber), sem er einstakur lykill fyrir afurð, ekki sýndur.

Ef þú byggir forrit á Dataverse, ættir þú að passa að nota **productnumber** (einkvæmt afurðakenni) sem samþættingarlykill. Ekki nota **msdyn_productnumber** þar sem það er ekki einkvæmt.

## <a name="initial-synchronization-of-products-and-migration-of-data-from-dataverse-to-finance-and-operations"></a>Upphafleg samstilling vöru og flutningur gagna úr Dataverse í fjármála- og reksturs

### <a name="initial-synchronization-of-products"></a>Upphafleg samstilling á afurðum

Þegar tvöföld skráning er virkjuð eru afurðir úr forritum fjármála- og reksturs samstilltar við Dataverse og forrit viðskiptavina. Afurðir stofnaðar í Dataverse og öðrum forritum Dynamics 365 áður en tvöfaldri ritun var gefin út verða ekki uppfærðar eða jafnaðar við afurðaögn úr forritum fjármála- og reksturs.

### <a name="matching-product-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>Samsvarandi vörugögn úr fjármála- og reksturs og öðrum Dynamics 365-forritum

Ef sömu vörur eru geymdar (skarast/samsvara) í fjármála- og reksturs og í Dataverse og öðrum forritum Dynamics 365, þegar gert er ráð fyrir tvíritun samstillingar vara úr fjármála- og reksturs, og tvöfaldar raðir munu birtast í Dataverse fyrir sömu vöru.
Til að forðast fyrri aðstæður, ef önnur Dynamics 365 forrit hafa vörur sem skarast/samsvara við fjármála- og reksturs, verður stjórnandi sem gerir kleift að nota tvískipt ræsingu dálkama **Fyrirtæki** (dæmi: "USMF") og **msdyn_productnumber** (dæmi: "1234:Svartur:S") áður en samstilling vara fer fram. Með öðrum orðum, þessa tvo dálka í afurðinni í Dataverse þarf að fylla út með viðkomandi fyrirtæki í fjármála- og reksturs sem þarf að passa við vöruna og með vörunúmeri hennar.

Þegar samstillingin er virk og fer fram verða vörur úr fjármála- og reksturs samstilltar við samsvarandi vörur í Dataverse og önnur Dynamics 365 forrit. Þetta á bæði við um einkvæmar afurðir og afbrigði afurða.

### <a name="migration-of-product-data-from-other-dynamics-365-apps-to-finance-and-operations"></a>Flutningur á afurðagögnum úr öðrum Dynamics 365 forritum í fjármála- og reksturs

Ef önnur Dynamics 365 forrit eru með vörur sem eru ekki til staðar í fjármála- og reksturs, getur kerfisstjórinn fyrst notað **EcoResReleasedProductCreationV2Entity** til að flytja inn þessar vörur í fjármála- og reksturs. Og í öðru lagi skal jafna afurðagögnin úr fjármálum- og rekstri og önnur Dynamics 365 forrit eins og lýst er hér að ofan.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

