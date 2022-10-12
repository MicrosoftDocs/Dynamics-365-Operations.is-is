---
title: Afurðasamanburðareiningar
description: Þessi grein lýsir vörusamanburðareiningum og hvernig á að útfæra þær þannig að viðskiptavinir geti gert vörusamanburð á Microsoft Dynamics 365 Commerce rafræn viðskipti vefsíður.
author: ashishmsft
ms.date: 10/03/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: 9ff45f3fbcc86b21f336d580582adef586417de4
ms.sourcegitcommit: 66b954827826706ea2ba00c2afd5d694ad92148d
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/03/2022
ms.locfileid: "9618386"
---
# <a name="product-comparison-modules"></a>Afurðasamanburðareiningar

[!include [banner](../includes/banner.md)]

Þessi grein lýsir vörusamanburðareiningum og hvernig á að útfæra þær þannig að viðskiptavinir geti gert vörusamanburð á Microsoft Dynamics 365 Commerce rafræn viðskipti vefsíður.

> [!NOTE]
> Vörusamanburður og vörusamanburðarhnappaeiningar eru fáanlegar frá og með Dynamics 365 Commerce útgáfu 10.0.29 útgáfu. Þeir geta verið notaðir fyrir bæði fyrirtæki til neytenda (B2C) og fyrirtæki til fyrirtækja (B2B) vefsíður.

Vörusamanburðarvirkni gerir kaupendum kleift að bera saman vöruupplýsingar á vörusamanburðarsíðu til að hjálpa þeim að taka betri kaupákvarðanir. Þessi virkni er stillt í Commerce site builder með því að nota vörusamanburðareininguna. Á vörulistasíðum (PLP), eins og flokkaniðurstöðum, leitarniðurstöðum og vörusöfnunarsíðum, geturðu stillt hnapp fyrir vörusamanburð sem gerir kaupendum kleift að bæta vörum við samanburðarbakka. Þessi virkni er stillt í vefsíðugerð með því að nota vörusamanburðarhnappseininguna, sem virkar eins og [flýtisýnareining](quick-view-module.md).

Þegar notendur síðunnar bæta við vörum til samanburðar með því að velja þær á vöruflísum birtist samanburðarbakki neðst á síðunni. Samanburðarbakkinn sýnir vörurnar sem kaupandinn er að bera saman ásamt stuttum sýnishornum af vörunum. Notendur vefsvæðis geta einnig bætt við vörum frá vöruupplýsingasíðum (PDP) og þeir geta bætt við sérstökum vöruafbrigðum til að bera saman við vörumeistara.

Eftir að viðskiptavinir hafa bætt nokkrum vörum við samanburðarbakkann geta þeir valið **Bera saman** til að vera vísað á vörusamanburðarsíðu. Vörusamanburðarsíðan sýnir vöruupplýsingar fyrir hverja valda vöru svo að viðskiptavinir geti borið saman myndir, verð, vörustærðir (stærð, stíll og litur), upplýsingar um samanlagðar einkunnir og aðrar vörueiginleikar.

Eftirfarandi mynd sýnir dæmi um bera saman vöruhnappinn, hnappinn fjarlægja úr samanburði, samanburðarbakkann og vörusamanburðarsíðuna.

![Yfirlit yfir vörusamanburð sem sýnir samanburðarhnappinn fyrir vöru, hnappinn fjarlægja úr samanburði, samanburðarbakkaspjaldið og vörusamanburðarsíðuna.](./media/Product-Comparison-Overview.png)

> [!NOTE]
> - Vörusamanburðarsíðan ber saman sjálfgefið sett af vörueiginleikum og öllum eiginleikum sem hægt er að skoða á PDP fyrir tiltekna vöru.
> - Eiginleikar eins og afhendingarham, birgðahald og mælieiningu er ekki hægt að skoða á vörusamanburðarsíðu.
> - Viðskiptavinir geta bætt vörum úr mismunandi flokkum við samanburðarbakkann, að því gefnu að vörurnar séu úr sama vörulista.
> - Vörusamanburðarvirkni takmarkast eins og er við að bera saman vörur í einstökum vörulista. Notendur vefsvæðis geta ekki gert samanburð á vörulista.
> - Þú ættir að tryggja að **Gerðu mát viðskiptavinahlið** eign er hreinsuð fyrir allar einingar fyrir vörusamanburð.
> - Þú ættir að tryggja að skyndiminni á síðustigi sé óvirkt fyrir allar síður þar sem vörusamanburðareiningin er notuð. Þessar síður innihalda PDP, PLP og vörusamanburðarsíður. Fyrir frekari upplýsingar, sjá [Stilla skyndiminni síðu](e-commerce-extensibility/page-caching.md).

