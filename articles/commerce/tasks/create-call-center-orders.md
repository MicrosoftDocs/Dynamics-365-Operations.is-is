---
title: Stofna pantanir símavers
description: Í þessari grein er farið í gegnum dæmi um ferli þar sem notandi símaversins flettir upp viðskiptavin, býr til nýja pöntun, leitar að vöru og innheimtir greiðslu frá viðskiptavininum í Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 08/05/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: MCRCustomerService, SalesTable, MCRSourceIdTargetLookup, MCRSalesQuickQuote, MCRSalesOrderRecap, MCRCustPaymDialog, MCRCustPaymLookup
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 16d483896ce131e9a7bc60ab5ea7b8fa01a3bea8
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/06/2022
ms.locfileid: "9228511"
---
# <a name="create-call-center-orders"></a>Stofna pantanir símavers

[!include [banner](../includes/banner.md)]

Í þessari grein er farið í gegnum dæmi um ferli þar sem notandi símaversins flettir upp viðskiptavin, býr til nýja pöntun, leitar að vöru og innheimtir greiðslu frá viðskiptavininum í Microsoft Dynamics 365 Commerce. Aðferðin notar USRT kynningargagnafyrirtækið og er ætluð sölupöntunum. 

## <a name="prerequisites"></a>Forkröfur

Notandinn sem lýkur ferlinu verður að vera settur upp sem notandi símaver. Valfrjálst er hægt að gefa út Fabrikam hálfára vörulistann með að minnsta kosti einum frumkóða á honum.

### <a name="add-yourself-as-a-call-center-user"></a>Bættu þér við sem notanda símavera

Fylgdu þessum skrefum til að bæta þér við sem notanda símavera.

1. Í höfuðstöðvum viðskipta, farðu til **Verslun og verslun \> Rásir \> Símaver \> Allar símaver**.
1. Í **Notendur** reit, veldu **Rás notendur**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Í **notandanafn** reit, sláðu inn notandakennið þitt.
1. Í **Nafn** reit, sláðu inn notandanafnið þitt. Notandanafnið getur verið það sama og notendanafnið.
1. Í aðgerðarúðunni skal velja **Vista**.
1. Fara aftur til **Verslun og verslun \> Rásir \> Símaver \> Allar símaver**.
1. Veldu auðkenni smásölurásar símaversins.
1. Staðfestu að **Virkja pöntunarlok** valkostur er stilltur á **Já**. Ef valkosturinn er ekki sýnilegur geturðu sleppt þessu skrefi.

## <a name="complete-the-example-call-center-procedure"></a>Ljúktu við dæmið símaversferli

Fylgdu þessum skrefum til að klára dæmið um símaver.

1. Fárið í **Smásala og viðskipti \> Viðskiptavinir \> Þjónusta við viðskiptavini**.
1. Á **Viðskiptavinaleit** flipa, sláðu inn leitarskilyrði til að fletta upp viðskiptavininum. Fyrir þetta dæmi ferli, sláðu inn **Karen**.
1. Velja **Leita**. The **Viðskiptavinaleit** svarglugginn birtist og listar leitarniðurstöðurnar.
1. Veldu viðskiptamannaskrá fyrir **Karen Berg** sem hefur reikningsnúmer viðskiptavinar **2001**, og veldu síðan **Veldu**.
1. Á aðgerðarrúðunni velurðu **Ný sölupöntun**.
1. Til hægri velurðu **Fyrirsögn** flipa.
1. Á **Afhending** Flýtiflipi, í **Afhendingarmáti** reit, veldu **99 staðall**.

    ![Val á afhendingarmáta.](../media/Select_Mode_of_Delivery.png)

1. Til hægri velurðu **Línur** flipa.
1. Í **Sölupöntunarlínur** kafla, í nýju röðinni fyrir nýju sölulínuna, í **Vörunúmer** reit, sláðu inn vörunúmerið til að leita að. Fyrir þetta dæmi ferli, sláðu inn **81327**, og veldu síðan vöruna í fellilistanum til að bæta henni við sölupöntunina.
1. Í **Magn** reit skal slá inn sölumagn.
1. Í **Upprunakóði** reit, veldu frumkóðann fyrir vörulistann. Ef það eru engir virkir frumkóðar geturðu sleppt þessu skrefi.
1. Á aðgerðarrúðunni velurðu **Heill** til að ná greiðslu viðskiptavinarins. Þessi aðgerð opnar **Sölupöntun yfirlit** svargluggi, sem sýnir heildarupphæðina sem er á gjalddaga. Aðgerðin kveikir einnig á útreikningi á gjöldum, svo sem sendingu og meðhöndlun, og sýnir þau í **Sölupöntun yfirlit** valmynd.

    ![Heill hnappur.](../media/Complete_button.png)

1. Í **Sölupöntun yfirlit** valmynd, á **Greiðslur** Flýtiflipi, veldu **Bæta við** að ná greiðslunum.

    ![Samantektargluggi sölupöntunar.](../media/order_summary.png)

1. Í **Sláðu inn greiðsluupplýsingar viðskiptavina** valmynd, í **Greiðslumáti** reit, veldu greiðslumáta. Fyrir þetta dæmi ferli, veldu **Reiðufé**.
1. Í **Greiðslu upphæð** reit, sláðu inn greiðsluupphæðina. Fyrir þetta dæmi, sláðu inn **120.00**, sem jafngildir pöntunarjöfnuðinum sem er sýndur í **Sölupöntun yfirlit** valmynd. Með því að slá inn þessa upphæð geturðu klárað pöntunina sem fullgreidda.
1. Veldu **Í lagi**.
1. Veldu **Senda**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Sérstilla tölvupósta vegna færslna eftir afhendingarmáta](../customize-email-delivery-mode.md)

[Breyta afhendingarmáta á sölustað](../pos-change-delivery-mode.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
