---
title: Samstilla tilfangagetu
description: Í þessu efnisatriði er að finna upplýsingar um hvernig á að samstilla afkastagetu tilfanga í dagatölum og verkum.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 27b6fde91a72e37bb2712daba765032322cbd4e9
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760572"
---
# <a name="synchronize-resource-capacity"></a>Samstilla tilfangagetu

[!include [banner](../includes/banner.md)]

Vinnslur fyrir samstillingu tilfanga hjálpar til við að tryggja að upplýsingar fyrir dagatal og grunndagatal seytli niður í röðun tilfanga verks. Ef dagatali er breytt gera ferlin nauðsynlegar uppfærslur á áætlun tilfanga verks. Ferlin hjálpa einnig til með að bæta afköst, þar sem tilfangaupplýsingar á dagatalinu eru samstilltar fyrirfram. Því gerast uppfærslur á upplýsingum tilfanga hraðar. Mælt er með er skipuleggja ferlin sem runuvinnslu í stað þess að skipuleggja einn í einu. Annars er hætta á að einhver gleymi sameiginlegum dagsetningum þegar upplýsingarnar voru síðast samstilltar. Ef ekki eru notaðar sameiginlegar dagsetningar geta eyður komið fram við samstillingu á dagsetningu.

![Samstilling dagatals](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a>Samstilla tilfangagetu samantekta

Samstillingarferlið er hannað til að samstilla upplýsingar um öll dagatöl tilfanga. Þessar upplýsingar innihalda grunnupplýsingar dagatals um allar breytingar á Töflu yfir afkastagetu tilfangadagatals.verksins. Ef nýjum tilföngum er bætt við verkið, hjálpar samstilling við að tryggja að uppfærðu dagatalsupplýsingarnar séu tiltækar. Þessa samstillingu er hægt að gera hvenær sem er.

Mælt er með því að nota runuvinnslu. Valkostirnir er tiltækir í samstillingu frátekinnar afkastagetu.

1. Valið er **Verkefnastjórnun og bókhald** &gt; **Reglubundið** &gt; **Samstilling afkastagetu** &gt; **Samstilla afkastagetu samantekta**.
2. Stillið valkostina í eftirfarandi töflu.

    | Valkostur      | lýsing |
    |-------------|-------------|
    | Tímabilskóði | Einnig er hægt að velja kóða dagsetningabils í fjárhagi til að stilla upphafs og lokadag fyrir samstillingarferli fyrir tilfangagetu samantekta. |
    | Fyrsti vinnudagur  | Færa skal inn upphafsdag fyrir samstillingarferli fyrir tilfangagetu samantekta. |
    | Lokadagur    | Færa skal inn lokadag fyrir samstillingarferli fyrir tilfangagetu samantekta. |

[![Samstillingarferli](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)
