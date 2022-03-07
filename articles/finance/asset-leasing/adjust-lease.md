---
title: Leiðrétta leigusamninga
description: Þetta efnisatriði útskýrir hvernig á að leiðrétta leigusamning. Leiðrétting gæti verið nauðsynleg ef leiguskilmálum er breytt, leigan framlengd eða aðrar aðstæður breytast.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1016b69fd59bbe90924996f5c931cb5d0f779253de66f5f3821a8c3001d3313b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6729655"
---
# <a name="adjust-leases"></a>Leiðrétta leigusamninga

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Þetta efnisatriði útskýrir hvernig á að leiðrétta leigusamning. Leiðrétting gæti verið nauðsynleg ef leiguskilmálum er breytt, leigan framlengd eða aðrar aðstæður breytast. Eignarleiga uppfyllir leiðbeiningar sem efnisatriði um skráningarkerfi reikningsskilastaðla 842 (ASC 842) og alþjóðlegan reikningsskilastaðal 16 (IFRS 16) kveður á um varðandi breytingar á leigusamningum. ASC 842-20-15-1 skilgreinir breytingar á leigusamningi sem allar breytingar á skilmálum samnings sem valda breytingu á umfangi, eða meðferð á leigusamningi. Málsgrein 39 í IFRS 16 segir að leigjandi þurfi að endurmeta leiguskuldbindingu þannig að hún endurspegli breytingar á leigugreiðslum.

Fyrir fyrirtæki sem fylgja ASC 842 eða IFRS 16 er leigusamningur endurmetinn aftur til að endurspegla breytingu á núvirði á lágmarksgreiðslum á leigu í framtíðinni (PVFMLP). Þegar PVFMLP eykst er til staðar mun bókarfærslan sem er stofnuð vera debetfærsla á lykli afnotaréttar af eign og kreditfærsla á lykli leiguskuldbindingar fyrir mismuninn á milli nýja PVFMLP og eldri PVFMLP. Ef PVFMLP lækkar verður bókarfærslan debetfærsla á lykli leiguskuldbindingar og kreditfærsla á lykli afnotaréttar af eign fyrir mismuninum.

Ef leiðréttingin lækkar afnotarétt af eign 0 (núll) verður afgangurinn kreditfærður á bókunarlykil hagnaðar vegna breytinga á leigusamningi sem tilgreindur er á síðunni **Bókunarlyklar leigu**. Kerfisreikningar fyrir þessar færslur og aðrar leiðréttingarfærslur, svo sem breytingar á flokkun, ógreiddur stofnkostnaður, leiguhvatar, fyrirframgreiðslur og kostnaður sundurhlutunar sem hlýst af breytingum á leigusamningi.

Til að fá sérstaka leiðsögn varðandi leiðréttingarfærslur leigusamnings er mælt með því að skoða IFRS 16 og ASC 842.

## <a name="lease-adjustment-wizard"></a>Leiðsagnarforrit fyrir leiðréttingu leigusamnings

Til að leiðrétta leigusamning skal ljúka eftirfarandi skrefum. Breyttu gögnin munu uppfæra leiguáætlanir eftir að bóka er úr leiðsagnarforritinu **Leiðrétting leigusamnings**. Hægt er að vista vinnuna og loka leiðsagnarforritinu hvenær sem er og koma aftur síðar til að halda áfram vinnunni.

Til að opna leiðsagnarforritið **Leiðrétting leigusamnings** úr samantekt leigusamnings skal fylgja þessum skrefum.

1. Opnaðu **Eignarleiga \> Leigusamningar \> Samantekt leigusamnings**. 
2. Veljið leigusamninginn sem á breyta og veljið síðan **Leiðsagnarforrit leiðréttingar**.
3. Fylgið leiðbeiningum leiðsagnarforritsins til að færa inn nauðsynlegar breytingar.

Til að opna leiðsagnarforritið **Leiðrétting leigusamnings** á síðunni **Leiðrétting leigusamnings** fyrir leiðréttingu sem er þegar í gangi skal fylgja þessum skrefum.

