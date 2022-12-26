---
title: Algengar spurningar um verkþætti árslokunar
description: Í þessari grein er að finna spurningar sem geta komið upp við lokun árs, sem og svör sem kunna að koma að gagni við verkþætti lokunar í árslok.
author: moaamer
ms.date: 12/01/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 2e33c1dcbfa4da74f2e8acc6e29f04fda3abd185
ms.sourcegitcommit: 9f3a60a583da21382a14f32ce146fc9ce03f2a09
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/15/2022
ms.locfileid: "9853041"
---
# <a name="year-end-activities-faq"></a>Algengar spurningar um verkþætti árslokunar 

[!include [banner](../includes/banner.md)]

Í þessari grein er að finna spurningar sem geta komið upp við lokun árs, sem og svör sem kunna að koma að gagni við verkþætti lokunar í árslok. Upplýsingarnar í þessari grein eru fyrst og fremst tengdar spurningum sem varða verkþætti lokunar í árslok fyrir fjárhag og viðskiptaskuldir.

## <a name="general-ledger-year-end-enhancements"></a>Viðbætur fjárhags í árslok

Microsoft Dynamics 365 Finance útgáfu 10.0.20 fylgdu endurbætur fyrir lokun í árslok. Þessar endurbætur eru virkjaðar sjálfgefið frá og með útgáfu 10.0.25 og eru áskildar frá og með útgáfu 10.0.29. Ef fyrirtækið notar eldri útgáfu en 10.0.25 er mælt með að þessi eiginleiki sé virkjaður áður en ferlið fyrir lokun í árslok hefst. Kveikja þarf á þessum eiginleika í kerfinu til að hægt sé að nota hann. Stjórnendur geta notað vinnusvæði **Eiginleikastjórnun** til að athuga stöðu eiginleikans og kveikt á honum ef þörf krefur. Þar er eiginleikinn skráður á eftirfarandi hátt:

- **Eining:** fjárhagur
- **Heiti eiginleika:** Endurbætur fyrir fjárhag í árslok

Uppsetning sniðmáta fyrir lokun í árslok hefur verið færð á nýja uppsetningarsíðu, **Uppsetning sniðmáts árslokalokunar**. Núverandi síða lokunar í árslok verður eins og síðan **Endurmat á erlendum gjaldmiðli fjárhags**, þar sem listi birtist í hvert skipti sem lokun í árslok er keyrð eða bakfærð. Síðan mun ekki sýna sögulegar upplýsingar um lokanir í árslok sem voru gerðar áður en eiginleikinn er gerður virkur. Aðalbókari getur hafið lokun í árslok á nýju síðunni.

Til að bakfæra lokun í árslok skal velja nýjasta fjárhagsárið fyrir viðeigandi lögaðila og velja síðan **Bakfæra lokun í árslok**. Bakfærslan mun eyða bókhaldsfærslum fyrir síðustu lokun í árslok og mun ekki aftur keyra lokun í árslok sjálfkrafa. Ef eiginleikinn **Endurbætur fyrir fjárhag í árslok** er virkjaður eftir lokun í árslok og óskað er eftir að bakfæra sögulegar árslokaniðurstöður skal keyra sögulegar árslokaniðurstöður á ný eftir að fjárhagsfæribreytan **Eyða fyrirliggjandi árslokafærslum þegar ári er lokað aftur** hefur verið virkjuð.

Hægt er að keyra lokun í árslok aftur með því að hefja endurræsa ferlið fyrir fjárhagsárið og lögaðilann. Ferlið heldur áfram að nota færibreytustillingu fjárhags til að skera úr um hvort endurkeyrsla lokunar í árslok muni einungis taka til greina nýjar eða breyttar færslur, eða hvort ferlið verði endurkeyrt fyrir allar færslur og fyrri lokun bakfærð að fullu.

