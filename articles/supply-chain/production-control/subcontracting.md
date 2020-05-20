---
title: Úthýsing
description: Þetta efnisatriði aðstoðar þig við að búa til kynningu á úthýsingu framleiðslu í Dynamics 365 Supply Chain Management.
author: christophernread
manager: tfehr
ms.date: 09/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 05e6ccdce21ccc5f3e83ad860163cccadcea2edc
ms.sourcegitcommit: ffd845d4230646499b6f074cb43e69ab95787671
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/07/2020
ms.locfileid: "3346423"
---
# <a name="subcontracting"></a>Úthýsing

[!include [banner](../includes/banner.md)]

Þetta efnisatriði aðstoðar þig við að búa til kynningu á úthýsingu framleiðslu í Microsoft Dynamics 365 Supply Chain Management. Fyrsti hlutinn í þessu efnisatriði lýsir uppsetningu á gögnum. Annar hlutinn fer með þig í gegnum skref kynningarinnar.

## <a name="target-audience"></a>Markhópur

Í þessu efnisatriði muntu fræðast um uppsetningu úthýsingar í framleiðslu. Þú notar fyrirliggjandi gögn í HQUS-lögaðilanum til að búa til grunnuppsetningu á aðgerðaflæði úthýsingar. Sýnigögnin í HQUS-lögaðilanum innihalda færibreytur uppsetningar sem hafa verið forstilltar til að styðja við skrefin í kynningunni. Jafnvel þótt kynningin fjallar um helstu vandamál og áskoranir fyrir mismunandi hlutverk, getur kerfisstjóri lokið henni.

## <a name="demo-scenario"></a>Sýnikennsla

Í HQUS-lögaðilanum eru hágæða hátalarar framleiddir. Á meðan á framleiðsluferlinu stendur fara hátalararnir í gegnum eftirfarandi þrjár aðgerðir.

- **Fyrirfram samsetning** - Hátalaraboxið er sett saman. Efnið fyrir boxið er tekið til í vöruhúsinu áður en aðgerðin er hafin.
- **Húðun** - Eftir að hátalaraboxið hefur verið sett saman verður að húða það. Lánardrottinn (undirverktaki) lýkur þessari aðgerð. Fyrirfram samsetta hátalaraboxið er sent til undirverktaka húðunar ásamt tveimur efnisþáttum.
- **Ljúka** - Eftir að undirverktakinn hefur húðað fyrirfram samsetta hátalaraboxið er því skilað til HQUS-lögaðila svo hægt sé að ljúka endanlegri samsetningu á hátalaranum.

Eftirfarandi skýringarmynd sýnir aðgerðirnar þrjár og efnisþættina sem voru notaðir.

![Aðgerðirnar „Fyrirfram samsetning“, „Húðun“ og „Ljúka“ og efnisþættirnir sem eru notaðir](./media/subcontract01_operations-materials.png)

## <a name="setup"></a>Setja upp

Áður en byrjað er á kynningunni þarf að setja upp gögnin.

### <a name="set-up-the-finished-product"></a>Setja upp tilbúna afurð

Þessi aðferð fer með þig í gegnum uppsetningu á losaðir afurð D8100, „Húðað hátalarabox“.

1. Veldu **Afurðaupplýsingastjórnun \> Afurðir \> Losaðar afurðir** til að opna síðuna **Upplýsingar um losaðar afurðir**.
2. Í flýtisíureitnum skal slá inn **D8100** til að finna fyrirliggjandi afurð.

    ![Síun á losaðri afurð D8100 á síðunni „Upplýsingar um losaðar afurðir“](./media/subcontract02_filtering-released-products.png)

3. Á aðgerðasvæðinu, í flipanum **Hanna**, skal velja **Leið** til að opna síðuna **Leið**.

    Síðan **Leið** sýnir átta leiðarútgáfur fyrir losaða afurð D8100. Átta leiðarútgáfunum er skipt niður á fjórar leiðir á svæði 1 og á svæði 5. Leið 000400 er notuð fyrir kostnað, leið 00041 er notuð þegar húðunaraðgerðin er innri aðgerð og leið 00042 er notuð þegar húðunaraðgerðin er utanaðkomandi aðgerð.

    ![Átta leiðarútgáfur á leiðarsíðunni](./media/subcontract03_route-page.png)

