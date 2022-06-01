---
title: Stofna Commerce-vörulista fyrir B2B-svæði
description: Þetta efnisatriði lýsir því hvernig á að búa til Commerce vörulista fyrir Microsoft Dynamics 365 Commerce fyrirtæki-til-fyrirtæki (B2B) síður.
author: ashishmsft
ms.date: 05/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: 7382062706c2de01c499ee05aeb0b45ff6fb37cb
ms.sourcegitcommit: bca0cb730307948368a9aabe322cf963688ed8b1
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/19/2022
ms.locfileid: "8782838"
---
# <a name="create-commerce-catalogs-for-b2b-sites"></a>Stofna Commerce-vörulista fyrir B2B-svæði

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Þetta efnisatriði lýsir því hvernig á að búa til Commerce vörulista fyrir Microsoft Dynamics 365 Commerce fyrirtæki-til-fyrirtæki (B2B) síður. Fyrir svör við algengum spurningum um verslunarskrár fyrir B2B síður, sjá [Viðskiptabækur fyrir B2B Algengar spurningar](catalogs-b2b-sites-FAQ.md).

> [!NOTE]
> Þetta efni á við um Dynamics 365 Commerce útgáfu 10.0.27 og síðari útgáfur.

Þú getur notað Commerce vörulista til að bera kennsl á vörurnar sem þú vilt bjóða í B2B netverslunum þínum. Þegar þú býrð til vörulista auðkennirðu netverslanir sem vörurnar eru boðnar í, bætir við vörunum sem þú vilt hafa með og bætir vöruframboðið með því að bæta við vöruupplýsingum. Þú getur búið til marga vörulista fyrir hverja B2B netverslun.

Viðskiptavörubæklingar gera þér kleift að skilgreina eftirfarandi upplýsingar:

- **Skipulagssértækt leiðsögustigveldi** – Stofnanir geta búið til sérstaka flokkaskipan fyrir tiltekna vörulista.
- **Lýsigögn eiginda tiltekinna vörulista** - Eiginleikar innihalda upplýsingar um vöru. Með því að úthluta eiginleikum til flokks leiðsögustigveldis er hægt að skilgreina gildi fyrir þá eiginleika á stigi vara sem eru úthlutaðar í þann flokk. Stofnanir geta síðan klárað þessi verkefni:

    - Skilgreindu vörulistasértæk eigindagildi.
    - Stjórna sýnileika eiginda á vörulistastigi.
    - Veldu hreinsunartæki sem eru sértæk fyrir einstaka vörulista.

