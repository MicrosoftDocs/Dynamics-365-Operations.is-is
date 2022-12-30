---
title: Kostnaðarfærslueiningar
description: Í þessari grein er að finna upplýsingar um kostnaðarfærslur, sem gera kleift að skipta virði kostnaðar á milli innihalds kostnaðarsvæðis með vali á skiptingaraðferð.
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
ms.openlocfilehash: 0084d47bf85050749b2668d273db07670aaeae2a
ms.sourcegitcommit: 5b34b41ae74269ba639e2876bc5862ef468da1cc
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/15/2022
ms.locfileid: "9166804"
---
# <a name="cost-transaction-entities"></a>Kostnaðarfærslueiningar

[!include [banner](../includes/banner.md)]

## <a name="apportionment"></a>Skipting

Heildarkostnaður gerir kleift að skipta verðmæti kostnaðar á milli innihalds kostnaðarsvæðis (ferð, sendingargeymsla og svo framvegis) með því að velja úthlutunaraðferð. Skiptingaraðferðin er sett upp sem hluti af uppsetningu sjálfvirks kostnaðar sem byggir á viðskiptareglum. Það er dregið í gegn sem hluti af kostnaði þegar ferðalína er búin til.

### <a name="configure-the-apportionment-mapping-for-use-with-data-entities"></a>Stilla skiptingaraðferð til notkunar með gagnaeiningum

Þegar kostnaður er búinn til frá utanaðkomandi uppruna, svo sem flutningamiðlara, getur sá ekki tilgreint hvaða aðferð er valin til að skipta kostnaðarverðinu. Skiptingaraðferðin skilgreinir sjálfgefna skiptingaraðferðaðferð fyrir hverja kostnaðargerðarkóða. Tafla skiptingaraðferðar er aðgengileg á síðunni **Skiptingaraðferð** í Microsoft Dynamics 365 Supply Chain Management (**Heildarkostnaður \> Kostnaðaruppsetning \> Skiptingaraðferð**).

Ef skiptingarsamsetning hefur verið skilgreind og kostnaður sem samsvarar kostnaðartegund er búinn til með því að nota kostnaðarfærslueiningu verður vörpuð skiptingaraðferð notuð í stað hvers gildis sem hefur verið veitt í einingunni.

Ef ekkert gildi er til staðar í vörpunartöflunni, en verðmæti hefur verið gefið upp til einingar, verður uppgefið gildi notað.

Ef ekkert gildi er til í vörpunartöflunni eða færslunni sem hefur verið send til einingar er ekki hægt að búa þetta til.

### <a name="apportionment-mapping-itmapportionmentmapping"></a>Skiptingaraðferð (ITMApportionmentMapping)

Skiptingaraðferðeiningin (`ITMApportionmentMapping`) býr til tenda skiptingaraðferð og gerir notendum kleift að búa til eða uppfæra færslur.

| Nafn | Vörpun | Gagnagerð | Lykill | Skylda |
|---|---|---|---|---|
| Skiptingaraðferð | ITMApportionmentMapping.ApportionmentMethod | Int | Nr. | Nr. |
| Kostnaðargerðarkóði | ITMApportionmentMapping.ShipCostTypeId | Nvarchar(20) | **Já** | Nr. |

## <a name="voyage-costs-itmcosttransvoyageentity"></a>Kostnaður ferðar (ITMCostTransVoyageEntity)

Ferðakostnaðareiningin (`ITMCostTransVoyageEntity`) býr til ferðakostnaðarfærslur sem eru notaðar á ferðastigi. Meðan á innflutningsferlinu stendur notar kerfið **Flokkur** og **Skiptingaraðferð** gildin sem eru innifalin í einingunni til að ákvarða hvernig verðmæti kostnaðarins skiptist á milli innihalds ferðarinnar.

| Nafn | Vörpun | Gagnagerð | Lykill | Skylda |
|---|---|---|---|---|
| Skiptingaraðferð | ITMCostTrans.ApportionmentMethod | Int | Nr. | Nr. |
| Kostnaðarvirði | ITMCostTrans.CostValue | Tölustafir(32; 6) | Nr. | Nr. |
| Gjaldmiðill | ITMCostTrans.CurrencyCode | Nvarchar(3) | Nr. | **Já** |
| Línunúmer | ITMCostTrans.LineNum | Tölustafir(32; 16) | **Já** | Nr. |
| Tengd kostnaðargerð | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | Nr. | Nr. |
| Lágmarkskostnaður | ITMCostTrans.MinCostAmount | Tölustafir(32; 6) | Nr. | Nr. |
| Flokkur | ITMCostTrans.ShipCostCategory | Int | Nr. | Nr. |
| Kostnaðargerðarkóði | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | Nr. | Nr. |
| Fyrirtæki | ITMCostTrans.ShipDataArea | Nvarchar(4) | Nr. | **Já** |
| Ferð | ITMCostTrans.TransRecId | Nvarchar(20) | **Já** | Nr. |
| VSK-flokkur vöru | ITMCostTrans.TaxItemGroup | Nvarchar(10) | Nr. | Nr. |

