---
title: Úrræðaleit fyrir vöruhúsaaðgerðir á útleið
description: Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með innkaupapantanir i Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 56bd91d8a6fe895317021d806e180df3a2db302b
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645452"
---
# <a name="troubleshoot-outbound-warehouse-operations"></a>Úrræðaleit fyrir vöruhúsaaðgerðir á útleið

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með innkaupapantanir i Microsoft Dynamics 365 Supply Chain Management.

## <a name="i-receive-the-following-error-message-sales-order-could-not-be-released"></a>Ég fékk eftirfarandi villuboð: Ekki var hægt að losa sölupöntun.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Þetta vandamál getur komið upp af ýmsum ástæðum. Til dæmis, pöntunin er í lánastýringarbið og ekki er hægt að stofna sendingar fyrr en gilt póstfang er fært inn fyrir allar sölulínur sem tengjast sölupöntun. Að öðrum kosti er pöntunarbið sem þarf að leysa áður en hægt er að losa pöntunina í vöruhúsið. Þessi bið gæti verið bundin við pöntunina eða hún kann að vera á viðskiptavinalykli.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Bæta við eða uppfæra aðsetur á sölupöntunum og pöntunarlínunum og losa svo pöntunina í vöruhúsið. Aðeins er hægt að losa pantanir í vöruhúsið ef þær hafa gilt afhendingaraðsetur (samkvæmt uppsetningu á sniði aðseturs í einingunni **Fyrirtækisstjórnun**).

Rannsaka pöntun í bið og leysa vandamálið. Taktu síðan biðina af pöntuninni eða viðskiptavininum og losaðu pöntunina í vöruhúsið.

## <a name="i-receive-the-following-message-the-shipment-for-load-1-has-been-confirmed-however-no-lines-are-posted"></a>Ég fæ eftirfarandi skilaboð: „Sending á farmi 1% hefur verið staðfest“. Hins vegar eru engar línur bókaðar.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Sending í farmi var staðfest en engin frekari bókun fór fram.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Staðfesting sendingar hefur ekki áhrif á bókun. Þetta uppfærir bara sendingu og hleðslustöðu. Bókun verður að eiga sér stað í aðgreindu ferli.

## <a name="i-receive-the-following-error-message-direct-delivery-is-not-able-to-process-for-warehouse-1-as-it-has-warehouse-management-enabled-please-specify-another-warehouse-that-is-not-enabled-for-warehouse-management"></a>Ég fæ eftirfarandi villuboð: „Ekki er hægt að vinna úr beinni afhendingu fyrir vöruhús 1% því vöruhúsakerfi er virkt. Tilgreinið annað vöruhús sem er ekki virkt fyrir vöruhúsastjórnun.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Vöru er bætt við sölulínu fyrir beina afhendingu úr vöruhúsi þar sem vöruhúsakerfi (WMS) er virkt. Þessi villuboð birtast þegar sölulína er uppfærð. 

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Microsoft hefur metið þetta mál og hefur ákvarðað að þetta sé takmörkun eiginleika. Sem stendur styður vöruhúsakerfi ekki beina afhendingu. Til að nota beina afhendingu skal því velja vöru sem er ekki WMS og vöruhús.
