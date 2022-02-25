---
title: Vinna með breytingar á hönnunarafurðum
description: Þetta efnisatriði gefur upplýsingar um umsjón hönnunarbreytinga. Umsjón hönnunarbreytinga býður upp á skipulagða ferla til að stjórna breytingum á hönnunarafurðum, frá því að stinga upp á, leggja fram beiðni og gera breytingar til yfirferðar og samþykktar á breytingum, leggja mat á áhrif þeirra á fyrirliggjandi færslur og fylgja þeim eftir.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgEcmRequestSelection,EngChgEcmRequestProducts,EngChgEcmRequestPriorityChart,EngChgEcmRequestListPage,EngChgEcmRequestFilteredPart,EngChgEcmRequestDetails,EngChgEcmReason,EngChgEcmProjTableInformation,EngChgEcmProductRoute,EngChgEcmProductRelease,EngChgEcmProductPreview, EngChgEcmWhereUsed, EngChgEcmInventTrans,EngChgEcmHeaderSelection,EngChgEcmHeaderPreviewPart,EngChgEcmHeaderFilteredPart,EngChgEcmHeaderDetails, EngChgCaseWhereUsedAnalysis, EngChgCaseValidatorMessage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 93f5c3e4951784a6c4925b8f9026816bfaf551ee
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/09/2022
ms.locfileid: "8102911"
---
# <a name="manage-changes-to-engineering-products"></a>Vinna með breytingar á hönnunarafurðum

[!include [banner](../includes/banner.md)]

Umsjón hönnunarbreytinga býður upp á skipulagða ferla til að stjórna breytingum á hönnunarafurðum. Hægt er að nota ferlið *beiðni um hönnunarbreytingu* til að stinga upp á og leggja fram beiðni, og síðan nota ferlið *pöntun hönnunarbreytingar* til að gera þessar breytingar. Notendur geta stofnað beiðnir um hönnunarbreytingu eða pantanir hönnunarbreytingar og síðan er ferli sem fer yfir þetta og samþykkir, leggur mat á áhrif þeirra á fyrirliggjandi færslur og fylgir þeim eftir.

## <a name="engineering-change-requests"></a>Beiðnir um breytingu á hönnun

Beiðniferli hönnunarbreytinga gerir kleift að sækja beiðnir um breytingar frá öllum viðeigandi deildum innan fyrirtækisins. Það skiptir ekki máli hvort þú starfar sem hönnuður, eða í framleiðslu, innkaupum, vöruhúsi eða söludeild: allir geta notað beiðni um hönnunarbreytingu til að óska eftir breytingu. Þessi breyting gæti verið hugmynd um nýja afurð, vandamál sem þú tókst eftir meðan þú varst að vinna með fyrirliggjandi afurð, uppástunga til að bæta fyrirliggjandi afurð, eða eitthvað annað.

Þegar einhver hefur sent inn beiðni um breytingu, er ferlinu *yfirfara og samþykka* stjórnað af verkflæði sem finnur út hver þarf að samþykkja breytinguna (t.d. eigandi afurðarinnar).

Til að setja upp verkflæði fyrir pantanir og beiðnir um hönnunarbreytingar skal fara í **Umsjón hönnunarbreytinga \> Verkflæði hönnunar**. Veljið **Nýtt**, veljið hvort verkflæðið verði notað til að yfirfara pantanir hönnunarbreytinga eða beiðnir um hönnunarbreytingar og skilgreinið síðan verkflæðið.

Frekari upplýsingar um verkflæði er að finna í [Yfirlit yfir verkflæðiskerfi](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md). Frekari upplýsingar um eigendur afurða er að finna á [Eigendur afurða](product-owner.md).

### <a name="create-a-new-engineering-change-request"></a>Stofna nýja beiðni um hönnunarbreytingu

Til að stofna beiðni um hönnunarbreytingu skal fylgja einu af þessum skrefum.

