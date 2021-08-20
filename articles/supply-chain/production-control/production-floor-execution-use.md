---
title: Hvernig starfsfólk notar viðmót fyrir framkvæmd á framleiðslugólfi
description: Þetta efnisatriði lýsir því hvernig á að nota keyrsluviðmót framleiðslugólfsins frá sjónarhóli starfsmanns.
author: johanhoffmann
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgProductionFloorExecution
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: c2215ae4162616fec892a8bce6cff5d5f68e5aa1457b41d86bb540bdcff87197
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6747866"
---
# <a name="how-workers-use-the-production-floor-execution-interface"></a>Hvernig starfsfólk notar viðmót fyrir framkvæmd á framleiðslugólfi

[!include [banner](../includes/banner.md)]

Keyrsluviðmót framleiðslugólfsins er fínstillt fyrir snertingaskipanir. Hönnun þess býður upp á sjónræna skerpu sem mætir kröfum um aðgengi fyrir umhverfi vinnusalar. Það býður upp á alla sömu virkni og verkspjaldstækið. Hins vegar gerir það líka kleift að hefja margar vinnslur samhliða úr vinnslulistanum. (Þessi möguleiki er einnig þekktur sem *vinnslusamtvinnun*.) Þar að auki, úr vinnslulista, geta starfsmenn opnað leiðbeiningu sem var búin til í leiðarvísi Microsoft Dynamics 365. Á þennan hátt er hægt að fá sjónrænar leiðbeiningar á HoloLens.

## <a name="sign-in-to-the-production-floor-execution-interface-as-a-worker"></a>Innskráning í keyrsluviðmót framleiðslugólfsins sem starfsmaður

Áður en starfsmenn geta byrjað að nota tækið þarf umsjónaraðili eða tæknimaður að undirbúa það og opna það á réttri síðu í Dynamics 365 Supply Chain Management. Frekari upplýsingar um hvernig á að setja upp tækið er að finna í [Setja upp tæki til að keyra viðmót fyrir framkvæmd á framleiðslugólfi](production-floor-execution-setup.md).

Eftir að tækið hefur verið undirbúið birtist innskráningarsíðan í því. Þessi síða sýnir upplýsingar um stöðu á vinnslum fyrir staðbundinn vinnuflokk. Þessar upplýsingar eru uppfærðar með reglulegu millibili. Á síðunni nota starfsmenn kortakennið til að skrá sig inn. Þótt starfsmenn séu ekki með notandareikning fyrir Supply Chain Management, verða þeir að vera með reikning *tímaskráðs starfsmanns* sem þeir geta notað þegar þeir skrá sig inn.

![Innskráningarsíða fyrir keyrsluviðmót framleiðslugólfs.](media/pfei-sign-in-page.png "Innskráningarsíða fyrir keyrsluviðmót framleiðslugólfs")

Eftirstandandi hlutar í þessu efnisatriði lýsa því hvernig starfsmenn nota viðmótið.

## <a name="all-jobs-tab"></a>Flipi allra starfa

Flipinn **Allar vinnslur** sýnir vinnslulista með öllum framleiðsluverkunum sem eru með stöðuna *Ekki hafið*, *Stöðvað* eða *Hafið*. (Þetta flipaheiti er stillanlegt og gæti verið annað fyrir kerfið.)

![Flipi allra starfa.](media/pfei-all-jobs-tab.png "Flipi allra starfa")

Vinnslulistinn er með eftirfarandi dálka. Tölurnar samsvara tölunum í síðustu skýringarmynd.

