---
title: Forgangsröðuð áætlun
description: Þessi grein lýsir eiginleikanum forgangsraðaðri áætlanagerð frá Microsoft Dynamics 365 Supply Chain Management.
author: t-benebo
ms.date: 10/15/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-10-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 1a952fe5734f01325842a8a130b9322eadc67951
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740593"
---
# <a name="priority-based-planning"></a>Forgangsröðuð áætlun

[!include [banner](../../includes/banner.md)]

Þessi grein lýsir eiginleikanum forgangsraðaðri áætlanagerð frá Microsoft Dynamics 365 Supply Chain Management. Eiginleikinn bætir við stuðningi við eftirspurnardrifna áætlanagerð, sem er eitt skref í [Eftirspurnarstýrð efnisþarfaráætlun (DDMRP)](ddmrp-overview.md). Forgangsröðuð áætlun gerir kerfinu kleift að búa til áætlaðar pantanir sem ráðast af forgangsröðun áætlana í stað dagsetning þarfa.

Forgangsröðuð áætlun gerir þér kleift að forgangsraða áfyllingarpöntunum til að tryggja að brýnni eftirspurn sé forgangsraðað fram yfir minna mikilvæga eftirspurn. Til dæmis verður áfyllingarpöntun vegna efnisskorts sett í forgang fram yfir hefðbundna áfyllingarpöntun. Kerfið getur sjálfkrafa skipt stærri pöntunum í aðskildar minni pantanir þar sem pöntunarlínur eru flokkaðar eftir forgangi. Það getur þá unnið úr öllum pöntunum með miklum forgangi.

