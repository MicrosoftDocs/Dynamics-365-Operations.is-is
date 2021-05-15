---
title: Bættu frammistöðu rafrænna skýrslugerðarlausna með því að bæta við gagnagjöfum með reiknaða reiti með færibreytum
description: Þetta efnisatriði útskýrir hvernig hægt er að auka afköst rafrænna skýrslugerðarlausna með því að bæta við gagnagjöfum reiknaðra reita með færibreytum.
author: NickSelin
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4ee5a074c5c6d2e2144181e39917b1cc42dfc015
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944839"
---
# <a name="improve-the-performance-of-er-solutions-by-adding-parameterized-calculated-field-data-sources"></a>Bættu frammistöðu rafrænna skýrslugerðarlausna með því að bæta við gagnagjöfum með reiknaða reiti með færibreytum

[!include [banner](../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig hægt er að taka [afkastarakningu](trace-execution-er-troubleshoot-perf.md) af sniðum [Rafrænnar skýrslugerðar](general-electronic-reporting.md) sem eru keyrðar og síðan nota upplýsingarnar úr þessum rakningum til að bæta afköst með því að stilla gagnagjafa **Reiknaðra reita** með færibreytum.

Sem hluti af hönnunarferlinu fyrir skilgreiningar rafrænnar skýrslugerðar til að búa til viðskiptaskjöl, skilgreinir þú aðferðina sem er notuð til að ná í gögn úr forritinu og færa þau inn í úttak sem er myndað. Með því að hanna gagnagjafa með færibreytum fyrir rafræna skýrslugerð af gerðinni **Reiknaður reitur**, er hægt að draga úr fjölda gagnagrunnskalla og draga umtalsvert úr tíma og kostnaði sem fer í að safna saman upplýsingum um framkvæmd rafræns skýrslugerðarsniðs.

## <a name="prerequisites"></a>Forkröfur

- Til að ljúka dæmunum í þessu efnisatriði þarftu að hafa aðgang að einu af eftirfarandi [hlutverkum](../sysadmin/tasks/assign-users-security-roles.md):

    - Þróunaraðili rafrænnar skýrslulausnar
    - Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar
    - Kerfisstjóri

- Stilla verður fyrirtæki á **DEMF**.
- Fylgja skal leiðbeiningunum í [Viðauka 1](#appendix1) í þessu efnisatriði til að sækja þætti fyrir dæmi um rafræna skýrslugerðarlausna Microsoft sem nauðsynlegir eru til að ljúka dæmunum í þessu efnisatriði.
- Fylgja skal leiðbeiningunum í [Viðauka 2](#appendix2) í þessu efnisatriði til að skilgreina lágmarkssafn af færibreytum rafrænnar skýrslugerðar sem er nauðsynlegt til að nota umgjörð rafrænnar skýrslugerðar til að bæta afköstin í dæminu um rafræna skýrslugerðarlausn Microsoft.

## <a name="import-the-sample-er-solution"></a>Flytja inn dæmið um rafræna skýrslugerðarlausn

Ímyndaðu þér að þú þurfir að hanna rafræna skýrslugerðarlausn til að búa til nýja skýrslu sem sýnir lánardrottnafærslur. Eins og er geturðu fundið færslurnar fyrir valinn lánardrottin á síðunni **Lánardrottnafærslur** síðunni (farðu á **Viðskiptaskuldir** \> **Lánardrottnar** \> **Allir lánardrottnar**, veldu lánardrottin og síðan, í aðgerðarúðunni, í flipanum **Lánardrottinn** í **Færslur** hópnum velurðu **Færslur**). Hins vegar viltu hafa allar lánardrottnafærslur saman í einu rafrænu skjali á XML-sniði. Þessi lausn mun samanstanda af nokkrum skilgreiningum rafrænnar skýrslugerðar sem innihalda nauðsynlegt gagnalíkan, líkanavörpun og sniðseiningar.

Fyrsta skrefið er að flytja inn dæmið um rafræna skýrslugerðarlausn til að búa til skýrslu um lánardrottnafærslu.

1. Skráðu þig inn í tilvikið af Microsoft Dynamics 365 Finance sem fyrirtækinu þínu er úthlutað.
2. Í þessu efnisatriði býrðu til og breytir skilgreiningum fyrir sýnifyrirtækið **Litware, Inc.**. Gakktu því úr skugga um að þessari skilgreiningarveitu hafi verið bætt við Finance-tilvikið þitt og verið merkt sem virk. Nánari upplýsingar er að finna í [Stofna skilgreiningarveitendur og merkja þá sem virka](tasks/er-configuration-provider-mark-it-active-2016-11.md).
3. Á vinnusvæðinu **Rafræn skýrslugerð** skal velja reitinn **Skilgreiningar skýrslugerðar**.
4. Á síðunni **Skilgreiningar**, skal flytja inn skilgreiningar rafrænnar skýrslugerðar sem voru sóttar sem forkröfur í Finance, í eftirfarandi röð: gagnalíkan, líkanavörpun, snið. Fyrir hverja skilgreiningu skal fylgja þessum skrefum:

    1. Í aðgerðarúðunni skal velja **Skipta út** \> **Hlaða úr XML-skrá**.
    2. Veljið **Vafra** til að velja viðeigandi skrá fyrir skilgreiningu rafrænnar skýrslugerðar á XML-sniði.
    3. Veljið **Í lagi**.

![Skilgreiningar fluttar inn á síðunni Skilgreiningar](./media/er-calculated-field-ds-performance-imported-configurations.png)

## <a name="review-the-sample-er-solution"></a>Yfirfara dæmi um rafræna skýrslugerðarlausn

### <a name="review-the-model-mapping"></a>Fara yfir líkanavörpun

1. Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal stækka **Líkan aukinna afkasta** og velja **Vörpun aukinna afkasta**.
2. Í aðgerðarúðunni skal velja **Hönnuður**.
3. Á síðunni **Líkanavörpun á gagnagjafa**, á aðgerðasvæðinu, skal velja **Hönnuður**.

    Þessi líkanavörpun rafrænnar skýrslugerðar er hönnuð til að framkvæma eftirfarandi aðgerðir:

    - Sækja listann yfir lánardrottnafærslur sem eru geymdar í töflunni VendTrans (**Trans** gagnagjafi).
    - Fyrir hverja færslu skal sækja úr VendTable-töflunni færslu lánardrottins sem færslan hefur verið bókuð fyrir (**\#Vend** gagnagjafi).

    > [!NOTE]
    > **\#Vend** gagnagjafinn er stilltur til að sækja samsvarandi lánardrottnafærslu með því að nota fyrirliggjandi tengslin „margar við eina“ **\@.'\>Relations'.VendTable\_AccountNum**.

    Líkanavörpunin í þessari skilgreiningu innleiðir grunngagnalíkanið fyrir eitthvert snið rafrænnar skýrslugerðar sem búið var til fyrir þetta líkan og keyrt í Finance. Þess vegna er efnið í gagnagjafanum **Trans** opið fyrir rafrænum skýrslugerðarsniðum á borð við útdrátt af **líkani** gagnagjafa.

    ![Trans-gagnagjafi á hönnunarsíðu líkanavörpunar](media/er-calculated-field-ds-performance-mapping-1.png)

4. Lokið síðunni **Hönnuður líkanavörpunar**.
5. Lokið síðunni **Líkanavörpun á gagnagjafa**.

### <a name="review-format"></a>Skoðaðu sniðmátið

1. Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal stækka **Líkan aukinna afkasta** og velja **Snið aukinna afkasta**.
2. Í aðgerðarúðunni skal velja **Hönnuður**.
3. Á síðunni **Sniðshönnuður**, í flipanum **Vörpun**, skal velja **Stækka/fella saman**.
4. Stækkið **Líkanið**, **Gögnin** og **Færsluna**.

    Þetta snið rafrænnar skýrslugerðar er hannað til að mynda skýrslu um lánardrottnafærslur á XML-sniði.

    ![Snið gagnagjafa og skilgreindar bindingar á sniðseiningum á síðu sniðshönnuðar](media/er-calculated-field-ds-performance-format.png)

5. Lokaðu síðunni **Sniðshönnuður**.

## <a name="run-the-sample-er-solution-to-trace-execution"></a>Keyra dæmi um lausn rafrænnar skýrslugerðar til að rekja framkvæmd

Ímyndum okkur að þú hafir lokið við að hanna fyrstu útgáfu af lausn rafrænnar skýrslugerðar. Núna viltu prófa hana í Finance-tilviki og greina afköst keyrslunnar.

### <a name="turn-on-the-er-performance-trace"></a>Kveikja á afkastarakningu rafrænnar skýrslugerðar

1. Veldu fyrirtækið **DEMF**.
2. Fylgdu leiðbeiningunum í [Kveikja á afkastarakningu rafrænnar skýrslugerðar](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace) til að búa til afkastarakningu á meðan snið rafrænnar skýrslugerðar er keyrt.

    ![Svarglugginn Notandafæribreytur](media/er-calculated-field-ds-performance-format-user-parameters.png)

### <a name="run-the-er-format"></a><a id="run-format"></a>Keyra snið rafrænnar skýrslugerðar

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Snið aukinna afkasta**.
3. Í aðgerðarúðunni skal velja **Keyra**.

## <a name="use-the-performance-trace-to-analyze-model-mapping-performance"></a>Nota afkastarakningu til að greina afköst líkanavörpunar

1. Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Vörpun aukinna afkasta**.
2. Í aðgerðarúðunni skal velja **Hönnuður**.
3. Á síðunni **Líkanavarpanir**, í aðgerðarúðunni, skal velja **Hönnuður**.
4. Á síðunni **Hönnuður líkanavörpunar**, í aðgerðarúðunni, skal velja **Afkastarakning**.
5. Veljið nýjustu rakninguna sem var mynduð og veljið síðan **Í lagi**.

Nýjar upplýsingar eru nú tiltækar fyrir sum atriði gagnagjafa fyrir núverandi líkanavörpun:

- Raunverulegur tími sem fór í að ná í gögn með því að nota gagnagjafann
- Sami tími sýndur sem prósenta af heildartímanum sem fór í að keyra alla líkanavörpunina

![Upplýsingar um keyrslutíma á hönnunarsíðu líkanavörpunar](./media/er-calculated-field-ds-performance-mapping-2.png)

Hnitanetið **Tölfræði um afköst** sýnir að gagnagjafinn **Trans** kallar á VendTrans-töfluna einu sinni. Gildið **\[265\]\[Q:265\]** af gagnagjafanum **Trans** gefur til kynna að 265 færslur lánardrottins hafi verið sóttar úr forritstöflunni og þeim skilað í gagnalíkanið.

Hnitanetið **Tölfræði um afköst** sýnir einnig að núverandi líkanavörpun tvítekur gagnagrunnsbeiðnir á meðan **\#Vend** gagnagjafinn er keyrður. Þessi tvítekning gerist af eftirfarandi ástæðum:

- Kallað er á lánardrottnatöfluna tvisvar sinnum fyrir hverja af 265 endurteknu lánardrottnafærslunum, sem gerir samtals 530 köll:

    - Eitt kall er gert til að slá inn númer lánardrottnalykilsins.
    - Eitt kall er gert til að slá inn lánardrottnaheitið.

- Kallað er á lánardrottnatöfluna fyrir hverja endurtekna lánardrottnafærslu, jafnvel þótt sóttar færslur hafi verið bókaðar fyrir aðeins fimm lánardrottna. Af 530 köllum, eru 525 tvítekin. Eftirfarandi mynd sýnir skilaboðin sem berast um tvítekin köll (gagnagrunnsbeiðnir).

![Skilaboð um tvítekna gagnagrunnsbeiðni á hönnunarsíðu líkanavörpunar](./media/er-calculated-field-ds-performance-mapping-2a.png)

Takið eftir að af heildarkeyrslutíma líkanavörpunar (u.þ.b. átta sekúndur) hefur meira en 80% (u.þ.b. sex sekúndum) verið eytt í að sækja gildi úr forritstöflunni VendTable. Sú prósenta er of há fyrir tvær eigindir af fimm lánardrottnum, í samanburði við magn upplýsinga úr forritstöflunni VendTrans.

Til að draga úr fjölda kalla sem gerð eru til að ná í upplýsingar um lánardrottin fyrir hverja færslu, og til að auka afköst líkanavörpunarinnar, er hægt að nota vistun í skyndiminni fyrir gagnagjafann **\#Vend**.

> [!NOTE]
> **Trans\\\#Vend** gagnagjafinn verður vistaður í skyndiminni um það sem nemur núverandi færslu af **Trans** gagnagjafanum við keyrslu.

Með því að sækja **\#Vend** gagnagjafann er dregið úr fjölda tvítekinna kalla úr 525 í 260, en tvítekningum er ekki algjörlega útrýmt. Til að útrýma tvítekningum að fullu leyti er hægt að skilgreina nýjan gagnagjafa með færibreytum af gerðinni **Reiknaður reitur**.

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a>Bæta líkanavörpun á grundvelli upplýsinga úr framkvæmdarakningu

### <a name="change-the-logic-of-the-model-mapping"></a>Breyta reiknireglu líkanavörpunar

Fylgið þessum skrefum til að nota vistun í skyndiminni og gagnagjafa af gerðinni **Reiknaður reitur** til að hjálpa til við koma í veg fyrir tvítekin köll á gagnagrunn.

1. Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Vörpun aukinna afkasta**.
2. Í aðgerðarúðunni skal velja **Hönnuður**.
3. Á síðunni **Líkanavarpanir**, í aðgerðarúðunni, skal velja **Hönnuður**.
4. Á síðunni **Hönnuður líkanavörpunar** skal fylgja þessum skrefum til að bæta við gagnagjafa af gerðinni **Töflufærslur** til að fá aðgang að færslum í forritstöflunni VendTable:

    1. Í rúðunni **Gerðir gagnagjafa** skal stækka **Dynamics 365 for Operations** og velja **Töflufærslur**.
    2. Veljið **Bæta við rót**.
    3. Í gluggann, í reitinn **Heiti**, skal slá inn **Vend**.
    4. Í reitinn **Tafla** skal slá inn **VendTable**.
    5. Veljið **Í lagi**.

5. Hægt er að stilla færibreytur kalla til gagnagjafa af gerðinni **Reiknaður reitur** eingöngu ef þessir gagnagjafar eru í hólfi. Þess vegna skal fylgja þessum skrefum til að bæta við gagnagjafa af gerðinni **Tómt hólf** til að geyma nýjum færibreytustilltum gagnagjafa af gerðinni **Reiknaður reitur**:

    1. Í rúðunni **Gerðir gagnagjafa** skal stækka **Almennt** og velja **Tómt hólf**.
    2. Veljið **Bæta við rót**.
    3. Í gluggann, í reitinn **Heiti**, skal slá inn **Kassi**.
    3. Veljið **Í lagi**.

    ![Gagnagjafi í kassa á hönnunarsíðu líkanavörpunar](./media/er-calculated-field-ds-performance-mapping-3.png)

6. Fylgið þessum skrefum til að bæta við færibreytustilltum gagnagjafa af gerðinni **Reiknaður reitur**:

    1. Í rúðunni **Gagnagjafar** skal velja **Kassi**.
    2. Í rúðunni **Gerðir gagnagjafa** skal stækka **Virknir** og velja **Reiknaður reitur**.
    3. Veljið **Bæta við**.
    4. Í gluggann, í reitinn **Heiti**, skal slá inn **Vend**.
    5. Veljið **Breyta formúlu**.
    6. Á síðunni **Formúluhönnuður** skal velja **Færibreytur** til að tilgreina færibreyturnar sem þarf að útvega þegar kallað er á þennan gagnagjafa.
    7. Í svarglugganum **Færibreytur** skal velja **Ný**.
    8. Í reitinn **Heiti** skal færa inn **parmVendAccNumber**.
    9. Í reitnum **Gerð** velurðu **Strengur**.
    10. Veljið **Í lagi**.
    11. Í reitinn **Formúla** skal færa inn **FIRSTORNULL(FILTER(Vend, Vend.AccountNum=parmVendAccNumber))**.
    12. Veljið **Vista** og lokið síðunni **Formúluhönnuður**.
    13. Veljið **Í lagi** til að bæta við nýja gagnagjafanum.

7. Fylgið þessum skrefum til að merkja viðbættan gagnagjafa sem vistun í skyndiminni við keyrsluna:

    1. Í rúðunni **Gagnagjafar** skal velja **Kassi\\Vend**.
    2. Veljið **Skyndiminni**.

    > [!NOTE]
    > **Kassi\\Vend** gagnagjafinn verður vistaður í skyndiminni um það sem nemur öllum lánardrottnafærslum af **Trans** gagnagjafanum við keyrslu.

8. Fylgið eftirfarandi skrefum til að uppfæra faldaðan **Trans\\\#Vend** gagnagjafa svo að hann noti **Kassi\\Vend** gagnagjafann:

    1. Í rúðunni **Gagnagjafar** skal stækka **Trans**.
    2. Veljið **Trans\\\#Vend** gagnagjafa og veljið **Breyta** \> **Breyta formúlu**.
    3. Á síðunni **Formúluhönnuður**, í reitinn **Formúla**, skal slá inn **Box.Vend(\@.AccountNum)**.
    4. Veljið **Vista** og lokið svo síðunni **Formúluhönnuður**.
    5. Veljið **Í lagi** til að ljúka við breytingar á völdum gagnagjafa.

9. Veljið **Vista**.

    ![Vend-gagnagjafi á hönnunarsíðu líkanavörpunar](./media/er-calculated-field-ds-performance-mapping-4.png)

10. Lokið síðunni **Hönnuður líkanavörpunar**.
11. Lokið síðunni **Líkanavarpanir**.

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a>Ljúka við breyttu útgáfuna af líkanavörpun rafrænnar skýrslugerðar

1. Á síðunni **Skilgreiningar**, í flýtiflipanum **Útgáfur**, skal velja útgáfuna **1.2** af skilgreiningunni **Vörpun aukinna afkasta**.
2. Veljið **Breyta stöðu** \> **Ljúka** og veljið síðan **Í lagi**.

## <a name="run-the-modified-er-solution-to-trace-execution"></a>Keyra breytta lausn rafrænnar skýrslugerðar til að rekja framkvæmd

Endurtakið skrefin í hlutanum [Keyra snið rafrænnar skýrslugerðar](#run-format) fyrr í þessu efnisatriði til að búa til nýja afkastarakningu.

## <a name="use-the-performance-trace-to-analyze-adjustments-to-the-model-mapping"></a>Nota afkastarakningu til að greina leiðréttingar á líkanavörpun 

1. Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Vörpun aukinna afkasta**.
2. Í aðgerðarúðunni skal velja **Hönnuður**.
3. Á síðunni **Líkanavarpanir**, í aðgerðarúðunni, skal velja **Hönnuður**.
4. Á síðunni **Hönnuður líkanavörpunar**, í aðgerðarúðunni, skal velja **Afkastarakning**.
5. Veljið nýjustu rakninguna sem var mynduð og veljið síðan **Í lagi**.

Takiði eftir að leiðréttingar sem voru gerðar á líkanavörpun hafa eytt tvíteknum fyrirspurnum til gagnagrunns. Fjöldi kalla í gagnagrunnstöflur og gagnagjafa fyrir þessa líkanavörpun hefur einnig verið fækkað.

![Rakningarupplýsingar á hönnunarsíðu líkanavörpunar 1](./media/er-calculated-field-ds-performance-mapping-5.png)

Heildarkeyrslutími hefur verið minnkaður um 20-falt (úr u.þ.b 8 sekúndum í 400 millisekúndur). Afköst á allri lausn rafrænnar skýrslugerðar hefur þar af leiðandi verið endurbætt.

![Rakningarupplýsingar á hönnunarsíðu líkanavörpunar 2](./media/er-calculated-field-ds-performance-mapping-5a.png)

## <a name="appendix-1-download-the-components-of-the-sample-microsoft-er-solution"></a><a name="appendix1"></a>Viðauki 1: Sækja þætti fyrir dæmið um rafræna skýrslugerðarlausn Microsoft

Sækja þarf eftirfarandi skrár og vista þær staðbundið.

| Skrá                                        | Efni |
|---------------------------------------------|---------|
| Aukin afköst model.version.1     | [Sýnishorn af skilgreiningu gagnalíkans rafrænnar skýrslugerðar](https://download.microsoft.com/download/4/6/f/46f0f3fa-782b-414a-8f7b-b6c64a388661/Performance_improvement_model.version.1.xml) |
| Aukin afköst mapping.version.1.1 | [Sýnishorn af skilgreiningu líkanavörpunar rafrænnar skýrslugerðar](https://download.microsoft.com/download/8/9/1/8913a763-afb8-4bf4-aaf1-95ad793ffc5a/Performance_improvement_mapping.version.1.1.xml) |
| Aukin afköst format.version.1.1  | [Sýnishorn af skilgreiningu á sniði rafrænnar skýrslugerðar](https://download.microsoft.com/download/9/0/c/90c75963-bc78-4edc-9096-556bbe281f10/Performance_improvement_format.version.1.1.xml) |

## <a name="appendix-2-configure-the-er-framework"></a><a name="appendix2"></a>Viðauki 2: Skilgreina umgjörð rafrænnar skýrslugerðar

Áður en byrjað er að nota umgjörð rafrænnar skýrslugerðar til að bæta afköstin í dæminu um rafræna skýrslugerðarlausn Microsoft, þarf að skilgreina lágmarkssafn af færibreytum rafrænnar skýrslugerðar.

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a>Skilgreina færibreytur Rafræn skýrslugerðar

1. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
2. Á síðunni **Skilgreiningar þýðingar**, í hlutanum **Tengdir tenglar**, skal velja **Færibreytur rafrænnar skýrslugerðar**.
3. Á síðunni **Færibreytur rafrænnar skýrslugerðar**, í flipanum **Almennt**, skal stilla valkostinn **Kveikja á hönnunarstillingu** á **Já**.
4. Í flipanum **Viðhengi** skal stilla eftirfarandi færibreytur:

    - Í reitnum **Skilgreiningar** skal velja gerðina **Skrá** fyrir **DEMF** fyrirtækið.
    - Í reitunum **Verksafn**, **Tímabundið**, **Grunnlína** og **Annað** skal velja gerð fyrir **Skrá**.

Frekari upplýsingar um færibreytur rafrænnar skýrslugerðar er að finna í [Skilgreina ramma rafrænnar skýrslugerðar](electronic-reporting-er-configure-parameters.md).

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a>Virkja skilgreiningarveitu rafrænnar skýrslugerðar

Allar skilgreiningar rafrænnar skýrslugerðar sem bætt er við eru merktar sem eign skilgreingarveitu rafrænnar skýrslugerðar. Skilgreiningarveita rafrænnar skýrslugerðar sem er virkjuð á vinnusvæðinu **Rafræn skýrslugerð** er notuð í þessum tilgangi. Þess vegna þarf að virkja skilgreiningarveitu rafrænnar skýrslugerðar á vinnusvæðinu **Rafræn skýrslugerð** áður en byrjað er að bæta við eða breyta skilgreiningum rafrænnar skýrslugerðar.

> [!NOTE]
> Aðeins eigandi skilgreiningar rafrænnar skýrslugerðar getur breytt skilgreiningunni. Þess vegna, áður en hægt er að breyta skilgreiningu rafrænnar skýrslugerðar, verður að virkja viðeigandi skilgreiningarveitu rafrænnar skýrslugerðar á vinnusvæðinu **Rafræn skýrslugerð**.

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a>Fara yfir lista yfir skilgreiningarveitur rafrænnar skýrslugerðar

1. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
2. Á síðunni **Skilgreiningar þýðingar**, í hlutanum **Tengdir tenglar**, skal velja **Skilgreiningarveitur**.
3. Á síðunni **Tafla yfir skilgreiningarveitur** er hver færsla með einkvæmt heiti og vefslóð. Farið yfir efnið á þessari síðu. Ef færsla fyrir **Litware, Inc.** er þegar til skal sleppa næsta ferli, [Bæta við nýrri skilgreiningarveitu rafrænnar skýrslugerðar](#ActivateProvider).

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a>Bæta við nýrri skilgreiningarveitu rafrænnar skýrslugerðar

1. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
2. Á síðunni **Skilgreiningar þýðingar**, í hlutanum **Tengdir tenglar**, skal velja **Skilgreiningarveitur**.
3. Á síðunni **Skilgreiningarveitur** skal velja **Ný**.
4. Í reitinn **Heiti** skal færa inn **Litware, Inc.**
5. Í reitinn **Veffang** skal færa inn `https://www.litware.com`.
6. Veljið **Vista**.

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a>Virkja skilgreiningarveitu rafrænnar skýrslugerðar

1. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
2. Á síðunni **Skilgreiningar þýðingar**, í hlutanum **Skilgreiningarveitur**, skal velja reitinn **Litware, Inc.** og síðan velja **Stilla sem virkt**.

Nánari upplýsingar um skilgreiningarveitur rafrænnar skýrslugerðar er að finna í [Stofna skilgreiningarveitur og merkja þær sem virkar](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="additional-resources"></a>Frekari upplýsingar

- [Yfirlit yfir rafræna skýrslugerð](general-electronic-reporting.md)
- [Rekja keyrslu á sniðum rafrænnar skýrslugerðar til að úrræðaleita vandamál sem tengjast afköstum](trace-execution-er-troubleshoot-perf.md)
- [Stuðningur við færibreytur kallar á ER gagnagjafa af reitagerðinni Reiknað](er-calculated-field-type.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
