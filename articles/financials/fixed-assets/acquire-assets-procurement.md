---
title: "Kaupa eignir með innkaupum"
description: "Þessi grein lýsir því hvernig hægt er að setja upp samþættingu á milli eigna og viðskiptaskulda til að búa sjálfkrafa til eignir úr innkaupapöntunum eða reikningum lánardrottins, eða bóka sjálfkrafa kaup og leiðréttingarfærslur kaupa fyrir eignir."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 3481
ms.assetid: d4e73a3f-633b-48b2-b8db-7a4a59a4d7ec
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 84e7e6eb17e5741a2984c570786a495864ffbc74
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="acquire-assets-through-procurement"></a>Kaupa eignir með innkaupum

[!include[banner](../includes/banner.md)]


Þessi grein lýsir því hvernig hægt er að setja upp samþættingu á milli eigna og viðskiptaskulda til að búa sjálfkrafa til eignir úr innkaupapöntunum eða reikningum lánardrottins, eða bóka sjálfkrafa kaup og leiðréttingarfærslur kaupa fyrir eignir.

 Eftirfarandi leiðir eru tiltækar til þess að samþætta eignir og viðskiptaskuldir og þú verður að nota sömu aðferðina fyrir allar eignir:
-   Stofna verður eign handvirkt áður en númeri eignar er bætt við línu í innkaupapöntun eða reikningi lánardrottins. Kaupvirðisfærsla er sjálfkrafa bókuð fyrir eignina þegar reikningur lánardrottins er bókaður. Þetta er sjálfgefin aðferð.
-   Stofna verður eign handvirkt áður en númeri eignar er bætt við línu í innkaupapöntun eða reikningi lánardrottins. Engin kaupfærsla er bókuð fyrir eignina þegar reikningurinn lánardrottins er bókaður.
-   eign er stofnuð sjálfkrafa þegar innhreyfingarskjal afurða er bókað eða reikningur lánardrottins sem er með hakað við gátreitinn Stofna nýja eign. Kaupvirðisfærsla er sjálfkrafa bókuð fyrir eignina þegar reikningur lánardrottins er bókaður.
-   eign er stofnuð sjálfkrafa þegar innhreyfingarskjal afurða er bókað eða reikningur lánardrottins sem er með hakað við gátreitinn Stofna nýja eign. Engin kaupfærsla er bókuð fyrir eignina þegar reikningurinn lánardrottins er bókaður.

Veljið eina af fyrstu tveimur aðferðunum ef kosin er að stofna eignir handvirkt, og úthluta síðan eignanúmeri í innkaupapöntun eða reikningur lánardrottins. Veljið eina af síðustu tveimur aðferðunum ef kosin er sveigjanlegri nálgun: stundum er hægt að stofna eignir handvirkt, og stundum er að stofna sjálfkrafa eignir, byggðar á eignaupplýsingum í upplýsingum línuvöru. 

Hvort sem eignir eru stofnaðar handvirkt eða notuð sveigjanlegri nálgun, þarf að taka ákvörðun um hvort að kaupfærsla skuli einungis bókuð í Eignum, eða hvort að mögulegt skuli vera að bóka hana um leið og reikningur lánardrottins er bókaður. Sum fyrirtæki kjósa að notendur stofni kaup og kaupfærslur handvirkt í Eignum með því að nota handvirka skráningu í færslubók eða tillögur. 

Þetta efnisatriði fjallar nánar um hverja aðferð í smáatriðum.

## <a name="methods-for-manually-creating-fixed-assets"></a>Aðferðir fyrir að stofna eign handvirkt
Þegar reikningur lánardrottins er bókaður þar sem númer eignar hefur verið fært inn í línu og ef  gátreiturinn  Leyfa eignakaup úr innkaupum valkostur hefur verið valinn í síðunni færibreytur eigna, bókfærist kaup sjálfkrafa, og staða eignar breytist yfir í opið. 

Ef ekki er hægt að bóka kaup, er annað hvort hægt að færa inn handvirkt kaupfærslu í Eignir, eða nota kauptillögu í  færslubókinni til þess að stofna margar kaupfærslur í einu.

> [!NOTE]                                                                                                                              
> Ef fjárhagur er settur upp til þess að takmarka bókun kaupfærslu við ákveðinn notendahóp,  verður sá sem skráir inn að vera meðlimur í þeim notendahópi til þess að geta bókað kaupfærslur út frá reikningum.

