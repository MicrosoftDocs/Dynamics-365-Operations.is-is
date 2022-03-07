---
title: Hafist handa með altækt birgðabókhald
description: Í þessu efnisatriði er lýst hvernig á að hefjast handa með altækt birgðabókhald.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: cfba2b8320399cc2eb3f2231e8a172d902633f16
ms.sourcegitcommit: 1e5a46271bf7fae2f958d2b1b666a8d2583e04a8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/25/2021
ms.locfileid: "7678860"
---
# <a name="get-started-with-global-inventory-accounting"></a>Hafist handa með altækt birgðabókhald

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)] <!--KFM: Until 4/30/2022 -->

Altækt birgðabókhald gerir kleift að nota meira en eitt birgðabókhald í fjárhagsbókum altæks birgðabókhalds sem búið er að setja upp. Tengja verður hvern fjárhag altæks birgðabókhalds við *viðtekna reglu*. Regla er safn af eftirfarandi gerðum reikningsskilaaðferða:

- Kostnaðarhlutur
- Grunnmæling inntaks
- Áætlun kostnaðarflæðis
- Kostnaðareining

> [!NOTE]
> Jafnvel eftir að kveikt er á altæku birgðabókhaldi er enn hægt að sinna birgðabókhaldi í Microsoft Dynamics 365 Supply Chain Management eins og venjulega.

Altækt birgðabókhald er innbót. Til að gera aðgerðir þess aðgengilegar verður þú að setja hana upp frá Microsoft Dynamics Lifecycle Services (LCS). Þú getur valið að meta það í prufuumhverfi áður en þú setur það í framleiðsluumhverfi.

Eins og er styður altækt birgðabókhald ekki alla eiginleika kostnaðarstjórnunar sem eru innbyggðir í Supply Chain Management. Þess vegna er mikilvægt að þú metir hvort grunneiginleikarnir sem nú eru tiltækir uppfylli kröfur þínar.

## <a name="how-to-get-the-global-inventory-accounting-public-preview"></a><a name="sign-up"></a>Hvernig á að fá opna forútgáfu altæks birgðabókhalds

> [!IMPORTANT]
> Til að nota altækt birgðabókhald verður þú að vera með stöðugt LCS-virkjað umhverfi (ekki OneBox-umhverfi). Auk þess þarf að keyra Supply Chain Management útgáfu 10.0.19 eða nýrri.

