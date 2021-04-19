---
title: Fyrirspurnir um heildarkostnað
description: Þetta efnisatriði lýsir því hvernig á að finna og nota ýmsar gerðir fyrirspurna sem eru í boði fyrir Heildarkostnaður eininguna.
author: sherry-zheng
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMLine, ITMItemTracking, ITMContainerActivityTracking, ITMContainerTracking
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-21
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 22a2e76780adb43b053b6cf7fd08411a4a60aeac
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823362"
---
# <a name="landed-cost-inquiries"></a>Fyrirspurnir um heildarkostnað

[!include [banner](../../includes/banner.md)]

## <a name="voyage-line-inquiries"></a>Fyrirspurnir um ferðalínur

Fyrirspurnin um **Línur ferðar** sýnir allar línur ferðar sem snerta birgðir. Hægt er að nota þessa fyrirspurn sem síu til að fá aðstoð við að finna vöru, innkaupapöntun eða aðrar gagnlegar upplýsingar. Einnig er hægt að nota hana til að auðkenna væntanlegan afhendingardag vöru sem kann að vera á einni eða fleiri ferðum. Á þennan hátt getur hún auðveldað umsjón með væntanlegri móttöku birgða.

Til að opna þessa fyrirspurn skal fara í **Heildarkostnaður \> Fyrirspurnir \> Línur ferðar**.

### <a name="overview-tab"></a>Yfirlitsflipi

Flipinn **Yfirlit** á fyrirspurnarsíðu fyrir **Línur ferðar** inniheldur hnitanet sem sýnir grunnupplýsingar um hverja ferðalínu sem á við. Eftirfarandi tafla lýsir dálkunum í hnitanetinu.

| Dálkur | lýsing |
|---|---|
| **Vörunúmer** | Vara fyrir ferðalínu. |
| **Tilvísun** | Gerð pöntunar (innkaupapöntun eða flutningspöntun). |
| **Númer** | Númer innkaupapöntunar eða flutningspöntunar. |
| **Fólíó** | Fólíóið sem tengist ferðalínunni. |
| **Gámur** | Gámurinn sem tengist ferðalínunni. |
| **Ferð** | Ferðin sem tengist ferðalínunni. |
| **Magn** | Magn vörunnar fyrir ferðalínuna. |
| (Aðrar víddir) | Hægt er að sýna dálka fyrir fleiri víddir eftir þörfum. Þær víddir fela í sér rununúmer, birgðastöðu og vöruhús. Á aðgerðasvæðinu skal velja **Birgðir \> Sýna víddir** til að opna svarglugga þar sem hægt er að velja víddirnar sem á að hafa með. |

### <a name="general-tab"></a>Almennt

Veljið flipann **Almennt** til að skoða frekari upplýsinga um línuna sem er valin í flipanum **Yfirlit**.

### <a name="dimensions-tab"></a>Flipinn Víddir

Veljið flipann **Víddir** til að skoða gildi fyrir allar tiltækar víddir fyrir línuna sem er valin í flipanum **Yfirlit** óháð því hvaða víddir hafa verið valdar til að koma fram í þeim flipa.

## <a name="cost-estimate-inquiries"></a>Fyrirspurnir um kostnaðarmat

Í hvert skipti sem kostnaðarmat er útbúið er því bætt við fyrirspurnarsíðuna **Kostnaðarmat**. Fyrir ítarlegar upplýsingar um hvernig á að útbúa, skoða og vinna með kostnaðarmat (þ.m.t. mat á fyrirspurnarsíðunni) skal skoða [Áætla og stjórna heildarkostnaði](estimate-manage-landed-costs.md).

## <a name="item-tracking"></a>Vörurakning

Notið síðuna **Vörurakning** til að skoða opnar innkaupapöntunarlínur og núverandi stöðu þeirra. Línur þurfa ekki að tengjast ferð til að birtast hér. Ef vara tengist hins vegar ferð sýnir færslulína vörurakningar kenni ferðarinnar.

Til að opna þessa síðu skal fara á **Heildarkostnaður \> Fyrirspurnir \> Rakning \> Vörurakning**.

