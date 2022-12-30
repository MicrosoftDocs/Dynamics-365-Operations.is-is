---
title: Samstilla gjöld innan samstæðu
description: Þessi grein útskýrir samstillingu samstæðugjalda
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
ms.openlocfilehash: e7b3de3d7da7be6c1c8b5c3842862e7bccd78277
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857287"
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
