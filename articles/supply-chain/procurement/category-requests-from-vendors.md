---
title: Tegundabeiðnir frá lánardrottnum
description: Í þessu efnisatriði er lýst hvernig lánardrottnar geta óskað eftir innkaupaflokkum fyrir reikningana þeirra. Þar er einnig lýst samþykktarferlinu sem innkaupafulltrúar ljúka.
author: Henrikan
ms.date: 04/19/2021
ms.topic: article
ms.search.form: VendRequestNewCategory
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 560b62183f9c0c45c872998373a90dc9dc0ebbb3
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571714"
---
# <a name="category-requests-from-vendors"></a>Tegundabeiðnir frá lánardrottnum

[!include [banner](../includes/banner.md)]

Ferli tegundabeiðni gerir lánardrottnum kleift að óska eftir því að nýir innkaupaflokkar verði tengdir við reikningana þeirra. Tengd innkaupa- og aðfangaferli geta þá notað þessa innkaupaflokka. (Frekari upplýsingar er að finna í [Yfirlit innkaupavörulista](procurement-catalogs.md).)

Lánardrottnar setja af stað beiðnir um flokka á vinnusvæðinu **Lánardrottnaupplýsingar**. Þær eru síðan sendar til yfirferðar og samþykkis hjá stofnuninni. Samþykktum flokkum er bætt við listann yfir innkaupaflokka fyrir reikning lánardrottins.

## <a name="turn-on-the-feature-in-your-system"></a>Kveikja á eiginleikanum í kerfinu

