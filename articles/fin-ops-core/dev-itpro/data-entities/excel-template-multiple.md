---
title: Gagnasniðmát með mörgum vinnublöðum
description: Þetta efnisatriði lýsir því hvernig skal flytja gögn með því að nota Excel gagnaeiningasniðmát inn í Finance and Operations.
author: Sunil-Garg
ms.date: 01/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: 001795914c683a6182b885b79be7e225ad80e5cd
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750565"
---
# <a name="data-templates-with-multiple-worksheets"></a>Gagnasniðmát með mörgum vinnublöðum

[!include [banner](../includes/banner.md)]

Gagnastjórnun í forritinu styður sem byggjast á sniðmátum Microsoft Excel fyrir gagnaeiningar. Þessi sniðmát geta innihaldið einn eða fleiri vinnublöð. Sniðmát með mörgum vinnublöðum eru oft notaðar þegar auðvelt er að stýra gögnum í einni skrá og flytja hana inn í margar gagnaeiningar. Dæmi um þetta væri svæði og vöruhús.

## <a name="upload-a-file-once-and-map-it-to-all-entities"></a>Hlaða upp skrá einu sinni og varpa henni til allra eininga
Við skulum taka dæmi þar sem ein Excel-skrá með vinnublöðum sem kallast **Svæði** og **Vöruhús**. Til að setja upp gagnainnflutningsverkið myndir þú nýskrá fyrstu gagnaeininguna, **Svæði** og síðan hlaða upp skránni. Þú munt geta valið **Svæði** sem vinnublaðið sem verður notað fyrir þessa einingu.

Ef þú skráir til viðbótar aðra einingu **Vöruhús** án þess að fara úr **Bæta við skrá** skráarsniðinu, þá mun vinnublaðsleitin leyfa þér að velja vinnublaðið **Vöruhús** án þess að þurfa að hlaða skránni upp aftur. Eina ástæðan fyrir því að hlaða inn nýjum skrá væri ef **Vöruhús** gögnin voru í annarri skrá.

![Mörg vinnublöð](./media/AddFileMultipleWorkSheets.png)

## <a name="fix-worksheet-to-entity-mapping"></a>Festa vinnublað til einingarvörpunar

Vörpun vinnublaðsins til gagnaeiningar í innflutningsverkinu er hægt að festa frá hnitanetinu. **Vinnublað** dálkurinn í hnitanetinu sýnir vinnublaðið úr skránni sem var varpað. Þú getur valið annað vinnublað úr fellilistanum. Ef valið vinnublað er þegar varpað í einingu í gagnaverkinu biður kerfið þig um að staðfesta breytingarnar. Við mælum með að þú festir allar varpanir í hnitanetinu.

![Uppfæra vörpun vinnublaðs](./media/UpdateMappings.png)

## <a name="re-map-to-a-new-file"></a>Endurvarpa á nýja skrá

Í tilfellum þar sem ný útgáfa af sömu skrá eða algjörri nýju skrá verður að hlaða upp fyrir fyrirliggjandi einingar í gagnaverki, verður þú að nota **Bæta við skrá** upplifuninni og bæta einingunum við aftur eins og verið væri að setja þær inn í fyrsta sinn. Kerfið mun staðfesta að þú viljir skrifa yfir fyrirliggjandi einingar í gagnaverkinu áður en haldið er áfram. Einingar sem ekki er bætt við aftur (eða skrifað yfir) munu áfram halda fyrri vörpunum úr fyrri skrá.

## <a name="upload-a-file-using-run-project"></a>Hlaða upp skrá með því að nota Keyra verk

Þú getur hlaðið upp Excel-skrá meðan þú notar **Keyra verk** valmöguleikann til að framkvæma innflutningsverk. Þú verður að gæta þess að hlaða aðeins upp skrám sem eru með sömu vinnublaði og fyrirliggjandi varpanir á gagnaeiningarnar í gagnaverkinu. Ef vinnublað er ekki að finna í skránni sem nýlega var hlaðið upp, birtir kerfið villu og stoppar innflutning. Ef breyta verður vörpunin á vinnublaðið fyrir einingu, þá verður að uppfæra varpanirnar í gagnaverkinu fyrst innan frá gagnaverkinu, áður en þú notar skrána í **Keyra verk** upplifuninni.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]