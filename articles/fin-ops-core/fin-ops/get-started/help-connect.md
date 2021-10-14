---
title: Skilgreining hjálparupplifunar fyrir Finance and Operations-forrit
description: Þetta efnisatriði lýsir þáttum hjálparkerfisins fyrir sum Microsoft Dynamics 365-forrit.
author: margoc
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3a6c37822e84ba08fa0720ed2b3912cbec1448e3
ms.sourcegitcommit: e40a9fac5bac9f57a6dcfe73a1f21856eab9b6a9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/02/2021
ms.locfileid: "7594858"
---
# <a name="configure-the-help-experience-for-finance-and-operations-apps"></a>Skilgreining hjálparupplifunar fyrir Finance and Operations-forrit

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er að finna yfirlit yfir þætti hjálparkerfisins fyrir Finance and Operations-forrit á borð við Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce og Dynamics 365 Human Resources. Efnisatriðið útskýrir einnig hvernig á að tengja þessa þætti og býður upp á samantekt yfir ferlið til að búa til sérstillta hjálp.

## <a name="help-architecture"></a>Högun Hjálpar

Finance and Operations-forrit innihalda almenn yfirlit og önnur efnisatriði sem eru birt á vefsvæðinu [Fylgiskjöl Microsoft Dynamics 365](/dynamics365/). Þetta efni er svo hægt að nálgast á **hjálparsvæði** vörunnar. Eftirfarandi skýringarmynd sýnir hluta hjálparkerfisins.

[![Högun Hjálpar.](./media/help-architecture.png)](./media/help-architecture.png)

Hjálparkerfi vörunnar sækir greinar á docs.microsoft.com og önnur tengd vefsvæði. Það sækir einnig verkleiðbeiningar sem eru vistaðar í viðskiptaferlavinnslunni (BPM) í Microsoft Dynamics Lifecycle Services (LCS).

## <a name="adding-task-guides"></a>Verkefnaleiðbeiningum bætt við

> [!NOTE]
> Flipinn **Verkefnaleiðbeiningar** er ekki til staðar í „Human Resources“ eða „Commerce“. <!--We are currently working to enable this functionality in a future release.--> Hins vegar eru verkefnaleiðbeiningarnar „Hafist handa“ í „Human Resources“ til staðar og þar er að finna upplýsingar um grunnvirknina. Hjálparleiðbeiningar eru í boði á vefsvæðinu [Fylgiskjöl Microsoft Dynamics 365](/dynamics365/) fyrir bæði „Human Resources“ og „Commerce“.

Á síðunni **Kerfisfæribreytur** geta kerfisstjórar skilgreint aðgang að viðeigandi verkleiðbeiningasöfnum fyrir innleiðingu.

> [!NOTE]
> - Til að grunnstilla hjálpina þarf notandi að skrá sig inn með því að nota lykil hjá sama leigjanda og leigjandanum þar sem forritið er virkjað.
> - Ekki er hægt að tengja LCS-safn úr tilviki forritsins sem er keyrt á staðbundnu sýndardrifi (VHD).

