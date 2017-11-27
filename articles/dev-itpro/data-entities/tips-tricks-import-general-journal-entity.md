---
title: "Bestu starfsvenjur til að flytja inn fylgiskjöl með því að nota einingu Almennrar færslubókar"
description: "Þetta efnisatriði veitir ábendingar fyrir innflutning gagna í Almenna færslubók með því að nota einingu almennrar færslubókar."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 94363
ms.assetid: 0b8149b5-32c5-4518-9ebd-09c9fd7f4cfc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 688fa17072cb340d6d02be31528339fb98601825
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="best-practices-for-importing-vouchers-using-the-general-journal-entity"></a>Bestu starfsvenjur til að flytja inn fylgiskjöl með því að nota einingu Almennrar færslubókar

[!include[banner](../includes/banner.md)]


Þetta efnisatriði veitir ábendingar fyrir innflutning gagna í Almenna færslubók með því að nota einingu almennrar færslubókar.  

Hægt er að nota eininguna Almenna færslubók til að flytja einungis inn fylgiskjöl sem hafa reikningsgerðina **Fjárhag, Viðskiptavin, Lánardrottin eða Banka**. Fylgiskjal er hægt að færa inn sem eina lína með því að nota bæði svæðið **Lykill** og **Mótlykill**, eða í margra línu fylgiskjali, þar sem aðeins svæðið **Lykill** er notað (og **Mótlykill** er haft autt í hverri línu). Einingin Almenn færslubók styður ekki allar gerð lykils. Þess í stað eru til aðrar einingar fyrir aðstæður ar sem mismunandi samsetningar gerða lykla er krafist. Til dæmis til að flytja inn verkfærslu, skal nota verkeiningu kostnaðarskýrslu færslubókar. Hver eining er hönnuð til að styðja við tilteknar aðstæður sem þýðir að viðbótarreitir gætu verið í einingum fyrir þær aðstæður en ekki í einingum fyrir mismunandi aðstæður.

## <a name="setup"></a>Uppsetning
Áður en flutt er inn með því að nota einingu almennrar færslubókar, skal staðfesta eftirfarandi uppsetningu:

-   **Uppsetningu númeraraða fyrir rununúmer færslubókar** – að Sjálfgefnu þegar flutt er inn með einingu Almennrar færslubókar, nota rununúmer færslubókar númeraröðina sem er skilgreind í færibreytum fjárhags. Ef þú stillir númeraröð fyrir rununúmer færslubókar í **Handvirkt**, er sjálfgefinn númer ekki notuð. Þessi uppsetning er ekki studd.
-   **Fjárhagsvíddarskilgreining** – Hvert fyrirtæki verður að skilgreina röð fjárhagsvídda þegar einingarnar eru notaðar til að flytja inn færslur. Pöntunin er skilgreind fyrir sniðið **samþættingu fjárhagsvídda**, í **Fjárhag** &gt; **Bókhaldslykil** &gt; **Víddir** &gt; **Fjárhagsvíddarskilgreining fyrir samþættingu forrita** &gt; **Velja gagnaeiningar**. Hlutar fjárhagslykilsins sem er flutt inn verður að hafa sömu röð. Annars mun villa eiga sér stað við innflutning.

## <a name="general-journal-entity-setup"></a>Uppsetningar einingar almennrar færslubókar
Tvær stillingar í gagnastjórnun hafa áhrif á hvernig sjálfgefið rununúmer færslubókar eða númer fylgiskjals eru notuð:

-   **Samstæðubyggð úrvinnsla** (á gagnaeiningu)
-   **Sjálfmynduð** (á reitavörpun)

Eftirfarandi kaflar lýsa áhrif þessara stillinga og einnig útskýrir hvernig rununúmer færslubókar og fylgiskjalsnúmer eru myndaðar.

### <a name="journal-batch-number"></a>Rununúmer færslubókar

