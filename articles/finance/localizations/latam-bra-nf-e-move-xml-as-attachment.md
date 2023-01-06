---
title: Færa NF-e XML-skrár sem viðhengi
description: Þessi grein útskýrir hvernig á að færa NF-e XML skrár úr Microsoft Dynamics 365 Finance eða Dynamics 365 Supply Chain Management gagnagrunni og gera þær tiltækar sem viðhengi í staðinn.
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
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270625"
---
# <a name="move-nf-e-xml-files-as-attachments"></a>Færa NF-e XML-skrár sem viðhengi

[!include [banner](../includes/banner.md)] 


Þegar rafræn reikningsskjöl (NF-e) eru gefin út eru XML-skrár búnar til og geymdar í Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management gagnagrunnum. Í brasilísku staðfærslunni er hægt að nota **NF-e XML flutt sem viðhengi** til að losa gagnagrunnsplássið sem XML skrárnar nota.

Fyrir tiltekið tímabil og fjárhagsstofnun færir eiginleikinn NF-e XML skrár úr gagnagrunni Finance eða Supply Chain Management yfir í Blob geymslu frá Azure áskriftinni þinni. Þessi hreyfing gerir skrárnar aðeins tiltækar sem viðhengi. Eftir að XML-skrár hafa verið færðar í Blob-geymsluna er upprunalegum skrám eytt úr gagnagrunni Finance eða Supply Chain Management. Því er gagnagrunnsplássinu sem geymir þær skrár sem notaðar eru sleppt.

Fylgið eftirfarandi skrefum til að virkja **NF-e XML flutt sem viðhengi** eiginleika.

1. Í Finance eða Supply Chain Management skaltu opna vinnusvæði **Eiginleikastjórnun**.
2. Á flipanum **Allt** skaltu leita að og velja **NF-e XML flutt sem viðhengi**.
3. Veldu **Virkja núna**.

Fylgdu eftirfarandi skrefum til að færa NF-e XML-skrár sem viðhengi

1. Farið í **Viðskiptakröfur** \> **Fjárhagsskjöl** \> **Rafræn fjárhagsskjöl** \> **Færa NF-e XML-skrár sem viðhengi**.
2. Í reitunum **Frá dagsetningu** og **Til dagsetningar** skal velja upphafs- og lokadagsetningar.
3. Sláið inn eða veldu gildi í reitnum **Kenni fjármagnsfyrirtækis**.
4. Veldu **Í lagi**.

> [!IMPORTANT]
> Þetta ferli er ekki afturkræft. Eftir að þú færir NF-e XML skrárnar geta notendur aðeins skoðað þær með því að velja **Viðhengi** efst á síðunni **Fjárhagsskjal**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
