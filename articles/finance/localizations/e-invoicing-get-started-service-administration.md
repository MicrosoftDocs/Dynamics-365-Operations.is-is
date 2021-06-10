---
title: Hafist handa með þjónustu rafrænna reikninga fyrir Brasilíu
description: Þetta efnisatriði útskýrir hvernig á að hefjast handa með rafrænni reikningsfærslu.
author: gionoder
ms.date: 05/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 7c4d69edd4a8f7c7acc2ac1bc22c1ba6eaba25ae
ms.sourcegitcommit: 90a289962598394ad98209026013689322854b7b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/24/2021
ms.locfileid: "6092407"
---
# <a name="get-started-with-electronic-invoicing-service-administration"></a>Hafist handa með þjónustu rafrænna reikninga fyrir Brasilíu

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a>Forkröfur

Áður en ferlið í þessu efnisatriði er klárað þurfa eftirfarandi skilyrði að vera til staðar:

- Þú verður að hafa aðgang að reikningi á Microsoft Dynamics Lifecycle Services (LCS).
- Þú verður að vera með LCS-verk sem inniheldur útgáfu 10.0.17 eða nýrri af Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management. Þar að auki verða þessi forrit að vera sett upp á einni af eftirfarandi Azure-staðsetningum:

    - Bandaríkin
    - Evrópa
    - Bretland
    - Asía

- Þú verður að hafa aðgang að reikningnum þínum hjá Dynamics 365 Regulatory Configuration Services (LCS).
- Þú verður að virkja altækan eiginleika fyrir RCS-reikninginn þinn í eiginleikastjórnun. Frekari upplýsingar er að finna í [Regulatory Configuration Services (RCS) – Altækir eiginleikar](rcs-globalization-feature.md).
- Stofna verður lyklageymslu og geymslureikning í Azure. Frekari upplýsingar er að finna í [Stofna Azure-geymslureikning og lyklageymslu](e-invoicing-create-azure-storage-account-key-vault.md).

## <a name="install-the-add-in-for-microservices-in-lifecycle-services"></a>Setja upp innbótina fyrir microservices í Lifecycle Services

1. Skráðu þig inn á LCS-reikninginn þinn og veldu LCS-verkefni á stjórnborði LCS-verkefnisins.
2. Í verkefninu, á stjórnborði umhverfisins, skaltu velja uppsetningarverkefni LCS. Verkefnið sem þú velur verður að vera í gangi.
3. Í flipanum **Power Platform Samþætting** í **Innbætur umhverfis** skal velja **Setja upp nýja innbót**.
4. Velja **Rafræn reikningsfærsla**.
5. Í reitinn **AAD-forritskenni** skal færa inn **091c98b0-a1c9-4b02-b62c-7753395ccabe**. Þetta er fast gildi.
6. Í reitinn **AAD-leigjandakenni** skal færa inn leigjandakenni Azure-áskriftareiknings.
7. Farið yfir skilmálana og veljið því næst gátreitinn.
8. Velja **Setja upp**.


## <a name="set-up-the-parameters-for-rcs-integration-with-electronic-invoicing"></a>Setja upp færibreytur fyrir RCS-samþættingu við rafræna reikningsfærslu

1. Skráðu þig inn á RCS-reikninginn þinn.
2. Í vinnusvæðinu **Rafræn skýrslugerð** í kaflanum **Skyldir tenglar**, velurðu **Færibreytur rafrænnar skýrslugerðar**.
3. Í flipanum **Þjónusta rafrænnar reikningsfærslu**, í reitinn **URI fyrir endastöð þjónustu** skal slá inn viðeigandi endastöð þjónustu fyrir Azure-staðfestninguna þína eins og sýnt er í eftirfarandi töflu.

    | Gagnamiðstöð Azure-staðsetningar | URI fyrir endastöð þjónustu                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | Bandaríkin              | <p>`https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Evrópa                     | <p>`https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Bretland             | <p>`https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Asía                       | <p>`https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |

4. Gangið úr skugga um að reiturinn **Forritsauðkenni** sé stilltur á **0cdb527f-a8d1-4bf8-9436-b352c68682b2**. Gildið er fast.
5. Í reitinn **LCS-umhverfiskenni** skal færa inn auðkenni LCS-umhverfis.
6. Veljið **Vista** og lokið síðan skjámyndinni.

## <a name="create-key-vault-references"></a>Stofna tilvísanir lyklageymslu

