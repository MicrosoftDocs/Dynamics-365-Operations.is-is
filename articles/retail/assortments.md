---
title: "Stjórnun vöruúrvals"
description: "Í þessu efnisatriði er fjallað um grundvallarhugtök stjórnunar á vöruúrvali í Microsoft Dynamics 365 for Retail og hugleiðingar um framkvæmd verka."
author: jblucher
manager: AnnBe
ms.date: 3/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application user
ms.search.scope: Retail, Operations
ms.search.region: Global
ms.author: jeffbl
ms.search.validFrom: 2017-11-21
ms.dyn365.ops.version: Application update 5
ms.translationtype: HT
ms.sourcegitcommit: 44b0c4e39ac7410d27ce531c898bb8c423af334a
ms.openlocfilehash: 303f86d6a57e039cb51700744697949845239b10
ms.contentlocale: is-is
ms.lasthandoff: 03/12/2018

---

# <a name="assortment-management"></a>Stjórnun vöruúrvals
[!INCLUDE [banner](../includes/banner.md)]

## <a name="overview"></a>Yfirlit
Microsoft Dynamics 365 for Retail veitir *vöruúrval* sem gerir þér kleift að stjórna afurðaframboði yfir rásum. Vöruúrval ákvarðar hvaða afurðir eru í boði í tilteknum verslunum og á tilteknu tímabili.

Í Retail er vöruúrval vörpun af einni eða fleiri rásum (eða flokkum rása þegar stigveldi fyrirtækja eru notuð) á eina eða fleiri afurðir (eða afurðaflokka þegar flokkastigveldi er notað).

Heildarsamsetning afurða í rás er ákvörðuð af útgefnu vöruúrvali sem er úthlutað til rásarinnar. Þess vegna er hægt að skilgreina margar gerðir af vöruúrvali fyrir hverja rás.

### <a name="basic-assortment-setup"></a>Grunnuppsetning vöruúrvals
Í eftirfarandi dæmi er einkvæmt vöruúrval skilgreint fyrir hverja verslun. Í þessu tilviki er aðeins afurð 1 í boði í verslun 1 og aðeins afurð 2 er í boði í verslun 2.

![Hver afurð er fáanleg í einni verslun](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/jblucher-manage-assortments/articles/retail/media/Managing-assortments-figure1.png?raw=true "Hver afurð er fáanleg í einni verslun")

Til að bjóða upp á afurð 2 í verslun 1 geturðu bætt afurðinni við vöruúrval 1.

![Afurð 2 bætt við vöruúrval 1](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/jblucher-manage-assortments/articles/retail/media/Managing-assortments-figure2.png?raw=true "Afurð 2 bætt við vöruúrval 1")

Að öðrum kosti er hægt að bæta verslun 1 við vöruúrval 2.

![Verslun 1 bætt við vöruúrval 2](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/jblucher-manage-assortments/articles/retail/media/Managing-assortments-figure3.png?raw=true "Verslun 1 bætt við vöruúrval 2")

### <a name="organization-hierarchies"></a>Stigveldi fyrirtækis
Í tilfellum þar sem margar rásir deila sama vöruúrvalinu er hægt að skilgreina vöruúrvalið með því að nota stigveldi fyrirtækis fyrir Retail úrval. Þegar hnútum frá þessu stigveldi er bætt við verða allar rásir í þessum hnút og undirhnútum innifaldar.

![Stigveldi fyrirtækis](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/jblucher-manage-assortments/articles/retail/media/Managing-assortments-figure4.png?raw=true "Stigveldi fyrirtækis")

### <a name="product-categories"></a>Afurðartegundir
Á svipaðan hátt er hægt að bæta við afurðaflokkum með því að nota stigveldi afurðartegunda á afurðasíðunni. Þú getur skilgreint vöruúrval með því bæta við einum eða fleiri hnútum tegundastigveldis. Í þessu tilfelli mun vöruúrvalið innihalda allar afurðir í þessum tegundarhnút og undirhnútum hans.

