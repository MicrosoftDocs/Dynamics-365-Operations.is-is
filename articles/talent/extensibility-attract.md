---
title: "Stækkunarhæfni í Attract"
description: "Þetta efnisatriði lýsir því hvernig þú getur stækkað Microsoft Dynamics 365 for Talent - Attract-forritið með því að nota Microsoft Power platform."
author: josaw
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: 0af60a0aea0f7a5de793631445aaebb37dbb0d74
ms.contentlocale: is-is
ms.lasthandoff: 10/22/2018

---

# <a name="extensibility-in-attract"></a>Stækkunarhæfni í Attract

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Talent er byggð ofan á Common Data Service (CDS) fyrir Apps-verkvanginn og hægt er að stækka það með ýmsum hætti með því að nota Microsoft Power Platform og eiginleika sem Common Data Service for Apps býður upp á. Þar af leiðandi er hægt að grunnstilla og sérsníða kerfið með því að nota Microsoft PowerApps og Microsoft Flow. Þú getur einnig fengið frekari greiningar um fólk með því að nota Microsoft Power BI. Ennfremur gera nýjar sérsniðnar aðgerðir, svo sem aðgerðir PowerApps og Web Content (Iframe), ráðningarferlið meira aðlagað en nokkru sinni fyrr. Með því að nota þessar aðgerðir getur þú sérsniðið ráðningarferlið við viðskiptaþarfir þínar og ferli fyrirtækisins og getur tryggt að bæði ráðningarteymið og umsækjendur hafi óaðfinnanlega sérsniðna upplifun.

## <a name="take-advantage-of-the-microsoft-power-platform"></a>Nýttu þér Microsoft Power Platform 

Vegna þess að öll gögnin frá Attract eru geymd í Common Data Service for Apps, getur þú notað verkfæri frá Microsoft Power Platform til að laga Attract að sértækum viðskiptaþörfum þínum.

### <a name="powerapps"></a>PowerApps

Þú getur notað PowerApps til að byggja upp forrit á auðveldan hátt sem tengjast Attract-gögnum þínum og nota tjáningu eins og tjáningarnar í Microsoft Excel til að bæta við rökum. Forrit sem þú byggir með því að nota PowerApps geta keyrt á vefnum og á Apple iOS og Google Android tækjum.

Til dæmis er hægt að gera kynningarfundi háskóla auðveldara fyrir ráðningaraðila með því að byggja upp lítið forrit sem gerir þeim kleift að skanna ferilskrár og mata umsækjendur á störfum í Attract. Einnig er hægt að byggja upp forrit sem hjálpar til við að uppfylla nauðsynlega reglufylgni fyrirtækisins þíns. Nánari upplýsingar um PowerApps og hvernig á að nota það til að byggja upp forrit er að finna í [Sameina gögn í Common Data Service fyrir forrit](https://docs.microsoft.com/en-us/powerapps).

### <a name="microsoft-flow"></a>Microsoft Flow 

Þú getur notað Microsoft Flow til að búa til sjálfvirkan vinnuflæði sem keyrir ofan á Attract-gögnum. Þú getur auðveldlega tengst hundruðum vinsælra forrita og þjónustu án þess að þurfa að skrifa kóða. Með því að byggja upp flæði sem hafa samskipti við Attract Job, umsækjendur og umsóknareiningar í Common Data Service for Apps, geturðu gert ýmsar aðgerðir sjálfvirkar. Til dæmis, þegar frambjóðandi samþykkir tilboð, getur tilkynning verið sendur til þjálfunarteymisins eða fréttirnar geta verið tilkynntar á Twitter. Nánari upplýsingar um flæði er að finna í [Microsoft Flow fylgiskjölunum](https://docs.microsoft.com/en-us/flow/).

### <a name="power-bi"></a>Power BI

Power BI gerir þér kleift að byggja upp og skoða sérsniðnar skýrslur og yfirlit sem gefa þér dýpri innsýn í Attract-gögnin þín. Nánari upplýsingar um Power BI og hvernig á að búa til gagnvirkar skýrslur og yfirlit að finna í [Power BI-fylgigögnunum](https://docs.microsoft.com/en-us/power-bi/).

### <a name="custom-activities"></a>Sérsniðnir verkþættir 

Þú getur bætt við sérsniðnum aðgerðum, svo sem aðgerðum PowerApps-forrita og vefefnis (iframe), á stigi sniðmáts starfsferlisins eða meðan þú býrð til nýtt starf. Þessar aðgerðir gera þér kleift að sérsníða ráðningarferlið og koma með viðskiptagrunn sem er einstakt fyrir fyrirtæki þitt í Attract.

#### <a name="powerapps-activity"></a>PowerApps-aðgerð 

PowerApps-virkni leyfir stofnendum sniðmáta fyrir starf eða starfsferil að fella inn í PowerApps-forrit í ráðningarflæðinu. Eftir að þú hefur búið til og birta forritið getur þú slegið inn forritakenni þess í aðgerðarstillingunum. Með því að nota PowerApps-forrit geturðu lesið og skrifað gögn í Common Data Service for Apps. Þú getur jafnvel tengt forritið við flæði. Til dæmis hefur þú forrit sem ráðningaraðilar nota til að fylla út eyðublað meðan þeir halda starfsviðtal í síma. Í þessu tilfelli er hægt að tengja forritið við flæði sem metur hvort umsækjandi geti farið lengra í starfsumsóknarferlinu. Þessi tegund af aðgerðar má aðeins skoða af meðlimum ráðningarhópsins. Nánari upplýsingar um hvernig á að stilla PowerApps virkni er að finna í [Aðgerðir í Attract](./activities-attract.md).

> [!NOTE]
> PowerApps-aðgerðin er aðeins í boði með Viðbót við alhliða ráðningar.

#### <a name="web-content-iframe-activity"></a>Vefefni (iframe) virkni

Vefefni (iframe) virkni gerir þér kleift að fella inn sérsniðna veflausn sem þú hefur byggt upp í ráðningarferlinu eða í vefgátt umsækjanda. Þú getur lesið og skrifað gögn beint úr Common Data Service for Apps. Þú getur einnig sérsniðið lausnina þannig að það kalli fram flæði eða nýtir Microsoft Azure-eiginleika. Nánari upplýsingar um hvernig á að stilla virkni vefefnis sjá [Aðgerðir í Attract](./activities-attract.md).

> [!NOTE]
> Vefefnisaðgerðin er aðeins í boði með Viðbót við alhliða ráðningar.

