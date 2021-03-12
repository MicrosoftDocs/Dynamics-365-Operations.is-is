---
title: Setja upp aðallykla flokka
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp flokka aðallykla í Dynamics 365 Finance.
author: aprilolson
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MainAccountCategory, MainAccountCategoryLink
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0d53181d63f7b362662d993e21671e9b685b5dfe
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968428"
---
# <a name="set-up-main-account-categories"></a>Setja upp aðallykla flokka

[!include [banner](../../includes/banner.md)]

Í þessu efnisatriði er útskýrt hvernig á að setja upp flokka aðallykla. Flokkar aðallykla eru notaðir fyrir sjálfgefnar skýrslur í fjárhagsskýrslu og Power BI. Hægt er að endurnefna flokka aðallykla sem eru stofnaðir sjálfvirkt en ekki eyða. Hægt er að stofna viðbótar lykilflokka og nota vegna skýrslugerðar og greiningar. Þetta efni notar sýnifyrirtækið USMF.

## <a name="create-a-main-account-category"></a>Stofna tegund aðallykils
1. Í skoðunarrúðunni ferðu í **Kerfiseiningar > Fjárhagur > Bókhaldslykill > Lyklar > Flokkar aðallykla**.
2. Veljið **Nýtt**.
3. Í reitnum **Flokkur aðallykils** skal færa inn einkvæmt heiti.
4. Í reitnum **Lýsing** færirðu inn lýsingu á flokki aðallykils.
5. Í reitnum **Gerð aðallykils** skal velja þá gerð aðallykils sem verður tengd við flokkinn.

## <a name="link-main-accounts-to-account-category"></a>Tengja aðallykla við tegund aðallykils
1. Smelltu á **Tengja aðallykla**.
2. Á listanum velurðu aðallyklana sem á að tengja við aðallyklaflokkinn með því að haka við reitina í dálkinum **Tengt**. Úthlutun aðallykla á flokk aðallykla mun safna saman stöðum lyklanna þegar sá flokkur er notaður fyrir fjárhagsskýrslugerð og fjárhagsgreiningu.  
3. Veldu eða hreinsaðu valkostinn **Tengt** til að velja aðallykla.
4. Veljið **Í lagi**.
5. Velja skal **Já**.
