---
title: Setja upp skyldubundnar greiðslutilvísanir
description: Notið þetta ferli til að setja upp skyldubundna greiðslutilvísun fyrir sérstakan fjárhagslykil og bóka greiðslu.
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MainAccount, LedgerJournalTable, LedgerJournalTransDaily
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Iceland
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 94efa65de6c79c35a0b3d07ec8d8d122587fa680
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4408065"
---
# <a name="set-up-mandatory-payment-references"></a>Setja upp skyldubundnar greiðslutilvísanir

[!include [banner](../../includes/banner.md)]

Notið þetta ferli til að setja upp skyldubundna greiðslutilvísun fyrir sérstakan fjárhagslykil og bóka greiðslu. Þegar fjárhagslykill er valin í færslubók verður að tilgreina tilvísun greiðslu fyrir færslubókarlínu.

Þessi skráning notar sýnigögn DEMF fyrirtækis Þessi Virkni er eingöngu tiltæk fyrir lögaðila með aðalaðsetur á Íslandi.

Þessi virkni er gjarnan notað af bókhaldarar , aðalbókarar, bókurum.


## <a name="set-up-the-main-account"></a>Setja upp aðallykill
1. Fara í Fjárhagur > Bókhaldslyklar > Lyklar > Aðallyklar.
2. Nota flýtiafmörkun til að finna færslur Til dæmis, sía svæðið aðallykill með gildið '170150'.
3. Í listanum skal smella á tengilinn í valinni línu.
4. Smella á Breyta.
5. Velja eða hreinsa sem gátreit Krefjast tilvísun greiðslu.
6. Smellið á „Vista“.

## <a name="create-a-payment-with-a-payment-reference"></a>Greiðsla er stofnuð með tilvísun greiðslu
1. Fara í fjárhag > Færslubókarfærslur > Almennar færslubækur.
2. Smellið á „Nýtt“.
3. Í listanum skal merkja valda línu.
4. Í reitnum Heiti skal smella á fellilistahnappinn til að opna leitina.
5. Í listanum skal smella á tengilinn í valinni línu.
6. Smellið á Línur.
7. Í listanum skal merkja valda línu.
8. Í reitnum Lykill skal tilgreina gildi sem óskað er eftir.
9. Í reitnum Debet skal slá inn tölu.
10. Í reitnum Mótlykill skal tilgreina gildi sem óskað er eftir.
11. Smellið á flipann Greiðslu.
12. Færa inn gildi í greiðslutilvísunarsvæðið.
13. Smellið á „Vista“.
14. Smellið á „Bóka“.

