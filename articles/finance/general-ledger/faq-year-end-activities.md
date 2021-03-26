---
title: Algengar spurningar um verkþætti árslokunar
description: Þetta efnisatriði hefur verið sett saman til að aðstoða við verkþætti árslokalokunar.
author: kweekley
manager: tfehr
ms.date: 01/25/2021
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a9feafcab5969e9ec8fcbb8a6903d7b59505f6ae
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249412"
---
# <a name="year-end-activities-faq"></a>Algengar spurningar um verkþætti árslokunar 

Þetta efnisatriði hefur verið sett saman til að aðstoða við verkþætti árslokalokunar. Upplýsingarnar í þessu efnisatriði einblína fyrst og fremst á spurningar sem varða verkþætti árslokalokunar fyrir fjárhag og viðskiptaskuldir.

## <a name="general-ledger-how-do-i-know-that-were-running-year-end-close-and-not-undoing-year-end-close"></a>Fjárhagur: Hvernig veit ég að við erum að keyra árslokalokun en ekki að afturkalla árslokalokun?
Við höfum séð fyrirtæki reyna að keyra lokun í árslok en voru í staðinn að afturkalla árslokalokun. Ef árslokalokun gengur mjög hratt fyrir sig eða hún býr ekki til opnunarstöður skal villuleita stillinguna **Afturkalla fyrri lokun** í **Lokun í árslok** (**Fjárhagur > Tímabil lokunar > Lokun í árslok > Keyra fjárhagslokun**). 

[![Keyrsla árslokalokunar í samanburði við afturköllun árslokalokun](./media/faq-2020-yr-end-01.png)](./media/faq-2020-yr-end-01.png)

Ef valkosturinn **Afturkalla fyrri lokun** er stilltur á **Já** er verið að afturkalla fyrri árslokalokun. Þegar afturköllun er keyrð verður öllum færslum lokunar- og opnunarstöðu eytt rétt eins og árslokalokun hafi aldrei verið keyrð. Fylgiskjölunum er eytt. Lokun í árslok verður ekki keyrð aftur sjálfkrafa. Hefja þarf ferlið aftur og í þetta skipti breyta **Afturkalla fyrri lokun** í **Nei**. 

> [!NOTE]
> Færsla lokunarstöðu er valfrjálst stofnuð á árinu sem verið er að loka. Þetta gerist aðeins ef fjárhagsfæribreytan **Stofna lokunarfærslur í millifærslu** er stillt á **Já**. Færsla opnunarstöðu er alltaf stofnuð vegna þess að hún er upphafsstaða næsta árs.  
 
## <a name="general-ledger-what-is-the-difference-between-undo-and-delete-gl-parameter-for-year-end-close"></a>Fjárhagur: Hver er munurinn á því að afturkalla og eyða færibreytum fjárhags fyrir lokun í árslok?
Ruglingur getur orðið vegna mismunarins milli færibreytunnar **Afturkalla fyrri lokun**, sem er í glugganum **Lokun í árslok**, og færibreytunnar **Eyða lokunarfærslum árs í millifærslu** í fjárhag (**Fjárhagur > Tímabil lokunar > Lokun í árslok > Keyra fjárhagslokun**).  

[![Munurinn á því að afturkalla og eyða færibreytum fjárhags fyrir lokun í árslok](./media/faq-2020-yr-end-02.png)](./media/faq-2020-yr-end-02.png)

Veljið **Afturkalla fyrri lokun** í fellivalmynd svargluggans þegar lokunarferli í árslok er keyrt til að eyða öllum færslum lokunar- og opnunarstöðu rétt eins og lokun í árslok hafi aldrei verið keyrð. Fylgiskjölunum verður eytt. Lokun í árslok verður ekki keyrð aftur sjálfkrafa. Til að keyra lokun í árslok þarf að hefja þetta ferli aftur og í þetta skipti breyta **Afturkalla fyrri lokun** í **Nei** (**Fjárhagur > Fjárhagsuppsetning > Fjárhagsfæribreytur**). 

