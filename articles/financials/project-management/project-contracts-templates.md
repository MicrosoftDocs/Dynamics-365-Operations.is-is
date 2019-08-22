---
title: Samstilla verksamninga og verk beint frá Project Service Automation við Finance and Operations
description: Þetta efnisatriði fjallar um sniðmát og undirliggjandi verkefni sem notuð eru til að samstilla verksamninga og verk beint frá Microsoft Dynamics 365 for Project Service Automation til Microsoft Dynamics 365 for Finance and Operations.
author: KimANelson
manager: AnnBe
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: be23b99ddc224328cf067fe0bf36be93fcef4337
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846035"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance-and-operations"></a>Samstilla verksamninga og verk beint frá Project Service Automation við Finance and Operations

[!include[banner](../includes/banner.md)]

Þetta efnisatriði fjallar um sniðmát og undirliggjandi verkefni sem notuð eru til að samstilla verksamninga og verk beint frá Microsoft Dynamics 365 for Project Service Automation til Microsoft Dynamics 365 for Finance and Operations.

> [!NOTE] 
> Ef þú notar Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 7.3.0, verður þú að setja upp KB 4074835.

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Gagnaflæði fyrir Project Service Automation til Finance and Operations

> [!NOTE]
> Áður en þú getur notað samþættingarlausn Project Service Automation við Finance and Operations ættir þú að hafa kynnst eiginleika gagnasamþættingar fyrir Microsoft Dynamics 365.

Samþættingarlausn Project Service Automation við Finance and Operations notar eiginleika gagnasamþættingar til að samstilla gögn þvert yfir tilvik af Project Service Automation og Finance and Operations. Samþættingarsniðmátið sem er tiltækt með eiginleika gagnasamþættingar gerir gögnum kleift að flæða varðandi verksamninga, verk, verksamningslínur og áföngum verksamningslína frá Project Service Automation til Finance and Operations.

Eftirfarandi skýringarmynd sýnir hvernig gögnin eru samstillt milli Project Service Automation og Finance and Operations.

