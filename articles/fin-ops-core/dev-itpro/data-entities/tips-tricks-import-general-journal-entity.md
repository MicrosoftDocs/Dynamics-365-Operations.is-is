---
title: Innflutningur fylgiskjala með því að nota einingu almennrar færslubókar
description: Þetta efnisatriði veitir ábendingar fyrir innflutning gagna í Almenna færslubók með því að nota einingu almennrar færslubókar.
author: rcarlson
manager: AnnBe
ms.date: 04/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 94363
ms.assetid: 0b8149b5-32c5-4518-9ebd-09c9fd7f4cfc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: adc5ad88b7b58c67154b340f4125b0b89a0cf4d6
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5566898"
---
# <a name="importing-vouchers-by-using-the-general-journal-entity"></a>Innflutningur fylgiskjala með því að nota einingu almennrar færslubókar

[!include [banner](../includes/banner.md)]

Þetta efnisatriði veitir ábendingar fyrir innflutning gagna í Almenna færslubók með því að nota einingu almennrar færslubókar.

Hægt er að nota eininguna Almenna færslubók til að flytja einungis inn fylgiskjöl sem hafa reikningsgerðina **Fjárhag**, **Viðskiptavin**, **Lánardrottinn** eða **Banka**. Fylgiskjal er hægt að færa inn sem eina lína með því að nota bæði svæðið **Lykill** og **Mótlykill**, eða í margra línu fylgiskjali, þar sem aðeins svæðið **Lykill** er notað (og **Mótlykill** er haft autt í hverri línu). Einingin Almenn færslubók styður ekki allar gerð lykils. Þess í stað eru til aðrar einingar fyrir aðstæður ar sem mismunandi samsetningar gerða lykla er krafist. Til dæmis til að flytja inn verkfærslu, skal nota verkeiningu kostnaðarskýrslu færslubókar. Hver eining er hönnuð til að styðja við tilteknar atburðarásir. Þetta þýðir að fleiri reitir geta verið tiltækir í einingum fyrir þessar atburðarásir. Hins vegar gætu viðbótarreitir ekki verið í boði í einingum fyrir mismunandi atburðarásir.

## <a name="setup"></a>Setja upp
Áður en flutt er inn með því að nota einingu almennrar færslubókar, skal staðfesta eftirfarandi uppsetningu:

- **Uppsetningu númeraraða fyrir rununúmer færslubókar** – að Sjálfgefnu þegar flutt er inn með einingu Almennrar færslubókar, nota rununúmer færslubókar númeraröðina sem er skilgreind í færibreytum fjárhags. Ef þú stillir númeraröð fyrir rununúmer færslubókar í **Handvirkt**, er sjálfgefinn númer ekki notuð. Þessi uppsetning er ekki studd.
- **Fjárhagsvíddarskilgreining** – Hvert fyrirtæki verður að skilgreina röð fjárhagsvídda þegar einingarnar eru notaðar til að flytja inn færslur. Pöntunin er skilgreind fyrir sniðið **samþættingu fjárhagsvídda**, í **Fjárhag** &gt; **Bókhaldslykil** &gt; **Víddir** &gt; **Fjárhagsvíddarskilgreining fyrir samþættingu forrita** &gt; **Velja gagnaeiningar**. Hlutar fjárhagslykilsins sem er flutt inn verður að hafa sömu röð. Annars mun villa eiga sér stað við innflutning.

## <a name="general-journal-entity-setup"></a>Uppsetningar einingar almennrar færslubókar
Tvær stillingar í gagnastjórnun hafa áhrif á hvernig sjálfgefið rununúmer færslubókar eða númer fylgiskjals eru notuð:

- **Samstæðubyggð úrvinnsla** (á gagnaeiningu)
- **Sjálfmynduð** (á reitavörpun)

Eftirfarandi hlutar lýsa áhrifum þessara stillinga. Þeir útskýra einnig hvernig kerfið býr til rununúmer fyrir færslubækur og fylgiskjalsnúmer.

### <a name="journal-batch-number"></a>Rununúmer færslubókar

