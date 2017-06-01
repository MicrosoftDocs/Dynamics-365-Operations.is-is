---
title: "Jaðarbúnaðarhermir smásölu"
description: "Þessi grein lýsir verkfærinu jaðarbúnaðarhermi smásölu sem er veitt með Dynamics 365 for Operations - Retail."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 266544
ms.assetid: 16f31e70-15fc-441e-9727-e6a31c3a48f5
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 894aaaaa844447030dae73826d326f99366aa068
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017


---

# <a name="retail-peripheral-simulator"></a>Jaðarbúnaðarhermir smásölu

[!include[banner](includes/banner.md)]


Þessi grein lýsir verkfærinu jaðarbúnaðarhermi smásölu sem er veitt með Dynamics 365 for Operations - Retail.

<a name="overview"></a>Yfirlit
--------

Microsoft Dynamics 365 for Operations - Jaðarbúnaðarhermir smásölu er verkfæri sem auðveldar notandanum að setja upp, prófa og úrræðaleita jaðartæki sem eru notuð í smásölu. Hægt er að nota jaðarbúnaðarhermi til að einfalda prófun á jaðartæki smásölu og einangra vandamál sem orsakast af rangri uppsetningu eða bilun í tækisreklum. Jaðarbúnaðarhermir inniheldur skjáborðsforritið sem er með sýndarútgáfum af tækjum sem Dynamics 365 for Operations - Retail styður. Hluti fyrir hverja sýndartæki sýnir tengslin á milli tækið og sölustaðnum smásölu (POS). Einnig er hægt að nota hann til að veita inntak, sem gildir fyrir mismunandi aðstæður í POS. Jaðarbúnaðarhermir styður samskipti á milli POS og eftirfarandi sýndartækja:

-   **Prentari** – Jaðarbúnaðarhermir getur sýna kvittanir sem eru skilgreindar fyrir POS-prentara.
-   **Birta línu** – Hægt er að skilgreina sýndarlínuskjá til að birta verkþætti á efnislega línuskjár.
-   **Kortalesari (MSR)** – Hægt er að senda hermdar kortalesaratilvik í POS úr jaðarbúnaðarhermi.
-   **Skúffu** – Hægt er að herma efnislegt peningaskúffu.
-   **Skúffu 2** – með því að setja upp aðra peningaskúffu í jaðarbúnaðarhermi er hægt að herma aðstæður sem fela í sér einn afgreiðslukassa sem er með tvær virkar vaktir.
-   **Skanna** – Sýndarstrikamerkjaskanni sem styður jaðarbúnaðarhermi getur gefið út skönnunartilvik strikamerkja.
-   **Vigt** – Sýndarvigt gerir kleift að herma eftir samspil vigtuðu vörur við POS.
-   **Persónulegt auðkennisnúmer (PIN-takkaborð)** – Hægt er að herma eftir aðgerðum PIN-takkaborðs. **Athugasemd:** Koma verður á stuðningi við efnislegt pin-takkaborðinu gegnum tengilínu greiðslunnar.
-   **Sækja undirskrift** – jaðarbúnaðarhermir inniheldur sýndarundirskriftatæki þar sem hægt er að setja upp kvaðningu um undirskriftir sem krafist er fyrir sumar greiðslumátar, eins og greiðslur frá viðskiptavini.

Einnig er hægt að nota jaðarbúnaðarhermi til að herma eftir lyklaborði kortalesara tilvik sem eiga að skanna strikamerki og Kortalesara. Sýndarjaðarbúnaðarhermirinn styður sérstaklega Tengingu Hlutar og Embedding fyrir Retail POS (OPOS) tæki.

## <a name="key-scenarios"></a>Lykilsviðsmyndir
### <a name="troubleshooting"></a>Úrræðaleit

