---
title: Stofna sniðmát fyrir tölvupóst fyrir færslutilvik
description: Þetta efnisatriði lýsir því hvernig á að búa til, hlaða upp og skilgreina tölvupóstssniðmát fyrir færslutilvik í Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: annbe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: ea484bfc1e9b293c53d7293c50630c4955000131
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/10/2020
ms.locfileid: "3983158"
---
# <a name="create-email-templates-for-transactional-events"></a>Stofna sniðmát fyrir tölvupóst fyrir færslutilvik

[!include [banner](includes/banner.md)]

Þetta efnisatriði lýsir því hvernig á að búa til, hlaða upp og skilgreina tölvupóstssniðmát fyrir færslutilvik í Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Dynamics 365 Commerce býður upp á lausn til að senda tölvupóst til að láta viðskiptavini vita af færslutilvikum (til dæmis þegar pöntun er send inn, pöntun er tilbúin til afhendingar eða pöntun hefur verið send). Þetta efnisatriði lýsir skrefum til að búa til, hlaða upp og skilgreina sniðmát fyrir tölvupóst sem eru notuð til að senda færslutengdan tölvupóst.

## <a name="create-an-email-template"></a>Stofna sniðmát fyrir tölvupóst

Áður en hægt er að varpa tilteknu færslutilviki í tölvupóstssniðmát verður að stofna sniðmátið.

Til að stofna tölvupóstsniðmát, skal fylgja eftirfarandi skrefum.

1. Í höfuðstöðvum Commerce skal opna **Tölvupóstssniðmát fyrirtækis**, sem er undir **Smásala og viðskipti \> Uppsetning höfuðstöðva \> Tölvupóstssniðmát fyrirtækis** eða **Fyrirtækisstjórnun \> Uppsetning \> Tölvupóstssniðmát fyrirtækis**.
1. Veljið **Nýtt**.
1. Undir **Almennt** skal stilla eftirfarandi reiti:

    - **Tölvupóstkenni** – tölvupóstkennið er einkvæmt kennimerki fyrir sniðmát og það er gildið sem er sýnt þegar sniðmát er valið til að varpa í tilvik.
    - **Lýsing á tölvupósti** – hægt er að nota þennan valfrjálsa reit fyrir lýsingu á sniðmátinu. Gildið sem fært er inn birtist aðeins í Commerce Headquarters.
    - **Nafn sendanda** – heitið sem fært er inn birtist í reitnum „Frá“ í flestum tölvupóstforritum.
    - **Netfang sendanda** – færið inn netfangið sem á að nota fyrir tölvupóst sem er sendur með því að nota þetta sniðmát.
    - **Sjálfgefinn tungumálakóði** – þessi reitur tilgreinir staðfærða útgáfu tölvupóstsins sem er sjálfgefið sendur, ef ekkert tungumál er í rásinni sem ræsir þetta sniðmát.

1. Undir **Efni tölvupóstskilaboða** skal velja **Nýtt**.
1. Í reitinn **Tungumál** er fært inn tungumálið fyrir sniðmát tölvupósts. Hægt er að bæta við fleiri tungumálum og staðfærðum sniðmátum síðar.
1. Í reitnum **Efni** skal færa inn efni tölvupóstsins sem á að birtast í efnisreit tölvupóstsins.
1. Veljið **Breyta** til að hlaða upp tölvupóstssniðmátinu.

## <a name="create-an-email-message-body-by-using-html"></a>Meginmál tölvupóstskilaboðanna búið til með HTML

Meginmál tölvupóstsins er skrifað í HTML. Hægt er að nota allar útlit, stíl og vörumerki sem HTML og stölluð stílblöð (CSS) leyfa. Einnig er hægt að nota myndir ef þær eru hýstar á vefsvæði sem er í boði opinberlega. Til að bæta við mynd skal slá inn vefslóð myndarinnar í **src**-eigind HTML **&lt;img&gt;**-merkisins.

> [!NOTE]
> Tölvupóstforrit nota útlit og stíltakmarkanir sem gætu krafist leiðréttingar í HTML og CSS sem er notað fyrir meginmál skilaboðanna. Við mælum með því að notandi kynni sér bestu starfsvenjur fyrir stofnun HTML sem vinsælustu tölvupóstforritin styðja.

## <a name="add-placeholders-to-the-email-message-body"></a>Staðgenglum bætt við meginmál tölvupóstskilaboða

Tölvupóstur getur innihaldið staðgengla sem er skipt út fyrir sértæk gildi fyrir viðskiptavini og færslur þegar tölvupósturinn er búinn til. Staðgenglar eru alltaf innan prósentumerkja (%) og eru settir beint inn í HTML-skjalið.

Eftirfarandi er dæmi.

```html
<p>
    Hello %customername%,<br />
    Order number %salesid%, can be picked up from the <b>%pickupstorename%</b> store.
</p>
```

### <a name="order-placeholders-sales-order-level"></a>Pöntunarstaðgenglar (stig sölupantana)

Eftirfarandi staðgenglar sækja og sýna gögn sem eru skilgreind á stigi sölupantana (öfugt við sölulínustigið).

