---
title: Regulatory Configuration Service
description: Í þessu efnisatriði er sýnt yfirlit yfir möguleika Regulatory Configuration Service (RCS) og útskýrt hvernig á að nálgast þessa þjónustu.
author: JaneA07
ms.date: 06/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 4ee68b691bba7f3314b5278b0bcc26504c1583335914a1e7c645abd5303f02c6
ms.sourcegitcommit: fa5ff2a0822aac16b518a2aea0d3389f79793390
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/07/2021
ms.locfileid: "7012014"
---
# <a name="regulatory-configuration-service"></a>Regulatory Configuration Service

[!include [banner](../includes/banner.md)]

Regulatory Configuration Service (RCS) sjálfstæður hönnuður þjónusta líftímastjórnunar fyrir altæka virkni án kóða/með litlum kóða. RCS gerir altækum hagsmunaaðilum kleift að stækka og sérstilla altæk svæði skatts, rafrænnar reikningsfærslu, lögbundna skýrslugerð, bankaviðskipti og viðskiptaskjöl án þess að þróunaraðilar þurfi að koma við sögu. Þessi altæka nálgun án kóða/með litlum kóða gerir sameininguna auðveldari, hraðvirkari og ekki eins kostnaðarsamt að búa til eða stækka.

RCS býður upp á eftirfarandi möguleika:

- Stuðningur fyrir alla virkni sem rafræn skýrslugerð býður upp á.
- Frumskilyrði til að skilgreina nýja altæka örþjónustu.
- Stuðningur fyrir rafræna reikningsfærslu. Frekari upplýsingar eru í [Rafrænar reikningsfærslur](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga).
- Stuðningur fyrir skattaútreikning. Nánari upplýsingar eru í [Skattaþjónusta](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).
- Stuðningur fyrir nýja virkni altæks eiginleika sem einfaldar líftímastjórnun fjölþátta eiginleika og veitir frekari möguleika til að skilgreina aðgerðir og setja upp færibreytur eiginleika. Frekari upplýsingar er að finna í [Regulatory Configuration Services – einfölduð altæk eiginleikastjórnun fyrir altækar þjónustur](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services).
- Stuðningur fyrir miðstýrða útgáfu, geymslu og deilingu á sérstilltum skilgreiningum í altækri geymslu til að einfalda skilgreiningarstjórnun án þess að þurfa að nota Microsoft Dynamics Lifecycle Services (LCS).

## <a name="access-rcs"></a>Aðgangur að RCS

Þú getur skráð þig fyrir eða skráð þig inn í RCS af síðunni [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/).

![Nýskráning/innskráning í RCS.](media/202103_RCS%20Marketing%20page_updated_1.jpg)

Á síðunni **Regulatory Configuration Service** skal yfirfara og samþykkja viðbótarskilmálana fyrir notkun á þjónustunni og síðan velja einn af eftirfarandi hnöppum:

- **Nýskráðu** þig ef þú ert að nota þjónustuna í fyrsta skipti og ert að nota netfang fyrirtækis til að úthluta þjónustuumhverfi fyrirtækisins
- **Innskráðu** þig þú hefur skráð þig fyrir þjónustunni áður og vilt opna umhverfi fyrirtækisins

> [!NOTE] 
> Þegar þú hefur skráð þig mælum við með því að þú bætir öðrum SysAdmin-notanda við RCS-umhverfið. Þessi notandi fær stöðuna annar stjórnandi fyrir umhverfið. Þetta hjálpar til við að veita stöðugleika fyrir aðgang að RCS-umhverfinu, þar sem hlutverk SysAdmin er að hafa umsjón með notendum fyrir það umhverfi. Þú getur bætt við notendum með því að nota **RCS vinnusvæði > Kerfisstjórnun**.

## <a name="regional-availability"></a>Svæði í boði

RCS er almennt í boði á eftirfarandi svæðum:

- Bandaríkin
- Indland
- Frakkland
- Evrópa

Fyrir heildarlista yfir svæði skal skoða [Dynamics 365 og Power Platform: Aðgengileiki, staðsetning gagna, tungumál og staðfærsla](https://aka.ms/dynamics_365_international_availability_deck).

## <a name="rcs-default-company"></a>Sjálfgefið fyrirtæki RCS

Virkni hönnunartíma sem er notuð í RCS er samnýtt í öllum fyrirtækjum. Engin virkni miðast við ákveðið fyrirtæki. Þess vegna er mælt með að nota eitt fyrirtæki, **DAT**, sem RCS-umhverfi.

Í sumum aðstæðum gæti verið sniðugt að láta snið rafrænnar skýrslugerðar nota færibreytur sem tengjst tilteknum lögaðila. Aðeins í þessum tilfellum ætti að nota val á sjálfgefnu fyrirtæki. Til dæmis sjá [Grunnstilla ER-snið til að nota færibreytur sem eru tilgreindar fyrir hvern lögaðila](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-configure-format.md).

## <a name="related-rcs-documentation"></a>Tengd RCS-fylgigögn

Frekari upplýsingar um tengda þætti er að finna í eftirfarandi efnisatriðum:

- **RCS:**

    - [Stofna skilgreiningar rafrænnar skýrslugerðar í RCS og hlaða þeim upp í altæka geymslu](rcs-global-repo-upload.md)

- **Altæk geymsla:**

    - [Búa til skilgreiningu rafrænnar skýrslugerðar og hlaða upp í altæka geymslu](rcs-global-repo-upload.md)
    - [Deila skilgreiningum í altækri geymslu](rcs-global-repo-share-configuration.md)
    - [Aukin síun í altækri geymslu](enhanced-filtering-global-repo.md)
    - [Sækja skilgreiningar rafrænnar skýrslugerðar úr altækri geymslu](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md)
    - [Hætta með skilgreiningar í altækri geymslu](discontinuing-configurations-rcs-global-repo.md)
    - [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) úrelding á geymslu](rcs-lcs-repo-dep-faq.md)

- **Altækur eiginleiki:**

    - [Regulatory Configuration Service (RCS) – altækur eiginleiki](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services)


## <a name="troubleshooting-rcs-sign-up"></a>Úrræðaleit vegna RCS-nýskráningar

Þegar þú skráir þig fyrir RCS af þjónustusíðunni gæti komið upp vandamál sem tengist Azure Active Directory (Azure AD). Villuboðin sem koma upp gefa til kynna að slökkt er á skráningu fyrir RCS og kveikja þarf á henni áður en hægt er að klára skráningarferlið.

![Villuboð RCS-skráningar.](media/01_RCSSignUpError.jpg)

Vandamálið kemur upp vegna þess að lokað er fyrir skráningu á tilfallandi áskriftum og virkja þarf eiginleikann `AllowAdHocSubscriptions` í leigjandanum. 

- Ef tæknideildin stjórnar Azure-leigjendum fyrirtækisins skal hafa samband við þá deild og láta vita af vandanum.
- Ef þú berð ábyrgð á umsjón leigjenda Azure getur þú leyst úr vandamálunum með því að fylgja skrefunum í [Hvað er nýskráning í sjálfsafgreiðslu fyrir Azure Active Directory](/azure/active-directory/enterprise-users/directory-self-service-signup#how-do-i-control-self-service-settings).