## <a name="methods-for-automatically-creating-fixed-assets"></a>Aðferðir fyrir að stofna eign sjálfkrafa
Þegar er að bóka innhreyfingarskjal afurða sem er með Stofna nýja fastra eigna valkostur valinn fyrir línu er ný eign er stofnuð með stöðuna Ekki enn keypt. Síðan, þegar reikningur lánardrottins er bókaður með nýrri eign, bókfærist kaupfærsla fyrir hina nýju eign og staða eignar breytist yfir í opið, ef eign er settur þannig upp að hann leyfir eignakaup frá viðskiptaskuldir, og ef sá sem skráir er meðlimur í notendahópi sem getur bókfært kaupfærslur. 

Ef  valkosturinn Ný eign? var ekki valinn í innkaupalínunni þegar innhreyfingarskjal afurða var bókaður, en var aftur á móti valinn þegar reikningur lánardrottins var bókaður, stofnast ný eign og eignast með stöðuna opið, ef eign er settur upp til þess að leyfa stofnun og kaup. Viðbótareign stofnast ekki þegar þú bókar reikning lánardrottins ef reikningur var þegar stofnaður þegar innhreyfingarskjal afurða var bókaður.

### <a name="capitalization-threshold"></a>Fjármögnunarþröskuldur

Þegar aðferð er notuð þar sem eign stofnast og er keypt sjálfkrafa,  er hægt að stilla kerfið þannig að það sannreyni hvort að innkaupaupphæð eignar nái tilgreindum þröskuldi eignafærslu fyrir afskriftir eigna. Ef svo er, þá mun afskriftar gátreiturinn verða valinn í bókum fyrir eignina þegar hún er stofnuð út frá viðskiptaskuldir. 

fjármögnunarþröskuldur er gjaldmiðilsupphæð sem ákvarðar hvort að eignir eru afskrifaðar ef þær ná hinni tilgreindu upphæð. Til dæmis,  ef eign er keypt og innkaupaupphæð er undir þröskuldi eignafærslu, þá er eignin ekki merkt til afskriftar; ef innkaupaupphæð hins vegar nær eða fer yfir þröskuldinn, þá merkist eignin til afskriftar. 

Hægt er að setja upp fjármögnunarþröskuldinum síðunni eignaflokkur.

## <a name="scenario"></a>Aðstæður
Eftirfarandi dæmi fjallar um heilan verkhring samþættingar eigna og lánardrottna. Sýnishorn uppsetningar eru birt og notkun kauptillagna er einnig lýst. 

Í þessu dæmi, er kerfið sett upp á eftirfarandi hátt:

-   Eignir stofnast sjálfkrafa þegar innhreyfingarskjal afurða eða reikningur lánardrottins eru bókaðir, en eign er settur upp til að koma í veg fyrir bókun kaupfærslna frá viðskiptaskuldir.
-   Lyklar eru tilgreind í svæðinu lykilgerð eigna fyrir fylgiskjal eignar og lykilgerðu eignaúthreyfinga í síðunni vöruflokkur.
-   fjármögnunarþröskuldinum fyrir tölvuflokkinn (COMP) er 1,500.
-   Færa skal inn innkaupapöntun fyrir nýja fartölvu sem starfsmaður mun nota, bóka innkaupapöntun, sannreyna að starfsmaður í flutningum bóki innhreyfingarskjal afurða, bóka reikning lánardrottins, og sannreyna síðan að bókari uppfæri fartölvueign yfir í stöðuna opið.

Til að hefja verkið, skal nota síðuna innkaupapöntun til þess að færa inn upplýsingar um fartölvuna, sem kostar 1,600. Velja skal  gátreitinn Ný eign? í flýtiflipa eigna fyrir innkaupapöntunarlínunum, velja COMP sem eignaflokk, og vista innkaupapöntun. 

Þegar fartölvan hefur verið móttekin, kemur starfsmaður í flutningumog bókar innhreyfingarskjal afurða til að skrásetja móttöku fartölvunnar. Fartölvueign er stofnuð og er með stöðuna Ekki enn keypt. Upphæðin er hærri en fjármögnunarþröskuldinum . Þess vegna er Afskrifta valkostur valinn í bókum fyrir fartölvueignina. Eftirfarandi færslur áttu sér stað.

| Lýsing                               | Reikningur             | Debet    | Kredit   |
|-------------------------------------------|---------------------|----------|----------|
| Innkaup, innkaup innhreyfingarskjals afurðar        | Óreikningsfærðar innhreyfingar | 1.600,00 |          |
| Innkaup, innhreyfingarskjal afurða mótfærslu innkaupa | Uppsöfnuð innkaup   |          | 1.600,00 |

