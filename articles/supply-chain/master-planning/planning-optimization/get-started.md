---
title: Byrjaðu á aðalskipulagi
description: Þessi grein útskýrir hvernig á að byrja að nota aðalskipulagsvirkni í Dynamics 365 Supply Chain Management.
author: t-benebo
ms.date: 05/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 958de3f9ae6ead6cb6914bd3b7a4560e768013ab
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740330"
---
# <a name="get-started-with-master-planning"></a>Byrjaðu á aðalskipulagi

[!include [banner](../../includes/banner.md)]

Aðalskipulag í birgðakeðjustjórnun er veitt af ytri þjónustu sem kallast áætlanagerð hagræðingarviðbót fyrir Dynamics 365 Supply Chain Management. Þetta efni útskýrir hvernig á að fá og setja upp þá þjónustu.

## <a name="availability"></a>Framboð

Hagræðing áætlanagerðar er eins og er fáanleg í eftirfarandi Azure landsvæðum: Bandaríkjunum, Kanada, Brasilíu, Evrópu, Frakklandi, Bretlandi, Ástralíu, KyrrahafsAsíu, Japan og Indlandi. Ef reynt er að setja upp innbæturnar á öðru svæði birtir LCS skilaboð um að svæðið sé ekki stutt. Fyrir frekari upplýsingar um Azure landsvæði og tengd svæði, sjá [Azure landsvæði](https://azure.microsoft.com/global-infrastructure/geographies/#geographies).

Athugið að fínstilling áætlanagerðar styður ekki uppsetningu á staðnum á Dynamics 365 Supply Chain Management.

## <a name="licensing"></a>Leyfisveiting

Ef þú getur keyrt aðalskipulagningu með því að nota núverandi leyfi þitt þarftu ekki að kaupa viðbótarleyfi til að byrja að nota fínstillingu skipulagsins.

## <a name="install-and-enable-planning-optimization"></a>Setja upp og virkja fínstillingu skipulagningar

Til að nota Fínstilling skipulagningar verður að ganga úr skugga um að kerfið sé með allar forkröfur í lagi og virkja svo leyfislykil þess og setja upp Viðbót fyrir Fínstillingu skipulagningar fyrir Dynamics 365 Supply Chain Management.

### <a name="prerequisites"></a>Forkröfur

Áður en viðbót fyri Fínstillingu skipulagningar er settu upp verður eftirfarandi að vera til staðar:

- Nauðsynlegt er að keyra Supply Chain Management á öflugu LCS virkt umhverfi, á stigi 2 eða hærra (ekki OneBox-umhverfi), með Dynamics 365 Supply Chain Management útgáfu 10.0.7 eða nýrri. Ef reynt er að setja upp viðbótina í OneBox-umhverfi verður uppsetningunni ekki lokið og því verður að hætta við uppsetninguna.

- Kerfið verður að vera sett upp fyrir Power Platform samþættingu. Fyrir frekari upplýsingar, sjá [Microsoft Power Platform samþættingu við fjármála- og rekstraröpp](../../../fin-ops-core/dev-itpro/power-platform/overview.md).

### <a name="enable-the-planning-optimization-license"></a>Virkja leyfi Fínstillingar skipulagningar

Til að nota Fínstillingu skipulagningar verður að virkja skilgreiningarlykilinn. Þannig er það gert:

1. Setjið kerfið í viðhaldsstillingu eins og lýst er í [Viðhaldsstilling](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Opnið **Kerfisstjórnun \> Setja upp \> Skilgreining leyfis**.
1. Í flipanum **Skilgreiningarlyklar** skal velja gátreitinn fyrir **Fínstilling skipulagningar**.
1. Slökkvið á viðhaldsstillingu eins og lýst er í [Viðhaldsstilling](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).

### <a name="install-the-planning-optimization-add-in"></a>Setjið upp innbótina Fínstilling skipulagningar

Setja verður upp viðbótina frá LCS verkinu og kveikt á virkni fínstillingar skipulagningar úr notendaviðmóti (UI) Supply Chain Management notandaviðmóti.

Til að setja upp viðbót Fínstillingar skipulagningar:

1. Skráðu þig inn á LCS og opnaðu viðkomandi umhverfi.
1. Farðu í **Fullar upplýsingar**.
1. Flettu niður að flýtiflipanum **Umhverfisinnbætur**.
1. Veldu **Setja upp nýja innbót**.
1. Veldu **Fínstillingu skipulagningar**.
1. Fylgdu uppsetningarleiðbeiningunum og samþykktu skilmála og skilyrði.
1. Velja **Setja upp**.
1. Á flýtiflipanum **Umhverfisviðbætur** ættir þú að sjá að hagræðing skipulags er að setja upp.
1. Eftir nokkrar mínútur ætti **Setur upp** að breytast í **Uppsett** (þú gætir þurft að endurnýja síðuna). Þegar það er sett upp ertu tilbúinn til að virkja hagræðingu skipulags í Dynamics 365 Supply Chain Management.

Aðaltilgangurinn með því að setja upp viðbót fyrir fínstillingu skipulagningar er að tengja þjónustuna og umhverfið. Þess vegna þarf að setja viðbótina upp sérstaklega í hverju umhverfi þar sem nota á fínstillingu skipulagningar, óháð því hvaða kóði er fluttur á milli umhverfanna.

## <a name="integrate-planning-optimization-with-your-system"></a>Samþætta Fínstillingu skipulagningar við kerfið

Til að stilla hvort nota eigi innbótina fínstilling skipulagningara fyrir aðaláætlanagerð, farðu í **Aðaláætlanargerð** \> **Uppsetning** \> **Færibreytur fínstillingar skipulagningar**.

### <a name="connection-status"></a>Staða tengingar

Staða tengingarinnar gefur til kynna núverandi stöðu tengingarinnar milli Supply Chain Management og þjónustunnar Fínstilling skipulagningar. Eftirfarandi tafla sýnir hugsanleg gildi.

| Staða tengingar | Lýsing | Er hægt að nota fínstillingu skipulagningar? |
|---|---|---|
| Tengt | Tengingu hafa verið komið á milli þjónustunnar fínstilling skipulagningar og Supply Chain Management. | Já |
| Tengir | Nú stendur yfir beiðni um að kveikja á tengingunni við þjónustuna fínstilling skipulagningar. | Nei |
| Aftengt | Engin tenging er við þjónustuna fínstilling skipulagningar. Hægt er að kveikja á tengingunni frá LCS, eins og lýst er fyrr í þessari grein. | Nr. |
| Aftengir | Nú stendur yfir beiðni um að slökkva á tengingunni við þjónustuna fínstilling skipulagningar. | Nei |
| Sækir stöðu | Kerfið bíður eftir stöðuupplýsingum úr þjónustunni fínstilling skipulagningar. | Nei |

### <a name="the-use-planning-optimization-option"></a>Valkosturinn Nota fínstillingu skipulagningar

Stilling á valkostinum **Nota fínstillingu skipulags** ákvarðar hvaða áætlunarvél er notuð við aðaláætlanagerð:

- **Já** - Fínstilling skipulags er notuð við aðaláætlungargerð.
- **Nei** – Úrelta aðalskipulagsvélin er notuð við aðalskipulagningu.

Þessi stilling gildir um alla lögaðila (fyrirtæki). Ekki er hægt að nota áætlanagerð fínstillingu í sumum lögaðilum og úrelta aðalskipulagsvél í öðrum lögaðilum.

> [!NOTE]
> Ef fyrirliggjandi runuvinnslur áætlanagerðar sem voru stofnaðar fyrir úrelda aðalskipulagsvél eru ræst á meðan **Notaðu hagræðingu áætlanagerðar** valkostur er stilltur á **Já**, munu þau störf mistakast.

### <a name="integration-with-the-setup"></a>Samþætting við uppsetninguna

Ef kveikt er á fínstillingu áætlanagerðar er aðaláætlanagerð lokið með því að nota viðbót fyrir fínstillingu skipulagningar. Í þessu tilfelli verða niðurstöður og eiginleikar aðaláætlunargerðar fyrir áhrifum.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
