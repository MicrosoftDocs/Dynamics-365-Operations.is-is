---
title: Hlutfallsskipting hausagjalda á samsvarandi sölulínur
description: Þetta efnisatriði lýsir viðbótarmöguleikum til að reikna út og nota sjálfvirk gjöld í pantanir Commerce-rásar með því að nota ítarlegan eiginleika sjálfvirkra gjalda.
author: hhaines
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: cca35be696c8dd9956176e54e77a60f0252e0760
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/06/2021
ms.locfileid: "6352181"
---
# <a name="prorate-header-charges-to-matching-sales-lines"></a>Hlutfallsskipting hausagjalda á samsvarandi sölulínur


[!include [banner](includes/banner.md)]

Þetta efnisatriði lýsir virkninni fyrir flokkun á sjálfvirkum gjöldum á hausstigi og hlutfallsskipting þeirra á sölulínur Commerce. Þessi virkni er tiltæk fyrir færslur sem eru búnar til á sölustað (POS) í Retail útgáfu 10.0.1 og sölur sem eru búnar til í símaveri í Retail útgáfu 10.0.2.

Þessi virkni er aðeins tiltæk ef kveikt er á eiginleikanum [ítarleg sjálfvirk gjöld](/dynamics365/unified-operations/retail/omni-auto-charges) með því að nota valkostinn á síðunni **Færibreytur Commerce**. Auk þess má nota ítarlega reikningsaðferð fyrir sjálfvirk gjöld eingöngu fyrir sölupantanir sem eru búnar til í gegnum Commerce-rásir (POS, símaver og verkvang rafrænna viðskipta Dynamics).

Þessi nýja virkni veitir fyrirtækjum meiri sveigjanleika í því hvernig sjálfvirk gjöld á hausstigi eru reiknuð og notuð í sölufærslum.

Í útgáfum forritsins sem eru eldri en útgáfa 10.0.1 eru sjálfvirk gjöld fyrir hausstig sem eru með tiltekin tengsl flutningsmáta reiknuð aðeins þegar það er samsvörun við flutningsmáta sem er skilgreindur í sölupöntunarhaus.

Til dæmis eru sjálfvirk gjöld fyrir hausstig skilgreind fyrir flutningsmáta **99** og flutningsmáta **11**. Sölupöntun er búin til og flutningsmátinn **99** er skilgreindur í pöntunarhaus. Hins vegar eru nokkrar sölulínur settar upp þannig að þær eru fluttar með því að nota flutningsmátann **11**. Í þessu tilfelli eru aðeins gjöld á hausstigi sem eru tengd við flutningsmátann **99** tekin til greina og notuð í sölupöntun.

Í Commerce eru gjöld hausstigs með viðbótar eiginleika sem gerir þér kleift að skilgreina [skilgreinda stigskiptingu gjalds](/dynamics365/unified-operations/retail/configure-call-center-delivery) sem byggist á virði pöntunar. Til dæmis, ef virði pöntunar er á milli $50,00 og $200,00, gæti fyrirtæki viljað innheimta farmgjald sem nemur $5,00. Hins vegar, ef virði pöntunar er á milli $200,01 og $500,00 getur farmgjaldið numið $4,00.

Sum fyrirtæki vilja njóta góðs af stigskiptum útreikningi á gjaldi sem er boðið upp á með gjöldum á hausstigi. Hins vegar, í tilfellum sem fela í sér blandaðan flutningsmáta, þarf einnig að ganga úr skugga um að gjöldin sem eru reiknuð séu byggð á samsvörun við flutningsmátann sem er skilgreindur í hverri sölulínu fyrir sig.

Nú er hægt að skilgreina sjálfvirk gjöld á hausstigi þannig að allir flutningsmátar í pöntuninni eru teknir til greina þegar gjöld eru reiknuð út. Þessi virkni krefst flóknari reiknireglu útreiknings til að reikna út gjöld á hausstigi. Reiknireglan flokkar saman allar vörur sem eru afhentar með sama flutningsmátanum og meðhöndlar þann flokk sem reikniflokk fyrir vörurnar þegar hún reiknar út sjálfvirk gjöld á hausstigi. Fyrir vörur sem eru með sama flutningsmátann byggist útreikningur sjálfvirkra gjalda á sameinuðu söluvirði varanna. Á þennan hátt er viðeigandi stigi sjálfvirks gjalds ákvarðað.

