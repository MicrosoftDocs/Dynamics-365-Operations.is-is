---
title: Yfirlit yfir rásir
description: Þetta efni birtir yfirlit yfir rásir í Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 099ccd9f769ea5c431c1a82532d8654cbbd082b1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413119"
---
# <a name="channels-overview"></a>Yfirlit yfir rásir


[!include [banner](includes/banner.md)]

Þetta efni birtir yfirlit yfir rásir í Microsoft Dynamics 365 Commerce. Það felur í sér upplýsingar um þau verk sem ljúka verður bæði áður en eða eftir að þú hefur lokið við að setja hverja rás upp.

## <a name="types-of-channels"></a>Gerðir rása

Dynamics 365 Commerce styður þrjár mismunandi rásategundir: smásölu, símaver og netrásir.

### <a name="retail-channels"></a>Smásölurásir

Smásölurásir standa fyrir hefbundnar verslanir. Hvert verslun getur haft sína eigin afgreiðslukassa á sölustað, tekju- og kostnaðarlykla og starfsfólk. 

### <a name="call-center-channels"></a>Rásir símavers

Símaversrásir sýna símaverspöntun og stjórnun viðskiptavina.

### <a name="online-channels"></a>Netrásir

Netrásir eru netverslanir á netinu. Þegar netrás hefur verið stofnuð verður að búa til vefsíðu með Microsoft Dynamics 365 Commerce vefsvæðishönnunartóli eða annari e-Commerce lausn þriðja aðila.

## <a name="channel-setup-basics"></a>Grunnatriði rásaruppsetningar

Uppsetning rásar er framkvæmd í viðskiptatækinu. Hver rás getur haft sínar eigin greiðsluaðferðir, verðhópa, stigveldi vöru, úrval og vöruúrval. Eftir að þú stofnar rás úthlutarðu þeim afurðum sem þú vilt að verslunin selji. Hver rásartegund hefur einstakt sett af eiginleikum sem kann að þurfa að stilla. Til dæmis þarf verslunarrás að fá úthlutað starfsmönnum, skrám og viðskiptavinum. Þegar ný rás er búin til þarf að tengja hana við stigveldi fyrirtækis.

## <a name="channel-setup-prerequisites"></a>Skilyrði fyrir rásauppsetningu

Áður en hægt er að setja upp rás verður að klára nokkur forsenduverk sem byggjast á gerð rásarinnar. Fyrir frekari upplýsingar, sjá [Forsendur rásaruppsetningar](channels-prerequisites.md).

## <a name="set-up-a-channel"></a>Setja upp rás

Eftir að þú hefur lokið forsendum verkefna, notaðu eftirfarandi tengla til að fá frekari leiðbeiningar um uppsetningu.

- [Setja upp smásölurás](channel-setup-retail.md)
- [Setja upp rás símavers](channel-setup-callcenter.md)
- [Setja upp netrás](channel-setup-online.md)

<!--
## Post-channel configuration

After you create a channel, you may need to complete some of the below tasks:

- [Add channel to an organizational hierarchy](add-channel-org-hierarchy.md)
- Set up fulfillment groups. (LINK TBD)
- Configure the POS registers for the store. (LINK TBD)
- Assign product assortments to the store. (LINK TBD)
- Process assortments to generate the list of products that are included in the assortment and to make the products available in the retail store. (LINK TBD)
- Send data such as number sequences, hardware profiles, and POS screen layouts to the Retail POS registers.(LINK TBD)
- Publish the retail store to send store data to Retail POS. (LINK TBD)
- Run the jobs to send the store data to Retail POS. (LINK TBD)
-->

## <a name="additional-resources"></a>Frekari upplýsingar

[Skilyrði fyrir rásauppsetningu](channels-prerequisites.md)

[Setja upp smásölurás](channel-setup-retail.md)
    
[Setja upp netrás](channel-setup-online.md)

[Setja upp rás símavers](channel-setup-callcenter.md)

[Setja upp stigveldi fyrirtækis](channels-org-hierarchies.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]