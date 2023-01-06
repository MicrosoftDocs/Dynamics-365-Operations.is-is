---
title: Vinnur úr mótteknum rafrænum skjölum
description: Þessi grein veitir yfirlit yfir vinnslu rafræna skjala á innleið.
author: gionoder
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 554bc8fde3b2135eb878d885541c76ecd6d66493
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277302"
---
# <a name="processing-of-incoming-electronic-documents"></a>Vinnur úr mótteknum rafrænum skjölum

[!include [banner](../includes/banner.md)]

Innkomin rafræn skjöl, svo sem rafræna reikningar söluaðila, er hægt að flytja inn og vinna með á tvennan hátt:

- Skrár eru sóttar af ytri rásum og sendar beint til tengdra forrita. Þar fara þær í frekari umbreytingu og eru svo fluttar inn í gagnagrunninn.
- Skrár fara í gegnum forvinnslu í þjónustu Rafrænnar Reikningagerðar og berast þá til tengds forrits.

Rafrænn reikningur styður tvær rásir fyrir móttekin skjöl: tölvupóst og Microsoft SharePoint möppur.

Til að tilgreina hvort skjöl fara í forvinnslu eða berast beint í tengda forritið þitt:

- **Gagnarás** – Kerfið mun senda skjalið beint til tengda forritsins.
- **Gagnarás með pípuvinnslu** – Hægt er að setja upp fleiri aðgerðir sem verða keyrðar áður en skjalið er sent til tengda forritsins.

Til að fá upplýsingar um hvernig á að setja upp aðstæður fyrir vinnslu á rafrænum skjölum á innleið fyrir mismunandi rásir, sjá [Skilgreina tölvupóstsrás](e-invoicing-configure-email.md) og [Skilgreina SharePoint-rás](e-invoicing-configure-sharepoint-channel.md).
