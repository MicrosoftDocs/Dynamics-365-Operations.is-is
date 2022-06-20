---
title: VSK yfirlýsing (Danmörk)
description: Þessi grein lýsir því hvernig á að setja upp og búa til fyrirfram virðisaukaskattsskýrslu (VSK) fyrir Danmörku.
author: anasyash
ms.date: 03/10/2022
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: ''
ms.openlocfilehash: 666dc96cb169ab28ac3938299a3f245e3b4511ab
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863000"
---
# <a name="vat-declaration-denmark"></a>VSK yfirlýsing (Danmörk)

[!include [banner](../includes/banner.md)]

Þessi grein lýsir því hvernig á að setja upp virðisaukaskattsskýrslu (VSK) fyrir Danmörku og forskoða hana í Microsoft Excel.

Til að búa til skýrsluna sjálfkrafa skaltu fyrst búa til nógu marga VSK-kóða til að halda sérstakt VSK bókhald fyrir hvern reit á fyrirfram VSK yfirlýsingunni. Að auki, í forritssértækum færibreytum rafrænnar skýrslugerðar (ER) sniðs fyrir fyrirfram VSK yfirlýsingu, tengja virðisaukaskattskóða við uppflettingarniðurstöðu uppflettanna fyrir reitina á VSK yfirlýsingunni.

