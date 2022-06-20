---
title: Setja upp Azure-tilföng fyrir rafrænar reikningsfærslur
description: Þessi grein veitir yfirlit yfir ferlið við uppsetningu Microsoft Azure úrræði fyrir rafræna reikninga.
author: dkalyuzh
ms.date: 01/26/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: c5b7b2ca4d7733fb1c75ded8798655699284fe1a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907730"
---
# <a name="set-up-azure-resources-for-electronic-invoicing"></a>Setja upp Azure-tilföng fyrir rafrænar reikningsfærslur

[!include [banner](../includes/banner.md)]

Ferlið við að setja upp Microsoft Azure úrræði fyrir rafræna reikninga eru þrjú skref. Fyrstu tvö skrefin, „Búa til Azure lykilhólf í Azure gáttinni“ og „Búa til Azure geymslureikning í Azure gáttinni,“ eru nauðsynleg. Þriðja skrefið, „Stilla a SharePoint tenging,“ er valfrjálst.

## <a name="create-an-azure-key-vault-in-the-azure-portal"></a>Búðu til Azure lykilhólf í Azure gáttinni

Búðu til lykilhólf í Azure áskriftinni þinni. Við mælum með að þú búir til sérstaka lyklageymslu fyrir rafræna reikninga og að þú sameinar ekki leyndarmál við önnur forrit. Búðu til eins mörg leyndarmál og vottorð og þú þarft fyrir aðstæður þínar í rafrænum skjölum. Þú verður að búa til að minnsta kosti eitt leyndarmál til að geyma samnýtt undirskrift (SAS) tákn Azure geymslureikningsins sem þú býrð til í næsta skrefi.

Fyrir upplýsingar um hvernig á að ljúka þessu skrefi, sjá [Búðu til Azure lykilhólf í Azure gáttinni](e-invoicing-create-azure-key-vault-azure-portal.md).

## <a name="create-an-azure-storage-account-in-the-azure-portal"></a>Stofna Azure-geymslureikning í Azure-gáttinni

Þú átt öll rafræn skjöl og skrár sem eru búin til af rafrænum reikningaþjónustu eða fer inn í þjónustuna. Þessi skjöl og skrár eru geymdar á Azure geymslureikningi sem þú býrð til í Azure áskriftinni þinni. Þjónustan mun fá aðgang að geymslureikningnum þínum með því að nota SAS táknið sem er tekið úr Key Vault leyndarmálinu þínu.

Fyrir upplýsingar um hvernig á að ljúka þessu skrefi, sjá [Búðu til Azure geymslureikning í Azure gáttinni](e-invoicing-create-azure-storage-account-azure-portal.md).

## <a name="configure-a-sharepoint-connection"></a>Skilgreina SharePoint-tengingu

Í sumum tilfellum gætirðu þurft að vista rafrænar skrár í SharePoint og sækja þá frá SharePoint. Til að tryggja að rafræn reikningaþjónusta hafi aðgang að þínum SharePoint möppur, stilla aðgang að SharePoint.

Fyrir upplýsingar um hvernig á að ljúka þessu skrefi, sjá [Stilla a SharePoint Tenging](e-invoicing-create-sharepoint-connection.md).
