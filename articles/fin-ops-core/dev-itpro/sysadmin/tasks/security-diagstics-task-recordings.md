---
title: Öryggisgreining fyrir verkskráningu
description: Þessi grein veitir upplýsingar um hvernig á að greina og stjórna kröfum um öryggisheimildir byggðar á verkskráningu.
author: Peakerbl
ms.date: 05/05/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: ''
ms.dyn365.ops.version: Version 10.0.9
ms.openlocfilehash: cb69bf997100f25cd0ad2b7e34139857199e5d00
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880168"
---
# <a name="security-diagnostics-for-task-recordings"></a>Öryggisgreining fyrir verkskráningu

[!include [banner](../../includes/banner.md)]

## <a name="before-you-begin"></a>Áður en hafist er handa

Þessi grein veitir upplýsingar um hvernig á að greina og stjórna kröfum um öryggisheimildir byggðar á verkskráningu. Áður en þú klárar skrefin í þessari grein verður þú að hafa verkskráningu á viðskiptaferlinu sem þú vilt greina. Upplýsingar um hvernig viðskiptaferli er skráð er að finna í [Tilföng verkskráningar](../../user-interface/task-recorder.md). 

## <a name="manage-security-for-a-task-recording"></a>Stjórna öryggi fyrir verkskráningu

1. Farðu í **Kerfisstjórnun** > **Öryggi** > **Öryggisgreining fyrir verkskráningu**.
2. Opna verkskráningu úr staðsetningu sinni. Veldu **Opna í þessari tölvu** eða **Opna í Lifecycle Services** og veldu **Loka**.
3. Þetta opnar síðuna **Upplýsingar um öryggisvalmyndaratriði** þar sem finna má listi yfir öryggishluti sem eru nauðsynlegir fyrir ferlið.

 > [!NOTE]
 > Valmyndaratriðin **Aðgerð** og **Úttak** eru ekki á listanum.

4. Í reitinn **Notandakenni** skal velja notanda. Ef notandinn hefur ekki heimild fyrir sum valmyndaratriði mun reiturinn **Vantar heimildir** uppfærast í **Já**.
  
  ![Upplýsingasíða um öryggisvalmyndaratriði.](../media/Security-Menu-Item-Details.png)

5. Veljið **Bæta við tilvísun** til að sjá lista yfir öryggishlutina, þar á meðal hlutverk, skyldur og réttindi sem veita heimildina sem vantar.
6. Velja öryggishlut af listanum:

    - Ef **Hlutverk** er valið skal velja **Bæta hlutverkum við notanda**. Þetta mun opna síðuna **Úthluta notendum á hlutverk**. Frekari upplýsingar má finna á síðunni [Úthluta notendum á öryggishlutverk](assign-users-security-roles.md).
    - Ef **Skylda** er valið skal velja **Bæta skyldu við hlutverk**, velja hlutverkin sem bæta á skyldunni við og velja svo **Í lagi**.
    - Ef **Réttindi** eru valin skal velja **Bæta réttindum við skyldur**, velja hlutverk sem bæta á skyldunni við og velja svo **Í lagi**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]