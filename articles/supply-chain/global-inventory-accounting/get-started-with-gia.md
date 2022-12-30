---
title: Hafist handa með altækt birgðabókhald
description: Í þessari grein er lýst hvernig á að hefjast handa með altækt birgðabókhald.
author: JennySong-SH
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 463a66002ec7a6536c9ff829f9ea2c3734138eae
ms.sourcegitcommit: 6221a25f81aa83ab335de7cb6b6c3014dbec0116
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/19/2022
ms.locfileid: "9177149"
---
# <a name="get-started-with-global-inventory-accounting"></a>Hafist handa með altækt birgðabókhald

[!include [banner](../includes/banner.md)]

Altækt birgðabókhald gerir kleift að nota meira en eitt birgðabókhald í fjárhagsbókum altæks birgðabókhalds sem búið er að setja upp. Tengja verður hvern fjárhag altæks birgðabókhalds við *viðtekna reglu*. Regla er safn af eftirfarandi gerðum reikningsskilaaðferða:

- Kostnaðarhlutur
- Grunnmæling inntaks
- Áætlun kostnaðarflæðis
- Kostnaðareining

> [!NOTE]
> Jafnvel eftir að kveikt er á altæku birgðabókhaldi er enn hægt að sinna birgðabókhaldi í Microsoft Dynamics 365 Supply Chain Management eins og venjulega.

Altækt birgðabókhald er innbót. Til að gera aðgerðir þess aðgengilegar verður þú að setja hana upp frá Microsoft Dynamics Lifecycle Services (LCS). Þú getur valið að meta það í prufuumhverfi áður en þú setur það í framleiðsluumhverfi.

Eins og er styður altækt birgðabókhald ekki alla eiginleika kostnaðarstjórnunar sem eru innbyggðir í Supply Chain Management. Þess vegna er mikilvægt að þú metir hvort grunneiginleikarnir sem nú eru tiltækir uppfylli kröfur þínar.

## <a name="how-to-get-the-global-inventory-accounting-add-in"></a><a name="sign-up"></a>Hvernig á að fá innbót altæks birgðabókhalds

> [!IMPORTANT]
> Til að nota altækt birgðabókhald verður þú að vera með stöðugt LCS-virkjað umhverfi (ekki OneBox-umhverfi). Auk þess þarf að keyra Supply Chain Management útgáfu 10.0.19 eða nýrri.

### <a name="supply-chain-management-version-10019-to-10026"></a>Supply Chain Management útgáfa 10.0.19 til 10.0.26

