---
title: Stofna beiðni um tilboð
description: Þessi verklýsing sýnir hvernig á að stofna beiðni um tilboð.
author: GalynaFedorova
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchRFQCaseTableListPage, PurchCreateRFQCase, InventLocationIdLookup, PurchRFQCaseTable, InventItemIdLookupSimple, EcoResCategorySingleLookup, UnitOfMeasureLookup, PurchRFQEditLines, PurchRFQEditLinesPrintOptions, VendRFQJournal, SrsReportViewerForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aed08083d83a47d914ecd6c9421825163c5c467a
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/03/2022
ms.locfileid: "8673832"
---
# <a name="create-a-request-for-quotation"></a>Stofna beiðni um tilboð

[!include [banner](../../includes/banner.md)]

Þessi verklýsing sýnir hvernig á að stofna beiðni um tilboð. Þetta verk myndi yfirleitt gert af innkaupaaðila. Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF eða með því að nota eigin gögn. Þú Þarft að hafa sett upp beiðnigerðir áður en byrjað er. Þegar þessu verki hefur verið lokið og þú hefur stofnað og sent tilboðsbeiðni er hægt að færa svör fyrir hvern lánardrottinn, gera samanburð á þeim og veita samninga.


## <a name="prepare-a-new-rfq"></a>Útbúa skal nýja beiðni um tilboð
1. Farðu í **Skoðunarrúðu > Kerfiseiningar > Innkaup og aðföng > Beiðnir um tilboð > Allar beiðnir um tilboð**.
2. Smellt er á **Nýtt**.
    Eftirfarandi gerðir innkaupa eru tiltækar: Innkaupapöntun (það er sjálfgefið): skjal sem staðfestir tilboð um að kaupa afurðir, eða samþykki tilboðs um að selja afurðir in skiptum fyrir greiðslu. Innkaupabeiðni – Þessi gerð er sjálfkrafa valin ef stofna á tilboðsbeiðni beint úr innkaupabeiðni. Ef þessi valkostur er valinn handvirk kemur upp villa. Innkaupasamningur - samningur um að kaupa ákveðið magn eða virði vöru yfir tíma. Ef þessi valkostur er valinn verður að velja dagsetningabilið sem á við innkaupasamninginn.  
3. Í reitinn **Titill skjals** skal slá inn gildi.
4. Í reitinn **Gerð beiðni** slærðu inn eða velur gildi.
    + Ef aðferð við stigagjöf er tengd gerð beiðni verður hún sjálfgefin aðferð við stigagjöf fyrir tilboðsbeiðni sem verið er að stofna. Þá er mögulegt að breyta aðferð við stigagjöf seinna.  
    + Í reitinn **Afhendingardagur** færirðu inn dagsetningu.  
    + Velja skal þá dagsetningu þegar á að taka á móti afurðunum.  
    + Í reitinn **Lokadagur og gildistími** færirðu inn dagsetningu og tíma.  
    + Tilgreina skal dagsetninguna og tímann innan hvers lánardrottnar verða svara beiðni um tilboð.  
5. Í reitnum **Vöruhús** slærðu inn eða velur gildi. Afhendingaraðsetur mun vera sjálfgefið aðsetur vöruhússins.  
6. Smellt er á **OK**.

## <a name="add-lines"></a>Bæta við línum

Eftir að þú hefur tilgreint grunnupplýsingar um tilboðsbeiðnir þínar tilgreinir þú vörur eða þjónustu sem þú vilt að lánardrottnar geri tilboð í. Þetta er sjálfgefin línugerð.

1. Í reitinn **Vörunúmer** skal slá inn eða velja gildi. Ef verið er að nota USMF er hægt að velja 'T0020'.  
2. Í reitnum **Magn** slærðu inn tölu.
3. Smella á **Bæta við línu**.
4. Í reitnum **Gerð línu** velurðu „Flokkur“. Hægt er að nota línugerðina Tegund til að stofna Tilboðsbeiðnir fyrir vörur eða þjónustu sem eru ekki hluti af birgðum. Svo þarf að velja gerð af vörur eða þjónustu úr stigveldi innkaupaflokka.  
5. Í reitinn **Innkaupaflokkur** slærðu inn eða velur gildi.
6. Í reitinn **Afurðarheiti** skal slá inn gildi.
7. Í reitnum **Magn** slærðu inn tölu.
8. Í reitinn **Eining** skal slá inn eða velja gildi.

## <a name="add-vendors"></a>Bæta við lánardrottnum
1. Smelltu á **Haus** til að breyta úr línuyfirliti í hausyfirlit. 
2. Útvíkkaðu hlutann **Lánardrottinn**.
3. Smelltu á **Bæta lánardrottnum sjálfkrafa við.** Þú getur bæta lánardrottnum á beiðni um tilboð sjálfkrafa samkvæmt innkaupategund umbeðnu varanna. Ef það eru engir lánardrottnar samþykkt fyrir tegundum í línum er hægt að bæta lánardrottnum við handvirkt.  
4. Smelltu á **Bæta við**.
5. Í reitinn **Lánardrottnalykill** skal færa inn eða velja gildi.
6. Smelltu á **Bæta við**.
7. Í reitinn **Lánardrottnalykill** skal færa inn eða velja gildi. Þegar lánardrottinn hefur verið valinn er staðan Stofnuð. Upplýsingar lánardrottinsins hafa samkvæmt þessu verið vistaðar í beiðninni um tilboð, en notandi hefur ekki sent beiðni um tilboð til lánardrottins. Hægt er að bæta lánardrottni við tilboðsbeiðni óháð stöðu lánardrottins.  

## <a name="send-the-rfq-to-vendors"></a>Senda beiðni um tilboð til lánardrottna
1. Í **aðgerðasvæðinu** er smellt á **Senda**. Í síðunni senda beiðni um tilboð skal gengið úr skugga um að lánardrottnar í listanum séu þeir sem á að senda tilboðsbeiðni til.  
2. Smelltu á **Prenta**. Þessi svargluggi gerir notanda kleift að prenta beiðni um tilboð. Ef kosið er að prenta svarblað er innihald þessa skilgreint í færibreytum innkaupa og aðfanga. Til að velja hvernig á að prenta svarblöð, þegar búið er að opna prentglugga smellirðu á Ítarlegir prentunarvalkostir. Ein beiðni um tilboð verður prentuð fyrir hvern lánardrottinn sem inniheldur línur sem hafa stöðuna Stofnað eða Sent. Línur sem hætt var við og línur með skráðum svörum verða ekki prentaðar.   
3. Smelltu á **Hætta við**.
4. Smellt er á **OK**.
5. Lokið síðunni.
6. Lokið síðunni.

## <a name="view-the-rfq-journal"></a>Skoða færslubók tilboðsbeiðna
1. Fara í **innkaup og aðföng > Beiðnir um tilboð > eftirfylgni við Beiðni um tilboð > Færslubækur beiðna um tilboð**.
2. Smelltu á **Forskoða/prenta**.
3. Smelltu á **forskoðunina Upprunalegt**.
4. Lokið síðunni.
5. Lokið síðunni.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]