4. Í efri rúðunni, í hnitanetinu **Útgáfur**, skal velja leiðarútgáfu **00042** fyrir svæði **5**.
5. Í neðri rúðunni, í flipanum **Yfirlit** skal velja aðgerð **20** (**Cbnt Ctsc**) í hnitanetinu.

    ![Aðgerð 20 fyrir leiðarútgáfu 00042 fyrir svæði 5 er valið](./media/subcontract04_route-version-operation.png)

6. Veldu flipann **Almennt**.

    Athugaðu að reiturinn **Leiðargerð** er stilltur á **Lánardrottinn**. Þetta gildi gefur til kynna að aðgerð 20 (Cbnt CtSc) er aðgerð undirverktaka.

    ![Reitur leiðargerðar er stilltur á Lánardrottinn í flipanum Almennt](./media/subcontract05_general-tab.png)

7. Veldu flipann **Tilfangaþarfir**.

    Eiginleikar verða notaðir til að finna viðeigandi tilfang meðan á framleiðsluröðun stendur. Fyrir aðgerð 20 (Cbnt CtSc), athugaðu að tilfang sem hefur tvenns konar eiginleika, **Húðun** og **Húðuð box**, er krafist.

    ![Eiginleikarnir Húðun og Húðað box á flipa tilfangaþarfa](./media/subcontract06_resource-requirements-tab.png)

8. Veldu **Viðeigandi tilföng** til að opna svargluggann **Viðeigandi tilföng**.

    Þrjú tilföng finnast sem samsvara tilfangaþörfum fyrir aðgerðina. Taktu eftir að tilföng 8851 og 8852 eru af gerðinni **Lánardrottinn**.

    ![Þrjú viðeigandi tilföng í svarglugganum Viðeigandi tilföng](./media/subcontract07_applicable-resources-dialog.png)

9. Veldu **Í lagi** til að loka svarglugganum **Viðeigandi tilföng** og fara aftur á síðuna **Leið**.
10. Lokaðu síðunni **Leið** til að fara aftur á síðuna **Upplýsingar um losaðar afurðir**.

    ![Upplýsingasíða um losaðar afurðir](./media/subcontract08_released-product-details-page.png)

11. Á aðgerðasvæðinu, í flipanum **Hanna**, skal velja **Uppskriftarútgáfur** til að opna síðuna **Uppskriftarútgáfur**.

    Síðan **Uppskriftarútgáfur** sýnir fjórar uppskriftarútgáfur fyrir losaða afurð D8100. Uppskrift 000040 er notuð fyrir kostnað og áætlanagerð, uppskrift 000041 er notuð ef húðunaraðgerðin er gerð innanhúss og uppskriftir 000042 og 000043 eru notaðar ef húðunaraðgerð er úthýst.

    Athugaðu að vara S8050 er afurð af vörugerðinni **Þjónusta**. Þessi vara táknar úthýstu vinnuna.

    ![Fjórar uppskriftarútgáfur á útgáfusíðu uppskriftar](./media/subcontract09_bom-versions-page.png)

12. Á flýtiflipanum **Uppskriftarlínur** skal velja **Breyta** til að opna svargluggann **Breyta uppskriftarlínu**.

    Þegar framleiðslupöntun er búin til og áætluð fyrir losaða afurð D8100 verður innkauppöntun sjálfkrafa búin til fyrir vöru S8050. Þessi innkaupapöntun verður tengd við framleiðslupöntunina. Til þess að innkaupapantanir verði sjálfkrafa búnar til verður reiturinn **Línugerð** að vera stilltur á **Lánardrottinn** og velja þarf lánardrottnalykil fyrir undirverktakann. Í þessu tilviki er lánardrottnalykillinn US-801.

    Takið eftir að uppskriftarlínan er tengd við húðunaraðgerðina með aðgerðarnúmerinu (í þessu tilviki 20).

    ![Breyta svarglugga uppskriftarlínu](./media/subcontract10_edit-bom-line-dialog.png)

### <a name="create-a-password-for-warehouse-workers"></a>Stofna aðgangsorð fyrir starfsmenn í vöruhúsi

Þú verður að skilgreina aðgangsorð fyrir starfsmenn í vöruhúsi sem nota handbúnað.

1. Veldu **Vöruhúsakerfi \> Uppsetning \> Starfsmaður** til að opna síðuna **Verknotendur**.
2. Á flýtiflipanum **Notendur** skal velja línuna fyrir notanda **51**.

    ![Verknotendasíða](./media/subcontract11_work-users-page.png)

3. Veldu **Endurstilla aðgangsorð**.
4. Í reitunum **Aðgangsorð** og **Staðfesta aðgangsorð** skal slá inn **1**.
5. Veldu **Stilla aðgangsorð**.