[![Stillingar fjárhagsfæribreytu](./media/faq-2020-yr-end-03.png)](./media/faq-2020-yr-end-03.png)

Færibreytan **Eyða lokunarfærslum árs í millifærslu** í fjárhag er aðeins notuð þegar lokun í árslok er keyrð (ekki afturkölluð) (valkosturinn **Afturkalla fyrri lokun** er stilltur á **Nei**). Ef færibreytan er stillt á **Já** verður öllum færslum lokunar- og opnunarstöðu eytt og lokun í árslok verður keyrð á nýjan leik. Þetta ferli er notað þegar fyrirtækið vill að allar færslur, þ.m.t. leiðréttingar frá síðustu árslokalokun, verði bókaðar í einni bókhaldsfærslu fyrir færslur lokunar- og opnunarstöðu. 

Ef þessi valkostur er stilltur á **Nei** verða allar færslur lokunar- og opnunarstöðu áfram. Þeim verður ekki eytt. Þess í stað verður ný færsla lokunar- og opnunarstöðu aðeins búin til fyrir annaðhvort delta-færsluna eða nýju færslurnar sem bókaðar voru eftir síðustu lokun í árslok fyrir það fjárhagsár.  

> [!NOTE]
> Færsla lokunarstöðu er búin til á árinu sem verið er að loka. Þetta gerist aðeins ef **Stofna lokunarfærslur í millifærslu** færibreytan í fjárhag er stillt á **Já**. Færsla opnunarstöðu er alltaf stofnuð vegna þess að hún er upphafsstaða næsta árs. 

## <a name="general-ledger-what-can-be-changed-to-enhance-performance-of-year-end-processing"></a>Fjárhagur: Hverju er hægt að breyta til að auka afköst í árslokavinnslu? 
Hægt er að gera nokkrar breytingar til að bæta frammistöðu við lokun í árslok. Mælt er með að þú skoðir hvort þessar ráðlögðu breytingar henti fyrirtækinu þínu.  

### <a name="dimension-sets"></a>Víddasamstæður
Þegar lokun í árslok er keyrð er hver staða víddasamstæðu endurbyggð, sem hefur bein áhrif á afköst. Sum fyrirtæki stofna víddasamstæður að óþörfu vegna þess að þær voru notaðar einhvern tímann áður eða gætu verið notaðar á einhverjum tímapunkti.  Þessar óþörfu víddasamstæður eru samt sem áður endurbyggðar við lokun í árslok, sem lengir ferlið. Taktu þér tíma til að meta víddasamstæðurnar þínar og eyddu öllum óþarfa víddasamstæðum.

Óþörfu víddasamstæðurnar hafa áhrif á runuvinnsluna **BudgetDimensionFocusInitializeBalance** (**Fjárhagur > Bókhaldslykill > Víddir > Fjárhagsvíddasamstæður**).

[![Samstæður fjárhagsvídda](./media/faq-2020-yr-end-04.png)](./media/faq-2020-yr-end-04.png)

### <a name="year-end-close-template-configuration"></a>Sniðmátsskilgreining árslokalokunar
Sniðmát árslokalokunar gerir fyrirtækjum kleift að velja fjárhagsvíddarstigið sem vinna á með þegar stöður hagnaðar og taps eru fluttar í óráðstafað eigið fé. Stillingarnar gera fyrirtækinu kleift að vinna með ítarlegar fjárhagsvíddir (**Loka öllum**) þegar stöðurnar eru fluttar í óráðstafað eigið fé eða velja að taka saman upphæðirnar í eitt víddargildi (**Loka einni**). Hægt er að skilgreina þetta fyrir hverja fjárhagsvídd. Frekari upplýsingar um þessar stillingar er að finna í efnisatriðinu [Lokun í árslok](year-end-close.md).

