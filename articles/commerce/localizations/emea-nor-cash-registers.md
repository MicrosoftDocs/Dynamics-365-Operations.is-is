---
title: Afgreiðslukassavirkni fyrir Noreg
description: Þetta efni veitir yfirlit yfir virkni sjóðakassa sem er í boði fyrir Noreg í Microsoft Dynamics 365 Commerce, og veitir leiðbeiningar um uppsetningu virkninnar.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2017-10-31
ms.openlocfilehash: bb87b3a7405ef3d8435748813fa66db74b8f0971
ms.sourcegitcommit: 0d2de52e12fdb9928556d37a4813a67b303695dc
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 12/21/2021
ms.locfileid: "7944941"
---
# <a name="cash-register-functionality-for-norway"></a>Afgreiðslukassavirkni fyrir Noreg

[!include[banner](../includes/banner.md)]

Þetta efni veitir yfirlit yfir virkni sjóðsvéla sem er í boði fyrir Noreg í Dynamics 365 Commerce. Það veitir einnig leiðbeiningar um uppsetningu virkninnar. Virknin samanstendur af eftirfarandi hlutum:

- Algengar sölustaða (POS) eiginleikar sem eru í boði fyrir viðskiptavini í öllum löndum eða svæðum. Sem dæmi má nefna valmöguleika sem gerir þér kleift að koma í veg fyrir að afrit af kvittun sé prentað oftar en einu sinni.
- Noregssértækir eiginleikar, svo sem stafrænar undirskriftir fyrir söluviðskipti.

## <a name="overview-of-cash-register-functionality-for-norway"></a>Yfirlit yfir virkni peningakassa fyrir Noreg

### <a name="common-pos-features"></a>Algengar POS eiginleikar

Til að fræðast um POS eiginleika sem eru í boði fyrir viðskiptavini í öllum löndum eða svæðum, sjá [Hjálparúrræði fyrir Dynamics 365 Retail](../index.md).

Eftirfarandi POS staðsetningareiginleikar sem áður voru innleiddir og gerðir aðgengilegir viðskiptavinum í öllum löndum eða svæðum er nú hægt að nota sérstaklega fyrir Noreg:

- **Prentaðu textareiti á kvittun í stórri leturstærð.** Þú getur notað **Leturstærð** færibreytu í kvittunarsniðshönnuður til að tilgreina að stóra leturstærð ætti að nota fyrir reit á kvittunarsniði. (Stóra leturstærðin er um það bil tvöfalt hærri en venjulega leturstærð.) Til dæmis er hægt að nota þessa færibreytu til að prenta "Copy" vísirinn á afrit af kvittun með stórum stöfum.
- **Skráðu prentun kvittunarafrita í atburðaskrá POS endurskoðunar.** Þú getur notað **Endurskoðun** færibreytu í POS virknisniðinu til að gera kleift að prenta afrit af kvittunum og skrá aðra POS endurskoðunaratburði. Endurskoðunarviðburðirnir eru skráðir í gagnagrunn rásarinnar og í höfuðstöðvum. Þú getur skoðað endurskoðunarviðburðina á **Endurskoðunarviðburðir** síðu.
- **Koma í veg fyrir að afrit af kvittun sé prentað oftar en einu sinni.** Þegar **Endurskoðun** færibreytan í POS-virknisniðinu er virkjuð, the **Leyfa prentun kvittunarafrita** POS heimild stjórnar hvort hægt sé að prenta afrit af kvittunum. Það er líka valkostur sem gerir þér kleift að koma í veg fyrir að afrit af kvittun sé prentað oftar en einu sinni.

Að auki var eftirfarandi POS eiginleiki innleiddur fyrir Noreg en gerður aðgengilegur viðskiptavinum í öllum löndum eða svæðum:

- **Skráðu viðbótarviðburði í atburðaskrá POS endurskoðunar.** Ef **Endurskoðun** færibreytan í POS virknisniðinu er virkjuð, eftirfarandi atburðir eru skráðir í POS endurskoðunaratburðaskrá:

    - Verðkannanir
    - Skattafföll
    - Leiðréttingar á línumagni
    - Hreinsun færslur úr rásargagnagrunni

### <a name="norway-specific-pos-features"></a>Noregs-sértækir POS eiginleikar

Eftirfarandi POS-eiginleikar fyrir Noreg eru virkjaðir þegar **ISO kóða** færibreytan í POS-virknisniðinu er stillt á **Nei**.

#### <a name="digital-signing-of-sales-transactions"></a>Stafræn undirritun söluviðskipta

