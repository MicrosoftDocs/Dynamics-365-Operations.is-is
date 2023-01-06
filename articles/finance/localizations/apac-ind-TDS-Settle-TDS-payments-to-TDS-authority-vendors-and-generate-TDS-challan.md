---
title: Gera upp TDS-greiðslur hjá TDS-lánardrottnayfirvaldi og mynda TDS-greiðslukvittun
description: Í þessari grein er útskýrt hvernig á að gera upp skatta sem dregnir eru frá upprunalegri greiðslu (TDS) til lánardrottnayfirvalds TDS.
author: kailiang
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: e1ee65a555193433e6712a8caa892d7a3ad7bf61
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8848511"
---
# <a name="settle-tds-payments-to-tds-authority-vendors-and-generate-tds-challan"></a>Gera upp TDS-greiðslur hjá TDS-lánardrottnayfirvaldi og mynda TDS-greiðslukvittun

[!include [banner](../includes/banner.md)]

Í þessari grein er útskýrt hvernig á að gera upp skatta sem dregnir eru frá upprunalegri greiðslu (TDS) til lánardrottnayfirvalds TDS.

1. Farið í **Viðskiptaskuldir \> Greiðslur \> Greiðslubók lánardrottins**.

    [![Greiðslubókarsíða lánardrottins.](./media/apac-ind-TDS-51.png)](./media/apac-ind-TDS-51.png)

2. Á síðunni **Greiðslubók lánardrottins** skal velja **Ný** til að búa til nýja færslubókarlínu.
3. Í reitnum **Lykill** skal velja lánardrottnayfirvald TDS til að gera upp TDS-greiðslur við.
4. Veljið **Jöfnunarfærslur** til að opna síðuna **Jöfnunarfærslur** þar sem hægt er að skoða jafnaðar TDS-færslur fyrir lánardrottnayfirvald TDS.

    Jafnaðar TDS-færslur fyrir jöfnunartímabil eru sýndar á eftirfarandi hátt:

    - TDS-færslur þar sem eðli matsflokksins er **Fyrirtæki** eru sýndar sem ein færslulína.
    - TDS-færslur þar sem eðli matsflokksins er **HUF**, **Firma**, **Einstaklingur**, **AOP**, **BOI**, **Staðaryfirvald** eða **Annað** eru sýndar sem ein færslulína.
    - Reiturinn **Upphæð** sýnir heildarupphæð TDS sem á að greiða lánardrottnayfirvaldi TDS.

5. Veljið **Staðgreiðsluskattsfærslur** til að skoða ólíkar TDS-færslur sem eru hafðar með fyrir jöfnunarfærslurnar. Hægt er að skoða skiptingu hverrar TDS-færslu sem hefur verið tekin með í jöfnunarferlið fyrir jöfnunartímabilið á þessari síðu.
6. Í flipanum **Yfirlit** skal velja gátreitinn **Merkja** fyrir TDS-færslurnar sem á að gera upp við lánardrottnayfirvald TDS.

    Flipinn **Yfirlit** sýnir eftirfarandi upplýsingar fyrir hverja opna TDS-færslu:

    - **Dagsetning** – Færsludagsetning TDS.
    - **Fylgiskjal** – Fylgiskjalsnúmerið.
    - **Uppruni** – Einingin sem TDS-færslan er bókuð í.
    - **Söluaðili/viðskiptavinur** – Númer lánardrottins eða viðskiptavinalykils sem TDS er dregið frá.
    - **Heiti aðila sem dregið er frá** – Heiti lánardrottins eða viðskiptavinar sem TDS er dregið frá.
    - **Eðli mats** – Eðli matsflokks sem aðilinn sem dregið er frá tilheyrir.
    - **Upphæð** – Upphæð reiknings sem TDS var reiknað fyrir.
    - **Skattupphæð** – TDS-upphæð sem reiknuð var fyrir færsluna.

    > [!NOTE]
    > Hreinsið gátreitinn **Merkja** fyrir allar TDS-færslur sem á ekki að jafna gagnvart lánardrottnayfirvaldi TDS.

    Í flipanum **Almennt** sýnir reiturinn **PAN** varanlegt lykilnúmer (PAN) frádráttaraðilans. Reiturinn **Dagsetning** sýnir dagsetningu TDS-útreiknings og reiturinn **Gildi** sýnir heildarprósentuna sem var notuð í TDS-útreikningnum.

