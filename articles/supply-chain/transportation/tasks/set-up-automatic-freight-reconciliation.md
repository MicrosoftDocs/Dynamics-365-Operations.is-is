--- 
title: "Setja upp sjálfvirka afstemmingu farms"
description: "Þessi verklýsing sýnir hvernig á að setja upp gögn fyrir sjálfvirka afstemmingu farms."
author: BibiSp
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 97f0c4d8fe06ab2fc252b9543cb688306214c79f
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-automatic-freight-reconciliation"></a>Setja upp sjálfvirka afstemmingu farms

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Þessi verklýsing sýnir hvernig á að setja upp gögn fyrir sjálfvirka afstemmingu farms. Þetta er yfirleitt gert af stjórnanda vöruhúss. Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF.


## <a name="set-up-the-freight-bill-type"></a>Setja upp gerð farmbréfs
1. Fara í flutningsstjórnun > Uppsetningu > afstemmingu Farms > gerð farmbréfs.
    * Farmbréfið skilgreinir hvernig farmbréf og reikninga flutningsaðila ætti að jafna þær.  
2. Smellið á „Nýtt“.
3. Sláið inn gildi í reitnum Farms uppskrift gerð.
4. Í svæðinu samsetning Vélar, slærðu inn 'Microsoft.Dynamics.Ax.Tms.Bll.GenericNormalizer'.
    * Þetta er stöðluð Flutningsmáta stjórnun samsvarandi vél kóða safnið.  
5. Í svæðinu Vélaklasi, slærðu inn 'Microsoft.Dynamics.Ax.Tms.dll'.
    * Þetta er stöðluð Flutningsmáta stjórnun samsvarandi vél kóða safnið.  
6. Smellið á „Nýtt“.
7. Lýsingarsvæði, að velja gildið sem ættu að stemma á farmbréfið og reikning flutningsaðila.  
8. Velja skal Já í svæðinu Jöfnun áskilin.
    * Ef þetta svæði var stillt á Já þetta merkir að gildið sem er valin í svæðinu Lýsingu verður að vera jöfn á farmbréfið og reikning flutningsaðila. Ef það var stillt á Nei, svæðið má vera autt á eina af þeim.  
9. Smellið á „Vista“.

## <a name="set-up-the-freight-bill-type-assignment"></a>Setja upp úthlutanir á gerð farmbréfs
1. Lokið síðunni.
2. Fara í flutningsstjórnun > Uppsetningu > afstemmingu Farms > úthlutun á gerð farmbréfs.
    * Úthlutun á gerð farmbréfs er notuð til að tilgreina hvaða gerð farmbréfs er notað fyrir tiltekna flutningsaðila.   
3. Smellið á „Nýtt“.
4. Sláið inn eða veldu gildi í reitnum Hamur.
5. Sláið inn eða veldu gildi í reitnum Farmflytjandi.
6. Í reitnum gerð Farmbréfs skal velja þá gerð farmbréfs sem þú varst að stofna.
7. Lokið síðunni.

## <a name="set-up-the-audit-master"></a>Setja upp endurskoðunarsniðmát
1. Fara í flutningsstjórnun > Uppsetningu > afstemmingu Farms > endurskoðunarsniðmát.
    * Aðalgögn endurskoðunar skilgreinir mörk verðvikmarka fyrir farmgjöld sjálfvirka afstemmingu. Hún tilgreinir með hversu mikið er upphæða á farmbréfið og flutningsaðila reiknings getur verið önnur og leyfa enn afstemmingu að eiga sér stað. Hann skilgreinir einnig hvernig á að meðhöndla misræmi.  
2. Smellið á „Nýtt“.
3. Í reitinn Kenni endurskoðunarsniðmáts skal færa inn gildi.
4. Í svæðinu farmflytjanda sendingar, velja sama farmflytjanda sem var áður.
5. Í reitnum gerð Farmbréfs skal velja þá gerð farmbréfs sem þú varst að stofna.
6. Víkkið út hlutann Vikmörk.
7. Færið inn tölu í svæðinu Lágmarks vikmörk.
8. Færið inn tölu í svæðinu Hámarks vikmörk.
9. Víkkið út hlutann Niðurstaða.
10. Í reitinn Ástæðukóði ofgreiðslu skal slá inn eða veldu gildi.
    * Ef upphæða sem eru mismunandi á farmbréfið og reikning flutningsaðila, tilgreina ofgreiðsla eða vangreiðsla ástæðukóða lykla sem á að skrá muninn á svo lengi sem mismunur er innan stig vikmarka.  
11. Í reitinn Ástæðukóði vangreiðslu skal slá inn eða veldu gildi.
12. Lokið síðunni.


