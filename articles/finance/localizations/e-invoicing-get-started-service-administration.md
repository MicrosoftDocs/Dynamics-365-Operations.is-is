---
title: Hafist handa með þjónustuveitu viðbótar rafrænnar reikningsfærslu
description: Þetta efnisatriði útskýrir hvernig á að hefjast handa með viðbót rafrænnar reikningsfærslu.
author: gionoder
manager: AnnBe
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 05b00380cec7511adad2467d3f252799a4aaee5c
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592527"
---
# <a name="get-started-with-electronic-invoicing-add-on-service-administration"></a>Hafist handa með þjónustuveitu viðbótar rafrænnar reikningsfærslu

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

## <a name="prerequisites"></a>Forkröfur

Áður en ferlið í þessu efnisatriði er klárað þurfa eftirfarandi skilyrði að vera til staðar:

- Þú verður að hafa aðgang að reikningi á Microsoft Dynamics Lifecycle Services (LCS).
- Þú verður að vera með LCS-verk sem inniheldur útgáfu 10.0.17 eða nýrri af Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management. Þar að auki verða þessi forrit að vera sett upp á einni af eftirfarandi Azure-staðsetningum:

    - Austurhluti Bandaríkjanna
    - Vesturhluti Bandaríkjanna
    - Norðurhluti Evrópusambandsins
    - Vesturhluti Evrópusambandsins

- Þú verður að hafa aðgang að reikningnum þínum hjá Dynamics 365 Regulatory Configuration Services (LCS).
- Þú verður að virkja altækan eiginleika fyrir RCS-reikninginn þinn í eiginleikastjórnun. Frekari upplýsingar er að finna í [Regulatory Configuration Services (RCS) – Altækir eiginleikar](rcs-globalization-feature.md).
- Stofna verður lyklageymslu og geymslureikning í Azure. Frekari upplýsingar er að finna í [Stofna Azure-geymslureikning og lyklageymslu](e-invoicing-create-azure-storage-account-key-vault.md).

## <a name="install-the-add-on-for-microservices-in-lifecycle-services"></a>Setja upp viðbótina fyrir microservices í Lifecycle Services

1. Skráðu þig inn á LCS-reikninginn þinn.
2. Veldu reitinn **Stjórnun forskoðunareiginleika**.
3. Í hlutanum **Opnir forskoðunareiginleikar** skal velja **Þjónusta rafrænnar reikningsfærslu**.
4. Gangið úr skugga um að valkosturinn **Virkja forskoðunareiginleika** sé stilltur á **Já**.
5. Á LCS-stjórnborðinu skal velja LCS-uppsetningarverkið. LCS-verkið verður að vera í gangi.
7. Í flipanum **Innbætur umhverfis** skal velja **Setja upp nýja innbót**.
8. Veljið **Rafrænar reikningsfærsluþjónustur** og í reitinn **AAD-forritskenni** skal færa inn **091c98b0-a1c9-4b02-b62c-7753395ccabe**. Þetta er fast gildi.
10. Í reitinn **AAD-leigjandakenni** skal færa inn leigjandakenni Azure-áskriftareiknings.
11. Farið yfir skilmálana og veljið því næst gátreitinn.
12. Velja **Setja upp**.


## <a name="set-up-the-parameters-for-rcs-integration-with-the-electronic-invoicing-add-on"></a>Setja upp færibreytur fyrir RCS-samþættingu við viðbót rafrænnar reikningsfærslu

1. Skráðu þig inn á RCS-reikninginn þinn.
2. Í vinnusvæðinu **Rafræn skýrslugerð** í kaflanum **Skyldir tenglar**, velurðu **Færibreytur rafrænnar skýrslugerðar**.
3. Í flipanum **Þjónusta rafrænnar reikningsfærslu**, í reitinn **URI fyrir endastöð þjónustu** skal slá inn viðeigandi endastöð þjónustu fyrir Azure-staðfestninguna þína eins og sýnt er í eftirfarandi töflu.

    | Gagnamiðstöð Azure-staðsetningar | URI fyrir endastöð þjónustu                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | Austurhluti Bandaríkjanna                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | Vesturhluti Bandaríkjanna                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | Norðurhluti Evrópusambandsins                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | Vesturhluti Evrópusambandsins                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

4. Gangið úr skugga um að reiturinn **Forritsauðkenni** sé stilltur á **0cdb527f-a8d1-4bf8-9436-b352c68682b2**. Gildið er fast.
5. Í reitinn **LCS-umhverfiskenni** skal færa inn auðkenni LCS-áskriftarreiknings.
6. Veljið **Vista** og lokið síðan skjámyndinni.

## <a name="create-key-vault-secret"></a>Stofna leynilykil lyklageymslu

1. Skráðu þig inn á RCS-reikninginn þinn.
2. Á vinnusvæðinu **Altækur eiginleiki**, í hlutanum **Umhverfi**, skal velja reitinn **Viðbót rafrænnar reikningsfærslu**.
3. Á síðunni **Uppsetningar umhverfis**, á aðgerðasvæðinu, skal velja **Þjónustuumhverfi** og síðan velja **Færibreytur lyklageymslu**.
4. Veljið **Nýr** til að stofna leynilykil lyklageymslu.
5. Í reitinn **Heiti** skal slá inn heiti á leynilykli lyklageymslu. Í reitnum **Lýsing** skal færa inn lýsingu.
6. Í reitinn **URI lyklageymslu** skal líma leynilykilinn úr Azure-lyklageymslu.
7. Veljið **Vista**.

