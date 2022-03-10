---
title: Viðhaldsstarfskraftar og starfskraftahópar
description: Þetta efni útskýrir viðhaldsstarfskrafta starfsmannahópa í eignastjórnun.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetWorkerGroupCopyFromResourceGroup, EntAssetWorkerGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1e976a28349a4bc7a371d23eb4df724e0ffd36a0553aec2deeb2ff07d0a63579
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6750125"
---
# <a name="maintenance-workers-and-worker-groups"></a>Viðhaldsstarfskraftar og starfskraftahópar

[!include [banner](../../includes/banner.md)]

 

Þetta efni útskýrir viðhaldsstarfskrafta starfsmannahópa í eignastjórnun. Í eignastjórnun geturðu tengt viðhaldsstarfsmenn við virka staði. (Sjá frekari upplýsingar um hagnýta staði [Stofna virkar staðsetningar](../functional-locations/create-functional-locations.md) .) Þessi virkni gæti verið gagnleg ef þú ert til dæmis að skipuleggja viðhaldsstörf á vél sem er staðsett á hagnýtum stað 01 og þú vilt úthluta viðhaldsstarfsmönnum frá sama stað til að framkvæma verkið.

Þú getur einnig búið til hópa starfsmanna viðhalds og tengt viðhald starfsmanna við þá. Þessi virkni er gagnleg þegar þú vinnur einfalda tímasetningu vinnu og þú vilt skipuleggja hóp viðhaldsstarfsmanna í vinnupöntun. Þú getur notað viðhaldsstarfsmenn og hópa viðhaldsstarfsmanna til að setja upp valinn viðhaldsstarfsmenn og ábyrga viðhaldsstarfsmenn. 


## <a name="create-workers"></a>Stofna starfskrafta

1. Veldu **Eignastýring** \> **Uppsetning** \> **Starfskraftar** \> **Starfskraftar**.
2. Veldu **Nýtt** til að bæta nýjum starfskrafti við listann.
3. Í retinum **starfskraftur** velurðu starfskraftinn.
4. Stilltu **Virkur** kostur á **Já** til að tímasetja starfsmanninn eftir verkbeiðnum.

    Á flýtiflipanum **Almennt** eru reitirnir **Tilföng** og **Lýsing** sjálfkrafa fylltir út ef tilföng hafa verið valin fyrir starfsmanninn. Reiturinn **Dagatal** er einnig sjálfkrafa fyllt út, að því tilskildu að þú hafir sett upp starfsmanninn sem auðlind og úthlutað dagatali til þess tilfanga á **Tilföng** síðu (**Fyrirtækjastjórnun** \> **Tilföng** \> **Tilföng**).

5. Á flýtiflipanum **Hópar** veldu **Bæta við**, og veldu síðan viðhald starfsmannahóps fyrir starfsmanninn. Starfskraftur getur tengst fleiri en einum hóp.
6. Í venjulegu skipulagi er tengsl starfsmanns við hóp gildi frá og með þeim degi þegar þú bætir við hópnum og hann rennur aldrei út. Þessi dagsetning er sýnd í reitnum **Virkt**. Til að sjá reitinn **Virkt** veldu **Útsýni** \> **Allt**. Ef tengsl starfsmanns við hóp ættu að takmarkast við ákveðið tímabil, notaðu **Árangursrík** og **Fyrning** reiti til að skilgreina tímabilið.
7. Á flýtiflipanum **Virkar staðsetningar** veldu **Bæta við**, og veldu síðan virka staðsetningu fyrir viðhaldsstarfsmanninn. Tilgreindu einnig hvaða staðsetning er aðal virkni staða starfsmannsins.

    > [!NOTE]
    > Þegar þú bætir starfsmanni við virkar stöðum birtast allar virkar eignir sem tengjast þessum virkni stöðum á ýmsum valmyndaratriðum, svo sem **Virku eignir mínar** og **Virku virku staðirnir mínir**. Þeir birtast einnig í eignaleitunum sem eru sýndar þegar þú býrð til nýja eign, viðhaldsbeiðni eða vverkbeiðni.

    Reitirnir á flýtiflipanum **Upplýsingar** sýna fjölda viðhaldsstarfsmannahópa og virka staði sem valinn viðhaldsstarfsmaður er tengdur.

## <a name="create-worker-groups"></a>Stofna strafskraftahópa

1. Veldu **Eignastýring** \> **Uppsetning** \> **Starfskraftar** \> **Hópar viðhaldsstarfsmanna**.
2. Veldu **Nýtt** til að bæta nýjum starfsmannahóp við listann.
3. Í **Hópur viðhaldsstarfsmanna** reitinn, sláðu inn kenni hópsins.
4. Færið inn lýsandi nafn í reitinn **Heiti**.
5. Á flýtiflipanum **Starfskraftar** veldu **Bæta við**, og veldu síðan viðhald starfsmannahóps fyrir starfsmannahópinn. Fyrir upplýsingar um **Árangursrík** og **Fyrning** reitir, sjá skref 6 í fyrri aðferð.
6. Ef tilfangahópur ætti að tengjast völdum hópi viðhaldsstarfsmanna skaltu velja **Afrita úr tilfangahóp**. Í **Hópur** reitinn, veldu auðlindahópinn sem á að afrita dagatalstillingar frá. Síðan, í **starfsmannahópur** veldu starfsmannahópinn sem á að afrita dagatalsstillingar auðlindahópsins til. Þetta skref skiptir aðeins máli ef þú vilt að viðhaldsstarfsmenn noti dagatalið sem er tengt auðlindinni (vinnumiðstöð) við tímasetningu vinnu.

    Reitirnir á flýtiflipanum **Upplýsingar** sýna fjölda viðhaldsstarfsmannahópa og virka staði sem valinn viðhaldsstarfsmaður er tengdur.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]