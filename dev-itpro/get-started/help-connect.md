---
title: "Tenging við hjálpargögnin"
description: "Þetta efnisatriði lýsir þætti í hjálparkerfinu fyrir Microsoft Dynamics 365 for Operations og veitir yfirlit yfir hvernig á að tengja þá og yfirlit yfir hvernig á að stofna sérsniðna hjálp."
author: margoc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 5ac5e30cff2239f601778001368fa7aaba478f5c
ms.lasthandoff: 03/31/2017


---

# <a name="connect-the-help-system"></a>Tenging við hjálpargögnin

Þetta efnisatriði lýsir þætti hjálparkerfinu fyrir Microsoft Dynamics 365 fyrir Aðgerðir. Hún veitir yfirlit yfir hvernig á að tengja þessa íhluti og yfirlit yfir hvernig á að stofna sérsniðna hjálp. 

<a name="help-architecture"></a>Högun Hjálpar
-----------------

Eftirfarandi skýringarmynd sýnir hluta Dynamics 365 fyrir Aðgerðir sem aðstoða Við kerfið. Afurð í hjálparkerfinu sækir greinum úr Dynamics 365 fyrir Aðgerðir svæði í https://docs.microsoft.com, eins og verki leiðbeiningar geymd í Viðskiptaferlavinnslu í Lifecycle Services (LCS). 
**Athugasemd:** aðgerðir á lista í skýringarmynd með stjörnu (\*) eru áætlaðir en er ekki tiltækt enn. [![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)

## <a name="connecting-the-help-system"></a>Tengingu við hjálparkerfi
Með því að nota í **Kerfisfæribreytum** síðu kerfisstjórum tengjast stykki af í hjálparkerfinu að innleiðingu. [![Færibreytuskjámynd kerfið með Hjálp stillingar](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) á á **kerfisfæribreytum** síðunni, skal fylgja þessum skrefum:

1.  **Mikilvægt:** í fyrsta sinn sem er opnuð í **Hjálp** flipanum tengjast verður þjónustutilviki Lifecycle Services. Gætið þess að smella á tengilinn innstimplun skjámyndinni, bíða tengingu skal loka svarglugganum og smellið **í lagi** til að fá í á **Kerfisfæribreytum** síðu. [![Tengjast LCS](./media/connect-to-lcs-crop-1024x365.png "Tengjast LCS")](./media/connect-to-lcs-crop.png)
2.  Veljið Lifecycle Services verk til að tengjast.
3.  Veljið BPM söfn (innan valins verks) til að sækja verkskráningu úr .
4.  Velja birtingarröð BPM safna. Þetta ákvarðar í hvaða röð verkskráning úr í söfn birtast á **Hjálp** rúðunni.

Eftir að þessum skrefum hefur verið lokið, er hægt að opna rúðuna **Hjálp** og smella á flipann **Verkleiðbeiningar**. Þú sérð verkefnaleiðbeiningar sem eiga við síðu sem þú ert á í Dynamics 365 for Operations. Ef engin verkefnaleiðbeiningar finnast er hægt að færa inn lykilorð til þess að fínstilla leitina.

### <a name="showing-translated-task-guides"></a>Sýnir þýddar leiðbeiningar verkefninu

Þýdd verkefni leiðbeiningar voru sent fyrst í 2016 Maí APQC, vefhlutinn sameinaður Safnið og safn Hafist. Í Dynamics 365 for Operations til að sjá staðfærða hjálp leiðarvísis fyrir verk , skal tryggja að þú sért tengd við maí safnið. Tungumálið sem leiðarvísi fyrir verk sem birtist í stjórnast hvers notanda eftir tungumálastillingar undir **Valkosti**&gt;**Kjörstillingar**. **Athugasemd:** þó margar verkefnaleiðbeiningar hafi verið þýdd, er Dynamics 365 for Operations-biðlarinn ekki að sýna þýdd heiti verkefnaleiðbeininga. Einnig er aðeins í verki leiðbeiningar sem var losuð í Febrúar 2016 eru tiltækar í þýðingar í safninu Maí. Við munum gefa út uppfærða safn með fleiri þýðingum.

-   Ef verkefnaleiðbeiningar hefur verið þýdd, þegar þú opnar þessi verkefnaleiðbeiningar birtist allan texta þeirra í valið tungumál.
-   Ef verkefnaleiðbeiningar hefur ekki enn verið þýdd, þegar þú opnar það, bara nokkrar af textanum (Texti stjórnbúnaðar) munu birtast í valið tungumál.

## <a name="creating-custom-help"></a>Stofnun sérsniðinnar hjálpar
Hægt er að stofna sérsniðna hjálp fyrir innleiðingu á Dynamics 365 for Operations eftir stofnun verkskráningar sem endurspegla innleiðingu og vistar þær á LCS Business Ferli Safnið. Fyrir samstarfsaðila, ef þú færir safn inn í fyrirtækissafn og hefur það með í lausn, verður það tiltækt viðskiptavinum þínum. Einnig er hægt gera afrit af APQC Unified global library og síðan opna síðan afritið, opna verkskráningar úr því, breyta þeim og vista skráningar með breytingunum. Nánari upplýsingar, sjá [Hvernig stofna á verkskráningu sem nota á sem fylgiskjal eða þjálfun](../user-interface/task-recorder.md).

<a name="see-also"></a>Sjá einnig
--------

[Help overview](help-overview.md)

[Yfirlit verkefna verkskráningar](../user-interface/task-recorder.md)

[Stofna verkskráning til að nota sem fylgiskjölum eða þjálfun](../user-interface/task-recorder-training-docs.md)

[Stofna Nýja Þjálfun Söfn fyrir Dynamics 365 fyrir Aðgerðir innan Lifecycle Services með Verkskráningu (Ytri tengil)](https://docs.com/mufife/163372c6-f366-4c5a-94fa-93e2c25f878a/creating-new-training-libraries-for-dynamics-ax)


