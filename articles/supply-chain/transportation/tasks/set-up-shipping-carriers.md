---
title: Setja upp farmflytjendur
description: Þessi grein sýnir hvernig á að setja upp flutningsaðila og skilgreina upplýsingar eins og þjónustu, sendingarmáta, flutningsútboð, flutningstakmarkanir og sendingarhlutfall.
author: Weijiesa
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSShippingCarrierCustomerAccount,TMSCarrier
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: weijiesa
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 48586a0ddaa7cd95a81380dadffef8f276076dd2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858973"
---
# <a name="set-up-shipping-carriers"></a>Setja upp farmflytjendur

[!include [banner](../../includes/banner.md)]

Þessi grein sýnir hvernig á að setja upp flutningsaðila og skilgreina upplýsingar eins og þjónustu, sendingarmáta, flutningsútboð, flutningstakmarkanir og sendingarhlutfall. Samræmingaraðili við flutninga getur þá úthluta farmflytjanda á hleðslu á inn eða útleið.

## <a name="create-a-new-shipping-carrier"></a>Stofna nýtt farmflytjandi

1. Farðu í **Skoðunarrúðu > Kerfiseiningar > Uppsetning > Flutningsaðilar > Farmflytjendur**.
2. Veljið **Nýtt** á aðgerðasvæðinu.
3. Í reitnum **Farmflytjandi** skal færa inn gildi.
4. Í reitinn **Heiti** skal slá inn gildi.
5. Í reitnum **Stilling** velurðu valkost úr fellivalmyndinni.

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a>Fyllið inn almennar upplýsingar um farmflytjanda

1. Víxla útvíkkun á liðnum **Yfirlit**.
2. Kanna eða afhaka gátreitinn **Virkja farmflytjanda**.
3. Í reitnum **Lánardrottnalykill** velurðu valkost úr fellivalmyndinni. Veljið lánardrottnalykil sem á að úthluta farmflytjanda.  
4. Í reitnum **Gerð flutningstilboðs** velurðu valkost. Veljið **Handvirkt** til að nota Tilboðssíðu flutninga eða velja **EDI** til að uppfæra tilboð með því að nota Rafræna gagnamillifærslu (EDI).  
5. Merkja eða afmerkja gátreitinn **Virkja mat á farmflytjanda**.

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a>Stofna nauðsynlega þjónustuna fyrir farmflytjanda

1. Víxlaðu útvíkkun á liðnum **Þjónusta**.
2. Veljið **Nýtt**.
3. Í reitinn **Flutningsþjónusta** skal slá inn gildi.
4. Í reitinn **Heiti** skal slá inn gildi.
5. Í **Hlaða auðkenni sniðmáts** reit, veldu hleðslusniðmát til að tengja við þjónustuna. Hleðslusniðmátið skilgreinir hámarksmælingar fyrir þyngd og rúmmál heilrar farms. Til dæmis gæti hleðslusniðmátsins staðið fyrir stærð vörubíls eða gáms. Auðkenni hleðslusniðmáts eru einnig tilgreind í hleðslusniðmátum og þegar þú notar [hlaða bygging vinnubekkur](load-building-workbench.md), sem hjálpar þér að beita álagsuppbyggingaraðferðum til að búa til álag. Fyrir vikið mun kerfið geta samræmt hverja nýja farm við viðeigandi flutningsþjónustu með því að bera saman tilgreind hleðslusniðmátsauðkenni.
6. Í reitnum **Flutningsaðferð** velurðu valkost úr fellivalmyndinni.

## <a name="set-up-the-address-for-the-carrier-optional"></a>Setja upp aðsetur fyrir flutningsaðila (valfrjálst)

1. Víxlaðu útvíkkun á liðnum **Heimilisföng**.
2. Veljið **Nýtt**.
3. Í reitinn **Nafn eða lýsing** skal færa inn gildi.
4. Í reitnum **Land/landsvæði** velurðu valkost úr fellivalmyndinni.
5. Í reitnum **Póstnúmer** velurðu valkost úr fellivalmyndinni.
6. Í reitinn **Gata** skal slá inn gildi.
7. Veljið **Í lagi**.

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a>Setja upp taxtaforstilling fyrir farmflytjanda.

1. Víxlaðu útvíkkun á liðnum **Taxtaforstillingar**.
2. Veljið **Nýtt**.
3. Í reitinn **Taxtaforstilling** skal slá inn gildi.
4. Í reitinn **Heiti** skal slá inn gildi.
5. Í reitnum **Svæði** velurðu valkost úr fellivalmyndinni.
6. Í reitnum **Vöruhús** velurðu valkost úr fellivalmyndinni.
7. Í reitnum **Taxtavél** velurðu valkost úr fellivalmyndinni. Veljið taxtavél sem er í samræmi við samning sem á að hafa með farmflytjanda.  
8. Í reitnum **Taxtasniðmát** velurðu valkost úr fellivalmyndinni.
9. Í reitnum **Flutningstímavél** velurðu valkost úr fellivalmyndinni.
10. Veljið **Vista**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]