---
title: Skilgreina sameiginlegar færibreytur
description: Þú þarft að setja upp sameiginlegar færibreytur fyrir skýrslur sem eru samnýttar á milli fyrirtækja, svo sem stöðufærslur. Í þessari grein er því lýst hvernig á að setja upp færibreytur Mannauðs á milli lögaðila.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmSharedParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a7b399e0e8972a15837648d7ae6ec0eaacb5196b
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/06/2021
ms.locfileid: "5130424"
---
# <a name="configure-shared-parameters"></a>Skilgreina sameiginlegar færibreytur

Þú þarft að setja upp sameiginlegar færibreytur fyrir skýrslur sem eru samnýttar á milli fyrirtækja, svo sem stöðufærslur. Í þessari grein er því lýst hvernig á að setja upp færibreytur Mannauðs á milli lögaðila.

Sumar gerðir af færslum, eins og stöðufærslur, eru samnýttar á milli fyrirtækja. Fyrir°þessar færslur þarf að setja upp samnýttar færibreytur. Til dæmis er síðan **Samnýttar færibreytur fyrir mannauð** til að setja upp færibreytur mannauðs á milli lögaðila. 

Á síðunni **Samnýttar færibreytur fyrir mannauð** eru færibreyturnar flokkaðar í svæði,°byggt á virkni þeirra. 

### <a name="previously-released-functionality"></a>Áður losuð virkni
Á flipanum **Auðkenni** verður að velja auðkenningargerðir sem tákna auðkennisnúmer sem skráð°eru á síðunni. Setja verður upp gerð auðkennis áður en hægt er að færa inn auðkennisupplýsingar fyrir starfsmenn. Upplýsingar um kennitölu, þjóðkennisnúmer, auðkenni útlendinga og persónulegan auðkennikóða eru á síðunni **Gerð auðkennis**. Til að skilgreina nýja auðkennisgerð eða fara yfir lista með fyrirliggjandi gerðum skal smella á **Stjórnun starfsfólks** &gt; **Tenglaflipa** &gt; **Uppsetningu** &gt; **Gerðir auðkenna**. Hægt er að færa inn einfaldan kóða og lýsingu. 

### <a name="if-youre-using-dynamics-365-human-resources"></a>Ef notað er Dynamics 365 Human Resources
Á flipanum **Auðkenni** verður að velja auðkenningargerðir sem tákna auðkennisnúmer sem skráð°eru á síðunni. Setja verður upp gerð auðkennis áður en hægt er að færa inn auðkennisupplýsingar fyrir starfsmenn. Upplýsingar um kennitölu, þjóðkennisnúmer, auðkenni útlendinga og persónulegan auðkennikóða eru á síðunni **Gerð auðkennis**. Til að skilgreina nýja auðkennisgerð eða fara yfir lista með fyrirliggjandi gerðum, smellið á **Mannauður** &gt; **Uppsetning** &gt; **Gerð auðkennis**. Hægt er að færa inn einfaldan kóða og lýsingu. 

Á flipanum **Númeraraðir** er hægt að velja númeraraðir sem eru notaðir fyrir eftirfarandi færslur: Starfsmannanúmer, Stöðu, Auðkenni notandabeiðnar, I-9 skjal, Umsækjandi, Umræða, Auðkenni fríðinda og°starfsmannaaðgerðina (ef þessi færslugerð er virkjuð). Til að viðhalda tilvísunum og kóða númeraraða skal nota listasíðuna **Númeraraðir**. Notið síðuleitar eiginleikann til að finna þessa síðu. 

Á flipanum **Stöður** skal gefa til kynna hvort nýjar stöður eru tiltækar fyrir sjálfgefna úthlutun:

-   **Alltaf** - Hægt er að tengja starfsmenn við nýjar stöður þegar stöður eru búnar til. Þegar stöður eru stofnaðar í **Tiltækt fyrir úthlutun** eru dagsetning og tími í **Almennt** flipanum á **Stöðu** síðunni sjálfkrafa sett á stofnunardagsetningu og tíma.
-   **Aldrei** - Þú getur ekki úthlutað starfsmönnum á nýjar stöður þegar stöður eru búnar til. Ef þessi valkostur er valinn þarf að opna síðuna **Staða** fyrir hverja nýja stöðu þegar hún verður tiltæk, og svo, á flipanum **Almennt** skal slá inn **Tiltækt fyrir úthlutun** dagsetninguna til að virkja úthlutun starfsmanns.
