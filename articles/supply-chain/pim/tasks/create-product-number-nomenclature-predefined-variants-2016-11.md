---
title: Stofna nafnakerfi afurðarnúmers fyrir fyrirframskilgreind afurðarafbrigði
description: Þessi grein útskýrir hvernig á að setja inn nafnakerfi afurðarnúmers fyrir fyrirframskilgreind afurðarafbrigði og hvernig því er úthlutað á viðeigandi afurðarvíddarflokknum.
author: t-benebo
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e77c8eabe1657f7fbfef71747627207dccff3b60
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887313"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a>Stofna nafnakerfi afurðarnúmers fyrir fyrirframskilgreind afurðarafbrigði

[!include [banner](../../includes/banner.md)]

Þessi grein útskýrir hvernig á að setja inn nafnakerfi afurðarnúmers fyrir fyrirframskilgreind afurðarafbrigði og hvernig því er úthlutað á viðeigandi afurðarvíddarflokknum. Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF. Nýtt nafnakerfi afurðarnúmers er úthlutað á afurðavíddaflokkinn Litur og stærð. Þetta verk myndi yfirleitt vera framkvæmt af hálfu vöruhönnuðar.


## <a name="create-a-product-number-nomenclature"></a>Stofnaðu Nafnakerfi afurðarnúmers

1. Farið í **Afurðaupplýsingastjórnun \> Uppsetning \> Nafnakerfi afurðar**.
1. Veljið **Nýtt**.
1. Í reitnum **Heiti** er fært inn heiti nafnakerfis sem gerir auðveldara að greina viðmiðunarafurðarvíddarflokk, til dæmis `ColorSize`.
1. Í reitinn **Lýsing** skal slá inn gildi.
1. Veljið **Bæta við**.
1. Veldu númer **afurðarsniðmáts**.
1. Veljið **Bæta við**.
1. Veldu **Textafasta**.
1. Í reitnum **Texti** skal slá inn gildi.
1. Veljið **Bæta við**.
1. Veldu **Litur**.
1. Veljið **Bæta við**.
1. Veldu **Textafasta**.
1. Í reitnum **Texti** skal slá inn gildi.
1. Veljið **Bæta við**.
1. Veldu **Stærð**.
1. Lokið síðunni.

## <a name="assign-the-nomenclature-to-a-product-master"></a>Úthluta skal nafnakerfi á afurðarsniðmát

1. Veldu **Afurðavíddaflokka**.
2. Veldu hópinn **SizeCol afurðarvídd**.
3. Veljið **Breyta**.
4. Veldu **Já** í reitnum **Nota nafnakerfi**.
5. Í reitnum **Nafnakerfi afurðarafbrigðisnúmers** skal færa inn eða velja gildi.
6. Lokið síðunni.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]