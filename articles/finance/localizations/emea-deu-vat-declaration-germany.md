---
title: VSK-skýrsla (Þýskaland)
description: Í þessari grein er lýst hvernig á að setja upp og búa til ítarlega VSK-skýrslu fyrir Þýskaland á opinberu XML-sniði.
author: AdamTrukawka
ms.date: 03/10/2022
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: ''
ms.openlocfilehash: 04c625b554d96f8ed28ceffef9647fe9cbf7fe2f
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689461"
---
# <a name="vat-declaration-germany"></a>VSK-skýrsla (Þýskaland)

[!include [banner](../includes/banner.md)]

Í þessari grein er lýst hvernig á að setja upp og búa til ítarlega VSK-skýrslu fyrir Þýskaland á opinberu XML-sniði. Þessi grein útskýrir einnig hvernig á að forskoða virðisaukaskattsskýrsluna í Microsoft Excel.

Til að búa skýrsluna til sjálfkrafa þarf að búa til nógu marga VSK-kóða til að halda sérstakt VSK-bókhald fyrir hvern glugga í ítarlegri VSK-skýrslunni. Auk þess, í forritstengdum færibreytum rafræns skýrslugerðarsniðs fyrir VSK-skýrsluna, skal tengja VSK-kóða við uppflettiniðurstöður fyrir gluggana í VSK-skýrslunni.

