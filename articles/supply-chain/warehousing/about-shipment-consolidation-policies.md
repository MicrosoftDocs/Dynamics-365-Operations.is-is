---
title: Samstæðureglur sendingar
description: Í þessu efnisatriði er að finna yfirlit yfir virkni sem býður upp á sveigjanlega skilgreiningu samstæðureglna sendinga.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSShipConsolidationError, WHSShipConsolidationSetShipment, WHSShipConsolidationPolicySelect, WHSShipPlanningListPage, TMSCarrierGroup, WHSShipConsolidationTemplate, WHSShipConsolidationTemplateApply, WHSShipConsolidationTemplateCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: f895b13b2e11d4cb341f80b3cfeb40ed998ccfc4
ms.sourcegitcommit: d9bffbeae2ba14f06294dd275383077d4d65c4fa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/01/2020
ms.locfileid: "4654221"
---
# <a name="shipment-consolidation-policies"></a>Samstæðureglur sendingar

Samstæðuferli sendingar sem notar samstæðureglur sendingar leyfa sjálfvirka samstæðu sendingar við sjálfvirka og Handvirk losun í vöruhúsið. Sjálfvirka samstæðan sem var tiltæk áður en þessi eiginleiki var kynntur var með harðkóðuð svæði og var byggður á **samstæða sendingar við losun í vöruhús** reitinum sem var stillt fyrir Vöruhús.

Samstæðureglur sendingar eru notaðar fyrir eftirfarandi virkni:

- Runuvinnsla fyrir sjálfvirka losun í vöruhúsi
- **Losun í vöruhúsi** skipun í sölupöntun eða flutningspöntun
- Tilgreind **losun í vöruhúsi** síða
- **Losunin í vöruhúsi** skipunin á síðunni **vinnusvæði farmáætlunar**
- Handvirk samstæða sendinga á síðunum **samstæða sendinga** og **vinnusvæði samstæðu sendinga**

Áður en samstæðuregla sendingar var kynnt, er aðgerðin samstæðuaðgerð innt af hendi sem stilling á stigi vöruhúss. Allar pantanir fyrir alla viðskiptavini úr einu vöruhúsi voru meðhöndlaðar eins og þær hefðu sömu samstæðukröfur. Reglur um samstæðu sendinga bæta við stuðningi við aðstæður þar sem mismunandi fyrirtæki hafa ólíkar þarfir fyrir samstæðu sendinga.

Fyrirspurnir eru notaðar til að auðkenna samstæðureglu sendingar sem gildir, og síðan breytanleg Samstæða reita ákvarðar hvernig farmlínur eru flokkaðar á afhendingarstigið. (Þetta mynstur líkist mynstri sem bylgjusniðmátin fylgja.) Að auki hefur valkostinum **sameina við fyrirliggjandi sendingar** verið bætt við hverja reglu. Þegar kveikt er á þessum valkosti mun ferlið *losun í vöruhúsi* finna sendingar fyrir samstæðu með því að leita í fyrirliggjandi sendingum sem voru stofnaðar út frá sömu samstæðureglu. Í þessu tilviki mun kerfið velja fyrirliggjandi sendingu eða farm í stað þess að búa til nýja. Kerfið mun hins vegar aðeins sameina við fyrirliggjandi sendingar sem eru með stöðuna *opið*; sendingar sem tilheyra bylgjuútgáfu með stöðuna *losað* eða hærra verða ekki taldar sem markmið fyrir samstæðu.

Þegar samstæðureglur sendingar eru gerðar tiltækar er stillingin **samstæða sendingar við losun í vöruhús** sem var áður tiltæk á uppsetningarsíðu **vöruhúss** hulin. Til að aðstoða við umbreytingu í nýja samstæðueiginleika sendingar er aðgerð á síðu **samstæðureglna sendingar** sem stofnar sjálfgefin regla sem inniheldur sjálfkrafa gömlu stillingarnar fyrir núverandi vöruhús. Eftir að þessi sjálfgefna regla er stofnuð er stillingin **Taka sendingu með í samstæðu við losun í vörugeymslu** á uppsetningarsíðunni **Vöruhús** ekki lengur tekin til greina.

