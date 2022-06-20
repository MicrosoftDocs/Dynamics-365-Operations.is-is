---
title: Uppfæra númer og dagsetningar vottorða fyrir TDS-færslur
description: Þessi grein útskýrir hvernig á að uppfæra endurheimtanlegt skírteinisnúmer og dagsetningar sem voru skráðar fyrir lánardrottna-, viðskiptamanna- og fjárhagsreikninga fyrir frádráttarskatt frá uppruna (TDS).
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
ms.openlocfilehash: 147a27261a4a282550f0bacede78c9edd38b4fe6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904442"
---
# <a name="update-certificate-numbers-and-dates-for-tds-transactions"></a>Uppfæra númer og dagsetningar vottorða fyrir TDS-færslur

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir hvernig á að uppfæra endurheimtanlegt skírteinisnúmer og dagsetningar sem voru skráðar fyrir lánardrottna-, viðskiptamanna- og fjárhagsreikninga fyrir frádráttarskatt frá uppruna (TDS). Hægt er að skoða vottorðin fyrir TDS-færslur á síðunni **Endurheimtanleg vottorð**. Hægt er að uppfæra vottorðin með því að nota síðuna **Uppfæra vottorð**.

Fylgið þessum skrefum til að uppfæra vottorðanúmerin og dagsetningarnar fyrir TDS-færslur.

1. Farið í **Skattur \> Skattskýrslur \> Staðgreiðsluskattur \> Uppfæra vottorð**.

    [![Síða vottorðauppfærslu.](./media/apac-ind-TDS-45.png)](./media/apac-ind-TDS-45.png)

2. Á síðunni **Uppfæra vottorð**, í hlutanum **Velja**, í reitnum **Skattgerð**, skal velja **TDS**.
3. Í reitnum **Vottorðanúmer** skal velja TDS-vottorðanúmer viðskiptavinar eða lánardrottins.

    > [!NOTE]
    > Reiturinn **Númer vottorðs** sýnir aðeins TDS-vottorðanúmer sem gátreiturinn **Lokað** er hreinsaður fyrir á síðunni **Endurheimtanleg vottorð**.

    Reiturinn **Dagsetning vottorðs** sýnir dagsetningu vottorðsins. Reiturinn **Gerð lykils** sýnir gerð lykilsins sem TDS-vottorðanúmerið er móttekið fyrir and reiturinn **Heiti** sýnir heiti lykilsins.

5. Í reitunum **Frá dagsetningu** og **Til dagsetningar** skal velja upphafs- og lokadagsetningar tímabilsins til að sýna TDS-færslur fyrir.
6. Veljið **Sýna gögn** til að skoða TDS-færslur sem voru bókaðar á völdu tímabili.

    Í flipanum **Yfirlit** sýnir hnitanetið í efri rúðunni eftirfarandi upplýsingar um hverja TDS-færslu sem var bókuð fyrir lánardrottin eða viðskiptavin á völdu tímabili:

    - **Fylgiskjal** – Fylgiskjalsnúmer TDS-færslunnar.
    - **Dagsetning** – Dagsetning TDS-færslunnar.
    - **Upphæð** – Upphæð reiknings sem TDS var reiknað fyrir.
    - **Skattupphæð** – TDS-skattupphæð sem reiknuð var fyrir færsluna.

7. Til að færa tilteknar TDS-færslur úr efra hnitanetinu og yfir í neðra hnitanetið skal velja færslurnar og síðan velja **Hafa með**. Að öðrum kosti skal velja **Taka allt með** til að færa allar TDS-færslur úr efra hnitanetinu og yfir í neðra hnitanetið.

    Til að færa tilteknar TDS-færslur eða allar TDS-færslur úr neðra hnitanetinu og yfir í efra hnitanetið skal nota hnappinn **Útiloka** eða **Útiloka allt**.

8. Veljið **Uppfæra** til að uppfæra reitina **Númer vottorðs** og **Dagsetning vottorðs** fyrir TDS-færslur í neðra hnitanetinu.
10. Farið í **Skattur \> Óbeinir skattar \> Staðgreiðsluskattur \> Endurheimtanlegt vottorð** og veljið **Fyrirspurn** til að skoða uppfærðar færslulínur sem eru með nýju vottorðanúmerin á síðunni **Vottorðafærslur**.

    [![Færslusíða vottorðs.](./media/apac-ind-TDS-46.png)](./media/apac-ind-TDS-46.png)
