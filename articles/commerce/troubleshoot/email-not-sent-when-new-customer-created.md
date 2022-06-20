---
title: Kynningartölvupóstur er ekki sendur þegar nýir viðskiptavinir eru stofnaðir
description: Þessi grein veitir leiðbeiningar um bilanaleit sem geta hjálpað ef velkomin tölvupósttilkynning er ekki send þegar nýr viðskiptavinur er búinn til í Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 02/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: 8e95b33d4b8a9af13c613ab89dd33de6b4934694
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853684"
---
# <a name="welcome-email-is-not-sent-when-new-customers-are-created"></a>Kynningartölvupóstur er ekki sendur þegar nýir viðskiptavinir eru stofnaðir

[!include [banner](../../includes/banner.md)]

Þessi grein veitir leiðbeiningar um bilanaleit sem geta hjálpað ef velkomin tölvupósttilkynning er ekki send þegar nýr viðskiptavinur er búinn til í Microsoft Dynamics 365 Commerce.

## <a name="description"></a>Lýsing

Þegar nýr viðskiptavinur er stofnaður í höfuðstöðvum Commerce er velkominn tölvupóstur ekki sendur til viðskiptavinarins, jafnvel þó að tölvupósttilkynning sé stillt fyrir **Viðskiptavinur búinn til** gerð tölvupósts tilkynninga.

## <a name="resolution"></a>Upplausn

### <a name="set-the-correct-email-id-value-for-the-customer-created-email-notification-type"></a>Stilltu rétt tölvupóstauðkennisgildi fyrir tegundina Tilkynningatilkynninga í tölvupósti til viðskiptavinar

Til að stilla rétt **Netfang** gildi fyrir **Viðskiptavinur búinn til** tegund tölvupósttilkynningar í höfuðstöðvum, fylgdu þessum skrefum.

1. Fara til **Verslun og verslun \> Uppsetning höfuðstöðva \> Tilkynningaprófíl fyrir viðskiptapóst**.
1. Í vinstri yfirlitsrúðunni skaltu velja tölvupósttilkynningarsniðið.
1. Undir **Stillingar smásöluviðburðatilkynninga**, fyrir **Viðskiptavinur búinn til** tegund tölvupósts tilkynninga, stilltu **Netfang** sviði til **NewCust**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Setja upp forstillingu tilkynningar í tölvupósti](../email-notification-profiles.md)
