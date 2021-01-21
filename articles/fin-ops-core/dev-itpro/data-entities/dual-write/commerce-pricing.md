---
title: Notið Dynamics 365 Commerce-verðlagningarkerfi ásamt Dynamics 365 Sales
description: Þetta efnisatriði lýsir því hvernig á að nota verðvél Microsoft Dynamics 365 Commerce til að stofna sölutilboð í Dynamics 365 Sales.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: shajain
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-11-03
ms.openlocfilehash: fad5c21d75db62b85efe803f1667dd3f9164a5fc
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594919"
---
# <a name="use-the-dynamics-365-commerce-pricing-engine-with-dynamics-365-sales"></a>Notið Dynamics 365 Commerce-verðlagningarkerfi ásamt Dynamics 365 Sales

[!include [banner](../../includes/banner.md)]

Þetta efnisatriði lýsir því hvernig á að nota verðvél Microsoft Dynamics 365 Commerce til að stofna sölutilboð í Dynamics 365 Sales.

Dynamics 365 Commerce -Verðlagningarvélin styður flestar aðstæður smásöluviðskipta til neytanda (B2C), svo sem verðlagningu á verslunarstigi, verðlagningar miðað við tengsl og vildarverð, blönduðum afslætti, magnafslætti og þröskuldarafslætti. Verðlagningarvélin notar flóknar reglur til að ákvarða besta verðið fyrir tiltekið tilboð eða pöntun.

Þegar þú notar [Tvöfalda skráningu](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview) eru þrír valmöguleikar fyrir verðþarfir. Hægt er að nota fasta verðlagningu sem kemur úr verðlistanum í Dynamics 365 Sales, verðlagningarvélinni í Dynamics 365 Supply Chain Management eða verðlagningarvélinni í Dynamics 365 Commerce. Á meðal þessara valkosta hentar Commerce-verðlagningarvélin best fyrir B2C-aðstæður.

## <a name="use-the-commerce-pricing-engine-in-sales"></a>Nota Commerce-vélverðlagningarvélina við sölu

> [!NOTE]
> Eins og stendur er einungis hægt að nota Commerce-verðlagningarvél fyrir tilboðsgerð við sölu. Samþætting sölupantana við verðlagningu í Commerce er ekki enn tiltæk.

Þegar notendur búa til tilboð við sölu afritar rammi tvöfaldrar skráningar upplýsingar um tilboðið í Commerce. Allar breytingar á fyrirliggjandi tilboðslínum eða öllum nýbættum tilboðslínum í Sales eru afritaðar í Commerce. Þegar notendur vilja nota Commerce-verðlagningarvél til að verðleggja tilboðið geta þeir valið **Verðtilboð** til að uppfæra verð tilboðsins miðað við Commerce-verðlagningarvélina. Verð eru þá sjálfkrafa uppfærð í bæði Sales og Commerce.

## <a name="prerequisites"></a>Forkröfur

- Áður en hægt er að nota Commerce-verðlagningarvél í sölu þarf að fylgja skrefunum í [Viðfang til sjóðstreymis við tvöfalda skráningu](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-prospect-to-cash/).
- Þú verður að slökkva á mati verðsamnings fyrir handvirkan innslátt með því að fylgja þessum skrefum:

    1. Í Commerce umhverfinu skal fara í **Viðskiptakröfur \> Uppsetning \> Færibreytur viðskiptakröfu**.
    1. Á flipanum **Verð**, á flpianum fyrir **Mat verðsamnings** skal hreinsa gátreitinn **Handvirk færsla** .

## <a name="additional-resources"></a>Frekari upplýsingar

[Viðfang til sjóðstreymis í tvískiptingu](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-prospect-to-cash/)