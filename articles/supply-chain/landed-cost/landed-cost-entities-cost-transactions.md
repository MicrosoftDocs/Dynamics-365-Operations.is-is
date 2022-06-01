---
title: Kostnaðarviðskiptaeiningar
description: Þetta efnisatriði veitir upplýsingar um kostnaðarfærslueiningar, sem gera kleift að skipta verðmæti kostnaðar á innihald kostnaðarsvæðis með vali á úthlutunaraðferð.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 41a9525cb766907b7de97f1e856a3b640d7718ac
ms.sourcegitcommit: 611202adaa080250636efabb3b3b32b850d92d04
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/28/2022
ms.locfileid: "8813165"
---
# <a name="cost-transaction-entities"></a>Kostnaðarviðskiptaeiningar

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until GA with 10.0.28 -->

## <a name="apportionment"></a>Skipting

Landaður kostnaður gerir kleift að skipta verðmæti kostnaðar á innihald kostnaðarsvæðis (siglingar, flutningsgámur og svo framvegis) með því að velja úthlutunaraðferð. Úthlutunaraðferðin er stillt sem hluti af uppsetningu sjálfvirks kostnaðar sem byggir á viðskiptareglum. Það er dreginn í gegn sem hluti af kostnaði þegar ferðalína er búin til.

### <a name="configure-the-apportionment-mapping-for-use-with-data-entities"></a>Stilltu úthlutunarvörpunina til notkunar með gagnaeiningum

Þegar kostnaður er búinn til úr utanaðkomandi uppsprettu eins og flutningsmiðlara, getur þessi ytri uppspretta ekki tilgreint ákjósanlega aðferð til að skipta kostnaðarverðmæti. Úthlutunarvörpunin skilgreinir sjálfgefna skiptingaraðferð fyrir hvern kostnaðartegundarkóða. Hægt er að nálgast úthlutunarkortatöfluna frá **Úthlutunarkortlagning** síðu í Microsoft Dynamics 365 Supply Chain Management (**Landaður kostnaður \> Kostnaðaruppsetning \> Úthlutunarkortlagning**).

Ef vörpunarsamsetning hefur verið skilgreind og kostnaður sem passar við kostnaðartegundarkóðann er búinn til með því að nota kostnaðarfærslueiningu, verður kortlagða skiptingaraðferðin notuð í stað hvers konar gildis sem hefur verið veitt einingunni.

Ef ekkert gildi er til staðar í kortlagningartöflunni, en gildi hefur verið veitt til einingarinnar, verður uppgefið gildi notað.

Ef ekkert gildi er til í hvorki vörpunartöflunni né færslunni sem hefur verið send til einingarinnar mun sköpun mistakast.

### <a name="apportionment-mapping-itmapportionmentmapping"></a>Úthlutunarkortlagning (ITMApportionmentMapping)

Úthlutunarkortunareiningin (`ITMApportionmentMapping`) býr til tengslakortunarsambönd og gerir notendum kleift að búa til eða uppfæra færslur.

| Nafn | Vörpun | Gagnagerð | Lykill | Skylda |
|---|---|---|---|---|
| Skiptingaraðferð | ITMApportionmentMapping.ApportionmentMethod | Int | Nr. | Nr. |
| Kostnaðargerðarkóði | ITMApportionmentMapping.ShipCostTypeId | Nvarchar (20) | **Já** | Nr. |

## <a name="voyage-costs-itmcosttransvoyageentity"></a>Ferðakostnaður (ITMCostTransVoyageEntity)

Ferðakostnaður eining (`ITMCostTransVoyageEntity`) býr til ferðakostnaðarfærslur sem eru notaðar á ferðastigi. Í innflutningsferlinu notar kerfið **Flokkur** og **Úthlutunaraðferð** gildi sem eru innifalin í einingunni til að ákvarða hvernig verðmæti kostnaðar er skipt yfir innihald ferðarinnar.

