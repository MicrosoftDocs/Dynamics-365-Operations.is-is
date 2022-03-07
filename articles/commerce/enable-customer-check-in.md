---
title: Virkja innskráningartilkynningar viðskiptavinar á sölustað (POS)
description: Í þessu efnisatriði er lýst hvernig á að virkja tilkynningar um innskráningu viðskiptavina á Microsoft Dynamics 365 Commerce sölustað.
author: bicyclingfool
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: b42dc7766f8a69a7409c28d21b49cc96eca18dd4
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271426"
---
# <a name="enable-customer-check-in-notifications-in-point-of-sale-pos"></a>Virkja innskráningartilkynningar viðskiptavinar á sölustað (POS)

[!include [banner](includes/banner.md)]

Í þessu efnisatriði er lýst hvernig á að virkja tilkynningar um innskráningu viðskiptavina á Microsoft Dynamics 365 Commerce sölustað.

Í tölvupóstunum „sækja má pöntun“ geta fyrirtæki gefið upp tengil eða hnapp sem gerir viðskiptavinum kleift að tilkynna versluninni að þeir séu í nágrenninu og eru að bíða eftir pakkinn verður færður þeim fyrir utan. Viðskiptavinir fá síðan staðfestingu á innskráningu og verslunin fær tilkynningu í formi verks í forriti sölustaðar. Þetta verk virkar sem kvaðning fyrir sölustarfsfólk um að fara með pöntunina að bifreið viðskiptavinar. Því þarf viðskiptavinurinn ekki að fara inn í búðina.

Verkflæði innskráningar viðskiptavinar getur einnig verið skilgreint til að safna viðbótarupplýsingum frá viðskiptavinum á borð við bílastæðanúmer, gerð bifreiðar og litur hennar og leiðbeiningar um afhendingu. Starfsmaður smásöluverslunar getur notað þessar upplýsingar til að auðvelda uppfyllingu pöntunar.

## <a name="enable-customer-check-in"></a>Virkja innskráningu viðskiptavinar

Þegar kveikt er á innskráningareiginleika viðskiptavinar býr Commerce til kenni pöntunarstaðfestingar (einnig þekkt sem tilvísunarkenni rásarinnar). Það býr einnig til kenni pöntunarstaðfestingar fyrir pantanir sem eru stofnaðar í gegnum rás sölustaðar eða símavers. 

Til að kveikja á innskráningareiginleika viðskiptavinar í Commerce Headquarters skal fylgja þessum skrefum.

1. Opna skal **Vinnusvæði \> Eiginleikastjórnun**.
2. Leitið að eiginleikanum **Búa til samræmt snið tilvísunarkennis rásar milli rása**. 
3. Veljið eiginleikann og veljið svo **Virkja núna** á eiginleikasvæðinu. 

## <a name="create-a-check-in-confirmation-page"></a>Búa til staðfestingarsíðu innskráningar

Á svæði rafrænna viðskipta þarf að búa til nýja síðu sem þjónar hlutverki staðfestingar á innskráningu. Með viðbótarstillingum getur síðan einnig innihaldið eyðublað sem safnar viðbótarupplýsingum frá viðskiptavinum til að auðvelda uppfyllingu pöntunar. Upplýsingar um hvernig á að setja upp síðuna og eininguna er að finna í [Innritunareiningin viðskiptavinar](check-in-pickup-module.md).

## <a name="configure-the-transactional-email-template"></a>Skilgreina sniðmát færslutölvupósta

Bæta þarf **Ég er mætt(ur)** tengli eða hnapp við sniðmátið fyrir færslutölvupósta sem viðskiptavinir fá þegar þeir mega sækja pantanirnar sínar. Viðskiptavinir munu nota þennan tengil eða hnapp til að tilkynna versluninni að þeir séu mættir til að sækja pöntunina. 

Bætið tenglinum eða hnappnum við sniðmátið sem er varpað í tilkynningargerðina **Pökkun lokið** og flutningsmátann sem er notaður fyrir uppfyllingu pöntunar fyrir utan verslun. Í sniðmátinu er búinn til HTML-tengill eða hnappur sem bendir á vefslóð staðfestingarsíðu innritunar sem var stofnuð. Eftirfarandi er dæmi.

```
<a href="https://[YOUR_SITE_DOMAIN]/[CHECK-IN_CONFIRMATION_PAGE]?channelReferenceId=%channelreferenceid%&channelId=%channelid%&packingSlipId=%packingslipid%" target="_blank">I am here!</a>
```
Nánari upplýsingar um hvernig á að stilla sniðmát fyrir tölvupósta eru í [Sérstilla tölvupósta vegna færslna eftir afhendingarmáta](customize-email-delivery-mode.md). 

## <a name="a-check-in-confirmation-task-is-created-in-pos"></a>Staðfestingarverkefni fyrir innritun er stofnað í sölustað

Þegar viðskiptavinur hefur tilkynnt versluninni að hann sé kominn til að sækja pöntun fær hann tilkynningu um staðfestingu innskráningar og verk er búið til í verklistanum á sölustað fyrir verslunina þar sem viðskiptavinurinn sækir pöntunina. Verkið inniheldur allar upplýsingar um viðskiptavin og pöntun sem þarf til að uppfylla pöntunina. Í verkinu sýnir leiðbeiningarreiturinn allar upplýsingar sem safnað var saman frá viðskiptavini í gegnum skjámynd viðbótarupplýsinga. 

## <a name="additional-resources"></a>Frekari upplýsingar

[Innskráning í afhendingareiningu](check-in-pickup-module.md)
