---
title: Setja upp forsendur fyrir ósamkvæmistýringu.
description: Notið þetta efni til að virkja sjórnunarferli ósamkvæmni.
author: perlynne
manager: tfehr
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, InventTestReportSetup, SysUserManagement, SysUserSetup, InventTestDiagnosticType, InventTestMiscCharges, InventTestOperation, InventProblemType, InventProblemTypeSetup, InventQuarantineZone
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8c4de822dcda604241416165a961e4b0bacaeb5b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430590"
---
# <a name="set-up-prerequisites-for-nonconformance-management"></a>Setja upp forsendur fyrir ósamkvæmistýringu.

[!include [banner](../../includes/banner.md)]

Notið þetta efni til að virkja sjórnunarferli ósamkvæmni. Ósamkvæmni lýsir ferli eða vöru sem uppfyllir ekki gæðastaðla, þar sem uppruni og gerð vandamálsins eru í lýsandi upplýsingum. Þessi aðferð notar sýnifyrirtækið USMF. Þetta ferli er yfirleitt framkvæmt af starfsmanni á sviði gæða.


## <a name="enable-quality-management-processes-within-the-company"></a>Virkja ferli gæðastjórnunar innan fyrirtækisins:
1. Í skoðunarrúðunni ferðu í **Kerfiseiningar > Birgðastýring > Uppsetning > Birgðir og færibreytur vöruhúsakerfis**.
2. Veldu flipann **Gæðastjórnun**.
3. Veldu **Já** í reitnum **Nota gæðastjórnun** til að virkja gæðastjórnunarferli fyrir fyrirtækið.
4. Í reitinn **tímagjald** skal færa tölu í gjaldmiðli landsins. Tímagjaldið er notuð til að reikna kostnað fyrir aðgerðir sem tengjast ósamkvæmni. Tímagjaldið og reiknaður kostnaður veita tilvísunarupplýsingar fyrir ósamkvæmni og hafa ekki samskipti við aðrar aðgerðir.  
5. Veldu **Uppsetning skýrslu** til að skilgreina gerðir athugasemda fyrir gæðaskýrslu sem verða notaðar í mismunandi gerðum skýrslum gæðastjórnunar.

## <a name="enable-user-for-nonconformance-processing"></a>Virkja notenda fyrir ósamkvæmnivinnslu.
1. Í skoðunarrúðunni ferðu í **Kerfiseiningar > Kerfisstjórnun > Notendur > Notendur**. 
2. Notið flýtiafmörkun til að finna notandinn sem verður að samþykkja eða hafna færslum ósamkvæmni. Til dæmis, sía í reitnum **Heiti** með gildið `Ricardo`. Til að keyra samþykki á ósamkvæmi verður notandi sem samþykkir eða hafnar ósamkvæmi að hafa „Heiti“ úthlutað á síðunni **Notendur**. Til að nota athugasemdir skjals verður notandinn einnig að hafa skjalaafgreiðslu virkjaða í valkostum notanda.  
3. Merktu röðina með viðkomandi færslu.
4. Veldu **Notendastillingar**.
5. Veldu flipann **Stillingar**.
6. Velja skal **Já** í reitnum **Virkja skjalastjórnun**.

## <a name="define-diagnostic-types-for-nonconformance-processing"></a>Skilgreina gerðir greininga fyrir ósamkvæmnivinnslu.
1. Í skoðunarrúðunni ferðu í **Kerfiseiningar > Birgðastjórnun > Uppsetning > Gæðastjórnun > Greiningagerðir**. Notaðu **greiningargerðir** síðuna til að skilgreina flokkun greiningaraðgerða. Leiðrétting auðkennir hvers konar greiningaraðgerð á að framkvæma á samþykktri ósamkvæmni, hver á að framkvæma hana og umbeðna eða áætlaða dagsetningu þegar henni á að vera lokið.  
2. Veljið **Nýtt**.
3. Í reitinn **Greining** skal slá inn gildi.
4. Í reitinn **Lýsing** skal slá inn gildi.

