---
title: Breyta og endurskoða færslur smásöluverslunar
description: Þetta efnisatriði lýsir virkni til að breyta og endurskoða færslur smásöluverslunar.
author: josaw1
manager: AnnBe
ms.date: 10/14/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: f53573b8afb2003f6796930f5877185e533a4715
ms.sourcegitcommit: 92322167f57b66d2accc134aaf862e6b9931ec94
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/31/2019
ms.locfileid: "2693067"
---
# <a name="edit-and-audit-retail-store-transactions"></a>Breyta og endurskoða færslur smásöluverslunar

[!include [banner](includes/banner.md)]

[!include [banner](includes/preview-banner.md)]

Viðskiptavinir Dynamics 365 Retail nota forrit á sölustað bæði frá fyrsta og þriðja aðila. Með forriti sölustaðar frá fyrsta aðila eru færslur smásöluverslunar teknar inn í Retail Headquarters úr rásunum í gegnum runuvinnslu. Með forritum frá þriðju aðilum eru færslurnar teknar inn í Retail Headquarters í gegnum samþættingu. Í báðum tilvikum, þegar búið er að taka færslurnar inn í Retail Headquarters, þarf að framkvæma samræmisathugun sem keyrir margar villuleitir á færslunum þannig að aðeins færslur sem tekist hefur að villuleita verða teknar inn í uppgjörið sem á að bóka í Retail Headquarters. 

Smásölufærslur standast ekki villuleit af ýmsum ástæðum. Til dæmis gæti villa í samþættingarkóðanum eða villa í forriti sölustaðar valdið ósamkvæmum gögnum, eða notandavillu, eins og að eyða afurð eftir að hún hefur verið samstillt við rásina eða að loka fjárhagstímabili án þess að bóka smásölufærslur fyrir viðkomandi tímabil, sem getur valdið ósamkvæmum gögnum.

Þótt þessar færslur séu merktar og útilokaðar frá uppgjörunum geta þær truflað daglegt bókunarferli viðskiptavinar á smásölu í fjárhag.

Í Retail er hægt að breyta tilgreindum smásölufærslum sem stóðust ekki villuleit á meðan unnið er að endurskoðun á öllum breytingunum. 

## <a name="edit-and-audit-transactions"></a>Breyta og endurskoða færslur

Í Retail, útgáfu 10.0.5, er aðeins hægt að breyta staðgreiddum færslum eins og sölu- og skilafærslum. Breytingar á pöntunum viðskiptavinar eða netpöntunum eru ekki studdar. Í Retail, útgáfu 10.0.6, og nýrri er einnig stuðningur við breytingar á umsjón með reiðufjárfærslum.

1. Setja upp Dynamics Excel-innbótina.

2. Farið er á vinnusvæðið **Fjárhagur smásöluverslunar**. Reiturinn **Bilanir við villuleit í færslu** býður upp á forsíað yfirlit yfir færsluskjámynd Retail sem féll á einni eða fleiri villuleitarreglum.
 
3. Opnið skjámyndina. Smellið á færsluna sem stóðst ekki villuleit, á **Office-innbót** og svo á **Breyta valinni færslu**. Excel-skrá með upplýsingum um valda færslu opnast með eftirfarandi vinnublöðum:

    - Línur: Þetta vinnublað er með haus og afurðarlínur og tengd gögn fyrir færsluna.
    - Greiðslur: Þetta vinnublað er með upplýsingar um greiðslulínur fyrir færsluna.
    - Afslættir: Þetta vinnublað er með afsláttartengdar upplýsingar fyrir færsluna.
    - Skattar: Þetta vinnublað er með upplýsingar um skatt sem tengist færslunni.
    - Gjöld: Þetta vinnublað er með gjaldtengdar upplýsingar fyrir færsluna.

4. Í Excel-skránni er viðeigandi reitum breytt og gögnunum svo hlaðið aftur upp í Retail Headquarters með birtingaraðgerð Dynamics Excel-innbótarinnar. Breytingarnar koma fram í kerfinu þegar búið er að birta þær. Meðan á birtingu stendur fer engin villuleit fram á breytingunum sem notendur gera.

