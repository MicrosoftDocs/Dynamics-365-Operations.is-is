---
title: "Flytja vörur og vöruhúsakerfi úr AX 2012 í Finance and Operations"
description: "Í þessu efnisatriði er að finna yfirlit yfir vörur og valkosti flutnings vöruhúsastjórnunar."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventLocationWHSProcessEnablement, WHSLocationProfile, InventTableStorageDimensionGroupChange, InventUpdateBlockedItem, WHSParameters, WHSReservationHierarchy, WHSUOMSeqGroupTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 1714054
ms.assetid: 79a1a3b9-3a36-4162-8839-ec39b5e26602
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 92d0b4dd9611de4d717f30dc8736c673835bea29
ms.contentlocale: is-is
ms.lasthandoff: 03/26/2018

---

# <a name="migrate-products-and-warehouse-management-from-ax-2012-to-finance-and-operations"></a>Flytja vörur og vöruhúsakerfi úr AX 2012 í Finance and Operations

[!INCLUDE [banner](../includes/banner.md)]

Í þessu efnisatriði er að finna yfirlit yfir flutningsvalkosti vöru- og vöruhúsastjórnunar innan Microsoft Dynamics 365 for Finance and Operations.

<a name="introduction"></a>Inngangur
------------

Vörur eru við uppfærslu á Fjármál og Aðgerðir læstar ef þeir tengjast geymslu víddaflokki með stillingum sem ekki stemma kröfur vídd flokki geymslustillingum Fjármál og Aðgerða. Hins vegar eftir uppfærslu, er hægt að nota safn yfirfærslna valkosti í í **geymslu víddarflokk Breytingu vara** til að opna vörurnar sem voru lokaðar á meðan á uppfærslu stendur. Síðan er hægt að vinna færslur fyrir þessar vörur. Sumar þessara vörurnar gæti þegar verið tengd við víddaflokkunum geymslu þar sem Setur, Vöruhús og Staðsetning birgðavíddir eru virk og efnislega rakin. Í þessu tilfelli er hægt að nota í **geymslu víddarflokk Breytingu vara** stendur til að virkja þær vörur sem nota á í þjónustustýringar vöruhús. Þessi aðgerð er gagnleg ef óskað er að nota aðgerða námskeiðsstjórnunar vöruhús fyrir núverandi vöru.

## <a name="upgrading-to-finance-and-operations-when-ax-2012-r3-wmsii-is-used"></a>Uppfærsluferli Fjármál og Aðgerðum, AX 2012 R3 WMSII sé notuð
Fjármál og Aðgerðum, ekki lengra styður í eldri **WMSII** kerfiseininguna úr Microsoft Dynamics AX 2012. Í staðinn er hægt að nota nýju **Vöruhúsastjórnun** kerfi. Í fyrri útgáfum væri að velja birgðavíddir Staðsetning og Brettakenni fyrir fjárhagslegra birgða. Hins vegar sem hluti af uppfærsluferlinu Brettakenni birgðavídd er ekki lengur að virkja til fjárhagslegra birgða. Allar vörur sem tengjast geymslu birgðavíddarflokk sem notar birgðavídd Brettakenni verði að loka og won't unnin.

### <a name="enabling-items-in-finance-and-operations"></a>Virkjun á vörum í Fjármál og Aðgerðir

Fjármál Aðgerða, og vörurnar sem verður notuð sem hluti af þjónustustýringar vöruhús verður að tengja við geymsluvídd flokka þar sem það **Nota þjónustustýringar vöruhús** færibreytan er valin. Þegar þessar stillingar eru valdar, Setur, Vöruhús, Birgðir stöðu, Staðsetningu og plate Leyfi birgðavíddir verði gerðar virkar. Hægt er að breyta þessari gerð geymslu víddarflokki fyrir vörur sem eru þegar tengdar víddaflokkunum geymslu þar sem Staðsetning birgðavídd er virk.

### <a name="items-that-are-blocked-for-inventory-updates"></a>Vörur sem eru lokaðar fyrir birgðauppfærslur

Til að skoða lista yfir losaðar vörur sem voru lokaðar á meðan á uppfærslu stendur og ekki er hægt að vinna með því að smella á **Birgðastjórnun**&gt;**Uppsetningu**&gt;**Birgða**&gt;**læstar Vörur uppfærsla birgða**.

### <a name="reapplying-blocked-products"></a>Reapplying læstar vörur

Til að opna vörurnar sem voru lokaðar á meðan á uppfærslu stendur, verður að velja nýtt geymslu víddarflokk fyrir vörurnar. Athugið að hægt er að breyta geymslu vídd flokki jafnvel þó að opnar birgðafærslur eru til staðar. Til þess að vörurnar sem voru læst þegar uppfærsla er notuð, þarf tveir:

-   Breyta geymslu birgðavíddarflokk sem notar aðeins Setur, Vöruhús og Staðsetning birgðavíddir geymslu víddarflokki fyrir vöruna. Komið sem afleiðing þessari breytingu Brettakenni birgðavídd er ekki notuð lengur.
-   Breyta geymslu birgðavíddarflokk sem notar þjónustustýringar vöruhús geymslu víddarflokki fyrir vöruna. Komið sem afleiðing þessari breytingu birgðavídd Leyfi plate nú notuð.

