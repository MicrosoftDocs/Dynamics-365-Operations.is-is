---
title: Prófun á sérsniðnu vottorði NF-e
description: Í þessu efnisatriði er að finna upplýsingar um hvernig á að virkja og nota sérsniðið vottorð NF-e.
author: gionoder
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: f13e8b8229bbd9e174e5bde7858a468048ba309b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990087"
---
# <a name="nf-e-custom-certificate-validation"></a>Prófun á sérsniðnu vottorði NF-e

[!include [banner](../includes/banner.md)]

Þegar kveikt er á sannprófunareiginleika fyrir sérsniðið vottorð NF-e, heimilar sérsniðin sannprófun tengingu við vefþjónustur. Þessi tenging er nauðsynleg til að flytja NF-e og taka á móti heimild frá SEFAZ.

Eiginleikinn **Tilgangur með sannvottun þjóns** úr vottorðinu V5 er gefinn út af brasilískum vottunaraðila rótarvottorðs. Sjálfgefið er að slökkt sé á þessum eiginleika og nauðsynlegt er að virkja hann handvirkt. Í sumum tilvikum getur sjálfvirk uppfærsla á vottorði skipt yfir þannig að þessi eiginleiki verði ekki lengur virkur. Ef þetta gerist hefur það áhrif á TLS-tenginguna og er þá ekki lengur hægt að treysta henni. Möguleikinn á að gefa út NF-e í vinnsluumhverfum fyrir fylkin Minas Gerais (MG) og Paraná (PR) verður einnig fyrir áhrifum.

Þessi uppfærsla opnar á aðra lausn fyrir prófun vottorðs, sem þýðir að það er mögulegt að koma á öruggum samskiptum.