1. Skráðu þig inn á RCS-reikninginn þinn.
2. Á vinnusvæðinu **Altækur eiginleiki**, í hlutanum **Umhverfi**, skal velja reitinn **Rafræn reikningsfærsla**.
3. Á síðunni **Uppsetningar umhverfis**, á aðgerðasvæðinu, skal velja **Þjónustuumhverfi** og síðan velja **Færibreytur lyklageymslu**.
4. Veljið **Nýr** til að stofna tilvísun lyklageymslu.
5. Í reitinn **Heiti** skal slá inn heiti á tilvísun lyklageymslu. Í reitnum **Lýsing** skal færa inn lýsingu.
6. Í reitinn **URI lyklageymslu** skal líma leyniorð leynilykilinn úr Azure-lyklageymslu. Frekari upplýsingar er að finna í [Stofna Azure-geymslureikning og lyklageymslu](e-invoicing-create-azure-storage-account-key-vault.md).
7. Veljið **Vista**.

## <a name="create-storage-account-secret"></a>Stofna leynilykil geymslureiknings

1. Á síðunni **Uppsetningar umhverfis**, á aðgerðasvæðinu, skal velja **Þjónustuumhverfi** > **Færibreytur lyklageymslu**.
2. Veljið **Tilvísun lyklageymslu** og í **Vottorð** hlutanum skal velja **Bæta við**.
3. Í reitinn **Heiti** skal færa inn heiti fyrir leynilykil geymslureiknings. Frekari upplýsingar er að finna í [Stofna Azure-geymslureikning og lyklageymslu](e-invoicing-create-azure-storage-account-key-vault.md).
4. Í reitnum **Lýsing** skal færa inn lýsingu.
5. Í reitnum **Gerð** skal velja **Leynilykill**.
6. Veljið **Vista** og lokið síðan skjámyndinni.

## <a name="create-a-digital-certificate-secret"></a>Búa til leynilykil stafræns vottorðs

1. Á síðunni **Uppsetningar umhverfis**, á aðgerðasvæðinu, skal velja **Þjónustuumhverfi** og síðan velja **Færibreytur lyklageymslu**.
2. Veljið **Tilvísun lyklageymslu** og svo í **Vottorð** hlutanum skal velja **Bæta við**.
3. Heiti leynilykils stafræna skírteinisins er sleginn í reitinn **Nafn**. Frekari upplýsingar er að finna í [Stofna Azure-geymslureikning og lyklageymslu](e-invoicing-create-azure-storage-account-key-vault.md).
4. Í reitnum **Lýsing** skal færa inn lýsingu.
5. Í reitnum **Gerð** skal velja **Vottorð**.
6. Veljið **Vista** og lokið síðan skjámyndinni.

## <a name="create-a-service-environment"></a>Stofna þjónustuumhverfi

1. Skráðu þig inn á RCS-reikninginn þinn.
2. Á vinnusvæðinu **Altækur eiginleiki**, í hlutanum **Umhverfi**, skal velja reitinn **Rafræn reikningsfærsla**.
3. Á síðunni **Uppsetningar umhverfis**, á aðgerðasvæðinu, skal velja **Þjónustuumhverfi**.
4. Velja skal **Nýtt** til að stofna nýtt þjónustuumhverfi.
5. Í reitinn **Heiti** skal slá inn heiti á umhverfi rafrænnar reikningsfærslu. Í reitnum **Lýsing** skal færa inn lýsingu.
6. Í reitnum **SAS-leynilykill geymslu** skal velja heiti leynilykils geymslureikningsins sem þarf að nota til að auðkenna aðgang að geymslureikningnum.
7. Í hlutanum **Notendur** skal velja **Bæta við** til að bæta við notanda sem hefur heimild til að senda inn rafræna reikninga í gegnum umhverfið og einnig tengjast við geymslureikninginn.
8. Í reitinn **Notandakenni** skal færa inn samnefni notandans. Í reitinn **Tölvupóstur** skal færa inn netfang notandans.
9. Veljið **Vista**.
10. Ef reikningar fyrir tiltekið land/svæði þurfa vottorðakeðju til að nota stafræna undirskrift, þá skal á aðgerðasvæðinu velja **Færibreytur lyklageymslu** og síðan velja **Vottorðakeðja** og fara í gegnum þessi skref:
    1. Veljið **Ný** til að búa til nýja vottorðakeðju.
    2. Í reitinn **Heiti** skal færa inn heiti vottorðakeðjunnar. Í reitnum **Lýsing** skal færa inn lýsingu.
    3. Í hlutanum **Vottorð** skal velja **Bæta við** til að bæta vottorði við keðjuna.
    4. Notið hnappinn **Upp** eða **Niður** til að breyta stöðu vottorðs í keðjunni.
    5. Veljið **Vista** og lokið síðan skjámyndinni.
    6. Lokið síðunni.
