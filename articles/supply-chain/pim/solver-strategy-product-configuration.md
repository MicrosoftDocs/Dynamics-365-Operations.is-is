---
title: Leysisstefna fyrir afurðarafbrigði
description: Þetta efnisatriði lýsir því hvernig hægt er að nota leysisstefnu til að bæta árangur afurðarafbrigðis.
author: cvocph
ms.date: 02/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PCCreateProductConfigurationModel, PCProductConfigurationModelListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 38755cc224ee2ae642d3caf7ad8ffea61f987206efc3ecd2ef81ecaf21cd6f4e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6765979"
---
# <a name="solver-strategy-for-product-configuration"></a>Leysisstefna fyrir afurðarafbrigði

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir því hvernig hægt er að nota leysisstefnu til að bæta árangur afurðarafbrigðis.

Hugmyndin um leysisstefnu var fyrst kynnt í heildaruppfærslu 7 (CU7) for Microsoft Dynamics AX 2012 R2. Hún var útvíkkuð í heildaruppfærslu 8 (CU8) fyrir Microsoft Dynamics AX 2012 R3 og Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.

Hugmyndin um leysisstefnuna samanstendur nú af eftirfarandium lausnarmenn samanstendur nú af eftirfarandi aðferðum:

- Sjálfgefið
- Lágmarkslén fyrst
- Ofan og niður
- Z3

## <a name="solver-strategy"></a>Leysisstefna 

Afrbrigðalíkan afurðar er hægt að móta sem [vandamál uppfylltra skilyrða (CSP)](http://aima.cs.berkeley.edu/2nd-ed/newchap05.pdf). Microsoft Solver Foundation (MSF) býður upp á tvær tegundir af leysisstefnum til að leysa CSP sem hægt er að nota úr afbrigðalíkönum afurðar. Þessar leysisstefnur reiða sig á [leiðsagnarreglur](https://techterms.com/definition/heuristic) sem eru notaðar til að ákvarða röðina sem breytur CSP eru taldar vera á meðan verið er að leysa úr vandamálinu. Leiðsagnarreglur geta haft veruleg áhrif á afköst á meðan verið er að leysa úr vandamálinu eða flokki vandamála.

Leysisstefnan fyrir afbrigðalíkan afurðar ákvarðar hvaða sem skilgreinir hvaða lausn er notuð með leiðsagnarreglum. Aðferðirnar **Sjálfgefið**, **Lágmarkslén fyrst** og **Ofan og niður** nota tvær lausnir fyrir MSF, á meðan **Z3** aðferðin notar Z3 lausn. 

Framkvæmdarrannsóknir á raunverulegum viðskiptavini hafa sýnt að breyting á leysisstefnunni fyrir afbrigðalíkan afurðar getur dregið úr svartíma frá mínútum til millisekúndna. Þess vegna er það þess virði að reyna að mismunandi leysisstefnur til að finna skilvirkustu stefnuna fyrir afbrigðalíkan afurðar.

## <a name="change-the-settings-for-the-solver-strategy"></a>Breyta stillingum fyrir leysisstefnuna

Til að breyta leysisstefnunni, á síðunni **Afbrigðalíkan afurðar**, í aðgerðarglugganum, velurðu **Eiginleikar líkana**. Síðan skaltu velja leysisstefnuna í svarglugganum **Breyta upplýsingum líkans**.

[![Breyta leysisstefnunni.](./media/solver-strategy.png)](./media/solver-strategy.png)

Eins og er, er ekkert sem sjálfkrafa greinir hvaða leysisstefna muni vera skilvirkasta stefnan fyrir afbrigðalíkan afurða sem er háð skilyrðum. Þess vegna verður þú að prófa hverja leysisstefnu fyrir sig.

Í eftirfarandi töflu eru ráðleggingar um leysisstefnur til að nota við ýmsar aðstæður.

| Leysisstefna      | Notaðu stefnuna við þessar aðstæður |
|----------------------|-----------------------------------|
| Sjálfgefið              | **Sjálfgefna** stefnan hefur verið fínstillt til að leysa líkön sem treysta á töfluskorðanir. Framkvæmdarrannsóknir viðskiptavinar hafa sýnt að þessi stefna sé skilvirkasta stefnan í aðstæðum þar sem töfluskorður eru mikið notaðar. |
| Lágmarkslén fyrst | **Lágmarkslén fyrst** og **Ofan og niður** stefnurnar eru nátengdar. Framkvæmdarrannsóknir viðskiptavina hafa sýnt að stefnan **Ofan og niður** er betri en stefnan **Lágmarkslén fyrst**. Hins vegar er stefnan **Lágmarkslén fyrst** haldið í vörunni fyrir afturvirka samhæfni. Báðar þessar leysisstefnur hafa sýnt fram á meiri skilvirkni við að leysa líkön sem innihalda nokkrar reikningssegðir þar sem engar töfluskorður eru notaðar. Hins vegar er stefnan **Sjálfgefið** í sumum tilfellum betri en þessar tvær stefnur. Mundu því að prófa hverja stefnu fyrir sig. |
| Ofansækið             | **Lágmarkslén fyrst** og **Ofan og niður** stefnurnar eru nátengdar. Framkvæmdarrannsóknir viðskiptavina hafa sýnt að stefnan **Ofan og niður** er betri en stefnan **Lágmarkslén fyrst**. Hins vegar er stefnan **Lágmarkslén fyrst** haldið í vörunni fyrir afturvirka samhæfni. Báðar þessar leysisstefnur hafa sýnt fram á meiri skilvirkni við að leysa líkön sem innihalda nokkrar reikningssegðir þar sem engar töfluskorður eru notaðar. Hins vegar er stefnan **Sjálfgefið** í sumum tilfellum betri en þessar tvær stefnur. Mundu því að prófa hverja stefnu fyrir sig. |
| Z3                   | Við mælum með því að þú notir stefenuna **Z3** sem sjálfgefna leysisstefnu. Ef þú hefur áhyggjur af afköstum og sveigjanleika getur þú metið hinar stefnurnar. |

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit afurðarafbrigða](build-product-configuration-model.md)

[Leiðsagnarreglur](https://techterms.com/definition/heuristic)

[Vandamál uppfylltra skilyrði](http://aima.cs.berkeley.edu/2nd-ed/newchap05.pdf)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]