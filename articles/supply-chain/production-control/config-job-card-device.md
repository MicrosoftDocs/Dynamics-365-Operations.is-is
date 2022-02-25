---
title: Skilgreina verkspjald fyrir tæki
description: Í þessu efnisatriði er lýst ýmsum valkostum til að stilla verkspjaldstækið.
author: johanhoffmann
ms.date: 05/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgRegistrationSetupTouch, JmgRegistrationTouchUserConfiguration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: 4c7a9585d96a1e08790e0f3c972e704971f27dc0
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/09/2022
ms.locfileid: "8103439"
---
# <a name="configure-job-card-for-devices"></a>Skilgreina verkspjald fyrir tæki

[!include [banner](../includes/banner.md)]

Verkspjaldstækið er notað af starfsmönnum í vinnusal til að skrá dagleg störf, t.d. hvenær störf hefjast, athugasemdir um störf tilkynntar, skráning afleiddra verkþátta og tilkynningar um fjarvistir. Þessar skráningar eru grundvöllur þess að fylgjast með framvindu og kostnaði framleiðslupantana og til að reikna út grunn fyrir laun starfsmanna. Í þessu efnisatriði er lýst ýmsum valkostum til að stilla verkspjaldstækin.

## <a name="enable-new-features-in-feature-management"></a>Virkja nýja eiginleika í eiginleikastjórnun

