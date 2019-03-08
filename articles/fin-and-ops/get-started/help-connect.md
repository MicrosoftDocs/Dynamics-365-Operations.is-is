---
title: Tengja hjálparkerfið
description: Þetta efnisatriði lýsir þætti í hjálparkerfinu fyrir Microsoft Dynamics 365 for Finance and Operations og veitir yfirlit yfir hvernig á að tengja þá og yfirlit yfir hvernig á að stofna sérsniðna hjálp.
author: margoc
manager: AnnBe
ms.date: 11/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
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
ms.openlocfilehash: 673b01648127fe1d19fb3c75c4d6812c4f22c761
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "317730"
---
# <a name="connect-the-help-system"></a>Tengja hjálparkerfið

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir þætti í hjálparkerfinu fyrir Microsoft Dynamics 365 for Finance and Operations. Það veitir yfirlit yfir hvernig á að tengja þá og yfirlit yfir hvernig á að stofna sérsniðna hjálp.

## <a name="help-architecture"></a>Högun Hjálpar

Eftirfarandi skýringarmynd sýnir hluta hjálparkerfisins í Finance and Operations. Hjálparkerfi innan vörunnar sækir greinar úr svæði Finance and Operations á https://docs.microsoft.com, auk verkefnaleiðbeininga sem eru geymdar í Viðskiptaferlavinnslu í Lifecycle Services (LCS).

> [!NOTE]
> Aðgerðirnar sem eru listaðar í skýringarmyndinni með stjörnu (\*) eru á vegvísnum, en eru ekki tiltækar enn.

[![Högun Hjálpar](./media/help-architecture.png)](./media/help-architecture.png)

## <a name="connecting-the-help-system"></a>Tenging við hjálparkerfi

> [!NOTE]
> Flipinn **Verkleiðbeiningar** er ekki í boði eins og stendur í Microsoft Dynamics 365 for Talent og Microsoft Dynamics 365 for Retail. Við erum að vinna í því að virkja þessa aðgerð í útgáfum í framtíðinni. Verkefnaleiðbeiningarnar í Hafist handa í Talent eru enn tiltækar og í þeim er farið yfir grunnvirkni. Leiðbeiningar fyrir aðstoð er einnig að finna á docs.microsoft.com site ([docs.microsoft.com/dynamics365/unified-operations](../../index.md)) fyrir bæði Retail og Talent.

Með skjámyndinni **Kerfisfæribreytur** tengja kerfisstjórar stykki í hjálparkerfinu fyrir innleiðingu.

