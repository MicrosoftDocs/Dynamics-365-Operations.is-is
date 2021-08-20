---
title: Færibreytur ekki notaðar af fínstillingu skipulagningar
description: Í þessu efnisatriði er að finna lista yfir færibreytur sem fínstilling skipulagningar tekur ekki til greina sem stendur meðan á aðgerð stendur.
author: crytt
ms.date: 6/29/2021
ms.topic: article
ms.search.form: ReqParameters, ReqGroup, ReqItemTable, ReqPlanSched, EcoResProductDetailsExtended, InventItemOrderSetup, WorkCalendarTable, PdsDispositionMaster
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-06-29
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 1992523ae10f30196ebe55d7c7fe6a2549a3a12853da261bd4a129523b8e4ea2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6714284"
---
# <a name="parameters-not-used-by-planning-optimization"></a>Færibreytur ekki notaðar af fínstillingu skipulagningar

[!include [banner](../../includes/banner.md)]

Í þessu efnisatriði er að finna lista yfir færibreytur sem fínstilling skipulagningar tekur ekki til greina sem stendur meðan á aðgerð stendur. Þjónustuáætlun gæti sleppt færibreytu vegna þess að tengd virkni er til að mynda ekki studd. Að öðrum kosti gæti færibreytan hafa úrelst vegna breytinga á virkni.

Eftirfarandi hlutar telja upp þær breytur sem fínstilling skipulagningar notar ekki á tilteknum síðum. Þeir útskýra einnig hvers vegna hver færibreyta er ekki notuð.

## <a name="master-planning-parameters-page"></a>Færibreytusíða aðaláætlanagerðar

Fínstilling áætlanagerðar notar ekki eftirfarandi færibreytur eða valkosti á síðunni **Færibreytur aðaláætlanagerðar**:

- Flipinn **Almennt**:

    - **Núgildandi spáráætlun** – Bíður stuðnings *Spár*.
    - **Núgildandi föst aðaláætlun** – Bíður stuðnings frá *Afrita fasta áætlun yfir í breytilega áætlun*.
    - **Núgildandi breytileg aðaláætlun** – Bíður stuðnings frá *Afrita breytilega áætlun yfir í breytilega áætlun*.
    - **Afrita allt og uppfæra fasta aðaláætlun í breytilega aðaláætlun** – Bíður stuðnings frá *Afrita fasta áætlun yfir í breytilega áætlun*.
    - **Upphafstími fyrir útreikning seinkana** – Bíður stuðnings frá *Reiknaðar seinkanir*.
    - **Nota breytilega neikvæða daga** – Fínstilling skipulagningar notar alltaf nálgunina *Nota breytilega neikvæða daga*.
    - **Dagatal dagsins í dag** – Bíður stuðnings frá *Röðun*.
    - **Notkun skyndiminnis** – Skilgreiningin á Microsoft Azure áskriftinni meðhöndlar afkastapunkta.
    - **Fjöldi verka í hjálparverkbúnti** – Skilgreining Azure-áskriftar meðhöndlar afkastapunkta.
    - **Forvinnsla: Sía sjálfkrafa eftir atriðum með beinni eftirspurn** – Skilgreining Azure-áskriftar meðhöndlar afkastapunkta.
    - **Eftirvinnsla: Sía sjálfkrafa eftir atriðum með beinni eftirspurn** – Skilgreining Azure-áskriftar meðhöndlar afkastapunkta.
    - **Fjöldi pantana í staðfestingarbúnti** – Skilgreining Azure-áskriftar meðhöndlar afkastapunkta.
    - **Fjöldi þráða** – Skilgreining Azure-áskriftar meðhöndlar afkastapunkta.
    - **Tímalokun áætlunarferlis í mínútum** – Skilgreining Azure-áskriftar meðhöndlar afkastapunkta.
    - **Áætlun upphafstíma** – Bíður stuðnings frá *Áætlanagerð*.