Nokkrar af stillingunum sem lýst er í þessu efnisatriði verða að vera virkar í kerfinu áður en boðið er upp á þær. Notið síðuna [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að virkja einhverja eða alla eftirfarandi eiginleika eins og þörf krefur.

### <a name="generate-license-plate"></a>Mynda númeraplötu

Til að gera þennan eiginleika tiltækan skal virkja eftirfarandi eiginleika í [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (í röð):

1. *Númeraplata fyrir tilkynningu um lok var bætt við verkspjaldstækið*<br>(Frá og með Supply Chain Management útgáfu 10.0.21 er sjálfgefið kveikt á þessum eiginleika. Frá og með Supply Chain Management útgáfu 10.0.25 er þessi eiginleiki nauðsynlegur.)
1. *Kveiktu á sjálfvirkri myndun á númeraplötunúmeri þegar tilkynnt er um lok í verkspjaldstækinu.*<br>(Frá og með Supply Chain Management útgáfu 10.0.25 er þessi eiginleiki nauðsynlegur.)

### <a name="print-label"></a>Prenta merki

Til að gera þennan eiginleika tiltækan skal virkja eftirfarandi eiginleika í [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (í röð):

1. *Númeraplata fyrir tilkynningu um lok var bætt við verkspjaldstækið*<br>(Frá og með Supply Chain Management útgáfu 10.0.21 er sjálfgefið kveikt á þessum eiginleika. Frá og með Supply Chain Management útgáfu 10.0.25 er þessi eiginleiki nauðsynlegur.)
1. *Prenta merki úr verkspjaldstæki*<br>(Frá og með Supply Chain Management útgáfu 10.0.25 er þessi eiginleiki nauðsynlegur.)

### <a name="allow-locking-of-touch-screen"></a>Leyfa læsingu á snertiskjá

Frá og með Supply Chain Management útgáfu 10.0.21 er sjálfgefið kveikt á þessum eiginleika. Frá og með Supply Chain Management 10.0.25 er þessi eiginleiki skylda og ekki hægt að slökkva á honum. Ef þú ert að keyra útgáfu eldri en 10.0.25 geta stjórnendur kveikt eða slökkt á þessari virkni með því að leita að *Eiginleiki til að læsa vinnukortabúnaði og vinnukortastöð svo hægt sé að hreinsa þau* eiginleiki í [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) vinnurými.

## <a name="manage-your-device-configurations"></a>Umsjón með tækjaskilgreiningum

Til að setja upp tækjaskilgreiningar skal fara í **Framleiðslustýring > Uppsetning > Framkvæmd framleiðslu > Skilgreina verkspjald fyrir tæki**. Síðan **Skilgreina verkspjald fyrir tæki** opnast, sem sýnir lista yfir skilgreiningar sem eru til. Héðan er hægt er að gera eftirfarandi: 

- Veljið einhverja skilgreiningu tækis sem sýnd er í vinstri dálknum til að skoða og breyta henni.
- Veljið **Ný** á aðgerðasvæðinu til að bæta nýrri tækjaskilgreiningu við listann. Færið síðan inn heiti í reitinn **Skilgreining** til að auðkenna nýju skilgreininguna. Gildið sem fært er inn hér verður að vera einkvæmt á milli allra skilgreininga tækis og ekki er hægt að breyta því síðar.

Skoðið eftirfarandi hluta til að fá upplýsingar um sérhverja stilingu til að skilgreina verkspjaldstæki.

## <a name="general-settings"></a>Almennar stillingar

Flýtiflipinn **Almennt** gerir þér kleift að skilgreina sérhvern valkost sem er í boði fyrir valda tækjaskilgreiningu. Eftirfarandi stillingar eru tiltækar:

- **Tilkynna magn við útstimplun** - Stillið þetta á **Já** til að biðja starfsmenn að senda inn athugasemd um verk í vinnslu við útstimplun. Þegar stillt er á **Nei** verða starfsmenn ekki beðnir um þetta.
- **Læsa starfsmanni** - Þegar þessi valkostur er stilltur á **Nei** verður sérhver starfsmaður skráður strax út eftir að hafa búið til skráningu (t.d. nýtt verk) og mun tækið síðan fara aftur á innskráningarsíðuna. Þegar þessi valkostur er stilltur á **Já** helst sérhver starfsmaður innskráður í verkspjaldstækinu. Hins vegar getur starfsmaðurinn enn skráð sig út handvirkt til að leyfa öðrum starfsmanni að skrá sig inn á meðan verkspjaldstækið er áfram keyrt undir sama notandareikningi innan kerfisins. Nánari upplýsingar um þessar gerðir reikninga er að finna í [Úthlutaðir notendur](#assigned-users).
- **Strikamerkjaskanni** - Stillið þetta á **Já** til að gefa upp valkost í verkspjaldstækinu sem gerir starfsmönnum kleift að skrá upphaf nýs verks með því að skanna strikamerki.
- **Nota rauntíma skráningar** - Stillið þetta á **Já** til að stilla tímann fyrir hverja nýja skráningu þannig að hún jafngildi þeim tíma sem skráning var send af starfsmanni. Stillið á **Nei** til að nota frekar innskráningartímann. Þú vilt yfirleitt stilla þetta á **Já** ef þú hefur virkjað valkostina **Læsa starfsmanni** og/eða **Einn starfsmaður**, þar sem starfsmenn eru oft innskráðir í lengri tíma.
- **Einn starfsmaður** - Stillið þennan valkost á **Já** ef aðeins einn starfsmaður notar hvert verkspjaldstæki þar sem þessi skilgreining er virk. Þegar þessi valkostur er valinn er valkosturinn **Læsa starfsmanni** sjálfkrafa stilltur á **Já**. Að auki fjarlægir þessi valkostur kröfu (og getu) um að starfsmaður skrái sig inn með kortkenni (eða sambærilegu). Þess í stað skráir starfsmaðurinn sig inn í Supply Chain Management með reikningi kerfisnotanda sem er tengdur við *tímaskráður starfsmaður* (úr töflunni *starfsmenn*) og skráist inn í verkspjaldstækið sem þessi starfsmaður á sama tíma.  Nánari upplýsingar um þessar gerðir reikninga er að finna í [Úthlutaðir notendur](#assigned-users).
- **Leyfa starfsmönnum að stilla persónulegar síur** - Stillið þennan valkost á **Já** til að gera starfsmönnum kleift að sía verkin sem þeir sjá í tækinu. Starfsmaðurinn getur breytt gildum fyrir eitthvert þriggja síuskilyrðanna: **Framleiðslueining**, **Tilfangaflokkur** og **Tilfang**. Aðeins verk sem eru áætluð í tilföngum sem samsvara völdu síuskilyrði verða sýnd í tækinu. Einnig er hægt að úthluta sjálfgefnum gildum fyrir einhver eða öll þessi skilyrði og gilda þau jafnvel þegar þessi valkostur er ekki valinn.
- **Leyfa að læsa snertiskjá** - Stillið þennan valkost á **Já** til að leyfa starfsmönnum að læsa snertiskjá verkspjaldstækis svo þeir geti þrifið hann. Þegar þetta er virkt er hnappnum **Læsa skjá fyrir þrif** bætt við innskráningarsíðu tækis. Þegar starfsmaður velur þennan hnapp læsist snertiskjárinn tímabundið til að koma í veg fyrir óvæntan innslátt og niðurtalning er sýnd. Nú getur starfmaðurinn þrifið skjáinn og tækið með góðu móti. Þegar talningu lýkur opnast snertiskjárinn aftur sjálfkrafa.
- **Lengd skjálæsingar** - Þegar valkosturinn **Leyfa læsingu snertiskjás** er virkur skal nota þennan valkost til að tilgreina sekúndufjöldann sem skjárinn á að vera læstur í fyrir þrif. Tímalengd verður að vera 5 til 120 sekúndur.
- **Framleiðslueining** - Veljið framleiðslueiningu sem á að nota sem sjálfgefið síuskilyrði fyrir lista yfir verk sem eru sýnd hverjum starfsmanni. Aðeins verk sem eru áætluð í tilföngum sem flokkuð eru undir valinni framleiðslueiningu birtast upphaflega í tækinu. Ef **Leyfa starfsmönnum að stilla persónulegar síur** er virkjað, geta starfsmenn breytt þessu gildi, annars á þessi sía alltaf við þegar þessi tækjaskilgreining er virk.
- **Tilfangaflokkur** - Veljið tilfangaflokk sem á að nota sem sjálfgefið síuskilyrði fyrir lista yfir verk sem eru sýnd hverjum starfsmanni. Aðeins verk sem eru áætluð í tilföngum sem flokkuð eru undir völdum tilfangaflokki birtast upphaflega í tækinu. Ef **Leyfa starfsmönnum að stilla persónulegar síur** er virkjað, geta starfsmenn breytt þessu gildi, annars á þessi sía alltaf við þegar þessi tækjaskilgreining er virk.
- **Tilfang** - Veljið tilfang sem á að nota sem sjálfgefið síuskilyrði fyrir lista yfir verk sem eru sýnd hverjum starfsmanni. Aðeins verk sem eru áætluð í völdu tilfangi birtast upphaflega í tækinu. Ef **Leyfa starfsmönnum að stilla persónulegar síur** er virkjað, geta starfsmenn breytt þessu gildi, annars á þessi sía alltaf við þegar þessi tækjaskilgreining er virk.
- **Mynda númeraplötu** - Stillið þennan valkost á **Já** til að mynda nýja númeraplötu í hvert sinn sem starfsmaður notar verkspjaldstækið til að skrá sem lokið. Númeraplötunúmerið er myndað úr númeraröð sem er sett upp á síðunni **Færibreytur vöruhúsakerfis**. Þegar stillt er á **Nei** verða starfsmenn að tilgreina fyrirliggjandi númeraplötu þegar skráð sem lokið.
- **Prenta merki** - Stillið þennan valkost á **Já** til að prenta nýja númeraplötumerki í hvert sinn sem starfsmaður notar verkspjaldstækið til að skrá sem lokið. Skilgreining merkisins er sett upp í skjalaleið, eins og lýst er í [Skipulag skjalaleiðar fyrir númeraplötumerki](../warehousing/document-routing-layout-for-license-plates.md).

<a name="assigned-users"></a>

## <a name="assigned-users"></a>Úthlutaðir notendur

Nota skal flýtiflipann **Úthlutaðir notendur** til að tengja einn eða fleiri kerfisnotendur við núverandi grunnstillingu tækis. Hverjum kerfisnotenda er aðeins hægt að úthluta einni verktækjaskilgreiningu.

Þegar tæki er sett upp, skráir starfsmaður upplýsingatækni sig gjarnan inn í Supply Chain Management með reikningi kerfisnotanda. Þar eftir verður skilgreining verktækis sem tengist þessum kerfisnotanda notuð svo framarlega sem kerfisnotandinn helst skráður inn. Þessir notandareikningar kerfisins takmarkast venjulega við að leyfa aðeins aðgang að verkspjaldssíðu í tæki en engan annan hluta Supply Chain Management.

Eftir að kerfisnotandi hefur skráð sig inn og skilgreiningu verktækis hefur verið hlaðið inn geta starfsmenn þá skráð sig inn í verkspjaldstækið með því að nota reikninginn *tímaskráður starfsmaður* (t.d. með því að skanna strikamerki á kortinu sínu) svo þeir geti hafið ný verk og gert annars konar skráningar. Ýmsir starfsmenn geta skráð sig inn og út yfir daginn, svo lengi sem sama tækjaskilgreining er í gildi á þeirri vél vegna þess að kerfisnotandinn er enn skráður inn í Supply Chain Management fyrir daginn.

Hins vegar, eins og áður er getið, þegar tækjaskilgreining er notuð með valkostinum **Einn starfsmaður** geta starfsmenn venjulega sjálfir skráð sig inn í Supply Chain Management með því að nota kerfisnotanda sem tengist eigin reikningi *tímaskráður starfsmaður*, þannig að þeir hlaða inn tækjaskilgreiningu og skrá sig inn sem starfsmaður í verkspjaldstækinu á sama tíma.

## <a name="additional-resources"></a>Frekari upplýsingar

[Bóka sem tilbúið úr verkspjaldstæki](report-finished-job-device.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]