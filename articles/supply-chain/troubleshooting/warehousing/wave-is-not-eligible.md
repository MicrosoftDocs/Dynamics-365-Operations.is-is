---
title: Ekki var hægt að hreinsa upp bylgju
description: Ekki var hægt að hreinsa upp bylgju
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWaveTable_WHSWaveProcessingDataCleanup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3e5142cf40a6c0d308e8e952bbe17e85b498826d
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924328"
---
# <a name="wave-isnt-eligible-for-cleanup"></a>Ekki var hægt að hreinsa upp bylgju

Villukóði: WaveNotEligibleForCleanup

## <a name="symptoms"></a>Einkenni

Kerfið sýnir eftirfarandi villuboð:

> Ekki er hægt að hreinsa upp bylgju %1.

Ekki er hægt að hreinsa bylgjugögnin.  

## <a name="cause"></a>Orsök

Bylgjan er í vinnslu eins og gefið er til kynna með einu af eftirfarandi skilyrðum:

- Reiturinn **Staða bylgju** er stilltur á *Keyrir*.
- Þegar þú velur **Runuvinnsla** í hópnum **Bylgja** á flipanum **Bylgja** í aðgerðasvæðinu er **Staða** reiturinn ekki stilltur á *Lokið*, *Villa* eða *Hætt við*. Þess vegna er runuvinnsla í keyrslu.

## <a name="resolution"></a>Upplausn

Á Aðgerðasvæði, á flipanum **Bylgja** í **flokknum Bylgja** skal velja **Runuvinnsla** og síðan fylgja einu af eftirfarandi skrefum:

- Ef **Staða** svæðið er stillt á *Keyra*: Á Aðgerðasvæði, á flipanum **Runuvinnsla** í **flokknum Runuvinnsla** skal velja **Skoða verkefni**. Hægt er að fylgjast með framvindunni með því að uppfæra síðuna **Runuverk**.
- Ef **Staða** svæðið er ekki stillt á *Keyra*: Á Aðgerðasvæði, á flipanum **Runuvinnsla** í flokknum **Aðgerðir** skal velja **Breyta stöðu**. Í **Velja nýja stöðu** reitnum skal velja *Í bið*. Veljið síðan **Í lagi**.
