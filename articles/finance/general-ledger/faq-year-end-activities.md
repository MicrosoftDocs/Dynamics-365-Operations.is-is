---
title: Algengar spurningar um verkþætti árslokunar
description: Í þessari grein er að finna spurningar sem geta komið upp við lokun árs, sem og svör sem kunna að koma að gagni við verkþætti lokunar í árslok.
author: moaamer
ms.date: 11/08/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 2a75d1e3e68837a437b2369ba369b0063e015b12
ms.sourcegitcommit: 78cbb125f20a33df38bda0546203b8f837cbcd93
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/09/2022
ms.locfileid: "9751958"
---
# <a name="year-end-activities-faq"></a>Algengar spurningar um verkþætti árslokunar 

[!include [banner](../includes/banner.md)]

Í þessari grein er að finna spurningar sem geta komið upp við lokun árs, sem og svör sem kunna að koma að gagni við verkþætti lokunar í árslok. Upplýsingarnar í þessari grein eru fyrst og fremst tengdar spurningum sem varða verkþætti lokunar í árslok fyrir fjárhag og viðskiptaskuldir.

## <a name="general-ledger-year-end-enhancements"></a>Viðbætur fjárhags í árslok 
Útgáfu 10.0.20 fylgdu endurbætur fyrir lokun í árslok, sem eru sjálfgefið virkar frá og með útgáfu 10.0.25. Ef fyrirtækið notar eldri útgáfu en 10.0.25 er mælt með að þessi eiginleiki sé virkjaður áður en lokun í árslok hefst. Kveikja þarf á þessum eiginleika í kerfinu til að hægt sé að nota hann. Stjórnendur geta notað vinnusvæðið „Eiginleikastjórnun“ til að skoða stöðu eiginleikans og kveikja á honum ef þess er krafist. Þar er eiginleikinn skráður á eftirfarandi hátt:

 - Eining: Fjárhagur
 - Heiti eiginleika: Endurbætur fyrir fjárhag í árslok

Uppsetning sniðmáta fyrir lokun í árslok hefur verið færð á nýja uppsetningarsíðu, **Uppsetning sniðmáts árslokalokunar**. Núverandi síða lokunar í árslok mun breytast, á svipaðan hátt og endurmat á erlendum gjaldmiðli fjárhags, þar sem listi birtist í hvert skipti sem árslokalokun er keyrð eða bakfærð. Aðalbókari getur hafið lokun í árslok á nýju síðunni. 

Til að bakfæra lokun í árslok skal velja nýjasta fjárhagsárið fyrir viðeigandi lögaðila og velja hnappinn **Bakfæra árslokalokun**. Bakfærslan mun eyða bókhaldsfærslum fyrir síðustu lokun í árslok og mun ekki aftur keyra lokun í árslok sjálfkrafa. 

Hægt er að keyra lokun í árslok aftur með því að hefja endurræsa ferlið fyrir fjárhagsárið og lögaðilann. Ferlið heldur áfram að nota færibreytustillingu fjárhags til að skera úr um hvort endurkeyrsla árslokalokunar muni einungis taka til greina nýjar eða breyttar færslur, eða bakfæra að fullu fyrri lokun og endurkeyra ferlið fyrir allar færslur.  

## <a name="general-ledger-how-do-i-know-that-were-running-year-end-close-and-not-undoing-year-end-close"></a>Fjárhagur: Hvernig veit ég að við erum að keyra árslokalokun en ekki að afturkalla árslokalokun?
Við höfum séð fyrirtæki reyna að keyra lokun í árslok en voru í staðinn að afturkalla árslokalokun. Ef árslokalokun gengur mjög hratt fyrir sig eða hún býr ekki til opnunarstöður skal villuleita stillinguna **Afturkalla fyrri lokun** í **Lokun í árslok** (**Fjárhagur > Tímabil lokunar > Lokun í árslok > Keyra fjárhagslokun**). 

[![Keyrsla lokunar í árslok í samanburði við afturköllun lokunar í árslokalok.](./media/faq-2020-yr-end-01.png)](./media/faq-2020-yr-end-01.png)

