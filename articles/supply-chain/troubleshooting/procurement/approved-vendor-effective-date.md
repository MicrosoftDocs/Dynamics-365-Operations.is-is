---
title: Ekki er hægt að breyta upphafsdegi fyrir samþykktan lánardrottin
description: Listi yfir samþykkta lánardrottna eftir afurðareiningu leyfir ekki að gildisdagsetningunni sé breytt
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: cb6dbd134d63daa163261cabdbd7eceb978877ae
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476616"
---
# <a name="cant-change-the-effective-date-for-an-approved-vendor"></a>Ekki er hægt að breyta upphafsdegi fyrir samþykktan lánardrottin


## <a name="symptoms"></a>Einkenni

Afurð er með samþykktan lánardrottin sem er með t.d. gildisdagsetningu 11. janúar 2018 (*11/01/2018*), og lokadaginn *Aldrei*. Ef reynt er að breyta gildisdagsetningunni í 10. janúar 2018 (*10/01/2018*) eða 12. janúar 2018 (*12/01/2018*) kemur upp eftirfarandi villu:

> Ekki tókst að stofna færslu í lista yfir samþykkta birgja (PdsApproveVendorList). Gildið 'Lokadagsetning' þarf að vera stærra en eða jafnt og gildið fyrir ‚Gildisdagsetning‘.

## <a name="resolution"></a>Lausn

Aðeins er hægt að framlengja tímabilið þar sem lánardrottinn hefur verið samþykktur. Eftirfarandi reglur gilda:

- Til að breyta gildisdagsetningu þannig að hún sé á undan fyrirliggjandi færslum (tímabilum) fyrir lánardrottin vörunnar, verður lokadagur nýja tímabilsins að vera á undan öllum lokadagsetningum í fyrirliggjandi færslum.
- Til að breyta lokadagsetningunni þannig að hún verði síðar en á fyrirliggjandi tímabilum verður gildisdagsetningin að vera á eftir síðustu lokadagsetningunni í fyrirliggjandi færslu.
- Til að draga úr heildartímabilinu sem lánardrottinn hefur verið samþykktur fyrir, þarf að eyða eða breyta fyrirliggjandi færslum. Að öðrum kosti er hægt að nota rofann **stytta** meðan á innflutningi stendur. Þessi rofi eyðir öllum fyrirliggjandi færslum í töflunni fyrir samþykkta lánardrottna eftir vöru.

Fyrir dæmið sem lýst er í útgáfulýsingunni þar sem færsla er með gildisdagsetningu *11/01/2018* og lokadag *Aldrei*, er hægt að flytja inn nýja færslu sem er með gildisdagsetningu *10/01/2018* og lokadagsetningu *Aldrei*. Hins vegar er ekki hægt að stytta tímabilið þannig að gildisdagsetningin uppfærist í *12/01/2018* í gegnum gagnastjórnun. Þú verður að gera þessa breytingu í gegnum notandaviðmótið.
