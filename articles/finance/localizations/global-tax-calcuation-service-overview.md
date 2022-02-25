---
title: Yfirlit skattaútreiknings
description: Þetta efnisatriði skýrir heildarumfang og eiginleika skattaútreikningsgetu.
author: wangchen
ms.date: 11/17/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1dff1767b8e19215a2b27f87c45325e6abd1266e
ms.sourcegitcommit: f2a78e0d7d461ca843ac2f9abff7690275db9196
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/09/2022
ms.locfileid: "8105438"
---
# <a name="tax-calculation-overview"></a>Yfirlit skattaútreiknings

[!include [banner](../includes/banner.md)]

Skattaútreikningur er þjónusta með stillanlegri þjónustu fyrir marga notendur sem gerir altæku skattkerfi kleift að einfalda skattaákvörðun og útreikning og gera það sjálfvirkt. Skattvélin er fullkomlega stillanleg. Einingarnar sem hægt er að stilla fela í sér, en takmarkast ekki við, skattalega gagnalíkansins, skattkóða, fylkisins fyrir skattskyldu og formúlu skattútreiknings. Skattkerfið keyrir á Microsoft Azure verkvangi og býður upp á nútímatækni og sveigjanleika.

Skattútreikningur er samþættur við Dynamics 365 Finance og Dynamics 365 Supply Chain Management. Að lokum verður hún einnig samþætt við Dynamics 365 Project Operations, Dynamics 365 Commerce og önnur forrit frá fyrstu og þriðju aðilum.