-   Í **samstæðubyggð úrvinnsla** stilling á einingu Almennrar færslubókar hefur ekki áhrif á hvernig rununúmer færslubókar eru myndaðar.
-   Ef **rununúmer Færslubókar** er stillt á **sjálfmynduð**, er stifbap nýtt rununúmer færslubókar fyrir hverja línu sem er flutt inn. Þessi hegðun er ekki ráðleg. **sjálfmynduð** stilling finnst í innflutningi verks, undir **skoða kort** á í **Vörpunarupplýsingar** flipa.
-   Ef **rununúmer Færslubókar** er ekki stillt á **sjálfmynduð**, er rununúmer færslubókar stofnuð á eftirfarandi hátt.
    -   Ef rununúmer færslubókar sem er skilgreint í innfluttu skránni passar við fyrirliggjandi, óbókaða færslubók eru allar línur sem hafa samsvarandi rununúmer færslubókar flutt inn í fyrirliggjandi færslubók. Línur eru aldrei fluttar inn í rununúmer bókaðrar færslubókar. Þess í stað nýtt númer er stofnað.
    -   Ef rununúmer færslubókar sem er skilgreint í innfluttu skránni passar ekki við fyrirliggjandi, óbókaða færslubók eru allar línur sem hafa sama rununúmer færslubókar flokkaðar undir nýrri færslubók. Til dæmis, allar línur sem hafa rununúmer færslubókar 1 eru flutt inn í nýja færslubók og allar línur sem hafa rununúmer færslubókar 2 eru flutt inn í seinni nýja færslubók. Rununúmer færslubókar er stofnuð með því að nota númeraröð sem skilgreind er í færibreytum fjárhags.

### <a name="voucher-number"></a>Fylgiskjalsnúmer

-   Þegar notuð er **samstæðubyggð úrvinnsla** stilling á einingu Almennri færslubók, verður að gefa upp númer fylgiskjals í innfluttu skránni. Hver færsla í Almennu færslubókinni er úthlutað fylgiskjalsnúmer sem er gefin upp í innfluttu skránni, jafnvel ef fylgiskjal er ekki jafnað. Ef óskað er að nota samstæðubyggða úrvinnslu en þú vilt einnig nota númeraröð sem skilgreind er fyrir fylgiskjalsnúmer hefur verið búin til bráðabót sem fyrir febrúar 2016 útgáfa. Númer bráðabótar er 3170316 og og má hlaða niður frá Lifecycle services (LCS). Nánari upplýsingar, sjá [Niðurhal bráðabóta af Lifecycle Services](..\migration-upgrade\download-hotfix-lcs.md).
    -   Til að virkja þessa aðgerð, á færslubókarheiti sem notað er fyrir innflutningi skal stilla  **úthlutun númers við bókun** á **Já**.
    -   Samt sem áður þarf að skilgreina númer fylgiskjals í innfluttu skránni. Hins vegar er þetta númer tímabundin og skrifað er yfir það af fylgiskjalsnúmer þegar færslubókin er bókuð. Þú verður að ganga úr skugga um að línurnar í færslubókinni eru rétt flokkaðar eftir tímabundið fylgiskjalsnúmer. Til dæmis, við bókun, finnast þrjár línur sem hafa tímabundið fylgiskjalsnúmer 1. Tímabundið fylgiskjalsnúmer fyrir allar þrjár línur er skrifað yfir af næsta númeri í númeraröð. Ef þessar þrjár línur ekki eru jafnaðar færslur, er fylgiskjal ekki bókuð. Næst, ef línur finnast sem hafa tímabundið fylgiskjalsnúmer 2, er þetta númer yfirskrifað af næsta númer fylgiskjals í númeraröð, og svo framvegis.

<!-- -->

-   Þegar ekki er notuð stillingin **samstæðubyggð úrvinnsla** þarf ekki að gefa upp neitt númer fylgiskjals í innfluttu skránni. Fylgiskjalsnúmer eru stofnaðar við innflutning, byggt á uppsetningu færslubókarheitis (**Eitt fylgiskjal einungis**, **í samhengi við jöfnun** og svo framvegis). Til dæmis, ef færslubókarheiti er skilgreint sem **í samhengi við jöfnun**, fær fyrsta lína nýtt sjálfgefið fylgiskjalsnúmer. Kerfið metur síðan línu til að ákvarða hvort debet er jafn mikið og kredit. Ef mótlykill er til staðar í línunni, fær næstu línu sem flutt er inn nýtt fylgiskjalsnúmer. Ef enginn mótlykill er til staðar, metur kerfið hvort debet er jafn mikið og kredit um leið og hver ný lína er innflutt.
-   Ef í **Fylgiskjalsnúmer** reitur er stillt á **sjálfmynduð**, tekst innflutningurinn ekki. **sjálfmynduð** stilling fyrir reitinn **Fylgiskjalsnúmer** er ekki studd.

Sjálfgefið er að Eining Almennrar færslubókar noti samstæðubyggð úrvinnsla. Eftir að þú metur viðskiptaþarfir í þínu fyrirtæki, er hægt að breyta **samstæðubyggð úrvinnsla** stillingu með því að smella á **gagnaeiningar** í á **gagnastjórnun** vinnusvæði. Samstæðubyggð úrvinnsla er notuð til að flýta innflutningsferlinu. Ef þú notar ekki samstæðubyggð úrvinnsla, verður innflutningur einingar Almennrar færslubókar hægvirkari.