1. **Valdálkur** – Dálkurinn lengst til vinstri notar gátmerki til að gefa til kynna vinnslur sem starfsmaðurinn hefur valið. Starfsmenn geta valið margar vinnslur í listanum samtímis. Til að velja allar vinnslurnar á listanum skal velja gátmerkið í dálkhausnum. Þegar ein vinnsla er valin eru upplýsingar um þessa vinnslu sýndar á neðri hluta síðunnar.
1. **Dálkur vinnslustöðu** – Þessi dálkur notar tákn til að gefa til kynna stöðu hverrar vinnslu. Vinnslur með ekkert tákn í þessum dálki hafa stöðuna *Ekki hafið*. Grænn þríhyrningur gefur til kynna vinnslur sem eru með stöðuna *Hafin*. Tvær gular lóðréttar línur gefa til kynna vinnslur sem eru með stöðuna *Stöðvuð*.
1. **Dálkur með háan forgang** - Þessi dálkur notar upphrópunarmerki til að gefa til kynna vinnslur sem háan forgang.
1. **Pöntun** - Þessi dálkur sýnir númer framleiðslupöntunar fyrir vinnslu.
1. **Lýsing** – Þessi dálkur sýnir lýsingu á aðgerðinni sem vinnsla er hluti af.
1. **Umbeðið** – Þessi dálkur sýnir magnið sem áætlað er að vinnsla framleiði.
1. **Hafið** – Þessi dálkur sýnir magnið sem þegar hefur verið sett í gang fyrir vinnslu.
1. **Lokið** – Þessi dálkur sýnir magnið sem þegar hefur verið lokið fyrir vinnslu.
1. **Rýrnað** -Þessi dálkur sýnir magnið sem þegar hefur verið fært til rýrnunar fyrir vinnslu.
1. **Eftirstandandi** – Þessi dálkur sýnir magnið sem á eftir að ljúka fyrir vinnslu.

## <a name="active-jobs-tab"></a>Flipi fyrir virkar vinnslur

Fliparnir **Virkar vinnslur** sýna lista yfir allar vinnslu sem innskráður starfsmaður hefur þegar byrjað á. (Þetta flipaheiti er stillanlegt og gæti verið annað fyrir kerfið.)

![Flipi fyrir virkar vinnslur.](media/pfei-active-jobs-tab.png "Flipi fyrir virkar vinnslur")

Listinn yfir virkar vinnslur er með eftirfarandi dálkum:

- **Valdálkur** – Dálkurinn lengst til vinstri notar gátmerki til að gefa til kynna vinnslur sem starfsmaðurinn hefur valið. Starfsmenn geta valið margar vinnslur í listanum samtímis. Til að velja allar vinnslurnar á listanum skal velja gátmerkið í dálkhausnum. Þegar ein vinnsla er valin eru upplýsingar um þessa vinnslu sýndar á neðri hluta síðunnar.
- **Pöntun** - Þessi dálkur sýnir númer framleiðslupöntunar fyrir vinnslu.
- **Lýsing** – Þessi dálkur sýnir lýsingu á aðgerðinni sem vinnsla er hluti af.
- **Umbeðið** – Þessi dálkur sýnir magnið sem áætlað er að vinnsla framleiði.
- **Hafið** – Þessi dálkur sýnir magnið sem þegar hefur verið sett í gang fyrir vinnslu.
- **Lokið** – Þessi dálkur sýnir magnið sem þegar hefur verið lokið fyrir vinnslu.
- **Rýrnað** -Þessi dálkur sýnir magnið sem þegar hefur verið fært til rýrnunar fyrir vinnslu.
- **Eftirstandandi** – Þessi dálkur sýnir magnið sem á eftir að ljúka fyrir vinnslu.

## <a name="my-machine-tab"></a>Flipinn fyrir vélina mína

Flipinn **Vélin mín** gerir starfsmönnum kleift að velja eign sem er tengd við tilfang vélar innan síunnar sem er stillt í flipanum **Allar vinnslur**. Starfsmaðurinn getur síðan skoðað stöðu og ástand valinnar eignar með því að lesa gildi fyrir allt að fjóra valda teljara og lista yfir nýlegar viðhaldsbeiðnir og skráða niðurtíma. Starfsmaðurinn getur einnig beðið um viðhald fyrir valda eign og skráð og breytt niðurtíma vélar. (Þetta flipaheiti er stillanlegt og gæti verið annað fyrir kerfið.)
 
![Flipinn fyrir vélina mína.](media/pfei-my-machine-tab.png "Flipinn fyrir vélina mína")

Flipinn **Vélin mín** er með eftirfarandi dálka. Tölurnar samsvara tölunum í síðustu skýringarmynd.

1. **Eign vélar** – Veljið eign vélar sem á að fylgjast með. Byrjið á því að slá inn heiti til að velja úr lista yfir samsvarandi eignir, eða veljið stækkunarglerið til að velja úr lista yfir allar eignir sem tengjast tilföngunum sem eru innan síu vinnslulistans.

    > [!NOTE]
    > Notendur Supply Chain Management geta úthlutað hverri eign tilfangi eftir þörfum með því að nota síðuna **Allar eignir** (í flipanum **Eign** með því að nota fellilistann **Tilfang**). Frekari upplýsingar eru í [Stofna eign](../asset-management/objects/create-an-object.md).

