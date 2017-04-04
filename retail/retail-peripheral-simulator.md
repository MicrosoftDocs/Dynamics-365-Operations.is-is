---
title: "Jaðarbúnaði hermi smásölu"
description: "Þetta efnisatriði lýsir jaðarbúnaði hermi verkfæri sem er gefin upp með Microsoft Dynamics 365 aðgerða - Smásölu."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 266544
ms.assetid: 16f31e70-15fc-441e-9727-e6a31c3a48f5
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 42dc414ff2bb6359b47d89c3bd3c510e4258f816
ms.openlocfilehash: b2229466040351d8c2b9494b30b4c928651820b8
ms.lasthandoff: 03/31/2017


---

# <a name="retail-peripheral-simulator"></a>Jaðarbúnaði hermi smásölu

Þetta efnisatriði lýsir jaðarbúnaði hermi verkfæri sem er gefin upp með Microsoft Dynamics 365 aðgerða - Smásölu.

<a name="overview"></a>Yfirlit
--------

Microsoft Dynamics 365 aðgerða - jaðarbúnaði hermi Smásölu er verkfæri sem auðveldar notandanum að setja upp prófa og úrræðaleit jaðartæki sem eru notaðar í smásölu. Hægt er að nota jaðarbúnaði hermi auðvelda prófun jaðartæki smásölu og isolate úthreyfingar röðunarvandamál röng uppsetning eða malfunctioning tækið lyftara. Jaðarbúnaði hermi inniheldur biðlaraforrits forritið aðgerðir sýndarfyrirtækisins útgáfum tæki sem Dynamics 365 aðgerða - styður Smásölu. Hluti fyrir hverja sýndarfyrirtæki tækið sýnir tengslin á milli tækið og retail sölustaðnum (POS). Hægt er að nota hana til að veita inntak, sem gildir fyrir mismunandi aðstæður Sölustaðar. Jaðarbúnaði hermi styður tengslin á milli Sölustað og tæki eftirfarandi sýndarfyrirtæki:

-   **Prentari** – jaðarbúnaði hermir getur sýna innhreyfingar sem eru skilgreindar fyrir Sölustað.
-   **Birta línu** – hægt er að skilgreina virtual línuskjá til að birta verkþætti á efnislega línuskjár.
-   **Kortalesari (Kortalesara)** – hægt er að senda hermdar kortalesara tilvik Sölustað úr jaðarbúnaði hermi.
-   **Skúffu** – hægt er að herma efnislegt peningaskúffu.
-   **Skúffu 2** – með Því að setja upp önnur peningaskúffunni í jaðarbúnaði hermi, hægt er að herma aðstæður sem fela í sér einn afgreiðslukassa sem er með tvær virkar vaktir.
-   **Skanna** – sýndarfyrirtæki strikamerkjaskanni sem styður jaðarbúnaði hermi út strikamerki skönnun tilvik.
-   **Vigt** – sýndarfyrirtæki vigt gerir kleift að herma eftir samspil vigtuðu vörur með Sölustað.
-   **Persónuleg kenni (pin-NÚMER) talnaborð** – hægt er að herma pin-NÚMER takkaborð aðgerðir. **Athugasemd:** komið stuðning efnislegt pin-takkaborðinu gegnum tengilínu greiðslunnar.
-   **Sækja undirskrift** – jaðarbúnaði hermi inniheldur sýndarfyrirtæki undirskrift sækja tæki sem hægt er að setja upp kvaðningu um undirskriftir sem krafist er fyrir sumar greiðslumátar, eins og greiðslur frá viðskiptavini.

Einnig er hægt að nota jaðarbúnaði hermi til að herma eftir lyklaborð kortalesara tilvik sem eiga að skanna strikamerki og Kortalesara. Sýndarfyrirtæki jaðarbúnaði hermi sérstaklega styður Tengingu Hlutar og Embedding fyrir Retail POS (OPOS) tæki.

## <a name="key-scenarios"></a>Lykill aðstæður
### <a name="troubleshooting"></a>Úrræðaleit

