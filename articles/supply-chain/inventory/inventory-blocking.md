---
title: Birgðalæsing
description: Þetta efni veitir yfirlit yfir birgðalæsingu, sem er partur af gæðaskoðunarferli í Supply Chain Management. Hægt er að nota birgðalæsingu til að koma í veg fyrir að vörur séu unnar eða notaðar.
author: yufeihuang
ms.date: 03/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventBlocking, InventQualityOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2094
ms.assetid: 1968e32f-eff9-4c17-8f7f-a870f0c38fbc
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 606bc23f552b57d0f4e3fdad28d1144cdf43e5d5
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/09/2022
ms.locfileid: "8103539"
---
# <a name="inventory-blocking"></a>Birgðalæsing

[!include [banner](../includes/banner.md)]

Þetta efni veitir yfirlit yfir birgðalæsingu, sem er partur af gæðaskoðunarferli í Supply Chain Management. Hægt er að nota birgðalæsingu til að koma í veg fyrir að vörur séu unnar eða notaðar.

Hægt er að loka vörubirgðum á eftirfarandi vegu.

- Handvirkt
- Með því að stofna gæðapöntun
- Með því að nota ferlið sem myndar gæðapöntun
- Með því að nota Birgðastöðulokun

## <a name="blocking-items-manually"></a>Læsa vörum handvirkt

Hægt er að loka á magn af vöru með því að stofna færslu í síðunni **birgðalæsing**. Aðeins er hægt að læsa vörum handvirkt sem eru í boði sem lagerbirgðir. Fyrir handvirkt læst magn verður að hugleiða hvort áætlun verkþátta innihaldi viðbúnar uppskriftir sem væntanlegt magn á lager. Áætlaðar innhreyfingar eru læstar vörur sem von er á að sé tiltækt sem birgðir á lager eftir skoðun. Hægt er að viðhalda viðbúinni dagsetningu. Að sjálfgefnu **Áætlaðar innhreyfingar** valkostur er valinn fyrir vörur sem eru læstar gegnum gæðapöntun. Hægt er að afturkalla handvirka lokun á handvirkt læstu magni með því að eyða færslu á síðunni **birgðalæsing**.

## <a name="blocking-items-by-creating-a-quality-order"></a>Læsa vörum með því að stofna gæðapöntun

Hægt er að tilgreina vörurnar sem verða skoðaðar með því að stofna gæðapöntun á í **gæðapantanir** síðu. Þegar gæðapöntun er stofnuð er magn vöru sem tilgreint er lokað. Þegar gæðapöntun er mynduð sjálfkrafa er úrtaksáætlun vörunnar sem er tengd við gæðapöntunina stjórnar aðeins magni vara sem verður að skoða, ekki magni sem eru læst. magn vöru sem er færð inn á gæðapöntunina er magnið sem er lokað Óháð því magni sem er sent til skoðunar, eins og tilgreint er af úrtaksáætlun

> [!NOTE]
> Að nota bæði fyrningardagsetningu lotunnar og loka fyrir birgðastöðuaðgerðir er ekki studdur af aðalskipulagningu. Þetta gæti leitt til tvöfalds útilokunar á lagerbirgðum sem getur komið fram við skipulagningu meistarans. Við mælum með því að þú reiðir þig á kóðana á lotunotkun, í stað birgðastöðu, til að loka fyrir útrunnið lotur.

## <a name="blocking-items-by-using-a-process-that-generates-a-quality-order"></a>Læsa vörum með ferli sem myndar gæðapöntun

Ef gæðaferli tilgreinir að vara verður að vera skoðuð, er magn af vörunni læst sjálfkrafa. Þessvegna, Þegar gæðapöntun er mynduð sjálfkrafa er úrtaksáætlun vörunnar sem er tengd við gæðapöntunina stjórnar bæði magni vara sem eru útilokaðar og magni vara sem verður að skoða. Ef valkosturinn **full læsing** í **vöruúrtak** síðu er valinn er lokað fyrir fullt magn af til dæmis innkaupapöntunarlína við skoðun, óháð magni vörusýnishorns.

