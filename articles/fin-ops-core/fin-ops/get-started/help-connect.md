---
title: Tengja hjálparkerfið
description: Þetta efnisatriði lýsir þætti í hjálparkerfinu fyrir forrit Finance and Operations og veitir yfirlit yfir hvernig á að tengja þá og yfirlit yfir hvernig á að stofna sérsniðna hjálp.
author: margoc
manager: AnnBe
ms.date: 10/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4427388d75c1aef40a978ce35c831d5b714f2562
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/03/2020
ms.locfileid: "3006173"
---
# <a name="connect-the-help-system"></a>Tengja hjálparkerfið

[!include [banner](../includes/banner.md)]

Þetta efni lýsir íhlutum hjálparkerfisins fyrir forrit Finance and Operations, eins og Dynamics 365 Finance, Supply Chain Management, Commerce og Human Resources. Það veitir yfirlit yfir hvernig á að tengja þá og yfirlit yfir hvernig á að stofna sérsniðna hjálp.

## <a name="help-architecture"></a>Högun Hjálpar

Eftirfarandi skýringarmynd sýnir hluta hjálparkerfisins. Hjálparkerfi innan vörunnar sækir greinar úr https://docs.microsoft.com, auk verkefnaleiðbeininga sem eru geymdar í Viðskiptaferlavinnslu í Lifecycle Services (LCS).

> [!NOTE]
> Aðgerðirnar sem eru listaðar í skýringarmyndinni með stjörnu (\*) eru á vegvísnum, en eru ekki tiltækar enn.

[![Högun Hjálpar](./media/help-architecture.png)](./media/help-architecture.png)

## <a name="connecting-the-help-system"></a>Tenging við hjálparkerfi

> [!NOTE]
> Flipinn **Verkleiðbeiningar** er ekki í boði eins og stendur í Dynamics 365 Human Resources eða Commerce. Við erum að vinna í því að virkja þessa aðgerð í útgáfum í framtíðinni. Verkefnaleiðbeiningarnar í Hafist handa í Human Resources eru enn tiltækar og í þeim er farið yfir grunnvirkni. Málsmeðferð til vinnu er einnig fáanleg á docs.microsoft.com vefsvæðinu fyrir bæði Human Resources og Commerce.

Með skjámyndinni **Kerfisfæribreytur** tengja kerfisstjórar stykki í hjálparkerfinu fyrir innleiðingu.

[![Skjámynd kerfisfæribreyta með stillingum hjálparkerfis](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)

Á síðunni **Kerfisfæribreytur** skal fylgja þessum skrefum:

> [!IMPORTANT]
> Í fyrsta skipti er sem þú opnar flipann **Hjálp** verður þú að tengjast Lifecycle Services. Gætið þess að smella á tengil í miðri skjámyndinni, bíða eftir tengingu, loka svarglugga og smella á **Í lagi** til að komast á síðuna **Kerfisfæribreytur**.
>
> [![Tengjast við LCS](./media/connect-to-lcs-crop-1024x365.png "Tengjast við LCS")](./media/connect-to-lcs-crop.png)

1. Veljið Lifecycle Services verk til að tengjast.
2. Veljið BPM söfn (innan valins verks) til að sækja verkskráningu úr .
3. Velja birtingarröð BPM safna. Þetta ákvarðar í hvaða röð verkskráning úr í söfn birtast á **Hjálp** rúðunni.

Eftir að þessum skrefum hefur verið lokið, er hægt að opna rúðuna **Hjálp** og smella á flipann **Verkleiðbeiningar**. Nú sérðu verkefnaleiðbeiningar sem eiga við um síðuna sem þú ert á í forritum Finance and Operations. Ef engin verkefnaleiðbeiningar finnast er hægt að færa inn lykilorð til þess að fínstilla leitina.

### <a name="showing-translated-task-guides"></a>Sýnir þýddar leiðbeiningar verkefninu

Þýddar verkefnaleiðbeiningar voru sendar í maí 2016 APQC Unified Library, og í safninu Hafist handa (getting started). Í forritum Finance and Operations til að sjá staðfærða hjálp leiðarvísis fyrir verk , skal tryggja að þú sért tengd/ur við maí safnið. Tungumálið sem leiðarvísir fyrir verk birtist í er stjórnað fyrir hvern notanda samkvæmt tungumálastillingar undir **Valkostir** &gt; **> Kjörstillingar**.

> [!NOTE]
> Þó margar verkefnaleiðbeiningar hafi verið þýdd, er biðlarinn ekki að sýna þýdd heiti verkefnaleiðbeininga. Einnig, aðeins verkefnaleiðbeiningar sem voru gefnar út í febrúar 2016 eru í boði í þýðingu í maí safninu. Við munum gefa út uppfærða safn með fleiri þýðingum.
>
> - Ef verkefnaleiðbeiningar hefur verið þýdd, þegar þú opnar þessi verkefnaleiðbeiningar birtist allan texta þeirra í valið tungumál.
> - Ef verkefnaleiðbeiningar hefur ekki enn verið þýdd, þegar þú opnar það, bara nokkrar af textanum (Texti stjórnbúnaðar) munu birtast í valið tungumál.

## <a name="creating-custom-help"></a>Stofnun sérsniðinnar hjálpar

Hægt er að nota verkefnaleiðbeiningar til að stofna sérsniðna hjálp eða tengja vefsvæði við hjálparsvæðið.

### <a name="create-custom-help-with-task-guides"></a>Stofna sérsniðna hjálp með verkefnaleiðbeiningum

Hægt er að stofna sérsniðna hjálp fyrir Finance and Operations, Supply Chain Management og Commerce með því að stofna verkskráningar sem endurspegla innleiðingu þína og vista þær í LCS Business Process Library. Að auki getur þú ekki stofnað sérsniðnar verkefnaleiðbeiningar fyrir Human Resources.

Fyrir samstarfsaðila, ef þú færir safn inn í fyrirtækissafn og hefur það með í lausn, verður það tiltækt viðskiptavinum þínum. Einnig er hægt gera afrit af APQC Unified global library og síðan opna síðan afritið, opna verkskráningar úr því, breyta þeim og vista skráningar með breytingunum. Nánari upplýsingar er að finna [Tilföng verkskráningar](../../dev-itpro/user-interface/task-recorder.md).

### <a name="connect-a-custom-site"></a>Tengja sérsniðið svæði

Microsoft hefur útvegað hvítbók og sýnikóða sem lýsa því hvernig á að stofna og tengja sérsniðið svæði hjálpar við hjálparsvæðið. Frekari upplýsingar má finna á

- [Búðu til sérsniðna hjálp fyrir forrit Finance and Operations (hvítbók)](https://go.microsoft.com/fwlink/?linkid=2041185)
- [Sérsniðin hjálp GitHub-geymslu](https://github.com/microsoft/dynamics356f-o-custom-help)

## <a name="additional-resources"></a>Frekari upplýsingar

[Hjálparkerfi](help-overview.md)

[Tilföng verkskráningar](../../dev-itpro/user-interface/task-recorder.md)

[Búa til fylgiskjöl eða þjálfun með verkskráningu](../../dev-itpro/user-interface/task-recorder-training-docs.md)
