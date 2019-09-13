---
title: Framkvæmdapöntun fyrir fyrstu samstillingu Finance and Operations og Common Data Service
description: Þetta efni tilgreinir röð samstillingarinnar sem þú verður að fylgja til að búa til upphafsgögnin.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 1473c3bad55734d5f83ee3e4c1654921b872f3bb
ms.sourcegitcommit: 3f05ede8b8acdf0550240a83a013e093b4ad043d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/13/2019
ms.locfileid: "1873129"
---
# <a name="execution-order-for-initial-synchronization-of-finance-and-operations-and-common-data-service"></a>Framkvæmdapöntun fyrir fyrstu samstillingu Finance and Operations og Common Data Service

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Áður en þú notar gagnasamþættingu verður þú að búa til fyrstu gögn sem krafist er fyrir viðskiptavini, lánardrottna og tengiliði. Til dæmis viltu búa til nýtjan lið **Lánardrottnahóp** og stillir gildið **Greiðsluskilmála** á **Net30**. Í þessu tilfelli, áður en þú reynir að búa til liðinn **Lánardrottnahóp** verður þú að ganga úr skugga um að **Net30** sé til í bæði Microsoft Dynamics 365 for Finance and Operations og Common Data Service. (Í framtíðinni mun Microsoft gefa út tvískipta verkvangsaðgerð sem kallast Upphafssamstilling. Þessi aðgerð mun gera staka samstillingu gagna milli Finance and Operations og Common Data Service sem hluti af tvískiptu uppsetningunni.)

> [!TIP]
> Microsoft er að gefa út tvískipt kort fyrir öll tilvísunargögn, þ.m.t. **Greiðsluskilmála** (Greiðsluskilmálar). Ef þú ert nú þegar með upphafsgögnin í einu kerfinu, getur lítil uppfærsluaðgerð á plötunni kallað fram tvískipt skrif á þá skrá.

Þú verður að fylgja eftirfarandi forgangsröð og ganga úr skugga um að upphafsgögnin séu aðgengileg bæði varðandi Finance and Operations og Common Data Service.

## <a name="vendor"></a>Lánardrottinn

Hér er röð framkvæmdar fyrir eininguna **Lánardrottinn**:

1. Lánardrottnaflokkur

    1. Greiðsluskilmálar

        1. Greiðsludagur og línur
        2. Greiðsluáætlun

2. Greiðsluháttur lánardrottins

## <a name="customer-organization"></a>Viðskiptavinur (fyrirtæki)

Hér er röð framkvæmdar fyrir eininguna **Viðskiptavinur**:

1. Flokkur viðskiptavina

    1. Greiðsluskilmálar

        1. Greiðsludagur og línur
        2. Greiðsla 

2. Greiðslumáti viðskiptavinar

## <a name="contact-person"></a>Tengiliður (Einstaklingur)

Hér er röð framkvæmdar fyrir eininguna **Tengiliður**:

1. Viðskiptavinur
2. Lánardrottinn
