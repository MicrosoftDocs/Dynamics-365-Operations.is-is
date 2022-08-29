---
title: Yfirlit skattaútreiknings
description: Þessi grein útskýrir heildarumfang og eiginleika skattaútreikningsmöguleikans.
author: EricWangChen
ms.date: 03/02/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.search.form: TaxIntegrationTaxServiceParameters
ms.openlocfilehash: 2765b922bcc58837c32973b7ca96e0d63eb8b9d6
ms.sourcegitcommit: 14a27b776befbc6793390f97e8fb0279c0ea18c1
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/15/2022
ms.locfileid: "9295993"
---
# <a name="tax-calculation-overview"></a>Yfirlit skattaútreiknings

[!include [banner](../includes/banner.md)]

Skattaútreikningur er þjónusta með stillanlegri þjónustu fyrir marga notendur sem gerir altæku skattkerfi kleift að einfalda skattaákvörðun og útreikning og gera það sjálfvirkt. Skattvélin er fullkomlega stillanleg. Einingarnar sem hægt er að stilla fela í sér, en takmarkast ekki við, skattalega gagnalíkansins, skattkóða, fylkisins fyrir skattskyldu og formúlu skattútreiknings. Skattkerfið keyrir á Microsoft Azure verkvangi og býður upp á nútímatækni og sveigjanleika.

Skattaútreikningur er samþættur Dynamics 365 Finance og Dynamics 365 Supply Chain Management. Að lokum verður hún einnig samþætt við Dynamics 365 Project Operations, Dynamics 365 Commerce og önnur forrit frá fyrstu og þriðju aðilum.

> [!IMPORTANT]
> Þegar skattaútreikningur er virkjaður gætu sumar aðgerðir á tengdum gögnum verið framkvæmdar í gagnamiðstöð annarri en gagnamiðstöðinni sem heldur utan um þjónustugögnin. Yfirfarið [Skilmálana](https://go.microsoft.com/fwlink/?linkid=2156043) áður en skattaútreikningur er virkjaður. Persónuvernd þín er okkur mikilvæg. Frekari upplýsingar má finna í [tilkynningu okkar um persónuvernd](https://go.microsoft.com/fwlink/?LinkId=521839).

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
- Brasilía
- Kanada
- Evrópa
- Frakkland
- Indland
- Japan
- Suður-Afríka
- Sviss
- Sameinuðu arabísku furstadæmin
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
| 10.0.26         | Skattaútreikningsstilling 40.54.234 |
| 10.0.27         | Skattaútreikningsstilling 40.54.234 |
| 10.0.28         | Skattaútreikningsstilling 40.54.234 |
| 10.0.29         | Skattaútreikningsstilling 40.55.236 |


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

Eftirfarandi færslur eru studdar í Finance-útgáfu 10.0.26: 

- Almennar færslubækur
- Reikningabók lánardrottins

Eftirfarandi færslur eru studdar í Finance-útgáfu 10.0.28: 

- Greiðslubók lánardrottins
- Greiðslubók viðskiptavinar

Eftirfarandi færslur eru studdar í Finance-útgáfu 10.0.29: 


- Tímabilsbækur

## <a name="supported-countriesregions"></a>Studd lönd/svæði

Skattaútreikning er hægt að keyra með studdum staðsetningareiginleikum í eftirfarandi löndum/svæðum fyrir aðal heimilisfang lögaðila: 

Styður í útgáfu 10.0.21:

- Austurríki
- Belgía
- Danmörk
- Eistland
- Finnland
- Frakkland
- Þýskaland
- Ungverjaland
- Ísland
- Írland
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

Styður í útgáfu 10.0.22:

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

Styður í útgáfu 10.0.23:

- Taíland
- Japan
- Malasía
- Singapúr

Styður í útgáfu 10.0.24:

- Mexíkó

Styður í útgáfu 10.0.26:

- Kína
- Tékkland
- Spánn

Fyrir öll lönd/svæði sem Microsoft hefur ekki staðfært, er einnig hægt að virkja og keyra skattaútreikning með öðrum alþjóðlegum eiginleikum.

## <a name="related-resources"></a>Tengd tilföng

[Hafist handa með skattþjónustu](./global-get-started-with-tax-calculation-service.md)

[Mörg VSK-skráningarnúmer](./emea-multiple-vat-registration-numbers.md)

[Stuðningur skattaeiginleika fyrir flutningspöntun](./tasks/tax-feature-support-for-transfer-order.md)

[Hvernig á að byggja upp viðbót í skattsþjónustu](./tax-service-add-data-fields-tax-integration-by-extension.md)