| Staðgengilsheiti    | Staðgengilsgildi                                                |
|---------------------|------------------------------------------------------------------|
| customername        | Nafn viðskiptavinarins sem sendi inn pöntunina.                   |
| salesid             | Sölukenni pöntunar.                                       |
| deliveryaddress     | Afhendingaraðsetur fyrir sendar pantanir.                         |
| customeraddress     | Aðsetur viðskiptavinarins.                                     |
| deliverydate        | Afhendingardagsetning.                                               |
| shipdate            | Sendingardagsetning.                                                   |
| modeofdelivery      | Afhendingarmáti pöntunarinnar.                                  |
| Gjöld             | Heildargjöld fyrir pöntunina.                                 |
| Skattur                 | Heildarskattur fyrir pöntunina.                                     |
| samtala               | Heildarupphæð pöntunarinnar.                                  |
| ordernetamount      | Heildarupphæðin fyrir pöntunina, að frádregnum heildarskatti.             |
| afsláttur            | Heildarafsláttur pöntunarinnar.                                |
| storename           | Heiti verslunarinnar þaðan sem pöntunin er upprunnin.                |
| storeaddress        | Aðsetur verslunarinnar þaðan sem pöntunin er upprunnin.                  |
| storeopenfrom       | Opnunartími verslunarinnar þaðan sem pöntunin er upprunnin.             |
| storeopento         | Lokunartími verslunarinnar þaðan sem pöntunin er upprunnin.             |
| pickupstorename     | Heiti verslunarinnar þar sem pöntunin verður sótt.         |
| pickupstoreaddress  | Aðsetur verslunarinnar þar sem pöntunin verður sótt.      |
| pickupopenstorefrom | Opnunartími verslunarinnar þar sem pöntunin verður sótt. |
| pickupopenstoreto   | Lokunartími verslunarinnar þar sem pöntunin verður sótt. |

### <a name="order-line-placeholders-sales-line-level"></a>Staðgenglar pöntunarlínu (sölulínustig)

Eftirfarandi staðgenglar sækja og sýna gögn fyrir einstakar afurðir (línur) á sölupöntuninni.

| Staðgengilsheiti               | Staðgengilsgildi |
|--------------------------------|-------------------|
| productid                      | Afurðakennið fyrir línuna. |
| lineproductname                | Nafn vörunnar. |
| lineproductdescription         | Lýsing á afurðinni. |
| linequantity                   | Fjöldi eininga sem voru pantaðar fyrir línuna, auk mælieiningarinnar (til dæmis **ea** eða **par**). |
| lineunit                       | Mælieiningin fyrir línuna. |
| linequantity_withoutunit       | Einingafjöldi sem var pantaður fyrir línuna, án mælieiningar. |
| linequantitypicked             | Þegar **PickOrder** viðburðurinn er notaður, fjöldi eininga sem voru teknar til. Annars, **0** (núll). |
| linequantitypicked_withoutunit | Þegar **PickOrder** viðburðurinn er notaður, fjöldi eininga sem voru tíndar, án mælieiningar. Annars, **0** (núll). |
| linequantitypacked             | Þegar tilvikin **PackOrder** og **Pöntun tilbúin til afhendingar** eru notuð, fjöldi eininga sem var pakkað. Annars, **0** (núll). |
| linequantitypacked_withoutuom  | Þegar tilvikin **PackOrder** og **Pöntun tilbúin til afhendingar** eru notuð, fjöldi eininga sem var pakkað, án mælieiningarinnar. Annars, **0** (núll). |
| linequantityshipped            | Alltaf **0**, nema þegar tiltekin tilvik eru notuð, eins og lýst er í næstu línu. |
| linequantityshipped_withoutuom | Þegar **ShipOrder** viðburðurinn er notaður, fjöldi eininga sem voru tíndar, án mælieiningar. Annars, **0** (núll). |
| lineprice                      | Verð einnar einingar. |
| linenetamount                  | Verð línunnar eftir að einingafjöldi og afsláttur eru notuð. |
| linediscount                   | Afsláttur fyrir einstaka einingu. |
| lineshipdate                   | Sendingardagsetning fyrir línuna. |
| linedeliverydate               | Afhendingardagsetning línunnar. |
| linedeliverymode               | Afhendingarmáti fyrir línuna. |
| linedeliveryaddress            | Afhendingaraðsetur fyrir línuna. |
| giftcardnumber                 | Gjafakortsnúmer, fyrir afurðir af gerðinni gjafakort. |
| giftcardbalance                | Staða gjafakorts, fyrir afurðir af gerðinni gjafakort. |
| giftcardmessage                | Gjafakortsskilaboð, fyrir afurðir af gerðinni gjafakort. |
| giftcardpin                    | PIN-númer gjafakortsins, fyrir afurðir af gerðinni gjafakort. (Þessi staðgengill er tilgreindur fyrir ytri gjafakort.) |
| giftcardexpiration             | Lokadagur gjafakortsins, fyrir afurðir af gerðinni gjafakort. (Þessi staðgengill er tilgreindur fyrir ytri gjafakort.) |
| giftcardrecipientname          | Heiti viðtakanda gjafakortsins, fyrir afurðir af gerðinni gjafakort. |
| giftcardbuyername              | Heiti kaupanda gjafakortsins, fyrir afurðir af gerðinni gjafakort. |

