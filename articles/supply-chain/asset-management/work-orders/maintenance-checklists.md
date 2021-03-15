---
title: Viðhaldsgátlistar
description: Þetta efni lýsir viðhaldsgátlistum í eignastýringu.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderChecklist, EntAssetMobileWorkOrderLineChecklistDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b2ec7130fbe8c397c30cdc2a76f34ecfdfdc0737
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/16/2021
ms.locfileid: "5017919"
---
# <a name="maintenance-checklists"></a>Viðhaldsgátlistar

[!include [banner](../../includes/banner.md)]



Viðhaldsgátlistar eru settir upp á tegundum viðhaldsverka. Þú fyllir út viðhaldsgátlista sem hluti af ferlinu við að ljúka verkbeiðni. Nánari upplýsingar um hvernig skuli setja upp viðhaldsgátlista á gerðum viðhaldsverka á síðunni **Sjálfgefin tegund viðhaldsverka** skaltu skoða [Tegundaflokkar viðhaldsverka og gerðir viðhaldsverka, gerðaafbrigði viðhaldsverka, viðskipti með viðhaldsverk og viðhaldsgátlistar](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).

Þegar þú vinnur með viðhaldsgátlista í verkbeiðni geturðu fyllt út fyrirframskilgreinda gátlista um viðhald sem tengjast tegundum viðhaldsverka. Þú getur líka bætt við fleiri viðhaldsgátlistum.


## <a name="fill-in-a-maintenance-checklist"></a>Fylltu út viðhaldsgátlista

1. Smelltu á **Eignastýringu** > **Sameiginlegt** > **Verkbeiðnir** > **Allar verkbeiðnir** eða **Virkar verkbeiðnir**.

2. Veldu verkbeiðni og síðan á aðgerðarrúðunni, á flipanum **Verkbeiðni**, í hópnum **Línur**, velurðu **Viðhaldsgátlisti**.

3. **Gátlisti yfir verkbeiðni um viðhaldsverk** sérðu gátlista fyrir viðhald fyrir öll verk á verkbeiðni. Ef verkbeiðniverkin eru með mismunandi gerðir viðhaldsverka kunna viðhaldsgátslistar að vera mismunandi á hverju verkbeiðniverki. Veldu verkbeiðniverk til að vinna með tengdan viðhaldsgátlista. Upplýsingar um valda viðhaldsgátlistalínu eru sýndar á flýtiflipanum **Línuupplýsingar**.

4. Ljúktu við allar viðhaldsgátlistalínurnar, eina í einu, í sömu röð og þær birtast. Þú lýkur viðhaldslistalínu með því að fylla út reitina á flýtflipanum **Línuupplýsingar**. Upplýsingarnar sem þarf til að ljúka línu geta verið mismunandi eftir línugerð. Til dæmis, á línu af gerðinni **Texti** bætirðu við athugasemd sem útskýrir niðurstöðu athugunarinnar. Á línu af gerðinni **Mæling** bætirðu við teljaragildinu sem þú lest á búnaðinum og þú getur líka bætt við athugasemd, eftir þörfum. Viðhaldsgátlistalína af gerðinni **Haus** er notuð sem fyrirsögn til að flokka viðhaldsgátlistalínurnar sem birtast fyrir neðan hann. Þú þarft ekki að fylla út haus. Eins og fyrir allar aðrar gerðir af línum viðhaldsgátlista er hægt að bæta við athugasemd í gerðina **Haus**.

5. Ef leiðbeiningar eru tengdar viðhaldsgátlistalínu skal velja gátreitinn **Leiðbeiningar**. Lestu leiðbeiningar fyrir valda línu viðhaldsgátlista í reitnum **Leiðbeiningar** á flýtiflipanum **Línuupplýsingar**.

6. Þegar þú hefur lokið við viðhaldsgátlistalínu skaltu velja gátreitinn **Kannað** á þeirri línu til að merkja hana sem lokið. Til að fleygja viðhaldsgátlistalínu vegna þess að hún skiptir ekki máli fyrir verkbeiðnina skaltu velja gátreitinn **Á ekki við** á línunni. Ef gátreiturinn **Áskilið** er valinn í línu viðhaldsgátlista verðurðu að velja annaðhvort gátreitinn **Villuleitað** eða gátreitinn **Á ekki við**.

>[!NOTE]
>Þú getur aðeins uppfært skráningar viðhaldsgátlista ef verkbeiðnin er [Virk](../setup-for-work-orders/work-order-lifecycle-states.md) líftímastaða.  


## <a name="add-a-maintenance-checklist-line"></a>Bæta við viðhaldsgátlistalínu

