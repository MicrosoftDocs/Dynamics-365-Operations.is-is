---
title: Skipuleggja staðbundna bókhaldslykla
description: Þetta efnisatriði veitir upplýsingar sem hjálpa til við að skipuleggja bókhaldslykla þegar til staðar eru lagalegar/staðbundnar kröfur fyrir fyrirtækið þitt.
author: VeselinaE
ms.date: 10/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts, LedgerConsolidateAccountGroup, MainAccountConsolidateAccount, DimensionDetails, MainAccountDetails
ROBOTS: ''
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.tgt_pltfrm: ''
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.search.industry: ''
ms.author: veneva
ms.search.validFrom: 10/07/2021
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e224a2e24b4ba293c953c6c883307038128e2f04
ms.sourcegitcommit: ba10ba2cd4fb4267afb5aacae4f6a52aa2456e7e
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/11/2021
ms.locfileid: "7798297"
---
# <a name="plan-your-local-chart-of-accounts"></a>Skipuleggja staðbundna bókhaldslykla

[!include [banner](../includes/banner.md)]

Þetta efnisatriði veitir upplýsingar sem hjálpa til við að skipuleggja bókhaldslykla þegar fyrirtækið inniheldur lögaðila sem þurfa að uppfylla kröfur tiltekinna staða þar sem viðskipti eru stunduð. Þetta efnisatriði notar eftirfarandi hugtök til að lýsa bókhaldslyklum:

- **Altækt** – Bókhaldslykill sem fyrirtækið notar alþjóðlega. Í flestum tilvikum sameinar þú í þennan bókhaldslykil.
- **Staðbundið** – Bókhaldslykill sem lögaðilar í tilteknu landi eða svæði notar.
- **Samnýttur** – Bókhaldslykill sem fleiri en einn lögaðili geta notað. Bæði er hægt að samnýta altækan bókhaldslykil og staðbundinn bókhaldslykil.

Þú getur búið til og samnýtt marga bókhaldslykla. Fleiri en einn lögaðili getur notað samnýttan bókhaldslykil, en aðeins er hægt að úthluta einum bókhaldslykli á hvern lögaðila. Bókhaldslykill sem lögaðili notar er skilgreindur á síðunni **Fjárhagur**.

Þegar bókhaldslykill er hannaður vilja mörg fyrirtæki nota altækan bókhaldslykil. Möguleiki samnýtts bókhaldslykils gerir kleift að stofna altækan bókhaldslykil. Ávinningur fylgir því að búa til og nota einn bókhaldslykil. Til dæmis verður stjórnun, umsjón, viðhald og skýrslugerð auðveldari.

Flest fyrirtæki kjósa altækan bókhaldslykil og auðveldast er að innleiða hann. Engu að síður þurfa sumir lögaðilar staðbundinn bókhaldslykil af eftirfarandi ástæðum:

- Staðbundnar lagalegar kröfur
- Kröfur um staðbundna bókhaldsstaðla
- Iðnaðarkröfur
- Sértækar kröfur um skýrslugerð og greiningu fyrirtækis

Ef fyrirtækið krefst þess að lögaðili noti staðbundinn bókhaldslykil eru tveir kostir í boði til að koma því til leiða:

- Úthlutaðu altækum bókhaldslykli og skilgreindu aðrar leiðir til að uppfylla staðbundnar kröfur.
- Úthlutaðu lögaðila staðbundinn bókhaldslykil og skilgreindu tengsl við altæka bókhaldslykilinn.

Skipulag fyrirtækis og skýrslugerðar ákvarða valkostinn sem er notaður.

[![ Skýringarmynd sem sýnir hvernig skipulag fyrirtækisins ákvarðar hvort nota á altækan eða staðbundinn bókhaldslykil](./media/local-chart-of-accounts-diagram.png)](./media/local-chart-of-accounts-diagram.png)

Ef lögaðila er úthlutað altækum bókhaldslykli eru eftirfarandi valkostir í boði til að uppfylla staðbundnar skýrslukröfur:

- Gera staðbundna sameiningu.
- Nota fjárhagsvídd til að rekja staðbundinn bókhaldslykil.
- Búa til staðbundna aðallykla í altækum bókhaldslykli.
- Gera utanaðkomandi vörpun í staðbundinn bókhaldslykil.

Ef staðbundnum bókhaldslykli er úthlutað á lögaðilann er altæk sameining eini möguleikinn í boði til að uppfylla altækar skýrslukröfur.

## <a name="global-chart-of-accounts-assigned-to-a-legal-entity"></a>Altækum bókhaldslykli úthlutað á lögaðila

