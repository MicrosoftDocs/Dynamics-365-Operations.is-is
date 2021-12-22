---
title: Skilgreina hjáleiðir fyrir skref í valmyndaratriðum fartækis
description: Þetta efnisatriði lýsir því hvernig á að skilgreina hjáleiðir fyrir valmyndaratriði þannig að starfsmenni geta sett núverandi verk í bið, sinnt öðru verki og farið svo aftur í upprunalegt verk án þess að glata upplýsingum.
author: Mirzaab
ms.date: 10/15/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-10-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 536fe2fa8819129f14e31ff966ab2349f836f0f7
ms.sourcegitcommit: fd6270dc7f49f93a8155d2b827153b13edb7be8a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/09/2021
ms.locfileid: "7902122"
---
# <a name="configure-detours-for-steps-in-mobile-device-menu-items"></a>Skilgreina hjáleiðir fyrir skref í valmyndaratriðum fartækis

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!--KFM: Preview until GA with 10.0.23 -->

> [!IMPORTANT]
> Eiginleikarnir sem lýst er í þessu efnisatriði eiga aðeins við um nýja farsímaforrit Warehouse Management. Þeir hafa ekki áhrif á gamla vöruhúsaforrið, sem nú er úrelt.

Þetta efnisatriði lýsir því hvernig á að skilgreina hjáleiðir fyrir valmyndaratriði þannig að starfsmenni geta sett núverandi verk „í bið“, sinnt öðru verki og farið svo aftur í upprunalegt verk án þess að glata upplýsingum.

Hjáleið er aðskilið valmyndaratriði sem hægt er að opna í skrefi í aðalverki. Undir lok hjáleiðar er starfsmaður sendur aftur á staðinn þar sem hann fór úr aðalverkinu. Í grunnstillingunni tilgreinir þú valmyndaratriðið sem á að vera hjáleið. Einnig velur þú hvaða reitargildi á að framsenda (afrita) sjálfkrafa úr aðalverkinu í hjáleiðina og færa inn þar. Þar af leiðandi verður þú að skilja hvar í verkflæðinu þú vilt að hjáleiðin sé tiltæk starfsmönnum. Þú verður einnig að tryggja að upplýsingarnar sem á að afrita í hjáleiðina séu tiltækar fyrir það skref verkflæðisins.

## <a name="enable-detours-in-your-system"></a>Virkja hjáleiðir í kerfinu

Áður en hægt er að skilgreina hjáleiðir fyrir skref í valmyndaratriðum fartækis þarf að ljúka eftirfarandi ferli til að virkja nauðsynlega eiginleika og búa til heiti áskildra reita í fartækjaforriti Warehouse Management.

1. Opna skal **Kerfisstjórnun \> Vinnusvæði \> Eiginleikastjórnun**.
1. Á vinnusvæðinu [**Eiginleikastjórnun** ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)skal virkja eiginleikann sem er sýndur á eftirfarandi hátt:

    - **Eining:** *Vöruhúsakerfi*
    - **Heiti eiginleika:** *Leiðbeiningar fyrir skref vöruhúsaforrits*

    Frekar upplýsingar um eiginleikann *Leiðbeiningar fyrir skref vöruhúsaforrits* er að finna í [Sérsníða þrepatitla og leiðbeiningar fyrir farsímaforrit Warehouse Management ](mobile-app-titles-instructions.md). Þessi eiginleiki er skilyrði fyrir eiginleikann *Hjáleiðir forrits vöruhúsakerfis*.

1. Virkjaðu eiginleikann sem er sýndur á eftirfarandi hátt:

    - **Eining:** *Vöruhúsakerfi*
    - **Heiti eiginleika:** *Hjáleiðir forrits vöruhúsakerfis*

    Þessi eiginleiki er eiginleikinn sem lýst er í þessu efnisatriði.

1. Uppfærðu heiti reita í farsímaforriti Warehouse Management með því að fara í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Reitarheiti vöruhúsaforrits** og veldu **Búa til sjálfgefna uppsetningu**. Frekari upplýsingar eru í [Skilgreina reiti fyrir farsímaforrit vöruhúsakerfis](configure-app-field-names-priorities-warehouse.md).
1. Endurtaktu fyrra skrefið fyrir hvern lögaðila (fyrirtæki) þar sem þú notar farsímaforrit Warehouse Management.

## <a name="configure-a-detour-from-a-menu-specific-override"></a>Skilgreina hjáleið úr hnekkingu valmyndar

Notaðu eftirfarandi ferli til að setja upp hjáleið úr hnekkingu valmyndar.

