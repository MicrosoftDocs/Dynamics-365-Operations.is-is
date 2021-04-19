---
title: Bæta útreikningi við afbrigðalíkan afurðar
description: Þessi verklýsing sýnir hvernig á að bæta nýjan útreikning við afbrigðalíkani afurðar.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 268baa4b518f6df52d4393f7278a79cbe1733844
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812676"
---
# <a name="add-a-calculation-to-a-product-configuration-model"></a>Bæta útreikningi við afbrigðalíkan afurðar

[!include [banner](../../includes/banner.md)]

Þessi verklýsing sýnir hvernig á að bæta nýjan útreikning við afbrigðalíkani afurðar. Hún sýnir hvernig hægt er að stofna röksegð með notkun "Ef" virknitákn til að setja hæð hátalara til 10 fyrir hvítum hátalara og 15 fyrir allar aðrar frágang húss. Ferlið notar hágæða hátalaraíhlut fyrir USMF sýnigögn fyrirtækisins.


## <a name="add-a-calculation"></a>Bæta við útreikningum

## <a name="create-calculation-expression"></a>Stofna segð útreiknings
1. Smella á Breyta segð.
2. Færið inn í svæðið ConstraintBody ‚If[CabinetFinish == „white", 10, 15]'.
3. Smella á Villuleita.
4. Smellið á „Loka“.
5. Smellið á „Í lagi“.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]