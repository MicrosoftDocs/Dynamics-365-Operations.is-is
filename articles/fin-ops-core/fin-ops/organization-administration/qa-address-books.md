---
title: Algengar spurningar um aðsetursbækur
description: Þetta efnisatriði veitir svör við algengum spurningum tengdum aðsetursbókum.
author: msftbrking
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DirPartyCheckDuplicate, DirPartyTable
audience: Application User
ms.reviewer: sericks
ms.custom: 23601
ms.assetid: b177fa0f-ac9a-415e-9498-15438e132f60
ms.search.region: Global
ms.author: brking
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 60e6fb7d38bd3ca78538ca10a15f6fb09bba52a3
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693905"
---
# <a name="address-books-faq"></a>Algengar spurningar um aðsetursbækur

[!include [banner](../includes/banner.md)]

## <a name="how-do-i-check-for-duplicate-records"></a>Hvernig leita ég að tvíteknum skráasafnsfærslum?

Hægt er að leita að tvíteknum færslum beint úr listasíðunni **Altæk aðsetursbók**. Á aðgerðasvæðinu, í flipanum **Aðili**, í hópnum **Vinna með**, smellið á **Leita að tvítekningum**. Veljið svo gildin sem á að taka með í athugun tvítekninga.

## <a name="can-i-bulk-add-or-delete-party-records-from-an-address-book"></a>Er hægt að bæta við eða eyða skrám aðila úr aðsetursbók í magni?

Já, hægt er að bæta mörgum aðilafærslum í aðsetursbók og fjarlægja einnig margar aðilafærslur.

- Til að bæta mörgum aðilafærslum í aðsetursbók, skal, á listasíðunni **Altæk aðsetursbók** velja þá aðila í listanum. Síðan skal, í Aðgerðarrúðunni, á flipanum **Aðili** í hópnum **Vinna með** smella á **Úthluta aðilum**. Veljið aðsetursbækur sem á að bæta völdum aðilafærslum við og smellið síðan á **Í lagi**. Öllum völdum aðilafærslum er bætt við valdar aðsetursbækur.
- Til að fjarlægja margar aðilafærslur úr aðsetursbók, skal, á listasíðunni **Altæk aðsetursbók** velja þá aðila í listanum. Síðan skal, í Aðgerðarrúðunni, á flipanum **Aðili** í hópnum **Vinna með** smella á **Fjarlægja aðila**. Veljið aðsetursbækur þaðan sem fjarlægja á aðila, og smellið síðan á **Í lagi**. Allar valdar aðilafærslur eru fjarlægðar úr völdum aðsetursbókum.

## <a name="can-i-change-the-party-type-of-a-record-or-do-i-have-to-delete-the-old-record-and-create-a-new-one"></a>Er hægt að breyta gerð færslu aðila eða þarf að eyða gömlum færslunni og stofna nýja?

Einstaka sinnum gæti þurft að breyta gerð°færslu úr einstaklingur í fyrirtæki eða úr fyrirtæki í einstaklingur. Til dæmis er Nancy meðlimur söluhópsins fyrir Fabrikam U.K. Á sölusýningu í London, hittir hún sex ný viðföng. Nancy stofnar viðfangsfærslu aðila fyrir hvert viðfang. Þegar Nancy vistar færslurnar, er hver færsla einnig stofnuð í altæku aðsetursbókinni. Fabrikam hefur sett sjálfgefna aðilagerð á fyrirtæki en tvö nýju viðfanganna ættu að hafa færslugerð einstaklings. Þess vegna þarf Nancy, þegar hún kemur til baka frá sölusýningunni, að breyta gerð aðila í þessum tveimur viðfangsfærslum. Til að breyta færslu aðila úr einni gerð aðila í aðra, verður fyrst að stofna nýja færslu aðila af réttri gerð í altæku aðsetursbókinni. Síðan þarf að tengja°eldri færslu aðila við þessa nýja færslu. Eftir að hafa framkvæmt nýja tengingu aðila, þarf að eyða upprunalegri aðilafærslu sem hefur ranga færslugerð.

## <a name="how-do-i-change-the-name-or-address-of-a-party-record"></a>Hvernig á að breyta heiti eða aðsetri aðilafærslu?

Hægt er að uppfæra heiti aðilafærslu og aðsetur sem tengjast færslunni, hvenær sem er.

- Opna færslu aðila til að uppfæra heiti aðilafærslu, og smellið síðan á **Breyta** á Aðgerðarúðunni. Á flýtiflipanum **Almennt**, skal°færa inn nýtt heiti fyrir aðila og vista svo færsluna.
- Til að uppfæra aðsetur aðilafærslu, skal opna aðilafærsluna og svo velja aðsetur til að uppfæra á flýtiflipanum **Aðsetur**. Smellið á **Breyta**, og síðan, á **Breyta aðsetri** síðunni, er hægt að gera nauðsynlegar breytingar á aðsetri eða aðsetursfæribreytum.

