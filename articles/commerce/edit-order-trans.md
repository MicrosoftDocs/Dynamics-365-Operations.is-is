---
title: Breyta og endurskoða netpöntun og ósamstilltum færslum pöntunar viðskiptavinar
description: Þessi grein lýsir því hvernig á að breyta og endurskoða netpöntun og ósamstilltar færslur pöntunar viðskiptavinar í Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: dac7ffe6d62aaea11f2f5af0476db446b091938b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287678"
---
# <a name="edit-and-audit-online-order-and-asynchronous-customer-order-transactions"></a>Breyta og endurskoða netpöntun og ósamstilltum færslum pöntunar viðskiptavinar

[!include [banner](../includes/banner.md)]

Þessi grein lýsir því hvernig á að breyta og endurskoða netpöntun og ósamstilltar færslur pöntunar viðskiptavinar í Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Stuðningi var bætt við Commerce-útgáfur 10.0.5 og 10.0.6 til að gera breytingar á staðgreiddum færslum (eins og sölu og vöruskilum) og reiðufjárstjórnunarfærslum (eins og skiptimyntarfærslum og að fjarlægja skiptimynt). Stuðningi var bætt við Commerce-útgáfu 10.0.7 fyrir breytingar á pöntunarfærslum á netinu og ósamstilltum pöntunum viðskiptavinar.

## <a name="edit-and-audit-order-transactions"></a>Breyta og endurskoða pöntunarfærslur

Fylgið eftirfarandi skrefum til að breyta og endurskoða pöntunarfærslur í Commerce Headquarters.

1. Setjið upp [Microsoft Dynamics Office Add-in](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview).
1. Opnið síðuna **Færibreytur smásölu** á flipanum **Pantanir viðskiptavinar** á flýtiflipanum **Pöntun**, tilgreinið biðkóða fyrir **Biðkóði fyrir villur við samstillingu pöntunar**.
1. Opnið vinnusvæðið **Fjármál verslunar**. Reitirnir **Samstillingarvillur í pöntunum á netinu** og **Samstillingarvillur í pöntunum viðskiptavina** birta yfirlit af síðu smásölufærslna sem þegar hefur verið síað. Hver breyting birtir færsluskrár þar sem samstilling á samsvarandi pöntunargerð tókst ekki.
1. Opnið annað hvort síðuna **Samstillingarvillur í pöntunum á netinu** eða síðuna **Samstillingarvillur í pöntunum viðskiptavina**. Smellið á skrá til að skoða villuupplýsingar. Flýtiflipinn **Staða samstillingar** veitir eftirfarandi upplýsingar um villuna:

    - Staða pöntunar í bið
    - Upplýsingar um pöntunarvillu
    - Breytt dagsetning og tími
    - Fjöldi tilrauna

1. Þegar villuupplýsingarnar tilgreina að lagfæra skuli skrána skal velja **Office-viðbót** og síðan **Breyta valinni færslu**. Excel-skrá með upplýsingum um valda færslu opnast.

    - Excel-skráin inniheldur eftirfarandi vinnublöð ef færslan sem var breytt er pöntunarfærsla á netinu:

        - **Færsla** – Þetta vinnublað er með hausupplýsingar fyrir færsluna.
        - **Sölufærsla** – Þetta vinnublað er með línuupplýsingar fyrir færsluna.
        - **Greiðslufærslur** – Þetta vinnublað er með upplýsingar um greiðslulínur fyrir færsluna.
        - **Afsláttarfærslur** – Þetta vinnublað er með afsláttartengdar upplýsingar fyrir færsluna.
        - **Skattafærslur** – Þetta vinnublað er með skatttengdar upplýsingar fyrir færsluna.
        - **Gjaldafærslur** – Þetta vinnublað er með gjaldtengdar upplýsingar fyrir færsluna.

    - Excel-skráin inniheldur eftirfarandi vinnublöð ef færslan sem var breytt er ósamstillt pöntun viðskiptavinar:

        - **Línur** – Þetta vinnublað er með haus- og línuupplýsingar fyrir færsluna.
        - **Greiðslur** – Þetta vinnublað er með upplýsingar um greiðslulínur fyrir færsluna.
        - **Afslættir** – Þetta vinnublað er með afsláttartengdar upplýsingar fyrir færsluna.
        - **Skattar** – Þetta vinnublað er með upplýsingar um skatt sem tengist færslunni.
        - **Gjöld** – Þetta vinnublað er með gjaldtengdar upplýsingar fyrir færsluna.

1. Opnið Excel-skrána, veljið svæðið **Staða pöntunar í bið**, sláið inn **Breyta** og birtið síðan breytinguna. Þannig er komið í veg fyrir að verkið **Samstilla pöntun** sem er í keyrslu í runustillingu sleppi þessari skrá við úrvinnslu.
1. Í Excel-skránni er viðeigandi reitum breytt og gögnunum svo hlaðið aftur upp í Commerce Headquarters með birtingaraðgerð Excel-innbótarinnar í Dynamics. Breytingarnar koma fram í kerfinu þegar búið er að birta gögnin. Meðan á birtingu stendur fer engin villuleit fram á breytingunum sem notendur gera.
1. Hægt er að skoða alla færsluslóð breytinganna með því að velja **Skoða slóð endurskoðunar** í hausnum **Smásölufærsla** til að sjá breytingar á haus og í viðeigandi hluta og færslu á viðeigandi færslusíðu. Til dæmis verða allar breytingar sem tengjast sölulínum sýnilegar á síðunni **Sölufærslur** og allar breytingar sem tengjast greiðslum verða sýnilegar á síðunni **Greiðslufærslur**. Eftirfarandi upplýsingum um endurskoðun er haldið við fyrir breytingarnar:

    - Breytt dagsetning og tími
    - Svæði
    - Gamalt gildi
    - Nýtt gildi
    - Breytt af

1. Þegar lokið er við að gera breytingar og þær hafa verið birtar skal smella á **Samstilla pöntun** til að hefja samstillingarferlið strax. Einnig er hægt að bíða eftir að samstillingarferlið sem er keyrt í runustillingu ljúki við að vinna úr færslunni.

Þegar samstillingu pantana er lokið eru þær sjálfgefið settar í biðstöðu, á grundvelli biðkóðans sem er skilgreindur í færibreytum Commerce. Áður en hægt er að vinna úr pöntununum fyrir uppfyllingu eða aðrar aðgerðir þarf að taka pantanirnar úr biðstöðu.

## <a name="additional-resources"></a>Frekari upplýsingar

[Breyta og endurskoða færslur staðgreiðslu við afhendingu og stjórnun reiðufjár](edit-cash-trans.md)

[Breyta fjárhagsvíddum fyrir smásölufærslur](edit-financial-dim.md)

[Stofna Excel-vinnubók til að breyta smásölufærslum](create-excel-edit.md)

[Bæta svæðum við Excel-vinnubók til að breyta smásölufærslum](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
