---
title: Undirbúningur afurðar
description: Þetta efnisatriði útskýrir hvernig hægt er að nota undirbúningsathuganir til að ganga úr skugga um að nauðsynlegum aðalgögnum sé lokið fyrir afurð áður en hún er notuð í færslum.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 23ee82922a2103d02a4c1fe0c364fa381c4984c3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842011"
---
# <a name="product-readiness"></a>Undirbúningur afurðar

[!include [banner](../includes/banner.md)]

Hægt er að nota undirbúningsathuganir til að ganga úr skugga um að nauðsynleg aðalgögn hafi verið tilgreind fyrir afurð áður en hún er notuð í færslum. Þegar undirbúningsathuganir eru notaðar er notandi eða teymi ábyrgt fyrir því að staðfesta ákveðin fyrirframskilgreind gögn sem tengjast afurð. Ef til er opin undirbúningsathugun fyrir afurð, verður ekki hægt að losa afurðina eða nota hana í færslum.

Gátreiturinn **Virkt** fyrir hönnunarafurð, afbrigði eða útgáfu er aðeins í boði þegar búið er að færa inn og staðfesta öll nauðsynleg gögn, og þegar búið er að vinna úr öllum undirbúningsathugunum. Á þeim tímapunkti er hægt að losa afurðina, útgáfuna eða afbrigðið í annað fyrirtæki og nota í færslum. Hægt er að búa til undirbúningsathuganir fyrir nýjar afurðir, ný afbrigði og nýjar hönnunarútgáfur.

## <a name="types-of-readiness-checks"></a>Gerðir undirbúningsathugana

Það eru þrjár gerðir undirbúningsathugana:

- **Kerfisathugun** – Kerfið sannprófar hvort það sé gild færsla. Til dæmis gæti færslan verið virk uppskrift.
- **Handvirk athugun** – Notandi sannprófar hvort færslan er gild. Til dæmis gæti undirbúningsathugun krafist staðfestingar á sjálfgefnum pöntunarstillingum. Í sumum tilfellum, t.d. þegar afurð er í hönnun og verður þar af leiðandi ekki sett í birgðir, eru engar sjálfgefnar pöntunarstillingar áskildar. Hins vegar gætu sjálfgefnar pöntunarstillingar verið nauðsynlegar fyrir aðra afurð af sömu gerð vegna þess að afurðina má geyma í birgðum. Notandinn ber ábyrgð á því að taka rétta ákvörðun um hvort undirbúningsathugun sé nauðsynleg.
- **Gátlisti** - Notandi svarar spurningum á gátlista og kerfið ákvarðar hvort svörin uppfylli væntingar. Gátlistinn getur verið um hvaða viðfangsefni sem er. Til dæmis er hægt að nota hann til að ákveða hvort markaðssetningarefni eða fylgiskjölum afurðar sé lokið.

## <a name="how-readiness-checks-are-created-for-a-new-product-variant-or-version"></a>Hvernig undirbúningsathuganir eru búnar til fyrir nýja afurð, afbrigði eða útgáfu

Þegar stofnuð er ný **afurð** hönnunar, ákveður kerfið hvort regla undirbúningsathugunar hafi verið sett upp fyrir flokk hönnunarafurðar. (Hægt er að nota reglur undirbúningsathugunar fyrir stig útgefinna afurða, stiga útgefinna afbrigða og stig hönnunarútgáfu.) Ef búið er að setja upp reglu eiga sér stað eftirfarandi viðburðir:

- Undirbúningsathuganir eru búnar til fyrir afurðina samkvæmt viðeigandi reglu.
- Hönnunarútgáfan er stillt á óvirk til að loka fyrir að afurðin verði notuð. Allar útgáfur tiltekinnar afurðar sem um ræðir eru stilltar á óvirkar.

Ef nýtt **afbrigði** er stofnað fyrir afurð, athugar kerfið hvort undirbúningsathuganir hafi verið settar upp í flokki hönnunarafurðar. (Hægt er að nota undirbúningsathuganir á stigi útgefins afbrigðis og stigi hönnunarútgáfu.) Ef búið er að setja upp undirbúningsathugun eiga sér stað eftirfarandi viðburðir:

- Undirbúningsathuganir eru búnar til fyrir afurðina.
- Hönnunarútgáfan er stillt á óvirk til að loka fyrir að afurðin verði notuð.

