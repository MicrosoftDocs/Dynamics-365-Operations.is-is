---
title: Prófun á sérsniðnu vottorði NF-e
description: Í þessu efnisatriði er að finna upplýsingar um hvernig á að virkja og nota sérsniðið vottorð NF-e.
author: gionoder
ms.date: 07/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 8144e16b127bdbe954ef44f52c5ac71689a2036e6085e9a4ccc8bb17f91ae9b8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755592"
---
# <a name="nf-e-custom-certificate-validation"></a>Staðfesting sérsniðins NF-e vottorðs

[!include [banner](../includes/banner.md)]

Sjálfgefið er slökkt á eiginleikanum **Tilgangur með sannvottun þjóns** úr vottorðinu sem er gefið út af brasilískum vottunaraðila rótarvottorðs og kveikja verður handvirkt á honum. Í sumum tilvikum getur sjálfvirk uppfærsla á vottorði skipt yfir þannig að þessi eiginleiki verði ekki lengur virkur. Ef þetta gerist hefur það áhrif á TLS-tenginguna og er þá ekki lengur hægt að treysta henni. Möguleikinn á að gefa út Brazilian electronic fiscal document model 55 (NF-e) í vinnsluumhverfum fyrir fylkin Minas Gerais (MG) og Paraná (PR).

Til að virkja endurbót fyrir **NF-e sérsniðna staðfestingu** skal fara **í Eiginleikastjórnun**. Þessi eiginleiki leyfir aðra lausn fyrir V5 og V10 staðfestingar vottorðs og leyfir áreiðanlega tengingu við vefþjónusturnar, sem er skilyrði fyrir örugga sendingu NF-e og móttöku heimildar frá SEFAZ.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