### <a name="migration-processes"></a>Yfirfærsluferli

Fjármál Aðgerða, og rekja vara er hluti af þjónustustýringar vöruhús. Þessi ferli fyrir öll vöruhús og staðsetningar þeirra verður að tengja við forstillingu staðsetningu. Conceptually, eigi að nota þjónustustýringar vöruhús tvær ferli þarf að meðhöndla:

-   Fyrirliggjandi vöruhús verður að vera virkjað til að nota vöruhúsakerfisferli.
-   Fyrirliggjandi losaðar vörur verður að tengja við nýjan geymslu víddaflokk sem notar þjónustustýringar vöruhús.

Ef uppruni víddaflokkunum geymslu Brettakenni birgðavídd er staðsetningar fyrirliggjandi lagerbirgða sem birgðavídd Brettakenni verða að tengjast forstillingu staðsetningu þar sem á **Nota leyfi plate rakningu** færibreytan er valin. Fyrirliggjandi vöruhúsum ætti ekki virkjaður nota vöruhús þjónustustýringar, hægt að breyta geymslu víddaflokkunum við birgðir á lager sem annast aðeins Setur, Vöruhús og Staðsetning birgðavíddir.

### <a name="using-the-warehouse-management-processes"></a>Notkun á ferlum vöruhúsakerfis

Áður en hægt er að nota losa vöru í við **Vöruhúsastjórnun** einingunni sem vara verður að nota geymsluvídd flokka þar sem er **Nota þjónustustýringar vöruhús** færibreytan er valin.

#### <a name="enable-warehouses-to-use-warehouse-management-processes"></a>Virkja vöruhús til þess að nota þjónustustýringar vöruhúss

1.  Stofna að minnsta kosti eina nýju staðsetningu reglu.
2.  Smellt er á **Vöruhúsastjórnun**&gt;**Uppsetningu**&gt;**Gera vöruhúsið þjónustustýringar**&gt;**Leyfa uppsetningu vöruhússins**.
3.  Á við **Leyfa uppsetningu vöruhússins** síðunni, bæta við vöruhús sem á að vera virkur. Hægt er að ljúka þessi skref á síðunni eða með því að nota samþætting við Microsoft Office.
4.  Tengið forstillingu staðsetningu allra staðsetninga. Auðveldlega er hægt að ljúka þessu skrefi með Microsoft Office samþættingu af síðunni. Hægt er að flytja og flytja inn gögn eða nota gögn skattaðilinn vinnslu í [gagnastjórnun](../../dev-itpro/data-entities/data-entities.md).
5.  Villuleita breytingarnar. Hluti af villuleit í mismunandi fjarvistarkóðann heilleiki eiga sér stað. Hluti af stærri uppfærsluferlið vandamál koma upp þurfi leiðrétt uppruna innleiðingar. Í þessu tilfelli viðbótar gagnauppfærslu þarf.
6.  Vinna breytingarnar.

#### <a name="change-the-storage-dimension-group-for-items-so-that-it-uses-warehouse-management-processes"></a>Breyttu geymsluvíddarflokki fyrir vörur, svo að hún noti ferli vöruhúsakerfis

1.  Búa til nýtt **Birgða stöðu** gildi, og tengið það sem er **Sjálfgefin staða Verslunar** í í **Vöruhús færibreytur birgðastjórnunar** stillingar.
2.  Stofna nýjan víddaflokk geymslu þar sem það **Nota þjónustustýringar vöruhús** færibreytan er valin.
3.  Á við **Sendingarfrátekninga stigveldi** síðunni, tilgreinið nýja sendingarfrátekninga stigveldi samkvæmt geymslu vörunnar og rekja víddaflokka.
4.  Stofna eitt eða fleiri einingar lotunúmerið sem innihalda að minnsta kosti sama einingar sem notaðar eru til í birgðaeiningum.
5.  Smellt er á **Vöruhúsastjórnun**&gt;**Uppsetningu**&gt;**Gera vöruhúsið þjónustustýringar**&gt;**geymslu víddarflokk Breytingu vara**.
6.  Á við **geymslu víddarflokk Breytingu vara** síðunni, bæta við vörunúmer víddaflokkunum geymslu og einingu flokka númeraraða. Hægt er að ljúka þessi skref á síðunni með því að nota samþætting við Microsoft Office eða með því að nota einingu vinnslu gagna í [gagnastjórnun](../../dev-itpro/data-entities/data-entities.md).
7.  Villuleita breytingarnar. Hluti af villuleit í mismunandi fjarvistarkóðann heilleiki eiga sér stað. Hluti af stærri uppfærsluferlið vandamál koma upp þurfi leiðrétt uppruna innleiðingar. Í þessu tilfelli viðbótar gagnauppfærslu þarf.
8.  Vinna breytingarnar. Uppfærsla á allar birgðavíddir getur framkvæmt á meðan. Hægt að fylgjast með framvindu með vinnslum runuverk.



