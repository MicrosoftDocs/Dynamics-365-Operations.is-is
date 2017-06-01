---
title: "Skipuleggja skýrsluhluta í skýrsluhönnun"
description: "Eftir hannað höfum einingar og mynduðum skýrslum, það er gagnlegt að skipuleggja þessum hlutum þannig að þeir verði auðveldara fyrir notendum að staðsetja. Þessi skrá er útskýrt hvernig raða fyrirliggjandi skýrslur einingar og hlutum í skýrsluhönnun."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: ShylaThompson
ms.search.scope: Management Reporter, Core
ms.custom: 59161
ms.assetid: 32e728c5-3b06-4049-8070-ade01e951d49
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 
ms.dyn365.ops.version: 
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: a8739f426c401aacbab56179bad429a231060f57
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017


---

# <a name="organize-report-components-in-report-designer"></a>Skipuleggja skýrsluhluta í skýrsluhönnun

[!include[banner](../includes/banner.md)]


Eftir hannað höfum einingar og mynduðum skýrslum, það er gagnlegt að skipuleggja þessum hlutum þannig að þeir verði auðveldara fyrir notendum að staðsetja. Þessi skrá er útskýrt hvernig raða fyrirliggjandi skýrslur einingar og hlutum í skýrsluhönnun.

Hægt að endurnefna möppur, skýrslur, einingar og aðra hluti í skýrsluhönnun til að auðvelda röðun skráa. Hugsanlega þarf að uppfæra tengingar við þá hluti, allt eftir gerð hlutarins sem var endurnefndur.

## <a name="rename-a-folder-or-building-block-in-report-designer"></a>Mappa eða eining endurnefnd í Skýrsluhönnun
Í Skýrsluhönnun er hægt að endurnefna möppur, skýrsluskilgreiningar, línuskilgreiningar, dálkskilgreiningar og skipuritsskilgreiningar. **Athugasemd:** Þegar eining endurnefna þarf að uppfæra skýrslugerð skilgreiningar sem nota eininguna. Annars er ekki hægt að mynda nýja skýrslu.

### <a name="rename-a-folder-or-building-block-in-report-designer"></a>Mappa eða eining endurnefnd í Skýrsluhönnun

1.  Í Skýrsluhönnun er yfirlitssvæðið notað til að finna möppuna eða hlutinn sem á að endurnefna.
2.  Hægrismellið á möppuna eða hlutinn og smellið síðan á **Endurnefna**. Reiturinn **Heiti** á yfirlitssvæðinu verður virkur.
3.  Nýja heitið er fært inn og ýtt á færslulykilinn.
4.  Ef einingin er línuskilgreining, dálkskilgreining eða skipuritsskilgreiningu verður að uppfæra aðrar einingar sem tengjast því. Hægrismellið á eininguna sem var endurnefnt í skrefi 3, veljið **Tengingar** og veljið svo atriði af listanum til að uppfæra.
5.  Endurtakið skref 4 þar til öll tengd atriði hafa verið uppfærð.

## <a name="create-and-manage-report-groups"></a>Stofnun og stjórnun skýrsluhópa
Setja má skýrsluskilgreiningar saman í hóp til að mynda margar skýrslur samtímis. Til að stofna, breyta, eyða og mynda skýrsluhópa þarf að hafa hlutverk hönnuðar eða stjórnanda. Notendur með hlutverk stofnanda geta myndað skýrsluhópa og geta einnig breytt stillingum skýrsluskilgreininga notanda fyrir skýrsluhópa.

### <a name="create-a-report-group"></a>Skýrsluhópur stofnaður