Ef ný **útgáfa** hönnunar er stofnuð fyrir afurð, athugar kerfið hvort undirbúningsathuganir hafi verið settar upp í flokki hönnunarafurðar. (Hægt er að nota undirbúningsathuganir á stigi hönnunarútgáfu.) Ef búið er að setja upp undirbúningsathugun eiga sér stað eftirfarandi viðburðir:

- Undirbúningsathuganir eru búnar til fyrir afurðina.
- Hönnunarútgáfan er stillt á óvirk til að loka fyrir að afurðin verði notuð.

## <a name="view-readiness-checks"></a>Skoða undirbúningsathuganir

### <a name="view-open-readiness-checks-for-a-product-or-product-version"></a>Skoða opnar undirbúningsathuganir fyrir afurð eða afurðarútgáfu

Til að finna opnu undirbúningsathuganirnar fyrir afurð skal opna síðuna **Upplýsingar um losaðar afurðir**. Síðan, á aðgerðasvæðinu, í flipanum **Afurð**, í flokknum **Undirbúningsathuganir**, skal velja **Undirbúningsathuganir**.

Til að finna opnar undirbúningsathuganir fyrir útgáfu afurðar skal opna síðuna **Hönnunarútgáfur** fyrir útgefna afurð og velja útgáfu. Síðan, á aðgerðasvæðinu, í flipanum **Afurð**, í flokknum **Gátlisti**, skal velja **Undirbúningsathuganir**.

### <a name="view-open-readiness-checks-that-are-assigned-to-you"></a>Skoða opnar undirbúningsathuganir sem þú færð úthlutaðar

Til að skoða opnar undirbúningsathuganir sem eru úthlutaðar þér skal fylgja einu þessara skrefa.

- Farið í **Umsjón hönnunarbreytinga \> Almennt \> Undirbúningur afurðar \> Opnu undirbúningsathuganirnar mínar**.
- Farið í **Afurðarupplýsingastjórnun \> Vinnusvæði \> Undirbúningur afurðar fyrir afmarkaða framleiðslu**.

Uppsetningin sem tilgreinir hver fær undirbúningsathugun úthlutaða er gerð fyrir flokk hönnunarafurðar. Undirbúningsathugunum er hægt að úthluta á einstakling eða teymi. Ef undirbúningsathugun er úthlutað á teymi þarf einn einstaklingur í teyminu að vinna úr undirbúningsathuguninni. Frekari upplýsingar eru í [Hönnunarútgáfur og flokkar hönnunarafurðar](engineering-versions-product-category.md).

## <a name="process-open-readiness-checks"></a>Meðhöndla opnar undirbúningsathuganir

### <a name="process-system-and-manual-readiness-checks"></a>Meðhöndla undirbúningsathuganir kerfis og handvirkar

Þegar síðan **Undirbúningsathuganir** er opnuð, er hægt að skoða viðfangsefni undirbúningsathugana fyrir kerfið og handvirkar athuganir með því að velja **Skoða tengdar upplýsingar** á aðgerðasvæðinu. Síðan er hægt að ljúka við og/eða staðfesta gögn undirbúningsathugunar. Opnar undirbúningsathuganir hafa **Staða** gildi *Í bið*. Þessi staða gefur til kynna að enn þurfi að vinna úr undirbúningsathuguninni. Til að vinna úr undirbúningsathugun skal fylgja einu af þessum skrefum.

- Á aðgerðasvæðinu skal velja **Athuga/ljúka** til að yfirfara og ljúka undirbúningsathugun. Þegar þessu er lokið verður reiturinn **Staða** uppfærður í *Í lagi*.
- Á aðgerðasvæðinu skal velja **Sleppa** ef sleppa á undirbúningsathugun sem ekki er áskilin. Til dæmis er hægt að setja upp undirbúningsathugun fyrir verðútreikninga. Hins vegar er hægt að ákveða að sleppa þessu athuguninni á meðan afurðin er enn í hönnunaráfanganum. Í þessu tilvikum er reiturinn **Staða** uppfærður í *Sleppt*.

Háð skilgreiningunni á undirbúningsathugun, þegar reiturinn **Staða** fyrir undirbúningsathugun er uppfærður í *Í lagi*, gæti þurft að framkvæma aukaskref til að samþykkja undirbúningsathugunina. Í þessu tilvikum skal velja **Samþykki** til að ljúka við undirbúningsathugun. Þetta samþykktarskref er alltaf áskilið þegar undirbúningsathugun er sleppt.