Til að skrá sig fyrir opinni forútgáfu altæks birgðabókhalds skal senda LCS-umhverfiskennið í tölvupósti á [Teymi altæks birgðabókhalds](mailto:GlobalInvAccount@microsoft.com). Þegar þú hefur fengið samþykki fyrir forritinu mun teymið senda þér eftirfylgnipóst sem inniheldur beta-lykil altæks birgðabókhalds og endastöðvar þjónustunnar. Þegar þú hefur fengið beta-lykilinn geturðu [sett upp innbótina](#install).

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

### <a name="set-up-dataverse"></a>Setja Dataverse upp

Áður en Dataverse er sett upp skal bæta þjónustureglum altæks birgðabókhalds við leigjandann með því að fylgja þessum skrefum.

1. Setjið upp Azure AD einingu fyrir Windows PowerShell v2 eins og lýst er í [Setja upp Azure Active Directory PowerShell fyrir Graph](/powershell/azure/active-directory/install-adv2).
1. Keyra eftirfarandi PowerShell-skipun.

    ```powershell
    Connect-AzureAD # (open a sign in window and sign in as a tenant user)

    New-AzureADServicePrincipal -AppId "7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9" -DisplayName "d365-scm-costaccountingservice"

    New-AzureADServicePrincipal -AppId "5f58fc56-0202-49a8-ac9e-0946b049718b" -DisplayName "d365-scm-operationdataservice"
    ```

Næst skal stofna notendur forrits fyrir altækt birgðabókhald í Dataverse með því að fylgja þessum skrefum.

1. Opnið vefslóð Dataverse umhverfisins.
1. Farið í **Ítarleg stilling \> Kerfi \> Öryggi \> Notendur** og stofnið notanda forrits. Notið reitinn **Yfirlit** til að breyta síðuyfirlitinu í *Notendur forrits*.
1. Veljið **Nýtt**.
1. Stilltu reitinn **Forritskenni** á *7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9*.
1. Veljið **Úthluta hlutverki** og veljið því næst *Kerfisstjóri*. Ef til er hlutverk sem heitir *Common Data Service Notandi* skal líka velja það.
1. Endurtakið skrefin á undan, en stillið reitinn **Forritskenni** á *5f58fc56-0202-49a8-ac9e-0946b049718b*.

Frekari upplýsingar eru í [Stofna notanda forrits](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).

Ef sjálfgefið tungumál Dataverse-uppsetningar er ekki enska skal fylgja þessum skrefum.

1. Farið í **Ítarleg stilling \> Stjórnun \> Tungumál**.
1. Veljið *Enska* (*LanguageCode=1033*) og síðan **Nota**.

## <a name="install-the-add-in"></a><a name="install"></a>Setja upp innbótina

Fylgið þessum skrefum til að setja upp innbótina þannig að hægt sé að nota altækt birgðabókhald.

1. [Skráðu þig](#sign-up) fyrir opinni forútgáfu altæks birgðabókhalds.
1. Skráðu þig inn í [LCS](https://lcs.dynamics.com/Logon/Index).
1. Farið í **Stjórnun forskoðunareiginleika**.
1. Veldu plústáknið (**+**).
1. Í reitinn **Kóði** skal slá inn beta-lykil innbótar fyrir altækt birgðabókhald. (Þú ættir að hafa fengið beta-lykilinn í tölvupósti þegar þú nýskráðir þig.)
1. Veldu síðan **Opna fyrir**.
1. Opnaðu LCS-umhverfi þar sem þú vilt bæta við þjónustunni.
1. Farðu í **Fullar upplýsingar**.
1. Farið í **Power Platform samþætting** og veljið **Uppsetning**.
1. Í svarglugganum **Uppsetning á umhverfi Power Platform** er gátreiturinn valinn og síðan **Uppsetning**. Venjulega tekur uppsetningin á milli 60 og 90 mínútur.
1. Að lokinni uppsetningu á Microsoft Power Platform-umhverfinu, í flýtiflipanum **Innbætur umhverfis**, skal velja **Setja upp nýja innbót**.
1. Veljið **Altækt birgðabókhald**.
1. Fylgdu uppsetningarleiðbeiningunum og samþykktu skilmála og skilyrði.
1. Velja **Setja upp**.
1. Í flýtiflipanum **Innbætur umhverfis** ættir þú að sjá að verið er að setja upp altækt birgðabókhald. Eftir nokkrar mínútur ætti staðan að breytast úr *Setur upp* í *Uppsett*. (Hugsanlega verður þú að endurhlaða síðuna til að breytingin komi í ljós). Á þeim tímapunkti er altækt birgðabókhald tilbúið til notkunar.

## <a name="set-up-the-integration"></a>Setja upp samþættingu

Fylgið þessum skrefum til að setja upp samþættingu milli altæks birgðabókhalds og Supply Chain Management.

1. Skráðu þig inn í Supply Chain Management.
1. Farið í **Kerfisstjórnun \> Eiginleikastjórnun**.
1. Veldu **Leita að uppfærslum**.
1. Í flipanum **Allt** skal leita að eiginleikanum sem heitir *Altækt birgðabókhald*.
1. Veldu **Virkja núna**.
1. Farið í **Altækt birgðabókhald \> Uppsetning \> Færibreytur altæks birgðabókhalds \> Færibreytur samþættingar**.
1. Í reitina **Endastöð gagnaþjónustu** og **Endastöð altæks birgðabókhalds** skal færa inn vefslóðir úr tölvupóstinum sem teymi altæks birgðabókhalds sendi þér þegar þú nýskráðir þig fyrir forútgáfunni.

Altækt birgðabókhald er nú tilbúið til notkunar.
