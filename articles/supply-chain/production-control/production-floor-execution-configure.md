---
title: Grunnstilla viðmót fyrir framkvæmd á framleiðslugólfi
description: Í þessari grein er útskýrt hvernig á að búa til eina eða fleiri skilgreiningar fyrir keyrsluviðmót framleiðslugólfs. Þegar keyrsluviðmót framleiðslugólfs er opnað hleður það sjálfkrafa inn valinni skilgreiningu og vinnslusíu sem eiga sérstaklega við um vafrann og tækið. Í skilgreiningunni setur þú reglurnar sem verða að gilda fyrir tiltekna notkun.
author: johanhoffmann
ms.date: 11/07/2022
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
ms.openlocfilehash: 641b293617df608bc07b97c077dbcd05664f8e2a
ms.sourcegitcommit: 4abf9b375fed6885ea11a425c524958fea29c3b9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/07/2022
ms.locfileid: "9748687"
---
# <a name="configure-the-production-floor-execution-interface"></a>Grunnstilla viðmót fyrir framkvæmd á framleiðslugólfi

[!include [banner](../includes/banner.md)]

Starfsmenn í vinnusal nota keyrsluviðmót framleiðslugólfs til að skrá dagsvinnu þeirra, t.d. þegar þeir hefja vinnu, koma með ábendingar varðandi vinnslur, skrá óbeinar aðgerðir og tilkynna fjarvistir. Þessar skráningar eru grundvöllur þess að fylgjast með framvindu og kostnaði framleiðslupantana og til að reikna út grunn fyrir laun starfsmanna.

Þegar keyrsluviðmót framleiðslugólfs er opnað hleður það sjálfkrafa inn valinni skilgreiningu og vinnslusíu sem eiga sérstaklega við um vafrann og tækið. Í skilgreiningunni setur þú reglurnar sem verða að gilda fyrir tiltekna notkun. Hér eru nokkur dæmi um notkun:

- Á tæki á fyrirtækisganginum stimpla starfsmenn sig inn þegar þeir mæta til vinnu og stimpla sig út þegar þeir fara úr vinnu.
- Í tæki í vinnusal skrá starfsmenn á vél þegar þeir hefja og ljúka vinnu. Þeir skrá einnig hlé og óbeinar aðgerðir.

Þessi grein lýsir ýmsum valkostum til að stilla viðmóti fyrir framkvæmd á framleiðslugólfi fyrir hvert tæki sem er í notkun á svæðinu þínu.

## <a name="turn-on-the-production-floor-execution-interface-and-its-related-optional-features"></a>Kveikja á keyrsluviðmóti framleiðslugólfs og tengdum valmöguleikum þess

