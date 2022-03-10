---
title: Áfyllingaraðferðir og magnbreyting
description: Í þessu efnisatriði er að finna upplýsingar um áfyllingaraðferðir í fínstillingu skipulagningar. Þar er einnig útskýrt hvernig margs konar pöntunarmagn fyrir afurð hefur áhrif á niðurstöðuna.
author: ChristianRytt
ms.date: 6/1/2021
ms.topic: article
ms.search.form: ReqGroup, ReqItemTable, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-06-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 017dabb46265769bf727056a9bf1a8c0cfdc99f6
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7567296"
---
# <a name="replenishment-methods-and-quantity-modification"></a>Áfyllingaraðferðir og magnbreyting

[!include [banner](../../includes/banner.md)]

Í þessu efnisatriði er að finna upplýsingar um áfyllingaraðferðir í fínstillingu skipulagningar. Þar er einnig útskýrt hvernig margs konar pöntunarmagn fyrir afurð hefur áhrif á niðurstöðuna.

Áfyllingaraðferðir eru einnig þekktar sem þekjuaðferðir og lotustærðaraðferðir.

## <a name="coverage-codes"></a>Þekjukóðar

Hægt er að stilla fínstillingu skipulagningar þannig að hún noti aðrar áfyllingaraðferðir. Áfyllingaraðferðir eru leið sem kerfið notar til að reikna út þarfir fyrir afurð. Áfyllingaraðferðir eru skilgreindar af þekjukóðum sem hægt er að setja upp í annaðhvort þekjuflokknum eða afurðinni.

Hægt er að nota eftirfarandi þekjukóða í fínstillingu skipulagningar:

- **Tímabil** – Áfyllingaraðferðin sameinar alla eftirspurn fyrir tímabil í eina pöntun fyrir afurðina. Pöntunin verður áætluð fyrir fyrsta dag tímabilsins og magn hennar mun uppfylla nettóþarfir á settu tímabili. Tímabilið hefst á fyrstu eftirspurn eftir afurðinni og nær yfir skilgreinda tímalengd. Næsta tímabil hefst með næstu þörfum eftir afurðinni. Þekjukóði *tímabilsins* er oft notaður fyrir ófyrirsjáanlega birgðanotkun, árstíðabundnar afurðir eða dýrar afurðir. Eftirfarandi skýringarmynd sýnir dæmi.

    ![Dæmi um notkun tímabilsþekjukóða.](./media/coverage-code-period.png "Dæmi um notkun tímabilsþekjukóða")

- **Þörf** – Í áfyllingaraðferðinni stofnar kerfið áætlaða innkaupa-, flutnings- eða framleiðslupöntun eftir þörfum afurðarinnar. Þessi aðferð er notuð fyrir dýrar afurðir þar sem eftirspurnin er breytileg. Þekjukóði *þarfa* er oft notaður í aðstæðum stillanlegrar afurðar eða framleiðslu eftir pöntun. Eftirfarandi skýringarmynd sýnir dæmi.

    ![Dæmi um notkun á þekjukóða þarfa.](./media/coverage-code-requirement.png "Dæmi um notkun á þekjukóða þarfa")

- **Lágm./Hám.** – Áfyllingaraðferðin byggir á birgðastöðunni. Hún skilgreinir áfyllingu birgða upp að tilteknu stigi þegar fyrirséð lagerstaða er undir tilteknum þröskuldi. Áfyllingarmagnið verður munurinn á milli hámarksstigs og spáðs stigs lagermagns. *Lágm./hám.* þekjukóðinn er oft notaður fyrir fyrirséða birgðanotkun, vinsælar afurðir eða ódýrari afurðir. Eftirfarandi skýringarmynd sýnir dæmi.

    ![Dæmi um notkun á þekjukóða lágm./hám.](./media/coverage-code-min-max.png "Dæmi um notkun á þekjukóða lágm./hám.")

- **Handvirkt** – Í áfyllingaraðferðinni stingur kerfið ekki upp á innkaupa-, flutnings- eða framleiðslupöntun fyrir afurðina. Í staðinn er skipuleggjandi afurðarinnar ábyrgur fyrir stofnun nauðsynlegra pantana vegna áfyllingar afurðar. *Handvirkur* þekjukóði er oft notaður fyrir afurðir þar sem áætlaðar pantanir myndaðar af kerfinu eru óþarfar.

## <a name="impact-of-the-order-quantity-from-default-order-settings"></a>Áhrif á pöntunarmagn úr sjálfgefnum pöntunarstillingum

Á síðunni **Sjálfgefin pöntunarstilling** fyrir losaða afurð er hægt að tilgreina hverja af eftirfarandi pöntunarstillingum í flýtiflipunum **Innkaupapöntun**, **Birgðir** og **Sölupöntun**. (Flýtiflipinn **Birgðir** er notaður fyrir bæði flutningspantanir og framleiðslupantanir.)

