---
title: Ekki er lokað á vinnu
description: Ekki er lokað á vinnu
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d64ab282972e46e8857581b59e5705dd15667328
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924205"
---
# <a name="work-isnt-blocked"></a>Ekki er lokað á vinnu

Villukóði: WHSUnblockNotBlockedWorkErrorMessage

## <a name="symptoms"></a>Einkenni

Kerfið sýnir eftirfarandi villuboð:

> Vinna með kenni %1 er ekki útilokuð.

## <a name="cause"></a>Orsök

Valkosturinn **Lokuð bylgja** á bylgjunni er stilltur á *Nei*. Ekki er hægt að opna vinnuna þar sem hún er ekki lokuð eins og er.

## <a name="resolution"></a>Upplausn

 Aðeins er hægt að opna vinnu þegar valkosturinn **Lokuð bylgja** er stilltur á *Já*.
