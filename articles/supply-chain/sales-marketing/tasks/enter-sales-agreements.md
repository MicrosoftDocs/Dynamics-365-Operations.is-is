---
title: Færa inn sölusamninga
description: Þetta efni útskýrir hvernig stofna á sölusamning sem bindur sig einum viðskiptavini til að kaupa vöru fyrir samþykkta upphæð yfir tíma í skiptum fyrir sérstakan afslátt.
author: Henrikan
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesAgreementListPage, SalesAgreementCreate, SalesAgreement, InventItemIdLookupSimple, AgreementConfirmRunForm, SrsReportViewerForm, SalesAgreementCustomerReferencesPart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Service industries
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ee2c1494842c5fd2aa598546ba655c33d6fd3f16
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7568304"
---
# <a name="enter-sales-agreements"></a>Færa inn sölusamninga

[!include [banner](../../includes/banner.md)]

Þetta efni útskýrir hvernig stofna á sölusamning sem bindur sig einum viðskiptavini til að kaupa vöru fyrir samþykkta upphæð yfir tíma í skiptum fyrir sérstakan afslátt. Hægt er að keyra þessa ferli í sýnifyrirtækinu USMF eða í eigin gögnum.


## <a name="set-up-sales-agreement-header"></a>Setja upp Haus sölusamnings
1. Í skoðunarrúðunni ferðu í **Einingar > Sala og markaðssetning > Sölusamningar > Sölusamningar**.
2. Veljið **Nýtt**.
3. Í reitnum **Viðskiptavinalykill** velurðu skrána sem óskað er eftir af fellivalmyndinni.
4. Í reitnum **Flokkun sölusamninga** velurðu skrána sem óskað er eftir af fellivalmyndinni.
5. Víkkaðu út hlutann **Almennt**.
6. Í reitnum **Sjálfgefin ráðstöfun** skal velja **Ráðstöfunarvirði afurðar**. Ráðstöfunargerð er áskilið skilyrði sem þarf að tengja við samninginn til að skilgreina hvernig verður að uppfylla samnings. Fjögur áður skilgreindar gerðir gera þér kleift að setja upp markmið viðskiptavinarins um ráðstöfun, sýnt sem magn eða gildi. Aðeins má nota magn ráðstöfunargerðar á tiltekinni vöru, en gerðir byggt á gildi á við um sölu á bæði tilteknar og ótilteknar vörur.  
7. Í reitnum **Lokadagur** skal stilla dagsetninguna í framtíðardagsetningu þegar samningurinn er að renna út.
8. Veljið **Í lagi**.

## <a name="set-up-product-value-commitment-lines"></a>Setja upp afurðargildi skuldbindingarlína
1. Veldu **Bæta við línu**.
2. Í reitnum **Vörunúmer** velurðu skrána sem óskað er eftir af fellivalmyndinni. Gerð ráðstöfunar sem valin er fyrir samninginn hefur áhrif á þær upplýsingar sem þú getur fært inn fyrir samningslínur. Til dæmis, fyrir samning sem byggist á virði verður að tilgreina samtals nettóupphæð (í gjaldmiðli sem samið var um) sem viðskiptavinur bindur sig að kaupa vörur fyrir. Í þessu dæmi eru reitirnir **Magn** og **Eining** í línunni ótiltækir þar sem verið er að stofna samning fyrir viðskiptavin sem á að kaupa sérstakt gildi afurðar.   
3. Í reitnum **Nettóupphæð** skal slá inn peningaupphæð sem viðskiptavinurinn hefur ráðstafað í kaup.
4. Í reitnum **Afsláttarprósenta** skal færa inn gildi prósentu sem á við sölupöntunarlínur viðskiptavinarins sem tengjast þessum samningi.
5. Útvíkkaðu hlutann **upplýsingar Línu**.
6. Velja skal **Já** í reitinn **Hámarki er framfylgt**.
    - Val á **Hámarki er framfylgt** þýðir að heildarupphæð allra sölupöntunarlínanna sem nota sérstakt verð ráðstöfunar, afslátt og/eða greiðsluskilmála má ekki fara yfir upphæðina sem er tilgreind í ráðstöfuninni.  
    - Lágmarks- og hámarks losunarupphæðir tilgreina svið gilda sem verður selt á hverja sölupöntun sem notar valinn samning.   
7. Útvíkkaðu hlutann **Haus sölusamnings**. Nema staða samnings sé stillt á **Gildur**, er ekki hægt að tengja sölupantanir við samning og þar af leiðandi ekki stuðla að uppfyllingu á þeim samningi. Hægt er að breyta stöðunni handvirkt á þessu stigi. Þó væri myndi yfirleitt breyta stöðu þegar samnings fyrir viðskiptavin er staðfest.  
8. Á Aðgerðasvæðinu skal velja **Sölusamningur**.
9. Veldu **Staðfesting**. Gangið úr skugga um að valkosturinn **Merkja samning sem gildan** sé stilltur á **Já**.  
10. Velja skal **Já** í reitnum **Prenta skýrslu**.
11. Veljið **Í lagi**.
12. Lokið síðunni. Samningurinn er nú gildur. Hægt er að hefja tengingu á pöntunum viðskiptavina við samning til mótfærslu við skuldbindingarmarkið.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]