![Afurðartegundir](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/jblucher-manage-assortments/articles/retail/media/Managing-assortments-figure5.png?raw=true "Afurðartegundir")

### <a name="excluded-products-or-categories"></a>Útilokaðar afurðir eða tegundir
Til viðbótar við að innihalda afurðir og tegundir í vöruúrvali er hægt að nota útilokunarvalkostinn til að skilgreina tilteknar afurðir eða tegundir sem ættu að vera útilokaðar frá vöruúrvali. Í eftirfarandi dæmi viltu hafa með allar afurðir í tiltekinni tegund nema afurð 2. Í þessu tilfelli þarf ekki að skilgreina afurð vöruúrvals eftir afurð eða stofna fleiri tegundarhnúta. Í staðinn er einfaldlega hægt að bæta tegundinni við en útiloka afurðina.

> [!NOTE]
> Ef afurð er bæði innifalinn og útilokuð í einu eða fleiri gerðum vöruúrvals samkvæmt skilgreiningu, verður afurðin alltaf talin útilokuð.

![Útilokuð afurð](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/jblucher-manage-assortments/articles/retail/media/Managing-assortments-figure6.png?raw=true "Útilokuð afurð")

### <a name="global-and-released-products"></a>Alþjóðlegar og útgefnar afurðir
Vöruúrval er skilgreint á alþjóðavísu og getur innihaldið rásir frá mörgum lögaðilum. Afurðirnar og tegundirnar sem eru í vöruúrvalinu er einnig deilt þvert yfir lögaðila. Hins vegar verður að gefa út afurð áður en hægt er að selja, panta, telja eða taka á móti henni í rásinni (til dæmis á sölustaðnum \[Sölustaður\]). Því þrátt fyrir að tvær verslanir ólíkra lögaðila geti deilt vöruúrvali sem inniheldur sömu afurðir eru afurðirnar aðeins tiltækar ef þær hafa verið gefnar út til þessara lögaðila.

### <a name="dynamic-and-static-assortments"></a>Gagnvirkt og kyrrstætt vöruúrval
Vöruúrval getur verið skilgreint með tilteknum rásum og afurðum eða með því að telja með fyrirtækiseiningar og tegundir. Vöruúrval, þar með taldar tilvísanir í þessa flokka, er litið á sem gagnvirkt vöruúrval. Ef skilgreiningin eða innihald þessara flokka breytist meðan vöruúrvalið er virkt breytist skilgreiningin á vöruúrvalinu einnig.

Til dæmis er vöruúrval upphaflega skilgreint og útgefið þannig að það vísar til afurðartegundar. Ef viðbótarafurðum er síðar bætt við tegundina eru þær afurðir sjálfkrafa innifaldar í skilgreiningunni á núverandi vöruúrvali. Ekki Þarf að bæta afurðunum handvirkt við vöruúrvalið. Á svipaðan hátt, ef fyrirtækiseiningu er bætt við annan hnút, er vöruúrval fyrirtækiseiningarinnar sjálfkrafa leiðrétt á grundvelli þeirrar skilgreiningar.

### <a name="stopped-products"></a>Stöðvaðar afurðir 
Hægt er að „stöðva" útgefna afurð fyrir söluferlið með því að kveikja á stillingunni **Sjálfgefin pöntun**. Þessi stilling er oftast notuð þegar afurð er við lok líftíma síns og ætti ekki að selja á hvaða rás sem er. Vöruúrval virðir þessa stillingu og stöðvaðar afurðir verða ekki flokkaðar, óháð stillingu vöruúrvals.

### <a name="blocked-products"></a>Læstar afurðir
Auk þess að stöðva sölu á afurð er hægt að loka tímabundið á sölu á afurð. Þú getur skilgreint þessa stillingu í flipanum **Retail** fyrir útgefna afurð. Læstar afurðir eru ennþá flokkaðar, en þú færð skilaboð á sölustaðnum sem segir að ekki sé hægt að selja afurðin.