Hægt er að nota jaðarbúnaðarhermi til að leita úrræða við uppsetningu tækis. Ef þú ert ekki með jaðarbúnaðarhermi eða annað tæki í sama klasa, getur verið erfitt að ákvarða hvaðan vandamál stafa. Hins vegar þegar þú ert með jaðarbúnaðarhermi er hægt er að setja upp sýndartæki, og keyra sömu slóðir kóða og viðskiptagrunninn sem eru notuð fyrir efnislegar tæki. Frá sjónarhóli jaðarbúnaðarhermis er meginmunurinn á sýndartæki og efnislegu tæki er þjónustuhlut eða tækisrekill. Fyrir efnisleg tæki ákvarðast þjónustuhlutur af framleiðanda tækis. Aftur á móti fyrir jaðarbúnaðarhermi fylgja þjónustuhlutir með sem hluti af jaðarbúnaðarhermi. Þegar jaðarbúnaðarhermir er að vinna rétt, ef tæki virkar ekki rétt eftir tækjaheiti vélbúnaðarreglunni er breytt í heiti raunverulegum tækis, er hægt gera ráð fyrir að sé vandamál með þjónustuhlutnum sem framleiðanda látið í té.

### <a name="training"></a>Nám

Hægt er að nota jaðarbúnaðarhermi til að bæta raunhæft lag við gjaldkeraþjálfun þegar efnislegar vélbúnaður uppsetningu er ekki tiltæk. Þegar jaðarbúnaðarhermir er innifalinn í þjálfunaraðstæður getur gjaldkeri átt skilvirkari samskipti við POS með því að veita ílag eins og skönnun strikamerkis afurðar og lestur gjafakorta og með því að fylgjast með hvaða kvittanir eru prentaðar fyrir tiltekna færslu.

### <a name="testing"></a>Prófun

Hægt er að nota jaðarbúnaðarhermi til að prófa afurðastrikamerki, kvittanasnið og svo framvegis, án þess að þurfa að virkja efnislega vélbúnaðarreglu í sýndarfyrirtæki. Þar sem efnislegs vélbúnaðar er ekki krafist og þarf ekki að virkja vélbúnaðarstöð eða POS-biðlara á efnisleg tölvu er hægt að fljótlegri hátt prófun breytingar sem gerðar eru í bakskrifstofunnar hvað varðar.

## <a name="set-up-the-peripheral-simulator"></a>Uppsetning jaðarbúnaðarhermis
### <a name="set-up-a-hardware-profile"></a>Setja upp vélbúnaðarreglu

1.  Til að setja upp jaðarbúnaðarhermi skal fara í **Smásala og viðskipti** &gt; **Uppsetning rásar** &gt; **Uppsetning sölustaðar** &gt; **Forstillingar sölustaðar** &gt; **Vélbúnaðarreglur**.
2.  Smelltu á **Nýtt** til að stofna nýja forstillingu.
3.  Skráið gildi í svæðunum **Númer forstillingar** og **lýsing**.
4.  Eftirfarandi tafla er notuð til að setja upp sýndartæki sem þarf að prófa. Hér er skýring á dálkum í töflunni:
    -   **Tækið** – Þessum dálki gefur heiti flýtiflipa sem útvíkka til að setja upp tækið.
    -   **Gerð tækis** – Þessum dálki gefur gildið sem er valið í svæðinu sem er merkt með nafn tækis.
    -   **Heiti tækis** – Þessum dálki gefur nákvæmt gildið sem er fært inn heiti tækis. **Mikilvægt:** heiti tækis sem hér eru gefnar krafist er, þar sem vélbúnaðarstöðin notar þessi tilteknu heiti að aðsetur tæki. Ef þessi tilgreindu heiti eru ekki notuð er ekki hægt að nota tækið.

    | Tæki            | Gerð tækis | Nafn tækis              |
    |-------------------|-------------|--------------------------|
    | Prentari           | OPOS        | MockOPOSPrinter          |
    | Línuskjár      | OPOS        | MockOPOSLineDisplay      |
    | Kortalesari               | OPOS        | MockOPOSMSR              |
    | Útgefandi            | OPOS        | MockOPOSDrawer1          |
    | Drawer2           | OPOS        | MockOPOSDrawers          |
    | Skanni           | OPOS        | MockOPOSScanner          |
    | Vigt             | OPOS        | MockOPOSScale            |
    | PIN-takkaborð           | OPOS        | MockOPOSPinPad           |
    | Sækja undirskrift | OPOS        | MockOPOSSignatureCapture |

**Athugasemd:** Ekki er þörf á sérstakri uppsetningu vélbúnaðarreglu til að herma eftir kortalesaratilvikum úr strikamerkjaskanna og Kortalesara.

