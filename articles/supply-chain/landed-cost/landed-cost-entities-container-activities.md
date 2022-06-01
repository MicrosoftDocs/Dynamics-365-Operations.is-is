---
title: Gámastarfsemi eining
description: Þetta efnisatriði veitir upplýsingar um gámastarfsemi, sem eru notuð til að fylgjast með framvindu flutningsgáma.
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
ms.openlocfilehash: 7bb2b97e8885e3b1265f0c93585873c8a64f1dfb
ms.sourcegitcommit: 611202adaa080250636efabb3b3b32b850d92d04
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/28/2022
ms.locfileid: "8813164"
---
# <a name="container-activities-entity"></a>Gámastarfsemi eining

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until GA with 10.0.28 -->

Gámastarfsemi er notuð til að fylgjast með framvindu flutningsgáma. Færsla er búin til fyrir hvern áfanga sem er úthlutað á ferðasniðmátið sem er valið við stofnun flutningsgáma. Færslur eru einnig búnar til þegar flutningsgámurinn er búinn til í gegnum gagnaeiningu.

Upplýsingar um framvindu flutningsgáms berast oft frá utanaðkomandi aðilum. Gámavirknieiningin gerir ytri aðilum eins og flutningsmiðlara kleift að uppfæra færsluna beint. Þess vegna er ekki þörf á handvirkri uppfærslu á gögnum.

## <a name="container-activities-itmcontaineractivityentity"></a>Gámastarfsemi (ITMContainerActivityEntity)

Þú getur notað gámavirknieininguna (`ITMContainerActivityEntity`) til að búa til viðbótarvirkniskrár. Að öðrum kosti getur flutningsmiðlari sent uppfærslur fyrir staðfest **Raunveruleg lokadagsetning** gildi.

| Nafn | Vörpun | Gagnagerð | Lykill | Skylda |
|---|---|---|---|---|
| Raunverulegur lokadagur | ITMContainerActivityTable. Raunveruleg lokadagsetning | Datetime | Nr. | Nr. |
| Afhendingarmáti | ITMContainerActivityTable.DlvModeId | Nvarchar(10) | Nr. | Nr. |
| Áætluð lokadagsetning | ITMContainerActivityTable.EsimatedDate | Datetime | Nr. | Nr. |
| Línunúmer | ITMContainerActivityTable.LineNum | Númeric(32, 16) | **Já** | Nr. |
| Athugasemdir | ITMContainerActivityTable.Notes | nvarchar(MAX) | Nr. | Nr. |
| Aðgerð | ITMContainerActivityTable.ShipActivityId | Nvarchar(10) | Nr. | **Já** |
| Gámur | ITMContainerActivityTable.ShipContainerId | Nvarchar (20) | **Já** | **Já** |
| Ferð | ITMContainerActivityTable.ShipId | Nvarchar (20) | **Já** | **Já** |
| Leggur | ITMContainerActivityTable.ShipLegId | Nvarchar (20) | Nr. | **Já** |
| Þjónustuaðili | ITMContainerActivityTable.ShipService Provider | Nvarchar (20) | Nr. | Nr. |
| Hitastig | ITMContainerActivityTable.Ship Temperature | Númeric(32, 6) | Nr. | Nr. |
| Skip | ITMContainerActivityTable.ShipVesselId | Nvarchar (20) | Nr. | Nr. |
| Upphafsdagsetning | ITMContainerActivityTable.StartDate | Datetime | Nr. | Nr. |

## <a name="tracking-control"></a>Rekjastýring

Eftirlitsstjórnstöðin gerir kleift að kveikja á uppfærslu á tilteknum upprunareit með uppfærslu á tilteknu markreiti. Ef bæði gildi upprunareitsins og gildi markreitsins eru uppfærð með því að nota gámavirknieininguna, mun markreiturinn sýna einingagildið. Þessi hegðun tengist rakningarstýringarskrám sem hafa a **Búðu til tegund** verðmæti á *Leiðslutími*.

Fyrir kostnaðarsvæði sem hafa a **Búðu til tegund** verðmæti á *Stöðuuppfærsla* eða *Autt* (sem er notendaskilgreint gildi), mun kerfið uppfæra siglingastöðu eða miðsvæði í samræmi við uppsetningu rakningarstýringar.

## <a name="calculated-fields"></a>Reiknuð svæði

Gildi eftirfarandi reita í gámavirknifærslu eru reiknuð út frá gildum annarra reita. Þrátt fyrir að þessir reiknuðu reitir séu ekki með í gagnaeiningunni verða þeir stilltir ef reitirnir sem útreikningarnir byggja á eru gefnir upp.

- **Áætlaðir dagar** = **Áætluð lokadagsetning** –**Upphafsdagur**
- **Raunverulegir dagar** = **Raunveruleg lokadagsetning** –**Upphafsdagur**
