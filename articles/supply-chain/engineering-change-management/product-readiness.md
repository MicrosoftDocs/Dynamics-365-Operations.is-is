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
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 4286f72f9aed1b4dd91e7c45203cfab2af43f3c2
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571954"
---
# <a name="product-readiness"></a>Undirbúningur afurðar

[!include [banner](../includes/banner.md)]

Hægt er að nota undirbúningsathuganir til að ganga úr skugga um að nauðsynleg aðalgögn hafi verið tilgreind fyrir afurð áður en hún er notuð í færslum. Þegar undirbúningsathuganir eru notaðar er notandi eða teymi ábyrgt fyrir því að staðfesta ákveðin fyrirframskilgreind gögn sem tengjast afurð.

Hægt er að haka í gátreitinn **Virkt** fyrir hönnunarafurð, afbrigði eða útgáfu þegar búið er að færa inn og staðfesta öll nauðsynleg gögn, og þegar búið er að vinna úr öllum undirbúningsathugunum. Ef ekki hefur verið unnið úr einni eða fleiri athugunum fyrir afurðina, útgáfuna eða afbrigðið, þá færðu tilkynningu um að ekki hafi verið lokið við allar athuganir þegar þú reynir að merkja við gátreitinn **Virkt**.

Hægt er að búa til undirbúningsathuganir fyrir nýjar hönnunarafurðir, afbrigði og útgáfur. Einnig er hægt að nota undirbúningsathugunir á staðlaðar (ekki hannaðar) afurðir (sjá einnig [Undirbúningsathuganir á stöðluðum afurðum](#standard-products)). 

Þú getur notað staðlaðar afurðir í viðskiptum jafnvel þótt ekki sé búið að ljúka öllum undirbúningsathugunum. Ef þú þarft að loka fyrir að afurð sé notuð í viðskiptum skaltu nota líftímastöðu hennar. Þú getur úthlutað líftímastöðu sem kemur í veg fyrir að afurð sé notuð í viðskiptum og síðan, eftir að öllum undirbúningsathugunum er lokið, úthlutað nýrri líftímastöðu sem leyfir nauðsynlegar færslur.

## <a name="types-of-readiness-checks"></a>Gerðir undirbúningsathugana

Það eru þrjár gerðir undirbúningsathugana:

- **Kerfisathugun** – Kerfið sannprófar hvort það sé gild færsla. Til dæmis gæti færslan verið virk uppskrift.
- **Handvirk athugun** – Notandi sannprófar hvort færslan er gild. Til dæmis gæti undirbúningsathugun krafist staðfestingar á sjálfgefnum pöntunarstillingum. Í sumum tilfellum, t.d. þegar afurð er í hönnun og verður þar af leiðandi ekki sett í birgðir, eru engar sjálfgefnar pöntunarstillingar áskildar. Hins vegar gætu sjálfgefnar pöntunarstillingar verið nauðsynlegar fyrir aðra afurð af sömu gerð vegna þess að afurðina má geyma í birgðum. Notandinn ber ábyrgð á því að taka rétta ákvörðun um hvort undirbúningsathugun sé nauðsynleg.
- **Gátlisti** - Notandi svarar spurningum á gátlista og kerfið ákvarðar hvort svörin uppfylli væntingar. Gátlistinn getur verið um hvaða viðfangsefni sem er. Til dæmis er hægt að nota hann til að ákveða hvort markaðssetningarefni eða fylgiskjölum afurðar sé lokið.

<a name="checks-engineering"></a>

## <a name="how-readiness-checks-are-created-for-a-new-engineering-product-variant-or-version"></a>Hvernig undirbúningsathuganir eru búnar til fyrir nýja hönnunarafurð, afbrigði eða útgáfu

Hægt er að nota reglur undirbúningsathugunar fyrir stig útgefinna afurða, stiga útgefinna afbrigða og stig hönnunarútgáfu.

Þegar ný *hönnunarafurð* er stofnuð ákveður kerfið hvort [regla undirbúningsathugunar gildi](#assign-policy) um hana. Ef regla um undirbúningsathugun á við eiga eftirfarandi atburðir sér stað:

- Undirbúningsathuganir eru búnar til fyrir afurðina samkvæmt viðeigandi reglu.
- Hönnunarútgáfan er stillt á óvirk til að loka fyrir að afurðin verði notuð. Allar hönnunarútgáfur afurðarinnar eru stilltar á óvirkar.

Ef nýtt *afbrigði* er stofnað fyrir afurð, athugar kerfið hvort regla undirbúningsathuganir gildi um það. (Hægt er að nota undirbúningsathuganir á stigi útgefins afbrigðis og stigi hönnunarútgáfu.) Ef búið er að setja upp undirbúningsathugun eiga sér stað eftirfarandi viðburðir:

- Undirbúningsathuganir eru búnar til fyrir afurðina samkvæmt viðeigandi reglu.
- Hönnunarútgáfan og afbrigðið eru stillt á óvirk til að loka fyrir að afurðin verði notuð.

Ef ný *útgáfa* hönnunar er stofnuð fyrir afurð, athugar kerfið hvort regla undirbúningsathuganir gildi um það. (Hægt er að nota undirbúningsathuganir á stigi hönnunarútgáfu.) Ef regla gildir eiga sér stað eftirfarandi viðburðir:

- Undirbúningsathuganir eru búnar til fyrir afurðina samkvæmt viðeigandi reglu.
- Hönnunarútgáfan er stillt á óvirk til að loka fyrir að afurðin verði notuð.

> [!NOTE]
> Einnig er hægt að setja upp reglur fyrir undirbúningsathugun fyrir staðlaðar vörur (sem ekki eru tæknivörur). Nánari upplýsingar er að finna í hlutanum [Undirbúningsathuganir á hefðbundnum vörum](#standard-products) síðar í þessu efnisatriði.

## <a name="view-readiness-checks"></a>Skoða undirbúningsathuganir

### <a name="view-open-readiness-checks-for-a-product-or-product-version"></a>Skoða opnar undirbúningsathuganir fyrir afurð eða afurðarútgáfu

Til að finna opnu undirbúningsathuganirnar fyrir afurð skal opna síðuna **Upplýsingar um losaðar afurðir**. Síðan, á aðgerðasvæðinu, í flipanum **Afurð**, í flokknum **Undirbúningsathuganir**, skal velja **Undirbúningsathuganir**.

Til að finna opnar undirbúningsathuganir fyrir útgáfu afurðar skal opna síðuna **Hönnunarútgáfur** fyrir útgefna afurð og velja útgáfu. Síðan, á aðgerðasvæðinu, í flipanum **Afurð**, í flokknum **Gátlisti**, skal velja **Undirbúningsathuganir**.

### <a name="view-open-readiness-checks-that-are-assigned-to-you"></a>Skoða opnar undirbúningsathuganir sem þú færð úthlutaðar

Til að skoða opnar undirbúningsathuganir sem eru úthlutaðar þér skal fylgja einu þessara skrefa.

- Farið í **Umsjón hönnunarbreytinga \> Almennt \> Undirbúningur afurðar \> Opnu undirbúningsathuganirnar mínar**.
- Farið í **Afurðarupplýsingastjórnun \> Vinnusvæði \> Undirbúningur afurðar fyrir afmarkaða framleiðslu**.

Uppsetningin sem tilgreinir hver fær undirbúningsathugun úthlutaða er gerð fyrir flokk undirbúningsregla. Undirbúningsathugunum er hægt að úthluta á einstakling eða teymi. Ef undirbúningsathugun er úthlutað á teymi þarf einn einstaklingur í teyminu að vinna úr undirbúningsathuguninni.

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

Notið reglur um undirbúning afurðar til að stjórna undirbúningsathugunum sem eiga við um afurð. Hver undirbúningsregla inniheldur safn af undirbúningsathugunum. Þegar reglu undirbúningsathugunar er úthlutað á flokk hönnunarafurðar eða sameiginlega afurð, verða gerðar undirbúningsathugunir á öllum afurðunum sem tengjast þeim flokki eða sameiginlegu afurð sem hafðar eru með í undirbúningsreglunni.

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
| Í gangi | Nota skal þennan valkost til að auðvelda að vinna með undirbúningsreglurnar. Stillið þetta á *Já* fyrir allar undirbúningsreglur sem eru notaðar. Stillið þetta á *Nei* til að merkja undirbúningsreglu sem óvirka þegar hún er ekki notuð. Athugið að ekki er hægt að gera undirbúningsreglu óvirka sem er úthlutað á flokk hönnunarafurðar eða samnýtta vöru, og aðeins er hægt að eyða óvirkum undirbúningsreglum. |

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
| Fyrirtæki | Ef reiturinn **Framkvæma í** er stilltur á *Eitt fyrirtæki* skal velja fyrirtækið. |
| Gerð eiganda | Veljið hvort undirbúningsathugun sem línan myndar eigi að úthluta á einstakling eða hóp. |
| Eigandi | Velja skal einstaklinginn eða hópinn sem úthluta á athugun undirbúnings sem lína myndar á. |
| Spurningalisti | Veljið spurningalistann sem á að nota fyrir gátlistann. Gátlistinn er staðbundinn gátlisti innan fyrirtækisins þar sem undirbúningsathugun er framkvæmd. Kerfið þarf að geta metið hvort gátlistanum hafi verið svarað rétt. Þess vegna þarf að setja upp gátlistann þannig að mat sé framkvæmt út frá réttum svörum. Frekari upplýsingar um hvernig á að stofna spurningalista er að finna í [Nota spurningalista](/dynamicsax-2012/appuser-itpro/using-questionnaires) og tengdum efnisatriðum þess. |
| Sjálfvirkt samþykki | Færslur undirbúningsathugunar fela í sér gátreitinn **Samþykkt** sem tilgreinir samþykktarstöðuna. Veljið gátreitinn **Sjálfvirkt samþykki** fyrir athuganir sem á að stilla á samþykktar um leið og úthlutaður notandi lýkur þeim. Hreinsið þennan gátreit til að krefjast beins samþykkis sem viðbótarskrefs. |
| Skylda | Veljið þennan gátreit fyrir athuganir sem notandi sem fékk hana úthlutaða verður að ljúka. Ekki er hægt að sleppa áskyldum athugunum. |

<a name="assign-policy"></a>

## <a name="assign-readiness-policies-to-standard-and-engineering-products"></a>Tilgreindu undirbúningsreglur fyrir hefðbundnar afurðir og hönnunarafurðir

Þegar ný vara er stofnuð á grundvelli hönnunarflokks er bæði *útgefin vara* og tengd *sameiginleg vara* stofnuð. Hvernig undirbúningsreglur eru leystar fyrir útgefna afurð fer eftir því hvort kveikt hafi verið á eiginleikanum *Undirbúningsathuganir afurðar*. (Frekari upplýsingar er að finna í hlutanum [Undirbúningsathuganir á stöðluðum afurðum](#standard-products) síðar í þessu efnisatriði.)

- Þegar *slökkt* er á eiginleikanum *Undirbúningsathuganir afurðar* í kerfinum er undirbúningsreglan stillt og aðeins sýnd í færslum [hönnunarflokks](engineering-versions-product-category.md). Til að fá upplýsingar um hvaða regla á við um útgefna afurð athugar kerfið reitinn **Undirbúningsregla afurðar** fyrir tengdan hönnunarflokk. Hægt er að breyta undirbúningsreglunni fyrir núverandi vöru með því að breyta tengdri hönnunarafurð (ekki sameiginlegri vöru).
- Þegar eiginleikinn *Undirbúningsathuganir afurðar* er *Virkur* bætist reitur fyrir **Undirbúningsreglu afurðar** við síðuna **Afurð** (þar sem sameiginlegar afurðir eru settar upp) og á síðuna **Útgefin afurð** (þar sem gildið er skrifvarið og tekið úr tengdri sameiginlegri afurð). Kerfið finnur undirbúningsreglu fyrir útgefna afurð með því að athuga tengda sameiginlega afurð. Þegar hönnunarflokkur er notaður til að stofna nýja hönnunarafurð býr kerfið bæði til sameiginlega afurð og útgefna afurð og afritar allar stillingar á **Undirbúningsreglu afurðar** fyrir hönnunarflokkinn í nýju sameiginlegu afurðina. Síðan er hægt að breyta undirbúningsreglu fyrir fyrirliggjandi vöru með því að breyta tengdri sameiginlegri vöru (ekki útgefnum verkfræðiflokki).

Til að úthluta undirbúningsreglu fyrir sameiginlega vöru skal fylgja eftirfarandi skrefum.

1. Fara í **Afurðarupplýsingar \> Afurðir \> Afurðir**.
1. Opnaðu eða búðu til vöru sem úthluta á undirbúningsreglu fyrir.
1. Í flýtiflipanum **Almennt** skal stilla reitinn **Undirbúningsregla afurðar** á heiti reglunnar sem á að gilda um afurðina.

Til að úthluta undirbúningsreglu á hönnunarflokk skal fylgja eftirfarandi skrefum.

1. Farið í **Umsjón hönnunarbreytinga \> Uppsetning \> Upplýsingar um flokka hönnunarafurða**.
1. Opna skal eða útbúa hönnunarflokkinn sem úthluta á undirbúningsreglu a.
1. Í flýtiflipanum **Undirbúningsregla afurðar** skal stilla reitinn **Undirbúningsregla afurðar** á heiti reglunnar sem á að gilda um hönnunarflokkinn.

<a name="standard-products"></a>

## <a name="readiness-checks-on-standard-products"></a>Undirbúningsathuganir á stöðluðum afurðum

Hægt er að virkja undirbúningsathuganir afurðar fyrir staðlaðar afurðir (aðrar en hönnunarafurðir) með því að kveikja á eiginleikanum *Undirbúningsathuganir afurðar* í eiginleikastjórnun. Þessi eiginleiki gerir nokkrar smávægilegar breytingar á kerfi undirbúningsathugunar þannig að það styðji staðlaðar afurðir.

### <a name="enable-readiness-checks-on-standard-products"></a>Virkja undirbúningsathuganir á stöðluðum vörum

Til að gera kerfinu kleift að framkvæma undirbúningsathuganir á stöðluðum vörum skal fylgja eftirfarandi skrefum.

- Virkið umsjón hönnunarbreytinga í kerfinu eins og lýst er í [Yfirlit yfir umsjón hönnunarbreytinga](product-engineering-overview.md).
- Notið [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að kveikja á eiginleikanum sem heitir *Undirbúningsathuganir afurðar*.

<!-- KFM: This section requires confirmation before publishing

### How readiness checks are created for standard products

When you create a new non-engineering *released product*, the system determines whether a readiness check policy has been set up for the related shared product. If a policy has been set up, the following events occur:

- Readiness checks are created for the released product, according to the applicable policy.
- The released product is blocked from being used until all checks are marked as completed.

If a new *variant* is created for a product, the system checks whether readiness checks have been set up on the related shared product. If a readiness check has been set up, the following events occur:

- Readiness checks are created for the released product, according to the applicable policy.
- The released product is blocked from being used until all checks are marked as completed.

For engineering products, readiness checks are created in the same way that they are created when the *Product readiness checks* feature is turned off. For more information, see the [How readiness checks are created for a new engineering product, variant, or version](#checks-engineering) section earlier in this topic.

-->

### <a name="create-readiness-policies-for-standard-products"></a>Búa til undirbúningsreglur fyrir staðlaðar vörur

Hægt er að útbúa undirbúningsreglur fyrir staðlaðar afurðir rétt eins og gert er fyrir hönnunarafurðir. Sjá upplýsingarnar fyrr í þessari efnisatriði.

### <a name="assign-readiness-policies-to-standard-products"></a>Úthluta undirbúningsreglum fyrir staðlaðar afurðir

Til að úthluta undirbúningsreglu á staðlaða afurð skal opna tengda sameiginlega afurð og stilla reitinn **Undirbúningsregla afurðar** á heiti reglunnar sem á að gilda. Frekari upplýsingar er að finna í hlutanum [Úthluta undirbúningsreglum á staðlaðar afurðir og hönnunarafurðir](#assign-policy) fyrr í þessu efnisatriði.

### <a name="view-and-process-readiness-checks-on-standard-products"></a>Skoða og vinna með undirbúningsathuganir á stöðluðum vörum

Þegar kveikt er á þessum eiginleika eru undirbúningsathugunir skoðaðar og unnið úr þeim fyrir staðlaðar afurðir rétt eins og gert er fyrir hönnunarafurð. Sjá upplýsingarnar fyrr í þessari efnisatriði.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
