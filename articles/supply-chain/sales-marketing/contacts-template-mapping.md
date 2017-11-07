---
title: "Samstilla tengiliði frá Sales til tengiliða eða viðskiptavina í Finance and Operations"
description: "Þetta efnisatriði fjallar um sniðmát og undirliggjandi verkefni sem notuð eru til að samstilla Tengilið (Tengiliðir) og Tengilið (Viðskiptavinir) úr Microsoft Dynamics 365 for Sales í Microsoft Dynamics 365 for Finance and Operations, Enterprise útgáfu."
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: 41e27776b94df059ada13efb9a3dbf6a29d67f36
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="synchronize-contacts-from-sales-to-contacts-or-customers-in-finance-and-operations"></a>Samstilla tengiliði frá Sales til tengiliða eða viðskiptavina í Finance and Operations

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Áður en þú getur notað lausnina Prospect to cash þarftu að kynna þér [Dynamics 365 gagnasamþættingu](/common-data-service/entity-reference/dynamics-365-integration). 

Þetta efnisatriði fjallar um sniðmát og undirliggjandi verkefni sem notuð eru til að samstilla Tengiliðseiningar (Tengiliðir) og Tengilið (Viðskiptavinir) úr Microsoft Dynamics 365 for Sales (Sales) í Microsoft Dynamics 365 for Finance and Operations, Enterprise útgáfu (Finance and Operations).

## <a name="templates-and-tasks"></a>Sniðmát og verkefni

Eftirfarandi sniðmát og undirliggjandi verkefni eru notuð til að samstilla Tengilið (Tengiliðir) í Sales við Tengilið (Viðskiptavinir) í Finance and Operations:

- **Heiti sniðmátanna:**

    - Tengiliðir (Sales við Fin and Ops)
    - Tengiliðir við Viðskiptavin (Sales við Fin and Ops)

- **Heiti verkefnanna í verkinu:**

    - Tengiliðir
    - ContactToCustomer

Eftirfarandi samstilliningarverkefni er nauðsynlegt fyrir samstilingu Tengiliðar: Lyklar (Sales við Fin and Ops)

## <a name="entity-sets"></a>Einingastamstæður

| Sala    | CDS     | Finance and Operations |
|----------|---------|------------------------|
| Tengiliðir | Tengiliður | Tengiliðir fyrir skuldatryggingu           |
| Tengiliðir | Lykill | Viðskiptavinir V2           |

## <a name="entity-flow"></a>Einingaflæði

Tengiliðum er stjórnað í Sales og samstilltir við Common Data Service (CDS) og Finance and Operations.

Tengiliður í Sales getur orðið Tengiliður í CDS og Finance and Operations. Hinn kosturinn er að verða Lykill í CDS og Viðskiptavinur í Finance and Operations. Til að ákvarða hvort tengliður ætti að vera tekinn úr Sales fyrir samstillingu við CDS og Finance and Operations (til dæmis Tengiliðir í Sales &gt; Tengiliður í CDS &gt; Tengliðir í Finance and Operations) leitar kerfið að eftirfarandi eiginleikum Tengiliðar í Sales:

- **Samstilla við Lykil í CDS og Viðskiptavin í Finance and Operations:** Tengiliðir þar sem **Er virkur viðskiptavinur** er stillt á **Já**
- **Samstilla við Tengilið í CDS og Tengilið í Finance and Operations:** Tengiliðir þar sem **Er virkur viðskiptavinur** er stillt á **Nei** og **Fyrirtæki** (Yfirlykill/Tengiliður) bendir á Lykil (ekki Tengilið)

## <a name="prospect-to-cash-solution-for-sales"></a>Prospect to cash lausn fyrir Sales 

Nýjum **Er virkur viðskiptavinur** reit hefur verið bætt við Tengiliðinn. Þessi reitur er notaður til að greina á milli Tengiliða sem hafa söluvirkni og Tengiliða sem hafa ekki söluvirkni. **Er virkur viðskiptavinur** er aðeins stillt á **Já** fyrir Tengiliði sem hafa tengd tilboð, pantanir eða reikninga. Aðeins þeir Tengiliðir eru samstillir við Finance and Operations sem Viðskiptavinir.

Nýjum **IsCompanyAnAccount** reit hefur verið bætt við Tengiliðinn. Þessi reitur er notaður til að gefa til kynna hvort Tengiliður er tengdur við Fyrirtæki (Yfirlykil/Tengilið) af gerðinni **Lykill**. Þessar upplýsingar eru notaðar til að auðkenna Tengiliði sem samstilla á við Finance and Operations sem Tengiliði.

Nýjum reit fyrir **Númer Tengiliðar** hefur verið bætt við Tengiliðinn til að tryggja einkvæman raunlykil fyrir samþættinguna. Þegar nýr Tengiliður er stofnaður verður gildið **Númer tengiliðar** sjálfkrafa til með því að nota númeraröð. Gildið samanstendur af **CON**, því næst hækkandi talnaröð og svo sex stafa viðskeyti. Hér er dæmi: **CON-01000-BVRCPS**

Þegar samþættingarlausninni fyrir Sales er bætt við Sales stillir uppfærsluforskrift reitinn **Númer tengiliðar** fyrir Tengiliði sem fyrir eru með því að nota talnaröðina sem var nefnd áður. Uppfærsluforskriftin stillir líka reitinn **Er virkur viðskiptavinur** á **Já** fyrir alla Tengiliði með söluvirkni.

## <a name="in-finance-and-operations"></a>Í Finance and Operations 

