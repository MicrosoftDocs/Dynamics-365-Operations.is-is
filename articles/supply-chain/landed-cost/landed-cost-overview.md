---
title: Eining heildarkostnaðar
description: Eining heildarkostnaðar hjálpar fyrirtækjum að einfalda sendingaraðgerðir á innleið með því að veita notendum fulla stjórn á fjárhag og vörum fyrir innflutta farma, frá framleiðanda til vöruhúss.
author: Weijiesa
ms.date: 12/07/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: aa6f3baf6e6d980ac3c15e2045d1fcdef08ec296
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/04/2022
ms.locfileid: "8694628"
---
# <a name="landed-cost-module"></a>Eining heildarkostnaðar

[!include [banner](../../includes/banner.md)]

Einingin **Heildarkostnaður** hjálpar fyrirtækjum að einfalda sendingaraðgerðir á innleið með því að veita notendum fulla stjórn á fjárhag og vörum fyrir innflutta farma, frá framleiðanda til vöruhúss. Fyrir innfluttar vörur getur heildarkostnaður verið 40 prósent eða meira af samtals kostnaði hverrar innfluttrar vöru. Því er áskorun að leggja fram nákvæmt mat á heildarkostnaði.

Fyrirtæki geta notað heildarkostnað til að ljúka eftirfarandi verkum:

- Áætla heildarkostnað á þeim tíma þegar verið er að stofna ferð.
- Skiptið heildarkostnaði niður á margar vörur og innkaupapantanir eða flutningspantanir í einni ferð.
- Styðja við flutning á vörum á milli efnislegra staðsetninga með því að sjá heildarkostnað.
- Sjá uppsöfnun fyrir vörur í flutningi.

Heildarkostnaður býður upp á nákvæmt og tímanlegt kostnaðarmat fyrir sameiginlegan kostnað í heildarkostnaði. Á sama tíma veitir það aukinn fjárhagslegan og skiplagðan sýnileika í framlengdri aðfangakeðju. Það hjálpar einnig að draga úr stjórnun kostnaðar og kostnaðarvillum.

## <a name="highlights"></a>Hápunktar

### <a name="voyages"></a>Ferðir

Í heildarkostnaði er ferð ákveðin hreyfing frá út-staðsetningu, í gegnum tiltekna áfangastaða yfir tiltekið tímabil, til tiltekinnar staðsetningar í vöruhúsi á innleið. Hægt er að bæta innkaupapöntunum og pöntunarlínum við annaðhvort einn gám eða marga gáma fyrir ferð og kostnaðinum verður úthlutað á réttan hátt aftur í vörulínuna. 

### <a name="item-ownership"></a>Vörueignarréttur

Í Microsoft Dynamics 365 Supply Chain Management eru vörur venjulega mótteknar á viðtökustað vöruhúss og síðan reikningsfærðar. Samkvæmt flestum alþjóðlegum viðskiptasamningum tekur fyrirtæki hins vegar við eignarhaldi á vörum frá þeim tíma þegar þær fara frá upprunalegri höfn, áður en þær hafa verið efnislega mótteknar. Heildarkostnaður gerir fyrirtækjum klieft að reikningsfæra vörur áður en þær hafa verið efnislega mótteknar. Þetta hugtak er þekkt sem pöntun vara í flutningi. Það býr til nýja gerð pöntunar til að stjórna móttöku á vörum eftir að upprunaleg innkaupapöntun hefur verið reikningsfærð.

### <a name="costs"></a>Kostnaður

Þegar þú stofnar ferð í heildarkostnaði er hægt að bæta kostnaði sjálfkrafa við hann. Þessi kostnaður er settur upp í heildarkostnaði og ýmsir valmöguleikar kostnaðar og kostnaðargrunnar eru í boði fyrir hann. Hægt er að setja upp hvern kostnað fyrir mismunandi stig ferðar og skipta honum niður á vörustigið í gegnum reglur um skiptingar sem styðja magn, rúmmál, þyngd, upphæð og skilgreinda deila rúmmálsmælingar. Þessi áætlaði kostnaður gefur rétt mat á öllum kostnaði fyrir ferð.

Heildarkostnaður keyrir síðan bráðabirgðabókun/-uppsöfnun á áætluðum heildarkostnaði til að ganga úr skugga um að nákvæmur útreikningur á áætluðum kostnaði sé gefinn upp þegar ferð er stofnuð. Þegar þessi sjálfvirki kostnaður er reikningsfærður, er áætlaður kostnaður bakfærður og honum skipt út fyrir raunverulegan kostnað samkvæmt kostnaðarreikningum.