Ef valkosturinn **Afturkalla fyrri lokun** er stilltur á **Já** er verið að afturkalla fyrri árslokalokun. Þegar afturköllun er keyrð verður öllum færslum lokunar- og opnunarstöðu eytt rétt eins og árslokalokun hafi aldrei verið keyrð. Fylgiskjölunum er eytt. Lokun í árslok verður ekki keyrð aftur sjálfkrafa. Hefja þarf ferlið aftur og í þetta skipti breyta **Afturkalla fyrri lokun** í **Nei**. 

> [!NOTE]
> Færsla lokunarstöðu er valfrjálst stofnuð á árinu sem verið er að loka. Þetta gerist aðeins ef fjárhagsfæribreytan **Stofna lokunarfærslur í millifærslu** er stillt á **Já**. Færsla opnunarstöðu er alltaf stofnuð vegna þess að hún er upphafsstaða næsta árs.  
 
## <a name="general-ledger-what-is-the-difference-between-undo-and-delete-gl-parameter-for-year-end-close"></a>Fjárhagur: Hver er munurinn á því að afturkalla og eyða færibreytum fjárhags fyrir lokun í árslok?
Ruglingur getur orðið vegna mismunarins milli færibreytunnar **Afturkalla fyrri lokun**, sem er í glugganum **Lokun í árslok**, og færibreytunnar **Eyða lokunarfærslum árs í millifærslu** í fjárhag (**Fjárhagur > Tímabil lokunar > Lokun í árslok > Keyra fjárhagslokun**).  

[![Munurinn á því að afturkalla og eyða færibreytum fjárhags fyrir lokun í árslok.](./media/faq-2020-yr-end-02.png)](./media/faq-2020-yr-end-02.png)

Veljið **Afturkalla fyrri lokun** í fellivalmynd svargluggans þegar lokunarferli í árslok er keyrt til að eyða öllum færslum lokunar- og opnunarstöðu rétt eins og lokun í árslok hafi aldrei verið keyrð. Fylgiskjölunum verður eytt. Lokun í árslok verður ekki keyrð aftur sjálfkrafa. Til að keyra lokun í árslok þarf að hefja þetta ferli aftur og í þetta skipti breyta **Afturkalla fyrri lokun** í **Nei** (**Fjárhagur > Fjárhagsuppsetning > Fjárhagsfæribreytur**). 

[![Stillingar fjárhagsfæribreytu.](./media/faq-2020-yr-end-03.png)](./media/faq-2020-yr-end-03.png)

Færibreytan **Eyða lokunarfærslum árs í millifærslu** í fjárhag er aðeins notuð þegar lokun í árslok er keyrð (ekki afturkölluð) (valkosturinn **Afturkalla fyrri lokun** er stilltur á **Nei**). Ef færibreytan er stillt á **Já** verður öllum færslum lokunar- og opnunarstöðu eytt og lokun í árslok verður keyrð á nýjan leik. Þetta ferli er notað þegar fyrirtækið vill að allar færslur, þ.m.t. leiðréttingar frá síðustu árslokalokun, verði bókaðar í einni bókhaldsfærslu fyrir færslur lokunar- og opnunarstöðu. 

Ef þessi valkostur er stilltur á **Nei** verða allar færslur lokunar- og opnunarstöðu áfram. Þeim verður ekki eytt. Þess í stað verður ný færsla lokunar- og opnunarstöðu aðeins búin til fyrir annaðhvort delta-færsluna eða nýju færslurnar sem bókaðar voru eftir síðustu lokun í árslok fyrir það fjárhagsár.  

> [!NOTE]
> Færsla lokunarstöðu er búin til á árinu sem verið er að loka. Þetta gerist aðeins ef **Stofna lokunarfærslur í millifærslu** færibreytan í fjárhag er stillt á **Já**. Færsla opnunarstöðu er alltaf stofnuð vegna þess að hún er upphafsstaða næsta árs. 