Tengiliðir eru merktir með eiginleikanum **IsContactPersonExternallyMaintained**. Þessi eiginleiki gefur til kynna að tilteknum Tengilið sé stjórnað utan frá. Í þessu tilfelli er Tengiliðum sem er stjórnað utan frá stjórnað í Sales.

## <a name="preconditions-and-mapping-setup"></a>Skilyrði og vörpunaruppsetning

### <a name="contact-to-contact"></a>Frá Tengilið til Tengiliðs

- Uppfærðu **CDS-fyrirtækjaauðkenni** í **Uppruna &gt; CDS** vörpun.

    - Sjálfgefið sniðmátsgildi fyrir **Organization_OrganizationId [Fyrirtækjaauðkenni]** er **ORG001**.
    - Sjálfgefið sniðmátsgildi fyrir **PrimaryAccount_Organization_OrganizationId [Fyrirtækjaauðkenni]** er **ORG001**.

- **Svæðiskóði fyrir aðsetursland** er nauðsynlegur í Finance and Operations. Til að koma í veg fyrir samstillingarvillur er hægt að tilgreina sjálfgefið gildi í vörpununum **CDS &gt; Aðgerðir**. Sjálfgefna gildið er svo notaðu ef reiturinn er skilinn eftir auður í Sales. Sjálfgefið sniðmátsgildi fyrir **PrimaryAddressCountryRegionISOCode** er **USA**.
- Gakktu úr skugga um að gildi fyrir eftirfarandi reiti séu til staðar í Finance and Operations. Ef upplýsingarnar eru ekki nauðsynlegar í Finance and Operations er hægt að fjarlægja vörpunina úr vörpununum **CDS &gt; Ákvörðunarstaður**.

    - **Heiti reits í Finance and Operations::** Ákvörðun
    - **Vörpun:** PrimaryAccountRole = DecisionMakingRole

### <a name="contact-to-customer"></a>Frá Tengilið til Viðskiptavinar

- Uppfærðu **CDS-fyrirtækjaauðkenni** í **Uppruna &gt; CDS** vörpun. Sjálfgefið sniðmátsgildi fyrir **Organization_OrganizationId [Fyrirtækjaauðkenni]** er **ORG001**.
- **Svæðiskóði fyrir aðsetursland** er nauðsynlegur í Finance and Operations. Til að koma í veg fyrir samstillingarvillur er hægt að tilgreina sjálfgefið gildi í vörpununum **CDS &gt; Ákvörðunarstaður**. Sjálfgefna gildið er svo notaðu ef reiturinn er skilinn eftir auður í Sales. Sjálfgefið sniðmátsgildi fyrir **PrimaryAddressCountryRegionISOCode** er **USA**.
- **CustomerGroup** er nauðsynlegt í Finance and Operations. Til að koma í veg fyrir samstillingarvillur er hægt að tilgreina sjálfgefið gildi í vörpununum **CDS &gt; Ákvörðunarstaður**. Sjálfgefna gildið er svo notaðu ef reiturinn er skilinn eftir auður í Sales. Sjálfgefið sniðmátsgildi fyrir **CustomerGroupId** er **10**.
- Með því að bæta eftirfarandi vörpunum úr **CDS &gt; Ákvörðunarstað** geturðu dregið úr fjölda handvirkra uppfærslna í Finance and Operations. Hægt er að nota sjálfgefið gildi eða gildisvörpun frá til dæmis **Land/Svæði** eða **Borg**.

    - **SiteId** - Einnig er hægt að skilgreina sjálfgefið svæði fyrir vörur í inance and Operations. Svæði er nauðsynlegt til að búa til tilboð og sölupantanir í Finance and Operations. Sniðmátsgildi fyrir **SiteId** er ekki skilgreint.
    - **WarehouseId** - Einnig er hægt að skilgreina sjálfgefið vöruhús fyrir vörur í inance and Operations. Vöruhús er nauðsynlegt til að búa til tilboð og sölupantanir í Finance and Operations. Sniðmátsgildi fyrir **WarehouseId** er ekki skilgreint.
    - **LanguageId** - Tungumál er nauðsynlegt til að búa til tilboð og sölupantanir í Finance and Operations. Sjálfgefið sniðmátsgildi fyrir **LanguageId** er **en-us**.

## <a name="template-mapping-in-data-integrator"></a>Sniðmátsvörpun í gagnasamþáttara

Eftirfarandi skýringamyndir sýna dæmi um sniðmátsvörpun í gagnasamþáttara.

### <a name="contact-to-contact"></a>Frá Tengilið til Tengiliðs

![Sniðmátsvörpun í gagnasamþáttara](./media/contacts-template-mapping-data-integrator-1.png)

![Sniðmátsvörpun fyrir Tengiliði í gagnasamþáttara](./media/contacts-template-mapping-data-integrator-2.png)

### <a name="contact-to-customer"></a>Frá Tengilið til Viðskiptavinar

![Sniðmátsvörpun í gagnasamþáttara](./media/contacts-template-mapping-data-integrator-3.png)

![Sniðmátsvörpun fyrir Tengiliði í gagnasamþáttara](./media/contacts-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a>Tengd efnisatriði

[Samstilla afurðir úr Finance and Operations í afurðir í Sales](products-template-mapping.md)

[Samstilla lykla frá Sales til viðskiptavina í Finance and Operations](accounts-template-mapping.md)

[Samstilla hausa og línur sölutilboðs úr Sales við Finance and Operations](sales-quotation-template-mapping.md)

[Samstilla hausa og línur sölupöntunar úr Sales við Finance and Operations](sales-order-template-mapping.md)

[Samstilla hausa og línur sölureiknings úr Sales við Finance and Operations](sales-invoice-template-mapping.md)