Kveikja verður á keyrsluviðmóti fyrir framleiðslugólf, auk nokkurra valfrjálsra stillinga sem lýst er í þessari grein, í kerfinu áður en hægt er að nota það. Notið síðuna [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að virkja einhverja eða alla eftirfarandi eiginleika sem lýst er í eftirfarandi undirköflum eins og þörf krefur.

### <a name="the-production-floor-execution-interface"></a>Viðmót fyrir framkvæmd á framleiðslugólfi

Þetta er aðaleiginleikinn sem lýst er í þessari grein og er forsenda allra annarra eiginleika sem nefnd eru í þessum hluta. Frá og með útgáfu 10.0.25 af Supply Chain Management er hún skylda og ekki er hægt að slökkva á henni. Ef þú ert að keyra útgáfu sem er eldri en 10.0.25, þá geta stjórnendur kveikt eða slökkt á þessum eiginleika með því að leita að eiginleikanum *Framkvæmd framleiðslugólfs* á vinnusvæðinu [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="generate-license-plates"></a>Mynda númeraplötur

Þessir eiginleikar gera prentun númeraplötu tiltæka við keyrsluviðmót framleiðslugólfsins. Ef þú vilt nota þetta skaltu kveikja á eftirfarandi eiginleika í [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (í þessari röð):

1. *Númeraplata fyrir tilkynningu um lok var bætt við verkspjaldstækið*<br>(Sem hluti af Supply Chain Management, útgáfa 10.0.21, er sjálfgefið kveikt á þessum eiginleika. Sem hluti af Supply Chain Management, útgáfa 10.0.25, er þessi eiginleiki áskilinn.)
1. *Kveiktu á sjálfvirkri myndun á númeraplötunúmeri þegar tilkynnt er um lok í verkspjaldstækinu.*<br>(Frá og með Supply Chain Management, útgáfa 10.0.25, er þessi eiginleiki áskilinn.)

### <a name="print-labels"></a>Prenta merkimiða

Þessir eiginleikar gera prentun merkimiða tiltæka við keyrsluviðmót framleiðslugólfsins. Ef þú vilt nota þetta skaltu kveikja á eftirfarandi eiginleika í [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (í þessari röð):

1. *Númeraplata fyrir tilkynningu um lok var bætt við verkspjaldstækið*<br>(Sem hluti af Supply Chain Management, útgáfa 10.0.21, er sjálfgefið kveikt á þessum eiginleika. Sem hluti af Supply Chain Management, útgáfa 10.0.25, er þessi eiginleiki áskilinn.)
1. *Prenta merki úr verkspjaldstæki*<br>(Frá og með Supply Chain Management, útgáfa 10.0.25, er þessi eiginleiki áskilinn.)

### <a name="allow-locking-the-touch-screen"></a>Leyfa læsingu á snertiskjá

Þessi eiginleiki gerir starfskröftum kleift að læsa snertiskjánum svo að þeir geti þrifið hann.

Sem hluti af Supply Chain Management, útgáfa 10.0.21, er sjálfgefið kveikt á þessum eiginleika. Frá og með útgáfu 10.0.25 af Supply Chain Management er þessi eiginleiki skylda og ekki er hægt að slökkva á henni. Ef þú ert að keyra útgáfu sem er eldri en 10.0.25, þá geta stjórnendur kveikt eða slökkt á þessum eiginleika með því að leita að eiginleikanum *Til að læsa vinnsluspjaldstæki og afgreiðslustöð svo hægt sé að hreinsa tækin* á vinnusvæðinu [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="asset-management-functionality-for-the-production-floor-execution-interface"></a>Virkni eignarstýringar fyrir viðmót framkvæmdar á framleiðslugólfi

Þessi eiginleiki bætir eftirfarandi stjórnunarflipa eigna við keyrsluviðmót framleiðslugólfsins: Starfskraftar geta notað þennan flipa til að velja eign sem er tengd við vélatilföng sem eru innan valdrar síu af vinnslulistanum. Fyrir valda vélaeign getur starfskrafturinn skoðað stöðu og ástand eignarinnar úr teljaragildi í allt að fjórum völdum teljurum.

Sem hluti af Supply Chain Management, útgáfa 10.0.25, er sjálfgefið kveikt á þessum eiginleika. (Frá og með útgáfu 10.0.29 af Supply Chain Management er þessi eiginleiki skylda og ekki er hægt að slökkva á honum.) Ef þú ert að keyra útgáfu sem er eldri en 10.0.29, þá geta stjórnendur kveikt eða slökkt á þessum eiginleika með því að leita að eiginleikanum *Framkvæmd framleiðslugólfs* á vinnusvæðinu [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="job-search"></a>Leit að störfum

Gerir notendum kleift að bæta leitarreit við verklista. Starfskraftar geta fundið tiltekið starf með því að slá inn auðkenni starfsins eða finna öll störf fyrir tiltekna pöntun með því að slá inn kenni pöntunarinnar. Starfskraftar geta slegið inn kennið með því að nota lyklaborð eða með því að skanna strikamerki.

Sem hluti af Supply Chain Management, útgáfa 10.0.25, er sjálfgefið kveikt á þessum eiginleika. (Frá og með útgáfu 10.0.29 af Supply Chain Management er þessi eiginleiki skylda og ekki er hægt að slökkva á honum.) Ef þú ert að keyra útgáfu sem er eldri en 10.0.29, þá geta stjórnendur kveikt eða slökkt á þessum eiginleika með því að leita að eiginleikanum *Verkleit fyrir keyrsluviðmót framleiðslugólfs* á vinnusvæðinu [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="report-on-co-products-and-by-products"></a>Skýrsla um aukaafurðir og hliðarafurðir

Þessi eiginleiki gerir starfsmönnum kleift að nota vinnsluviðmót framleiðslugólfs til að tilkynna um framvindu runupantana. Þessi tilkynnagjöf felur í sér tilkynningu um aukaafurðum og hliðarafurðum.

Til að nota þennan eiginleika þarf að kveikja á honum fyrir kerfið þitt. Sem hluti af Supply Chain Management, útgáfa 10.0.29, er sjálfgefið kveikt á þessum eiginleika. Stjórnendur geta kveikt eða slökkt á þessari virkni með því að leita að eiginleikanum *Skýrsla um aukaafurðir og hliðarafurðir úr keyrsluviðmóti framleiðslugólfs* á vinnusvæðinu [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="display-full-serial-batch-and-license-plate-numbers"></a>Sýna öll raðnúmer, rununúmer og númeraplötunúmer

Þessi eiginleiki býður upp á bætta upplifun til að skoða lista yfir raðnúmer, runu og númeraplötunúmer í keyrsluviðmóti framleiðslugólfsins. Skjárinn breytist úr spjaldyfirliti með takmörkuðum fjölda stafa í listayfirlit sem hefur nægilegt pláss til að sýna öll gildin. Listinn gefur einnig möguleika á að leita að tilteknum tölum.

Til að nota þennan eiginleika þarf að kveikja á honum fyrir kerfið þitt. Sem hluti af Supply Chain Management, útgáfa 10.0.25, er sjálfgefið kveikt á þessum eiginleika. (Frá og með útgáfu 10.0.29 af Supply Chain Management er þessi eiginleiki skylda og ekki er hægt að slökkva á honum.) Ef þú ert að keyra útgáfu sem er eldri en 10.0.29, geta stjórnendur kveikt eða slökkt á þessari virkni með því að leita að eiginleikanum *Sýna öll raðnúmer, rununúmer og númeraplötunúmer í keyrsluviðmóti framleiðslugólfsins* á vinnusvæðinu [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Sem hluti af Supply Chain Management, útgáfa 10.0.25, er sjálfgefið kveikt á þessum eiginleika. Stjórnendur geta kveikt eða slökkt á þessari virkni með því að leita að eiginleikanum *Sýna öll raðnúmer, rununúmer og númeraplötunúmer í keyrsluviðmóti framleiðslugólfsins* á vinnusvæðinu [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="register-material-consumption"></a>Skrá efnisnotkun

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: Preview until further notice -->

Þessi eiginleiki gerir starfsmönnum kleift að nota keyrsluviðmót framleiðslugólfsins til að skrá efnisnotkun, rununúmer og raðnúmer. Sumir framleiðendur, sérstaklega þeir sem eru í framleiðsluiðnaði, verða að skrá sérstaklega efnismagn sem er notað fyrir hverja runu eða framleiðslupöntun. Til dæmis gætu starfskraftar notað vog til að vigta magn efnis sem er notað á meðan þeir vinna. Til að tryggja fullan rekjanleika efnisins verða þessi fyrirtæki einnig að skrá rununúmerin sem voru notuð til að framleiða hverja vöru.

Tvær útgáfur eru af þessari eiginleiki. Einn styður atriði sem *eru ekki* virkjuð til að nota vöruhúsakerfisferla (WMS). Hugbúnaðurinn styður vörur sem *eru* virkjuð til að nota vöruhúsakerfi. Til að nota þennan eiginleika skaltu kveikja á öðrum eða báðum eftirfarandi eiginleikum í [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (í þessari röð), eftir því hvort þú ert með vörur sem eru virkir fyrir WMS:

- *Skrá efnisnotkun í keyrsluviðmóti framleiðslugólfs (ekki vöruhúsakerfi)*
- *(Forútgáfa) Skrá efnisnotkun í keyrsluviðmóti framleiðslugólfs (virkjað fyrir vöruhúsakerfi)*

> [!IMPORTANT]
> Hægt er að nota eiginleikann sem er ekki vöruhúsakerfi einan og sér. Hins vegar, ef þú notar vöruhúsakerfi verður þú að virkja báða eiginleika.

### <a name="report-on-catch-weight-items"></a>Skýrsla um vörur fyrir þyngd afurðar

Starfsmenn geta notað keyrsluviðmót framleiðslugólfsins til að tilkynna um framvindu runupantana fyrir vörur fyrir þyngd afurðar. Runupantanir eru búnar til úr formúlum, sem hægt er að skilgreina til að hafa framleiðsluþyngd vöru, eins og formúluvörur, aukaafurðir og hliðarafurðir. Einnig er hægt að skilgreina formúlu til að hafa formúlulínur fyrir innihaldsefni sem eru skilgreind fyrir þyngd afurðar. Framleiðsluþyngd vöru notar tvær mælieiningar til að rekja birgðir: magn framleiðsluþyngdar og birgðamagn. Til dæmis, í matvælaiðnaði, er hægt að skilgreina pakkað kjöt sem framleiðsluþyngd vöru, þar sem magn framleiðsluþyngdar er notað til að rekja fjölda kassa og birgðamagn er notað til að rekja þyngd kassa.

Til að nota þennan eiginleika skaltu kveikja á eftirfarandi eiginleika í [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- *Skýrsla um vörur með framleiðsluþyngd úr keyrsluviðmóti framleiðslugólfs*

### <a name="the-my-day-dialog"></a>Svarglugginn „Dagurinn minn“

Svarglugginn **Dagurinn minn** veitir starfskröftum yfirlit yfir daglegar skráningar þeirra og núverandi stöðu fyrir greiddan vinnutíma, greidda yfirvinnu, fjarveru og greidda fjarveru.

Til að nota þennan eiginleika þarf að kveikja á honum fyrir kerfið þitt. Sem hluti af Supply Chain Management, útgáfa 10.0.29, er sjálfgefið kveikt á þessum eiginleika. Stjórnendur geta kveikt eða slökkt á þessari virkni með því að leita að eiginleikanum *Yfirlitið „Dagurinn minn“ fyrir keyrsluviðmót framleiðslugólfs* á vinnusvæðinu [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="teams"></a>Teymi

Þegar mörgum starfskröftum er úthlutað í sama framleiðsluverkið geta þeir myndað teymi. Teymið getur tilnefnt einn starfsmann sem verkefnisstjóra. Þeir starfsmenn sem eftir eru verða þá sjálfkrafa aðstoðarmenn þess verkefnisstjóra. Aðeins verkefnisstjórinn skal skrá verkefnastöðu fyrir væntanlegt teymi. Tímaskráningar gilda fyrir alla meðlimi hópsins.

Til að nota þennan eiginleika skaltu kveikja á eftirfarandi eiginleika í [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- *Framleiðsluteymi í keyrsluviðmóti framleiðslugólfs*

### <a name="additional-configuration-in-the-production-floor-execution-interface"></a>Viðbótargrunnstillingar viðmóts fyrir framkvæmd á framleiðslugólfi

Þessi eiginleiki bætir við stillingum fyrir eftirfarandi virkni við síðuna **Stilla framkvæmd á framleiðslugólfi**:

- Opna sjálfkrafa svargluggann **Hefja vinnslu** þegar leit er lokið.
- Opna sjálfkrafa svargluggann **Tilkynna um framvindu** þegar leit er lokið.
- Fylla út fyrirfram eftirstandandi magn í svarglugganum **Tilkynna um framvindu**.
- Virkja breytingar á efnisnotkun úr svarglugganum **Tilkynna um framvindu**. (Þessi virkni krefst einnig eiginleikans *Skrá efnisnotkun í keyrsluviðmóti framleiðslugólfs (ekki)* vöruhúsakerfi).
- Virkja leit eftir verkkenni.

Upplýsingar um hvernig á að nota stillingarnar koma fram síðar í þessari grein.

Til að nota þennan eiginleika skaltu kveikja á eftirfarandi eiginleika í [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- *Viðbótarstillingar á keyrsluviðmóti framleiðslugólfs*

### <a name="enable-the-my-jobs-tab"></a>Virkja flipann störfin mín

Flipinn **Störfin mín** gerir starfskröftum kleift að skoða auðveldlega öll óbyrjuð og ókláruð verk sem þeim er úthlutað sérstaklega. Það er gagnlegt í fyrirtækjum þar sem verk er stundum eða alltaf úthlutað til tiltekinna starfskrafta (mannauður) í stað annarra gerða tilfanga (svo sem véla).

Til að nota þennan eiginleika skaltu kveikja á eftirfarandi eiginleika í [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- *Flipinn „Verkin mín“ í keyrsluviðmóti framleiðslugólfs*

### <a name="enable-use-of-a-numpad-on-the-sign-in-page"></a>Virkja notkun á talnaborði á innskráningarsíðunni

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: Preview until 10.0.31 GA -->

Þessi eiginleiki gerir stjórnendum kleift að bæta talnaborðsstjórnun við innskráningarsíðuna fyrir keyrsluviðmót framleiðslugólfs. Starfskraftar geta notað talnaborðið til að skrá sig inn með kortakenni eða kennitölu.

Til að nota þennan eiginleika skaltu kveikja á eftirfarandi eiginleika í [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- *Virkja notkun á talnaborði á innskráningarsíðunni*

## <a name="work-with-production-floor-execution-configurations"></a>Vinna með skilgreiningar á keyrslum framleiðslugólfs

Til að stofna og vinna með skilgreiningar á keyrslum framleiðslugólfs skal fara í **Framleiðslustýringu \> Uppsetning \> Framkvæmd framleiðslu \> Grunnstilla framkvæmd á framleiðslugólfi**. Síðan **Grunnstilla framkvæmd á framleiðslugólfi** sýnir lista yfir fyrirliggjandi skilgreiningar. Á þessari síðu er hægt að framkvæma eftirfarandi aðgerðir:

- Veljið einhverja skilgreiningu framleiðslugólfs sem sýnd er í vinstri dálknum til að skoða og breyta henni.
- Veljið **Ný** á aðgerðasvæðinu til að bæta nýrri skilgreiningu við listann. Síðan skal færa í reitinn **Skilgreining** heiti til að auðkenna nýju skilgreininguna. Heitið sem fært er inn verður að vera einkvæmt á milli allra skilgreininga og ekki er hægt að breyta því síðar. Í reitinn **Lýsing** er valfrjálst að slá inn lýsingu á skilgreiningunni.

Næst skal stilla hinar ýmsu stillingar fyrir valda skilgreiningu, eins og lýst er í eftirfarandi undirköflum.

### <a name="the-general-fasttab"></a>Flýtiflipinn Almennt

Eftirfarandi stillingar eru tiltækar á flýtiflipanum **Almennt**:

- **Aðeins inn- og útstimplun** - Stillið þennan valkost á *Já* til að búa til einfaldara viðmót sem býður aðeins upp á inn- og útstimplunarvirkni. Þessi stilling óvirkjar flesta aðra valmöguleika á þessari síðu. Fjarlægja verður allar færslubókarlínur úr **Flipavali** áður en hægt er að virkja þennan valkost.
- **Virkja leit** - Stilltu þennan valkost á *Já* til að taka leitarreit með á verkefnalistann. Starfskraftar geta fundið tiltekið starf með því að slá inn auðkenni starfsins eða finna öll störf fyrir tiltekna pöntun með því að slá inn kenni pöntunarinnar. Starfskraftar geta slegið inn kennið með því að nota lyklaborð eða með því að skanna strikamerki.
- **Virkja leit eftir verkkenni** – Stillið þennan valkost á *Já* til að gera starfskröftum kleift að leita eftir verkefni (til viðbótar við vinnu- og pöntunarkenni) í leitarsvæði viðmóts fyrir framkvæmd á framleiðslugólfi. Aðeins er hægt að stilla þennan valkost á *Já* þegar valkosturinn **Virkja leit** er einnig stilltur á *Já*.
- **Opna svarglugga upphafs sjálfkrafa** Þegar þessi valkostur er stilltur á *Já* er svargluggi **Hefja vinnslu** opnaður sjálfkrafa þegar starfskraftur nota leitarstikuna til að leita að verki.
- **Opna svarglugga skýrsluframvindu sjálfkrafa** Þegar þessi valkostur er stilltur á *Já* er svargluggi **Tilkynna um framvindu** opnaður sjálfkrafa þegar starfskraftur nota leitarstikuna til að leita að verki.
- **Virkja leiðréttingu á efni** – Stilltu þennan valkost á *Já* til að virkja hnappinn **Breyta efni** í svarglugganum **Tilkynna framvindu**. Starfsmenn geta valið þennan hnapp til að stilla efnisnotkun fyrir verkið.
- **Tilkynna magn við útstimplun** - Stillið þennan valkost á *Já* til að biðja starfsmenn að senda inn athugasemd um verk í vinnslu við útstimplun. Þegar þessi valkostur er stilltur á *Nei* verða starfsmenn ekki beðnir um þetta.
- **Læsa starfsmanni** - Þegar þessi valkostur er stilltur á *Nei* verða starfsmenn skráðir strax út eftir að þeir eru búnir að gera skráningu (t.d. nýtt verk). Viðmót fer síðan aftur á innskráningarsíðuna. Þegar þessi valkostur er stilltur á *Já* haldast starfskraftur innskráðir í keyrsluviðmóti framleiðslugólfs. Hins vegar getur starfsmaður skráð sig út handvirkt svo annar starfsmaður geti skráð sig inn á meðan keyrsluviðmót framleiðslugólfs er keyrt áfram undir sama reikningi kerfisnotanda. Nánari upplýsingar um þessar gerðir reikninga er að finna í [Úthlutaðir notendur](config-job-card-device.md#assigned-users).
- **Nota rauntíma skráningar** - Stillið þetta á *Já* til að stilla tímann fyrir hverja nýja skráningu þannig að hún jafngildi þeim tíma þegar starfsmaðurinn sendi inn skráninguna. Þegar þessi valkostur er stilltur á *Nei* er innskráningartíminn notaður í staðinn. Þú vilt yfirleitt stilla þennan valkost á *Já* ef þú hefur stillt valkostina **Læsa starfsmanni** og/eða **Einn starfsmaður** á *Já* þar sem starfsmenn eru oft innskráðir í lengri tíma.
- **Einn starfskraftur** – Stillið þennan valkost á *Já* ef aðeins einn starfskraftur notar hvert keyrsluviðmót framleiðslugólf þar sem þessi grunnstilling er virk. Þegar þessi valkostur er stilltur á *Já* er valkosturinn **Loka á starfsmann** sjálfkrafa stilltur á *Já*. Að auki fjarlægir þessi valkostur kröfu (og getu) um að starfsmaður skrái sig inn með kortakenni (eða sambærilegu auðkenni). Þess í stað skráir starfsmaðurinn sig inn í Microsoft Dynamics 365 Supply Chain Management með reikningi kerfisnotanda sem er tengdur við *tímaskráðan starfsmann* (úr töflunni *starfskraftar*) og skráist inn í keyrsluviðmót framleiðslugólfs sem þessi starfsmaður á sama tíma.
- **Virkja talnaborð** – Stillið þennan valkost á *Já* til að bæta talnaborði við innskráningarskjáinn, sem gerir starfsmönnum kleift að slá inn spjaldkenni eða einkanúmer með á talnaborði á skjánum. Stilltu þennan möguleika á *Nei* til að fela talnaborðið.
- **Leyfa að læsa snertiskjá** - Stillið þennan valkost á *Já* til að leyfa starfskrafti að læsa snertiskjá viðmót fyrir framkvæmd á framleiðslugólfi svo þeir geti þrifið hann. Þegar þessi valkostur er stilltur á *Já* er hnappi **Læsa skjá fyrir hreinsun** bætt við inn á innskráningarsíðu. Þegar starfsmaður velur þennan hnapp læsist snertiskjárinn tímabundið til að koma í veg fyrir óvæntan innslátt. Niðurteljari er einnig sýndur. Starfsmaðurinn getur þá þrifið skjáinn og tækið með góðu móti. Þegar niðurtalningu er lokið aflæsist snertiskjárinn sjálfkrafa.
- **Lengd skjálæsingar** - Þegar valkosturinn **Leyfa læsingu snertiskjás** er stilltur á *Já* skal nota þennan valkost til að tilgreina fjölda sekúndna sem snertiskjárinn á að vera læstur vegna þrifa. Tímalengd verður að vera 5 til 120 sekúndur.
- **Mynda númeraplötu** - Stillið þennan valkost á *Já* til að mynda nýja númeraplötu í hvert sinn sem starfsmaður notar keyrsluviðmót framleiðslugólfs til að skrá sem lokið. Númeraplötunúmerið er myndað úr númeraröð sem er sett upp á síðunni **Færibreytur vöruhúsakerfis**. Þegar þessi valkostur er stilltur á *Nei* verða starfsmenn að tilgreina fyrirliggjandi númeraplötu þegar þeir tilkynna lok.
- **Prenta merki** - Stillið þennan valkost á *Já* til að prenta nýja númeraplötumerki í hvert sinn sem starfsmaður notar keyrsluviðmót framleiðslugólfs til að skrá sem lokið. Skilgreining merkisins er sett upp í skjalaleið, eins og lýst er í [Útlit merkimiða skjalasendinga](../warehousing/document-routing-layout-for-license-plates.md).

### <a name="the-tab-selection-fasttab"></a>Flýtiflipinn Val á flipa

Notaðu stillingarnar á flýtiflipanum **Flipaval** til að velja hvaða flipar í keyrsluviðmóti framleiðslugólfsins eiga að sýna þegar núverandi stillingar eru virkar. Hægt er að hanna eins marga flipa og þarf að bæta við og raða þeim hér eins og nauðsynlegt er með því að nota hnappana á tækjastiku flýtiflipans. Frekari upplýsingar um hvernig á að hanna flipa og vinna með stillingar hér er að finna á [Hanna viðmótið fyrir framkvæmd á framleiðslugólfi](production-floor-execution-tabs.md).

### <a name="the-report-progress-fasttab"></a>Flýtiflipi framvindu skýrslu

Eftirfarandi stillingar eru tiltækar á flýtiflipanum **Tilkynna um framvindu**:

- **Virkja leiðréttingu á efni** – Stilltu þennan valkost á *Já* til að taka með hnappinn **Breyta efni** í svarglugganum **Tilkynna framvindu**. Starfsmenn geta valið þennan hnapp til að stilla efnisnotkun fyrir verkið.
- **Sjálfgefið magn sem eftir er** – Stillið þennan valkost á *Já* til að foráfylla það magn sem eftir er af væntanlegu magni fyrir framleiðsluverk í svarglugganum **Tilkynna framvindu**.

## <a name="clean-up-job-configurations"></a>Skilgreiningar á hreinsunarvinnu

Þegar umsjónarmaður vinnusalar setur upp keyrsluviðmót framleiðslugólfsins, velur hann skilgreiningu og vinnusíu. Þetta val er vistað í tilvísunartöflu í Supply Chain Management og vafrinn notar kenni sem er geymt í staðbundinni köku til að finna réttu línuna í þeirri töflu. Taflan skráir líka dagsetninguna og tímann sem starfsmaður var síðast innskráður í hvert tæki.

Runuvinnslu hreinsar reglulega færslur í tilvísanatöflunni fyrir tæki sem hafa ekki skráð neinar aðgerðir síðustu 60 daga. Einnig er hægt að hreinsa færslurnar handvirkt hvenær sem er með því að fylgja þessum skrefum.

1. Farið í **Framleiðslustýring \> Uppsetning \> Framkvæmd framleiðslu \> Grunnstilla framkvæmd á framleiðslugólfi**.
1. Á aðgerðasvæðinu skal velja **Hreinsa biðlaragrunnstillingar**.
1. Í svarglugganum **Hreinsa biðlaragrunnstillingu** skal stilla reitinn **Fjöldi daga** á dagafjölda án aðgerða (á undan deginum í dag) sem á að taka til greina. Allar skilgreiningar og innskráningarfærslur eru fjarlægðar fyrir tæki sem hafa ekki verið virk á þessum tíma.
1. Veljið **Í lagi** til að hreinsa út viðeigandi skilgreiningar byggt á stillingunni **Fjöldi daga**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