1.  Farið í **Leiga \> Leigusamningar \> Leiðréttingar leigusamnings**.
2.  Veljið leigusamning sem er með leiðréttingarstöðuna **Í vinnslu** og veljið síðan **Leiðsagnarforrit leiðréttingar**.
3.  Í reitina **Upphafsdagsetning breytingar** og **Bókunardagsetning** skal færa inn viðeigandi dagsetningar.
4.  Veljið **Næst**.

    Leigusamningnum hefur nú verið bætt við síðuna **Leiðréttingar leigusamnings** þar sem hægt er að færa inn nýjar upplýsingar um hann.

    Þegar leigusamningnum hefur verið breytt eiga reitir er varða afnotarétt við um hann. Ef enginn beinn kostnaður, leiguhvatar, fyrirframgreiðslur eða kostnaður sundurhlutunar er tengdur við breyttan leigusamning skal skilja samsvarandi reiti eftir auða. Upprunalegu upphæðirnar eiga ekki við um uppfærða leigusamninginn. 

    Leigusali veitir t.d. 1000 USD hvata til að samþykkja framlengingu á leigusamningi. Í þessu tilviki þegar þú breytir leigusamningnum til að gera ráð fyrir framlengingunni færir þú **1.000** inn í reitinn **Leiguhvatar sem koma til vegna leiðréttingar**.

    Greiðsluáætlunarlínurnar sýna nú allar greiðslur frá mánuðinum og síðari mánaða í reitnum **Upphafsdagsetning breytingar**. Þar sem breytingar eru fram í tímann, geta greiðsluáætlunarlínur ekki hafist fyrr en leiðréttingin byrjar. Til að skoða greiðsluáætlunarlínur frá því fyrir upphafsdagsetningu breytingar skal fara á síðuna **Útgáfuferill leigusamnings**.

8.  Veljið **Næst**.

    Á næstu síðu koma fram lykilupplýsingar um áætlaða leiðréttingu leigusamningsins, svo sem bókfært virði leiguskuldbindingarinnar fyrir breytinguna og nýja áætlaða leiguskuldbindingu eftir breytingu. Á síðunni birtist einnig forskoðun á bókarfærslunni fyrir væntanlega leiðréttingu leigusamnings.

9.  Veljið **Senda í verkflæði** til að senda leiðréttingu leigusamningsins í verkflæðiskerfið ef verkflæði fyrir leiðréttingar leigusamnings er virkt og leiðréttingin hefur ekki enn verið samþykkt. Frekari upplýsingar um hvernig á að nota verkflæði fyrir leiðréttingu leigusamnings er að finna í [Nota verkflæði fyrir leiðréttingar leigusamnings](use-create-lease-wrkflw.md).

    > [!NOTE]
    > Á þessu stigi endurreiknar kerfið leiðréttingarbreyturnar til að staðfesta að engar færslur hafi verið bókaðar á móti leigusamningnum frá því að yfirlit leiðréttingar og leiðréttingabók voru fyrst reiknuð. Ef einhver gildi breytast er hnitanet leiðréttingayfirlits uppfært og hægt er að yfirfara upplýsingarnar áður en leiðréttingar leigusamningsins eru sendar aftur inn í verkflæðiskerfið.

10. Ef verkflæði er ekki virkt, eða leiðrétting leigusamnings hefur verið samþykkt, skal velja **Ljúka** til að vinna úr breytingunum og bóka færslu leiðréttingabókar.

    > [!NOTE] 
    > Á þessu stigi endurreiknar kerfið leiðréttingarbreyturnar til að staðfesta að engar færslur hafi verið bókaðar á móti leigusamningnum frá því að yfirlit leiðréttingar og leiðréttingabók voru fyrst reiknuð. Ef einhver gildi breytast er hnitanet leiðréttingayfirlits uppfært og hægt er að yfirfara breytingarnar áður en valið er **Ljúka**. Ef verkflæðið er virkt og leiðrétting leigusamnings hefur verið samþykkt munu allar breytingar á yfirliti leiðréttingar leiða til þess að samþykktarstaðan verði stillt aftur á **Ekki sent inn**. Í þessu tilfelli ætti að senda aftur leiðréttingu leigusamnings inn í verkflæðiskerfið.

    Á síðunni **Leiðréttingar leigusamnings** er leiðréttingarstaðan nú stillt á **Lokið**.

    Á síðunni **Leiðréttingar leigusamnings** er enn hægt að skoða flýtiflipana **Yfirlit leiðréttingar** og **Forskoðun leiðréttingarfærslu**. Leiguverð og dagsetningar eru sýndar í útgáfusögu viðkomandi leigu.

    Ný útgáfa leigusamnings og nýjar áætlanir eru nú búnar til með því að nota breyttar upplýsingar. 

13. Til að skoða nýju áætlanirnar skal fara í leiguna og velja síðan **Bækur**.
14. Til að skoða nýmyndaðar greiðsluáætlun skal velja **Greiðsluáætlun**.
15. Til að skoða nýju afskriftaráætlun leiguskuldbindingar sem er mynduð úr nýju upplýsingunum skal loka síðunni **Greiðsluáætlun** og opna síðan síðuna **Afskriftaráætlun leiguskuldbindingar**.
16. Til að skoða nýmyndaða afskriftaráætlun eigna skal opna síðuna **Afskriftaráætlun eigna** á síðunni **Upplýsingar um bók**.
17. Til að skoða færslu leiðréttingabókar skal velja **Færslubækur \> Eignarleigubók**.

## <a name="cancel-a-lease-adjustment"></a>Hætta við leiðréttingu leigusamnings

Til að eyða leiðréttingu leigusamnings sem er í vinnslu skal fylgja þessum skrefum.

