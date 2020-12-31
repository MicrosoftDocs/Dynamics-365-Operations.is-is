---
title: Nýir notendur stofnaðir
description: Notendur eru innri starfsmenn fyrirtækisins, eða ytri viðskiptavinir og lánardrottnar sem þurfa aðgang að kerfinu til að framkvæma vinnslum.
author: peakerbl
manager: AnnBe
ms.date: 06/08/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6f861b7493d039b332358be7df7d0198cbadcb7a
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679841"
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
1. Farðu í **Kerfisstjórnun \> Notendur \> Notendur**.
2. Á Aðgerðasvæðinu skal velja **Flytja inn notendur**.
3. Í listanum skal merkja valda línu.
4. Veldu **Flytja inn notendur**.
5. Veljið **Loka**.

