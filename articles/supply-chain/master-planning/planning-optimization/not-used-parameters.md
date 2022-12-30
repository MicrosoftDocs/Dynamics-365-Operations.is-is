---
title: Færibreytur ekki notaðar af fínstillingu áætlanagerðar
description: Í þessari grein er að finna lista yfir færibreytur sem fínstilling skipulagningar tekur ekki til greina sem stendur meðan á aðgerð stendur.
author: t-benebo
ms.date: 09/02/2021
ms.topic: article
ms.search.form: ReqParameters, ReqGroup, ReqItemTable, ReqPlanSched, EcoResProductDetailsExtended, InventItemOrderSetup, WorkCalendarTable, PdsDispositionMaster
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-06-29
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: db8a8e929bf75c4d1dac0c1b0a7cbc848ff291a9
ms.sourcegitcommit: b3579ac62e1ea15664a114abcc2409cad76d4f19
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/14/2022
ms.locfileid: "9682669"
---
# <a name="parameters-not-used-by-planning-optimization"></a>Færibreytur ekki notaðar af fínstillingu áætlanagerðar

[!include [banner](../../includes/banner.md)]

Í þessari grein er að finna lista yfir færibreytur sem fínstilling skipulagningar tekur ekki til greina sem stendur meðan á aðgerð stendur. Þjónustuáætlun gæti sleppt færibreytu vegna þess að tengd virkni er til að mynda ekki studd. Að öðrum kosti gæti færibreytan hafa úrelst vegna breytinga á virkni.

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

## <a name="coverage-groups-page"></a>Síða þekjuflokka

Fínstilling skipulagningar notar ekki eftirfarandi færibreytur eða valkosti á síðunni **Þekjuflokkar**:

- Flýtiflipinn **Almennt**

  - **Jákvæðir dagar** – Gildið *Jákvæðir dagar* er ekki notað. Með fínstillingu áætlanagerðar eru jákvæðir dagar álitnir ótakmarkaðir.
  - **Nota lagerbirgðir** – Bíður stuðnings frá *Notkun lagerbirgða*.
  - **Nota tilgreinda uppskriftar- eða formúluútgáfu** – Bíður stuðnings frá *Formúluútgáfur með auka-/hliðarafurðum*.
  - **Nota tilgreinda leiðarútgáfu** – Bíður stuðnings frá *Eftirspurn með tiltekna kröfu uppskriftar eða leiðar skilgreinda*.


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

- Flipinn **Afhendingartími**:

  - **Innkaupatími** – Í útgáfum af þjónustu fínstillingar áætlanagerðar sem eru eldri en 6. ágúst 2021 notar fínstilling áætlanagerðar þessar færibreytur til að reikna út rétta pöntun og afhendingardagsetningar, en hún vistar ekki reiknaða afhendingartíma í áætlaðri pöntun. Í síðari útgáfum notar þjónustan einnig reiknaðan afhendingartíma til að stilla reitinn **Afhendingartími** og valkostinn **Vinnudagar** eins og krafist er fyrir viðkomandi áætlaða pöntun.
  - **Framleiðslutími** – Í útgáfum af þjónustu fínstillingar áætlanagerðar sem eru eldri en 6. ágúst 2021 notar fínstilling áætlanagerðar þessar færibreytur til að reikna út rétta pöntun og afhendingardagsetningar, en hún vistar ekki reiknaða afhendingartíma í áætlaðri pöntun. Í síðari útgáfum notar þjónustan einnig reiknaðan afhendingartíma til að stilla reitinn **Afhendingartími** og valkostinn **Vinnudagar** eins og krafist er fyrir viðkomandi áætlaða pöntun.
  - **Flutningstími** – Í útgáfum af þjónustu fínstillingar áætlanagerðar sem eru eldri en 6. ágúst 2021 notar fínstilling áætlanagerðar þessar færibreytur til að reikna út rétta pöntun og afhendingardagsetningar, en hún vistar ekki reiknaða afhendingartíma í áætlaðri pöntun. Í síðari útgáfum notar þjónustan einnig reiknaðan afhendingartíma til að stilla reitinn **Afhendingartími** og valkostinn **Vinnudagar** eins og krafist er fyrir viðkomandi áætlaða pöntun.
  - **Vinnudagar** – Í útgáfum af þjónustu fínstillingar áætlanagerðar sem eru eldri en 6. ágúst 2021 notar fínstilling áætlanagerðar þessar færibreytur til að reikna út rétta pöntun og afhendingardagsetningar, en hún vistar ekki reiknaða afhendingartíma í áætlaðri pöntun. Í síðari útgáfum notar þjónustan einnig reiknaðan afhendingartíma til að stilla reitinn **Afhendingartími** og valkostinn **Vinnudagar** eins og krafist er fyrir viðkomandi áætlaða pöntun.

## <a name="master-plans-page"></a>Síða aðaláætlana

