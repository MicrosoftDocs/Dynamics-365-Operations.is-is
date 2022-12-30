---
title: GS1 strikamerki
description: Í þessari grein er lýst hvernig setja á upp GS1 strikamerki og QR-kóða svo hægt sé að skanna merkingar í vöruhúsi.
author: Mirzaab
ms.date: 03/21/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: e1c1c274054ed1c14c9b3fc0595baa029bf3124d
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336366"
---
# <a name="gs1-bar-codes"></a>GS1 strikamerki

[!include [banner](../includes/banner.md)]

Vöruhússtarfsmenn þurfa oft að ljúka nokkrum verkefnum þegar þeir nota skanna fyrir farsíma til að skrá hreyfingar vöru, spjalds eða geymis. Þessi verkefni geta falið í sér bæði að skanna strikamerkingar og færa inn upplýsingar handvirkt í fartækið. Strikamerkin nota tiltekið snið fyrirtækis sem þú skilgreinir og stjórnar með Microsoft Dynamics 365 Supply Chain Management.

GS1 strikamerki fyrir merkimiða voru þróuð til að bjóða upp á alþjóðlegan staðal fyrir gagnaskipti á milli fyrirtækja. Þær eru fáanlegar bæði í línulegum (1D) táknmyndum (strikamerkjasniðum), svo sem GS1-128 og 2D táknmyndum, svo sem GS1 DataMatrix og GS1 QR-kóða. GS1 strikamerki kóða ekki aðeins gögnin heldur leyfa þér einnig að nota fyrirfram skilgreindan lista af *auðkennum forrita* til að skilgreina merkingu gagnanna. GS1 staðallinn skilgreinir gagnasniðið og ýmis konar gögn sem hægt er að nota til að kóða. Ólíkt eldri strikamerkjastöðlum geta GS1-strikamerki haft marga gagnaþætti. Þess vegna getur ein skönnun á strikamerkjum náð yfir nokkrar tegundir vöruupplýsinga, eins og lotuna og fyrningardagsetninguna.

GS1 stuðningur í Supply Chain Management einfaldar verulega skönnunarferlið í vöruhúsum þar sem bretti og geymar eru merkt með því að nota strikamerki á GS1 sniði. Vöruhússtarfsmenn geta dregið út allar nauðsynlegar upplýsingar með einni skönnun á GS1 strikamerki. Með því að útiloka nauðsyn þess að gera margar skannanir og/eða slá inn upplýsingar handvirkt, hjálpa GS1 strikamerkin til við að minnka tímann sem tengist verkefnum. Um leið hjálpa þau einnig til við að bæta nákvæmni.

Skipulagsstjórar verða að setja upp nauðsynlegan lista yfir auðkenni forrita og tengja hvert þeirra við viðeigandi valmyndaratriði fyrir fartæki. Þá er hægt að nota auðkenni forritsins yfir vöruhús sem alhliða stillingu fyrir flutning og pökkun. Þess vegna munu allir merkimiðar fara fram á sameinuðu eyðublaði.

Nema annað sé tekið fram vísar hugtakið *strikamerki* í þessari grein bæði til línulegra strikamerkja (1D) og tvívíðra QR-kóða.

## <a name="the-gs1-bar-code-format"></a>GS1 strikamerkjasnið

