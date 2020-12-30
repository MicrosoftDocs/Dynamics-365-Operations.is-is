---
title: Kynning á virkum staðsetningum
description: Þetta efni veitir yfirlit yfir virkar staðsetningar í eignastýringu.
author: josaw1
manager: tfehr
ms.date: 06/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationEditSubLocations, EntAssetFunctionalLocationLookup, EntAssetFunctionalLocationRename, EntAssetFunctionalLocation
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 80ea318d750f1ef18f270fa246ab54ecb63aa790
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430222"
---
# <a name="introduction-to-functional-locations"></a>Kynning á virkum staðsetningum

[!include [banner](../../includes/banner.md)]

 

Þetta efni veitir yfirlit yfir virkar staðsetningar í eignastýringu. Virkar staðsetningar eru þættir í tæknilegri uppbyggingu, svo sem virkar einingar í kerfi. Virkar staðsetningar eru búnar til með stigveldi og þú setur upp eignir á þeim. Uppsetning virkra staðsetninga í fyrirtækinu þínu fer eftir kröfum fyrirtækisins.

Hér eru nokkur dæmi um hvernig þú getur notað virkar staðsetningar:

- **Virkt** - Virkar staðsetningar geta verið notendamiðaðar og notuð til að stjórna eignum sem hafa svipaða hegðun.
- **Ferlistengt** - Virkar staðsetningar geta verið verkflæðisbundnar.
- **Rúmfræðilegt** - Virkar staðsetningar geta táknað landfræðilega staðsetningu eða staði.

Hverri virkri staðsetningu er stjórnað sjálfstætt í eignastjórnun. Hér eru sumar nytsamlegar aðgerðir virkra staðsetninga:

- Settu upp forskriftir um virkni staðsetningar.
- Settu upp kröfur um eignaupplýsingar.
- Settu upp viðhaldsraðir til fyrirbyggjandi og viðbragðs viðhalds.
- Stýra uppsettar eignum.
- Fylgstu með virkum beiðnum og verkbeiðnum sem tengjast uppsettum eignum.
- Rektu galla sem eru skráðir á eignir.
- Fylgstu með viðhaldskostnaði á eignunum sem tengjast virkri staðsetningu á hverjum tíma.

Virkar staðsetningar veita rekjanleika eigna í tengslum við beiðnir, verkbeiðnir, bilanaskráningar, ástandsmat, framleiðslu stöðvunarskráninga og skráningar eignateljara.

> [!NOTE]
> Jafnvel þó eign sé sett upp á ýmsum virkum staðsetningum á lífstímas sínum getur kostnaðurinn tengst hverjum stað. Með öðrum orðum, er eignakostnaður alltaf tengdur virku staðsetningunni sem eignin var sett upp á á hverjum tíma.

Virkar staðsetningar eru **ekki** sveigjanlegar. Þess vegna, eftir að þú hefur sett upp virkt staðsetningarstigveldi, geturðu ekki flutt staðsetningu í því. 

Eftir að þú hefur búið til virka staðsetningarveldi er næsta skref að setja upp eignir á það. Nánari upplýsingar er að finna í [Setja upp eignir á virkum staðsetningum](../functional-locations/install-objects-on-functional-locations.md).

## <a name="all-functional-locations"></a>Allar virkar staðsetningar

Veldu **Eignastýring** \> **Sameiginlegt** \> **Virkar staðsetningar** \> **Allar virkar staðsetningar** til að opna listasíðuna **Allar virkar staðsetningar**. Þessi síða sýnir allar virkar staðsetningar og nokkrar af þeim upplýsingum sem tengjast hverri. Til að skoða aðeins virkar virkar staðsetningar skaltu velja **Virkar virkar staðsetningar**. Til að skoða aðeins þær virku staðsetningar sem þú tengist sem starfskraftur skaltu velja **Mínar virku virku staðsetningar**. (Þessi tengsl eru sett upp á síðunni **Starfskraftar**. Sjá frekari upplýsingar [Viðhaldsstarfsmenn og starfsmannahópar](../setup-for-objects/workers-and-worker-groups.md).)

Á listasíðunni **Allar virkar staðsetningar** velurðu tengil í dálkinum **Virk staðsetning** til að skoða upplýsingar um valinn skrá. Til að breyta virkri staðsetningu skaltu velja hnappinn **Breyta**. Í smáatriðinu eru ítarlegar upplýsingar sem tengjast staðsetningu. Það felur einnig í sér gluggann **Tengdar upplýsingar** til hægri. Þessi gluggi sýnir stigveldi virkrar staðsetningarinnar. Þú getur stækkað og fellt saman gluggann **Tengdar upplýsingar**.

Hnapparnir á aðgerðarglugganum eru skipulagðir á flipa. Eftirfarandi tafla lýsir stuttlega hnöppunum sem tengjast eignastýringu.

| Heiti hnapps                         | Lýsing                                                                                                                                  |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Breyta                                | Skiptu á milli breytingastillinga og skoðunarstillinga fyrir síðuna.                                                                                         |
| Nýjar                                 | Búa til nýja virka staðsetningu.                                                                                                            |
| Eyða                              | Eyða valinni virkri staðsetningu.                                                                                                     |
| Endurnefna                              | Endurnefna valda virka staðsetningu.                                                                                                     |
| Afrita skipulag virkrar staðsetningar  | Afritaðu stigveldi virkrar staðsetningar.                                                                                                      |
| Settu upp eign                       | Settu upp eign, þ.mt undireignir, á virkri staðsetningu.                                                                        |
| Skipta út eign                       | Skiptu út eignastigveldi með öðru eignastigveldi á virkni staðsetningunni.                                                         |
| Kostnaðarstýring                        | Opnaðu síðuna **Virk staðsetningarkostnaðarstýring** þar sem þú getur gert kostnaðarútreikning fyrir valinn virkan stað.                |
| Klukkustundastjórnun                        | Opnaðu síðuna **Virk staðsetningarklukkustundarstýring** þar sem þú getur gert kostnaðarútreikning fyrir valinn virkan stað.                |
| Eignir                              | Opnaðu síðuna **Allar eignir** þar sem þú getur skoðað lista yfir eignir sem tengjast valinni virkri staðsetningu.                      |
| Beiðnir                            | Opnaðu síðuna **Virkar eignir** þar sem þú getur skoðað lista yfir beiðnir sem tengjast valinni virkri staðsetningu.               |
| Verkbeiðnir                         | Opnaðu síðuna **Virkar verkbeiðnir** þar sem þú getur skoðað lista yfir verkbeiðnir sem tengjast valinni virkri staðsetningu.         |
| Bilanir                              | Opnaðu síðuna **Eignabilanir** þar sem þú getur skoðað lista yfir skráningar á eignabilunum sem tengjast valinni virkri staðsetningu. |
| Uppfæra stöðu virkrar staðsetningar    | Uppfæra stig valinnar virkrar staðsetningar.                                                                                        |
| Kladdi líftímastöðu                 | Skoðaðu notkunarskrá sem sýnir stig valinnar virkrar staðsetningar.                                                                        |
