---
title: Veiting mannauðs í innviðum fjármála og rekstrar
description: Þessi grein útskýrir ferlið við að útvega nýtt framleiðsluumhverfi fyrir Microsoft Dynamics 365 Human Resources í fjármála- og rekstrarinnviðum.
author: twheeloc
ms.date: 01/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 15060d8bdd598476081c22d7280319da3db0cb31
ms.sourcegitcommit: 1401d66b6b64c590ca1f8f339d622e922920cf15
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/20/2022
ms.locfileid: "9178411"
---
# <a name="provision-human-resources-in-the-finance-and-operations-infrastructure"></a>Veiting mannauðs í innviðum fjármála og rekstrar

_**Á við um:** Mannauður um innviði fjármála- og rekstrarappa_ 

> [!NOTE]
> Frá og með júlí 2022 er ekki hægt að útvega nýtt mannauðsumhverfi á sjálfstæðum mannauðsinnviðum og nýjum Microsoft Dynamics Ekki er hægt að búa til verkefni um líftímaþjónustu (LCS). Viðskiptavinir geta innleitt mannauðsumhverfi á fjármála- og rekstrarinnviðum.

Þessi grein útskýrir ferlið við að útvega nýtt framleiðsluumhverfi fyrir Microsoft Dynamics 365 Human Resources í fjármála- og rekstrarinnviðum.

## <a name="prerequisites"></a>Forkröfur

Áður en þú byrjar að útvega nýtt umhverfi verða eftirfarandi forsendur að vera til staðar:

- Þú hefur keypt mannauð í gegnum CSP (Cloud Solution Provider) eða fyrirtækjaarkitektúr (EA) samning. Ef þú ert með fyrirliggjandi Dynamics 365 leyfi sem inniheldur nú þegar starfsmannaþjónustuáætlunina og þú getur ekki klárað skrefin í þessari grein, hafðu samband við þjónustudeild.
- Alheimsstjórinn hefur skráð sig inn á [Microsoft Dynamics Lífsferilsþjónusta (LCS)](https://lcs.dynamics.com) og búið til nýtt fjármála- og rekstrarverkefni.

## <a name="provision-a-human-resources-trial-environment"></a>Úthluta prófunarumhverfi Human Resources

> [!NOTE]
> Frá og með apríl 2022 verður prufuumhverfi mannauðs ekki tiltækt í sjálfstæðu forritinu. Hugsanlegir viðskiptavinir sem hafa áhuga á að meta mannauðsgetu í fjármála- og rekstraröppum geta notað ókeypis 30 daga prufuáskriftina ásamt kynningargögnum. Dynamics 365 Finance mun innihalda mannauðsmöguleikana sem eru færðir til Finance innviða með sameiningu sjálfstæða forritsins. Fyrir frekari upplýsingar, sjá [Sameining starfsmannaframboðs sameinar getu viðskiptavina](https://cloudblogs.microsoft.com/dynamics365/it/2021/09/15/merging-of-hr-offerings-brings-capabilities-together-for-customers). Fyrir frekari upplýsingar um Dynamics 365 Finance prufur, sjá [skref-fyrir-skref leiðbeiningar](../fin-ops-core/fin-ops/get-started/before-you-buy.md).

## <a name="plan-human-resources-environments"></a>Skipuleggja umhverfi Human Resources

Áður en fyrsta Human Resources-umhverfið er búið til ætti að kortleggja vel og vandlega þarfir umhverfisins fyrir verkið. Grunnáskrift að Human Resources inniheldur tvö umhverfi: framleiðsluumhverfi og sjálfgefið staðlað samþykkispróf (Sandbox) umhverfi. Það fer eftir því hversu flókið verkefnið er, þú hefur möguleika á að kaupa viðbótarumhverfi til að styðja við verkefnisstarfsemi.

Hér eru nokkur atriði varðandi valfrjálst viðbótarumhverfi:

- **Gagnaflutningur** – Gagnaflutningar gera kleift að nota sandkassaumhverfið þitt í prófunartilgangi í gegnum verkefnið. Þegar þú ert með viðbótarumhverfi getur gagnaflutningsaðgerðir haldið áfram á meðan prófunar- og stillingaraðgerðir eiga sér stað samtímis í öðru umhverfi.
- **Samþætting** – Stilla og prófa samþættingar, sem gætu falið í sér innbyggðar samþættingar eða sérsniðnar samþættingar, eins og þær fyrir launaskrá, rakningarkerfi umsækjenda eða bótakerfi og veitendur.
- **Þjálfun** – Þú gætir þurft sérstakt umhverfi sem er stillt með mengi af þjálfunargögnum, svo þú getir þjálfað starfsmenn þína í notkun nýja kerfisins. 
- **Fjölfasa verkefni** – Þú gætir þurft viðbótarumhverfi til að styðja við uppsetningu, gagnaflutning, prófun eða aðra starfsemi í verkefnisfasa sem er fyrirhugaður eftir upphaflega gangsetningu verkefnisins.
- **Þróun** – Í fjármála- og rekstrarinnviðum geturðu nú framlengt lausnina og þróað þínar eigin aðlögun. Hver verktaki þarf að nota sitt eigið þróunarumhverfi. Fyrir frekari upplýsingar, sjá [Dreifa og fá aðgang að þróunarumhverfi](/fin-ops-core/dev-itpro/dev-tools/access-instances).
- **GULL** – Fyrir nýjar dreifingar er algeng venja að nota sérstakt GOLD umhverfi sem er haldið óspilltu fyrir uppsetningu og gagnaflutning. Þetta umhverfi er hægt að nota í gegnum útfærsluna til að fríska upp á annað umhverfi. Það verður notað til að búa til nýja framleiðsluumhverfið sem hefur grunnstillingu og gagnaflutning. Þú getur ekki sett upp framleiðsluumhverfi á fjármála- og rekstrarinnviðum fyrr en þú hefur lokið viðbúnaðarferlinu. Fyrir frekari upplýsingar, sjá [Undirbúðu þig fyrir gangsetningu](/fin-ops-core/fin-ops/imp-lifecycle/prepare-go-live).

<!--NOTE: Need to come back and verify Tier-1 can be used and if a customer cannot purchase tier 3-5 need specific documentation about this.-->

> [!IMPORTANT]
> Þegar þú íhugar umhverfi þitt mælum við með eftirfarandi aðferð:
>
> - Notaðu sjálfgefna staðlaða samþykkisprófið þitt (áður Sandbox) umhverfið þitt eða annað umhverfi til að gera sýndarklippingu áður en þú byrjar.
> - Hafðu ítarlegan gátlista fyrir niðurfellingu sem inniheldur hvern gagnapakka sem þarf til að flytja lokagögnin yfir í framleiðsluumhverfið meðan á útfærslunni stendur. Þessi tilmæli eru sérstaklega mikilvæg ef þú ert ekki með sérstakt GOLD umhverfi til að geyma stillingarnar þínar.
> - Notaðu sjálfgefið staðlað staðfestingarpróf (áður Sandbox) umhverfi þitt eða annað tier-2 eða hærra umhverfi sem PRÓFUMhverfi þitt í gegnum verkefnið þitt. Ef þú þarft viðbótarumhverfi getur fyrirtækið þitt keypt þau gegn aukakostnaði.

## <a name="create-an-lcs-project"></a>Búa til LCS-verk

Til að nota LCS til að stjórna Human Resources umhverfi þínu, þarftu fyrst að búa til LCS-verk. Ef þú ert að flytja mannauðsumhverfið þitt yfir í fjármála- og rekstrarinnviðina, verður þú að búa til nýtt LCS verkefni fyrir fjármála- og rekstrarforrit. Fyrir frekari upplýsingar, sjá [Flytja mannauðsumhverfið þitt](hr-admin-migrate-overview). Ef þú ert nú þegar með LCS verkefni fyrir önnur fjármála- og rekstrarforrit geturðu virkjað mannauðseiginleikana í **Eiginleikastjórnun** vinnurými. Frekari upplýsingar er að finna í [Eiginleikastjórnunaryfirlit](/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

Þegar nýr viðskiptavinur skráir sig í mannauð inniheldur áskriftin vinnusvæði fyrir framkvæmdarverkefni. Eftir að viðskiptavinur virkjar þjónustuna þarf umsjónarmaður leigjanda að skrá sig inn á<https://lcs.dynamics.com> með því að nota leigjandareikninginn. Verkefnavinnusvæðið er sjálfkrafa búið til fyrir fyrirtækið. Fyrir frekari upplýsingar, sjá [Lifecycle Services (LCS) fyrir viðskiptavini fjármála- og rekstrarappa](/fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs).

> [!NOTE]
> Til að tryggja árangursríka úthlutun verður að úthluta reikningnum sem þú notar til að útvega mannauðsumhverfið annaðhvort **Kerfisstjóri** hlutverk eða **Kerfisaðlögun** hlutverk í Power Apps umhverfi sem tengist mannauðsumhverfi. Fyrir frekari upplýsingar um hvernig á að úthluta öryggishlutverkum til notenda í Microsoft Power Platform, sjá [Stilltu öryggi notenda fyrir auðlindir](/power-platform/admin/database-security).

Þú verður að ljúka innleiðingarferli LCS verkefnisins áður en þú getur byrjað að dreifa umhverfi. Fyrir frekari upplýsingar, sjá [Inngangur verkefna](/fin-ops-core/dev-itpro/lifecycle-services/project-onboarding). Fyrir frekari upplýsingar um hvernig á að nota LCS, sjá [Lifecycle Services (LCS) notendahandbók](/fin-ops-core/dev-itpro/lifecycle-services/lcs-user-guide).

## <a name="deploy-human-resources-environments"></a>Settu upp mannauðsumhverfi

Innleiðing fjármála- og rekstrarforrita, þar með talið mannauðs, í skýinu krefst þess að þú skiljir umhverfið og áskriftina sem þú ert að dreifa til, hver getur framkvæmt hvaða verkefni og hvaða gögn og sérstillingar þú verður að stjórna. Við mælum með því að þú notir þjónustureikning í stað nafngreinds notanda þegar þú setur upp nýtt umhverfi. Fyrir frekari upplýsingar um hvernig á að dreifa umhverfi á fjármála- og rekstrarinnviðum, sjá [Yfirlit yfir dreifingu skýja](/fin-ops-core/dev-itpro/deployment/cloud-deployment-overview).

Til að setja upp framleiðsluumhverfi fyrir mannauð á fjármála- og rekstrarinnviðum verður þú að ljúka viðbúnaðarferlinu. Fyrir frekari upplýsingar, sjá [Undirbúðu þig fyrir gangsetningu](/fin-ops-core/fin-ops/imp-lifecycle/prepare-go-live). Þetta ferli inniheldur áskriftarmatið í LCS. Fyrir frekari upplýsingar, sjá [Áskriftarmat](/fin-ops-core/dev-itpro/lifecycle-services/subscription-estimator).

## <a name="integrate-microsoft-power-platform-with-human-resources"></a>Samþætta Microsoft Power Platform með mannauði

Microsoft Power Platform býður upp á fjölda möguleika fyrir Dynamics 365 forrit í gegnum Power Platform stjórnendamiðstöð. Þú getur samþætt og framlengt notkun mannauðsgagna með því að nota Microsoft Power Platform. Fyrir upplýsingar um hvernig á að samþætta mannauð við Microsoft Power Platform, sjá [Microsoft Power Platform samþættingu við Finance and Operations öpp](/fin-ops-core/dev-itpro/power-platform/overview).

## <a name="supported-geographies"></a>Studdar staðsetningar

Fyrir upplýsingar um tungumál og landsvæði sem eru studd fyrir mannauð, sjá [Alþjóðlegt að hönnun: Lærðu um lönd og tungumál sem studd eru](https://dynamics.microsoft.com/availability-reports/).

## <a name="grant-access-to-the-environment"></a>Veita aðgang að umhverfinu

Að sjálfgefnu hefur altæki stjórnandinn sem bjó til umhverfið aðgang að því. Þú verður að veita sérstaklega aðgang til viðbótarnotenda forritsins. Þú verður að bæta við notendum og úthluta þeim viðeigandi hlutverkum í umhverfi Human Resources. Frekari upplýsingar má finna í [Stofna nýja notendur](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) og [Úthluta notendum á öryggishlutverk](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles).

## <a name="additional-resources"></a>Frekari upplýsingar
Þú getur lært meira um hvernig á að nota og stjórna verkefnum í LCS á innviðum fjármála- og rekstrarappa með því að nota eftirfarandi úrræði:

- [Tilföng Lifecycle Services](/fin-ops-core/dev-itpro/lifecycle-services/lcs.md)
- [Notandahandbók Lifecycle Services (LCS)](/fin-ops-core/dev-itpro/lifecycle-services/lcs-user-guide.md)
- [Yfirlit yfir uppsetningu sjálfsafgreiðslu](../fin-ops-core/dev-itpro/deployment/infrastructure-stack.md)
- [Heimasíða starfsemi gagnagrunnshreyfinga](../fin-ops-core/dev-itpro/database/dbmovement-operations.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
