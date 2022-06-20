---
title: Uppsetning vörusendingar
description: Þessi grein útskýrir hvernig á að nota birgðaferla sendingar á innleið.
author: yufeihuang
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ConsignmentDraftReplenishmentOrderJournal, ConsignmentProductReceiptLines, ConsignmentReplenishmentOrder, ConsignmentVendorPortalOnHand, InventJournalOwnershipChange, InventOnHandItemListPage, PurchTable, PurchTablePart, PurchVendorPortalConfirmedOrders, DirPartyTable, EcoResTrackingDimensionGroup, InventJournalName, InventOwner, InventTableInventoryDimensionGroups, VendTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 220834
ms.assetid: 3c9d6de4-45d4-459a-aef7-0d9ad2c22b3a
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 66215811c8c48412fb137967107abca3774f5f0c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872037"
---
# <a name="set-up-consignment"></a>Uppsetning vörusendingar

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir hvernig á að nota birgðaferla sendingar á innleið.

Vörusendingarbirgðir eru birgðir sem eru í eigu lánardrottinn en geymd á þínu svæði. Þegar þú ert tilbúinn að nota eða neyta birgða, tekurðu yfir eignarhald birgðanna. Þessi grein inniheldur upplýsingar um hvernig eigi að taka á móti birgðum í eigu lánardrottins á hendi án þess að stofna fjárhagsfærslur, hvernig eigi að hefja framleiðsluferli þar sem birgðahald í eigu lánardrottins er efnislega frátekið. og hvernig á að breyta eignarhaldi á hráefni til að vera fær um að vinna úr notkun sem hluta af vinnslu framleiðslupöntunar. Það er líka einhverjar upplýsingar um hvernig lánardrottinn getur fylgst notkun á birgðum þeirra með því að nota viðmót fyrir samstarf lánardrottna.

## <a name="overview-of-the-consignment-process"></a>Yfirlit yfir ferli vörusendingar

Í þessu dæmi hefur fyrirtækið USMF samkomulagi um vörusendingar við lánardrottinn US-104 fyrir hráefnið M9211CI.

1. Áfyllingarpöntun Vörusendingar er stofnaður handvirkt af einhverjum í USMF, miðað við áætlaða eftirspurn. Pöntun er stofnuð fyrir lánardrottinn US-104 og línu er bætt við fyrir vöru MS9211CI.
1. Lánardrottinn fær upplýsingar um áætlaða afhendingardagsetningu. Þetta getur gerst á þrjá vegu:
    - Einhver sem vinnur hjá USMF sendir upplýsingar um pöntun til lánardrottins.
    - Lánardrottinn getur einnig að fylgjast viðbúnum birgðum á lager með því að nota viðmót fyrir samstarf lánardrottna.
    - Einhver sem vinna hjá USMF síar gögn á **lagerbirgðir** síða til að sýna einungis færslur lánardrottins US-104, þar sem er staða innhreyfingar er **Pantað**, og sendir síðan þessar upplýsingar til lánardrottins.
