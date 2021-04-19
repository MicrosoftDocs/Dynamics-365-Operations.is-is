---
title: Afturkalla pöntunaraðgerð á sölustað
description: Í þessu efnisatriði eru útskýrðir eiginleikar í boði fyrir bættar síður afturköllunar á pöntun á sölustað.
author: hhainesms
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 2f7ad4f53917bb607afe84a2c457518c3f8f7a08
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799107"
---
# <a name="recall-order-operation-in-pos"></a>Afturkalla pöntunaraðgerð á sölustað

[!include [banner](includes/banner.md)]

Aðgerðin **Afturköllun pöntunar** á sölustað Commerce veitir uppfærða pöntunarleit og síunareiginleika og upplýsingar um tiltekna pöntun. Þessi eiginleiki er tiltækur í Commerce-útgáfum 10.0.15 og nýrri.

Til að virkja þessa virkni þarf að kveikja á eiginleikanum **Bætt afturköllunaraðgerð pöntunar á sölustað** á vinnusvæðinu **Eiginleikastjórnun** í Commerce Headquarters. Þegar búið er að virkja eiginleikann skal íhuga að uppfæra [skjáútlit](pos-screen-layouts.md) á sölustað til að nýta einhverjar af þessum breytingum.

Skilgreining á aðgerðarhnappnum **Endurkalla pöntun** gerir fyrirtækjum kleift að setja upp aðgerðina með fyrirframskilgreindri birtingu.

![Grunnstilling hnappahnits](media/recallorderbuttongrid.png)

Birtingarkostir eru eftirfarandi:
- **Ekkert** – Þessi valkostur setur upp aðgerðina án sérstakrar birtingar. Þegar notandi opnar aðgerðina með þessari skilgreiningu verða þeir beðnir um að leita og finna pantanir eða velja úr fyrirframskilgreindum pöntunarsíum.
- **Pantanir sem á að uppfylla** – Þegar notandi ræsir aðgerðina, keyrir fyrirspurn sjálfkrafa til að leita að og birta lista yfir pantanir sem á að uppfylla í verslun notandans. Þessar pantanir eru skilgreindar fyrir sótt í verslun eða sendingu úr verslun og línur þessara pantana hafa enn ekki verið teknar til eða pakkaðar.
- **Pantanir sem á að sækja** – Þegar notandi ræsir aðgerðina, keyrir fyrirspurn sjálfkrafa til að leita að og birta lista yfir pantanir sem eru skilgreindar að verði sóttar í verslun í núverandi verslun notandans.
- **Pantanir sem á að senda** – Þegar notandi ræsir aðgerðina, keyrir fyrirspurn sjálfkrafa til að leita að og birta lista yfir pantanir sem eru skilgreindar að verði sendar úr núverandi verslun notandans.

Þegar aðgerðin **Endurkalla pöntun** er ræst á sölustað, ef birtingin er stillt á **Ekkert**, getur notandi leitað að og sótt pantanir á einn af eftirfarandi hátt.
- Skanna strikamerki pöntunar. Þetta mun leita í reitum pöntunarnúmers, rásartilvísunar og innhreyfingarkennis að samsvörun.
- Veljið táknið **Leita að pöntunum** eða **Leita og sía** í AppBar til að nota síunaraðferðina til að hafa upp á pöntunum sem uppfylla síuskilyrðið.
- Velja skal úr forskilgreindri síu úr fellivalmyndinni **Sýna pantanir** (pantanir til að uppfylla, pantanir til að sækja eða pantanir til að senda).

![RecallOrderMainMenu](media/recallordermain.png)

Eftir að leitarskilyrði er notað, birtir forritið lista yfir samsvarandi sölupantanir. Mikilvægt er að hafa í huga að þegar leitar-/síuvalkostir eru notaðir þurfa sóttar pantanir ekki að vera pantanir sem tengdar eru við núverandi verslun notanda. Þetta leitarferli mun sækja og sýna allar pantanir viðskiptavina sem passa við leitarskilyrðið jafnvel þótt pöntunin hafi verið stofnuð eða stillt á að vera uppfyllt af annarri verslun/rás eða staðsetningu vöruhúss.

![RecallOrderDetail](media/orderrecalldetail.png)

Notandi getur valið pöntun á listanum til að skoða frekari upplýsingar. Upplýsingaspjaldið hægra megin á skjánum sýnir atriði valdrar pöntunar, þ.m.t. upplýsingar pöntunarlínu, upplýsingar um afhendingu og upplýsingar um uppfyllingu.

Í AppBar getur notandi valið aðgerð. Það fer eftir stöðu pöntunarinnar hvort ákveðnar aðgerðir eru virkar eða ekki.

- **Skil** – Hefjið ferlið við að stofna skil fyrir einhverja reikningsfærða afurð í valdri pöntun viðskiptavinar.

- **Hætta við** – Gefa út fulla afturköllun á valinni sölupöntun. Þessi valkostur verður ekki í boði fyrir pantanir sem settar eru í gang í gegnum símaversrás og er ekki hægt að nota til að hætta við pöntun að hluta til.

- **Uppfylla** – Flytur notandann yfir á uppfyllingarsíðu pöntunar sem verður fyrirframsíuð fyrir valda pöntun. Aðeins pöntunarlínur sem verslun notanda má uppfylla fyrir valda pöntun eru sýndar.

- **Breyta** – Leyfir notendum að gera breytingar á valinni pöntun viðskiptavinar. Pantanir eru aðeins breytilegar í [ákveðnum aðstæðum](customer-orders-overview.md#edit-an-existing-customer-order).

- **Sótt** – Þessi valkostur verður í boði ef pöntunin er með eina eða fleiri línur úthlutaðar sem sóttar í núverandi verslun notanda. Þessi aðgerð ræsir tiltektarflæðið, sem gerir notandanum kleift að velja afurðirnar sem á að taka til og stofnar sölufærslu tiltektarinnar.

## <a name="add-notifications-to-the-recall-order-operation"></a>Bæta tilkynningum við endurköllunaraðgerð pöntunar

Í útgáfu 10.0.18 og nýrri er hægt að skilgreina tilkynningar sölustaðar og viðvaranir virkra reita fyrir aðgerðina **Endurköllun pöntunar** ef þess er óskað. Frekari upplýsingar er að finna í [Sýna pöntunartilkynningar á sölustað (POS)](notifications-pos.md).  

[!INCLUDE[footer-include](../includes/footer-banner.md)]
