---
title: "Skilgreining samþykktarferlis í verkflæði"
description: "Notið eftirfarandi ferli til að stilla eiginleika fyrir samþykktarskref."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195643
ms.assetid: f853f57b-83ae-4fb0-a9fa-06ea3fc34fa1
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: bf3523b2768b197b3c75b9a8490f621eced91a7a
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="configure-an-approval-process-in-a-workflow"></a>Skilgreining samþykktarferlis í verkflæði

[!INCLUDE [banner](../includes/banner.md)]

Notið eftirfarandi ferli til að stilla eiginleika fyrir samþykktarskref.

Til að skilgreina samþykktarferli í verkflæðisritlinum, er hægrismellt á samþykktareiningu og smellið síðan á **Eiginleika** til að opna skjámyndina **Eiginleika**.
Gefa samþykktarferlinu heiti
-------------------------

Fylgið eftirfarandi skrefum til að gefa samþykktarferlinu heiti.
1.  Í vinstri glugganum, smelltu á **grunnstillingar**.
2.  Í reitinn **Heiti** er slegið inn einkvæmt heiti fyrir samþykktarferlið.

## <a name="specify-when-the-system-automatically-acts-on-the-document"></a>Tilgreindu hvenær kerfið bregst sjálfkrafa við vegna skjals
Hægt er að skilgreina kerfið þannig það vinni sjálfkrafa að skjölum sem standast ákveðin skilyrði. Til dæmis, getur kerfið samþykkja kostnaðarskýrslur sem hafa heildarupphæðir sem eru lægri en 100 USD. Fylgið eftirfarandi skrefum til að tilgreina hvenær kerfið grípur til aðgerða vegna skjals.
1.  Í vinstri glugganum, smelltu á **sjálfvirkar aðgerðir**.
2.  Útvíkkið gátreitur **virkja sjálfvirkar aðgerðir** .
3.  Smelltu á **Bæta við Aðgerð**.
4.  Færið inn skilyrði.
5.  Færa inn viðbótarskilyrði ef þess gerist þörf:
6.  Til að sannreyna að skilyrðin sem voru færð hafi verið sett upp rétt, skal ljúka eftirfarandi skrefum:
    1.  Smellið á **Prófun** til að opna **Kanna verkflæðisskilyrði** skjámyndinni.
    2.  Veljið færslu í svæðinu **Villuleita skilyrði** á skjámyndinni.
    3.  Smellið á **Prófun**. Kerfið metur færsluna og ákveður hvort hún standist skilyrði sem þú tiltókst.
    4.  Smelltu á **Í lagi** eða **Hætta við** til að fara aftur síðuna **Eiginleikar**.

7.  Í listanum **ljúka aðgerð sjálfvirkt** skal velja aðgerðina sem kerfið á að grípa til vegna skjalsins.

## <a name="specify-when-notifications-are-sent"></a>Tilgreinið hvenær tilkynningar eru sendar út
Hægt er að senda tilkynningar til fólks þegar skjal hefur verið samþykkt, hafnað, framselja eða stigmagnað, eða þegar beðið hefur verið um breytingu. Fylgið eftirfarandi skrefum til að tilgreina hvenær senda á út tilkynningar og til hvers tilkynningar eru sendar.
1.  Á svæðinu vinstra megin, smella á **tilkynningar**.
2.  Veldu gátreitinn sem er við hliðina á tilvikunum sem á að senda tilkynningar vegna.
    -   **Úthluta** – Úthluta skjalinu til annars notanda til samþykkis.
    -   **Hækka** – Þegar úthlutaður notandi hefur ekki bregðast á skjal í tíminn.
    -   **Samþykkja** – Þegar skjal hefur verið samþykkt.
    -   **Hafna** – Þegar skjali hefur verið hafnað.
    -   **Biðja um breytingu** – úthlutaður notandi hefur beðið um breytingu á skjalinu sem var sent.

3.  Veljið línu fyrir tilvik sem þú valdir í skrefi 2.
4.  Smellið á flipann **Tilkynningartexti**.
5.  Færið inn tilkynningartextann í textareitinn.
6.  Hægt er að sérsníða textann með því að færa inn staðgengla sem skipt verður út fyrir viðeigandi gagna þegar þau birtast notendum. Fylgið eftirfarandi skrefum til að færa inn staðgengil:
    1.  Smella skal á textareit þar sem staðgengillinn á að birtast.
    2.  Smella á **Setja inn staðgengil**
    3.  Í listanum sem birtist skal velja staðgengilinn til að setja inn.
    4.  Smellt er á **Setja inn**.

7.  Til að bæta þýðingum á tilkynningunni við skal smella á **Þýðingar**. Í skjámyndinni sem birtist, skal fylgja þessum skrefum:
    1.  Smellið á **Bæta við**.
    2.  Í listanum sem birtist skal velja tungumálið sem á að færa inn í textanum.
    3.  Í svæðið **þýddur texti** skal færa inn textann.
    4.  Hægt er að sérsníða texta með því að færa inn staðgengla.
    5.  Smellið á **Loka**.

