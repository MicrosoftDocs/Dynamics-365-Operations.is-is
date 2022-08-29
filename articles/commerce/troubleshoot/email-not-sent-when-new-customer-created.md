---
title: Kynningartölvupóstur er ekki sendur þegar nýir viðskiptavinir eru stofnaðir
description: Þessi grein veitir leiðbeiningar um bilanaleit sem geta hjálpað ef velkomin tölvupósttilkynning er ekki send þegar nýr viðskiptavinur er búinn til í Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 08/01/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: 5aa7d864555f96194500989e2d7ad200d8892121
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/02/2022
ms.locfileid: "9219405"
---
# <a name="welcome-email-isnt-sent-when-new-customers-are-created"></a>Velkominn tölvupóstur er ekki sendur þegar nýir viðskiptavinir eru búnir til

[!include [banner](../../includes/banner.md)]

Þessi grein veitir leiðbeiningar um bilanaleit sem geta hjálpað ef velkomin tölvupósttilkynning er ekki send þegar nýr viðskiptavinur er búinn til í Microsoft Dynamics 365 Commerce.

## <a name="description"></a>Lýsing

Þegar nýr viðskiptavinur er stofnaður í höfuðstöðvum Commerce er velkominn tölvupóstur ekki sendur til viðskiptavinarins, jafnvel þó að tölvupósttilkynning sé stillt fyrir **Viðskiptavinur búinn til** gerð tölvupósts tilkynninga.

## <a name="resolution"></a>Upplausn

### <a name="associate-an-email-notification-profile-under-commerce-parameters"></a>Tengdu tilkynningasnið í tölvupósti undir Viðskiptafæribreytur

1. Í höfuðstöðvunum, farðu til **Verslun og verslun \> Uppsetning höfuðstöðva \> Færibreytur \> Viðskiptabreytur \> Almennt**.
2. Í **Tilkynningarprófíll í tölvupósti** fellilistanum, veldu tölvupósttilkynningarsniðið sem inniheldur kortlagningu á milli tilkynningagerðar sem viðskiptavinur hefur búið til og tölvupóstsniðmáts sem búið er til viðskiptavinar.  

> [!NOTE] 
> Þegar þú virkjar tilkynningar búnar til viðskiptavina munu viðskiptavinir sem eru búnir til í öllum rásum innan lögaðilans fá tölvupóst sem búinn er til viðskiptavinar. Eins og er er ekki hægt að takmarka tilkynningar sem viðskiptavinir hafa búið til við eina rás.

Fyrir frekari upplýsingar, sjá [Búðu til tölvupóstsniðmát fyrir viðskiptaviðburði](../email-templates-transactions.md). 

## <a name="additional-resources"></a>Frekari upplýsingar

[Setja upp forstillingu tilkynningar í tölvupósti](../email-notification-profiles.md)