Fyrir Danmörku verður þú að stilla **Tilkynna reiti leit**. Fyrir frekari upplýsingar um hvernig á að setja upp forritssértækar færibreytur, sjá [Settu upp forritssértækar færibreytur fyrir VSK-yfirlýsingareiti](#set-up-application-specific-parameters) kafla síðar í þessari grein.

Í eftirfarandi töflu sýnir dálkurinn „Upplitsniðurstaða“ uppflettingarniðurstöðuna sem er forstillt fyrir tiltekna virðisaukaskattsyfirlýsingarlínu á sniði VSK-yfirlýsingarinnar. Notaðu þessar upplýsingar til að tengja virðisaukaskattskóða rétt við uppflettingarniðurstöðuna og síðan við línuna í virðisaukaskattsskýrslunni.

### <a name="vat-declaration-overview"></a>Yfirlit yfir virðisaukaskattsskýrslu

VSK yfirlýsingin í Danmörku inniheldur eftirfarandi upplýsingar.

**VAT til greiðslu**

| Lýsing                                                  | Skattstofn/skattfjárhæð | Uppflettingarniðurstaða/Total                                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Útskattur                                                   | Skattupphæð          | **Úttaksvirðisaukaskattur**</br> **Innlend VATUskattur** (einnig tilkynnt í reitnum „VSK“)                                                                                                                                                                                                                                                                       |
| Virðisaukaskattur af vörum o.fl. Keypt erlendis                           | Skattupphæð          | **Kaupa vörur erlendis**</br>**Kaupa vörur erlendis Notaskattur** (einnig tilkynnt í reitnum „VSK“)</br>**PurchaseGoodsEU** (Skattstofninn er skráður í "Rammi A - vöruöflun.")</br>**PurchaseGoodsEUUseTax** (Skattupphæðin er einnig gefin upp í reitnum „VSK“. Skattstofninn er skráður í "reitur A - vöruöflun.")                   |
| VSK af þjónustu sem keypt er erlendis og kann að falla undir bakfærð gjöld | Skattupphæð          | **InnkaupaþjónustaErlendis**</br> **InnkaupaþjónustaErlendis Notaskattur** (einnig tilkynnt í reitnum „VSK“)</br>**PurchaseServicesEU** (Skattstofninn er skráður í "Rammi A - öflun þjónustu.")</br>**InnkaupaþjónustaEUUseTax** (Skattupphæðin er einnig gefin upp í reitnum „VSK“. Skattstofninn er tilgreindur í "reitur A - þjónustuöflun.") |
| Samtals til greiðslu                                                | Skattupphæð          | Samtals þrjár fyrri kassarnir                                                                                                                                                                                                                                                                                                            |

**Frádráttur**

| Lýsing                                                                               | Skattstofn/skattfjárhæð | Uppflettingarniðurstaða/Total                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Innskattur                                                                                 | Skattupphæð          | **Inntaksvirðisaukaskattur**</br> **Innlend VATUskattur** (einnig tilkynnt í reitnum „Framtaksvirðisaukaskattur“)</br>**Kaupa vörur erlendis Notaskattur** (einnig greint frá í „VSK á vörur o.fl. Keypt erlendis“ kassi)</br>**InnkaupaþjónustaErlendis Notaskattur** (einnig tilgreint í reitnum „VSK af þjónustu sem keypt er erlendis með öfuggreiðslu“)</br>**PurchaseGoodsEUUseTax** (einnig greint frá í „VSK á vörur o.fl. Keypt erlendis“ kassi)</br> **InnkaupaþjónustaEUUseTax** (einnig tilgreint í reitnum „VSK af þjónustu sem keypt er erlendis með öfuggreiðslu“) |
| Gjald fyrir olíu og fljótandi jarðolíugas                                                                  | Skattupphæð          | **OilGasDuty**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Gjald fyrir jarðgas og veitugas                                                             | Skattupphæð          | **NaturalTownGasDuty**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Kolefnisgjald                                                                               | Skattupphæð          | **CarbonDuty**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| CO2-skylda                                                                                   | Skattupphæð          | **CO2-skylda**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Vatnsgjald                                                                              | Skattupphæð          | **WaterCharge**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Samtals frádráttur                                                                          | Skattupphæð          | Samtals fyrri sex kassar                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Heildarupphæð gjalda (plústala = ganga frá greiðslu, mínustala = fá endurgreiðslu) | Skattupphæð          | "Heildar til greiðslu" - "Heildarfrádráttur"                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |

**Viðbótarupplýsingar**

| Lýsing                                                                                                                                                                                                                                | Skattstofn/skattfjárhæð | Uppflettingarniðurstaða/Total                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|-------------------------------------------------|
| Reitur A - vöruöflun. Verðmæti án virðisaukaskatts af vörukaupum innan sambandsins.                                                                                                                                                   | Skattstofn            | **PurchaseGoodsEU PurchaseGoodsEUUseTax**       |
| Reitur A - öflun þjónustu. Verðmæti án virðisaukaskatts af öflun þjónustu innan sambandsins.                                                                                                                                             | Skattstofn            | **Innkaupaþjónusta ESB Innkaupaþjónusta ESBNota Skattur** |
| Reitur B - vöruframboð - skal tilkynna til "ESB-sala án VSK"/DK VIES. Verðmæti vöruafhendingar innan Sambandsins án virðisaukaskatts                                                                                                           | Skattstofn            | **SalesGoodsEU**                                |
| Reitur B - vistir - ekki tilkynnt til "ESB-sala án VSK"/DK VIES. Verðmæti án virðisaukaskatts af tilteknum vörum innan sambandsins, td uppsetningar, samsetningar, fjarsölu og nýrra flutningatækja til óskattskyldra aðila. | Skattstofn            | **Sala Uppsetning Assembly EtcEU**              |
| Reitur B - framboð á þjónustu. Verðmæti án virðisaukaskatts af þjónustu innan Sambandsins sem kaupandi ber að greiða virðisaukaskatt fyrir sem öfug gjaldfærslu - verður einnig að tilkynna til "ESB-sala án virðisaukaskatts"/DK VIES.                          | Skattstofn            | **Söluþjónusta ESB**                             |
| Askja C - aðrar vistir. Verðmæti afhendingar á öðrum vörum og þjónustu sem er afhent án virðisaukaskatts á yfirráðasvæði Danmerkur, til annarra aðildarríkja ESB og til þriðju landa eða þriðju landsvæði.                                     | Skattstofn            | **Aðrar birgðir Án vsk**                     |

#### <a name="purchase-reverse-charge-vat"></a>Kaupa öfug gjaldfærslu VSK

Ef þú stillir VSK-kóða til að bóka innkominn bakfærsla VSK með því að nota notkunarskatt skaltu tengja VSK-kóðana þína við uppflettingarniðurstöðuna fyrir **Tilkynna reiti leit** sem inniheldur "UseTax" í nafninu.

Að öðrum kosti er hægt að stilla tvo aðskilda söluskattskóða: einn fyrir virðisaukaskatt sem ber að greiða og einn fyrir virðisaukaskattsfrádrátt. Tengdu síðan hvern kóða við samsvarandi leitarniðurstöður fyrir **Tilkynna reiti leit**.

Til dæmis, fyrir skattskyldar yfirtökur innan samfélags, stillir þú söluskattskóða **UT_S_EU** með afnotaskatti og tengja það við **PurchaseGoodsEUUseTax** uppflettingarniðurstaða af **Tilkynna reiti leit**. Í þessu tilviki, skattfjárhæðir sem nota **UT_S_EU** VSK-kóði kemur fram í „VSK á vörur o.fl. Keypt erlendis" og "Inntaks VSK" kassa. Skattstofnar endurspeglast í "Kassi A - kaup á vörum."

Að öðrum kosti stillirðu tvo VSK-kóða:

- **VAT_S_EU**, sem hefur skatthlutfallsgildi upp á -25 prósent
- **InVAT_S_EU**, sem hefur skatthlutfallsgildi 25 prósent

Þú tengir síðan kóðana við uppflettingarniðurstöður af **Tilkynna reiti leit** á eftirfarandi hátt:

- Félagi **VAT_S_EU** með **PurchaseGoodsEU** uppflettingarniðurstöðu.
- Félagi **InVAT_S_EU** með **Inntaksvirðisaukaskattur** uppflettingarniðurstöðu.

Í þessu tilviki, upphæðir sem nota **VAT_S_EU** VSK-kóði kemur fram í „VSK á vörur o.fl. Keypt í útlöndum" kassa og "reitur A - vöruöflun." Upphæðir sem nota **InVAT_S_EU** VSK-kóði endurspeglast í reitnum „VSK“.

Frekari upplýsingar um hvernig á að stilla öfuga gjaldfærslu VSK, sjá [Andstæðar gjaldtökur](emea-reverse-charge.md).

## <a name="configure-system-parameters"></a>Stilla kerfisfæribreytur

Til að búa til virðisaukaskattsyfirlýsingu verður þú að stilla virðisaukaskattsnúmerið.

1. Fara í **Fyrirtækisstjórnun** > **Fyrirtæki** > **Lögaðilar**.
2. Veldu lögaðilann og veldu síðan **Skráningarauðkenni**.
3. Veldu eða búðu til heimilisfangið í Danmörku og síðan á **Skráningarauðkenni** Flýtiflipi, veldu **Bæta við**.
4. Í **Skráningartegund** reit, veldu skráningartegundina sem er tileinkuð Danmörku og sem notar **VSK auðkenni** skráningarflokk.
5. Í **Skráningarnúmer** reit, sláðu inn skattnúmerið.
6. Á **Almennt** flipa, í **Árangursrík** reit, sláðu inn dagsetninguna þegar númerið tekur gildi.

Fyrir frekari upplýsingar um hvernig á að setja upp skráningarflokka og skráningargerðir, sjá [Skráningarauðkenni](emea-registration-ids.md).

## <a name="set-up-a-vat-declaration-preview-for-denmark"></a>Settu upp forskoðun virðisaukaskattsskýrslu fyrir Danmörku

### <a name="import-er-configurations"></a>Flytja inn rafræn skýrslugerð grunnstillingar

Opnaðu **Rafræn skýrslugerð** vinnusvæði, og flytja inn **VSK yfirlýsing Excel (DK)** ER snið.

Frekari upplýsingar er að finna í [Sækja skilgreiningar rafrænnar skýrslugerðar úr altækri geymslu skilgreiningarþjónustu](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

### <a name="set-up-application-specific-parameters-for-vat-declaration-fields"></a><a name="set-up-application-specific-parameters"></a> Settu upp forritssértækar færibreytur fyrir VSK-yfirlýsingareiti

> [!NOTE]
> Við mælum með að þú kveikir á eiginleikanum, **Notaðu forrita sérstakar færibreytur frá fyrri útgáfum af ER sniðum** í **Eiginleikastjórnun** vinnurými. Þegar þessi eiginleiki er virkur verða færibreytur sem eru stilltar fyrir fyrri útgáfu af ER-sniði sjálfkrafa gildar fyrir síðari útgáfu af sama sniði. Ef þessi eiginleiki er ekki virkur verður þú að stilla forritssértækar færibreytur sérstaklega fyrir hverja sniðútgáfu. The **Notaðu forrita sérstakar færibreytur frá fyrri útgáfum af ER sniðum** eiginleiki er fáanlegur í **Eiginleikastjórnun** vinnusvæði sem byrjar í Finance útgáfu 10.0.23. Fyrir frekari upplýsingar um hvernig á að setja upp færibreytur ER sniðs fyrir hvern lögaðila, sjá [Settu upp færibreytur ER sniðs fyrir hvern lögaðila](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-set-up.md).

Til að búa til virðisaukaskattsyfirlýsingu sjálfkrafa skaltu tengja söluskattskóða í forritinu og leitarniðurstöður í ER uppsetningu.

Fylgdu þessum skrefum til að skilgreina hvaða VSK-kóðar búa til hvaða reiti á VSK-yfirlýsingunni.

1. Fara til **Vinnurými** > **Rafræn skýrslugerð**, og veldu **Skýrslustillingar**.
2. Veldu **VSK yfirlýsing Excel (DK)** stillingar og veldu síðan **Stillingar \> Uppsetning á sérstökum breytum fyrir forrit**.
3. Á **Sértækar breytur fyrir forrit** síðu, á **Uppflettingar** Flýtiflipi, veldu **Tilkynna reiti leit**.
4. Á **Skilyrði** Flýtiflipi, stilltu eftirfarandi reiti til að tengja vsk-kóða og skýrslureit.

    | Reitur                  | Lýsing                                                                                                                                                                                                                                                                                                          |
    |------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Niðurstaða uppflettingar          | Veldu gildi skýrslureitsins. Nánari upplýsingar um gildin og úthlutun þeirra á lína VSK-skýrslu er að finna í [Yfirlit yfir virðisaukaskattsskýrslu](#vat-declaration-overview) kafla fyrr í þessari grein.                                                                                               |
    | Skattkóði               | Veldu VSK-kóðann sem á að tengja við skýrslureitinn. Bókaðar skattfærslur sem nota valda vsk-kóðann verða safnað í viðeigandi framtalsreit. Við mælum með að þú aðskiljir vsk-kóða á þann hátt að einn vsk-kóði myndar upphæðir í aðeins einum framtalsreit. |
    | Færsluflokkari | Ef þú bjóst til nógu marga VSK-kóða til að ákvarða framtalsreit skaltu velja **\* Ekki autt\***. Ef þú bjóst ekki til nógu marga VSK-kóða þannig að einn VSK-kóði myndar upphæðir í aðeins einum framtalareit, geturðu sett upp færsluflokkara. Eftirfarandi færsluflokkar eru fáanlegir:</br>-   **Innkaup**</br>-   **Undanþegin kaup** (skattfrjálst kaup)</br>-   **PurchaseReverseCharge** (skattur af öfugri gjaldfærslu)</br>-   **Sala**</br>-   **Undanþegin sölu** (skattfrjáls sala)</br>-   **SalesReverseCharge** (skattur sem greiddur er af öfugri greiðslu eða öfugri sölu)</br>-   **Notaðu skatt**. </br>Fyrir hvern færsluflokkara er einnig tiltækur flokkari fyrir kreditnótu. Til dæmis er einn af þessum flokkunaraðilum **PurchaseCreditNote** (kaupinneignarnóta).</br>Vertu viss um að búa til tvær línur fyrir hvern VSK-kóða: eina sem hefur færsluflokkunargildið og eina sem hefur færsluflokkarann fyrir kreditnótugildi. |


    > [!NOTE]
    > Tengja alla söluskattskóða við uppflettingarniðurstöður. Ef einhverjir söluskattskóðar ættu ekki að mynda gildi á virðisaukaskattsskýrslunni skaltu tengja þá við **Annað** uppflettingarniðurstöðu.

    ![Síða sértækra færibreyta fyrir forrit.](media/7db74920fad66a0db7fad60758698cc0.png)


5. Í **Ríki** reit, breyttu gildinu í **Lokið**.

### <a name="set-up-the-vat-reporting-format-for-preview-amounts-in-excel"></a>Settu upp VSK-skýrslusnið fyrir forskoðunarupphæðir í Excel

1. Í **Eiginleikastjórnun** vinnusvæði, finndu og veldu **Skýrslur á sniði VSK-yfirlits.** Eiginleiki á listanum og veldu síðan **Virkja núna**.
2. Fara til **Aðalbók** > **Uppsetning** > **Fjárhagsfæribreytur**.
3. Á **Söluskattur** flipa, á **Skattavalkostir** flýtiflipann, í **Sniðkortlagning virðisaukaskattsyfirlits** reit, veldu **VSK yfirlýsing Excel (DK)** ER snið.

   Þetta snið er prentað þegar þú keyrir **Tilkynna söluskatt fyrir uppgjörstímabil** skýrslu. Það er líka prentað þegar þú velur **Prenta** á **Söluskattsgreiðslur** síðu.

4. Á **Skattayfirvöld** síðu, veldu skattyfirvöld og síðan í **Skýrsluskipulag** reit, veldu **Sjálfgefið**.

Ef þú ert að stilla virðisaukaskattsyfirlýsinguna í lögaðila sem hefur [margar virðisaukaskattsskráningar](emea-reporting-for-multiple-vat-registrations.md), fylgdu þessum skrefum.

1. Fara til **Aðalbók** \> **Uppsetning** \> **Fjárhagsfæribreytur**.
2. Á **Söluskattur** flipa, á **Rafræn skýrslugerð fyrir lönd/svæði** Flýtiflipi, á línunni fyrir **DNK**, veldu **VSK yfirlýsing Excel (DK)** ER snið.

## <a name="set-up-electronic-messages"></a>Settu upp rafræn skilaboð

### <a name="download-and-import-the-data-package-that-has-example-settings-for-electronic-messages"></a>Sæktu og flyttu inn gagnapakkann sem hefur dæmi um stillingar fyrir rafræn skilaboð

Gagnapakkinn inniheldur rafræn skilaboðastillingar sem notaðar eru til að forskoða virðisaukaskattsskýrsluna í Excel. Þú getur framlengt þessar stillingar eða búið til þínar eigin. Fyrir frekari upplýsingar um hvernig á að vinna með rafræn skilaboð og búa til þínar eigin stillingar, sjá [Rafræn skilaboð](../general-ledger/electronic-messaging.md).

1. Í [Microsoft Dynamics Lífsferilsþjónusta (LCS)](https://lcs.dynamics.com/v2), í Samnýtt eignasafn, veldu **Gagnapakki** sem eignategund og hlaðið síðan niður **DK VSK yfirlýsing pakki**. Skráin sem hlaðið er niður er nefnd **DK VSK yfirlýsing pakka.zip**.
2. Í fjármálum, í **Gagnastjórnun** vinnusvæði, veldu **Flytja inn**.
3. Á **Flytja inn** flýtiflipann, í **Nafn hóps** reit, sláðu inn nafn fyrir starfið.
4. Á flýtiflipanum **Valdar einingar** skal velja **Bæta við skrá**.
5. Í **Bæta við skrá** valmynd skaltu ganga úr skugga um að **Upprunagagnasnið** reiturinn er stilltur á **Pakki**, veldu **Hladdu upp og bættu við**, og veldu síðan zip-skrána sem þú sóttir áðan.
6. Veljið **Loka**.
7. Eftir að gagnaeiningunum hefur verið hlaðið upp skaltu velja á aðgerðarrúðunni **Flytja inn**.
8. Fara til **Skattur** > **Fyrirspurnir og skýrslur** > **Rafræn skilaboð** > **Rafræn skilaboð**, og staðfestu rafrænu skilaboðavinnsluna sem þú fluttir inn (**DK virðisaukaskattsyfirlýsing**).

### <a name="configure-electronic-messages"></a>Stilla rafræn skilaboð

1. Fara til **Skattur** > **Uppsetning** > **Rafræn skilaboð** > **Fylltu færslur aðgerðir**.
2. Veldu línu fyrir **DK Fylltu út virðisaukaskattsskýrslur**, og veldu síðan **Breyta fyrirspurn**.
3. Notaðu síuna til að tilgreina uppgjörstímabilin sem á að hafa með í skýrslunni.
4. Ef þú verður að tilkynna skattfærslur frá öðrum uppgjörstímabilum í annarri skýrslu, stofnaðu nýja **Fylltu út færslur** aðgerð og veldu viðeigandi uppgjörstímabil.

## <a name="preview-the-vat-declaration-in-excel"></a>Forskoðaðu virðisaukaskattsskýrsluna í Excel

### <a name="preview-the-vat-declaration-in-excel-from-the-report-sales-tax-for-settlement-period-periodic-task"></a><a name="preview-vat-excel"></a> Forskoðaðu virðisaukaskattsskýrsluna í Excel úr reglubundnu verkinu Tilkynna söluskatt fyrir uppgjörstímabil

1. Fara til **Skattur** > **Reglubundin verkefni** > **Yfirlýsingar** > **Söluskattur** > **Tilkynna söluskatt fyrir uppgjörstímabil**.
2. Í **Uppgjörstímabil** reit, veldu gildi.
3. Í **Útgáfa söluskattsgreiðslu** reit, veldu eitt af eftirfarandi gildum:

    - **Upprunalegt** : Búa til skýrslu fyrir söluskattsfærslur upprunalegu söluskattsgreiðslunnar eða áður en söluskattsgreiðslan er mynduð.
    - **Leiðréttingar** : Búa til skýrslu fyrir söluskattsfærslur allra síðari söluskattsgreiðslna fyrir tímabilið.
    - **Heildarlisti** : Búa til skýrslu fyrir allar söluskattsfærslur tímabilsins, þar á meðal frumritið og allar leiðréttingar.

4. Í **Frá dags** reit, veldu upphafsdag skýrslutímabilsins.
5. Veldu **Allt í lagi**, og skoðaðu Excel skýrsluna.

### <a name="settle-and-post-sales-tax"></a>Jafna og bóka virðisaukaskatt

1. Fara til **Skattur** > **Reglubundin verkefni** > **Yfirlýsingar** > **Söluskattur** > **Gera upp og bóka söluskatt**.
2. Í **Uppgjörstímabil** reit, veldu gildi.
3. Í **Útgáfa söluskattsgreiðslu** reit, veldu eitt af eftirfarandi gildum:

    - **Upprunalegt** : Mynda upprunalega söluskattsgreiðslu fyrir uppgjörstímabilið.
    - **Nýjustu leiðréttingar** : Mynda leiðréttingarsöluskattsgreiðslu eftir að upprunaleg söluskattsgreiðsla fyrir uppgjörstímabilið var stofnuð.

4. Í **Frá dags** reit, veldu upphafsdag skýrslutímabilsins.
5. Veldu **Í lagi**.

### <a name="preview-the-vat-declaration-in-excel-from-a-sales-tax-payment"></a>Forskoða virðisaukaskattsskýrsluna í Excel frá söluskattsgreiðslu

1. Fara til **Skattur** > **Fyrirspurnir og skýrslur** > **Fyrirspurnir um söluskatt** > **Söluskattsgreiðslur**, og veldu söluskattsgreiðslulínu.
2. Veldu **Prenta skýrslu**, og veldu síðan **Allt í lagi**.
3. Skoðaðu Excel skrána sem er búin til fyrir valda greiðslulínu söluskatts.

> [!NOTE]
> Skýrslan er aðeins mynduð fyrir valda línu söluskattsgreiðslunnar. Ef þú verður að búa til, til dæmis, leiðréttingaryfirlýsingu sem inniheldur allar leiðréttingar fyrir tímabilið, eða varayfirlýsingu sem inniheldur frumgögn og allar leiðréttingar, notaðu **Tilkynna söluskatt fyrir uppgjörstímabil** reglubundið verkefni.

## <a name="generate-a-vat-declaration-from-electronic-messages"></a>Búðu til virðisaukaskattsskýrslu úr rafrænum skilaboðum

Þegar þú notar rafræn skilaboð til að búa til skýrsluna geturðu safnað skattagögnum frá mörgum lögaðilum. Fyrir frekari upplýsingar, sjá [Keyra virðisaukaskattsskýrslu fyrir marga lögaðila](#run-vat-declaration) kafla síðar í þessari grein.

Eftirfarandi aðferð á við um rafræn skilaboðavinnsludæmið sem þú fluttir inn áðan úr LCS Shared eignasafninu.

1. Fara til **Skattur \> Fyrirspurnir og skýrslur \> Rafræn skilaboð \> Rafræn skilaboð**.
2. Í vinstri glugganum velurðu **DK virðisaukaskattsyfirlýsing**.
3. Á **Skilaboð** Flýtiflipi, veldu **Nýtt**, og síðan, í **Keyra vinnslu** valmynd, veldu **Allt í lagi**.
4. Veldu skilaboðalínuna sem er búin til, sláðu inn lýsingu og tilgreindu síðan upphafs- og lokadagsetningar yfirlýsingarinnar.

   > [!NOTE]
   > Skref 5 til 7 eru valfrjáls.

5. Valfrjálst: Á **Skilaboð** Flýtiflipi, veldu **Safna gögnum**, og veldu síðan **Allt í lagi**. Vöruskattsgreiðslur sem voru búnar til áður er bætt við skilaboðin. Fyrir frekari upplýsingar, sjá [Gera upp og bóka söluskatt](#settle-and-post-sales-tax) kafla fyrr í þessari grein. Ef þú sleppir þessu skrefi geturðu samt búið til virðisaukaskattsskýrslu með því að nota **Útgáfa skattframtals** sviði í **Yfirlýsing** valmynd.
6. Valfrjálst: Á **Skilaboðaatriði** Flýtiflipi, skoðaðu söluskattsgreiðslur sem eru fluttar til vinnslu. Sjálfgefið er að allar söluskattsgreiðslur valins tímabils sem ekki voru innifalin í öðrum skilaboðum í sömu vinnslu eru innifaldar.
7. Valfrjálst: Veldu **Upprunalegt skjal** til að fara yfir söluskattsgreiðslurnar eða velja **Eyða** að undanskilja söluskattsgreiðslur frá afgreiðslu. Ef þú sleppir þessu skrefi geturðu samt búið til virðisaukaskattsskýrslu með því að nota **Útgáfa skattframtals** sviði í **Yfirlýsing** valmynd.
8. Á **Skilaboð** Flýtiflipi, veldu **Uppfæra stöðu**. Í **Uppfæra stöðu** valmynd, veldu **Tilbúið til að búa til**, og veldu síðan **Allt í lagi**. Staðfestu að skilaboðastöðu sé breytt í **Tilbúið til að búa til**.
9. Veldu **Búðu til skýrslu**. Til að forskoða virðisaukaskattsupphæðir, í **Keyra vinnslu** valmynd, veldu **Forskoðunarskýrsla**, og veldu síðan **Allt í lagi**.
10. Í **Rafrænar skýrslubreytur** valmynd, stilltu reitina eins og lýst er í [Forskoðaðu virðisaukaskattsskýrsluna í Excel úr reglubundnu verkinu Tilkynna söluskatt fyrir uppgjörstímabil](#preview-vat-excel) kafla fyrr í þessari grein og veldu síðan **Allt í lagi**.
11. Veldu **Viðhengi** hnappinn (táknið fyrir bréfaklemmu) í efra hægra horninu á síðunni og veldu síðan **Opið** til að opna skrána. Farið yfir upphæðirnar í Excel skjalinu.

## <a name="run-a-vat-declaration-for-multiple-legal-entities"></a><a name="run-vat-declaration"></a> Keyra virðisaukaskattsskýrslu fyrir marga lögaðila

Til að nota sniðin til að tilkynna um virðisaukaskattsyfirlýsingu fyrir hóp lögaðila, verður þú fyrst að setja upp forritssértækar færibreytur ER-sniða fyrir VSK-kóða frá öllum nauðsynlegum lögaðilum.

### <a name="set-up-electronic-messages-to-collect-tax-data-from-several-legal-entities"></a>Settu upp rafræn skilaboð til að safna skattagögnum frá nokkrum lögaðilum

Fylgdu þessum skrefum til að setja upp rafræn skilaboð til að safna gögnum frá mörgum lögaðilum.

1. Fara til **Vinnurými** > **Eiginleikastjórnun**.
2. Finndu og veldu **Fyrirspurnir þvert á fyrirtæki fyrir aðgerðir til að fylla út færslur** eiginleiki á listanum og veldu síðan **Virkja núna**.
3. Fara til **Skattur** > **Uppsetning** > **Rafræn skilaboð** > **Fylltu færslur aðgerðir**.
4. Á **Fylltu færslur aðgerð** síðu, veldu línuna fyrir **DK Fylltu út virðisaukaskattsskýrslur**.

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
