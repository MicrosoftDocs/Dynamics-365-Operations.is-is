---
title: Vandamál við umreikning gjaldmiðils í verðsamningi
description: Verð verðsamninga eru ekki endurreiknuð samkvæmt gjaldmiðlinum þegar gjaldmiðillinn er annar í innkaupapöntun
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 1b6dc36c5f5ee6b611eebd81f378399ce1748c63
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476624"
---
# <a name="trade-agreement-currency-conversion-issues"></a>Vandamál við umreikning gjaldmiðils í verðsamningi

## <a name="symptoms"></a>Einkenni

Verð verðsamninga eru ekki endurreiknuð samkvæmt gjaldmiðlinum þegar gjaldmiðillinn er annar í innkaupapöntun.

## <a name="resolution"></a>Lausn

Eiginleikinn *Almennur gjaldmiðill* gerir kleift að skilgreina verð og afslætti í aðeins einum gjaldmiðli. Síðan er hægt að umbreyta í aðra gjaldmiðla eftir því sem þörf er á. Þegar búið er að framkvæma umreikninginn getur eiginleikinn sjálfkrafa notað snjallverðsléttun.
