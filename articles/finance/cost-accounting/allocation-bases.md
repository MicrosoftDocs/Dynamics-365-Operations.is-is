---
title: Úthlutunargrunnar
description: Í þessu efnisatriði er að finna upplýsingar um úthlutunargrunna. Úthlutunargrunnar eru lykilþættir í kostnaðarbókhaldi og eru að mestu notaðir til að úthluta rekstrarkostnaði.
author: AndersGirke
ms.date: 05/24/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimensionMember, CAMAllocationBaseDetail, CAMFormulaAllocationBaseDetail, CAMAllocationBasePreview, CAMAllocationBase, CAMCostAllocationRule, CAMPredefinedMemberAllocationBase
audience: Application User
ms.reviewer: roschlom
ms.custom: 223174
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 15155a987094da6047dea9245f543b5ed38e3680
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814057"
---
# <a name="allocation-bases"></a>Úthlutunargrunnar 

[!include [banner](../includes/banner.md)]

Úthlutunargrunnar eru grundvöllur úthlutunar rekstrarkostnaðar í kostnaðarbókhaldi. Úthlutunargrunnur getur verið magn, eins og þær vélastundir sem notaðar eru, notaðar kílóvatt-stundir (kWh), eða þeir fermetrar sem eru í notkun. Úthlutunargrunnar eru aðallega notaðir til að úthluta rekstrarkostnaði afurða sem framleiddar eru. Til dæmis úthlutar tæknideild kostnaði sínum samkvæmt fjölda þeirra tölva sem hver deild notar.

Það eru þrjár gerðir af úthlutunargrunnum í kostnaðarbókhaldi:

- Fyrirframskilgreindir úthlutunargrunnar fyrir víddarstak
- Stigveldi úthlutunargrunna
- Formúla úthlutunargrunna

## <a name="predefined-dimension-member-allocation-bases"></a>Fyrirframskilgreindir úthlutunargrunnar fyrir víddarstak

Úthlutunargrunnar fyrirframskilgreindra víddarstaka eru stofnaðir sjálfkrafa þegar víddarstak af einni af eftirfarandi tegundum er stofnað:

- Tölfræðileg víddarstök
- Víddarstök kostnaðareiningar

> [!NOTE]
> Úthlutunargrunnar fyrirframskilgreindra víddarstaka sem byggjast á víddarstaki kostnaðareiningar taka aðeins tillit til gilda úr gagnaveitunni, eins og fjárhag eða áætlun.

### <a name="example-1-use-a-cost-element-dimension-member-as-the-allocation-base"></a>Dæmi 1: Notaðu víddarstak kostnaðareiningar sem úthlutunargrunn
Þetta dæmi sýnir hvernig á að stofna úthlutunarreglu kostnaðar sem úthlutar kostnaðareiningu 10002 (Starfsmannatryggingar) á stöðu sem er skráð á kostnaðareiningu 10001 (Laun). Úthlutunarreglan er skilgreind eftir launahlutfalli hverrar deildar samanborið við heildarlaun. (Þörf á endurskoðun!)

Í fjárhag eru bókhaldslyklar skilgreindir sem hér segir.

| Bókhaldslykill | Aðallykill | lýsing        | Gerð aðallykils |
|------------------|--------------|--------------------|-------------------|
| Samnýtt           | 10001        | Laun           | Útgjöld           |
| Samnýtt           | 10002        | Starfsmannatryggingar | Útgjöld           |

Skilgreina kostnaðareiningarstak og skilgreina gagnatengi. Eftir að gögn eru flutt inn eru eftirfarandi færslur stofnaðar í kostnaðarbókhaldi.

**Víddarstök kostnaðareiningar**

| Víddarheiti kostnaðareiningar | Kostnaðareining |  lýsing       | Gerð    |
|-----------------------------|--------------|--------------------|---------|
| Kostnaðareiningar               | 10001        | Laun           | Aðal |
| Kostnaðareiningar               | 10002        | Starfsmannatryggingar | Aðal |

**Úthlutunargrunnar fyrirframskilgreindra víddarstaka** 

| Nafn  | lýsing        | Vídd kostnaðareiningar |
|-------|--------------------|------------------------|
| 10001 | Laun           | Kostnaðareiningar          |
| 10002 | Starfsmannatryggingar | Kostnaðareiningar          |

Í fjárhagnum hafa eftirfarandi færslur verið bókaðar:

