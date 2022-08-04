---
title: Vinna með brot
description: Þessi grein lýsir hvers vegna, hvenær og hvernig á að nota brot í Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 02/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f911c5ee209cfcde5d2b2aef2c8f7343eb694cd3
ms.sourcegitcommit: 9cfccb5c260ce56a3457f9ea12e80f54ea55a3b4
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 07/21/2022
ms.locfileid: "9183290"
---
# <a name="work-with-fragments"></a>Vinna með brot 

[!include [banner](includes/banner.md)]

Þessi grein lýsir hvers vegna, hvenær og hvernig á að nota brot í Microsoft Dynamics 365 Commerce.

Brot gera ráð fyrir miðlægri höfundarupplifun fyrir einingasamsetningar sem þarf að endurnýta á vefsvæðinu þínu. Til dæmis eru fyrirsagnir, síðufætur og borðar oft stilltir sem brot því þeim er deilt á margar síður. Þú getur hugsað um brot sem litlar vefsíður sem hægt er að setja inn á aðrar síður á vefsvæðinu. Brot hafa sinn eigin líftíma. Með öðrum orðum, þau eru búin til, vísað til, uppfærð og þeim eytt sem sjálfstæðum aðilum í höfundatólunum.

Eftir að brot eru stillt er hægt að nota þau alls staðar sem hægt er að nota einingar í vefsvæðinu. Hægt er að vísa í brot á síðum, í skipulagi, í sniðmátum og í öðrum brotum.

> [!NOTE]
> Brot geta verið ívafin í allt að sjö stig djúpt inni í öðrum brotum.

Til dæmis, ef þú vilt auglýsa árstíðabundinn viðburð yfir margar síður á svæðinu okkar, geturðu notað brot. Fyrsta skrefið í því ferli að búa til nýtt brot er að velja gerð einingar sem þú vilt byrja á. Fyrir þetta dæmi er hægt að smíða brot úr hetjueiningunni.

> [!NOTE]
> Brot er hægt að smíða úr hvaða einingagerð sem er.

Þú getur síðan stillt hetjubrotið með sérstöku kynningarinnihaldinu. Þú getur líka staðfært það eins og þú vilt. Nýja sjálfstæða hetjubrotið er síðan hægt að nota sem forstillta einingu á vefsvæðinu þínu. Þú getur auðveldlega bætt því við sniðmát, á tilteknar síður eða í önnur brot sem geta innihaldið hetjueiningar.

Allir staðirnir þar sem brotinu er bætt við eru tilvísanir í miðlægahetjubrotið sem þú bjóst til. Ef þú birtir breytingar á brotinu endurspeglast þessar breytingar strax á öllum þeim stöðum þar sem vísað er í brotið á vefnum. Þess vegna veita brot öflug og skilvirk leið til að endurnýta og stjórna miðlægum stillingum á vefsíðu. Með því að nota þau á áhrifaríkan hátt geturðu aukið lipurð verulega og hjálpað til við að draga úr kostnaði sem fylgir stjórnun á innihaldi vefsvæðisins.

Eftirfarandi mynd sýnir hvernig brot er hægt að nota til að miðstýra höfundarstillingu samskiptaeininga á e-verslunarsíðu.