1. Búðu til hnekkingu valmyndar fyrir tiltekna valmynd og skref eins og lýst er í [Sérsníða þrepatitla og leiðbeiningar fyrir farsímaforrit Warehouse Management](mobile-app-titles-instructions.md).
1. Finndu samsetningu gilda fyrir **Kenni skrefs** og **Heiti valmyndaratriðis** sem þú vilt breyta og veldu síðan gildið í dálknum **Kenni skrefs**.
1. Á síðunni sem birtist, á flýtiflipanum **Hjáleiðir í boði (valmyndaratriði)**, er hægt að tilgreina valmyndaratriðið sem á að vera hjáleið. Einnig er hægt að velja hvaða reitargildi úr aðalverkinu eigi að vera sjálfkrafa afrituð í og úr hjáleiðinni. Dæmi sem sýna hvernig á að nota þessar stillingar er að finna í aðstæðum síðar í þessu efnisatriði.

## <a name="sample-scenario-1-sales-picking-where-a-location-inquiry-acts-as-a-detour"></a>Sýnidæmi 1: Tiltekt sölu þar sem fyrirspurn staðsetningar virkar sem hjáleið

Þessar aðstæður sýna hvernig á að skilgreina fyrirspurn staðsetningar sem hjáleið í verkflæði sölutiltektar sem starfsmaður stýrir. Þessi hjáleið gerir starfsmönnum kleift að fletta upp á öllum númeraplötum í staðsetningunni sem þeir eru að tína úr og velja númeraplötuna sem ætlunin er að nota til að ljúka tiltektinni. Svona hjáleið getur reynst gagnleg ef strikamerkið er ónýtt og þar af leiðandi ekki hægt að lesa það með skannanum. Að öðrum kosti gæti reynst gagnlegt ef starfsmaður verður að kynna sér hvað er í raun á lager í kerfinu. Athugaðu að þessar aðstæður virka aðeins ef tínt er úr númeraplötustýrðum staðsetningum.

### <a name="enable-sample-data"></a>Virkja gögn sýnishorna

Til að nota tiltekin dæmi um færslur og gildi til að fara í gegnum þessar aðstæður þarftu að nota kerfi þar sem stöðluð sýnigögn eru uppsett. Þú verður einnig að velja lögaðilann **USMF** áður en þú byrjar.

### <a name="create-a-menu-specific-override-and-configure-the-detour-for-scenario-1"></a>Búa til hnekkingu valmyndar og skilgreina hjáleið fyrir aðstæður 1

Í þessu ferli verður skilgreind hjáleið fyrir valmyndaratriðið **Tiltekt sölu** í skrefi númeraplötu.

1. Farðu í **Warehouse Management \> Uppsetning \> Fartæki \> Skref fartækis**.
1. Finndu skrefakennið sem heitir *LicensePlateId* og veldu það.
1. Á aðgerðasvæðinu skal velja **Bæta við skilgreiningu skrefs**.
1. Í felliglugganum skaltu nota reitinn **Valmyndaratriði** til að finna og velja *Tiltekt sölu*.
1. Veldu **Í lagi**.
1. Upplýsingasíðan fyrir hnekkinguna sem var búin til birtist. Á flýtiflipanum **Hjáleiðir í boði (valmyndaratriði)** skal velja **Bæta við** á tækjastikunni.
1. Í svarglugganum **Bæta við hjáleið** skal velja **Staðsetningarfyrirspurn** sem hjáleiðina sem verður gerð tiltæk í farsímaforriti Warehouse Management.
1. Veldu **Í lagi**.
1. Á flýtiflipanum **Hjáleiðir í boði (valmyndaratriði)** skal velja hjáleiðina sem var bætt við og velja síðan **Velja reiti til að senda** á tækjastikunni.
1. Í svarglugganum **Velja reiti til að senda** skal tilgreina upplýsingar sem senda til og frá hjáleiðinni. Í þessum aðstæðum gerir þú starfsmönnum kleift að nota staðsetningu sem þeir eiga að tína úr sem inntak fyrir hjáleið staðsetningarfyrirspurnar. Í hlutanum **Senda úr sölutiltekt** skal því velja **Bæta við** á tækjastikunni til að bæta línu við hnitanetið. Stilltu síðan eftirfarandi gildi fyrir nýju línuna:

    - **Afrita úr sölutiltekt:** *Staðsetning*
    - **Líma í staðsetningarfyrirspurn:** *Staðsetning*