- Flipinn **Áætlaðar pantanir**:

    - **Móttökutími** – Bíður stuðnings frá *Áætlanagerð*.
    - **Framleiðsla** – Bíður stuðnings frá *Áætlanagerð*.
    - Reitir í hlutanum **Verkefni** – Bíður stuðnings frá *Áætlanagerð*.

- Flipinn **Stöðluð uppfærsla**:

    - **Uppfæra merkingu** – Bíður stuðnings frá *Staðfesting*.
    - **Rjúfa staðfestingu ef villa kemur upp** – Bíður stuðnings frá *Staðfestingu*.
    - **Flokka eftir lánardrottni** – Bíður stuðnings frá *Staðfestingu*.
    - **Flokka eftir kaupendaflokki** – Bíður stuðnings frá *Staðfestingu*.
    - **Flokka eftir innkaupasamningi** – Bíður stuðnings frá *Staðfestingu*.
    - **Flokka eftir tímabili** – Bíður stuðnings frá *Staðfestingu*.
    - **Finna innkaupasamning** – Bíður stuðnings frá *Staðfestingu*.
    - **Flokka eftir forgangi í áætlunargerð** – Bíður stuðnings frá *Staðfestingu*.
    - **Flokka eftir tímabili** – Bíður stuðnings frá *Staðfestingu*.

## <a name="coverage-groups-page"></a>Síða þekjuflokka

Fínstilling skipulagningar notar ekki eftirfarandi færibreytur eða valkosti á síðunni **Þekjuflokkar**:

- Flýtiflipinn **Almennt**

    - **Jákvæðir dagar** – Bíður stuðnings frá *Jákvæðum dögum*.
    - **Nota lagerbirgðir** – Bíður stuðnings frá *Notkun lagerbirgða*.
    - **Nota tilgreinda uppskriftar- eða formúluútgáfu** – Bíður stuðnings frá *Formúluútgáfur með auka-/hliðarafurðum*.
    - **Nota tilgreinda leiðarútgáfu** – Bíður stuðnings frá *Eftirspurn með tiltekna kröfu uppskriftar eða leiðar skilgreinda*.

- Flýtiflipinn **Aðgerð**:

    - **Aðgerðarboð** – Bíður stuðnings frá *Aðgerðum*.
    - **Tímamörk aðgerðar** – Bíður stuðnings frá *Aðgerðum*.
    - **Fresta álagningu** – Bíður stuðnings frá *Aðgerðum*.
    - **Flýta fyrir álagningu** – Bíður stuðnings frá *Aðgerðum*.
    - **Grunndagsetning** – Bíður stuðnings frá *Aðgerðum*.
    - **Flýta fyrir** – Bíður stuðnings frá *Aðgerðum*.
    - **Fresta** – Bíður stuðnings frá *Aðgerðum*.
    - **Minnka** – Bíður stuðnings frá *Aðgerðum*.
    - **Hækka** – Bíður stuðnings frá *Aðgerðum*.
    - **Afleiddar aðgerðir** – Bíður stuðnings frá *Aðgerðum*.

- Flýtiflipinn **Annað**:

    - **Frysta tímamörk (í dögum)** – Stuðningurinn *Frysta tímamörk* er ekki áætlaður í fínstillingu skipulagningar.
    - **Tímamörk niðurbrots uppskriftar (dagar)** – Bíður stuðnings frá *Áætlanagerð*.
    - **Tímamörk áætlaðrar afkastagetu (dagar)** – Bíður stuðnings frá *Áætlanagerð*.
    - **Samþykkt tímamörk beiðni (dagar)** – Bíður stuðnings frá *Beiðni*.
    - **Tímamörk spáráætlunar** – Bíður stuðnings frá *Spá*.

- Flýtiflipinn **Seinkanir**:

    - **Reiknaðar seinkanir** – Bíður stuðnings frá *Reiknaðar seinkanir*.
    - **Tímamörk útreiknaðra seinkana (dagar)** – Bíður stuðnings frá *Reiknaðar seinkanir*.

## <a name="item-coverage-page"></a>Síða vöruþekju