Hægt er að nota jaðarbúnaði hermi til að leita úrræða uppsetningu tækis. Ef ekki jaðarbúnaði hermi eða öðru tæki sama klasa, getur verið erfitt að ákvarða þar sem vandamál stafa. Hins vegar þegar jaðarbúnaði hermi er hægt er að setja upp sýndarfyrirtæki tæki, og keyra slóðir sama kóða og viðskiptagrunninn sem eru notuð fyrir efnislegar tæki. Megin munurinn á sýndarfyrirtæki tæki og efnislegt tæki er þjónustuhlut eða bílstjóra tæki frá jaðarbúnaði hermi. Fyrir efnislegar tæki þjónustuhlutinn ákvarðast af framleiðanda tækis. Með gagnstætt fyrir jaðarbúnaði hermi þjónustuhlutina fylgja með sem hluti af jaðarbúnaði hermi. Þegar jaðarbúnaði hermi er að vinna rétt, ef tæki ekki að vinna rétt eftir tækjaheiti vélbúnaðarreglunni er breytt í heiti raunverulegum tækis, er hægt gera ráð fyrir að sé vandamál með þjónustuhlutnum sem framleiðanda látið í té.

### <a name="training"></a>Nám

Hægt er að nota jaðarbúnaði hermi til að bæta realistic lag sem gjaldkera þjálfun þegar efnislegar vélbúnaður uppsetningu er ekki tiltæk. Þegar jaðarbúnaði hermi er höfð með í þjálfun aðstæður gjaldkeri getur áhrifaríkari samskipti við Sölustaðnum eftir útvegar ílag svo afurð strikamerkis skannana sem kóða og gjafakorts swipes kort og eftir fylgjast hvaða kvittanir eru prentaðar fyrir tiltekna færslu.

### <a name="testing"></a>Prófun

Hægt er að nota jaðarbúnaði hermi til að prófa afurðastrikamerkja kvittana og svo framvegis, án þess að þurfa að virkja efnislegt vélbúnaðarreglu í sýndarfyrirtæki. Þar sem efnislegt vélbúnaðar er ekki krafist og þarf ekki að virkja vélbúnaðarstöð eða efnisleg tölvu biðlara Sölustaðar, er hægt að fljótlegri hátt prófun breytingar sem gerðar eru í bakskrifstofunnar hvað varðar.

## <a name="set-up-the-peripheral-simulator"></a>Setja upp jaðarbúnaði útblásturs
### <a name="set-up-a-hardware-profile"></a>Setja upp vélbúnaðarreglu

1.  Til að setja upp jaðarbúnaði hermi, farið **Smásölu og commerce**&gt;**Rásar uppsetningu**&gt;**uppsetning Smásölustaðar**&gt;**POS forstillingar**&gt;**vélbúnaðarreglur**.
2.  Til að stofna nýja forstillingu er smellt á **Nýtt**.
3.  Færið inn gildi í á **Reglunúmer** og **Lýsing** svæði.
4.  Eftirfarandi tafla er notuð til að setja upp sýndarfyrirtæki tæki sem þarf að prófa. Hér er skýringu á dálkum í töflunni:
    -   **Tækið** – Þessum dálki gefur heiti FastTab sem útvíkka til að setja upp tækið.
    -   **Gerð tækis** – Þessum dálki gefur gildið sem er valið í svæðinu sem er merkt með nafn tækis.
    -   **Heiti tækis** – Þessum dálki gefur nákvæmt gildið sem er fært inn heiti tækis. **Mikilvægt:** heiti tækis sem hér eru gefnar krafist er, þar sem retail hardware station notar þessi tiltekna nöfn að aðsetur tæki. Ef ekki er að nota þessi tiltekna nöfn, tækið ekki hægt að nota.

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

**Athugasemd:** Engar uppsetning vélbúnaðarreglunni er krafist til að herma eftir lyklaborð kortalesara tilvika úr skanna strikamerki og Kortalesara.

### <a name="assign-the-hardware-profile-to-a-register"></a>Úthluta vélbúnaðarregluna afgreiðslukassa

