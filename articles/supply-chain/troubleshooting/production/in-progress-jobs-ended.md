---
title: Verkum í vinnslu lýkur þegar tilkynnt er um hlutamagn í síðasta verki
description: Þegar ég nota verkspjaldstækið til að skrá hlutamagn í síðustu vinnslu framleiðslupöntunar er öllum fyrri vinnslum sem eru með stöðuna Í vinnslu lokið.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 11511d4ac7524facdd0d647e9bc38fe09c282be1
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476702"
---
# <a name="previous-in-progress-jobs-are-ended-when-reporting-partial-quantity-on-last-job"></a>Fyrri verkum í vinnslu er lokið þegar tilkynnt er um hlutamagn í síðasta verki

## <a name="symptoms"></a>Einkenni

Þegar ég nota verkspjaldstækið til að skrá hlutamagn í síðustu vinnslu framleiðslupöntunar er öllum fyrri vinnslum á pöntuninni sem hafa stöðuna í vinnslu sjálfkrafa lokið.

## <a name="resolution"></a>Lausn

Þessi hegðun er samkvæmt hönnuninni. Á síðunni **Sjálfgildi framleiðslupöntunar** á flipanum **Bóka sem tilbúið** er valkostur sem kallast **Merkja lok ferlis**. Þegar þetta efnisatriði er stillt á *Já* er færslubók leiðarspjalds bókuð þegar starfskraftur notar verkspjaldstækið eða afgreiðslustöð verkspjalds til að skrá síðustu aðgerðina. Þessi færslubók merkir alla aðgerðir sem lokið og lýkur öllum framleiðsluverkum. Þegar valkosturinn **Merkja lok ferlis** er stilltur á *Já* virðir kerfið ekki stöðu vinnslu sem starfskrafturinn valdi þegar hann tilkynnti um síðustu aðgerðina. Kerfið segir ekki til um það hvort starfskrafturinn sé að tilkynna um heildarmagn eða hluta.