Sérhver söluviðskipti eru stafrænt undirrituð. Undirskriftin er búin til og skráð í færslubók POS á sama tíma og gengið er frá færslunni. Undirskriftin er einnig aðgengileg í dagbókinni sem er flutt út í endurskoðunarskyni.

Aðeins færslur vegna staðgreiðslu eru undirritaðar. Hér eru nokkur dæmi um viðskipti sem eru útilokuð frá undirritunarferlinu:

- Fyrirframgreiðslur (innborgun á viðskiptareikningi)
- Fyrirframgreiðslur fyrir sölupantanir (innborgun viðskiptavinapöntunar)
- Útgáfa gjafakorts
- Viðskipti sem ekki eru sölu (flot færsla, fjarlæging tilboðs, og svo framvegis)

Gögnin sem eru undirrituð eru textastrengur sem samanstendur af eftirfarandi gagnareitum. Gagnareitirnir eru aðskildir með semíkommum.

1. Fyrri undirskrift fyrir sama POS (núll\[**0**\] er notað fyrir fyrstu færsluna.)
2. Færsludagsetning
3. Færslutími
4. Röð undirritað viðskiptanúmer
5. Viðskiptaupphæð með skatti
6. Viðskiptaupphæð án skatts

Stafræna undirskriftarferlið notar RSA 1024-bita lykil sem hefur SHA-1 kjötkássaaðgerð (RSA-SHA1-1024). Vottorð sem er sett upp á Commerce Scale Unit er notað til undirritunar. Einkvæmt auðkenni vottorðsins (fótspor) er skráð ásamt undirskriftinni.

Undirskriftin er geymd í gagnagrunni verslana og gagnagrunni höfuðstöðva (HQ) ásamt viðskiptagögnum. Þú getur skoðað færsluundirskriftina, ásamt færslugögnunum sem voru notuð til að búa hana til, á **Viðskipti í ríkisfjármálum** Flýtiflipi á **Verslunarviðskipti** síðu.

#### <a name="receipts"></a>Móttökur

Kvittanir fyrir Noreg geta innihaldið viðbótarupplýsingar sem voru útfærðar með því að nota sérsniðna reiti:

- **Titill kvittunar** – Þú getur bætt reit við útlit kvittunarsniðs til að auðkenna tegund kvittunar. Til dæmis mun sölukvittun innihalda textann „Sölukvittun“.
- **Undirritað viðskiptaröðnúmer** – Raðnúmer undirritaðrar færslu getur birst á kvittuninni til að tengja prentaða kvittun við stafræna undirskrift í gagnagrunninum.
- **Samtölur kvittunar** – Sérsniðnir reitir fyrir heildarupphæðir innhreyfinga útiloka upphæðir sem ekki eru til sölu frá heildarupphæðum færslu. Fjárhæðir sem ekki eru í sölu innihalda upphæðir fyrir eftirfarandi aðgerðir:

    - Fyrirframgreiðslur (innborgun á viðskiptareikningi)
    - Fyrirframgreiðslur fyrir sölupantanir (innborgun viðskiptavinapöntunar)
    - Útgáfa gjafakorts
    - Að bæta fé á gjafakort

#### <a name="x-and-z-reports"></a>X og Z greinir frá

Upplýsingarnar sem koma fram í X og Z skýrslum eru byggðar á norskum kröfum. Til dæmis, **Heildarsala í reiðufé** upphæðir innihalda aðeins upphæðir fyrir staðgreiðsluviðskipti og undanskilja útgáfu gjafakortaaðgerða og fyrirframgreiðslu. Heildarsala í reiðufé er einnig skráð eftir vöruflokki og greiðslumáta. Að auki uppsafnað **Heildarsala** og **Heildarávöxtun** upphæðum er viðhaldið og prentað.

#### <a name="saf-t-cash-register-audit-file"></a>Endurskoðunarskrá SAF-T sjóðsskrár

Hægt er að flytja út POS-færslubókina á forskilgreindu sniði staðlaðrar endurskoðunarskrár - Skattur (SAF-T) Cash Register. Endurskoðunarskráin inniheldur upplýsingar um stofnunina, viðeigandi aðalgögn (svo sem vöruflokka, vörur og skattakóða), gögn um staðgreiðsluviðskipti ásamt undirskriftum fyrir þær færslur, gögn sem ekki eru um söluviðburði og skýrslugögn í lok dags. .

Hægt er að flytja út endurskoðunarskrána fyrir eftirfarandi aðstæður:

- Á hverja verslun
- Allar verslanir
- Á hverja flugstöð
- Allar útstöðvar

Einnig er hægt að senda skýrslu frá einum lögaðila fyrir hönd annars lögaðila. Í þessu tilviki verður þú að keyra útflutninginn frá starfandi lögaðila og tilgreina lögaðila sem tilkynnir sem sendanda skýrslunnar.

