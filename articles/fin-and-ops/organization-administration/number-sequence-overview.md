---
title: "Númeraraðir"
description: "Númeraraðir eru notaðar til að mynda lesanleg, einkvæm kennimerki fyrir skýrslur aðalgagna og færslur sem krefjast kennimerkja."
author: MargoC
manager: AnnBe
ms.date: 08/17/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: NumberSequenceTableListPage, NumberSequenceConfiguration
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 15461
ms.assetid: 6e19bd1d-192b-4da2-8573-84f6e1ce98ef
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 5f4ff7eb8ee9b87b9d90af4d215743596555fd73
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="number-sequences"></a>Númeraraðir

[!INCLUDE [banner](../includes/banner.md)]

Númeraraðir eru notaðar til að mynda lesanleg, einkvæm kennimerki fyrir skýrslur aðalgagna og færslur sem krefjast kennimerkja. færsla aðalgagna eða færsla sem krefst kennimerkis er vísað til sem *tilvísun*.

Áður en hægt er að stofna nýjar færslur fyrir tilvísun verður að setja upp númeraröð og tengja hana við tilvísunina. Mælt er með því að nota síðurnar í **Fyrirtækisstjórnun** til að setja upp númeraraðir. Ef Kerfiseining stillingar eru áskilin er hægt að nota síðuna færibreytur í kerfi til að tilgreina númeraröð fyrir tilvísanir í því kerfi. Til dæmis í **viðskiptakröfur** og **viðskiptaskuldir** , er hægt að setja upp flokka númeraraða til að úthluta tilteknum númeraraðir til ákveðinna viðskiptavina eða lánardrottna. 

Þegar sett er upp númeraröð, verður að tilgreina svið, sem skilgreinir hvaða fyrirtæki notar númeraröðina. Umfang getur verið **Samnýtt**, **Fyrirtæki**, **lögaðila**, eða **rekstrareining**. Umfang **lögaðila** og **fyrirtækja** má sameina við **tímabil fjárhagsdagatals** til að búa til enn sértækari númeraraðir. 

Talnarunu snið samanstanda af hluti. Númeraraðir með annað umfang en **samnýtt** geta innihaldið hluti sem samsvara umfangi. Til dæmis getur talnaröð með umfangið **lögaðili** innihaldið hluta lögaðila. Með því að hafa svið hluta í snið númeraraðar, er hægt að greina svið tiltekna færslu með því að líta á númeri þess. 

