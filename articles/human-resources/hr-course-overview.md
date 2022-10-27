---
title: Yfirlit yfir námskeið
description: Þessi grein útskýrir hvernig mannauðsstjórar og stjórnendur geta notað námskeiðseiginleikana til að viðhalda upplýsingum um námskeið sem eru í boði fyrir starfsmenn.
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable, HcmLearningWorkspace
audience: Application User
ms.custom: 7532
ms.assetid: a6950c29-8b3e-45b2-9084-ddfb1317ffaa
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: a1fd00fb9feea9ab426f67095770389696452215
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/25/2022
ms.locfileid: "9716284"
---
# <a name="courses-overview"></a>Yfirlit yfir námskeið

Microsoft Dynamics 365 Human Resources veitir lausn fyrir námsþarfir fyrirtækis þíns. Þessi lausn býður upp á tvær námsleiðir: *sýndarmynd* og *leiðbeinandi undir forystu*.

*Sýndarnám* er námsupplifun sem er efld með auðlindum á netinu. Í *þjálfun undir leiðbeinanda*, leiðbeinandi auðveldar þjálfun fyrir hóp starfsmanna eða nemenda.

Í námseiningunni okkar geta starfsmenn mannauðs, stjórnendur, þjálfunarstjórar og stjórnendur búið til og úthlutað báðum námsleiðum til starfsmanna.

> [!NOTE]
> Til að nota sýndarnámskeið verður þú að virkja **Endurbætur á námskeiði** eiginleiki í Eiginleikastjórnun.

## <a name="set-up-virtual-courses"></a>Settu upp sýndarnámskeið

Til að stilla sýndarnámskeið verður þú að virkja **Endurbætur á námskeiði** eiginleiki í Eiginleikastjórnun. Fara til **Námskeið \> Nýtt**, og stilltu **Sýndarmynd** valmöguleika til **Já**. Eftir að aðgerðin hefur verið virkjað þarf námskeiðstengil. The **Staða námskeiðs** reiturinn verður stilltur á **Opið**. The **Leyfa starfsmanni að skrá sig sjálfur** valkostur verður stilltur á **Já** en hægt er að stilla á **Nei**.

Eftir **Endurbætur á námskeiði** eiginleiki er virkur í eiginleikastjórnun, eftirfarandi breytingar eiga sér stað:

- Skilgreina þarf skiladag fyrir námskeiðsverkefni.
- Námskeiðshlekkur er nauðsynlegur.
- **Sjálfsafgreiðsla starfsmanna** mun sýna starfsmannayfirlit í **Námskeið**. Notandi getur skoðað námskeið sem eru tímasett, væntanleg fljótlega og úthlutað.
- Starfsmenn geta lokið sýndarnámskeiðum og staðfest sjálfir fyrir þeim.

## <a name="set-up-instructor-led-courses"></a>Settu upp kennarastýrð námskeið

Ekki þarf að stilla námskeið undir forystu kennara áður en þau eru notuð.

Eftirfarandi upplýsingar eru valfrjálsar og hægt er að tilgreina þær fyrir námskeið. Ef þessar upplýsingar verða færðar inn fyrir námskeið ætti að setja þær upp áður en námskeiðsskrárnar eru búnar til:

- Námskeiðsgerð
- Kennslustofuflokkar
- Námskeiðshópar
- Námskeiðsstaðir
- Kennslustofur
- Leiðbeinendur
- Námskeiðsgerðir

Þú getur notað *námskeiðstegundir* að flokka námskeið eftir uppbyggingu þeirra eða innihaldi. Þú getur búið til námskeiðsgerðir á **Tegundir námskeiða**  síðu.

Lágmarks- og hámarksfjöldi þátttakenda sem hægt er að skrá á námskeið er skilgreindur á **Almennt**  Flýtiflipi á **Námskeið**  síðu.

### <a name="course-setup-type"></a>Uppsetning námskeiðsgerðar 

*Uppsetningargerðir* ákvarða uppbyggingu námskeiðsins. Það eru þrjár uppsetningargerðir fyrir námskeið.

| Uppsetningargerð | Lýsing |
|------|--------|
| Staðlað | Námskeið af þessari gerð eru ekki með daglega dagskrá. Það er sjálfgefin uppsetningargerð þegar þú býrð til nýtt námskeið. |
| Dagskrá | Veldu þessa uppsetningargerð til að skipuleggja smáatriði hvers dags námskeiðs sem fer fram yfir marga daga. |
| Dagskrá ‚+ lotur | <p>Veldu þessa uppsetningargerð fyrir flóknari námskeið. Til dæmis er hægt að skipta dagskrá námskeiðsins í *lög* og *fundum*:</p><ul><li>*Lög* eru ákveðin námssvið fyrir námskeið.</li><li>*Fundir* skipta upp brautum og hjálpa til við að bera kennsl á tiltekna ferla eða tækni sem skipta máli fyrir braut.</li></ul> |

### <a name="course-tasks"></a>Verkefni námskeiðs

Ljúktu eftirfarandi verkefnum fyrir hvert námskeið:

- Skrá þátttakendur.
- Tilgreina lokadagsetningu skráningar.
- Tilgreina hámarks- og lágmarksfjölda þátttakenda.
- Úthluta staðsetningu og kennslustofu á námskeið.
- Mæla með hótelum fyrir þátttakendur námskeiðs.
- Búðu til námskeiðslýsingu sem hægt er að setja á **Sjálfsafgreiðsla starfsmanna**.

> [!NOTE]
> Aðeins er hægt að eyða námskeiði ef enginn hefur skráð sig á það.

### <a name="course-statuses"></a>Stöður námskeiðs

Eftirfarandi tafla sýnir stöðu námskeiða og þær aðgerðir sem eru gerðar fyrir hverja.

| Staða | Aðgerðir |
|------|--------|
| Stofnað | <ul><li>Færðu inn og breyttu upplýsingum námskeiðs.</li><li>Breyttu námskeiðsstöðu í **Opið**, svo starfsmenn geti skráð sig á námskeiðið.</li></ul> | 
| Opið | <ul><li>Skrá þátttakendur á námskeiðið</li><li>Fjarlægja þátttakendur úr námskeið.</li><li>Staðfesta þátttakendur í námskeið.</li><li>Breyttu námskeiðsstöðu í **Lokað**  eða **Hætt við** fyrir þátttakendur sem hafa stöðu **Staðfest**.</li></ul>|
| Lokað | Hægt er að opna námskeiðið aftur. |
| Hætt við | Hægt er að opna námskeiðið aftur. |

### <a name="course-participants"></a>Þátttakendur á námskeiði

*Þátttakendur á námskeiðinu* eru starfsmenn sem taka þátt í þjálfunarnámskeiði eða viðburði. Aðeins er hægt að skrá þátttakendur á opin námskeið.

### <a name="workflow"></a>Verkflæði

Starfsmenn sem skrá sig á námskeið í gegnum **Sjálfsafgreiðsla starfsmanna**  síðu getur látið skráningu sína vísað í gegnum verkflæði til samþykkis. Þú getur úthlutað verkflæði til námskeiðs á **Almennt**  Flýtiflipi á **Námskeið**  síðu.