## <a name="general-ledger-the-general-ledger-year-end-enhancements-feature-is-enabled-why-cant-i-view-my-previous-year-closings-in-the-history-section-of-the-year-end-close-page"></a>Fjárhagur: Eiginleikinn fyrir endurbætur á fjárhag í árslok er virkur. Hvers vegna get ég ekki skoðað fyrri árslokanir í söguhluta síðunnar „Lokun í árslok“?

Áður en hægt er að virkja eiginleikann **Endurbætur fyrir fjárhag í árslok** er athugað með dagsetningu og tíma lokunar í árslok á síðasta ári. Ferill var ekki skráður í hvert skipti sem lokun í árslok fór fram. Þar af leiðandi eru upplýsingar um keyrslu á lokun í árslok fyrir hvert ár ekki tiltækar til birtingar. Eftir að eiginleikinn hefur verið virkjaður er unnið með upplýsingar um ferli lokunar í árslok. Hægt er að skoða fylgiskjöl frá öllum ferlum lokunar í árslok á síðunni **Fylgiskjalafærslur**, jafnvel þeim sem keyrðar voru fyrir virkjun eiginleikans. 

## <a name="general-ledger-the-year-end-close-process-is-failing-because-of-the-following-error-the-year-end-close-cant-be-run-because-one-or-more-ledger-transactions-posted-into-the-fiscal-year-that-you-are-closing-were-settled-to-a-ledger-transaction-in-a-different-fiscal-year-what-does-this-error-mean"></a>Fjárhagur: Ferli lokunar í árslok er að mistakast vegna eftirfarandi villu: „Ekki er hægt að keyra lokun í árslok vegna þess að ein eða fleiri fjárhagsfærslur sem eru bókaðar á fjárhagsárið sem verið er að loka voru jafnaðar við fjárhagsfærslu á öðru fjárhagsári.“ Hvað þýðir þessi villa?

Þar sem eiginleikinn **Munurinn á fjárhagsjöfnun og lokun í árslok** er virkur eru aðeins jafnaðar fjárhagsfærslur frá fjárhagsárinu sem verið er að loka útilokaðar í opnunarstöðu. Þetta veldur því að mismunur er á debet- og kreditfærslum. Frekari upplýsingar eru í [Munurinn á fjárhagsjöfnun og lokun í árslok](awareness-between-ledger-settlement-year-end-close.md).

## <a name="general-ledger-reversal-of-the-year-end-close-process-is-failing-because-of-the-following-error-the-year-end-close-for-112022-cant-be-reversed-because-beginning-balance-transaction-have-been-ledger-settled-in-fiscal-year-112023-what-does-this-error-mean"></a>Fjárhagur: Bakfærsla á ferli lokunar í árslok er að mistakast vegna eftirfarandi villu: „Ekki er hægt að bakfæra lokun í árslok fyrir 1/1/2022 vegna þess að upphafsstöðufærsla hefur verið gerð upp í fjárhag á fjárhagsárinu 1/1/2023.“ Hvað þýðir þessi villa?

Þar sem eiginleikinn **Munurinn á fjárhagsjöfnun og lokun í árslok** er virkur er ekki leyfilegt að bakfæra árslokavinnslu ef opnunarfærslur hafa verið gerðar upp á nýju fjárhagsári. Bakfæra skal fjárhagsjöfnun á nýja fjárhagsárinu 2023 áður en lokun í árslok fyrir 1. janúar 2022 er bakfærð. Að öðrum kosti skal endurloka árinu fyrir 1. janúar 2022, en aðeins fyrir nýjar leiðréttingarfærslur. Til að loka árinu aftur fyrir leiðréttingar eingöngu skal gera fjárhagsfæribreytuna **Eyða fyrirliggjandi árslokafærslum þegar ári er lokað aftur** óvirka.

## <a name="general-ledger-why-isnt-the-ledger-settlement-automation-processing-decembers-ledger-settlement-transactions"></a>Fjárhagur: Hvers vegna er sjálfvirkni fjárhagsjöfnunar ekki að vinna úr jöfnunarfærslum í fjárhag fyrir desember?