1.  Í Skýrsluhönnun er smellt á **Skýrsluhópar** á yfirlitssvæðinu.
2.  Á **Skrá** valmyndinni, smellið á **Nýtt** &gt; **Skilgreining skýrsluhóps** til að opna nýjan flokk skýrslu í vafra. Einnig er hægt að smella á **Skýrsluhópur** hnappinn ![Skýrsluhópur](https://i-technet.sec.s-msft.com/dynimg/IC679515.gif "Skýrsluhópur") á tækjastikunni.
3.  Smellið á flipann **Skýrsluhópur**. Til að hnekkja upplýsingum úr stökum skýrsluskilgreiningum fyrir myndun þessarar skýrslu skal velja gátreitinn **Hnekkja stillingum fyrirtækis, upplýsinga og dagsetningar úr stökum skýrsluskilgreiningum**. Heiti fyrirtækis, upplýsingastig, tímabundnar stillingar og dagsetning eru fyllt inn sjálfkrafa en er hægt að uppfæra.
4.  Veljið gátreitinn **Taka með alla skýrslugjaldmiðla** ef búa á til margar skýrslur með skýrslugjaldmiðlum. Skoðun í mörgum gluggum má fá með því að smella á hnappinn **Gjaldmiðill** í Vefskoðun þegar skýrslan er skoðuð.
5.  Í reitnum **Skýrslur í hóp** skal smella á **Bæta við** til að velja skýrslurnar sem eiga að vera í skýrsluhópnum. Til að velja margar skýrslur í svarglugganum **Bæta við** skal halda Ctrl-lyklinum niðri á meðan skýrslur eru valdar. Þegar lokið hefur verið val skýrslur, smellið á **í lagi**.
6.  Smellið á **Skrá** &gt; **Vista** til að vista nýjan skýrsluhóp.

### <a name="modify-a-report-group"></a>Skýrsluhópi breytt

1.  Í Skýrsluhönnun er smellt á **Skýrsluhópar** á yfirlitssvæðinu.
2.  Tvísmellið á skýrsluhóp til að breyta.
3.  Smellið á flipann **Skýrsluhópur** og breytið því sem þarf.
4.  Í valmyndinni **Skrá** skal smella á **Vista** til að vista breyttan skýrsluhóp. Einnig er hægt að smella á **Vista** hnappinn ![Vista](https://i-technet.sec.s-msft.com/dynimg/IC679516.gif "Vista") á tækjastikunni.

**athugasemd:** Ef gerð hefur verið áætlun um myndun skýrslna með tilteknu millibili í stillingum skýrsluskilgreiningar er hægt að hnekkja þeim stillingum og mynda skýrslu strax.

### <a name="generate-a-report-group-report"></a>Myndun skýrslu í skýrsluhóp

1.  Í Skýrsluhönnun er smellt á **Skýrsluhópar** á yfirlitssvæðinu.
2.  Opnið skýrsluhópinn sem á að mynda.
3.  Smellið á hnappinn **Búa til skýrslu** ![Búa til skýrslu](https://i-technet.sec.s-msft.com/dynimg/IC679517.gif "Búa til skýrslu") til að búa til skýrslur.

### <a name="delete-a-report-group"></a>Skýrsluhópi eytt

1.  Í Skýrsluhönnun er smellt á **Skýrsluhópar** á yfirlitssvæðinu.
2.  Hægrismellið á skýrsluhópinn til að eyða og veljið **Eyða**.
3.  Þegar staðfestingarskilaboð birtast skal smella á **Já**.

## <a name="report-group-tab-controls"></a>Stýringar flipa skýrsluhóps
Eftirfarandi tafla lýsir stýringum í á **Skýrslu Flokkur** flipa.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Eftirlit</th>
<th>Lýsing</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Hnekkja stillingum fyrirtækis, upplýsinga og dagsetningar úr stökum skýrsluskilgreiningum</td>
<td>Veljið þennan gátreit til að hnekkja stökum skýrsluskilgreiningum skýrslna í þessum skýrsluhópi fyrir myndun þessara skýrslna eingöngu.</td>
</tr>
<tr class="even">
<td>Nafn fyrirtækis</td>
<td>Veljið fyrirtækið sem nota á í skýrslunum.</td>
</tr>
<tr class="odd">
<td>Lýsing á stigi</td>
<td>Tilgreinið hvaða upplýsingar eiga að vera í skýrslunni.
<ul>
<li><strong>Fjárhagur</strong>− Samantektarskýrsla á háu stigi. Ekki er hægt að kafa niður í reikninga og víddir nema þeim sé bætt við í gegnum skipurit.</li>
<li><strong>Fjárhagur &amp; reikningur</strong> − Skýrsla sem inniheldur samantekt á háu stigi með ítarupplýsingum um reikning.</li>
<li><strong>Fjárhagsreikningur &amp; færsla</strong> − Skýrsla sem inniheldur samantekt á háu stigi með ítarupplýsingum um færslur.</li>
</ul></td>
</tr>
<tr class="even">
<td>Tímabundið</td>
<td>Tilgreinið hvaða verkþættir eiga að vera í skýrslunni.
<ul>
<li><strong>Aðeins bókaðar aðgerðir</strong>− Inniheldur aðeins færslur og innistæður sem eru bókaðar í fjárhagsgögnunum.</li>
<li><strong>Bókaðar og óbókaðar aðgerðir</strong>− Inniheldur allar færslur og innistæður sem eru færðar inn og bókaðar í fjárhagsgögnunum.</li>
<li><strong>Aðeins óbókaðar aðgerðir</strong>− Inniheldur aðeins færslur sem eru færðar inn en eru ekki enn bókaðar í fjárhagsgögnunum.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Taka með alla skýrslugjaldmiðla</td>
<td>Ef aðrir skýrslugjaldmiðlar eru grunnstilltir í ERP-kerfi Microsoft Dynamics eru þeir taldir upp hér. Veljið gátreit til að mynda viðbótarskýrslur í tilgreindum gjaldmiðlum. Hægt er að skoða skýrslurnar í Vefskoðun með því að smella á hnappinn <strong>Gjaldmiðill</strong> og velja gjaldmiðil.</td>
</tr>
<tr class="even">
<td>Upplýsingar um dagsetningu ekki vistaðar með skýrsluskilgreiningu</td>
<td><ul>
<li>Grunntímabil</li>
<li>Grunnár</li>
<li>Tímabil</li>
</ul>
Aðeins stillingar sjálfgefins grunntímabils eru vistaðar með skýrsluskilgreiningunni.</td>
</tr>
<tr class="odd">
<td>Upplýsingar um dagsetningu vistaðar með skýrsluskilgreiningu</td>
<td><ul>
<li>Dagsetning skýrslu</li>
<li>Sjálfgefið grunntímabil</li>
</ul></td>
</tr>
<tr class="even">
<td>Skýrslur í hóp</td>
<td>Bæta við, fjarlægja og endurpanta skýrslur í skýrsluhópnum.
<ul>
<li>Til að bæta skýrsluskilgreiningum við skýrsluhóp er tvísmellt á skýrsluhópinn til að opna hann og svo smellt á <strong>Bæta við</strong>. Veljið skýrslurnar sem á að hafa með í skýrsluhópnum og smellið svo á <strong>Í lagi</strong>.</li>
<li>Til að fjarlægja skýrslu úr skýrsluhópi er skýrslan valin og smellt á <strong>Fjarlægja</strong>.</li>
<li>Til að breyta því í hvaða röð skýrslurnar eru myndaðar er skýrsla valin á listanum og síðan smellt á <strong>Flytja upp</strong> eða <strong>Flytja niður</strong>.</li>
</ul></td>
</tr>
</tbody>
</table>



<a name="see-also"></a>Sjá einnig
--------

[Fjárhagsskýrslugerð](financial-reporting-intro.md)




