---
title: Skilyrði fyrir rásauppsetningu
description: Þetta efni birtir yfirlit yfir forsendur fyrir uppsetningu rása í Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 02/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 0705efac4659f96ebca1c67f6f0ab8d23c99d81e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4997701"
---
# <a name="channel-setup-prerequisites"></a>Skilyrði fyrir rásauppsetningu


[!include [banner](includes/banner.md)]

Þetta efni birtir yfirlit yfir forsendur fyrir uppsetningu rása í Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Áður en hægt er að stofna rás í Dynamics 365 Commerce verður nokkrum nauðsynlegum verkum að vera lokið. Eftirfarandi listar með forsenduverkum eru skipulagðir eftir gerð rásar.

> [!NOTE]
> Enn er verið að skrifa nokkur skjöl og tenglar verða uppfærðir þegar nýtt efni er birt.

## <a name="initialization"></a>Frumstilling

- [Frumstilla grunngögn](enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a>Altækar forsendur sem krafist er fyrir allar rásategundir

- [Skilgreina og stilla uppbyggingu lögaðila](channels-legal-entities.md) 
- [Skilgreindu fyrirtækjastigveldið](channels-org-hierarchies.md)
- [Setja upp vöruhús](channels-setup-warehouse.md)
- [Stilla virðisaukaskatt](../finance/general-ledger/indirect-taxes-overview.md?toc=/dynamics365/commerce/toc.json)
- [Setja upp forstillingu tilkynningar í tölvupósti](email-notification-profiles.md)
- [Setja upp númeraraðir](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=/dynamics365/commerce/toc.json)
- [Settu upp sjálfgefna viðskiptavini og heimilisfangabók](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a>Skilyrði fyrir rásum í Retail

- [Upplýsingakóðar og upplýsingakóðaflokkar](info-codes-retail.md)
- [Setja upp virknireglu f. smásölu](retail-functionality-profile.md)
- [Setja upp heimilifangabók starfsmanna](new-address-book.md)
- [Setja upp útlit afgreiðsluskjás](pos-screen-layouts.md)
- [Setja upp vélbúnaðarstöð](retail-hardware-station-configuration-installation.md)

## <a name="call-center-channel-prerequisites"></a>Forsendur rásar símavers

- Færibreytur símavers
- [Símaverspöntun og endurgreiðslumátar](work-with-payments.md)
- [Stillingar afhendingarmáta og gjalda símavers](configure-call-center-delivery.md)

## <a name="online-channel-prerequisites"></a>Skilyrði netrásar

- [Búa til virkniforstillingu á netinu](online-functionality-profile.md)

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir rásir](channels-overview.md)

[Yfirlit yfir fyrirtæki og fyrirtækjastigveldi](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[Setja upp stigveldi fyrirtækis](channels-org-hierarchies.md)

[Stofna lögaðila](channels-legal-entities.md)

[Setja upp smásölurás](channel-setup-retail.md)
    
[Setja upp netrás](channel-setup-online.md)
