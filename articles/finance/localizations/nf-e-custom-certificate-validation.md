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
# <a name="nf-e-custom-certificate-validation"></a><span data-ttu-id="07ef8-103">Prófun á sérsniðnu vottorði NF-e</span><span class="sxs-lookup"><span data-stu-id="07ef8-103">NF-e custom certificate validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="07ef8-104">Þegar kveikt er á sannprófunareiginleika fyrir sérsniðið vottorð NF-e, heimilar sérsniðin sannprófun tengingu við vefþjónustur.</span><span class="sxs-lookup"><span data-stu-id="07ef8-104">When you turn the NF-e custom certificate verification feature, custom validation allows a connection with the web services.</span></span> <span data-ttu-id="07ef8-105">Þessi tenging er nauðsynleg til að flytja NF-e og taka á móti heimild frá SEFAZ.</span><span class="sxs-lookup"><span data-stu-id="07ef8-105">This connection is required to transmit NF-e and receive authorization from SEFAZ.</span></span>

<span data-ttu-id="07ef8-106">Eiginleikinn **Tilgangur með sannvottun þjóns** úr vottorðinu V5 er gefinn út af brasilískum vottunaraðila rótarvottorðs.</span><span class="sxs-lookup"><span data-stu-id="07ef8-106">The **Server authentication purpose** property from the certificate V5 is issued by the Brazilian Root Certificate Authority.</span></span> <span data-ttu-id="07ef8-107">Sjálfgefið er að slökkt sé á þessum eiginleika og nauðsynlegt er að virkja hann handvirkt.</span><span class="sxs-lookup"><span data-stu-id="07ef8-107">This property is turned off by default and must be manually enabled.</span></span> <span data-ttu-id="07ef8-108">Í sumum tilvikum getur sjálfvirk uppfærsla á vottorði skipt yfir þannig að þessi eiginleiki verði ekki lengur virkur.</span><span class="sxs-lookup"><span data-stu-id="07ef8-108">In some circumstances, the automatic certificate update can switch this property to no longer be enabled.</span></span> <span data-ttu-id="07ef8-109">Ef þetta gerist hefur það áhrif á TLS-tenginguna og er þá ekki lengur hægt að treysta henni.</span><span class="sxs-lookup"><span data-stu-id="07ef8-109">If this happens, the TLS connection is affected and is no longer trusted.</span></span> <span data-ttu-id="07ef8-110">Möguleikinn á að gefa út NF-e í vinnsluumhverfum fyrir fylkin Minas Gerais (MG) og Paraná (PR) verður einnig fyrir áhrifum.</span><span class="sxs-lookup"><span data-stu-id="07ef8-110">The ability to issue NF-e on production environments for states of Minas Gerais (MG) and Paraná (PR) states is also impacted.</span></span>

<span data-ttu-id="07ef8-111">Þessi uppfærsla opnar á aðra lausn fyrir prófun vottorðs, sem þýðir að það er mögulegt að koma á öruggum samskiptum.</span><span class="sxs-lookup"><span data-stu-id="07ef8-111">This update allows for an alternative solution for certificate validation, which means that it’s possible to establish a secure communication.</span></span>