Eftir að viðeigandi gjöld á hausstigi eru fengin fyrir sölulínur sem eru afhentar með sama flutningsmátanum, eru útreiknuðum gjöldum hlutfallsskipt á stigi sölulína. Vegna þess að þessi gjöld eru á línustigi og ekki haldið á hausstigi er gerður sértækari tengill á milli virði vörunnar og gjaldsins sem reiknað er fyrir það. Þessi aðferð getur verið gagnleg í atburðarásum hlutaskila, þar sem fyrirtæki vill endurgreiða aðeins hluta af gjaldinu í stað alls gjaldsins þegar einungis nokkrum vörum er skilað.

## <a name="scenarios"></a>Sviðsmyndir

Eftirfarandi tvær sýnidæmi lýsa því hvernig þessi gjöld eru reiknuð út bæði þegar nýja virknin er notuð og þegar hún er ekki notuð.

### <a name="scenario-1"></a>Aðstæður 1

Þessi atburðarás lýsir hegðuninni þegar valkosturinn **Hlutfallsskipting á samsvarandi sölulínur** er stilltur á **Nei** í uppsetningu sjálfvirks gjalds. (Hegðunin jafngildir hegðun gjalda á hausstigi í forritsútgáfum sem eru eldri en útgáfa 10.0.1.)

Í þessari atburðarás hefur fyrirtækið skilgreint gjöld hausstigs fyrir flutningsmáta sem tengist **99** og flutningsmáta sem tengist **11**. Engin sjálfvirk gjöld eru skilgreind fyrir flutningsmátann **21**.

![Sjálfvirk gjöld fyrir flutningsmátann 99 þegar slökkt er á hlutfallsskiptingu á samsvarandi línu.](media/99_disabled.png)

![Sjálfvirk gjöld fyrir flutningsmátann 11 þegar slökkt er á hlutfallsskiptingu á samsvarandi línu.](media/11_disabled.png)

Sölupöntun er stofnuð í símaverinu og flutningsmátinn er stilltur á **99**. Þessi pöntun inniheldur fimm vörur. Tvær pöntunarlínur hafa verið skilgreindar til að nota flutningsmátann **99**, tvær línur hafa verið skilgreindar til að nota flutningsmátann **11** og ein lína hefur verið skilgreind til að nota flutningsmátann **21** eins og sýnt er í eftirfarandi töflu.

| vara  | Línumagn | Afhendingarmáti | Verð á einingu |
|-------|---------------|---------------|----------------|
| 81331 | 1             | 11            | $10            |
| 81332 | 1             | 99            | $50            |
| 81333 | 2             | 11            | $30            |
| 81334 | 3             | 99            | $10            |
| 81334 | 3             | 21            | $5             |

Í þessari atburðarás er heildarpöntunin metin samkvæmt töflu fyrir sjálfvirk gjöld fyrir flutningsmátann **99**. Heildarsamtala allra sölulína er notuð til að ákvarða samsvarandi stig í skilgreiningu fyrir sjálfvirkt gjald og þetta gjald notað á hausstigi pöntunar. Í þessu dæmi er samtala pöntunar $165,00 og farmgjaldið er $15,00 er notað í pöntunarhaus. Aldrei er vísað í eða sjálfvirk gjöld notuð sem eru skilgreind fyrir flutningsmátann **11**.

