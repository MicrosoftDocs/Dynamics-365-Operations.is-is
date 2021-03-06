---
title: Úrræðaleit fyrir vöruhúsavinnu
description: Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með vöruhúsavinnu í Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 08cc074fe851b952ebfc942ae3d1cb05240d3b91
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837442"
---
# <a name="troubleshoot-warehouse-work"></a>Úrræðaleit fyrir vöruhúsavinnu

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með vöruhúsavinnu í Microsoft Dynamics 365 Supply Chain Management.

## <a name="i-cant-move-license-plates-that-have-serial-number-items-when-blank-issue-and-blank-receipt-are-allowed-on-the-tracking-dimension-group"></a>Ekki er hægt að færa númeraplötur sem eru með raðnúmer þegar auðir reitir og auð innhreyfing eru leyfð í rakningarvíddarflokknum.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Ekki er hægt að færa númeraplötu með því að nota valmyndaratriðið **Hreyfing** ef raðnúmerið er með stillingar fyrir *Auð úthreyfing heimil* og *Auð innhreyfing heimil* í rakningarvíddaflokki, og ef margar númeraplötur eru á sömu staðsetningu þar sem sumar eru með raðnúmer og sumar þeirra ekki.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Þetta vandamál verður lagfært með breytingum sem eru virkjaðar í [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687). Þessar breytingar gera reitinn **Raðnúmer** valfrjálsan þegar auð kvittun og auðir reitir eru leyfð.

## <a name="i-receive-the-following-error-message-in-the-warehouse-management-mobile-app-when-i-process-movements-the-inventory-owner-1-is-not-allowed-in-this-process"></a>Ég fæ eftirfarandi villuboð í farsímaforriti vöruhúsakerfis þegar ég keyri hreyfingar: „Birgðaeigandinn %1 er ekki leyfður í þessu ferli.“

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Rakningarvíddin **Eigandi** er ekki til staðar þegar farsímaforrit vöruhúsakerfis er notað fyrir hreyfingar. Regluleg birgðaflutningsfærslubók úr biðlara Supply Chain Management virðist ekki virka eins og ætlað var og aðeins er hægt að bóka hana ef víddin **Eigandi** er fyllt út.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Microsoft hefur metið þetta mál og hefur ákvarðað að þetta sé takmörkun eiginleika. Sem stendur styður vöruhúsakerfisferli aðeins birgðir sem eru í eigu lögaðilans.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]