Ef þú verður að úthluta altækum bókhaldslykli á lögaðila eru fjórir valkostir í boði til að skilgreina kerfið eins og lýst var hér á undan. Fyrir alla fjóra valkostina er einn bókhaldslykill skilgreindur og tengdur við hvern lögaðila á síðunni **Fjárhagur**. Hver valkostur notar þá aðra aðferð til að uppfylla kröfur um staðfæringu. Eftirfarandi hlutar lýsa hástigs skrefunum til að skilgreina kerfið fyrir kröfur um staðfæringu. Þeir lýsa einnig kostum og ókostum við hvern valkost.

### <a name="do-local-consolidation"></a>Gera staðbundna sameiningu

Staðbundin sameining er sú aðferð sem mælt er með til að uppfylla staðbundnar kröfur um bókhaldslykla og nýta sér virkni kerfisins sem var hönnuð í þessum tilgangi.

#### <a name="set-up-consolidation-for-a-local-chart-of-accounts"></a>Setja upp sameiningu fyrir staðbundinn bókhaldslykil

1. Búðu til einn altækan bókhaldslykil sem inniheldur alla nauðsynlega aðallykla.
2. Í hverjum lögaðila skal úthluta altækum bókhaldslykli á síðunni **Fjárhagur**.
3. Búðu til samstæðulögaðila fyrir hverja staðfæringu sem krafist er.
4. Fylgið einu af eftirfarandi skrefum:

    - Ef aðeins er þörf á einni staðfæringu skal skilgreina samstæðulykilinn á síðunni **Aðallykill** eða nota síðurnar **Samstæðuflokkar** og **Fleiri samstæðulyklar**.
    - Ef þörf er á fleiri en einni staðfæringu eða ef bæði númer og heiti lykils þarfnast þýðingar skal nota síðurnar **Samstæðuflokkar** og **Fleiri samstæðulyklar** til að uppfylla kröfur um staðfæringu.

5. Keyrðu samstæðuferlið til að umbreyta gildinu úr upprunalegum lögaðila sem notar altækan bókhaldslykil í samstæðufyrirtæki sem notar staðbundinn bókhaldslykil.

#### <a name="advantages"></a>Ávinningur

- Þessi nálgun býður upp á áreiðanlega leið til að vinna í öllu fyrirtækinu.
- Ein þýðing á staðbundinni stöðu er gerð.
- Þessi aðferð styður þýðingu á bæði auðkenni aðallykils og heiti hvers aðallykils.
- Hún styður margar staðfæringar.

#### <a name="disadvantages"></a>Ókostir

- Til viðbótar er annað samstæðufyrirtæki búið til.
- Ferli viðbótarsamstæðu er lokið.
- Þessi nálgun getur komið fram á staðbundnu grafi eingöngu eftir að samstæðuferlinu er lokið.

### <a name="use-a-financial-dimension-to-track-the-local-chart-of-accounts"></a>Nota fjárhagsvídd til að rekja staðbundinn bókhaldslykil

Þessi aðferð notar fjárhagsvídd þar sem fjárhagsvíddargildin tákna staðbundna aðallykla sem krafist er fyrir staðfærsluna. Hún virkar vel ef aðeins er þörf á einni staðfæringu. Notagildi hennar minnkar þó þegar þú bætir við fleiri staðfæringum og fjárhagsvíddum.

#### <a name="set-up-a-financial-dimension-for-a-local-chart-of-accounts"></a>Setja upp fjárhagsvídd fyrir staðbundinn bókhaldslykil

1. Búðu til einn altækan bókhaldslykil sem inniheldur alla nauðsynlega aðallykla.
2. Í hverjum lögaðila skal úthluta altækum bókhaldslykli á síðunni **Fjárhagur**.
3. Búðu til fjárhagsvídd sem sýnir staðbundinn bókhaldslykil.
4. Búðu til fjárhagsvíddargildi sem sýnir aðallykla í staðbundnum bókhaldslykli.
5. Uppfærðu lykilskipulagið þannig að það innihaldi fjárhagsvíddina „staðbundinn bókhaldslykill“.
6. Gakktu úr skugga um að fjárhagsvíddin „staðbundinn bókhaldslykill“ hafi alltaf gildi og að hún leyfi ekki tómt gildi. Íhugaðu að nota afleiddar víddir eða fastar víddir.
7. Búðu til fjárhagsvíddasamstæðu þar sem fjárhagsvíddin „staðbundinn bókhaldslykill“ er fyrsta valda fjárhagsvíddin. Hægt er að nota fjárhagsvíddasamstæðuna þegar prófjöfnuður er myndaður.