1.  Eftir vélbúnaðarregluna stofnast fara **Smásölu og commerce**&gt;**Rásar uppsetningu**&gt;**uppsetning Smásölustaðar**&gt;**Skráir**.
2.  Í á **afgreiðslukassar** skal smella á tengil á **númer Afgreiðslukassa** fyrir skrá sem á að nota jaðarbúnaði hermi.
3.  Smellið á **Breyta**.
4.  Í á **Forstillingar**, í hlutanum við **vélbúnaðarreglu** skal velja vélbúnaðarreglu sem stofnaður var fyrir sýndarfyrirtæki jaðartæki.
5.  Click **Save**.

### <a name="synchronize-changes-to-the-channel-database"></a>Samstilla breytingar á gagnagrunni rásar

1.  Fara í **Smásölu og commerce**&gt;**Retail ÞAÐ**&gt;**dreifingaráætlun**.
2.  Velja skal **1090** dreifingaráætlun.
3.  Smellið á **Keyra nú** til að samstilla breytingar á Sölustað.

Eftir að gögn eru samstillt nýja forstillingu vélbúnaðar og breytingar á afgreiðslukassanum eru tiltækar í gagnagrunni rásar.

## <a name="install-the-peripheral-simulator"></a>Setja upp jaðarbúnaði útblásturs
1.  Fara í **Smásölu og commerce**&gt;**Rásar uppsetningu**&gt;**uppsetning Smásölustaðar**&gt;**POS forstillingar**&gt;**vélbúnaðarreglur**.
2.  Smellið á **Sækja**, og smellið síðan á **PeripheralSimulator**. **Athugasemd:** slökkva þarf á sprettiglugga áður en hægt er að sækja jaðarbúnaði hermi.
3.  Opna eftir niðurhalið er lokið er við **hleður Niður** möppu og tvísmellið **VirtualPeripherals.msi** til að ræsa uppsetningarforritið.
4.  Setja upp jaðarbúnaði hermi með því að nota sjálfgefnar stillingarnar.

Auk jaðarbúnaði hermi verður að setja upp common control hlutir úr Monroe Aðstoðar Þjónustu. Annars jaðarbúnaði hermi ekki að vinna rétt. Sækja common control hlutir, að fara í <http://monroecs.com/oposccos_current.htm>.

## <a name="using-the-peripheral-simulator"></a>Með því að nota jaðarbúnaði útblásturs
Til að hefja jaðarbúnaði hermi, smellið á **Ræsa** á tölvunni, gerð **Retail jaðarbúnaði hermi**, og veljið síðan forritið þegar hún birtist í leitarniðurstöðum. Eftir jaðarbúnaði hermi, byrja á tækjaheiti til að sjá studd tæki. Þessar tæki verða þau skráð sem flipar á vinstri hlið gluggans. Til að skoða tiltekna tækis, smellið á flipann til að tækið.

### <a name="line-display-capabilities"></a>Birta getu línu

Línuskjá er tækið sem kemur fram í jaðarbúnaði hermi. Þegar sýndarfyrirtæki línuskjá er skilgreind, hún sýnir atriði eins og þeir eru að skanna í færslu á Sölustað. Auk línuatriði, sem birta sýnir heildarupphæð sem er þegar valinn er á greiðslumáta á Sölustað. Hún sýnir líka stöðu sem gjaldfellur ef greiðslumáta er færð inn en staða er enn gjalddaga fyrir færslu. Þegar Sölustaðnum er ekki notuð getur boð til að tilgreina í útliti afgreiðsluskjás er lokað. Skilgreina verður skilaboð í í **Línu birta** FastTab í vélbúnaðarreglu.

### <a name="cash-drawer-capabilities"></a>Reiðufé skúffu getu

