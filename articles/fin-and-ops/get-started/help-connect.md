---
title: "Tenging við hjálpargögnin"
description: "Þetta efnisatriði lýsir þáttum í hjálparkerfinu fyrir Microsoft Dynamics 365 for Finance and Operations og veitir yfirlit yfir hvernig eigi að tengja þá og yfirlit yfir hvernig eigi að stofna sérsniðna hjálp."
author: margoc
manager: AnnBe
ms.date: 09/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c0942b66859da3659be49b19986bfd146ac43130
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="connect-the-help-system"></a>Tenging við hjálpargögnin

[!include[banner](../includes/banner.md)]


Þetta efnisatriði lýsir þáttum í hjálparkerfinu fyrir Microsoft Dynamics 365 for Finance and Operations. Það veitir yfirlit yfir hvernig á að tengja þá og yfirlit yfir hvernig á að stofna sérsniðna hjálp. 

## <a name="help-architecture"></a>Högun Hjálpar
Eftirfarandi skýringarmynd sýnir hluta hjálparkerfisins í Finance and Operations. Hjálparkerfi innan vörunnar sækir greinar úr svæði Finance and Operations á https://docs.microsoft.com auk verkefnaleiðbeininga sem eru geymdar í Viðskiptaferlavinnslu í Lifecycle Services (LCS). 
> [!NOTE]
> Aðgerðirnar sem eru listaðar í skýringarmyndinni með stjörnu (\*) eru á vegvísnum, en eru ekki tiltækar enn. [![Högun Hjálpar](./media/help-architecture.png)](./media/help-architecture.png)


## <a name="connecting-the-help-system"></a>Tenging við hjálparkerfi
> [!NOTE]
> Flipinn **Verkefnaleiðbeiningar** er ekki tiltækur eins og er í Microsoft Dynamics 365 for Talent og Microsoft Dynamics 365 for Retail. Við erum að vinna í því að virkja þessa aðgerð í útgáfum í framtíðinni. Verkefnaleiðbeiningarnar í Hafist handa í Talent eru enn tiltækar og í þeim er farið yfir grunnvirkni. Leiðbeiningar fyrir aðstoð er einnig að finna á docs.microsoft.com site ([docs.microsoft.com/dynamics365/unified-operations](../../index.md)) fyrir bæði Retail og Talent.
 

Með skjámyndinni **Kerfisfæribreytur** tengja kerfisstjórar stykki í hjálparkerfinu fyrir innleiðingu. [![Snið kerfisfæribreyta með Stillingar fyrir hjálp ](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) á **kerfisfæribreytum** síðunni, skal fylgja þessum skrefum:

> [!IMPORTANT]
> Í fyrsta skipti er sem þú opnar flipann **Hjálp** verður þú að tengjast Lifecycle Services. Gætið þess að smella á tengil í miðri skjámyndinni, bíða eftir tengingu, loka svarglugga og smella á **Í lagi** til að komast í **Kerfisfæribreytur** síðuna.[![Tengjast LCS](./media/connect-to-lcs-crop-1024x365.png "Tengjast LCS")](./media/connect-to-lcs-crop.png)

1.  Veljið Lifecycle Services verk til að tengjast.
2.  Veljið BPM söfn (innan valins verks) til að sækja verkskráningu úr .
    - Fyrir Finance and Operations, fyrir Microsoft efni, skal velja nýjasta APQU Unified Library fyrir Finance and Operations. 
    - Safn verður gefið út fyrir Retail í nánustu framtíð. 
    - Þú þarft ekki að velja safn fyrir Talent — búið er að setja tengingu við rétt safn fyrir þig. 

3.  Velja birtingarröð BPM safna. Þetta ákvarðar í hvaða röð verkskráning úr í söfn birtast á **Hjálp** rúðunni.

Eftir að þessum skrefum hefur verið lokið, er hægt að opna rúðuna **Hjálp** og smella á flipann **Verkleiðbeiningar**. Þú sérð verkefnaleiðbeiningar sem eiga við síðu sem þú ert á í Finance and Operations. Ef engin verkefnaleiðbeiningar finnast er hægt að færa inn lykilorð til þess að fínstilla leitina.

### <a name="showing-translated-task-guides"></a>Sýnir þýddar leiðbeiningar verkefninu

Þýddar verkefnaleiðbeiningar voru sendar í maí 2016 APQC Unified Library, og í safninu Hafist handa (getting started). Ef þú notar Finance and Operations og vilt sjá staðbundna verkefnahjálp skaltu ganga úr skugga um að þú sért tengd(ur) við safnið fyrir maí. Tungumálið sem leiðarvísir fyrir verk birtist í er stjórnað fyrir hvern notanda samkvæmt tungumálastillingar undir **Valkostir** &gt; **> Kjörstillingar**. 

> [!NOTE]
> Þó að margar verkefnaleiðbeiningar hafi verið þýddar sýnir Finance and Operations-biðlarinn ekki þýdd heiti verkefnaleiðbeininga eins og er. Einnig, aðeins verkefnaleiðbeiningar sem voru gefnar út í febrúar 2016 eru í boði í þýðingu í maí safninu. Við munum gefa út uppfærða safn með fleiri þýðingum.
> -   Ef verkefnaleiðbeiningar hefur verið þýdd, þegar þú opnar þessi verkefnaleiðbeiningar birtist allan texta þeirra í valið tungumál.
> -   Ef verkefnaleiðbeiningar hefur ekki enn verið þýdd, þegar þú opnar það, bara nokkrar af textanum (Texti stjórnbúnaðar) munu birtast í valið tungumál.

## <a name="creating-custom-help"></a>Stofnun sérsniðinnar hjálpar
Hægt er að stofna sérsniðna hjálp fyrir Finance and Operations og fyrir Retail með því að stofna verkskráningar sem endurspegla innleiðingu þína og vista þær í LCS Business Process Library. Ekki er hægt að stofna sérsniðnar verkefnaleiðbeiningar fyrir Talent. 

Fyrir samstarfsaðila, ef þú færir safn inn í fyrirtækissafn og hefur það með í lausn, verður það tiltækt viðskiptavinum þínum. Einnig er hægt gera afrit af APQC Unified global library og síðan opna síðan afritið, opna verkskráningar úr því, breyta þeim og vista skráningar með breytingunum. Frekari upplýsingar er að finna í efnisatriðinu [Hvernig stofna á verkskráningu sem nota á sem fylgigögn eða þjálfun](../../dev-itpro/user-interface/task-recorder.md).

<a name="see-also"></a>Sjá einnig
--------

[Hjálparyfirlit](help-overview.md)

[yfirlit verkskráningar](../../dev-itpro/user-interface/task-recorder.md)

[Stofna verkskráning til að nota sem fylgiskjölum eða þjálfun](../../dev-itpro/user-interface/task-recorder-training-docs.md)





