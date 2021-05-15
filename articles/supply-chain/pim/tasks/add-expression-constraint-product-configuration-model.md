---
title: Bæta skorðu á segð við afbrigðalíkan afurðar
description: Þessi verklýsing sýnir hvernig hægt er að bæta nýjum skorðusegð við afbrigðalíkani afurðar.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9cd5475e48cbcd8dcee6b228297f58e364ac503d
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920882"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a>Bæta skorðu á segð við afbrigðalíkan afurðar

[!include [banner](../../includes/banner.md)]

Þessi verklýsing sýnir hvernig hægt er að bæta nýjum skorðusegð við afbrigðalíkani afurðar. Hún sýnir hvernig er hægt að gefa fyrirmæli sem um að hornvörn verður að nota í hátalara ef notandinn hefur valið sé framgrill í málmi. Ferlið notar hágæða hátalaraíhlut fyrir USMF sýnigögn fyrirtækisins.

## <a name="create-an-expression-constraint"></a>Stofna segð töfluskorðu

1. Farið í **Afurðarupplýsingastjórnun \> Afurðir \> Afbrigðalíkön afurða**.
3. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Þetta dæmi nota hágæða hátalara líkanið.  
4. Í listanum skal velja tengilinn í valinni línu.
5. Stækka **Skorður** hlutann.
6. Veljið **Bæta við**.
7. Velja **Stofna**.
8. Í reitinn **Heiti** skal slá inn gildi.

## <a name="enter-expression"></a>Færa inn segð

1. Veljið **Breyta segð**.
    * Ef notendaviðmótinu í verkinu á skráningu á þessu stigi er aflæsa, má nota IntelliSense og lista yfir tákn til að byggja skorðusegð.  
2. Í reitinn **ConstraintBody** skal færa inn 'Implies[FrontGrill=="Metal", CornerProtection] '.
    * Rökhugsun á bakvið þessa segð segir: Ef Framgrill er úr málmi, þá verður að velja valkostinn hornvörn.  
3. Veldu **Staðfesta**.
    * Villuleita aðgerð keyrir gegnum skorðusegð og athugar málskipanarvilla.  
4. Veljið **Loka**.
5. Veljið **Í lagi**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]