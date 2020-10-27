---
title: Verkþáttarbyggð úthýsing
description: Þetta umfjöllunarefni lýsir ítarlega hvernig á að nota undirverktaka aðgerðir í framleiðsluflæði fyrir lean-framleiðslu.
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, PlanActivity, ReqSupplyDemandSchedule, PlanActivityServiceDetails, PlanActivityServiceWizard
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 267034
ms.assetid: 15c76a51-fa6d-42d2-994a-c67df6bae6a9
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 48a1943833408767fe77456f66bbe109170a29e2
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/10/2020
ms.locfileid: "3985658"
---
# <a name="activity-based-subcontracting"></a>Verkþáttarbyggð úthýsing

[!include [banner](../includes/banner.md)]

Þetta umfjöllunarefni lýsir ítarlega hvernig á að nota undirverktaka aðgerðir í framleiðsluflæði fyrir lean-framleiðslu.

Í Microsoft Dynamics 365 Supply Chain Management eru tvær nálganir við úthýsingu: framleiðslupantanir og lean-framleiðsla. Í lean-framleiðslu er úthýsingarvinna byggðt upp sem þjónusta sem er tengd við verkþátt framleiðsluflæðis. Sérstök gerð kostnaðarflokks sem kallast **Bein útvistun** hefur verið kynnt til sögunnar og úthýsingarþjónusta er ekki lengur hluti af uppskrift (BOM). Kostnaðarbókhald vinnu undirverktaka er samþætt að fullu inn í kostnaðarútreikningslausn fyrir lean-framleiðslu.

## <a name="production-flows-that-involve-subcontractors"></a>Framleiðsluflæði sem taka til undirverktaka
Meginregla framleiðsluflæðis breytist ekki þegar aðgerðir eru útvistaðar. Efnið flæðir enn á milli staðsetninga, ferlisaðgerðir breyta efni í afurð og flutningsaðgerðir flytja efni eða afurð af einni staðsetningu í aðra. Hægt er að byggja staðsetningar og vinnuflokka á lánardrottnastýrðu með því að úthluta lánardrottnalykli á vöruhús eða á tilföng í tilfangaflokki.  

Á grunni þessarar virkni þarf lean-framleiðsla ekki neina tilgreinda eiginleika til að styðja flæði efnis og afurða. Allar hugsanlegar sviðsmyndir sem taka til lánardrottna sem veitenda framleiðslu- eða flutningsþjónustu má byggja á uppbyggingu framleiðsluflæðis og aðgerða.  

Til dæmis vinnur undirverktaki í geymslusvæði sem er staðsett hjá undirverktaka. Þegar afgreiðslueiningar eru tæmdar hjá undirverktaka er kanban-spjöldum skilað í samsetningarhólfið ásamt næstu sendingu. Síðan er fyllt á geymslusvæðið hjá undirverktakanum. Flutning til og frá undirverktaka má byggja á skýrum flutningsaðgerðum til að styðja tiltektar- og sendingarferli. Ef skýrrar skráningar er ekki krafist til að styðja efnislegan flutning, er hægt að sleppa flutningsaðgerðunum.  

Undirverktaka má nota til að álagsjafna heildargetu framleiðsluflæðis. Til dæmis er framleiðsluflæði byggt á notkun áætlaðrar kanban-regla. Áætlunin notar kanban-röðunarspjald til að áætla og álagsljafna báða vinnuflokka við eftirspurn. Áætlunin fylgist einnig með sameinaðri birgðaáætlun fyrir geymslusvæðið á síðunni **Birgðaáætlun**. Marga undirverktaka er hægt að byggja á einu eða mörgum framleiðsluflæðum og það kunna að vera margar kanban-reglur sem hægt er að nota til að setja sömu afurðina á sömu staðsetningu með mismunandi aðgerðum. Áætlunin getur umbreytt kanban-reglu í aðra kanban-reglu í enduráætlun kanban-reglu sem var upphaflega stofnuð fyrir Innra framleiðsla til valkostur ferli. Reyndar hefur undirverktakaeðli vinnuflokksins ekki áhrif á framleiðsluflæði. Sama meginregla vinnu gildir fyrir two samhliða innra vinnuflokkur eða fyrir tvo undirverktaka hólf.   