Hægt er að nota síðuna **Losa í vöruhús** til að hnekkja handvirkt viðeigandi samstæðureglu á sama hátt og hægt er að hnekkja uppfyllingarreglum.

Hægt er að nota skipunina **Losa \> Losa í vöruhús** á síðunni **Vinnusvæði hleðsluáætlunar** til að búa til hleðslu á útleið sem byggist á sölupöntunum og flutningspöntunarlínum áður en losað er í vöruhúsið. Þessar hleðslur nota sömu samstæðurök og fram komu með samstæðu sendingarreglna.

Hægt er að nota síðuna **Samstæðuvinnusvæði sendinga** til að sameina fyrirliggjandi sendingar sem hafa ekki enn verið staðfestar en hafa þegar verið losaðar í vöruhúsið. Þessi virkni styður aðstæður þar sem sjálfvirka losunarferlið, sem er með eigin sendingarsamstæðu, er keyrt mörgum sinnum á dag, en hugsanlegar viðbótarsamstæður eru auðkenndar handvirkt áður en sendingunni til flutningsaðila er lokið meðan á staðfestingarferlinu stendur. Þessi virkni býður upp á samstæðu sendinga á útleið sem eru stofnaðar úr sölupöntunar- eða flutningspöntunarlínum hvenær sem er eftir að sendingar eru losaðar í vöruhúsið en áður en þær eru staðfestar.

Síðan **Samstæðuvinnusvæði sendinga** virkar eins og hleðsluvinnusvæði, þar sem hægt er að meta skoða sendingar á sama tíma og úthluta ekki pöntunum sem ekki eru samstæðupantanir á tiltekna sendingu. Hægt er að nota samstæðusniðmát sendinga til að meta tillögur um sameiningu mörgum sinnum og staðfesta þær. Sumar reglur eru innleiddar til að koma í veg fyrir óleyfilega samstæðu og til að vara við hugsanlegum villum.

## <a name="overview-of-new-functionality"></a>Yfirlit yfir nýja virkni

Þessi hluti lýsir þeim síðum, skipunum og eiginleikum sem eru breytt eða hefur verið bætt við þegar kveikt er á eiginleikanum *Samstæðureglur sendingar* og hann notaður.

### <a name="shipment-consolidation-policies-page"></a>Síða samstæðureglna sendingar

Reglur eru flokkaðar eftir gerð verkbeiðni. Gerðin **Sölupantanir** stendur fyrir sendingar í _Sölupöntun_ og gerðin **Flutningspantanir** stendur fyrir sendingar í _Flutningsútgáfa_.

Sérhver samstæðuregla sendingar er með fyrirspurn sem skilgreinir hvenær hún er notuð og raðnúmer sem ákvarðar keyrslupöntunina. Samstæða er notuð fyrir hverja einstaka samsetningu valinna reita. Önnur færibreyta sem er gefin upp er notuð fyrir samstæðu með fyrirliggjandi sendingum (opnum). Reglurnar eru metnar og notaðar í hvert skipti sem ný sending er stofnuð (fyrir bylgjuvinnslu).

Ef reglu vantar í eitthvert skyldusvæði eða ef hún inniheldur bönnuð svæði er reglan merkt sem ógild í hlutanum **Valið**. Listarnir yfir áskilin og bönnuð svæði eru harðkóðaðir og hægt er að stækka þá.

Eftirfarandi listi sýnir áskilin svæði. Vegna þess að sendingum er alltaf skipt út fyrir þessum svæðum er ekki hægt að flokka margar sendingar með ólík gildi fyrir þessi svæði.

- Fyrir sölupantanir:

    - **Reikningsnúmer:** _WHSShipmentTable.AccountNum_
    - **Viðtakandi afhendingar:** _WHSShipmentTable.DeliveryName_
    - **Póstfang (RecId):** _WHSShipmentTable.DeliveryPostalAddress_
    - **Vöruhús:** _WHSShipmentTable.InventLocationId_

- Fyrir flutningspantanir:

    - **Frá vöruhúsi:** _InventTransferTable.InventLocationIdFrom_
    - **Í vöruhús:** _InventTransferTable.InventLocationIdTo_