Peningaskúffu er önnur tæki sem kemur fram í jaðarbúnaði hermi. Þegar vélbúnaðarregluna skilgreind sem nota á sýndarfyrirtæki peningaskúffur Sölustaðnum opnar peningaskúffu fyrir virka vakt svar skúffu aðgerðir eins og talning skiptimyntar, og þannig að gjaldkeri geti gert breytt eða innborgunar reiðufé við staðlaða cash-and-carry færslur. Sýndarfyrirtæki peningaskúffur hafa merkin **Aðal skúffu** og **Aukaáherslu skúffu**. Þessar merki tákna Skúffu og Útgefanda 2 í vélbúnaðarreglu, bilsins. Þegar í skúffu er lokað, birtist mynd af lokuðum peningaskúffu og hnappinn á lokuðu peningaskúffunni er merktur **Opna skúffu**. Ef smellt er á þennan hnapp myndina skipt með mynd opna peningaskúffunni til að tilgreina skúffan er nú opin. Á hnapp á opna peningaskúffuna er merktur **Loka skúffu**. Margar aðgerðir á Sölustað getur valdið peningaskúffunni til að opna. Flest aðgerðir getur ekki haldið áfram meðan peningaskúffu er opin. Undantekningar eru sum ferlin lok vinnudags. Ef villuskilaboð birtast sem tilgreinir ekki er hægt að framkvæma aðgerð meðan peningaskúffu er opin fær notandinn Sölustaðar, notandi verður að loka sýndarfyrirtæki eða efnisleg peningaskúffunni til að halda áfram. Ef merkt er við peningaskúffu sem **Samnýttum** í forstillingu vélbúnaðar kerfið ekki staðfesta skúffan er lokað fyrir aðgerð. Aðgerðin eftirspurnarinnar fer svo eins og venjulega og jafnvel þótt peningaskúffu er opin. Þessi hegðun styður aðstæður þar sem peningaskúffur eru samnýttar á milli sölu tengir og einn tengja notar peningaskúffu meðan annarri tengja framkvæmir ótengd verkefni á sínar POS-tæki. Breytingar sem gerðar eru á peningaskúffunni ekki eru kostnaðarjafnaðar evident þar til núverandi vakt lokað og nýja vakt er opin.

### <a name="msr-capabilities"></a>Kortalesari getu

Jaðarbúnaði hermi veitir traust stuðning fyrir sýndarfyrirtæki Kortalesara aðgerðir með því að vinna í ham fyrir OPOS eða lyklaborð kortalesara ham. OPOS-ham krefst Kortalesara að skilgreina í vélbúnaðarreglu að gegna OPOS tækis. Lyklaborð kortalesara ham rétt sendir lyklaborð kortalesara gögn tilvik Microsoft Windows. Mismunur í uppsetningu, auk mismunandi OPOS- og lyklaborði afhendingarmáta kortalesara út á eftirfarandi hátt:

-   Biðlara Sölustaðar gerir OPOS-Kortalesari tæki fyrir tiltekna dæmi, eins og aðstæður sem leyfa kortalesara gögn fyrir vildarkort eða kort færslu gjafakorts.
-   Lyklaborð kortalesara ham jaðarbúnaði hermi sendir gögn kortalesara lyklaborð svæðið sem er virk þegar gögn eru send. Þessi hegðun svipar hegðun á sér stað ef gögnum er færð inn með því að nota með lyklaborði. Notandinn sem nota á Kortalesara sem lyklaborðið kortalesara verður að skipta á Retail Modern POS (MPOS) til að tryggja að gögn er móttekin í svæðinu rétt. Þess vegna er hægt að skilgreina seinkun, þannig að notandi hafi tíma til að ganga úr skugga um að sem gögn verða send til að leiðrétta svæðið.

#### <a name="testing-gift-and-payment-card-swipes"></a>Prófa swipes gjafakorts og greiðslu korts

Sýndarfyrirtæki Kortalesara jaðarbúnaði hermi gefur einnig er hægt að skilgreina tiltekin Kortalesara gögn til að prófa aðstæður fyrir swipes gjafakorts og greiðslu korts. Til að stofna kort er smellt á plúsmerkið (**+**), og veljið tegund korts. Tilgreina kortanúmer síðan eða rekja gagna sem á að senda POS ásamt gildistíma mánuð og ár fyrir spjaldið sem verið er að skilgreina. Gildið sem valið er í á **Tegund korts** svæði er einungis merki sem er hægt að varpa á spjald. Þetta merki auðveldar að auðkenna spjöld þegar þeir sem eru var lesið gegnum jaðarbúnaði hermi. Hægt er að velja kort sem hafa verið skilgreindir í jaðarbúnaði hermi með vinstri örina (**&lt;**) og hægri örina (**&gt;**) hnapparnir hér fyrir ofan mynd af kortinu. Hægt er að breyta og eyða spjöld með því að nota í **Breyta** og **Eyða** hnappana við hliðina á plúsmerkið (**+**) hnappinn.