## <a name="can-i-merge-two-or-more-party-records-into-one-record"></a>Er hægt að sameina tvær eða fleiri aðilafærslur í eina færslu?

Einstaka sinnum gæti verið óskað eftir að sameina tvær eða fleiri aðilafærslur í eina færslu. Þetta getur gerst ef búin hefur verið til ein eða fleiri tvíteknar aðilafærslur, annaðhvort viljandi eða óvart. Þegar verið er að sameina aðilafærslur skal velja eina skrá til að halda. Upplýsingar úr öðrum færslum eru svo sameinaðar í þessari færslu. Til dæmis kemur í ljós að upplýsingar um Fabrikam eru geymdur í þremur aðilafærslum; A, B og C. Ákveðið er að halda aðilafærslu A. Þess vegna verða°upplýsingarnar sem eru geymdar í aðilafærslum B og C sameinaðar í aðilafærslu A. Við ákveðnar aðstæður er ekki hægt að sameina aðilafærslur:

- Ekki er hægt að sameina aðilafærslur sem eru tengdar við sama aðilahlutverk, eins og viðskiptavin eða lánardrottinn í sama lögaðila. Til dæmis er aðili A tengdur við viðskiptavin í lögaðilanum 123 og aðili B er tengdur við annan viðskiptavin í lögaðilanum 123. Ekki er hægt að sameina þessar aðilafærslur því ef þær væru sameinaðar yrði sameinaða aðilafærslan tengdu við marga viðskiptavini með sama lögaðila og það er ekki leyft. Hins vegar er hægt að sameina færslurnar ef aðili B er tengdur lánardrottni°lögaðila°123 eða viðskiptavini í öðrum lögaðila.
- Ekki er hægt að sameina færslur innri aðila fyrirtækis í sama lögaðila, hóp eða rekstrareiningu.

## <a name="should-i-create-a-party-record-in-the-global-address-book-or-in-another-place-such-as-the-customer-or-vendor-page"></a>Á ég að stofna færslu aðila í altæku aðsetursbókinni eða á öðrum stað, eins og Viðskiptavin eða Lánardrottinn síðu?

Hægt er að færa inn aðilafærslur annað hvort°í altæku aðsetursbókina eða á viðeigandi einingarsíðu. Þegar færslu er bætt við í einni staðsetningu, er sömu færslu ávallt bætt í hinni staðsetningunni. Til dæmis, ef aðilafærslu fyrir viðskiptaviner bætt í altæka aðsetursbók, er færslunni einnig°bætt við á síðunni **Viðskiptavinur**. Á sama hátt, ef aðilafærslu er bætt við fyrir viðskiptavin á síðunni **Viðskiptavinur** er færslunni einnig bætt við í altæka aðsetursbók. Notið eftirfarandi leiðbeiningar til að ákveða hvar eigi að færa inn nýjar aðilafærslur:

- **Stofna aðilafærslu þegar einingargerð er ekki þekkt** – Ef verður að stofna aðilafærslu°en einingargerð er ekki þekkt (til dæmis er ekki vitað hvort einingin er viðskiptavinur eða tækifæri), skal stofna færslu í altæku aðsetursbókinni. Hægt er að velja einingargerð síðar.
- **Stofna aðilafærslu þegar einingargerð er þekkt** - Ef einingargerð aðila er þekkt er hægt að stofna færslu á viðeigandi síðu fyrir þá gerð. Til dæmis skal stofna færslu fyrir viðskiptavin á síðunni **Viðskiptavinur**. Þegar færsla er stofnuð og vistuð með því að nota viðeigandi einingarsíðu er færslan stofnuð sjálfkrafa í altæku aðsetursbókinni.

## <a name="can-i-translate-address-information-for-party-records"></a>Er hægt að þýða upplýsingar um aðsetur fyrir aðilafærslur?

Hægt er að setja upp þýðingar á upplýsingum um aðsetur,°þannig að upplýsingarnar birtast á tungumáli notanda (kerfistungumál) í forritinu en á öðru tungumáli í skjölum s.s. sölupöntunum. Hægt er að færa inn þýðingar fyrir heiti lands/svæðis, málefni aðseturs og nafnaraðir. Til dæmis er tungumál kerfis er danska og sölupöntun er stofnuð fyrir viðskiptavin í Frakklandi. Í þessu tilfelli er hægt að skoða færslu viðskiptavinar á dönsku í forritinu en birta upplýsingar um aðsetur á frönsku í prentuðu sölupöntuninni. Þegar settar eru upp þýðingar ætti að færa inn þýðingu fyrir hverja vöru í lista. Allar vörur sem ekki eru færðar inn þýðingar fyrir munu birtast í tungumáli kerfisins. Til dæmis þegar tungumál kerfis er danska og skjal er sent viðskiptavini á Spáni. Ef ekki hafa verið færðar inn þýðingar á spænsku (ESP) fyrir upplýsingar um aðsetur munu þær upplýsingar birtast á dönsku bæði í forritið og prentaða skjalinu.
