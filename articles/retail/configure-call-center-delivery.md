---
title: Grunnstilla afhendingarmáta og gjöld í símaveri
description: Þetta efni lýsir því hvernig á að setja upp afhendingarmáta og gjöld fyrir símaverspöntun í Dynamics 365 Retail.
author: josaw1
manager: AnnBe
ms.date: 04/26/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailMCRChannelDetailPage, MCROrderParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: b67a1d91e41e1a4c21e0e877c06812dededbe731
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/24/2019
ms.locfileid: "2019486"
---
# <a name="configure-call-center-delivery-modes-and-charges"></a>Grunnstilla afhendingarmáta og gjöld í símaveri

[!INCLUDE [banner](includes/banner.md)]

Þegar sölupöntun er settur í Dynamics 365 Retail, ef sá sem færði inn sölupöntunina er tengd við símaversrás eru rök og reglur notuð til að sannprófa afhendingarmátann (afhendingarmáti) og reikna út gjöld fyrir pöntunina.

Þegar þú býrð til sölupöntun getur þú valið afhendingarmáta á sölupöntunarhausnum og sölupöntunarlínunum. Sjálfgefið er að afhendingarmátinn sem þú velur á hausnum er notaður fyrir allar sölupöntunarlínur. Þú getur hins vegar hunsað sjálfgefna afhendingarmátann á einstökum sölulínum eins og þú þarfnast. Þú getur einnig skilgreint afhendingarmáta á viðskiptavinarskrá. Þá, þegar pantanir eru búnar til fyrir viðskiptavininn, er þessi afhendingarmáti notuð að sjálfgefnu í sölupöntunarhausnum.

Retail hefur eiginleika sem leyfir notendum að takmarka afhendingarmátana sem rás getur notað, afhendingarmátann sem hægt er að nota fyrir vöru og afhendingarmátana sem gilda fyrir sendingar á tiltekna áfangastaði. Gjöld geta einnig verið skilgreind þannig að viðbótargjöldum er bætt við pöntun viðskiptavinar, byggt á afhendingarmátanum sem eru valinn fyrir sölupöntunina og heildarverðmæti pöntunar.

## <a name="define-delivery-modes"></a>Skilgreina afhendingarmáta

Áður en þú tilgreinir hvaða afhendingarmáta er hægt að nota fyrir símaverspantanir og skilgreinir reglur og gjöld sem tengjast þeim, verður þú að skilgreina afhendingarmátana. Fara í **Sala og markaðssetning \> Uppsetning \> Dreifing \> Afhendingarmátar**. Velja **Nýr** til að búa til nýjan afhendingarmáta. Einnig er hægt að velja núverandi afhendingarham í listanum og síðan velja **Breyta** til að gera breytingar.

Í **Afhendingarmáti** reitinn getur þú slegið inn hvaða samsetningu af bók- og tölustöfum sem er, byggt á kröfum fyrirtækis þíns. Þú getur síðan notað **Lýsing** reitinn til að veita frekari samhengi. **Gjaldaflokkur** og **Flýta** reitirnir eru valfrjáls og verður útskýrðir nánar síðar í þessu efnisatriði.

Í **Smásölurásir** flýtiflipanum, skal bæta við hvaða smásölurás sem ætti að vera heimilt að nota afhendingarmátann þegar sölufærslur er búið til í þeirri rás.

Í **Vörur** flýtiflipanum er hægt að tilgreina hvaða vörur og/eða vöruflokkar má senda með þessum afhendingarmáta og hverjar ekki. Til dæmis, ef vara er ekki hægt að flytja í lofti vegna reglna um hættuleg efnum (spilliefni), vertu viss um að varan eða vöruflokkurinn sé undanskilinn frá öllum afhendingarmátum sem fela í sér flutninga í lofti.

Á **Aðsetur** flýtiflipanum getur þú tilgreint hvaða lönd eða svæði, eða ríki, hægt er að nota afhendingarmátann fyrir og hver ekki. Til dæmis eru pantanir sem eru sendar til Hawaii eða Alaska ekki gjaldgengar til afhendingar á jörðu niðri. Því ber að útiloka þessi ríki frá öllum afhendingarmáta sem er í tengslum við flutningsþjónustu á jörðu, en innifela þau í alla afhendingarmáta sem er í tengslum við flutningsþjónustu í lofti.

