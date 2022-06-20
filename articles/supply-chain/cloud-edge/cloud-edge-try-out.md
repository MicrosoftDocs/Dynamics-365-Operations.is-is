---
title: Prófaðu kvörðunareiningar í dreifðri blandaðri grannfræði
description: Þessi grein veitir upplýsingar um hvernig á að prófa skýja- og brúnkvarðaeiningarnar fyrir framleiðslu- og vöruhúsastjórnunarálag.
author: perlynne
ms.date: 05/02/2022
ms.topic: article
ms.search.form: ScaleUnitWorkloadsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-03-03
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 5645955109e7a942e617b3b90a27065c2a8fe4a3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893585"
---
# <a name="try-out-scale-units-in-a-distributed-hybrid-topology"></a>Prófaðu kvörðunareiningar í dreifðri blandaðri grannfræði

[!include [banner](../includes/banner.md)]

Ferlið við að prófa dreifða blendinguna er einfalt. Á fyrsta stigi ættir þú að sannreyna sérstillingar til að tryggja að þær virki í dreifðu svæðisfræðinni. Þú hefur tvo valkosti.

## <a name="option-1-evaluate-customizations-in-development-environments"></a>Valkostur 1: Metið sérstillingar í þróunarumhverfi

Áður en þú byrjar að setja inn sandkassaumhverfið þitt, mælum við með því að þú skoðar mælieiningar í þróunaruppsetningu, eins og eins kassa umhverfi (einnig þekkt sem tier-1 umhverfi), svo að þú getir sannreynt ferla, sérstillingar og lausnir. Á þessu stigi verða gögn og sérstillingar sett inn í heildræn umhverfi. Þú getur keyrt á einu umhverfi, sem getur tekið hlutverk bæði fyrirtækismiðstöðvarinnar og mælikvarðaeiningarinnar. Að öðrum kosti geturðu haft tvö þróunarumhverfi, þar af annað sem tekur hlutverk miðstöðvarinnar og hitt tekur hlutverk mælieininga. Þessi uppsetning býður upp á bestu leiðina til að bera kennsl á og lagfæra vandamál. Nýjasta [Forskoða smíði](../../fin-ops-core/fin-ops/get-started/one-version.md#how-can-i-get-early-access-to-non-released-platform-updates) er einnig hægt að nota til að ljúka þessu stigi.

Þú ættir að nota [mælitæki fyrir dreifingu eininga fyrir þróunarumhverfi með einum kassa](https://github.com/microsoft/SCMScaleUnitDevTools) að setja upp og viðhalda umhverfinu. Þessi verkfæri gera þér kleift að stilla miðstöð og mælieiningar í einu eða tveimur eins-kassa umhverfi. Verkfærin eru bæði sem tvíundarútgáfa og í frumkóða á GitHub. Kynntu þér verkefnið wiki, sem inniheldur a [Skref fyrir skref notkunarleiðbeiningar](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide) sem lýsir því hvernig á að nota tækin. Ef þú ert [að dreifa brúnum mælieiningum á sérsniðnum vélbúnaði með því að nota staðbundin viðskiptagögn (LBD)](cloud-edge-edge-scale-units-lbd.md), þú verður að fylgja öðru ferli.

## <a name="option-2-acquire-add-ins-and-deploy-in-your-sandbox-environments"></a>Valkostur 2: Fáðu þér viðbætur og settu í sandkassaumhverfið þitt

Til að prófa hina dreifðu blendingu svæðisfræði verður þú að hafa tvö sandkassaumhverfi (tier 2), annað þeirra hefur gögnin þín (fyrirtækjamiðstöð) og hitt er fyrir mælikvarðaeininguna og hefur "tóm gögn."

Þú verður að eignast viðbætur fyrir að minnsta kosti eina skýja- eða brúnkvarðaeiningu. Samsvarandi verkefna- og umhverfistímar verða síðan veittir inn [Microsoft Dynamics Lífsferilsþjónusta (LCS)](https://lcs.dynamics.com/), svo að hægt sé að beita kvarðaeiningaumhverfinu með því að nota [Gátt Scal Unit Manager](https://aka.ms/SCMSUM).

Hafðu samband við þjónustudeild Microsoft til að biðja um að sandkassaumhverfið verði virkt.

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