### <a name="assign-the-hardware-profile-to-a-register"></a>Tengið vélbúnaðarreglu við afgreiðslukassa

1.  Eftir að vélbúnaðarreglan er stofnuð skal fara í **Smásölu og viðskipti**&gt;**Rásar uppsetningu**&gt;**uppsetning Smásölustaðar**&gt;**Skráir**.
2.  Í listanum **afgreiðslukassar** skal smella á tengil í svæðinu **númer Afgreiðslukassa** fyrir skrá sem á að nota jaðarbúnaðarhermi.
3.  Smellið á **Breyta**.
4.  Í hlutanum **Forstillingar**, í svæðinu **vélbúnaðarreglu** skal velja vélbúnaðarreglu sem stofnaður var fyrir sýndarjaðartæki.
5.  Smellið á **Vista**.

### <a name="synchronize-changes-to-the-channel-database"></a>Samstilla breytingar við gagnagrunn rásar

1.  Fara í **Smásölu og viðskipti** &gt; **upplýsingatækni í smásölu** &gt; **dreifingaráætlun**.
2.  Velja dreifingaráætlun **1090**.
3.  Smelltu á **Keyra nú** til að samstilla breytingar við POS.

Eftir að gögn eru samstillt eru ný forstillingu vélbúnaðar og breytingar á afgreiðslukassanum tiltækar í gagnagrunni rásar.

## <a name="install-the-peripheral-simulator"></a>Setja upp jaðarbúnaðarhermi
1.  Farðu í **Smásala og viðskipti** &gt; **Uppsetningu rásar** &gt; **Uppsetning POS** &gt; **Forstillingar POS** &gt; **Vélbúnaðarreglur**.
2.  Smellið á **Sækja**, og smellið síðan á **PeripheralSimulator**. **Athugasemd:** slökkva þarf á sprettiglugga áður en hægt er að sækja jaðarbúnaðarhermi.
3.  Eftir að niðurhali er lokið skal opna möppuna **Hlaða niður** og tvísmellið á **VirtualPeripherals.msi** til að ræsa uppsetningarforritið.
4.  Setja upp jaðarbúnaðarhermi með því að nota sjálfgefnar stillingarnar.

Auk jaðarbúnaðarhermis verður að setja upp almenna stýrihluti frá Monroe Consulting Services. Annars er jaðarbúnaðarhermir ekki að vinna rétt. Til að sækja almenna stýrihlutir þarf að fara í <http://monroecs.com/oposccos_current.htm>.

## <a name="using-the-peripheral-simulator"></a>Notkun jaðarbúnaðarhermis
Til að hefja jaðarbúnaðarhermi, smellið á **Ræsa** á tölvunni, ritið **Jaðarbúnaðarhermir smásölu**, og veljið síðan forritið þegar það birtist í leitarniðurstöðum. Eftir að jaðarbúnaðarhermir er ræstur er smellt á tækjaheiti til að sjá studd tæki. Þessar tæki verða skráð sem flipar á vinstri hlið gluggans. Til að skoða tiltekið tæki, smellið á flipann fyrir það tæki.

### <a name="line-display-capabilities"></a>Geta línubirtingar

Línubirting er fyrsta tækið sem kemur fram í jaðarbúnaðarhermi. Þegar sýndarlínuskjár er skilgreindur sýnir hann vörur eins og þær eru skannaðar í færslu í POS. Auk línuatriði, sýnir skjárinn heildarupphæð sem er þegar valinn er á greiðslumáta í POS. Hann sýnir líka stöðu sem gjaldfellur ef greiðslumáta er færð inn en staða er enn gjalddaga fyrir færslu. Þegar POS er ekki notuð er hægt að birta skilaboð til að tilgreina að skúffan sé lokað. Skilgreina verður skilaboð í flýtiflipanum **Línu birta** í vélbúnaðarreglu.

### <a name="cash-drawer-capabilities"></a>Geta peningaskúffu