## <a name="general-ledger-what-can-be-changed-to-enhance-performance-of-year-end-processing"></a>Fjárhagur: Hverju er hægt að breyta til að auka afköst í árslokavinnslu? 
Hægt er að gera nokkrar breytingar til að bæta frammistöðu við lokun í árslok. Mælt er með að þú skoðir hvort þessar ráðlögðu breytingar henti fyrirtækinu þínu.  

### <a name="dimension-sets"></a>Víddasamstæður
Þegar lokun í árslok er keyrð er hver staða víddasamstæðu endurbyggð, sem hefur bein áhrif á afköst. Sum fyrirtæki stofna víddasamstæður að óþörfu vegna þess að þær voru notaðar einhvern tímann áður eða gætu verið notaðar á einhverjum tímapunkti.  Þessar óþörfu víddasamstæður eru samt sem áður endurbyggðar við lokun í árslok, sem lengir ferlið. Taktu þér tíma til að meta víddasamstæðurnar þínar og eyddu öllum óþarfa víddasamstæðum.

Óþörfu víddasamstæðurnar hafa áhrif á runuvinnsluna **BudgetDimensionFocusInitializeBalance** (**Fjárhagur > Bókhaldslykill > Víddir > Fjárhagsvíddasamstæður**).

[![Fjárhagsvíddasamstæður.](./media/faq-2020-yr-end-04.png)](./media/faq-2020-yr-end-04.png)

### <a name="year-end-close-template-configuration"></a>Sniðmátsskilgreining árslokalokunar
Sniðmát árslokalokunar gerir fyrirtækjum kleift að velja fjárhagsvíddarstigið sem vinna á með þegar stöður hagnaðar og taps eru fluttar í óráðstafað eigið fé. Stillingarnar gera fyrirtækinu kleift að vinna með ítarlegar fjárhagsvíddir (**Loka öllum**) þegar stöðurnar eru fluttar í óráðstafað eigið fé eða velja að taka saman upphæðirnar í eitt víddargildi (**Loka einni**). Hægt er að skilgreina þetta fyrir hverja fjárhagsvídd. Frekari upplýsingar um þessar stillingar er að finna í greininni [Lokun í árslok](year-end-close.md).

Mælt er með að þú metir kröfur fyrirtækisins og, ef mögulegt, loka eins mörgum víddum og hægt er með valkostinum **Loka einni** fyrir árslok til að bæta afköst. Með því að loka í einu víddargildi (sem má einnig vera autt gildi) reiknar kerfið út færri atriði þegar stöður eru ákvarðaðar fyrir lykilfærslur óráðstafaðs eigin fjár.

## <a name="degenerate-dimensions"></a>Blindvíddir

Blindvídd er lítið sem ekkert hægt að endurnýta, hvort sem er stök eða með öðrum víddum. Tvær gerðir blindvídda er til. Fyrri gerðin er vídd sem er blindvídd þegar hún stendur stök. Yfirleitt birtist slík blindvídd aðeins í einni færslu eða þá mjög fáum. Hin gerðin er vídd sem verður blindvídd í tengslum við eina eða fleiri víddir til viðbótar sem sýna sömu eiginleika, samkvæmt þeim umröðunum sem hægt er að mynda. Blindvídd getur haft veruleg áhrif á vinnslu lokunar í árslok. Til að lágmarka möguleika á mögulegum vandamálum við vinnslu skal skilgreina allar blindvíddir sem **Loka einni** í uppsetningu lokunar í árslok eins og lýst er í hlutanum hér á undan.

## <a name="general-ledger-what-does-the-period-close-year-end-close-do"></a>Fjárhagur: Hvað gerir lokun tímabils, lokun í árslok?
 
[![Tímabil lokunar, árslokalokun.](./media/faq-2020-yr-end-05.png)](./media/faq-2020-yr-end-05.png)

