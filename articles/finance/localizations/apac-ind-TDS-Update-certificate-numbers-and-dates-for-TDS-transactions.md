---
title: Uppfæra númer og dagsetningar vottorða fyrir TDS-færslur
description: Í þessu efnisatriði er útskýrt hvernig á að uppfæra endurheimtanleg vottorðanúmer og dagsetningar sem voru skráðar fyrir lánardrottin, viðskiptavin og fjárhagslykil fyrir skatt sem dreginn er frá í upphafi (TDS).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 248de8e12703a84482b67d0899857a6efb33531c
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023324"
---
# <a name="update-certificate-numbers-and-dates-for-tds-transactions"></a>Uppfæra númer og dagsetningar vottorða fyrir TDS-færslur

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er útskýrt hvernig á að uppfæra endurheimtanleg vottorðanúmer og dagsetningar sem voru skráðar fyrir lánardrottin, viðskiptavin og fjárhagslykil fyrir skatt sem dreginn er frá í upphafi (TDS). Hægt er að skoða vottorðin fyrir TDS-færslur á síðunni **Endurheimtanleg vottorð**. Hægt er að uppfæra vottorðin með því að nota síðuna **Uppfæra vottorð**.

Fylgið þessum skrefum til að uppfæra vottorðanúmerin og dagsetningarnar fyrir TDS-færslur.

1. Farið í **Skattur \> Skattskýrslur \> Staðgreiðsluskattur \> Uppfæra vottorð**.

    [![Síða vottorðauppfærslu](./media/apac-ind-TDS-45.png)](./media/apac-ind-TDS-45.png)

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

    [![Færslusíða vottorðs](./media/apac-ind-TDS-46.png)](./media/apac-ind-TDS-46.png)