## <a name="create-storage-account-secret"></a>Stofna leynilykil geymslureiknings

1. Farið í **Kerfisstjórnun** > **Uppsetning** > **Færibreytur lyklageymslu** og veljið leynilykil lyklageymslu.
2. Í hlutanum **Vottorð** skal velja **Bæta við**.
3. Í reitinn **Heiti** skal færa inn heiti leynilykils geymslureikningsins og í reitinn **Lýsing** skal færa inn lýsingu.
4. Í reitnum **Gerð** skal velja **Vottorð**.
5. Veljið **Vista** og lokið síðan skjámyndinni.

## <a name="create-a-digital-certificate-secret"></a>Búa til leynilykil stafræns vottorðs

1. Farið í **Kerfisstjórnun** > **Uppsetning** > **Færibreytur lyklageymslu** og veljið leynilykil lyklageymslu.
2. Í hlutanum **Vottorð** skal velja **Bæta við**.
3. Í reitinn **Heiti** skal færa inn heiti leynilykils stafræns vottorðs og í reitinn **Lýsing** skal færa inn lýsingu.
4. Í reitnum **Gerð** skal velja **Vottorð**.
5. Veljið **Vista** og lokið síðan skjámyndinni.

## <a name="create-an-electronic-invoicing-add-on-environment"></a>Stofna umhverfi fyrir viðbót rafrænnar reikningsfærslu

1. Skráðu þig inn á RCS-reikninginn þinn.
2. Á vinnusvæðinu **Altækur eiginleiki**, í hlutanum **Umhverfi**, skal velja reitinn **Viðbót rafrænnar reikningsfærslu**.

## <a name="create-a-service-environment"></a>Stofna þjónustuumhverfi

1. Á síðunni **Uppsetningar umhverfis**, á aðgerðasvæðinu, skal velja **Þjónustuumhverfi**.
2. Velja skal **Nýtt** til að stofna nýtt þjónustuumhverfi.
3. Í reitinn **Heiti** skal slá inn heiti á umhverfi rafrænnar reikningsfærslu. Í reitnum **Lýsing** skal færa inn lýsingu.
4. Í reitnum **SAS-leynilykill geymslu** skal velja heiti leynilykils geymslureikningsins sem þarf að nota til að auðkenna aðgang að geymslureikningnum.
5. Í hlutanum **Notendur** skal velja **Bæta við** til að bæta við notanda sem hefur heimild til að senda inn rafræna reikninga í gegnum umhverfið og einnig tengjast við geymslureikninginn.
6. Í reitinn **Notandakenni** skal færa inn samnefni notandans. Í reitinn **Tölvupóstur** skal færa inn netfang notandans.
7. Veljið **Vista**.
8. Ef reikningar fyrir tiltekið land/svæði þurfa vottorðakeðju til að nota stafræna undirskrift, þá skal á aðgerðasvæðinu velja **Færibreytur lyklageymslu** og síðan velja **Vottorðakeðja** og fara í gegnum þessi skref:

    1. Veljið **Ný** til að búa til nýja vottorðakeðju.
    2. Í reitinn **Heiti** skal færa inn heiti vottorðakeðjunnar. Í reitnum **Lýsing** skal færa inn lýsingu.
    3. Í hlutanum **Vottorð** skal velja **Bæta við** til að bæta vottorði við keðjuna.
    4. Notið hnappinn **Upp** eða **Niður** til að breyta stöðu vottorðs í keðjunni.
    5. Veljið **Vista** og lokið síðan skjámyndinni.
    6. Lokið síðunni.
9. Á síðunni **Þjónustuumhverfi**, á aðgerðasvæðinu, skal velja **Birta** til að birta umhverfið í skýinu. Gildi reitsins **Staða** er breytt í **Birt**.

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

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance-and-supply-chain-management"></a>Setja upp samþættingu á viðbót rafrænnar reikningsfærslu í Finance and Supply Chain Management

### <a name="turn-on-the-electronic-invoicing-add-on-integration-feature"></a>Kveikið á eiginleika fyrir samþættingu rafrænnar reikningsfærsluviðbótar

1. Skráðu þig inn í tilvikið þitt af Finance eða Supply Chain Management.
2. Á vinnusvæðinu **Eiginleikastjórnun** skal leita að eiginleikanum **Samþætting viðbótar rafrænnar reikningsfærslu**. Ef þessi eiginleiki birtist ekki á síðunni skal velja **Athuga með uppfærslur**.
3. Veljið eiginleikann og veljið svo **Virkja núna**.

### <a name="set-up-the-service-endpoint-url"></a>Setja upp vefslóð fyrir endastöð þjónustu

1. Farið í **Fyrirtækisstjórnun \> Uppsetning \> Færibreytur rafrænna skjala**.
2. Í flipanum **Innsendingarþjónusta**, í reitinn **Vefslóð fyrir endastöð þjónustu** skal slá inn viðeigandi endastöð þjónustu fyrir Azure-staðfestinguna þína eins og sýnt er í eftirfarandi töflu.

    | Gagnamiðstöð Azure-staðsetningar | ULR endastöð þjónustu                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | Austurhluti Bandaríkjanna                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | Vesturhluti Bandaríkjanna                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | Norðurhluti Evrópusambandsins                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | Vesturhluti Evrópusambandsins                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

3. Í reitinn **Umhverfi** skal færa inn heiti á umhverfi rafrænnar reikningsfærsluviðbótar.
4. Veljið **Vista** og lokið síðan skjámyndinni.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
