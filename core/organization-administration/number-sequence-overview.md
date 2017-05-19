---
title: Talnarunuyfirlit
description: "Númeraraðir í Microsoft Dynamics 365 for Operations eru notaðar til að mynda lesanleg, einkvæm kenni fyrir skýrslur aðalgagna og færsluskrár sem krefjast kenna. færsla aðalgagna eða færsla sem krefst kennimerkis er vísað til sem <em>tilvísun</em>."
author: MargoC
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15461
ms.assetid: 6e19bd1d-192b-4da2-8573-84f6e1ce98ef
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: ce03d3b55ecdc05f70a36762f7de49b3018b6451
ms.contentlocale: is-is
ms.lasthandoff: 04/25/2017


---

# <a name="number-sequence-overview"></a>Talnarunuyfirlit

[!include[banner](../includes/banner.md)]


Númeraraðir í Microsoft Dynamics 365 for Operations eru notaðar til að mynda lesanleg, einkvæm kenni fyrir skýrslur aðalgagna og færsluskrár sem krefjast kenna. færsla aðalgagna eða færsla sem krefst kennimerkis er vísað til sem <em>tilvísun</em>.

Áður en hægt er að stofna nýjar færslur fyrir tilvísun í Microsoft Dynamics 365 for Operations verður að setja upp númeraröð og tengja hana við tilvísunina. Mælt er með því að nota síðurnar í **Fyrirtækisstjórnun** til að setja upp númeraraðir. Ef Kerfiseining stillingar eru áskilin er hægt að nota síðuna færibreytur í kerfi til að tilgreina númeraröð fyrir tilvísanir í því kerfi. Til dæmis í **viðskiptakröfur** og **viðskiptaskuldir** , er hægt að setja upp flokka númeraraða til að úthluta tilteknum númeraraðir til ákveðinna viðskiptavina eða lánardrottna. Þegar sett er upp númeraröð, verður að tilgreina svið, sem skilgreinir hvaða fyrirtæki notar númeraröðina. Umfang getur verið **Samnýtt**, **Fyrirtæki**, **lögaðila**, eða **rekstrareining**. Umfang **lögaðila** og **fyrirtækja** má sameina við **tímabil fjárhagsdagatals** til að búa til enn sértækari númeraraðir. Talnarunu snið samanstanda af hluti. Númeraraðir með annað umfang en **samnýtt** geta innihaldið hluti sem samsvara umfangi. Til dæmis getur talnaröð með umfangið **lögaðili** innihaldið hluta lögaðila. Með því að hafa svið hluta í snið númeraraðar, er hægt að greina svið tiltekna færslu með því að líta á númeri þess. Auk hluta sem samsvara umfangi, geta sniðmát númeraraðar innihaldið **fasta** og **tölustafahluta** . Hlutinn **Fasti** inniheldur safn stafa, tölustafa eða tákn sem breytast ekki. **Tölustafa** Hluti inniheldur safn af bókstöfum eða tölustöfum sem hækka í hvert skipti sem tala er notuð. Nota númerstákn (\#) til að tákna hækkandi tölustafi og og-merki (&) til að tilgreina hækkandi bókstafi. Sniðið \#\#\#\#\#\_2017 stofnar t.d. röðina 00001\_2017, 00002\_2017 og svo framvegis.
Talnarunu dæmi
------------------------

Eftirfarandi dæmi sýna hvernig á að nota hluta til að stofna snið númeraraðar. Sérstaklega, sýna dæmin áhrif þess að nota sviðshluta.
### <a name="expense-report-numbers"></a>Númer kostnaðarskýrslu

Í eftirfarandi dæmi eru kostnaðarskýrslutölur settar upp fyrir lögaðilann sem heitir **CS**. **Svæði:**Ferðir og útgjöld **Tilvísun:**númer Kostnaðarskýrslu **Umfang:**Lögaðili **Lögaðili:**CS
| Hlutar  | Hlutagerð | Gildi     |
|-----------|--------------|-----------|
| Hluti 1 | Lögaðili | CS        |
| Hluti 2 | Fasti     | -ÚTGJÖLD- |
| Hluti 3 | Bók- og tölustafir | \#\#\#\#  |

**Dæmi um forsniðið númer**: CS-EXPENSE-0039 Þú getur sett upp svipað talnarunusnið fyrir aðra lögaðila. Til dæmis, fyrir lögaðila sem nefnist **RW**, ef aðeins gildið hluta lögaðila er breytt er forsniðið númer RW-EXPENSE-0039. Einnig er hægt að breyta heiltölusniði númeraraðar fyrir aðra lögaðila. Til dæmis er hægt að sleppa svið hluta lögaðila til að stofna forsniðið númer svo Lokagildistíma 0001.

### <a name="sales-order-numbers"></a>Sölupöntunarnúmer

Í eftirfarandi dæmi eru númer sölupöntunar sett upp fyrir fyrirtækjakennið **CEU**. **Svæði:**sala **Tilvísun:**Sölupöntun **Umfang:**Fyrirtæki **Fyrirtæki:**CEU
| Hlutar  | Gerð hluta | Virði    |
|-----------|--------------|----------|
| Hluti 1 | Fasti     | SO-      |
| Hluti 2 | Bók- og tölustafir | \#\#\#\# |

**Dæmi um forsniðið númer:** SO-0029 Jafnvel þótt sviðshluti er ekki tekið með í sniði , byrjar tölusetning upp á nýtt fyrir hvert fyrirtækjakenni. Ef notað er sama snið fyrir öll fyrirtækiskenni , eru sama númer notað í hverju fyrirtæki. Til dæmis sölupöntunarnúmer SO 0029 er notað í hverju fyrirtæki. Einnig er hægt að breyta heiltölusniði númeraraðar fyrir önnur fyrirtækiskenni.

### <a name="purchase-requisition-numbers"></a>Númer innkaupabeiðna

Í eftirfarandi dæmi, eru númer innkaupabeiðna úr öllu fyrirtækinu. **Svæði:**innkaup **Tilvísun:**Innkaupabeiðni **Umfang:**samnýtt
| Hlutar  | Gerð hluta | Virði    |
|-----------|--------------|----------|
| Hluti 1 | Fasti     | Req      |
| Hluti 2 | Bók- og tölustafir | \#\#\#\# |

**Dæmi um forsniðið númer**: Req0052 Þar sem umfang er **samnýtt** er sniðmát númeraraðar notað þvert yfir fyrirtækið. Hægt er að setja upp mismunandi röð snið fyrir mismunandi hluta fyrirtækisins. Afkastaatriði fyrir númeraraðir
-----------------------------------------------

Íhugið eftirfarandi upplýsingar um hvernig afbrigði númeraröðum geta haft áhrif á afköst kerfisins áður en hægt er að setja upp númeraraðir.
### <a name="continuous-and-non-continuous-number-sequences"></a>Samfelld og ekki samfelld númeraraðir

Númeraraðir geta verið samfelldar eða ósamfelldar. Samfelld númeraröð sleppir ekki neinum tölum en númer má ekki nota í númeraröð. Tölur úr ósamfelldri talnarunu eru notuð í röð, en talnarunan kann að sleppa tölum. Til dæmis, ef notandi hættir færslu, númer er myndað en ekki notað. Í samfelldni númeraröð, það númer er endurnýtt síðar. Í ósamfelldri númeraröð, ernúmer ekki notað. Samfelld númeraraðir eru yfirleitt áskilin fyrir ytri skjöl, eins og innkaupapöntunum, sölupöntunum og reikningum. Hins vegar samfelldri númeraröð getur haft neikvæð áhrif svartíma kerfi þar sem kerfið að biðja um númer úr gagnagrunninum í hvert skipti nýtt skjal eða færsla er stofnuð. Ef ósamfelld númeraröð er notuð, er hægt að virkja **forúthlutun** á **afkoma** flýtiflipa í **númeraröð** síðu. Þegar tilgreindur er fjöldi til að forúthluta, velur kerfið þessar tölur og vistar þær í minni. Ný tölur eru beðnir úr gagnagrunninum aðeins eftir að fyrirframúthlutað magn hefur verið notað. Ef ekki eru fyrirliggjandi lagaskilyrði um að notaðar séu samfelldar númeraraðir er ráðlagt að nota ekki samfelldar númeraraðir fyrir betri afköst.

### <a name="automatic-cleanup-of-number-sequences"></a>Sjálfvirk tiltekt númeraraðir

Ef rafmagnsleysi kemur upp, villa forrits eða önnur óvænt óhöpp getur kerfið ekki endurunnið númer sjálfkrafa fyrir samfelldri númeraröð. Hægt er að keyra tiltekt handvirkt eða sjálfvirkt til að endurheimta týnd númer. Íhugaðu vandlega notkun þjóns þegar hreinsunarferli er áætlað. Mælt er með því að tiltektin sé keyrð sem runuvinnsla utan háannatíma.