- Færslur sem sýna aðallykilinn Laun koma úr launakerfi og eru bókaðar á kostnaðarstaði.
- Kostnaður vegna starfsmannatrygginga er bókaður handvirkt á sjálfgefinn kostnaðarstað.

| Dagsetning reikningsskila | Kostnaðarstaður |  lýsing        | Aðallykill |  lýsing       | Upphæð í bókhaldsgjaldmiðli |
|-----------------|-------------|---------------------|--------------|--------------------|-------------------------------|
| 03-01-2017      | CC001       | Mannauður                  | 10001        | Laun           | 2.000,00                      |
| 03-01-2017      | CC002       | FI                  | 10001        | Laun           | 5.000,00                      |
| 03-01-2017      | CC003       | Upplýsingatækni                  | 10001        | Laun           | 3.000,00                      |
| 01-03-2017      | CC099       | Sjálfgefin hlutverkamiðstöð | 10002        | Starfsmannatryggingar | 1.000,00                      |

Eftir að unnið hefur verið úr upprunagögnum úr fjárhagi eru eftirfarandi færslur stofnaðar í kostnaðarbókhaldi.

**Kostnaðarfærslur**

| Kostnaðarhlutur |  lýsing        | Kostnaðareining  |  lýsing       | Kostnaðarhegðun   |Upphæð|Dagsetning reikningsskila|
|-------------|---------------------|---------------|--------------------|-----------------|------|---------------|
| CC001       | Mannauður                  | 10001         | Laun           | Óflokkað    |2.000,00|  01-03-2017    |
| CC002       | FI                  | 10001         | Laun           | Óflokkað    |5.000,00|     01-03-2017         |
| CC003       | Upplýsingatækni                  | 10001         | Laun           | Óflokkað    |3.000,00|      01-03-2017        |
| CC099       | Sjálfgefin hlutverkamiðstöð | 10002         | Starfsmannatryggingar | Óflokkað    |1.000,00|      01-03-2017       |

Í þessu einfaldaða dæmi er kostnaðarúthlutunarregla stofnuð til að úthluta kostnaðareiningu 10002 (Starfsmannatryggingar) á stöðu sem er skráð á kostnaðareiningu 10001 (Laun).

**Kostnaðardreifingarregla**

| Hnútur á víddarstigveldi kostnaðarhlutar | Hnútur á víddarstigveldi kostnaðareiningar | Kostnaðarhegðun | Úthlutunargrunnur |
|--------------------------------------|---------------------------------------|---------------|-----------------|
| CC099                                | 10002                                 | Óflokkað  | 10001           |

**Útreikningur rekstrarkostnaðar**

Eftir að kostnaðareining 10001 (Laun) hefur verið notuð sem úthlutunargrunnur er niðurstaða útreiknings á rekstrarkostnaði eftirfarandi.

| Kostnaðarhlutur | lýsing | Mæligildi |   Úthlutunarþáttur         | Upphæð |
|-------------|-------------|-----------|-----------------------------|--------|
| CC001       | Mannauður          | 2.000     | (2,000 ÷ 10,000) × 1,000.00 | 200,00 |
| CC002       | FI          | 5.000     | (5,000 ÷ 10,000) × 1,000.00 | 500,00 |
| CC003       | Upplýsingatækni          | 3.000     | (3,000 ÷ 10,000) × 1,000.00 | 300.00 |

**Færslubók**

| Færslubók | Færslubókargerð                          | Fjárhagsdagatalstímabil | Ár | Tímabil   | Útgáfa                                                                 |
|---------|---------------------------------------|------------------------|------|----------|-------------------------------------------------------------------------|
| 00001   | Útreikningabók kostnaðardreifingar | Fjárhagur                 | 2017 | 1. tímabil | Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1 |

**Færslubókarfærslur stöðu kostnaðarhlutar**

| Dagsetning reikningsskila | Kostnaðarhlutur | lýsing         | Kostnaðareining | lýsing        | Kostnaðarhegðun |  Upphæð  |
|-----------------|-------------|---------------------|--------------|--------------------|---------------|----------|
| 01-31-2017      | CC099       | Sjálfgefin hlutverkamiðstöð | 10002        | Starfsmannatryggingar | Óflokkað  | 1.000,00 |

**Kostnaðarfærslur**

