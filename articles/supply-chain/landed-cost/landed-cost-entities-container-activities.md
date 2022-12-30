---
title: Aðgerðaeining geymis
description: Þessi grein býður upp á upplýsingar um gámaaðgerðir, sem eru notaðar til að rekja framvindu flutningsgáma.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 6a518003f8624ef05ac86be1b963c3f916420278
ms.sourcegitcommit: 5b34b41ae74269ba639e2876bc5862ef468da1cc
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/15/2022
ms.locfileid: "9167574"
---
# <a name="container-activities-entity"></a>Aðgerðaeining geymis

[!include [banner](../includes/banner.md)]

Gámaaðgerðir er notað til að fylgjast með framgangi gáma. Færsla er búin til fyrir hvern legg sem er úthlutað ferðasniðinu sem er valið við gerð sendingargeymis. Skrár eru einnig búnar til þegar gámurinn er búinn til í gegnum gagnaeiningu.

Upplýsingar um framgang flutningsgáms í flutningi eru oft fengnar frá ytri uppruna. Eining gámaaðgerða gerir ytri uppruna eins og flutningsmiðlara kleift að uppfæra færsluna með beinum hætti. Því er ekki þörf á handvirkri uppfærslu gagna.

## <a name="container-activities-itmcontaineractivityentity"></a>Gámaaðgerðir (ITMContainerActivityEntity)

Hægt er að nota einingu gámaaðgerða (`ITMContainerActivityEntity`) til að stofna frekari færslur aðgerða. Einnig getur farmflytjandi sent uppfærslur til að fá staðfest **Raunverulegur lokadagur**.

| Nafn | Vörpun | Gagnagerð | Lykill | Skylda |
|---|---|---|---|---|
| Raunverulegur lokadagur | ITMContainerActivityTable.ActualEndDate | Datetime | Nr. | Nr. |
| Afhendingarmáti | ITMContainerActivityTable.DlvModeId | Nvarchar(10) | Nr. | Nr. |
| Áætluð lokadagsetning | ITMContainerActivityTable.EsimatedDate | Datetime | Nr. | Nr. |
| Línunúmer | ITMContainerActivityTable.LineNum | Tölustafir(32; 16) | **Já** | Nr. |
| Athugasemdir | ITMContainerActivityTable.Notes | Nvarchar(MAX) | Nr. | Nr. |
| Aðgerð | ITMContainerActivityTable.ShipActivityId | Nvarchar(10) | Nr. | **Já** |
| Gámur | ITMContainerActivityTable.ShipContainerId | Nvarchar(20) | **Já** | **Já** |
| Ferð | ITMContainerActivityTable.ShipId | Nvarchar(20) | **Já** | **Já** |
| Leggur | ITMContainerActivityTable.ShipLegId | Nvarchar(20) | Nr. | **Já** |
| Þjónustuaðili | ITMContainerActivityTable.ShipServiceProvider | Nvarchar(20) | Nr. | Nr. |
| Hitastig | ITMContainerActivityTable.ShipTemperature | Tölustafir(32; 6) | Nr. | Nr. |
| Skip | ITMContainerActivityTable.ShipVesselId | Nvarchar(20) | Nr. | Nr. |
| Upphafsdagsetning | ITMContainerActivityTable.StartDate | Datetime | Nr. | Nr. |

## <a name="tracking-control"></a>Rakningarstýring

Miðstöð rakningarstýringar virkjar uppfærslu á tilteknum upprunareit sem uppfærsla á tilteknum markreit á að ræsa. Ef bæði gildi upprunareitsins og gildi markreitsins eru uppfærð með því að nota einingu gámaaðgerða mun markreiturinn sýna einingagildið. Þessi hegðun tengist færslum rakningarstýringar sem eru með **Gerð stofnunar** gildi fyrir *Afhendingartíma*.

Fyrir kostnaðarþætti sem eru með gildi fyrir **Gerð stofnunar** fyrir *Stöðuuppfærslu* eða *Autt* (sem er gildi skilgreint af notanda) mun kerfið uppfæra ferðastöðuna eða markreitinn samkvæmt skilgreiningu rakningarstýringar.

## <a name="calculated-fields"></a>Reiknuð svæði

Gildi eftirfarandi reita í verkþáttarfærslu gáms eru reiknuð út frá gildum í öðrum reitum. Þrátt fyrir að þessir reiknuðu reitir séu ekki teknir með í gagnaeiningunni verða þeir settir upp ef þeir reitir sem útreikningar byggjast á eru gefnir upp.

- **Áætlaðir dagar** = **Áætluð lokadagsetning** – **Upphafsdagur**
- **Raunverulegir dagar** = **Raunveruleg lokadagsetning** – **Upphafsdagur**
