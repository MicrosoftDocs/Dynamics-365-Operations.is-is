---
title: Samstilla gjöld innan samstæðu
description: Þetta efnisatriði útskýrir samstillingu samstæðugjalda
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 2c7f60786743cf750b2bb17ccc0dadf71d859766
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/03/2022
ms.locfileid: "8678576"
---
# <a name="synchronize-intercompany-charges"></a>Samstilla gjöld innan samstæðu

[!include [banner](../../includes/banner.md)]

Gjöld eru einungis samstillt á milli sölupöntunar samstæðunnar og innkaupapöntunar samstæðunnar og samstilling á sér alltaf stað.

Ef reiturinn **Leyfa breytingar á verði** er valinn í innkaupapöntun samstæðunnar eða sölupöntun samstæðunnar er hægt að bæta gjaldi handvirkt við sölupöntun samstæðunnar eða innkaupapöntun samstæðunnar. Annars er það ekki hægt.

Ef reiturinn **Leyfa breytingar á verði** er ekki valinn í sölupöntun samstæðunnar er ekki hægt að bæta gjaldi handvirkt við sölupöntun samstæðu.

Ef reiturinn **Leyfa breytingar á verði** er ekki valinn í innkaupapöntun samstæðunnar er ekki hægt að bæta gjaldi við innkaupapöntun samstæðu.

Ef reiturinn **Leyfa breytingar á verði** er gerður virkur bæði í innkaupapöntun samstæðunnar og sölupöntun samstæðunnar er hægt að bæta gjöldum handvirkt við báðar pantanir. Þetta getur hinsvegar leitt til þess að mörgum gjöldum er bætt við á rangan hátt.

Til að komast hjá árekstrum af þessu tagi er best að gera það leyfilegt að bæta gjöldum annaðhvort við sölupöntun samstæðunnar eða innkaupapöntun samstæðunnar, en ekki við báðar.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
