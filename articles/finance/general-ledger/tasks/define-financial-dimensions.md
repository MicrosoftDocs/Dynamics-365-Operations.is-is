---
title: Skilgreina fjárhagsvíddir
description: Þessi leiðarvísir fyrir verk sýnir hvernig bætt er við einingu afrita fjárhagsvídd og sérstillta fjárhagsvídd.
author: aprilolson
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionDetails,  DimensionAttributeTableExtensionActivate, DimensionValueDetails
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6fbe739eec0cfa1e7b0276872640bd4f82be3ef7
ms.sourcegitcommit: c69926b4285cb2ec2d9ce1ad72d1cb852024dd5e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138337"
---
# <a name="define-financial-dimensions"></a>Skilgreina fjárhagsvíddir

[!include [banner](../../includes/banner.md)]

Þessi leiðarvísir fyrir verk sýnir hvernig bætt er við einingu afrita fjárhagsvídd og sérstillta fjárhagsvídd.  Leiðbeiningarnar nota USMF sýnigögn fyrirtækið.


## <a name="create-an-entity-backed-financial-dimension"></a>Stofna fjárhagsvídd afritaðra eininga.
1. Farðu í **Skoðunarrúðu > Kerfiseiningar > Fjárhag > Bókhaldslykill > Víddir > Fjárhagsvíddir**.
2. Smellt er á **Nýtt**.
3. Í reitnum **Notandagildi** skal velja kerfisskilgreinda einingu til að byggja fjárhagsvíddina á. 
4. Í reitinn **Heiti víddar** skal slá inn gildi til að lýsa fjárhagsvíddinni. Heitið getur verið annað en kerfisskilgreind eining en má ekki innihalda bil eða sérstafi.
5. Smellið á **Virkja**. Virkjun fjárhagsvíddar uppfærir töflu með fjárhagsvíddarheitinu og fjarlægir eyddum víddum. Hægt er að færa inn víddargildi áður en fjárhagsvídd er virkjuð en fjárhagsvídd er ekki hægt að nota fyrr en hún er virkjuð.  
6. Smelltu á **Loka** í virkjunarskilaboðunum.
7. Smellið á **Virkja**. Hægt er að tímasetja virkjun víddar þannig að hún keyri í runu á tilteknum degi og tíma.  
8. Í **Aðgerðasvæði** er smellt á **Víddargildi**. Sum víddargildi eru bundin fyrirtæki. Hægt er að staðfesta hvort þær eru bundnar fyrirtæki með því hvort heiti fyrirtækisins er sýnt í lista yfir víddargildi.  

## <a name="create-a-custom-financial-dimension"></a>Stofna sérstillta fjárhagsvídd
1. Lokið síðunni.
2. Smellt er á **Nýtt**.
3. Í reitnum **Nota virði frá** skaltu velja **Sérsniðin vídd**.
4. Í reitinn **Heiti víddar** skal slá inn gildi til að lýsa fjárhagsvíddinni.
    - Heitið getur ekki innihaldið bil eða sérstafi.  
    - Einnig er hægt að tilgreina lykilsíu til að takmarka magn og gerð upplýsinga sem hægt er að færa inn víddargildi fyrir.   
    - Hægt er að færa inn stafi sem eru þeir sömu og fyrir hvert víddargildi eins og stafi eða bandstrik. Einnig er hægt að færa inn tákn (#) og merki (&) sem frátakara fyrir stafi og tölustafi sem breytast í hvert skipti sem víddargildi eru stofnuð. Nota skal númeratákn (#) sem frátakara fyrir tölustafi og merki (&) sem frátakara fyrir stafi.  Dæmi: Til að takmarka víddargildi við stafina CC og þrjár tölur færirðu inn CC-### sem sniðsíu.  
5. Smellið á **Virkja**. Virkjun fjárhagsvíddar uppfærir töflu með fjárhagsvíddarheitinu og fjarlægir eyddum víddum. Hægt er að færa inn víddargildi áður en fjárhagsvídd er virkjuð en fjárhagsvídd er ekki hægt að nota fyrr en hún er virkjuð.     
6. Smellið á **Virkja**. Hægt er að tímasetja virkjun víddar þannig að hún keyri í runu á tilteknum degi og tíma.      
7. Í **Aðgerðasvæði** er smellt á **Víddargildi**.
8. Smellt er á **Nýtt**.
9. Í reitnum **Víddargildi** skal slá inn heiti til að lýsa því fjárhagsvíddargildi.
10. Í reitnum **Lýsing** skal færa inn lýsingu sem lýsir fjárhagsvíddargildi.