#### <a name="advantages"></a>Ávinningur

- Aðallyklar fyrir bæði altæka og staðbundna bókhaldslykilinn eru til á færslustigi. Aðallykillinn er altækkur og fjárhagsvíddargildið er staðbundið.
- Þessi aðferð býður upp á skýrslugjöf í rauntíma og yfirlit yfir bæði altæka fjárhagsstöðu og staðbundna fjárhagsstöðu.

#### <a name="disadvantages"></a>Ókostir

- Í færibreytum fjárhags, ef reiturinn **Gildi sem notuð eru fyrir safnlykil** er stilltur á **Dreifing á fjárhagsupphæðum**, verða fjárhagsvíddirnar sem sýna aðallykilinn fyrir útgjöld/eign/tekjur ranglega notaðar fyrir safnlykil viðskiptakrafa og viðskiptaskulda. Mælt er með því að stilla reitinn á upprunaskjal í staðinn til að tryggja að rétt fjárhagsvíddargildi séu notuð.
- Ef krafist er margra staðbundinna bókhaldslykla og ein fjárhagsvídd er notuð fyrir þá alla, getur listinn yfir fjárhagsvíddargildin sem eru notuð verið langur og erfitt að vinna með.
- Ef krafist er margra staðbundinna bókhaldslykla og aðskilin fjárhagsvídd er notuð til að sýna hvern þeirra, getur það haft áhrif á nytsemi og afköst kerfisins þegar fjárhagsvíddum og fjárhagsvíddasamstæðum er bætt við.
- Mælt er með því að íhuga vandlega fjölda fjárhagsvídda sem þú þarft á að halda, fjölda gilda í hverri þeirra og fjölda fjárhagsvíddasamstæða, vegna þess að allir þessir þættir geta haft áhrif á afköst kerfisins.

### <a name="create-local-main-accounts-in-the-global-chart-of-accounts"></a>Búa til staðbundna aðallykla í altækum bókhaldslykli

*Það sem ritsjórinn spurði um:* Í þessari aðferð inniheldur staðbundinn aðallykill í altækum bókhaldslykli aðallyklana í staðbundnum bókhaldslykli í altækum bókhaldslykli.

*Upprunaleg útgáfa:* Aðferð staðbundins aðallykils innan altæks bókhaldslykils er sú að aðallyklar staðbundins bókhaldslykils eru hafðir með í altækum bókhaldslykli.

*Ætti að segja þetta:* Í þessari aðferð eru staðbundnir aðallyklar í staðbundnum bókhaldslykli hafðir með í altækum bókhaldslykli.


#### <a name="set-up-local-main-accounts-in-the-global-chart-of-accounts"></a>Setja upp staðbundna aðallykla í altækum bókhaldslykli

1. Búðu til einn bókhaldslykil sem inniheldur aðallyklana fyrir bæði altækan bókhaldslykil og staðbundinn bókhaldslykil.
2. Í hverjum lögaðila skal úthluta bókhaldslykli á síðunni **Fjárhagur**.
3. Búðu til samtölulykla í bókhaldslyklinum til að leggja saman aðallyklana sem þjóna sama tilgangi.
4. Búðu til hnekkingar lögaðila á hverjum staðbundnum lykli til að koma í veg fyrir færslur úr öðrum lögaðila sem staðbundni lykillinn var ekki hannaður fyrir.
5. Búðu til hnekkingar lögaðila á hverjum altækum lykli til að koma í veg fyrir færslur frá staðbundnum lögaðilum.

#### <a name="advantages"></a>Ávinningur

- Yfirlit í rauntíma yfir bæði altæka fjárhagsstöðu og staðbundna fjárhagsstöðu er í boði í tilteknum skýrslum og í tilteknum yfirlitum í kerfinu, t.d. fjárhagsskýrslu efnahagsreiknings. Einnig er hægt að nálgast það með því að nota hnappinn **Tímabil** í samtölulyklinum.
- Þú ert ekki með viðbótarhluta í fjárhagslyklinum.

#### <a name="disadvantages"></a>Ókostir

- Notkun og sýnileiki samtölulykils er takmörkuð. Til dæmis eru samtölulyklar ekki sýnilegir á listasíðunni **Prófjöfnuður**.
- Viðhald krefst meiri vinnu.
- Myndun fjárhagsskýrslna krefst meiri handvirkrar vinnu.

### <a name="do-external-mapping-to-the-local-chart-of-accounts"></a>Gera utanaðkomandi vörpun í staðbundinn bókhaldslykil

