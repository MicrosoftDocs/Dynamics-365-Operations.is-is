---
title: Nýir notendur stofnaðir
description: Notendur eru innri starfsmenn fyrirtækisins, eða ytri viðskiptavinir og lánardrottnar sem þurfa aðgang að kerfinu til að framkvæma vinnslum.
author: maertenm
manager: AnnBe
ms.date: 02/06/2020
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
ms.openlocfilehash: 9db4b6d355d6499bce6c550b2fbe76b82cf69fd4
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143581"
---
# <a name="create-new-users"></a>Nýir notendur stofnaðir

[!include [banner](../../includes/banner.md)]

Notendur eru innri starfsmenn fyrirtækisins, eða ytri viðskiptavinir og lánardrottnar sem þurfa aðgang að kerfinu til að keyra vinnslur.

## <a name="associate-a-user-with-a-license-new-license-types-only"></a>Úthlutaðu notanda leyfi (aðeins nýjar tegundir leyfis)
Fyrir viðskiptavini sem eru á einni af nýju leyfistegundunum sem bætt var við í október 2019, verða notendur að hafa úthluta leyfi. Notendur sem er úthlutað leyfi bætast sjálfkrafa við sem kerfisnotendur sem hafa engin hlutverk í fyrsta skipti sem þeir skrá sig inn.

Kerfisstjórar geta það [úthluta leyfi til notenda](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) í [stjórnunarmiðstöð Microsoft 365](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).

## <a name="associate-an-external-user-with-a-license-new-license-types-only"></a>Úthlutaðu ytri notanda leyfi (aðeins nýjar tegundir leyfis)
Notendur utan leigjandans sem umhverfinu var dreift í þurfa að vera fulltrúar í hýsingaraðilum leigjanda (Azure Active Directory (Azure AD)) svo að hægt sé að fá þeim leyfi. Þessum utanaðkomandi notendum ætti að bæta við leigjandann í Azure AD sem gestanotendum og úthluta þeim síðan viðeigandi leyfum. Nánari upplýsingar er að finna í [Bæta Azure Active Directory B2B samvinnunotendum við í Azure-gáttinni](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).

## <a name="add-a-new-user"></a>Bæta við nýr notandi
1. Farðu í **Kerfisstjórnun \> Notendur \> Notendur**.
2. Í aðgerðarúðunni velurðu **Nýtt**.
3. Í reitnum **Notandakenni** er fært inn einkvæmt kenni fyrir notandann. Notandakenni er áskilið.  
4. Í reitnum **Notandanafn** skal færa inn notandaheiti.  
5. Í reitinn **Lén** er lén notanda fært inn.  
6. Í reitinn **Samheiti** skal slá inn samheiti notandans.  
7. Í reitnum **Fyrirtæki** skal velja óskað fyrirtæki. 
8. Á flýtiflipanum **Hlutverk notanda** velurðu **Úthluta hlutverkum** til að úthluta notendum á öryggishlutverk. Nánari upplýsingar er að finna á [Úthluta notendum á öryggishlutverk](assign-users-security-roles.md).
9. Veljið **Í lagi**.
10. Veljið **Vista**.

## <a name="import-users"></a>Flytja inn notendur
1. Á Aðgerðasvæðinu skal velja **Flytja inn notendur**.
2. Í listanum skal merkja valda línu.
3. Veldu **Flytja inn notendur**.
4. Veljið **Loka**.