Viðhaldsgátlistar eru búnir til út frá skilgreiningunni á sjálfgefinni gerð viðhaldsverksins og færðir yfir í verkbeiðnistörf. Ef þess er krafist geturðu bætt viðhaldsgátlistalínum við í verkbeiðnistarf. Viðhaldsgátlistalínum sem er handvirkt bætt við fá tilvísunina **Handvirkt**.

1. Á síðunni **Gátlisti yfir verkbeiðni um viðhaldsverk** velurðu verkbeiðnivinnslu til að bæta viðhaldsgátlista við.

2. Á flýtiflipanum **Línur viðhaldsgátlista** velurðu línu viðhaldsgátlista. Síðan, til að setja inn nýja línu á eftir valinni línu ýtirðu á lykilinn **Niðurör**. Næsta númer í röðinni er sjálfkrafa sett inn í reitinn **Línunúmer**. Veldu nýja línu til að setja nýja línu fyrir valda línu **Bættu við línu**. 

3. Í reitinn **Heiti** slærðu inn heiti fyrir línu viðhaldsgátlista.

4. Í reitnum **Gerð** velurðu gerð fyrir viðhaldsgátlistalínuna. Flýtiflipinn **Línuupplýsingar** inniheldur tengda reiti fyrir sérhverja gerð viðhaldsgátlista.
    - **Texti** - Notaðu þessa tegund til að bæta við viðhaldslistalínu fyrir viðhald sem hefur texta sem lýsir því sem gera þarf. Til dæmis er hægt að nota þessa gerð viðhaldsgátlista ef þú vilt að starfsmaður athugi eða skoði eitthvað en þú býst ekki við ákveðinni (mælanlegri) niðurstöðu. Þegar þú hefur valið þessa tegund, á flýtiflipanum **Línuupplýsingar**, í reitinn **Leiðbeiningar**, slærðu inn texta sem lýsir því sem gera þarf.
    - **Haus** - Lína viðhaldsgátlista af þessari gerð er notuð sem haus til að flokka línur viðhaldsgátlista sem birtast fyrir neðan hann. Þessi tegund er gagnleg ef þú ert með nokkrar viðhaldsgátlistalínur sem hægt er að skipta í ákveðin svæði. Eftir að þú hefur valið þessa tegund skaltu slá inn lýsandi heiti í reitinn **Heiti**.
    - **Sniðmát** - Þessi gerð á ekki við þegar þú bætir við viðhaldsgátlistalínu handvirkt við verkbeiðnivinnslu.  
    - **Breyta** - Notaðu þessa gerð notuð til að skilgreina mögulega útkomu á sviði á viðhaldsgátlistalínu. Upplýsingar um hvernig setja skal upp breytur viðhaldslista eru í [Flokkar viðhaldsverkgerðar og viðhaldsverkgerðir, afbrigði viðhaldsverkgerðar, viðskipti viðhaldsvinnslu og viðhaldsgátlistar](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md). Eftir að þú hefur valið þessa tegund skaltu slá inn lýsandi heiti á breytunni í reitinn **Heiti**. Á flýtiflipanum **Línulýsing**, í reitnum **Breyta**, velurðu breytuna. Í reitinn **Leiðbeiningar** skal slá inn texta sem lýsir því sem þarf að gera.
    - **Mæling** - Notaðu þessa tegund til að skrá sérstaka mælingu á viðhaldsgátlistalínunni. Eftir að þú hefur valið þessa tegund skaltu slá inn heiti á sniðmátinu í reitinn **Heiti**. Á flýtiflipanum **Línulýsing**, í reitunum **Teljari** og **Eining**, velurðu viðeigandi gildi. Í reitinn **Leiðbeiningar** skal slá inn texta sem lýsir því sem þarf að gera.

5. Þegar þú hefur lokið handvirkt við að bæta við viðhaldslistalínum viðhalds skaltu fylla út línurnar eins og lýst er í kaflanum **Fylltu út viðhaldsgátlista** hér að ofan.

>[!NOTE]
>Á síðunni **Gátlisti yfir verkbeiðni um viðhaldsverk** er ekki hægt að eyða línum viðhaldsgátlista sem hafa tilvísunina **Vinnslugerð**. Þú getur aðeins eytt línum viðhaldsgátlista sem þú eða aðrir starfsmenn viðhalds hafa stofnað handvirkt og sem eru með tilvísunina **Handvirkt**.

Eftirfarandi skýringarmynd hér að neðan sýnir dæmi um viðhaldsgátlista.

![Mynd 1](media/14-work-orders.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]