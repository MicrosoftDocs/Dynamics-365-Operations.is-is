---
title: Kemba gagnagjafa af keyrðu sniði rafrænnar skýrslugerðar til að greina gagnaflæði og umbreytingu
description: Þessi grein útskýrir hvernig þú getur villuleitt gagnaveitur á keyrðu ER sniði til að skilja betur stillt gagnaflæði og umbreytingu.
author: NickSelin
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 6fca177093caf42ad27b58eaa97e3f6997289eeb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884229"
---
# <a name="debug-data-sources-of-an-executed-er-format-to-analyze-data-flow-and-transformation"></a>Kemba gagnagjafa af keyrðu sniði rafrænnar skýrslugerðar til að greina gagnaflæði og umbreytingu

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

Þegar lausn rafrænnar skýrslugerðar er [skilgreind](tasks/er-format-configuration-2016-11.md) til að útbúa skjöl á útleið, skilgreinir þú aðferðirnar sem notaðar eru til að ná gögnum úr forritinu og færa þau inn í úttakið sem búið er til. Til að gera lífsferilsstuðning ER lausnarinnar skilvirkari ætti lausnin þín að samanstanda af ER gagnalíkani og kortlagningarhlutum þess, og einnig ER sniði og kortlagningarhlutum þess, þannig að líkanskortlagningin sé forritssértæk en aðrir íhlutir eru áfram umsókn-agnostic. Þar af leiðandi gætu nokkrir hlutar rafrænnar skýrslugerðar haft áhrif á ferli gagnainnsláttar í úttakinu sem búið er til.

Stundum líta gögn myndaðs úttaks út fyrir að vera öðruvísi en sömu gögn í gagnagrunni forritsins. Í þessum tilvikum er æskilegt að ákvarða hvaða íhlutur rafrænnar skýrslugerðar er ábyrgur fyrir gagnaumbreytingu. Kembiforritseiginleiki gagnagjafa rafrænnar skýrslugerðar dregur umtalsvert úr tíma og kostnaði sem eru hluti af þessari skoðun. Hægt er að stöðva keyrslu sniðs rafrænnar skýrslugerðar og opna kembiviðmót gagnagjafans. Þar er hægt að fletta upp tiltækum gagnagjöfum og velja staka gagnagjafa til keyrslu. Þessi handvirka keyrsla líkir eftir keyrslu gagnagjafans við raunkeyrslu á snið rafrænnar skýrslugerðar. Niðurstaðan kemur fram á síðu þar sem hægt er að greina gögnin sem eru móttekin.

