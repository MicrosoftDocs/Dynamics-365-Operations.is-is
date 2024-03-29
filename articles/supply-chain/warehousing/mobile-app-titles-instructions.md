---
title: Sérsníða þrepatitla og leiðbeiningar fyrir farsímaforrit Warehouse Management
description: Þessi grein lýsir því hvernig á að búa til og sýna sérsniðnar leiðbeiningar fyrir hvert skref verkflæðis sem er sett upp fyrir fartækjaforrit vöruhúsakerfis.
author: Mirzaab
ms.date: 08/09/2022
ms.topic: article
ms.search.form: WHSMobileAppFlowStepListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-08-11
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: faa9bfa320823664603153601c56654170e7e23a
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334477"
---
# <a name="customize-step-titles-and-instructions-for-the-warehouse-management-mobile-app"></a>Sérsníða þrepatitla og leiðbeiningar fyrir farsímaforrit Warehouse Management

> [!IMPORTANT]
> Eiginleikarnir sem lýst er í þessari greineiga aðeins við um nýja farsímaforrit Warehouse Management. Þeir hafa ekki áhrif á gamla vöruhúsaforrið, sem nú er úrelt.

Þessi grein lýsir því hvernig á að búa til og sýna sérsniðnar leiðbeiningar fyrir öll skref allra verkflæða sem eru sett upp fyrir fartækjaforrit vöruhúsakerfis. Þegar starfsmenn vöruhússins fá vel skrifaðar leiðbeiningar geta þeir strax byrjað að nota ný flæði án þess að þurfa neina þjálfun. Þessi eiginleiki veitir eftirfarandi ávinning:

- **Undirbúðu starfsmenn á fljótlegri hátt með því að leyfa þeim að fylgja einföldum leiðbeiningum fyrir hvert skref í verki.** Í hverju skrefi flæðis eru leiðbeiningar sem gera starfsmönnum í framlínu kleift að skilja verkið.
- **Útvegaðu leiðbeiningar sem passa við þína eigin ferla.** Skrifaðu eigin leiðbeiningar sem passa við viðskipta- og vöruhúsaferli þín. Þú getur til dæmis látið orðalagið passa við þinn raunveruleika og staðbundnar skammstafanir.

## <a name="turn-the-warehouse-app-step-instructions-feature-on-or-off"></a>Kveikja eða slökkva á eiginleika fyrir skrefaleiðbeiningar vöruhúsaforrits