![Mynd sem sýnir hvernig brot er hægt að nota til að miðstýra höfundarstillingu samskiptaeininga á netverslunarsíðu.](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a>Stofna brot

Þú getur annaðhvort búið til nýtt brot eða vistað fyrirliggjandi einingarstillingu sem brot.

### <a name="save-an-existing-module-configuration-as-a-fragment"></a>Vistaðu núverandi einingarstillingu sem brot

Til að umbreyta áður stilltri einingu í endurnýtanlegt brot í Commerce síðusmið skal fylgja þessum skrefum.

1. Opnaðu síðu eða sniðmát sem inniheldur eininguna sem þú vilt breyta í brot.
1. Á yfirlitssvæðinu vinstra megin eða beint á sjónrænum síðuhönnuði skal velja eininguna sem var skilgreind áður.
1. Veljið úrfellingarmerkið (**...**) við hliðina á heiti einingarinnar á annaðhvort yfirlitssvæðinu eða valda tækjastiku einingarinnar í sjónrænum síðuhönnuði. 
1. Veljið **Deila sem broti**. 
1. Í svargluggann **Vista sem brot** skal færa inn heiti fyrir síðubrotið.
1. Veldu **Í lagi** til að vista einingastillinguna sem brot sem hægt er að bæta við aðrar síður.
<!-- The following image shows how to save a module configuration as a fragment.-->
<!--![A screen capture of how to save a module configuration as a fragment.](./media/save-as-fragment.png)-->

### <a name="create-a-new-fragment"></a>Stofna nýtt brot

Til að búa til nýtt brot í vefsmið Commerce skal fylgja þessum skrefum.

1. Í stýriglugganum vinstra megin velurðu **Brot**.
1. Veljið **Nýtt**. Svargluggi fyrir **Nýtt brot** birtist sem sýnir allar tiltæku einingargerðirnar. Eins og áður var getið er hægt að búa til brot úr hvaða einingartegund sem er.
1. Veldu tegund einingar fyrir brotið þitt.

<!-- The following image shows where to create a new fragment.-->
<!-- ![A screen capture of where to create a new fragment.](./media/fragment-nav-menu.png)-->
> [!TIP]
> Með því að velja almenna gámaeiningagerð færðu mestan sveigjanleika þegar þú þarft að uppfæra og stilla brotið þitt seinna.

## <a name="add-remove-or-edit-fragments-on-a-page"></a>Bættu við, fjarlægðu eða breyttu brotum á síðu

Eftirfarandi aðferðir lýsa því hvernig á að bæta við, fjarlægja og breyta einingum.

### <a name="add-a-fragment"></a>Bæta við broti

Til að breyta broti milli rása í vefsmið Commerce skal fylgja þessum skrefum.

1. Á yfirlitssvæðinu vinstra megin eða beint á sjónrænum síðuhönnuði skal velja gám eða hólf þar sem bæta á undireiningunum við.
1. Veljið úrfellingarmerkið (**...**) við hliðina á heiti gámsins eða hólfsins.  Ef sjónrænn síðuhönnuður er notaður, skal velja plústáknið (**+**).  
1. Veljið **Bæta við broti**.
    <!-- ![A screen capture of how to add an existing fragment to a slot or container.](./media/add-fragment.png)-->
 
    > [!NOTE]
    > Ef geymirinn eða hólfið styður ekki nýjar undireiningar er valkosturinn **Bæta broti** ekki tiltækur.
    
1. Í svarglugganum **Velja brot** skal leita að og velja brot til að bæta við. Ef engin tiltæk brot eru tilgreind gætirðu fyrst þurft að búa til brot úr einingagerð sem valinn gámur eða hólf styður.
1. Veldu brotið sem þú vilt til að bæta því við gám eða hólf á síðunni þinni.
<!--    ![A screen capture of the fragment picker modal window.](./media/fragment-picker.png)-->

> [!NOTE]
> Einingarnar sem eru leyfðar í gámi eða hólfi eru skilgreindar af sniðmáti síðunnar eða eigin skilgreiningum eininganna.

### <a name="remove-a-fragment"></a>Fjarlægja brot

Til að fjarlægja brot úr hófli eða gámi á síðu í Commerce síðusmíð skal fylgja þessum skrefum.

1. Á yfirlitssvæðinu vinstra megin skal velja úrfellingarmerkið (**...**) við hliðina á heiti brotsins sem á að fjarlægja og síðan velja ruslakörfutáknið.  Annars er hægt að velja brotið í sjónrænum síðuhönnuði og velja ruslakörfutákni í tækjastiku brotsins.
1. Þegar þú færð kvaðningu um að staðfesta að þú viljir fjarlægja brotið skaltu velja **Í lagi**.

> [!NOTE]
> Þegar þú fjarlægir brot af síðu fjarlægirðu bara tilvísunina til þess af þeirri síðu. Þú eyðir brotinu **ekki** af vefsvæðinu. Til að eyða brotum af vefsvæðinu verðurðu að nota notendaviðmót brotaskoðara. Þú getur eingöngu eytt brotum af síðu ef ekki er vísað í þau af síðum, sniðmátum eða öðrum brotum.

### <a name="edit-a-fragment"></a>Breyta broti

Til að breyta brotum verður þú að nota brotaritilsviðmótið. Þessi takmörkun er samkvæmt hönnuninni. Hún hjálpar til við að tryggja að höfundar rugla ekki saman ferlinu við að breyta einingunum fyrir ákveðna síðu og því að breyta brotum sem hægt er að deila á margar síður.

Til að breyta broti milli rása í vefsmið Commerce skal fylgja þessum skrefum.

1. Í stýriglugganum vinstra megin velurðu **Brot**.
1. Undir **Brot** velurðu brotið sem á að breyta.
1. Breyttu einingareiginleikum og uppbyggingu brotsins eins og þú vilt. Ferlið líkist ferlinu við að breyta einingum er breytt á blaðsíðu ritstjórans.

Þú getur einnig breytt broti með því að velja það á síðu, í sniðmáti eða í foreldrabroti og síðan velja **Breyta broti** í eiginleikaglugganum til hægri.

### <a name="rename-a-fragment"></a>Endurnefna brot

Fylgdu þessum skrefum til að endurnefna núverandi brot í vefsvæðisgerð.

1. Í vinstri yfirlitsrúðunni, veldu **Brot**.
1. Veldu brotaheiti brotsins sem þú vilt endurnefna.
1. Veldu **Breyta** til að byrja að breyta brotinu. Athugaðu að þú getur ekki breytt broti ef einhver annar er þegar að breyta brotinu.
1. Í brotaeiginleikarúðunni skaltu velja pennatáknið við hliðina á brotaheitinu.
1. Breyttu nafni brotsins eftir þörfum.
1. Veldu gátmerkið til að staðfesta nafnbreytinguna.
1. Veldu **Ljúka við breytingar**.

Þú getur endurnefna brot eftir að það er búið til með því að breyta því og velja síðan pennatáknið við hliðina á brotsheitinu í eignarúðunni.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir sniðmát og útlit](templates-layouts-overview.md)

[Vinna með sniðmát](work-with-templates.md)

[Vinna með forstillt útlit](work-with-layouts.md)

[Vinna með birtingarhópa](publish-groups.md)

[Skoðaðu útgáfuferil til að snúa síðum og brotum til baka](version-history-revert.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