| Nafn | Vörpun | Gagnagerð | Lykill | Skylda |
|---|---|---|---|---|
| Skiptingaraðferð | ITMCostTrans.ApportionmentMethod | Int | Nr. | Nr. |
| Kostnaðarvirði | ITMCostTrans.CostValue | Númeric(32, 6) | Nr. | Nr. |
| Gjaldmiðill | ITMCostTrans.CurrencyCode | Nvarchar(3) | Nr. | **Já** |
| Línunúmer | ITMCostTrans.LineNum | Númeric(32, 16) | **Já** | Nr. |
| Tengd kostnaðargerð | ITMCostTrans.LinkCostTypeId | Nvarchar (20) | Nr. | Nr. |
| Lágmarkskostnaður | ITMCostTrans.MinCostAmount | Númeric(32, 6) | Nr. | Nr. |
| Flokkur | ITMCostTrans.ShipCostCategory | Int | Nr. | Nr. |
| Kostnaðargerðarkóði | ITMCostTrans.ShipCostTypeId | Nvarchar (20) | Nr. | Nr. |
| Fyrirtæki | ITMCostTrans.ShipDataArea | Nvarchar(4) | Nr. | **Já** |
| Ferð | ITMCostTrans.TransRecId | Nvarchar (20) | **Já** | Nr. |
| VSK-flokkur vöru | ITMCostTrans.TaxItemGroup | Nvarchar(10) | Nr. | Nr. |

## <a name="shipping-container-costs-itmcosttransshippingcontainerentity"></a>Sendingargámakostnaður (ITMCostTransShippingContainerEntity)

Sendingargámakostnaður eining (`ITMCostTransShippingContainerEntity`) býr til flutningsgámakostnað sem er notaður á flutningsgámastigi. Í innflutningsferlinu notar kerfið **Flokkur** og **Úthlutunaraðferð** gildi sem eru innifalin í einingunni til að ákvarða hvernig verðmæti kostnaðar er skipt yfir innihald flutningsgámsins.

The **Samanlagt**, **·**, og **Tengdur fótur** reitir eru sérstakir fyrir færslur þar sem **Kostnaðarsvæði** gildi er *Sendingargámur*. Þess vegna eru þau ekki til staðar í gagnaeiningum fyrir önnur kostnaðarsvæði.

| Nafn | Vörpun | Gagnagerð | Lykill | Skylda |
|---|---|---|---|---|
| Samanlagt | ITMCostTrans.AggregatedCost | Int | Nr. | Nr. |
| Skiptingaraðferð | ITMCostTrans.ApportionmentMethod | Int | Nr. | Nr. |
| Kostnaðarvirði | ITMCostTrans.CostValue | Númeric(32, 6) | Nr. | Nr. |
| Gjaldmiðill | ITMCostTrans.CurrencyCode | Nvarchar(3) | Nr. | **Já** |
| Línunúmer | ITMCostTrans.LineNum | Númeric(32, 16) | **Já** | Nr. |
| Tengd kostnaðargerð | ITMCostTrans.LinkCostTypeId | Nvarchar (20) | Nr. | Nr. |
| Tengdur leggur | ITMCostTrans.LinkLegId | Nvarchar (20) | Nr. | Nr. |
| Lágmarkskostnaður | ITMCostTrans.MinCostAmount | Númeric(32, 6) | Nr. | Nr. |
| Sendingargámur | ITMCostTrans.TransRecId | Nvarchar (20) | **Já** | Nr. |
| Flokkur | ITMCostTrans.ShipCostCategory | Int | Nr. | Nr. |
| Kostnaðargerðarkóði | ITMCostTrans.ShipCostTypeId | Nvarchar (20) | Nr. | Nr. |
| Fyrirtæki | ITMCostTrans.ShipDataArea | Nvarchar(4) | Nr. | **Já** |
| Ferð | ITMCostTrans.TransRecId | Nvarchar (20) | **Já** | Nr. |
| Leggur | ITMCostTrans.ShipLegId | Nvarchar (20) | Nr. | Nr. |
| VSK-flokkur vöru | ITMCostTrans.TaxItemGroup | Nvarchar(10) | Nr. | Nr. |

