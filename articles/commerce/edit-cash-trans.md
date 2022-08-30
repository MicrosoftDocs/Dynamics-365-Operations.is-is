---
title: Breyta og endurskoða færslur staðgreiðslu við afhendingu og stjórnun reiðufjár
description: Þessi grein fjallar um hvernig á að breyta og endurskoða færslur staðgreiðslu við afhendingu og stjórnun reiðufjár í Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.industry: Retail
ms.openlocfilehash: 22a0f76b6797e1051af6a7f3069f79c3be832d46
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283723"
---
# <a name="edit-and-audit-cash-and-carry-and-cash-management-transactions"></a>Breyta og endurskoða færslur staðgreiðslu við afhendingu og stjórnun reiðufjár

[!include [banner](../includes/banner.md)]

Þessi grein fjallar um hvernig á að breyta og endurskoða færslur staðgreiðslu við afhendingu og stjórnun reiðufjár í Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Dynamics 365 Commerce-viðskiptavinir nota bæði forrit fyrir sölustað frá fyrsta aðila og forrit fyrir sölustað frá þriðja aðila. Þegar forrit sölustaðar frá fyrsta aðila er notað eru færslur verslunar teknar inn í Commerce Headquarters úr rásunum með runuvinnslu. Þegar notuð eru forrit frá þriðju aðilum eru færslurnar teknar inn í Commerce Headquarters með samþættingu. Þegar færslurnar hafa verið teknar inn í Commerce Headquarters verður að framkvæma samræmisathugun í báðum tilvikum. Þetta ferli keyrir margar villuleitir á færslunum og aðeins færslur sem tekst að villuleita í eru teknar inn í uppgjörið til að hægt sé að birta færslurnar í Commerce Headquarters.

Færslur Commerce standast mögulega ekki villuleit af ýmsum ástæðum. Villa í samþættingarkóðanum eða söluforritinu getur valdið ósamkvæmum gögnum. Einnig getur notandavilla valdið ósamkvæmum gögnum. Þegar notandi t.d. eyðir afurð eftir að hún hefur verið samstillt við rásina eða notandi lokar fjárhagstímabili án þess að bóka færslur fyrir viðkomandi tímabil. Þrátt fyrir að slíkar færslur séu merktar og útilokaðar frá uppgjörunum geta færslurnar truflað daglegt bókunarferli viðskiptavinar í fjárhag. Í Commerce er hægt að breyta færslum sem standast ekki villuleit á meðan unnið er að endurskoðun á öllum breytingunum.

## <a name="edit-transactions"></a>Breyta færslum

Í Commerce-útgáfu 10.0.5 er aðeins hægt að breyta staðgreiddum færslum eins og sölu- og skilafærslum. Ekki er hægt að breyta pöntunum viðskiptavina og pöntunum á netinu. Í Commerce-útgáfu 10.0.6 og nýrri útgáfum er einnig hægt að breyta reiðufjárstjórnunarfærslum.

Fylgja skal eftirfarandi skrefum til að breyta pöntunarfærslum í Commerce Headquarters.

1. Setjið upp [Microsoft Dynamics Office Add-in](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview).
1. Opnið vinnusvæðið **Fjármál verslunar** í Commerce Headquarters. Reiturinn **Bilanir við villuleit færslu** sýnir forsíað yfirlit færslusíðunnar sem stóðst ekki eina eða fleiri villuleitarreglur.
1. Opnið færslusíðuna, veljið færsluna sem stóðst ekki villuleit, því næst **Office-innbót** og síðan **Breyta valinni færslu**. Excel-skrá með upplýsingum um valda færslu opnast. Þessi skrá inniheldur eftirfarandi vinnublöð:

    - **Línur** – Þetta vinnublað er með haus og afurðarlínur og tengd gögn fyrir færsluna.
    - **Greiðslur** – Þetta vinnublað er með upplýsingar um greiðslulínur fyrir færsluna.
    - **Afslættir** – Þetta vinnublað er með afsláttartengdar upplýsingar fyrir færsluna.
    - **Skattar** – Þetta vinnublað er með upplýsingar um skatt sem tengist færslunni.
    - **Gjöld** – Þetta vinnublað er með gjaldtengdar upplýsingar fyrir færsluna.

1. Í Excel-skránni er viðeigandi reitum breytt og gögnunum svo hlaðið aftur upp í Commerce Headquarters með birtingaraðgerð Excel-innbótarinnar í Dynamics. Breytingarnar koma fram í kerfinu þegar búið er að birta gögnin. Meðan á birtingu stendur fer engin villuleit fram á breytingunum sem notendur gera.
1. Hægt er að skoða alla færsluslóð breytinganna með því að velja **Skoða slóð endurskoðunar** í hausnum **Smásölufærsla** til að sjá breytingar á haus og í viðeigandi hluta og færslu á viðeigandi færslusíðu. Til dæmis verða allar breytingar sem tengjast sölulínum sýnilegar á síðunni **Sölufærslur** og allar breytingar sem tengjast greiðslum verða sýnilegar á síðunni **Greiðslufærslur**. Eftirfarandi upplýsingum um endurskoðun er haldið við fyrir breytingarnar:

    - Breytt dagsetning og tími
    - Svæði
    - Gamalt gildi
    - Nýtt gildi
    - Breytt af

1. Þegar breytingarnar hafa verið gerðar og birtar skal því næst keyra aftur **Villuleita í færslum verslunar** til að staðfesta að breytingarnar sem voru gerðar séu samræmdar og gildar.