[![Gagnaflæði fyrir samþættingu Project Service Automation við Finance and Operations](./media/ProjectsAndContractsFlow.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>Sniðmát og verkefni

Til að fá aðgang að tiltækum sniðmátum, í stjórnendamiðstöð Microsoft PowerApps, skal velja **Verk** og síðan í efra hægra horninu skal velja **Nýtt verk** til að velja almenn sniðmát.

Eftirfarandi sniðmát og undirliggjandi verkefni eru notuð til að samstilla verksamninga og verk frá Project Service Automation til Finance and Operations:

- **Heiti sniðmátsins í gagnasamþættingu:** Verk og samningar (PSA til Fin and Ops)
- **Heiti verkefna í verkinu:**

    - Verksamningar PSA til Fin og Ops
    - Verk PSA til Fin and Ops
    - Verksamningslínur PSA til Fin and Ops
    - Áfangar verksamningslína PSA til Fin and Ops

Áður en samstilling verksamninga og verka getur átt sér stað verður þú að samstilla lykla.

## <a name="entity-set"></a>Einingastamstæða

| Project Service Automation       | Finance and Operations                                 |
|----------------------------------|--------------------------------------------------------|
| Pantanir                           | Samþættingareining fyrir verksamning                |
| Verk                         | Einingarsamþætting fyrir verk                         |
| Pantanalínur                      | Samþættingareining fyrir verksamningslínu           |
| Áfangar verksamningslína | Samþættingareining fyrir þáttaskil verksamningslínu. |

## <a name="entity-flow"></a>Einingaflæði

Verksamningum er stjórnað í Project Service Automation og þeir eru samstilltir við Finance and Operations sem verksamningar. Sem hluti af samþættingarsniðmátinu er hægt að stilla samþættingarupprunann í Finance and Operations fyrir verksamninginn.

Tíma og efnisverkum og föstum samningsverðum er stjórnað í Project Service Automation og þau eru samstillt við Finance and Operations sem verk. Sem hluti af sniðmátssamþættingunni er hægt að stilla samþættingarupprunann í Finance and Operations fyrir verkið.

Verksamningslínum er stjórnað í Project Service Automation og þær eru samstilltar við Finance and Operations sem reikningsreglur verksamnings. Ef reikningsaðferðin er frábrugðin sjálfgefinni verkgerð mun samstillingin uppfæra verkgerðina fyrir samningslínuverkið og verkflokkinn.

Áföngum verksamningslína er stjórnað í Project Service Automation og þær eru samstilltar við Finance and Operations sem reikningsreglur verksamnings.

## <a name="project-service-automation-to-finance-and-operations-integration-solution"></a>Samþættingarlausn Project Service Automation við Finance and Operations

Reiturinn **Kenni verksamnings** er í boði á síðunni **Verksamningar**. Þessi reitur hefur verið gerður að einkvæmum lykli til að styðja við samþættinguna.

Þegar nýr verksamningur hefur verið búinn til, ef gildið fyrir **kenni verksamnings** er ekki þegar til, myndast það sjálfkrafa með því að nota númeraröð. Gildið samanstendur af **ORD** fylgt eftir með stigvaxandi númeraröð og síðan viðskeyti með sex stöfum. Hér er dæmi: **ORD-01022-Z4M9Q0**.

Reiturinn **Verknúmer** er að finna á síðunni **Verk**. Þessi reitur hefur verið gerður að einkvæmum lykli til að styðja við samþættinguna.

Þegar nýtt verk hefur verið búið til, ef gildið fyrir **Verknúmer** er ekki þegar til, myndast það sjálfkrafa með því að nota númeraröð. Gildið samanstendur af **PRJ** fylgt eftir með stigvaxandi númeraröð og síðan viðskeyti með sex stöfum. Hér er dæmi: **PRJ-01049-CCNID0**.

Þegar samþættingarlausn Project Service Automation við Finance and Operations er notuð<TO DO: link in the top level document link where we will be adding the instructions for applying the PSA solution>, stillir uppfærsluforskrift reitinn **Kenni verksamnings** fyrir núverandi verksamninga og reitinn **Verknúmer** fyrir núverandi verk í Project Service Automation.

## <a name="prerequisites-and-mapping-setup"></a>Skilyrði og vörpunaruppsetning

- Áður en samstilling verksamninga og verka getur átt sér stað verður þú að samstilla lykla.
- Í tengistillingu skal bæta við reitarvörpun samþættingarlykils fyrir **msdyn\_fyrirtækjaeiningar** til **msdyn\_heiti \[Heiti\]**. Þú gætir fyrst þurft að bæta verkefni við tengistillinguna. Nánari upplýsingar er að finna í [Sameina gögn í Common Data Service fyrir forrit](https://docs.microsoft.com/powerapps/administrator/data-integrator).
- Í tengistillingunni þinni skaltu bæta við reitarvörpun samþættingarlykils fyrir **msdyn\_verk** til **msdynce\_verknúmer \[Verknúmer\]**. Þú gætir fyrst þurft að bæta verkefni við tengistillinguna. Nánari upplýsingar er að finna í [Sameina gögn í Common Data Service fyrir forrit](https://docs.microsoft.com/powerapps/administrator/data-integrator).
- **SourceDataID** fyrir verksamninga og verk má uppfæra í annað gildi eða fjarlægja úr vörpuninni. Sjálfgefið sniðmátsgildi er **Project Service Automation**.
- Vörpunin **PaymentTerms** verður að vera uppfærð þannig að hún endurspegli gilda greiðsluskilmála í Finance and Operations. Þú getur einnig fjarlægt vörpunina úr verkefni verks. Sjálfgefið gildi vörpunar hefur sjálfgefin gildi fyrir sýnigögn. Eftirfarandi tafla sýnir gildin í Project Service Automation.

    | Virði | lýsing   |
    |-------|---------------|
    | 1     | Net 30        |
    | 2     | 2% 10, Net 30 |
    | 3     | Net 45        |
    | 4     | Net 60        |

## <a name="power-query"></a>Power Query

Þú verður að nota Microsoft Power Query fyrir Excel til að sía gögn ef eftirfarandi skilyrði eru uppfyllt:

- Þú hefur sölupantanir í Microsoft Dynamics 365 for Sales.
- Þú ert með margar fyrirtækjaeiningar í Project Service Automation og þessum fyrirtækjaeiningum verður varpað í marga lögaðila í Finance and Operations.

Ef þú verður að nota Power Query skaltu fylgja þessum leiðbeiningum:

- Sniðmát verksamninga (PSA til Fin and Ops) hefur sjálfgefna síu sem inniheldur aðeins sölupantanir af gerðinni **Vinnuliður (msdyn\_ordertype = 192350001)**. Þessi sía hjálpar til við að tryggja að verksamningar séu ekki búnir til fyrir sölupantanir í Finance and Operations. Ef þú býrð til þitt eigið sniðmát þarftu að bæta við þessari síu.
- Þú verður að búa til Power Query síu sem inniheldur aðeins fyrirtækjasamninga sem ætti að samstilla við lögaðila af tengistillingu samþættingar. Til dæmis ættu verksamningar sem þú hefur með einingu fyrirtækjasamnings fyrir Contoso US að vera samstilltir við USSI lögaðilann en verksamningar sem þú hefur með einingu samningsfyrirtækis Contoso Global ætti að vera samstillt við USMF lögaðilann. Ef þú bætir ekki þessari síu við vörpun verkefnis verða allir verksamningar samstilltir við lögaðilann sem er skilgreindur fyrir tengistillinguna, óháð samningi fyrirtækjaeiningar.

## <a name="template-mapping-in-data-integration"></a>Sniðmátsvörpun í Gagnasamþættingu

> [!NOTE] 
> Reitirnir **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState** og **AddressZipCode** eru ekki teknir með í sjálfgefinni vörpun fyrir verksamninga. Þú getur bætt við vörpunum ef það er nauðsynlegt að þessi gögn séu samstillt fyrir verksamninga.
>
> Reitirnir **Lýsing**, **ParentID** , **ProjectGroup** , **ProjectManagerPersonnelNumber**, og **ProjectType** eru ekki teknir með í sjálfgefna vörpun fyrir verk. Þú getur bætt við vörpunum ef það er nauðsynlegt að þessi gögn séu samstillt fyrir verk.

Eftirfarandi skýringarmyndir sýna dæmi um vörpunarsniðmát í gagnasamþættingu. Vörpunin sýnir reitaupplýsingarnar sem verða samstilltar frá Project Service Automation við Finance and Operations.

[![Kortlagning sniðmáts](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![Kortlagning sniðmáts](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![Kortlagning sniðmáts](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![Kortlagning sniðmáts](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)
