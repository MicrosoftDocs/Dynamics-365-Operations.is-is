---
title: Stofna farmbréf
description: Þetta efnisatriði lýsir hvernig á að stofna farmbréf þegar verið er að nota vöruhúsakerfisferli.
author: MarkusFogelberg
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSBillOfLading, WHSLoadPlanningWorkbench, WHSBillOfLadingCarrier, WHSBillOfLadingOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: 193583
ms.assetid: 1ad0c1cb-4346-4042-a59b-923115fac03e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a14d971475c71e6a02957acfa0c6e6494c4638fc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5807633"
---
# <a name="create-a-bill-of-lading"></a>Stofna farmbréf

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir hvernig á að stofna farmbréf þegar verið er að nota vöruhúsakerfisferli.  

Farmbréf er lagagerningur milli flytjanda sem sendir vörur og flutningsaðila. Skjalið fylgir sendum vörum, og það gegnir hlutverki kvittunar fyrir sendingu þegar vörur eru afhentar á ákvörðunarstað. Ef verið er að nota vöruhúsakerfi, eru tvær leiðir til að mynda farmbréf:

  -   Búa til skýrslu handvirkt með því að nota síðuna **farmbréf** .
  -   Búa til skýrslu úr **vinnusvæði farmáætlunar**.

Ef þú myndar farmbréf úr **vinnusvæði farmáætlun**, verður staða farms að vera **Sent.** Ef fleiri en einn sendingar eru í farminum er farmbréf stofnuð fyrir hverja sendingu. Eftir að farmbréf hefur verið stofnað er hægt gera breytingar á því á **farmbréf** síðu.

## <a name="master-bill-of-lading"></a>Aðalfarmbréf
Ef fleiri en ein sending er í farmi er hægt að Stofna aðalfarmbréf. Þetta hefur sama útlit og upplýsingar um farmbréf, en inniheldur samantekið efni fyrir allar sendingar. Ef valkosturinn **Stofna aðalfarmbréf þegar það eru fleiri en ein sending í farmi** er stilltur á **Já** á síðunni **færibreytur Flutningsstjórnunar** er aðalfarmbréfið myndað sjálfkrafa ef þú stofnar farmbréf úr **vinnusvæði Farmáætlun**, og það eru fleiri en ein sending til staðar. Einnig er hægt að fá lista yfir í farmbréf með því að smella á **tengdar upplýsingar** &gt; **farmbréf**. Ef verið er að stofna farmbréf handvirkt er hægt að stofna aðalfarmbréf á **farmbréf** síðu.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]