## <a name="step-by-step-walkthrough"></a>Kynning skref fyrir skref

**Aðstæður og bakgrunnur**

Framleiðslupöntun upp á 10 stykki er búin til fyrir afurðina D8100, „Húðað hátalarabox“. Húðunin á boxinu er úthýst aðgerð sem lánardrottinn US-801, „Perfect Coating Solutions“, gerir. Framleiðslupöntunin samanstendur af þremur aðgerðum. Í fyrstu aðgerðinni er boxið fyrirfram samsett sem aðgerð innanhúss. Efnið fyrir fyrirfram samsetninguna er losað fyrir tiltekt í vöruhúsi hráefna. Eftir að fyrirfram samsetningu er lokið er fyrirfram samsetta boxið sent til „Perfect Coating Solutions“ ásamt tveimur efnisþáttum sem þarf að nota fyrir húðunaraðgerðina. Þegar húðaða boxið er móttekið frá lánardrottni fer það í gegnum endanlega samsetningaraðgerð innanhúss áður en það er tilkynnt sem lokið.

1. Veldu **Framleiðslustýring \> Framleiðslupantanir \> Allar framleiðslupantanir** til að opna síðuna **Allar framleiðslupantanir**.
2. Á aðgerðasvæðinu skal velja **Ný framleiðslupöntun** til að opna svargluggann **Stofna framleiðslupöntun**.

    ![Svarglugginn „Stofna framleiðslupöntun“](./media/subcontract12_create-production-order-dialog.png)

3. Í svæðið **Vörunúmer** veldu **D8100**.
4. Eftir að þú velur vörunúmer birtast reitir fyrir birgðavíddir. Í reitnum **Litur** er valið **Króm**.

    Skilaboðagluggi birtist sem spyr hvort ætti að setja inn virkar útgáfur fyrir uppskrift og leið.

    ![Skilaboðagluggi](./media/subcontract13_message-box.png)

5. Velja skal **Já**. 

    Í svarglugganum **Stofna framleiðslupöntun** eru virku útgáfur uppskriftar og leiðar fyrir afurð D8100 valdar sjálfkrafa í reitunum **Uppskriftarnúmer** og **Leiðarnúmer**. Í þessu tilviki er uppskrift **000040** og leið **000040** valin.
    
    > [!NOTE]
    > Fyrir bæði uppskrift og leið er útgáfa 000040 notuð fyrir kostnað og áætlanagerð.

6. Í reitnum **Svæði** skal velja **5**.
7. Í reitnum **Vöruhús** skal velja **51**.
8. Í reitunum **Uppskriftarnúmer** og **Leiðarnúmer** skal breyta sjálfkrafa valda gildinu í **000042**.

    > [!NOTE]
    > Fyrir bæði uppskrift og leið er útgáfa 000042 notuð til að úthýsa húðun á boxinu á lánardrottin US-801.

    ![Gildi stillt í svarglugganum „Stofna framleiðslupöntun“](./media/subcontract14_create-production-order-dialog-set.png)

9. Veldu **Stofna** til að búa til framleiðslupöntun og fara aftur á síðuna **Allar framleiðslupantanir**.

    ![Ný framleiðslupöntun á síðunni „Allar framleiðslupantanir“](./media/subcontract15_new-production-order.png)

10. Á aðgerðasvæðinu, í flipanum **Framleiðslupöntun** skal velja **Áætlun** til að opna svargluggann **Áætlun**.

    ![Svarglugginn Áætlun](./media/subcontract16_estimate-dialog.png)

11. Veldu **Í lagi** til að staðfesta áætlunina og fara aftur á síðuna **Allar framleiðslupantanir**.

    > [!NOTE]
    > Þegar framleiðslupöntun er áætluð er innkaupapöntunin fyrir þjónustuvöru S8050 búin til fyrir lánardrottin US-801.

12. Á aðgerðasvæðinu í flipanum **Framleiðslupöntun** skal velja **Uppskrift** til að opna síðuna **Uppskrift** þar sem hægt er að skoða uppskriftarlínur fyrir framleiðslupöntun.

    Athugaðu að fyrir þjónustuvöru S8050 er tilvísun í framleiðslupöntunina sem var búin til þegar framleiðslupöntunin var áætluð.

    ![Uppskriftarlínur framleiðslupöntunar á uppskriftarsíðunni](./media/subcontract17_production-order-bom-lines.png)

