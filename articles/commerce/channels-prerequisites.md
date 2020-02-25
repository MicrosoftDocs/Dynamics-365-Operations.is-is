---
title: Skilyrði fyrir rásauppsetningu
description: Þetta efni birtir yfirlit yfir forsendur fyrir uppsetningu rása í Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b861d90f1333c8f6e61a83602ed74e30b65f3dc1
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002290"
---
# <a name="channel-setup-prerequisites"></a>Skilyrði fyrir rásauppsetningu


[!include [banner](includes/banner.md)]

Þetta efni birtir yfirlit yfir forsendur fyrir uppsetningu rása í Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Áður en hægt er að stofna rás í Dynamics 365 Commerce verður nokkrum nauðsynlegum verkum að vera lokið. Eftirfarandi listar með forsenduverkum eru skipulagðir eftir gerð rásar.

> [!NOTE]
> Enn er verið að skrifa nokkur skjöl og tenglar verða uppfærðir þegar nýtt efni er birt.

## <a name="initialization"></a>Frumstilling

- [Frumstilla grunngögn](../retail/enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a>Altækar forsendur sem krafist er fyrir allar rásategundir

- [Skilgreina og stilla uppbyggingu lögaðila](channels-legal-entities.md) 
- [Skilgreindu fyrirtækjastigveldið](channels-org-hierarchies.md)
- [Setja upp vöruhús](channels-setup-warehouse.md)
- [Stilla virðisaukaskatt](https://docs.microsoft.com/en-us/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json)
- [Setja upp forstillingu tilkynningar í tölvupósti](email-notification-profiles.md)
- [Setja upp númeraraðir](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview?toc=/dynamics365/commerce/toc.json)
- [Settu upp sjálfgefna viðskiptavini og heimilisfangabók](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a>Skilyrði fyrir rásum í Retail

- [Upplýsingakóðar og upplýsingakóðaflokkar](https://docs.microsoft.com/en-us/dynamics365/retail/info-codes-retail?toc=/dynamics365/commerce/toc.json)
- [Setja upp virknireglu f. smásölu](retail-functionality-profile.md)
- [Setja upp heimilifangabók starfsmanna](new-address-book.md)
- [Setja upp útlit afgreiðsluskjás](https://docs.microsoft.com/en-us/dynamics365/retail/pos-screen-layouts?toc=/dynamics365/commerce/toc.json)
- [Setja upp vélbúnaðarstöð](https://docs.microsoft.com/en-us/dynamics365/retail/retail-hardware-station-configuration-installation?toc=/dynamics365/commerce/toc.json)

## <a name="call-center-channel-prerequisites"></a>Forsendur rásar símavers

- Færibreytur símavers
- Endurgreiðslumátar símavers
- Leigugerð
- Greiðsluþjónustur
- Biðkóðar pantana

## <a name="online-channel-prerequisites"></a>Skilyrði fyrir netrásum

- [Stofna virknireglu fyrir netverslun.](online-functionality-profile.md)

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir rásir](channels-overview.md)

[Yfirlit yfir fyrirtæki og fyrirtækjastigveldi](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[Setja upp stigveldi fyrirtækis](channels-org-hierarchies.md)

[Stofna lögaðila](channels-legal-entities.md)

[Setja upp smásölurás](channel-setup-retail.md)
    
[Setja upp netrás](channel-setup-online.md)