## <a name="validate-delivery-modes-for-a-call-center-order"></a>Sannprófa afhendingarmáta fyrir símaverspöntun

Eftir að afhendingarmátar eru skilgreind verður þú að keyra **Vinna afhendingarmáta** runuvinnslu. Þetta vinnsla gerir afhendingarmátana tiltæka þannig að hægt sé að nota þær í sölupöntunarferli fyrir smásölurásir. Til að keyra **Vinna afhendingarmáta** vinnsluna, farðu í **Retail \> Upplýsingatækni smásölu \> Vinna afhendingarmáta**. Þessa vinnslu ætti að keyra hvenær sem nýjar afhendingarmátar eru bættir við smásölurás eða breytingar eru gerðar á núverandi samböndum milli afhendingarmátar/rás.

Eftir að þú hefur keyrt **Vinna afhendingarmáta** runuvinnsluna, geturðu farið í **Retail \> Rásir \> Símaver \> Öll símaver**. Á **Öll símaver** síðunni, í aðgerðarrúðunni, á **Uppsetning** flipanum, veldu **Afhendingarmátar**. **Afhengingarmátar** síðan sýnir alla gilda afhendingarmáta fyrir valda símaversrás. Til að breyta núverandi afhendingarmátum eða bæta við nýjum afhendingarmátum, veldu **Stjórna afhendingarmátum**. Athugaðu að **Vinna afhendingarmáta** vinnsluna verður að keyra í hvert skipti sem breytingar eru gerðar.

## <a name="define-charges-for-delivery-services"></a>Skilgreina gjöld fyrir afhendingarþjónustu

Þegar sölupantanir eru búnar til fyrir viðskiptavini gæti fyrirtæki viljað bæta við gjöldum sem eru reiknuð sjálfkrafa miðað við afhendingarmátann sem er valið fyrir pöntunina. Þessar gjöld geta verið grunnstillt þannig að þau séu þau sömu fyrir alla viðskiptavini og afhendingarmáta. Að öðrum kosti geta gjöldin verið breytileg eftir viðskiptavinur og/eða afhendingarmáta sem eru valdir fyrir sölupöntunina.

Til að skilgreina gjöldin skaltu fara í **Retail \> Uppsetning rásar \> Gjöld \> Sjálfvirk gjöld**. Veldu **Nýtt** til að bæta við nýjum gjöldum. Einnig er hægt að velja núverandi færslu og síðan velja **Breyta**.

Gjöld geta verið skilgreind þannig að þau eru reiknuð á stigi annaðhvort pöntunarhauss eða pöntunarlína. Notaðu **Stig** reitinn til að velja það stig sem þú vilt.

Hægt er að skilgreina gjöld fyrir tiltekinn viðskiptavin, hóp viðskiptavina eða alla viðskiptavini. Í **Reikningskóði** reitnum skaltu velja **Tafla** til að skilgreina gjöld sem aðeins eru lögð á sérstakrar viðskiptavin. Veldu **Hópur** til að skilgreina gjöld fyrir tiltekinn viðskiptavinahóp. Veldu **Allt** til að leggja gjöldin á sérhvern viðskiptavin sem leggur inn sölupöntun sem notar tengda afhendingarmátann. Ef þú valdir **Tafla** eða **Hópur** í **Reikningskóði** reitnum skaltu velja viðskiptavininn eða viðskiptavinahópinn í **Reikningstengsl** reitnum.

