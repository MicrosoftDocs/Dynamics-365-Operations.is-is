---
title: Stofna farmbréf
description: Þessi grein lýsir því hvernig á að búa til farmskírteini þegar verið er að nota vöruhúsastjórnunarferli.
author: Weijiesa
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
ms.author: weijiesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 34e84fee13dcff574f1700ba2b8f577f4c401cbc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885784"
---
# <a name="create-a-bill-of-lading"></a>Stofna farmbréf

[!include [banner](../includes/banner.md)]

Þessi grein lýsir því hvernig á að búa til farmskírteini þegar verið er að nota vöruhúsastjórnunarferli.  

Farmbréf er lagagerningur milli flytjanda sem sendir vörur og flutningsaðila. Skjalið fylgir sendum vörum, og það gegnir hlutverki kvittunar fyrir sendingu þegar vörur eru afhentar á ákvörðunarstað. Ef verið er að nota vöruhúsakerfi, eru tvær leiðir til að mynda farmbréf:

  -   Búa til skýrslu handvirkt með því að nota síðuna **farmbréf** .
  -   Búa til skýrslu úr **vinnusvæði farmáætlunar**.

Ef þú myndar farmbréf úr **vinnusvæði farmáætlun**, verður staða farms að vera **Sent.** Ef fleiri en einn sendingar eru í farminum er farmbréf stofnuð fyrir hverja sendingu. Eftir að farmbréf hefur verið stofnað er hægt gera breytingar á því á **farmbréf** síðu.

## <a name="master-bill-of-lading"></a>Aðalfarmbréf
Ef fleiri en ein sending er í farmi er hægt að Stofna aðalfarmbréf. Þetta hefur sama útlit og upplýsingar um farmbréf, en inniheldur samantekið efni fyrir allar sendingar. Ef valkosturinn **Stofna aðalfarmbréf þegar það eru fleiri en ein sending í farmi** er stilltur á **Já** á síðunni **færibreytur Flutningsstjórnunar** er aðalfarmbréfið myndað sjálfkrafa ef þú stofnar farmbréf úr **vinnusvæði Farmáætlun**, og það eru fleiri en ein sending til staðar. Einnig er hægt að fá lista yfir í farmbréf með því að smella á **tengdar upplýsingar** &gt; **farmbréf**. Ef verið er að stofna farmbréf handvirkt er hægt að stofna aðalfarmbréf á **farmbréf** síðu.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]