Eiginleikinn **Sjálfvirknivæða fjárhagsjafnanir** keyrir sjálfvirkni fyrir færslur sem eru dagsettar frá fyrsta degi fjárhagsársins til núverandi dagsetningar þegar tilvikið er keyrt. Á fjárhagsárum sem lýkur 31. desember gæti þurft að breyta dagsetningu keyrslu fyrir tilvikið til að tryggja að það sé keyrt í desember. Til dæmis er sjálfvirkni sett upp til að keyra á fyrsta degi hvers mánaðar. Þessi sjálfvirkni verður keyrð 1. desember 2022 og keyrsla er á áætlun 1. janúar 2023. Mælt er með að tilvikinu sé breytt fyrir 1. janúar 2023 þannig að það keyri í staðinn 31. desember 2022. Með þessari breytingu er tryggt að færslurnar sem eru dagsettar 2. desember til og með 31. desember verði teknar með í sjálfvirku uppgjöri.

## <a name="general-ledger-whats-the-difference-between-the-reverse-year-end-close-action-and-the-delete-existing-year-end-entries-when-reclosing-parameter-for-year-end-close"></a>Fjárhagur: Hver er munurinn á aðgerðinni „Bakfæra lokun við árslok“ og færslunum „Eyða núverandi færslum fyrir árslok“ þegar verið er að endurloka færibreytu fyrir lokun við árslok?

Ruglingur getur verið hvað varðar muninn á aðgerðinni **Bakfæra lokun í árslok** og færslunum **Eyða núverandi færslum fyrir árslok** þegar verið er að endurloka færibreytunni í fjárhag (**Fjárhagur \> Uppsetning fjárhags \> Færibreytur fjárhags**).

Veljið aðgerðina **Bakfæra lokun í árslok** þegar lokunarferli í árslok er keyrt til að eyða öllum færslum lokunar- og opnunarstöðu rétt eins og lokun í árslok hafi aldrei verið keyrð. Í þessu tilviki verður fylgiskjölunum eytt. Lokun í árslok verður ekki keyrð aftur sjálfkrafa. Til að keyra lokun í árslok skal velja aðgerðina **Keyra lokun í árslok**.

Færibreytan **Eyða fyrirliggjandi árslokafærslum þegar ári er lokað aftur** í Fjárhag er aðeins notuð þegar verið er að keyra (ekki bakfæra) lokun í árslok. Ef færibreytan er stillt á **Já** verður öllum færslum lokunar- og opnunarstöðu eytt og lokun í árslok verður keyrð á nýjan leik. Þessi valkostur er notaður þegar fyrirtæki vill að allar færslur, þ.m.t. leiðréttingar frá síðustu lokun í árslok, verði bókaðar í einni bókhaldsfærslu fyrir færslur lokunar- og opnunarstöðu. Ef færibreytan er stillt á **Nei** verða allar færslur lokunar- og opnunarstöðu geymdar áfram. Þeim er ekki eytt. Þess í stað verður ný færsla lokunar- og opnunarstöðu aðeins búin til fyrir annaðhvort delta-færsluna eða nýjar færslur sem hafa verið bókaðar eftir síðustu lokun í árslok fyrir það fjárhagsár.

> [!NOTE]
> Færsla lokunarstöðu er búin til á árinu sem verið er að loka. Þetta gerist aðeins ef **Stofna lokunarfærslur í millifærslu** færibreytan í fjárhag er stillt á **Já**. Færsla opnunarstöðu er alltaf stofnuð vegna þess að hún er upphafsstaða næsta árs.

## <a name="general-ledger-what-is-the-difference-between-close-all-and-close-single-options-on-the-transfer-profit-and-loss-dimension-section-of-the-year-end-close-process"></a>Fjárhagur: Hver er munurinn á valkostunum „Loka öllum“ og „Loka einni“ í hlutanum „Flytja víddir hagnaðar og taps“ í ferlinu Lokun í árslok?

