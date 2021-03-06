---
title: Ekki er farið eftir stillingum losunarreglu í uppskriftarlínum
description: Ekki er farið eftir stillingum losunarreglu í uppskriftarlínum
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PurchTable,ProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 84a84728016119a2a02f59f6903171afbceb48e7
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026611"
---
# <a name="flushing-principle-settings-on-bom-lines-arent-respected"></a>Ekki er farið eftir stillingum losunarreglu í uppskriftarlínum

KB númer: 4612725

## <a name="symptoms"></a>Einkenni

Þetta vandamál kemur upp þegar reiturinn **Sjálfvirk uppskriftanotkun** á flipanum **Sjálfvirk uppfærsla** á síðunni **Færibreytur framleiðslustýringar** er stilltur á *Losunarregla*. Þessi stilling gefur til kynna að allar uppskriftalínur skuli sjálfkrafa notast þegar innkaupapöntun berst. Ef reiturinn **Losunarregla** á uppskriftarlínur er sérstaklega stilltur á *Handvirkt* má búast við að uppskriftarlínurnar verði ekki notaðar sjálfkrafa. Þegar þetta vandamál kemur eru uppskriftarlínur þar sem reiturinn **Losunarregla** er stilltur á *Handvirkt* samt notaðar.

## <a name="resolution"></a>Upplausn

Ef vandamálið kemur upp gæti verið að breytur fyrir framleiðslustjórnun séu settar upp til að víkja frá stillingu **Losunarreglu** á uppskriftarlínur. Á síðunni **færibreytur Framleiðslustýringar**, á flipanum **Sjálfvirk uppfærsla**, skal athuga gildið í reitnum **Sjálfvirk uppskriftarnotkun**. Ef það er stillt á *Alltaf* mun kerfið líta framhjá stillingu **Losunarregla** á öllum uppskriftarlínu og mun alltaf losa línurnar. Til að láta kerfið virða **Losunarregla** á uppskriftarlínum er gildinu í reitnum **Sjálfvirk uppskriftanotkun** breytt í *Losunarregla*.