Mælt er með að þú metir kröfur fyrirtækisins og, ef mögulegt, loka eins mörgum víddum og hægt er með valkostinum **Loka einni** fyrir árslok til að bæta afköst. Með því að loka í einu víddargildi (sem má einnig vera autt gildi) reiknar kerfið út færri atriði þegar stöður eru ákvarðaðar fyrir lykilfærslur óráðstafaðs eigin fjár.

### <a name="10013-update-or-later"></a>10.0.13 uppfærsla eða nýrri
Ef búið er að uppfæra í útgáfu 10.0.13 eða nýrri frá síðasta skipti sem fyrirtækið keyrði lokun í árslok, gæti lokunarferli ársloka tekið lengri tíma sökum [Innleiðingar HashV2-eiginleika](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/verify-hash-function-changes-after-update-to-dynamics-365-finance-2020-release-wave-2). (Hugtakið *tætigildi (hash)* vísar í svæði sem er reiknað út frá öðrum strengjasvæðum. API til að reikna út GUID-gildi tætigildis var uppfært til að auka öryggið.) Til að flýta fyrir lokunarferli ársloka er mælt með að endurbyggja stöður víddasamstæðna áður en lokun í árslok er keyrð. Ef þú hefur þegar endurbyggt stöður víddasamstæðna eftir uppfærslu í 10.0.13, er ekki nauðsynlegt að keyra aftur ferli endurbyggingar.
 
## <a name="general-ledger--what-does-the-period-close--year-end-close-do"></a>Fjárhagur – Hvað gerir Tímabil lokunar – Lokun í árslok?
 
[![Tímabil lokunar, árslokalokun](./media/faq-2020-yr-end-05.png)](./media/faq-2020-yr-end-05.png)

### <a name="performance-improvements-for-rebuilding-financial-dimension-sets-new-feature"></a>Afkastaendurbætur fyrir endurbyggingu fjárhagsvíddarsamstæða (nýr eiginleiki)
Nýjum eiginleika sem var bætt við í útgáfu 10.0.16 bætir afköst við lokun í árslok og samstæðuferli. Eiginleikinn er með heiti, Afkastaendurbætur fyrir endurbyggingu fjárhagsvíddarsamstæða Þessi eiginleiki breytir því hvernig víddasamstæður eru endurbyggðar þannig að þær verða aðeins endurbyggðar fyrir viðeigandi tímaramma. Í fyrri útgáfum voru víddasamstæður endurbyggðar fyrir allar dagsetningar. Ef þú ert til dæmis að loka árinu 2020 mun kerfið aðeins endurbyggja stöðuna fyrir færslur innan fjárhagsársins 2020. Ef verið er að keyra sameiningu fyrir tímabilið frá 1. nóvember 2020 til 30. nóvember 2020 mun kerfið aðeins endurbyggja stöðurnar fyrir það tímabil.

Þar sem litið er á þennan eiginleika sem breytingu sem getur valdið bilun þarf að virkja hann með því að nota vinnusvæðið **Eiginleikastjórnun**.
 
[![Árslokalokun](./media/faq-2020-yr-end-06.png)](./media/faq-2020-yr-end-06.png)

## <a name="accounts-payable-what-changes-have-been-made-to-support-1099-year-end-reporting-for-2020"></a>Viðskiptaskuldir: Hvaða breytingar hafa verið gerðar til að styðja 1099-árslokaskýrslugerð fyrir 2020?

Tveimur nýjum eftirlitseiginleikum var bætt við fyrir 1099-árslokabreytingar á árinu 2020. Fyrri eiginleikinn, **Láta breytingar taka gildi fyrir eyðublöð 1099-NEC og 1099-MISC fyrir 2020**, var gefinn út um mitt árið sem áskilinn eiginleiki. Tilgangur hans er að tryggja að hægt sé að rekja 1099-færslugögn á árinu 2020 fyrir nýja eyðublaðið 1099-NEC. Þessi eiginleiki bætti við 1099-reitum sem þarf til að styðja við nýja 1099-NEC og uppfærði 1099-MISC-reitina. Þessi uppfærsla uppfærir einnig gögn lánardrottinsfærslu í 1099-hólfi lánardrottins. 

