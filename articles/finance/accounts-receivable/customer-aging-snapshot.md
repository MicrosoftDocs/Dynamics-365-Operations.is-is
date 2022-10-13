---
title: Aldursgreiningarmynd viðskiptavinar
description: Þessi grein veitir upplýsingar um skyndimyndir um öldrun viðskiptavina. Aldursgreiningarmynd reiknar út aldursgreinda stöður fyrir hóp viðskiptavina á einum tímapunkti.
author: JodiChristiansen
ms.date: 10/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2021-05-05
ms.dyn365.ops.version: 10.0.17
ms.search.form: ''
ms.openlocfilehash: 88145cdccfe3f1d0d3de4e31dfa519b27df6550a
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/12/2022
ms.locfileid: "9643686"
---
# <a name="customer-aging-snapshots"></a>Aldursgreiningarmynd viðskiptavinar

[!include [banner](../includes/banner.md)]

Þessi grein veitir upplýsingar um skyndimyndir um öldrun viðskiptavina. Aldursgreiningarmynd reiknar út aldursgreinda stöður fyrir hóp viðskiptavina á einum tímapunkti. Hægt er að stofna færslur aldursgreiningarmynda fyrir alla viðskiptavini eða fyrir viðskiptavini í viðskiptavinahóp.

Upplýsingar úr aldursgreiningarmyndum eru sýndar á listasíðunni **Aldursgreindar stöður** og á síðunni **Innheimtur**. Það verður að stofna aldursgreiningarmynd áður en hægt er að nota listasíðuna **Aldursgreindar stöður**. Listasíðan sýnir aðeins viðskiptavini sem aldursgreiningarmynd hefur verið stofnuð fyrir.

Vinnusvæðið **Skuldir og innheimta viðskiptavinar** sýnir einnig aldursgreiningu viðskiptavinar. Frekari upplýsingar er að finna í [Skulda- og innheimtuumsjón Power BI Efni](credit-collections-power-bi.md).

> [!NOTE]
> Til að draga úr þeim tíma sem þarf til að búa til öldrunarmynd skaltu kveikja á eftirfarandi eiginleikum í **Eiginleikastjórnun** vinnusvæði: **Öldrunarárangur viðskiptavina**
> **Öldrunarárangur viðskiptavina með hópum viðskiptavina**  
> Með báða eiginleikana virka, **Viðskiptavinalaugar** er hægt að nota þegar öldrunarmyndin er búin til. 

Þegar aldursgreiningarmynd viðskiptavinar er búin til skal nota eftirfarandi reiti til að færa inn upplýsingar um hann:

- **Skilgreining aldurstímabils** – Veljið skilgreiningu aldurstímabils fyrir aldursgreiningarmyndina. Hægt er að hafa eina aldursgreiningarmynd fyrir hverja skilgreiningu aldurstímabils. Aldursgreiningarmyndin og skilgreining aldurstímabilsins þarf að búa til hvort í sínu lagi.
- **Kenni hóps** – Þessi reitur er valfrjáls. Hægt er að nota hóp til að skilgreina safn viðskiptavina sem á að vinna úr í aldursgreiningarmyndinni. Ef viðskiptavinahópur er valinn í þessum reit verður aldursgreiningarmynd búin til eingöngu fyrir viðskiptavinalykla sem eru hluti af þeim viðskiptavinahópi. Valinn viðskiptavinahópur verður að vera af gerðinni **Aldursgreningarmynd**. Ef þessi reitur er skilinn eftir auður verður aldursgreiningarmynd búin til fyrir alla viðskiptavinalykla.


- **Skilyrði** – Aldursgreiningarmyndin mun eldast út frá dagsetningunni sem er valin:

    - **Færsludagsetning** – Hver færsla er aldursgreind út frá færsludagsetningu hennar.
    - **Gjalddagi** – Hver færsla er aldursgreind út frá gjalddaga hennar.
    - **Dagsetning skjals** – Hver færsla er aldursgreind út frá dagsetningu skjalsins.

