---
title: Kerfið finnur ekki fyrirhugaða pöntun meðan á aðgerðum stendur á mörgum pöntunum
description: Villa "Áætluð pöntun er ekki til" kemur upp þegar þú framkvæmir aðgerðir á mörgum áætlunarpöntunum og að minnsta kosti tvær pantanir tilheyra sama vöruauðkenni.
author: t-benebo
ms.date: 12/07/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo_ReqTransPoMarkChangeType
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-12-07
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 0ece4a331b63b86e896c5b337a58185ed3ea1049
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920854"
---
# <a name="the-system-cant-find-a-planned-order-during-operations-on-multiple-orders"></a>Kerfið finnur ekki fyrirhugaða pöntun meðan á aðgerðum stendur á mörgum pöntunum

Villukóði SYS24774

## <a name="symptoms"></a>Einkenni

Þú færð eftirfarandi villuboð þegar þú reynir að framkvæma aðgerð á mörgum skipulögðum pöntunum á sama tíma og að minnsta kosti tvær af pöntunum tilheyra sama vöruauðkenni. Til dæmis gæti villa komið fram þegar pantanir eru staðfestar eða pöntunargerð þeirra er breytt.

> Tillaga %1 er ekki til.

## <a name="cause"></a>Orsök

Þegar kerfið staðfestir eða breytir gerð pöntunar verður það að endurskoða fyrirliggjandi áætlaðar pantanir fyrir vöruna til að ganga úr skugga um að áætlað framboð passi við eftirspurn og núverandi framboð. Sem hluti af þessu ferli endurskapar kerfið áætlaðar pantanir fyrir vöruna. Því er önnur skipulögð pöntunin sem kerfið gerir ráð fyrir að vinna ekki lengur til.

## <a name="workaround"></a>Hjáleið

Samþykktu pantanir áður en þú afgreiðir þær. Þannig verður pöntunum ekki eytt þegar kerfið vinnur úr fyrstu pöntun vörunnar.
