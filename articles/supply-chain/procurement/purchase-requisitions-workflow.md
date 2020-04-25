---
title: Verkflæði fyrir innkaupabeiðni
description: Verkflæðisferlið færir innkaupabeiðnir í endurskoðunarferli úr upphaflegu stöðunni Drög í endanlegu stöðuna Samþykkt. Þegar innkaupabeiðni er sent til endurskoðunar, hefst verkflæðisferli. Eftir að innkaupabeiðnin er samþykkt getir innkaupapöntun verið myndað fyrir innkaupabeiðnilínur og send til lánardrottins fyrir uppfyllingu pöntunar.
author: mkirknel
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqAuthorization, WorkflowParticipantExpenToken
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2234
ms.assetid: dad3ba5a-2892-45d2-874a-300896f59b34
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0a3d0b6c4ef9e6f21e1542bece9046e98edcab6b
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207834"
---
# <a name="purchase-requisition-workflow"></a>Verkflæði fyrir innkaupabeiðni

[!include [banner](../includes/banner.md)]

Verkflæðisferlið færir innkaupabeiðnir í endurskoðunarferli úr upphaflegu stöðunni Drög í endanlegu stöðuna Samþykkt. Þegar innkaupabeiðni er sent til endurskoðunar, hefst verkflæðisferli. Eftir að innkaupabeiðnin er samþykkt getir innkaupapöntun verið myndað fyrir innkaupabeiðnilínur og send til lánardrottins fyrir uppfyllingu pöntunar.

Áður en hægt er að senda innkaupabeiðni í endurskoðun verður að stilla verkflæði. Verkflæðisferlið getur innihaldið einn eða fleiri endurskoðunarskref, í hvaða röð sem er. Einnig er hægt að skilgreina verkflæðisferlið til að sleppa verk sem fara yfir og samþykkja innkaupabeiðni sjálfkrafa. Hægt er að skilgreina verkflæði til að leiða innkaupabeiðnina sem eitt skjal eða hægt er að leiða einstakar innkaupabeiðnilínur til viðeigandi yfirlesarar. Einnig er hægt að stofna aðstæður þar sem innkaupabeiðnin er látin vera í leið sem einu skjali til sumra yfirlesara og völdum innkaupabeiðnilínum er leitt til annarra yfirlesara.  

Ef innkaupabeiðnilínur eru endurskoðaðar ein og ein, verður að ljúka skoðunarferlinu fyrir allar innkaupabeiðnilínur áður en verkflæðisferli getur farið á næsta skref, og áður en hægt er að ljúka endurskoðunarferlinu fyrir innkaupabeiðnina alla. Þegar the endurskoðunarferli hefur verið lokið fyrir innkaupabeiðni og allar hennar línur, er heildar staða af innkaupabeiðni er uppfærð í í **Samþykkt**.  

Hægt er að skilgreina verkflæði til að endurspegla viðskiptaferli fyrir innkaupabeiðnir í fyrirtækinu. Þegar skilgreind er verkflæðisferli innkaupabeiðna, íhugið eftirfarandi punktar:

-   Hvaða útgjöld verður að endurskoða?
-   Hvaða útgjöld er hægt að samþykkja sjálfkrafa?
-   Hverjir verða að skoða og samþykkja útgjaldabeiðnir? Hvaða hlutverk hafa þessir notendur fengið úthlutað?
-   Hvaða ferli verður að fylgja ef yfirlesari er ekki tiltækur?

Eftirfarandi dæmi sýna tvær leiðir til að skilgreina verkflæði fyrir innkaupabeiðnir.

## <a name="example-1-route-a-purchase-requisition-as-a-single-document-for-review"></a>Dæmi 1: Leið innkaupabeiðni sem einu skjali til yfirferðar
Eftirfarandi skýringarmynd sýnir hvernig innkaupabeiðni getur fara í gegnum endurskoðunarferli verkflæðis sem eitt skjal. Línur á innkaupabeiðninni er ekki settar í leið hver fyrir sig. Í þessu dæmi er eftirfarandi hlutverk teknar með í verkflæðisferlinu:

