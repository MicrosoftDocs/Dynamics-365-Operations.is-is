---
title: Skrá endurheimtanlegt vottorðanúmer TDS
description: Þessi grein útskýrir hvernig á að nota síðuna Endurheimtanleg vottorð til að skrá vottorðsnúmer og dagsetningar fyrir skatta sem eru dregin frá uppruna (TDS) vottorð sem eru móttekin fyrir tiltekinn lánardrottinn, viðskiptamann eða höfuðbók.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 513412e292167795fad9d80b68e6e5e14dbd13c5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853257"
---
# <a name="record-tds-recoverable-certificate-numbers"></a>Skrá endurheimtanlegt vottorðanúmer TDS

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir hvernig á að nota **Endurheimtanleg vottorð** síðu til að skrá vottorðanúmer og dagsetningar fyrir TDS-vottorð (Tax Deducted at Source) sem eru móttekin fyrir tiltekinn lánardrottinn, viðskiptamann eða höfuðbók. Til að uppfæra vottorðanúmer og dagsetningar TDS sem er skráð fyrir TDS-færslur á þessari síðu skal nota síðuna **Uppfæra vottorð** (**Fjárhagur \> Reglubundið \> Staðgreiðsluskattur \> Uppfæra vottorð**). Þegar búið er að uppfæra númer TDS-vottorða skal loka þeim.

Fylgið þessum skrefum til að skrá númer og dagsetningar TDS-vottorða.

1. Opnið **Skattur \> Óbeinn skattur \> Staðgreiðsluskattur \> Endurheimtanleg vottorð**.

    [![Síða endurheimtanlegra vottorða.](./media/apac-ind-TDS-49.png)](./media/apac-ind-TDS-49.png) 

2. Á síðunni **Endurheimtanleg vottorð**, í reitnum **Skattgerð**, skal velja **TDS**.
3. Veljið **Ný** til að stofna nýja skrá.
4. Í reitnum **Númer vottorðs** skal færa inn númer TDS-vottorðs.
5. Í reitnum **Lykilgerð** skal velja gerð lykils sem TDS-vottorð er móttekið fyrir: **Lánardrottinn**, **Viðskiptavinur** eða **Fjárhagur**.
6. Í reitnum **Lykill** skal velja númer lánardrottna-, viðskiptavina- eða fjárhagslykils eftir því hvaða gerð lykils er valin. Reiturinn **Heiti** sýnir heiti lánardrottna-, viðskiptavina- eða fjárhagslykils.
7. Í reitinn **Upphæð vottorðs** skal færa inn upphæð TDS-vottorðs.
8. Í reitinn **Dagsetning** skal færa inn dagsetningu vottorðs fyrir númer vottorðs.
9. Veljið **Fyrirspurnir** til að opna síðuna **Færslur vottorðs** þar sem hægt er að skoða TDS-færslurnar sem númer og dagsetning TDS-vottorðs eru uppfærð fyrir. Þessar upplýsingar er hægt að uppfæra á síðunni **Uppfæra vottorð** (**Skattur \> Skattskýrslur \> Staðgreiðsluskattur \> Uppfæra vottorð**).

    Síðan **Uppfæra vottorð** sýnir eftirfarandi upplýsingar fyrir hverja TDS-færslu:

    - **Dagsetning** – Bókunardagsetning TDS-færslunnar.
    - **Fylgiskjal** – Fylgiskjalsnúmer TDS-færslunnar.
    - **Uppruni** – Einingin sem TDS-færslan var stofnuð í.
    - **Lykill** – Númer lánardrottna-, viðskiptavina- eða fjárhagslykils sem TDS-færslan var stofnuð fyrir.
    - **Heiti** – Heiti lánardrottna-, viðskiptavina- eða fjárhagslykils sem TDS-færslan var stofnuð fyrir.
    - **Upphæð** – Upphæð reiknings sem TDS var reiknað fyrir.
    - **Skattupphæð** – TDS-skattupphæð sem reiknuð var fyrir færsluna.
    - **Dagsetning vottorðs** – Dagsetning TDS-vottorðs sem var uppfært fyrir TDS-færsluna.
    - **Númer vottorðs** – Númer TDS-vottorðs sem var uppfært fyrir TDS-færsluna.

10. Á síðunni **Endurheimtanleg vottorð** skal velja gátreitinn **Lokað** til að loka númeri TDS-vottorðs þegar búið er að uppfæra það fyrir TDS-færslur á síðunni **Uppfæra vottorð**.

    Til að velja gátreitinn **Lokað** fyrir allar færslur á síðunni skal velja **Merkja allt**.

    > [!NOTE]
    > Númer TDS-vottorða sem gátreiturinn **Lokað** er valinn fyrir eru ekki í boði á síðunni **Uppfæra vottorð**.