SAF-T Cash Register sniðið er innleitt í höfuðstöðvum með því að nota [Rafræn skýrslugerð](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md). 

## <a name="setting-up-commerce-for-norway"></a>Að setja upp verslun fyrir Noreg

Þessi hluti lýsir stillingum sem eru sértækar og mælt er með fyrir Noreg. Fyrir frekari upplýsingar, sjá [Hjálparúrræði fyrir Dynamics 365 Retail](../index.md).

Til að nota Noreg-sértæka virkni verður þú að klára þessi verkefni:

- Stilltu **Land/svæði** sviði til **NOR** (Noregur) í aðal heimilisfangi lögaðilans.
- Stilltu **ISO kóða** sviði til **NEI** (Noregur) í POS virknisniði allra verslana sem eru staðsettar í Noregi.

Þú verður einnig að tilgreina eftirfarandi stillingar fyrir Noreg.

### <a name="set-up-the-legal-entity"></a>Settu upp lögaðilann

Gakktu úr skugga um að nafn lögaðilans sé tilgreint. Þetta nafn verður prentað á X og Z skýrslur.

Að auki, á **Upplýsingar um bankareikning** flýtiflipann, í **Leiðarnúmer** reit, tilgreinið fyrirtækisnúmer.

### <a name="set-up-value-added-tax-vat-per-norwegian-requirements"></a>Settu upp virðisaukaskatt (VSK) í samræmi við norskar kröfur


Þú verður að búa til VSK-kóða, VSK-flokka og VSK-flokka vöru. Þú verður einnig að setja upp upplýsingar um söluskatt fyrir vörur og þjónustu. Fyrir frekari upplýsingar um hvernig á að setja upp og nota söluskatt, sjá [Söluskattyfirlit](../../finance/general-ledger/indirect-taxes-overview.md).

Þú verður einnig að tilgreina VSK-flokka og virkja **Verð eru með söluskatti** valkostur fyrir verslanir sem eru staðsettar í Noregi.

### <a name="set-up-functionality-profiles"></a>Settu upp virknisnið

Þú verður að virkja endurskoðun og setja upp númerun kvittunar.

### <a name="update-pos-permissions-groups-and-individual-permission-settings-for-store-workers"></a>Uppfærðu POS heimildahópa og einstakar heimildastillingar fyrir starfsmenn verslunarinnar

Stilltu **Leyfa prentun kvittunarafrits** leyfi að viðeigandi gildi:

- **Leyfðu alltaf** – Rekstraraðili getur prentað afrit af kvittun mörgum sinnum.
- **Leyfa aðeins einu sinni** – Rekstraraðili getur aðeins prentað afrit af kvittun einu sinni.
- **Leyfa aðeins einu sinni og aðeins ef HQ DB er tiltækt** – Rekstraraðili getur aðeins prentað afrit af kvittun einu sinni og aðeins ef HQ gagnagrunnurinn er tiltækur í gegnum Commerce Data Exchange : Rauntímaþjónusta, þannig að kerfið geti sannreynt að engin afrit af kvittuninni hafi áður verið prentuð í neinni verslun.
- **Aldrei** – Rekstraraðili getur ekki prentað afrit af kvittun.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Stilltu sérsniðna reiti þannig að hægt sé að nota þá á kvittunarsniði fyrir sölukvittanir

Á **Tungumálatexti** síðu, bætið við eftirfarandi skrám fyrir merki sérsniðnu reitanna fyrir kvittunarútlit. Athugið að **Tungumálakenni**, **·**, og **Texti** gildin sem eru sýnd í töflunni eru aðeins dæmi. Þú getur breytt þeim til að uppfylla kröfur þínar.

| Kenni tungumáls | Texti                   | Textakenni |
|-------------|------------------------|---------|
| en-US       | Titill kvittunar          | 900011  |
| en-US       | Er gjafakort           | 900012  |
| en-US       | Samtala (sala)          | 900013  |
| en-US       | Samtala skatts (sala)      | 900014  |
| en-US       | Samtala með skatti (sala) | 900015  |
| en-US       | Skattupphæð (sala)     | 900016  |
| en-US       | Færsluauðkenni reiðufés    | 900017  |

Á **Sérsniðnir reitir** síðu skaltu bæta við eftirfarandi færslum fyrir sérsniðna reiti fyrir útlit kvittunar. Athugið að **Textaauðkenni fyrir texta** gildi verða að samsvara **Textaauðkenni** gildi sem þú tilgreindir á **Tungumálatexti** síðu.

