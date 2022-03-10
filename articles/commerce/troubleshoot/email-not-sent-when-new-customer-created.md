---
title: Velkominn tölvupóstur er ekki sendur þegar nýir viðskiptavinir eru búnir til
description: Þetta efni veitir leiðbeiningar um úrræðaleit sem geta hjálpað ef tilkynning í tölvupósti er ekki send þegar nýr viðskiptavinur er búinn til í Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 02/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: 1a4faf6cd189f69232e7f9ab8d0e79b320cfe2d9
ms.sourcegitcommit: d2e5d38ed1550287b12c90331fc4136ed546b14c
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/25/2022
ms.locfileid: "8349931"
---
# <a name="welcome-email-is-not-sent-when-new-customers-are-created"></a>Velkominn tölvupóstur er ekki sendur þegar nýir viðskiptavinir eru búnir til

[!include [banner](../../includes/banner.md)]

Þetta efni veitir leiðbeiningar um úrræðaleit sem geta hjálpað ef tilkynning í tölvupósti er ekki send þegar nýr viðskiptavinur er búinn til í Microsoft Dynamics 365 Commerce.

## <a name="description"></a>Lýsing

Þegar nýr viðskiptavinur er stofnaður í höfuðstöðvum Commerce er velkominn tölvupóstur ekki sendur til viðskiptavinarins, jafnvel þó að tölvupósttilkynning sé stillt fyrir **Viðskiptavinur búinn til** gerð tölvupósts tilkynninga.

## <a name="resolution"></a>Upplausn

### <a name="set-the-correct-email-id-value-for-the-customer-created-email-notification-type"></a>Stilltu rétt tölvupóstauðkennisgildi fyrir tegundina Tilkynningatilkynninga í tölvupósti til viðskiptavinar

Til að stilla rétt **Netfang** gildi fyrir **Viðskiptavinur búinn til** tegund tölvupósttilkynningar í höfuðstöðvum, fylgdu þessum skrefum.

1. Fara til **Verslun og verslun \> Uppsetning höfuðstöðva \> Tilkynningarprófíll fyrir viðskiptatölvupóst**.
1. Í vinstri yfirlitsrúðunni skaltu velja tölvupósttilkynningarsniðið.
1. Undir **Stillingar smásöluviðburðatilkynninga**, fyrir **Viðskiptavinur búinn til** tegund tölvupósts tilkynninga, stilltu **Netfang** sviði til **NewCust**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Setja upp forstillingu tilkynningar í tölvupósti](../email-notification-profiles.md)
