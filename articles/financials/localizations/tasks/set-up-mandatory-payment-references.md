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
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Iceland
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dd3d0b5f6babd221c2427efa07a771be2dccdc4e
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537990"
---
# <a name="set-up-mandatory-payment-references"></a>Setja upp skyldubundnar greiðslutilvísanir

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

