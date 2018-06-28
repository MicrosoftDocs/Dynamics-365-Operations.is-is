---
title: "Uppfæra vöruhúsakerfis úr Microsoft Dynamics AX 2012 í Finance and Operations"
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e0ff3a22b89ce22096198d2e1dd1ea9ed10239a9
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---

# <a name="upgrade-warehouse-management-from-microsoft-dynamics-ax-2012-to-finance-and-operations"></a>Uppfæra vöruhúsakerfis úr Microsoft Dynamics AX 2012 í Finance and Operations


[!include [banner](../includes/banner.md)]

Þetta efnisatriði veitir yfirlit yfir uppfærsluferlið frá Microsoft Dynamics AX 2012 R3, sem keyrir WMSII-eininguna, í Microsoft Dynamics 365 for Finance and Operations.

Fjármál og Aðgerðum, ekki lengra styður í eldri **WMSII** kerfiseininguna úr Microsoft Dynamics AX 2012. Í staðinn er hægt að nota eininguna **Vöruhúsakerfi**. Í WMSII-einingunni var hægt að velja birgðavíddir staðsetningar og brettakennis fyrir fjárhagslegar birgðir, en þó er ekki hægt að nota birgðavíddir brettakennis fyrir fjárhagslegar birgðir í Finance and Operations.

Við uppfærslu eru allar vörur sem tengjast geymsluvíddarflokki sem notar birgðavíddir brettakennis auðkenndar, merktar sem útilokaðar, og ekki unnið úr til uppfærslu.

## <a name="upgrading-to-finance-and-operations-when-ax-2012-r3-wmsii-is-used"></a>Uppfærsluferli Fjármál og Aðgerðum, AX 2012 R3 WMSII sé notuð
Eftir uppfærsluna geturðu notað nokkra valkosti í skjámyndinni **Breyta geymsluvíddarflokki fyrir vörur** til að opna vörur sem voru útlokaðar meðan á uppfærslu stóoð og síðan vinna úr færslum fyrir þessar vörur.

### <a name="enabling-items-in-finance-and-operations"></a>Virkjun á vörum í Fjármál og Aðgerðir
Þessi breyting er nauðsynleg vegna þess að í Finance and Operations er vörurakning hluti af vöruhúsakerfisferlinu. Þessi ferli fyrir öll vöruhús og staðsetningar þeirra verður að tengja við forstillingu staðsetningu. Ef þú vilt nota vöruhúsakerfisferli verður eftirfarandi að vera stillt:
-   Fyrirliggjandi vöruhús verða að geta notað vöruhúsakerfisferla 
-   Fyrirliggjandi losaðar vörur verða að vera tengdar við geymsluvíddarflokk sem notar vöruhúsakerfisferla 

Ef uppruni geymsluvíddarflokka notar birgðavíddir brettakennis verður staðsetning núverandi lagerbirgða sem notaði birgðavíddir brettakennis að vera tengt við staðsetningarforstillingu þar sem færibreytan **Nota rakningu númeraplötu** er valin. Fyrirliggjandi vöruhúsum ætti ekki virkjaður nota vöruhús þjónustustýringar, hægt að breyta geymslu víddaflokkunum við birgðir á lager sem annast aðeins Setur, Vöruhús og Staðsetning birgðavíddir. 

> [!NOTE] 
>  Þú getur breytt geymslumvíddarflokknum fyrir vörur, jafnvel þó að opnar birgðafærslur séu til staðar.

## <a name="find-products-that-were-blocked-because-of-pallet-id"></a>Finna vörur sem var lokað á vegna brettakennis
Til að skoða lista yfir losaðar vörur sem voru lokaðar á meðan á uppfærslu stendur og ekki er hægt að vinna með því að smella á **Birgðastjórnun**&gt;**Uppsetningu**&gt;**Birgða**&gt;**læstar Vörur uppfærsla birgða**.

## <a name="change-storage-dimension-group-for-blocked-products"></a>Breyta geymsluvíddarflokki fyrir vörur sem er lokað á 
 
Til að nota sem hluta af vöruhúsakerfisferli verður vara að vera tengd við geymsluvíddarflokk þar sem birgðavíddir staðsetningar er virk og færibreytan **Nota vöruhúsakerfisferla** er valin. Þegar þessar stillingar eru valdar, Setur, Vöruhús, Birgðir stöðu, Staðsetningu og plate Leyfi birgðavíddir verði gerðar virkar.

