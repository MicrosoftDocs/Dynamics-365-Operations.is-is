---
title: Regulatory Configuration Service (RCS) – altækir eiginleikar
description: Þetta efnisatriði útskýrir hvernig á að nota Microsoft Regulatory Configuration Services (RCS) og altæku geymsluna til að stofna og nota altæka eiginleika.
author: JaneA07
manager: AnnBe
ms.date: 06/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RCS, RCSWorkspace, e-Invoicing service
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: ae46dab5250fbe8096f43e420cb7ef33a5862af0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4444289"
---
# <a name="regulatory-configuration-services-rcs---globalization-features"></a>Regulatory Configuration Service (RCS) – altækir eiginleikar

[!include [banner](../includes/banner.md)]

Hægt er að nota Microsoft Regulatory Configuration Services (RCS) til að stofna altækan eiginleika sem hægt er að nota í altækri þjónustu, svo sem rafrænnar reikningsfærsluþjónustu. RCS gerir þér kleift að framkvæma þessi verk:

- Skilgreina tengda íhluti eiginleika.
- Stjórna líftíma eiginleikans í gegnum stöðu eiginleika.
- Gera eiginleika tiltækan fyrir skilgreind umhverfi.
- Deila eiginleika með öðrum fyrirtækjum.

Eftirfarandi ferli útskýra hvernig notandi í RCS getur bætt við altækum eiginleika og tengdum íhlutum, uppfært stöðu eiginleika og gert eiginleikann tiltækan þannig að hægt sé að nota hann í altækri þjónustu.

Áður en ferlunum er lokið þarf að ljúka við skrefin sem tengjast eftirfarandi verkum:

