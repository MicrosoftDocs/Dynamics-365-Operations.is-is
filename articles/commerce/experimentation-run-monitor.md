---
title: Keyra og fylgjast með tilraun
description: Þessi grein lýsir því hvernig á að keyra og fylgjast með tilraun í þjónustu þriðja aðila. Þar er einnig lýst því hvernig á að gera breytingar á afbrigðum eftir að tilraunin hófst.
author: sushma-rao
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: c9f62c97b46fa00791de52b2804dad5edde7f625
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909584"
---
# <a name="run-and-monitor-an-experiment"></a>Keyra og fylgjast með tilraun

Þessi grein lýsir því hvernig á að keyra og fylgjast með tilrauninni þinni í forriti frá þriðja aðila og breyta tilbrigðum ef þörf krefur. Áður en þú klárar skrefin í þessari grein þarftu fyrst að gera það [birta](experimentation-preview-publish.md) tilraun þína í verslun. 

Eftirfarandi skýringarmynd sýnir öll skrefin sem taka þátt í uppsetningu og vinnslu á tilraun á vefsvæði rafrænna viðskipta í Dynamics 365 Commerce. Fjallað er um fleiri skref í aðskildum greinum.

[ ![Tilraunaferli notanda - Keyra og fylgjast með.](./media/experimentation_run_monitor.svg) ](./media/experimentation_run_monitor.svg#lightbox)

Þegar afbrigðin hafa verið birt þarf að fara í gegnum öll skrefin sem þú þarft að gera í Commerce til að keyra tilraunina þína. Næsta skref er að ákvarða hvaða afbrigði eru sýnd hverjum notanda þegar þeir óska eftir síðu. Þjónusta þriðja aðila tekur þá ákvörðun en fyrst þarf að virkja tilraunina innan þjónustunnar. Þar sem skrefin til að virkja tilraun eru breytileg frá þjónustu til þjónustu þarf að fylgja leiðbeiningunum sem eru innifaldar í þjónustunni eða veitunni. Ef tilraunin er ekki virkjuð munu notendur aðeins sjá sjálfgefna útgáfu síðunnar (engin afbrigði verða birt).

Þú þarft að halda tilrauninni nógu lengi í gangi til að safna gögnum fyrir tölfræðilega gildar niðurstöður. Notið þjónustu þriðja aðila til að fylgjast með gögnum sem tengjast tilraunum og greiningu á meðan tilraunin er í gangi.

## <a name="adjust-your-variations"></a>Leiðrétta afbrigði
Ef þú þarft að breyta afbrigðunum af einhverjum ástæðum skaltu fylgja skrefunum hér að neðan.

> [!IMPORTANT]
> Ef gerðar eru breytingar á virkri tilraun í Commerce eða þjónustu þriðja aðila getur það haft umtalsverð áhrif á niðurstöðurnar. Íhugið að láta tilraunina hafa sinn gang og búa síðan til nýja tilraun fyrir stórar breytingar.

1. Í vefsmið Commerce skal velja **Tilraunir** á vinstra yfirlitssvæðinu og síðan velja tilraunina. 
1. Veljið afbrigðið sem á að uppfæra úr fellivalmyndinni.
1. Gerið nauðsynlegar breytingar, forskoðið og birtið síðan afbrigðin. Frekari upplýsingar er að finna í [Forskoða og birta tilraun](experimentation-preview-publish.md).
1. Farið í þjónustu þriðja aðila til að gera breytingar á uppsetningu tilraunar.
    
## <a name="previous-step"></a>Fyrra skref
[Forskoða og birta tilraun](experimentation-preview-publish.md)

## <a name="next-step"></a>Næsta skref
[Kynna afbrigði og ljúka tilraun](experimentation-review-complete.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]