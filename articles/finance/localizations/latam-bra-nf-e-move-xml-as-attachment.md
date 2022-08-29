---
title: Færa NF-e XML-skrár sem viðhengi
description: Þessi grein útskýrir hvernig á að færa NF-e XML skrár úr Microsoft Dynamics 365 Fjármál eða Dynamics 365 Supply Chain Management gagnagrunni og gera þær aðgengilegar sem viðhengi í staðinn.
author: gionoder
ms.date: 11/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2022-01-27
ms.dyn365.ops.version: 10.0.25
ms.custom: 97423
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 7bb0fb975c6d73cc4e990b39ea9b5a0c0455db74
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270625"
---
# <a name="move-nf-e-xml-files-as-attachments"></a>Færa NF-e XML-skrár sem viðhengi

[!include [banner](../includes/banner.md)] 


Þegar rafræn ríkisfjármálaskjöl (NF-e) eru gefin út eru XML skrár búnar til og geymdar í Microsoft Dynamics 365 Fjármál og Dynamics 365 Supply Chain Management gagnagrunna. Í brasilískri staðsetningu geturðu notað **NF-e XML færa sem viðhengi** eiginleika til að losa um gagnagrunnsrýmið sem þessar XML skrár neyta.

Fyrir tiltekið tímabil og fjárhagslega stofnun færir eiginleikinn NF-e XML skrárnar úr gagnagrunninum þínum á fjármála- eða framboðskeðjustjórnun yfir í Blob geymsluna úr Azure áskriftinni þinni. Þessi hreyfing gerir skrárnar aðeins aðgengilegar sem viðhengi. Eftir að XML-skrárnar hafa verið fluttar yfir í Blob-geymsluna er upprunalegum skrám eytt úr gagnagrunni Fjármála- eða Supply Chain Management. Þess vegna losnar gagnagrunnsrýmið sem þessar skrár notuðu.

Fylgdu þessum skrefum til að virkja **NF-e XML færa sem viðhengi** eiginleiki.

1. Í Finance eða Supply Chain Management, opnaðu **Eiginleikastjórnun** vinnurými.
2. Á **Allt** flipann, leitaðu að og veldu **NF-e XML færa sem viðhengi** eiginleiki.
3. Veldu **Virkja núna**.

Fylgdu þessum skrefum til að færa NF-e XML skrár sem viðhengi.

1. Fara til **Reikningur fáanlegur** \> **Fjárhagsskjöl** \> **Rafræn ríkisfjármálaskjöl** \> **Færa NF-e XML sem viðhengi**.
2. Í **Frá dags** og **Til dagsins í dag** reiti skaltu velja upphafs- og lokadagsetningar.
3. Í **Auðkenni ríkisfjármálastofnunar** reit, veldu gildi.
4. Veldu **Í lagi**.

> [!IMPORTANT]
> Þetta ferli er ekki afturkræft. Eftir að þú hefur fært NF-e XML skrárnar geta notendur aðeins skoðað þær með því að velja **Viðhengi** efst á **Fjárhagsskjal** síðu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