- **Rásir** – Stofnanir geta tengt fleiri en eina B2B netrás við vörulista. Stuðningur frá enda til enda fyrir vörulista er sem stendur aðeins í boði fyrir B2B netverslanir.
- **Stigveldi viðskiptavina** – Fyrir tiltekna B2B rás geta stofnanir gert sérstakan vörulista aðgengilegan völdum B2B samstarfsaðilum með því að tengja stigveldi viðskiptavina við þann vörulista.
- **Verðflokkar** - Þú getur stillt verð og kynningar sem eru sértækar fyrir tiltekinn vörulista. Þessi hæfileiki er kjarnaástæða þess að skilgreina vörulista fyrir B2B rás. Verðflokkar fyrir vörulista gera stofnunum kleift að gera vörur aðgengilegar fyrir fyrirhugaðar B2B stofnanir og beita valinn verðlagningu og afslætti. B2B viðskiptavinir sem panta úr stilltum vörulista geta notið góðs af sérstökum verðum og kynningum eftir að þeir hafa skráð sig inn á Commerce B2B síðu. Til að stilla vörulistasértæk verð skaltu velja **Verðflokkar** á **Vörulistar** flipa til að tengja einn eða fleiri verðflokka við vörulistann. Allir viðskiptasamningar, verðleiðréttingarbækur og háþróaðir afslættir sem hafa verið tengdir við sama verðflokk verða notaðir þegar viðskiptavinir panta úr þeim vörulista. (Ítarlegir afslættir fela í sér þröskuld, magn og afslætti.) Fyrir frekari upplýsingar um verðflokka, sjá [Verðflokkar](price-management.md#price-groups).

> [!NOTE]
> Þessi eiginleiki er fáanlegur frá og með Dynamics 365 Commerce útgáfu 10.0.27 útgáfu. Til að stilla vörulistasértækar stillingar eins og leiðsögustigveldi og stigveldi viðskiptavina, í höfuðstöðvum Commerce, opnaðu **Eiginleikastjórnun** vinnusvæði (**Kerfisstjórnun \> Vinnurými \> Eiginleikastjórnun**), virkjaðu **Virkjaðu notkun margra vörulista á smásölurásum** lögun og keyrðu síðan **1110 CDX** starf.

## <a name="catalog-process-flow"></a>Skráarferlisflæði

Ferlið við að búa til og vinna vörulista hefur fjögur almenn skref. Hvert skref er útskýrt í smáatriðum í næsta kafla.

1. **[Skilgreining](#configure-the-catalog)**

    - Tengja leiðsögustigveldið.
    - Tilgreindu gildistíma og fyrningardagsetningar, ef þær eiga við.
    - Bættu við og flokkaðu vörur.
    - Tengja verðflokka.
    - Tengdu stigveldi viðskiptavina sem er sérstakt fyrir B2B stofnanir þínar. 
    - Tengja sjálfgefna víddareigindahóp fyrir hreinsunarefni eins og stærð, stíl og lit.
    - Stilltu lýsigögn eiginda.

1. **[Staðfesting](#validate-the-catalog)** - Í þessu skrefi keyrir þú löggildingarreglur sem framfylgja sérstakri hegðun. Hér eru nokkur dæmi:

    - Gakktu úr skugga um að það séu engar óflokkaðar vörur.
    - Gakktu úr skugga um að allir hlutir sem eru flokkaðir á hverja rás séu tengdir vörulista.

1. **[Samþykki](#approve-the-catalog)**
1. **[Birting](#publish-the-catalog)**

## <a name="set-up-the-catalog"></a>Settu upp vörulistann

Notaðu upplýsingarnar í þessum hluta til að setja upp vörulistann þinn.

### <a name="configure-the-catalog"></a>Stilltu vörulistann

Í höfuðstöðvum viðskipta, farðu til **Verslun og verslun \> Vörulistar og úrval \> Allir vörulistar** til að stilla vörulistann þinn.

Þegar þú býrð til nýjan vörulista verður þú fyrst að tengja hann við eina eða fleiri rásir. Aðeins hlutir sem eru tengdir við valda rás [úrval](/dynamics365/unified-operations/retail/assortments) hægt að nota þegar vörulistinn er búinn til. Til að tengja vörulistann við eina eða fleiri rásir velurðu **Bæta við** á **Viðskiptarásir** Flýtiflipi á **Uppsetning vörulista** síðu.

#### <a name="associate-the-navigation-hierarchy"></a>Tengja leiðsögustigveldið

Til að bæta vörum við vörulista verður þú að velja leiðsagnarstigveldi. Leiðsögustigveldið styður flokkaskipan vörulistans. Þú verður að velja eitt af leiðsögustigveldunum sem tengjast rásunum sem þú valdir á **Viðskiptarásir** Flýtiflipi á **Uppsetning vörulista** síðu. Til að tengja sjálfgefið leiðsagnarstigveldi við hverja rás þína skaltu fara á **Verslun og verslun \> Rásaruppsetning \> Rásarflokkar og vörueiginleikar**.

#### <a name="specify-time-effective-and-expiration-dates"></a>Tilgreindu gildistíma og gildistíma

Til að tilgreina gildistíma og fyrningardagsetningar fyrir vörulista skaltu velja efsta hnút vörulistastigveldisins til að fara aftur í aðalyfirlit vörulista. Síðan, á **Almennt** Flýtiflipa, stilltu gildis- og fyrningardagsetningar eftir þörfum.

#### <a name="add-and-categorize-products"></a>Bættu við og flokkaðu vörur

Til að stilla vörur til að bæta við vörulista, í höfuðstöðvum Commerce, farðu á **Verslun og verslun \> Vörulistar og úrval \> Allir vörulistar**. Síðan, á **Vörulistar** flipa, veldu **Bæta við vörum**.

Að öðrum kosti skaltu velja hnút í leiðsögustigveldinu. Þú munt þá geta bætt vörum beint við flokk í vörulistanum.

#### <a name="associate-price-groups"></a>Tengja verðflokka

Til að stilla vörulistasértæk verð verður að tengja einn eða fleiri verðflokka við vörulistann. Til að tengja verðflokka við vörulista, í höfuðstöðvum Commerce, farðu á **Verslun og verslun \> Vörulistar og úrval \> Allir vörulistar**. Síðan, á **Vörulistar** flipi, undir **Verðlag**, veldu **Verðflokkar**. Allir viðskiptasamningar, verðleiðréttingarbækur og háþróaðir afslættir (þröskuldur, magn og samsetningarafsláttur) sem hafa verið tengdir við sama verðflokk verða notaðir þegar viðskiptavinir panta úr vörulista.

Fyrir frekari upplýsingar um verðflokka, sjá [Verðflokkar](price-management.md#price-groups).

> [!NOTE]
> Þú getur ekki búið til nýjan verðflokk úr **Allir vörulistar** síðu. Þess í stað verður þú að búa það til úr **Allir verðflokkar** síðu. Þú verður þá að tengja það við vörulistann á **Allir vörulistar** síðu.

#### <a name="associate-a-customer-hierarchy"></a>Tengja stigveldi viðskiptavina

Til að tengja stigveldi viðskiptavina, í höfuðstöðvum Commerce, farðu á **Verslun og verslun \> Vörulistar og úrval \> Allir vörulistar**. Síðan, á **Vörulistar** flipi, undir **Stigveldi viðskiptavina**, veldu **Úthluta stigveldum** til að tengja eitt eða fleiri stigveldi viðskiptavina við vörulistann.

> [!NOTE]
> Þú getur ekki búið til nýtt stigveldi viðskiptavina úr **Allir vörulistar** síðu. Þess í stað verður þú að búa það til úr **Stigveldi viðskiptavina** síðu. Þú verður þá að tengja það við vörulistann á **Allir vörulistar** síðu.

#### <a name="associate-default-dimension-attribute-group-for-refiners-such-as-size-style-and-color"></a>Tengja sjálfgefna víddareigindahóp fyrir hreinsunarefni eins og stærð, stíl og lit

Til að tengja sjálfgefna víddareigindahóp fyrir hreinsunartæki eins og stærð, stíl og lit, í höfuðstöðvum Commerce, farðu á **Verslun og verslun \> Vörulistar og úrval \> Allir vörulistar**. Síðan, á **Vörulistar** flipi, undir **Eiginleikar**, veldu **Eiginleikahópar**.

#### <a name="set-attribute-metadata"></a>Stilla eigind lýsigagna

Til að stilla lýsigögn eiginda, í höfuðstöðvum Commerce, farðu á **Verslun og verslun \> Vörulistar og úrval \> Allir vörulistar**. Síðan, á **Vörulistar** flipi, undir **Eiginleikar**, veldu **Stilltu lýsigögn eiginda**. Til að velja eiginleikana sem ættu að vera sýnilegir og fínstillanlegir skaltu velja flokk í tilheyrandi vörulistasértæku leiðsögustigveldi og síðan, undir **Skrá vörueiginleika**, veldu eigind. Veldu síðan **Sýna eigind á rás**. Sjálfgefið er að allir sýnilegir eiginleikar eru einnig leitartækir. Veldu **Hægt að betrumbæta**.

### <a name="validate-the-catalog"></a>Staðfesta vörulistann

Áður en nýr vörulisti er tiltækur til notkunar verður hann að vera staðfestur og birtur.

Fylgið eftirfarandi skrefum til að villuleita í vörulista.

1. Á **Vörulistar** flipi á **Allir vörulistar** síða, undir **Staðfesta** velja **Staðfesta vörulista** að keyra löggildingu. Þetta skref er nauðsynlegt. Það mun sannreyna að nauðsynleg uppsetning sé nákvæm.
1. Veldu **Skoða niðurstöður** til að skoða upplýsingar um löggildinguna. Ef villur finnast verður þú að leiðrétta gögnin og keyra síðan löggildinguna aftur þar til hún stenst.

### <a name="approve-the-catalog"></a>Samþykkja vörulistann

Eftir að vörulisti hefur verið staðfestur verður hann að vera samþykktur.

Til að hefja verkflæði vörulistasamþykktar skaltu fylgja þessum skrefum.

1. Á aðgerðaglugganum á **Allir vörulistar** síðu, veldu **Verkflæði \> Sendu inn**.
1. Fara til **Verslun og verslun \> Uppsetning höfuðstöðva \> Verkflæði viðskipta** til að stilla skrefin og viðurkennda notendur fyrir verkflæðið. Verkflæðið mun skilgreina skrefin sem þarf til að koma vörulistanum í **Samþykkt** stöðu.

### <a name="publish-the-catalog"></a>Birta vörulistann

Eftir að vörulisti er í an **Samþykkt** stöðu, þú getur birt hana með því að velja **Birta** á **Vörulistar** matseðill. Eftir að vörulistinn er í a **Birt** ástand, það er hægt að nota í símaver pantanafærslu og senda vörulista. Þú getur gefið út vörulista annað hvort handvirkt eða með því að nota lotuferli. Gildistíminn sem þú tilgreindir fyrir vörulistann ákvarðar hvenær vörurnar eru fáanlegar í netversluninni. Fyrningardagsetningin sem þú skilgreindir ákvarðar hvenær vörurnar eru fjarlægðar úr netversluninni.

> [!NOTE]
> Hægt er að gefa út vörulista sem inniheldur vörur sem hafa viðvaranir. Hins vegar munu þessar vörur ekki birtast í netversluninni.

## <a name="additional-resources"></a>Frekari upplýsingar

[Stækkunarhæfniáhrif Commerce-vörulista fyrir B2B-sérstillingar](catalogs-b2b-sites-dev.md)

[Algengar spurningar um Commerce-vörulista fyrir B2B](catalogs-b2b-sites-FAQ.md)
