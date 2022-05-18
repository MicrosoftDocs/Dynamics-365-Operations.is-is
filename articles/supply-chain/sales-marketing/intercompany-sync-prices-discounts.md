---
title: Samstilla verð og afslætti innan samstæðu
description: Þetta efnisatriði útskýrir samstillingu verða og afslátta fyrir samstæðusölupantanir og samstæðuinnkaupapantanir
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
ms.openlocfilehash: 90fa2244b5947c37b8498d1c70cddf894979f931
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/03/2022
ms.locfileid: "8673635"
---
# <a name="synchronize-intercompany-prices-and-discounts"></a>Samstilla verð og afslætti innan samstæðu

[!include [banner](../../includes/banner.md)]

Afslættir og verð eru alltaf samstillt á milli innkaupapöntunar samstæðu og sölupöntun samstæðu. Það er einnig hægt að samstilla verð og afslætti við og frá upprunalegri sölupöntun svo allar sölupantanir hafi sömu verð og afslætti. Þetta er gert af síðunni **Innan samstæðu** sem er opnuð í flipanum **Almennt** á listasíðunni **Allir viðskiptavinir** - annaðhvort í **Sala og markaðssetning** eða í **Innkaup og aðföng**.

Reiturinn **Verð og afsláttur** er samstilltur við samstæðusölupöntunarlínuna. Það þýðir að með því að velja reitinn **Leyfa breytingar á verði** og reitinn **Leyfa breytingar á afslætti** hefur breyting á milli sölupöntunar innan samstæðu og innkaupapöntunar innan samstæðu verið leyfð. Breyting á einingaverði, verðeiningu eða gjöldum sölunnar á sölupöntun innan samstæðu ákvarðar verðið á innkaupapöntunarlínu innan samstæðu.

Ef reiturinn **Leyfa breytingar á verði** og reiturinn **Leyfa breytingar á afslætti** eru virkjaðir í sölupöntun innan samstæðu eða innkaupapöntun innan samstæðu, er hægt að breyta verði eða afslætti handvirkt í öðru hvoru. Annars er það ekki hægt.

Ef reitirnir **Leyfa breytingar á verði** og **Leyfa breytingar á afslætti** eru ekki virkjaðir í sölupöntun innan samstæðu, er ekki hægt að gera breytingar á verðinu handvirkt (eða ýmsum gjöldum) eða á afslætti í sölupöntun innan samstæðu.

Ef reitirnir **Leyfa breytingar á verði** og **Leyfa breytingar á afslætti** eru ekki virkjaðir í innkaupapöntun innan samstæðu, er ekki hægt að gera breytingar á verðinu handvirkt (eða ýmsum gjöldum) eða á afslætti í innkaupapöntun innan samstæðu.

Ef reitirnir **Leyfa breytingar á verði** og **Leyfa breytingar á afslætti** eru gerðir virkir bæði í innkaupapöntun samstæðunnar og sölupöntun samstæðunnar er hægt að handvirkar breytingar á báðum pöntunum. Þetta getur hinsvegar leitt til aðstæðna þar sem uppfærslur sem einstaklingur gerir verði hnekkt af uppfærslum sem annar einstaklingur gerir í öðru fyrirtæki á sömu pöntuninni.

> [!NOTE]
> Ef svæðið **Verð og afsláttur** er virkjað, bæði á sölupöntun og innkaupapöntun innan samstæðu, þá hefur starfsmaður ekki stjórn á verðlagningunni.

Til að koma í veg fyrir slíka árekstra, er besta leiðin að leyfa einungis breytingar á verðum og afsláttum í sölupöntunum innan samstæðu eða innkaupapöntunum innan samstæðu. Þetta næst með því að virkja reitina **Leyfa breytingar á verði** og **Leyfa breytingar á afslætti** í annarri þessara pantana.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
