---
title: Setjið upp og keyrið vinnslu til að kalla á einfalt útflutningssnið rafrænnar skýrslugerðar til að búa til Excel-skýrslu
description: Þessi grein gefur dæmi sem sýnir hvernig á að setja upp og nota rafræn skilaboð.
author: AdamTrukawka
ms.date: 07/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.21
ms.custom: ''
ms.search.form: ''
ms.openlocfilehash: 6090c45a98b672f718f89fc1d2e1c060498bb8a0
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279335"
---
# <a name="set-up-and-run-processing-to-call-a-simple-exporting-er-format-to-generate-an-excel-report"></a>Setjið upp og keyrið vinnslu til að kalla á einfalt útflutningssnið rafrænnar skýrslugerðar til að búa til Excel-skýrslu

[!include [banner](../includes/banner.md)]

Eftir að snið rafrænnar skýrslugerðar hefur verið stofnað, því varpað í gagnaveitur og því lokið, er hægt að keyra það með af vinnusvæðinu **Rafræn skýrslugerð**. Eftir að skýrslan hefur verið búin til er hægt að vista hana á staðnum.

Til að stjórna eftirfarandi þáttum skýrslugerðarferlisins skal setja upp úrvinnslu á rafrænum skilaboðum:

- Skrá upplýsingar um þann sem bjó til skýrsluna.
- Skrá upplýsingar um hvenær skýrslan var gerð.
- Vista skýrslur sem voru búnar til fyrir fyrri tímabil.

Eftirfarandi dæmi um hvernig hægt er að setja upp rafræn skilaboð til að búa til skýrslu sem byggist á útflutningssniði rafrænnar skýrslugerðar fyrir Microsoft Excel. Ef þú vilt fylgja þessu dæmi verður útflutningssnið rafrænnar skýrslugerðar fyrir Excel að hafa verið búið til, því varpað í gagnaveitur og því lokið. Auk þess verður númeraröð að vera uppsett fyrir rafræn skilaboð.

Þegar vinnsla er búin til er gagnlegt að skilgreina fyrst aðgerðir og stöður vinnslunnar sem verða settar upp. Eftirfarandi skýringarmynd sýnir ferlið fyrir þetta dæmi.

![Vinnsluskema](media/processing-scheme.png)

## <a name="create-message-statuses"></a>Stofna skilaboðastöður

1. Opnið **Skattur** \> **Uppsetning** \> **Rafræn skilaboð** \> **Stöður skilaboða**.
2. Stofna eftirfarandi stöður skilaboða:

    - Nýjar
    - Undirbúið
    - Myndað

    ![Stöður skilaboða](media/message-statuses.png)

3. Í línunni fyrir stöðuna **Ný** skal velja gátreitinn **Leyfa eyðingu** til að gera notendum kleift að eyða skilaboðum sem eru með þessa stöðu.

## <a name="create-additional-fields"></a>Stofna önnur svæði

1. Opnið **Skattur** \> **Uppsetning** \> **Rafræn skilaboð** \> **Önnur svæði**.
2. Bætið við öðrum svæðum og gildum þeirra.
3. Stillið valkostinn **Breyting notanda** á **Já** til að leyfa notendum að breyta svæðinu.

![Önnur svæði](media/additional-fields.png)

## <a name="create-message-processing-actions"></a>Stofnið úrvinnsluaðgerðir skilaboða

Í þessu dæmi verða eftirfarandi aðgerðir skilaboðaúrvinnslu búnar til:

- **Stofna skilaboð**
- **Uppfæra í undirbúið**
- **Búa til skýrslu**
- **Uppfæra í upphafsstöðu** (valfrjálst)

Fylgja skal þessum skrefum til að búa til aðgerðir.

1. Opnið **Skattur** \> **Uppsetning** \> **Rafræn skilaboð** \> **Úrvinnsluaðgerðir skilaboða**.
2. Stofnið aðgerð með heitinu **Stofna skilaboð**. Á flýtiflipanum **Almennt**, í reitnum **Gerð aðgerðar** skal velja **Stofna skilaboð**.
3. Stofnið aðgerð með heitinu **Uppfæra í undirbúið** og stillið eftirfarandi svæði:

    - Á flýtiflipanum **Almennt**, á svæðinu **Gerð aðgerðar**, skal velja **Úrvinnsla notanda á skilaboðastigi**.
    - Á flýtiflipanum **Upphafsstöður**, á svæðinu **Staða skilaboða**, skal velja **Ný**.
    - Á flýtiflipanum **Lokastöður**, á svæðinu **Staða skilaboða**, skal velja **Undirbúin**. Á svæðinu **Gerð svars** skal fara í **Keyrsla heppnaðist**.

