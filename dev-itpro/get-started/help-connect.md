---
title: "Tenging við hjálpargögnin"
description: "Þetta efnisatriði lýsir þætti í hjálparkerfinu fyrir Microsoft Dynamics 365 for Operations og veitir yfirlit yfir hvernig á að tengja þá og yfirlit yfir hvernig á að stofna sérsniðna hjálp."
author: margoc
manager: AnnBe
ms.date: 04/04/2017
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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: f9af4de5f15125569d8f3e78f36e6a2b9c2a089b
ms.contentlocale: is-is
ms.lasthandoff: 04/25/2017


---

# <a name="connect-the-help-system"></a>Tenging við hjálpargögnin

[!include[banner](../includes/banner.md)]


Þetta efnisatriði lýsir þætti í hjálparkerfinu fyrir Microsoft Dynamics 365 for Operations. Það veitir yfirlit yfir hvernig á að tengja þá og yfirlit yfir hvernig á að stofna sérsniðna hjálp. 

<a name="help-architecture"></a>Högun Hjálpar
-----------------

Eftirfarandi skýringarmynd sýnir hluta hjálparkerfisins í Dynamics 365 for Operations. Hjálparkerfi innan vörunnar sækir greinar úr svæði Dynamics 365 for Operations á https://docs.microsoft.com auk verkefnaleiðbeininga sem eru geymdar í Viðskiptaferlavinnslu í Lifecycle Services (LCS). 
**Athugasemd** Aðgerðirnar sem eru listaðar í skýringarmyndinni með stjörnu (\*) eru á vegvísnum, en eru ekki tiltækar enn. [![Högun Hjálpar](./media/help-architecture.png)](./media/help-architecture.png)

## <a name="connecting-the-help-system"></a>Tenging við hjálparkerfi
Með skjámyndinni **Kerfisfæribreytur** tengja kerfisstjórar stykki í hjálparkerfinu fyrir innleiðingu. [![Snið kerfisfæribreyta með Stillingar fyrir hjálp ](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) á **kerfisfæribreytum** síðunni, skal fylgja þessum skrefum:

> [!IMPORTANT]
> Í fyrsta skipti er sem þú opnar flipann **Hjálp** verður þú að tengjast Lifecycle Services. Gætið þess að smella á tengil í miðri skjámyndinni, bíða eftir tengingu, loka svarglugga og smella á **Í lagi** til að komast á síðuna **Kerfisfæribreytur**.[![Tengjast LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)

1.  Veljið Lifecycle Services verk til að tengjast.
2.  Veljið BPM söfn (innan valins verks) til að sækja verkskráningu úr .
3.  Velja birtingarröð BPM safna. Þetta ákvarðar í hvaða röð verkskráning úr í söfn birtast á **Hjálp** rúðunni.

Eftir að þessum skrefum hefur verið lokið, er hægt að opna rúðuna **Hjálp** og smella á flipann **Verkleiðbeiningar**. Þú sérð verkefnaleiðbeiningar sem eiga við síðu sem þú ert á í Dynamics 365 for Operations. Ef engin verkefnaleiðbeiningar finnast er hægt að færa inn lykilorð til þess að fínstilla leitina.

### <a name="showing-translated-task-guides"></a>Sýnir þýddar leiðbeiningar verkefninu

Þýddar verkefnaleiðbeiningar voru sendar í maí 2016 APQC Unified Library, og í safninu Hafist handa (getting started). Í Dynamics 365 for Operations til að sjá staðfærða hjálp leiðarvísis fyrir verk , skal tryggja að þú sért tengd við maí safnið. Tungumálið sem leiðarvísir fyrir verk birtist í er stjórnað fyrir hvern notanda samkvæmt tungumálastillingar undir **Valkostir** &gt; **> Kjörstillingar**. 

> [!NOTE]
> Þó svo margar verkefnaleiðbeiningar hafi verið þýddar er Dynamics 365 for Operations-biðlarinn ekki að sýna þýdd heiti verkefnaleiðbeininga. Einnig, aðeins verkefnaleiðbeiningar sem voru gefnar út í febrúar 2016 eru í boði í þýðingu í maí safninu. Við munum gefa út uppfærða safn með fleiri þýðingum.
> -   Ef verkefnaleiðbeiningar hefur verið þýdd, þegar þú opnar þessi verkefnaleiðbeiningar birtist allan texta þeirra í valið tungumál.
> -   Ef verkefnaleiðbeiningar hefur ekki enn verið þýdd, þegar þú opnar það, bara nokkrar af textanum (Texti stjórnbúnaðar) munu birtast í valið tungumál.

## <a name="creating-custom-help"></a>Stofnun sérsniðinnar hjálpar
Hægt er að stofna sérsniðna hjálp fyrir innleiðingu á Dynamics 365 for Operations eftir stofnun verkskráningar sem endurspegla innleiðingu og vistar þær á LCS Business Ferli Safnið. Fyrir samstarfsaðila, ef þú færir safn inn í fyrirtækissafn og hefur það með í lausn, verður það tiltækt viðskiptavinum þínum. Einnig er hægt gera afrit af APQC Unified global library og síðan opna síðan afritið, opna verkskráningar úr því, breyta þeim og vista skráningar með breytingunum. Frekari upplýsingar er að finna í efnisatriðinu [Hvernig stofna á verkskráningu sem nota á sem fylgigögn eða þjálfun](../user-interface/task-recorder.md).

<a name="see-also"></a>Sjá einnig
--------

[Hjálparyfirlit](help-overview.md)

[yfirlit verkskráningar](../user-interface/task-recorder.md)

[Stofna verkskráning til að nota sem fylgiskjölum eða þjálfun](../user-interface/task-recorder-training-docs.md)





