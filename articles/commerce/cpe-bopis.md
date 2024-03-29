---
title: Stilltu BOPIS í a Dynamics 365 Commerce sandkassa umhverfi
description: Þessi grein útskýrir hvernig á að stilla kaupa á netinu, sækja í verslun (BOPIS) í a Microsoft Dynamics 365 Commerce sandkassaumhverfi eftir að það hefur verið útvegað.
author: BrianShook
ms.date: 06/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-04-20
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 16cea7beb6ca05b5e96a9713b1217b414e27d56e
ms.sourcegitcommit: 252cb41c3029b623354698463f7b44a29fd9f184
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/15/2022
ms.locfileid: "9013176"
---
# <a name="configure-bopis-in-a-dynamics-365-commerce-sandbox-environment"></a>Stilltu BOPIS í a Dynamics 365 Commerce sandkassa umhverfi

[!include [banner](includes/banner.md)]

Þessi grein útskýrir hvernig á að stilla kaup á netinu, afhending í verslun (BOPIS) í a Microsoft Dynamics 365 Commerce sandkassaumhverfi eftir að umhverfið hefur verið útvegað.

## <a name="prerequisite"></a>Skilyrði

Ljúktu aðeins við aðferðirnar í þessari grein eftir að Commerce sandkassaumhverfið þitt hefur verið útvegað og stillt. Fyrir upplýsingar um hvernig á að útvega og stilla umhverfið þitt, sjá [Ákvæði a Dynamics 365 Commerce sandkassa umhverfi](provisioning-guide.md) og [Stilla a Dynamics 365 Commerce sandkassa umhverfi](./cpe-post-provisioning.md).

Eftir að viðskiptaumhverfið þitt hefur verið útbúið og stillt frá enda til enda geturðu notað þessa grein til að virkja BOPIS aðstæður.

## <a name="configure-the-pos"></a>Stilla sölustað

### <a name="configure-modern-pos"></a>Grunnstilla Modern sölustað

BOPIS atburðarásir sem fela í sér kreditkortagreiðslu krefjast vélbúnaðarstöðvar. Vélbúnaðarstöð innbyggð í Modern sölustað fyrir Windows og Android biðlara. Ef þú notar sölukerfi í skýinu eða Modern sölustað fyrir iOS, verður biðlari sölustaðarins (POS) að vera paraður við samnýtta vélbúnaðarstöð. Þessi grein útskýrir hvernig á að stilla BOPIS fyrir Windows og Android viðskiptavinum. Frekari upplýsingar um hvernig á að setja upp vélbúnaðarstöðvar, sjá [Grunnstilling og uppsetning á vélbúnaðarstöð fyrir Retail](./retail-hardware-station-configuration-installation.md).

1. Opnaðu **Smásala og viðskipti \> Uppsetning rásar \> Uppsetning sölustaðar \> Afgreiðslukassar**.
2. Veldu skráningu **SANFRAN-5** og veldu síðan **Breyta**.
3. Breyttu gildi reitsins **Forstilling vélbúnaðar** úr **HW002** í **HW001**, og smelltu síðan á **Vista**.
4. Til að samstilla breytingarnar, opnaðu **Smásala og viðskipti \> Upplýsingatækni smásölu og viðskipta \> Dreifingaráætlun**.
5. Veldu dreifingaráætlun **1090** og veldu síðan **Keyra núna** á aðgerðasvæðinu.
6. Veldu **Já** og síðan **Í lagi** til að hefja samstillingu gagna. 

### <a name="install-modern-pos"></a>Setja upp Modern POS

1. Opnaðu **Smásala og viðskipti \> Uppsetning rásar \> Uppsetning sölustaðar \> Tæki**.
2. Veljið tæki **SANFRANCIS-5**.
3. Veldu **Hlaða niður** á aðgerðarsvæðinu og veldu því næst **Skilgreiningarskrá**.
4. Veldu **Hlaða niður** og veldu því næst **Retail Modern POS**. 
5. Þegar niðurhal á **ModernPOSSetup.exe** skránni er lokið skaltu velja **Opna skrá**.

    ![Opin skrá.](./dev-itpro/media/PAYMENTS/openfile.png)