## <a name="folio-costs-itmcosttransfolioentity"></a>Folio kostnaður (ITMCostTransFolioEntity)

Folio kostnaðareiningin (`ITMCostTransFolioEntity`) býr til kostnaðarfærslur sem eiga við folio-stigið. Í innflutningsferlinu notar kerfið **Flokkur** og **Úthlutunaraðferð** gildi sem eru innifalin í einingunni til að ákvarða hvernig verðmæti kostnaðar er skipt yfir innihald hverrar blaðsíðu.

| Nafn | Vörpun | Gagnagerð | Lykill | Skylda |
|---|---|---|---|---|
| Skiptingaraðferð | ITMCostTrans.ApportionmentMethod | Int | Nr. | Nr. |
| Kostnaðarvirði | ITMCostTrans.CostValue | Númeric(32, 6) | Nr. | Nr. |
| Gjaldmiðill | ITMCostTrans.CurrencyCode | Nvarchar(3) | Nr. | **Já** |
| Línunúmer | ITMCostTrans.LineNum | Númeric(32, 16) | **Já** | Nr. |
| Tengd kostnaðargerð | ITMCostTrans.LinkCostTypeId | Nvarchar (20) | Nr. | Nr. |
| Lágmarkskostnaður | ITMCostTrans.MinCostAmount | Númeric(32, 6) | Nr. | Nr. |
| Flokkur | ITMCostTrans.ShipCostCategory | Int | Nr. | Nr. |
| Kostnaðargerðarkóði | ITMCostTrans.ShipCostTypeId | Nvarchar (20) | Nr. | Nr. |
| Fyrirtæki | ITMCostTrans.ShipDataArea | Nvarchar(4) | Nr. | **Já** |
| Fólíó | ITMCostTrans.TransRecId | Nvarchar (20) | **Já** | Nr. |
| VSK-flokkur vöru | ITMCostTrans.TaxItemGroup | Nvarchar(10) | Nr. | Nr. |

## <a name="purchase-order-costs-itmcosttranspurchaseentity"></a>Innkaupapöntunarkostnaður (ITMCostTransPurchaseEntity)

Kostnaðareining innkaupapöntunar (`ITMCostTransPurchaseEntity`) býr til kostnaðarfærslur sem eiga við haus innkaupapöntunar. Í innflutningsferlinu notar kerfið **Flokkur** og **Úthlutunaraðferð** gildi sem eru innifalin í einingunni til að ákvarða hvernig verðmæti kostnaðar er skipt yfir innihald hverrar blaðsíðu.

| Nafn | Vörpun | Gagnagerð | Lykill | Skylda |
|---|---|---|---|---|
| Skiptingaraðferð | ITMCostTrans.ApportionmentMethod | Int | Nr. | Nr. |
| Kostnaðarvirði | ITMCostTrans.CostValue | Númeric(32, 6) | Nr. | Nr. |
| Gjaldmiðill | ITMCostTrans.CurrencyCode | Nvarchar(3) | Nr. | **Já** |
| Línunúmer | ITMCostTrans.LineNum | Númeric(32, 16) | **Já** | Nr. |
| Tengd kostnaðargerð | ITMCostTrans.LinkCostTypeId | Nvarchar (20) | Nr. | Nr. |
| Lágmarkskostnaður | ITMCostTrans.MinCostAmount | Númeric(32, 6) | Nr. | Nr. |
| Innkaupapöntun | ITMCostTrans.TransRecId | Nvarchar (20) | **Já** | Nr. |
| Flokkur | ITMCostTrans.ShipCostCategory | Int | Nr. | Nr. |
| Kostnaðargerðarkóði | ITMCostTrans.ShipCostTypeId | Nvarchar (20) | Nr. | Nr. |
| Fyrirtæki | ITMCostTrans.ShipDataArea | Nvarchar(4) | Nr. | **Já** |
| VSK-flokkur vöru | ITMCostTrans.TaxItemGroup | Nvarchar(10) | Nr. | Nr. |

