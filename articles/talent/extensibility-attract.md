---
title: Stækkunarhæfni í Attract
description: Þetta efnisatriði lýsir því hvernig þú getur stækkað Microsoft Dynamics 365 for Talent - Attract-forritið með því að nota Microsoft Power platform.
author: andreabichsel
manager: AnnBe
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 9360ac52bd53dc473ca61a424f3be933bcf357d1
ms.sourcegitcommit: ef08bf1258aefb525d56bf85ef19311be26ab94c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/30/2019
ms.locfileid: "1795221"
---
# <a name="extensibility-in-attract"></a>Stækkunarhæfni í Attract

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Talent er byggt ofan á Common Data Service verkvanginn og hægt er að stækka það með ýmsum hætti með því að nota Microsoft Power Platform og eiginleika sem Common Data Service býður upp á. Þar af leiðandi er hægt að grunnstilla og sérsníða kerfið með því að nota Microsoft PowerApps og Microsoft Flow. Þú getur einnig fengið frekari greiningar um fólk með því að nota Microsoft Power BI. Ennfremur gera nýjar sérsniðnar aðgerðir, svo sem aðgerðir PowerApps og Web Content (Iframe), ráðningarferlið meira aðlagað en nokkru sinni fyrr. Með því að nota þessar aðgerðir getur þú sérsniðið ráðningarferlið við viðskiptaþarfir þínar og ferli fyrirtækisins og getur tryggt að bæði ráðningarteymið og umsækjendur hafi óaðfinnanlega sérsniðna upplifun.

## <a name="extending-option-sets-in-attract"></a>Safn valkosta fyrir stækkunarhæfni í Attract