## <a name="shipping-container-costs-itmcosttransshippingcontainerentity"></a>Kostnaðarfærslur gáms (ITMCostTransShippingContainerEntity)

Kostnaðareining sendingargáms (`ITMCostTransShippingContainerEntity`) býr til sendingargámskostnað sem leggst á sendingargámastigi. Meðan á innflutningsferlinu stendur notar kerfið **Flokkur** og **Skiptingaraðferð** gildin sem eru innifalin í einingunni til að ákvarða hvernig verðmæti kostnaðarins skiptist á milli gámsins.

Reitirnir **Samanlagt**, **Leggur** og **Tengdur leggur** eiga sérstaklega við um færslur þar sem gildið **Kostnaðarsvæði** er *Flutningsgámur*. Því eru þau ekki til staðar í gagnaeiningum fyrir önnur kostnaðarsvæði.

| Nafn | Vörpun | Gagnagerð | Lykill | Skylda |
|---|---|---|---|---|
| Samanlagt | ITMCostTrans.AggregatedCost | Int | Nr. | Nr. |
| Skiptingaraðferð | ITMCostTrans.ApportionmentMethod | Int | Nr. | Nr. |
| Kostnaðarvirði | ITMCostTrans.CostValue | Tölustafir(32; 6) | Nr. | Nr. |
| Gjaldmiðill | ITMCostTrans.CurrencyCode | Nvarchar(3) | Nr. | **Já** |
| Línunúmer | ITMCostTrans.LineNum | Tölustafir(32; 16) | **Já** | Nr. |
| Tengd kostnaðargerð | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | Nr. | Nr. |
| Tengdur leggur | ITMCostTrans.LinkLegId | Nvarchar(20) | Nr. | Nr. |
| Lágmarkskostnaður | ITMCostTrans.MinCostAmount | Tölustafir(32; 6) | Nr. | Nr. |
| Gámur | ITMCostTrans.TransRecId | Nvarchar(20) | **Já** | Nr. |
| Flokkur | ITMCostTrans.ShipCostCategory | Int | Nr. | Nr. |
| Kostnaðargerðarkóði | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | Nr. | Nr. |
| Fyrirtæki | ITMCostTrans.ShipDataArea | Nvarchar(4) | Nr. | **Já** |
| Ferð | ITMCostTrans.TransRecId | Nvarchar(20) | **Já** | Nr. |
| Leggur | ITMCostTrans.ShipLegId | Nvarchar(20) | Nr. | Nr. |
| VSK-flokkur vöru | ITMCostTrans.TaxItemGroup | Nvarchar(10) | Nr. | Nr. |

## <a name="folio-costs-itmcosttransfolioentity"></a>Kostnaður fólíó (ITMCostTransFolioEntity)

Eining fyrir kostnað fólíó (`ITMCostTransFolioEntity`) býr til kostnaðarfærsluskrár sem eiga við um fólíóstigið. Meðan á innflutningsferlinu stendur notar kerfið **Flokkur** og **Skiptingaraðferð** gildin sem eru innifalin í einingunni til að ákvarða hvernig verðmæti kostnaðarins skiptist á milli hvers fólíó.

| Nafn | Vörpun | Gagnagerð | Lykill | Skylda |
|---|---|---|---|---|
| Skiptingaraðferð | ITMCostTrans.ApportionmentMethod | Int | Nr. | Nr. |
| Kostnaðarvirði | ITMCostTrans.CostValue | Tölustafir(32; 6) | Nr. | Nr. |
| Gjaldmiðill | ITMCostTrans.CurrencyCode | Nvarchar(3) | Nr. | **Já** |
| Línunúmer | ITMCostTrans.LineNum | Tölustafir(32; 16) | **Já** | Nr. |
| Tengd kostnaðargerð | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | Nr. | Nr. |
| Lágmarkskostnaður | ITMCostTrans.MinCostAmount | Tölustafir(32; 6) | Nr. | Nr. |
| Flokkur | ITMCostTrans.ShipCostCategory | Int | Nr. | Nr. |
| Kostnaðargerðarkóði | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | Nr. | Nr. |
| Fyrirtæki | ITMCostTrans.ShipDataArea | Nvarchar(4) | Nr. | **Já** |
| Fólíó | ITMCostTrans.TransRecId | Nvarchar(20) | **Já** | Nr. |
| VSK-flokkur vöru | ITMCostTrans.TaxItemGroup | Nvarchar(10) | Nr. | Nr. |

