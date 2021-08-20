---
title: Stuðningstími fyrir stjórnun líkans (forútgáfa)
description: Í þessu efnisatriði er lýst leiðum til að vinna með vélnámslíkönum fyrirtækisins til að hámarka spágildi þeirra.
author: ShivamPandey-msft
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 3daec03b7ba349d8f72863317e2d601a83417d58
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/17/2021
ms.locfileid: "6638393"
---
# <a name="model-management-lifecycle-preview"></a>Stuðningstími fyrir stjórnun líkans (forútgáfa)

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er lýst leiðum til að vinna með vélnámslíkönum fyrirtækisins til að hámarka spágildi þeirra.

Við mælum með því að þú þjálfir AI-líkanið í sandkassaumhverfi og notir síðan stýrðar lausnir til að setja það upp í framleiðsluumhverfi. Þessi aðferð hjálpar til við að tryggja að réttar stýringar séu til staðar til að stjórna stuðningstíma líkans.

Þar sem AI-líkanið er byggt á fyrirliggjandi reikningi og gögnum viðskiptavina er mikilvægt að sandkassaumhverfið sé með nýlegt afrit af framleiðslugögnunum. Þú getur byrjað á því að þjálfa líkanið þitt með því að fylgja skrefunum í [Nota greiðsluspár viðskiptavina](use-customer-payment-predictions.md). Eftir að líkanið hefur verið endurþjálfað skaltu meta niðurstöðurnar eins og lýst er í [Leggja mat á upprunalega greiðsluspá viðskiptavinarins](evaluate-payment-prediction.md). Notaðu upplýsingarnar í [Bæta spálíkanið](improve-model.md) til að prófa þig áfram með samsetningar eiginleika og síu sem getur hjálpað til við að bæta líkanið.

Þegar niðurstöður þjálfunarinnar eru fullnægjandi skaltu fylgja þessum skrefum í [Dreifa AI-líkaninu](https://docs.microsoft.com/ai-builder/distribute-model) til að flytja líkanið í vinnsluumhverfið.