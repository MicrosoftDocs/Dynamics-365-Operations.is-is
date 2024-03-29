---
title: Setja upp símaversrásir
description: Þessi grein veitir upplýsingar um hvernig á að vinna úr pöntunum fyrir símaver með því að nota Dynamics 365 Commerce.
author: josaw1
ms.date: 02/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MCROrderParameters, MCRSalesTableOrderHistory, SalesOrderProcessingWorkspace
audience: Application User
ms.reviewer: josaw
ms.custom: 78973
ms.assetid: 09fca083-ac0d-4f30-baf2-bb00a626be12
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: c6d21385d956534c799af5b9e20a54c9970da368
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8854872"
---
# <a name="set-up-call-center-channels"></a>Setja upp símaversrásir

[!include [banner](includes/banner.md)]

Fyrirtæki getur skilgreint margar rásir símavers í Dynamics 365 Commerce. Rásir símavers eru stilltar í **Retail og Commerce** \> **Rásir** \> **Símaver** \> **Öll símaver** og þau eru sérstæk fyrir lögaðila.

Þegar ný rás símavers er búin til er henni kerfisbundið úthlutað rekstrareiningarnúmeri. Vegna þess að símaver eru búin til sem rekstrareiningar geta notendur tengt rásir símavers við ýmsa Commerce eiginleika, t.d. vöruúrval, vörulista og tiltekna sendingarmáta.

Hægt er að stilla sjálfgefið vöruhús á rás símavers. Þegar sölupantanir eru síðan búnar til í þeirri rás er sjálfgefna vöruhúsið sjálfkrafa slegið inn í sölupöntunarhaus nema annað vöruhús hafi verið skilgreint fyrir viðskiptavininn sem er valinn fyrir sölupöntunina. Í því tilfelli er vöruhús viðskiptavinar slegið inn að sjálfgefnu.

Notendur verða að vera tengdir við rás símavers til að nota eiginleika símavers. Sérhver sölupöntun sem notandi býr til er sjálfkrafa tengd við rás símavers notanda. Eins og er getur einn notandi ekki tengst við margar rásir símavers á sama tíma.

Einnig er hægt að skilgreina forstillingu fyrir tilkynningar í tölvupósti á rás símavers. Forstillingin skilgreinir sett af sniðmáti fyrir tölvupóst sem er notað þegar tölvupóstur er sendur til viðskiptavina sem leggja inn pantanir í gegnum rás símaversins. Hægt er að stilla tölvupóstsræsingar við kerfisatvik á borð við innsendingu pöntunar eða afhendingu pöntunar.

Áður en hægt er að vinna úr sölum með réttum hætti í gegnum rás símavers, verður að skilgreina réttan [greiðslumáta](/dynamics365/unified-operations/retail/work-with-payments) og afhendingarsnið fyrir rásina.

Á stigi símaversrásar er hægt að skilgreina önnur sjálfgefin gildi sem tengjast fjárhagsvíddum sem verða tengd við pantanir sem eru búnar til af þeirri rás.

## <a name="options-for-order-processing-behavior"></a>Valkostir fyrir hegðun á vinnslu pantana

Þrjár stillingar í grunnstillingum símavers hafa mikil áhrif á þá eiginleika og aðgerðir sem eru í boði fyrir sölupantanir sem eru búnar til gagnvart þessu símaveri: **Virkja lok pöntunar**, **Virkja beina sölu** og **Virkja verðstýringu pöntunar**.

### <a name="enable-order-completion"></a>Virkja lok pöntunar

Stillingin **Virkja lok pöntunar** á rás símavers hefur mikil áhrif á vinnsluflæði pantana á sölupöntunum sem eru færðar inn í rásina. Þegar kveikt er á þessari stillingu verða allar sölupantanir að fara í gegnum sett af villuleitarreglum áður en hægt er að staðfesta þær. Hægt er að keyra þessar reglur með því að velja hnappinn **Lokið** sem er bætt við á aðgerðarsvæðinu á síðu sölupöntunar. Allar sölupantanir sem eru búnar til þegar kveikt er á stillingunni **Virkja lok pöntunar** verða að fara í gegnum lokunarferli pöntunar. Þetta ferli tryggir að náð sé í reglu greiðslu og greiðslustaðfestingar. Til viðbótar við framfylgni á greiðslu getur innsendingarferli pöntunar kveikt á [athugun á svikum](/dynamics365/unified-operations/retail/set-up-fraud-alerts) sem eru skilgreindar í kerfinu. Pantanir sem falla á greiðslu eða prófun á svikum eru settar í bið og er ekki hægt að losa til frekari vinnslu (á borð við tiltekt eða afhendingu) fyrr en málið sem olli biðinni er leyst.