> [!NOTE]
> Eingöngu er hægt að breyta færslum sem stóðust ekki villuleit. Þegar breyta á færslu sem staðist hefur villuleit skal breyta villuleitarstöðu færslunnar í **Villa** eða **Engin** og síðan birta breytinguna. Því næst er hægt að breyta gögnunum í hausnum eða undirskrám færslunnar og birta hausinn eða færslurnar.

## <a name="bulk-edit-transactions-that-are-linked-to-a-statement"></a>Breyta mörgum færslum í einu sem tengjast uppgjöri

Commerce-útgáfa 10.0.6 og nýrri útgáfur styðja breytingar á fjölda færslna í einu á uppgjörsstigi.

Fylgja skal eftirfarandi skrefum til að breyta mörgum færslum í einu sem tengjast uppgjöri í Commerce Headquarters.

1. Opnið síðuna **Uppgjör** og veljið uppgjörið sem inniheldur færslurnar sem skal breyta.
1. Veljið hnappinn **Opna í Microsoft Office**.
1. Veljið einn af eftirfarandi valkostum miðað við atriðin sem þarf að breyta:

    - **Breyta staðgreiddum færslum** – Þessi valkostur gerir notanda kleift að breyta öllum staðgreiddum færslum sem eru innifaldar í uppgjörinu. Eftirfarandi Excel-vinnublöð eru í boði:

        - **Færsla** – Þetta vinnublað er með allar upplýsingar á hausstigi fyrir sölufærslurnar.
        - **Sölufærsla** – Þetta vinnublað er með allar upplýsingar á línustigi fyrir sölufærslurnar.
        - **Greiðslufærslur** – Þetta vinnublað er með allar upplýsingar um greiðslulínurnar fyrir sölufærslurnar.
        - **Afsláttarfærslur** – Þetta vinnublað er með allar upplýsingar um afsláttarlínur fyrir sölufærslurnar.
        - **Skattfærslur** – Þetta vinnublað er með allar upplýsingar um skattlínur fyrir sölufærslurnar.
        - **Gjaldfærslur** – Þetta vinnublað er með allar upplýsingar um gjaldlínur fyrir sölufærslurnar.

    - **Breyta reiðufjárstjórnunarfærslum** – Þessi valkostur gerir notanda kleift að breyta öllum reiðufjárstjórnunarfærslum sem eru innifaldar í uppgjörinu. Eftirfarandi Excel-vinnublöð eru í boði:

        - **Færsla** – Þetta vinnublað er með allar upplýsingar á hausstigi fyrir reiðufjárstjórnunarfærslurnar.
        - **Greiðslufærslur á vörslureikningi** – Þetta vinnublað er með allar færsluupplýsingar um peningaflutning í banka.
        - **Greiðslufærslur í öryggisskáp** – Þetta vinnublað er með allar færsluupplýsingar um peningaflutning í öryggisskáp.
        - **Talning skiptimyntar** – Þetta vinnublað er með allar færsluupplýsingar um talningu skiptimyntar.
        - **Tekju-/útgjaldafærsla** – Þetta vinnublað er með allar upplýsingar um tekju/-útgjaldafærslulínu.
        - **Greiðslufærslur** - Þetta vinnublað er með allar greiðslutengdar upplýsingar fyrir aðgerðina **Greiða reikning** og tekju/-kostnaðarfærsluna.

1. Gerið breytingar á áskildum færslum.

    > [!NOTE]
    > Villuleit fer ekki fram þegar birtur er fjöldi færslna sem var breytt á sama tíma. Ganga þarf úr skugga um að breytingarnar sem gerðar eru séu réttar og að öll gögn á öllum vinnublöðunum samsvari sér. Þegar t.d. á að breyta færsludagsetningunni til að stjórna sviðsmyndum þar sem fjárhags- eða birgðahaldstíminn fyrir opnar færslur er lokaður verður að breyta dagsetningunni á öllum Excel-vinnublöðunum sem eru með dálkinn **Viðskiptadagsetning**. Til að staðfesta færslur eftir að þeim hefur verið breytt er hægt að smella á **Villuleita færslur aftur** á síðunni **Uppgjör**. Bíðið þar til villuleitarverkinu lýkur áður en yfirlitið er birt.

1. Þegar uppsöfnun hefur þegar verið gerð skal opna síðuna **Uppsafnaðar færslur** og velja **Endurgera XML-skrá sölupöntunar**.

## <a name="bulk-edit-transactions-that-arent-linked-to-a-statement"></a>Breyta mörgum færslum í einu sem tengjast ekki uppgjöri

Commerce-útgáfa 10.0.10 og nýrri útgáfur styðja breytingar á fjölda færslna sem stóðust ekki villuleit en eru ekki tengdar við uppgjör.

Fylgið eftirfarandi skrefum til að breyta mörgum færslum í einu sem ekki tengjast uppgjöri í Commerce Headquarters.

1. Opnið síðuna **Allar verslanir** og veljið verslunina sem skal breyta færslum fyrir.
1. Veljið hnappinn **Opna í Microsoft Office** og síðan **Breyta staðgreiddum færslum**.
1. Breytið áskildum færslum og birtið þær síðan.

## <a name="additional-resources"></a>Frekari upplýsingar

[Breyta og endurskoða netpöntun og ósamstilltar færslur pöntunar viðskiptavinar](edit-order-trans.md)

[Breyta fjárhagsvíddum fyrir smásölufærslur](edit-financial-dim.md)

[Stofna Excel-vinnubók til að breyta smásölufærslum](create-excel-edit.md)

[Bæta svæðum við Excel-vinnubók til að breyta smásölufærslum](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