1.  Farið í **Leiga \> Leigusamningar \> Leiðréttingar leigusamnings**.
2.  Veljið hvaða leiðréttingu leigusamnings, sem er vinnslu, á að hætta við.
3.  Veljið **Hætta við leiðréttingu**. 
4.  Veljið **Í lagi**.

    > [!NOTE] 
    > Ef valið er **Hætta við** í leiðagnarforritinu **Leiðrétting leigusamnings** eru teknar til baka nýjustu breytingarnar sem var lokið við í leiðsagnarforritinu, en leiðrétting sem er í vinnslu er ekki fjarlægð.

## <a name="use-the-lease-adjustment-workflow"></a>Nota verkflæði fyrir leiðréttingu leigusamnings

Þessi hluti útskýrir hvernig á að nota verkflæði fyrir leiðréttingu leigusamnings. Verkflæði fyrir leiðréttingu leigusamnings hjálpar til við að stjórna leiðréttingum leigusamnings á skipulegan hátt með því að bjóða upp á nokkur samþykktarskref og úthluta þeim á tiltekna notendur sem samþykkja leiðréttingu á leigusamningi áður en hún er endanleg. Þegar leiðrétting á leigusamningi hefur verið samþykkt í verkflæði er hægt að nota leiðsagnarforritið **Leiðrétting leigusamnings** til að ljúka við leiðréttingu á leigusamningi.

1.  Til að senda inn leiðréttingu á leigusamningi til samþykkis skal fara í **Leiga \> Leigusamningar \> Leiðrétting leigusamnings**.
2.  Veljið kenni leigusamnings fyrir leiðréttingu á leigusamningi og veljið síðan **Leiðsagnarforrit leiðréttingar**.
3.  Á síðust síðu leiðsagnarforritsins skal velja **Senda inn til samþykkis**.
4.  Sláið inn athugasemd um leiðréttinguna og veljið síðan **Í lagi**.

    Stöðu verkflæðis er breytt í **Bíður samþykkis** og allir reitirnir í leiðsagnarforritinu eru læstir fyrir breytingum.

5.  Til að samþykkja leiðréttingu á leigusamningi skal fara í **Leiga \> Leigusamningar \> Leiðrétting leigusamnings**.
6.  Veljið kenni leigusamnings fyrir leiðréttingu á leigusamningi og farið yfir flýtiflipana **Yfirlit leiðréttingar** og **Forskoðun leiðréttingarfærslu**.
7.  Veljið **Verkflæði \> Samþykkt**.

    Á síðunni **Leiðréttingar leigusamnings** er leiðréttingarstaðan nú stillt á **Samþykkt**. Á þessu stigi er leiðrétting á leigusamningi tilbúin til bókunar í gegnum færslu leiðréttingabókar.

8.  Til að halda áfram að vinna úr leiðréttingu leigusamningsins og bóka leiðréttingarfærsluna skal fara í **Leiga \> Leigusamningar \> Leiðrétting leigusamnings**.
9.  Veljið kenni leigusamnings fyrir leiðréttingu á leigusamningi og veljið síðan **Leiðsagnarforrit leiðréttingar**.
10. Veljið **Næsta** þar til komið er á síðustu síðu leiðsagnarforritsins og veljið þá **Ljúka**.

Kerfið endurreiknar bókfært virði leigusamningsins til að tryggja að breytur leiðréttingarinnar sem voru samþykktar séu uppfærðar. Ef einhverjar breytingar eru til staðar er samþykktarstaðan stillt aftur á **Drög** og senda ætti leiðréttingu leigusamnings aftur inn í verkflæðiskerfið.

## <a name="view-lease-versions"></a>Skoða útgáfur leigusamnings

Ef leigusamningur hefur verið leiðréttur er hægt að skoða mismunandi útgáfur af honum. Einnig er hægt að skoða eldri áætlanir og eldri upplýsingar um leigusamning.

1. Á síðunni **Samantekt leigusamnings** skal velja leigusamning og velja síðan á aðgerðasvæðinu **Útgáfuferill leigusamnings**.

    Ef breytingar hafa verið gerðar á völdum leigusamningi birtast ólíkar útgáfur á síðunni **Útgáfuferill leigusamnings**. Upprunalegi leigusamningurinn er merktur með **1** og útgáfurnar þar á eftir með hækkandi númeraröð.

    Fyrir valda útgáfu leigusamnings er hægt að skoða fjárhagsvíddirnar, frekari upplýsingar um samninginn, staðsetningu og greiðsluáætlunarlínur.

2. Til að skoða eldri áætlanir skal opna breyttan leigusamning á síðunni **Samantekt leigusamnings** velja viðeigandi bók og velja síðan **Útgáfuferill bókar** á aðgerðasvæðinu.
3. Á síðunni **Bókaútgáfa** skal velja útgáfu og áætlun til að skoða.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]