7. Veldu **skjámynd** til að skoða fylgiskjalsfærslur fyrir TDS-færsluna.
8. Lokið síðunni.
10. Veljið **Þættir staðgreiðsluskatts** til að opna síðuna **Þættir staðgreiðsluskatts** þar sem hægt er að skoða TDS sem var reiknað fyrir hvern TDS-skattþátt fyrir tiltekinn TDS-skattkóða.

    Í flipanum **Yfirlit** sýnir reiturinn **Skattþáttur** TDS-skattþáttinn sem var notaður fyrir færsluna. Reiturinn **Upphæð** sýnir TDS-upphæðina sem var reiknuð út fyrir TDS-skattþáttinn í grunngjaldmiðlinum. Reiturinn **Uppsöfnuð upphæð** sýnir heildarupphæð TDS sem var reiknuð út fyrir TDS-skattþáttinn fyrir allar jafnaðar færslur.

    Í flipanum **Upphæð** sýnir hlutinn **Sjálfgefinn gjaldmiðill** TDS-upphæðina sem var reiknuð fyrir TDS-skattþáttinn í sjálfgefna gjaldmiðlinum. Hlutinn **Aukagjaldmiðill** sýnir upphæðina í aukagjaldmiðlinum.

11. Lokið síðunni **Þættir staðgreiðsluskatts**.
12. Takið eftir að á síðunni **Breytingar á opnum færslum**, í reitnum **Upphæð**, er heildarupphæð sem á að jafna gagnvart lánardrottnayfirvaldi TDS fyrir jöfnunartímabilið uppfærð.
13. Til að jafna TDS-færslur mismunandi TDS-jöfnunartímabila gagnvart lánardrottnayfirvaldi TDS skal velja gátreitinn **Merkja** fyrir færslurnar.
14. Lokið síðunni **Breytingar á opnum færslum**.

    > [!NOTE]
    > Ef aðeins fáeinar færslur eru valdar fyrir jöfnunina á síðunni **Staðgreiðsluskattsfærslur** verður heildarupphæð TDS á völdum færslum uppfærð í reitnum **Leiðrétting** á síðunni **Breytingar á opnum færslum**. Leiðréttingarupphæðin er uppfærð í færslubókarlínunni á síðunni **Færslubókarfylgiskjal** og síðunni **Breytingar á opnum færslum** er lokað.

    Á síðunni **Færslubókarfylgiskjal** sýnir reiturinn **Debetfærsla** heildarupphæðina sem greiða á lánardrottnayfirvaldi TDS.

15. Færið inn upplýsingar um mótlykilinn.

    > [!NOTE]
    > Ef TDS-færslur eru með mismunandi skattlykilnúmer (TAN) verða færslubókarlínur stofnaðar fyrir hvert TAN á síðunni **Færslubókarfylgiskjal**.

16. Í flipanum **Greiðsluþóknun**, í reitnum **Kenni þóknunar**, skal velja kenni þóknunar sem er með gerð þóknunar sem **Vextir** eða **Annað** til að rukka greiðsluþóknun fyrir seinkaðar greiðslur sem eru greiddar lánardrottnayfirvaldi TDS.

    Í flipanum **Skattaupplýsingar**, í hlutanum **Fyrirtækjaupplýsingar**, sýnir reiturinn **Heiti** nafn fyrirtækisins. Í hlutanum **Staðgreiðsluskattur** sýnir reiturinn **Skattlykilnúmer (TAN)** TAN sem er hengt við færslulínuna.

17. Villuleita og bóka færslubók.
18. Veljið **Staðgreiðsluskattur \> Upplýsingar um greiðslukvittun** til að færa inn upplýsingar um greiðslukvittun vegna færslunnar.

    Reiturinn **Fylgiskjal** sýnir fylgiskjalsnúmer færslunnar.
    
