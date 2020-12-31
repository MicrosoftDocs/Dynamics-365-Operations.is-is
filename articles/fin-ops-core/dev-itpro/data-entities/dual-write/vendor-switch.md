---
title: Skipta á milli lánardrottnahönnunar
description: Þetta efni lýsir hvernig skuli skipta á milli samþættingar lánardrottnagagna milli forrita Finance and Operations og Dataverse.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 731efd3ae841960f3a2c0b9be210c5c68ac835f5
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685510"
---
# <a name="switch-between-vendor-designs"></a>Skipta á milli lánardrottnahönnunar

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



## <a name="vendor-data-flow"></a>Gagnaflæði lánardrottins 

Ef þú velur að nota eininguna **Lykill** til að geyma lánardrottna af gerðinni **Fyrirtæki** og eininguna **Hafa samband** til að geyma lánardrottna af gerðinni **Einstaklingur** stillirðu eftirfarandi verkflæði. Annars er ekki þörf á þessari stillingu.

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a>Notaðu stækkaða lánardrottnahönnun fyrir framleiðendur af gerðinni Fyrirtæki

Lausnapakkinn **Dynamics365FinanceExtended** inniheldur eftirfarandi sniðmát verkflæðisferla. Þú verður að búa til verkflæði fyrir hvert sniðmát.

+ Stofna lánardrottna í reikningstöflu
+ Stofna lánardrottna í lánardrottnatöflu
+ Uppfæra lánardrottna í reikningstöflu
+ Uppfæra lánardrottna í lánardrottnatöflu

Til að stofna nýja verkflæðisferla með ferlissniðmáti verkflæðis fylgirðu þessum skrefum.

1. Stofnaðu verkflæðisferli fyrir eininguna **Lánardrottinn** og veldu sniðmát verkflæðisferlisins **Stofna lánardrottna í reikningstöflu**. Veljið síðan **Í lagi**. Þetta verkflæði annast stofnunaraðstæður lánardrottins fyrir eininguna **Lykill**.

    ![Stofna lánardrottna í reikningstöflu verkflæðisferlis](media/create_process.png)

2. Stofnaðu verkflæðisferli fyrir eininguna **Lánardrottinn** og veldu sniðmát verkflæðisferlisins **Uppfæra lánardrottna í reikningstöflu**. Veljið síðan **Í lagi**. Þetta verkflæði annast uppfærsluaðstæður lánardrottins fyrir eininguna **Lykill**.
3. Stofnaðu verkflæðisferli fyrir eininguna **Reikningur** og veldu sniðmát verkflæðisferlisins **Stofna lánardrottna í lánardrottnatöflu**.
4. Stofnaðu verkflæðisferli fyrir eininguna **Reikningur** og veldu sniðmát verkflæðisferlisins **Uppfæra lánardrottna í lánardrottnatöflu**.
5. Þú getur stillt verkflæði sem annaðhvort rauntíma- eða bakgrunnsverkflæði út frá þörfum þínum. Til að stilla verkflæði sem bakgrunnsflæði velurðu **Umbreyta í bakgrunnsverkflæði**.

    ![Hnappurinn Umbreyta í bakgrunnsverkflæði](media/background_workflow.png)

6. Virkjaðu verkflæðin sem þú stofnaðir fyrir töflurnar **Reikningur** og **Lánardrottinn** til að hefja notkun á einingunni **Reikningur** til að geyma upplýsingar um lánardrottna af gerðinni **Fyrirtæki**.

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a>Notaðu stækkaða lánardrottnahönnun fyrir framleiðendur af gerðinni Einstaklingur

Lausnapakkinn **Dynamics365FinanceExtended** inniheldur eftirfarandi sniðmát verkflæðisferla. Þú verður að búa til verkflæði fyrir hvert sniðmát.

+ Stofna lánardrottna af gerðinni einstaklingur í lánardrottnatöflu
+ Stofna lánardrottna af gerðinni einstaklingur í tengiliðatöflu
+ Uppfæra lánardrottna af gerðinni einstaklingur í tengiliðatöflu
+ Uppfæra lánardrottna af gerðinni einstaklingur í lánardrottnatöflu

Til að stofna nýja verkflæðisferla með ferlissniðmáti verkflæðis fylgirðu þessum skrefum.

1. Stofnaðu verkflæðisferli fyrir eininguna **Lánardrottinn** og veldu sniðmát verkflæðisferlisins **Stofna lánardrottna af gerðinni einstaklingur í tengiliðatöflu**. Veljið síðan **Í lagi**. Þetta verkflæði annast stofnunaraðstæður lánardrottins fyrir eininguna **Tengiliður**.
2. Stofnaðu verkflæðisferli fyrir eininguna **Lánardrottinn** og veldu sniðmát verkflæðisferlisins **Uppfæra lánardrottna af gerðinni einstaklingur í tengiliðatöflu**. Veljið síðan **Í lagi**. Þetta verkflæði annast uppfærsluaðstæður lánardrottins fyrir eininguna **Tengiliður**.
3. Stofnaðu verkflæðisferli fyrir eininguna **Tengiliður** og veldu sniðmát verkflæðisferlisins **Stofna lánardrottna af gerðinni einstaklingur í tengiliðatöflu**.
4. Stofnaður verkflæðisferli fyrir eininguna **Tengiliður** og veldu sniðmát verkflæðisferlisins **Uppfæra lánardrottna af gerðinni einstaklingur í tengiliðatöflu**.
5. Þú getur stillt verkflæði sem annaðhvort rauntíma- eða bakgrunnsverkflæði út frá þörfum þínum. Til að stilla verkflæði sem bakgrunnsflæði velurðu **Umbreyta í bakgrunnsverkflæði**.
6. Virkjaðu verkflæðin sem þú stofnaðir í töflunum **Tengiliður** og **Lánardrottinn** til að hefja notkun á einingunni **Tengiliður** til að geyma upplýsingar um lánardrottna af gerðinni **Einstaklingur**.
