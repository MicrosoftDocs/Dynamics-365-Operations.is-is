---
title: Birgðamagn ekki uppfært vegna of fárra færslna
description: Ekki er hægt að uppfæra birgðamagn um -1% vegna þess að það eru ekki nógu margar birgðafærslur fyrir vöruna %2 sem er með tilgreindar víddir.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 88130a969039dd741c8ea4fbaabe81acf0e6fb6a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476611"
---
# <a name="system-cant-update-inventory-quantity-because-of-insufficient-transactions"></a>Kerfið getur ekki uppfært birgðamagn vegna of fárra færslna

## <a name="symptoms"></a>Einkenni

Þetta vandamál getur komið upp ef kerfið getur ekki að uppfært birgðamagn vegna þess að það eru ekki nægar birgðafærslur sem eru með tilgreindar stærðir. Þú færð eftirfarandi villuboð:

> Ekki var hægt að uppfæra birgðamagnið -%1 vegna þess að ekki voru nógu margar birgðafærslur fyrir vöruna %2 með málin Stærð=%3, Litur=%4, Viðbætur=%5, Staður=%6, Vöruhús=%7, Staðsetning=%8, Birgðastaða=Tiltækar, Leyfisplata=%9, Lotunúmer=%10 tilvísunarauðkenni %11 á lotukenni %12.

## <a name="resolution"></a>Lausn

Ganga skal úr skugga um að engar birgðafærslur séu efnislega í frátekt á móti magninu. Til dæmis gætu þessar færslur opnað gæðapantanir, birgðalokunarfærslur eða úttakspantanir.