11. Á síðunni **Þjónustuumhverfi**, á aðgerðasvæðinu, skal velja **Birta** til að birta umhverfið í skýinu. Gildi reitsins **Staða** er breytt í **Birt**.

## <a name="create-a-connected-application"></a>Búa til tengt forrit

1. Á síðunni **Uppsetningar umhverfis**, á aðgerðasvæðinu, skal velja **Tengd forrit**.
2. Veljið **Nýtt** til að stofna tengt forrit.
3. Í reitinn **Heiti** skal færa inn heiti forritsins sem á að tengja.
4. Í reitinn **Forrit** skal færa inn vefslóð fyrir umhverfi Finance and Supply Chain Management sem tengjast á við.
4. Í reitinn **Leigjandi** skal færa inn leigjanda umhverfis Finance and Supply Chain Management.
5. Veljið **Vista**.
6. Á aðgerðasvæðinu skal velja **Athuga tengingu** til að prófa tenginguna við umhverfið. Lokið því næst síðunni.

## <a name="link-connected-applications-to-environments"></a>Tengja tengd forrit við umhverfi

1. Á síðunni **Uppsetningar umhverfis** skal velja **Nýtt** til að úthluta tengdu forriti á umhverfi.
2. Í reitnum **Tengt forrit** skal velja tengt forrit.
3. Í reitnum **Þjónustuumhverfi** skal velja þjónustuumhverfi.
4. Veljið **Vista** og lokið síðan skjámyndinni.

## <a name="set-up-electronic-invoicing-integration-in-finance-and-supply-chain-management"></a>Setja upp samþættingu á rafrænni reikningsfærslu í Finance and Supply Chain Management

### <a name="turn-on-the-electronic-invoicing-integration-feature"></a>Kveikið á eiginleika fyrir samþættingu rafrænnar reikningsfærslu

1. Skráðu þig inn í tilvikið þitt af Finance eða Supply Chain Management.
2. Á vinnusvæðinu **Eiginleikastjórnun** skal leita að eiginleikanum **Samþætting rafrænnar reikningsfærslu**. Ef þessi eiginleiki birtist ekki á síðunni skal velja **Athuga með uppfærslur**.
3. Veljið eiginleikann og veljið svo **Virkja núna**.

### <a name="set-up-the-service-endpoint-url"></a>Setja upp vefslóð fyrir endastöð þjónustu

1. Farið í **Fyrirtækisstjórnun \> Uppsetning \> Færibreytur rafrænna skjala**.
2. Í flipanum **Innsendingarþjónusta**, í reitinn **Vefslóð fyrir endastöð þjónustu** skal slá inn viðeigandi endastöð þjónustu fyrir Azure-staðfestinguna þína eins og sýnt er í eftirfarandi töflu.

    | Gagnamiðstöð Azure-staðsetningar | URI fyrir endastöð þjónustu                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | Bandaríkin              | <p>`https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Evrópa                     | <p>`https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Bretland             | <p>`https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Asía                       | <p>`https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |

3. Í reitinn **Umhverfi** skal færa inn heiti á þjónustuumhverfi sem er birt í rafrænni reikningsfærslu.
4. Veljið **Vista** og lokið síðan skjámyndinni.

### <a name="enable-flighting-keys"></a>Virkja fluglykla

Virkjaðu fluglykla fyrir Microsoft Dynamics 365 Finance eða Microsoft Dynamics 365 Supply Chain Management útgáfu 10.0.17 eða eldri. 
1. Framkvæmið eftirfarandi SQL-skipun:

    SETJA INN Í SYSFLIGHTING (ÚTGÁFUHEITI, VIRKJAÐ) GILDI ('BusinessDocumentSubmissionServiceEnabled', 1)
    
    SETJA INN Í SYSFLIGHTING (ÚTGÁFUHEITI, VIRKJAÐ) GILDI ('ElectronicInvoicingServiceIntegrationFeature', 1)

2. Framkvæma IISreset-skipun fyrir öll AOS.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