**Loka öllum** viðheldur upphaflegum fjárhagsvíddargildum úr bókuðum færslum og notar þær til að stofna opnunarstöður fyrir lykil óráðstafaðs eigin fjár. Aðskildar upphafsstöður óráðstafaðs eigin fjár verða stofnaðar fyrir hverja einkvæma samsetningu fjárhagsvíddargilda. Ef **Loka einni** er valið eru allar bókaðar færslur sem eru með þá fjárhagsvídd dregnar saman í upphafsstöðu óráðstafaðs eigin fjár fyrir víddargildið sem er fært inn í reitinn sem birtist eftir **Loka einni**. 

Til dæmis voru allar færslur fyrir fjárhagsárið bókaðar með lykilskipulaginu Aðallykill - Deild. Fyrir fjárhagsvíddina Deild í sniðmátinu er **Loka einni** valið og 100 er fært inn sem víddargildið. Ef heildartekjur af öllum færslum sem bókaðar eru í deildir 200, 300 og 400 er 100.000 USD verður ein opnunarstaða stofnuð fyrir Óráðstafað eigið fé - 100. Ef **Loka einni** er valið en fjárhagsvíddargildið er skilið eftir autt verða allar færslur bókaðar í óráðstafað eigið fé og víddargildið verður autt.

## <a name="general-ledger-when-i-select-close-single-option-on-the-transfer-profit-and-loss-dimension-section-of-the-year-end-close-process-will-my-detailed-transactional-information-be-lost"></a>Fjárhagur: Munu ítarlegu færsluupplýsingarnar mínar glatast þegar ég vel „Loka einni“ í hlutanum „Flytja víddir hagnaðar og taps“ í ferlinu Lokun í árslok?

Valkostirnir **Loka öllum** og **Loka einni** eru notaðir til að tilgreina hvaða fjárhagsvíddir í færslunum sem bókaðar eru á rekstrarreikninga verða fluttar í aðallykil óráðstafaðs eigin fjár. Þetta hefur ekki áhrif á sögulega, ítarlega bókun í rekstrarreikningi, sem verður áfram ítarleg. Valkosturinn hefur áhrif á nákvæmni þeirra upplýsinga sem eru færðar á lykla óráðstafaðs eigin fjár sem opnunarstaða á nýja árinu. 

## <a name="general-ledger-the-year-end-close-process-is-failing-because-the-reporting-currency-for-the-year-does-not-balance-what-does-this-mean"></a>Fjárhagur: Ferlið „Lokun í árslok“ er að mistakast vegna þess að skýrslugjaldmiðill fyrir árið stemmir ekki. Hvað þýðir það?

Þessi villa getur komið upp eftir að eiginleikinn **Munurinn á fjárhagsjöfnun og lokun í árslok**  (eiginleikinn „Skilningur“) hefur verið virkjaður. Þegar eiginleikinn er virkur verða fjárhagsfærslur sem hafa verið jafnaðar ekki lengur hafðar með í opnunarstöðu næsta fjárhagsárs þegar lokun í árslok er keyrð í fjárhag. Það getur verið krefjandi fyrir viðskiptavini að undanskilja fjárhagsfærslur sem hafa verið jafnaðar við lokun við árslok ef Fjárhagur er skilgreindur með skýrslugjaldmiðli.   
Fjárhagsjöfnun er aðeins framkvæmd fyrir bókhaldsgjaldmiðilinn.  Þegar fjárhagsfærslur eru jafnaðar tryggir sannprófun aðeins að debetfærslur í bókhaldsgjaldmiðli séu jafnar kreditfærslum í bókhaldsgjaldmiðli. Upphæðir í skýrslugjaldmiðli fyrir þessar fjárhagsfærslur eru ekki sannprófaðar og eru hugsanlega ekki þannig að debetfærslur = kreditfærslur.  Að auki reiknar fjárhagsjöfnun ekki sjálfkrafa út og bókar hagnað/tap í skýrslugjaldmiðlinum.  Vegna þessara takmarkana verður hagnaðar-/tapfærsla að vera til staðar í skýrslugjaldmiðli þegar fjárhagsjöfnun er gerð.  Ef hagnaður/tap er ekki með í fjárhagsjöfnun leiðir lokun í árslok til þess að skilaboð birtast um mismun.  Frekari upplýsingar eru í [Mismunur er á „Munur á fjárhagsjöfnun“ og skýrslugjaldmiðli](reporting-currency-yec.md).