Næst, skal bóka reikningur lánardrottins fyrir fartölvuna. Staða fartölvunnar breytist ekki vegna þess að eign er stilltur þannig að hann kemur í veg fyrir bókanir á kaupfærslum þegar verið er að bóka reikningur lánardrottins. Valkosturinn Stofna nýja eign var valinn þegar reikningur lánardrottins var bókaður. Þess vegna innhreyfingarlykill eignar var notuð. Úthreyfingarlykill eignar var ekki notaður vegna þess að engin kaup voru bókuð; hann verður notaður síðar þegar bókari fyrirtækisins bókar kaupfærslu í Eignum með því að nota kauptillögur. 

Eftirfarandi færslur áttu sér stað.

| Lýsing                               | Reikningur             | Debet    | Kredit   |
|-------------------------------------------|---------------------|----------|----------|
| Innkaup, innhreyfingarskjal afurða mótfærslu innkaupa | Uppsöfnuð innkaup   | 1.600,00 |          |
| Staða lánardrottins                            | Viðskiptavinir    |          | 1.600,00 |
| Innkaup, Kvittun fyrir eign             | Tölvukostnaður    | 1.600,00 |          |
| Innkaup, innkaup innhreyfingarskjals afurðar        | Óreikningsfærðar innhreyfingar |          | 1.600,00 |

Að lokum, skoðar bókari allar eignir sem hafa stöðuna Ekki enn keypt. Þess vegna er hina nýju fartölvueign yfirfarin. Bókari opnar síðan síðuna kauptillaga út frá  færslubókarlínum, og stofnar kaupvirðisfærslur fyrir allar eignir sem hafa reikning en ennþá stöðuna ekki enn keypt. Þegar færslubókin er bókuð breytist staða fartölvueignarinnar í Opna. Úthreyfingarlykill eignar er skuldfærður og  eignakauparlykill er tekjufærður. 

Eftirfarandi eru nánari útfærslur á þessu dæmi:

-   Ef eign er settur upp til þess að leyfa bókun eignakaupa um leið og reikningar lánardrottins eru bókaðir, þá þarf bókari ekki að nota kauptillögur í Eignum vegna þess að kaupfærsla hefur verið stofnuð. Ennfremur, ólíkir lyklar uppfærast þegar reikningur lánardrottins er bókfærður. Í staðinn fyrir tölvukostnað, er móttökubirgðareikningur eignar debetfærður og tvær aðrar færslur eiga sér stað: eignakaupalykillinn er debetfærður og úthreyfingarlykil birgða fyrir eignir er kreditfærður.
-   Ef Valkosturinn Stofna nýja eign er ekki valinn þegar innhreyfingarskjal afurða er bókaður, er engin eign stofnuð á þeim tíma. Ef valkosturinn stofna nýjan eign er valinn áður en að reikningur lánardrottins er bókaður, stofnast eign með stöðuna Ekki enn keypt, eða stöðuna  Opinn ef kaupfærslur eru einnig bókaðar þegar bókun reikningur lánardrottins fer fram.
-   Ef kostnaður við fartölvuna er 1,400 í staðinn fyrir 1,600, er fjármögnunarþröskuldi ekki náð. Þess vegna er eign er stofnuð og Afskriftir valkostur er hreinsaður.
-   Ef komubók er notuð, er síðan samþykktarbók reiknings notuð eftir að komubók hefur verið bókuð til að sækja fylgiskjal, tengja innkaupapöntun við reikningur lánardrottins, veljið síðan gátreitinn stofna nýja eign, og bókið síðan reikning lánardrottins. Ef þú ert meðlimur í notendahópi sem getur stofnað kaupfærslur, stofnast kaupin og eignin fær stöðuna opin.
-   Ef einungis hluti af magni er móttekinn, stofnast engin eignakaup fyrir fyrsta reikningur lánardrottins vegna takmarkana á notendahópi. Eina leiðin til að bóka kaup fyrir næsta reikningur lánardrottins sem uppfyllir það magn sem pantað var er ef kaupfærsla hefur þegar verið færð inn fyrir fyrsta reikningur lánardrottins , og ef þú ert meðlimur í notendahópi sem hefur leyfi til að bóka kaup.


Frekari upplýsingar eru í [Samþætting eigna](fixed-asset-integration.md).




