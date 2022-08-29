---
title: Samræmd afurðaupplifun
description: Þessi grein lýsir samþættingu vörugagna milli fjármála- og rekstrarappa og Dataverse.
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
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288923"
---
# <a name="unified-product-experience"></a>Samræmd afurðaupplifun

[!include [banner](../../includes/banner.md)]



Þegar vistkerfi fyrirtækja samanstendur af Dynamics 365 forritum, svo sem Finance, Supply Chain Management og Sales, nota fyrirtæki þessi forrit oft til að fá upplýsingar um vöru. Þetta er vegna þess að þessi forrit bjóða upp á öfluga vöruinnviði ásamt háþróuðum verðlagningarhugtökum og nákvæmum birgðagögnum fyrir lagermagn. Fyrirtæki sem nota utanaðkomandi vörulífsferilsstjórnunarkerfi (PLM) til að útvega vörugögnin geta beint vörum frá fjármála- og rekstrarforritum yfir í önnur Dynamics 365 forrit. Sameinað vöruupplifun færir samþætta vörugagnalíkanið inn í Dataverse, þannig að allir notendur forrita, þ.m.t Power Platform notendur, geta nýtt sér ríkuleg vörugögn sem koma frá fjármála- og rekstraröppum.

Hérna er vöruupplýsingamódelið úr Sales.

![Gagnamódel fyrir vörur í CE.](media/dual-write-product-4.jpg)

Hér er vörugagnalíkanið frá fjármála- og rekstraröppum.

![Gagnalíkan fyrir vörur í fjármálum og rekstri.](media/dual-write-products-5.jpg)

Þessi tvö afurðalíkön hafa verið samþætt í Dataverse eins og sýnt er hér að neðan.

![Gagnamódel fyrir vörur í forritum Dynamics 365.](media/dual-write-products-6.jpg)

Tvískrifa töflukortin fyrir vörur hafa verið hönnuð til að flæða gögnum eingöngu í eina átt, í næstum rauntíma frá fjármála- og rekstrarforritum til Dataverse. Samt sem áður hafa vöruinnviðir verið opnaðir svo að hún verði tvíátta ef þess er krafist. Þó að hægt sé að sérsníða það er það á þína ábyrgð, þar sem Microsoft mælir ekki með þessari aðferð.

## <a name="templates"></a>Sniðmát

Afurðarupplýsingar innihalda allar upplýsingar sem tengjast vörunni og skilgreiningu hennar, svo sem afurðarvíddir eða mælingar og geymsluvíddir. Eins og eftirfarandi tafla sýnir er búið að stofna safn af töflukortum til að samstilla afurðir og tengdar upplýsingar.