Þegar búið er að vinna úr öllum opnum undirbúningsathugunum fyrir nýja afurð, afbrigði eða útgáfu og þær samþykktar eins og gert er ráð fyrir, verður varan sjálfkrafa virk og þar af leiðandi tilbúin til notkunar.

### <a name="process-checklist-readiness-checks"></a>Vinna úr undirbúningsathugunum gátlista

Til að opna gátlista skal opna síðuna **Undirbúningsathuganir** og síðan, í aðgerðasvæðinu, velja **Gátlisti upphafs**. Þegar gátlistanum er lokið, staðfestir kerfið hvort undirbúningsathugun hafi verið í lagi, samkvæmt stillingunum í spurningalistanum. Ef athugunin var í lagi verður reiturinn **Staða** uppfærður í *Í lagi*. Ef undirbúningsathugun er ekki áskilin er hægt að sleppa henni. Í þessu tilvikum er reiturinn **Staða** uppfærður í *Sleppt*.

Háð skilgreiningunni á undirbúningsathugun, þegar reiturinn **Staða** fyrir undirbúningsathugun er uppfærður í *Í lagi*, gæti þurft að framkvæma aukaskref til að samþykkja undirbúningsathugunina. Í þessu tilvikum skal velja **Samþykki** til að ljúka við undirbúningsathugun. Þetta samþykktarskref er alltaf áskilið þegar undirbúningsathugun er sleppt.

Þegar búið er að vinna úr öllum opnum undirbúningsathugunum fyrir nýja afurð, afbrigði eða útgáfu og þær samþykktar eins og þörf er á, verður varan sjálfkrafa virk og þar af leiðandi tilbúin til notkunar.

## <a name="create-and-manage-product-readiness-policies"></a>Stofna og stjórna reglum um undirbúning afurðar

Notið reglur um undirbúning afurðar til að stjórna undirbúningsathugunum sem eiga við um afurð. Vegna þess að undirbúningsreglu er úthlutað á hönnunarflokk, eiga allar athuganir í undirbúningsreglunni við allar hönnunarafurðirnar sem byggja á hönnunarflokknum. Frekari upplýsingar eru í [Hönnunarútgáfur og flokkar hönnunarafurðar](engineering-versions-product-category.md).

Hver undirbúningsregla inniheldur safn af undirbúningsathugunum. Þegar undirbúningsreglu er úthlutað á flokk hönnunarafurðar, verða allar afurðir sem eru stofnaðar út frá þeim flokki hönnunarafurða með undirbúningsathuganirnar sem eru gefna upp í undirbúningsreglunni.

Til að vinna með undirbúningsreglum afurðar skal fara í **Umsjón hönnunarbreytinga \> Uppsetning \> Undirbúningsreglur afurðar**. Fylgið svo einu af eftirfarandi skrefum.

- Til að stofna nýjan flokk skal velja **Ný** á aðgerðasvæðinu og síðan stilla reitina eins og lýst er í eftirfarandi undirköflum.
- Til að breyta fyrirliggjandi reglu skal velja hana úr listasvæðinu, velja **Breyta** á aðgerðasvæðinu og síðan stilla reitina eins og lýst er í eftirfarandi undirköflum.
- Til að eyða fyrirliggjandi reglu skal velja hana á listasvæðinu, velja **Breyta** á aðgerðasvæðinu, og síðan í flýtiflipanum **Almennt** skal ganga úr skugga um að valkosturinn **Virkur** sé stilltur á *Nei*. Veljið svo **Eyða** á aðgerðasvæðinu.

### <a name="header"></a>Haus

Stillið eftirfarandi reiti í haus undirbúningsreglu afurðar.

| Svæði | lýsing |
|---|---|
| Nafn | Færið inn heiti fyrir regluna. |
| lýsing | Færðu inn lýsingu á reglunni. |

### <a name="general-fasttab"></a>Flýtiflipinn Almennt

Stillið eftirfarandi reiti í flýtiflipanum **Almennt** í undirbúningsreglu afurðar.

