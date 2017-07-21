---
title: "Bakfært gjald VSK | Microsoft Docs"
description: "Í þessu efnisatriði er fjallað um uppsetningu á bakfærðu gjaldi virðisaukaskatts (VSK) fyrir evrópsk lönd."
author: epodkolz
manager: AnnBe
ms.date: 05/12/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epodkolz
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 6cb473962f40ed9ef2f5f807f089098764f47009
ms.openlocfilehash: b3c94fa73410d9bdcaaec11dee04a7a239e4d45a
ms.contentlocale: is-is
ms.lasthandoff: 06/14/2017

---

# <a name="reverse-charge-vat"></a>Bakfærður VSK
Þetta efnisatriði lýsir almennri nálgun til að setja upp fyrir bakfært gjald virðisaukaskatts (VSK) fyrir evrópsk lönd.

Bakfært gjald er skattaskema sem flytur ábyrgðarsvið fyrir bókhald og skýrslugerð um VSK frá seljanda til kaupanda af vörum og/eða þjónustu. Þar af leiðandi tilkynna viðtakendur á vöru og/eða þjónustu bæði útskatt (í hlutverki seljanda) og innskatt (í hlutverki kaupanda) í VSK-skilum sínum.

Tilskipun Evrópusambandsins (ESB) lætur aðildarríkin ákveða hvernig þau aðlaga almennar þarfir við staðbundnar kröfur. Þar af leiðandi er skema fyrir bakfærð gjöld aðeins innleitt í sumum löndum fyrir sumar vörur og/eða þjónustu og það eru aukaleg skilyrði eða takmarknir á sölutölum. Ábyrgðarsvið fyrir VSK-greiðslu fer eftir stöðu birgis og kaupanda í öðrum löndum. Ef kaupandi er ábyrgur fyrir skil á vsk verður að taka það skýrt fam á reikningnum sem birgirnn gefur út. Til dæmis verður reikningurinn að innihalda orðin „Bakfært gjalds“ og þarf að tilgreina hvaða stöður eru undir skema bakfærðra gjalda. 

Til að nota bakfærð gjöld, verður að ljúka við eftirfarandi uppsetningu.

## <a name="set-up-sales-tax-codes"></a>Setja upp VSK-kóða
Mælt er með að nota sérstaka vsk-kóða fyrir innkaupaaðgerðir og söluaðgerðir.

<table>
<body>
<tr>
<td><strong>Kóði virðisaukaskatts fyrir sölu</strong></td>
<td>Stofna vsk-kóða fyrir söluaðgerðir bakfærðra gjalda (<strong>Skattur</strong> > <strong>Óbeinn skatta</strong> > <strong>vsk</strong> > <strong>Virðisaukaskattskóða</strong>).
</td>
</tr>
<tr>
<td><strong>VSK-kóði fyrir innkaup</strong></td>
<td><p>Stofna neikvæða og jákvæða vsk-kóða fyrir VSK bakfærð gjöld fyrir innkaup (<strong>Skattur</strong> > <strong>Óbeinir skattar</strong> > <strong>vsk</strong> > <strong>virðisaukaskattskóða</strong>).</p>
<ol>
<li>Stofna vsk-kóða sem hafa jákvætt gildi.</li>
<li>Stofna vsk-kóða sem hafa neikvætt gildi. Stilltu valkostinn <strong>Leyfa neikvæða vsk-prósentu</strong> á <strong>Já</strong>.
Það verður að úthluta neikvæðum VSK-kóða á VSK-flokk vöru og þeim VSK-flokki síðan úthlutað fyrir vörur sem falla undir bakfærðan VSK.</li>
</ol>
<p>Nánari upplýsingar má finna í næsta hluta, „Setja upp flokka VSK-kóða og VSK-flokka vöru.“</p>
</td>
</tr>
</tbody>
</table>

## <a name="set-up-sales-tax-groups-and-item-sales-tax-groups"></a>Setja upp VSK-flokka og VSK-flokka fyrir vörur
Mælt er með að nota sérstaka vsk-flokka fyrir innkaupaaðgerðir og söluaðgerðir.

<table>
<tr>
<td><strong>VSK-flokkar fyrir sölu</strong></td>
<td>Stofna vsk-flokka fyrir söluaðgerðir sem eru með bakfærðr gjöld (<strong>Skattur</strong> > <strong>Óbeinn skatta</strong> > <strong>vsk</strong> > <strong>Virðisaukaskattsflokkar</strong>). Á flipanum <strong>Uppsetning</strong> skal hafa með vsk-kóða fyrir bakfærð gjöld í þessum flokki. Veljið gátreitina <strong>Undanþegnar</strong> og <strong>Bakfært gjald</strong> fyrir vsk-kóða.</td>
</tr>
<tr>
<td><strong>VSK-flokkur fyrir innkaup</strong></td>
<td>Stofna vsk-flokka fyrir innkaupaaðgerðir sem eru með bakfærð gjöld (<strong>Skattur</strong> > <strong>Óbeinn skatta</strong> > <strong>vsk</strong> > <strong>Virðisaukaskattsflokkar</strong>). Á flipanum <strong>Uppsetning</strong> þarf að hafa með bæði neikvæða og jákvæða vsk-kóða í þessum flokki. Veljið gátreitinn <strong>Bakfært gjald</strong> fyrir vsk-kóðann sem hefur neikvætt gildi.</td>
</tr>
<tr>
<td><strong>VSK-flokkar vöru</strong></td>
<td>Stofna eða uppfæra vsk-flokk vöru með vsk-kóðann sem hefur neikvætt gildi (<strong>Skattur</strong> > <strong>Óbeinir skattar</strong> > <strong>vsk</strong> > <strong>VSK-flokkar vöru</strong>). Það verður að úthluta sjálfgefnum vsk-flokki vöru á vörur og efnisflokka sem falla undir bakfærslu.</td>
</tr>
</table>

