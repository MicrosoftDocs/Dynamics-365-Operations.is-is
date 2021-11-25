---
title: Færa NF-e XML-skrár sem viðhengi
description: Þetta efni útskýrir hvernig á að flytja NF-e XML skrár úr Microsoft Dynamics 365 Finance eða Dynamics 365 Supply Chain Management gagnagrunn og gera þau aðgengileg sem viðhengi í staðinn.
author: gionoder
ms.date: 11/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2022-01-27
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: c7b82d486cecf6b20f1283fa609c360b3003efca
ms.sourcegitcommit: ebf6546835e4d6a80aea1dfae81e119e294387f0
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/12/2021
ms.locfileid: "7799557"
---
# <a name="move-nf-e-xml-files-as-attachments"></a>Færa NF-e XML-skrár sem viðhengi

[!include [banner](../includes/banner.md)] 


Þegar rafræn fjárhagsskjöl (NF-e) eru gefin út eru XML skrár búnar til og geymdar í Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management gagnagrunna. Í brasilískri staðsetningu geturðu notað **NF-e XML færa sem viðhengi** eiginleika til að losa um gagnagrunnsrýmið sem þessar XML skrár neyta.

Fyrir tiltekið tímabil og fjárhagslega stofnun færir eiginleikinn NF-e XML skrárnar úr gagnagrunni fjármála- eða birgðakeðjustjórnunar yfir í Blob geymsluna úr Azure áskriftinni þinni. Þessi hreyfing gerir skrárnar aðeins aðgengilegar sem viðhengi. Eftir að XML-skrárnar hafa verið fluttar yfir í Blob-geymsluna er upprunalegu skránum eytt úr gagnagrunni Fjármála- eða Supply Chain Management. Þess vegna losnar gagnagrunnsrýmið sem þessar skrár notuðu.

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