13. Lokaðu síðunni **Uppskrift** til að fara aftur á síðuna **Framleiðslupantanir**.
14. Á aðgerðasvæðinu í flipanum **Tímasetja** skal velja **Tímasetja verk** til að opna svargluggann **Vinnsluröðun**.
15. Tilgreindu eftirfarandi gildi:

    - Í reitnum **Röðunarstefna** er valið **Áfram frá morgundegi**.
    - Stilltu valkostinn **Takmörkuð geta** á **Já**.

    ![Svargluggi vinnsluröðunar](./media/subcontract18_job-scheduling-dialog.png)

16. Veldu **Í lagi** til að loka svarglugganum **Vinnsluröðun** og fara aftur á síðuna **Allar framleiðslupantanir**.
17. Á aðgerðasvæðinu, í flipanum **Tímasetja** skal velja **Gantt** til að opna síðuna **Gantt-rit - tilfangayfirlit**.

    Gantt-ritið veitir sjónrænt yfirlit yfir hvernig framleiðsluverkin eru áætluð á tilföngunum. Taktu eftir því að utanaðkomandi húðunaraðgerðin samanstendur af þremur verkum: vinnsluverki, flutningsverki og biðtímaverki.

    ![Gantt-rit á Gantt-ritinu - Yfirlitssíða tilfanga](./media/subcontract19_gantt-chart.png)

18. Lokaðu síðunni **Gantt-rit - tilfangayfirlit** til að fara aftur á síðuna **Allar framleiðslupantanir**.
19. Á aðgerðasvæðinu, í flipanum **Framleiðslupöntun** skal velja **Losa** til að opna svargluggann **Losa**.

    ![Svarglugginn Losa](./media/subcontract20_release-dialog.png)

20. Velja skal **Í lagi** til að loka svarglugganum **Losa**.
21. Veldu **Framleiðslustýring \> Reglubundin verkefni \> Losa í vöruhús \> Sjálfvirk losun á uppskriftar- og formúlulínum** til að opna svargluggann **Sjálfvirk losun uppskriftar og formúlulína**.

    ![Svarglugginn Sjálfvirk losun uppskriftar og formúlulína](./media/subcontract21_auto-release-bom-formula-lines-dialog.png)

22. Veldu **Í lagi** til að keyra Sjálfvirk losun á verki uppskriftar og formúlulína.

    Þetta verk losar tiltektarvinnu á hráefnum til vöruhúss.

23. Veldu **Framleiðslustýring \> Framleiðslupantanir \> Allar framleiðslupantanir** til að opna síðuna **Allar framleiðslupantanir**.
24. Notaðu flýtisíureitinn til að velja framleiðslupöntunina sem þú hefur verið að vinna við.
25. Á aðgerðasvæðinu, í flipanum **Vöruhús**, skal velja **Upplýsingar um verk** til að opna síðuna **Verk**.

    Taktu eftir að síðan sýnir tvö sett af verkum fyrir tiltekt á hráefni. Fyrra verkið er fyrir efni M8100 og M8101. Aðgerð 10 notar þessa efnisþætti. Seinna verkið er fyrir efni M8202 og M8250. Aðgerð 20 notar þessa efnisþætti, sem er úthýsta aðgerðin.

    ![Tvö sett af verkum fyrir hráefnatiltekt á Verksíðunni](./media/subcontract22_work-page.png)

26. Opnaðu vöruhúsaforritið til að vinna við vöruhúsaverkið fyrir aðgerð 10.

    <!-- TBD – screen shots for processing pick work for the materials. -->

27. Veldu **Framleiðslustýring \> Framleiðslupantanir \> Allar framleiðslupantanir** til að opna síðuna **Allar framleiðslupantanir**.
28. Notaðu flýtisíureitinn til að velja framleiðslupöntunina sem þú hefur verið að vinna við.
29. Á aðgerðasvæðinu, í flipanum **Framleiðslupöntun**, skal velja **Opna** til að opna svargluggann **Opna**.
30. Í flipanum **Almennt** skal tilgreina eftirfarandi gildi:

    - Í **Frá aðg. nr.** reitur, veljið **10**.
    - Í **Til aðg. nr.** reitur, veljið **10**.

    ![Gildi stillt í Almenna flipanum](./media/subcontract23_start-dialog.png)

