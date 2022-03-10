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
ms.openlocfilehash: a41cf955d151726348bea83e52a24bc8784352c2d07268ced944e4cc6bf35491
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712911"
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
