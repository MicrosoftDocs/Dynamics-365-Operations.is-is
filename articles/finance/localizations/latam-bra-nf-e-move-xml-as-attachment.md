---
title: Færa NF-e XML-skrár sem viðhengi
description: Þessi grein útskýrir hvernig á að færa NF-e XML skrár úr þínum Microsoft Dynamics 365 Fjármál eða Dynamics 365 Supply Chain Management gagnagrunn og gera þau aðgengileg sem viðhengi í staðinn.
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
ms.openlocfilehash: ce9061896759efeb8e8960e84656d5fc1f0616ae
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877898"
---
# <a name="move-nf-e-xml-files-as-attachments"></a>Færa NF-e XML-skrár sem viðhengi

[!include [banner](../includes/banner.md)] 


Þegar rafræn ríkisfjármálaskjöl (NF-e) eru gefin út eru XML skrár búnar til og geymdar í Microsoft Dynamics 365 Fjármál og Dynamics 365 Supply Chain Management gagnagrunna. Í brasilískri staðsetningu geturðu notað **NF-e XML færa sem viðhengi** eiginleika til að losa um gagnagrunnsrýmið sem þessar XML skrár neyta.

Fyrir tiltekið tímabil og fjárhagslega stofnun færir eiginleikinn NF-e XML skrárnar úr gagnagrunni fjármála- eða birgðakeðjustjórnunar yfir í Blob geymsluna úr Azure áskriftinni þinni. Þessi hreyfing gerir skrárnar aðeins aðgengilegar sem viðhengi. Eftir að XML-skrárnar hafa verið fluttar yfir í Blob-geymsluna er upprunalegu skránum eytt úr gagnagrunni Fjármála- eða Supply Chain Management. Þess vegna er gagnagrunnsrýmið sem þessar skrár notuðu losað.

Fylgdu þessum skrefum til að virkja **NF-e XML færa sem viðhengi** eiginleiki.

1. Opnaðu í Finance eða Supply Chain Management **Eiginleikastjórnun** vinnurými.
2. Á **Allt** flipann, leitaðu að og veldu **NF-e XML færa sem viðhengi** eiginleiki.
3. Veldu **Virkja núna**.

Fylgdu þessum skrefum til að færa NF-e XML skrár sem viðhengi.

1. Fara til **Reikningur fáanlegur** \> **Fjárhagsskjöl** \> **Rafræn ríkisfjármálaskjöl** \> **Færa NF-e XML sem viðhengi**.
2. Í **Frá dags** og **Til dagsins í dag** reiti, veldu upphafs- og lokadagsetningar.
3. Í **Auðkenni ríkisfjármálastofnunar** reit, veldu gildi.
4. Veldu **Í lagi**.

> [!IMPORTANT]
> Þetta ferli er ekki afturkræft. Eftir að þú hefur fært NF-e XML skrárnar geta notendur aðeins skoðað þær með því að velja **Viðhengi** efst á **Fjárhagsskjal** síðu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
