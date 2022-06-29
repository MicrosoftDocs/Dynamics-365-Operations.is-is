---
title: Setja upp eignir á virkum staðsetningum
description: Þessi grein útskýrir hvernig á að setja upp eignir á virkum stöðum í eignastýringu.
author: johanhoffmann
ms.date: 06/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationObjectChange, EntAssetFunctionalLocationObjectInstall, EntAssetFunctionalLocationObject
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3ae571f4ad7210b31d212b0472610b36dc5c488b
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016073"
---
# <a name="install-assets-on-functional-locations"></a>Setja upp eignir á virkum staðsetningum

[!include [banner](../../includes/banner.md)]

 

Eftir að þú hefur búið til skipulag virkra staðsetninga er næsta skref að setja upp eignir á viðkomandi virkum staðsetningum. Þessi grein útskýrir hvernig á að setja upp eignir á þessum virkum stöðum í eignastýringu. Nánari upplýsingar um hvernig stofna eigi aðallykla, sjá [Kynning á eignum](../objects/introduction-to-objects.md).

Ef þú hefur búið til eignaskipulag verður að setja upp alla eignaskipan á virka staðsetningu. Þess vegna er aðeins hægt að velja yfireignir (efstu eignir sem hafa enga yfireign) á virkri staðsetnigu. Allar tengdar undireignir (undireignir) verða einnig settar upp á virkri staðsetningu. Þegar þú setur upp eignir á virkri staðsetningu, gætu fjárhagsvíddir virkrar staðsetningar verið fluttar sjálfkrafa yfir á þær, allt eftir uppsetningu á gerð virkrar staðsetningar sem er valin fyrir virka staðsetningu. Nánari upplýsingar um hvernig setja skal upp gerðir virkra staðsetinga er að finna í [Gerðir virkra staðsetninga](../setup-for-functional-locations/functional-location-types.md).

> [!NOTE]
> Þú getur sett upp eignategundir á gerð virkrar staðsetningar sem er notuð fyrir virka staðsetningu. Í þessu tilfelli, þegar þú setur upp eignir á virkri staðsetningu eru aðeins yfireignir sem eru með sömu eignategund sýndar á listanum yfir eignir sem hægt er að setja upp á virkri staðsetningu.

Eftir að þú hefur sett upp eignir á virkri staðsetningu geturðu skipt út yfireign eða eignaskipulagi eins og þú þarft. Eins og þegar þú setur upp eignir velurðu yfireign sem á að skipta um. Einnig verður skipt út öllum tengdum undireignum. 


## <a name="install-an-asset-structure-on-a-functional-location"></a>Settu upp eignaskipulag á virkri staðsetningu

1. Veldu **Eignastýring** \> **Virkir staðir** \> **Allir virkir staðir** eða **Virkir virkir staðir**.
2. Veldu virka staðsetningu til að setja upp eign á.
3. Velja **Setja upp eign**.

    Hlutinn **Eigindir** sýnir lista yfir eigindakröfur sem eru settar upp á gerð virkrar staðsetningar sem er valin fyrir virka staðsetningu. Egindirnar eru eingöngu ætlað til upplýsinga. Kerfið staðfestir ekki eigindirnar gagnvart eignareigindunum sem eru settir upp á eigninni sem þú ert að setja upp. Þú verður að gera þá staðfestingu eftir að þú hefur valið eign í reitnum **Eignir**.

4. Í reitnum **Eignir** veldu yfireignina sem á að setja upp. Allar tengdar undireignir fylgja sjálfkrafa með uppsetningunni.

    Hlutinn **Eigindir eigna** til hægri á eignalistanum sýnir eignareigindirnar sem tengjast völdum eigninni.

5. Í reitnum **Virkt**, veldu dagsetningu og tíma sem eignauppsetningin gildir frá. Eftir þann dag og tíma mun kostnaður vegna eignarinnar og tengdar undireignir tengjast virkni staðsetningunni.

    > [!NOTE]
    > Eignaeigindunum sem eru settar upp á eigninni er bætt við hlutann **Eigindir**. Til dæmis, eigindakröfunni **Þyngd** hefur verið bætt við sem krafa bæði á eignina og virkri staðsetningu. Ef eignin hefur eigindakröfur af sömu gerð og virk staðsetningin, eru gildi eigindaskilyrða eignarinnar færð inn í reitnum **Gildi**. Þess vegna getur þú staðfest eignaverðin gagnvart eiginleikakröfunum sem settar eru upp á virkri staðsetningu. Eigindakröfur sem settar eru upp á virkni staðsetningunni eru merktar með hakmerki.