Eftirfarandi reitir eru ekki í boði fyrir allar skjalagerðir. Þessir reitir eru ekki sýnilegir í notandaviðmóti og ekki er hægt að nota þá fyrir samstæðu.

- **Sendingarkenni:** _WHSShipmentTable.ShipmentId_
- **Staða:** _WHSShipmentTable.ShipmentStatus_
- **Samstæðuregla sendingar:** _WHSShipmentTable.ShipConsolidationPolicyName_
- **Vinnufærslugerð:** _WHSShipmentTable.WorkTransType_
- **Bylgjukenni:** _WHSShipmentTable.WaveId_
- **Hleðsluauðkenni:** _WHSShipmentTable.LoadId_
- **Sendingarkenni:** _WHSLoadLine.ShipmentId_
- **Hleðsluauðkenni:** _WHSLoadLine.LoadId_

Þegar regla er stofnuð er hópur áskilinna reita sjálfgefið notaður sem samstæðureitir. Hins vegar er hægt að breyta listanum með því að nota vinstri og hægri örvahnappana. (Ferlið líkist ferlinu við val á aðferðunum í bylgjusniðmátum.)

Gildin sem notendur velja fyrir þessa reiti verða notuð fyrir allar nýlega stofnaðar sendingar eða þeim verður bætt við fyrirliggjandi sendingar meðan á samstæðu stendur með þessar sendingar. Þegar tvær sendingar hafa sama gildi fyrir reit sem er valin fyrir samstæðu þessara sendinga eru sendingarnar sameinaðar. Sama regla gildir fyrir alla síðari samstæðureiti sem eru valdir. Ef gildin eru önnur er annarri sendingunni fleygt og hún verður valin fyrir nýja sendingu. Sjálfvirka samstæðuferlið felst í því að stofna allar einkvæmar samsetningar gilda fyrir samstæðureiti sendingar og úthluta svo sendingu á viðeigandi samsetningu.

Reitir sem ekki eru valdir eru hunsaðir við samstæðuferlið. Ef tvær sendingar hafa mismunandi gildi fyrir reit sem ekki er valinn er reiturinn hreinsaður (þ.e. hafður auður). Ef báðar sendingarnar hafa sama gildi fyrir svæði sem er ekki valið er reiturinn fylltur út.

Listi yfir samstæðureiti (þ.e. reitir sem verða hreinsaðir ef þeir hafa mismunandi gildi) eru harðkóðaðir. Listinn inniheldur alla reiti sem eru frumstilltir á sölupöntunar- eða flutningspöntunarlínu þegar ný sending er stofnuð. Ef reitur er ekki frumstilltur úr sölupöntunar- eða flutningspöntunarlínu er hann þannig hunsaður þegar nýjum gögnum er bætt við fyrirliggjandi sendingu.

### <a name="release-to-warehouse-page"></a>Losa í vöruhúsasíðu

- Nýr reitur í neðra hnitanetinu sýnir samstæðuregluna sem var notuð.
- Nýr hnappur gerir notanda kleift að velja og/eða hnekkja samstæðureglunni handvirkt.

### <a name="release-to-warehouse-command-on-the-load-planning-workbench-page"></a>Skipunin „Losa í vöruhús“ á síðunni „Vinnusvæði hleðsluáætlunar“

- Rökin voru leiðrétt þannig að þau nota samstæðureglur í notkun.
- Sendingar eru nú sameinaðar innan einnar hleðslu.

### <a name="consolidate-shipments-page"></a>Síða sameiningar sendingar

- Leitinni að svipuðum sendingum (þ.e. mögulegum sendingum fyrir sameiningu) var breytt þannig að hún notar reiti sem eru valdir í samstæðureglu sendingar.
- Reitir sem hafa mismunandi gildi í mismunandi sendingum eru nú auðir. (Áður voru gildin úr völdu „grunnsendingunni“ notuð.)

### <a name="shipment-consolidation-workbench-page"></a>Síða samstæðuvinnusvæðis sendinga

- Ný virkni endurgerir ferli handvirkrar samstæðu á stærri kvarða.
- Nú er hægt að opna þessa síðu af valmyndinni **Losa í vöruhús** í einingunni **Vöruhúsakerfi**.
- Reikniritið greinir fyrirliggjandi sendingar sem hafa ekki enn verið sendar. Það leggur svo til samstæðu, byggt á reitum sem eru valdir í samstæðureglum.

