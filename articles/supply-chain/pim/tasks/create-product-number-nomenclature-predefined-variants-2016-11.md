---
title: Stofna nafnakerfi afurðarnúmers fyrir fyrirframskilgreind afurðarafbrigði
description: Þetta efni útskýrir hvernig á að setja inn nafnakerfi afurðarnúmers fyrir fyrirframskilgreind afurðarafbrigði og hvernig því er úthlutað á viðeigandi afurðarvíddarflokknum.
author: ShylaThompson
manager: tfehr
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3a15d1f4ecbf85e22bfadc1dd680d24bc56d807f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007542"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a>Stofna nafnakerfi afurðarnúmers fyrir fyrirframskilgreind afurðarafbrigði

[!include [banner](../../includes/banner.md)]

Þetta efni útskýrir hvernig á að setja inn nafnakerfi afurðarnúmers fyrir fyrirframskilgreind afurðarafbrigði og hvernig því er úthlutað á viðeigandi afurðarvíddarflokknum. Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF. Nýtt nafnakerfi afurðarnúmers er úthlutað á afurðavíddaflokkinn Litur og stærð. Þetta verk myndi yfirleitt vera framkvæmt af hálfu vöruhönnuðar.


## <a name="create-a-product-number-nomenclature"></a>Stofnaðu Nafnakerfi afurðarnúmers
1. Veldu **Skilgreining afurðarafbrigðislíkans**.
2. Veldu **Nafnakerfi afurðar**.
3. Veljið **Nýtt**.
4. Í reitnum **Heiti** er fært inn heiti nafnakerfis sem gerir auðveldara að greina viðmiðunarafurðarvíddarflokk, til dæmis `ColorSize`.
5. Í reitinn **Lýsing** skal slá inn gildi.
6. Veljið **Bæta við**.
7. Veldu númer **afurðarsniðmáts**.
8. Veljið **Bæta við**.
9. Veldu **Textafasta**.
10. Í reitnum **Texti** skal slá inn gildi.
11. Veljið **Bæta við**.
12. Veldu **Litur**.
13. Veljið **Bæta við**.
14. Veldu **Textafasta**.
15. Í reitnum **Texti** skal slá inn gildi.
16. Veljið **Bæta við**.
17. Veldu **Stærð**.
18. Lokið síðunni.

## <a name="assign-the-nomenclature-to-a-product-master"></a>Úthluta skal nafnakerfi á afurðarsniðmát
1. Veldu **Afurðavíddaflokka**.
2. Veldu hópinn **SizeCol afurðarvídd**.
3. Veljið **Breyta**.
4. Veldu **Já** í reitnum **Nota nafnakerfi**.
5. Í reitnum **Nafnakerfi afurðarafbrigðisnúmers** skal færa inn eða velja gildi.
6. Lokið síðunni.