- Farið í **Umsjón hönnunarbreytinga \> Almennt \> Umsjón hönnunarbreytinga \> Beiðnir um breytingu á hönnun** og veljið síðan **Ný** á aðgerðasvæðinu.
- Opnið síðuna **Upplýsingar um afurð** fyrir fyrirliggjandi hönnunarafurð. Síða, á aðgerðasvæðinu, í flipanum **Hönnun**, í flokknum **Umsjón hönnunarbreytinga**, skal velja **Beiðni um hönnunarbreytingu \> Ný beiðni um hönnunarbreytingu**.

Ný breytingabeiðni er stofnuð. Nú er hægt að stilla reitina fyrir hvern flýtiflipa eins og lýst er í eftirfarandi undirköflum.

#### <a name="general-fasttab"></a>Flýtiflipinn Almennt

Flýtiflipi **Almennt** gerir þér kleift að bjóða upp á almenna lýsingu á breytingabeiðninni. Eftirfarandi tafla lýsir reitunum í þessum flýtiflipa.

| Svæði | lýsing |
|---|---|
| Beiðni um breytingu | Færið inn heiti á beiðni hönnunarbreytingar. |
| Titill | Færið inn texta sem lýsir stuttlega eða greinir frá breytingunum í beiðninni. |
| Forgangur | Veljið gildi til að gefa til kynna hversu aðkallandi breytingin er. Hægt er að sérsníða tiltæk gildi fyrir fyrirtækið eins og þörf er á. (Frekari upplýsingar er að finna í [Koma á algengum gildum fyrir umsjón hönnunarbreytinga](engineering-change-management-setup.md).) |
| Tegund | Veljið gildi til að lýsa því hvers konar breytingu verið er að óska eftir. Hægt er að sérsníða tiltæk gildi fyrir fyrirtækið eins og þörf er á. (Frekari upplýsingar er að finna í [Koma á algengum gildum fyrir umsjón hönnunarbreytinga](engineering-change-management-setup.md).) |
| Villustig | Veljið gildi til að gefa til kynna alvarleika vandamálsins sem ætti að lagfæra með því að framkvæma beiðnina. Hægt er að sérsníða tiltæk gildi fyrir fyrirtækið eins og þörf er á. (Frekari upplýsingar er að finna í [Koma á algengum gildum fyrir umsjón hönnunarbreytinga](engineering-change-management-setup.md).) |
| Umbeðið af | Nafn notandans sem stofnaði beiðnina. |
| Kveikt | Dagsetningin þegar beiðnin var stofnuð. |
| Staða | Staða beiðninnar. Þegar beiðni er fyrst stofnuð er staðan *Stofnuð*. Þegar beiðnin er samþykkt breytist staðan í *Samþykkt*. Ef tengd breytingapöntun hefur verið stofnuð fyrir beiðnina breytist staðan í *Fylgst með*. |
| Breyta röð | Númer breytingapöntunar, ef breytingabeiðninni var fylgt eftir í gegnum breytingapöntun. |

#### <a name="information-fasttab"></a>Flýtiflipi upplýsinga

Flýtiflipinn **Upplýsingar** gerir kleift að bæta við meiri upplýsingum um beiðnina.

Til að bæta línu við hnitanetið skal velja **Ný** á tækjastikunni fyrir ofan hnitanetið og síðan velja einn af eftirfarandi valkostum:

- **Skrá** – Hlaða upp skrá.
- **Mynd** - Hlaðið upp myndaskrá.
- **Athugasemd** – Færið inn athugasemd beint í hnitanetið.
- **Vefslóð** – Sláið inn vefslóð beint í hnitanetið.

Eftirfarandi tafla lýsir reitunum í hverri línu.

| Svæði | lýsing |
|---|---|
| Tími og dagsetning stofnunar | Dagsetning og tími þegar línan var búin til. |
| Gerð | Gerð upplýsinganna sem línan var stofnuð fyrir (skrá, mynd, athugasemd eða vefslóð). |
| lýsing | Færa inn lýsingu fyrir línuna. |
| Takmörkun | Gildi sem tilgreinir hvort upplýsingarnar sem hefur verið bætt við komu frá innri eða ytri uppruna. |
| Meðfylgjandi | Valinn gátreitur gefur til kynna að línan feli í sér viðhengi (skrá eða mynd). Til að hlaða niður viðhenginu skal velja línuna og velja svo **Opna** á tækjastikunni fyrir ofan hnitanetið. |

