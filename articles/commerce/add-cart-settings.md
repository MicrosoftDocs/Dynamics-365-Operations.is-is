---
title: Nota stillingar til að bæta vöru við körfu
description: Þessi grein fjallar um ""Bæta vöru í körfu"" stillingar og lýsir því hvernig eigi að nota þær í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 16644e6746d182cd86a40861c4e30a85a9d3d478
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277028"
---
# <a name="apply-add-product-to-cart-settings"></a>Nota stillingar til að bæta vöru við körfu

[!include [banner](includes/banner.md)]

Þessi grein fjallar um **Bæta vöru í körfu** stillingar og lýsir því hvernig eigi að nota þær í Microsoft Dynamics 365 Commerce.

Stuðst er við mismunandi verkflæði þegar vöru er bætt í körfuna á Dynamics 365 Commerce svæði fyrir rafræn viðskipti. Til dæmis gæti notandi vefsvæðisins verið færður á síðu körfunnar. Einnig getur notandinn verið á núverandi síðu en fengið tilkynningu sem staðfestir að vörunni hafi verið bætt í körfuna.

Til að styðja við mismunandi verkflæði er reitur fyrir **Bæta vöru í körfu** tiltækur í **Stillingar \> Viðbætur** í vefsmið Commerce. Veldu einn af eftirfarandi stillingarmöguleikum til að innleiða samsvarandi verkflæði:

- **Fara á síðu körfu** – Þegar notendur bæta vöru í körfuna er farið með þá á síðu körfunnar.
- **Sýna tilkynningu** – Þegar notendur bæta vöru í körfuna fá þeir tilkynningu um staðfestingu og geta haldið áfram að skoða hana á upplýsingasíðu vörunnar (PDP).
- **Sýna smákörfu** – Þegar notendur bæta vöru í körfuna er innihald smákörfunnar sýnt. Notendur geta farið yfir allar vörurnar í körfunni og haldið áfram til að ganga frá greiðslu ef allt er til reiðu.
- **Sýna tilkynningu með tilkynningareiningu** – Þegar notendur bæta vöru í körfuna er tilkynningareiningin notuð til að sýna tilkynningu um staðfestingu. Til að þessi stilling virki þarf að bæta tilkynningareiningunni við síðuhausinn.
- **Ekki fara á síðu körfu** – Þegar notendur bæta vöru í körfuna halda þeir áfram á núverandi síðu.

Eftirfarandi skýringarmynd sýnir dæmi um stillingarmöguleikann **Bæta vöru í körfu** í vefsmiðnum.

![Dæmi um stillingarmöguleika fyrir „Bæta vöru í körfu“ í vefsmið](./media/AW_sitesettings.PNG)

> [!IMPORTANT]
> - Síðustillingin **Bæta vöru í körfu** er í boði í Dynamics 365 Commerce útgáfu 10.0.11. Ef verið er að uppfæra úr eldri útgáfu af Dynamics 365 Commerce verður að uppfæra appsettings.json-skrána handvirkt. Upplýsingar um hvernig á að uppfæra appsettings.json-skrána er að finna í [Uppfærslur á SDK og einingasafni](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).
> - Stillingarmöguleikinn **Sýna smákörfu** er tiltækur frá og með Dynamics 365 Commerce útgáfu 10.0.20. Ef verið er að uppfæra úr eldri útgáfu af Dynamics 365 Commerce verður að uppfæra appsettings.json-skrána handvirkt. Upplýsingar um hvernig á að uppfæra appsettings.json-skrána er að finna í [Uppfærslur á SDK og einingasafni](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

Eftirfarandi mynd sýnir dæmi um staðfestingartilkynninguna „bætt í körfu“ á Fabrikam-svæðinu.

![Dæmi um staðfestingartilkynninguna „bætt í körfu“ á Fabrikam-svæðinu](./media/ecommerce-addtocart-notifications.PNG)

Eftirfarandi mynd sýnir dæmi um staðfestingartilkynninguna „bætt í körfu“ á svæði Adventure Works.

![Dæmi um staðfestingartilkynninguna „bætt í körfu“ á svæði Adventure Works](./media/AW_minicart.PNG)

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit einingasafns](starter-kit-overview.md)

[Kaupgluggaeining](add-buy-box.md)

[Eining til að velja verslun](store-selector.md)