| Kostnaðarhlutur |  lýsing        | Kostnaðareining |    lýsing     | Kostnaðarhegðun | Upphæð    | Dagsetning reikningsskila |
|-------------|---------------------|--------------|--------------------|---------------|-----------|-----------------|
| CC099       | Sjálfgefin hlutverkamiðstöð | 10002        | Starfsmannatryggingar | Óflokkað  | -1.000,00 | 31-01-2017      |
| CC001       | Mannauður                  | 10002        | Starfsmannatryggingar | Óflokkað  | 200,00    | 31-01-2017      |
| CC002       | FI                  | 10002        | Starfsmannatryggingar | Óflokkað  | 500,00    | 31-01-2017      |
| CC099       | Upplýsingatækni                  | 10002        | Starfsmannatryggingar | Óflokkað  | 300.00    | 31-01-2017      |

### <a name="example-2-use-a-statistical-dimension-member-as-the-allocation-base"></a>Dæmi 2: Notaðu tölfræðilegt víddarstak sem úthlutunargrunn

Hægt er að nota tölfræðileg víddarstök sem úthlutunargrunna til að skilgreina stefnur eða gefa upp ópeningalega notkun eftir kostnaðarhlutum. Hægt er að stofna tölfræðileg víddarstök handvirkt eða flytja þau úr skrá með því að nota innflutnings-/útflutningsverkfærið í gagnastjórnun.

**Tölfræðileg víddarstök**

| Heiti tölfræðilegrar víddar | Tölfræðileg eining | lýsing               | Eining |
|----------------------------|---------------------|---------------------------|------|
| Tölfræðilegar einingar       | FTE                 | Starfsmenn í fullu starfi       | Ea   |
| Tölfræðilegar einingar       | Rafmagn         | Rafmagnsnotkun   | kWh  |

Þegar tölfræðilegt víddarstak er vistað er samsvarandi skrá stofnuð í úthlutunargrunnum fyrirframgreindra víddarstaka.

**Úthlutunargrunnar fyrirframskilgreindra víddarstaka**

| Nafn        | lýsing             | Tölfræðilegt víddarstak |
|-------------|-------------------------|-------------------------------|
| FTE         | Starfsmenn í fullu starfi     | Tölfræðilegar einingar          |
| Rafmagn | Rafmagnsnotkun | Tölfræðilegar einingar          |

Tölfræðiaðgerðir geta komið frá ýmsum stöðum:

- Hægt er að mæla rafmagnsnotkun með mælum sem eru settir upp víðs vegar um fyrirtækið.
- Töflur hafa að geyma tölfræðiaðgerðir. Til dæmis hefur HcmEmployment taflan að geyma lista yfir alla starfsmenn og þá kostnaðarstaði sem þeir tilheyra.

| Nafn       | Kostnaðarstaður |  lýsing  | Gerð starfskrafts |
|------------|-------------|----|-------------|
| Starfsmaður A | CC001       | Mannauður | Starfsmaður    |
| Starfsmaður B | CC002       | FI | Starfsmaður    |
| Starfsmaður C | CC002       | FI | Starfsmaður    |
| Starfsmaður D | CC003       | Upplýsingatækni | Starfsmaður    |
| Starfsmaður F | CC003       | Upplýsingatækni | Starfsmaður    |

> [!NOTE]
> Hægt er að nota allar töflur sem innihalda fjárhagslegar víddir sem uppsprettu tölfræðiaðgerða.

Kostnaðarbókhald styður safn tölfræðiaðgerða með því að notast við eftirfarandi gagnatengingar:

- Innflutnings-/útflutningsverkfæri í gagnastjórnun
- Tölfræðiaðgerðir

Til að sækja tölfræðiaðgerðir úr kerfinu er veitusniðmát tölfræðiaðgerðar nauðsynlegt. Sjáið veitusniðmát tölfræðiaðgerðar til að fá nánari upplýsingar. (Tengli verður bætt við þegar þetta efnisatriði hefur verið skrifað.)

**Veitusniðmát tölfræðiaðgerðar**

| Nafn  | Aðgerð | Frumtafla  | Summusvæði      | Dagsetningarsvæði     |
|-------|----------|---------------|----------------|----------------|
| FTE | Fjöldi    | HcmEmployment | Ekki tiltækt | Ekki tiltækt |

