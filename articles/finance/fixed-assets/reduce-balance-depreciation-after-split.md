---
title: Afskrift lækkandi stöðu eftir skipti
description: Þetta efnisatriði lýsir aðferðinni sem er notuð í eignum til að reikna afskriftir eftir skiptingu eignar með því að minnka bókfært virði.
author: moaamer
manager: Ann Beebe
ms.date: 11/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-11-17
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ea89d54b9b8287d9c81b75a99c5808b5deb05cef
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976092"
---
# <a name="reduce-balance-depreciation-after-a-split"></a>Afskrift lækkandi stöðu eftir skipti

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir aðferðinni sem er notuð í eignum til að reikna afskriftir eftir skiptingu eignar í aðra eign með því að minnka bókfært virði. Afskriftarárið sem er skilgreint í eignabók er fjárhagsárið. Frekari upplýsingar er að finna í [Minnka bókfært virði](reduce-balance-depreciation.md) og [Skipta eign](tasks/split-fixed-asset.md).

Ef eign er skipt á fjárhagstímabil sem er síðar en tímabilið þegar eignin var keypt mun afskrift með minnkun bókfærðs virðis gilda fyrir bókað nettóvirði (BNV) fyrir fyrra ár. Hún mun einnig gilda fyrir leiðréttingafærslur kaupa og afskrifta sem myndaðar voru úr færslunni sem skipti eigninni. Þessi hegðun gerir ráð fyrir því að eignin hafi verið keypt á einu fjárhagsári og skipt á seinna fjárhagsári. Upphæðin sem verður að vera afskrifuð fyrir upprunalegu eignina eftir skiptin endurspeglar BNV eignarinnar, áður en henni var skipt, og leiðréttingarfærslu kaupa og afskriftar sem var bókuð fyrir skiptinguna.

Eftirfarandi skilyrði eru til dæmis í gildi:

- Fjárhagstímabilið er frá 30. júní til 1. júlí.
- Prósenta lækkandi afskriftar er 18 prósent og eign er keypt í júní 2019 á kaupverðinu $10.000.
- Afskrift fyrsta fjárhagsárs jafngildir $18.000, mánaðarleg afskrift samsvarar $150 og eignin er síðan afskrifuð fram í nóvember 2019 að upphæð $738,75.
- Í nóvember 2019 er 80 prósentum af eigninni skipt í aðra eign.

[![Afskrift lækkandi stöðu eftir skipti](./media/reduce-balance-depreciation-after-split.png)](./media/reduce-balance-depreciation-after-split.png)

Upphæðin til afskriftar fyrir upprunalegu eignina er $1.822,25. Þessi upphæð samsvarar BNV áður en skipt færsla er bókuð ($9111,25), auk kaupleiðréttingar sem er mynduð við bókun á skiptifærslunni (-$8000), auk afskriftarleiðréttingarinnar sem er mynduð við skiptifærsluna ($711). Þess vegna er afskriftin fyrir annað ár (1.822,25 × 18 prósent) ÷ 12 = $27,33.

Upphæðin til afskriftar fyrir nýju eignina á fyrsta árinu er (8.000 × 18 prósent) ÷ 12 = $120.
