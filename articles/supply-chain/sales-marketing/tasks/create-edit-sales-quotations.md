---
title: Stofna og breyta sölutilboðum
description: Þetta ferli sýnir hvernig á að stofna og uppfæra sölutilboð.
author: omulvad
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesQuotationListPage, SalesCreateQuotation, SalesQuotationTable, SalesQuotationTotals, SalesQuotationPriceSimulation, SalesQuotationEditLines, SrsReportViewerForm, smmSetNumSeqIfManual, CustTable, SalesTable, CustQuotationConfirmationJournal, CustQuotationJournal, CustSalesLines, SalesQuotationCopying, SalesQuotationDeleteQuotations, SalesQuotationListPagePreviewPane, SalesQuotationTypeGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 51e80cf500181601cf6e0d2910b91c429c404f01
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836447"
---
# <a name="create-and-edit-sales-quotations"></a>Stofna og breyta sölutilboðum

[!include [banner](../../includes/banner.md)]

Þetta ferli sýnir hvernig á að stofna og uppfæra sölutilboð. Hægt er að keyra þetta ferli á eigin gögn eða í sýnigögn USMF fyrirtækis.


## <a name="create-a-sales-quotation"></a>Stofna sölutilboð
1. Farðu í **Skoðunarrúðu > Kerfiseiningar > Sala og markaðssetning > Sölutilboð > Öll tilboð**.
2. Smellt er á **Nýtt**.
3. Í reitnum **Reikningsgerð** skaltu velja Viðfang.
4. Í reitnum **Viðfang** skaltu færa inn eða velja gildi.
5. Víkkaðu út hlutann **Almennt**. Þar sem valið var að stofna tilboð úr svæðinu Sölu- og markaðssetning er gerðin sjálfkrafa stillt á Sölutilboð. Til að stofna tilboð fyrir verk verðurðu að fara í það úr einingunni **Verkefnastjórnun og bókhald**.
6. Smellt er á **OK**. Svæði og aðgerðir í tilboðslínunum er mjög svipuð þær á sölupöntunarlínum.   Eins og sölupantanir er hægt að stofna tilboð fyrir tiltekna vöru eða þegar vörunúmerið er ekki þekkt eða er ekki til þegar tilboð var stofnað, hægt er að stofna tilboð fyrir söluflokk.     
7. Í reitinn **Vara** skal færa inn eða velja gildi.
8. Í reitinn **Svæði** skal slá inn gildi.
9. Í reitnum **Magn** slærðu inn tölu. Ef gildir viðskiptasamningar fyrir vöruna sem valin er á línunni eru til, verð og afslátt sjálfkrafa afritaðir í tilboðslínunni. Gangið úr skugga um að svæði einnigs inniheldur gildi og hægt er einnig að færa afsláttargildi ef óskað er. 
10. Smellt er á **Vista**.
11. Á **Aðgerðasvæðinu** er smellt á **Sölutilboð**.
12. Smelltu á **Samtölur**.
13. Smellt er á **OK**.
14. Veldu sölutilboðslínuna.
15. Á **aðgerðasvæðinu** er smellt á **Tilboð**.
16. Smelltu á **Verðhermingu**.
    - Í síðunni **Keyra verðhermingu** er hægt að gera tilraunir með leiðrétta áætlaðar tekjur eða arðsemisgreiningu af tilboði byggt á viðkomandi einingarverð, afsláttarupphæð, afsláttarprósenta, heildarupphæð, framlegð, eða framlegðarhlutfall. Þegar þú ert ánægður með tölur, nota sem tillaga fyrir tilboðslínuna og verðtengd svæði verða uppfærðar samkvæmt því.  
    - Hægt er að stofna eins margar verðhermingar og óskað er. Þegar smellt er á **Nýtt** eru verðskilyrði úr núgildandi tilboðslínu afrituð á síðuna. Síðan er hægt að breyta gildi í hvaða verð-tengdum svæðum í þau sem eru markmiðið. Breyting á eitt af svæðunum kveikir endurútreikningur í öllum öðrum svæðum. Til þess að reikna út framlegð sölu og framlegðarhlutfall, verður einingarkostnað afurðar að vera þekkt. Notið flipann hermunarverð fyrir ítarlegri yfirlit yfir upphaflegt verð, lögð til breytingar og áhrif þeirra á tilboðssamtölur. Almenna reglan er að þegar hermun stillir nýja upphæð er notað í tilboðslínunni, endurreiknar kerfið og færir inn nýtt gildi í reitinn einingarverð. Ef hermunina er byggð á nýja framlegð eða nýtt framlegðarhlutfall, er aðeins nettóupphæð svæðið er uppfært og einingarverð er autt. Í báðum tilvikum afsláttum sem voru í tilboðslínunni fyrir hermun verður eytt.
17. Á **aðgerðasvæðinu** er smellt á **Tilboð**.
18. Smelltu á **Senda tilboð**.
19. Veldu Já í reitnum **Prenta tilboð**.
20. Smellt er á **OK**. Skýrslan getur tekið mínútu til að mynda. Lokaðu ekki síðunni fyrr en það hefur verið gert.

## <a name="update-a-sales-quotation"></a>Uppfæra sölutilboð
1. Farðu í **Skoðunarrúðu > Kerfiseiningar > Sala og markaðssetning > Sölutilboð > Öll tilboð**.
2. Í **Aðgerðasvæðinu** skal smellt á **Fylgja eftir**.
3. Smelltu á **Umbreyta í viðskiptavin**.
4. Í reitinn **Viðskiptavinalykill** skal slá inn gildi.
5. Smelltu á **Villuleit**. Gangið úr skugga um að þú sjáir skilaboð um að fært inn í lykilnúmerið er frjálst til notkunar.  
6. Smellt er á **OK**. Kerfið hefur nú stofnað nýjan viðskiptavinalykil fyrir viðfang á tilboðinu.  
7. Lokið síðunni.
8. Í **Aðgerðasvæðinu** skal smellt á **Fylgja eftir**.
9. Smellið á **Staðfesta**.
10. Í reitinn **Ástæða** skal slá inn eða velja gildi.
11. Smellt er á **OK**.
12. Á **aðgerðasvæðinu** er smellt á **Almennt**.
13. Smelltu á **Sölupantanir**.
14. Lokið síðunni.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]