Fínstilling skipulagningar notar ekki eftirfarandi færibreytur eða valkosti á síðunni **Vöruþekja**:

- Flipinn **Almennt**:

    - **Gerð áætlaðrar pöntunar** – Fínstilling skipulagningar styður ekki valkost *kanban*, bíður stuðnings frá *Kanban*.
    - **Frysta tímamörk (í dögum)** – Stuðningurinn *Frysta tímamörk* er ekki áætlaður í fínstillingu skipulagningar.
    - **Tímamörk niðurbrots uppskriftar (dagar)** – Bíður stuðnings frá *Áætlanagerð*.
    - **Tímamörk áætlaðrar afkastagetu (dagar)** – Bíður stuðnings frá *Áætlanagerð*.
    - **Samþykkt tímamörk beiðni (dagar)** – Bíður stuðnings frá *Beiðni*.
    - **Uppfylla lágmarkskröfur** – Fínstilling skipulagningar styður ekki valkostina *Dagurinn í dag*, *Fyrsta útgáfa* og *Þekjutímamörk*. Hún notar alltaf valkostinn *Dagurinn í dag + öflunartími*.
    - **Lágmarkstímabil** – Bíður stuðnings frá *Lágmarksbirgðastigi*.
    - **Áætlunarformúla** – Bíður stuðnings frá *Formúluútgáfur með auka-/hliðarafurðir*.
    - **Sjálfgefinn forgangur** – Bíður stuðnings frá *Formúluútgáfur með auka-/hliðarafurðir*.
    - **Núverandi forgangur** – Bíður stuðnings frá *Formúluútgáfur með auka-/hliðarafurðir*.
    - **Dagsetningu breytt** – Bíður stuðnings frá *Formúluútgáfur með auka-/hliðarafurðir*.
    - **Nota lagerbirgðir** – Bíður stuðnings frá *Notkun lagerbirgða*.

## <a name="master-plans-page"></a>Síða aðaláætlana

Fínstilling skipulagningar notar ekki eftirfarandi færibreytur eða valkosti á síðunni **Aðaláætlanir**:

- Flýtiflipinn **Almennt**

    - **Hafa með lagerbirgðir** – Bíður stuðnings frá *Notkun lagerbirgða*.
    - **Hnekkja lagerbirgðum** – Bíður stuðnings frá *Notkun lagerbirgða*.
    - **Nota lagerbirgðir** – Bíður stuðnings frá *Notkun lagerbirgða*.
    - **Taka með birgðafærslur** – Bíður stuðnings frá *Notkun lagerbirgða*.
    - **Hafa sölutilboð með** – Bíður stuðnings frá *Sölutilboðum*.
    - **Hafa með tilboðsbeiðni** – Bíður stuðnings frá *Tilboðsbeiðni*.
    - **Nota endingartíma** – Bíður stuðnings frá *Endingartíma*.
    - **Taka með samfelldniáætlun** – Bíður stuðnings frá *Samfelldniáætlunargerð*.
    - **Aðferð áætlanagerðar** – Bíður stuðnings frá *Áætlanagerð*.
    - **Takmarkaður eiginleiki** – Bíður stuðnings frá *Áætlanagerð*.
    - **Tímamörk afkastagetu fyrir röðun afturábak** – Bíður stuðnings frá *Áætlanagerð*.
    - **Takmörkuð geta** – Bíður stuðnings frá *Áætlanagerð*.
    - **Tímamörk takmarkaðrar getu** – Bíður stuðnings frá *Áætlanagerð*.
    - **Takmörkuð geta fyrir flöskuhálstilföng** – Bíður stuðnings frá *Áætlanagerð*.
    - **Tímamörk afkastagetu fyrir flöskuhálstilföng** – Bíður stuðnings frá *Áætlanagerð*.
    - **Áætlaðar pantanir** – Fínstilling skipulagningar notar fastar númeraraðir.
    - **Lota** – Fínstilling skipulagningar notar fastar númeraraðir.
    - **Samfelldniáætlun** – Fínstilling skipulagningar notar fastar númeraraðir.