#### <a name="products-fasttab"></a>Flýtiflipi afurða

Flýtiflipinn **Afurðir** gerir þér kleift að sýna hverja afurð sem verður fyrir áhrifum vegna breytingabeiðninnar. Hægt er að nota hnappana á tækjastikunni til að bæta afurðum við hnitanetið eða til að fjarlægja afurðir.

Þessi listi er aðeins ætlaður til upplýsinga. Þess vegna er hægt að bæta við eins mörgum tengdum afurðum og þú telur viðeigandi. Ef breytingabeiðni er stofnuð á síðunni **Upplýsingar um afurð** fyrir fyrirliggjandi afurð, þá ætti sú afurð að vera sýnd í flýtiflipanum **Afurðir** þegar búið er að vista færslu sem óskað er eftir.

#### <a name="source-fasttab"></a>Flýtiflipi gagnagjafa

Flýtiflipinn **Gagnagjafi** gerir kleift að rekja upprunastað breytingabeiðninnar. Hann er gagnlegur ef til dæmis á að skoða hvort breytingabeiðnin hafi verið stofnuð úr sölupöntun, hver stofnaði hana og hvaða í hvaða fyrirtæki hún var stofnuð.

### <a name="evaluate-the-business-impact-of-a-change-request-and-send-notifications"></a>Mat lagt á áhrif breytingabeiðninnar á reksturinn og senda tilkynningar

Þegar beiðni um breytingu er yfirfarin er hægt að leita að tengslum. Á þennan hátt er hægt að meta áhrif umbeðinnar breytingar á opnum færslum, svo sem sölupantanir, framleiðslupantanir og lagerbirgðir. Þegar farið er yfir breytingarbeiðnir er hægt að senda tilkynningar til þeirra aðila sem bera ábyrgð á að sinna ýmsum tegundum tengdra pantana.

#### <a name="review-affected-transactions-block-selected-transactions-and-send-notifications"></a>Farðu yfir viðkomandi færslur, lokaðu á valdar færslur og sendu tilkynningar

Fylgið eftirfarandi skrefum til að fara yfir viðkomandi færslur, loka á valdar færslur og senda tengdar tilkynningar.

1. Farið í **Umsjón hönnunarbreytinga \> Almennt \> Umsjón hönnunarbreytinga \> Beiðnir um breytingu á hönnun**.
1. Annaðhvort opnið fyrirliggjandi breytingabeiðni eða veljið **Ný** á aðgerðasvæðinu til að stofna nýja breytingabeiðni.
1. Á aðgerðasvæðinu, í flipanum **Beiðni um breytingu**, í flokknum **Rekstraráhrif**, skal velja einn af eftirfarandi hnöppum:

    - **Leita** - Skannar allar opnar færslur og opnar síðan svargluggann **Rekstraráhrif á opnar færslur**, sem sýnir allar færslur sem verða fyrir áhrifum vegna breytingarinnar.
    - **Skoða fyrri leit** - Opnið svargluggann **Rekstraráhrif á opnar færslur**, sem sýnir niðurstöður fyrri leitar. (Ekki er leitað að nýju.)