19. Veljið gátreitinn **TDS lagt inn með bókarfærslu** ef TDS-upphæðin er lögð inn með því að nota bókarfærslu.
20. Í reitnum **Númer greiðslukvittunar** skal færa inn númer greiðslukvittunar sem er notuð til að greiða lánardrottnayfirvaldi TDS.
21. Í reitinn **Dagsetning** skal færa inn dagsetningu greiðslukvittunar.
22. Í reitnum **Heiti banka** skal velja heiti bankans sem greiða á TDS-upphæðina til vegna lánardrottnayfirvalds TDS sem leggja á inn á. Þessi reitur sýnir alla bankareikninga sem settir voru upp fyrir lánardrottnayfirvald TDS á **Viðskiptaskuldir \> Allir lánardrottnar \> Uppsetning \> Bankareikningar**.
23. Í reitinn **BSR-kóði** skal færa inn BSR-kóða (Basic Statistical Return) bankans.
24. Lokið síðunni.

### <a name="example"></a>Dæmi

Tímabilið 01/04/2009 er gert upp fyrir TDS-hlutaflokkinn **Leiga** með því að nota reglubundið TDS-uppgjörsferli. Heildarupphæð TDS sem nemur 141.625,00 er bókuð á lykil lánardrottnayfirvalds TDS fyrir TDS-uppgjörstímabil. Hægt er að skoða þessa upphæð í reitnum **Upphæð** á síðunni **Breytingar á opnum færslum** fyrir lánardrottnayfirvald TDS.

Ef valið er **Staðgreiðsluskattsfærslur** til að skoða mismunandi TDS-færslur sem voru gerðar upp fyrir tímabilið, birtast eftirfarandi upplýsingar.

| TDS upphæð |
|------------|
| 16,995.00  |
| 22,660.00  |
| 28,325.00  |
| 16,995.00  |
| 28,325.00  |
| 16,995.00  |
| 11,330.00  |

Fyrir ákveðna TDS-upphæð er hægt að velja **Þættir staðgreiðsluskatts** til að skoða TDS sem var reiknað fyrir hvern TDS-skattaþátt fyrir ákveðinn TDS-skattkóða. Í þessu dæmi er valið **Þættir staðgreiðsluskatts** fyrir TDS-upphæðina 16.995,00. Skattupphæðin sem reiknuð var í hvern þátt í færslunni kemur fram.

| Skatthluti | Upphæð    | Uppsöfnuð upphæð |
|---------------|-----------|--------------------|
| SNERTIMÖRK:           | 1,5000.00 | 125,000.00         |
| Álag      | 1,500.00  | 12,500.00          |
| PE-Cess       | 330.00    | 2,750.00           |
| SHE Cess      | 165.00    | 1,375.00           |

Ef aðeins voru valdar TDS-upphæðirnar 16.995,00, 22.660,00 og 28.325,00 fyrir uppgjörið á síðunni **Staðgreiðsluskattar**, er heildarupphæð jöfnunar sýnd sem **67.980,00** í reitnum **Leiðrétting** á síðunni **Breytingar á opnum færslum**. Ef þessi færsla er merkt fyrir jöfnun og síðuan **Breytingar á opnum færslum** er lokuð, er upphæðin **67.980,00** sýnd í reitnum **Debetfærsla** á síðunni **Fylgiskjal færslubókar**.

Nú er hægt að bóka dagbókina og búa til TDS challan.

### <a name="adjustment-of-advance-payments-that-are-made-to-tds-authority-vendors"></a>Leiðrétting á fyrirframgreiðslum sem greiddar eru lánardrottnayfirvöldum TDS

Til að breyta fyrirframgreiðslu sem var greidd lánardrottnayfirvaldi TDS yfir í raunverulega greiðslu skal fara í **Viðskiptaskuldir \> Lánardrottnar \> Allir lánardrottnar \> Breytingar á færslum**. Ef raunveruleg greiðsla sem er innt af hendi fer umfram fyrirframgreiðsluna verða tvö númer greiðslukvittunar búin til fyrir færsluna. Hins vegar er aðeins fyrsta númer greiðslukvittunarinnar sýnt í fyrirspurn TDS.