31. Veldu **Í lagi** til að loka svarglugganum **Opna** og fara aftur á síðuna **Allar framleiðslupantanir**.

    Taktu eftir að staðan á framleiðslupöntuninni er nú **Opin**. Sjálfvirk bókun á færslubók tiltektarlista notar efnin fyrir aðgerð 10. Sjálfvirk bókun á færslubók leiðarspjalda gerir grein fyrir tímanotkun fyrir aðgerð 10.

32. Opnaðu vöruhúsaforritið til að vinna við vöruhúsaverkið fyrir aðgerð 20.

    <!-- TBD – screen shots for processing pick work for the materials. -->

33. Á aðgerðasvæðinu, í flipanum **Framleiðslupöntun**, skal velja **Opna** til að opna svargluggann **Opna**.
34. Í flipanum **Almennt** skal tilgreina eftirfarandi gildi:

    - Í **Frá aðg. nr.** reitur, veljið **20**.
    - Í **Til aðg. nr.** reitur, veljið **20**.
    - Í **Magn** reitinn er fært inn **10**.
    - Stilltu valkostinn **Bóka tiltektarlistann núna** á **Nei**.

    ![Gildi stillt í Almenna flipanum](./media/subcontract24_general-tab.png)

35. Veldu **Í lagi** til að loka svarglugganum **Opna** og fara aftur á síðuna **Allar framleiðslupantanir**.

    Tiltektarlisti er búinn til fyrir þau efni sem húðunaraðgerðin og þjónustuvaran notar. Þjónustuvaran sýnir kostnað á úthýstri aðgerð.

36. Á aðgerðasvæðinu, í flipanum **Skoða**, skal velja **Tínslulisti** til að opna síðuna **Tínslulisti**.
37. Veldu tínslulistann sem ekki er bókaður og veldu síðan færslubókarnúmerið til að skoða færslubókarlínurnar.

    ![Færslubókarlínur á síðu tínslulista](./media/subcontract25_picking-list.png)

38. Í aðgerðasvæðinu skal velja **Prenta** \> **Skýrsla tínslulista** til að opna svargluggann **Skýrsla tínslulista**.
39. Stilltu valkostinn **Nota útlit fylgiseðils** á **Já**.

    ![Svarglugginn Skýrsla tínslulista](./media/subcontract26_picking-list-report-dialog.png)

40. Veldu **Í lagi** til að búa til skýrslu fyrir **Tínslulista**.

    Í þessu tilfelli er fylgiseðill lánardrottins prentaður út frá færslubók tiltektarlista framleiðslunnar. Fylgiseðillinn tilgreinir þau efni sem eru send til lánardrottins sem mun sjá um húðunaraðgerðina.

    ![Skýrsla tiltektarlista](./media/subcontract27_picking-list-report.png)

41. Lokaðu skýrslunni **Tínslulisti** til að fara aftur á síðuna **Tínslulisti**.
42. Á aðgerðasvæðinu skal velja **Bóka** til að opna svargluggann **Bóka færslubók**.

    ![Svarglugginn Bóka færslubók](./media/subcontract28_post-journal-dialog.png)

43. Veldu **Í lagi** til að loka svarglugganum **Bóka færslubók**.
44. Opna innkaupapöntunina.

    ![Síða innkaupapöntunar](./media/subcontract29_purchase-order-page.png)

45. Á aðgerðasvæðinu, í flipanum **Innkaup**, skal velja **Staðfesta**.
46. Veldu **Bóka** til að opna svargluggann **Bóka færslubók**.
47. Veldu **Í lagi** til að loka svarglugganum **Bóka færslubók** og fara aftur á síðuna **Innkaupapöntun**.
48. Breyttu einingarverðinu úr **33** í **40**.

    ![Breyting á einingarverði á síðu innkaupapöntunar](./media/subcontract30_unit-price.png)

49. Staðfestu innkaupapöntunina aftur.
50. Innhreyfingarskjal.

    ![Svarglugginn Bókun innhreyfingarskjals](./media/subcontract31_posting-product-receipt-dialog.png)

51. Innkaupareikningur.
52. Uppfærðu samsvörunarstöðuna.

    ![Reikningssíða lánardrottins](./media/subcontract32_vendor-invoice-page.png)

53. Bóka sem lokið.

    ![Svarglugginn Bóka sem lokið](./media/subcontract33_report-as-finished-dialog.png)

54. Lok.

    ![Svarglugginn Lok](./media/subcontract34_end-dialog.png)

55. Kostnaðarsamanburður.

    ![Gröf kostnaðarsamanburðar](./media/subcontract35_cost-comparison-charts.png)

Vantar uppsetningu í gögnum.
