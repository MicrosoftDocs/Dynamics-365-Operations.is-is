---
title: "Skilgreiningar lánardrottinsbeiðni"
description: "Þetta efnisatriði lýsir svæðunum sem nauðsynlegt er að fylla í nýrri lánardrottnabeiðni."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendProspectiveVendorRegistrationConfig
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: ba426692e2e404ab75e5730b8205115fc59e402f
ms.openlocfilehash: e9b22a6f846607e8afc5d4f01c685f1364b1c01d
ms.contentlocale: is-is
ms.lasthandoff: 02/08/2018

---

# <a name="vendor-request-configurations"></a>Skilgreiningar lánardrottinsbeiðni
[!include[banner](../includes/banner.md)]

Til að ljúka lánardrottnabeiðni þarf tengiliður lánardrottins að fara í gegnum leiðsagnarforrit fyrir skráningu væntanlegs lánardrottins.

Í **Grunnstillingar lánardrottinsbeiðni** skjámyndinni getur þú stofnað forstillingar sem tilgreina svæði og sýnilegar svæði í leiðsagnarforriti fyrir skráningu væntanlegs lánardrottins.

Leiðsagnarforrit fyrir skráningu lánardrottins byrjar á því að spyrja væntanlegan lánardrottin hvaða land/svæði lánardrottinn á viðskipti í. Þessar upplýsingar ákvarða viðeigandi grunnstillingu. Ef engin ákveðin grunnstilling er skilgreind fyrir land/svæði verður sjálfgefið grunnstillingar notað.

### <a name="set-up-a-vendor-request-configuration"></a>Setja upp grunnstillingar lánardrottinsbeiðni

Sjálfgefið er að lánardrottins grunnstilling sé tiltæk í skjámynd grunnstillinga lánardrottinsbeiðni.

Ekki er hægt að velja land/svæði fyrir sjálfgefna grunnstillingu, þannig að ekki er hægt að breyta **Löndum/svæðum**.

1.  Smelltu á **Innkaup og aðföng** > **Uppsetning** > **Lánardrottnar**, og smelltu síðan á **Grunnstillingar lánardrottinsbeiðni**.
2.  Smelltu á flipann **Svæði** til að stilla staða skráðra svæða.
-   Falið (ekki sýnilegt)
-   Sýnt (sýnilegt en ekki skylt)
-   Nauðsynlegt (sýnilegt og skylt)
3.  Smelltu á flipann **Innihald** til að tilgreina hvort textinn á að sjást í leiðsagnarforritinu og hvort það ætti að vera viðurkenning á því að væntanlegur lánardrottna notandi verður að samþykkja þetta áður en hann fer í næsta skref í leiðsagnarforritinu. Beðið verður um viðurkenninguna fyrir hvaða skilmála og skilyrði sem notandinn verður að samþykkja til að halda áfram.

Þú getur einnig slegið inn staðfestingarskilaboð sem munu birtast þegar búið er að fara í gegnum leiðsagnarforritið, og þú getur bætt við einni eða fleiri spurningalistum.

### <a name="create-a-vendor-configuration-for-a-specific-countryregion"></a>Búa til grunnstillingar lánardrottins fyrir tiltekna land/svæði
1.  Smelltu á **Innkaup og aðföng** > **Uppsetning** > **Lánardrottnar**, og smelltu síðan á **Grunnstillingar lánardrottinsbeiðni**.
2.  Smellt er á **Ný** til að búa til nýjar grunnstillingu, og nafn á grunnstillinguna.
3.  Smellið á **Vista**.
4.  Opnaðu flipann **Land/svæði** til að velja landið/svæðið sem á að nota grunnstillinguna fyrir.
5.  Ljúktu grunnstillingunni með því að fylgja leiðbeiningunum um sjálfgefna grunnstillingu.