Til að kveikja á villuleitareiginleika gagnagjafa skaltu stilla valkostinn **Virkja gagnakembingu við sniðskeyrslu** á **Já** í notendafæribreytum rafrænnar skýrslugerðar. Hægt er að ræsa kembingu gagnagjafa þegar snið rafrænnar skýrslugerðar keyrt til að mynda skjöl á útleið. Einnig er hægt að nota valkostinn **Hefja kembingu** til að ræsa gagnakerfiskembingu fyrir snið rafrænnar skýrslugerðar sem er skilgreint í reitnum [Aðgerðarhönnuður rafrænnar skýrslugerða](./tasks/er-format-configuration-2016-11.md#design-the-format-of-an-electronic-document).

Þessi grein veitir leiðbeiningar um að hefja kembiforrit gagnagjafa fyrir keyrð ER snið. Það útskýrir hvernig upplýsingarnar geta hjálpað til við að skilja gagnaflæði og gagnaumbreytingu. Dæmin í þessari grein nota viðskiptaferlið fyrir greiðslur lánardrottins.

## <a name="limitations"></a>Takmarkanir

Kembiforrit gagnagjafa er hægt að nota til að fá aðgang að gögnum gagnagjafa sem notuð eru í sniði rafrænnar skýrslugerðar sem keyrð eru til að mynda skjöl á útleið. Ekki er hægt að nota hana til að kemba gagnaveitur á sniðum rafrænnar skýrslugerðar sem eru hönnuð til að þátta skjöl á innleið.

Eftirfarandi stillingar á sniði rafrænnar skýrslugerðar eru ekki aðgengilegar fyrir kembingu gagnagjafa eins og er:

- Sníða umbreytingar
- Villuleitarreglur sniðs og vörpunar
- Virkja segðir
- Upplýsingar um gagnasöfnun í minni

## <a name="prerequisites"></a>Forkröfur

- Til að klára dæmin í þessari grein verður þú að hafa aðgang að einu af eftirfarandi [hlutverkum](../sysadmin/tasks/assign-users-security-roles.md):

    - Þróunaraðili rafrænnar skýrslulausnar
    - Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar
    - Kerfisstjóri

- Stilla verður fyrirtæki á **DEMF**.

- Fylgdu skrefunum í [Viðauki 1](#appendix1) þessarar greinar til að hlaða niður íhlutum Microsoft ER lausnarinnar sem þarf til að vinna úr greiðslum lánardrottins.
- Fylgdu skrefunum í [Viðauki 2](#appendix2) þessarar greinar til að undirbúa viðskiptaskuldir fyrir greiðsluvinnslu lánardrottins með því að nota ER lausnina sem þú munt hala niður.

## <a name="process-a-vendor-payment-to-get-a-payment-file"></a>Vinna úr greiðslu lánardrottins til að sækja greiðsluskrá

1. Fylgdu skrefunum í [Viðauki 3](#appendix3) þessarar greinar til að afgreiða greiðslur lánardrottins.

    ![Greiðsluferli lánardrottins í vinnslu.](./media/er-data-debugger-process-payment.png)

2. Hlaða niður og vista zip-skrána í staðbundnu tölvunni.
3. Útvíkkið **ISO20022 Credit transfer.xml** greiðsluskrána úr zip-skránni.
4. Opnið útdregnu greiðsluskrána með því að nota XML-skrárskoðara.

    Í greiðsluskránni inniheldur alþjóðlegt bankareikningsnúmer (IBAN-kóði) bankareiknings lánardrottins ekki nein bil. Því er það frábrugðið gildinu sem var [slegið inn](#enteredIBANcode) á síðunni **Bankareikningar**.

    ![IBAN-kóði án bila.](./media/er-data-debugger-payment-file.png)

    Hægt er að nota kembiforrit fyrir gagnagjafa rafrænnar skýrslugerðar til að finna út hvaða íhlutir rafrænnar skýrslugerðarlausnar eru notaðir til að stytta bil í IBAN-númerinu.

## <a name="turn-on-data-source-debugging"></a>Kveikja á kembingu gagnagjafa

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Á síðunni **Skilgreiningar**, í aðgerðarúðunni, í flipanum **Skilgreiningar**, í flokknum **Ítarlegar stillingar**, skal velja **Færibreytur notanda**.
3. Stilltu valkostinn **Virkja gagnakembingu við sniðskeyrslu** á **Já**.

    > [!NOTE]
    > Þessi breyta er notendasértæk og fyrirtækjasértæk.

    ![Svarglugginn Notandafæribreytur.](./media/er-data-debugger-user-parameters.png)

## <a name="process-a-vendor-payment-for-debugging"></a>Vinna úr greiðslu lánardrottins fyrir kembileit

1. Fylgdu skrefunum í [Viðauki 3](#appendix3) þessarar greinar til að afgreiða greiðslur lánardrottins.
2. Í skilaboðaglugganum skal velja **Já** til að staðfesta að þú viljir rjúfa úrvinnslu lánardrottnagreiðslu og í staðinn hefja kembingu á gagnagjafa á síðunni **Kemba gagnagjafa**.

    ![Staðfestingarboðsreitur.](./media/er-data-debugger-start-debugging.png)

## <a name="debug-data-sources-that-are-used-in-payment-processing"></a>Kembigagnaveitur sem eru notaðar í greiðsluvinnslu

### <a name="debug-the-model-mapping"></a>Kemba líkanavörpun

1. Á síðunni **Kemba gagnagjafa**, á aðgerðasvæðinu, skal velja **Líkanavörpun** til að hefja kembingu á þessum íhlut rafrænnar skýrslugerðar.
2. Í gagnaveitusvæðinu vinstra megin skal velja **\$notSentTransactions** gagnagjafa og síðan **Lesa allar færslur**.

    Hægt er að velja **Lesa 1 færslu**, **Lesa 10 færslur**, **Lesa 100 færslur** eða **Lesa allar færslur** til að þvinga lestur á viðeigandi fjölda færslna úr völdum gagnagjafa. Á þennan hátt er hægt að líkja eftir aðgangi að gagnagjafanum út frá sniði rafrænnar skýrslugerðar sem verið er að keyra.

3. Í gagnasvæðinu hægra megin skal velja **Útvíkka allt**.

    Hægt er að sjá að valinn gagnagjafi af gerðinni **Færslulisti** inniheldur eina færslu.

4. Útvíkkaðu gagnagjafann **\$notSentTransactions** og veldu földuðu aðferðina **vendBankAccountInTransactionCompany()**.
5. Útvíkkið **vendBankAccountInTransactionCompany()** aðferðina og veljið faldaða **IBAN** reitinn.
6. Veldu **Sækja gildi**.

    Hægt er að velja **Sækja gildi** til að þvinga lestur á gildi valins reits í völdum gagnagjafa. Á þennan hátt er hægt að líkja eftir aðgangi að þessum reit út frá sniði rafrænnar skýrslugerðar sem verið er að keyra.

7. Veldu **Útvíkka allt**.

    ![Gildi IBAN-reits í líkanavörpun.](./media/er-data-debugger-debugging-model-mapping.png)

    Eins og sjá má er líkanavörpunin ekki ábyrg fyrir styttingu á bilum því að IBAN-númerið sem hún skilar fyrir bankareikning lánardrottins inniheldur bil. Þess vegna verður að halda áfram með kembingu gagnaveitu.

### <a name="debug-the-format-mapping"></a>Kemba vörpun sniðs

1. Á síðunni **Kemba gagnagjafa**, á aðgerðasvæðinu, skal velja **Vörpun sniðs** til að halda áfram kembingu á þessum íhlut rafrænnar skýrslugerðar.
2. Veldu **\$PaymentByDebtor** gagnagjafann og svo **Lesa allar færslur**.
3. Útvíkkið **\$PaymentByDebtor**.
4. Útvíkkið **\$PaymentByDebtor.Lines** og veljið svo **Lesa allar færslur**.
5. Útvíkkið **\$PaymentByDebtor.Lines.CreditorAccount**.
6. Útvíkkið **\$PaymentByDebtor.Lines.CreditorAccount.Identification** og veljið svo **\$PaymentByDebtor.Lines.CreditorAccount.Identification.IBAN**.
7. Veldu **Sækja gildi**.
8. Veldu **Útvíkka allt**.

    ![Gildi IBAN-reitsins í vörpun sniðs.](./media/er-data-debugger-debugging-format-mapping.png)

    Eins og sjá má eru gagnagjafar sniðsvörpunar ekki ábyrgir fyrir styttingu á bilum því að IBAN-númerið sem þeir skila fyrir bankareikning lánardrottins inniheldur bil. Þess vegna verður að halda áfram með kembingu gagnaveitu.

### <a name="debug-the-format"></a>Kemba snið

1. Á síðunni **Kemba gagnagjafa**, á aðgerðasvæðinu, skal velja **Snið** til að halda áfram kembingu á þessum íhlut rafrænnar skýrslugerðar.
2. Víkkaðu sniðseiningar til að velja **ISO20022CTReports** \> **XMLHeader** \> **Skjal** \> **CstmrCdtTrfInitn** \> **PmtInf** og veljið svo **Lesa allar færslur**.
3. Víkkaðu sniðseiningar til að velja **ISO20022CTReports** \> **XMLHeader** \> **Skjal** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** og veljið svo **Lesa allar færslur**.
4. Víkkaðu sniðseiningar til að velja **ISO20022CTReports** \> **XMLHeader** \> **Skjal** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** og veldu svo **Sækja gildi**.
5. Veldu **Útvíkka allt**.

    ![Gildi IBAN-reitsins á sniðinu.](./media/er-data-debugger-debugging-format.png)

   Eins og sjá má er sniðsbindingin ekki ábyrg fyrir styttingu á bilum því að IBAN-númerið sem hún skilar fyrir bankareikning lánardrottins inniheldur bil. Þess vegna er einingin **BankIBAN** skilgreind til að nota umbreytingu sniðs sem styttir bil.

6. Lokið kembiforriti gagnagjafans.

### <a name="review-the-format-transformations"></a>Fara yfir umbreytingu sniðs

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Á síðunni **Grunnstillingar** skal velja **Greiðslulíkan** \> **ISO20022 Kreditfærsla**.
3. Veldu **Hönnuður** og víkkaðu svo einingarnar til að velja **Skjal** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**.

    ![BankIBAN eining á síðunni Sniðshönnuður.](./media/er-data-debugger-referred-transformation.png)

    Eins og sjá má er einingin **BankIBAN** skilgreind til að nota umbreytinguna **fjarlægja það sem er ekki bók- eða tölustafir**.

4. Veljið flipann **Umbreytingar**.

    ![Umbreytingarflipi fyrir eininguna BankIBAN.](./media/er-data-debugger-transformation.png)

    Eins og sjá má er umbreytingin **fjarlægja það sem er ekki bók- eða tölustafir** skilgreind til að nota segð sem styttir bil í textastrengnum sem gefinn er upp.

## <a name="start-to-debug-in-the-operation-designer"></a>Hefja kembingu í aðgerðarhönnuði

Þegar skilgreind eru útgáfudrög að sniði rafrænnar skýrslugerðar sem hægt er að keyra beint úr aðgerðarhönnuði, er hægt að fá aðgang að kembiforriti gagnagjafans með því að velja **Hefja kembingu** í aðgerðasvæðinu.

![Ræsihnappur kembingar á síðu aðgerðarhönnuðar.](./media/er-data-debugger-run-from-designer.png)

Sniðsvörpun og sniðþættir í sniði rafrænnar skýrslugerðar sem verið er að breyta eru tiltækir fyrir kembingu.

## <a name="start-to-debug-in-the-model-mapping-designer"></a>Hefja kembingu í hönnuði líkanavörpunar

Þegar skilgreind er líkanavörpun rafrænnar skýrslugerðar sem hægt er að keyra á síðunni **Líkanavörpun**, er hægt að fá aðgang að kembiforriti gagnagjafans með því að velja **Hefja kembingu** á aðgerðasvæðinu.

![Ræsihnappur fyrir kembingu á hönnunarsíðu líkanavörpunar.](./media/er-data-debugger-run-from-designer-mapping.png)

Líkanavörpunaríhlutur vörpunar rafrænnar skýrslugerðar sem verið er að breyta er tiltækur fyrir kembingu.

## <a name="appendix-1-get-an-er-solution"></a><a name="appendix1"></a>Viðauki 1: Sækja lausn rafrænnar skýrslugerðar

### <a name="download-an-er-solution"></a>Sækja lausn rafrænnar skýrslugerðar

Ef ætlunin er að nota lausn rafrænnar skýrslugerðar til að búa til rafræna greiðsluskrá fyrir lánardrottnagreiðslu sem unnið er úr, er hægt að [sækja](download-electronic-reporting-configuration-lcs.md) greiðslusnið **ISO20022-kreditfærsla** rafrænnar skýrslugerðar sem er í boði í samnýttu eignasafni í Microsoft Dynamics Lifecycle Services (LCS) eða í Altæku geymslunni.

![Innflutningur greiðslusniðs rafrænnar skýrslugerðar á síðu skilgreiningageymslu.](./media/er-data-debugger-import-from-repo.png)

Til viðbótar við valið ER snið, eftirfarandi [stillingar](general-electronic-reporting.md#Configuration) verður að vera sjálfkrafa flutt inn í þinn Microsoft Dynamics 365 Fjármálatilvik sem hluti af **ISO20022 Kreditmillifærsla** ER lausn:

- **Greiðslulíkan** Uppsetning ER gagnalíkans
- **ISO20022 Kreditmillifærsla** ER snið stillingar
- **Vörpun greiðslulíkans 1611** ER skilgreining vörpunar greiðslulíkans
- **Vörpun greiðslulíkans í viðtökustað ISO20022** Skilgreining líkanavörpunar rafrænnar skýrslugerðar

Hægt er að finna þessar skilgreiningar á síðunni **Skilgreiningar** fyrir ramma rafrænnar skýrslugerðar (**Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**).

![Skilgreiningar fluttar inn á síðunni Skilgreiningar.](./media/er-data-debugger-configurations.png)

Ef einhverjar fyrri uppgefnar skilgreiningar vantar í skilgreiningartrénu þarf að hlaða þeim niður handvirkt úr samnýttu eignasafni LCS á sama hátt og greiðslusnið **ISO20022-kreditfærslu** rafrænnar skýrslugerðar var hlaðið niður.

### <a name="analyze-the-downloaded-er-solution"></a>Greina sótta lausn rafrænnar skýrslugerðar

#### <a name="review-the-model-mapping"></a>Fara yfir líkanavörpun

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Veljið **Greiðslulíkan** \> **Vörpun greiðslulíkans 1611**.
3. Veljið **Hönnuður**.
4. Veljið vörpunarfærsluna **Greiðslulíkanavörpun ISO20022 CT**.
5. Veljið **Hönnuður** og farið yfir líkanavörpun sem er opin.

    Takið eftir því að reiturinn **Greiðslur** í gagnalíkaninu er bundinn gagnagjafanum **\$notSentTransactions** sem skilar lista yfir greiðslulínur lánardrottna sem verið er að vinna úr.

    ![Greiðslureitur á síðunni Hönnuður líkanavörpunar.](./media/er-data-debugger-model-mapping.png)

#### <a name="review-the-format-mapping"></a>Fara yfir vörpun sniðs

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Veljið **Greiðslulíkan** \> **ISO20022 kreditfærsla**.
3. Veljið **Hönnuður**.
4. Í flipanum **Vörpun** skal fara yfir sniðsvörpunina sem er opin.

    Takið eftir að **Skjal** \> **CstmrCdtTrfInitn** \> **PmtInf** eining **ISO20022CTReports** \> **XMLHeader** skrárinnar tengist **\$PaymentByDebtor** gagnagjafa sem er stilltur í hópfærslur á reitnum **Greiðslur** í gagnagjafa.

    ![PmtInf-eining á síðunni Sniðshönnuður.](./media/er-data-debugger-format-mapping.png)

#### <a name="review-the-format"></a>Yfirfara snið

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Veljið **Greiðslulíkan** \> **ISO20022 kreditfærsla**.
3. Veljið **Hönnuður** og farið yfir sniðið sem er opið.

    Takið eftir að sniðsstillingin undir **Skjal** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** er stillt á að setja inn IBAN-númer reiknings lánardrottins í greiðsluskrána.

    ![BankIBAN sniðseining á síðunni Sniðshönnuður.](./media/er-data-debugger-format.png)

## <a name="appendix-2-configure-accounts-payable"></a><a name="appendix2"></a>Viðauki 2: Skilgreina Viðskiptaskuldir

### <a name="modify-a-vendor-property"></a>Breyta eiginleika lánardrottins

1. Farið í **Viðskiptaskuldir** \> **Lánardrottnar** \> **Allir lánardrottnar**.
2. Velja skal lánardrottin **DE-01002** og síðan, á aðgerðasvæðinu, í flipanum **Lánardrottinn**, í flokknum **Uppsetning**, skal velja **Bankareikningar**.
3. Á flipanum **Auðkenni** í reitnum **IBAN** <a name="enteredIBANcode"></a>skal slá inn **GB33 BUKB 2020 1555 5555 55**.
4. Veldu **Vista**.

![IBAN-reitur stilltur á bankareikningssíðu lánardrottins.](./media/er-data-debugger-iban.png)

### <a name="set-up-a-method-of-payment"></a>Setja upp greiðslumáta

1. Farið í **Viðskiptaskuldir** \> **Greiðsluuppsetning** \> **Greiðsluháttur**.
2. Veljið greiðslumátann **SEPA CT**.
3. Í flipanum **Skráasnið**, í hlutanum **Skráasnið**, skal stilla valkostinn **Almennt rafrænt útflutningssnið** á **Já**.
4. Í **Útflutningssnið skilgreiningarsvæðinu** skal velja **ISO20022 Kreditfærsla** snið fyrir rafræna skýrslugerð.
5. Veldu **Vista**.

![Stillingar skráarsniðs á síðunni Greiðsluháttur.](./media/er-data-debugger-payment-method.png)

### <a name="add-a-vendor-payment"></a>Bæta við greiðslu lánardrottins

1. Farið í **Viðskiptaskuldir** \> **Greiðslur** \> **Greiðslubók lánardrottins**.
2. Bæta við nýrri greiðslubók.
3. Veldu **Línur** og bættu við nýrri greiðslulínu.
4. Í reitnum **Reikningur** velurðu lánardrottinn **DE-01002**.
5. Í reitnum **Debet** skal slá inn gildi.
6. Í reitnum **Greiðsluháttur** skal velja **SEPA CT**.
7. Veldu **Vista**.

![Lánardrottnagreiðslu bætt við síðu lánardrottnagreiðslu.](./media/er-data-debugger-payment-journal.png)

## <a name="appendix-3-process-a-vendor-payment"></a><a name="appendix3"></a>Viðauki 3: Meðhöndla greiðslu lánardrottins

1. Farið í **Viðskiptaskuldir** \> **Greiðslur** \> **Greiðslubók lánardrottins**.
2. Á síðunni **Greiðslubók lánardrottins** skal velja þá greiðslubók sem var áður stofnuð og síðan velja **Línur**.
3. Veljið greiðslulínuna og svo **Greiðslustaða** \> **Engin**.
4. Veldu **Búa til greiðslur**.
5. Í reitnum **Greiðsluháttur** skal velja **SEPA CT**.
6. Í reitnum **Bankareikningur** skal velja **DEMF OPER**.
7. Í svarglugganum **Búa til greiðslur** skal velja **Í lagi**.
8. Í **Svargluggi rafrænna skýrslufæribreyta** velurðu **Í lagi**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