Seinni eftirlitseiginleikinn, **1099-uppgjör uppfærð samkvæmt skattalögum 2020**, inniheldur eftirfarandi breytingar.

- 1099-OID - Skattstofan hefur breytt eyðublaðinu í samfellda notkun.
   - Fylla verður út þriðja og fjórða tölustaf skýrslugerðarársins þegar það er prentað. Nota skal þriðja og fjórða tölustaf **Skýrslugerðarárs** í **Prentunarvalkostir 1099-skatteyðublaðs**. 

- 1099-NEC – Nýtt eyðublað fyrir 2020. Þetta skráir laun sem ekki snerta starfsmenn. 

-   1099-MISC – Vegna þess að eyðublað 1099-NEC var búið til, hefur skattstofan endurskoðað eyðublað 1099-MISC og endurraðað reitarnúmerum til að tilkynna tilteknar tekjur.
Breytingar á tekjuskráningu og reitarnúmerum eyðublaðs eru taldar upp hér að neðan.
   - Greiðandi gerði beinar sölur fyrir 5000 Bandaríkjadali eða meira (gátreitur) í reit 7.
   - Hagnaður uppskerutryggingar er tilkynntur í reit 9.
   - Heildarandvirði til lögfræðings er tilkynnt í reit 10.
   - Frestanir samkvæmt grein 409A eru tilkynntar í reit 12.
   - Óviðurkenndar frestaðar tekjur eru tilkynntar í reit 14.
   - Í reitum 15, 16 og 17 eru staðgreiðsluskattar ríkis gefnir, auðkennisnúmer ríkis og upphæð tekna í ríkinu, í þessari röð.

- Engar breytingar á 1099-DIV eða 1099-INT árið 2020.

