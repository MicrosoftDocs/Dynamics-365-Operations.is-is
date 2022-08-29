---
title: VSK yfirlýsing (Þýskaland)
description: Þessi grein lýsir því hvernig á að setja upp og búa til fyrirfram virðisaukaskattsskýrslu (VSK) fyrir Þýskaland á opinberu XML sniði.
author: AdamTrukawka
ms.date: 03/10/2022
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: ''
ms.openlocfilehash: 8ee288a1ec7ae950bdff9da7d373e29daef74d3c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269405"
---
# <a name="vat-declaration-germany"></a>VSK yfirlýsing (Þýskaland)

[!include [banner](../includes/banner.md)]

Þessi grein lýsir því hvernig á að setja upp og búa til fyrirfram virðisaukaskattsskýrslu (VSK) fyrir Þýskaland á opinberu XML sniði. Þessi grein útskýrir einnig hvernig á að forskoða virðisaukaskattsskýrsluna í Microsoft Excel.

Til að búa til skýrsluna sjálfkrafa skaltu búa til nógu marga VSK-kóða til að halda sérstakt VSK-bókhald fyrir hvern reit á fyrirfram VSK-yfirlýsingunni. Að auki, í forritssértækum færibreytum rafrænnar skýrslugerðar (ER) sniðs fyrir fyrirfram VSK yfirlýsingu, tengja virðisaukaskattskóða við uppflettingarniðurstöðu uppflettinganna fyrir reitina á VSK yfirlýsingunni.