- **Margfeldi** – Áætlaðar pantanir verða margfeldi af þessu magni.

    Ef til dæmis reiturinn **Margfeldi** er stilltur á *5* getur pöntun verið fyrir magnið 5, 10, 15, 20 og svo framvegis.

- **Lágmarksmagn pöntunar** – Áætlaðar pantanir verða ekki minna en tilgreint gildi.

    Ef til dæmis reiturinn **Lágmarksmagn pöntunar** er stillt á *10* verður áætluð pöntun með magnið 10 stofnuð þótt aðeins magn upp á fjórir sé nauðsynlegt til að anna eftirspurn.

- **Hámarksmagn pöntunar** – Áætlaðar pantanir fara ekki yfir tiltekið gildi. Ef eftirspurnin er meiri en gildið í **Hámarksmagn pöntunar** verða stofnaðar margar áætlaðar pantanir til að anna henni.

    Ef til dæmis reiturinn **Hámarksmagn pöntunar** er stilltur á *100* og eftirspurnin er 450 verða stofnaðar fjórar áætlaðar pantanir fyrir magnið 100 og ein áætluð pöntun fyrir magnið 50.

## <a name="examples-of-replenishment-that-use-the-minmax-coverage-code"></a>Dæmi um áfyllingu sem notar hám./lágm. þekjukóði

Ef ekkert gildi er tilgreint í reitnum **Margfeldi** fyrir afurð á síðunni **Sjálfgefin pöntunarstilling** og ef notuð er *Hám./lágm.* áfyllingaraðferðin mun fínstilling skipulagningar fylla á birgðirnar upp að tiltekinni stöðu þegar spáð lagerstaða er undir tilteknum þröskuldi.

Ef skilgreint er meira en eitt magn fyrir afurð mun *Hám./lágm.* áfyllingaraðferðin breyta hegðun sinni og taka til greina gildið **Margfeldi**.

Með öðrum orðum mun fínstilling skipulagningar ennþá fylla á birgðirnar upp að skilgreindri hámarksstöðu þegar spáð lagerstaða er minni en skilgreind lágmarksstaða. Hinsvegar verður áfyllingarmagnið að vera margfeldi af gildinu **Margfeldi**.

Ef áfyllingarmagnið (munurinn á hámarksstöðu og spáðri lagerstöðu) er ekki margfeldi af skilgreindu margfeldismagni, notar fínstilling skipulagningar fyrsta mögulega gildið sem, ásamt spáðri lagerstöðu, verður undir hámarksstöðunni. Ef samtalan er minni en lágmarksstaðan notar fínstilling skipulagningar fyrsta gildið sem, ásamt spáðri lagerstöðu, verðu fyrir ofan hámarksstöðuna.

Eftirfarandi undirhlutar sýna dæmi um hvernig margfeldi af pöntunarmagni fyrir afurð hefur áhrif á niðurstöðuna fyrir *Lágm./hám.* áfyllingaraðferð.

### <a name="example-1"></a>Dæmi 1

Afurð er með eftirfarandi skilgreiningu:

- **Þekjukóði:** *Lágm./hám.*
- **Lágmark:** *15*
- **Hámark:** *22*
- **Margfalt:** *0*

Það eru 10 stykki á lager af afurðinni og það er engin önnur eftirspurn eða framboð.

Þegar aðaláætlanagerð er keyrð verður áætluð pöntun fyrir 12 stykkjum stofnuð til að fylla á birgðirnar upp í hámarksmagnið.

### <a name="example-2"></a>Dæmi 2

Afurð er með eftirfarandi skilgreiningu:

- **Þekjukóði:** *Lágm./hám.*
- **Lágmark:** *15*
- **Hámark:** *22*
- **Margfalt:** *5*

Það eru 10 stykki á lager af afurðinni og það er engin önnur eftirspurn eða framboð.

Þegar aðaláætlanagerð er keyrð verður áætluð pöntun upp á 10 stykki stofnuð (vegna þess að 15 stykki af áfyllingu ásamt 10 stykkjum af lagerbirgðum fara yfir hámarksmagnið).

### <a name="example-3"></a>Dæmi 3

Afurð er með eftirfarandi skilgreiningu:

- **Þekjukóði:** *Lágm./hám.*
- **Lágmark:** *21*
- **Hámark:** *24*
- **Margfalt:** *5*

Það eru 10 stykki á lager af afurðinni og það er engin önnur eftirspurn eða framboð.

Þegar aðaláætlanagerð er keyrð verður áætluð pöntun upp á 15 stykki stofnuð (vegna þess að 10 stykki af áfyllingu ásamt 10 stykkjum af lagerbirgðum fara undir lágmarksmagnið).

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
