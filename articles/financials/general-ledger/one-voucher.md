---
title: Eitt fylgiskjal
description: "Eitt fylgiskjal fyrir fjárhagsbækur (almenna færslubók, eignabók, greiðslubók lánardrottins, o.s.frv.) gerir þér kleift að slá inn margar undirbókarfærslur í tengslum við eitt fylgiskjal."
author: kweekley
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-03-16
ms.dyn365.ops.version: 8.0.2
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 9f996131830f9bd4efd534143b3fb761c5ccc756
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---

# <a name="one-voucher"></a>Eitt fylgiskjal

[!include [banner](../includes/banner.md)]

> [!NOTE]
>  Þessi virkni verður í boði í Dynamics 365 for Finance and Operations útgáfu 8.0, sem verður fáanleg í vorútgáfu '18.   

<a name="what-is-one-voucher"></a>Hvað er „Eitt fylgiskjal“?
======================

Núverandi virkni fyrir fjárhagsbækur (almenna færslubók, eignabók, greiðslubók lánardrottins, o.s.frv.) gerir þér kleift að slá inn margar undirbókarfærslur í tengslum við eitt fylgiskjal. Við vísum í þessa virkni sem „Eitt fylgiskjal.“ Hægt er að stofna eitt fylgiskjal með því að nota eina af eftirfarandi aðferðum:

-   Setjið upp færslubókarheitið (**Fjárhagur** \> **Uppsetning færslubókar** \>**Færslubókarheiti**) þannig að reiturinn **Nýtt fylgiskjal** sé stilltur á **Aðeins eitt fylgiskjalsnúmer**. * Sérhverri línu sem bætt er við færslubókina er nú að finna í sama fylgiskjalinu. Vegna þess að sérhverri línu er bætt við sama fylgiskjalið, er hægt að færa inn fylgiskjalið sem marglínu fylgiskjal, sem lykil/mótlykil í sömu línunni eða sem samsetningu.

[![Stök lína](./media/same-line.png)](./media/same-line.png)
 
> [!IMPORTANT] 
> *  Athugaðu að skilgreiningin á „Einu fylgiskjali“ inniheldur EKKI færslubókarheiti sem eru sett upp sem **Eitt fylgiskjalsnúmer** eingöngu og notandinn færir síðan inn fylgiskjal sem inniheldur eingöngu fjárhagslyklagerðir.  Í þessu skjali merkir „Eitt fylgiskjal“ að það sé eitt fylgiskjal sem inniheldur fleiri en einn lánardrottin, viðskiptavin, banka, eign eða verk. 

-   Sláið inn marglínu fylgiskjal þar sem enginn mótlykill er.

[![Marglínu fylgiskjal](./media/Multi-line.png)](./media/Multi-line.png)

-   Sláið inn fylgiskjal þar sem bæði lykillinn og mótlykillinn innihalda lyklagerð undirbókar, svo sem lánardrottinn/lánardrottinn, viðskiptavinur/viðskiptavinur, lánardrottinn/viðskiptavinur eða banki/banki.

[![Fylgiskjal undirbókar](./media/subledger.png)](./media/subledger.png)

<a name="issues-with-one-voucher"></a>Vandamál varðandi eitt fylgiskjal
=======================

