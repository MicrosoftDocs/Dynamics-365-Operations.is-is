---
title: Stilltu CPOS til að nota sérsniðið Azure AD app
description: Þessi grein útskýrir hvernig á að stilla Cloud POS (CPOS) til að nota sérsniðið Azure Active Directory (Azure AD) app.
author: boycez
ms.date: 08/02/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: baa0c3da25308345037b5dd1b4c5907d6213e7f7
ms.sourcegitcommit: bd3b55e1af28e592c97b540de1e87cd8ba9c35a8
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/03/2022
ms.locfileid: "9223820"
---
# <a name="configure-cpos-to-use-a-custom-azure-ad-app"></a>Stilltu CPOS til að nota sérsniðið Azure AD app

[!include [banner](includes/banner.md)]

Sjálfgefið er Cloud POS (CPOS) í Microsoft Dynamics 365 Commerce bendir á skráð fyrsta aðila Microsoft app í Azure Active Directory (Azure AD). Þess vegna er hægt að nota CPOS án þess að þurfa að gera breytingar á Azure AD. Hins vegar gætirðu viljað benda tilvikinu þínu af CPOS á sérsniðið Azure AD app sem þú stjórnar. Þessi grein útskýrir hvernig á að stilla CPOS til að nota sérsniðið Azure AD app.

## <a name="set-up-a-custom-retail-server-app-in-azure-ad"></a>Settu upp sérsniðið Retail Server app í Azure AD

Til að búa til og stilla sérsniðið Retail Server app í Azure AD, fylgdu þessum skrefum.