| Svæði | lýsing |
|---|---|
| Gerð afurðar | Veljið hvort reglan eigi við um afurðir af gerðinni *Vara* eða *Þjónusta*. Ekki er hægt að breyta þessari stillingu eftir að búið er að vista færsluna. |
| Í gangi | Nota skal þennan valkost til að auðvelda að vinna með undirbúningsreglurnar. Stillið þetta á *Já* fyrir allar undirbúningsreglur sem eru notaðar. Stillið þetta á *Nei* til að merkja undirbúningsreglu sem óvirka þegar hún er ekki notuð. Athugið að ekki er hægt að gera undirbúningsreglu óvirka sem er úthlutað á flokk hönnunarafurðar, og aðeins er hægt að eyða óvirkum undirbúningsreglum. |

### <a name="readiness-control-fasttab"></a>Flýtiflipi undirbúningsstjórnunar

Fyrir hverja gerð undirbúningsathugunar sem á að hafa með í reglunni skal bæta við línu í flýtiflipanum **Stjórnun undirbúnings**. Notið eftirfarandi hnappa á tækjastiku flýtiflipans til að bæta við og fjarlægja línur eins og þörf er á:

- **Bæta við athugun** - Bætið staðlaðri undirbúningsathugun við regluna. Þegar þessi hnappur er valinn birtist svarglugginn **Bæta við athugun**. Þar er hægt að velja úr lista yfir tiltækar athuganir.
- **Bæta fyrirliggjandi spurningalista við** – Bæta auðri línu við hnitanetið. Síðan er hægt að úthluta fyrirliggjandi spurningalista með því að stilla reitina í eftirfarandi töflu.
- **Afrita** – Bæta afriti af valinni línu við hnitanetið.
- **Eyða** – Eyða völdu línunni úr hnitanetinu.

Stillið eftirfarandi reiti fyrir hverja línu sem er bætt við.

| Svæði | lýsing |
| --- | --- |
| Úrvinnslusvæði | Veljið svæðið sem athugunin tengist. |
| Gerð | Veljið hvort athugunin er kerfisathugun, handvirk athugun eða gátlisti (spurningalisti). |
| Nafn | Ef merkt er við gátlista skal færa inn heiti. Þetta svæði er sjálfkrafa stillt fyrir kerfisathugun og handvirka athugun. |
| lýsing | Ef gátlisti er valinn skal færa inn lýsingu. Þetta svæði er sjálfkrafa stillt fyrir kerfisathugun og handvirka athugun og lýsingin útskýrir gerð athugunar. |
| Gera skoðun þann | Veljið hvort línan eigi að búa til undirbúningsathuganir sem svar við nýrri útgefinni afurð, útgefnu afbrigði eða útgefinni útgáfu. |
| Keyra í | Veljið hvort undirbúningsathuganir sem línan býr til eigi við um öll fyrirtæki eða eitt fyrirtæki. |
| Fyrirt.   | Ef reiturinn **Framkvæma í** er stilltur á *Eitt fyrirtæki* skal velja fyrirtækið. |
| Gerð eiganda | Veljið hvort undirbúningsathugun sem línan myndar eigi að úthluta á einstakling eða hóp. |
| Eigandi | Velja skal einstaklinginn eða hópinn sem úthluta á athugun undirbúnings sem lína myndar á. |
| Spurningalisti | Veljið spurningalistann sem á að nota fyrir gátlistann. Gátlistinn er staðbundinn gátlisti innan fyrirtækisins þar sem undirbúningsathugun er framkvæmd. Kerfið þarf að geta metið hvort gátlistanum hafi verið svarað rétt. Þess vegna þarf að setja upp gátlistann þannig að mat sé framkvæmt út frá réttum svörum. Frekari upplýsingar um hvernig á að stofna spurningalista er að finna í [Nota spurningalista](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/using-questionnaires) og tengdum efnisatriðum þess. |
| Sjálfvirkt samþykki | Færslur undirbúningsathugunar fela í sér gátreitinn **Samþykkt** sem tilgreinir samþykktarstöðuna. Veljið gátreitinn **Sjálfvirkt samþykki** fyrir athuganir sem á að stilla á samþykktar um leið og úthlutaður notandi lýkur þeim. Hreinsið þennan gátreit til að krefjast beins samþykkis sem viðbótarskrefs. |
| Skylda | Veljið þennan gátreit fyrir athuganir sem notandi sem fékk hana úthlutaða verður að ljúka. Ekki er hægt að sleppa áskyldum athugunum. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]