Eiginleiki eins fylgiskjals veldur vandamálum í uppgjöri, skattaútreikningum, afstemmingu undirbókar við fjárhagsbók, fjárhagsskýrslugerð og fleira. (Til dæmis, til að fá frekari upplýsingar um vandamál sem geta komið upp við uppgjör skal sjá [Stakt fylgiskjal með mörgum færslum viðskiptavina eða lánardrottna](https://docs.microsoft.com/en-us/dynamics365/unified-operations/financials/accounts-payable/single-voucher-multiple-customer-vendor-records).) Til að vinna og skrá rétt þurfa þessi ferli og skýrslur færsluupplýsingar. Þó að sumar aðstæður gætu samt sem áður virkað rétt, fer eftir uppsetningu fyrirtækisins, koma oft upp vandamál þegar margar færslur eru færðar inn í eitt fylgiskjal.

Til dæmis þegar eftirfarandi marglínu fylgiskjal er bókað.

[![Dæmi](./media/example.png)](./media/example.png)

Þá er búin til skýrslan **Útgjöld lánardrottins** á vinnusvæðinu **Fjármálainnsýn**. Skýrslan flokkar stöður kostnaðarlykla í lánardrottnaflokk og síðan lánardrottin. Við gerð skýrslunnar getur kerfið ekki ákvarðað hvaða lánardrottnaflokkar/lánardrottnar stofnuðu til kostnaðarins 250,00. Færsluupplýsingar vantar og þess vegna gerir kerfið ráð fyrir að fyrsti lánardrottin sem finnst í fylgiskjalinu hafi stofnað til 250,00. 250,00, sem er hluti af stöðu aðallykils 600120, er þá sýnt undir þeim lánardrottnaflokki/lánardrottni. Það er mjög líklegt að fyrsti lánardrottin í fylgiskjalinu sé ekki sá rétti og verður skýrslan því röng.

[![Kostnaður](./media/expenses.png)](./media/expenses.png)

<a name="the-future-of-one-voucher"></a>Framtíð eins fylgiskjals
=========================

Vegna þeirra vandkvæða sem minnst var á verður virkni eins fylgiskjals gerð úreld. Hins vegar, vegna þess að það eru virknigloppur sem treysta á þessa virkni, mun virknin ekki vera úreld öll í einu. Í staðinn munum við nota eftirfarandi áætlun: 

- **Vorútgáfa 2018** - Slökkt verður á virkninni sjálfgefið með færibreytu fjárhagsbókar. Hins vegar er hægt að kveikja á virkninni ef fyrirtækið hefur atburðarás sem heyrir undir atburðarás á viðskiptagloppum sem eru útlistaðar seinna í þessu efnisatriði.

  -   Ef viðskiptavinur hefur viðskiptaatburðarás sem ekki krefst eins fylgiskjals skal ekki kveikja á virkninni. Við munum ekki laga „villur“ á þeim svæðum sem eru auðkenndar síðar í þessu efnisatriði ef þessi virkni er notuð jafnvel þó að önnur lausn sé til staðar.

  -   Hættið að nota Eitt fylgiskjal fyrir samþættingu í Microsoft Dynamics 365 Finance and Operations, nema virknin sé nauðsynleg fyrir eina af virknigloppunum.

- **Haustútgáfa 2018 og síðar** - Fyllt verður upp í virknigloppurnar. Eftir að fyllt hefur verið upp í virknigloppurnar verður slökkt á virkni eins fylgiskjals til frambúðar.

- > [!IMPORTANT]
  > Athugaðu að valkosturinn **Eitt fylgiskjal eingöngu** hefur EKKI verið fjarlægður úr uppsetningu færslubókarheitis.  Þessi valkostur er ennþá studdur þegar fylgiskjalið inniheldur eingöngu fjárhagslyklagerðir.  Viðskiptavinir verða að gæta þess að nota þessa stillingu vegna þess að fylgiskjalið mun ekki bókast ef þeir nota **Eitt fylgiskjalsnúmer eingöngu**, en færa svo inn fleiri en einn viðskiptavin, lánardrottin, banka, eign eða verk.  Einnig geta viðskiptavinir ennþá fært inn lyklagerðir undirbókar, t.d. greiðslu innan eins fylgiskjals sem inniheldur lyklagerðir lánardrottins/banka.  

<a name="why-use-one-voucher"></a>Af hverju að nota Eitt fylgiskjal?
====================

Byggt á samtölum við viðskiptavini höfum við tekið saman eftirfarandi lista yfir aðstæður þar sem viðskiptavinir nota virknina Eitt fylgiskjal eða ástæður þess að þeir nota hana. Nokkrar af þessum viðskiptakröfum er aðeins hægt að uppfylla með því að nota Eitt fylgiskjal. Hins vegar, í mörgum tilfellum, geta aðrir valkostir uppfyllt sömu viðskiptakröfum.

<a name="scenarios-that-require-one-voucher"></a>Tilfelli sem krefjast Eins fylgiskjals
----------------------------------

Eftirtaldar tilfelli er aðeins hægt að ná með því að nota virknina Eitt fylgiskjal. Fyllt verður í þessar virknigloppur með öðrum eiginleikum í haustútgáfu 2018 og seinni útgáfum.

-   **Bóka lánardrottin eða greiðslur viðskiptavinar á samantektarskjámynd bankareiknings**

    -   Fyrirtæki miðlar lista yfir lánardrottna og upphæðum á bankann sinn og bankinn notar listann til að greiða lánardrottnum fyrir hönd fyrirtækisins. Bankinn bókar samtölu greiðslnanna sem staka úttekt af bankareikningnum.

>   Samantekt á greiðslum lánardrottins er aðeins studd af Einu fylgiskjali. Hver seljandi er færður inn sem aðskilin lína til að viðhalda upplýsingum í undirbók viðskiptaskuldar, en samantekna upphæðin fyrir allar greiðslur eru jafnaðar við eina línu fyrir bankareikninginn. Þess vegna er úttektin sýnd sem stök samantekin upphæð í undirbók bankans.

-   Fyrirtæki greiðir innborgun viðskiptavina eða bankinn greiðir innborgun viðskiptavina fyrir hönd fyrirtækisins og innborgunin er sýnd sem eingreiðsla á bankareikningnum.

>   Samantekt á greiðslum viðskiptavina er yfirleitt studd með innborgunarvirkni. Hins vegar, ef þú notar „brúun" á greiðslumáta, er þessi atburðarás aðeins studd með Einu fylgiskjali. Greiðslur viðskiptavina eru færðar inn á sama hátt og lýst er fyrir samantekt á greiðslu lánardrottins.

-   **Kerfi til að flokka færslur frá viðskiptatilviki**

    -   Fyrirtæki hefur stakt viðskiptatilfelli sem kveikir á mörgum færslum. Hins vegar vill bókhaldsdeildin skoða bókhaldsfærslurnar saman fyrir betri endurskoðun.

>   Ef fyrirtæki þarf að skoða bókhaldsfærslur viðskiptatilviks saman verður að nota Eitt fylgiskjal. 

- **Landsbundnar aðgerðir**

  -   Aðgerðin Eitt stjórnsýsluskjal (SAD) fyrir Pólland krefst þess eins og er að notað sé eitt fylgiskjal. Þangað til flokkunarvalkostur er tiltækur fyrir þessa aðgerð, verður að halda áfram að nota virknina Eitt fylgiskjal. Það kunna að vera til fleiri landsbundnar aðgerðir sem krefjast virknina Eitt fylgiskjal.

- **Greiðslubók fyrirframgreiðslu fyrir viðskiptavini sem hefur skatta á mörgum „línum"**

  -   Viðskiptavinur greiðir fyrirframgreiðslu fyrir pöntun, og línurnar í pöntuninni hafa mismunandi skatta sem verða að vera skráðir fyrir fyrirframgreiðsluna. Fyrirframgreiðsla á greiðsla viðskiptavinar er ein færsla sem hermir eftir línum pöntunar, þannig að hægt sé að skrá viðeigandi skatt fyrir upphæðina á hverri línu.

Í þessari tilfelli eru viðskiptavinirnar í eina fylgiskjalinu sömu viðskiptavinirnir vegna þess að færslan líkir eftir línum fyrir pöntun viðskiptavinar. Fyrirframgreiðslan verður að vera færð inn í eitt fylgiskjal vegna þess að skattaútreikningur verður að vera gerður á „línum“ stöku greiðslunnar sem viðskiptavinurinn gerði.

-   **Viðhald eigna: Vinna upp afskriftir, skipta eign, reikna út afskrift á losun**

Eftirfarandi eignafærslur búa einnig til margar færslur innan eins fylgiskjals:
-   Viðbótarkaup eru gerð á eign og „vinna upp" afskrift er reiknuð út.
-   Eign er skipt.
-   Færibreyta til að reikna afskriftir við losun er virkjuð og síðan er eignin losuð.

<a name="scenarios-that-dont-require-one-voucher"></a>Tilfelli sem þurfa ekki Eitt fylgiskjal
----------------------------------------

Hægt er að gera eftirfarandi tilfelli með öðrum leiðum og ekki ætti að nota Eitt fylgiskjal.

-   **Bóka greiðslur viðskiptavinar á samantektarskjámynd bankareiknings**

Fyrirtæki greiðir innborgun viðskiptavina eða bankinn greiðir innborgun viðskiptavina fyrir hönd fyrirtækisins og innborgunin er sýnd sem eingreiðsla á bankareikningnum.

Samantekt á greiðslum viðskiptavina er studd með virkni innborgunar þegar brúun er ekki notuð á greiðslumátann.

-   **Greiðslujöfnun**

Í greiðslujöfnun eru stöður lánardrottins og viðskiptavinar greiðslujafnaðar gagnvart hvor annarri vegna þess að lánardrottin og viðskiptavinur eru sami aðilinn. Þessi nálgun lágmarkar peningafærslur milli fyrirtækis og viðskiptavinar/lánardrottins.

Hægt er að greiðslujafna með því að færa inn aukningu og minnkun í aðskildum fylgiskjölum og bóka jöfnunina á jöfnunarfjárhagslykil.

-   **Bóka í samantekt á fjárhagsbók**

Fyrirtæki vilja oft bóka í samantekt fjárhagsbókar til að lágmarka gagnamagn. Hins vegar krefjast fyrirtæki vanalega að færsluupplýsingunum sé samt sem áður viðhaldið. Þegar bókun er gerð í samantekt í gegnum eitt fylgiskjal eru færsluupplýsingar ekki þekktar og því ekki hægt að viðhalda þeim.

   -   Vegna þess að ekki er hægt að viðhalda færsluupplýsingum eins og er, þá mælum við með því að Eitt fylgiskjal sé ekki notað til að bóka í samantekt.
   -   Eftir að stuðningur við Eitt fylgiskjal er fjarlægður getum við innleitt upprunaskjals- og bókhaldsrammann í færslubókina. Þessir rammar munu síðan halda við samantekt á færsluupplýsingum og stuðningi í fjárhagsbókinni.

-   **Gera upp margar óbókaðar greiðslur á sama reikninginn**

Þessi atburðarás er venjulega að finna í smásölufyrirtækjum þar sem viðskiptavinir geta notað margar greiðsluaðferðir til að greiða fyrir innkaup. Í þessari tilfelli verður fyrirtækið að geta skráð margar óbókaðar greiðslur og jafna þær á móti reikningi viðskiptavinar.

Nýr eiginleiki sem var bætt í Microsoft Dynamics 365 for Operations útgáfa 1611 (nóvember 2016) gerir kleift að gera upp margar óbókaðar greiðslur á móti einum reikningi. Margar greiðslur viðskiptavina þurfa ekki lengur að vera færðar inn í eitt fylgiskjal.

-   **Flytja inn bankayfirlitsfærslur**

Bankar greiða oft og fá greiðslur fyrir hönd fyrirtækis og þessar færslur eru skráðar í Finance and Operations með skrá sem berst frá bankanum. Fyrirtæki vilja oft að flokka saman þessar færslur með því að nota bankayfirlitsnúmerið í skránni. Vegna þess að hver færsla er sýnd í smáatriðum á bankayfirlitinu, er ekki krafist samantektar í bankaundirbók.

Hægt er að flokka færslur með því að nota aðra reiti í færslubókinni, svo sem sjálft rununúmer færslubókarinnar eða skjalsnúmerið.

-   **Flytja stöður**

Fyrirtækið gæti þurft að flytja stöðu frá einum lánardrottni til annars lánardrottins, annaðhvort út af mistökum eða vegna þess að annar lánardrottin hefur tekið yfir ábyrgðina. Flutningur af þessu tagi á sér einnig stað fyrir lyklagerðir eins og viðskiptavini og bankareikninga.

Stöðufærslur frá einum lykli (lánardrottni, viðskiptavini, bankareikningi, o.s.frv.) til annars lykils er hægt að gera í gegnum aðskilin fylgiskjöl og hægt er að bóka jöfnunina á jöfnunarfjárhagslykil.

-   **Færa inn upphafsstöðu**

Fyrirtæki færa oft inn upphafsstöður fyrir lykla undirbóka (lánardrottin, viðskiptavin, eignir o.s.frv.) sem eina fylgiskjalsfærslu. Upphafsstöður fyrir hvern undirbókarlykil er hægt að færa inn sem aðskildin fylgiskjöl og hægt er að bóka jöfnunina á jöfnunarfjárhagslykil.

-   **Leiðrétta bókhaldsfærslu á bókuðu skjali viðskiptavinar eða lánardrottins**

Fyrirtæki gæti þurft að leiðrétta fjárhagslykil viðskiptakrafna eða viðskiptaskulda vegna bókhaldsfærslu á bókuðum reikningi, en reikninginn er ekki hægt að bakfæra eða leiðrétta með öðrum hætti.

Ef þarf að gera leiðréttingu á fjárhagslykli viðskiptakrafna eða viðskiptaskulda verður að gera hana beint á fjárhagslyklinum. Ekki er hægt að gera aðlögunina með því að bóka í gegnum lánardrottin eða viðskiptavin. Þessi nálgun krefst þess leiðréttingin sé gerð á „óvirkum tíma“ svo að fjárhagslykillinn geti tímabundið leyft handvirka færslu.

-   **„Kerfið leyfir það“**

Fyrirtæki nota oft virknina Eitt fylgiskjal eingöngu vegna þess að kerfið leyfir notkun þess án þess að gerð sé grein fyrir afleiðingunum.