Ef kerfið inniheldur ekki eiginleikann sem lýst er í þessu efnisatriði skal fara í [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og kveikja á eiginleikanum *Leyfa lánardrottnum að sækja um innkaupaflokka með samstarfi lánardrottna*.

Eftir að kveikt er á eiginleikanum er enn hægt að bæta innkaupaflokkum handvirkt við reikninga lánardrottins. Frekari upplýsingar er að finna í [Samþykkja lánardrottnar fyrir tiltekna innkaupaflokka](tasks/approve-vendors-specific-procurement-categories.md).

## <a name="vendor-collaboration-requirements"></a>Kröfur lánardrottnasamstarfs

Áður en lánardrottin getur unnið með tegundabeiðnir þarf að setja þær upp fyrir samstarf lánardrottna.

Lánardrottinn verður að hafa að minnsta kosti einn notanda lánardrottnasamstarfs. Aðeins notendur söluaðila með *Kerfisstjóri lánardrottins (ytriytri)* geta búið til og sent inn beiðnir um flokka.

Frekari upplýsingar, sjá [Setja upp og vinna með samstarf lánardrottna](set-up-maintain-vendor-collaboration.md).

## <a name="set-up-the-vendor-category-request-workflow"></a>Setja upp verkflæði fyrir tegundarbeiðni lánardrottins

Vinnuflæðið *Tegundarbeiðni lánardrottins* verður að vera sett upp í verkflæði innkaupa og aðfanga. Lánardrottnar munu senda inn nýjar tegundabeiðnir sem hægt er að yfirfara og samþykkja. Umbeðnum innkaupaflokkum er bætt við reikning lánardrottins þegar búið er að samþykkja tegundabeiðni.

Eftirfarandi dæmi sýnir hvernig á að setja upp einfalt verkflæði fyrir *Tegundarbeiðni lánardrottins* sem er með einn samþykktaraðila. Þú verður að fara yfir innri ferla þína til að ákvarða viðeigandi uppsetningu á verkflæði fyrir stofnunina þína.

1. Opnið **Innkaup og aðföng \> Uppsetning \> Verkflæði innkaupa og aðfanga**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Í svarglugganum skal velja **Verkflæði fyrir tegundarbeiðni lánardrottins** til að opna verkflæðisritilinn.
1. Skráðu þig inn í verkflæðisritilinn.
1. Á aðgerðasvæðinu skal velja **Eiginleikar**.
1. Á síðunni **Eiginleikar** fyrir verkflæðið, í reitnum **Innsendingarleiðbeiningar**, skal færa inn leiðbeiningartexta. Leiðbeiningarnar verða sýnilegar lánardrottnum þegar þeir senda inn tegundabeiðni.
1. Lokaðu síðunni **Eiginleikar**.
1. Dragðu verkflæðiseininguna **Samþykkja nýja tegundabeiðni** inn á vinnusvæðið.
1. Dragðu tengil úr verkflæðiseiningunni **Byrja** í verkflæðiseininguna **Samþykkja nýja tegundabeiðni**.
1. Dragðu tengil úr verkflæðiseiningunni **Samþykkja nýja tegundabeiðni** í verkflæðiseininguna **Ljúka**.
1. Tvípikkaðu (eða tvísmelltu) á verkflæðið **Samþykkja nýja tegundabeiðni**.
1. Veldu og haltu (eða hægrismelltu) á verkflæðiseininguna **Skref 1** og veldu síðan **Eiginleikar**.
1. Á síðuna **Eiginleikar** fyrir verkflæðiseininguna, í reitinn **Efni vinnuliðar**, skal færa inn texta efnis. Þessi texti verður sýndur sem gildið í reitnum **Efni** á síðunni **Vinnuliðir sem úthlutað er á mig**.
1. Í reitinn **Leiðbeiningar vinnuliðar** skal færa inn leiðbeiningartexta. Leiðbeiningarnar verða sýnilegar samþykktaraðilum þegar þeir velja **Verkflæði** á aðgerðasvæði tegundabeiðni.
1. Á svæðinu vinstra megin skal velja **Úthlutun**.
1. Í flipanum **Úthlutunargerð** skal stilla **Úthluta notanda á þessa verkflæðiseiningu** á *Notandi*.
1. Í flipanum **Notandi**, á listanum **Tiltækir notendur**, skal velja samþykktaraðila. Til dæmis skal velja notanda í innkaupadeildinni.
1. Veljið hægri örvarhnappinn (**\>**) til að færa samþykktaraðilann yfir í listann **Valdir notendur**.
1. Lokaðu síðunni **Eiginleikar**.
1. Veljið **Vista og loka**.
1. Í reitinn **Athugasemdir útgáfu** skal færa inn athugasemdir um verkflæðið.
1. Veljið **Í lagi** til að vista verkflæðið.
1. Ef þú ert tilbúin(n) til að hefjast handa og prófa verkflæðið skaltu velja **Virkja nýju útgáfuna**. Annars skaltu velja **Ekki virkja nýja útgáfuna**.
1. Veljið **Í lagi** til að ljúka uppsetningu verkflæðis.

> [!TIP]
> Ef stofnunin þín krefst ekki samþykkis á tegundabeiðnum ættirðu að skilgreina verkflæðið fyrir sjálfvirka samþykkt.

Frekari upplýsingar um hvernig á að setja upp verkflæði er að finna í [Yfirlit yfir verkflæðiskerfi](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md).

## <a name="create-and-submit-a-category-request"></a>Stofna og senda tegundabeiðni

Þessi hluti lýsir því hvernig lánardrottnar geta notað vinnusvæðið **Lánardrottnaupplýsingar** til að stofna, breyta, skoða og senda inn tegundabeiðnir.

### <a name="start-a-new-request"></a>Byrja á nýrri beiðni

Fylgið eftirfarandi skrefum til að hefja nýja tegundabeiðni.

1. Á vinnusvæðinu **Lánardrottnaupplýsingar** skal velja reitinn **Tegundabeiðnir**.
1. Á síðunni **Tegundabeiðnir**, á aðgerðasvæðinu, skal velja **Ný tegundabeiðni**.
1. Í svarglugganum **Ný tegundabeiðni** skal finna flokkinn sem á að sækja um með því að fletta í trénu og/eða nota síuna efst í listanum. Veldu gátreitinn fyrir hvern viðeigandi flokk.

    Athugið eftirfarandi stig:

    - Flokkar sem eru virkir í reikningi lánardrottins eru sýndir sem valdir og er ekki hægt að fjarlægja.
    - Hægt er að óska eftir mörgum innkaupaflokkum í einni tegundabeiðni.

1. Velja skal **Í lagi** til að stofna drög að beiðni.

    Ný drög að beiðninni birtast nú á síðunni **Tegundabeiðnir**.

1. Opnaðu nýju drögin að beiðninni til að skoða og breyta þeim eftir þörfum.

    - Til að skoða lista yfir flokka sem eru nú þegar í beiðninni skal velja flýtiflipann **Umbeðnir flokkar**.
    - Til að skoða virka flokka skal opna upplýsingareitinn **Virkir flokkar** hægra megin á síðunni.
    - Til að bæta flokki við beiðnina skal velja **Bæta við** á tækjastikunni í flýtiflipanum **Umbeðnir flokkar**.
    - Til að fjarlægja flokk úr beiðninni skal velja flokkinn í flýtiflipanum **Umbeðnir flokkar** og síðan velja **Fjarlægja** á tækjastikunni.
    - Til að hengja skjal við beiðnina skal velja **Viðhengi** á aðgerðasvæðinu. Viðhengd skjöl verða aðgengileg samþykktaraðilum þegar þeir yfirfara tegundabeiðnina.
    - Til að fjarlægja viðhengt skjal úr beiðninni skal velja **Viðhengi** á aðgerðasvæðinu. Veljið skjalið til að fjarlægja og veljið svo **Eyða** á aðgerðasvæðinu.

1. Ef þú ert tilbúin(n) til að senda inn beiðnina skaltu velja **Senda inn** á aðgerðasvæðinu. Annars skaltu loka síðunni og sleppa skrefunum sem eftir eru í þessu ferli. Hægt að fara aftur í beiðnina síðar.
1. Lesið allar leiðbeiningar um innsendingu sem birtast og veljið síðan **Senda inn**.
1. Í reitinn **Athugasemd** skal færa inn nauðsynlegar viðbótarupplýsingar. Veljið svo **Senda** til að ljúka beiðninni.

### <a name="edit-a-draft-or-recalled-request"></a>Breyta drögum eða afturkallaðri beiðni

Til að breyta drögum eða afturkallaðari tegundabeiðni skal fylgja þessum skrefum.

1. Á vinnusvæðinu **Lánardrottnaupplýsingar** skal velja reitinn **Tegundabeiðnir**.
1. Veljið drögin eða afturkallaða beiðni til að opna hana.
1. Breytið beiðninni eftir þörfum og lokið henni síðan eða sendið hana inn eins og lýst er í ferlinu hér á undan.

### <a name="submit-a-draft-or-recalled-request"></a>Senda drög eða afturkalla beiðni

Fylgja skal eftirfarandi skrefum til að senda drög eða endurkalla tegundabeiðni.

1. Á vinnusvæðinu **Lánardrottnaupplýsingar** skal velja reitinn **Tegundabeiðnir**.
1. Veljið drögin eða afturkallað beiðni sem á að senda inn.
1. Á aðgerðasvæðinu skal velja **Senda**.
1. Lesið allar leiðbeiningar um innsendingu sem birtast og veljið síðan **Senda inn**.
1. Í reitinn **Athugasemd** skal færa inn nauðsynlegar viðbótarupplýsingar. Veljið svo **Senda** til að ljúka beiðninni.

    Stöðu tegundabeiðninnar er breytt í eitt af eftirfarandi gildi:

    - _Bíður umsagnar_ – Beiðnin er í verkflæðinu.
    - _Bíður samþykkis_ – Samþykki er nauðsynlegt.

### <a name="recall-a-submitted-request-that-hasnt-yet-been-approved"></a>Afturkalla innsenda beiðni sem hefur ekki verið samþykkt

Fylgið eftirfarandi skrefum til að afturkalla tegundabeiðni sem hefur verið send inn en hefur ekki enn verið samþykkt.

1. Á vinnusvæðinu **Lánardrottnaupplýsingar** skal velja reitinn **Tegundabeiðnir**.
1. Veljið beiðnina í bið sem á að afturkalla.
1. Á aðgerðasvæðinu skal velja **Afturkalla**.
1. Í reitnum **Færa inn athugasemd** eru færðar inn allar viðbótarupplýsingar sem nauðsynlegar eru. Veljið svo **Senda** til að ljúka beiðninni.

    Stöðu beiðninnar er breytt í _Hætt við_. Beiðnin verður áfram í þessari stöðu þar til henni er eytt eða hún er send aftur.

### <a name="delete-a-draft-or-recalled-request"></a>Eyða drögum eða afturkallaðri beiðni

Fylgja skal eftirfarandi skrefum til að eyða drögum eða endurkalla tegundabeiðni.

1. Á vinnusvæðinu **Lánardrottnaupplýsingar** skal velja reitinn **Tegundabeiðnir**.
1. Veljið drögin eða afturkallaða beiðni sem á að eyða.
1. Á aðgerðasvæðinu skal velja **Eyða**.
1. Veljið **Já** til að staðfesta eyðinguna.

### <a name="view-completed-requests"></a>Skoða loknar beiðnir

Til að skoða loknar beiðnir skal opna vinnusvæðið **Lánardrottnaupplýsingar** og velja reitinn **Tegundabeiðnir**. Tegundabeiðnum sem er lokið fá eina af eftirfarandi stöðum:

- _Samþykkt_ – Beiðnin var samþykkt. Til að skoða nýlega viðbættum flokkum skal fara aftur á vinnusvæðið **Lánardrottnaupplýsingar**, opna fellilistann **Frekari upplýsingar** á svæðinu vinstra megin og síðan velja **Flokkar**.
- _Hafnað_ – Beiðninni var hafnað. Hægt er að stofna nýja tegundabeiðni eins og þörf krefur.

## <a name="review-category-requests"></a>Yfirfara tegundabeiðnir

Þessi hluti útskýrir hvernig á að samþykkja, hafna og úthluta tegundabeiðnum sem lánardrottnar senda inn og hvernig á að skoða loknar beiðnir. Þessar verkflæðisaðgerðir eru fyrir tegundabeiðnina í heild sinni.

### <a name="view-category-requests"></a>Skoða tegundabeiðnir

Til að skoða tegundabeiðnir skal fylgja eftirfarandi skrefum.

1. Farið í **Innkaup og aðföng \> Lánardrottnar \> Beiðnir lánardrottnasamstarfs \> Tegundabeiðnir**.

    Síðan **Tegundabeiðnir** birtist. Sjálfgefin síða sýnir tegundabeiðnir sem eru með stöðuna *Bíður aðgerðar*.

1. Til að skoða allar beiðnir skal velja *Allar* í reitnum **Sýna beiðnir**.
1. Opnaðu beiðni til að skoða hana og breyta eftir þörfum.

    - Til að skoða lista yfir flokka sem eru nú þegar í beiðninni skal velja flýtiflipann **Umbeðnir flokkar**.
    - Til að skoða virka flokka skal opna upplýsingareitinn **Virkir flokkar** hægra megin á síðunni.
    - Ef skjöl voru send inn sýnir hnappurinn **Viðhengi** (bréfaklemma) á aðgerðasvæðinu fjölda viðhengdra skjala. Veljið hnappinn **Viðhengi** til að skoða meðfylgjandi skjöl. Veljið síðan skjalið sem á að skoða og veljið **Opna** til að skoða það.
    - Til að hengja skjal við beiðnina skal velja **Viðhengi** á aðgerðasvæðinu. Viðhengd skjöl verða aðgengileg samþykktaraðilum þegar þeir yfirfara tegundabeiðnina.
    - Til að fjarlægja viðhengt skjal úr beiðninni skal velja **Viðhengi** á aðgerðasvæðinu. Veljið skjalið til að fjarlægja og veljið svo **Eyða** á aðgerðasvæðinu.
    - Til að skoða verkflæðissöguna skal velja **Verkflæði** á aðgerðasvæðinu. Í valkostum vinnuflæðis skal velja **Meira** og síðan **Verkflæðissaga**. Síðan **Verkflæðissaga** birtist.

### <a name="approve-a-pending-category-request"></a>Samþykkja tegundabeiðni sem bíður

Fylgið eftirfarandi skrefum til að samþykkja tegundabeiðni í biðstöðu.

1. Farið í **Innkaup og aðföng \> Lánardrottnar \> Beiðnir lánardrottnasamstarfs \> Tegundabeiðnir**.
1. Veljið beiðni í biðstöðu til að samþykkja.
1. Yfirfara nýja tegundabeiðni
1. Valfrjálst: Í flýtiflipanum **Almennt**, í reitnum **Ástæðukóði**, skal velja ástæðukóða. Síðan, í reitnum **Athugasemd ástæðu**, skal færa inn athugasemd um ástæðukóðann.
1. Í aðgerðasvæðinu skal velja **Verkflæði**.
1. Veljið **Samþykkja** í valkostum verkflæðis.
1. Í reitinn **Athugasemd** skal færa inn nauðsynlegar viðbótarupplýsingar. Veljið síðan **Samþykkja** til að ljúka beiðninni.

    Stöðu tegundabeiðninnar er breytt í _Samþykkt_ og innkaupaflokkunum er bætt við reikning lánardrottins.

### <a name="reject-a-pending-category-request"></a>Hafna tegundabeiðni í bið

Fylgið eftirfarandi skrefum til að hafna tegundabeiðni í bið.

1. Farið í **Innkaup og aðföng \> Lánardrottnar \> Beiðnir lánardrottnasamstarfs \> Tegundabeiðnir**.
1. Veljið beiðni í bið sem á að hafna.
1. Yfirfara nýja tegundabeiðni
1. Á aðgerðarúðunni skal velja **Breyta**.
1. Í flýtiflipanum **Almennt**, í reitnum **Ástæðukóði**, skal velja ástæðukóða. Síðan, í reitnum **Athugasemd ástæðu**, skal færa inn athugasemd um ástæðukóðann.
1. Í aðgerðarúðunni skal velja **Vista**.
1. Í aðgerðasvæðinu skal velja **Verkflæði**.
1. Í valkostum Verkflæðis skal velja **Meira** og síðan **Hafna**.
1. Í reitinn **Athugasemd** skal færa inn nauðsynlegar viðbótarupplýsingar. Veljið svo **Hafna** til að ljúka beiðninni.

    Stöðu tegundabeiðninnar er breytt í _Hafnað_. Á þessu stigi getur lánardrottinn stofnað nýja tegundabeiðni eftir þörfum.

### <a name="delegate-a-pending-category-request"></a>Úthluta tegundabeiðni í bið

Fylgja skal eftirfarandi skrefum til að úthluta tegundabeiðni í bið á annan notanda.

1. Farið í **Innkaup og aðföng \> Lánardrottnar \> Beiðnir lánardrottnasamstarfs \> Tegundabeiðnir**.
1. Veljið beiðni í bið sem ætlunin er að samþykkja.
1. Í aðgerðasvæðinu skal velja **Verkflæði**.
1. Í valkostum verkflæðis skal velja **Meira** og síðan **Úthluta**.
1. Í reitnum **Notandi** skal velja þann notanda sem úthluta á tegundabeiðninni vegna yfirferðar.
1. Í reitinn **Athugasemd** skal færa inn nauðsynlegar viðbótarupplýsingar.
1. Veljið **Úthluta** til að ljúka við úthlutunina. Notandinn sem er valinn getur nú farið yfir tegundabeiðnina.

### <a name="view-procurement-categories-for-a-vendor"></a>Skoða innkaupaflokka fyrir lánardrottin

Fylgið eftirfarandi skrefum til að skoða innkaupaflokka fyrir lánardrottin þegar tegundabeiðni hefur verið samþykkt.

1. Farið í **Innkaup og aðföng \> Lánardrottnar \> Allir lánardrottnar**.
1. Á síðunni **Allir lánardrottnar** skal velja lánardrottin sem ætlunin er að skoða innkaupaflokka fyrir.
1. Á aðgerðasvæðinu skal opna flipann **Almennt** og í flokknum **Setja upp** skal velja **Flokkar**.

    Þá birtist síðan **Flokkar**. Flýtiflipinn **Innkaup** sýnir innkaupaflokka sem bætt var við í gegnum tegundabeiðnina.

1. Á flýtiflipanum **Innkaup** er hægt að gera breytingar ef þörf er. Til dæmis er hægt að stilla reitinn **Tegundarstaða lánardrottins** á _Æskilegt_.