6. Veldu **Áfram** til að fara í gegnum uppsetningarferlið. Þegar uppsetningunni er lokið skaltu velja **Loka**.

### <a name="activate-modern-pos"></a>Virkja Modern POS

1. Smelltu á **Upphafshnappinn** og sláðu inn **Retail Modern POS**.
2. Veldu **Retail Modern POS** forritið til að ræsa virkjunina.
3. Veljið **Næst**. Reitirnir **Vefslóð þjóns**, **Auðkenni tækis** og **Skráningarnúmer** ættu að vera forstilltir með því að nota upplýsingar úr skilgreiningarskránni sem þú hlóðst niður í fyrri aðgerð.
4. Veldu **Virkja**.
5. Svargluggi sannvottunar opnast. Veldu reikninginn sem notar netfangið sem áður var tengt starfsmanni **000713 - Andrew Collette**.

    > [!NOTE]
    > Ef þú hefur ekki enn tengt starfsmann auðkennið þitt, þá mun virkjun ekki ná árangri. Í þessu tilviki skaltu fylgja skrefunum undir "Tengdu starfsmann við auðkenni þitt" í hlutanum [Stilla a Dynamics 365 Commerce sandkassa umhverfi](cpe-post-provisioning.md#associate-a-worker-with-your-identity) grein.
    
6. Þegar þú ert beðin/n um að láta fyrirtæki þitt stjórna tækinu skaltu velja **Aðeins þetta forrit**.
7. Þegar virkjun er lokið skaltu velja **Hefjast handa**.

### <a name="enable-bopis-in-modern-pos"></a>Virkja BOPIS í Modern sölustað

1. Skráðu þig inn á Modern sölustað með því að nota **000713** sem kenni stjórnanda og **123** sem aðgangsorð.
2. Þegar sýnikennslumyndbandið er spilað skaltu velja gátreitina tvo neðst í vinstra horninu í svarglugganum og loka síðan svarglugganum.
3. Ef þér er ekki beðið um að loka vaktinni, flettu til hægri á **Ávarpssíðunni** og smelltu á **Loka vakt**.
4. Þegar þú hefur skráð þig inn skaltu smella á **Framkvæma aðgerð utan skúffu** við kvaðningu.
5. Flettu til hægri á **Ávarpssíðunni** og smelltu á aðgerðina **Velja vélbúnaðarstöð**.
6. Smelltu á **Stjórna** og stilltu valkostinn **Nota vélbúnaðarstöð** á **Kveikt** og smelltu síðan á **Í lagi**.
7. Skrá út af Sölustað og síðan skrá aftur inn.
8. Eftir að þú hefur skráð þig inn skaltu velja **Opna nýja vakt** og velja síðan **Skúffu**.

## <a name="complete-a-bopis-scenario"></a>Ljúktu við BOPIS-atburðarás

### <a name="create-a-storefront-order-for-in-store-pickup"></a>Búðu til pöntun í netverslun til að sækja í verslun

1. Farðu á slóðina sem þú tilgreindir í skrefinu [Frumstilla rafræn viðskipti](./provisioning-guide.md#initialize-e-commerce) við grunnstillingu umhverfisins.
2. Veldu hlut og veldu **Setja í körfu**.
3. Veldu innkaupapokasíðuna og smelltu á **Sækja þetta** fyrir pöntunarlínuna sem þú varst að bæta við.
4. Í svargluggann **Velja verslun** slærðu inn **San Francisco** og smelltu síðan á **Leitarhnappinn**.
5. Finndu verslunina í San Francisco á niðurstöðulistanum og veldu **Sækja hér**.
6. Smelltu á **Skrá út sem gestur** á innkaupapokasíðunni. 

    > [!NOTE]
    > Til að halda áfram og ljúka kaupum verður þú að samþykkja yfirlýsinguna um kökur. Þessi tilkynning birtist sem borði efst á síðunni þar sem gengið er frá kaupum.

7. Færðu inn eftirfarandi upplýsingar fyrir greiðslumáta kreditkorta:

    - **Nafn korthafa:** Sláðu inn hvaða nafn sem er.
    - **Kortanúmer:** Sláðu inn **4111-1111-1111-1111**.
    - **Gildistími:** Sláðu inn **10/20**.
    - **CVV-númer:** Sláðu inn **737**.

    > [!IMPORTANT]
    > Ekki skal undir neinum kringumstæðum reyna að nota raunverulegar kreditkortaupplýsingar á prófunarsvæðinu.

8. Haltu áfram að ljúka kaupum með því að slá inn upplýsingar um heimilisfang greiðanda og smelltu síðan á **Vista og halda áfram**.
9. Smelltu á **Ljúka kaupum** þegar allt er til reiðu að leggja fram pöntunina.

### <a name="synchronize-online-orders-to-the-back-office"></a>Samstilltu pantanir á netinu við skrifstofuna

Frekari upplýsingar um hvernig á að samstilla pantanir á netinu er að finna í [Bókun á netsölu og -greiðslum](./tasks/posting-online-sales-payments.md).

### <a name="pick-up-an-order-in-the-store"></a>Sækja pöntun í verslunina

1. Skráðu þig inn POS
2. Á **Upphafsskjánum** smellirðu á **Uppfylling pöntunar**
3. Veldu línuna úr pöntuninni sem var gerð á netinu á listanum yfir vörurnar sem á að sækja.
4. Meðan pöntunarlínan er valin skaltu velja **Sækja**.

    Vörunni á línunni er bætt á færsluskjáinn og **$0,00** birtist sem upphæðin til greiðslu.

5. Veldu upphæðina til greiðslu **$0,00** eða veldu hvaða greiðslumáta sem er til að ljúka við færsluna.

## <a name="troubleshooting"></a>Úrræðaleit

### <a name="online-orders-that-are-retrieved-in-the-pos-have-a-non-zero-balance-due"></a>Netpantanir sem eru sóttar í sölustaðinn eru ekki með núlljafnaða upphæð til greiðslu

Þegar valið er að sækja vöru í verslun, ef upphæð til greiðslu er ekki 0 (núll), skal ganga úr skugga um að Modern sölustaður sé notaður og vélbúnaðarstöðin sé virk. Þegar sölukerfi í skýinu eða Modern sölustaður fyrir iOS er notað, skal ganga úr skugga um að samnýtta vélbúnaðarstöðin sé virk. Einhver tegund af virkri vélbúnaðarstöð er nauðsynleg til að sækja greiðslur sem gerðar voru á netinu.

### <a name="general-issues-with-payment-capture"></a>Almenn vandamál varðandi greiðslutöku

Hvað öll almenn vandamál varðar, ættir þú fyrst að skoða tilvikaannála Modern sölustaðarins eða upplýsingaþjónustunnar á netinu (IIS). Þú getur fundið þessar skrár undir eftirfarandi hnútum í tilvikaannál Windows:

- Application and Services Logs \> Microsoft \> Dynamics \> Commerce-Modern sölustaður
- Application and Services Logs \> Microsoft \> Dynamics \> Commerce-vélbúnaðarstöð

## <a name="additional-resources"></a>Frekari upplýsingar

[Ákvæði a Dynamics 365 Commerce sandkassa umhverfi](provisioning-guide.md)

[Stilltu valfrjálsa eiginleika fyrir a Dynamics 365 Commerce sandkassa umhverfi](cpe-optional-features.md)

[Microsoft Dynamics Lifecycle Services (LSC)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure-gátt](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce vefsvæði](https://aka.ms/Dynamics365CommerceWebsite)

[Adyen-greiðslutengill](./dev-itpro/adyen-connector.md?tabs=8-1-3)

[Vista netgreiðslumáta með Adyen-tengli](./dev-itpro/adyen-connector-listpi.md)

[Greiðsluyfirlit Omni-rásar](./omni-channel-payments.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
