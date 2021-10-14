---
title: Samstilla vinnupantanir úr Field Service við sölupantanir í Supply Chain Management
description: Þetta efnisatriði fjallar um sniðmát og undirliggjandi verk sem eru notuð til að samstilla vinnupantanir í Field Service við sölupantanir í Supply Chain Management.
author: Henrikan
ms.date: 04/09/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: henrikan
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: c54f5eaec1ae453ba9e55ef54d47c8591276ec89
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7568376"
---
# <a name="synchronize-work-orders-in-field-service-to-sales-orders-in-supply-chain-management"></a>Samstilla vinnupantanir úr Field Service við sölupantanir í Supply Chain Management

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Þetta efnisatriði fjallar um sniðmát og undirliggjandi verk sem eru notuð til að samstilla vinnupantanir í Dynamics 365 Field Service við sölupantanir í Dynamics 365 Supply Chain Management.

[![Samstilling viðskiptaferla milli Supply Chain Management og Field Service.](./media/field-service-integration.png)](./media/field-service-integration.png)


## <a name="templates-and-tasks"></a>Sniðmát og verkefni

Eftirfarandi sniðmát og undirliggjandi verk eru notuð til að keyra samstillingu vinnupantana í Field Service við sölupantanir í Supply Chain Management.

### <a name="names-of-the-templates-in-data-integration"></a>Heiti sniðmátanna í gagnasamþættingu

Sniðmátið **Vinnupantanir til sölupantana (Field Service til Supply Chain Management)** er notað til að keyra samstillingu.

### <a name="names-of-the-tasks-in-the-data-integration-project"></a>Heiti verksins í gagnasamþættingarverki

- WorkOrderHeader
- WorkOrderServiceLineEstimate
- WorkOrderServiceLineUsed
- WorkOrderProductLineEstimate
- WorkOrderProductLineUsed

Eftirfarandi samstillingarverkefni eru nauðsynleg áður en samstillingar við sölureikningshausa og línur geta átt sér stað:

- Vöruþjónustuvörur (Supply Chain Management til Field Service)
- Lyklar (Sales til Supply Chain Management) - Beint

## <a name="entity-set"></a>Einingastamstæða

| **Field Service** | **Birgðakeðjustjórnun** |
|-------------------------|-------------------------|
| msdyn_workorders        | Dataverse hausar sölupöntunar |
| msdyn_workorderservices | Dataverse sölupöntunarlínur   |
| msdyn_workorderproducts | Dataverse sölupöntunarlínur   |

## <a name="entity-flow"></a>Einingaflæði

Vinnapantanir eru búnar til í Field Service. Ef vinnupantanirnar innihalda aðeins utanaðkomandi afurðir og ef gildið **Staða vinnupöntunar** er frábrugðið **Opin-ótímasett** og **Lokað - Hætt við** er hægt að samstilla vinnupantanirnar við Supply Chain Management með Microsoft Dataverse-gagnasamþættingarverki. Uppfærslur á vinnupöntunum verða samstilltar sem sölupantanir í Supply Chain Management. Þessar uppfærslur innihalda upplýsingar um upprunagerð og stöðu.

## <a name="estimated-versus-used"></a>Metið á móti notað

Í Field Service hafa afurðir og þjónusta á vinnupöntunum bæði gildið **Metið** og gildið **Notað** fyrir magn og upphæðir. Hins vegar, í Supply Chain Management hafa sölupantanir ekki sama hugtakið um gildin **Metið** og **Notað**. Til að styðja við afurðarúthlutun sem notar væntanlegt magn á sölupöntun í Supply Chain Management, en til þess að halda notuðu magni sem ætti að nota og reikningsfæra, eru tvö sett af verkefnum sem samstilla afurðir og þjónustur á vinnupöntun. Eitt sett af verkefnum er fyrir gildið **Metið** og hitt sett af verkefnum er fyrir gildið **Notað**.

Þessi hegðun býður upp á aðstæður þar sem metin gildi eru notuð til úthlutunar eða frátekningar í Supply Chain Management, á meðan notuð gildi eru notuð fyrir notkun og reikningsfærslu.

### <a name="estimated"></a>Metið

Til að samstilla afurðalínur eru gildin **Metið** notuð þegar gildið **Línustaða** er **Metið**, valkosturinn **Úthlutað** er stilltur á **Já** og gildið **Kerfisstaða** er ekki **Lokað - Bókað**.

