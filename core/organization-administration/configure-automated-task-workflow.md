---
title: "Skilgreining á sjálfvirku verki í verkflæði"
description: "Þetta efnisatriði útskýrir hvernig skilgreina á eiginleika sjálfvirks verks."
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 192061
ms.assetid: c0aceb57-b5e6-4ef3-91e7-89a21c9f048a
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 358065dd127703191ba441d0603307a3b7e5df60
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017


---

# <a name="configure-an-automated-task-in-a-workflow"></a>Skilgreining á sjálfvirku verki í verkflæði

[!include[banner](../includes/banner.md)]


Þetta efnisatriði útskýrir hvernig skilgreina á eiginleika sjálfvirks verks.

Til að skilgreina sjálfvirkt verk í verkflæðisritlinum, er hægrismellt á samþykktarskrefið og smellið síðan á **Eiginleika** til að opna í **Eiginleika** síðu. Notið síðan eftirfarandi ferli til að stilla eiginleika fyrir sjálfvirkt verk.

## <a name="name-the-task"></a>Gefa verkinu heiti
Fylgið þessum skrefum til að færa inn heiti á sjálfvirkt verk.

1.  Í vinstri glugganum, smelltu á **grunnstillingar**.
2.  Á svæðinu **Heiti** skal færa inn einkvæmt heiti fyrir verkið.

## <a name="specify-when-notifications-are-sent"></a>Tilgreinið hvenær tilkynningar eru sendar út
Hægt er að senda tilkynningar til fólks þegar sjálfvirkt verk hefur verið keyrt eða hætt við. Fylgið eftirfarandi skrefum til að tilgreina hvenær senda á út tilkynningar og til hvers þær eru sendar.

1.  Á svæðinu vinstra megin, smella á **tilkynningar**.
2.  Veldu gátreitinn sem er við hliðina á tilvikunum sem á að senda tilkynningar vegna.
    -   **Framkvæmd** – Tilkynningar eru sendar þegar verkið hefur verið keyrð.
    -   **Hætt við** – Tilkynningar eru sendar þegar verkið hefur verið hætt við.

3.  Veljið línu fyrir tilvik sem þú valdir í skrefi 2.
4.  Á **tilkynningartexti** flipanum í textareitinn, færa inn texta tilkynningarinnar.
5.  Hægt er að sérsníða tilkynningu með því að færa inn staðgengla. Staðgenglar eru settir í stað viðeigandi gagna þegar tilkynning birtist notendum. Fylgið eftirfarandi skrefum til að færa inn staðgengil:
    1.  Smellið á textahólfið þar sem staðgengillinn á að birtast.
    2.  Smella á **Setja inn staðgengil**
    3.  Í listanum sem birtist skal velja staðgengilinn til að setja inn.
    4.  Smellt er á **Setja inn**.

6.  Til að bæta þýðingum við Tilkynningar skal fylgja þessum skrefum:
    1.  Smellt er á **Þýðingar**.
    2.  Á síðunni sem birtist er smellt á **bæta við**.
    3.  Í listanum sem birtist skal velja tungumálið sem verið er að færa inn í textanum.
    4.  Í svæðið **þýddur texti** skal færa inn textann.
    5.  Til að sérsníða textann geturðu sett inn staðgengla eins og lýst er í skrefi 5.
    6.  Smellið á **Loka**.

7.  Á **Viðtakanda** flipanum, tilgreinið hverjum tilkynningar eru sendar. Veljið einn af valkostum í eftirfarandi töflu, og fylgið svo viðbótarskref fyrir valkostinn áður en farið er í skrefi 8.
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Valkostur</th>
    <th>Viðtakendur tilkynninga.</th>
    <th>Viðbótarskref</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Þátttakendur</td>
    <td>Notendur sem tilheyra tilteknum hópi eða hlutverki</td>
    <td><ol>
    <li>Eftor að þú velur <strong>viðtakanda</strong>, Á flipanum <strong>Hlutverkamiðað</strong> , á listanum <strong>Gerð þátttakanda</strong> skal velja gerð hóps eða hlutverks til að senda tilkynningu á.</li>
    <li>Í listanum <strong>Þátttakanda</strong> skal velja hópi eða hlutverk til að senda tilkynningar til.</li>
    </ol></td>
    </tr>
    <tr class="even">
    <td>Verkflæðisnotandi</td>
    <td>Notendur sem taka þátt í núverandi verkflæði</td>
    <td><ul>
    <li>Eftir að þú velur <strong>verkflæðisnotandi</strong>, á <strong>verkflæðisnotandi</strong> flipanum, á <strong>verkflæðisnotandi</strong> listanum, veldu notandann sem tekur þátt í verkflæði.</li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td>Notandi</td>
    <td>Tilteknir notendur Microsoft Dynamics 365 for Operations</td>
    <td><ol>
    <li>Eftir að þú velur <strong>Notanda</strong>, skal smellið á <strong>Notanda</strong> flipa.</li>
    <li><strong>Tiltækir notendur</strong>: listinn inniheldur alla notendur í Dynamics 365 for Operations. Veldu Notendur til að senda tilkynningar til, og færðu síðan þessa notendur í <strong>Valdir notendur</strong> lista.</li>
    </ol></td>
    </tr>
    </tbody>
    </table>

8.  Endurtakið skref 3 til 7 hvert tilvik sem valin var í skrefi 2.




