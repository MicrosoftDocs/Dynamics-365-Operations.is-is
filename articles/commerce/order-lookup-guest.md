---
title: Virkja uppflettingu pöntunar fyrir gestakaup
description: Þessi grein lýsir því hvernig á að virkja pöntunarleit fyrir gestaafgreiðslur í Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-08-15
ms.dyn365.ops.version: Release 10.0.22
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 757e83887e318dd6aa54106fb78305f1d94e0f90
ms.sourcegitcommit: e25fe4228add88dd37f4f38ece86979e1c621f6a
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/01/2022
ms.locfileid: "9734268"
---
# <a name="enable-order-lookup-for-guest-checkouts"></a>Virkja uppflettingu pöntunar fyrir gestakaup

[!include [banner](includes/banner.md)]

Þessi grein lýsir því hvernig á að virkja pöntunarleit fyrir gestaafgreiðslur í Microsoft Dynamics 365 Commerce.

Pöntunarútlit fyrir útritun gesta gerir viðskiptavinum sem ganga frá kaupum sem gestanotendur kleift að fletta upp pöntunum sínum. Uppflettimöguleiki pöntunar er gagnlegur þegar viðskiptavinir vilja framkvæma aðgerðir eins og að athuga uppfyllingarstöðu vöru í pöntun, staðfesta heimilisfangið sem pöntun var send á, endurpanta vöru eða staðfesta verslunina þar sem pöntunin verður sótt.

Viðskiptavinir sem leggja inn pantanir sem skráðir notendur geta séð pöntunarupplýsingar sínar þegar þeir eru innskráðir, en viðskiptavinir sem nota greiðsluferlið sem gestir til að ganga frá pöntunum geta það ekki. Þegar uppflettieiginleiki pöntunar fyrir greiðsluferli gesta er hinsvegar virkjað býður hann upp á skjámynd sem viðskiptavinir geta notað til að leita að pöntunum sem þeir gerðu sem gestir. Í þessari skjámynd slá viðskiptavinir inn auðkenni pöntunarstaðfestingar og (valfrjálst) netfangið sem þeir gáfu upp í greiðsluferlinu.

Að auki er einnig hægt að hafa með tengil eða hnapp sem fer með viðskiptavininn beint á síðu pöntunarupplýsinga fyrir pöntunina hans í öllum tölvupóstum sem tengjast pöntunum. Þessi tengill eða hnappur virkar fyrir pantanir sem bæði skráðir notendur og gestanotendur gera.

## <a name="turn-on-necessary-features-in-commerce-headquarters"></a>Kveikja á nauðsynlegum eiginleikum í Commerce Headquarters

Til að virkja uppflettingu pöntunar fyrir greiðsluferli gesta þarf að kveikja á eftirfarandi eiginleikum í **Vinnusvæði \> Eiginleikastjórnun** í Commerce Headquarters.

| Eiginleiki | Notkun |
|---------|---------|
| Retail eiginleiki fyrir leit nafnlauss notanda að pöntunarupplýsingum | Þessi eiginleiki birtir notandaviðmótið í færibreytum Commerce sem gerir þér kleift að virkja API fyrir uppflettingu pöntunar fyrir notendur sem eru ekki auðkenndir og stilla hvernig persónuupplýsingar eru sýndar. |
| Virkja myndun á öflugra tilvísunarkenni rásar | Þessi eiginleiki býr til öruggara 12 stafa tilvísunarauðkenni rásar (auðkenni pöntunarstaðfestingar) sem hægt er að flytja inn í fyrirspurnarstrenginn þegar flett er upp á pöntuninni. |
| Búa til samræmt snið tilvísunarkennis rásar milli rása | Þessi eiginleiki býr til öruggt tilvísunarnúmer rásar fyrir pantanir sem eru lagðar fram í gegnum vefsvæði rafrænna viðskipta, sölustað smásölu (POS) eða símaver. Áður en hægt er að kveikja á þessum eiginleika verður að kveikja á eiginleikanum **Virkja myndun á öflugra tilvísunarkenni rásar**. |

Þegar þú hefur kveikt á eiginleikanum **Virkjunareiginleiki fyrir leit nafnlauss notanda smásölu að pöntunarupplýsingum** þarftu að virkja API sem styður nafnlausa uppflettingu pöntunar í Commerce Headquarters. Opnið **Smásala og viðskipti \> Uppsetning höfuðstöðva \> Færibreytur \> Pantanir viðskiptavinar**. Á síðunni **Pantanir viðskiptavinar**, í flýtiflipanum **Leita að pöntun**, skal stilla valkostinn **Virkja ósannvottaða uppflettingu pöntunar** á **Já** eins og sýnt er á eftirfarandi mynd.

## <a name="manage-the-display-of-personal-data"></a>Stjórna birtingu persónuupplýsinga

