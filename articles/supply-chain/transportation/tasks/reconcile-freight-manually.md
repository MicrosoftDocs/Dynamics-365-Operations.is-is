---
title: Afstemma farmbréf handvirkt
description: Þessi verklýsing sýnir hvernig afstemmingu farms handvirkt.
author: Weijiesa
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, TMSFreightBillDetail, TMSInvoiceTable, TMSFreightBillInvoiceReconcile, TMSInvoiceJournal, LedgerJournalTable, LedgerJournalTransDaily, TMSFBDetailReconcile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: weijiesa
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8afec41cdb10185077d39a665d0153df1c9bdb9f
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672739"
---
# <a name="reconcile-freight-manually"></a>Afstemma farm handvirkt

[!include [banner](../../includes/banner.md)]]

Þessi verklýsing sýnir hvernig afstemmingu farms handvirkt. Þetta er yfirleitt gert af samræmingaraðila flutninga. Hægt er að nota þetta ferli í sýnigögn fyrirtækisins USMF.


## <a name="select-a-load-to-reconcile"></a>Veljið hleðslu til að afstemma
1. Fara í flutningsstjórnun > Áætlanagerð > Vinnusvæði hleðsluáætlunar.
2. Hreinsa gátreitinn Fela sent og móttekið. 
3. Velja farms sem hefur farmkenni 00006 á listanum.

## <a name="create-a-carrier-invoice"></a>Stofna reikning flutningsaðila
Ef afstemmingu farms handvirkt og ekki sjálfkrafa mótteknir reikningar flutningsaðila, er hægt að stofna reikning á grundvelli farmbréfs.  
1. Smelltu á Tengdar upplýsingar.
2. Skoða upplýsingar farmbréfs.
3. Smelltu á Stofna farmbréfsreikning.
4. Í reitinn Reikningur skal færa inn gildi.
5. Smellið á „Í lagi“.

## <a name="reconcile-the-invoice"></a>Afstemma reikning
Til að stemma af farmflytjanda reiknings og til farmbréfs, er þetta gert línu fyrir lína.  
1. Smelltu á Jafna farmbréf og reikninga.
2. Útvíkka hlutann Reikningsupplýsingar.
3. Útvíkkið hlutann Ójafnaðar upplýsingar farmbréfs.
4. Í listanum skal merkja valda línu.
5. Smellt er á Jöfnun.
6. Útvíkkið hlutann upplýsingar um jafnað farmbréf

## <a name="submit-the-invoice-for-approval"></a>Senda reikninginn til samþykkis
1. Smellið á Senda til samþykktar
2. Lokið síðunni.
3. Hreinsa gátreitinn Fela samþykkt 
4. Smellið á Reikningabók lánardrottna
5. Smellið til að elta tengilinn í reitnum tilvísunarnúmer færslubókar.
6. Smellið á „Línur“.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]