Þegar kveikt er á stillingunni **Virkja lok pöntunar** fyrir rás símavers, ef vörulínur eru færðar inn á sölupöntun og notandi rásar reynir að loka eða fletta í burtu frá skjámynd sölupöntunar án þess að velja fyrst **Lokið**, framfylgir kerfið lokunarferli pöntunar með því að opna samantektarsíðu sölupöntunar og krefjast þess að notandi sendi pöntunina rétt. Ef ekki er hægt að senda pöntun á réttan hátt ásamt greiðslu, getur notandinn notað virknina [biðpantanir](/dynamics365/unified-operations/retail/work-with-order-holds) til að setja pöntunina í bið. Ef notandi er að reyna að hætta við pöntun verður hann eða hún að hætta henni á réttan hátt með því að nota annaðhvort aðgerðina Hætta við eða aðgerðina Eyða, fer eftir því hvaða aðgerð öryggi notanda leyfir.

Ef kveikt er á stillingunni **Virkja lok pöntunar** fyrir rás símavers, verður reiturinn **Staða greiðslu** rakinn á pöntuninni. Kerfið reiknar út **Greiðslustöðu** þegar sölupöntun er send. Aðeins pantanir sem hafa samþykkta greiðslustöðu geta farið í gegnum kerfið fyrir frekari skre í vinnslu á pöntun, svo sem tiltekt og afhending. Ef greiðslum er hafnað, mun kvikna á flagginu **ekki vinna úr** á ítarlegri pöntunarstöðu, sem setur pöntunina í bið þar til greiðsluvandinn er leystur.

Að auki, ef kveikt er á stillingunni **Virkja lok pöntunar**, þegar notendur búa til sölupantanir og eru í færslusniði vörulínu, verður reiturinn **Uppruni** tiltækur í sölupöntunarhaus. Reiturinn **Uppruni** er notaður til að grípa [upprunakóða vörulista](/dynamics365/unified-operations/retail/call-center-catalogs) við aðstæður beinnar markaðssölu. Þessi kóði getur síðan keyrt sérstök verð og kynningar.

Jafnvel þótt slökkt sé á stillingunni **Virkja lok pöntunar** geta notendur enn notað upprunakóða á sölupöntun. Hins vegar verða þeir fyrst að opna upplýsingar sölupöntunarhauss til að fá aðgang að reitnum **Uppruni**. Með öðrum orðum þá er þörf á frekari smellum. Sama hegðun á við um eiginleika eins og afhendingu lokið og flýttar pantanir. Þessar aðgerðir eru tiltækir fyrir allar pantanir sem eru búnar til í símaverinu. Hins vegar þegar kveikt er á stillingunni **Virkja lok pöntunar** geta notendur séð grunnstillingar þessara aðgerða á söluhaus á meðan þeir eru í yfirliti færslulínu. Þeir þurfa ekki að kafa niður í upplýsingar sölupöntunarhauss til að finna viðeigandi stillingar og reiti.

> [!NOTE]
> Þegar **Umni-rás viðskiptapöntunargreiðslur** eiginleiki er virkur, símaverið **Virkja pöntunarlok** hnappur verður falinn í höfuðstöðvum á **Almennt** Flýtiflipi rásarinnar þinnar á **Verslun og verslun \> Rásir \> Símaver**.

### <a name="enable-direct-selling"></a>Virkja beina sölu