## <a name="purchase-order-costs-itmcosttranspurchaseentity"></a>Kostnaður innkaupapöntunar (ITMCostTransPurchaseEntity)

Eining kostnaðar einnkaupapöntunar (`ITMCostTransPurchaseEntity`) býr til kostnaðarfærslur sem eiga við um haus innkaupapöntunar. Meðan á innflutningsferlinu stendur notar kerfið **Flokkur** og **Skiptingaraðferð** gildin sem eru innifalin í einingunni til að ákvarða hvernig verðmæti kostnaðarins skiptist á milli hvers fólíó.

| Nafn | Vörpun | Gagnagerð | Lykill | Skylda |
|---|---|---|---|---|
| Skiptingaraðferð | ITMCostTrans.ApportionmentMethod | Int | Nr. | Nr. |
| Kostnaðarvirði | ITMCostTrans.CostValue | Tölustafir(32; 6) | Nr. | Nr. |
| Gjaldmiðill | ITMCostTrans.CurrencyCode | Nvarchar(3) | Nr. | **Já** |
| Línunúmer | ITMCostTrans.LineNum | Tölustafir(32; 16) | **Já** | Nr. |
| Tengd kostnaðargerð | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | Nr. | Nr. |
| Lágmarkskostnaður | ITMCostTrans.MinCostAmount | Tölustafir(32; 6) | Nr. | Nr. |
| Innkaupapöntun | ITMCostTrans.TransRecId | Nvarchar(20) | **Já** | Nr. |
| Flokkur | ITMCostTrans.ShipCostCategory | Int | Nr. | Nr. |
| Kostnaðargerðarkóði | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | Nr. | Nr. |
| Fyrirtæki | ITMCostTrans.ShipDataArea | Nvarchar(4) | Nr. | **Já** |
| VSK-flokkur vöru | ITMCostTrans.TaxItemGroup | Nvarchar(10) | Nr. | Nr. |

## <a name="item-costs-itmcosttransitementity"></a>Vörukostnaður (ITMCostTransItemEntity)

Kostnaðareining vöru (`ITMCostTransItemEntity`) býr til kostnaðarfærslur sem eiga við um vörustig. Þessi eining á við um vörur á innkaupapöntunarlínum. Virði kostnaðarins leggst að fullu á línuna.

**Leiðréttingarupphæð** og **Leiðrétting virðis** eru sérgreindir fyrir kostnaðarsvæði á línustigi. Því eru þau ekki til staðar í gagnaeiningum fyrir önnur kostnaðarsvæði.

| Nafn | Vörpun | Gagnagerð | Lykill | Skylda |
|---|---|---|---|---|
| Leiðréttingarupphæð | ITMCostTrans.AdjustmentAmount | Tölustafir(32; 6) | Nr. | Nr. |
| Kostnaðarvirði | ITMCostTrans.CostValue | Tölustafir(32; 6) | Nr. | Nr. |
| Gjaldmiðill | ITMCostTrans.CurrencyCode | Nvarchar(3) | Nr. | **Já** |
| Línunúmer | ITMCostTrans.LineNum | Tölustafir(32; 16) | **Já** | Nr. |
| Tengd kostnaðargerð | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | Nr. | Nr. |
| Lágmarkskostnaður | ITMCostTrans.MinCostAmount | Tölustafir(32; 6) | Nr. | Nr. |
| Innkaupapöntun | ITMCostTrans.TransRecId | Nvarchar(20) | **Já** | Nr. |
| Númer innkaupapöntunarlínu | ITMCostTrans.TransRecId | Nvarchar(20) | **Já** | Nr. |
| Flokkur | ITMCostTrans.ShipCostCategory | Int | Nr. | Nr. |
| Kostnaðargerðarkóði | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | Nr. | Nr. |
| Fyrirtæki | ITMCostTrans.ShipDataArea | Nvarchar(4) | Nr. | **Já** |
| VSK-flokkur vöru | ITMCostTrans.TaxItemGroup | Nvarchar(10) | Nr. | Nr. |
| Leiðrétting virðis | ITMCostTrans.ValueAdjustmentMethod | Int | Nr. | Nr. |

## <a name="transfer-line-costs-itmcosttranstransferlineentity"></a>Kostnaðarfærslur flutningslínu (ITMCostTransTransferLineEntity)

Eining flutningskostnaðarlínu (`ITMCostTransTransferLineEntity`) býr til kostnaðarfærslur sem gilda um flutningspöntunarlínustigið. Virði þessa kostnaðar leggst að fullu á flutningspöntunarlínuna.

**Leiðréttingarupphæð** og **Leiðrétting virðis** eru sérgreindir fyrir kostnaðarsvæði á línustigi. Því eru þau ekki til staðar í gagnaeiningum fyrir önnur kostnaðarsvæði.