1. Skráðu þig inn á [Azure Active Directory stjórnendamiðstöð](https://aad.portal.azure.com) með því að nota hvaða Azure AD notandareikningur. Notendareikningurinn þarf ekki að hafa stjórnandaheimildir.
1. Velja skal **Azure Active Directory**.
1. Veldu **App skráningar**, og veldu síðan **Ný skráning** að opna **Skráðu umsókn** valmynd.
1. Stilltu eftirfarandi svæði:

    - **Nafn** - Sláðu inn sérsniðið nafn fyrir appið. Til dæmis, slá inn **Sérsniðinn smásöluþjónn**.
    - **Styðja tegundir reikninga** - Veldu sjálfgefna valmöguleikann, **Reikningar í þessari skipulagsskrá eingöngu (aðeins Microsoft - einn leigjandi)**.
    - **Beina URI** – Þessi reitur er valfrjáls. Skildu það eftir autt.
    - **Þjónustutré auðkenni** – Þessi reitur er valfrjáls. Skildu það eftir autt.
    
1. Veldu **Skrá**. Stillingarsíðan fyrir nýskráða appið birtist.
1. Í **Yfirlit \> Nauðsynjar** kafla, veldu **Bættu við URI forritauðkenni**, og veldu síðan **Sett** við hliðina á **Umsóknarauðkenni URI**. Skrifaðu niður fyrirhugað gildi og veldu síðan **Vista** að samþykkja það gildi. 
1. Veldu **Bættu við umfangi**, og stilltu síðan eftirfarandi reiti:

    - **Gildisheiti** – Sláðu inn sérsniðið heiti fyrir umfangið. Til dæmis, slá inn **Legacy.Access.Full**.
    - **Hver getur samþykkt** – Tilgreindu hvort bæði stjórnendur og notendur eða aðeins stjórnendur geta gefið samþykki, byggt á öryggisstefnu fyrirtækisins.
    - **Sýningarheiti stjórnandasamþykkis** – Sláðu inn skjáheiti. Til dæmis, slá inn **Aðgangur að smásöluþjóni**.
    - **Lýsing á samþykki stjórnanda** – Sláðu inn lýsingu. Til dæmis, slá inn **Veitir aðgang að Retail Server API**.

1. Veldu **Bæta við umfangi** til að ljúka ferlinu við að búa til umfang.

## <a name="set-up-a-custom-cpos-app-in-azure-ad"></a>Settu upp sérsniðið CPOS app í Azure AD

Til að búa til og stilla sérsniðið CPOS app í Azure AD, fylgdu þessum skrefum.

1. Skráðu þig inn á [Azure Active Directory stjórnendamiðstöð](https://aad.portal.azure.com) með því að nota hvaða Azure AD notandareikningur. Notendareikningurinn þarf ekki að hafa stjórnandaheimildir.
1. Velja skal **Azure Active Directory**.
1. Veldu **App skráningar**, og veldu síðan **Ný skráning** að opna **Skráðu umsókn** valmynd.
1. Stilltu eftirfarandi svæði:

    - **Nafn** - Sláðu inn nafn fyrir appið. Til dæmis, slá inn **Sérsniðin Cloud POS**.
    - **Styðja tegundir reikninga** - Veldu sjálfgefna valmöguleikann, **Reikningar í þessari skipulagsskrá eingöngu (aðeins Microsoft - einn leigjandi)**.
    - **Beina URI** – Veldu **Einsíðu umsókn (SPA)** í fellilistanum og sláðu síðan inn CPOS URI.
    - **Þjónustutré auðkenni** – Þessi reitur er valfrjáls. Skildu það eftir autt.

1. Veldu **Skrá**. Stillingarsíðan fyrir nýskráða appið birtist.
1. Í **Auglýst** kafla, stilltu **oauth2AllowIdTokenImplicitFlow** og **oauth2AllowImplicitFlow** breytur til **satt**, og veldu síðan **Vista**.
1. Í **Stilling tákns** kafla, fylgdu þessum skrefum til að bæta við tveimur kröfum:

    - Veldu **Bæta við valkvæðri kröfu**. Stilltu **Tegund tákns** sviði til **auðkenni**, og veldu síðan **sid** krafa. Veljið **Bæta við**.
    - Veldu **Bæta við valkvæðri kröfu**. Stilltu **Tegund tákns** sviði til **Aðgangur**, og veldu síðan **sid** krafa. Veljið **Bæta við**.

1. Í **API heimildir** kafla, veldu **Bættu við heimild**.
1. Á **API sem stofnunin mín notar** flipanum, leitaðu að Retail Server appinu sem þú bjóst til í [Settu upp sérsniðið Retail Server app í Azure AD](#set-up-a-custom-retail-server-app-in-azure-ad) kafla. Veldu síðan **Bæta við heimildum**.
1. Í **Yfirlit** kafla, skráið ykkur gildið í **Auðkenni umsóknar (viðskiptavinar).** sviði.

## <a name="update-the-cpos-configuration-file"></a>Uppfærðu CPOS stillingarskrána

Opnaðu CPOS config.json skrána og gerðu eftirfarandi uppfærslur í henni.

1. Skiptu um **AADClientId** lykilgildi með **Auðkenni umsóknar (viðskiptavinar).** gildi sérsniðna CPOS forritsins sem þú bjóst til í [Settu upp sérsniðið CPOS app í Azure AD](#set-up-a-custom-cpos-app-in-azure-ad) kafla.
1. Skiptu um **AADRetailServerResourceId** lykilgildi með **Umsóknarauðkenni URI** gildi sérsniðna Retail Server appsins sem þú bjóst til í [Settu upp sérsniðið Retail Server app í Azure AD](#set-up-a-custom-retail-server-app-in-azure-ad) kafla.

CPOS mun nota báðar færibreyturnar þegar það sendir beiðnir til Azure AD að eignast öryggismerki.

## <a name="update-identity-providers-settings-in-commerce-headquarters"></a>Uppfærðu stillingar auðkennisveitu í höfuðstöðvum Commerce

Næst verður þú að uppfæra stillingar auðkennisveitna í höfuðstöðvum Commerce.

1. Í höfuðstöðvum viðskipta, opnaðu **Viðskipti samnýtt færibreytur** síðu.
1. Á **Auðkennisveitendur** flipa, í **Auðkennisveitendur** kafla, veldu línuna þar sem **Tegund** reiturinn er stilltur á **Azure Active Directory** og **Útgefandi** reiturinn bendir á þinn Azure AD leigjanda. Þessi stilling lýsir því yfir að þú munt vinna með barnanet sem innihalda gögnin sem tengjast auðkennisveitunni sem samsvarar Azure AD leigjanda.
1. Í **Traust aðilar** kafla, veldu **Bæta við** til að bæta við röð.
1. Stilltu eftirfarandi svæði:

    - **ClientId** – Sláðu inn **Auðkenni umsóknar (viðskiptavinar).** gildi sérsniðna CPOS forritsins sem þú bjóst til í [Settu upp sérsniðið CPOS app í Azure AD](#set-up-a-custom-cpos-app-in-azure-ad) kafla.
    - **Tegund** – Veldu **Opinber**.
    - **UserType** – Veldu **Vinnumaður**.

1. Veldu línuna sem þú bættir við. The **Auðkenni miðlaraauðlinda** kafla fyrir neðan **Traust aðilar** kafla sýnir smásölumiðlara appauðkennin sem hægt er að nálgast með appinu sem þú valdir í **Traust aðilar** rist.
1. Í **Auðkenni miðlaraauðlinda** kafla, veldu **Bæta við** til að bæta við röð.
1. Í **Auðkenni miðlaraauðlindar** reit, sláðu inn **Umsóknarauðkenni URI** gildi sérsniðna Retail Server appsins sem þú bjóst til í [Settu upp sérsniðið Retail Server app í Azure AD](#set-up-a-custom-retail-server-app-in-azure-ad) kafla.

    > [!IMPORTANT]
    > Allir reitirnir sem nefndir eru í skrefunum á undan eru hástafaviðkvæmir. Gildin sem þú slærð inn verða að passa nákvæmlega við gildin sem eru stillt í Azure AD stjórnendamiðstöð.

1. Fara til **Upplýsingatækni í smásölu og viðskiptum \> Dreifingaráætlun**, og keyra **1110** (**Alþjóðleg uppsetning**) starf.

Þú getur nú virkjað CPOS tæki með því að nota þín eigin Azure AD app.

## <a name="additional-resources"></a>Frekari upplýsingar

[Virkjun á sölustað (POS) tæki](dev-itpro/retail-device-activation.md)

[Stjórna virknilyklum og villuleita tæki](set-up-activation-accounts-validate-devices-hq.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
