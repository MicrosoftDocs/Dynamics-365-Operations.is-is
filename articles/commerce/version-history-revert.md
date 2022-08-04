---
title: Skoðaðu útgáfuferil til að snúa síðum og brotum til baka
description: Þessi grein lýsir því hvernig á að skoða útgáfuferil síðu eða brots og fara aftur í eldri útgáfu í Microsoft Dynamics 365 Commerce vefsmiður.
author: phinneyridge
ms.date: 06/21/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: niholman
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: fa2ecdd9d9bc7e60b279d850573b5caa6df2c659
ms.sourcegitcommit: 9cfccb5c260ce56a3457f9ea12e80f54ea55a3b4
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 07/21/2022
ms.locfileid: "9183337"
---
# <a name="view-version-history-to-revert-pages-and-fragments"></a>Skoðaðu útgáfuferil til að snúa síðum og brotum til baka

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Þessi grein lýsir því hvernig á að skoða útgáfuferil síðu eða brots og fara aftur í eldri útgáfu í Microsoft Dynamics 365 Commerce vefsmiður.

Viðskiptasíðugerð gerir þér kleift að skoða útgáfuferil síðu eða brots og fara aftur í tiltekna fyrri útgáfu af skjali ef þörf krefur. Á meðan skjal er opið geturðu valið **Sýna sögu** á skipanastikunni til að opna a **Útgáfusaga** valmynd, þar sem **Útgáfa** flipinn listar sögu allra útgáfur og vistar starfsemi fyrir síðuna eða brotið. Þú getur síðan valið fyrri útgáfu af skjalinu á listanum, forskoðað það og endurheimt það sem núverandi útgáfu. The **Virkni** flipi svargluggans sýnir alla virknisögu skjalsins, þar á meðal alla vistun, birtingu og afbirtingu.

> [!NOTE]
> Ný útgáfa af skjali er búin til í hvert skipti sem höfundur vefsvæðis gerir breytingar og velur síðan **Búið að klippa** fyrir skjalið. 

Til að skoða útgáfuferil síðu eða brots og fara aftur í fyrri útgáfu skaltu fylgja þessum skrefum.

1. Í Site Builder, opnaðu síðuna eða brotið sem þú vilt skoða útgáfuferilinn fyrir.
1. Veldu á skipanastikunni **Sýna sögu**.

    ![Sýna söguhnapp.](./media/version-history-1.png)

1. Í **Útgáfusaga** valmynd, á **Útgáfa** flipanum, veldu fyrri útgáfu af skjalinu. Eiginleikarúðan til hægri sýnir smámynd af völdu útgáfunni og upplýsingar um hver breytti henni og hvenær.

    ![Útgáfuferilslistasýn.](./media/version-history-2.png)

1. Til að skoða fullkomlega sýnishorn af völdu útgáfu skjalsins skaltu velja **Forskoðun**. Til að loka forskoðuninni og fara aftur í **Útgáfusaga** valmynd, veldu **Hætta forskoðun**.
1. Til að endurheimta fyrri útgáfu af skjali skaltu velja það á listanum á **Útgáfa** flipann og veldu síðan **Endurheimta**. A **Endurheimta útgáfu\<version number\>** skilaboðakassi birtist og biður þig um að staðfesta endurheimtunaraðgerðina. 

    ![Endurheimta hnappinn og staðfestingarskilaboðakassi.](./media/version-history-3.png)

1. Til að halda áfram með endurheimtunaraðgerðina skaltu velja **Endurheimta**. Vefsíðugerð er endurnýjuð og sýnir endurheimtu útgáfuna af síðunni eða brotinu.
1. Til að birta endurheimtu útgáfuna skaltu velja **Ljúktu við klippingu**, og veldu síðan **Birta**.
