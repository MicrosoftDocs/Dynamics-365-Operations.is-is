---
title: Fela afhendingarstillingar utan flutningsaðila fyrir sendingarmöguleikana í POS
description: Þetta efni lýsir stillingarvalkosti sem getur komið í veg fyrir að afhendingarstig utan flutningsaðila birtist fyrir val þegar sendingarpantanir eru búnar til í forritinu sölustaðnum (POS).
author: hhainesms
ms.date: 10/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: a5f08fc86dc093fd0ead219b808fa720a43f6b6b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797119"
---
# <a name="hide-non-carrier-delivery-modes-from-the-shipping-options-in-pos"></a>Fela afhendingarstillingar utan flutningsaðila fyrir sendingarmöguleikana í POS


[!include [banner](includes/banner.md)]

Þetta efni lýsir stillingarmöguleikum sem er í boði fyrir POS-forritið. Þessi stillingarmöguleiki breytir hegðun við val á afhendingaraðferð þegar sendingarpantanir eru búnar til í POS.

Þegar notendur stofna sendingarpantanir viðskiptavina í POS geta þeir valið afhendingaraðferð fyrir sendinguna. Þessi virkni er tiltæk óháð því hvort öll pöntunin er send eða eingöngu valdar línur.

Sjálfgefið er að svarglugginn þar sem afhendingarháttur er valinn sýnir allar gildar afhendingarstillingar fyrir samsetningu rásar, hlutar og afhendingarfangs. Þessar afhendingaraðferðir eru skilgreindar á síðunni **Afhendingarmátar** í Bakvinnslu (**Sala og markaðsstarf \> Uppsetning \> Dreifing \> Afhendingarmátar**). Afhendingaraðferðir „ekki flutningsaðili“, svo sem **Framkvæma** eða **Pallbíll**, gæti einnig birst fyrir val í valmyndinni.

Hins vegar hefur eiginleika verið bætt við sem gerir þér kleift að fela afhendingaraðferðir án flutningsaðila í valmyndinni. Til að kveikja á þessum eiginleika, á síðunni **Commerce-færibreytur**, á flipanum **Pantanir viðskiptavina**, stillirðu valkostinn **Sýna aðeins valkosti flutningsmáta fyrir skipapantanir** á **Já**. Eftir að þú kveikir á þessari aðgerð og keyrir viðeigandi dreifingarvinnslur til að samstilla upplýsingarnar við gagnagrunn rásarinnar, birtast ekki afhendingarstillingar fyrir flutning fyrir val á meðan á því að búa til sendingarpantanir í POS.


[!INCLUDE[footer-include](../includes/footer-banner.md)]