Eftir að unnið hefur verið úr upprunagögnum tölfræðiaðgerðar eru eftirfarandi færslur stofnaðar í kostnaðarbókhaldi.

**Tölfræðilegar færslur**

| Kostnaðarhlutur | lýsing      | Dagsetning reikningsskila | Tölfræðilegt víddarstak | lýsing         | Mæligildi |
|-------------|------------------|-----------------|------------------------------|---------------------|-----------|
| CC001       | Mannauður               | 31-01-2017      | FTE                        | Starfsmenn í fullu starfi | 1,00      |
| CC002       | FI               | 31-01-2017      | FTE                        | Starfsmenn í fullu starfi | 2.00      |
| CC003       | Upplýsingatækni               | 31-01-2017      | FTE                        | Starfsmenn í fullu starfi | 2.00      |

Hér er dæmi um kostnaðardreifingarreglu ef úthlutunargrunnur fyrirframskilgreinds víddarstaks fyrir FTE er úthlutaður sem úthlutunargrunnur þess.

| Kostnaðarhlutur | lýsing  | Mæligildi | Úthlutunarþáttur |
|-------------|------|-----------|-------------------|
| CC001       | Mannauður   | 1,00      | (1/5) × upphæð    |
| CC002       | FI   | 2.00      | (2/5) × upphæð    |
| CC003       | Upplýsingatækni   | 2.00      | (2/5) × upphæð    |

Hægt er að nota gagnaeiningu úr innfluttum tölfræðiaðgerðum til að flytja tölfræðiaðgerðir í kostnaðarbókhald. Einnig er hægt að nota innflutnings-/útflutningsverkfærið í gagnastjórnun. Í Excel er rafmagnsnotkun skráð sem hér segir.

| Dagsetning reikningsskila | Víddarstök | Mæligildi | Kennimerki uppruna |
|-----------------|------------------|-----------|-------------------|
| 31-01-2017      | CC001            | 2,450.00  | Rafmagn       |
| 31-01-2017      | CC002            | 4,100.00  | Rafmagn       |
| 31-01-2017      | CC003            | 15,000.00 | Rafmagn       |

Eftir að unnið hefur verið úr upprunagögnum tölfræðiaðgerðar eru eftirfarandi færslur stofnaðar í kostnaðarbókhaldi.

**Tölfræðilegar færslur**

| Kostnaðarhlutur |    | Dagsetning reikningsskila | Tölfræðilegt víddarstak |    lýsing          | Mæligildi |
|-------------|----|-----------------|------------------------------|-------------------------|-----------|
| CC001       | Mannauður | 31-01-2017      | Rafmagn                  | Notkun electricity | 2,450.00  |
| CC002       | FI | 31-01-2017      | Rafmagn                  | Notkun electricity | 4,100.00  |
| CC003       | Upplýsingatækni | 31-01-2017      | Rafmagn                  | Rafmagnsnotkun | 15,000.00 |

Hér er dæmi um kostnaðardreifingarreglu ef úthlutunargrunnur fyrirframskilgreinds víddarstaks rafmagns er úthlutaður sem úthlutunargrunnur þess.

| Kostnaðarhlutur | lýsing  | Mæligildi | Úthlutunarþáttur          |
|-------------|------|-----------|----------------------------|
| CC001       | Mannauður   | 2,450.00  | (2.450 ÷ 21.550) × upphæð  |
| CC002       | FI   | 4,100.00  | (4.100 ÷ 21.550) × upphæð  |
| CC003       | Upplýsingatækni   | 15,000.00 | (15.000 ÷ 21.550) × upphæð |

## <a name="hierarchy-allocation-bases"></a>Stigveldi úthlutunargrunna

Kostnaðarbókarar geta stofnað stigveldi úthlutunargrunns með því að nota hnút á víddarstigveldi kostnaðarhlutar á gildandi úthlutunargrunn. Á þennan hátt er hægt að takmarka svið upprunalegs úthlutunargrunns fyrirframgreinds víddarstaks. Hægt er að nota einn úthlutunargrunn fyrirframgreinds víddarstaks til að stofna nokkur stigveldi úthlutunargrunna. Hægt er að viðhalda víddastigveldi kostnaðarhlutar sem tengist stigveldi úthlutunargrunna.