| Heiti                            | Gerð    | Textakenni myndatexta |
|---------------------------------|---------|-----------------|
| Titill kvittunar                    | Innhreyfing | 900011          |
| IsGiftCard                      | Innhreyfing | 900012          |
| SalesTotalExt                   | Innhreyfing | 900013          |
| TaxTotalExt                     | Innhreyfing | 900014          |
| TotalWithTaxExt                 | Innhreyfing | 900015          |
| AmountPerTaxExt                 | Innhreyfing | 900016          |
| CashTransactionSequentialNumber | Innhreyfing | 900017          |

> [!NOTE]
> Það er mikilvægt að þú tilgreinir rétt sérsniðin svæðisheiti eins og þau eru skráð í töflunni hér að ofan. Rangt sérsniðið heiti svæðis mun valda því að gögn vantar í kvittanir.

### <a name="configure-receipt-formats"></a>Stilltu kvittunarsnið

Fyrir öll nauðsynleg kvittunarsnið, breyttu gildinu **Prenthegðun** sviði til **Alltaf að prenta** fyrir kvittunarsniðið.

Í kvittunarsniðshönnuður skaltu bæta eftirfarandi sérsniðnum reitum við viðeigandi kvittunarhluta. Athugaðu að svæðisnöfn samsvara tungumálatextanum sem þú skilgreindir í fyrri hlutanum.

1. Fyrirsögn:

    - **Titill kvittunar** – Þessi reitur auðkennir tegund kvittunar.
    - **Auðkenni reiðufjárfærslu** – Þessi reitur prentar raðnúmer undirritaðrar reiðufjárfærslu.

2. Línur:

    - **Er gjafakort** – Þessi reitur merkir kvittunarlínuna sem tengda aðgerðinni Gefa út gjafakort eða Bæta við gjafakort.

3. Fótur:

    - **Samtals (sala)** – Þessi reitur prentar út heildarsöluupphæð kvittunarinnar í reiðufé. Upphæðin er án skatts. Fyrirframgreiðslur og gjafakortaaðgerðir eru undanskildar.
    - **Heildarskattur (sala)** – Þessi reitur prentar út heildarskattupphæð kvittunarinnar fyrir staðgreiðslusölu. Fyrirframgreiðslur og gjafakortaaðgerðir eru undanskildar.
    - **Samtals með sköttum (sölu)** – Þessi reitur prentar út heildarsöluupphæð kvittunarinnar í reiðufé. Upphæðin inniheldur skatt. Fyrirframgreiðslur og gjafakortaaðgerðir eru undanskildar.
    - **Skattupphæð (sala)** – Þessi reitur prentar út skattupphæð kvittunar fyrir staðgreiðslusölu á skattkóða. Fyrirframgreiðslur og gjafakortaaðgerðir eru undanskildar.

Fyrir frekari upplýsingar um hvernig á að vinna með kvittunarsnið, sjá [Setja upp og hanna kvittunarsnið](../receipt-templates-printing.md).

### <a name="configure-the-saf-t-cash-register-export-format"></a>Stilltu útflutningssnið SAF-T Cash Register

Hægt er að hlaða niður SAF-T sjóðsskránni frá Microsoft Dynamics Lífsferilsþjónusta (LCS). Fyrir frekari upplýsingar, sjá [Flytja inn rafrænar skýrslustillingar](../../fin-ops-core/dev-itpro/analytics/electronic-reporting-import-ger-configurations.md). Þú verður að hlaða niður eftirfarandi stillingum:

- **Smásölurásargögn.útgáfa.1** – Uppsetning gagnalíkans.
- **DMM Retail channel data.version.1.14** – Uppsetning kortlagningar gagnalíkans.
- **NO SAF T Cash Register.version.1.20** – Sniðstillingin.

Eftir að þú hefur flutt inn stillingarnar, á **Viðskiptabreytur** síðu, á **Rafræn skjöl** flipa, í **SAF-T útflutningssnið fyrir sjóðvélar** reit, veldu nafn sniðstillingarinnar sem var flutt inn.

Þú verður einnig að varpa nauðsynlegum aðalgögnum til fyrirframskilgreindra SAF-T staðalkóða. Nánari upplýsingar er að finna í SAF-T sjóðsskrárskjölunum sem norska skattastofnunin veitir. Til að búa til kortlagninguna verður þú að stilla nýja **SAF-T Kóði gjaldkera** reit á eftirfarandi síðum:

- Vöruflokkar
- Greiðslumátar
- VSK-kóðar

### <a name="configure-channel-components"></a>Stilltu rásaríhluti

Til að virkja Noreg-sértæka virkni verður þú að stilla rásaríhluti. Fyrir frekari upplýsingar, sjá [leiðbeiningar um dreifingu](emea-nor-fi-deployment.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