Til að opna vörurnar sem voru lokaðar á meðan á uppfærslu stendur, verður að velja nýtt geymslu víddarflokk fyrir vörurnar. Athugið að hægt er að breyta geymslu vídd flokki jafnvel þó að opnar birgðafærslur eru til staðar. Til þess að vörurnar sem voru læst þegar uppfærsla er notuð, þarf tveir:

-   Breyta geymslu birgðavíddarflokk sem notar aðeins Setur, Vöruhús og Staðsetning birgðavíddir geymslu víddarflokki fyrir vöruna. Komið sem afleiðing þessari breytingu Brettakenni birgðavídd er ekki notuð lengur.
-   Breyta geymslu birgðavíddarflokk sem notar þjónustustýringar vöruhús geymslu víddarflokki fyrir vöruna. Komið sem afleiðing þessari breytingu birgðavídd Leyfi plate nú notuð.

## <a name="configure-warehouse-management-processes"></a>Stilla vöruhúsakerfisferla
Áður en hægt er að nota losa vöru í við **Vöruhúsastjórnun** einingunni sem vara verður að nota geymsluvídd flokka þar sem er **Nota þjónustustýringar vöruhús** færibreytan er valin.

### <a name="enable-warehouses-to-use-warehouse-management-processes"></a>Virkja vöruhús til þess að nota þjónustustýringar vöruhúss

1.  Stofna að minnsta kosti eina nýju staðsetningu reglu.
2.  Smellt er á **Vöruhúsastjórnun**&gt;**Uppsetningu**&gt;**Gera vöruhúsið þjónustustýringar**&gt;**Leyfa uppsetningu vöruhússins**.
3.  Á við **Leyfa uppsetningu vöruhússins** síðunni, bæta við vöruhús sem á að vera virkur. Hægt er að ljúka þessi skref á síðunni eða með því að nota samþætting við Microsoft Office.
4.  Tengið forstillingu staðsetningu allra staðsetninga. Auðveldlega er hægt að ljúka þessu skrefi með Microsoft Office samþættingu af síðunni. Hægt er að flytja og flytja inn gögn eða nota gögn skattaðilinn vinnslu í [gagnastjórnun](../../dev-itpro/data-entities/data-entities.md).
5.  Villuleita breytingarnar. Hluti af villuleit í mismunandi fjarvistarkóðann heilleiki eiga sér stað. Hluti af stærri uppfærsluferlið vandamál koma upp þurfi leiðrétt uppruna innleiðingar. Í þessu tilfelli viðbótar gagnauppfærslu þarf.
6.  Vinna breytingarnar.

### <a name="change-the-storage-dimension-group-for-items-so-that-it-uses-warehouse-management-processes"></a>Breyttu geymsluvíddarflokki fyrir vörur, svo að hún noti ferli vöruhúsakerfis

1.  Búa til nýtt **Birgða stöðu** gildi, og tengið það sem er **Sjálfgefin staða Verslunar** í í **Vöruhús færibreytur birgðastjórnunar** stillingar.
2.  Stofna nýjan víddaflokk geymslu þar sem það **Nota þjónustustýringar vöruhús** færibreytan er valin.
3.  Á við **Sendingarfrátekninga stigveldi** síðunni, tilgreinið nýja sendingarfrátekninga stigveldi samkvæmt geymslu vörunnar og rekja víddaflokka.
4.  Stofna eitt eða fleiri einingar lotunúmerið sem innihalda að minnsta kosti sama einingar sem notaðar eru til í birgðaeiningum.
5.  Smellt er á **Vöruhúsastjórnun**&gt;**Uppsetningu**&gt;**Gera vöruhúsið þjónustustýringar**&gt;**geymslu víddarflokk Breytingu vara**.
6.  Á við **geymslu víddarflokk Breytingu vara** síðunni, bæta við vörunúmer víddaflokkunum geymslu og einingu flokka númeraraða. Hægt er að ljúka þessi skref á síðunni með því að nota samþætting við Microsoft Office eða með því að nota einingu vinnslu gagna í [gagnastjórnun](../../dev-itpro/data-entities/data-entities.md).
7.  Villuleita breytingarnar. Hluti af villuleit í mismunandi fjarvistarkóðann heilleiki eiga sér stað. Hluti af stærri uppfærsluferlið vandamál koma upp þurfi leiðrétt uppruna innleiðingar. Í þessu tilfelli viðbótar gagnauppfærslu þarf.
8.  Vinna breytingarnar. Uppfærsla á allar birgðavíddir getur framkvæmt á meðan. Hægt að fylgjast með framvindu með vinnslum runuverk.

