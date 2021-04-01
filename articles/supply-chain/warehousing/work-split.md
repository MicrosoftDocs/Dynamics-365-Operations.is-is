---
title: Skipta vinnu
description: Þetta efnisatriði veitir upplýsingar um virkni vinnuskiptingar. Þessi virkni gerir þér kleift að skipta stórum verkbeiðnum niður í nokkrar smærri verkbeiðnir sem síðan er hægt að úthluta á marga vöruhúsastarfskrafta. Á þennan hátt er hægt að velja sömu vinnu samtímis af nokkrum starfskröftum í vöruhúsi.
author: mirzaab
manager: tfehr
ms.date: 10/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: WHSWorkTableListPage
ms.author: mirzaab
ms.search.validFrom: 2020-10-15
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 6dbf0f6dd0c691db74eaad2174d8f9849b4cb26a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5245083"
---
# <a name="work-split"></a>Skipta vinnu

Virkni vinnuskiptingar gerir þér kleift að skipta stórum vinnukennum (þ.e. verkbeiðnum sem eru með margar línur) niður í nokkur smærri vinnukenni sem síðan er hægt að úthluta á marga vöruhúsastarfskrafta. Á þennan hátt er hægt að velja sama stofnnúmer vinnu samtímis af nokkrum starfskröftum í vöruhúsi.

> [!IMPORTANT]
> Aðeins er hægt að skipta verkbeiðnum sem eru með stöðuna *Opin* eða *Í gangi*.

## <a name="turn-on-the-work-split-functionality"></a>Kveikja á virkni vinnuskiptingar

