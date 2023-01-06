---
title: Virkja gengisgerð fyrir staðgreiðsluskatt á heimsvísu og uppsetningu fyrir tegund dagsetningar
description: Þessi grein útskýrir hvernig á að virkja gengisgerð fyrir staðgreiðsluskatt á heimsvísu og uppsetningu fyrir tegund dagsetningar.
author: kailiang
ms.date: 08/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 9db9cf41381b8b4de7dffe1c755a7df805a003ea
ms.sourcegitcommit: adadbc6e355e2ad68a1f6af26a1be1f89dc8eec6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/22/2022
ms.locfileid: "9573225"
---
# <a name="enable-the-global-withholding-tax-currency-exchange-rate-type-and-date-type-setup"></a>Virkja gengisgerð fyrir staðgreiðsluskatt á heimsvísu og uppsetningu fyrir tegund dagsetningar

[!include[banner](../includes/banner.md)]

Þessi grein útskýrir hvernig á að virkja gengisgerð fyrir staðgreiðsluskatt á heimsvísu og uppsetningu fyrir tegund dagsetningar. Nú getur þú valið tiltekna gerð gengis og gerð gengisútreiknings fyrir gjaldmiðil staðgreiðsluskatts. Þetta val ákvarðar gengi erlends gjaldeyris sem notað er til að reikna staðgreiðsluskattinn, í gjaldmiðli staðgreiðsluskattsins, í greiðslufærslunum.

Þessi aðgerð er fáanleg í Microsoft Dynamics 365 Finance útgáfum 10.0.29 og nýrri.

1. Farið í **Skattur** \> **Uppsetning** \> **Færibreytur** \> **Færibreytur fjárhags**.
2. Á flipanum **Staðgreiðsluskattur** skal stilla valkstinn **Virkja gjaldmiðil ítarlegs staðgreiðsluskatts** á **Já**.
3. Veljið **Gerð gengis** fyrir gjaldmiðil til að halda eftir skatti.
4. Í reitnum **Gerð útreikningsdagsetningar** velja tegund reikningsdags sem ákvarðar gengi staðgreiðsluskatts:

    - **Greiðsludagur** – Ákvarðið gengi miðað við bókunardag greiðsludagbókar.
    - **Reikningsdagsetning** – Ákvarðið gengi miðað við reikningsdag greiðsludagbókar. Ef reikningsdagur fylgiskjals er auður verður bókunardagsetning reiknings notuð. 
    - **Skjaladagsetning**  – Ákvarðið gengi miðað við skjaladagsetningu greiðsludagbókar. Ef skjaladagur fylgiskjals er auður verður greiðsludagur notaður.

5. Veldu **Vista**.

Ef gjaldmiðill færslunnar er annar en gjaldmiðill staðgreiðsluskattsins sem skilgreindur er í staðgreiðsluskattskóðanum verður upphæð staðgreiðsluskattsins reiknuð af gjaldmiðli færslunnar, byggt á fyrri stillingum, og verður skráð í útsendum staðgreiðsluskattsfærslum.