Í þessari atburðarás, ef viðskiptavinur skilar sumum vörunum í pöntuninni og ef [gjaldakóðinn hefur verið skilgreindur svo hann verði endurgreiddur](/dynamics365/unified-operations/retail/omni-auto-charges#setup-and-configuration-2) er heildargjald á hausstigi notað kerfisbundið á endurgreiðsluna, jafnvel þótt aðeins sumar vörurnar hafi verið skilað.

### <a name="scenario-2"></a>Aðstæður 2

Í þessari atburðarás eru gjöld á hausstigi skilgreind fyrir flutningsmáta sem tengist **99** og flutningsmáta sem tengist **11**. Hinsvegar er valkosturinn **Hlutfallslega við samsvarandi sölulínur** stilltur á **Já** fyrir þessar töflur sjálfvirks gjalds.

![Sjálfvirk gjöld fyrir flutningsmátann 99 þegar kveikt er á hlutfallsskiptingu samsvarandi línu.](media/99_enabled.png)

![Sjálfvirk gjöld fyrir flutningsmátann 11 þegar kveikt er á hlutfallsskiptingu samsvarandi línu.](media/11_enabled.png)

Þessi atburðarás notar sömu sölupöntunina og inniheldur fimm línur. Flutningsmátinn í pöntunarhaus er stilltur á **99** en flutningsmátinn fyrir hverja vöru í sölupöntuninni er skilgreindur eins og sýnt er í eftirfarandi töflu.

| vara  | Línumagn | Afhendingarmáti | Verð á einingu |
|-------|---------------|---------------|----------------|
| 81331 | 1             | 11            | $10            |
| 81332 | 1             | 99            | $50            |
| 81333 | 2             | 11            | $30            |
| 81334 | 3             | 99            | $10            |
| 81334 | 3             | 21            | $5             |

Vegna þess að skilgreining sjálfvirks gjalds er stillt til að hlutfallsskipta samsvarandi sölulínur, framkvæmir kerfið eftirfarandi útreikningsskref.

1. Allar vörur sem eru með sama flutningsmátann eru flokkaðar saman og kerfið reiknar út heildarvirði afurðar fyrir vörurnar í flokknum.

    **Afhendingarmáti 11**

    - Vara 81331, magn 1 = $10
    - Vara 81333, magn 2 = $60 nettó ($30 á einingu)
    - **Heildarvirði afurðar fyrir flutningsmátann 11 = $70**

    **Afhendingarmáti 99**

    - Vara 81332, magn 1 = $50
    - Vara 81334, magn 3 = $30 nettó
    - **Heildarvirði afurðar fyrir flutningsmátann 99 = $80**

    **Afhendingarmáti 21**

    - Vara 81334, magn 3 = $15 nettó
    - **Heildarvirði afurðar fyrir flutningsmátann 21 = $15**

2. Kerfið leitar eftir skilgreiningu fyrir sjálfvirk gjöld hausstigs sem passa við viðskiptavininn og stillingar á flutningsmáta fyrir hvern vöruhóp. Ef skilgreiningin finnst lítur kerfið á stigskiptu skilgreininguna til að finna gjaldið sem á að nota, sem byggist á heildarvirði afurðar fyrir vörur í flokki flutningsmátans.

    **Afhendingarmáti 11**

    - Heildarvirði afurða = $70
    - **Andvirði gjalds = $7**

    **Afhendingarmáti 99**

    - Heildarvirði afurða = $80
    - **Andvirði gjalds = $15**

    **Afhendingarmáti 21**

    - Heildarvirði afurða = $15
    - **Andvirði gjalds = $0** (Engin sjálfvirk gjöld hafa verið skilgreind fyrir þessa samsetningu á viðskiptavini og flutningsmáta.)

    ![Gjöld fyrir flutningsmáta 11 falla undir undirstrikað stig.](media/step2mode11.png)

    ![Gjöld fyrir flutningsmáta 99 falla undir undirstrikað stig.](media/step2mode99.png)

3. Kerfið reiknar út andvirði gjalds sem á að nota fyrir hverja línu, bygg á reiknireglu hlutfallsskiptingar sem tekur mið af hlutfallslegu andvirði línunnar í tengslum við heildarvirði afurðarhópsins.

    **Afhendingarmáti 11**

    - Gildi gjalds = $7
    - Andvirði afurðarhóps = $70
    - Lína 1 virði = $10 (= 14,2857 prósent af hópvirði)
    - Lína 3 virði = $60 (= 85,7143 prósent af hópvirði)
    - **Línugjald fyrir línu 1 = $1**
    - **Línugjald fyrir línu 3 = $6**

    **Afhendingarmáti 99**

    - Andvirði gjalds = $15
    - Virði afurðarhóps = $80
    - Lína 2 virði = $50 (= 62,5 prósent af hópvirði)
    - Lína 4 virði = $30 (= 37,5 prósent af hópvirði)
    - **Línugjald fyrir línu 2 = $9,38**
    - **Línugjald fyrir línu 4 = $5,62**

    **Afhendingarmáti 21**

    - Andvirði gjalds = $0
    - Virði afurðarhóps = $15
    - Lína 5 virði = $15 (= 100 prósent af hópvirði)
    - **Línugjald fyrir línu 5 = $0**

Þar af leiðandi er, fyrir þetta dæmi, verður vöru 81334 úthlutað farmgjald sem nemur $5,62. Hægt er að skoða þessi gjöld á síðunni **Vinna með gjöld** fyrir sölulínuna. Eftirfarandi skýringarmynd sýnir hvernig þessi síða lítur út fyrir vöru 81334.

![Hlutfallslega skipt gjöld í sölulínu fyrir vöru 81334.](media/proratedlinecharge.png)

Þegar þessi útreikningsaðferð er notuð í atburðarás fyrir hlutaskil, ef gjaldakóðinn er endurgreiðanlegur, verður aðeins hluti gjaldsins sem er úthlutað á þá línu endurgreiddur þegar vörunni er skilað.

## <a name="additional-resources"></a>Frekari upplýsingar

[Ítarleg sjálfvirk gjöld fyrir omni-rás](omni-auto-charges.md)

[Kveikja á og grunnstilla sjálfvirk gjöld eftir rás](auto-charges-by-channel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]