- Flýtiflipinn **Tímamörk í dögum**:

    - **Frysta** – Stuðningurinn *Frysta tímamörk* er ekki áætlaður í fínstillingu skipulagningar.
    - **Niðurbrot** – Bíður stuðnings frá *Áætlanagerð*.
    - **Spáráætlun** – Bíður frekari stuðnings *Spár*.
    - **Geta** – Bíður stuðnings frá *Áætlanagerð*.
    - **Samfelldniáætlun** – Bíður stuðnings frá *Samfelldniáætlunargerð*.
    - **Aðgerðarboð** – Bíður stuðnings frá *Aðgerðum*.
    - **Reiknaðar seinkanir** – Bíður frekari stuðnings frá *Reiknaðar seinkanir*.
    - **Röðun** – Bíður stuðnings frá *Framleiðslu*.

- Flýtiflipinn **Reiknaðar seinkanir**:

    - **Tryggja að áætlaðar pantanir séu ekki stofnaðar fyrir keyrsludagsetningu aðaláætlanagerðar** – Bíður stuðnings frá *Reiknaðar seinkanir*.
    - **Bæta við reiknaðri seinkun á dagsetningu þarfa** (í hlutanum **Áætlaðar innkaupapantanir**) – Bíður stuðnings frá *Reiknaðar seinkanir*.
    - **Bæta við reiknaðri seinkun á dagsetningu þarfa** (í hlutanum **Áætlaðar framleiðslupantanir**) – Bíður stuðnings frá *Reiknaðar seinkanir*.
    - **Bæta við reiknaðri seinkun á dagsetningu þarfa** (í hlutanum **Áætlaður flutningur**) – Bíður stuðnings frá *Reiknaðar seinkanir*.
    - **Bæta við reiknaðri seinkun á dagsetningu þarfa** (í hlutanum **Áætlað kanban**) – Bíður stuðnings frá *Reiknaðar seinkanir*.

- Flýtiflipinn **Röðun**:

    - **Raðaðar áætlaðar pantanir eftir áætlanagerð** – Bíður stuðnings frá *Röðun*.
    - **Rammagerð** – Bíður stuðnings frá *Röðun*.
    - **Tímabilsgerð** – Bíður stuðnings frá *Röðun*.
    - **Fjöldi ramma í herferðartímabili** – Bíður stuðnings frá *Röðun*.

## <a name="released-product-details-page"></a>Upplýsingasíða um losaðar afurðir

Fínstilling skipulagningar notar ekki eftirfarandi færibreytu eða valkost á síðunni **Upplýsingar um losaðar afurðir**:

- Flýtiflipinn **Hönnuður**:

    - **Gerð framleiðslu** – Fínstilling skipulagningar styður ekki valkostinn *Áætlunarvara*, bíður stuðnings frá *Áætlunarvörum*.

## <a name="default-order-settings-page"></a>Síða sjálfgefinna pöntunarstillinga

Fínstilling skipulagningar notar ekki eftirfarandi færibreytu eða valkost á síðunni **Sjálfgefnar pöntunarstillingar**:

- Flýtiflipinn **Birgðir**:

    - **Stýring afhendingardagsetninga** – Fínstilling skipulagningar styður ekki valkostinn *CTP*, bíður stuðnings frá *CTP*.

## <a name="working-time-calendars-page"></a>Síða vinnutímadagatala

Fínstilling skipulagningar notar ekki eftirfarandi færibreytu á síðunni **Vinnutímadagatöl**:

- **Grunndagatal** – Bíður stuðnings frá *Grunndagatölum*.

## <a name="batch-disposition-master-page"></a>Síða aðalrunuráðstöfunar

Fínstilling skipulagningar notar ekki eftirfarandi færibreytu á síðunni **Aðalrunuráðstöfun**:

- Flýtiflipinn **Uppsetning**:

    - **Nettó** – Bíður stuðnings frá *Ráðstöfunarkóðar runu*.