Til að samstilla þjónustulínur eru gildin **Metið** notuð þegar gildið **Línustaða** er **Metið** og gildið **Kerfisstaða** er ekki **Lokað - Bókað**.

### <a name="used"></a>Notað

Gildin **Notað** eru notuð fyrir notkun og reikningsfærslu. Í þessum tilfellum eru gildin **Notað** samstillt.

Eftirfarandi tafla veitir yfirlit yfir mismunandi samsetningar fyrir afurðalínur.

| Kerfisstaða <br>(Þjónusta á staðnum) | Línustaða <br>(Þjónusta á staðnum) | Úthlutað <br>(Þjónusta á staðnum) |Samstillt gildi <br>(Supply Chain Management) |
|--------------------|-------------|-----------|---------------------------------|
| Opið - Tímasett   | Áætlað   | Já       | Áætlað                       |
| Opið - Tímasett   | Metið   | Númer        | Notað                            |
| Opið - Tímasett   | Notað        | Já       | Notað                            |
| Opið - Tímasett   | Notað        | Númer        | Notað                            |
| Opið - Í vinnslu | Metið   | Já       | Metið                       |
| Opið - Í vinnslu | Metið   | Númer        | Notað                            |
| Opið - Í vinnslu | Notað        | Já       | Notað                            |
| Opið - Í vinnslu | Notað        | Númer        | Notað                            |
| Opið - Lokið   | Metið   | Já       | Metið                       |
| Opið - Lokið   | Metið   | Númer        | Notað                            |
| Opið - Lokið   | Notað        | Já       | Notað                            |
| Opið - Lokið   | Notað        | Númer        | Notað                            |
| Lokað - Bókað    | Metið   | Já       | Notað                            |
| Lokað - Bókað    | Metið   | Númer        | Notað                            |
| Lokað - Bókað    | Notað        | Já       | Notað                            |
| Lokað - Bókað    | Notað        | Númer        | Notað                            |

Eftirfarandi tafla veitir yfirlit yfir mismunandi samsetningar á þjónustulínum.

| Kerfisstaða <br>(Þjónusta á staðnum) | Línustaða <br>(Þjónusta á staðnum) | Samstillt gildi <br>(Supply Chain Management) |
|--------------------|-------------|-----------|
| Opið - Tímasett   | Áætlað   | Áætlað |
| Opið - Tímasett   | Notað        | Notað      |
| Opið - Í vinnslu | Metið   | Metið |
| Opið - Í vinnslu | Notað        | Notað      |
| Opið - Lokið   | Metið   | Metið |
| Opið - Lokið   | Notað        | Notað      |
| Lokað - Bókað    | Metið   | Notað      |
| Lokað - Bókað    | Notað        | Notað      |

Samstilling á gildunum **Metið** á móti gildunum **Notað** er stjórnað með tveimur settum af verkefnum fyrir afurðalínur og þjónustulínur. Fyrirfram ákveðnar síur kveikja á réttu verki og undirliggjandi vörpun hjálpar til við að tryggja að rétt gildi fyrir **Metið** á móti **Notað** séu samstillt.

### <a name="example"></a>Dæmi

1. Vinnupöntun er búin til og tímasett í Field Service.

    Gildið **Kerfisstaða** er **Opið - Tímasett**.

    - **Afurðalína:** Metið magn = 5ea, Notað magn = 0ea, Línustaða = Metin, Úthlutað = Nei
    - **Þjónustulína:** Metið magn = 2t, Notað magn = 0h, Línustaða = Metin

    Í þessu dæmi er gildið **Notað magn** fyrir afurðina **0** (núll) og gildið **Metið magn** fyrir þjónustuna **2t** samstillt við Supply Chain Management.

2. Afurðum er úthlutað í Field Service.

    Gildið **Kerfisstaða** er **Opið - Tímasett**.

    - **Afurðalína:** Metið magn = 5ea, Notað magn = 0ea, Línustaða = Metin, úthlutað = Já
    - **Þjónustulína:** Metið magn = 2t, Notað magn = 0h, Línustaða = Metin

    Í þessu dæmi er gildið **Áætlað magn** fyrir afurðina **5ea** og gildið **Metið magn** fyrir þjónustuna **2t** samstillt við Supply Chain Management.