Ef kveikt er á stillingunni **Virkja beina sölu** fyrir rás símaver geta notendur nýtt sér eiginleika viðbótarsölu og krosssölu í Commerce. Í þessu tilfelli birtast sprettigluggar við pöntunarfærslu og benda á aðrar afurðir sem notandi símavers getur boðið viðskiptavininum. Ráðlagðar afurðir byggjast á afurðinni sem var verið að panta á sölupöntunarlínu. Eins og er eru ráðleggingar viðbótarsölu og krosssölu skilgreindar á vörustigi afurða og vörulista. Ef slökkt er á stillingunni **Virkja beina sölu** fyrir rás símavers birtast sprettigluggir ekki við pöntunarfærslu, jafnvel þótt gild viðbótarsala og krosssala var skilgreind fyrir vöru sem verið er að panta.

Þegar kveikt er á stillingunni **Virkja beina sölu** er einnig kveikt á eiginleikum forskrifta og mynda á síðu sölupöntunarfærslu. Í þessu tilfelli er upplýsingagluggi í boði hægra megin á síðunni við pöntunarfærslu. Þessi gluggi getur sýnt forskriftir sem tengjast almennu ferli pantanavinnslu, upprunakóða vörulista sem var notaður eða forskriftum sem tengjast vörunum sem verið er að panta. Að auki getur myndglugginn sýnt mynd afurðar fyrir vörurnar sem verið er að panta ef mynd hefur verið skilgreind fyrir vöruna í vöruuppsetningu.

### <a name="enable-order-price-control"></a>Virkja verðstýringu pöntunar

Þegar kveikt er á stillingunni **Virkja verðstýringu pöntunar** geta aðeins notendur með heimild breytt söluverði vöru við pöntunarfærslu. Breytingarnar verða að vera innan skilgreindra vikmarka. Notendur sem ekki hafa viðeigandi heimild þurfa að leggja fram beiðni um breytingu á verði í staðinn. Unnið verður úr beiðninni í gegnum verkferla kerfisins fyrir endurskoðun og samþykki.

## <a name="channel-users"></a>Rásarnotendur

Þegar rás símavers er skilgreind þarf að tengja rásarnotendur við símaverið. Annars er ekki hægt að nota símaverið í kerfinu. Þegar notendur skrá sig inn í Commerce og færa inn sölupantanir eða skila pöntunum á síðu sem tengist pöntunarfærslu, er notandakenni þeirra sannprófað gagnvart stillingu símaversrásar. Ef notandi er tengdur við tiltekna rás símavers erfa pantanir sem notandi býr til einkenni og sjálfgefin gildi þeirrar rásar.

Sjálfgefið er að kveikt sé á flaggi **Sölu** á sölupöntunarhaus fyrir allar pantanir sem notandi símavers býr til. Pantanir geta síðan notfært sér eiginleika Commerce-sértækra verða og kynningartilboða kerfisins.


Notendur sem eru ekki tengdir við símaver rás nota staðlaða pöntunarfærslu eiginleika Microsoft Dynamics 365 Fjármál. Pantanir sem þessir notendur færa inn í gegnum skjámynd sölupöntunarfærslu verða ekki kerfisbundið auðkenndar sem Commerce pantanir. Þar að auki munu pantanirnar sem þessir notendur hafa fært inn ekki heyra undir neinar úrvinnslureglur pöntunarloka, verðlagningu eða aðrar villuprófanir á pöntun sem hægt er að skilgreina í grunnstillingum símaversrásar eða kerfisfæribreytum símavers.

Þegar stillingu á rás símavers og skilgreiningu á rásarnotendum er lokið, til að hjálpa að tryggja æskilega kerfishegðun, skal ganga úr skugga um að allar nauðsynlegar færibreytur símavers séu skilgreindar í **Retail og Commerce** \> **Uppsetning rásar** \> **Uppsetning símavers** \> **Færibreytur símavers**. Tryggja skal að tengdar númeraraðir séu einnig skilgreindar.

> [!NOTE]
> Til að nota símaversvirkni Retail verður stillingarlykilinn fyrir **Sent mörgum** að vera virkur. Þennan stillingarlykil er að finna í lyklunum **Stillingu viðskipta** undir **Kerfisstjórnun**\> **Uppsetning** \> **Stilling leyfis**. Þetta er nauðsynlegt vegna símaversaðgerða sem framkvæma ýmsar sannprófanir á grundvelli afhendingarfangs sem er stillt á sölupöntunarlínustig. 



[!INCLUDE[footer-include](../includes/footer-banner.md)]
