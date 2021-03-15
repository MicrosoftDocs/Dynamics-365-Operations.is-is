---
title: Setja upp greiðsluseðlasnið fyrir verkreikninga
description: Fyrirtæki yfirleitt tengja prentaða greiðsluseðlar við reikninga til að aðstoða viðskiptavina og veita þannig greiðslutilvísun fyrir bókun og jöfnun.
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OMLegalEntity, CustFormletterParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cca7ceb3c862d8a7b2d5a88111b9b3ea46a6c9ea
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988075"
---
# <a name="set-up-payment-slip-format-for-project-invoices"></a>Setja upp greiðsluseðlasnið fyrir verkreikninga

[!include [banner](../../includes/banner.md)]

Fyrirtæki yfirleitt tengja prentaða greiðsluseðlar við reikninga til að aðstoða viðskiptavina og veita þannig greiðslutilvísun fyrir bókun og jöfnun. Hægt er að nota greiðsluseðillinn fyrir reikninga verks eða þjónustusamning , innheimtubréf, vaxtanótur og reikningsyfirlit auk sölureikninga og reikningur með frjálsum texta. Til að vinna greiðsluseðlar, fyrst uppsetning kenninúmer lánardrottins og snið greiðsluseðill í viðhengi.

Þessi aðferð notar sýnigögn DEMF fyrirtækisins. 

Þessi Virkni er eingöngu tiltæk fyrir lögaðila með aðalaðsetur fyrir Danmörk.


## <a name="set-up-a-creditor-id-number"></a>Setja upp Kenninúmer lánardrottins
1. Fara í Fyrirtækisstjórnun > Fyrirtæki > Lögaðilar.
2. Útvíkka eða draga saman hluta upplýsingar bankareiknings.
3. Smellið á „Breyta“.
4. Færa inn gildi í svæðið Kenni FI-Lánardrottins.
5. Smellið á „Vista“.
6. Lokið síðunni.

## <a name="set-up-a-payment-slip-format-for-invoices-notes-letters-and-statements"></a>Setja upp snið greiðsluseðill fyrir reikninga, seðlar, bréf og yfirlit
1. Fara í Viðskiptakröfur > Uppsetning > Eyðublöð > Uppsetning eyðublaða.
2. Smellið á flipann Reikningur.
3. Í Tengd greiðslukvittun á svæði fyrir reikning viðskiptavinar, velja valkost.
    * Ekkert – ekki prenta greiðsluseðil. Þessi kostur er valinn ef greiðsluupphæðin er í öðrum gjaldmiðli en danskar krónur (DKK).   FIK 751 – Prenta FIK 751 greiðsluseðil ef ætlunin er að skrifa greiðsluupphæðina og gjalddaga handvirkt á greiðsluseðilinn.   FIK 752 – Prenta FIK 752 greiðsluseðil ef ætlunin er að nota tölvugerðan greiðsluseðil sem er með fyrirframprentaða greiðsluupphæð og gjalddaga.  
4. Smellið á „Vista“.
5. Smellt er á flipanum reikningur með frjálsum texta.
6. Tengd greiðslukvittun á reikningur með frjálsum texta svæði, velja valkost.
    * Ekkert – ekki prenta greiðsluseðil. Þessi kostur er valinn ef greiðsluupphæðin er í öðrum gjaldmiðli en danskar krónur (DKK).   FIK 751 – Prenta FIK 751 greiðsluseðil ef ætlunin er að skrifa greiðsluupphæðina og gjalddaga handvirkt á greiðsluseðilinn.   FIK 752 – Prenta FIK 752 greiðsluseðil ef ætlunin er að nota tölvugerðan greiðsluseðil sem er með fyrirframprentaða greiðsluupphæð og gjalddaga.  
7. Smellið á „Vista“.
8. Smellið á flipann vaxtanóta.
9. Í Tengd greiðslukvittun á svæði fyrir vaxtanóta, velja valkost.
    * Ekkert – ekki prenta greiðsluseðil. Þessi kostur er valinn ef greiðsluupphæðin er í öðrum gjaldmiðli en danskar krónur (DKK).   FIK 751 – Prenta FIK 751 greiðsluseðil ef ætlunin er að skrifa greiðsluupphæðina og gjalddaga handvirkt á greiðsluseðilinn.   FIK 752 – Prenta FIK 752 greiðsluseðil ef ætlunin er að nota tölvugerðan greiðsluseðil sem er með fyrirframprentaða greiðsluupphæð og gjalddaga.  
10. Smellið á „Vista“.
11. Smellt er á flipanum innheimtubréfs.
12. Í Tengd greiðslukvittun á svæðinu innheimtubréf, velja valkost.
    * Ekkert – ekki prenta greiðsluseðil. Þessi kostur er valinn ef greiðsluupphæðin er í öðrum gjaldmiðli en danskar krónur (DKK).   FIK 751 – Prenta FIK 751 greiðsluseðil ef ætlunin er að skrifa greiðsluupphæðina og gjalddaga handvirkt á greiðsluseðilinn.   FIK 752 – Prenta FIK 752 greiðsluseðil ef ætlunin er að nota tölvugerðan greiðsluseðil sem er með fyrirframprentaða greiðsluupphæð og gjalddaga.  
13. Smellið á „Vista“.
14. Smellið á flipann lyklayfirlit.
15. Í Tengd greiðslukvittun á svæðinu lyklayfirlit, velja valkost.
    * Ekkert – ekki prenta greiðsluseðil. Þessi kostur er valinn ef greiðsluupphæðin er í öðrum gjaldmiðli en danskar krónur (DKK).   FIK 751 – Prenta FIK 751 greiðsluseðil ef ætlunin er að skrifa greiðsluupphæðina og gjalddaga handvirkt á greiðsluseðilinn.   FIK 752 – Prenta FIK 752 greiðsluseðil ef ætlunin er að nota tölvugerðan greiðsluseðil sem er með fyrirframprentaða greiðsluupphæð og gjalddaga.  
16. Smellið á „Vista“.
17. Lokið síðunni.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]