Peningaskúffa er annað tækið sem kemur fram í jaðarbúnaðarhermi. Þegar vélbúnaðarreglan er skilgreind til að sýndarpeningaskúffur opnar POS peningaskúffu fyrir virka vakt sem svar skúffuaðgerðir eins og talning skiptimyntar, svo að gjaldkeri geti gefið til baka eða innborgunar reiðufé við staðlaða reiðufjárfærslur. Sýndarpeningaskúffur hafa merkin **Aðalskúffa** og **Aukaskúffa**. Þessar merki tákna Skúffu og Skúffu 2 í vélbúnaðarreglu, í þeirri röð. Þegar skúffu er lokað, birtist mynd af lokuðum peningaskúffu og hnappinn á lokuðu peningaskúffunni er merktur **Opna skúffu**. Ef smellt er á þennan hnapp er myndina skipt út fyrir mynd af opna peningaskúffunni til að tilgreina skúffan er nú opin. Hnappurinn á opna peningaskúffuna er merktur **Loka skúffu**. Margar aðgerðir í POS getur valdið því að peningaskúffunni opnast. Flest aðgerðir getur ekki haldið áfram meðan peningaskúffu er opin. Undantekningar eru sum ferli í lok vinnudags. Ef villuskilaboð birtast notanda sem tilgreina a ekki er hægt að framkvæma aðgerð meðan peningaskúffa er opin þarf notandinn að loka sýndar- eða efnislegri peningaskúffu til að halda áfram. Ef merkt er við peningaskúffu sem **Samnýttum** í forstillingu vélbúnaðar staðfestir kerfið ekki að skúffan er lokað á undan aðgerð. Aðgerðin heldur áfram eins og venjulega og jafnvel þótt peningaskúffu er opin. Þessi hegðun styður aðstæður þar sem peningaskúffur eru samnýttar á milli sölu tengir og einn starfsmaður notar peningaskúffu meðan annarri starfsmaður framkvæmir ótengd verkefni á sitt POS-tæki. Breytingar sem gerðar eru á peningaskúffunni eru ekki augljósar fyrr en núverandi vakt er lokið og nýja vakt er opin.

### <a name="msr-capabilities"></a>Geta kortalesara

Jaðarbúnaðarhermir veitir traustan stuðning fyrir sýndarkortalesara aðgerðir með því að vinna í ham fyrir OPOS eða lyklaborð kortalesara ham. OPOS-ham krefst að Kortalesara sé skilgreindur í vélbúnaðarreglu til að virka sem OPOS-tæki. Lyklaborð kortalesara ham rétt sendir lyklaborð kortalesara gögn tilvik til Microsoft Windows. Auk mismunar í uppsetningu eru stillingar OPOS- og lyklaborði kortalesara mismunandi á eftirfarandi hátt:

-   POS-biðlari gerir OPOS-Kortalesari tæki fyrir tiltekna dæmi, eins og aðstæður sem leyfa kortalesara gögn fyrir vildarkort eða kort færslu gjafakorts.
-   Í lyklaborð kortalesara ham sendir jaðarbúnaðarhermir gögn kortalesara á lyklaborðssvæðið sem er virkt þegar gögn eru send. Þessi hegðun svipar til hegðunar sem á sér stað ef gögn eru færð inn með því að nota lyklaborð. Notandinn sem nota á Kortalesara sem lyklaborðið kortalesara verður að skipta yfir í Retail Modern POS (MPOS) til að tryggja að gögn er móttekin í svæðinu rétt. Þess vegna er hægt að skilgreina seinkun, þannig að notandi hafi tíma til að ganga úr skugga um að sem gögn verða send til rétts svæðið.

#### <a name="testing-gift-and-payment-card-swipes"></a>Prófa greiðslukortalestur gjafakorts og greiðslukorts

Sýndarkortalesara jaðarbúnaðarhermir leyfir þér einnig að skilgreina tiltekin Kortalesaragögn til að prófa aðstæður fyrir greiðslukortalestur gjafakorts og greiðslu korts. Til að stofna kort er smellt á plúsmerkið (**+**), og veljið tegund korts. Tilgreina kortanúmer síðan eða rekja gögn sem á að senda POS ásamt gildistíma mánuð og ár fyrir spjaldið sem verið er að skilgreina. Gildið sem valið er í svæðinu **Tegund korts** er einungis merki sem er hægt að varpa á spjald. Þetta merki auðveldar að auðkenna kort þegar þau eru lesin gegnum jaðarbúnaðarhermi. Hægt er að velja kort sem hafa verið skilgreindir í jaðarbúnaðarhermi með vinstri örina (**&lt;**) og hægri örina (**&gt;**) hnapparnir hér fyrir ofan mynd af kortinu. Hægt er að breyta og eyða kortum með því að nota **Breyta** og **Eyða** hnappana við hliðina á plúsmerkið (**+**) hnappinn.

