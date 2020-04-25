---
title: Setja upp farmflytjendur
description: Þetta efni sýnir hvernig eigi að setja upp flytjanda og skilgreina upplýsingar eins og þjónustu, afhendingarmáta sendingar, flutningstilboð, takmarkanir fyrir flutningsstöðu og flutningstaxta.
author: ShylaThompson
manager: tfehr
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6e6a29dce877a53d125c5a151da6cfbb13d46b29
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201595"
---
# <a name="set-up-shipping-carriers"></a>Setja upp farmflytjendur

[!include [banner](../../includes/banner.md)]

Þetta efni sýnir hvernig eigi að setja upp flytjanda og skilgreina upplýsingar eins og þjónustu, afhendingarmáta sendingar, flutningstilboð, takmarkanir fyrir flutningsstöðu og flutningstaxta. Samræmingaraðili við flutninga getur þá úthluta farmflytjanda á hleðslu á inn eða útleið.


## <a name="create-a-new-shipping-carrier"></a>Stofna nýtt farmflytjandi
1. Farðu í **Skoðunarrúðu > Kerfiseiningar > Uppsetning > Flutningsaðilar > Farmflytjendur**.
2. Veldu **Nýtt** í aðgerðarrúðunni.
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
5. Í reitnum **Flutningsaðferð** velurðu valkost úr fellivalmyndinni.

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

