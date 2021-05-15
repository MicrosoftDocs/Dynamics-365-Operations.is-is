---
title: Setja upp verð sem byggir á eigindum fyrir skilgreinanlegar afurðir
description: Þetta efni útskýrir hvernig á að setja upp eigindabyggða úthlutun.
author: ShylaThompson
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0c30c520e7265c2676937f5191844f6789c364e6
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921242"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a>Setja upp verð sem byggir á eigindum fyrir skilgreinanlegar afurðir

[!include [banner](../../includes/banner.md)]

Þetta efni útskýrir hvernig á að setja upp eigindabyggða úthlutun. Sem skilyrði, verður að hafa afbrigðalíkan afurðar sem hefur eitt eða fleiri íhluti og eiginleika. Þessi aðferð notar hágæða hátalara líkanið gögn fyrirtækisins sýnigögn USMF. Venjulega notar framleiðslustjóri þetta ferli.


## <a name="create-a-new-price-model"></a>Búa til nýtt verðlíkan

1. Farið í **Afurðarupplýsingastjórnun \> Afurðir \> Afbrigðalíkön afurða**.
1. Á listanum velurðu línuna fyrir **Hágæða hátalara** en velur ekki tengilinn fyrir heitið.
1. Í aðgerðarúðunni skal velja **Tegund**.
1. Veldu **Verðlíkön**.
1. Veljið **Nýtt**.
1. Í reitinn **Verðlíkan** skal rita gildi. Notið nafn sem gerir auðvelt að bera kennsl á líkan.  
1. Í reitinn **Lýsing** skal slá inn gildi.
1. Veljið **Vista**.

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