## <a name="general-ledger-what-can-be-changed-to-help-enhance-the-performance-of-year-end-processing"></a>Fjárhagur: Hverju er hægt að breyta til að hjálpa til við að auka afköstin í árslokavinnslu?

Hægt er að gera nokkrar breytingar til að bæta afköst við lokun í árslok. Mælt er með að skoða hvort þessar ráðlögðu breytingar henti viðkomandi fyrirtæki.

### <a name="optimize-year-end-close-service"></a>Þjónustan „Fínstilla lokun í árslok“

Þjónustan **Fínstilla lokun í árslok** gerir viðskiptavinum Microsoft Dynamics 365 Finance kleift að flýta fyrir lokun í árslok með því að færa úrvinnslu lokunar í árslok í örþjónustu. Tíminn sem sparast með skilvirkri lokun í árslok gerir öllum Finance-teymum kleift að bregðast tímanlega við nauðsynlegum breytingum áður en fjárhagsskýrslur eru búnar til. Með því að vinna lokun í árslok með örþjónustu má nýta mikilvæg tilföng í annað mikilvægara. Vinnsluhækkunin lágmarkar álagið á SQL Server og gefur viðskiptavinum tækifæri til að hraða vinnslu á lokun í árslok.

Þjónustan **Fínstilla lokun í árslok** er tiltæk í útgáfu 10.0.31, þannig að fleiri viðskiptavinir geti notað nýju þjónustuna fyrir lokun á árinu 2022. Þjónustan hefur auk þess verið sett afturvirkt í útgáfur 10.0.30 og 10.0.29. Frekari upplýsingar er að finna í [Fínstilla lokun í árslok](optimize-year-end-close.md).

### <a name="dimension-sets"></a>Víddasamstæður

Þegar lokun í árslok er keyrð er staða hverrar víddasamstæðu endurbyggð. Þetta hefur bein áhrif á afkomu. Sum fyrirtæki stofna víddasamstæður að óþörfu vegna þess að þær voru notaðar einhvern tímann áður eða gætu verið notaðar á einhverjum tímapunkti. Þessar óþörfu víddasamstæður eru samt sem áður endurbyggðar við lokun í árslok, sem lengir ferlið. Gefðu þér tíma til að skoða víddasamstæðurnar þínar og eyða öllum samstæðum sem eru óþarfar.

Óþörfu víddasamstæðurnar hafa líka áhrif á runuvinnsluna **BudgetDimensionFocusInitializeBalance** (**Fjárhagur \> Bókhaldslykill \> Víddir \> Fjárhagsvíddasamstæður**).

[![Fjárhagsvíddasamstæður.](./media/faq-2020-yr-end-04.png)](./media/faq-2020-yr-end-04.png)

### <a name="year-end-close-template-configuration"></a>Sniðmátsskilgreining árslokalokunar

Sniðmát árslokalokunar gerir fyrirtækjum kleift að velja fjárhagsvíddarstigið sem vinna á með þegar stöður hagnaðar og taps eru fluttar í óráðstafað eigið fé. Stillingarnar gera fyrirtækinu kleift að vinna með ítarlegar fjárhagsvíddir (**Loka öllum**) þegar stöðurnar eru fluttar í óráðstafað eigið fé eða velja að taka saman upphæðirnar í eitt víddargildi (**Loka einni**). Hægt er að skilgreina þetta fyrir hverja fjárhagsvídd. Frekari upplýsingar um þessar stillingar er að finna í greininni [Lokun í árslok](year-end-close.md).

Mælt er með að þú metir kröfur fyrirtækisins og, ef mögulegt, loka eins mörgum víddum og hægt er með valkostinum **Loka einni** fyrir árslok til að bæta afköst. Með því að loka í einu víddargildi (sem má einnig vera autt gildi) reiknar kerfið út færri atriði þegar stöður eru ákvarðaðar fyrir lykilfærslur óráðstafaðs eigin fjár.