### <a name="example-hierarchy-allocation-bases-that-are-based-on-full-time-employees-in-the-organization"></a>Dæmi: Stigveldi úthlutunargrunna sem byggjast á starfsmönnum í fullu starfi í fyrirtækinu
Hér er dæmi um víddastigveldi kostnaðarhlutar sem hægt er að stofna til að lýsa einfölduðu fyrirtæki.

| Heiti stigveldis | Hnútastig 0 | Hnútastig 1 | Hnútastig 2 | Meðlimir víddar |
|----------------|--------------|--------------|--------------|-------------------|
| Fyrirtæki   | Stjórnarformaður          | Fjármálastjóri          | FICO         | CC001             |
| Fyrirtæki   | Stjórnarformaður          | Fjármálastjóri          | Mannauður           | CC002             |
| Fyrirtæki   | Stjórnarformaður          | Framkvæmdastjóri upplýsingasviðs          | Upplýsingatækni           | CC003             |

Úthlutunargrunnur fyrirframgreinds víddarstaks fyrir FTE sem var stofnað í síðasta hluta hefur að geyma eftirtaldar færslur.

**Tölfræðilegar færslur**

| Kostnaðarhlutur | lýsing  | Dagsetning reikningsskila | Tölfræðilegt víddarstak | lýsing | Mæligildi |
|-------------|------|-----------------|------------------------------|---------------------|-----------|
| CC001       | Mannauður   | 31-01-2017      | FTE                        | Starfsmenn í fullu starfi | 1,00      |
| CC002       | FI   | 31-01-2017      | FTE                        | Starfsmenn í fullu starfi | 2.00      |
| CC003       | Upplýsingatækni   | 31-01-2017      | FTE                        | Starfsmenn í fullu starfi | 2.00      |

Kostnaður verður að dreifast milli kostnaðarstaða sem heyra undir fjármálastjóra fyrirtækisins. Það er staðfest að rétt úthlutunarhlutfall er fjöldi starfsmanna í fullu starfi eftir kostnaðarstöðum.

**Stigveldi úthlutunargrunna**

| Nafn                  | Úthlutunargrunnur | Víddarstigveldi kostnaðarhlutar | Hnútur á víddarstigveldi kostnaðarhlutar |
|-----------------------|-----------------|---------------------------------|--------------------------------------|
| Fjöldi starfsmanna í fullu starfi undir fjármálastjóra | FTE           | Fyrirtæki                    | Fjármálastjóri                                  |

Forskoðunaraðgerð gerir þér kleift að villuleita stigveldi úthlutunargrunns sem er stofnaður, á grundvelli tölfræðilegra færslna í kerfinu.

**Upplýsingar um úthlutunargrunn**

| Kostnaðarhlutur | lýsing  |  Mæligildi |
|-------------|------|------------|
| CC001       | Mannauður   | 1,00       |
| CC002       | FI   | 2.00       |

Hér er dæmi um kostnaðardreifingarreglu ef fjöldi FTE í stigveldi úthlutunargrunns fjármálastjóra er úthlutaður sem úthlutunargrunnur hans.

| Kostnaðarhlutur | lýsing  | Mæligildi | Úthlutunarþáttur |
|-------------|------|-----------|-------------------|
| CC001       | Mannauður   | 1,00      | (1/3) × upphæð    |
| CC002       | FI   | 2.00      | (2/3) × upphæð    |

## <a name="formula-allocation-bases"></a>Formúla úthlutunargrunna

Formúla úthlutunargrunns gerir þér kleift að skilgreina ítarlegar formúlur svo hægt sé að ná réttum úthlutunargrunn. Hægt er að stofna formúlu úthlutunargrunna handvirkt.

Þegar formúla úthlutunargrunns er stofnuð er valið hvaða tölfræðilega vídd og kostnaðareiningarvídd eigi að vera á bak við formúluna. Hægt er að nota alla úthlutunargrunna sem koma út áður völdum víddum í formúlu úthlutunargrunns.

> [!NOTE]
> Hægt er að nota áður skilgreindar formúlur úthlutunargrunns til að skilgreina nýja formúlu úthlutunargrunns.

Í stofnum formúlu úthlutunargrunns er hægt að stofna auknefni og tengja það við annað hvort úthlutunargrunn eða fasta. Auknefnin eru notuð til að skilgreina formúluna.

Hægt er að nota eftirtalda virkja til að skilgreina formúlu.