GS1 almennar upplýsingar tilgreina hvaða tákn má nota fyrir GS1 strikamerki og hvernig á að kóða gögnin í strikamerkinu. Í þessum hluta er stuttur inngangur að greininni. Allar nánari upplýsingar er að finna í [Almennum forskriftum GS1](https://www.gs1.org/docs/barcodes/GS1_General_Specifications.pdf) sem GS1 gefur út. GS1 skilgreiningarskjalið er uppfært reglulega og upplýsingarnar sem það veitir eru uppfærðar með GS1 almennum skilgreiningum, útgáfu 22.0.

GS1-strikamerki nota eftirfarandi tákn:

- **Línuleg eða 1D-strikamerki** – GS1-128 og GS1 DataBar
- **2D strikamerki** – GS1 DataMatrix, GS1 QR-kóði og GS1 Dotcode

Athugaðu að minnst er sérstaklega á GS1 í GS1-128, sem er sérstakt tilvik af venjulegum kóða-128 línulegum strikamerkjum, GS1 DataMatrix, og GS1 QR-kóða. Munurinn á GS1 útgáfu og ekki GS1 útgáfu er að sérstakur stafur (FNC1) er til staðar sem fyrsti stafur í gögnum strikamerkisins. Tilvist FNC1 stafs gefur til kynna að túlka skuli gögnin í strikamerkinu í samræmi við GS1 skilgreininguna.

Gögnin í strikamerkinu sjálfu samanstanda af mörgum gagnaþáttum sem hver um sig er auðkenndur með auðkenni forritsins við upphaf reitsins. Venjulega eru gögnin einnig birt undir strikamerkinu á læsilegu sniði, þar sem kennimerki forritsins er sýnt í sviga. Eftirfarandi er dæmi: `(01) 09521101530001 (17) 210119 (10) AB-123`. Þetta strikamerki inniheldur þrjá þætti:

- **Kenni forrits 01** – GS1 Global Trade Item Number (GTIN) vörunnar.
- **Kennimerki forrits 17** – Lokadagur.
- **Kennimerki forrits 10** – Rununúmerið.

Fyrir hverja einingu gætu gögnin verið með fyrirfram skilgreinda lengd eða breytilega lengd. Það er fastlisti af kennum forrita sem hafa fyrirfram skilgreindar lengdir. Öll önnur auðkenni forrita eru með breytilega lengd og GS1 forritaauðkennalistinn tilgreinir hámarkslengd og snið gagna. Til dæmis er auðkenni forrits 01 með fyrirfram skilgreinda lengd 16 stafir (tveir fyrir auðkenni forritsins sjálfs og svo 14 fyrir GTIN) og auðkenni forrits 17 er með fyrirfram skilgreinda lengd átta stafir (tveir fyrir auðkenni forritsins sjálfs og svo sex fyrir dagsetninguna). Hins vegar er kenni forrits 10 með tveimur númerum fyrir sjálft kenni forrits og þá allt að 20 bók- og tölustöfum.

Þegar einingar eru settar saman ef eining fylgir einingu af breytilegri lengd, verður að nota skiltákn. Þessi skiltákn getur verið annað hvort sérstakur FNC1 stafur eða skiltákn flokksins (ekki prentanlegur stafur sem er með ASCII kóða 29 og sextándakerfiskóða 1D). Ekki ætti að nota skiltákn eftir síðastu eininguna. Þrátt fyrir að ekki ætti að nota skiltákn efti einingum sem hafa fyrirfram skilgreinda lengd er nærvera hans ekki mikilvæg villa.

Í strikamerkjagögnum frá fyrra dæmi um strikamerki sem inniheldur auðkenni forrits 01, 17 og 10 verða gögnin í kóða 128, QR-kóða eða DataMatrix tákni kóðuð sem `<FNC1>`**`01`**`09521101530001`**`17`**`210119`**`10`**`AB-123` (auðkenni forrits eru sýnd feitletruð). Best er að setja alla einingar sem hafa breytilega lengd í lokin, til að koma í veg fyrir þörf á viðbótarskiltákn hóps. Strikamerkið getur þó einnig haft aðra efnisröð, þar sem skiltáknið er áskilið. Eftirfarandi er dæmi: `<FNC1>`**`01`**`09521101530001`**`10`**`AB-123<GS>`**`17`**`210119`.

### <a name="dates-and-decimal-numbers"></a>Dagsetningar og tugabrot

Dagsetningar eru alltaf sýndar á sniðinu *ÁÁMMDD*, þar sem öld ársins er ákvörðuð með GS1 skilgreiningum. Aðeins er hægt að tákna dagsetningar frá 49 árum í fortíð til 50 ára í framtíðinni (miðað við yfirstandandi ár).

Sumar gagnaeiningar innihalda tugabrot. Til dæmis tákna kenni forrits 3100, 3101, ... 3105 nettóþyngd í kílóum. Þar sem þessi kenni forrita hafa fyrirfram skilgreinda lengd 10 eru sex tölur tiltækar fyrir magnið. Staðsetning tugabrotsins er tilgreind með síðasta númeri í kenni forritsins. Þess vegna er einnig hægt að tákna þennan hóp kenna forrita sem *310n*. Þar sem GS1-staðallinn tilgreinir að það þurfi alltaf að vera að minnsta kosti ein tala vinstra megin við tugabrotið, er heimilt að hámarki að nota fimm tugabrot.

Hér eru nokkur dæmi sem sýna hvernig talan *123456* verður túlkuð með mismunandi auðkenni forrita (sýnt feitletrað):

- **`3100`**`123456` &rarr; 123456 (heiltala)
- **`3101`**`123456` &rarr; 12345,6 (eitt tugasæti)
- **`3102`**`123456` &rarr; 1234,56 (tvö tugasæti)
- **`3103`**`123456` &rarr; 123,456 (þrír aukastafir)
- **`3104`**`123456` &rarr; 12,3456 (fjórir aukastafir)
- **`3105`**`123456` &rarr; 1,23456 (fimm aukastafir)

## <a name="scanning-gs1-bar-codes-in-supply-chain-management"></a>Skanna GS1-strikamerki í Supply Chain Management

Til að skanna GS1 strikamerki nota starfskraftar í vöruhúsi skanna sem er innbyggður í eða tengdur við fartæki. Skanninn sendir síðan skannaða strikamerkið í farsímaforrit vöruhúsakerfis sem röð lyklaborðstilvika. Þessi aðferð er einnig kölluð *Lyklaborð kortalesara* eða *Kortalesari*. Farsímaforritið sendir síðan móttekinn texta eins og hann kemur fyrir til Supply Chain Management. Þegar kerfið tekur á móti inntaksgögnum, ákvarðar það fyrst hvort gögnin byrja á einu af stilltu forskeytunum sem gefa til kynna að gögnin séu í raun GS1-strikamerki (sjá hlutann [Setja upp altæka valkosti GS1](#set-gs1-options)). Ef skönnuðu gögnin byrja ekki á einu af þessum forskeytum notar kerfið GS1 þáttara til að þátta gögnin og draga út einstök gögn í samræmi við auðkenni þeirra. Eftir að gögnunum hefur verið þáttað mun annað hvort núverandi inntaksreitur eða margir reitir verða fylltir út með skönnuðum gögnum.

### <a name="configuration-of-bar-code-scanner-hardware-and-software"></a>Stillingar á vélbúnaði og -hugbúnaði fyrir strikamerkjaskanna

Til að Supply Chain Management þekki og afkóða GS1 strikamerki á réttan hátt, verður að stilla vélbúnaðarskannann eða stuðningshugbúnaðinn til að framkvæma eftirfarandi aðgerðir:

- Bættu við forskeyti við skönnuðu strikamerkin til að kerfið geti þekkt GS1-strikamerki.
- Umbreyta óprentanlegu ASCII-skiltákninu (ASCII kóði 29 eða sextándakerfiskóða 1D) í prenthæfan staf, svo sem tilda (~).

Þó að þú getir bætt öllum forskeytum við skannaða strikamerkið er einn kostur að bæta við ISO/IEC 15424 auðkennistákn, einnig þekktur sem *AIM-auðkenni*. Þetta þriggja stafa auðkenni byrjar á `]`, hefur síðan einn staf sem auðkennir táknið sem er notuð og hefur síðan númer sem er notað sem frekari breytari. Til dæmis tilgreinir AIM-auðkennið `]C1` Kóða 128 strikamerki (vegna stafsins `C`) og breytirinn `1` tilgreinir að það sé FNC1 stafur í fyrstu stöðu gagnanna. Á hinn bóginn er `]C0` Code 128-strikamerki sem hefur einhvern annan staf sem fyrsta staf í gögnunum.

Eftirfarandi fimm kenni tákna samsvara GS1-strikamerkjum sem hafa einingar auðkenni forritsins:

- `]C1` – Kóði 128 (`C`) með FNC1-staf í fyrstu stöðu (`1`), einnig þekktur sem GS1-128.
- `]e0` – GS1 DataBar.
- `]d2` – DataMatrix (`d`) með ECC 200 og FNC1 í fyrstu stöðu (`2`), einnig þekkt sem GS1 DataMatrix.
- `]Q3` – QR-kóði (`Q`) Gerð 2 tákn með FNC1 í fyrstu stöðu (`3`), einnig þekktur sem GS1 QR-kóði.
- `]J1` – GS1 DotCode.

Ef þessi auðkenni eru notuð krefst samhæfi við önnur en GS1 strikamerki þess að skannar eða skönnunarhugbúnaður sé stilltur til að fjarlægja öll auðkenni sem samsvara ekki GS1 auðkennum. T.d. ef „venjulegt“ strikamerki með kóða 39 er skannað er forskeytinu `]A0` bætt við. Þar sem kerfið mun ekki skilja þetta forskeyti sem eitt af GS1 forskeytunum mun það túlka það sem gögn og gefa ófyrirsjáanlegar niðurstöður.

> [!NOTE]
> Til hægðarauka mun útgáfa 2.0.17.0 og síðar í farsímaforritinu Warehouse Management fjarlægja AIM-forskeyti sem eru ekki á fyrri listanum. Þessi hegðun styður tilvik þar sem þú getur stillt skannann til að bæta við AIM-forskeytinu en ekki til að fjarlægja óæskilegu forskeytin.

### <a name="single-and-multiple-field-scanning"></a>Skönnun á stökum og mörgum reitum

Eftir að gögn hafa verið þáttað úr strikamerkinu, verða þau mötuð inn í flæðisstýringar fartækisins. Það eru tvær aðferðir sem unnið verður úr í kjölfarið:

- **Skönnun á stökum reit** – Þessi aðferð fyllir aðeins út í reitinn sem strikamerkið var skannað inn í. Til dæmis, ef þú skannar strikamerkið `<FNC1>`**`01`**`09521101530001`**`17`**`210119`**`10`**`AB-123` á meðan bendillinn er í reitnum **Vara**, verður `09521101530001` GTIN úr strikamerkinu slegið inn í þann reit. Til dæmis, ef þú skannar strikamerkið á meðan bendillinn er í reitnum **Runukenni**, verður `AB-123` rununúmer úr strikamerkinu slegið inn í þann reit. Þessi stilling virkar fyrir alla reiti í öllum flæðum og krefst þess að aðeins sé hægt að stilla GS1 hefðbundna uppsetningu. Ef strikamerki inniheldur mörg atriði verður samt að skanna það margsinnis, því aðeins eitt stykki af strikamerkinu í einu verður slegið inn í flæðið fyrir fartækið. Þessi hegðun er stjórnað með GS1 almennri uppsetningu, eins og lýst er í hlutanum [Hefja almenna GS1-uppsetningu](#generic-gs1-setup).
- **Skönnun margra reita** – Þessi aðferð fyllir út í marga reiti þegar eitt strikamerki er skannað, með því að ýta viðbótargögnum inn í flæðisástand fartækisins. Til dæmis er reglan stillt til að ýta kenni forrits 01 í `ItemId` stjórnunar- og forritakenni 10 í `InventBatchId` reitinn. Í þessu tilviki, ef þú skannar strikamerkið `<FNC1>`**`01`**`09521101530001`**`17`**`210119`**`10`**`AB-123`, verður gögnum fyrir báðar breyturnar send á sama tíma. Kerfið mun því ekki biðja þig um vöru- og/eða rununúmerið í flæðinu. Þessari hegðun er stjórnað af GS1-reglum sem eru tengdar valmyndaratriðum, eins og lýst er í hlutanum [Setja upp GS1-reglum á valmyndaratriði fartækis](#policies-for-menus).

> [!WARNING]
> Sjálfgefnar GS1 reglur hafa verið prófaðar til að virka án óvæntrar hegðunar. Hins vegar getur sérsniðnar GS1 reglur sem er tengd valmyndaratriðum valdið ófyrirsjáanlegri hegðun, vegna þess að flæðið gæti ekki búist við því að einhver gögn séu tiltæk á tilteknum tíma.

## <a name="turn-on-the-gs1-feature"></a>Kveikja á GS1-eiginleikanum

Áður en hægt er að nota þennan eiginleika þarf að kveikja á honum í kerfinu. Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikja á honum. Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:

- **Eining:** *Vöruhúsakerfi*
- **Heiti eiginleika:** *Skanna GS1-strikamerki*

### <a name="turn-on-the-enhanced-parser-for-gs1-barcodes-feature"></a>Kveikja á bættum þáttari fyrir GS1-strikamerki

Ef þú notar GS1-strikamerki mælum við með því að þú kveikir einnig á eiginleikanum *Bættur þáttari fyrir GS1-strikamerki*. Þessi eiginleiki býður upp á betri útfærslu á GS1-strikamerkjaþáttaranum. Við það bætast eftirfarandi úrbætur:

- Það fylgir algrím almennrar GS1-forskriftar fyrir þáttun tákngagna og staðfestir að gögnin í tákninu séu gild samkvæmt skilgreiningunni.
- Það krefst þess ekki að þú setjir upp gildið **Hámarkslengd kennis** og notar lengstu pörun forskeyta úr stilltum kennum forrita.
- Auðveldara er að stilla tugabrot kenna forrita með því að nota bókstafinn *n* til að passa við hvaða tölu sem er. Til dæmis er hægt að stilla bara eitt kenni fyrir forrit (*310n*) í stað sérstakra kenna fyrir forrit (*3101*, *3102*, *3103* og svo framvegis).
- Það lagar vandamál þar sem rangt kóðuð gögn eru túlkuð sem reitargögn.
- Það kemur sem sérstakur flokkur sem hægt er að endurnota í öðru samhengi og gerir kleift að nota stækkunarhæfnispunkt til að meðhöndla skönnuð gögn áður en flæðisviðin eru fyllt út.

## <a name="set-up-global-gs1-options"></a><a name="set-gs1-options"></a>Setja upp altæka valkosti GS1

Síðan **Færibreytur Warehouse Management** býður upp á nokkrar stillingar sem setja á altæka valkosti GS1.

Til að setja upp altæka valkosti GS1 skal fylgja þessum skrefum.

1. Farðu í **vöruhúsakerfi \> Uppsetning \> Færibreytur vöruhúsakerfis**.
1. Á flýtiflipanum **Strikamerki** stillirðu eftirfarandi reiti.

    - **FNC1-stafur**, **Datamatrix-stafur**, og **QR-kóðastafur** – Tilgreinið stafi sem ber að túlka sem forskeyti fyrir hverja tegund GS1-strikamerkis.
    - **Skiltákn fyrir hópa** Tilgreina stafinn sem kemur í stað ASCII hópskiltáknsins.
    - **Hámarkslengd auðkennis** – Tilgreinið hámarksfjölda stafa sem leyfilegt er að nota fyrir auðkenni forritsins. Ekki er þörf á þessum reit ef kveikt er á eiginleikanum *Bættur þáttari fyrir GS1* fyrir kerfið þitt.

> [!NOTE]
> Forskeyti segja kerfinu að strikamerki sé dulkóðað samkvæmt GS1-staðlinum. Hægt er að nota allt þrjú forskeyti (**FNC1-staf**, **Staf gagnafylkis** og **QR-kóðastaf**) saman og af ýmsum ástæðum.

## <a name="gs1-application-identifiers"></a>Kennimerki GS1 forrits

GS1 snið kóða ekki aðeins gögnin heldur leyfa þér einnig að nota fyrirfram skilgreindan lista af auðkennum forrita til að skilgreina merkingu gagnanna. Skipulagsstjórar verða að setja upp nauðsynlegan lista yfir auðkenni forrita og tengja hvert þeirra við viðeigandi valmyndaratriði fyrir fartæki. Auðkennin er síðan hægt að nota á milli vöruhúsa sem alhliða stillingu fyrir flutning og pökkun. Þess vegna munu allir merkimiðar fara fram á sameinuðu eyðublaði.

Kerfið notar gögnin, einkum fyrirfram skilgreind auðkenni forrita, til að setja reglur sem eiga að gilda um viðeigandi skannaðar upplýsingar.

Hvert auðkenni forritsins gefur kerfinu merki um að síðari stafir í skannaða strikamerkinu skuli teljast blokk dulkóðaðra upplýsinga. Uppsetning auðkenna forritsins skilgreinir hvernig kerfið á að túlka strikamerki og vista það sem gildi í kerfinu.

Skipulagsstjórar geta notað stöðluð alþjóðleg forritaskilríki og/eða búið til sín eigin.

### <a name="load-the-standard-application-identifiers"></a>Sækja staðlað forritsauðkenni

Til að hefjast handa á skjótan hátt er hægt að hlaða inn lista yfir algeng alþjóðleg auðkenni forrits. Þú getur síðan víkkað eða breytt listanum síðar eins og þú krefst.

Til að hlaða inn stöðluðum kennimerkjum forrita skal fylgja þessum skrefum.

1. Farðu í **Warehouse Management \> Uppsetning \> GS1 \> GS1 auðkenni forrits**.
1. Á aðgerðasvæðinu skal velja **Stofna sjálfgefna uppsetningu**:

> [!WARNING]
> Skipunin **Stofna sjálfgefna uppsetningu** eyðir öllum núverandi skilgreindum auðkennum forrits og skiptir þeim út fyrir hefðbundna listann. Eftir að þú hleður inn sjálfgefinni uppsetningu getur þú hins vegar sérsniðið listann eins og þú vilt.

### <a name="set-up-custom-application-identifiers"></a>Setja upp sérsniðin auðkenni forrita

Ef sum eða öll auðkenni forrita sem fyrirtækið notar eru frábrugðin staðalsafninu er hægt að búa til eigin kóða frá grunni eða sérsníða staðalsafnið eftir þörfum.

Til að setja upp og sérsníða eigin GS1 forritsauðkenni skal fylgja eftirfarandi skrefum.

1. Farðu í **Warehouse Management \> Uppsetning \> GS1 \> GS1 auðkenni forrits**.
1. Fylgið einu af eftirfarandi skrefum:

    - Til að búa til nýtt auðkenni: Veldu **Nýtt** á aðgerðasvæðinu.
    - Til að breyta auðkenni sem þegar er til: Veldu auðkennið og veldu svo **Breyta** á aðgerðasvæðinu.

1. Stilltu eftirfarandi reiti fyrir nýja eða valda auðkennið:

    - **Kennimerki forrits** – Færðu inn auðkenniskóðann fyrir kennimerki forritsins. Venjulega er þessi kóði tveggja stafa heiltala en getur verið lengri. Fyrir tugabrot segir síðasti tölustafurinn til um fjölda aukastafa. Nánari upplýsingar er að finna í lýsingu gátreitsins **Aukastafur** síðar í þessum lista. Ef eiginleikinn *Bættur þáttari fyrir GS1-strikamerki* er virkur er hægt að búa til eitt kenni forrits fyrir öll afbrigði tugabrotin með því að nota bókstafinn *n* sem síðasta stafinn í kenni forritsins. Til dæmis er hægt að stilla bara eitt kenni fyrir forrit (*310n*) í stað sérstakra kenna fyrir forrit fyrir hvert tugabrot (*3101*, *3102*, *3103* og svo framvegis).
    - **Lýsing** – Færðu inn stutta lýsingu á kennimerkinu.
    - **Föst lengd** – Veldu þennan gátreit ef gildi sem eru skönnuð með því að nota þetta kennimerki forrits eru með fastan fjölda stafa. Hreinsa þennan gátreit ef lengd gilda er breytileg. Í því tilviki þarf að gefa upp lok gildisins með því að nota skiltákn flokksins sem var tilgreint á síðunni **Færibreytur Warehouse Management**.
    - **Lengd** – Færðu inn hámarksfjölda stafa sem geta birst í gildunum sem eru skönnuð með því að nota kennimerki forritsins. Ef gátreiturinn **Föst lengd** er valinn er gert ráð fyrir nákvæmlega þessum fjölda stafa.
    - **Gerð** – Veldu gerð gildis sem er skannað með því að nota þetta kennimerki forrits (*Tölustafir*, *Bókstafir og tölur* eða *Dagsetning*). Nánari upplýsingar um hvernig dagsetningar og tölur eru sýndar í gögnum um strikamerki er að finna í hlutanum [Dagsetningar og tugabrot](#dates-and-decimal-numbers).
    - **Aukastafur** – Veldu þennan gátreit ef gildið inniheldur mögulegt tugabrot. Ef þessi reitur er valinn mun kerfið nota síðasta tölustaf kennimerkis forritsins til að ákvarða fjölda aukastafa. Nánari upplýsingar um hvernig dagsetningar og tölur eru sýndar í gögnum um strikamerki er að finna í hlutanum [Dagsetningar og tugabrot](#dates-and-decimal-numbers).

> [!WARNING]
> Þrátt fyrir að kerfið geri þér kleift að stilla gátreitinn **Föst lengd** fyrir hvaða kenni forrits sem er, ætti aðeins að nota hann fyrir undirflokk kenna forrita sem hafa fyrirfram skilgreinda lengd samkvæmt Almennum forskriftum GS1. Endurbætt GS1 þáttari inniheldur nú þegar lista yfir öll auðkenni forrita sem hafa fyrirfram skilgreindar lengdir.

> [!NOTE]
> Gildið **Skiltákn fyrir hópa** sem er tilgreint á síðunni **Færibreytur vöruhúsakerfis** er valfrjálst ef gildi þar sem kennimerki forrits í fastri lengd fylgir í kjölfarið.

## <a name="establish-the-generic-gs1-setup"></a><a name="generic-gs1-setup"></a>Hefja almenna GS1-uppsetningu

Með almennri GS1-uppsetningu er komið upp safni algengra varpana. Þessar varpanir stemma hvern viðeigandi innsláttarreit í fartækjaforritinu við kennimerki forritsins sem stýrir því hvernig túlka og geyma eigi gildi úr skönnuðum strikamerkjum í þeim reit. Þessar stillingar eiga sjálfgefið við um allar skannanir fyrir öll valmyndaratriði fartækis. Hins vegar er hægt að skrifa yfir þær fyrir einn eða fleiri tiltekna reiti með GS1-reglu sem er úthlutað á tiltekið valmyndaratriði.

Almenn uppsetning GS1 gerir aðeins kleift að skanna eitt gildi í einu. Ef þú þarft því að hlaða mörgum reitargildum úr einni skönnun þarftu að setja upp GS1-reglu fyrir viðeigandi valmyndaratriði.

Frekari upplýsingar um GS1-reglur er að finna í næsta hluta.

### <a name="load-the-standard-generic-gs1-setup"></a>Hlaða hefðbundna almenna uppsetningu GS1

Síðan **Almenn uppsetning GS1** gerir þér kleift að hlaða stöðluðu safni varpana á milli reita fartækis og staðlaðra kennimerkja forrits sem sjálfgefna uppsetningin býr til.

Til að setja upp almenna uppsetningu GS1 skal fara í **Warehouse Management \> Uppsetning \> GS1 \> Almenn uppsetning GS1**. Veldu síðan **Búa til sjálfgefna uppsetningu** til að úthluta sjálfkrafa viðeigandi kennimerki forrits í hvern reit sem er yfirleitt notaður af valmyndaratriðum fartækis.

> [!WARNING]
> Ef einhver almenn uppsetning GS1 er þegar til staðar mun skipunin **Stofna sjálfgefna uppsetningu** eyða henni að fullu og hlaða hefðbundnu uppsetningunni.

### <a name="customize-the-standard-generic-gs1-setup"></a>Sérsníða hefðbundna almenna uppsetningu GS1

Til að sérsníða almenna uppsetningu GS1 skal fylgja þessum skrefum.

1. Farðu í **Warehouse Management \> Uppsetning \> GS1 \> Almenn uppsetning GS1**.
1. Fylgið einu af eftirfarandi skrefum:

    - Til að búa til nýja vörpun: Veldu **Ný** á aðgerðasvæðinu.
    - Til að breyta núverandi vörpun: Veldu vörpunina og veldu svo **Breyta** á aðgerðasvæðinu.

1. Stilltu eftirfarandi reiti fyrir nýju eða völdu vörpunina:

    - **Reitur** – Veldu eða færðu inn færslureit fartækjaforritsins sem gildi á innleið á að vera úthlutað í. Gildið er ekki birtingarnafnið sem starfsmenn sjá. Í staðinn er það heiti lykils sem er úthlutað í reitinn í undirliggjandi kóða. Sjálfgefin uppsetning býður upp á safn reita sem eru líklegir til að koma að gagni og inniheldur einföld heiti lykla fyrir hvern reit og samsvarandi forritaða virkni. Hins vegar gæti þurft að ræða við þróunaraðila til að finna rétt val fyrir innleiðinguna.
    - **Kennimerki forrits** – Veldu viðeigandi kennimerki forrits eins og það er skilgreint á síðunni **GS1 kennimerki forrits**. Kennimerkið ákvarðar hvernig strikamerkið verður túlkað og geymt sem gildi fyrir nefndan reit. Eftir að þú hefur valið kennimerki forrits sýnir reiturinn **Lýsing** lýsingu á því.

## <a name="set-up-gs1-policies-to-be-to-mobile-device-menu-items"></a><a name="policies-for-menus"></a>Setja upp GS1-reglum á valmyndaratriði fartækis

Tilgangur GS1 staðalsins er að gera starfsmönnum kleift að hlaða inn nokkrum gildum þegar þeir skanna eitt strikamerki í einu. Til að ná þessu markmiði verða skipulagsstjórar að setja upp GS1 stefnu sem segir kerfinu hvernig á að túlka strikamerki með mörgum gildum. Seinna er hægt að setja reglur á valmyndaratriði fyrir fartæki til að stjórna því hvernig strikamerki er túlkað þegar starfsmenn skanna það á meðan þeir nota tiltekið valmyndaratriði.

Ef engin GS1 stefna er gefin í valmyndaratriði getur kerfið aðeins tekið eitt gildi. Þetta gildi er notað á inntak fartækjaforritsins sem er valið þegar starfsmaðurinn gerir skönnun, eins og almenn uppsetning GS1 tilgreinir. Ef GS1-stefnu er úthlutað á valmyndaratriðið notar kerfið enn almenna uppsetningu GS1 til að varpa fyrsta gildi strikamerkisins á valda reitinn. Hins vegar getur hún sótt fleiri reitargildi eins og tilgreint er af viðeigandi stefnu.

### <a name="load-the-standard-specific-gs1-policies"></a>Sækja staðlaðar sértækar GS1 stefnur

Þú getur hlaðið inn GS1-stefnu til að hefjast handa á skjótan hátt. Þú getur síðan víkkað út eða breytt stefnjunum síðar eftir hentisemi.

Til að hlaða inn stöðluðum kennimerkjum forrita skal fylgja þessum skrefum.

1. Farðu í **Warehouse Management \> Uppsetning \> GS1 \> GS1-stefna**.
1. Á aðgerðasvæðinu skal velja **Stofna sjálfgefna uppsetningu**:

> [!WARNING]
> Skipunin **Stofna sjálfgefna uppsetningu** eyðir öllum núverandi skilgreindum stefnum og skiptir þeim út fyrir hefðbundið safn af stefnum. Eftir að sjálfgefna uppsetningin hefur verið hlaðin er hins vegar hægt að sérsníða stefnurnar eftir þörfum.

### <a name="set-up-custom-specific-gs1-policies"></a>Setja upp sérstakar GS1-stefnur

> [!WARNING]
> Sumar GS1-reglur virka hugsanlega ekki með hverju farsímaflæði sem er notað. Þegar þú stillir sérsniðnar GS1-reglur verður þú að prófa flæðið með því að nota mismunandi upplýsingar sem eru skannaðar á mismunandi stöðum í flæðinu. Á þennan hátt er hægt að ákvarða hvort flæðið hegðar sér eins og þú ætlast til.

Til að setja upp og sérsníða GS1-stefnurnar þínar skaltu fylgja þessum skrefum.

1. Farðu í **Warehouse Management \> Uppsetning \> GS1 \> GS1-stefna**.
1. Fylgið einu af eftirfarandi skrefum:

    - Til að búa til nýja stefnu: Veldu **Ný** á aðgerðasvæðinu.
    - Til að breyta fyrirliggjandi stefnu: Veldu hana í listaglugganum.

1. Í haus nýju eða völdu reglunnar skal stilla eftirfarandi gildi:

    - **Heiti reglu** – Færðu inn heiti fyrir regluna.
    - **Lýsing** – Færðu inn stutta lýsingu á reglunni.

1. Í flýtiflipanum fyrir neðan hausinn skal varpa reitarheitum í kennimerki forrits eins og þörf er á fyrir núverandi reglu. Notaðu hnappana á tækjastikunni til að bæta við eða fjarlægja línur eftir þörfum. Fyrir hverja línu skal stilla eftirfarandi reiti:

    - **Reitur** – Veldu eða færðu inn færslureit fartækjaforritsins sem gildi á innleið á að vera úthlutað í. Gildið er ekki birtingarnafnið sem starfsmenn sjá. Í staðinn er það heiti lykils sem er úthlutað í reitinn í undirliggjandi kóða. Sjálfgefin uppsetning býður upp á safn reita sem eru líklegir til að koma að gagni og inniheldur einföld heiti lykla fyrir hvern reit og samsvarandi forritaða virkni. Hins vegar gæti þurft að ræða við þróunaraðila til að finna rétt val fyrir innleiðinguna.
    - **Kennimerki forrits** – Veldu viðeigandi kennimerki forrits eins og það er skilgreint á síðunni **GS1 kennimerki forrits**. Kennimerkið ákvarðar hvernig strikamerkið verður túlkað og geymt sem gildi fyrir nefndan reit. Eftir að þú hefur valið kennimerki forrits sýnir reiturinn **Lýsing** lýsingu á því.
    - **Röðun** – Hvert strikamerki með mörgum gildum inniheldur röð af kennimerkjum forrits þar sem gildi fyrir hverju og einu þeirra. Viðeigandi GS1-regla ber kennsl á hvaða kennimerki forrits er varpað í sérhvern reit gagnagrunns. Ef strikamerki notar hinsvegar sama kennimerki forrits oftar en einu sinni notar kerfið röðina sem kennimerki forritsins birtast í kóðanum til að varpa þeim í reiti. Fyrir raðir sem deila auðkenni forrits með einni eða fleiri röðum skal nota þennan reit til að setja upp röðina sem samsvarandi raðir eru unnar í. Fyrst verður unnið úr þeirri röð sem hefur lægsta flokkunargildið.

> [!NOTE]
> Fyrir strikamerki sem innihalda fleiri en eitt eins kennimerki forrits *verður að* nota reitinn **Röðun** til að ákvarða röð reitanna.

## <a name="assign-gs1-policies-to-mobile-device-menu-items"></a>Úthluta GS1-reglum á valmyndaratriði fartækis

Sjálfgefið er að allir valmyndarhlutir fartækisins séu með innsláttarreiti þar sem starfsmenn geta skannað eitt gildi, í samræmi við almenna GS1 uppsetninguna. Ef þú vilt að starfsmenn geti skannað fleiri en eitt reitargildi í einni skönnun fyrir hvaða valmyndaratriði sem er fyrir fartæki verður þú að úthluta GS1-reglu með því að fylgja þessum skrefum.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmyndaratriði fartækis**.
1. Stofnaðu eða opnaðu valmyndaratriði.
1. Í flýtiflipanum **Almennt** skal stilla reitinn **GS1-regla** á þá relgu sem á við um valmyndaratriðið.

## <a name="gs1-setup-example"></a>Dæmi um uppsetningu GS1

Þetta dæmi á við um kerfi þar sem GS1-valkostir eru settir upp á eftirfarandi hátt:

- Á síðunni **Færibreytur Warehouse Management** eru eftirfarandi altækar stillingar settar á:

    - **FNC1-stafur** *\]C1*
    - **Skiltákn fyrir hópa:** *\~*

- Á síðunni **GS1 kennimerki forrits** eiga eftirfarandi kennimerki forrits við í þessu dæmi.

    | Kennimerki forrits | lýsing | Föst lengd | Lengd | Gerð | Tugabrot |
    |---|---|---|---|---|---|
    | 01 | GTIN | Valið | 14 | Tölugildi | Útleyst |
    | 10 | Rununúmer | Útleyst | 20 | Bókstafir og tölur | Útleyst |
    | 17 | Gildistími | Valið | 6 | Dagsetning | Útleyst |
    | 30 | Magn sem tekið er á móti | Útleyst | 8 | Tölugildi | Útleyst |

- Á síðunni **Almenn uppsetning GS1** eiga eftirfarandi stillingar fyrir almenna GS1-reglu við í þessu dæmi.

    | Svæði | Kennimerki forrits | lýsing |
    |---|---|---|
    | ItemId | 01 | GTIN |

- Á síðunni **GS1-regla** er regla þar sem reiturinn **Heiti reglu** er stilltur á *Móttaka innkaupa*. Þessi regla inniheldur eftirfarandi línur.

    | Svæði | Kennimerki forrits | lýsing | Röðun |
    |---|---|---|---|
    | ExpDate | 17 | Gildistími | 0 |
    | InventBatchId | 10 | Rununúmer | 0 |
    | Magn | 30 | Magn sem tekið er á móti | 0 |

- Á síðunni **Valmyndaratriði fartækis** er til valmyndaratriði sem heitir *Móttaka innkaupa*. Reiturinn **GS1-regla** er stilltur á *Móttaka innkaupa*.

Eftir að vörur í innkaupapöntun eru komnar í vöruhúsið fylgir starfskrafturinn þessum skrefum.

1. Á fartækinu skal velja valmyndaratriðið **Móttaka innkaupa**.
1. Sláðu inn innkaupapöntunarnúmerið.
1. Veldu reitinn **Vara** og skannaðu eftirfarandi strikamerki: `]C10100000012345678~3030~10b1~17220215`.

Kerfið þáttar skannaða strikamerkið með eftirfarandi hætti vegna stillinga sem eru settar upp í þessu dæmi.

| Reitarlykill | Kenni umsóknar | Virði | Nóta |
|---|---|---|---|
| ItemId | 01 | 00000012345678 | Vegna þess að starfsmaðurinn skannaði í reitnum **Vara** er fyrsta gildið í strikamerkinu varpað í þann reit. Vörpunin er tekin úr almennri uppsetningu GS1. |
| Magn | 30 | 30 | Vegna þess að verið er að sækja nokkur reitargildi í einni skönnun er þessi vörpun og allar næstu varpanir sóttar úr GS1-reglunni sem er úthlutað á valmyndaratriðið **Móttaka innkaupa**. Þetta gildi er magnið sem var móttekið. |
| InventBatchId | 10 | b1 | Þetta gildi er runukennið. |
| ExpDate | 17 | 220215 | Dagsetningarsniðið er ÁÁMMDD. Því er lokadagurinn 15. febrúar 2022. |

Kvittunin er síðan skráð og viðeigandi gildi gagnagrunnsins eru færð inn á eftir stöku skönnuninni.
