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
ms.openlocfilehash: b74bc2d3133af7e87663a4e6bafb8780e0a6a66f
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797299"
---
# <a name="execution-order-for-initial-sychronization-of-finance-and-operations-and-common-data-service"></a>Framkvæmdapöntun fyrir fyrstu samstillingu Finance and Operations og Common Data Service

Áður en þú notar gagnasamþættingu verður þú að búa til fyrstu gögn sem krafist er fyrir viðskiptavini, lánardrottna og tengiliði. Til dæmis ef þú vilt búa til nýjan lið **Lánardrottnahóp** og stilla **Greiðsluskilmála** hans á **Net30** þá þarftu, áður en þú reynir að stofna liðinn **Lánardrottnahóp** að ganga úr skugga um að **Net30** sé bæði til í Finance and Operations og Common Data Service. (Í framtíðinni munum við gefa út tvískipta verkvangsaðgerð sem kallast **Upphafssamstilling**. Hún mun gera staka samstillingu gagna milli Finance and Operations og Common Data Service sem hluti af tvískiptu uppsetningunni.)

Ábending: Við gefum út tvískipt kort fyrir öll tilvísunargögn, þ.m.t. **Greiðsluskilmála** (Greiðsluskilmálar). Ef þú ert nú þegar með upphafsgögnin í einu kerfinu, getur lítil uppfærsluaðgerð á plötunni kallað fram tvískipt skrif á þá skrá. 

Þú verður að fylgja eftirfarandi forgangsröð og ganga úr skugga um að upphafsgögnin séu aðgengileg bæði varðandi Finance and Operations og Common Data Service.   

## <a name="vendor"></a>Lánardrottinn

Röð framkvæmdar fyrir lánardrottinn er:

```
Vendor Group
    Terms of payment
        Payment day & lines
        Payment schedule
Vendor payment method
```

## <a name="customer-organization"></a>Viðskiptavinur (fyrirtæki)

Röð framkvæmdar fyrir viðskiptavin er:

```
Customer Group
    Terms of payment
        Payment day & lines
        Payment 
Customer payment method
```

## <a name="contact-person"></a>Tengiliður (Einstaklingur)

Röð framkvæmdar fyrir tengilið er:

```
Customer
Vendor               
```
