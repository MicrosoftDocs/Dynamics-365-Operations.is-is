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
ms.openlocfilehash: faf381458fec27e3140579486485d89bb81dfd4c2eae2d60f906c69491009f4c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6780363"
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
