---
title: Flutningur undirbókar í Fjárhag
description: Þetta efni lýsir getu Microsoft Dynamics 365 Finance tengt flutningsferli undirbókar í aðalbókinni.
author: roschlom
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-01-18
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 1efdf095e379b73d553ca3525abbeee8ca35bcbb
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897505"
---
# <a name="subledger-transfer-to-the-general-ledger"></a>Flutningur undirbókar í Fjárhag

[!include [banner](../includes/banner.md)]

Þetta efni lýsir getu í Microsoft Dynamics 365 Finance sem tengjast reglum um flutning á lotum dagbókarfærslna undirbókar.

Í útgáfu 8.1 voru gerðar breytingar til að leyfa flutning á reglum sem úreltu valkostinn **Samstillt**. Nánari upplýsingar er að finna í [Fjarlægðar eða úreltar aðgerðir fyrir Finance and Operations](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=%2fdynamics365%2ffinance%2ftoc.json#finance-and-operations-81-with-platform-update-20).

Eftirfarandi valkostir eru tiltækir til að flytja hópi á hærri stærð. 

 - Ósamstilltur - Þessi valkostur mun tafarlaust tímasetja flutning bókhaldsgagnanna á undirstöðunni til fjárhags. Fylgiskjal fjárhags verða tekin upp um leið og fjármagni er frjálst að afgreiða þessa beiðni á netþjóninum. 

- Tímasett lota - Þessi valkostur bætir bókhaldsfærslunum sem eru fluttar yfir í vinnslukví í aðalbókinni, þar sem færslurnar verða unnar í pöntun. Fylgiskjal fjárhags verða tekin upp um leið á áætluðum tíma ef fjármagni er frjálst að afgreiða þessa runuvinnslu á netþjóninum. 
 
Í útgáfu 10.0.8 voru gerðar úrbætur til að auka afköst ósamstillts valkosts. Þessi aðgerð er gerð virk undir nafni eiginleikans **Flutningur undirliða yfir í hagræðingu almenns fjárhags**. 
 
Þessi virkni bætir flutning gagna frá stórhýsinu yfir í aðalbókina. Það gerir ferlið kleift að vera skilvirkara og það flokka saman smærri viðskipti til að flytja. Þetta gerir kleift að nýta hópþjónninn á skilvirkari hátt. Þessi virkni krefst þess að runuþjónninn sé sett upp, nettengdur og sé í gangi til að valkosturinn Ósamstilltur flutningur virki. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]