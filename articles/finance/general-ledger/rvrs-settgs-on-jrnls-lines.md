---
title: Afturkalla stillingar á færslubókum og línum
description: Í þessu efnisatriði er útskýrt hvers vegna bakfærsla sem færð var inn í almenna færslubók er hugsanlega ekki höfð með í bókuðu færslunni.
author: kweekley
ms.date: 04/29/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-5-05
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ff8c0bda8e750e95261039b373cfb96a76034f6f
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/07/2022
ms.locfileid: "8724446"
---
# <a name="reverse-settings-on-journals-and-lines"></a>Afturkalla stillingar á færslubókum og línum

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er útskýrt hvers vegna bakfærsla sem færð var inn í almenna færslubók er hugsanlega ekki höfð með í bókuðu færslunni.  

## <a name="symptom"></a>Einkenni

Almenn færslubók inniheldur bakfærslu og dagsetningu hennar í færslubókinni. Þegar þú bókar dagbókina er ekkert fylgiskjal bakfært. Af hverju gerist þetta?

## <a name="resolution"></a>Lausn

Þegar færslubókin er bókuð skoðar bakfærsluferlið eingöngu stillingar **Bakfærslu** og **Dags. bakfærslu** í hlutanum **Línur** í fylgiskjalinu. Þessi aðferð gerir færslubók kleift að hafa með sum fylgiskjöl sem eru merkt fyrir bakfærslu og önnur ekki.

Gildin úr færslubókinni eru aðeins notuð sem sjálfgefin gildi þegar *nýjum* línum er bætt við. Breyting á gildum í færslubókinni hefur ekki áhrif á línur sem eru til staðar. Í þessu dæmi voru línur afsláttarkóðans slegnar inn fyrst. Þegar þú slærð inn línuupplýsingarnar áður en þú tilgreinir færslubókina sem bakfærslu, verður merking hennar sem bakfærslu og dagsetningu bakfærslu ekki notuð í neinum línum sem eru til staðar.

Ef bakfærslunni eða dagsetningu bakfærslunnar er breytt í fyrirliggjandi línu mun sú breyting koma fram í öðrum línum í sama fylgiskjalinu. Til að hámarka afköst er netið ekki uppfært eftir að breytingar hafa verið færðar yfir á aðrar línur. Hægt er að birta uppfærð gildi með því að endurhlaða hnitanetið.


