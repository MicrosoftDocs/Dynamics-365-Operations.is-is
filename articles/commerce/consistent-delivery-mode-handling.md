---
title: Virkjaðu samræmda afhendingarham meðhöndlun í rafrænum viðskiptarásum
description: Þetta efnisatriði lýsir því hvernig á að virkja samræmda afhendingarham meðhöndlun til að takast á við hugsanleg vandamál sem tengjast gjaldstreymi inn Microsoft Dynamics 365 Commerce rafræn viðskipti.
author: gvrmohanreddy
ms.date: 02/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: 4cecd70dacd72572afc8e6cb65530bf2be4cc93d
ms.sourcegitcommit: d2e5d38ed1550287b12c90331fc4136ed546b14c
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/25/2022
ms.locfileid: "8349926"
---
# <a name="enable-consistent-delivery-mode-handling-in-e-commerce-channels"></a>Virkjaðu samræmda afhendingarham meðhöndlun í rafrænum viðskiptarásum 

[!include [banner](includes/banner.md)]

Þetta efnisatriði lýsir því hvernig á að virkja samræmda afhendingarham meðhöndlun til að takast á við hugsanleg vandamál sem tengjast gjaldstreymi inn Microsoft Dynamics 365 Commerce rafræn viðskipti.

Í Dynamics 365 Commerce, gjöld á haus sem ekki eru hlutfallsleg eru ekki sjálfgefið notuð í rafrænum viðskiptarásum. Þessi hegðun gæti valdið öðru eða báðum eftirfarandi vandamálum í rafrænum viðskiptarásum:

- Gjöld sem ekki eru hlutfallsleg á hausstigi birtast ekki.
- Gjöld fyrir afhendingarmáta eru ekki í samræmi á milli vals á afhendingarmáta og yfirlits yfir afgreiðslupöntun.

Til að laga þessi vandamál verður þú að kveikja á **Virkjaðu samræmda afhendingarham meðhöndlun í rás** eiginleiki. Þessi eiginleiki tryggir að gjöld á haus sem ekki eru hlutfallsleg birtast í rafrænum viðskiptarásum og að upplýsingar um afhendingu sölupöntunar séu meðhöndlaðar stöðugt af sama verkflæði beiðninnar.

## <a name="turn-on-the-enable-consistent-delivery-mode-handling-in-channel-feature"></a>Kveiktu á Virkja samræmda afhendingarham meðhöndlun í rás eiginleikanum

Til að virkja **Virkjaðu samræmda afhendingarham meðhöndlun í rás** í höfuðstöðvum Commerce skaltu fylgja þessum skrefum.

1. Opnaðu **Eiginleikastjórnun** vinnusvæði (**Kerfisstjórnun \> Vinnurými \> Eiginleikastjórnun**).
1. Leitaðu að og veldu á listanum yfir tiltæka eiginleika **Virkjaðu samræmda afhendingarham meðhöndlun í rás**.
1. Í hægri glugganum velurðu **Virkja núna**.