Fyrir Þýskaland verður þú að stilla **Tilkynna reiti leit**. Fyrir frekari upplýsingar um hvernig á að setja upp forritssértækar færibreytur, sjá [Settu upp forritssértækar færibreytur fyrir VSK-yfirlýsingareiti](#set-up-application-specific-parameters-for-vat-declaration-fields) kafla síðar í þessari grein.

Í eftirfarandi töflu sýnir dálkurinn „Upplitsniðurstaða“ uppflettingarniðurstöðuna sem er forstillt fyrir tiltekna virðisaukaskattsskýrslulínu á sniði VSK-skýrslu. Notaðu þessar upplýsingar til að tengja virðisaukaskattskóða rétt við uppflettingarniðurstöðuna og síðan við línuna í virðisaukaskattsskýrslunni.

### <a name="vat-declaration-overview"></a><a name="vat-declaration-overview"></a> Yfirlit yfir virðisaukaskattsskýrslu

Fyrirfram virðisaukaskattsyfirlýsingin í Þýskalandi inniheldur eftirfarandi upplýsingar.

**KAFLI – AFHENDINGAR OG ANNAR ÞJÓNUSTA**

**Skattskyld sala**

| Lína | Box – skattstofn | Box – skattupphæð | Lýsing                                                                                                                                      | Niðurstaða uppflettingar                                                                             |
|-----|----------------|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| 20  | 81             | Án kóða     | Skattskyld sala á 19 prósenta skatthlutfalli.                                                                                                       | 20-Taxable Sales Standard</br>73-BadDebtsWriteOffStandard (81/50) – með mínusmerki             |
| 21  | 86             | Án kóða     | Skattskyld sala á skatthlutfalli 7 prósent.                                                                                                        | 21-Taxable Sales Lækkað</br>73-BadDebtsWriteOffReduced (86/50) – með mínusmerki               |
| 22  | 35             | 36               | Skattskyld sala á öðrum skatthlutföllum.                                                                                                                | 22-Taxable SalesAðrir verð</br>73-BadDebtsWriteOffOtherRates (35/36/50) – með mínusmerki      |
| 23  | 77             | *Engin skattupphæð*  | Sendingar frá landbúnaðar- og skógræktarfyrirtækjum í samræmi við §24 í þýsku virðisaukaskattslögunum (UStG) til viðskiptavina sem hafa virðisaukaskattsnúmer. | 23-EUSalaMeðalhlutfall24</br>73-BadDebtsWriteOffEUSalesAverageRate24 (77/50) – með mínusmerki |
| 24  | 76             | 80               | Sala sem greiða þarf skatt fyrir, samkvæmt §24 í UStG (sagnarvörur, drykkir og áfengir vökvar).                                | 24-Meðaltalsverð24</br>73-BadDebtsWriteOff SalesAverageRate24 (76/80/50)                    |

**Skattfrjáls sala með innskattsfrádrætti**

| Lína | Box – skattstofn | Box – skattupphæð | Lýsing                                                                       | Niðurstaða uppflettingar                       |
|-----|----------------|------------------|-----------------------------------------------------------------------------------|-------------------------------------|
| 26  | 41             | *Engin skattupphæð*  | Sendingar innan samfélags til viðskiptavina sem eru með virðisaukaskattsnúmer.                       | 26-EU Sala                          |
| 27  | 44             | *Engin skattupphæð*  | Afhendingar innan samfélags á nýjum ökutækjum til kaupenda sem eru ekki með virðisaukaskattsnúmer.    | 27-EUSalaNý farartæki               |
| 28  | 49             | *Engin skattupphæð*  | Afhendingar innan samfélags á nýjum ökutækjum utan fyrirtækis.                     | 28-EUSalaNý farartækiUtanfyrirtæki |
| 29  | 43             | *Engin skattupphæð*  | Önnur skattfrjáls sala sem hefur innskattsfrádrátt, svo sem útflutningssendingar. | 29-ExportOtherTaxFreeSales          |

**Skattfrjáls sala án innskattsfrádráttar**

| Lína | Box – skattstofn | Box – skattupphæð | Lýsing                                            | Niðurstaða uppflettingar                           |
|-----|----------------|------------------|--------------------------------------------------------|-----------------------------------------|
| 30  | 48             | *Engin skattupphæð*  | Skattfrjáls sala sem hefur ekki innskattsfrádrátt. | 30-Tax Free SalesWithoutInputTaxDeduction |

**Kaup innan bandalags**

| Lína | Box – skattstofn | Box – skattupphæð | Lýsing                                                                                                                   | Niðurstaða uppflettingar                                                    |
|-----|----------------|------------------|-------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| 33  | 91             | *Engin skattupphæð*  | Skattfrjáls kaup innan samfélags á sumum hlutum og fjárfestingargull.                                                    | 33-TaxFreeEUKaup                                             |
| 34  | 89             | Án kóða     | Skattskyld kaup innan samfélags með 19 prósenta skatthlutfalli.                                                             | 34-EUPurchase Standard</br>34-UseTaxEUPurchase Standard (89/61)        |
| 35  | 93             | Án kóða     | Skattskyld kaup innan samfélags með 7 prósenta skatthlutfalli.                                                              | 35-EUKauplækkað</br>35-UseTaxEUPurchaseReduced (93/61)          |
| 36  | 95             | 98               | Skattskyld kaup innan samfélags á öðrum skatthlutföllum.                                                                      | 36-EUKaupAðrir Verð</br>36-UseTaxEUPurchaseOtherRates (95/98/61) |
| 37  | 94             | 96               | Skattskyld kaup innan samfélags á nýjum ökutækjum frá birgjum sem eru ekki með virðisaukaskattsnúmer, á almennu skatthlutfalli. | 37-EUKaupökutæki</br>37-UseTaxEUPurchase Vehicles (94/96/61)     |

**KAFLI – RÉTTHAFI SEM SKATTSKULDA**

| Lína | Box – skattstofn | Box – skattupphæð | Lýsing                                                                        | Niðurstaða uppflettingar                                                                                        |
|-----|----------------|------------------|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| 40  | 46             | 47               | Önnur þjónusta frumkvöðla, byggð á restinni af samfélagssvæðinu.        | 40-bótaþegiSkattskuldari</br>40-UseTax BeneficiaryTaxDebtor (46/47/66)                                                                              |
| 41  | 73             | 74               | Sala sem fellur undir 2. mgr. 13b. gr. 3 í UStG.                               | 41-RáðþegiSkattskuldariFasteignaflutningur</br>41-UseTax BeneficiaryTaxDebtorFasteignaflutningur (73/74/67) |
| 42  | 84             | 85               | Önnur þjónusta sem fellur undir 2. mgr. 13b. gr. 1, 2 og 4 til 12 í UStG. | 42-BótþegiSkattskuldariAnnað</br>42-UseTax BeneficiaryTaxDebtorAnnað (84/85/67)                           |

**KAFLI – VIÐBÓTARUPPLÝSINGAR UM SÖLU**

| Lína | Box – skattstofn  | Box – skattupphæð | Lýsing                                                                                                | Niðurstaða uppflettingar                                                                                    |
|-----|-----------------|------------------|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| 48  | 42              | *Engin skattupphæð*  | Afhendingar frá fyrsta viðskiptavini ef um er að ræða þríhyrningsviðskipti innan samfélags.                   | 48-AfhendingarFyrsti viðskiptavinurEUT þríhyrningslaga                                                           |
| 49  | 60              | *Engin skattupphæð*  | Skattskyld sala starfandi frumkvöðuls sem þjónustuþegi skuldar skatt samkvæmt. | 49-Söluþjónusta ReverseCharge                                                                    |
| 50  | 21              | *Engin skattupphæð*  | Önnur óskattskyld þjónusta.                                                                                | 50-Önnur þjónusta Óskattskyld                                                                       |
| 51  | 45              | *Engin skattupphæð*  | Önnur óskattskyld sala þegar frammistaða er ekki í Þýskalandi.                                    | 51-Önnur Sala Óskattskyld                                                                          |
| 52  | *Engin skattupphæð* | *Engin skattupphæð*  | VSK.                                                                                                       | UMFERÐ 20 + Umf 21 + Umf 22 + Umf 2 4 + Umf 34 + Umf 35 + Umf 36 + Umf 37 + Umf 40 + Umf 41 + Umf 42 |

**KAFLI – FRADRAGSKTTUR**

| Lína | Box – skattupphæð | Lýsing                                                                                                | Niðurstaða uppflettingar                                                                                                                                                                |
|-----|------------------|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 55  | 66               | Inntaksupphæðir reikningsskatts frá öðrum fyrirtækjum, þjónustu og þríhyrningsviðskiptum innan samfélags.     | 55-InputTax 40-UseTaxBeneficiaryTaxDebtor (46/47/66)</br>74-BadDebtsWriteOffInputTax (66/37) – með mínusmerki                                                                   |
| 56  | 61               | Innskattsfjárhæðir af vörukaupum innan samfélags.                                           | 56-InputTaxEUPurchase 34-UseTaxEUPurchase Standard (89/61)</br>35-UseTaxEUPurchaseReduced (93/61)</br>36-UseTaxEUPurchaseOtherRates (95/98/61)</br>37-UseTaxEUPurchase Vehicles (94/96/61) |
| 57  | 62               | Innlagður innflutningssöluskattur.                                                                                 | 57-InputTaxImport                                                                                                                                                            |
| 58  | 67               | Innskattsfjárhæðir af þjónustu í skilningi §13b í UStG.                                        | 58-InputTax Services</br>41-UseTax BeneficiaryTaxDebtorFasteignaflutningur (73/74/67)</br>42-UseTax BeneficiaryTaxDebtorAnnað (84/85/67)                                                 |
| 59  | 63               | Innskattsfjárhæðir sem eru reiknaðar samkvæmt almennum meðaltöxtum.                                  | 59-InputTaxAverageRates</br>74-BadDebtsWriteOffInputTaxAverageRates (63/37) – með mínusmerki                                                                                    |
| 60  | 59               | Innskattsfrádráttur vegna afhendingar innan samfélags á nýjum ökutækjum utan fyrirtækis og smáfyrirtækja. | 60-InputTaxEUPaukaNý Ökutæki</br>74-BadDebtsWriteOffInputTaxEUPauka ný ökutæki (59/37) – með mínusmerki                                                                  |
| 61  | 64               | Leiðrétting á innskattsfrádrætti.                                                                     | 61-InputTax Correction                                                                                                                                                        |
| 62  | \-               | Eftirstandandi upphæð.                                                                                      | UMFERÐ 52 – UMFERÐ 55 – UMFERÐ 56 – UMFERÐ 57 – UMFERÐ 58 – UMFERÐ 50 – UMFERÐ 60 – UMFERÐ 61                                                                                                        |

**KAFLI – AÐRAR SKATTFÆRÐIR**

| Lína | Box – skattupphæð | Lýsing                                                                                                                                                                                                                                                         | Niðurstaða uppflettingar                                 |
|-----|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| 64  | 65               | Skattur vegna breytinga á skattlagningarformi og aukaskattur á skattlagðar útborganir vegna breytinga á skatthlutfalli.                                                                                                                                        | 64-Additional TaxDueChangeTaxRate              |
| 65  | 69               | Rangar eða óréttmætar skattfjárhæðir sem eru sýndar á reikningum og skattfjárhæðir sem eru skuldaðir í samræmi við 2. málslið 6a (4), 2. málslið 6a (4), 7. málslið 17. liðar (1) eða 2. mgr. 25b. útvistunarfyrirtæki eða vöruhúsvörður. | 65-TaxLækkun Leiðrétting                      |
| 67  | 39               | Frádráttur fastrar sérstakrar fyrirframgreiðslu vegna varanlegrar framlengingar. Þessi röð er venjulega aðeins fyllt út með síðustu fyrirfram tilkynningu skatttímabilsins.                                                                                                  | Innsláttarfæri notanda í skýrsluglugganum |
| 68  | 83               | Eftirstöðvar fyrirframgreiðslu söluskatts og eftirstöðvar umfram. Láttu mínusskrá fylgja með fyrir framan upphæðina.                                                                                                                                                          | UMFERÐ 62 + UMFERÐ 64 – UMFERÐ 65 – UMFERÐ 66             |

**KAFLI – VIÐBÓTARUPPLÝSINGAR UM LÆKNINGAR**

| Lína | Box – skattstofn | Box – skattupphæð | Lýsing                                                            | Niðurstaða uppflettingar                                                                                                                                                                                                    |
|-----|----------------|------------------|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 73  | 50             | \-               | Lækkun gjaldstofns á línum 20 til 24.                      | 73-BadDebtsWriteOffStandard (81/50)</br>73-BadDebtsWriteOffReduced (86/50)</br>73-BadDebtsWriteOffOtherRates (35/36/50)</br>73-BadDebtsWriteOffEUSalesAverageRate24 (77/50)</br>73-BadDebtsWriteOff SalesAverageRate24 (76/80/50) |
| 74  | \-             | 37               | Lækkun frádráttarbærra innskattsfjárhæða á línum 55, 59 og 60. | 74-BadDebtsWriteOffInputTax (66/37)</br>74-BadDebtsWriteOffInputTaxAverageRates (63/37)</br>74-BadDebtsWriteOffInputTaxEUPauka ný farartæki (59/37)                                                                     |

#### <a name="purchase-reverse-charge-vat"></a>Kaupa öfug gjaldfærslu VSK

Ef þú stillir VSK-kóða til að bóka VSK með því að nota virðisaukaskatt, tengdu VSK-kóðana þína við uppflettingarniðurstöðuna fyrir **Tilkynna reiti leit** sem inniheldur "UseTax" í nafninu.

Að öðrum kosti er hægt að stilla tvo aðskilda VSK-kóða: einn fyrir virðisaukaskatt sem ber að greiða og einn fyrir VSK-frádrátt. Tengdu síðan hvern kóða við samsvarandi leitarniðurstöður fyrir **Tilkynna reiti leit**.

Til dæmis, fyrir skattskyldar kaup innan samfélags á venjulegu gengi, stillir þú söluskattskóða **UT_S_EU** með afnotaskatti og tengja það við **34-UseTaxEUPurchase Standard** uppflettingarniðurstaða af **Tilkynna reiti leit**. Í þessu tilviki, upphæðir sem nota **UT_S_EU** söluskattskóði endurspeglast í reitunum 089 og 061 (línur 34 og 56).

Að öðrum kosti stillirðu tvo söluskattskóða:

  - **VAT_S_EU**, sem hefur skatthlutfallsgildi upp á -19 prósent
  - **InVAT_S_EU**, sem hefur 19 prósent skatthlutfall

Þú tengir síðan kóðana við uppflettingarniðurstöður af **Tilkynna reiti leit** á eftirfarandi hátt:

  - Félagi **VAT_S_EU** með **34-EUPurchase Standard** uppflettingarniðurstöðu.
  - Félagi **InVAT_S_EU** með **56-InputTaxEUPurchase** uppflettingarniðurstöðu.

Í þessu tilviki, upphæðir sem nota **VAT_S_EU** söluskattskóði endurspeglast í reit 089 (lína 34). Upphæðir sem nota **InVAT_S_EU** söluskattskóði kemur fram í reit 061 (röð 56).

Frekari upplýsingar um hvernig á að stilla öfuga gjaldfærslu VSK, sjá [Öfug gjöld](emea-reverse-charge.md).

## <a name="configure-system-parameters"></a>Stilla kerfisfæribreytur

Til að búa til virðisaukaskattsyfirlýsingu verður þú að stilla skattnúmer (Steuernummer) fyrirtækis þíns.

1. Fara í **Fyrirtækisstjórnun** > **Fyrirtæki** > **Lögaðilar**.
2. Veldu lögaðilann og veldu síðan **Skráningarauðkenni**.
3. Veldu eða búðu til heimilisfangið í Þýskalandi og síðan á **Skráningarauðkenni** Flýtiflipi, veldu **Bæta við**.
4. Í **Skráningartegund** reit skaltu velja skráningartegundina sem er tileinkuð Þýskalandi og sem notar **Fyrirtækjaauðkenni (COID)** skráningarflokk.
5. Í **Skráningarnúmer** reit, sláðu inn skattnúmerið.
6. Á **Almennt** flipa, í **Árangursrík** reit, sláðu inn dagsetninguna þegar númerið tekur gildi.

Fyrir frekari upplýsingar um hvernig á að setja upp skráningarflokka og skráningargerðir, sjá [Skráningarauðkenni](emea-registration-ids.md).

## <a name="set-up-a-vat-declaration-for-germany"></a>Settu upp virðisaukaskattsskýrslu fyrir Þýskaland

### <a name="import-er-configurations"></a>Flytja inn rafræn skýrslugerð grunnstillingar

Opnaðu **Rafræn skýrslugerð** vinnusvæði, og flyttu inn eftirfarandi útgáfur eða nýrri af þessum ER sniðum:

   - VSK-yfirlýsing Excel (DE).version.101.16.12.xml
   - VSK Yfirlýsing XML (DE).version.101.16.xml

### <a name="set-up-application-specific-parameters-for-vat-declaration-fields"></a><a name="set-up-application-specific-parameters-for-vat-declaration-fields"></a> Settu upp forritssértækar færibreytur fyrir VSK-yfirlýsingareiti

Til að búa til virðisaukaskattsyfirlýsingu sjálfkrafa skaltu tengja söluskattskóða í forritinu og leitarniðurstöður í ER uppsetningu.

> [!NOTE]
> Við mælum með að þú kveikir á eiginleikanum, **Notaðu forrita sérstakar færibreytur frá fyrri útgáfum af ER sniðum** í **Eiginleikastjórnun** vinnurými. Þegar þessi eiginleiki er virkur verða færibreytur sem eru stilltar fyrir fyrri útgáfu ER-sniðs sjálfkrafa gildar fyrir síðari útgáfu af sama sniði. Ef þessi eiginleiki er ekki virkur verður þú að stilla forritssértækar færibreytur sérstaklega fyrir hverja sniðútgáfu. The **Notaðu forrita sérstakar færibreytur frá fyrri útgáfum af ER sniðum** eiginleiki er fáanlegur í **Eiginleikastjórnun** vinnusvæði sem byrjar í Finance útgáfu 10.0.23. Fyrir frekari upplýsingar um hvernig á að setja upp færibreytur ER sniðs fyrir hvern lögaðila, sjá [Settu upp færibreytur ER sniðs fyrir hvern lögaðila](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-set-up.md).

Fylgdu þessum skrefum til að skilgreina hvaða VSK-kóðar búa til hvaða reiti á VSK-yfirlýsingunni.

1. Fara til **Vinnurými** > **Rafræn skýrslugerð**, og veldu **Skýrslustillingar**.
2. Veldu **VSK yfirlýsing XML (DE)** stillingar og veldu síðan **Stillingar \> Uppsetning á sérstökum breytum fyrir forrit**.
3. Á **Sértækar breytur fyrir forrit** síðu, á **Uppflettingar** Flýtiflipi, veldu **Tilkynna reiti leit**.
4. Á **Skilyrði** Flýtiflipi, stilltu eftirfarandi reiti til að tengja vsk-kóða og skýrslureit.

    | Reitur                  | Lýsing                                                                                                                                                                                                                                                                                                          |
    |------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Niðurstaða uppflettingar          | Veldu gildi skýrslureitsins. Frekari upplýsingar um gildin og úthlutun þeirra í línur VSK-skýrslu er að finna í [Yfirlit yfir virðisaukaskattsskýrslu](#vat-declaration-overview) kafla fyrr í þessari grein.                                                                                               |
    | Skattkóði               | Veldu VSK-kóðann sem á að tengja við skýrslureitinn. Bókaðar skattfærslur sem nota valda vsk-kóðann verða safnað í viðeigandi framtalsreit. Við mælum með að þú aðskiljir vsk-kóða á þann hátt að einn vsk-kóði myndar upphæðir í aðeins einum framtalsreit. |
    | Færsluflokkari | Ef þú bjóst til nógu marga VSK-kóða til að ákvarða framtalsreit skaltu velja **\* Ekki autt\***. Ef þú bjóst ekki til nógu marga VSK-kóða þannig að einn VSK-kóði myndar upphæðir í aðeins einum framtalsreit, geturðu sett upp færsluflokkara. Eftirfarandi færsluflokkar eru í boði:</br>-   **Innkaup**</br>-   **Undanþegin kaup** (skattfrjáls kaup)</br>-   **PurchaseReverseCharge** (skattur af öfugri gjaldfærslu)</br>-   **Sala**</br>-   **Undanþegin sölu** (skattfrjáls sala)</br>-   **SalesReverseCharge** (skattur sem greiddur er af öfugri greiðslu eða öfugri sölu)</br>-   **Notaðu skatt**. </br>Fyrir hvern færsluflokkara er einnig tiltækur flokkari fyrir kreditnótu. Til dæmis er einn af þessum flokkunaraðilum **PurchaseCreditNote** (kaupinneignarnóta).</br>Vertu viss um að búa til tvær línur fyrir hvern VSK-kóða: eina sem hefur færsluflokkunargildið og eina sem hefur færsluflokkarann fyrir kreditnótugildi. |

    > [!NOTE]
    > Tengja alla VSK-kóða við uppflettingarniðurstöður. Ef einhverjir söluskattskóðar ættu ekki að mynda gildi á virðisaukaskattsskýrslunni skaltu tengja þá við **Annað** uppflettingarniðurstöðu.

    ![Síða sértækra færibreyta fyrir forrit](media/69ecb881f12819259ca166b9b98b8303.jpg)

5. Í **Ríki** reit, breyttu gildinu í **Lokið**.
6. Á aðgerðarrúðunni velurðu **Útflutningur** til að flytja út stillingar á forritssértækum færibreytum.
7. Veldu **VSK yfirlýsing Excel (DE)** stillingar og veldu síðan á aðgerðarrúðunni **Flytja inn** til að flytja inn færibreyturnar sem þú stilltir fyrir **VSK yfirlýsing XML (DE)**.
8. Í reitnum **Staða** skal velja **Lokið**.

### <a name="set-up-the-vat-reporting-format-for-preview-amounts-in-excel"></a>Settu upp VSK-skýrslusnið fyrir forskoðunarupphæðir í Excel

1. Í **Eiginleikastjórnun** vinnusvæði, finndu og virkjaðu **Skýrslur á sniði virðisaukaskattsyfirlits** eiginleiki.
2. Fara til **Aðalbók** > **Uppsetning** > **Fjárhagsfæribreytur**.
3. Á **Söluskattur** flipa, á **Skattavalkostir** Flýtiflipi, í **Sniðskortlagning virðisaukaskattsyfirlits** reit, veldu **VSK yfirlýsing Excel (DE)**.

   Þetta snið er prentað þegar þú keyrir **Tilkynna söluskatt fyrir uppgjörstímabil** skýrslu. Það er líka prentað þegar þú velur **Prenta** á **Söluskattsgreiðslur** síðu.

4. Á **Skattayfirvöld** síðu, veldu skattyfirvöld og síðan í **Skýrsluskipulag** reit, veldu **Sjálfgefið**.

Ef þú ert að stilla virðisaukaskattsyfirlýsinguna í lögaðila sem hefur [margar virðisaukaskattsskráningar](emea-reporting-for-multiple-vat-registrations.md), fylgdu þessum skrefum:

1. Fara til **Aðalbók** > **Uppsetning** > **Fjárhagsfæribreytur**.
2. Á **Söluskattur** flipa, á **Rafræn skýrslugerð fyrir lönd/svæði** Flýtiflipi, á línunni fyrir **DEU**, veldu **VSK yfirlýsing Excel (DE)** ER snið.

## <a name="set-up-electronic-messages"></a>Settu upp rafræn skilaboð

### <a name="download-and-import-the-data-package-that-has-example-settings-for-electronic-messages"></a>Sæktu og flyttu inn gagnapakkann sem hefur dæmi um stillingar fyrir rafræn skilaboð

Gagnapakkinn inniheldur rafrænar skilaboðastillingar sem notaðar eru til að búa til virðisaukaskattsskýrslu á XML-sniði og síðan forskoða hana í Excel. Þú getur framlengt þessar stillingar eða búið til þínar eigin. Fyrir frekari upplýsingar um hvernig á að vinna með rafræn skilaboð og búa til þínar eigin stillingar, sjá [Rafræn skilaboð](../general-ledger/electronic-messaging.md).

1. Í [Microsoft Dynamics Lífsferilsþjónusta (LCS)](https://lcs.dynamics.com/v2), í Samnýtt eignasafn, veldu **Gagnapakki** sem eignategund og hlaðið síðan niður **DE VSK yfirlýsing EM pakki**. Skráarheitið sem hlaðið er niður er **DE VSK yfirlýsing EM package.zip**.
2. Í Dynamics 365 Finance, í **Gagnastjórnun** vinnusvæði, veldu **Flytja inn**.
3. Á **Flytja inn** Flýtiflipi, í **Nafn hóps** reit, sláðu inn nafn fyrir starfið.
4. Á flýtiflipanum **Valdar einingar** skal velja **Bæta við skrá**.
5. Í **Bæta við skrá** valmynd skaltu ganga úr skugga um að **Upprunagagnasnið** reiturinn er stilltur á **Pakki**, veldu **Hladdu upp og bættu við**, og veldu síðan zip-skrána sem þú sóttir áðan.
6. Veljið **Loka**.
7. Eftir að gagnaeiningunum hefur verið hlaðið upp skaltu velja á aðgerðarrúðunni **Flytja inn**.
8. Fara til **Skattur** > **Fyrirspurnir og skýrslur** > **Rafræn skilaboð** > **Rafræn skilaboð**, og staðfesta rafræn skilaboðavinnslu sem þú fluttir inn.

### <a name="configure-electronic-messages"></a>Stilla rafræn skilaboð

1. Fara til **Skattur** > **Uppsetning** > **Rafræn skilaboð** > **Fylltu færslur aðgerðir**.
2. Veldu línu fyrir **DE Fylltu út virðisaukaskattsskýrslur**, og veldu síðan **Breyta fyrirspurn**.
3. Notaðu síuna til að tilgreina uppgjörstímabilin sem á að hafa með í skýrslunni.
4. Ef þú verður að tilkynna skattfærslur frá öðrum uppgjörstímabilum í annarri yfirlýsingu skaltu búa til nýja **Fylltu út færslur** aðgerð og veldu viðeigandi uppgjörstímabil.

## <a name="preview-the-vat-declaration-in-excel"></a>Forskoðaðu virðisaukaskattsskýrsluna í Excel

### <a name="preview-the-vat-declaration-in-excel-from-the-report-sales-tax-for-settlement-period-periodic-task"></a>Forskoðaðu virðisaukaskattsskýrsluna í Excel úr reglubundnu verkinu Tilkynna söluskatt fyrir uppgjörstímabil

1. Fara til **Skattur** > **Reglubundin verkefni** > **Yfirlýsingar** > **Söluskattur** > **Tilkynna söluskatt fyrir uppgjörstímabil**.
2. Í **Uppgjörstímabil** reit, veldu gildi.
3. Í **Útgáfa söluskattsgreiðslu** reit, veldu eitt af eftirfarandi gildum:

    - **Upprunalegt** : Búa til skýrslu fyrir söluskattsfærslur upprunalegu söluskattsgreiðslunnar eða áður en söluskattsgreiðslan er mynduð.
    - **Leiðréttingar** : Búa til skýrslu fyrir söluskattsfærslur allra síðari söluskattsgreiðslna fyrir tímabilið.
    - **Heildarlisti** : Búa til skýrslu fyrir allar söluskattsfærslur tímabilsins, þar á meðal frumritið og allar leiðréttingar.

4. Í **Frá dags** reit, veldu upphafsdag skýrslutímabilsins.
5. Veldu **Allt í lagi**, og skoðaðu Excel skýrsluna.

### <a name="settle-and-post-sales-tax"></a><a name="settle-and-post-sales-tax"></a>Jafna og bóka virðisaukaskatt

1. Fara til **Skattur** > **Reglubundin verkefni** > **Yfirlýsingar** > **Söluskattur** > **Gera upp og bóka söluskatt**.
2. Í **Uppgjörstímabil** reit, veldu gildi.
3. Í **Útgáfa söluskattsgreiðslu** reit, veldu eitt af eftirfarandi gildum:

    - **Upprunalegt** : Búðu til upphaflega söluskattsgreiðslu fyrir uppgjörstímabilið.
    - **Nýjustu leiðréttingar** : Mynda leiðréttingarskattsgreiðslu eftir að upprunaleg söluskattsgreiðsla fyrir uppgjörstímabilið var stofnuð.

4. Í **Frá dags** reit, veldu upphafsdag skýrslutímabilsins.
5. Veldu **Í lagi**.

### <a name="preview-the-vat-declaration-in-excel-from-a-sales-tax-payment"></a>Forskoða virðisaukaskattsskýrsluna í Excel frá söluskattsgreiðslu

1. Fara til **Skattur** > **Fyrirspurnir og skýrslur** > **Fyrirspurnir um söluskatt** > **Söluskattsgreiðslur**, og veldu söluskattsgreiðslulínu.
2. Veldu **Prenta skýrslu**, og veldu síðan **Allt í lagi**.
3. Skoðaðu Excel skrána sem er búin til fyrir valda greiðslulínu söluskatts.

    > [!NOTE]
    > Skýrslan er aðeins mynduð fyrir valda línu söluskattsgreiðslunnar. Ef þú vilt búa til, til dæmis, leiðréttingaryfirlýsingu sem inniheldur allar leiðréttingar fyrir tímabilið, eða varayfirlýsingu sem inniheldur upprunalegu gögnin og allar leiðréttingar, notaðu **Tilkynna söluskatt fyrir uppgjörstímabil** reglubundið verkefni.

## <a name="generate-a-vat-declaration-from-electronic-messages"></a>Búðu til virðisaukaskattsskýrslu úr rafrænum skilaboðum

Þegar þú notar rafræn skilaboð til að búa til skýrsluna geturðu safnað skattagögnum frá mörgum lögaðilum. Fyrir frekari upplýsingar, sjá [Keyra virðisaukaskattsskýrslu fyrir marga lögaðila](#run-a-vat-declaration-for-multiple-legal-entities) kafla síðar í þessari grein.

Eftirfarandi aðferð á við um rafræn skilaboðavinnsludæmi sem þú fluttir inn úr LCS Shared eignasafni.

1. Fara til **Skattur** > **Fyrirspurnir og skýrslur** > **Rafræn skilaboð** > **Rafræn skilaboð**.
2. Í vinstri glugganum velurðu **DE VSK yfirlýsing**.
3. Á **Skilaboð** Flýtiflipi, veldu **Nýtt**, og síðan, í **Keyra vinnslu** valmynd, veldu **Allt í lagi**.
4. Veldu skilaboðalínuna sem er búin til, sláðu inn lýsingu og tilgreindu síðan upphafs- og lokadagsetningar yfirlýsingarinnar.

    > [!NOTE]
    > Skref 5 til 7 eru valfrjáls.

5. Valfrjálst: Á **Skilaboð** Flýtiflipi, veldu **Safna gögnum**, og veldu síðan **Allt í lagi**. Vöruskattsgreiðslur sem voru búnar til áður er bætt við skilaboðin. Fyrir frekari upplýsingar, sjá [Gera upp og bóka söluskatt](#settle-and-post-sales-tax) kafla fyrr í þessari grein. Ef þú sleppir þessu skrefi geturðu samt búið til virðisaukaskattsyfirlýsingu með því að nota **Útgáfa skattframtals** sviði í **Yfirlýsing** valmynd.
6. Valfrjálst: Á **Skilaboðaatriði** Flýtiflipi, skoðaðu söluskattsgreiðslur sem eru fluttar til vinnslu. Sjálfgefið er að allar söluskattsgreiðslur valins tímabils sem ekki voru innifalin í öðrum skilaboðum í sömu vinnslu eru innifalin.
7. Valfrjálst: Veldu **Upprunalegt skjal** til að fara yfir söluskattsgreiðslurnar, eða veldu **Eyða** að undanskilja söluskattsgreiðslur frá afgreiðslu. Ef þú sleppir þessu skrefi geturðu samt búið til virðisaukaskattsyfirlýsingu með því að nota **Útgáfa skattframtals** sviði í **Yfirlýsing** valmynd.
8. Á **Skilaboð** Flýtiflipi, veldu **Uppfæra stöðu**. Í **Uppfæra stöðu** valmynd, veldu **Tilbúið til að búa til**, og veldu síðan **Allt í lagi**. Staðfestu að skilaboðastöðu sé breytt í **Tilbúið til að búa til**.
9. Veldu **Búðu til skýrslu**. Til að forskoða virðisaukaskattsupphæðir, í **Keyra vinnslu** valmynd, veldu **Forskoðunarskýrsla**, og veldu síðan **Allt í lagi**.
10. Í **Rafrænar skýrslubreytur** valmynd, stilltu eftirfarandi reiti og veldu síðan **Allt í lagi**.

    | **Svæði**                                   | **Lýsing**                                                                                                                                                                                                              |
    |---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Jöfnunartímabil                           | Veldu uppgjörstímabil. Ef þú valdir **Safna gögnum** í skrefi 5 geturðu skilið þennan reit eftir auðan. Skýrslan verður til fyrir þær söluskattsfærslur sem eru innifaldar í innheimtum söluskattsgreiðslum. |
    | Útgáfa skattframtals                     | Veljið eitt af eftirfarandi gildum:</br>-   **Upprunalegt** – Mynda skýrslu fyrir söluskattsfærslur upprunalegu söluskattsgreiðslunnar eða áður en söluskattsgreiðslan er mynduð.</br>-   **Leiðréttingar** – Mynda skýrslu fyrir söluskattsfærslur allra síðari söluskattsgreiðslna fyrir tímabilið.</br>-   **Heildarlisti** – Búðu til skýrslu fyrir allar söluskattsfærslur tímabilsins, þar á meðal frumritið og allar leiðréttingar.|
    | Skattfulltrúi | Veldu þann aðila sem er skattfulltrúi fyrir virðisaukaskattsskýrslu, ef við á. Upplýsingar um valinn aðila eru fluttar út til **DatenLieferant** XML frumefni. |
    | Tengiliður | Veldu einstakling í fyrirtækinu sem er gagnaveitandi. Upplýsingar um valinn aðila eru fluttar út í **DatenLieferant** XML frumefni. |
    | Leiðrétt skil | Veldu **Já** ef þetta er virðisaukaskattsskýrsla til leiðréttingar. Í þessu tilviki mun XML þátturinn KZ10 hafa gildið **1**.|
    | Stuðningsskjöl | Veldu **Já** ef þú sendir líka fylgiskjöl. Í þessu tilviki mun XML þátturinn KZ22 hafa gildið **1**.|
    | SEPA-umboð fyrir beingreiðslu verður afturkallað sem undantekning| Veldu **Já** ef SEPA beingreiðsluheimild verður afturkölluð sem undantekning fyrir þetta forskráningartímabil. Til dæmis vegna jöfnunarbeiðna. Eftirstöðvar skal greiða sérstaklega. Í þessu tilviki mun XML þátturinn KZ26 hafa gildið **1**. |
    | Jöfnun á þeirri endurgreiðsluupphæð sem óskað er eftir | Veldu **Já** ef óskað er eftir skuldajöfnun á endurgreiðslufjárhæð eða ef endurgreiðslufjárhæð hefur verið ráðstafað. Í þessu tilviki mun XML þátturinn KZ29 hafa gildið **1**. |
    | Sérstök fyrirframgreiðsla varanleg framlenging | Færið inn frádráttarfjárhæð fastrar sérstakrar fyrirframgreiðslu til varanlegrar framlengingar. Þessari frádráttarfjárhæð er venjulega aðeins lokið við síðustu forskráningu skatttímabilsins. Upphæðin er flutt út í línu 67 (reitur 39) og XML-einingu KZ39 í virðisaukaskattsskýrslu. |

11. Veldu **Viðhengi** í efra hægra horninu á síðunni og veldu síðan **Opið**.
12. Skoðaðu upphæðirnar í Excel skjalinu og veldu síðan **Búðu til skýrslu**.
13. Til að búa til virðisaukaskattsyfirlýsingu á XML-sniði, í **Keyra vinnslu** valmynd, veldu **Búðu til skýrslu**, og veldu síðan **Allt í lagi**.
14. Í **Rafrænar skýrslubreytur** valmynd, stilltu reitina eins og lýst er í skrefi 10.
15. Veldu **Viðhengi** í efra hægra horninu á síðunni skaltu hlaða niður skránni og nota hana til að senda inn til skattyfirvalda.

## <a name="run-a-vat-declaration-for-multiple-legal-entities"></a><a name="run-a-vat-declaration-for-multiple-legal-entities"></a> Keyra virðisaukaskattsskýrslu fyrir marga lögaðila

Til að nota sniðin til að tilkynna um virðisaukaskattsyfirlýsingu fyrir hóp lögaðila, verður þú fyrst að setja upp forritssértækar færibreytur ER-sniða fyrir VSK-kóða frá öllum nauðsynlegum lögaðilum.

### <a name="set-up-electronic-messages-to-collect-tax-data-from-several-legal-entities"></a>Settu upp rafræn skilaboð til að safna skattagögnum frá nokkrum lögaðilum

Fylgdu þessum skrefum til að setja upp rafræn skilaboð sem safna gögnum frá mörgum lögaðilum.

1. Fara til **Vinnurými** > **Eiginleikastjórnun**.
2. Finndu og veldu **Fyrirspurnir þvert á fyrirtæki fyrir aðgerðir til að fylla út færslur** eiginleiki á listanum og veldu síðan **Virkja núna**.
3. Fara til **Skattur** > **Uppsetning** > **Rafræn skilaboð \> Fylltu færslur aðgerðir**.
4. Á **Fylltu færslur aðgerð** síðu, veldu línuna fyrir **DE Fylltu út virðisaukaskattsskýrslur**.

   Í **Uppsetning gagnaheimilda** rist, nýtt **Fyrirtæki** reitur er í boði. Fyrir núverandi færslur sýnir þessi reitur auðkenni núverandi lögaðila.

5. Í **Uppsetning gagnaheimilda** grid, bæta við línu fyrir hvern viðbótar lögaðila sem þarf að vera með í skýrslugerð. Stilltu eftirfarandi reiti fyrir hverja nýja línu.

    | Reitur                  | Lýsing                                                                                                                   |
    |------------------------|-------------------------------------------------------------------------------------------------------------------------------|
    | Nafn                   | Sláðu inn gildi sem hjálpar þér að skilja hvaðan þessi skrá kemur. Til dæmis, slá inn **VSK greiðsla dótturfélags 1**. |
    | Gerð skilaboðaatriðis      | Veldu **VSK skil**. Þetta gildi er eina gildið sem er tiltækt fyrir allar færslurnar.                                    |
    | Lykilgerð           | Veldu **Allt**.                                                                                                               |
    | Aðaltöfluheiti      | Tilgreindu **Skattskýrsluskírteini** fyrir allar heimildir.                                                                             |
    | Reitur skjalnúmers  | Tilgreindu **Skírteini** fyrir allar heimildir.                                                                                      |
    | Dagsetningarreitur skjals    | Tilgreindu **TransDate** fyrir allar heimildir.                                                                                    |
    | Reikningsreitur skjals | Tilgreindu **Skatttímabil** fyrir allar heimildir.                                                                                    |
    | Fyrirtæki                | Veldu auðkenni lögaðilans.                                                                                            |
    | Fyrirspurn notanda             | Þessi gátreitur er sjálfkrafa valinn þegar þú skilgreinir viðmið með því að velja **Breyta fyrirspurn**.                                 |

6. Veldu fyrir hverja nýja línu **Breyta fyrirspurn**, og tilgreindu tengt uppgjörstímabil fyrir lögaðilann sem tilgreint er í **Fyrirtæki** sviði á línunni.

Þegar uppsetningunni er lokið mun **Safna gögnum** virka á **Rafræn skilaboð** síða safnar söluskattsgreiðslum frá öllum lögaðilum sem þú skilgreindir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
