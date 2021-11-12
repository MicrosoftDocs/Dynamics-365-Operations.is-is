---
title: Stofna sniðmát fyrir tölvupóst fyrir færslutilvik
description: Þetta efnisatriði lýsir því hvernig á að búa til, hlaða upp og skilgreina tölvupóstssniðmát fyrir færslutilvik í Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 10/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 69ba8821cde6788d6e0accb37288f92acdfc776c
ms.sourcegitcommit: 6bf9e18989e6d77497a9dda1c362f324b3c2fbf2
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/27/2021
ms.locfileid: "7713798"
---
# <a name="create-email-templates-for-transactional-events"></a>Stofna sniðmát fyrir tölvupóst fyrir færslutilvik

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Þetta efnisatriði lýsir því hvernig á að búa til, hlaða upp og skilgreina tölvupóstssniðmát fyrir færslutilvik í Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce býður upp á tilbúna lausn fyrir tölvupóstsendingar sem tilkynna viðskiptavini um færslutilvik. Til dæmis er hægt að senda tölvupósta þegar pöntun er gerð, er tilbúin til afhendingar eða hefur verið send. Þetta efnisatriði lýsir skrefum til að búa til, hlaða upp og skilgreina sniðmát fyrir tölvupóst sem eru notuð til að senda færslutengdan tölvupóst.

## <a name="notification-types"></a>Tilkynningagerðir

Tilkynningar geta verið stilltar á að láta viðskiptavini vita í gegnum tölvupóst þegar tiltekin tilvik koma upp sem hluti af pöntunar- og viðskiptavinaferlinu. Til að stilla tilkynningar þarf að varpa sniðmáti fyrir tölvupóst í tilkynningargerð með því að tilkynningaforstillingu fyrir Commerce-tölvupóst. Upplýsingar um hvernig á að setja upp forstillingar tölvupóststilkynninga skal skoða [Setja upp forstillingu tilkynningar í tölvupósti](email-notification-profiles.md).

Dynamics 365 Commerce styður eftirfarandi tilkynningargerðir.

### <a name="order-created"></a>Pöntun búin til

Tilkynningagerðin *Pöntun búin til* er ræst þegar ný sölupöntun er búin til í Commerce Headquarters.

> [!NOTE]
> Tilkynningagerðin Pöntun búin til er ekki ræst fyrir staðgreiðslufærslur sem eiga sér stað á afgreiðslukassa. Í því tilviki er í staðinn kvittun send í tölvupósti og/eða prentuð. Frekari upplýsingar er að finna í [Senda kvittanir í tölvupósti úr Modern POS (MPOS)](email-receipts.md).

### <a name="order-confirmed"></a>Pöntun staðfest

Tilkynningagerðin *pöntun staðfest* er ræst þegar skjal pöntunarstaðfestingar er búið til fyrir sölupöntun úr Commerce Headquarters.

### <a name="picking-completed"></a>Tiltekt lokið

Tilkynningagerðin *tiltekt lokið* er ræst þegar tiltektarlisti fyrir pöntun er merktur sem lokið í Commerce Headquarters.

> [!NOTE]
> Tilkynningagerðin Tiltekt lokið er ekki ræst þegar vara er merkt sem tínd á afgreiðslukassa.

### <a name="packing-completed"></a>Pökkun lokið

Tilkynningagerðin *pökkun lokið* er ræst þegar skjal fylgiseðils er búið til fyrir pöntun í Commerce Headquarters á afgreiðslukassa.

Tilkynningargerðin Pökkun lokið styður eftirfarandi viðbótarstaðgengla tölvupósts til að koma á „má sækja pöntun“ og uppflettingaraðgerð pöntunar úr færslutölvupóstum.

| Staðgengilsheiti    | Notkun |
| ------------------- | ------- |
| `pickupstorename`     | Heiti verslunarinnar þar sem hægt er að sækja pöntunina. |
| `pickupstoreaddress`  | Aðsetur verslunarinnar þar sem hægt er að sækja pöntunina. |
| `pickupstorehourfrom` | Opnunartími verslunar þar sem er sótt. |
| `pickupstorehourto`   | Lokunartími verslunar þar sem er sótt. |
| `pickupchannelid`     | Rásarkenni verslunar þar sem er sótt. |
| `packingslipid`      | Auðkenni fylgiseðilsins fyrir pöntunina sem verður sótt. |
| `confirmationid`      | Staðfestingarkenni pöntunar sem verður sótt. (Þetta auðkenni er stundum kallað tilvísunarkenni rásar.) |

