---
title: TDS-útreikningur á reikningum
description: Þessi grein veitir tilvísun fyrir færslur þar sem skattur sem dreginn er af uppruna (TDS) er reiknaður á reikningsstigi.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: efc12e0839fe87e9db435f481ce1fd733c286d6c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855364"
---
# <a name="tds-calculation-on-invoices"></a>TDS-útreikningur á reikningum

[!include [banner](../includes/banner.md)]

Þessi grein veitir tilvísun fyrir færslur þar sem skattur sem dreginn er af uppruna (TDS) er reiknaður á reikningsstigi.

| Raðnúmer | Færslugerð                                 | Færsluupphæð | Síðuheiti og valslóð                                 | Gerð lykils og gerð mótlykils                         |
| ------------- | ------------------------------------------------ | ------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 1.            | Kaup gerð af lánardrottni / skráningarkostnaður   | Debet- eða kredit  | Almenn dagbókarsíða (Almenn færslubók  > bókhaldsfærslur > Almennar færslubækur), Færslubókarsamþykkt reiknings (Viðskiptaskuldir > Reikningar > Komubók), Dagbókarsíða reiknings (Viðskiptaskuldir >  Reikningar > Reikningabók) | Fjárhagur (Dr.)  Lánardrottinn (Cr.).  Staðgreiðsluskattur er aðeins reiknaður fyrir samsetninguna Lánardrottinn-Fjárhagur þegar Fjárhagslykillinn er með reikningsgerðina **Innkaup**  **peningar**. |
| 2.            | Kaup gerð af viðskiptavini / skráningarkostnaður | Debet- eða kredit  | Almennar dagbókarsíður (Almenn færslubók  > bókhaldsfærslur >   Almennar færslubækur), Dagbókarsíða reiknings (Viðskiptaskuldir >  Reikningar > Reikningabók) | Fjárhagur (Dr.) viðskiptavinur (Cr.)                                 |
| 3.            | Eignakaup af lánardrottni              | Debet- eða kredit  | Almenn dagbókarsíða (Almenn færslubók  > bókhaldsfærslur > Almennar færslubækur), Komubók reikninga (Viðskiptaskuldir > Reikningar > Komubók), Dagbókarsíða reiknings (Viðskiptaskuldir >  Reikningar > Reikningabók) | Fasteignir (Dr.)  Lánardrottinn (Cr.)                             |
| 4.            | Eignakaup af viðskiptavini            | Debet- eða kredit  | Almennar dagbókarsíður (Almenn færslubók  > bókhaldsfærslur >   Almennar færslubækur), Dagbókarsíða reiknings (Viðskiptaskuldir >  Reikningar > Reikningabók) | Eignir (Dr.)  Viðskiptavinur (Cr.)                           |
| 5.            | Innkaupareikningur (TDS til greiðslu)                  |                    | Síða innkaupapöntunar (Viðskiptaskuldir > Innkaupapantanir > Allar innkaupapantanir) |                                                              |
| 6.            | Sölureikningur (TDS krafa)                  |                    | Síða sölupantana (Viðskiptakröfur > Pantanir > Allar sölupantanir), Síða reikninga með frjálsum texta (Viðskiptakröfur > Reikningar > Allir reikningar með frjálsum texta) |                                                              |