1. **Stillingar** – Veljið tannhjólið til að opna svarglugga þar sem hægt er að velja hvaða teljara á að skoða fyrir valda eign vélar. Gildi fyrir þessa teljara eru sýnd efst í flipanum **Eignastýring**. Valmyndin **Stillingar** (sem sýnd er í eftirfarandi skjámynd) gerir notanda kleift að virkja allt að fjóra teljara. Fyrir hvern teljara sem á að virkja skal nota uppflettireitinn efst í glugganum til að velja teljara. Uppflettireiturinn sýnir alla teljarana sem tengjast eigninni sem valin er efst á síðunni **Eignastýring**. Stillið hvern teljara til að annaðhvort fylgjast með gildinu fyrir **Uppsafnað** eða síðasta gildi fyrir **Raungildi** fyrir teljarann. Til dæmis ef teljari er settur á sem fylgist með hversu margar klukkustundir vél hefur verið í notkun, þá ætti að stilla hann á **Uppsafnað**. Ef settur er á teljari til að mæla síðasta uppfærða hitastig eða þrýsting, þá ætti að stilla hann á **Raungildi**. Veldu **Í lagi** til að vista stillingarnar þínar og loka glugganum.

    ![Flipastillingar fyrir vélina mína.](media/pfei-my-machine-tab-settings.png "Flipastillingar fyrir vélina mína")

1. **Biðja um viðhald** – Veljið þennan hnapp til að opna svarglugga þar sem hægt er að stofna viðhaldsbeiðni. Hægt er að skrifa lýsingu og athugasemd. Beiðnin verður send á notanda Supply Chain Management sem getur þá breytt viðhaldsbeiðninni í verkbeiðni viðhalds.
1. **Skrá niðurtíma** – Veljið þennan hnapp til að opna svarglugga þar sem hægt er að skrá niðurtíma vélar. Hægt verður að velja ástæðukóða og slá inn dagsetningu/tímalengd niðurtímans. Skráning niðurtíma vélar er notuð til að reikna út skilvirkni á eign vélar.
1. **Skoða eða breyta** – Veljið þennan hnapp til að opna svarglugga þar sem hægt er að breyta eða skoða fyrirliggjandi færslur niðurtíma.


## <a name="starting-and-completing-production-jobs"></a>Hefja og ljúka framleiðsluvinnslum

Starfsmenn hefja framleiðsluvinnu með því að velja vinnslu í flipanum **Allar vinnslur** og velja síðan **Hefja vinnslu** til að opna svargluggann **Hefja vinnslu**.

![Svargluggi fyrir upphaf vinnslu.](media/pfei-start-job-dialog.png "Svargluggi fyrir hefja verk")

Starfsmenn nota svargluggann **Hefja vinnslu** til að staðfesta framleiðslumagnið og hefja síðan vinnsluna. Starfsmenn geta leiðrétt magnið með því að velja reitinn **Magn** og nota síðan talnaborðið sem birtist. Starfsmenn velja síðan **Hefja** til að byrja að vinna í vinnslunni. Svarglugginn **Hefja vinnslu** er lokaður og vinnslunni er bætt við flipann **Virkar vinnslur**.

Starfsmenn geta hafið vinnslu sem er með einhverja stöðu. Þegar starfsmaður setur vinnslu í gang sem er með stöðuna *Ekki hafið*, mun reiturinn **Magn** í svarglugganum **Hefja vinnslu** upphaflega sýna allt magnið. Þegar starfsmaður setur vinnslu í gang sem er með stöðuna *Hafið* eða *Stöðvað* mun reiturinn **Magn** upphaflega sýna eftirstöðvarnar.

## <a name="reporting-good-quantities"></a>Vörumagn gefið upp

Þegar starfsmaður lýkur vinnslu að fullu eða hluta til, getur hann gefið upp vörumagnið sem valin vinnsla framleiddi í flipanum **Virkar vinnslur** og síðan velja **Gefa upp framvindu**. Síðan í svarglugganum **Gefa upp framvindu** færir starfsmaðurinn inn vörumagnið með því að nota talnaborðið. Magnið er autt að sjálfgefnu. Eftir að magn er fært inn getur starfsmaðurinn uppfært stöðu vinnslunnar í *Í vinnslu*, *Stöðvað* eða *Lokið*.

![Svargluggi framvinduskýrslu.](media/pfei-report-progress-dialog.png "Svargluggi framvinduskýrslu")

