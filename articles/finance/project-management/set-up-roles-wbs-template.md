---
title: Setja upp hlutverk á sniðmátum fyrir sundurliðun verkþátta
description: Í þessu efnisatriði er að finna upplýsingar um hvernig á að setja upp hlutverkaupplýsingar fyrir sniðmát fyrir sundurliðun verkþátta.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5dfb429eae933ba4d687ec4cbd417d2f78308e47
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760576"
---
# <a name="set-up-roles-on-work-breakdown-structure-templates"></a>Setja upp hlutverk á sniðmátum fyrir sundurliðun verkþátta

[!include [banner](../includes/banner.md)]

Verkefnisstjórar geta sett upp WBS-sniðmát fyrir sundurliðun verkþátta sem hægt er að nota þegar þeir stofna WBS fyrir ný verk. Verkefnisstjórar geta bætt við hlutverkum þegar sniðmát er stofnað. Notið eftirfarandi ferli til að úthluta hlutverki til WBS-sniðmáts.

1. Veljið **Verkefnastjórnun og bókhald** > **Uppsetning** > **Verk** > **Sniðmát fyrir sundurliðun verkþátta**.
2. Veljið **Upplýsingar** fyrir valið WBS-sniðmát.
3. Velja verk í lista og síðan, í svæðinu **Hlutverk** skal velja hlutverk til að úthluta á verkefnið.

## <a name="work-with-a-wbs"></a>Vinna með WBS

Hægt er að stofna nýtt WBS eða afrita WBS úr fyrirliggjandi WBS-sniðmáti. Stjórnandi verks getur auðveldlega stjórnað tilföngum með því að úthluta hlutverkum á ný verk í WBS. Hægt er að skipta út hlutverkum eftir að tilfang er fengið eða eftir að staðfest tilfang sem á að vinna við verkið er auðkennt. Þessi sveigjanleika gerir verkefnisstjórum kleift að framkvæma eftirfarandi verkefni:

- Auðkennið fjölda tilfanga sem þarf fyrir WBS vinnupakka.
- Áætla kostnað verks.
- Stofna bráðabirgðafjárhagsáætlun.
- Meta tímalengd verkþáttar, sem byggir á hlutverkum og tilföngum.
- Þróa einhverjar verkstjórnunaráætlanir, byggt á upplýsingum um tiltæk verk.

Auka valkostum hefur verið bætt í WBS til að nýta betur virkni tilfanga.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valkostur</th>
<th>Lýsing</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Úthlutanir tilfanga</td>
<td>Skoða úthlutuð tilföng, dagsetningar, tímafjölda og bókunargerð fyrir verk í WBS.</td>
</tr>
<tr class="even">
<td>Mynda lið sjálfkrafa</td>
<td>Bæta við áætluðum tilföngum sjálfkrafa með því að nota hlutverk sem eru tengd verkefni. Finance stingur sjálfkrafa upp á áætluðum tilföngum með því að nota greiningu um ákvörðun um mörg skilyrði sem byggir á hlutverkum. Eftir að hlutverk og framlag (klukkustundir) hefur verið stillt fyrir verk í WBS og skipulag hefur verið losað skal velja <strong>Mynda lið sjálfkrafa</strong>. Áskildum fjölda áætlaðra tilfanga er bætt við WBS og flipann <strong>Áætlun Verks og hóps</strong>.</td>
</tr>
<tr class="odd">
<td>Tilföng (fellilisti)</td>
<td>Á síðunni <strong>Ræsa úthlutun tilfanga</strong> er hægt að velja tilföng í bundna bókun eða óbundna bókun, á grundvelli tilgreindrar tímalengdar. Hægt er að breyta stillingum yfirlits til að sjá og stilla tímalengd verkþátta tilfanga. Hægt er að velja og úthluta tilföngum á stigi pakkavinnu með eftirfarandi valkostum:
<ul>
<li><strong>Samþykkja</strong> -Staðfesta breytingar á tilföngum sem er úthlutað á verkefni.</li>
<li><strong>Hætta við</strong> -Hætta við breytingar á tilföngum sem er úthlutað á verkefni.</li>
<li><strong>Úthluta sjálfkrafa</strong> – Þessi valkostur velur tiltæk mönnuð tilföng með samsvarandi hlutverki og úthlutar á valið verk.</li>
</ul></td>
</tr>
</tbody>
</table>

1. Á **Öll verk** síðunni skal velja verkið **XYZ Uppfærsla þrep 2**.
2. Veljið **Áætlun** > **Aðgerðir** > **Sundurliðun verkþátta**.
3. Veljið **Nýtt** til að bæta eftirfarandi verkþætti af stigi eitt við WBS:

    - Verið er að hefja
    - Áætlun
    - Í gangi
    - Eftirlit og stjórn
    - Lok

4. Setja upp dagsetningar og framlag (klukkustundir), eins og sýnt er á eftirfarandi mynd.

    [![Stilla dagsetningar og framlag](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Veljið verklínuna **Hefja** og síðan, í svæðinu **Hlutverk**, veljið **Yfirverkefnastjóri**.
6. Velja **Birta**.
7. Í sömu línu í svæðinu **Tilfang**, veljið **Daniel Goldschmidt** og svo **Samþykkja**.
8. Veljið verklínuna **Áætlanagerð** og síðan, í svæðinu **Hlutverk** veljið **Viðskiptagreinir**.
9. Veljið **Birta**, og smellið síðan á **Mynda lið sjálfkrafa**.
10. Smellt er á **Já** í glugganum sem birtist.
11. Í svæðinu **Tilfang** skal staðfesta að gildið sé **Viðskiptagreinir 1**.
12. Fyrir tilfangið **Viðskiptagreinir 1**, opnið uppflettingu og veljið **Ræsa skjámynd úthlutana**. Til að velja starfskraft fyrir verkið.
13. Veljið **Óbundnar úthlutanir** &gt; **Full afkastageta**.

    > [!NOTE] 
    > Það berst ekki viðvörun um að tilgreind viðföng séu nú 2, þar sem fjöldi tilfanga helst 1.

14. Á síðunni **Sundurliðun Verkþátta** skal staðfesta úthlutun tilfanga á WBS og velja svo **Vista**.
