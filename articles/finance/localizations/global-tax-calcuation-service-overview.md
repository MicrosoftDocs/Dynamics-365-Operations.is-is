---
title: Yfirlit skattaútreiknings
description: Þessi grein skýrir heildarumfang og eiginleika skattaútreikningsgetu.
author: EricWangChen
ms.date: 09/08/2022
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
ms.openlocfilehash: cafc4c7089e0c042fc65c1e3fd21f8f1e930b785
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689885"
---
# <a name="tax-calculation-overview"></a>Yfirlit skattaútreiknings

[!include [banner](../includes/banner.md)]

Skattaútreikningur er þjónusta með stillanlegri þjónustu fyrir marga notendur sem gerir altæku skattkerfi kleift að einfalda skattaákvörðun og útreikning og gera það sjálfvirkt. Skattvélin er fullkomlega stillanleg. Einingarnar sem hægt er að stilla fela í sér, en takmarkast ekki við, skattalega gagnalíkansins, skattkóða, fylkisins fyrir skattskyldu og formúlu skattútreiknings. Skattkerfið keyrir á Microsoft Azure verkvangi og býður upp á nútímatækni og sveigjanleika.

Skattaútreikningur samþættist Dynamics 365 Finance og Dynamics 365 Supply Chain Management. Að lokum verður hún einnig samþætt við Dynamics 365 Project Operations, Dynamics 365 Commerce og önnur forrit frá fyrstu og þriðju aðilum.

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
Mælt er með því að þú flytjir inn og setjir upp skattaútreikningsstillingar með þeirri útgáfu sem passar við útgáfu Finance eða Supply Chain Management.

| Finance- eða Supply Chain Management-útgáfa | Útgáfa skattaskilgreiningar               |
| --------------- | --------------------------------------- |
| 10.0.31         | Skattaútreikningsstilling 40.56.240 |
| 10.0.30         | Skattaútreikningsstilling 40.55.239 |
| 10.0.29         | Skattaútreikningsstilling 40.55.236 |
| 10.0.28         | Skattaútreikningsstilling 40.54.234 |
| 10.0.27         | Skattaútreikningsstilling 40.54.234 |


## <a name="data-flow"></a>Gagnaflæði

Hér er útlistun á gagnaflæðisferlinu fyrir Skattaútreikningur. 

1. Í RCS skaltu skoða og flytja inn skilgreiningar á líkönum skattskyldra skjala og skilgreiningar líkanavörpunar. Ef þú verður að stækka skilgreiningar fyrir ítarlegri aðstæður skaltu skoða [Bæta við gagnareitum í skattaskilgreiningum](tax-service-add-data-fields-tax-configurations.md).
2. Í RCS skaltu búa til eða vinna með skattaeiginleika. Þú getur notað skattaeiginleika til að vinna með skatthlutföll og gildissviðsreglur skatts.
3. Eftir að uppsetningu skattaeiginleika er lokið skaltu befa út skattaskilgreiningarnar og skattaeiginleikana úr RCS í altæku geymsluna.
4. Í Finance skaltu velja hvaða útgáfu af uppsetningu skattaeiginleika á að nota fyrir tiltekinn lögaðila.
5. Í Finance og Supply Chain Management skaltu stýra aðgerðum eins og venjulega. Þegar skattaútreiknings er þörf mun biðlarinn safna upplýsingum úr færslunni, eins og sölupöntun eða innkaupapöntun og pakka upplýsingunum saman innihaldi. Þá verður send beiðni um að reikna skattinn.
6. Skattaútreikningsbeiðni berst frá viðskiptavini og útreikningi er lokið. Skattaniðurstöðunni er þá skilað til biðlarans.
7. Biðlari Dynamics 365 fær skattaniðurstöðuna og birtir skattaútreikninginn á síðu söluskatts.

## <a name="supported-transactions"></a>Studdar færslur

Hægt er að virkja skattaútreikning eftir færslum. 

Í eftirfarandi töflu er listi yfir þær færslur sem stuðst er við í samsvarandi útgáfu.

| Útgáfa | Færslur |
|---------|--------------|
| 10.0.29 | Tímabilsbækur |
| 10.0.28 | Greiðslubók lánardrottins<br> Greiðslubók viðskiptavinar | 
| 10.0.26 | Almennar færslubækur<br> Reikningabók lánardrottins |
| 10.0.23 | Reikningur með frjálsum texta |
| 10.0.21| Sala<br><ul><li>Sölutilboð</li><li>Sölupöntun</li><li>Staðfesting</li><li>Tiltektarlisti</li><li>Fylgiseðill</li><li>Sölureikningur</li><li>Kreditnóta</li><li>Skila pöntun</li><li>Ýmis hausgjöld</li><li>Ýmis línugjöld</li></ul>Innkaup<br><ul><li>Innkaupapöntun</li><li>Staðfesting</li><li>Komulisti</li><li>Innhreyfingarskjal afurða</li><li>Innkaupareikningur</li><li>Ýmis hausgjöld</li><li>Ýmis línugjöld</li><li>Kreditnóta</li><li>Skila pöntun</li><li>Innkaupabeiðni</li><li>Ýmis gjöld innkaupabeiðnilínu</li><li>Beiðni um tilboð</li><li>Ýmis hausgjöld fyrir beiðni um tilboð</li><li>Ýmis línugjöld fyrir beiðni um tilboð</li></ul>Birgðir<ul><li>Flutningspantanir - senda</li><li>Móttaka flutningspöntunar</li></ul>|

## <a name="supported-countriesregions"></a>Studd lönd/svæði

Hægt er að keyra skattaútreikning með studdum staðfærslueiginleika. Í eftirfarandi töflu er listi yfir lönd/svæði fyrir aðalheimilisfang lögaðila.

| Útgáfa | Land/svæði |
|---------|----------------|
| 10.0.26 | - Kína <br>- Tékkland<br>- Spánn |
| 10.0.24 | Mexíkó |
| 10.0.23 | - Taíland <br>- Japan <br>- Malasía <br>- Singapúr |
| 10.0.22 | - Ástralía<br>- Barein <br>- Kanada<br>- Egyptaland <br>- Hong Kong (sérstjórnarsvæði) <br>- Kúveit <br>- Nýja-Sjáland <br>- Óman <br>- Katar <br>- Sádi-Arabía <br>- Suður-Afrík <br>- Sameinuðu arabísku furstadæmin |
| 10.0.21 | - Austurríki <br>- Belgía <br>- Danmörk <br>- Eistland <br>- Finnland <br>- Frakkland <br>- Þýskaland <br>- Ungverjaland <br>- Ísland <br>- Írland <br>- Ítalía <br>- Lettland <br>- Litháen <br>- Holland <br>- Noregur <br>- Pólland <br>- Svíþjóð <br>- Sviss <br>- Bretland <br>- Bandaríkin |

Fyrir hvaða land/svæði sem er sem ekki er staðfært af Microsoft er einnig hægt að virkja Skattaútreikning og keyra hann með öðrum altækum eiginleikum.

## <a name="related-resources"></a>Tengd tilföng

[Hafist handa með skattþjónustu](./global-get-started-with-tax-calculation-service.md)

[Mörg VSK-skráningarnúmer](./emea-multiple-vat-registration-numbers.md)

[Stuðningur skattaeiginleika fyrir flutningspöntun](./tasks/tax-feature-support-for-transfer-order.md)

[Hvernig á að byggja upp viðbót í skattsþjónustu](./tax-service-add-data-fields-tax-integration-by-extension.md)
