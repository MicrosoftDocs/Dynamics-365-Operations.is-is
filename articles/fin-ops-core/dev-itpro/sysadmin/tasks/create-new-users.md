---
title: Nýir notendur stofnaðir
description: Notendur eru innri starfsmenn fyrirtækisins, eða ytri viðskiptavinir og lánardrottnar sem þurfa aðgang að kerfinu til að framkvæma vinnslum.
author: maertenm
manager: AnnBe
ms.date: 10/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3c347a34a389c32d005cc8086c4a1349ecb8a698
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570522"
---
# <a name="create-new-users"></a>Nýir notendur stofnaðir

[!include [task guide banner](../../includes/task-guide-banner.md)]

Notendur eru innri starfsmenn fyrirtækisins, eða ytri viðskiptavinir og lánardrottnar sem þurfa aðgang að kerfinu til að keyra vinnslur.

## <a name="associate-a-user-with-a-license-new-license-types-only"></a>Úthlutaðu notanda leyfi (aðeins nýjar tegundir leyfis)
Fyrir viðskiptavini sem eru á einni af nýju leyfistegundunum sem bætt var við í október 2019, verða notendur að hafa úthluta leyfi. Notendur sem er úthlutað leyfi bætast sjálfkrafa við sem kerfisnotendur sem hafa engin hlutverk í fyrsta skipti sem þeir skrá sig inn. Notendur sem ekki er úthlutað leyfi fá viðvörunarskilaboð.

Kerfisstjórar geta það [úthluta leyfi til notenda](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) í [stjórnunarmiðstöð Microsoft 365](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).

## <a name="add-a-new-user"></a>Bæta við nýr notandi
1. Farðu í **Kerfisstjórnun \> Notendur \> Notendur**.
2. Í aðgerðarúðunni velurðu **Nýtt**.
3. Í reitnum **Notandakenni** er fært inn einkvæmt kenni fyrir notandann. Notandakenni er áskilið.  
4. Í reitnum **Notandanafn** skal færa inn notandaheiti.  
5. Í reitinn **Lén** er lén notanda fært inn.  
6. Í reitinn **Samheiti** skal slá inn samheiti notandans.  
7. Í reitnum **Fyrirtæki** skal velja óskað fyrirtæki. 
8. Á flýtiflipanum **Hlutverk notanda** velurðu **Úthluta hlutverkum** til að [úthluta notendum á öryggishlutverk](assign-users-security-roles.md)
9. Veljið **Í lagi**.
10. Veljið **Vista**.

## <a name="import-users"></a>Flytja inn notendur
1. Á Aðgerðasvæðinu skal velja **Flytja inn notendur**.
2. Í listanum skal merkja valda línu.
3. Veldu **Flytja inn notendur**.
4. Veljið **Loka**.

