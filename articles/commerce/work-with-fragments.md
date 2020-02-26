---
title: Vinna með brot
description: Þetta efni lýsir því hvers vegna, hvenær og hvernig skuli nota brot í Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 01/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: retail
ms.author: phinneyridge
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f29046ded47ed9c49a2cc841aa7c1f6492b49aec
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/05/2020
ms.locfileid: "3026041"
---
# <a name="work-with-fragments"></a>Vinna með brot 


[!include [banner](includes/banner.md)]

Þetta efni lýsir því hvers vegna, hvenær og hvernig skuli nota brot í Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

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

Fylgdu þessum skrefum til að umbreyta áður uppsettri einingu í endurnýtanlegt brot.

1. Opnaðu síðu eða sniðmát sem inniheldur eininguna sem þú vilt breyta í brot.
1. Í útlínuglugganum til vinstri velurðu úrfellingarhnappinn (**...**) við hliðina á einingunni. 
1. Veldu **Deila sem broti**. 
1. Svargluggi birtist. Sláðu inn heiti og lýsigögn fyrir brotið.
1. Veldu **Í lagi** til að vista einingastillinguna sem brot sem hægt er að bæta við aðrar síður.

Eftirfarandi mynd sýnir hvernig vista má einingastillingu sem brot.

![Skjámynd um hvernig á að vista einingastillingu sem brot](./media/save-as-fragment.png)

### <a name="create-a-new-fragment"></a>Stofna nýtt brot

Fylgið eftirfarandi skrefum til að stofna nýtt brot.

1. Í stýriglugganum vinstra megin velurðu **Brot**.
1. Veljið **Nýtt síðubrot**. Gluggi birtist sem sýnir allar tiltækar gerðir eininga. Eins og áður var getið er hægt að búa til brot úr hvaða einingartegund sem er.
1. Veldu tegund einingar fyrir brotið þitt.

Eftirfarandi mynd sýnir hvar á að búa til nýtt brot.

![Skjámynd um hvar eigi að búa til nýtt brot](./media/fragment-nav-menu.png)

> [!TIP]
> Með því að velja almenna gámaeiningagerð færðu mestan sveigjanleika þegar þú þarft að uppfæra og stilla brotið þitt seinna.

## <a name="add-remove-or-edit-fragments-on-a-page"></a>Bættu við, fjarlægðu eða breyttu brotum á síðu

Eftirfarandi aðferðir lýsa því hvernig á að bæta við, fjarlægja og breyta einingum.

### <a name="add-a-fragment"></a>Bæta við broti

Til að bæta broti við síðu skaltu fylgja þessum skrefum.

1. Í útlínuglugganum til vinstri velurðu gám eða hólf sem hægt er að bæta undireiningum við.
1. Veldu úrfellingarhnappinn við hliðina á heiti gámsins eða hólfsins og velur síðan **Bæta við broti**. Svargluggi birtist.

    ![Skjámynd um hvernig bæta má núverandi broti við rauf eða ílát](./media/add-fragment.png)
 
    > [!NOTE]
    > Ef gámurinn eða hólfið styðja ekki nýjar undireiningar er valkosturinn **Bæta við broti** er ekki í boði.
    
1. Leitaðu að og veldu broti til að bæta við í valmyndinni. Ef engin tiltæk brot eru tilgreind gætirðu fyrst þurft að búa til brot úr einingagerð sem valinn gámur eða hólf styður.
1. Veldu brotið sem þú vilt til að bæta því við gám eða hólf á síðunni þinni.

    ![Skjámynd af staðfestingaglugga brotavals](./media/fragment-picker.png)

> [!NOTE]
> Einingarnar sem eru leyfðar í gámi eða hólfi eru skilgreindar af sniðmáti síðunnar eða eigin skilgreiningum eininganna.

### <a name="remove-a-fragment"></a>Fjarlægja brot

Til að fjarlægja brot úr hólfi eða gámi á síðu skaltu fylgja þessum skrefum.

1. Í útlínuglugganum til vinstri velurðu úrfellingarhnappinn við hliðina á heiti brotanna sem á að fjarlægja og síðan velurðu ruslatunnuhnappinn.
1. Þegar þú færð kvaðningu um að staðfesta að þú viljir fjarlægja brotið skaltu velja **Í lagi**.

> [!NOTE]
> Þegar þú fjarlægir brot af síðu fjarlægirðu bara tilvísunina til þess af þeirri síðu. Þú eyðir brotinu **ekki** af vefsvæðinu. Til að eyða brotum af vefsvæðinu verðurðu að nota notendaviðmót brotaskoðara. Þú getur eingöngu eytt brotum af síðu ef ekki er vísað í þau af síðum, sniðmátum eða öðrum brotum.

### <a name="edit-a-fragment"></a>Breyta broti

Til að breyta brotum verður þú að nota brotaritilsviðmótið. Þessi takmörkun er samkvæmt hönnuninni. Hún hjálpar til við að tryggja að höfundar rugla ekki saman ferlinu við að breyta einingunum fyrir ákveðna síðu og því að breyta brotum sem hægt er að deila á margar síður.

Fylgið eftirfarandi skrefum til að breyta broti.

1. Í stýriglugganum vinstra megin velurðu **Brot**.
1. Undir **Brot** velurðu brotið sem á að breyta.
1. Breyttu einingareiginleikum og uppbyggingu brotsins eins og þú vilt. Ferlið líkist ferlinu við að breyta einingum er breytt á blaðsíðu ritstjórans.

Þú getur einnig breytt broti með því að velja það á síðu, í sniðmáti eða í foreldrabroti og síðan velja **Breyta broti** í eiginleikaglugganum til hægri.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir sniðmát og útlit](templates-layouts-overview.md)

[Vinna með sniðmát](work-with-templates.md)

[Vinna með forstillt útlit](work-with-layouts.md)

[Unnið með birta hópa](publish-groups.md)