| Nafn | Vörpun | Gagnagerð | Lykill | Skylda |
|---|---|---|---|---|
| Leiðréttingarupphæð | ITMCostTrans.AdjustmentAmount | Tölustafir(32; 6) | Nr. | Nr. |
| Kostnaðarvirði | ITMCostTrans.CostValue | Tölustafir(32; 6) | Nr. | Nr. |
| Gjaldmiðill | ITMCostTrans.CurrencyCode | Nvarchar(3) | Nr. | **Já** |
| Línunúmer | ITMCostTrans.LineNum | Tölustafir(32; 16) | **Já** | Nr. |
| Tengd kostnaðargerð | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | Nr. | Nr. |
| Lágmarkskostnaður | ITMCostTrans.MinCostAmount | Tölustafir(32; 6) | Nr. | Nr. |
| Flokkur | ITMCostTrans.ShipCostCategory | Int | Nr. | Nr. |
| Kostnaðargerðarkóði | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | Nr. | Nr. |
| Fyrirtæki | ITMCostTrans.ShipDataArea | Nvarchar(4) | Nr. | **Já** |
| Flutningspöntun | ITMCostTrans.TransRecId | Nvarchar(20) | **Já** | Nr. |
| Númer flutningspöntunarlínu | ITMCostTrans.TransRecId | Nvarchar(20) | **Já** | Nr. |
| VSK-flokkur vöru | ITMCostTrans.TaxItemGroup | Nvarchar(10) | Nr. | Nr. |
| Leiðrétting virðis | ITMCostTrans.ValueAdjustmentMethod | Int | Nr. | Nr. |

### <a name="transaction-table"></a>Færslutafla

Kostnaðarfærsluskrá er tengd við kostnaðarsvæði með úthlutun á færslutöflunúmeri (`TransTableId`). Þegar krafist er sérstakra auðkennisnúmera fyrir töflu er einingu skipt á grundvelli þessara gilda, þannig að til sé eining fyrir hvert kostnaðarsvæði.

Gildið fyrir færslutöfluna (`TransTableId`) er undirliggjandi í vali á einingu kostnaðarfærslu.

### <a name="calculated-fields"></a>Reiknuð svæði

Eftirfarandi reitir eru ekki tiltækir fyrir innsetningu eða uppfærslu þegar kostnaðarliðir eru notaðir, vegna þess að þessir reitir eru aðeins stilltir þegar gripið er til sérstakra aðgerða gegn ferðafærslunni:

- **Áætlaður kostnaður** – Þessi reitur er stilltur þegar reikningur er birtur fyrir ferðina (innkaupapöntun) eða millifærsla er móttekin.
- **Gjaldmiðill áætlaðs kostnaðar** – Þessi reitur er stilltur þegar reikningur er birtur fyrir ferðina (innkaupapöntun) eða flutningur er móttekinn.
- **Raunkostnaður** – Þessi reitur er stilltur þegar sölureikningur er bókaður. Þetta tengist kostnaðinum.

### <a name="find-auto-costs"></a>Leita að sjálfvirkum kostnaði

**Leita að sjálfvirkum kostnaði** hnappurinn er tiltækur fyrir hvert kostnaðarsvæði (ferð, sendingargeymir og svo framvegis) til að uppfæra kostnaðarfærslur fyrir það kostnaðarsvæði frá upplýsingunum í stillitöflunum. Þegar þú velur hnappinn fyrir kostnaðarsvæði hreinsar kerfið núverandi kostnað fyrir það kostnaðarsvæði og býr til nýjar skrár, byggt á núverandi uppsetningu á sjálfvirkum kostnaðarborðum.

Færsluskrár vegna kostnaðar sem stofnað er til með því að nota gagnaeiningu eru flaggaðar sem fluttar inn. Þessum skrám er ekki eytt þegar þú velur **Finna sjálfvirkan kostnað** vegna þess að þær verða ekki endurskapaðar úr uppsetningartöflum fyrir sjálfvirkan kostnað. Hins vegar er enn hægt að eyða kostnaðarfærsluskrá sem er flaggað sem innflutt.

### <a name="linked-fields"></a>Tengdir reitir

Hægt er að tengja hverja kostnaðarfærslu við aðra færslu á sama kostnaðarsvæði. Þessi tengsl eru stofnuð í gegnum reitinn **Tengd kostnaðargerð**. Þetta gerir kleift að reikna út kostnaðarvirði sem prósentu af öðrum kostnaði.

Reitinn **Tengd kostnaðargerð** er aðeins hægt að staðfesta ef fyrst er unnið úr færslunni sem vísað er í, eða ef hún er þegar til í töflunni. Sama krafa á við um **Tengda legginn** sem er eingöngu notaður fyrir kostnaðarsvæði sendingargeymis.
