---
title: Bæta útreikningi við afbrigðalíkan afurðar
description: Þessi verklýsing sýnir hvernig á að bæta nýjan útreikning við afbrigðalíkani afurðar.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d201061ff47203f09f96dc08ff6fc8ac437a6f9e
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570658"
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