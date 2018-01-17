---
title: "Setja upp forsendur fyrir stjórnun"
description: "Notið þetta ferli til að virkja sjórnunarferli ósamkvæmni."
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 4bb4af7cb7aff101a8b9e6162823515f63b12886
ms.openlocfilehash: 9b5b05a3c00f093066a2714964bb99146427c3bc
ms.contentlocale: is-is
ms.lasthandoff: 11/02/2017

---
# <a name="set-up-prerequisites-for-management"></a>Setja upp forsendur fyrir stjórnun

[!include[task guide banner](../../includes/task-guide-banner.md)]

Notið þetta ferli til að virkja sjórnunarferli ósamkvæmni. Ósamkvæmni lýsir ferli eða vöru sem uppfyllir ekki gæðastaðla, þar sem uppruni og gerð vandamálsins eru í lýsandi upplýsingum. Þessi aðferð notar sýnifyrirtækið USMF. Þetta ferli er yfirleitt framkvæmt af starfsmanni á sviði gæða.


## <a name="enable-quality-management-processes-within-the-company"></a>Virkja ferli gæðastjórnunar innan fyrirtækisins:
1. Fara í Birgðastjórnun > Uppsetning > Birgðir og færibreytur vöruhúsakerfis.
2. Smellið á flipann gæðastjórnun.
3. Velja skal Já í svæðinu á Notkun gæðastjórnunar.
    * Veljið þessa færibreytu til að virkja ferli gæðastjórnunar fyrir fyrirtækið.  
4. Í reitinn Tímagjald skal slá inn númer.
    * Nota skal reitinn tímagjald til að færa inn tímagjald fyrir vinnu í gjaldmiðli landsins. Tímagjaldið er notuð til að reikna kostnað fyrir aðgerðir sem tengjast ósamkvæmni. Tímagjaldið og reiknaður kostnaður veita tilvísunarupplýsingar fyrir ósamkvæmni og hafa ekki samskipti við aðrar aðgerðir.  
5. Smellt er á uppsetningu Skýrslu.
    * Þessi síða gerir þér kleift að skilgreina gerð athugasemdar fyrir gæðapöntun sem verða notaðir fyrir mismunandi gerðir gæðastjórnunarskýrslurnar.  
6. Lokið síðunni.
7. Lokið síðunni.

## <a name="enable-user-for-nonconformance-processing"></a>Virkja notenda fyrir ósamkvæmnivinnslu.
1. Farið í Kerfisstjórnun > Notendur > Notendur.
    * Til að keyra samþykki á ósamkvæmi verður notandi sem samþykkir eða hafnar ósamkvæmi að hafa „Heiti“ úthlutað á síðunni Notendur. Til að nota athugasemdir skjals verður notandinn einnig að hafa skjalaafgreiðslu virkjaða í valkostum notanda.  
2. Nota flýtiafmörkun til að finna færslur Til dæmis, sía svæðið Heiti með gildinu ‚Ricardo'.
    * Notið síuna til að finna notandinn sem verður að samþykkja eða hafna færslum ósamkvæmni.  
3. Í listanum skal smella á tengilinn í valinni línu.
    * Til að keyra samþykki á ósamkvæmi skal ganga úr skugga um að notandi sem samþykkir eða hafnar ósamkvæmi að hafi „Heiti“ úthlutað á síðunni Notendur.  
4. Smelltu á Notandastillingar
5. Smellið á flipann fríðindi.
6. Velja skal Já í svæðinu virkja skjalastjórnun.
    * Til að nota athugasemdir skjals verður notandinn einnig að hafa skjalaafgreiðslu virkjaða í valkostum notanda.  
7. Lokið síðunni.
8. Lokið síðunni.
9. Lokið síðunni.

## <a name="define-diagnostic-types-for-nonconformance-processing"></a>Skilgreina gerðir greininga fyrir ósamkvæmnivinnslu.
1. Fara í birgðastjórnun > Uppsetningu >gæðastjórnun > gerðir Greininga.
    * Notaðu greiningargerðir  síðuna til að skilgreina flokkun greiningaraðgerða. Leiðrétting auðkennir hvers konar greiningaraðgerð á að framkvæma á samþykktri ósamkvæmni, hver á að framkvæma hana og umbeðna eða áætlaða dagsetningu þegar henni á að vera lokið.  