### <a name="pin-pad"></a>PIN-takkaborð

Hægt er að skilgreina PIN-takkaborðshermi til að herma eftir OPOS PIN-takkaborðinu. Þegar kortamillifærslur (EFT) er framkvæmd í POS og krafist er PIN-færslu, hringir vélbúnaðarstöðin í PIN-tækið til að biðja um skráningu pin-NÚMER. Til að virka krefst Pin-takkaborð í jaðarbúnaðarhermi stuðnings við EFT-greiðslutengi.

### <a name="printer"></a>Prentari

Sýndarjaðarbúnaði prentara sýnir aðeins kvittanir eins og þær eru prentaðar úr POS. Ef prentaðgerð framleiðir margar kvittanir, er hægt að fletta gegnum kvittanirnar.

#### <a name="configure-receipt-printing"></a>Grunnstilla kvittanaprentun

1.  Farðu í **Smásala og viðskipti** &gt; **Uppsetningu rásar** &gt; **Uppsetning POS** &gt; **Forstillingar POS** &gt; **Vélbúnaðarreglur**.
2.  Veljið vélbúnaðarregluna sem þú stofnaðir fyrir sýndarjaðartæki.
3.  Á flýtiflipanum **Prentara** smellið á **Breyta**.
4.  Í svæðinu **Kenni kvittunarforstillingar** skal velja forstillingu kvittunar.
5.  Smellið á **Vista**.

### <a name="scale"></a>Vigt

Þegar vigtaðri afurð er bætt við færslu í POS og vigt er skilgreind sækir POS þyngd frá vigtinni. Fyrir bæði efnislegt og sýndarvigt ætti að tilgreina afurð eða þyngd áður en varan er bætt við færsluna. Áður en vigtaðri afurð er bætt við færsluna, skal fara í vigt í jaðarbúnaðarhermi og nota plúsmerkið (**+**) og mínustáknið (**–**) hnappana til að leiðrétta þyngdina sem kvarðinn á að tilkynna. Einnig er hægt að færa inn æskilega vigt beint í svæðið **Núverandi gildi**. Hægt er að leiðrétta einingum fyrir þyngd á vigt fyrir með því að nota plúsmerkið (**+**), **Breyta**, og **Eyða** hnappa. Á þennan hátt er hægt að tilgreina einingar samkvæmt afurðum sem eru vigtaðar eða staðnum þar sem það kvarði er notaður.

#### <a name="configure-a-scale-product"></a>Grunnstilla vigtaða afurð

1.  Fara í **Smásölu og** **viðskipti** &gt; **Afurðir og tegundir** &gt; **Losaðar afurðir eftir flokki**.
2.  Opna afurðarfærslu.
3.  Veljið afurð til að vigta.
4.  Á flýtiflipanum **Smásala** stilltu valkostinn **Vigtuð afurð** úr **Nei** í **Já**.

#### <a name="synchronize-changes-to-the-channel-database"></a>Samstilla breytingar við gagnagrunn rásar

1.  Fara í **Smásölu og viðskipti** &gt; **upplýsingatækni í smásölu** &gt; **dreifingaráætlun**.
2.  Veldu **1040** dreifingaráætlun.
3.  Smelltu á **Keyra nú** til að samstilla breytingar við POS.

Þegar vigtuð afurð er bætt við færslu í POS og vigt er skilgreind sækir POS þyngd frá vigtinni.

### <a name="signature-capture"></a>Sækja undirskrift

Sýndarundirskriftatæki biður notanda um að veita undirskrift á sýndarundirskriftarborði þegar greiðslumátinn sem notaður er krefst undirskriftar. Notandi getur samþykkt undirskrift til að sýna það í POS. Gjaldkeri getur síðan samþykkt undirskrift. Undirskriftin er þá vista með greiðslumáta og samstillt bakskrifstofu ásamt öðrum færslugögn.