Hægt er að grunnstilla gjöld þannig að þau eru sett á tiltekinn afhendingarmáta, hóp afhendingarmáta eða alla afhendingarmáta. Ef þú velur **Tafla** í **Kóði fyrir afhendingarmáta** reitinn, verður þú að velja tiltekinn afhendingarmáta í **Tengsl afhendingarmáta** reitnum. Ef þú velur **Hópur** verður þú að velja hóp afhendingarmáta í **Tengsl afhendingarmáta** reitnum. Hópar afhendingarmáta eru skilgreindir á **Retail \> Uppsetning rásar \> Gjöld \> Afhendingargjald hópur**. Þeir geta síðan verið tengdir einum eða fleiri afhendingarmáta á **afhendingarmáti** síðunni. Ef þú velur hóp þegar þú skilgreinir gjöld, notar hvaða afhendingarmáti sem er tengdur við valda afhendingarhópinn þau gjöld. Að lokum, ef þú velur **Allt** í **Kóði afhendingarmáta** reitnum, nota allir afhendingarmátar gjöldin. Þess vegna velurðu ekki gildi í **Afhendingarmáti tengsl** reitnum.

Í **Línur** hlutanum er hægt að skilgreina einn eða fleiri gjöld eftir gjaldeyri, eins og þú þarfnast. Gjöld verða að vera tengd við gjaldakóða sem skilgreinir fjárhagsbókunarreglurnar fyrir gjaldið. **Flokkur** reiturinn er notaður til að skilgreina hvernig gjöld eru reiknuð. Til dæmis, ef viðskiptavinir ættu að vera rukkaðir um fastagjald sem nemur 9,95 USD fyrir að fá pöntun senda með tilteknum afhendingarmáta, skaltu nota **Fast** flokkinn. Ef fyrirtæki ákveður að rukka viðskiptavini um prósentuhlutfall af pöntuninni í heild til að standa straum af afhendingargjöldum skaltu nota **Prósent** flokkinn. Raunverulegur gjald til viðskiptavina er skilgreindur í **Virði gjalda** reitnum.

Smásölufyrirtæki grunnstilla oft stigskipt gjöld. Í því tilviki er sú upphæð sem viðskiptavinir greiða fyrir afhendingu byggð á pöntunarvirði. Til að grunnstilla stigskipt gjöld skal slá inn gildi í **Frá upphæð** og **Til upphæðar** reitina auk þess að ákvarða gjaldið sjálft í **Virði gjalda** reitnum. Til dæmis, fyrir pantanir sem hafa minna virði en 50 USD, rukkar smásöluaðili 5,95 USD fyrir flutninga á jörðu niðri. Fyrir pantanir sem hafa virði sem er jafnt og eða meira en 50 USD, en minna en 100 USD, rukkar smásöluaðili 7,95 USD. Að lokum, fyrir pantanir sem hafa virði sem er jafnt og eða meira en 100 USD, rukkar smásöluaðili engin flutningsgjöld. Eftirfarandi mynd sýnir grunnstillingu þessara gjalda.

![Föst stigskipt gjöld dæmi](media/fixedtieredcharges.png)

Þú getur notað blöndu af flokkum fyrir gjöld, allt eftir þörfum fyrirtækisins. Til dæmis, fyrir allar pantanir sem hafa virði sem er minna en 100 USD, er fast flutningsgjald upp á 9,95 USD. Þá, fyrir pantanir sem hafa virði sem er jafnt og eða meira en 100 USD, eru afhendingargjöld reiknuð með 5% hlutfalli af pöntunarvirði. Eftirfarandi mynd sýnir grunnstillingu þessara gjalda.

![Blönduð stigskipt gjöld dæmi](media/mixedtieredcharges.png)

## <a name="apply-delivery-modes-during-order-entry-in-a-call-center"></a>Virkja afhendingarmáta meðan á pöntunarfærslu stendur í símaveri

Þegar nýr sölupöntun er búin til verður að tilgreina gildi í **Afhendingarmáti** reitinn á **Afhending** flýtiflipanum á sölupöntunarhausnum. Þetta reitur gæti verið fyllt út sjálfkrafa, byggt á sjálfgefnum gildum frá viðskiptavinarskránni.

Afhendingarmátinn sem er skilgreindur á pöntunarhausnum er sjálfkrafa afritaður í sölupöntunarlínurnar um leið og þær eru búnar til. Hins vegar er hægt að breyta afhendingarmáta uppsetningu fyrir tiltekna línuvöru á **Afhending** flipanum í **Línuupplýsingar** hluta færslusíðu sölupöntunar.

