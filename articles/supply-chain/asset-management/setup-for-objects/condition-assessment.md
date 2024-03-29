---
title: Ástandsmat
description: Í þessari grein er útskýrt hvernig búa á til sniðmát fyrir ástandsmat og skráningu á eign í Eignastýringu.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectCondition, EntAssetConditionTemplate
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c43424a0955d7a046186e8a4120c050990df6060
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015057"
---
# <a name="condition-assessment"></a>Ástandsmat

[!include [banner](../../includes/banner.md)]

 

Í þessari grein er útskýrt hvernig búa á til sniðmát fyrir ástandsmat og skráningu á eign í Eignastýringu. Ástandsmat er framkvæmt með reglulegu millibili og meginmarkmiðið er að búa til og viðhalda skilyrðum um eignir. Séð frá fyrirbyggjandi viðhaldssjónarmiði er mikilvægt að fylgjast með lykilupplýsingum eins og núverandi ástandi og endingartíma. Enn fremur, ef þú framkvæmir ástandsmat með reglulegu millibili, muntu geta fylgst með og borið saman aðstæður á vélum í verksmiðjunni.

Hægt er að nota ástandsmat til að mæla og hafa eftirlit með mörgum aðstæðum á búnaði þínum. Dæmi: Þú gætir mælt titring á vélunum þínum. Eftir að þú hefur skráð titringsmælingar í Eignastjórnun á ýmsum gerðum búnaðar geturðu leitað að nýjasta skráða matinu og skoðað titringsmælingar.

Skilyrðamat er búið til á eignir. Þú setur upp sniðmát fyrir mat á ástandi á eignategund áður en þú framkvæmir skilyrði fyrir mati á ástandi. Ástæðan fyrir því að nota sniðmát til ástandsmats er að forðast breytileika á gögnum um svipaðar eignir. Röðin til að setja upp og nota ástandsmat í eignastjórnun er: Fyrst setur þú upp nauðsynleg skilyrði fyrir mat á ástandi. Næst tengir þú sniðmát við eignategundir í forminu **Gerðir eigna**. Að lokum geturðu búið til skráningar á matsástandi á eign í forminu **Eignir**.

## <a name="create-a-condition-assessment-template"></a>Búðu til sniðmát fyrir ástandsmat

1. Veldu **Eignastýring** > **Uppsetning** > **Eignagerðir** > **Ástandsmat**.
2. Veldu **Nýtt** til að stofna nýtt sniðmát.
3. Settu inn auðkenni fyrir sniðmátið í reitnum **Sniðmát**.
4. Í reitnum **Heiti** slærðu inn heiti fyrir sniðmátið.
5. Á flýtiflipann **Línur ástandsmats** bætirðu við línum sem krafist er fyrir ástandsmatið, þar með talið val á viðeigandi ástandsgerð og mælieining.
6. Á flýtiflipanum **Eignagerðir** bætirðu við eignagerðum sem ættu að nota sniðmátið fyrir ástandsmat.
7. Í reitunum **Línur** og **Eignagerðir** í hópnum **Upplýsingar** efst á skjánum muntu sjá fjölda matslína og eignagerða sem tengjast völdu sniðmáti fyrir ástandsmat.


## <a name="create-condition-assessment-registration-on-an-asset"></a>Búðu til skráningu á matsástandi á eign

1. Veldu **Eignastýring** > **Eignir** > **Allar eignir**.
2. Í listanum velurðu eignina sem þú vilt stofna skráningu ástandsmats fyrir.
3. Á flipanum **Almennt** er smellt á **Ástandsmat**.
4. Smelltu á **Nýtt** til að búa til nýja skráningu.
5. Veldu dagsetningu fyrir ástandsmatið í reitnum **Dagsetning**.
6. Veldu nafn starfsmannsins sem framkvæmdi matsskráninguna í reitnum **Starfskraftur**.
7. Í reitnum **Línur** sérðu fjölda matslína sem settar eru upp í ástandasmati.
8. Veldu sniðmát fyrir ástandsmatið í reitnum **Sniðmát**. Heiti sniðmátsins er sjálfkrafa sett inn í reitnum **Heiti** og tengdar skráningarlínur eru settar inn á flýtiflipann **Línur ástandsmats**.
9. Þú getur sett inn athugasemdir sem tengjast völdum ástandsmati á flýtiflipann **Athugasemdir**.
10. Fyrir hverja línu ástandsmats skal setja inn mælingargögn í reitinn **Gildi**.
11. Hægt er að segja inn athugasemd varðandi valda skráningarlínu á flýtiflipann **Línur ástandsmats** > reitnum **Athugasemdir**. Ef þú bætir athugasemd við línu, þá er gátreiturinn **Athugasemd** sjálfkrafa valinn.

Eftir að þú ert búinn að gera skráningu á ástandsmati á eign geturðu prentað skýrslu um ástandsmat.

>[!NOTE]
>Einnig er hægt að skrá ástandsmat á verkbeiðni (**Eignastýring** > **Verkbeiðnir** > **Allar verkbeiðnir** > **Ástandsmat** hnappur.)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]