6. Veljið **Í lagi**.

    > [!NOTE]
    > Fylgdu skrefum 1 til 6 í þessu ferli til að breyta uppsetningu á eign með því að setja hana upp á nýjan virkan stað. Þegar þú setur upp eign á nýjan virkan stað er eignin sjálfkrafa fjarlægð frá fyrri virkni stað. Allar virkar viðhaldsbeiðnir eða vinnupantanir sem voru búnar til á eigninni áður en þú settir hana upp á nýjan virkan stað er **ekki** sjálfkrafa flutt á nýja virkni stað. Ef þessar viðhaldsbeiðnir og verkbeiðnir eru enn nauðsynlegar fyrir eignina, verður þú að búa þær til handvirkt eftir að eignin er sett upp á nýjum stað.

7. Til að skoða lista yfir allar eignir, þar á meðal undireignir, sem eru settar upp á starfræna staðsetningu, velurðu virkni staðsetningu á síðunni **Allar virkar staðsetningar** og veldu síðan **Eignir**.
8. Til að skoða lista yfir virkar viðhaldsbeiðnir, virkar verkbeiðnir eða bilanaskráningar sem tengjast eignunum sem eru settar upp á virkri staðsetningu skaltu velja virku staðsetninguna á síðunni **Allar virkar staðsetningar** og veldu síðan **Beiðnir**, **Verkbeiðnir**, eða **Bilanir**.

> [!NOTE]
> Þegar eignatengdum gögnum er breytt eru þau uppfærð sjálfkrafa á virkri staðsetningu sem eignin er sett upp á. Þessi sjálfvirka uppfærsla lýtur að breytingum á viðhaldsbeiðnum, verkbeiðnum, skráningum á eignabilunum, skráningum á niðurtíma vegna viðhalds og skráningum eignamælinga.

## <a name="automatically-create-one-asset-on-a-functional-location"></a>Búðu til sjálfkrafa eina eign á virkum stað

Þú getur sett upp stig virkrar staðsetningar og gerðir virkra staðsetninga til að meðhöndla sjálfvirka stofnun *einnar* eignar á virkum stað. Eignin fær sama kenni og heiti og virka staðsetningin. Þessi virkni gæti verið gagnleg þegar þú ert að sjá um viðhald á stórum, kyrrstæðum eignum, svo sem byggingu.

Áður en þú getur sjálfkrafa stofnað eign á virkri staðsetningu verða eftirfarandi uppsetningargögn að vera tiltæk:

- Stofnaðu gerð virkrar staðsetningar til að meðhöndla sjálfvirka stofnun eignar. Í **Tegund eigna** reit, veldu eignategund. Sjá [Gerðir virkra staðsetninga](../setup-for-functional-locations/functional-location-types.md) til að fá nánari upplýsingar um staðsetningarleiðbeiningar.
- Stofnaðu lítítmastöðu virkrar staðsetningar til að meðhöndla sjálfvirka stofnun eignar. Stillið valkostinn **Stofna eign** á **Já**. Sjá [Líftímastöður virkra staðsetninga](../setup-for-functional-locations/functional-location-stages.md) til að fá nánari upplýsingar um staðsetningarleiðbeiningar.

Eftir að uppsetningargögnin eru tiltæk ertu tilbúinn að búa til eign.

1. Á síðunni **Allar virkar staðsetningar**, vertu viss um að virka staðsetningin þar sem þú vilt að eignin verði sjálfkrafa búin til noti þá gerð virkrar staðsetningar sem þú bjóst til í þessu skyni.
2. Velja virka staðsetningu á listanum.
3. Veldu **Uppfærðu stöðu virkrar staðsetningar**, og veldu síðan líftímastöðuna sem þú bjóst til í þessum tilgangi. Ein eign er nú sjálfkrafa sett upp á virkri staðsetningu. Þessi eign er með sama kenni og heiti og virka staðsetningin.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]