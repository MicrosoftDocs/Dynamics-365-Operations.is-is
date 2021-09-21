---
title: Ekki er hægt að færa númeraplötu ef auð úthreyfing og auð innhreyfing eru leyfðar
description: Þú getur ekki fært númeraplötu ef raðnúmerið er með auða úthreyfingu og auða innhreyfingu leyfðar. Þetta verður lagað með því að gera reit raðnúmers valfrjálsan.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 0047f79aa417c8fc910447505f07963d014f54e7
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476652"
---
# <a name="cant-move-license-plate-if-serial-number-has-blank-issue-and-blank-receipt-allowed"></a>Ekki er hægt að færa númeraplötu ef raðnúmer er með auða úthreyfingu og auða innhreyfingu leyfðar

## <a name="symptoms"></a>Einkenni

Ekki er hægt að færa númeraplötu með því að nota valmyndaratriðið **Hreyfing** ef raðnúmerið er með stillingar fyrir *Auð úthreyfing heimil* og *Auð innhreyfing heimil* í rakningarvíddaflokki, og ef margar númeraplötur eru á sömu staðsetningu þar sem sumar eru með raðnúmer og sumar þeirra ekki.

## <a name="resolution"></a>Lausn

Þetta vandamál verður lagfært með breytingum sem eru virkjaðar í [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687). Þessar breytingar gera reitinn **Raðnúmer** valfrjálsan þegar auð kvittun og auðir reitir eru leyfð.
