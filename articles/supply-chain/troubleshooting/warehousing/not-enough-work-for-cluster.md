---
title: Ekki fannst nægileg vinna fyrir klasa eftir að hafa skilgreint forstillingu
description: Ef þú skilgreinir klasaforstillingu gætir þú fengið villuboð sem segja að ekki finnist nægilega mikil vinna. Breyttu forstillingunni og stilltu „Virkja stöður“ á „Nei“.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 139fd72e571c8ef83af2fd0e497cf334b6ef0ea4
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476626"
---
# <a name="not-enough-work-found-for-cluster-when-using-system-directed-cluster-picking"></a>Ekki fannst næg vinna fyrir klasa við notkun kerfisstýrðrar klasatiltektar

## <a name="symptoms"></a>Einkenni

Þegar ferlið *Kerfisstýrð klasatiltekt* er notað, ef klasaforstilling er skilgreind þar sem t.d. hægt er að tína úr 10 staðsetningum, virkar ferlið samkvæmt áætlun þegar næg vinna er til að tína í 10 staðsetningum. Ef hinsvegar aðeins átta staðsetningar eru til að tína úr, koma upp eftirfarandi villuboð:

> Ekki finnst nægileg vinna fyrir klasann.

## <a name="resolution"></a>Lausn

Til að laga þetta vandamál skal breyta klasaforstillingunni og stilla valkostinn **Virkja stöður** á *Nei*.