## <a name="set-up-reverse-charge-groups"></a>Setja upp bakfærsluflokka
Á síðunni **Bakfærðuir vöruflokkar** (**Skattur** > **Uppsetning** > **VSK** > **Bakfærðir vöruflokkar**), er hægt að skilgreina flokka af vörum eða þjónustu, eða einstaka vöru eða þjónustu, sem bakfærsla getur átt við. Tilgreindu lista yfir vörur, vöruflokka og tegundir fyrir sölu og/eða innkaup fyrir hvern vöruflokk bakfærðra gjalda.

## <a name="set-up-reverse-charge-rules"></a>Setja upp bakfærslureglur
Á síðunni **Reglur um bakfærð gjöld** (**Skattur** > **Uppsetning** > **VSK** > **Reglur um bakfærð gjöld**), er hægt að skilgreina hvaða reglur gilda fyrir innkaup og sölu. Hægt er að skilgreina hóp af reglum um hæfi bakfærðra gjalda. Fyrir hverja reglu skal stilla eftirfarandi svæði:

- **Gerð skjals** – Veljið **Innkaupapöntun**, **reikningabók Lánardrottins**, **sölupöntun**, **textareikning**, **reikningabók Viðskiptavina**, og/eða **lánardrottinsreikning**.
- **Gerð lands/svæðis sem samstarfsaðila** – Veljið **Innanlands**, **ESB**, eða **Erlendir**. Einnig, ef reglan getur átt við allar skjalaflutningsaðferðir, án tillits til land eða svæði aðseturs þeirra, veljið **Allar**.
- **Innanlands afhendingaraðsetur** – Veljið þennan gátreit til að nota regluna á afhendingar í sama landi eða svæði. Ekki er hægt að velja þennan gátreit fyrir skjalagerðirnar **reikningabók Lánardrottins** og **reikningabók Viðskiptavina**.
- **Bakfærslugjald vöruflokks** – Veldu flokkinn sem hægt er að beita reglunni á.
- **Þröskuldsupphæðin** -Bakfærsluskemanu er beitt á reikninginn ef gildið af vörum eða þjónustu sem eru hafðar með í bakfærsluvöruflokki fer yfir þau mörk sem þú tilgreinir hér.

Hægt er að nota reitina **Gildisdagsetningu** og **Gildistíma** til að ákvarða það tímabil þegar reglan gildir.

Þar að auki er hægt að tilgreina hvort tilkynning birtist og skjalalínan er uppfærð með sjálfgefinni bakfærslugjaldi vsk-flokks ef skilyrði fyrir skjalið sem línan er uppfyllt. Eftirtaldir valkostir eru í boði:

- **Ekkert** -Skjalalínan er ekki uppfærð.
- **Kvaðning** – Tilkynning birtist til að staðfesta að hægt sé að nota fyrir bakfærslugjald.
- **Stilla** -Skjalalínan er uppfærð án aukatilkynningar.

## <a name="set-up-default-parameters"></a>Setja upp sjálfgefnar færibreytur
Til að virkja aðgerðir, á síðunni **fjárhagsfæribreytur** á flipanum **Bakfærður** skal stilla valkostinn **Virkja bakfærslugjald** á **Já**. Í reitunum **VSK-flokkur innkaupapöntunar** og **Skattflokkur VSK** skal velja sjálfgefinn vsk-flokka. Þegar hæfisskilyrði bakfærslugjalds eru uppfyllt er sölu- eða innkaupapöntunarlína uppfærð með þessum vsk-flokkum.

## <a name="reverse-charge-on-a-sales-invoice"></a>Bakfærslugjald á sölureikningi
Um sölu undir Bakfærð Gjöld skema rukkar seljandi ekki VSK. Þess í stað gefur reikningurinn upp bæði vörurnar sem falla undir bakfærðan VSK og heildarupphæð bakfærðs virðisaukaskatts.

Þegar sölureikningur er bókaður sem bakfærð gjöld hafa vsk-færslur skattastefnuna **Útskattur** og núll vsk og gátreiturinn **Bakfært gjald** er valinn.

## <a name="reverse-charge-on-a-purchase-invoice"></a>Bakfærslugjald á innkaupareikningi
Fyrir kaup undir Bakfærð Gjöld skema er kaupandi sem fær reikninginn sem er með bakfærðum gjöldum kaupandi og seljandi fyrir VSK-bókhald.

Þegar innkaupareikningur sem er með bakfærðum gjöldum er bókaður eru tvær vsk-færslur stofnaðar. Ein færsla er með skattastefnuna **Innskattur**. Hin færslan hefur skattstefnuna **Útskatt** og gátreiturinn **Bakfært gjald** valinn.