[![Skjámynd kerfisfæribreyta með stillingum hjálparkerfis.](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)

Til að skilgreina verkefnaleiðbeiningar fyrir lausn skal fylgja þessum skrefum á síðunni **Kerfisfæribreytur**.

> [!IMPORTANT]
> Í fyrsta skipti er sem þú opnar flipann **Hjálp** verður þú að tengjast Lifecycle Services. Gætið þess að velja tengil í miðri skjámyndinni, bíða eftir tengingu, loka svarglugga og velja **Í lagi** til að komast á síðuna **Kerfisfæribreytur**.
>
> [![Tengjast við LCS](./media/connect-to-lcs-crop-1024x365.png "Tengjast við LCS.")](./media/connect-to-lcs-crop.png)

1. Veljið Lifecycle Services verk til að tengjast.
2. Veljið BPM söfn (innan valins verks) til að sækja verkskráningu úr .
3. Velja birtingarröð BPM safna. Birtingarröðin ákvarðar í hvaða röð verkskráningar úr söfnunum birtast á svæðinu **Hjálp**.

Eftir að þessum skrefum hefur verið lokið, er hægt að opna rúðuna **Hjálp** og velja flipann **Verkleiðbeiningar**. Nú sérðu verkefnaleiðbeiningar sem eiga við um síðuna sem þú ert á í Finance and Operations forritum. Ef engin verkefnaleiðbeiningar finnast er hægt að færa inn lykilorð til þess að fínstilla leitina.

### <a name="showing-translated-task-guides"></a>Sýnir þýddar leiðbeiningar verkefninu

Þýddar verkefnaleiðbeiningar voru gefnar út í maíútgáfu APQC Unified Library 2016, og í safninu „Hafist handa“. Til að skoða staðfærðar verkleiðbeiningar hjálpar þarf að ganga úr skugga um að Dynamics 365-lausnin sé tengd við útgáfu safnsins frá maí 2016. Notendur geta breytt tungumálinu sem verkefnaleiðbeiningar birtast á með því að breyta tungumálastillingum undir **Valkostir** &gt; **Kjörstillingar**.

> [!NOTE]
> Þrátt fyrir að margar verkefnaleiðbeiningar hafi verið þýddar sýnir biðlarinn ekki heiti þýddra verkleiðbeininga, eins og er. Í maíútgáfu safnsins 2016 verða auk þess þýðingar eingöngu í boði fyrir verkleiðbeiningar sem gefnar voru út í febrúar 2016. Microsoft mun gefa út uppfært safn sem inniheldur fleiri þýðingar.
>
> - Ef verkefnaleiðbeiningar hefur verið þýdd, þegar þú opnar þessi verkefnaleiðbeiningar birtist allan texta þeirra í valið tungumál.
> - Ef verkefnaleiðbeiningar hefur ekki enn verið þýdd, þegar þú opnar það, bara nokkrar af textanum (Texti stjórnbúnaðar) munu birtast í valið tungumál.

## <a name="adding-custom-help"></a>Sérsniðinni hjálp bætt við

Hægt er að nota verkefnaleiðbeiningar til að stofna sérsniðna hjálp eða tengja vefsvæði við **hjálparsvæðið**.

### <a name="create-custom-help-by-using-task-guides"></a>Stofna sérsniðna hjálp með því að nota verkefnaleiðbeiningar

Hægt er að stofna sérsniðna hjálp fyrir studd forrit með því að stofna verkskráningar sem endurspegla innleiðingu og vista þær í viðskiptaferlissafni í LCS. Ekki er hægt að búa til sérsniðnar verkefnaleiðbeiningar fyrir „Human Resources“.

Fyrir samstarfsaðila, ef þú færir safn inn í fyrirtækissafn og hefur það með í lausn, verður það tiltækt viðskiptavinum þínum. Einnig er hægt að taka afrit af APQC Unified Library og opna síðan verkskráningarnar í afritinu, breyta þeim og vista breytingarnar. Nánari upplýsingar er að finna [Tilföng verkskráningar](../../dev-itpro/user-interface/task-recorder.md).

### <a name="connect-a-custom-help-site"></a>Tengja sérstillt hjálparsvæði

Finance and Operations-forrit eru sjaldan notuð eins og þau eru afhent. Þess í stað er lausnin sérsniðin og útvíkkuð til að passa við þarfir fyrirtækisins. Einnig er hægt að sérsníða og víkka út hjálparupplifunina. Til dæmis er hægt að bæta við sérsniðinni hjálp á **hjálparsvæðið**.

Microsoft hefur gefið út verkfærasett til að auðvelda uppsetningu og teningu sérsniðinnar hjálpar á **hjálparsvæðinu**. Frekari upplýsingar um hvernig hægt er að setja upp sérsniðna hjálparlausn sem er tengd við **hjálparsvæðið** er finna í [Sérsniðið hjálparyfirlit](../../dev-itpro/help/custom-help-overview.md).

Ef óskað er eftir samstarfi við Microsoft í tengslum við verkfæri og ferli til að sérsnið hjálpar skal fylla út eyðublaðið á [https://aka.ms/customhelpfeedback](https://aka.ms/customhelpfeedback).

## <a name="see-also"></a>Sjá einnig

[Hjálparkerfi](help-overview.md)  
[Sérsniðið hjálparyfirlit](../../dev-itpro/help/custom-help-overview.md)  
[Tilföng verkskráningar](../../dev-itpro/user-interface/task-recorder.md)  
[Búa til fylgiskjöl eða þjálfun með verkskráningu](../../dev-itpro/user-interface/task-recorder-training-docs.md)  
[Sérsniðin hjálp GitHub-geymslu](https://github.com/microsoft/dynamics356f-o-custom-help)  


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
