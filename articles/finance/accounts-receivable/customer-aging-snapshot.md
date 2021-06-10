---
title: Aldursgreiningarmynd viðskiptavinar
description: Í þessu efnisatriði er að finna upplýsingar um aldursgreiningarmynd viðskiptavinar. Aldursgreiningarmynd reiknar út aldursgreinda stöður fyrir hóp viðskiptavina á einum tímapunkti.
author: JodiChristiansen
ms.date: 05/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-05-05
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: b88d3fe97d14d3e2f766367de501148063582000
ms.sourcegitcommit: 16376a301a0f121f384d77f9976638f701f8e88e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/28/2021
ms.locfileid: "6123363"
---
# <a name="customer-aging-snapshots"></a>Aldursgreiningarmynd viðskiptavinar

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er að finna upplýsingar um aldursgreiningarmynd viðskiptavinar. Aldursgreiningarmynd reiknar út aldursgreinda stöður fyrir hóp viðskiptavina á einum tímapunkti. Hægt er að stofna færslur aldursgreiningarmynda fyrir alla viðskiptavini eða fyrir viðskiptavini í viðskiptavinahóp.

Upplýsingar úr aldursgreiningarmyndum eru sýndar á listasíðunni **Aldursgreindar stöður** og á síðunni **Innheimtur**. Það verður að stofna aldursgreiningarmynd áður en hægt er að nota listasíðuna **Aldursgreindar stöður**. Listasíðan sýnir aðeins viðskiptavini sem aldursgreiningarmynd hefur verið stofnuð fyrir.

Vinnusvæðið **Skuldir og innheimta viðskiptavinar** sýnir einnig aldursgreiningu viðskiptavinar. Frekari upplýsingar er að finna í [Skulda- og innheimtuumsjón Power BI Efni](credit-collections-power-bi.md).

> [!NOTE]
> Til að draga úr þeim tíma sem þarf til að búa til aldursgreiningarmynd skal kveikja á eiginleikanum **Aukin afköst við aldursgreiningu viðskiptavinar** á vinnusvæðinu **Eiginleikastjórnun**. Notið hins vegar ekki viðskiptavinahópa þegar kveikt er á þessum eiginleika. Ef viðskiptavinahópur er valinn mun eiginleikinn ekki virka, en enn verður hægt að búa til aldursgreiningarmynd.

Þegar aldursgreiningarmynd viðskiptavinar er búin til skal nota eftirfarandi reiti til að færa inn upplýsingar um hann:

- **Skilgreining aldurstímabils** – Veljið skilgreiningu aldurstímabils fyrir aldursgreiningarmyndina. Hægt er að hafa eina aldursgreiningarmynd fyrir hverja skilgreiningu aldurstímabils. Aldursgreiningarmyndin og skilgreining aldurstímabilsins þarf að búa til hvort í sínu lagi.
- **Kenni hóps** – Þessi reitur er valfrjáls. Hægt er að nota hóp til að skilgreina safn viðskiptavina sem á að vinna úr í aldursgreiningarmyndinni. Ef viðskiptavinahópur er valinn í þessum reit verður aldursgreiningarmynd búin til eingöngu fyrir viðskiptavinalykla sem eru hluti af þeim viðskiptavinahópi. Valinn viðskiptavinahópur verður að vera af gerðinni **Aldursgreningarmynd**. Ef þessi reitur er skilinn eftir auður verður aldursgreiningarmynd búin til fyrir alla viðskiptavinalykla.

    > [!NOTE]
    > Ef kveikt er á **Aukin afköst við aldursgreiningu viðskiptavinar** skal ekki velja viðskiptavinahóp.

- **Skilyrði** – Aldursgreiningarmyndin mun eldast út frá dagsetningunni sem er valin:

    - **Færsludagsetning** – Hver færsla er aldursgreind út frá færsludagsetningu hennar.
    - **Gjalddagi** – Hver færsla er aldursgreind út frá gjalddaga hennar.
    - **Dagsetning skjals** – Hver færsla er aldursgreind út frá dagsetningu skjalsins.

- **Aldursgreining frá og með** – Veljið dagsetninguna sem á að nota í reitnum **Núgildandi dagsetning** fyrir aldursgreiningarmyndina. Aldursgreiningartímabil eru síðan reiknuð út frá þeirri dagsetningu. 

    - **Dagurinn í dag** - Nota kerfisdagsetningu. Veljið þennan valkost ef vinnsla er sett upp til að keyra í endurtekinni runu. Síðan, í hvert skipti sem runan er keyrð, er notuð kerfisdagsetning þeirrar keyrslu.
    - **Valinn dagsetning** – Nota dagsetningu sem þú tilgreinir. Ef þessi valkostur er valinn þarf að færa inn dagsetningu aldursgreiningar.

    Til dæmis er núverandi aldurstímabil 30 dagar. Ef valið er **Dagurinn í dag** í þessum reit, hefst núverandi aldursgreiningartímabil á deginum í dag og felur þá í sér 29 dagana á undan. Ef valið er **Valin dagsetning** og færð er inn dagsetning, hefst núverandi aldursgreiningartímabil á tilgreindum degi og felur þá í sér 29 dagana á undan.

- **Uppfæra innheimtustöðu** – Stillið þennan valkost á **Já** til að uppfæra innheimtustöðu færslnanna á síðunni **Innheimtur** úr **Loforð um greiðslu** í **Loforð um greiðslu svikið** ef dagsetning aldursgreiningar kemur á eftir dagsetningunni í reitnum **Dagsetning greiðsluloforðs**. Stillið þennan valkost á **Nei** til að skilja innheimtustöðuna eftir óbreytta á síðunni **Innheimtur**.
- **Hafa með viðskiptavini með núllstöðu** – Stillið þennan valkost á **Já** til að hafa með alla viðskiptavini burtséð frá stöðu þeirra. Ef allir viðskiptavinir eru hafðir með er mælt með því að kveikja á eiginleikanum **Aukin afköst við aldursgreiningu viðskiptavinar** og að nota ekki viðskiptavinahópa. Stillið þennan valkost á **Nei** til að hafa eingöngu með viðskiptavini sem eru með stöðu. Þessi stilling hraðar afköstum vegna þess að viðskiptavinum sem ekki eru með stöðu er sleppt.
- **Fyrirtækjasvið** – Í flipanum **Fyrirtækjasvið** skal velja lögaðilana (fyrirtækin) sem hafa á með í aldursgreiningarmyndinni. Aðeins er hægt að velja lögaðila sem eru settir upp fyrir miðstýrðar greiðslur. Færslur frá völdum lögaðilum eru síðan hafðar með í aldursgreiningartímabilum fyrir viðskiptavini sem eru með sömu aðilakennin í öllum þessum lögaðilum. Upphæðir gjaldmiðils eru umreiknaðar í gjaldmiðil lögaðilans sem notandi er skráður inn á þegar hann býr til aldursgreiningarmyndina.

Mælt er með því að tímasetja þessa vinnslu til að keyra hana í runu.

> [!NOTE]
> Til að stuðla að auknum runuafköstum þegar aldursgreiningarmyndir eru búnar til skal færa inn númer í reitinn **Hámarksfjöldi runuverka** í flýtiflipanum **Sjálfgefnar innheimtur** í flipanum **Innheimtur** á síðunni **Færibreytur viðskiptakrafa**. Í reitnum **Aldursgreina stöður viðskiptavina** er mælt með að byrja á sjálfgefna gildinu **100** og síðan leiðrétta gildið til að hámarka vinnslu fyrir kringumstæðurnar.