## <a name="define-quality-charges-for-nonconformance-processing"></a>Skilgreina gæðastjórnunargjöld fyrir ósamkvæmnivinnslu.
1. Í skoðunarrúðunni ferðu í **Kerfiseiningar > Birgðastjórnun > Uppsetning > Gæðastjórnun > Gæðastjórnunargjöld**. Nota síðu **Gæðastjórnunargjöld** til að skilgreina flokkun á gjöldum sem verður notuð í aðgerðir sem tengjast ósamkvæmni.  
2. Veljið **Nýtt**.
3. Í reitnum **Gjaldakóði** skal slá inn gildi.
4. Í reitinn **Lýsing** skal slá inn gildi.

## <a name="define-the-operations-for-nonconformance-processing"></a>Skilgreinið starfsemi fyrir ósamkvæmivinnslu
1. Í skoðunarrúðunni ferðu í **Kerfiseiningar > Birgðastjórnun > Uppsetning > Gæðastjórnun > Aðgerðir**. Notið síðuna **Aðgerðir** til þess að skilgreina flokkun á vinnu sem gætu verið að framkvæmda fyrir samþykkta ósamkvæmni. Þegar aðgerð er tengd við ósamkvæmni, er hægt að skilgreina upplýsingar um tengt efni, vinnustundir og ýmis gjöld sem eru nauðsynleg til þess að framkvæma aðgerðina. Þessar upplýsingar eru grunnurinn fyrir útreikninga á áætluðum kostnaði við að framkvæma aðgerðina.  
2. Veljið **Nýtt**.
3. Í reitinn **Aðgerðir** skal slá inn gildi.
4. Í reitinn **Lýsing** skal slá inn gildi.

## <a name="define-problem-types-for-nonconformance-processing"></a>Skilgreina gerðir vandamála fyrir ósamkvæmnivinnslu.
1. Í skoðunarrúðunni ferðu í **Kerfiseiningar > Birgðastjórnun > Uppsetning > Gæðastjórnun > Vandamálagerðir**. Nota skal **Vandamálagerðir** síðu til að skilgreina flokkun gæðavanda sem kemur fyrir í ýmsum ósamkvæmnigerðum. Gerðir ósamkvæmi innihalda: **Innra**, **Viðskiptavinur**, **Lánardrottinn**, **Þjónustubeiðni**, **Framleiðsla** og **Framleiðsla aukaafurða**. Ein Gerð vandamáls eina hægt að tengja við margar gerðir ósamkvæmni.  
2. Veljið **Nýtt**.
3. Í reitinn **Vandamálagerð** skal slá inn gildi.
4. Í reitinn **Lýsing** skal slá inn gildi.
5. Veldu **Gerðir ósamkvæmnitilvika**. Notaðu síðuna **Gerðir ósamkvæmni** til að heimila notkun á vandamálagerð í einni eða fleiri gerðum ósamkvæmni. Til dæmis getur vandamálagerð sem tengist gallakóða átt við um allar gerðir ósamkvæmni, en aftur á móti getur vandamálagerð um kvartanir viðskiptamanna aðeins átt við um viðskiptavininn og gerðir ósamkvæmni í þjónustubeiðnum.  
6. Veljið **Nýtt**.
7. Í reitnum **Gerð ósamkvæmni** í nýju línunni skal velja valkost.

## <a name="define-quarantine-zones-for-nonconformance-processing"></a>Virkja biðgeymslusæði fyrir ósamkvæmnivinnslu.
1. Í skoðunarrúðunni ferðu í **Kerfiseiningar > Birgðastjórnun > Uppsetning > Gæðastjórnun > Biðgeymslusvæði**.
2. Veljið **Nýtt**.
3. Í reitinn **Biðgeymslusvæði** skal slá inn gildi.
4. Í reitinn **Lýsing** skal slá inn gildi.
5. Lokið síðunni.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]