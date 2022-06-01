---
title: Settu upp og búðu til jákvæðar launaskrár með því að nota rafræna skýrslugerð
description: Þetta efnisatriði útskýrir hvernig á að setja upp jákvæð laun með því að nota rafræna skýrslugerð.
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
ms.openlocfilehash: bc2f17d62b429b599d5ac5f2a521819275d36b64
ms.sourcegitcommit: 2b4ee1fe05792332904396b5f495d74f2a217250
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/18/2022
ms.locfileid: "8770248"
---
# <a name="set-up-positive-pay-files-by-using-electronic-reporting"></a>Settu upp jákvæðar launaskrár með því að nota rafræna skýrslugerð

Þetta efnisatriði útskýrir hvernig á að setja upp jákvæð laun og búa til jákvæðar launaskrár með því að nota rafræna skýrslugerð.

> [!NOTE] 
> Áður en þú notar **Búðu til jákvæða launaskrá banka** virka, þú þarft að endurnýja aðilalistann fyrst.
> Fara í **Gagnastjórnun > Flytja inn / flytja út > Framwork færibreytur** 
> **Einingastillingar** flýtiflipann og velja **Endurnýja einingarlista**.


Setja upp jákvæða greiðslu til að búa til rafræna lista yfir ávísanir sem eru gefnar í banka. Þegar ávísun er afhent bankanum ber bankinn hana saman við tékkalistann. Ef ávísunin stemmir við ávísun í listanum samþykkir bankinn ávísunina. Ef ávísunin stemmir ekki við ávísun í listanum heldur bankinn henni eftir til skoðunar.

## <a name="security-for-positive-pay-files"></a>Öryggi í jákvæðum greiðsluskrám
Jákvæðu greiðsluskránni geta innihaldið viðkvæmar upplýsingar um greiðsluþegar og upphæðir ávísunar. Þess vegna skaltu vera viss um að nota viðeigandi öryggisráðstafanir frá þeim tíma sem skrárnar eru myndaðar og þar til þær eru mótteknar í bankanum. Jákvæðum greiðsluskrám er hlaðið niður í staðsetninguna sem tilgreind er af vafranum. Vegna þess að jákvæðar greiðsluskrár geta innihaldið viðkvæmar upplýsingar er mikilvægt að aðeins viðurkenndir notendur hafi aðgang til að búa til og skoða þessar upplýsingar í Microsoft Dynamics 365 Fjármál. Notið eftirfarandi töflu til að ákvarða heimildir sem krafist er.

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

## <a name="set-up-the-electronic-reporting-configuration"></a>Settu upp rafræna skýrslugerð

1. Fara til **Vinnurými \> Rafræn skýrslugerð**.
2. Á flísum fyrir **Microsoft** stillingarveita, veldu **Geymslur**.
3. Veldu **Altækt** og síðan **Opna**.
4. Ef það þarf að koma á tengingu við geymsluna skaltu velja bláa tengilinn í svarglugganum.
5. Finndu og veldu á stillingalistanum **Jákvæð launalíkan \> Jákvæð launaform**.
6. Á **Útgáfur** Flýtiflipi, veldu nýjustu útgáfuna og veldu síðan **Flytja inn**.

## <a name="set-up-a-positive-pay-format"></a>Setja upp snið jákvæðra greiðslna

1. Fara til **Handbært fé og bankastjórnun \> Uppsetning \> Jákvæð launaform**.
2. Veljið **Nýtt**.
3. Stilltu **Greiðslusnið** og **Lýsing** sviðum.
4. Veldu **Almennt rafrænt útflutningssnið** gátreit.
5. Stilltu **Flytja út sniðstillingar** sviði til **Jákvæð launaform**.

## <a name="assign-a-positive-pay-format-to-a-bank-account"></a>Úthlutaðu jákvætt launasnið á bankareikning
Fyrir hvern bankareikning sem á að mynda upplýsingar um jákvæða greiðslu til, verður að úthluta jákvæða greiðslusniðinu sem tilgreint var í fyrra ferli. Á síðunni Bankareikningar, veljið jákvæða greiðslusniðið sem samsvarar bankareikningnum. Í svæðinu **Upphafsdagur jákvæðrar greiðslu** þarf að færa inn fyrstu dagsetningu til að mynda jákvæðar greiðsluskrár. 

>[!Important]
> Sláðu inn dagsetningu í **Jákvæð laun upphafsdagur** akurvöllur. Ef skilið er eftir autt mun fyrsta jákvæða launaskráin sem myndast innihalda allar ávísanir sem hafa verið búnar til fyrir þennan bankareikning.

1. Fara til **Handbært fé og bankastjórnun \> Reikningar banka \> Bankareikningar**.
2. Opnaðu bankareikninginn.
3. Á **Almennt** flýtiflipann, stilltu **Jákvæð launaform** reitnum á sniðið sem var búið til áður.
4. Stilltu **Jákvæð laun upphafsdagur** reit til núverandi dagsetningar.