### <a name="performance-improvements-for-rebuilding-financial-dimension-sets"></a>Afkastaendurbætur fyrir endurbyggingu fjárhagsvíddarsamstæða
Nýr eiginleiki sem var bætt við í útgáfu 10.0.16 bætir afköst við lokun í árslok og samstæðuferli. Eiginleikinn er með heiti, Afkastaendurbætur fyrir endurbyggingu fjárhagsvíddarsamstæða Þessi eiginleiki breytir því hvernig víddasamstæður eru endurbyggðar þannig að þær verða aðeins endurbyggðar fyrir viðeigandi tímaramma. Í fyrri útgáfum voru víddasamstæður endurbyggðar fyrir allar dagsetningar. Ef þú ert til dæmis að loka árinu 2020 mun kerfið aðeins endurbyggja stöðuna fyrir færslur innan fjárhagsársins 2020. Ef verið er að keyra sameiningu fyrir tímabilið frá 1. nóvember 2020 til 30. nóvember 2020 mun kerfið aðeins endurbyggja stöðurnar fyrir það tímabil.

Kveikja þarf á þessum eiginleika í kerfinu til að hægt sé að nota hann. Stjórnendur geta notað vinnusvæðið „Eiginleikastjórnun“ til að skoða stöðu eiginleikans og kveikja á honum ef þess er krafist. Þar er eiginleikinn skráður á eftirfarandi hátt:
 
- Eining: Fjárhagur
- Heiti eiginleika: Afkastaendurbætur fyrir endurbyggingu fjárhagsvíddarsamstæða

## <a name="accounts-payable-what-changes-have-been-made-to-support-1099-year-end-reporting-for-2021"></a>Viðskiptaskuldir: Hvaða breytingar hafa verið gerðar til að styðja 1099-árslokaskýrslugerð fyrir 2021?

DIV-, NEC- og MISC-eyðublöðunum var breytt lítillega árið 2021 og einhverjum reitum var bætt við.

#### <a name="div-new-box2e-2f"></a>DIV: nýr reitur 2e, 2f
 
- Reitur 2e. Sýnir í reit 1a þann hluta upphæðarinnar sem skal gefa upp sem ágóða í hluta 897 vegna sölu bandarískra fasteigna (USRPI).  
- Reitur 2f. Sýnir í reit 2a þann hluta upphæðarinnar sem skal gefa upp sem ágóða í hluta 897 vegna sölu USRPI (sölu bandarískra fasteigna). Athugið að reitir 2e og 2f eiga aðeins við um erlenda einstaklinga og lögaðila sem hafa tekjur sem breytast ekki þegar þær fara í gegnum, eða er dreift til, beinna eða óbeinna erlendra eigenda eða viðtakenda. Það er almennt túlkað sem tengt viðskiptum eða rekstri innan Bandaríkjanna. Skoðaðu leiðbeiningarnar fyrir skattframtalið. 
 
#### <a name="nec-new-box-2"></a>NEC: nýr reitur 2 
 
Ef hakað er við reit 2 skal gefa upp neytendavörur sem kosta 5000 Bandaríkjadali eða meira og sem voru seldar viðkomandi til endursölu, í kaupsölu, með innborgun eða á öðrum grundvelli. Almennt séð skal gefa upp tekjur af sölu þessara vara á þessum vörum í skrá C (eyðublað 1040). 
 
Á meðan hefur stærð eyðublaðs fyrir NEC breyst. Við prentun eru þrjú eyðublöð á síðu. 
 
#### <a name="misc-new-box-11"></a>MISC: nýr reitur 11 
 
Reitur 11 sýnir upphæðina sem greidd er fyrir kaup á fiski til endursölu frá öllum aðilum sem stunda viðskipti með eða rekstur tengdan fiski. Skoðaðu leiðbeiningarnar fyrir skattframtalið til að gefa upp þessar tekjur. 
 