- **Aldursgreining frá og með** – Veljið dagsetninguna sem á að nota í reitnum **Núgildandi dagsetning** fyrir aldursgreiningarmyndina. Aldursgreiningartímabil eru síðan reiknuð út frá þeirri dagsetningu. 

    - **Dagurinn í dag** - Nota kerfisdagsetningu. Veljið þennan valkost ef vinnsla er sett upp til að keyra í endurtekinni runu. Síðan, í hvert skipti sem runan er keyrð, er notuð kerfisdagsetning þeirrar keyrslu.
    - **Valinn dagsetning** – Nota dagsetningu sem þú tilgreinir. Ef þessi valkostur er valinn þarf að færa inn dagsetningu aldursgreiningar.

   Til dæmis er núverandi aldurstímabil 30 dagar. Ef valið er **Dagurinn í dag** í þessum reit, hefst núverandi aldursgreiningartímabil á deginum í dag og felur þá í sér 29 dagana á undan. Ef valið er **Valin dagsetning** og færð er inn dagsetning, hefst núverandi aldursgreiningartímabil á tilgreindum degi og felur þá í sér 29 dagana á undan.

- **Uppfæra innheimtustöðu** – Stillið þennan valkost á **Já** til að uppfæra innheimtustöðu færslnanna á síðunni **Innheimtur** úr **Loforð um greiðslu** í **Loforð um greiðslu svikið** ef dagsetning aldursgreiningar kemur á eftir dagsetningunni í reitnum **Dagsetning greiðsluloforðs**. Stillið þennan valkost á **Nei** til að skilja innheimtustöðuna eftir óbreytta á síðunni **Innheimtur**.
- **Hafa með viðskiptavini með núllstöðu** – Stillið þennan valkost á **Já** til að hafa með alla viðskiptavini burtséð frá stöðu þeirra. Ef þú tekur alla viðskiptavini með mælum við með að þú kveikir á báðum **Öldrunarárangur viðskiptavina** og **Öldrunarárangur viðskiptavina með hópum viðskiptavina** eiginleikar. Stillið þennan valkost á **Nei** til að hafa eingöngu með viðskiptavini sem eru með stöðu. Þessi stilling mun hjálpa til við að flýta fyrir afköstum, vegna þess að viðskiptavinum sem ekki eru með inneign er sleppt.
- **Farðu framhjá útreikningum á lánamörkum við öldrun** - Ef þessi valkostur er stilltur á **Já** öldrunarferlið mun ekki endurreikna **Samtala fylgiseðils** magn, **Opin pöntun undirsamtala** upphæð og **Inneign í boði** fyrir hvern viðskiptavin. Þessar stöður eru sýndar á **Eldri jafnvægi** síðu, í staðreyndaboxinu undir **Lánamörk**. Til að fá hraðari frammistöðu á öldrunarferlinu skaltu stilla þennan valkost á **Já**. Stilltu það á **Nei** að endurreikna stöðuna þegar öldrunarferlið er keyrt. 
- **Fyrirtækjasvið** – Í flipanum **Fyrirtækjasvið** skal velja lögaðilana (fyrirtækin) sem hafa á með í aldursgreiningarmyndinni. Aðeins er hægt að velja lögaðila sem eru settir upp fyrir miðstýrðar greiðslur. Færslur frá völdum lögaðilum eru síðan hafðar með í aldursgreiningartímabilum fyrir viðskiptavini sem eru með sömu aðilakennin í öllum þessum lögaðilum. Upphæðir gjaldmiðils eru umreiknaðar í gjaldmiðil lögaðilans sem notandi er skráður inn á þegar hann býr til aldursgreiningarmyndina.

Mælt er með því að tímasetja þessa vinnslu til að keyra hana í runu.

> [!NOTE]
> Til að stuðla að auknum runuafköstum þegar aldursgreiningarmyndir eru búnar til skal færa inn númer í reitinn **Hámarksfjöldi runuverka** í flýtiflipanum **Sjálfgefnar innheimtur** í flipanum **Innheimtur** á síðunni **Færibreytur viðskiptakrafa**. Í **Aldursstaða viðskiptavina** reit, mælum við með að þú byrjir með gildi á milli **12** og **20** og stilltu síðan gildið til að hámarka vinnslu fyrir aðstæður þínar. Við mælum ekki með því að setja þetta gildi hærra en **30** þar sem það mun hafa áhrif á frammistöðu. 