Þar sem kerfið inniheldur líklega mjög mikinn fjölda innkaupapöntunarlína sýnir síðan **Vörurakning** í upphafi engar færslur. Byrjið á því að nota síureitina sem eru efst á síðunni til að skilgreina safn innkaupapöntunarlína sem leitað er að. Síðan skal velja **Uppfæra** á aðgerðasvæðinu til að búa til listann. Hægt er að nota stjörnu (\*) sem algildistaf í hvaða síureit sem er. Til dæmis til að finna allar innkaupapöntunarlínur fyrir vörur sem innihalda orðið „DVD“ í heiti sínu skal stilla reitinn **Gerð** á **Afurðarheiti** og færa inn *\*DVD\** í reitinn **Reitargildi**.

> [!NOTE]
> Sem stendur innihalda biðpantanir eingöngu sölupantanir. Sölutilboð eru ekki birt eða litið á þær sem biðpantanir.

Eftirfarandi tafla lýsir dálkum í hnitanetinu á síðunni **Vörurakning**.

| Dálkur | lýsing |
|---|---|
| **Til hafnar** | Lokaáfangastaðurinn. |
| **Staðfest** | Staðfest dagsetning innkaupapöntunarlínunnar. |
| **Afhendingardagur** | Afhendingardagsetning innkaupapöntunarlínunnar. |
| **Ferð** | Ef lína tengist ferð, auðkenni ferðar. |
| **Gámur** | Ef lína er hengd við gám, auðkenni gáms. |
| **Afhendingarhöfn** | Núverandi höfn samkvæmt fyrsta leggnum í skjámynd rakningar þar sem engin raunveruleg dagsetning er stillt fyrir gáminn sem tengist innkaupapöntunarlínunni. |
| **Aðgerð** | Núverandi verkþáttur samkvæmt fyrsta leggnum í skjámynd rakningar þar sem engin raunveruleg dagsetning er stillt fyrir gáminn sem tengist innkaupapöntunarlínunni. |
| **Áætluð lokadagsetning** | Dagsetningin þegar búist er við að ferðin verði móttekin í vöruhúsi á áfangastað. |
| **Nafn** | Nafn lánardrottins. |
| **Staða ferðar** | Staða ferðar sem er hengd við innkaupapöntunarlínuna. |
| **Vörunúmer** | Vörunúmer innkaupapöntunarlínunnar. |
| **Ytri** | Vörunúmer lánardrottins. |
| **Vöruheiti** | Heiti vörunnar fyrir innkaupapöntunarlínuna. |
| **Magn** | Magn innkaupapöntunarlínu fyrir innkaupapöntunarlínuna. |
| **Eining** | Mælieining innkaupapöntunarlínunnar. |
| **Tilvísun** | Gerð pöntunar (innkaupapöntun eða flutningspöntun) |
| **Númer tilvísunar** | Númer innkaupapöntunar eða flutningspöntunar. |
| **Biðpöntun** | Tákn gefur til kynna að það séu sölubiðpantanir fyrir vöruna. |
| (Aðrar víddir) | Hægt er að sýna dálka fyrir fleiri víddir eftir þörfum. Þær víddir fela í sér rununúmer, birgðastöðu og vöruhús. Á aðgerðasvæðinu skal velja **Sýna víddir** til að opna svarglugga þar sem hægt er að velja víddirnar sem á að hafa með. |

### <a name="related-information-about-backorders"></a>Tengdar upplýsingar um biðpantanir

Til að skoða frekari upplýsingar um biðpantanir skal velja flipann **Tengdar upplýsingar** hægra megin á síðunni og síðan velja **Biðpantanir**. Til að skoða enn meiri upplýsingar um tiltekna biðpöntun skal velja línu fyrir hana og síðan velja tengilinn **Meira**.

## <a name="individual-shipping-container-tracking"></a>Rakning á stökum gámum

Fyrirspurn um **Rakningu á stökum gámum** býður upp á síu sem gerir kleift að finna gám og síðan bera kennsl á allar ferðalínur þess gáms.

Til að opna þessa fyrirspurn skal fara í **Heildarkostnaður \> Fyrirspurnir \> Rakning \> Rakning á stökum gámum**.

## <a name="multiple-shipping-container-tracking"></a>Rakning margra gáma

Fyrirspurn um **Rakningu á mörgum gámum** býður upp á síu sem gerir kleift að finna safn af gámum og síðan bera kennsl á allar ferðalínur þessara gáma.

Til að opna þessa fyrirspurn skal fara í **Heildarkostnaður \> Fyrirspurnir \> Rakning \> Rakning margra gáma**.