Áður en hægt er að nota virkni vinnuskiptingar þarf að kveikja á eiginleikanum og eiginleika forsendanna í kerfinu. Stjórnendur geta notað stillingar [eiginleikastjórnunar](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikanna og kveikja á þeim ef þörf krefur.

Fyrst skal kveikja á forsendueiginleikanum *Vinnulokun fyrir allt fyrirtækið* ef ekki er nú þegar kveikt á honum. Í vinnusvæðinu **Stjórnun eiginleika** er þessi eiginleiki skráður á eftirfarandi hátt:

- **Eining:** *Vöruhúsakerfi*
- **Heiti eiginleika:** *Vinnulokun fyrir allt fyrirtækið*

> [!NOTE]
> Þegar þessi eiginleiki er virkjaður er gagnauppfærsla sjálfkrafa notuð þegar búið er að kveikja á eiginleikann yfir alla lögaðila.

Næst er kveikt á eiginleikanum *Skipta verki* sem er sýndur á eftirfarandi hátt:

- **Eining:** *Vöruhúsakerfi*
- **Heiti eiginleika:** *Skipta verki*

## <a name="enhancements-to-the-work-details-and-all-work-pages"></a>Viðbætur á síðum verkupplýsinga og öllum verkum

Eiginleikinn *Skipta verki* bætir eftirfarandi tveimur hnöppum við flipann **Verk** á aðgerðasvæðinu á síðunum **Upplýsingar um verk** og **Öll verk**:

- **Skipta verki** – Skipta núverandi vinnukenni niður í mörg smærri vinnukenni sem mismunandi starfskraftar geta unnið úr.
- **Hætta við lotu verkskiptingar** - Hættir við lotu verkskiptingar og gerir verk tiltækt fyrir úrvinnslu.

![Hnappar fyrir Skipta verki og Hætta við lotu verkskiptingar](media/Work_split_buttons.png "Hnappar fyrir Skipta verki og Hætta við lotu verkskiptingar")

> [!IMPORTANT]
> Hnappurinn **Skipta verki** verður ekki í boði ef einhver eftirfarandi skilyrða eru uppfyllt:
>
> - Verkstaðan er eitthvað annað en *Opin* eða *Í gangi*.
> - Gámagerðarauðkenni tengist vinnukenninu. (Ekki er hægt að skipta hólfi kerfisbundið vegna þess að það krefst líkamlegrar aðgerðar.)
> - Vinnan tengist klasa.
> - Gerð verkbeiðni er einhver önnur en ein af eftirfarandi gerðum:
>
>    - Sölupantanir
>    - Tiltekt hráefnis
>    - Flutningsútgáfa
>
> - Annar notandi er að skipta vinnunni. Ef reynt er að opna síðu skiptingar fyrir verk sem þegar verið að skipta af hálfu annars notanda, færðu eftirfarandi villuboð: „Verið er að skipta niður vinnu með auðkennið \#\#\#\#. Reyna skal aftur eftir smástund. Ef þessi skilaboð halda áfram að birtast skal hafa samband við yfirmann.

Ný ástæða verklokunar, *Skipta verki*, gefur til kynna þegar verið er að skipta niður verkkenninu. Hún er sýnd bæði á síðunni **Skipta verki** og í vöruhúsaforritinu ef notandi reynir að keyra vinnu. Þegar lokunarástæður eru notaðar verður heiti reitsins **Lokuð bylgja** fyrir verkkennið breytt í **Lokað fyrir**.

## <a name="initiate-a-work-split"></a>Hefja vinnuskipti

Þessi eiginleiki bætir við nýrri **Skipta vinnu** síðu sem gerir notendum kleift að skipta vinnulínum úr vinnukenninu. Þegar síðan er fyrst opnuð sýnir hún línur sem eru með verkstöðuna *Opin* og eru tiltækar til skiptingar. Í aðgerðasvæði skal velja **Skipta vinnu** til að skipta valinni vinnu.

Til að skipta vinnu skal fylgja þessum skrefum.

1. Opnið eina af eftirfarandi vinnusíðum:

    - **Upplýsingar um verk** (**Vöruhúsakerfi \> Verk \> Upplýsingar um verk**)
    - **Öll verk** (**Vöruhúsakerfi \> Verk \> Öll verk**)

1. Í hnitanetinu skal velja vinnukennið sem á að skipta. Stilla verður reitinn **Gerð verkbeiðni** á eitt af eftirfarandi gildum:

    - Sölupantanir
    - Tiltekt hráefnis
    - Flutningsútgáfa

1. Á aðgerðasvæðinu, í flipanum **Verk**, í flokknum **Verk**, skal velja **Skipta verki**.

    Síðan **Skipta verki** opnast og sýnir vinnulínurnar sem eru opnar og má skipta. Aðeins lausar vinnulínur eru sýndar sjálfkrafa. Til að skoða allar línur fyrir verkkennið (t.d. línur sem eru af verkgerðinni *Frágangur*) skal velja gátreitinn **Sýna allar línur** fyrir ofan hnitanetið.

    Eftirfarandi skilaboð birtast: „Notendur geta ekki unnið úr línum fyrir vinnu fyrr en lokið er við skiptingu og þessari síðu er lokað.“

    Reiturinn **Ástæða fyrir vinnulokun** fyrir núverandi vinnu verður stilltur á *Skipta vinnu* og lokað verður fyrir vinnuna.

    ![Ástæða lokunar](media/Blocking_reason.png "Ástæða lokunar")

1. Veljið línurnar sem á að fjarlægja úr núverandi vinnukenni og bætið við nýtt vinnunkenni. Eftirfarandi tilvik gerast:

    - Þegar vinnu er skipt er hætt við valda línu eða línur úr upprunalegu vinnukenninu og síðan afritaðar í nýtt vinnukenni.
    - Fyrirliggjandi skipulag vinnusniðmáts og staðsetningin á fráganginum (og líka tiltektar/frágangsparanir í framtíðinni) er geymt. Gildi fyrir eftirfarandi reiti vinnukennis eru afritaðir úr upprunalegri vinnu og yfir í nýju vinnuna:

        - Hleðsluauðkenni
        - Auðkenni sendingar
        - Gerð verkbeiðni
        - Pöntunarnúmer
        - Vefsvæði
        - Vöruhús
        - Forgangur vinnu
        - Auðkenni vinnuhóps
        - Bylgjuauðkenni
        - Stofnnúmer vinnu

    - Eftirfarandi reitir eru ekki afritaðir í nýja verkkennið:

        - **Verkkenni** – Nýtt verkkenni er búið til úr tilheyrandi númeraröð.
        - **Verkstaða** – Þessi reitur er stilltur á *Opin*.
        - **Læst af** – Þessi reitur er upphaflega skilinn eftir auður.
        - **Auðkenni númeraplötu markmiðs** - Þessi reitur er skilinn eftir auður.
        - **Stofnuð dagsetning og tími** - Þessi reitur er stilltur á núverandi dagsetningu og tíma.
        - **Lokuð bylgja/frosin** - Þessi reitur er endurreiknaður fyrir upprunalega vinnukennið og nýja vinnukennið.

1. Á aðgerðasvæðinu skal velja **Skipta vinnu**.

Meðan verið er að skipta vinnu birtast eftirfarandi skilaboð: „Aðgerð í vinnslu - Skipta vinnu“. Á meðan þessi skilaboð eru sýnileg er hægt að hætta við aðgerðina með því að velja **Hætta við** í skilaboðaglugganum.

Ef gátreiturinn **Sýna allar línur** er hreinsaður mun línan sem var skipt út og hætt við ekki sjást lengur í hnitanetinu. Ef gátreiturinn er valinn er hægt að sjá að gildið á reitnum **Verkstaða** fyrir þá línu hefur breyst í *Hætt við*.

Eftirfarandi tilkynning er sýnd til að gefa til kynna að nýja verkkennið hafi verið búið til: „Vinnan \#\#\#\# var stofnuð sem hluti af skiptingu á upprunalegu vinnunni \#\#\#\#.“

Aðrar vinnulínur úr upprunalega verkkenninu (t.d. línur *Frágangs*) verða aðlagaðar eins og þörf er á til að endurspegla línurnar í vinnunni sem hætt var við. Til dæmis, ef hætt var við upprunalega verkkennið sem var með *Frágangslínu* með magn upp á 15 og *Tiltektarlínu* sem var með heildarmagnið 10, verður nýja magn *Frágangs* í upprunalega verkkenninu núna 5.

Nýja verkinu verður ekki úthlutað á neinn notanda strax. Hins vegar er hægt að úthluta því á notanda eftir þörfum með því að nota stöðluðu virknina á síðunni **Upplýsingar um verk**.

> [!IMPORTANT]
> Aðeins er hægt að skipta vinnukennum sem innihalda tvær eða fleiri lausar vinnulínur. Ef **Skipta vinnu** er valið þegar aðeins ein vinnulína er til staðar, færðu eftirfarandi villuboð: „Að minnsta kosti ein vinnulína verður að vera eftir í upprunalegu verki. Í þessu tilvikum kemur engin skipting fram.

## <a name="finish-a-work-split"></a>Ljúka vinnuskiptum

Til að ljúka skiptingu vinnu þarf að fjarlægja lokunarástæðuna *Skipta vinnu*. Hægt er að ljúka þessu skrefi á tvennan hátt:

- Notandinn sem er að skipta vinnunni lokar síðunni **Skipta vinnu** með því að velja hnappinn **Loka** (**X**) uppi í hægra horninu. Þegar síðunni er lokað verður lokunarástæðan *Skipta vinnu* fjarlægð. Staðan *Lokað fyrir* fyrir þessa vinnu verður endurreiknuð og ef engar eftirstandandi lokunarástæður eru til staðar fyrir þessa vinnu, verður opnað fyrir vinnuna aftur.
- Hvaða notandi sem er opnar verkkennið og velur hnappinn **Hætta við lotu vinnuskiptingar** á aðgerðasvæðinu. Lokunarástæðan *Skipta vinnu* verður fjarlægð og staðan *Lokað fyrir* fyrir þessa vinnu verður endurreiknuð rétt eins og þegar síðan **Skipta vinnu** er lokuð.

Þegar lokunarástæðan *Skipta vinnu* hefur verið fjarlægð, verður hægt að keyra vinnuna í fartæki svo lengi sem staðan **Lokað fyrir** er stillt á *Nei* í verkkenninu.

## <a name="user-blocking-on-the-warehouse-app"></a>Lokun notanda á vöruhúsaforriti

Ef reynt er að nota vöruhúsaforritið til að keyra tiltekt fyrir verkkenni sem verið er að skipta, birtast eftirfarandi villuboð: „Verið er að skipta niður vinnu með auðkennið \#\#\#\#.“ Ef þessi skilaboð birtast skal velja **Hætta við**. Síðan er hægt að halda áfram með aðra vinnu.

## <a name="other-blocked-operations"></a>Aðrar lokaðar aðgerðir

Allar aðgerðir sem breyta vinnulínum, birgðafærslum eða áfyllingartenglum sem tengjast vinnu sem verið er að skipta munu mistakast og eftirfarandi villuboð birtast: „Verið er að skipta niður vinnu með auðkennið \#\#\#\#.“


[!INCLUDE[footer-include](../../includes/footer-banner.md)]