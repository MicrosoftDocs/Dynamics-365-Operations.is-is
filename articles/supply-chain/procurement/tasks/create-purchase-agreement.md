---
title: Stofna innkaupasamning
description: Þessi grein leiðbeinir við stofnun innkaupasamnings.
author: GalynaFedorova
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchAgreement, PurchAgreementCreate, InventItemIdLookupSimple, AgreementConfirmRunForm, PurchAgreementHistory
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 108c3a47132b262ebe2e15f00d26191b75469959
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877567"
---
# <a name="create-a-purchase-agreement"></a>Stofna innkaupasamning

[!include [banner](../../includes/banner.md)]

Þessi grein leiðbeinir við stofnun innkaupasamnings. Þetta verk myndi yfirleitt gert af innkaupastjóra. Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF eða með því að nota eigin gögn. Þú Þarft að hafa sett upp flokkanir innkaupasamnings áður en byrjað er. Þegar Innkaupapöntun er stofnuð og hægt er að nota hana þegar þú stofnar innkaupapöntun, og það afrita skilyrði innkaupasamnings í haus og allar línur í pöntun sem verða fyrir áhrifum af samninginn.


## <a name="create-a-new-purchase-agreement"></a>Stofna nýjan innkaupasamning
1. Farðu í **Skoðunarrúðu > Kerfiseiningar > Innkaup og aðföng > Innkaupasamningar > Innkaupasamningar**.
2. Smellt er á **Nýtt**.
3. Í reitnum **Lánardrottnalykill** velurðu fellivalmyndina og velur röðina með viðeigandi skrá.
4. Í reitnum **Flokkun innkaupasamnings** velurðu fellivalmyndina og velur röðina með viðeigandi skrá.
5. Útvíkka **Almennt** flýtiflipa.
6. Í reitinn **Lokadagur** skal rita dagsetningu.

    - Þessi lokadagur verður sjálfgefið fyrir allar línur ráðstöfunar og ákvarða hve lengi hver tiltekin ráðstöfun er gild.  

7. Í reitinn **Heiti skjals** skal færa inn heiti fyrir innkaupasamninginn.

    - Hafðu reitinn **Sjálfgefin ráðstöfun** stilltan á **Ráðstafað afurðarmagn** (eða breyttu honum, ef hann er ekki stilltur á þetta).  
    - Sjálfgefin ráðstöfunargildið ákvarðar valkostirnir þínir á samningslínur. Ef nýrrar ráðstöfunargerðar er þörf þegar verið er að stofna samningslínur, þarftu að breyta sjálfgefinni ráðstöfun í hausnum. Til eru 4 gerðir ráðstafana: **Ráðstöfun afurðarmagns** - fyrir ákveðið magn afurðar; **Ráðstöfunarvirði afurðar** - fyrir tiltekna gjaldmiðilsupphæð afurðar; **Ráðstöfunarvirði vörutegundar** - fyrir upphæð í tilteknum gjaldmiðli í innkaupaflokki þar sem upphæðin getur verið fyrir vöru í vörulista eða vöru sem er ekki á vörulista; **Ráðstöfunarvirði** - fyrir tiltekna gjaldmiðilsupphæð sem getur verið uppfyllt af hvaða vöru eða af hvaða innkaupategund sem er.  

8. Veljið **Í lagi**.

## <a name="add-a-commitment"></a>Bæta við skuldbindingu
1. Veldu **Bæta við línu**.
2. Í reitnum **Vörunúmer** velurðu skrána sem óskað er eftir af fellivalmyndinni.
3. Í reitnum **Magn** slærðu inn tölu. Þetta er heildarmagn sem þú hefur samþykkt að kaupa frá lánardrottni.  
4. Í reitnum **Einingarverð** skal slá inn tölu.
5. Útvíkkaðu hlutann **upplýsingar Línu**.
6. Stilltu valkostinn **Hámarki er framfylgt** á **Já**. Valkosturinn **Hámarki er framfylgt** takmarkar notkun á ráðstöfun. Aðeins er hægt að kaupa upp að því magni sem er tilgreint er í reitnum **Magn** fyrir línuna.  

## <a name="add-header-conditions"></a>Bæta við fyrirsagnaskilyrði
1. Í aðgerðasvæðinu velurðu **Valkostir**.
2. Veldu **Breyta skjámynd**.
3. Veldu **Hausyfirlit**.
4. Útvíkkaðu kaflann **Skilmálar**.
5. Í reitnum **Greiðsluháttur** velurðu skrána sem óskað er eftir af fellilistanum. Greiðsluskilmálar úr lykli lánardrottins eru sýnd hér sjálfgefið.  
6. Í reitnum **Afhendingarmáti** velurðu skrána sem óskað er eftir af fellilistanum.
7. Í reitnum **Afhendingarskilmálar** skal smella á fellilistahnappinn til að opna leitina.

## <a name="confirm-and-activate-the-agreement"></a>Vista og virkja samning
1. Í aðgerðasvæðinu smellirðu á **Innkaupasamningur**.
2. Veldu **Staðfesting**. Stilltu valkostinn **Merkja samning sem gildan** á **Já**.  
3. Veljið **Í lagi**.
4. Í aðgerðasvæðinu smellirðu á **Innkaupasamningur**.
5. Veldu **Staðfestingar innkaupasamnings**. Valkosturinn **Forskoðun/Prenta** gerir kleift að búa til skjal fyrir innkaupasamning sem síðan er hægt að prenta eða senda til lánardrottins. Ef þú uppfæra samning síðar og staðfesta hann aftur, verða báðar útgáfur sýnd hér.  
6. Lokið síðunni.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]