## <a name="reporting-scrap"></a>Tilkynna rýrnun

Þegar starfsmaður lýkur vinnslu að fullu eða hluta til, getur hann gefið upp rýrnun með því að velja flipann **Virkar vinnslur** og síðan velja **Gefa upp rýrnun**. Síðan í svarglugganum **Gefa upp rýrnun** færir starfsmaðurinn inn magn rýrnunar með því að nota talnaborðið. Starfsmaðurinn velur einnig ástæðu (*Engin*, *Vél*, *Notandi* eða *Efni*).

![Svargluggi rýrnunarskýrslu.](media/pfei-report-scrap-dialog.png "Svargluggi rýrnunarskýrslu")

## <a name="completing-a-job-and-starting-a-new-job"></a>Vinnslu lokið og ný vinnsla hafin

Venjulega ljúka starfsmenn vinnslu með því að velja eina eða fleiri núgildandi vinnslur í flipanum **Virkar vinnslur** og velja síðan **Framvinduskýrsla**. Þeir færa síðan inn magnið sem var framleitt (vörumagnið) og stilla stöðuna á *Lokið*. Ef fleiri en ein vinnsla var valin notar starfsmaður þá hnappana **Fyrri** eða **Næsta** til að flakka á milli þeirra. Til að hefja nýja vinnslu velur starfsmaðurinn hana í flipanum **Allar vinnslur** og velur síðan **Hefja vinnslu**.

Starfsmaður getur einnig hafið nýja vinnslu á meðan fyrri vinnslan er enn opin. Aftur velur starfsmaðurinn nýju vinnsluna í flipanum **Allar vinnslur** og velur síðan **Hefja vinnslu**. Hins vegar í þessu tilviki lætur svarglugginn **Hefja vinnslu** starfsmanninn vita að hann sé að vinna í vinnslu og að hann verði þess vegna annaðhvort að stöðva eða ljúka vinnslunni áður en hann byrjar á nýrri vinnslu.

## <a name="working-on-multiple-jobs-in-parallel"></a>Unnið í mörgum vinnslum samhliða

Einn starfsmaður getur unnið í mörgum vinnslum samtímis (þ.e. samhliða). Í slíku tilfelli kallsst vinnslusafnið sem starfsmaðurinn er að vinna í *vinnslubúnt*. Starfsmaðurinn getur bætt nýjum vinnslum við búntið eða lokið við eina eða fleiri vinnslur í búnti. Eftirfarandi tvær aðstæður sýna hvernig starfsmaður getur í vinnslum samhliða.

### <a name="scenario-1-a-worker-who-has-no-active-jobs-wants-to-start-two-jobs-and-work-on-them-in-parallel"></a>Aðstæður 1: Starfsmaður er ekki með neina virka vinnslu og vill byrja á tveimur vinnslum og vinna í þeim samhliða

Starfsmaðurinn velur vinnslurnar tvær í flipanum **Allar vinnslur** og velur síðan **Hefja vinnslu**. Svarglugginn **Hefja vinnslu** sýnir báðar valdar vinnslur og getur starfsmaðurinn breytt upphafsmagninu í báðum þeirra. Starfsmaðurinn staðfestir síðan svargluggann og getur hafið báðar vinnslurnar.

### <a name="scenario-2-a-worker-who-has-two-active-jobs-that-are-in-progress-wants-to-start-a-third-job-and-work-on-it-in-parallel-with-the-other-two"></a>Aðstæður 2: Starfsmaður sem er með tvær virkar vinnslur sem eru í gangi, vill hefja þriðju vinnsluna og vinna í henni samhliða hinum tveimur

Starfsmaðurinn velur þriðju vinnsluna í flipanum **Allar vinnslur** og velur síðan **Búnt**. Í svarglugganum **Búnt** getur starfsmaðurinn leiðrétt magnið sem á að byrja á. Starfsmaðurinn staðfestir síðan svargluggann með því að velja **Búnt**.

## <a name="working-on-indirect-activities"></a>Unnið í óbeinum verkþáttum

Óbeinir verkþættir eru verkþættir sem tengjast framleiðslupöntun ekki með beinum hætti. Hægt er að skilgreina óbeina verkþætti á sveigjanlegan hátt eins og lýst er í [Setja upp óbeina verkþætti fyrir tíma og mætingu](/dynamicsax-2012/appuser-itpro/set-up-indirect-activities-for-time-and-attendance).