Áður en hægt er að nota þennan eiginleika þarf að kveikja á honum í kerfinu. (Frá og með útgáfu 10.0.29 af Supply Chain Management er þessi eiginleiki skylda og ekki er hægt að slökkva á honum.) Ef þú ert að keyra útgáfu sem er eldri en 10.0.29, þá geta stjórnendur kveikt eða slökkt á þessum eiginleika með því að leita að eiginleikanum *Leiðbeiningar fyrir skref vöruhúsaforrits* á vinnusvæðinu [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="step-titles-and-step-instructions-in-the-app"></a>Titlar og leiðbeiningar skrefa í forritinu

Hvert skref í verkflæði í fartækjaforriti Warehouse Management er auðkennt með skrefakenni. Auk þess er titill, táknmynd og leiðbeiningar í hverju skrefi. (Frekari upplýsingar er að finna í [Úthluta skrefatáknum og titlum fyrir farsímaforrit Warehouse Management](step-icons-titles.md).)

### <a name="step-titles"></a>Titill skrefs

*Titill skrefs* er stutt lýsing á hvað starfsmaður á að gera í skrefi. Hann birtist sem stór texti efst á skjánum, eins og sýnt er á eftirfarandi mynd.

![Dæmi um titil skrefs í fartækjaforriti Warehouse Management](media/wma-step-title.png "Dæmi um titil skrefs í fartækjaforriti Warehouse Management")

> [!TIP]
> Vegna þess hve textinn er stór ættir þú að reyna að hafa titil skrefanna eins stuttan og mögulegt er. Annars gæti verið klippt á textann. Fyrir langa titla geta starfsmenn þó enn ýtt á og haldið inni titlinum til að opna svarglugga sem sýnir allan textann.

### <a name="step-instructions"></a>Fyrirmæli skrefs

*Skrefaleiðbeining* er lengri lýsing sem veitir frekari upplýsingar um hvað starfsmaður á að gera í skrefinu. Hún birtist í sprettiglugga eins og sýnt er á eftirfarandi mynd.

![Dæmi um skrefaleiðbeiningu í fartækjaforrit Warehouse Management](media/wma-step-instructions.png "Dæmi um skrefaleiðbeiningu í fartækjaforriti Warehouse Management")

Skrefaleiðbeiningin er sjálfkrafa sýnd þegar skref er opnað. Starfsmenn geta afþakkað hana með því að pikka út fyrir sprettigluggann. Að auki inniheldur svarglugginn gátreitinn **Ekki sýna aftur** sem starfsmenn geta valið til að koma í veg fyrir að leiðbeiningin birtist næst þegar þeir framkvæma sama verkið.

## <a name="load-the-default-setup"></a>Hlaða sjálfgefinni uppsetningu

Þegar þú kveikir fyrst á eiginleikanum *Skrefaleiðbeiningar vöruhúsaforrits* mun kerfið ekki innihalda neina sérsniðna skrefatitla eða leiðbeiningar. Þú ættir þar af leiðandi fyrst að hlaða inn sjálfgefinni uppsetningu. Sjálfgefin uppsetning gefur upp texta fyrir öll tiltæk skrefakenni á öllum studdum tungumálum. Til að hlaða sjálfgefinni uppsetningu skal fylgja þessum skrefum.

1. Farðu í **Warehouse Management \> Uppsetning \> Fartæki \> Skref fartækis**.
1. Á aðgerðasvæðinu skal velja **Stofna sjálfgefna uppsetningu**: Fyllt er út í síðuna með stöðluðum skrefum.

## <a name="customize-step-titles-and-instructions"></a>Sérsníða titla og leiðbeiningar skrefa

Til að sérsníða titil og/eða leiðbeiningar fyrir hvert skref á hvaða fjölda tungumála sem er skaltu fylgja þessum skrefum.

1. Farðu í **Warehouse Management \> Uppsetning \> Fartæki \> Skref fartækis**.

    Í síðulistanum **Skref fartækis** eru öll tiltæk skref í kerfinu sýnd. Hægt er að deila hvaða skrefakenni sem er með eins mörgum valmyndaratriðum fartækis og þarf til. Ef skrefakenni er deilt með mörgum valmyndaratriðum er sami titill og leiðbeining sýnd fyrir öll þessi valmyndaratriði. Hins vegar geturðu búið til hnekkingar til að sérsníða titil og leiðbeiningu fyrir tiltekin valmyndaratriði. (Nánari upplýsingar er að finna í næsta hluta.)

    Netið inniheldur eftirfarandi dálka:

    - **Heiti valmyndaratriðis** – Línur þar sem þessi dálkur er auður nota sjálfgefinn titil og leiðbeiningu skrefs sem gilda um öll valmyndaratriði fartækis sem engin hnekking er skilgreind fyrir. Línur þar sem þessi dálkur er stilltur á heiti valmyndaratriðis eru með hnekkingar sem gilda aðeins um tiltekið valmyndaratriði.
    - **Kenni skrefs** – Einkvæmt auðkenni skrefs.
    - **Titill fyrir innslátt** – Titillinn sem er sýndur þegar forritið biður um nýjar upplýsingar. Venjulega eru reitirnir á síðunni auðir (þ.e. þeir eru ekki með nein forstillt gildi).
    - **Titill til staðfestingar** – Titillinn sem er sýndur þegar forritið biður um staðfestingu á gildi sem er þegar vistað í kerfinu. Venjulega hafa reitirnir á síðunni forstillt gildi.

1. Finndu samsetningu gilda fyrir **Kenni skrefs** og **Heiti valmyndaratriðis** sem þú vilt breyta og veldu gildið í dálknum **Kenni skrefs**. Síðan sem opnast sýnir allar tiltækar þýðingar fyrir titil og leiðbeiningu valins skrefs.
1. Fylgdu einu af þessum skrefum til að sérsníða textann fyrir hvaða tungumál sem er. Báðir valkostirnir gera þér kleift að breyta textum fyrir tungumál sem þegar eru til staðar. Aðeins fyrri valkosturinn gerir þér hins vegar kleift að bæta við textum fyrir ný tungumál, en aðeins seinni valkosturinn gerir þér kleift að skoða og breyta textum fyrir allar fyrirliggjandi hnekkingar á valmyndaratriði fyrir valið tungumál.

    - Á tækjastikunni skal velja **Bæta við** til að opna svarglugga þar sem þú getur bætt við eða breytt texta fyrir öll studd tungumál. Stilltu reitinn **Viðmiðunartungumál** á tungumálið sem þú vilt skoða gildin fyrir. Gildin eru sýnd í vinstri dálknum. Stilltu reitinn **Tungumál þýðingar** á tungumálið sem þú vilt bæta við eða sérsníða. Í hægri dálknum skaltu breyta gildunum í reitunum **Titill fyrir innslátt**, **Leiðbeining fyrir innslátt**, **Titill fyrir staðfestingu** og **Leiðbeiningu fyrir staðfestingu** eins og þú þarfnast. Veljið síðan **Í lagi**.
    - Í hnitanetinu skaltu finna og velja línuna þar sem reiturinn **Tungumál** er stilltur á tungumálið sem þú vilt breyta. Á tækjastikunni velurðu **Skoða &lt;tungumál&gt; þýðingu þessa skrefs** til að opna svarglugga þar sem þú getur breytt textum fyrir allar tiltækar hnekkingar fyrir valið tungumál. Svarglugginn inniheldur hnitanet sem er með línur fyrir bæði staðlaða texta (þar sem reiturinn **Heiti valmyndaratriðis** er auður) og fyrir hvern tiltækan texta hnekkingar (þar sem reiturinn **Heiti valmyndaratriðis** er stilltur á heiti valmyndaratriðis sem hnekkingin gildir fyrir). Breyttu gildunum í reitunum **Titill fyrir innslátt**, **Leiðbeining fyrir innslátt**, **Titill fyrir staðfestingu** og **Leiðbeiningu fyrir staðfestingu** eins og þú þarfnast. Veljið síðan **Í lagi**.

1. Haltu áfram að vinna þar til þú hefur skilgreint alla nauðsynlega titla og leiðbeiningar fyrir hvert tungumál.

## <a name="add-menu-specific-overrides"></a>Bæta við hnekkingum ákveðins valmyndaratriðis

Eins og minnst var á í fyrri hlutanum getur þú búið til hvað fjölda sem er af hnekkingum ákveðins valmyndaratriðis fyrir hvert skrefakenni. Þú gætir notað þennan möguleika til að breyta leiðbeiningunum svo að þær passi betur við staðbundna viðskiptaferla þína fyrir tiltekið valmyndaratriði. Fyrir sölutiltekt sem dæmi, ef fyrirtækið þitt gefur yfirleitt starfsmönnum verkkenni á prentuðu skjali, getur þú boðið upp á vísbendingu um að starfsmenni ættu að byrja á því að skanna verkkennið.

Hver hnekking á við um tiltekinn valmyndarlið fyrir fartæki og getur innihaldið fjölda þýðinga. Ef engin hnekking er til fyrir valmyndaratriði notar valmyndaratriðið staðlaða texta. Ef engin þýðing hnekkingar er skilgreind fyrir tungumál eru staðlaðir textar notaðir, jafnvel fyrir valmyndaratriði þar sem hnekking er skilgreind fyrir önnur tungumál.

Fylgdu þessum skrefum til að búa til og skilgreina hnekkingu.

1. Farðu í **Warehouse Management \> Uppsetning \> Fartæki \> Skref fartækis**.
1. Í hnitanetinu skal finna og velja línuna sem búa á til hnekkingu fyrir.
1. Á aðgerðasvæðinu skal velja **Bæta við skilgreiningu skrefs**.
1. Í felliglugganum **Bæta við skilgreiningu skrefs** skal stilla reitinn **Valmyndaratriði** á heiti valmyndaratriðis fartækis sem hnekkingin þín gildir um. Veljið síðan **Í lagi**.
1. Síðan sem birtist sýnir alla texta sem eru í boði fyrir nýju hnekkinguna. Í upphafi er bara eitt tungumál búið til. Öll önnur tungumál munu áfram nota staðlaða texta nema þú bætir þessum tungumálum við hér. Breyttu textunum og bættu við nýjum tungumálum eftir þörfum, eins og lýst er í fyrri hlutanum.