1. Birgðum er afhent frá US-104 USMF.
1. Þegar efni berst USMF, er áfyllingarpöntun vörusendingar uppfærð með innhreyfingarskjal afurða. Aðeins efnislegu magni birgða á lager í eigu lánardrottins eru skráðar. Það eru engar færslur fjárhags stofnuð vegna þess að birgðum er enn í eigu lánardrottins.
1. Lánardrottinn fylgist með Uppfærslur í efnislegum lagerbirgðum með **vörusendingabirgðir á lager** síðu.
1. Þar sem efnislegar birgðir er á lager, tekur framleiðsluferli frá birgðir í eigu lánardrottins og hefur framleiðslupöntun fyrir fullunnin vara sem mun nota hráefni M9211CI.
1. Eigandi frátekins hráefnis sem á að nota í framleiðslu dagsins í dag er breytt úr US-104 í USMF. Þetta er gert með því að nota birgðabók eignarhaldsbreytingar. Þetta ferli stofnar innkaupapantanir þar sem **Uppruni** svæði er stillt á **Vörusendingar**.
1. Lánardrottins fylgist með notkun (eignarhaldsbreytingunni) á **Afurðirnar mótteknar frá vörusendingabirgðir** síðu og gefur út reikning á grunni samningar milli fyrirtækjanna tveggja.
1. Framleiðsluferli notar hráefni með tiltektarlista framleiðslu. Efnislegu frátekt uppfærist sjálfkrafa til að endurspegla að birgðir á lager er í eigu USMF.
1. Unnið er úr reikningi frá US-104 gagnvart innkaupapantanir sem voru mynduð sjálfkrafa þegar unnið var úr birgðabók eignarhaldsbreytinga. Gengið er frá greiðslu til lánardrottins US-104 fyrir birgðir sem var notað.

USMF framkvæmir viðbótar reglubundnar vinnslur:

- Efnislegar hreyfingar birgða í eigu lánardrottins milli mismunandi vöruhúsa eru unnar með flutningabók.
- Efnislegar lageribirgðir er uppfært með því að nota **vörutalningar** færslubók. Talning geta einnig notað af lánardrottins til að uppfæra lagerbirgðir, ef þeir hafa heimild til að gera þetta.

Lánardrottinn, US-104 getur fylgjast með uppfærslu með því að nota **vörusendingabirgðir á lager** síðuna.

## <a name="consignment-replenishment-orders"></a>Áfyllingarpantanir vörusendingar

Áfyllingarpöntun vörusendingar er skjal sem er notað til að biðja um og halda utan um birgðamagn afurða sem lánardrottinn ætlar að afhenda innan ákveðið tímabil með því að stofna pantaðar birgðafærslur. Yfirleitt, mun þetta byggjast á spá og raunveruleg eftirspurn tilteknar vörur. Birgðir sem tekið verður á móti gagnvart áfyllingarpöntun vörusendingar helst í eignarhaldi lánardrottins. Aðeins varsla afurða tengdar uppfærslu efnisleg innhreyfing er skráð og þar af leiðandi eiga sér ekki stað neinar uppfærslur á fjárhagsfærslum.

**Eigandi** víddin er notuð til að aðskilja upplýsingar um hvaða er í eigu lánardrottins og sem er í eigu lögaðila sem tekur á móti. Áfyllingarpöntunarlínur vörusendingar hafa stöðuna **Opin pöntun** eins lengi og heildarmagn lína hefur ekki verið móttekinn eða hætt við. Þegar allt magnið hefur verið tekið á móti eða afturkallaðar, er stöðunni breytt í **Lokið**. Efnislegar lagerbirgðir sem tengjast áfyllingarpöntun vörusendingar má skrá með skráningarferli sem og ferli fyrir uppfærslu innhreyfingarskjal afurða. Hægt að gera skráningu sem hluti af komuferli vöru eða með því að uppfæra pöntunarlínurnar handvirkt. Þegar Uppfærsluferli innhreyfingarskjals Afurða er notuð, er færsla gerð í færslubók innhreyfingarskjala afurða, sem er hægt að nota til að staðfesta móttöku á vörum til lánardrottna.

[![Áfyllingarpantanir vörusendingar.](./media/consignment-replenishment-order.png)](./media/consignment-replenishment-order.png)

## <a name="inventory-ownership-change-journal"></a>Færslubók eignarhaldsbreytingar birgða

**Birgðafærslubók fyrir breytingu á eignarhaldi** er notuð til að rekja flutninga á eignarhaldi vörusendingabirgða úr lánardrottni í núverandi lögaðila sem neytir þess. Ekki eru stofnaðar neinar væntanlegar birgðafærslur fyrir færslubókina. Eins og öllum birgðabók verður það að vera tilgreindur með heiti birgðabókar. Þessi nöfn eru stofnaðar á **heiti birgðabóka** síðuna og **færslubókargerð** verður að vera stillt á **breytingu á Eignarhaldi**.

