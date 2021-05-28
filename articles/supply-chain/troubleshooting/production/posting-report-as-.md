---
title: Villa þegar Bóka sem tilbúið færslubók er bókuð.
description: Þegar bókað er í færslubókina Tilkynna sem lokið birtast villuboð þar sem fram kemur að ekki sé hægt að minnka pantað magn.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTableListPage, ProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 55db7d0033dd66c1b973abf96671a20ab05d61d8
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026598"
---
# <a name="error-when-the-report-as-finished-journal-is-posted"></a>Villa þegar Bóka sem tilbúið færslubók er bókuð.

KB númer: 4612891

## <a name="symptoms"></a>Einkenni

Villa kemur upp þegar dagbókin **Tilkynna sem lokið** er bókuð og eftirfarandi villuboð munu berast:

> Ekki er hægt að minnka pantað magn því ekki eru nógu margar opnar birgðafærslur með stöðu pöntunar. Vörurnar eru keyptar, mótteknar eða skráðar.

Þessi villa á sér aðeins stað þegar reiturinn **Gallað magn** er stilltur á fyrstu línu færslubókarinnar **Tilkynna sem lokið** og reiturinn **Gallalaust magn** er stilltur á síðustu línu. Ef reiturinn **Gallað magn** er stilltur á síðustu línu kemur engin villa upp.

## <a name="resolution"></a>Upplausn

Til að koma í veg fyrir þessa villu skal opna síðuna **færibreytur Framleiðslustýringar** og síðan, á flipanum **Almennt**, stilla valkostinn **Auka eftirstandandi magn með villumagni** valkostinn á *Já*.
