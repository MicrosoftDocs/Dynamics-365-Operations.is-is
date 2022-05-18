---
title: Fyrirframgreiðslur viðskiptavinar
description: Í þessu efnisatriði er því lýst hvernig á að setja upp og vinna úr fyrirframgreiðslum viðskiptavina (einnig þekkt sem innborganir viðskiptavina).
author: twheeloc
ms.date: 04/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, LedgerJournalTransCustPaym, CustParameters
audience: Application User
ms.reviewer: twheeloc
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: ''
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eb0f2290a38d89d90ac0d30a59e21fb3e9a6d894
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/04/2022
ms.locfileid: "8691892"
---
# <a name="customer-prepayments"></a>Fyrirframgreiðslur viðskiptavinar

[!include [banner](../includes/banner.md)]

Fyrirframgreiðslur viðskiptavina eru notaðar þegar greiðsla frá viðskiptavini er móttekin en enginn reikningur er til staðar sem hægt er að jafna greiðsluna við. Þessar greiðslutegundir eru einnig kallaðar innborganir viðskiptavina.

Ferlið við að setja upp og vinna með fyrirframgreiðslur viðskiptavina samanstendur af eftirfarandi grunnskrefum.

1. Búðu til bókunarreglu viðskiptavinar fyrir fyrirframgreiðslur.
2. Stillið færibreytuna **Bókunarregla með fylgiskjali fyrirframgreiðslubókar**.
3. Stofnið fyrirframgreiðslubók og veljið gátreitinn **Fylgiskjal fyrirframgreiðslubókar** í hverri línu.
4. Bóka greiðslubók viðskiptavinar.
5. Þegar búið er að búa til reikning skal jafna fyrirframgreiðsluna við hann með því að nota síðuna **Jafna opnar færslur**.

## <a name="create-a-customer-posting-profile-for-prepayments"></a>Búðu til bókunarreglu viðskiptavinar fyrir fyrirframgreiðslur

Þegar fyrirframgreiðslur eða innborganir frá viðskiptavinum eru samþykktar áður en vörur eða þjónusta er afhent, eða áður en reikningur verður til í kerfinu, vill notandinn yfirleitt skrá reiðuféð sem skuld í stað eignar í bókhaldslyklinum. Hins vegar geta kröfur vegna skráningar á þessum upphæðum í fjárhagnum verið mismunandi eftir landi eða svæði. Því skal ráðfæra sig við bókarana varðandi staðbundnar reglugerðir sem eiga við.

Almennt er ferlið við að búa til bókunarreglu sem hægt er að nota fyrir fyrirframgreiðslur það sama og ferlið við að búa til aðrar bókunarreglur. Helsti munurinn liggur í aðallyklinum sem er valinn í reitnum **Safnlykill**. Frekari upplýsingar eru í [Bókunarreglur viðskiptavina](customer-posting-profiles.md).

## <a name="define-parameters-for-customer-prepayments"></a>Skilgreina færibreytur fyrir fyrirframgreiðslur viðskiptavina

Hafa skal í huga tvær færibreytur aðallykils viðskiptakrafa þegar kerfið er stillt fyrir fyrirframgreiðslur viðskiptavina. Fylgdu þessum skrefum til að grunnstilla færibreyturnar.

1. Opnið **Viðskiptakröfur \> Setja upp \> Færibreytur viðskiptakrafna**.
2. Valfrjálst: Í flipanum **Fjárhagur og virðisaukaskattur**, í flýtiflipanum **Greiðsla**, skal stilla valkostinn **VSK í fylgiskjali fyrirframgreiðslubókar** á **Já**.
3. Í reitnum **Bókunarregla með fylgiskjali fyrirframgreiðslubókar** skal velja bókunarreglu viðskiptavinar sem á að nota þegar fyrirframgreiðslur viðskiptavinar eru bókaðar.
4. Lokið síðunni.

## <a name="create-customer-prepayment-vouchers"></a>Stofna fylgiskjal fyrirframgreiðslu viðskiptavinar

Þegar greiðslubók viðskiptavinar er stofnuð þarf fyrir hverja fyrirframgreiðslu að stilla valkostinn **Fylgiskjal fyrirframgreiðslubókar** á **Já** á síðunni **Greiðslubók viðskiptavinar**. Fylgdu þessum skrefum til að búa til fyrirframgreiðslu viðskiptavinar.

1. Farið í **Viðskiptakröfur \> Greiðslur \> Greiðslubók viðskiptavinar**.
2. Veljið **Ný** til að stofna færslubók.
3. Í reitnum **Heiti** skal velja færslubókina sem á að nota.

    > [!IMPORTANT]
    > Ef valkosturinn **VSK í fylgiskjali fyrirframgreiðslubókar** er stilltur á **Já** í fyrra ferlinu, þarf að velja heiti færslubókar þar sem færibreytan **Upphæð með virðisaukaskatti** er valin. 

4. Valfrjálst: Í reitinn **Lýsing** skal færa inn nákvæma lýsingu.
5. Veldu **Línur**.
6. Ef auð lína er ekki til skal velja **Ný** til að stofna línu.
7. Í reitinn **Dagsetning** skal færa inn dagsetninguna þegar bóka á fyrirframgreiðsluna.
8. Í reitinn **Lykill** skal velja viðskiptavin fyrirframgreiðslunnar.
9. Valfrjálst: Í reitinn **Lýsing** skal færa inn nákvæma lýsingu á færslunni.
10. Í reitinn **Kredit** skal færa inn upphæð fyrirframgreiðslunnar.
11. Í reitnum **Mótlykill** skal velja lykilinn til að jafna við greiðsluna. Veljið til að mynda bankann eða aðallykilinn til að bóka greiðsluna á.
12. Í reitnum **Greiðslumáti** skal velja greiðslumáta viðskiptavinar.
13. Í flipanum **Greiðsla** skal stilla valkostinn **Fylgiskjal fyrirframgreiðslubókar** á **Já**.
14. Endurtakið skref 7 til 13 fyrir hverja fyrirframgreiðslu til viðbótar sem þarf að bóka.
15. Veljið **Bóka** til að ganga frá færslubókinni.

## <a name="settle-prepayments-with-invoices"></a>Jafna fyrirframgreiðslur með reikningum

Hægt er að nota vinnusvæðið **Greiðslur viðskiptavinar** til að finna og jafna greiðslur sem hafa ekki verið jafnaðar að fullu á auðveldan hátt.

1. Í yfirlitinu **Heim** skal velja reitinn **Greiðslur viðskiptavinar**.
2. Í hlutanum **Færslur viðskiptavinar**, í flipanum **Ójafnaðar greiðslur**, skal leita að og velja greiðslu til að jafna.
3. Smellt er á **Jafna færslur**.
4. Veljið gátreitinn **Merkja** fyrir reikninginn og greiðsluna sem verða jöfnuð.
5. Veldu **Bóka**.

Frekari upplýsingar um hvernig á að jafna opnar færslur er að finna í [Yfirlit jöfnunar](/dynamics365/finance/cash-bank-management/settlement-overview).