Líkt og allir aðrir verkþættir í framleiðsluflæði geta undirverktakaaðgerðir notað og framboðið birgðaskráðar, óbirgðaskráðar (verk í vinnslu \[VÍV\]) og hálfkláruð efni og afurðir. Í öllum tilvikum eru ferlin fyrir tímasetningu og framkvæmd undirverktakaaaðgerða þau sömu. Þar fyrir utan eru þessi ferli þau sömu og ferli fyrir Innra vinna.

## <a name="purchase-process-for-subcontracted-activities-services"></a>Innkaupaferli fyrir undirverktakaaðgerðir (þjónusta)
Innkaupaferli fyrir undirverktakaaðgerðir er á grunni efnislegs efnisflæðis sem er skráð með kanban-vinnsluframvindu, til dæmis, Byrja eða Ljúka. Fjárhagslega flæðið, til dæmis, kostnaður af undirverktakavinnu, er aukaflæði sem fylgir efnislegu flæði. Um leið er Innkaupaferlið sjálfstætt ferli sem leyfir handvirka leiðréttingu á innkaupaskjali í hverju skrefi. Hér er innkaupaferli fyrir undirverktakaaðgerðir:

1.  Stofnaðu innkaupasamning. Innkaupasamningur er stofnaður fyrir þjónustuna og tengdur við verkþátt í framleiðsluflæði.
2.  Stofna innkaupapöntun. Losunarinnkaupapantanir má stofna fyrir þjónustuna, byggt á áætluðum kanban-vinnslum. Vinnslur fyrir sömu þjónustu má flokka í innkaupapöntunarlínur eftir degi, viku eða mánuði. Hægt er að stofna innkaupapöntunarlínu hvenær sem er eftir að kanban-vinnslur eru stofnaðar. Innkaupapöntunarlínur má jafnvel stofna eftir upplýsingar. Þessi valkostur er yfirleitt valinn ef undirverktaki veitir þjónustu án viðbótartilkynningar, á grunni kanbans eða kanban-spjalda sem undirverktaki móttekur. Í þessu tilviki er hægt að fela frávik milli innkaupapöntunar og reiknings.
3.  Mynda kanban-spjöld, efni, og tiltektarlista til að senda til undirverktaka til undirbúnings fyrir vinnslu. Á grunni sundurliðað líkans af framleiðsluflæði, er undirbúningur gerður á kanban-spjaldi fyrir ferli aðgerðir með því að nota tiltektarlista og undirbúningsaðgerðir. Einnig er hægt að gera undirbúning á kanban-spjaldi fyrir flutningsvinnslur með því að nota tiltektarlista og byrjun eða lok. Fyrir birgðaskráð efni geta bæði ferlin verið studd af WMS-Tiltekt og Sending ferli. Hægt er að stofna farmbréf eftir þörfum.
4.  Mynda kanban-afgreiðslueiningar og kanban-spjöld. Eftir vinnslu er spjöldum skilað til undirverktaka. Yfirleitt innihalda spjöldin fylgiseðil sem tilgreinir aþð efnislega efni sem hefur verið sent. Tilvísunar í veitta þjónustu er ekki þörf. Koma efnis efni eða afurðar til viðskiptamanns er skráð á kanban-spjald, eftir kanban-spjöldum. (Annaðhvort er kanban-spjalið fyrir vinnsluaðgerðir eða kanban-spjaldið fyrir flutningsvinnslu notað, eftir líkansaðgerðum.).
5.  Mynda innhreyfingaráðgjöf. Innhreyfingaráðgjöf er hægt að nota til að skipta út fylgiseðli fyrir móttekna þjónustu. Innhreyfingarráðgjöf er hægt að mynda á lokinna kanban-vinnsla fyrir úthýsingarverkþætti fyrir valið tímabil. Fyrir hverja vinnslumóttöku eru innhreyfingar stofnaðar fyrir tengda innkaupapöntunarlínu. Innhreyfingarráðgjöfina má prenta og senda til undirverktaka sem staðfesting á innhreyfingu.
6.  Mynda reikning.

Ferlinu lýkur þegar undirverktaki er reikningsfærður fyrir tímabil. Reikningsjöfnun er gerð gagnvart þeirri innhreyfingaráðgjöf sem er stofnuð. Þar sem innhreyfingarráðgjöf stendur fyrir nákvæma efnislega innhreyfingu efnis, er þríhliða jöfnun einfölduð.

