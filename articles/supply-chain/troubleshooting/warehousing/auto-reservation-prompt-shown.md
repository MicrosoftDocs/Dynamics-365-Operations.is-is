---
title: Kvaðning um sjálfvirka frátekningu er sýnd með tiltækum birgðum
description: Þegar þú notar vöru í vöruhúsi sem hefur ekki virkjað vöruhúsaferli er kvaðning um sjálfvirka frátekningu sýnd. Tilgreindu allar víddir hér að ofan sem „Staðsetning“.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a15502ce8c5bc61d37cedd746985176408a2f362
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476697"
---
# <a name="auto-reservation-prompt-for-batch-number-is-shown-even-with-available-inventory"></a>Kvaðning sjálfvirkrar frátekningar fyrir rununúmer er sýnd jafnvel með tiltækum birgðum

## <a name="symptoms"></a>Einkenni

Þegar notuð er vara sem er með *runa fyrir ofan* frátekningastigveldi í vöruhúsi sem hefur ekki virkjað vöruhúsaferla og sjálfvirk frátekning er virkjuð, birtist kvaðning sjálfvirkrar frátekningar fyrir rununúmer þótt aðeins ein runa er tiltæk fyrir tiltekt.

Hins vegar þegar sama varan er notuð í vöruhúsi þar sem vöruhúsaferli eru virkjuð, er kvaðning sjálfvirkrar frátekningar ekki sýnd.

## <a name="resolution"></a>Lausn

Ef frátekningastigveldi er skilgreint sem *runa fyrir ofan* eða *raðnúmer fyrir ofan* verður alltaf að tilgreina vídd sem vísað er í (**Rununúmer** eða **Raðnúmer**) í eftirspurnarpöntunum. Vöruhúsaferli gætu lokið upplýsingunum ef ein runa eða raðnúmer er í boði. En þar sem vöruhúsið er ekki virkjað fyrir vöruhúsaferli, verður notandinn alltaf að tilgreina allar víddir fyrir ofan **Staðsetningu**.
