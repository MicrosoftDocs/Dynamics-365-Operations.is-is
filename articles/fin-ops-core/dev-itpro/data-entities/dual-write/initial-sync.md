---
title: Framkvæmdapöntun fyrir fyrstu samstillingu Finance and Operations forrit og Common Data Service
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
ms.openlocfilehash: befe4e12a10f4a39b90bcb4faba6431a063a40e2
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019840"
---
# <a name="execution-order-for-initial-synchronization-of-finance-and-operations-apps-and-common-data-service"></a>Framkvæmdapöntun fyrir fyrstu samstillingu Finance and Operations forrit og Common Data Service

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

Áður en þú notar gagnasamþættingu verður þú að búa til fyrstu gögn sem krafist er fyrir viðskiptavini, lánardrottna og tengiliði. Til dæmis viltu búa til nýtjan lið **Lánardrottnahóp** og stillir gildið **Greiðsluskilmála** á **Net30**. Í þessu tilfelli, áður en þú reynir að búa til liðinn **Lánardrottnahóp** verður þú að ganga úr skugga um að **Net30** sé til í bæði forritinu og Common Data Service. (Í framtíðinni mun Microsoft gefa út tvískipta verkvangsaðgerð sem kallast Upphafssamstilling. Þessi aðgerð mun gera staka samstillingu gagna milli forritsins og Common Data Service sem hluti af tvískiptu uppsetningunni.)

> [!TIP]
> Microsoft er að gefa út tvískipt kort fyrir öll tilvísunargögn, þ.m.t. **Greiðsluskilmála** (Greiðsluskilmálar). Ef þú ert nú þegar með upphafsgögnin í einu kerfinu, getur lítil uppfærsluaðgerð á plötunni kallað fram tvískipt skrif á þá skrá.

Þú verður að fylgja eftirfarandi forgangsröð og ganga úr skugga um að upphafsgögnin séu aðgengileg í forritinu og Common Data Service.

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