Auk hluta sem samsvara umfangi, geta sniðmát númeraraðar innihaldið **fasta** og **tölustafahluta** . Hlutinn **Fasti** inniheldur safn stafa, tölustafa eða tákn sem breytast ekki. **Tölustafa** Hluti inniheldur safn af bókstöfum eða tölustöfum sem hækka í hvert skipti sem tala er notuð. Nota númerstákn (\#) til að tákna hækkandi tölustafi og og-merki (&) til að tilgreina hækkandi bókstafi. Sniðið \#\#\#\#\#\_2017 stofnar t.d. röðina 00001\_2017, 00002\_2017 og svo framvegis.

<a name="number-sequence-examples"></a>Talnarunu dæmi
------------------------

Eftirfarandi dæmi sýna hvernig á að nota hluta til að stofna snið númeraraðar. Sérstaklega, sýna dæmin áhrif þess að nota sviðshluta.

### <a name="expense-report-numbers"></a>Númer kostnaðarskýrslu

Í eftirfarandi dæmi eru kostnaðarskýrslutölur settar upp fyrir lögaðilann sem heitir **CS**. 

- **Svið:** Ferðalög og kostnaður 
- **Tilvísun:** Númer kostnaðarskýrslu 
- **Umfang:**lögaðila 
- **Lögaðili:** CS

| Hlutar  | Hlutagerð | Gildi     |
|-----------|--------------|-----------|
| Hluti 1 | Lögaðili | CS        |
| Hluti 2 | Fasti     | -ÚTGJÖLD- |
| Hluti 3 | Bók- og tölustafir | \#\#\#\#  |

**Dæmi um snið númer**: CS-kostnað - 0039 

Þú getur sett upp svipað talnarunusnið fyrir aðra lögaðila. Til dæmis, fyrir lögaðila sem nefnist **RW**, ef aðeins gildið hluta lögaðila er breytt er forsniðið númer RW-EXPENSE-0039. Einnig er hægt að breyta heiltölusniði númeraraðar fyrir aðra lögaðila. Til dæmis er hægt að sleppa svið hluta lögaðila til að stofna forsniðið númer svo Lokagildistíma 0001.

### <a name="sales-order-numbers"></a>Sölupöntunarnúmer

Í eftirfarandi dæmi eru númer sölupöntunar sett upp fyrir fyrirtækjakennið **CEU**. 

- **: Svæði** Sölu 
- **Tilvísun:** Sölupöntun 
- **Umfang:** Fyrirtækið 
- **Fyrirtæki:** CEU

| Hlutar  | Gerð hluta | Virði    |
|-----------|--------------|----------|
| Hluti 1 | Fasti     | SO-      |
| Hluti 2 | Bók- og tölustafir | \#\#\#\# |

**Dæmi um snið númer**: SO-0029 

Jafnvel þótt svið hluta er ekki tekið með í sniði endurræsir tölusetning fyrir hvert fyrirtækjakenni. Ef notað er sama snið fyrir öll fyrirtækiskenni , eru sama númer notað í hverju fyrirtæki. Til dæmis sölupöntunarnúmer SO 0029 er notað í hverju fyrirtæki. Einnig er hægt að breyta heiltölusniði númeraraðar fyrir önnur fyrirtækiskenni.

### <a name="purchase-requisition-numbers"></a>Númer innkaupabeiðna

Í eftirfarandi dæmi, eru númer innkaupabeiðna úr öllu fyrirtækinu. 

- **Svæði:** Innkaup 
- **Tilvísun:** Innkaupabeiðni 
- **Umfang:** Deilt

| Hlutar  | Gerð hluta | Virði    |
|-----------|--------------|----------|
| Hluti 1 | Fasti     | Req      |
| Hluti 2 | Bók- og tölustafir | \#\#\#\# |

**Dæmi um snið númer**: Req0052 

Þar sem umfang er **Deilt** er sniðmát númeraraðar notað þvert yfir fyrirtækið. Hægt er að setja upp mismunandi röð snið fyrir mismunandi hluta fyrirtækisins. 

<a name="performance-considerations-for-number-sequences"></a>Afkastaatriði fyrir númeraraðir
-----------------------------------------------

Íhugið eftirfarandi upplýsingar um hvernig afbrigði númeraröðum geta haft áhrif á afköst kerfisins áður en hægt er að setja upp númeraraðir.

### <a name="continuous-and-non-continuous-number-sequences"></a>Samfelld og ekki samfelld númeraraðir

Númeraraðir geta verið samfelldar eða ósamfelldar. Samfelld númeraröð sleppir ekki neinum tölum en númer má ekki nota í númeraröð. Tölur úr ósamfelldri talnarunu eru notuð í röð, en talnarunan kann að sleppa tölum. Til dæmis, ef notandi hættir færslu, númer er myndað en ekki notað. Í samfelldni númeraröð, það númer er endurnýtt síðar. Í ósamfelldri númeraröð, ernúmer ekki notað. 

Samfelld númeraraðir eru yfirleitt áskilin fyrir ytri skjöl, eins og innkaupapöntunum, sölupöntunum og reikningum. Hins vegar samfelldri númeraröð getur haft neikvæð áhrif svartíma kerfi þar sem kerfið að biðja um númer úr gagnagrunninum í hvert skipti nýtt skjal eða færsla er stofnuð. 

Ef ósamfelld númeraröð er notuð, er hægt að virkja **forúthlutun** á **afkoma** flýtiflipa í **númeraröð** síðu. Þegar tilgreindur er fjöldi til að forúthluta, velur kerfið þessar tölur og vistar þær í minni. Ný tölur eru beðnir úr gagnagrunninum aðeins eftir að fyrirframúthlutað magn hefur verið notað. 

Ef ekki eru fyrirliggjandi lagaskilyrði um að notaðar séu samfelldar númeraraðir er ráðlagt að nota ekki samfelldar númeraraðir fyrir betri afköst.

### <a name="automatic-cleanup-of-number-sequences"></a>Sjálfvirk tiltekt númeraraðir

Ef rafmagnsleysi kemur upp, villa forrits eða önnur óvænt óhöpp getur kerfið ekki endurunnið númer sjálfkrafa fyrir samfelldri númeraröð. Hægt er að keyra tiltekt handvirkt eða sjálfvirkt til að endurheimta týnd númer. 

Íhugaðu vandlega notkun þjóns þegar hreinsunarferli er áætlað. Mælt er með því að tiltektin sé keyrð sem runuvinnsla utan háannatíma.






