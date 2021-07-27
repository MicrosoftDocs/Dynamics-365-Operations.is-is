---
title: Skilgreina sameiginlegar færibreytur
description: Þú þarft að setja upp sameiginlegar færibreytur fyrir skýrslur sem eru samnýttar á milli fyrirtækja, svo sem stöðufærslur. Í þessari grein er því lýst hvernig á að setja upp færibreytur Mannauðs á milli lögaðila.
author: andreabichsel
ms.date: 06/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSharedParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7aff01bee8cadcf852ae32fd60447c68e2174a2a
ms.sourcegitcommit: 43962e6fedaf55aab2f28f53bc38a69d2ff58403
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/01/2021
ms.locfileid: "6332996"
---
# <a name="configure-shared-parameters"></a>Skilgreina sameiginlegar færibreytur

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þú þarft að setja upp sameiginlegar færibreytur fyrir skýrslur sem eru samnýttar á milli fyrirtækja, svo sem stöðufærslur. Í þessari grein er því lýst hvernig á að setja upp færibreytur Mannauðs á milli lögaðila.

Sumar gerðir af færslum, eins og stöðufærslur, eru samnýttar á milli fyrirtækja. Fyrir°þessar færslur þarf að setja upp samnýttar færibreytur. Til dæmis er síðan **Samnýttar færibreytur fyrir mannauð** til að setja upp færibreytur mannauðs á milli lögaðila. 

Á síðunni **Samnýttar færibreytur fyrir mannauð** eru færibreyturnar flokkaðar í svæði,°byggt á virkni þeirra. 

### <a name="settings"></a>Stillingar
Á flipanum **Auðkenni** verður að velja auðkenningargerðir sem tákna auðkennisnúmer sem skráð°eru á síðunni. Setja verður upp gerð auðkennis áður en hægt er að færa inn auðkennisupplýsingar fyrir starfsmenn. Upplýsingar um kennitölu, þjóðkennisnúmer, auðkenni útlendinga og persónulegan auðkennikóða eru á síðunni **Gerð auðkennis**. Til að skilgreina nýja auðkennisgerð eða fara yfir lista með fyrirliggjandi gerðum skal smella á **Stjórnun starfsfólks** &gt; **Tenglaflipa** &gt; **Uppsetningu** &gt; **Gerðir auðkenna**. Hægt er að færa inn einfaldan kóða og lýsingu. 

Á flipanum **Númeraraðir** er hægt að velja númeraraðir sem eru notaðir fyrir eftirfarandi færslur: Starfsmannanúmer, Stöðu, Auðkenni notandabeiðnar, I-9 skjal, Umsækjandi, Umræða, Auðkenni fríðinda og°starfsmannaaðgerðina (ef þessi færslugerð er virkjuð). Til að viðhalda tilvísunum og kóða númeraraða skal nota listasíðuna **Númeraraðir**. Notið síðuleitar eiginleikann til að finna þessa síðu. 

Á flipanum **Stöður** skal gefa til kynna hvort nýjar stöður eru tiltækar fyrir sjálfgefna úthlutun:

- **Alltaf** - Hægt er að tengja starfsmenn við nýjar stöður þegar stöður eru búnar til. Þegar stöður eru stofnaðar í **Tiltækt fyrir úthlutun** eru dagsetning og tími í **Almennt** flipanum á **Stöðu** síðunni sjálfkrafa sett á stofnunardagsetningu og tíma.
- **Aldrei** - Þú getur ekki úthlutað starfsmönnum á nýjar stöður þegar stöður eru búnar til. Ef þessi valkostur er valinn þarf að opna síðuna **Staða** fyrir hverja nýja stöðu þegar hún verður tiltæk. Síðan í flipanum **Almennt** skal færa inn dagsetninguna **Tiltækt til úthlutunar** til að virkja úthlutun starfsmanns.

Í flipanum **Ítarlegri aðgangur** er hægt að takmarka aðgang að sumum upplýsingum eða tenglum:

- **Takmarka aðgang að upplýsingum starfsmanns** – Kveiktu á þessum eiginleika ef notendur eiga að geta skoðað upplýsingar um starfsmenn aðeins fyrir þá lögaðila sem þeir hafa aðgang að og fyrir starfsmenn sem starfa hjá þessum lögaðilum.

    Eftir að kveikt er á þessum eiginleika verður þú að fylgja þessum skrefum til að setja upp viðeigandi heimildir fyrir hvern notanda þar sem þarf að takmarka aðgengi hans:

    1. Á síðunni **Notendur** skal velja notanda.
    1. Veljið hlutverk fyrir notandann. Boðið verður upp á valkostinn **Úthluta fyrirtækjum**.
    1. Veljið **Úthluta fyrirtækjum**.
    1. Á nýju síðunni skaltu velja **Veita ákveðnum fyrirtækjum aðgang hverju fyrir sig** og veldu síðan fyrirtækin sem notandinn á að hafa aðgang að.
    1. Endurtakið skref 2 til 4 fyrir öll hin hlutverkin sem notandinn hefur, þar með talið hlutverk notanda í kerfinu.

    > [!NOTE]
    > Fyrirtækin sem notandi hefur aðgang að verða að vera í samræmi við öll hlutverk notandans.

- **Virkja launayfirlit í fyrirtækjum** – Launum starfsmanna er úthlutað á hvern lögaðila starfsins. Stundum getur starfsmaður starfað í mörgum lögaðilum samtímis. Þegar kveikt er á þessum eiginleika birtast laun fyrir hvern lögaðila í sjálfsafgreiðslu starfsmanns og sjálfsafgreiðslu stjórnanda án þess að farið sé fram á að þú skiptir um lögaðila. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
