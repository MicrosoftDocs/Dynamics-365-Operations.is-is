---
title: Setja upp verð sem byggir á eigindum fyrir skilgreinanlegar afurðir
description: Þetta efni útskýrir hvernig á að setja upp eigindabyggða úthlutun.
author: ShylaThompson
manager: tfehr
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3a75f3afcf4761ac6a9575eae9a620a1e9f01c8e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430182"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a>Setja upp verð sem byggir á eigindum fyrir skilgreinanlegar afurðir

[!include [banner](../../includes/banner.md)]

Þetta efni útskýrir hvernig á að setja upp eigindabyggða úthlutun. Sem skilyrði, verður að hafa afbrigðalíkan afurðar sem hefur eitt eða fleiri íhluti og eiginleika. Þessi aðferð notar hágæða hátalara líkanið gögn fyrirtækisins sýnigögn USMF. Venjulega notar framleiðslustjóri þetta ferli.


## <a name="create-a-new-price-model"></a>Búa til nýtt verðlíkan
1. Veldu **Skilgreining afurðarafbrigðislíkans** á heimasíðunni.
2. Veldu **Afbrigðalíka afurðar** í kaflanum **Tenglar**.
3. Á listanum velurðu línuna fyrir **Hágæða hátalara** en velur ekki tengilinn fyrir heitið.
4. Í aðgerðarúðunni skal velja **Tegund**.
5. Veldu **Verðlíkön**.
6. Veljið **Nýtt**.
7. Í reitinn **Verðlíkan** skal rita gildi. Notið nafn sem gerir auðvelt að bera kennsl á líkan.  
8. Í reitinn **Lýsing** skal slá inn gildi.
9. Veljið **Vista**.

## <a name="add-price-elements"></a>Bæta við verðeiningum
1. Veljið **Breyta**. Hver íhlutur í framleiðslulíkani getur haft grunnverð einingu og fjölda verðsegðarreglna. Einnig er hægt að bæta verði í mismunandi gjaldmiðlum.  
2. Í reitinn **Grunnverðssegð** skal slá inn gildi. Til dæmis, skrifið 100. Grunnverðssegð getur verið tölugildi eða það getur verið samsett af útreikningi sem felur í sér eina eða fleiri eigindir.  
3. Veljið **Bæta við**.
4. Í reitinn **Heiti** skaltu færa inn `Rosewood`. Nafn verð segð gerir auðveldara að verð einingarinnar sem stendur. Í þessu dæmi er mælt stofna verðeining fyrir Rosewood speaker cabinet ljúka valkost.  
5. Veldu **Breyta ástandi**. Skilyrði verð hjálpar til við að tryggja samræmda segðareining verð er innifalinn í söluverði ef tiltekna samsetningu af eigindir eru til staðar.  
6. Í reitinn **ConstraintBody** skal slá inn `CabinetFinish=="Rosewood"`.
7. Veljið **Í lagi**.
8. Í reitinn **Segð** skal slá inn gildi. Til dæmis, slá inn `50`. 
9. Lokið síðunni.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]