---
title: TDS-útreikningur á reikningum
description: Í þessu efnisatriði er að finna tilvísun í færslur þar sem skattur sem dreginn er frá í uppruna (TDS) er reiknaður á reikningsstigi.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 496e87e3028025f738d2f0a697d91c18b77ad1c9
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023332"
---
# <a name="tds-calculation-on-invoices"></a>TDS-útreikningur á reikningum

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er að finna tilvísun í færslur þar sem skattur sem dreginn er frá í uppruna (TDS) er reiknaður á reikningsstigi.

| Raðnúmer | Færslugerð                                 | Færsluupphæð | Síðuheiti og valslóð                                 | Gerð lykils og gerð mótlykils                         |
| ------------- | ------------------------------------------------ | ------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 1.            | Kaup gerð af lánardrottni / skráningarkostnaður   | Debet- eða kredit  | Almenn dagbókarsíða (Almenn færslubók  > bókhaldsfærslur > Almennar færslubækur), Færslubókarsamþykkt reiknings (Viðskiptaskuldir > Reikningar > Komubók), Dagbókarsíða reiknings (Viðskiptaskuldir >  Reikningar > Reikningabók) | Fjárhagur (Dr.)  Lánardrottinn (Cr.).  Staðgreiðsluskattur er aðeins reiknaður fyrir samsetninguna Lánardrottinn-Fjárhagur þegar Fjárhagslykillinn er með reikningsgerðina **Innkaup**  **peningar**. |
| 2.            | Kaup gerð af viðskiptavini / skráningarkostnaður | Debet- eða kredit  | Almennar dagbókarsíður (Almenn færslubók  > bókhaldsfærslur >   Almennar færslubækur), Dagbókarsíða reiknings (Viðskiptaskuldir >  Reikningar > Reikningabók) | Fjárhagur (Dr.) viðskiptavinur (Cr.)                                 |
| 3.            | Eignakaup af lánardrottni              | Debet- eða kredit  | Almenn dagbókarsíða (Almenn færslubók  > bókhaldsfærslur > Almennar færslubækur), Komubók reikninga (Viðskiptaskuldir > Reikningar > Komubók), Dagbókarsíða reiknings (Viðskiptaskuldir >  Reikningar > Reikningabók) | Fasteignir (Dr.)  Lánardrottinn (Cr.)                             |
| 4.            | Eignakaup af viðskiptavini            | Debet- eða kredit  | Almennar dagbókarsíður (Almenn færslubók  > bókhaldsfærslur >   Almennar færslubækur), Dagbókarsíða reiknings (Viðskiptaskuldir >  Reikningar > Reikningabók) | Eignir (Dr.)  Viðskiptavinur (Cr.)                           |
| 5.            | Innkaupareikningur (TDS til greiðslu)                  |                    | Síða innkaupapöntunar (Viðskiptaskuldir > Innkaupapantanir > Allar innkaupapantanir) |                                                              |
| 6.            | Sölureikningur (TDS krafa)                  |                    | Síða sölupantana (Viðskiptakröfur > Pantanir > Allar sölupantanir), Síða reikninga með frjálsum texta (Viðskiptakröfur > Reikningar > Allir reikningar með frjálsum texta) |                                                              |