4. Stofnið aðgerð með heitinu **Búa til skýrslu** og stillið eftirfarandi svæði:

    - Á flýtiflipanum **Almennt**, á svæðinu **Gerð aðgerðar**, skal velja **Útflutningur á rafrænum skýrslum**. Á svæðinu **Vörpun sniðmáts** skal velja útflutningssnið rafrænnar skýrslugerðar. Valkostirnir eru **Excel**, **XML**, **JSON**, **Texti** og **Annað**.
    - Á flýtiflipanum **Upphafsstöður**, á svæðinu **Staða skilaboða**, skal velja **Undirbúin**.
    - Á flýtiflipanum **Lokastöður**, á svæðinu **Staða skilaboða**, skal velja **Mynduð**. Á svæðinu **Gerð svars** skal fara í **Keyrsla heppnaðist**.

    ![Aðgerð skýrslugerðar](media/generate-report-action.png)

5. Valfrjálst: Til að leyfa notendum að endurgera skýrslu nokkrum sinnum er hægt að stofna aðgerðina sem kallast **Uppfæra í upphafsstöðu** og stilla eftirfarandi svæði:

    - Á flýtiflipanum **Almennt**, á svæðinu **Gerð aðgerðar**, skal velja **Úrvinnsla notanda á skilaboðastigi**.
    - Á flýtiflipanum **Upphafsstöður**, á svæðinu **Staða skilaboða**, skal velja **Myndaðar**.
    - Í flýtiflipanum **Lokastöður** skal bæta við aðskilinni línu fyrir hvora skilaboðastöðuna fyrir sig (**Undirbúið** og **Nýtt**). Fyrir báðar línur skal stilla svæðið **Gerð svars** á **Tókst að framkvæma**.

## <a name="electronic-message-processing"></a>Rafræn skilaboð í vinnslu

Í þessu dæmi á að setja upp allar aðgerðirnar svo þær keyri hver fyrir sig. Gert er ráð fyrir að notandinn muni frumstilla allar aðgerðir.

1. Opnið **Skattur** \> **Uppsetning** \> **Rafræn skilaboð** \> **Úrvinnsla rafrænna skilaboða**.
2. Bætið við færslu fyrir vinnsluna og bætið við öllum áður skilgreindum aðgerðum og öðrum svæðum.
3. Valfrjálst: Á flýtiflipanum **Öryggishlutverk** skal skilgreina öryggishlutverk fyrir vinnslurnar til að takmarka aðgang að tilteknum skýrslum.
4. Opnið **Skattur** \> **Fyrirspurnir og skýrslur** \> **Rafræn skilaboð** \> **Rafræn skilaboð**.
5. Veljið **Ný** til að stofna ný skilaboð. Á þessum tímapunkti er hægt að bæta við dagsetningum og lýsingu. Einnig er hægt að uppfæra gildið á viðbótarsvæði eins og þörf krefur.

    ![Rafræn skilaboð stofnuð](media/create-electronic-message.png)

    Fyllt er sjálfkrafa inn í hnitanetið á flýtiflipanum **Aðgerðakladdi** með kladda yfir allar aðgerðir sem eru framkvæmdar á skilaboðinu.

    Nú er hægt að eyða eða uppfæra stöðu skilaboða. 

6. Til að uppfæra stöðu skilaboða skal velja **Uppfæra stöðu**. Í reitnum **Ný staða** skal velja **Undirbúið** og síðan velja **Í lagi**.

    ![Skilaboðastaða uppfærð](media/update-status.png)

    Skilaboðastaða er uppfærð í **Tilbúin**.

7. Búðu til skýrsluna með því að velja **Mynda skýrslu**.

    Skýrslan er búin til og uppfærsla gerð á stöðu skilaboða og aðgerðakladda.

8. Til að skoða myndaða skýrslu skal velja hnappinn **Viðhengi** (bréfaklemmutákn) efst í hægra horni síðunnar.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
