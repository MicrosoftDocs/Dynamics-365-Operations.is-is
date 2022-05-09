---
title: GS1 strikamerki
description: Í þessu efnisatriði er lýst hvernig setja á upp GS1 strikamerki og QR-kóða svo hægt sé að skanna merkingar í vöruhúsi.
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
ms.openlocfilehash: ea928bc8a020035adb36ae2e7873c656e8c3985d
ms.sourcegitcommit: 1050e58e621d9a0454895ed07c286936f8c03320
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 04/21/2022
ms.locfileid: "8625279"
---
# <a name="gs1-bar-codes"></a>GS1 strikamerki

[!include [banner](../includes/banner.md)]

Vöruhússtarfsmenn þurfa oft að ljúka nokkrum verkefnum þegar þeir nota skanna fyrir farsíma til að skrá hreyfingar vöru, spjalds eða geymis. Þessi verkefni geta falið í sér bæði að skanna strikamerkingar og færa inn upplýsingar handvirkt í fartækið. Strikamerkin nota tiltekið snið fyrirtækis sem þú skilgreinir og stjórnar með Microsoft Dynamics 365 Supply Chain Management.

GS1 strikamerki fyrir sendingarmerki voru þróuð til að veita alþjóðlegan staðal fyrir gagnaskipti milli fyrirtækja. Þau eru fáanleg í bæði línulegum (1D) táknmyndum (strikamerkjasniðum), eins og GS1-128, og 2D táknmyndum, eins og GS1 DataMatrix og GS1 QR kóða. GS1 strikamerki kóða ekki aðeins gögn heldur leyfa þér einnig að nota fyrirfram skilgreindan lista yfir *auðkenni forrita* að skilgreina merkingu þessara gagna. GS1 staðallinn skilgreinir gagnasniðið og ýmis konar gögn sem hægt er að nota til að kóða. Ólíkt eldri strikamerkjastöðlum geta GS1 strikamerki haft marga gagnaþætti. Þess vegna getur ein skönnun á strikamerkjum náð yfir nokkrar tegundir vöruupplýsinga, eins og lotuna og fyrningardagsetninguna.

GS1 stuðningur í Supply Chain Management einfaldar skönnunarferlið verulega í vöruhúsum þar sem bretti og ílát eru merkt með því að nota strikamerki á GS1 sniði. Vöruhússtarfsmenn geta dregið út allar nauðsynlegar upplýsingar með einni skönnun á GS1 strikamerki. Með því að útiloka nauðsyn þess að gera margar skannanir og/eða slá inn upplýsingar handvirkt, hjálpa GS1 strikamerkin til við að minnka tímann sem tengist verkefnum. Um leið hjálpa þau einnig til við að bæta nákvæmni.

Skipulagsstjórar verða að setja upp nauðsynlegan lista yfir auðkenni forrita og tengja hvert þeirra við viðeigandi valmyndaratriði fyrir fartæki. Þá er hægt að nota auðkenni forritsins yfir vöruhús sem alhliða stillingu fyrir flutning og pökkun. Þess vegna munu allir merkimiðar fara fram á sameinuðu eyðublaði.

Nema annað sé tekið fram notar þetta efni hugtakið *strikamerki* að vísa til bæði línulegra (1D) strikamerkja og 2D strikamerkja.

## <a name="the-gs1-bar-code-format"></a>GS1 strikamerkjasniðið

