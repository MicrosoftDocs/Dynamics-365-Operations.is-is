---
title: Stofna innkaupavörulista
description: Þetta efnisatriði útskýrir hvernig á að stofna innkaupavörulista.
author: mkirknel
manager: AnnBe
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProcCategoryHierarchyManagement, CatProcureCatalogListPage, CatProcureCatalogCreate, CatProcureCatalogEdit, SysPolicyListPage, SysPolicy, CatCatalogPolicyRule, PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqAddItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 55bc7479ca9ba3ca86e23b5bee106ef169c40077
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836390"
---
# <a name="create-a-procurement-catalog"></a>Stofna innkaupavörulista

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þetta efnisatriði útskýrir hvernig á að stofna innkaupavörulista. Þetta verk myndi venjulega framkvæmt af fagmanni á sviði innkaupa. Einnig muntu læra hvernig starfsmenn geta notað vörulista þegar þeir stofna beiðni. Áður en hægt er að stofna vörulista verður að vera tegundastigveldi innkaupa í kerfinu. Stigveldið er erft af nýjum vörulista, ásamt öllum afurðum sem eru í stigveldinu. Hægt er að nota þessari handbók í sýnigögnum USMF-fyrirtækisins þar sem tegundastigveldi innkaupa er tiltækt, sem og dæmi sem notað er í skrefum ferlisins.


## <a name="ensure-that-a-procurement-category-hierarchy-exists"></a>Tryggið að til tegundastigveldi innkaupa sé til staðar.
1. Farðu í **skoðunarrúðu > Kerfiseiningar > Innkaup og aðföng > Innkaupaflokkar**. Tegundastigveldi innkaupa er tiltækt í sýnigögnum USMF-fyrirtækisins og afurðir hefur verið bætt við flokkinn **Skrifstofuvélar/Tölvur**. Ef verið er að keyra þetta ferli sem leiðarvísi fyrir verk þarf að aflæsa leiðarvísi fyrir verk til að fletta í gegnum tegundina. Ef stigveldi var ekki tiltækt, yrði það stofnað með því að smella á **Nýtt**. Einungis er hægt að gera þetta einu sinni.  
2. Lokið síðunni.

## <a name="create-a-catalog"></a>Stofna vörulista
1. Farðu í **skoðunarrúðu > Kerfiseiningar > Innkaup og aðföng > Vörulistar > Innkaupavörulistar**.
2. Smelltu á **Nýr innkaupavörulisti** til að opna fellilistann.
3. Í reitinn **Heiti** skal slá inn gildi.
4. Veljið **Í lagi**.
5. Í trénu útvíkkarðu **CORP PROCUREMENT CATEGORIES**.
6. Í trénu skal útvíkka **OFFICE MACHINES**.
7. Í trénu skal velja **Tölvur**.

  - Afurðir fyrir innkaupategundina birtast á listanum. Eigi að bæta vöru við flokk þarf að gera þetta á síðunni **Tegundastigveldi innkaupa** eða á síðunni **Vöruupplýsingar**.  
  - **Sjálfgefin** uppfærslugerð ákvarðar hvort nýjar afurðir sem hefur verið bætt við tegundastigveldi innkaupa eru sýnileg strax í vörulistanum. Ef gerð uppfærslu er stillt á **Gagnvirkt**, eru breytingar sýnilegar strax. Ef gerð uppfærslu er **Föst**, eru nýjar afurðir einungis sýnilegt fyrir fólk á vörulista eftir að vörulista hefur verið birt aftur. Aðgerðin **Birta** er tiltæk í Aðgerðarúðunni efst á síðunni. Ef vörur eru fjarlægðar úr tegundastigveldi innkaupa, sést breytingu strax, án tillits til gildisins í reitnum **sjálfgefin** uppfærslugerð.  

8. Á aðgerðarrúðunni velurðu **Yfirlit flokks** og tryggir að **Virkja** sé valið.
9. Veldu **Virkja vörulista**.
10. Lokið síðunni.

## <a name="make-the-catalog-visible"></a>Gera vörulista sýnilegan
1. Farðu í **skoðunarrúðu > Kerfiseiningar > Innkaup og aðföng > Uppsetning > Reglur > Innkaupareglur**.
2. Veldu **Innkaupareglu USMF** Velja þarf innkaupastefna fyrir lögaðilann sem starfsmaðurinn sem er tengdur við þína forstillingu má panta vörur í. Í sýnigögnum USMF er kerfisstjóranotandinn tengdur við starfskraft sem kallast **Julia Funderburk** og hún pantar vörur í USMF að sjálfgefnu.  
3. Velja vörulista sem nýverið var stofnuð
4. Veljið **Í lagi**.

## <a name="use-the-catalog"></a>Nota vörulista
1. Farðu í **skoðunarrúðu > Kerfiseiningar > Innkaup og aðföng > Innkaupabeiðnir > Allar innkaupabeiðnir**.
2. Veljið **Nýtt**.
3. Í reitinn **Heiti** skal slá inn gildi.
4. Veljið **Í lagi**.
5. Veldu **Bæta afurðum við**.
6. Í listanum skal finna og velja þá skráningu sem óskað er eftir. Hægt er að nota tegundastigveldi vinstra megin eða sía efst á listanum til að sía vörurnar.  
7. Veldu **Bæta við línum**.
8. Veljið **Í lagi**.