Raunkostnaður er bakfærður áætlaður kostnaður sem er bókaður þegar kostnaður er reikningsfærður með því að nota millilykla sem eru settir upp fyrir hverja kostnaðargerð (t.d. toll, farm og tryggingu). Þessar bókanir fylgja bókunarhegðuninni sem tengist tiltekinni vöru. Þær uppfæra birgðirbókun sjálfkrafa burtséð frá því hvort bókunargerðin sé fyrst inn, fyrst út (FIFO), síðast inn, síðast út (LIFO), hlaupandi vegið meðaltal eða hlaupandi meðaltal. Allar bókunargerðir birgðalíkanaflokka eru studdar. Fyrir hlaupandi meðaltal og bókun staðlaðs kostnaðar eru frávikslyklar innkaupaverðs í boði til að bóka mismuninn á milli áætlaðs kostnaðar og raunkostnaðar.

### <a name="item-and-order-tracking"></a>Vöru- og pöntunarrakning

Þar sem ferð fer frá upprunalegri út-staðsetningu og til vöruhúss á áfangastað, geta notendur uppfært hvert skref, eða *legg*, ferðarinnar eftir þörfum. Fyrir hvern legg er afhendingartími og sendingarstaða auðkennd. Staðfestar afhendingardagsetningar fyrir flutning yfir á næsta legg ferðarinnar eru einnig auðkenndar. Saman gefa þessar afhendingardagsetningar áætlaða afhendingardagsetningu á vörum í vöruhús á innleið. Notendur geta breytt þessum afhendingardagsetningum. Í þessu tilfelli er áætlaður afhendingardagur varanna þá uppfærðu sjálfkrafa út frá afhendingartímunum og leggjum ferðarinnar. Sýnileiki á vörum í flutningi eftir ferð og skipi er í boði fyrir hvern gám fyrir sig áður en vörurnar eru mótteknar. Vegna þess að dagsetningarnar eru uppfærðar fyrir hverja innkaupapöntunarlínu fyrir sig, er vörustjórnun og áætlanagerð vöruhúss betri í fyrirtækinu.

## <a name="landed-cost-concepts"></a>Hugtök heildarkostnaðar

Eftirfarandi tafla tekur saman nokkur hugtök varðandi Heildarkostnað.

| Hugtak | lýsing |
|---|---|
| Ferð | Yfirleitt er ferð eitt skip. Það fer hins vegar eftir starfsvenjum og ferlum hvort það sé einn lánardrottin eða ein innkaupapöntun. Engar takmarkanir eru á notkun þessa hugtaks. |
| Fólíó | Fólíó er oft ákvarðað samkvæmt tollreglugerðum. Það getur innihaldið eina vöru lánardrottins fyrir eina einingu/fyrirtæki fyrir hverja sendingu. Vörur í fólíói geta verið í einum gámi eða mörgumgámum. |
| Gámur | Gámar geyma innkaupapantanalínur. Þeir eru stigi fyrir neðan sendingarstigið. Þeir eru notaðir ef kostnaður vara skiptist eftir gámi eða ef móttöku er lokið á hvern gám. |
| Gámagerð | Gerðir gáma geta ákvarðað verð fyrir kostnaðargerð (til dæmis, farmur). Þær veita einnig gagnlegar sendingarupplýsingar. |
| Kostnaðargerð | Kostnaðargerðir auðkenna kostnað sem tengist innflutningi, svo sem tolli, farmi eða tryggingu. |
| Sjálfvirkur kostnaður | Sjálfvirkur kostnaður virkar eins og viðskiptasamningar. Sjálfvirkur kostnaður er tengdur við stig ferðar. |
| Afh.staður | Hafnir eru svæði þar sem tekið er við vörum og þær fluttar annað. |
| Skip | Samgöngutæki er miðillinn sem er notaður til að flytja vörur, svo sem skip eða flugvél. |
| Vörur í flutningi | Það fer eftir stillingunum hvernig gengið er frá vörum í flutningsvöruhúsi eftir að reikningur er uppfærður. |
| Aðgerð | Hægt er að nota aðgerðir til að vista öll mikilvæg skref ferðarinnar á milli tveggja hafna. Hægt er að nota þetta til að uppfæra dagsetningar. |
| Sniðmát ferðar | Sniðmát ferða eru leiðir sem vörur fara á milli tveggja hafna. |

Til að bera saman hugtök og eiginleika eininganna **Heildarkostnaður** og **Flutningsstjórnun (TMS)** skal skoða [Heildarkostnaður í samanburði við flutningsstjórnun](landed-cost-vs-tms.md).
