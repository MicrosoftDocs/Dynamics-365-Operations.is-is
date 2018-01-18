---
title: "Samstilla afurðir úr Finance and Operations í afurðir í Sales"
description: "Þetta efnisatriði fjallar um sniðmát og undirliggjandi verkefni sem notuð eru til að samstilla afurðir úr Microsoft Dynamics 365 for Finance and Operations, Enterprise edition í Microsoft Dynamics 365 for Sales."
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 405a6cf9f3e6cc52925ff7d9f10836196343c36b
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-products-from-finance-and-operations-to-products-in-sales"></a>Samstilla afurðir úr Finance and Operations í afurðir í Sales

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Áður en þú getur notað lausnina Prospect to cash þarftu að kynna þér [Dynamics 365 gagnasamþættingu](/common-data-service/entity-reference/dynamics-365-integration). 

Þetta efnisatriði fjallar um sniðmát og undirliggjandi verkefni sem notuð eru til að samstilla afurðir úr Microsoft Dynamics 365 for Finance and Operations, Enterprise edition í Microsoft Dynamics 365 for Sales.

## <a name="template-and-task"></a>Sniðmát og verkefni

Eftirfarandi sniðmát og undirliggjandi verkefni eru notuð til að samstilla afurðir úr Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations) í Microsoft Dynamics 365 for Sales (Sales).

-   Nafn sniðmáts: Afurðir (Fin and Ops í Sales)

-   Nafn verkefnis í verki: Afurðir

Samstilla verkefni nauðsynleg fyrir samstillingu afurðar: Ekkert

## <a name="entity-set"></a>Einingastamstæða

| **Finance and Operations** | **CDS** | **Sala**  |
|----------------------------|---------|------------|
| Seljanlegar útgefnar afurðir | Afurð | Afurðir   |

## <a name="entity-flow"></a>Einingaflæði

Afurðum er stýrt í Finance and Operations og þær eru samstilltar í Sales. Gagnaeiningin **Seljanlegar útgefnar afurðir** í Finance and Operations flytja aðeins út afurðir sem eru seljanlegar, sem þýðir að afurðir hafi þær upplýsingar sem þarf að nota í sölupöntun. Sömu reglur gilda þegar afurð er villuleituð með virkninni **Villuleita** á síðunni **Útgefnar afurðir**.

**Afurðarnúmerið** er notað sem lykill, sem þýðir að afurðarafbrigði eru samstillt í CDS og Sales með einstökum **Auðkennum afurðar** á hvert **Afurðarafbrigði**.

## <a name="prospect-to-cash-solution-for-sales"></a>Prospect to cash lausn fyrir Sales

Í Sales er nýjum reitum í afurðum sem er **Unnið með utan frá** bætt við til að gefa til kynna að gefinni afurð sé bætt við utan frá. Gildið er sjálfkrafa stillt á **Já** við innflutning í Sales.

-   **Unnið með utan frá = Já**: Afurð á uppruna sinn í Finance and Operations og ekki er hægt að breyta henni í Sales.

-   **Unnið með utan frá = Nei**: Afurð er skráð beint inn í Sales.

-   **Unnið með utan frá = Autt**: Afurð er til í Sales áður en lausnin Prospect to cash er virkjuð.

Upplýsingarnar í **Unnið með utan frá** eru notaðar til að tryggja að aðeins **Verðtilboð** og **Sölupantanir** með **Afurðum sem unnið er með utan frá** séu samstilltar við Finance and Operations.

**Afurðum sem unnið er með utan frá** er sjálfkrafa bætt við fyrsta gilda **Verðlistann** með sama gjaldmiðlinum. Athugaðu að listanum er raðað í stafrófsröð eftir **Heiti**. Söluverð afurðar úr Finance and Operations er notað sem verð í **Verðlistanum**. Þetta þýðir að það verður að hafa **Verðlista** í Sales fyrir hvern **Sölugjaldmiðil afurðar** í Finance and Operations. Gjaldmiðill í útgefnum seljanlegum afurðum er stilltur á bókhaldsgjaldmiðilinn í þeim lögaðila, þaðan sem afurðin er flutt út frá.

> [!NOTE]
> Afurðarsamstilling gengur ekki eftir án **Verðlista** með samsvarandi gjaldmiðli.

## <a name="preconditions-and-mapping-setup"></a>Skilyrði og vörpunaruppsetning

-   Áður en fyrsta samstilling er keyrð, verður að fylla út **Töflu fyrir einkvæma afurð** fyrir núverandi afurðir í Finance and Operations. Núverandi afurðir samstillast ekki fyrr en þessu er lokið.

    -   Notaðu Leit í Finance and Operations til að leita að **Fylla út töflu fyrir einkvæma afurð**.

    -   Smelltu á **Fylla út töflu fyrir einkvæma afurð** til að keyra vinnsluna. Aðeins þarf að keyra þessa vinnslu einu sinni.

-   Vertu viss um að nauðsynlegt **ValueMap** fyrir sölu á **Mælieiningu** (UOM) í Finance and Operations sé til í **Uppruna -\> CDS vörpun SalesUnitSymbol / DefaultSellingUnitOfMeasure**.

-   Uppfærðu **CDS-fyrirtækjaauðkenni Organization_OrganizationId** í **Uppruni -\> CDS**.

    -   Sniðmátsgildi er sjálfkrafa ORG001.

-   Uppfærðu **ValueMap** fyrir **Einingahóp** (**defaultuomscheduleid.name**) í **CDS -\> Viðtökustaður** svo það hæfi **Einingahópum** í Sales.

    -   Sniðmátsgildi er sjálfkrafa á **Sjálfgefin eining**.

-   Vertu viss um að allar afurðir sem selja mælieiningar úr Finance and Operations séu til í Sales með gildi **CDS-tiltektarlista**.

-   Vertu viss um að **Verðlistar** séu til í Sales fyrir hvern sölugjaldmiðil afurðar í Finance and Operations.

-   Hægt er að stofna afurðir í Sales með stöðunni **Drög** eða **Virk**. Þessu er stýrt í **Kerfisstillingar** undir **Sala** í Sales.

    -   Virkja þarf afurðir sem stofnaðar eru með stöðu fyrir drög áður en hægt er að bæta þeim við **Verðtilboð** eða **Sölupöntun**.

## <a name="template-mapping-in-data-integrator"></a>Sniðmátsvörpun í gagnasamþáttara

Eftirfarandi skýringamyndir sýna dæmi um sniðmátsvörpun í gagnasamþáttara.

![sniðmátsvörpun í gagnasamþáttara](./media/products-template-mapping-data-integrator-1.png)

![sniðmátsvörpun fyrir afurðir í gagnasamþáttara](./media/products-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a>Tengd efnisatriði

[Samstilla lykla frá Sales til viðskiptavina í Finance and Operations](accounts-template-mapping.md)

[Samstilla tengiliði úr Sales við tengiliði eða viðskiptavini í Finance and Operations](contacts-template-mapping.md)

[Samstilla hausa og línur sölutilboðs úr Sales við Finance and Operations](sales-quotation-template-mapping.md)

[Samstilla hausa og línur sölupöntunar úr Sales við Finance and Operations](sales-order-template-mapping.md)

[Samstilla hausa og línur sölureiknings úr Sales við Finance and Operations](sales-invoice-template-mapping.md)