Til dæmis, Shannon, starfsmaður á gólfi í Contoso, vill mæta á fund fyrirtækis og fundir eru flokkaðir sem óbeinn verkþáttur. Önnur hvor af eftirfarandi aðstæðum eiga við:

- **Shannon vinnur í einu eða fleiri virkum verkum.** Shannon velur **Verkþáttur**, gerir grein fyrir verkþættinum (fundur) og staðfestir valið. Skilaboð sem birtast láta hana vita að hún sé með verk sem eru í vinnslu. Í skilaboðunum getur Shannon valið að ljúka eða stöðva verkin sem hún vinnur að áður en hún fer á fundinn.
- **Shannon er ekki með nein virk verk.** Shannon velur **Verkþáttur**, gerir grein fyrir verkþættinum (fundur) og staðfestir valið. Hún er nú skráð sem á fundinum.

Í báðum aðstæðum, eftir að Shannon staðfestir val sitt, fer hún á annaðhvort innskráningarsíðuna eða síðu sem mun bíða þess að hún staðfesti að hún hafi skilað úr óbeina verkþættinum. Síðan sem birtist fer eftir skilgreiningunni á keyrsluviðmóti framleiðslugólfsins. (Frekari upplýsingar er að finna í [Skilgreina keyrsluviðmót framleiðslugólfsins](production-floor-execution-configure.md).)

## <a name="registering-breaks"></a>Skráning hléa

Starfsmenn geta skráð hlé. Hægt er að skilgreina hlé með sveigjanlegum hætti eins og lýst er í [Laun byggð á skráningum](pay-based-on-registrations.md).

Starfsmaður skráir hlé með því að velja **Hlé** og síðan velja spjaldið sem stendur fyrir gerð hlés (t.d. hádegismatur). Eftir að starfsmaðurinn staðfestir valið sýnir tækið annaðhvort innskráningarsíðuna eða síðu sem bíður þess að starfsmaðurinn staðfesti að þeir hafi skilað úr hléinu. Síðan sem birtist fer eftir skilgreiningunni á keyrsluviðmóti framleiðslugólfsins. (Frekari upplýsingar er að finna í [Skilgreina keyrsluviðmót framleiðslugólfsins](production-floor-execution-configure.md).)

## <a name="opening-instructions"></a>Leiðbeiningar um opnun

Starfsmenn geta opnað skjal sem er hengt við verk með því að velja **Leiðbeiningar**. Hnappurinn **Leiðbeiningar** er aðeins í boði ef skjal er tengt við verkið í aðalgögnum. Til dæmis verður skjal sem er tengt við afurðina á síðunni **Útgefnar afurðir** í Supply Chain Management aðgengilegt starfsmönnum í keyrsluviðmóti vinnusalar.

## <a name="opening-mixed-reality-guides-for-hololens"></a>Leiðarvísar með blönduðum veruleika opnaðir fyrir HoloLens

[Dynamics 365 Guides](https://dynamics.microsoft.com/mixed-reality/guides/) getur eflt starfsmenn með því að bjóða upp á verklega kennslu sem notar blandaðan veruleika. Hægt er að skilgreina stöðluð ferli þar sem ítarlegar leiðbeiningar leiðbeina starfsmönnum um verkfæri og hluta sem þeir þurfa á að halda og sýna hvernig á að nota þessi verkfæri í raunverulegum aðstæðum í vinnunni. Hér er yfirlit yfir ferlið.

1. Í hvert sinn sem starfsmaður opnar verkefnalista í keyrsluviðmóti vinnusalar, finnur viðmótið alla viðeigandi leiðarvísa fyrir verkin sem eru sýnd.
1. Starfsmaðurinn velur **Leiðarvísar** til að skoða listann yfir leiðarvísa.
1. Starfsmaðurinn velur viðeigandi leiðarvísi úr listanum.
1. Keyrsluviðmót vinnusalar sýnir QR-kóða fyrir valdan leiðarvísi.
1. Starfsmaðurinn setur á HoloLens og lítur á QR-kóðann til að hefja leiðarvísinn.
1. Starfsmaðurinn vinnur í gegnum leiðarvísinn til að læra inn á verkið.

Frekari upplýsingar um hvernig á að stofna, úthluta og nota leiðarvísa fyrir HoloLens er að finna í [Láta starfsmenn í framleiðslu fá leiðarvísa með blönduðum veruleika](instruction-guides-in-production-overview.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]