- Í **samstæðubyggð úrvinnsla** stilling á einingu Almennrar færslubókar hefur ekki áhrif á hvernig rununúmer færslubókar eru myndaðar.
- Ef **rununúmer Færslubókar** er stillt á **sjálfmynduð**, er stifbap nýtt rununúmer færslubókar fyrir hverja línu sem er flutt inn. Þessi hegðun er ekki ráðleg. **sjálfmynduð** stilling finnst í innflutningi verks, undir **skoða kort** á í **Vörpunarupplýsingar** flipa.
- Ef **rununúmer Færslubókar** er ekki stillt á **sjálfmynduð**, er rununúmer færslubókar stofnuð á eftirfarandi hátt.

    - Ef rununúmer færslubókar sem er skilgreint í innfluttu skránni passar við fyrirliggjandi, óbókaða færslubók eru allar línur sem hafa samsvarandi rununúmer færslubókar flutt inn í fyrirliggjandi færslubók. Línur eru aldrei fluttar inn í rununúmer bókaðrar færslubókar. Þess í stað nýtt númer er stofnað.
    - Ef rununúmer færslubókar sem er skilgreint í innfluttu skránni passar ekki við fyrirliggjandi, óbókaða færslubók eru allar línur sem hafa sama rununúmer færslubókar flokkaðar undir nýrri færslubók. Til dæmis, allar línur sem hafa rununúmer færslubókar 1 eru flutt inn í nýja færslubók og allar línur sem hafa rununúmer færslubókar 2 eru flutt inn í seinni nýja færslubók. Rununúmer færslubókar er stofnuð með því að nota númeraröð sem skilgreind er í færibreytum fjárhags.

### <a name="voucher-number"></a>Fylgiskjalsnúmer

- Þegar notuð er **samstæðubyggð úrvinnsla** stilling á einingu Almennri færslubók, verður að gefa upp númer fylgiskjals í innfluttu skránni. Hver færsla í Almennu færslubókinni er úthlutað fylgiskjalsnúmer sem er gefin upp í innfluttu skránni, jafnvel ef fylgiskjal er ekki jafnað. Athugaðu eftirfarandi punkta ef óskað er eftir því að nota samstæðubyggða úrvinnslu en þú vilt einnig nota númeraröð sem skilgreind er fyrir fylgiskjalsnúmer.

    - Til að virkja þessa aðgerð, á færslubókarheiti sem notað er fyrir innflutningi skal stilla **úthlutun númers við bókun** á **Já**.
    - Samt sem áður þarf að skilgreina númer fylgiskjals í innfluttu skránni. Hins vegar er þetta númer tímabundið og mun fylgiskjalsnúmer skrifa yfir það þegar færslubókin er bókuð. Gakktu úr skugga um að línurnar í færslubókinni eru rétt flokkaðar eftir tímabundið fylgiskjalsnúmer. Til dæmis, við bókun, finnast þrjár línur sem hafa tímabundið fylgiskjalsnúmer 1. Tímabundið fylgiskjalsnúmer fyrir allar þrjár línur er skrifað yfir af næsta númeri í númeraröð. Ef þessar þrjár línur ekki eru jöfnuð færsla er fylgiskjal ekki bókað. Næst, ef línur finnast sem hafa tímabundið fylgiskjalsnúmer 2, er þetta númer yfirskrifað af næsta númer fylgiskjals í röð, og svo framvegis.

- Þegar ekki er notuð stillingin **samstæðubyggð úrvinnsla** þarf ekki að gefa upp neitt númer fylgiskjals í innfluttu skránni. Fylgiskjalsnúmer eru stofnaðar við innflutning, byggt á uppsetningu færslubókarheitis (**Eitt fylgiskjal einungis**, **í samhengi við jöfnun** og svo framvegis). Til dæmis, ef færslubókarheiti er skilgreint sem **í samhengi við jöfnun**, fær fyrsta lína nýtt sjálfgefið fylgiskjalsnúmer. Kerfið metur síðan línu til að ákvarða hvort debet er jafn mikið og kredit. Ef mótlykill er til staðar í línunni, fær næstu línu sem flutt er inn nýtt fylgiskjalsnúmer. Ef enginn mótlykill er til staðar, metur kerfið hvort debet er jafn mikið og kredit um leið og hver ný lína er innflutt.
- Ef í **Fylgiskjalsnúmer** reitur er stillt á **sjálfmynduð**, tekst innflutningurinn ekki. **sjálfmynduð** stilling fyrir reitinn **Fylgiskjalsnúmer** er ekki studd.

Sjálfgefið er að Eining Almennrar færslubókar noti samstæðubyggð úrvinnsla. Eftir að þú metur viðskiptaþarfir í þínu fyrirtæki, er hægt að breyta **samstæðubyggð úrvinnsla** stillingu með því að smella á **gagnaeiningar** í á **gagnastjórnun** vinnusvæði. Samstæðubyggð úrvinnsla er notuð til að flýta innflutningsferlinu. Ef þú notar ekki samstæðubyggð úrvinnsla, verður innflutningur einingar Almennrar færslubókar hægvirkari.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]