Eftirfarandi mynd sýnir dæmi um vörusamanburðarsíðu.

![Vörusamanburðarsíða.](./media/Product-Comparison-Page.png)

## <a name="add-the-product-comparison-module-to-a-new-product-comparison-page"></a>Bættu vörusamanburðareiningunni við nýja vörusamanburðarsíðu

Þú getur búið til sérstaka vörusamanburðarsíðu með því að bæta vörusamanburðareiningu við meginmál síðunnar. Auk þess að gera viðskiptavinum kleift að bera saman vöruupplýsingar um mismunandi vörur, geturðu stillt vörusamanburðareininguna til að gefa viðskiptavinum kost á að ganga fljótt frá kaupum sínum eftir að þeir bera saman vörur. Vörusamanburðareiningin inniheldur einnig **Tómur samanburður** rifa, þar sem þú getur bætt við efnisblokkareiningu sem lýsir tómu ástandi (til dæmis "Vörusamanburðurinn þinn er tómur").

Til að bæta vörusamanburðareiningu við nýja vörusamanburðarsíðu skaltu fylgja þessum skrefum.

1. Farðu í **Síður** og veldu **Ný** til að búa til nýja síðu.
1. Í **Búðu til nýja síðu** svargluggi, undir **Nafn síðu**, sláðu inn viðeigandi síðuheiti (til dæmis, **Vörusamanburður**), og veldu síðan **Næst**.
1. Undir **Veldu sniðmát**, veldu viðeigandi sniðmát (til dæmis sniðmátið sem er notað af sjálfgefna flokkasíðunni þinni) og veldu síðan **Næst**.
1. Undir **Veldu skipulag**, veldu síðuútlit (til dæmis, **Sveigjanlegt skipulag**), og veldu síðan **Næst**.
1. Undir **Farið yfir og klárað**, skoðaðu stillingar síðunnar. Ef þú verður að breyta síðuupplýsingunum skaltu velja **Til baka**. Ef síðuupplýsingarnar eru réttar skaltu velja **Búa til síðu**.
1. Í **Aðal rauf**, veldu sporbaug (**...**), og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu **Ílát** mát og veldu síðan **Allt í lagi**.
1. Í **Ílát** rauf, veldu sporbaug (**...**), og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu **Vörusamanburður** mát og veldu síðan **Allt í lagi**.
1. Í **Hnappur fyrir skyndiskoðun** rauf, veldu sporbaug (**...**), og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu **Vara fljótt útsýni** mát og veldu síðan **Allt í lagi**.
1. Í eiginleikarúðunni til hægri skaltu stilla **Vara fljótt útsýni** mát eiginleika.
1. Í **Tómur samanburður** rauf, veldu sporbaug (**...**), og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu **Efnisblokk** mát og veldu síðan **Allt í lagi**.
1. Í eiginleikarúðunni til hægri skaltu stilla **Efnisblokk** mát eiginleika. 
1. Veldu **Vista** og veldu síðan **Forskoðun** til að forskoða síðuna.
1. Veldu **Ljúka við breytingar** til að athuga á síðunni og veldu síðan **Birta** til að birta hana.

Eftirfarandi mynd sýnir dæmi um tóma samanburðarsíðu í vefsíðugerð.

![Vörusamanburðareining.](./media/Product-comparison-module.png)

## <a name="add-a-product-comparison-button-to-product-tiles-on-search-and-category-results-pages"></a>Bættu vörusamanburðarhnappi við vöruflísar á leitar- og flokkaniðurstöðusíðum

Vörusamanburðarhnappurinn gerir notendum kleift að bæta vöru fljótt við samanburðarbakkann þegar þeir skoða vörur á listasíðu. Þeir geta bætt einni eða fleiri vörum við samanburðarbakkann af listasíðu án þess að þurfa að fara í PDP.

Vörusamanburðarhnappurinn er studdur af vörusafninu, leitarniðurstöðum og PDP-kaupakassaeiningum.

Til að bæta vörusamanburðarhnappi við vöruflísar á leitar- og flokkaniðurstöðusíðum skaltu fylgja þessum skrefum.