### <a name="pin-pad"></a>PIN-takkaborð

Hægt er að skilgreina takkaborð hermi pin-NÚMER til að herma eftir að OPOS pin-takkaborðinu. Þegar færsla sem kortamillifærslur millifærslu (EFT) er framkvæmd á Sölustaðnum og krefst færslu pin-NÚMER, símtala retail hardware station tækið pin-NÚMER til að biðja um skráningu pin-NÚMER. Pin-takkaborð í jaðarbúnaði hermi krefst EFT greiðslu connector stuðning virki.

### <a name="printer"></a>Prentari

Sýndarfyrirtæki jaðarbúnaði prentara sýnir aðeins innhreyfingar sem þær eru prentaðar frá. Ef prenta aðgerð framleiðir margar innhreyfingar, er hægt að fletta gegnum innhreyfingar.

#### <a name="configure-receipt-printing"></a>Skilgreina prentun á kvittun

1.  Fara í **Smásölu og commerce**&gt;**Rásar uppsetningu**&gt;**uppsetning Smásölustaðar**&gt;**POS forstillingar**&gt;**vélbúnaðarreglur**.
2.  Veljið vélbúnaðarregluna sem þú stofnaðir fyrir sýndarfyrirtæki jaðartæki.
3.  Á við **Prentara** FastTab, smellið á **Breyta**.
4.  Í því **Kenni kvittunarforstillingar** skal velja forstillingu kvittunar.
5.  Click **Save**.

### <a name="scale"></a>Vigt

Þegar vigtuð afurð er bætt við færslu á Sölustað og vigt er skilgreind sækir Sölustaðnum þyngd frá vigtinni. Fyrir bæði efnislegt og sýndarfyrirtæki kvarðann, afurð eða þyngd ætti að tilgreina áður en varan er bætt við færsluna. Áður en vigtuð afurð er bætt við færsluna, fara vigt í jaðarbúnaði hermi og nota á plúsmerkið (**+**) og mínustáknið (**–**) hnappana til að leiðrétta þyngd kvarðann á skýrsluna. Einnig er hægt að færa inn æskileg vægi beint í í **Núverandi gildi** svæði. Hægt er að leiðrétta einingum fyrir þyngd á vigt fyrir með því að nota á plúsmerkið (**+**), **Breyta**, og **Eyða** hnappa. Á þennan hátt er einingum er hægt að tilgreina samkvæmt afurðir sem eru vegið eða staðinn þar sem það kvarði sé notaður.

#### <a name="configure-a-scale-product"></a>Skilgreina vigtuð afurð

1.  Fara í **Smásölu og****commerce**&gt;**Afurðir og tegundir**&gt;**Losaðar afurðir eftir flokki**.
2.  Opna afurð færslu.
3.  Velja afurðar til vigta.
4.  Á við **Retail** FastTab, setja í **Vigtuð afurð** valkosturinn úr **Nei** til **Já**.

#### <a name="synchronize-changes-to-the-channel-database"></a>Samstilla breytingar á gagnagrunni rásar

1.  Fara í **Smásölu og commerce**&gt;**Retail ÞAÐ**&gt;**dreifingaráætlun**.
2.  Velja skal **1040** dreifingaráætlun.
3.  Smellið á **Keyra nú** til að samstilla breytingar á Sölustað.

Eftir að gögnin samstillt þegar vigtuð afurð er bætt við færsluna Sölustaðar, á POS kannar kvarðann fyrir þyngd.

### <a name="signature-capture"></a>Sækja undirskrift

Sýndarfyrirtæki undirskrift fanga minnir notanda til að veita undirskrift á takkaborð fanga sýndarfyrirtæki undirskriftar þegar greiðslumátinn sem notaður er krefst undirskriftar. Getur notandi samþykkt undirskrift til að sýna það á Sölustaðnum. Gjaldkeri getur síðan samþykkja undirskrift. Undirskriftin er þá vista með greiðslumáta og samstillt bakskrifstofu ásamt öðrum færslugögn.

