---
title: Bæta útreikningi við afbrigðalíkan afurðar
description: Þessi verklýsing sýnir hvernig á að bæta nýjan útreikning við afbrigðalíkani afurðar.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 55f8fcfdafb2d5fb5a4d4800221fabf4b2111f86
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150264"
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