-   **Umsækjandinn** – notandinn sem biður um vörur eða þjónustu. Umsækjanda getur undirbúa innkaupabeiðnina eða annars starfsmaður getur undirbúa innkaupabeiðni fyrir hönd umsækjanda. Þessi starfsmaður er sá undirbúningsaðili. Undirbúningsaðili er ábyrgur fyrir stjórnun innkaupabeiðni í gegnum yfirferðarferlið. Aðeins undirbúningsaðili innkaupabeiðnina má breyta henni.

**Athugasemd** Starfsmaður verður að hafa viðeigandi heimildir til að stofna innkaupabeiðni fyrir hönd einhvers annars. Nota skal **heimild innkaupabeiðnar** síðu til að setja upp þessar heimildir.

-   **Innkaupaaðilinn** – notandinn sem framkvæmir innkaupayfirferð og getur samþykkja skjalið.
-   **Stjórnandi umsækjanda** – notandinn sem framkvæmir stjórnandayfirferð og getur samþykkja skjalið.

![endurskoðunarferli fyrir verkflæði innkaupabeiðni](./media/purchreqworkflowoverview_submission.gif)  
Í þessu dæmi fylgir verkflæðiferlið fyrir innkaupabeiðni þessum skrefum:

1.  Undirbúningsaðili sendir innkaupabeiðni til yfirferðar
2.  Innkaupaaðilinn fær tilkynningu. Innkaupaaðilinn fær tilkynningu sem biður innkaupaaðilinn um að staðfesta upplýsingarnar í innkaupabeiðninni. Ef nauðsynlegar upplýsingar vantar, getur innkaupaaðili annað hvort bætt upplýsingar við eða endursent innkaupabeiðnina til undirbúningsaðili til að bæta því við. Þegar allar nauðsynlegar upplýsingar hafa verið fyllt út heldur innkaupabeiðnin áfram í næsta skref í endurskoðunarferlinu.
3.  Stjórnandi umsækjandans fer yfir innkaupabeiðnina. Innkaupabeiðni gæti verið sett í leið til stjórnanda umsækjanda ef, til dæmis, upphæð innkaupabeiðni fer yfir eyðsluþak umsækjanda fyrir innkaupabeiðnir. Stjórnandi umsækjanda geta samþykkt eða hafnað innkaupabeiðninni eða endursent hana til undirbúningsaðili fyrir breytingar.

## <a name="example-2-route-the-individual-purchase-requisition-lines-for-review"></a>Dæmi 2: Vísa einstakar innkaupabeiðnilínur til yfirferðar
Eftirfarandi dæmi sýnir hvernig einstakar innkaupabeiðnilínur má setja í leið í gegnum verkflæði. Almennt séð, er Ferli fyrir hverja línu það sami og ferli fyrir innkaupabeiðni sem farið er yfir sem eitt skjal. Hins vegar verður hver lína að ljúka verkflæðisferlið fyrir sig áður en hægt er að ljúka verkflæði fyrir innkaupabeiðni í heild.  

Í þessu dæmi, starfsmaður færir inn beiðni fyrir veggspjöld og stuttermaboli fyrir markaðsherferð. Kostnaður á veggspjöldum er skipt á milli markaðsdeildar og söludeildar. Ef kostnaður vegna veggspjalda eða stuttermabola fer yfir ráðningartakmarkanir fyrir stjórnendur deildanna verður innkaupabeiðnin einnig að vera endurskoða af stjórnanda hópsins.  

Í þessu dæmi er eftirfarandi hlutverk teknar með í verkflæðisferlinu:

-   **Umsækjandinn** – notandinn sem biður um vörur eða þjónustu. Umsækjanda getur undirbúa innkaupabeiðnina eða annars starfsmaður getur undirbúa innkaupabeiðni fyrir hönd umsækjanda. Þessi starfsmaður er sá undirbúningsaðili. Undirbúningsaðili er ábyrgur fyrir stjórnun innkaupabeiðni í gegnum yfirferðarferlið. Aðeins undirbúningsaðili innkaupabeiðnina má breyta henni.