Frekari upplýsingar um eiginleika innskráningar og uppflettingar viðskiptavinar er að finna í [Setja upp landfræðilega greiningu og áframsendingu](geo-detection-redirection.md) og [Virkja uppflettingu pöntunar fyrir gestakaup](order-lookup-guest.md).

### <a name="order-ready-for-pickup"></a>Pöntun tilbúin til afhendingar

Tilkynningagerðin *má sækja pöntun* er ræst þegar pöntun er merkt sem pökkuð og afhendingarmátinn er stilltur á **Viðskiptavinur sækir** í einni eða fleiri pöntunarlínum.

> [!NOTE]
> Tilkynningargerðin Má sækja pöntun hefur verið úrelt og í staðinn er komin tilkynningargerðin Pökkun lokið. Þessi tilkynningargerð er sérstillt af afhendingarmáta.

### <a name="order-shipped"></a>Pöntun send

Tilkynningagerðin *pöntun send* er ræst þegar pöntun sem er með annan afhendingarmáta en að sækja í verslun er reikningsfærð.

> [!NOTE]
> Tilkynningargerðin Pöntun send hefur verið úrelt og í staðinn er komin tilkynningargerðin Pöntun reikningsfærð. Þessi tilkynningargerð er sérstillt af afhendingarmáta.

### <a name="order-invoiced"></a>Pöntun reikningsfærð

Tilkynningargerð *pöntun reikningsfærð* er ræst þegar pöntun er reikningsfærð á sölustað eða í Commerce Headquarters.

### <a name="issue-gift-card"></a>Gefa út gjafakort

Tilkynningargerðin *gefa út gjafakort* er ræst þegar sölupöntun sem inniheldur afurð af gjafakortsgerðinni er reikningsfærð.

> [!NOTE]
> Tilkynningapóstur um útgefið gjafakort er sent á viðtakanda gjafakortsins. Viðtakandi gjafakortsins er tilgreindur í Commerce Headquarters, í stakri sölupöntunarlínu á flipanum **Pökkun** undir **Upplýsingar um línu**. Hægt er að tilgreina hann annaðhvort handvirkt eða forritað.

Tilkynningagerðin Gefa út gjafakort styður eftirfarandi viðbótarstaðgengla.

| Staðgengilsheiti      | Notkun |
| --------------------- | ------- |
| `giftcardnumber`        | Gjafakortsnúmer, fyrir afurðir af gerðinni gjafakort. |
| `giftcardbalance`       | Staða gjafakorts, fyrir afurðir af gerðinni gjafakort. |
| `giftcardmessage`       | Gjafakortsskilaboð, fyrir afurðir af gerðinni gjafakort. |
| `giftcardpin`         | PIN-númer gjafakortsins, fyrir afurðir af gerðinni gjafakort. (Þessi staðgengill er tilgreindur fyrir ytri gjafakort.) |
| `giftcardexpiration`    | Lokadagur gjafakortsins, fyrir afurðir af gerðinni gjafakort. (Þessi staðgengill er tilgreindur fyrir ytri gjafakort.) |
| `giftcardrecipientname` | Heiti viðtakanda gjafakortsins, fyrir afurðir af gerðinni gjafakort. |
| `giftcardbuyername`     | Heiti kaupanda gjafakortsins, fyrir afurðir af gerðinni gjafakort. |

Frekari upplýsingar um gjafakort er að finna í [Netverslun með stafræn gjafakort](digital-gift-cards.md) og [Stuðningur við utanaðkomandi gjafakort](dev-itpro/gift-card.md).

### <a name="order-cancellation"></a>Pöntun afturkölluð

Tilkynningagerðin *pöntun afturkölluð* er ræst þegar pöntun er afturkölluð í Commerce Headquarters.

### <a name="customer-created"></a>Viðskiptavinur stofnaður