1. Þar sem hjáleiðin í þessum aðstæðum er skilgreind í skrefi númeraplötu reynist það gagnlegt ef starfsmenn geta fengið númeraplötuna úr fyrirspurninni aftur í aðalflæðið. Í hlutanum **Sækja aftur úr staðsetningarfyrirspurn** skal því velja **Bæta við** á tækjastikunni til að bæta línu við hnitanetið. Stilltu síðan eftirfarandi gildi fyrir nýju línuna:

    - **Afrita úr fyrirspurn staðsetningar:** *Númeraplata*
    - **Líma í sölutiltekt:** *Númeraplata*

1. Veldu **Í lagi**.

Hjáleiðin er nú skilgreind að fullu. Hnappur til að hefja hjáleiðina **Staðsetningarfyrirspurn** birtist nú í skrefi númeraplötu fyrir valmyndaratriðið **Tiltekt sölu**.

### <a name="complete-a-sales-pick-on-a-mobile-device-and-use-the-detour"></a>Ljúka tiltekt sölu á fartæki og nota hjáleiðina

Í þessu ferli er sölutiltekt lokið með farsímaforriti Warehouse Management. Þú notar hjáleiðina sem þú varst að skilgreina til að finna númeraplötuna sem þú notar til að ljúka við tiltektarskrefið.

1. Í Microsoft Dynamics 365 Supply Chain Management skal stofna sölupöntun sem þarf tiltektarskref til að tína úr staðsetningu sem er rakin með númeraplötu. Losaðu svo sölupöntunina í vöruhúsið. Skráið niður vinnuauðkennið sem er myndað.
1. Opnaðu farsímaforrit Warehouse Management og skráðu þig inn í vöruhús 24. (Í stöðluðum kynningargögnum skráirðu þig inn með því að nota *24* sem notandakenni og *1* sem lykilorð.)
1. Veldu valmyndina **Á útleið** og veldu svo valmyndaratriðið **Tiltekt sölu**.
1. Fylgdu leiðbeiningum um gagnaskráningu á skjánum til að færa inn vinnukennið sem var búið til í skrefi 1.
1. Í skrefinu sem inniheldur textann **Skanna númeraplötu** skal opna valmynd aðgerða. Þú ættir að sjá nýjan hnapp sem er merktur **Staðsetningarfyrirspurn**. Ör í efra vinstra horninu gefur til kynna að hnappurinn muni hefja hjáleið. Veldu **Staðsetningarfyrirspurn**.
1. Hjáleiðin er hafin. Á næstu síðu skaltu staðfesta staðsetninguna sem var afrituð úr aðalflæðinu.
1. Í listanum yfir tiltækar númeraplötur á staðsetningu skal pikka á númeraplötuna sem á að afrita aftur í aðalflæðið. Veldu svo hnappinn **Til baka**.
1. Þú ert komin(n) aftur í aðalflæði sölutiltektar og númeraplatan hefur verið afrituð aftur í það úr hjáleiðinni. Staðfestu gildið til að halda áfram í næsta skref.
1. Nú geturðu lokið því sem eftir er af staðlaða flæðinu með því að færa inn umbeðnar leiðbeiningar um gagnaskráningu.

Vöruhúsavinnu er nú lokið. Starfsmaðurinn opnaði hjáleið til að framkvæma aukaverk (staðsetningarfyrirspurn) án þess að staða hans í aðalverkinu tapaðist, og náði í upplýsingarnar sem þurfti til að ljúka aðalverkinu.

## <a name="sample-scenario-2-item-inquiry-with-movement-and-adjustment-detours"></a>Sýnidæmi 2: Vörufyrirspurn með hjáleið hreyfingar og leiðréttingar

Þessar aðstæður sýna hvernig á að skilgreina hreyfingu og leiðréttingar sem margar hjáleiðir í verkflæði staðsetningarfyrirspurnar. Þessi möguleiki getur komið að gagni í aðstæðum þar sem starfsmaður kemur á staðsetningu, kemst að því að birgðirnar í staðsetningunni eru aðrar en þær sem eru skráðar í kerfinu og verður því að leiðrétta eða færa til vörur.

Þú getur skipt út fyrirspurn um staðsetningu með númeraplötufyrirspurn eða vörufyrirspurn eftir þörfum.

### <a name="enable-sample-data"></a>Virkja gögn sýnishorna

Til að nota tiltekin dæmi um færslur og gildi til að fara í gegnum þessar aðstæður þarftu að nota kerfi þar sem stöðluð sýnigögn eru uppsett. Þú verður einnig að velja lögaðilann **USMF** áður en þú byrjar.