Fínstilling skipulagningar notar ekki eftirfarandi færibreytur eða valkosti á síðunni **Aðaláætlanir**:

- Flýtiflipinn **Almennt**

  - **Hnekkja lagerbirgðum** – Bíður stuðnings frá *Notkun lagerbirgða*.
  - **Nota lagerbirgðir** – Bíður stuðnings frá *Notkun lagerbirgða*.
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
  - **Reiknaðar seinkanir** – Bíður frekari stuðnings frá *Reiknaðar seinkanir*.
  - **Röðun** – Bíður stuðnings frá *Framleiðslu*.

- Flýtiflipinn **Reiknaðar seinkanir**:

  - **Tryggja að áætlaðar pantanir séu ekki stofnaðar fyrir keyrsludagsetningu aðaláætlanagerðar** – Bíður stuðnings frá *Reiknaðar seinkanir*.
  - **Bæta við reiknaðri seinkun á dagsetningu þarfa** (í hlutanum **Áætlaðar innkaupapantanir**) – Bíður stuðnings frá *Reiknaðar seinkanir*.
  - **Bæta við reiknaðri seinkun á dagsetningu þarfa** (í hlutanum **Áætlaðar framleiðslupantanir**) – Bíður stuðnings frá *Reiknaðar seinkanir*.
  - **Bæta við reiknaðri seinkun á dagsetningu þarfa** (í hlutanum **Áætlaður flutningur**) – Bíður stuðnings frá *Reiknaðar seinkanir*.
  - **Bæta við reiknaðri seinkun á dagsetningu þarfa** (í hlutanum **Áætlað kanban**) – Bíður stuðnings frá *Reiknaðar seinkanir*.

- Flýtiflipinn **Aðgerðaboð**:

  - **Uppfæra frestaða dagsetningu sem þarfadagsetningu** - Þessari færibreytu er hætt fínstillingu áætlanagerðar.

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

- Flýtiflipinn **Innkaupapöntun**:

  - **Afhendingartími innkaupa** – Í útgáfum af þjónustu fínstillingar áætlanagerðar sem eru eldri en 6. ágúst 2021 notar fínstilling áætlanagerðar þessar færibreytur til að reikna út rétta pöntun og afhendingardagsetningar, en hún vistar ekki reiknaða afhendingartíma í áætlaðri pöntun. Í síðari útgáfum notar þjónustan einnig reiknaðan afhendingartíma til að stilla reitinn **Afhendingartími** og valkostinn **Vinnudagar** eins og krafist er fyrir viðkomandi áætlaða pöntun.
  - **Vinnudagar** – Í útgáfum af þjónustu fínstillingar áætlanagerðar sem eru eldri en 6. ágúst 2021 notar fínstilling áætlanagerðar þessar færibreytur til að reikna út rétta pöntun og afhendingardagsetningar, en hún vistar ekki reiknaða afhendingartíma í áætlaðri pöntun. Í síðari útgáfum notar þjónustan einnig reiknaðan afhendingartíma til að stilla reitinn **Afhendingartími** og valkostinn **Vinnudagar** eins og krafist er fyrir viðkomandi áætlaða pöntun.

- Flýtiflipinn **Birgðir**:

  - **Stýring afhendingardagsetninga** – Fínstilling skipulagningar styður ekki valkostinn *CTP*, bíður stuðnings frá *CTP*.
  - **Afhendingartími birgða** – Í útgáfum af þjónustu fínstillingar áætlanagerðar sem eru eldri en 6. ágúst 2021 notar fínstilling áætlanagerðar þessar færibreytur til að reikna út rétta pöntun og afhendingardagsetningar, en hún vistar ekki reiknaða afhendingartíma í áætlaðri pöntun. Í síðari útgáfum notar þjónustan einnig reiknaðan afhendingartíma til að stilla reitinn **Afhendingartími** og valkostinn **Vinnudagar** eins og krafist er fyrir viðkomandi áætlaða pöntun.
  - **Vinnudagar** – Í útgáfum af þjónustu fínstillingar áætlanagerðar sem eru eldri en 6. ágúst 2021 notar fínstilling áætlanagerðar þessar færibreytur til að reikna út rétta pöntun og afhendingardagsetningar, en hún vistar ekki reiknaða afhendingartíma í áætlaðri pöntun. Í síðari útgáfum notar þjónustan einnig reiknaðan afhendingartíma til að stilla reitinn **Afhendingartími** og valkostinn **Vinnudagar** eins og krafist er fyrir viðkomandi áætlaða pöntun.

## <a name="batch-disposition-master-page"></a>Síða aðalrunuráðstöfunar

Fínstilling skipulagningar notar ekki eftirfarandi færibreytu á síðunni **Aðalrunuráðstöfun**:

- Flýtiflipinn **Uppsetning**:

  - **Nettó** – Bíður stuðnings frá *Ráðstöfunarkóðar runu*.
 