| Tákn | Texti           |
|---------|----------------|
| ( )     | Svigar    |
| \<      | Minni en   |
| \>      | Stærri en    |
| +       | samlagning       |
| –       | Frádráttur    |
| \*      | Margföldun |

Hefðbundnar **EF** yrðingar eru ekki studdar. Hins vegar er hægt að stofna yrðingar og villuleita til að ganga úr skugga um að þær séu sannar.

| Skýrsla | Prófun | Niðurstaða |
|-----------|------------|--------|
| a \> b    | TRUE       | 1      |
| a \> b    | FALSE      | 0      |

### <a name="example-1-a-simple-formula"></a>Dæmi 1: Einföld formúla

Rafmagnsreikningar eru oft í tveimur hlutum:

- Fasta þóknun fyrir tengingu við hnitanet
- Kostnað sem tengist notkun á kWh

Úthlutunargrunnar fyrirframskilgreindra víddarstaks rafmagns hafa þegar verið skilgreindir og hafa að geyma þessi gildi.

**Tölfræðilegar færslur**

| Kostnaðarhlutur | Nafn | Dagsetning reikningsskila | Tölfræðilegt víddarstak | lýsing             | Mæligildi |
|-------------|------|-----------------|------------------------------|-------------------------|-----------|
| CC001       | Mannauður   | 31-01-2017      | Rafmagn                  | Notkun electricity | 2,450.00  |
| CC002       | FI   | 31-01-2017      | Rafmagn                  | Notkun electricity | 4,100.00  |
| CC003       | Upplýsingatækni   | 31-01-2017      | Rafmagn                  | Rafmagnsnotkun | 15,000.00 |

Þurfi nú að dreifa fastri þóknun jafnt yfir kostnaðarhluta sem nota rafmagns eru tveir valkostir við að úthluta kostnaðinum:

- Stofna nýjan fyrirframskilgreindan úthlutunargrunn, Fast rafmagn, og setja svo gildið 1,00 á hvern kostnaðarhlut sem notar rafmagn.
- Stofna formúlu úthlutunargrunns, Fast rafmagn, sem nýtir fyrirframskilgreindan úthlutunargrunn fyrir rafmagn sem er þegar skilgreindur í kerfinu. Kosturinn við þessa leið er að það þarf aðeins að setja gögnin inn í kostnaðarbókhald fyrir eitt tölfræðilegt víddarstak fyrir rafmagn.

**Formúla úthlutunargrunns** 

| Nafn              | Vídd kostnaðareiningar | Tölfræðileg vídd | Formúla |
|-------------------|------------------------|-----------------------|---------|
| Fast rafmagn |                        | Tölfræðilegar einingar  |         |

Áður en hægt er að fylla út svæðið **Formúla** verður að tilgreina auknefnið sem nota á í formúlunni.

**Staðlar í formúlu úthlutunargrunns**

| Samnefni | Fasti | Úthlutunargrunnur |
|-------|----------|-----------------|
| a     |          | Rafmagn     |
| b     | 0,01     |                 |

Athugið að 0 (núll) er ekki stutt sem fasti.

**Formúla úthlutunargrunns**

| Nafn              | Vídd kostnaðareiningar | Tölfræðileg vídd | Formúla |
|-------------------|------------------------|-----------------------|---------|
| Fast rafmagn |                        | Tölfræðilegar einingar  | a \> b  |

Forskoðunaraðgerð gerir þér kleift að villuleita formúlu úthlutunargrunns sem er stofnaður, á grundvelli tölfræðilegra færslna í kerfinu.

**Upplýsingar um úthlutunargrunn**

| Kostnaðarhlutur | lýsing  | Formúla           | Mæligildi |
|-------------|------|-------------------|-----------|
| CC001       | Mannauður   | 2.450,00 \> 0,01  | 1,00      |
| CC002       | FI   | 4.100,00 \> 0,01  | 1,00      |
| CC003       | Upplýsingatækni   | 15.000,00 \> 0,01 | 1,00      |

Hér er dæmi um kostnaðardreifingarreglu ef formúlu úthlutunargrunns fyrir rafmagn er úthlutað sem úthlutunargrunnur þess.

**Mæligildi úthlutunarþáttar kostnaðarhlutar**

| Kostnaðarhlutur | Nafn | Mæligildi |  Úthlutunarþáttur |
|-------------|------|-----------|--------------------|
| CC001       | Mannauður   | 1,00      | (1/3) × upphæð     |
| CC002       | FI   | 1,00      | (1/3) × upphæð     |
| CC003       | Upplýsingatækni   | 1,00      | (1/3) × upphæð     |