Til að setja upp altækt birgðabókhald fyrir Supply Chain Management útgáfu 10.0.19 til 10.0.26 skal byrja á því að [setja upp innbótina](#install). Sendu síðan LCS-umhverfiskenni og heiti fyrirtækisins með tölvupósti á [Teymi altæks birgðabókhalds](mailto:GlobalInvAccount@microsoft.com). Teymið sendir þér eftirfylgnipóst sem inniheldur endastöðvar fyrir altæka birgðabókhaldsþjónustu.

### <a name="supply-chain-management-version-10027-and-later"></a>Supply Chain Management útgáfa 10.0.27 og nýrri

Til að setja upp altækt birgðabókhald fyrir Supply Chain Management útgáfu 10.0.27 og nýrri skal einfaldlega [setja upp innbótina](#install). Fyrir þessar útgáfur af Supply Chain Management verða endapunktar alhliða birgðabókhalds settir upp sjálfkrafa svo þú þarft ekki að finna þá handvirkt. Ef þú lendir í vandræðum við uppsetningu viðbótarinnar skaltu hafa samband við teymi [Altæks birgðabókhalds](mailto:GlobalInvAccount@microsoft.com).

## <a name="licensing"></a>Leyfisveiting

Leyfisveiting altæks birgðabókhalds fer saman við hefðbundna eiginleika birgðabókhalds sem eru í boði fyrir Supply Chain Management. Þú þarft ekki að kaupa viðbótarleyfi til að nota altækt birgðabókhald.

## <a name="prerequisites"></a>Forkröfur

### <a name="set-up-microsoft-power-platform-integration"></a>Setja upp Microsoft Power Platform-samþættingu

Áður en hægt er að virkja virkni innbótarinnar þarf að samþætta við Microsoft Power Platform með því að fylgja þessum skrefum.

1. Opnaðu LCS-umhverfi þar sem þú vilt bæta við þjónustunni.
1. Farðu í **Fullar upplýsingar**.
1. Í hlutanum **Power Platform samþætting** skal velja **Uppsetning**.
1. Í svarglugganum **Uppsetning á umhverfi Power Platform** er gátreiturinn valinn og síðan **Uppsetning**. Venjulega tekur uppsetningin á milli 60 og 90 mínútur.
1. Að lokinni uppsetningu Microsoft Power Platform sýnir síðan heiti umhverfisins. Auk þess sýnir hlutinn **Power Platform samþætting** fullyrðinguna „uppsetningu Power Platform-umhverfis er lokið“. Altækt birgðabókhald krefst ekki forrits tvöfaldrar skráningar.

Frekari upplýsingar er að finna í [Virkja að lokinni uppsetningu umhverfis](../../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md#enable-after-deploy).

## <a name="install-or-update-the-add-in-and-solution"></a><a name="install"></a>Setja upp eða uppfæra viðbót og lausn

Notaðu eftirfarandi ferli til að setja upp eða uppfæra innbót og lausn altæks birgðabókhalds. Hluti ferlisins sem þú ættir að fylgjast með fer eftir því hvort þú ert að setja upp í fyrsta skipti eða þarft bara að uppfæra lausnina fyrir fyrirliggjandi uppfærslu.

- Ef þú hefur aldrei sett viðbótina upp áður skaltu fylgja öllu ferlinu til að setja upp bæði viðbótina og lausnina.
- Ef þú ert að nota altækt birgðabókhald en þarft að uppfæra lausnina í [Power Platform stjórnendamiðstöðinni](https://admin.powerplatform.microsoft.com) skal aðeins fara í gegnum skref 6 og sleppa hinum skrefunum.

Til að setja upp eða uppfæra viðbót og lausn:

1. Skráðu þig inn í [LCS](https://lcs.dynamics.com/Logon/Index).
1. Opnaðu LCS-umhverfi þar sem þú vilt bæta við þjónustunni.
1. Farðu í **Fullar upplýsingar**.
1. Farið í **Power Platform samþætting** og veljið **Uppsetning**.
1. Í svarglugganum **Uppsetning á umhverfi Power Platform** er gátreiturinn valinn og síðan **Uppsetning**. Venjulega tekur uppsetningin á milli 60 og 90 mínútur.
1. Þegar uppsetningu Microsoft Power Platform umhverfisins er lokið skaltu skrá þig inn í [Power Platform stjórnendamiðstöðina](https://admin.powerplatform.microsoft.com) og setja síðan upp eða uppfæra lausn altæks birgðabókhalds með því að gera eftirfarandi skref:
   1. Veldu umhverfið þar sem þú vilt setja upp eða uppfæra lausnina.
   1. Veldu **Dynamics 365 forrit**.
   1. Veldu **Setja upp forrit**.
   1. Veldu **Dynamics 365 Altækt birgðabókhald**.
   1. Smellið á **Næsta** til að setja upp.
1. Eftir að lausnin hefur verið sett upp skal fara aftur í LCS umhverfi. Í flýtiflipanum **Innbætur umhverfis** skal velja **Setja upp nýja innbót**.
1. Veljið **Altækt birgðabókhald**.
1. Fylgdu uppsetningarleiðbeiningunum og samþykktu skilmála og skilyrði.
1. Velja **Setja upp**.
1. Í flýtiflipanum **Innbætur umhverfis** ættir þú að sjá að verið er að setja upp altækt birgðabókhald. Eftir nokkrar mínútur ætti staðan að breytast úr *Setur upp* í *Uppsett*. (Hugsanlega verður þú að endurhlaða síðuna til að breytingin komi í ljós). Á þeim tímapunkti er altækt birgðabókhald tilbúið til notkunar.

Ef sjálfgefið tungumál Dataverse-uppsetningar er ekki enska skal fylgja þessum skrefum.

1. Farið í **Ítarleg stilling \> Stjórnun \> Tungumál**.
1. Veljið *Enska* (*LanguageCode=1033*) og síðan **Nota**.

## <a name="set-up-the-integration"></a>Setja upp samþættingu

Fylgið þessum skrefum til að setja upp samþættingu milli altæks birgðabókhalds og Supply Chain Management.

1. Skráðu þig inn í Supply Chain Management.
1. Farið í **Kerfisstjórnun \> Eiginleikastjórnun**.
1. Veldu **Leita að uppfærslum**.
1. Í flipanum **Allt** skal leita að eiginleikanum sem heitir *(forskoðun) Altækt birgðabókhald*.
1. Veldu **Virkja núna**.
1. Farið í **Altækt birgðabókhald \> Uppsetning \> Færibreytur altæks birgðabókhalds \> Færibreytur samþættingar**.
1. Gerðu eitt af eftirfarandi skrefum eftir því hvaða útgáfu af Supply Chain Management þú ert að keyra:
    - **Supply Chain Management útgáfa 10.0.19 til 10.0.26**: Í reitina **Endastöð gagnaþjónustu** og **Endastöð altæks birgðabókhalds** skal færa inn vefslóðirnar sem voru sendar þér í tölvupósti frá teymi altæks birgðabókhalds (sjá einnig [Hvernig á að ná í innbót altæks birgðabókhalds](#sign-up)).
    - **Supply Chain Management útgáfa 10.0.27 og nýrri**: Ekki þarf að færa inn endastöðarnar þannig að þú getur sleppt þessu skrefi.

Altækt birgðabókhald er nú tilbúið til notkunar.
