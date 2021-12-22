---
title: Virkja innskráningartilkynningar viðskiptavinar á sölustað (POS)
description: Í þessu efnisatriði er lýst hvernig á að virkja tilkynningar um innskráningu viðskiptavina á Microsoft Dynamics 365 Commerce sölustað.
author: bicyclingfool
ms.date: 12/03/2021
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
ms.openlocfilehash: 320e9d73ca98bf4ed22ac9bdff2fc34ae83223ec
ms.sourcegitcommit: 5f5a8b1790076904f5fda567925089472868cc5a
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 12/03/2021
ms.locfileid: "7891413"
---
# <a name="enable-customer-check-in-notifications-in-point-of-sale-pos"></a>Virkja innskráningartilkynningar viðskiptavinar á sölustað (POS)

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

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

Bætið tenglinum eða hnappnum við sniðmátið sem er varpað í tilkynningargerðina **Pökkun lokið** og flutningsmátann sem er notaður fyrir uppfyllingu pöntunar fyrir utan verslun. Í sniðmátinu, búðu til HTML tengil eða hnapp sem vísar á vefslóð innritunar staðfestingarsíðunnar sem þú bjóst til, og sem inniheldur færibreytanöfn og gildi, eins og sýnt er í eftirfarandi dæmi.

`<a href="https://[YOUR_SITE_DOMAIN]/[CHECK-IN_CONFIRMATION_PAGE]?channelReferenceId=%confirmationid%&channelId=%channelid%&packingSlipId=%packingslipid%" target="_blank">I am here!</a>`

Nánari upplýsingar um hvernig á að stilla sniðmát fyrir tölvupósta eru í [Sérstilla tölvupósta vegna færslna eftir afhendingarmáta](customize-email-delivery-mode.md). 

## <a name="a-check-in-confirmation-task-is-created-in-pos"></a>Staðfestingarverkefni fyrir innritun er stofnað í sölustað

Eftir að viðskiptavinur hefur tilkynnt versluninni að hann sé til staðar fyrir afhendingu sýnir innritunarsíðan staðfestingarskilaboð og valfrjálsan QR kóða sem inniheldur pöntunarstaðfestingarauðkenni viðskiptavinarins. Jafnframt er búið til verk í verkefnalistanum í POS fyrir verslunina þar sem viðskiptavinurinn er að sækja pöntunina. Það verkefni inniheldur allar upplýsingar um viðskiptavini og pöntun sem þarf til að uppfylla pöntunina. Leiðbeiningarreitur verksins sýnir allar upplýsingar sem safnað var frá viðskiptavininum í gegnum viðbótarupplýsingaeyðublaðið.

## <a name="end-to-end-testing"></a>Próf frá enda til enda

Innritun viðskiptavina krefst þess að tilteknar breytur og gildi séu send á innritunarsíðuna og síðan á innritunarforrit viðskiptavinarins. Þess vegna er auðveldasta aðferðin að prófa eiginleikann í umhverfi þar sem hægt er að búa til og pakka prófunarpöntun. Þannig er hægt að búa til tölvupóst „pöntun tilbúin til afhendingar“ sem hefur vefslóð sem inniheldur nauðsynleg færibreytanöfn og gildi.

Fylgdu þessum skrefum til að prófa innritunareiginleika viðskiptavina.

1. Búðu til innritunarsíðu viðskiptavinar og bættu síðan við og stilltu innritunareiningu viðskiptavinar. Fyrir frekari upplýsingar, sjá [Innritun fyrir afhendingareiningu](check-in-pickup-module.md). 
1. Kíktu á síðuna en ekki birta hana.
1. Bættu eftirfarandi tengli við sniðmát tölvupósts sem er kallað fram af tilkynningunni um heildarpökkun fyrir afhendingarmáta. Fyrir frekari upplýsingar, sjá [Búðu til tölvupóstsniðmát fyrir viðskiptaviðburði](email-templates-transactions.md).

    - **Fyrir forframleiðslu (UAT) umhverfi:** Bættu við kóðabútinum frá [Stilltu viðskiptapóstsniðmátið](#configure-the-transactional-email-template) kafla fyrr í þessu efni.
    - **Fyrir framleiðsluumhverfi:** Bættu við eftirfarandi kóða með athugasemdum svo að núverandi viðskiptavinir verði ekki fyrir áhrifum.

        `<!-- https://[DOMAIN]/[CHECK_IN_PAGE]?channelReferenceId=%confirmationid%&channelId=%pickupchannelid%&packingSlipId=%packingslipid%&preview=inprogress -->`

1. Búðu til pöntun þar sem afhendingarmáti er tilgreindur.
1. Þegar þú færð tölvupóstinn sem er ræstur af tilkynningunni um að fullu pakkningunni er lokið skaltu prófa innritunarflæðið með því að opna innritunarsíðuna sem hefur vefslóðina sem þú bættir við áðan. Vegna þess að vefslóðin inniheldur`&preview=inprogress` flagga, þú verður beðinn um að auðkenna áður en þú getur skoðað síðuna.
1. Sláðu inn allar viðbótarupplýsingar sem þarf til að stilla eininguna.
1. Gakktu úr skugga um að staðfestingarsýn innritunar sé rétt sýnd.
1. Opnaðu POS útstöð fyrir verslunina þar sem pöntunin verður sótt.
1. Veldu **Pantanir til að sækja** flísar og staðfestu að röðin birtist.
1. Staðfestu að allar viðbótarupplýsingar sem voru stilltar í innritunareiningunni birtist í upplýsingarúðunni.

Eftir að þú hefur staðfest að innritunareiginleikinn viðskiptavina virki frá enda til enda skaltu fylgja þessum skrefum.

1. Birtu innritunarsíðuna.
1. Ef þú ert að prófa í framleiðsluumhverfi skaltu afskrifa slóðina í tölvupóstsniðmátinu „pöntun tilbúin til afhendingar“, svo að **ég er hér** hlekkur eða hnappur birtist. Hladdu síðan upp sniðmátinu aftur.

## <a name="additional-resources"></a>Frekari upplýsingar

[Innskráning í afhendingareiningu](check-in-pickup-module.md)

[Sérstilla tölvupósta vegna færslna eftir afhendingarmáta](customize-email-delivery-mode.md)

[Stofna sniðmát fyrir tölvupóst fyrir færslutilvik](email-templates-transactions.md)