**Athugasemd** Starfsmaður verður að hafa viðeigandi heimildir til að stofna innkaupabeiðni fyrir hönd einhvers annars. Nota skal **heimild innkaupabeiðnar** síðu til að setja upp þessar heimildir.

-   **Innkaupaaðilinn** – notandinn sem framkvæmir innkaupayfirferð og getur samþykkja skjalið.
-   **Stjórnandi umsækjanda** – notandinn sem framkvæmir stjórnandayfirferð og getur samþykkja skjalið.
-   **Deildarstjórinn**– notandinn sem framkvæmir yfirferð á útgjöldum og getur samþykkja skjalið.
-   **Hópstjórinn** – notandinn sem framkvæmir endurskoðun fyrir undirskriftarvald og getur samþykkja skjalið.

![endurskoðunarferli fyrir Verkflæði innkaupabeiðnilína](./media/purchreqlineworkflowoverview.gif)  
Í þessu dæmi inniheldur verkflæðiferlið fyrir innkaupabeiðnilínur þessi skrefum:

1.  Undirbúningsaðili sendir innkaupabeiðni til yfirferðar Hverri lína er sett í leið til yfirlesara sem er skilgreindur í verkflæðisferlinu.
2.  Innkaupaaðilinn fær tilkynningu. Innkaupaaðilinn fær tilkynningu sem biður innkaupaaðilinn um að staðfesta upplýsingarnar í innkaupabeiðninni og á innkaupabeiðnilínunum. Þegar innkaupabeiðnin er opnuð af innkaupaaðilinn eru allar línur sjáanlegar en sjónrænn vísir sýnir hvaða línur hafa verið send til innkaupaaðilinn til skoðunar. Ef nauðsynlegar upplýsingar vantar, getur innkaupaaðili annað hvort bætt upplýsingar við eða endursent innkaupabeiðnilínuna til undirbúningsaðili til að bæta því við. Þegar allar nauðsynlegar upplýsingar hafa verið fyllt út heldur innkaupabeiðnilína áfram í næsta skref í endurskoðunarferlinu. Innkaupabeiðnilínur getur haldið áfram í gegnum yfirlestrarferlið óháð hvor við aðra.
3.  Stjórnandi línu umsækjandans fer yfir innkaupabeiðnilínurnar og samþykkir þær. Samþykktin gæti verið sett í leið til stjórnanda umsækjanda ef, til dæmis, upphæð innkaupabeiðnilínu fer yfir eyðsluþak umsækjanda við fyrir innkaupabeiðnilínur. Stjórnanda getur samþykkja eða hafnað einni eða báðum í innkaupapöntunarlínum.
4.  Deildarstjóri fyrir markaðsdeild endurskoðar innkaupabeiðnilínur fyrir bæði veggspjöld og stuttermaboli. Deildarstjóri söludeildar fer yfir innkaupabeiðnilínu aðeins fyrir veggspjöld, þar sem það er eini kostnaður sem er gjaldfæra í söludeild.
5.  Stjórnandi hópsins fer yfir og samþykkir innkaupabeiðnilínu fyrir stuttermaboli aðeins ef krafist er samþykkis stjórnandi hóps vegna, til dæmis, upphæð á línu innkaupabeiðninnar er hærri en í samþykkistakmörk deildarstjóra. Hópstjóri þarf ekki að samþykkja innkaupabeiðnilínu á veggspjöld.

## <a name="configuring-a-workflow-for-purchase-requisitions"></a>Skilgreina verkflæði fyrir innkaupabeiðnir
Til að vísa innkaupabeiðnina til endurskoðunar, þarf að skilgreina ferli verkflæðiferli innkaupabeiðninnar. Verkflæðisskilgreiningin sem þú skilgreinir stjórnar samspilinu milli notandans sem bað um vörurnar (umsækjandans) og yfirlesarans og samþykkjandans í verkflæðinu. Leið sem innkaupabeiðnin fer fer eftir skilyrðum sem eru tilgreind í verkflæðisskilgreiningunni. Til dæmis þessara skilyrða ákvarða hvenær innkaupabeiðnir ætti að setja í leið, notandi eða hlutverk sem ætti að leiða hana til, og aðgerðir sem notendur geta framkvæmt.  

