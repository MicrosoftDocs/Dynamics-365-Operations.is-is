---
title: Skipta á milli lánardrottnahönnunar
description: Þetta efni lýsir hvernig skuli skipta á milli samþættingar lánardrottnagagna milli forrita Finance and Operations og Common Data Service.
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
ms.openlocfilehash: 0ecc401706911f8b92146b95bb6415185df8b451
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997553"
---
# <a name="switch-between-vendor-designs"></a>Skipta á milli lánardrottnahönnunar

[!include [banner](../../includes/banner.md)]



## <a name="vendor-data-flow"></a>Gagnaflæði lánardrottins 

Ef þú velur að nota eininguna **Lykill** til að geyma lánardrottna af gerðinni **Fyrirtæki** og eininguna **Hafa samband** til að geyma lánardrottna af gerðinni **Einstaklingur** stillirðu eftirfarandi verkflæði. Annars er ekki þörf á þessari stillingu.

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a>Notaðu stækkaða lánardrottnahönnun fyrir framleiðendur af gerðinni Fyrirtæki

Lausnapakkinn **Dynamics365FinanceExtended** inniheldur eftirfarandi sniðmát verkflæðisferla. Þú verður að búa til verkflæði fyrir hvert sniðmát.

+ Stofna lánardrottna í lyklaeiningu
+ Stofna lánardrottna í lánardrottnaeiningu
+ Uppfæra lánardrottna í lyklaeiningu
+ Uppfæra lánardrottna í lánardrottnaeiningu

Til að stofna nýja verkflæðisferla með ferlissniðmáti verkflæðis fylgirðu þessum skrefum.

1. Stofnaðu verkflæðisferli fyrir eininguna **Lánardrottinn** og veldu ferlissniðmát verkflæðis **Stofna lánardrottna í lyklaeiningu**. Veljið síðan **Í lagi**. Þetta verkflæði annast stofnunaraðstæður lánardrottins fyrir eininguna **Lykill**.

    ![Stofna lánardrottna í verkflæðisferlis lyklaeiningar](media/create_process.png)

2. Stofnaðu verkflæðisferli fyrir eininguna **Lánardrottinn** og veldu ferlissniðmát verkflæðis **Uppfæra lánardrottna í lyklaeiningu**. Veljið síðan **Í lagi**. Þetta verkflæði annast uppfærsluaðstæður lánardrottins fyrir eininguna **Lykill**.
3. Stofnaðu verkflæðisferli fyrir eininguna **Lykill** og veldu ferlissniðmát verkflæðis **Stofna lánardrottna í lánardrottnaeiningu**.
4. Stofnaðu verkflæðisferli fyrir eininguna **Lykill** og veldu ferlissniðmát verkflæðis **Uppfæra lánardrottna í lánardrottnaeiningu**.
5. Þú getur stillt verkflæði sem annaðhvort rauntíma- eða bakgrunnsverkflæði út frá þörfum þínum. Til að stilla verkflæði sem bakgrunnsflæði velurðu **Umbreyta í bakgrunnsverkflæði**.

    ![Hnappurinn Umbreyta í bakgrunnsverkflæði](media/background_workflow.png)

6. Virkjaðu verkflæðin sem þú stofnaðir fyrir einingarnar **Lykill** og **Lánardrottinn** til að hefja notkun á einingunni **Lykill** til að geyma upplýsingar um lánardrottna af gerðinni **Fyrirtæki**.

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a>Notaðu stækkaða lánardrottnahönnun fyrir framleiðendur af gerðinni Einstaklingur

Lausnapakkinn **Dynamics365FinanceExtended** inniheldur eftirfarandi sniðmát verkflæðisferla. Þú verður að búa til verkflæði fyrir hvert sniðmát.

+ Búðu til lánardrottinn af gerðinni Einstaklingur í einingunni Lánardrottinn
+ Búðu til lánardrottinn af gerðinni Einstaklingur í einingunni Tengiliður
+ Uppfæra lánardrottinn af gerðinni Einstaklingur í einingunni Tengiliður
+ Uppfæra lánardrottinn af gerðinni Einstaklingur í einingunni Lánardrottinn

Til að stofna nýja verkflæðisferla með ferlissniðmáti verkflæðis fylgirðu þessum skrefum.

1. Stofnaðu verkflæðisferli fyrir eininguna **Lánardrottinn** og veldu ferlissniðmát verkflæðis **Stofna lánardrottna af gerðinni Einstaklingur í tengiliðaeiningu**. Veljið síðan **Í lagi**. Þetta verkflæði annast stofnunaraðstæður lánardrottins fyrir eininguna **Tengiliður**.
2. Stofnaðu verkflæðisferli fyrir eininguna **Lánardrottinn** og veldu ferlissniðmát verkflæðis **Uppfæra lánardrottna af gerðinni Einstaklingur í tengiliðaeiningu**. Veljið síðan **Í lagi**. Þetta verkflæði annast uppfærsluaðstæður lánardrottins fyrir eininguna **Tengiliður**.
3. Stofnaðu verkflæðisferli fyrir eininguna **Tengiliður** og veldu sniðmátið **Stofna lánardrottna af gerðinni Einstaklingur í lánardrottnaeiningu**.
4. Stofnaðu verkflæðisferli fyrir eininguna **Tengiliður** og veldu sniðmátið **Uppfæra lánardrottna af gerðinni Einstaklingur í lánardrottnaeiningu**.
5. Þú getur stillt verkflæði sem annaðhvort rauntíma- eða bakgrunnsverkflæði út frá þörfum þínum. Til að stilla verkflæði sem bakgrunnsflæði velurðu **Umbreyta í bakgrunnsverkflæði**.
6. Virkjaðu verkflæðin sem þú stofnaðir í einingunum **Tengiliður** og **Lánardrottinn** til að hefja notkun á einingunni **Tengiliður** til að geyma upplýsingar um lánardrottna af gerðinni **Einstaklingur**.