Ef valinn afhendingarmáti er ekki gildur fyrir vöruna eða afhendingaraðsetrið sem skilgreint er fyrir pöntunina eða pöntunarlínuna færðu villuboð. Þú verður þá að velja afhendingarmáta sem hefur verið skilgreindur til að styðja við grunnstillingu vöru eða aðseturs.

## <a name="calculation-of-delivery-charges-during-entry-of-order"></a>Útreikningur á afhendingargjöldum á meðan pöntunarfærslu stendur

Ef kveikt er á stillingu **Virkja lok pöntunar** fyrir símaversrásina þína er sendingargjöld reiknaður sjálfkrafa fyrir sölupantanir þegar notendur velja **Ljúka**. Eftirfarandi skilaboð birtast efst á **Samantekt sölupöntunar** síðu: „Stigskipt gjöld reiknuð.“ Gjöldin sem eru reiknuð eru bætt við gildin í **Heildarsala** reitnum. Á **Upphæð** flýtiflipanum, sýnir **Gjöld** reiturinn heildarfjárhæð allra gjalda sem hafa verið reiknaðar fyrir pöntunina og línurnar. Til að sjá nánari sundurliðun á gjöldum skaltu velja **Pöntun** á **Samantekt sölupöntunar** síðunni, og veldu síðan **Gjöld** valkost til að skoða, bæta við eða breyta gjöldum. Athugaðu að útreikningur á afhendingargjöldum á pöntunarhausnum byggist á afhendingarmátanum sem tengist hausnum. Afhendingargjöld tengd línustigi eru reiknaðar út frá afhendingarmátanum sem er grunnstillt fyrir sölulínuna. Ef margar tegundir afhendingarmáta eru notaðar á mismunandi línum gætu verið notuð margskonar gjöld og þau lögð saman. Heildarupphæðin er síðan sýnd í **Gjöld** reitnum á **Samantekt sölupöntunar** síðunni.

Ef slökkt er á stillingunni **Virkja lok pöntunar**, verða notendur að kveikja handvirkt á útreikningi á gjöldum. Á **Sölupöntun** síðunni, á aðgerðarrúðunni, á **Selja** flipanum, í **Reikna** hópnum, veldu **Stigskipt gjöld**. Skilaboðin „Stigskipt gjöld reiknuð“ birtist. Þú getur þá valið **Gjöld** valkostinn á **Selja** flipanum til að skoða, breyta, eða eyða reiknaða gjöldum.

## <a name="use-expedited-delivery-modes-on-call-center-orders"></a>Notaðu flýta afhendingarmáta á símaverspantanir

Ef þú vilt geturðu tengt flýtikóðann við hvaða afhendingarmáta sem þú grunnstillir. Þessi kóði er notuð sem forgangsröðun og skýrslugerðartæki. Það veldur því ekki að viðbótargjöld verði sett á pöntunina sem stendur. Til að setja upp flýtikóða skaltu fara í **Sala og markaðssetning \> Uppsetning \> Dreifing \> Flýtikóðar**.

Til dæmis, fyrir pantanir sem verða fluttar með flugi næsta dag, verður að tiltekt að eiga sér stað í vörugeymslunni fyrir klukkan 13:00 á hverjum degi. Í þessu tilfelli er hægt að búa til flýtikóða og þessi kóða er hægt að tengja við allar gerðir afhendingarmáta fyrir næsta dag, sem eru grunnstilltar í kerfinu. Þegar vörugeymsla býr til tiltektarbylgju má nota viðeigandi flýtikóða í **Flýta** reitnum sem afmörkun, þannig að tiltekt er aðeins keyrð fyrir pantanir sem hafa afhendingarmáta sem tengist þeim kóða.

Að auki, þegar símaverspöntun er færð inn, er hægt að beita flýtikóðanum handvirkt annaðhvort í sölupöntunarhaus eða í einstaka sölupöntunarlínu. Líkt og áður, hægt er að nota kóðann til flokkunar eða skýrslugerðar. Stundum þarf að meðhöndla pöntun gætilega vegna vandamáls í þjónustudeild. Í þessu tilviki er hægt að beita tilteknum flýtikóða á pöntunarhausinn eða línurnar til að hjálpa til við að auðkenna og forgangsraða pöntuninni á meðan uppfyllingarferlinu stendur.
