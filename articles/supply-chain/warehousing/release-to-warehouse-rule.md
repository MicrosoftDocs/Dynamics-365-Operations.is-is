---
title: Reglu fyrir losun í vöruhús
description: Í þessu efnisatriði er að finna upplýsingar um eiginleika reglu fyrir losun í vöruhús, sem býður upp á sveigjanleika við losun í vöruhúsið. Hann bætir við skilgreiningarvalkosti sem stjórnar því hvort kerfið leyfi að losa pöntunarlínur sem eru fráteknar að hluta til.
author: mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 2fbc292ccf8e1f459bef4d70b8c37b2da8c3dd17
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580025"
---
# <a name="release-to-warehouse-rule"></a>Reglu fyrir losun í vöruhús

[!include [banner](../includes/banner.md)]

Eiginleikinn *Regla fyrir losun í vöruhús* veitir sveigjanleika þegar losað er í vöruhús. Hann bætir við skilgreiningarvalkosti fyrir hvert vöruhús. Hægt er að nota þennan valkost til að tilgreina hvort hægt sé að losa í vöruhús pöntunarlínur sem eru fráteknar að hluta til. Eiginleikinn vinnur saman með ítarlegri virkni dreifingar frá dreifingarstöð í kringumstæðum þar sem hluti af magni pöntunarlínu er merkt á móti birgðauppruna, en eftirstandandi hluta er hægt að vinna úr í vöruhúsinu. Þess vegna er hægt að losa línuna þannig að úrvinnsla vöruhúss á tiltæku birgðamagni getur haldið áfram.

## <a name="turn-on-and-initialize-the-release-to-warehouse-rule-feature"></a>Kveikja á og frumstilla eiginleikann fyrir losunarreglu í vöruhús

### <a name="turn-on-the-feature"></a>Kveikja á eiginleikanum

Áður en þú getur notað eiginleikann *Losunarregla vöruhúss* verður að vera kveikt á honum í kerfinu. Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikt á honum ef þörf krefur. Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:

- **Eining:** *Vöruhúsakerfi*
- **Heiti eiginleika:** *Losunarregla vöruhúss*

### <a name="initialize-the-feature"></a>Frumstilla eiginleikann

Þegar kveikt er á eiginleikann í kerfinu þarf að frumstilla hann til að stilla regluna á rétta upphafsstöðu fyrir öll vöruhús.

- Fyrir vöruhús sem ekki eru virkjuð fyrir vöruhúsakerfi er reglan upphaflega stillt á **Á ekki við**.
- Fyrir vöruhús sem eru virkjuð fyrir vöruhúsakerfi er reglan upphaflega stillt á **Leyfa hlutafrátekningu**

Til að frumstilla eiginleikann og stilla losunarreglu vöruhúss fyrir öll vöruhús skal fylgja þessum skrefum.

1. Farðu í **vöruhúsakerfi \> Uppsetning \> Færibreytur vöruhúsakerfis**.
1. Á síðunni **Færibreytur vöruhúsakerfis**, í flipanum **Almennt**, í hlutanum **Upplýsingar um fyrirtæki**, skal velja tengilinn fyrir regluna **Frumstilla losun í vöruhús**. (Ef þessi tengill er ekki sýndur er annaðhvort ekki kveikt á eiginleikann eða hann hefur þegar verið frumstilltur.)
1. Þegar notandi er beðinn um að staðfesta aðgerðina skal velja **Já** til að frumstilla eiginleikann.

## <a name="set-the-release-to-warehouse-rule-for-each-warehouse"></a><a name="set-option-warehouse"></a>Stilla losunarreglu vöruhúss fyrir hvert vöruhús

