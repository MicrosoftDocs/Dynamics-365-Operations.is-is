---
title: Virkja samræmda meðhöndlun afhendingarmáta í rásum rafrænna viðskipta
description: Þessi grein lýsir því hvernig á að virkja samræmda afhendingarham meðhöndlun til að takast á við hugsanleg vandamál sem tengjast gjaldstreymi inn Microsoft Dynamics 365 Commerce rafræn viðskipti.
author: gvrmohanreddy
ms.date: 02/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: 43450c9d380bd57c234bb1c9acfbe296ab115f14
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279651"
---
# <a name="enable-consistent-delivery-mode-handling-in-e-commerce-channels"></a>Virkja samræmda meðhöndlun afhendingarmáta í rásum rafrænna viðskipta 

[!include [banner](includes/banner.md)]

Þessi grein lýsir því hvernig á að virkja samræmda afhendingarham meðhöndlun til að takast á við hugsanleg vandamál sem tengjast gjaldstreymi inn Microsoft Dynamics 365 Commerce rafræn viðskipti.

Í Dynamics 365 Commerce, gjöld sem ekki eru hlutfallsleg á hausstigi eru ekki sjálfgefið notuð í rafrænum viðskiptarásum. Þessi hegðun gæti valdið öðru eða báðum eftirfarandi vandamálum í rafrænum viðskiptarásum:

- Gjöld sem ekki eru hlutfallsleg á hausstigi birtast ekki.
- Gjöld fyrir afhendingarmáta eru ekki í samræmi á milli vals á afhendingarmáta og yfirlits yfir afgreiðslupöntun.

Til að laga þessi vandamál verður þú að kveikja á **Virkjaðu samræmda afhendingarham meðhöndlun í rás** eiginleiki. Þessi eiginleiki tryggir að gjöld á haus sem ekki eru hlutfallsleg birtast í rafrænum viðskiptarásum og að afhendingarupplýsingar sölupöntunar séu meðhöndlaðar stöðugt af sama verkflæði beiðninnar.

## <a name="turn-on-the-enable-consistent-delivery-mode-handling-in-channel-feature"></a>Kveiktu á Virkja samræmda afhendingarham meðhöndlun í rás eiginleikanum

Til að virkja **Virkjaðu samræmda afhendingarham meðhöndlun í rás** í höfuðstöðvum Commerce skaltu fylgja þessum skrefum.

1. Opnaðu **Eiginleikastjórnun** vinnusvæði (**Kerfisstjórnun \> Vinnurými \> Eiginleikastjórnun**).
1. Leitaðu að og veldu á listanum yfir tiltæka eiginleika **Virkjaðu samræmda afhendingarham meðhöndlun í rás**.
1. Í hægri glugganum velurðu **Virkja núna**.