3. Þjónustutæknimaður byrjar að vinna í vinnupöntun og skráir efnisnotkun upp á 6.

    Gildið **Kerfisstaða** er **Opið - Í vinnslu**.

    - **Afurðalína:** Metið magn = 5ea, Notað magn = 6ea, Línustaða = Notað, Úthlutað = Já
    - **Þjónustulína:** Metið magn = 2t, Notað magn = 0h, Línustaða = Metin

    Í þessu dæmi er gildið **Notað magn** fyrir afurðina **6** og gildið **Metið magn** fyrir þjónustuna **2t** samstillt við Supply Chain Management.

4. Þjónustutæknimaðurinn lýkur vinnupöntun og skráir notaðan tíma upp á 1,5 klst.

    Gildið **Kerfisstaða** er **Opið - Lokið**.

    - **Afurðalína:** Metið magn = 5ea, Notað magn = 6ea, Línustaða = Notað, Úthlutað = Já
    - **Þjónustulína:** Metið magn = 2t, Notað magn = 1,5t, Línustaða = Metin

    Í þessu dæmi er gildið **Notað magn** fyrir afurðina **6** og **Notað magn** fyrir þjónustuna **1,5t** samstillt við Supply Chain Management.

## <a name="sales-order-origin-and-status"></a>Uppruni og staða sölupöntunar

### <a name="sales-origin"></a>Uppruni pöntunar

Til að halda utan um sölupantanir sem koma upprunalega frá vinnupöntunum er hægt að búa til uppruna sölupöntunar þar sem valkosturinn **Úthlutun upprunagerðar** er stilltur á **Já** og reiturinn **Upprunagerð sölupöntunar** er stilltur á **Samþætting vinnupöntunar**.

Sjálfgefið er að vörpun velji uppruna sölupöntunar fyrir upprunagerð sölupöntunarinnar **Samþætting vinnupöntunar** fyrir allar sölupantanir sem eru búnar til úr vinnupöntunum. Þessi hegðun getur verið gagnleg þegar unnið er með sölupantanir í Supply Chain Management. Þú verður að ganga úr skugga um að sölupantanir sem eru upprunnar frá vinnupöntunum séu ekki samstilltar aftur við Field Service sem vinnupantanir.

Nánari upplýsingar um hvernig á að búa til rétta uppsetningu á uppruna sölupöntunar í Supply Chain Management er að finna í kaflanum „Uppsetning á forsendum og vörpun“ í þessu efnisatriði.

### <a name="status"></a>Staða

Þegar sölupöntunin er upprunnin frá vinnupöntun birtist reiturinn **Ytri staða vinnupöntunar** í flipanum **Uppsetning** á sölupöntunarhaus. Þessi reitur sýnir kerfisstöðu frá vinnupöntuninni í Field Service til að hjálpa til við að fylgjast með samstilltri stöðu vinnupöntunar í sölupöntunum í Supply Chain Management. Þessi reitur getur einnig hjálpað notendum að ákvarða hvenær eigi að afhenda og reikningsfæra sölupantanir.

Reiturinn **Ytri staða vinnupöntunar** getur haft eftirfarandi gildi:

- Opið - Tímasett
- Opið - Í vinnslu
- Opið - Lokið
- Lokað - Bókað

## <a name="field-service-crm-solution"></a>CRM-lausn Field Service

Til að styðja við samþættingu milli Field Service og Supply Chain Management, er þörf á frekari virkni frá CRM-lausn Field Service. Lausnin inniheldur eftirfarandi breytingar.

### <a name="work-order-entity"></a>Eining vinnupöntunar

Reitnum **Er eingöngu með utanaðkomandi afurðir** hefur verið bætt við eininguna **Vinnupantanir** og birtist á síðunni. Hann er notaður til að fylgjast stöðugt með því hvort vinnupöntun samanstandi eingöngu af utanaðkomandi afurðum. Vinnupöntun inniheldur eingöngu utanaðkomandi afurðir þegar öllum tengdum afurðum er viðhaldið í Supply Chain Management. Þessi reitur hjálpar til við að tryggja að notendur samstilli ekki vinnupantanir sem hafa afurðir sem þekkir ekki.

### <a name="work-order-product-entity"></a>Afurðareining vinnupöntunar

