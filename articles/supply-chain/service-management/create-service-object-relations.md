---
title: Um tengsl þjónustuhluta
description: Þessi grein lýsir því hvernig á að stofna tengsl þjónustuhlutar í þjónustusamningi og þjónustupöntun.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b4d9424b5678a6f37d46203e5d4e359b020fda7a
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016971"
---
# <a name="create-service-object-relations"></a>Um tengsl þjónustuhluta 

[!include [banner](../includes/banner.md)]


Þessi grein lýsir því hvernig á að stofna tengsl þjónustuhlutar í þjónustusamningi og þjónustupöntun. Þegar þú býrð til þjónustuhlutvensl tengirðu þjónustuhlutinn við þjónustusamning eða þjónustupöntun. Þegar beiðnir þjónustu viðskiptavinar fyrir vöru sem þjónustuhlut, hægt er að velja þá þjónustuhlutar af lista yfir tengsl þjónustuhluta.

## <a name="create-a-service-object-relation-for-a-service-agreement"></a>Stofna tengsl þjónustuhlutar fyrir þjónustusamning

Fylgið eftirfarandi skrefum til að stofna þjónustuhlutatengsl fyrir þjónustusamning:

1.  Veljið **Þjónustustjórnun** \> **Þjónustusamningar** \> **þjónustusamningar**.

2.  Í **Þjónustusamningar** listanum, velja núverandi þjónustusamning eða smella á **Nýtt** til að búa til nýjan þjónustusamning.

3.  Í **þjónustusamningar** skjámynd í **Aðgerðarúða** á flipanum **Þjónustusamningur** í **Tengsl** flokknum, skal smella á **Þjónustuhlutir**.

4.  Í **Þjónustuhlutir** skjámynd, smelltu **Nýtt**, og veldu síðan þjónustuhlut fyrir þessa þjónustusamning.

5.  Til að úthluta sniðmátaruppskrift (BOM) til þjónustusamningsins, smelltu á **Aðgerðir** og veldu síðan **Hengja við sniðmát BOM**. Í **Velja sniðmát BOM** skjámynd, í **Sniðmát BOM** reit, velja sniðmát. 

## <a name="create-a-service-object-relation-for-a-service-order"></a>Stofna tengsl þjónustuhlutar í þjónustupöntun

Fylgið eftirfarandi skrefum til að stofna tengsl þjónustuhlutar í þjónustupöntun:

1.  Smelltu á **Þjónustustjórnun** \> **Þjónustupantanir** \> **Þjónustupantanir**.

2.  Í **þjónustupantanir** listanum, velja núverandi þjónustupöntun, eða búa til nýja þjónustupöntun.

3.  Í **þjónustupantanir** skjámynd á **Aðgerðarúða**, á flipanum **Þjónustupöntun**, í flokknum **Tengsl** skal velja **Þjónustuhlutir**.

4.  Í **Þjónustuhlutir** skjámynd, smelltu **Nýtt**, og veldu síðan þjónustuhlutur fyrir þessa þjónustupöntun.

5.  Til að úthluta sniðmát BOM til þjónustusamninginn, smelltu á **Aðgerðir** og veldu síðan **Hengja við sniðmát BOM**. Í **Velja sniðmát BOM** skjámynd, í **Sniðmát BOM** reit, velja sniðmát. 


## <a name="see-also"></a>Sjá einnig

[Yfirlit yfir þjónustuhluti](service-objects.md)

[Tengsl þjónustuhluta](service-object-relations.md)

[Sniðmátsuppskriftir](template-boms.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]