#### <a name="set-up-a-tender-to-require-a-signature"></a>Setja upp greiðslumáta til að krefjast undirskriftar

1.  Fara í **Smásölu og viðskipti** &gt; **miðlunarleiðir** &gt;**smásöluverslanir** &gt; **allar smásöluverslanir**.
2.  Veljið smásöluverslun.
3.  Smellið á **Breyta**.
4.  Smellið á **Setja upp**, og síðan, í **Uppsetning** er smellt á **greiðsluhætti**.
5.  Smellið á **Breyta**.
6.  Veljið greiðslumáta sem krefst undirskriftar.
7.  Í hlutanum **Almennt** undir **Móttaka undirskriftar**, skal stilla valkostinn **Nota undirskriftartæki** á **Já**.
8.  Í svæðinu **Lágmarksupphæð undirskriftatækis** er færð inn lágmarksupphæð sem ætti að kveikja á að undirskrift sé sótt.

#### <a name="synchronize-changes-to-the-channel-database"></a>Samstilla breytingar við gagnagrunn rásar

1.  Fara í **Smásölu og viðskipti** &gt; **upplýsingatækni í smásölu** &gt; **dreifingaráætlun**.
2.  Veldu **1070** dreifingaráætlun.
3.  Smelltu á **Keyra nú** til að samstilla breytingar við POS.

Eftir að gögnin eru samstillt þegar greiðslumáta er notað sem þarfnast undirskriftar og upphæð fjármögnunarþröskuldi undirskrift, biður POS um undirskriftar í sýndaruundirskriftatækinu.

## <a name="additional-configuration"></a>Viðbótargrunnstillingar
Hægt er að breyta skilgreiningarskrá jaðarbúnaðarhermis svo að hún taki betur á þeim aðstæðum sem verið er að prófa. Hægt er að finna skilgreiningarskrá á C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\VirtualPeripherals\\Microsoft.Dynamics.Commerce.VirtualPeripherals.Client.exe.config. Skilgreiningarskránni skilgreinir einingarnar sem eru tiltækar fyrir prófun á vigtina kortategundir sem eru tiltækar fyrir prófun og strikamerkjagerðir. Til dæmis eftir textagildi í skilgreiningarskránni er breytt, er hægt að bæta nýja kortategund eða mælieiningu sem hægt er að velja í keyrslutíma. Nýju gildin sem birtast eftir að forritið er endurræst.

## <a name="troubleshooting"></a>Úrræðaleit
Verkþættir fyrir jaðarbúnaðarhermi eru skráðar innan jaðarbúnaðarhermis. Hægt er að finna atburðaskrána á C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\VirtualPeripherals\\Microsoft.Dynamics.Commerce.VirtualPeripherals.Client.exe.config. Jaðarbúnaðarhermir tilkynnir einnig vandamál í tilvikakladda Windows sem hægt er að fara á **Forrita- og þjónustukladdar** &gt; **Microsoft** &gt; **DynamicsAX**. Ef breytingar sem gerðar voru á vélbúnaðarreglunni eða öðrum svæðum eru ekki augljósar þegar MPOS eða jaðarbúnaðarhermir eru notuð, skal athuga verk verkraðaradreifingar sem er notuð til að samstilla gögn í gagnagrunn rásar. Ef breytingar voru samstilltar en eru ekki enn augljósar í POS, skal endurræsa POS-biðlara. Breytingar á skilgreindum peningaskúffum taka ekki gildi fyrr en ný vakt er stofnuð. Þess vegna ef breytingar eru gerðar á peningaskúffum skal ganga úr skugga um að fyrirliggjandi vakt sé alltaf lokað til að prófa nýja uppsetningu peningaskúffu. Stundum ef rekill framleiðanda vörunnar er settur upp eftir almennum stýrihlutum frá Monroe Consulting Services getur rekillinn valdið því að almennir stýrihlutir hætti að virka rétt. Í þessu tilfelli ætti að enduruppsetja almenna stýrihlutir.

<a name="see-also"></a>Sjá einnig
--------

[Yfirlit yfir jaðartæki smásölu](retail-peripherals-overview.md)




