---
title: Skilgreina sameiginlegar færibreytur
description: Í þessari grein er því lýst hvernig á að setja upp færibreytur Mannauðs á milli lögaðila.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSharedParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c0d8dbca302d90cc402feb4715a6fcc2b935d8b1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906183"
---
# <a name="configure-shared-parameters"></a>Skilgreina sameiginlegar færibreytur

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þú verður að setja upp samnýttar færibreytur fyrir færslur sem er deilt á milli fyrirtækja, svo sem **Staða** skrár. Í þessari grein er því lýst hvernig á að setja upp færibreytur Mannauðs á milli lögaðila.

Sumar tegundir af skrám, svo sem **Staða** skrám, er deilt á milli fyrirtækja. Fyrir°þessar færslur þarf að setja upp samnýttar færibreytur. Til dæmis, the **Mannauður sameiginlegar breytur** síða er notuð til að setja upp mannauðsfæribreytur þvert á lögaðila. 

Á síðunni **Samnýttar færibreytur fyrir mannauð** eru færibreyturnar flokkaðar í svæði,°byggt á virkni þeirra. 

### <a name="settings"></a>Stillingar
Á flipanum **Auðkenni** verður að velja auðkenningargerðir sem tákna auðkennisnúmer sem skráð°eru á síðunni. Setja verður upp gerð auðkennis áður en hægt er að færa inn auðkennisupplýsingar fyrir starfsmenn. Upplýsingar um kennitölu, þjóðkennisnúmer, auðkenni útlendinga og persónulegan auðkennikóða eru á síðunni **Gerð auðkennis**. Til að skilgreina nýja auðkennistegund eða skoða listann yfir núverandi gerðir, farðu á **Starfsmannastjórnun** &gt; **Tenglar** &gt; **Uppsetning** &gt; **Auðkennisgerðir**. Hægt er að færa inn einfaldan kóða og lýsingu. 

Á **Númeraraðir** flipanum geturðu valið töluröðina sem eru notaðar fyrir eftirfarandi færslur: **Starfsmannanúmer**, **·**, **notandabeiðni**, **-9 skjal**, **·**, **·**, **bóta**, og **Starfsmannaaðgerðir** (ef þessi skráargerð er virkjuð). Til að viðhalda tilvísunum og kóða númeraraða skal nota listasíðuna **Númeraraðir**. Notið síðuleitar eiginleikann til að finna þessa síðu. 

Á flipanum **Stöður** skal gefa til kynna hvort nýjar stöður eru tiltækar fyrir sjálfgefna úthlutun:

- **Alltaf** - Hægt er að tengja starfsmenn við nýjar stöður þegar stöður eru búnar til. Þegar stöður eru stofnaðar í **Tiltækt fyrir úthlutun** eru dagsetning og tími í **Almennt** flipanum á **Stöðu** síðunni sjálfkrafa sett á stofnunardagsetningu og tíma.
- **Aldrei** - Þú getur ekki úthlutað starfsmönnum á nýjar stöður þegar stöður eru búnar til. Ef þessi valkostur er valinn þarf að opna síðuna **Staða** fyrir hverja nýja stöðu þegar hún verður tiltæk. Síðan í flipanum **Almennt** skal færa inn dagsetninguna **Tiltækt til úthlutunar** til að virkja úthlutun starfsmanns.

Í flipanum **Ítarlegri aðgangur** er hægt að takmarka aðgang að sumum upplýsingum eða tenglum:

- **Takmarka aðgang að upplýsingum starfsmanna** – Veldu þennan eiginleika ef notendur ættu aðeins að geta skoðað starfsmannaupplýsingar fyrir þá lögaðila sem þeir hafa aðgang að, og fyrir starfsmenn sem hafa starf hjá þeim lögaðilum.

    Eftir að þessi eiginleiki hefur verið valinn skaltu fylgja þessum skrefum til að stilla viðeigandi heimildir fyrir hvern notanda sem þarf að takmarka útsýni:

    1. Á síðunni **Notendur** skal velja notanda.
    1. Veljið hlutverk fyrir notandann. Boðið verður upp á valkostinn **Úthluta fyrirtækjum**.
    1. Veljið **Úthluta fyrirtækjum**.
    1. Á nýju síðunni skaltu velja **Veita ákveðnum fyrirtækjum aðgang hverju fyrir sig** og veldu síðan fyrirtækin sem notandinn á að hafa aðgang að.
    1. Endurtaktu skref 2 til 4 fyrir hvert viðbótarhlutverk sem notandinn hefur, þar með talið kerfisnotendahlutverkið.

    > [!NOTE]
    > Fyrirtækin sem notandi hefur aðgang að verða að vera í samræmi við öll hlutverk notandans.

- **Virkja launayfirlit í fyrirtækjum** – Launum starfsmanna er úthlutað á hvern lögaðila starfsins. Stundum getur starfsmaður starfað í mörgum lögaðilum samtímis. Þegar þessi eiginleiki er valinn munu bætur fyrir hvern lögaðila birtast í **Sjálfsafgreiðsla starfsmanna** og **Sjálfsafgreiðslustjóri** án þess að þú þurfir að skipta um lögaðila. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