Þegar kveikt er á eiginleikann og hann frumstilltur verða öll vöruhús með upphaflega stillingu, eins og lýst var í hlutanum hér á undan. Hægt er að breyta þessari stillingu fyrir einstök vöruhús með því að fylgja þessum skrefum.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Vöruhús \> Vöruhús**.
1. Veljið vöruhúsið til að grunnstilla.
1. Veldu **Breyta** til að setja síðuna í breytingastillingu.
1. Í flýtiflipanum **Vöruhús**, í hlutanum **Frátekningar**, stjórnar reiturinn **Skilyrði fyrir frátekningu á birgðum** því hvort hlutafrátekning á pöntunum er leyfð. Veljið eitt af eftirfarandi gildum:

    - **Á ekki við** – Þegar kveikt er á eiginleikann og hann frumstilltur, er þessu gildi sjálfkrafa úthlutað á öll vöruhús sem ekki eru virkjuð fyrir vöruhúsakerfi. Ekki er hægt að breyta þessu. Þetta gildi er ekki í boði fyrir vöruhús sem eru virkjuð fyrir vöruhúsakerfi.
    - **Leyfa hlutafrátekningu** - Hægt er að losa pantanir þegar magn er tekið frá. Kerfið metur hvort merkja eigi ófrátekið magn fyrir ítarlega dreifingu frá dreifingarstöð og merkir það magn eftir þörfum. Ef engin merking er til staðar stofnar kerfið verk eingöngu fyrir frátekna magnið. Þegar kveikt er á eiginleikann og hann frumstilltur, er þessu gildi sjálfkrafa úthlutað á öll vöruhús sem eru virkjuð fyrir vöruhúsakerfi. Þetta gildi er ekki í boði fyrir vöruhús sem eru ekki virkjuð fyrir vöruhúsakerfi.
    - **Krefjast fullrar frátektar** – Aðeins er hægt að losa pantanir ef allt magnið er tekið frá. Ekki er hægt að losa þær ef heildarmagnið er ekki annaðhvort efnislega frátekið eða áætlað fyrir dreifingu frá dreifingarstöð. Þetta gildi er ekki í boði fyrir vöruhús sem eru ekki virkjuð fyrir vöruhúsakerfi.

1. Veljið **Vista**.

## <a name="scenarios"></a>Sviðsmyndir

Þessi hluti býður upp á tvær aðstæður sem hægt er að vinna með til að fræðast um hvað eiginleikinn gerir og hvernig á að nota hann.

### <a name="make-sample-data-available"></a>Gera sýnigögn tiltæk

Til að vinna í gegnum þessar sýniaðstæður með því að nota sýniskrárnar og sýnigildin sem eru kynnt í þessu efnisatriði verður þú að vinna á kerfi þar sem venjulegu [sýnigögnin](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) eru sett upp. Þar að auki verður þú að velja **USMF**-lögaðila áður en þú byrjar.

Einnig er hægt að nota þessa atburðarás sem leiðsögn fyrir eiginleikann þegar unnið er í framleiðslukerfi. Í slíku tilfelli þarf hinsvegar að skipta út eigin gildum og einhverjar nauðsynlegar færslugerðir gæti vantað sem stöðluðu sýnigögnin bjóða upp á.

### <a name="scenario-1-require-full-release-no-planned-cross-docking"></a><a name="scenario1"></a>Aðstæður 1: Krefjast fullrar losunar (engin áætluð dreifing frá dreifingarstöð)