Einu birgðafærslur sem eru stofnaðar eru þær sem tengjast bókaðri færslubók. Þegar búið er að bóka færslubókina:

- Birgðir í eigu lánardrottins er gefið út með því að nota **breytingu á Eignarhaldi** tilvísun með **Selt** stöðu.
- Lagerbirgðir er síðan móttekin af lögaðila sem notar þær með því að nota birgðafærsla með uppfærðu innhreyfingarskjal afurða á innkaupapöntun. Þetta stillir stöðuna á pöntuninni í **Móttekið**. Innkaupapantanir notaðar fyrir vörusendingar hafa **Uppruna** svæðið stillt á **Vörusendingar**.

Ekki er hægt að uppfæra magn í innkaupapöntunarlínum vörusendingar eftir að pöntun hefur verið stofnað.

[![Færslubók eignarhaldsbreytingar birgða.](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)

## <a name="vendor-collaboration-in-consignment-processes"></a>Samstarf lánardrottna í ferli vörusendingar

Ef lánardrottnana þínir nota viðmót fyrir samstarf lánardrottna, geta þeir nota þetta að vakta notkun á birgðum á þínu svæði. Viðmót samstarf lánardrottna er með þremur síður sem tengjast vinnslu vörusendingar á innleið:

- **Innkaupapantanir** **sem nota vörusendingabirgðir** - Sýnir nákvæmar upplýsingar um innkaupapöntun tengd eignarhaldsbreytingu úr ferli vörusendingar.
- **Afurðir mótteknar frá vörusendingabirgðum** -Sýnir upplýsingar um vörur og magn sem hefur innhreyfingar afurða uppfært á meðan stendur á ferli eignarhaldsbreytingar.
- **Vörusendingarbirgðir á lager** - Sýnir upplýsingar um vörurnar vörusendingar sem þeir áætlað að afhenda og vörurnar sem eru þegar efnislega tiltækt á svæði viðskiptavinar.

Nánari upplýsingar um uppsetningu á lánardrottnum til að nota samstarf lánardrottna er að finna í [Öryggi notanda í gátt lánardrottins](../procurement/configure-security-vendor-portal-users.md).

## <a name="inventory-owners"></a>Birgðaeigendur

Til að skrá efnislegar vörusendingabirgðir á innleið, þarf að skilgreina lánardrottinseiganda. Þetta er gert á **eigandi birgða** síðuna. Þegar velja **lánardrottnalykil** myndar þetta sjálfgefin gildi fyrir **Heiti** og **Eigandi** svæðum. Gildið í **Eiganda** svæði verður sýnilegt til lánadrottna, svo þú gætir viljað breyta þeim, ef nöfn á lánardrottnalykill eru ekki auðvelt fyrir utanaðkomandi fólki til að bera kennsl á. Mögulegt er að breyta á **Eigandi** svæði, en aðeins fram að þeim punkti þegar vista á **eigandi birgða** færslan. Í **Heiti** svæði er fyllt út með nafn þess aðila sem lánardrottnalykill er tengd við, og þessu er ekki hægt að breyta.

[![Birgðaeigendur.](./media/inventory-owners.png)](./media/inventory-owners.png)

## <a name="tracking-dimension-group"></a>Rakningarvíddarflokkur

Vörur sem nota á í ferli vörusendingar verður að tengjast við **rakningarvíddarflokkur** þar sem víddin **Eigandi** er stillt á **Virk**. Vídd eiganda hefur ávallt **Efnislegar birgðir** og **Fjárhagslegar birgðir** valkostir valinn. **Þekjuáætlun eftir vídd** er aldrei valin.

[![Rakningarvíddarflokkur.](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
