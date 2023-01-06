---
title: Setja upp og mynda jákvæða greiðsluskrá launa með því að nota rafræna skýrslugerð
description: Þessi grein útskýrir hvernig á að setja upp jákvæða greiðslu með því að nota rafræna skýrslugerð.
author: panolte
ms.date: 03/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankPositivePayFormat
audience: Application User
ms.reviewer: twheeloc
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 491048c7274ba6bb52e0a4b7a6ea5cd0f5ff4741
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878219"
---
# <a name="set-up-positive-pay-files-by-using-electronic-reporting"></a>Setja upp jákvæðar greiðsluskrár með rafrænni skýrslugerð

Þessi grein útskýrir hvernig á að setja upp jákvæða greiðslu og mynda jákvæðar greiðsluskrár.

> [!NOTE] 
> Áður en aðgerðin **Mynda jákvæða greiðsluskrá banka** er notuð þarf að uppfæra einingalistann fyrst.
> Farðu í flýtiflipann **Gagnastjórnun > Flytja inn / Flytja út > Færibreytur ramma** 
> **Einingastillingar**, veldu **Uppfæra einingalista**.


Setja upp jákvæða greiðslu til að búa til rafræna lista yfir ávísanir sem eru gefnar í banka. Þegar ávísun er svo innleyst í bankanum ber bankinn ávísunina saman við lista yfir ávísanir. Ef ávísunin stemmir við ávísun í listanum samþykkir bankinn ávísunina. Ef ávísunin stemmir ekki við ávísun í listanum heldur bankinn henni eftir til skoðunar.

## <a name="security-for-positive-pay-files"></a>Öryggi í jákvæðum greiðsluskrám
Jákvæðu greiðsluskránni geta innihaldið viðkvæmar upplýsingar um greiðsluþegar og upphæðir ávísunar. Þess vegna skaltu vera viss um að nota viðeigandi öryggisráðstafanir frá þeim tíma sem skrárnar eru myndaðar og þar til þær eru mótteknar í bankanum. Jákvæðum greiðsluskrám er hlaðið niður í staðsetninguna sem tilgreind er af vafranum. Vegna þess að jákvæðar greiðsluskrár geta innihaldið viðkvæmar upplýsingar, er mikilvægt að aðeins heimilaðir notendur hafi aðgang til að mynda og skoða þessar upplýsingar í Microsoft Dynamics 365 Finance. Notið eftirfarandi töflu til að ákvarða heimildir sem krafist er.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Verkefni</th>
<th>Réttindi</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Mynda jákvæðar skrár úr listasíðunni <strong>Bankareikningar</strong> eða úr síðunni <strong>Bankareikningar</strong>.</td>
<td><ul>
<li><strong>Viðhalda upplýsingum um jákvæða greiðslu banka</strong> (BankPositivePayProcess)</li>
<li><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</li>
</ul></td>
</tr>
<tr class="even">
<td>Mynda jákvæðar greiðsluskrár fyrir marga lögaðila og bankareikninga úr síðunni <strong>Mynda jákvæða greiðsluskrá</strong>.</td>
<td><ul>
<li><strong>Viðhalda upplýsingum um jákvæða greiðslu banka</strong> (BankPositivePayProcess)</li>
<li><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Skoða jákvæðar greiðsluskrár á síðunni <strong>Samantekt jákvæðra greiðsluskráa</strong>.</td>
<td><strong>Skoða jákvæðar greiðsluupplýsingar banka fyrir marga lögaðila</strong> (BankPositivePayView)</td>
</tr>
<tr class="even">
<td>Staðfesta jákvæða greiðsluskrá banka á síðunni <strong>Samantekt jákvæðra greiðsluskráa</strong>.</td>
<td><strong>Staðfesta jákvæða greiðsluskrá</strong> (BankPositivePayConfirm)</td>
</tr>
<tr class="odd">
<td>Afturkalla jákvæða greiðsluskrá banka á síðunni <strong>Samantekt jákvæðra greiðsluskráa</strong>.</td>
<td><strong>Afturkalla jákvæða greiðsluskrá banka</strong> (BankPositivePayRecall)</td>
</tr>
</tbody>
</table>

## <a name="set-up-the-electronic-reporting-configuration"></a>Setja upp skilgreiningu rafrænnar skýrslugerðar

1. Fara í **Vinnusvæði \> Rafræn skýrslugerð**.
2. Í reitnum fyrir skilgreiningarveitu **Microsoft** skal velja **Gagnageymslur**.
3. Veldu **Altækt** og síðan **Opna**.
4. Ef koma þarf á tengingu við gagnageymsluna skal velja bláa tengilinn í svarglugganum.
5. Í skilgreiningalistanum skal finna og velja **Jákvætt greiðslulíkan \> Jákvætt greiðslusnið**.
6. Í flýtiflipanum **Útgáfur** skal velja síðustu útgáfuna og velja svo **Flytja inn**.

## <a name="set-up-a-positive-pay-format"></a>Setja upp snið jákvæðra greiðslna

1. Farðu í **Reiðufjár- og bankastjórnun \> Uppsetning \> Jákvæð greiðslusnið**.
2. Veljið **Nýtt**.
3. Stilltu reitina **Greiðslusnið** og **Lýsing**.
4. Veldu gátreitinn **Almennt rafrænt útflutningssnið**.
5. Stilltu reitinn **Skilgreining útflutningssniðs** á **Jákvætt greiðslusnið**.

