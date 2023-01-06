---
title: Ítarlegar stillingar Invoice capture-lausnar
description: Þessi grein veitir upplýsingar um ítarlegar stillingar í Invoice capture-lausninni.
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: a1e24b700d0f30fd90f2619dd6e6687736a86774
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690990"
---
# <a name="invoice-capture-solution-advanced-settings"></a>Ítarlegar stillingar Invoice capture-lausnar

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Þessi grein veitir upplýsingar um ítarlegar stillingar í Invoice capture-lausninni.

## <a name="create-additional-connections-for-channels"></a>Búa til fleiri tengingar fyrir rásir

Þú verður að búa til tengingar við tölvupóst eða geymslu skráa til að hægt sé að fylgjast með innkomnum reikningum frá mismunandi rásum. Þú verður að skrá tengingar í upphafi til að veita aðgang að sjálfvirku flæði sem er notað í lausninni.

Eftirfarandi tengitegundir eru notaðar til að flytja inn reikninga:

- Office 365 Outlook
- Outlook.com
- OneDrive
- SharePoint

Rásin til að flytja inn reikning mun nota tengingarnar í frekari stillingarskrefum. Áður en notendur geta búið til rás af tiltekinni tengingu verður að veita þeim öryggishlutverkið **Stjórnandi** og þeir verða að búa til tengingar.

Fylgdu þessum skrefum til að stofna tengingu við Microsoft Dataverse.

1. Farðu í **Kerfi stjórnanda \> Sjálfgefin lausn**.
2. Smelltu á **Nýtt** og veldu síðan **Tilvísun tengingar**.
3. Í reitinn **Birtingarheiti** skal færa inn heiti.
4. Veldu **Microsoft Dataverse** sem tengilinn.
5. Ef verið er að setja upp tengingu í fyrsta skipti skal velja **Ný tenging**.
6. Í svarglugganum sem birtist skal búa til Dataverse tengingu og síðan velja **Búa til**.
7. Sláðu inn Dataverse reikninginn og aðgangsorðið.
8. Eftir að staðfesting er í lagi skal fara á tengisíðuna, velja **Uppfæra**, velja lykilinn og síðan velja **Búa til**.

Til að stofna tengingu við tölvupóst eða skráageymslu skal fylgja leiðbeiningunum hér að neðan.

1. Á síðunni **Stofnun tengingar**, í reitnum **Tegund tengingar**, skal velja **Office 365 Outlook**.
2. Fyrir tengingu tölvupósts er hægt að velja **Outlook.com** eða **Office 365 Outlook** sem tengingu. Fyrir tengingu skráageymslu er hægt að velja annaðhvort **OneDrive** eða **SharePoint**.

Til að fara yfir núverandi tengingar skal fara í **Sjálfgefin lausn\> Hlutir \> Tilvísanir í tengingar**. Notandinn sem býr til rásir ætti að hafa að minnsta kosti eina Dataverse tengingu til viðbótar við tilteknar tengingar fyrir tölvupóst eða skráargeymslu. Sá sem bjó til nýju rásina ætti að vera eigandi tengingarinnar.