> [!IMPORTANT]
> Þegar skattaútreikningur er virkjaður gætu sumar aðgerðir á tengdum gögnum verið framkvæmdar í gagnamiðstöð annarri en gagnamiðstöðinni sem heldur utan um þjónustugögnin. Yfirfarið [Skilmálana](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md) áður en skattaútreikningur er virkjaður. Persónuvernd þín er okkur mikilvæg. Frekari upplýsingar má finna í [tilkynningu okkar um persónuvernd](https://go.microsoft.com/fwlink/?LinkId=521839).

Skattaútreikningur er skattakerfi frá Microsoft sem býður upp á mikinn sveigjanleika og getur hjálpað þér að framkvæma eftirfarandi verk:

- Ákvarða sjálfkrafa rétta söluskattshópinn, söluskattshópinn og skattkóða í gegnum aukið ákvörðunarferli.
- Styðjast við mörg skattskrárnúmer hjá einum lögaðila og ákveða sjálfkrafa rétt skattskrárnúmer fyrir skattskyld viðskipti.
- Styðja skattákvörðun, útreikning, bókun og uppgjör vegna flutningspantana.
- Skilgreindu stillanlegar formúlur og skilyrði skattaútreikninga fyrir þínar tilteknu viðskiptaþarfir.
- Deildu skattákvörðun og útreikningslausn á milli lögaðila til að vista aðgerðir og koma í veg fyrir villur.
- Styddu ákvarðanir skattskráningarnúmers viðskiptavinar og lánardrottins.
- Styðja ákvörðun listakóða.
- Styddu við færibreytur skattaútreiknings á stigi skattaumdæmis.

Til að nota skattaútreikning skal setja upp innbót skattaútreikningsins úr verkefninu í Microsoft Dynamics Lifecycle Services. Ljúkið síðan uppsetningunni í [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/) og gerið skattaútreikning virkan í Finance and Supply Chain Management. Frekari upplýsingar eru í [Hafist handa með skattþjónustu](global-get-started-with-tax-calculation-service.md).

## <a name="availability"></a>Til ráðstöfunar

Skattaútreikningur er almennt aðgengilegur öllum viðskiptavinum í framleiðsluumhverfi frá og með útgáfu 10.0.21.

Áfram verður boðið upp á nýja eiginleika. Athugaðu nýjustu útgáfuáætlun með reglulegu millibili til að fá upplýsingar um umfang studdra eiginleika.

Skattaútreikningur er í boði á eftirfarandi staðsetningum Azure. Fleiri Azure-staðsetningum verður bætt við eftir því hverjar þarfir viðskiptavinanna eru.

- Asía og Kyrrahaf
- Ástralía
- Kanada
- Evrópa
- Japan
- Bretland
- Bandaríkin

> [!NOTE]
> Skattaútreikningur styður ekki eldri útgáfu af Dynamics 365, svo sem Dynamics AX 2012 eða uppsetningu á staðnum af Dynamics 365.

## <a name="versions"></a>Útgáfur
Við mælum með því að þú flytur inn og stillir upp skattaútreikninginn þinn með útgáfunni sem passar við útgáfuna þína fyrir fjármála- eða framboðskeðjustjórnun.

| Útgáfa fjármála eða birgðakeðjustjórnunar | Skattstillingarútgáfa               |
| --------------- | --------------------------------------- |
| 10.0.18         | Skattstillingar - Evrópa 30.12.82     |
| 10.0.19         | Skattaútreikningsstilling 36.38.193 |
| 10.0.20         | Skattaútreikningsstilling 40.43.208 |
| 10.0.21         | Skattaútreikningsstilling 40.48.215 |
| 10.0.22         | Skattaútreikningsstilling 40.48.215 |
| 10.0.23         | Skattaútreikningsstilling 40.50.221 |
| 10.0.24         | Skattaútreikningsstilling 40.50.225 |
| 10.0.25         | Skattaútreikningsstilling 40.50.225 |


## <a name="data-flow"></a>Gagnaflæði

Hér er yfirlit yfir gagnaflæðisferlið fyrir skattútreikning. 

1. Í RCS skaltu skoða og flytja inn skilgreiningar á líkönum skattskyldra skjala og skilgreiningar líkanavörpunar. Ef þú verður að stækka skilgreiningar fyrir ítarlegri aðstæður skaltu skoða [Bæta við gagnareitum í skattaskilgreiningum](tax-service-add-data-fields-tax-configurations.md).
2. Í RCS skaltu búa til eða vinna með skattaeiginleika. Þú getur notað skattaeiginleika til að vinna með skatthlutföll og gildissviðsreglur skatts.
3. Eftir að uppsetningu skattaeiginleika er lokið skaltu befa út skattaskilgreiningarnar og skattaeiginleikana úr RCS í altæku geymsluna.
4. Í Finance skaltu velja hvaða útgáfu af uppsetningu skattaeiginleika á að nota fyrir tiltekinn lögaðila.
5. Í Finance og Supply Chain Management skaltu stýra aðgerðum eins og venjulega. Þegar skattaútreiknings er þörf mun biðlarinn safna upplýsingum úr færslunni, eins og sölupöntun eða innkaupapöntun og pakka upplýsingunum saman innihaldi. Þá verður send beiðni um að reikna skattinn.
6. Skattaútreikningsbeiðni berst frá viðskiptavini og útreikningi er lokið. Skattaniðurstöðunni er þá skilað til biðlarans.
7. Biðlari Dynamics 365 fær skattaniðurstöðuna og birtir skattaútreikninginn á síðu söluskatts.

## <a name="supported-transactions"></a>Studdar færslur

Hægt er að virkja skattaútreikning eftir færslum. 

Eftirfarandi færslur eru studdar í Finance-útgáfu 10.0.21: 

- Sala

    - Sölutilboð
    - Sölupöntun
    - Staðfesting
    - Tiltektarlisti
    - Fylgiseðill
    - Sölureikningur
    - Kreditnóta
    - Skila pöntun
    - Ýmis hausgjöld
    - Ýmis línugjöld

- Innkaup

    - Innkaupapöntun
    - Staðfesting
    - Komulisti
    - Innhreyfingarskjal afurða
    - Innkaupareikningur
    - Ýmis hausgjöld
    - Ýmis línugjöld
    - Kreditnóta
    - Skila pöntun
    - Innkaupabeiðni
    - Ýmis gjöld innkaupabeiðnilínu
    - Beiðni um tilboð
    - Ýmis hausgjöld fyrir beiðni um tilboð
    - Ýmis línugjöld fyrir beiðni um tilboð

- Birgðir

    - Flutningspantanir - senda
    - Móttaka flutningspöntunar

Eftirfarandi færslur eru studdar í Finance-útgáfu 10.0.23: 

- Reikningur með frjálsum texta

## <a name="supported-countriesregions"></a>Studd lönd/svæði

Hægt er að virkja skattaútreikning eftir lögaðila. 

Eftirfarandi lönd/svæði fyrir aðalaðsetur lögaðila eru studd í útgáfu 10.0.21:

- Austurríki
- Belgía
- Danmörk
- Eistland
- Finnland
- Frakkland
- Þýskaland
- Ungverjaland
- Ísland
- Ítalía
- Lettland
- Litháen
- Holland
- Noregur
- Pólland
- Svíþjóð
- Sviss
- Bretland
- Bandaríkin

Eftirfarandi lönd/svæði fyrir aðalaðsetur lögaðila eru studd í útgáfu 10.0.22:

- Ástralía
- Barein
- Kanada
- Egyptaland
- Hong Kong (sérstjórnarsvæði)
- Kúveit
- Nýja-Sjáland
- Óman
- Katar
- Sádi-Arabískt
- Suður-Afríka
- Sameinuðu arabísku furstadæmin

Eftirfarandi lönd/svæði fyrir aðalaðsetur lögaðila eru studd í útgáfu 10.0.23:

- Taíland
- Japan
- Malasía
- Singapúr

Eftirfarandi lönd/svæði fyrir aðalaðsetur lögaðila eru studd í útgáfu 10.0.24:

- Mexíkó

## <a name="related-resources"></a>Tengd tilföng

[Hafist handa með skattþjónustu](./global-get-started-with-tax-calculation-service.md)

[Mörg VSK-skráningarnúmer](./emea-multiple-vat-registration-numbers.md)

[Stuðningur skattaeiginleika fyrir flutningspöntun](./tasks/tax-feature-support-for-transfer-order.md)

[Hvernig á að byggja upp viðbót í skattsþjónustu](./tax-service-add-data-fields-tax-integration-by-extension.md)
