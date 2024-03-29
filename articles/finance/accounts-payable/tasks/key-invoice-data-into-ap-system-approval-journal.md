---
title: Færa reikningsgögn inn í viðskiptaskuldir með færslubókarsamþykkt
description: Þessi grein útskýrir sýnir hvernig á að nota komubók til að stofna reikninga og nota síðan færslubókarsamþykkt til að uppfæra kostnaðarlykla.
author: abruer
ms.date: 02/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransInvoiceRegister, HcmWorkerLookUp, LedgerJournalTransApprove, LedgerJournalTransApproveFetchVouchers, LedgerTransVoucher
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: afe1471949bbf892f4e28ed3bea830ee491a517f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909215"
---
# <a name="key-invoice-data-into-accounts-payable-using-an-approval-journal"></a>Færa reikningsgögn inn í viðskiptaskuldir með færslubókarsamþykkt

[!include [banner](../../includes/banner.md)]

Þessi grein útskýrir sýnir hvernig á að nota komubók til að stofna reikninga og nota síðan færslubókarsamþykkt til að uppfæra kostnaðarlykla.

## <a name="create-and-post-and-invoice"></a>Stofna og bóka og reikningsfæra
1. Í skoðunarrúðunni ferðu í **Einingar > Viðskiptaskuldir > Reikningar > Komubók**.
2. Veljið **Nýtt**.
3. Veldu heiti komubókarinnar sem þú vilt nota.
4. Veldu **Línur** til að opna skrána og færa inn kostnaðarlínur.
5. Veljið lánardrottin. Til dæmis færirðu inn eða velur `US-104`.
6. Í reitnum **Reikningur** færirðu inn gildi.
7. Í reitinn **Lýsing** skal slá inn gildi.
8. Í reitnum **Kredit** skal slá inn tölu.
9. Í reitnum **Samþykkt af** velurðu samþykktaraðila úr fellivalmyndinni.
10. Veldu **Bóka**.

## <a name="approve-an-invoice"></a>Samþykkja reikning
1. Í skoðunarrúðunni ferðu í **Einingar > Viðskiptaskuldir > Reikningar > Reikningssamþykki**.
2. Veljið **Nýtt**.
3. Veldu heiti færslubókarsamþykkt reiknings sem þú vilt nota.
4. Veldu **Línur** til að birta síðu þar sem er hægt að velja reikninga sem á að samþykkja.
5. Veljið **Finna fylgiskjöl** til að birta alla reikninga sem eru tilbúnar til samþykkis.
6. Merktu við reikninginn sem þú bjóst til og smelltu síðan á **Velja**. Fylgiskjala sem valinn er fyrir ofan eru fluttar yfir á þessum lista eftir að þeim var valið.  
7. Veljið **Í lagi**.
8. Veldu reitinn **Lykilnúmer** til að bæta kostnaðarlykli við reikning.
9. Færið inn lykilnúmer og flipinn við svæðið. Til dæmis er slegið inn `600120`.
10. Veldu **Bóka**.
11. Veldu **Fylgiskjal** til að skoða færslur sem voru bókaðar. Lykill Reiknings sem bíður samþykkist er bakfærður og skipt út fyrir raunverulega kostnaðarlykil.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
