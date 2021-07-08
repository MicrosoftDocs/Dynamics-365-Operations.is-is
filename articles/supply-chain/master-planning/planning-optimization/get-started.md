---
title: Byrjaðu með hagræðingu skipulags
description: Þetta efnisatriði útskýrir hvernig skuli hefja notkun á virkninni Fínstilling skipulagningar.
author: ChristianRytt
ms.date: 05/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 2867a4f9418e9435e2980fc24314914595ec44d0
ms.sourcegitcommit: cbbb35c71ab4ff1ae08fa4f7cc97019b207246be
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301675"
---
# <a name="get-started-with-planning-optimization"></a>Hafist handa með fínstillingu áætlanagerðar

[!include [banner](../../includes/banner.md)]

Eins og hefur [áður verið tilkynnt](../../get-started/removed-deprecated-features-scm-updates.md#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios), er á dagskrá að fínstilling skipulagningar takið við af núverandi innbyggðri vél aðaláætlanagerðar.

Ef verið er að nota innbyggða vél aðaláætlanagerðar, ætti að huga að flutningi yfir í fínstillingu skipulagningar. Mikilvægt er að hefja flutningsferlið strax vegna þess að aðgerðir þínar kunna að verða fyrir áhrifum þegar úreldingu er framfylgt. Til að koma í veg fyrir vandamál í síðustu stundu þegar úreldingu er framfylgt, mælum við eindregið með því að þú ljúkir við flutninginn fyrir 1. desember 2020. 

Sem stendur styður virknin fyrir fínstillingu skipulagningar ekki alla eiginleika sem eru í boði í vél áætlanagerðar sem er byggð inn í Supply Chain Management. Þess vegna er mikilvægt að þú metir hvort eiginleikasettið sem nú er fáanlegt í fínstillingu skipulagsins uppfylli kröfur þínar. Ekki er kveikt á virkni fyrir fínstillingu skipulagningar að sjálfgefnu sem stendur í Dynamics Lifecycle Services, þannig að þú hefur tækifæri til að meta stöðuna áður en kveikt er á eiginleikanum.

> [!NOTE]
> Þú þarft að biðja um undantekningu á flutningi yfir í fínstillingu skipulagningar ef ferli aðaláætlanagerðar felur ekki í sér framleiðslu (áætlaðar framleiðslupantanir sem aðaláætlanagerðin býr til) og þú þarft að nota innbyggða vél aðaláætlanagerðar í útgáfu sem er nýrri en 10.0.15. Frá og með útgáfu 10.0.16 verður sýnd villa í umhverfum þegar innbyggð aðaláætlanagerð er keyrð án þess að búa til áætlaðar framleiðslupantanir. Nota ætti fínstillingu skipulagningar fyrir allar nýjar uppsetningar sem búa ekki til áætlaðar framleiðslupantanir meðan á aðaláætlanagerð stendur. Eigendur núverandi umhverfa sem keyra innbyggða vél aðaláætlanagerðar án þess að búa til áætlaðar framleiðslupantanir, fá tölvupóst með upplýsingum um undantekningarferlið. Við mælum með því að þú vinnir með samstarfsaðila til að meta og leggja drög að flutningnum yfir í Fínstillingu skipulagningar.

Áður en þú kveikir á fínstillingu skipulags mælum við eindregið með því að þú metir niðurstöður greiningar á fínstillingu skipulagningar. Frekari upplýsingar er að finna í [Greining á samsvörun áætlunarfínstillingar](planning-optimization-fit-analysis.md).

## <a name="availability"></a>Til ráðstöfunar

Fínstilling áætlanagerðar er í boði í eftirfarandi Azure-svæðum: Bandaríkin, Kanada, Evrópa, Bretland og Ástralía og Asíu-Kyrrahafi. Ef reynt er að setja upp innbæturnar á öðru svæði birtir LCS skilaboð um að svæðið sé ekki stutt.

Athugið að fínstilling áætlanagerðar styður ekki uppsetningu á staðnum á Dynamics 365 Supply Chain Management.

## <a name="licensing"></a>Leyfisveiting

Ef þú getur keyrt aðalskipulagningu með því að nota núverandi leyfi þitt þarftu ekki að kaupa viðbótarleyfi til að byrja að nota fínstillingu skipulagsins.

## <a name="install-and-enable-planning-optimization"></a>Setja upp og virkja fínstillingu skipulagningar

Til að nota Fínstilling skipulagningar verður að ganga úr skugga um að kerfið sé með allar forkröfur í lagi og virkja svo leyfislykil þess og setja upp Viðbót fyrir Fínstillingu skipulagningar fyrir Dynamics 365 Supply Chain Management.

### <a name="prerequisites"></a>Forkröfur

Áður en viðbót fyri Fínstillingu skipulagningar er settu upp verður eftirfarandi að vera til staðar:

- Nauðsynlegt er að keyra Supply Chain Management á öflugu LCS virkt umhverfi, á stigi 2 eða hærra (ekki OneBox-umhverfi), með Dynamics 365 Supply Chain Management útgáfu 10.0.7 eða nýrri. Ef reynt er að setja upp viðbótina í OneBox-umhverfi verður uppsetningunni ekki lokið og því verður að hætta við uppsetninguna.

- Kerfið verður að vera sett upp fyrir Power Platform samþættingu. Frekari upplýsingar er að finna í [Microsoft Power Platform samþætting við Finance and Operations forrit](../../../fin-ops-core/dev-itpro/power-platform/overview.md).

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
| Tengir | Nú stendur yfir beiðni um að kveikja á tengingunni við þjónustuna fínstilling skipulagningar. | Nr |
| Aftengt | Engin tenging er við þjónustuna fínstilling skipulagningar. Hægt er að kveikja á tengingunni úr LCS, eins og lýst er fyrr í þessu efni. | Nr |
| Aftengir | Nú stendur yfir beiðni um að slökkva á tengingunni við þjónustuna fínstilling skipulagningar. | Nr |
| Sækir stöðu | Kerfið bíður eftir stöðuupplýsingum úr þjónustunni fínstilling skipulagningar. | Nr |

### <a name="the-use-planning-optimization-option"></a>Valkosturinn Nota fínstillingu skipulagningar

Stilling á valkostinum **Nota fínstillingu skipulags** ákvarðar hvaða áætlunarvél er notuð við aðaláætlanagerð:

- **Já** - Fínstilling skipulags er notuð við aðaláætlungargerð.
- **Nei** - Innbyggða áætlunarvélin Supply Chain Management er notuð til aðaláætlunargerðar.

Þessi stilling gildir um alla lögaðila (fyrirtæki). Ekki er hægt að nota fínstillingu skipulagningar í sumum lögaðilum og innbyggða aðaláætlanagerð í öðrum lögaðilum.

> [!NOTE]
> Ef fyrirliggjandi runuvinnslur áætlunargerðar sem voru stofnuð fyrir innbyggðu áætlunarvélina Supply Chain Management eru sett af stað á meðan valkosturinn **Nota fínstillingu skipulagningar** er stilltur á **Já** munu þær vinnslur ekki takast.

### <a name="integration-with-the-setup"></a>Samþætting við uppsetninguna

Ef kveikt er á fínstillingu áætlanagerðar er aðaláætlanagerð lokið með því að nota viðbót fyrir fínstillingu skipulagningar. Í þessu tilfelli verða niðurstöður og eiginleikar aðaláætlunargerðar fyrir áhrifum.

## <a name="additional-resources"></a>Frekari upplýsingar

[Ákvæði og skilmálar fyrir forskoðunina](https://go.microsoft.com/fwlink/?linkid=2015274)

[Yfirlit yfir fínstillingu áætlanagerðar](planning-optimization-overview.md)

[Greining á samsvörun áætlunarfínstillingar](planning-optimization-fit-analysis.md)

[Skoða áætlunarsögu og skipulagsskrár](plan-history-logs.md)

[Nota síur á áætlun](plan-filters.md)

[Hætta við áætlunarvinnslu](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
