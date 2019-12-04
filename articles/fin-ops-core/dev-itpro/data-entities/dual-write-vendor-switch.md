---
title: Skipta á milli hönnunar lánardrottna
description: ''
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 4e97ff0b0e6195b5e3703e15a0bb0de7644ef8d1
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772365"
---
# <a name="switch-between-vendor-designs"></a>Skipta á milli hönnunar lánardrottna

[!include [banner](../includes/banner.md)]

## <a name="vendor-data-flow"></a>Gagnaflæði lánardrottins 

Ef þú notar önnur forrit Dynamics 365 við stjórnun lánardrottins og þú vilt einangra upplýsingar lánardrottins frá viðskiptavinum, notarðu þessa grunn lánardrottinshönnun.  

![Grunnlánardrottnaflæði](media/dual-write-switch-1.png)
 
Ef þú notar önnur forrit Dynamics 365 við stjórnun lánardrottins og þú vilt halda áfram að nota eininguna **Lykill** til að geyma upplýsingar lánardrottins geturðu notað þessa útvíkkuðu lánardrottinshönnun. Í þessari hönnun eru stækkaðar upplýsingar um lánardrottinn, eins og staða lánardrottins í bið og lánardrottinssniðs vistaðar í einingunni **lánardrottnar** í Common Data Service. 

![Útvíkkað lánardrottnaflæði](media/dual-write-switch-2.png)
 
Fylgdu skrefunum hér að neðan til að nota stækkaða lánardrottnahönnun: 
 
1. Lausnapakkinn **FramboðChainCommon** inniheldur ferlissniðmát verkflæðis eins og sýnt er á eftirfarandi mynd.
    > [!div class="mx-imgBorder"]
    > ![Ferlissniðmát verkflæðis](media/dual-write-switch-3.png)
2. Búðu til nýja verkflæðisferla með ferlissniðmáti verkflæðis: 
    1. Stofnaðu nýtt verkflæðisferli fyrir eininguna **Lánardrottinn** sem notar ferlissniðmát verkflæðis **Stofna lánardrottna í lykileiningu** og smelltu á **Í lagi**. Þetta verkflæði annast stofnunaraðstæður lánardrottins fyrir eininguna **Lykill**.
        > [!div class="mx-imgBorder"]
        > ![Stofna lánardrottna í lykileiningu](media/dual-write-switch-4.png)
    2. Stofnaðu nýtt verkflæðisferli fyrir eininguna **Lánardrottinn** sem notar ferlissniðmát verkflæðis **Uppfæra lykileiningu** og smelltu á **Í lagi**. Þetta verkflæði annast uppfærsluaðstæður lánardrottins fyrir eininguna **Lykill**. 
        > [!div class="mx-imgBorder"]
        > ![Uppfæra lyklaeiningu](media/dual-write-switch-5.png)
    3. Stofnaðu ný verkflæðisferli úr sniðmátunum sem voru stofnuð í einingunni **Lyklar**. 
        > [!div class="mx-imgBorder"]
        > ![Stofna lánardrottna í lykileiningu](media/dual-write-switch-6.png)
        > [!div class="mx-imgBorder"]
        > ![Uppfæra lánardrottnaeiningu](media/dual-write-switch-7.png)
    4. Þú getur stillt verkflæði sem rauntíma eða bakgrunnsverkflæði út frá þörfum þínum. 
        > [!div class="mx-imgBorder"]
        > ![Umbreyta í bakgrunnsverkflæði](media/dual-write-switch-8.png)
    5. Virkjaðu verkflæðin sem þú stofnaðir í einingunum **Lykill** og **Lánardrottinn** til að hefja notkun á Customer Engagement-einingunni **Lykill** til að geyma upplýsingar lánardrottins. 
 