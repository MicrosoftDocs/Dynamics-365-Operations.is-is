---
title: Kveikja á og grunnstilla sjálfvirk gjöld eftir rás
description: Þetta efni útskýrir hvernig á að virkja og stilla sjálfvirkt gjald eftir rás í Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: 1be07c754e563298d82f6ca54f09ae3aa9118602
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413137"
---
# <a name="enable-and-configure-auto-charges-by-channel"></a>Kveikja á og grunnstilla sjálfvirk gjöld eftir rás

Þetta efni útskýrir hvernig á að virkja og stilla sjálfvirk gjöld (sjálfvirk gjöld) eftir rás í Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Þú gætir haft atburðarás þar sem nota þarf endurvinnslugjöld eða önnur gjöld fyrir hóp af vörum sem eru seldar í öllum eða sumum verslunum í tilteknu ríki (til dæmis í Kaliforníu). Eiginleikinn **Kveikja á síun sjálfvirkra gjalda eftir rás** í Commerce gerir þér kleift að tilgreina sjálfvirka gjaldtöku eftir rás (til dæmis ákveðin verslunarrás). Þessi eiginleiki er tiltækur í Dynamics 365 Commerce útgáfa 10.0.10 og síðar.

Til að virkja og stilla sjálfvirkt gjald eftir rás verður þú að klára eftirfarandi verkefni:

- Kveiktu á eiginleikanum **Kveikja á síun sjálfvirkra gjalda eftir rás**.
- Grunnstilltu tilgang fyrir stigveldi fyrirtækis.
- Skilgreina sjálfvirkt gjald eftir rás.

> [!NOTE]
> Eiginleikinn **Kveikja á síun sjálfvirkra gjalda eftir rás** virkar aðeins ef einnig er kveikt á ítarlegum sjálfvirkum gjaldaeiginleikanum. Nánari upplýsingar um hvernig á að kveikja á háþróaðri sjálfvirkri gjaldtöku er að finna í [Ítarleg sjálfvirk gjöld fyrir omni-rás](omni-auto-charges.md).

## <a name="turn-on-the-enable-filter-auto-charges-by-channel-feature"></a>Kveiktu á eiginleikanum Kveikja á síun sjálfvirkra gjalda eftir rás

Fylgdu þessum skrefum til að virkja sjálfvirka gjaldtöku eftir rás í Commerce.

1. Farðu í **Kerfisstjóri \> Vinnusvæði \> Eiginleikastjórnun**.
1. Á flipanum **Ekki gert virkt**, á listanum **Heiti eiginleika**, finnurðu og velur **Kveikja á síun sjálfvirkra gjalda eftir rás**.
1. Neðst í hægra horninu velurðu **Virkja núna**. Þegar kveikt hefur verið á eiginleikanum birtist hann á listanum á flipanum **Allt**.
1. Farðu í **Retail og Commerce \> Upplýsingatækni í Retail og Commerce \> Dreifingaráætlun**.
1. Í vinstri glugganum finnurðu og velur vinnsluna **1110** (**Altækar stillingar**).
1. Í aðgerðaglugganum velurðu **Keyra núna** til að breiða út stillingarbreytingarnar.

> [!WARNING]
> Ef þú slekkur á eiginleikanum **Kveikja á síun sjálfvirkra gjalda eftir rás** þegar þú hefur þegar notað hann birtist reiturinn **Tengsl smásölurásar** undir **Sjálfvirk gjöld** ekki lengur og þú tapar öllum núverandi stillingum. Ef fjarlæging á stillingum **Tengsla smásölurásar** valda tvíritun á reglum um sjálfvirkt gjald mun tilraun til að slökkva á eiginleikanum ekki takast. Passaðu að fara yfir allar reglur um gjöld fyrir sjálfvirk gjöld og gera nauðsynlegar breytingar áður en slökkt er á eiginleikanum.

## <a name="configure-the-organization-hierarchy-purpose"></a>Grunnstilltu tilgang fyrir stigveldi fyrirtækis

Nýr tilgangur stigveldisskipulags sem nefndur er **Sjálfvirkt gjald í Retail** hefur verið stofnað til að stjórna stigveldinu fyrir sjálfvirka gjaldtöku eftir rás.

Fylgdu þessum skrefum til að tengja sjálfgefið stigveldi við skipulag stigveldis í Commerce.
        
1. Farðu í **Fyrirtækisstjórnun \> Fyrirtæki \> Tilgangur stigveldis fyrirtækis**.
1. Veldu á vinstri glugganum **Sjálfvirkt gjald í Retail**.
1. Undir **Úthlutuð stigveldi** velurðu **Bæta við**.
1. Í valmyndinni **Stigveldi fyrirtækis** velurðu stigveldi fyrirtækis (til dæmis, **Smásöluverslnair eftir svæðum**) og veldu síðan **Í lagi**.
1. Undir **Úthlutuð stigveldi** velurðu **Setja sem sjálfgildi**.
1. Farðu í **Retail og Commerce \> Upplýsingatækni í Retail og Commerce \> Dreifingaráætlun**.
1. Í vinstri glugganum finnurðu og velur vinnsluna **1040** (**Afurðir**).
1. Í aðgerðarúðunni velurðu **Keyra núna**.
1. Endurtaktu tvö síðustu skref til að keyra vinnslurnar **1070** (**Stilling rásar**) og **1110** (**Altækar stillingar**).

