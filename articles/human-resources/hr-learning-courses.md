---
title: Uppsetning námskeiða
description: Mannauðsstjórar og stjórnendur geta notað eiginleika námskeiðsaðgerða til að viðhalda upplýsingum um þjálfun sem er í boði fyrir starfsmenn.
author: andreabichsel
manager: tfehr
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7532
ms.assetid: a6950c29-8b3e-45b2-9084-ddfb1317ffaa
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: e642146701edad6b2275156e89048bc5a418c8a0
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467916"
---
# <a name="set-up-training-courses"></a>Uppsetning námskeiða

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Mannauðsstjórar og stjórnendur geta notað eiginleika námskeiðsaðgerða til að viðhalda upplýsingum um þjálfun sem er í boði fyrir starfsmenn.

 <a name="set-up-prerequisites"></a>Uppsetningarforkröfur
---------------------

Eftirfarandi upplýsingar þarf og setja verður upp áður en hægt er að stofna námskeið.
-   **Námskeiðsgerðir**

Eftirfarandi upplýsingar eru valfrjálsar upplýsingar sem hægt er að tilgreina fyrir námskeið. Ef þú veist að þú munt færa inn þessar upplýsingar fyrir námskeið, ætti að setja upp upplýsingarnar áður en myndaðar eru skráningar fyrir námskeiðið.
-   **Kennslustofuflokkar**
-   **Námskeiðshópar**
-   **Námskeiðsstaðir**
-   **Kennslustofur**
-   **Leiðbeinendur**

## <a name="course-types"></a>Námskeiðsgerðir
Hægt er að nota námskeiðsgerðir til að flokka námskeið samkvæmt skipan eða efni námskeiðsins. Hægt er að stofna námskeiðsgerðir á **Námskeiðsgerðir** síðu. Velja verður gerð námskeiðs þegar stofnuð er skrá á námskeið.

## <a name="course-setup-type"></a>Uppsetning námskeiðsgerðar
Í eftirfarandi töflu er listi yfir þrjár gerðir uppsetningu fyrir námskeið. Uppsetningargerðir ákvarða skipan námskeiðs.

<table>
<thead>
<tr class="header">
<th>Gerð uppsetningar</th>
<th>Lýsing</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Staðlað</strong></td>
<td>Veljið þessa gerð fyrir námskeið sem hafa ekki dagskrá. Þetta er sjálfgefin gerð uppsetningu þegar nýtt námskeið er stofnað.</td>
</tr>
<tr class="even">
<td><strong>Dagskrá</strong></td>
<td>Veljið þessa gerð til að áætla upplýsingar um hvern dag á námskeiði sem á sér stað yfir marga daga.</td>
</tr>
<tr class="odd">
<td><strong>Dagskrá ‚+ lotur</strong></td>
<td>Veljið þessa gerð fyrir flóknari námskeið. Til dæmis er hægt að skipta dagskrá fyrir námskeið í námskeiðshluta og lotur.
<ul>
<li><strong>Skor</strong> - Skor eru ákveðin fagsvið fyrir námskeið.</li>
<li><strong>Lotur</strong> - Lotur skipta upp skorum og geta aðstoðað við að bera kennsl á sérstakar aðferðir eða tækni sem eru viðeigandi fyrir hvert skor.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="course-tasks"></a>Verkefni námskeiðs
Fyrir hvern tilgang er hægt að ljúka eftir farandi verkum.
- Skrá þátttakendur
- Tilgreina lokadagsetningu skráningar
- Tilgreina hámarks- og lágmarksfjölda þátttakenda.
- Úthluta staðsetningu og kennslustofu á námskeið.
- Mæla með hótelum fyrir þátttakendur námskeiðs.
- Stofna námskeiðslýsingu, sem síðan er hægt að auglýsa á sjálfsafgreiðslu°starfsmanna

  >**Athugasemd** Aðeins er hægt að eyða námskeiði ef enginn hefur skráð sig á það. 

## <a name="course-statuses"></a>Stöður námskeiðs
Í eftirfarandi töflu er listi yfir stöður mögulegar námskeiðs og aðgerðir sem hægt er að ljúka við námskeið sem hefur tiltekna stöðu.

<table>
<thead>
<tr class="header">
<th>Staða</th>
<th>Aðgerðir</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Stofnaður</strong></td>
<td><ul>
<li>Færðu inn og breyttu upplýsingum námskeiðs.</li>
<li>Breyta námskeiðsstöðunni í <strong>Opin</strong> svo að starfsmenn geta skráð sig í námskeiðið.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Opna</strong></td>
<td><ul>
<li>Skrá þátttakendur á námskeiðið</li>
<li>Fjarlægja þátttakendur úr námskeið.</li>
<li>Staðfesta þátttakendur í námskeið.</li>
<li>Breyta námskeiðsstöðunni í <strong>Lokað</strong> eða <strong>Hætt við</strong>.</li>
<li>Áætla spurningalista fyrir þátttakendur sem eru með stöðuna <strong>Staðfest</strong>.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Lokað</strong></td>
<td>Hægt er að opna námskeiðið aftur.</td>
</tr>
<tr class="even">
<td><strong>Hætt við</strong></td>
<td>Hægt er að opna námskeiðið aftur.</td>
</tr>
</tbody>
</table>

## <a name="course-participants"></a>Þátttakendur á námskeiði
Þátttakendur á námskeiði eru starfsmenn sem taka þátt í þjálfunarnámskeiði eða atburði. Aðeins er hægt að skrá þátttakendur í opin námskeið. Lágmarks og hámarksfjöldi þátttakenda sem hægt er að skrá á námskeið er skilgreindur á flýtiflipanum **Almennt** í skjámyndinni **Námskeið**.

<a name="workflow"></a>Verkflæði
--------

Starfsmenn sem skrá sig á námskeið gegnum í **Starfsmanns sjálfsafgreiðsla** síðu geta verið með skráningu beint í gegnum verkflæði fyrir samþykki. Þú getur úthlutað verkflæði fyrir námskeið í flýtiflipanum **Almennt** á síðunni **Námskeið**.







[!INCLUDE[footer-include](../includes/footer-banner.md)]