[![Skjámynd kerfisfæribreyta með stillingum hjálparkerfis](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)

Á síðunni **Kerfisfæribreytur** skal fylgja þessum skrefum:

> [!IMPORTANT]
> Í fyrsta skipti er sem þú opnar flipann **Hjálp** verður þú að tengjast Lifecycle Services. Gætið þess að smella á tengil í miðri skjámyndinni, bíða eftir tengingu, loka svarglugga og smella á **Í lagi** til að komast á síðuna **Kerfisfæribreytur**.
>
> [![Tengjast við LCS](./media/connect-to-lcs-crop-1024x365.png "Tengjast við LCS")](./media/connect-to-lcs-crop.png)

1. Veljið Lifecycle Services verk til að tengjast.
2. Veljið BPM söfn (innan valins verks) til að sækja verkskráningu úr .

    - Fyrir Finance and Operations, fyrir Microsoft efni, skal velja nýjasta APQU Unified Library fyrir Finance and Operations.
    - Safn verður gefið út fyrir Retail í nánustu framtíð.
    - Þú þarft ekki að velja safn fyrir Talent — búið er að setja tengingu við rétt safn fyrir þig.

3. Velja birtingarröð BPM safna. Þetta ákvarðar í hvaða röð verkskráning úr í söfn birtast á **Hjálp** rúðunni.

Eftir að þessum skrefum hefur verið lokið, er hægt að opna rúðuna **Hjálp** og smella á flipann **Verkleiðbeiningar**. Nú sérðu verkefnaleiðbeiningar sem eiga við um síðuna sem þú ert á í Finance and Operations. Ef engin verkefnaleiðbeiningar finnast er hægt að færa inn lykilorð til þess að fínstilla leitina.

### <a name="showing-translated-task-guides"></a>Sýnir þýddar leiðbeiningar verkefninu

Þýddar verkefnaleiðbeiningar voru sendar í maí 2016 APQC Unified Library, og í safninu Hafist handa (getting started). Ef þú notar Finance and Operations og vilt sjá staðbundna verkefnahjálp skaltu ganga úr skugga um að þú sért tengd(ur) við safnið fyrir maí. Tungumálið sem leiðarvísir fyrir verk birtist í er stjórnað fyrir hvern notanda samkvæmt tungumálastillingar undir **Valkostir** &gt; **> Kjörstillingar**.

> [!NOTE]
> Þó að margar verkefnaleiðbeiningar hafi verið þýddar sýnir Finance and Operations-biðlarinn ekki þýdd heiti verkefnaleiðbeininga eins og er. Einnig, aðeins verkefnaleiðbeiningar sem voru gefnar út í febrúar 2016 eru í boði í þýðingu í maí safninu. Við munum gefa út uppfærða safn með fleiri þýðingum.
>
> - Ef verkefnaleiðbeiningar hefur verið þýdd, þegar þú opnar þessi verkefnaleiðbeiningar birtist allan texta þeirra í valið tungumál.
> - Ef verkefnaleiðbeiningar hefur ekki enn verið þýdd, þegar þú opnar það, bara nokkrar af textanum (Texti stjórnbúnaðar) munu birtast í valið tungumál.

## <a name="creating-custom-help"></a>Stofnun sérsniðinnar hjálpar

Hægt er að nota verkefnaleiðbeiningar til að stofna sérsniðna hjálp eða tengja vefsvæði við hjálparsvæðið.

### <a name="create-custom-help-with-task-guides"></a>Stofna sérsniðna hjálp með verkefnaleiðbeiningum

Hægt er að stofna sérsniðna hjálp fyrir Finance and Operations og fyrir Retail með því að stofna verkskráningar sem endurspegla innleiðingu þína og vista þær í LCS Business Process Library. Ekki er hægt að stofna sérsniðnar verkefnaleiðbeiningar fyrir Talent.

Fyrir samstarfsaðila, ef þú færir safn inn í fyrirtækissafn og hefur það með í lausn, verður það tiltækt viðskiptavinum þínum. Einnig er hægt gera afrit af APQC Unified global library og síðan opna síðan afritið, opna verkskráningar úr því, breyta þeim og vista skráningar með breytingunum. Frekari upplýsingar er að finna í efnisatriðinu [Hvernig stofna á verkskráningu sem nota á sem fylgigögn eða þjálfun](../../dev-itpro/user-interface/task-recorder.md).

### <a name="connect-a-custom-site"></a>Tengja sérsniðið svæði

Microsoft hefur útvegað hvítbók og sýnikóða sem lýsa því hvernig á að stofna og tengja sérsniðið svæði hjálpar við hjálparsvæðið. Frekari upplýsingar má finna á

- [Stofna sérsniðna hjálp fyrir Finance and Operations (hvítbók)](https://go.microsoft.com/fwlink/?linkid=2041185)
- [Sérsniðin hjálp GitHub-geymslu](https://github.com/microsoft/dynamics356f-o-custom-help)

## <a name="additional-resources"></a>Frekari upplýsingar

[Hjálparyfirlit](help-overview.md)

[yfirlit verkskráningar](../../dev-itpro/user-interface/task-recorder.md)

[Stofna verkskráning til að nota sem fylgiskjölum eða þjálfun](../../dev-itpro/user-interface/task-recorder-training-docs.md)
