---
title: Margar birgðafærslur fyrir rununúmer þegar slökkt er á „Við efnislega uppfærslu“
description: Fjölmargar birgðafærslur eru stofnaðar eftir að þú stillir innkaupapöntunarlínu fyrir vörur þar sem valkosturinn „Við efnislega uppfærslu“ fyrir lotunúmerahópinn er stilltur á Nei.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventNumGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: b8aef8835e90b7437bb7833c13c3d287d4ca836bf1fefc01bfeafef1c93329bc
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768595"
---
# <a name="multiple-inventory-transactions-for-batch-numbers-when-on-physical-update-is-disabled"></a>Margar birgðafærslur fyrir rununúmer þegar slökkt er á „Við efnislega uppfærslu“

KB númer: 4613390

## <a name="symptoms"></a>Einkenni

Fjölmargar birgðafærslur eru stofnaðar eftir að þú stillir innkaupapöntunarlínu fyrir vörur þar sem valkosturinn **Við efnislega uppfærslu** fyrir lotunúmerahópinn er stilltur á *Nei*.

Þegar búið er að stofna vöru þar sem valkosturinn **Við efnislega uppfærslu** í lotunúmeraflokknum er stilltur á *Nei* stofnar kerfið sjálfkrafa nýtt lotunúmer ef breyta á innkaupalínumagni og vista síðuna fyrir innkaupapöntun.

## <a name="resolution"></a>Upplausn

Stillingin **Við efnislega uppfærslu** fyrir lotunúmerahópa virkar með eftirfarandi hætti:

- Þegar valkosturinn er stilltur á *Já* eru ný lotunúmer aðeins búin til eftir efnislegar uppfærslur (til dæmis þegar atriði eru send eða móttekin).
- Þegar valkosturinn er stilltur á *Nei* er nýtt lotunúmer stofnað í hvert sinn sem viðeigandi uppfærsla á sér stað (til dæmis þegar nýju magni er bætt við innkaupapöntun).