Tilkynningagerðin *viðskiptavinur stofnaður* er ræst þegar ný eining viðskiptavinar er búin til í Commerce Headquarters.

### <a name="b2b-prospect-approved"></a>B2B-viðfang samþykkt

Tilkynningagerðin *B2B-viðfang samþykkt* er ræst þegar beiðni um innleiðingu viðfangs er samþykkt í Commerce Headquarters. Frekari upplýsingar um hvernig á að samþykkja eða hafna B2B-viðföngum er að finna í [Setja upp notanda sem stjórnanda fyrir nýjan samstarfsaðila](b2b/manage-b2b-users.md#set-up-the-administrator-user-for-a-new-business-partner). 

Tilkynningagerðin B2B-viðfang samþykkt styður eftirfarandi viðbótarstaðgengla.

| Staðgengilsheiti | Notkun                                                      |
| ---------------- | ------------------------------------------------------------ |
| `firstname`       | Fornafn B2B-viðfangs er fært inn í umsóknina. |
| `lastname`         | Eftirnafn B2B-viðfangs er fært inn í umsóknina. |
| `company`          | Heiti fyrirtækis umsækjanda eins og það er fært inn í umsóknina. |
| `email`            | Netfang viðfangs er fært inn í umsóknina.   |
| `zipcode`          | Póstnúmer fyrir aðalaðsetur viðfangs. |
| `comments`         | Athugasemdin sem viðfangið færði inn í umsóknina. |
| `storename`        | Heiti rásarinnar þar sem viðfangið er stofnað. |
| `storeurl`         | Sjálfgefið autt. Búa þarf til sérsniðna viðbót til að nota þennan staðgengil. |

### <a name="b2b-prospect-approved"></a>B2B-viðfang samþykkt

Tilkynningagerðin *B2B-viðfangi hafnað* er ræst þegar beiðni um innleiðingu viðfangs er hafnað í Commerce Headquarters. Frekari upplýsingar um hvernig á að samþykkja eða hafna B2B-viðföngum er að finna í [Setja upp notanda sem stjórnanda fyrir nýjan samstarfsaðila](b2b/manage-b2b-users.md#set-up-the-administrator-user-for-a-new-business-partner). 

Tilkynningagerðin B2B-viðfangi hafnað styður eftirfarandi viðbótarstaðgengla.

| Staðgengilsheiti | Notkun                                                      |
| ---------------- | ------------------------------------------------------------ |
| `firstname`        | Fornafn B2B-viðfangs er fært inn í umsóknina. |
| `lastname`         | Eftirnafn B2B-viðfangs er fært inn í umsóknina. |
| `company`          | Heiti fyrirtækis umsækjanda eins og það er fært inn í umsóknina. |

## <a name="create-an-email-template"></a>Stofna sniðmát fyrir tölvupóst

Áður en hægt er að varpa tilteknu færslutilviki í tölvupóstssniðmát verður að stofna sniðmátið.

Til að stofna tölvupóstsniðmát, skal fylgja eftirfarandi skrefum.

1. Í höfuðstöðvum Commerce skal opna **Smásala og viðskipti \> Uppsetning höfuðstöðva \> Tölvupóstssniðmát fyrirtækis** eða **Fyrirtækisstjórnun \> Uppsetning \> Tölvupóstssniðmát fyrirtækis**.
1. Veljið **Nýtt**.
1. Undir **Almennt** skal stilla eftirfarandi reiti:

    - **Kenni tölvupósts** – Kenni tölvupósts er einkvæmt kennimerki fyrir sniðmát. Það er gildið sem er sýnt þegar sniðmát er valið til að varpa í tilvik.
    - **Lýsing á tölvupósti** – hægt er að nota þennan valfrjálsa reit fyrir lýsingu á sniðmátinu. Gildið sem fært er inn birtist aðeins í Commerce Headquarters.
    - **Nafn sendanda** – heitið sem fært er inn birtist í reitnum „Frá“ í flestum tölvupóstforritum.
    - **Netfang sendanda** – færið inn netfangið sem á að nota fyrir tölvupóst sem er sendur með því að nota þetta sniðmát.
    - **Sjálfgefinn tungumálakóði** – Þessi reitur tilgreinir staðfærða útgáfu tölvupóstsins sem er sjálfgefið send, ef ekkert tungumál er í rásinni sem ræsir þetta sniðmát.

1. Undir **Efni tölvupóstskilaboða** skal velja **Nýtt**.
1. Í reitinn **Tungumál** er fært inn tungumálið fyrir sniðmát tölvupósts. Hægt er að bæta við fleiri tungumálum og staðfærðum sniðmátum síðar.
1. Í reitnum **Efni** skal færa inn efni tölvupóstsins sem á að birtast í efnisreit tölvupóstsins.
1. Veljið **Breyta** til að hlaða upp tölvupóstssniðmátinu.

## <a name="create-an-email-message-body-by-using-html"></a>Meginmál tölvupóstskilaboðanna búið til með HTML

Meginmál tölvupóstsins er skrifað í HTML. Hægt er að nota allar útlit, stíl og vörumerki sem HTML og stölluð stílblöð (CSS) leyfa. Einnig er hægt að nota myndir ef þær eru hýstar á vefsvæði sem er í boði opinberlega. Til að bæta við mynd skal slá inn vefslóð myndarinnar í **src**-eigind HTML **&lt;img&gt;**-merkisins.

> [!NOTE]
> Tölvupóstforrit nota útlit og stíltakmarkanir sem gætu krafist leiðréttingar í HTML og CSS sem er notað fyrir meginmál skilaboðanna. Við mælum með því að notandi kynni sér bestu starfsvenjur þegar HTML er búið til sem flest tölvupóstforrit styðja.

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

| Staðgengilsheiti     | Notkun                                                      |
| -------------------- | ------------------------------------------------------------ |
| `customername`         | Nafn viðskiptavinarins sem sendi inn pöntunina.               |
| `customeraddress`      | Aðsetur viðskiptavinarins.                                 |
| `customeremailaddress` | Netfangið sem viðskiptavinurinn færði inn við greiðsluferli.     |
| `salesid`              | Sölukenni pöntunar.                                   |
| `orderconfirmationid`  | Krossrásarkennið sem var búið til við stofnun pöntunar.   |
| `channelid`            | Kenni smásölu- eða netrásar sem pöntunin fór í gegnum. |
| `deliveryname`         | Nafnið sem er tilgreint fyrir afhendingaraðsetrið.         |
| `deliveryaddress`      | Afhendingaraðsetur fyrir sendar pantanir.                     |
| `deliverydate`         | Afhendingardagsetning.                                           |
| `shipdate`             | Sendingardagsetning.                                               |
| `modeofdelivery`       | Afhendingarmáti pöntunarinnar.                              |
| `ordernetamount`       | Heildarupphæðin fyrir pöntunina, að frádregnum heildarskatti.         |
| `discount`            | Heildarafsláttur pöntunarinnar.                            |
| `charges`              | Heildargjöld fyrir pöntunina.                             |
| `tax`                  | Heildarskattur fyrir pöntunina.                                 |
| `total`                | Heildarupphæð pöntunarinnar.                              |
| `storename`            | Heiti verslunarinnar þaðan sem pöntunin er upprunnin.            |
| `storeaddress`         | Aðsetur verslunarinnar þaðan sem pöntunin er upprunnin.              |
| `storeopenfrom`        | Opnunartími verslunarinnar þaðan sem pöntunin er upprunnin.         |
| `storeopento`          | Lokunartími verslunarinnar þaðan sem pöntunin er upprunnin.         |
| `pickupstorename`      | Heiti verslunarinnar þar sem pöntunin verður sótt.\*   |
| `pickupstoreaddress`   | Aðsetur verslunarinnar þar sem pöntunin verður sótt.\* |
| `pickupopenstorefrom`  | Opnunartími verslunarinnar þar sem pöntunin verður sótt.\* |
| `pickupopenstoreto`    | Lokunartími verslunarinnar þar sem pöntunin verður sótt.\* |
| `pickupchannelid`     | Rásarauðkenni verslunar sem er tilgreint fyrir afhendingarmáta.\* |
| `packingslipid`        | Auðkenni fylgiseðilsins sem var búinn til þegar línum í pöntun var pakkað.\* |

\* Þessir staðgenglar skila aðeins gögnum þegar þeir eru notaðir fyrir tilkynningagerðina **Pöntun tilbúin til afhendingar**. 

### <a name="order-line-placeholders-sales-line-level"></a>Staðgenglar pöntunarlínu (sölulínustig)

Eftirfarandi staðgenglar sækja og sýna gögn fyrir einstakar afurðir (línur) á sölupöntuninni.

| Staðgengilsheiti               | Notkun |
|--------------------------------|-------------------|
| `productid`                      | <p>Kenni afurðarinnar. Þetta auðkenni tekur til afbrigða.</p><p><strong>Athugasemd:</strong> Þessi staðgengill hefur verið afskráður í hag `lineproductrecid`.</p> |
| `lineproductrecid`               | Kenni afurðarinnar. Þetta auðkenni tekur til afbrigða. Það auðkennir hlut á afbrigðastigi. |
| `lineitemid`                     | Vörustigsauðkenni afurðarinnar. (Þetta auðkenni tekur ekki til afbrigða.) |
| `lineproductvariantid`           | Kenni afurðarinnar eða afurðarafbrigðisins. |
| `lineproductname`                | Nafn vörunnar. |
| `lineproductdescription`         | Lýsing á afurðinni. |
| `linequantity`                   | Fjöldi eininga sem voru pantaðar fyrir línuna, auk mælieiningarinnar (til dæmis **ea** eða **par**). |
| `lineunit`                       | Mælieiningin fyrir línuna. |
| `linequantity_withoutunit`       | Einingafjöldi sem var pantaður fyrir línuna, án mælieiningar. |
| `linequantitypicked`             | Þegar **PickOrder** viðburðurinn er notaður, fjöldi eininga sem voru teknar til. Annars, **0** (núll). |
| `linequantitypicked_withoutunit` | Þegar **PickOrder** viðburðurinn er notaður, fjöldi eininga sem voru tíndar, án mælieiningar. Annars, **0** (núll). |
| `linequantitypacked`             | Þegar tilvikin **PackOrder** og **Pöntun tilbúin til afhendingar** eru notuð, fjöldi eininga sem var pakkað. Annars, **0** (núll). |
| `linequantitypacked_withoutuom`  | Þegar tilvikin **PackOrder** og **Pöntun tilbúin til afhendingar** eru notuð, fjöldi eininga sem var pakkað, án mælieiningarinnar. Annars, **0** (núll). |
| `linequantityshipped`            | Alltaf **0**, nema þegar tiltekin tilvik eru notuð, eins og lýst er í næstu línu. |
| `linequantityshipped_withoutuom` | Þegar **ShipOrder** viðburðurinn er notaður, fjöldi eininga sem voru tíndar, án mælieiningar. Annars, **0** (núll). |
| `lineprice`                      | Verð einnar einingar. |
| `linenetamount`                  | Verð línunnar eftir að einingafjöldi og afsláttur eru notuð. |
| `linediscount`                   | Afsláttur fyrir einstaka einingu. |
| `lineshipdate`                   | Sendingardagsetning fyrir línuna. |
| `linedeliverydate`               | Afhendingardagsetning línunnar. |
| `linedeliverymode`               | Afhendingarmáti fyrir línuna. |
| `linedeliveryaddress`            | Afhendingaraðsetur fyrir línuna. |
| `linepickupdate`                 | Afhendingardagur sem viðskiptavinur tilgreindi, fyrir pantanir sem nota afhendingarmáta. |
| `linepickuptimeslot`             | Afhendingartímabilið sem viðskiptavinur tilgreindi, fyrir pantanir sem nota afhendingarmáta. |
| `giftcardnumber`                 | Gjafakortsnúmer, fyrir afurðir af gerðinni gjafakort. |
| `giftcardbalance`                | Staða gjafakorts, fyrir afurðir af gerðinni gjafakort. |
| `giftcardmessage`                | Gjafakortsskilaboð, fyrir afurðir af gerðinni gjafakort. |
| `giftcardpin`                    | Festa gjafakortsins, fyrir afurðir af gerðinni gjafakort. (Þessi staðgengill er tilgreindur fyrir ytri gjafakort.) |
| `giftcardexpiration`             | Lokadagur gjafakortsins, fyrir afurðir af gerðinni gjafakort. (Þessi staðgengill er tilgreindur fyrir ytri gjafakort.) |
| `giftcardrecipientname`          | Heiti viðtakanda gjafakortsins, fyrir afurðir af gerðinni gjafakort. |
| `giftcardbuyername`              | Heiti kaupanda gjafakortsins, fyrir afurðir af gerðinni gjafakort. |

### <a name="format-of-order-line-placeholders-in-the-email-message-body"></a>Snið staðgengla pöntunarlínu í meginmáli tölvupóstskilaboðanna

Þegar HTML er búið til fyrir einstakar pöntunarlínur í meginmáli tölvupóstskilaboðanna, umlykja endurtekna HTML-blokk og staðgengla fyrir línurnar með eftirfarandi staðgenglum. Taktu eftir að staðgenglarnir eru innan í HTML-athugasemdamerkjum.

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

- Staðgengillinn **%message%** er notaður til að setja texta kvittunar inn í tölvupóstinn. Til að tryggja að meginmál kvittunar sé rétt myndþýtt skal umlykja **%message%** Staðgenglana með HTML-merkjunum **&lt;pre&gt;** og **&lt;/pre&gt;**.
- Staðgengilinn **%receiptid%** er hægt að nota til að sýna QR-kóða eða strikamerki sem stendur fyrir kvittunarkennið. (QR-kóðar og strikamerki eru mynduð gagnvirkt og með þjónustuð af þriðja aðila.) Frekari upplýsingar um hvernig á að sýna QR-kóða eða strikamerki í tölvupóstkvittun er að finna í [Bæta QR-kóða eða strikamerki við tölvupósta sem tengjast færslum eða kvittunum](add-qr-code-barcode-email.md).

## <a name="upload-the-email-html"></a>Hlaða upp HTML-tölvupósti

Eftir að búið er að búa til og prófa HTML fyrir meginmál skeytisins verður að hlaða því upp í Commerce Headquarters. Sem stendur er ekki hægt að flytja út HTML-tölvupóst. Þess vegna þarf að vinna með aðalafritið af HTML fyrir utan Commerce Headquarters.

Til að hlaða upp nýju eða breyttu HTML fyrir sniðmát fyrir tölvupóst skal fylgja þessum skrefum.

1. Í Commerce Headquarters þarf að opna **Smásala og viðskipti \> Uppsetning höfuðstöðva \> Tölvupóstssniðmát fyrirtækis**.
1. Veldu línuna fyrir tungumálið sem þú vilt bæta við eða skipta út HTML fyrir. Einnig er hægt að velja **Nýtt** til að stofna nýja línu fyrir nýtt tungumál.
1. Veljið **Breyta**.
1. Í svarglugganum sem birtist skal smella á **Fletta**. Flettið á HTML-skjalið sem á að hlaða upp, veljið það og veljið síðan **Opna**.
1. Veldu **Hlaða upp**.
1. Eftir að HTML tölvupósts notanda birtist í forskoðunarglugganum skal velja **Í lagi**.
1. Gakktu úr skugga um að gátreiturinn **Er með meginmál** sé valinn fyrir línuna.

Ef Commerce Headquarters hefur þegar verið skilgreint til að senda tölvupóst verður nýr eða uppfærður tölvupóstur sendur á alla viðskiptavini sem framkvæma færslu sem ræsir tilvik sem er varpað á sniðmátið.

Frekari upplýsingar um hvernig á að skilgreiningu tölvupósts í Dynamics 365 Commerce er að finna í [Skilgreining og sending tölvupósts](../fin-ops-core/fin-ops/organization-administration/configure-email.md).

## <a name="additional-resources"></a>Frekari upplýsingar 

[Setja upp forstillingu tilkynningar í tölvupósti](email-notification-profiles.md)

[Skilgreining og sending tölvupósts](../fin-ops-core/fin-ops/organization-administration/configure-email.md)

[Setja upp tölvupóst innhreyfingar](/dynamicsax-2012/appuser-itpro/set-up-email-receipts)

[Senda kvittanir í tölvupósti frá Modern POS ](email-receipts.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
