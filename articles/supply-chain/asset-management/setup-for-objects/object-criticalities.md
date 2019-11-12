---
title: Mikilvægisgerðir eigna
description: Umræðuefnið útskýrir gerðir eignamikilvægis í eignastýringu.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f96fcc7ebb8928c6d6b17b30465ad1625d9b5be4
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571071"
---
# <a name="asset-criticality-types"></a>Mikilvægisgerðir eigna

[!include [banner](../../includes/banner.md)]

 

Umræðuefnið útskýrir gerðir eignamikilvægis í eignastýringu. Mikilvægi eigna er tengd eignum og færð yfir í verkbeiðnum. Það er ekki hægt að breyta því í verkbeiðni. Skilvirkni eigna er notuð til að reikna út gagnrýni á verkþörf meðan á tímasetningu verkbeiðni stendur. Með öðrum orðum, það er notað til að reikna út að hve miklu leyti viðhaldsstörf á eign hafa áhrif á framleiðsluáætlun og framleiðni fyrirtækisins. Nánari upplýsingar um uppsetninguna sem er tengd útreikningi á matseinkunnum fyrir tímasetningar verkbeiðni, sjá [Færibreytur eignastýringar](../setup-for-objects/enterprise-asset-management-parameters.md).

Til að setja upp gagnrýni skaparðu fyrst þær tegundir gagnrýni sem ætti að nota í uppsetningu eigna. Þú setur síðan upp eignamikilvægi.

## <a name="set-up-criticality-types"></a>Setja upp gerðir mikilvægis

1. Veldu **Eignastýring** \> **Uppsetning** \> **Eignir** \> **Gerðir mikilvægis**.
2. Veljið **Ný** til að stofna nýja skrá.
3. Í retinum **Gagnrýni** slærðu inn tölu sem gefur til kynna mikilvægi.
4. Á svæðinu **Heiti** skal færa inn einkvæmt heiti fyrir gerð mikilvægis.
5. Í reitnum **Stuðull** skal slá inn stuðul. Þessi þáttur er notaður við útreikning á tímasetningu verkbeiðnaáætlana til að ákvarða mikilvægisskrá sem ætti að nota. (Færslan sem hefur hæsta þáttinn er alltaf notuð.) Þessi stilling skiptir máli ef, eins og sýnt er á eftirfarandi mynd, eru gagnrýni línur búnar til sem hafa sama gagnrýni gildi.

    ![Síðan Gerðir mikilvægis](media/23-setup-for-objects.png)

## <a name="set-up-asset-criticalities"></a>Setja upp mikilvægi eigna

1. Veldu **Eignastýring** \> **Uppsetning** \> **Eignamikilvægi**.
2. Veljið **Ný** til að stofna nýja skrá.
3. Taktu viðeigandi val í upplýsingagjöfina eftir því hvaða smáatriða er krafist varðandi gagnrýni í reitunum **Virk staðsetning**, **Gerð eigna**, **Framleiðandi**, **Fyrirmynd**, **Eignir**, **Starfsflokkur**, **Atvinnugerð**, **Atvinnugerðafbrigði**, og **Starfsskylda**.

    > [!NOTE]
    > Þegar eignagagnrýni er valið fer Eignastjórn í gegnum allar skrár yfir mikilvægi eigna til að athuga hvort mögulegt sé samsvörun. Það athugar alltaf sértækustu samsetninguna fyrst. Með öðrum orðum, Eignastjórnun kannar fyrst **Starfsskylda**. Ef engin samsvörun finnst, þá athugar hún **Atvinnugerðafbrigði**. Ef engin samsvörun finnst, þá athugar hún **Atvinnugerðafbrigði** og svo framvegis. Eins og þú sérð á skipulagi síðunnar þýðir þessi hegðun að til að finna sértækustu samsetninguna, þá velur eignastjórnun hverja skrá frá hægri til vinstri fyrir leik. Ef engin samsvörun er notuð er „sjálfgefna“ skráin sem hefur engin val verið notuð.

4. Í **Gagnrýni** veldu eitt af mikilvægisgildunum sem þú bjóst til í fyrri aðferð.

### <a name="notes-about-criticality-setup"></a>Athugasemdir um skipulag gagnrýni

- Ef þú breytir mikilvægi eigna í þessari uppsetningu eftir að þú hefur þegar notað það í vinnupöntun, er gagnrýninn á vinnuskipulagið ekki uppfærður til samræmis.
- Gagnrýnin á verkbeiðni er endurútreiknuð í hvert skipti sem vinnupöntunarlínu er bætt við eða henni eytt úr verkbeiðninni.
- Ef verkbeiðni inniheldur nokkur vinnupöntunarstörf er mesta gagnrýni samkvæmt **Þáttur** reit á síðunni **Gerðir gagnrýni**, er alltaf notuð í nni.
- Almennt getur gagnrýni eigna breyst á tímabili. Gagnrýni getur orðið fyrir áhrifum af kaup á nýjum búnaði, endurbótum og svo framvegis. Íhugaðu að endurmeta eignatengsl þitt með reglulegu millibili (til dæmis einu sinni á ári eða annað hvert ár) til að ganga úr skugga um að skilgreiningar á mikilvægi þínu samsvari núverandi framleiðsluuppsetningunni.
