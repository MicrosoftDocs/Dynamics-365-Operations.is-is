---
title: Viðhaldsgátlistar
description: Þetta efni lýsir viðhaldsgátlistum í eignastýringu.
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
ms.openlocfilehash: 325ff1fa0811d6aac5189cc69f21483fce6b3e8f
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875720"
---
# <a name="maintenance-checklists"></a>Viðhaldsgátlistar


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Viðhaldsgátlistar eru settir upp á tegundum viðhaldsverka og notaðir þegar unnið er við verkbeiðnir. Að fylla út viðhaldsgátlista er hluti af því að ljúka verkbeiðni. Sjá kaflann [Flokkar viðhaldsverkgerðar og viðhaldsverkgerðir, afbrigði viðhaldsverkgerðar, viðskipti viðhaldsvinnslu og viðhaldsgátlistar](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md) til að fá frekari upplýsingar um hvernig á að setja upp viðhaldsgátlista yfir gerðir viðhaldsverka í skjámyndinni **Sjálfgefin tegund viðhaldsverka**.

Þegar þú vinnur með viðhaldsgátlista í verkbeiðni geturðu fyllt út fyrirframskilgreinda gátlista um viðhald sem tengjast tegundum viðhaldsverka. Það er einnig mögulegt að bæta við viðbótargátlistum yfir viðhald.

## <a name="fill-out-a-maintenance-checklist"></a>Fylltu út viðhaldsgátlista

1. Smelltu á **Eignastýringu** > **Sameiginlegt** > **Verkbeiðnir** > **Allar verkbeiðnir** eða **Virkar verkbeiðnir**.

2. Veldu verkbeiðnina og smelltu á **Viðhaldsgátlisti**.

3. Í **Gátlisti yfir verkbeiðni um viðhaldsverk** sérðu gátlista fyrir viðhald fyrir öll verk á verkbeiðni. Ef verkbeiðniverkin eru með mismunandi gerðir viðhaldsverka kunna viðhaldsgátslistar að vera mismunandi á hverju verkbeiðniverki. Veldu verkbeiðniverk til að vinna með tengdan viðhaldsgátlista. Upplýsingar um valda viðhaldsgátlistalínu eru sýndar á flýtiflipanum **Línuupplýsingar**.

4. Ljúktu við allar viðhaldsgátlistalínurnar, eina í einu, í sömu röð og þær eru sýndar. Viðhaldsgátlistalína af gerðinni „Haus“ er notuð sem fyrirsögn til að flokka viðhaldsgátlistalínurnar hér neðan. Þú þarft ekki að fylla út haus en eins og fyrir allar gerðir viðhaldsgátlistalína er mögulegt að bæta við **Athugasemd** í hausinn.

5. Ef leiðbeiningar eru tengdar viðhaldsgátlistalínu skal velja gátreitinn **Leiðbeiningar**. Lestu leiðbeiningar fyrir valda viðhaldsgátlistalínu á flýtiflipanum **Línuupplýsingar** > kaflanum **Leiðbeiningar**.

6. Upplýsingarnar sem krafist er til að ljúka viðhaldslistalínu geta verið breytilegar, allt eftir gerð viðhaldsgátlistans. Þú lýkur viðhaldslistalínu með því að fylla út reitina á flýtflipanum **Línuupplýsingar**. Til dæmis, á línu af gerðinni „Texti“, bætirðu **Athugasemd** við sem útskýrir hver var niðurstaða þeirrar gátlistalínu. Á línu af gerðinni „Mæling“ bætirðu við **Gildi teljara** sem þú lest á búnaðinum og þú getur líka bætt við **Athugasemd**, ef nauðsyn krefur.

- Þegar þú hefur lokið við viðhaldsgátlistalínu skaltu velja gátreitinn **Kannað** á línunni til að merkja hana sem lokið. Ef þú vilt fleygja viðhaldsgátlistalínu vegna þess að hún skiptir ekki máli fyrir verkbeiðnina skaltu velja gátreitinn **Á ekki við** á línunni. Ef viðhaldsgátlistalína er merkt **Skylda** verður þú að merkja hana sem annaðhvort „Merkt“ eða „Á ekki við“.  
- Þú getur aðeins uppfært skráningar viðhaldsgátlista ef verkbeiðnin er [Virk](../setup-for-work-orders/work-order-lifecycle-states.md) líftímastaða.  


