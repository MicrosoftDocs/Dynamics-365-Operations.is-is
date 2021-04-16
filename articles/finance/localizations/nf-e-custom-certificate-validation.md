---
title: Prófun á sérsniðnu vottorði NF-e
description: Í þessu efnisatriði er að finna upplýsingar um hvernig á að virkja og nota sérsniðið vottorð NF-e.
author: gionoder
ms.date: 10/06/2020
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
ms.openlocfilehash: 895513f51798a797ebf59f8a5be4f5cde006726d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813969"
---
# <a name="nf-e-custom-certificate-validation"></a>Prófun á sérsniðnu vottorði NF-e

[!include [banner](../includes/banner.md)]

Þegar kveikt er á sannprófunareiginleika fyrir sérsniðið vottorð NF-e, heimilar sérsniðin sannprófun tengingu við vefþjónustur. Þessi tenging er nauðsynleg til að flytja NF-e og taka á móti heimild frá SEFAZ.

Eiginleikinn **Tilgangur með sannvottun þjóns** úr vottorðinu V5 er gefinn út af brasilískum vottunaraðila rótarvottorðs. Sjálfgefið er að slökkt sé á þessum eiginleika og nauðsynlegt er að virkja hann handvirkt. Í sumum tilvikum getur sjálfvirk uppfærsla á vottorði skipt yfir þannig að þessi eiginleiki verði ekki lengur virkur. Ef þetta gerist hefur það áhrif á TLS-tenginguna og er þá ekki lengur hægt að treysta henni. Möguleikinn á að gefa út NF-e í vinnsluumhverfum fyrir fylkin Minas Gerais (MG) og Paraná (PR) verður einnig fyrir áhrifum.

Þessi uppfærsla opnar á aðra lausn fyrir prófun vottorðs, sem þýðir að það er mögulegt að koma á öruggum samskiptum.




[!INCLUDE[footer-include](../../includes/footer-banner.md)]