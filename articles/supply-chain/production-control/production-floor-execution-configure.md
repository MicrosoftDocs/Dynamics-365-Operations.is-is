---
title: Grunnstilla viðmót fyrir framkvæmd á framleiðslugólfi
description: Í þessu efnisatriði er útskýrt hvernig á að búa til eina eða fleiri skilgreiningar fyrir keyrsluviðmót framleiðslugólfs. Þegar keyrsluviðmót framleiðslugólfs er opnað hleður það sjálfkrafa inn valinni skilgreiningu og vinnslusíu sem eiga sérstaklega við um vafrann og tækið. Í skilgreiningunni setur þú reglurnar sem verða að gilda fyrir tiltekna notkun.
author: johanhoffmann
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgProductionFloorExecutionConfiguration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 30f36ccf967c47d6a034c00544d45cdfdc3d1907
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/09/2022
ms.locfileid: "8103389"
---
# <a name="configure-the-production-floor-execution-interface"></a>Grunnstilla viðmót fyrir framkvæmd á framleiðslugólfi

[!include [banner](../includes/banner.md)]

Starfsmenn í vinnusal nota keyrsluviðmót framleiðslugólfs til að skrá dagsvinnu þeirra, t.d. þegar þeir hefja vinnu, koma með ábendingar varðandi vinnslur, skrá óbeinar aðgerðir og tilkynna fjarvistir. Þessar skráningar eru grundvöllur þess að fylgjast með framvindu og kostnaði framleiðslupantana og til að reikna út grunn fyrir laun starfsmanna.

Þegar keyrsluviðmót framleiðslugólfs er opnað hleður það sjálfkrafa inn valinni skilgreiningu og vinnslusíu sem eiga sérstaklega við um vafrann og tækið. Í skilgreiningunni setur þú reglurnar sem verða að gilda fyrir tiltekna notkun. Hér eru nokkur dæmi um notkun:

- Á tæki á fyrirtækisganginum stimpla starfsmenn sig inn þegar þeir mæta til vinnu og stimpla sig út þegar þeir fara úr vinnu.
- Í tæki í vinnusal skrá starfsmenn á vél þegar þeir hefja og ljúka vinnu. Þeir skrá einnig hlé og óbeinar aðgerðir.

Þetta efni lýsir hinum ýmsu valkostum til að stilla framkvæmdarviðmót framleiðslugólfs fyrir hvert tæki sem er í notkun á vefsvæðinu þínu.

## <a name="turn-on-the-production-floor-execution-interface-and-its-related-optional-features"></a>Kveikja á keyrsluviðmóti framleiðslugólfs og tengdum valmöguleikum þess