### <a name="degenerate-dimensions"></a>Blindvíddir

Blindvídd er lítið sem ekkert hægt að endurnýta, hvort sem er stök eða með öðrum víddum. Tvær gerðir blindvídda er til. Fyrri gerðin er vídd sem er blindvídd þegar hún stendur stök. Yfirleitt birtist slík blindvídd aðeins í einni færslu eða þá mjög fáum. Hin gerðin er vídd sem verður blindvídd í tengslum við eina eða fleiri víddir til viðbótar sem sýna sömu eiginleika, samkvæmt þeim umröðunum sem hægt er að mynda. Blindvídd getur haft veruleg áhrif á vinnslu lokunar í árslok. Til að lágmarka möguleika á mögulegum vandamálum við vinnslu skal skilgreina allar blindvíddir sem **Loka einni** í uppsetningu lokunar í árslok eins og lýst er í hlutanum hér á undan.

## <a name="accounts-payable-what-changes-have-been-made-to-support-1099-year-end-reporting-for-2022"></a>Viðskiptaskuldir: Hvaða breytingar hafa verið gerðar til að styðja 1099-árslokaskýrslugerð fyrir 2022?

#### <a name="update-to-all-1099-forms"></a>Uppfæra í öll 1099 eyðublöð

Eftirfarandi breytingar hafa verið gerðar á öllum 1099 eyðublöðum fyrir skattárið 2022:

- Árið 2021 var árið fast á 1099 eyðublöðum. Frá og með árinu 2022 er árið fyllt út með skýrslunni.

#### <a name="1099-misc"></a>1099-MISC

Eftirfarandi uppfærslur hafa verið gerðar á eyðublaði 1099-MISC fyrir skattárið 2022:

- Reitur 13: Tilgreinir nú FATCA (lög um skattlagningu vegna erlendra reikninga).
- Reitur 14: Nú notaður til að tilkynna um of háar „gylltar fallhlífagreiðslur“.
- Reitur 15: Nú notaður til að tilkynna um greiðsluna samkvæmt NQDC (óviðurkenndar frestaðar tekjur).
- Reitur 16: Nú notaður til að tilkynna um afdregna skatta ríkis.
- Reitur 17: Nú notaður til að tilkynna um ríkisnúmer greiðanda.
- Reitur 18: Nú notaður til að tilkynna um tekjur ríkis.

## <a name="accounts-payable-1099--how-do-i-change-the-1099-box-and-values-for-a-vendor-that-wasnt-tracking-1099-information-throughout-the-year"></a>Viðskiptaskuldir: 1099 – Hvernig breyti ég 1099-reitnum og -gildum fyrir lánardrottin sem rakti ekki 1099-upplýsingar yfir árið?

Nota skal aðgerðina **Uppfæra 1099** til að fara í gegnum áður greiddar reikningsfærslur og endurúthluta 1099-gögnum á réttan hátt samkvæmt stillingunum í flipanum **1099-skatteyðublað** á síðunni **Lánardrottinn**. Til að nota aðgerðina **Uppfæra 1099** skal fara í **Viðskiptaskuldir \> Lánardrottnar \> Allir lánardrottnar**, velja lánardrottin og velja svo **Uppfæra 1099** á flipanum **Lánardrottinn** á aðgerðasvæðinu.

## <a name="can-i-run-the-update-1099-functionality-for-all-my-vendors-at-once"></a>Get ég keyrt eiginleikann „Uppfæra 1099“ fyrir alla lánardrottna mína í einu?

Hægt er að nota síðuna **Uppfæra 1099-gögn fyrir marga lánardrottna** til að uppfæra 1099-reitinn í lánardrottinsfærslu og til að uppfæra færslur með upplýsingum úr 1099-reitnum. Til að opna þessa síðu skal fara í **Viðskiptaskuldir \> Reglubundið verkefni \> 1099-skatteyðublað**. Til að opna síðuna þarf að úthluta þér öryggisréttindum fyrir **Uppfæra 1099-reit og færslur fyrir marga lánardrottna**.

