---
title: Setja upp Azure-tilföng fyrir rafrænar reikningsfærslur
description: Þessi grein inniheldur yfirlit yfir ferlið við að setja upp Microsoft Azure tilföng fyrir rafræna reikningsfærslu.
author: gionoder
ms.date: 01/26/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: f11e4eac831d54a6cac765a5adc4e4ffddbe0a22
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283086"
---
# <a name="set-up-azure-resources-for-electronic-invoicing"></a>Setja upp Azure-tilföng fyrir rafrænar reikningsfærslur

[!include [banner](../includes/banner.md)]

Ferlið til að setja upp Microsoft Azure tilföng fyrir rafræna reikningsfærslu er í þremur skrefum. Fyrstu tvö skrefin: „Stofna Azure-lyklageymslu í Azure-gáttinni“ og „Stofna Azure-geymslureikning í Azure-gáttinni“ eru áskilin. Þriðja skrefið, „Stilla SharePoint tengingu,“ er valfrjálst.

## <a name="create-an-azure-key-vault-in-the-azure-portal"></a>Stofna Azure-lyklageymslu í Azure-gáttinni

Búðu til lyklageymslu í Azure-áskriftinni þinni. Mælt er með því að búa til aðskilda lyklageymslu fyrir rafræna reikningsfærslu og sameina ekki leynilykla við önnur forrit. Búðu til eins marga leynilykla og vottorð og þörf er á fyrir aðstæðurnar í rafrænum skjölum. Búa verður til að minnsta kosti einn leynilykil til að geyma SAS-lykil Azure-geymslureiknings sem verður búinn til í næsta skrefi.

Frekari upplýsingar um hvernig á að ljúka þessu skrefi er að finna í [Stofna Azure-lyklageymslu í Azure-gáttinni](e-invoicing-create-azure-key-vault-azure-portal.md).

## <a name="create-an-azure-storage-account-in-the-azure-portal"></a>Stofna Azure-geymslureikning í Azure-gáttinni

Þú átt öll rafræn skjöl og skrár sem eru búin til af rafrænni reikningsfærsluþjónustu eða skráir þig í þjónustuna. Þessi skjöl og skrár eru geymd á Azure-geymslureikningi sem stofnaður var í Azure-áskriftinni þinni. Þjónustan mun komast inn á geymslureikninginn þinn með því að nota SAS-lykilinn sem er fenginn úr leynilykli lyklageymslunnar.

Frekari upplýsingar um hvernig á að ljúka þessu skrefi er að finna í [Stofna Azure-geymslureikning í Azure-gáttinni](e-invoicing-create-azure-storage-account-azure-portal.md).

## <a name="configure-a-sharepoint-connection"></a>Skilgreina SharePoint-tengingu

Í sumum aðstæðum gæti þurft að vista rafrænar skrár í SharePoint og sækja þær úr SharePoint. Til að tryggja að rafræna reikningsfærsluþjónustan geti opnað SharePoint möppurnar þínar skal skilgreina aðgang að SharePoint.

Frekari upplýsingar um hvernig á að ljúka þessu skrefi er að finna í [Skilgreina SharePoint tengingu](e-invoicing-create-sharepoint-connection.md).