Forrit fyrir Finance and Operations | Önnur Dynamics 365 forrit | Lýsing
-----------------------|--------------------------------|---
[Allar afurðir](mapping-reference.md#138) | msdyn_globalproducts | Taflan fyrir allar vörur inniheldur allar vörur sem eru tiltækar í fjármála- og rekstraröppum, bæði útgefnar vörur og vörur sem ekki hafa verið gefnar út.
[CDS-útgefnar einkvæmar afurðir](mapping-reference.md#213) | Afurð | Taflan **Afurð** inniheldur dálkana sem skilgreina afurðina. Hún felur í sér einstakar afurðir (afurðir með undirgerðaafurð) og afurðarafbrigðin. Eftirfarandi tafla sýnir vörpun.
[Litir](mapping-reference.md#170) | msdyn\_productcolors
[Afbrigði](mapping-reference.md#171) | msdyn\_productconfigurations
[Sjálfgefnar pöntunarstillingar](mapping-reference.md#172) | msdyn_productdefaultordersettings |
[Afurðartegundir](mapping-reference.md#166) | msdyn_productcategories | Hver vöruflokkur og upplýsingar um uppbyggingu hans og einkenni eru að finna í vöruflokkstöflunni.
[Úthlutanir afurðategundar](mapping-reference.md#167) | msdyn_productcategoryassignments | Til að úthluta vöru í flokk er hægt að nota töfluna fyrir vöruflokkaúthlutanir.
[Tegundastigveldi afurðar](mapping-reference.md#168) | msdyn_productcategoryhierarchies | Stigveldi afurðar eru notuð til að flokka eða flokka afurðir. Flokkastigveldin eru fáanleg í Dataverse með því að nota töflu tegundastigveldi afurðar.
[Hlutverk tegundastigveldis afurðar](mapping-reference.md#169) | msdyn_productcategoryhierarchyroles | Hægt er að nota afurðastigveldi fyrir mismunandi hlutverk í D365 fjármálum og rekstri. Þau tilgreina hvaða flokkur er notaður í hverju hlutverki hlutverkatöflu afurðaflokks er notaður.
[Sjálfgefnar vörupöntunarstillingar V2](mapping-reference.md#175) | msdyn_productspecificdefaultordersettings |
[Afurðavíddaflokkar](mapping-reference.md#173) | msdyn\_productdimensiongroups | Afurðavíddarhópurinn skilgreindi hvaða afurðavíddir skilgreina vöruna.
[Litir afurðarsniðmáts.](mapping-reference.md#187) | msdyn_sharedproductcolors | Taflan **Sameiginlegur afurðalitur** gefur til kynna liti sem sérstakt afurðarsniðmát getur haft. Þetta hugtak er flutt í Dataverse til að halda gögnum samkvæmum.
[Skilgreiningar afurðarsniðmáts](mapping-reference.md#188) | msdyn_sharedproductconfigurations | Taflan **Sameiginleg skilgreining afurða** gefur til kynna skilgreiningar sem sérstakt afurðarsniðmát getur haft. Þetta hugtak er flutt í Dataverse til að halda gögnum samkvæmum.
[Stærðir afurðarsniðmáts](mapping-reference.md#190) | msdyn_sharedproductsizes | Taflan **Sameiginleg afurðastærð** gefur til kynna stærðir sem sérstakt afurðarsniðmát getur haft. Þetta hugtak er flutt í Dataverse til að halda gögnum samkvæmum.
[Stílar afurðarsniðmáts](mapping-reference.md#191) | msdyn_sharedproductstyles | Taflan **Sameiginlegur afurðastíll** gefur til kynna stíla sem sérstakt afurðarsniðmát getur haft. Þetta hugtak er flutt í Dataverse til að halda gögnum samkvæmum.
[Afurðarnúmer sem eru auðkennd með strikamerki](mapping-reference.md#164) | msdyn\_productbarcodes | Strikamerki afurða eru notuð til að bera kennsl á afurðir á einkvæman hátt.
[Afurðartengdur umreikningur eininga](mapping-reference.md#176) | msdyn_productspecificunitofmeasureconversions |
[Útgefnar afurðir V2](mapping-reference.md#189) | msdyn\_sharedproductdetails | The **msdyn\_ samnýtt vöruupplýsingar** taflan inniheldur dálka úr fjármála- og rekstraröppum sem skilgreina vöruna og innihalda fjárhags- og stjórnunarupplýsingar vörunnar.
[Stærðir](mapping-reference.md#174) | msdyn\_productsizes
[Geymsluvíddarflokkar](mapping-reference.md#177) | msdyn_productstoragedimensiongroups | Víddarhópur afurðageymslu táknar aðferðina sem notuð er til að skilgreina staðsetningu afurðarinnar í vöruhúsinu.
[Stílar](mapping-reference.md#178) | msdyn\_ vörustílum
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

Með tvískrifavirknina virka verða vörurnar úr fjármálum og rekstri samstilltar í aðrar Dynamics 365 vörur í **Drög** ríki. Þeim er bætt við fyrsta verðlistann með sama gjaldmiðil og er notaður í forriti viðskiptavinar og raðar heiti verðlista eftir stafrófsröð. Með öðrum orðum, þeim er bætt við fyrsta verðlistann í Dynamics 365 appi sem passar við gjaldmiðil lagatöflunnar þinnar þar sem varan er gefin út í fjármála- og rekstrarappi. Ef engin verðlisti er til staðar fyrir tiltekinn gjaldmiðil verður verðlisti sjálfkrafa búinn til og afurðinni verður úthlutað á hann.

Núverandi útfærsla á tvískriftarviðbótunum sem tengja sjálfgefna verðskrána við eininguna flettir upp gjaldmiðlinum sem tengist fjármála- og rekstrarappinu og finndu fyrsta verðlistann í forritinu fyrir þátttöku viðskiptavina með því að nota stafrófsröðun á nafni verðlista. Til að stilla sjálfgefinn verðlista fyrir tiltekinn gjaldmiðil þegar margir verðlistar eru til fyrir þann gjaldmiðil þarf að uppfæra heiti verðlistans í heiti sem kemur á undan öllum öðrum verðlistum í stafrófsröð fyrir þennan sama gjaldmiðil. Ef hún er ekki með neinn verðlista fyrir tiltekinn gjaldmiðil er nýr búinn til.

Sjálfgefið er að vörur úr fjármála- og rekstrarforritum eru samstilltar við önnur Dynamics 365 forrit í **Drög** ríki. Til að samstilla vöruna við stöðuna **Virkt**, svo að þú getir til dæmis notað hana beint í sölupöntunartilboðum þarf að velja eftirfarandi stillingu: **Kerfið> Stjórnun> Kerfisstjórnun> Kerfisstillingar> Sala** og velja **Stofna vörur í virkri stöðu = já**.

Þegar vörur eru samstilltar verður þú að slá inn gildi fyrir **Sölueining** reit í fjármála- og rekstrarappinu, því það er skyldureitur í sölu.

Stofnun afurðafjölskyldna úr Dynamics 365 Sales er ekki studd með samstillingu tvöfaldrar skráningar fyrir afurðir.

Samstilling vara á sér stað frá fjármála- og rekstrarappinu til Dataverse. Þetta þýðir að hægt er að breyta gildum dálka vörutöflunnar Dataverse, en þegar samstillingin er ræst (þegar vörudálki er breytt í fjármála- og rekstrarappi) mun þetta skrifa yfir gildin í Dataverse.

Forrit fyrir Finance and Operations | Forrit viðskiptavinatengsla |
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
[Stílar](mapping-reference.md#178) | msdyn\_ vörustílum
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

Sjálfgefið pöntunarstillingar skilgreina svæði og vöruhús þar sem afurðir verða upprunnin frá eða geymdar, í lágmarks, hámarks, margar og staðlaðs magns sem verða notuð fyrir viðskipti eða birgðastjórnun, afhendingartíma, stöðvunarflagg, og aðferðina pöntun lofað. Þessar upplýsingar eru aðgengilegar í Dataverse með því að nota sjálfgefnu pöntunarstillingarnar og afurðatengda sjálfgefnr pöntunarstillingaeiningu. Þú getur lesið frekari upplýsingar um virknina í [Grein um sjálfgefnar pöntunarstillingar](../../../../supply-chain/production-control/default-order-settings.md).

Forrit fyrir Finance and Operations | Forrit viðskiptavinatengsla |
---|---
[Sjálfgefnar pöntunarstillingar](mapping-reference.md#172) | msdyn_productdefaultordersettings |
[Sjálfgefnar vörupöntunarstillingar V2](mapping-reference.md#175) | msdyn_productspecificdefaultordersettings |

## <a name="unit-of-measure-and-unit-of-measure-conversions"></a>Mælieining og umreikningur á mælieiningum viðskipta

Mælieiningarnar og umreikningur á þeim eru aðgengilegar í Dataverse eftir gagnalíkaninu sem sýnt er á myndinni.

![Gagnalíkan fyrir mælieiningu.](media/dual-write-product-three.png)

Mælieiningarhugtakið er samþætt á milli fjármála- og rekstrarforrita og annarra Dynamics 365 forrita. Fyrir hvern einingaflokk í fjármála- og rekstrarappi er stofnaður einingahópur í Dynamics 365 appi sem inniheldur einingar sem tilheyra einingaflokknum. Sjálfgefin grunneining er einnig búin til fyrir hvern einingahóp.

Forrit fyrir Finance and Operations | Forrit viðskiptavinatengsla |
---|---
[Afurðartengdur umreikningur eininga](mapping-reference.md#176) | msdyn_productspecificunitofmeasureconversions |
[Einingar](mapping-reference.md#219) | uoms
[Umreikningur eininga](mapping-reference.md#199) | msdyn_ unitofmeasureconversions

## <a name="initial-synchronization-of-units-data-matching-between-finance-and-operations-and-dataverse"></a>Upphafleg samstilling eininga gagnasamsvörun milli fjárhags og rekstrar og Dataverse

### <a name="initial-synchronization-of-units"></a>Upphafleg samstilling á einingum

Þegar tvískrifað er virkt eru einingar úr fjármála- og rekstrarforritum samstilltar við önnur Dynamics 365 forrit. Einingaflokkarnir samstilltir úr fjármála- og rekstraröppum í Dataverse hafa fána sett sem gefur til kynna að þeir séu "viðhaldnir að utan".

### <a name="matching-units-and-unit-classesgroups-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>Samsvörun einingar og einingaflokka/hópa gögn úr fjármálum og rekstri og öðrum Dynamics 365 forritum

Í fyrsta lagi er mikilvægt að hafa í huga að samstillingarlykillinn fyrir eininguna er msdyn_symbol. Þess vegna verður þetta gildi að vera einstakt í Dataverse eða öðrum Dynamics 365 forritum. Vegna þess að í öðrum Dynamics 365 öppum eru það pörin „Unit group ID“ og „Name“ sem skilgreina sérstöðu einingu, þá þarf að huga að mismunandi atburðarásum til að passa einingagögn milli fjármála- og rekstrarappa og Dataverse.

Fyrir einingar sem passa/skarast í fjármála- og rekstrarforritum og öðrum Dynamics 365 forritum:

+ **Einingin tilheyrir einingahópi í öðrum Dynamics 365 öppum sem samsvarar tilheyrandi einingaflokki í fjármála- og rekstraröppum**. Í þessu tilviki verður að fylla út dálkinn msdyn_symbol í öðrum Dynamics 365 forritum með einingatákninu frá fjármála- og rekstrarforritum. Þess vegna, þegar gögnin verða jöfnuð og einingahópurinn stilltur sem „Utanaðkomandi viðhald“ í öðrum Dynamics 365 forritum.
+ **Einingin tilheyrir einingaflokki í öðrum Dynamics 365 forritum sem samsvarar ekki tengdum einingaflokki í fjármála- og rekstraröppum (enginn fyrirliggjandi einingaflokkur í fjármála- og rekstraröppum fyrir einingaflokkinn í öðrum Dynamics 365 forritum).** Í þessu tilfelli verður að fylla út msdyn_symbol með streng af handahófi. Athugaðu að þetta gildi verður að vera einstakt í öðrum Dynamics 365 forritum.

Fyrir einingar og einingaflokka í fjármálum og rekstri sem ekki eru til í öðrum Dynamics 365 forritum:

Sem hluti af tvískrifa eru einingahóparnir úr fjármála- og rekstrarforritum og samsvarandi einingar búnar til og samstilltar í öðrum Dynamics 365 forritum og Dataverse og einingahópurinn verður stilltur sem "Viðhald að utan". Ekki er þörf á neinu auka átaki fyrir ræsingu.

Fyrir einingar í öðrum Dynamics 365 forritum sem eru ekki til í fjármála- og rekstrarforritum:

Fyllt verður út dálkinn msdyn_symbol fyrir allar einingar. Einingarnar er alltaf hægt að búa til í fjármála- og rekstraröppum í samsvarandi einingaflokki (ef hann er til). Ef einingaflokkurinn er ekki til verður fyrst að búa til einingaflokkinn (athugið að þú getur ekki búið til einingaflokk í fjármála- og rekstrarforritum nema með framlengingu ef þú ert að lengja upptalninguna) sem samsvarar hinum Dynamics 365 forritaeiningahópnum. Síðan er hægt að stofna eininguna. Athugaðu að einingatáknið í fjármála- og rekstrarforritum verður að vera msdyn_symbol sem áður var tilgreint í öðrum Dynamics 365 forritum fyrir eininguna.

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

Til að bera kennsl á vörur á milli Dynamics 365 Finance og vara í Dataverse samþættingarlyklarnir eru notaðir.
Fyrir afurðir er **(productnumber)** einkvæmur lykill sem auðkennir afurð í Dataverse. Hann er samsettur með samtengingu á: **(company, msdyn_productnumber)**. The **fyrirtæki** gefur til kynna lögaðila í fjármálum og rekstri og **msdyn_vörunúmer** gefur til kynna vörunúmer viðkomandi vöru í fjármálum og rekstri.

Fyrir notendur Dynamics 365 forrits er afurðin auðkennd í UI með **msdyn_productnumber** (athugið að merki dálksins er **Vörunúmer**). Á vöruforminu eru bæði fyrirtækið og msydn_productnumber sýnt. Hins vegar er dálkurinn (productnumber), sem er einstakur lykill fyrir afurð, ekki sýndur.

Ef þú byggir forrit á Dataverse, ættir þú að passa að nota **productnumber** (einkvæmt afurðakenni) sem samþættingarlykill. Ekki nota **msdyn_productnumber** þar sem það er ekki einkvæmt.

## <a name="initial-synchronization-of-products-and-migration-of-data-from-dataverse-to-finance-and-operations"></a>Upphafleg samstilling afurða og flutningur gagna frá Dataverse til fjármögnunar og rekstrar

### <a name="initial-synchronization-of-products"></a>Upphafleg samstilling á afurðum

Þegar tvískrifað er virkt eru vörur úr fjármála- og rekstrarforritum samstilltar við Dataverse og þátttökuforrit viðskiptavina. Vörur búnar til í Dataverse og önnur Dynamics 365 forrit áður en dual-write var gefið út verða ekki uppfærð eða samræmd við vörugögn úr fjármála- og rekstraröppum.

### <a name="matching-product-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>Samsvörun vörugagna frá fjármálum og rekstri og öðrum Dynamics 365 forritum

Ef sömu vörur eru hafðar (skarast/samsvörun) í fjármálum og rekstri og í Dataverse og önnur Dynamics 365 forrit, þegar tvískrift er virkjað mun samstilling afurða úr fjármálum og rekstri eiga sér stað og tvíteknar línur birtast í Dataverse fyrir sömu vöru.
Til að forðast fyrri aðstæður, ef önnur Dynamics 365 forrit eru með vörur sem skarast/samræmast fjármálum og rekstri, þá verður kerfisstjórinn sem virkjar tvöfalda ritun að ræsa dálkana **Fyrirtæki** (dæmi: "USMF") og **msdyn_vörunúmer** (dæmi: "1234:Black:S") áður en samstilling vöru fer fram. Með öðrum orðum, þessir tveir dálkar í vörunni í Dataverse skal fylla út hjá viðkomandi fyrirtæki í fjármálum og rekstri sem þarf að passa vöruna við og með vörunúmeri hennar.

Síðan, þegar samstillingin er virkjuð og fer fram, verða vörurnar úr fjármálum og rekstri samstilltar við samsvarandi vörur í Dataverse og önnur Dynamics 365 forrit. Þetta á bæði við um einkvæmar afurðir og afbrigði afurða.

### <a name="migration-of-product-data-from-other-dynamics-365-apps-to-finance-and-operations"></a>Flutningur vörugagna úr öðrum Dynamics 365 forritum yfir í fjármál og rekstur

Ef önnur Dynamics 365 forrit eru með vörur sem eru ekki til staðar í fjármálum og rekstri getur stjórnandinn fyrst notað **EcoReleasedProductCreationV2Entity** vegna innflutnings á þeim vörum í fjármálum og rekstri. Og í öðru lagi, passaðu vörugögnin úr fjármálum og rekstri og öðrum Dynamics 365 forritum eins og lýst er hér að ofan.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