8.  Smellið á flipann **viðtakandi**.
9.  Tilgreinið til hvers tilkynningar eru sendar. Veljið einn af valkostum í eftirfarandi töflu, og fylgið svo viðbótarskref fyrir valkostinn áður en farið er í skrefi 10.

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
    <td><strong>Þátttakendur</strong></td>
    <td>Notendur sem tilheyra tilteknum hópi eða hlutverki</td>
    <td><ol>
    <li>Eftir að <strong>Þáttakandi</strong> er valin, smellið á <strong>byggt á hlutverki</strong> flipa.</li>
    <li>Í listanum <strong>gerð Þátttakanda</strong> skal velja gerð hóps eða hlutverk til að senda tilkynningar til.</li>
    <li>Í listanum <strong>Þátttakanda</strong> skal velja hópi eða hlutverk til að senda tilkynningar til.</li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><strong>Verkflæðisnotandi</strong></td>
    <td>Notendur sem taka þátt í núverandi verkflæði</td>
    <td><ol>
    <li>Eftir að þú velur <strong>Notanda verkflæðis</strong>, skal smellið á <strong>Notanda verkflæðis</strong> flipa.</li>
    <li>Í <strong>verkflæðisnotandi</strong> skal velja notandann sem tekur þátt í verkflæðinu.</li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td><strong>Notandi</strong></td>
    <td>Sértækir notendur Microsoft Dynamics 365 for Finance and Operations</td>
    <td><ol>
    <li>Eftir að þú velur <strong>Notanda</strong>, skal smellið á <strong>Notanda</strong> flipa.</li>
    <li>Listinn <strong>Tiltækir notendur</strong>: inniheldur alla notendur í Microsoft Dynamics 365 for Finance and Operations. Veldu Notendur til að senda tilkynningar til, og færðu síðan þessa notendur í <strong>Valdir notendur</strong>: lista.</li>
    </ol></td>
    </tr>
    </tbody>
    </table>

10. Endurtakið skref 3 til 9 hvert tilvik sem valin var í skrefi 2.

## <a name="specify-a-final-approver"></a>Tilgreina hver endanlegur samþykkjandi er
Gott gæti verið að tilnefna endanlegur samþykkjandi fyrir aðstæður þar sem samþykkjandi er sá sem sendi skjalið til samþykkis. Fylgið eftirfarandi skrefum til að tilgreina endanlegan samþykkjanda.
1.  Í vinstri glugganum, smelltu á **ítarlegar stillingar**.
2.  Veljið gátreitinn **Nota endanlegs samþykkjanda**.
3.  Veljið notandann, sem verður endanlegi samþykkjandinn, af listanum.

## <a name="set-a-time-limit"></a>Setja upp tímamörk
Fylgið eftirfarandi skrefum ef verður að ljúka samþykktarferlinu innan tiltekins tíma.

| **Ábending**                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| Valkostirnir sem valdir í þessum skrefum munu hnekkja valkostunum sem valdir eru á flipunum **Verkefni** og **Hækkun** í hverju samþykktarskrefi. |

1.  Í vinstri glugganum, smelltu á **ítarlegar stillingar**.
2.  Beldu **Stilla tímamörk** **verkflæðiseiningar** gátreitinn.
3.  Í reitnum **tímalengd** tilgreinið þegar samþykktarferli á að vera lokið. Veldu einn af eftirfarandi valkostum:
    -   **Klukkustundir** – færið Inn fjölda klukkustunda sem samþykktarferlið verður að vera lokið. Þá velja dagatalið sem fyrirtækið notar og færa inn upplýsingar um vinnuviku fyrirtækisins.
    -   **Dagar** – færið Inn fjölda klukkustunda sem samþykktarferlið verður að vera lokið. Þá velja dagatalið sem fyrirtækið notar og færa inn upplýsingar um vinnuviku fyrirtækisins.
    -   **Vikur** – færið Inn fjölda klukkustunda sem samþykktarferlið verður að vera lokið.
    -   **Mánuðir** — velja daginn og vikuna sem verður að vera búið að klára samþykktarferlið fyrir. Til dæmis getur samþykktarferlið átt að vera lokið fyrir föstudaginn í þriðju viku mánaðarins.
    -   **Ár** — velja daginn og vikuna sem verður að vera búið að klára samþykktarferlið fyrir. Til dæmis getur samþykktarferlið átt að vera lokið fyrir föstudaginn í þriðju viku desembermánaðar.

4.  Ef farið er yfir tímamörkin mun kerfið grípa til aðgerða vegna skjalsins. Veljið aðgerðina, sem kerfið á að framkvæma, í listanum **Aðgerðir**.

## <a name="specify-which-actions-are-available-to-the-user"></a>Tilgreina hvaða aðgerðir verða tiltækar notandanum.
Þegar notandi fær skjal úthlutað til samþykktar verður hann að vinna í skjalinu. Fylgið eftirfarandi skrefum til að tilgreina hvaða aðgerðir notandi getur gripið til vegna skjalsins sem lagt var fyrir.
1.  Í vinstri glugganum, smelltu á **ítarlegar stillingar**.
2.  Veljið gátreitinn **Samþykkja** ef notendur eiga að geta samþykkt skjöl.
3.  Veljið gátreitinn **hafna** ef notendur eiga að geta hafnað skjöl.
4.  Veljið gátreitinn **Breytingabeiðni** ef notendur eiga að geta beðið um breytingar á skjölum.
5.  Veljið gátreitinn **framselja** ef notandinn á að geta framselt skjalinu til annars notanda.

**Athugasemd**: **Heimila aðgerðir úr verklistanum í Enterprise Portal** gátreitur er úreltur.

## <a name="configure-the-approval-steps"></a>Skilgreining samþykktarskrefs
Samþykktarferli samanstendur af samþykktarskref. Ljúktu við eftirfarandi ferli til að bæta skrefum samþykktarferlið og skilgreina skrefum.
1.  Tvísmellið samþykktarferlið í ritill verkflæðis. Verkflæðisritlinum birtir skref í samþykktarferlinu.
2.  Til að bæta við samþykktarskrefi, draga skrefið í **verkflæðiseiningar** á vinnusvæði.
3.  Til að skilgreina samþykktarskref, sjá [Skilgreina samþykktarskref](configure-approval-step-workflow.md).






