---
title: Vinnureglur
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp vinnureglur.
author: perlynne
manager: tfehr
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPolicy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 530abffb4c80a2d2f0e58e0c5a34294f7cba0b1a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4998454"
---
# <a name="work-policies"></a>Vinnureglur

[!include [banner](../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig á að setja upp kerfið og vöruhúsaforritið þannig að þau styðji vinnureglur. Hægt er að nota þessa virkni til að skrá birgðir á fljótlegan hátt án þess að stofna frágangsvinnu þegar tekið er á móti innkaupa- eða flutningspöntun, eða þegar lokið er við framleiðsluferla. Þetta efnisatriði veitir almennar upplýsingar. Ítarlegar upplýsingar sem tengjast móttöku á númeraplötu er að finna í [Móttaka númeraplötu í gegnum vöruhúsaforritið](warehousing-mobile-device-app-license-plate-receiving.md).

Vinnuregla stjórnar því hvort vöruhúsavinna sé stofnuð þegar framleidd vara er tilkynnt sem lokið eða þegar tekið er á móti vörum með því að nota vöruhúsaforritið. Setja skal upp hverja vinnureglu með því að skilgreina skilyrðin þar sem það á við: gerðir verkbeiðna og ferlar, birgðastaðsetningar og (valfrjálst) afurðirnar. Til dæmis þarf að móttaka innkaupapöntun fyrir afurð *A0001* á staðsetningu *RECV* í vöruhúsi *24*. Síðar er afurðin notuð í öðru ferli á staðsetningu *RECV*. Í slíku tilfelli er hægt að setja upp vinnureglu til að koma í veg fyrir að frágangsvinna verði stofnuð þegar starfsmaður tilkynnir afurð *A0001* sem móttekna á staðsetningu *RECV*.

> [!NOTE]
> - Til að vinnuregla verði virk þarf að skilgreina að minnsta kosti eina staðsetningu fyrir hana í flýtiflipanum **Birgðastaðsetningar** á síðunni **Vinnureglur**. 
> - Ekki er hægt að tilgreina sömu staðsetninguna fyrir margar vinnureglur.
> - Valkosturinn **Prenta merki** fyrir valmyndaratriði fartækis prentar ekki númeraplötumerki nema vinna hafi verið stofnuð.

## <a name="activate-the-features-in-your-system"></a>Gera eiginleikana virka í kerfinu

Til að bjóða upp á alla þá virkni sem lýst er í þessu efnisatriði í kerfinu, skal kveikja á eftirfarandi tveimur eiginleikum í [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- Viðbætur við móttöku á númeraplötu
- Endurbætur á vinnureglu fyrir vinnu á innleið

## <a name="the-work-policies-page"></a>Vinnureglusíðan

Til að setja upp vinnureglur skal fara í **Vöruhúsakerfi \> Uppsetning \> Vinna \> Vinnureglur**. Því næst, í hverjum flýtiflipa, skal stilla reitina eins og lýst er í eftirfarandi undirhlutum.

### <a name="the-work-order-types-fasttab"></a>Flýtiflipi fyrir gerðir verkbeiðna

Í flýtiflipanum **Gerðir verkbeiðna** skal bæta við öllum gerðum verkbeiðna og tengdum vinnuferlum sem vinnureglan gildir um. Eftirfarandi gerðir verkbeiðni og tengdir vinnuferlar eru studdir fyrir vinnureglur.

| Gerð verkpöntunar | Vinnuferli |
|---|---|
| Tiltekt hráefnis| Öll tengd ferli |
| Frágangur aukaafurða og hliðarafurða | Öll tengd ferli |
| Frágangur fullbúinnar vöru | Öll tengd ferli |
| Flutningsinnhreyfing | Móttaka (og frágangur) númeraplötu |
| Innkaupapantanir | <ul><li>Móttaka (og frágangur) númeraplötu</li><li>Móttaka (og frágangur) farmvöru</li><li>Móttaka (og frágangur) innkaupapöntunarlínu</li><li>Móttaka (og frágangur) innkaupapöntunarvöru</li></ul> |

Til að setja upp vinnureglu þannig að hún eigi við um nokkra vinnuferla sömu verkbeiðnigerðar, skal bæta aðskildri línu fyrir hvert vinnuferli við hnitanetið.

Fyrir hverja línu í hnitanetinu skal stilla reitinn **Aðferðir vinnustofnunar** á eitt af eftirfarandi gildum:

- **Aldrei** - Vinnureglan kemur í veg fyrir að vöruhúsavinna verði stofnuð fyrir valda verkbeiðnigerð og tengt vinnuferli.
- **Dreifing frá dreifingarstöð** - Vinnureglan stofnar dreifingarvinnu frá dreifingarstöð með því að nota regluna sem var valin í reitnum **Heiti reglu fyrir dreifingu frá dreifingarstöð**.

### <a name="the-inventory-locations-fasttab"></a>Flýtiflipi birgðastaðsetninga

Í flýtiflipanum **Birgðastaðsetningar** skal bæta við staðsetningunum þar sem þessi vinnuregla á að gilda. Ef engin staðsetning tengist vinnureglu, verður vinnureglan ekki notuð fyrir neitt ferli.

Ekki er hægt að tilgreina sömu staðsetninguna fyrir margar vinnureglur.

Hægt er að nota vöruhúsastaðsetningu sem er úthlutað á staðsetningarforstillingu þar sem slökkt er á valkostinum **Nota rakningu númeraplötu**. Í slíku tilfelli skrá starfsmenn lagerbirgðirnir beint.

### <a name="the-products-fasttab"></a>Flýtiflipi afurða

Í flipanum **Afurðir** skal stilla reitinn **Afurðaval** til að stjórna því hvaða afurðir reglan á að gilda fyrir:

- **Allar** – Reglan á að gilda um allar afurðir.
- **Valið** – Reglan á aðeins að gilda um afurðir sem koma fram í hnitanetinu. Notið tækjastikuna í flýtiflipanum **Afurðir** til að bæta afurðum við hnitanetið eða fjarlægja þær úr hnitanetinu.

## <a name="default-and-custom-to-locations"></a>Sjálfgefnar og sérsniðnar „til“ staðsetningar

> [!NOTE]
> Til að gera virknina sem lýst er í þessum hluta tiltæka í kerfinu þarf að kveikja á eiginleikunum *Viðbætur við móttöku á númeraplötu* og *Viðbætur við vinnureglu fyrir vinnu á innleið* í [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Áður studdi kerfið að taka aðeins á móti á sjálfgefinni staðsetningu sem er skilgreind fyrir hvert vöruhús. Valmyndaratriði fartækis sem nota eftirfarandi ferla við stofnun vinnu bjóða aftur á móti upp á valkostinn **Nota sjálfgefin gögn**. Þessi valkostur gerir kleift að úthluta sérstilltri "til" staðsetningu á eitt eða fleiri valmyndaratriði. (Þessi valkostur var þegar tiltækur fyrir nokkrar aðrar gerðir valmyndaratriða.)

- Móttaka (og frágangur) númeraplötu
- Móttaka (og frágangur) farmvöru
- Móttaka (og frágangur) innkaupapöntunarlínu
- Móttaka (og frágangur) innkaupapöntunarvöru

Stillingin **Til staðsetningar** fyrir valmyndaratriði hnekkir sjálfgefinni móttökustaðsetningu fyrir vöruhúsið, fyrir allar pantanir sem unnið er úr með því að nota þetta valmyndaratriði.

Til að setja upp valmyndaratriði fartækis til að styðja móttöku á sérstilltri staðsetningu skal fylgja þessum skrefum.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmyndaratriði fartækis**.
1. Veljið eða búið til valmyndaratriði sem notar einn ferlanna við stofnun vinnu sem gefnir eru upp í þessum hluta.
1. Í flipanum **Almennt** skal stilla valkostinn **Nota sjálfgefin gögn** á **Já**.
1. Á aðgerðasvæðinu skal velja **Sjálfgefin gögn**.
1. Á síðunni **Sjálfgefin gögn** skal stilla eftirfarandi gildi:

    - **Reitur sjálfgefinna gagna:** Stilið þennan reit á *Til staðsetningar*.
    - **Vöruhús:** Veljið vöruhús áfangastaðar til að nota með þessu valmyndaratriði.
    - **Staðsetning:** Þessi reitur birtir öll staðsetningarauðkennin sem eru í boði fyrir valið vöruhús. Stillingin á þessum reit hefur hins vegar engin áhrif í raun og veru. Þess vegna er hægt að skilja hann eftir auðan. Engu að síður er hægt að nota listann til að staðfesta auðkennið sem færa verður inn í reitinn **Harðkóðað gildi**.
    - **Harðkóðað gildi:** Færið inn staðsetningarauðkennið fyrir móttökustaðsetninguna sem gildir um þetta valmyndaratriði.

> [!TIP]
> Vinnureglu er aðeins hægt að nota ef allar móttökustaðsetningarnar eru gefnar upp í uppsetningu viðeigandi vinnureglu. Þessi krafa gildir óháð því hvort verið sé að nota sjálfgefna móttökustaðsetningu vöruhúss eða sérstillta „til“ staðsetningu.

## <a name="example-scenario-warehouse-receiving"></a>Sýnidæmi: Vöruhúsamóttaka

Allar afurðir sem tekið er á móti með ferlinu *Móttaka (og frágangur) innkaupapöntunarvöru* verða að vera skráðar í staðsetningu *FL-001* og þær verða að vera tiltækar í vöruhúsi *24*. Hins vegar ætti ekki að stofna vinnu. Afurðir sem tekið er á móti með einhverju öðru ferli (þ.e. með því að nota önnur valmyndaratriði fartækis) á að skrá á sjálfgefna móttökustaðsetningu vöruhúss (*RECV*) og vinnu á að stofna eins og venjulega. (Þetta dæmi sýnir ekki uppsetningu sjálfgefinnar móttöku.)

Þetta dæmi krefst eftirfarandi þátta:

- Vinnureglu fyrir ferlið *Móttaka (og frágangur) innkaupapöntunarvöru* á staðsetningu *FL-001* fyrir allar afurðir
- Valmyndaratriði fartækis sem inniheldur sjálfgefin gögn og sem stillir reitinn **Til staðsetningar** á *FL-001*

### <a name="prerequisites"></a>Forkröfur

Til að gera virknina sem lýst er í þessu dæmi tiltæka í kerfinu þarf að kveikja á eiginleikunum *Viðbætur við móttöku á númeraplötu* og *Viðbætur við vinnureglu fyrir vinnu á innleið* í [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Þetta dæmi notar stöðluð sýnigögn. Til að fara í gegnum það með því að nota gildin sem hér koma fram, þarf að nota kerfi þar sem sýnigögn eru uppsett. Þar að auki verður þú að velja **USMF**-lögaðila.

### <a name="set-up-a-work-policy"></a>Setja upp vinnureglu

1. Fara í **Vöruhúsakerfi \> Uppsetning \> Vinna \> Vinnureglur**.
1. Veljið **Nýtt**.
1. Í reitinn **Heiti vinnureglu** skal færa inn *Engin frágangsvinna innkaupavöru*.
1. Veljið **Vista**.
1. Í flýtiflipanum **Gerðir verkbeiðni** skal velja **Bæta við** til að bæta línu við hnitanetið og síðan stilla eftirfarandi gildi fyrir nýju línuna:

    - **Gerð verkbeiðni:** *Innkaupapantanir*
    - **Vinnuferli:** *Móttaka (og frágangur) innkaupapöntunarvöru*
    - **Aðferð við stofnun vinnu:** *Aldrei*
    - **Heiti reglu fyrir dreifingu frá dreifingarstöð:** Skiljið reitinn eftir auðan.

1. Í flýtiflipanum **Birgðastaðsetningar** skal velja **Bæta við** til að bæta línu við hnitanetið og síðan stilla eftirfarandi gildi fyrir nýju línuna:

    - **Vöruhús:** *24*
    - **Staðsetning:** *FL-001*

1. Í flýtiflipanum **Afurðir** skal stilla reitinn **Afurðaval** á *Allt*.
1. Veljið **Vista**.

### <a name="set-up-a-mobile-device-menu-item-to-change-the-receiving-location"></a>Setja upp valmyndaratriði fartækis til að breyta móttökustaðsetningunni

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmyndaratriði fartækis**.
1. Á svæðinu vinstra megin skal velja fyrirliggjandi valmyndaratriði fyrir **Móttaka innkaupa**.
1. Í flipanum **Almennt** skal stilla valkostinn **Nota sjálfgefin gögn** á *Já*.
1. Veljið **Vista**.
1. Á aðgerðasvæðinu skal velja **Sjálfgefin gögn**.
1. Í flýtiflipanum **Sjálfgefin gögn**, á aðgerðasvæðinu, skal velja **Ný** til að bæta línu við hnitanetið og síðan stilla eftirfarandi gildi fyrir nýju línuna:

    - **Reitur sjálfgefinna gagna:** *Til staðsetningar*
    - **Vöruhús:** *24*
    - **Staðsetning:** Skiljið þennan reit eftir auðan.
    - **Harðkóðað gildi:** *FL-001*

1. Veljið **Vista**.

### <a name="receive-a-purchase-order-without-creating-work"></a>Móttaka innkaupapöntun án stofnunar vinnu

Dæmið í þessum hluta sýnir hvernig á að taka á móti vöru innkaupapöntunar, en án þess að stofna vinnu, á staðsetningu sem er ólík sjálfgefinni móttökustaðsetningu sem er uppsett fyrir vöruhúsið. Þetta dæmi notar vinnuregluna og atriði fartækis sem búið var til fyrr í þessu sýnidæmi.

#### <a name="create-a-purchase-order"></a>Stofna innkaupapöntun

1. Farðu í **Innkaup og aðföng \> Innkaupapantanir \> Allar innkaupapantanir**.
1. Veljið **Nýtt**.
1. Sláðu inn eftirfarandi gildi í svarglugganum **Búa til innkaupapöntun**:

    - **Lánardrottnalykill:** *US-101*
    - **Svæði:** *2*
    - **Vöruhús:** *24*

1. Veljið **Í lagi** til að loka svarglugganum og opnið nýju innkaupapöntunina.
1. Í flýtiflipanum **Innkaupapöntunarlínur** skal stilla eftirfarandi gildi fyrir auðu línuna:

    - **Vörunúmer:** *A0001*
    - **Magn:** *1*

1. Veljið **Vista**.
1. Skráið niður innkaupapöntunarnúmerið.

#### <a name="receive-a-purchase-order"></a>Móttaka innkaupapöntunar

1. Í fartækinu skal skrá sig inn í vöruhús *24* með því að nota *24* fyrir notandakenni og *1* fyrir aðgangsorð.
1. Veljið **Á innleið**.
1. Veljið **Innkaup móttekin**. Reiturinn **Staðsetning** ætti að stilla á *FL-001*.
1. Sláið inn innkaupapöntunarnúmerið fyrir innkaupapöntunina sem var stofnuð í fyrra ferlinu.
1. Í **vörunúmerasvæðið** skal slá inn *A0001*.
1. Veljið **Í lagi**.
1. Í **Magn** reitinn er fært inn *1*.
1. Veljið **Í lagi**.

Innkaupapöntunin er nú móttekin en engin vinna er tengd henni. Lagerbirgðir hafa verið uppfærðar og magn *1* af vöru *A0001* er nú tiltækt á staðsetningu *FL-001*.

## <a name="example-scenario-manufacturing"></a>Sýnidæmi: Framleiðsla

Í eftirfarandi dæmi eru tvær framleiðslupantanir, *PRD 001* og *PRD 002*. Framleiðslupöntunin *PRD-001* hefur aðgerðar sem nefnist *Samsetningu*, þar sem afurð *SC1* verið skráð sem lokið á staðsetningu *001*. Framleiðslupöntunin *PRD 002* hefur aðgerðar sem nefnist *Málun* og notar afurð *SC1* frá staðsetningu *001*. Framleiðslupöntunin *PRD-002* notar einnig *RM1* hráefni úr staðsetningunni *001*. Hráefni *RM1* er geymt á staðsetningu vöruhúss *BULK-001* og verður tínt yfir á staðsetningu *001* af vöruhúsavinnu fyrir tiltekt hráefnis. Vinna tiltektar er myndað þegar *PRD 002 framleiðsla* er losuð.

[![Reglur vöruhúsavinnu](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)

Þegar ætlunin er að skilgreina vinnureglu vöruhúss fyrir þetta sýnidæmi ætti að hafa eftirfarandi punkta í huga:

- Vöruhúsavinna fyrir frágang á fullbúnum vörum er ekki áskilin þegar afurð *SC1* er tilkynnt sem lokið frá framleiðslupöntun *PRD-001* til staðsetningar *001*. Ástæðan er vegna þess að aðgerðin *Málun* fyrir framleiðslupöntun *PRD 002* notar afurð *SC1* á sömu staðsetningunni.
- Vinna vöruhús fyrir tiltekt hráefnis er krafist til að flytja *RM1* hráefni frá staðsetningu vöruhúss *BULK-001* á staðsetningu *001*.

Hér er dæmi um vinnureglu sem hægt er að setja upp, byggt á þessum atriðum:

- **Heiti vinnureglu:** *Engin frágangsvinna*
- **Gerðir verkbeiðna:** *Frágangur fullbúinna vara* og *Frágangur aukaafurða og hliðarafurða*
- **Birgðastaðsetningar:** Vöruhús *51* og staðsetning *001*
- **Afurðir:** *SC1*

Eftirfarandi sýnidæmi býður upp á ítarlegar leiðbeiningar um uppsetningu á vinnureglu vöruhúss fyrir þetta dæmi.

## <a name="example-scenario-report-as-finished-to-a-location-that-isnt-license-platecontrolled"></a>Sýnidæmi: Tilkynna sem lokið á staðsetningu sem er ekki númeraplötustýrð

Þetta sýnidæmi kemur með dæmi þar sem framleiðslupöntun er tilkynnt sem lokið á staðsetningu sem er ekki númeraplötustýrð.

Þetta dæmi notar stöðluð sýnigögn. Til að fara í gegnum það með því að nota gildin sem hér koma fram, þarf að nota kerfi þar sem sýnigögn eru uppsett. Þar að auki verður þú að velja **USMF**-lögaðila.

### <a name="set-up-a-warehouse-work-policy"></a>Setja upp reglur vöruhúsavinnu

Ferli vöruhúsa innihalda ekki alltaf vöruhúsavinnu. Með því að skilgreina vinnustefnu, sem getur komið í veg fyrir stofnun vinnu fyrir tiltekt hráefnis og frágangur fullbúinna vara fyrir safn af afurðum á tiltekna staði.

1. Fara í **Vöruhúsakerfi \> Uppsetning \> Vinna \> Vinnureglur**.
1. Veljið **Nýtt**.
1. Í reitinn **Heiti vinnureglu** skal færa inn *Engin frágangsvinna*.
1. Í aðgerðarúðunni skal velja **Vista**.
1. Í flýtiflipanum **Gerðir verkbeiðni** skal velja **Bæta við** til að bæta línu við hnitanetið og síðan stilla eftirfarandi gildi fyrir nýju línuna:

    - **Gerð verkbeiðni:** *Frágangur á fullunnum vörum*
    - **Vinnuferli:** *Öll tengd vinnuferli*
    - **Aðferð við stofnun vinnu:** *Aldrei*
    - **Heiti reglu fyrir dreifingu frá dreifingarstöð:** Skiljið reitinn eftir auðan.

1. Veljið **Bæta við** aftur til að bæta annarri línu við hnitanetið og því næst stilla eftirfarandi gildi fyrir nýju línuna:

    - **Gerð verkbeiðni:** *Frágangur aukaafurða og hliðarafurða*
    - **Vinnuferli:** *Öll tengd vinnuferli*
    - **Aðferð við stofnun vinnu:** *Aldrei*
    - **Heiti reglu fyrir dreifingu frá dreifingarstöð:** Skiljið reitinn eftir auðan.

1. Í flýtiflipanum **Birgðastaðsetningar** skal velja **Bæta við** til að bæta línu við hnitanetið og síðan stilla eftirfarandi gildi fyrir nýju línuna:

    - **Vöruhús:** *51*
    - **Staðsetning:** *001*

1. Í flýtiflipanum **Afurðir** skal stilla reitinn **Afurðaval** á *Valið*.
1. Í flýtiflipanum **Afurðir** skal velja **Bæta við** til að bæta línu við hnitanetið.
1. Í nýju línunni skal stilla reitinn **Vörunúmer** á *L0101*.
1. Í aðgerðarúðunni skal velja **Vista**.

### <a name="set-up-an-output-location"></a>Setja upp staðsetningu úttaks

1. Fara á **Fyrirtækisstjórnun \> Tilföng \> Tilfangaflokkar**.
1. Á svæðinu vinstra megin skal velja tilfangaflokkinn **5102**.
1. Stilltu eftirfarandi gildi á flýtiflipanum **Almennt**:

    - **Vöruhús úttaks:** *51*
    - **Staðsetning úttaks:** *001*

1. Í aðgerðarúðunni skal velja **Vista**.

> [!NOTE]
> Staðsetning *001* er ekki númeraplötustýrð staðsetning. Hægt er að setja upp staðsetningu úttaks sem er ekki númeraplötustýrð eingöngu ef gildandi vinnuregla er til fyrir staðsetninguna.

### <a name="create-a-production-order-and-report-it-as-finished"></a>Stofna framleiðslupöntun og skrá sem lokið.

1. Fara í **Framleiðslustýringar \> Framleiðslupantanir \> Allar framleiðslupantanir**.
1. Á aðgerðasvæðinu skal velja **Ný framleiðslupöntun**.
1. Í svarglugganum **Stofna framleiðslupöntun** skal stilla reitinn **Vörunúmer** á *L0101*.
1. Veljið **Stofna** til að stofna pöntunina og loka svarglugganum.

    Ný framleiðslupöntun er bætt við hnitanetið á síðunni **Allar framleiðslupantanir**.

    Halda nýju framleiðslupöntuninni valdri.

1. Á aðgerðasvæðinu, í flipanum **Framleiðslupöntun**, í flokknum **Uppsetning**, skal velja **Áætla**.
1. Í svarglugganum **Áætla** skal lesa áætlunina og síðan velja **Í lagi** til að loka svarglugganum.
1. Á aðgerðasvæðinu, í flipanum **Framleiðslupöntun**, í flokknum **Uppsetning**, skal velja **Hefja**.
1. Í svarglugganum **Hefja**, í flipanum **Almennt**, skal stilla reitinn **Sjálfvirk uppskriftanotkun** á *Aldrei*.
1. Veldu **Í lagi** til að vista stillingarnar þínar og loka glugganum.
1. Á aðgerðasvæðinu, í flipanum **Framleiðslupöntun**, í flokknum **Uppsetning**, skal velja **Tilkynna sem lokið**.
1. Í svarglugganum **Tilkynna sem lokið**, í flipanum **Almennt**, skal stilla valkostinn **Leyfa villu** á *Já*.
1. Veldu **Í lagi** til að vista stillingarnar þínar og loka glugganum.
1. Á aðgerðarrúðunni, á flipanum **Vöruhús**, í hópnum **Almennt** skaltu velja **Upplýsingar um vinnu**.

Þegar framleiðslupöntunin er tilkynnt sem lokið, er engin vinna búin til fyrir frágang. Þetta gerist vegna þess að vinna regla er skilgreind sem kemur í veg fyrir vinnu búnar til þegar afurð *L0101* er skráð sem lokið á staðsetningu *001*.

## <a name="more-information"></a>Meiri upplýsingar

Nánari upplýsingar um valmyndaratriði fartækja, sjá [Uppsetning fartækja fyrir vöruhúsavinnu](configure-mobile-devices-warehouse.md).

Frekari upplýsingar um móttöku á númeraplötu og vinnureglur er að finna í [Móttaka númeraplötu í gegnum vöruhúsaforritið](warehousing-mobile-device-app-license-plate-receiving.md).

Frekari upplýsingar um stjórnun á farmi á innleið er að finna í [Meðhöndlun vöruhúss á farmi á innleið fyrir innkaupapantanir](inbound-load-handling.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]