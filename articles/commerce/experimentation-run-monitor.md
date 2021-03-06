---
title: Keyra og fylgjast með tilraun
description: Þetta efnisatriði lýsir því hvernig á að keyra og fylgjast með tilraun í þjónustu þriðja aðila. Þar er einnig lýst því hvernig á að gera breytingar á afbrigðum eftir að tilraunin hófst.
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
ms.openlocfilehash: 4afc19ed103f204fec61ab20b88f767ad5f05b38
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792536"
---
# <a name="run-and-monitor-an-experiment"></a>Keyra og fylgjast með tilraun

Þetta efnisatriði lýsir því hvernig á að keyra og fylgjast með tilraun í forriti þriðja aðila og breyta afbrigðum eftir því sem þörf krefur. Áður en þú klárar skrefin í þessu efnisatriði þarftu fyrst að [birta](experimentation-preview-publish.md) tilraunina þína í Commerce. 

Eftirfarandi skýringarmynd sýnir öll skrefin sem taka þátt í uppsetningu og vinnslu á tilraun á vefsvæði rafrænna viðskipta í Dynamics 365 Commerce. Önnur skref eru afgreidd í aðskildum efnisatriðum.

[ ![Ferli tilraunanotanda - Keyra og fylgjast með](./media/experimentation_run_monitor.svg) ](./media/experimentation_run_monitor.svg#lightbox)

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