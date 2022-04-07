---
title: Endurgreiðanleg gjöld eru rangreiknuð út frá því magni sem skilað er
description: Þetta efnisatriði veitir leiðbeiningar um úrræðaleit sem geta hjálpað þegar gjaldkerar sjá rangt endurgreiðanleg gjöld á sölustað (POS) fyrir magn vara sem er skilað.
author: gvrmohanreddy
ms.date: 03/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: c8ecaa0cb73d06ac66b57cce815264e841a2259b
ms.sourcegitcommit: 94ebdaae6dc996b205ac78ed546e38f91f4f46ed
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/28/2022
ms.locfileid: "8489726"
---
# <a name="refundable-charges-are-miscalculated-based-on-the-quantity-returned"></a>Endurgreiðanleg gjöld eru rangreiknuð út frá því magni sem skilað er

[!include [banner](../../includes/banner.md)]

Þetta efnisatriði veitir leiðbeiningar um úrræðaleit sem geta hjálpað þegar gjaldkerar sjá rangt endurgreiðanleg gjöld á sölustað (POS) fyrir magn vara sem er skilað.

## <a name="description"></a>Lýsing

Viðskiptavinur skilar hlutamagni af vörum sem voru keyptar fyrir sölupöntun sem hefur endurgreiðanleg gjöld á línustigi. Hins vegar, í stað þess að sýna endurgreiðslu að hluta, sýnir POS öll gjöld sem endurgreiðanleg.

Til dæmis kaupir viðskiptavinur fimm vörur á $5 fyrir hverja vöru, fyrir heildargjöld upp á $25. Viðskiptavinurinn skilar síðan þremur af fimm hlutum. Hins vegar er gjaldkeranum sýnd $25 endurgreiðanleg gjöld í POS, í stað væntanlegs $15 endurgreiðanlegs gjalds fyrir þá þrjá hluti sem voru skilaðir.

## <a name="resolution"></a>Upplausn

### <a name="turn-on-the-enable-refunding-charges-based-on-the-refunded-quantity-feature"></a>Kveiktu á Virkja endurgreiðslugjöld byggð á eiginleikanum fyrir endurgreitt magn

Frá Microsoft Dynamics 365 Commerce útgáfa 10.0.26, the **Virkjaðu endurgreiðslugjöld byggð á endurgreiddu magni** eiginleiki gerir kleift að reikna endurgreiðanleg gjöld á línustigi út frá því magni vara sem er skilað.

Til að virkja **Virkjaðu endurgreiðslugjöld byggð á endurgreiddu magni** í höfuðstöðvum Commerce skaltu fylgja þessum skrefum.

1. Opnaðu **Eiginleikastjórnun** vinnusvæði (**Kerfisstjóri \> Vinnurými \> Eiginleikastjórnun**).
1. Í listanum yfir tiltæka eiginleika skaltu leita að og velja **Virkjaðu endurgreiðslugjöld byggð á endurgreiddu magni** eiginleiki.
1. Í hægri glugganum velurðu **Virkja núna**.