## <a name="assign-a-positive-pay-format-to-a-bank-account"></a>Úthluta jákvæðu greiðslusniði á bankareikninga
Fyrir hvern bankareikning sem á að mynda upplýsingar um jákvæða greiðslu til, verður að úthluta jákvæða greiðslusniðinu sem tilgreint var í fyrra ferli. Á síðunni Bankareikningar, veljið jákvæða greiðslusniðið sem samsvarar bankareikningnum. Í svæðinu **Upphafsdagur jákvæðrar greiðslu** þarf að færa inn fyrstu dagsetningu til að mynda jákvæðar greiðsluskrár. 

>[!Important]
> Færðu inn dagsetningu í reitinn **Upphafsdagur jákvæðrar greiðslu**. Ef hann er skilinn eftir auður verður fyrsta jákvæða greiðsluskráin sem búin er til með allar ávísanir sem hafa verið búnar til fyrir þennan bankareikning.

1. Farið í **Reiðufjár- og bankastjórnun \> Bankareikningar \> Bankareikningar**.
2. Opnaðu bankareikninginn.
3. Í flýtiflipanum **Almennt** skal stilla reitinn **Jákvætt greiðslusnið** á sniðið sem var búið til áður.
4. Stilltu reitinn **Upphafsdagur jákvæðrar greiðslu** á daginn í dag.

## <a name="assign-a-number-sequence-for-positive-pay-files"></a>Setja upp númeraröð fyrir jákvæðar greiðsluskrár
Hver jákvæða greiðsluskrá verður að hafa einkvæmt númer. Á síðunni **Færibreytur reiðufjár- og bankastjórnunar** skal búa til númeraröð fyrir jákvæðar greiðsluskrár í flipanum **Númeraraðir**.

## <a name="generate-a-positive-pay-file-for-a-single-bank-account"></a>Mynda jákvæða greiðsluskrá fyrir stakan bankareikning
Hægt er að mynda jákvæða greiðsluskrá fyrir einn lögaðila og einn bankareikning. Til upplýsinga um hvernig á að mynda jákvæðar greiðsluskrár fyrir marga lögaðila og bankareikninga á sama tíma er vísað í næsta hluta. Til að mynda jákvæða greiðsluskrá fyrir einn lögaðila og einn bankareikning, opnið svargluggann **Mynda jákvæða greiðsluskrá** á síðunni **Bankareikningar**. Í svæðinu **Lokadagsetning**, færið inn síðustu dagsetningu ávísunar til að taka með í jákvæðri greiðsluskrá. Allar ávísanir sem ekki hafa verið með í jákvæðri greiðsluskrá fyrir þessa dagsetningu ávísunar eru í skránni.

1. Farið í **Reiðufjár- og bankastjórnun \> Bankareikningar \> Bankareikningar**.
2. Opnaðu bankareikning sem jákvæð greiðsla er sett upp fyrir.
3. Veldu **Stjórna greiðslum \> Jákvæð greiðsla \> Jákvæð greiðsluskrá**.
4. Stilltu reitinn **Lokadagsetning**. Ávísanir sem voru búnar til á undan þessari dagsetningu verða hafðar með.

## <a name="generate-a-positive-pay-file-for-multiple-bank-accounts"></a>Mynda jákvæða greiðsluskrá fyrir marga bankareikninga
Til að búa til jákvæðar greiðsluskrár fyrir marga bankareikninga skal nota reglubundna verkið **Jákvæð greiðsluskrá**. Veljið snið jákvæðrar greiðslu fyrir skrána og tilgreinið hvort eigi að mynda skrá fyrir alla lögaðila eða fyrir valinn lögaðila. Einnig er hægt að mynda jákvæða greiðsluskrá fyrir alla bankareikninga sem nota tilgreinda sniðið fyrir jákvæða greiðslu eða fyrir valinn bankareikning. Í svæðinu **Lokadagsetning**, færið inn síðustu dagsetningu ávísunar til að taka með í jákvæðri greiðsluskrá. Allar ávísanir sem ekki hafa verið með í jákvæðri greiðsluskrá fyrir þessa dagsetningu ávísunar eru í skránni.

## <a name="view-the-results-of-positive-pay-file-generation"></a>Skoða niðurstöður myndunar jákvæðrar greiðsluskrár
Eftir að jákvæð greiðsluskrá er mynduð, er hægt að skoða niðurstöðurnar á síðunni **Samantekt jákvæðrar greiðsluskrár**. Til að skoða upplýsingar um einstakar ávísanir skal fara á síðuna **Upplýsingar jákvæðrar greiðsluskrár**.

## <a name="confirm-a-positive-pay-file"></a>Staðfesta jákvæða greiðsluskrá
Eftir að búið er að greiða ávísanir sem eru talin upp í jákvæðu greiðsluskránni berst staðfestingarnúmer frá bankanum. Síðan er hægt að staðfesta jákvæðu greiðsluskrána. Á síðunni **Samantekt jákvæðrar greiðsluskrár**, veljið jákvæða greiðsluskrá sem hefur stöðuna **Stofnuð**, og veljið síðan aðgerðina **Slá inn staðfestingu**. Þegar jákvæð greiðsluskrá er staðfest er staðfestingarnúmerið sem berst frá bankanum skráð.

## <a name="recall-a-positive-pay-file"></a>Afturkalla jákvæða greiðsluskrá
Ef nauðsynlegt er að breyta jákvæðri greiðsluskrá er hægt að afturkalla hana. Á síðunni **Samantekt jákvæðrar greiðsluskrár** veljið jákvæða greiðsluskrá sem hefur stöðuna **Stofnuð**, og veljið síðan aðgerðina **Aturkalla**. Svæðið sem gefur til kynna hvort ávísun hefur verið tekin með í jákvæðri greiðsluskrá er endurstillt fyrir hverja ávísun í jákvæðu greiðsluskránni. Síðan er hægt að stofna nýja jákvæða greiðsluskrá sem inniheldur ávísunina sem var afturkölluð.


XML-skránni verður hlaðið niður.