## <a name="add-a-maintenance-checklist-line"></a>Bæta við viðhaldsgátlistalínu

Viðhaldsgátlistar eru búnir til út frá skilgreiningunni á sjálfgefinni gerð viðhaldsverksins og færðir yfir í verkbeiðnistörf. Ef þess er krafist geturðu bætt viðhaldsgátlistalínum við í verkbeiðnistarf. Viðhaldsgátlistalínum sem er handvirkt bætt við fá tilvísunina „Handvirkt“.

1. Í **Gátlisti yfir verkbeiðni um viðhaldsverk** velurðu verkbeiðnivinnslu sem þú vilt bæta viðhaldsgátlista við.

2. Á flýtiflipanum **Viðhaldsgátlistalínur** velurðu viðhaldsgátlistalínu og ýtir á ör niður-hnappinn á lyklaborðinu þínu ef þú vilt setja nýja línu á eftir valinni viðhaldsgátlistalínu. Næsta númer í röðinni er sjálfkrafa sett inn í reitinn **Línunúmer**. Þú getur einnig valið viðhaldsgátlistalínu og smellt á hnappinn **Bæta við línu** ef þú vilt setja inn nýja línu fyrir ofan valda gátlistalínu viðhalds.

3. Settu inn heiti fyrir sniðmát viðhaldsgátlista í reitinn **Heiti**.

4. Í reitnum **Gerð** velurðu gerð fyrir viðhaldsgátlistalínuna. Fyrir hverja gerð viðhaldsgátlista eru tengdir reitir sýndir á flýtiflipanum **Línuupplýsingar**.  
  a. „Texti“ er notaður til að bæta við viðhaldsgátlistalínu með textalýsingu á því hvað eigi að gera. Þessa gerð viðhaldsgátlista má nota ef þú vilt að starfsmaður athugi eða skoði eitthvað en þú býst ekki við ákveðinni (mælanlegri) niðurstöðu. Settu inn lýsingu á því hvað á að gera í kaflanum **Leiðbeiningar** á flýtiflipanum **Línulýsing**. b. „Haus“ er notaður sem fyrirsögn til að flokka viðhaldsgátlistalínurnar sem eru sýndar fyrir neðan hausinn. Þetta er gagnlegt ef þú ert með nokkrar viðhaldsgátlistalínur sem hægt er að skipta í ákveðin svæði. Færið inn lýsandi heiti á svæðinu **Heiti**.  
  c. „Sniðmát“ á ekki við þegar þú bætir við viðhaldsgátlistalínu handvirkt við verkbeiðnivinnslu.  
  d. „Breyta“ er notuð til að skilgreina mögulega útkomu á sviði á viðhaldsgátlistalínu. Uppsetningin á breytum viðhaldslista er lýst í [Flokkar viðhaldsverkgerðar og viðhaldsverkgerðir, afbrigði viðhaldsverkgerðar, viðskipti viðhaldsvinnslu og viðhaldsgátlistar](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md). Í reitnum **Heiti** slærðu inn heiti til að lýsa breytu. Veldu breytuna í reitnum **Breyta**. Settu inn lýsingu á því hvað á að gera í kaflanum **Leiðbeiningar** á flýtiflipanum **Línulýsing**.  
  e. „Mæling“ er notuð til að skrá tiltekna mælingu. Í reitnum **Heiti** slærðu inn heiti fyrir mælinguna. Á flýtiflipanum **Línulýsing** velurðu **Teljari** og **Eining**. Settu inn lýsingu á því hvað á að gera í kaflanum **Leiðbeiningar**.  

5. Þegar þú ert búinn að bæta við viðhaldsgátlistalínum handvirkt skaltu fylla út línurnar eins og lýst er í hlutanum hér að ofan.

>[!NOTE]
>Í **Gátlisti yfir viðhaldsvinnslu verðbeiðni** geturðu ekki eytt gátlistum fyrir viðhaldsgátlistalínur með tilvísuninni „Vinnslugerð“. Þú getur aðeins eytt gátlistum fyrir viðhaldsgátlista með tilvísuninni „Handvirkt“ sem þú eða aðrir starfsmenn viðhalds hafa stofnað handvirkt.


![Mynd 1](media/14-work-orders.png)