## <a name="item-costs-itmcosttransitementity"></a>Vörukostnaður (ITMCostTransItemEntity)

Kostnaðareiningin (`ITMCostTransItemEntity`) stofnar kostnaðarfærslur sem eiga við vörustigið. Þessi eining er sértæk fyrir vörur á innkaupapöntunarlínum. Verðmæti kostnaðar er lagt að fullu á línuna.

The **Leiðréttingarupphæð** og **Verðmætisleiðrétting** reitir eru sérstakir fyrir kostnaðarsvæðin á línustigi. Þess vegna eru þau ekki til staðar í gagnaeiningum fyrir önnur kostnaðarsvæði.

| Nafn | Vörpun | Gagnagerð | Lykill | Skylda |
|---|---|---|---|---|
| Leiðréttingarupphæð | ITMCostTrans.AdjustmentAmount | Númeric(32, 6) | Nr. | Nr. |
| Kostnaðarvirði | ITMCostTrans.CostValue | Númeric(32, 6) | Nr. | Nr. |
| Gjaldmiðill | ITMCostTrans.CurrencyCode | Nvarchar(3) | Nr. | **Já** |
| Línunúmer | ITMCostTrans.LineNum | Númeric(32, 16) | **Já** | Nr. |
| Tengd kostnaðargerð | ITMCostTrans.LinkCostTypeId | Nvarchar (20) | Nr. | Nr. |
| Lágmarkskostnaður | ITMCostTrans.MinCostAmount | Númeric(32, 6) | Nr. | Nr. |
| Innkaupapöntun | ITMCostTrans.TransRecId | Nvarchar (20) | **Já** | Nr. |
| Númer innkaupapöntunarlínu | ITMCostTrans.TransRecId | Nvarchar (20) | **Já** | Nr. |
| Flokkur | ITMCostTrans.ShipCostCategory | Int | Nr. | Nr. |
| Kostnaðargerðarkóði | ITMCostTrans.ShipCostTypeId | Nvarchar (20) | Nr. | Nr. |
| Fyrirtæki | ITMCostTrans.ShipDataArea | Nvarchar(4) | Nr. | **Já** |
| VSK-flokkur vöru | ITMCostTrans.TaxItemGroup | Nvarchar(10) | Nr. | Nr. |
| Leiðrétting virðis | ITMCostTrans.ValueAdjustmentMethod | Int | Nr. | Nr. |

## <a name="transfer-line-costs-itmcosttranstransferlineentity"></a>Flutningslínukostnaður (ITMCostTransTransferLineEntity)

Flutningslínukostnaðareiningin (`ITMCostTransTransferLineEntity`) býr til kostnaðarfærslur sem eiga við línustig millifærslupöntunar. Verðmæti þessa kostnaðar er sett að fullu á millifærslupöntunarlínuna.

The **Leiðréttingarupphæð** og **Verðmætisleiðrétting** reitir eru sérstakir fyrir kostnaðarsvæðin á línustigi. Þess vegna eru þau ekki til staðar í gagnaeiningum fyrir önnur kostnaðarsvæði.

