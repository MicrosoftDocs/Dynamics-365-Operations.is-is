---
title: Skipta á milli lánardrottnahönnunar
description: Þessi grein lýsir hvernig skuli skipta á milli samþættingar lánardrottnagagna milli forrita fjármála- og reksturs og Dataverse.
author: RamaKrishnamoorthy
ms.date: 09/20/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 5a1b3a6049e7e31e7e5bdcf690a766ecea8dc4b1
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/02/2022
ms.locfileid: "9112335"
---
# <a name="switch-between-vendor-designs"></a>Skipta á milli lánardrottnahönnunar

[!include [banner](../../includes/banner.md)]





## <a name="vendor-data-flow"></a>Gagnaflæði lánardrottins 

Ef þú velur að nota töfluna **Lykill** til að geyma lánardrottna af gerðinni **Fyrirtæki** og töfluna **Hafa samband** til að geyma lánardrottna af gerðinni **Einstaklingur** stillirðu eftirfarandi verkflæði. Annars er ekki þörf á þessari stillingu.

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a>Notaðu stækkaða lánardrottnahönnun fyrir framleiðendur af gerðinni Fyrirtæki

Lausnapakkinn **Dynamics365FinanceExtended** inniheldur eftirfarandi sniðmát verkflæðisferla. Þú verður að búa til verkflæði fyrir hvert sniðmát.

+ Stofna lánardrottna í reikningstöflu
+ Stofna lánardrottna í lánardrottnatöflu
+ Uppfæra lánardrottna í reikningstöflu
+ Uppfæra lánardrottna í lánardrottnatöflu

Til að stofna nýja verkflæðisferla með ferlissniðmáti verkflæðis fylgirðu þessum skrefum.

1. Stofnaðu verkflæðisferli fyrir töfluna **Lánardrottinn** og veldu sniðmát verkflæðisferlisins **Stofna lánardrottna í reikningstöflu**. Veljið síðan **Í lagi**. Þetta verkflæði annast stofnunaraðstæður lánardrottins fyrir töfluna **Lykill**.

    ![Stofna lánardrottna í reikningstöflu verkflæðisferlis.](media/create_process.png)

2. Stofnaðu verkflæðisferli fyrir töfluna **Lánardrottinn** og veldu sniðmát verkflæðisferlisins **Uppfæra lánardrottna í reikningstöflu**. Veljið síðan **Í lagi**. Þetta verkflæði annast uppfærsluaðstæður lánardrottins fyrir töfluna **Lykill**.
3. Stofnaðu verkflæðisferli fyrir töfluna **Reikningur** og veldu sniðmát verkflæðisferlisins **Stofna lánardrottna í lánardrottnatöflu**.
4. Stofnaðu verkflæðisferli fyrir töfluna **Reikningur** og veldu sniðmát verkflæðisferlisins **Uppfæra lánardrottna í lánardrottnatöflu**.
5. Þú getur stillt verkflæði sem annaðhvort rauntíma- eða bakgrunnsverkflæði út frá þörfum þínum. Til að stilla verkflæði sem bakgrunnsflæði velurðu **Umbreyta í bakgrunnsverkflæði**.

    ![Hnappurinn Umbreyta í bakgrunnsverkflæði.](media/background_workflow.png)

6. Virkjaðu verkflæðin sem þú stofnaðir fyrir töflurnar **Reikningur** og **Lánardrottinn** til að hefja notkun á töflunni **Reikningur** til að geyma upplýsingar um lánardrottna af gerðinni **Fyrirtæki**.

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a>Notaðu stækkaða lánardrottnahönnun fyrir framleiðendur af gerðinni Einstaklingur

Lausnapakkinn **Dynamics365FinanceExtended** inniheldur eftirfarandi sniðmát verkflæðisferla. Þú verður að búa til verkflæði fyrir hvert sniðmát.

+ Stofna lánardrottna af gerðinni einstaklingur í lánardrottnatöflu
+ Stofna lánardrottna af gerðinni einstaklingur í tengiliðatöflu
+ Uppfæra lánardrottna af gerðinni einstaklingur í tengiliðatöflu
+ Uppfæra lánardrottna af gerðinni einstaklingur í lánardrottnatöflu

Til að stofna nýja verkflæðisferla með ferlissniðmáti verkflæðis fylgirðu þessum skrefum.

1. Stofnaðu verkflæðisferli fyrir töfluna **Lánardrottinn** og veldu sniðmát verkflæðisferlisins **Stofna lánardrottna af gerðinni einstaklingur í tengiliðatöflu**. Veljið síðan **Í lagi**. Þetta verkflæði annast stofnunaraðstæður lánardrottins fyrir töfluna **Tengiliður**.
2. Stofnaðu verkflæðisferli fyrir töfluna **Lánardrottinn** og veldu sniðmát verkflæðisferlisins **Uppfæra lánardrottna af gerðinni einstaklingur í tengiliðatöflu**. Veljið síðan **Í lagi**. Þetta verkflæði annast uppfærsluaðstæður lánardrottins fyrir töfluna **Tengiliður**.
3. Stofnaðu verkflæðisferli fyrir töfluna **Tengiliður** og veldu sniðmát verkflæðisferlisins **Stofna lánardrottna af gerðinni einstaklingur í tengiliðatöflu**.
4. Stofnaður verkflæðisferli fyrir töfluna **Tengiliður** og veldu sniðmát verkflæðisferlisins **Uppfæra lánardrottna af gerðinni einstaklingur í tengiliðatöflu**.
5. Þú getur stillt verkflæði sem annaðhvort rauntíma- eða bakgrunnsverkflæði út frá þörfum þínum. Til að stilla verkflæði sem bakgrunnsflæði velurðu **Umbreyta í bakgrunnsverkflæði**.
6. Virkjaðu verkflæðin sem þú stofnaðir í töflunum **Tengiliður** og **Lánardrottinn** til að hefja notkun á töflunni **Tengiliður** til að geyma upplýsingar um lánardrottna af gerðinni **Einstaklingur**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
