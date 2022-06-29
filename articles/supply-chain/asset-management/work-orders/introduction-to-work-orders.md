---
title: Kynning á verkbeiðnum
description: Þessi grein veitir yfirlit yfir verkbeiðnir í eignastýringu.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderLineNote, EntAssetWorkOrderTable, EntAssetWorkOrderActive, EntAssetWorkOrderHoursInfoPart, EntAssetWorkOrderLineListPage, EntAssetWorkOrderAddObjectBOMItem, EntAssetWorkOrderTablePoolAdd, EntAssetWorkOrderPurchReqListPagePreviewPane, EntAssetWorkOrderPoolReferenceAdd, EntAssetWorkOrderWorkspace, EntAssetWorkOrderTableAdjust, EntAssetWorkOrderGantt, EntAssetWorkOrderNotes, EntAssetWorkOrderActivePart, EntAssetWorkOrderTableInfoPart, EntAssetWorkOrderLineListPagePreviewPane, EntAssetWorkOrderTool, EntAssetMobileWorkOrderLineDetails, EntAssetMobileWorkOrderLineList, EntAssetMobileWorkOrderDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5eb911ec4ba9655c4ecaea3bf9a4f8736fa036c2
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016711"
---
# <a name="introduction-to-work-orders"></a>Kynning á verkbeiðnum

[!include [banner](../../includes/banner.md)]



Verkbeiðnir eru notaðar til að stjórna viðhaldsverkum, veita nauðsynlegar upplýsingar um þau og skrá notkun í þau. Hver verkbeiðni getur innihaldið eitt eða fleiri verkbeiðnivinnslur og hægt er að tengja eina eða fleiri eignir við hverja verkbeiðni. Hver verkbeiðnivinnsla skilgreinir viðhaldsverk sem er áætlað á eignina.

Hægt er að búa til verkbeiðnir á eftirfarandi hátt:

- Fyrir viðhaldsverk sem byggjast á almanaki þar sem kveikt er á stillingunni „Stofna sjálfvirkt“ sjálfkrafa með því að nota [Áætla viðhaldsáætlanir](../preventive-and-reactive-maintenance/schedule-maintenance-plans.md).

- Fyrir viðhaldslotur sem byggjast á almanaki þar sem kveikt er á stillingunni „Stofna sjálfvirkt“ sjálfkrafa með því að nota [Áætla viðhaldslotur](../preventive-and-reactive-maintenance/maintenance-rounds.md).

- Fyrir fyrirbyggjandi viðhaldssverk eða viðhaldsbeiðnir úr [Viðhaldsskema](../preventive-and-reactive-maintenance/maintenance-schedule.md).

- Handvirkt

- Af síðunni **Allar viðhaldsbeiðnir**, **Virkar viðhaldsbeiðnir** eða **Mínar viðhaldsbeiðnir á virkri staðsetningu**.

>[!NOTE]
>Verkbeiðnivinnslur sem tengjast sömu eign tengjast sama verkefnisauðkenni.

## <a name="all-work-orders"></a>Allar verkbeiðnir

Veldu **Eignastýring** > **Verkbeiðnir** > **Allar vinnupantanir** að opna **Allar vinnupantanir** listasíðu. Þessi síða sýnir allar verkbeiðnir og nokkrar af þeim upplýsingum sem tengjast hverri.

Myndin hér að neðan sýnir dæmi um listasíðuna **Allar verkbeiðnir**.

![Mynd 1.](media/01-work-orders.png)

Til að skoða lista yfir aðeins virkar vinnupantanir skaltu velja **Eignastýring** > **Verkbeiðnir** > **Virkar vinnupantanir**. 

Til að skoða lista yfir verkbeiðniverk sem innihalda eignir sem eru settar upp á virkum stöðum sem þú tengist sem starfsmaður skaltu velja **Eignastýring** > **Verkbeiðnir** > **Viðhaldsstörfin mín fyrir starfræna staðsetningu verkbeiðni**. (Samband starfskrafta og virkra staðsetninga er sett upp á síðunni **Starfskraftar**. Sjá frekari upplýsingar [Viðhaldsstarfsmenn og starfsmannahópar](../setup-for-objects/workers-and-worker-groups.md).)

Hér eru nokkrar leiðir sem hægt er að nota síðuna **Allar verkbeiðnir**:

- Í hnitalínuyfirlitinu velurðu tengil í dálknum **Verkbeiðni** til að sýna upplýsingasýn fyrir valda skrá. Þú getur síðan valið **Breyta** til að opna skrána fyrir breytingar.

- Í yfirliti upplýsinga skoðarðu ítarlegar upplýsingar sem tengjast verkbeiðninni.  

- Í yfirliti upplýsinga velurðu flipann **Línur** til að skoða upplýsingar um verkbeiðnivinnsluna eða velur flipann **Haus** til að skoða upplýsingar um verkbeiðni.  

- Stækkaðu gluggann **Tengdar upplýsingar** hægra megin á síðunni til að skoða viðbótarupplýsingar sem tengjast valinni verkbeiðni.

Myndin hér að neðan sýnir dæmi um upplýsingayfirlitið **Allar verkbeiðnir**.

![Mynd 2.](media/02-work-orders.png)


Hnapparnir á aðgerðarglugganum eru skipulagðir á flipa. Eftirfarandi tafla lýsir stuttlega hnöppunum sem tengjast eignastýringu:



| Heiti hnapps                     | Lýsing                                                                                                                                                                                                                                                             |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Breyta                            | Breyta valinni verkbeiðni.                                                                                                                                                                                                                                           |
| Nýjar                             | Stofna nýja verkbeiðni.                                                                                                                                                                                                                                                  |
| Eyða                          | Eyða valinni verkbeiðni.                                                                                                                                                                                                                                         |
| Verkbeiðnihópur                 | Bættu valinni verkbeiðni við verkbeiðnasafn eða fjarlægðu hana úr verkbeiðnasafninu.                                                                                                                                                                                           |
| Leiðrétta                          | Aðlagaðu upplýsingar um áætlað upphaf og lok, þjónustustig, ábyrgan viðhaldsstarfsmann eða ábyrgan viðhaldsstarfsmannahóp á völdum verkbeiðnum.                                                                                                                                     |
| Tengd verkbeiðni              | Búðu til nýja verkbeiðni sem tengist völdum vinnslum verkbeiðni. Þetta er gagnlegt ef þú vilt skrá aðal- og annars flokks verkbeiðnir.                                                                                                                              |
| Afrita verkbeiðni                 | Búðu til nýja verkbeiðni sem byggist á fyrirliggjandi verkbeiðni.                                                                                                                                                                                                               |
| Viðburðarferill                   | Skoðaðu skránigarsögu fyrir verkbeiðnina.                                                                                                                                                                                                                |
| Athugasemdir fyrir verkbeiðni viðhaldsverks                           | Stofnaðu lýsingu á verkbeiðni eða settu inn minnispunkta eða athugasemdir við hana. Fyrst velurðu **Bæta tímastimpli við** til að bæta notandanafni þínu og tímastimpli við athugasemdina. Skýringar eru sýndar á flipanum **Lýsing** á flýtiflipanum **Línulýsing** af síðunni **Verkbeiðni**.         |
| Verkfæri                           | Stofnaðu lista yfir nauðsynleg verkfæri í verkbeiðni. Verkfæri eru sett upp sem tilföng í **Fyrirtækisstjórnun** > **Tilföng** > **Tilföng**.                                                                                                      |
| Viðhaldsgátlisti           | Skoðaðu gátlistann fyrir eignina sem er tengd verkbeiðninni.                                                                                                                                                                                                              |
| Bilun eignar                     | Skoða eða skrá bilunarupplýsingar um eign. Þessar upplýsingar eru notaðar fyrir bilanastýringu.                                                                                                                                                                                      |
| Niðurtími vegna viðhalds            | Tilgreindu niðurtíma vegna viðhalds fyrir verkbeiðni.                                                                                                                                                                                                                               |
| Ástandsmat            | Skráðu ástandsmatsmælingar á verkbeiðnina.                                                                                                                                                                                                             |
| Eignateljarar                 | Stofnaðu eða skoðaðu teljaraskráningar á eignina.                                                                                                                                                                                                                     |
| Spá                        | Skoðaðu eða stofnaðu spár í verkbeiðni.                                                                                                                                                                                                                               |
| Færslubækur                        | Skoða eða búa til verkbeiðnibækur. Hægt er að afrita færslubókarlínur úr spám.                                                                                                                                                                                         |
| Verkfærslur            | Skoða öll bókuð viðskipti sem tengjast verkbeiðnum sem búnar eru til fyrir eignina.                                                                                                                                                                                             |
| Uppfæra stöðu verkbeiðni           | Uppfærðu líftímastöðu verkbeiðninnar.                                                                                                                                                                                                                                                |
| Kladdi líftímastöðu                      | Skoða kladdaskrá sem sýnir líftímastöður valinnar verkbeiðni.                                                                                                                                                                                                                   |
| Eignaskjöl                | Skoða lista yfir skjöl sem fylgja eignum sem tengjast verkbeiðni. Þessi skjöl eru sett upp í **Eignastjórnun** > **Uppsetning** > **Eignaskjöl**.                                                                                                 |
| Áætlun                        | Tímaáætla valdar verkbeiðnir.                                                                                                                                                                                                                                      |
| Sending            | Tímasettu valda verkbeiðni fyrir einn starfsmann.                                                                                                                                                                                                                        |
| Eyða áætlun                 | Eyða tímastillingu fyrir valda verkbeiðni.                                                                                                                                                                                                                          |
| Áætlaðar verkbeiðnir viðhaldsverka             | Opnaðu listasíðuna **Áætlaðar verkbeiðnir viðhaldsvinnsla**.                                                                                                                                                                                                                             |
| Innkaupabeiðni verkbeiðni | Opna listasíðuna **Innkaupabeiðni verkbeiðni**.                                                                                                                                                                                                                 |
| Innkaup verkbeiðni             | Opna listasíðuna **Innkaup verkbeiðni**.                                                                                                                                                                                                                             |
| Kostnaðarstýring                    | Berðu saman kostnaðaráætlun og raunkostnað verkbeiðninnar.                                                                                                                                                                                                                |
| Klukkustundastjórnun                    | Berðu saman spáða tíma og rauntíma verkbeiðninnar.                                                                                                                                                                                                                |
| Skýrsla verkbeiðni               | Prenta skýrslu verkbeiðni.                                                                                                                                                                                                                                                |
| Notkun verkbeiðni          | Prenta notkunarskýrslu.                                                                                                                                                                                                                                               |


Hnapparnir í hópnum **Verk** á flipanum **Verkbeiðni** í aðgerðaglugganum tengjast virkni fyrir spár, færslubækur og reikningsfærslur í kerfiseiningunni **Verkefnastjórnun og bókhald**.

>[!NOTE]
>Til að hafa spár með sem voru stofnaðar í verkbeiðni þegar röðun er keyrð skaltu nota spárlíkanið sem valið var á síðunni **Færibreytur eignastýringar**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]