### <a name="create-a-menu-specific-override-and-configure-the-detour-for-scenario-2"></a>Búa til hnekkingu valmyndar og skilgreina hjáleið fyrir aðstæður 2

Í þessu ferli verður skilgreind hjáleið fyrir valmyndaratriðið **Tiltekt sölu** í skrefi númeraplötu.

1. Farðu í **Warehouse Management \> Uppsetning \> Fartæki \> Skref fartækis**.
1. Leitaðu að og veldu skrefakennið sem heitir *LocationInquiryList*.

    > [!NOTE]
    > Til að nota vörufyrirspurn í stað staðsetningarfyrirspurnar skal velja línu þar sem skrefakennið heitir *ItemInquiryList*. Til að nota fyrirspurn númeraplötu skal velja l´nu þar sem skrefakennið heitir *LPInquiryList*.

1. Á aðgerðasvæðinu skal velja **Bæta við skilgreiningu skrefs**.
1. Í felliglugganum skaltu nota reitinn **Valmyndaratriði** til að finna og velja *Staðsetningarfyrirspurn*.
1. Veldu **Í lagi**.
1. Upplýsingasíðan fyrir hnekkinguna sem var búin til birtist. Á flýtiflipanum **Hjáleiðir í boði (valmyndaratriði)** skal velja **Bæta við** á tækjastikunni.
1. Í svarglugganum **Bæta við hjáleið** skal velja **Hreyfing** sem hjáleiðina sem verður gerð tiltæk í farsímaforriti Warehouse Management.
1. Veldu **Í lagi**.
1. Á flýtiflipanum **Hjáleiðir í boði (valmyndaratriði)** skal velja hjáleiðina sem var bætt við og velja síðan **Velja reiti til að senda** á tækjastikunni.
1. Í glugganum **Velja reiti til að senda** skal tilgreina upplýsingar sem senda til og frá hjáleiðinni. Í þessum aðstæðum býstu við því að starfsmenn leiti að númeraplötustýrum staðsetningum. Það reynist því gagnlegt að afrita númeraplötuna úr fyrirspurninni í hjáleiðina **Hreyfing**. Í hlutanum **Senda úr sölutiltekt** skal velja **Bæta við** á tækjastikunni til að bæta línu við hnitanetið. Stilltu síðan eftirfarandi gildi fyrir nýju línuna:

    - **Afrita úr staðsetningarfyrirspurn:** *Staðsetning*
    - **Líma í hreyfingu:** *Staðs / NP*

    Í þessari hjáleið býstu ekki við að neinar upplýsingar séu afritaðar til baka vegna þess að aðalflæðið var fyrirspurn þar sem ekki er þörf á neinum viðbótarskrefum.

1. Veldu **Í lagi**.

Hjáleiðin er nú skilgreind að fullu. Hnappur til að hefja hjáleiðina **Hjáleið** birtist nú í skrefi númeraplötu fyrir valmyndaratriðið **Staðsetningarfyrirspurn**.

### <a name="do-a-location-inquiry-on-a-mobile-device-and-use-the-detour"></a>Spyrjast fyrir um staðsetningu í fartæki og nota hjáleiðina

Í þessu ferli er fyrirspurn um staðsetningu send með farsímaforriti Warehouse Management. Þú notar síðan hjáleiðina til að ljúka vöruhreyfingu.

1. Opnaðu farsímaforrit Warehouse Management og skráðu þig inn í vöruhús 24. (Í stöðluðum kynningargögnum skráirðu þig inn með því að nota *24* sem notandakenni og *1* sem lykilorð.)
1. Veldu valmyndina **Birgðir** og veldu svo valmyndaratriðið **Staðsetningarfyrirspurn**.
1. Sláðu inn staðsetningu til að spyrjast fyrir um, svo sem *FL-001*.
1. Þegar listinn birtist skaltu pikka á og halda einu spjaldinu úr honum til að sýna tiltækar hjáleiðir.
1. Veldu **Hreyfing**.
1. Taktu eftir að númeraplatan hefur verið afrituð úr spjaldinu sem þú valdir. Staðfestu gildið.
1. Nú er hægt að fylgja staðlaða verkflæðinu til að ljúka við hreyfinguna. Þegar vinnu er lokið skal opna valmynd aðgerða og velja **Hætta við**.
1. Þú ert komin(n) aftur á síðuna **Staðsetningarfyrirspurn**. Athugaðu að gildin eru ekki uppfærð sjálfkrafa. Þar af leiðandi þarf að endurhlaða síðuna handvirkt til að sjá breytingarnar úr hjáleið hreyfingar.
