---
title: Staðfesting sérsniðins NF-e vottorðs
description: Í þessari grein er að finna upplýsingar um hvernig á að virkja og nota sérsniðið vottorð NF-e.
author: gionoder
ms.date: 07/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.custom: 97423
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: f78fdbd133aecaf9dbf8abe0006abd6deb1b1b15
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288545"
---
# <a name="nf-e-custom-certificate-validation"></a>Staðfesting sérsniðins NF-e vottorðs

[!include [banner](../includes/banner.md)]

Sjálfgefið er slökkt á eiginleikanum **Tilgangur með sannvottun þjóns** úr vottorðinu sem er gefið út af brasilískum vottunaraðila rótarvottorðs og kveikja verður handvirkt á honum. Í sumum tilvikum getur sjálfvirk uppfærsla á vottorði skipt yfir þannig að þessi eiginleiki verði ekki lengur virkur. Ef þetta gerist hefur það áhrif á TLS-tenginguna og er þá ekki lengur hægt að treysta henni. Möguleikinn á að gefa út Brazilian electronic fiscal document model 55 (NF-e) í vinnsluumhverfum fyrir fylkin Minas Gerais (MG) og Paraná (PR).

Til að virkja endurbót fyrir **NF-e sérsniðna staðfestingu** skal fara **í Eiginleikastjórnun**. Þessi eiginleiki leyfir aðra lausn fyrir V5 og V10 staðfestingar vottorðs og leyfir áreiðanlega tengingu við vefþjónusturnar, sem er skilyrði fyrir örugga sendingu NF-e og móttöku heimildar frá SEFAZ.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
