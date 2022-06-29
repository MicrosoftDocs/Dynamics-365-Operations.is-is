---
title: Fækka dögum á áskrifarþóknunum
description: Til þess að stytta fjölda daga í fyrirliggjandi áskriftarþóknun er hægt að stofna nýja færslu, þar sem tímabilið sem ekki á lengur að vera hluti af áskriftarþóknun er fjarlægt.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 370722d5c2f66e316d7c37f711cdd086bc53f6a8
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/15/2022
ms.locfileid: "9014823"
---
# <a name="reduce-the-days-on-subscription-fees"></a>Fækka dögum á áskrifarþóknunum 

[!include [banner](../includes/banner.md)]


Til þess að stytta fjölda daga í fyrirliggjandi áskriftarþóknun er hægt að stofna nýja færslu, þar sem tímabilið sem ekki á lengur að vera hluti af áskriftarþóknun er fjarlægt.

## <a name="reduce-the-days-on-a-subscription-fee"></a>Fækka dögum í áskriftarþóknun

1.  Smellur **Þjónustustjórnun** \> **Þjónustuáskrift** \> **Allar þjónustuáskriftir**. Veldu þjónustuáskriftina og smelltu svo á **Áskriftargjald** í aðgerðasvæðinu

2.  Í reitnum **Gerð áskriftar** skal velja **Minnkunardagar**.

3.  Notaðu reitina **Frá dagsetningu** og **Til dagsetningar** til að skilgreina dagsetningabil áskriftargjaldsins, sem á að fjarlægja úr tímabili áskriftarþóknunar og smelltu síðan á **Í lagi**.

Til þess að skoða stofnaða færslu skal smella á **Þóknunarfærslur** í skjámyndinni **Áskrift**.

## <a name="example"></a>Dæmi

Ef tímabil áskriftarfærslu gildir frá 1. janúar til 31. janúar og þú vilt stytta tímabilið um 10 daga skaltu búa til nýja færslu þar sem stytta tímabilið er 1. janúar til 10. janúar. (Sytta tímabilið getur einnig verið 5. janúar til 15. janúar eða önnur tíu daga tímabil).

Ennfremur, ef **Frá dagsetningu** á stytta tímabilinu er 21. janúar (31 mínus 10) væri hægt að stilla **Til dagsetningar** á hvaða dagsetningu sem er eftir 31. janúar og 10 dagar verða samt sem áður fjarlægðir úr tímabili þóknunarfærslu.

## <a name="see-also"></a>Sjá einnig

[Dæmi um minnkunardaga](reduction-days-example.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]