## <a name="assign-a-number-sequence-for-positive-pay-files"></a>Setja upp númeraröð fyrir jákvæðar greiðsluskrár
Hver jákvæða greiðsluskrá verður að hafa einkvæmt númer. Á **Stærðir reiðufjár og bankastjórnunar** síðu, búðu til númeraröð fyrir jákvæðar greiðsluskrár á **Númeraraðir** flipa.

## <a name="generate-a-positive-pay-file-for-a-single-bank-account"></a>Mynda jákvæða greiðsluskrá fyrir stakan bankareikning
Hægt er að mynda jákvæða greiðsluskrá fyrir einn lögaðila og einn bankareikning. Til upplýsinga um hvernig á að mynda jákvæðar greiðsluskrár fyrir marga lögaðila og bankareikninga á sama tíma er vísað í næsta hluta. Til að mynda jákvæða greiðsluskrá fyrir einn lögaðila og einn bankareikning, opnið svargluggann **Mynda jákvæða greiðsluskrá** á síðunni **Bankareikningar**. Í svæðinu **Lokadagsetning**, færið inn síðustu dagsetningu ávísunar til að taka með í jákvæðri greiðsluskrá. Allar ávísanir sem ekki hafa verið með í jákvæðri greiðsluskrá fyrir þessa dagsetningu ávísunar eru í skránni.

1. Fara til **Handbært fé og bankastjórnun \> Bankareikningar \> Bankareikningar**.
2. Opnaðu bankareikning sem jákvæð laun eru sett upp fyrir.
3. Veldu **Stjórna greiðslum \> Jákvæð laun \> Jákvæð launaskrá**.
4. Stilltu **Lokadagur** sviði. Ávísanir sem voru búnar til fyrir þessa dagsetningu verða teknar með.

## <a name="generate-a-positive-pay-file-for-multiple-bank-accounts"></a>Mynda jákvæða greiðsluskrá fyrir marga bankareikninga
Til að búa til jákvæða launaskrá fyrir marga bankareikninga skaltu nota **Jákvæð launaskrá** reglubundið verkefni. Veljið snið jákvæðrar greiðslu fyrir skrána og tilgreinið hvort eigi að mynda skrá fyrir alla lögaðila eða fyrir valinn lögaðila. Einnig er hægt að mynda jákvæða greiðsluskrá fyrir alla bankareikninga sem nota tilgreinda sniðið fyrir jákvæða greiðslu eða fyrir valinn bankareikning. Í svæðinu **Lokadagsetning**, færið inn síðustu dagsetningu ávísunar til að taka með í jákvæðri greiðsluskrá. Allar ávísanir sem ekki hafa verið með í jákvæðri greiðsluskrá fyrir þessa dagsetningu ávísunar eru í skránni.

## <a name="view-the-results-of-positive-pay-file-generation"></a>Skoða niðurstöður myndunar jákvæðrar greiðsluskrár
Eftir að jákvæð greiðsluskrá er mynduð, er hægt að skoða niðurstöðurnar á síðunni **Samantekt jákvæðrar greiðsluskrár**. Til að skoða upplýsingar um einstakar athuganir, farðu í **Jákvæðar upplýsingar um launaskrá** síðu.

## <a name="confirm-a-positive-pay-file"></a>Staðfesta jákvæða greiðsluskrá
Eftir að búið er að greiða ávísanir sem eru talin upp í jákvæðu greiðsluskránni berst staðfestingarnúmer frá bankanum. Síðan er hægt að staðfesta jákvæðu greiðsluskrána. Á síðunni **Samantekt jákvæðrar greiðsluskrár**, veljið jákvæða greiðsluskrá sem hefur stöðuna **Stofnuð**, og veljið síðan aðgerðina **Slá inn staðfestingu**. Þegar jákvæð greiðsluskrá er staðfest er staðfestingarnúmerið sem berst frá bankanum skráð.

## <a name="recall-a-positive-pay-file"></a>Afturkalla jákvæða greiðsluskrá
Ef nauðsynlegt er að breyta jákvæðri greiðsluskrá er hægt að afturkalla hana. Á síðunni **Samantekt jákvæðrar greiðsluskrár** veljið jákvæða greiðsluskrá sem hefur stöðuna **Stofnuð**, og veljið síðan aðgerðina **Aturkalla**. Svæðið sem gefur til kynna hvort ávísun hefur verið tekin með í jákvæðri greiðsluskrá er endurstillt fyrir hverja ávísun í jákvæðu greiðsluskránni. Síðan er hægt að stofna nýja jákvæða greiðsluskrá sem inniheldur ávísunina sem var afturkölluð.


XML skránni sem myndast verður hlaðið niður.
