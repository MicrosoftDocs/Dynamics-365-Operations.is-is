---
title: Skilyrði fyrir uppsetningu rásar
description: Þessi grein sýnir yfirlit yfir forsendur rásauppsetningar í Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 02/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 98ca2dc4691534853467c1680890199d08bc4e79
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282296"
---
# <a name="channel-setup-prerequisites"></a>Skilyrði fyrir uppsetningu rásar

[!include [banner](includes/banner.md)]

Þessi grein sýnir yfirlit yfir forsendur rásaruppsetningar í Microsoft Dynamics 365 Commerce.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