### <a name="example"></a>Dæmi

Í eftirfarandi dæmi er gæðapöntun mynduð þegar fylgiseðill innkaupapöntunar er bókaður. Í á **gæðatengingar** síðunni, tilgreindirðu að bókun fylgiseðils innkaupapöntunar er ferlið sem virkjar gæðapöntun.

|Uppsetning |Aðgerðir notanda |Niðurstaða |
|----|---|---|
| Gæðatenging tilgreinir að við bókun fylgiseðils innkaupapöntunar þarf að mynda gæðapöntun. Uppsetning vörusýna gæðapöntunar tilgreinir að 10% af magn í innkaupapöntunarlínu verða að vera skoðaðar. Enn fremur, afþví **full læsing** valkosturinn er valinn sýnir sýnishorn vörunnar að allt magnið í innkaupapöntunarlínunni verður að vera læst við skoðun óháð því magni sem er sent til skoðunar. | Fylgiseðillinn er bókaður. | Gæðapöntun er mynduð. Tíu prósent af magni innkaupapöntunar af hlutnum er sendur til skoðunar. Heildarmagn á innkaupapöntunarlínunni er lokað. |

## <a name="blocking-items-by-using-inventory-status-blocking"></a>Læsa vörum Með því að nota Birgðastöðulokun

Hægt er að tilgreina hvaða birgðastöður eru lokunarstöður með því að nota **birgðalæsingu** færibreytur á í **Birgða stöður** síðu. Þú getur ekki notað birgðastöðu sem lokunar stöður fyrir framleiðslupantanir, sölupantanir, flutningspantanir, færslur á útleið eða samþættingar verks. Notið vörur með stöðu tiltækar birgðir fyrir vinnu á útleið. Ef vörur með stöðuna **slitin** og aðaláætlanagerð er keyrð fyrir þessar vörur, er litið á þessar vörur þannig að þær vanti og birgðir eru endurnýjaðar sjálfkrafa.

## <a name="take-care-when-blocking-items-that-use-both-inventory-status-blocking-and-quality-order-blocking"></a>Fara skal varlega þegar verið er að loka vörum sem nota bæði birgðastöðulokun og gæðapöntunarlokun

Hægt er að stofna gæðapöntun sem tengist birgðum með birgðastöðu sem er með færibreytuna **Birgðalæsing** virkjaða. Í þessu tilviki mun gæðapöntunin búa til skrá birgðalæsingar til viðbótar við það sem var stofnað af birgðastöðunni. Vegna þess að birgðalæsing gæðapöntunar verður með færibreytuna **Væntanlegar innhreyfingar** virkjaða býr þetta til aukafærsluna *Pantaðar birgðir* sem birgðastaðan lokar einnig á. Þessi samsetning getur leitt til erfiðleika við að skilja merkingu myndaðra birgðafærslna vegna þess að hún mun birtast líkt og heildarmagn sem er útilokað sé umfram heildarmagn á lager. Við skulum skoða færslur í dæmi um innhreyfingu á 10 stykkjum af vöru A0001 með gæðapöntun sem gerð er til að taka 1 stk af sýnishorni. Hegðunin ræðst einnig af því hvort valkosturinn **Taka frá pantaðar vörur** er virkur á síðunni **Færibreytur birgða- og vöruhúsakerfis**.

>[!NOTE]
>Ef verið er að nota birgðastöðulokun og gæðapantanir saman er eindregið mælt með að hafa valkostinn **Taka frá pantaðar vörur** virkjaðan.

### <a name="example-with-reserve-ordered-items-enabled"></a>Dæmi með „Taka frá pantaðar vörur“ virkt

Þegar **Taka frá pantaðar vörur** er virkjað fá allar birgðalokunarfærslur annaðhvort stöðuna *Frátekið efnislegt* eða *Frátekið pantað*.