5. Hægt er að skoða alla færsluslóð breytinganna með því að smella á **Skoða slóð endurskoðunar** í hausnum **Smásölufærsla** til að sjá breytingar á haus og í viðeigandi hluta og færslu á viðeigandi færslusíðu. Til dæmis verða allar breytingar sem tengjast sölulínum sýnilegar á síðunni **Sölufærslur**, breytingar sem tengjast greiðslum verða sýnilegar á síðunni **Greiðslufærslur** o.s.frv. Upplýsingar um endurskoðun sem unnið er með fyrir breytingarnar eru eftirfarandi.

   - Breytt dagsetning og tími
   - Svæði 
   - Gamalt gildi
   - Nýtt gildi
   - Breytt af

6. Þegar breytingarnar hafa verið gerðar og birtar skal keyra valmöguleikann **Villuleita í færslum verslunar** aftur til að staðfesta að breytingarnar sem voru gerðar séu samræmdar og gildar.

> [!NOTE]
> Aðeins er hægt að breyta færslum sem stóðust ekki villuleit. Ef óskað er eftir að breyta færslum sem staðist hafa villuleit skal breyta villuleitarstöðu færslunnar sem á að breyta í **Villa** eða **Engin** og þá er hægt að breyta henni. 


## <a name="bulk-edit-transactions"></a>Fjöldabreytingafærslur

Í Retail, útgáfu 10.0.6, og nýrri er valkosturinn fyrir fjöldabreytingar á smásölufærslum á uppgjörsstigi studdur. 

1. Nota skal skref 1–3 hér að ofan í Excel-innbótinni til að opna færslur sem á að breyta.

2. Veljið einn valkostanna hér að neðan.

    - **Breyta staðgreiddum færslum**. Þessi valkostur gerir kleift að breyta öllum staðgreiddum færslum sem eru innifaldar í uppgjörinu. Eftirfarandi Excel-vinnublöð eru í boði.
    
       - **Færsla**: Þetta vinnublað er með allar upplýsingar á hausstigi fyrir sölufærslurnar.
       - **Sölufærsla**: Þetta vinnublað er með allar upplýsingar á línustigi fyrir sölufærslurnar.
       - **Greiðslufærslur**: Þetta vinnublað er með allar upplýsingar um greiðslulínurnar fyrir sölufærslurnar.
       - **Afsláttarfærslur**: Þetta vinnublað er með allar upplýsingar um afsláttarlínur fyrir sölufærslurnar.
       - **Skattfærslur**: Þetta vinnublað er með allar upplýsingar um skattlínur fyrir sölufærslurnar.
       - **Gjaldfærslur**: Þetta vinnublað er með allar upplýsingar um gjaldlínur fyrir sölufærslurnar.

    - **Breyta reiðufjárstjórnunarfærslum**. Þessi valkostur gerir kleift að breyta öllum reiðufjárstjórnunarfærslum sem eru innifaldar í uppgjörinu. Eftirfarandi Excel-vinnublöð eru í boði.
     
       - **Færsla**: Þetta vinnublað er með allar upplýsingar á hausstigi fyrir reiðufjárstjórnunarfærslurnar.
       - **Greiðslufærslur á vörslureikningi**: Þetta vinnublað er með allar færsluupplýsingar um peningaflutning í banka.
       - **Greiðslufærslur í öryggisskáp**: Þetta vinnublað er með allar færsluupplýsingar um peningaflutning í öryggisskáp.
       - **Talning skiptimyntar**: Þetta vinnublað er með allar færsluupplýsingar um talningu skiptimyntar.
       - **Tekju-/útgjaldafærsla**: Þetta vinnublað er með allar upplýsingar um tekju/-útgjaldafærslulínu.
       - **Greiðslufærslur**: Þetta vinnublað er með allar greiðslutengdar upplýsingar fyrir aðgerðina **Greiða reikning**, sem og tekju/-kostnaðarfærsluna.

3.  Villuleitir eru ekki framkvæmdar þegar fjöldabreyttar færslur eru birtar. Tryggja verður að allar breytingar séu réttar og að gögnin séu samsvarandi á öllum vinnublöðunum. Til dæmis, ef óskað er eftir að breyta færsludagsetningunni til að stjórna sviðsmyndum þar sem fjárhags- eða birgðahaldstíminn fyrir opnar smásölufærslur er lokaður þarf að breyta dagsetningunni á öllum Excel-vinnublöðunum sem eru með dálkinn **Viðskiptadagsetning**. Til að staðfesta færslur eftir að þeim hefur verið breytt er hægt að nota **Villuleita færslur aftur** á síðunni með **smásöluuppgjörunum**.