| Nafn | Vörpun | Gagnagerð | Lykill | Skylda |
|---|---|---|---|---|
| Leiðréttingarupphæð | ITMCostTrans.AdjustmentAmount | Númeric(32, 6) | Nr. | Nr. |
| Kostnaðarvirði | ITMCostTrans.CostValue | Númeric(32, 6) | Nr. | Nr. |
| Gjaldmiðill | ITMCostTrans.CurrencyCode | Nvarchar(3) | Nr. | **Já** |
| Línunúmer | ITMCostTrans.LineNum | Númeric(32, 16) | **Já** | Nr. |
| Tengd kostnaðargerð | ITMCostTrans.LinkCostTypeId | Nvarchar (20) | Nr. | Nr. |
| Lágmarkskostnaður | ITMCostTrans.MinCostAmount | Númeric(32, 6) | Nr. | Nr. |
| Flokkur | ITMCostTrans.ShipCostCategory | Int | Nr. | Nr. |
| Kostnaðargerðarkóði | ITMCostTrans.ShipCostTypeId | Nvarchar (20) | Nr. | Nr. |
| Fyrirtæki | ITMCostTrans.ShipDataArea | Nvarchar(4) | Nr. | **Já** |
| Flutningspöntun | ITMCostTrans.TransRecId | Nvarchar (20) | **Já** | Nr. |
| Flytja pöntunarlínunúmer | ITMCostTrans.TransRecId | Nvarchar (20) | **Já** | Nr. |
| VSK-flokkur vöru | ITMCostTrans.TaxItemGroup | Nvarchar(10) | Nr. | Nr. |
| Leiðrétting virðis | ITMCostTrans.ValueAdjustmentMethod | Int | Nr. | Nr. |

### <a name="transaction-table"></a>Færslutafla

Kostnaðarfærsluskrá er tengd við kostnaðarsvæði með úthlutun á færslutöflunúmeri (`TransTableId`). Þegar þörf er á sérstökum töfluauðkennisnúmerum er einingunum skipt út frá þessum gildum, þannig að eining er til fyrir hvert kostnaðarsvæði.

Gildi fyrir færslutöfluna (`TransTableId`) er óbeint við val á kostnaðarfærslueiningunni.

### <a name="calculated-fields"></a>Reiknuð svæði

Eftirfarandi reitir eru ekki tiltækir fyrir innsetningu eða uppfærslu þegar kostnaðarfærslueining er notuð, vegna þess að þessir reitir eru aðeins stilltir þegar tilteknar aðgerðir eru gerðar gegn ferðaskránni:

- **Áætlaður kostnaður** – Þessi reitur er stilltur þegar reikningur er bókaður fyrir ferðina (innkaupapöntun) eða millifærsla er móttekin.
- **Áætlaður kostnaðargjaldmiðill** – Þessi reitur er stilltur þegar reikningur er bókaður fyrir ferðina (innkaupapöntun) eða millifærsla er móttekin.
- **Raunverulegur kostnaður** – Þessi reitur er stilltur þegar reikningur lánardrottins er bókaður. Það tengist kostnaðinum.

### <a name="find-auto-costs"></a>Leita að sjálfvirkum kostnaði

A **Finndu bílakostnað** hnappur sem er tiltækur fyrir hvert kostnaðarsvæði (sigling, sendingargámur og svo framvegis) veitir leið til að uppfæra kostnaðarfærslur fyrir það kostnaðarsvæði út frá upplýsingum í stillingatöflunum. Þegar þú velur hnappinn fyrir kostnaðarsvæði, hreinsar kerfið núverandi kostnað fyrir það kostnaðarsvæði og býr til nýjar færslur, byggðar á núverandi uppsetningu sjálfvirkrar kostnaðaruppsetningartöflur.

Kostnaðarfærslur sem eru búnar til með því að nota gagnaeiningu eru merktar sem innfluttar. Þessum skrám er ekki eytt þegar þú velur **Finndu bílakostnað**, vegna þess að þær verða ekki endurbúnar úr sjálfvirku kostnaðaruppsetningartöflunum. Hins vegar er enn hægt að eyða kostnaðarfærsluskrá sem er merkt innflutt.

### <a name="linked-fields"></a>Tengdir reitir

Hægt er að tengja hverja kostnaðarfærslu við aðra færslu á sama kostnaðarsvæði. Þetta félag er stofnað í gegnum **Tengd kostnaðartegund** sviði. Það gerir kleift að reikna kostnaðargildi sem hlutfall af öðrum kostnaði.

The **Tengd kostnaðartegund** Aðeins er hægt að staðfesta reitinn ef færsluna sem vísað er til er unnin fyrst eða ef hún er þegar til í töflunni. Sama krafa á við um **Tengdur fótur** reit sem er eingöngu notaður fyrir kostnað á kostnaðarsvæði sendingargáma.