Flýtiflipinn **Leita að pöntun** á síðunni **Pantanir viðskiptavina** í Commerce Headquarters inniheldur reitinn **Hafa með persónuupplýsingar í uppflettingu gesta á pöntun** sem gerir þér kleift að stjórna því hvort viðskiptavinir fái að sjá persónuupplýsingar. Þessar persónuupplýsingar innihalda heimilisfang viðtakanda og síðustu fjóra tölustafina á kreditkortanúmeri viðskiptavinar. Persónuupplýsingar eru sjálfgefið ekki sýndar viðskiptavinum þegar nafnlaus uppfletting pöntunar er virkjuð. Eftirfarandi tafla lýsir tiltækum valkostum.

| Valkostur | Niðurstaða |
|--------|--------|
| Aldrei | Sjálfgefna gildið. Engar persónuupplýsingar koma fram í uppflettingum pantana. Þegar skráðir notendur sem eru innskráðir fletta upp pöntun sem þeir stofnuðu meðan þeir voru innskráðir, geta þeir séð persónulegar upplýsingar sínar. |
| Aðeins pantanir gesta | Persónuupplýsingar koma fram í uppflettingum pantana fyrir pantanir sem viðskiptavinir stofnuðu sem gestir. Ef skráður notandi stofnaði pöntun verður sá notandi að skrá sig inn til að sjá persónuupplýsingarnar sínar. |
| Allar pantanir | Persónuupplýsingar koma fram í öllum uppflettingum pantana. |

> [!NOTE]
> Þessir valkostir skera úr um hvenær persónuupplýsingar á borð við heimilisfang viðskiptavinar og síðustu fjórir tölustafirnir í kreditkortanúmeri viðskiptavinar eru sýndar nafnlausum gestanotendum. Til að vernda friðhelgi skráðra viðskiptavina mælum við með því að þú veljir valkostinn **Aðeins pantanir gesta**. Öruggasti valkosturinn er þó **Aldrei**.

Eftir að þú hefur breytt gildi á **Láttu persónuupplýsingar fylgja með í uppflettingu gestapöntunar** reit, þú verður að keyra starf 1070 (**Rásar stillingar**) í höfuðstöðvum viðskipta með því að fara til **Verslun og verslun \> Upplýsingatækni í smásölu og viðskiptum \> Dreifingaráætlun**.

## <a name="configure-the-order-lookup-module"></a>Skilgreina uppflettieiningu pöntunar

Uppflettieining pantana í einingasafni Commerce er notuð fyrir myndræna framsetningu skjámyndar sem gestanotendur nota til að fletta upp á pöntunum. Hægt er að hafa uppflettieiningu pantana með í hólfi meginmáls á hvaða síðu sem er sem krefst ekki innskráningar viðskiptavinar. Frekari upplýsingar um hvernig á að skilgreina eininguna er að finna í [Uppflettieining pantana](order-lookup-module.md).

## <a name="configure-the-order-details-page"></a>Stilltu síðuna með pöntunarupplýsingum

Áður en gestanotendur geta skoðað pöntunarupplýsingar sínar verður að stilla pöntunarupplýsingasíðuna á netverslunarsíðunni þinni þannig að hún krefjist ekki innskráningar. Til að slökkva á innskráningarkröfunni fyrir pöntunarupplýsingasíðuna þína skaltu opna síðuna í Commerce site builder, velja **Sjálfgefin síða (áskilið)** rauf í tré útsýni, og hreinsa **Þarfnast innskráningar?** gátreitinn neðst á eiginleikaglugganum hægra megin.

## <a name="add-a-link-to-order-details-in-transactional-emails"></a>Bættu við tengli til að panta upplýsingar í viðskiptatölvupósti

Í pöntunartengdum tölvupóstum geturðu gefið upp hlekk eða hnapp sem fer með viðskiptavini á pöntunarupplýsingasíðuna fyrir pöntunina. Til að bæta við þessum hlekk eða hnappi, búðu til HTML tengil sem vísar á pöntunarupplýsingasíðuna á netverslunarsíðunni þinni og sendu pöntunarstaðfestingarauðkenni og netfang viðskiptavinar sem vefslóðarfæribreytur, eins og sýnt er í eftirfarandi dæmi.

`<a href="https://[domain]/[orderdetailspage]?confirmationId=%orderconfirmationid%&propertyName=email&propertyValue=%customeremailaddress%" target="_blank">View my order status</a>`

> [!NOTE]
> Til að virkja pöntunarleitareiginleikann skaltu ganga úr skugga um að **Tilvitnanir** lykill er virkjaður undir **Leyfisstillingar** > **Stillingarlyklar**.
>
>![Stillingar leyfislykla tilboða verða að vera virkjaðar](./media/Quotations_License_Key_Configuration.png)

## <a name="additional-resources"></a>Frekari upplýsingar

[Uppflettieining pantana](order-lookup-module.md)

[Setja upp forstillingu tilkynningar í tölvupósti](email-notification-profiles.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
