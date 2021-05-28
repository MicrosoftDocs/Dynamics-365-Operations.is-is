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
ms.openlocfilehash: 1fa54cdfdbc5608fb6c7114dced0f96bab47253e
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026623"
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
