---
title: Kynning á verkbeiðnum
description: Þetta efni veitir yfirlit yfir verkbeiðnir í eignastjórnun.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9483c50a15fca566b1f5e089297795bbbe09c042
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875722"
---
# <a name="introduction-to-work-orders"></a>Kynning á verkbeiðnum

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Verkbeiðnir eru notaðar til að stjórna, veita nauðsynlegar upplýsingar um og skrá notkun í viðhaldsvinnslum. Verkbeiðni getur innihaldið eitt eða fleiri verkbeiðnivinnslur og hægt er að tengja eina eða fleiri eignir við verkbeiðni. Hver verkbeiðnilína skilgreinir viðhaldsvinnslu sem er áætluð á eignina.

Hægt er að stofna verkbeiðnir sjálfvirkt eða handvirkt:

- Notaðu sjálfkrafa skjámyndina **Tímasetja viðhaldsáætlanir** fyrir dagatalsbyggðar viðhaldsáætlanir sem eru stilltar á „Stofna sjálfvirkt“.  

- Notaðu sjálfkrafa skjámyndina **Tímasetja viðhaldslotur** fyrir dagatalsbyggðar viðhaldslotur sem eru stilltar á „Stofna sjálfvirkt“.  

- Búðu til úr viðhaldsáætlun, sem getur verið fyrirbyggjandi viðhaldsvinnslur eða viðhaldsbeiðnir.  

- Stofnaðu verkbeiðni á handvirkan hátt.  

- Búðu til verkbeiðni úr **Allar viðhaldsbeiðnir** eða **Virkar viðhaldsbeiðnir** eða **Mínar viðhaldsbeiðnir á virkri staðsetningu**.

>[!NOTE]
>Verkbeiðnivinnslur sem tengjast sömu eign tengjast sama verkefnisauðkenni.

## <a name="all-work-orders"></a>Allar verkbeiðnir

Smelltu á **Eignastjórnun** > **Sameiginlegt** > **Verkbeiðnir** > **Allar verkbeiðnir** til að opna listann. **Allar verkbeiðnir** inniheldur lista yfir allar verkbeiðnir og sýnir nokkrar af þeim upplýsingum sem tengjast verkbeiðni.

![Mynd 1](media/01-work-orders.png)

- Smelltu á **Eignastjórnun** > **Sameiginlegt** > **Verkbeiðnir** > **Virkar verkbeiðnir** til að sjá lista yfir virkar verkbeiðnir.

- Smelltu á **Eignastjórnun** > **Sameiginlegt** > **Verkbeiðnir** > **Mínar viðhaldsbeiðnir á virkri staðsetningu** til að sjá lista yfir verkbeiðnivinnslur sem innihalda eignir settar upp á virkum staðsetningum sem þú tengist sem starfskraftur (sett upp í [Viðhaldsstarfsmenn og starfsmannahópar](../setup-for-objects/workers-and-worker-groups.md)).

- Á listanum **Allar verkbeiðnir** (hnitalínuyfirlit) smellirðu á tengil í dálkinum **Verkbeiðni** til að sýna yfirlit upplýsinga um valda skrá. Smelltu á hnappinn **Breyta** til að opna fyrir breytingar.  

- Í yfirlit upplýsinga sérðu ítarlegar upplýsingar sem tengjast verkbeiðninni.  

- Í yfirliti upplýsinga velurðu tengilinn **Línur** til að sjá vinnsluupplýsingar um verkbeiðnina eða velur tengilinn **Haus** til að sjá upplýsingar um verkbeiðni.  

- Lóðrétti glugginn **Tengdar upplýsingar** til hægri á skjánum inniheldur verkbeiðnitengdar upplýsingar til viðbótar. Stækkaðu rúðuna til að sjá tengdar upplýsingar fyrir valda verkbeiðni.  


![Mynd 2](media/02-work-orders.png)


Hnapparnir í aðgerðaglugganum eru skipulagðir á flipa í aðgerðaglugganum. Hér er stutt lýsing á hnöppunum sem tengjast Enterprise Asset Management:



| Heiti hnapps                     | Lýsing                                                                                                                                                                                                                                                             |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Breyta                            | Breyta valinni verkbeiðni.                                                                                                                                                                                                                                           |
| Nýjar                             | Stofna nýja verkbeiðni.                                                                                                                                                                                                                                                  |
| Eyða                          | Eyða valinni verkbeiðni.                                                                                                                                                                                                                                         |
| Verkbeiðnihópur                 | Bættu völdum verkbeiðnum við verkbeiðnasafn eða fjarlægðu úr verkbeiðnasafninu.                                                                                                                                                                                           |
| Leiðrétta                          | Aðlagaðu upplýsingar um áætlað upphaf og lok, þjónustustig, ábyrgan viðhaldsstarfsmann eða ábyrgan viðhaldsstarfsmannahóp á völdum verkbeiðnum.                                                                                                                                     |
| Tengd verkbeiðni              | Búðu til nýja verkbeiðni sem tengist völdum vinnslum verkbeiðni. Þetta er gagnlegt ef þú vilt skrá aðal- og annars flokks verkbeiðnir.                                                                                                                              |
| Afrita verkbeiðni                 | Búðu til nýja verkbeiðni byggða á fyrirliggjandi verkbeiðni.                                                                                                                                                                                                                |
| Viðburðarferill                   | Sjá skráningarsögu um verkbeiðnina.                                                                                                                                                                                                                |
| Athugasemdir verkbeiðni viðhaldsverks                           | Stofnaðu lýsingu eða settu inn minnispunkta eða athugasemdir við verkbeiðni. Byrjaðu á því að smella á hnappinn **Bæta tímastimpli við** til að bæta notandanafni þínu og tímastimpli við athugasemdina. Minnispunktar birtast á skjámyndinni **Verkbeiðni** > flýtiflipanum **Línuupplýsingar** > flipanum **Lýsing**. |
| Verkfæri                           | Stofnaðu lista yfir nauðsynleg verkfæri í verkbeiðni. Verkfæri eru sett upp sem tilföng í **Fyrirtækisstjórnun** > **Sameiginlegt** > **Tilföng** > **Tilföng**.                                                                                                      |
| Viðhaldsgátlisti           | Skoðaðu gátlista fyrir eignina sem er tengd verkbeiðninni.                                                                                                                                                                                                              |
| Bilun eignar                     | Skoðaðu eða skráðu villuupplýsingar um eign sem á að nota við bilanastjórnun.                                                                                                                                                                                        |
| Niðurtími vegna viðhalds            | Tilgreindu niðurtíma vegna viðhalds fyrir verkbeiðni.                                                                                                                                                                                                                               |
| Ástandsmat            | Skráðu ástandsmatsmælingar á verkbeiðnina.                                                                                                                                                                                                             |
| Eignateljarar                 | Stofnaðu eða skoðaðu teljaraskráningar á eignina.                                                                                                                                                                                                                     |
| Spá                        | Skoðaðu eða stofnaðu spár í verkbeiðni.                                                                                                                                                                                                                               |
| Færslubækur                        | Skoða eða búa til verkbeiðnibækur. Hægt er að afrita færslubókarlínur úr spám.                                                                                                                                                                                         |
| Verkfærslur            | Skoða öll bókuð viðskipti sem tengjast verkbeiðnum sem búnar eru til fyrir eignina.                                                                                                                                                                                             |
| Uppfæra stöðu verkbeiðni                | Uppfærðu líftímastöðu verkbeiðni.                                                                                                                                                                                                                                                |
| Kladdi líftímastöðu                       | Kladdi sem sýnir líftímastöðu valinnar verkbeiðni.                                                                                                                                                                                                                   |
| Eignaskjöl                | Skoða lista yfir skjöl sem fylgja eignum sem tengjast verkbeiðni. Þessi skjöl eru sett upp í **Eignastjórnun** > **Uppsetning** > **Eignaskjöl**.                                                                                                 |
| Áætlun                        | Tímaáætla valdar verkbeiðnir.                                                                                                                                                                                                                                      |
| Sending            | Tímasettu valda verkbeiðni fyrir einn starfsmann.                                                                                                                                                                                                                        |
| Eyða áætlun                 | Eyða tímastillingu fyrir valda verkbeiðni.                                                                                                                                                                                                                          |
| Áætlaðar verkbeiðnir viðhaldsvinnsla             | Opnaðu listasíðuna **Áætlaðar verkbeiðnir viðhaldsvinnsla**.                                                                                                                                                                                                                             |
| Innkaupabeiðni verkbeiðni | Opna listasíðuna **Innkaupabeiðni verkbeiðni**.                                                                                                                                                                                                                 |
| Innkaup verkbeiðni             | Opna listasíðuna **Innkaup verkbeiðni**.                                                                                                                                                                                                                             |
| Kostnaðarstýring                    | Berðu saman kostnaðaráætlun og raunkostnað verkbeiðninnar.                                                                                                                                                                                                                |
| Klukkustundastjórnun                    | Berðu saman spáða tíma og rauntíma verkbeiðninnar.                                                                                                                                                                                                                |
| Skýrsla verkbeiðni               | Prenta skýrslu verkbeiðni.                                                                                                                                                                                                                                                |
| Notkun verkbeiðni          | Prenta notkunarskýrslu.                                                                                                                                                                                                                                               |


Hnapparnir á flipanum **Verkbeiðni** > hópnum **Verk** tengjast virkni í einingunni **Verkefnisstjórnun og bókhald** varðandi spár, færslubækur og reikningsfærslur.

>[!NOTE]
>Spár sem eru búnar til í verkbeiðni geta verið með þegar röðun er keyrð með spárlíkaninu sem valið var í skjámyndinni **Færibreytur eignastýringar**.