### <a name="example-2-an-advanced-formula"></a>Dæmi 2: Ítarleg formúla
Í þessu dæmi á rafmagnskostnaður ekki bara að fylgja raunverulegri rafmagnsnotkun í kWh. Yfirstjórn vill innleiða hvata til að minnka rafmagnsnotkun. 

| Regla              | Taxti | 
|-------------------|------|
| a <= 10000,00 kWh | 0.75 |
| a > 10000,00 kWh  | 1.15 |

Ný formúla úthlutunargrunns, Rafmagnsnotkun, er stofnuð.

**Formúla úthlutunargrunns**

| Nafn              | Vídd kostnaðareiningar | Tölfræðileg vídd | Formúla |
|-------------------|------------------------|-----------------------|---------|
| Rafmagnsnotkun |                        | Tölfræðilegar einingar  |         |

Áður en hægt er að fylla út svæðið **Formúla** verður að tilgreina auknefnið sem nota á í formúlunni.

**Staðlar í formúlu úthlutunargrunns**

| Samnefni | Fasti  | Úthlutunargrunnur |
|-------|-----------|-----------------|
| a     |           | Rafmagn     |
| b     | 10.000,00 |                 |
| c     | 0.75      |                 |
| d     | 1.15      |                 |

**Formúla úthlutunargrunns**

| Nafn              | Vídd kostnaðareiningar | Tölfræðileg vídd | Formúla                                                    |
|-------------------|------------------------|-----------------------|------------------------------------------------------------|
| Fast rafmagn |                        | Tölfræðilegar einingar  | ((a \> b) × ((b × c) + (a – b) × d)) + ((a \<= b] × a × c) |

Forskoðunaraðgerð gerir þér kleift að villuleita formúlu úthlutunargrunns sem er stofnaður, á grundvelli tölfræðilegra færslna í kerfinu.

**Upplýsingar um úthlutunargrunn**

| Kostnaðarhlutur |    | Formúla                                                                                                                             | Mæligildi |
|-------------|----|-------------------------------------------------------------------------------------------------------------------------------------|-----------|
| CC001       | Mannauður | ((2.450,00 \> 10.000,00) × ((10.000,00 × 0,75) + (2.450,00 – 10.000,00) × 1,15)) + ((2.450,00 \<= 10.000,00) × 2.450,00 × 0,75)     | 1,837.50  |
| CC002       | FI | ((4.100,00 \> 10.000,00) × ((10.000,00 × 0,75) + (4.100,00 – 10.000,00) × 1,15)) + ((4.100,00 \<= 10.000,00) × 4.100,00 × 0,75)     | 3,075.00  |
| CC003       | Upplýsingatækni | ((15.000,00 \> 10.000,00) × ((10.000,00 × 0,75) + (15.000,00 – 10.000,00) × 1,15)) + ((15.000,00 \<= 10.000,00) × 15.000,00 × 0,75) | 1,3250.00 |

Hér sést formúlan fyrir CC003 (UPPLÝSINGATÆKNI) betur:

((15.000,00 \> 10.000,00) × ((10.000,00 × 0,75) + (15.000,00 – 10.000,00) × 1,15)) + ((15.000,00 \<= 10.000,00) × 15.000,00 × 0,75) = 13.250,00

(1 × (7.500,00 + 5.000,00 × 1,15)) + (0 × 15.000,00 × 0,75)            

1 × 7.500,00 + 5.750,00 + 0 

Hér er dæmi um kostnaðardreifingarreglu ef formúlu úthlutunargrunns fyrir fast rafmagn er úthlutað sem úthlutunargrunnur þess.


| Kostnaðarhlutur | lýsing | Mæligildi |        Úthlutunarþáttur         |
|-------------|-------------|-----------|----------------------------------|
|    CC001    |     Mannauður      | 1,837.50  | (1.837,50 ÷ 18.162,50) × upphæð  |
|    CC002    |     FI      | 3,075.00  | (3.075,00 ÷ 18.162,50) × upphæð  |
|    CC003    |     Upplýsingatækni      | 13,250.00 | (13.250,00 ÷ 18.162,50) × upphæð |



[!INCLUDE[footer-include](../../includes/footer-banner.md)]