![Stillingar tilgangs gjalda stigveldis fyrirtækis í Retail](media/Auto-charges-org-hierarchy-purpose.png)

## <a name="define-auto-charges-by-channel"></a>Skilgreina sjálfvirkt gjald eftir rás

Þegar þú hefur kveikt á eiginleikanum **Kveikja á síun sjálfvirkra gjalda eftir rás** og stillt tilgang fyrirtækjastigveldis **Sjálfvirkt gjald í Retail** er hægt að skilgreina sjálfvirk gjöld eftir rás á annaðhvort hausstigi raðar eða línustigi raðar.

Fylgdu þessum skrefum til að skilgreina sjálfvirka gjaldtöku eftir rás í Commerce.

1. Farðu í **Viðskiptakröfur \> Uppsetning gjalda \> Sjálfvirk gjöld**.
1. Í vinstri glugganum, í reitnum **Stig**, velurðu annaðhvort **Haus** eða **Lína**, eftir því hverjar viðskiptakröfur þínar eru.
1. Í reitnum **Númer smásölurásar** velurðu viðeigandi rásakóða (til dæmis, **Tafla** eða **Hópur**). Ef sjálfgefin stilling, **Allt**, er notuð eru gjaldareglur notaðar á allar rásir.

    - Ef þú velur **Hópur** skaltu passa að gjaldtökuhópur smásölurásar sé stofnaður í **Retail og Commerce \> Uppsetning rásar \> Gjöld \> Gjaldhópar smásölurásar**.
    - Ef þú velur **Tafla** geturðu valið ákveðna rás (til dæmis, **San Fransiskó**) í reitnum **Tengsl smásölurásar**.

1. Farðu í **Retail og Commerce \> Upplýsingatækni í Retail og Commerce \> Dreifingaráætlun**.
1. Í vinstri glugganum finnurðu og velur vinnsluna **1040** (**Afurðir**).
1. Í aðgerðarúðunni velurðu **Keyra núna**.
1. Endurtaktu tvö síðustu skref til að keyra vinnslurnar **1070** (**Stilling rásar**) og **1110** (**Altækar stillingar**).
    
![Sjálfvirk gjöld skilgreind eftir rás](media/Auto-charges-line-charge-by-channel.png)

## <a name="example-scenario"></a>Dæmi

Eftirfarandi dæmi sýnir skrefin sem þarf til að stilla vöru þannig að endurvinnslugjöld eru innheimt þegar varan er seld á verslunarrás í San Francisco. Dæmið sýnir einnig hvernig sjálfvirka gjaldið birtist í POS-forritinu í Commerce.

Fyrirtækið skilgreinir gjaldakóða sem nefndur er **ENDURVINNA** eins og sýnt er á eftirfarandi mynd.

![Gjaldakóðinn ENDURVINNA](media/Auto-charges-charge-code.png)

Sjálfvirkt gjald er stofnað á línustiginu. Það hefur eftirfarandi stillingu:

- Reiturinn **Kóði lykils** er stilltur á **Allt**.
- Reiturinn **Kóði vöru** er stilltur á **Tafla**.
- Reiturinn **Vöruvensl** er stilltur á afurðakennið **91001**.
- Reiturinn **Kóði afhendingarmáta** er stilltur á **Allt**.
- Reiturinn **Kóði smásölurásar** er stilltur á **Tafla**.
- Reiturinn **Tengsl smásölurásar** er stilltur á verslunina í **San Fransiskó**.

Sjálfvirk gjaldalína er stofnuð. Það hefur eftirfarandi stillingu:

- Reiturinn **Gjaldmiðill** er stilltur **USD**.
- Reiturinn **Kóði gjalda** er stilltur á **ENDURVINNA**.
- Reiturinn **Flokkur** er stilltur **Fast**.
- Reiturinn **Gjöld** er stilltur á **$6,25**.

![Stillingar sjálfvirku gjaldalínunnar og sjálfvirku gjaldalínunnar](media/Auto-charges-recyclingfee-line-fee.png)

Í POS-forritinu er sölupöntun stofnuð í verslunarrásinni í **San Fransiskó**. Línan **Gjöld** sýnir endurvinnslugjald upp á **$6,25**.

Með því að velja **Færslukosti \> Gjöld \> Stjórna gjöldum** í POS-forritinu geturðu skoðað gjaldakóðann og lýsingu fyrir endurvinnslugjaldið.

![Endurvinnslugjald í POS-forritinu](media/pos-auto-charges-recyclingfee-line-fee.png)

## <a name="additional-resources"></a>Frekari upplýsingar

[Ítarleg sjálfvirk gjöld fyrir omni-rás](omni-auto-charges.md)

[Skipta gjöldum í haus í hlutfalli við samsvarandi sölulínur](pro-rate-charges-matching-lines.md)