Innleiðing altæks bókhaldslykils gerir ráð fyrir að þú stjórnir vörpun og staðfæringum utan kerfisins. Í þessari aðferð býrðu bara til einn altækan bókhaldslykil í Microsoft Dynamics 365 Finance og meðhöndlar kröfurnar utan kerfisins.

#### <a name="set-up-external-mapping-to-a-local-chart-of-accounts"></a>Setja upp ytri vörpun í staðbundinn bókhaldslykil

1. Búðu til einn altækan bókhaldslykil sem inniheldur alla nauðsynlega aðallykla.
2. Í hverjum lögaðila skal úthluta altækum bókhaldslykli á síðunni **Fjárhagur**.
3. Gera vörpun í staðbundinn bókhaldslykil utan við Finance.

#### <a name="advantages"></a>Ávinningur

- Þessi nálgun býður upp á sameinaðar leiðir til að vinna í öllu fyrirtækinu.

#### <a name="disadvantages"></a>Ókostir

- Engar staðbundnar skýrslugerðir frá kerfinu eru í boði.
- Villur koma gjarnan upp í þessari aðferð þegar fjárhagsskýrslur eru búnar til.

## <a name="local-chart-of-accounts-assigned-to-legal-entity"></a>Staðbundnum bókhaldslykli er úthlutað á lögaðila

Ef fyrirtækið þitt ákveður að nota ekki altækan bókhaldslykil í öllum lögaðilum verður aðskilinn bókhaldslykill búinn til fyrir hvern einkvæman staðbundinn bókhaldslykil. Hver lögaðili er síðan tengdur við samsvarandi bókhaldslykil á síðunni **Fjárhagur**.

### <a name="do-global-consolidation"></a>Gera altæka sameiningu

Í þessari aðferð er samstæðufyrirtæki notað til að taka saman og sameina stöðurnar úr hverju staðbundnu upprunafyrirtæki í sameinaðan altækan bókhaldslykil í samstæðufyrirtækinu. Þessi aðferð krefst þess að þú vinnir með vörpun á hverjum staðbundnum bókhaldslykli í altækan bókhaldslykil í samstæðufyrirtækinu.

#### <a name="set-up-global-consolidation"></a>Setja upp altæka sameiningu

1. Búðu til aðskilinn bókhaldslykil fyrir hvern lögaðila sem er með annan staðbundinn bókhaldslykil. Ef einhverjir lögaðilar eru með sama staðbundna bókhaldslykilinn er aðeins þörf á einum staðbundnum bókhaldslykli og hægt er að samnýta hann.
2. Í hverjum lögaðila skal úthluta viðeigandi bókhaldslykli á síðunni **Fjárhagur**.
3. Valfrjálst: Búðu til bókhaldslykil fyrir altækan bókhaldslykil fyrir hvert samstæðufyrirtæki sem er með annan altækan bókhaldslykil.
4. Búðu til samstæðulögaðila fyrir hvert samstæðustig sem gerð er krafa um og úthlutaðu viðeigandi bókhaldslykli á síðunni **Fjárhagur**.
5. Fylgið einu af eftirfarandi skrefum:

    - Ef aðeins þarf eina sameiningu skal skilgreina samstæðulykilinn á síðunni **Aðallykill**.
    - Ef þörf er á fleiri en einni sameiningu eða ef bæði númer og heiti lykils þarfnast þýðingar skal nota síðurnar **Samstæðuflokkar** og **Fleiri samstæðulyklar** til að sýna kröfurnar fyrir altækan bókhaldslykil.

6. Keyrðu samstæðuferlið til að flytja stöðurnar úr staðbundnum lögaðilum í samstæðulögaðilann. Þessi samstæðulögaðili notar samstæðulykla sem þú skilgreindir í skrefi 5.

#### <a name="advantages"></a>Ávinningur

- Snið staðbundinna bókhaldsstaðla er notað á hverjum stað fyrir sig.
- Þessi aðferð auðveldar vinnu staðbundins fjárhagsteymis.

#### <a name="disadvantages"></a>Ókostir

- Ekkert yfirlit í rauntíma yfir altæka stöðu er í boði.
- Keyra má samstæðuferlið oftar.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Yfirlit yfir bókhaldslykil](plan-chart-of-accounts.md)
- [Grunnstilla fjárhag](configure-ledger.md)
- [Fjárhagsvíddir og bókun](Default-dimensions.md#balancing-dimension)
- [Fjárhagsvíddasamstæður](financial-dimension-sets.md)
- [Yfirlit yfir samstæðu og niðurfellingu](../budgeting/consolidation-elimination-overview.md)
- [Hópar samstæðulykla og samstæðulyklar til viðbótar](../budgeting/consolidation-account-groups-consolidation-accounts.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