### <a name="format-of-order-line-placeholders-in-the-email-message-body"></a>Snið staðgengla pöntunarlínu í meginmáli tölvupóstskilaboðanna

Þegar HTML er búið til fyrir einstakar pöntunarlínur í meginmáli tölvupóstskilaboðanna, umlykja endurtekna HTML-blokk og staðgengla fyrir línurnar með eftirfarandi staðgenglum sem eru settir inn í HTML-athugasemdarmerki.

```html
<!--%tablebegin.salesline%-->

(Insert the repeating block of HTML and placeholders for individual lines here.)

<!--%tableend.salesline%-->
```

Eftirfarandi er dæmi.

```HTML
<table>
    <tr>
        <td>Product name</td>
        <td>Quantity</td>
        <td>Price</td>
    </tr>
    <!--%tablebegin.salesline%-->
    <tr>
        <td>%lineproductname%</td>
        <td>%linequantity_withoutunit%</td>
        <td>%lineprice%</td>
    </tr>
    <!--%tableend.salesline%-->
</table>
```

## <a name="create-a-template-for-emailed-receipts"></a>Stofna sniðmát fyrir kvittanir sem sendar eru í tölvupósti

Hægt er að fá kvittanir sendar í tölvupósti til viðskiptavina sem gera innkaup á sölustað. Almennt eru skrefin til að búa til sniðmát fyrir kvittanir sem sendar eru í tölvupósti þau sömu og skrefin við stofnun sniðmáta fyrir önnur færslutilvik. Eftirfarandi breytingar eru hins vegar áskildar:

- Kenni tölvupósts í sniðmátinu fyrir tölvupóst verður að vera **emailRecpt**.
- Texti kvittunar er settur inn í tölvupóst með því að nota staðgengilinn **%message%**. Til að tryggja að meginmál kvittunar sé rétt myndþýtt skal umlykja **%message%** staðgenglana með HTML-merkjunum **&lt;pre&gt;** og **&lt;/pre&gt;**.
- Línuskilum í HTML fyrir síðuhaus og síðufót tölvupóstsins er breytt í HTML-merkin **&lt;br/&gt;** þannig að meginmál kvittunarinnar sé rétt myndþýtt. Til að útiloka óæskilegt lóðrétt bil í tölvupóstkvittunum skal fjarlægja línuskil frá hvaða stað sem er í HTML þar sem ekki er krafist lóðrétts bils.

Frekari upplýsingar um hvernig kvittanir í tölvupósti eru settar upp eru í [Setja upp kvittanir í tölvupósti](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-email-receipts).

## <a name="upload-the-email-html"></a>Hlaða upp HTML-tölvupósti

Eftir að búið er að búa til og prófa HTML fyrir meginmál skeytisins verður að hlaða því upp í Commerce Headquarters. Sem stendur er ekki hægt að flytja út HTML-tölvupóst. Þess vegna þarf að vinna með aðalafritið af HTML fyrir utan Commerce Headquarters.

Til að hlaða upp nýju eða breyttu HTML fyrir sniðmát fyrir tölvupóst skal fylgja þessum skrefum.

1. Í Commerce Headquarters þarf að opna **Smásala og viðskipti \> Uppsetning höfuðstöðva \> Tölvupóstssniðmát fyrirtækis**.
1. Veldu línuna fyrir tungumálið sem þú vilt bæta við eða skipta út HTML fyrir. Einnig er hægt að velja **Nýtt** til að stofna nýja línu fyrir nýtt tungumál.
1. Veljið **Breyta**.
1. Í svarglugganum sem birtist skal smella á **Fletta**. Flettið á HTML-skjalið sem á að hlaða upp, veljið það og veljið síðan **Opna**.
1. Veldu **Hlaða upp**.
1. Eftir að HTML tölvupósts notanda birtist í forskoðunarglugganum skal velja **Í lagi**.
1. Gangið úr skugga um að gátreiturinn **Með meginmáli** sé valinn fyrir línuna.

Ef Commerce Headquarters hefur þegar verið skilgreint til að senda tölvupóst verður nýr eða uppfærður tölvupóstur sendur á alla viðskiptavini sem framkvæma færslu sem ræsir tilvik sem er varpað á sniðmátið.

Frekari upplýsingar um hvernig á að skilgreiningu tölvupósts í Dynamics 365 Commerce er að finna í [Skilgreining og sending tölvupósts](../fin-ops-core/fin-ops/organization-administration/configure-email.md).

## <a name="additional-resources"></a>Frekari upplýsingar 

[Setja upp forstillingu tilkynningar í tölvupósti](email-notification-profiles.md)

[Skilgreining og sending tölvupósts](../fin-ops-core/fin-ops/organization-administration/configure-email.md)

[Setja upp tölvupóst innhreyfingar](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-email-receipts)

[Senda kvittanir í tölvupósti frá Modern POS ](email-receipts.md)