Til að fá stutt yfirlit yfir þennan eiginleika skaltu skoða eftirfarandi myndskeið: [Stuðningur við fínstillingu skipulagningar fyrir forgangsraðaða áætlun í Dynamics 365 Supply Chain Management.](https://youtu.be/GmMHzFETTQc)

## <a name="turn-on-priority-based-planning-in-your-system"></a>Kveiktu á forgangsröðuð áætlun í kerfinu þínu

Áður en hægt er að nota þennan eiginleika þarf að kveikja á honum í kerfinu. Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikja á honum. Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:

- **Eining:** *Aðaláætlanagerð*
- **Heiti eiginleika:** *Forgangsraðaður stuðningur við MRP fyrir fínstillingu skipulagningar*

## <a name="where-and-how-planning-priorities-are-assigned"></a>Hvar og hvernig forgangi við áætlun er úthlutað

Upplýsingar um *Forgangur í áætlanagerð* framboð og eftirspurn er grunnurinn í forgangur í áætlunargerð. Forgangur í áætlanagerð skilgreinir mikilvægi eftirspurnar eða framboðslínu. Aðaláætlanagerð notar það þegar reiturinn **Þekjukóði** er stilltur á *Forgangur*.

Forgangur í áætlanagerð er yfirleitt tala á milli 0 (núll) og 100, þar sem 0 táknar hæsta mikilvægi. Það er sýnt og stillt í reitnum **Forgangur í áætlanagerð**. Þú finnur þennan reit á eftirfarandi síðum: **Eftirspurnarspárlínur**, **Upplýsingar um sölupöntun**, **Upplýsingar um innkaupapöntun**, **Upplýsingar um flutningspöntun** og **Upplýsingar um áætlaða pöntun**.

Þegar reiturinn **Þekjukóði** fyrir viðkomandi vöru eða þekjuflokk er stilltur á *Forgangur* jafnar aðaláætlanagerð framboðið við eftirspurn með því að nota eftirspurnarstýrða nálgun þar sem það reiknar út forgang í áætlanagerð og, fyrir hverja vöru sem er losuð, tekur tillit til gildanna sem eru sett fyrir reitina **Lágmark**, **Endurpöntunarmark** og **Hámark** á síðunni **Vöruþekja**.

> [!NOTE]
> Gildið *Forgangur* er aðeins tiltækt í reitnum **Þekjukóði** þegar fínstilling skipulagningar er virk.

Tengd *forgangslíkan fyrir áætlanagerð* stjórna forgangi í áætlunargerð og skipta áætluðum pöntunum eftir forgangssviði. Þeir leyfa þér einnig að stilla sjálfgefin gildi forgangs í áætlunargerð fyrir hverja tegund framboðs eða eftirspurnar og skilgreina útreikningsaðferð fyrir forgangs.

## <a name="types-of-priority-calculation-methods"></a>Gerðir reikningsaðferð forgangs

Í hverju forgangslíkani fyrir áætlanagerð er **Útreikningsaðferð fyrir forgang** þar sem kemur fram hvernig aðaláætlanagerð beitir forgangi við áætlaðar pantanir. Tiltæk gildi eru *Prósenta af hámarki birgðamagns* og *Forgangssvið*. *Forgangssvið* táknar ítarlegri útgáfu af aðferðinni *Prósenta af hámarki birgðamagns*.

### <a name="percent-of-maximum-inventory-quantity"></a>Prósenta af hámarki birgðamagns

Í útreikningsaðferðinni *Prósenta af hámarki birgðamagns*, finnur útreikningsaðferð birgðaforgangs núverandi *allt tiltækt birgðamagn* (nettóflæði) sem prósentuhlutfall af **Hámarksbirgðamagni** sem sett er fyrir vöru. Þá er búin til ein áætluð pöntun fyrir hverja vöru og lánardrottinn (nema hámarks pöntunarmagn sé notað til að þvinga skiptingu). Skipulagsforgangur pöntunarinnar er reiknaður sem prósenta af hámarkinu.

Eftirfarandi formúla er notuð:

*Prósentuhlutfall hámarks* = (*Nettóflæðisstaða* × 100) ÷ *Hámarks birgðamagn frá vöruþekju*

Í þessari formúlu er *Nettóflæðisstaða* reiknuð á eftirfarandi hátt:

*Nettóflæðisstaða* = *Á lager* + *Í pöntun* – *Viðurkennd eftirspurn*

- *Í pöntun* eru áætlaðar birgðir.
- *Viðurkennd eftirspurn* táknar nettókröfur sem hafa kröfudagsetningu innan tímamörk áætlunartímans.

Meðan á aðaláætlunarkeyrslu stendur eru nýjar áætlaðar pantanir búnar til þegar nettóflæðistaða er minni en magn endurpöntunarmarks vöru. Fyrirhugað pöntunarmagn vöru er mismunurinn á milli gildi **Hámarksbirgðamagns** sem er stillt á vöruna og nettóflæðisstöðu. Fyrirhuguð forgangsröðun pöntunar er reiknuð sem *nettóflæðisstaða* sem prósenta af **Hámarksbirgðamagni**.

> [!NOTE]
> Reiknaður forgangur má ekki vera neikvæður, jafnvel þótt eftirspurn sé meiri en heildarframboð. Ef eftirspurn er meiri en framboðið í heild er reiknaður forgangur stilltur á 0 (núll).

### <a name="priority-ranges"></a>Forgangssvið

Útreikningsaðferðin *Forgangssvið* er ítarlegri en aðferðin *Prósentuhlutfall hámarksbirgða* og er stillt á stigi forgangslíkan fyrir áætlanagerð. Hægt er að stofna nokkrar nýjar áætlaðar birgðapantanir til að anna eftirspurn á vöru. Forgangsröðun áætlaðs framboðs er í samræmi við þau gildi sem skilgreind eru í hnitanetinu **Forgangssvið áætlanagerðar** á síðunni **Forgangslíkön fyrir áætlanagerð**.

Eftirfarandi viðbótarreglur taka gildi þegar **Útreikningsaðferð forgangs** er settur á *Forgangssvið*:

- Ef valkosturinn **Íhugaðu forgang eftirspurnar** fyrir áætlað forgangslíkan er stilltur á *Já* mun forgangur sem er stilltur á hverja eftirspurnarlínu takmarka ramma forgangssviðið. Forgangur allra nýrra áætlaðra pantana um framboð verður ekki minni en eftirspurnarinnar. Efra gildi sviðsins er talið þröskuldur sem forganggildi eftirspurnarinnar er borið saman við. Ef forgangur kröfunnar er nákvæmlega mitt á milli efri þröskuldsgilda tveggja sviða, verður valið það svið sem hefur mestan forgang (þ.e. lægsta forganggildi).
- Ef reiturinn **Stofnun áætlaðrar pöntunar** fyrir áætlaða forgangslíkan er stilltur á *Framboð með mikilvægastan forgang*, verður aðeins eitt framboð búið til að uppfylla alla leið upp að hámarki. Forgangurinn verður stilltur á forgang fyrsta sviðsins sem setur af stað framboð.
- Ef engar lagerbirgðir, ekkert framboð og engin eftirspurn eru til staðar verður línan í hnitanetinu **Forgangssvið áætlanagerðar** þar sem reiturinn **Frá magn** er stillt á *Núll* notuð.
- Ef eftirspurn er til staðar, en engar lagerbirgðir eða áætlað framboð, verður línan í hnitanetinu **Forgangssvið áætlanagerðar** þar sem **Frá magn** er stillt á *Núll eða minna* notuð.
- Þegar sviðið sem eftirspurnin er hluti af er metið hefur stillingin **Íhugaðu forgang eftirspurnar** áfram áhrif.

## <a name="differences-between-traditional-timeline-calculations-and-priority-based-planning"></a>Munur á hefðbundnum útreikningum tímalínu og forgangsbundinni áætlanagerð

Forgangsröðuð áætlun er frábrugðið hefðbundnum tímalínuútreikningum á eftirfarandi hátt:

- Allir fyrirframáætlaðir úrvinnsluaðilar eru enn í gildi. Slíkir forvinnsluaðilar eru m.a. þarfarakning samþykktra áætlaðra pantana gegn sölueftirspurn, vörpun innkaupabeiðni og frátekningarrök. Aðeins er unnið úr eftirspurn sem er ekki uppfyllt af þessum forvinnsluaðilum.
- Á meðan á þarfarakningu stendur eru allar birgðir teknar til skoðunar, óháð forgangi þeirra. Framboð felur í sér lagerbirgðir, losaðar birgðir og ófestan hluta samþykktra áætlaðra pantana.
- Ekki er hægt að festa „neikvæða daga“ á framboð allan þekjutímann.
- Þegar framboðið er fast við eftirspurn er framboðið sem hefur mestan forgang (þ.e. lægsta forganggildi) notað fyrst. Birgðir á lager er talin hafa forgangsgildi 0 (núll). Þar af leiðir verður það notað sem fyrsti uppruni.
- Nýjar áætlaðar framboðslínur verða búnar til samkvæmt hefðbundnum reglum um lágmarksstærð pöntunar, hámarksstærð pöntunar, margföldun magns og svo framvegis.

## <a name="planning-priority-models"></a>Forgangslíkön fyrir áætlanagerð

*Forgangslíkön fyrir áætlanagerð* er skipað í þekjuflokka og stýra forgangi í áætlunargerð fyrir áætlaðar pantanir. Þau skilgreina rökin sem ákvarða hvernig gildi forgangur í áætlunargerð er reiknað fyrir hverja áætlaða pöntun og hvernig forgangsröðun er úthlutað á áætlaðar pantanir, framboðslínur og eftirspurnarlínur.

Til að vinna með forgangslíkan fyrir áætlanagerð skal fara í **Aðaláætlanagerð \> Uppsetning \> Forgangslíkön fyrir áætlanagerð**. Eins og áður var fjallað um er ein mikilvægasta stilling líkans gildið **Útreikningsaðferð forgangs**. Þessi stilling stjórnar útreikningsaðferðinni sem er notuð þegar aðaláætlanagerð úthlutar forgangsgildi áætlaðar pantanir.

> [!NOTE]
> Forgangslíkön fyrir áætlanagerð gilda fyrir allt fyrirtækið þvert á alla lögaðila.

### <a name="coverage-group"></a>Þekjuflokkur

Stofnaðu nýjan þekjuflokk sem þú hyggst nota fyrir forgangsmiðaða áætlunargerð eins og lýst er í [Skilgreina þekjureglur fyrir vörur](../tasks/define-coverage-rules-items.md). Þegar þú hefur búið til þekjuflokkinn skaltu stilla eftirfarandi reiti til viðbótar:

- **Þekjukóði** – Veldu *Forgangur* ef þekjuflokkurinn notar forgangsbundna áætlanagerð.
- **Forgangslíkan fyrir áætlanagerð** – Veldu hvaða forgangslíkan fyrir áætlanagerð sem er fyrir allat fyrirtækið.

### <a name="item-coverage"></a>Vöruþekja

Setja upp stillingar þekju eins og lýst er í [Þekjustillingar](../coverage-settings.md). Sjálfgefið er að gildi **Þekjuflokks** sem valinn er fyrir þekjuflokkinn sé afritað í stillingum vöruþekju.. Hins vegar er hægt að hnekkja sjálfgildi eftir þörfum. Í sumum tilvikum er reiturinn **Þekjukóði** fyrir þekjufærsla vöru stilltur á *Áætlunargerð*, en ekkert forgangslíkan fyrir áætlanagerð er skilgreint fyrir tengdan þekjuflokk. Í þessum tilvikum eru sjálfgefið notuð öll líkön þar sem reiturinn **Útreikningsaðferð forgangs** stilltur á *Prósentuhlutfall hámarksbirgða* og reiturinn **Stofnun áætlaðrar pöntunar** er stilltur á *Framboð með mikilvægastan forgang*.

Stilltu reitinn **Þekjukóði** á *Forgangur* til að gera reitinn **Endurpöntunarmark** í vöruþekjustillingunum tiltækan. Í þessum reit sláið inn magn endurpöntunarmarks sem á að nota þegar tekin er ákvörðun um hvenær skuli leggja inn áætlaðar pantanir sem eru með **Þekjukóði** gildi *Forgangur*.

Magn endurpöntunarmarks er oft reiknað sem eftirspurn á afhendingartíma plús lágmarksgildi (öryggisbirgðir). Það verður að vera gildi á milli **Lágmark** og **Hámark** gilda.

Til dæmis væri hægt að stilla reitina á eftirfarandi hátt:

- **Lágmark:** *10*
- **Endurpöntunarmark:** *45*
- **Hámark:** *60*

Til dæmis, þetta endurpöntunarmarksmagn er byggt á sjö daga afhendingartíma og daglegri notkun að meðaltali 5. Þess vegna er eftirspurnin á afhendingartíma 35. Við þetta er bætt lágmarksgildinu 10 (öryggisbirgðum) þannig að niðurstaðan verði endurpöntunarmark upp á 45. Þegar þessi uppsetning er notuð verður framboð lagt til þegar áætluð staða á lager fer undir 45. Forgangsröðunin verður byggð á uppsetningu forgangs í áætlunargerð.

### <a name="manage-planning-priority-models"></a>Stjórna forgangslíkönum fyrir áætlanagerð

Til að vinna með forgangslíkön fyrir áætlanagerð. skaltu fylgja þessum leiðbeiningum.

1. Fara skal í **Aðaláætlanagerð \> Uppsetning \> Forgangslíkön fyrir áætlanagerð**.
1. Veldu núverandi líkan á listasvæðinu eða veldu **Nýtt** á aðgerðasvæðinu til að búa til nýjan.
1. Í haus færslunnar skal stilla eftirfarandi reiti:

    - **Heiti** - Færið inn heiti fyrir líkanið. Heitið verður að vera einkvæmt hjá öllum lögaðilum innan fyrirtækisins.
    - **Lýsing** – Færið inn lýsingu á líkan.
    - **Reikningsaðferð forgangs** – Veljið eitt af eftirfarandi gildum:

        - *Forgangssvið* – Þegar þetta gildi er hnitanetið **Forgangssvið áætlanagerðar** tiltækt. Þar verður þú að setja upp nokkur forgangssvið til að skilgreina gildi forgangs í áætlanagerð.
        - *Prósenta af hámarki birgðamagns* – Reikna út forgangsgildið sem prósentuhlutfall samkvæmt áætlaðri efnislegri birgðastöðu af hámarki birgðamagns.

    - **Útreikningsaðferð forgangs** - Þessi reitur er tiltækur þegar reiturinn **Útreikningsaðferð forgangs** er settur á *Forgangssvið*. Veljið eitt af eftirfarandi gildum:

        - *Framboð með mikilvægastan forgang* – Ekki skipta niður áætluðum pöntunum samkvæmt forgangssviðinu. Forgangur í áætlanagerð fyrir áætlaða pöntun er byggður á mikilvægasta forgangssviðinu (þ.e. lægsta forgangssvið áætlanagerðar).
        - *Skipta samkvæmt forgangssviðum* – Skipta eftirspurn í margar áætlaðar pantanir, byggt á forgangssviðum áætlanagerðar. Forgangur í áætlanagerð fyrir einstakar áætlaðar pantanir er skilgreindur af forgangi í áætlanagerð á tengdu forgangssviði.

    - **Íhuga forgang eftirspurnar** – Stillið þennan valkost á *Já* til að takmarka forgang nýrrar áætlaðrar pöntunar sem er búin til fyrir framboð. (Forgangurinn verður ekki lægri en tengd eftirspurn). Ef þessi valkostur er stilltur á *Nei* verður forgangur eftirspurnarpöntunar ekki tekinn til greina þegar forgangur birgðapöntunar er reiknaður út.

1. Ef þú stillir reitinn **Útreikningsaðferð forgangs** á *Forgangssvið* skaltu nota hnappinn **Bæta við** og **Fjarlægja** á tækjastiku flýtiflipans **Forgangssvið áætlanagerðar** til að bæta við eða fjarlægja forgangssviðslínum eins og þú krefst. Ef margar línur eru til og þú setur inn nýja línu, þá er forgangur í áætlunargerð sjálfkrafa stillt á meðaltal valinnar línu og línu fyrir ofan hana. Fyrir hverja línu skal stilla eftirfarandi reiti:

    - **Forgangur í áætlanagerð** – Sláðu inn gildi á bilinu 0,00 til 100,00. Þetta gildi táknar forgang í áætlunargerð sem er notaður fyrir línuna. Lægsta forgangsgildið táknar hæsta forgangsgildið. Sjálfgefið gildi er úthlutað en hægt er að breyta því eftir þörfum. Ekki er hægt að nota sama **forgang í áætlunargerð** fyrir fleiri en eitt forgangssvið áætlanagerðar fyrir sama forgangslíkan fyrir áætlanagerð.
    - **Lýsing** – Færið inn lýsingu á forgangssviði áætlunargerðar (eins og *Endurpöntunarmark að hámarki*).
    - **Frá-magn** – Neðri mörkum forgangssviðs áætlanagerðar. Þetta gildi er skrifvarið og miðast við er búið til sjálfkrafa út frá gildunum **Til-magni** og **Prósenta af til-magni**.
    - **Til magn** – Veljið reitinn úr vöruþekju sem nota skal til að skilgreina efri mörk sviðsins. Eftirfarandi gildi eru studd og hafa þau áhrif á gildið **Frá magn** á næsta sviði:

        - *Núll* – Þetta gildi stendur fyrir neikvætt till núllsvið (*Núll eða minna* til *Núll*). Fyrir línur þar sem þetta gildi er valið er **Prósent af til magni** skrifvarin og er alltaf stillt á *100* prósent.
        - *Lágmarksbirgðamagn* – Þetta gildi stendur **Lágmarksgildi** fyrir vöru á síðunni **Vöruþekja**. Fyrir línur þar sem þetta gildi er valið er hægt að breyta reitnum **Prósent af til magni** og er notaður til að stilla gildið **Frá-magn** í næsta sviði (t.d. í *80% af Lágmarksmagni birgða*).
        - *Endurpöntunarmark* – Þetta gildi stendur fyrir gildið **Endurpöntunarmark** fyrir vöru á síðunni **Vöruþekja**. Fyrir línur þar sem þetta gildi er valið er hægt að breyta reitnum **Prósent af til magni** og er notaður til að stilla gildið **Frá-magn** fyrir næsta sviði (t.d. í *80% af endurpöntunarmarki*).
        - *Hámarksbirgðamagn* – Þetta gildi stendur **Hámarksgildi** fyrir vöru á síðunni **Vöruþekja**. Fyrir línur þar sem þetta gildi er valið er hægt að breyta reitnum **Prósent af til magni** og er notaður til að stilla gildið **Frá-magn** næsta sviðs (t.d. í *80% af Lágmarksmagni birgða*).
        - *Ótakmarkað* – Þetta gildi táknar ótakmarkað efra stig sviðsins (*Ótakmarkað eða minna* til *Ótakmarkað*). Fyrir línur þar sem þetta gildi er valið er **Prósent af til magni** skrifvarin og er alltaf stillt á *100* prósent.

    - **Prósent af til magni** – Sláðu inn prósentugildi sem er notað til að reikna efri mörk forgangssviðs áætlanagerðar, byggt á gildinu sem er valið í reitnum **Til magn**. Til dæmis ef reiturinn **Til-magn** er stillt á *Lágmarksmagn birgða* og reiturinn **Prósent af til-magni** er stillt á *50*, verða efri mörkin 50% af lágmarksbirgðagildi í tengdri vöruþekju.

1. Á flýtiflipanum **Sjálfgildi forgangs í áætlanagerð** stilltu þá reiti sem þú krefst til að skilgreina sjálfgildi forgangs í áætlunargerð fyrir hverja framboðs- eða eftirspurnarlínu (sölupöntun, innkaupapöntun, flutningspöntun eða eftirspurnarspá). Aðeins er hægt að færa inn jákvæð gildi.

## <a name="view-and-maintain-planning-priority"></a>Skoða og vinna með forgang í áætlunargerð

Forgangur í áætlanagerð birtist og er stillt reitnum í **Forgangur í áætlanagerð**. Þetta svæði er að finna á síðunum sem eru taldar upp í eftirfarandi töflu. Forgangurinn er stillt sem tala á milli 0 (núll) og 100, þar sem 0 táknar hæsta mikilvægi.

| Síða | Svæðastaðsetning | Gildisgjafi |
|---|---|---|
| Eftirspurnarspárlínur | <p>Flipinn **Vara**</p><p>(Veljið línu í efri hlutanum og veljið síðan flipann **Vara**).</p> | Sjálfgefið gildi eða gildi sem er stillt handvirkt |
| Upplýsingar um sölupöntun | <p>Flipinn **Afhending** á flýtiflipanum **Upplýsingar um línu**</p><p>(Veljið línu á flýtiflipanum **Sölupöntunarlínur** og síðan flýtiflipann **Upplýsingar um línu**, veljið flipann **Afhending**).</p> | Sjálfgefið gildi, gildi innan samstæðu eða gildi sem er stillt handvirkt |
| Upplýsingar um innkaupapöntun | <p>Flipinn **Afhending** á flýtiflipanum **Upplýsingar um línu**</p><p>(Veljið línu á flýtiflipanum **Innkaupapöntunarlínur** og síðan flýtiflipann **Upplýsingar um línu**, veljið flipann **Afhending**).</p> | Gildi sem sett er við festingu frá áætluðum pöntunum, gildi innan samstæðu eða gildi sem er stillt handvirkt |
| Upplýsingar um flutningspöntun | <p>Flipinn **Afhending** á flýtiflipanum **Upplýsingar um línu**</p><p>(Veljið línu á flýtiflipanum **Flutningspöntunarlínur** og síðan flýtiflipann **Upplýsingar um línu**, veljið flipann **Afhending**).</p> | Gildi sem er stillt við staðfesting frá áætluðum pöntunum eða gildi sem er stillt handvirkt |
| Upplýsingar tillögu | Flýtiflipinn **Almennt** | Gildi sem er reiknað við aðaláætlanagerð eða gildi sem er stillt handvirkt |

### <a name="intercompany-trade"></a>Samstæðuviðskipti

Gildi **Forgangs í áætlunargerð** um framboð innan samstæðu og eftirspurnarlínur er deilt á milli tengdra aðila. Breyting á hvorri hlið kemur fram á tengdu pöntunarlínunni.

Hér eru nokkur dæmi:

- Notandi breytir forgangur í áætlunargerð fyrir samstæðusölupöntunarlínu úr 20 í 30. Þessi breyting kemur fram á tengdri samstæðuinnkaupapöntunarlínu.
- Notandi breytir forgangur í áætlunargerð fyrir samstæðuinnkaupapöntunarlínu úr 40 í 50. Þessi breyting endurspeglast í tengdri sölupöntunarlínu innan samstæðu.