Kveikja verður á keyrsluviðmóti fyrir framleiðslugólf, auk nokkurra valfrjálsra stillinga sem lýst er í þessu efnisatriði, í kerfinu áður en hægt er að nota það. Notið síðuna [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að virkja einhverja eða alla eftirfarandi eiginleika sem lýst er í eftirfarandi undirköflum eins og þörf krefur.

### <a name="the-production-floor-execution-interface"></a>Viðmót fyrir framkvæmd á framleiðslugólfi

Þetta er aðaleiginleikinn sem lýst er í þessu efni og er forsenda allra annarra eiginleika sem nefndir eru í þessum hluta. Frá og með Supply Chain Management 10.0.25 er það skylda og ekki hægt að slökkva á henni. Ef þú ert að keyra útgáfu sem er eldri en 10.0.25, þá geta stjórnendur kveikt eða slökkt á þessari virkni með því að leita að *Framleiðslugólf framkvæmd* eiginleiki í [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) vinnurými.

### <a name="generate-license-plates"></a>Mynda númeraplötur

Þessir eiginleikar gera prentun númeraplötu tiltæka við keyrsluviðmót framleiðslugólfsins. Ef þú vilt nota þetta skaltu kveikja á eftirfarandi eiginleika í [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (í þessari röð):

1. *Númeraplata fyrir tilkynningu um lok var bætt við verkspjaldstækið*<br>(Frá og með Supply Chain Management útgáfu 10.0.21 er sjálfgefið kveikt á þessum eiginleika. Frá og með Supply Chain Management útgáfu 10.0.25 er þessi eiginleiki nauðsynlegur.)
1. *Kveiktu á sjálfvirkri myndun á númeraplötunúmeri þegar tilkynnt er um lok í verkspjaldstækinu.*<br>(Frá og með Supply Chain Management útgáfu 10.0.25 er þessi eiginleiki nauðsynlegur.)

### <a name="print-labels"></a>Prenta merkimiða

Þessir eiginleikar gera prentun merkimiða tiltæka við keyrsluviðmót framleiðslugólfsins. Ef þú vilt nota þetta skaltu kveikja á eftirfarandi eiginleika í [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (í þessari röð):

1. *Númeraplata fyrir tilkynningu um lok var bætt við verkspjaldstækið*<br>(Frá og með Supply Chain Management útgáfu 10.0.21 er sjálfgefið kveikt á þessum eiginleika. Frá og með Supply Chain Management útgáfu 10.0.25 er þessi eiginleiki nauðsynlegur.)
1. *Prenta merki úr verkspjaldstæki*<br>(Frá og með Supply Chain Management útgáfu 10.0.25 er þessi eiginleiki nauðsynlegur.)

### <a name="allow-locking-the-touch-screen"></a>Leyfa læsingu á snertiskjá

Þessi eiginleiki gerir það mögulegt að leyfa starfsmönnum að læsa snertiskjánum svo þeir geti sótthreinsað hann.

Frá og með Supply Chain Management útgáfu 10.0.21 er sjálfgefið kveikt á þessum eiginleika. Frá og með Supply Chain Management 10.0.25 er þessi eiginleiki skylda og ekki hægt að slökkva á honum. Ef þú ert að keyra útgáfu eldri en 10.0.25 geta stjórnendur kveikt eða slökkt á þessari virkni með því að leita að *Eiginleiki til að læsa vinnukortabúnaði og vinnukortastöð svo hægt sé að hreinsa þau* eiginleiki í [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) vinnurými.

### <a name="asset-management-functionality-for-the-production-floor-execution-interface"></a>Virkni eignarstýringar fyrir viðmót framkvæmdar á framleiðslugólfi

Þessi eiginleiki bætir eftirfarandi stjórnunarflipa eigna við keyrsluviðmót framleiðslugólfsins: Starfskraftar geta notað þennan flipa til að velja eign sem er tengd við vélatilföng sem eru innan valdrar síu af vinnslulistanum. Fyrir valda vélaeign getur starfskrafturinn skoðað stöðu og ástand eignarinnar úr teljaragildi í allt að fjórum völdum teljurum. Ef þú vilt nota þennan eiginleika skaltu kveikja á eftirfarandi eiginleika í [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- *Virkni eignarstýringar fyrir viðmót framkvæmdar á framleiðslugólfi*<br>(Frá og með Supply Chain Management útgáfu 10.0.25 er þessi eiginleiki sjálfgefið á.)

### <a name="enable-job-search"></a>Virkja starfaleit

Gerir notendum kleift að bæta leitarreit við verklista. Starfskraftar geta fundið tiltekið starf með því að slá inn auðkenni starfsins eða finna öll störf fyrir tiltekna pöntun með því að slá inn kenni pöntunarinnar. Starfskraftar geta slegið inn kennið með því að nota lyklaborð eða með því að skanna strikamerki. Ef þú vilt nota þetta skaltu kveikja á eftirfarandi eiginleika í [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- *Verkleit fyrir keyrsluviðmót framleiðslugólfs*<br>(Frá og með Supply Chain Management útgáfu 10.0.25 er þessi eiginleiki sjálfgefið á.)

### <a name="enable-reporting-on-co-products-and-by-products"></a>Kveikja á tilkynningum um aukaafurðir og hliðarafurðir

Þessi eiginleiki gerir starfsmönnum kleift að nota vinnsluviðmót framleiðslugólfs til að tilkynna um framvindu runupantana. Þessi tilkynnagjöf felur í sér tilkynningu um aukaafurðum og hliðarafurðum. Til að nota þennan eiginleika skaltu kveikja á eftirfarandi eiginleika í [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- *Skýrsla um aukaafurðir og hliðarafurðir úr keyrsluviðmóti framleiðslugólfs*

## <a name="work-with-production-floor-execution-configurations"></a>Vinna með skilgreiningar á keyrslum framleiðslugólfs

Til að búa til og viðhalda framkvæmdarstillingum framleiðslugólfs, farðu á **Framleiðslueftirlit \> Uppsetning \> Framleiðsluframkvæmd \> Stilltu framkvæmd framleiðslugólfs**. Síðan **Grunnstilla framkvæmd á framleiðslugólfi** sýnir lista yfir fyrirliggjandi skilgreiningar. Á þessari síðu er hægt að framkvæma eftirfarandi aðgerðir:

- Veljið einhverja skilgreiningu framleiðslugólfs sem sýnd er í vinstri dálknum til að skoða og breyta henni.
- Veldu **Nýtt** á aðgerðarrúðunni til að bæta nýrri stillingu við listann. Síðan skal færa í reitinn **Skilgreining** heiti til að auðkenna nýju skilgreininguna. Nafnið sem þú slærð inn verður að vera einstakt meðal allra stillinga og þú munt ekki geta breytt því síðar.

Næst skaltu stilla ýmsar stillingar fyrir valda stillingu. Eftirfarandi reitir eru tiltækir:

- **Aðeins inn- og útstimplun** - Stillið þennan valkost á *Já* til að búa til einfaldara viðmót sem býður upp á inn- og útstimplunarvirkni. Þetta óvirkjar flesta aðra valmöguleika á þessari síðu. Fjarlægja verður allar færslubókarlínur úr **Flipavali** áður en hægt er að virkja þennan valkost.
- **Virkja leit** - Stilltu þennan valkost á *Já* til að taka leitarreit með á verkefnalistann. Starfskraftar geta fundið tiltekið starf með því að slá inn auðkenni starfsins eða finna öll störf fyrir tiltekna pöntun með því að slá inn kenni pöntunarinnar. Starfskraftar geta slegið inn kennið með því að nota lyklaborð eða með því að skanna strikamerki.
- **Tilkynna magn við útstimplun** - Stillið þennan valkost á *Já* til að biðja starfsmenn að senda inn athugasemd um verk í vinnslu við útstimplun. Þegar þessi valkostur er stilltur á *Nei* verða starfsmenn ekki beðnir um þetta.
- **Læsa starfsmanni** - Þegar þessi valkostur er stilltur á *Nei* verða starfsmenn skráðir strax út eftir að þeir eru búnir að gera skráningu (t.d. nýtt verk). Viðmótið mun þá fara aftur á innskráningarsíðuna. Þegar þessi valkostur er stilltur á *Já*, munu starfsmenn vera skráðir inn á framkvæmdarviðmót framleiðslugólfs. Hins vegar getur starfsmaður skráð sig út handvirkt þannig að annar starfsmaður geti skráð sig inn á meðan framkvæmdarviðmót framleiðslugólfs heldur áfram að keyra undir sama kerfisnotandareikningi. Nánari upplýsingar um þessar gerðir reikninga er að finna í [Úthlutaðir notendur](config-job-card-device.md#assigned-users).
- **Nota rauntíma skráningar** - Stillið þetta á *Já* til að stilla tímann fyrir hverja nýja skráningu þannig að hún jafngildi þeim tíma þegar starfsmaðurinn sendi inn skráninguna. Þegar þessi valkostur er stilltur á *Nei* er innskráningartíminn notaður í staðinn. Þú vilt yfirleitt stilla þennan valkost á *Já* ef þú hefur stillt valkostina **Læsa starfsmanni** og/eða **Einn starfsmaður** á *Já* þar sem starfsmenn eru oft innskráðir í lengri tíma.
- **Einhleypur vinnumaður** – Stilltu þennan valkost á *Já* ef aðeins einn starfsmaður notar hvert framkvæmdarviðmót framleiðslugólfs þar sem þessi uppsetning er virk. Þegar þessi valkostur er stilltur á *Já* er valkosturinn **Loka á starfsmann** sjálfkrafa stilltur á *Já*. Að auki fjarlægir þessi valkostur kröfu (og getu) um að starfsmaður skrái sig inn með kortakenni (eða sambærilegu auðkenni). Í staðinn skráir starfsmaðurinn sig inn á Microsoft Dynamics 365 Supply Chain Management með því að nota kerfisnotendareikning sem er tengdur við a *tímaskráður starfsmaður* (frá *verkamenn* töflu), og skráir sig inn á framkvæmdarviðmót framleiðslugólfs sem sá starfsmaður á sama tíma.
- **Leyfðu læsingu á snertiskjánum** – Stilltu þennan valkost á *Já* til að leyfa starfsmönnum að læsa snertiskjá framkvæmdarviðmóts framleiðslugólfs svo þeir geti sótthreinsað hann. Þegar þessi valkostur er stilltur á *Já*, a **Læsiskjár til að hreinsa** hnappur er bætt við innskráningarsíðuna. Þegar starfsmaður velur þennan hnapp læsist snertiskjárinn tímabundið til að koma í veg fyrir óvæntan innslátt. Niðurteljari er einnig sýndur. Starfsmaðurinn getur þá þrifið skjáinn og tækið með góðu móti. Þegar niðurtalningu er lokið aflæsist snertiskjárinn sjálfkrafa.
- **Lengd skjálæsingar** - Þegar valkosturinn **Leyfa læsingu snertiskjás** er stilltur á *Já* skal nota þennan valkost til að tilgreina fjölda sekúndna sem snertiskjárinn á að vera læstur vegna þrifa. Tímalengd verður að vera 5 til 120 sekúndur.
- **Búðu til númeraplötu** – Stilltu þennan valkost á *Já* að búa til nýja númeraplötu í hvert sinn sem starfsmaður notar framkvæmdarviðmót framleiðslugólfs til að tilkynna sem lokið. Númeraplötunúmerið er myndað úr númeraröð sem er sett upp á síðunni **Færibreytur vöruhúsakerfis**. Þegar þessi valkostur er stilltur á *Nei* verða starfsmenn að tilgreina fyrirliggjandi númeraplötu þegar þeir tilkynna lok.
- **Prentaðu merkimiðann** – Stilltu þennan valkost á *Já* að prenta númeraplötumerki þegar starfsmaður notar framkvæmdarviðmót framleiðslugólfs til að tilkynna sem lokið. Skilgreining merkisins er sett upp í skjalaleið, eins og lýst er í [Skipulag skjalaleiðar fyrir númeraplötumerki](../warehousing/document-routing-layout-for-license-plates.md).
- **Flipaval** – Notið stillingar í þessum hluta til að velja hvaða flipar eigi að birtast af keyrsluviðmóti framleiðslugólfs þegar núgildandi skilgreining er virk. Hægt er að hanna eins marga flipa og þarf að bæta við og raða þeim hér eins og nauðsynlegt er. Frekari upplýsingar um hvernig á að hanna flipa og vinna með stillingar hér er að finna á [Hanna viðmótið fyrir framkvæmd á framleiðslugólfi](production-floor-execution-tabs.md).

## <a name="clean-up-job-configurations"></a>Skilgreiningar á hreinsunarvinnu

Þegar umsjónarmaður vinnusalar setur upp keyrsluviðmót framleiðslugólfsins, velur hann skilgreiningu og vinnusíu. Þetta val er vistað í tilvísunartöflu í Supply Chain Management og vafrinn notar kenni sem er geymt í staðbundinni köku til að finna réttu línuna í þeirri töflu. Taflan skráir líka dagsetninguna og tímann sem starfsmaður var síðast innskráður í hvert tæki.

Runuvinnslu hreinsar reglulega færslur í tilvísanatöflunni fyrir tæki sem hafa ekki skráð neinar aðgerðir síðustu 60 daga. Einnig er hægt að hreinsa færslurnar handvirkt hvenær sem er með því að fylgja þessum skrefum.

1. Farið í **Framleiðslustýring \> Uppsetning \> Framkvæmd framleiðslu \> Grunnstilla framkvæmd á framleiðslugólfi**.
1. Á aðgerðasvæðinu skal velja **Hreinsa biðlaragrunnstillingar**.
1. Í svarglugganum **Hreinsa biðlaragrunnstillingu** skal stilla reitinn **Fjöldi daga** á dagafjölda án aðgerða (á undan deginum í dag) sem á að taka til greina. Allar skilgreiningar og innskráningarfærslur eru fjarlægðar fyrir tæki sem hafa ekki verið virk á þessum tíma.
1. Veljið **Í lagi** til að hreinsa út viðeigandi skilgreiningar byggt á stillingunni **Fjöldi daga**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