#### <a name="set-up-a-tender-to-require-a-signature"></a>Setja upp greiðslumáta til að krefjast undirskriftar

1.  Fara í **Smásölu og commerce**&gt;**Rásir**&gt;**Smásöluverslanir**&gt;**Allar smásöluverslanir**.
2.  Veljið smásöluverslunar.
3.  Smellið á **Breyta**.
4.  Smellið á **Setja upp**, og síðan, í í **Uppsetning** er smellt á **greiðsluhætti**.
5.  Smellið á **Breyta**.
6.  Veljið greiðslumáta sem krefst undirskriftar.
7.  Í á **Almennt** undir hlutanum **Sækja Undirskrift**, stilla á **Nota sækja undirskrift** valkosturinn að **Já**.
8.  Í því **lágmarksupphæð sækja Undirskrift** svæðinu, færið inn lágmarksupphæð sem ætti að kveikja sækja undirskrift.

#### <a name="synchronize-changes-to-the-channel-database"></a>Samstilla breytingar á gagnagrunni rásar

1.  Fara í **Smásölu og commerce**&gt;**Retail ÞAÐ**&gt;**dreifingaráætlun**.
2.  Velja skal **1070** dreifingaráætlun.
3.  Smellið á **Keyra nú** til að samstilla breytingar á Sölustað.

Eftir að gögnin samstillt þegar greiðslumáta er notað sem þarfnast undirskriftar og upphæð fjármögnunarþröskuldi undirskrift, Sölustaðnum biður fyrir undirskriftar sýndarfyrirtæki sækja undirskrift.

## <a name="additional-configuration"></a>Frekari skilgreiningu
Hægt er að breyta skilgreiningarskrá jaðarbúnaði hermi til fleiri hæfilega aðseturs áætlunum sem verið er að prófa. Hægt er að finna skilgreiningarskrá á C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\VirtualPeripherals\\Microsoft.Dynamics.Commerce.VirtualPeripherals.Client.exe.config. Skilgreiningarskránni skilgreinir einingarnar sem eru tiltækar fyrir prófun á vigtina kortategundir sem eru tiltækar fyrir prófun og strikamerkjagerðir. Til dæmis eftir textagildi í skilgreiningarskránni er breytt, er hægt að bæta nýja kortategund eða mælieiningu sem hægt er að velja í keyrslutíma. Nýju gildin sem birtast þegar forritið er endurræst.

## <a name="troubleshooting"></a>Úrræðaleit
Verkþættir fyrir jaðarbúnaði hermi séu skráðar innan jaðarbúnaði hermi. Hægt er að finna í kladdaskrá í C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\VirtualPeripherals\\Microsoft.Dynamics.Commerce.VirtualPeripherals.Client.exe.config. Jaðarbúnaði hermi skýrslur einnig úthreyfingar tilvikakladda Windows sem hægt er að fara á **Hugbúnaðar og Þjónustu Kladda**&gt;**Microsoft**&gt;**DynamicsAX**. Ef breytingar sem gerðar voru vélbúnaðarregluna eða öðrum svæðum ekki eru kostnaðarjafnaðar evident þegar MPOS eða jaðarbúnaði hermi, athuga verkraðara dreifingu sem er notuð til að samstilla gögn í gagnagrunn rásar. Ef breytingar voru samstilltar en enn ekki eru kostnaðarjafnaðar evident á Sölustað, endurræsa biðlara Sölustaðar. Breytingar á skilgreindu peningaskúffur ekki eru kostnaðarjafnaðar gildi fyrr en ný vakt er stofnuð. Þess vegna ef breytingar eru gerðar á peningaskúffur gangið úr skugga um að alltaf vaktinni er lokað fyrirliggjandi til að prófa nýja uppsetningu skúffu reiðufé. Stundum ef bílstjóra framleiðanda vörunnar er sett upp eftir common control hlutir þjónustum Monroe Aðstoðar ökumaðurinn getur valdið common control hlutir að stöðva vinna rétt. Í þessu tilfelli ætti að setja common control hlutir.

<a name="see-also"></a>Sjá einnig
--------

[Retail peripherals overview](retail-peripherals-overview.md)


