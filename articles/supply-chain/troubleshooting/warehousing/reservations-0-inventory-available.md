---
title: Ekki er hægt að gera birgðafrátekningar vegna þess að 0,00 er í boði
description: Villa kviknar sem segir að kerfið geti ekki gengið frá bókunum vegna þess að aðeins eru 0,00 tiltæk í birgðum. Þetta vandamál stafar líklega af opinni vinnu.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 75d72f7ee1bdecca5a087b75b1de9907b9d244ab
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476691"
---
# <a name="system-cant-make-reservations-because-000-are-available-in-the-inventory"></a>Kerfið getur ekki gengið frá bókunum vegna þess að 0,00 eru tiltæk í birgðum

## <a name="symptoms"></a>Einkenni

Þetta vandamál getur komið upp ef kerfið getur ekki að uppfært birgðamagn vegna þess að það eru ekki nægar birgðafærslur sem eru með tilgreindar stærðir. Þú færð eftirfarandi villuboð:

> Efnislegt lagersvæði =%1, Vöruhús=%2, Birgðastaða =Tiltækt, Rununúmer=%3, Eigandi=%4: %5 er ekki hægt að taka frá vegna þess að aðeins 0,00 eru tiltæk í birgðum.

## <a name="resolution"></a>Lausn

Þetta vandamál stafar líklega af opinni vinnu. Annaðhvort skal ljúka vinnu eða taka við án þess að stofna vinnu. Ganga skal úr skugga um að engar birgðafærslur séu efnislega í frátekt á móti magninu. Til dæmis gætu þessar færslur verið opnar gæðapantanir, birgðalokunarfærslur eða úttakspantanir.
