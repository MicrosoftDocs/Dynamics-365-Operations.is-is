---
title: Ekki er hægt að stofna farmlínu vegna þess að birgðavíddir eru ógildar
description: Eftirfarandi villuboð kunna birtast um ógildar birgðavíddir þegar reynt er að losa skilapöntun í vöruhúsið. Fjarlægja þetta úr pöntunarlínu.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: b02408b61b07b272a7e7d52004dc2492d60ef28c
ms.sourcegitcommit: 0d14c4a1e6cf533dd20463f1a84eae8f6d88f71b
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/14/2022
ms.locfileid: "8119213"
---
# <a name="cant-create-load-line-for-return-sales-order-due-to-invalid-inventory-dimensions"></a>Ekki er hægt að stofna farmlínu fyrir vöruskilapöntun vegna þess að birgðavíddir eru ógildar

## <a name="symptoms"></a>Einkenni

Eftirfarandi villuboð birtast þegar reynt er að losa skilapöntun í vöruhúsið:

> Ekki er hægt að stofna hleðslulínu fyrir þessa pöntunarlínu vegna þess að hún inniheldur ógildar birgðavíddir. Ekki er hægt að vísa til birgðavídda sem eru staðsettar fyrir neðan staðsetningarvíddina í frátekningarstigveldinu. Fjarlægðu ógildu víddirnar úr pöntunarlínunni.

## <a name="resolution"></a>Lausn

Því miður styður afurðin ekki hleðsluvinnslu fyrir söluskilaferli. Þar af leiðandi er ekki hægt að losa sölupöntun aftur í vöruhúsið.

Í sölupöntunarfærslum er ekki hægt að vísa til birgðavídda sem eru staðsettar fyrir neðan víddina **Staðsetning** í frátekningarstigveldinu. Lausnin við slíku er að fjarlægja ógildu víddirnar úr pöntunarlínunni.