| Tilvísun í birgðafærslu | Innhreyfing | Úthreyfing | Magn | Vefsvæði | Vöruhús | Birgðastaða | Staður | Númeraplata | Athugasemd |
|---|---|---|---|---|---|---|---|---|---|
| Innkaupapöntun | Innkeypt | | 10 stk. | 2 | 24 | Læsing | RECV | receiptLp1 | | 
| Stöðvun í birgðum | | Frátekið á lager | -9 stk. | 2 | 24 | Læsing | | | Færsla sem birgðastöðulokunin býr til |
| Stöðvun í birgðum | | Frátekið á lager | -1 stk. | 2 | 24 | Læsing | RECV | receiptLp1 | Færsla sem sýnatökuútilokun gæðapöntunar býr til |
| Stöðvun í birgðum | Raðað | | 1 stk. | 2 | 24 | Læsing | RECV | receiptLp1 | Áætlaðar innhreyfingar úr lokun á sýnatöku gæðapöntunar |
| Stöðvun í birgðum | | Frátekið pantað | 1 stk. | 2 | 24 | Læsing | | | Færsla sem birgðastöðulokunin býr til

### <a name="example-with-reserve-ordered-items-disabled"></a>Dæmi með „Taka frá pantaðar vörur“ óvirkt

Þegar **Taka frá pantaðar vörur** er óvirt verður ekki hægt að taka frá væntanlegar innhreyfingar vegna þess að þær eru með stöðuna *Pantað* þannig að einhver lokun verður eftir í stöðunni *Í pöntun*.

| Tilvísun í birgðafærslu | Innhreyfing | Úthreyfing | Magn | Vefsvæði | Vöruhús | Birgðastaða | Staður | Númeraplata | Athugasemd |
|---|---|---|---|---|---|---|---|---|---|
| Innkaupapöntun | Innkeypt | | 10 stk. | 2 | 24 | Læsing | RECV | receiptLp1 | |
| Stöðvun í birgðum | | Frátekið á lager | -9 stk. | 2 | 24 | Læsing | | | Færsla sem birgðastöðulokunin býr til |
| Stöðvun í birgðum | | Frátekið á lager | -1 stk. | 2 | 24 | Læsing | RECV | receiptLp1 | Færsla sem sýnatökuútilokun gæðapöntunar býr til |
| Stöðvun í birgðum | Raðað | | 1 stk. | 2 | 24 | Læsing | RECV | receiptLp1 | Áætlaðar innhreyfingar úr lokun á sýnatöku gæðapöntunar |
| Stöðvun í birgðum | | Í pöntun | 1 stk. | 2 | 24 | Læsing | RECV | receiptLp1 | Færsla sem birgðastöðulokunin býr til

Athugið muninn á færslustöðu og víddunum á milli þessara tveggja tilvika. Af þessum ástæðum er mælt með því að virkja **Taka frá pantaðar vörur**.

### <a name="disable-expected-receipts-from-quality-orders-that-sample-blocked-inventory-feature"></a>Slökktu á væntanlegum kvittunum frá gæðapöntunum sem sýna sýnishorn af lokuðum birgðaeiginleika

Til að einfalda birgðafærslur þegar um er að ræða gæðapantanir sem sýnishorn af birgðum er lokað vegna birgðastöðu, býður kerfið upp á eiginleika sem slekkur á væntanlegum innhreyfingum frá slíkum gæðapöntunum. Vegna þess að væntanleg innhreyfing er strax læst með lokun birgðastöðu, er engin lækkun á birgðum á lager vegna þessarar breytingar.

Slökkt er á þessum eiginleika að sjálfgefnu. Stjórnendur geta kveikt eða slökkt á því með því að leita að *Slökktu á væntanlegum innhreyfingum frá gæðapöntunum sem taka sýnishorn af lokuðum birgðum* eiginleiki í [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) vinnurými.

## <a name="additional-resources"></a>Frekari upplýsingar

[Stofna og viðhalda á birgðalokun](tasks/create-maintain-inventory-blocking.md)

[Gæðastjórnunarferli](quality-management-processes.md)

[Skoða gæði vara](tasks/inspect-quality-goods.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]