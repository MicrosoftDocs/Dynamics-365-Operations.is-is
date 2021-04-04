---
title: Gagnafræðileg próf með gögnum með Regression Suite Automation Tool
description: Í þessu efni er fjallað um ráðleggingar varðandi prófanir á gögnum með því að nota Regression Suite Automation Tool.
author: kfend
manager: AnnBe
ms.date: 09/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 21761
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2019-09-11
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 63d747cb04cf0d6503e326e8e2ac8b86002c23ca
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5566377"
---
# <a name="data-agnostic-testing-using-the-regression-suite-automation-tool"></a>Gagnafræðileg próf með gögnum með Regression Suite Automation Tool

[!include [banner](../includes/banner.md)]

Þó að virkni löggildingar ERP forrita geti ekki verið að fullu gagnagagnræn, þá eru til margir áfangar og aðferðir til að prófa. Þessir prófunarstig eru m.a.:  

- SysTest rammi
- ATL rammi
- Regression Suite Automation Tool (RSAT)

[![Próf flokkunarpýramída](./media/rsat-data-agnostic-testing-01.PNG)](./media/rsat-data-agnostic-testing-01.PNG)

## <a name="overview"></a>Yfirlit
-   **SysTest umgjörð** - SysTest umgjörðin er áreiðanleg til að skrifa einingapróf. Vegna þess að einingapróf eru venjulega að prófa aðferð eða aðgerð, ættu þau alltaf að vera gögn samnýtt og aðeins háð innsláttargögnum sem eru til staðar sem hluti af prófinu.
-   **ATL umgjörð** - Microsoft er með ATL ramma sem er abstrakt á SysTest umgjörðina og gerir hagnýt prófaskrif mun einfaldari og áreiðanlegri. Þessa ramma ætti að nota til að skrifa íhlutapróf eða einföld samþættingarpróf.
-   **RSAT** - RSAT er notað við samþættingarpróf og hagsveiflupróf. Hagsveifluprófin, einnig kölluð aðhvarfsgildingarprófanir, eru háð fyrirliggjandi gögnum. Samt sem áður geta þessi próf orðið gagnörvandi ef þú tekur til viðbótarþátta. 

    - O Þar sem einingapróf og íhlutapróf eru lágmörk og geta að öllu leyti verið gagnagagnafull gögn (ekki háð núverandi gagnapakka), eru hagsveiflupróf eða aðhvarfsgildingarprófanir háð nokkrum gögnum sem fyrir eru. Þessi gögn fela í sér uppsetningu, stillingar (breytur) og aðalgögn (viðskiptavini, smásali, hlutir osfrv.), En aldrei viðskiptagögn. Gakktu úr skugga um að meðan á prófinu stendur, ef einhverju af þessu er breytt, að þeim sé snúið aftur sem hluti af lokaprófinu.
    - Veldu aðalgögn út frá ákveðnum forsendum í stað þess að velja ákveðna skrá. Til dæmis, ef þú vilt velja hlut út frá víddargildum hans og framboði á lager, síaðu vörulistann með þessum gildum, veldu fyrsta hlutinn og afritaðu númerið sem á að nota til framtíðarprófa. Ef það er einföld aðalgagnalína eins og viðskiptavinur, söluaðili eða hlutur, þá er hægt að búa hana til sem hluta af sjálfvirkni og nota í framtíðarprófum með keðju. 
    - O Sláðu inn sérstök auðkenni, svo sem reikningsnúmer, í gegnum númeraröðina eða með því að nota Microsoft Excel-aðgerðir eins og =TEXT(NOW(),"yyyymmddhhmm"). Þessi aðgerð mun veita einstakt númer á hverri mínútu, sem gerir þér kleift að fylgjast með þegar aðgerðin átti sér stað. Þetta er hægt að nota fyrir breytur eins og móttökunúmer vöru og reikningsnúmer lánardrottins. Þessar prófanir halda áfram að vinna í sama gagnagrunni aftur og aftur, án þess að þurfa neina endurreisn.
    - Stilltu alltaf **Breyta stillingu** umhverfisins á **Lesa** eða **Breyta** sem fyrsta prófatilvikið vegna þess að sjálfgefinn valkostur er **Sjálfvirkt**. Valkostirnir **Sjálfvirkt** nota alltaf fyrri stillingu og geta valdið óáreiðanlegum prófum. 
 
    [![Valkostasíða, afkastaflipi](./media/rsat-data-agnostic-testing-02.PNG)](./media/rsat-data-agnostic-testing-02.PNG)
 
    - Staðfesta aðeins eftir að þú síar á tiltekin viðskipti í stað almennrar staðfestingar. Til dæmis, fyrir fjölda færslna, síaðu að viðskiptanúmerinu eða viðskiptadeginum þannig að löggildingin útiloki öll önnur viðskipti. 
    - Ef þú ert að athuga jafnvægi viðskiptavina eða fjárhagsáætlunarprófun skaltu vista gildi fyrst og bæta síðan við viðskiptagildi þínu til að staðfesta væntanlega niðurstöðu í stað þess að staðfesta fast væntanlegt gildi. 
 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]