Þessar aðstæður sýna hvernig eiginleikinn virkar fyrir vöruhús sem stillt eru á **Krefjast fullrar frátekningar**.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Vöruhús \> Vöruhús**.
1. Fyrir vöruhús _62_ skal stilla reitinn **Skilyrði fyrir frátekningu á birgðum** á **Krefjast fullrar frátekningar** eins og lýst er í hlutanum [Stilla losunarreglu vöruhúss fyrir hvert vöruhús](#set-option-warehouse) fyrr í þessu efnisatriði.
1. Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.
1. Smellið á **Nýtt** til að stofna nýja sölupöntun.
1. Sláið inn eftirfarandi gildi í svarglugganum **Stofna sölupöntun**:

    - Í flipanum **Viðskiptavinur** skaltu stilla reitinn **Reikningur viðskiptavinar** á _US-004_.
    - Í flýtiflipanum **Almennt** skal stilla reitinn **Vöruhús** á _62_.

1. Veljið **Í lagi** til að stofna nýja sölupöntun og loka svarglugganum.
1. Nýja sölupöntunin þín opnast. Hún inniheldur auða línu í hnitaneti í hlutanum **Sölupöntunarlínur**. Stilltu eftirfarandi gildi á þessari línu:

    - **Vörunúmer:** *A0001*
    - **Magn:** *2*

1. Veldu **Bæta við línu** til að bæta við nýrri línu og stilltu eftirfarandi gildi:

    - **Vörunúmer:** *A0002*
    - **Magn:** *2*

1. Veljið fyrstu pöntunarlínuna og síðan í valmyndinni **Birgðir** fyrir ofan hnitanetið skal smella á **Frátekning**.
1. Á síðunni **Frátekning** skal velja **Frátektarlota** til að taka frá heildarmagn valdrar línu í vöruhúsinu.
1. Lokið síðunni **Frátekning** til að fara aftur í sölupöntunina.
1. Ekki taka frá pöntunarlínu númer tvö.
1. Á aðgerðasvæðinu, í flipanum **Vöruhús**, skal velja **Losa í vöruhús**.
1. Takið eftir að eftirfarandi villuboð birtast: „Taka verður heildarmagn efnislega frá.“ Þess vegna stofnar kerfið enga vinnu, sendingu eða hleðslu fyrir pöntunina.

    > [!NOTE]
    > Sömu villuboðin birtast ef lína tvö er frátekin að hluta til.

### <a name="scenario-2-allow-partial-release"></a>Aðstæður 2: Leyfa hlutalosun

Þessar aðstæður sýna hvernig eiginleikinn virkar fyrir vöruhús sem stillt eru á **Leyfa hlutalosun**.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Vöruhús \> Vöruhús**.
1. Fyrir vöruhús _62_ skal stilla reitinn **Skilyrði fyrir frátekningu á birgðum** á **Leyfa hlutafrátekningu** eins og lýst er í hlutanum [Stilla losunarreglu vöruhúss fyrir hvert vöruhús](#set-option-warehouse) fyrr í þessu efnisatriði.
1. Eins og gert var í [fyrri aðstæðum](#scenario1) skal fara í **Sala og markaðssetning \> Sölupantanir \> Allar sölupantanir** og stofna sölupöntun fyrir viðskiptavinalykil _US-004_ úr vöruhúsi _62_. Bætið við eftirfarandi tveimur pöntunarlínum:

    - **Lína 1:** Stillið reitinn **Vörunúmer** á _A0001_, reitinn **Magn** á _2_ og reitinn **Eining** á _ea_.
    - **Lína 2:** Stillið reitinn **Vörunúmer** á _A0002_, reitinn **Magn** á _2_ og reitinn **Eining** á _ea_.

1. Eins og gert var í [fyrri aðstæðum](#scenario1) skal taka frá heildarmagn fyrir pöntunarlínu 1, en ekki taka frá pöntunarlínu 2.
1. Á aðgerðasvæðinu, í flipanum **Vöruhús**, skal velja **Losa í vöruhús**.
1. Takið eftir að villuboð birtast ekki í þetta skipti. Þess í stað stofnar kerfið vinnu, sendingar og hleðslur eins og ætlast er til og sýnir niðurstöðurnar.
1. Til að skoða upplýsingar um sendingar, hleðslu og vinnu skal nota valkostina í valmyndinni **Vöruhús** fyrir ofan hnitanetið:

    - **Lína 1:** Þrír valkostir eru í boði: **Sendingarupplýsingar**, **Upplýsingar um hleðslu** og **Upplýsingar um verk**. Velja skal hvern valkost til að skoða upplýsingar um sendinguna, hleðsluna og vinnuna sem stofnað var þegar pöntunin var losuð í vöruhúsið.
    - **Lína 2:** Aðeins valkosturinn **Upplýsingar um verk** er í boði. Veljið hann og takið eftir að ekkert verk hefur verið stofnað því að engar birgðir voru teknar frá. Þess vegna var engin sending eða hleðsla stofnuð heldur.

> [!NOTE]
> Vænta má sömu útkomu þegar lína tvö er frátekin að hluta. Í því tilfelli verður verk stofnað fyrir magn frátekinnar línu en ekki fyrir ófrátekna magnið.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]