Almennar forskriftir GS1 tilgreina hvaða táknmyndir má nota fyrir GS1 strikamerki og hvernig á að umrita gögnin í strikamerkinu. Þessi hluti veitir stutta kynningu á efninu. Fyrir allar upplýsingar, sjá [GS1 Almennar upplýsingar](https://www.gs1.org/docs/barcodes/GS1_General_Specifications.pdf) sem eru gefin út af GS1. GS1 forskriftarskjalið er uppfært reglulega og upplýsingarnar sem það veitir eru uppfærðar með GS1 General Specifications útgáfu 22.0.

GS1 strikamerki nota eftirfarandi táknmyndir:

- **Línuleg eða 1D strikamerki** – GS1-128 og GS1 DataBar
- **2D strikamerki** - GS1 DataMatrix, GS1 QR kóða og GS1 punktakóði

Athugaðu að það er sérstaklega minnst á GS1 í GS1-128, sem er sértilvik um venjulegan Code-128 línulega strikamerkið, GS1 DataMatrix og GS1 QR kóða. Munurinn á GS1 útgáfunni og útgáfunni sem er ekki GS1 er tilvist sérstafs (FNC1) sem fyrsta stafurinn í strikamerkjagögnunum. Tilvist FNC1 stafs gefur til kynna að túlka ætti gögnin í strikamerkinu í samræmi við GS1 forskriftina.

Gögnin í strikamerkinu sjálfu samanstanda af mörgum gagnaþáttum sem hver um sig er auðkenndur með auðkenni forrits í upphafi reitsins. Venjulega eru gögnin einnig sett fram undir strikamerkinu á læsilegu sniði, þar sem auðkenni forritsins er sýnt innan sviga. Eftirfarandi er dæmi: `(01) 09521101530001 (17) 210119 (10) AB-123`. Þetta strikamerki inniheldur þrjá þætti:

- **Auðkenni umsóknar 01** – GS1 alþjóðlegt vörunúmer (GTIN) vörunnar.
- **Auðkenni umsóknar 17** - Gildistími.
- **Auðkenni umsóknar 10** – Lotunúmerið.

Fyrir hvern þátt gætu gögnin annað hvort haft fyrirfram skilgreinda lengd eða breytilega lengd. Það er fastur listi yfir forritaauðkenni sem hafa fyrirfram skilgreinda lengd. Öll önnur auðkenni forrita eru með breytilegri lengd og GS1 forritaauðkennislisti tilgreinir hámarkslengd og snið gagna. Til dæmis hefur forritaauðkenni 01 fyrirfram skilgreinda lengd upp á 16 stafi (tveir fyrir forritaauðkenni sjálft og síðan 14 fyrir GTIN), og forritsauðkenni 17 hefur fyrirfram skilgreinda lengd sem eru átta stafir (tveir fyrir forritsauðkenni sjálft og síðan sex fyrir dagsetningin). Hins vegar hefur forritaauðkenni 10 tvær tölur fyrir sjálft forritsauðkennið og síðan allt að 20 tölustafi.

Þegar þættir eru settir saman, ef þáttur fylgir staki með breytilegri lengd, verður að nota skiljustaf. Þessi aðskilnaður getur verið annað hvort sérstakur FNC1 stafurinn eða hópskiljustafur (óprentanlegur stafur sem hefur ASCII kóða 29 og sextándakóða 1D). Skiljuna ætti ekki að nota eftir síðasta þáttinn. Þó að skilja ætti ekki að nota eftir þætti sem hafa fyrirfram skilgreinda lengd, þá er tilvist hans ekki mikilvæg villa.

Í strikamerkisgögnum frá fyrra dæmi um strikamerki sem inniheldur forritaauðkenni 01, 17 og 10, verða gögnin í kóða-128, QR kóða eða DataMatrix tákni kóðuð sem`<FNC1>`**`01`**`09521101530001`**`17`**`210119`**`10`**`AB-123` (auðkenni forrita eru feitletruð). Sem besta starfsvenjan ætti að setja alla þætti sem hafa breytilega lengd í lokin, til að útrýma þörfinni fyrir viðbótareiginleika fyrir hópa. Hins vegar getur strikamerkið einnig verið með annarri röð þátta, þar sem skiljan er skylda. Hér er dæmi:`<FNC1>`**`01`**`09521101530001`**`10`**`AB-123<GS>`**`17`**`210119`.

### <a name="dates-and-decimal-numbers"></a>Dagsetningar og aukastafir

Dagsetningar eru alltaf fulltrúar í *ÁÁMMDD* sniði, þar sem öld ársins ræðst af GS1 forskriftum. Aðeins er hægt að tákna dagsetningar frá 49 árum í fortíðinni til 50 ára í framtíðinni (miðað við yfirstandandi ár).

Sumir gagnaeiningar innihalda aukastafi. Til dæmis tákna forritsauðkenni 3100, 3101, ... 3105 nettóþyngd í kílóum. Vegna þess að þessi forritsauðkenni hafa fyrirfram skilgreinda lengd 10, eru sex tölur tiltækar fyrir magnið. Staða tugamerkisins er tilgreind með síðustu tölunni á auðkenni forritsins. Þess vegna er einnig hægt að tákna þessa fjölskyldu forritaauðkenna sem *310n*. Vegna þess að GS1 staðallinn tilgreinir að það þurfi alltaf að vera að minnsta kosti ein tala vinstra megin við tugastafinn, þá eru að hámarki fimm aukastafir leyfðir.

Hér eru nokkur dæmi sem sýna hvernig talan *123456* verður túlkað af mismunandi forritaauðkennum (birt með feitletrun):

- **`3100`**`123456`&rarr; 123456 (heil tala)
- **`3101`**`123456`&rarr; 12345.6 (einn aukastafur)
- **`3102`**`123456`&rarr; 1234,56 (tveir aukastafir)
- **`3103`**`123456`&rarr; 123.456 (þrír aukastafir)
- **`3104`**`123456`&rarr; 12.3456 (fjórir aukastafir)
- **`3105`**`123456`&rarr; 1.23456 (fimm aukastafir)

## <a name="scanning-gs1-bar-codes-in-supply-chain-management"></a>Skanna GS1 strikamerki í Supply Chain Management

Til að skanna GS1 strikamerki nota vöruhúsamenn skanni sem er innbyggður í eða tengdur við farsíma. Skanninn sendir síðan skannaða strikamerkið til vöruhúsastjórnunar farsímaforritsins sem röð lyklaborðsatburða. Þessi aðgerðarmáti er einnig þekktur sem a *lyklaborðsfleygur* eða *fleyg*. Farsímaforritið sendir síðan móttekinn texta eins og hann er til birgðakeðjustjórnunar. Þegar kerfið tekur á móti inntaksgögnum ákvarðar það fyrst hvort gögnin byrji á einu af stilltu forskeytum sem gefa til kynna að gögnin séu í raun GS1 strikamerki (sjá [Settu upp alþjóðlega GS1 valkosti](#set-gs1-options) kafla). Ef skönnuðu gögnin byrja á einu af þessum forskeytum notar kerfið GS1 flokka til að flokka gögnin og draga út einstaka gagnaeiningar í samræmi við auðkenni þeirra. Eftir að gögnin hafa verið þáttuð verða annað hvort núverandi innsláttarreitur eða margir reitir fylltir út með skönnuðu gögnunum.

### <a name="configuration-of-bar-code-scanner-hardware-and-software"></a>Stilling vélbúnaðar og hugbúnaðar fyrir strikamerkjaskanna

Til að birgðakeðjustjórnun geti borið kennsl á og afkóða GS1 strikamerki á réttan hátt, verður að stilla vélbúnaðarskanni eða stuðningshugbúnað til að framkvæma eftirfarandi aðgerðir:

- Bættu forskeyti við skannað strikamerki, svo að kerfið geti þekkt GS1 strikamerki.
- Umbreyttu óprentanlega ASCII hópskiljustafinn (ASCII kóði 29 eða sextándakóði 1D) í prenthæfan staf, eins og tilde (~).

Þó að þú getir bætt hvaða forskeyti sem er við skannaða strikamerkið er einn valkostur að bæta við ISO/IEC 15424 táknfræðiauðkenni, einnig þekkt sem *AIM auðkenni*. Þetta þriggja stafa auðkenni byrjar á`]`, hefur síðan einn staf sem auðkennir táknfræðina sem er notuð og hefur síðan tölu sem er notuð sem frekari breyting. Til dæmis, AIM auðkennið`]C1` tilgreinir Code 128 strikamerki (vegna stafsins`C`), og breytirinn`1` tilgreinir að það sé FNC1 stafur í fyrstu stöðu gagnanna. Á hinn bóginn,`]C0` er Code 128 strikamerki sem hefur hvaða annan staf sem fyrsta staf gagnanna.

Eftirfarandi fimm táknfræðiauðkenni samsvara GS1 strikamerkjum sem hafa forritsauðkenni:

- `]C1`– Kóði 128 (`C`) með FNC1 staf í fyrstu stöðu (`1`), einnig þekkt sem GS1-128.
- `]e0`– GS1 DataBar.
- `]d2`– DataMatrix (`d`) með ECC 200 og FNC1 í fyrstu stöðu (`2`), einnig þekkt sem GS1 DataMatrix.
- `]Q3`- QR kóða (`Q`) Model 2 tákn með FNC1 í fyrstu stöðu (`3`), einnig þekktur sem GS1 QR kóða.
- `]J1`– GS1 punktakóði.

Ef þú notar þessi auðkenni krefst samhæfni við strikamerki sem ekki eru GS1 að skannanir eða skannahugbúnaðurinn sé stilltur til að fjarlægja auðkenni sem samsvara ekki GS1 auðkennum. Til dæmis, ef þú skannar "venjulegt" Code 39 strikamerki, forskeytið`]A0` verður bætt við. Þar sem kerfið mun ekki skilja þetta forskeyti sem eitt af GS1 forskeytum, mun það túlka það sem gögn og gefa óvæntar niðurstöður.

> [!NOTE]
> Til hægðarauka mun útgáfa 2.0.17.0 og síðar af Warehouse Management farsímaforritinu fjarlægja öll AIM forskeyti sem eru ekki með á fyrri listanum. Þessi hegðun styður tilvik þar sem þú getur stillt skannann til að bæta við AIM forskeytinu en ekki fjarlægja óæskileg forskeyti.

### <a name="single-and-multiple-field-scanning"></a>Skönnun á einum og mörgum sviðum

Eftir að gögnin hafa verið flokkuð úr strikamerkinu verða þau færð inn í flæðistýringar farsímatækisins. Það eru tvær aðferðir sem verða unnar í röð:

- **Skönnun á einum vettvangi** – Þessi aðferð fyllir aðeins út reitinn sem strikamerkið var skannað inn í. Til dæmis ef þú skannar strikamerkið`<FNC1>`**`01`**`09521101530001`**`17`**`210119`**`10`**`AB-123` meðan bendillinn er í **Atriði** reit, GTIN`09521101530001` frá strikamerkinu verður slegið inn í þann reit. Ef þú skannar sama strikamerki á meðan bendillinn er í **Lotu auðkenni** reit, lotunúmerið`AB-123` frá strikamerkinu verður slegið inn. Þessi háttur virkar fyrir alla reiti í öllum flæði og krefst þess aðeins að GS1 almenna uppsetningin sé stillt. Ef strikamerki inniheldur marga þætti verður samt að skanna það mörgum sinnum, því aðeins eitt stykki strikamerkis í einu verður slegið inn í farsímaflæðið. Þessari hegðun er stjórnað af GS1 almennu uppsetningunni, eins og lýst er í [Komdu á almennri GS1 uppsetningu](#generic-gs1-setup) kafla.
- **Skönnun á mörgum sviðum** – Þessi aðferð fyllir út marga reiti þegar einn strikamerki er skannaður, með því að ýta viðbótargögnum í flæðisstöðu farsíma. Til dæmis er stefnan stillt til að ýta forritaauðkenni 01 inn í`ItemId` stjórna og forritaauðkenni 10 í`InventBatchId` sviði. Í þessu tilviki, ef þú skannar strikamerkið`<FNC1>`**`01`**`09521101530001`**`17`**`210119`**`10`**`AB-123`, gögnum fyrir báðar breyturnar verður ýtt á sama tíma. Þess vegna mun kerfið ekki biðja þig um vöruna og/eða lotunúmerið í flæðinu. Þessari hegðun er stjórnað af GS1 reglum sem eru tengdar við valmyndaratriði, eins og lýst er í [Settu upp GS1 reglur þannig að þær séu fyrir valmyndaratriði farsíma](#policies-for-menus) kafla.

> [!WARNING]
> Sjálfgefnar GS1 reglur hafa verið prófaðar til að virka án óvæntrar hegðunar. Hins vegar getur aðlögun GS1 reglna sem eru tengd við valmyndaratriði valdið óvæntri hegðun, vegna þess að flæðið gæti ekki búist við að einhver gögn séu tiltæk á tilteknum tíma.

## <a name="turn-on-the-gs1-feature"></a>Kveikja á GS1-eiginleikanum

Kveikja þarf á þessum eiginleika í kerfinu til að hægt sé að nota hann. Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikja á honum. Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:

- **Eining:** *Vöruhúsakerfi*
- **Eiginleikaheiti:** *Skannaðu GS1 strikamerki*

### <a name="turn-on-the-enhanced-parser-for-gs1-barcodes-feature"></a>Kveiktu á Enhanced parser fyrir GS1 strikamerki eiginleikann

Ef þú notar GS1 strikamerki mælum við með að þú virkir líka *Aukinn flokkari fyrir GS1 strikamerki* eiginleiki. Þessi eiginleiki veitir bætta útfærslu á GS1 strikamerkjagreiningunni. Það bætir við eftirfarandi endurbótum:

- Það fylgir GS1 General Specification reikniritinu fyrir þáttun tákngagna og staðfestir að gögnin í tákninu séu gild samkvæmt forskriftinni.
- Það þarf ekki að setja upp a **Hámarkslengd auðkennis** gildi og notar lengstu forskeytissamsvörun frá stilltum forritaauðkennum.
- Það gerir þér auðveldara að stilla aukastafaauðkenni með því að nota bókstafinn *n* til að passa við hvaða tölu sem er. Til dæmis geturðu stillt aðeins eitt forritaauðkenni (*310n*) í stað aðskilinna forritaauðkenna (*3101*, *·*, *·*, og svo framvegis).
- Það lagar vandamál þar sem rangt kóðuð gögn eru túlkuð sem svæðisgögn.
- Það kemur sem sérstakur flokkur sem hægt er að endurnýta í öðru samhengi og gerir kleift að nota stækkanleikapunkt til að vinna með skönnuð gögn áður en flæðisreitirnir eru fylltir út.

## <a name="set-up-global-gs1-options"></a><a name="set-gs1-options"></a>Setja upp altæka valkosti GS1

Síðan **Færibreytur Warehouse Management** býður upp á nokkrar stillingar sem setja á altæka valkosti GS1.

Til að setja upp altæka valkosti GS1 skal fylgja þessum skrefum.

1. Farðu í **vöruhúsakerfi \> Uppsetning \> Færibreytur vöruhúsakerfis**.
1. Á flýtiflipanum **Strikamerki** stillirðu eftirfarandi reiti.

    - **FNC1 stafur**, **stafur**, og **QR kóða stafur** – Tilgreindu stafi sem ætti að túlka sem forskeyti fyrir hverja tegund af GS1 strikamerki.
    - **Hópaskil** – Tilgreindu stafinn sem kemur í stað ASCII hópskiljustafs.
    - **Hámarkslengd auðkennis** – Tilgreinið hámarksfjölda stafa sem leyfilegt er að nota fyrir auðkenni forritsins. Þessi reitur er ekki nauðsynlegur ef *Aukinn GS1 flokkari* kveikt er á eiginleikanum í kerfinu þínu.

> [!NOTE]
> Forskeyti segja kerfinu að strikamerki sé kóðað samkvæmt GS1 staðlinum. Hægt er að nota allt þrjú forskeyti (**FNC1-staf**, **Staf gagnafylkis** og **QR-kóðastaf**) saman og af ýmsum ástæðum.

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

    - **Kennimerki forrits** – Færðu inn auðkenniskóðann fyrir kennimerki forritsins. Venjulega er þessi kóði tveggja stafa heiltala en getur verið lengri. Fyrir tugabrot segir síðasti tölustafurinn til um fjölda aukastafa. Nánari upplýsingar er að finna í lýsingu gátreitsins **Aukastafur** síðar í þessum lista. Ef *Aukinn flokkari fyrir GS1 strikamerki* eiginleiki er virkur geturðu búið til eitt forritaauðkenni fyrir öll aukastafaafbrigði með því að nota bókstafinn *n* sem síðasta stafurinn í auðkenni forritsins. Til dæmis geturðu stillt aðeins eitt forritaauðkenni (*310n*) í stað sérstaks forritaauðkennis fyrir hvern fjölda aukastafa (*3101*, *·*, *·*, og svo framvegis).
    - **Lýsing** – Færðu inn stutta lýsingu á kennimerkinu.
    - **Föst lengd** – Veldu þennan gátreit ef gildi sem eru skönnuð með því að nota þetta kennimerki forrits eru með fastan fjölda stafa. Hreinsa þennan gátreit ef lengd gilda er breytileg. Í því tilviki þarf að gefa upp lok gildisins með því að nota skiltákn flokksins sem var tilgreint á síðunni **Færibreytur Warehouse Management**.
    - **Lengd** – Færðu inn hámarksfjölda stafa sem geta birst í gildunum sem eru skönnuð með því að nota kennimerki forritsins. Ef gátreiturinn **Föst lengd** er valinn er gert ráð fyrir nákvæmlega þessum fjölda stafa.
    - **Gerð** – Veldu gerð gildis sem er skannað með því að nota þetta kennimerki forrits (*Tölustafir*, *Bókstafir og tölur* eða *Dagsetning*). Fyrir frekari upplýsingar um hvernig dagsetningar og tölur eru sýndar í strikamerkjagögnum, sjá [Dagsetningar og aukastafir](#dates-and-decimal-numbers) kafla.
    - **Aukastafur** – Veldu þennan gátreit ef gildið inniheldur mögulegt tugabrot. Ef þessi reitur er valinn mun kerfið nota síðasta tölustaf kennimerkis forritsins til að ákvarða fjölda aukastafa. Fyrir frekari upplýsingar um hvernig dagsetningar og tölur eru sýndar í strikamerkjagögnum, sjá [Dagsetningar og aukastafir](#dates-and-decimal-numbers) kafla.

> [!WARNING]
> Þó að kerfið leyfi þér að stilla **Föst lengd** gátreitinn fyrir hvaða forritsauðkenni sem er, ætti hann aðeins að nota fyrir undirmengi forritaauðkenna sem hafa fyrirfram skilgreinda lengd samkvæmt GS1 almennum forskriftum. Aukinn GS1 flokkari inniheldur nú þegar lista yfir öll forritsauðkenni sem hafa fyrirfram skilgreinda lengd.

> [!NOTE]
> The **Hópaskil** gildi sem tilgreint er á **Vöruhússtjórnunarfæribreytur** síða er valfrjáls ef gildi sem er fylgt eftir með forritaauðkenni hefur fasta lengd.

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

## <a name="set-up-gs1-policies-to-be-to-mobile-device-menu-items"></a><a name="policies-for-menus"></a> Settu upp GS1 reglur þannig að þær séu fyrir valmyndaratriði farsíma

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
> Sumar GS1 reglur virka kannski ekki með hverju farsímaflæði sem þú notar. Þegar þú stillir sérsniðnar GS1 stefnur, verður þú að prófa flæði farsímans með því að nota mismunandi upplýsingar sem eru skannaðar á mismunandi stöðum í flæðinu. Þannig geturðu ákvarðað hvort flæðið hegðar sér eins og þú býst við.

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
1. Veldu **Atriði** reit og skannaðu eftirfarandi strikamerki:`]C10100000012345678~3030~10b1~17220215`.

Kerfið þáttar skannaða strikamerkið með eftirfarandi hætti vegna stillinga sem eru settar upp í þessu dæmi.

| Reitarlykill | Kenni umsóknar | Virði | Nóta |
|---|---|---|---|
| ItemId | 01 | 00000012345678 | Vegna þess að starfsmaðurinn skannaði í reitnum **Vara** er fyrsta gildið í strikamerkinu varpað í þann reit. Vörpunin er tekin úr almennri uppsetningu GS1. |
| Magn | 30 | 30 | Vegna þess að verið er að sækja nokkur reitargildi í einni skönnun er þessi vörpun og allar næstu varpanir sóttar úr GS1-reglunni sem er úthlutað á valmyndaratriðið **Móttaka innkaupa**. Þetta gildi er magnið sem var móttekið. |
| InventBatchId | 10 | b1 | Þetta gildi er runukennið. |
| ExpDate | 17 | 220215 | Dagsetningarsniðið er ÁÁMMDD. Því er lokadagurinn 15. febrúar 2022. |

Kvittunin er síðan skráð og viðeigandi gildi gagnagrunnsins eru færð inn á eftir stöku skönnuninni.
