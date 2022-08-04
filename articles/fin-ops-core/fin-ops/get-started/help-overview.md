---
title: Hjálparkerfi (inniheldur myndband)
description: Þessi grein veitir yfirlit yfir hjálparkerfið fyrir fjármála- og rekstrarforrit.
author: edupont04
ms.date: 07/20/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: tfehr
ms.custom:
- "16381"
- intro-internal
ms.assetid: 018c148c-9cbd-41e0-8186-d75dbf66288f
ms.search.region: Global
ms.author: edupont
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 57c17cab920c531b3eb125260064d01dd8662576
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 07/06/2022
ms.locfileid: "9124195"
---
# <a name="help-system"></a>Hjálparkerfi

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Notendur eftirfarandi forrita geta fengið aðgang að samhengishjálp og öðru efni sem byggist á sama hjálparkerfi:

- Dynamics 365 Commerce
- Dynamics 365 Finance
- Dynamics 365 Human Resources
- Dynamics 365 Supply Chain Management

Í öllum þessum forritum er hægt að fá aðgang að hjálp fyrir tiltekna vöru af svæðinu **Hjálp**.

![Hjálparsvæði.](./media/help-pane-ops-help.png)

## <a name="help-on-docsmicrosoftcom"></a>Hjálp á docs.microsoft.com

Svæðið docs.microsoft.com ([docs.microsoft.com/dynamics365](/dynamics365/)) er sjálfgefinn uppruni fyrir fylgiskjöl fyrir áður skráð forrit. Þetta vefsvæði býður upp á eftirfarandi eiginleika:

- **Aðgangur að nýjasta efninu** – svæðið gefur Microsoft hraðar og sveigjanlegri leið til að stofna, afhenda og uppfæra fylgiskjal vöru. Þess vegna er auðvelt að fá aðgang að nýjustu tækniupplýsingum.
- **Efni sem er skrifað af sérfræðingum** – Aðilar samfélagsins, hvort sem þeir starfa hjá Microsoft eða ekki, geta lagt fram efni á vefsvæðið.

Hægt er að finna efni á docs.microsoft.com með því að nota hvaða leitarvél sem er. Til að niðurstöður verði sem bestar mælum við með að þú notir leit á vefsvæðum, svo sem **site:docs.microsoft.com dynamics 365 „leitarorð“**.

## <a name="get-notified-about-changes-through-an-rss-feed"></a>Fá tilkynningu um breytingar með RSS-straumi

Til að gerast áskrifandi að RSS straumi fyrir allar uppfærslur sem gerðar eru á efninu á docs.microsoft.com í gegnum fjármála- og rekstrarforritin, notaðu eftirfarandi tengil:

[RSS-straumur](/api/search/rss?$filter=scopes%2fany(t%3A%20t%20eq%20%27dynamics365-finops%27)&locale=en-us)

> [!NOTE]
> RSS-straumurinn skilar lista yfir 100 nýjustu uppfærslur á efnisatriðum. Listanum er ekki raðað eftir dagsetningu.  

Einnig er hægt að gerast áskrifandi að RSS-straumi með forriti:

- [Commerce](/api/search/rss?$filter=scopes%2fany(t%3A%20t%20eq%20%27dynamics365-commerce%27)&locale=en-us)  
- [Finance](/api/search/rss?$filter=scopes%2fany(t%3A%20t%20eq%20%27dynamics365-finance%27)&locale=en-us)  
- [Human Resources](/api/search/rss?$filter=scopes%2fany(t%3A%20t%20eq%20%27dynamics365-hr%27)&locale=en-us)  
- [Aðfangakeðja](/api/search/rss?$filter=scopes%2fany(t%3A%20t%20eq%20%27dynamics365-supplychain%27)&locale=en-us)  
- [Mannauður](/api/search/rss?$filter=scopes%2fany(t%3A%20t%20eq%20%27dynamics365-talent%27)&locale=en-us)  

### <a name="leave-us-feedback"></a>Skildu eftir ábendingu

Ef þú hefur athugasemdir eða spurningar um grein, skildu eftir athugasemd neðst á síðunni.

1. Veljið **Athugasemdir** til að sjá athugasemdir neðst á síðunni. Síðan skaltu velja **Framleiðslusvörun** eða **Skrá þig inn til að skrifa athugasemdir við fylgiskjöl**.

2. Byrjið að færa inn athugasemdir og smellið síðan á **Senda inn ábendingu**.

    ![Setja inn ummæli.](./media/feedback.png)

> [!NOTE]
> Ef senda á inn athugasemdir um fylgiskjöl þarf að skrá sig inn með GitHub-reikningi. Frekari upplýsingar er að finna í [Uppsetning og stjórnun GitHub-forstillingar](https://help.github.com/github/setting-up-and-managing-your-github-profile).

## <a name="contribute-to-the-documentation"></a>Veita framlag til fylgigagna

Þú getur lagt fram og gert breytingar á fylgiskjölum. Til að byrja skaltu velja **Breyta** hnappur (blýantartákn) á grein. Eftirfarandi myndband sýnir hvernig þú veitt framlag til fylgigagna okkar.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE36liB]

