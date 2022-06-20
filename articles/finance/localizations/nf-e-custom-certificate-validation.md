---
title: Staðfesting sérsniðins NF-e vottorðs
description: Þessi grein veitir upplýsingar um að virkja og nota sérsniðna NF-e vottorðið.
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
ms.openlocfilehash: 3d69aa9d6d0ce33fbed9ba1c7a7af441e14d0d07
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875905"
---
# <a name="nf-e-custom-certificate-validation"></a>Staðfesting sérsniðins NF-e vottorðs

[!include [banner](../includes/banner.md)]

Sjálfgefið er slökkt á eiginleikanum **Tilgangur með sannvottun þjóns** úr vottorðinu sem er gefið út af brasilískum vottunaraðila rótarvottorðs og kveikja verður handvirkt á honum. Í sumum tilvikum getur sjálfvirk uppfærsla á vottorði skipt yfir þannig að þessi eiginleiki verði ekki lengur virkur. Ef þetta gerist hefur það áhrif á TLS-tenginguna og er þá ekki lengur hægt að treysta henni. Möguleikinn á að gefa út Brazilian electronic fiscal document model 55 (NF-e) í vinnsluumhverfum fyrir fylkin Minas Gerais (MG) og Paraná (PR).

Til að virkja endurbót fyrir **NF-e sérsniðna staðfestingu** skal fara **í Eiginleikastjórnun**. Þessi eiginleiki leyfir aðra lausn fyrir V5 og V10 staðfestingar vottorðs og leyfir áreiðanlega tengingu við vefþjónusturnar, sem er skilyrði fyrir örugga sendingu NF-e og móttöku heimildar frá SEFAZ.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