1. Í Site Builder, farðu á **Síður**, og opnaðu flokkasíðuna sem þú vilt bæta vörusamanburðarhnappi við.
1. Í **Aðal rauf**, veldu sporbaug (**...**), og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu **Leitarniðurstöður** mát og veldu síðan **Allt í lagi**.
1. Í **Vörusamanburðarhnappur** rifa á **Leitarniðurstöður** mát, veldu sporbaug (**...**), og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu **Vörusamanburðarhnappur** mát og veldu síðan **Allt í lagi**.
1. Í eiginleikarúðunni til hægri skaltu stilla **Vörusamanburðarhnappur** mát eiginleika.
1. Veldu **Vista** og veldu síðan **Forskoðun** til að forskoða síðuna.
1. Veldu **Ljúka við breytingar** til að athuga á síðunni og veldu síðan **Birta** til að birta hana.

## <a name="add-a-product-comparison-preview-panel-module-to-pages-on-your-website"></a>Bættu við forskoðunarborðseiningu vörusamanburðar við síður á vefsíðunni þinni

Forskoðunareining fyrir vörusamanburð veitir viðskiptavinum þínum möguleika á að skoða vörur sem þeir bæta við eða fjarlægja úr samanburðinum. Forskoðunarspjaldið býður einnig upp á möguleika til að fletta beint á samanburðarsíðuna eða hreinsa allan vörulistann. 

Við mælum með því að þú kveikir á forskoðunarspjaldinu á öllum síðum sem hafa **Vörusamanburðarhnappur** virkt. Hægt er að bæta einingunni við **Vörusamanburðarhnappur** sem rauf, eða það er hægt að nota það sem sjálfstæða einingu sem þú getur stillt á hvaða síðu sem er, jafnvel þegar það er engin virkni til að bæta við eða fjarlægja vörur til að bera saman. 

Þú verður að bæta forskoðunarborðseiningunni fyrir vörusamanburð handvirkt á síðu. Þú ættir aðeins að bæta við einni forskoðunarborðseiningu á síðu. Ef þú bætir mörgum tilfellum af einingunni á síðu, verður fyrsta einingin sýnd og restin verður hunsuð.

![Forskoðunarspjald fyrir vörusamanburð](./media/product-comparison-preview-panel-2.png)

Ef þú tilgreinir vörusamanburðarmörk hefurðu möguleika á að virkja gráa staðgengla á forskoðunarspjaldinu sem gefa til kynna hversu mörgum fleiri vörum er hægt að bæta við samanburðinn. Gráum staðgengjum er skipt út fyrir vörur þegar þeim er bætt við samanburðinn. Til að stilla vörusamanburðarmörk og virkja gráa staðgengla, í vefsvæðisgerð, farðu á **Vefstillingar > Viðbætur**, og gerðu breytingar þínar í **Vörusamanburður** kafla. Uppsetningin verður notuð á öll forskoðunarspjöld fyrir allar síður. 


## <a name="specify-the-maximum-number-of-products-to-show-in-the-comparison-tray"></a>Tilgreindu hámarksfjölda vara til að sýna í samanburðarbakkanum

Þú getur tilgreint hámarksfjölda vara til að sýna í samanburðarbakkanum með því að fara á **Vefstillingar \> Framlengingar** í síðugerð. Þú getur stillt aðskilin hámarksmörk fyrir skjáborð og farsíma/spjaldtölvu. Sjálfgefið er að engin takmörk séu framfylgt ef engin hámarksmörk eru skilgreind.

> [!NOTE]
> Til að fá sem besta vafraupplifun mælum við með að þú stillir hámarksfjölda vara í samanburðarbakkanum á **2** fyrir farsímaútsýnina og **4** fyrir skjáborðið til að draga úr magni láréttrar skrununar sem þarf.

Til að tilgreina hámarksfjölda vara í samanburðarbakkanum skaltu fylgja þessum skrefum.

1. Í Site Builder, farðu á **Vefstillingar \> Framlengingar**.
1. Fyrir **Vörur í samanburðarmörkum - borðtæki** eign, sláðu inn hámarksfjölda vara sem ætti að sýna í samanburðarbakkanum fyrir skjáborðsútsýni.
1. Fyrir **Vörur í samanburðarmörkum - farsímar og spjaldtölvur** eign, sláðu inn hámarksfjölda vara sem ætti að sýna í samanburðarbakkanum fyrir farsíma- og spjaldtölvuútsýni.
1. Veldu á skipanastikunni **Vista og birta**.

![Vefstillingar til að takmarka vörur í samanburðarbakkanum.](./media/Site-settings-to-limit-products-in-comparison-tray.png)