- RCS-tilvik opnað.
- Stofnun og virkjun skilgreiningarveitu. Nánari upplýsingar er að finna í [Stofna skilgreiningarveitendur og merkja þá sem virka](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

Í tilviki Finance and Operations-forrita skal fylgja þessum skrefum.

1. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
2. Ef engu RCS-umhverfi er úthlutað fyrir fyrirtækið skaltu velja **Regulatory Services – Skilgreining** og fylgja leiðbeiningunum til að úthluta einu slíku.

> [!NOTE]
> Ef RCS-umhverfi hefur þegar verið útvegað fyrir þitt fyrirtæki, notaðu slóðina á síðunni til að fá aðgang að umhverfinu með því að velja innskráningarvalkostinn.

## <a name="turn-on-the-globalization-features"></a>Kveikja á altækum eiginleikum

1. Í RCS-tilvikinu skal velja reitinn **Eiginleikastjórnun**.
2. Á vinnusvæðinu **Eiginleikastjórnun** skal velja **Altækir eiginleikar** í listanum og síðan velja **Virkja núna**.

    ![Altækir eiginleikar í eiginleikastjórnun](./media/RCS_GlobalF_1%20Feature%20mgmt.JPG)

## <a name="globalization-features"></a>Altækir eiginleikar

Til að nota altækan eiginleika verður fyrst að flytja hann inn úr altæku geymslunni og búa til eigin útgáfu af honum. Hægt er að bæta við altækum eiginleikum með tvennum hætti:

- Bæta við afleiddum eiginleika sem byggir á fyrirliggjandi eiginleika sem hefur verið birtur eða honum deilt.
- Bæta við nýjum eiginleika sem hefur verið búinn til frá grunni.

## <a name="access-globalization-features"></a>Aðgangur að altækum eiginleikum

1. Gangið úr skugga um að kveikt sé á eiginleikanum **Altækir eiginleikar** í eiginleikastjórnun eins og lýst er hér á undan í þessu efnisatriði.
2. Opnið nýja vinnusvæðið **Altækir eiginleikar** og síðan, undir **Eiginleikar**, skal velja reitinn **Rafræn reikningsfærsla**.

    ![Vinnusvæði altækra eiginleika](./media/RCS_GlobalF_2%20Feature%20wrkspace.JPG)

    Síðan **Eiginleikar rafrænnar reikningsfærslu** opnast.

    ![Eiginleikasíða rafrænnar reikningsfærslu](./media/RCS_GlobalF_3%20Feature%20form.JPG)

## <a name="add-a-derived-globalization-feature"></a>Bæta við afleiddum altækum eiginleika

Hægt er að bæta við nýjum altækum eiginleika með því að notast við fyrirliggjandi eiginleika sem hefur verið birtur eða honum deilt.

1. Veljið **Flytja inn** til að opna síðuna **Flytja inn eiginleika úr altækri geymslu**.

    ![Flytja inn eiginleika af síðu altækrar geymslu](./media/RCS_GlobalF_4%20Feature%20import%20form%20GR.JPG)

2. Veljið **Samstilla** til að fá nýjustu eiginleikana.

    Samstillti listinn inniheldur eiginleika sem eru tiltækir annaðhvort vegna þess að þeir voru gefnir út af Microsoft eða vegna þess að þeim var deilt með öðrum skilgreiningarveitum.

    ![Samstilltur listi yfir eiginleika](./media/RCS_GlobalF_5%20Feature%20GR%20sync.JPG)

3. Í listanum skal velja eiginleikana sem á að flytja inn og síðan velja **Flytja inn**. Þú færð skilaboð þegar valdir eiginleikar hafa verið fluttir inn.

    ![Skilaboð um lokinn innflutning](./media/RCS_GlobalF_6%20Feature%20GR%20import%20success.JPG)

4. Veljið **Bæta við** og síðan í fellilista svarglugga skal velja valkostinn **Byggt á fyrirliggjandi útgáfu**.
5. Færið inn heiti og lýsingu á eiginleikanum.
6. Í lista yfir tiltæka eiginleika skal velja grunnútgáfu eiginleikans og síðan velja **Stofna eiginleika**.

    ![Afleiddum eiginleika bætt við](./media/RCS_GlobalF_7%20Feature%20create%20derived.JPG)

    Eiginleikinn sem bætt var við er stofnaður og er með stöðuna **Drög**.

    ![Afleiddur eiginleiki sem er með stöðuna drög](./media/RCS_GlobalF_8%20Feature%20draft%20create.JPG)

7. Yfirfara skal íhluti eiginleika til að ákvarða hvort uppfærslur eru nauðsynlegar:

    - Fara skal yfir skilgreiningarnar ef skyldi reynast nauðsynlegt að sérstilla snið rafrænnar skýrslugerðar og bindingu þeirra við sniðsvarpanir fyrir eiginleikaútgáfuna.
    - Fara skal yfir uppsetninguna ef skyldi reynast nauðsynlegt að sérstilla flipann **Aðgerðir**, flipann **Gildissviðsreglur** eða flipann **Breytur** fyrir eiginleikaútgáfuna.

8. Í flipanum **Útgáfur** skal velja dagsetningu fyrir **Gildir frá** og færa inn lýsingu ef reiturinn **Lýsing** er auður.
9. Veljið **Breyta stöðu** til að ljúka við eiginleikann. Hægt er að bjóða upp á fullkláraða eiginleika fyrir tiltekið umhverfi til að hægt sé að nota þá í altækri þjónustu, eða hægt er að birta þá í altæku geymslunni.

> [!NOTE]
> Eiginleikar sem eru með gildi fyrir **Staða útgáfu eiginleika** sem **Útgefið** er hægt að deila með ytri fyrirtækjum.

## <a name="add-a-new-globalization-feature"></a>Bæta við nýjum altækum eiginleika

Hægt er að bæta við nýjum altækum eiginleika með því að búa hann til frá grunni.

1. Á síðunni **Flytja inn eiginleika úr altækri geymslu** skal velja **Bæta við** og síðan, í fellilista svargluggans, skal velja valkostinn **Nýr eiginleiki**.
2. Færið inn heiti og lýsingu á eiginleikanum.
3. Veljið **Stofna eiginleika**.

    ![Nýjum eiginleika bætt við](./media/RCS_GlobalF_9%20Feature%20create%20new.JPG)

4. Í flipanum **Útgáfur** skal velja dagsetningu fyrir **Gildir frá** og síðan velja **Breyta stöðu** til að ljúka við eiginleikann. Hægt er að bjóða upp á fullkláraða eiginleika fyrir tiltekið umhverfi til að hægt sé að nota þá í altækri þjónustu, eða hægt er að birta þá í altæku geymslunni.

> [!NOTE]
> Eiginleikar sem eru með gildi fyrir **Staða útgáfu eiginleika** sem **Útgefið** er hægt að deila með ytri fyrirtækjum.

## <a name="feature-component-overview"></a>Eiginleikastjórnunaryfirlit

Altækir eiginleikar eru með nokkra íhluti:

- **Útgáfa** – Þessi íhlutur styður eiginleika líftímastjórnunar og gerir notendum kleift að stjórna stöðu fyrir mismunandi útgáfur af eiginleikanum.
- **Skilgreiningar** - Þessi íhlutur gerir notendum kleift að stjórna, skoða og breyta tengdum sniðum rafrænnar skýrslugerðar og sniðsvörpunum.
- **Uppsetningar** – Þessi íhlutur leyfir notendum altækrar þjónustu, t.d. rafrænnar reikningsfærsluþjónustu, að stjórna uppsetningu á tengdri eiginleikaútgáfu. Hann styður þar af leiðandi sveigjanlega smíði á samskipta- og svörunarreglum.
- **Umhverfi** – Þessi íhlutur leyfir notendum altækrar þjónustu, t.d. rafrænnar reikningsfærsluþjónustu, að stjórna umhverfi þar sem uppsetning eiginleikaútgáfu er notuð og veitir notendum sem hafa aðgang að henni heimild.
- **Fyrirtæki** – Þessi íhlutur gerir notendum kleift að deila eiginleika með ytri fyrirtækjum.

## <a name="configuring-feature-components"></a>Eiginleikaíhlutir skilgreindir

### <a name="version-and-status"></a>Útgáfa og staða

Útgáfan er notuð til að stjórna stuðningstíma altæks eiginleika.

Hægt er að breyta stöðunni í reitnum **Staða** í flipanum **Útgáfa**. Eftirfarandi stöður eru í boði:

- **Drög** – Aðeins er hægt að breyta eiginleikanum þegar hann er í þessari stöðu.
- **Lokið** – Eiginleikinn og allir tengdir íhlutir hafa verið fullkláraðir (lokið) og ekki er hægt að breyta þeim.
- **Útgefið** – Eiginleikinn og allir tengdir íhlutir hafa verið gefnir út í altæku geymslunni.
- **Deilt** – Eiginleikanum og öllum tengdum íhlutum hefur verið deilt með ytri fyrirtækjum.
- **Virkjað** – Eiginleikinn og allir tengdir íhlutir hafa verið virkjaðir til að nota í altækri þjónustu, t.d. rafrænni reikningsfærsluþjónustu.

> [!NOTE]
> Eiginleikar verða að fara í réttri röð í gegnum þessar stöður. Þess vegna er ekki endilega hægt að nálgast allar stöður á hverju stigi líftíma.

### <a name="configurations"></a>Afbrigði

Eftirtaldar aðgerðir er hægt að stilla:

- **Skoða** – Skoða undirliggjandi skilgreiningar eiginleika sem krefjast ekki neinnar uppfærslu.
- **Breyta** – Stofna útgáfudrög af valinni skilgreiningu til að hægt sé að breyta sniði eða sniðsvörpun í sniðshönnuði.
- **Eyða** – Eyða valinni skilgreiningu úr eiginleikanum.
- **Endurreikna grunn** – Endurreikna grunn eiginleikans. Nánari upplýsingar er að finna í hlutanum [Endurreikna grunn afleiddra altækra eiginleika](#rebase) síðar í þessu efnisatriði.

### <a name="setups"></a>Uppsetningar

Eftirtaldar aðgerðir eru í boði fyrir uppsetningar eiginleika:

- **Bæta við** – Stofna nýja uppsetningu eiginleika. Hægt er að taka þessa eiginleikauppsetningu úr fyrirliggjandi eiginleikauppsetningu eða búa hana til frá grunni.
- **Eyða** – Eyða valinni uppsetningu eiginleika.
- **Skoða** – Skoða undirliggjandi uppsetningu eiginleika sem þarfnast ekki breytinga.
- **Breyta** – Stofna, eyða eða breyta eigindum þriggja helstu íhluta eiginleikauppsetningar:

    - Aðgerðir og færibreytur þeirra
    - Gildissviðsreglur
    - Breytur

![Uppsetningarsíða eiginleikaútgáfu](./media/RCS_GlobalF_10%20Feature%20set%20up.JPG)

### <a name="environments"></a>Umhverfi

Eftirtaldar aðgerðir eru í boði fyrir umhverfi:

- **Virkja** – Fyrir valda eiginleikaútgáfu skal velja útgefið umhverfi og velja dagsetningu fyrir **Gildir frá** þegar hún á að vera í boði. Nánari upplýsingar er að finna í hlutanum [Skilgreina umhverfi fyrir virkjun](#configureenvironment) síðar í þessu efnisatriði.
- **Hætta við** – Fjarlægja umhverfi fyrir eiginleikauppsetningu.

### <a name="organizations"></a>Fyrirtæki

Fylgið eftirfarandi skrefum til að samnýta altæka eiginleika með ytra fyrirtæki.

1. Á síðunni **Eiginleikar rafrænnar reikningsfærslu** skal velja eiginleikann og eiginleikaútgáfuna sem á að samnýta.
2. Í flipanum **Fyrirtæki** skal velja **Samnýta með** og síðan, í fellilistaglugganum, skal færa inn lénsheiti fyrirtækisins.
3. Veldu **Deila**.

    ![Samnýta eiginleika með fyrirtæki](./media/RCS_GlobalF_20%20Feature%20orgn_share%20with.JPG)

Eiginleikanum er deilt með ytra fyrirtækinu og er aðgengilegur fyrir það fyrirtæki í altæku geymslunni. Þaðan er hægt að flytja hann inn í tilvik fyrirtækisins í RCS eða Dynamics 365 Finance svo hægt sé að nota hann.

## <a name="rebase-derived-globalization-features"></a><a name="rebase"></a>Endurreikna grunn afleiddra altækra eiginleika

Hægt er að endurreikna grunn afleidds altæks eiginleika yfir í nýja eða uppfærða útgáfu grunneiginleikans. Á þennan hátt er hægt að uppfæra breytingar sem hafa átt sér stað í grunnútgáfunni sjálfkrafa. Uppfærð útgáfa grunneiginleika er stofnuð af upprunalegri skilgreiningarveitu og hún er síðan gefin út eða samnýtt.

![Uppfærð útgáfa grunneiginleika](./media/RCS_GlobalF_12%20Feature%20new%20version.JPG)

Til dæmis, ef ætlunin er að endurgera afleidda útgáfu eiginleika sem var stofnuð þarf fyrst að sækja nýjustu útgáfuna aðgerðarinnar með því að flytja hana inn úr altæku geymslunni.

1. Á síðunni **Eiginleikar rafrænnar reikningsfærslu** skal velja **Flytja inn**.
2. Veljið **Samstilla** til að fá nýjustu eiginleikana.
3. Í listanum yfir eiginleika skal velja eiginleikana sem á að flytja inn og síðan velja **Flytja inn**.

    ![Nýjasta útgáfa eiginleika flutt inn](./media/RCS_GlobalF_13%20Feature%20new%20version%20import.JPG)

4. Í listanum yfir eiginleika skal velja eiginleikann sem á að endurreikna grunn fyrir.
5. Í flipanum **Útgáfa** skal velja **Ný** til að búa til drög að útgáfu.

    ![Ný drög að útgáfu búin til](./media/RCS_GlobalF_14%20Feature%20new%20base%20version.JPG)

6. Veldu **Endurreikna grunn**.
7. Í svarglugganum **Endurreikna grunn** skal velja nýjustu útgáfu eiginleikans til að endurreikna til.

    ![Gluggi fyrir endurreikning grunns](./media/RCS_GlobalF_15%20Feature%20rebase%20version.JPG)

8. Veljið **Í lagi**.
9. Farið yfir íhluti eiginleikans og gerið allar nauðsynlegar breytingar.
10. Veljið **Breyta stöðu** til að ljúka við eiginleika með endurreiknaðan grunn. Þegar endurreikning grunns er lokið er hægt að framkvæma fleiri aðgerðir. Til dæmis er hægt að gefa út eiginleikann og gera hann tiltækan til að nota í altækri þjónustu.

    ![Eiginleikastaða uppfærð í Lokið](./media/RCS_GlobalF_16%20Feature%20rebase%20version%20complete.JPG)

## <a name="configure-environments-for-globalization-features"></a><a name="configureenvironment"></a>Stilla umhverfi fyrir altæka eiginleika

Notendur altækrar þjónustu geta stjórnað umhverfinu til að setja upp altækan eiginleika og veitt heimild til annarra notenda sem hafa aðgang að honum.

1. Á vinnusvæðinu **Altækir eiginleikar**, undir **Umhverfi**, skal velja reitinn **Rafræn reikningsfærsla**.

    ![Vinnusvæði altækra eiginleika](./media/RCS_GlobalF_17%20Feature%20environment.JPG)

2. Veljið **Færibreytur lyklageymslu** og veljið síðan **Nýr** til að búa til leynilykil Azure-lyklageymslu.
3. Sláið inn heiti og lýsingu fyrir lyklageymsluna og síðan, í reitnum **Lyklageymsla**, skal slá inn vefslóðina sem auðkennir tilfang lyklageymslunnar í Azure.
4. Í flýtiflipanum **Vottorð** skal velja **Bæta við** til að bæta vottorðinu við og færa inn heiti og lýsingu fyrir hvert vottorð.

    ![Vottorði bætt við](./media/RCS_GlobalF_18%20Feature%20envn%20key%20vault%20parameter.JPG)

5. Velja skal **Nýtt** til að stofna nýtt umhverfi.
6. Færa skal inn heiti, lýsingu og samnýtt leynitákn undirskriftar fyrir aðgang sem þarf fyrir geymsluna.
7. Á flýtiflipanum **Notendur** skal velja **Nýr** til að bæta við nýjum notanda sem fær aðgang að þessu umhverfi.
8. Sláið inn notandakenni og tölvupóstfang notanda.
9. Endurtakið skref 7 og 8 til að bæta við fleiri notendum.
10. Veljið **Gefa út** til að gefa út umhverfið.

    ![Útgefið umhverfi](./media/RCS_GlobalF_19%20Feature%20envn%20publishing.JPG)