#### <a name="electronic-filing"></a>Rafræn skattskil 
Upplýsingar um rafræn skattskil er að finna í [efni um kröfur fyrir rafræn skattskil](https://www.irs.gov/pub/irs-pdf/p1220.pdf).

Uppfæra sniðlýsingar og uppsetningu skráa fyrir rafræn skýrslu árið 2021 
- Hluti 2, „A“-færsla útgefanda. 
- Upphæðarkóðar – hærri staða svæðis 28–45, lengt í 18. 
 
#### <a name="sec-2-issuer-a-record-for-reporting-payments-on-form-1099-div"></a>Hluti 2, „A“-færsla útgefanda, fyrir skráningu greiðslna á eyðublað 1099-DIV: 
- Gerð upphæðar – hluta 897, hefðbundnar arðgreiðslur, og upphæðarkóða H bætt við. 
- Gerð upphæðar – hluta 897, söluhagnaður, og upphæðarkóða J bætt við. 
 
#### <a name="sec-3-payee-b-record"></a>Hluti 3, „B“-færsla móttakanda greiðslu 
- Almennar upplýsingafærslur – þriðja atriði uppfært úr 16 í 18 greiðsluupphæðasvæði. 
- Heiti svæðis greiðslu H – staða svæðis 247–258, heiti svæðis, lengd og almenn lýsing svæðis. 
- Heiti svæðis greiðslu J – staða svæðis 259–270, heiti svæðis, lengd og almenn lýsing svæðis. 
- Autt svæði uppfært svæðisstöðu 271–286. 
- Vísir fyrir erlent ríki uppfært í svæðisstöðu 287. 
- Svæði fyrstu nafnalínu móttakanda greiðslu uppfært í svæðisstöðu 288–327. 
- Svæði annarrar nafnalínu móttakanda greiðslu uppfært í svæðisstöðu 328–367. 
- Færslustaðsetningar, eyðublað 1099-MISC – svæðisstöðu 548 og vísi fyrir svæðisheiti FATCA-skilakrafna eytt. 
- Færslustaðsetningar, eyðublað 1099-NEC – 545-546 uppfærð í autt, svæði 547 uppfært í vísi fyrir beina sölu, lengd og lýsing og athugasemdir svæðis 548–722 uppfært í autt. 
 
#### <a name="sec-4-end-of-issuer-c-record"></a>Hluti 4, lok „C“-færslu útgefanda 
- Heiti svæðis greiðslu H – staða svæðis 304–321, heiti svæðis, lengd og almenn lýsing svæðis. 
- Heiti svæðis greiðslu J – staða svæðis 322–339, heiti svæðis, lengd og almenn lýsing svæðis. 
- Heiti svæði 340–499 – lengd uppfærð í 160. 
 
#### <a name="sec-5-state-totals-k-record"></a>Hluti 5, gefa upp samtölu „K“-færslu 
- Heiti svæðis greiðslu H – staða svæðis 304–321, heiti svæðis, lengd og almenn lýsing svæðis. 
- Heiti svæðis greiðslu J – staða svæðis 322–339, heiti svæðis, lengd og almenn lýsing svæðis. 
- Heiti svæði 340–499 – lengd uppfærð í 160.  

## <a name="accounts-payable-1099--how-do-i-change-the-1099-box-and-values-for-a-vendor-that-wasnt-tracking-1099-information-throughout-the-year"></a>Viðskiptaskuldir: 1099 – Hvernig breyti ég 1099-reitnum og -gildum fyrir lánardrottin sem var ekki að rekja 1099-upplýsingar yfir árið?
Notaðu aðgerðina „Uppfæra 1099“ (**Viðskiptaskuldir > Lánardrottnar > Allir lánardrottnar > Velja lánardrottin > Lánardrottnaflipi í borða > Uppfæra 1099**) til að fara í gegnum áður greiddar reikningsfærslur til að endurúthluta 1099-gögnum á réttan hátt samkvæmt stillingunum í flipanum **1099-skatteyðublað** á síðunni **Lánardrottinn**.

## <a name="can-i-run-the-update-1099-for-all-my-vendors-at-once"></a>Get ég keyrt Uppfærslu 1099 fyrir alla lánardrottna mína í einu?
Nr. Reglubundin 1099-uppfærsla er gerð fyrir einn lánardrottin í einu. Ef þörf er á þessari kröfu í fyrirtækinu skal kjósa með hugmyndinni sem ber heitið [Runuvinnsla fyrir uppfærslu 1099-gagna lánardrottins](https://experience.dynamics.com/ideas/idea/?ideaid=5493d608-350e-eb11-b5d9-0003ff68ded8).

## <a name="accounts-payable-1099--recalculate-existing-1099-amounts-versus-update-all-in-the-update-1099-utility"></a>Viðskiptaskuldir: 1099 – „Endurreikna núverandi 1099-upphæðir“ gagnvart „Uppfæra allt“ í 1099-uppfærsluforritinu
Gátreiturinn **Endurreikna núverandi 1099-upphæðir** endurstillir 1099-upphæðina í samtals greidd gildi þegar hann er notaður í tengslum við gátreitinn **Uppfæra allt**. 

[![Færslur 1099-skatteyðublaðs: Áður en reglubundin uppfærsla er keyrð.](./media/faq-2020-yr-end-07.png)](./media/faq-2020-yr-end-07.png)

Gátreiturinn **Endurreikna núverandi 1099-upphæðir** er aðeins notaður þegar það eru 1099-gildi að hluta til á reikningnum eða ef honum var breytt á 1099-skatteyðublaðinu. Ímyndaðu þér til dæmis að þú sért með reikning upp á 1000 Bandaríkjadali, en notandinn slær handvirkt 1099-upphæð inn á reikninginn sem nemur 500 Bandaríkjadölum.

[![Færslur 1099-skatteyðublaðs: Merkir bæði Uppfæra allt og Endurreikna núverandi 1099-upphæðir.](./media/faq-2020-yr-end-08.png)](./media/faq-2020-yr-end-08.png)

Þegar þetta er greitt verða 500 Bandaríkjadalir 1099-upphæðin sem verður greidd. Ef reglubundinn endurútreikningur er gerður mun kerfið breyta 1099-upphæðinni í 1000 Bandaríkjadali, sem er heildargreiðslan.

[![Færslur 1099-skatteyðublaðs: Eftir reglubundna 1099-keyrslu.](./media/faq-2020-yr-end-09.png)](./media/faq-2020-yr-end-09.png)

## <a name="accounts-payable-1099--manually-create-1099-transactions"></a>Viðskiptaskuldir: 1099 – Stofna handvirkt 1099-færslur
Fyrirtæki gæti þurft að stofna 1099-færslur handvirkt sem ekki eru tengdar reikningi. Hægt er að bæta við handvirkum 1099-færslum með því að fara í **Viðskiptaskuldir > Reglubundin verk > 1099-skatteyðublað > Jöfnun lánardrottins á 1099-eyðublöðum**. Veljið hnappinn **Handvirkar 1099-færslur**. 

Handvirkt stofnaðar 1099-færslur eru ekki uppfærðar með ferlinu **Uppfæra allt** eða **Endurreikna núverandi 1099-upphæðir** í hjálparforritinu **Uppfæra 1099**.

## <a name="accounts-payable-1099--does-dynamics-365-finance-support-the-1096-form"></a>Viðskiptaskuldir: 1099 – Styður Dynamics 365 Finance 1096-eyðublaðið? 

Dynamics 365 Finance prentar ekki út eyðublaðið 1096 Annual Summary and Transmittal of US Information Returns.

## <a name="accounts-payable-1099--are-there-any-new-features-that-support-1099-reporting-for-public-sector"></a>Viðskiptaskuldir: 1099 – Eru til nýir eiginleikar sem styðja 1099 skýrslugerð fyrir opinbera geirann? 
Nýjum eiginleika fyrir opinbera geirann, **Uppfæra 1099-upplýsingar eftir aðallykli**, hefur verið bætt við, sem hægt er að virkja á vinnusvæðinu **Eiginleikastjórnun**. Þessi eiginleiki gerir kleift að tengja 1099-gildin fyrir lánardrottin eftir aðallyklinum í dreifingu á fjárhagsupphæð, frekar en eftir sjálfgefna lyklinum í lánardrottnafærslunni.

Frekari upplýsingar eru í [Setja upp lánardrottna fyrir skýrsluna 1099](../localizations/noam-usa-set-up-vndrs-1099-rprtg.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
