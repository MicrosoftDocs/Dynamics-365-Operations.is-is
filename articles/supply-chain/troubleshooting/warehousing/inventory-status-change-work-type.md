---
title: Ekki er hægt að velja breytingu á birgðastöðu sem vinnugerð
description: Ekki er hægt að stofna vinnusniðmátslínu fyrir breytingu á birgðastöðu því að vinnugerðin er aðeins notuð af kerfisvinnslum. Velja skal aðra vinnutegund.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ad7f26f3235d15779583f9cdadeb4e6dca16242a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476694"
---
# <a name="cant-select-inventory-status-change-in-the-work-type-column"></a>Ekki er hægt að velja breytingu á birgðastöðu í vinnugerðardálknum

## <a name="symptoms"></a>Einkenni

Þegar Microsoft Dynamics 365 Supply Chain Management er stillt gætir þú fengið eftirfarandi villuboð:

> Ekki er hægt að stofna vinnusniðmátslínu fyrir Breyting á birgðastöðu því að vinnutegundin er ógild. Velja skal aðra vinnutegund.

## <a name="resolution"></a>Lausn

Þessi hegðun er samkvæmt hönnuninni. Vinnutegundin *Breyting á birgðastöðu* er aðeins notuð af kerfisvinnslu. Ekki er hægt að stilla þetta. Vegna þess að listi yfir vinnugerðir er fastur sem tölusetning er ekki hægt að sía aukafærslur úr fellivalmyndinni **Vinnutegund**.