## <a name="accounts-payable-1099--recalculate-existing-1099-amounts-versus-update-all-in-the-update-1099-utility"></a>Viðskiptaskuldir: 1099 – „Endurreikna núverandi 1099-upphæðir“ gagnvart „Uppfæra allt“ í 1099-uppfærsluforritinu

Gátreiturinn **Endurreikna núverandi 1099-upphæðir** endurstillir 1099-upphæðina í samtals greidd gildi þegar hann er notaður ásamt gátreitnum **Uppfæra allt**.

[![Færslur 1099-skatteyðublaðs: Áður en reglubundin uppfærsla er keyrð.](./media/faq-2020-yr-end-08.png)](./media/faq-2020-yr-end-08.png)

Gátreiturinn **Endurreikna núverandi 1099-upphæðir** er aðeins notaður þegar það eru 1099-gildi að hluta til á reikningnum eða ef reikningnum var breytt á 1099-skatteyðublaðinu. Til dæmis ef þú ert með reikning sem er metinn á 1.000,00 USD en notandinn slær handvirkt inn 1099-upphæð sem nemur 500,00 USD á reikninginn.

[![Færslur 1099-skatteyðublaðs: Merkir bæði Uppfæra allt og Endurreikna núverandi 1099-upphæðir.](./media/faq-2020-yr-end-07.png)](./media/faq-2020-yr-end-07.png)

Þegar reikningurinn er greiddur verður 500 USD 1099-upphæðin sem verður greidd. Ef þú framkvæmir endurútreikning verður 1099-upphæðinni breytt í 1.000 USD, sem er heildarupphæðin sem var greidd.

[![Færslur 1099-skatteyðublaðs: Eftir reglubundna 1099-keyrslu.](./media/faq-2020-yr-end-09.png)](./media/faq-2020-yr-end-09.png)

## <a name="accounts-payable-1099--manually-create-1099-transactions"></a>Viðskiptaskuldir: 1099 – Stofna handvirkt 1099-færslur

Fyrirtæki gæti þurft að stofna 1099-færslur handvirkt sem ekki eru tengdar reikningi. Hægt er að bæta við handvirkum 1099-færslum með því að fara í **Viðskiptaskuldir \> Reglubundin verk \> 1099-skatteyðublað \> Jöfnun lánardrottins á 1099-eyðublöðum**. Veljið hnappinn **Handvirkar 1099-færslur**.

Handvirkt stofnaðar 1099-færslur eru ekki uppfærðar með ferlinu **Uppfæra allt** eða **Endurreikna núverandi 1099-upphæðir** í hjálparforritinu **Uppfæra 1099**.

## <a name="accounts-payable-1099--does-dynamics-365-finance-support-the-1096-form"></a>Viðskiptaskuldir: 1099 – Styður Dynamics 365 Finance 1096-eyðublaðið?

Dynamics 365 Finance prentar ekki út eyðublaðið 1096 Annual Summary and Transmittal of US Information Returns.

## <a name="accounts-payable-1099--are-there-any-new-features-that-support-1099-reporting-for-public-sector"></a>Viðskiptaskuldir: 1099 – Eru til nýir eiginleikar sem styðja 1099 skýrslugerð fyrir opinbera geirann?

Nýjum eiginleika fyrir opinbera geirann, **Uppfæra 1099-upplýsingar eftir aðallykli**, hefur verið bætt við, sem hægt er að virkja á vinnusvæðinu **Eiginleikastjórnun**. Þessi eiginleiki gerir kleift að tengja 1099-gildin fyrir lánardrottin eftir aðallyklinum í dreifingu á fjárhagsupphæð, frekar en eftir sjálfgefna lyklinum í lánardrottnafærslunni.

Frekari upplýsingar eru í [Setja upp lánardrottna fyrir skýrsluna 1099](../localizations/noam-usa-set-up-vndrs-1099-rprtg.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