## <a name="configuring-activities-for-subcontracting"></a>Grunnstilling aðgerða fyrir úthýsingu
Eftirfarandi hlutar útskýra hvernig á að grunnstilla aðgerðir fyrir úthýsingu,

### <a name="subcontracted-services"></a>Þjónusta undirverktaka

Greiðsluliðurinn sem er notaður í úthýsingu byggða á verkþætti verður að vera afurð sem hefur eftirfarandi eiginleika:

-   **Gerð afurðar:** Þjónusta
-   **Flokkar birgðalíkana:** Ekki á lager

Þessi krafa setur notkun á fyrst inn, fyrsta út (FIFO (fyrst inn - fyrst út)) birgðalíkan. **Athugasemd:** Kostnaðarútreikningur á afurðum krefst að staðalkostnaður þjónustu sé skilgreindur. Innkaupasamnings við lánardrottin er áskilinn. Að öðrum kosti er ekki hægt að nota þjónustu fyrir úthýsingu byggða á verkþáttum.

### <a name="subcontracted-process-activities"></a>Verkþættir úthýsingar

Til að skilgreina a ferli verkþátt sem verkþátt úthýsingar skal fylgja þessum skrefum.

1.  Grunnstilla úthýstan vinnuflokk. Til að skilgreina vinnuflokk sem undirverktaka, verður að stofna tilfang af gerðinni **Lánardrottinn** og tengja það við vinnuflokk (tilfangaflokk). Keyrsla kostnaðartegundar af kostnaðarflokksgerðinni **Bein útvistun** ætti að vera úthlutað til vinnuflokks. Kostnaðartegundir fyrir uppsetningu og magn eru ekki áskildar.
2.  Eftir að ferlisverkþáttur er stofnaður og tengdur við úthýstan vinnuflokk verður þú skilgreina þjónustu fyrir verkþáttinn áður en hægt er að virkja útgáfu framleiðsluflæðis. Þessu skrefi er lokið á síðunni **Verkþáttur** **upplýsingasíða**. Fyrir aðgerðir sem tengjast undirverktaka vinnuflokkur, er flýtiflipinn **Þjónustuskilmálar** sýndur. Á þessum flýtiflipi skal bæta við sjálfgefinni þjónustu sem er gild fyrir frálagsatriði. Ef tilgreind frálagsatriði þurfa mismunandi þjónustu eða mismunandi þjónustufæribreytur (til dæmis mismunandi þjónustuhlutfall), geturðu bætt við annarri þjónustu í verkþáttinn.

## <a name="subcontracted-transfer-activities"></a>Flutningsaðgerðir verktaka
Flutningsverkþáttur er skilgreindur sem úthýstur verkþáttur, eftir stillingum á **Flutt með** flutningsverkþátta. Eftirtaldir valkostir eru í boði:

-   **Farmsendandi** - Aðgerðinni er úthýst ef flutningur frá vöruhúsi er stjórnað af lánardrottni (eins og það er skilgreint af eiginleika vöruhússsins). Allir valdir innkaupasamningar fyrir þjónustu verða að hafa sama kenni lánardrottins og vöruhúsið.
-   **Viðtakandi** - Aðgerðinni er úthýst ef flutningur til vöruhúss er stjórnað af lánardrottni (eins og það er skilgreint af eiginleika vöruhússsins). Allir valdir innkaupasamningar fyrir þjónustu verða að hafa sama kenni lánardrottins og vöruhúsið.
-   **Flutningsaðili** - Aðgerðinni er úthýst til allra lánardrottna sem veita þjónustuna. Til að vera gildur verður flutningsaðili að vera stofnaður fyrir vöruhúsakerfi og skal haaf úthluðum lánardrottnalykill.

Eins og fyrir verkþætti verður þú skilgreina sjálfgefna þjónustu fyrir flutningsaðgerðir verktaka á flýtiflipanum **Þjónustuskilmálar** á **Verkþáttur** **upplýsingasíða**.

## <a name="service-quantity-calculation"></a>Útreikningur þjónustumagns
Allt innkaupaferlið er byggt á vörutilvísun sem þjónustu. Þessi vörutilvísun er mæld í mælieiningum þjónustu. Þjónusta er yfirleitt mæld annaðhvort í fjölda þjónustu (einingum) eða í tíma. Til að reikna út þjónustumagn á grunni skráðra loka kanban-vinnsla er hægt að nota eftirfarandi aðferðir:

-   **Útreikningur sem byggður á fjölda vinnsla** – Ein kanban-vinnsla jafnast á við *n* þjónustueiningar, án tillits til þess afurðarmagns sem er gefið upp. Í lean-framleiðslu samsvarar ein vinnsla einni afgreiðslueiningu. Þessi útreikningur aðferð gildir um alla þjónustu sem er með fast verð á hverja afgreiðslueiningu. Þess vegna gildir þessi aðferð yfirleitt um flutningsaðgerðir. Hins vegar getur hún einnig átt við um verkþætti sem vinna heilar afgreiðslueiningar.
-   **Útreikningur sem er byggður á afurðarmagni** – Þjónustumagn er í hlutfalli við það afurðarmagn sem er áætlað/birgðum. Þegar uppgefið af er reiknað er hægt að hafa villumagn annaðhvort með eða útiloka það. Þessi útreikningsaðferð gildir um öll mál þar sem þjónustuverð á einingu unninnar afurðar hefur verið samþykkt.
-   **Útreikningur sem er byggður á verkþáttatíma** – Fræðilegir verkþáttatímar eru reiknaðir, byggðir á vinnslutíma verkþáttar, samtals unnu magni og the samtals ferli magn, og afkastagetu unninnar afurðar. Þessi útreikningsaðferð á við um þjónustu sem er greidd samkvæmt tímagjaldi og er með frávik í tíma á hverja unna vöru.

## <a name="cost-accounting-of-subcontracted-services"></a>Kostnaðarbókhald þjónustu undirvektaka
Þegar innhreyfingaráðgjöf eða fylgiseðill lánardrottins á innkaupapöntun sem var stofnuð fyrir framleiðsluflæði (með öðrum orðum innkaupapöntun sem var mynduð á grunni kanban-vinnsla fyrir úthýstar aðgerðir) er bókuð, er gildi innhreyfingarinnar reikningsfært á VÍV-reikningi framleiðsluflæðis. Frávik reikninga eru einnig reikningsfærð í framleiðsluflæðið. Kostnaðartegund fyrir úthýsta vinnu hefur verið kynnt til sögunnar. Þessi kostnaðartegund virkjar gegnsæja rakningu gilda úthýstrar vinnu sem er úthlutað í VÍV og notað á tímabil.  

Bakfærslukostnaðaraðferð fyrir lean-framleiðslu í lok kostnaðartímabils reiknar út raunfrávik afurða sem eru framleiddar úr framleiðsluflæðinu á meðan kostnaðartímabilinu stendur.

## <a name="modeling-transfers-as-subcontracted-activities"></a>Líkan millifærslur sem undirverktaka aðgerðir
Fólk álítur flutning oft vera ekki notaðan í framleiðslu og að hann bæti engu virði við vöru. En þegar kostnaður úthýsingar er hins vegar borinn saman í kostnaði Innra framleiðsla, þarf að taka tilliti til kostnaðar af viðbótarflutningsaðgerðum. Framleiðsluflæði sem spannar margar staðsetningar og krefst flutningsþjónustu ætti að byggja flutningskostnaðinn á hluta af kostnaði við framboð á afurðum til viðskiptamanna. 

Úthýsingar byggðar á verkþáttum í lean-framleiðslu leyfa þér að samþætta flutningsaðila og flutningslánardrottna sem flytja efni og afurðir milli staðsetninga í framleiðsluflæði. Með því að gera líkan af flutningsverkþætti er hægt að úthluta flutningsaðila eða lánardrottni. Flutningsaðgerðir/vinnsla er byggð á þjónustu og innkaupasamnings, og hægt er að stofna innkaupapöntun og innhreyfingaráðgjöf, á grunni raunflutningsvinnslu. Þessi virkni er sú sama og virknin fyrir verkþætti úthýsingar.  

Núna styður Supply Chain Management uppskriftarútreikninga sem fela í sér flutningsþjónustu, stofnun á tengdum innkaupapöntunum, samþætta skráningu innhreyfinga og samþættingu á flutningsþjónustukostnaði í kostnaðarútreikning framleiðsluflæðis.