- Reitnum **Pöntun er eingöngu með utanaðkomandi afurðir** hefur verið bætt við eininguna **Afurð vinnupöntunar** og birtist á síðunni. Hann er notaður til að fylgjast stöðugt með því hvort afurð vinnupöntunar sé viðhaldið í Supply Chain Management. Þessi reitur hjálpar til við að tryggja að notendur samstilli ekki afurðir vinnupöntunar sem Supply Chain Management þekkir ekki.
- Reitnum **Kerfisstöðuhaus** hefur verið bætt við eininguna **Afurð vinnupöntunar** og birtist á síðunni. Hann er notaður til að fylgjast stöðugt með kerfisstöðu vinnupöntunar og hjálpar til við að tryggja rétta síun þegar afurðir vinnupöntunar eru samstilltar við Supply Chain Management. Þegar síur eru notaðar á samþættingarverk eru upplýsingarnar **Kerfisstöðuhaus** einnig notaðar til að ákvarða hvort eigi að samstilla metin eða notuð gildi.
- Reiturinn **Reikningsfærð einingarupphæð** sýnir magnið sem er reikningsfært á hverja rauneiningu sem er notuð. Gildið er reiknað út sem **Heildarupphæð** deilt með gildinu **Raunverulegt magn**. Reiturinn er notaður fyrir samþættingu við kerfi sem styðja ekki mismunandi gildi fyrir notað magn og reikningsfært magn. Þessi reitur birtist ekki í notandaviðmótinu. 
- Reiturinn **Reikningsfærð afsláttarupphæð** er reiknaður sem gildið **Afsláttarupphæð** ásamt sléttuninni frá útreikningnum á gildinu **Reikningsfærð einingarupphæð**. Þessi reitur er notaður fyrir samþættingu og birtist ekki í notandaviðmóti.
- Reiturinn **Magn tugastafs** geymir gildið úr reitnum **Magn** sem tugatölu. Þessi reitur er notaður fyrir samþættingu og birtist ekki í notandaviðmóti. 
- Gildið í reitnum **Notað** er endurstillt á **0** (núll) ef gildið **Línustaða** fyrir afurð vinnupöntunar er breytt úr **Notað** í **Metið**. Þessi breyting hjálpar til við að koma í veg fyrir aðstæður þar sem notað magn sem er ranglega slegið inn sé notað til samstillingar þegar gildið **Línustaða** er **Metið** og valkosturinn **Úthlutað** er stilltur á **Nei**.

### <a name="work-order-service-entity"></a>Þjónustueining vinnupöntunar

- Reitnum **Pöntun er eingöngu með utanaðkomandi afurðir** hefur verið bætt við eininguna **Þjónusta vinnupöntunar** og birtist á síðunni. Hann er notaður til að fylgjast stöðugt með því hvort þjónusta vinnupöntunar sé viðhaldið í Supply Chain Management. Þessi reitur hjálpar til við að tryggja að notendur samstilli ekki þjónusta vinnupöntunar sem Supply Chain Management þekkir ekki.
- Reitnum **Kerfisstöðuhaus** hefur verið bætt við eininguna **Þjónusta vinnupöntunar** og birtist á síðunni. Hann er notaður til að fylgjast stöðugt með kerfisstöðu vinnupöntunar og hjálpar til við að tryggja rétta síun þegar þjónusta vinnupöntunar er samstillt við Supply Chain Management. Þegar síur eru notaðar á samþættingarverk eru upplýsingarnar **Kerfisstöðuhaus** einnig notaðar til að ákvarða hvort eigi að samstilla metin eða notuð gildi.
- Reiturinn **Tímalengd í klst.** geymir gildið úr reitnum **Tímalengd** eftir að gildinu er umbreytt úr mínútum í klukkustundir. Þessi reitur er notaður fyrir samþættingu og birtist ekki í notandaviðmóti.
- Reiturinn **Metin tímalengd í klst.** geymir gildið úr reitnum **Metin tímalengd** eftir að gildinu er umbreytt úr mínútum í klukkustundir. Þessi reitur er notaður fyrir samþættingu og birtist ekki í notandaviðmóti.
- Reiturinn **Reikningsfærð einingarupphæð** geymir upphæðina sem er reikningsfærð á hverja rauneiningu sem er notuð. Gildið er reiknað út sem **Heildarupphæð** deilt með gildinu **Raunverulegt magn**. Þessi reitur er notaður fyrir samþættingu við kerfi sem styðja ekki mismunandi gildi fyrir notaða magnið og reikningsfærða magnið. Reiturinn birtist ekki í notandaviðmótinu.
- Reiturinn **Reikningsfærð afsláttarupphæð** er reiknaður sem gildið **Afsláttarupphæð** ásamt sléttuninni frá útreikningnum á gildinu **Reikningsfærð einingarupphæð**. Þessi reitur er notaður fyrir samþættingu og birtist ekki í notandaviðmóti.
- Reiturinn **Ytri línupöntun** er útreiknað neikvætt línupöntunarnúmer sem hægt er að nota í ytri kerfum þar sem afurð vinnupöntunar og þjónustulínur eru sameinaðar. Þessi reitur gerir afurðum vinnupantana sem eru settar inn kleift að hafa jákvæð línunúmer og þjónustur vinnupantana að hafa neikvæð línunúmer. Gildi reitsins er reiknað út sem gildið **Línupöntun** margfaldað með -1. Þessi reitur birtist ekki í notandaviðmótinu.
- Gildið í reitnum **Notað** er endurstillt á **0** (núll) ef gildið **Línustaða** fyrir þjónustu vinnupöntunar er breytt úr **Notað** í **Metið** af einhverri ástæðu. Þessi breyting hjálpar til við að koma í veg fyrir aðstæður þar sem notað magn sem er ranglega slegið inn sé notað til samstillingar þegar gildið **Línustaða** er **Metið** og gildið **Kerfisstöðuhaus** er **Lokað - Bókað**.

