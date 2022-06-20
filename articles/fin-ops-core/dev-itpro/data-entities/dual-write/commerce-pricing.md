---
title: Notið Dynamics 365 Commerce-verðlagningarkerfi ásamt Dynamics 365 Sales
description: Þessi grein lýsir því hvernig á að nota Microsoft Dynamics 365 Commerce verðlagningarvél til að búa til sölutilboð í Dynamics 365 Sales.
author: ShalabhjainMSFT
ms.date: 11/19/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: global
ms.author: shajain
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 11a164ec15c8b7a69172a153b961011a8b324712
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881395"
---
# <a name="use-the-dynamics-365-commerce-pricing-engine-with-dynamics-365-sales"></a>Notið Dynamics 365 Commerce-verðlagningarkerfi ásamt Dynamics 365 Sales

[!include [banner](../../includes/banner.md)]

Þessi grein lýsir því hvernig á að nota Microsoft Dynamics 365 Commerce verðlagningarvél til að búa til sölutilboð í Dynamics 365 Sales.

Dynamics 365 Commerce -Verðlagningarvélin styður flestar aðstæður smásöluviðskipta til neytanda (B2C), svo sem verðlagningu á verslunarstigi, verðlagningar miðað við tengsl og vildarverð, blönduðum afslætti, magnafslætti og þröskuldarafslætti. Verðlagningarvélin notar flóknar reglur til að ákvarða besta verðið fyrir tiltekið tilboð eða pöntun.

Þegar þú notar [Tvöfalda skráningu](./dual-write-overview.md) eru þrír valmöguleikar fyrir verðþarfir. Hægt er að nota fasta verðlagningu sem kemur úr verðlistanum í Dynamics 365 Sales, verðlagningarvélinni í Dynamics 365 Supply Chain Management eða verðlagningarvélinni í Dynamics 365 Commerce. Á meðal þessara valkosta hentar Commerce-verðlagningarvélin best fyrir B2C-aðstæður.

## <a name="use-the-commerce-pricing-engine-in-sales"></a>Nota Commerce-vélverðlagningarvélina við sölu

> [!NOTE]
> Eins og stendur er einungis hægt að nota Commerce-verðlagningarvél fyrir tilboðsgerð við sölu. Samþætting sölupantana við verðlagningu í Commerce er ekki enn tiltæk.

Þegar notendur búa til tilboð við sölu afritar rammi tvöfaldrar skráningar upplýsingar um tilboðið í Commerce. Allar breytingar á fyrirliggjandi tilboðslínum eða öllum nýbættum tilboðslínum í Sales eru afritaðar í Commerce. Þegar notendur vilja nota Commerce-verðlagningarvél til að verðleggja tilboðið geta þeir valið **Verðtilboð** til að uppfæra verð tilboðsins miðað við Commerce-verðlagningarvélina. Verð eru þá sjálfkrafa uppfærð í bæði Sales og Commerce.

## <a name="prerequisites"></a>Forkröfur

- Áður en hægt er að nota Commerce-verðlagningarvél í sölu þarf að fylgja skrefunum í [Viðfang til sjóðstreymis við tvöfalda skráningu](./dual-write-prospect-to-cash.md).
- Þú verður að slökkva á mati verðsamnings fyrir handvirkan innslátt með því að fylgja þessum skrefum:

    1. Í Commerce umhverfinu skal fara í **Viðskiptakröfur \> Uppsetning \> Færibreytur viðskiptakröfu**.
    1. Á flipanum **Verð**, á flpianum fyrir **Mat verðsamnings** skal hreinsa gátreitinn **Handvirk færsla** .

## <a name="additional-resources"></a>Frekari upplýsingar

[Viðfang til sjóðstreymis í tvískiptingu](./dual-write-prospect-to-cash.md)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]