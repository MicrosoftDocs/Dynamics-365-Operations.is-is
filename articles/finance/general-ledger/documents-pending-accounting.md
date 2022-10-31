---
title: Skjöl sem bíða bókhalds
description: Í þessari grein er fjallað um notkun eiginleikans á síðunni „Skjöl sem bíða bókhalds“.
author: ryanCCarlson2
ms.date: 09/02/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: f37d46659b2fc5bf9933719811a7b90cc4e80f52
ms.sourcegitcommit: 6bd8822f7aa781d596b70956bead834117cf302c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/20/2022
ms.locfileid: "9709250"
---
# <a name="documents-pending-accounting"></a>Skjöl sem bíða bókhalds

[!include [banner](../includes/banner.md)]

Í þessari grein er fjallað um notkun eiginleikans á síðunni **„Skjöl sem bíða bókhalds“**.

Eiginleikinn **„Aukin afköst fyrir bókhaldsramma upprunaskjals“** er í boði í Microsoft Dynamics 365 Finance 10.0.30. Þessi eiginleiki bætir bókunarferli skjalabókunar upprunaskjala. Byrjað verður á bókunarferli fyrir reikninga með frjálsum texta.

Þegar kveikt er á þessum eiginleika er bókun undirbókarskjals aðskilin myndun bókhalds eða ferli *færslubókarskráningar* sem myndar heildarupplýsingar bókhalds sem eru fluttar yfir í fjárhag. Dæmi: í bókunarferli reikninga með frjálsum texta er reikningur viðskiptavinar í einingunni **„Viðskiptakröfur“** skráður áður en heildarbókhaldsfærsla er mynduð. Þessi eiginleiki eykur afköst svo hægt sé að skrá reikninga viðskiptavina hraðar á meðan myndun bókhaldsfærslu er seinkað.

Eftirfarandi hnappar eru í boði á síðunni **„Skjöl sem bíða bókhalds“**.

- **Mynda bókhaldsfærslu** – senda skjal sem bíður bókhalds til færslubókarskráningar.
- **Skoða dreifingu** – skoða dreifingu á fjárhagsupphæðum fyrir valið skjal á listanum.
- **Skoða villukladda** – skoða allar villuboðsupplýsingar sem eru til fyrir skjal þar sem bókhaldsstaða gefur til kynna villur. Hægt er að skoða sömu villuboðsupplýsingar með því að velja tengilinn **„Villukladdi“** í skjalalínunni.

Bókhald er myndað með sjálfvirkri bakgrunnsvinnslu sem kallast **„Úrvinnsluhluti bókhaldsramma“**. Frekari upplýsingar um uppsetningu og stillingu allra sjálfvirkra ferla er að finna í [„Sjálfvirkni ferlis“](../../fin-ops-core/dev-itpro/sysadmin/process-automation.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