1. Svarglugginn **Rekstraráhrif á opnar færslur** býður upp á nokkra flipa sem sýna lista yfir færslur af tiltekinni gerð sem verða fyrir áhrifum (**Sölupantanir**, **Innkaupapantanir**, **Framleiðslupantanir**, **Birgðir** o.s.frv.). Í hverjum flipa kemur einnig fram fjöldi viðkomandi færslna af þeirri gerð. Veldu flipa til að skoða viðeigandi lista.
1. Til að vinna með færslu í listanum skal velja hana og síðan einn af eftirfarandi hnöppum á verkfærastikunni:

    - **Skoða færslu** – Opna valda færslu.
    - **Útiloka pöntun** – Þessi hnappur er aðeins á flipanum **Sölupantanir**. Veljið það til að loka fyrir valda sölupöntun.
    - **Útiloka línu** – Þessi hnappur er aðeins á flipanum **Sölupantanir**. Veljið það til að loka fyrir valda innkaupapöntunarlínu.
    - **Senda ábyrgðarmanni tilkynningu** – Þessi hnappur er aðeins á flipanum **Sölupantanir**. Veljið það til að senda tilkynningu um breytingar til notandans sem er settur sem ábyrgur fyrir valda sölupöntun. Frekari upplýsingar um hverjir geta séð tilkynningarnar og hvernig er að finna í [Yfirfara og vinna úr tilkynningum um breytingar á færslum](#review-notifications).
    - **Senda pöntunaraðila tilkynningu** – Þessi hnappur er aðeins á flipanum **Sölupantanir**. Veljið það til að senda tilkynningu um breytingu til notandans sem er valinn sem pöntunaraðili fyrir valda innkaupapöntun. Frekari upplýsingar um hverjir geta séð tilkynningarnar og hvernig er að finna í [Yfirfara og vinna úr tilkynningum um breytingar á færslum](#review-notifications).
    - **Tilkynna framleiðslu** – Þessi hnappur er aðeins á flipanum **Framleiðslupantanir**. Ólíkt sölu- og innkaupapantanum hafa framleiðslupantanir ekki einn einasta notanda sem er valinn sem ábyrgur fyrir þeim frá upphafi til enda. Í staðinn eigna ýmsir umsjónaraðilar eða skipuleggjendur sér tiltekið svæði eða tiltekinn hluta framleiðslunnar (til dæmis ákveðin tilföng eða tilfangaflokka). Þegar þú velur þennan hnapp fá fyrir vikið allir notendur sem bera ábyrgð tilföngum sem tengjast valinni framleiðslupöntun tilkynningu um breytingar. Frekari upplýsingar um hverjir geta séð tilkynningarnar og hvernig er að finna í [Yfirfara og vinna úr tilkynningum um breytingar á færslum](#review-notifications).
    - **Senda undirbúningsaðila tilkynningu** – Þessi hnappur er aðeins á flipanum **Innkaupabeiðnir**. Veljið það til að senda tilkynningu um breytingu til notandans sem er valinn sem undirbúningsaðili fyrir valda innkaupabeiðni. Frekari upplýsingar um hverjir geta séð tilkynningarnar og hvernig er að finna í [Yfirfara og vinna úr tilkynningum um breytingar á færslum](#review-notifications).
    - **Tilkynna ábyrgðarmanni sölu** – Þessi hnappur er aðeins á flipanum **Tilboð**. Veldu það til að senda tilkynningu um breytingu til notandans sem er valinn sem ábyrgur fyrir valið tilboð. Frekari upplýsingar um hverjir geta séð tilkynningarnar og hvernig er að finna í [Yfirfara og vinna úr tilkynningum um breytingar á færslum](#review-notifications).
    - **Úrkast** - Þennan hnapp er aðeins hægt að nálgast á flipanum **Birgðir**. Veldu það til að rýra valdar birgðir.
    - **Skoða feril** – Opna feril yfir aðgerðir sem gerðar hafa verið á völdu færslunni með því að nota svargluggann **Rekstraráhrif á opnar færslur**. (Ferillinn sýnir til dæmis hvort tilkynningar hafa verið sendar eða færslur hafa verið lokaðar.) 
    - **Skoða allar færslur** – Opna heildarlista yfir allar færslur, ekki bara opnar færslur.

> [!IMPORTANT]
> The **Tilkynna framleiðslu** hnappurinn er aðeins tiltækur ef *Verkfræðitilkynningar vegna framleiðslu* kveikt er á eiginleikanum fyrir kerfið þitt. Fyrir leiðbeiningar um hvernig á að kveikja eða slökkva á þessum eiginleika og forsendum hans, sjá [Yfirlit yfir verkfræðibreytingastjórnun](product-engineering-overview.md).

#### <a name="review-and-process-change-notifications-for-transactions"></a><a name="review-notifications"></a>Yfirfara og vinna úr tilkynningum um breytingar á viðskiptum

Þú getur lesið og unnið úr breytingartilkynningunum sem þú færð á eftirfarandi hátt:

- Nema þegar um er að ræða framleiðslupantanir, tilkynningar um breytingar sem þú berð ábyrgð á birtast í aðgerðamiðstöðinni. Hnappurinn **Sýna skilaboð** (bjöllutáknið) hægra megin á yfirlitsstikunni gefur til kynna hvenær skilaboð eru tiltæk fyrir núverandi notanda í aðgerðamiðstöðinni. Veljið hnappinn **Sýna skilaboð** til að opna aðgerðamiðstöðina og fara yfir skilaboðin.
- Til að skoða allar framleiðslupantanir þar sem tilkynning um hönnun hefur verið send skal fara í **Framleiðslupantanir \> Framleiðslupantanir \> Allar framleiðslupantanir**. Því næst skal á aðgerðasvæðinu, í flipanum **Framleiðslupöntun**, í flokknum **Beiðni um hönnunarbreytingu**, velja **Tilkynningar um hönnun** til að opna síðuna **Tilkynningar um hönnun**.
- Fyrir framleiðslupantanir er hægt að velja að skoða aðeins tilkynningar um breytingar sem eiga við um framleiðslutilföngin sem þú hefur umsjón með. Á vinnusvæðinu **Stjórnun á framleiðslugólfi**, á aðgerðasvæðinu, skal velja **Skilgreina eigið vinnusvæði** til að sía síðuna þannig að hún sýni aðeins upplýsingar um framleiðslueiningar, flokka og/eða tilföng sem þú hefur umsjón með. Í hlutanum **Samantekt** sýnir reitur sem heitir **Framleiðslupantanir með breyttum afurðum** fjöldann af tilkynningum sem passa við síustillingarnar. Veldu þennan reit til að opna síðuna **Tilkynningar um hönnun** sem sýnir heildarlista yfir færslur sem uppfylla skilyrði síunnar.

Þegar þú ert að fara yfir tilkynningar um framleiðslupantanir á síðunni **Tilkynningar um hönnun** geturðu notað tengla til að fara á tengdar breytingapantanir eða framleiðslupantanir með því að velja dálkagildi eða nota tengdar skipanir á aðgerðasvæðinu. Eftir að þú hefur lokið við að meta breytingu og eftir að þú hefur hætt við eða breytt framleiðslupöntunum eftir þörfum geturðu merkt tilkynningu sem leysta. Í aðgerðasvæðinu er síðan smellt á **Leysa úr**. Tilkynningin er fjarlægð úr öllum yfirlitum notenda.

> [!IMPORTANT]
> Getan til að senda tilkynningar um framleiðslupantanir krefst þess að *Verkfræðitilkynningar vegna framleiðslu* kveikt er á eiginleikum fyrir kerfið þitt. Fyrir leiðbeiningar um hvernig á að kveikja eða slökkva á þessum eiginleika og forsendum hans, sjá [Yfirlit yfir verkfræðibreytingastjórnun](product-engineering-overview.md).

### <a name="create-a-change-order-from-a-change-request"></a>Stofna breytingapöntun úr breytingabeiðni

Hönnuður sem fer yfir beiðni um hönnunarbreytingu getur stofnað pöntun hönnunarbreytingar beint af síðunni **Beiðnir um breytingu á hönnun**. Á aðgerðasvæðinu, í flipanum **Beiðni um breytingu**, í flokknum **Hönnunarbreytingapöntun**, skal velja **Afrita tengil og afurðir**.

## <a name="engineering-change-orders"></a>Raðir hönnunarbreytinga

Hönnunarbreytingapantanir bjóða upp á skipulagt ferli til að gera breytingar á hönnunarafurðum. Breytingar eru lagðar til með því að nota afrit af gögnum sem tengjast hönnuninni. Þetta hefur ekki áhrif á raunverulegu aðalgögnin. Frekari upplýsingar um gögn sem tengjast hönnuninni er að finna í [Hönnunarútgáfur og flokkar hönnunarafurðar](engineering-versions-product-category.md).

Hægt er að stofna hönnunarbreytingapöntun sem byggir á samþykktri hönnunarbreytingabeiðni. Hönnuðir geta einnig stofnað hönnunarbreytingapantanir frá grunni. Hægt er að taka margar afurðir með í eina hönnunarbreytingapöntun með því að fylgja einhverju þessara skrefa:

- Veljið afurðir handvirkt.
- Notið uppskriftir til að hafa með afurðir sem eru lægra í afurðarskipulaginu (þ.e. undireiningar).
- Notið leit að notkunarstað til að hafa með afurðir sem eru hærra í afurðarskipulaginu (þ.e. yfireiningar).

Eftir að tillögum að breytingum er lokið mun verkflæði sjá um yfirferðar- og samþykktarferlið. Hægt er að setja upp mismunandi verkflæði, byggt á forgangi og alvarleika.

Til að setja upp verkflæði fyrir pantanir og beiðnir um hönnunarbreytingar skal fara í **Umsjón hönnunarbreytinga \> Verkflæði hönnunar**. Veljið **Nýtt**, veljið hvort verkflæðið verði notað til að yfirfara pantanir hönnunarbreytinga eða beiðnir um hönnunarbreytingar og skilgreinið síðan verkflæðið.

Frekari upplýsingar um verkflæði er að finna í [Yfirlit yfir verkflæðiskerfi](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md).

Hér eru nokkrir dæmigerðir aðilar sem gætu þurft að samþykkja hönnunarbreytingapöntun:

- **Eigendur afurða** - Frekari upplýsingar um eigendur afurða er að finna á [Eigendur afurða](product-owner.md).
- **Ábyrgur stjórnandi teymis** - Reiturinn **Hönnuður** í yfirlitinu **Haus** fyrir hönnunarbreytingarpöntun sýnir hönnuðinn sem stofnaði hönnunarbreytingapöntunina. Ef hönnuðurinn tilheyrir teymi sem er skilgreint í kerfinu mun reiturinn **Ábyrgð** sýna stjórnanda þess teymis.
- **Fjármáladeild** - Fjármáladeildin gæti þurft að fara yfir mál þar sem breytingin hefur mikinn kostnað í för með sér.

Hægt er að velja hvort eigi að vinna úr hönnunarbreytingapöntun strax eftir samþykki, sem hluti af verkflæðinu, eða hvort gera eigi úrvinnsluna síðar, sem handvirkt skref. Þegar verið er að vinna úr hönnunarbreytingapöntun, verða hönnunargögn raunverulegrar afurðar uppfærð.

Meðan farið er yfir beiðir um breytingu, á aðgerðasvæðinu, í flipanum **Beiðni um breytingu**, í flokknum **Rekstraráhrif**, skal velja **Leita** til að leggja mat á áhrif framlagðrar breytingar á opnar færslur, t.d. sölupantanir, framleiðslupantanir og birgðir. Niðurstöðurnar eru sýndar í svarglugganum **Rekstraráhrif á opnar færslur**, þar sem hægt er að velja færslur sem verða fyrir áhrifum og síðan nota skipanir í tækjastikunni til að skoða frekari upplýsingar, láta ábyrgan notanda vita eða loka fyrir færsluna.

### <a name="engineering-change-orders-in-engineering-or-operational-companies"></a>Hönnunarbreytingapantanir í hönnunar- eða rekstrarfyrirtæki

Eins og lýst er í [Hönnunarfyrirtæki og reglur um eignarétt gagna](engineering-org-data-ownership-rules.md), er mismunandi hvaða afurðargögnum hægt er að breyta, en það fer eftir gerð lögaðila sem unnið er í (hönnunarfyrirtæki eða rekstrarfyrirtæki). Reglur um eignarétt gagna eiga einnig við um hönnunarbreytingapantanir. Þess vegna fer það eftir lögaðilanum, þar sem hönnunarbreytingapöntun er stofnuð, hvers konar breytingar hægt er að gera. Hér eru nokkur dæmi:

- Fyrir hönnunarbreytingapantanir í *hönnunarfyrirtæki* er hægt að gera einfaldar breytingar á hönnunargögnum. Til dæmis er hægt að búa til nýjar útgáfur af afurð, breyta skipulagi afurðar í gegnum uppskriftina og breyta eigindargildum hönnunar. Fyrir hverja afurð skal velja eitt eftirfarandi gilda í reitnum **Áhrif**:

    - **Ekkert** – Uppfæra fyrirliggjandi afurðarútgáfu (uppfærsla innan útgáfu).
    - **Ný útgáfa** – Stofna nýja útgáfu sem byggir á valinni afurðarútgáfu.
    - **Ný afurð** – Stofna alveg nýja afurð sem byggir á valinni afurðarútgáfu.
    - **Nýtt afbrigði** – Stofna nýtt afbrigði sem byggir á valdri afurðarútgáfu. Upplýsingar um uppskriftina og leiðina verða afritaðar.

- Í hönnunarbreytingapöntunum í *rekstrarfyrirtæki* er hægt að breyta skipulagsgögnum afurðarinnar. Til dæmis er hægt að bæta við fyrirliggjandi uppskrift með stillingum fyrir innkaupum, bæta við staðbundnum leiðum eða staðbundnar uppskriftir og jafnvel bæta við uppskrift með því að bæta við nýjum uppskriftarlínum fyrir staðbundið efni umbúða, smurvökva eða leiðbeiningar á staðbundnu tungumáli. Viðbætur sem notendur gera í rekstrarfyrirtækinu verður viðhaldið þegar nýjar uppfærslur eru sendar frá hönnunarfyrirtækinu. Frekari upplýsingar er að finna í [Hönnunarfyrirtæki og reglur um eignarétt gagna](engineering-org-data-ownership-rules.md).

    Þegar unnið er úr hönnunarbreytingapöntunum í hönnunarfyrirtækinu, eru afurðirnar aðeins búnar til og/eða uppfærðar í hönnunarfyrirtækinu. Þess vegna, ef einnig á að uppfæra aðalgögn afurðar, þarf einnig að losa afurðirnar til rekstrarfyrirtækja.

- Hægt er að losa afurðir beint úr hönnunarbreytingapöntunum. Opnið breytingarpöntunina og síðan, í aðgerðasvæðinu, í flipanum **Breytingapöntun**, í flokknum **Losun afurða**, skal velja **Skipulag afurðarlosunar**. Ferlið virkar á sama hátt og þegar afurðir eru losaðar af síðunni **Útgefnar afurðir**. Frekari upplýsingar er að finna í [Skipulag afurðarútgáfu](release-product-structure.md).
- Hægt er að losa afurðir sjálfkrafa úr hönnunarbreytingapöntunum byggt á eftirfarandi þáttum:

    - Endurútgáfur til fyrirtækja þar sem afurðir voru áður losaðar. Veljið **Leita** til að skanna allar fyrri útgáfur og veljið síðan **Skoða** til að skoða niðurstöðurnar. Síðan **Skoða** sýnir fyrri afurðarlosanir, og hægt er að velja hvaða afurðir á að endurútgefa. Lokið síðan síðunni **Skoða** og veljið **Vinna úr** til að endurútgefa valdar afurðir.
    - Sjálfvirkar útgáfustillingar í útgáfustjórnun afurðategund hönnunar. Hægt er að gera þessa losun sem hluta af verkflæðinu. Þegar blokkin **safna útgáfutillögum** er notuð, verður útgáfutillagan fyllt með tillögum um endurútgáfur (sjá fyrri listaatriði) og afurðir verða losaðar í fyrirtæki ef gátreiturinn **Sjálfvirk losun** er valinn í stjórnun útgáfu fyrir afurðategund hönnunar. Hægt er að velja **Skoða** til að skoða niðurstöðurnar eins og lýst er í fyrra listaatriði. Afurðirnar verða einnig losaðar þegar blokkin **vinna úr útgáfutillögum** er notuð. Ef aðeins er valið að safna útgáfutillögum sem hluti af verkflæðinu, er hægt að hefja útgáfuna handvirkt með því að velja **Vinna úr** eins og lýst er í fyrra listaatriði.

## <a name="follow-up-on-an-engineering-change-request-via-an-engineering-change-order"></a>Fylgja eftir beiðni um hönnunarbreytingu í gegnum hönnunarbreytingapöntun

Um leið og beiðni um hönnunarbreytingu er samþykkt, er hægt að fylgja henni eftir í gegnum hönnunarbreytingapöntun. Hægt er að sameina margar beiðnir um hönnunarbreytingar í eina hönnunarbreytingapöntun. Ein hönnunarbreytingapöntun getur jafnvel innihaldið margar afurðir. (Venjulega er þessi nálgun notuð þegar sömu breytingar verða að vera notaðar á margar afurðir.) Hins vegar er ekki hægt að búa til margar hönnunarbreytingapantanir úr einni beiðni um hönnunarbreytingu.

Til að fylgja eftir breytingabeiðni í gegnum breytingapöntun skal opna breytingabeiðnina og síðan, á aðgerðasvæðinu, í flipanum **Breytingapöntun**, í flokknum **Hönnunarbreytingapöntun**, skal velja **Afrita tengil og afurðir**. Síðan er hægt að velja fyrirliggjandi hönnunarbreytingapöntun til að tengja hönnunarbeiðnina við, eða hægt er að stofna nýja hönnunarbreytingapöntun fyrir þessa tilteknu beiðni.

## <a name="engineering-change-order-report"></a>Skýrsla um hönnunarbreytingaröð

Skýrsla um hönnunarbreytingapöntun lýsir breytingunum sem voru gerðar í hönnunarbreytingapöntun. Hún er gagnleg bæði meðan á ferli yfirferðar og samþykktar stendur og eftir það.

Til að skoða skýrslu um hönnunarbreytingapöntun skal opna viðeigandi breytingapöntun og síða, á aðgerðasvæðinu, í flipanum **Breytingapöntun**, í flokknum **Yfirlit**, skal velja **Skýrsla um hönnunarbreytingapöntun**.

## <a name="fields-on-an-engineering-change-order"></a>Reitir í hönnunarbreytingapöntun

Flestir reitir hönnunarbreytingapantana eru þeir sömu og reitirnir fyrir útgefnar afurðir, hönnunarútgáfur, skjöl, uppskriftir (línur) og leiðir (aðgerðir). Hins vegar tilheyra reitirnir í eftirfarandi töflu eingöngu breytingapöntunum.

| Svæði | lýsing |
|---|---|
| Ástæður hönnunarbreytingar | Veljið ástæðu fyrir því að breyta viðkomandi afurð. |
| Lýsing á breytingu | Færðu inn lýsingu á breytingunni. |
| Nauðsynlegt sérverkfæri | Tilgreinið hvort þörf er á sérstökum verkfærum til að koma breytingunni á. |
| Hönnun efnislosunar | Veljið ráðstöfunarkóða fyrir allan úrgang sem verður til þegar breytingin er gerð. |
| Samþykki viðskiptavinar er nauðsynlegt | Tilgreinið hvort krafist er samþykkis viðskiptavinar áður en hægt er að gera breytinguna. |
| Móttekið samþykki viðskiptavinar | Tilgreinið stöðuna á samþykki viðskiptavinar. |
| Umhverfisöryggi og heilbrigði | Tilgreinið hvort umhverfis- og öryggisreglur eiga við um breytinguna. Ef svo er, er hægt að velja viðeigandi reglur. |

Hægt er að nota hnappinn **Vinna með/afrita upplýsingar um breytingu** til að afrita upplýsingar um breytingu milli afurðanna sem er breytt.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