### <a name="date-effectivity"></a>Dagsetningarvirkni
Vöruúrval er dagsetningarvirkt. Þess vegna geta smásalar skilgreint hvenær afurðir eiga eða eiga ekki að vera tiltækar fyrir hverja rás. Hægt er að skilgreina og gefa út vöruúrval fram í tímann og tilgreina upphafs- og lokadagsetningar. Afurðirnar verða sjálfkrafa tiltækar eða ekki tiltækar á tilgreindum dagsetningum.

### <a name="process-assortments-batch-job"></a>Runuvinnsla á vöruúrvalsvinnu
Fyrst þarf að vinna úr vöruúrvali sem er skilgreint í Retail áður en það tekur gildi. Vinnslan er gerð af eftirfarandi ástæðum:

- Skilgreiningar á vöruúrvali verða að vera afstaðlaðar þannig að rásir geti auðveldlega nýtt þær. Afurðasamsetning fyrir rás er hægt að skilgreina með mörgum gerðum af vöruúrvali sem ná yfir ýmis dagsetningabil. Þegar einhverjar af þessum upplýsingum eru reiknaðar fram í tímann á þjóninum batna afköst rásarinnar.
- Afurðir og rásir í vöruúrvalinu geta breyst út fyrir sjálft vöruúrvalið. Gagnvirkt vöruúrval sem inniheldur tilvísanir í tegundir eða fyrirtækiseiningar verður að vinna úr reglulega þannig að það innihaldi eða útiloki færslur sem byggjast á núverandi úthlutun.

## <a name="implementation-considerations"></a>Umhugsunarefni fyrir innleiðingu
Íhugið eftirfarandi kröfur um innleiðingu þegar vöruúrval er áætlað og stjórnað fyrir innleiðingu smásölunnar:

- **Afritunargögn og stærð gagnagrunns** - Þótt vöruúrval hjálpi til við að þjóna þörfum fyrirtækisins til að stjórna afurðaframboði, er það einnig mikilvægt verkfæri til að stjórna stærð rásar og ótengdum gagnagrunnum. Vel stjórnað vöruúrval hjálpar til við að draga úr gagnamagninu sem þarf að vinna úr og afrita í rás og ótengda gagnagrunna. Það dregur einnig úr fjölda færslna sem verður að viðhalda. Færri færslur í þessum gagnagrunnum auka afköst þegar þú bætir vörum við færslu, leitar og flettir upp á afurðum.
- **Dagsetningarvirkni/vöruúrval að renna út á tíma** - Eitt árangursríkasta verkfærið til að stjórna fjölda afurða í rás og ótengdum gagnagrunnum er dagsetningarvirkni vöruúrvals. Ef árstíðabundnar afurðir eða afurðir sem eru að renna út á tíma eru skildar eftir með engan líftíma munu gagnagrunnarnir stækka án takmarkanna. Hægt er að nota ýmsar leiðir til að ná tökum á ástandinu. Til dæmis er hægt að vinna með aðskilið vöruúrval fyrir árstíðabundnar afurðir og afurðir sem eru alltaf í boði.
- **Sölur og skil utan vöruúrvals** – Þessi möguleiki hjálpar smásölum að stjórna vöruúrvali sínu á árangursríkan hátt með því að leyfa þeim að takmarka fjölda tiltækra afurða til afurða sem tilheyra undirstöðuafurðum samsetningarinnar fyrir verslunina. Þessi möguleiki hjálpar einnig smásölum að takast á við aðstæður þar sem afurð var ranglega sleppt úr vöruúrvali eða þar sem afurð var skilað utan virkra dagsetninga fyrir vöruúrvalið.

Ef afurðargögn eru ekki til í gagnagrunni rásar mun sölustaðurinn hafa samskipti í rauntíma við höfuðstöðvar til að sækja nauðsynlegar upplýsingar svo hægt sé að selja, skila eða setja afurðina á pöntun viðskiptavinar. Afurðarupplýsingar sem eru sóttar með þessum hætti eru aðeins tiltækar á meðan á þessari færslu stendur. Afurðinni er ekki bætt við skilgreiningu vöruúrvalsins. Þess vegna verða næstu samskipti í rauntíma gerð eftir þörfum.

