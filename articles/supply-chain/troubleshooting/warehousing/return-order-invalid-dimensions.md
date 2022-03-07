---
title: Ekki er hægt að stofna farmlínu vegna þess að birgðavíddir eru ógildar
description: Eftirfarandi villuboð kunna birtast um ógildar birgðavíddir þegar reynt er að losa skilapöntun í vöruhúsið. Fjarlægja þetta úr pöntunarlínu.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac58
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 3cb728f6a989cdac63c91d49baaea094bace59e4
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476676"
---
# <a name="cant-create-load-line-for-return-sales-order-due-to-invalid-inventory-dimensions"></a>Ekki er hægt að stofna farmlínu fyrir vöruskilapöntun vegna þess að birgðavíddir eru ógildar

## <a name="symptoms"></a>Einkenni

Eftirfarandi villuboð birtast þegar reynt er að losa skilapöntun í vöruhúsið:

> Ekki er hægt að stofna hleðslulínu fyrir þessa pöntunarlínu vegna þess að hún inniheldur ógildar birgðavíddir. Ekki er hægt að vísa til birgðavídda sem eru staðsettar fyrir neðan staðsetningarvíddina í frátekningarstigveldinu. Fjarlægðu ógildu víddirnar úr pöntunarlínunni.

## <a name="resolution"></a>Lausn

Því miður styður afurðin ekki hleðsluvinnslu fyrir söluskilaferli. Þar af leiðandi er ekki hægt að losa sölupöntun aftur í vöruhúsið.

Í sölupöntunarfærslum er ekki hægt að vísa til birgðavídda sem eru staðsettar fyrir neðan víddina **Staðsetning** í frátekningarstigveldinu. Lausnin við slíku er að fjarlægja ógildu víddirnar úr pöntunarlínunni.
