---
title: Fartækjavinnusvæði fyrir samþykkt innkaupapöntunar
description: Þessi grein veitir upplýsingar um fartækjavinnusvæðið fyrir samþykkt innkaupapöntunar sem gerir þér kleift að skoða innkaupapantanir og svara þeim með aðgerðum. Til dæmis er hægt að samþykkja eða hafna innkaupapöntun.
author: GalynaFedorova
ms.date: 05/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchVendorPortalRequests
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30211
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b5336549937edca6beb94137896f84b460f257f7
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111331"
---
# <a name="purchase-order-approval-mobile-workspace"></a>Fartækjavinnusvæði fyrir samþykkt innkaupapöntunar

[!include [banner](../includes/banner.md)]
[!include [mobile app deprecation](../../fin-ops-core/dev-itpro/includes/mobile-app-deprecation-banner.md)]

Þessi grein veitir upplýsingar um fartækjavinnusvæðið **Samþykki innkaupapöntunar**. Þetta vinnusvæði gerir kleift að skoða innkaupapantanir og bregðast við þeim með aðgerðum. Til dæmis er hægt að samþykkja eða hafna innkaupapöntun.
 
## <a name="overview"></a>Yfirlit 
Innkaupapantanir sem þarfnast samþykkis fara í gegnum samþykktarverkflæði. Verkflæðið getur innihaldið ýmis þrep sem krefjast þess að einn eða fleiri einstaklingar grípi til aðgerða. Til dæmis gæti einstaklingur þurft að ljúka við verk eða samþykkja innkaupapöntunina. 

Vinnusvæðið **Samþykkt innkaupapöntunar** gerir kleift að skoða á auðveldan hátt og bregðast við innkaupapöntunum úr fartækinu. Þetta vinnusvæði leyfir þér einnig að grípa til sömu verkflæðisaðgerða sem þú getur gripið til í vefbiðlara.

## <a name="prerequisites"></a>Forkröfur
Forkröfur eru mismunandi eftir þeirri útgáfu Supply Chain Management sem hefur verið innleidd í fyrirtækinu.

### <a name="prerequisites-if-you-use-supply-chain-management"></a>Forkröfur ef þú notar Supply Chain Management 
Ef Supply Chain Management hefur verið innleitt í fyrirtækinu verður kerfisstjóri að birta fartækjavinnusvæðið **Samþykkt innkaupapöntunar**. Leiðbeiningar er að finna í [Fartækjavinnusvæði birt](../../fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Skilyrði ef þú notar Microsoft Dynamics 365 for Operations útgáfu 1611 með verkvangsuppfærslu 3 eða nýrri
Ef Microsoft Dynamics 365 for Operations útgáfa 1611 með verkvangsuppfærslu 3 eða síðar hefur verið sett upp fyrir fyrirtækið þitt, verður kerfisstjórinn að ljúka eftirfarandi skilyrðum. 

<table>
<thead>
<tr class="header">
<th>Skilyrði</th>
<th>Hlutverk</th>
<th>lýsing</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Innleiða KB 4017918.</td>
<td>Kerfisstjóri</td>
<td>KB 4017918 er X++ uppfærsla eða lýsigagnabráðabót sem inniheldur fartækjavinnusvæðið <strong>Samþykkt innkaupapöntunar</strong>. Til að setja upp KB 4017918 verður kerfisstjóri að fylgja eftirfarandi skrefum.
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Sækja bráðabót lýsigagna frá Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Setja upp bráðabót lýsigagna</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Stofna virkjanlegan pakka</a> sem inniheldur <strong>SCMMobile</strong> líkanið og hlaða síðan virkjanlega pakkann í LCS.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Notaðu virkjanlega pakkann</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Útgáfa fartækjavinnusvæðisins <strong>Samþykkt innkaupapöntunar</strong></td>
<td>Kerfisstjóri</td>
<td>Sjáið <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Fartækjavinnusvæði birt</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Sæktu og settu upp fartækjaforritið
Sæktu og settu upp fartækjaforrit fyrir fjármál- og rekstur:

- [Fyrir Android síma](https://go.microsoft.com/fwlink/?linkid=850662)
- [Fyrir iPhone síma](https://go.microsoft.com/fwlink/?linkid=850663)


## <a name="sign-in-to-the-mobile-app"></a>Innskráning í fartækjaforritið

1. Ræstu forritið í fartækinu þínu.
2. Færðu inn vefslóð þína fyrir Microsoft Dynamics 365.
3. Í fyrsta sinn sem þú skráir þig inn, er beðið um notandanafn og aðgangsorð þitt. Færðu inn skilríki
4. Eftir að þú hefur skráð þig inn, birtast tiltæk vinnusvæði fyrir fyrirtækið. Athugið að ef kerfisstjóri gefur út nýtt vinnusvæði síðar, verður að endurræsa listann yfir fartækjavinnusvæði.

![Vinnusvæði samþykktar á innkaupapöntun í lista yfir tiltæk vinnusvæði.](./media/po-workspaces.png)

## <a name="view-orders-that-are-assigned-to-you"></a>Skoða pantanir sem þér hefur verið úthlutað
1. Veldu vinnusvæðið **Samþykkt innkaupapöntunar** í fartækinu.
2. Veldu **Pantanir úthlutaðar á mig** til að skoða allar innkaupapantanir þar sem þú hefur verið beðin(n) um að grípa til aðgerða í verkflæði samþykktar á innkaupapöntun.
3. Veldu pöntun. Á síðunni **Upplýsingar um pöntun** sjást hausupplýsingar og línur pöntunar. Einnig er hægt að finna leiðbeiningar í verkflæðisverkinu.
4. Veldu **Dreifing á fjárhagsupphæð** til að opna síðuna **Dreifing á fjárhagsupphæð hauss**.
5. Farðu aftur á síðuna **Upplýsingar um pöntun** og veldu línu. Úr upplýsingum um pöntunarlínu er einnig hægt að skoða línutengda dreifingu á fjárhagsupphæð.

## <a name="complete-an-action-on-the-purchase-order"></a>Ljúka við aðgerð í innkaupapöntun
Þegar þú hefur skoðað innkaupapöntunina sem þér hefur verið úthlutað og þú hefur lesið verkflæðisfyrirmæli ættir þú að vera tilbúin(n) til aðgerða.

1. Veldu vinnusvæðið **Samþykkt innkaupapöntunar** í fartækinu.
2. Veldu **Pantanir úthlutaðar á mig** til að skoða allar innkaupapantanir þar sem þú hefur verið beðin(n) um að grípa til aðgerða í verkflæði samþykktar á innkaupapöntun.
3. Veldu pöntun og skoðaðu upplýsingasíðuna.
4. Veldu **Aðgerðir** til að sýna tiltækar aðgerðir. Aðgerðir sem eru tiltækar fara eftir verkinu sem þér hefur verið úthlutað.

    | Verkaðgerð    | Samþykktaraðgerð  |
    |----------------|------------------|
    | Tilbúið       | Samþykkja          |
    | Vöruskil         | Hafna           |
    | Biðja um breytingu | Biðja um breytingu   |
    | Úthluta       | Úthluta         |

5. Velja viðeigandi aðgerð.
6. Færðu inn athugasemd á síðunni **Ljúka verki**. Athugaðu að ef þú velur aðgerðina **Úthluta**, verður þú að velja notanda til að úthluta verkinu.
7. Velja **Ekkert**. Þegar þú endurnýjar vinnusvæðið hverfur innkaupapöntunin af listanum. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