Dæmin í þessu efnisatriði lýsa hvernig innkaupabeiðni er hægt að setja í leið í gegnum verkflæði sem eitt skjal eða einstakar innkaupabeiðnilínur. Einnig er hægt að skilgreina verkflæði fyrir innkaupabeiðnir til að endurspegla yfirferð innra eftirlits fyrir innkaupabeiðnir sem er skilgreind fyrir fyrirtækið.  

Yfirlesarar eða þáttakendur sem verkefni er úthlutað til í verkflæðis geta verið meðlimir tiltekinn notendaflokk, notendur sem hafa tiltekna öryggishlutverk, notendum sem tengjast innsendingaraðila í á stjórnendastigveldi eða nefndir notendur eða notendur sem hafa ábyrgð á tiltekinni útgjöld.

### <a name="purchase-requisition-expenditure-reviewers"></a>Yfirlesarar fyrir útgjöld innkaupabeiðna

skilgreiningu skoðunarmanns leyfa þér að setja útgjalda í leið á gagnvirkan hátt fyrir endurskoðun, á grundvelli notandans sem er úthlutað á verkhlutverki eða fjárhagsvídd þar sem útgjöldin eru gjaldfærð. Verkflæðisferlið notar tilgreindan eiganda verkhlutverks eða fjárhagsvíddar til að ákvarða hvert á að senda útgjöldin.  

Hægt er að tilgreina eina eða fleiri skilgreiningar skoðunarmanns útgjalda og síðan velja skilgreiningu þegar verkflæði er stofnað. Hægt er að skilgreina gildi skoðunarmanns útgjalda fyrir hvern lögaðila í fyrirtækinu. Eftir að þú hefur skilgreint skilgreiningar fyrir skoðunarmanns útgjalda má úthluta skilgreiningunni á verkflæðisverk.  

Ekki þarf að setja upp skilgreiningu fyrir skilgreining skoðunarmanns útgjalda. Þess í stað er Hægt að úthluta tilteknum notanda eða notendaflokki sem skoðunarmanns þegar verkflæðið er skilgreint. Hinsvegar, Ef fyrirtækið er flókið geta skoðunarmaður útgjalda aukið skilvirkni samþykktarferlis. Þar að auki, ef sett er upp skoðunarmenn útgjalda, þarf ekki að uppfæra verkflæði fyrir verkefni skoðunarmanns í hvert skipti sem skoðunarmaður breytir um vinnuhlutverk.  

Hægt er að setja upp skoðunarmaður útgjalda á **skoðunarmaður útgjalda fyrir Innkaupabeiðni** síðunni. Stofna skilgreining skoðunarmanns útgjalda og færa inn gildin fyrir hvern lögaðila í þínu fyrirtækið. Fyrir innkaupabeiðnir sem eru tengdir við verk, er hægt að tilgreina það hlutverk sem er ábyrgur fyrir að endurskoða innkaupabeiðnunum: verkstjóri, verkstjórnandi eða sölustjórnandi Verks. Útgjöldum verða sett í leið til þess notanda sem hefur fengið það hlutverk úthlutað. Einnig er hægt setja útgjöldum í leið til eiganda fjárhagsvíddar með því að velja viðeigandi valkost fyrir fjárhagsvídd á flipanum **dreifing á fyrirtæki**.  

Til að nota einn af skoðunarmaður útgjalda sem sett eru upp í verkflæði, verður að setja í **Gerð þátttakanda** valkostinn á **þátttakendur í Útgjöldum** í á **Úthlutun** eiginleika fyrir viðkomandi verkflæðiseiningu.

<a name="additional-resources"></a>Frekari upplýsingar
--------

[Stofna beiðni um notkun](tasks/create-requisition-consumption.md)

[Skilgreina viðskiptaferli verkflæði fyrir innkaupabeiðnir](https://mbs.microsoft.com/customersource/Global/AX/learning/documentation/white-papers/Defining_business_process_workflows_for_purchase_requisitions)

[Verkflæði innkaupa og aðfanga](procurement-sourcing-workflows.md)

[Yfirlit yfir innkaupabeiðni](purchase-requisitions-overview.md)