## <a name="preconditions-and-mapping-setup"></a>Skilyrði og vörpunaruppsetning

Áður en vinnupantanir eru samstilltar er mikilvægt að uppfæra eftirfarandi stillingar í kerfunum.

### <a name="setup-in-field-service"></a>Uppsetning í Field Service

- Gakktu úr skugga um að númeraröðin sem er notuð fyrir vinnupantanir í Field Service skarist ekki á við númeraröðina sem notuð er fyrir sölupantanir í Supply Chain Management. Annars geta núverandi sölupantanir verið uppfærðar ranglega í Field Service eða Supply Chain Management.
- Reiturinn **Stofna reikning vinnupöntunar** þarf að vera stilltur á **Aldrei** vegna þess að reikningsfærslan verður gerð í Supply Chain Management. Farðu í **Field Service** \> **Stillingar** \> **Stjórnun** \> **Stillingar Field Service** og gakktu úr skugga um að reiturinn **Stofna reikning vinnupöntunar** sé stilltur á **Aldrei**.

### <a name="setup-in-supply-chain-management"></a>Uppsetning í Supply Chain Management

Samþætting vinnupöntunar krefst þess að söluuppruninn verði settur upp. Söluuppruninn er notaður til að greina sölupantanir í Supply Chain Management sem voru stofnaðar út frá vinnupöntunum í Field Service. Þegar sölupöntun hefur söluuppruna af gerðinni **Samþætting vinnupöntunar** birtist reiturinn **Ytri staða vinnupöntunar** á sölupöntunarhausnum. Til viðbótar hjálpar söluuppruni að tryggja að sölupantanir sem voru stofnaðar úr vinnupöntunum í Field Service séu síaðar út á meðan samstilling stendur yfir á sölupöntunum Supply Chain Management við Field Service.

1. Farðu í **Sala og markaðssetning** \> **Uppsetning** \> **Sölupantanir** \> **Söluuppruni**.
2. Veldu **Nýr** til að búa til nýjan söluuppruna.
3. Í reitinn **Söluuppruni** skal slá inn heiti söluuppruna, t.d. **Vinnupöntun**.
4. Í reitinn **Lýsing** skal færa inn lýsingu, t.d. **Vinnupöntun Field Service**.
5. Veldu gátreitinn **Úthlutun upprunagerðar**.
6. Stilltu reitinn **Upprunagerð sölu** á **Samþætting vinnupöntunar**.
7. Veldu **Vista**.


### <a name="setup-in-data-integration"></a>Uppsetning í gagnasamþættingu

