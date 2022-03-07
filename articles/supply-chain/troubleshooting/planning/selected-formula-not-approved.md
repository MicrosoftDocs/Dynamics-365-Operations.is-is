---
title: Valið formúlunúmer er ekki samþykkt fyrir runupöntun
description: Þegar reynt er að festa áætlaða pöntun berast villuboð sem segja að valið formúlunúmer sé ekki samþykkt fyrir runupöntun.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4f993c92ca0a2f8f79e4b0e0eda43904529163f8
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294097"
---
# <a name="selected-formula-number-isnt-approved-for-a-batch-order"></a>Valið formúlunúmer er ekki samþykkt fyrir runupöntun

Villukóði PRO2614

## <a name="symptoms"></a>Einkenni

Þegar reynt er að fastsetja áætlaða pöntun berast eftirfarandi villuboð:

> Valið formúlunúmer er ekki samþykkt fyrir runupöntun.

## <a name="cause"></a>Orsök

Kerfið staðfestir festingaraðgerðina til að ganga úr skugga um samþykkt formúla sé tiltæki fyrir virka vöru. Þú verður líklega að samþykkja formúluna.

## <a name="resolution"></a>Lausn

Til að samþykkja formúlu skal fylgja þessum skrefum.

1. Farið í **Stjórnun framleiðsluupplýsinga \> Uppskriftir og formúlur \> Formúlur**.
1. Veljið viðeigandi formúlu.
1. Á aðgerðasvæðinu, í flipanum **Formúla**, í flokknum **Vinna með**, skal velja **Samþykkja formúlu**.
1. Í svarglugganum **Samþykkja uppskrift eða formúlu** skal velja samþykktaraðila og velja síðan **Í lagi**.