Fyrir Þýskaland þarf að skilgreina **Leit skýrslureits**. Frekari upplýsingar um hvernig á að setja upp forritstengdar færibreytur er að finna í hlutanum [Setja upp færibreytur tiltekins forrits fyrir reiti VSK-skýrslu](#set-up-application-specific-parameters-for-vat-declaration-fields) síðar í þessari grein.

Í eftirfarandi töflu sýnir dálkurinn „Niðurstaða uppflettingar“ niðurstöðuna sem er forstillt fyrir tiltekna línu VSK-skýrslu á VSK-skýrslusniðinu. Notaðu þessar upplýsingar til að tengja VSK-kóða við niðurstöðu uppflettingar á réttan hátt og síðan við línuna í VSK-skýrslunni.

### <a name="vat-declaration-overview"></a><a name="vat-declaration-overview"></a>Yfirlit VSK-skýrslu

Eftirtaldar upplýsingar koma fram í ítarlegri VSK-skýrslu í Þýskalandi.

**HLUTI – AFHENDINGAR OG ÖNNUR ÞJÓNUSTA**

**Skattskyld sala**

| Lína | Reitur – skattstofn | Gluggi – skattupphæð | Lýsing                                                                                                                                      | Niðurstaða uppflettingar                                                                             |
|-----|----------------|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| 20  | 81             | Án kóða     | Skattskyld sala við 19% skatthlutfall.                                                                                                       | 20-TaxableSalesStandard</br>73-BadDebtsWriteOffStandard (81/50) – með mínusmerki             |
| 21  | 86             | Án kóða     | Skattskyld sala við 7% skatthlutfall.                                                                                                        | 21-TaxableSalesReduced</br>73-BadDebtsWriteOffReduced (86/50) – með mínusmerki               |
| 22  | 35             | 36               | Skattskyld sala í öðrum skattþrepum.                                                                                                                | 22-TaxableSalesOtherRates</br>73-BadDebtsWriteOffOtherRates (35/36/50) – með mínusmerki      |
| 23  | 77             | *Enginn skattupphæð*  | Afhendingar frá fyrirtækjum í landbúnaði og skógrækt, í samræmi við § 24 í VSK-lögum Þýskalands (UStG), til viðskiptavina með VSK-númer | 23-EUSalesAverageRate24</br>73-BadDebtsWriteOffEUSalesAverageRate24 (77/50) – með mínusmerki |
| 24  | 76             | 80               | Sala sem greiða þarf skatt af, samkvæmt §24 í UStG (sag, drykkjarvörur og áfengi).                                | 24-SalesAverageRate24</br>73-BadDebtsWriteOffSalesAverageRate24 (76/80/50)                    |

**Skattfrjáls sala með innskattsfrádrætti**

| Lína | Reitur – skattstofn | Gluggi – skattupphæð | Lýsing                                                                       | Niðurstaða uppflettingar                       |
|-----|----------------|------------------|-----------------------------------------------------------------------------------|-------------------------------------|
| 26  | 41             | *Enginn skattupphæð*  | Afhendingar innan bandalags til viðskiptavina sem eru með VSK-númer.                       | 26-EUSales                          |
| 27  | 44             | *Enginn skattupphæð*  | Afhendingar innan bandalags á nýjum bifreiðum til kaupenda án VSK-númers    | 27-EUSalesNewVehicles               |
| 28  | 49             | *Enginn skattupphæð*  | Afhendingar innan bandalags á nýjum bifreiðum utan fyrirtækis.                     | 28-EUSalesNewVehiclesOutsideCompany |
| 29  | 43             | *Enginn skattupphæð*  | Aðrar skattfrjálsar sölur sem hafa innskattsfrádrátt, svo sem útflutningsafhendingar. | 29-ExportOtherTaxFreeSales          |

**Skattfrjáls sala án innskattsfrádráttar**

| Lína | Reitur – skattstofn | Gluggi – skattupphæð | Lýsing                                            | Niðurstaða uppflettingar                           |
|-----|----------------|------------------|--------------------------------------------------------|-----------------------------------------|
| 30  | 48             | *Enginn skattupphæð*  | Skattfrjáls sala sem er ekki með frádrátt frá innskatti. | 30-TaxFreeSalesWithoutInputTaxDeduction |

**Kaup innan bandalags**

| Lína | Reitur – skattstofn | Gluggi – skattupphæð | Lýsing                                                                                                                   | Niðurstaða uppflettingar                                                    |
|-----|----------------|------------------|-------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| 33  | 91             | *Enginn skattupphæð*  | Skattfrjáls kaup innan samfélagsins á sumum hlutum og gulli vegna fjárfestingar.                                                    | 33-TaxFreeEUPurchase                                             |
| 34  | 89             | Án kóða     | Skattskyld kaup innan bandalags við 19% skatthlutfall.                                                             | 34-EUPurchaseStandard</br>34-UseTaxEUPurchaseStandard (89/61)        |
| 35  | 93             | Án kóða     | Skattskyld kaup innan bandalags við 7% skatthlutfall.                                                              | 35-EUPurchaseReduced</br>35-UseTaxEUPurchaseReduced (93/61)          |
| 36  | 95             | 98               | Skattskyld kaup innan bandalags í öðrum skattþrepum                                                                      | 36-EUPurchaseOtherRates</br>36-UseTaxEUPurchaseOtherRates (95/98/61) |
| 37  | 94             | 96               | Skattskyld kaup innan samfélagsins á nýjum bifreiðum frá birgjum sem eru ekki með VSK-númer, með almennu skatthlutfalli. | 37-EUPurchaseVehicles</br>37-UseTaxEUPurchaseVehicles (94/96/61)     |

**HLUTI – RÉTTHAFI SEM SKATTSKULDARI**

| Lína | Reitur – skattstofn | Gluggi – skattupphæð | Lýsing                                                                        | Niðurstaða uppflettingar                                                                                        |
|-----|----------------|------------------|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| 40  | 46             | 47               | Önnur þjónusta frumkvöðuls, sem byggir á því sem eftir er af samfélagsvæðinu.        | 40-BeneficiaryTaxDebtor</br>40-UseTaxBeneficiaryTaxDebtor (46/47/66)                                                                              |
| 41  | 73             | 74               | Sala sem fellur undir hluta 13b (2) nr. 3 af UStG.                               | 41-BeneficiaryTaxDebtorRealEstateTransfer</br>41-UseTaxBeneficiaryTaxDebtorRealEstateTransfer (73/74/67) |
| 42  | 84             | 85               | Önnur þjónusta sem fellur undir hluta 13b (2) nr. 1, 2 og 4 til og með 12 af UStG. | 42-BeneficiaryTaxDebtorOther</br>42-UseTaxBeneficiaryTaxDebtorOther (84/85/67)                           |

**HLUTI – VIÐBÓTARUPPLÝSINGAR UM SÖLU**

| Lína | Reitur – skattstofn  | Gluggi – skattupphæð | Lýsing                                                                                                | Niðurstaða uppflettingar                                                                                    |
|-----|-----------------|------------------|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| 48  | 42              | *Enginn skattupphæð*  | Afhendingar fyrsta viðskiptavinar þegar um er að ræða þríhliða viðskipti innan bandalags.                   | 48-DeliveriesFirstCustomerEUTriangular                                                           |
| 49  | 60              | *Enginn skattupphæð*  | Skattskyld sala frumkvöðulsins sem viðtakandi þjónustunnar skuldar skatt fyrir. | 49-SalesServicesReverseCharge                                                                    |
| 50  | 21              | *Enginn skattupphæð*  | Önnur þjónusta sem ekki er skattskyld.                                                                                | 50-OtherServicesNonTaxable                                                                       |
| 51  | 45              | *Enginn skattupphæð*  | Önnur óskattskyld sala þegar sýningarstaður er ekki í Þýskalandi.                                    | 51-OtherSalesNonTaxable                                                                          |
| 52  | *Enginn skattupphæð* | *Enginn skattupphæð*  | VSK                                                                                                       | Röð 20 + Röð 21 + Röð 22 + Röð 2 + Röð 4 + Röð 34 + Röð 35 + Röð 36 + Röð 37 + Röð 40 + Röð 41 + Röð 42 |

**HLUTI – FRÁDRÁTTARBÆR INNSKATTUR**

| Lína | Gluggi – skattupphæð | Lýsing                                                                                                | Niðurstaða uppflettingar                                                                                                                                                                |
|-----|------------------|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 55  | 66               | Skattupphæðir inntaksreiknings frá öðrum fyrirtækjum, þjónustum og þríhliða viðskiptum innan samfélags.     | 55-InputTax 40-UseTaxBeneficiaryTaxDebtor (46/47/66)</br>74-BadDebtsWriteOffInputTax (66/37) – með mínusmerki                                                                   |
| 56  | 61               | Innskattsupphæðir vegna vörukaupa innan bandalags                                           | 56-InputTaxEUPurchase 34-UseTaxEUPurchaseStandard (89/61)</br>35-UseTaxEUPurchaseReduced (93/61)</br>36-UseTaxEUPurchaseOtherRates (95/98/61)</br>37-UseTaxEUPurchaseVehicles (94/96/61) |
| 57  | 62               | Áfallinn virðisaukaskattur fyrir innflutning.                                                                                 | 57-InputTaxImport                                                                                                                                                            |
| 58  | 67               | Færið inn skattupphæðir vegna þjónustu í skilningi §13b í UStG.                                        | 58-InputTaxServices</br>41-UseTaxBeneficiaryTaxDebtorRealEstateTransfer (73/74/67)</br>42-UseTaxBeneficiaryTaxDebtorOther (84/85/67)                                                 |
| 59  | 63               | Innskattsupphæðir sem eru reiknaðar samkvæmt almennum meðaltöxtum.                                  | 59-InputTaxAverageRates</br>74-BadDebtsWriteOffInputTaxAverageRates (63/37) – með mínusmerki                                                                                    |
| 60  | 59               | Setja inn skattafrádrátt fyrir afhendingar innan bandalags á nýjum bifreiðum nema fyrir fyrirtækið og lítil fyrirtæki. | 60-InputTaxEUPurchaseNewVehicles</br>74-BadDebtsWriteOffInputTaxEUPurchaseNewVehicles (59/37) – með mínusmerki                                                                  |
| 61  | 64               | Leiðrétting á innskattsfrádrætti.                                                                     | 61-InputTaxCorrection                                                                                                                                                        |
| 62  | \-               | Upphæð eftirstöðvanna.                                                                                      | Röð 52 – Röð 55 – Röð 56 – Röð 57 – Röð 58 – Röð 50 – Röð 60 – Röð 61                                                                                                        |

**HLUTI – AÐRAR SKATTUPPHÆÐIR**

| Lína | Gluggi – skattupphæð | Lýsing                                                                                                                                                                                                                                                         | Niðurstaða uppflettingar                                 |
|-----|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| 64  | 65               | Skattur vegna breytinga á formi skattlagningar og viðbótarskattur af skattlögðum afborgunum vegna breytinga á skatthlutfalli.                                                                                                                                        | 64-AdditionalTaxDueChangeTaxRate              |
| 65  | 69               | Rangar eða óréttmætar skattaupphæðir sem koma fram á reikningum og skattaupphæðir sem eru skuldaðar í samræmi við kafla 6a (4) málsgrein 2, kafla 17 (1) málsgrein 7 eða kafla 25b (2) í UStG, eða sem útvistað fyrirtæki eða birgir skuldar. | 65-TaxDecreaseCorrection                      |
| 67  | 39               | Frádráttur sérstakrar fyrirframgreiðslu fyrir varanlega framlengingu. Þessi lína er yfirleitt aðeins fyllt út með síðustu tilkynningu um fyrirframgreiðslu á skattatímabilinu.                                                                                                  | Innsláttarfæribreyta notanda í skýrslusvarglugganum |
| 68  | 83               | Eftirstöðvar fyrirfram VSK-greiðslu og eftirstandandi umframupphæð. Setjið inn mínusmerki fyrir framan upphæðina.                                                                                                                                                          | Lína 62 + Lína 64 – Lína 65 – Lína 66             |

**HLUTI – VIÐBÓTARUPPLÝSINGAR UM LÆKKANIR**

| Lína | Reitur – skattstofn | Gluggi – skattupphæð | Lýsing                                                            | Niðurstaða uppflettingar                                                                                                                                                                                                    |
|-----|----------------|------------------|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 73  | 50             | \-               | Lækkun á skattstofni á línur 20 til og með 24.                      | 73-BadDebtsWriteOffStandard (81/50)</br>73-BadDebtsWriteOffReduced (86/50)</br>73-BadDebtsWriteOffOtherRates (35/36/50)</br>73-BadDebtsWriteOffEUSalesAverageRate24 (77/50)</br>73-BadDebtsWriteOffSalesAverageRate24 (76/80/50) |
| 74  | \-             | 37               | Lækkun frádráttarbærra innskattsfjárhæða í línum 55, 59 og 60. | 74-BadDebtsWriteOffInputTax (66/37)</br>74-BadDebtsWriteOffInputTaxAverageRates (63/37)</br>74-BadDebtsWriteOffInputTaxEUPurchaseNewVehicles (59/37)                                                                     |

#### <a name="purchase-reverse-charge-vat"></a>Innkaup, bakfærður VSK

Ef þú grunnstillir VSK-kóða til að bóka bakfærðan VSK á innleið með því að nota neysluskatt skaltu tengja VSK-kóðana við niðurstöðu uppflettingar í **Uppfletting í skýrslureit** sem inniheldur „UseTax“ í heitinu.

Annars er hægt að grunnstilla tvo aðskilda VSK-kóða: einn fyrir VSK til greiðslu og annan fyrir VSK-frádrátt. Síðan skal tengja hvern kóða við samsvarandi niðurstöður uppflettingar á **Uppfletting í skýrslureit**.

Fyrir skattskyld kaup innan ESB á stöðluðum taxta skal til dæmis grunnstilla VSK-kóðann **UT_S_EU** með neysluskatti og tengja hann við uppflettiniðurstöðuna **34-UseTaxEUPurchaseStandard** í **Uppfletting í skýrslureit**. Í þessu tilviki eru upphæðir sem nota VSK-kóðann **UT_S_EU** sýndar í reitum 089 og 061 (línur 34 og 56).

Einnig getur þú stillt tvo VSK-kóða:

  - **VAT_S_EU**, sem er með -19 prósent skatt
  - **InVAT_S_EU**, sem er með 19 prósent skatt

Kóðana tengir þú svo við niðurstöður uppflettingar í **Uppfletting í skýrslureit** á eftirfarandi hátt:

  - Tengja **VAT_S_EU** við **34-EUPurchaseStandard** niðurstöður uppflettingar.
  - Tengja **InVAT_S_EU** við **56-InputTaxEUPurchase** niðurstöður uppflettingar.

Í þessu tilviki koma upphæðir sem nota VSK-kóðann **VAT_S_EU** fram í glugga 089 (línu 34). Upphæðir sem nota VSK-kóðann **InVAT_S_EU** koma fram í glugga 061 (línu 56).

Frekari upplýsingar um hvernig á að grunnstilla bakfærðan VSK er að finna í [Bakfærð gjöld](emea-reverse-charge.md).

## <a name="configure-system-parameters"></a>Skilgreina kerfisfæribreytur

Til að útbúa VSK-skýrslu verður að skilgreina skattnúmer (Steuernummer) fyrirtækisins.

1. Fara í **Fyrirtækisstjórnun** > **Fyrirtæki** > **Lögaðilar**.
2. Veldu lögaðilann og veldu síðan **Skráningarkenni**.
3. Veldu eða búðu til heimilisfangið í Þýskalandi og svo **Bæta við** á flýtiflipanum **Skráningarkenni**.
4. Í reitnum **Skráningargerð** skal velja skráningargerðina sem tilheyrir Þýskalandi og sem notar skráningarflokkinn **Fyrirtækiskenni (COID)**.
5. Í reitinn **Skráningarnúmer** skal færa inn skattnúmerið.
6. Í flipanum **Almennt**, í reitinn **Gildistími**, skal færa inn dagsetningu þegar númerið tekur gildi.

Frekari upplýsingar um hvernig á að setja upp skráningarflokka og skráningargerðir er að finna í [Skráningarkenni](emea-registration-ids.md).

## <a name="set-up-a-vat-declaration-for-germany"></a>Setja upp VSK-skýrsla fyrir Þýskaland

### <a name="import-er-configurations"></a>Flytja inn rafræn skýrslugerð grunnstillingar

Opnaðu vinnusvæðið **Rafræn skýrslugerð** og flyttu inn eftirfarandi útgáfur eða nýrri af þessum sniðum rafrænnar skýrslugerðar:

   - VSK-skýrsla í Excel (DE).version.101.16.12.xml
   - VSK-skýrsla XML (DE).version.101.16.xml

### <a name="set-up-application-specific-parameters-for-vat-declaration-fields"></a><a name="set-up-application-specific-parameters-for-vat-declaration-fields"></a>Setja upp færibreytur tiltekins forrits fyrir VSK-skýrslureiti

Til að búa sjálfkrafa til VSK-skýrslu skaltu tengja VSK-kóða í forritinu og fletta upp niðurstöðum í skilgreiningu rafrænnar skýrslugerðar.

> [!NOTE]
> Mælt er með að eiginleikinn **Nota sértækar færibreytur fyrir forrit úr fyrri útgáfum ER-sniða** á vinnusvæðinu **Eiginleikastjórnun** sé virkjaður. Þegar þessi eiginleiki er virkjaður verða færibreytur sem eru grunnstilltar fyrir fyrri útgáfu af rafrænu skýrslugerðarsniði sjálfkrafa virkar fyrir síðari útgáfu af sama sniði. Ef þessi eiginleiki er ekki virkur verður þú að grunnstilla færibreytur tiltekins forrits sérstaklega fyrir hverja útgáfu af sniði. Eiginleikinn **Nota sértækar færibreytur fyrir forrit úr fyrri útgáfum ER-sniða** er í boði á vinnusvæðinu **Eiginleikastjórnun** frá og með útgáfu 10.0.23 af Finance. Frekari upplýsingar um hvernig á að setja upp færibreytur á rafrænu skýrslugerðarsniði fyrir hvern lögaðila er að finna í [Setja upp færibreytur á sniði rafrænnar skýrslugerðar fyrir hvern lögaðila](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-set-up.md).

Fylgdu þessum skrefum til að skilgreina hvaða VSK-kóðar búa til hvaða glugga í VSK-skýrslunni.

1. Farið í **Vinnusvæði** > **Rafræn skýrslugerð**, og veljið **Skilgreiningar skýrslugerðar**.
2. Veldu skilgreininguna **VSK-skýrsla í XML (DE)** og veldu síðan **Skilgreiningar \> Uppsetning á færibreytum tiltekins forrits**.
3. Á síðunni **Færibreytur tiltekins forrits**, í flýtiflipanum **Uppflettingar**, skal velja **Uppfletting í skýrslureit**.
4. Í flýtiflipanum **Skilyrði** skal stilla eftirfarandi reiti til að tengja VSK-kóða og skýrslureiti.

    | Svæði                  | Lýsing                                                                                                                                                                                                                                                                                                          |
    |------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Niðurstaða uppflettingar          | Veljið gildi skýrslureitarins. Frekari upplýsingar um gildin og úthlutun þeirra í línum VSK-skýrslu er að finna í hlutanum [Yfirlit VSK-skýrslu](#vat-declaration-overview) fyrr í þessari grein.                                                                                               |
    | Skattkóði               | Veldu VSK-kóðann sem á að tengja við skýrslureitinn. Bókaðar skattfærslur sem nota valinn VSK-kóða verður safnað í viðeigandi skýrsluglugga. Mælt er með að aðskilja VSK-kóðana á þann hátt að einn VSK-kóði búi til upphæðir í aðeins einum skýrsluglugga. |
    | Flokkari færslna | Ef þú bjóst til nógu marga VSK-kóða til að ákvarða skýrsluglugga skaltu velja **\*Ekki autt\***. Ef þú bjóst ekki til nógu marka VSK-kóða þannig að einn VSK-kóði búi til upphæðir í aðeins einum skýrsluglugga er hægt að setja upp færsluflokkara. Eftirfarandi færsluflokkarar eru í boði:</br>-   **Innkaup**</br>-   **PurchaseExempt** (skattfrjáls kaup)</br>-   **PurchaseReverseCharge**(innskattur af bakfærslu innkaupa)</br>-   **Sala**</br>-   **SalesExempt** (skattfrjáls sala)</br>-   **SalesReverseCharge** (gjaldfallinn skattur úr bakfærðu gjaldi kaupa eða sölu)</br>-   **Nota skatt**. </br>Fyrir hvern færsluflokkara er flokkari fyrir kreditnótuna líka í boði. Til dæmis er einn þessara flokkara **PurchaseCreditNote** (innkaupakreditnóta).</br>Gættu þess að stofna tvær línur fyrir hvern VSK-kóða: eina sem er með gildi færsluflokkara og eina sem er með færsluflokkara fyrir gildi kreditnótu. |

    > [!NOTE]
    > Tengdu alla VSK-kóða við niðurstöður uppflettingar. Ef einhverjir VSK-kóðar mynda ekki gildi í VSK-skýrslunni skal tengja þá við uppflettiniðurstöðuna **Annað**.

    ![Síða sértækra færibreyta fyrir forrit](media/69ecb881f12819259ca166b9b98b8303.jpg)

5. Í reitnum **Staða** skal breyta gildinu í **Lokið**.
6. Á aðgerðasvæðinu skal velja **Flytja út** til að flytja út stillingar færibreyta tiltekins forrits.
7. Veldu skilgreininguna **VSK-skýrsla í Excel (DE)** og síðan á aðgerðasvæðinu skal velja **Flytja inn** til að flytja inn færibreyturnar sem voru skilgreindar fyrir **VSK-skýrsla í XML (DE)**.
8. Í reitnum **Staða** skal velja **Lokið**.

### <a name="set-up-the-vat-reporting-format-for-preview-amounts-in-excel"></a>Setja upp snið VSK-skýrslu til að forskoða upphæðir í Excel

1. Á vinnusvæðinu **Eiginleikastjórnun** skaltu finna og virkja eiginleikann **Skýrslugerð VSK-yfirlita**.
2. Opnið **Fjárhagur** > **Uppsetning**  >  **Færibreytur fyrir fjárhag**.
3. Í flipanum **Virðisaukaskattur**, í flýtiflipanum **Valkostir skatts**, í reitnum **Sniðsvörpun VSK-skýrslu**, skal velja **VSK-skýrsla Excel (DE)**.

   Þetta snið er prentað þegar skýrslan **Gefa upp virðisaukaskatt fyrir jöfnunartímabil** er keyrð. Það er einnig prentað þegar **Prenta** er valið á síðunni **VSK-greiðslur**.

4. Ef tilkynna þarf leiðréttingarnar skal í hlutanum **Sérstök skýrsla** stilla **Taka með leiðréttingar** á **Já**.
5. Á síðunni **Skattayfirvöld** skal velja skattayfirvöld og í reitnum **Útlit skýrslu** skal velja **Sjálfgefið**.

Ef VSK-skýrsla er skilgreind í lögaðila sem er með [margar VSK-skráningar](emea-reporting-for-multiple-vat-registrations.md) skal fylgja þessum skrefum:

1. Opnið **Fjárhagur** > **Uppsetning**  >  **Færibreytur fyrir fjárhag**.
2. Í flipanum **Virðisaukaskattur**, í flýtiflipanum **Rafræn skýrslugerð fyrir lönd/svæði**, í línunni fyrir **DEU**, skal velja rafræna skýrslugerðarsniðið **VSK-skýrsla í Excel (DE)**.

## <a name="set-up-electronic-messages"></a>Setja upp rafræn skilaboð

### <a name="download-and-import-the-data-package-that-has-example-settings-for-electronic-messages"></a>Sækja og flytja inn gagnapakkann sem er með dæmastillingar fyrir rafræn skilaboð

Gagnapakkinn inniheldur stillingar rafrænna skilaboða sem eru notaðar til að útbúa VSK-skýrsluna á XML-sniði og síðan forskoða hana í Excel. Þú getur notað þessar stillingar eða búið til þínar eigin. Frekari upplýsingar um hvernig á að vinna með rafræn skilaboð og búa til sínar eigin stillingar er að finna í [Rafræn skilaboð](../general-ledger/electronic-messaging.md).

1. Í [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/v2), í samnýttu eignasafni, skal velja **Gagnapakka** sem eignagerð og sækja svo **DE EM-pakka VSK-skýrslu**. Skráarheitið sem er sótt er **DE VAT Statement EM package.zip**.
2. Á vinnusvæðið **Gagnastjórnun** í Dynamics 365 Finance skal velja **Innflutningur**.
3. Í flýtiflipann **Flytja inn**, í reitinn **Heiti hóps**, skal færa inn heiti fyrir verkið.
4. Á flýtiflipanum **Valdar einingar** skal velja **Bæta við skrá**.
5. Í svarglugganum **Bæta við skrá** skal staðfesta að reiturinn **Snið upprunagagna** sé stilltur á **Pakki**, velja **Hlaða upp og bæta við** og velja svo zip-skrána sem var sótt áður.
6. Veljið **Loka**.
7. Þegar gagnaeiningunum er hlaðið upp skal á aðgerðasvæðinu velja **Flytja inn**.
8. Opnið **Skattur**  >  **Fyrirspurnir og skýrslur**  >  **Rafræn skilaboð**  >  **Rafræn skilaboð** og staðfestið vinnslu rafrænna skilaboða sem flutt voru inn.

### <a name="configure-electronic-messages"></a>Skilgreina rafræn skilaboð

1. Opnið **Skattur**  >  **Uppsetning**  >  **Rafræn skilaboð**  >  **Fylla út færsluaðgerðir**.
2. Veldu línuna fyrir **DE Fylla út færslur VSK-skila** og síðan velja **Breyta fyrirspurn**.
3. Notaðu síuna til að tilgreina jöfnunartímabil sem á að hafa með í skýrslunni.
4. Ef tilkynna þarf skattfærslur frá öðrum jöfnunartímabilum í annarri skýrslu skal búa til nýja aðgerð fyrir **Fylla út færslur** og velja viðeigandi jöfnunartímabil.

## <a name="preview-the-vat-declaration-in-excel"></a>Forskoða VSK-skýrsluna í Excel

### <a name="preview-the-vat-declaration-in-excel-from-the-report-sales-tax-for-settlement-period-periodic-task"></a>Forskoða VSK-skýrsluna í Excel úr „Gefa upp virðisaukaskatt“ fyrir reglubundið verk jöfnunartímabils

1. Opna **Skattur** > **Reglubundin verkefni** > **Skattframtöl** > **Virðisaukaskattur** > **Virðisaukaskattsskýrsla fyrir jöfnunartímabil**.
2. Veljið gildi í reitnum **Jöfnunartímabil**.
3. Í reitnum **Útgáfa VSK-greiðslu** skal velja eitt eftirfarandi gilda:

    - **Upprunalegt**: Búðu til skýrslu fyrir VSK-færslur upprunalegrar VSK-greiðslu eða áður en VSK-greiðslan er mynduð.
    - **Leiðréttingar**: Búðu til skýrslu fyrir VSK-færslur fyrir allar komandi VSK-greiðslur fyrir tímabilið.
    - **Heildarlisti**: Búðu til skýrslu fyrir allar VSK-færslur fyrir tímabilið, þ.m.t. upprunalegt og allar leiðréttingar.

4. Í reitnum **Frá dagsetningu** velurðu upphafsdagsetningu skýrslutímabilsins.
5. Veldu **Í lagi** og farðu yfir Excel-skýrsluna.

### <a name="settle-and-post-sales-tax"></a><a name="settle-and-post-sales-tax"></a>Jafna og bóka virðisaukaskatt

1. Farið í **Skattur** > **Reglubundin verkefni** > **Skattskýrslur** > **Virðisaukaskattur** > **Jafna og bóka VSK**.
2. Veljið gildi í reitnum **Jöfnunartímabil**.
3. Í reitnum **Útgáfa VSK-greiðslu** skal velja eitt eftirfarandi gilda:

    - **Upprunalegt**: Búðu til upprunalega VSK-greiðslu fyrir jöfnunartímabilið.
    - **Nýjustu leiðréttingar**: Búðu til leiðréttingu á VSK-greiðslur eftir að upprunaleg VSK-greiðsla fyrir jöfnunartímabilið var búin til.

4. Í reitnum **Frá dagsetningu** velurðu upphafsdagsetningu skýrslutímabilsins.
5. Veldu **Í lagi**.

### <a name="preview-the-vat-declaration-in-excel-from-a-sales-tax-payment"></a>Forskoða VSK-skýrsluna í Excel úr VSK-greiðslu

1. Opnaðu **Skattur** > **Fyrirspurnir og skýrslur** > **Fyrirspurnir um virðisaukaskatt** > **Greiðslur virðisaukaskatts** og veldu greiðslulínu virðisaukaskatts.
2. Veldu **Prenta skýrslu** og veldu síðan **Í lagi**.
3. Farðu yfir Excel-skrána sem er búin til fyrir valda VSK-greiðslulínu.

    > [!NOTE]
    > Skýrslan er aðeins gerð fyrir valda línu VSK-greiðslunnar. Ef þú verður til dæmis að búa til leiðréttingarskýrslu sem inniheldur allar leiðréttingar fyrir tímabilið eða staðgengilsskýrslu sem inniheldur upprunaleg gögn og allar leiðréttingar skaltu nota reglubundna verkið **Gefa upp virðisaukaskatt fyrir jöfnunartímabil**.

## <a name="generate-a-vat-declaration-from-electronic-messages"></a>Búa til VSK-skýrslu úr rafrænum skilaboðum

Þegar þú notar rafræn skilaboð til að búa til skýrsluna geturðu safnað skattgögnum frá mörgum lögaðilum. Frekari upplýsingar er að finna í hlutanum [Keyra VSK-skýrslu fyrir marga lögaðila](#run-a-vat-declaration-for-multiple-legal-entities) síðar í þessari grein.

Eftirfarandi ferli á við um dæmi um vinnslu rafrænna skilaboða sem þú fluttir inn úr LCS samnýttu eignasafni.

1. Opnið **Skattur**  >  **Fyrirspurnir og skýrslur**  >  **Rafræn skilaboð**  >  **Rafræn skilaboð**.
2. Veljið **DE VSK-skýrsla** í vinstra svæðinu.
3. Í flýtiflipanum **Skilaboð** skal velja **Nýtt** og síðan í svarglugganum **Keyra vinnslu** skal velja **Í lagi**.
4. Veldu skilaboðalínuna sem er búin til, sláðu inn lýsingu og tilgreindu svo upphafs- og lokadagsetningar fyrir skýrsluna.

    > [!NOTE]
    > Skref 5 til 7 eru valfrjáls.

5. Valfrjálst: Í flýtiflipanum **Skilaboð** skal velja **Safna gögnum** og velja síðan **Í lagi**. VSK-greiðslurnar sem voru gerðar áður er bætt við skilaboðin. Frekari upplýsingar er að finna í hlutanum [Jafna og bóka virðisaukaskatt](#settle-and-post-sales-tax) fyrr í þessari grein. Ef þú sleppir þessu skrefi geturðu samt búið til VSK-skýrslu með því að nota reitinn **Útgáfa skattskýrslu** í svarglugganum **Skýrsla**.
6. Valfrjálst: Í flýtiflipanum **Skilaboðaatriði** skal yfirfara VSK-greiðslur sem fluttar eru til vinnslu. Allar VSK-greiðslur á völdu tímabili sem voru ekki hafðar með í neinum öðrum skilaboðum sömu vinnslunnar eru sjálfgefið hafðar með.
7. Valfrjálst: Veldu **Upprunalegt skjal** til að yfirfara VSK-greiðslur eða veldu **Eyða** til að útiloka VSK-greiðslur frá vinnslu. Ef þú sleppir þessu skrefi geturðu samt búið til VSK-skýrslu með því að nota reitinn **Útgáfa skattskýrslu** í svarglugganum **Skýrsla**.
8. Í flýtiflipanum **Skilaboð** skal velja **Uppfæra stöðu**. Í svarglugganum **Uppfæra stöðu** skal velja **Tilbúið til myndunar** og síðan velja **Í lagi**. Staðfestu að stöðu skilaboðanna sé breytt í **Tilbúin til að mynda**.
9. Veldu **Búa til skýrslu**. Til að forskoða upphæðir VSK-skýrslu skal í svarglugganum **Keyra vinnslu** velja **Forskoða skýrslu** og síðan velja **Í lagi**.
10. Í svarglugganum **Rafrænar skýrslugerðarfæribreytur** skal stilla eftirfarandi reiti og velja síðan **Í lagi**.

    | **Svæði**                                   | **Lýsing**                                                                                                                                                                                                              |
    |---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Jöfnunartímabil                           | Veljið jöfnunartímabil. Ef **Safna gögnum** var valið í skrefi 5 er hægt að skilja þetta svæði eftir autt. Skýrslan verður gerð fyrir VSK-færslur sem eru innifaldar í innheimtum VSK-greiðslum. |
    | Útgáfa skattskýrslu                     | Veljið eitt af eftirfarandi gildum:</br>-   **Upprunalegt** – Búðu til skýrslu fyrir VSK-færslur upprunalegrar VSK-greiðslu eða áður en VSK-greiðslan er mynduð.</br>-   **Leiðréttingar** – Búðu til skýrslu fyrir VSK-færslur fyrir allar komandi VSK-greiðslur fyrir tímabilið.</br>-   **Heildarlisti** – Búðu til skýrslu fyrir allar VSK-færslur fyrir tímabilið, þ.m.t. upprunalegt og allar leiðréttingar.|
    | Skattfulltrúi | Veldu aðila sem er skattalegur fulltrúi fyrir VSK-skýrslu, ef við á. Upplýsingar um valinn aðila eru fluttar út XML-eininguna **DatenLieferant**. |
    | Tengiliður | Veljið einstakling innan stofnunarinnar/fyrirtækisins sem er gagnaveita. Upplýsingar um valdan aðila eru fluttar út XML-eininguna **DatenLieferant**. |
    | Leiðrétt skil | Veljið **Já** ef um leiðrétta VSK-skýrslu er að ræða. Í þessu tilviki mun XML þáttur KZ10 hafa gildið **1**.|
    | Stuðningsskjöl | Velja skal **Já** ef einnig eru send stuðningsgögn. Í þessu tilviki mun XML þáttur KZ22 hafa gildið **1**.|
    | SEPA-umboð fyrir beingreiðslu verður afturkallað sem undantekning| Veljið **Já** ef SEPA-umboð fyrir beingreiðslu verður afturkallað sem undantekning fyrir þetta forskráningartímabil. Til dæmis vegna mótfærslubeiðna. Eftirstöðvar á að greiða sérstaklega. Í þessu tilviki mun XML þáttur KZ26 hafa gildið **1**. |
    | Mótfærsla á endurgreiðsluupphæðarinnar sem óskað er eftir | Veldu **Já** ef mótbóka á endurgreiðsluupphæð sem vantar eða ef endurgreiðsluupphæðinni hefur verið úthlutað. Í þessu tilviki mun XML þáttur KZ29 hafa gildið **1**. |
    | Sérstök fyrirframgreiðsla varanlegrar framlengingar | Færið inn upphæð frádráttar fastrar sérstakrar fyrirframgreiðslu fyrir varanlega framlengingu. Þessari frádráttarupphæð er yfirleitt aðeins lokið í síðustu forskráningu skattatímabils Upphæðin er flutt út í línu 67 (reitur 39) og XML-einingu KZ39 VSK-skýrslu. |

11. Veljið **Viðhengi** efst í hægra horninu á síðunni og veljið síðan **Opna**.
12. Farið yfir upphæðir í Excel-skjalinu og veljið síðan **Mynda skýrslu**.
13. Til að búa til VSK-skýrslu á XML-sniði skal velja svargluggann **Keyra vinnslu**, velja **Búa til skýrslu** og síðan velja **Í lagi**.
14. Í svarglugganum **Rafrænar skýrslugerðarfæribreytur** skal stilla reitina eins og lýst er í skrefi 10.
15. Veldu **Viðhengi** efst til hægri á síðunni, sæktu skrána og notaðu hana þegar þú sendir inn til skattayfirvalda.

## <a name="run-a-vat-declaration-for-multiple-legal-entities"></a><a name="run-a-vat-declaration-for-multiple-legal-entities"></a>Keyra VSK-skýrslu fyrir marga lögaðila

Til að nota sniðin til að gefa upp VSK-skýrsluna fyrir hóp af lögaðilum þarf fyrst að setja upp forritstengdar færibreytur rafræna skýrslugerðarsniðanna fyrir VSK-kóða frá öllum nauðsynlegum lögaðilum.

### <a name="set-up-electronic-messages-to-collect-tax-data-from-several-legal-entities"></a>Setja upp rafræn skilaboð til að safna skattgögnum frá nokkrum lögaðilum

Fylgdu þessum skrefum til að setja upp rafræn skilaboð sem safna gögnum frá mörgum lögaðilum.

1. Opnið **Vinnusvæði** > **Eiginleikastjórnun**.
2. Finndu og veldu eiginleikann **Fyrirspurnir milli fyrirtækja fyrir fyllingu færsluaðgerða** í listanum og veldu síðan **Virkja núna**.
3. Opnið **Skattur**  >  **Uppsetning**  >  **Rafræn skilaboð \> Fylla út færsluaðgerðir**.
4. Á síðunni **Fylla út færsluaðgerð** skal velja línuna fyrir **DE Fylla út VSK-skilafærslu**.

   Í hnitanetinu **Uppsetning gagnagjafa** er nýr reitur fyrir **Fyrirtæki** í boði. Fyrir fyrirliggjandi færslur sýnir þessi reitur auðkenni núverandi lögaðila.

5. Í hnitanetinu **Uppsetning gagnagjafa** skal bæta við línu fyrir hvern aukalegan lögaðila sem á að vera í skýrslugjöfinni. Fyrir hverja nýja línu skal stilla eftirfarandi reiti:

    | Svæði                  | Lýsing                                                                                                                   |
    |------------------------|-------------------------------------------------------------------------------------------------------------------------------|
    | Nafn                   | Sláðu inn gildi sem hjálpar þér að skilja hvaðan þessi færsla kemur. Sláðu til dæmis inn **VSK-greiðsla dótturfyrirtækis 1**. |
    | Gerð skilaboðaatriðis      | Veljið **VSK-endurgreiðslu**. Þetta gildi er eina gildið sem er í boði fyrir allar færslunar.                                    |
    | Lykilgerð           | Velja **Allt**                                                                                                               |
    | Aðaltöfluheiti      | Tilgreinið **TaxReportVoucher** fyrir allar færslurnar.                                                                             |
    | Reitur skjalnúmers  | Tilgreinið **Fylgiskjal** fyrir allar færslurnar.                                                                                      |
    | Dagsetningarreitur skjals    | Tilgreina **TransDate** fyrir allar færslur.                                                                                    |
    | Reikningsreitur skjals | Tilgreinið **TaxPeriod** fyrir allar færslurnar.                                                                                    |
    | Fyrirtæki                | Veljið auðkenni lögaðilans.                                                                                            |
    | Fyrirspurn notanda             | Þessi gátreitur er valinn sjálfkrafa þegar þú skilgreinir skilyrði með því að velja **Breyta fyrirspurn**.                                 |

6. Fyrir hverja nýja línu skal velja **Breyta fyrirspurn** og tilgreina tengt jöfnunartímabil sem á við um lögaðilann sem er tilgreindur í reitnum **Fyrirtæki** í línunni.

Þegar uppsetningunni er lokið safnar aðgerðin **Safna gögnum** á síðunni **Rafræn skilaboð** VSK-greiðslum frá öllum lögaðilum sem eru skilgreindir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
