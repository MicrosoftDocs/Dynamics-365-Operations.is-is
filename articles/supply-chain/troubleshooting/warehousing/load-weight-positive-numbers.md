---
title: Þyngd farms getur aðeins innihaldið jákvæðar tölur
description: Þegar unnið er úr vinnu milli staðsetninga gætir þú fengið villu hvað varðar þyngd farms og að hætt verði við uppfærsluna þína. Fylgdu þessum skrefum til að laga vandamálið.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 8ea1f6679a521e3e8683b8e5f18f509e98044414
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476648"
---
# <a name="load-weight-error-and-update-canceled-when-processing-work-between-locations"></a>Villa varðandi hleðsluþyngd og uppfærsla afturkölluð þegar vinnsla fer fram á milli staða

## <a name="symptoms"></a>Einkenni

Ef það er opin vinna þegar unnið er úr vinnu frá pökkunarstaðsetningum til geymslustaðsetningar eða frá geymslu til dreifingarstaðsetninga gætir þú fengið eftirfarandi villur:

> Reiturinn „Þyngd farms“ (=-%1) getur aðeins innihaldið jákvæðar tölur. Uppfærsla hefur verið rofin.

## <a name="resolution"></a>Lausn

Til að laga þetta vandamál skal fara í **Kerfisstjórnun \> Reglubundin verk \> Gagnagrunnur \> Samræmisathugun** og keyra ferlið fyrir **Samræmisathugun á hleðsluþyngd vöruhúss**.
