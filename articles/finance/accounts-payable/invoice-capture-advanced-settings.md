---
title: Ítarlegar stillingar fyrir reikningsfangalausn
description: Þessi grein veitir upplýsingar um háþróaðar stillingar í reikningsupptökulausninni.
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
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690990"
---
# <a name="invoice-capture-solution-advanced-settings"></a>Ítarlegar stillingar fyrir reikningsfangalausn

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Þessi grein veitir upplýsingar um háþróaðar stillingar í reikningsupptökulausninni.

## <a name="create-additional-connections-for-channels"></a>Búðu til viðbótartengingar fyrir rásir

Þú verður að búa til tengingar við tölvupóst eða skráageymslu til að virkja eftirlit með reikningum sem berast frá mismunandi rásum. Þú verður að skrá tengingar í upphafi til að veita aðgang fyrir sjálfvirk flæði sem notuð eru í lausninni.

Eftirfarandi tengigerðir eru notaðar til að flytja inn reikninga:

- Office 365 Horfur
- Outlook.com
- OneDrive
- SharePoint

Rásin fyrir innflutning reikninga mun nota tengingarnar í frekari stillingarskrefum. Áður en notendur geta búið til rás fyrir tiltekna tengingu, **Stjórnandi** Það verður að veita þeim öryggishlutverk og þeir verða að skapa tengsl.

Til að búa til tengingu við Microsoft Dataverse, fylgdu þessum skrefum.

1. Fara til **Stjórnunarkerfi \> Sjálfgefin lausn**.
2. Veldu **Nýtt**, og veldu síðan **Tengivísun**.
3. Í **Birta nafn** reit, sláðu inn nafn.
4. Veldu **Microsoft Dataverse** sem tengi.
5. Ef þú ert að setja upp tenginguna í fyrsta skipti skaltu velja **Nýtt samband**.
6. Í glugganum sem birtist skaltu búa til a Dataverse tengingu og veldu síðan **Búa til**.
7. Sláðu inn Dataverse reikning og lykilorð.
8. Eftir að staðfesting hefur verið samþykkt, farðu á tengingarsíðuna, veldu **Endurnýja**, veldu reikninginn og veldu síðan **Búa til**.

Fylgdu þessum skrefum til að búa til tölvupósts- eða skráageymslutengingu.

1. Á **Tengingarsköpun** síðu, í **Tengi gerð** reit, veldu **Office 365 Horfur**.
2. Fyrir tölvupósttengingu geturðu valið **Outlook.com** eða **Office 365 Horfur** sem tengi. Fyrir skráageymslutengingu geturðu valið annað hvort **OneDrive** eða **SharePoint**.

Til að skoða núverandi tengingar skaltu fara á **Sjálfgefin lausn \> Hlutir \> Tilvísanir í tengingar**. Notandinn sem býr til rásir ætti að hafa að minnsta kosti eina Dataverse tengingu til viðbótar við sérstakar tölvupóst- eða skráageymslutengingar. Höfundur nýju rásarinnar ætti að vera eigandi tengingarinnar.