Gakktu úr skugga um að **samþættingarlykill** sé til fyrir **msdyn_workorders**
1. Farðu í gagnasamþættingu
2. Veldu flipann **Tenging stillt**
3. Veldu stillingu á tengingu sem er notuð fyrir samstillingu vinnupöntunar
4. Veldu flipann **Samþættingarlykill**
5. Finndu msdyn_workorders og athugaðu hvort lyklinum **msdyn_name (vinnupöntunarnúmer)** hafi verið bætt við. Ef hann er ekki sýndur skaltu bæta honum við með því að smella á **Bæta við lykli** og smella á **Vista** efst á síðunni

## <a name="template-mapping-in-data-integration"></a>Sniðmátsvörpun í Gagnasamþættingu

Eftirfarandi myndir sýna sniðmátsvörpunina í Gagnasamþættingu.

### <a name="work-orders-to-sales-orders-field-service-to-supply-chain-management-workorderheader"></a>Verkbeiðnir til sölupantana (Field Service til Supply Chain Management): WorkOrderHeader

Sía: (msdyn_systemstatus ne 690970005) og (msdyn_systemstatus ne 690970000) og (msdynce_hasexternallymaintainedproductsonly eq true)

[![Sniðmátsvörpun í gagnasamþættingu fyrir verkbeiðnir til sölupantana (Field Service til Supply Chain Management): WorkOrderHeader.](./media/FSWorkOrder1.png )](./media/FSWorkOrder1.png)

### <a name="work-orders-to-sales-orders-field-service-to-supply-chain-management-workorderservicelineestimate"></a>Verkbeiðnir til sölupantana (Field Service til Supply Chain Management): WorkOrderServiceLineEstimate

Síða: (msdynce_headersystemstatus ne 690970005) og (msdynce_headersystemstatus ne 690970000) og (msdynce_orderhasexternalmaintainedproductsonly eq true) og (msdyn_linestatus eq 690970000) og (msdynce_headersystemstatus ne 690970004)

[![Sniðmátsvörpun í gagnasamþættingu fyrir verkbeiðnir til sölupantana (Field Service til Supply Chain Management): WorkOrderServiceLineEstimate.](./media/FSWorkOrder2.png )](./media/FSWorkOrder2.png)

### <a name="work-orders-to-sales-orders-field-service-to-supply-chain-management-workorderservicelineused"></a>Verkbeiðnir til sölupantana (Field Service til Supply Chain Management): WorkOrderServiceLineUsed

Sía: (msdynce_headersystemstatus ne 690970005) og (msdynce_headersystemstatus ne 690970000) og (msdynce_orderhasexternalmaintainedproductsonly eq true) og ((msdyn_linestatus eq 690970001) eða (msdynce_headersystemstatus eq 690970004))

[![Sniðmátsvörpun í gagnasamþættingu fyrir verkbeiðnir til sölupantana (Field Service til Supply Chain Management): WorkOrderServiceLineUsed.](./media/FSWorkOrder3.png )](./media/FSWorkOrder3.png)

### <a name="work-orders-to-sales-orders-field-service-to-supply-chain-management-workorderproductlineestimate"></a>Verkbeiðnir til sölupantana (Field Service til Supply Chain Management): WorkOrderProductLineEstimate

Sía: (msdynce_headersystemstatus ne 690970005) og (msdynce_headersystemstatus ne 690970000) og (msdynce_orderhasexternalmaintainedproductsonly eq true) og (msdyn_linestatus eq 690970000) and (msdynce_headersystemstatus ne 690970004) og (msdyn_allocated eq true)

[![Sniðmátsvörpun í gagnasamþættingu fyrir verkbeiðnir til sölupantana (Field Service til Supply Chain Management): WorkOrderProductLineEstimate.](./media/FSWorkOrder4.png )](./media/FSWorkOrder4.png)

### <a name="work-orders-to-sales-orders-field-service-to-supply-chain-management-workorderproductlineused"></a>Verkbeiðnir til sölupantana (Field Service til Supply Chain Management): WorkOrderProductLineUsed

Sía: (msdynce_headersystemstatus ne 690970005) og (msdynce_headersystemstatus ne 690970000) og (msdynce_orderhasexternalmaintainedproductsonly eq true) og ((msdyn_linestatus eq 690970001) eða (msdynce_headersystemstatus eq 690970004) eða (msdyn_allocated ne true))

[![Sniðmátsvörpun í gagnasamþættingu fyrir verkbeiðnir til sölupantana (Field Service til Supply Chain Management): WorkOrderProductLineUsed.](./media/FSWorkOrder5.png )](./media/FSWorkOrder5.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]