Myndbandið [Hvernig á að leggja sitt af mörkum til skjala Microsoft Dynamics 365](https://youtu.be/m5djioozRbg) (sýnt hér að ofan) er innifalið í rás Microsoft Dynamics 365 á YouTube.

Frekari upplýsingar er að finna á [Leiðbeiningar fyrir Docs-þátttakanda](/contribute), sem er birt af teyminu sem bjó til docs.microsoft.com vefsvæðið.

> [!NOTE]
> Við samþykkjum aðeins framlög á ensku efni okkar eins og stendur.

## <a name="task-guides"></a>Verkleiðbeiningar

Verkefnaleiðbeiningar eru stýrð, leiðbeind, gagnvirka reynslu sem fer með þig í gegnum þrep í verki eða viðskiptaferli. Hægt er að opna (spila) verkefnaleiðbeiningar úr **Hjálp** rúðunni. Þegar er verkefnaleiðbeiningar eru valdar í fyrsta skipti mun **hjálparsvæði** sýna nákvæmar leiðbeiningar fyrir verkið. Staðfærðar verkleiðbeiningar eru í boði.

Microsoft gaf út verkefnahandbókasöfn fyrir vöruútgáfur í desember 2017 útgáfunni af Dynamics 365 Finance and Operations. The [Aðgangur að verkefnaleiðbeiningum frá hjálparrúðunni](#accessing-task-guides-from-the-help-pane) kafla þessarar greinar útskýrir hvernig á að finna réttar verkefnaleiðbeiningar fyrir vöruna þína.

![Lesgluggi verkefnaleiðbeininga.](./media/task-guide-ops.png)

Til að byrja gagnvirka leiðsögn skal velja **Opna verkefnaleiðbeiningar** neðst á rúðunni **Hjálp**. Svartur bendill sýnir hvar á að fara fyrst. Fylgja skal leiðbeiningunum sem birtast í notendaviðmótinu og færa inn gögn samkvæmt leiðbeiningum.

![Fyrirmæli um skref í verkefnaleiðbeiningum.](./media/task-guide-step-1-ops.png)

> [!IMPORTANT]
> Gögn sem þú færir inn þegar verkefnaleiðbeiningar eru spilaðar eru raunveruleg. Ef unnið er í vinnsluumhverfi, verða gögn færð inn í fyrirtækinu sem verið er að nota þá stundina.

Hægt er að nota verkskráningu til að stofna eigin sérsniðnar verkefnaleiðbeiningar. Frekari upplýsingar eru í [Stofna fylgiskjöl eða þjálfun með verkskráningu](../../dev-itpro/user-interface/task-recorder-training-docs.md).

## <a name="in-product-help"></a>Hjálp innan vörunnar

Í sumum reitum eru lýsingar til að hjálpa notendum að opna þá, t.d. þegar þeir eru ekki vissir um hvaða gögn reiturinn inniheldur. Þar að auki býður svæðið **Hjálp** fyrir hverja vöru upp á samhengisaðgang að efni sem getur hjálpað notendum að komast í gang, opna atriði og fá frekari upplýsingar.

Velja skal hnappinn **Hjálp** (**?**) og síðan velja **Hjálp**. Einnig er hægt að ýta á **Ctrl+Shift+?**. Í báðum tilvikum opnast **Hjálparsvæði**. Í **Hjálp** er hægt að opna efnisatriði eða verkleiðbeiningar sem eiga við um reiti afurðarinnar sem notandi er staddur í.

![Hjálparsvæði.](./media/help-pane-ops-help.png)

### <a name="accessing-help-topics-from-the-help-pane"></a>Opna hjálparefni af hjálparsvæðinu

Á **hjálparsvæðinu** er hægt að opna efnisatriði sem eiga við biðlarann. Þegar þú opnar **Hjálp** svæðinu fyrstu sýnir flipinn **Hjálp** þér þær greinar sem eiga við um síðuna sem þú ert á. Ef engin efnisatriði finnast er hægt að færa inn leitarorð til þess að fínstilla leitina. Þegar þú velur grein í **Hjálp** gluggann er hann opnaður á nýjum flipa í vafranum þínum.

> [!IMPORTANT]
> Þessi hluti gildir ekki um Dynamics 365 Human Resources. Hjálparkerfið fyrir mannauðskerfið er sjálfkrafa tengt við verkleiðbeiningar fyrir afurðina. Einnig er ekki hægt að stofna sérsniðnar verkleiðbeiningar fyrir mannauðsstjóra.

### <a name="accessing-task-guides-from-the-help-pane"></a>Fara í verkefnaleiðbeiningar úr rúðunni Hjálp

Áður en hægt er að opna verkefnaleiðbeiningar á **hjálparsvæðinu** þarf kerfisstjóri að skilgreina nokkrar stillingar á síðunni **Kerfisfæribreytur** í fjármálum, Supply Chain Management eða viðskiptum. Frekari upplýsingar er að finna í [Verkefnaleiðbeiningum bætt við](help-connect.md#adding-task-guides).

<!-- > [!NOTE]
> - In order to configure Help, you must be signed in with an account in the same tenant as the tenant in which the app is deployed.
> - It is not possible to connect to an LCS library from an instance of the app running in a local virtual hard drive (VHD).

![System Parameters form with Help settings.](./media/system-parameters_ops-1024x437.png)

On the **System parameters** page, follow these steps:

1. **Important:** The first time that you open the Help tab, you must connect to Lifecycle Services. Be sure to select the link in the middle of the form, wait for the connection, close the dialog box, and then select **OK** to get to the parameters form.

    ![Connect to LCS.](./media/connect-to-lcs-crop-1024x365.png)

2. Select the Lifecycle Services project to connect to.
3. Select BPM libraries (within the selected project) to retrieve task recordings from.
4. Set the display order of the BPM libraries. This setting determines the order in which task recordings from the libraries will appear in the Help pane.-->

Eftir að kerfisstjóri hefur lokið við þessi skref, er hægt að opna **hjálparsvæðið** og velja flipann **Verkefnaleiðbeiningar**. Nú sérðu verkefnaleiðbeiningar sem eiga við um síðuna sem þú ert á. Ef engin verkefnaleiðbeiningar finnast er hægt að færa inn lykilorð til þess að fínstilla leitina. Eftir að smellt er á verkleiðbeiningar á svæðinu **Hjálp** sýnir **hjálparsvæðið** skref fyrir skref leiðbeiningar og hægt er að spila verkefnaleiðbeiningar.

![Lesgluggi verkefnaleiðbeininga.](./media/task-guide-ops.png)

### <a name="where-are-the-translated-task-guides-for-microsoft-libraries"></a>Hvar eru þýddu verkefnaleiðbeiningarnar fyrir Microsoft-söfn?

Þýddar Verkefnaleiðbeiningar eru útgefnar í söfnum sem hafa „Öll tungumál“ í titlinum. Tryggja þarf að tening við viðeigandi safn sé til staðar til að skoða þýdda verkleiðbeiningahjálp. Hver notandi getur breytt tungumálinu sem verkefnaleiðbeiningar birtast á með því að breyta tungumálastillingum undir **Valkostir** &gt; **Kjörstillingar**.

- Ef verkefnaleiðbeiningar hefur verið þýdd, þegar þú opnar þessi verkefnaleiðbeiningar birtist allan texta þeirra í valið tungumál.
- Ef verkleiðbeiningar hafa ekki enn verið þýddar birtist aðeins texti stjórntækja á völdu tungumáli þegar þær eru opnaðar.

## <a name="creating-custom-help"></a>Stofnun sérsniðinnar hjálpar

Hægt er að stofna hjálp fyrir notendur með því að stofna sérsniðnar verkefnaleiðbeiningar eða tengja eigið vefsvæði við svæðið **Hjálp**. Frekari upplýsingar er hægt að finna í eftirfarandi efni:

- [Tilföng verkskráningar](../../dev-itpro/user-interface/task-recorder.md)
- [Sérsniðið hjálparyfirlit](../../dev-itpro/help/custom-help-overview.md)

## <a name="additional-resources"></a>Frekari upplýsingar

Í eftirfarandi töflu er listi yfir vefsíður okkar. Svæði sem hafa stjörnu (\*) við nafnið krefjast innskráningu með því að nota reikning sem tengist þjónustuáætlun.

| Svæði | lýsing |
|------|-------------|
| [Docs.microsoft.com](/dynamics365/) | Þetta vefsvæði hýsir eða tengir í fylgiskjöl afurðar fyrir Dynamics 365. |
| [Microsoft Learn](/learn/) | Þetta vefsvæði er ókeypis Microsoft netnámskeiðssvæði. |
| [Microsoft DynamicsLifecycle Services (LCS)](https://lcs.dynamics.com/)\* | Þetta vefsvæði veitir sameiginlegt vinnusvæði í skýi sem viðskiptaaðilar og viðskiptavinir geta notað til að stjórna verkum úr aðgerðum forsölu og framkvæmdar. Þetta er gagnlegt í öllum áföngum framkvæmdar. |
| [Stuðningsblogg](https://aka.ms/AXSupportBlog) | Þetta vefsvæði veitir ábendingar og tækni sem eru skrifaðar inn af þjónustuveri. |
| [Docs.microsoft.com/fyrri útgáfur](/previous-versions/dynamics/) | Þetta vefsvæði hýsir efni frá fyrri útgáfum. |
| [Samfélag Dynamics](https://community.dynamics.com/) | Þetta vefsvæði hýsir umræðuþræði, blogg og myndskeið. |
| [Microsoft.com/dynamics365](https://www.microsoft.com/dynamics365/home) | Þetta vefsvæði veitir upplýsingar um mat og sölu. |




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