2. Smellið á „Nýtt“.
3. Í reitinn GREINING skal slá inn gildi.
4. Sláið inn gildi í reitnum „Lýsing“.
5. Lokið síðunni.

## <a name="define-quality-charges-for-nonconformance-processing"></a>Skilgreina gæðastjórnunargjöld fyrir ósamkvæmnivinnslu.
1. Fara í birgðastjórnun > Uppsetning > Gæðaeftirlit > Gæðastjórnunargjöld.
    * Nota síðu Gæðastjórnunargjöld til að skilgreina flokkun á gjöldum sem verður notuð í aðgerðir sem tengjast ósamkvæmni.  
2. Smellið á „Nýtt“.
3. Í reitnum Gjaldakóði skal slá inn gildi.
4. Sláið inn gildi í reitnum „Lýsing“.
5. Lokið síðunni.

## <a name="define-the-operations-for-nonconformance-processing"></a>Skilgreinið starfsemi fyrir ósamkvæmivinnslu
1. Fara í birgðastjórnun > Uppsetning > Gæðastjórnun > Aðgerðir.
    * Notið síðuna aðgerðir til þess að skilgreina flokkun á vinnu sem gætu verið að framkvæmda fyrir samþykkta ósamkvæmni. Þegar aðgerð er tengd við ósamkvæmni, er hægt að skilgreina upplýsingar um tengt efni, vinnustundir og ýmis gjöld sem eru nauðsynleg til þess að framkvæma aðgerðina. Þessar upplýsingar eru grunnurinn fyrir útreikninga á áætluðum kostnaði við að framkvæma aðgerðina.  
2. Smellið á „Nýtt“.
3. Í reitinn Starfsemi skal slá inn gildi.
4. Sláið inn gildi í reitnum „Lýsing“.
5. Lokið síðunni.

## <a name="define-problem-types-for-nonconformance-processing"></a>Skilgreina gerðir vandamála fyrir ósamkvæmnivinnslu.
1. Fara í birgðastjórnun > Uppsetningu > gæðastjórnun > gerðir vandamála.
    * Nota skal vandamálagerðir síðu til að skilgreina flokkun gæðavanda sem kemur fyrir í ýmsum ósamkvæmnigerðum. Gerðir ósamkvæmi innihalda: Viðskiptavinur, Innra, Framleiðsla, Þjónustubeiðni  eða Lánardrottinn og framleiðsla aukaafurða Ein Gerð vandamáls eina hægt að tengja við margar gerðir ósamkvæmni.  
2. Smellið á „Nýtt“.
3. Í reitinn gerð VANDAMÁLs skal slá inn gildi.
4. Sláið inn gildi í reitnum „Lýsing“.
5. Smelltu á Gerðir ósamkvæmnitilvika.
    * Notaðu síðuna gerðir ósamkvæmni til að heimila notkun á vandamálagerð í einni eða fleiri gerðum ósamkvæmni. Til dæmis getur vandamálagerð sem tengist gallakóða átt við um allar gerðir ósamkvæmni, en aftur á móti getur vandamálagerð um kvartanir viðskiptamanna aðeins átt við um viðskiptavininn og gerðir ósamkvæmni í þjónustubeiðnum.  
6. Smellið á „Nýtt“.
7. Í listanum skal merkja valda línu.
8. Veljið valkost í svæðinu tegund ósamkvæmni.
9. Lokið síðunni.
10. Lokið síðunni.

## <a name="define-quarantine-zones-for-nonconformance-processing"></a>Virkja biðgeymslusæði fyrir ósamkvæmnivinnslu.
1. Fara í birgðastjórnun > Uppsetning > Gæðastjórnun > Biðgeymslusvæði.
2. Smellið á „Nýtt“.
3. Í reitinn biðgeymslusvæði skal slá inn gildi.
4. Sláið inn gildi í reitnum „Lýsing“.
5. Lokið síðunni.

