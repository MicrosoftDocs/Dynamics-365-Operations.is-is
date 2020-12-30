---
title: Afturkalla pöntunaraðgerð á sölustað
description: Í þessu efnisatriði eru útskýrðir eiginleikar í boði fyrir bættar síður afturköllunar á pöntun á sölustað.
author: hhainesms
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 42b11ff16757d633b868dfdf248341193a44378f
ms.sourcegitcommit: 9c05d48f6e03532aa711e1d89d0b2981e9d37200
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/03/2020
ms.locfileid: "4665299"
---
# <a name="recall-order-operation-in-pos"></a>Afturkalla pöntunaraðgerð á sölustað

[!include [banner](includes/banner.md)]

Aðgerðin **Afturköllun pöntunar** á sölustað Commerce veitir uppfærða pöntunarleit og síunareiginleika og upplýsingar um tiltekna pöntun. Þessi eiginleiki er tiltækur í Commerce-útgáfum 10.0.15 og nýrri.

Til að virkja þessa virkni þarf að kveikja á eiginleikanum **Bætt afturköllunaraðgerð pöntunar á sölustað** á vinnusvæðinu **Eiginleikastjórnun** í Commerce Headquarters. Þegar búið er að virkja eiginleikann skal íhuga að uppfæra [skjáútlit](pos-screen-layouts.md) á sölustað til að nýta einhverjar af þessum breytingum.

Skilgreining á aðgerðarhnappnum **Endurkalla pöntun** gerir fyrirtækjum kleift að setja upp aðgerðina með fyrirframskilgreindri birtingu.

![Grunnstilling hnappahnits](media/recallorderbuttongrid.png)

Birtingarkostir eru eftirfarandi:
- **Ekkert** – Þessi valkostur setur upp aðgerðina án sérstakrar birtingar. Þegar notandi opnar aðgerðina með þessari skilgreiningu verða þeir beðnir um að leita og finna pantanir eða velja úr fyrirframskilgreindum pöntunarsíum.
- **Pantanir sem á að uppfylla** – Þegar notandi ræsir aðgerðina, keyrir fyrirspurn sjálfkrafa til að leita að og birta lista yfir pantanir sem á að uppfylla í versluninni. Þessar pantanir eru skilgreindar fyrir sótt í verslun eða sendingu úr verslun og línur þessara pantana hafa enn ekki verið teknar til eða pakkaðar.
- **Pantanir sem á að sækja** – Þegar notandi ræsir aðgerðina, keyrir fyrirspurn sjálfkrafa til að leita að og birta lista yfir pantanir sem eru skilgreindar að verði sóttar í verslun í núverandi verslun notandans.
- **Pantanir sem á að senda** – Þegar notandi ræsir aðgerðina, keyrir fyrirspurn sjálfkrafa til að leita að og birta lista yfir pantanir sem eru skilgreindar að verði sendar úr núverandi verslun notandans.

Þegar aðgerðin **Endurkalla pöntun** er ræst á sölustað, ef birtingin er stillt á **Ekkert**, getur notandi leitað að og sótt pantanir á einn af eftirfarandi hátt.
- Skanna strikamerki pöntunar. Þetta mun leita í reitum pöntunarnúmers, rásartilvísunar og innhreyfingarkennis að samsvörun.
- Veljið táknið **Leita að pöntunum** eða **Leita og sía** í AppBar til að nota síunaraðferðina til að hafa upp á pöntunum sem uppfylla síuskilyrðið.
- Velja skal úr forskilgreindri síu úr fellivalmyndinni **Sýna pantanir** (pantanir til að uppfylla, pantanir til að sækja eða pantanir til að senda).

![RecallOrderMainMenu](media/recallordermain.png)

Eftir að leitarskilyrði er notað, birtir forritið lista yfir samsvarandi sölupantanir.

![RecallOrderDetail](media/orderrecalldetail.png)

Notandi getur valið pöntun á listanum til að skoða frekari upplýsingar. Upplýsingaspjaldið hægra megin á skjánum sýnir atriði valdrar pöntunar, þ.m.t. upplýsingar pöntunarlínu, upplýsingar um afhendingu og upplýsingar um uppfyllingu.

Í AppBar getur notandi valið aðgerð. Það fer eftir stöðu pöntunarinnar hvort ákveðnar aðgerðir eru virkar eða ekki.

- **Skila** – Keyrir skil fyrir einn eða fleiri reikninga sem tengjast valinni pöntun viðskiptavinar.

- **Hætta við** – Gefa út fulla afturköllun á valinni sölupöntun.

- **Uppfylla** – Flytur notandann yfir á uppfyllingarsíðu pöntunar sem verður fyrirframsíuð fyrir valda pöntun. Aðeins pöntunarlínur sem verslun notanda má uppfylla fyrir valda pöntun eru sýndar.

- **Breyta** – Leyfir notendum að gera breytingar á valinni pöntun viðskiptavinar.

- **Taka til** – Ræsir tiltektarflæðið, sem gerir notandanum kleift að velja afurðirnar sem á að taka til og stofnar sölufærslu tiltektarinnar.