## <a name="comparison-of-functionality"></a>Samanburður á virkni

Eftirfarandi tafla sýnir samantekt á því hvernig sendingarsamstæða virkar þegar ekki eru notaðar samstæðureglur sendingar og þegar þær eru notaðar.

| Án samstæðureglna sendingar | Með samstæðureglum sendingar |
|---|----|
| Ekki tiltækt | Sölu- eða flutningsendingar sem eru valdar fyrir samstæðu verða að hafa sömu samstæðureglu og sendingin sem verið er að stofna, eða að öðrum kosti vera úthlutað á opna sendingu (þegar kveikt er á valkostinum **Samstæða með fyrirliggjandi sendingum**). |
| Ferlið *Losa í vöruhús* leitar ekki í fyrirliggjandi sendingum til að finna sendingu fyrir samstæðu. Aðeins sendingar sem eru stofnaðar með núverandi tilviki ferlisins *Losa í vöruhús* eru notaðar til að finna sendingu fyrir samstæðu. | Ef kveikt er á valkostinum **Samstæða með fyrirliggjandi sendingum** fyrir samstæðureglu sem verið er að nota leitar ferlið *Losa í vöruhús* í fyrirliggjandi sendingum sem voru stofnaðar á grundvelli sömu samstæðureglu til að finna sendingu fyrir samstæðu. Þess vegna, ef um er að ræða tvær reglur, verður sending sem verið er að stofna á grundvelli reglu 2 aldrei notuð í samstæðum með sendingu sem var búin til samkvæmt reglu 1. |
| Ekki tiltækt | Ef listi yfir reiti samstæðureglu er auður eða ef ekki er hægt að finna reglu er ný sending stofnuð fyrir hverja sölupöntunar- eða flutningspöntunarlínu. |
| Eftirfarandi samstæðureitur skilgreinir einkvæma samsetningu gilda sem notuð er til að sameina sendingar fyrir *flutningslínu*. (Allir aðrir reitir eru hunsaðir.)<ul><li>Pöntunarnúmer (OrderNum)</li></ul> | Eftirfarandi samstæðureitir skilgreina einkvæma samsetningu gilda sem notuð er til að sameina sendingar fyrir *flutningslínu*. (Allir aðrir reitir eru hunsaðir.)<ul><li>Pöntunarnúmer (OrderNum)</li><li>Viðtakandi sendingar (DeliveryName)</li><li>Póstfang (DeliveryPostalAddress)</li><li>ISO-landskóði (CountryRegionISOCode)</li><li>Heimilisfang (Address)</li><li>Svæði (InventSiteId)</li><li>Vöruhús (InventLocationId)</li><li>Farmflytjandi (CarrierCode)</li><li>Flutningsþjónusta (CarrierServiceCode)</li><li>Afhendingarmáti (ModeCode)</li><li>Flutningsaðilaflokkur (CarrierGroupCode)</li><li>Afhendingarskilmálar (DlvTermId)</li></ul>Þessir reitir eru einu reitirnir sem eru í boði og frumstilltir þegar ný sending er stofnuð. |
| Eftirfarandi samstæðureitir skilgreina einkvæma samsetningu gilda sem notuð er til að sameina sendingar fyrir *sölulínu*. (Allir aðrir reitir eru hunsaðir.)<ul><li>Pöntunarnúmer (OrderNum)</li><li>Tilvísun viðskiptavinar (CustomerRef)</li><li>Innkaupabeiðni viðskiptavinar (CustomerReq)</li><li>Afhendingarskilmálar (DlvTermId)</li></ul> | Eftirfarandi samstæðureitir skilgreina einkvæma samsetningu gilda sem notuð er til að sameina sendingar fyrir *sölulínu*. (Allir aðrir reitir eru hunsaðir.)<ul><li>Pöntunarnúmer (OrderNum)</li><li>Reikningsnúmer (AccountNum)</li><li>Viðtakandi sendingar (DeliveryName)</li><li>Póstfang (DeliveryPostalAddress)</li><li>ISO-landskóði (CountryRegionISOCode)</li><li>Heimilisfang (Address)</li><li>Svæði (InventSiteId)</li><li>Vöruhús (InventLocationId)</li><li>Farmflytjandi (CarrierCode)</li><li>Flutningsþjónusta (CarrierServiceCode)</li><li>Afhendingarmáti (ModeCode)</li><li>Flutningsaðilaflokkur (CarrierGroupCode)</li><li>Kenni miðlara (BrokerCode)</li><li>Stefna (LoadDirection)</li><li>Afhendingarskilmálar (DlvTermId)</li><li>Tilvísun viðskiptavinar (CustomerRef)</li><li>Innkaupabeiðni viðskiptavinar (CustomerReq)</li></ul>Þessir reitir eru einu reitirnir sem eru í boði og frumstilltir þegar ný sending er stofnuð. |
| Ekki tiltækt | Eftirfarandi samstæðureitir eru áskildir fyrir *sölulína* og ekki er hægt að fjarlægja þá:<ul><li>Reikningsnúmer (AccountNum)</li><li>Viðtakandi sendingar (DeliveryName)</li><li>Póstfang (DeliveryPostalAddress)</li><li>Vöruhús (InventLocationId)</li></ul>Sjálfgefið er að þessum reitum sé úthlutað þegar ný regla er stofnuð. Ekki er hægt að fjarlægja þá. |
| Ferlið *Losun hleðslna í vöruhús* á síðunni **Vinnusvæði hleðsluáætlunar** notar eigin aðskilda kóða til að stofna sendingar og bylgjur. | Samstæðureglur sendinga eru notaðar til að ákvarða hvaða reiti skal meta fyrir samstæðu. Sendingar eru aðeins sameinaðar innan einnar hleðslu. |
| Veljið handvirkt **Sameina sendingar** á síðunni **Allar sendingar** og veljið síðan mark „grunnsendingar“. Sían leggur til allar fyrirliggjandi sendingar sem eru með samsvarandi gildi fyrir nokkra lykilreiti. | Veljið handvirkt **Sameina sendingar** á síðunni **Allar sendingar** og veljið síðan mark „grunnsendingar“. Kerfið leggur til aðrar fyrirliggjandi sendingar með því að finna samsvarandi gildi nokkurra lykilreita sem eru skilgreindir fyrir viðeigandi samstæðureglur sendingar. |
| Hægt er að nota skipunina **Sameina sendingar** á síðunni **Allar sendingar** fyrir aðeins eina sendingu. | Síðan **Samstæðuvinnusvæði sendinga** hjálpar til við að finna sendingar sem eru ekki enn í sendingu. Þessar sendingar eru greindar út frá nokkrum lykilreitum sem eru skilgreindir í samstæðureglum sendingar. Allar sendingar þar sem gildin fyrir þessa reiti eru samsvarandi eru lagðar til fyrir samstæðu.<p>Hægt er að viðhalda samstæðunni handvirkt með því að fjarlægja sendingar úr tillögum um samstæður og/eða með því að bæta sendingum við þær. Ýmsar gerðir af villum geta komið upp, en hægt er að hnekkja sumum þeirra.</p> |
| **Athugasemd:** Ferlið *Sjálfvirk losun sölupantana til vöruhúss* skiptir sölulínum í hópa. Hver hópur hefur sitt eigið einkvæma **ReleaseToWarehouseId** gildi og er unninn sérstaklega með ferlinu *Losa í vöruhús*. Þetta ferli stofnar nýja vinnu óháð uppsetningu vinnuhlés. | **Athugasemd:** Ferlið *Sjálfvirk losun sölupantana til vöruhúss* úthlutar sama **ReleaseToWarehouseId** gildi á allar sölulínur sem verið er að vinna. Allar sölulínur eru unnar af *Losa í vöruhús* á sama tíma. Til að tryggja fyrri hegðun þarf að skilgreina vinnuhlé fyrir hvert sendingarauðkenni. |

## <a name="additional-resources"></a>Frekari upplýsingar

- [Skilgreina samstæðureglur sendingar](configure-shipment-consolidation-policies.md)