**Safn valkosta** (tínslulisti) er gerð svæðis sem hægt er að hafa með í einingu. Það skilgreinir safn valkosta. Þegar safn valkosta birtist í skjámynd notar það stýringu fellilista.  Í Attract eru mörg svæði sem eru söfn valkosta.  Við erum farin að kynna möguleikann á því að stækka söfn valkosta, fyrst reitinn fyrir ástæðu höfnunar, reitinn fyrir starfsgerð og reitinn fyrir gerð starfsaldurs.   Einnig er hægt að bæta við staðfærðum birtingarmerkjum fyrir þá valkosti sem þú bætir við. Nánari upplýsingar eru í [Sérstilla merki fyrir söfn valkosta](https://docs.microsoft.com/powerapps/developer/common-data-service/customize-labels-support-multiple-languages).

> [!NOTE]
> Virknin fyrir auglýsingu starfs á LinkedIn krefst notkunar á reitunum **Starfsgerð** og **Starfsaldursgerð** á síðunni **Upplýsingar um starf**. Sjálfgefin gildi í þessum reitum eru studd af LinkedIn og birtast þegar starfið er auglýst. Ef þú ert þar af leiðandi að auglýsa störf á LinkedIn og þú breytir núverandi gildum á safni valkosta fyrir þessi svæði, mun starfið samt birtast en LinkedIn mun ekki sýna sérstilltu gildin **Starfsgerð** og **Starfsaldursgerð**.  

Hér fyrir neðan eru leiðbeiningar um uppfærslu á svæðinu **Ástæða fyrir höfnun** með gildum sem eru tiltekin fyrir reksturinn þinn.  

1. Til að stækka safn valkosta fyrir **Ástæða fyrir höfnun** skal fara á [Vefsvæði fyrir stjórnanda PowerApps](https://admin.powerapps.com).
2. Þú verður hugsanlega beðin/n um að skrá þig inn á reikninginn þinn. Gefðu upp notandakennið þitt og aðgangsorð sem þú notar til að skrá þig inn í Dynamics365 og/eða Office365, og smelltu síðan á **Næsta**.
3. Í flipanum **Umhverfi** skal velja umhverfið sem á að stjórna og tvísmella til að komast í flipann **Upplýsingar**.
4. Í flipanum **Upplýsingar** skal velja **Stjórnunarmiðstöð Dynamics 365**.
5. Veljið tilvikið sem á að breyta og veljið **Opna**.
6. Farið í **Stillingar** og síðan **Sérstillingar** og veljið **Sérstilla kerfið**.
7. Finnið eininguna sem á að stækka safn valkosta fyrir með því að velja **Einingar** og stækka flokkinn. Í þessu dæmi yrði það **Eining starfsumsóknar**.
8. Farið á svæðið sem á stækka safn valkosta fyrir með því að velja valkostinn **Svæði**. Í þessu dæmi yrði það **msdyn_rejectionreason**. Tvísmelltu á svæðið.
9. Í svæðinu **Safn valkosta** skal velja **Breyta**.
10. Veldu **+** táknið.
11. Sláðu inn **Merki**.  (Þetta verður að vera einkvæmt gildi - ekki afrit).
12. Veljið **Vista**.
13. Veljið **Gefa út** efst á síðunni.

## <a name="take-advantage-of-the-microsoft-power-platform"></a>Nýttu þér Microsoft Power Platform 

Vegna þess að öll gögnin frá Attract eru geymd í Common Data Service getur þú notað verkfæri frá Microsoft Power Platform til að laga Attract að sértækum viðskiptaþörfum þínum.

### <a name="powerapps"></a>PowerApps

Þú getur notað PowerApps til að byggja upp forrit á auðveldan hátt sem tengjast Attract-gögnum þínum og nota tjáningu eins og tjáningarnar í Microsoft Excel til að bæta við rökum. Forrit sem þú byggir með því að nota PowerApps geta keyrt á vefnum og á Apple iOS og Google Android tækjum.

Til dæmis er hægt að gera kynningarfundi háskóla auðveldara fyrir ráðningaraðila með því að byggja upp lítið forrit sem gerir þeim kleift að skanna ferilskrár og mata umsækjendur á störfum í Attract. Einnig er hægt að byggja upp forrit sem hjálpar til við að uppfylla nauðsynlega reglufylgni fyrirtækisins þíns. Nánari upplýsingar um PowerApps og hvernig á að nota það til að byggja upp forrit er að finna í [Sameina gögn í Common Data Service](https://docs.microsoft.com/powerapps).

### <a name="microsoft-flow"></a>Microsoft Flow 

Þú getur notað Microsoft Flow til að búa til sjálfvirkan vinnuflæði sem keyrir ofan á Attract-gögnum. Þú getur auðveldlega tengst hundruðum vinsælra forrita og þjónustu án þess að þurfa að skrifa kóða. Með því að byggja upp flæði sem hafa samskipti við Attract Job, umsækjendur og umsóknareiningar í Common Data Service, geturðu gert ýmsar aðgerðir sjálfvirkar. Til dæmis, þegar frambjóðandi samþykkir tilboð, getur tilkynning verið sendur til þjálfunarteymisins eða fréttirnar geta verið tilkynntar á Twitter. Nánari upplýsingar um flæði er að finna í [Microsoft Flow fylgiskjölunum](https://docs.microsoft.com/flow/).

### <a name="power-bi"></a>Power BI

Power BI gerir þér kleift að byggja upp og skoða sérsniðnar skýrslur og yfirlit sem gefa þér dýpri innsýn í Attract-gögnin þín. Nánari upplýsingar um Power BI og hvernig á að búa til gagnvirkar skýrslur og yfirlit að finna í [Power BI-fylgigögnunum](https://docs.microsoft.com/power-bi/).

### <a name="custom-activities"></a>Sérsniðnir verkþættir 

Þú getur bætt við sérsniðnum aðgerðum, svo sem aðgerðum PowerApps-forrita og vefefnis (iframe), á stigi sniðmáts starfsferlisins eða meðan þú býrð til nýtt starf. Þessar aðgerðir gera þér kleift að sérsníða ráðningarferlið og koma með viðskiptagrunn sem er einstakt fyrir fyrirtæki þitt í Attract.

#### <a name="powerapps-activity"></a>PowerApps-aðgerð 

PowerApps-virkni leyfir stofnendum sniðmáta fyrir starf eða starfsferil að fella inn í PowerApps-forrit í ráðningarflæðinu. Eftir að þú hefur búið til og birta forritið getur þú slegið inn forritakenni þess í aðgerðarstillingunum. Með því að nota PowerApps-forrit geturðu lesið og skrifað gögn í Common Data Service. Þú getur jafnvel tengt forritið við flæði. Til dæmis hefur þú forrit sem ráðningaraðilar nota til að fylla út eyðublað meðan þeir halda starfsviðtal í síma. Í þessu tilfelli er hægt að tengja forritið við flæði sem metur hvort umsækjandi geti farið lengra í starfsumsóknarferlinu. Þessi tegund af aðgerðar má aðeins skoða af meðlimum ráðningarhópsins. Nánari upplýsingar um hvernig á að stilla PowerApps virkni er að finna í [Aðgerðir í Attract](./activities-attract.md).

> [!NOTE]
> PowerApps-aðgerðin er aðeins í boði með Viðbót við alhliða ráðningar.

#### <a name="web-content-iframe-activity"></a>Vefefni (iframe) virkni

Vefefni (iframe) virkni gerir þér kleift að fella inn sérsniðna veflausn sem þú hefur byggt upp í ráðningarferlinu eða í vefgátt umsækjanda. Þú getur lesið og skrifað gögn beint úr Common Data Service. Þú getur einnig sérsniðið lausnina þannig að það kalli fram flæði eða nýtir Microsoft Azure-eiginleika. Nánari upplýsingar um hvernig á að stilla virkni vefefnis sjá [Aðgerðir í Attract](./activities-attract.md).

> [!NOTE]
> Vefefnisaðgerðin er aðeins í boði með Viðbót við alhliða ráðningar.