- Rafræn skattskil – Sniðið hefur breyst til að koma til móts við nýja NEC-eyðublaðið og breytingar á MISC-reitum sem lýst er hér að ofan. Fyrir ákveðnar upplýsingar um kröfur rafrænna skattskila skal skoða [IRS Publication 1220](https://www.irs.gov/pub/irs-pdf/p1220.pdf).

## <a name="accounts-payable-1099--how-do-i-change-the-1099-box-and-values-for-a-vendor-that-wasnt-tracking-1099-information-throughout-the-year"></a>Viðskiptaskuldir: 1099 – Hvernig breyti ég 1099-reitnum og -gildum fyrir lánardrottin sem var ekki að rekja 1099-upplýsingar yfir árið?
Notaðu aðgerðina „Uppfæra 1099“ (**Viðskiptaskuldir > Lánardrottnar > Allir lánardrottnar > Velja lánardrottin > Lánardrottnaflipi í borða > Uppfæra 1099**) til að fara í gegnum áður greiddar reikningsfærslur til að endurúthluta 1099-gögnum á réttan hátt samkvæmt stillingunum í flipanum **1099-skatteyðublað** á síðunni **Lánardrottinn**.

## <a name="can-i-run-the-update-1099-for-all-my-vendors-at-once"></a>Get ég keyrt Uppfærslu 1099 fyrir alla lánardrottna mína í einu?
Nr. Reglubundin 1099-uppfærsla er gerð fyrir einn lánardrottin í einu. Ef þörf er á þessari kröfu í fyrirtækinu skal kjósa með hugmyndinni sem ber heitið [Runuvinnsla fyrir uppfærslu 1099-gagna lánardrottins](https://experience.dynamics.com/ideas/idea/?ideaid=5493d608-350e-eb11-b5d9-0003ff68ded8).

## <a name="accounts-payable-1099--recalculate-existing-1099-amounts-vs-update-all-in-the-update-1099-utility"></a>Viðskiptaskuldir: 1099 – „Endurreikna núverandi 1099-upphæðir“ gagnvart „Uppfæra allt“ í 1099-uppfærsluforritinu.
Gátreiturinn **Endurreikna núverandi 1099-upphæðir** endurstillir 1099-upphæðina í samtals greidd gildi þegar hann er notaður í tengslum við gátreitinn **Uppfæra allt**. 

[![Færslur 1099-skatteyðublaðs: Áður en reglubundin uppfærsla er keyrð](./media/faq-2020-yr-end-07.png)](./media/faq-2020-yr-end-07.png)

Gátreiturinn **Endurreikna núverandi 1099-upphæðir** er aðeins notaður þegar það eru 1099-gildi að hluta til á reikningnum eða ef honum var breytt á 1099-skatteyðublaðinu. Ímyndaðu þér til dæmis að þú sért með reikning upp á 1000 Bandaríkjadali, en notandinn slær handvirkt 1099-upphæð inn á reikninginn sem nemur 500 Bandaríkjadölum.

[![Færslur 1099-skatteyðublaðs: Merkir bæði Uppfæra allt og Endurreikna núverandi 1099-upphæðir](./media/faq-2020-yr-end-08.png)](./media/faq-2020-yr-end-08.png)

Þegar þetta er greitt verða 500 Bandaríkjadalir 1099-upphæðin sem verður greidd. Ef reglubundinn endurútreikningur er gerður mun kerfið breyta 1099-upphæðinni í 1000 Bandaríkjadali, sem er heildargreiðslan.

[![Færslur 1099-skatteyðublaðs: Eftir reglubundna 1099-keyrslu](./media/faq-2020-yr-end-09.png)](./media/faq-2020-yr-end-09.png)

## <a name="accounts-payable-1099--manually-create-1099-transactions"></a>Viðskiptaskuldir: 1099 – Stofna handvirkt 1099-færslur
Fyrirtæki gæti þurft að stofna 1099-færslur handvirkt sem ekki eru tengdar reikningi. Hægt er að bæta við handvirkum 1099-færslum með því að fara í **Viðskiptaskuldir > Reglubundin verk > 1099-skatteyðublað > Jöfnun lánardrottins á 1099-eyðublöðum**. Veljið hnappinn **Handvirkar 1099-færslur**. 

Handvirkt stofnaðar 1099-færslur eru ekki uppfærðar með ferlinu **Uppfæra allt** eða **Endurreikna núverandi 1099-upphæðir** í hjálparforritinu **Uppfæra 1099**.

## <a name="accounts-payable-1099--does-dynamics-365-finance-support-the-1096-form"></a>Viðskiptaskuldir: 1099 – Styður Dynamics 365 Finance 1096-eyðublaðið? 

Dynamics 365 Finance prentar ekki út eyðublaðið 1096 Annual Summary and Transmittal of US Information Returns.

## <a name="accounts-payable-1099--are-there-any-new-features-that-support-1099-reporting-for-public-sector"></a>Viðskiptaskuldir: 1099 – Eru til nýir eiginleikar sem styðja 1099 skýrslugerð fyrir opinbera geirann? 
Nýjum eiginleika fyrir opinbera geirann, **Uppfæra 1099-upplýsingar eftir aðallykli**, hefur verið bætt við, sem hægt er að virkja á vinnusvæðinu **Eiginleikastjórnun**. Þessi eiginleiki gerir kleift að tengja 1099-gildin fyrir lánardrottin eftir aðallyklinum í dreifingu á fjárhagsupphæð, frekar en eftir sjálfgefna lyklinum í lánardrottnafærslunni.

Frekari upplýsingar eru í [Setja upp lánardrottna fyrir skýrsluna 1099](../localizations/noam-usa-set-up-vndrs-1099-rprtg.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]